---
title: Exchange Online 사서함의 보류 유형을 식별하는 방법
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6057daa8-6372-4e77-a636-7ea599a76128
description: Office 365 사서함에 저장할 수 있는 다양 한 유형의 보존을 식별 하는 방법에 대해 알아봅니다. 이러한 보류 유형에는 소송 보존, eDiscovery 보류 및 Office 365 보존 정책이 포함 됩니다. 사용자가 조직 차원의 보존 정책에서 제외 되었는지 여부도 확인할 수 있습니다.
ms.openlocfilehash: e0c1c54cedfc7494233f12f043bb6d033576eca8
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32253889"
---
# <a name="how-to-identify-the-type-of-hold-placed-on-an-exchange-online-mailbox"></a><span data-ttu-id="a3c0b-105">Exchange Online 사서함의 보류 유형을 식별하는 방법</span><span class="sxs-lookup"><span data-stu-id="a3c0b-105">How to identify the type of hold placed on an Exchange Online mailbox</span></span>

<span data-ttu-id="a3c0b-106">이 문서에서는 Office 365에서 Exchange Online 사서함에 적용 되는 보류를 확인 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-106">This article explains how to identify holds placed on Exchange Online mailboxes in Office 365.</span></span>

<span data-ttu-id="a3c0b-107">Office 365에서는 조직에서 사서함 콘텐츠가 영구적으로 삭제 되지 않도록 하는 여러 가지 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-107">Office 365 offers a number of ways that your organization can prevent mailbox content from being permanently deleted.</span></span> <span data-ttu-id="a3c0b-108">이를 통해 조직은 준수 regulars을 충족 하거나 법률 또는 기타 조사 유형에 따라 콘텐츠를 보존할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-108">This allows your organization to retain content to meet compliance regulars or for the duration of legal or other types of investigations.</span></span> <span data-ttu-id="a3c0b-109">다음은 Office 365에서 보존 기능 ( *보류*라고도 함)의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-109">Here's a list of the retention features (also called *holds*) in Office 365:</span></span>

- <span data-ttu-id="a3c0b-110">**소송 보존** -Exchange Online의 사용자 사서함에 적용 되는 보존입니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-110">**Litigation Hold** - Holds that are applied to user mailboxes in Exchange Online.</span></span>

- <span data-ttu-id="a3c0b-111">**ediscovery 보류** -보안 및 준수 센터에서 eDiscovery 사례와 관련 된 보류입니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-111">**eDiscovery hold** - Holds that are associated with an eDiscovery case in the security and compliance center.</span></span> <span data-ttu-id="a3c0b-112">eDiscovery 보류는 사용자 사서함 및 해당 하는 Office 365 그룹 및 Microsoft 팀의 해당 사서함에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-112">eDiscovery holds can be applied to user mailboxes, and on the corresponding mailbox for Office 365 Groups and Microsoft Teams.</span></span>

- <span data-ttu-id="a3c0b-113">원본 **위치 유지** -exchange Online의 exchange 관리 센터에서 원본 위치 eDiscovery & 보존 도구를 사용 하 여 사용자 사서함에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-113">**In-Place Hold** - Holds that are applied to user mailboxes by using the In-Place eDiscovery & Hold tool in the Exchange admin center in Exchange Online.</span></span>

- <span data-ttu-id="a3c0b-114">**office 365 보존 정책** -Exchange Online의 사용자 사서함과 Office 365 그룹 및 Microsoft 팀의 해당 사서함에 있는 콘텐츠를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-114">**Office 365 retention policy** - Retains content in user mailboxes in Exchange Online and in the corresponding mailbox for Office 365 Groups and Microsoft Teams.</span></span> <span data-ttu-id="a3c0b-115">사용자 사서함에 저장 되는 비즈니스용 Skype 대화를 보관 하는 보존 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-115">You can create a retention policy retains Skype for Business Conversations, which are stored in user mailboxes.</span></span>

  <span data-ttu-id="a3c0b-116">사서함에 할당할 수 있는 Office 365 보존 정책에는 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-116">There are two types of Office 365 retention policies that can be assigned to mailboxes.</span></span>

    - <span data-ttu-id="a3c0b-117">**특정 위치 보존 정책** -특정 사용자의 콘텐츠 위치에 할당 되는 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-117">**Specific location retention policies** - These are policies that are assigned to the content locations of specific users.</span></span> <span data-ttu-id="a3c0b-118">Exchange Online PowerShell의 **Get-Mailbox** cmdlet을 사용 하 여 특정 사서함에 할당 된 보존 정책에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-118">You use the **Get-Mailbox** cmdlet in Exchange Online PowerShell to get information about retention policies assigned to specific mailboxes.</span></span>

    - <span data-ttu-id="a3c0b-119">**조직 전체 보존 정책** -조직의 모든 콘텐츠 위치에 할당 되는 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-119">**Organization-wide retention policies** - These are policies that are assigned to all content locations in your organization.</span></span> <span data-ttu-id="a3c0b-120">Exchange Online PowerShell에서 **set-organizationconfig** cmdlet을 사용 하 여 조직 차원의 보존 정책에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-120">You use the **Get-OrganizationConfig** cmdlet in Exchange Online PowerShell to get information about organization-wide retention policies.</span></span>
  <span data-ttu-id="a3c0b-121">자세한 내용은 [Overview the Office 365 보존 정책 개요](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations)의 "전체 조직이 나 특정 위치에 보존 정책 적용" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-121">For more information, see the "Applying a retention policy to an entire organization or specific locations" section in [Overview of Office 365 retention policies](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).</span></span>

- <span data-ttu-id="a3c0b-122">**office 365 보존 레이블** -사용자가 Office 365 보존 레이블 (콘텐츠를 보존 하 고 유지 한 다음 콘텐츠를 보존 하 고 사서함의 항목에 저장 \*\* )을 적용 하는 경우 사서함이 있는 것 처럼 사서함에 보류가 설정 됩니다. 소송 보존 또는 Office 365 유지 정책에 할당 된 위치</span><span class="sxs-lookup"><span data-stu-id="a3c0b-122">**Office 365 retention labels** - If a user applies an Office 365 retention label (one that's configured to retain content or retain and then delete content) to *any* folder or item in their mailbox, a hold is placed on the mailbox just as if the mailbox was placed on Litigation Hold or assigned to an Office 365 retention policy.</span></span> <span data-ttu-id="a3c0b-123">자세한 내용은이 문서의 [폴더 또는 항목 섹션에 보존 레이블이 적용 되었기 때문에 보류 중인 사서함 확인](#identifying-mailboxes-on-hold-because-a-retention-label-has-been-applied-to-a-folder-or-item) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-123">For more information, see the [Identifying mailboxes on hold because a retention label has been applied to a folder or item](#identifying-mailboxes-on-hold-because-a-retention-label-has-been-applied-to-a-folder-or-item) section in this article.</span></span>

<span data-ttu-id="a3c0b-124">보류 중인 사서함을 관리 하려면 대기 시간 변경, 일시적으로 또는 영구 제거 또는 Office 365 보존 정책에서 사서함을 제외 하는 등의 작업을 수행할 수 있도록 사서함에 저장 된 보류 유형을 확인 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-124">To manage mailboxes on hold, you may have to identify the type of hold that's placed on a mailbox so that you can perform tasks such as changing the hold duration, temporarily or permanently removing the hold, or excluding a mailbox from a Office 365 retention policy.</span></span> <span data-ttu-id="a3c0b-125">이러한 경우 첫 번째 단계는 사서함에 적용 된 보류 유형을 식별 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-125">In these cases, the first step is to identify the type of hold placed on the mailbox.</span></span> <span data-ttu-id="a3c0b-126">또한 단일 사서함에 여러 보류 (및 서로 다른 형식 보존)을 적용할 수 있으므로 사서함에 저장 된 모든 보류를 확인 하 여 해당 보류를 제거 하거나 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-126">And because multiple holds (and different types of holds) can be placed on a single mailbox, you'll have to identify all holds placed on a mailbox if you want to remove or change those holds.</span></span>

## <a name="step-1-obtaining-the-guid-for-holds-placed-on-a-mailbox"></a><span data-ttu-id="a3c0b-127">1 단계: 사서함에 저장 된 보류의 GUID 가져오기</span><span class="sxs-lookup"><span data-stu-id="a3c0b-127">Step 1: Obtaining the GUID for holds placed on a mailbox</span></span>

<span data-ttu-id="a3c0b-128">Exchange Online PowerShell에서 다음 두 cmdlet을 실행 하 여 사서함에 저장 된 보류의 GUID를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-128">You can run the following two cmdlets in Exchange Online PowerShell to get the GUID of the holds that are placed on a mailbox.</span></span> <span data-ttu-id="a3c0b-129">GUID를 얻은 후에는이를 사용 하 여 2 단계에서 특정 보류를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-129">After you obtain a GUID, you use it to identify the specific hold in Step 2.</span></span> <span data-ttu-id="a3c0b-130">소송 보존은 GUID로 식별 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-130">Note that Litigation Holds are not identified by a GUID.</span></span> <span data-ttu-id="a3c0b-131">소송 보존은 사서함에 대해 사용 하거나 사용 하지 않도록 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-131">Litigation Holds are either enabled or disabled for a mailbox.</span></span>

- <span data-ttu-id="a3c0b-132">**Get-mailbox** -이 cmdlet을 사용 하 여 사서함에 대해 소송 보존을 사용 하도록 설정 했는지 여부를 확인 하 고, eDiscovery 보류에 대 한 guid, 원본 위치 유지 및 사서함에 특별히 할당 된 Office 365 보존 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-132">**Get-Mailbox** - Use this cmdlet to determine whether Litigation Hold is enabled for a mailbox and to get the GUIDs for eDiscovery holds, In-Place Holds, and Office 365 retention policies that are specifically assigned to a mailbox.</span></span> <span data-ttu-id="a3c0b-133">이 cmdlet의 출력은 사서함이 조직 차원의 보존 정책에서 명시적으로 제외 되었는지 여부도 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-133">The output of this cmdlet will also indicate if a mailbox has been explicitly excluded from an organization-wide retention policy.</span></span>

- <span data-ttu-id="a3c0b-134">**set-organizationconfig** -이 cmdlet을 사용 하 여 조직 전체 보존 정책의 guid를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-134">**Get-OrganizationConfig** - Use this cmdlet to get the GUIDs for organization-wide retention policies.</span></span>

<span data-ttu-id="a3c0b-135">Exchange Online PowerShell에 연결하려면 [Exchange Online PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-135">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>

### <a name="get-mailbox"></a><span data-ttu-id="a3c0b-136">Get-Mailbox</span><span class="sxs-lookup"><span data-stu-id="a3c0b-136">Get-Mailbox</span></span>

<span data-ttu-id="a3c0b-137">다음 명령을 실행 하 여 사서함에 적용 된 보류 및 Office 365 보존 정책에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-137">Run the following command to get information about the holds and Office 365 retention policies applied to a mailbox.</span></span>

```
Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
```

> [!TIP]
> <span data-ttu-id="a3c0b-138">InPlaceHolds 속성에 값이 너무 많고 이러한 속성이 모두 표시 되는 것은 아닌 경우 `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` 명령을 실행 하 여 각 GUID를 별도의 줄에 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-138">If there are too many values in the InPlaceHolds property and not all of them are displayed, you can run the `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` command to display each GUID on a separate line.</span></span>

<span data-ttu-id="a3c0b-139">다음 표에는 *InPlaceHolds* 속성의 값에 따라 **Get-Mailbox** cmdlet을 실행할 때의 서로 다른 유형의 보류를 식별 하는 방법에 대 한 설명이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-139">The following table describes how to identify different types of holds based on the values in the *InPlaceHolds* property when you run the **Get-Mailbox** cmdlet.</span></span>


|<span data-ttu-id="a3c0b-140">보류 유형</span><span class="sxs-lookup"><span data-stu-id="a3c0b-140">Hold type</span></span>  |<span data-ttu-id="a3c0b-141">예제 값</span><span class="sxs-lookup"><span data-stu-id="a3c0b-141">Example value</span></span>  |<span data-ttu-id="a3c0b-142">보류를 확인 하는 방법</span><span class="sxs-lookup"><span data-stu-id="a3c0b-142">How to identify the hold</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="a3c0b-143">소송 대기</span><span class="sxs-lookup"><span data-stu-id="a3c0b-143">Litigation Hold</span></span>     |    `True`     |     <span data-ttu-id="a3c0b-144">*LitigationHoldEnabled* 속성이로 `True`설정 된 경우 사서함에 대해 소송 보존을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-144">Litigation Hold is enabled for a mailbox if the *LitigationHoldEnabled* property is set to `True`.</span></span>    |
|<span data-ttu-id="a3c0b-145">eDiscovery 보류</span><span class="sxs-lookup"><span data-stu-id="a3c0b-145">eDiscovery hold</span></span>     |  `UniH7d895d48-7e23-4a8d-8346-533c3beac15d`       |   <span data-ttu-id="a3c0b-146">*InPlaceHolds 속성* 은 보안 및 준수 센터에서 eDiscovery 사례와 관련 된 보류의 GUID를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-146">The *InPlaceHolds property* contains the GUID of any hold associated with an eDiscovery case in the security and compliance center.</span></span> <span data-ttu-id="a3c0b-147">GUID는 `UniH` 접두사 (통합 보류 표시)로 시작 되므로 eDiscovery 보류 임을 알릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-147">You can tell this is an eDiscovery hold because the GUID starts with the `UniH` prefix (which denotes a Unified Hold).</span></span>      |
|<span data-ttu-id="a3c0b-148">원본 위치 유지</span><span class="sxs-lookup"><span data-stu-id="a3c0b-148">In-Place Hold</span></span>     |     `c0ba3ce811b6432a8751430937152491` <br/> <span data-ttu-id="a3c0b-149"> 선택하거나 </span><span class="sxs-lookup"><span data-stu-id="a3c0b-149">or</span></span> <br/> `cld9c0a984ca74b457fbe4504bf7d3e00de`  |     <span data-ttu-id="a3c0b-150">*InPlaceHolds* 속성은 사서함에 배치 된 원본 위치 유지의 GUID를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-150">The *InPlaceHolds* property contains the GUID of the In-Place Hold that's placed on the mailbox.</span></span> <span data-ttu-id="a3c0b-151">GUID가 접두사로 시작 하지 않거나 `cld` 접두사로 시작 하지 않으므로 원본 위치 유지로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-151">You can tell this is an In-Place Hold because the GUID either doesn't start with a prefix or it starts with the `cld` prefix.</span></span>     |
|<span data-ttu-id="a3c0b-152">Office 365 보존 정책이 특별히 사서함에 적용 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-152">Office 365 retention policy specifically applied to the mailbox</span></span>     |    `mbxcdbbb86ce60342489bff371876e7f224:1` <br/> <span data-ttu-id="a3c0b-153"> 선택하거나 </span><span class="sxs-lookup"><span data-stu-id="a3c0b-153">or</span></span> <br/> `skp127d7cf1076947929bf136b7a2a8c36f:3`     |     <span data-ttu-id="a3c0b-154">InPlaceHolds 속성은 사서함에 적용 된 특정 위치 보존 정책의 guid를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-154">The InPlaceHolds property contains GUIDs of any specific location retention policy that's applied to the mailbox.</span></span> <span data-ttu-id="a3c0b-155">GUID는 `mbx` 또는 `skp` 접두사로 시작 되므로 보존 정책을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-155">You can identify retention policies because the GUID starts with the `mbx` or the `skp` prefix.</span></span> <span data-ttu-id="a3c0b-156">접두사 `skp` 는 보존 정책이 사용자 사서함의 비즈니스용 Skype 대화에 적용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-156">The `skp` prefix indicates that the retention policy is applied to Skype for Business conversations in the user's mailbox.</span></span>    |
|<span data-ttu-id="a3c0b-157">조직 전체 Office 365 보존 정책에서 제외 됨</span><span class="sxs-lookup"><span data-stu-id="a3c0b-157">Excluded from an organization-wide Office 365 retention policy</span></span>     |   `-mbxe9b52bf7ab3b46a286308ecb29624696`      |     <span data-ttu-id="a3c0b-158">사서함이 조직 차원의 Office 365 보존 정책에서 제외 된 경우에는 사서함이 제외 된 보존 정책의 GUID가 InPlaceHolds 속성에 표시 되 고 `-mbx` 접두사로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-158">If a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy the mailbox is excluded from is displayed in the InPlaceHolds property and is identified by the `-mbx` prefix.</span></span>    |

### <a name="get-organizationconfig"></a><span data-ttu-id="a3c0b-159">set-organizationconfig</span><span class="sxs-lookup"><span data-stu-id="a3c0b-159">Get-OrganizationConfig</span></span>
<span data-ttu-id="a3c0b-160">**사서함** cmdlet을 실행할 때 *InPlaceHolds* 속성이 비어 있으면 여전히 사서함에 적용 되는 하나 이상의 조직 수준 Office 365 보존 정책이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-160">If the *InPlaceHolds* property is empty when you run the **Get-Mailbox** cmdlet, there still may be one or more organization-wide Office 365 retention policies applied to the mailbox.</span></span> <span data-ttu-id="a3c0b-161">Exchange Online PowerShell에서 다음 명령을 실행 하 여 조직 전반의 Office 365 보존 정책에 대 한 guid 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-161">Run the following command in Exchange Online PowerShell to get a list of GUIDs for organization-wide Office 365 retention policies.</span></span>

```
Get-OrganizationConfig | FL InPlaceHolds
```

> [!TIP]
> <span data-ttu-id="a3c0b-162">InPlaceHolds 속성에 값이 너무 많고 이러한 속성이 모두 표시 되는 것은 아닌 경우 `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` 명령을 실행 하 여 각 GUID를 별도의 줄에 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-162">If there are too many values in the InPlaceHolds property and not all of them are displayed, you can run the `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command to display each GUID on a separate line.</span></span>

<span data-ttu-id="a3c0b-163">다음 표에서는 여러 유형의 조직 차원의 보류와 **set-organizationconfig** cmdlet을 실행할 때 *InPlaceHolds* 속성에 포함 된 guid에 따라 각 형식을 식별 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-163">The following table describes the different types of organization-wide holds and how to identify each type based on the GUIDs contained in *InPlaceHolds* property when you run the **Get-OrganizationConfig** cmdlet.</span></span>


|<span data-ttu-id="a3c0b-164">보류 유형</span><span class="sxs-lookup"><span data-stu-id="a3c0b-164">Hold type</span></span>  |<span data-ttu-id="a3c0b-165">예제 값</span><span class="sxs-lookup"><span data-stu-id="a3c0b-165">Example value</span></span>  |<span data-ttu-id="a3c0b-166">설명</span><span class="sxs-lookup"><span data-stu-id="a3c0b-166">Description</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="a3c0b-167">exchange 사서함, exchange 공용 폴더 및 팀 대화방에 적용 되는 Office 365 보존 정책</span><span class="sxs-lookup"><span data-stu-id="a3c0b-167">Office 365 retention policies applied to Exchange mailboxes, Exchange public folders, and Teams chats</span></span>    |      `mbx7cfb30345d454ac0a989ab3041051209:2`   |   <span data-ttu-id="a3c0b-168">exchange 사서함, exchange 공용 폴더 및 1xn 채팅에 적용 되는 조직 차원의 보존 정책은 `mbx` 접두사를 사용 하 여 시작 되는 guid로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-168">Organization-wide retention policies applied to Exchange mailboxes, Exchange public folders, and 1xN chats in Microsoft Teams are identified by GUIDs that start with the `mbx` prefix.</span></span> <span data-ttu-id="a3c0b-169">1xn 채팅은 개별 채팅 참가자의 사서함에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-169">Note that 1xN chats are stored in the mailbox of the individual chat participants.</span></span>      |
|<span data-ttu-id="a3c0b-170">office 365 그룹 및 팀 채널 메시지에 적용 되는 office 365 보존 정책</span><span class="sxs-lookup"><span data-stu-id="a3c0b-170">Office 365 retention policy applied to Office 365 Groups and Teams channel messages</span></span>     |   `grp1a0a132ee8944501a4bb6a452ec31171:3`      |    <span data-ttu-id="a3c0b-171">Microsoft 팀의 Office 365 그룹 및 채널 메시지에 적용 되는 조직 차원의 보존 정책은 `grp` 접두사로 시작 되는 guid로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-171">Organization-wide retention policies applied to Office 365 groups and channel messages in Microsoft Teams are identified by GUIDs that start with the `grp` prefix.</span></span> <span data-ttu-id="a3c0b-172">채널 메시지는 Microsoft 팀과 연결 된 그룹 사서함에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-172">Note that channel messages are stored in the group mailbox that is associated with a Microsoft Team.</span></span>     |

<span data-ttu-id="a3c0b-173">Microsoft 팀에 적용 되는 자세한 정보 보존 정책은 "팀 위치" 섹션의 [보존 정책 개요](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-173">For more information retention policies applied to Microsoft Teams, see the "Teams location" section [Overview of retention policies](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).</span></span>

### <a name="understanding-the-format-of-the-inplaceholds-value-for-retention-policies"></a><span data-ttu-id="a3c0b-174">보존 정책에 대 한 InPlaceHolds 값의 형식 이해</span><span class="sxs-lookup"><span data-stu-id="a3c0b-174">Understanding the format of the InPlaceHolds value for retention policies</span></span>

<span data-ttu-id="a3c0b-175">InPlaceHolds 속성의 항목을 Office 365 보존 정책으로 식별 하는 접두사 (m b x, p 또는 grp) 외에,이 값에는 정책에 대해 구성 된 보존 작업 유형을 식별 하는 접미사도 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-175">In addition to the prefix (mbx, skp, or grp) that identifies an item in the InPlaceHolds property as an Office 365 retention policy, the value also contains a suffix that identifies the type of retention action that's configured for the policy.</span></span> <span data-ttu-id="a3c0b-176">예를 들어 다음 예제에서는 동작 접미사가 굵은 형식으로 강조 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-176">For example, the action suffix is highlighted in bold type in the following examples:</span></span>

   <span data-ttu-id="a3c0b-177">`skp127d7cf1076947929bf136b7a2a8c36f`**주파수**</span><span class="sxs-lookup"><span data-stu-id="a3c0b-177">`skp127d7cf1076947929bf136b7a2a8c36f`**:1**</span></span>

   <span data-ttu-id="a3c0b-178">`mbx7cfb30345d454ac0a989ab3041051209`**: 2**</span><span class="sxs-lookup"><span data-stu-id="a3c0b-178">`mbx7cfb30345d454ac0a989ab3041051209`**:2**</span></span>

   <span data-ttu-id="a3c0b-179">`grp1a0a132ee8944501a4bb6a452ec31171`**: 3**</span><span class="sxs-lookup"><span data-stu-id="a3c0b-179">`grp1a0a132ee8944501a4bb6a452ec31171`**:3**</span></span>

<span data-ttu-id="a3c0b-180">다음 표에서는 가능한 세 가지 보존 작업을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-180">The following table defines the three possible retention actions:</span></span>

|<span data-ttu-id="a3c0b-181">값</span><span class="sxs-lookup"><span data-stu-id="a3c0b-181">Value</span></span>  |<span data-ttu-id="a3c0b-182">설명</span><span class="sxs-lookup"><span data-stu-id="a3c0b-182">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="a3c0b-183">**개**</span><span class="sxs-lookup"><span data-stu-id="a3c0b-183">**1**</span></span>     | <span data-ttu-id="a3c0b-184">보존 정책이 항목을 삭제 하도록 구성 되어 있음을 나타냅니다. 정책은 항목을 보존 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-184">Indicates the retention policy is configured to delete items; the policy doesn't retain items.</span></span>        |
|<span data-ttu-id="a3c0b-185">**2**</span><span class="sxs-lookup"><span data-stu-id="a3c0b-185">**2**</span></span>    |    <span data-ttu-id="a3c0b-186">항목을 포함 하도록 보존 정책이 구성 되었음을 나타냅니다. 보존 기간이 만료 된 후에는 정책이 항목을 삭제 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-186">Indicates the retention policy is configured to hold items; the policy doesn't delete items after the retention period expires.</span></span>     |
|<span data-ttu-id="a3c0b-187">**3(sp3)**</span><span class="sxs-lookup"><span data-stu-id="a3c0b-187">**3**</span></span>     |   <span data-ttu-id="a3c0b-188">보존 정책이 항목을 보관 하도록 구성 되어 있음을 나타내고 보존 기간이 만료 되 면 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-188">Indicates the retention policy is configured to hold items and then delete them after the retention period expires.</span></span>      |

<span data-ttu-id="a3c0b-189">보존 작업에 대 한 자세한 내용은 [보존 정책 개요](retention-policies.md#retaining-content-for-a-specific-period-of-time)의 "특정 기간 동안 콘텐츠 보존" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-189">For more information about retention actions, see the "Retaining content for a specific period of time" section in [Overview of retention policies](retention-policies.md#retaining-content-for-a-specific-period-of-time).</span></span>
   
## <a name="step-2-using-the-guid-to-identify-the-hold"></a><span data-ttu-id="a3c0b-190">2 단계: GUID를 사용 하 여 보류 식별</span><span class="sxs-lookup"><span data-stu-id="a3c0b-190">Step 2: Using the GUID to identify the hold</span></span>

<span data-ttu-id="a3c0b-191">사서함에 적용 되는 보류에 대 한 guid를 얻은 후에는 해당 guid를 사용 하 여 보류를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-191">After you obtain the GUID for a hold that is applied to a mailbox, the next step is to use that GUID to identify the hold.</span></span> <span data-ttu-id="a3c0b-192">다음 섹션에서는 보류 GUID를 사용 하 여 보류 (및 기타 정보)의 이름을 식별 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-192">The following sections show how to identify the name of the hold (and other information) by using the hold GUID.</span></span>

### <a name="ediscovery-holds"></a><span data-ttu-id="a3c0b-193">eDiscovery 보류</span><span class="sxs-lookup"><span data-stu-id="a3c0b-193">eDiscovery holds</span></span>

<span data-ttu-id="a3c0b-194">Security & 준수 센터 PowerShell에서 다음 명령을 실행 하 여 사서함에 적용 된 eDiscovery 보존을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-194">Run the following commands in Security & Compliance Center PowerShell to identify an eDiscovery hold that's applied to the mailbox.</span></span> <span data-ttu-id="a3c0b-195">1 단계에서 확인 한 eDiscovery 보존에 대 한 GUID (a \* 접두사를 포함 하지 않음)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-195">Use the GUID (not including the UniH prefix) for the eDiscovery hold that you identified in Step 1.</span></span> <span data-ttu-id="a3c0b-196">첫 번째 명령은 보류에 대 한 정보가 포함 된 변수를 만듭니다. 이 변수는 다른 명령에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-196">The first command creates a variable that contains information about the hold; this variable is used in the other commands.</span></span> <span data-ttu-id="a3c0b-197">두 번째 명령은 보류가 연결 된 eDiscovery 사례의 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-197">The second command displays the name of the eDiscovery case the hold is associated with.</span></span> <span data-ttu-id="a3c0b-198">세 번째 명령은 보류의 이름과 보류가 적용 되는 사서함 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-198">The third command displays the name of the hold and a list of the mailboxes the hold applies to.</span></span>

```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold | FL Name,ExchangeLocation
```

<span data-ttu-id="a3c0b-199">보안 & 준수 센터 powershell에 연결 하려면 [connect to security & 준수 센터 powershell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-199">To connect to Security & Compliance Center PowerShell, see  [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

### <a name="in-place-holds"></a><span data-ttu-id="a3c0b-200">원본 위치 유지</span><span class="sxs-lookup"><span data-stu-id="a3c0b-200">In-Place Holds</span></span>

<span data-ttu-id="a3c0b-201">Exchange Online PowerShell에서 다음 명령을 실행 하 여 사서함에 적용 된 원본 위치 유지를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-201">Run the following command in Exchange Online PowerShell to identify the In-Place Hold that's applied to the mailbox.</span></span> <span data-ttu-id="a3c0b-202">1 단계에서 확인 한 원본 위치 유지에 대해 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-202">Use the GUID for the In-Place Hold that you identified in Step 1.</span></span> <span data-ttu-id="a3c0b-203">이 명령은 보류의 이름과 보류가 적용 되는 사서함 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-203">The command displays the name of the hold and a list of the mailboxes the hold applies to.</span></span>

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name,SourceMailboxes
```
<span data-ttu-id="a3c0b-204">원본 위치 유지의 GUID가 `cld` 접두사로 시작 되는 경우에는 이전 명령을 실행할 때 접두사를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-204">Note that if the GUID for the In-Place Hold starts with the `cld` prefix, be sure to include the prefix when running the previous command.</span></span>

### <a name="office-365-retention-policies"></a><span data-ttu-id="a3c0b-205">Office 365 보존 정책</span><span class="sxs-lookup"><span data-stu-id="a3c0b-205">Office 365 retention policies</span></span>

<span data-ttu-id="a3c0b-206">Security & 준수 센터 PowerShell에서 다음 명령을 실행 하 여 사서함에 적용 되는 Office 365 보존 정책 (조직 전체 또는 특정 위치)을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-206">Run the following command in Security & Compliance Center PowerShell to identity the Office 365 retention policy (organization-wide or specific location) that's applied to the mailbox.</span></span> <span data-ttu-id="a3c0b-207">1 단계에서 확인 한 GUID (m b x,로 p, 또는 grp 접두사 또는 작업 접미사는 포함 하지 않음)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-207">Use the GUID (not including the mbx, skp, or grp prefix or the action suffix) that you identified in Step 1.</span></span>

```
Get-RetentionCompliancePolicy <hold GUID without prefix or suffix> -DistributionDetail  | FL Name,*Location
```

## <a name="identifying-mailboxes-on-hold-because-a-retention-label-has-been-applied-to-a-folder-or-item"></a><span data-ttu-id="a3c0b-208">폴더 또는 항목에 보존 레이블이 적용 되었기 때문에 보류 중인 사서함 확인</span><span class="sxs-lookup"><span data-stu-id="a3c0b-208">Identifying mailboxes on hold because a retention label has been applied to a folder or item</span></span>

<span data-ttu-id="a3c0b-209">사용자가 콘텐츠를 보존 하도록 구성 된 보존 레이블을 적용 하거나 사서함의 모든 폴더 또는 항목에 대 한 콘텐츠를 삭제 하는 경우에는 *ComplianceTagHoldApplied* mailbox 속성을 **True**로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-209">Whenever a user applies a retention label that's configured to retain content or retain and then delete content to any folder or item in their mailbox, the *ComplianceTagHoldApplied* mailbox property is set to **True**.</span></span> <span data-ttu-id="a3c0b-210">이 문제가 발생 하는 경우 사서함은 소송 보존에 적용 된 것으로 간주 되거나 Office 365 보관 정책에 할당 되는 것 처럼 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-210">When this happens, the mailbox is considered to be on hold, just as if it was placed on Litigation Hold or assigned to an Office 365 retention policy.</span></span> <span data-ttu-id="a3c0b-211">*ComplianceTagHoldApplied* 속성을 **True**로 설정 하면 다음 작업이 수행 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-211">When the *ComplianceTagHoldApplied* property is set to **True**, the following things may occur:</span></span>

- <span data-ttu-id="a3c0b-212">사서함 이나 사용자의 Office 365 사용자 계정이 삭제 되 면 사서함이 [비활성 사서함](inactive-mailboxes-in-office-365.md)이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-212">If the mailbox or the user's Office 365 user account is deleted, the mailbox becomes an [inactive mailbox](inactive-mailboxes-in-office-365.md).</span></span>
- <span data-ttu-id="a3c0b-213">사서함 (기본 사서함 또는 보관 사서함이 사용 하도록 설정 된 경우)을 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-213">You won't be able to disable the mailbox (either the primary mailbox or the archive mailbox, if it's enabled).</span></span>
- <span data-ttu-id="a3c0b-214">사서함의 항목이 예상 보다 오래 보존 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-214">Items in the mailbox may be retained longer than expected.</span></span> <span data-ttu-id="a3c0b-215">이는 사서함이 보류 중 이므로 영구적으로 삭제 (제거) 되는 것 이기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-215">This is because the mailbox is on hold and therefore no items will be permanently deleted (purged).</span></span>

<span data-ttu-id="a3c0b-216">*ComplianceTagHoldApplied* 속성의 값을 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-216">To view the value of the *ComplianceTagHoldApplied* property, run the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

<span data-ttu-id="a3c0b-217">보존 레이블에 대 한 자세한 내용은 Overview For [Office 365 보존 레이블](labels.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-217">For more information about retention labels, see [Overview of Office 365 retention labels](labels.md).</span></span>

## <a name="managing-mailboxes-on-delay-hold"></a><span data-ttu-id="a3c0b-218">지연 보류 시 사서함 관리</span><span class="sxs-lookup"><span data-stu-id="a3c0b-218">Managing mailboxes on delay hold</span></span>

<span data-ttu-id="a3c0b-219">사서함에서 모든 유형의 보류가 제거 된 후에는 *DelayHoldApplied* mailbox 속성의 값이 **True**로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-219">After any type of hold is removed from a mailbox, the value of the *DelayHoldApplied* mailbox property is set to **True**.</span></span> <span data-ttu-id="a3c0b-220">다음 번에 관리 되는 폴더 도우미가 사서함을 처리 하 고 보류가 제거 되었음을 감지할 때 이러한 상황이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-220">This occurs the next time the Managed Folder Assistant processes the mailbox and detects that a hold has been removed.</span></span> <span data-ttu-id="a3c0b-221">이를 *지연 보존* 이라고 하며, 사서함에서 데이터를 영구적으로 삭제 (제거) 하지 못하도록 30 일 동안 실제로 보존을 제거 하는 작업이 지연 됨을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-221">This is called a *delay hold* and means that the actual removal of the hold is delayed for 30 days to prevent data from being permanently deleted (purged) from the mailbox.</span></span> <span data-ttu-id="a3c0b-222">이를 통해 관리자는 보존을 실제로 제거한 후 제거 되는 사서함 항목을 검색 하거나 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-222">This gives admins an opportunity to search for or recover mailbox items that will be purged after the hold is actually removed.</span></span> <span data-ttu-id="a3c0b-223">사서함에 연기 대기를 설정 하면 사서함이 소송 보존 상태에 있는 것 처럼 여전히 무제한 기간 동안 유지 되는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-223">When a delay hold is placed on the mailbox, the mailbox is still considered to be on hold for an unlimited duration, as if the mailbox was on Litigation Hold.</span></span> <span data-ttu-id="a3c0b-224">30 일 후에 지연 보류가 만료 되 고 Office 365에서 자동으로 지연 대기 ( *DelayHoldApplied* 속성을 **False**로 설정)을 제거 하 여 보류를 실제로 제거 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-224">After 30 days, the delay hold expires, and Office 365 will automatically attempt to remove the delay hold (by setting the *DelayHoldApplied* property to **False**) so that the hold will be actually removed.</span></span> <span data-ttu-id="a3c0b-225">*DelayHoldApplied* 속성을 False로 **설정**하면 다음에 관리 되는 폴더 도우미가 사서함을 처리할 때 제거 하도록 표시 된 항목이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-225">After the *DelayHoldApplied* property to **False**, items that are marked for removal will be purged the next time the mailbox is processed by the Managed Folder Assistant.</span></span>

<span data-ttu-id="a3c0b-226">사서함에 대 한 *DelayHoldApplied* 속성의 값을 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-226">To view the value for the *DelayHoldApplied* property for a mailbox, run the following command in Exchange Online PowerShell.</span></span>

```
Get-Mailbox <username> | FL DelayHoldApplied
```

<span data-ttu-id="a3c0b-227">만료 되기 전에 지연 보존을 제거 하려면 Exchange Online PowerShell에서 다음 명령을 실행 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-227">To remove the delay hold before it expires, you can run the following command in Exchange Online PowerShell:</span></span> 
 
```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
<span data-ttu-id="a3c0b-228">*RemoveDelayHoldApplied* 매개 변수를 사용 하려면 Exchange Online의 법적 보존 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-228">Note that you must be assigned the Legal Hold role in Exchange Online to use the *RemoveDelayHoldApplied* parameter</span></span> 

<span data-ttu-id="a3c0b-229">비활성 사서함에 대 한 지연 대기를 제거 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-229">To remove the delay hold on an inactive mailbox, run the following command in Exchange Online PowerShell:</span></span>

```
Set-Mailbox <DN or Exchange GUID> -InactiveMailbox -RemoveDelayHoldApplied
```

> [!TIP]
> <span data-ttu-id="a3c0b-230">이전 명령에서 비활성 사서함을 지정 하는 가장 좋은 방법은 해당 고유 이름이 나 Exchange GUID 값을 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-230">The best way to specify an inactive mailbox in the previous command is to use its Distinguished Name or Exchange GUID value.</span></span> <span data-ttu-id="a3c0b-231">이러한 값 중 하나를 사용 하면 실수로 잘못 된 사서함을 지정 하는 것을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-231">Using one of these values helps prevent accidentally specifying the wrong mailbox.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="a3c0b-232">다음 단계</span><span class="sxs-lookup"><span data-stu-id="a3c0b-232">Next steps</span></span>

<span data-ttu-id="a3c0b-233">사서함에 적용 되는 보류를 확인 한 후 보류 시간을 변경 하거나 보류를 일시적으로 또는 영구적으로 제거 하거나 정책에서 비활성 사서함을 제외 하 고 Office 365 보존 정책의 경우에는 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-233">After you identify the holds that are applied to a mailbox, you can perform tasks such as changing the duration of the hold, temporarily or permanently removing the hold, or in the case of Office 365 retention policies, excluding an inactive mailbox from the policy.</span></span> <span data-ttu-id="a3c0b-234">보류와 관련 된 작업을 수행 하는 방법에 대 한 자세한 내용은 다음 항목 중 하나를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-234">For more information about performing tasks related to holds, see the one of the following topics:</span></span>

- <span data-ttu-id="a3c0b-235">Security & 준수 센터 PowerShell에서 [ \<new-retentioncompliancepolicy-addexchangelocationexception user mailbox>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/Set-RetentionCompliancePolicy?view=exchange-ps) 명령을 실행 하 여 조직 차원의 Office 365 보존 정책에서 사서함을 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-235">Run the [Set-RetentionCompliancePolicy -AddExchangeLocationException \<user mailbox>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/Set-RetentionCompliancePolicy?view=exchange-ps) command in Security & Compliance Center PowerShell to exclude a mailbox from an organization-wide Office 365 retention policy.</span></span> <span data-ttu-id="a3c0b-236">이 명령은 *ExchangeLocation* 속성 값이 같은 `All`보존 정책에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-236">Note that this command can only be used for retention policies where the value for the *ExchangeLocation* property equals `All`.</span></span>

- <span data-ttu-id="a3c0b-237">Exchange Online PowerShell에서 [접두사 또는 suffix> \<명령 없이 ExcludeFromOrgHolds 보류 GUID](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox?view=exchange-ps) 를 실행 하 여 조직 차원의 Office 365 보존 정책에서 비활성 사서함을 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c0b-237">Run the [Set-Mailbox -ExcludeFromOrgHolds \<hold GUID without prefix or suffix>](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox?view=exchange-ps) command in Exchange Online PowerShell to exclude an inactive mailbox from an organization-wide Office 365 retention policy.</span></span>

- [<span data-ttu-id="a3c0b-238">Office 365에서 비활성 사서함에 대 한 보존 기간 변경</span><span class="sxs-lookup"><span data-stu-id="a3c0b-238">Change the hold duration for an inactive mailbox in Office 365</span></span>](change-the-hold-duration-for-an-inactive-mailbox.md)

- [<span data-ttu-id="a3c0b-239">Office 365에서 비활성 사서함 삭제</span><span class="sxs-lookup"><span data-stu-id="a3c0b-239">Delete an inactive mailbox in Office 365</span></span>](delete-an-inactive-mailbox.md)

- [<span data-ttu-id="a3c0b-240">보류 중인 클라우드 기반 사서함의 복구 가능한 항목 폴더에서 항목 삭제</span><span class="sxs-lookup"><span data-stu-id="a3c0b-240">Delete items in the Recoverable Items folder of cloud-based mailboxes on hold</span></span>](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md)
