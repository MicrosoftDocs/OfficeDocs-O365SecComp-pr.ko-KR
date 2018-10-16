---
title: 관리자 도움말 대기-클라우드 기반 사서함의 복구 가능한 항목 폴더에서 항목 삭제
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: '관리자를 위한: 해당 사서함이 법적 보유 중일 경우에 Exchange Online 사서함에 대 한 사용자의 복구 가능한 항목 폴더에서 항목을 삭제 합니다. 이것이 Office 365에 실수로 넘어가 되는 데이터를 삭제할 수 있는 효과적인 방법입니다.'
ms.openlocfilehash: a10965ad088da98b4e4d84d823c124e5b192d505
ms.sourcegitcommit: b164d4af65709133e0b512a4327a70fae13a974d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2018
ms.locfileid: "25577087"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a><span data-ttu-id="06c66-104">관리자 도움말 대기-클라우드 기반 사서함의 복구 가능한 항목 폴더에서 항목 삭제</span><span class="sxs-lookup"><span data-stu-id="06c66-104">Delete items in the Recoverable Items folder of cloud-based mailboxes on hold - Admin Help</span></span>

<span data-ttu-id="06c66-p102">Exchange Online 사서함에 대 한 복구 가능한 항목 폴더에서 실수로 또는 악의적 삭제 보호 하기 위해 존재 합니다. 또한 유지 되 고, 검색 보류 및 eDiscovery와 같은 Office 365 규정 준수 기능에 액세스 하는 항목을 저장 하는데 사용 됩니다. 그러나 일부 상황에서 조직에는 실수로 삭제 해야 자신이 복구 가능한 항목 폴더에 보존 된 하는 데이터 있을 수 있습니다. 등 사용자 수 모른 보내기 또는 중요 한 정보 또는 심각한 비즈니스 영향을 미칠 수 있는 정보를 포함 하는 전자 메일 메시지를 전달 합니다. 메시지를 영구적으로 삭제 하는 경우에 것 수 보존할 무기한 법적 보유가 사서함에 배치 되어 있으므로 합니다. 이 시나리오는 Office 365에 데이터를 실수로 넘어가 된 되므로 데이터 액체 엎질렀는지 여부 라고 합니다. 이러한 상황에서 해당 사서함이 대기 상태에 놓일 Office 365의 다른 보류 기능 중 하나를 사용 하는 경우에 Exchange Online 사서함에 대 한 사용자의 복구 가능한 항목 폴더에서 항목을 삭제할 수 있습니다. 이러한 유형의 보류 소송 보존을 포함 하 고, 원본 위치 유지, eDiscovery 보류 및 Office 365 보안에서 만든 Office 365 보존 정책이 포함 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p102">The Recoverable Items folder for an Exchange Online mailbox exists to protect from accidental or malicious deletions. It's also used to store items that are retained and accessed by Office 365 compliance features, such as holds and eDiscovery searches. However, in some situations organizations might have data that's been unintentionally retained in the Recoverable Items folder that they must delete. For example, a user might unknowingly send or forward an email message that contains sensitive information or information that may have serious business consequences. Even if the message is permanently deleted, it might be retained indefinitely because a legal hold has been placed on the mailbox. This scenario is known as data spillage because data has been unintentionally spilled into Office 365. In these situations, you can delete items in a user's Recoverable Items folder for an Exchange Online mailbox, even if that mailbox is placed on hold with one of the different hold features in Office 365. These types of holds include Litigation Holds, In-Place Holds, eDiscovery holds, and Office 365 retention policies created in the Office 365 Security &amp; Compliance Center.</span></span> 
  
 <span data-ttu-id="06c66-p103">이 문서에서는 보류에 있는 클라우드 기반 사서함에 대 한 복구 가능한 항목 폴더에서 항목을 삭제 하는 방법에 설명 합니다. 이 절차는 사서함에 대 한 액세스를 사용 하지 않도록 설정 하 고는 관리 되는 폴더 도우미에서 사서함을 처리, 일시적으로 보류를 제거 하 고, 복구 가능한 항목 폴더에서 항목을 삭제 하 고 되돌리는 다음을 사용 하지 않도록 설정 하는 단일 항목 복구를 사용 하지 않도록 설정 사서함의 이전 구성입니다. 하는 프로세스는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p103">This article explains how to delete items from the Recoverable Items folder for cloud-based mailboxes that are on hold. This procedure involves disabling access to the mailbox and disabling single item recovery, disabling the Managed Folder Assistant from processing the mailbox, temporarily removing the hold, deleting items from the Recoverable Items folder, and then reverting the mailbox to its previous configuration. Here's the process:</span></span> 
  
[<span data-ttu-id="06c66-116">1 단계: 사서함에 대 한 정보를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-116">Step 1: Collect information about the mailbox</span></span>](#step-1-collect-information-about-the-mailbox)

[<span data-ttu-id="06c66-117">2 단계: 사서함 준비</span><span class="sxs-lookup"><span data-stu-id="06c66-117">Step 2: Prepare the mailbox</span></span>](#step-2-prepare-the-mailbox)

[<span data-ttu-id="06c66-118">3 단계: 사서함에서 모든 보류를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-118">Step 3: Remove all holds from the mailbox</span></span>](#step-3-remove-all-holds-from-the-mailbox)

[<span data-ttu-id="06c66-119">4 단계: 사서함에서 지연 보류를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-119">Step 4: Remove the delay hold from the mailbox</span></span>](#step-4-remove-the-delay-hold-from-the-mailbox)

[<span data-ttu-id="06c66-120">복구 가능한 항목 폴더에서 항목을 삭제 하는 5 단계:</span><span class="sxs-lookup"><span data-stu-id="06c66-120">Step 5: Delete items in the Recoverable Items folder</span></span>](#step-5-delete-items-in-the-recoverable-items-folder)

[<span data-ttu-id="06c66-121">6 단계: 사서함을 이전 상태로 되돌리기</span><span class="sxs-lookup"><span data-stu-id="06c66-121">Step 6: Revert the mailbox to its previous state</span></span>](#step-6-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> <span data-ttu-id="06c66-p104">이 문서에 설명 된 절차 될 되는 데이터 영구적으로 삭제 (비우기)에서 Exchange Online 사서함 수 있습니다. 즉, 메시지 복구 가능한 항목 폴더에서 삭제를 복구할 수 없는 및 법적 개시 또는 기타 준수 용도로 사용할 수 없습니다. 원본 위치 유지는 소송 보존의 일환으로 보류에 추가 되는 사서함에서 메시지를 삭제 하려는 경우 eDiscovery 보류 또는 Office 365 보안에서 Office 365 보존 정책을 만든 &amp; 준수 센터, 레코드 관리 또는 법률 확인 보류를 제거 하기 전에 부서 합니다. 조직에 사서함에 보존 여부를 정의 하는 정책을 사용할 수 있습니다 또는 데이터 액체 엎질렀는지 여부 문제가 발생 한 설정이 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p104">The procedures outlined in this article will result in data being permanently deleted (purged) from an Exchange Online mailbox. That means messages that you delete from the Recoverable Items folder can't be recovered and won't be available for legal discovery or other compliance purposes. If you want to delete messages from a mailbox that's placed on hold as part of a Litigation Hold, In-Place Hold, eDiscovery hold, or Office 365 retention policy created in the Office 365 Security &amp; Compliance Center, check with your records management or legal departments before removing the hold. Your organization might have a policy that defines whether a mailbox on hold or a data spillage incident takes priority.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="06c66-126">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="06c66-126">Before you begin</span></span>

- <span data-ttu-id="06c66-127">다음 관리 역할을 모두 Exchange Online에 할당할를 검색 하 고 5 단계에서에서 복구 가능한 항목 폴더에서 메시지를 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-127">You have to be assigned both of the following management roles in Exchange Online to search for and delete messages from the Recoverable Items folder in Step 5.</span></span>
    
  - <span data-ttu-id="06c66-p105">**사서함 검색** -이 역할을 사용 하면 조직에서 사서함을 검색할 수 있습니다. Exchange 관리자가 기본적으로이 역할을 할당 되지 않습니다. 사용자가 직접이 역할을 할당 하려면 추가 자신 검색 관리 역할 그룹의 구성원으로 Exchange Online 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p105">**Mailbox Search** - This role lets you to search mailboxes in your organization. Exchange administrators aren't assigned this role by default. To assign yourself this role, add yourself as a member of the Discovery Management role group in Exchange Online.</span></span> 
    
  - <span data-ttu-id="06c66-p106">**사서함 가져오기 내보내기** -이 역할을 통해 사용자의 사서함에서 메시지를 삭제할 수 있습니다. 기본적으로이 역할은 모든 역할 그룹에 할당 되지 않습니다. 사용자의 사서함에서 메시지를 삭제 하려면 추가할 수 있습니다는 사서함 가져오기 내보내기 역할 조직 관리 역할 그룹에 Exchange 온라인.</span><span class="sxs-lookup"><span data-stu-id="06c66-p106">**Mailbox Import Export** - This role lets you to delete messages from a user's mailbox. By default, this role isn't assigned to any role group. To delete messages from users' mailboxes, you can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> 
    
- <span data-ttu-id="06c66-p107">이 문서에서 설명 하는 절차는 비활성 사서함에 대 한 지원 되지 않습니다. 있기 때문입니다 보류 (또는 Office 365 보존 정책)를 다시 적용할 수 없습니다 비활성 사서함을 제거 하면 됩니다. 비활성 사서함에서 보류를 제거할 때 기본 일시 삭제 된 사서함으로 변경 되 고 관리 하는 폴더 도우미에 의해 처리 된 후 조직에서 영구적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p107">The procedure described in this article isn't supported for inactive mailboxes. That's because you can't re-apply a hold (or Office 365 retention policy) to an inactive mailbox after you remove it. When you remove a hold from an inactive mailbox, it's changed to a normal soft-deleted mailbox and will be permanently deleted from your organization after it's processed by the Managed Folder Assistant.</span></span>
    
- <span data-ttu-id="06c66-p108">보존 잠금을 사용 하 여 잠긴 되는 Office 365 보존 정책에 할당 된 사서함에 대해이 절차를 수행할 수 없습니다. 보존 잠금을 제거 하거나는 관리 되는 폴더 도우미는 사서함에서 사용 하지 않도록 설정 및 Office 365 보존 정책에서 사서함을 제외 하면 때문입니다. 보존 정책 잠금에 대 한 자세한 내용은 [보존 정책 잠금](retention-policies.md#locking-a-retention-policy)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="06c66-p108">You can't perform this procedure for a mailbox that has been assigned to an Office 365 retention policy that's been locked with a Preservation Lock. That's because a Preservation Lock prevents you from removing or excluding the mailbox from the Office 365 retention policy and from disabling the Managed Folder Assistant on the mailbox. For more information about locking retention policies, see [Locking a retention policy](retention-policies.md#locking-a-retention-policy).</span></span>
    
- <span data-ttu-id="06c66-p109">사서함 보류에 추가 되지 않습니다 (또는 단일 항목 복구를 사용할 수 없으면) 하는 경우에 복구 가능한 항목 폴더에서 항목을 간단히 삭제할 수 있습니다. 이 작업을 수행 하는 방법에 대 한 자세한 내용은 [메시지에 대 한 검색 및 삭제를 ](https://go.microsoft.com/fwlink/?linkid=852453)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="06c66-p109">If a mailbox isn't placed on hold (or doesn't have single item recovery enabled), you can simply delete the items from the Recoverable Items folder. For more information about how to do this, see [Search for and delete messages ](https://go.microsoft.com/fwlink/?linkid=852453).</span></span>
  
## <a name="step-1-collect-information-about-the-mailbox"></a><span data-ttu-id="06c66-142">1 단계: 사서함에 대 한 정보를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-142">Step 1: Collect information about the mailbox</span></span>

<span data-ttu-id="06c66-p110">이 첫번째 단계가이 절차에 영향을 주는 대상 사서함에서 선택 된 속성을 수집 하는 것입니다. 이러한 설정을 기록해 또는 이러한 속성 중 일부를 변경 하 고 복구 가능한 항목 폴더에서 항목을 삭제 한 후 다음 6 단계에서에서 원래 값으로 다시 되돌릴 수 있으므로 텍스트 파일에 저장 해야 합니다. 다음은 수집 해야하는 사서함 속성의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p110">This first step is to collect selected properties from the target mailbox that will affect this procedure. Be sure to write down these settings or save them to a text file because you'll change some of these properties and then revert back to the original values in Step 6, after you delete items from the Recoverable Items folder. Here's a list of the mailbox properties you need to collect.</span></span>
  
-  <span data-ttu-id="06c66-146">*SingleItemRecoveryEnabled* 및 *RetainDeletedItemsFor* ; 필요한 경우 단일 복구를 사용 하지 않도록 설정 하 고 3 단계에서에서 삭제 된 항목 보존 기간을 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-146">*SingleItemRecoveryEnabled*  and  *RetainDeletedItemsFor*  ; if necessary, you'll disable single recovery and increase the deleted items retention period in Step 3.</span></span> 
    
-  <span data-ttu-id="06c66-p111">*LitigationHoldEnabled* 및 *InPlaceHolds* ; 3 단계에서에서 일시적으로 제거할 수 있도록 사서함에 배치 하는 모든 보류를 식별 해야 합니다. 사서함에 배치 될 수 있는 형식 보류를 식별 하는 방법에 대 한 팁에 대 한 [자세한 내용](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) 은 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="06c66-p111">*LitigationHoldEnabled*  and  *InPlaceHolds*  ; you need to identify all the holds placed on the mailbox so that you can temporarily remove them in Step 3. See the [More information](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) section for tips about how to identify the type hold that might be placed on a mailbox.</span></span> 
    
<span data-ttu-id="06c66-p112">또한 있도록 가져옵니다. 사서함 클라이언트 액세스 설정을 해제할 수 있습니다 일시적으로 소유자 (또는 다른 사용자에 게) 하는 동안이 절차는 사서함에 액세스할 수 없습니다 있도록 필요 합니다. 마지막으로 복구 가능한 항목 폴더의 현재 크기 및 항목 수를 얻을 수 있습니다. 5 단계에서에서 복구 가능한 항목 폴더에서 항목을 삭제 한 후이 정보를 사용 하 여 실제로 제거 된 항목을 확인 하기 위해 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p112">Additionally, you need to get the mailbox client access settings so you can temporarily disable them so the owner (or other users) can't access the mailbox during this procedure. Finally, you can get the current size and number of items in the Recoverable Items folder. After you delete items in the Recoverable Items folder in Step 5, you'll use this information to verify that items were actually removed.</span></span>
  
1. <span data-ttu-id="06c66-p113">[Exchange Online PowerShell에 연결](https://go.microsoft.com/fwlink/?linkid=396554)합니다. Exchange Online에서 적절 한 관리 역할 할당 된 관리자 계정에 대 한 사용자 이름 및 암호를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p113">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Be sure to use a user name and password for an administrator account that's been assigned the appropriate management roles in Exchange Online.</span></span> 
    
2. <span data-ttu-id="06c66-154">단일 항목 복구 하 고 삭제 된 항목 보존 기간에 대 한 정보를 가져오려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-154">Run the following command to get information about single item recovery and the deleted item retention period.</span></span>

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   <span data-ttu-id="06c66-p114">단일 항목 복구를 사용 하는 경우 2 단계에서에서 사용 하지 않도록 설정 해야 합니다. 하는 경우 삭제 된 항목 보존 기간을 30 일 동안 설정 되지 않습니다 (Exchange Online의 최대 값) 다음 2 단계에서에서 늘릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p114">If single item recovery is enabled, you'll have to disable it in Step 2. If the deleted item retention period isn't set for 30 days (the maximum value in Exchange Online), then you can increase it in Step 2.</span></span> 
    
3. <span data-ttu-id="06c66-157">사서함의 사서함에 대 한 액세스 설정 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-157">Run the following command to get the mailbox access settings for the mailbox.</span></span> 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   <span data-ttu-id="06c66-158">2 단계에서에서 이러한 액세스 방법의 모든를 비활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-158">You'll disable all of these access methods in Step 2.</span></span>
    
4. <span data-ttu-id="06c66-159">보류 및 사서함에 적용 된 Office 365 보존 정책에 대 한 정보를 가져오려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-159">Run the following command to get information about the holds and Office 365 retention policies applied to the mailbox.</span></span>
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > <span data-ttu-id="06c66-160">실행할 수 *InPlaceHolds* 속성에 너무 많은 값이 모두 하지 표시 하는 경우는 `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` 별도 줄에 각 값을 표시 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-160">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
5. <span data-ttu-id="06c66-161">모든 조직 전체의 Office 365 보존 정책에 대 한 정보를 가져오려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-161">Run the following command to get information about any organization-wide Office 365 retention policies.</span></span> 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   <span data-ttu-id="06c66-162">조직에 있는 조직 수준의 Office 365 보존 정책, 3 단계에서에서 이러한 정책에서 사서함을 제외 하도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-162">If your organization has any organization-wide Office 365 retention policies, you'll have to exclude the mailbox from these policies in Step 3.</span></span>

   > [!TIP]
    > <span data-ttu-id="06c66-163">실행할 수 *InPlaceHolds* 속성에 너무 많은 값이 모두 하지 표시 하는 경우는 `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` 별도 줄에 각 값을 표시 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-163">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
6. <span data-ttu-id="06c66-164">폴더와 사용자의 기본 사서함의 복구 가능한 항목 폴더에 하위 폴더에서 항목의 총 수와 현재 크기를 가져오려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-164">Run the following command to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="06c66-165">폴더 및 보관 사서함의 복구 가능한 항목 폴더에 하위 폴더의 크기와 총 항목 수를 가져오려면 다음 명령을 실행 하는 사용자의 보관 사서함을 사용 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="06c66-165">If the user's archive mailbox is enabled, run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in their archive mailbox.</span></span> 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="06c66-p115">5 단계에서에서 항목을 삭제 하는 경우에 삭제 또는 사용자의 기본 보관 사서함의 복구 가능한 항목 폴더에서 항목을 삭제 하지를 선택할 수 있습니다. 참고 보관 자동을 확장 하면 해당 사서함에 대해 활성화 된 경우 보조 보관 사서함에 있는 항목은 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p115">When you delete items in Step 5, you can choose to delete or not delete items in the Recoverable Items folder in the user's primary archive mailbox. Note that if auto-expanding archiving is enabled for the mailbox, items in an auxiliary archive mailbox won't be deleted.</span></span>
  
## <a name="step-2-prepare-the-mailbox"></a><span data-ttu-id="06c66-168">2 단계: 사서함 준비</span><span class="sxs-lookup"><span data-stu-id="06c66-168">Step 2: Prepare the mailbox</span></span>

<span data-ttu-id="06c66-169">수집 하 고 사서함에 대 한 정보를 저장 한 후 다음 단계는 다음과 같은 작업을 수행 하 여 사서함을 준비 하는 것:</span><span class="sxs-lookup"><span data-stu-id="06c66-169">After collecting and saving information about the mailbox, the next step is to prepare the mailbox by performing the following tasks:</span></span> 
  
- <span data-ttu-id="06c66-170">**사서함에 대 한 클라이언트 액세스를 사용 하지 않도록 설정** 하 사서함 소유자 수는 없습니다 자신의 사서함에 액세스 하 고이 절차는 동안 사서함 데이터를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-170">**Disable client access to mailbox** so that the mailbox owner can't access their mailbox and make any changes to the mailbox data during this procedure.</span></span> 
    
- <span data-ttu-id="06c66-171">30 일에 **삭제 된 항목 보존 기간을 늘립니다** (Exchange Online의 최대값) 5 단계에서에서 삭제 하기 전에 복구 가능한 항목 폴더에서 항목 삭제 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-171">**Increase the deleted item retention period** to 30 days (the maximum value in Exchange Online) so that items aren't purged from the Recoverable Items folder before you can delete them in Step 5.</span></span> 
    
- <span data-ttu-id="06c66-172">5 단계에서에서 복구 가능한 항목 폴더에서 삭제 하면 (삭제 된 항목 보존 기간을 기간)에 대 한 **단일 항목 복구를 사용 하지 않도록 설정** 하는 항목이 있으므로 유지 되지 않을 것입니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-172">**Disable single Item recovery** so that items won't be retained (for the duration of the deleted item retention period) after you delete them from the Recoverable Items folder in Step 5.</span></span> 
    
- <span data-ttu-id="06c66-173">It 관리 사서함을 처리 하며 5 단계에서에서 삭제 된 항목을 유지 하지 않도록 **관리 되는 폴더 도우미가 사용 하지 않도록 설정** 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-173">**Disable the Managed Folder Assistant** so that it doesn't process the mailbox and retain the items that you delete in Step 5.</span></span> 
    
<span data-ttu-id="06c66-174">Exchange Online PowerShell에서 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-174">Perform the following steps in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="06c66-p116">사서함에 대 한 모든 클라이언트 액세스를 사용 하지 않도록 설정 하려면 다음 명령을 실행 합니다. 명령 구문 사서함에서 모든 클라이언트 액세스 방법 활성화 되었는지 하는 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p116">Run the following command to disable all client access to the mailbox. The command syntax assumes that all client access methods were enabled on the mailbox.</span></span>

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > <span data-ttu-id="06c66-p117">사서함에 모든 클라이언트 액세스 방법을 사용 하지 않으려면 60 분까지 걸릴 수 있습니다. Note 이러한 액세스 메서드를 사용 하지 않도록 설정에서 로그인 현재 사서함 소유자 분리 하지 않습니다. 소유자 되지 로그인 하는 경우 이러한 액세스 방법을 사용할 수 없는 후 자신의 사서함에 액세스 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p117">It might take up to 60 minutes to disable all client access methods to the mailbox. Note that disabling these access methods won't disconnect the mailbox owner they're currently signed in. If the owner isn't signed in, then they won't be able to access their mailbox after these access methods are disabled.</span></span> 
  
2. <span data-ttu-id="06c66-p118">최대 30 일의 삭제 된 항목 보존 기간을 늘리려면 다음 명령을 실행 합니다. 이 현재 설정을 30 일 보다 작은 이라고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p118">Run the following command to increase the deleted item retention period the maximum of 30 days. This assumes that the current setting is less than 30 days.</span></span> 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. <span data-ttu-id="06c66-182">단일 항목 복구를 사용 하지 않도록 설정 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-182">Run the following command to disable single item recovery.</span></span>
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > <span data-ttu-id="06c66-p119">단일 항목 복구를 사용 하지 않도록 설정 하려면 최대 60 분까지 걸릴 수 있습니다. 이 기간 경과할 때까지 복구 가능한 항목 폴더에서 항목을 삭제 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="06c66-p119">It might take up to 60 minutes to disable single item recovery. Don't delete items in the Recoverable Items folder until this period has elapsed.</span></span> 
  
4. <span data-ttu-id="06c66-p120">관리 되는 폴더 도우미에서 사서함을 처리 하지 않으려면 다음 명령을 실행 합니다. 앞에서 설명한 것 처럼 경우 비활성화할 수 있습니다는 관리 되는 폴더 도우미만 사서함에 보존 잠금에는 Office 365 보존 정책이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p120">Run the following command to prevent the Managed Folder Assistant from processing the mailbox. As previously explained, you can disable the Managed Folder Assistant only if an Office 365 retention policy with a Preservation Lock is not applied to the mailbox.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a><span data-ttu-id="06c66-187">3 단계: 사서함에서 모든 보류를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-187">Step 3: Remove all holds from the mailbox</span></span>

<span data-ttu-id="06c66-p121">복구 가능한 항목 폴더에서 항목을 삭제 하기 전에 마지막 단계는 사서함에 배치 모든 (즉 1 단계에서에서 식별) 보류를 제거 하는 것입니다. 복구 가능한 항목 폴더에서 삭제 한 후 항목을 유지 되지 않을 것 되도록 모든 보류를 제거 해야 합니다. 다음 섹션에서는 다양 한 유형의 사서함에서 보류를 제거 하는 방법에 대 한 정보를 포함 합니다. 사서함에 배치 될 수 있는 형식 보류를 식별 하는 방법에 대 한 팁에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 하십시오. 자세한 내용은 [유형을 식별 하는 방법을 hold Exchange Online 사서함에 배치](identify-a-hold-on-an-exchange-online-mailbox.md)를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p121">The last step before you can delete items from the Recoverable Items folder is to remove all holds (that you identified in Step 1) placed on the mailbox. All holds must be removed so that items won't be retained after you delete them from the Recoverable Items folder. The following sections contain information about removing different types of holds on a mailbox. See the [More information](#more-information) section for tips about how to identify the type hold that might be placed on a mailbox. For additional information, see [How to identify the type of hold placed on an Exchange Online mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>
  
> [!CAUTION]
> <span data-ttu-id="06c66-193">앞서 설명한 것 처럼 사서함에서 보류를 제거 하기 전에 레코드 관리 또는 법률 부서를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-193">As previously stated, check with your records management or legal departments before removing a hold from a mailbox.</span></span> 
  
 ### <a name="litigation-hold"></a><span data-ttu-id="06c66-194">소송 보존</span><span class="sxs-lookup"><span data-stu-id="06c66-194">Litigation Hold</span></span>
  
<span data-ttu-id="06c66-195">다음 명령을 실행 Exchange Online 사서함에서 소송 보존을 제거 하는 PowerShell 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-195">Run the following command in Exchange Online PowerShell to remove a Litigation Hold from the mailbox.</span></span>

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> <span data-ttu-id="06c66-p122">클라이언트 액세스 방법 및 단일 항목 복구를 사용 하지 않도록 설정 하려면와 마찬가지로 걸릴 수 있습니다 소송 보존을 제거 하려면 최대 60 분입니다. 이 기간 경과할 때까지 복구 가능한 항목 폴더에서 항목을 삭제 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="06c66-p122">Similar to disabling the client access methods and single item recovery, it might take up to 60 minutes to remove the Litigation Hold. Don't delete items from the Recoverable Items folder until this period has elapsed.</span></span> 
  
 ### <a name="in-place-hold"></a><span data-ttu-id="06c66-198">원본 위치 유지</span><span class="sxs-lookup"><span data-stu-id="06c66-198">In-Place Hold</span></span>
  
<span data-ttu-id="06c66-p123">다음 명령을 실행 Exchange Online 사서함에 배치 되는 원본 위치 유지를 식별 하는 PowerShell 합니다. 1 단계에서에서 식별 된 원본 위치 유지 하는 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p123">Run the following command in Exchange Online PowerShell to identify the In-Place Hold that's placed on the mailbox. Use the GUID for the In-Place Hold that you identified in Step 1.</span></span> 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
<span data-ttu-id="06c66-p124">원본 위치 유지를 확인 한 후 보류에서 사서함을 제거 하려면 Exchange 관리 센터 (EAC) 또는 Exchange Online PowerShell을 사용할 수 있습니다. 자세한 내용은 [만들기 또는 제거 In-place Hold](https://go.microsoft.com/fwlink/?linkid=852668)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="06c66-p124">After you identify the In-Place Hold, you can use the Exchange admin center (EAC) or Exchange Online PowerShell to remove the mailbox from the hold. For more information, see [Create or remove an In-Place Hold](https://go.microsoft.com/fwlink/?linkid=852668).</span></span>
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a><span data-ttu-id="06c66-203">특정 사서함에 적용 하는 office 365 보존 정책</span><span class="sxs-lookup"><span data-stu-id="06c66-203">Office 365 retention policies applied to specific mailboxes</span></span>
  
<span data-ttu-id="06c66-p125">다음 명령을 실행 [Office 365 보안 &amp; 준수 센터 PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) 사서함에 적용 되는 Office 365 보존 정책을 식별 합니다. GUID를 사용 하 여 (포함 하지는 `mbx` 또는 `skp` 접두사) 1 단계에서에서 식별 하는 보존 정책에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p125">Run the following command in [Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the Office 365 retention policy that is applied to the mailbox. Use the GUID (not including the  `mbx` or  `skp` prefix) for the retention policy that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
<span data-ttu-id="06c66-206">**날짜 관리 방식** 으로 이동 하는 보존 정책, 파악 한 후 \> 보안에서 **보존** 페이지 &amp; 준수 센터 이전 단계에서 식별 하는 보존 정책을 편집 하 고 목록에서 사서함을 제거 합니다. 보존 정책에 포함 된 받는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-206">After you identify the retention policy, go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the retention policy that you identified in the previous step, and remove the mailbox from the list of recipients that are included in the retention policy.</span></span> 
  
 ### <a name="organization-wide-office-365-retention-policies"></a><span data-ttu-id="06c66-207">조직 전체의 Office 365 보존 정책</span><span class="sxs-lookup"><span data-stu-id="06c66-207">Organization-wide Office 365 retention policies</span></span>
  
<span data-ttu-id="06c66-p126">조직에서 모든 사서함에 조직 차원 및 Exchange 전체 Office 365 보존 정책이 적용 됩니다. 이러한 (사서함 수준이 아닌 함) 조직 수준에서 적용 되 고 1 단계에서에서 **Get-organizationconfig** cmdlet을 실행 하는 경우 반환 됩니다. 다음 명령을 실행 [보안 &amp; 준수 센터 PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) 를 조직 전체의 Office 365 보존 정책을 식별 합니다. GUID를 사용 하 여 (포함 하지는 `mbx` 접두사) 1 단계에서에서 식별 하는 조직 전체의 보존 정책에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p126">Organization-wide and Exchange-wide Office 365 retention policies are applied to every mailbox in the organization. They are applied at the organization level (not the mailbox level) and are returned when you run the **Get-OrganizationConfig** cmdlet in Step 1. Run the following command in [Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the organization-wide Office 365 retention policies. Use the GUID (not including the  `mbx` prefix) for the organization-wide retention policies that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

<span data-ttu-id="06c66-p127">**날짜 관리 방식** 으로 이동 하는 조직 전체의 Office 365 보존 정책, 파악 한 후 \> 보안에서 **보존** 페이지 &amp; 준수 센터에서 식별 하는 각 조직 전체의 보존 정책 편집은 이전 단계를 실행 하 고 사서함 제외 된 받는 사람 목록에 추가 합니다. 이렇게 하면 사용자의 사서함 보존 정책에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p127">After you identify the organization-wide Office 365 retention policies, go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit each organization-wide retention policy that you identified in the previous step, and add the mailbox to the list of excluded recipients. Doing this will remove the user's mailbox from the retention policy.</span></span> 

### <a name="office-365-retention-labels"></a><span data-ttu-id="06c66-214">Office 365 보존 레이블</span><span class="sxs-lookup"><span data-stu-id="06c66-214">Office 365 retention labels</span></span>

<span data-ttu-id="06c66-p128">다음은 콘텐츠를 보존 또는 유지 하 고 다음 콘텐츠를 모든 폴더 또는 사서함의 항목을 삭제 하도록 구성 된 레이블을 적용 하는 사용자, 때마다 *ComplianceTagHoldApplied* 사서함 속성을 **True**로 설정 됩니다. 이러한 상황이 발생 하는 경우에 사서함 수, 기다리는 경우 처럼 소송 보존에 배치 또는 Office 365 보존 정책에 할당 된 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p128">Whenever a user applies a label that's configured to retain content or retain and then delete content to any folder or item in their mailbox, the *ComplianceTagHoldApplied* mailbox property is set to **True**. When this happens, the mailbox is considered to be on hold, just as if it was placed on Litigation Hold or assigned to an Office 365 retention policy.</span></span>

<span data-ttu-id="06c66-217">*ComplianceTagHoldApplied* 속성의 값을 보려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-217">To view the value of the *ComplianceTagHoldApplied* property, run the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

<span data-ttu-id="06c66-p129">사서함이에 식별 한 후 보존 레이블 폴더 또는 항목에 적용 되, 콘텐츠 검색 도구를 사용 하 여 보안에서 수 및 ComplianceTag 검색 조건을 사용 하 여 레이블이 지정 된 항목을 찾으려고 준수 센터 때문에 보관 합니다. 자세한 내용은 [키워드 쿼리 및 콘텐츠 검색을 위한 검색 조건에서](keyword-queries-and-search-conditions.md#conditions-for-common-properties)"검색 조건" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="06c66-p129">After you've identified that a mailbox is on hold because a retention label is applied to a folder or item, you can use the Content Search tool in the Security & Compliance Center to search for labeled items by using the ComplianceTag search condition. For more information, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md#conditions-for-common-properties).</span></span>

<span data-ttu-id="06c66-220">레이블에 대 한 자세한 내용은 [Office 365 개요 레이블](labels.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="06c66-220">For more information about labels, see [Overview of Office 365 labels](labels.md).</span></span>

 ### <a name="ediscovery-case-holds"></a><span data-ttu-id="06c66-221">eDiscovery 사례를 포함 하</span><span class="sxs-lookup"><span data-stu-id="06c66-221">eDiscovery case holds</span></span>
  
<span data-ttu-id="06c66-p130">다음 명령을 실행 [보안 &amp; 준수 센터 PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) 사서함에 적용 되는 eDiscovery 사례와 관련 된 보류를 식별할 수 있습니다. GUID를 사용 하 여 (포함 하지는 `UniH` 접두사) eDiscovery에 대 한 1 단계에서에서 확인 된을 유지 합니다. 두번째 명령은 보류;와 연결 된 eDiscovery 사례의 이름을 표시 하는 note 세번째 명령은 보류의 이름을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p130">Run the following commands in [Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the hold associated with an eDiscovery case that's applied to the mailbox. Use the GUID (not including the  `UniH` prefix) for the eDiscovery hold that you identified in Step 1. Note that the second command displays the name of the eDiscovery case the hold is associated with; the third command displays the name of the hold.</span></span> 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

<span data-ttu-id="06c66-p131">EDiscovery 사례와 보류의 이름을 결정 했다면, 한 후 이동은 **검색 &amp; 조사** \> 보안에서 **eDiscovery** 페이지 &amp; 준수 센터 대/소문자를 열고 보류에서 사서함을 제거 합니다. 자세한 내용은 참조 [Office 365 보안에서 eDiscovery 사례 관리 &amp; 준수 센터](manage-ediscovery-cases.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p131">After you've identified the name of the eDiscovery case and the hold, go to the **Search &amp; investigation** \> **eDiscovery** page in the Security &amp; Compliance Center, open the case, and remove the mailbox from the hold. For more information, see [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](manage-ediscovery-cases.md).</span></span>
  
## <a name="step-4-remove-the-delay-hold-from-the-mailbox"></a><span data-ttu-id="06c66-227">4 단계: 사서함에서 지연 보류를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-227">Step 4: Remove the delay hold from the mailbox</span></span>

<span data-ttu-id="06c66-p132">모든 유형의 대기 사서함에서 제거 되 면 후 *DelayHoldApplied* 사서함 속성의 값을 **True**로 설정 됩니다. 이 관리 되는 폴더 도우미는 사서함을 처리 하 고 보류 제거 된 감지 다음에 발생 합니다. 이 *지연 유지* 라고 하 고 사서함에서 영구적으로 삭제 되 고에서 데이터를 방지 하기 위해 30 일 동안 보류의 실제 제거 배달이 지연 것을 의미 합니다. (지연 보류의 용도 admins를 검색 하거나 경과한 보류에서 제거 된 후 사서함 항목을 복구할 수 있도록 합니다.)  지연 보류의 사서함에 배치 되 면 때 사서함은 여전히 사서함에 소송 보존으로 설정 된 하는 경우으로 대기는 무제한 기간에 대 한 것으로 간주 됩니다. 30 일 후 지연 보류 만료 되 면 및 Office 365 됩니다 ( *DelayHoldApplied* 속성을 **False**로 설정) 하 여 지연 보류를 제거 하려고 자동으로 보존이 실제로 제거 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p132">After any type of hold is removed from a mailbox, the value of the *DelayHoldApplied* mailbox property is set to **True**. This occurs the next time the Managed Folder Assistant processes the mailbox and detects that a hold has been removed. This is called a *delay hold* and means the actual removal of the hold is delayed for 30 days to prevent data from being permanently deleted from the mailbox. (The purpose of a delay hold is to give admins an opportunity to search for or recover mailbox items that will be purged after a hold is removed.)  When a delay hold is placed on the mailbox, the mailbox is still considered to be on hold for an unlimited duration, as if the mailbox was on Litigation Hold. After 30 days, the delay hold expires, and Office 365 will automatically attempt to remove the delay hold (by setting the *DelayHoldApplied* property to **False**) so that the hold is actually removed.</span></span> 

<span data-ttu-id="06c66-p133">5 단계에서에서 항목을 삭제 하기 전에 사서함에서 지연 보류를 제거 해야 합니다. 먼저, 지연 대기 Exchange Online PowerShell에서 다음 명령을 실행 하 여 사서함에 적용 하는 경우를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p133">Before you can delete items in Step 5, you have to remove the delay hold from the mailbox. First, determine if the delay hold is applied to the mailbox by running the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox <username> | FL DelayHoldApplied
```

<span data-ttu-id="06c66-p134">*DelayHoldApplied* 속성 값은 **False**로 설정 하는 경우 지연 보류 사서함에 배치 된 되지 않았습니다. 단계 5로 이동 하 고 복구 가능한 항목 폴더에서 항목을 삭제 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p134">If the value of the *DelayHoldApplied* property is set to **False**, a delay hold has not been placed on the mailbox. You can go to Step 5 and delete items in the Recoverable Items folder.</span></span>

<span data-ttu-id="06c66-237">*DelayHoldApplied* 속성 값은 **True**로 설정 하는 경우에 지연 보류를 제거 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-237">If the value of the *DelayHoldApplied* property is set to **True**, run the following command to remove the delay hold:</span></span>

```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
<span data-ttu-id="06c66-238">할당 되어야 합니다 법적 보존 역할 Exchange 온라인 *RemoveDelayHoldApplied* 매개 변수를 사용 하 여 note 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-238">Note that you must be assigned the Legal Hold role in Exchange Online to use the *RemoveDelayHoldApplied* parameter.</span></span>

## <a name="step-5-delete-items-in-the-recoverable-items-folder"></a><span data-ttu-id="06c66-239">복구 가능한 항목 폴더에서 항목을 삭제 하는 5 단계:</span><span class="sxs-lookup"><span data-stu-id="06c66-239">Step 5: Delete items in the Recoverable Items folder</span></span>

<span data-ttu-id="06c66-p135">이제 준비가 실제로 사용 하 여 [검색 사서함](https://go.microsoft.com/fwlink/?linkid=852595) cmdlet은 Exchange Online PowerShell 복구 가능한 항목 폴더에서 항목을 삭제 합니다. **Search-mailbox** cmdlet을 실행 하는 경우 다음과 같은 세가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p135">Now you're ready to actually delete items in the Recoverable Items folder by using the [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) cmdlet in Exchange Online PowerShell. You have three options when running the **Search-Mailbox** cmdlet.</span></span> 
  
- <span data-ttu-id="06c66-242">삭제 하기 전에 필요한 경우 항목을 검토할 수 있습니다를 삭제 하기 전에 대상 사서함에 항목을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-242">Copy items to a target mailbox before you delete them so that you can review the items, if necessary, before you delete them.</span></span>
    
- <span data-ttu-id="06c66-243">대상 사서함에 항목을 복사 하 고 같은 명령에서이 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-243">Copy items to a target mailbox and delete them in the same command.</span></span>
    
- <span data-ttu-id="06c66-244">대상 사서함으로 복사 하지 않고 항목을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-244">Delete items without copying them to a target mailbox.</span></span> 
    
<span data-ttu-id="06c66-p136">사용자의 기본 보관 사서함의 복구 가능한 항목 폴더에서 항목을 참고 실행 하는 경우에 삭제 됩니다는 \* \* 검색 사서함 \* \* cmdlet입니다. 이 방지 하려면 *DoNotIncludeArchive* 스위치를 포함할 수 있습니다. 앞서 설명한 것 처럼 자동 확장 보관 하는 경우 사용할 수는 사서함에 대해는 \* \* 검색 사서함 \* \* cmdlet을 보조 보관 사서함의 항목을 삭제 하지 않습니다. 자동 확장 하는 방법에 대 한 자세한 내용은 보관, [Office 365 무제한 보관의 개요](unlimited-archiving.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="06c66-p136">Note that items in the Recoverable Items folder in the user's primary archive mailbox will also be deleted when you run the \*\* Search-Mailbox \*\* cmdlet. To prevent this, you can include the  *DoNotIncludeArchive*  switch. And as previously stated, if auto-expanding archiving is enabled for the mailbox, the \*\* Search-Mailbox \*\* cmdlet doesn't deleted items in an auxiliary archive mailbox. For more information about auto-expanding archive, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="06c66-p137">( *SearchQuery* 매개 변수를 사용 하 여) 하 여 검색 쿼리를 포함 하는 경우 **검색 사서함** cmdlet은 검색 결과에 최대 10, 000 항목을 반환 합니다. 따라서 검색 쿼리를 포함 하는 경우에 10, 000 개 이상의 항목을 삭제 하려면 **사서함 검색** 명령을 여러 번 실행 해야할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p137">If you include a search query (by using the  *SearchQuery*  parameter), the **Search-Mailbox** cmdlet will return a maximum of 10,000 items in the search results. Therefore if you include a search query, you might have to run the **Search-Mailbox** command multiple times to delete more than 10,000 items.</span></span> 
  
<span data-ttu-id="06c66-p138">다음 예제에서는 이러한 각 옵션에 대 한 명령 구문을 보여줍니다. 사용 하 여 이러한 예제는 `-SearchQuery size>0` 복구 가능한 항목 폴더의 모든 하위 폴더에서 모든 항목을 삭제 하는 매개 변수 값입니다. 특정 조건에 맞는 항목만 삭제할 해야하는 경우에 날짜 범위 나 메시지의 제목 등의 다른 조건을 지정 하려면 *SearchQuery* 매개 변수를 사용할 수 있습니다. [SearchQuery 매개 변수를 사용 하는 다른 예제](#other-examples-of-using-the-searchquery-parameter) 아래를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="06c66-p138">The following examples show the command syntax for each of these options. These examples use the  `-SearchQuery size>0` parameter value, which deletes all items from all subfolders in the Recoverable Items folder. If you need to delete only items that match specific conditions, you can also use the  *SearchQuery*  parameter to specify other conditions, such as the subject of a message or a date range. See the [other examples of using the SearchQuery parameter](#other-examples-of-using-the-searchquery-parameter) below.</span></span> 
  
### <a name="example-1"></a><span data-ttu-id="06c66-255">예 1</span><span class="sxs-lookup"><span data-stu-id="06c66-255">Example 1</span></span>

<span data-ttu-id="06c66-p139">사용자의 복구 가능한 항목 폴더의 모든 항목 조직의 검색 사서함의 폴더에 복사 하는이 예제입니다. 이렇게 하면 영구적으로 삭제 하기 전에 항목을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p139">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox. This lets you review the items before you permanently delete them.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

<span data-ttu-id="06c66-p140">이전 예제에서는 사서함 검색에 항목을 복사할 필요가 없습니다. 모든 대상 사서함에 메시지를 복사할 수 있습니다. 그러나 잠재적으로 중요 한 사서함 데이터에 대 한 액세스를 방지 하려면 메시지 권한이 부여 된 직원에 게 제한 된 액세스 권한이 있는 사서함에 복사 하는 것이 좋습니다. 기본적으로 기본 검색 사서함에 대 한 액세스 제한 된 검색 관리 역할 그룹의 구성원에 게 Exchange 온라인 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p140">In the previous example, it isn't required to copy items to the Discovery Search Mailbox. You can copy messages to any target mailbox. However, to prevent access to potentially sensitive mailbox data, we recommend copying messages to a mailbox that has access restricted to authorized personnel. By default, access to the default Discovery Search Mailbox is restricted to members of the Discovery Management role group in Exchange Online.</span></span> 
  
### <a name="example-2"></a><span data-ttu-id="06c66-262">예 2</span><span class="sxs-lookup"><span data-stu-id="06c66-262">Example 2</span></span>

<span data-ttu-id="06c66-263">이 예에서는 조직의 검색 사서함의 폴더를 사용자의 복구 가능한 항목 폴더의 모든 항목을 복사 하 고 사용자의 복구 가능한 항목 폴더에서 항목을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-263">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox and then deletes the items from the user's Recoverable Items folder.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a><span data-ttu-id="06c66-264">예 3</span><span class="sxs-lookup"><span data-stu-id="06c66-264">Example 3</span></span>

<span data-ttu-id="06c66-265">대상 사서함으로 복사 하지 않고 사용자의 복구 가능한 항목 폴더의 모든 항목을 삭제 하는이 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-265">This example deletes all items in the user's Recoverable Items folder, without copying them to a target mailbox.</span></span> 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a><span data-ttu-id="06c66-266">SearchQuery 매개 변수를 사용 하는 다른 예제</span><span class="sxs-lookup"><span data-stu-id="06c66-266">Other examples of using the SearchQuery parameter</span></span>

<span data-ttu-id="06c66-p141">*SearchQuery* 매개 변수를 사용 하 여 특정 메시지를 찾으려면의 몇가지 예는 다음과 같습니다. 특정 항목을 검색 하려면 *SearchQuery* 매개 변수를 사용 하는 경우에 검색 결과 검토 하 고 다음 쿼리 수정 필요한 경우 검색 결과 삭제 하기 전에 수 있도록 대상 사서함에 검색 결과 복사 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p141">Here are a few examples of using the  *SearchQuery*  parameter to find specific messages. If you use the  *SearchQuery*  parameter to search for specific items, consider copying the search results to a target mailbox so that you can review the search results and then revise the query if necessary before you delete the results of a search.</span></span> 
  
<span data-ttu-id="06c66-269">제목 필드에서 특정 구를 포함 하는 메시지를 반환 하는이 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-269">This example returns messages that contain a specific phrase in the Subject field.</span></span>
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

<span data-ttu-id="06c66-270">이 예제에서는 지정된 된 날짜 범위 내에서 보낸 메시지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-270">This example returns messages that were sent within the specified date range.</span></span>
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
<span data-ttu-id="06c66-271">이 예제에서는 지정 된 사람에 게 보낸 메시지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-271">This example returns messages that were sent to the specified person.</span></span>

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a><span data-ttu-id="06c66-272">항목이 삭제 되 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-272">Verify that items were deleted</span></span>

<span data-ttu-id="06c66-p142">사서함의 복구 가능한 항목 폴더에서 항목을 성공적으로 삭제 했는지를 확인 하려면 cmdlet을 사용 **Get-mailboxfolderstatistics** Exchange 온라인 PowerShell 크기와 복구 가능한 항목 폴더의 항목 수를 확인 합니다. 1 단계에서에서 수집 된 내용으로 이러한 통계를 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p142">To verify that you've successfully deleted items from the Recoverable Items folder of a mailbox, use **Get-MailboxFolderStatistics** cmdlet in Exchange Online PowerShell to check the size and number of items in Recoverable Items folder. You can compare these statistics with the ones you collected in Step 1.</span></span> 
  
<span data-ttu-id="06c66-275">폴더와 사용자의 기본 사서함의 복구 가능한 항목 폴더에 하위 폴더에서 항목의 총 수와 현재 크기를 가져오려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-275">Run the following command in to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
<span data-ttu-id="06c66-276">폴더 및 사용자의 보관 사서함의 복구 가능한 항목 폴더에 하위 폴더의 크기와 총 항목 수를 가져오려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-276">Run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in the user's archive mailbox.</span></span> 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-6-revert-the-mailbox-to-its-previous-state"></a><span data-ttu-id="06c66-277">6 단계: 사서함을 이전 상태로 되돌리기</span><span class="sxs-lookup"><span data-stu-id="06c66-277">Step 6: Revert the mailbox to its previous state</span></span>

<span data-ttu-id="06c66-p143">마지막 단계를 이전 구성으로 다시 사서함으로 돌아가려면입니다. 즉, 2 단계에서에서 변경 되는 속성을 다시 설정 하 고 3 단계에서에서 제거 된 보류를 다시 적용 합니다. 이는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p143">The final step is to revert the mailbox back to its previous configuration. This means resetting the properties that you changed in Step 2 and re-applying the holds that you removed in Step 3. This includes:</span></span>
  
- <span data-ttu-id="06c66-p144">이전 값으로 다시 삭제 된 항목 보존 기간을 변경 합니다. 또는 남겨둘 수 있습니다 Exchange에서 30 일, 최대 값으로 설정이 온라인 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p144">Changing the deleted item retention period back to its previous value. Alternatively, you can just leave this set to 30 days, the maximum value in Exchange Online.</span></span>
    
- <span data-ttu-id="06c66-283">단일 항목 복구를 다시 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-283">Re-enabling single Item recovery.</span></span>
    
- <span data-ttu-id="06c66-284">다시 소유자가 사서함에 액세스할 수 있도록 클라이언트 액세스 방법을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-284">Re-enabling the client access methods so that the owner can access their mailbox.</span></span>
    
- <span data-ttu-id="06c66-285">보류 및 제거 하는 Office 365 보존 정책을 다시 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-285">Re-applying the holds and Office 365 retention policies that you removed.</span></span>
    
- <span data-ttu-id="06c66-286">다시 사용 하도록 설정의 관리 되는 폴더 도우미가 사서함 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-286">Re-enabling the Managed Folder Assistant to process the mailbox.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="06c66-287">다시 보류 또는 Office 365를 적용 한 후 24 시간은 때까지 대기 하는 것이 좋습니다 보존 정책 (및 원본 위치에 있는지 확인 (영문))는 관리 되는 폴더 도우미는 사서함을 처리를 다시 활성화 하기 전에 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-287">We recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant to process the mailbox.</span></span> 
  
<span data-ttu-id="06c66-288">Exchange Online PowerShell에서 (지정된 된 시퀀스)에서 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-288">Perform the following steps (in the specified sequence) in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="06c66-p145">원래 값 삭제 된 항목 보존 기간을 변경 하려면 다음 명령을 다시 실행 합니다. 이전 설정이 30 일 보다 작은; 것이 가정 예: 14 일입니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p145">Run the following command to change the deleted item retention period back to its original value. This assumes that the previous setting is less than 30 days; for example 14 days.</span></span> 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. <span data-ttu-id="06c66-291">단일 항목 복구를 다시 사용 하도록 설정 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-291">Run the following command to re-enable single item recovery.</span></span>
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. <span data-ttu-id="06c66-292">다시 사서함에 모든 클라이언트 액세스 메서드를 사용 하도록 설정 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-292">Run the following command to re-enable all client access methods to the mailbox.</span></span>
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. <span data-ttu-id="06c66-p146">3 단계에서에서 제거 된 보류를 다시 적용 합니다. 보류의 유형에 따라 다음 절차 중 하나를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p146">Re-apply the holds that you removed in Step 3. Depending on the type of hold, use one of the following procedures.</span></span>
    
    <span data-ttu-id="06c66-295">**소송 보존**</span><span class="sxs-lookup"><span data-stu-id="06c66-295">**Litigation Hold**</span></span>
    
    <span data-ttu-id="06c66-296">사서함에 대 한 소송 보존을 다시 사용 하도록 설정 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-296">Run the following command to re-enable a Litigation Hold for the mailbox.</span></span>
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    <span data-ttu-id="06c66-297">**원본 위치 유지**</span><span class="sxs-lookup"><span data-stu-id="06c66-297">**In-Place Hold**</span></span>
    
    <span data-ttu-id="06c66-298">사서함에 다시 추가 원본 위치 유지를 EAC (또는 Exchange Online PowerShell)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-298">Use the EAC (or Exchange Online PowerShell) to add the mailbox back to the In-Place Hold.</span></span> 
    
    <span data-ttu-id="06c66-299">**특정 사서함에 적용 하는 office 365 보존 정책**</span><span class="sxs-lookup"><span data-stu-id="06c66-299">**Office 365 retention policies applied to specific mailboxes**</span></span>
    
    <span data-ttu-id="06c66-p147">보안을 사용 하 여 &amp; 준수 센터 사서함 Office 365 보존 정책에 다시 추가 합니다. **날짜 관리 방식** 으로 이동 \> 보안에서 **보존** 페이지 &amp; 준수 센터 보존 정책을 편집 하 고 사서함 보존 정책에 적용 되는 받는 사람 목록에 다시 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p147">Use the Security &amp; Compliance Center to add the mailbox back to the Office 365 retention policy. Go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the retention policy, and add the mailbox back to the list of recipients that the retention policy is applied to.</span></span> 
    
    <span data-ttu-id="06c66-302">**조직 전체의 Office 365 보존 정책**</span><span class="sxs-lookup"><span data-stu-id="06c66-302">**Organization-wide Office 365 retention policies**</span></span>
    
    <span data-ttu-id="06c66-p148">정책에서 제외 하 여 한 조직 수준의 또는 Exchange 전체 보존 정책을 제거 하는 경우 다음 사용 하 여 보안 &amp; 준수 센터의 목록에서 사서함을 제거 하려면 사용자를 제외 합니다. **날짜 관리 방식** 으로 이동 \> 보안에서 **보존** 페이지 &amp; 준수 센터 조직 전체의 보존 정책을 편집 하 고 제외 된 받는 사람 목록에서 사서함을 제거 합니다. 이 수행 하는 사용자의 사서함에 보존 정책을 다시 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p148">If you removed an organization-wide or Exchange-wide retention policy by excluding it from the policy, then use the Security &amp; Compliance Center to remove the mailbox from the list of excluded users. Go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the organization-wide retention policy, and remove the mailbox from the list of excluded recipients. Doing this will re-apply the retention policy to the user's mailbox.</span></span> 
    
    <span data-ttu-id="06c66-306">**eDiscovery 사례를 포함 하**</span><span class="sxs-lookup"><span data-stu-id="06c66-306">**eDiscovery case holds**</span></span>
    
    <span data-ttu-id="06c66-p149">보안을 사용 하 여 &amp; 사서함을 추가 하려면 준수 센터 eDiscovery 사례와 관련 된 보류를 백업 합니다. 이동 하는 **검색 &amp; 조사** \> 보안에서 **eDiscovery** 페이지 &amp; 준수 센터 대/소문자를 열고 사서함 보류에 다시 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p149">Use the Security &amp; Compliance Center to add the mailbox back the hold that's associated with an eDiscovery case. Go to the **Search &amp; investigation** \> **eDiscovery** page in the Security &amp; Compliance Center, open the case, and add the mailbox back to the hold.</span></span> 
    
5. <span data-ttu-id="06c66-p150">관리 되는 폴더 도우미는 사서함을 다시 처리할 수 있도록 하려면 다음 명령을 실행 합니다. 듯이 다시 보류 또는 Office 365를 적용 한 후 24 시간은 때까지 대기 하는 것이 좋습니다 보존 정책 (및 원본 위치에 있는지 확인 (영문)) 관리 되는 폴더 도우미를 다시 활성화 하기 전에 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p150">Run the following command to allow the Managed Folder Assistant to process the mailbox again. As previously stated, we recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. <span data-ttu-id="06c66-311">사서함을 이전 구성으로 다시 되돌렸습니다 있는지를 확인 하려면 다음 명령을 실행 수 있으며 다음 설정의 1 단계에서에서 수집 하는 것과 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-311">To verify that the mailbox has been reverted back to its previous configuration, you can run the following commands and then compare the settings to the ones that you collected in Step 1.</span></span>

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a><span data-ttu-id="06c66-312">추가 정보</span><span class="sxs-lookup"><span data-stu-id="06c66-312">More information</span></span>

<span data-ttu-id="06c66-p151">다음은 다양 한 유형의 **Get-mailbox** 또는 **Get-organizationconfig** cmdlet을 실행 하는 경우 *InPlaceHolds* 속성의 값에 따라 보류를 식별 하는 방법에 설명 하는 테이블입니다. 자세한 내용은 [유형을 식별 하는 방법을 hold Exchange Online 사서함에 배치](identify-a-hold-on-an-exchange-online-mailbox.md)를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p151">Here's a table that describes how to identify different types of holds based on the values in the  *InPlaceHolds*  property when you run the **Get-Mailbox** or **Get-OrganizationConfig** cmdlets. For more detailed information, see [How to identify the type of hold placed on an Exchange Online mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>

<span data-ttu-id="06c66-315">앞부분에 설명 하 고, 모든 보류를 제거 하려면 있고 하기 전에 사서함에서 Office 365 보존 정책이 성공적으로 복구 가능한 항목 폴더에서 항목을 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-315">As previously explained, you have to remove all holds and Office 365 retention policies from a mailbox before you can successfully delete items in the Recoverable Items folder.</span></span> 
  
|<span data-ttu-id="06c66-316">**종류를 유지 합니다.**</span><span class="sxs-lookup"><span data-stu-id="06c66-316">**Hold type**</span></span>|<span data-ttu-id="06c66-317">**예제 값**</span><span class="sxs-lookup"><span data-stu-id="06c66-317">**Example value**</span></span>|<span data-ttu-id="06c66-318">**보류를 식별 하는 방법**</span><span class="sxs-lookup"><span data-stu-id="06c66-318">**How to identify the hold**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="06c66-319">소송 보존</span><span class="sxs-lookup"><span data-stu-id="06c66-319">Litigation Hold</span></span>  <br/> | `True` <br/> |<span data-ttu-id="06c66-320">*LitigationHoldEnabled* 속성이로 설정 된 `True`합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-320">The  *LitigationHoldEnabled*  property is set to  `True`.</span></span>  <br/> |
|<span data-ttu-id="06c66-321">원본 위치 유지</span><span class="sxs-lookup"><span data-stu-id="06c66-321">In-Place Hold</span></span>  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |<span data-ttu-id="06c66-p152">*InPlaceHolds* 속성의 사서함에 배치 되는 원본 위치 유지의 GUID를 포함 합니다. 이 In-place Hold GUID를 접두사로 시작 되지 않으면 때문에 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p152">The  *InPlaceHolds*  property contains the GUID of the In-Place Hold that's placed on the mailbox. You can tell this is an In-Place Hold because the GUID doesn't start with a prefix.  </span></span><br/> <span data-ttu-id="06c66-324">사용할 수는 ' Get-mailboxsearch InPlaceHoldIdentity<hold GUID></span><span class="sxs-lookup"><span data-stu-id="06c66-324">You can use the  \`Get-MailboxSearch -InPlaceHoldIdentity <hold GUID></span></span> | <span data-ttu-id="06c66-325">FL' 사서함에서 원본 위치 유지 하는 방법에 대 한 정보를 얻을 수 있는 Exchange Online PowerShell에서 명령 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-325">FL\` command in Exchange Online PowerShell to get information about the In-Place Hold on the mailbox.</span></span>  <br/> |
| <span data-ttu-id="06c66-326">보안에서 office 365 보존 정책을 &amp; 준수 센터 특정 사서함에 적용</span><span class="sxs-lookup"><span data-stu-id="06c66-326">Office 365 retention policies in the Security &amp; Compliance Center applied to specific mailboxes</span></span>  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> <span data-ttu-id="06c66-327">또는</span><span class="sxs-lookup"><span data-stu-id="06c66-327">or</span></span>  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |<span data-ttu-id="06c66-p153">**Get-mailbox** cmdlet을 실행 하는 경우 *InPlaceHolds* 속성은 사서함에 적용 된 Office 365의 guid가 보존 정책도 포함 합니다. 으로 시작 하는 GUID 때문에 보존 정책을 식별할 수는 `mbx` 접두사입니다. 보존 정책의 GUID로 시작 하는 경우는 `skp` 비즈니스 대화에 대 한 보존 정책을 Skype에 적용 되는지 나타내는 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p153">When you run the **Get-Mailbox** cmdlet, the  *InPlaceHolds*  property also contains GUIDs of Office 365 retention policies applied to the mailbox. You can identify retention policies because the GUID starts with the  `mbx` prefix. Note that if the GUID of the retention policy starts with the  `skp` prefix, that indicates that the retention policy is applied to Skype for Business conversations.  </span></span><br/> <span data-ttu-id="06c66-331">사서함에 적용 되는 Office 365 identity 보존 정책, 보안에서 다음 명령을 실행 &amp; 준수 센터 PowerShell:</span><span class="sxs-lookup"><span data-stu-id="06c66-331">To identity the Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell:</span></span> <br/> <br/><span data-ttu-id="06c66-332">' Get RetentionCompliancePolicy<retention policy GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="06c66-332">\`Get-RetentionCompliancePolicy <retention policy GUID without prefix></span></span> | <span data-ttu-id="06c66-333">FL 이름`<br/><br/>Be sure to remove the  `mbx` or  `skp'이 명령을 실행 하면 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-333">FL Name`<br/><br/>Be sure to remove the  `mbx` or  `skp\` prefix when you run this command.</span></span>  <br/> |
|<span data-ttu-id="06c66-334">보안에서 조직 전체의 Office 365 보존 정책 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="06c66-334">Organization-wide Office 365 retention policies in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="06c66-335">값 없음</span><span class="sxs-lookup"><span data-stu-id="06c66-335">No value</span></span>  <br/> <span data-ttu-id="06c66-336">또는</span><span class="sxs-lookup"><span data-stu-id="06c66-336">or</span></span>  <br/>  <span data-ttu-id="06c66-337">`-mbxe9b52bf7ab3b46a286308ecb29624696`(사서함은 조직 수준의 정책에서 제외를 나타냄)</span><span class="sxs-lookup"><span data-stu-id="06c66-337">`-mbxe9b52bf7ab3b46a286308ecb29624696` (indicates that the mailbox is excluded from an organization-wide policy)</span></span>  <br/> |<span data-ttu-id="06c66-338">*InPlaceHolds* 속성이 비어 있는 **Get-mailbox** cmdlet을 실행 하는 경우, 하는 경우에 여전히 있을 수 있습니다 하나 이상의 조직 전체의 Office 365 보존 정책 사서함에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-338">Even if the  *InPlaceHolds*  property is empty when you run the **Get-Mailbox** cmdlet, there still might be one or more organization-wide Office 365 retention policies applied to the mailbox.</span></span>  <br/> <span data-ttu-id="06c66-339">이 확인 하려면 실행할 수 있습니다는 ' Get-organizationconfig</span><span class="sxs-lookup"><span data-stu-id="06c66-339">To verify this, you can run the  \`Get-OrganizationConfig</span></span> | <span data-ttu-id="06c66-340">FL InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> To identity the organization-wide Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell: <br/><br/> `Get RetentionCompliancePolicy<retention policy GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="06c66-340">FL InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> To identity the organization-wide Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell: <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix></span></span> | <span data-ttu-id="06c66-341">FL 이름`<br/><br/>Note that if a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy is displayed in the  *InPlaceHolds*  property of the user's mailbox when you run the **Get-Mailbox** cmdlet; it's identified by the prefix  `-mbx`; for example,  `-mbxe9b52bf7ab3b46a286308ecb29624696'</span><span class="sxs-lookup"><span data-stu-id="06c66-341">FL Name`<br/><br/>Note that if a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy is displayed in the  *InPlaceHolds*  property of the user's mailbox when you run the **Get-Mailbox** cmdlet; it's identified by the prefix  `-mbx`; for example,  `-mbxe9b52bf7ab3b46a286308ecb29624696\`</span></span> <br/> |
|<span data-ttu-id="06c66-342">eDiscovery 사례 유지 (영문) 보안 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="06c66-342">eDiscovery case hold in the Security &amp; Compliance Center</span></span>  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |<span data-ttu-id="06c66-p154">*InPlaceHolds* 속성은 또한 보안에서 eDiscovery 사례와 관련 된 모든 보류의 GUID가 포함 &amp; 준수 센터의 사서함에 배치 될 수입니다. 이런 현상이 발생 eDiscovery 사례 보류도 시작 하는 GUID를 알 수는 `UniH` 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="06c66-p154">The  *InPlaceHolds*  property also contains the GUID of any hold associated with an eDiscovery case in the Security &amp; Compliance Center that might be placed on the mailbox. You can tell this is an eDiscovery case hold because the GUID starts with the  `UniH` prefix.  </span></span><br/> <span data-ttu-id="06c66-p155">사용할 수 있습니다는 `Get-CaseHoldPolicy` 보안에서 cmdlet &amp; 준수 센터 PowerShell 보류의 사서함에 연결 된 eDiscovery 사례에 대 한 정보를 얻을 수 있습니다. 명령을 실행할 수 등 ' Get CaseHoldPolicy<hold GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="06c66-p155">You can use the  `Get-CaseHoldPolicy` cmdlet in Security &amp; Compliance Center PowerShell to get information about the eDiscovery case that the hold on the mailbox is associated with. For example, you can run the command  \`Get-CaseHoldPolicy <hold GUID without prefix></span></span> | <span data-ttu-id="06c66-347">FL 이름` to display the name of the case hold that's on the mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the mailbox is associated with, run the following commands:<br/><br/>`$CaseHold Get CaseHoldPolicy = <hold GUID without prefix> `<br/><br/>`Get ComplianceCase $CaseHold.CaseId</span><span class="sxs-lookup"><span data-stu-id="06c66-347">FL Name` to display the name of the case hold that's on the mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the mailbox is associated with, run the following commands:<br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/>`Get-ComplianceCase $CaseHold.CaseId</span></span> | <span data-ttu-id="06c66-348">FL 이름 '</span><span class="sxs-lookup"><span data-stu-id="06c66-348">FL Name\`</span></span>


