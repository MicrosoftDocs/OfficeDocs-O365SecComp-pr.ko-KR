---
title: Office 365에서 아웃 바운드 스팸 정책 알림 구성
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/10/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
ms.collection:
- M365-security-compliance
description: 관리자는 Office 365에서 아웃 바운드 스팸 감지에 대 한 알림 설정을 수정 하는 방법을 확인할 수 있습니다.
ms.openlocfilehash: c48b6cd634417a00040fb5479313782b44f6aa8d
ms.sourcegitcommit: 81b3bff27bc60235a38004c5b0297ac454331b25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2019
ms.locfileid: "36822518"
---
# <a name="configure-outbound-spam-policy-notifications-in-office-365"></a><span data-ttu-id="c2e81-103">Office 365에서 아웃 바운드 스팸 정책 알림 구성</span><span class="sxs-lookup"><span data-stu-id="c2e81-103">Configure outbound spam policy notifications in Office 365</span></span>

<span data-ttu-id="c2e81-104">아웃바운드 전자 메일 보내기 서비스를 사용하는 경우 아웃바운드 스팸 필터링이 항상 사용하도록 설정되므로 서비스와 받는 사람을 사용하여 조직을 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-104">Outbound spam filtering is always enabled if you use the service for sending outbound email, thereby protecting organizations using the service and their intended recipients.</span></span> <span data-ttu-id="c2e81-105">인바운드 필터링과 마찬가지로 아웃바운드 스팸 필터링도 연결 필터링과 콘텐츠 필터링으로 구성되지만, 아웃바운드 필터 설정은 구성할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-105">Similar to inbound filtering, outbound spam filtering is comprised of connection filtering and content filtering, however the outbound filter settings are not configurable.</span></span> <span data-ttu-id="c2e81-106">스팸으로 확인된 아웃바운드 메시지는 위험성이 높은 배달 풀을 통해 라우팅되므로 일반 아웃바운드 IP 풀이 차단 목록에 추가될 가능성이 줄어듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-106">If an outbound message is determined to be spam, it is routed through the higher risk delivery pool, which reduces the probability of the normal outbound-IP pool being added to a block list.</span></span> <span data-ttu-id="c2e81-107">서비스를 통해 아웃바운드 스팸을 계속 보내는 고객에 대해서는 메시지 보내기가 차단됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-107">If a customer continues to send outbound spam through the service, they will be blocked from sending messages.</span></span>

<span data-ttu-id="c2e81-108">아웃 바운드 스팸 필터링을 사용 하지 않도록 설정 하거나 변경할 수는 없지만 다음과 같은 아웃 바운드 스팸 알림 설정을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-108">Although you can't disable or change outbound spam filtering, you can configure the following outbound spam notification settings:</span></span>

- <span data-ttu-id="c2e81-109">**의심 스러운 메시지 복사본 보내기**: 이러한 메시지는 SCL 등급에 관계 없이 스팸으로 표시 되며, 필터에 의해 거부 되지 않으며, 위험성이 높은 배달 풀을 통해 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-109">**Send copies of suspicious messages**: These messages are marked as spam (regardless of the SCL rating) and are not rejected by the filter, but are routed through the higher risk delivery pool.</span></span> <span data-ttu-id="c2e81-110">EAC (exchange 관리 센터) 또는 exchange online powershell 또는 exchange online Protection powershell의 \*\* \*-get-hostedoutboundspamfilterpolicy\*\* cmdlet을 사용 하 여 검색 된 이러한 메시지에 대 한 받는 사람을 추가로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-110">You can use the Exchange admin center (EAC) or the **\*-HostedOutboundSpamFilterPolicy** cmdlets in Exchange Online PowerShell or Exchange Online Protection PowerShell to specify addition recipients for these detected messages.</span></span> <span data-ttu-id="c2e81-111">받는 사람이 **숨은 참조** 로 추가 됩니다 (보낸 **사람 및 받는 사람 필드는 원본** 에 **대** 한 sender 및 recipients).</span><span class="sxs-lookup"><span data-stu-id="c2e81-111">Note that the recipients are added as **Bcc** recipients (the **From** and **To** fields are the original sender and recipient).</span></span>

- <span data-ttu-id="c2e81-112">**보낸 사람이 차단 된 경우 알림 보내기**: 상당한 양의 스팸이 특정 사용자 로부터 들어오는 경우 사용자는 전자 메일 메시지를 보낼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-112">**Send notifications when a sender is blocked**: When a significant amount of spam is coming from a particular user, the user is disabled from sending email messages.</span></span> <span data-ttu-id="c2e81-113">기본적으로 관리자에 게 알림이 제공 되지만 Office 365 보안 & 준수 센터에서 **전자 메일을 보내는 사용자 제한** [정책을](alert-policies.md) 사용 하 여 추가 알림 받는 사람을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-113">Admins are notified by default, but you can use the **User restricted from sending email** [alert policy](alert-policies.md) in the Office 365 Security & Compliance Center to configure additional notification recipients.</span></span>

  <span data-ttu-id="c2e81-114">이 알림의 모양을 보려면 [보낸 사람이 보내는 아웃 바운드 스팸 차단 되 면 샘플 알림](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c2e81-114">To see what this notification looks like, see [Sample notification when a sender is blocked sending outbound spam](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md).</span></span> <span data-ttu-id="c2e81-115">다시 사용 하도록 설정 하는 방법에 대 한 자세한 내용은 [스팸 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소 제거](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2e81-115">For information about getting re-enabled, see [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="c2e81-116">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="c2e81-116">What do you need to know before you begin?</span></span>

- <span data-ttu-id="c2e81-117">예상 완료 시간: 5분</span><span class="sxs-lookup"><span data-stu-id="c2e81-117">Estimated time to complete: 5 minutes</span></span>

- <span data-ttu-id="c2e81-118">보안 및 준수 센터를 열려면 [Office 365 보안 및 준수 센터로 이동](go-to-the-securitycompliance-center.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c2e81-118">To open the Security & Compliance Center, see [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md).</span></span>

- <span data-ttu-id="c2e81-119">EAC를 열려면 exchange online 또는 exchange online [Protection](exchange-admin-center-in-exchange-online-protection-eop.md)의 exchange [관리 센터](https://docs.microsoft.com/Exchange/exchange-admin-center) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c2e81-119">To open the EAC, see [Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) or [Exchange admin center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="c2e81-120">Exchange Online PowerShell을 열려면 [Exchange Online powershell에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2e81-120">To open Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="c2e81-121">Exchange Online Protection PowerShell을 열려면 [Exchange Online Protection powershell에 연결](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2e81-121">To open Exchange Online Protection PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="c2e81-122">이 절차를 수행 하려면 먼저 계정에 사용 권한을 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-122">Your account needs to be assigned permissions before you can perform this procedure.</span></span> <span data-ttu-id="c2e81-123">필요한 사용 권한을 확인 하려면 [Office 365 보안 & 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)에서 "알림 관리" 역할 항목을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2e81-123">To see what permissions you need, see the "Manage Alerts" role entry in [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="use-the-eac-to-configure-additional-recipients-for-outbound-spam-messages"></a><span data-ttu-id="c2e81-124">EAC를 사용 하 여 아웃 바운드 스팸 메시지에 대 한 추가 받는 사람 구성</span><span class="sxs-lookup"><span data-stu-id="c2e81-124">Use the EAC to configure additional recipients for outbound spam messages</span></span>

1. <span data-ttu-id="c2e81-125">EAC에서 **보호** \> **아웃 바운드 스팸으로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-125">In the EAC, go to **Protection** \> **Outbound spam**.</span></span>

2. <span data-ttu-id="c2e81-126">**Default**라는 정책을 선택 하 고 편집 아이콘](media/ITPro-EAC-EditIcon.png) **편집** ![을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-126">Select the policy named **Default**, and then click **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.png).</span></span>

3. <span data-ttu-id="c2e81-127">등록 정보 페이지가 열리면 **아웃 바운드 스팸 기본 설정** 탭이 선택 되어 있는지 확인 하 고 다음 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-127">In the properties page that opens, verify that the **Outbound spam preferences** tab is selected, and then configure the following setting:</span></span>

   <span data-ttu-id="c2e81-128">**의심 스러운 모든 아웃 바운드 전자 메일 메시지의 복사본을 다음 전자 메일 주소 또는 주소로 보내기**:이 확인란을 선택 하 고 검색 된 메시지의 **숨은 참조** 필드에 추가 해야 하는 하나 이상의 관리자 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-128">**Send a copy of all suspicious outbound email messages to the following email address or addresses**: Select the check box and enter the email addresses of one or more administrators who should be added to the **Bcc** field of detected messages.</span></span> <span data-ttu-id="c2e81-129">세미콜론 (;)을 사용 하 여 여러 전자 메일 주소를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-129">Separate multiple email addresses with a semicolon ( ; ).</span></span>

   <span data-ttu-id="c2e81-130">작업을 마친 후 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-130">When you're finished, click **Save**.</span></span>

### <a name="use-exchange-online-powershell-or-exchange-online-protection-powershell-to-configure-additional-recipients-for-outbound-spam-messages"></a><span data-ttu-id="c2e81-131">Exchange Online PowerShell 또는 Exchange Online Protection PowerShell을 사용 하 여 아웃 바운드 스팸 메시지에 대 한 추가 받는 사람 구성</span><span class="sxs-lookup"><span data-stu-id="c2e81-131">Use Exchange Online PowerShell or Exchange Online Protection PowerShell to configure additional recipients for outbound spam messages</span></span>

<span data-ttu-id="c2e81-132">아웃 바운드 스팸 메시지에 대 한 추가 받는 사람을 사용 하도록 설정 하 고 구성 하려면 다음 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-132">To enable and configure additional recipients for outbound spam messages, use the following syntax:</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients <recipients>
```

- <span data-ttu-id="c2e81-133">기존 값을 모두 덮어쓰는 받는 사람을 지정 하려면 구문을 `emailaddress1,emailaddress2,...emailaddressN`사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-133">To specify recipients that overwrite all existing values, use the syntax `emailaddress1,emailaddress2,...emailaddressN`.</span></span>

- <span data-ttu-id="c2e81-134">다른 항목에 영향을 주지 않고 받는 사람을 선택적으로 추가 하거나 제거 `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`하려면 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-134">To selectively add or remove recipients without affecting the other entries, use the syntax `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`.</span></span>

<span data-ttu-id="c2e81-135">이 예에서는 chris@contoso.com, laura@contoso.com 및 julia@contoso.com를 숨은 참조 받는 사람을 아웃 바운드 스팸 메시지에 대해 사용 하도록 설정 하 고 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-135">This example enables and configures chris@contoso.com, laura@contoso.com and julia@contoso.com as Bcc recipients for outbound spam messages.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients chris@contoso.com,laura@contoso.com,julia@contoso.com
```

<span data-ttu-id="c2e81-136">이 예에서는 michelle@contoso.com를 추가 숨은 참조 받는 사람으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-136">This example adds michelle@contoso.com as an additional Bcc recipient.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Add=michelle@contoso.com}
```

<span data-ttu-id="c2e81-137">이 예에서는 숨은 참조 받는 사람 목록에서 chris@contoso.com 및 julia@contoso.com을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-137">This example removes chris@contoso.com and julia@contoso.com from the list of Bcc recipients.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Remove='chris@contoso.com','julia@contoso.com'}
```

<span data-ttu-id="c2e81-138">구문 및 매개 변수에 대 한 자세한 내용은 [get-hostedoutboundspamfilterpolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c2e81-138">For detailed syntax and parameter information, see [Set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).</span></span>

<span data-ttu-id="c2e81-139">**Note**: 명령을 `Get-HostedOutboundSpamFilterPolicy | Format-List` 실행 하 여 *사람은 bccsuspiciousoutboundmail* 및 *BccSuspiciousOutboundAdditionalRecipients* 속성의 현재 값을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-139">**Note**: Run the command `Get-HostedOutboundSpamFilterPolicy | Format-List` to see the current values of the *BccSuspiciousOutboundMail* and *BccSuspiciousOutboundAdditionalRecipients* properties.</span></span>

## <a name="use-the-security--compliance-center-to-configure-notifications-when-a-sender-is-blocked"></a><span data-ttu-id="c2e81-140">보안 & 준수 센터를 사용 하 여 보낸 사람이 차단 된 경우 알림을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-140">Use the Security & Compliance Center to configure notifications when a sender is blocked</span></span>

1. <span data-ttu-id="c2e81-141">보안 & 준수 센터에서 **알림** \> **경고 정책**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-141">In the Security & Compliance Center, go to **Alerts** \> **Alert Policies**.</span></span>

2. <span data-ttu-id="c2e81-142">**사용자가 전자 메일을 보낼 수 없도록 제한**된 정책을 찾아 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-142">Find and select the policy named **User restricted from sending email**.</span></span>

3. <span data-ttu-id="c2e81-143">플라이 아웃이 열리면 **정책 편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-143">In the fly out that opens, click **Edit policy**.</span></span>

4. <span data-ttu-id="c2e81-144">표시 된 **받는 사람 편집** 페이지에서 다음 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-144">In the **Edit recipients** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="c2e81-145">**전자 메일 알림 보내기** **:가 선택 되어 있는지 확인** 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-145">**Send email notifications**: Verify that **On** is selected.</span></span>

   - <span data-ttu-id="c2e81-146">**전자 메일 받는 사람**: 기본적으로 **tenantadmins** 가 여기에 불과합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-146">**Email recipients**: By default **TenantAdmins** is the only value here.</span></span> <span data-ttu-id="c2e81-147">받는 사람을 더 추가 하려면이 상자에서 비어 있는 지점을 클릭 하 고 받는 사람 입력을 시작한 다음 이름이 확인 되 면 받는 사람을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-147">To add additional recipients, click in an empty spot in this box, start typing the recipient, and select the recipient when their name resolves.</span></span> <span data-ttu-id="c2e81-148">받는 사람을 제거 하려면 이름 옆에 있는 **X** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-148">To remove recipients, click on the **X** next to their names.</span></span>

   - <span data-ttu-id="c2e81-149">**일별 알림 제한**: 기본값은 **제한이**없지만 1에서 200 사이의 다양 한 제한을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-149">**Daily notification limit**: The default value is **No limit**, but you can configure various limits from 1 to 200.</span></span>

   <span data-ttu-id="c2e81-150">작업을 마친 후 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e81-150">When you're finished, click **Save**.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="c2e81-151">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="c2e81-151">For more information</span></span>

[<span data-ttu-id="c2e81-152">아웃 바운드 메시지에 대 한 위험성이 높은 배달 풀</span><span class="sxs-lookup"><span data-stu-id="c2e81-152">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="c2e81-153">스팸 방지 보호 기능 FAQ</span><span class="sxs-lookup"><span data-stu-id="c2e81-153">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
