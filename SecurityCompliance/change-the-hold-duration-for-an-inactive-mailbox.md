---
title: Office 365에서 비활성 사서함에 대 한 보존 기간 변경
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/29/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: bdee24ed-b8cf-4dd0-92ae-b86ec4661e6b
description: Office 365 사서함 비활성 이루어진 후 보류 또는 비활성 사서함에 할당 하는 Office 365 보존 정책의 기간을 변경할 수 있습니다. 보류 기간 폴더에 보관 된 복구 가능한 항목에 얼마나 오래 항목을 정의 합니다.
ms.openlocfilehash: 22bd9f9294b625a38d243f6235097d1aee437121
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533534"
---
# <a name="change-the-hold-duration-for-an-inactive-mailbox-in-office-365"></a><span data-ttu-id="3d5c6-104">Office 365에서 비활성 사서함에 대 한 보존 기간 변경</span><span class="sxs-lookup"><span data-stu-id="3d5c6-104">Change the hold duration for an inactive mailbox in Office 365</span></span>

<span data-ttu-id="3d5c6-p102">비활성 사서함을 사용 하 여가 자신이 조직을 떠난 후 이전 직원의 전자 메일을 유지 합니다. 사서함이 소송 보존, In-place Hold, Office 365 보존 정책 때 비활성화 또는 eDiscovery 사례와 관련 된 보류의 사서함에 배치 하 고 해당 하는 Office 365 사용자 계정의 삭제 됩니다. 비활성 사서함의 내용은 비활성 적용 되기 전에 사서함에 배치 된 보류의 기간에 대 한 보관 됩니다. 보류 기간 폴더에 보관 된 복구 가능한 항목에 얼마나 오래 항목을 정의 합니다. 복구 가능한 항목 폴더에 있는 항목에 대 한 보존 기간 만료 되 면 해당 항목은 영구적으로 삭제 (비우기) 비활성 사서함에서. 사서함 비활성 이루어진 후 보류 또는 비활성 사서함에 할당 하는 Office 365 보존 정책의 기간을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p102">An inactive mailbox is used to retain a former employee's email after he or she leaves your organization. A mailbox becomes inactive when a Litigation Hold, an In-Place Hold, an Office 365 retention policy, or a hold that's associated with an eDiscovery case is placed on the mailbox, and the corresponding Office 365 user account is deleted. The contents of an inactive mailbox are retained for the duration of the hold that was placed on the mailbox before it was made inactive. The hold duration defines how long items in the Recoverable Items folder are held. When the hold duration expires for an item in the Recoverable Items folder, the item is permanently deleted (purged) from the inactive mailbox. After a mailbox is made inactive, you can change the duration of the hold or Office 365 retention policy assigned to the inactive mailbox.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="3d5c6-p103">사서함을 비활성화하기 위해 새 원본 위치 유지를 만들 수 있는 2017년 7월 1일 마감 날짜를 연기했습니다. 하지만 올해 말이나 내년 초에는 Exchange Online에 새 원본 위치 유지를 만들 수 없습니다. 그때는 소송 보존과 Office 365 보존 정책만 사용하여 비활성화 사서함을 만들 수 있습니다. 그러나 원본 위치 유지에 있는 기존 비활성화 사서함은 계속 지원되며 비활성화 사서함에서 원본 위치 유지를 계속 관리할 수 있습니다. 관리 항목으로는 원본 위치 유지 기간 변경 및 원본 위치 유지를 삭제하여 비활성화 사서함을 영구 삭제하는 작업이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds to make a mailbox inactive. But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. At that time, only Litigation Holds and Office 365 retention policies can be used to create an inactive mailbox. However, existing inactive mailboxes that are on In-Place Hold will still be supported, and you can continue to manage the In-Place Holds on inactive mailboxes. This includes changing the duration of an In-Place Hold and permanently deleting an inactive mailbox by removing the In-Place Hold.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="3d5c6-116">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="3d5c6-116">Before you begin</span></span>

- <span data-ttu-id="3d5c6-p104">비활성 사서함에 소송 보존에 대 한 보존 기간을 변경 하려면 Exchange Online PowerShell을 사용 해야 합니다. Exchange 관리 센터 (EAC)를 사용할 수 없습니다. 하지만 유지 하는 위치에 대 한 보존 기간을 변경 하려면 Exchange Online PowerShell 또는 EAC를 사용할 수 있습니다. Office 365 보안을 사용 하 여 수 &amp; 준수 센터 또는 보안 &amp; 는 Office 365 보존 정책에 대 한 보존 기간을 변경 하려면 준수 센터 PowerShell 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p104">You have to use Exchange Online PowerShell to change the hold duration for a Litigation Hold on an inactive mailbox. You can't use the Exchange admin center (EAC). But you can use Exchange Online PowerShell or the EAC to change the hold duration for an In-Place Hold. You can use the Office 365 Security &amp; Compliance Center or the Security &amp; Compliance Center PowerShell to change the hold duration for an Office 365 retention policy.</span></span>
    
- <span data-ttu-id="3d5c6-121">Exchange Online PowerShell 또는 보안 연결을 &amp; 준수 센터 PowerShell, 다음 항목 중 하나를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-121">To connect to Exchange Online PowerShell or Security &amp; Compliance Center PowerShell, see one of the following topics:</span></span>
    
  - [<span data-ttu-id="3d5c6-122">원격 PowerShell을 사용하여 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="3d5c6-122">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
  - [<span data-ttu-id="3d5c6-123">Office 365 보안 연결할 &amp; 준수 센터 PowerShell</span><span class="sxs-lookup"><span data-stu-id="3d5c6-123">Connect to Office 365 Security &amp; Compliance Center PowerShell</span></span>](https://go.microsoft.com/fwlink/?linkid=799771)
    
- <span data-ttu-id="3d5c6-p105">EDiscovery 사례와 관련 된 메모를 포함 하는 변경할 수 있는 보존 기간이 없는 것을 의미 하는 무한 보존 됩니다. 항목 보류에서 제거 되 고 비활성 사서함 삭제 될 때까지 또는 무제한 보관 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p105">Note that holds associated with eDiscovery cases are infinite holds, which means there is no hold duration that can be changed. Items are held forever or until the hold is removed and the inactive mailbox is deleted.</span></span>
    
- <span data-ttu-id="3d5c6-126">비활성 사서함에 대 한 자세한 내용은 [Office 365에서 비활성 사서함](inactive-mailboxes-in-office-365.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-126">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a><span data-ttu-id="3d5c6-127">1 단계: 비활성 사서함에서 보류를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-127">Step 1: Identify the holds on an inactive mailbox</span></span>

<span data-ttu-id="3d5c6-128">다양 한 유형의 보류 또는 하나 이상의 Office 365 보존 정책을 비활성 사서함에 배치 될 수 있습니다, 때문에 비활성 사서함에서 보류를 식별 하는 첫번째 단계가입니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-128">Because different types of holds or one or more Office 365 retention policies might be placed on an inactive mailbox, the first step is to identify the holds on an inactive mailbox.</span></span>
  
<span data-ttu-id="3d5c6-129">다음 명령을 실행 Exchange Online 조직에서 모든 비활성 사서함에 대 한 보류 정보를 표시 하는 PowerShell 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-129">Run the following command in Exchange Online PowerShell to display the hold information for all inactive mailboxes in your organization.</span></span>
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,LitigationHoldDuration,InPlaceHolds
```
   
<span data-ttu-id="3d5c6-p106">**LitigationHoldEnabled** 속성에 대 한 값 **True** 소송 보존으로 설정에서 비활성 사서함 인지를 나타냅니다. EDiscovery 유지 원본 위치 유지 또는 Office 365 보존 정책 비활성 사서함에 배치 되는 경우 보류 또는 보존 정책에 대 한 GUID **InPlaceHolds** 속성에 대 한 값으로 표시 됩니다. 예 다음 5 비활성 사서함에 대 한 결과 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p106">The value of **True** for the **LitigationHoldEnabled** property indicates that the inactive mailbox is on Litigation Hold. If an In-Place Hold, eDiscovery hold, or Office 365 retention policy is placed on an inactive mailbox, a GUID for the hold or retention policy is displayed as the value for the **InPlaceHolds** property. For example, the following shows results for 5 inactive mailboxes.</span></span> 
  
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
   
<span data-ttu-id="3d5c6-133">다음 표에서 각 사서함을 비활성화 하려면 사용 된 다섯 개의 서로 다른 보류 형식을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-133">The following table identifies the five different hold types that were used to make each mailbox inactive.</span></span>
  
|<span data-ttu-id="3d5c6-134">**비활성 사서함**</span><span class="sxs-lookup"><span data-stu-id="3d5c6-134">**Inactive mailbox**</span></span>|<span data-ttu-id="3d5c6-135">**종류를 유지 합니다.**</span><span class="sxs-lookup"><span data-stu-id="3d5c6-135">**Hold type**</span></span>|<span data-ttu-id="3d5c6-136">**비활성 사서함에서 보류를 식별 하는 방법**</span><span class="sxs-lookup"><span data-stu-id="3d5c6-136">**How to identify the hold on the inactive mailbox**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3d5c6-137">Ann Beebe</span><span class="sxs-lookup"><span data-stu-id="3d5c6-137">Ann Beebe</span></span>  <br/> |<span data-ttu-id="3d5c6-138">소송 보존</span><span class="sxs-lookup"><span data-stu-id="3d5c6-138">Litigation Hold</span></span>  <br/> |<span data-ttu-id="3d5c6-139">*LitigationHoldEnabled* 속성이로 설정 된 `True`합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-139">The  *LitigationHoldEnabled*  property is set to  `True`.</span></span>  <br/> |
|<span data-ttu-id="3d5c6-140">Pilar Pinilla</span><span class="sxs-lookup"><span data-stu-id="3d5c6-140">Pilar Pinilla</span></span>  <br/> |<span data-ttu-id="3d5c6-141">원본 위치 유지</span><span class="sxs-lookup"><span data-stu-id="3d5c6-141">In-Place Hold</span></span>  <br/> |<span data-ttu-id="3d5c6-p107">*InPlaceHolds* 속성은 비활성 사서함에 배치 된 원본 위치 유지의 GUID를 포함 합니다. 이 In-place Hold ID를 접두사로 시작 되지 않으면 때문에 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p107">The  *InPlaceHolds*  property contains the GUID of the In-Place Hold that's placed on the inactive mailbox. You can tell this is an In-Place Hold because the ID doesn't start with a prefix.  </span></span><br/> <span data-ttu-id="3d5c6-144">사용할 수는 ' Get-mailboxsearch InPlaceHoldIdentity<hold GUID></span><span class="sxs-lookup"><span data-stu-id="3d5c6-144">You can use the  \`Get-MailboxSearch -InPlaceHoldIdentity <hold GUID></span></span> | <span data-ttu-id="3d5c6-145">FL' 비활성 사서함에서 원본 위치 유지 하는 방법에 대 한 정보를 얻을 수 있는 Exchange Online PowerShell에서 명령 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-145">FL\` command in Exchange Online PowerShell to get information about the In-Place Hold on the inactive mailbox.</span></span>  <br/> |
|<span data-ttu-id="3d5c6-146">Mario 씨 Necaise</span><span class="sxs-lookup"><span data-stu-id="3d5c6-146">Mario Necaise</span></span>  <br/> |<span data-ttu-id="3d5c6-147">보안에서 조직 전체의 Office 365 보존 정책 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="3d5c6-147">Organization-wide Office 365 retention policy in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="3d5c6-p108">*InPlaceHolds* 속성이 비어 있습니다. 이 하나 이상의 조직 차원의 또는 (Exchange 전체) Office 365 보존 정책 비활성 사서함에 적용 되는 것을 나타냅니다. 이 경우에 실행할 수 있습니다는 ' Get-organizationconfig</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p108">The  *InPlaceHolds*  property is empty. This indicates that one or more organization-wide or (Exchange-wide) Office 365 retention policy is applied to the inactive mailbox. In this case, you can run the  \`Get-OrganizationConfig</span></span> | <span data-ttu-id="3d5c6-151">Select-object-ExpandProperty InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies that are applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> <br/>To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.  <br/><br/> `Get RetentionCompliancePolicy<retention policy GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="3d5c6-151">Select-Object -ExpandProperty InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies that are applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> <br/>To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.  <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix></span></span> | <span data-ttu-id="3d5c6-152">FL 이름 '</span><span class="sxs-lookup"><span data-stu-id="3d5c6-152">FL Name\`</span></span><br/><br/>
|<span data-ttu-id="3d5c6-153">Carol Olson</span><span class="sxs-lookup"><span data-stu-id="3d5c6-153">Carol Olson</span></span>  <br/> |<span data-ttu-id="3d5c6-154">보안에서 office 365 보존 정책 &amp; 준수 센터 특정 사서함에 적용</span><span class="sxs-lookup"><span data-stu-id="3d5c6-154">Office 365 retention policy in the Security &amp; Compliance Center applied to specific mailboxes</span></span>  <br/> |<span data-ttu-id="3d5c6-p109">*InPlaceHolds* 속성은 비활성 사서함에 적용 되는 Office 365 보존 정책의 GUID가 포함 됩니다. 이 보존 정책으로 시작 하는 GUID 하기 때문에 특정 사서함에 적용 하는 것을 알 수 있습니다는 `mbx` 접두사입니다. 비활성 사서함에 적용 된 보존 정책의 GUID를 시작 하는 경우는 `skp` 접두사를 나타내는 것 비즈니스 대화에 대 한 보존 정책이 Skype에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p109">The  *InPlaceHolds*  property contains the GUID of the Office 365 retention policy that's applied to the inactive mailbox. You can tell this is a retention policy that applied to specific mailboxes because the GUID starts with the  `mbx` prefix. Note that if GUID of the retention policy applied to the inactive mailbox started with the  `skp` prefix, that would indicate that the retention policy is applied to Skype for Business conversations.  </span></span><br/><br/> <span data-ttu-id="3d5c6-158">비활성 사서함에 적용 되는 Office 365 identity 보존 정책, 보안에서 다음 명령을 실행 &amp; 준수 센터 PowerShell 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-158">To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.</span></span><br/><br/> <span data-ttu-id="3d5c6-159">' Get RetentionCompliancePolicy<retention policy GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="3d5c6-159">\`Get-RetentionCompliancePolicy <retention policy GUID without prefix></span></span> | <span data-ttu-id="3d5c6-160">FL 이름` <br/><br/>Be sure to remove the  `mbx` or  `skp'이 명령을 실행 하면 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-160">FL Name` <br/><br/>Be sure to remove the  `mbx` or  `skp\` prefix when you run this command.</span></span>  <br/> |
|<span data-ttu-id="3d5c6-161">Abraham McMahon</span><span class="sxs-lookup"><span data-stu-id="3d5c6-161">Abraham McMahon</span></span>  <br/> |<span data-ttu-id="3d5c6-162">eDiscovery 사례 유지 (영문) 보안 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="3d5c6-162">eDiscovery case hold in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="3d5c6-p110">*InPlaceHolds* 속성은 비활성 사서함에 배치 되는 eDiscovery 사례 보류의 GUID를 포함 합니다. 이런 현상이 발생 eDiscovery 사례 보류도 시작 하는 GUID를 알 수는 `UniH` 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p110">The  *InPlaceHolds*  property contains the GUID of the eDiscovery case hold that's placed on the inactive mailbox. You can tell this is an eDiscovery case hold because the GUID starts with the  `UniH` prefix.  </span></span><br/> <span data-ttu-id="3d5c6-p111">사용할 수 있습니다는 `Get-CaseHoldPolicy` 보안에서 cmdlet &amp; 준수 센터 PowerShell 보류 비활성 사서함에 연결 된 eDiscovery 사례에 대 한 정보를 얻을 수 있습니다. 명령을 실행할 수 등 ' Get CaseHoldPolicy<hold GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="3d5c6-p111">You can use the  `Get-CaseHoldPolicy` cmdlet in Security &amp; Compliance Center PowerShell to get information about the eDiscovery case that the hold on the inactive mailbox is associated with. For example, you can run the command  \`Get-CaseHoldPolicy <hold GUID without prefix></span></span> | <span data-ttu-id="3d5c6-167">FL 이름` to display the name of the case hold that's on the inactive mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the inactive mailbox is associated with, run the following commands.  <br/><br/> `$CaseHold Get CaseHoldPolicy = <hold GUID without prefix> `<br/><br/> `Get ComplianceCase $CaseHold.CaseId</span><span class="sxs-lookup"><span data-stu-id="3d5c6-167">FL Name` to display the name of the case hold that's on the inactive mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the inactive mailbox is associated with, run the following commands.  <br/><br/> `$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/> `Get-ComplianceCase $CaseHold.CaseId</span></span> | <span data-ttu-id="3d5c6-168">FL 이름 '</span><span class="sxs-lookup"><span data-stu-id="3d5c6-168">FL Name\`</span></span><br/><br/><br/> <span data-ttu-id="3d5c6-p112">**참고:** 비활성 사서함에 대 한을 포함 하 고 eDiscovery를 사용 하 여 하지 것이 좋습니다. 법적 문제와 관련 된 특정, 시간 제한이 사례를 위한 eDiscovery 사례 때문입니다. 특정 시점 법률 사례 아마도 종료 하 고 대/소문자와 관련 된 보류 제거 되 고 eDiscovery 사례 됩니다 (닫히거나 삭제). 실제로 비활성 사서함에 배치 되는 보류 eDiscovery 사례와 연결 하 고 보류가 이거나 eDiscovery 사례 닫히거나 삭제 하는 경우 비활성 사서함 영구적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p112">**Note:** We don't recommend using eDiscovery holds for inactive mailboxes. That's because eDiscovery cases are intended for specific, time-bound cases related to a legal issue. At some point, a legal case will probably end and the holds associated with the case will be removed and the eDiscovery case will be closed (or deleted). In fact, if a hold that's placed on an inactive mailbox is associated with an eDiscovery case, and the hold is released or the eDiscovery case is closed or deleted, the inactive mailbox will be permanently deleted.</span></span> 

<span data-ttu-id="3d5c6-173">Office 365 보존 정책에 대 한 자세한 내용은 [보존 정책 개요](retention-policies.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-173">For more information about Office 365 retention policies, see [Overview of retention policies](retention-policies.md).</span></span>
  
## <a name="step-2-change-the-hold-duration-for-an-inactive-mailbox"></a><span data-ttu-id="3d5c6-174">비활성 사서함에 대 한 보존 기간을 변경 하는 2 단계:</span><span class="sxs-lookup"><span data-stu-id="3d5c6-174">Step 2: Change the hold duration for an inactive mailbox</span></span>

<span data-ttu-id="3d5c6-175">비활성 사서함에 어떤 유형의 보류 놓입니다 파악 한 후 (및 여러 보존 한지), 다음 단계를 보류에 대 한 기간을 변경 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-175">After you identify what type of hold is placed on the inactive mailbox (and whether there are multiple holds), the next step is to change the duration for the hold.</span></span> 
  
### <a name="change-the-duration-for-a-litigation-hold"></a><span data-ttu-id="3d5c6-176">소송 보존에 대 한 기간을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-176">Change the duration for a Litigation Hold</span></span>

<span data-ttu-id="3d5c6-p113">비활성 사서함에 배치 되는 소송 보존에 대 한 보존 기간을 변경 하려면 Exchange Online PowerShell을 사용 하는 방법을 다음과 같습니다. EAC를 사용할 수 없습니다. 보존 기간을 변경 하려면 다음 명령을 실행 합니다. 이 예제에서는 대기 기간 제한 없음된 기간으로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p113">Here's how to use Exchange Online PowerShell to change the hold duration for a Litigation Hold that is placed on an inactive mailbox. You can't use the EAC. Run the following command to change the hold duration. In this example, the hold duration is changed to an unlimited period of time.</span></span>
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldDuration unlimited
```

<span data-ttu-id="3d5c6-181">비활성 사서함의 항목은 무기한 또는 보존이 제거 되거나 보존 기간의 다른 값으로 변경 될 때까지 유지 되는 것이 반환이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-181">The result is that items in the inactive mailbox are retained indefinitely or until the hold is removed or the hold duration is changed to a different value.</span></span>
  
> [!TIP]
> <span data-ttu-id="3d5c6-p114">비활성 사서함을 식별 하는 가장 좋은 방법은 **고유 이름** 또는 **Exchange GUID** 값을 사용 하 여 됩니다. 이러한 값 중 하나를 사용 하 여 실수로 잘못 된 사서함을 지정 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p114">The best way to identify an inactive mailbox is by using its **Distinguished Name** or **Exchange GUID** value. Using one of these values helps prevent accidentally specifying the wrong mailbox.</span></span> 
  
### <a name="change-the-duration-for-an-in-place-hold"></a><span data-ttu-id="3d5c6-184">원본 위치 유지 하는 것에 대 한 기간을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-184">Change the duration for an In-Place Hold</span></span>

 <span data-ttu-id="3d5c6-185">EAC 또는 Exchange Online PowerShell 유지 하는 위치에 대 한 보존 기간을 변경 하려면 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-185">You can use the EAC or Exchange Online PowerShell to change the hold duration for an In-Place Hold.</span></span> 
  
#### <a name="use-the-eac-to-change-the-hold-duration"></a><span data-ttu-id="3d5c6-186">EAC를 사용 하 여 보존 기간을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="3d5c6-186">Use the EAC to change the hold duration</span></span>

1. <span data-ttu-id="3d5c6-p115">이름을 변경 하려는 원본 위치 유지를 알고 있는 경우에 다음 단계로 이동 합니다. 그렇지 않은 경우 비활성 사서함에 배치 된 원본 위치 유지의 이름을 가져오려면 다음 명령을 실행 합니다. [1 단계에서](#step-1-identify-the-holds-on-an-inactive-mailbox)에서 구한는 원본 위치 유지 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p115">If you know the name of the In-Place Hold that you want to change, go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. <span data-ttu-id="3d5c6-190">EAC에서 **규정 준수 관리** 로 이동 \> **원본 위치 eDiscovery &amp; 유지**합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-190">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
3. <span data-ttu-id="3d5c6-191">변경 하려는 원본 위치 유지를 선택 하 고 **편집** 을 클릭 한 다음 ![편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-191">Select the In-Place Hold you want to change, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
4. <span data-ttu-id="3d5c6-192">**원본 위치 eDiscovery &amp; 유지** 속성 페이지에서 **원본 위치 유지**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-192">On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**.</span></span> 
    
5. <span data-ttu-id="3d5c6-193">기간을 유지 현재에 따라 다음 중 하나:</span><span class="sxs-lookup"><span data-stu-id="3d5c6-193">Do one of the following based on the current hold duration:</span></span>
    
1. <span data-ttu-id="3d5c6-194">무제한 기간에 대 한 항목을 보존 하려면 **무기한 유지** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-194">Click **Hold indefinitely** to hold items for an unlimited period of time.</span></span> 
    
2. <span data-ttu-id="3d5c6-p116">특정 기간에 대 한 항목을 유지 하려면 **자신의 받은 날짜를 기준으로 항목을 보관할 일 번호 지정** 클릭 합니다. 항목에 대 한 유지 하려는 일 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p116">Click **Specify number of days to hold items relative to their received date** to hold items for a specific period. Type the number of days that you want to hold items for.</span></span> 
    
    ![원본 위치 유지 기간을 변경하는 작업의 스크린샷입니다.](media/cfcfd92a-9d65-40c0-90ef-ab72697b0166.png)
  
6. <span data-ttu-id="3d5c6-198">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-198">Click **Save**.</span></span>
    
#### <a name="use-exchange-online-powershell-to-change-the-hold-duration"></a><span data-ttu-id="3d5c6-199">Exchange Online PowerShell을 사용 하 여 보존 기간을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="3d5c6-199">Use Exchange Online PowerShell to change the hold duration</span></span>

1. <span data-ttu-id="3d5c6-p117">이름을 변경 하려는 원본 위치 유지를 알고 있는 경우에 다음 단계로 이동 합니다. 그렇지 않은 경우 비활성 사서함에 배치 된 원본 위치 유지의 이름을 가져오려면 다음 명령을 실행 합니다. [1 단계에서](#step-1-identify-the-holds-on-an-inactive-mailbox)에서 구한는 원본 위치 유지 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p117">If you know the name of the In-Place Hold that you want to change, go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. <span data-ttu-id="3d5c6-p118">보존 기간을 변경 하려면 다음 명령을 실행 합니다. 이 예제에서는 대기 기간 2,555 일 (약 7 년)로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p118">Run the following command to change the hold duration. In this example, the hold duration is changed to 2,555 days (approximately 7 years).</span></span> 
    
    ```
    Set-MailboxSearch <identity of In-Place Hold> -ItemHoldPeriod 2555
    ```

     <span data-ttu-id="3d5c6-205">보존 기간 제한 없음된 기간을 변경 하려면 _-ItemHoldPeriod 무제한으로_사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-205">To change the hold duration to an unlimited period of time, use  _-ItemHoldPeriod unlimited_.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="3d5c6-206">추가 정보</span><span class="sxs-lookup"><span data-stu-id="3d5c6-206">More information</span></span>

- <span data-ttu-id="3d5c6-p119">**비활성 사서함에 있는 항목에 대 한 보존 기간 계산 방법?** 사서함 항목을 받거나 만든 원래 날짜에서 기간 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p119">**How is the hold duration calculated for an item in an inactive mailbox?** The duration is calculated from the original date a mailbox item was received or created.</span></span> 
    
- <span data-ttu-id="3d5c6-p120">**보존 기간이 만료 될 때 수행 하는 작업?** 복구 가능한 항목 폴더에서 사서함 항목에 대 한 보존 기간 만료 되 면 해당 항목은 영구적으로 삭제 (비우기) 비활성 사서함에서. 비활성 사서함에 배치 보류에 대해 지정 된 기간이 있으면 복구 가능한 항목 폴더의 항목 (하지 않는 경우 비활성 사서함에 대 한 보존 기간 변경 된) 되지 비워집니다 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p120">**What happens when the hold duration expires?** When the hold duration expires for a mailbox item in the Recoverable Items folder, the item is permanently deleted (purged) from the inactive mailbox. If there is no duration specified for the hold placed on the inactive mailbox, items in the Recoverable Items folder are never purged (unless the hold duration for the inactive mailbox is changed).</span></span> 
    
- <span data-ttu-id="3d5c6-p121">**은 비활성 사서함에서 아직 처리 하는 Exchange 보존 정책?** (인, 보존 태그를 **삭제** 하는 보존 작업을 사용 하 여 구성) 삭제 정책 됩니다 (의 메시징 레코드 관리 또는 MRM, Exchange Online의 기능)는 Exchange 보존 정책 비활성 이었습니다 때 사서함에 적용 된, 하는 경우 비활성 사서함에서 처리를 계속 합니다. 즉, 보존 기간이 만료 될 때 삭제 정책을 사용 하 여 태그가 지정 된 항목을 복구 가능한 항목 폴더를 이동 됩니다. 이러한 항목 항목에 대 한 보존 기간이 만료 될 때 다음 비활성 사서함에서 비워집니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p121">**Is an Exchange retention policy still processed on inactive mailboxes?** If an Exchange retention policy (the messaging records management, or MRM, feature in Exchange Online) was applied to a mailbox when it was made inactive, the deletion policies (which are retention tags configured with a **Delete** retention action) will continue to be processed on the inactive mailbox. That means items that are tagged with a deletion policy are moved to the Recoverable Items folder when the retention period expires. Those items are then purged from the inactive mailbox when the hold duration for an item expires.</span></span> 
    
    <span data-ttu-id="3d5c6-p122">이와 반대로 비활성 사서함에 할당 된 보존 정책에 포함 된 모든 보관 정책 (인, **보관 폴더로 이동** 보존 작업을 사용 하 여 구성 하는 보존 태그)은 무시 됩니다. 즉, 보존 기간이 만료 되는 기본 사서함에 남아 있을 하는 보관 정책을 사용 하 여 태그가 지정 된 비활성 사서함의 항목입니다. 보관 사서함으로 또는 보관 사서함의 복구 가능한 항목 폴더를 이동 하지는 합니다. 사용자는 비활성 사서함에 로그인 할 수 없습니다 되므로 보관 정책을 처리를 데이터 센터 리소스를 사용할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p122">Conversely, any archive policies (which are retention tags configured with a **MoveToArchive** retention action) that are included in the retention policy assigned to an inactive mailbox are ignored. That means items in an inactive mailbox that are tagged with an archive policy remain in the primary mailbox when the retention period expires. They're not moved to the archive mailbox or to the Recoverable Items folder in the archive mailbox. Because a user can't sign in to an inactive mailbox, there's no reason to consume datacenter resources to process archive policies.</span></span> 
    
- <span data-ttu-id="3d5c6-p123">**새 보존 기간을 확인 하려면 다음 명령 중 하나를 실행 합니다.** 첫번째 명령은 소송 보존으로 설정 합니다. 두번째 사용자 계정의 원본 위치 유지입니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p123">**To check the new hold duration, run one of the following commands.** The first command is for Litigation Hold; the second is for In-Place Hold.</span></span> 

    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | FL LitigationHoldDuration
    ```

    ```
    Get-MailboxSearch <identity of In-Place Hold> | FL ItemHoldPeriod
    ```

- <span data-ttu-id="3d5c6-p124">**같은 일반 사서함의 관리 되는 폴더 도우미 (MFA)도 비활성 사서함 처리.** Exchange Online에서 7 일 마다 한번씩 약 MFA는이 사서함을 처리합니다. 비활성 사서함에 대 한 보존 기간을 변경한 후에 즉시 처리를 시작 하려면 비활성 사서함에 대 한 새 보존 기간의 **Start-managedfolderassistant** cmdlet을 사용할 수 있습니다. 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p124">**Like regular mailboxes, the Managed Folder Assistant (MFA) also processes inactive mailboxes.** In Exchange Online, the MFA processes mailboxes approximately once every 7 days. After you change the hold duration for an inactive mailbox, you can use the **Start-ManagedFolderAssistant** cmdlet to immediately start processing the new hold duration for the inactive mailbox. Run the following command.</span></span> 

    ```
    Start-ManagedFolderAssistant -InactiveMailbox <identity of inactive mailbox>
    ```
   
- <span data-ttu-id="3d5c6-p125">**보류 많은 guid가 표시 되는 보류 중 일부만 비활성 사서함에 배치 되는 경우.** 비활성 사서함에 배치 되는 (소송 보존을 포함 하 고)를 제외한 모든 보류에 대 한 Guid를 표시 하려면 다음 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d5c6-p125">**If a lot of holds are placed on an inactive mailbox, not all of the hold GUIDs will be displayed.** You can run the following command to display the GUIDs for all holds (except Litigation Holds) that are placed on an inactive mailbox.</span></span> 
    
    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds
    ```
