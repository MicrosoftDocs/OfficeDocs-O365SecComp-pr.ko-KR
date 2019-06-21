---
title: 사서함 감사 관리
ms.author: chrisda
author: chrisda
manager: serdars
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: 사서함 감사 로깅은 기본적으로 Microsoft 365에서 설정 됩니다 (기본 사서함 감사 또는 사서함 감사가 기본적으로 라고도 함). 즉, 사서함 소유자, 대리인 및 관리자가 수행 하는 특정 작업이 사서함 감사 로그에 자동으로 기록 되므로 사서함에 대해 수행 된 작업을 검색할 수 있습니다.
ms.openlocfilehash: f100fa1eb8244aeaea463440025ee489ec019406
ms.sourcegitcommit: ef2657e4221296be7032191f2d91e8ff727523c6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/21/2019
ms.locfileid: "35117693"
---
# <a name="manage-mailbox-auditing"></a><span data-ttu-id="90ae0-104">사서함 감사 관리</span><span class="sxs-lookup"><span data-stu-id="90ae0-104">Manage mailbox auditing</span></span>

<span data-ttu-id="90ae0-105">2019 년 1 월부터 Microsoft가 모든 Microsoft 365 조 직에 대해 기본적으로 사서함 감사 로깅을 설정 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-105">Starting in January 2019, Microsoft is turning on mailbox audit logging by default for all Microsoft 365 organizations.</span></span> <span data-ttu-id="90ae0-106">즉, 사서함 소유자, 대리인 및 관리자가 수행 하는 특정 작업이 자동으로 기록 되며, 사서함 감사 로그에서 해당 사서함을 검색할 때 이러한 레코드를 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-106">This means that certain actions performed by mailbox owners, delegates, and admins are automatically logged, and the corresponding mailbox audit records will be available when you search for them in the mailbox audit log.</span></span> <span data-ttu-id="90ae0-107">사서함 감사를 기본적으로 설정 하기 전에 조직의 모든 사용자 사서함에 대해이 기능을 수동으로 사용 하도록 설정 해야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-107">Before mailbox auditing was turned on by default, you had to manually enable it for every user mailbox in your organization.</span></span>

<span data-ttu-id="90ae0-108">아래에는 기본적으로 사서함을 감사 하는 몇 가지 이점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-108">Here are some benefits of mailbox auditing on by default:</span></span>

- <span data-ttu-id="90ae0-109">새 사서함을 만들 때 감사가 자동으로 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-109">Auditing is automatically enabled when you create a new mailbox.</span></span> <span data-ttu-id="90ae0-110">새 사용자에 대해 수동으로이 기능을 사용 하도록 설정할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-110">You don't need to manually enable it for new users.</span></span>

- <span data-ttu-id="90ae0-111">감사 되는 사서함 작업을 관리할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-111">You don't need to manage the mailbox actions that are audited.</span></span> <span data-ttu-id="90ae0-112">미리 정의 된 사서함 작업 집합은 각 로그온 유형 (관리자, 위임 및 소유자)에 대해 기본적으로 감사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-112">A predefined set of mailbox actions are audited by default for each logon type (Admin, Delegate, and Owner).</span></span>

- <span data-ttu-id="90ae0-113">Microsoft가 새 사서함 작업을 출시할 때 (특히 사용자의 조직 보호 및 법적 조사에 도움을 주는 작업) 작업이 기본적으로 감사 되는 사서함 작업 목록에 자동으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-113">When Microsoft releases a new mailbox action (particularly actions that help protect your organization and help with forensic investigations), the action is automatically added to the list of mailbox actions that are audited by default.</span></span> <span data-ttu-id="90ae0-114">즉, 사서함에 대 한 새 작업 추가를 모니터링할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-114">This means you don't need to monitor add new actions on mailboxes.</span></span>

- <span data-ttu-id="90ae0-115">모든 사서함에 대해 동일한 작업을 감사 하 고 있으므로 조직 전체에 일관 된 사서함 감사 정책이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-115">You have a consistent mailbox auditing policy across your organization (because you're auditing the same actions for all mailboxes).</span></span>

> [!TIP]
> <span data-ttu-id="90ae0-116">기본적으로 사서함 감사 릴리스를 고려해 야 할 중요 한 사항은 다음과 같습니다. 사서함 감사를 관리할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-116">The important thing to remember about the release of mailbox auditing on by default is: you don't need to do anything to manage mailbox auditing.</span></span> <span data-ttu-id="90ae0-117">그러나 자세한 내용을 보거나 기본 설정에서 사서함 감사를 사용자 지정 하거나 완전히 해제 하려면이 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="90ae0-117">However, to learn more, customize mailbox auditing from the default settings, or turn it off altogether, this topic can help you.</span></span>

## <a name="verify-mailbox-auditing-on-by-default-is-turned-on"></a><span data-ttu-id="90ae0-118">기본적으로 사서함 감사가 설정 되어 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="90ae0-118">Verify mailbox auditing on by default is turned on</span></span>

<span data-ttu-id="90ae0-119">조직에 대해 기본적으로 사서함 감사가 설정 되어 있는지 확인 하려면 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-119">To verify that mailbox auditing on by default is turned on for your organization, run the following command in [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell):</span></span>

```
Get-OrganizationConfig | Format-List AuditDisabled
```

<span data-ttu-id="90ae0-120">**False** 값은 조직에 대해 기본적으로 사서함 감사가 사용 되도록 설정 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-120">The value **False** indicates that mailbox auditing on by default is enabled for the organization.</span></span> <span data-ttu-id="90ae0-121">기본적으로 조직 값은 특정 사서함에 대 한 사서함 감사 설정을 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-121">This on by default organizational value overrides the mailbox auditing setting on specific mailboxes.</span></span> <span data-ttu-id="90ae0-122">예를 들어 사서함에 대해 사서함 감사를 사용 하지 않도록 설정 된 경우 (해당 사서함에서 *Auditenabled* 속성이 **False** 인 경우) 사서함에 대 한 mailbox 감사가 기본적으로 설정 되어 있으므로 사서함에 대해 기본 사서함 작업이 계속 감사 됩니다. 조직.</span><span class="sxs-lookup"><span data-stu-id="90ae0-122">For example, if mailbox auditing is disabled for a mailbox (the *AuditEnabled* property is **False** on the mailbox), the default mailbox actions will still be audited for the mailbox, because mailbox auditing on by default is enabled for the organization.</span></span>

<span data-ttu-id="90ae0-123">특정 사서함에 대해 사서함 감사를 사용 하지 않도록 설정 하려면 사서함 소유자 및 사서함에 대 한 액세스 권한을 위임 받은 다른 사용자에 대해 사서함 감사 바이패스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-123">To keep mailbox auditing disabled for specific mailboxes, you configure mailbox auditing bypass for the mailbox owner and other users who have been delegated access to the mailbox.</span></span> <span data-ttu-id="90ae0-124">자세한 내용은이 항목의 [사서함 감사 로깅 바이패스](#bypass-mailbox-audit-logging) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="90ae0-124">For more information, see the [Bypass mailbox audit logging](#bypass-mailbox-audit-logging) section in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="90ae0-125">조직에 대해 기본적으로 사서함 감사가 설정 되어 있으면 영향을 받는 사서함에 대 한 *Auditenabled* 속성은 **False** 에서 **True**로 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-125">When mailbox auditing on by default is turned on for the organization, the *AuditEnabled* property for affected mailboxes won't be changed from **False** to **True**.</span></span> <span data-ttu-id="90ae0-126">즉 사서함에 대 한 *Auditenabled* 속성을 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-126">In other words, mailbox auditing on by default ignores the *AuditEnabled* property on mailboxes.</span></span>

## <a name="supported-mailbox-types"></a><span data-ttu-id="90ae0-127">지원 되는 사서함 유형</span><span class="sxs-lookup"><span data-stu-id="90ae0-127">Supported mailbox types</span></span>

<span data-ttu-id="90ae0-128">다음 표에는 기본적으로 사서함 감사에서 현재 지원 되는 사서함 유형이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-128">The following table shows the mailbox types that are currently supported by mailbox auditing on by default:</span></span>

|<span data-ttu-id="90ae0-129">**사서함 유형**</span><span class="sxs-lookup"><span data-stu-id="90ae0-129">**Mailbox type**</span></span>|<span data-ttu-id="90ae0-130">**지원**</span><span class="sxs-lookup"><span data-stu-id="90ae0-130">**Supported**</span></span>|<span data-ttu-id="90ae0-131">**지원되지 않음**</span><span class="sxs-lookup"><span data-stu-id="90ae0-131">**Not supported**</span></span>|
|:---------|:---------:|:---------:|
|<span data-ttu-id="90ae0-132">사용자 사서함</span><span class="sxs-lookup"><span data-stu-id="90ae0-132">User mailboxes</span></span>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
|<span data-ttu-id="90ae0-134">공유 사서함</span><span class="sxs-lookup"><span data-stu-id="90ae0-134">Shared mailboxes</span></span>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
|<span data-ttu-id="90ae0-136">Office 365 그룹 사서함</span><span class="sxs-lookup"><span data-stu-id="90ae0-136">Office 365 Group mailboxes</span></span>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
|<span data-ttu-id="90ae0-138">리소스 사서함</span><span class="sxs-lookup"><span data-stu-id="90ae0-138">Resource mailboxes</span></span>||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="90ae0-140">공용 폴더 사서함</span><span class="sxs-lookup"><span data-stu-id="90ae0-140">Public folder mailboxes</span></span>||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|

## <a name="logon-types-and-mailbox-actions"></a><span data-ttu-id="90ae0-142">로그온 유형 및 사서함 작업</span><span class="sxs-lookup"><span data-stu-id="90ae0-142">Logon types and mailbox actions</span></span>

<span data-ttu-id="90ae0-143">로그온 유형은 사서함에 대해 감사 된 작업을 수행한 사용자를 분류 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-143">Logon types classify the user that did the audited actions on the mailbox.</span></span> <span data-ttu-id="90ae0-144">다음 목록에서는 사서함 감사 로깅에 사용 되는 로그온 유형에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-144">The following list describes the logon types that are used in mailbox audit logging:</span></span>

- <span data-ttu-id="90ae0-145">**소유자**: 사서함 소유자 (사서함과 연결 된 계정)입니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-145">**Owner**: The mailbox owner (the account that's associated with the mailbox).</span></span>

- <span data-ttu-id="90ae0-146">**대리인**:</span><span class="sxs-lookup"><span data-stu-id="90ae0-146">**Delegate**:</span></span>

  - <span data-ttu-id="90ae0-147">다른 사서함에 대 한 SendAs, SendOnBehalf FullAccess 권한이 할당 된 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-147">A user who's been assigned the SendAs, SendOnBehalf, or FullAccess permission to another mailbox.</span></span>

  - <span data-ttu-id="90ae0-148">사용자의 사서함에 대 한 FullAccess 권한이 할당 된 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-148">An admin who's been assigned the FullAccess permission to a user's mailbox.</span></span>

- <span data-ttu-id="90ae0-149">**관리자**:</span><span class="sxs-lookup"><span data-stu-id="90ae0-149">**Admin**:</span></span>

  - <span data-ttu-id="90ae0-150">다음 Microsoft eDiscovery 도구 중 하나를 사용 하 여 사서함을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-150">The mailbox is searched with one of the following Microsoft eDiscovery tools:</span></span>

    - <span data-ttu-id="90ae0-151">준수 센터의 콘텐츠 검색</span><span class="sxs-lookup"><span data-stu-id="90ae0-151">Content Search in the Compliance center.</span></span>

    - <span data-ttu-id="90ae0-152">준수 센터의 eDiscovery 또는 고급 eDiscovery</span><span class="sxs-lookup"><span data-stu-id="90ae0-152">eDiscovery or Advanced eDiscovery in the Compliance center.</span></span>

    - <span data-ttu-id="90ae0-153">Exchange Online의 원본 위치 eDiscovery</span><span class="sxs-lookup"><span data-stu-id="90ae0-153">In-Place eDiscovery in Exchange Online.</span></span>

  - <span data-ttu-id="90ae0-154">[Microsoft Exchange SERVER MAPI 편집기](https://go.microsoft.com/fwlink/p/?linkId=204086)를 사용 하 여 사서함에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-154">The mailbox is accessed by using the [Microsoft Exchange Server MAPI Editor](https://go.microsoft.com/fwlink/p/?linkId=204086).</span></span>

### <a name="mailbox-actions-for-user-mailboxes-and-shared-mailboxes"></a><span data-ttu-id="90ae0-155">사용자 사서함 및 공유 사서함에 대 한 사서함 작업</span><span class="sxs-lookup"><span data-stu-id="90ae0-155">Mailbox actions for user mailboxes and shared mailboxes</span></span>

<span data-ttu-id="90ae0-156">다음 표에서는 사용자 사서함 및 공유 사서함에 대 한 사서함 감사 로깅에서 사용할 수 있는 사서함 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-156">The following table describes the mailbox actions that are available in mailbox audit logging for user mailboxes and shared mailboxes.</span></span>

- <span data-ttu-id="90ae0-157">확인 표시 (</span><span class="sxs-lookup"><span data-stu-id="90ae0-157">A check mark (</span></span> ![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<span data-ttu-id="90ae0-159">)는 사서함 작업이 로그온 유형에 대해 기록 될 수 있음을 나타냅니다 (모든 작업을 모든 로그온 유형에 사용할 수 있는 것은 아님).</span><span class="sxs-lookup"><span data-stu-id="90ae0-159">) indicates the mailbox action can be logged for the logon type (not all actions are available for all logon types).</span></span>

- <span data-ttu-id="90ae0-160">확인 표시 후 <sup>\*</sup> 에 별표 ()는 로그온 유형에 대해 기본적으로 사서함 작업이 기록 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-160">An asterisk ( <sup>\*</sup> ) after the check mark indicates the mailbox action is logged by default for the logon type.</span></span>

- <span data-ttu-id="90ae0-161">사서함에 대 한 모든 권한이 있는 관리자는 대리인으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-161">Remember, an admin with Full Access permission to a mailbox is considered a delegate.</span></span>

|<span data-ttu-id="90ae0-162">**사서함 작업**</span><span class="sxs-lookup"><span data-stu-id="90ae0-162">**Mailbox action**</span></span>|<span data-ttu-id="90ae0-163">**설명**</span><span class="sxs-lookup"><span data-stu-id="90ae0-163">**Description**</span></span>|<span data-ttu-id="90ae0-164">**Admin**</span><span class="sxs-lookup"><span data-stu-id="90ae0-164">**Admin**</span></span>|<span data-ttu-id="90ae0-165">**대리인**</span><span class="sxs-lookup"><span data-stu-id="90ae0-165">**Delegate**</span></span>|<span data-ttu-id="90ae0-166">**소유자**</span><span class="sxs-lookup"><span data-stu-id="90ae0-166">**Owner**</span></span>|
|:---------|:---------|:---------:|:---------:|:---------:|
|<span data-ttu-id="90ae0-167">**AddFolderPermissions**</span><span class="sxs-lookup"><span data-stu-id="90ae0-167">**AddFolderPermissions**</span></span>|<span data-ttu-id="90ae0-168">**참고**:이 값은 사서함 작업으로 허용 되지만 **updatefolderpermissions** 작업에 이미 포함 되어 있으며 별도로 감사 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-168">**Note**: Although this value is accepted as a mailbox action, it's already included in the **UpdateFolderPermissions** action and isn't audited separately.</span></span> <span data-ttu-id="90ae0-169">즉,이 값을 사용 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="90ae0-169">In other words, don't use this value.</span></span>||||
|<span data-ttu-id="90ae0-170">**ApplyRecord**</span><span class="sxs-lookup"><span data-stu-id="90ae0-170">**ApplyRecord**</span></span>|<span data-ttu-id="90ae0-171">항목은 레코드로 레이블이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-171">An item is labeled as a record.</span></span>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="90ae0-175">**복사**</span><span class="sxs-lookup"><span data-stu-id="90ae0-175">**Copy**</span></span>|<span data-ttu-id="90ae0-176">메시지가 다른 폴더에 복사되었습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-176">A message was copied to another folder.</span></span>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|||
|<span data-ttu-id="90ae0-178">**만들기**</span><span class="sxs-lookup"><span data-stu-id="90ae0-178">**Create**</span></span>|<span data-ttu-id="90ae0-179">사서함의 일정, 연락처, 메모 또는 작업 폴더 (예: 새 모임 요청이 만들어짐)에 항목이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-179">An item was created in the Calendar, Contacts, Notes, or Tasks folder in the mailbox (for example, a new meeting request is created).</span></span> <span data-ttu-id="90ae0-180">메시지 만들기, 보내기 또는 받기는 감사 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-180">Note that creating, sending, or receiving a message isn't audited.</span></span> <span data-ttu-id="90ae0-181">또한 사서함 폴더를 만드는 것은 감사 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-181">Also, creating a mailbox folder is not audited.</span></span>|<span data-ttu-id="90ae0-182">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-182">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-183">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-183">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="90ae0-185">**FolderBind**</span><span class="sxs-lookup"><span data-stu-id="90ae0-185">**FolderBind**</span></span>|<span data-ttu-id="90ae0-p113">사서함 폴더에 액세스했습니다. 관리자 또는 대리인이 사서함을 열 때에도 작업이 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-p113">A mailbox folder was accessed. This action is also logged when the admin or delegate opens the mailbox. </span></span><br/><br/> <span data-ttu-id="90ae0-188">**참고**: 대리인에 의해 수행 된 폴더 바인드 작업에 대 한 감사 기록이 통합 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-188">**Note**: Audit records for folder bind actions performed by delegates are consolidated.</span></span> <span data-ttu-id="90ae0-189">24 시간 내에 개별 폴더 액세스에 대 한 감사 레코드 하나를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-189">One audit record is generated for individual folder access within 24 hour period.</span></span>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
|<span data-ttu-id="90ae0-192">**HardDelete**</span><span class="sxs-lookup"><span data-stu-id="90ae0-192">**HardDelete**</span></span>|<span data-ttu-id="90ae0-193">메시지가 복구 가능한 항목 폴더에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-193">A message was purged from the Recoverable Items folder.</span></span>|<span data-ttu-id="90ae0-194">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-194">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-195">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-195">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-196">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-196">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|
|<span data-ttu-id="90ae0-197">**MailboxLogin**</span><span class="sxs-lookup"><span data-stu-id="90ae0-197">**MailboxLogin**</span></span>|<span data-ttu-id="90ae0-198">사용자가 사서함에 로그인 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-198">The user signed into their mailbox.</span></span> |||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="90ae0-200">**대해 수행한 messagebind**</span><span class="sxs-lookup"><span data-stu-id="90ae0-200">**MessageBind**</span></span>|<span data-ttu-id="90ae0-201">메시지가 미리 보기 창에 표시되거나 열렸습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-201">A message was viewed in the preview pane or opened.</span></span>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|||
|<span data-ttu-id="90ae0-203">**ModifyFolderPermissions**</span><span class="sxs-lookup"><span data-stu-id="90ae0-203">**ModifyFolderPermissions**</span></span>|<span data-ttu-id="90ae0-204">**참고**:이 값은 사서함 작업으로 허용 되지만 **updatefolderpermissions** 작업에 이미 포함 되어 있으며 별도로 감사 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-204">**Note**: Although this value is accepted as a mailbox action, it's already included in the **UpdateFolderPermissions** action and isn't audited separately.</span></span> <span data-ttu-id="90ae0-205">즉,이 값을 사용 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="90ae0-205">In other words, don't use this value.</span></span>||||
|<span data-ttu-id="90ae0-206">**Move**</span><span class="sxs-lookup"><span data-stu-id="90ae0-206">**Move**</span></span>|<span data-ttu-id="90ae0-207">메시지가 다른 폴더로 이동했습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-207">A message was moved to another folder.</span></span>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="90ae0-211">**MoveToDeletedItems**</span><span class="sxs-lookup"><span data-stu-id="90ae0-211">**MoveToDeletedItems**</span></span>|<span data-ttu-id="90ae0-212">메시지가 삭제되어 지운 편지함 폴더로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-212">A message was deleted and moved to the Deleted Items folder.</span></span>|<span data-ttu-id="90ae0-213">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-213">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-214">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-214">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-215">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-215">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|
|<span data-ttu-id="90ae0-216">**RecordDelete**</span><span class="sxs-lookup"><span data-stu-id="90ae0-216">**RecordDelete**</span></span>|<span data-ttu-id="90ae0-217">레코드로 레이블이 지정 된 항목은 일시 삭제 (복구 가능한 항목 폴더로 이동) 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-217">An item that's labeled as a record was soft-deleted (moved to the Recoverable Items folder).</span></span> <span data-ttu-id="90ae0-218">레코드로 레이블이 지정 된 항목은 영구적으로 삭제할 수 없습니다 (복구 가능한 항목 폴더에서 제거).</span><span class="sxs-lookup"><span data-stu-id="90ae0-218">Items labeled as records can't be permanently deleted (purged from the Recoverable Items folder).</span></span>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|<span data-ttu-id="90ae0-222">**RemoveFolderPermissions**</span><span class="sxs-lookup"><span data-stu-id="90ae0-222">**RemoveFolderPermissions**</span></span>|<span data-ttu-id="90ae0-223">**참고**:이 값은 사서함 작업으로 허용 되지만 **updatefolderpermissions** 작업에 이미 포함 되어 있으며 별도로 감사 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-223">**Note**: Although this value is accepted as a mailbox action, it's already included in the **UpdateFolderPermissions** action and isn't audited separately.</span></span> <span data-ttu-id="90ae0-224">즉,이 값을 사용 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="90ae0-224">In other words, don't use this value.</span></span>||||
|<span data-ttu-id="90ae0-225">**SendAs**</span><span class="sxs-lookup"><span data-stu-id="90ae0-225">**SendAs**</span></span>|<span data-ttu-id="90ae0-p118">메시지가 SendAs 권한을 사용하여 전송되었습니다. 즉 사서함 소유자가 보낸 것처럼 보이도록 하여 다른 사용자가 메시지를 보냈습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-p118">A message was sent using the SendAs permission. This means another user sent the message as though it came from the mailbox owner.</span></span>|<span data-ttu-id="90ae0-228">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-228">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-229">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-229">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>||
|<span data-ttu-id="90ae0-230">**SendOnBehalf**</span><span class="sxs-lookup"><span data-stu-id="90ae0-230">**SendOnBehalf**</span></span>|<span data-ttu-id="90ae0-p119">메시지가 SendOnBehalf 권한을 사용하여 전송되었습니다. 즉 다른 사용자가 사서함 소유자 대신에 메시지를 보냈습니다. 받는 사람은 메시지를 대신 보낸 사용자와 해당 메시지를 실제로 보낸 사용자를 메시지에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-p119">A message was sent using the SendOnBehalf permission. This means another user sent the message on behalf of the mailbox owner. The message indicates to the recipient who the message was sent on behalf of and who actually sent the message.</span></span>|<span data-ttu-id="90ae0-234">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-234">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-235">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-235">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>||
|<span data-ttu-id="90ae0-236">**SoftDelete**</span><span class="sxs-lookup"><span data-stu-id="90ae0-236">**SoftDelete**</span></span>|<span data-ttu-id="90ae0-p120">메시지가 지운 편지함 폴더에서 삭제되어가 영구적으로 삭제되었습니다. 소프트 삭제된 항목이 복구 가능한 항목 폴더로 이동됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-p120">A message was permanently deleted or deleted from the Deleted Items folder. Soft-deleted items are moved to the Recoverable Items folder.</span></span>|<span data-ttu-id="90ae0-239">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-239">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-240">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-240">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-241">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-241">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|
|<span data-ttu-id="90ae0-242">**업데이트**</span><span class="sxs-lookup"><span data-stu-id="90ae0-242">**Update**</span></span>|<span data-ttu-id="90ae0-243">메시지 또는 해당 속성이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-243">A message or its properties was changed.</span></span>|<span data-ttu-id="90ae0-244">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-244">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-245">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-245">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-246">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-246">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|
|<span data-ttu-id="90ae0-247">**UpdateCalendarDelegation**</span><span class="sxs-lookup"><span data-stu-id="90ae0-247">**UpdateCalendarDelegation**</span></span>|<span data-ttu-id="90ae0-248">일정 위임이 사서함에 할당 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-248">A calendar delegation was assigned to a mailbox.</span></span> <span data-ttu-id="90ae0-249">일정 위임 같은 조직에서 사서함 소유자의 일정을 관리 하는 다른 사람에 게 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-249">Calendar delegation gives someone else in the same organization permissions to manage the mailbox owner's calendar.</span></span>|<span data-ttu-id="90ae0-250">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-250">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>||<span data-ttu-id="90ae0-251">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-251">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|
|<span data-ttu-id="90ae0-252">**Updatefolderpermissions 작업이 로깅됩니다**</span><span class="sxs-lookup"><span data-stu-id="90ae0-252">**UpdateFolderPermissions**</span></span>|<span data-ttu-id="90ae0-253">폴더 사용 권한이 변경 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-253">A folder permission was changed.</span></span> <span data-ttu-id="90ae0-254">폴더 사용 권한은 조직에서 사서함의 폴더에 액세스할 수 있는 사용자와 해당 폴더에 있는 메시지를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-254">Folder permissions control which users in your organization can access folders in a mailbox and the messages located in those folders.</span></span>|<span data-ttu-id="90ae0-255">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-255">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-256">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-256">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-257">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-257">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|
|<span data-ttu-id="90ae0-258">**UpdateInboxRules**</span><span class="sxs-lookup"><span data-stu-id="90ae0-258">**UpdateInboxRules**</span></span>|<span data-ttu-id="90ae0-259">받은 편지함 규칙을 추가, 제거 또는 변경 했습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-259">An inbox rule was added, removed, or changed.</span></span> <span data-ttu-id="90ae0-260">받은 편지함 규칙은 지정 된 조건에 따라 사용자의 받은 편지함에서 메시지를 처리 하 고, 메시지를 지정 된 폴더로 이동 하거나 메시지를 삭제 하는 것과 같이 규칙의 조건이 충족 될 때 작업을 수행 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-260">Inbox rules are used to process messages in the user's Inbox based on the specified conditions and take actions when the conditions of a rule are met, such as moving a message to a specified folder or deleting a message.</span></span>|<span data-ttu-id="90ae0-261">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-261">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-262">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-262">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-263">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-263">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|

> [!IMPORTANT]
> <span data-ttu-id="90ae0-264">조직에서 기본적으로 사서함 감사를 사용 하도록 설정 *하기 전에* 모든 로그온 유형에 대해 감사를 위해 사서함 작업을 사용자 지정 하는 경우 사용자 지정 설정이 사서함에 보존 되며 기본 사서함 작업에 의해 덮어쓰기 되지 않습니다. 이 섹션에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-264">If you customized the mailbox actions to audit for any logon type *before* mailbox auditing on by default was enabled in your organization, the customized settings are preserved on the mailbox and aren't overwritten by the default mailbox actions as described in this section.</span></span> <span data-ttu-id="90ae0-265">감사 사서함 작업을 기본값으로 되돌리려면 (언제 든 지이 작업을 수행할 수 있음)이 항목의 뒷부분에 나오는 [기본 사서함 작업 복원](#restore-the-default-mailbox-actions) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="90ae0-265">To revert the audit mailbox actions to their default values (which you can do at any time), see the [Restore the default mailbox actions](#restore-the-default-mailbox-actions) section later in this topic.</span></span>

### <a name="mailbox-actions-for-office-365-group-mailboxes"></a><span data-ttu-id="90ae0-266">Office 365 그룹 사서함에 대 한 사서함 작업</span><span class="sxs-lookup"><span data-stu-id="90ae0-266">Mailbox actions for Office 365 Group mailboxes</span></span>

<span data-ttu-id="90ae0-267">기본적으로 사서함 감사는 Office 365 그룹 사서함에 대 한 사서함 감사 로깅을 제공 하지만 로깅할 항목을 사용자 지정할 수 없습니다 (로그온 유형에 대해 기록 되는 사서함 작업을 추가 하거나 제거할 수 없음).</span><span class="sxs-lookup"><span data-stu-id="90ae0-267">Mailbox auditing on by default brings mailbox audit logging to Office 365 Group mailboxes, but you can't customize what's being logged (you can't add or remove mailbox actions that are logged for any logon type).</span></span>

<span data-ttu-id="90ae0-268">다음 표에서는 각 로그온 유형에 대해 Office 365 그룹 사서함에 기본적으로 기록 되는 사서함 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-268">The following table describes the mailbox actions that are logged by default on Office 365 Group mailboxes for each logon type.</span></span>

<span data-ttu-id="90ae0-269">Office 365 그룹 사서함에 대 한 모든 권한이 있는 관리자는 대리인으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-269">Remember, an admin with Full Access permission to an Office 365 Group mailbox is considered a delegate.</span></span>

|<span data-ttu-id="90ae0-270">**사서함 작업**</span><span class="sxs-lookup"><span data-stu-id="90ae0-270">**Mailbox action**</span></span>|<span data-ttu-id="90ae0-271">**설명**</span><span class="sxs-lookup"><span data-stu-id="90ae0-271">**Description**</span></span>|<span data-ttu-id="90ae0-272">**Admin**</span><span class="sxs-lookup"><span data-stu-id="90ae0-272">**Admin**</span></span>|<span data-ttu-id="90ae0-273">**대리인**</span><span class="sxs-lookup"><span data-stu-id="90ae0-273">**Delegate**</span></span>|<span data-ttu-id="90ae0-274">**소유자**</span><span class="sxs-lookup"><span data-stu-id="90ae0-274">**Owner**</span></span>|
|:---------|:---------|:---------:|:---------:|:---------:|
|<span data-ttu-id="90ae0-275">**만들기**</span><span class="sxs-lookup"><span data-stu-id="90ae0-275">**Create**</span></span>|<span data-ttu-id="90ae0-276">일정 항목 만들기</span><span class="sxs-lookup"><span data-stu-id="90ae0-276">Creation of a calendar Item.</span></span> <span data-ttu-id="90ae0-277">메시지 만들기, 보내기 또는 받기는 감사 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-277">Note that creating, sending, or receiving a message isn't audited.</span></span>|<span data-ttu-id="90ae0-278">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-278">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-279">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-279">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>||
|<span data-ttu-id="90ae0-280">**HardDelete**</span><span class="sxs-lookup"><span data-stu-id="90ae0-280">**HardDelete**</span></span>|<span data-ttu-id="90ae0-281">메시지가 복구 가능한 항목 폴더에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-281">A message was purged from the Recoverable Items folder.</span></span>|<span data-ttu-id="90ae0-282">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-282">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-283">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-283">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-284">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-284">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|
|<span data-ttu-id="90ae0-285">**MoveToDeletedItems**</span><span class="sxs-lookup"><span data-stu-id="90ae0-285">**MoveToDeletedItems**</span></span>|<span data-ttu-id="90ae0-286">메시지가 삭제되어 지운 편지함 폴더로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-286">A message was deleted and moved to the Deleted Items folder.</span></span>|<span data-ttu-id="90ae0-287">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-287">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-288">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-288">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-289">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-289">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|
|<span data-ttu-id="90ae0-290">**SendAs**</span><span class="sxs-lookup"><span data-stu-id="90ae0-290">**SendAs**</span></span>|<span data-ttu-id="90ae0-291">메시지가 SendAs 권한을 사용하여 전송되었습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-291">A message was sent using the SendAs permission.</span></span>|<span data-ttu-id="90ae0-292">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-292">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-293">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-293">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>||
|<span data-ttu-id="90ae0-294">**SendOnBehalf**</span><span class="sxs-lookup"><span data-stu-id="90ae0-294">**SendOnBehalf**</span></span>|<span data-ttu-id="90ae0-295">메시지가 SendOnBehalf 권한을 사용하여 전송되었습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-295">A message was sent using the SendOnBehalf permission.</span></span> |<span data-ttu-id="90ae0-296">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-296">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-297">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-297">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>||
|<span data-ttu-id="90ae0-298">**SoftDelete**</span><span class="sxs-lookup"><span data-stu-id="90ae0-298">**SoftDelete**</span></span>|<span data-ttu-id="90ae0-p126">메시지가 지운 편지함 폴더에서 삭제되어가 영구적으로 삭제되었습니다. 소프트 삭제된 항목이 복구 가능한 항목 폴더로 이동됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-p126">A message was permanently deleted or deleted from the Deleted Items folder. Soft-deleted items are moved to the Recoverable Items folder.</span></span>|<span data-ttu-id="90ae0-301">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-301">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-302">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-302">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-303">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-303">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|
|<span data-ttu-id="90ae0-304">**업데이트**</span><span class="sxs-lookup"><span data-stu-id="90ae0-304">**Update**</span></span>|<span data-ttu-id="90ae0-305">메시지 또는 해당 속성이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-305">A message or its properties was changed.</span></span>|<span data-ttu-id="90ae0-306">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-306">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-307">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-307">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|<span data-ttu-id="90ae0-308">![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="90ae0-308">![Check mark](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup></span></span>|

### <a name="verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type"></a><span data-ttu-id="90ae0-309">각 로그온 유형에 대해 기본 사서함 작업이 기록 되는지 확인</span><span class="sxs-lookup"><span data-stu-id="90ae0-309">Verify that default mailbox actions are being logged for each logon type</span></span>

<span data-ttu-id="90ae0-310">기본적으로 사서함 감사는 모든 사서함에 새 *Defaultauditset* 속성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-310">Mailbox auditing on by defaults adds a new *DefaultAuditSet* property to all mailboxes.</span></span> <span data-ttu-id="90ae0-311">이 속성의 값은 사서함에서 기본 사서함 작업 (Microsoft에서 관리)이 감사 되 고 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-311">The value of this property indicates whether the default mailbox actions (managed by Microsoft) are being audited on the mailbox.</span></span>

<span data-ttu-id="90ae0-312">사용자 사서함 또는 공유 사서함에 값을 표시 하려면 MailboxIdentity \<\> 를 이름, 별칭, 전자 메일 주소 또는 사서함의 upn (사용자 계정 이름)으로 바꾸고 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-312">To display the value on user mailboxes or shared mailboxes, replace \<MailboxIdentity\> with the name, alias, email address, or user principal name (username) of the mailbox and run the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox -Identity <MailboxIdentity> | Format-List DefaultAuditSet
```

<span data-ttu-id="90ae0-313">Office 365 그룹 사서함에 값을 표시 하려면 MailboxIdentity \<\> 을 공유 사서함의 이름, 별칭 또는 전자 메일 주소로 바꾸고 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-313">To display the value on Office 365 group mailboxes, replace \<MailboxIdentity\> with the name, alias, or email address of the shared mailbox and run the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox -Identity <MailboxIdentity> -GroupMailbox | Format-List DefaultAuditSet
```

<span data-ttu-id="90ae0-314">값 `Admin, Delegate, Owner` 은 다음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-314">The value `Admin, Delegate, Owner` indicates:</span></span>

- <span data-ttu-id="90ae0-315">세 가지 로그온 유형에 대 한 기본 사서함 작업을 모두 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-315">The default mailbox actions for all three logon types are being audited.</span></span> <span data-ttu-id="90ae0-316">이 값은 Office 365 그룹 사서함에만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-316">Note that this is the only value you'll see on Office 365 Group mailboxes.</span></span>

- <span data-ttu-id="90ae0-317">관리자가 사용자 사서함 또는 공유 사서함의 로그온 유형에 대해 감사 된 사서함 작업을 변경 *하지* 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-317">An admin *has not* changed the audited mailbox actions for any logon type on a user mailbox or a shared mailbox.</span></span> <span data-ttu-id="90ae0-318">참고 기본적으로 사서함 감사를 시작한 후의 기본 상태는 조직에서 처음으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-318">Note this is the default state after mailbox auditing on by default is initially turned on in your organization.</span></span>

<span data-ttu-id="90ae0-319">관리자가 로그온 유형에 대해 감사 되는 사서함 작업 ( *Auditadmin*, *Auditadmin*또는 **Set mailbox** cmdlet의 *auditadmin* 매개 변수를 사용 하 여)을 변경한 적이 없는 경우이 속성 값은 서로 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-319">If an admin has ever changed the mailbox actions that are audited for a logon type (by using the *AuditAdmin*, *AuditDelegate*, or *AuditOwner* parameters on the **Set-Mailbox** cmdlet), the property value will be different.</span></span>

<span data-ttu-id="90ae0-320">예를 들어 사용자 사서함 `Owner` 또는 공유 사서함의 *defaultauditset* 속성에 대 한 값은 다음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-320">For example, the value `Owner` for the *DefaultAuditSet* property on a user mailbox or shared mailbox indicates:</span></span>

- <span data-ttu-id="90ae0-321">사서함 소유자에 대 한 기본 사서함 작업을 감사 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-321">The default mailbox actions for the mailbox owner are being audited.</span></span>

- <span data-ttu-id="90ae0-322">`Delegate` 및 `Admin` 로그온 유형에 대 한 감사 된 사서함 작업이 기본 작업에서 변경 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-322">The audited mailbox actions for the `Delegate` and `Admin` logon types have been changed from the default actions.</span></span>

<span data-ttu-id="90ae0-323">*Defaultauditset* 속성의 값이 비어 있으면 사용자 사서함 이나 공유 사서함에서 세 가지 로그온 유형에 대 한 사서함 작업이 모두 변경 되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-323">A blank value for the *DefaultAuditSet* property indicates the mailbox actions for all three logon types have been changed on the user mailbox or a shared mailbox.</span></span>

<span data-ttu-id="90ae0-324">자세한 내용은이 항목의 " [사서함 작업을 기본값으로 기록](#change-or-restore-mailbox-actions-logged-by-default) " 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="90ae0-324">For more information, see the [Change or restore mailbox actions logged by default](#change-or-restore-mailbox-actions-logged-by-default) section in this topic</span></span>

### <a name="display-the-mailbox-actions-that-are-being-logged-on-mailboxes"></a><span data-ttu-id="90ae0-325">기록 중인 사서함 작업을 사서함에 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-325">Display the mailbox actions that are being logged on mailboxes</span></span>

<span data-ttu-id="90ae0-326">현재 사용자 사서함 또는 공유 사서함에 대해 로그온 중인 사서함 작업을 확인 하려면 MailboxIdentity \<\> 를 이름, 별칭, 전자 메일 주소 또는 사서함의 사용자 이름 (username)으로 바꾸고 다음 중 하나 이상을 실행 합니다. Exchange Online PowerShell의 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-326">To see the mailbox actions that are currently being logged on user mailboxes or shared mailboxes, replace \<MailboxIdentity\> with the name, alias, email address, or user principal name (username) of the mailbox, and run one or more of the following commands in Exchange Online PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="90ae0-327">Office 365 그룹 사서함의 `-GroupMailbox` 다음 **사서함** 명령에 스위치를 추가할 수는 있지만 표시 되는 값은 생각 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="90ae0-327">Although you can add the `-GroupMailbox` switch to the following **Get-Mailbox** commands for Office 365 Group mailboxes, don't believe the values you see.</span></span> <span data-ttu-id="90ae0-328">Office 365 그룹 사서함에 대해 감사 되는 기본 및 정적 사서함 작업은이 항목 앞부분의 [office 365 그룹 사서함에 대 한 사서함 작업](#mailbox-actions-for-office-365-group-mailboxes) 섹션에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-328">The default and static mailbox actions that are audited for Office 365 Group mailboxes are described in the [Mailbox actions for Office 365 Group mailboxes](#mailbox-actions-for-office-365-group-mailboxes) section earlier in this topic.</span></span>

#### <a name="owner-actions"></a><span data-ttu-id="90ae0-329">소유자 작업</span><span class="sxs-lookup"><span data-stu-id="90ae0-329">Owner actions</span></span>

```
Get-Mailbox -Identity <MailboxIdentity> | Select-Object -ExpandProperty AuditOwner
```

#### <a name="delegate-actions"></a><span data-ttu-id="90ae0-330">대리인 작업</span><span class="sxs-lookup"><span data-stu-id="90ae0-330">Delegate actions</span></span>

```
Get-Mailbox -Identity <MailboxIdentity> | Select-Object -ExpandProperty AuditDelegate
```

#### <a name="admin-actions"></a><span data-ttu-id="90ae0-331">관리 작업</span><span class="sxs-lookup"><span data-stu-id="90ae0-331">Admin actions</span></span>

```
Get-Mailbox -Identity <MailboxIdentity> | Select-Object -ExpandProperty AuditAdmin
```

## <a name="change-or-restore-mailbox-actions-logged-by-default"></a><span data-ttu-id="90ae0-332">기본적으로 기록 되는 사서함 작업 변경 또는 복원</span><span class="sxs-lookup"><span data-stu-id="90ae0-332">Change or restore mailbox actions logged by default</span></span>

<span data-ttu-id="90ae0-333">앞에서 설명한 것 처럼 사서함 감사를 기본적으로 수행 하는 주요 이점은 다음과 같습니다. 감사 되는 사서함 작업을 관리할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-333">As previously explained, one of the key benefits of having mailbox auditing on by default is: you don't need to manage the mailboxes actions that are audited.</span></span> <span data-ttu-id="90ae0-334">Microsoft는이 작업을 자동으로 수행 하므로 기본적으로 새로운 사서함 작업이 릴리스될 때 감사 되도록 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-334">Microsoft does this for you and we'll automatically add new mailbox actions to be audited by default as they're released.</span></span>

<span data-ttu-id="90ae0-335">그러나 조직에서 사용자 사서함 및 공유 사서함에 대 한 다른 사서함 작업 집합을 감사 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-335">However, your organization might be required to audit a different set of mailbox actions for user mailboxes and shared mailboxes.</span></span> <span data-ttu-id="90ae0-336">이 섹션의 절차에서는 각 로그온 유형에 대해 감사 되는 사서함 작업을 변경 하는 방법과 Microsoft가 관리 하는 기본 작업으로 되돌리는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-336">The procedures in this section show you how to change the mailbox actions that are audited for each logon type, and how to revert back to the Microsoft-managed default actions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90ae0-337">다음 절차를 사용 하 여 사용자 사서함 또는 공유 사서함에 기록 된 사서함 작업을 사용자 지정 하는 경우 Microsoft에서 릴리스한 모든 새 기본 사서함 작업은 해당 사서함에서 자동으로 감사 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-337">If you use the following procedures to customize the mailbox actions that are logged on user mailboxes or shared mailboxes, any new default mailbox actions released by Microsoft will not be automatically audited on those mailboxes.</span></span> <span data-ttu-id="90ae0-338">사용자 지정한 작업 목록에 새 사서함 작업을 수동으로 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-338">You'll need to manually add any new mailbox actions to your customized list of actions.</span></span>

### <a name="change-the-mailbox-actions-to-audit"></a><span data-ttu-id="90ae0-339">감사로 사서함 작업 변경</span><span class="sxs-lookup"><span data-stu-id="90ae0-339">Change the mailbox actions to audit</span></span>

<span data-ttu-id="90ae0-340">**사서함** Cmdlet에서 *auditadmin*, *auditadmin*또는 *auditadmin* 매개 변수를 사용 하 여 사용자 사서함 및 공유 사서함에 대해 감사 되는 사서함 작업을 변경할 수 있습니다 (Office 365 그룹에 대 한 감사 된 작업). 사서함은 사용자 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-340">You can use the *AuditAdmin*, *AuditDelegate*, or *AuditOwner* parameters on the **Set-Mailbox** cmdlet to change the mailbox actions that are audited for user mailboxes and shared mailboxes (audited actions for Office 365 group mailboxes can't be customized).</span></span>

<span data-ttu-id="90ae0-341">다음과 같은 두 가지 방법을 사용 하 여 사서함 작업을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-341">You can use two different methods to specify the mailbox actions:</span></span>

- <span data-ttu-id="90ae0-342">*교체* (덮어쓰기)이 구문을 `action1,action2,...actionN`사용 하 여 기존 사서함 작업을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-342">*Replace* (overwrite) the existing mailbox actions by using this syntax: `action1,action2,...actionN`.</span></span>

- <span data-ttu-id="90ae0-343">다음 `@{Add="action1","action2",..."actionN"}` 구문을 사용 하 여 기존 값에 영향을 주지 않고 사서함 작업을 `@{Remove="action1","action2",..."actionN"}` *추가 하거나 제거* 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-343">*Add or remove* mailbox actions without affecting other existing values by using this syntax: `@{Add="action1","action2",..."actionN"}` or `@{Remove="action1","action2",..."actionN"}`.</span></span>

<span data-ttu-id="90ae0-344">이 예에서는 Gabriela Laureano "사서함에 대 한 관리자 사서함 작업을 소프트 삭제 및 하드 삭제의 기본 동작을 덮어쓰는 방법으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-344">This example changes the admin mailbox actions for the mailbox named "Gabriela Laureano" by overwriting the default actions with SoftDelete and HardDelete.</span></span>

```
Set-Mailbox -Identity "Gabriela Laureano" -AuditAdmin HardDelete,SoftDelete
```

<span data-ttu-id="90ae0-345">이 예에서는 사서함 laura@contoso.onmicrosoft.com에 MailboxLogin owner 작업을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-345">This example adds the MailboxLogin owner action to the mailbox laura@contoso.onmicrosoft.com.</span></span>

```
Set-Mailbox -Identity laura@contoso.onmicrosoft.com -AuditOwner @{Add="MailboxLogin"}
```

<span data-ttu-id="90ae0-346">이 예에서는 팀 토론 사서함에 대 한 MoveToDeletedItems 대리인 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-346">This example removes the MoveToDeletedItems delegate action for the Team Discussion mailbox.</span></span>

```
Set-Mailbox -Identity "Team Discussion" -AuditDelegate @{Remove="MoveToDeletedItems"}
```

<span data-ttu-id="90ae0-347">사용 하는 방법에 관계 없이 사용자 사서함 또는 공유 사서함에 대해 감사 된 사서함 작업을 사용자 지정 하면 다음과 같은 결과가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-347">Regardless of the method you use, customizing the audited mailbox actions on user mailboxes or shared mailboxes has the following results:</span></span>

- <span data-ttu-id="90ae0-348">사용자 지정한 로그온 유형의 경우 감사 된 사서함 작업은 더 이상 Microsoft에서 관리 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-348">For the logon type that you customized, the audited mailbox actions are no longer managed by Microsoft.</span></span>

- <span data-ttu-id="90ae0-349">사용자 지정한 로그온 유형이 [앞에서 설명한](#verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type)대로 사서함의 *defaultauditset* 속성 값에 더 이상 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-349">The logon type that you customized is no longer displayed in the *DefaultAuditSet* property value for the mailbox as [previously described](#verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type).</span></span>

### <a name="restore-the-default-mailbox-actions"></a><span data-ttu-id="90ae0-350">기본 사서함 작업 복원</span><span class="sxs-lookup"><span data-stu-id="90ae0-350">Restore the default mailbox actions</span></span>

<span data-ttu-id="90ae0-351">사용자 사서함 또는 공유 사서함에 대해 감사 되는 사서함 작업을 사용자 지정한 경우 다음 구문을 사용 하 여 하나 또는 모든 로그온 유형의 기본 사서함 작업을 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-351">If you customized the mailbox actions that are audited on a user mailbox or a shared mailbox, you can restore the default mailbox actions for one or all logon types by using this syntax:</span></span>

```
Set-Mailbox -Identity <MailboxIdentity> -DefaultAuditSet <Admin | Delegate | Owner>
```

<span data-ttu-id="90ae0-352">여러 *Defaultauditset* 값을 쉼표로 구분 하 여 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-352">You can specify multiple *DefaultAuditSet* values separated by commas</span></span>

<span data-ttu-id="90ae0-353">**참고**: 다음 절차는 Office 365 그룹 사서함에는 적용 되지 않으며 [여기](#mailbox-actions-for-office-365-group-mailboxes)에 설명 된 기본 작업으로 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-353">**Note**: The following procedures don't apply to Office 365 Group mailboxes (they're limited to the default actions as described [here](#mailbox-actions-for-office-365-group-mailboxes)).</span></span>

<span data-ttu-id="90ae0-354">이 예에서는 사서함 mark@contoso.onmicrosoft.com의 모든 로그온 유형에 대해 감사 된 기본 사서함 작업을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-354">This example restores the default audited mailbox actions for all logon types on the mailbox mark@contoso.onmicrosoft.com.</span></span>

```
Set-Mailbox -Identity mark@contoso.onmicrosoft.com -DefaultAuditSet Admin,Delegate,Owner
```

<span data-ttu-id="90ae0-355">이 예에서는 사서함 chris@contoso.onmicrosoft.com의 관리 로그온 유형에 대해 감사 된 기본 사서함 작업을 복원 하지만 대리인 및 소유자 로그온 유형에 대해 사용자 지정 된 감사 사서함 작업은 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-355">This example restores the default audited mailbox actions for the Admin logon type on the mailbox chris@contoso.onmicrosoft.com, but leaves the customized audited mailbox actions for the Delegate and Owner logon types.</span></span>

```
Set-Mailbox -Identity chris@contoso.onmicrosoft.com -DefaultAuditSet Admin
```

<span data-ttu-id="90ae0-356">로그온 유형에 대해 기본적으로 감사 된 사서함 작업을 복원 하면 다음과 같은 결과가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-356">Restoring he default audited mailbox actions for a logon type has the following results:</span></span>

- <span data-ttu-id="90ae0-357">현재 사서함 작업 목록은 로그온 유형의 기본 사서함 작업으로 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-357">The current list of mailbox actions is replaced with the default mailbox actions for the logon type.</span></span>

- <span data-ttu-id="90ae0-358">Microsoft에서 릴리스한 모든 새 사서함 작업은 로그온 유형에 대 한 감사 된 작업 목록에 자동으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-358">Any new mailbox actions that are released by Microsoft are automatically added to the list of audited actions for the logon type.</span></span>

- <span data-ttu-id="90ae0-359">사서함에 대 한 *Defaultauditset* 속성 값이 복원 된 로그온 유형을 포함 하도록 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-359">The *DefaultAuditSet* property value for the mailbox is updated to include the restored logon type.</span></span>

## <a name="turn-off-mailbox-auditing-on-by-default-for-your-organization"></a><span data-ttu-id="90ae0-360">조직에 대해 기본적으로 사서함 감사 해제</span><span class="sxs-lookup"><span data-stu-id="90ae0-360">Turn off mailbox auditing on by default for your organization</span></span>

<span data-ttu-id="90ae0-361">Exchange Online PowerShell에서 다음 명령을 실행 하 여 전체 조직에 대해 기본적으로 사서함 감사를 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-361">You can turn off mailbox auditing on by default for your entire organization by running the following command in Exchange Online PowerShell:</span></span>

```
Set-OrganizationConfig -AuditDisabled $true
```

<span data-ttu-id="90ae0-362">기본적으로 사서함 감사를 해제 하면 다음과 같은 결과가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-362">Turning off mailbox auditing on by default has the following results:</span></span>

- <span data-ttu-id="90ae0-363">조직에서 사서함 감사를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-363">Mailbox auditing is disabled for your organization.</span></span>

- <span data-ttu-id="90ae0-364">기본적으로 사서함 감사를 사용 하지 않도록 설정한 시간부터 사서함에서 감사가 사용 되도록 설정 된 경우에도 사서함 작업이 감사 되지 않습니다 (사서함의 *Auditenabled* 속성이 **True**).</span><span class="sxs-lookup"><span data-stu-id="90ae0-364">From the time you disabled mailbox auditing on by default, no mailbox actions are audited, even if auditing is enabled on a mailbox (the *AuditEnabled* property on the mailbox is **True**).</span></span>

- <span data-ttu-id="90ae0-365">사서함 감사는 새 사서함에 대해 사용 하도록 설정 되지 않으며 새 사서함 이나 기존 우편함에서 *Auditenabled* 속성을 **True** 로 설정 하면 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-365">Mailbox auditing is not enabled for new mailboxes and setting the *AuditEnabled* property on a new or existing mailbox to **True** will be ignored.</span></span>

- <span data-ttu-id="90ae0-366">**Get-mailboxauditbypassassociation** cmdlet을 사용 하 여 구성 되는 모든 사서함 감사 바이패스 연결 설정은 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-366">Any mailbox audit bypass association settings (configured by using the **Set-MailboxAuditBypassAssociation** cmdlet) are ignored.</span></span>

- <span data-ttu-id="90ae0-367">기존 사서함 감사 레코드는 레코드에 대 한 감사 로그 기간 제한이 만료 될 때까지 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-367">Existing mailbox audit records are retained until the audit log age limit for the the record expires.</span></span>

### <a name="turn-on-mailbox-auditing-on-by-default"></a><span data-ttu-id="90ae0-368">기본적으로 사서함 감사 켜기</span><span class="sxs-lookup"><span data-stu-id="90ae0-368">Turn on mailbox auditing on by default</span></span>

<span data-ttu-id="90ae0-369">조직에 대 한 사서함 감사를 다시 설정 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-369">To turn mailbox auditing back on for your organization, run the following command in Exchange Online PowerShell:</span></span>

```
Set-OrganizationConfig -AuditDisabled $false
```

## <a name="bypass-mailbox-audit-logging"></a><span data-ttu-id="90ae0-370">사서함 감사 로깅 바이패스</span><span class="sxs-lookup"><span data-stu-id="90ae0-370">Bypass mailbox audit logging</span></span>

<span data-ttu-id="90ae0-371">현재 조직에서 사서함 감사가 기본적으로 설정 된 경우에는 특정 사서함에 대해 사서함 감사를 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-371">Currently, you can't disable mailbox auditing for specific mailboxes when mailbox auditing on by default is turned on in your organization.</span></span> <span data-ttu-id="90ae0-372">예를 들어 *Auditenabled* mailbox 속성을 **False** 로 설정 하는 것은 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-372">For example, setting the *AuditEnabled* mailbox property to **False** is ignored.</span></span>

<span data-ttu-id="90ae0-373">그러나 Exchange Online PowerShell에서 **get-mailboxauditbypassassociation** cmdlet을 사용 하 여 작업이 수행 되는 위치에 관계 없이 지정 된 사용자의 *모든* 사서함 작업이 로깅되지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-373">However, you can still use the **Set-MailboxAuditBypassAssociation** cmdlet in Exchange Online PowerShell to prevent *any and all* mailbox actions by the specified users from being logged, regardless where the actions occur.</span></span> <span data-ttu-id="90ae0-374">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-374">For example:</span></span>

- <span data-ttu-id="90ae0-375">바이패스 된 사용자가 수행한 사서함 소유자 작업은 로깅되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-375">Mailbox owner actions performed by the bypassed users aren't logged.</span></span>

- <span data-ttu-id="90ae0-376">공유 사서함을 포함 하 여 다른 사용자의 사서함에 대 한 바이패스 된 사용자가 수행 하는 위임 작업은 기록 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-376">Delegate actions performed by the bypassed users on other users' mailboxes (including shared mailboxes) aren't logged.</span></span>

- <span data-ttu-id="90ae0-377">바이패스 된 사용자가 수행한 관리 작업은 로깅되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-377">Admin actions performed by the bypassed users aren't logged.</span></span>

<span data-ttu-id="90ae0-378">특정 사용자에 대 한 사서함 감사 로깅을 무시 하려면 MailboxIdentity \<\> 을 사용자의 이름, 전자 메일 주소, 별칭 또는 upn (사용자 계정 이름)으로 바꾸고 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-378">To bypass mailbox audit logging for a specific user, replace \<MailboxIdentity\> with the name, email address, alias, or user principal name (username) of the user and run the following command:</span></span>

```
Set-MailboxAuditBypassAssociation -Identity <MailboxIdentity> -AuditByPassEnabled $true
```

<span data-ttu-id="90ae0-379">지정한 사용자에 대해 감사가 무시 되는지 확인 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-379">To verify that auditing is bypassed for the specified user, run the following command:</span></span>

```
Get-MailboxAuditBypassAssociation -Identity <MailboxIdentity> | Format-List AuditByPassEnabled
```

<span data-ttu-id="90ae0-380">**True** 값은 사용자에 대해 사서함 감사 로깅이 무시 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-380">The value **True** indicates that mailbox audit logging is bypassed for the user.</span></span>

## <a name="more-information"></a><span data-ttu-id="90ae0-381">추가 정보</span><span class="sxs-lookup"><span data-stu-id="90ae0-381">More information</span></span>

- <span data-ttu-id="90ae0-382">기본적으로 사서함 감사 로그 레코드는 삭제 되기 전에 90 일 동안 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-382">By default, mailbox audit log records are retained for 90 days before they're deleted.</span></span> <span data-ttu-id="90ae0-383">Exchange Online PowerShell에서 **설정 된 사서함** Cmdlet의 *Auditlogagelimit* 매개 변수를 사용 하 여 감사 로그 레코드의 보존 기간을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-383">You can change the age limit for audit log records by using the *AuditLogAgeLimit* parameter on the **Set-Mailbox** cmdlet in Exchange Online PowerShell.</span></span> <span data-ttu-id="90ae0-384">그러나이 값을 높이면 Microsoft 365 감사 로그에서 90 일 보다 오래 된 이벤트를 검색할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-384">However, increasing this value doesn't allow you to search for events that are older than 90 days in the Microsoft 365 audit log.</span></span>

  <span data-ttu-id="90ae0-385">보존 기간을 늘릴 경우 Exchange Online PowerShell에서 [search-mailboxauditlog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog) cmdlet을 사용 하 여 사용자의 사서함 감사 로그에서 90 일 보다 오래 된 레코드를 검색 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-385">If you increase the age limit, you need to use the [Search-MailboxAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog) cmdlet in Exchange Online PowerShell to search the user's mailbox audit log for records that are older than 90 days.</span></span>

- <span data-ttu-id="90ae0-386">조직에 대해 기본적으로 사서함 감사를 수행 하기 전에 사서함에 대 한 *Auditlogagelimit* 속성을 변경한 경우 사서함의 기존 감사 로그 보존 기간은 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-386">If you've changed the *AuditLogAgeLimit* property for a mailbox prior to mailbox auditing on by default being turned on for organization, the mailbox's existing audit log age limit isn't changed.</span></span> <span data-ttu-id="90ae0-387">즉, 기본적으로 사서함을 감사 하는 경우 사서함 감사 레코드의 현재 보존 기간에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-387">In other words, mailbox auditing on by default doesn't effect the current age limit for mailbox audit records.</span></span>

- <span data-ttu-id="90ae0-388">Office 365 그룹 사서함에서 *Auditlogagelimit* 값을 변경 하려면 `-GroupMailbox` **Set-mailbox** 명령에 스위치를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-388">To change the *AuditLogAgeLimit* value on an Office 365 Group mailbox, you need to include the `-GroupMailbox` switch in the **Set-Mailbox** command.</span></span>

- <span data-ttu-id="90ae0-389">사서함 감사 로그 레코드는 각 사용자의 사서함에 있는 복구할 수 있는 항목 폴더에 있는 하위 폴더 ( *감사*)에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-389">Mailbox audit log records are stored in a subfolder (named *Audits*) in the Recoverable Items folder in each user's mailbox.</span></span> <span data-ttu-id="90ae0-390">사서함 감사 레코드 및 복구할 수 있는 항목 폴더에 대해서는 다음 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-390">Keep the following things in mind about mailbox audit records and the Recoverable Items folder:</span></span>

  - <span data-ttu-id="90ae0-391">사서함 감사 레코드는 복구 가능한 항목 폴더의 저장소 할당량을 기준으로 계산 됩니다 (기본적으로 30GB) (경고 할당량은 20gb).</span><span class="sxs-lookup"><span data-stu-id="90ae0-391">Mailbox audit records count against the storage quota of the Recoverable Items folder, which is 30GB by default (the warning quota is 20 GB).</span></span> <span data-ttu-id="90ae0-392">저장소 할당량은 다음과 같은 경우 자동으로 100 GB (90 GB 경고 할당량 포함)로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-392">The storage quota is automatically increased to 100 GB (with a 90 GB warning quota) when:</span></span>

    - <span data-ttu-id="90ae0-393">보류가 사서함에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-393">A hold is placed on a mailbox.</span></span>

    - <span data-ttu-id="90ae0-394">사서함이 준수 센터의 보존 정책에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-394">The mailbox is assigned to a retention policy in the Compliance Center.</span></span>

  - <span data-ttu-id="90ae0-395">또한 사서함 감사 레코드는 [복구 가능한 항목 폴더에 대 한 폴더 제한](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#mailbox-folder-limits)에 대해서도 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-395">Mailbox audit records also count against the [folder limit for the Recoverable Items folder](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#mailbox-folder-limits).</span></span> <span data-ttu-id="90ae0-396">감사 하위 폴더에는 최대 300만 개의 항목을 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-396">A maximum of 3 million items (audit records) can be stored in the Audits subfolder.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90ae0-397">기본적으로 사서함 감사가 복구 가능한 항목 폴더의 저장소 할당량 또는 폴더 제한에 영향을 주는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-397">It's unlikely that mailbox auditing on by default will impact the storage quota or the folder limit for the Recoverable Items folder.</span></span>

    - <span data-ttu-id="90ae0-398">Exchange Online PowerShell에서 다음 명령을 실행 하 여 복구 가능한 항목 폴더의 감사 하위 폴더에 있는 항목의 크기 및 수를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-398">You can run the following command in Exchange Online PowerShell to display the size and number of items in the Audits subfolder in the Recoverable Items folder:</span></span>

      ```
      Get-MailboxFolderStatistics -Identity <MailboxIdentity> -FolderScope RecoverableItems | Where-Object {$_.Name -eq 'Audits'} | Format-List FolderPath,FolderSize,ItemsInFolder
      ```

    - <span data-ttu-id="90ae0-399">복구 가능한 항목 폴더의 감사 로그 레코드에 직접 액세스할 수는 없습니다. 대신 **search-mailboxauditlog** cmdlet을 사용 하거나 Microsoft 365 감사 로그를 검색 하 여 사서함 감사 레코드를 찾아서 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-399">You can't directly access an audit log record in the Recoverable Items folder; instead, you use the **Search-MailboxAuditLog** cmdlet or search the Microsoft 365 audit log to find and view mailbox audit records.</span></span>

- <span data-ttu-id="90ae0-400">사서함이 보류 중이거나 준수 센터의 보존 정책에 할당 된 경우에는 사서함의 *Auditlogagelimit* 속성에 정의 된 기간 동안 감사 로그 레코드가 여전히 보존 됩니다 (기본적으로 90 days).</span><span class="sxs-lookup"><span data-stu-id="90ae0-400">If a mailbox is placed on hold or assigned to a retention policy in the Compliance Center, audit log records are still retained for the duration that's defined by the mailbox's *AuditLogAgeLimit* property (90 days by default).</span></span> <span data-ttu-id="90ae0-401">보류 중인 사서함에 대해 감사 로그 레코드를 더 오랫동안 보존 하려면 사서함의 *Auditlogagelimit* 값을 늘려야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90ae0-401">To retain audit log records longer for mailboxes on hold, you need to increase mailbox's *AuditLogAgeLimit* value.</span></span>
