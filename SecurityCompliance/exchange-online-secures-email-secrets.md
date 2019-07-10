---
title: How Exchange Online secures your email secrets
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 07/01/2019
audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 989ba10c-f73f-4efb-ad1b-af3322e5f376
ms.collection:
- M365-security-compliance
description: Office 365의 보안, 개인 정보 및 규정 준수 정보를 제공 하는 Office 365 보안 센터 외에 Office 365에서 데이터 센터에 제공 하는 비밀을 보호 하는 방법을 알고 싶을 수 있습니다. DKM (Distributed Key Manager) 라는 기술을 사용 합니다.
ms.openlocfilehash: 8350785968c68b22c58be17ec68d94ff908c95d9
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599434"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a>How Exchange Online secures your email secrets

이 문서에서는 Microsoft가 데이터 센터에서 사용자의 전자 메일 암호를 보호하는 방법을 서명합니다.
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a>사용자가 제공한 암호 정보는 어떻게 보호됩니까?

Office [365의 보안, 개인 정보 및 규정 준수 정보](https://go.microsoft.com/fwlink/?linkid=874644)를 제공 하는 Office 365 보안 센터 외에 office 365에서 데이터 센터에 제공 하는 비밀을 보호 하는 방법을 알고 싶을 수 있습니다. DKM (Distributed Key Manager) 라는 기술을 사용 합니다.
  
[배포 된 키 관리자](office-365-bitlocker-and-distributed-key-manager-for-encryption.md) (DKM)는 비밀 키 집합을 사용 하 여 정보를 암호화 하 고 암호를 해독 하는 클라이언트 쪽 기능입니다. Active Directory 도메인 서비스에서 특정 보안 그룹의 구성원만 DKM으로 암호화된 데이터를 해독하기 위해 해당 키에 액세스할 수 있습니다. Exchange Online에서는 Exchange 프로세스가 실행되는 특정 서비스 계정만 해당 보안 그룹에 속합니다. 데이터 센터의 표준 운영 절차의 일부로, 이 보안 그룹에 속하는 사용자에게 자격 증명이 제공되지 않으므로 이러한 암호를 해독할 수 있는 키에 액세스할 수 없습니다.
  
디버깅, 문제 해결 또는 감사 목적으로, 데이터 센터 관리자는 보안 그룹에 속하는 임시 자격 증명을 획득하기 위해 승격된 액세스 권한을 요청해야 합니다. 이 프로세스에는 여러 수준의 법적 승인이 필요합니다. 액세스가 허용되면 모든 작업이 기록되고 감사됩니다. 또한 액세스 권한은 설정된 시간 간격 동안만 부여되며 그 이후에는 자동으로 만료됩니다.
  
추가 보호를 위해 DKM 기술에는 자동화된 키 롤오버 및 보관 기능이 포함됩니다. 따라서 동일한 키를 무제한으로 사용하지는 않으면서 이전 콘텐츠에 계속 액세스할 수 있습니다.
  
## <a name="where-does-exchange-online-make-use-of-dkm"></a>Exchange Online은 어디에서 DKM을 사용합니까?

Microsoft는 [분산 키 관리자](office-365-bitlocker-and-distributed-key-manager-for-encryption.md) 를 사용 하 여 Exchange Online 데이터 센터에서 비밀을 암호화 합니다. 예를 들면 다음과 같습니다.
  
- 연결된 계정에 대한 전자 메일 계정 자격 증명. 연결된 계정은 Hotmail, Gmail 및 yahoo! 메일 계정과 같은 타사 계정입니다.
    
- 고객 키 [Office 365에서 고객 키](controlling-your-data-using-customer-key.md)를 사용 하는 경우 [Azure 키 자격 증명 모음](https://docs.microsoft.com/azure/key-vault/key-vault-whatis) 을 사용 하 여 비밀을 보호 합니다.
    
## <a name="related-topics"></a>관련 항목

[Office 365의 암호화](encryption.md)
  
[Office 365의 암호화에 대한 기술 관련 세부 정보](technical-reference-details-about-encryption.md)
  
[Office 365 보안 &amp; 및 준수 센터의 서비스 보증](https://go.microsoft.com/fwlink/?linkid=874645)
  

