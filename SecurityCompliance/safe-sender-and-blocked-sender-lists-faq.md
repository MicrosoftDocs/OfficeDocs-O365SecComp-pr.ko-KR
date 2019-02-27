---
title: Exchange Online의 수신 허용-보낸 사람 및 수신 거부 목록
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 111ab6b0-2dd2-4a87-a928-4931df6b3c4d
ms.collection:
- M365-security-compliance
description: exchange online 또는 EOP (exchange online Protection) 관리자는 서비스를 통과 하는 전자 메일 메시지가 스팸으로 표시 되지 않도록 할 수 있습니다. 이 작업을 수행 하는 한 가지 방법은 조직의 사용자에 대해 수신 허용-보낸 사람 및 수신 거부 목록을 만드는 것입니다.
ms.openlocfilehash: 390b414c44da6b30193bcb6b9db0b8162aafffb7
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275658"
---
# <a name="safe-sender-and-blocked-sender-lists-in-exchange-online"></a><span data-ttu-id="523aa-104">Exchange Online의 수신 허용-보낸 사람 및 수신 거부 목록</span><span class="sxs-lookup"><span data-stu-id="523aa-104">Safe sender and blocked sender lists in Exchange Online</span></span>

<span data-ttu-id="523aa-p102">exchange online 또는 EOP (exchange online Protection) 관리자는 서비스를 통과 하는 전자 메일 메시지가 스팸으로 표시 되지 않도록 할 수 있습니다. 이 작업을 수행 하는 한 가지 방법은 조직의 사용자에 대해 수신 허용-보낸 사람 및 수신 거부 목록을 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="523aa-p102">As an Exchange Online or Exchange Online Protection (EOP) administrator, you can help ensure that an email message traveling through the service isn't marked as spam. One way to do this is to create safe sender and blocked sender lists for the people in your organization.</span></span> 
  
 <span data-ttu-id="523aa-107">*에서이 목록을 사용 하 여 작업 하는 방법에 대 한 업데이트 된 버전의 팁 및 절차를 참조 하세요* . [수신 허용 목록 또는 기타 방법으로 스팸으로 표시 된 허위 긍정 전자 메일을 방지](https://go.microsoft.com/fwlink/p/?LinkID=534224)합니다.</span><span class="sxs-lookup"><span data-stu-id="523aa-107">*See the updated version of the tips and procedures for how to work with these lists as an admin in* [Prevent false positive email marked as spam with a safelist or other techniques](https://go.microsoft.com/fwlink/p/?LinkID=534224).</span></span> 
  
<span data-ttu-id="523aa-108">관리자가 아닌 경우 Outlook에서 수신 허용-보낸 사람 목록을 사용 하 여 자신의 정크 메일을 관리 하려는 경우에는 [정크 메일 필터](https://go.microsoft.com/fwlink/?LinkId=817222)개요의 단계를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="523aa-108">If you're not an admin, and you just want to manage your own junk email in Outlook by using a safe sender list, check out the steps in this overview of [the Junk Email Filter](https://go.microsoft.com/fwlink/?LinkId=817222).</span></span> 
  
## <a name="what-is-the-safe-and-blocked-sender-limits-in-exchange-online"></a><span data-ttu-id="523aa-109">Exchange Online에서 수신 허용 및 차단 된 보낸 사람 제한은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="523aa-109">What is the safe and blocked sender limits in Exchange Online?</span></span>

<span data-ttu-id="523aa-p103">Exchange Online의 수신 및 차단 된 보낸 사람 제한은 Active Directory 및 Outlook 제한과 다릅니다. 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="523aa-p103">The safe and blocked sender limits in Exchange Online differ from the Active Directory and Outlook limits. They are:</span></span>
  
- <span data-ttu-id="523aa-112">수신 허용-보낸 사람 제한: 1024</span><span class="sxs-lookup"><span data-stu-id="523aa-112">Safe sender limit: 1,024</span></span>
    
- <span data-ttu-id="523aa-113">차단 된 보낸 사람 제한: 500</span><span class="sxs-lookup"><span data-stu-id="523aa-113">Blocked sender limit: 500</span></span>
    
<span data-ttu-id="523aa-114">참고:</span><span class="sxs-lookup"><span data-stu-id="523aa-114">Note:</span></span>
  
<span data-ttu-id="523aa-p104">[KB2590466](https://support.microsoft.com/help/2590466/you-receive-the-error-junk-e-mail-validation-error-in-outlook-web-app)에 설명 되어 있는 오류가 발생할 수 있습니다. 이 문제를 해결 하려면 "내 연락처에서 전자 메일 신뢰" 확인란의 선택을 취소 합니다. 또는 "MaxSafeSenders" 특성에 대해 설정 된 Exchange Online에서 허용 되는 최대 제한인 1024에 표시 되도록 기본 연락처 폴더에 있는 전자 메일 주소 크기를 줄일 수 있습니다. 이 특성 및 사서함 cmdlet에 대 한 자세한 내용은 다음 항목을 slmgr.vbs.</span><span class="sxs-lookup"><span data-stu-id="523aa-p104">You may experience the error that is described in [KB2590466](https://support.microsoft.com/help/2590466/you-receive-the-error-junk-e-mail-validation-error-in-outlook-web-app). To resolve this issue, clear the "Trust emails from my contacts" check box. Alternatively, decrease the amount of email addresses that are in your default Contacts folder to bring it within the maximum allowed limit of 1024 in Exchange Online that is set for "MaxSafeSenders" attribute. For more information about this attribute and the Set-Mailbox cmdlet, seethe following topic:</span></span>
  
[<span data-ttu-id="523aa-119">Set-Mailbox</span><span class="sxs-lookup"><span data-stu-id="523aa-119">Set-Mailbox</span></span>](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Set-Mailbox)
  
## <a name="see-also"></a><span data-ttu-id="523aa-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="523aa-120">See also</span></span>

[<span data-ttu-id="523aa-121">Exchange 2016의 보낸 사람 필터링</span><span class="sxs-lookup"><span data-stu-id="523aa-121">Sender filtering in Exchange 2016</span></span>](http://technet.microsoft.com/library/b833f864-ff10-46a0-a653-28fb9ba30896.aspx)

