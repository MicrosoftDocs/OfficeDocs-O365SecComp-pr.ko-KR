---
title: Office 365의 암호화
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/15/2019
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 0a322724-08ca-43db-b69a-afbfa20484cd
ms.collection:
- M365-security-compliance
- Strat_O365_IP
description: Office 365에서는 콘텐츠가 rest에서 암호화 되 고 가장 강력한 암호화, 프로토콜 및 기술이 제공 된 상태로 전송 됩니다. Office 365의 암호화에 대 한 개요를 가져옵니다.
ms.openlocfilehash: 1dd31990e4a284c81ce9fa8b2aced45b8a06a0c6
ms.sourcegitcommit: 01f827d7a3fe6d982924cabb0bcc8d6a19ecc57c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/16/2019
ms.locfileid: "36436298"
---
# <a name="encryption-in-office-365"></a>Office 365의 암호화

암호화는 파일 보호 및 정보 보호 전략의 중요 한 부분입니다. 이 문서에서는 Office 365의 암호화에 대 한 개요를 제공 합니다. 조직에 대 한 암호화 설정 방법과 같은 암호화 작업과 Office 문서를 암호로 보호 하는 방법에 대 한 도움말을 볼 수 있습니다.
  
- TLS와 같은 인증서 및 기술에 대 한 자세한 내용은 [Office 365의 암호화에 대 한 기술 참조 세부 정보](technical-reference-details-about-encryption.md)를 참조 하세요.

- 조직에 대 한 암호화를 구성 하거나 설정 하는 방법에 대 한 자세한 내용은 [set up encryption In Office 365 Enterprise](set-up-encryption.md)를 참조 하세요.

## <a name="what-is-encryption-and-how-does-it-work-in-office-365"></a>암호화는 무엇 이며, Office 365에서 어떤 방식으로 작동 하나요?

암호화 프로세스에서는 일반 텍스트를 의미 하는 데이터를 암호 텍스트에 인코딩합니다. 일반 텍스트와 달리 암호 해독은 사용자 또는 컴퓨터에서 사용할 수 없습니다. 암호 해독에는 인증 된 사용자만 있으면 서 암호화 키가 필요 합니다. 암호화를 사용 하면 인증 된 받는 사람만 콘텐츠를 해독할 수 있습니다. 콘텐츠에는 파일, 전자 메일 메시지, 일정 항목 등이 포함 됩니다.
  
암호화는 콘텐츠 가로채기를 차단 하지 않습니다. 암호화는 조직에 대 한 보다 큰 정보 보호 전략의 일부입니다. 암호화를 사용 하면 권한 있는 사용자만 암호화 된 데이터를 사용할 수 있습니다.
  
동시에 여러 계층의 암호화를 적용할 수 있습니다. 예를 들어 전자 메일을 전송 하는 데 사용할 통신 채널과 전자 메일 메시지를 암호화할 수 있습니다. Office 365을 사용 하는 경우 데이터가 rest와 전송에서 암호화 되 고, 전송 계층 보안/보안 소켓 계층 (TLS/SSL), IPSec (인터넷 프로토콜 보안) 및 고급 암호화를 포함 하는 기술을 사용 하는 경우 표준 (AES)
  
## <a name="encryption-for-data-at-rest-and-data-in-transit"></a>휴지 및 전송 중인 데이터에 대 한 암호화

 **휴지 상태의 데이터** 에는 SharePoint 라이브러리에 업로드 한 파일, Project Online 데이터, 비즈니스용 Skype 모임에서 업로드 한 문서, Office 365의 폴더에 저장 한 전자 메일 메시지 및 첨부 파일이 포함 됩니다. 사서함 및 비즈니스용 OneDrive에 업로드 한 파일
  
 **전송 중인 데이터의 예로** 는 배달 중인 메일 메시지 또는 온라인 모임에서 발생 하는 대화 등이 있습니다. Office 365에서 사용자의 장치가 Office 365 서버와 통신 하거나 Office 365 서버가 다른 서버와 통신 하는 경우 데이터가 전송 중입니다.
  
Office 365에서는 여러 계층 및 암호화 종류를 함께 사용 하 여 데이터를 보호 합니다. 다음 표에는 추가 정보에 대 한 링크가 포함 된 몇 가지 예가 나와 있습니다.
  
|**콘텐츠 종류**|**암호화 기술**|**자세한 정보를 볼 수 있는 리소스**|
|:-----|:-----|:-----|
|장치에 있는 파일 이러한 파일에는 폴더에 저장 된 전자 메일 메시지, 컴퓨터, 태블릿 또는 휴대폰에 저장 된 Office 문서, Microsoft 클라우드에 저장 된 데이터가 포함 될 수 있습니다.  <br/> |Microsoft 데이터 센터의 BitLocker BitLocker는 Windows 컴퓨터 및 태블릿과 같은 클라이언트 컴퓨터 에서도 사용할 수 있습니다.  <br/> Microsoft 데이터 센터의 DKM (분산 키 관리자)  <br/> Office 365에 대한 고객 키  <br/> |[Windows IT 센터: BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) <br/> [Microsoft 보안 센터: 암호화](https://www.microsoft.com/en-us/TrustCenter/Security/Encryption) <br/> [클라우드 보안 컨트롤 계열: 휴지에서 데이터 암호화](https://blogs.microsoft.com/microsoftsecure/2015/09/10/cloud-security-controls-series-encrypting-data-at-rest) <br/> [Exchange Online이 전자 메일 암호를 보호하는 방법](exchange-online-secures-email-secrets.md) <br/> [고객 키를 사용하여 Office 365에서 데이터 제어](controlling-your-data-using-customer-key.md) <br/> |
|사용자 간 전송 중인 파일 이러한 파일에는 사용자 간에 공유 되는 Office 문서 또는 SharePoint 목록 항목이 포함 될 수 있습니다.  <br/> |전송 중인 파일에 대 한 TLS  <br/> |[비즈니스용 OneDrive 및 SharePoint Online에서의 데이터 암호화](data-encryption-in-odb-and-spo.md) <br/> [비즈니스용 Skype Online: 보안 및 보관](https://technet.microsoft.com/library/skype-for-business-online-security-and-archiving.aspx) <br/> |
|받는 사람 간 전송 되는 전자 메일입니다. 이 전자 메일에는 Exchange Online에서 호스팅하는 전자 메일이 포함 됩니다.  <br/> |전송 중인 전자 메일에 대 한 Azure 권한 관리, S/MIME 및 TLS를 사용한 Office 365 메시지 암호화  <br/> |[Office 365 메시지 암호화 (OME)](ome.md) <br/> [Office 365의 전자 메일 암호화](email-encryption.md) <br/> [Office 365의 전자 메일 연결 보안을 위해 Exchange Online에서 TLS를 사용하는 방법](exchange-online-uses-tls-to-secure-email-connections.md) <br/> |

## <a name="what-if-i-need-more-control-over-encryption-to-meet-security-and-compliance-requirements"></a>보안 및 규정 준수 요구 사항을 충족 하기 위해 암호화를 보다 강력 하 게 제어 해야 하는 경우

Office 365에서는 Office 365에서 볼륨 암호화, 파일 암호화 및 사서함 암호화를 위한 Microsoft managed 솔루션을 제공 합니다. 또한 Office 365에서는 관리 및 제어할 수 있는 암호화 솔루션을 제공 합니다. 이러한 암호화 솔루션은 Azure를 기반으로 구축 됩니다.
  
자세한 내용은 다음 리소스를 참조 하십시오.
  
- [Azure 권한 관리 란?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)

- [관리 센터에서 권한 관리 활성화](https://support.office.com/article/5b6d3ac7-b1ac-428e-b03e-50e882f85a6e)

- [Set up Information Rights Management (IRM) in SharePoint admin center](set-up-irm-in-sp-admin-center.md)

- [고객 키를 사용하여 Office 365에서 데이터 제어](controlling-your-data-using-customer-key.md)

## <a name="how-do-i"></a>방법 ...

|**이 작업을 수행 하려면**|**다음 리소스를 참조 하세요.**|
|:-----|:-----|
|조직에 대 한 암호화 설정  <br/> |[Office 365 Enterprise의 암호화 설정](set-up-encryption.md) <br/> |
|Office 365의 인증서, 기술 및 TLS 암호 도구에 대 한 세부 정보 보기  <br/> |[Office 365의 암호화에 대 한 기술 세부 정보](technical-reference-details-about-encryption.md) <br/> |
|모바일 장치에서 암호화 된 메시지 작업  <br/> |[Android 장치에서 암호화 된 메시지 보기](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> [IPhone 또는 iPad에서 암호화 된 메시지 보기](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |
|암호 보호를 사용 하 여 문서 암호화  <br/><br/>  암호 보호는 브라우저의 Office 365에서 지원 되지 않습니다. 데스크톱 버전의 Word, Excel 및 PowerPoint를 암호 보호에 사용 합니다. |[문서, 통합 문서 또는 프레젠테이션에서 보호 기능 추가 또는 제거](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) <br/> **보호 추가** 섹션을 선택한 다음 **암호를 사용 하 여 암호화**를 확인 합니다.  |
|문서에서 암호화 제거  <br/> |[문서, 통합 문서 또는 프레젠테이션에서 보호 기능 추가 또는 제거](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) <br/> **보호 제거** 섹션을 선택 하 고 **암호 암호화 제거**를 참조 하세요.  |

## <a name="related-topics"></a>관련 항목

[Office 365 보안 및 정보 보호 기능 계획](plan-for-security-and-compliance.md)

[Office 365 및 Microsoft 365 비즈니스 요금제를 보호 하는 10 가지 주요 방법](https://docs.microsoft.com/office365/admin/security-and-compliance/secure-your-business-data?view=o365-worldwide)
