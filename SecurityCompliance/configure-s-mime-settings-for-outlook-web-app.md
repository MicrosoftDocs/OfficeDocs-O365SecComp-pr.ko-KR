---
title: 웹용 Outlook에 대 한 Exchange Online의 S/MIME 설정 구성
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c7dee22c-9b5b-425c-91a9-d093204ff84e
ms.collection:
- M365-security-compliance
description: exchange online 관리자가 웹에서 Outlook의 S/MIME 설정을 보고 구성 하기 위해 수행 해야 하는 작업에 대 한 간략 한 설명입니다.
ms.openlocfilehash: d890b7f39d16d8c0f3866d5ff0024fe31160af6b
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693337"
---
# <a name="configure-smime-settings-in-exchange-online-for-outlook-on-the-web"></a>웹용 Outlook에 대 한 Exchange Online의 S/MIME 설정 구성

Exchange Online 관리자는 웹에서 outlook (이전의 outlook web App)을 설정 하 여 S/MIME로 보호 된 메시지를 보내고 받을 수 있습니다. **get-smimeconfig** 및 **get-smimeconfig** cmdlet을 사용 하 여 Exchange Online PowerShell에서이 기능을 보고 관리 합니다. exchange online powershell에 연결 하려면 [exchange online powershell에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조 하세요.

구문과 매개 변수에 대 한 자세한 내용은 [get-smimeconfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) 및 [get-smimeconfig](http://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx)를 참조 하십시오.

## <a name="considerations-for-chrome"></a>Chrome에 대 한 고려 사항

Google Chrome 웹 브라우저에서 웹의 Outlook에서 S/mime을 사용 하려면 사용자 (또는 다른 관리자)가 Chromium 정책을 설정 하 고 구성 해야 합니다. **** 정책은 다음 구문을 사용 해야 합니다 ( `<extension-id>;https://outlook.office.com/owa/SmimeCrxUpdate.ashx` 예: `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`). 또한이 정책을 적용 하려면 도메인에 가입 된 컴퓨터가 필요 하므로 Chrome에서 S/MIME을 사용 하려면 도메인에 가입 된 컴퓨터가 필요 합니다.

이 단계는 Chrome을 사용 하기 위한 필수 구성 요소입니다. 사용자가 설치한 S/MIME 컨트롤은 대체 되지 않습니다. **extensioninstallforcelist** 정책에 대 한 자세한 내용은 [extensioninstallforcelist](http://dev.chromium.org/administrators/policy-list-3#ExtensionInstallForcelist)를 참조 하십시오.

## <a name="for-more-information"></a>자세한 내용

[메시지 서명 및 암호화를 위한 S/MIME](s-mime-for-message-signing-and-encryption.md)
