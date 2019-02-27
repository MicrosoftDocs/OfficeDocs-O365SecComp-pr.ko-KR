---
title: 웹용 Outlook에 대 한 Exchange Online의 S/MIME 설정 구성
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c7dee22c-9b5b-425c-91a9-d093204ff84e
ms.collection:
- M365-security-compliance
description: exchange online 관리자가 웹에서 Outlook의 S/MIME 설정을 보고 구성 하기 위해 수행 해야 하는 작업에 대 한 간략 한 설명입니다.
ms.openlocfilehash: 74d2f37f0cabc0b49abdd78d2a10928b543fd615
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295361"
---
# <a name="configure-smime-settings-in-exchange-online-for-outlook-on-the-web"></a><span data-ttu-id="18c31-103">웹용 Outlook에 대 한 Exchange Online의 S/MIME 설정 구성</span><span class="sxs-lookup"><span data-stu-id="18c31-103">Configure S/MIME settings in Exchange Online for Outlook on the web</span></span>

<span data-ttu-id="18c31-p101">Exchange Online 관리자는 웹에서 outlook (이전의 outlook web App)을 설정 하 여 S/MIME로 보호 된 메시지를 보내고 받을 수 있습니다. **get-smimeconfig** 및 **get-smimeconfig** cmdlet을 사용 하 여 Exchange Online PowerShell에서이 기능을 보고 관리 합니다. exchange online powershell에 연결 하려면 [exchange online powershell에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="18c31-p101">As an admin for Exchange Online, you can set up Outlook on the web (formerly known as Outlook Web App) to allow sending and receiving S/MIME-protected messages. Use the **Get-SmimeConfig** and **Set-SmimeConfig** cmdlets to view and manage this feature in Exchange Online PowerShell. To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

<span data-ttu-id="18c31-107">구문과 매개 변수에 대 한 자세한 내용은 [get-smimeconfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) 및 [get-smimeconfig](http://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="18c31-107">For detailed syntax and parameter information, see [Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) and [Set-SmimeConfig](http://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx).</span></span>

## <a name="considerations-for-chrome"></a><span data-ttu-id="18c31-108">Chrome에 대 한 고려 사항</span><span class="sxs-lookup"><span data-stu-id="18c31-108">Considerations for Chrome</span></span>

<span data-ttu-id="18c31-p102">Google Chrome 웹 브라우저에서 웹의 Outlook에서 S/mime을 사용 하려면 사용자 (또는 다른 관리자)가 Chromium 정책을 설정 하 고 구성 해야 합니다. \*\*\*\* 정책은 다음 구문을 사용 해야 합니다 ( `<extension-id>;https://outlook.office.com/owa/SmimeCrxUpdate.ashx` 예: `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`). 이 단계는 Chrome을 사용 하기 위한 필수 구성 요소입니다. 사용자가 설치한 S/MIME 컨트롤은 대체 되지 않습니다. **extensioninstallforcelist** 정책에 대 한 자세한 내용은 [extensioninstallforcelist](http://dev.chromium.org/administrators/policy-list-3#ExtensionInstallForcelist)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="18c31-p102">To use S/MIME in Outlook on the web in the Google Chrome web browser, you (or another admin) must set and configure the Chromium policy named **ExtensionInstallForcelist** to install the Microsoft S/MIME extension in Chrome. The policy should use the syntax: `<extension-id>;https://outlook.office.com/owa/SmimeCrxUpdate.ashx` For example: `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`. This step is a prerequisite for using Chrome; it does not replace the S/MIME control that's installed by users. For details about the **ExtensionInstallForcelist** policy, see [ExtensionInstallForcelist](http://dev.chromium.org/administrators/policy-list-3#ExtensionInstallForcelist).</span></span>

## <a name="for-more-information"></a><span data-ttu-id="18c31-113">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="18c31-113">For more information</span></span>

[<span data-ttu-id="18c31-114">메시지 서명 및 암호화를 위한 S/MIME</span><span class="sxs-lookup"><span data-stu-id="18c31-114">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)
