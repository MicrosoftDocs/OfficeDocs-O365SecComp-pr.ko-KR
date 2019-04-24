---
title: Office 365 메시지 암호화
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/6/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f87cb016-7876-4317-ae3c-9169b311ff8a
description: Office 365 메시지 암호화를 사용 하면 조직에서 조직 내부 및 외부의 사용자 간에 암호화 된 전자 메일 메시지를 보내고 받을 수 있습니다. 전자 메일 메시지 암호화는 의도 된 받는 사람만 메시지 콘텐츠를 볼 수 있도록 합니다.
ms.openlocfilehash: 06c43bcb3364b83114e2d7b1a2ef0273858cffb0
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261316"
---
# <a name="office-365-message-encryption"></a>Office 365 메시지 암호화

Office 365 메시지 암호화를 사용 하면 조직에서 조직 내부 및 외부의 사용자 간에 암호화 된 전자 메일 메시지를 보내고 받을 수 있습니다. Office 365 메시지 암호화는 Outlook.com, yahoo!, Gmail 및 기타 전자 메일 서비스에서 작동 합니다. 전자 메일 메시지 암호화는 의도 된 받는 사람만 메시지 콘텐츠를 볼 수 있도록 합니다.
  
이 문서는 Office 365 메시지 암호화에 대 한 보다 광범위 한 문서에 포함 되어 있습니다. 다음 표를 사용 하 여 필요한 정보를 신속 하 게 찾을 수 있습니다.
  
|||
|:-----|:-----|
|이 문서 읽기 ...  <br/> |...  <br/> |
|[Office 365의 보호 된 메시지에 대해 자세히 알아보기](https://support.office.com/article/2baf3ac7-12db-40a4-8af7-1852204b4b67.aspx) <br/> |암호화 된 메시지의 작동 방식과 사용할 수 있는 옵션에 대해 자세히 알아보려면 최종 사용자를 선택 합니다.  <br/> |
|[보호 된 메시지를 열려면 어떻게 해야 합니까?](https://support.office.com/article/1157a286-8ecc-4b1e-ac43-2a608fbf3098.aspx) <br/> |사용자에 게 전송 되는 보호 된 메시지를 읽으려고 하는 최종 사용자입니다. 이 문서에는 여러 Outlook 버전에서 메시지를 읽는 방법 및 다른 전자 메일 계정 (예: gmail 및 yahoo! 등의 Office 365 외부에 포함)에 대 한 정보가 포함 되어 있습니다. 거래처.  <br/> |
|[Outlook에서 암호화 된 메시지 보내기, 확인 및 회신](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx) <br/> |Outlook에서 암호화 된 메시지를 보내거나 보거나 회신 하려는 최종 사용자입니다. 사용자가 Office 365 조직의 구성원이 아니더라도 Outlook에서 보낸 암호화 된 메시지에 대 한 알림도 계속 받게 됩니다. 이 문서를 사용 하 여 Office 365에서 보낸 암호화 된 메시지를 보고 회신 하는 방법에 대 한 지침을 확인할 수 있습니다.  <br/> |
|[디지털 서명 되거나 암호화 된 메시지 보내기](https://support.office.com/article/a18ecf7f-a7ac-4edd-b02e-687b05eff547) <br/> |Mac 용 Outlook을 사용 하 여 암호화 된 메시지를 보내거나 보거나 회신 하려는 최종 사용자입니다. 이 문서에서는 S/MIME과 같이 OME 이외의 암호화 방법 사용에 대해서도 설명 합니다.  <br/> |
|[Android 장치에서 암호화 된 메시지 보기](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> |Android 장치에서 Office 365 메시지 암호화로 암호화 된 메시지를 받은 최종 사용자는 무료 OME Viewer 앱을 사용 하 여 메시지를 확인 하 고 암호화 된 회신을 보낼 수 있습니다. 이 문서에서는 이러한 방법을 설명 합니다.  <br/> |
|[iPhone 또는 iPad에서 암호화 된 메시지 보기](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |iPhone 또는 iPad에서 Office 365 메시지 암호화로 암호화 된 메시지를 받은 최종 사용자는 무료 OME Viewer 앱을 사용 하 여 메시지를 확인 하 고 암호화 된 회신을 보낼 수 있습니다. 이 문서에서는 이러한 방법을 설명 합니다.  <br/> |
|Office 365 메시지 암호화 (OME) (이 문서)  <br/> |추가 리소스를 찾을 수 있는 위치에 대 한 자세한 내용은 Office 365 또는 Exchange Online Protection 관리자에 게 문의 하세요.  <br/> |
|[OME 버전 비교](ome-version-comparison.md)  <br/> |office 365 또는 Exchange Online Protection 관리자는 레거시 office 365 메시지 암호화와 새 OME 기능 간의 차이점을 알아보고 함께 작업할 수 있는 방법을 확인 하려는 경우  <br/> |
|[Office 365 메시지 암호화 FAQ](ome-faq.md) <br/> |라이선스 및 새 기능과 레거시 OME를 비교 하는 등의 일반적인 질문에 대 한 답을 제공 하는 Office 365 또는 Exchange Online Protection 관리자입니다.  <br/> |
|[새로운 Office 365 메시지 암호화 기능 설정](set-up-new-message-encryption-capabilities.md) <br/> |office 365 조직에 대해 새 office 365 메시지 암호화 기능을 설정 하는 방법을 알아보려면 office 365 또는 Exchange Online Protection 관리자에 게 문의 하세요.  <br/> |
|[Office 365에서 전자 메일 메시지를 암호화하기 위한 메일의 흐름 규정을 정의](define-mail-flow-rules-to-encrypt-email.md) <br/> |이미 office 365 메시지 암호화를 설정 했으며 조직에서 보낸 전자 메일 메시지를 자동으로 암호화 하는 메일 흐름 규칙을 정의할 준비가 된 office 365 또는 Exchange Online Protection 관리자입니다.  <br/> |
|[Office 365 메시지 암호화 관리](manage-office-365-message-encryption.md) <br/> |이미 office 365 메시지 암호화를 설정 했으며 OME에 대 한 선택적 설정을 구성 하려는 office 365 또는 Exchange Online Protection 관리자입니다.  <br/> |
|[암호화된 메시지에 조직의 브랜드 추가](add-your-organization-brand-to-encrypted-messages.md) <br/> |회사 브랜딩을 적용 하 여 조직의 office 365 메시지 암호화 전자 메일 메시지와 OME 포털의 콘텐츠 모양을 사용자 지정 하려는 Office 365 또는 Exchange Online Protection 관리자입니다.  <br/> |
|[Office 365 메시지 암호화 전자 메일 해지](revoke-ome-encrypted-mail.md) <br/> |office 365 메시지 암호화를 사용 하 여 암호화 된 전자 메일을 해지 하려는 office 365 또는 Exchange Online Protection 관리자입니다.  <br/> |
|[메시지 정책 및 규정 준수 서비스 설명](https://technet.microsoft.com/en-us/library/5c43c8eb-f8f7-4b5a-a743-b1dab7dc2fc8#bkmk_O365_MessageEncryption) 의 Office 365 메시지 암호화 <br/> |office 365에서 제공 하는 지원 되는 sku를 포함 하 여 office 365 메시지 암호화 기능에 대 한 자세한 설명을 확인 합니다.  <br/> |
|[Office 365 메시지 암호화 레거시 정보](legacy-information-for-message-encryption.md) <br/> |이미 office 365 메시지 암호화를 설정한 office 365 또는 Exchange Online Protection 관리자 이며, 새 기능이 출시 되기 전에 OME가 작동 한 방법에 대 한 정보를 확인할 수 있습니다. 새 기능 없이 OME을 사용 하 여 새 배포를 설정할 수는 없지만 Microsoft는 계속 해 서 기존 배포를 지원 합니다. <br/> |
||

이 문서의 나머지 부분은 새로운 OME 기능에 적용 됩니다.
  
## <a name="how-office-365-message-encryption-works"></a>Office 365 메시지 암호화가 작동 하는 방식

Office 365 메시지 암호화는 azure Information Protection의 일부인 Microsoft azure RMS (서비스 권한 관리)를 기반으로 작성 된 온라인 서비스가 됩니다. 여기에는 전자 메일을 보호 하는 데 도움이 되는 암호화, id 및 권한 부여 정책이 포함 됩니다. 권한 관리 템플릿, [전달 금지 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)및 [암호화 전용 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 사용 하 여 메시지를 암호화할 수 있습니다.

그러면 사용자가 이러한 옵션을 사용 하 여 전자 메일 메시지와 다양 한 Office 365 첨부 파일을 암호화할 수 있습니다. 지원 되는 첨부 파일 형식에 대 한 전체 목록은 [전자 메일 메시지에 대 한 irm 소개에서 "irm 정책이 메시지에 첨부 될 때 확인 되는 파일 형식"](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM)을 참조 하십시오.

관리자는이 보호를 적용 하는 메일 흐름 규칙을 정의할 수도 있습니다. 예를 들어 특정 받는 사람에 게 주소를 지정 하거나 제목 줄에 특정 단어를 포함 하는 모든 메시지를 암호화 해야 하는 규칙을 만들 수 있으며, 받는 사람이 메시지 내용을 복사 하거나 인쇄할 수 없도록 지정할 수도 있습니다.

이전 버전의 OME과 달리 새로운 기능은 조직 내부에서 메일을 보내는 지, 아니면 Office 365 외부의 받는 사람에 게 제공 되는지 여부에 관계 없이 통합 된 보낸 사람을 위한 환경입니다. 또한 outlook 2016 또는 웹용 outlook에서 Office 365 계정으로 전송 되는 보호 된 전자 메일 메시지를 받는 받는 사람은 메시지를 확인 하기 위해 추가 작업을 수행할 필요가 없습니다. 완벽 하 게 작동 합니다. 다른 전자 메일 클라이언트와 전자 메일 서비스 공급자를 사용 하는 받는 사람도 향상 된 환경을 제공 합니다. 자세한 내용은 [Office 365의 보호 된 메시지에 대 한](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) 정보 및 [보호 된 메시지를 여는 방법](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098)를 참조 하십시오.

이전 버전의 OME와 새 OME 기능 간의 차이점에 대 한 자세한 목록은 [OME 버전 비교](ome-version-comparison.md)를 참조 하십시오.

다른 사용자가 암호화 메일 흐름 규칙과 일치 하는 전자 메일 메시지를 보내면 메시지가 전송 되기 전에 암호화 됩니다. 모든 Office 365 end-Outlook 클라이언트를 사용 하 여 메일을 읽는 사용자는 보낸 사람과 같은 조직에 없는 경우에도 암호화 및 권한으로 보호 되는 메일에 대 한 기본, 첫 번째 읽기 환경을 수신 합니다. 지원 되는 outlook 클라이언트에는 outlook 데스크톱, outlook Mac, iOS 및 Android의 outlook 모바일 및 웹용 outlook (이전의 outlook web App)이 포함 됩니다.
  
Outlook.com, gmail 및 Yahoo 계정으로 전송 된 암호화 또는 권한으로 보호 된 메일을 수신 하는 암호화 된 메시지를 받는 사람은 Microsoft 계정, gmail을 사용 하 여 쉽게 인증할 수 있는 OME 포털로 지시 하는 래퍼 메일을 받습니다. Yahoo 자격 증명
  
Outlook 이외의 클라이언트에서 암호화 되거나 권한으로 보호 된 메일을 읽는 최종 사용자는 OME 포털을 사용 하 여 자신이 받은 암호화 및 권한으로 보호 된 메시지를 볼 수 있습니다.

또한 보호 된 메일의 보낸 사람이 gcc high이 고 받는 사람이 Outlook.com와 같은 다른 전자 메일 공급자의 상업용 Office 365 사용자, 사용자 및 사용자를 포함 하 여 gcc high를 초과 하는 경우 받는 사람은 다음으로 리디렉션하는 래퍼 메일을 받습니다. 받는 사람이 메시지를 읽고 회신할 수 있는 OME 포털입니다. 그렇지 않고 보낸 사람과 받는 사람이 모두 GCC High 환경에 있는 경우 Outlook 클라이언트를 사용 하 여 메일을 읽는 받는 사람은 같은 조직에 있지 않은 경우에도 암호화 및 권한으로 보호 되는 메일에 대 한 기본, 최초 클래스 읽기 환경을 수신 합니다. 보낸 사람으로
  
OME을 사용 하 여 암호화할 수 있는 메시지 및 첨부 파일의 크기 제한이 증가 했습니다. 제한에 대 한 자세한 내용은 [Exchange Online 제한을](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)참조 하세요.
  
## <a name="defining-rules-for-office-365-message-encryption"></a>Office 365 메시지 암호화에 대한 규칙 정의

Office 365 메시지 암호화에 대 한 새로운 기능을 사용 하도록 설정 하는 한 가지 방법은 exchange online 및 exchange online Protection 관리자가 메일 흐름 규칙을 정의 하는 것입니다. 이러한 규칙은 전자 메일 메시지를 암호화 해야 하는 조건을 결정 합니다. 규칙에 대해 암호화 동작을 설정 하면 규칙 조건과 일치 하는 모든 메시지가 전송 되기 전에 암호화 됩니다.
  
메일 흐름 규칙은 융통성이 있으므로 단일 규칙에서 특정 보안 요구 사항을 충족할 수 있도록 조건을 조합할 수도 있습니다. 예를 들어 지정 된 키워드를 포함 하 고 외부 받는 사람에 게 보내는 모든 메시지를 암호화 하는 규칙을 만들 수 있습니다. 새로운 Office 365 메시지 암호화 기능을 통해 암호화 된 전자 메일을 받는 사람이 보낸 회신을 암호화할 수도 있습니다.
  
새 OME 기능을 활용 하기 위해 메일 흐름 규칙을 만드는 방법에 대 한 자세한 내용은 [Define rules for Office 365 Message Encryption](define-mail-flow-rules-to-encrypt-email.md)을 참조 하십시오.
  
## <a name="sending-viewing-and-replying-to-encrypted-email-messages"></a>암호화된 전자 메일 메시지 보내기, 보기 및 회신

Office 365 메시지 암호화를 사용 하면 사용자가 outlook 및 웹용 outlook에서 암호화 된 전자 메일을 보낼 수 있습니다. 또한 관리자는 키워드 일치 또는 기타 조건에 따라 전자 메일을 자동으로 암호화 하기 위해 Office 365에서 메일 흐름 규칙을 설정할 수 있습니다.
  
Office 365 조직에 있는 암호화 된 메시지의 받는 사람은 이러한 메시지를 outlook for PC, outlook for Mac, 웹용 outlook, iOS 용 outlook, Android 용 outlook 등을 비롯 한 모든 버전에서 원활 하 게 읽을 수 있습니다. 다른 전자 메일 클라이언트에서 암호화 된 메시지를 수신 하는 사용자는 OME 포털에서 메시지를 볼 수 있습니다.
  
암호화 된 메시지를 보내고 보는 방법에 대 한 자세한 지침은 다음 문서를 참조 하세요.
  
- [보호 된 메시지를 열려면 어떻게 해야 합니까?](https://support.office.com/article/1157a286-8ecc-4b1e-ac43-2a608fbf3098.aspx)

- [Outlook에서 암호화 된 메시지 보내기, 확인 및 회신](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)

## <a name="get-started-with-the-new-ome-capabilities"></a>새로운 OME 기능을 시작 합니다.

조직 내에서 새 OME 기능을 사용할 준비가 되 면 [Set up Office 365 Message Encryption capabilities](set-up-new-message-encryption-capabilities.md)를 참조 하세요.
