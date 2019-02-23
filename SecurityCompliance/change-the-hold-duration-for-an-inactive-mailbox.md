---
title: Office 365에서 비활성 사서함에 대 한 보존 기간 변경
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/29/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: bdee24ed-b8cf-4dd0-92ae-b86ec4661e6b
description: Office 365 사서함이 비활성 상태가 되 면 비활성 사서함에 할당 된 보류 또는 Office 365 보존 정책의 기간을 변경할 수 있습니다. 보류 기간은 복구 가능한 항목 폴더에서 항목이 보관 되는 기간을 정의 합니다.
ms.openlocfilehash: 3f92d51505ba8a9a9f4b8e78d0fb79036b6db489
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220618"
---
# <a name="change-the-hold-duration-for-an-inactive-mailbox-in-office-365"></a><span data-ttu-id="acbaf-104">Office 365에서 비활성 사서함에 대 한 보존 기간 변경</span><span class="sxs-lookup"><span data-stu-id="acbaf-104">Change the hold duration for an inactive mailbox in Office 365</span></span>

<span data-ttu-id="acbaf-p102">비활성 사서함은 조직에서 이전 직원의 전자 메일을 유지 하는 데 사용 됩니다. 소송 보존, 원본 위치 유지, Office 365 보존 정책 또는 eDiscovery 사례와 연결 된 보류가 사서함에 배치 되 고 해당 Office 365 사용자 계정이 삭제 되 면 사서함이 비활성화 됩니다. 비활성 사서함의 콘텐츠는 비활성 상태로 설정 되기 전에 사서함에 적용 된 보류 기간 동안 보존 됩니다. 보류 기간은 복구 가능한 항목 폴더에서 항목이 보관 되는 기간을 정의 합니다. 복구 가능한 항목 폴더의 항목에 대 한 보존 기간이 만료 되 면 해당 항목이 비활성 사서함에서 영구적으로 삭제 (제거) 됩니다. 사서함을 비활성화 한 후 비활성 사서함에 할당 된 보류 또는 Office 365 보존 정책의 기간을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p102">An inactive mailbox is used to retain a former employee's email after he or she leaves your organization. A mailbox becomes inactive when a Litigation Hold, an In-Place Hold, an Office 365 retention policy, or a hold that's associated with an eDiscovery case is placed on the mailbox, and the corresponding Office 365 user account is deleted. The contents of an inactive mailbox are retained for the duration of the hold that was placed on the mailbox before it was made inactive. The hold duration defines how long items in the Recoverable Items folder are held. When the hold duration expires for an item in the Recoverable Items folder, the item is permanently deleted (purged) from the inactive mailbox. After a mailbox is made inactive, you can change the duration of the hold or Office 365 retention policy assigned to the inactive mailbox.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="acbaf-p103">사서함을 비활성화하기 위해 새 원본 위치 유지를 만들 수 있는 2017년 7월 1일 마감 날짜를 연기했습니다. 하지만 올해 말이나 내년 초에는 Exchange Online에 새 원본 위치 유지를 만들 수 없습니다. 그때는 소송 보존과 Office 365 보존 정책만 사용하여 비활성화 사서함을 만들 수 있습니다. 그러나 원본 위치 유지에 있는 기존 비활성화 사서함은 계속 지원되며 비활성화 사서함에서 원본 위치 유지를 계속 관리할 수 있습니다. 관리 항목으로는 원본 위치 유지 기간 변경 및 원본 위치 유지를 삭제하여 비활성화 사서함을 영구 삭제하는 작업이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds to make a mailbox inactive. But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. At that time, only Litigation Holds and Office 365 retention policies can be used to create an inactive mailbox. However, existing inactive mailboxes that are on In-Place Hold will still be supported, and you can continue to manage the In-Place Holds on inactive mailboxes. This includes changing the duration of an In-Place Hold and permanently deleting an inactive mailbox by removing the In-Place Hold.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="acbaf-116">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="acbaf-116">Before you begin</span></span>

- <span data-ttu-id="acbaf-p104">비활성 사서함의 소송 보존에 대 한 보존 기간을 변경 하려면 Exchange Online PowerShell을 사용 해야 합니다. EAC (Exchange 관리 센터)를 사용할 수 없습니다. 그러나 Exchange Online PowerShell 또는 EAC를 사용 하 여 원본 위치 유지에 대 한 보존 기간을 변경할 수 있습니다. office 365 보안 &amp; 및 준수 센터 또는 보안 &amp; 준수 센터 PowerShell을 사용 하 여 office 365 보존 정책의 보류 기간을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p104">You have to use Exchange Online PowerShell to change the hold duration for a Litigation Hold on an inactive mailbox. You can't use the Exchange admin center (EAC). But you can use Exchange Online PowerShell or the EAC to change the hold duration for an In-Place Hold. You can use the Office 365 Security &amp; Compliance Center or the Security &amp; Compliance Center PowerShell to change the hold duration for an Office 365 retention policy.</span></span>
    
- <span data-ttu-id="acbaf-121">Exchange Online powershell 또는 보안 &amp; 준수 센터 PowerShell에 연결 하려면 다음 항목 중 하나를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="acbaf-121">To connect to Exchange Online PowerShell or Security &amp; Compliance Center PowerShell, see one of the following topics:</span></span>
    
  - [<span data-ttu-id="acbaf-122">원격 PowerShell을 사용하여 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="acbaf-122">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
  - [<span data-ttu-id="acbaf-123">Office 365 보안 및 준수 센터 PowerShell에 연결</span><span class="sxs-lookup"><span data-stu-id="acbaf-123">Connect to Office 365 Security &amp; Compliance Center PowerShell</span></span>](https://go.microsoft.com/fwlink/?linkid=799771)
    
- <span data-ttu-id="acbaf-p105">eDiscovery 사례와 관련 된 보류는 무제한 보존으로, 변경할 수 있는 보존 기간은 없습니다. 항목이 영구적으로 또는 보류를 제거 하 고 비활성 사서함이 삭제 될 때까지 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p105">Note that holds associated with eDiscovery cases are infinite holds, which means there is no hold duration that can be changed. Items are held forever or until the hold is removed and the inactive mailbox is deleted.</span></span>
    
- <span data-ttu-id="acbaf-126">비활성 사서함에 대 한 자세한 내용은 [Office 365의 비활성 사서함](inactive-mailboxes-in-office-365.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="acbaf-126">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a><span data-ttu-id="acbaf-127">1 단계: 비활성 사서함의 보류 확인</span><span class="sxs-lookup"><span data-stu-id="acbaf-127">Step 1: Identify the holds on an inactive mailbox</span></span>

<span data-ttu-id="acbaf-128">비활성 사서함에는 여러 가지 유형의 보류 또는 하나 이상의 Office 365 보존 정책이 적용 될 수 있으므로 첫 번째 단계는 비활성 사서함에 대 한 보류를 확인 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-128">Because different types of holds or one or more Office 365 retention policies might be placed on an inactive mailbox, the first step is to identify the holds on an inactive mailbox.</span></span>
  
<span data-ttu-id="acbaf-129">Exchange Online PowerShell에서 다음 명령을 실행 하 여 조직의 모든 비활성 사서함에 대 한 보류 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-129">Run the following command in Exchange Online PowerShell to display the hold information for all inactive mailboxes in your organization.</span></span>
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,LitigationHoldDuration,InPlaceHolds
```
   
<span data-ttu-id="acbaf-p106">**LitigationHoldEnabled** 속성의 **True** 값은 비활성 사서함이 소송 보존 상태를 나타냅니다. 원본 위치 유지, eDiscovery 보존 또는 Office 365 보존 정책이 비활성 사서함에 배치 되 면 보류 또는 보존 정책에 대 한 GUID가 **InPlaceHolds** 속성의 값으로 표시 됩니다. 예를 들어 다음은 5 개의 비활성 사서함에 대 한 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p106">The value of **True** for the **LitigationHoldEnabled** property indicates that the inactive mailbox is on Litigation Hold. If an In-Place Hold, eDiscovery hold, or Office 365 retention policy is placed on an inactive mailbox, a GUID for the hold or retention policy is displayed as the value for the **InPlaceHolds** property. For example, the following shows results for 5 inactive mailboxes.</span></span> 
  
||
|:-----|
|
```
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
LitigationHoldDuration: 365.00:00:00
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491}
...
DisplayName           : Mario Necaise
Name                  : marion
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {}
...
DisplayName           : Carol Olson
Name                  : carolo
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {mbxcdbbb86ce60342489bff371876e7f224}
...
DisplayName           : Abraham McMahon
Name                  : abrahamm
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {UniH7d895d48-7e23-4a8d-8346-533c3beac15d}
```
   
<span data-ttu-id="acbaf-133">다음 표에는 각 사서함을 비활성화 하는 데 사용 되는 5 가지 서로 다른 보존 유형이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-133">The following table identifies the five different hold types that were used to make each mailbox inactive.</span></span>
  
|<span data-ttu-id="acbaf-134">**비활성 사서함**</span><span class="sxs-lookup"><span data-stu-id="acbaf-134">**Inactive mailbox**</span></span>|<span data-ttu-id="acbaf-135">**보류 유형**</span><span class="sxs-lookup"><span data-stu-id="acbaf-135">**Hold type**</span></span>|<span data-ttu-id="acbaf-136">**비활성 사서함에서 보류를 확인 하는 방법**</span><span class="sxs-lookup"><span data-stu-id="acbaf-136">**How to identify the hold on the inactive mailbox**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="acbaf-137">Ann Beebe</span><span class="sxs-lookup"><span data-stu-id="acbaf-137">Ann Beebe</span></span>  <br/> |<span data-ttu-id="acbaf-138">소송 보존</span><span class="sxs-lookup"><span data-stu-id="acbaf-138">Litigation Hold</span></span>  <br/> |<span data-ttu-id="acbaf-139">*LitigationHoldEnabled* 속성은로 `True`설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-139">The  *LitigationHoldEnabled*  property is set to  `True`.</span></span>  <br/> |
|<span data-ttu-id="acbaf-140">Pilar Pinilla</span><span class="sxs-lookup"><span data-stu-id="acbaf-140">Pilar Pinilla</span></span>  <br/> |<span data-ttu-id="acbaf-141">원본 위치 유지</span><span class="sxs-lookup"><span data-stu-id="acbaf-141">In-Place Hold</span></span>  <br/> |<span data-ttu-id="acbaf-p107">*InPlaceHolds* 속성은 비활성 사서함에 배치 된 원본 위치 유지의 GUID를 포함 합니다. ID가 접두사로 시작 되지 않으므로 현재 위치 유지로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p107">The  *InPlaceHolds*  property contains the GUID of the In-Place Hold that's placed on the inactive mailbox. You can tell this is an In-Place Hold because the ID doesn't start with a prefix.  </span></span><br/> <span data-ttu-id="acbaf-144">Exchange Online PowerShell의 `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` 명령을 사용 하 여 비활성 사서함의 원본 위치 유지에 대 한 정보를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-144">You can use the  `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` command in Exchange Online PowerShell to get information about the In-Place Hold on the inactive mailbox.</span></span>  <br/> |
|<span data-ttu-id="acbaf-145">고 대 Necaise</span><span class="sxs-lookup"><span data-stu-id="acbaf-145">Mario Necaise</span></span>  <br/> |<span data-ttu-id="acbaf-146">보안 &amp; 및 준수 센터의 조직 전체 Office 365 보존 정책</span><span class="sxs-lookup"><span data-stu-id="acbaf-146">Organization-wide Office 365 retention policy in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="acbaf-p108">*InPlaceHolds* 속성은 비어 있습니다. 이는 하나 이상의 조직 전체 또는 (Exchange 전체) Office 365 보존 정책이 비활성 사서함에 적용 됨을 나타냅니다. 이 경우 Exchange Online PowerShell에서 `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` 명령을 실행 하 여 조직 전반의 Office 365 보존 정책의 guid 목록을 가져올 수 있습니다. Exchange 사서함에 적용 되는 조직 전체 보존 정책의 GUID는 `mbx` 접두사로 시작 합니다. 예를 `mbxa3056bb15562480fadb46ce523ff7b02`들어</span><span class="sxs-lookup"><span data-stu-id="acbaf-p108">The  *InPlaceHolds*  property is empty. This indicates that one or more organization-wide or (Exchange-wide) Office 365 retention policy is applied to the inactive mailbox. In this case, you can run the  `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies that are applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  </span></span><br/> <br/><span data-ttu-id="acbaf-151">비활성 사서함에 적용 되는 Office 365 보존 정책을 식별 하려면 보안 &amp; 준수 센터 PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-151">To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.</span></span>  <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>
|<span data-ttu-id="acbaf-152">에이 옛 아들</span><span class="sxs-lookup"><span data-stu-id="acbaf-152">Carol Olson</span></span>  <br/> |<span data-ttu-id="acbaf-153">특정 사서함에 적용 되는 보안 &amp; 및 준수 센터의 Office 365 보존 정책</span><span class="sxs-lookup"><span data-stu-id="acbaf-153">Office 365 retention policy in the Security &amp; Compliance Center applied to specific mailboxes</span></span>  <br/> |<span data-ttu-id="acbaf-p109">*InPlaceHolds* 속성은 비활성 사서함에 적용 되는 Office 365 보존 정책의 GUID를 포함 합니다. GUID는 `mbx` 접두사로 시작 되므로 특정 사서함에 적용 되는 보존 정책 임을 확인할 수 있습니다. 비활성 사서함에 적용 된 보존 정책의 GUID가 `skp` 접두사로 시작 되 면 보존 정책이 비즈니스용 Skype 대화에 적용 되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p109">The  *InPlaceHolds*  property contains the GUID of the Office 365 retention policy that's applied to the inactive mailbox. You can tell this is a retention policy that applied to specific mailboxes because the GUID starts with the  `mbx` prefix. Note that if GUID of the retention policy applied to the inactive mailbox started with the  `skp` prefix, that would indicate that the retention policy is applied to Skype for Business conversations.  </span></span><br/><br/> <span data-ttu-id="acbaf-157">비활성 사서함에 적용 되는 Office 365 보존 정책을 식별 하려면 보안 &amp; 준수 센터 PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-157">To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.</span></span><br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name` <br/><br/><span data-ttu-id="acbaf-158">이 명령을 실행할 때 `mbx` or `skp` 접두사를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-158">Be sure to remove the  `mbx` or  `skp` prefix when you run this command.</span></span>  <br/> |
|<span data-ttu-id="acbaf-159">Abraham McMahon</span><span class="sxs-lookup"><span data-stu-id="acbaf-159">Abraham McMahon</span></span>  <br/> |<span data-ttu-id="acbaf-160">보안 &amp; 및 준수 센터에서 eDiscovery 사례 보류</span><span class="sxs-lookup"><span data-stu-id="acbaf-160">eDiscovery case hold in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="acbaf-p110">*InPlaceHolds* 속성은 비활성 사서함에 저장 된 eDiscovery 사례 보류의 GUID를 포함 합니다. GUID는 `UniH` 접두사로 시작 되므로 eDiscovery 사례 보류 임을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p110">The  *InPlaceHolds*  property contains the GUID of the eDiscovery case hold that's placed on the inactive mailbox. You can tell this is an eDiscovery case hold because the GUID starts with the  `UniH` prefix.  </span></span><br/> <span data-ttu-id="acbaf-p111">보안 &amp; 및 준수 센터 `Get-CaseHoldPolicy` PowerShell에서 cmdlet을 사용 하 여 비활성 사서함의 보류가 연결 된 eDiscovery 사례에 대 한 정보를 확인할 수 있습니다. 예를 들어 명령을 `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` 실행 하 여 비활성 사서함에 대 한 사례 보류의 이름을 표시할 수 있습니다. 이 명령을 실행할 때 `UniH` 접두사를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p111">You can use the  `Get-CaseHoldPolicy` cmdlet in Security &amp; Compliance Center PowerShell to get information about the eDiscovery case that the hold on the inactive mailbox is associated with. For example, you can run the command  `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` to display the name of the case hold that's on the inactive mailbox. Be sure to remove the  `UniH` prefix when you run this command.  </span></span><br/><br/> <span data-ttu-id="acbaf-166">비활성 사서함의 보류가 연결 된 eDiscovery 사례를 식별 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-166">To identity the eDiscovery case that the hold on the inactive mailbox is associated with, run the following commands.</span></span>  <br/><br/> `$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/> `Get-ComplianceCase $CaseHold.CaseId | FL Name`<br/><br/><br/> <span data-ttu-id="acbaf-p112">**참고:** 비활성 사서함에 대해서는 eDiscovery 보류를 사용 하지 않는 것이 좋습니다. eDiscovery 사례는 법적 문제와 관련 된 특정 시간 바인딩 사례에 사용 되기 때문입니다. 특정 시점에 법적 사례가 종료 되 고 사례와 관련 된 보류가 제거 되 고 eDiscovery 사례가 닫히거나 삭제 됩니다. 실제로 비활성 사서함에 있는 보류가 ediscovery 사례와 연결 되 고 보류가 해제 되거나 eDiscovery 사례가 종료 되거나 삭제 되 면 비활성 사서함이 영구적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p112">**Note:** We don't recommend using eDiscovery holds for inactive mailboxes. That's because eDiscovery cases are intended for specific, time-bound cases related to a legal issue. At some point, a legal case will probably end and the holds associated with the case will be removed and the eDiscovery case will be closed (or deleted). In fact, if a hold that's placed on an inactive mailbox is associated with an eDiscovery case, and the hold is released or the eDiscovery case is closed or deleted, the inactive mailbox will be permanently deleted.</span></span> 

<span data-ttu-id="acbaf-171">Office 365 보존 정책에 대 한 자세한 내용은 [Overview의 보존 정책 개요](retention-policies.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="acbaf-171">For more information about Office 365 retention policies, see [Overview of retention policies](retention-policies.md).</span></span>
  
## <a name="step-2-change-the-hold-duration-for-an-inactive-mailbox"></a><span data-ttu-id="acbaf-172">2 단계: 비활성 사서함에 대 한 보존 기간 변경</span><span class="sxs-lookup"><span data-stu-id="acbaf-172">Step 2: Change the hold duration for an inactive mailbox</span></span>

<span data-ttu-id="acbaf-173">비활성 사서함에 적용 되는 보존 유형 및 여러 보류가 있는지 확인 한 후에는 보존 기간을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-173">After you identify what type of hold is placed on the inactive mailbox (and whether there are multiple holds), the next step is to change the duration for the hold.</span></span> 
  
### <a name="change-the-duration-for-a-litigation-hold"></a><span data-ttu-id="acbaf-174">소송 보존 기간 변경</span><span class="sxs-lookup"><span data-stu-id="acbaf-174">Change the duration for a Litigation Hold</span></span>

<span data-ttu-id="acbaf-p113">Exchange Online PowerShell을 사용 하 여 비활성 사서함에 있는 소송 보존의 보존 기간을 변경 하는 방법은 다음과 같습니다. EAC는 사용할 수 없습니다. 다음 명령을 실행 하 여 보존 기간을 변경 합니다. 이 예에서는 보존 기간이 무제한으로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p113">Here's how to use Exchange Online PowerShell to change the hold duration for a Litigation Hold that is placed on an inactive mailbox. You can't use the EAC. Run the following command to change the hold duration. In this example, the hold duration is changed to an unlimited period of time.</span></span>
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldDuration unlimited
```

<span data-ttu-id="acbaf-179">따라서 비활성 사서함의 항목은 무기한 보존 되거나 보존 기간이 다른 값으로 변경 될 때까지 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-179">The result is that items in the inactive mailbox are retained indefinitely or until the hold is removed or the hold duration is changed to a different value.</span></span>
  
> [!TIP]
> <span data-ttu-id="acbaf-p114">비활성 사서함을 식별 하는 가장 좋은 방법은 해당 **고유 이름이** 나 **Exchange GUID** 값을 사용 하는 것입니다. 이러한 값 중 하나를 사용 하면 실수로 잘못 된 사서함을 지정 하는 것을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p114">The best way to identify an inactive mailbox is by using its **Distinguished Name** or **Exchange GUID** value. Using one of these values helps prevent accidentally specifying the wrong mailbox.</span></span> 
  
### <a name="change-the-duration-for-an-in-place-hold"></a><span data-ttu-id="acbaf-182">원본 위치 유지 기간 변경</span><span class="sxs-lookup"><span data-stu-id="acbaf-182">Change the duration for an In-Place Hold</span></span>

 <span data-ttu-id="acbaf-183">EAC 또는 Exchange Online PowerShell을 사용 하 여 원본 위치 유지에 대 한 보존 기간을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-183">You can use the EAC or Exchange Online PowerShell to change the hold duration for an In-Place Hold.</span></span> 
  
#### <a name="use-the-eac-to-change-the-hold-duration"></a><span data-ttu-id="acbaf-184">EAC를 사용 하 여 보존 기간 변경</span><span class="sxs-lookup"><span data-stu-id="acbaf-184">Use the EAC to change the hold duration</span></span>

1. <span data-ttu-id="acbaf-p115">변경할 원본 위치 유지의 이름을 알고 있는 경우 다음 단계로 이동 합니다. 그렇지 않으면 다음 명령을 실행 하 여 비활성 사서함에 배치 된 원본 위치 유지의 이름을 가져옵니다. [1 단계](#step-1-identify-the-holds-on-an-inactive-mailbox)에서 구한 원본 위치 유지 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p115">If you know the name of the In-Place Hold that you want to change, go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. <span data-ttu-id="acbaf-188">EAC에서 **규정 준수 관리** \> 원본 \*\* &amp; 위치 eDiscovery 유지\*\*로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-188">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
3. <span data-ttu-id="acbaf-189">변경 하려는 원본 위치 유지를 선택 하 고 편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) **편집** ![을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-189">Select the In-Place Hold you want to change, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
4. <span data-ttu-id="acbaf-190">원본 **위치 eDiscovery &amp; 보류** 속성 페이지에서 원본 **위치 유지**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-190">On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**.</span></span> 
    
5. <span data-ttu-id="acbaf-191">현재 보존 기간에 따라 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-191">Do one of the following based on the current hold duration:</span></span>
    
1. <span data-ttu-id="acbaf-192">**무기한 보존** 을 클릭 하 여 항목을 무제한으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-192">Click **Hold indefinitely** to hold items for an unlimited period of time.</span></span> 
    
2. <span data-ttu-id="acbaf-p116">특정 기간에 대 한 항목을 포함 하도록 **받은 날짜를 기준으로 항목을 보관할 일 수 지정** 을 클릭 합니다. 항목을 보유할 일 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p116">Click **Specify number of days to hold items relative to their received date** to hold items for a specific period. Type the number of days that you want to hold items for.</span></span> 
    
    ![원본 위치 유지 기간을 변경하는 작업의 스크린샷입니다.](media/cfcfd92a-9d65-40c0-90ef-ab72697b0166.png)
  
6. <span data-ttu-id="acbaf-196">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-196">Click **Save**.</span></span>
    
#### <a name="use-exchange-online-powershell-to-change-the-hold-duration"></a><span data-ttu-id="acbaf-197">Exchange Online PowerShell을 사용 하 여 보존 기간 변경</span><span class="sxs-lookup"><span data-stu-id="acbaf-197">Use Exchange Online PowerShell to change the hold duration</span></span>

1. <span data-ttu-id="acbaf-p117">변경할 원본 위치 유지의 이름을 알고 있는 경우 다음 단계로 이동 합니다. 그렇지 않으면 다음 명령을 실행 하 여 비활성 사서함에 배치 된 원본 위치 유지의 이름을 가져옵니다. [1 단계](#step-1-identify-the-holds-on-an-inactive-mailbox)에서 구한 원본 위치 유지 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p117">If you know the name of the In-Place Hold that you want to change, go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. <span data-ttu-id="acbaf-p118">다음 명령을 실행 하 여 보존 기간을 변경 합니다. 이 예에서는 보존 기간이 2555 일 (약 7 년)으로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p118">Run the following command to change the hold duration. In this example, the hold duration is changed to 2,555 days (approximately 7 years).</span></span> 
    
    ```
    Set-MailboxSearch <identity of In-Place Hold> -ItemHoldPeriod 2555
    ```

     <span data-ttu-id="acbaf-203">보류 시간을 무제한으로 변경 하려면 _-ItemHoldPeriod 무제한적_을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-203">To change the hold duration to an unlimited period of time, use  _-ItemHoldPeriod unlimited_.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="acbaf-204">추가 정보</span><span class="sxs-lookup"><span data-stu-id="acbaf-204">More information</span></span>

- <span data-ttu-id="acbaf-p119">**비활성 사서함의 항목에 대해 보존 기간을 계산 하는 방법** 기간은 사서함 항목을 받거나 만든 원래 날짜부터 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p119">**How is the hold duration calculated for an item in an inactive mailbox?** The duration is calculated from the original date a mailbox item was received or created.</span></span> 
    
- <span data-ttu-id="acbaf-p120">**보존 기간이 만료 되 면 어떻게 됩니까?** 복구 가능한 항목 폴더의 사서함 항목에 대해 보존 기간이 만료 되 면 해당 항목이 비활성 사서함에서 영구적으로 삭제 (제거) 됩니다. 비활성 사서함에 대 한 보존 기간을 지정 하지 않은 경우에는 복구 가능한 항목 폴더의 항목은 제거 되지 않습니다 (비활성 사서함의 보존 기간이 변경 되지 않은 경우).</span><span class="sxs-lookup"><span data-stu-id="acbaf-p120">**What happens when the hold duration expires?** When the hold duration expires for a mailbox item in the Recoverable Items folder, the item is permanently deleted (purged) from the inactive mailbox. If there is no duration specified for the hold placed on the inactive mailbox, items in the Recoverable Items folder are never purged (unless the hold duration for the inactive mailbox is changed).</span></span> 
    
- <span data-ttu-id="acbaf-p121">**비활성 사서함에서 Exchange 보존 정책이 여전히 처리 되 고 있습니까?** 사용 하지 않을 때 exchange 보존 정책 (메시징 레코드 관리 또는 mrm, exchange Online 기능)을 사서함에 적용 한 경우 **삭제** 보존 작업을 사용 하 여 구성 된 보존 태그에 해당 하는 삭제 정책이 비활성 사서함에서 계속 처리 됩니다. 즉, 삭제 정책을 사용 하 여 태그가 지정 된 항목은 보존 기간이 만료 될 때 복구 가능한 항목 폴더로 이동 됩니다. 그런 다음 항목의 보존 기간이 만료 되 면 해당 항목이 비활성 사서함에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p121">**Is an Exchange retention policy still processed on inactive mailboxes?** If an Exchange retention policy (the messaging records management, or MRM, feature in Exchange Online) was applied to a mailbox when it was made inactive, the deletion policies (which are retention tags configured with a **Delete** retention action) will continue to be processed on the inactive mailbox. That means items that are tagged with a deletion policy are moved to the Recoverable Items folder when the retention period expires. Those items are then purged from the inactive mailbox when the hold duration for an item expires.</span></span> 
    
    <span data-ttu-id="acbaf-p122">반대로 비활성 사서함에 할당 된 보존 정책에 포함 된 모든 보관 정책 ( **MoveToArchive** 보존 작업으로 구성 된 보존 태그)은 무시 됩니다. 즉, 보존 기간이 만료 되 면 보관 정책으로 태그가 지정 된 비활성 사서함의 항목이 기본 사서함에 남아 있습니다. 보관 사서함 이나 보관 사서함의 복구 가능한 항목 폴더로 이동 되지 않습니다. 사용자가 비활성 사서함에 로그인 할 수 없기 때문에 보관 정책을 처리 하기 위해 데이터 센터 리소스를 사용 해야 하는 이유는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p122">Conversely, any archive policies (which are retention tags configured with a **MoveToArchive** retention action) that are included in the retention policy assigned to an inactive mailbox are ignored. That means items in an inactive mailbox that are tagged with an archive policy remain in the primary mailbox when the retention period expires. They're not moved to the archive mailbox or to the Recoverable Items folder in the archive mailbox. Because a user can't sign in to an inactive mailbox, there's no reason to consume datacenter resources to process archive policies.</span></span> 
    
- <span data-ttu-id="acbaf-p123">**새로 보존 기간을 확인 하려면 다음 명령 중 하나를 실행 합니다.** 첫 번째 명령은 소송 보존에 대 한 것입니다. 두 번째는 원본 위치 유지를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p123">**To check the new hold duration, run one of the following commands.** The first command is for Litigation Hold; the second is for In-Place Hold.</span></span> 

    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | FL LitigationHoldDuration
    ```

    ```
    Get-MailboxSearch <identity of In-Place Hold> | FL ItemHoldPeriod
    ```

- <span data-ttu-id="acbaf-p124">**일반 사서함 처럼 MFA (관리 되는 폴더 도우미)도 비활성 사서함을 처리 합니다.** Exchange Online에서 MFA는 사서함을 약 7 일 마다 처리 합니다. 비활성 사서함에 대 한 보존 기간을 변경한 후에는 **시작 managedfolderassistant** cmdlet을 사용 하 여 비활성 사서함에 대 한 새 보존 기간을 즉시 처리 하도록 시작할 수 있습니다. 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p124">**Like regular mailboxes, the Managed Folder Assistant (MFA) also processes inactive mailboxes.** In Exchange Online, the MFA processes mailboxes approximately once every 7 days. After you change the hold duration for an inactive mailbox, you can use the **Start-ManagedFolderAssistant** cmdlet to immediately start processing the new hold duration for the inactive mailbox. Run the following command.</span></span> 

    ```
    Start-ManagedFolderAssistant -InactiveMailbox <identity of inactive mailbox>
    ```
   
- <span data-ttu-id="acbaf-p125">**비활성 사서함에 많은 보존을 적용 하는 경우 보류 guid 중 일부가 표시 되지 않습니다.** 다음 명령을 실행 하 여 비활성 사서함에 저장 된 모든 보류 (소송 보존 제외)의 guid를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acbaf-p125">**If a lot of holds are placed on an inactive mailbox, not all of the hold GUIDs will be displayed.** You can run the following command to display the GUIDs for all holds (except Litigation Holds) that are placed on an inactive mailbox.</span></span> 
    
    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds
    ```
