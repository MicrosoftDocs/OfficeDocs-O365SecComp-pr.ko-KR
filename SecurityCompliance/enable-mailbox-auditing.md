---
title: Office 365에서 사서함 감사 사용
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
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: Office 365에서 사서함 감사 로깅 사서함 소유자, 대리인 및 관리자의 사서함 액세스를 기록 하도록 켤 수 있습니다. 기본적으로 Office 365에서 사서함 감사 설정 되지 않은 합니다. 사서함에 대 한 로깅 사서함 감사를 사용 하도록 설정한 후에 사서함에 수행 하는 작업에 대 한 Office 365 감사 로그를 검색할 수 있습니다.
ms.openlocfilehash: 6d3de226e7c0e03be824b14e1b16fadaae3f040e
ms.sourcegitcommit: 8294182d4dd124f035a221de0b90159ef7eec4ae
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/19/2018
ms.locfileid: "25639667"
---
# <a name="enable-mailbox-auditing-in-office-365"></a><span data-ttu-id="1c168-105">Office 365에서 사서함 감사 사용</span><span class="sxs-lookup"><span data-stu-id="1c168-105">Enable mailbox auditing in Office 365</span></span>
  
<span data-ttu-id="1c168-p102">Office 365에서 사서함 감사 로깅 사서함 소유자, 대리인 및 관리자의 사서함 액세스를 기록 하도록 켤 수 있습니다. 기본적으로 Office 365에서 사서함 감사 설정 되지 않은 합니다. 즉, 이벤트를 감사 해야 사서함은 사서함 활동에 대 한 Office 365 감사 로그를 검색 하는 경우 결과에 나타나지 않습니다. 하지만 사용자 사서함에 대 한 로깅 사서함 감사를 설정한 후 사서함 활동에 대 한 감사 로그를 검색할 수 있습니다. 또한 사서함 감사 로깅을 사용 대리인, 관리자가 수행 된 일부 작업에 및 소유자가 기본적으로 기록 됩니다. 로그 (한 다음 검색)에 추가 작업 단계 3을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1c168-p102">In Office 365, you can turn on mailbox audit logging to log mailbox access by mailbox owners, delegates, and administrators. By default, mailbox auditing in Office 365 isn't turned on. That means mailbox auditing events won't appear in the results when you search the Office 365 audit log for mailbox activity. But after you turn on mailbox audit logging for a user mailbox, you can search the audit log for mailbox activity. Additionally, when mailbox audit logging is turned on, some actions performed by administrators, delegates, and owners are logged by default. To log (and then search for) additional actions, see Step 3.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="1c168-112">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="1c168-112">Before you begin</span></span>
  
- <span data-ttu-id="1c168-p103">Exchange Online PowerShell을 사용 하 여 사서함을 사용 하도록 설정 해야하는 로깅 감사 합니다. Office 365 보안을 사용할 수 없습니다 &amp; 준수 센터 또는 Exchange 관리 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p103">You have to use Exchange Online PowerShell to enable mailbox audit logging. You can't use the Office 365 Security &amp; Compliance Center or the Exchange admin center.</span></span>
    
- <span data-ttu-id="1c168-115">사서함 감사는 Office 365 그룹 또는 팀이 Microsoft에서 팀과 관련 된 사서함에 대 한 로깅을 활성화할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-115">You can't enable mailbox audit logging for the mailbox that's associated with an Office 365 Group or a team in Microsoft Teams.</span></span>
    
- <span data-ttu-id="1c168-116">사용자의 사서함에 대해 모든 액세스 권한이 할당된 관리자는 대리인으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-116">An administrator who has been assigned the Full Access permission to a user's mailbox is considered a delegate user.</span></span>
  
## <a name="step-1-connect-to-exchange-online-powershell"></a><span data-ttu-id="1c168-117">1 단계: Exchange Online PowerShell에 연결</span><span class="sxs-lookup"><span data-stu-id="1c168-117">Step 1: Connect to Exchange Online PowerShell</span></span>

1. <span data-ttu-id="1c168-118">로컬 컴퓨터에서 Windows PowerShell을 열고 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-118">On your local computer, open Windows PowerShell and run the following command.</span></span>
   
    ```
    $UserCredential = Get-Credential
    ```

2. <span data-ttu-id="1c168-119">**Windows PowerShell 자격 증명 요청** 대화 상자에서 Office 365 전역 관리자 계정의 사용자 이름 및 암호를 입력한 다음 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-119">In the **Windows PowerShell Credential Request** dialog box, type user name and password for an Office 365 global admin account, and then click **OK**.</span></span>
    
3. <span data-ttu-id="1c168-120">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-120">Run the following command:</span></span>
    
    ```
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
    ```

3. <span data-ttu-id="1c168-121">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-121">Run the following command.</span></span>

    ```
    Import-PSSession $Session
    ```
   
4. <span data-ttu-id="1c168-122">Exchange Online 조직에 연결 하려는 있는지를 확인 하려면 조직에 있는 모든 사서함의 목록을 가져오려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-122">To verify that you're connected to your Exchange Online organization, run the following command to get a list of all the mailboxes in your organization.</span></span>
    
    ```
    Get-Mailbox
    ```
  
<span data-ttu-id="1c168-123">자세한 내용은 하거나 Exchange Online 조직에 연결할 때 문제가 있으면 [원격 PowerShell을 사용 하는 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?LinkId=517283)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1c168-123">For more information or if you have problems connecting to your Exchange Online organization, see [Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283).</span></span>
  
## <a name="step-2-enable-mailbox-audit-logging"></a><span data-ttu-id="1c168-124">2단계: 사서함 감사 로깅 사용</span><span class="sxs-lookup"><span data-stu-id="1c168-124">Step 2: Enable mailbox audit logging</span></span>

<span data-ttu-id="1c168-p104">Exchange Online 조직에 연결한 후 PowerShell을 사용 하 여 사서함에 대 한 로깅 사서함 감사를 사용 하도록 설정 합니다. 또는 조직에서 모든 사서함에 대 한 사서함 감사를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p104">After you connect to your Exchange Online organization, use PowerShell to enable mailbox audit logging for a mailbox. Alternatively, you can enable mailbox auditing for all mailboxes in your organization.</span></span>
  
<span data-ttu-id="1c168-127">사서함 감사 Pilar Pinilla의 사서함에 대 한 로깅을 설정 하는이 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-127">This example enables mailbox audit logging for Pilar Pinilla's mailbox.</span></span>
  
```
Set-Mailbox -Identity "Pilar Pinilla" -AuditEnabled $true
```

<span data-ttu-id="1c168-128">아래 예에서는 조직의 모든 사용자 사서함에 대한 사서함 감사 로깅을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-128">This example enables mailbox audit logging for all user mailboxes in your organization.</span></span>
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditEnabled $true
```
  
## <a name="step-3-specify-owner-actions-to-audit"></a><span data-ttu-id="1c168-129">3단계: 감사할 소유자 작업 지정</span><span class="sxs-lookup"><span data-stu-id="1c168-129">Step 3: Specify owner actions to audit</span></span>

<span data-ttu-id="1c168-p105">사서함에 대 한 감사 사용 하도록 설정 하면 사서함 소유자가 수행 된 일부 작업은 기본적으로 감사 됩니다. 감사 하는 기타 소유자 작업을 지정 해야 합니다. 목록 및 설명은 기본적으로 로깅되는 소유자 작업 및 감사할 수 있는 다른 작업에 대 한 [사서함 감사 작업](#mailbox-auditing-actions) 섹션에서 표를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p105">When you enable auditing for a mailbox, some actions performed by the mailbox owner are audited by default. You have to specify other owner actions to audit. See the table in the [Mailbox auditing actions](#mailbox-auditing-actions) section for a list and description of owner actions that are logged by default and the other actions that can be audited.</span></span> 
  
<span data-ttu-id="1c168-p106">이 예에서는 Pilar Pinilla의 사서함에 대 한 감사 사서함에 **MailboxLogin** 및 **HardDelete** 소유자 작업을 추가 합니다. 이 예제는 사서함 감사 기능이 이미 활성화 된이 사서함에 대 한 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p106">This example adds the **MailboxLogin** and **HardDelete** owner actions to mailbox auditing for Pilar Pinilla's mailbox. This example assumes that mailbox auditing has already been enabled for this mailbox.</span></span> 

```
Set-Mailbox "Pilar Pinilla" -AuditOwner @{Add="MailboxLogin","HardDelete"}
```

<span data-ttu-id="1c168-p107">이 예에서는 사서함 감사 Don 홀 사서함에 대 한 로깅을 사용 하도록 설정 하 고 사서함 소유자에 의해 수행 되는 **MailboxLogin** 작업만 기록 됩니다 지정 합니다. Note이 예제에서는 기본 UpdateFolderPermissions 작업을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p107">This example enables mailbox audit logging for Don Hall's mailbox and specifies that only the **MailboxLogin** action performed by the mailbox owner will be logged. Note that this example overwrites the default UpdateFolderPermissions action.</span></span> 
  
```
Set-Mailbox "Don Hall" -AuditEnabled $true -AuditOwner MailboxLogin
```
   
<span data-ttu-id="1c168-p108">조직에서 모든 사서함에 **MailboxLogin**, **HardDelete**및 **SoftDelete** 소유자 작업을 추가 하는이 예제입니다. 이 예제는 사서함 감사 기능이 이미 활성화 된 모든 사서함에 대 한 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p108">This example adds the **MailboxLogin**, **HardDelete**, and **SoftDelete** owner actions to all mailboxes in the organization. This example assumes that mailbox auditing has already been enabled for all mailboxes.</span></span> 
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditOwner @{Add="MailboxLogin","HardDelete","SoftDelete"}
```
  
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="1c168-139">작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="1c168-139">How do you know this worked?</span></span>

<span data-ttu-id="1c168-140">사서함에 대한 사서함 감사 로깅이 사용하도록 설정되었는지 확인하려면 **Get-Mailbox** cmdlet을 사용하여 해당 사서함에 대한 감사 설정을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-140">To verify that you have successfully enabled mailbox audit logging for a mailbox, use the **Get-Mailbox** cmdlet to retrieve the auditing settings for that mailbox.</span></span> 
  
<span data-ttu-id="1c168-141">아래 예에서는 강진영에 대한 감사 설정을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-141">This example retrieves the auditing settings for Pilar Pinilla.</span></span>

```
Get-Mailbox "Pilar Pinilla"| FL Audit*
```
   
<span data-ttu-id="1c168-142">아래 예에서는 조직 내 모든 사용자 사서함에 대한 감사 설정을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-142">This example retrieves the auditing settings for all user mailboxes in your organization.</span></span>

```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,Audit*
```
   
<span data-ttu-id="1c168-143">**AuditEnabled** 속성의 **True** 값을 확인 해당 사서함 감사 로깅을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-143">A value of **True** for the **AuditEnabled** property verifies that mailbox audit logging is enabled.</span></span> 
    
## <a name="mailbox-auditing-actions"></a><span data-ttu-id="1c168-144">사서함 감사 작업</span><span class="sxs-lookup"><span data-stu-id="1c168-144">Mailbox auditing actions</span></span>
  
<span data-ttu-id="1c168-p109">다음 표에서 사서함으로 기록 될 수 있는 작업이 나와 감사 로깅. 표에 서로 다른 사용자 로그온 유형에 대 한 동작을 기록할 수 있습니다를 포함 합니다. 테이블을 **No** 해당 로그온 형식에 대 한 동작을 기록할 수 없는 나타냅니다. 별표 ( **\*** )를 나타냅니다 사서함에 대해 활성화 되어 사서함 감사 로깅 때 기본적으로는 작업 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p109">The following table lists the actions that can be logged by mailbox audit logging. The table includes which action can be logged for the different user logon types. In the table, a **No** indicates that an action can't be logged for that logon type. An asterisk ( **\*** ) indicates that the action is logged by default when mailbox audit logging is enabled for the mailbox.</span></span> 
  
|<span data-ttu-id="1c168-149">**작업**</span><span class="sxs-lookup"><span data-stu-id="1c168-149">**Action**</span></span>|<span data-ttu-id="1c168-150">**설명**</span><span class="sxs-lookup"><span data-stu-id="1c168-150">**Description**</span></span>|<span data-ttu-id="1c168-151">**Admin**</span><span class="sxs-lookup"><span data-stu-id="1c168-151">**Admin**</span></span>|<span data-ttu-id="1c168-152">**대리인\*\*\***</span><span class="sxs-lookup"><span data-stu-id="1c168-152">**Delegate\*\*\***</span></span>|<span data-ttu-id="1c168-153">**소유자**</span><span class="sxs-lookup"><span data-stu-id="1c168-153">**Owner**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1c168-154">**복사**</span><span class="sxs-lookup"><span data-stu-id="1c168-154">**Copy**</span></span> <br/> |<span data-ttu-id="1c168-155">메시지가 다른 폴더에 복사되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-155">A message was copied to another folder.</span></span>  <br/> |<span data-ttu-id="1c168-156">예</span><span class="sxs-lookup"><span data-stu-id="1c168-156">Yes</span></span>  <br/> |<span data-ttu-id="1c168-157">아니요</span><span class="sxs-lookup"><span data-stu-id="1c168-157">No</span></span>  <br/> |<span data-ttu-id="1c168-158">아니요</span><span class="sxs-lookup"><span data-stu-id="1c168-158">No</span></span>  <br/> |
|<span data-ttu-id="1c168-159">**만들기**</span><span class="sxs-lookup"><span data-stu-id="1c168-159">**Create**</span></span> <br/> |<span data-ttu-id="1c168-p110">사서함, 일정, 연락처, 메모 또는 작업 폴더에서 항목을 만들 예, 새 모임 요청을 생성 됩니다. 참고는 만들기, 보내기 또는 메시지를 받는 감사 되지 않습니다. 또한 사서함 폴더 만들기 (영문)을 감사 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p110">An item is created in the Calendar, Contacts, Notes, or Tasks folder in the mailbox; for example, a new meeting request is created. Note that creating, sending, or receiving a message isn't audited. Also, creating a mailbox folder is not audited.</span></span>  <br/> |<span data-ttu-id="1c168-163">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-163">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-164">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-164">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-165">예</span><span class="sxs-lookup"><span data-stu-id="1c168-165">Yes</span></span>  <br/> |
|<span data-ttu-id="1c168-166">**FolderBind**</span><span class="sxs-lookup"><span data-stu-id="1c168-166">**FolderBind**</span></span> <br/> |<span data-ttu-id="1c168-p111">사서함 폴더에 액세스했습니다. 관리자 또는 대리인이 사서함을 열 때에도 작업이 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p111">A mailbox folder was accessed. This action is also logged when the admin or delegate opens the mailbox.</span></span>  <br/> |<span data-ttu-id="1c168-169">예</span><span class="sxs-lookup"><span data-stu-id="1c168-169">Yes</span></span>  <br/> |<span data-ttu-id="1c168-170">예\*\*</span><span class="sxs-lookup"><span data-stu-id="1c168-170">Yes\*\*</span></span>  <br/> |<span data-ttu-id="1c168-171">아니요</span><span class="sxs-lookup"><span data-stu-id="1c168-171">No</span></span>  <br/> |
|<span data-ttu-id="1c168-172">**HardDelete**</span><span class="sxs-lookup"><span data-stu-id="1c168-172">**HardDelete**</span></span> <br/> |<span data-ttu-id="1c168-173">메시지가 복구 가능한 항목 폴더에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-173">A message was purged from the Recoverable Items folder.</span></span>  <br/> |<span data-ttu-id="1c168-174">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-174">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-175">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-175">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-176">예</span><span class="sxs-lookup"><span data-stu-id="1c168-176">Yes</span></span>  <br/> |
|<span data-ttu-id="1c168-177">**MailboxLogin**</span><span class="sxs-lookup"><span data-stu-id="1c168-177">**MailboxLogin**</span></span> <br/> |<span data-ttu-id="1c168-178">사용자가 자신의 사서함에 로그인했습니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-178">The user signed in to their mailbox.</span></span>  <br/> |<span data-ttu-id="1c168-179">아니요</span><span class="sxs-lookup"><span data-stu-id="1c168-179">No</span></span>  <br/> |<span data-ttu-id="1c168-180">아니요</span><span class="sxs-lookup"><span data-stu-id="1c168-180">No</span></span>  <br/> |<span data-ttu-id="1c168-181">예</span><span class="sxs-lookup"><span data-stu-id="1c168-181">Yes</span></span>  <br/> |
|<span data-ttu-id="1c168-182">**MessageBind**</span><span class="sxs-lookup"><span data-stu-id="1c168-182">**MessageBind**</span></span> <br/> |<span data-ttu-id="1c168-183">메시지가 미리 보기 창에 표시되거나 열렸습니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-183">A message was viewed in the preview pane or opened.</span></span>  <br/> |<span data-ttu-id="1c168-184">예</span><span class="sxs-lookup"><span data-stu-id="1c168-184">Yes</span></span>  <br/> |<span data-ttu-id="1c168-185">아니요</span><span class="sxs-lookup"><span data-stu-id="1c168-185">No</span></span>  <br/> |<span data-ttu-id="1c168-186">아니요</span><span class="sxs-lookup"><span data-stu-id="1c168-186">No</span></span>  <br/> |
|<span data-ttu-id="1c168-187">**Move**</span><span class="sxs-lookup"><span data-stu-id="1c168-187">**Move**</span></span> <br/> |<span data-ttu-id="1c168-188">메시지가 다른 폴더로 이동했습니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-188">A message was moved to another folder.</span></span>  <br/> |<span data-ttu-id="1c168-189">예</span><span class="sxs-lookup"><span data-stu-id="1c168-189">Yes</span></span>  <br/> |<span data-ttu-id="1c168-190">예</span><span class="sxs-lookup"><span data-stu-id="1c168-190">Yes</span></span>  <br/> |<span data-ttu-id="1c168-191">예</span><span class="sxs-lookup"><span data-stu-id="1c168-191">Yes</span></span>  <br/> |
|<span data-ttu-id="1c168-192">**MoveToDeletedItems**</span><span class="sxs-lookup"><span data-stu-id="1c168-192">**MoveToDeletedItems**</span></span> <br/> |<span data-ttu-id="1c168-193">메시지가 삭제되어 지운 편지함 폴더로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-193">A message was deleted and moved to the Deleted Items folder.</span></span>  <br/> |<span data-ttu-id="1c168-194">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-194">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-195">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-195">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-196">예</span><span class="sxs-lookup"><span data-stu-id="1c168-196">Yes</span></span>  <br/> |
|<span data-ttu-id="1c168-197">**SendAs**</span><span class="sxs-lookup"><span data-stu-id="1c168-197">**SendAs**</span></span> <br/> |<span data-ttu-id="1c168-p112">메시지가 SendAs 권한을 사용하여 전송되었습니다. 즉 사서함 소유자가 보낸 것처럼 보이도록 하여 다른 사용자가 메시지를 보냈습니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p112">A message was sent using the SendAs permission. This means another user sent the message as though it came from the mailbox owner.</span></span>  <br/> |<span data-ttu-id="1c168-200">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-200">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-201">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-201">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-202">아니요</span><span class="sxs-lookup"><span data-stu-id="1c168-202">No</span></span>  <br/> |
|<span data-ttu-id="1c168-203">**SendOnBehalf**</span><span class="sxs-lookup"><span data-stu-id="1c168-203">**SendOnBehalf**</span></span> <br/> |<span data-ttu-id="1c168-p113">메시지가 SendOnBehalf 권한을 사용하여 전송되었습니다. 즉 다른 사용자가 사서함 소유자 대신에 메시지를 보냈습니다. 받는 사람은 메시지를 대신 보낸 사용자와 해당 메시지를 실제로 보낸 사용자를 메시지에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p113">A message was sent using the SendOnBehalf permission. This means another user sent the message on behalf of the mailbox owner. The message indicates to the recipient who the message was sent on behalf of and who actually sent the message.</span></span>  <br/> |<span data-ttu-id="1c168-207">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-207">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-208">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-208">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-209">아니요</span><span class="sxs-lookup"><span data-stu-id="1c168-209">No</span></span>  <br/> |
|<span data-ttu-id="1c168-210">**SoftDelete**</span><span class="sxs-lookup"><span data-stu-id="1c168-210">**SoftDelete**</span></span> <br/> |<span data-ttu-id="1c168-p114">메시지가 지운 편지함 폴더에서 삭제되어가 영구적으로 삭제되었습니다. 소프트 삭제된 항목이 복구 가능한 항목 폴더로 이동됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p114">A message was permanently deleted or deleted from the Deleted Items folder. Soft-deleted items are moved to the Recoverable Items folder.</span></span>  <br/> |<span data-ttu-id="1c168-213">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-213">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-214">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-214">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-215">예</span><span class="sxs-lookup"><span data-stu-id="1c168-215">Yes</span></span>  <br/> |
|<span data-ttu-id="1c168-216">**업데이트**</span><span class="sxs-lookup"><span data-stu-id="1c168-216">**Update**</span></span> <br/> |<span data-ttu-id="1c168-217">메시지 또는 해당 속성이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-217">A message or its properties was changed.</span></span>  <br/> |<span data-ttu-id="1c168-218">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-218">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-219">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-219">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-220">예</span><span class="sxs-lookup"><span data-stu-id="1c168-220">Yes</span></span>  <br/> |
|<span data-ttu-id="1c168-221">**UpdateCalendarDelegation**</span><span class="sxs-lookup"><span data-stu-id="1c168-221">**UpdateCalendarDelegation**</span></span> <br/> |<span data-ttu-id="1c168-p115">일정 위임 사서함에 할당 합니다. 일정 위임에 사서함 소유자의 일정을 관리 하는 동일한 조직 권한을에서 다른 사용자를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p115">A calendar delegation was assigned to a mailbox. Calendar delegation gives someone else in the same organization permissions to manage the mailbox owner's calendar.</span></span>  <br/> |<span data-ttu-id="1c168-224">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-224">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-225">아니요</span><span class="sxs-lookup"><span data-stu-id="1c168-225">No</span></span>  <br/> |<span data-ttu-id="1c168-226">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-226">Yes\*</span></span>  <br/> |
|<span data-ttu-id="1c168-227">**UpdateFolderPermissions**</span><span class="sxs-lookup"><span data-stu-id="1c168-227">**UpdateFolderPermissions**</span></span> <br/> |<span data-ttu-id="1c168-p116">폴더 사용 권한 변경 되었습니다. 폴더 사용 권한 제어 조직에 있는 사용자 사서함 및 해당 폴더에 있는 메시지의 폴더에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p116">A folder permission was changed. Folder permissions control which users in your organization can access folders in a mailbox and the messages located in those folders.</span></span>  <br/> |<span data-ttu-id="1c168-230">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-230">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-231">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-231">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-232">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-232">Yes\*</span></span>  <br/> |
|<span data-ttu-id="1c168-233">**UpdateInboxRules**</span><span class="sxs-lookup"><span data-stu-id="1c168-233">**UpdateInboxRules**</span></span> <br/> |<span data-ttu-id="1c168-p117">받은 편지함 규칙 추가, 제거 또는 변경 되었음을 합니다. 받은 편지함 규칙을 지정 된 조건에 따라 사용자의 받은 편지함의 메시지를 처리 하는 데 사용 되 하 고 지정 된 폴더로 메시지 이동 하거나 삭제 하는 메시지와 같은 규칙의 조건이 충족 되 면 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p117">An inbox rule has been added, removed, or changed. Inbox rules are used to process messages in the user's Inbox based on the specified conditions and take actions when the conditions of a rule are met, such as moving a message to a specified folder or deleting a message.</span></span>  <br/> |<span data-ttu-id="1c168-236">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-236">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-237">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-237">Yes\*</span></span>  <br/> |<span data-ttu-id="1c168-238">예\*</span><span class="sxs-lookup"><span data-stu-id="1c168-238">Yes\*</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="1c168-239"><sup>\*</sup>사서함에 대 한 감사 사용 하도록 설정 하는 경우 기본적으로 감사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-239"><sup>\*</sup> Audited by default if auditing is enabled for a mailbox.</span></span><br/><br/>  <span data-ttu-id="1c168-p118"><sup>\*\*</sup>대리자에 의해 수행 되는 폴더 바인딩 작업에 대 한 항목 통합 됩니다. 하나의 로그 항목은 24 시간의 시간 범위 내에서 개별 폴더 액세스에 대 한 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p118"><sup>\*\*</sup> Entries for folder bind actions performed by delegates are consolidated. One log entry is generated for individual folder access within a time span of 24 hours.</span></span><br/><br/><span data-ttu-id="1c168-242"><sup>\*\*\*</sup>관리자에 게 사용자의 사서함에 대 한 전체 액세스 권한을 할당 된 대리인 사용자로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-242"><sup>\*\*\*</sup> An administrator who has been assigned the Full Access permission to a user's mailbox is considered a delegate user.</span></span> 
  
<span data-ttu-id="1c168-p119">특정 유형의 사서함 감사 하기 위한 작업을 더이상 필요 하는 경우에 이러한 작업을 사용 하지 않도록 설정 하는 사서함 감사 로깅 구성을 수정 해야 합니다. 기존 로그 항목의 외에 감사 로그 항목에 대 한 보존 기간 제한에 도달할 때까지 삭제 되지 않습니다. 감사 로그 항목에 대 한 보존 기간에 대 한 자세한 내용은 [Office 365 보안 및 규정 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md#before-you-begin)의 "시작 하기 전에" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1c168-p119">If you no longer require certain types of mailbox actions to be audited, you should modify the mailbox's audit logging configuration to disable those actions. Existing log entries aren't purged until the retention age limit for audit log entries is reached. For more information about the retention age for audit log entries, see the "Before you begin" section in [Search the audit log in the Office 365 Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md#before-you-begin).</span></span>
  
## <a name="more-infotab"></a>[<span data-ttu-id="1c168-246">추가 정보</span><span class="sxs-lookup"><span data-stu-id="1c168-246">More info</span></span>](#tab/)
  
- <span data-ttu-id="1c168-p120">Office 365 감사 로그를 사용 하 여 기록 된 사서함 활동에 대 한 검색 합니다. 특정 사용자 사서함에 대 한 활동을 검색할 수 있습니다. 다음 스크린샷에서 Office 365 감사 로그에서 검색할 수 있는 사서함 작업의 목록을 보여줍니다. 이러한 작업은과 같은 작업을 설명 하는이 항목의 "사서함 작업을 감사" 섹션에는 note 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p120">Use the Office 365 audit log to search for mailbox activity that have been logged. You can search for activity for a specific user mailbox. The following screenshot shows a list of mailbox activities that you can search for in the Office 365 audit log. Note that these activities are the same actions that are described in the "Mailbox auditing actions" section in this topic.</span></span>
    
    ![활동 드롭다운 목록에서 "Exchange 사서함 작업"을 선택 하 여 사서함 감사 작업에 대 한 Office 365 감사 로그를 검색할 수 있습니다.](media/fadc34f8-9de2-4688-8b1a-bc5540e69a23.png)
  
    <span data-ttu-id="1c168-252">다음 표에서 각 사서함 활동을 검색할 수 하 고 작업을 감사 하는 해당 사서함을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-252">The following table describes each mailbox activity that you can search for and shows the corresponding mailbox auditing action.</span></span>
    
    |<span data-ttu-id="1c168-253">**감사 로그에 활동**</span><span class="sxs-lookup"><span data-stu-id="1c168-253">**Activity in the audit log**</span></span>|<span data-ttu-id="1c168-254">**사서함 감사 동작**</span><span class="sxs-lookup"><span data-stu-id="1c168-254">**Mailbox auditing action**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="1c168-255">생성된 된 사서함 항목</span><span class="sxs-lookup"><span data-stu-id="1c168-255">Created mailbox item</span></span>  <br/> |<span data-ttu-id="1c168-256">만들기</span><span class="sxs-lookup"><span data-stu-id="1c168-256">Create</span></span>  <br/> |
    |<span data-ttu-id="1c168-257">다른 폴더에 복사 된 메시지</span><span class="sxs-lookup"><span data-stu-id="1c168-257">Copied messages to another folder</span></span>  <br/> |<span data-ttu-id="1c168-258">복사</span><span class="sxs-lookup"><span data-stu-id="1c168-258">Copy</span></span>  <br/> |
    |<span data-ttu-id="1c168-259">사용자 사서함에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-259">User signed in to mailbox</span></span>  <br/> |<span data-ttu-id="1c168-260">MailboxLogin</span><span class="sxs-lookup"><span data-stu-id="1c168-260">MailboxLogin</span></span>  <br/> |
    |<span data-ttu-id="1c168-261">대신 보내기 권한을 사용 하 여 메시지를 보낸 사람이</span><span class="sxs-lookup"><span data-stu-id="1c168-261">Sent message using Send On Behalf permissions</span></span>  <br/> |<span data-ttu-id="1c168-262">SendOnBehalf</span><span class="sxs-lookup"><span data-stu-id="1c168-262">SendOnBehalf</span></span>  <br/> |
    |<span data-ttu-id="1c168-263">사서함에서 제거 된 메시지</span><span class="sxs-lookup"><span data-stu-id="1c168-263">Purged messages from the mailbox</span></span>  <br/> |<span data-ttu-id="1c168-264">HardDelete</span><span class="sxs-lookup"><span data-stu-id="1c168-264">HardDelete</span></span>  <br/> |
    |<span data-ttu-id="1c168-265">지운 편지함 폴더로 메시지 이동</span><span class="sxs-lookup"><span data-stu-id="1c168-265">Moved messages to Deleted Items folder</span></span>  <br/> |<span data-ttu-id="1c168-266">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="1c168-266">MoveToDeletedItems</span></span>  <br/> |
    |<span data-ttu-id="1c168-267">다른 폴더로 메시지 이동</span><span class="sxs-lookup"><span data-stu-id="1c168-267">Moved messages to another folder</span></span>  <br/> |<span data-ttu-id="1c168-268">이동</span><span class="sxs-lookup"><span data-stu-id="1c168-268">Move</span></span>  <br/> |
    |<span data-ttu-id="1c168-269">다른 사람 이름으로 보내기 권한을 사용 하 여 메시지를 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-269">Sent message using Send As permissions</span></span>  <br/> |<span data-ttu-id="1c168-270">SendAs</span><span class="sxs-lookup"><span data-stu-id="1c168-270">SendAs</span></span>  <br/> |
    |<span data-ttu-id="1c168-271">업데이트 된 메시지</span><span class="sxs-lookup"><span data-stu-id="1c168-271">Updated message</span></span>  <br/> |<span data-ttu-id="1c168-272">업데이트</span><span class="sxs-lookup"><span data-stu-id="1c168-272">Update</span></span>  <br/> |
    |<span data-ttu-id="1c168-273">지운 편지함 폴더에서 삭제 된 메시지</span><span class="sxs-lookup"><span data-stu-id="1c168-273">Deleted messages from Deleted Items folder</span></span>  <br/> |<span data-ttu-id="1c168-274">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="1c168-274">SoftDelete</span></span>  <br/> |
    |<span data-ttu-id="1c168-275">폴더에 추가 된 사용 권한</span><span class="sxs-lookup"><span data-stu-id="1c168-275">Added permissions to folder</span></span>  <br/> |<span data-ttu-id="1c168-276">UpdateFolderPermissions</span><span class="sxs-lookup"><span data-stu-id="1c168-276">UpdateFolderPermissions</span></span>  <br/> |
    |<span data-ttu-id="1c168-277">폴더의 수정 된 사용 권한</span><span class="sxs-lookup"><span data-stu-id="1c168-277">Modified permissions of folder</span></span>  <br/> |<span data-ttu-id="1c168-278">UpdateFolderPermissions</span><span class="sxs-lookup"><span data-stu-id="1c168-278">UpdateFolderPermissions</span></span>  <br/> |
    |<span data-ttu-id="1c168-279">폴더에서 제거 된 사용 권한</span><span class="sxs-lookup"><span data-stu-id="1c168-279">Removed permissions from folder</span></span>  <br/> |<span data-ttu-id="1c168-280">UpdateFolderPermissions</span><span class="sxs-lookup"><span data-stu-id="1c168-280">UpdateFolderPermissions</span></span>  <br/> |
    |<span data-ttu-id="1c168-281">일정 폴더에 대 한 대리인 액세스와 추가 되거나 제거 된 사용자</span><span class="sxs-lookup"><span data-stu-id="1c168-281">Added or removed user with delegate access to calendar folder</span></span>  <br/> |<span data-ttu-id="1c168-282">UpdateCalendarDelegation</span><span class="sxs-lookup"><span data-stu-id="1c168-282">UpdateCalendarDelegation</span></span>  <br/> |
   
    <span data-ttu-id="1c168-p121">이전 화면에 표시 된 **추가 대리인 사서함 사용 권한** 및 **제거 됨, 사서함 권한 위임** 활동 작업을 감사 하는 사서함과 관련이 없는 note 합니다. 관리자가 할당 또는 FullAccess 사서함 권한이 제거 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p121">Note that the **Added delegate mailbox permissions** and **Removed delegate mailbox permissions** activities shown in the previous screenshot aren't related to mailbox auditing actions. They indicate whether an administrator assigned or removed the FullAccess mailbox permission.</span></span> 
    
    <span data-ttu-id="1c168-285">Office 365 감사 로그에 대 한 정보를 참조 하십시오. [Office 365 보안에서 감사 로그를 검색 &amp; 준수 센터](search-the-audit-log-in-security-and-compliance.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-285">For information about the Office 365 audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
    
- <span data-ttu-id="1c168-286">다음 시나리오에서는 관리자만 사서함에 액세스한다고 간주합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-286">Mailboxes are considered to be accessed by an administrator only in the following scenarios:</span></span>
    
  - <span data-ttu-id="1c168-287">Exchange Online 또는 Office 365에서 콘텐츠 검색에서 원본 위치 eDiscovery는 사서함을 검색 하는데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-287">In-Place eDiscovery in Exchange Online or Content Search in Office 365 is used to search a mailbox.</span></span>
    
  - <span data-ttu-id="1c168-288">[Microsoft Exchange Server MAPI 편집기](https://go.microsoft.com/fwlink/p/?linkId=204086)를 사용하여 사서함에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-288">[Microsoft Exchange Server MAPI Editor](https://go.microsoft.com/fwlink/p/?linkId=204086) is used to access the mailbox.</span></span> 
    
- <span data-ttu-id="1c168-289">사서함 감사 로깅을 사용하도록 설정할 때 로그온 유형(관리자, 대리인 또는 소유자)별로 기록할 사용자 작업(예: 메시지 액세스, 이동 또는 삭제)도 지정할 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="1c168-289">When you enable audit logging for a mailbox, you can also specify which user actions (for example, accessing, moving, or deleting a message) will be logged for each logon type (admin, delegate, or owner).</span></span>
    
- <span data-ttu-id="1c168-290">사서함 감사 로깅을 사용하도록 설정하지 않으려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-290">To disable mailbox audit logging, run the following command:</span></span>

  ```
  Set-Mailbox -Identity <identity of mailbox> -AuditEnabled $false
   ```

- <span data-ttu-id="1c168-p122">**Get-mailbox** cmdlet을 실행 하는 경우 각 유형의 사용자에 대해 감사 되는 작업을 표시 되지 않습니다. 하지만 특정 사용자 로그온 형식에 대 한 감사 된 모든 작업을 표시 하려면 다음 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c168-p122">The actions that are audited for each type of user aren't displayed when you run the **Get-Mailbox** cmdlet. But you can run the following commands to display all the audited actions for a specific user logon type.</span></span> 

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditAdmin
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditDelegate
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditOwner
    ```

- <span data-ttu-id="1c168-p123">사서함 감사 로그 내보내기 하 고 하나 이상의 사용자에 대 한 포함할 항목을 지정할 수도 있습니다. 보고서 및 감사 로그의 각 항목에는 해당 작업을 수행한 사용자에 대 한 때 수행 되는 작업 및 작업의 성공 여부를 정보가 포함 됩니다. 자세한 내용은 [사서함 감사 로그 내보내기](https://go.microsoft.com/fwlink/p/?LinkID=404104)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1c168-p123">You can also export a mailbox audit log and specify the entries to include for one or more users. Each entry in the report and the audit log includes information about who performed the action and when, the action performed , and whether the action was successful. For more information, see [Export mailbox audit logs](https://go.microsoft.com/fwlink/p/?LinkID=404104).</span></span>
