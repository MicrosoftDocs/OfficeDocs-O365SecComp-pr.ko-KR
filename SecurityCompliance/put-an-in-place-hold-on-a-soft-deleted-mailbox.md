---
title: In-place Hold 일시 삭제 된 사서함에 Exchange 온라인 상태로
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
description: 원본 위치 유지 일시 삭제 된 사서함에 대 한 비활성 확인 하 고 해당 내용을 보존을 만드는 방법에 알아봅니다. 그런 다음 비활성 사서함을 검색 하려면 Microsoft eDiscovery 도구를 사용할 수 있습니다.
ms.openlocfilehash: 226929764fe39b99f526301029d4a41e2fa486cc
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027615"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a><span data-ttu-id="33b13-104">In-place Hold 일시 삭제 된 사서함에 Exchange 온라인 상태로</span><span class="sxs-lookup"><span data-stu-id="33b13-104">Put an In-Place Hold on a soft-deleted mailbox in Exchange Online</span></span>

<span data-ttu-id="33b13-p102">원본 위치 유지 일시 삭제 된 사서함에 대 한 비활성 확인 하 고 해당 내용을 보존을 만드는 방법에 알아봅니다. 그런 다음 비활성 사서함을 검색 하려면 Microsoft eDiscovery 도구를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33b13-p102">Learn how to create an In-Place Hold for a soft-deleted mailbox to make it inactive and preserve its contents. Then you can use Microsoft eDiscovery tools to search the inactive mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="33b13-p103">새로 만들기 위한 원본 위치 유지 Exchange Online (Office 365 및 Exchange Online 독립 실행형 계획)에서 2017 년 7 월 1, 마감을 연기 했을 때 했습니다. 하지만 올해 또는 초기 다음 연도 새로 만들기 원본 위치 유지 Exchange 온라인 수 없습니다. 원본 위치 유지를 사용 하는 대신, 또는 사용할 수 있습니다 [eDiscovery 사례](https://go.microsoft.com/fwlink/?linkid=780738) [보존 정책](https://go.microsoft.com/fwlink/?linkid=827811) 에서 Office 365 보안 &amp; 준수 센터입니다. 원본 위치 유지는 새로운 해제, 후에 여전히 기존 전체가 보유 하 고 수정할 수 있습니다 하 고 새로 만들기 전체를 포함 하 고 Exchange Server 2013 및 Exchange 하이브리드 배포는 여전히 지원 됩니다. 및 여전히 소송 보존으로 설정에서 사서함을 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33b13-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds in Exchange Online (in Office 365 and Exchange Online standalone plans). But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. As an alternative to using In-Place Holds, you can use [eDiscovery cases](https://go.microsoft.com/fwlink/?linkid=780738) or [retention policies](https://go.microsoft.com/fwlink/?linkid=827811) in the Office 365 Security &amp; Compliance Center. After we decommission new In-Place Holds, you'll still be able to modify existing In-Place Holds, and creating new In-Place Holds in Exchange Server 2013 and Exchange hybrid deployments will still be supported. And, you'll still be able to place mailboxes on Litigation Hold.</span></span> 
  
<span data-ttu-id="33b13-p104">여기서 사용자 조직, 왼쪽 및가 해당 사용자 계정 및 사서함 삭제 된 상황이 있을 수 있습니다. 나중에, 유지 하는 사서함에 대 한 정보는 실현 합니다. 어떻게 해야 합니까? 삭제 된 사서함 보존 기간이 만료 되지 않았으면 하는 경우 (일시 삭제 된 사서함 라고 함)는 삭제 된 사서함에 In-place Hold를 입력 하 고 비활성 사서함을 만들 수 있습니다. *비활성 사서함* 이 있는 자신이 조직을 떠난 후 이전 직원의 전자 메일을 유지 하기 위해 사용 됩니다. 비활성 이었습니다 때 일시 삭제 된 사서함에 있던 원본 위치 유지 기간이 배치에 대 한 비활성 사서함의 내용은 유지 됩니다. Office 365 보안에서 콘텐츠 검색 Exchange online에서는 원본 위치 eDiscovery를 사용 하 여 사서함을 검색할 수 사서함 비활성 이루어진 후 &amp; 준수 센터 또는 SharePoint Online에서 eDiscovery 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="33b13-p104">You might have a situation where a person has left your organization, and their corresponding user account and mailbox were deleted. Afterwards, you realize there's information in the mailbox that needs to be preserved. What can you do? If the deleted mailbox retention period hasn't expired, you can put an In-Place Hold on the deleted mailbox (called a  soft-deleted mailbox ) and make it an inactive mailbox. An  *inactive mailbox*  is used to preserve a former employee's email after he or she leaves your organization. The contents of an inactive mailbox are preserved for the duration of the In-Place Hold that was is placed on the soft-deleted mailbox when it was made inactive. After the mailbox is made inactive, you can search the mailbox by using In-Place eDiscovery in Exchange Online, Content Search in the Office 365 Security &amp; Compliance Center, or the eDiscovery Center in SharePoint Online.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="33b13-p105">Exchange Online에서 일시 삭제 된 사서함: 특정 보존 기간 내에서 복구할 수 있지만 삭제 된 사서함 Exchange Online에서 일시 삭제 된 사서함 보존 기간 30 일입니다. 즉, 사서함 수 있음을 복구할 (또는 비활성 사서함 내용을) 삭제 되 고 30 일 이내입니다. 30 일 후 일시 삭제 된 사서함은 영구적으로 삭제를 위해 표시 하 고 복구 하거나 수 비활성 합니다.</span><span class="sxs-lookup"><span data-stu-id="33b13-p105">In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period. The soft-deleted mailbox retention period in Exchange Online is 30 days. This means that the mailbox can be recovered (or made an inactive mailbox) within 30 days of being deleted. After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered or made inactive.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="33b13-123">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="33b13-123">Before you begin</span></span>
<span data-ttu-id="33b13-124"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="33b13-124"></span></span>

- <span data-ttu-id="33b13-p106">Windows PowerShell에서 **New-mailboxsearch** cmdlet을 사용 하면 일시 삭제 된 사서함에는 원본 위치 유지를 배치 해야 합니다. Exchange 관리 센터 (EAC) 또는 SharePoint Online에서 eDiscovery 센터를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="33b13-p106">You have to use the **New-MailboxSearch** cmdlet in Windows PowerShell to put an In-Place Hold on a soft-deleted mailbox. You can't use the Exchange admin center (EAC) or the eDiscovery Center in SharePoint Online.</span></span> 
    
- <span data-ttu-id="33b13-127">Windows PowerShell을 사용하여 Exchange Online에 연결하는 방법에 대한 자세한 내용은 [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="33b13-127">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="33b13-128">조직에서 일시 삭제 된 사서함에 대 한 id 정보를 가져오려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="33b13-128">Run the following command to get identity information about the soft-deleted mailboxes in your organization.</span></span> 
    
  ```
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- <span data-ttu-id="33b13-129">비활성 사서함에 대 한 자세한 내용은 [Exchange Online에서 비활성 사서함](http://technet.microsoft.com/library/2f2948c5-1c5a-4643-865c-b36e4ac1414b.aspx)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="33b13-129">For more information about inactive mailboxes, see [Inactive mailboxes in Exchange Online](http://technet.microsoft.com/library/2f2948c5-1c5a-4643-865c-b36e4ac1414b.aspx).</span></span>
    
## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a><span data-ttu-id="33b13-130">비활성 사서함 하도록 일시 삭제 된 사서함에는 원본 위치 유지를 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="33b13-130">Put an In-Place Hold on a soft-deleted mailbox to make it an inactive mailbox</span></span>
<span data-ttu-id="33b13-131"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="33b13-131"></span></span>

<span data-ttu-id="33b13-p107">일시 삭제 된 사서함을 비활성 사서함 만들기 **New-mailboxsearch** cmdlet을 사용 합니다. 자세한 내용은 [New-mailboxsearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="33b13-p107">Use the **New-MailboxSearch** cmdlet to make a soft-deleted mailbox an inactive mailbox. For more information, see [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).</span></span>
  
1. <span data-ttu-id="33b13-134">일시 삭제 된 사서함의 속성을 포함 하는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33b13-134">Create a variable that contains the properties of the soft-deleted mailbox.</span></span> 
    
  ```
  $SoftDeletedMailbox = Get-Mailbox -SoftDeletedMailbox -Identity <identity of soft-deleted mailbox>
  ```

    > [!IMPORTANT]
    > <span data-ttu-id="33b13-p108">이전 명령에서 일시 삭제 된 사서함을 식별할 **DistinguishedName** 또는 **ExchangeGuid** 속성 값을 사용 합니다. 이러한 속성은는 활성 사서함과 일시 삭제 된 사서함 수는 동일한 기본 SMTP 주소 수도 있지만 조직 전체에서 각 사서함에 대 한 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="33b13-p108">In the previous command, use the value of the **DistinguishedName** or **ExchangeGuid** property to identify the soft-deleted mailbox. These properties are unique for each mailbox in your organization, whereas it's possible that an active mailbox and a soft-deleted mailbox might have the same primary SMTP address.</span></span> 
  
2. <span data-ttu-id="33b13-p109">원본 위치 유지를 만들고 일시 삭제 된 사서함에 배치 합니다. 이 예제에서는 대기 기간이 지정 됩니다. 즉, 무기한 보류 비활성 사서함에서 제거 될 때까지 또는 항목에 보관 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33b13-p109">Create an In-Place Hold and place it on the soft-deleted mailbox. In this example, no hold duration is specified. This means items will be held indefinitely or until the hold is removed from the inactive mailbox.</span></span>
    
  ```
  New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true
  
  ```

    <span data-ttu-id="33b13-p110">원본 위치 유지를 만들 때 보류 기간을 지정할 수도 있습니다. 이 예제에서는 약 7 년에 대 한 비활성 사서함에 있는 항목을 보유 합니다.</span><span class="sxs-lookup"><span data-stu-id="33b13-p110">You can also specify a hold duration when you create the In-Place Hold. This example holds items in the inactive mailbox for approximately 7 years.</span></span>
    
  ```
  New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true -ItemHoldPeriod 2777
  ```

3. <span data-ttu-id="33b13-142">잠시 후 일시 삭제 된 사서함 비활성 사서함 인지를 확인 하려면 다음 명령 중 하나를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="33b13-142">After a few moments, run one of the following commands to verify that the soft-deleted mailbox is an inactive mailbox.</span></span>
    
  ```
  Get-Mailbox -InactiveMailboxOnly
  ```

    <span data-ttu-id="33b13-143">또는</span><span class="sxs-lookup"><span data-stu-id="33b13-143">Or</span></span>
    
  ```
  Get-Mailbox -InactiveMailboxOnly -Identity $SoftDeletedMailbox.DistinguishedName  | FL IsInactiveMailbox
  ```

## <a name="more-information"></a><span data-ttu-id="33b13-144">추가 정보</span><span class="sxs-lookup"><span data-stu-id="33b13-144">More information</span></span>
<span data-ttu-id="33b13-145"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="33b13-145"></span></span>

<span data-ttu-id="33b13-p111">비활성 사서함 일시 삭제 된 사서함을 변경한 후 다양 한 방법으로 사서함을 관리할 수 있습니다. 자세한 내용은 다음을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="33b13-p111">After you make a soft-deleted mailbox an inactive mailbox, there are a number of ways you can manage the mailbox. For more information, see:</span></span>
  
- [<span data-ttu-id="33b13-148">Exchange Online에서 비활성 사서함에 대 한 보존 기간 변경</span><span class="sxs-lookup"><span data-stu-id="33b13-148">Change the hold duration for an inactive mailbox in Exchange Online</span></span>](http://technet.microsoft.com/library/96eb634e-af2f-454e-8014-b698396811c4.aspx)
    
- [<span data-ttu-id="33b13-149">Exchange Online에서 비활성 사서함 복구</span><span class="sxs-lookup"><span data-stu-id="33b13-149">Recover an inactive mailbox in Exchange Online</span></span>](http://technet.microsoft.com/library/283838b4-66ba-4c34-b221-e1a3875e1d29.aspx)
    
- [<span data-ttu-id="33b13-150">Exchange Online에서 비활성 사서함 복원</span><span class="sxs-lookup"><span data-stu-id="33b13-150">Restore an inactive mailbox in Exchange Online</span></span>](http://technet.microsoft.com/library/1fb02feb-49e5-4485-aec5-9f1537b772b6.aspx)
    
- [<span data-ttu-id="33b13-151">Exchange Online에서 비활성 사서함에서 보류를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33b13-151">Remove a hold from an inactive mailbox in Exchange Online</span></span>](http://technet.microsoft.com/library/930a98c3-cd81-4aaa-8e22-19714cb2b731.aspx)
    

