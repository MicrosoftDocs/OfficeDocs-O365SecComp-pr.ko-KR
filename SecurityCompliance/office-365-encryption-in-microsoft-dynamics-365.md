---
title: Microsoft Dynamics 365에서 office 365 암호화
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 5/31/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: '요약: Microsoft Dynamics 365 암호화를 이해 합니다.'
ms.openlocfilehash: 181db1724f140c86fb1ac1dbf4a4bfb7063d25a3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532898"
---
# <a name="office-365-encryption-in-microsoft-dynamics-365"></a>Microsoft Dynamics 365에서 office 365 암호화

Microsoft은 Dynamics 365 나머지 사용자 장치 및 데이터 센터 간에 전송 되는 동안 및 Microsoft 데이터베이스에 동시에 고객 데이터를 보호 하기 위해 암호화 기술을 사용 합니다. 고객 및 Microsoft 데이터 센터 사이 설정 된 연결 암호화 되 고 업계 표준 TLS를 사용 하 여 모든 공용 끝점의 보안이 유지 됩니다. TLS는 효과적으로 데이터 기밀성 및 데스크톱 및 데이터 센터 간의 무결성을 보장 하기 보안이 향상 된 브라우저-서버 연결을 설정 합니다. 데이터 암호화 활성화 한 후 해당 해제할 수 없습니다. 자세한 내용은 [필드 수준 데이터 암호화](https://msdn.microsoft.com/en-us/library/dn481562.aspx)를 참조 하십시오.

Dynamics 365 사용자 이름 및 전자 메일 암호와 같은 중요 한 정보를 포함 하는 기본 엔터티 특성 집합에 대 한 표준 Microsoft SQL Server 셀 수준 암호화를 사용 합니다. 이 기능은 FIPS 140-2와 관련 된 규정 준수 요구 사항을 충족 하는 조직에서는 도움이 됩니다. 필드 수준 데이터 암호화는 [Microsoft Dynamics CRM 전자 메일 라우터](https://technet.microsoft.com/en-us/library/hh699800.aspx), 사용자 이름 및 Dynamics 365 인스턴스 및 전자 메일 서비스 간의 통합을 사용 하도록 설정 하려면 암호를 저장 해야 하는 활용 하는 경우에 특히 중요 합니다. 

Dynamics 365 모든 인스턴스 (나머지)에서 디스크에 기록 하는 경우에 데이터의 실시간 암호화를 수행 하려면 [Microsoft SQL Server 투명 한 데이터 암호화](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=sql-server-2017) (TDE)를 사용 합니다. TDE는 SQL Server, Azure SQL 데이터베이스 및 Azure SQL 데이터 웨어하우스에 데이터 파일을 암호화합니다. 기본적으로 Microsoft를 저장 하 고 프로그램 인스턴스의 Dynamics 365 대 한 데이터베이스 암호화 키를 관리 합니다. (Financials에 대 한 Dynamics 365 사용 되는 키를.NET Framework 데이터 보호 API에 의해 생성 됩니다.) 

Dynamics 365 관리 센터에서 관리 키 기능 자체 Dynamics 365 인스턴스와 연결 된 데이터베이스 암호화 키를 관리 하는 기능 관리자에 게 제공 합니다. (자체 관리 되는 데이터베이스 암호화 키는만 Microsoft Dynamics 365 년 1 월 2017 업데이트에서 사용할 수 있으며 하지 될 수 있습니다 이상 버전에 사용할 수 있습니다. 자세한 내용은 참조 [Dynamics 365 (온라인) 인스턴스에 대 한 암호화 키를 관리](https://docs.microsoft.com/dynamics365/customer-engagement/admin/manage-encryption-keys-instance)합니다.) 키 관리 기능에는 PFX 및 BYOK 암호화 키 파일을 모두, HSM에 저장 된 연결과 같이 지원 합니다. (생성 (영문) 및 인터넷을 통해 HSM로 보호 되는 키를 전송 하는 방법에 대 한 자세한 내용은 [생성 하 고 Azure 키 볼트에 대 한 HSM 암호로 보호 된 키를 전송 하는 방법](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)을 참조). 

업로드 암호화 키 옵션을 사용 하려면 공용 및 개인 암호화 키를 모두 필요 합니다.

키 관리 기능을 안전 하 게 암호화 키를 저장할 Azure 키 추적용을 사용 하 여 암호화 키 관리 로그 아웃 하는 복잡성을 수행 합니다. Azure 키 추적용 보호 암호화 키와 클라우드 응용 프로그램 및 서비스에서 사용 하는 비밀 하는데 도움이 됩니다. 키 관리 기능 Azure 키 추적용 구독 해야 하 고 대부분의 경우는 추적용 내에서 Dynamics 365 사용 되는 암호화 키에 액세스할 필요가 없습니다는 필요 하지 않습니다.
