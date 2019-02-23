---
title: Office 365 메시지 암호화 FAQ
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 02/11/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0432dce9-d9b6-4e73-8a13-4a932eb0081e
description: Office 365의 새 메시지 보호 기능이 작동 하는 방식에 대 한 질문이 있나요? 여기에서 대답을 확인 하세요.
ms.openlocfilehash: 651d3f5953f0a6864259ed3a0c8ecde79f40d631
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217118"
---
# <a name="office-365-message-encryption-faq"></a>Office 365 메시지 암호화 FAQ

Office 365의 새 메시지 보호 기능이 작동 하는 방식에 대 한 질문이 있나요? 여기에서 대답을 확인 하세요. 또한 azure information protection에서 데이터 보호 서비스, azure 권한 관리에 대 한 질문에 대 한 답변을 얻을 수 있도록 [azure information protection의 데이터 보호에 대 한](https://docs.microsoft.com/information-protection/get-started/faqs-rms) 질문과 대답을 확인 하세요.

||
|:-----|
|이 문서는 Office 365 메시지 암호화에 대 한 보다 광범위 한 문서에 포함 되어 있습니다. 이 문서는 관리자와 itpros 전문가를 위한 것입니다. 암호화 된 메시지를 보내거나 받는 방법에 대 한 정보를 찾으려는 경우에는 [Office 365 메시지 암호화 (OME)](ome.md) 의 문서 목록을 참조 하 여 요구 사항에 가장 적합 한 문서를 검색 하세요. |
||
  
## <a name="what-is-office-365-message-encryption-ome"></a>Office 365 메시지 암호화 란 무엇입니까 (OME)?

OME는 전자 메일 암호화 및 권한 관리 기능을 결합 합니다. 권한 관리 기능은 Azure Information Protection에 의해 구동 됩니다.
  
## <a name="who-can-use-ome"></a>누가 OME를 사용할 수 있나요?

다음 조건에서 OME의 새 기능을 사용할 수 있습니다.
  
- Office 365에서 Exchange Online에 대 한 OME 또는 IRM을 설정 하지 않은 경우
    
- OME 및 IRM을 설정한 경우 azure Information Protection에서 azure 권한 관리 서비스를 사용 하는 경우 다음 단계를 사용할 수 있습니다.
    
- AD RMS (Active Directory Rights Management services)와 함께 Exchange Online을 사용 하는 경우에는 이러한 새로운 기능을 즉시 사용 하도록 설정할 수 없습니다. 대신 [AD RMS를 Azure Information Protection로 마이그레이션](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) 해야 합니다. 마이그레이션이 완료 되 면 OME를 성공적으로 설정할 수 있습니다. 
    
    Azure Information Protection으로 마이그레이션하지 않고 Exchange Online에서 온-프레미스 AD RMS를 계속 사용 하도록 선택 하는 경우 이러한 새로운 기능을 사용할 수 없게 됩니다.
    
## <a name="what-subscriptions-do-i-need-to-use-the-new-ome-capabilities"></a>새 OME 기능을 사용 하는 데 필요한 구독은 무엇입니까?

새 OME 기능을 사용 하려면 다음 계획 중 하나가 필요 합니다.
  
- office 365 메시지 암호화는 office 365 Enterprise e3 및 e5, microsoft Enterprise e3 및 e5, microsoft 365 Business, office 365 A1, A3, A5 및 Office 365 정부 G3 및 G5의 일부로 제공 됩니다. 고객은 Azure Information protection에서 제공 하는 새로운 보호 기능을 수신 하기 위해 추가 라이선스가 필요 하지 않습니다. 
    
- 또한 다음 계획에 Azure Information Protection 계획 1을 추가 하 여 exchange online 계획 1, exchange online 계획 2, office 365 F1, office 365 business Essentials, office 365 business Premium 등의 새로운 Office 365 메시지 암호화 기능을 받을 수 있습니다. Office 365 Enterprise E1.
    
- Office 365 메시지 암호화에서 각 사용자 benefiting 기능을 사용 하도록 허가 받아야 합니다.
    
- 전체 목록은 Office 365 메시지 암호화에 대 한 [Exchange Online 서비스 설명을](https://technet.microsoft.com/library/exchange-online-service-description.aspx) 참조 하세요. 
    
## <a name="can-i-use-exchange-online-with-bring-your-own-key-byok-in-azure-information-protection"></a>Exchange Online을 사용 하 여 Azure Information Protection에서 직접 키 (byok)를 가져올 수 있나요?

예로! OME을 설정 하기 전에 시작 하기 전에 확인을 설정 하는 단계를 완료 하는 것이 좋습니다.
  
byok에 대 한 자세한 내용은 [Azure information Protection 테 넌 트 키 계획 및 구현](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key)를 참조 하세요.
  
## <a name="do-ome-and-byok-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Azure Information Protection을 사용 하 여 OME 및 byok를 수행 하 고, subpoenas와 같은 타사 데이터 요청에 대 한 Microsoft의 접근 방식을 변경 합니다.

아니요. OME 및 Azure Information Protection에서 byok 라는 자체 암호화 키를 제공 하 고 제어 하는 옵션은 사법 기관에 대응 하도록 설계 되지 않았습니다. Azure Information Protection에 대 한 byok를 사용 하는 OME는 준수 중심 고객을 위해 설계 되었습니다. Microsoft는 고객 데이터에 대 한 타사 요청을 매우 심각 하 게 수행 합니다. 클라우드 서비스 공급자는 항상 고객 데이터에 대 한 개인 정보를 제공 합니다. 소환장이 발생 하는 경우에는 항상 제 3 자가 고객에 게 리디렉션되어 정보를 얻도록 시도 합니다. (정부 Smith의 블로그에서 [고객 데이터 보호 스누핑](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/))를 읽어 보십시오. 받은 요청의 세부 정보를 주기적으로 게시 합니다. 타사 데이터 요청에 대 한 자세한 내용은 Microsoft 보안 센터에서 [고객 데이터에 액세스 하기 위해 정부 및 법 집행 요청에 응답](https://www.microsoft.com/en-us/trustcenter/privacy/govt-requests-for-data) 을 참조 하세요. 또한 [OST (온라인 서비스 약관)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx)에서 "고객 데이터 공개"를 참조 하세요.
  
## <a name="how-is-this-feature-related-to-legacy-office-365-message-encryption-ome-and-information-rights-management-irm-features"></a>이 기능은 어떻게 레거시 Office 365 메시지 암호화 (OME) 및 IRM (정보 권한 관리) 기능과 관련 되어 있습니까?

Office 365 메시지 암호화에 대 한 새로운 기능은 기존 IRM 및 레거시 OME 솔루션의 발전 사항입니다. 다음 표에서는 자세한 정보를 제공 합니다.
  
**레거시 OME, IRM 및 새로운 OME 기능 비교**

|**기능**|**이전 버전의 OME**|**IRM**|**새로운 OME 기능**|
|:-----|:-----|:-----|:-----|
|**암호화 된 전자 메일 보내기**|Exchange 메일 흐름 규칙만을 통해서만|최종 사용자가 PC 용 outlook, Mac 용 outlook 또는 웹용 outlook에서 시작 되었습니다. 또는 Exchange 메일 흐름 규칙을 통해|최종 사용자가 PC 용 outlook, Mac 용 outlook 또는 웹용 outlook에서 시작 되었습니다. 또는 메일 흐름 규칙을 통해|
|**권한 관리**|-|전달 금지 옵션 및 사용자 지정 서식 파일|전달 금지 옵션, 암호화 전용 옵션, 기본 및 사용자 지정 템플릿|
|**지원 되는 받는 사람 유형**|외부 받는 사람만|내부 받는 사람만|내부 및 외부 받는 사람|
|**받는 사람에 대 한 경험**|외부 받는 사람이 브라우저 또는 다운로드 된 모바일 앱에서 다운로드 하 여 연 HTML 메시지를 수신 했습니다.|내부 받는 사람만 outlook for PC, outlook for Mac 및 웹용 outlook에서 암호화 된 전자 메일을 수신 합니다.|내부 및 외부 받는 사람이 outlook for PC, outlook for Mac, 웹용 outlook, Android 용 outlook, 웹에서 outlook, 타사에 있는지 여부에 관계 없이 웹 포털을 통해 전자 메일을 받습니다. 조직. OME 포털에는 별도의 다운로드를 수행 하지 않아도 됩니다.|
|**고유한 키를 제공 합니다.**|사용할 수 없음|사용할 수 없음| byok 지원 됨|

## <a name="how-do-i-enable-the-new-ome-capabilities-for-my-organization"></a>조직에 대해 새 OME 기능을 사용 하도록 설정 하려면 어떻게 해야 하나요?

[새 Office 365 메시지 암호화 기능 설정을](set-up-new-message-encryption-capabilities.md)참조 하세요.
  
## <a name="will-the-previous-version-of-ome-be-deprecated"></a>이전 버전의 OME는 더 이상 사용 되지 않을 예정 입니까?

이전 버전의 OME를 사용할 수는 있지만 현재는 더 이상 사용 되지 않습니다. 그러나 조직은 신규 및 향상 된 OME 솔루션을 사용 하는 것이 매우 권장 됩니다. 아직 OME을 배포 하지 않은 고객은 이전 버전의 OME를 새로 배포 하는 것을 설정할 수 없습니다.
  
## <a name="my-organization-uses-active-directory-rights-management-can-i-use-this-functionality"></a>조직에서 Active Directory Rights Management를 사용 하 여이 기능을 사용할 수 있나요?

아니요. AD RMS (Active Directory Rights Management services)와 함께 Exchange Online을 사용 하는 경우에는 이러한 새로운 기능을 즉시 사용 하도록 설정할 수 없습니다. 대신 [AD RMS를 Azure Information Protection로 마이그레이션](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) 해야 합니다. 
  
## <a name="my-organization-has-an-exchange-hybrid-deployment-can-i-use-this-feature"></a>조직에 Exchange 하이브리드 배포를 포함 하는 경우 이 기능을 사용할 수 있나요?

온-프레미스 사용자는 Exchange Online 메일 흐름 규칙을 사용 하 여 암호화 된 메일을 보낼 수 있습니다. 이렇게 하려면 Exchange Online을 통해 전자 메일을 라우트 해야 합니다. 자세한 내용은 [2 부: 전자 메일 서버에서 Office 365으로 이동 하도록 메일 구성](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365)를 참조 하세요.
  
## <a name="what-email-client-do-i-need-to-use-in-order-to-create-an-ome-encrypted-message-what-applications-are-supported-for-sending-protected-messages"></a>OME 암호화 메시지를 만들기 위해 어떤 전자 메일 클라이언트를 사용 해야 하나요? 보호 된 메시지를 보내는 데 지원 되는 응용 프로그램은 무엇입니까?

outlook 2016, outlook 2013 for PC 및 Mac 및 웹용 outlook에서 보호 된 메시지를 만들 수 있습니다.
  
## <a name="what-email-clients-are-supported-to-read-and-reply-to-protected-emails"></a>보호 된 전자 메일을 읽고 회신할 수 있도록 지원 되는 전자 메일 클라이언트는 무엇입니까?

PC 및 Mac 용 outlook, 웹용 outlook 및 Office 365 사용자 인 경우 outlook mobile (Android 및 iOS)을 읽고 응답할 수 있습니다. 조직에서 허용 하는 경우 iOS 기본 메일 클라이언트도 사용할 수 있습니다. Office가 아닌 경우에는 사용자가 웹 브라우저를 통해 웹에서 암호화 된 메시지를 읽고 회신할 수 있습니다.
  
## <a name="what-file-types-are-supported-as-attachments-in-protected-emails-do-attachments-inherit-the-protection-policies-associated-with-protected-emails"></a>보호 된 전자 메일에서 첨부 파일로 지원 되는 파일 형식은 무엇입니까? 첨부 파일에서 보호 된 전자 메일과 연결 된 보호 정책을 상속 하나요?

보호 된 메일에 모든 파일 형식을 첨부할 수 있지만 보호 정책은 [여기](https://docs.microsoft.com/information-protection/rms-client/client-admin-guide-file-types)에 언급 된 파일 형식에만 적용 됩니다. 
  
Word, Excel 또는 PowerPoint 파일과 같은 파일 형식이 지원 되는 경우 받는 사람이 첨부 파일을 다운로드 한 후에도 파일이 항상 보호 됩니다. 예를 들어 첨부 파일이 전달 하지 않도록 보호 되 고 원래 받는 사람이 첨부 파일을 다운로드 하 여 새 받는 사람에 게 전달 하는 경우 새 받는 사람은 보호 된 파일을 열 수 없게 됩니다.
  
## <a name="are-pdf-file-attachments-supported"></a>PDF 파일이 첨부 파일을 지원 하나요?

보호 된 메시지에 PDF 파일을 첨부 하는 경우 메시지 자체는 보호 되지만 받는 사람이 받은 후에 추가 보호는 pdf 파일에 적용 되지 않습니다. 즉, 받는 사람은 PDF 파일을 다른 이름으로 저장, 전달, 복사 및 인쇄할 수 있습니다.
  
## <a name="are-onedrive-for-business-attachments-supported"></a>비즈니스용 OneDrive 첨부 파일이 지원 됩니까?

아직 아니에요. 비즈니스용 onedrive 첨부 파일이 지원 되지 않으며 최종 사용자가 비즈니스용 onedrive 첨부 파일을 포함 하는 메일을 암호화할 수 없습니다.
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies"></a>정책을 설정 하 여 메시지를 자동으로 암호화할 수 있습니까?

예로. Exchange Online의 메일 흐름 규칙을 사용 하 여 특정 조건에 따라 메시지를 자동으로 암호화 합니다. 예를 들어 받는 사람 ID, 받는 사람 도메인을 기반으로 하거나 메시지의 본문 또는 제목에 있는 콘텐츠를 사용 하 여 정책을 만들 수 있습니다. [Office 365에서 전자 메일 메시지를 암호화 하기 위한 메일 흐름 규칙 정의를](define-mail-flow-rules-to-encrypt-email.md) 참조 하세요.
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies-in-data-loss-prevention-dlp-through-the-security-amp-compliance-center"></a>보안 &amp; 및 준수 센터를 통해 DLP (데이터 손실 방지)에서 정책을 설정 하 여 메시지를 자동으로 암호화할 수 있습니까?

예로! 메일 흐름 규칙은 Exchange Online에서 설정 하거나, 보안 &amp; 및 준수 센터에서 DLP를 사용 하 여 설정할 수 있습니다.
  
## <a name="can-i-open-encrypted-messages-sent-to-a-shared-mailbox"></a>공유 사서함으로 보낸 암호화 된 메시지를 열 수 있습니까?

현재 암호화 된 메시지는 공유 사서함에 대해 지원 되지 않습니다.

## <a name="can-i-customize-encrypted-messages-with-my-company-branding"></a>회사 브랜딩을 사용 하 여 암호화 된 메시지를 사용자 지정할 수 있습니까?

예로! 전자 메일 메시지 및 OME 포털을 사용자 지정 하는 방법에 대 한 자세한 내용은 암호화 된 메시지에 조직의 브랜드 추가를 참조 하세요. [암호화 된 메시지에 조직의 브랜드 추가를](add-your-organization-brand-to-encrypted-messages.md) 참조 하세요.
  
## <a name="are-there-any-reporting-capabilities-or-insights-for-encrypted-emails"></a>암호화 된 전자 메일에 대 한 보고 기능 또는 정보가 있습니까?

현재는 아니지만 곧 제공 될 예정입니다.
  
## <a name="can-i-use-message-encryption-with-compliance-features-such-as-ediscovery"></a>eDiscovery와 같은 규정 준수 기능을 사용 하 여 메시지 암호화를 사용할 수 있나요?

예로. 모든 암호화 된 전자 메일 메시지는 Office 365 규정 준수 기능을 통해 검색할 수 있습니다.
  

