---
title: Office 365 조직 내의 사서함에에서는 보관 및 삭제 정책 설정
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/9/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
ms.assetid: ec3587e4-7b4a-40fb-8fb8-8aa05aeae2ce
description: 사용자의 보관 사서함에 항목을 자동으로 이동 하는 Office 365의 보관 및 삭제 정책을 만듭니다.
ms.openlocfilehash: 740164ee840a32aff20f5c2dc1b1ae433d95cfe5
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522299"
---
# <a name="set-up-an-archive-and-deletion-policy-for-mailboxes-in-your-office-365-organization"></a><span data-ttu-id="062ef-103">Office 365 조직 내의 사서함에에서는 보관 및 삭제 정책 설정</span><span class="sxs-lookup"><span data-stu-id="062ef-103">Set up an archive and deletion policy for mailboxes in your Office 365 organization</span></span>

 <span data-ttu-id="062ef-104">**이 문서는 관리자입니다. 보관 함 및 보존 정책 사서함의 항목에 추가 하 시겠습니까? [전자 메일 메시지에 보존 정책을 할당](https://support.office.com/article/3e5fd2dc-633f-4a38-b313-b31b81f7cf7a)참조 | [비즈니스에 대 한 웹에는 Outlook의 보존 및 보관 정책](https://support.office.com/article/465372e4-e16b-47db-bee0-aba44799085e)**</span><span class="sxs-lookup"><span data-stu-id="062ef-104">**This article is for administrators. Want to add archive and retention policies to items in your mailbox? See [Assign retention policy to email messages](https://support.office.com/article/3e5fd2dc-633f-4a38-b313-b31b81f7cf7a) | [Retention and archive policies in Outlook on the web for business](https://support.office.com/article/465372e4-e16b-47db-bee0-aba44799085e)**</span></span>
  
<span data-ttu-id="062ef-p101">Office 365에서 사용자의 보관 사서함에 항목을 자동으로 이동 하 고 사서함에서 항목을 자동으로 삭제 하는 보관 및 삭제 정책을 만들 수 있습니다. 보존 정책을 만들어이 작업을 수행 수 ' s 삭제 한 후 특정 기간 동안 하 고 있는 항목 사서함에서 특정 시간 제한에 도달한 후 사서함 및 사용자의 보관 사서함으로 이동 항목에 할당 합니다. 항목을 결정 하는 실제 규칙은 이동 되거나 삭제 하 고 사용자가 발생 하는 호출된 보존 태그입니다. 보존 태그는 사용자의 사서함에 할당 된 보존 정책에 연결 됩니다. 보존 태그에는 개별 메시지와 사용자의 사서함 폴더에 보존 설정을 적용 됩니다. 사서함에 그대로 남아 얼마나 오래 된 메시지 및 수행 하는 작업 메시지가 도착 하면 모바일 클라이언트가 지정 된 보존 기간을 정의 합니다. 메시지의 보존 기간에 도달 하면 사용자의 보관 사서함으로 이동 하거나 또는 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p101">In Office 365, you can create an archiving and deletion policy that automatically moves items to a user's archive mailbox and automatically deletes items from the mailbox. You can do this by creating a retention policy that' s assigned to mailboxes, and moves items to a user's archive mailbox after a certain period of time and that also deletes items from the mailbox after they reach a certain age limit. The actual rules that determine what items are moved or deleted and when that happens are called retention tags. Retention tags are linked to a retention policy, that in turn is assigned to a user's mailbox. A retention tag applies retention settings to individual messages and folders in a user's mailbox. It defines how long a message remains in the mailbox and what action is taken when the message reaches the specified retention age. When a message reaches its retention age, it's either moved to the user's archive mailbox or it's deleted.</span></span> 
  
<span data-ttu-id="062ef-p102">이 항목의 단계는 알프스로 하우스 라는 가상의 조직에 대 한 보관 및 보존 정책을 설정 합니다. 이 정책을 설정 하는 다음 작업이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p102">The steps in this topic will set up an archiving and retention policy for a fictitious organization named Alpine House. Setting up this policy includes the following tasks:</span></span>
  
- <span data-ttu-id="062ef-p103">조직에서 모든 사용자에 대 한 보관 사서함을 사용 하도록 설정 합니다. 이 사용자에 게 추가 사서함 저장소를 제공 하며 보존 정책을 보관 사서함에 항목을 이동할 수 있도록 필요 합니다. 것도 보겠습니다 이동 하 여 사용자 저장소 보관 정보 항목의 보관 사서함으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p103">Enabling an archive mailbox for every user in the organization. This gives users addition mailbox storage, and is required so that a retention policy can move items to the archive mailbox. It also let's a user store archival information by moving items to their archive mailbox.</span></span> 
    
- <span data-ttu-id="062ef-117">다음을 수행 하는 세가지 사용자 지정 보존 태그 만들기:</span><span class="sxs-lookup"><span data-stu-id="062ef-117">Creating three custom retention tags that do the following:</span></span> 
    
  - <span data-ttu-id="062ef-p104">사용자의 보관 사서함으로 이전 3 년에 속하는 항목에 자동으로 이동 합니다. 사용자의 기본 사서함에서 공간을 확보 항목 보관 사서함으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p104">Automatically moves items that are 3 years old to the user's archive mailbox. Moving items to the archive mailbox frees up space in a user's primary mailbox.</span></span>
    
  - <span data-ttu-id="062ef-p105">지운 편지함 폴더에서 이전에 5 년 동안 수 있는 항목을 자동으로 삭제 합니다. 또한 사용자의 기본 사서함에서 공간을 해제합니다. 사용자의 필요한 경우 이러한 항목을 복구 하려면 기회를 갖게 됩니다. 자세한 내용은 대 한 [자세한 정보](set-up-an-archive-and-deletion-policy-for-mailboxes.md#moreinfo) 섹션에서 각주를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="062ef-p105">Automatically deletes items that are 5 years old from the Deleted Items folder. This also frees up space in the user's primary mailbox. User's will have the opportunity to recover these items if necessary. See the footnote in the [More information](set-up-an-archive-and-deletion-policy-for-mailboxes.md#moreinfo) section for more details.</span></span> 
    
  - <span data-ttu-id="062ef-p106">자동으로 (및 영구적으로)를 모두 주 이전 7 년 및 보관 사서함 수 있는 항목을 삭제 합니다. 규정 준수로 인해 일부 조직의 특정 기간 동안에 대 한 전자 메일을 유지 해야 합니다. 이 시간 간격에는 다음이 만료 되 면 조직 이러한 항목 사용자 사서함을 영구적으로 제거 하고자 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p106">Automatically (and permanently) deletes items that are 7 years old from both the primary and archive mailbox. Because of compliance regulations, some organization's are required to retain email for a certain period of time. After this time period expires, an organization might want to permanently remove these items user mailboxes.</span></span> 
    
- <span data-ttu-id="062ef-p107">새 보존 정책 만들기 (영문) 하 고 새 사용자 지정 보존 태그를 추가 합니다. 또한 새 보존 정책에도 기본 제공 보존 태그를 추가할 수 있습니다. 이 사용자가 자신의 사서함에 있는 항목에 할당할 수 있는 개인 태그를 포함 합니다. 보관 사서함의 복구 가능한 항목 폴더에는 사용자의 기본 사서함의 복구 가능한 항목 폴더에서 항목을 이동 하는 보존 태그를 추가할 수도 있습니다. 이 사용이 하면 사서함은 대기 상태에 있을 때 사용자의 복구 가능한 항목 폴더에 있는 공간을 비웁니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p107">Creating a new retention policy and adding the new custom retention tags to it. Additionally, you'll also add built-in retention tags to the new retention policy. This includes personal tags that users can assign to items in their mailbox. You'll also add a retention tag that moves items from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in their archive mailbox. This helps free up space in a user's Recoverable Items folder when their mailbox is placed on hold.</span></span>
    
<span data-ttu-id="062ef-p108">조직에서 사서함에 대 한는 보관 및 삭제 정책을 설정 하려면이 문서의 단계 중 일부 또는 전부를 따를 수 있습니다. 조직에서 모든 사서함에 구현 하기 전에 몇가지 사서함에 대해이 프로세스를 테스트 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p108">You can follow some or all of the steps in this article to set up an archive and deletion policy for mailboxes in your own organization. We recommend that you test this process on a few mailboxes before implementing it on all mailboxes in your organization.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="062ef-134">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="062ef-134">Before you begin</span></span>

- <span data-ttu-id="062ef-135">이 항목의 단계를 수행 하려면 Office 365 조직에서 전역 관리자 여야 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-135">You have to be a global administrator in your Office 365 organization to perform the steps in this topic.</span></span> 
    
-  <span data-ttu-id="062ef-p109">Office 365에서 새 사용자 계정 만들기 하 고 사용자는 Exchange Online 라이선스를 할당 하는 경우 사용자에 대 한 사서함 자동으로 만들어집니다. 사서함을 만들 때 기본 MRM 정책 이라는 기본 보존 정책, 할당 된 자동으로 했습니다. 이 문서에서는 있습니다 됩니다 새 보존 정책을 만들고 할당 사용자 사서함에 기본 MRM 정책을 교체 합니다. 사서함에 한번에 할당 하는 보존 정책을 하나만 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p109">When you create a new user account in Office 365 and assign the user an Exchange Online license, a mailbox is automatically created for the user. When the mailbox is created, it's automatically assigned a default retention policy, named Default MRM Policy. In this article, you will create a new retention policy and then assign it to user mailboxes, replacing the Default MRM policy. A mailbox can have only one retention policy assigned to it at any one time.</span></span>
    
- <span data-ttu-id="062ef-140">자세한 내용은 보존 태그 및 보존 정책에 대 한 Exchange Online, [보존 태그 및 보존 정책을](https://go.microsoft.com/fwlink/p/?LinkId=404424)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="062ef-140">To learn more about retention tags and retention policies in Exchange Online, see [Retention tags and retention policies](https://go.microsoft.com/fwlink/p/?LinkId=404424).</span></span>
    
## <a name="step-1-enable-archive-mailboxes-for-users"></a><span data-ttu-id="062ef-141">사용자에 대 한 1 단계: 사용 보관 사서함</span><span class="sxs-lookup"><span data-stu-id="062ef-141">Step 1: Enable archive mailboxes for users</span></span>

<span data-ttu-id="062ef-p110">조직에서 각 사용자에 대 한 보관 사서함을 사용 하도록 설정 하는 첫번째 단계는 합니다. 사용자의 보관 사서함에 보존 기간 만료 된 후 "보관 함으로 이동" 보존 작업을 사용 하면 보존 태그 항목을 이동할 수 있도록 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p110">The first step is to enable the archive mailbox for each user in your organization. A user's archive mailbox has to be enabled so that a retention tag with a "Move to Archive" retention action can move the item after the retention age expires.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="062ef-p111">하기만 하는 프로세스를 완료 하기 전에 일부 지점에서 사용 중인이 프로세스 동안 언제 든 지 보관 사서함을 사용할 수 있습니다. 보관 사서함 설정 되지 않은 경우 보관 정책이 할당 된 모든 항목에 대해 아무 작업도 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p111">You can enable archive mailboxes any time during this process, just as long as they're enabled at some point before you complete the process. If an archive mailbox isn't enabled, no action is taken on any items that have an archive policy assigned to it.</span></span> 
  
1. <span data-ttu-id="062ef-146">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="062ef-147">전역 관리자 계정을 사용 하 여 Office 365에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-147">Sign in to Office 365 using your global administrator account.</span></span>
    
    
3. <span data-ttu-id="062ef-148">보안에서 &amp; 준수 센터, **데이터 관리 방식** 으로 이동 하십시오 \> **보관**합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-148">In the Security &amp; Compliance Center, go to **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="062ef-149">조직에서 사서함의 목록이 표시 되 고 해당 보관 사서함의 사용 여부.</span><span class="sxs-lookup"><span data-stu-id="062ef-149">A list of the mailboxes in your organization is displayed and whether the corresponding archive mailbox is enabled or disabled.</span></span> 
    
4. <span data-ttu-id="062ef-150">**Shift** 키를 누른 상태로 목록에서 첫번째 계정을 클릭 하 고 목록에서 마지막 하나를 클릭 하 여 모든 사서함을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-150">Select all the mailboxes by clicking on the first one in the list, holding down the **Shift** key, and then clicking the last one in the list.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="062ef-p112">이 단계에서는 보관 사서함이 없는 사용할 수 있는지를 가정 합니다. 보관 사용 하도록 설정 된 모든 사서함을 가진 **Ctrl** 키를 누른 비활성화 된 보관 사서함을 보유 한 각 사서함을 클릭 합니다. 또는 기반으로 보관 사서함이 사용 여부를 쉽게 사서함을 선택 하는 행을 정렬 하려면 열 머리글을 **보관 사서함** 을 클릭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p112">This step assumes that no archive mailboxes are enabled. If you have any mailboxes with the archive enabled, hold down the **Ctrl** key and click each mailbox that has a disabled archive mailbox. Or you can click the **Archive mailbox** column header to sort the rows based on whether the archive mailbox is enabled or disabled to make it easier to select mailboxes.</span></span> 
  
5. <span data-ttu-id="062ef-154">세부 정보 창의 **대량 편집**아래에서 **사용**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-154">In the details pane, under **Bulk Edit**, click **Enable**.</span></span>
    
    <span data-ttu-id="062ef-p113">2 년 보다 오래 된 항목을 새 보관 사서함으로 이동할 수 없다는 경고를 표시 합니다. 만들어질 때 새 사용자 사서함에 할당 하는 기본 보존 정책에는 2 년의 보존 기간에는 보관 기본 정책 태그 때문입니다. 2 단계에서에서 만들 수 있는 사용자 지정 보관 기본 정책 태그 3 년의 보존 기간을 있습니다. 즉, 3 년에 속하는 항목에 또는 오래 된 보관 사서함으로 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p113">A warning is displayed saying that items that are older than two years will be moved to the new archive mailbox. This is because the default retention policy that's assigned a new user mailbox when it's created has an archive default policy tag that has a retention age of 2 years. The custom archive default policy tag that you'll create in Step 2 has a retention age of 3 years. That means items that are 3 years or older will be moved to the archive mailbox.</span></span>
    
6. <span data-ttu-id="062ef-159">**예** 를 눌러 경고 메시지를 닫고 각 선택 된 사서함에 대 한 보관 사서함을 사용 하도록 설정 하는 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-159">Click **Yes** to close the warning message and start the process to enable the archive mailbox for each selected mailbox.</span></span> 
    
7. <span data-ttu-id="062ef-160">프로세스가 완료 되 면 **새로고침** 을 클릭 ![새로 고칠](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) **보관** 되는 용지의 목록을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-160">When the process is complete, click **Refresh** ![refresh](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) to update the list on the **Archive** page.</span></span> 
    
    <span data-ttu-id="062ef-161">보관 사서함에 모든 사용자의 조직에 대해 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-161">The archive mailbox is enabled for all user's in your organization.</span></span>
    
    ![사용 하도록 설정 하는 보관 사서함과 사서함 목록](media/61a7cb97-1bed-4808-aa5f-b6b761cfa8de.png)
  
8. <span data-ttu-id="062ef-p114">보안을 유지 &amp; 준수 센터 엽니다. 다음 단계에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p114">Leave the Security &amp; Compliance Center open. You'll use it in the next step.</span></span>
    
## <a name="step-2-create-new-retention-tags-for-the-archive-and-deletion-policies"></a><span data-ttu-id="062ef-165">2 단계: 보관 및 삭제 정책에 대 한 새 보존 태그 만들기</span><span class="sxs-lookup"><span data-stu-id="062ef-165">Step 2: Create new retention tags for the archive and deletion policies</span></span>

<span data-ttu-id="062ef-166">이 단계에서 이전에 설명 된 세 사용자 지정 보존 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-166">In this step, you'll create the three custom retention tags that were previously described.</span></span>
  
- <span data-ttu-id="062ef-167">알프스로 하우스 3 년 보관 함으로 이동 (사용자 지정 보관 정책)</span><span class="sxs-lookup"><span data-stu-id="062ef-167">Alpine House 3 Year Move to Archive (custom archive policy)</span></span>
    
- <span data-ttu-id="062ef-168">알프스로 하우스 7 년 영구적으로 삭제 (사용자 지정 삭제 정책)</span><span class="sxs-lookup"><span data-stu-id="062ef-168">Alpine House 7 Year Permanently Delete (custom deletion policy)</span></span>
    
- <span data-ttu-id="062ef-169">알프스로 하우스 삭제 된 항목 5 년 삭제 및 복구 허용 (지운 편지함 폴더에 대 한 사용자 지정 태그)</span><span class="sxs-lookup"><span data-stu-id="062ef-169">Alpine House Deleted Items 5 Years Delete and Allow Recovery (custom tag for the Deleted Items folder)</span></span>
    
<span data-ttu-id="062ef-170">새 보존 태그를 만들려면 Exchange Online 조직에서 Exchange 관리 센터 (EAC)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-170">To create new retention tags, you'll use the Exchange admin center (EAC) in your Exchange Online organization.</span></span>
  
1. <span data-ttu-id="062ef-171">보안에서 &amp; 준수 센터 왼쪽된 위 모서리에서 응용 프로그램 시작 관리자를 클릭 한 다음 **관리** 타일을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-171">In the Security &amp; Compliance Center, click the app launcher  in the upper left corner, and then click the **Admin** tile .</span></span> 
    
2. <span data-ttu-id="062ef-172">Office 365 관리 센터의 왼쪽된 탐색 창의 **관리 센터**를 클릭 한 다음 **Exchange**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-172">In the left navigation pane of the Office 365 admin center, click **Admin centers**, and then click **Exchange**.</span></span>
    
    ![스크린샷 옵션을 확장 하 고 선택 하는 Exchange 관리자와 Office 365 관리 센터 가운데에 표시 합니다.](media/47399df2-0bc4-42e2-b183-07750a46bc68.png)
  
3. <span data-ttu-id="062ef-174">EAC에서 **규정 준수 관리** 로 이동 \> **보존 태그**</span><span class="sxs-lookup"><span data-stu-id="062ef-174">In the EAC, go to **Compliance management** \> **Retention tags**</span></span>
    
    <span data-ttu-id="062ef-175">조직에 대 한 보존 태그의 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-175">A list of the retention tags for your organization is displayed.</span></span>
    
### <a name="create-a-custom-archive-default-policy-tag"></a><span data-ttu-id="062ef-176">사용자 지정 보관 기본 정책 태그 만들기</span><span class="sxs-lookup"><span data-stu-id="062ef-176">Create a custom archive default policy tag</span></span>
  
<span data-ttu-id="062ef-177">첫째, 사용자 지정 보관 기본 정책 태그 (DPT) 3 년 후 보관 사서함에 항목을 이동 합니다를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-177">First, you'll create a custom archive default policy tag (DPT) that will move items to the archive mailbox after 3 years.</span></span> 
  
1. <span data-ttu-id="062ef-178">**보존 태그** 페이지에서 **새 태그**를 클릭![새 아이콘](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), **전체 사서함 (기본값)에 자동으로 적용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-178">On the **Retention tags** page, click **New tag**![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), and then select **applied automatically to entire mailbox (default)**.</span></span> 
    
2. <span data-ttu-id="062ef-179">**전체 사서함 (기본값)에 자동으로 적용 하는 새 태그** 페이지에서 다음 필드에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-179">On the **New tag applied automatically to entire mailbox (default)** page, complete the following fields:</span></span> 
    
    ![새 보관 기본 정책 태그를 만들 설정](media/41c0a43c-9c72-44e0-8947-da0831896432.png)
  
1. <span data-ttu-id="062ef-181">**이름** 새 보존 태그에 대 한 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-181">**Name** Type a name for the new retention tag.</span></span> 
    
2. <span data-ttu-id="062ef-182">**보존 작업** **보관 사서함으로 이동** 보존 기간이 만료 되는 보관 사서함에 항목을 이동 하려면 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-182">**Retention action** Select **Move to Archive** to move items to the archive mailbox when the retention period expires.</span></span> 
    
3. <span data-ttu-id="062ef-p115">**보존 기간** **항목에는 다음 기간 (일)에 도달 하면**을 선택 하 고 보존 기간이 기간을 입력 합니다. 이 시나리오에 대 한 일 (3 년) 후 항목이 보관 사서함으로 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p115">**Retention period** Select **When the item reaches the following age (in days)**, and then enter the duration of the retention period. For this scenario, items will be moved to the archive mailbox after 1095 days (3 years).</span></span>
    
4. <span data-ttu-id="062ef-185">**메모** (선택 사항) 사용자 지정 보존 태그의 용도 설명 하는 메모를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-185">**Comment** (Optional) Type a comment that explains the purpose of the custom retention tag.</span></span> 
    
3. <span data-ttu-id="062ef-186">사용자 지정 보관 DPT를 만들려면 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-186">Click **Save** to create the custom archive DPT.</span></span> 
    
    <span data-ttu-id="062ef-187">새 보관 DPT 보존 태그의 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-187">The new archive DPT is displayed in the list of retention tags.</span></span>
    
### <a name="create-a-custom-deletion-default-policy-tag"></a><span data-ttu-id="062ef-188">사용자 지정 삭제 기본 정책 태그 만들기</span><span class="sxs-lookup"><span data-stu-id="062ef-188">Create a custom deletion default policy tag</span></span>
  
<span data-ttu-id="062ef-189">다음으로, 다른 사용자 지정 DPT 만들게 하지만이 7 년 후 항목이 영구적으로 삭제 하는 삭제 정책이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-189">Next, you'll create another custom DPT but this one will be a deletion policy that permanently deletes items after 7 years.</span></span>
  
1. <span data-ttu-id="062ef-190">**보존 태그** 페이지에서 **새 태그**를 클릭![새 아이콘](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), **전체 사서함 (기본값)에 자동으로 적용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-190">On the **Retention tags** page, click **New tag**![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), and then select **applied automatically to entire mailbox (default)**.</span></span> 
    
2. <span data-ttu-id="062ef-191">**전체 사서함 (기본값)에 자동으로 적용 하는 새 태그** 페이지에서 다음 필드에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-191">On the **New tag applied automatically to entire mailbox (default)** page, complete the following fields:</span></span> 
    
    ![새 삭제 기본 정책 태그를 만들 설정](media/f1f0ff62-eec9-4824-8e7c-d93dcfb09a79.png)
  
1. <span data-ttu-id="062ef-193">**이름** 새 보존 태그에 대 한 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-193">**Name** Type a name for the new retention tag.</span></span> 
    
2. <span data-ttu-id="062ef-194">**보존 작업** 보존 기간이 만료 되는 사서함에서 항목을 삭제 하려면 **영구적으로 삭제** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-194">**Retention action** Select **Permanently Delete** to purge items from the mailbox when the retention period expires.</span></span> 
    
3. <span data-ttu-id="062ef-p116">**보존 기간** **항목에는 다음 기간 (일)에 도달 하면**을 선택 하 고 보존 기간이 기간을 입력 합니다. 이 시나리오에 대 한 항목을 2555 일 (7 년) 후 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p116">**Retention period** Select **When the item reaches the following age (in days)**, and then enter the duration of the retention period. For this scenario, items will be purged after 2555 days (7 years).</span></span>
    
4. <span data-ttu-id="062ef-197">**메모** (선택 사항) 사용자 지정 보존 태그의 용도 설명 하는 메모를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-197">**Comment** (Optional) Type a comment that explains the purpose of the custom retention tag.</span></span> 
    
3. <span data-ttu-id="062ef-198">사용자 지정 삭제 DPT를 만들려면 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-198">Click **Save** to create the custom deletion DPT.</span></span> 
    
    <span data-ttu-id="062ef-199">새 삭제 DPT 보존 태그의 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-199">The new deletion DPT is displayed in the list of retention tags.</span></span>
    
### <a name="create-a-custom-retention-policy-tag-for-the-deleted-items-folder"></a><span data-ttu-id="062ef-200">지운 편지함 폴더에 대 한 사용자 지정 보존 정책 태그 만들기</span><span class="sxs-lookup"><span data-stu-id="062ef-200">Create a custom retention policy tag for the Deleted Items folder</span></span>
  
<span data-ttu-id="062ef-p117">만들어야 하는 마지막 보존 태그는 지운 편지함 폴더에 대 한 사용자 지정 보존 정책 태그 (RPT). 이 태그 지운 편지함 폴더에서 항목 5 년 후 삭제 하 고 사용자가 항목을 복구 하는 지운 편지함 복구 도구를 사용할 수 때 복구 기간을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p117">The last retention tag that you'll create is a custom retention policy tag (RPT) for the Deleted Items folder. This tag will delete items in the Deleted Items folder after 5 years, and provides a recovery period when users can use the Recover Deleted Items tool to recover an item.</span></span>
  
1. <span data-ttu-id="062ef-203">**보존 태그** 페이지에서 **새 태그** 를 클릭 ![새 아이콘](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), **기본 폴더에 자동으로 적용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-203">On the **Retention tags** page, click **New tag** ![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), and then select **applied automatically to a default folder**.</span></span> 
    
2. <span data-ttu-id="062ef-204">**기본 폴더에 자동으로 적용 하는 새 태그** 페이지에서 다음 필드에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-204">On the **New tag applied automatically to a default folder** page, complete the following fields:</span></span> 
    
    ![지운 편지함 폴더에 대 한 새 보존 정책 태그를 만드는 설정](media/6f3104bd-5edb-48ac-884d-5fe13d81dd1d.png)
  
1. <span data-ttu-id="062ef-206">**이름** 새 보존 태그에 대 한 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-206">**Name** Type a name for the new retention tag.</span></span> 
    
2. <span data-ttu-id="062ef-207">**다음과 같은 기본 폴더에이 태그 적용** 드롭다운 목록에서 **삭제 된 항목**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-207">**Apply this tag to the following default folder** In the drop-down list, select **Deleted Items**.</span></span>
    
3. <span data-ttu-id="062ef-208">**보존 작업** **삭제 및 복구 허용** 보존 기간이 만료 되 면 하지만 사용자가 삭제 된 항목 보존 기간 (이 기본적으로 14 일) 내에서 삭제 된 항목을 복구할 수 있도록 하는 경우 항목을 삭제 하려면 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-208">**Retention action** Select **Delete and Allow Recovery** to delete items when the retention period expires, but allow users to recover a deleted item within the deleted item retention period (which by default is 14 days).</span></span> 
    
4. <span data-ttu-id="062ef-p118">**보존 기간** **항목에는 다음 기간 (일)에 도달 하면**을 선택 하 고 보존 기간이 기간을 입력 합니다. 이 시나리오에 대 한 항목 1825 일 (5 년) 후 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p118">**Retention period** Select **When the item reaches the following age (in days)**, and then enter the duration of the retention period. For this scenario, items will be deleted after 1825 days (5 years).</span></span>
    
5. <span data-ttu-id="062ef-211">**메모** (선택 사항) 사용자 지정 보존 태그의 용도 설명 하는 메모를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-211">**Comment** (Optional) Type a comment that explains the purpose of the custom retention tag.</span></span> 
    
3. <span data-ttu-id="062ef-212">지운 편지함 폴더에 대 한 사용자 지정 RPT를 만들 수 있는 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-212">Click **Save** to create the custom RPT for the Deleted Items folder.</span></span> 
    
    <span data-ttu-id="062ef-213">새 RPT 보존 태그의 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-213">The new RPT is displayed in the list of retention tags.</span></span>

## <a name="step-3-create-a-new-retention-policy"></a><span data-ttu-id="062ef-214">3 단계: 새 보존 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="062ef-214">Step 3: Create a new retention policy</span></span>

<span data-ttu-id="062ef-p119">사용자 지정 보존 태그를 만든 후 다음 단계에서는 새 보존 정책을 만들고 보존 태그를 추가 하는 합니다. 2 단계에서에서 만든 세개의 사용자 지정 보존 태그 및 첫번째 섹션에서 언급 된 기본 제공 태그를 추가 합니다. 4 단계에서에서이 새 보존 정책을 사용자 사서함에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p119">After you create the custom retention tags, the next step is to create a new retention policy and add the retention tags. You'll add the three custom retention tags that you created in Step 2, and the built-in tags that were mentioned in the first section. In Step 4, you'll assign this new retention policy to user mailboxes.</span></span>
  
1. <span data-ttu-id="062ef-218">EAC에서 **규정 준수 관리** 로 이동 \> **보존 정책**입니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-218">In the EAC, go to **Compliance management** \> **Retention policies**.</span></span>
    
2. <span data-ttu-id="062ef-219">**보존 정책** 페이지에서 **새로 만들기** 를 클릭 ![새 아이콘](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif)합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-219">On the **Retention policies** page, click **New** ![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif).</span></span>
    
3. <span data-ttu-id="062ef-220">**이름** 상자에 새 보존 정책;에 대 한 이름을 입력합니다 예: **알프스로 하우스 보관 및 삭제 정책**입니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-220">In the **Name** box, type a name for the new retention policy; for example, **Alpine House Archive and Deletion Policy**.</span></span> 
    
4. <span data-ttu-id="062ef-221">**보존 태그** **추가** 클릭 ![새 아이콘](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif)합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-221">Under **Retention tags**, click **Add** ![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif).</span></span>
    
    <span data-ttu-id="062ef-p120">조직에서 보존 태그의 목록이 표시 됩니다. Note 2 단계에서에서 만든 사용자 지정 태그 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p120">A list of the retention tags in your organization is displayed. Note the custom tags that you created in Step 2 are displayed.</span></span>
    
5. <span data-ttu-id="062ef-p121">다음 스크린샷은 (이러한 태그의 [자세한 정보](set-up-an-archive-and-deletion-policy-for-mailboxes.md#moreinfo) 섹션에서 자세히 설명 된)에서 강조 표시 되는 9 보존 태그를 추가 합니다. 보존 태그를 추가 하려면 선택한 다음 **추가**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p121">Add the 9 retention tags that are highlighted in the following screenshot (these tags are described in more detail in the [More information](set-up-an-archive-and-deletion-policy-for-mailboxes.md#moreinfo) section). To add a retention tag, select it and then click **Add**.</span></span> 
    
    ![새 보존 정책에 보존 태그 추가](media/d8e87176-0716-4238-9e6a-7c4af35541dc.png)
  
    > [!TIP]
    > <span data-ttu-id="062ef-227">**Ctrl** 키를 누른 다음 각 태그를 클릭 하 여 여러 보존 태그를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-227">You can select multiple retention tags by holding down the **Ctrl** key and then clicking each tag.</span></span> 
  
6. <span data-ttu-id="062ef-228">보존 태그를 추가한 후 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-228">After you've added the retention tags, click **OK**.</span></span>
    
7. <span data-ttu-id="062ef-229">**새 보존 정책** 페이지에서 새 정책을 만들려면 다음 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-229">On the **New retention policy** page, click **Save** to create the new policy.</span></span> 
    
    <span data-ttu-id="062ef-p122">새 보존 정책 목록에 표시 됩니다. 세부 정보 창에서 연결 된 보존 태그를 표시 하도록 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p122">The new retention policy is displayed in the list. Select it to display the retention tags linked to it in the details pane.</span></span>
    
    ![새 보존 정책 및 연결 된 보존 태그의 목록](media/63bc45e6-110b-4dc9-a85f-8eb1961a8258.png)
  
## <a name="step-4-assign-the-new-retention-policy-to-user-mailboxes"></a><span data-ttu-id="062ef-233">4 단계: 사용자 사서함에 새 보존 정책 할당</span><span class="sxs-lookup"><span data-stu-id="062ef-233">Step 4: Assign the new retention policy to user mailboxes</span></span>

<span data-ttu-id="062ef-p123">새 사서함을 만들 때 기본적으로 기본 MRM 정책 이라는 보존 정책에 할당 됩니다. 이 단계에서 표시 됩니다 바꾸면이 보존 정책 (하기 때문에 사서함에 할당 된 보존 정책을 하나만 가질 수 있습니다) 만든 3 단계에서에서 사용자 사서함에 조직에서 새 보존 정책을 할당 합니다. 이 단계에서는 조직에서 새 정책의 할당 모든 사서함에 수는 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p123">When a new mailbox is created, a retention policy named Default MRM policy is assigned to it by default. In this step, you'll replace this retention policy (because a mailbox can have only one retention policy assigned to it) by assigning the new retention policy that you created in Step 3 to the user mailboxes in your organization. This step assumes that you'll assign the new policy to all mailboxes in your organization.</span></span>
  
1. <span data-ttu-id="062ef-237">EAC에서 **받는 사람** \> **사서함**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-237">In the EAC, go to **Recipients** \> **Mailboxes**.</span></span>
    
    <span data-ttu-id="062ef-238">조직에서 모든 사용자 사서함의 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-238">A list of all user mailboxes in your organization is displayed.</span></span> 
    
2. <span data-ttu-id="062ef-239">**Shift** 키를 누른 상태로 목록에서 첫번째 계정을 클릭 하 고 목록에서 마지막 하나를 클릭 하 여 모든 사서함을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-239">Select all the mailboxes by clicking on the first one in the list, holding down the **Shift** key, and then clicking the last one in the list.</span></span> 
    
3. <span data-ttu-id="062ef-240">**대량 편집**아래에서 EAC의 오른쪽의 세부 정보 창에서 **기타 옵션**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-240">In the details pane on the right side of the EAC, under **Bulk Edit**, click **More options**.</span></span>
    
4. <span data-ttu-id="062ef-241">**보존 정책**에서 **업데이트**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-241">Under **Retention Policy**, click **Update**.</span></span>
    
5. <span data-ttu-id="062ef-242">**대량 할당 보존 정책** 페이지에서 **보존 정책을 선택** 드롭다운 목록에서 선택 3; 단계에서에서 만든 보존 정책 예: **알프스로 하우스 보관 함 및 보존 정책**입니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-242">On the **Bulk assign retention policy** page, in the **Select the retention policy** drop-down list, select the retention policy that you created in Step 3; for example, **Alpine House Archive and Retention Policy**.</span></span>
    
6. <span data-ttu-id="062ef-243">새 보존 정책 할당을 저장 하려면 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-243">Click **Save** to save the new retention policy assignment.</span></span> 
    
7. <span data-ttu-id="062ef-244">새 보존 정책 사서함에 할당 된 있는지를 확인 하려면 다음을 수행할 수 있습니다: 사서함 페이지에서 사서함을 선택한 다음 편집을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-244">To verify that the new retention policy was assigned to mailboxes, you can do the following: select a mailbox on the Mailboxes page, and then click Edit.</span></span> 
    
1. <span data-ttu-id="062ef-245">**사서함** 페이지에서 사서함을 선택 하 고 **편집** 을 클릭 한 다음 ![편집](media/d7dc7e5f-17a1-4eb9-b42d-487db59e2e21.png)합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-245">Select a mailbox on the **Mailboxes** page, and then click **Edit** ![Edit](media/d7dc7e5f-17a1-4eb9-b42d-487db59e2e21.png).</span></span> 
    
2. <span data-ttu-id="062ef-246">선택한 사용자에 대 한 사서함 속성 페이지에서 **사서함 기능**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-246">On the mailbox properties page for the selected user, click **Mailbox features**.</span></span>
    
    <span data-ttu-id="062ef-247">사서함에 할당 하는 새 정책의 이름은 **보존 정책** 드롭다운 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-247">The name of the new policy assigned to the mailbox is displayed in the **Retention policy** drop-down list.</span></span> 
    

  
## <a name="optional-step-5-run-the-managed-folder-assistant-to-apply-the-new-settings"></a><span data-ttu-id="062ef-248">(선택 사항) 5 단계: 실행 하는 관리 되는 폴더 도우미가 새 설정을 적용 하려면</span><span class="sxs-lookup"><span data-stu-id="062ef-248">(Optional) Step 5: Run the Managed Folder Assistant to apply the new settings</span></span>
<span data-ttu-id="062ef-249"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="062ef-249"></span></span>

<span data-ttu-id="062ef-p124">4 단계에서에서 사서함에 새 보존 정책을 적용 한 후 걸릴 수 최대 7 일 Exchange Online 사서함에 적용할 새 보존 설정에 대 한 합니다. 7 일 마다 관리 되는 폴더 도우미가 프로세스 사서함 라는 프로세스 때문입니다. 관리 되는 폴더 도우미가 실행을 기다리는 대신를 실행 하 여 **Start-managedfolderassistant** cmdlet은 Exchange Online PowerShell 발생 하려면이 옵션을 강제로 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p124">After you apply the new retention policy to mailboxes in Step 4, it can take up to 7 days in Exchange Online for the new retention settings to be applied to the mailboxes. This is because a process called the Managed Folder Assistant processes mailboxes once every 7 days. Instead of waiting for the Managed Folder Assistant to run, you can force this to happen by running the **Start-ManagedFolderAssistant** cmdlet in Exchange Online PowerShell.</span></span> 
  
 <span data-ttu-id="062ef-p125">**관리 되는 폴더 도우미가 실행 하면 어떻게 됩니까?** 사서함의 항목을 검사 하 고 보존 될 수는 있는지 여부를 결정 하 여 보존 정책 설정이 적용 됩니다. 그런 다음 적절 한 보존 태그와 함께 항목 보존에 따라 달라 집니다을 스탬프 처리 하 고의 사용 보존 기간이 지난 항목에 지정 된 보존 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p125">**What happens when you run the Managed Folder Assistant?** It applies the settings in the retention policy by inspecting items in the mailbox and determining whether they're subject to retention. It then stamps items subject to retention with the appropriate retention tag, and then takes the specified retention action on items past their retention age.</span></span> 
  
<span data-ttu-id="062ef-256">Exchange Online PowerShell에 연결한 다음 조직의 모든 사서함에서 관리 되는 폴더 도우미를 실행 하는 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-256">Here are the steps to connect to Exchange Online PowerShell, and then run the Managed Folder Assistant on every mailbox in your organization.</span></span>
  
1. <span data-ttu-id="062ef-257">로컬 컴퓨터에서 Windows PowerShell을 열고 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-257">On your local computer, open Windows PowerShell and run the following command.</span></span>
    
    ```
    $UserCredential = Get-Credential
    ```

    <span data-ttu-id="062ef-258">**Windows PowerShell 자격 증명 요청** 대화 상자에서 사용자 이름 및 Office 365 전역 관리자 계정에 대 한 암호를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-258">In the **Windows PowerShell Credential Request** dialog box, type the user name and password for your Office 365 global admin account, and then click **OK**.</span></span>
    
2. <span data-ttu-id="062ef-259">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-259">Run the following command.</span></span>
    
    ```
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
    ```

3. <span data-ttu-id="062ef-260">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-260">Run the following command.</span></span>
    
    ```
    Import-PSSession $Session
    ```

4. <span data-ttu-id="062ef-261">Exchange Online 조직에 연결 하려는 있는지를 확인 하려면 조직에 있는 모든 사서함의 목록을 가져오려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-261">To verify that you're connected to your Exchange Online organization, run the following command to get a list of all the mailboxes in your organization.</span></span>
    
    ```
    Get-Mailbox
    ```

    > [!NOTE]
    > <span data-ttu-id="062ef-262">자세한 내용은 하거나 Exchange Online 조직에 연결할 때 문제가 있으면 [원격 PowerShell을 사용 하는 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?LinkId=517283)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="062ef-262">For more information or if you have problems connecting to your Exchange Online organization, see [Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283).</span></span> 
  
5. <span data-ttu-id="062ef-263">조직에서의 관리 되는 폴더 도우미가 모든 사용자 사서함에 대 한 시작 하려면 다음의 두 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-263">Run the following two commands to start the Managed Folder Assistant for all user mailboxes in your organization.</span></span>
    
    ```
    $Mailboxes = Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"}
    ```

    ```
    $Mailboxes.Identity | Start-ManagedFolderAssistant
    ```

<span data-ttu-id="062ef-p126">그거에요! 알프스로 하우스 조직에는 보관 및 삭제 정책을 설정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p126">That's it! You've set up an archive and deletion policy for the Alpine House organization.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="062ef-266">추가 정보</span><span class="sxs-lookup"><span data-stu-id="062ef-266">More information</span></span>
<span data-ttu-id="062ef-267"><a name="moreinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="062ef-267"></span></span>

- <span data-ttu-id="062ef-p127">보존 기간 계산 방법 사서함 항목의 보존 기간을 배달 날짜 또는 전송 되지 않은 초안 메시지 등의 항목에 대 한 만든 날짜에서 계산 하지만 사용자가 만들어집니다. 관리 되는 폴더 도우미가 사서함의 항목을 처리 하는 경우 시작 날짜와 함께 삭제 및 복구 허용 또는 영구 삭제 보존 작업 보존 태그에 포함 된 모든 항목에 대 한 만료 날짜 스탬프 처리 합니다. 보관 태그가 있는 항목에 move date 스탬프로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-p127">How is retention age calculated? The retention age of mailbox items is calculated from the date of delivery or the date of creation for items such as draft messages that aren't sent but are created by the user. When the Managed Folder Assistant processes items in a mailbox, it stamps a start date and an expiration date for all items that have retention tags with the Delete and Allow Recovery or Permanently Delete retention action. Items that have an archive tag are stamped with a move date.</span></span> 
    
- <span data-ttu-id="062ef-272">다음 표에서이 항목의 단계를 수행 하 여 만든 사용자 지정 보존 정책에 추가 되는 각 보존 태그에 대 한 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-272">The following table provides more information about each retention tag that is added to the custom retention policy that was created by following the steps in this topic.</span></span>
    
    |<span data-ttu-id="062ef-273">**보존 태그**</span><span class="sxs-lookup"><span data-stu-id="062ef-273">**Retention tag**</span></span>|<span data-ttu-id="062ef-274">**이 태그에서 수행 하는 작업**</span><span class="sxs-lookup"><span data-stu-id="062ef-274">**What this tag does**</span></span>|<span data-ttu-id="062ef-275">**기본 제공 또는 사용자 지정?**</span><span class="sxs-lookup"><span data-stu-id="062ef-275">**Built-in or custom?**</span></span>|<span data-ttu-id="062ef-276">**유형**</span><span class="sxs-lookup"><span data-stu-id="062ef-276">**Type**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="062ef-277">3 년 후 보관 함으로 이동 하는 알프스로 하우스</span><span class="sxs-lookup"><span data-stu-id="062ef-277">Alpine House 3 Year Move to Archive</span></span>  <br/> |<span data-ttu-id="062ef-278">1095 일 (3 년) 보관 사서함으로 오래 된 항목을 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-278">Moves items that are 1095 days (3 years) old to the archive mailbox.</span></span>  <br/> |<span data-ttu-id="062ef-279">사용자 정의 (참조 [2 단계: 보관 및 삭제 정책에 대 한 새 보존 태그 만들기](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )</span><span class="sxs-lookup"><span data-stu-id="062ef-279">Custom (See [Step 2: Create new retention tags for the archive and deletion policies](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )</span></span>  <br/> |<span data-ttu-id="062ef-280">기본 정책 태그 (보관); 이 태그는 전체 사서함에 자동으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-280">Default Policy Tag (archive); this tag is automatically applied to the entire mailbox.</span></span>  <br/> |
    |<span data-ttu-id="062ef-281">알프스로 하우스 7 년 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-281">Alpine House 7 Year Permanently Delete</span></span>  <br/> |<span data-ttu-id="062ef-282">지난 7 년 되었을 때 주 사서함 또는 보관 사서함의 항목을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-282">Permanently deletes items in the primary mailbox or the archive mailbox when they are 7 years old.</span></span>  <br/> |<span data-ttu-id="062ef-283">사용자 정의 (참조 [2 단계: 보관 및 삭제 정책에 대 한 새 보존 태그 만들기](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )</span><span class="sxs-lookup"><span data-stu-id="062ef-283">Custom (See [Step 2: Create new retention tags for the archive and deletion policies](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )</span></span>  <br/> |<span data-ttu-id="062ef-284">기본 정책 태그 (삭제); 이 태그는 전체 사서함에 자동으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-284">Default Policy Tag (deletion); this tag is automatically applied to the entire mailbox.</span></span>  <br/> |
    |<span data-ttu-id="062ef-285">알프스로 하우스 항목 5 년 후 삭제를 삭제 하 고 복구를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-285">Alpine House Deleted Items 5 Years Delete and Allow Recovery</span></span>  <br/> |<span data-ttu-id="062ef-p128">5 년 이전에 지운 편지함 폴더에서 항목을 삭제 합니다. 사용자가 삭제 되기 후 14 일을에 대 한 이러한 항목을 복구할 수 있습니다.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="062ef-p128">Deletes items from the Deleted Items folder that are 5 years old. Users can recover these items for up 14 days after they're deleted.<sup>\*</sup></span></span> <br/> |<span data-ttu-id="062ef-288">사용자 정의 (참조 [2 단계: 보관 및 삭제 정책에 대 한 새 보존 태그 만들기](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )</span><span class="sxs-lookup"><span data-stu-id="062ef-288">Custom (See [Step 2: Create new retention tags for the archive and deletion policies](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )</span></span>  <br/> |<span data-ttu-id="062ef-289">보존 정책 태그 (삭제 된 항목); 이 태그는 지운 편지함 폴더의 항목에 자동으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-289">Retention Policy Tag (Deleted Items); this tag is automatically applied to items in the Deleted items folder.</span></span>  <br/> |
    |<span data-ttu-id="062ef-290">복구 가능한 항목 14 일 후 보관 함으로 이동</span><span class="sxs-lookup"><span data-stu-id="062ef-290">Recoverable Items 14 days Move to Archive</span></span>  <br/> |<span data-ttu-id="062ef-291">항목을 복구 가능한 항목 폴더의 보관 사서함에 14 일에 대 한 복구 가능한 항목 폴더에 있었던 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-291">Moves items that have been in the Recoverable Items folder for 14 days to the Recoverable Items folder in the archive mailbox.</span></span>  <br/> |<span data-ttu-id="062ef-292">기본 제공</span><span class="sxs-lookup"><span data-stu-id="062ef-292">Built-in</span></span>  <br/> |<span data-ttu-id="062ef-293">보존 정책 태그 (복구 가능한 항목); 이 태그의 복구 가능한 항목 폴더의 항목에 자동으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-293">Retention Policy Tag (Recoverable Items); this tag is automatically applied to items in the Recoverable Items folder.</span></span>  <br/> |
    |<span data-ttu-id="062ef-294">정크 메일</span><span class="sxs-lookup"><span data-stu-id="062ef-294">Junk Email</span></span>  <br/> |<span data-ttu-id="062ef-p129">30 일에 대 한 정크 메일 폴더에 있었던 항목이 영구적으로 삭제 합니다. 사용자가 삭제 되기 후 14 일을에 대 한 이러한 항목을 복구할 수 있습니다.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="062ef-p129">Permanently deletes items that have been in the Junk Email folder for 30 days. Users can recover these items for up 14 days after they're deleted.<sup>\*</sup></span></span> <br/> |<span data-ttu-id="062ef-297">기본 제공</span><span class="sxs-lookup"><span data-stu-id="062ef-297">Built-in</span></span>  <br/> |<span data-ttu-id="062ef-298">보존 정책 태그 (정크 메일); 이 태그는 정크 메일 폴더의 항목에 자동으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-298">Retention Policy Tag (Junk Email); this tag is automatically applied to items in Junk Email folder.</span></span>  <br/> |
    |<span data-ttu-id="062ef-299">1개월 후 삭제</span><span class="sxs-lookup"><span data-stu-id="062ef-299">1 Month Delete</span></span>  <br/> |<span data-ttu-id="062ef-p130">30 일이 지난 수 있는 항목을 영구적으로 삭제 합니다. 사용자가 삭제 되기 후 14 일을에 대 한 이러한 항목을 복구할 수 있습니다.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="062ef-p130">Permanently deletes items that are 30 days old. Users can recover these items for up 14 days after they're deleted.<sup>\*</sup></span></span> <br/> |<span data-ttu-id="062ef-302">기본 제공</span><span class="sxs-lookup"><span data-stu-id="062ef-302">Built-in</span></span>  <br/> |<span data-ttu-id="062ef-303">개인; 사용자가이 태그를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-303">Personal; this tag can be applied by users.</span></span>  <br/> |
    |<span data-ttu-id="062ef-304">1년 후 삭제</span><span class="sxs-lookup"><span data-stu-id="062ef-304">1 Year Delete</span></span>  <br/> |<span data-ttu-id="062ef-p131">365 일 오래 된 항목을 영구적으로 삭제 합니다. 사용자가 삭제 되기 후 14 일을에 대 한 이러한 항목을 복구할 수 있습니다.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="062ef-p131">Permanently deletes items that are 365 days old. Users can recover these items for up 14 days after they're deleted.<sup>\*</sup></span></span> <br/> |<span data-ttu-id="062ef-307">기본 제공</span><span class="sxs-lookup"><span data-stu-id="062ef-307">Built-in</span></span>  <br/> |<span data-ttu-id="062ef-308">개인; 사용자가이 태그를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-308">Personal; this tag can be applied by users.</span></span>  <br/> |
    |<span data-ttu-id="062ef-309">삭제 안 함</span><span class="sxs-lookup"><span data-stu-id="062ef-309">Never Delete</span></span>  <br/> |<span data-ttu-id="062ef-310">이 태그는 보존 정책에 의해 삭제 되 고에서 항목을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-310">This tag prevent items from being deleted by a retention policy.</span></span>  <br/> |<span data-ttu-id="062ef-311">기본 제공</span><span class="sxs-lookup"><span data-stu-id="062ef-311">Built-in</span></span>  <br/> |<span data-ttu-id="062ef-312">개인; 사용자가이 태그를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-312">Personal; this tag can be applied by users.</span></span>  <br/> |
    |<span data-ttu-id="062ef-313">개인 1년 후 보관함으로 이동</span><span class="sxs-lookup"><span data-stu-id="062ef-313">Personal 1 year move to archive</span></span>  <br/> |<span data-ttu-id="062ef-314">항목을 1 년 후 보관 사서함으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-314">Moves items to the archive mailbox after 1 year.</span></span>  <br/> |<span data-ttu-id="062ef-315">기본 제공</span><span class="sxs-lookup"><span data-stu-id="062ef-315">Built-in</span></span>  <br/> |<span data-ttu-id="062ef-316">개인; 사용자가이 태그를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="062ef-316">Personal; this tag can be applied by users.</span></span>  <br/> |
   
    > <span data-ttu-id="062ef-p132"><sup>\*</sup>사용자는 Outlook 및 Outlook Web App에서 지운 편지함 복구 도구를 사용 하 여는 기본적으로 14 일 Exchange 온라인 삭제 된 항목 보존 기간 내에서 삭제 된 항목 복구를 수 있습니다. 관리자는 Windows PowerShell를 사용 하 여 최대 30 일에 삭제 된 항목 보존 기간을 높일 수 있습니다. 자세한 내용은 참조: [삭제 된 Windows 용 Outlook에서에서 항목을 복구](https://support.office.com/article/49e81f3c-c8f4-4426-a0b9-c0fd751d48ce) 하 고 [온라인 Exchange 사서함에 대 한 삭제 된 항목 보존 기간 변경](https://go.microsoft.com/fwlink/p/?LinkId=286940)</span><span class="sxs-lookup"><span data-stu-id="062ef-p132"><sup>\*</sup> Users can use the Recover Deleted Items tool in Outlook and Outlook Web App to recover a deleted item within the deleted item retention period, which by default is 14 days in Exchange Online. An administrator can use Windows PowerShell to increase the deleted item retention period to a maximum of 30 days. For more information, see: [Recover deleted items in Outlook for Windows](https://support.office.com/article/49e81f3c-c8f4-4426-a0b9-c0fd751d48ce) and [Change the deleted item retention period for a mailbox in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940)</span></span>
  
- <span data-ttu-id="062ef-p133">**복구 가능한 항목 14 일 후 보관 함으로 이동** 보존 태그를 사용 하면 사용 가능한를 사용 하 여 사용자의 기본 사서함의 복구 가능한 항목 폴더에 저장 공간을 합니다. 이 사용자의 사서함은 영구적으로 사용할 수 있는 수단 삭제 된 사용자의 사서함을 보류에 배치 된 경우에 유용 합니다. 항목에 보관 사서함으로 이동 하지 않고 불가능 한 주 사서함의 복구 가능한 항목 폴더에 대 한 저장소 할당량에 도달 하면 됩니다. 이 고 방지 하는 방법에 대 한 자세한 내용은 [증가에 있는 사서함에 대 한 할당량 대기 복구 가능한 항목을](https://go.microsoft.com/fwlink/p/?LinkId=786479)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="062ef-p133">Using the **Recoverable Items 14 days Move to Archive** retention tag helps free up storage space in the Recoverable Items folder in the user's primary mailbox. This is useful when a user's mailbox is placed on hold, which means nothing is ever permanently deleted the user's mailbox. Without moving items to the archive mailbox, it's possible the storage quota for the Recoverable Items folder in the primary mailbox will be reached. For more information about this and how to avoid it, see [Increase the Recoverable Items quota for mailboxes on hold](https://go.microsoft.com/fwlink/p/?LinkId=786479).</span></span>
