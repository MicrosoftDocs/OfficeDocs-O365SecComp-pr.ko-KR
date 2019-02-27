---
title: Office 365 보안 &amp; 및 준수 센터에서 보관 사서함 사용
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
description: Office 365 보안 &amp; 및 준수 센터를 사용 하 여 조직의 메시지 보존, eDiscovery 및 보존 요구 사항을 지원 하기 위해 보관 사서함을 사용 하도록 설정할 수 있습니다.
ms.openlocfilehash: 763097925ed0910fe9a66e5c556b8a2995df74e6
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296061"
---
# <a name="enable-archive-mailboxes-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="ebb3c-103">Office 365 보안 &amp; 및 준수 센터에서 보관 사서함 사용</span><span class="sxs-lookup"><span data-stu-id="ebb3c-103">Enable archive mailboxes in the Office 365 Security &amp; Compliance Center</span></span>
  
<span data-ttu-id="ebb3c-p101">Office 365 (원본 위치 보관이 라고도 함)의 보관은 사용자에 게 사서함 저장소 공간을 추가로 제공 합니다. 보관 사서함을 켜면 사용자가 Microsoft outlook 및 웹용 outlook (이전의 outlook web App)을 사용 하 여 보관 사서함에 메시지를 액세스 하 고 저장할 수 있습니다. 사용자는 기본 사서함과 해당 보관 사서함 간에 메시지를 이동 하거나 복사할 수도 있습니다. 지운 편지함 복구 도구를 사용 하 여 보관 사서함의 복구 가능한 항목 폴더에서 삭제 된 항목을 복구할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p101">Archiving in Office 365 (also called In-Place Archiving) provides users with additional mailbox storage space. After you turn on archive mailboxes, users can access and store messages in their archive mailboxes by using Microsoft Outlook and Outlook on the web (formerly known as Outlook Web App). Users can also move or copy messages between their primary mailbox and their archive mailbox. They can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
> [!TIP]
> <span data-ttu-id="ebb3c-p102">Office 365에서는 자동 확장 보관 기능과 무제한의 보관 저장소를 제공 합니다. 자동 확장 보관이 켜져 있는 경우 사용자의 보관 사서함에 있는 초기 저장소 할당량에 도달 하면 Office 365에서 자동으로 저장 공간을 추가 합니다. 즉, 사용자에 게 사서함 저장소 공간이 부족 하지 않으며, 처음에 보관 사서함을 사용 하도록 설정 하 고 조직에 대해 자동 확장 보관을 사용 하도록 설정한 후에는 별도로 관리할 필요가 없습니다. 자세한 내용은 [Office 365의 무제한 보관 개요](unlimited-archiving.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p102">Office 365 provides an unlimited amount of archive storage with the auto-expanding archiving feature. When auto-expanding archiving is turned on, and then the initial storage quota in a user's archive mailbox is reached, Office 365 automatically adds additional storage space. This means that users won't run out of mailbox storage space and you won't have to manage anything after you initially enable the archive mailbox and turn on auto-expanding archiving for your organization. For more information, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="ebb3c-112">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="ebb3c-112">Before you begin</span></span>

<span data-ttu-id="ebb3c-p103">보관 사서함을 사용 하거나 사용 하지 않도록 설정 하려면 Exchange Online의 Mail Recipients 역할을 할당 받아야 합니다. 기본적으로이 역할은 Exchange 관리 센터의 **사용 권한** 페이지에 있는 받는 사람 관리 및 조직 관리 역할 그룹에 할당 됩니다. 보안 &amp; 및 준수 센터에서 **보관** 페이지가 표시 되지 않으면 관리자에 게 필요한 사용 권한을 할당 해 달라고 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p103">You have to be assigned the Mail Recipients role in Exchange Online to enable or disable archive mailboxes. By default, this role is assigned to the Recipient Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. If you don't see the **Archive** page in the Security &amp; Compliance Center, ask your administrator to assign you the necessary permissions.</span></span> 
  
## <a name="enable-an-archive-mailbox"></a><span data-ttu-id="ebb3c-116">보관 사서함 사용</span><span class="sxs-lookup"><span data-stu-id="ebb3c-116">Enable an archive mailbox</span></span>
  
1. <span data-ttu-id="ebb3c-117">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-117">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="ebb3c-118">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-118">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="ebb3c-119">보안 &amp; 및 준수 센터의 왼쪽 창에서 **데이터 거 버 넌 스** \> **보관**함을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-119">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="ebb3c-p104">**보관** 페이지가 표시됩니다. **보관 사서함** 열은 각 사용자의 보관 사서함이 사용하도록 설정되었는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p104">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="ebb3c-122">사서함 목록에서 보관 사서함을 사용하도록 설정할 사용자를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-122">In the list of mailboxes, select the user that you want to enable the archive mailbox for.</span></span>
    
    ![선택한 사용자의 세부 정보 창에서 사용을 클릭 하 여 보관 사서함을 사용 하도록 설정 합니다.](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. <span data-ttu-id="ebb3c-124">선택한 사용자에 대 한 세부 정보 창에서 **사용**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-124">In the details pane for the selected user, click **Enable**.</span></span> 
    
    <span data-ttu-id="ebb3c-p105">보관 사서함을 사용 하도록 설정 하면 사용자 사서함에서 사서함에 할당 된 보관 정책 보다 오래 된 항목이 새 보관 사서함으로 이동 됨을 알리는 경고가 표시 됩니다. Exchange Online 사서함에 할당 된 보존 정책의 일부인 기본 보관 정책은 항목이 사서함으로 배달 되거나 사용자가 만든 날짜 후 2 년 후에 항목을 보관 사서함으로 이동 합니다. 자세한 내용은이 문서의 **추가 정보** 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p105">A warning is displayed saying that if you enable the archive mailbox, items in the user's mailbox that are older than the archiving policy assigned to the mailbox will be moved to the new archive mailbox. The default archive policy that is part of the retention policy assigned to Exchange Online mailboxes moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user. For more information, see the **More info** section in this article.</span></span> 
    
6. <span data-ttu-id="ebb3c-128">**예**를 클릭하여 보관 사서함을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-128">Click **Yes** to enable the archive mailbox.</span></span> 
    
    <span data-ttu-id="ebb3c-p106">보관 사서함을 만드는 데 몇 분 정도 걸릴 수 있습니다. 이 파일을 만들 때 **보관 사서함: enabled** 가 선택한 사용자에 대 한 세부 정보 창에 표시 됩니다. 세부 정보 창에서 정보를 업데이트 하려면](media/O365-MDM-Policy-RefreshIcon.gif) 새로 고침 아이콘 **새로 고침** ![을 클릭 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p106">It might take a few moments to create the archive mailbox. When it's created, **Archive mailbox: enabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="ebb3c-p107">Shift 또는 Ctrl 키를 사용해 여러 사서함을 선택하여 보관함을 대량으로 사용하도록 설정할 수도 있습니다. 여러 사서함을 선택한 후 세부 정보 창에서 기타 옵션을 클릭합니다. 그런 후에 보관함에서 **사용**을 클릭합니다. </span><span class="sxs-lookup"><span data-stu-id="ebb3c-p107">You can also bulk-enable archive mailboxes by selecting multiple users with disabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Enable** in the details pane.</span></span> 
  
## <a name="disable-an-archive-mailbox"></a><span data-ttu-id="ebb3c-134">보관 사서함 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="ebb3c-134">Disable an archive mailbox</span></span>
  
<span data-ttu-id="ebb3c-p108">보안 &amp; 및 준수 센터의 **보관** 페이지를 사용 하 여 사용자의 보관 사서함을 사용 하지 않도록 설정할 수도 있습니다. 보관 사서함을 사용 하지 않도록 설정한 후에는 사용 하지 않도록 설정 하 고 30 일 이내에 사용자의 기본 사서함에 다시 연결할 수 있습니다. 이 경우 보관 사서함의 원래 내용이 복원 됩니다. 30 일이 지나면 원래 보관 사서함의 내용은 영구적으로 삭제 되며 복구할 수 없습니다. 따라서 사용 하지 않도록 설정한 후 30 일 넘게 보관을 다시 사용 하도록 설정 하면 새 보관 사서함이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p108">You can also use the **Archive** page in the Security &amp; Compliance Center to disable a user's archive mailbox. After you disable an archive mailbox, you can reconnect it to the user's primary mailbox within 30 days of disabling it. In this case, the original contents of the archive mailbox are restored. After 30 days, the contents of the original archive mailbox are permanently deleted and can't be recovered. So if you re-enable the archive more than 30 days after disabling it, a new archive mailbox is created.</span></span> 
  
<span data-ttu-id="ebb3c-p109">사용자 사서함에 할당 된 기본 보관 정책이 항목을 배달 한 날짜 후 2 년 후에 항목을 보관 사서함으로 이동 합니다. 사용자의 보관 사서함을 사용 하지 않도록 설정 하면 사서함 항목에 대 한 아무 작업도 수행 되지 않으며 사용자의 기본 사서함에 남아 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p109">Note that the default archive policy assigned to users' mailboxes moves items to the archive mailbox two years after the date the item is delivered. If you disable a user's archive mailbox, no action will be taken on mailbox items and they will remain in the user's primary mailbox.</span></span>
  
<span data-ttu-id="ebb3c-142">보관 사서함을 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="ebb3c-142">To disable an archive mailbox:</span></span>
  
1. <span data-ttu-id="ebb3c-143">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-143">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="ebb3c-144">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-144">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="ebb3c-145">보안 &amp; 및 준수 센터의 왼쪽 창에서 **데이터 거 버 넌 스** \> **보관**함을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-145">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="ebb3c-p110">**보관** 페이지가 표시됩니다. **보관 사서함** 열은 각 사용자의 보관 사서함이 사용하도록 설정되었는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p110">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="ebb3c-148">사서함 목록에서 보관 사서함을 사용하지 않도록 설정할 사용자를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-148">In the list of mailboxes, select the user that you want to disable the archive mailbox for.</span></span>
    
5. <span data-ttu-id="ebb3c-149">세부 정보 창에서 **사용 안 함**을 클릭합니다. </span><span class="sxs-lookup"><span data-stu-id="ebb3c-149">In the details pane, click **Disable**.</span></span> 
    
    <span data-ttu-id="ebb3c-150">30 일 동안 보관 사서함을 다시 사용 하도록 설정 하 고 30 일 후에 보관 함의 모든 정보가 영구적으로 삭제 됨을 알리는 경고 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-150">A warning message is displayed saying that you'll have 30 days to re-enable the archive mailbox, and that after 30 days, all information in the archive will be permanently deleted.</span></span> 
    
6. <span data-ttu-id="ebb3c-151">**예**를 클릭하여 보관 사서함을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-151">Click **Yes** to disable the archive mailbox.</span></span> 
    
    <span data-ttu-id="ebb3c-p111">보관 사서함을 사용 하지 않도록 설정 하는 데 몇 분 정도 걸릴 수 있습니다. 사용 하지 않도록 설정 된 경우 **보관 사서함: 사용 안 함** 이 선택한 사용자의 세부 정보 창에 표시 됩니다. 세부 정보 창에서 정보를 업데이트 하려면](media/O365-MDM-Policy-RefreshIcon.gif) 새로 고침 아이콘 **새로 고침** ![을 클릭 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p111">It might take a few moments to disable the archive mailbox. When it's disabled, **Archive mailbox: disabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="ebb3c-p112">Shift 또는 Ctrl 키를 사용해 보관 사서함이 사용하도록 설정된 여러 사용자를 선택하여 보관 사서함을 사용하지 않도록 일괄 설정할 수도 있습니다. 여러 사서함을 선택한 후 세부 정보 창에서 **사용 안 함**을 클릭합니다. </span><span class="sxs-lookup"><span data-stu-id="ebb3c-p112">You can also bulk-disable archive mailboxes by selecting multiple users with enabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Disable** in the details pane.</span></span> 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a><span data-ttu-id="ebb3c-157">Exchange Online PowerShell을 사용 하 여 보관 사서함을 사용 하거나 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="ebb3c-157">Use Exchange Online PowerShell to enable or disable archive mailboxes</span></span>

<span data-ttu-id="ebb3c-p113">또한 Exchange Online PowerShell을 사용 하 여 보관 사서함을 사용 하도록 설정할 수 있습니다. PowerShell을 사용 하는 주요 이유는 조직의 모든 사용자에 대해 보관 사서함을 빠르게 사용 하도록 설정할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p113">You can also use Exchange Online PowerShell to enable archive mailboxes. The primary reason to use PowerShell is that you can quickly enable the archive mailbox for all users in your organization.</span></span>

<span data-ttu-id="ebb3c-p114">첫 번째 단계는 Exchange Online PowerShell에 연결 하는 것입니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p114">The first step is to connect to Exchange Online PowerShell. For instructions, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="ebb3c-162">Exchange Online에 연결 하 고 나면 다음 섹션의 명령을 실행 하 여 보관 사서함을 사용 하거나 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-162">After you're connected to Exchange Online, you can run the commands in the following sections to enable or disable archive mailboxes.</span></span>

### <a name="enable-archive-mailboxes"></a><span data-ttu-id="ebb3c-163">보관 사서함 사용</span><span class="sxs-lookup"><span data-stu-id="ebb3c-163">Enable archive mailboxes</span></span>

<span data-ttu-id="ebb3c-164">다음 명령을 실행 하 여 단일 사용자에 대해 보관 사서함을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-164">Run the following command to enable the archive mailbox for a single user.</span></span>
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="ebb3c-165">다음 명령을 실행 하 여 조직의 모든 사용자 (보관 사서함 현재 사용 하지 않도록 설정 되어 있지 않음)에서 보관 사서함을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-165">Run the following command to enable the archive mailbox for all users in your organization (whose archive mailbox is currently not enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a><span data-ttu-id="ebb3c-166">보관 사서함을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="ebb3c-166">Disable archive mailboxes</span></span>

<span data-ttu-id="ebb3c-167">다음 명령을 실행 하 여 단일 사용자에 대해 보관 사서함을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-167">Run the following command to disable the archive mailbox for a single user.</span></span>
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="ebb3c-168">다음 명령을 실행 하 여 조직의 모든 사용자 (보관 사서함 현재 사용 가능)에 대 한 보관 사서함을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-168">Run the following command to disable the archive mailbox for all users in your organization (whose archive mailbox is currently enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a><span data-ttu-id="ebb3c-169">추가 정보</span><span class="sxs-lookup"><span data-stu-id="ebb3c-169">More information</span></span>
  
- <span data-ttu-id="ebb3c-p115">보관 사서함을 통해 조직의 보존, eDiscovery 및 보존 요구 사항을 충족 하는 사용자를 지원할 수 있습니다. 예를 들어 조직의 Exchange 보존 정책을 사용 하 여 사서함 콘텐츠를 사용자의 보관 사서함으로 이동할 수 있습니다. 보안 &amp; 및 준수 센터의 콘텐츠 검색 도구를 사용 하 여 사용자의 사서함에서 특정 콘텐츠를 검색 하는 경우 사용자의 보관 사서함도 검색 됩니다. 또한 소송 보존을 수행 하거나 사용자 사서함에 Office 365 유지 정책을 적용 하는 경우 보관 사서함의 항목도 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p115">Archive mailboxes help you and your users to meet your organization's retention, eDiscovery, and hold requirements. For example, you can use your organization's Exchange retention policy to move mailbox content to users' archive mailbox. When you use the Content Search tool in the Security &amp; Compliance Center to search a user's mailbox for specific content, the user's archive mailbox will also be searched. And, when you place a Litigation Hold or apply an Office 365 retention policy to a user's mailbox, items in the archive mailbox are also retained.</span></span>
  
- <span data-ttu-id="ebb3c-p116">보관 사서함을 사용 하도록 설정 하면 사용자가 보관 사서함에 메시지를 저장할 수 있습니다. 사용자는 Microsoft outlook 및 웹용 Outlook을 사용 하 여 보관 사서함에 액세스할 수 있습니다. 이러한 클라이언트 응용 프로그램 중 하나를 사용 하면 사용자가 자신의 보관 사서함에서 메시지를 보고 기본 사서함과 해당 보관 사서함 간에 메시지를 이동 하거나 복사할 수 있습니다. 또한 사용자는 지운 편지함 복구 도구를 사용 하 여 보관 사서함의 복구 가능한 항목 폴더에서 삭제 된 항목을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p116">When an archive mailbox is enabled, users can store messages in their archive mailbox. Users can access their archive mailboxes by using Microsoft Outlook and Outlook on the web. Using either of these client applications, users can view messages in their archive mailbox and move or copy messages between their primary mailbox and their archive mailbox. Users can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
- <span data-ttu-id="ebb3c-p117">보관 사서함을 사용 하도록 설정한 후에는 조직에서 모든 사서함에 자동으로 할당 되는 기본 Exchange 보존 정책 (메시징 레코드 관리 또는 mrm 정책)을 활용할 수 있습니다. 보관 사서함을 사용 하도록 설정 하면 기본 Exchange 보존 정책이 자동으로 다음 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-p117">After archive mailboxes are enabled, your organization can take advantage of the default Exchange retention policy (also called Messaging Records Management or MRM policy) that is automatically assigned to every mailbox. When an archive mailbox is enabled, the default Exchange retention policy automatically does the following:</span></span> 
  
    - <span data-ttu-id="ebb3c-180">사용자의 기본 사서함에서 보관 사서함으로 2년 이상 된 항목을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-180">Moves items that are two years or older from a user's primary mailbox to their archive mailbox.</span></span> 
    
    - <span data-ttu-id="ebb3c-181">사용자의 기본 사서함에 있는 복구 가능한 항목 폴더에서 보관 사서함의 복구 가능한 항목 폴더로 14일 이상 된 항목을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-181">Moves items that are 14 days or older from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in their archive mailbox.</span></span>
    
- <span data-ttu-id="ebb3c-182">보관 사서함 및 Exchange 보존 정책에 대 한 자세한 내용은 다음 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ebb3c-182">For more information about archive mailboxes and Exchange retention policies, see:</span></span>
  
    
  - [<span data-ttu-id="ebb3c-183">보존 태그 및 보존 정책</span><span class="sxs-lookup"><span data-stu-id="ebb3c-183">Retention tags and retention policies</span></span>](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [<span data-ttu-id="ebb3c-184">Exchange Online의 기본 보존 정책</span><span class="sxs-lookup"><span data-stu-id="ebb3c-184">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [<span data-ttu-id="ebb3c-185">Office 365 조 직의 사서함에 대 한 보관 및 삭제 정책 설정</span><span class="sxs-lookup"><span data-stu-id="ebb3c-185">Set up an archive and deletion policy for mailboxes in your Office 365 organization</span></span>](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
