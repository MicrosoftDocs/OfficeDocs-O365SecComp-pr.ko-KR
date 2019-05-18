---
title: Office 365에서 비활성 사서함 삭제
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: f5caf497-5e8d-4b7a-bfff-d02942f38150
description: 더 이상 Office 365 비활성 사서함의 내용을 보존 하지 않아도 되는 경우에는 보류를 제거 하 여 비활성 사서함을 영구적으로 삭제할 수 있습니다. 보류를 제거한 후 비활성 사서함은 삭제 되도록 표시 되 고 처리 된 후 영구적으로 삭제 됩니다.
ms.openlocfilehash: b6cea7284ccb930ef10ec96c082291acb9f66f2f
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150470"
---
# <a name="delete-an-inactive-mailbox-in-office-365"></a><span data-ttu-id="cda46-104">Office 365에서 비활성 사서함 삭제</span><span class="sxs-lookup"><span data-stu-id="cda46-104">Delete an inactive mailbox in Office 365</span></span>

<span data-ttu-id="cda46-105">비활성 사서함은 직원이 퇴사한 후에 해당 전자 메일을 유지하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-105">An inactive mailbox is used to preserve a former employee's email after he or she leaves your organization.</span></span> <span data-ttu-id="cda46-106">비활성 사서함의 콘텐츠를 더 이상 보존할 필요가 없는 경우에는 보류를 제거 하 여 비활성 사서함을 영구적으로 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-106">When you no longer need to preserve the contents of an inactive mailbox, you can permanently delete the inactive mailbox by removing the hold.</span></span> <span data-ttu-id="cda46-107">또한 비활성 사서함에 여러 보류가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-107">Also, it's possible that multiple holds might be placed on an inactive mailbox.</span></span> <span data-ttu-id="cda46-108">예를 들어 비활성 사서함은 소송 보존 및 하나 이상의 원본 위치 유지에 배치 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-108">For example, an inactive mailbox might be placed on Litigation Hold and on one or more In-Place Holds.</span></span> <span data-ttu-id="cda46-109">또한 office 365 또는 Microsoft 365의 보안 및 준수 센터에서 만든 Office 365 보존 정책이 비활성 사서함에 적용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-109">Additionally, an Office 365 retention policy (created in the security and compliance center in Office 365 or Microsoft 365) might be applied to the inactive mailbox.</span></span> <span data-ttu-id="cda46-110">비활성 사서함에서 모든 보류 및 Office 365 보존 정책을 제거 하 여 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-110">You have to remove all holds and Office 365 retention policies from an inactive mailbox to delete it.</span></span> <span data-ttu-id="cda46-111">보류 및 보존 정책을 제거한 후 비활성 사서함은 삭제 되도록 표시 되며 처리 된 후 영구적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-111">After you remove the holds and retention policies, the inactive mailbox is marked for deletion and is permanently deleted after it's processed.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="cda46-p103">사서함을 비활성화하기 위해 새 원본 위치 유지를 만들 수 있는 2017년 7월 1일 마감 날짜를 연기했습니다. 하지만 올해 말이나 내년 초에는 Exchange Online에 새 원본 위치 유지를 만들 수 없습니다. 그때는 소송 보존과 Office 365 보존 정책만 사용하여 비활성화 사서함을 만들 수 있습니다. 그러나 원본 위치 유지에 있는 기존 비활성화 사서함은 계속 지원되며 비활성화 사서함에서 원본 위치 유지를 계속 관리할 수 있습니다. 관리 항목으로는 원본 위치 유지 기간 변경 및 원본 위치 유지를 삭제하여 비활성화 사서함을 영구 삭제하는 작업이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds to make a mailbox inactive. But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. At that time, only Litigation Holds and Office 365 retention policies can be used to create an inactive mailbox. However, existing inactive mailboxes that are on In-Place Hold will still be supported, and you can continue to manage the In-Place Holds on inactive mailboxes. This includes changing the duration of an In-Place Hold and permanently deleting an inactive mailbox by removing the In-Place Hold.</span></span> 
  
<span data-ttu-id="cda46-117">비활성 사서함에서 보류가 제거 된 후 발생 하는 작업에 대 한 설명을 보려면 [추가 정보](#more-information) 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cda46-117">See the [More information](#more-information) section for a description of what happens after holds are removed from an inactive mailbox.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="cda46-118">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="cda46-118">Before you begin</span></span>

- <span data-ttu-id="cda46-119">Exchange Online PowerShell을 사용 하 여 비활성 사서함에서 소송 보존을 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-119">You have to use Exchange Online PowerShell to remove a Litigation Hold from an inactive mailbox.</span></span> <span data-ttu-id="cda46-120">EAC(Exchange 관리 센터)는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-120">You can't use the Exchange admin center (EAC).</span></span> <span data-ttu-id="cda46-121">단계별 지침은 [Exchange Online PowerShell에 연결을](https://go.microsoft.com/fwlink/?linkid=396554)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cda46-121">For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).</span></span> <span data-ttu-id="cda46-122">Exchange Online PowerShell 또는 EAC를 사용 하 여 비활성 사서함에서 원본 위치 유지를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-122">You can use Exchange Online PowerShell or the EAC to remove an In-Place Hold from an inactive mailbox.</span></span> 
    
- <span data-ttu-id="cda46-123">보류를 제거 하 고 비활성 사서함을 삭제 하기 전에 비활성 사서함의 내용을 다른 사서함에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-123">You can copy the contents of an inactive mailbox to another mailbox before you remove the hold and delete an inactive mailbox.</span></span> <span data-ttu-id="cda46-124">자세한 내용은 [Office 365에서 비활성 사서함 복원을](restore-an-inactive-mailbox.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cda46-124">For details, see [Restore an inactive mailbox in Office 365](restore-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="cda46-125">비활성 사서함에서 보류 또는 Office 365 보존 정책을 제거 하는 경우 사서함의 일시 삭제 된 사서함 보존 기간이 만료 되 면 사서함이 영구적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-125">If you remove the hold or Office 365 retention policy from an inactive mailbox and the soft-deleted mailbox retention period for the mailbox has expired, the mailbox will be permanently deleted.</span></span> <span data-ttu-id="cda46-126">삭제 된 후에는 복구할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-126">After it's deleted, it can't be recovered.</span></span> <span data-ttu-id="cda46-127">보류를 제거 하기 전에 사서함의 내용이 더 이상 필요 하지 않은지 확인해 보십시오.</span><span class="sxs-lookup"><span data-stu-id="cda46-127">Before you remove the hold, be sure that you no longer need the contents in the mailbox.</span></span> <span data-ttu-id="cda46-128">비활성 사서함을 다시 활성화 하려면 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-128">If you want to re-activate an inactive mailbox, you can recover it.</span></span> <span data-ttu-id="cda46-129">자세한 내용은 [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cda46-129">For details, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="cda46-130">비활성 사서함에 대 한 자세한 내용은 [Office 365의 비활성 사서함](inactive-mailboxes-in-office-365.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cda46-130">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a><span data-ttu-id="cda46-131">1 단계: 비활성 사서함의 보류 확인</span><span class="sxs-lookup"><span data-stu-id="cda46-131">Step 1: Identify the holds on an inactive mailbox</span></span>

<span data-ttu-id="cda46-132">앞에서 설명한 것 처럼 소송 보존, 원본 위치 유지 또는 Office 365 보관 정책이 비활성 사서함에 배치 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-132">As previously stated, a Litigation Hold, In-Place Hold, or Office 365 retention policy might be placed on an inactive mailbox.</span></span> <span data-ttu-id="cda46-133">첫 번째 단계는 비활성 사서함에 대 한 보류를 확인 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-133">The first step is to identify the holds on an inactive mailbox.</span></span>
  
<span data-ttu-id="cda46-134">다음 명령을 실행 하 여 조직의 모든 비활성 사서함에 대 한 보류 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-134">Run the following command to display the hold information for all inactive mailboxes in your organization.</span></span>
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,InPlaceHolds
```

<span data-ttu-id="cda46-135">**LitigationHoldEnabled** 속성의 **True** 값은 비활성 사서함이 소송 보존 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-135">The value of **True** for the **LitigationHoldEnabled** property indicates that the inactive mailbox is on Litigation Hold.</span></span> <span data-ttu-id="cda46-136">비활성 사서함에 원본 위치 유지를 적용 하면 보류에 대 한 GUID가 **InPlaceHolds** 속성의 값으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-136">If an In-Place Hold is placed on an inactive mailbox, the GUID for the hold is displayed as the value for the **InPlaceHolds** property.</span></span> <span data-ttu-id="cda46-137">예를 들어 두 비활성 사서함에 대 한 다음 결과는 소송 보존을 Ann Beebe에 배치 하 고 두 개의 원본 위치 유지가 Pilar Pinilla에 배치 된다는 것을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-137">For example, the following results for two inactive mailboxes show that a Litigation Hold is placed on Ann Beebe and that two In-Place Holds are placed on Pilar Pinilla.</span></span> 
  
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
> <span data-ttu-id="cda46-138">전체 원본 위치 유지가 비활성 사서함에 배치 되는 경우에는 원본 위치 유지 Guid 중 일부가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-138">If a lot of In-Place Holds are placed on an inactive mailbox, not all of the In-Place Hold GUIDs will be displayed.</span></span> <span data-ttu-id="cda46-139">다음 명령을 실행 하 여 모든 원본 위치 유지 Guid를 표시할 수 있습니다.`Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`</span><span class="sxs-lookup"><span data-stu-id="cda46-139">You can run the following command to display all the In-Place Hold GUIDs:  `Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`</span></span>
  
## <a name="step-2-remove-a-hold-from-an-inactive-mailbox"></a><span data-ttu-id="cda46-140">2 단계: 비활성 사서함에서 보류 제거</span><span class="sxs-lookup"><span data-stu-id="cda46-140">Step 2: Remove a hold from an inactive mailbox</span></span>

<span data-ttu-id="cda46-141">비활성 사서함에 적용 되는 보존 유형 및 여러 보류가 있는지 확인 한 후에는 사서함에서 보류를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-141">After you identify what type of hold is placed on the inactive mailbox (and whether there are multiple holds), the next step is to remove the holds on the mailbox.</span></span> <span data-ttu-id="cda46-142">앞에서 설명한 것 처럼 비활성 사서함을 영구적으로 삭제 하려면 모든 보류를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-142">As previously stated, you have to remove all holds to permanently delete an inactive mailbox.</span></span> 
  
### <a name="remove-a-litigation-hold"></a><span data-ttu-id="cda46-143">소송 보존 제거</span><span class="sxs-lookup"><span data-stu-id="cda46-143">Remove a Litigation Hold</span></span>

<span data-ttu-id="cda46-144">앞에서 설명한 것 처럼, Windows PowerShell을 사용 하 여 비활성 사서함에서 소송 보존을 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-144">As previously stated, you have to use Windows PowerShell to remove a Litigation Hold from an inactive mailbox.</span></span> <span data-ttu-id="cda46-145">EAC는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-145">You can't use the EAC.</span></span> <span data-ttu-id="cda46-146">다음 명령을 실행 하 여 소송 보존을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-146">Run the following command to remove a Litigation Hold.</span></span>
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldEnabled $false
```

> [!TIP]
> <span data-ttu-id="cda46-147">비활성 사서함을 식별 하는 가장 좋은 방법은 해당 고유 이름이 나 Exchange GUID 값을 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-147">The best way to identify an inactive mailbox is by using its Distinguished Name or Exchange GUID value.</span></span> <span data-ttu-id="cda46-148">이러한 값 중 하나를 사용 하면 실수로 잘못 된 사서함을 지정 하는 것을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-148">Using one of these values helps prevent accidentally specifying the wrong mailbox.</span></span> 
  
### <a name="remove-in-place-holds"></a><span data-ttu-id="cda46-149">원본 위치 유지 제거</span><span class="sxs-lookup"><span data-stu-id="cda46-149">Remove In-Place Holds</span></span>

 <span data-ttu-id="cda46-150">비활성 사서함에서 원본 위치 유지를 제거 하는 방법에는 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-150">There are two ways to remove an In-Place Hold from an inactive mailbox:</span></span> 
  
- <span data-ttu-id="cda46-151">원본 **위치 유지 개체 삭제** 영구적으로 삭제 하려는 비활성 사서함이 원본 위치 유지를 위한 유일한 사서함 인 경우 현재 위치 유지 개체만 삭제 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-151">**Delete the In-Place Hold object** If the inactive mailbox that you want to permanently delete is the only source mailbox for an In-Place Hold, you can just delete the In-Place Hold object.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="cda46-152">원본 위치 유지 개체를 삭제 하려면 먼저 보류를 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-152">You have to disable the hold before you can delete an In-Place Hold object.</span></span> <span data-ttu-id="cda46-153">보류가 사용 되도록 설정 된 원본 위치 유지 개체를 삭제 하려고 하면 오류 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-153">If you try to delete an In-Place Hold object that has the hold enabled, you'll receive an error message.</span></span> 
  
- <span data-ttu-id="cda46-154">**비활성 사서함을 원본 위치 유지의 소스 사서함으로 제거** 원본 위치 유지를 위해 다른 원본 사서함을 유지 하려는 경우 소스 사서함 목록에서 비활성 사서함을 제거 하 고 현재 위치 유지 개체를 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-154">**Remove the inactive mailbox as a source mailbox of an In-Place Hold** If you want to retain other source mailboxes for an In-Place Hold, you can remove the inactive mailbox from the list of source mailboxes and keep the In-Place Hold object.</span></span> 
    
#### <a name="use-the-eac-to-delete-an-in-place-hold"></a><span data-ttu-id="cda46-155">EAC를 사용 하 여 원본 위치 유지 삭제</span><span class="sxs-lookup"><span data-stu-id="cda46-155">Use the EAC to delete an In-Place Hold</span></span>

1. <span data-ttu-id="cda46-156">삭제할 원본 위치 유지의 이름을 알고 있는 경우 다음 단계를 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-156">If you know the name of the In-Place Hold that you want to delete, you can go to the next step.</span></span> <span data-ttu-id="cda46-157">그렇지 않으면 다음 명령을 실행 하 여 영구적으로 삭제 하려는 비활성 사서함에 저장 된 원본 위치 유지의 이름을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-157">Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox that you want to permanently delete.</span></span> <span data-ttu-id="cda46-158">[1 단계: 비활성 사서함에서 보류 확인](#step-1-identify-the-holds-on-an-inactive-mailbox)에서 얻은 원본 위치 유지 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-158">Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. <span data-ttu-id="cda46-159">EAC에서 **규정 준수 관리** \> 원본 \*\* &amp; 위치 eDiscovery 유지\*\*로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-159">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
3. <span data-ttu-id="cda46-160">삭제할 원본 위치 유지를 선택 하 고 편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) **편집** ![을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-160">Select the In-Place Hold you want to delete, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
4. <span data-ttu-id="cda46-161">원본 \*\* &amp; 위치 eDiscovery 보류\*\* 속성 페이지에서 원본 **위치 유지**를 클릭 하 고 **선택한 사서함에 있는 검색 쿼리와 일치 하는 콘텐츠를 보류에** 저장 상자를 선택 취소 한 후에 **Save**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-161">On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**, uncheck the **Place content matching the search query in selected mailboxes on hold** box, and then click **Save**.</span></span>
    
5. <span data-ttu-id="cda46-162">원본 **위치 eDiscovery &amp; 유지** 페이지에서 원본 위치 유지를 다시 선택한 다음 삭제 아이콘 \*\*\*\*![](media/87565fbb-5147-4f22-9ed7-1c18ce664392.png)삭제를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-162">On the **In-Place eDiscovery &amp; Hold** page, select the In-Place Hold again, and then click **Delete**![Delete icon](media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span></span>
    
6. <span data-ttu-id="cda46-163">경고에서 **예** 를 클릭 하 여 원본 위치 유지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-163">On the warning, click **Yes** to delete the In-Place Hold.</span></span> 
    
#### <a name="use-exchange-online-powershell-to-delete-an-in-place-hold"></a><span data-ttu-id="cda46-164">Exchange Online PowerShell을 사용 하 여 원본 위치 유지 삭제</span><span class="sxs-lookup"><span data-stu-id="cda46-164">Use Exchange Online PowerShell to delete an In-Place Hold</span></span>

1. <span data-ttu-id="cda46-165">삭제할 원본 위치 유지의 속성을 포함 하는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-165">Create a variable that contains the properties of the In-Place Hold that you want to delete.</span></span> <span data-ttu-id="cda46-166">[1 단계: 비활성 사서함에서 보류 확인](#step-1-identify-the-holds-on-an-inactive-mailbox)에서 얻은 원본 위치 유지 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-166">Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. <span data-ttu-id="cda46-167">원본 위치 유지에 대 한 보류를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-167">Disable the hold on the In-Place Hold.</span></span>
    
```
  Set-MailboxSearch $InPlaceHold.Name -InPlaceHoldEnabled $false
```

3. <span data-ttu-id="cda46-168">원본 위치 유지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-168">Delete the In-Place Hold.</span></span>
    
```
  Remove-MailboxSearch $InPlaceHold.Name
```

#### <a name="use-the-eac-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a><span data-ttu-id="cda46-169">EAC를 사용 하 여 원본 위치 유지에서 비활성 사서함 제거</span><span class="sxs-lookup"><span data-stu-id="cda46-169">Use the EAC to remove an inactive mailbox from an In-Place Hold</span></span>

1. <span data-ttu-id="cda46-170">비활성 사서함에 배치 된 원본 위치 유지의 이름을 알고 있는 경우 다음 단계를 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-170">If you know the name of the In-Place Hold that's placed on the inactive mailbox, you can go to the next step.</span></span> <span data-ttu-id="cda46-171">그렇지 않으면 다음 명령을 실행 하 여 사서함에 배치 된 원본 위치 유지의 이름을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-171">Otherwise, run the following command to get the name of the In-Place Hold placed on the mailbox.</span></span> <span data-ttu-id="cda46-172">[1 단계: 비활성 사서함에서 보류 확인](#step-1-identify-the-holds-on-an-inactive-mailbox)에서 얻은 원본 위치 유지 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-172">Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. <span data-ttu-id="cda46-173">EAC에서 **규정 준수 관리** \> 원본 \*\* &amp; 위치 eDiscovery 유지\*\*로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-173">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
3. <span data-ttu-id="cda46-174">비활성 사서함에 저장 된 원본 위치 유지를 선택 하 고 편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) **편집** ![을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-174">Select the In-Place Hold that is placed on the inactive mailbox, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
4. <span data-ttu-id="cda46-175">원본 **위치 eDiscovery &amp; 보류** 속성 페이지에서 **원본을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-175">On the **In-Place eDiscovery &amp; Hold** properties page, click **Sources**.</span></span>
    
5. <span data-ttu-id="cda46-176">원본 사서함 목록에서 제거 하려는 비활성 사서함의 이름을 클릭 하 고 제거 아이콘](media/adf01106-cc79-475c-8673-065371c1897b.gif) **제거**![를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-176">In the list of source mailboxes, click the name of the inactive mailbox that you want to remove, and then click **Remove**![Remove icon](media/adf01106-cc79-475c-8673-065371c1897b.gif).</span></span>
    
6. <span data-ttu-id="cda46-177">**저장**을 클릭하여 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-177">Click **Save** to save the change.</span></span> <span data-ttu-id="cda46-178">작업이 성공적으로 완료 되었음을 알리는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-178">A message is displayed saying the operation was successfully completed.</span></span> 
    
7. <span data-ttu-id="cda46-179">비활성 사서함에 저장 된 다른 원본 위치 유지를 제거 하려면 1 ~ 6 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-179">Repeat steps 1 through 6 to remove other In-Place Holds placed on the inactive mailbox.</span></span>
    
#### <a name="use-exchange-online-powershell-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a><span data-ttu-id="cda46-180">Exchange Online PowerShell을 사용 하 여 원본 위치 유지에서 비활성 사서함 제거</span><span class="sxs-lookup"><span data-stu-id="cda46-180">Use Exchange Online PowerShell to remove an inactive mailbox from an In-Place Hold</span></span>

<span data-ttu-id="cda46-181">원본 사서함의 수가 많은 경우에는 비활성 사서함이 EAC의 **원본** 페이지에 나열 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-181">If the In-Place Hold contains a large number of source mailboxes, it's possible the inactive mailbox won't be listed on the **Sources** page in the EAC.</span></span> <span data-ttu-id="cda46-182">원본 위치 유지를 편집 하면 **소스** 페이지에 최대 3000의 사서함이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-182">Up to 3,000 mailboxes are displayed on the **Sources** page when you edit an In-Place Hold.</span></span> <span data-ttu-id="cda46-183">비활성 사서함이 **원본** 페이지에 나열 되지 않은 경우 Exchange Online PowerShell을 사용 하 여 현재 위치 유지에서 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-183">If an inactive mailbox isn't listed on the **Sources** page, you can use Exchange Online PowerShell to remove it from the In-Place Hold.</span></span> 
  
1. <span data-ttu-id="cda46-184">비활성 사서함에 배치 된 원본 위치 유지의 속성을 포함 하는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-184">Create a variable that contains the properties of the In-Place Hold placed on the inactive mailbox.</span></span> <span data-ttu-id="cda46-185">[1 단계: 비활성 사서함에서 보류 확인](#step-1-identify-the-holds-on-an-inactive-mailbox)에서 얻은 원본 위치 유지 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-185">Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. <span data-ttu-id="cda46-186">비활성 사서함이 현재 위치 유지에 대 한 원본 사서함으로 나열 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-186">Verify that the inactive mailbox is listed as a source mailbox for the In-Place Hold.</span></span> 
    
```
  $InPlaceHold.Sources
```

   <span data-ttu-id="cda46-187">**참고:** 원본 위치 유지의 *Sources* 속성은 소스 사서함을 해당 *LegacyExchangeDN* 속성으로 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-187">**Note:** The *Sources* property of the In-Place Hold identifies the source mailboxes by their *LegacyExchangeDN* properties.</span></span> <span data-ttu-id="cda46-188">이 속성은 비활성 사서함을 고유 하 게 식별 하므로 원본 위치 유지의 *Sources* 속성을 사용 하면 잘못 된 사서함을 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-188">Because this property uniquely identifies inactive mailboxes, using the *Sources* property from the In-Place Hold helps prevent removing the wrong mailbox.</span></span> <span data-ttu-id="cda46-189">이는 두 사서함의 별칭이 나 SMTP 주소가 같을 때 발생 하는 문제를 방지 하는 데도 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-189">This also helps to avoid issues if two mailboxes have the same alias or SMTP address.</span></span> 
   
3. <span data-ttu-id="cda46-190">변수의 원본 사서함 목록에서 비활성 사서함을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-190">Remove the inactive mailbox from the list of source mailboxes in the variable.</span></span> <span data-ttu-id="cda46-191">이전 단계에서 명령에 의해 반환 되는 비활성 사서함의 **LegacyExchangeDN** 을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-191">Be sure to use the **LegacyExchangeDN** of the inactive mailbox that's returned by the command in the previous step.</span></span> 
    
```
  $InPlaceHold.Sources.Remove("<LegacyExchangeDN of the inactive mailbox>")
```

    For example, the following command removes the inactive mailbox for Pilar Pinilla.
    
  ```
  $InPlaceHold.Sources.Remove("/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=9c8dfff651ec4908950f5df60cbbda06-pilarp")
  ```

4. <span data-ttu-id="cda46-192">비활성 사서함이 변수의 원본 사서함 목록에서 제거 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-192">Verify that the inactive mailbox is removed from the list of source mailboxes in the variable.</span></span>
    
```
  $InPlaceHold.Sources
```

5. <span data-ttu-id="cda46-193">비활성 사서함이 포함 되지 않은 업데이트 된 원본 사서함 목록을 사용 하 여 현재 위치 유지를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-193">Modify the In-Place Hold with the updated list of source mailboxes, which doesn't include the inactive mailbox.</span></span>
    
```
  Set-MailboxSearch $InPlaceHold.Name -SourceMailboxes $InPlaceHold.Sources
```

6. <span data-ttu-id="cda46-194">현재 위치 유지를 위해 비활성 사서함이 원본 사서함 목록에서 제거 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-194">Verify that the inactive mailbox is removed from the list of source mailboxes for the In-Place Hold.</span></span>
    
```
  Get-MailboxSearch $InPlaceHold.Name | FL Sources
```

## <a name="more-information"></a><span data-ttu-id="cda46-195">추가 정보</span><span class="sxs-lookup"><span data-stu-id="cda46-195">More information</span></span>

- <span data-ttu-id="cda46-196">**비활성 사서함은 일시 삭제 된 사서함의 유형입니다.**</span><span class="sxs-lookup"><span data-stu-id="cda46-196">**An inactive mailbox is a type of soft-deleted mailbox.**</span></span> <span data-ttu-id="cda46-197">Exchange Online에서 일시 삭제 된 사서함은 삭제 되었지만 특정 보존 기간 내에 복구할 수 있는 사서함입니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-197">In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period.</span></span> <span data-ttu-id="cda46-198">Exchange Online의 일시 삭제 된 사서함 보존 기간은 30 일입니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-198">The soft-deleted mailbox retention period in Exchange Online is 30 days.</span></span> <span data-ttu-id="cda46-199">즉, 사서함이 일시 삭제 된 30 일 이내에 복구 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-199">This means that the mailbox can be recovered within 30 days of being soft-deleted.</span></span> <span data-ttu-id="cda46-200">30 일이 지나면 일시 삭제 된 사서함이 영구적으로 삭제 되도록 표시 되며 복구할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-200">After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered.</span></span> 
    
- <span data-ttu-id="cda46-201">**비활성 사서함에서 보류를 제거한 후에 수행 되는 작업**</span><span class="sxs-lookup"><span data-stu-id="cda46-201">**What happens after you remove the hold on an inactive mailbox?**</span></span> <span data-ttu-id="cda46-202">사서함은 일시적으로 삭제 된 다른 사서함 처럼 취급 되며 30 일 일시 삭제 된 사서함 보존 기간이 만료 되 면 영구 삭제로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-202">The mailbox is treated like other soft-deleted mailboxes and is marked for permanent deletion after the 30-day soft-deleted mailbox retention period expires.</span></span> <span data-ttu-id="cda46-203">이 보존 기간은 사서함을 처음으로 비활성화 한 날짜에 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-203">This retention period starts on the date when the mailbox was first made inactive.</span></span> <span data-ttu-id="cda46-204">이 날짜는 일시 삭제 된 날짜, 즉 해당 Office 365 사용자 계정이 삭제 되었거나 **사서함 제거** cmdlet을 사용 하 여 Exchange Online 사서함이 삭제 된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-204">This date is known as the soft-deleted date, which is the date the corresponding Office 365 user account was deleted or when the Exchange Online mailbox was deleted with the **Remove-Mailbox** cmdlet.</span></span> <span data-ttu-id="cda46-205">일시 삭제 된 날짜는 보류를 제거한 날짜가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-205">The soft-deleted date isn't the date on which you remove the hold.</span></span> 
    
- <span data-ttu-id="cda46-206">**비활성 사서함이 보존을 제거한 즉시 영구적으로 삭제 됩니까?**</span><span class="sxs-lookup"><span data-stu-id="cda46-206">**Is an inactive mailbox permanently deleted immediately after the hold is removed?**</span></span> <span data-ttu-id="cda46-207">비활성 사서함의 일시 삭제 된 날짜가 30 일 보다 오래 된 경우 보존을 제거 하는 즉시 사서함이 영구적으로 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-207">If the soft-deleted date for an inactive mailbox is older than 30 days, the mailbox won't be permanently deleted as soon as you remove the hold.</span></span> <span data-ttu-id="cda46-208">사서함은 영구적으로 삭제 되도록 표시 되며 다음에 처리 될 때 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-208">The mailbox will be marked for permanent deletion and is deleted the next time it's processed.</span></span> 
    
- <span data-ttu-id="cda46-209">**일시 삭제 된 사서함 보존 기간은 비활성 사서함에 어떤 영향을 줍니까?**</span><span class="sxs-lookup"><span data-stu-id="cda46-209">**How does the soft-deleted mailbox retention period affect inactive mailboxes?**</span></span> <span data-ttu-id="cda46-210">비활성 사서함의 일시 삭제 된 날짜가 보존을 제거한 날짜 보다 30 일 보다 많은 경우에는 사서함이 영구적으로 삭제 되도록 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-210">If the soft-deleted date for an inactive mailbox is more than 30 days before the date the hold was removed, the mailbox is marked for permanent deletion.</span></span> <span data-ttu-id="cda46-211">그러나 비활성 사서함의 지난 30 일 이내에 일시 삭제 된 날짜가 있고 보존을 제거 하면 일시 삭제 된 사서함 보존 기간이 만료 될 때까지 사서함을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-211">But if an inactive mailbox has a soft-deleted date within the last 30 days and you remove the hold, you can recover the mailbox up until the soft-deleted mailbox retention period expires.</span></span> <span data-ttu-id="cda46-212">자세한 내용은 [Exchange Online에서 사용자 사서함 삭제 또는 복원을](https://go.microsoft.com/fwlink/?linkid=856835)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cda46-212">For details, see [Delete or restore user mailboxes in Exchange Online](https://go.microsoft.com/fwlink/?linkid=856835).</span></span> <span data-ttu-id="cda46-213">일시 삭제 된 사서함 보존 기간이 만료 되 면 비활성 사서함을 복구 하기 위한 절차를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-213">After the soft-deleted mailbox retention period expires, you have follow the procedures for recovering an inactive mailbox.</span></span> <span data-ttu-id="cda46-214">자세한 내용은 [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cda46-214">For details, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="cda46-215">**보류를 제거한 후 비활성 사서함에 대 한 정보를 표시 하는 방법은 무엇 인가요?**</span><span class="sxs-lookup"><span data-stu-id="cda46-215">**How do you display information about an inactive mailbox after the hold is removed?**</span></span> <span data-ttu-id="cda46-216">보류를 제거 하 고 비활성 사서함이 일시 삭제 된 사서함으로 다시 되돌아간 후에는 **사서함** cmdlet과 함께 *Inactivemailboxonly* 매개 변수를 사용 하 여 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-216">After a hold is removed and the inactive mailbox is reverted back to a soft-deleted mailbox, it won't be returned by using the  *InactiveMailboxOnly*  parameter with the **Get-Mailbox** cmdlet.</span></span> <span data-ttu-id="cda46-217">그러나 **undo-softdeletedmailbox** 명령을 사용 하 여 사서함에 대 한 정보를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-217">But you can display information about the mailbox by using the **Get-Mailbox -SoftDeletedMailbox** command.</span></span> <span data-ttu-id="cda46-218">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-218">For example:</span></span> 
    
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
  
<span data-ttu-id="cda46-219">위의 예제에서, 다음 예제 \*\* 에서는 일시 삭제 된 날짜를 식별 하며이 예에서는 10 월 30 일을 2014 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-219">In the above example, the *WhenSoftDeleted* property identifies the soft-deleted date, which in this example is October 30, 2014.</span></span> <span data-ttu-id="cda46-220">이 일시 삭제 된 사서함이 보존을 제거한 이전에 비활성화 된 사서함 인 경우에는 소송 *소프트 deleted* 속성 값 다음에 30 일이 영구적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-220">If this soft-deleted mailbox was previously an inactive mailbox for which the hold was removed, it will be permanently deleted 30 days after the value of the *WhenSoftDeleted* property.</span></span> <span data-ttu-id="cda46-221">이 경우 사서함은 11 월 30 2014 일 이후에 영구적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cda46-221">In this case, the mailbox is permanently deleted after November 30, 2014.</span></span>

