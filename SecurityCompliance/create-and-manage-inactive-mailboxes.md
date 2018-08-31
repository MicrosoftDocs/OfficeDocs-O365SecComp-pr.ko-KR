---
title: Office 365에서 비활성 사서함 만들기 및 관리
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 296a02bd-ebde-4022-900e-547acf38ddd7
description: 사서함을 보류 또는 Office 365 보존 정책을 적용 한 후 해당 하는 Office 365 사용자 계정의 삭제 하 여 Office 365에서 비활성 사서함을 만들 수 있습니다. 비활성 사서함의 항목은 비활성 적용 되기 전에에 적용 된 보존 또는 보존 정책의 기간에 대 한 보관 됩니다. 비활성 사서함을 영구적으로 삭제 하려면 방금 보류 또는 보존 정책을 제거 합니다.
ms.openlocfilehash: ed0af9077222d9151dc41010bca10590769118b1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533272"
---
# <a name="create-and-manage-inactive-mailboxes-in-office-365"></a><span data-ttu-id="bcf72-105">Office 365에서 비활성 사서함 만들기 및 관리</span><span class="sxs-lookup"><span data-stu-id="bcf72-105">Create and manage inactive mailboxes in Office 365</span></span>

<span data-ttu-id="bcf72-p102">Office 365를 사용 하면 삭제 된 사서함의 내용을 유지할 수 있습니다. 이 기능을 [비활성 사서함](inactive-mailboxes-in-office-365.md)을 호출 합니다. 비활성 사서함을 사용 하면 조직 남기기 후 이전 직원의 전자 메일을 보존 합니다. 사서함이 소송 보존 또는 Office 365 보존 정책 때 비활성화 (Office 365 보안에서 만든 &amp; 준수 센터) 해당 Office 365 사용자 계정이 삭제 되기 전에 사서함에 적용 됩니다. 비활성 사서함의 내용은 비활성 적용 되기 전에 사서함에 배치 된 보류의 기간에 대 한 보관 됩니다. 이 통해 관리자, 규정 준수 관리자 및 레코드 관리자 보안에서 콘텐츠 검색을 사용 하 여 &amp; 준수 센터 검색 하 고 비활성 사서함의 내용을 내보냅니다. 비활성 사서함 전자 메일을 수신할 수 없음 및 조직의 공유 주소록 또는 다른 목록에 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p102">Office 365 makes it possible for you to retain the contents of deleted mailboxes. This feature is called [inactive mailboxes](inactive-mailboxes-in-office-365.md). Inactive mailboxes allow you to retain former employees' email after they leave your organization. A mailbox becomes inactive when a Litigation Hold or an Office 365 retention policy (created in the Office 365 Security &amp; Compliance Center) is applied to the mailbox before the corresponding Office 365 user account is deleted. The contents of an inactive mailbox are retained for the duration of the hold that was placed on the mailbox before it was made inactive. This allows administrators, compliance officers, and records managers to use Content Search in the Security &amp; Compliance Center to search and export the contents of an inactive mailbox. Inactive mailboxes can't receive email and aren't displayed in your organization's shared address book or other lists.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bcf72-p103">사서함을 비활성화하기 위해 새 원본 위치 유지를 만들 수 있는 2017년 7월 1일 마감 날짜를 연기했습니다. 하지만 올해 말이나 내년 초에는 Exchange Online에 새 원본 위치 유지를 만들 수 없습니다. 그때는 소송 보존과 Office 365 보존 정책만 사용하여 비활성화 사서함을 만들 수 있습니다. 그러나 원본 위치 유지에 있는 기존 비활성화 사서함은 계속 지원되며 비활성화 사서함에서 원본 위치 유지를 계속 관리할 수 있습니다. 관리 항목으로는 원본 위치 유지 기간 변경 및 원본 위치 유지를 삭제하여 비활성화 사서함을 영구 삭제하는 작업이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds to make a mailbox inactive. But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. At that time, only Litigation Holds and Office 365 retention policies can be used to create an inactive mailbox. However, existing inactive mailboxes that are on In-Place Hold will still be supported, and you can continue to manage the In-Place Holds on inactive mailboxes. This includes changing the duration of an In-Place Hold and permanently deleting an inactive mailbox by removing the In-Place Hold.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="bcf72-118">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="bcf72-118">Before you begin</span></span>

- <span data-ttu-id="bcf72-p104">사서함을 비활성화 하려면, 할당 되어야 합니다 Exchange Online 계획 2 라이선스 소송 보존 또는 Office 365 보존 정책을 삭제 하기 전에 사서함에 적용 될 수 있도록 합니다. Exchange Online 계획 2 라이선스를 사용 하면 한 Office 365 엔터프라이즈 E3 및 e 5 구독에 속합니다. 사서함 (즉, 부분에서는 Office 365 Enterprise E1 구독) Exchange Online 계획 1 라이선스를 할당 되 면 보류 삭제 되기 전에 사서함에 적용 될 수 있도록 별도 Exchange Online 보관 라이선스 할당 해야 합니다. 자세한 내용은 [Exchange Online Archiving](https://go.microsoft.com/fwlink/p/?LinkId=286153)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p104">To make a mailbox inactive, it must be assigned an Exchange Online Plan 2 license so that a Litigation Hold or an Office 365 retention policy can be applied to the mailbox before it's deleted. Exchange Online Plan 2 licenses are part of an Office 365 Enterprise E3 and E5 subscriptions. If a mailbox is assigned an Exchange Online Plan 1 license (which is part of an Office 365 Enterprise E1 subscription), you would have to assign it a separate Exchange Online Archiving license so that a hold can be applied to the mailbox before it's deleted. For more information, see [Exchange Online Archiving](https://go.microsoft.com/fwlink/p/?LinkId=286153).</span></span>
    
- <span data-ttu-id="bcf72-p105">해당 하는 Office 365 사용자 계정을 삭제 한 후 삭제 된 Exchange Online 사서함에 연결 된 라이선스를 사용할 수 있습니다. 그런 다음 [비즈니스를 위한 Office 365에서 사용자에 게 라이선스 할당](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc) 다른 사용자에 게 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p105">The license associated with the deleted Exchange Online mailbox will be available after you delete the corresponding Office 365 user account. You can then [Assign licenses to users in Office 365 for business](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc) to another user.</span></span> 
    
- <span data-ttu-id="bcf72-p106">소송 보존 또는 Office 365 보존 정책을 삭제 하기 전에 사서함에 적용 되지 않습니다, 하는 경우 사서함의 내용을 보존 또는 검색할 수 없습니다. 삭제 된 사서함의 삭제, 30 일 이내에 복구할 수 있는 하지만 사서함 및 해당 콘텐츠를 영구적으로 삭제 됩니다 30 일 후 복구 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p106">If a Litigation Hold or an Office 365 retention policy isn't applied to a mailbox before it's deleted, the contents of the mailbox won't be retained or discoverable. However, the deleted mailbox can be recovered within 30 days of deletion, but the mailbox and its contents will be permanently deleted after 30 days if it isn't recovered.</span></span>
    
- <span data-ttu-id="bcf72-p107">소송 보존으로 설정 하는 방법에 대 한 자세한 내용은 [원본 위치 유지 및 소송 보존](https://go.microsoft.com/fwlink/p/?LinkId=846124)을 참조 하십시오. 보안에서 Office 365 보존 정책에 대 한 자세한 내용은 &amp; 준수 센터 [Office 365의 보존 정책 개요](retention-policies.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p107">For more information about Litigation Hold, see [In-Place Hold and Litigation Hold](https://go.microsoft.com/fwlink/p/?LinkId=846124). For more information about Office 365 retention policies in the Security &amp; Compliance Center, see [Overview of retention policies in Office 365](retention-policies.md).</span></span>
  
## <a name="create-an-inactive-mailbox"></a><span data-ttu-id="bcf72-129">비활성 사서함 만들기</span><span class="sxs-lookup"><span data-stu-id="bcf72-129">Create an inactive mailbox</span></span>

<span data-ttu-id="bcf72-p108">사서함을 비활성 만들기는 두 단계로: 1)의 사서함을 배치 소송 보존으로 설정 하거나는 Office 365 보존 정책을 적용 하 고, 2) 사서함을 삭제 하는 중에 또는 해당 Office 365 사용자 계정입니다. 사서함 활성화 되 면 해당 내용은 보류 또는 보존 정책이 제거 될 때까지 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p108">Making a mailbox inactive involves two steps: 1) placing the mailbox on Litigation Hold or applying an Office 365 retention policy to it, and 2) deleting the mailbox or corresponding Office 365 user account. After the mailbox is inactive, its contents are retained until the hold or retention policy is removed.</span></span>
  
### <a name="step-1-place-a-mailbox-on-litigation-hold-or-apply-an-office-365-retention-policy"></a><span data-ttu-id="bcf72-132">1 단계: 소송 보존에 배치 하는 사서함 또는 Office 365 보존 정책 적용</span><span class="sxs-lookup"><span data-stu-id="bcf72-132">Step 1: Place a mailbox on Litigation Hold or apply an Office 365 retention policy</span></span>

<span data-ttu-id="bcf72-p109">사서함을 소송 보존으로 설정 하거나 Office 365 보존 정책 적용 삭제 되기 전에 사서함의 내용을 유지 합니다. 두 유형의 보류 삭제 된 항목 및 수정 된 항목의 원래 버전을 포함 하 여 모든 사서함 콘텐츠를 유지 합니다. 비활성 사서함에 적용 되는 보류 또는 보존 정책을 제거 하 여 비활성 사서함을 영구적으로 삭제 될 때까지 또는 지정된 된 기간에 대 한 항목을 삭제 하 고 수정 된 비활성 사서함에 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p109">Placing a mailbox on Litigation Hold or applying an Office 365 retention policy retains the contents in the mailbox before it's deleted. Both types of holds will retain all mailbox content, including deleted items and original versions of modified items. Deleted and modified items are retained in the inactive mailbox for a specified period, or until you permanently delete the inactive mailbox by removing the hold or retention policy that's applied to the inactive mailbox.</span></span>
  
<span data-ttu-id="bcf72-136">보류 된 사서함에 이미 배치 되어 또는 사서함에는 Office 365 보존 정책을 이미 적용 한 경우 다음 작업을 수행 하기 됩니다 2 단계에서에서 설명한 것 처럼 해당 Office 365 사용자 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-136">If a hold is already placed on a mailbox, or if an Office 365 retention policy is already applied to a mailbox, then all you have to do is delete the corresponding Office 365 user account as explained in Step 2.</span></span>
  
<span data-ttu-id="bcf72-137">사서함을 소송 보존으로 설정 하거나 Office 365 보존 정책 적용에 대 한 단계별 절차를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-137">For step-by-step procedures for placing a mailbox on Litigation Hold or applying an Office 365 retention policy, see:</span></span>
  
- [<span data-ttu-id="bcf72-138">사서함을 소송 자료 보존으로 설정</span><span class="sxs-lookup"><span data-stu-id="bcf72-138">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/?linkid=856286)
    
- [<span data-ttu-id="bcf72-139">Office 365의 보존 정책 개요</span><span class="sxs-lookup"><span data-stu-id="bcf72-139">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
> [!NOTE]
> <span data-ttu-id="bcf72-p110">소송 보존을 포함 하 고 및 Office 365 보존 정책에 대 한 무기한 보류를 만들 수도 있고 대기 시간 기반 키를 누릅니다. 무기한 보존 설정에서 비활성 사서함의 내용을 무한대로 유지 됩니다 또는 보존 기간이 변경 되는 보존이 제거 될 때까지 또는까지 합니다. 보류 또는 보존 정책 (가정 하 고 사서함 30 일 보다 삭제 된)를 제거한 후 비활성 사서함을 영구적으로 삭제에 대 한 표시 됩니다 및 사서함의 내용을 더이상 보존 또는 검색할 수 없습니다. 시간 기반 보존 또는 Office 365 보존 정책에서 보류의 길이 지정합니다. 이 기간 항목 당 별로 이며 사서함 항목을 받은 되었거나 만들어진 날짜부터 계산 됩니다. 보류를 만료 되 면 사서함 항목에 대 한 항목을 나타내는 이동 또는 비활성 사서함의 복구 가능한 항목 폴더에 있는 한 후 해당 항목은 영구적으로 삭제 (비우기) 비활성 사서함에서 삭제 된 항목 보존 기간이 만료 후.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p110">For Litigation Holds and Office 365 retention policies, you can create an indefinite hold or on a time-based hold. In an indefinite hold, the contents of the inactive mailbox will be retained forever, or until the hold is removed or until the hold duration is changed. After the hold or retention policy is removed (assuming that the mailbox was deleted more than 30 days ago), the inactive mailbox will be marked for permanent deletion and the contents of the mailbox will no longer be retained or discoverable. In a time-based hold or Office 365 retention policy, you specify the duration of the hold. This duration is on a per-item basis and is calculated from the date a mailbox item was received or created. After the hold expires for a mailbox item, and that item moved to or is located in the Recoverable Items folder in the inactive mailbox, the item is permanently deleted (purged) from the inactive mailbox after the deleted item retention period expires.</span></span> 
  
### <a name="step-2-delete-the-mailbox"></a><span data-ttu-id="bcf72-146">2단계: 사서함 삭제</span><span class="sxs-lookup"><span data-stu-id="bcf72-146">Step 2: Delete the mailbox</span></span>

<span data-ttu-id="bcf72-p111">사서함은 대기 상태에 놓일을 사용 하거나 후는 Office 365 보존 정책을 적용할 사서함을 삭제 하려면 다음 단계가입니다. 사서함을 삭제 하는 가장 좋은 방법은 Office 365 관리 센터에서 해당 하는 Office 365 사용자 계정을 삭제 하려면 됩니다. Office 365 사용자 계정을 삭제 하는 방법에 대 한 정보를 [조직에서 사용자 삭제](https://support.office.com/article/d5155593-3bac-4d8d-9d8b-f4513a81479e)를 참고 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p111">After the mailbox is placed on hold or an Office 365 retention policy is applied to it, the next step is to delete the mailbox. The best way to delete a mailbox is to delete the corresponding Office 365 user account in the Office 365 admin center. For information about deleting Office 365 user accounts, see [Delete a user from your organization](https://support.office.com/article/d5155593-3bac-4d8d-9d8b-f4513a81479e).</span></span>
  
> [!NOTE]
> <span data-ttu-id="bcf72-p112">Exchange Online PowerShell에서 **Remove-mailbox** cmdlet을 사용 하 여 사서함을 삭제할 수도 있습니다. 자세한 내용은 [Exchange Online 사용자 사서함을 복원 또는 삭제](https://go.microsoft.com/fwlink/?linkid=856287)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p112">You can also delete the mailbox by using the **Remove-Mailbox** cmdlet in Exchange Online PowerShell. For more information, see [Delete or restore user mailboxes in Exchange Online](https://go.microsoft.com/fwlink/?linkid=856287).</span></span> 
  

## <a name="view-a-list-of-inactive-mailboxes"></a><span data-ttu-id="bcf72-152">비활성 사서함의 목록 보기</span><span class="sxs-lookup"><span data-stu-id="bcf72-152">View a list of inactive mailboxes</span></span>


<span data-ttu-id="bcf72-153">조직에서 비활성 사서함 목록을 보려면</span><span class="sxs-lookup"><span data-stu-id="bcf72-153">To view a list of the inactive mailboxes in your organization:</span></span>
  
1. <span data-ttu-id="bcf72-154">이동 [https://protection.office.com/](https://protection.office.com/) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-154">Go to [https://protection.office.com/](https://protection.office.com/) and sign in using the credentials for an administrator account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="bcf72-155">보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 거 버 넌 스** 를 클릭 \> * * 보존 * *.</span><span class="sxs-lookup"><span data-stu-id="bcf72-155">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> ** Retention **.</span></span>
    
3. <span data-ttu-id="bcf72-156">**보존** 페이지에서 **자세히**를 클릭![탐색 모음 타원](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif), **비활성 사서함**을 차례로 클릭 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-156">On the **Retention** page, click **More**![Navigation Bar ellipses](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif), and then click **Inactive mailboxes**.</span></span>
    
    ![보존 페이지에서 자세히를 클릭 하 고 비활성 사서함 목록을 표시 하려면 비활성 사서함을 클릭 한 다음](media/761bd90c-3e37-48f9-b1b9-479e90fea267.png)
  
    <span data-ttu-id="bcf72-p113">**비활성 사서함** 페이지가 표시 됩니다. 참고 하면 조직에서 비활성 사서함의 총 수에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p113">The **Inactive mailboxes** page is displayed. Note the total number of inactive mailboxes in your organization is displayed.</span></span> 
    
    ![조직에서 모든 비활성 사서함의 목록이 표시 됩니다.](media/57d9d183-0c6c-4bd8-82e7-115f7b7b6de7.png)
  
<span data-ttu-id="bcf72-161">또는 실행할 수도 있습니다 다음 명령은 Exchange 온라인 비활성 사서함 목록을 표시 하는 PowerShell 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-161">Alternatively, you can run the following command in Exchange Online PowerShell to display the list of inactive mailboxes.</span></span>

```
 Get-Mailbox -InactiveMailboxOnly | FT DisplayName,PrimarySMTPAddress,WhenSoftDeleted
```

<span data-ttu-id="bcf72-162">클릭 수 ![내보내기 검색 결과 아이콘](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **내보내기** 를 보거나 조직에서 비활성 사서함에 대 한 추가 정보가 포함 된 CSV 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-162">You can click ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Export** to view or download a CSV file that contains additional information about the inactive mailboxes in your organization.</span></span> 
  
<span data-ttu-id="bcf72-p114">비활성 사서함의 목록 및 기타 정보를 CSV 파일로 내보내려면 다음 명령을 실행할 수도 있습니다. 이 예제에서는 현재 디렉터리에 CSV 파일이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p114">You can also run the following command to export the list of inactive mailboxes and other information to a CSV file. In this example, the CSV file is created in the current directory.</span></span>

```
Get-Mailbox -InactiveMailboxOnly | Select Displayname,PrimarySMTPAddress,DistinguishedName,ExchangeGuid,WhenSoftDeleted | Export-Csv InactiveMailboxes.csv -NoType
```
   
> [!NOTE]
> <span data-ttu-id="bcf72-p115">것을 비활성 사서함 활성 사용자 사서함으로 동일한 SMTP 주소를 할 수도 있습니다. 이 경우 비활성 사서함을 고유 하 게 식별 하는 **고유 이름** 또는 **ExchangeGuid** 속성의 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p115">It's possible that an inactive mailbox may have the same SMTP address as an active user mailbox. In this case, the value of the **DistinguishedName** or **ExchangeGuid** property can be used to uniquely identify an inactive mailbox.</span></span> 
  
## <a name="search-and-export-the-contents-of-an-inactive-mailbox"></a><span data-ttu-id="bcf72-167">검색 및 비활성 사서함의 내용을 내보내기</span><span class="sxs-lookup"><span data-stu-id="bcf72-167">Search and export the contents of an inactive mailbox</span></span>

<span data-ttu-id="bcf72-p116">보안에서 콘텐츠 검색 도구를 사용 하 여 비활성 사서함의 내용에 액세스할 수 있습니다 &amp; 준수 센터입니다. 비활성 사서함을 검색 하는 경우에 특정 항목에 대 한 검색 키워드 검색 쿼리를 만들 수 있습니다 또는 비활성 사서함의 전체 콘텐츠를 반환할 수 있습니다. 검색 결과 미리 보고 하거나 Outlook 데이터 (PST) 파일 또는 개별 전자 메일 메시지로 검색 결과 내보낼 수 있습니다. 사서함을 검색 하 고 검색 결과 내보내기 (영문)에 대 한 단계별 절차에 대 한 다음 항목을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p116">You can access the contents of the inactive mailbox by using the Content Search tool in the Security &amp; Compliance Center. When you search an inactive mailbox, you can create a keyword search query to search for specific items or you can return the entire contents of the inactive mailbox. You can preview the search results or export the search results to an Outlook Data (PST) file or as individual email messages. For step-by-step procedures for searching mailboxes and exporting search results, see the following topics:</span></span>
  
- [<span data-ttu-id="bcf72-172">Office 365의에서 콘텐츠 검색</span><span class="sxs-lookup"><span data-stu-id="bcf72-172">Content Search in Office 365</span></span>](content-search.md)
    
- [<span data-ttu-id="bcf72-173">Office 365 보안에서 콘텐츠 검색 결과 내보낼 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="bcf72-173">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
<span data-ttu-id="bcf72-174">다음은 비활성 사서함을 검색할 때 주의 해야할 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-174">Here are a few things to keep in mind when searching inactive mailboxes.</span></span>
  
- <span data-ttu-id="bcf72-175">콘텐츠 검색 사용자 사서함을 포함 하는 경우 해당 사서함 그런 다음 비활성 이루어집니다 비활성 하 게 되 면 검색을 다시 실행 하는 경우 비활성 사서함을 검색 하는 콘텐츠 검색을 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-175">If a content search includes a user mailbox and that mailbox is then made inactive, the content search will continue to search the inactive mailbox when you re-run the search after it becomes inactive.</span></span>
    
- <span data-ttu-id="bcf72-p117">일부 경우에는 사용자는 활성 사서함과 동일한 SMTP 주소를가지고 있는 비활성 사서함 있을 수 있습니다. 이 경우 콘텐츠 검색에 대 한 위치도를 선택 하면 특정 사서함만 검색 됩니다. 즉, 검색 하는 사용자의 사서함을 추가 하는 경우 가정할 수 없습니다는 자신의 활성 및 비활성 사서함 검색 됩니다 되지 않습니다. 검색에 명시적으로 추가 하는 사서함을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p117">In some cases, a user may have an active mailbox and an inactive mailbox that have the same SMTP address. In this case, only the specific mailbox that you select as a location for a content search will be searched. In other words, if you add a user's mailbox to a search, you can't assume that both their active and inactive mailboxes will be searched; only the mailbox that you explicitly add to the search will be searched.</span></span>
    
- <span data-ttu-id="bcf72-p118">활성 사서함과 동일한 SMTP 주소를 사용 하 여 비활성 사서함 필요 하지 못하도록 하는 것이 좋습니다. 비활성 사서함을 복구 하거나 활성 사서함이 있는 (또는 활성 사서함의 보관) 비활성 사서함의 내용을 복원 하는 다음 삭제를 권장 비활성 사서함에 현재 할당 된 SMTP 주소를 다시 사용 해야하는 경우는 비활성 사서함입니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p118">We strongly recommend that you avoid having an active mailbox and inactive mailbox with the same SMTP address. If you need to reuse the SMTP address that is currently assigned to an inactive mailbox, we recommend that you recover the inactive mailbox or restore the contents of an inactive mailbox to an active mailbox (or the archive of an active mailbox), and then delete the inactive mailbox.</span></span>
    
## <a name="change-the-hold-duration-for-an-inactive-mailbox"></a><span data-ttu-id="bcf72-181">비활성 사서함의 유지 보존 기간 변경</span><span class="sxs-lookup"><span data-stu-id="bcf72-181">Change the hold duration for an inactive mailbox</span></span>

<span data-ttu-id="bcf72-p119">사서함 비활성 이루어진 후에 보류 또는 비활성 사서함에 적용 되는 Office 365 보존 정책을의 기간을 변경할 수 있습니다. 단계별 절차에 대 한 [변경을 Office 365에서 비활성 사서함에 대 한 보존 기간을](change-the-hold-duration-for-an-inactive-mailbox.md)참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p119">After a mailbox is made inactive, you can change the duration of the hold or the Office 365 retention policy applied to the inactive mailbox. For step-by-step procedures, see [Change the hold duration for an inactive mailbox in Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).</span></span>
  
## <a name="recover-an-inactive-mailbox"></a><span data-ttu-id="bcf72-184">비활성 사서함 복구</span><span class="sxs-lookup"><span data-stu-id="bcf72-184">Recover an inactive mailbox</span></span>

<span data-ttu-id="bcf72-p120">이전 직원이 조직에 반환 하는 경우 또는 이전된 직원의 직무에 적용할 새 직원 고용 하는 경우 비활성 사서함의 내용을 복구할 수 있습니다. 비활성 사서함을 복구 하는 경우 사서함 새 사서함으로 변환 됩니다 내용과 비활성 사서함의 폴더 구조 유지 되므로 및 사서함을 새 사용자 계정에 연결 됩니다. 복구한 후 비활성 사서함 존재 하지 않습니다. 단계별 절차 및 방법에 대 한 자세한 내용은 비활성 사서함을 복구 하는 경우 수행 되는, [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p120">If a former employee returns to your organization, or if a new employee is hired to take on the job responsibilities of the departed employee, you can recover the contents of the inactive mailbox. When you recover an inactive mailbox, the mailbox is converted to a new mailbox, the contents and folder structure of the inactive mailbox are retained, and the mailbox is linked to a new user account. After it's recovered, the inactive mailbox no longer exists. For step-by-step procedures and more information about happens when you recover an inactive mailbox, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>
  
[<span data-ttu-id="bcf72-189">비활성 사서함 관리</span><span class="sxs-lookup"><span data-stu-id="bcf72-189">Managing inactive mailboxes</span></span>](create-and-manage-inactive-mailboxes.md#manageinactivemailboxes)
  
## <a name="restore-the-contents-of-an-inactive-mailbox-to-another-mailbox"></a><span data-ttu-id="bcf72-190">비활성 사서함의 내용을 다른 사서함 복원</span><span class="sxs-lookup"><span data-stu-id="bcf72-190">Restore the contents of an inactive mailbox to another mailbox</span></span>

<span data-ttu-id="bcf72-p121">이전 직원의 직무에 가져와 다른 직원 또는 다른 사람을 비활성 사서함의 내용에 대 한 액세스를 요구 하는 경우 사용자 수 복원 (또는 병합) 기존 사서함을 비활성 사서함의 내용을 합니다. 비활성 사서함을 복원 하는 경우에 내용은 다른 사서함에 복사 됩니다. 비활성 사서함은 유지 하 고 비활성 사서함을 유지 됩니다. 비활성 사서함 여전히 검색 가능한 eDiscovery를 사용 하 여, 다른 사서함의 내용을 복원할 수 또는 복구 되거나 나중에 삭제 될 수 있습니다. 단계별 절차에 대 한 [Office 365에서 비활성 사서함 복원](restore-an-inactive-mailbox.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p121">If another employee takes on the job responsibilities of a former employee, or if another person needs access to the contents of the inactive mailbox, you can restore (or merge) the contents of the inactive mailbox to an existing mailbox. When you restore an inactive mailbox, the contents are copied to another mailbox. The inactive mailbox is retained and remains an inactive mailbox. The inactive mailbox can still be searched using eDiscovery, its contents can be restored to another mailbox, or it can be recovered or deleted at a later date. For step-by-step procedures, see [Restore an inactive mailbox in Office 365](restore-an-inactive-mailbox.md).</span></span>
  
## <a name="delete-an-inactive-mailbox"></a><span data-ttu-id="bcf72-196">비활성 사서함 삭제</span><span class="sxs-lookup"><span data-stu-id="bcf72-196">Delete an inactive mailbox</span></span>

<span data-ttu-id="bcf72-p122">더이상 비활성 사서함의 내용을 유지 해야하는 경우에 보류를 제거 하거나 비활성 사서함에 적용 되는 Office 365 보존 정책을 제거 하 여 비활성 사서함을 영구적으로 삭제할 수 없습니다. 사서함에서 30 일이 경과, 삭제 된 경우 사서함 보류를 제거 하 고 사서함을 복구할 수 없는 될 후 영구적으로 삭제에 대 한 표시 됩니다. 지난 30 일, 삭제 된 사서함 하는 경우 보류 또는 보존 정책을 제거한 후 사서함을 복구할 수 있습니다. 보류 또는 비활성 사서함을 영구적으로 삭제 하는 Office 365 보존 정책을 제거 하기 위한 단계별 절차에 대 한 [Office 365에서 비활성 사서함 삭제](delete-an-inactive-mailbox.md)를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcf72-p122">If you no longer need to retain the contents of an inactive mailbox, you can permanently delete the inactive mailbox by removing the hold or removing the Office 365 retention policy applied to the inactive mailbox. If the mailbox was deleted more than 30 days ago, the mailbox will be marked for permanent deletion after you remove the hold, and the mailbox will become non-recoverable. If the mailbox was deleted within the last 30 days, you can still recover the mailbox after removing the hold or retention policy. For step-by-step procedures for removing a hold or a Office 365 retention policy to permanently delete an inactive mailbox, see [Delete an inactive mailbox in Office 365](delete-an-inactive-mailbox.md).</span></span>