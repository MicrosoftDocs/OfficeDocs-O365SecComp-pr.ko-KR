---
title: 보류된 사물함의 복구 가능한 항목 할당량 증가
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a8bdcbdd-9298-462f-b889-df26037a990c
description: '보관 사서함을 사용 하도록 설정 하 고 자동 확장 보관을 설정 하 여 Office 365에서 사서함에 대 한 복구 가능한 항목 폴더의 크기를 늘립니다. '
ms.openlocfilehash: ebb052ba17ba8a84076e1e75a82713cc5cf437a1
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218478"
---
# <a name="increase-the-recoverable-items-quota-for-mailboxes-on-hold"></a><span data-ttu-id="881f9-103">보류된 사물함의 복구 가능한 항목 할당량 증가</span><span class="sxs-lookup"><span data-stu-id="881f9-103">Increase the Recoverable Items quota for mailboxes on hold</span></span>

<span data-ttu-id="881f9-p101">Exchange Online의 새 사서함에 자동으로 적용 되는 기본 mrm 정책 이라는 기본 보존 정책에는 복구 가능한 항목 14 일 후 보관 함으로 이동 되는 보존 태그가 포함 되어 있습니다. 이 보존 태그는 사용자의 기본 사서함에 있는 복구 가능한 항목 폴더의 항목을 사용자의 보관 사서함에 있는 복구 가능한 항목 폴더로 이동 합니다 (해당 항목에 대 한 보존 기간 14 일). 이 경우 사용자의 보관 사서함을 사용 하도록 설정 해야 합니다. 보관 사서함을 사용 하도록 설정 하지 않은 경우 보존 기간이 만료 되 면 아무 작업도 수행 되지 않습니다 (보류 중인 사서함에 대 한 복구 가능한 항목 폴더의 항목은 보관 사서함으로 이동 되지 않음). 보류 중인 사서함에서는 아무 것도 삭제 되지 않으므로 복구 가능한 항목 폴더의 저장소 할당량을 초과 하는 경우에는 특히 사용자의 보관 사서함이 사용 하도록 설정 되어 있지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-p101">The default retention policy—named Default MRM Policy—that is automatically applied to new mailboxes in Exchange Online contains a retention tag named Recoverable Items 14 days move to archive. This retention tag moves items from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in the user's archive mailbox after the 14-day retention period expires for an item. For this to happen, the user's archive mailbox must be enabled. If the archive mailbox isn't enabled, no action is taken, which means that items in the Recoverable Items folder for a mailbox on hold aren't moved to the archive mailbox after the 14-day retention period expires. Because nothing is deleted from a mailbox on hold, it's possible that the storage quota for the Recoverable Items folder might be exceeded, especially if the user's archive mailbox isn't enabled.</span></span> 
  
<span data-ttu-id="881f9-p102">Exchange Online의 사서함에 대 한 보존을 설정 하면이 제한을 초과할 가능성을 줄이기 위해 복구 가능한 항목 폴더의 저장소 할당량이 자동으로 30gb에서 100 GB로 증가 합니다. 보관 사서함을 사용 하도록 설정 하면 보관 사서함의 복구 가능한 항목 폴더에 대 한 저장소 할당량도 30gb에서 100 GB로 증가 합니다. Exchange Online의 자동 확장 보관 기능이 사용 하도록 설정 된 경우 사용자 보관의 복구 가능한 항목 폴더에 대 한 저장소 할당량은 무제한으로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-p102">To help reduce the chance of exceeding this limit, the storage quota for the Recoverable Items folder is automatically increased from 30 GB to 100 GB when a hold is placed on a mailbox in Exchange Online. If the archive mailbox is enabled, the storage quota for the Recoverable Items folder in the archive mailbox is also increased from 30 GB to 100 GB. If the auto-expanding archiving feature in Exchange Online is enabled, the storage quota for the Recoverable Items folder in the user's archive will be unlimited.</span></span>
  
 <span data-ttu-id="881f9-112"> 다음 표는 복구 가능한 항목 폴더의 저장소 할당량을 간략하게 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-112">The following table summarizes the storage quota for the Recoverable Items folder.</span></span> 
  
|<span data-ttu-id="881f9-113">**복구 가능한 항목 폴더 위치**</span><span class="sxs-lookup"><span data-stu-id="881f9-113">**Location of Recoverable Items folder**</span></span>|<span data-ttu-id="881f9-114">**보류되지 않은 사서함**</span><span class="sxs-lookup"><span data-stu-id="881f9-114">**Mailboxes not on hold**</span></span>|<span data-ttu-id="881f9-115">**보류된 사서함**</span><span class="sxs-lookup"><span data-stu-id="881f9-115">**Mailboxes on hold**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="881f9-116">기본 사서함</span><span class="sxs-lookup"><span data-stu-id="881f9-116">Primary mailbox</span></span>  <br/> |<span data-ttu-id="881f9-117">30GB</span><span class="sxs-lookup"><span data-stu-id="881f9-117">30 GB</span></span>  <br/> |<span data-ttu-id="881f9-118">100GB</span><span class="sxs-lookup"><span data-stu-id="881f9-118">100 GB</span></span>  <br/> |
|<span data-ttu-id="881f9-119">보관 사서함<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="881f9-119">Archive mailbox<sup>\*</sup></span></span> <br/> |<span data-ttu-id="881f9-120">제한 없음</span><span class="sxs-lookup"><span data-stu-id="881f9-120">Unlimited</span></span>  <br/> |<span data-ttu-id="881f9-121">제한 없음</span><span class="sxs-lookup"><span data-stu-id="881f9-121">Unlimited</span></span>  <br/> |
|<span data-ttu-id="881f9-122">**복구 가능한 항목 폴더 할당량**</span><span class="sxs-lookup"><span data-stu-id="881f9-122">**Total storage quota for the Recoverable Items folder**</span></span> <br/> |<span data-ttu-id="881f9-123">제한 없음</span><span class="sxs-lookup"><span data-stu-id="881f9-123">Unlimited</span></span>  <br/> |<span data-ttu-id="881f9-124">제한 없음</span><span class="sxs-lookup"><span data-stu-id="881f9-124">Unlimited</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="881f9-p103"><sup>\*</sup>Exchange Online (계획 2) 라이선스가 있는 사용자의 경우 보관 사서함의 초기 저장소 할당량은 100 GB입니다. 그러나 보류 중인 사서함에 대해 자동 확장 보관을 설정 하면 보관 사서함 및 복구 가능한 항목 폴더의 저장소 할당량이 110 GB로 증가 합니다. 필요한 경우 추가 보관 저장소 공간이 프로 비전 되어 보관 저장소의 크기가 무제한으로 제공 됩니다. 자동 확장 보관에 대 한 자세한 내용은 [Office 365의 무제한 보관 개요](unlimited-archiving.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="881f9-p103"><sup>\*</sup> The initial storage quota for the archive mailbox is 100 GB for users with an Exchange Online (Plan 2) license. However, when auto-expanding archiving is turned on for mailboxes on hold, the storage quota for both the archive mailbox and the Recoverable Items folder is increased to 110 GB. Additional archive storage space will be provisioned when necessary which results in an unlimited amount of archive storage. For more information about auto-expanding archiving, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
<span data-ttu-id="881f9-129">보류된 사서함의 기본 사서함에 있는 복구 가능한 항목 폴더의 저장소 할당량이 한도에 도달하려는 경우 다음 항목을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-129">When the storage quota for the Recoverable Items folder in the primary mailbox of a mailbox on hold is close to reaching its limit, you can do the following things:</span></span>
  
- <span data-ttu-id="881f9-p104">**보관 사서함을 사용 하도록 설정 하 고 자동 확장 보관을 설정** 하면 보관 사서함을 사용 하도록 설정 하 고 Exchange에서 자동 확장 보관 기능을 설정 하 여 복구 가능한 항목 폴더에 대해 무제한 저장소 용량을 사용 하도록 설정할 수 있습니다. 온라인. 이를 통해 기본 사서함의 복구 가능한 항목 폴더에 대해 110이 발생 하 고 사용자 보관의 복구 가능한 항목 폴더에 대해 무제한의 저장 용량을 사용할 수 있습니다. 방법: office [365 보안 &amp; 및 준수 센터에서 보관 사서함을 사용 하도록 설정](enable-archive-mailboxes.md) 하 고 [office 365에서 무제한 보관을 사용 하도록 설정](enable-unlimited-archiving.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-p104">**Enable the archive mailbox and turn on auto-expanding archiving** - You can enable an unlimited storage capacity for the Recoverable Items folder simply by enabling the archive mailbox and then turning on the auto-expanding archiving feature in Exchange Online. This results in 110 GB for the Recoverable Items folder in the primary mailbox and an unlimited amount of storage capacity for the Recoverable Items folder in the user's archive. See how: [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="881f9-p105">복구 가능한 항목 폴더의 저장소 할당량을 초과 하는 사서함에 대 한 보관을 사용 하도록 설정한 후에는 관리 되는 폴더 도우미를 실행 하 여 사용자가 만료 된 항목을 이동 하도록 도우미를 수동으로 시작 하 여 사서함을 처리할 수 있습니다. 보관 사서함의 복구 가능한 항목 폴더 자세한 내용은 [4 단계](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) 를 참조 하세요. 사용자 사서함의 다른 항목은 새 보관 사서함으로 이동할 수 있습니다. 보관 사서함을 사용 하도록 설정한 후 사용자에 게이를 알리는 것을 고려할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-p105">After you enable the archive for a mailbox that's close to exceeding the storage quota for the Recoverable Items folder, you might want to run the Managed Folder Assistant to manually trigger the assistant to process the mailbox so that expired items are moved the Recoverable Items folder in the archive mailbox. See [Step 4](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) for instructions. Note that other items in the user's mailbox might be moved to the new archive mailbox. Consider telling the user that this may happen after you enable the archive mailbox.</span></span> 
  
- <span data-ttu-id="881f9-p106">**보류 중인 사서함에 대 한 사용자 지정 보존 정책 만들기** -보관 사서함을 사용 하도록 설정 하 고 사서함에 대해 소송 보존 또는 원본 위치 유지를 자동 확장 하는 데 사용할 수 있습니다. 놓습니다. 이를 통해 보류 중인 사서함에 적용 되는 기본 mrm 정책과는 다른 보류 중인 사서함에 보존 정책을 적용할 수 있습니다. 이를 통해 특별히 사서함에 맞게 디자인 된 보존 태그를 적용할 수 있습니다. 여기에는 복구 가능한 항목 폴더에 대 한 새 보존 태그를 만드는 작업이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-p106">**Create a custom retention policy for mailboxes on hold** - In addition to enabling the archive mailbox and auto-expanding archiving for mailboxes on Litigation Hold or In-Place Hold, you might also want to create a custom retention policy for mailboxes on hold. This let's you apply a retention policy to mailboxes on hold that's different from the Default MRM Policy that's applied to mailboxes that aren't on hold. This lets you to apply retention tags that are specifically designed for mailboxes on hold. This includes creating a new retention tag for the Recoverable Items folder.</span></span> 
    
<span data-ttu-id="881f9-141">이 항목의 나머지 부분에서는 보류된 사서함에 대한 사용자 지정 보존 정책을 만드는 단계별 절차를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-141">The remainder of this topic describes the step-by-step procedures to create a custom retention policy for mailboxes on hold.</span></span>
  
[<span data-ttu-id="881f9-142">1단계: 복구 가능한 항목 폴더에 대한 사용자 지정 보존 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-142">Step 1: Create a custom retention tag for the Recoverable Items folder</span></span>](#step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder)

<span data-ttu-id="881f9-143">[[2 단계: 보류 된 사서함에 대 한 새 보존 정책 만들기](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)</span><span class="sxs-lookup"><span data-stu-id="881f9-143">[[Step 2: Create a new retention policy for mailboxes on hold](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)</span></span>

[<span data-ttu-id="881f9-144">3단계: 보류된 사서함에 새로운 보존 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-144">Step 3: Apply the new retention policy to mailboxes on hold</span></span>](#step-3-apply-the-new-retention-policy-to-mailboxes-on-hold)

[<span data-ttu-id="881f9-145">(옵션)4단계: 관리되는 폴더 도우미를 실행하여 새로운 보존 설정을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-145">(Optional) Step 4: Run the Managed Folder Assistant to apply the new retention settings</span></span>](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings)
  
## <a name="step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder"></a><span data-ttu-id="881f9-146">1단계: 복구 가능한 항목 폴더에 대한 사용자 지정 보존 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-146">Step 1: Create a custom retention tag for the Recoverable Items folder</span></span>

<span data-ttu-id="881f9-p107">첫 번째 단계는 복구 가능한 항목 폴더에 대 한 사용자 지정 보존 태그 (보존 정책 태그 또는 RPT 라고 함)를 만드는 것입니다. 앞에서 설명한 것 처럼이 RPT는 사용자의 기본 사서함에 있는 복구할 수 있는 항목 폴더의 항목을 사용자의 보관 사서함에 있는 복구할 수 있는 항목 폴더로 이동 합니다. PowerShell을 사용 하 여 복구 가능한 항목 폴더에 대 한 RPT를 만들어야 합니다. EAC (Exchange 관리 센터)를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-p107">The first step is to create a custom retention tag (called a retention policy tag or RPT) for the Recoverable Items folder. As previously explained, this RPT moves items from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in the user's archive mailbox. You have to use PowerShell to create an RPT for the Recoverable Items folder. You can't use the Exchange admin center (EAC).</span></span> 
  
1. <span data-ttu-id="881f9-151">[Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283)(원격 PowerShell을 사용하여 Exchange Online에 연결)</span><span class="sxs-lookup"><span data-stu-id="881f9-151">[Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283)</span></span>
    
2. <span data-ttu-id="881f9-152">복구할 수 있는 항목 폴더에 대한 새로운 RPT를 만들려면 다음 명령을 실행합니다. </span><span class="sxs-lookup"><span data-stu-id="881f9-152">Run the following command to create a new RPT for the Recoverable Items folder:</span></span> 
    
    ```
    New-RetentionPolicyTag -Name <Name of RPT> -Type RecoverableItems -AgeLimitForRetention <Number of days> -RetentionAction MoveToArchive
    ```

    <span data-ttu-id="881f9-p108">예를 들어 다음 명령을 사용하면 보존 기간이 30일인 “보류된 사서함의 30일 복구 가능한 항목”이라는 복구 가능한 항목 폴더에 대한 RPT가 만들어집니다. 이는 어떤 항목이 복구 가능한 항목 폴더에서 30일 동안 있은 후 사용자의 보관 사서함에 있는 복구 가능한 항목 폴더로 이동함을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-p108">For example, the following command creates a RPT for the Recoverable Items folder named "Recoverable Items 30 days for mailboxes on hold", with a retention period of 30 days. This means that after an item has been in the Recoverable Items folder for 30 days, it will be moved to the Recoverable Items folder in the user's archive mailbox.</span></span>
    
    ```
    New-RetentionPolicyTag -Name "Recoverable Items 30 days for mailboxes on hold" -Type RecoverableItems -AgeLimitForRetention 30 -RetentionAction MoveToArchive
    ```

    > [!TIP]
    > <span data-ttu-id="881f9-p109">복구 가능한 항목 rpt의 보존 기간은 rpt가 적용 __ 될 사서함에 대 한 삭제 된 항목 보존 기간과 동일 하 게 유지 하는 것이 좋습니다. 이렇게 하면 삭제 된 항목 보존 기간까지 삭제 된 항목을 보관 사서함으로 이동 하기 전에 복구할 수 있습니다. 이전 예에서는 사서함의 삭제 된 항목 보존 기간이 30 일 이기도 한 가정을 기준으로 보존 기간이 30 일로 설정 되었습니다. 기본적으로 Exchange Online 사서함은 14 일 동안 삭제 된 항목을 보존 하도록 구성 됩니다. 그러나이 설정을 최대 30 일로 변경할 수 있습니다. 자세한 내용은 [Exchange Online에서 사서함에 대 한 삭제 된 항목 보존 기간 변경을](https://go.microsoft.com/fwlink/p/?LinkId=286940)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="881f9-p109">We recommend that the retention period (defined by the  _AgeLimitForRetention_ parameter) for the Recoverable Items RPT is the same as the deleted item retention period for the mailboxes that the RPT will be applied to. This allows a user the entire deleted item retention period to recover deleted items before they are moved to the archive mailbox. In the previous example, the retention period was set to 30 days based on the assumption that the deleted item retention period for mailboxes is also 30 days. An Exchange Online mailbox is configured to retain deleted items for 14 days, by default. But you can change this setting to a maximum of 30 days. For more information, see [Change the deleted item retention period for a mailbox in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940).</span></span> 
  
## <a name="step-2-create-a-new-retention-policy-for-mailboxes-on-hold"></a><span data-ttu-id="881f9-161">2단계: 보류된 사서함에 대한 새로운 보존 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-161">Step 2: Create a new retention policy for mailboxes on hold</span></span>

<span data-ttu-id="881f9-p110">다음 단계는 새로운 보존 정책을 만들고 1단계에서 만든 복구 가능한 항목 RPT 등 이 새로운 보존 정책에 보존 태그를 추가하는 것입니다. 새로운 보존 정책은 다음 단계에서 보류된 사서함에 적용됩니다. </span><span class="sxs-lookup"><span data-stu-id="881f9-p110">The next step is to create a new retention policy and add retention tags to it, including the Recoverable Items RPT that you created in Step 1. This new policy will be applied to mailboxes on hold in the next step.</span></span> 
  
<span data-ttu-id="881f9-p111">새로운 보존 정책을 만들기 전에 추가할 추가적인 보존 태그를 결정합니다. 기본 MRM 정책에 추가되는 보존 태그의 목록 및 새로운 보존 태그에 대한 정보를 확인하려면 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="881f9-p111">Before you create the new retention policy, determine the additional retention tags that you want to add. For a list of the retention tags that are added to the Default MRM Policy and for information about creating new retention tags, see the following:</span></span>
  
- [<span data-ttu-id="881f9-166">Exchange Online의 기본 보존 정책</span><span class="sxs-lookup"><span data-stu-id="881f9-166">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- [<span data-ttu-id="881f9-167">보존 정책 태그를 지원하는 기본 폴더</span><span class="sxs-lookup"><span data-stu-id="881f9-167">Default folders that support Retention Policy Tags</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=746957)
    
- <span data-ttu-id="881f9-168">[보존 정책 만들기](https://go.microsoft.com/fwlink/p/?LinkId=404422) 항목의 "보존 태그 만들기" 섹션</span><span class="sxs-lookup"><span data-stu-id="881f9-168">The "Create a retention tag" section in the [Create a Retention Policy](https://go.microsoft.com/fwlink/p/?LinkId=404422) topic.</span></span>
    
<span data-ttu-id="881f9-169">EAC 또는 Exchange Online PowerShell을 사용 하 여 보존 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-169">You can use the EAC or Exchange Online PowerShell to create a retention policy.</span></span>
  
### <a name="use-the-eac-to-create-a-retention-policy"></a><span data-ttu-id="881f9-170">EAC를 사용하여 보존 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="881f9-170">Use the EAC to create a retention policy</span></span>
  
1. <span data-ttu-id="881f9-171">EAC에서 **준수 관리** \> **보존 정책**으로 이동한 다음 \*\*\*\* ![추가 아이콘](media/ITPro-EAC-AddIcon.gif)추가를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-171">In the EAC, go to **Compliance management** \> **Retention policies**, and then click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span>
    
2. <span data-ttu-id="881f9-172">**새 보존 정책** 페이지의 **이름**에서 **MRM Policy for Mailboxes on Hold** 등 보존 정책의 목적을 설명하는 이름을 입력합니다. </span><span class="sxs-lookup"><span data-stu-id="881f9-172">On the **New retention policy** page, under **Name**, type a name that describes the purpose of the retention policy; for example, **MRM Policy for Mailboxes on Hold**.</span></span> 
    
3. <span data-ttu-id="881f9-173">**보존 태그**에서 \*\*\*\* ![추가 아이콘](media/ITPro-EAC-AddIcon.gif)추가를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-173">Under **Retention tags**, click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="881f9-174">보존 태그 목록에서 1단계에서 만든 복구 가능한 항목 RPT를 선택한 다음 **추가**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-174">In the list of retention tags, select the Recoverable Items RPT that you created in Step 1, and then click **Add**.</span></span>
    
    ![사용자 지정 복구 가능한 항목 보존 태그 선택](media/eb49866b-bdef-4fcd-a6d9-01607c01249b.png)
  
5. <span data-ttu-id="881f9-p112">보존 정책에 추가할 추가적인 보존 태그를 선택합니다. 예를 들어 기존 MRM 정책에 포함되어 있는 것과 동일한 태그를 추가하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-p112">Select additional retention tags to add to the retention policy. For example, you might want to add the same tags that are included in the Default MRM Policy.</span></span>
    
6. <span data-ttu-id="881f9-178">보존 태그 추가가 완료되면 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-178">When you're finished adding retention tags, click **OK**.</span></span>
    
7. <span data-ttu-id="881f9-179">**저장**을 클릭하여 새 보존 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-179">Click **Save** to create the new retention policy.</span></span> 
    
    <span data-ttu-id="881f9-180">보존 정책에 연결된 보존 태그가 세부 정보 창에 표시된다는 점에 유의하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-180">Notice that the retention tags linked to the retention policy are displayed in the details pane.</span></span>
    
    ![보존 정책에 연결된 보존 태그가 세부 정보 창에 표시됩니다.](media/dad1c8f4-9928-4d6d-991a-6f6c5194eceb.png)
  
### <a name="use-exchange-online-powershell-to-create-a-retention-policy"></a><span data-ttu-id="881f9-182">Exchange Online PowerShell을 사용 하 여 보존 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="881f9-182">Use Exchange Online PowerShell to create a retention policy</span></span>
  
<span data-ttu-id="881f9-183">보류된 사서함에 대한 새 보존 정책을 만들려면 다음 명령을 실행합니다. </span><span class="sxs-lookup"><span data-stu-id="881f9-183">Run the following command to create new retention policy for mailboxes on hold.</span></span> 
  
```
New-RetentionPolicy <Name of retention policy>  -RetentionPolicyTagLinks <list of retention tags>

```

<span data-ttu-id="881f9-184">예를 들어 다음 명령을 사용하면 보존 정책 및 이전 그림에 표시되어 있는 연결된 보존 태그가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-184">For example, the following command creates the retention policy and linked retention tags that is displayed in the previous illustration.</span></span>
  
```
New-RetentionPolicy "MRM Policy for Mailboxes on Hold"  -RetentionPolicyTagLinks "Recoverable Items 30 days for mailboxes on hold","1 Month Delete","1 Week Delete","1 Year Delete","5 Year Delete","6 Month Delete","Default 2 year move to archive","Junk Email","Never Delete","Personal 1 year move to archive","Personal 5 year move to archive"
```
  
## <a name="step-3-apply-the-new-retention-policy-to-mailboxes-on-hold"></a><span data-ttu-id="881f9-185">3단계: 보류된 사서함에 새로운 보존 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-185">Step 3: Apply the new retention policy to mailboxes on hold</span></span>

<span data-ttu-id="881f9-p113">마지막 단계는 2 단계에서 만든 새 보존 정책을 조직의 보류 된 사서함에 적용 하는 것입니다. EAC 또는 Exchange Online PowerShell을 사용 하 여 단일 사서함 이나 여러 사서함에 보존 정책을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-p113">The last step is to apply the new retention policy that you created in Step 2 to mailboxes on hold in your organization. You can use the EAC or Exchange Online PowerShell to apply the retention policy to a single mailbox or to multiple mailboxes.</span></span> 
  
### <a name="use-the-eac-to-apply-the-new-retention-policy"></a><span data-ttu-id="881f9-188">EAC를 사용하여 새 보존 정책 적용하기</span><span class="sxs-lookup"><span data-stu-id="881f9-188">Use the EAC to apply the new retention policy</span></span>
  
1. <span data-ttu-id="881f9-189">**받는 사람** \> **사서함**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-189">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="881f9-190">목록 보기에서 보존 정책을 적용할 사서함을 선택 하 고 편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) **편집** ![을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-190">In the list view, select the mailbox you want to apply the retention policy to, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
3. <span data-ttu-id="881f9-191">**사용자 사서함** 페이지에서 **사서함 기능**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-191">On the **User Mailbox** page, click **Mailbox features**.</span></span>
    
4. <span data-ttu-id="881f9-192">**보존 정책**에서 2단계에서 만든 보존 정책을 선택하고 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-192">Under **Retention policy**, select the retention policy that you created in Step 2, and then click **Save**.</span></span>
    
<span data-ttu-id="881f9-193">EAC를 사용하여 여러 사서함에 보존 정책을 적용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-193">You can also use the EAC to apply the retention policy to multiple mailboxes.</span></span>
  
1. <span data-ttu-id="881f9-194">**받는 사람** \> **사서함**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-194">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="881f9-195">목록 보기에서 Shift 또는 Ctrl 키를 사용하여 여러 개의 사서함을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-195">In the list view, use the Shift or Ctrl keys to select multiple mailboxes.</span></span>
    
3. <span data-ttu-id="881f9-196">세부 정보 창에서 **기타 옵션**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-196">In the details pane, click **More options**.</span></span>
    
4. <span data-ttu-id="881f9-197">**보존 정책**에서 **업데이트**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-197">Under **Retention Policy**, click **Update**.</span></span>
    
5. <span data-ttu-id="881f9-198">**대량 할당 보존 정책** 페이지에서 2단계에서 만든 보존 정책을 선택하고  **저장**을 클릭합니다. </span><span class="sxs-lookup"><span data-stu-id="881f9-198">On the **Bulk assign retention policy** page, select the retention policy that you created in Step 2, and then click **Save**.</span></span> 
    
### <a name="use-exchange-online-powershell-to-apply-the-new-retention-policy"></a><span data-ttu-id="881f9-199">Exchange Online PowerShell을 사용 하 여 새 보존 정책 적용</span><span class="sxs-lookup"><span data-stu-id="881f9-199">Use Exchange Online PowerShell to apply the new retention policy</span></span>
  
<span data-ttu-id="881f9-p114">Exchange Online PowerShell을 사용 하 여 단일 사서함에 새 보존 정책을 적용할 수 있습니다. 그러나 PowerShell의 실제 기능은 조직의 모든 사서함을 소송 보존 또는 원본 위치 유지 상태로 빠르게 식별 한 다음 단일 명령으로 보류 중인 모든 사서함에 새 보존 정책을 적용 하는 데 사용할 수 있다는 것입니다. 다음은 Exchange PowerShell을 사용 하 여 하나 이상의 사서함에 보존 정책을 적용 하는 몇 가지 예입니다. 모든 예제에서는 2 단계에서 만든 보존 정책을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-p114">You can use Exchange Online PowerShell to apply a new retention policy to a single mailbox. But the real power of PowerShell is that you can use it to quickly identify all the mailboxes in your organization that are on either Litigation Hold or In-Place Hold, and then apply the new retention policy to all mailboxes on hold in a single command. Here are some examples of using Exchange PowerShell to apply a retention policy to one or more mailboxes. All of the examples apply the retention policy that was created in Step 2.</span></span>
  
<span data-ttu-id="881f9-204">이 예에서는 Pilar Pinilla의 사서함에 새로운 보존 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-204">This example applies the new retention policy to Pilar Pinilla's mailbox.</span></span>
  
```
Set-Mailbox "Pilar Pinilla" -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="881f9-205">이 예에서는 조직의 모든 소송 보존 사서함에 새로운 보존 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-205">This example applies the new retention policy to all mailboxes in the organization that are on Litigation Hold.</span></span>
  
```
$LitigationHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'}
```

```
$LitigationHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="881f9-206">이 예에서는 조직의 모든 원본 위치 유지 사서함에 새로운 보존 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-206">This example applies the new retention policy to all mailboxes in the organization that are on In-Place Hold.</span></span>
  
```
$InPlaceHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null}
```

```
$InPlaceHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="881f9-207">**Get-Mailbox** cmdlet를 사용하여 새로운 보존 정책이 적용되었는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-207">You can use the **Get-Mailbox** cmdlet to verify that the new retention policy was applied.</span></span> 
  
<span data-ttu-id="881f9-208">다음은 이전 예에서 소송 보존 사서함 및 원본 위치 유지 사서함에 "보류된 사서함에 대한 MRM 정책" 보존 정책이 적용되었는지 확인하기 위한 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-208">Here are some examples to verify that the commands in the previous examples applied the "MRM Policy for Mailboxes on Hold" retention policy to mailboxes on Litigation Hold and mailboxes on In-Place Hold.</span></span>
  
```
Get-Mailbox "Pilar Pinilla" | Select RetentionPolicy
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'} | FT DisplayName,RetentionPolicy -Auto
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null} | FT DisplayName,RetentionPolicy -Auto
```
  
## <a name="optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings"></a><span data-ttu-id="881f9-209">(옵션) 4단계: 관리되는 폴더 도우미를 실행하여 새로운 보존 설정을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-209">(Optional) Step 4: Run the Managed Folder Assistant to apply the new retention settings</span></span>

<span data-ttu-id="881f9-p115">보류 중인 사서함에 새 보존 정책을 적용 하 고 나면 Exchange Online에서 관리 되는 폴더 도우미가 새 보존 정책의 설정을 사용 하 여 이러한 사서함을 처리 하는 데 최대 7 일이 걸릴 수 있습니다. 관리 되는 폴더 도우미가 실행 될 때까지 기다리지 않고, **먼저 시작** 관리자를 트리거하여 새 보존 정책을 적용 한 사서함을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="881f9-p115">After you apply the new retention policy to mailboxes on hold, it can take up to 7 days in Exchange Online for the Managed Folder Assistant to process these mailboxes using the settings in the new retention policy. Instead of waiting for the Managed Folder Assistant to run, you can use the **Start-ManagedFolderAssistant** cmdlet to manually trigger the assistant to process the mailboxes that you applied the new retention policy to.</span></span> 
  
<span data-ttu-id="881f9-212">다음 명령을 실행하여 Pilar Pinilla의 사서함에 관리되는 폴더 도우미를 실행합니다. </span><span class="sxs-lookup"><span data-stu-id="881f9-212">Run the following command to start the Managed Folder Assistant for Pilar Pinilla's mailbox.</span></span>
  
```
Start-ManagedFolderAssistant "Pilar Pinilla"
```

<span data-ttu-id="881f9-213">다음 명령을 실행하여 보류된 모든 사서함에 관리되는 폴더 도우미를 실행합니다. </span><span class="sxs-lookup"><span data-stu-id="881f9-213">Run the following commands to start the Managed Folder Assistant for all mailboxes on hold.</span></span>
  
```
$MailboxesOnHold = Get-Mailbox -ResultSize unlimited | Where-Object {($_.InPlaceHolds -ne $null) -or ($_.LitigationHoldEnabled -eq "True")}
```

```
$MailboxesOnHold.DistinguishedName | Start-ManagedFolderAssistant
```

## <a name="more-information"></a><span data-ttu-id="881f9-214">추가 정보</span><span class="sxs-lookup"><span data-stu-id="881f9-214">More information</span></span>

- <span data-ttu-id="881f9-p116">사용자의 보관 사서함을 사용 하도록 설정한 후에는 사서함의 다른 항목 (복구 가능한 항목 폴더에 있는 항목은 제외)이 보관 사서함으로 이동 될 수 있음을 사용자에 게 알려 주는 것이 좋습니다. 이는 Exchange Online 사서함에 할당 된 기본 mrm 정책에 항목이 사서함으로 배달 된 후 2 년 후에 항목을 보관 사서함으로 이동 하는 보존 태그 (기본 2 년을 보관 함으로 이동 함)가 포함 되어 있기 때문입니다. 가. 자세한 내용은 [Exchange Online의 기본 보존 정책](https://go.microsoft.com/fwlink/p/?LinkId=746954) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="881f9-p116">After you enable a user's archive mailbox, consider telling the user that other items in their mailbox (not just items in the Recoverable Items folder) might be moved to the archive mailbox. This is because the Default MRM Policy that's assigned to Exchange Online mailboxes contains a retention tag (named Default 2 years move to archive) that moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user. For more information, see [Default Retention Policy in Exchange Online ](https://go.microsoft.com/fwlink/p/?LinkId=746954)</span></span>
    
- <span data-ttu-id="881f9-p117">사용자의 보관 사서함을 사용 하도록 설정한 후에는 해당 보관 사서함의 복구 가능한 항목 폴더에서 삭제 된 항목을 복구할 수 있음을 사용자에 게 알릴 수 있습니다. 보관 사서함에서 **지운** 편지함 폴더를 선택 하 고 **홈** 탭의 **서버에서 지운 편지함 복구** 를 클릭 하 여 Outlook에서이 작업을 수행할 수 있습니다. 삭제 된 항목을 복구 하는 방법에 대 한 자세한 내용은 [Windows 용 Outlook에서 삭제 된 항목 복구](https://go.microsoft.com/fwlink/p/?LinkId=624829)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="881f9-p117">After you enable a user's archive mailbox, you might also tell the user that they can recover deleted items in the Recoverable Items folder in their archive mailbox. They can do this in Outlook by selecting the **Deleted Items** folder in the archive mailbox, and then clicking **Recover Deleted Items from Server** on the **Home** tab. For more information about recovering deleted items, see [Recover deleted items in Outlook for Windows](https://go.microsoft.com/fwlink/p/?LinkId=624829).</span></span> 
