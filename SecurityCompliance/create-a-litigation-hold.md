---
title: 소송 보존 만들기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: e4cb614167f89cb6e99d96aa94027ba90d86543e
ms.sourcegitcommit: 1658be51e2c21ed23bc4467a98af74300a45b975
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/26/2019
ms.locfileid: "30862410"
---
# <a name="create-a-litigation-hold"></a><span data-ttu-id="17834-102">소송 보존 만들기</span><span class="sxs-lookup"><span data-stu-id="17834-102">Create a Litigation Hold</span></span>

<span data-ttu-id="17834-103">사서함에 대 한 소송 보존을 적용 하 여 삭제 된 항목을 비롯 한 모든 사서함 콘텐츠를 보존할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17834-103">You can place a mailbox on Litigation Hold to retain all mailbox content, including deleted items and the original versions of modified items.</span></span> <span data-ttu-id="17834-104">사용자 사서함에 소송 보존을 적용 하면 사용자의 보관 사서함에 있는 콘텐츠 (사용 하도록 설정 된 경우)도 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-104">When you place a user mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also retained.</span></span> <span data-ttu-id="17834-105">보류를 만들 때 삭제 및 수정 된 항목을 지정한 기간 동안 보존 하 고 사서함에서 영구적으로 삭제할 수 있도록 보존 기간 ( *시간 기반 보존*이 라고도 함)을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17834-105">When you create a hold, you can specify a hold duration (also called a *time-based hold*) so that deleted and modified items are retained for a specified period and then permanently deleted from the mailbox.</span></span> <span data-ttu-id="17834-106">또는 콘텐츠를 무기한 보존 ( *무기한 보류*라고 함) 하거나 소송 보존을 제거할 때까지 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-106">Or you can just retain content indefinitely (called an *infinite hold*) or until the Litigation Hold is removed.</span></span> <span data-ttu-id="17834-107">보존 기간을 지정 하는 경우에는 메시지가 수신 되거나 사서함 항목이 만들어진 날짜를 통해 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-107">If you do specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> 
  
<span data-ttu-id="17834-108">소송 보존을 만들 때 수행 되는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="17834-108">Here's what happens when you create a Litigation Hold.</span></span>
  
- <span data-ttu-id="17834-109">사용자가 영구적으로 삭제 한 항목은 보류 기간 동안 사용자의 사서함에 있는 복구할 수 있는 항목 폴더에 보관 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-109">Items that are permanently deleted by the user are retained in the Recoverable Items folder in the user's mailbox for the duration of the hold.</span></span>
    
- <span data-ttu-id="17834-110">사용자가 복구 가능한 항목 폴더에서 제거 된 항목은 보류 기간 동안 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-110">Items that are purged from the Recoverable Items folder by the user are retained for the duration of the hold.</span></span>
    
- <span data-ttu-id="17834-111">복구 가능한 항목 폴더의 저장소 할당량은 30gb에서 110 GB로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-111">The storage quota for the Recoverable Items folder is increased from 30 GB to 110 GB.</span></span>
    
- <span data-ttu-id="17834-112">사용자의 기본 및 보관 사서함에 있는 항목은 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-112">Items in the user's primary and the archive mailboxes are retained</span></span>
    
## <a name="before-you-begin"></a><span data-ttu-id="17834-113">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="17834-113">Before you begin</span></span>

- <span data-ttu-id="17834-114">exchange online 사서함에 소송 보존을 적용 하려면 exchange online 계획 2 라이선스를 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-114">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online Plan 2 license.</span></span> <span data-ttu-id="17834-115">사서함에 Exchange online 계획 1 라이선스가 할당 되는 경우이를 보류 상태로 설정 하려면 별도의 exchange online 보관 라이선스를 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-115">If a mailbox is assigned an Exchange Online Plan 1 license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    

## <a name="place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="17834-116">사서함을 소송 자료 보존으로 설정</span><span class="sxs-lookup"><span data-stu-id="17834-116">Place a mailbox on Litigation Hold</span></span>

<span data-ttu-id="17834-117">다음은 Exchange 관리 센터를 사용 하 여 사서함에 소송 보존을 적용 하는 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="17834-117">Here are the steps to place a mailbox on Litigation Hold using the Exchange admin center.</span></span>

1. <span data-ttu-id="17834-118">로 이동 [https://outlook.office.com/ecp](https://outlook.office.com/ecp) 하 고 전역 관리자 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-118">Go to [https://outlook.office.com/ecp](https://outlook.office.com/ecp) and sign in using your global administrator account.</span></span>

2. <span data-ttu-id="17834-119">왼쪽 탐색 창에서 **받는 사람 > 사서함** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-119">Click **Recipients > Mailboxes** in the left navigation pane.</span></span>

3. <span data-ttu-id="17834-120">소송 보존에 적용할 사서함을 선택 하 고 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-120">Select the mailbox that you want to place on Litigation Hold, and then click **Edit**.</span></span>

4. <span data-ttu-id="17834-121">사서함 속성 페이지에서 **사서함 기능**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-121">On the mailbox properties page, click **Mailbox features**.</span></span>
    
5. <span data-ttu-id="17834-122">**소송 보존: 사용 안 함**에서 **사용** 을 클릭 하 여 사서함을 소송 보존 상태로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-122">Under **Litigation hold: Disabled**, click **Enable** to place the mailbox on Litigation Hold.</span></span>
    
6. <span data-ttu-id="17834-123">**소송 보존** 페이지에서 다음 선택적 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-123">On the **Litigation hold** page, enter the following optional information:</span></span> 
    
    - <span data-ttu-id="17834-124">**소송 보존 기간 (일)** -이 상자를 사용 하 여 시간 기반 보존을 만들고 사서함이 소송 보존 상태에 있을 때 사서함 항목이 보관 되는 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-124">**Litigation hold duration (days)** - Use this box to create a time-based hold and specify how long mailbox items are held when the mailbox is placed on Litigation Hold.</span></span> <span data-ttu-id="17834-125">기간은 사서함 항목이 수신되거나 만들어진 날짜부터 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-125">The duration is calculated from the date a mailbox item is received or created.</span></span> <span data-ttu-id="17834-126">특정 항목에 대해 보존 기간이 만료 되 면 해당 항목은 더 이상 보존 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17834-126">When the hold duration expires for a specific item, that item will no longer be preserved.</span></span> <span data-ttu-id="17834-127">이 상자를 비워 두면 항목이 무기한 보존 되거나 보류가 제거 될 때까지 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-127">If you leave this box blank, items are preserved indefinitely or until the hold is removed.</span></span> <span data-ttu-id="17834-128">기간을 지정 하려면 days를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-128">Use days to specify the duration.</span></span>
    
    - <span data-ttu-id="17834-129">**참고** -이 상자를 사용 하 여 사서함이 소송 보존 상태 인지를 사용자에 게 알립니다.</span><span class="sxs-lookup"><span data-stu-id="17834-129">**Note** - Use this box to inform the user their mailbox is on Litigation Hold.</span></span> <span data-ttu-id="17834-130">메모는 Outlook 2010 이상 버전을 사용 중인 경우 사용자 사서함의 계정 정보 페이지에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-130">The note will appear on the Account Information page in the user's mailbox if they're using Outlook 2010 or later.</span></span> <span data-ttu-id="17834-131">사용자는이 페이지에 액세스 하 여 Outlook에서 **파일** 을 클릭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17834-131">To access this page, users can click **File** in Outlook.</span></span>
    
    - <span data-ttu-id="17834-132">**URL** -소송 보존에 대 한 자세한 내용은이 상자를 사용 하 여 사용자에 게 웹 사이트를 안내 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-132">**URL** - Use this box to direct the user to a website for more information about Litigation Hold.</span></span> <span data-ttu-id="17834-133">이 URL은 사용자 사서함의 계정 정보 페이지에서 Outlook 2010 이상 버전을 사용 하는 경우에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-133">This URL appears on the Account Information page in the user's mailbox if they are using Outlook 2010 or later.</span></span> <span data-ttu-id="17834-134">사용자는이 페이지에 액세스 하 여 Outlook에서 **파일** 을 클릭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17834-134">To access this page, users can click **File** in Outlook..</span></span>

7. <span data-ttu-id="17834-135">**소송 보존** 페이지에서 **저장** 을 클릭 한 다음 사서함 속성 페이지에서 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-135">Click **Save** on the **Litigation hold** page, and then click **Save** on the mailbox properties page.</span></span>

### <a name="create-a-litigation-hold-using-powershell"></a><span data-ttu-id="17834-136">PowerShell을 사용 하 여 소송 보존 만들기</span><span class="sxs-lookup"><span data-stu-id="17834-136">Create a Litigation Hold using PowerShell</span></span>

<span data-ttu-id="17834-137">[Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)에서 다음 명령을 실행 하 여 소송 보존을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17834-137">You can also create a Litigation Hold by running the following command in [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell):</span></span>

```
Set-Mailbox <username> -LitigationHoldEnabled $true
```

<span data-ttu-id="17834-138">이전 명령은 보존 기간이 지정 되지 않았으므로 항목을 무기한 보존 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-138">The previous command preserves items indefinitely because the hold duration isn't specified.</span></span> <span data-ttu-id="17834-139">다음 명령을 사용 하 여 시간 기반 보존을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17834-139">To created a time-based hold, using the following command:</span></span>

```
Set-Mailbox <username> -LitigationHoldEnabled $true -LitigationHoldDuration <number of days>
```

<span data-ttu-id="17834-140">자세한 내용은 [Set-Mailbox](https://docs.microsoft.com/en-us/powershell/module/exchange/mailboxes/set-mailbox)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="17834-140">For more information, see [Set-Mailbox](https://docs.microsoft.com/en-us/powershell/module/exchange/mailboxes/set-mailbox).</span></span>

## <a name="how-does-litigation-hold-work"></a><span data-ttu-id="17834-141">소송 보존의 작동 방식</span><span class="sxs-lookup"><span data-stu-id="17834-141">How does Litigation Hold work?</span></span>

<span data-ttu-id="17834-142">일반 삭제 된 항목 워크플로에서 사서함 항목은 사용자가 영구적으로 삭제 (Shift + Delete) 되거나 지운 편지함 폴더에서 삭제 될 때 복구 가능한 항목 폴더의 삭제 하위 폴더로 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-142">In the normal deleted item workflow, a mailbox item is moved to the Deletions subfolder in the Recoverable Items folder when a user permanently deletes it (Shift + Delete) or deletes it from the Deleted Items folder.</span></span> <span data-ttu-id="17834-143">삭제 보존 작업을 사용 하 여 구성 된 보존 태그 인 삭제 정책은 보존 기간이 만료 되 면 항목을 삭제 하위 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-143">A deletion policy (which is a retention tag configured with a Delete retention action) also moves items to the Deletions subfolder when the retention period expires.</span></span> <span data-ttu-id="17834-144">사용자가 복구 가능한 항목 폴더에서 항목을 제거 하거나 삭제 된 항목 보존 기간이 항목에 대해 만료 되는 경우 복구 가능한 항목 폴더의 제거 하위 폴더로 이동 되 고 영구 삭제 되도록 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-144">When a user purges an item in the Recoverable Items folder or when the deleted item retention period expires for an item, it's moved to the Purges subfolder in the Recoverable Items folder and marked for permanent deletion.</span></span> <span data-ttu-id="17834-145">다음에는 MFA (관리 되는 폴더 도우미)에서 사서함을 처리할 때 Exchange에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-145">It will be purged from Exchange the next time the mailbox is processed by the Managed Folder Assistant (MFA).</span></span>

<span data-ttu-id="17834-146">사서함을 소송 보존 상태로 설정 하면 제거 하위 폴더의 항목은 소송 보존에 지정 된 보존 기간 동안 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-146">When a mailbox is placed on Litigation Hold, items in the Purges subfolder are preserved for the hold duration specified by the Litigation Hold.</span></span> <span data-ttu-id="17834-147">보존 기간은 항목이 수신 되거나 만들어진 원래 날짜 로부터 계산 되며, 제거 하위 폴더의 항목이 보관 되는 기간을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="17834-147">The hold duration is calculated from the original date an item was received or created, and defines how long items in the Purges subfolder are held.</span></span> <span data-ttu-id="17834-148">제거 하위 폴더에 있는 항목에 대 한 보존 기간이 만료 되 면 해당 항목은 영구 삭제 되도록 표시 되며 다음에는 해당 사서함이 MFA에 의해 처리 될 때 Exchange에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-148">When the hold duration expires for an item in the Purges subfolder, the item is marked for permanent deletion and will be purged from Exchange the next time the mailbox is processed by the MFA.</span></span> <span data-ttu-id="17834-149">사서함에 무기한 보류가 적용 되 면 항목은 제거 된 하위 폴더에서 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17834-149">If an indefinite hold is placed on a mailbox, items will never be purged from the Purges subfolder.</span></span>

<span data-ttu-id="17834-150">다음 그림에서는 복구 가능한 항목 폴더 및 보류 워크플로 프로세스의 하위 폴더를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="17834-150">The following illustration shows the subfolders in the Recoverable Items folders and the hold workflow process.</span></span>

![소송 보존 수명 주기](media/LitigationHoldLifeCycle.png)

> [!NOTE]
> <span data-ttu-id="17834-152">eDiscovery 사례와 관련 된 보류를 사서함에 저장 하면 제거 된 항목은 삭제 하위 폴더에서 discoveryholds 하위 폴더로 이동 되 고 사서함이 eDiscovery 보류에서 릴리스될 때까지 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17834-152">If a hold associated with an eDiscovery case is placed on a mailbox, purged items are moved from the Deletions subfolder to the DiscoveryHolds subfolder and are preserved until the mailbox is released from the eDiscovery hold.</span></span>
  