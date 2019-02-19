---
title: Microsoft 클라우드의 암호화
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Microsoft 클라우드의 암호화 개요
ms.openlocfilehash: 75ed88d4755ab37f03b4821125e175a66015afa8
ms.sourcegitcommit: 24659bdb09f49d0ffed180a4b80bbb7c45c2d301
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/19/2019
ms.locfileid: "29664134"
---
# <a name="encryption-in-the-microsoft-cloud"></a>Microsoft 클라우드의 암호화

Microsoft 엔터프라이즈 클라우드 서비스 내의 고객 데이터는 다양 한 암호화 형식을 비롯 하 여 다양 한 기술과 프로세스에 의해 보호 됩니다. (이 문서의 Office 365 고객 데이터에는 Exchange Online 사서함 콘텐츠 (전자 메일 본문, 일정 항목 및 전자 메일 첨부 파일의 콘텐츠, 해당 되는 경우 비즈니스용 Skype 콘텐츠), SharePoint online 사이트 콘텐츠 및 파일에 저장 된 파일이 포함 됩니다. 비즈니스용 OneDrive 또는 비즈니스용 Skype에 업로드 되는 사이트 및 파일 Microsoft는 자사 제품 및 서비스에서 여러 암호화 방법, 프로토콜 및 암호를 사용 하 여 고객 데이터에 대 한 안전한 경로를 클라우드 서비스를 통해 전달 하 고, 고객 데이터의 기밀성을 보호 하는 데 도움을 줍니다. 클라우드 서비스 Microsoft는 고객 데이터에 대 한 무단 액세스에 대 한 장애물을 제공 하기 위해 가장 강력 하 고 보안 암호화 프로토콜 중 일부를 사용 합니다. 적절 한 키 관리는 암호화 모범 사례에도 중요 한 요소 이며, microsoft는 모든 microsoft 관리 암호화 키가 제대로 보호 되도록 하기 위해 작동 합니다.

고객 구성에 관계 없이 Microsoft의 엔터프라이즈 클라우드 서비스 내에 저장 된 고객 데이터는 하나 이상의 암호화 형식을 사용 하 여 보호 됩니다. (암호화 정책에 대 한 유효성 검사 및 해당 적용은 여러 타사 감사자에 의해 독립적으로 확인 되며, 이러한 감사에 대 한 보고서는 [서비스 트러스트 포털](https://aka.ms/stp)에서 사용할 수 있습니다.)

Microsoft는 전송 중에 고객 데이터를 암호화 하는 서비스 쪽 기술을 제공 합니다. 예를 들어 나머지 고객 데이터의 경우 microsoft Azure는 [bitlocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) 및 [DM-자리](https://en.wikipedia.org/wiki/Dm-crypt)를 사용 하며, microsoft Office 365에서는 bitlocker, [Azure Storage Service Encryption](https://azure.microsoft.com/documentation/articles/storage-service-encryption/), DKM ( [분산 키 관리자](https://support.office.com/article/989ba10c-f73f-4efb-ad1b-af3322e5f376) ) 및 Office 365 서비스를 사용 합니다. encryption. 전송, Azure, Office 365, microsoft 상업용 지원, microsoft Dynamics 365, microsoft Power BI 및 Visual Studio Team Services에서는 IPsec (인터넷 프로토콜 보안)과 같은 업계 표준 보안 전송 프로토콜을 사용 하는 고객 데이터를 제공 합니다. microsoft 데이터 센터와 사용자 장치 및 Microsoft 데이터 센터 간의 TLS (전송 계층 보안)

클라우드 서비스에는 Microsoft에서 제공 하는 암호화 보안의 기본 수준 외에도 관리할 수 있는 추가 암호화 옵션도 포함 되어 있습니다. 예를 들어 Azure vm (가상 컴퓨터)과 해당 사용자 간의 트래픽에 대해 암호화를 사용 하도록 설정할 수 있습니다. [Azure 가상 네트워크](https://azure.microsoft.com/services/virtual-network/)를 사용 하는 경우 업계 표준 IPsec 프로토콜을 통해 회사 VPN 게이트웨이와 Azure와 가상 네트워크에 있는 vm 간에 트래픽을 암호화할 수 있습니다. 또한 [새로운 Office 365 메시지 암호화 기능](set-up-new-message-encryption-capabilities.md) 을 사용 하면 모든 사용자에 게 암호화 된 메일을 보낼 수 있습니다.

[microsoft 보안 정책의](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5868ecc8-50b7-4f91-b43f-640e2b99e86e&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ%20and%20White%20Papers)구성 요소인 공개 키 인프라 작동 보안 표준에 따라 microsoft는 인증서에 대해 Windows 운영 체제에 포함 된 암호화 기능을 활용 하 고 미국 정부의 FIPS ( [연방 정보 처리 표준](http://csrc.nist.gov/publications/PubsFIPS.html) ) 140-2 표준을 충족 하는 암호화 모듈을 사용 하는 인증 메커니즘 (Microsoft에 대 한 관련 NIST 인증서 번호는 다음 위치에서 찾을 수 있습니다.http://csrc.nist.gov/groups/STM/cmvp/documents/140-1/1401vend.htm.)

> 참고 Microsoft 보안 정책에 리소스로 액세스 하려면 회사 또는 학교 계정을 사용 하 여 로그인 해야 합니다. 아직 구독 하지 않는 경우 [무료 평가판에 등록할 수](https://servicetrust.microsoft.com/Home/TrialSubscriptions)있습니다.

FIPS 140-2은이를 사용 하는 제품이 아닌 암호화를 구현 하는 제품 모듈의 유효성을 검사 하기 위해 특별히 설계 된 표준입니다. 서비스 내에서 구현 되는 암호화 모듈은 해시 수준, 키 관리 등에 대 한 요구 사항을 충족 하는 것으로 인증 될 수 있습니다. Microsoft의 클라우드 서비스에서 데이터의 기밀성, 무결성 또는 가용성을 보호 하기 위해 암호화 기능을 모두 사용 하는 경우에는 FIPS 140-2 표준을 충족 하는 모듈과 암호를 사용할 수 있습니다.

Microsoft는 클라우드 서비스에서 사용 되는 기본 암호화 모듈을 각각의 Windows 운영 체제에 대 한 새로운 릴리스로 인증 합니다.
- azure 및 azure 미국 정부
- dynamics 365 및 dynamics 365 미국 정부
- office 365, office 365 미국 정부 및 office 365 미국 정부 방어

Office 365 고객 데이터의 암호화 기능은 BitLocker, DKM, Azure Storage service encryption, Exchange Online의 서비스 암호화, 비즈니스용 Skype, 비즈니스용 OneDrive, SharePoint 등의 여러 서비스 쪽 기술에서 제공 됩니다. 온라인. Office 365 서비스 암호화에는 Azure 키 자격 증명 모음에 저장 되는 고객 관리 암호화 키를 사용 하는 옵션이 포함 되어 있습니다. [Office 365 고객 키](https://support.office.com/article/f2cd475a-e592-46cf-80a3-1bfb0fa17697)라는이 고객 관리 키 옵션은 Exchange online, SharePoint online, 비즈니스용 Skype 및 비즈니스용 OneDrive에 사용할 수 있습니다.

전송 중인 고객 데이터의 경우 모든 Office 365 서버가 클라이언트 컴퓨터와 기본적으로 TLS를 사용 하 여 보안 세션을 협상 하 여 고객 데이터를 보호 합니다.  이는 웹, 모바일 클라이언트 및 웹 브라우저에서 비즈니스용 Skype, outlook 및 outlook과 같은 클라이언트에서 사용 하는 모든 장치의 프로토콜에 적용 됩니다.

기본적으로 모든 고객 연결 서버는 TLS 1.2로 협상 하지만 필요한 경우 낮은 표준으로 협상 하는 것도 지원 합니다.

## <a name="related-links"></a>관련 링크

- [Azure의 암호화](office-365-azure-encryption.md)
- [암호화에 대한 BitLocker 및 분산 키 관리자(DKM)](office-365-bitlocker-and-distributed-key-manager-for-encryption.md)
- [Office 365 서비스 암호화](office-365-service-encryption.md)
- [비즈니스용 Skype, 비즈니스용 OneDrive, SharePoint online 및 Exchange Online에 대 한 Office 365 암호화](office-365-encryption-for-skype-onedrive-sharepoint-and-exchange.md)
- [전송 중인 데이터 암호화](office-365-encryption-for-data-in-transit.md)
- [고객 관리 암호화 기능](office-365-customer-managed-encryption-features.md)
- [암호화 위험 및 보호](office-365-encryption-risks-and-protections.md)
- [Microsoft Dynamics 365에서 암호화](office-365-encryption-in-microsoft-dynamics-365.md)