---
title: Office 365 보안에서 보관 사서함 사용 &amp; 준수 센터
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Office 365 보안을 사용 하 여 &amp; 준수 센터 조직의 메시지 보존, eDiscovery, 지원 및 유지 요구 사항에 대 한 보관 사서함을 사용 하도록 설정 합니다.
ms.openlocfilehash: 1c290cf19b396221dac702efd1395911e8a51631
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "28327100"
---
# <a name="enable-archive-mailboxes-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="15d12-103">Office 365 보안에서 보관 사서함 사용 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="15d12-103">Enable archive mailboxes in the Office 365 Security &amp; Compliance Center</span></span>
  
<span data-ttu-id="15d12-p101">(내부 보관이 라고도 함)는 Office 365의 보관 추가 사서함 저장 공간을 사용 하는 사용자를 제공 합니다. 보관 사서함에 대 한 정보를 설정한 후 사용자가 액세스 하 고 Microsoft Outlook을 사용 하 여 보관 사서함에 메시지를 저장할 수 및 Outlook Web app. 사용자를 이동 하거나 기본 사서함 및 보관 사서함 간 메시지 복사 수도 있습니다. 또한 지운 편지함 복구 도구를 사용 하 여 보관 사서함의 복구 가능한 항목 폴더에서 삭제 된 항목을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-p101">Archiving in Office 365 (also called In-Place Archiving) provides users with additional mailbox storage space. After you turn on archive mailboxes, users can access and store messages in their archive mailboxes by using Microsoft Outlook and Outlook Web App. Users can also move or copy messages between their primary mailbox and their archive mailbox. They can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
> [!TIP]
> <span data-ttu-id="15d12-p102">Office 365의 보관 저장소 자동 확장 보관 기능 무제한 금액을 제공합니다. 설정 보관 자동 확장 하 고 사용자의 보관 사서함의 초기 저장소 할당량에 도달 하면 다음을 Office 365 추가 저장 공간을 자동으로 추가 합니다. 사용자가 사서함 저장 공간 부족 실행 되지 않음 및 아무것도 하 고 나면 처음 관리 할 필요가 있는지 여부를이 나타내는 보관 사서함을 사용 하도록 설정 하 고 자동 확장 하면 조직에 대 한 보관 설정 합니다. 자세한 내용은 [Office 365 무제한 보관의 개요](unlimited-archiving.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="15d12-p102">Office 365 provides an unlimited amount of archive storage with the auto-expanding archiving feature. When auto-expanding archiving is turned on, and then the initial storage quota in a user's archive mailbox is reached, Office 365 automatically adds additional storage space. This means that users won't run out of mailbox storage space and you won't have to manage anything after you initially enable the archive mailbox and turn on auto-expanding archiving for your organization. For more information, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="15d12-112">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="15d12-112">Before you begin</span></span>

<span data-ttu-id="15d12-p103">역할을 할당 편지 병합 받는 사람 Exchange Online을 사용 하도록 설정 하거나 보관 사서함을 사용 하지 않도록 설정 해야 합니다. 기본적으로이 역할은 Exchange 관리 센터에서 **사용 권한** 페이지에서 받는 사람 관리 및 조직 관리 역할 그룹에 할당 됩니다. 보안에서 **보관** 페이지를 보이지 않으면 하는 경우 &amp; 준수 센터 필요한 사용 권한을 할당 하려면 관리자에 게 문의 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-p103">You have to be assigned the Mail Recipients role in Exchange Online to enable or disable archive mailboxes. By default, this role is assigned to the Recipient Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. If you don't see the **Archive** page in the Security &amp; Compliance Center, ask your administrator to assign you the necessary permissions.</span></span> 
  
## <a name="enable-an-archive-mailbox"></a><span data-ttu-id="15d12-116">보관 사서함 사용</span><span class="sxs-lookup"><span data-stu-id="15d12-116">Enable an archive mailbox</span></span>
  
1. <span data-ttu-id="15d12-117">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-117">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="15d12-118">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-118">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="15d12-119">보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 거 버 넌 스** 를 클릭 \> **보관**합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-119">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="15d12-p104">**보관** 페이지가 표시됩니다. **보관 사서함** 열은 각 사용자의 보관 사서함이 사용하도록 설정되었는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-p104">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="15d12-122">사서함 목록에서 보관 사서함을 사용하도록 설정할 사용자를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-122">In the list of mailboxes, select the user that you want to enable the archive mailbox for.</span></span>
    
    ![보관 사서함을 사용 하도록 설정 하려면 선택한 사용자의 세부 정보 창에서 사용을 클릭 합니다.](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. <span data-ttu-id="15d12-124">선택한 사용자에 대 한 세부 정보 창에서 **사용**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-124">In the details pane for the selected user, click **Enable**.</span></span> 
    
    <span data-ttu-id="15d12-p105">경고 메시지가 보관 사서함을 사용 하도록 설정 하는 경우 사용자의 사서함에서 사서함에 할당 된 보관 정책 보다 오래 된 항목은 새 보관 사서함으로 이동할 수 없다는 표시 됩니다. Exchange Online 사서함에 할당 된 보존 정책의 일부인 기본 보관 정책을 이동 하는 항목 보관 사서함에는 항목이 사서함으로 배달 되거나 사용자가 만든 날짜 로부터 2 년입니다. 자세한 내용은이 문서의 **추가 정보** 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="15d12-p105">A warning is displayed saying that if you enable the archive mailbox, items in the user's mailbox that are older than the archiving policy assigned to the mailbox will be moved to the new archive mailbox. The default archive policy that is part of the retention policy assigned to Exchange Online mailboxes moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user. For more information, see the **More info** section in this article.</span></span> 
    
6. <span data-ttu-id="15d12-128">**예**를 클릭하여 보관 사서함을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-128">Click **Yes** to enable the archive mailbox.</span></span> 
    
    <span data-ttu-id="15d12-p106">보관 사서함을 만들 수는 몇 시간이 걸릴 수 있습니다. 만들 때 **보관 사서함: 활성화** 선택한 사용자에 대 한 세부 정보 창에 표시 됩니다. **새로 고침** 을 클릭 해야할 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) 세부 정보 창에 대 한 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-p106">It might take a few moments to create the archive mailbox. When it's created, **Archive mailbox: enabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="15d12-p107">Shift 또는 Ctrl 키를 사용해 여러 사서함을 선택하여 보관함을 대량으로 사용하도록 설정할 수도 있습니다. 여러 사서함을 선택한 후 세부 정보 창에서 기타 옵션을 클릭합니다. 그런 후에 보관함에서 **사용**을 클릭합니다. </span><span class="sxs-lookup"><span data-stu-id="15d12-p107">You can also bulk-enable archive mailboxes by selecting multiple users with disabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Enable** in the details pane.</span></span> 
  
## <a name="disable-an-archive-mailbox"></a><span data-ttu-id="15d12-134">보관 사서함 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="15d12-134">Disable an archive mailbox</span></span>
  
<span data-ttu-id="15d12-p108">보안에서 **보관** 페이지를 사용할 수도 있습니다 &amp; 준수 센터 사용자의 보관 사서함을 사용 하지 않도록 설정 합니다. 보관 사서함을 해제 한 후 다시 연결할 수 있습니다 해당 사용자의 기본 사서함에 사용 하지 못하도록 30 일 이내입니다. 이 경우 보관 사서함의 원래 내용은 복원 됩니다. 30 일 후 원래 보관 사서함의 내용을 영구적으로 삭제 하 고 복구할 수 없습니다. 따라서 보관 30 일 보다 것을 비활성화 한 후 다시 사용, 하는 경우 새 보관 사서함이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-p108">You can also use the **Archive** page in the Security &amp; Compliance Center to disable a user's archive mailbox. After you disable an archive mailbox, you can reconnect it to the user's primary mailbox within 30 days of disabling it. In this case, the original contents of the archive mailbox are restored. After 30 days, the contents of the original archive mailbox are permanently deleted and can't be recovered. So if you re-enable the archive more than 30 days after disabling it, a new archive mailbox is created.</span></span> 
  
<span data-ttu-id="15d12-p109">메모는 기본 보관 정책에 할당 된 사용자의 사서함 보관 사서함으로 이동 항목 날짜 후 2 년 항목이 배달 됩니다. 사용자의 보관 사서함 사용 하지 않는 경우 사서함 항목에 대해 아무 작업도 수행 되지 것입니다 하 고 사용자의 기본 사서함에 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-p109">Note that the default archive policy assigned to users' mailboxes moves items to the archive mailbox two years after the date the item is delivered. If you disable a user's archive mailbox, no action will be taken on mailbox items and they will remain in the user's primary mailbox.</span></span>
  
<span data-ttu-id="15d12-142">보관 사서함을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-142">To disable an archive mailbox:</span></span>
  
1. <span data-ttu-id="15d12-143">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-143">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="15d12-144">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-144">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="15d12-145">보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 거 버 넌 스** 를 클릭 \> **보관**합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-145">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="15d12-p110">**보관** 페이지가 표시됩니다. **보관 사서함** 열은 각 사용자의 보관 사서함이 사용하도록 설정되었는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-p110">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="15d12-148">사서함 목록에서 보관 사서함을 사용하지 않도록 설정할 사용자를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-148">In the list of mailboxes, select the user that you want to disable the archive mailbox for.</span></span>
    
5. <span data-ttu-id="15d12-149">세부 정보 창에서 **사용 안 함**을 클릭합니다. </span><span class="sxs-lookup"><span data-stu-id="15d12-149">In the details pane, click **Disable**.</span></span> 
    
    <span data-ttu-id="15d12-150">경고 메시지가 없다는 30 일 보관 사서함을 다시 사용 하도록 설정 해야 하 고 30 일 후 보관 사서함에 정보를 모두 삭제 됨을 영구적으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-150">A warning message is displayed saying that you'll have 30 days to re-enable the archive mailbox, and that after 30 days, all information in the archive will be permanently deleted.</span></span> 
    
6. <span data-ttu-id="15d12-151">**예**를 클릭하여 보관 사서함을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-151">Click **Yes** to disable the archive mailbox.</span></span> 
    
    <span data-ttu-id="15d12-p111">보관 사서함 사용 하지 않으려면 잠시 걸릴 수 있습니다. 비활성화 되 면 **보관 사서함: 비활성화** 선택한 사용자에 대 한 세부 정보 창에 표시 됩니다. **새로 고침** 을 클릭 해야할 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) 세부 정보 창에 대 한 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-p111">It might take a few moments to disable the archive mailbox. When it's disabled, **Archive mailbox: disabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="15d12-p112">Shift 또는 Ctrl 키를 사용해 보관 사서함이 사용하도록 설정된 여러 사용자를 선택하여 보관 사서함을 사용하지 않도록 일괄 설정할 수도 있습니다. 여러 사서함을 선택한 후 세부 정보 창에서 **사용 안 함**을 클릭합니다. </span><span class="sxs-lookup"><span data-stu-id="15d12-p112">You can also bulk-disable archive mailboxes by selecting multiple users with enabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Disable** in the details pane.</span></span> 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a><span data-ttu-id="15d12-157">Exchange Online PowerShell을 사용 하 여 보관 사서함을 사용 하지 않도록 설정 하거나 사용</span><span class="sxs-lookup"><span data-stu-id="15d12-157">Use Exchange Online PowerShell to enable or disable archive mailboxes</span></span>

<span data-ttu-id="15d12-p113">보관 사서함을 사용 하도록 설정 하려면 Exchange Online PowerShell를 사용할 수도 있습니다. PowerShell을 사용 하는 주된 이유는 조직에서 모든 사용자에 대 한 보관 사서함을 빠르게 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-p113">You can also use Exchange Online PowerShell to enable archive mailboxes. The primary reason to use PowerShell is that you can quickly enable the archive mailbox for all users in your organization.</span></span>

<span data-ttu-id="15d12-p114">첫번째 단계에서는 Exchange Online PowerShell에 연결 하는 것입니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="15d12-p114">The first step is to connect to Exchange Online PowerShell. For instructions, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="15d12-162">Exchange Online에 연결 된 후 사용 하도록 설정 하거나 보관 사서함을 사용 하지 않도록 설정 하려면 다음 섹션에서 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-162">After you're connected to Exchange Online, you can run the commands in the following sections to enable or disable archive mailboxes.</span></span>

### <a name="enable-archive-mailboxes"></a><span data-ttu-id="15d12-163">보관 사서함 사용</span><span class="sxs-lookup"><span data-stu-id="15d12-163">Enable archive mailboxes</span></span>

<span data-ttu-id="15d12-164">단일 사용자에 대 한 보관 사서함을 사용 하도록 설정 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-164">Run the following command to enable the archive mailbox for a single user.</span></span>
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="15d12-165">(보관 사서함을 현재 사용할 수 없습니다) 조직에서 모든 사용자에 대 한 보관 사서함을 사용 하도록 설정 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-165">Run the following command to enable the archive mailbox for all users in your organization (whose archive mailbox is currently not enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a><span data-ttu-id="15d12-166">보관 사서함을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="15d12-166">Disable archive mailboxes</span></span>

<span data-ttu-id="15d12-167">단일 사용자에 대 한 보관 사서함을 사용 하지 않도록 설정 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-167">Run the following command to disable the archive mailbox for a single user.</span></span>
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="15d12-168">(보관 사서함 사용 중인) 조직에서 모든 사용자에 대 한 보관 사서함을 사용 하지 않도록 설정 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-168">Run the following command to disable the archive mailbox for all users in your organization (whose archive mailbox is currently enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a><span data-ttu-id="15d12-169">추가 정보</span><span class="sxs-lookup"><span data-stu-id="15d12-169">More information</span></span>
  
- <span data-ttu-id="15d12-p115">보관 사서함 사용자와 함께 조직의 보존, eDiscovery를 충족 하기 위해 도움말과 요구를 유지 합니다. 예, 사용자의 보관 사서함으로 사서함 콘텐츠를 이동 하려면 조직의 Exchange 보존 정책을 사용할 수 있습니다. 보안에서 콘텐츠 검색 도구를 사용 하면 &amp; 특정 콘텐츠를 사용자의 보관 사서함에 대 한 사용자의 사서함을 검색 하려면 준수 센터는 검색할 수도 있습니다. 및 보관 사서함에 있는 항목의 보존도 소송 보존를 배치 하거나 사용자의 사서함에 Office 365 보존 정책을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-p115">Archive mailboxes help you and your users to meet your organization's retention, eDiscovery, and hold requirements. For example, you can use your organization's Exchange retention policy to move mailbox content to users' archive mailbox. When you use the Content Search tool in the Security &amp; Compliance Center to search a user's mailbox for specific content, the user's archive mailbox will also be searched. And, when you place a Litigation Hold or apply an Office 365 retention policy to a user's mailbox, items in the archive mailbox are also retained.</span></span>
  
- <span data-ttu-id="15d12-p116">보관 사서함 사용 하는 경우 사용자가 자신의 보관 사서함에 메시지를 저장할 수 있습니다. 사용자가 사서함에 액세스할 수 보관 Microsoft Outlook 및 Outlook Web app.를 사용 하 여 사용 하 여 이러한 클라이언트 응용 프로그램 중 하나, 사용자가 자신의 보관 사서함의 메시지를 보려면 및 이동 하거나, 기본 사서함 및 보관 사서함 간의 메시지를 복사할 수 있습니다. 사용자가 자신의 보관 사서함의 복구 가능한 항목 폴더에서 삭제 된 항목 지운 편지함 복구 도구를 사용 하 여 복구도 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-p116">When an archive mailbox is enabled, users can store messages in their archive mailbox. Users can access their archive mailboxes by using Microsoft Outlook and Outlook Web App. Using either of these client applications, users can view messages in their archive mailbox and move or copy messages between their primary mailbox and their archive mailbox. Users can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
- <span data-ttu-id="15d12-p117">보관 사서함 사용 하도록 설정 된 후 조직 활용할 수 기본 Exchange 보존 정책 (메시징 레코드 관리 또는 MRM 정책 라고도 함)에 자동으로 모든 사서함에 할당 됩니다. 보관 사서함 사용 하는 경우 기본 Exchange 보존 정책은 자동으로 다음를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-p117">After archive mailboxes are enabled, your organization can take advantage of the default Exchange retention policy (also called Messaging Records Management or MRM policy) that is automatically assigned to every mailbox. When an archive mailbox is enabled, the default Exchange retention policy automatically does the following:</span></span> 
  
    - <span data-ttu-id="15d12-180">사용자의 기본 사서함에서 보관 사서함으로 2년 이상 된 항목을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-180">Moves items that are two years or older from a user's primary mailbox to their archive mailbox.</span></span> 
    
    - <span data-ttu-id="15d12-181">사용자의 기본 사서함에 있는 복구 가능한 항목 폴더에서 보관 사서함의 복구 가능한 항목 폴더로 14일 이상 된 항목을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-181">Moves items that are 14 days or older from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in their archive mailbox.</span></span>
    
- <span data-ttu-id="15d12-182">보관 사서함 및 Exchange 보존 정책에 대 한 자세한 내용은 다음을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d12-182">For more information about archive mailboxes and Exchange retention policies, see:</span></span>
  
    
  - [<span data-ttu-id="15d12-183">보존 태그 및 보존 정책</span><span class="sxs-lookup"><span data-stu-id="15d12-183">Retention tags and retention policies</span></span>](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [<span data-ttu-id="15d12-184">기본 보존 정책 in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="15d12-184">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [<span data-ttu-id="15d12-185">Office 365 조직 내의 사서함에에서는 보관 및 삭제 정책 설정</span><span class="sxs-lookup"><span data-stu-id="15d12-185">Set up an archive and deletion policy for mailboxes in your Office 365 organization</span></span>](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
