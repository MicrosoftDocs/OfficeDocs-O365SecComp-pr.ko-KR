---
title: Office 365 관리 액세스 권한 컨트롤
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: '요약: Office 365 관리 액세스 제어 및 데이터 분류의 개요'
ms.openlocfilehash: afa15d37aa8542985c59dbd9e3d82368421530e8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533505"
---
# <a name="administrative-access-controls-in-office-365"></a>Office 365 관리 액세스 권한 컨트롤 

## <a name="introduction"></a>소개
Microsoft는 투자를 과도 하 게 하 고 그에 따라 시스템 및 의도적으로 고객 콘텐츠에 대 한 Microsoft의 액세스를 제한 하는 동안 대부분의 Office 365 작업을 자동화 하는 컨트롤에 있습니다. 휴먼은 서비스를 관리 및 서비스를 작동 하는 소프트웨어입니다. 이 Microsoft을 규모로, Office 365를 관리 하 고 고객 등의 콘텐츠 악의적인 작업자는 Microsoft 엔지니어 등의 창 피싱에 대 한 내부 위협의 위험을 관리할 수 있습니다.

기본적으로 Microsoft 엔지니어 0 순위 관리 권한 및 0 순위 액세스 권한이 고객 콘텐츠를 Office 365의 합니다. Microsoft 엔지니어 수 있는 제한, 감사, 및 보안에 대 한 액세스는 고객의 시간 제한 간격에 대 한 콘텐츠 하지만 서비스 작업에 대 한 필요한 경우에 및 Microsoft 고위 경영진의 (및는 고객을 위한 구성원에 의해 승인 하는 경우에 사용이 허가 된 고객 Lockbox 기능을 고객에 대 한)입니다.

Microsoft은 클라우드 배달의 여러 양식을 사용 하 여 Office 365를 포함 하는 온라인 서비스를 제공 합니다.

- **공용 클라우드** -다중 테 넌 트 버전의 Office 365, Azure, 및 북미, 남아메리카, 유럽, 아시아, 오스트레일리아 등에서 호스팅되는 다른 서비스를 포함 합니다.
- 예: (21Vianet에서 운영)는 중국에서 Office 365 및 Office 365 독일의 (제외 하 고 위에서 언급 한), 미국, 대한민국 외부의 모든 군주 하 여 제 3 자 운영 클라우드를 포함 하는 **국가 구름 모양** -(Microsoft에서 운영 하는 하지만 한 모델에서 독일어 데이터 트러스트를 받을 대상, 독일 Telekom 제어 및 고객 데이터 및 고객 데이터를 포함 하는 시스템에 대 한 Microsoft의 액세스를 모니터링 합니다.).
- **정부 구름 모양** -미국 정부 고객에 게 사용할 수 있는 Office 365와 Azure 서비스를 포함 합니다.

이 문서의 목적 Office 365 서비스는 [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online), [Exchange Online Protection](https://docs.microsoft.com/Office365/SecurityCompliance/eop/exchange-online-protection-overview), [SharePoint Online](https://docs.microsoft.com/sharepoint/sharepoint-online) ( [비즈니스용 OneDrive](https://docs.microsoft.com/OneDrive/onedrive)포함) 및 [Skype 비즈니스에 대 한](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online)추가 정보로 일부 [Yammer Enterprise](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US) 액세스 제어 하는 방법에 대 한 다른 Office 365 서비스를이 문서의 범위를 벗어났습니다.

## <a name="office-365-access-controls"></a>Office 365 액세스 제어
액세스 제어 목적을 위해 Office 365 데이터는 고객 데이터 또는 다른 데이터 형식으로 분류 됩니다. 고객 데이터를 또는 고객 콘텐츠 (직접 만든 또는 Office 365 사용자가 전자 메일, SharePoint Online 콘텐츠를 포함 하 여 인스턴트 메시지를 업로드 한 콘텐츠 등의 Office 365 서비스의 고객의 사용을 통해 고객을 대신 하 여 제공 하는 모든 데이터 일정 항목, 문서 및 Office 365에 저장 된 연락처) 및 최종 사용자 식별 정보 (EUII) (데이터를 사용자에 게 고유한 이거나 하는 개별 사용자에 게 연결 가능한 이지만 고객 콘텐츠가 포함 되지 않습니다). 

계정 데이터 (관리 데이터 자신이 등록 또는 서비스 구매 및 신용 등 지불 기기에 대 한 정보는 지불 데이터 카드 세부 정보 때 관리자가 제공 하는 정보를 포함)를 포함 하는 다른 종류의 데이터 조직적 식별 정보 (테 넌 트 행위를 식별 하는데 사용할 수 있는 데이터 또는 사용 현황 데이터, 개별 사용자에 게 연결 가능한 없는 하 고 고객 콘텐츠가 포함 되지 않습니다), 및 시스템 메타 데이터 (구성 설정을 포함 하는 서비스 로그를 포함 합니다. 시스템 상태, Microsoft IP 주소 및 구독 및 테 넌 트에 대 한 기술 정보).

Microsoft는 아무도 있는지 확인 하는 액세스 제어 메커니즘을 설정 하는 고객 데이터 또는 액세스 제어 데이터에 대 한 승인 되지 않은 액세스 (다른 종류의 데이터 나 고객 콘텐츠 또는 EUII;에 대 한 액세스를 포함 하 여 환경 내에서 기능에 대 한 액세스를 관리 하는데 사용 되는 것 Microsoft 암호, 보안 인증서 및 기타 인증 관련 데이터를 포함) 또는 Office 365 프로덕션 환경에 대 한 승인 되지 않은 물리적, 논리적, 또는 원격 액세스 합니다.

Microsoft에서 사용 하 여 Office 365를 운영 하는 것에 대 한 액세스 제어 세 범주로 그룹화 될 수 있습니다.
- 격리 컨트롤
- 담당자 컨트롤
- 기술 컨트롤

이 결합 하는 경우 이러한 컨트롤 방지 하 고 Office 365의 악의적인 작업 감지 도움이 됩니다. 격리, 담당자 및 Microsoft에서 사용 되는 기술 컨트롤 외에 컨트롤의 네번째 범주: 고객에서 구현 하는 것입니다.

Office 365를 사용 하면 온-프레미스 환경에서 관리 되는 동일한 방식으로 데이터의 대부분이 하 여 데이터를 관리할 수 있습니다. 사용자가 조직을 Office 365에 대 한 자동으로 전역 관리자 (admin) 됩니다. 전역 관리자 관리 포털 (예: 관리 센터 및 원격 PowerShell)에서 모든 기능에 액세스할 수 있는 및 수 만들거나 편집 사용자, 다른 사용자에 게 관리자 역할을 할당, 사용자 암호 다시 설정, 사용자 라이선스를 관리, 도메인을 관리 하 고 고객 Lockbox 승인 무엇 보다 요청 합니다. 조직 마다 적어도 두 관리자 계정을 지정 하 고 조직의 크기에 따라 서로 다른 기능 하는 여러 관리자를 지정 하려는 수는 것이 좋습니다. 관리 역할 및 사용 권한을 할당 하는 방법에 대 한 정보를 [Office 365에서 관리자 역할에 할당](https://support.office.com/article/Assigning-admin-roles-in-Office-365-eac4d046-1afd-4f1a-85fc-8219c79e1504) 하 고 [Office 365에 대 한 관리자 역할](https://support.office.com/article/Permissions-in-Office-365-DA585EEA-F576-4F55-A1E0-87090B6AAA9D)을 참조 하십시오.


## <a name="related-links"></a>관련된 링크

- [격리 컨트롤](office-365-isolation-controls.md)
- [담당자 컨트롤](office-365-personnel-controls.md)
- [기술 컨트롤](office-365-technology-controls.md)
- [액세스 제어 모니터링 및 감사](office-365-monitoring-and-auditing-access-controls.md)
- [Yammer Enterprise 액세스 제어](office-365-yammer-enterprise-access-controls.md)