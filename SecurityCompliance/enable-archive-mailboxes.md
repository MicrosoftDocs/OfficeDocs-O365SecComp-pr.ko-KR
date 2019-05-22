---
title: 보안 및 준수 센터에서 보관 사서함 사용
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Office 365의 보안 및 규정 준수 센터를 사용하면 조직의 메시지 보존, 전자 검색 및 보유 요구 사항을 지원하기 위해 보관 사서함을 사용할 수 있습니다.
ms.openlocfilehash: 5cf399b311b6c342aff2d84477edaa945f8e0cd4
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153290"
---
# <a name="enable-archive-mailboxes-in-the-security--compliance-center"></a><span data-ttu-id="9adf4-103">보안 및 준수 센터에서 보관 사서함 사용</span><span class="sxs-lookup"><span data-stu-id="9adf4-103">Enable archive mailboxes in the Security & Compliance Center</span></span>
  
<span data-ttu-id="9adf4-104">Office 365(내부 보관이라고도 함)의 보관은 사용자에게 추가 사서함 저장소 공간을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-104">Archiving in Office 365 (also called In-Place Archiving) provides users with additional mailbox storage space.</span></span> <span data-ttu-id="9adf4-105">보관 사서함을 설정하면 사용자가 웹의 Microsoft Outlook 및 Outlook(이전의 Outlook Web App)을 사용하여 보관 사서함에 메시지를 액세스하고 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-105">After you turn on archive mailboxes, users can access and store messages in their archive mailboxes by using Microsoft Outlook and Outlook on the web (formerly known as Outlook Web App).</span></span> <span data-ttu-id="9adf4-106">또한 사용자는 기본 사서함과 보관 사서함 간에 메시지를 이동하거나 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-106">Users can manually move or copy messages from their primary mailbox to their archive mailbox.</span></span> <span data-ttu-id="9adf4-107">또한 지운 편지함 복구 도구를 사용하여 보관 사서함의 복구 가능한 항목 폴더에서 삭제된 항목을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-107">They can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
> [!TIP]
> <span data-ttu-id="9adf4-108">Office 365는 자동 확장 보관 기능을 통해 무제한의 보관 저장소를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-108">Office 365 provides an unlimited amount of archive storage with the auto-expanding archiving feature.</span></span> <span data-ttu-id="9adf4-109">자동 확장 보관 기능이 켜져 있고 사용자 보관 사서함의 초기 저장소 할당량에 도달하면 Office 365가 자동으로 추가 저장 공간을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-109">When auto-expanding archiving is turned on, and then the initial storage quota in a user's archive mailbox is reached, Office 365 automatically adds additional storage space.</span></span> <span data-ttu-id="9adf4-110">즉, 사용자가 사서함 저장 공간을 모두 소모하지 않으므로 처음에 보관 사서함을 사용하도록 설정하고 조직의 자동 확장 보관을 설정한 후에는 아무 것도 관리할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-110">This means that users won't run out of mailbox storage space and you won't have to manage anything after you initially enable the archive mailbox and turn on auto-expanding archiving for your organization.</span></span> <span data-ttu-id="9adf4-111">자세한 내용은 [Office 365 무제한 보관의 개요](unlimited-archiving.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9adf4-111">For more information, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="9adf4-112">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="9adf4-112">Before you begin</span></span>

<span data-ttu-id="9adf4-113">보관 사서함을 사용하거나 사용하지 않도록 설정하려면 Exchange Online에서 메일받는 사람 역할을 할당받아야합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-113">You have to be assigned the Mail Recipients role in Exchange Online to enable or disable archive mailboxes.</span></span> <span data-ttu-id="9adf4-114">기본적으로 이 역할은 Exchange 관리 센터의 **사용 권한** 페이지에서 받는 사람 관리 및 조직 관리 역할 그룹에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-114">By default, this role is assigned to the Recipient Management and Organization Management role groups on the **Permissions** page in the Exchange admin center.</span></span> <span data-ttu-id="9adf4-115">보안 및 준수 센터의 **보관** 페이지가 보이지 않으면 관리자에게 필요한 권한을 할당해 줄 것을 요청하십시오.</span><span class="sxs-lookup"><span data-stu-id="9adf4-115">If you don't see the **Archive** page in the Security & Compliance Center, ask your administrator to assign you the necessary permissions.</span></span> 
  
## <a name="enable-an-archive-mailbox"></a><span data-ttu-id="9adf4-116">보관 사서함 사용</span><span class="sxs-lookup"><span data-stu-id="9adf4-116">Enable an archive mailbox</span></span>
  
1. <span data-ttu-id="9adf4-117">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-117">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="9adf4-118">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-118">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="9adf4-119">보안 및 규정 준수 센터의 왼쪽 창에서 **데이터 관리** \> **보관**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-119">In the left pane of the Security & Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="9adf4-120">**보관** 페이지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-120">The **New search** page is displayed.</span></span> <span data-ttu-id="9adf4-121">**보관 사서함** 열은 각 사용자의 보관 사서함이 사용되도록 설정되었는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-121">The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="9adf4-122">사서함 목록에서 보관 사서함을 사용하도록 설정할 사용자를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-122">In the list of mailboxes, select the user that you want to enable the archive mailbox for.</span></span>
    
    ![선택한 사용자의 세부 정보 창에서 사용을 클릭하여 보관 사서함을 사용하도록 설정](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. <span data-ttu-id="9adf4-124">선택한 사용자의 세부 정보 창에서 **사용**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-124">In the details pane for the selected user, click **Enable**.</span></span> 
    
    <span data-ttu-id="9adf4-125">보관 사서함이 사용되도록 설정된다는 경고가 표시되고, 사서함에 할당된 보존 정책보다 오래된 사용자의 사서함 항목이 새 보관 사서함으로 이동됩니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-125">A warning is displayed saying that if you enable the archive mailbox, items in the user's mailbox that are older than the archiving policy assigned to the mailbox will be moved to the new archive mailbox.</span></span> <span data-ttu-id="9adf4-126">ExchangeOnline 사서함에 할당된 보존 정책에 속하는 기본 보관 정책은 사용자가 항목을 사서함으로 전달하거나 만든 날짜로부터 2년 후에 항목을 보관 사서함으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-126">The default archive policy that is part of the retention policy assigned to Exchange Online mailboxes moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user.</span></span> <span data-ttu-id="9adf4-127">자세한 내용은 이 문서의 **추가 정보** 섹션을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="9adf4-127">For more information, see the **More info** section in this article.</span></span> 
    
6. <span data-ttu-id="9adf4-128">**예**를 클릭하여 보관 사서함을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-128">Click **Yes** to enable the archive mailbox.</span></span> 
    
    <span data-ttu-id="9adf4-129">보관 사서함을 만드는 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-129">It might take a few moments to create the archive mailbox.</span></span> <span data-ttu-id="9adf4-130">생성되면 **보관 사서함: 사용 가능**이 선택한 사용자의 세부 정보 창에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-130">When it's created, **Archive mailbox: enabled** is displayed in the details pane for the selected user.</span></span> <span data-ttu-id="9adf4-131">세부 정보 창의 정보를 업데이트하려면 **새로 고침** ![새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif)을 클릭해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-131">You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="9adf4-132">(Shift 또는 Ctrl 키를 사용해) 보관 사서함을 사용할 수 없는 여러 사용자를 선택하여 보관함을 대량으로 사용하도록 설정할 수도 있습니다. </span><span class="sxs-lookup"><span data-stu-id="9adf4-132">You can also bulk-enable archives by selecting multiple mailboxes (use the Shift or Ctrl keys).</span></span> <span data-ttu-id="9adf4-133">여러 사서함을 선택한 후 세부 정보 창에서 **사용**을 클릭하십시오.</span><span class="sxs-lookup"><span data-stu-id="9adf4-133">After selecting multiple mailboxes, in the details pane, click **More options**.</span></span> 
  
## <a name="disable-an-archive-mailbox"></a><span data-ttu-id="9adf4-134">보관 사서함 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="9adf4-134">Disable an archive mailbox</span></span>
  
<span data-ttu-id="9adf4-135">보안 및 규정 준수 센터의 **보관 처리** 페이지를 사용하여 사용자 보관 사서함을 비활성화할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-135">You can also use the **Archive** page in the Security & Compliance Center to disable a user's archive mailbox.</span></span> <span data-ttu-id="9adf4-136">보관 사서함을 비활성화 한 후 다시 연결할 수 있습니다이 사용자의 기본 사서함을 해제 후 30 일 이내.</span><span class="sxs-lookup"><span data-stu-id="9adf4-136">If you disable a user's archive mailbox, you can reconnect it to the user's primary mailbox within 30 days of disabling it.</span></span> <span data-ttu-id="9adf4-137">이 경우 보관 사서함의 원래 내용은 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-137">In this case, the original contents of the archive mailbox are restored.</span></span> <span data-ttu-id="9adf4-138">30 일이 지나면 원래 보관 사서함의 내용을 영구적으로 삭제 하 고 복구할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-138">After 30 days, the contents of the original archive mailbox are permanently deleted and can't be recovered.</span></span> <span data-ttu-id="9adf4-139">따라서 아카이브 해제 한 후 30 일 이상 다시 설정, 보관 사서함이 새로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-139">So if you re-enable the archive more than 30 days after disabling it, a new archive mailbox is created.</span></span> 
  
<span data-ttu-id="9adf4-140">사용자의 사서함에 할당된 기본 보관 정책은 항목이 전달된 날짜로부터 2년 후에 항목을 보관 사서함으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-140">Note that the default archive policy assigned to users' mailboxes moves items to the archive mailbox two years after the date the item is delivered.</span></span> <span data-ttu-id="9adf4-141">사용자의 보관 사서함을 사용하지 않도록 설정하면 사서함 항목에 대해 아무 작업도 수행되지 않으며 사용자의 기본 사서함에 그대로 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-141">If you disable a user's archive mailbox, no action will be taken on mailbox items and they will remain in the user's primary mailbox.</span></span>
  
<span data-ttu-id="9adf4-142">보관 사서함을 사용하지 않으려면:</span><span class="sxs-lookup"><span data-stu-id="9adf4-142">To disable an archive mailbox:</span></span>
  
1. <span data-ttu-id="9adf4-143">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-143">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="9adf4-144">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-144">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="9adf4-145">보안 및 규정 준수 센터의 왼쪽 창에서 **데이터 관리** \> **보관**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-145">In the left pane of the Security & Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="9adf4-146">**보관** 페이지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-146">The **New search** page is displayed.</span></span> <span data-ttu-id="9adf4-147">**보관 사서함** 열은 각 사용자의 보관 사서함이 사용되도록 설정되었는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-147">The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="9adf4-148">사서함 목록에서 보관 사서함을 사용하지 않도록 설정할 사용자를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-148">In the list of mailboxes, select the user that you want to disable the archive mailbox for.</span></span>
    
5. <span data-ttu-id="9adf4-149">세부 정보 창에서 **사용 안 함**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-149">In the details pane, under In-Place Archive, click **Disable**.</span></span> 
    
    <span data-ttu-id="9adf4-150">30일 이내에 보관 사서함을 다시 사용하도록 설정해야 하고, 30일 이후에는 보관 사서함의 모든 정보가 영구적으로 삭제된다는 경고 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-150">A warning message is displayed saying that you'll have 30 days to re-enable the archive mailbox, and that after 30 days, all information in the archive will be permanently deleted.</span></span> 
    
6. <span data-ttu-id="9adf4-151">**예**를 클릭하여 보관 사서함을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-151">Click **Yes** to disable the archive mailbox.</span></span> 
    
    <span data-ttu-id="9adf4-152">보관 사서함을 사용 해제하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-152">It might take a few moments to disable the archive mailbox.</span></span> <span data-ttu-id="9adf4-153">사용하지 않도록 설정하면 **보관 사서함: 사용하지 않음**이 선택한 사용자의 세부 정보 창에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-153">When it's disabled, **Archive mailbox: disabled** is displayed in the details pane for the selected user.</span></span> <span data-ttu-id="9adf4-154">세부 정보 창의 정보를 업데이트하려면 **새로 고침** ![새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif)을 클릭해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-154">You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="9adf4-155">보관 사서함이 활성화 된 여러 사용자를 선택하여 보관 사서함을 일괄 비활성화할 수도 있습니다(Shift 또는 Ctrl 키 사용).</span><span class="sxs-lookup"><span data-stu-id="9adf4-155">You can also bulk-disable archives by selecting multiple mailboxes (use the Shift or Ctrl keys).</span></span> <span data-ttu-id="9adf4-156">여러 사서함을 선택한 후 세부 정보 창에서 **사용 안 함**을 클릭하십시오.</span><span class="sxs-lookup"><span data-stu-id="9adf4-156">After selecting multiple mailboxes, in the details pane, click **More options**.</span></span> 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a><span data-ttu-id="9adf4-157">Exchange Online PowerShell을 사용하여 보관 사서함을 사용하거나 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="9adf4-157">Use Exchange Online PowerShell to enable or disable archive mailboxes</span></span>

<span data-ttu-id="9adf4-158">Exchange Online PowerShell을 사용하여 보관 사서함을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-158">You can also use Exchange Online PowerShell to enable archive mailboxes.</span></span> <span data-ttu-id="9adf4-159">PowerShell을 사용하는 주된 이유는 조직의 모든 사용자에 대해 보관 사서함을 신속하게 사용할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-159">The primary reason to use PowerShell is that you can quickly enable the archive mailbox for all users in your organization.</span></span>

<span data-ttu-id="9adf4-160">첫 번째 단계는 Exchange Online PowerShell에 연결하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-160">The first step is to connect to Exchange Online PowerShell.</span></span> <span data-ttu-id="9adf4-161">지침을 확인하려면 [Exchange Online PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9adf4-161">For instructions, see [Connect to Office 365 PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="9adf4-162">Exchange Online에 연결되면 다음 섹션의 명령을 실행하여 보관 사서함을 사용하거나 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-162">After you're connected to Exchange Online, you can run the commands in the following sections to enable or disable archive mailboxes.</span></span>

### <a name="enable-archive-mailboxes"></a><span data-ttu-id="9adf4-163">보관 사서함 사용</span><span class="sxs-lookup"><span data-stu-id="9adf4-163">Enable archive mailboxes</span></span>

<span data-ttu-id="9adf4-164">다음 명령을 실행하여 단일 사용자가 보관 사서함을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-164">Run the following command to enable the archive mailbox for a single user.</span></span>
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="9adf4-165">다음 명령을 실행하여 조직의 모든 사용자(현재 보관 사서함을 사용할 수 없는 사용자)의 보관 사서함을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-165">Run the following command to enable the archive mailbox for all users in your organization (whose archive mailbox is currently not enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a><span data-ttu-id="9adf4-166">보관 사서함을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="9adf4-166">Disable archive mailboxes</span></span>

<span data-ttu-id="9adf4-167">다음 명령을 실행하여 단일 사용자가 보관 사서함을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-167">Run the following command to disable the archive mailbox for a single user.</span></span>
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="9adf4-168">다음 명령을 실행하여 조직의 모든 사용자(현재 보관 사서함을 사용할 수 있는 사용자)의 보관 사서함을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-168">Run the following command to disable the archive mailbox for all users in your organization (whose archive mailbox is currently enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a><span data-ttu-id="9adf4-169">추가 정보</span><span class="sxs-lookup"><span data-stu-id="9adf4-169">More information</span></span>
  
- <span data-ttu-id="9adf4-170">보관 사서함을 사용하도록 설정하면 사용자는 보관 사서함에 메시지를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-170">When an archive mailbox is enabled, users can store messages in their archive mailbox.</span></span> <span data-ttu-id="9adf4-171">사용자는 웹에서 Microsoft Outlook 및 Outlook을 사용하여 보관 사서함에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-171">Users can access their archive mailboxes by using Microsoft Outlook and Outlook on the web.</span></span> <span data-ttu-id="9adf4-172">이러한 클라이언트 응용 프로그램을 사용하여 사용자는 보관 사서함의 메시지를 보고 기본 사서함과 보관 사서함 간에 메시지를 이동하거나 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-172">Using either of these client applications, users can view an archive mailbox and move or copy messages between their primary mailbox and the archive.</span></span> <span data-ttu-id="9adf4-173">사용자는 지운 편지함 복구 도구를 사용하여 보관 사서함의 복구 가능한 항목 폴더에서 삭제된 항목을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-173">Users can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span>

   <span data-ttu-id="9adf4-174">현재 위치 보관을 지원하는 Outlook 라이선스 목록은 [Exchange 기능](https://support.office.com/article/outlook-license-requirements-for-exchange-features-46b6b7c5-c3ca-43e5-8424-1e2807917c99)의 Outlook 라이선스 요구 사항을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="9adf4-174">For a list of Outlook licenses that support In-Place Archiving, see [Outlook license requirements for Exchange features](https://support.office.com/article/outlook-license-requirements-for-exchange-features-46b6b7c5-c3ca-43e5-8424-1e2807917c99).</span></span>

- <span data-ttu-id="9adf4-175">보관 사서함은 사용자가 조직의 보존, eDiscovery 및 보류 요구 사항을 충족하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-175">Archive mailboxes help you and your users to meet your organization's retention, eDiscovery, and hold requirements.</span></span> <span data-ttu-id="9adf4-176">예를 들어, 조직의 Exchange 보존 정책을 사용하여 사용자의 보관 사서함으로 사서함 콘텐츠를 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-176">For example, you can use your organization's Exchange retention policy to move mailbox content to users' archive mailbox.</span></span> <span data-ttu-id="9adf4-177">보안 및 규정 준수 센터의 콘텐츠 검색 도구를 사용하여 사용자의 사서함에서 특정 콘텐츠를 검색하면 해당 사용자의 보관 사서함도 검색됩니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-177">When you use the Content Search tool in the Security & Compliance Center to search a user's mailbox for specific content, the user's archive mailbox will also be searched.</span></span> <span data-ttu-id="9adf4-178">또한 소송 자료를 보관하거나 Office 365 보존 정책을 사용자의 사서함에 적용하면 보관 사서함의 항목도 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-178">And, when you place a Litigation Hold or apply an Office 365 retention policy to a user's mailbox, items in the archive mailbox are also retained.</span></span>
  
- <span data-ttu-id="9adf4-179">보관 사서함을 사용하도록 설정하면 조직에서 모든 사서함에 자동으로 할당되는 기본 Exchange 보존 정책(메시징 레코드 관리 또는 MRM 정책이라고도 함)을 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-179">After archive mailboxes are enabled, your organization can take advantage of the default Exchange retention policy (also called Messaging Records Management or MRM policy) that is automatically assigned to every mailbox.</span></span> <span data-ttu-id="9adf4-180">보관 사서함을 사용하도록 설정하면 기본 Exchange 보존 정책이 자동으로 다음 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-180">When an archive mailbox is enabled, the default Exchange retention policy automatically does the following:</span></span> 
  
    - <span data-ttu-id="9adf4-181">사용자의 기본 사서함에서 보관 사서함으로 2년 이상 된 항목을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-181">Moves items that are two years or older from a user's primary mailbox to their archive mailbox.</span></span> 
    
    - <span data-ttu-id="9adf4-182">사용자의 기본 사서함에 있는 복구 가능한 항목 폴더에서 보관 사서함의 복구 가능한 항목 폴더로 14일 이상 된 항목을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="9adf4-182">Moves items that are 14 days or older from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in their archive mailbox.</span></span>
    
- <span data-ttu-id="9adf4-183">보관 사서함 및 Exchange 보존 정책에 대한 자세한 내용은 다음을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="9adf4-183">For more information about archive mailboxes and Exchange retention policies, see:</span></span>
    
  - [<span data-ttu-id="9adf4-184">보존 태그 및 보존 정책</span><span class="sxs-lookup"><span data-stu-id="9adf4-184">Retention tags and retention policies</span></span>](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [<span data-ttu-id="9adf4-185">Exchange Online의 기본 보존 정책</span><span class="sxs-lookup"><span data-stu-id="9adf4-185">Default Retention Policy in Exchange Online https://go.microsoft.com/fwlink/p/?LinkId=746954</span></span>](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [<span data-ttu-id="9adf4-186">Office 365 조직에서 사서함에 대한 보관 및 삭제 정책 설정</span><span class="sxs-lookup"><span data-stu-id="9adf4-186">Set up an archive and deletion policy for mailboxes in your Office 365 organization</span></span>](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
