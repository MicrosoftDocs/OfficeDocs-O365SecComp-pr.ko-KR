---
title: Office 365 메시지 암호화
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/6/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f87cb016-7876-4317-ae3c-9169b311ff8a
description: Office 365 메시지 암호화를 사용 하면 조직 보내고 사용자 조직 내부 및 외부 사용자 간의 암호화 된 전자 메일 메시지를 받을 수 있습니다. 전자 메일 메시지 암호화를 통해 확인만 받는 사람에 게 대상으로 하는 메시지 콘텐츠를 볼 수 있습니다.
ms.openlocfilehash: 57b1d34902bb1522a7974e97f8cd90e9f19b76f5
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29696262"
---
# <a name="office-365-message-encryption"></a>Office 365 메시지 암호화

Office 365 메시지 암호화를 사용 하면 조직 보내고 사용자 조직 내부 및 외부 사용자 간의 암호화 된 전자 메일 메시지를 받을 수 있습니다. Office 365 메시지 암호화 Outlook.com, yahoo!, Gmail, 및 다른 전자 메일 서비스에서 작동합니다. 전자 메일 메시지 암호화를 통해 확인만 받는 사람에 게 대상으로 하는 메시지 콘텐츠를 볼 수 있습니다.
  
이 문서는 Office 365 메시지 암호화에 대 한 문서를 더 큰 시리즈의 일부입니다. 다음 표를 사용 하 여 신속 하 게 필요한 정보를 찾을 수 있습니다.
  
|||
|:-----|:-----|
|이 문서를 읽으면...  <br/> |하는 경우...  <br/> |
|[Office 365의 보호 된 메시지에 대 한 설명](https://support.office.com/article/2baf3ac7-12db-40a4-8af7-1852204b4b67.aspx) <br/> |방법에 대 한 자세한 내용은 최종 사용자 메시지 작업 하 고 암호화 옵션을 사용할 수 있습니다.  <br/> |
|[보호 된 메시지를 열려면 어떻게 해야 합니까?](https://support.office.com/article/1157a286-8ecc-4b1e-ac43-2a608fbf3098.aspx) <br/> |최종 사용자가 전송 된 보호 된 메시지를 읽을 수입니다. 이 문서는 여러 버전의 Outlook 및 포함 하 여 Office 365 외부에서 gmail 및 yahoo! 계정 등, 다른 전자 메일 계정에서 메시지를 읽는 것에 대 한 정보를 포함 합니다.  <br/> |
|[보내기, 보기 및 Outlook에서 암호화 된 메시지에 회신](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx) <br/> |최종 사용자가 보내기, 확인 또는 Outlook에서 암호화 된 메시지에 회신 하려면입니다. Office 365 조직에 소속 모르는 경우에 사용자가 보낸 Outlook에서 암호화 된 메시지에 대 한 알림을 계속 나타납니다. 이 문서를 사용 하 여 보기 및 Office 365에서 보낸 암호화 된 메시지에 회신 하는 방법에 대 한 지침은.  <br/> |
|[디지털 서명 또는 암호화 된 메시지 보내기](https://support.office.com/article/a18ecf7f-a7ac-4edd-b02e-687b05eff547) <br/> |최종 사용자가 보내기, 보기, 또는 Outlook for mac입니다.를 사용 하 여 암호화 된 메시지에 회신 이 문서에서는 S/MIME 같은 OME 아닌 다른 암호화 방법을 사용 하 여 다룹니다.  <br/> |
|[Android 장치에서 암호화 된 메시지 보기](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> |최종 사용자가 있는 메시지를 받은 암호화 된 Office 365 메시지 암호화 Android 장치에서의 경우 암호화 된 회신을 주고 메시지를 볼 수 무료 OME 뷰어 응용 프로그램을 사용할 수 있습니다. 이 문서에 설명 방법입니다.  <br/> |
|[IPhone 또는 iPad에서 암호화 된 메시지 보기](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |최종 사용자가 있는 메시지를 받은 암호화 된 Office 365 메시지 암호화 iPhone 또는 iPad에서의 경우 암호화 된 회신을 주고 메시지를 볼 수 무료 OME 뷰어 응용 프로그램을 사용할 수 있습니다. 이 문서에 설명 방법입니다.  <br/> |
|Office 365 메시지 암호화 (OME) (이 문서)  <br/> |Office 365 또는 Exchange Online Protection 관리자가 추가 리소스를 찾을 수 있는 위치에 대해 알아봅니다.  <br/> |
|[OME 버전 비교](ome-version-comparison.md)  <br/> |Office 365 또는 Exchange Online Protection 관리자가 함께 작업할 수 하는 방법에 따라 레거시 Office 365 메시지 암호화 하 고 새 OME 기능 간의 차이점에 알아봅니다.  <br/> |
|[Office 365 메시지 암호화 FAQ](ome-faq.md) <br/> |Office 365 또는 Exchange Online Protection 관리자에 게에 대 한 답변을 일반적으로 대답 (영문) 라이선스 및 새 기능 및 레거시 OME 간의 비교를 포함 합니다.  <br/> |
|[새로운 Office 365 메시지 암호화 기능 설정](set-up-new-message-encryption-capabilities.md) <br/> |Office 365 또는 Exchange Online 보호 하려는 관리자가 Office 365 조직에 대 한 새 Office 365 메시지 암호화 기능을 설정 하는 방법을 설명 합니다.  <br/> |
|[Office 365에서 전자 메일 메시지를 암호화하기 위한 메일의 흐름 규정을 정의](define-mail-flow-rules-to-encrypt-email.md) <br/> |Office 365 또는 Exchange Online Protection 관리자에 게 Office 365 메시지 암호화 하 고 설정한 이미 자동으로 조직에서 보낸 전자 메일 메시지를 암호화 하는 메일 흐름 규칙을 정의 하려면 준비가 되었습니다.  <br/> |
|[Office 365 메시지 암호화 관리](manage-office-365-message-encryption.md) <br/> |Office 365 또는 Exchange Online Protection 관리자에 게 이미 Office 365 메시지 암호화를 설정 하 고 OME에 대 한 선택적 설정을 구성 하 려 합니다.  <br/> |
|[암호화된 메시지에 조직의 브랜드 추가](add-your-organization-brand-to-encrypted-messages.md) <br/> |Office 365 또는 Exchange Online Protection 관리자 참가 조직의 Office 365 메시지 암호화 전자 메일 메시지의 모양 및 OME 포털의 내용을 사용자 지정 브랜딩 회사를 적용 하려는 합니다.  <br/> |
|[Office 365 메시지 암호화 전자 메일 해지](revoke-ome-encrypted-mail.md) <br/> |Office 365 또는 Exchange Online 보호 하려는 관리자가 Office 365 메시지 암호화를 사용 하 여 암호화 된 전자 메일을 해지 합니다.  <br/> |
|Office 365 메시지 암호화 [메시지 정책 및 규정 준수 서비스 설명](https://technet.microsoft.com/en-us/library/5c43c8eb-f8f7-4b5a-a743-b1dab7dc2fc8#bkmk_O365_MessageEncryption) <br/> |Office 365 메시지 암호화 기능에 대 한 자세한 설명을 대 한 자세한 내용은 Sku, Office 365에서 사용할 수 있는 지원 포함 합니다.  <br/> |
|[Office 365 메시지 암호화 레거시 정보](legacy-information-for-message-encryption.md) <br/> |Office 365 또는 Exchange Online Protection 관리자에 게 Office 365 메시지 암호화 하 고를 이미 설정한 OME 릴리스 이전에 새 기능이 작동 하는 방법에 대 한 정보를 원하는 합니다. 새로운 기능 없이 OME를 사용 하 여 새 배포를 설정할 수 없습니다, 하는 동안 Microsoft 계속 기존 배포를 지원 합니다.  <br/> |
||

이 문서의 나머지 부분 새 OME 기능에 적용 됩니다.
  
## <a name="how-office-365-message-encryption-works"></a>Office 365 메시지 암호화의 작동 방식

Office 365 메시지 암호화는 Microsoft Azure RMS (권한 관리 Azure) Azure 정보 보호의 일부분으로 작성 되는 온라인 서비스입니다. Office 365 관리자 암호화에 대 한 조건을 확인 하려면 메일 흐름 규칙을 정의할 수 있습니다. 예, 규칙을 특정 받는 사람에 게 보내는 모든 메시지의 암호화가 필요 수 있습니다.
  
Exchange Online 아웃 암호화 메일 흐름 규칙에 맞는에서 전자 메일 메시지를 보내는 사람이 메시지 전송 하기 전에 암호화 됩니다. 모든 Office 365 최종 사용자에 게 메일을 읽을 수 Outlook 클라이언트를 사용 하는 네이티브, 보낸 사람이와 같은 조직에 모르는 경우에 암호화 및 권한으로 보호 된 메일에 대 한 경험을 읽는 고급 수신 합니다. 지원 되는 Outlook 클라이언트에는 Outlook 데스크톱, Outlook Mac iOS 및 Android, 모바일 Outlook 및 Outlook Web App 포함 합니다.
  
Outlook.com, Gmail, 및 yahoo 계정으로 전송 되는 암호화 또는 권한으로 보호 된 메일을 수신 하 게 암호화 된 메시지의 받는 사람 자신의 Microsoft 계정 또는 Gmail 또는 yahoo 자격 증명을 사용 하 여 OME 포털에 쉽게 인증할 수 있습니다.
  
Outlook 이외의 클라이언트에서 메일을 암호화 또는 권한 보호를 읽고 있는 최종 사용자에 게 OME 포털 사용 하 여 받은 하는 암호화 및 권한으로 보호 된 메시지를 볼 수 있습니다.
  
메시지 및 Office 365 메시지 암호화를 사용 하 여 암호화할 수 있는 첨부 파일에 대 한 크기 제한을 증가 했습니다. 제한 하는 방법에 대 한 자세한 내용은 참조 [Exchange Online 제한.](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
  
## <a name="defining-rules-for-office-365-message-encryption"></a>Office 365 메시지 암호화에 대한 규칙 정의

Office 365 메시지 암호화에 대 한 새로운 기능을 사용 하도록 설정 하는 한 가지 방법은 메일 흐름 규칙을 정의 하려면 Exchange Online 및 Exchange Online Protection 관리자입니다. 이러한 규칙에 따라 결정에서 어떤 조건 전자 메일 메시지를 암호화 해야 합니다. 암호화 작업 규칙에 대해 설정 된 경우이 로그는 전송 하기 전에 규칙 조건에 맞는 모든 메시지는 암호화 됩니다.
  
메일 흐름 규칙은 유연한 두면 조건을 결합 하는 단일 규칙에서 특정 보안 요구 사항을 충족할 수 있습니다. 예를 포함 하는 지정 된 키워드 외부 받는 사람에 게 보내는 모든 메시지를 암호화 하는 규칙을 만들 수 있습니다. Office 365 메시지 암호화에 대 한 새로운 기능에는 또한 암호화 된 전자 메일의 받는 사람에 대 한 회신 암호화합니다.
  
규칙을 만들어 메일 흐름을 새 OME 기능을 활용 하는 방법에 대 한 자세한 내용은 [Office 365 메시지 암호화에 대 한 규칙 정의](define-mail-flow-rules-to-encrypt-email.md)참조 하십시오.
  
## <a name="sending-viewing-and-replying-to-encrypted-email-messages"></a>암호화된 전자 메일 메시지 보내기, 보기 및 회신

Office 365 메시지 암호화와 사용자 Outlook 및 웹에 있는 Outlook에서 암호화 된 전자 메일을 보낼 수 있습니다. 또한 관리자가 키워드 일치 하는 또는 기타 조건에 따라 전자 메일을 자동으로 암호화를 Office 365의 메일 흐름 규칙을 설정할 수 있습니다.
  
Office 365 조직에 있는 암호화 된 메시지의 받는 사람 PC에 대 한 Outlook, Outlook for Mac, 웹에 있는 Outlook, iOS, Outlook 및 Android에 대 한 Outlook을 비롯 하 여 Outlook 버전에서 원활 하 게 해당 메시지를 읽을 수 없게 됩니다. 다른 전자 메일 클라이언트에서 암호화 된 메시지를 받는 사용자 OME 포털에서 메시지를 볼 수 있습니다.
  
보내고 암호화 된 메시지를 확인 하는 방법에 대 한 자세한 지침에 대 한 이러한 문서에 대 한 정보를 수행 합니다.
  
- [보호 된 메시지를 열려면 어떻게 해야 합니까?](https://support.office.com/article/1157a286-8ecc-4b1e-ac43-2a608fbf3098.aspx)

- [보내기, 보기 및 Outlook에서 암호화 된 메시지에 회신](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)

## <a name="get-started-with-the-new-ome-capabilities"></a>새 OME 기능 시작

조직 내에서 새 OME 기능을 사용 하 여 시작 준비가 된 것을 하는 경우 [새로운 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md)참조 하십시오.
