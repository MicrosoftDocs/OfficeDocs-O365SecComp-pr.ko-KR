---
title: Microsoft 클라우드의 암호화
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
description: Microsoft 클라우드에서 암호화를 간략하게 설명 합니다.
ms.openlocfilehash: b8dee7ca7a791878763b885ada40a1d87f074e8e
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533916"
---
# <a name="encryption-in-the-microsoft-cloud"></a>Microsoft 클라우드의 암호화

Microsoft의 enterprise 클라우드 서비스 내에서 고객 데이터는 다양 한 기술 및 다양 한 형태의 암호화를 비롯 한 프로세스에 의해 보호 됩니다. (Exchange Online 사서함 콘텐츠를 포함 하는이 문서에서 office 365 고객 데이터 (전자 메일 본문, 일정 항목 및 전자 메일 첨부 파일의 콘텐츠 및 해당 되는 경우 비즈니스 콘텐츠 용 Skype), SharePoint Online 사이트 콘텐츠 및 내에 저장 된 파일 사이트 및 비즈니스 또는 Skype 비즈니스용 OneDrive에 업로드 된 파일입니다.) Microsoft를 사용 하 여 여러 암호화 방법, 프로토콜 및 암호화의 제품 및 서비스 간에 클라우드 서비스를 통해 이동 하 고 내에 저장 된 고객 데이터의 기밀을 보호 하는 고객 데이터에 대 한 보안 경로 제공 하는 데 도움이 클라우드 서비스입니다. Microsoft 고객 데이터를 무단으로 액세스에 대해 장애를 제공 하는 사용할 수 있는 가장 강력한, 가장 안전한 암호화 프로토콜의 일부를 사용 합니다. 적절 한 키 관리 암호화 모범 사례의 필수적인 요소 이기도 하 고 Microsoft에서는 Microsoft에서 관리 되는 암호화 키를 모두 보안이 제대로 되는지 확인 합니다.

고객 구성에 관계 없이 Microsoft의 enterprise 클라우드 서비스 내에 저장 하는 고객 데이터는 하나 이상의 형태의 암호화를 사용 하 여 보호 됩니다. (암호화 보호 정책 및 해당 적용의 유효성을 검사 하 여 여러 타사 감사자 독립적으로 확인 되 및 이러한 감사 보고서는 [포털을 신뢰 하는 서비스에서](https://aka.ms/stp)사용할 수 있습니다.)

Microsoft에서 전송 하 고 나머지 부분에서 고객 데이터를 암호화 하는 서비스 측 기술을 제공 합니다. 예, 나머지 부분에서 고객 데이터에 대 한 Microsoft Azure [BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) 및 [DM 암호화](https://en.wikipedia.org/wiki/Dm-crypt)사용 하 여 및 Microsoft Office 365 BitLocker, [Azure 저장소 서비스 암호화](https://azure.microsoft.com/documentation/articles/storage-service-encryption/), [분산 키 관리자](https://support.office.com/article/989ba10c-f73f-4efb-ad1b-af3322e5f376) (DKM) 및 Office 365 서비스를 사용 하 여 암호화 합니다. 전송 중에 고객 데이터, Azure, Office 365, Microsoft 상업용 지원, Microsoft Dynamics 365, Microsoft Power BI 및 Visual Studio Team Services 사용 인터넷 프로토콜 보안 (IPsec) 등의 업계 표준 보안 전송 프로토콜 및 Microsoft 데이터 센터 간의 및 사용자 장치 및 Microsoft 데이터 센터 간의 계층 보안 (TLS)를 전송 합니다.

초기 수준의 Microsoft에서 제공 하는 암호화 보안 외에도 클라우드 서비스도 관리할 수 있는 추가 암호화 옵션을 포함 합니다. 예 (Vm)가 Azure 가상 컴퓨터 및 사용자에 게 간의 트래픽에 대 한 암호화를 사용할 수 있습니다. [Azure 가상 네트워크](https://azure.microsoft.com/services/virtual-network/)회사 VPN 게이트웨이 및 Azure 가상 네트워크에 있는 Vm 사이와 같이 간의 트래픽을 암호화 하는 업계 표준 IPsec 프로토콜을 사용할 수 있습니다. 또한 또한 [새로운 Office 365 메시지 암호화 기능](set-up-new-message-encryption-capabilities.md) 을 사용 하면 모든 사용자에 게 암호화 된 메일을 보낼 수 있습니다.

Microsoft는 공용 키 인프라 운영 보안 표준, [Microsoft 보안 정책](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5868ecc8-50b7-4f91-b43f-640e2b99e86e&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ%20and%20White%20Papers)구성 요소인에 맞게 인증서에 대 한 Windows 운영 체제에 포함 된 암호화 기능을 활용 하 고 미국 정부 기관의 [연방 정보 처리 표준](http://csrc.nist.gov/publications/PubsFIPS.html) (FIPS) 140-2 표준을 충족 하는 암호화 모듈의 사용을 포함 하는 인증 메커니즘입니다. (Microsoft에 대 한 관련 NIST 인증서 번호에서 찾을 수 있습니다.http://csrc.nist.gov/groups/STM/cmvp/documents/140-1/1401vend.htm.)

> [메모] 자원으로 Microsoft 보안 정책에 액세스 하려면 사용자 작업이 나 교육용 계정을 사용 하 여 로그인 해야 합니다. 하지 않을 경우는 구독을 아직 [무료 평가판에 대 한 등록할 수 있습니다](https://servicetrust.microsoft.com/Home/TrialSubscriptions).

FIPS 140-2는 제품을 사용 하는 것이 아니라 암호화를 구현 하는 제품 모듈 유효성을 검사 하는데 위해 특별히 설계 된 표준입니다. 서비스 내에서 구현 되는 암호화 모듈 해시 강도, 키 관리와 유사한에 대 한 요구 사항을 충족으로 인증 될 수 있습니다. 암호화 기능 기밀성, 무결성 또는 Microsoft의 클라우드 서비스에서 데이터의 가용성을 보호 하기 위해 사용 되는 언제 든 지 모듈 및 암호화를 사용 하 여 FIPS 140-2 표준을 충족 합니다.

각 새 버전의 Windows 운영 체제와 클라우드 서비스에 사용 되는 원본으로 사용 되는 암호화 모듈을 인증 하는 Microsoft:
- Azure 및 Azure 미국 정부 기관
- Dynamics 365 및 Dynamics 365 미국 정부 기관
- Office 365, Office 365 미국 정부 및 Office 365 미국 정부 방어의 중요성

보관 된 Office 365 고객 데이터의 암호화 알려준 Exchange BitLocker, DKM, Azure 저장소 서비스 암호화 및 암호화 서비스를 포함 하는 여러 서비스 측 기술, Online, Skype 비즈니스용 OneDrive 비즈니스, 및 SharePoint에 대 한 온라인. Office 365 서비스 암호화 키 추적용 Azure에에서 저장 된 고객 관리 되는 암호화 키를 사용 하는 옵션을 포함 합니다. [Office 365 고객 키](https://support.office.com/article/f2cd475a-e592-46cf-80a3-1bfb0fa17697)를 호출 하이 고객 관리 키 옵션을은 Exchange Online, SharePoint Online, 비즈니스, 용 Skype 및 비즈니스용 OneDrive에 사용할 수 있습니다.

전송 중에 고객 데이터에 대 한 모든 Office 365 서버를 사용 하 여 TLS 기본적으로 클라이언트 컴퓨터와 고객 데이터를 보호 하는 보안 세션을 협상 합니다.  이 비즈니스, Outlook, 웹, 모바일 클라이언트 및 웹 브라우저에서 Outlook에 대 한 Skype와 같은 클라이언트에서 사용 되는 모든 장치에서 프로토콜에 적용 됩니다.

(기본적으로 TLS 1.2를 모든 고객 관련 서버 협상 하지만 것도 지원 낮은 표준까지 아래로 협상 필요한 경우.)

## <a name="related-links"></a>관련된 링크

- [Azure의 암호화](office-365-azure-encryption.md)
- [암호화에 대한 BitLocker 및 분산 키 관리자(DKM)](office-365-bitlocker-and-distributed-key-manager-for-encryption.md)
- [Office 365 서비스 암호화](office-365-service-encryption.md)
- [비즈니스, SharePoint Online, 및 Exchange Online에 대 한 개발자를 위한 비즈니스에 대 한 Skype, OneDrive office 365 암호화](office-365-encryption-for-skype-onedrive-sharepoint-and-exchange.md)
- [전송 중인 데이터 암호화](office-365-encryption-for-data-in-transit.md)
- [고객 관리 암호화 기능](office-365-customer-managed-encryption-features.md)
- [암호화 위험 및 보호](office-365-encryption-risks-and-protections.md)
- [Microsoft Dynamics 365에서 암호화](office-365-encryption-in-microsoft-dynamics-365.md)