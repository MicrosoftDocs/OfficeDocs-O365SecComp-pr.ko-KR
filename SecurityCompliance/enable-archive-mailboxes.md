---
title: 보안 & 준수 센터에서 보관 사서함을 사용 하도록 설정
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Office 365의 Security & 준수 센터를 사용 하 여 조직의 메시지 보존, eDiscovery 및 보존 요구 사항을 지원 하기 위해 보관 사서함을 사용 하도록 설정할 수 있습니다.
ms.openlocfilehash: d363943910d970576976d8386196b450dd5694f3
ms.sourcegitcommit: 6c9340e4eb221bf81472ff3f1ae25ae21aaf5297
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/11/2019
ms.locfileid: "31813969"
---
# <a name="enable-archive-mailboxes-in-the-security--compliance-center"></a><span data-ttu-id="e11d4-103">보안 & 준수 센터에서 보관 사서함을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="e11d4-103">Enable archive mailboxes in the Security & Compliance Center</span></span>
  
<span data-ttu-id="e11d4-104">Office 365 (원본 위치 보관이 라고도 함)의 보관은 사용자에 게 사서함 저장소 공간을 추가로 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-104">Archiving in Office 365 (also called In-Place Archiving) provides users with additional mailbox storage space.</span></span> <span data-ttu-id="e11d4-105">보관 사서함을 켜면 사용자가 Microsoft outlook 및 웹용 outlook (이전의 outlook web App)을 사용 하 여 보관 사서함에 메시지를 액세스 하 고 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-105">After you turn on archive mailboxes, users can access and store messages in their archive mailboxes by using Microsoft Outlook and Outlook on the web (formerly known as Outlook Web App).</span></span> <span data-ttu-id="e11d4-106">사용자는 기본 사서함과 해당 보관 사서함 간에 메시지를 이동 하거나 복사할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-106">Users can also move or copy messages between their primary mailbox and their archive mailbox.</span></span> <span data-ttu-id="e11d4-107">지운 편지함 복구 도구를 사용 하 여 보관 사서함의 복구 가능한 항목 폴더에서 삭제 된 항목을 복구할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-107">They can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
> [!TIP]
> <span data-ttu-id="e11d4-108">Office 365에서는 자동 확장 보관 기능과 무제한의 보관 저장소를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-108">Office 365 provides an unlimited amount of archive storage with the auto-expanding archiving feature.</span></span> <span data-ttu-id="e11d4-109">자동 확장 보관이 켜져 있는 경우 사용자의 보관 사서함에 있는 초기 저장소 할당량에 도달 하면 Office 365에서 자동으로 저장 공간을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-109">When auto-expanding archiving is turned on, and then the initial storage quota in a user's archive mailbox is reached, Office 365 automatically adds additional storage space.</span></span> <span data-ttu-id="e11d4-110">즉, 사용자에 게 사서함 저장소 공간이 부족 하지 않으며, 처음에 보관 사서함을 사용 하도록 설정 하 고 조직에 대해 자동 확장 보관을 사용 하도록 설정한 후에는 별도로 관리할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-110">This means that users won't run out of mailbox storage space and you won't have to manage anything after you initially enable the archive mailbox and turn on auto-expanding archiving for your organization.</span></span> <span data-ttu-id="e11d4-111">자세한 내용은 [Office 365 무제한 보관의 개요](unlimited-archiving.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e11d4-111">For more information, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="e11d4-112">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="e11d4-112">Before you begin</span></span>

<span data-ttu-id="e11d4-113">보관 사서함을 사용 하거나 사용 하지 않도록 설정 하려면 Exchange Online의 Mail Recipients 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-113">You have to be assigned the Mail Recipients role in Exchange Online to enable or disable archive mailboxes.</span></span> <span data-ttu-id="e11d4-114">기본적으로이 역할은 Exchange 관리 센터의 **사용 권한** 페이지에 있는 받는 사람 관리 및 조직 관리 역할 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-114">By default, this role is assigned to the Recipient Management and Organization Management role groups on the **Permissions** page in the Exchange admin center.</span></span> <span data-ttu-id="e11d4-115">보안 & 준수 센터에 **보관** 페이지가 표시 되지 않으면 관리자에 게 필요한 사용 권한을 할당 해 달라고 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-115">If you don't see the **Archive** page in the Security & Compliance Center, ask your administrator to assign you the necessary permissions.</span></span> 
  
## <a name="enable-an-archive-mailbox"></a><span data-ttu-id="e11d4-116">보관 사서함 사용</span><span class="sxs-lookup"><span data-stu-id="e11d4-116">Enable an archive mailbox</span></span>
  
1. <span data-ttu-id="e11d4-117">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-117">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="e11d4-118">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-118">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="e11d4-119">Security & 준수 센터의 왼쪽 창에서 **데이터 거 버 넌 스** \> **보관**함을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-119">In the left pane of the Security & Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="e11d4-120">**보관** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-120">The **Archive** page is displayed.</span></span> <span data-ttu-id="e11d4-121">**보관 사서함** 열에는 각 사용자에 대해 보관 사서함이 사용 하도록 설정 되었는지 또는 사용 하지 않도록 설정 되어 있는지 여부가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-121">The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="e11d4-122">사서함 목록에서 보관 사서함을 사용 하도록 설정 하려는 사용자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-122">In the list of mailboxes, select the user that you want to enable the archive mailbox for.</span></span>
    
    ![선택한 사용자의 세부 정보 창에서 사용을 클릭 하 여 보관 사서함을 사용 하도록 설정 합니다.](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. <span data-ttu-id="e11d4-124">선택한 사용자에 대 한 세부 정보 창에서 **사용**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-124">In the details pane for the selected user, click **Enable**.</span></span> 
    
    <span data-ttu-id="e11d4-125">보관 사서함을 사용 하도록 설정 하면 사용자 사서함에서 사서함에 할당 된 보관 정책 보다 오래 된 항목이 새 보관 사서함으로 이동 됨을 알리는 경고가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-125">A warning is displayed saying that if you enable the archive mailbox, items in the user's mailbox that are older than the archiving policy assigned to the mailbox will be moved to the new archive mailbox.</span></span> <span data-ttu-id="e11d4-126">Exchange Online 사서함에 할당 된 보존 정책의 일부인 기본 보관 정책은 항목이 사서함으로 배달 되거나 사용자가 만든 날짜 후 2 년 후에 항목을 보관 사서함으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-126">The default archive policy that is part of the retention policy assigned to Exchange Online mailboxes moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user.</span></span> <span data-ttu-id="e11d4-127">자세한 내용은이 문서의 **추가 정보** 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="e11d4-127">For more information, see the **More info** section in this article.</span></span> 
    
6. <span data-ttu-id="e11d4-128">**예** 를 클릭 하 여 보관 사서함을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-128">Click **Yes** to enable the archive mailbox.</span></span> 
    
    <span data-ttu-id="e11d4-129">보관 사서함을 만드는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-129">It might take a few moments to create the archive mailbox.</span></span> <span data-ttu-id="e11d4-130">이 파일을 만들 때 **보관 사서함: enabled** 가 선택한 사용자에 대 한 세부 정보 창에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-130">When it's created, **Archive mailbox: enabled** is displayed in the details pane for the selected user.</span></span> <span data-ttu-id="e11d4-131">세부 정보 창에서 정보를 업데이트 하려면](media/O365-MDM-Policy-RefreshIcon.gif) 새로 고침 아이콘 **새로 고침** ![을 클릭 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-131">You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="e11d4-132">또한 사용 하지 않도록 설정 된 보관 사서함을 사용 하 여 여러 사용자를 선택 하 여 보관 사서함을 대량으로 사용 하도록 설정할 수 있습니다 (Shift 또는 Ctrl 키 사용).</span><span class="sxs-lookup"><span data-stu-id="e11d4-132">You can also bulk-enable archive mailboxes by selecting multiple users with disabled archive mailboxes (use the Shift or Ctrl keys).</span></span> <span data-ttu-id="e11d4-133">여러 사서함을 선택한 후 세부 정보 창에서 **사용** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-133">After selecting multiple mailboxes, click **Enable** in the details pane.</span></span> 
  
## <a name="disable-an-archive-mailbox"></a><span data-ttu-id="e11d4-134">보관 사서함 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="e11d4-134">Disable an archive mailbox</span></span>
  
<span data-ttu-id="e11d4-135">또한 Security & 준수 센터의 **보관** 페이지를 사용 하 여 사용자의 보관 사서함을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-135">You can also use the **Archive** page in the Security & Compliance Center to disable a user's archive mailbox.</span></span> <span data-ttu-id="e11d4-136">보관 사서함을 사용 하지 않도록 설정한 후에는 사용 하지 않도록 설정 하 고 30 일 이내에 사용자의 기본 사서함에 다시 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-136">After you disable an archive mailbox, you can reconnect it to the user's primary mailbox within 30 days of disabling it.</span></span> <span data-ttu-id="e11d4-137">이 경우 보관 사서함의 원래 내용이 복원됩니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-137">In this case, the original contents of the archive mailbox are restored.</span></span> <span data-ttu-id="e11d4-138">30일이 지나면 원래 보관 사서함의 내용이 영구적으로 삭제되어 복구할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-138">After 30 days, the contents of the original archive mailbox are permanently deleted and can't be recovered.</span></span> <span data-ttu-id="e11d4-139">따라서 비활성화한 지 30일 넘게 지난 뒤 보관 사서함을 다시 사용하도록 설정하면 새 보관 사서함이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-139">So if you re-enable the archive more than 30 days after disabling it, a new archive mailbox is created.</span></span> 
  
<span data-ttu-id="e11d4-140">사용자 사서함에 할당 된 기본 보관 정책이 항목을 배달 한 날짜 후 2 년 후에 항목을 보관 사서함으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-140">Note that the default archive policy assigned to users' mailboxes moves items to the archive mailbox two years after the date the item is delivered.</span></span> <span data-ttu-id="e11d4-141">사용자의 보관 사서함을 사용 하지 않도록 설정 하면 사서함 항목에 대 한 아무 작업도 수행 되지 않으며 사용자의 기본 사서함에 남아 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-141">If you disable a user's archive mailbox, no action will be taken on mailbox items and they will remain in the user's primary mailbox.</span></span>
  
<span data-ttu-id="e11d4-142">보관 사서함을 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="e11d4-142">To disable an archive mailbox:</span></span>
  
1. <span data-ttu-id="e11d4-143">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-143">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="e11d4-144">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-144">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="e11d4-145">Security & 준수 센터의 왼쪽 창에서 **데이터 거 버 넌 스** \> **보관**함을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-145">In the left pane of the Security & Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="e11d4-146">**보관** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-146">The **Archive** page is displayed.</span></span> <span data-ttu-id="e11d4-147">**보관 사서함** 열에는 각 사용자에 대해 보관 사서함이 사용 하도록 설정 되었는지 또는 사용 하지 않도록 설정 되어 있는지 여부가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-147">The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="e11d4-148">사서함 목록에서 보관 사서함을 사용 하지 않도록 설정 하려는 사용자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-148">In the list of mailboxes, select the user that you want to disable the archive mailbox for.</span></span>
    
5. <span data-ttu-id="e11d4-149">세부 정보 창에서 **사용 안 함을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-149">In the details pane, click **Disable**.</span></span> 
    
    <span data-ttu-id="e11d4-150">30 일 동안 보관 사서함을 다시 사용 하도록 설정 하 고 30 일 후에 보관 함의 모든 정보가 영구적으로 삭제 됨을 알리는 경고 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-150">A warning message is displayed saying that you'll have 30 days to re-enable the archive mailbox, and that after 30 days, all information in the archive will be permanently deleted.</span></span> 
    
6. <span data-ttu-id="e11d4-151">**예** 를 클릭 하 여 보관 사서함을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-151">Click **Yes** to disable the archive mailbox.</span></span> 
    
    <span data-ttu-id="e11d4-152">보관 사서함을 사용 하지 않도록 설정 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-152">It might take a few moments to disable the archive mailbox.</span></span> <span data-ttu-id="e11d4-153">사용 하지 않도록 설정 된 경우 **보관 사서함: 사용 안 함** 이 선택한 사용자의 세부 정보 창에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-153">When it's disabled, **Archive mailbox: disabled** is displayed in the details pane for the selected user.</span></span> <span data-ttu-id="e11d4-154">세부 정보 창에서 정보를 업데이트 하려면](media/O365-MDM-Policy-RefreshIcon.gif) 새로 고침 아이콘 **새로 고침** ![을 클릭 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-154">You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="e11d4-155">보관 사서함을 사용 하도록 설정한 여러 사용자를 선택 하 여 보관 사서함을 대량으로 사용 하지 않도록 설정할 수도 있습니다 (Shift 또는 Ctrl 키 사용).</span><span class="sxs-lookup"><span data-stu-id="e11d4-155">You can also bulk-disable archive mailboxes by selecting multiple users with enabled archive mailboxes (use the Shift or Ctrl keys).</span></span> <span data-ttu-id="e11d4-156">여러 사서함을 선택한 후 세부 정보 창에서 **사용 안 함을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-156">After selecting multiple mailboxes, click **Disable** in the details pane.</span></span> 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a><span data-ttu-id="e11d4-157">Exchange Online PowerShell을 사용 하 여 보관 사서함을 사용 하거나 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="e11d4-157">Use Exchange Online PowerShell to enable or disable archive mailboxes</span></span>

<span data-ttu-id="e11d4-158">또한 Exchange Online PowerShell을 사용 하 여 보관 사서함을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-158">You can also use Exchange Online PowerShell to enable archive mailboxes.</span></span> <span data-ttu-id="e11d4-159">PowerShell을 사용 하는 주요 이유는 조직의 모든 사용자에 대해 보관 사서함을 빠르게 사용 하도록 설정할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-159">The primary reason to use PowerShell is that you can quickly enable the archive mailbox for all users in your organization.</span></span>

<span data-ttu-id="e11d4-160">첫 번째 단계는 Exchange Online PowerShell에 연결 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-160">The first step is to connect to Exchange Online PowerShell.</span></span> <span data-ttu-id="e11d4-161">자세한 내용은 [Exchange Online PowerShell에 연결을](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="e11d4-161">For instructions, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="e11d4-162">Exchange Online에 연결 하 고 나면 다음 섹션의 명령을 실행 하 여 보관 사서함을 사용 하거나 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-162">After you're connected to Exchange Online, you can run the commands in the following sections to enable or disable archive mailboxes.</span></span>

### <a name="enable-archive-mailboxes"></a><span data-ttu-id="e11d4-163">보관 사서함 사용</span><span class="sxs-lookup"><span data-stu-id="e11d4-163">Enable archive mailboxes</span></span>

<span data-ttu-id="e11d4-164">다음 명령을 실행 하 여 단일 사용자에 대해 보관 사서함을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-164">Run the following command to enable the archive mailbox for a single user.</span></span>
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="e11d4-165">다음 명령을 실행 하 여 조직의 모든 사용자 (보관 사서함 현재 사용 하지 않도록 설정 되어 있지 않음)에서 보관 사서함을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-165">Run the following command to enable the archive mailbox for all users in your organization (whose archive mailbox is currently not enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a><span data-ttu-id="e11d4-166">보관 사서함 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="e11d4-166">Disable archive mailboxes</span></span>

<span data-ttu-id="e11d4-167">다음 명령을 실행 하 여 단일 사용자에 대해 보관 사서함을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-167">Run the following command to disable the archive mailbox for a single user.</span></span>
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="e11d4-168">다음 명령을 실행 하 여 조직의 모든 사용자 (보관 사서함 현재 사용 가능)에 대 한 보관 사서함을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-168">Run the following command to disable the archive mailbox for all users in your organization (whose archive mailbox is currently enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a><span data-ttu-id="e11d4-169">추가 정보</span><span class="sxs-lookup"><span data-stu-id="e11d4-169">More information</span></span>
  
- <span data-ttu-id="e11d4-170">보관 사서함을 통해 조직의 보존, eDiscovery 및 보존 요구 사항을 충족 하는 사용자를 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-170">Archive mailboxes help you and your users to meet your organization's retention, eDiscovery, and hold requirements.</span></span> <span data-ttu-id="e11d4-171">예를 들어 조직의 Exchange 보존 정책을 사용 하 여 사서함 콘텐츠를 사용자의 보관 사서함으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-171">For example, you can use your organization's Exchange retention policy to move mailbox content to users' archive mailbox.</span></span> <span data-ttu-id="e11d4-172">보안 & 준수 센터의 콘텐츠 검색 도구를 사용 하 여 사용자의 사서함에서 특정 콘텐츠를 검색 하는 경우 사용자의 보관 사서함도 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-172">When you use the Content Search tool in the Security & Compliance Center to search a user's mailbox for specific content, the user's archive mailbox will also be searched.</span></span> <span data-ttu-id="e11d4-173">또한 소송 보존을 수행 하거나 사용자 사서함에 Office 365 유지 정책을 적용 하는 경우 보관 사서함의 항목도 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-173">And, when you place a Litigation Hold or apply an Office 365 retention policy to a user's mailbox, items in the archive mailbox are also retained.</span></span>
  
- <span data-ttu-id="e11d4-174">보관 사서함을 사용 하도록 설정 하면 사용자가 보관 사서함에 메시지를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-174">When an archive mailbox is enabled, users can store messages in their archive mailbox.</span></span> <span data-ttu-id="e11d4-175">사용자는 Microsoft outlook 및 웹용 Outlook을 사용 하 여 보관 사서함에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-175">Users can access their archive mailboxes by using Microsoft Outlook and Outlook on the web.</span></span> <span data-ttu-id="e11d4-176">이러한 클라이언트 응용 프로그램 중 하나를 사용 하면 사용자가 자신의 보관 사서함에서 메시지를 보고 기본 사서함과 해당 보관 사서함 간에 메시지를 이동 하거나 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-176">Using either of these client applications, users can view messages in their archive mailbox and move or copy messages between their primary mailbox and their archive mailbox.</span></span> <span data-ttu-id="e11d4-177">또한 사용자는 지운 편지함 복구 도구를 사용 하 여 보관 사서함의 복구 가능한 항목 폴더에서 삭제 된 항목을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-177">Users can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
- <span data-ttu-id="e11d4-178">보관 사서함을 사용 하도록 설정한 후에는 조직에서 모든 사서함에 자동으로 할당 되는 기본 Exchange 보존 정책 (메시징 레코드 관리 또는 mrm 정책)을 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-178">After archive mailboxes are enabled, your organization can take advantage of the default Exchange retention policy (also called Messaging Records Management or MRM policy) that is automatically assigned to every mailbox.</span></span> <span data-ttu-id="e11d4-179">보관 사서함을 사용 하도록 설정 하면 기본 Exchange 보존 정책이 자동으로 다음 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-179">When an archive mailbox is enabled, the default Exchange retention policy automatically does the following:</span></span> 
  
    - <span data-ttu-id="e11d4-180">사용자의 기본 사서함에서 보관 사서함으로 2년 이상 된 항목을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-180">Moves items that are two years or older from a user's primary mailbox to their archive mailbox.</span></span> 
    
    - <span data-ttu-id="e11d4-181">사용자의 기본 사서함에 있는 복구 가능한 항목 폴더에서 보관 사서함의 복구 가능한 항목 폴더로 14일 이상 된 항목을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="e11d4-181">Moves items that are 14 days or older from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in their archive mailbox.</span></span>
    
- <span data-ttu-id="e11d4-182">보관 사서함 및 Exchange 보존 정책에 대 한 자세한 내용은 다음 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="e11d4-182">For more information about archive mailboxes and Exchange retention policies, see:</span></span>
    
  - [<span data-ttu-id="e11d4-183">보존 태그 및 보존 정책</span><span class="sxs-lookup"><span data-stu-id="e11d4-183">Retention tags and retention policies</span></span>](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [<span data-ttu-id="e11d4-184">Exchange Online의 기본 보존 정책</span><span class="sxs-lookup"><span data-stu-id="e11d4-184">Default Retention Policy in Exchange Online</span></span> ](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [<span data-ttu-id="e11d4-185">Office 365 조 직의 사서함에 대 한 보관 및 삭제 정책 설정</span><span class="sxs-lookup"><span data-stu-id="e11d4-185">Set up an archive and deletion policy for mailboxes in your Office 365 organization</span></span>](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
