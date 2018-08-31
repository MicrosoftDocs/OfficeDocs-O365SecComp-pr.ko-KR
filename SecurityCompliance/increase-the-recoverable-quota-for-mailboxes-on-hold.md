---
title: 보류된 사물함의 복구 가능한 항목 할당량 증가
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/22/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a8bdcbdd-9298-462f-b889-df26037a990c
description: '보관 사서함을 사용 하도록 설정 하 고 자동 확장을 Office 365의 사서함에 대 한 복구 가능한 항목 폴더의 크기를 늘리려면 보관 설정 합니다. '
ms.openlocfilehash: 2e7149ef10152a11dc638c04b61a261440b539b8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533023"
---
# <a name="increase-the-recoverable-items-quota-for-mailboxes-on-hold"></a><span data-ttu-id="ce53e-103">보류된 사물함의 복구 가능한 항목 할당량 증가</span><span class="sxs-lookup"><span data-stu-id="ce53e-103">Increase the Recoverable Items quota for mailboxes on hold</span></span>

<span data-ttu-id="ce53e-p101">기본 보존 정책-기본 MRM 정책 이라는-즉 Exchange Online에서 새로 만들기를 자동으로 적용 된 사서함 명명 된 복구 가능한 항목 14 일 후 보관 함으로 이동 보존 태그를 포함 합니다. 팀에서 14 일 보존 기간이 만료 된 항목에 대 한이 보존 태그 항목을 사용자의 기본 사서함의 복구 가능한 항목 폴더에서 사용자의 보관 사서함의 복구 가능한 항목 폴더를 이동 합니다. 발생 하려면이 옵션을 사용자의 보관 사서함 사용 해야 합니다. 보관 사서함 설정 되지 않은 경우 아무 작업도 수행, 즉, 14 일 보존 기간이 만료 후의 복구 가능한 항목 폴더의 사서함에 대해 보류의 항목 보관 사서함으로 이동 되지 않습니다. 없기 때문에 아무것도 대기 사서함에서 삭제 되는 복구 가능한 항목 폴더에 대 한 저장소 할당량을 초과 될 수 있습니다, 사용자의 보관 사서함 설정 되지 않은 경우에 특히 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p101">The default retention policy—named Default MRM Policy—that is automatically applied to new mailboxes in Exchange Online contains a retention tag named Recoverable Items 14 days move to archive. This retention tag moves items from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in the user's archive mailbox after the 14-day retention period expires for an item. For this to happen, the user's archive mailbox must be enabled. If the archive mailbox isn't enabled, no action is taken, which means that items in the Recoverable Items folder for a mailbox on hold aren't moved to the archive mailbox after the 14-day retention period expires. Because nothing is deleted from a mailbox on hold, it's possible that the storage quota for the Recoverable Items folder might be exceeded, especially if the user's archive mailbox isn't enabled.</span></span> 
  
<span data-ttu-id="ce53e-p102">이 제한을 초과 하면 가능성을 줄이려면 복구 가능한 항목 폴더에 대 한 저장소 할당량은 자동으로 늘어났습니다 30GB에서 100GB로 보류에 배치 될 때는 사서함 Exchange Online 합니다. 보관 사서함을 사용 하는 경우의 보관 사서함의 복구 가능한 항목 폴더에 대 한 저장소 할당량도 증가 30GB에서 100GB로 합니다. Exchange 기능 자동 확장 하는 보관 하는 경우에 온라인 상태가, 사용자의 보관에서 복구 가능한 항목 폴더에 대 한 저장소 할당량 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p102">To help reduce the chance of exceeding this limit, the storage quota for the Recoverable Items folder is automatically increased from 30 GB to 100 GB when a hold is placed on a mailbox in Exchange Online. If the archive mailbox is enabled, the storage quota for the Recoverable Items folder in the archive mailbox is also increased from 30 GB to 100 GB. If the auto-expanding archiving feature in Exchange Online is enabled, the storage quota for the Recoverable Items folder in the user's archive will be unlimited.</span></span>
  
 <span data-ttu-id="ce53e-112"> 다음 표는 복구 가능한 항목 폴더의 저장소 할당량을 간략하게 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-112">The following table summarizes the storage quota for the Recoverable Items folder.</span></span> 
  
|<span data-ttu-id="ce53e-113">**복구 가능한 항목 폴더 위치**</span><span class="sxs-lookup"><span data-stu-id="ce53e-113">**Location of Recoverable Items folder**</span></span>|<span data-ttu-id="ce53e-114">**보류되지 않은 사서함**</span><span class="sxs-lookup"><span data-stu-id="ce53e-114">**Mailboxes not on hold**</span></span>|<span data-ttu-id="ce53e-115">**보류된 사서함**</span><span class="sxs-lookup"><span data-stu-id="ce53e-115">**Mailboxes on hold**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce53e-116">기본 사서함</span><span class="sxs-lookup"><span data-stu-id="ce53e-116">Primary mailbox</span></span>  <br/> |<span data-ttu-id="ce53e-117">30GB</span><span class="sxs-lookup"><span data-stu-id="ce53e-117">30 GB</span></span>  <br/> |<span data-ttu-id="ce53e-118">100GB</span><span class="sxs-lookup"><span data-stu-id="ce53e-118">100 GB</span></span>  <br/> |
|<span data-ttu-id="ce53e-119">보관 사서함<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="ce53e-119">Archive mailbox<sup>\*</sup></span></span> <br/> |<span data-ttu-id="ce53e-120">제한 없음</span><span class="sxs-lookup"><span data-stu-id="ce53e-120">Unlimited</span></span>  <br/> |<span data-ttu-id="ce53e-121">제한 없음</span><span class="sxs-lookup"><span data-stu-id="ce53e-121">Unlimited</span></span>  <br/> |
|<span data-ttu-id="ce53e-122">**복구 가능한 항목 폴더 할당량**</span><span class="sxs-lookup"><span data-stu-id="ce53e-122">**Total storage quota for the Recoverable Items folder**</span></span> <br/> |<span data-ttu-id="ce53e-123">제한 없음</span><span class="sxs-lookup"><span data-stu-id="ce53e-123">Unlimited</span></span>  <br/> |<span data-ttu-id="ce53e-124">제한 없음</span><span class="sxs-lookup"><span data-stu-id="ce53e-124">Unlimited</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="ce53e-p103"><sup>\*</sup>보관 사서함에 대 한 초기 저장소 할당량은 Exchange Online (계획 2) 라이선스를 사용 하는 사용자에 대 한 100GB. 하지만, 자동 확장 보관을 설정 하는 경우 사용자의 보관 및 보관 사서함의 복구 가능한 항목 폴더에 대 한 저장소 할당량 제한 되지는 않습니다. 자동 확장 하는 방법에 대 한 자세한 내용은 [Office 365 무제한 보관의 개요](unlimited-archiving.md)를 참조 보관 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p103"><sup>\*</sup> The initial storage quota for the archive mailbox is 100 GB for users with an Exchange Online (Plan 2) license. However, when auto-expanding archiving is turned on, the storage quota for the user's archive and the Recoverable Items folder in the archive is unlimited. For more information about auto-expanding archiving, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
<span data-ttu-id="ce53e-128">보류된 사서함의 기본 사서함에 있는 복구 가능한 항목 폴더의 저장소 할당량이 한도에 도달하려는 경우 다음 항목을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-128">When the storage quota for the Recoverable Items folder in the primary mailbox of a mailbox on hold is close to reaching its limit, you can do the following things:</span></span>
  
- <span data-ttu-id="ce53e-p104">**보관 사서함을 사용 하도록 설정 하 고 자동 확장 보관 설정** -보관 사서함을 사용 하도록 설정 하 고 다음 Exchange에서 자동을 확장 하면 보관 기능을 설정 하 여 복구 가능한 항목 폴더에 대 한 사용 하 여 무제한 저장 용량이 설정할 수 있습니다 온라인. 이 기본 사서함과 사용자의 보관에서 복구할 수 있는 항목 폴더에 대 한 저장 용량에 무제한 금액의 복구 가능한 항목 폴더에 100GB에서 만들어집니다. 참조 방법: [Office 365 보안에서 보관 사서함 사용 &amp; 준수 센터](enable-archive-mailboxes.md) 고 [Office 365에서 무제한 보관을 사용](enable-unlimited-archiving.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p104">**Enable the archive mailbox and turn on auto-expanding archiving** - You can enable an unlimited storage capacity for the Recoverable Items folder simply by enabling the archive mailbox and then turning on the auto-expanding archiving feature in Exchange Online. This results in 100 GB for the Recoverable Items folder in the primary mailbox and an unlimited amount of storage capacity for the Recoverable Items folder in the user's archive. See how: [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="ce53e-p105">수동으로 이동 되도록 만료 된 항목의 사서함을 처리 하는 데 길잡이 트리거하는 관리 되는 폴더 도우미가 실행 해야할 복구 가능한 항목 폴더에 대 한 저장소 할당량을 초과 하면 되는 사서함에 대 한 보관을 활성화 한 후의 보관 사서함의 복구 가능한 항목 폴더입니다. 지침에 대 한 [4 단계를](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) 참조 하십시오. 참고 사용자의 사서함에서 다른 항목은 새 보관 사서함으로 이동할 수 있습니다. 보관 사서함을 사용 하도록 설정한 후 발생할 수 있습니다이 방향을 지시 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p105">After you enable the archive for a mailbox that's close to exceeding the storage quota for the Recoverable Items folder, you might want to run the Managed Folder Assistant to manually trigger the assistant to process the mailbox so that expired items are moved the Recoverable Items folder in the archive mailbox. See [Step 4](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) for instructions. Note that other items in the user's mailbox might be moved to the new archive mailbox. Consider telling the user that this may happen after you enable the archive mailbox.</span></span> 
  
- <span data-ttu-id="ce53e-p106">**보관 사서함에 대 한 사용자 지정 보존 정책 만들기** -보관 사서함을 사용 하도록 설정 하 고 자동 확장 사서함을 원본 위치 유지 또는 소송 보존으로 설정에 대 한 보관 외에 해야할 수에 사서함에 대 한 사용자 지정 보존 정책을 만들합니다 보류 합니다. 이 보겠습니다 정책을 적용 하면 보존 대기 대기 되지 않은 사서함에 적용 되는 기본 MRM 정책와에서는 다른 사서함에 있습니다. 이 보류에 있는 사서함에 대 한 특별히 설계 된 보존 태그를 적용할 수 있습니다. 복구 가능한 항목 폴더에 대 한 새 보존 태그 만들기 (영문) 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p106">**Create a custom retention policy for mailboxes on hold** - In addition to enabling the archive mailbox and auto-expanding archiving for mailboxes on Litigation Hold or In-Place Hold, you might also want to create a custom retention policy for mailboxes on hold. This let's you apply a retention policy to mailboxes on hold that's different from the Default MRM Policy that's applied to mailboxes that aren't on hold. This lets you to apply retention tags that are specifically designed for mailboxes on hold. This includes creating a new retention tag for the Recoverable Items folder.</span></span> 
    
<span data-ttu-id="ce53e-140">이 항목의 나머지 부분에서는 보류된 사서함에 대한 사용자 지정 보존 정책을 만드는 단계별 절차를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-140">The remainder of this topic describes the step-by-step procedures to create a custom retention policy for mailboxes on hold.</span></span>
  
[<span data-ttu-id="ce53e-141">1단계: 복구 가능한 항목 폴더에 대한 사용자 지정 보존 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-141">Step 1: Create a custom retention tag for the Recoverable Items folder</span></span>](#step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder)

<span data-ttu-id="ce53e-142">[[2 단계: 대기 사서함에 대 한 새 보존 정책 만들기](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)</span><span class="sxs-lookup"><span data-stu-id="ce53e-142">[[Step 2: Create a new retention policy for mailboxes on hold](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)</span></span>

[<span data-ttu-id="ce53e-143">3단계: 보류된 사서함에 새로운 보존 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-143">Step 3: Apply the new retention policy to mailboxes on hold</span></span>](#step-3-apply-the-new-retention-policy-to-mailboxes-on-hold)

[<span data-ttu-id="ce53e-144">(옵션)4단계: 관리되는 폴더 도우미를 실행하여 새로운 보존 설정을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-144">(Optional) Step 4: Run the Managed Folder Assistant to apply the new retention settings</span></span>](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings)
  
## <a name="step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder"></a><span data-ttu-id="ce53e-145">1단계: 복구 가능한 항목 폴더에 대한 사용자 지정 보존 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-145">Step 1: Create a custom retention tag for the Recoverable Items folder</span></span>

<span data-ttu-id="ce53e-p107">첫번째 단계는 복구 가능한 항목 폴더에 대 한 사용자 지정 보존 태그 (보존 정책 태그 또는 RPT 라고 함)를 만드는 것입니다. 앞에서 설명한 것 처럼이 RPT 사용자의 기본 사서함의 복구 가능한 항목 폴더에서 항목을 복구할 수 있는 항목 폴더에 사용자의 보관 사서함 이동합니다. 복구 가능한 항목 폴더에 대 한 RPT를 만들 수 PowerShell을 사용 해야 합니다. Exchange 관리 센터 (EAC)를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p107">The first step is to create a custom retention tag (called a retention policy tag or RPT) for the Recoverable Items folder. As previously explained, this RPT moves items from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in the user's archive mailbox. You have to use PowerShell to create an RPT for the Recoverable Items folder. You can't use the Exchange admin center (EAC).</span></span> 
  
1. [<span data-ttu-id="ce53e-150">원격 PowerShell을 사용하여 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="ce53e-150">Connect to Exchange Online using remote PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=517283)
    
2. <span data-ttu-id="ce53e-151">복구할 수 있는 항목 폴더에 대한 새로운 RPT를 만들려면 다음 명령을 실행합니다. </span><span class="sxs-lookup"><span data-stu-id="ce53e-151">Run the following command to create a new RPT for the Recoverable Items folder:</span></span> 
    
    ```
    New-RetentionPolicyTag -Name <Name of RPT> -Type RecoverableItems -AgeLimitForRetention <Number of days> -RetentionAction MoveToArchive
    ```

    <span data-ttu-id="ce53e-p108">예를 들어 다음 명령을 사용하면 보존 기간이 30일인 “보류된 사서함의 30일 복구 가능한 항목”이라는 복구 가능한 항목 폴더에 대한 RPT가 만들어집니다. 이는 어떤 항목이 복구 가능한 항목 폴더에서 30일 동안 있은 후 사용자의 보관 사서함에 있는 복구 가능한 항목 폴더로 이동함을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p108">For example, the following command creates a RPT for the Recoverable Items folder named "Recoverable Items 30 days for mailboxes on hold", with a retention period of 30 days. This means that after an item has been in the Recoverable Items folder for 30 days, it will be moved to the Recoverable Items folder in the user's archive mailbox.</span></span>
    
    ```
    New-RetentionPolicyTag -Name "Recoverable Items 30 days for mailboxes on hold" -Type RecoverableItems -AgeLimitForRetention 30 -RetentionAction MoveToArchive
    ```

    > [!TIP]
    > <span data-ttu-id="ce53e-p109">복구 가능한 항목 RPT에 대 한 보존 기간 ( _AgeLimitForRetention_ 매개 변수에 의해 정의 된) RPT 적용할 수 있는 사서함에 대 한 삭제 된 항목 보존 기간와 동일 하 게 되는 것이 좋습니다. 이렇게 하면 사용자 전체 삭제 된 항목 보존 기간 보관 사서함으로 이동 하기 전에 삭제 된 항목을 복구할 수 있습니다. 이전 예제에서 보존 기간 사서함에 대 한 삭제 된 항목 보존 기간은 30 일 수도 있다는 가정에 따라 30 일로 설정 되었습니다. Exchange Online 사서함은 기본적으로 14 일에 대 한 삭제 된 항목을 유지 하도록 구성 됩니다. 하지만 최대 30 일에이 설정을 변경할 수 있습니다. 자세한 내용은 [온라인 Exchange 사서함에 대 한 삭제 된 항목 보존 기간 변경](https://go.microsoft.com/fwlink/p/?LinkId=286940)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p109">We recommend that the retention period (defined by the  _AgeLimitForRetention_ parameter) for the Recoverable Items RPT is the same as the deleted item retention period for the mailboxes that the RPT will be applied to. This allows a user the entire deleted item retention period to recover deleted items before they are moved to the archive mailbox. In the previous example, the retention period was set to 30 days based on the assumption that the deleted item retention period for mailboxes is also 30 days. An Exchange Online mailbox is configured to retain deleted items for 14 days, by default. But you can change this setting to a maximum of 30 days. For more information, see [Change the deleted item retention period for a mailbox in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940).</span></span> 
  
## <a name="step-2-create-a-new-retention-policy-for-mailboxes-on-hold"></a><span data-ttu-id="ce53e-160">2단계: 보류된 사서함에 대한 새로운 보존 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-160">Step 2: Create a new retention policy for mailboxes on hold</span></span>

<span data-ttu-id="ce53e-p110">다음 단계는 새로운 보존 정책을 만들고 1단계에서 만든 복구 가능한 항목 RPT 등 이 새로운 보존 정책에 보존 태그를 추가하는 것입니다. 새로운 보존 정책은 다음 단계에서 보류된 사서함에 적용됩니다. </span><span class="sxs-lookup"><span data-stu-id="ce53e-p110">The next step is to create a new retention policy and add retention tags to it, including the Recoverable Items RPT that you created in Step 1. This new policy will be applied to mailboxes on hold in the next step.</span></span> 
  
<span data-ttu-id="ce53e-p111">새로운 보존 정책을 만들기 전에 추가할 추가적인 보존 태그를 결정합니다. 기본 MRM 정책에 추가되는 보존 태그의 목록 및 새로운 보존 태그에 대한 정보를 확인하려면 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p111">Before you create the new retention policy, determine the additional retention tags that you want to add. For a list of the retention tags that are added to the Default MRM Policy and for information about creating new retention tags, see the following:</span></span>
  
- [<span data-ttu-id="ce53e-165">기본 보존 정책 in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="ce53e-165">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- [<span data-ttu-id="ce53e-166">보존 정책 태그를 지 원하는 기본 폴더</span><span class="sxs-lookup"><span data-stu-id="ce53e-166">Default folders that support Retention Policy Tags</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=746957)
    
- <span data-ttu-id="ce53e-167">[보존 정책 만들기](https://go.microsoft.com/fwlink/p/?LinkId=404422) 항목의 "보존 태그 만들기" 섹션.</span><span class="sxs-lookup"><span data-stu-id="ce53e-167">The "Create a retention tag" section in the [Create a Retention Policy](https://go.microsoft.com/fwlink/p/?LinkId=404422) topic.</span></span>
    
<span data-ttu-id="ce53e-168">EAC 또는 Exchange Online PowerShell 보존 정책 만들기를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-168">You can use the EAC or Exchange Online PowerShell to create a retention policy.</span></span>
  
### <a name="use-the-eac-to-create-a-retention-policy"></a><span data-ttu-id="ce53e-169">EAC를 사용하여 보존 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="ce53e-169">Use the EAC to create a retention policy</span></span>
  
1. <span data-ttu-id="ce53e-170">EAC에서 **규정 준수 관리** 로 이동 \> **보존 정책**, 다음 **추가** 클릭 하 고 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif)합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-170">In the EAC, go to **Compliance management** \> **Retention policies**, and then click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span>
    
2. <span data-ttu-id="ce53e-171">**새 보존 정책** 페이지의 **이름**에서 **MRM Policy for Mailboxes on Hold** 등 보존 정책의 목적을 설명하는 이름을 입력합니다. </span><span class="sxs-lookup"><span data-stu-id="ce53e-171">On the **New retention policy** page, under **Name**, type a name that describes the purpose of the retention policy; for example, **MRM Policy for Mailboxes on Hold**.</span></span> 
    
3. <span data-ttu-id="ce53e-172">**보존 태그** **추가** 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif)합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-172">Under **Retention tags**, click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="ce53e-173">보존 태그 목록에서 1단계에서 만든 복구 가능한 항목 RPT를 선택한 다음 **추가**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-173">In the list of retention tags, select the Recoverable Items RPT that you created in Step 1, and then click **Add**.</span></span>
    
    ![사용자 지정 복구 가능한 항목 보존 태그 선택](media/eb49866b-bdef-4fcd-a6d9-01607c01249b.png)
  
5. <span data-ttu-id="ce53e-p112">보존 정책에 추가할 추가적인 보존 태그를 선택합니다. 예를 들어 기존 MRM 정책에 포함되어 있는 것과 동일한 태그를 추가하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p112">Select additional retention tags to add to the retention policy. For example, you might want to add the same tags that are included in the Default MRM Policy.</span></span>
    
6. <span data-ttu-id="ce53e-177">보존 태그 추가가 완료되면 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-177">When you're finished adding retention tags, click **OK**.</span></span>
    
7. <span data-ttu-id="ce53e-178">**저장**을 클릭하여 새 보존 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-178">Click **Save** to create the new retention policy.</span></span> 
    
    <span data-ttu-id="ce53e-179">보존 정책에 연결된 보존 태그가 세부 정보 창에 표시된다는 점에 유의하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-179">Notice that the retention tags linked to the retention policy are displayed in the details pane.</span></span>
    
    ![보존 정책에 연결된 보존 태그가 세부 정보 창에 표시됩니다.](media/dad1c8f4-9928-4d6d-991a-6f6c5194eceb.png)
  
### <a name="use-exchange-online-powershell-to-create-a-retention-policy"></a><span data-ttu-id="ce53e-181">Exchange Online PowerShell을 사용 하 여 보존 정책을 만들려면</span><span class="sxs-lookup"><span data-stu-id="ce53e-181">Use Exchange Online PowerShell to create a retention policy</span></span>
  
<span data-ttu-id="ce53e-182">보류된 사서함에 대한 새 보존 정책을 만들려면 다음 명령을 실행합니다. </span><span class="sxs-lookup"><span data-stu-id="ce53e-182">Run the following command to create new retention policy for mailboxes on hold.</span></span> 
  
```
New-RetentionPolicy <Name of retention policy>  -RetentionPolicyTagLinks <list of retention tags>

```

<span data-ttu-id="ce53e-183">예를 들어 다음 명령을 사용하면 보존 정책 및 이전 그림에 표시되어 있는 연결된 보존 태그가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-183">For example, the following command creates the retention policy and linked retention tags that is displayed in the previous illustration.</span></span>
  
```
New-RetentionPolicy "MRM Policy for Mailboxes on Hold"  -RetentionPolicyTagLinks "Recoverable Items 30 days for mailboxes on hold","1 Month Delete","1 Week Delete","1 Year Delete","5 Year Delete","6 Month Delete","Default 2 year move to archive","Junk Email","Never Delete","Personal 1 year move to archive","Personal 5 year move to archive"
```
  
## <a name="step-3-apply-the-new-retention-policy-to-mailboxes-on-hold"></a><span data-ttu-id="ce53e-184">3단계: 보류된 사서함에 새로운 보존 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-184">Step 3: Apply the new retention policy to mailboxes on hold</span></span>

<span data-ttu-id="ce53e-p113">조직에서 사서함 보류에 2 단계에서에서 만든 새 보존 정책을 적용 하려면 마지막 단계가입니다. EAC 또는 Exchange Online PowerShell를 사용 하 여 단일 사서함에 또는 여러 사서함에 보존 정책을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p113">The last step is to apply the new retention policy that you created in Step 2 to mailboxes on hold in your organization. You can use the EAC or Exchange Online PowerShell to apply the retention policy to a single mailbox or to multiple mailboxes.</span></span> 
  
### <a name="use-the-eac-to-apply-the-new-retention-policy"></a><span data-ttu-id="ce53e-187">EAC를 사용하여 새 보존 정책 적용하기</span><span class="sxs-lookup"><span data-stu-id="ce53e-187">Use the EAC to apply the new retention policy</span></span>
  
1. <span data-ttu-id="ce53e-188">**받는 사람** 에 게 이동 \> **사서함**입니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-188">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="ce53e-189">목록 보기에서 보존 정책을 적용 하려는 사서함을 선택 하 고 **편집** 을 클릭 한 다음 ![편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-189">In the list view, select the mailbox you want to apply the retention policy to, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
3. <span data-ttu-id="ce53e-190">**사용자 사서함** 페이지에서 **사서함 기능**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-190">On the **User Mailbox** page, click **Mailbox features**.</span></span>
    
4. <span data-ttu-id="ce53e-191">**보존 정책**에서 2단계에서 만든 보존 정책을 선택하고 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-191">Under **Retention policy**, select the retention policy that you created in Step 2, and then click **Save**.</span></span>
    
<span data-ttu-id="ce53e-192">EAC를 사용하여 여러 사서함에 보존 정책을 적용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-192">You can also use the EAC to apply the retention policy to multiple mailboxes.</span></span>
  
1. <span data-ttu-id="ce53e-193">**받는 사람** 에 게 이동 \> **사서함**입니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-193">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="ce53e-194">목록 보기에서 Shift 또는 Ctrl 키를 사용하여 여러 개의 사서함을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-194">In the list view, use the Shift or Ctrl keys to select multiple mailboxes.</span></span>
    
3. <span data-ttu-id="ce53e-195">세부 정보 창에서 **기타 옵션**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-195">In the details pane, click **More options**.</span></span>
    
4. <span data-ttu-id="ce53e-196">**보존 정책**에서 **업데이트**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-196">Under **Retention Policy**, click **Update**.</span></span>
    
5. <span data-ttu-id="ce53e-197">**대량 할당 보존 정책** 페이지에서 2단계에서 만든 보존 정책을 선택하고  **저장**을 클릭합니다. </span><span class="sxs-lookup"><span data-stu-id="ce53e-197">On the **Bulk assign retention policy** page, select the retention policy that you created in Step 2, and then click **Save**.</span></span> 
    
### <a name="use-exchange-online-powershell-to-apply-the-new-retention-policy"></a><span data-ttu-id="ce53e-198">Exchange Online PowerShell을 사용 하 여 새 보존 정책을 적용 하려면</span><span class="sxs-lookup"><span data-stu-id="ce53e-198">Use Exchange Online PowerShell to apply the new retention policy</span></span>
  
<span data-ttu-id="ce53e-p114">Exchange Online PowerShell를 사용 하 여 단일 사서함에 새 보존 정책을 적용할 수 있습니다. 이지만 PowerShell의 실제 전원은 신속 하 게 식별할 원본 위치 유지 또는 소송 보존으로 설정 되며 다음에 새 보존 정책을 모든 사서함에 적용 하는 조직에서 사서함 유지 (영문) 단일 명령을 모두 사용할 수 있습니다. 다음은 하나 이상의 사서함에 보존 정책을 적용 하려면 Exchange PowerShell을 사용 하 여의 몇가지 예입니다. 이 예제에서는 모든 2 단계에서에서 만든 보존 정책을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p114">You can use Exchange Online PowerShell to apply a new retention policy to a single mailbox. But the real power of PowerShell is that you can use it to quickly identify all the mailboxes in your organization that are on either Litigation Hold or In-Place Hold, and then apply the new retention policy to all mailboxes on hold in a single command. Here are some examples of using Exchange PowerShell to apply a retention policy to one or more mailboxes. All of the examples apply the retention policy that was created in Step 2.</span></span>
  
<span data-ttu-id="ce53e-203">이 예에서는 Pilar Pinilla의 사서함에 새로운 보존 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-203">This example applies the new retention policy to Pilar Pinilla's mailbox.</span></span>
  
```
Set-Mailbox "Pilar Pinilla" -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="ce53e-204">이 예에서는 조직의 모든 소송 보존 사서함에 새로운 보존 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-204">This example applies the new retention policy to all mailboxes in the organization that are on Litigation Hold.</span></span>
  
```
$LitigationHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'}
```

```
$LitigationHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="ce53e-205">이 예에서는 조직의 모든 원본 위치 유지 사서함에 새로운 보존 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-205">This example applies the new retention policy to all mailboxes in the organization that are on In-Place Hold.</span></span>
  
```
$InPlaceHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null}
```

```
$InPlaceHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="ce53e-206">**Get-Mailbox** cmdlet를 사용하여 새로운 보존 정책이 적용되었는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-206">You can use the **Get-Mailbox** cmdlet to verify that the new retention policy was applied.</span></span> 
  
<span data-ttu-id="ce53e-207">다음은 이전 예에서 소송 보존 사서함 및 원본 위치 유지 사서함에 "보류된 사서함에 대한 MRM 정책" 보존 정책이 적용되었는지 확인하기 위한 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-207">Here are some examples to verify that the commands in the previous examples applied the "MRM Policy for Mailboxes on Hold" retention policy to mailboxes on Litigation Hold and mailboxes on In-Place Hold.</span></span>
  
```
Get-Mailbox "Pilar Pinilla" | Select RetentionPolicy
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'} | FT DisplayName,RetentionPolicy -Auto
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null} | FT DisplayName,RetentionPolicy -Auto
```
  
## <a name="optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings"></a><span data-ttu-id="ce53e-208">(옵션) 4단계: 관리되는 폴더 도우미를 실행하여 새로운 보존 설정을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-208">(Optional) Step 4: Run the Managed Folder Assistant to apply the new retention settings</span></span>

<span data-ttu-id="ce53e-p115">보류에 있는 사서함에 새 보존 정책을 적용 한 후 걸릴 수 최대 7 일 Exchange 온라인는 관리 되는 폴더 도우미 설정을 사용 하 여 새 보존 정책에서 이러한 사서함을 처리 하는 데에 대 한 합니다. 관리 되는 폴더 도우미를 실행 하려면를 기다리지 않고 수동으로에 새 보존 정책을 적용 하는 사서함을 처리 하는 데 길잡이 트리거하 **Start-managedfolderassistant** cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p115">After you apply the new retention policy to mailboxes on hold, it can take up to 7 days in Exchange Online for the Managed Folder Assistant to process these mailboxes using the settings in the new retention policy. Instead of waiting for the Managed Folder Assistant to run, you can use the **Start-ManagedFolderAssistant** cmdlet to manually trigger the assistant to process the mailboxes that you applied the new retention policy to.</span></span> 
  
<span data-ttu-id="ce53e-211">다음 명령을 실행하여 Pilar Pinilla의 사서함에 관리되는 폴더 도우미를 실행합니다. </span><span class="sxs-lookup"><span data-stu-id="ce53e-211">Run the following command to start the Managed Folder Assistant for Pilar Pinilla's mailbox.</span></span>
  
```
Start-ManagedFolderAssistant "Pilar Pinilla"
```

<span data-ttu-id="ce53e-212">다음 명령을 실행하여 보류된 모든 사서함에 관리되는 폴더 도우미를 실행합니다. </span><span class="sxs-lookup"><span data-stu-id="ce53e-212">Run the following commands to start the Managed Folder Assistant for all mailboxes on hold.</span></span>
  
```
$MailboxesOnHold = Get-Mailbox -ResultSize unlimited | Where-Object {($_.InPlaceHolds -ne $null) -or ($_.LitigationHoldEnabled -eq "True")}
```

```
$MailboxesOnHold.DistinguishedName | Start-ManagedFolderAssistant
```

## <a name="more-information"></a><span data-ttu-id="ce53e-213">추가 정보</span><span class="sxs-lookup"><span data-stu-id="ce53e-213">More information</span></span>

- <span data-ttu-id="ce53e-p116">사용자의 보관 사서함을 활성화 한 후에 (아니라 항목 복구 가능한 항목 폴더에서) 사서함의 다른 항목은 보관 사서함으로 이동할 수 있습니다는 방향을 지시 하는 것이 좋습니다. 이 Exchange Online 사서함에 할당 된 기본 MRM 정책 항목 된 사서함에 게 배달 되거나 사용자가 만든 날짜 로부터 2 년 항목 보관 사서함으로 이동 하는 보존 태그 (명명 된 기본 2 년 후 보관 함으로 이동)를 포함 하기 때문에 사용자입니다. 자세한 내용은 [Exchange Online의 기본 보존 정책](https://go.microsoft.com/fwlink/p/?LinkId=746954) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p116">After you enable a user's archive mailbox, consider telling the user that other items in their mailbox (not just items in the Recoverable Items folder) might be moved to the archive mailbox. This is because the Default MRM Policy that's assigned to Exchange Online mailboxes contains a retention tag (named Default 2 years move to archive) that moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user. For more information, see [Default Retention Policy in Exchange Online ](https://go.microsoft.com/fwlink/p/?LinkId=746954)</span></span>
    
- <span data-ttu-id="ce53e-p117">사용자의 보관 사서함을 활성화 한 후 복구할 수 있는 사용자가 자신의 보관 사서함의 복구 가능한 항목 폴더에서 항목 삭제 알 수 있습니다. 보관 사서함의 **지운 편지함** 폴더를 선택 하 고 다음 **홈** 탭에서 **서버에서 지운 편지함 복구** 를 클릭 하 여 Outlook에서이 작업을 수행할 수 있습니다. 삭제 된 항목을 복구 하는 중에 대 한 자세한 내용은 [Windows 용 Outlook에서에서 항목 삭제 된 복구를](https://go.microsoft.com/fwlink/p/?LinkId=624829)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ce53e-p117">After you enable a user's archive mailbox, you might also tell the user that they can recover deleted items in the Recoverable Items folder in their archive mailbox. They can do this in Outlook by selecting the **Deleted Items** folder in the archive mailbox, and then clicking **Recover Deleted Items from Server** on the **Home** tab. For more information about recovering deleted items, see [Recover deleted items in Outlook for Windows](https://go.microsoft.com/fwlink/p/?LinkId=624829).</span></span> 
