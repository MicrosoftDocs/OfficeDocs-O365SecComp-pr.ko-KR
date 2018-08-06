---
title: Outlook Web App에 대 한 S/MIME 설정 구성
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/8/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: c7dee22c-9b5b-425c-91a9-d093204ff84e
description: 조직에 대 한 관리자로 Exchange 2013 및 Exchange Online 모두, S/MIME로 보호 된 메시지 보내기 및 받기를 허용 하도록 Outlook Web App을 설정할 수 있습니다. Exchange 관리 셸 인터페이스를 통해이 기능을 관리 하려면 SMIMEConfig cmdlet을 사용 합니다.
ms.openlocfilehash: d351129c7e12a66b530e0e4f82107728fd8387ae
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027135"
---
# <a name="configure-smime-settings-for-outlook-web-app"></a><span data-ttu-id="9c42d-104">Outlook Web App에 대 한 S/MIME 설정 구성</span><span class="sxs-lookup"><span data-stu-id="9c42d-104">Configure S/MIME settings for Outlook Web App</span></span>

<span data-ttu-id="9c42d-p102">Exchange 2013 및 Exchange Online의 조직 관리자는 S/MIME으로 보호되는 메시지 보내기와 받기를 허용하도록 Outlook Web App을 설정할 수 있습니다.  `SMIMEConfig` cmdlet을 사용하여 Exchange 관리 셸 인터페이스를 통해 이 기능을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="9c42d-p102">As an organization administrator for both Exchange 2013 and Exchange Online, you can set up Outlook Web App to allow sending and receiving S/MIME-protected messages. Use the  `SMIMEConfig` cmdlet to manage this feature through the Exchange Management Shell interface.</span></span> 
  
<span data-ttu-id="9c42d-107">`get-SMIMEConfig` 및  `set-SMIMEConfig`에 대한 예제 및 매개 변수 상세 설명 등의 자세한 내용은 [Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) 및 [Set-SmimeConfig](http://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx) 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9c42d-107">For more information such as a detailed description of parameters and examples for  `get-SMIMEConfig` and  `set-SMIMEConfig`, see the [Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) and [Set-SmimeConfig](http://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx) documentation.</span></span> 
  
<span data-ttu-id="9c42d-p103">이 절차를 수행 하려면 셸을만 사용할 수 있습니다. 온-프레미스 Exchange 조직에서 Exchange 관리 셸을 열려면 하는 방법을 알아보려면 **셸을 열**을 참조 하십시오. Exchange Online에 연결 하려면 Windows PowerShell을 사용 하는 방법을 알아보려면 [Exchange Online PowerShell 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9c42d-p103">You can only use the Shell to perform this procedure. To learn how to open the Exchange Management Shell in your on-premises Exchange organization, see **Open the Shell**. To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="9c42d-111">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="9c42d-111">For more information</span></span>

[<span data-ttu-id="9c42d-112">S/MIME 메시지 서명 및 암호화에 대 한</span><span class="sxs-lookup"><span data-stu-id="9c42d-112">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)
  

