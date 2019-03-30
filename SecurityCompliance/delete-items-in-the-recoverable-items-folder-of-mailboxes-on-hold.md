---
title: 보류에서 클라우드 기반 사서함의 복구 가능한 항목 폴더에 있는 항목 삭제-관리자 도움말
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: '관리자: 해당 사서함이 법적 보존 상태로 설정 된 경우에도 Exchange Online 사서함에 대 한 사용자의 복구 가능한 항목 폴더에서 항목을 삭제 합니다. 이 방법은 실수로 Office 365에 분산 된 데이터를 삭제 하는 효율적인 방법입니다.'
ms.openlocfilehash: 7badd45f582e4d5fef4cb5708c504573da0aba50
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000081"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a><span data-ttu-id="d01ee-104">보류에서 클라우드 기반 사서함의 복구 가능한 항목 폴더에 있는 항목 삭제-관리자 도움말</span><span class="sxs-lookup"><span data-stu-id="d01ee-104">Delete items in the Recoverable Items folder of cloud-based mailboxes on hold - Admin Help</span></span>

<span data-ttu-id="d01ee-105">Exchange Online 사서함에 대 한 복구 가능한 항목 폴더는 실수로 또는 악의적으로 삭제 되는 것을 방지 하기 위해 존재 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-105">The Recoverable Items folder for an Exchange Online mailbox exists to protect from accidental or malicious deletions.</span></span> <span data-ttu-id="d01ee-106">또한 보류 및 eDiscovery 검색과 같은 Office 365 준수 기능에서 유지 하 고 액세스 하는 항목을 저장 하는 데도 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-106">It's also used to store items that are retained and accessed by Office 365 compliance features, such as holds and eDiscovery searches.</span></span> <span data-ttu-id="d01ee-107">그러나 조직에서 삭제 해야 하는 복구 가능한 항목 폴더에 실수로 보존 된 데이터가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-107">However, in some situations organizations might have data that's been unintentionally retained in the Recoverable Items folder that they must delete.</span></span> <span data-ttu-id="d01ee-108">예를 들어 사용자가 중요 한 정보를 포함 하는 전자 메일 메시지를 실수로 보내거나 전달할 수 있으며 비즈니스에 심각한 영향을 줄 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-108">For example, a user might unknowingly send or forward an email message that contains sensitive information or information that may have serious business consequences.</span></span> <span data-ttu-id="d01ee-109">메시지가 영구적으로 삭제 된 경우에도 사서함에 법적 보존이 설정 되어 있기 때문에 무기한 유지 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-109">Even if the message is permanently deleted, it might be retained indefinitely because a legal hold has been placed on the mailbox.</span></span> <span data-ttu-id="d01ee-110">이 시나리오는 데이터가 실수로 Office 365에 분산 되어 있기 때문에 데이터 유출 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-110">This scenario is known as data spillage because data has been unintentionally spilled into Office 365.</span></span> <span data-ttu-id="d01ee-111">이러한 상황에서는 사용자의 복구 가능한 항목 폴더에서 Exchange Online 사서함에 대 한 항목을 삭제할 수 있으며 해당 사서함이 Office 365의 다른 보존 기능 중 하 나와 함께 유지 되는 경우에도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-111">In these situations, you can delete items in a user's Recoverable Items folder for an Exchange Online mailbox, even if that mailbox is placed on hold with one of the different hold features in Office 365.</span></span> <span data-ttu-id="d01ee-112">이러한 유형의 보류에는 소송 보존, 원본 위치 유지, eDiscovery 보류 및 office 365 또는 Microsoft 365의 보안 및 준수 센터에서 만든 office 365 고정 정책이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-112">These types of holds include Litigation Holds, In-Place Holds, eDiscovery holds, and Office 365 retention policies created in the security and compliance center in Office 365 or Microsoft 365.</span></span>
  
 <span data-ttu-id="d01ee-113">이 문서에서는 보류 중인 클라우드 기반 사서함에 대 한 복구 가능한 항목 폴더에서 항목을 삭제 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-113">This article explains how to delete items from the Recoverable Items folder for cloud-based mailboxes that are on hold.</span></span> <span data-ttu-id="d01ee-114">이 절차에서는 사서함에 대 한 액세스를 사용 하지 않도록 설정 하 고 단일 항목 복구를 사용 하지 않도록 설정 하 고 관리 되는 폴더 도우미가 사서함을 처리 하지 않도록 설정한 다음 일시적으로 보류를 제거 하 고 복구 가능한 항목 폴더에서 항목을 삭제 이전 구성으로 사서함을 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-114">This procedure involves disabling access to the mailbox and disabling single item recovery, disabling the Managed Folder Assistant from processing the mailbox, temporarily removing the hold, deleting items from the Recoverable Items folder, and then reverting the mailbox to its previous configuration.</span></span> <span data-ttu-id="d01ee-115">프로세스는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-115">Here's the process:</span></span> 
  
[<span data-ttu-id="d01ee-116">1 단계: 사서함에 대 한 정보 수집</span><span class="sxs-lookup"><span data-stu-id="d01ee-116">Step 1: Collect information about the mailbox</span></span>](#step-1-collect-information-about-the-mailbox)

[<span data-ttu-id="d01ee-117">2 단계: 사서함 준비</span><span class="sxs-lookup"><span data-stu-id="d01ee-117">Step 2: Prepare the mailbox</span></span>](#step-2-prepare-the-mailbox)

[<span data-ttu-id="d01ee-118">3 단계: 사서함에서 모든 보류 제거</span><span class="sxs-lookup"><span data-stu-id="d01ee-118">Step 3: Remove all holds from the mailbox</span></span>](#step-3-remove-all-holds-from-the-mailbox)

[<span data-ttu-id="d01ee-119">4 단계: 사서함에서 지연 된 보류 제거</span><span class="sxs-lookup"><span data-stu-id="d01ee-119">Step 4: Remove the delay hold from the mailbox</span></span>](#step-4-remove-the-delay-hold-from-the-mailbox)

[<span data-ttu-id="d01ee-120">5 단계: 복구 가능한 항목 폴더에서 항목 삭제</span><span class="sxs-lookup"><span data-stu-id="d01ee-120">Step 5: Delete items in the Recoverable Items folder</span></span>](#step-5-delete-items-in-the-recoverable-items-folder)

[<span data-ttu-id="d01ee-121">6 단계: 사서함을 이전 상태로 되돌리기</span><span class="sxs-lookup"><span data-stu-id="d01ee-121">Step 6: Revert the mailbox to its previous state</span></span>](#step-6-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> <span data-ttu-id="d01ee-122">이 문서에서 설명 하는 절차에 따라 Exchange Online 사서함에서 데이터가 영구적으로 삭제 (제거) 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-122">The procedures outlined in this article will result in data being permanently deleted (purged) from an Exchange Online mailbox.</span></span> <span data-ttu-id="d01ee-123">즉, 복구 가능한 항목 폴더에서 삭제 한 메시지는 복구할 수 없으며, 법적 검색 이나 다른 규정 준수 용도로는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-123">That means messages that you delete from the Recoverable Items folder can't be recovered and won't be available for legal discovery or other compliance purposes.</span></span> <span data-ttu-id="d01ee-124">보안 및 준수 센터에서 만든 소송 보존, 원본 위치 유지, eDiscovery 보존 또는 Office 365 보관 정책의 일부로 보존 된 메시지를 삭제 하려면 레코드 관리 또는 법률 부서에 문의 하세요. 보류를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-124">If you want to delete messages from a mailbox that's placed on hold as part of a Litigation Hold, In-Place Hold, eDiscovery hold, or Office 365 retention policy created in the security and compliance center, check with your records management or legal departments before removing the hold.</span></span> <span data-ttu-id="d01ee-125">조직에 보류 중인 사서함 또는 데이터 유출 인시던트가 우선적으로 적용 되는지 여부를 정의 하는 정책이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-125">Your organization might have a policy that defines whether a mailbox on hold or a data spillage incident takes priority.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="d01ee-126">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="d01ee-126">Before you begin</span></span>

- <span data-ttu-id="d01ee-127">5 단계에서 복구 가능한 항목 폴더에서 메시지를 검색 하 고 삭제 하려면 Exchange Online의 다음 관리 역할을 둘 다 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-127">You have to be assigned both of the following management roles in Exchange Online to search for and delete messages from the Recoverable Items folder in Step 5.</span></span>
    
  - <span data-ttu-id="d01ee-128">**사서함 검색** -이 역할을 사용 하 여 조직의 사서함을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-128">**Mailbox Search** - This role lets you to search mailboxes in your organization.</span></span> <span data-ttu-id="d01ee-129">Exchange 관리자에 게는 기본적으로이 역할이 할당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-129">Exchange administrators aren't assigned this role by default.</span></span> <span data-ttu-id="d01ee-130">자신을이 역할에 할당 하려면 자신을 Exchange Online의 검색 관리 역할 그룹의 구성원으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-130">To assign yourself this role, add yourself as a member of the Discovery Management role group in Exchange Online.</span></span> 
    
  - <span data-ttu-id="d01ee-131">**사서함 가져오기 내보내기** -이 역할을 사용 하면 사용자 사서함에서 메시지를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-131">**Mailbox Import Export** - This role lets you to delete messages from a user's mailbox.</span></span> <span data-ttu-id="d01ee-132">기본적으로 이 역할은 역할 그룹에 할당되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-132">By default, this role isn't assigned to any role group.</span></span> <span data-ttu-id="d01ee-133">사용자 사서함에서 메시지를 삭제 하려면 Exchange Online의 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-133">To delete messages from users' mailboxes, you can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> 
    
- <span data-ttu-id="d01ee-134">이 문서에서 설명 하는 절차는 비활성 사서함에서는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-134">The procedure described in this article isn't supported for inactive mailboxes.</span></span> <span data-ttu-id="d01ee-135">이는 제거 후 보류 (또는 Office 365 보존 정책)를 비활성 사서함에 다시 적용할 수 없기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-135">That's because you can't re-apply a hold (or Office 365 retention policy) to an inactive mailbox after you remove it.</span></span> <span data-ttu-id="d01ee-136">비활성 사서함에서 보류를 제거 하면 일시 삭제 된 일반 사서함으로 변경 되 고 관리 되는 폴더 도우미에 의해 처리 된 후 조직에서 영구적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-136">When you remove a hold from an inactive mailbox, it's changed to a normal soft-deleted mailbox and will be permanently deleted from your organization after it's processed by the Managed Folder Assistant.</span></span>
    
- <span data-ttu-id="d01ee-137">보존 잠금으로 잠긴 Office 365 보존 정책에 할당 된 사서함에 대해서는이 절차를 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-137">You can't perform this procedure for a mailbox that has been assigned to an Office 365 retention policy that's been locked with a Preservation Lock.</span></span> <span data-ttu-id="d01ee-138">이는 보존 잠금 때문에 Office 365 보존 정책에서 사서함을 제거 하거나 제외 하 고 사서함에서 관리 되는 폴더 도우미를 사용 하지 않도록 설정할 수 없기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-138">That's because a Preservation Lock prevents you from removing or excluding the mailbox from the Office 365 retention policy and from disabling the Managed Folder Assistant on the mailbox.</span></span> <span data-ttu-id="d01ee-139">보존 정책 잠금에 대 한 자세한 내용은 [잠금 a 보존 정책](retention-policies.md#locking-a-retention-policy)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d01ee-139">For more information about locking retention policies, see [Locking a retention policy](retention-policies.md#locking-a-retention-policy).</span></span>
    
- <span data-ttu-id="d01ee-140">사서함이 보류 되지 않거나 단일 항목 복구를 사용 하도록 설정 되지 않은 경우 복구 가능한 항목 폴더에서 항목을 삭제 하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-140">If a mailbox isn't placed on hold (or doesn't have single item recovery enabled), you can simply delete the items from the Recoverable Items folder.</span></span> <span data-ttu-id="d01ee-141">이 작업을 수행 하는 방법에 대 한 자세한 내용은 [메시지 검색 및 삭제 ](https://go.microsoft.com/fwlink/?linkid=852453)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d01ee-141">For more information about how to do this, see [Search for and delete messages ](https://go.microsoft.com/fwlink/?linkid=852453).</span></span>
  
## <a name="step-1-collect-information-about-the-mailbox"></a><span data-ttu-id="d01ee-142">1 단계: 사서함에 대 한 정보 수집</span><span class="sxs-lookup"><span data-stu-id="d01ee-142">Step 1: Collect information about the mailbox</span></span>

<span data-ttu-id="d01ee-143">첫 번째 단계는이 절차에 영향을 주는 대상 사서함에서 선택한 속성을 수집 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-143">This first step is to collect selected properties from the target mailbox that will affect this procedure.</span></span> <span data-ttu-id="d01ee-144">복구 가능한 항목 폴더에서 항목을 삭제 한 후 이러한 속성 중 일부를 변경 하 고 6 단계에서 원래 값으로 되돌리는 것 이므로 이러한 설정을 기록 하거나 텍스트 파일에 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-144">Be sure to write down these settings or save them to a text file because you'll change some of these properties and then revert back to the original values in Step 6, after you delete items from the Recoverable Items folder.</span></span> <span data-ttu-id="d01ee-145">여기에는 수집 해야 하는 사서함 속성의 목록이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-145">Here's a list of the mailbox properties you need to collect.</span></span>
  
-  <span data-ttu-id="d01ee-146">*singleitemrecoveryenabled* 및 *RetainDeletedItemsFor* ; 필요한 경우 한 번 복구를 사용 하지 않도록 설정 하 고 3 단계에서 삭제 된 항목 보존 기간을 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-146">*SingleItemRecoveryEnabled*  and  *RetainDeletedItemsFor*  ; if necessary, you'll disable single recovery and increase the deleted items retention period in Step 3.</span></span> 
    
-  <span data-ttu-id="d01ee-147">*LitigationHoldEnabled* 및 *InPlaceHolds* 3 단계에서 일시적으로 제거할 수 있도록 사서함에 설정 된 모든 보류를 식별 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-147">*LitigationHoldEnabled*  and  *InPlaceHolds*  ; you need to identify all the holds placed on the mailbox so that you can temporarily remove them in Step 3.</span></span> <span data-ttu-id="d01ee-148">사서함에 저장 될 수 있는 유형 보존을 식별 하는 방법에 대 한 팁을 보려면 [추가 정보](#more-information) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d01ee-148">See the [More information](#more-information) section for tips about how to identify the type hold that might be placed on a mailbox.</span></span> 
    
<span data-ttu-id="d01ee-149">또한 사서함 클라이언트 액세스 설정을 일시적으로 사용 하지 않도록 설정 하 여 소유자 (또는 다른 사용자)가이 절차 중에 사서함에 액세스할 수 없도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-149">Additionally, you need to get the mailbox client access settings so you can temporarily disable them so the owner (or other users) can't access the mailbox during this procedure.</span></span> <span data-ttu-id="d01ee-150">마지막으로 복구 가능한 항목 폴더의 현재 크기 및 항목 수를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-150">Finally, you can get the current size and number of items in the Recoverable Items folder.</span></span> <span data-ttu-id="d01ee-151">5 단계에서 복구 가능한 항목 폴더의 항목을 삭제 한 후에는이 정보를 사용 하 여 항목이 실제로 제거 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-151">After you delete items in the Recoverable Items folder in Step 5, you'll use this information to verify that items were actually removed.</span></span>
  
1. <span data-ttu-id="d01ee-152">[Exchange Online PowerShell에 연결합니다](https://go.microsoft.com/fwlink/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="d01ee-152">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).</span></span> <span data-ttu-id="d01ee-153">Exchange Online에서 적절 한 관리 역할이 할당 된 관리자 계정에 대해 사용자 이름과 암호를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-153">Be sure to use a user name and password for an administrator account that's been assigned the appropriate management roles in Exchange Online.</span></span> 
    
2. <span data-ttu-id="d01ee-154">다음 명령을 실행 하 여 단일 항목 복구 및 삭제 된 항목 보존 기간에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-154">Run the following command to get information about single item recovery and the deleted item retention period.</span></span>

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   <span data-ttu-id="d01ee-155">단일 항목 복구를 사용 하도록 설정 하면 2 단계에서이를 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-155">If single item recovery is enabled, you'll have to disable it in Step 2.</span></span> <span data-ttu-id="d01ee-156">삭제 된 항목 보존 기간이 30 일 (Exchange Online의 최대값)으로 설정 되지 않은 경우 2 단계에서이를 늘릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-156">If the deleted item retention period isn't set for 30 days (the maximum value in Exchange Online), then you can increase it in Step 2.</span></span> 
    
3. <span data-ttu-id="d01ee-157">다음 명령을 실행 하 여 사서함에 대 한 사서함 액세스 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-157">Run the following command to get the mailbox access settings for the mailbox.</span></span> 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   <span data-ttu-id="d01ee-158">2 단계에서 이러한 모든 access 메서드를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-158">You'll disable all of these access methods in Step 2.</span></span>
    
4. <span data-ttu-id="d01ee-159">다음 명령을 실행 하 여 사서함에 적용 된 보류 및 Office 365 보존 정책에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-159">Run the following command to get information about the holds and Office 365 retention policies applied to the mailbox.</span></span>
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > <span data-ttu-id="d01ee-160">*InPlaceHolds* 속성에 값이 너무 많고 이러한 속성이 모두 표시 되지 않는 경우에는 `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` 명령을 실행 하 여 각 값을 별도의 줄에 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-160">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
5. <span data-ttu-id="d01ee-161">다음 명령을 실행 하 여 조직 전체 Office 365 보존 정책에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-161">Run the following command to get information about any organization-wide Office 365 retention policies.</span></span> 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   <span data-ttu-id="d01ee-162">조직에서 조직 차원의 Office 365 보존 정책을 사용 하는 경우에는 3 단계에서 이러한 정책 으로부터 사서함을 제외 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-162">If your organization has any organization-wide Office 365 retention policies, you'll have to exclude the mailbox from these policies in Step 3.</span></span>

   > [!TIP]
    > <span data-ttu-id="d01ee-163">*InPlaceHolds* 속성에 값이 너무 많고 이러한 속성이 모두 표시 되지 않는 경우에는 `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` 명령을 실행 하 여 각 값을 별도의 줄에 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-163">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
6. <span data-ttu-id="d01ee-164">다음 명령을 실행 하 여 사용자의 기본 사서함에 있는 복구할 수 있는 항목 폴더에서 폴더 및 하위 폴더의 현재 크기와 총 항목 수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-164">Run the following command to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="d01ee-165">사용자의 보관 사서함을 사용할 수 있는 경우 다음 명령을 실행 하 여 보관 사서함에서 복구 가능한 항목 폴더의 폴더 및 하위 폴더에 있는 항목의 크기 및 총 수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-165">If the user's archive mailbox is enabled, run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in their archive mailbox.</span></span> 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="d01ee-166">5 단계에서 항목을 삭제 하는 경우 사용자의 기본 보관 사서함에서 복구 가능한 항목 폴더의 항목을 삭제 하거나 삭제 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-166">When you delete items in Step 5, you can choose to delete or not delete items in the Recoverable Items folder in the user's primary archive mailbox.</span></span> <span data-ttu-id="d01ee-167">사서함에 대해 자동 확장 보관을 사용 하도록 설정 된 경우 보조 보관 사서함의 항목은 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-167">Note that if auto-expanding archiving is enabled for the mailbox, items in an auxiliary archive mailbox won't be deleted.</span></span>
  
## <a name="step-2-prepare-the-mailbox"></a><span data-ttu-id="d01ee-168">2 단계: 사서함 준비</span><span class="sxs-lookup"><span data-stu-id="d01ee-168">Step 2: Prepare the mailbox</span></span>

<span data-ttu-id="d01ee-169">사서함에 대 한 정보를 수집 하 고 저장 한 다음에는 다음 작업을 수행 하 여 사서함을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-169">After collecting and saving information about the mailbox, the next step is to prepare the mailbox by performing the following tasks:</span></span> 
  
- <span data-ttu-id="d01ee-170">사서함 소유자가 사서함에 액세스할 수 없도록 사서함에 대 한 **클라이언트 액세스를 사용 하지 않도록 설정** 하 고이 절차 중에 사서함 데이터를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-170">**Disable client access to mailbox** so that the mailbox owner can't access their mailbox and make any changes to the mailbox data during this procedure.</span></span> 
    
- <span data-ttu-id="d01ee-171">**삭제 된 항목 보존 기간** 을 5 단계에서 삭제 하기 전에 복구 가능한 항목 폴더에서 항목을 제거 하지 않도록 최대 30 일 (Exchange Online의 최대값)으로 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-171">**Increase the deleted item retention period** to 30 days (the maximum value in Exchange Online) so that items aren't purged from the Recoverable Items folder before you can delete them in Step 5.</span></span> 
    
- <span data-ttu-id="d01ee-172">5 단계에서 복구 가능한 항목 폴더에서 항목을 삭제 한 후 항목이 보존 되지 않도록 하려면 **단일 항목 복구를 사용 하지 않도록 설정** 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-172">**Disable single Item recovery** so that items won't be retained (for the duration of the deleted item retention period) after you delete them from the Recoverable Items folder in Step 5.</span></span> 
    
- <span data-ttu-id="d01ee-173">사서함을 처리 하지 않고 5 단계에서 삭제 한 항목을 유지 하도록 **관리 되는 폴더 도우미를 사용 하지 않도록 설정 합니다** .</span><span class="sxs-lookup"><span data-stu-id="d01ee-173">**Disable the Managed Folder Assistant** so that it doesn't process the mailbox and retain the items that you delete in Step 5.</span></span> 
    
<span data-ttu-id="d01ee-174">Exchange Online PowerShell에서 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-174">Perform the following steps in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="d01ee-175">다음 명령을 실행 하 여 사서함에 대 한 모든 클라이언트 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-175">Run the following command to disable all client access to the mailbox.</span></span> <span data-ttu-id="d01ee-176">명령 구문에서는 사서함에서 모든 클라이언트 액세스 방법을 사용 하도록 설정 했다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-176">The command syntax assumes that all client access methods were enabled on the mailbox.</span></span>

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > <span data-ttu-id="d01ee-177">사서함에 대 한 모든 클라이언트 액세스 방법을 사용 하지 않도록 설정 하는 데 최대 60 분이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-177">It might take up to 60 minutes to disable all client access methods to the mailbox.</span></span> <span data-ttu-id="d01ee-178">이러한 access 메서드를 사용 하지 않도록 설정 해도 현재 로그인 되어 있는 사서함 소유자와의 연결이 끊어집니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-178">Note that disabling these access methods won't disconnect the mailbox owner they're currently signed in.</span></span> <span data-ttu-id="d01ee-179">소유자가 로그인 되어 있지 않으면 이러한 액세스 방법을 사용 하지 않도록 설정한 후에 사서함에 액세스할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-179">If the owner isn't signed in, then they won't be able to access their mailbox after these access methods are disabled.</span></span> 
  
2. <span data-ttu-id="d01ee-180">다음 명령을 실행 하 여 삭제 된 항목 보존 기간을 최대 30 일로 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-180">Run the following command to increase the deleted item retention period the maximum of 30 days.</span></span> <span data-ttu-id="d01ee-181">이 경우 현재 설정이 30 일 미만인 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-181">This assumes that the current setting is less than 30 days.</span></span> 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. <span data-ttu-id="d01ee-182">다음 명령을 실행 하 여 단일 항목 복구를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-182">Run the following command to disable single item recovery.</span></span>
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > <span data-ttu-id="d01ee-183">단일 항목 복구를 사용 하지 않도록 설정 하는 데 최대 60 분이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-183">It might take up to 60 minutes to disable single item recovery.</span></span> <span data-ttu-id="d01ee-184">이 기간이 경과할 때까지 복구 가능한 항목 폴더의 항목을 삭제 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="d01ee-184">Don't delete items in the Recoverable Items folder until this period has elapsed.</span></span> 
  
4. <span data-ttu-id="d01ee-185">다음 명령을 실행 하 여 관리 되는 폴더 도우미가 사서함을 처리 하지 못하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-185">Run the following command to prevent the Managed Folder Assistant from processing the mailbox.</span></span> <span data-ttu-id="d01ee-186">앞에서 설명한 것 처럼 보존 잠금이 있는 Office 365 보존 정책이 사서함에 적용 되지 않는 경우에만 관리 되는 폴더 도우미를 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-186">As previously explained, you can disable the Managed Folder Assistant only if an Office 365 retention policy with a Preservation Lock is not applied to the mailbox.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a><span data-ttu-id="d01ee-187">3 단계: 사서함에서 모든 보류 제거</span><span class="sxs-lookup"><span data-stu-id="d01ee-187">Step 3: Remove all holds from the mailbox</span></span>

<span data-ttu-id="d01ee-188">복구 가능한 항목 폴더에서 항목을 삭제 하는 마지막 단계는 사서함에 대해 1 단계에서 확인 한 모든 보류를 제거 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-188">The last step before you can delete items from the Recoverable Items folder is to remove all holds (that you identified in Step 1) placed on the mailbox.</span></span> <span data-ttu-id="d01ee-189">복구 가능한 항목 폴더에서 항목을 삭제 한 후에 항목이 보존 되지 않도록 하려면 모든 보존을 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-189">All holds must be removed so that items won't be retained after you delete them from the Recoverable Items folder.</span></span> <span data-ttu-id="d01ee-190">다음 섹션에는 사서함에서 서로 다른 유형의 보류를 제거 하는 방법에 대 한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-190">The following sections contain information about removing different types of holds on a mailbox.</span></span> <span data-ttu-id="d01ee-191">사서함에 저장 될 수 있는 유형 보존을 식별 하는 방법에 대 한 팁을 보려면 [추가 정보](#more-information) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d01ee-191">See the [More information](#more-information) section for tips about how to identify the type hold that might be placed on a mailbox.</span></span> <span data-ttu-id="d01ee-192">자세한 내용은 [Exchange Online 사서함에 대해 설정 된 보류 유형을 식별](identify-a-hold-on-an-exchange-online-mailbox.md)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d01ee-192">For additional information, see [How to identify the type of hold placed on an Exchange Online mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>
  
> [!CAUTION]
> <span data-ttu-id="d01ee-193">앞에서 설명한 것 처럼 사서함에서 보류를 제거 하기 전에 레코드 관리 또는 법률 부서에 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="d01ee-193">As previously stated, check with your records management or legal departments before removing a hold from a mailbox.</span></span> 
  
 ### <a name="litigation-hold"></a><span data-ttu-id="d01ee-194">소송 대기</span><span class="sxs-lookup"><span data-stu-id="d01ee-194">Litigation Hold</span></span>
  
<span data-ttu-id="d01ee-195">Exchange Online PowerShell에서 다음 명령을 실행 하 여 사서함에서 소송 보존을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-195">Run the following command in Exchange Online PowerShell to remove a Litigation Hold from the mailbox.</span></span>

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> <span data-ttu-id="d01ee-196">클라이언트 액세스 방법 및 단일 항목 복구를 사용 하지 않도록 설정 하는 것과 마찬가지로 소송 보존을 제거 하는 데 최대 60 분이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-196">Similar to disabling the client access methods and single item recovery, it might take up to 60 minutes to remove the Litigation Hold.</span></span> <span data-ttu-id="d01ee-197">이 기간이 경과할 때까지 복구 가능한 항목 폴더에서 항목을 삭제 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="d01ee-197">Don't delete items from the Recoverable Items folder until this period has elapsed.</span></span> 
  
 ### <a name="in-place-hold"></a><span data-ttu-id="d01ee-198">원본 위치 유지</span><span class="sxs-lookup"><span data-stu-id="d01ee-198">In-Place Hold</span></span>
  
<span data-ttu-id="d01ee-199">Exchange Online PowerShell에서 다음 명령을 실행 하 여 사서함에 배치 된 원본 위치 유지를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-199">Run the following command in Exchange Online PowerShell to identify the In-Place Hold that's placed on the mailbox.</span></span> <span data-ttu-id="d01ee-200">1 단계에서 확인 한 원본 위치 유지에 대해 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-200">Use the GUID for the In-Place Hold that you identified in Step 1.</span></span> 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
<span data-ttu-id="d01ee-201">원본 위치 유지를 확인 한 후 EAC (exchange 관리 센터) 또는 exchange Online PowerShell을 사용 하 여 보류에서 사서함을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-201">After you identify the In-Place Hold, you can use the Exchange admin center (EAC) or Exchange Online PowerShell to remove the mailbox from the hold.</span></span> <span data-ttu-id="d01ee-202">자세한 내용은 [만들기 또는 In-place Hold 제거](https://go.microsoft.com/fwlink/?linkid=852668) 항목을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="d01ee-202">For more information, see [Create or remove an In-Place Hold](https://go.microsoft.com/fwlink/?linkid=852668).</span></span>
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a><span data-ttu-id="d01ee-203">특정 사서함에 적용 되는 Office 365 보존 정책</span><span class="sxs-lookup"><span data-stu-id="d01ee-203">Office 365 retention policies applied to specific mailboxes</span></span>
  
<span data-ttu-id="d01ee-204">[Security & 준수 센터 PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) 에서 다음 명령을 실행 하 여 사서함에 적용 되는 Office 365 보존 정책을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-204">Run the following command in [Security & Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the Office 365 retention policy that is applied to the mailbox.</span></span> <span data-ttu-id="d01ee-205">1 단계에서 확인 한 보존 정책 `mbx` 에 `skp` 대해 또는 접두사를 제외 하 고 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-205">Use the GUID (not including the  `mbx` or  `skp` prefix) for the retention policy that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
<span data-ttu-id="d01ee-206">보존 정책을 식별 한 후 Security & 준수 센터의 **날짜 관리** \> **보존** 페이지로 이동 하 고, 이전 단계에서 식별 한 보존 정책을 편집 하 고, 다음 목록에서 사서함을 제거 합니다. 보존 정책에 포함 된 받는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-206">After you identify the retention policy, go to the **Date governance** \> **Retention** page in the Security & Compliance Center, edit the retention policy that you identified in the previous step, and remove the mailbox from the list of recipients that are included in the retention policy.</span></span> 
  
 ### <a name="organization-wide-office-365-retention-policies"></a><span data-ttu-id="d01ee-207">조직 전체 Office 365 보존 정책</span><span class="sxs-lookup"><span data-stu-id="d01ee-207">Organization-wide Office 365 retention policies</span></span>
  
<span data-ttu-id="d01ee-208">조직 전체 및 Exchange 전체 Office 365 보존 정책은 조직의 모든 사서함에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-208">Organization-wide and Exchange-wide Office 365 retention policies are applied to every mailbox in the organization.</span></span> <span data-ttu-id="d01ee-209">이러한 사용자는 조직 수준 (사서함 수준이 아님)에서 적용 되며 1 단계에서 **set-organizationconfig** cmdlet을 실행 하면 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-209">They are applied at the organization level (not the mailbox level) and are returned when you run the **Get-OrganizationConfig** cmdlet in Step 1.</span></span> <span data-ttu-id="d01ee-210">[Security & 준수 센터 PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) 에서 다음 명령을 실행 하 여 조직 전반의 Office 365 보존 정책을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-210">Run the following command in [Security & Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the organization-wide Office 365 retention policies.</span></span> <span data-ttu-id="d01ee-211">1 단계에서 확인 한 조직 차원의 `mbx` 보존 정책에 대해 접두사를 제외한 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-211">Use the GUID (not including the  `mbx` prefix) for the organization-wide retention policies that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

<span data-ttu-id="d01ee-212">조직 전반의 Office 365 보존 정책을 파악 한 후에는 Security & 준수 센터의 **날짜 관리** \> **보존** 페이지로 이동 하 고,에서 식별 한 각 조직 차원의 보존 정책을 편집 합니다. 이전 단계를 진행 하 고 제외 된 받는 사람 목록에 사서함을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-212">After you identify the organization-wide Office 365 retention policies, go to the **Date governance** \> **Retention** page in the Security & Compliance Center, edit each organization-wide retention policy that you identified in the previous step, and add the mailbox to the list of excluded recipients.</span></span> <span data-ttu-id="d01ee-213">이렇게 하면 보존 정책에서 사용자의 사서함이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-213">Doing this will remove the user's mailbox from the retention policy.</span></span> 

### <a name="office-365-retention-labels"></a><span data-ttu-id="d01ee-214">Office 365 보존 레이블</span><span class="sxs-lookup"><span data-stu-id="d01ee-214">Office 365 retention labels</span></span>

<span data-ttu-id="d01ee-215">사용자가 콘텐츠를 보존 하도록 구성 된 레이블을 적용할 때마다 해당 사서함의 폴더 또는 항목에 대 한 콘텐츠를 보존 하 고 삭제 하려면 *ComplianceTagHoldApplied* mailbox 속성을 **True**로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-215">Whenever a user applies a label that's configured to retain content or retain and then delete content to any folder or item in their mailbox, the *ComplianceTagHoldApplied* mailbox property is set to **True**.</span></span> <span data-ttu-id="d01ee-216">이 문제가 발생 하는 경우 사서함은 소송 보존에 적용 된 것으로 간주 되거나 Office 365 보관 정책에 할당 되는 것 처럼 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-216">When this happens, the mailbox is considered to be on hold, just as if it was placed on Litigation Hold or assigned to an Office 365 retention policy.</span></span>

<span data-ttu-id="d01ee-217">*ComplianceTagHoldApplied* 속성의 값을 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-217">To view the value of the *ComplianceTagHoldApplied* property, run the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

<span data-ttu-id="d01ee-218">폴더 또는 항목에 보존 레이블이 적용 되므로 사서함이 보류 중인 것을 확인 한 후에는 보안 및 준수 센터의 콘텐츠 검색 도구를 사용 하 여 new-compliancetag 검색 조건을 사용 하 여 레이블이 지정 된 항목을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-218">After you've identified that a mailbox is on hold because a retention label is applied to a folder or item, you can use the Content Search tool in the security and compliance center to search for labeled items by using the ComplianceTag search condition.</span></span> <span data-ttu-id="d01ee-219">자세한 내용은 [키워드 쿼리 및 검색 조건에서 콘텐츠 검색에 대 한](keyword-queries-and-search-conditions.md#conditions-for-common-properties)"검색 조건" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d01ee-219">For more information, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md#conditions-for-common-properties).</span></span>

<span data-ttu-id="d01ee-220">레이블에 대 한 자세한 내용은 Overview in [Office 365 labels](labels.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d01ee-220">For more information about labels, see [Overview of Office 365 labels](labels.md).</span></span>

 ### <a name="ediscovery-case-holds"></a><span data-ttu-id="d01ee-221">eDiscovery 사례 보류</span><span class="sxs-lookup"><span data-stu-id="d01ee-221">eDiscovery case holds</span></span>
  
<span data-ttu-id="d01ee-222">[Security & 준수 센터 PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) 에서 다음 명령을 실행 하 여 사서함에 적용 된 eDiscovery 사례와 관련 된 보류를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-222">Run the following commands in [Security & Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the hold associated with an eDiscovery case that's applied to the mailbox.</span></span> <span data-ttu-id="d01ee-223">1 단계에서 확인 한 eDiscovery 보존 `UniH` 에 대 한 GUID (접두사를 포함 하지 않음)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-223">Use the GUID (not including the  `UniH` prefix) for the eDiscovery hold that you identified in Step 1.</span></span> <span data-ttu-id="d01ee-224">두 번째 명령은 보류가 연결 된 eDiscovery 사례의 이름을 표시 합니다. 세 번째 명령은 보류의 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-224">Note that the second command displays the name of the eDiscovery case the hold is associated with; the third command displays the name of the hold.</span></span> 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

<span data-ttu-id="d01ee-225">ediscovery 사례 및 보류의 이름을 식별 한 후에는 준수 센터의 **ediscovery** \> **ediscovery** 페이지로 이동 하 고 케이스를 연 다음 보류에서 사서함을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-225">After you've identified the name of the eDiscovery case and the hold, go to the **eDiscovery** \> **eDiscovery** page in the compliance center, open the case, and remove the mailbox from the hold.</span></span> <span data-ttu-id="d01ee-226">자세한 내용은 [eDiscovery 사례](ediscovery-cases.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d01ee-226">For more information, see [eDiscovery cases](ediscovery-cases.md).</span></span>
  
## <a name="step-4-remove-the-delay-hold-from-the-mailbox"></a><span data-ttu-id="d01ee-227">4 단계: 사서함에서 지연 된 보류 제거</span><span class="sxs-lookup"><span data-stu-id="d01ee-227">Step 4: Remove the delay hold from the mailbox</span></span>

<span data-ttu-id="d01ee-228">사서함에서 모든 유형의 보류가 제거 된 후에는 *DelayHoldApplied* mailbox 속성의 값이 **True**로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-228">After any type of hold is removed from a mailbox, the value of the *DelayHoldApplied* mailbox property is set to **True**.</span></span> <span data-ttu-id="d01ee-229">다음 번에 관리 되는 폴더 도우미가 사서함을 처리 하 고 보류가 제거 되었음을 감지할 때 이러한 상황이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-229">This occurs the next time the Managed Folder Assistant processes the mailbox and detects that a hold has been removed.</span></span> <span data-ttu-id="d01ee-230">이를 *지연 보존* 이라고 하며, 데이터가 사서함에서 영구적으로 삭제 되는 것을 방지 하기 위해 보류의 실제 제거가 30 일 동안 지연 되는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-230">This is called a *delay hold* and means the actual removal of the hold is delayed for 30 days to prevent data from being permanently deleted from the mailbox.</span></span> <span data-ttu-id="d01ee-231">지연 보존의 목적은 관리자가 보류를 제거한 후 삭제 될 사서함 항목을 검색 하거나 복구할 수 있도록 하는 것입니다.  사서함에 연기 대기를 설정 하면 사서함이 소송 보존 상태에 있는 것 처럼 여전히 무제한 기간 동안 유지 되는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-231">(The purpose of a delay hold is to give admins an opportunity to search for or recover mailbox items that will be purged after a hold is removed.)  When a delay hold is placed on the mailbox, the mailbox is still considered to be on hold for an unlimited duration, as if the mailbox was on Litigation Hold.</span></span> <span data-ttu-id="d01ee-232">30 일 후에 지연 보류가 만료 되 고 Office 365에서 자동으로 지연 대기 ( *DelayHoldApplied* 속성을 **False**로 설정)을 제거 하 여 보류를 실제로 제거 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-232">After 30 days, the delay hold expires, and Office 365 will automatically attempt to remove the delay hold (by setting the *DelayHoldApplied* property to **False**) so that the hold is actually removed.</span></span> 

<span data-ttu-id="d01ee-233">5 단계에서 항목을 삭제 하려면 먼저 사서함에서 지연 유지를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-233">Before you can delete items in Step 5, you have to remove the delay hold from the mailbox.</span></span> <span data-ttu-id="d01ee-234">먼저 Exchange Online PowerShell에서 다음 명령을 실행 하 여 지연 보류가 사서함에 적용 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-234">First, determine if the delay hold is applied to the mailbox by running the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox <username> | FL DelayHoldApplied
```

<span data-ttu-id="d01ee-235">*DelayHoldApplied* 속성 값을 **False**로 설정 하면 대기 시간이 사서함에 저장 되지 않은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-235">If the value of the *DelayHoldApplied* property is set to **False**, a delay hold has not been placed on the mailbox.</span></span> <span data-ttu-id="d01ee-236">5 단계까지 이동 하 여 복구 가능한 항목 폴더의 항목을 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-236">You can go to Step 5 and delete items in the Recoverable Items folder.</span></span>

<span data-ttu-id="d01ee-237">*DelayHoldApplied* 속성 값이 **True**로 설정 된 경우 다음 명령을 실행 하 여 지연 보존을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-237">If the value of the *DelayHoldApplied* property is set to **True**, run the following command to remove the delay hold:</span></span>

```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
<span data-ttu-id="d01ee-238">*RemoveDelayHoldApplied* 매개 변수를 사용 하려면 Exchange Online의 법적 보존 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-238">Note that you must be assigned the Legal Hold role in Exchange Online to use the *RemoveDelayHoldApplied* parameter.</span></span>

## <a name="step-5-delete-items-in-the-recoverable-items-folder"></a><span data-ttu-id="d01ee-239">5 단계: 복구 가능한 항목 폴더에서 항목 삭제</span><span class="sxs-lookup"><span data-stu-id="d01ee-239">Step 5: Delete items in the Recoverable Items folder</span></span>

<span data-ttu-id="d01ee-240">이제 Exchange Online PowerShell의 [검색 사서함](https://go.microsoft.com/fwlink/?linkid=852595) cmdlet을 사용 하 여 복구 가능한 항목 폴더의 항목을 실제로 삭제할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-240">Now you're ready to actually delete items in the Recoverable Items folder by using the [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) cmdlet in Exchange Online PowerShell.</span></span> <span data-ttu-id="d01ee-241">**검색 사서함** cmdlet을 실행할 때는 다음과 같은 세 가지 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-241">You have three options when running the **Search-Mailbox** cmdlet.</span></span> 
  
- <span data-ttu-id="d01ee-242">삭제 하기 전에 대상 사서함에 항목을 복사 하 여 필요한 경우 항목을 검토 한 다음 삭제할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-242">Copy items to a target mailbox before you delete them so that you can review the items, if necessary, before you delete them.</span></span>
    
- <span data-ttu-id="d01ee-243">항목을 대상 사서함으로 복사 하 고 같은 명령에서 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-243">Copy items to a target mailbox and delete them in the same command.</span></span>
    
- <span data-ttu-id="d01ee-244">항목을 대상 사서함에 복사 하지 않고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-244">Delete items without copying them to a target mailbox.</span></span> 
    
<span data-ttu-id="d01ee-245">**검색 사서함** cmdlet을 실행 하면 사용자의 기본 보관 사서함에 있는 복구 가능한 항목 폴더의 항목도 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-245">Note that items in the Recoverable Items folder in the user's primary archive mailbox will also be deleted when you run the **Search-Mailbox** cmdlet.</span></span> <span data-ttu-id="d01ee-246">이를 방지 하기 위해 *만드는 경우 donotincludearchive* 스위치를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-246">To prevent this, you can include the  *DoNotIncludeArchive*  switch.</span></span> <span data-ttu-id="d01ee-247">앞에서 설명한 것 처럼 사서함에 대해 자동 확장 보관을 사용 하도록 설정 된 경우 \* \* 검색 사서함 \* \* cmdlet은 보조 보관 사서함의 항목을 삭제 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-247">And as previously stated, if auto-expanding archiving is enabled for the mailbox, the \*\* Search-Mailbox \*\* cmdlet doesn't deleted items in an auxiliary archive mailbox.</span></span> <span data-ttu-id="d01ee-248">자동 확장 보관에 대 한 자세한 내용은 [Office 365의 무제한 보관 개요](unlimited-archiving.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d01ee-248">For more information about auto-expanding archive, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="d01ee-249">*searchquery* 매개 변수를 사용 하 여 검색 쿼리를 포함 하는 경우 검색 **사서함** cmdlet은 최대 1만 개의 항목을 검색 결과에 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-249">If you include a search query (by using the  *SearchQuery*  parameter), the **Search-Mailbox** cmdlet will return a maximum of 10,000 items in the search results.</span></span> <span data-ttu-id="d01ee-250">따라서 검색 쿼리를 포함 하는 경우 1만 개 보다 많은 항목을 삭제 하려면 **검색 사서함** 명령을 여러 번 실행 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-250">Therefore if you include a search query, you might have to run the **Search-Mailbox** command multiple times to delete more than 10,000 items.</span></span> 
  
<span data-ttu-id="d01ee-251">다음 예제에는 이러한 각 옵션에 대 한 명령 구문이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-251">The following examples show the command syntax for each of these options.</span></span> <span data-ttu-id="d01ee-252">다음은 `-SearchQuery size>0` 복구 가능한 항목 폴더의 모든 하위 폴더에서 모든 항목을 삭제 하는 매개 변수 값을 사용 하는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-252">These examples use the  `-SearchQuery size>0` parameter value, which deletes all items from all subfolders in the Recoverable Items folder.</span></span> <span data-ttu-id="d01ee-253">특정 조건과 일치 하는 항목만 삭제 해야 하는 경우에는 *searchquery* 매개 변수를 사용 하 여 메시지 제목 또는 날짜 범위와 같은 다른 조건을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-253">If you need to delete only items that match specific conditions, you can also use the  *SearchQuery*  parameter to specify other conditions, such as the subject of a message or a date range.</span></span> <span data-ttu-id="d01ee-254">아래에서 [searchquery 매개 변수를 사용 하는 다른 예](#other-examples-of-using-the-searchquery-parameter) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d01ee-254">See the [other examples of using the SearchQuery parameter](#other-examples-of-using-the-searchquery-parameter) below.</span></span> 
  
### <a name="example-1"></a><span data-ttu-id="d01ee-255">예 1</span><span class="sxs-lookup"><span data-stu-id="d01ee-255">Example 1</span></span>

<span data-ttu-id="d01ee-256">이 예에서는 사용자의 복구할 수 있는 항목 폴더에 있는 모든 항목을 조직의 검색 사서함에 있는 폴더로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-256">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox.</span></span> <span data-ttu-id="d01ee-257">이렇게 하면 항목을 영구적으로 삭제 하기 전에 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-257">This lets you review the items before you permanently delete them.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

<span data-ttu-id="d01ee-258">이전 예제에서는 항목을 검색 검색 사서함에 복사할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-258">In the previous example, it isn't required to copy items to the Discovery Search Mailbox.</span></span> <span data-ttu-id="d01ee-259">모든 대상 사서함에 메시지를 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-259">You can copy messages to any target mailbox.</span></span> <span data-ttu-id="d01ee-260">그러나 중요 한 사서함 데이터에 대 한 액세스를 방지 하려면 액세스 권한이 있는 개인만 액세스할 수 있는 사서함으로 메시지를 복사 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-260">However, to prevent access to potentially sensitive mailbox data, we recommend copying messages to a mailbox that has access restricted to authorized personnel.</span></span> <span data-ttu-id="d01ee-261">기본적으로 Exchange Online의 검색 관리 역할 그룹 구성원에 게는 기본 검색 사서함에 대 한 액세스가 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-261">By default, access to the default Discovery Search Mailbox is restricted to members of the Discovery Management role group in Exchange Online.</span></span> 
  
### <a name="example-2"></a><span data-ttu-id="d01ee-262">예 2</span><span class="sxs-lookup"><span data-stu-id="d01ee-262">Example 2</span></span>

<span data-ttu-id="d01ee-263">이 예에서는 복구 가능한 항목 폴더의 모든 항목을 조직의 검색 사서함에 있는 폴더로 복사한 다음 사용자의 복구 가능한 항목 폴더에서 해당 항목을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-263">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox and then deletes the items from the user's Recoverable Items folder.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a><span data-ttu-id="d01ee-264">예제 3</span><span class="sxs-lookup"><span data-stu-id="d01ee-264">Example 3</span></span>

<span data-ttu-id="d01ee-265">이 예에서는 사용자의 복구 가능한 항목 폴더에서 대상 사서함으로 복사 하지 않고 모든 항목을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-265">This example deletes all items in the user's Recoverable Items folder, without copying them to a target mailbox.</span></span> 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a><span data-ttu-id="d01ee-266">searchquery 매개 변수를 사용 하는 다른 예</span><span class="sxs-lookup"><span data-stu-id="d01ee-266">Other examples of using the SearchQuery parameter</span></span>

<span data-ttu-id="d01ee-267">다음은 *searchquery* 매개 변수를 사용 하 여 특정 메시지를 찾는 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-267">Here are a few examples of using the  *SearchQuery*  parameter to find specific messages.</span></span> <span data-ttu-id="d01ee-268">*searchquery* 매개 변수를 사용 하 여 특정 항목을 검색 하는 경우 검색 결과를 검토 한 다음 검색 결과를 삭제 하기 전에 필요한 경우 쿼리를 수정할 수 있도록 결과를 대상 사서함으로 복사 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-268">If you use the  *SearchQuery*  parameter to search for specific items, consider copying the search results to a target mailbox so that you can review the search results and then revise the query if necessary before you delete the results of a search.</span></span> 
  
<span data-ttu-id="d01ee-269">다음은 제목 필드에 특정 구를 포함 하는 메시지를 반환 하는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-269">This example returns messages that contain a specific phrase in the Subject field.</span></span>
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

<span data-ttu-id="d01ee-270">이 예에서는 지정 된 날짜 범위 내에 전송 된 메시지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-270">This example returns messages that were sent within the specified date range.</span></span>
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
<span data-ttu-id="d01ee-271">이 예제에서는 지정 된 사람에 게 전송 된 메시지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-271">This example returns messages that were sent to the specified person.</span></span>

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a><span data-ttu-id="d01ee-272">항목이 삭제 되었는지 확인</span><span class="sxs-lookup"><span data-stu-id="d01ee-272">Verify that items were deleted</span></span>

<span data-ttu-id="d01ee-273">사서함의 복구할 수 있는 항목 폴더에서 항목이 삭제 되었는지 확인 하려면 Exchange Online PowerShell에서 **get-mailboxfolderstatistics** cmdlet을 사용 하 여 복구 가능한 항목 폴더의 항목 크기 및 수를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-273">To verify that you've successfully deleted items from the Recoverable Items folder of a mailbox, use **Get-MailboxFolderStatistics** cmdlet in Exchange Online PowerShell to check the size and number of items in Recoverable Items folder.</span></span> <span data-ttu-id="d01ee-274">이러한 통계를 1 단계에서 수집한 것과 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-274">You can compare these statistics with the ones you collected in Step 1.</span></span> 
  
<span data-ttu-id="d01ee-275">에서 다음 명령을 실행 하 여 사용자의 기본 사서함에 있는 복구할 수 있는 항목 폴더에서 폴더 및 하위 폴더의 현재 크기와 총 항목 수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-275">Run the following command in to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
<span data-ttu-id="d01ee-276">다음 명령을 실행 하 여 사용자의 보관 사서함에 있는 복구 가능한 항목 폴더의 폴더 및 하위 폴더에 있는 항목의 크기 및 총 수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-276">Run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in the user's archive mailbox.</span></span> 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-6-revert-the-mailbox-to-its-previous-state"></a><span data-ttu-id="d01ee-277">6 단계: 사서함을 이전 상태로 되돌리기</span><span class="sxs-lookup"><span data-stu-id="d01ee-277">Step 6: Revert the mailbox to its previous state</span></span>

<span data-ttu-id="d01ee-278">마지막 단계는 사서함을 다시 이전 구성으로 되돌리는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-278">The final step is to revert the mailbox back to its previous configuration.</span></span> <span data-ttu-id="d01ee-279">즉, 2 단계에서 변경한 속성을 다시 설정 하 고 3 단계에서 제거한 보존을 다시 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-279">This means resetting the properties that you changed in Step 2 and re-applying the holds that you removed in Step 3.</span></span> <span data-ttu-id="d01ee-280">성능 저하를 줄여주는 방법에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-280">This includes:</span></span>
  
- <span data-ttu-id="d01ee-281">삭제 된 항목 보존 기간을 이전 값으로 변경</span><span class="sxs-lookup"><span data-stu-id="d01ee-281">Changing the deleted item retention period back to its previous value.</span></span> <span data-ttu-id="d01ee-282">또는 Exchange Online에서이 설정을 최대 30 일로 그대로 두면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-282">Alternatively, you can just leave this set to 30 days, the maximum value in Exchange Online.</span></span>
    
- <span data-ttu-id="d01ee-283">단일 항목 복구를 다시 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-283">Re-enabling single Item recovery.</span></span>
    
- <span data-ttu-id="d01ee-284">소유자가 자신의 사서함에 액세스할 수 있도록 클라이언트 액세스 방법을 다시 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-284">Re-enabling the client access methods so that the owner can access their mailbox.</span></span>
    
- <span data-ttu-id="d01ee-285">제거한 보류 및 Office 365 보존 정책을 다시 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-285">Re-applying the holds and Office 365 retention policies that you removed.</span></span>
    
- <span data-ttu-id="d01ee-286">관리 되는 폴더 도우미가 사서함을 처리할 수 있도록 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-286">Re-enabling the Managed Folder Assistant to process the mailbox.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="d01ee-287">관리 되는 폴더 도우미가 사서함을 처리 하도록 다시 설정 하기 전에 보류 또는 Office 365 보존 정책을 다시 적용 하 고 현재 위치에 있는지 확인 한 후 24 시간을 기다리는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-287">We recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant to process the mailbox.</span></span> 
  
<span data-ttu-id="d01ee-288">Exchange Online PowerShell에서 지정 된 순서 대로 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-288">Perform the following steps (in the specified sequence) in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="d01ee-289">다음 명령을 실행 하 여 삭제 된 항목 보존 기간을 원래 값으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-289">Run the following command to change the deleted item retention period back to its original value.</span></span> <span data-ttu-id="d01ee-290">이는 이전 설정이 30 일 보다 작은 것으로 가정 합니다. 예: 14 일</span><span class="sxs-lookup"><span data-stu-id="d01ee-290">This assumes that the previous setting is less than 30 days; for example 14 days.</span></span> 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. <span data-ttu-id="d01ee-291">다음 명령을 실행 하 여 단일 항목 복구를 다시 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-291">Run the following command to re-enable single item recovery.</span></span>
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. <span data-ttu-id="d01ee-292">다음 명령을 실행 하 여 사서함에 대 한 모든 클라이언트 액세스 방법을 다시 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-292">Run the following command to re-enable all client access methods to the mailbox.</span></span>
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. <span data-ttu-id="d01ee-293">3 단계에서 제거한 보존을 다시 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-293">Re-apply the holds that you removed in Step 3.</span></span> <span data-ttu-id="d01ee-294">보존 유형에 따라 다음 절차 중 하나를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-294">Depending on the type of hold, use one of the following procedures.</span></span>
    
    <span data-ttu-id="d01ee-295">**소송 대기**</span><span class="sxs-lookup"><span data-stu-id="d01ee-295">**Litigation Hold**</span></span>
    
    <span data-ttu-id="d01ee-296">다음 명령을 실행 하 여 사서함에 대 한 소송 보존을 다시 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-296">Run the following command to re-enable a Litigation Hold for the mailbox.</span></span>
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    <span data-ttu-id="d01ee-297">**원본 위치 유지**</span><span class="sxs-lookup"><span data-stu-id="d01ee-297">**In-Place Hold**</span></span>
    
    <span data-ttu-id="d01ee-298">EAC (또는 Exchange Online PowerShell)를 사용 하 여 사서함을 원본 위치 유지 상태로 다시 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-298">Use the EAC (or Exchange Online PowerShell) to add the mailbox back to the In-Place Hold.</span></span> 
    
    <span data-ttu-id="d01ee-299">**특정 사서함에 적용 되는 Office 365 보존 정책**</span><span class="sxs-lookup"><span data-stu-id="d01ee-299">**Office 365 retention policies applied to specific mailboxes**</span></span>
    
    <span data-ttu-id="d01ee-300">보안 & 준수 센터를 사용 하 여 사서함을 보존 정책에 다시 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-300">Use the Security & Compliance Center to add the mailbox back to the retention policy.</span></span> <span data-ttu-id="d01ee-301">Security & 준수 센터의 **날짜 관리** \> **보존** 페이지로 이동 하 여 보존 정책을 편집한 후 보존 정책이 적용 되는 받는 사람 목록에 사서함을 다시 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-301">Go to the **Date governance** \> **Retention** page in the Security & Compliance Center, edit the retention policy, and add the mailbox back to the list of recipients that the retention policy is applied to.</span></span> 
    
    <span data-ttu-id="d01ee-302">**조직 전체 Office 365 보존 정책**</span><span class="sxs-lookup"><span data-stu-id="d01ee-302">**Organization-wide Office 365 retention policies**</span></span>
    
    <span data-ttu-id="d01ee-303">정책에서 조직 전체 또는 Exchange 전체 보존 정책을 제거한 경우에는 Security & 준수 센터를 사용 하 여 제외 된 사용자 목록에서 해당 사서함을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-303">If you removed an organization-wide or Exchange-wide retention policy by excluding it from the policy, then use the Security & Compliance Center to remove the mailbox from the list of excluded users.</span></span> <span data-ttu-id="d01ee-304">Security & 준수 센터의 **날짜 거 버 넌 스** \> **보존** 페이지로 이동 하 여 조직 차원의 보존 정책을 편집 하 고 제외 된 받는 사람 목록에서 사서함을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-304">Go to the **Date governance** \> **Retention** page in the Security & Compliance Center, edit the organization-wide retention policy, and remove the mailbox from the list of excluded recipients.</span></span> <span data-ttu-id="d01ee-305">이렇게 하면 보존 정책이 사용자 사서함에 다시 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-305">Doing this will re-apply the retention policy to the user's mailbox.</span></span> 
    
    <span data-ttu-id="d01ee-306">**eDiscovery 사례 보류**</span><span class="sxs-lookup"><span data-stu-id="d01ee-306">**eDiscovery case holds**</span></span>
    
    <span data-ttu-id="d01ee-307">보안 & 준수 센터를 사용 하면 eDiscovery 사례와 연결 된 보류를 다시 사서함에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-307">Use the Security & Compliance Center to add the mailbox back the hold that's associated with an eDiscovery case.</span></span> <span data-ttu-id="d01ee-308">**ediscovery** \> **ediscovery** 페이지로 이동 하 여 사례를 열고 사서함을 다시 보류에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-308">Go to the **eDiscovery** \> **eDiscovery** page, open the case, and add the mailbox back to the hold.</span></span> 
    
5. <span data-ttu-id="d01ee-309">다음 명령을 실행 하 여 관리 되는 폴더 도우미가 사서함을 다시 처리할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-309">Run the following command to allow the Managed Folder Assistant to process the mailbox again.</span></span> <span data-ttu-id="d01ee-310">앞에서 설명한 것 처럼 관리 되는 폴더 도우미를 다시 사용 하도록 설정 하기 전에 보류 또는 Office 365 보존 정책을 다시 적용 하 고 현재 위치에 있는지 확인 한 후 24 시간을 기다리는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-310">As previously stated, we recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. <span data-ttu-id="d01ee-311">사서함이 이전 구성으로 되돌아간 것을 확인 하려면 다음 명령을 실행 하 여 1 단계에서 수집한 설정과 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-311">To verify that the mailbox has been reverted back to its previous configuration, you can run the following commands and then compare the settings to the ones that you collected in Step 1.</span></span>

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a><span data-ttu-id="d01ee-312">추가 정보</span><span class="sxs-lookup"><span data-stu-id="d01ee-312">More information</span></span>

<span data-ttu-id="d01ee-313">다음은 *InPlaceHolds* 속성의 값에 따라 **get-Mailbox** 또는 **set-organizationconfig** cmdlet을 실행할 때 서로 다른 유형의 보류를 식별 하는 방법을 설명 하는 표입니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-313">Here's a table that describes how to identify different types of holds based on the values in the  *InPlaceHolds*  property when you run the **Get-Mailbox** or **Get-OrganizationConfig** cmdlets.</span></span> <span data-ttu-id="d01ee-314">자세한 내용은 [Exchange Online 사서함에 대해 설정 된 보류 유형을 식별](identify-a-hold-on-an-exchange-online-mailbox.md)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d01ee-314">For more detailed information, see [How to identify the type of hold placed on an Exchange Online mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>

<span data-ttu-id="d01ee-315">앞에서 설명한 것 처럼 복구 가능한 항목 폴더의 항목을 성공적으로 삭제 하려면 먼저 사서함에서 모든 보류 및 Office 365 보존 정책을 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-315">As previously explained, you have to remove all holds and Office 365 retention policies from a mailbox before you can successfully delete items in the Recoverable Items folder.</span></span> 
  
|<span data-ttu-id="d01ee-316">**보류 유형**</span><span class="sxs-lookup"><span data-stu-id="d01ee-316">**Hold type**</span></span>|<span data-ttu-id="d01ee-317">**예제 값**</span><span class="sxs-lookup"><span data-stu-id="d01ee-317">**Example value**</span></span>|<span data-ttu-id="d01ee-318">**보류를 확인 하는 방법**</span><span class="sxs-lookup"><span data-stu-id="d01ee-318">**How to identify the hold**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d01ee-319">소송 대기</span><span class="sxs-lookup"><span data-stu-id="d01ee-319">Litigation Hold</span></span>  <br/> | `True` <br/> |<span data-ttu-id="d01ee-320">*LitigationHoldEnabled* 속성은로 `True`설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-320">The  *LitigationHoldEnabled*  property is set to  `True`.</span></span>  <br/> |
|<span data-ttu-id="d01ee-321">원본 위치 유지</span><span class="sxs-lookup"><span data-stu-id="d01ee-321">In-Place Hold</span></span>  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |<span data-ttu-id="d01ee-322">*InPlaceHolds* 속성은 사서함에 배치 된 원본 위치 유지의 GUID를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-322">The  *InPlaceHolds*  property contains the GUID of the In-Place Hold that's placed on the mailbox.</span></span> <span data-ttu-id="d01ee-323">GUID가 접두사로 시작 되지 않으므로 현재 위치 유지로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-323">You can tell this is an In-Place Hold because the GUID doesn't start with a prefix.</span></span>  <br/> <span data-ttu-id="d01ee-324">Exchange Online PowerShell의 `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` 명령을 사용 하 여 사서함의 원본 위치 유지에 대 한 정보를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-324">You can use the  `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` command in Exchange Online PowerShell to get information about the In-Place Hold on the mailbox.</span></span>  <br/> |
| <span data-ttu-id="d01ee-325">특정 사서함에 적용 되는 보안 & 준수 센터의 Office 365 보존 정책</span><span class="sxs-lookup"><span data-stu-id="d01ee-325">Office 365 retention policies in the Security & Compliance Center applied to specific mailboxes</span></span>  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> <span data-ttu-id="d01ee-326"> 선택하거나 </span><span class="sxs-lookup"><span data-stu-id="d01ee-326">or</span></span>  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |<span data-ttu-id="d01ee-327">**사서함** 관리 cmdlet을 실행 하는 경우 *InPlaceHolds* 속성에는 사서함에 적용 되는 Office 365 보존 정책의 guid도 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-327">When you run the **Get-Mailbox** cmdlet, the  *InPlaceHolds*  property also contains GUIDs of Office 365 retention policies applied to the mailbox.</span></span> <span data-ttu-id="d01ee-328">GUID는 `mbx` 접두사로 시작 되므로 보존 정책을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-328">You can identify retention policies because the GUID starts with the  `mbx` prefix.</span></span> <span data-ttu-id="d01ee-329">보존 정책의 GUID가 `skp` 접두사로 시작 되 면 보존 정책이 비즈니스용 Skype 대화에 적용 됨을 나타내는 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-329">Note that if the GUID of the retention policy starts with the  `skp` prefix, that indicates that the retention policy is applied to Skype for Business conversations.</span></span>  <br/> <span data-ttu-id="d01ee-330">사서함에 적용 되는 Office 365 보존 정책을 식별 하려면 Security & 준수 센터 PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-330">To identity the Office 365 retention policy that's applied to the mailbox, run the following command in Security & Compliance Center PowerShell:</span></span> <br/> <br/>`Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/><span data-ttu-id="d01ee-331">이 명령을 실행할 때 `mbx` or `skp` 접두사를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-331">Be sure to remove the  `mbx` or  `skp` prefix when you run this command.</span></span>  <br/> |
|<span data-ttu-id="d01ee-332">보안 & 준수 센터의 조직 전체 Office 365 보존 정책</span><span class="sxs-lookup"><span data-stu-id="d01ee-332">Organization-wide Office 365 retention policies in the Security & Compliance Center</span></span>  <br/> |<span data-ttu-id="d01ee-333">No 값</span><span class="sxs-lookup"><span data-stu-id="d01ee-333">No value</span></span>  <br/> <span data-ttu-id="d01ee-334"> 선택하거나 </span><span class="sxs-lookup"><span data-stu-id="d01ee-334">or</span></span>  <br/>  <span data-ttu-id="d01ee-335">`-mbxe9b52bf7ab3b46a286308ecb29624696`(사서함이 조직 차원 정책에서 제외 됨을 나타냄)</span><span class="sxs-lookup"><span data-stu-id="d01ee-335">`-mbxe9b52bf7ab3b46a286308ecb29624696` (indicates that the mailbox is excluded from an organization-wide policy)</span></span>  <br/> |<span data-ttu-id="d01ee-336">*InPlaceHolds* 속성이 비어 있는 경우에도 사서함 cmdlet을 실행할 \*\*\*\* 때 하나 이상의 조직 수준 Office 365 보존 정책이 사서함에 적용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-336">Even if the  *InPlaceHolds*  property is empty when you run the **Get-Mailbox** cmdlet, there still might be one or more organization-wide Office 365 retention policies applied to the mailbox.</span></span>  <br/> <span data-ttu-id="d01ee-337">이를 확인 하려면 Exchange Online PowerShell에서 `Get-OrganizationConfig | FL InPlaceHolds` 명령을 실행 하 여 조직 전반의 Office 365 보존 정책의 guid 목록을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-337">To verify this, you can run the  `Get-OrganizationConfig | FL InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies.</span></span> <span data-ttu-id="d01ee-338">Exchange 사서함에 적용 되는 조직 수준 보존 정책의 GUID는 `mbx` 접두사로 시작 합니다. 예를 `mbxa3056bb15562480fadb46ce523ff7b02`들어</span><span class="sxs-lookup"><span data-stu-id="d01ee-338">The GUID for organization-wide retention policies applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.</span></span>  <br/> <span data-ttu-id="d01ee-339">사서함에 적용 되는 조직 차원의 Office 365 보존 정책을 식별 하려면 Security & 준수 센터 PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-339">To identity the organization-wide Office 365 retention policy that's applied to the mailbox, run the following command in Security & Compliance Center PowerShell:</span></span> <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/><span data-ttu-id="d01ee-340">사서함이 조직 차원의 Office 365 보존 정책에서 제외 되는 경우 **사서함** cmdlet을 실행 하면 보존 정책의 GUID가 사용자 사서함의 *InPlaceHolds* 속성에 표시 됩니다. 이 접두사는 접두사로 `-mbx`식별 됩니다. 예를 들어`-mbxe9b52bf7ab3b46a286308ecb29624696`</span><span class="sxs-lookup"><span data-stu-id="d01ee-340">Note that if a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy is displayed in the  *InPlaceHolds*  property of the user's mailbox when you run the **Get-Mailbox** cmdlet; it's identified by the prefix  `-mbx`; for example,  `-mbxe9b52bf7ab3b46a286308ecb29624696`</span></span> <br/> |
|<span data-ttu-id="d01ee-341">보안 & 준수 센터의 eDiscovery 사례 보류</span><span class="sxs-lookup"><span data-stu-id="d01ee-341">eDiscovery case hold in the Security & Compliance Center</span></span>  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |<span data-ttu-id="d01ee-342">*InPlaceHolds* 속성에는 또한 사서함에 있을 수 있는 보안 & 준수 센터에서 eDiscovery 사례와 관련 된 모든 보류의 GUID가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-342">The  *InPlaceHolds*  property also contains the GUID of any hold associated with an eDiscovery case in the Security & Compliance Center that might be placed on the mailbox.</span></span> <span data-ttu-id="d01ee-343">GUID는 `UniH` 접두사로 시작 되므로 eDiscovery 사례 보류 임을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-343">You can tell this is an eDiscovery case hold because the GUID starts with the  `UniH` prefix.</span></span>  <br/> <span data-ttu-id="d01ee-344">Security & 준수 센터 `Get-CaseHoldPolicy` PowerShell의 cmdlet을 사용 하 여 사서함의 보류가 연결 된 eDiscovery 사례에 대 한 정보를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-344">You can use the  `Get-CaseHoldPolicy` cmdlet in Security & Compliance Center PowerShell to get information about the eDiscovery case that the hold on the mailbox is associated with.</span></span> <span data-ttu-id="d01ee-345">예를 들어 명령을 `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` 실행 하 여 사서함에 대 한 케이스 보류의 이름을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-345">For example, you can run the command  `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` to display the name of the case hold that's on the mailbox.</span></span> <span data-ttu-id="d01ee-346">이 명령을 실행할 때 `UniH` 접두사를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-346">Be sure to remove the  `UniH` prefix when you run this command.</span></span>  <br/><br/> <span data-ttu-id="d01ee-347">사서함의 보류가 연결 된 eDiscovery 사례를 식별 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01ee-347">To identity the eDiscovery case that the hold on the mailbox is associated with, run the following commands:</span></span><br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/>`Get-ComplianceCase $CaseHold.CaseId | FL Name`


