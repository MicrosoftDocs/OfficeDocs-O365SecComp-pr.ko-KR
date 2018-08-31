---
title: Office 365에서 비활성 사서함 삭제
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: f5caf497-5e8d-4b7a-bfff-d02942f38150
description: 더이상 Office 365 비활성 사서함의 내용을 보존 해야하는 경우에 보류를 제거 하 여 비활성 사서함을 영구적으로 삭제할 수 없습니다. 보류를 제거한 후 비활성 사서함 삭제 하도록 표시 하 고 처리 된 후에 영구적으로 삭제 됩니다.
ms.openlocfilehash: 91b73fff6ca319735289abe7ea9351b5fba931a0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532970"
---
# <a name="delete-an-inactive-mailbox-in-office-365"></a><span data-ttu-id="73f73-104">Office 365에서 비활성 사서함 삭제</span><span class="sxs-lookup"><span data-stu-id="73f73-104">Delete an inactive mailbox in Office 365</span></span>

<span data-ttu-id="73f73-p102">비활성 사서함이 자신이 조직을 떠난 후 이전 직원의 전자 메일을 유지 하기 위해 사용 됩니다. 더이상 비활성 사서함의 내용을 보존 해야하는 경우에 보류를 제거 하 여 비활성 사서함을 영구적으로 삭제할 수 없습니다. 또한 것 여러 보존 비활성 사서함에 배치 될 수 있습니다. 예, 하나 이상의 원본 위치 유지 및 소송 보존으로 설정에서 비활성 사서함에 배치할 수 수 있습니다. 또한는 Office 365 보존 정책 (Office 365 보안에서 만든 &amp; 준수 센터) 비활성 사서함에 적용할 수 있습니다. 모든 보류 및 Office 365 보존 정책을 삭제 하려면 비활성 사서함에서 제거 해야 합니다. 보류 및 보존 정책을 제거한 후 비활성 사서함 삭제 하도록 표시 하 고 처리 된 후에 영구적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p102">An inactive mailbox is used to preserve a former employee's email after he or she leaves your organization. When you no longer need to preserve the contents of an inactive mailbox, you can permanently delete the inactive mailbox by removing the hold. Also, it's possible that multiple holds might be placed on an inactive mailbox. For example, an inactive mailbox might be placed on Litigation Hold and on one or more In-Place Holds. Additionally, an Office 365 retention policy (created in the Office 365 Security &amp; Compliance Center) might be applied to the inactive mailbox. You have to remove all holds and Office 365 retention policies from an inactive mailbox to delete it. After you remove the holds and retention policies, the inactive mailbox is marked for deletion and is permanently deleted after it's processed.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="73f73-p103">사서함을 비활성화하기 위해 새 원본 위치 유지를 만들 수 있는 2017년 7월 1일 마감 날짜를 연기했습니다. 하지만 올해 말이나 내년 초에는 Exchange Online에 새 원본 위치 유지를 만들 수 없습니다. 그때는 소송 보존과 Office 365 보존 정책만 사용하여 비활성화 사서함을 만들 수 있습니다. 그러나 원본 위치 유지에 있는 기존 비활성화 사서함은 계속 지원되며 비활성화 사서함에서 원본 위치 유지를 계속 관리할 수 있습니다. 관리 항목으로는 원본 위치 유지 기간 변경 및 원본 위치 유지를 삭제하여 비활성화 사서함을 영구 삭제하는 작업이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds to make a mailbox inactive. But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. At that time, only Litigation Holds and Office 365 retention policies can be used to create an inactive mailbox. However, existing inactive mailboxes that are on In-Place Hold will still be supported, and you can continue to manage the In-Place Holds on inactive mailboxes. This includes changing the duration of an In-Place Hold and permanently deleting an inactive mailbox by removing the In-Place Hold.</span></span> 
  
<span data-ttu-id="73f73-117">비활성 사서함에서 보류를 제거한 후 수행 하는 작업에 대 한 설명에 대 한 [자세한 내용](delete-an-inactive-mailbox.md#moreinfo) 은 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="73f73-117">See the [More information](delete-an-inactive-mailbox.md#moreinfo) section for a description of what happens after holds are removed from an inactive mailbox.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="73f73-118">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="73f73-118">Before you begin</span></span>

- <span data-ttu-id="73f73-p104">비활성 사서함에서 소송 보존을 제거 하려면 Exchange Online PowerShell을 사용 해야 합니다. Exchange 관리 센터 (EAC)를 사용할 수 없습니다. 단계별 지침은 [Connect to Exchange Online PowerShell를](https://go.microsoft.com/fwlink/?linkid=396554)참조 하십시오. 비활성 사서함에서 유지 하는 위치를 제거 하려면 Exchange Online PowerShell 또는 EAC를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p104">You have to use Exchange Online PowerShell to remove a Litigation Hold from an inactive mailbox. You can't use the Exchange admin center (EAC). For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). You can use Exchange Online PowerShell or the EAC to remove an In-Place Hold from an inactive mailbox.</span></span> 
    
- <span data-ttu-id="73f73-p105">보류를 제거 하 고 비활성 사서함을 삭제 하기 전에 비활성 사서함의 내용을 다른 사서함에 복사할 수 있습니다. 자세한 내용은 [Office 365에서 비활성 사서함 복원](restore-an-inactive-mailbox.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="73f73-p105">You can copy the contents of an inactive mailbox to another mailbox before you remove the hold and delete an inactive mailbox. For details, see [Restore an inactive mailbox in Office 365](restore-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="73f73-p106">비활성 사서함에서 보류 또는 Office 365 보존 정책을 제거 하는 경우 사서함에 대 한 일시 삭제 된 사서함 보존 기간이 만료 된 사서함 영구적으로 삭제 됩니다. 삭제 한 후에 복구할 수 없습니다. 보류를 제거 하기 전에 사서함의 내용이 필요 없는 해야 합니다. 비활성 사서함을 다시 활성화 하려는 경우에이 복구할 수 있습니다. 자세한 내용은 [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p106">If you remove the hold or Office 365 retention policy from an inactive mailbox and the soft-deleted mailbox retention period for the mailbox has expired, the mailbox will be permanently deleted. After it's deleted, it can't be recovered. Before you remove the hold, be sure that you no longer need the contents in the mailbox. If you want to re-activate an inactive mailbox, you can recover it. For details, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="73f73-130">비활성 사서함에 대 한 자세한 내용은 [Office 365에서 비활성 사서함](inactive-mailboxes-in-office-365.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="73f73-130">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a><span data-ttu-id="73f73-131">1 단계: 비활성 사서함에서 보류를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-131">Step 1: Identify the holds on an inactive mailbox</span></span>

<span data-ttu-id="73f73-p107">앞서 설명한 것 처럼 비활성 사서함에 소송 보존으로 설정, 원본 위치 유지 또는 Office 365 보존 정책에 배치할 수 있습니다. 첫번째 단계 비활성 사서함에서 보류를 식별 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p107">As previously stated, a Litigation Hold, In-Place Hold, or Office 365 retention policy might be placed on an inactive mailbox. The first step is to identify the holds on an inactive mailbox.</span></span>
  
<span data-ttu-id="73f73-134">조직에서 모든 비활성 사서함에 대 한 보류 정보를 표시 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-134">Run the following command to display the hold information for all inactive mailboxes in your organization.</span></span>
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,InPlaceHolds
```

<span data-ttu-id="73f73-p108">**LitigationHoldEnabled** 속성에 대 한 값 **True** 소송 보존으로 설정에서 비활성 사서함 인지를 나타냅니다. 비활성 사서함에 배치 되는 원본 위치 유지를 보류에 대 한 GUID **InPlaceHolds** 속성에 대 한 값으로 표시 됩니다. 예, 두 비활성 사서함에 대 한 다음과 같은 결과가 Ann Beebe에 배치 되는 소송 보존으로 설정 하 고는 Pilar Pinilla에 배치 되 두 원본 위치 유지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p108">The value of **True** for the **LitigationHoldEnabled** property indicates that the inactive mailbox is on Litigation Hold. If an In-Place Hold is placed on an inactive mailbox, the GUID for the hold is displayed as the value for the **InPlaceHolds** property. For example, the following results for two inactive mailboxes show that a Litigation Hold is placed on Ann Beebe and that two In-Place Holds are placed on Pilar Pinilla.</span></span> 
  
```
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491, ba6f4ba25b62490aaaa253eea27426ab}
```

> [!TIP]
> <span data-ttu-id="73f73-p109">원본 위치 유지 많은 비활성 사서함에 배치 되, 원본 위치 유지 Guid 중 일부만 표시 됩니다. 모든 원본 위치 유지 Guid를 표시 하려면 다음 명령을 실행할 수 있습니다.`Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`</span><span class="sxs-lookup"><span data-stu-id="73f73-p109">If a lot of In-Place Holds are placed on an inactive mailbox, not all of the In-Place Hold GUIDs will be displayed. You can run the following command to display all the In-Place Hold GUIDs:  `Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`</span></span>
  
## <a name="step-2-remove-a-hold-from-an-inactive-mailbox"></a><span data-ttu-id="73f73-140">2 단계: 비활성 사서함에서 보류를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-140">Step 2: Remove a hold from an inactive mailbox</span></span>

<span data-ttu-id="73f73-p110">비활성 사서함에 어떤 유형의 보류 놓입니다 파악 한 후 (및 여러 보존 한지), 다음 단계는 사서함에서 보류를 제거 하는 것입니다. 앞서 설명한 것 처럼 비활성 사서함을 영구적으로 삭제 하려면 모든 보류를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p110">After you identify what type of hold is placed on the inactive mailbox (and whether there are multiple holds), the next step is to remove the holds on the mailbox. As previously stated, you have to remove all holds to permanently delete an inactive mailbox.</span></span> 
  
### <a name="remove-a-litigation-hold"></a><span data-ttu-id="73f73-143">소송 보존을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-143">Remove a Litigation Hold</span></span>

<span data-ttu-id="73f73-p111">앞서 설명한 것 처럼 비활성 사서함에서 소송 보존을 제거 하려면 Windows PowerShell을 사용 해야 합니다. EAC를 사용할 수 없습니다. 소송 보존을 제거 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p111">As previously stated, you have to use Windows PowerShell to remove a Litigation Hold from an inactive mailbox. You can't use the EAC. Run the following command to remove a Litigation Hold.</span></span>
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldEnabled $false
```

> [!TIP]
> <span data-ttu-id="73f73-p112">비활성 사서함을 식별 하는 가장 좋은 방법은 고유 이름 또는 Exchange GUID 값을 사용 하 여 됩니다. 이러한 값 중 하나를 사용 하 여 실수로 잘못 된 사서함을 지정 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p112">The best way to identify an inactive mailbox is by using its Distinguished Name or Exchange GUID value. Using one of these values helps prevent accidentally specifying the wrong mailbox.</span></span> 
  
### <a name="remove-in-place-holds"></a><span data-ttu-id="73f73-149">원본 위치 유지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-149">Remove In-Place Holds</span></span>

 <span data-ttu-id="73f73-150">두 가지 방법으로 비활성 사서함에서 In-place Hold를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-150">There are two ways to remove an In-Place Hold from an inactive mailbox:</span></span> 
  
- <span data-ttu-id="73f73-151">**원본 위치 유지 개체를 삭제 합니다.** 원본 위치 유지 하는 것에 대 한 유일한 원본 사서함을 영구적으로 삭제 하려는 비활성 사서함을 사용 하는 경우에 In-place Hold 개체를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-151">**Delete the In-Place Hold object** If the inactive mailbox that you want to permanently delete is the only source mailbox for an In-Place Hold, you can just delete the In-Place Hold object.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="73f73-p113">원본 위치 유지 개체를 삭제 하기 전에 보류를 사용 하지 않도록 설정 해야 합니다. 원본 위치 유지 된 개체를 사용 하도록 설정 하는 보류를 삭제 하려고 하면 오류 메시지가 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p113">You have to disable the hold before you can delete an In-Place Hold object. If you try to delete an In-Place Hold object that has the hold enabled, you'll receive an error message.</span></span> 
  
- <span data-ttu-id="73f73-154">**원본 위치 유지 원본 사서함으로 비활성 사서함 제거** In-place Hold에 대 한 다른 원본 사서함을 유지 하려는 경우에 원본 사서함의 목록에서 비활성 사서함을 제거할 수 있으며 In-place Hold 개체를 유지 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-154">**Remove the inactive mailbox as a source mailbox of an In-Place Hold** If you want to retain other source mailboxes for an In-Place Hold, you can remove the inactive mailbox from the list of source mailboxes and keep the In-Place Hold object.</span></span> 
    
#### <a name="use-the-eac-to-delete-an-in-place-hold"></a><span data-ttu-id="73f73-155">EAC를 사용 하 여 원본 위치 유지를 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="73f73-155">Use the EAC to delete an In-Place Hold</span></span>

1. <span data-ttu-id="73f73-p114">삭제 하려는 원본 위치 유지의 이름을 알고 있는 경우에 다음 단계를 진행할 수 있습니다. 그렇지 않은 경우 비활성 사서함을 영구적으로 삭제 하려는에 배치 되는 원본 위치 유지의 이름을 가져오려면 다음 명령을 실행 합니다. 얻은 원본 위치 유지 GUID를 사용 하 여 [1 단계: 비활성 사서함에서 보류를 식별](delete-an-inactive-mailbox.md#step1)합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p114">If you know the name of the In-Place Hold that you want to delete, you can go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox that you want to permanently delete. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](delete-an-inactive-mailbox.md#step1).</span></span>
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. <span data-ttu-id="73f73-159">EAC에서 **규정 준수 관리** 로 이동 \> **원본 위치 eDiscovery &amp; 유지**합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-159">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
<span data-ttu-id="73f73-160"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="73f73-160"><<<<<<< HEAD</span></span>
3. <span data-ttu-id="73f73-161">삭제 하려는 원본 위치 유지를 선택 하 고 **편집** 을 클릭 한 다음 ![편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-161">Select the In-Place Hold you want to delete, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
=======
3. <span data-ttu-id="73f73-p115">삭제 하려는 원본 위치 유지를 선택 하 고 **편집**을 클릭 한 다음! [아이콘 편집](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p115">Select the In-Place Hold you want to delete, and then click **Edit**! [Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
>>>>>>> <span data-ttu-id="73f73-164">markjjo 변환</span><span class="sxs-lookup"><span data-stu-id="73f73-164">markjjo-conversion</span></span>
    
4. <span data-ttu-id="73f73-165">**원본 위치 eDiscovery &amp; 유지** 속성 페이지, **원본 위치 유지**를 클릭, **선택한 사서함에서 검색 쿼리 일치에 전체 콘텐츠 유지** 확인란의 선택을 취소 한 다음 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-165">On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**, uncheck the **Place content matching the search query in selected mailboxes on hold** box, and then click **Save**.</span></span>
    
5. <span data-ttu-id="73f73-166">**원본 위치 eDiscovery &amp; 유지** 페이지, 원본 위치 유지를 다시 선택 하 고 **삭제**를 클릭 한 다음![삭제 아이콘](media/87565fbb-5147-4f22-9ed7-1c18ce664392.png)합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-166">On the **In-Place eDiscovery &amp; Hold** page, select the In-Place Hold again, and then click **Delete**![Delete icon](media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span></span>
    
6. <span data-ttu-id="73f73-167">경고에서 **예** 를 원본 위치 유지 삭제를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-167">On the warning, click **Yes** to delete the In-Place Hold.</span></span> 
    
#### <a name="use-exchange-online-powershell-to-delete-an-in-place-hold"></a><span data-ttu-id="73f73-168">Exchange Online PowerShell을 사용 하 여 원본 위치 유지를 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="73f73-168">Use Exchange Online PowerShell to delete an In-Place Hold</span></span>

1. <span data-ttu-id="73f73-p116">삭제 하려는 원본 위치 유지의 속성을 포함 하는 변수를 만듭니다. 얻은 원본 위치 유지 GUID를 사용 하 여 [1 단계: 비활성 사서함에서 보류를 식별](delete-an-inactive-mailbox.md#step1)합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p116">Create a variable that contains the properties of the In-Place Hold that you want to delete. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](delete-an-inactive-mailbox.md#step1).</span></span>
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. <span data-ttu-id="73f73-171">원본 위치 유지에서 보류를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-171">Disable the hold on the In-Place Hold.</span></span>
    
```
  Set-MailboxSearch $InPlaceHold.Name -InPlaceHoldEnabled $false
```

3. <span data-ttu-id="73f73-172">원본 위치에 보류를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-172">Delete the In-Place Hold.</span></span>
    
```
  Remove-MailboxSearch $InPlaceHold.Name
```

#### <a name="use-the-eac-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a><span data-ttu-id="73f73-173">EAC를 사용 하 여 In-place Hold에서 비활성 사서함을 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="73f73-173">Use the EAC to remove an inactive mailbox from an In-Place Hold</span></span>

1. <span data-ttu-id="73f73-p117">비활성 사서함에 배치 된 원본 위치 유지의 이름을 알고 있는 경우에 다음 단계를 진행할 수 있습니다. 그렇지 않은 경우 원본 위치 유지는 사서함에 배치의 이름을 가져오려면 다음 명령을 실행 합니다. 얻은 원본 위치 유지 GUID를 사용 하 여 [1 단계: 비활성 사서함에서 보류를 식별](delete-an-inactive-mailbox.md#step1)합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p117">If you know the name of the In-Place Hold that's placed on the inactive mailbox, you can go to the next step. Otherwise, run the following command to get the name of the In-Place Hold placed on the mailbox. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](delete-an-inactive-mailbox.md#step1).</span></span>
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. <span data-ttu-id="73f73-177">EAC에서 **규정 준수 관리** 로 이동 \> **원본 위치 eDiscovery &amp; 유지**합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-177">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
3. <span data-ttu-id="73f73-178">비활성 사서함에 배치 된 원본 위치 유지를 선택 하 고 **편집** 을 클릭 한 다음 ![편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-178">Select the In-Place Hold that is placed on the inactive mailbox, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
4. <span data-ttu-id="73f73-179">**원본 위치 eDiscovery &amp; 유지** 속성 페이지에서 **소스**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-179">On the **In-Place eDiscovery &amp; Hold** properties page, click **Sources**.</span></span>
    
5. <span data-ttu-id="73f73-180">원본 사서함의 목록에서 제거 하려는 비활성 사서함의 이름을 클릭 하 고 **제거**를 클릭 한 다음![제거 아이콘](media/adf01106-cc79-475c-8673-065371c1897b.gif)합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-180">In the list of source mailboxes, click the name of the inactive mailbox that you want to remove, and then click **Remove**![Remove icon](media/adf01106-cc79-475c-8673-065371c1897b.gif).</span></span>
    
6. <span data-ttu-id="73f73-p118">변경 내용을 저장 하려면 **저장** 을 클릭 합니다. 메시지는 작업이 성공적으로 완료 되었다는 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p118">Click **Save** to save the change. A message is displayed saying the operation was successfully completed.</span></span> 
    
7. <span data-ttu-id="73f73-183">1 ~ 비활성 사서함에 배치 다른 원본 위치 유지를 제거 하는 6 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-183">Repeat steps 1 through 6 to remove other In-Place Holds placed on the inactive mailbox.</span></span>
    
#### <a name="use-exchange-online-powershell-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a><span data-ttu-id="73f73-184">Exchange Online PowerShell을 사용 하 여 In-place Hold에서 비활성 사서함을 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="73f73-184">Use Exchange Online PowerShell to remove an inactive mailbox from an In-Place Hold</span></span>

<span data-ttu-id="73f73-p119">원본 위치 유지 많은 수의 원본 사서함을 포함 하는 경우에 가능한 EAC에서 **원본** 페이지에서 비활성 사서함은 표시 되지 않습니다. 최대 3, 000 사서함은 **원본** 페이지에서을 편집할 때 표시는 원본 위치 유지 합니다. 비활성 사서함이 있는 **원본** 페이지에 나열 되지 않으면 현재 위치 유지에서 제거 하려면 Exchange Online PowerShell를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p119">If the In-Place Hold contains a large number of source mailboxes, it's possible the inactive mailbox won't be listed on the **Sources** page in the EAC. Up to 3,000 mailboxes are displayed on the **Sources** page when you edit an In-Place Hold. If an inactive mailbox isn't listed on the **Sources** page, you can use Exchange Online PowerShell to remove it from the In-Place Hold.</span></span> 
  
1. <span data-ttu-id="73f73-p120">비활성 사서함에 배치 원본 위치 유지의 속성을 포함 하는 변수를 만듭니다. 얻은 원본 위치 유지 GUID를 사용 하 여 [1 단계: 비활성 사서함에서 보류를 식별](delete-an-inactive-mailbox.md#step1)합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p120">Create a variable that contains the properties of the In-Place Hold placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](delete-an-inactive-mailbox.md#step1).</span></span>
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. <span data-ttu-id="73f73-190">원본 위치 유지 하는 것에 대 한 비활성 사서함을 원본 사서함으로 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-190">Verify that the inactive mailbox is listed as a source mailbox for the In-Place Hold.</span></span> 
    
```
  $InPlaceHold.Sources
```

   <span data-ttu-id="73f73-p121">**참고:** 원본 위치 유지 *원본* 속성은 해당 *LegacyExchangeDN* 속성에 의해 원본 사서함을 식별합니다. 이 속성은 비활성 사서함 고유 하 게 식별, 원본 위치 유지에서 *원본* 속성을 사용 하는 잘못 된 사서함을 제거를 방지 합니다. 두 사서함 동일한 별칭 또는 SMTP 주소를 포함 하는 경우 문제를 방지 하기 위해도 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p121">**Note:** The *Sources* property of the In-Place Hold identifies the source mailboxes by their *LegacyExchangeDN* properties. Because this property uniquely identifies inactive mailboxes, using the *Sources* property from the In-Place Hold helps prevent removing the wrong mailbox. This also helps to avoid issues if two mailboxes have the same alias or SMTP address.</span></span> 
   
3. <span data-ttu-id="73f73-p122">변수에 원본 사서함 목록에서 비활성 사서함을 제거 합니다. 이전 단계에서 명령에 의해 반환 되는 비활성 사서함의 **LegacyExchangeDN** 을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p122">Remove the inactive mailbox from the list of source mailboxes in the variable. Be sure to use the **LegacyExchangeDN** of the inactive mailbox that's returned by the command in the previous step.</span></span> 
    
```
  $InPlaceHold.Sources.Remove("<LegacyExchangeDN of the inactive mailbox>")
```

    For example, the following command removes the inactive mailbox for Pilar Pinilla.
    
  ```
  $InPlaceHold.Sources.Remove("/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=9c8dfff651ec4908950f5df60cbbda06-pilarp")
  ```

4. <span data-ttu-id="73f73-196">비활성 사서함 변수에 원본 사서함 목록에서 제거를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-196">Verify that the inactive mailbox is removed from the list of source mailboxes in the variable.</span></span>
    
```
  $InPlaceHold.Sources
```

5. <span data-ttu-id="73f73-197">비활성 사서함을 포함 하지는 원본 사서함의 업데이트 된 목록을 사용 하 여 원본 위치 유지를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-197">Modify the In-Place Hold with the updated list of source mailboxes, which doesn't include the inactive mailbox.</span></span>
    
```
  Set-MailboxSearch $InPlaceHold.Name -SourceMailboxes $InPlaceHold.Sources
```

6. <span data-ttu-id="73f73-198">원본 위치 유지 하는 것에 대 한 원본 사서함 목록에서 비활성 사서함을 제거를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-198">Verify that the inactive mailbox is removed from the list of source mailboxes for the In-Place Hold.</span></span>
    
```
  Get-MailboxSearch $InPlaceHold.Name | FL Sources
```

## <a name="more-information"></a><span data-ttu-id="73f73-199">추가 정보</span><span class="sxs-lookup"><span data-stu-id="73f73-199">More information</span></span>

- <span data-ttu-id="73f73-p123">**비활성 사서함을 사용 하면 일시 삭제 된 사서함의 형식이.** Exchange Online에서 일시 삭제 된 사서함: 특정 보존 기간 내에서 복구할 수 있지만 삭제 된 사서함 Exchange Online에서 일시 삭제 된 사서함 보존 기간 30 일입니다. 즉, 사서함 삭제 되 고 소프트-30 일 이내 복구할 수 있습니다. 30 일 후 일시 삭제 된 사서함 영구적으로 삭제에 대 한 표시 하 고 복구할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p123">**An inactive mailbox is a type of soft-deleted mailbox.** In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period. The soft-deleted mailbox retention period in Exchange Online is 30 days. This means that the mailbox can be recovered within 30 days of being soft-deleted. After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered.</span></span> 
    
- <span data-ttu-id="73f73-p124">**비활성 사서함에서 보류를 제거한 후 어떻게 됩니까?** 사서함 다른 일시 삭제 된 사서함 처럼 인식 되 고 30 일 일시 삭제 된 사서함 보존 기간이 만료 후 영구적으로 삭제를 위해 표시 됩니다. 이 보존 기간 때 사서함을 처음 설정한 비활성 날짜에 시작 합니다. 이 날짜를 날짜 해당 Office 365 사용자 계정이 삭제 되었습니다 또는 **Remove-mailbox** cmdlet을 통해 Exchange Online 사서함을 삭제 하는 경우 일시 삭제 된 날짜를 라고 합니다. 일시 삭제 된 날짜 보류를 제거 하는 날짜를 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p124">**What happens after you remove the hold on an inactive mailbox?** The mailbox is treated like other soft-deleted mailboxes and is marked for permanent deletion after the 30-day soft-deleted mailbox retention period expires. This retention period starts on the date when the mailbox was first made inactive. This date is known as the soft-deleted date, which is the date the corresponding Office 365 user account was deleted or when the Exchange Online mailbox was deleted with the **Remove-Mailbox** cmdlet. The soft-deleted date isn't the date on which you remove the hold.</span></span> 
    
- <span data-ttu-id="73f73-p125">**보존이 제거 된 후에 즉시 영구적으로 삭제 비활성 사서함은?** 비활성 사서함에 대 한 일시 삭제 된 날짜를 30 일 보다 오래 된 경우 보류를 제거 하는 즉시 영구적으로 사서함 삭제 되지 않습니다. 사서함은 영구적으로 삭제에 대 한 표시 하 고 처리 하는 다음 번 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p125">**Is an inactive mailbox permanently deleted immediately after the hold is removed?** If the soft-deleted date for an inactive mailbox is older than 30 days, the mailbox won't be permanently deleted as soon as you remove the hold. The mailbox will be marked for permanent deletion and is deleted the next time it's processed.</span></span> 
    
- <span data-ttu-id="73f73-p126">**일시 삭제 된 사서함 보존 기간에 주는 영향은 비활성 사서함?** 비활성 사서함에 대 한 일시 삭제 된 날짜 보류에서 제거 된 날짜 이전 30 일이 지난 경우 영구적으로 삭제에 대 한 사서함 된다고 나타납니다. 하지만 일시 삭제 된 사서함 보존 기간이 만료 될 때까지 사서함 비활성 사서함의 일시 삭제 된 날짜가 지난 30 일 내에서 보류를 제거 하는 경우 복구할 수 있습니다. 자세한 내용은, [삭제 또는 Exchange Online 사용자 사서함을 복원](https://go.microsoft.com/fwlink/?linkid=856835)을 참조 하십시오. 일시 삭제 된 사서함 보존 기간이 만료 되 면 후 비활성 사서함을 복구 하기 위한 절차에 따라 포함 합니다. 자세한 내용은 [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p126">**How does the soft-deleted mailbox retention period affect inactive mailboxes?** If the soft-deleted date for an inactive mailbox is more than 30 days before the date the hold was removed, the mailbox is marked for permanent deletion. But if an inactive mailbox has a soft-deleted date within the last 30 days and you remove the hold, you can recover the mailbox up until the soft-deleted mailbox retention period expires. For details, see [Delete or restore user mailboxes in Exchange Online](https://go.microsoft.com/fwlink/?linkid=856835). After the soft-deleted mailbox retention period expires, you have follow the procedures for recovering an inactive mailbox. For details, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="73f73-p127">**을 표시 하려면 어떻게 비활성 사서함에 대 한 정보 보존이 제거 후?** 보류에서 제거 된 후 일시 삭제 된 사서함에 다시 비활성 사서함은으로 **Get-mailbox** cmdlet과 함께 *InactiveMailboxOnly* 매개 변수를 사용 하 여 반환 되지 않습니다. 하지만 **Get-mailbox SoftDeletedMailbox** 명령을 사용 하 여 사서함에 대 한 정보를 표시할 수 있습니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="73f73-p127">**How do you display information about an inactive mailbox after the hold is removed?** After a hold is removed and the inactive mailbox is reverted back to a soft-deleted mailbox, it won't be returned by using the  *InactiveMailboxOnly*  parameter with the **Get-Mailbox** cmdlet. But you can display information about the mailbox by using the **Get-Mailbox -SoftDeletedMailbox** command. For example:</span></span> 
    
```
  Get-Mailbox -SoftDeletedMailbox -Identity pilarp | FL Name,Identity,LitigationHoldEnabled,In
  Placeholds,WhenSoftDeleted,IsInactiveMailbox
  Name                   : pilarp
  Identity               : Soft Deleted Objects\pilarp
  LitigationHoldEnabled  : False
  InPlaceHolds           : {}
  WhenSoftDeleted        : 10/30/2014 1:19:04 AM
  IsInactiveMailbox      : False
```
  
<span data-ttu-id="73f73-p128">위의 예제에서는 *WhenSoftDeleted* 속성은이 예에서 2014 년 10 월 30,이 일시 삭제 된 날짜를 식별 합니다. 일시 삭제 된 사서함이 된 경우 이전에 보류 제거 된 비활성 사서함, *WhenSoftDeleted* 속성의 값 후 30 일을 영구적으로 삭제 됩니다. 이 경우에 사서함이 2014 년 11 월 30, 후 영구적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f73-p128">In the above example, the *WhenSoftDeleted* property identifies the soft-deleted date, which in this example is October 30, 2014. If this soft-deleted mailbox was previously an inactive mailbox for which the hold was removed, it will be permanently deleted 30 days after the value of the *WhenSoftDeleted* property. In this case, the mailbox is permanently deleted after November 30, 2014.</span></span>

