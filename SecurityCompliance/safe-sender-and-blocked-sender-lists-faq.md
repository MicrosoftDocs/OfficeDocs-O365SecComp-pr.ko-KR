---
title: 수신 허용-보낸사람 및 수신된 거부 목록 Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 111ab6b0-2dd2-4a87-a928-4931df6b3c4d
description: Exchange Online 또는 Exchange Online Protection (EOP) 관리자 권한으로 서비스를 통해 이동 하는 전자 메일 메시지를 스팸으로 표시 되지 않습니다을 하도록 할 수 있습니다. 이 작업을 수행 하는 한 가지 방법은 조직에 있는 사람에 대 한 수신 허용 및 수신 차단된 보낸사람 목록을 만드는 것입니다.
ms.openlocfilehash: cbf886bdcc40044a31b285b6806aecbc95f0f97c
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003107"
---
# <a name="safe-sender-and-blocked-sender-lists-in-exchange-online"></a><span data-ttu-id="28fb9-104">수신 허용-보낸사람 및 수신된 거부 목록 Exchange Online</span><span class="sxs-lookup"><span data-stu-id="28fb9-104">Safe sender and blocked sender lists in Exchange Online</span></span>

<span data-ttu-id="28fb9-p102">Exchange Online 또는 Exchange Online Protection (EOP) 관리자 권한으로 서비스를 통해 이동 하는 전자 메일 메시지를 스팸으로 표시 되지 않습니다을 하도록 할 수 있습니다. 이 작업을 수행 하는 한 가지 방법은 조직에 있는 사람에 대 한 수신 허용 및 수신 차단된 보낸사람 목록을 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="28fb9-p102">As an Exchange Online or Exchange Online Protection (EOP) administrator, you can help ensure that an email message traveling through the service isn't marked as spam. One way to do this is to create safe sender and blocked sender lists for the people in your organization.</span></span> 
  
 <span data-ttu-id="28fb9-107">*업데이트 된 버전의 팁 및 관리자에으로 이러한 목록을 사용 하 여 작업 하는 방법에 대 한 절차를 참조 하십시오.* [수신 허용 목록 또는 기타 기술을 스팸으로 표시 false 양의 전자 메일을 방지](https://go.microsoft.com/fwlink/p/?LinkID=534224)합니다.</span><span class="sxs-lookup"><span data-stu-id="28fb9-107">*See the updated version of the tips and procedures for how to work with these lists as an admin in* [Prevent false positive email marked as spam with a safelist or other techniques](https://go.microsoft.com/fwlink/p/?LinkID=534224).</span></span> 
  
<span data-ttu-id="28fb9-108">관리자, 자신이 수신 허용-보낸사람 목록을 사용 하 여 Outlook에서 자신의 정크 메일을 관리 하려는 경우이 개요 [정크 메일 필터](https://go.microsoft.com/fwlink/?LinkId=817222)의 단계를 체크아웃 합니다.</span><span class="sxs-lookup"><span data-stu-id="28fb9-108">If you're not an admin, and you just want to manage your own junk email in Outlook by using a safe sender list, check out the steps in this overview of [the Junk Email Filter](https://go.microsoft.com/fwlink/?LinkId=817222).</span></span> 
  
## <a name="what-is-the-safe-and-blocked-sender-limits-in-exchange-online"></a><span data-ttu-id="28fb9-109">온라인 Exchange 제한 수신 허용 및 차단 된 보낸사람은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="28fb9-109">What is the safe and blocked sender limits in Exchange Online?</span></span>

<span data-ttu-id="28fb9-p103">Active Directory에서 다를 Exchange Online의 수신 허용 및 차단 된 보낸사람 제한 및 Outlook를 제한 합니다. 와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="28fb9-p103">The safe and blocked sender limits in Exchange Online differ from the Active Directory and Outlook limits. They are:</span></span>
  
- <span data-ttu-id="28fb9-112">수신 허용-보낸사람 제한: 1, 024</span><span class="sxs-lookup"><span data-stu-id="28fb9-112">Safe sender limit: 1,024</span></span>
    
- <span data-ttu-id="28fb9-113">차단 된 보낸사람 제한: 500 개</span><span class="sxs-lookup"><span data-stu-id="28fb9-113">Blocked sender limit: 500</span></span>
    
<span data-ttu-id="28fb9-114">참고:</span><span class="sxs-lookup"><span data-stu-id="28fb9-114">Note:</span></span>
  
<span data-ttu-id="28fb9-p104">KB 2590466 ("오류가 나타나면"정크 메일 유효성 검사 오류"Outlook Web App에서 Exchange Server 2010에 대 한")에 설명 된 오류가 발생할 수 있습니다. 이 문제를 해결 하려면 "내 연락처에서 보내는 전자 메일 신뢰" 확인란의 선택을 취소 합니다. 전자 메일 주소는 허용 되는 최대 내에서 가져올 기본 연락처 폴더에서를 제한 하는 1, 024 Exchange 온라인 "MaxSafeSenders" 특성에 대해 설정 된 시간 또는 줄이기 이 특성 및 Set-mailbox cmdlet에 대 한 자세한 내용은 다음 항목을 seethe:</span><span class="sxs-lookup"><span data-stu-id="28fb9-p104">You may experience the error that is described in KB 2590466 ("You receive the error "Junk e-mail validation error" in Outlook Web App for Exchange Server 2010"). To resolve this issue, clear the "Trust emails from my contacts" check box. Alternatively, decrease the amount of email addresses that are in your default Contacts folder to bring it within the maximum allowed limit of 1,024 in Exchange Online that is set for "MaxSafeSenders" attribute. For more information about this attribute and the Set-Mailbox cmdlet, seethe following topic:</span></span>
  
[<span data-ttu-id="28fb9-119">Set-Mailbox</span><span class="sxs-lookup"><span data-stu-id="28fb9-119">Set-Mailbox</span></span>](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Set-Mailbox?view=exchange-ps)
  
## <a name="see-also"></a><span data-ttu-id="28fb9-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="28fb9-120">See also</span></span>

[<span data-ttu-id="28fb9-121">보낸 사람이 Exchange 2016에서 필터링</span><span class="sxs-lookup"><span data-stu-id="28fb9-121">Sender filtering in Exchange 2016</span></span>](http://technet.microsoft.com/library/b833f864-ff10-46a0-a653-28fb9ba30896.aspx)

