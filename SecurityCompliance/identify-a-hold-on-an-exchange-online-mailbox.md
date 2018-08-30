---
title: Exchange Online 사서함의 보류 유형을 식별하는 방법
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6057daa8-6372-4e77-a636-7ea599a76128
ms.openlocfilehash: d24e51bca0e3d290f110b1ab40f3ee9ae7993678
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533764"
---
# <a name="how-to-identify-the-type-of-hold-placed-on-an-exchange-online-mailbox"></a><span data-ttu-id="7c38e-102">Exchange Online 사서함의 보류 유형을 식별하는 방법</span><span class="sxs-lookup"><span data-stu-id="7c38e-102">How to identify the type of hold placed on an Exchange Online mailbox</span></span>

<span data-ttu-id="7c38e-103">이 문서에서는 Office 365의 Exchange Online 사서함에 배치 하는 보류를 식별 하는 방법에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-103">This article explains how to identify holds placed on Exchange Online mailboxes in Office 365.</span></span>

<span data-ttu-id="7c38e-p101">Office 365에는 다양 한 조직에서 영구적으로 삭제 되 고 사서함 콘텐츠를 방지할 수 있는 방법 제공 합니다. 이렇게 하면 준수 사람은 충족 하기 위해 콘텐츠를 유지 하려면 조직 또는 법률 또는 기타 유형의 조사의 기간에 대 한 합니다. Office 365에서 보존 기능 (보류) 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p101">Office 365 offers a number of ways that your organization can prevent mailbox content from being permanently deleted. This allows your organization to retain content to meet compliance regulars or for the duration of legal or other types of investigations. Here's a list of the retention features (also called holds) in Office 365:</span></span>

- <span data-ttu-id="7c38e-107">**소송 보존으로 설정** -Exchange Online에서 사용자 사서함에 적용 되는 보류 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-107">**Litigation Hold** - Holds that are applied to user mailboxes in Exchange Online.</span></span>

- <span data-ttu-id="7c38e-p102">**eDiscovery 보류** -보안 및 규정 준수 센터의 eDiscovery 사례와 연결 된 보류 합니다. eDiscovery 보류 Office 365 그룹 및 Microsoft 팀의 사용자 사서함 및 해당 사서함에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p102">**eDiscovery hold** - Holds that are associated with an eDiscovery case in the Security & Compliance Center. eDiscovery holds can be applied to user mailboxes, and on the corresponding mailbox for Office 365 Groups and Microsoft Teams.</span></span>

- <span data-ttu-id="7c38e-110">**원본 위치 유지** -Exchange 관리자의 원본 위치 eDiscovery & 유지 도구를 사용 하 여 사용자 사서함에 적용 되는 보류를 가운데에 Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="7c38e-110">**In-Place Hold** - Holds that are applied to user mailboxes by using the In-Place eDiscovery & Hold tool in the Exchange admin center in Exchange Online.</span></span>

- <span data-ttu-id="7c38e-p103">**Office 365 보존 정책** -Office 365 그룹 및 팀이 Microsoft Exchange Online 및 해당 사서함에서 사용자 사서함의 콘텐츠를 유지 합니다. 보존을 만들 수 정책 사용자 사서함에 저장 되는 비즈니스 대화에 대 한 Skype를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p103">**Office 365 retention policy** - Retains content in user mailboxes in Exchange Online and in the corresponding mailbox for Office 365 Groups and Microsoft Teams. You can create a retention policy retains Skype for Business Conversations, which are stored in user mailboxes.</span></span>

  <span data-ttu-id="7c38e-113">사서함에 할당 될 수 있는 Office 365 보존 정책에는 다음과 같은 두가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-113">There are two types of Office 365 retention policies that can be assigned to mailboxes.</span></span>

    - <span data-ttu-id="7c38e-p104">**특정 위치 보존 정책** -이것은 특정 사용자의 콘텐츠 위치에 할당 된 정책입니다. Exchange Online PowerShell에서 Get-mailbox cmdlet를 사용 하 여 특정 사서함에 할당 된 보존 정책에 대 한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p104">**Specific location retention policies** - These are policies that are assigned to the content locations of specific users. You use the Get-Mailbox cmdlet in Exchange Online PowerShell to get information about retention policies assigned to specific mailboxes.</span></span>

    - <span data-ttu-id="7c38e-p105">**조직 전체의 보존 정책** -이것은 조직에서 모든 콘텐츠 위치에 할당 된 정책입니다. Exchange Online PowerShell에서 Get-organizationconfig cmdlet를 사용 하 여 조직 전체의 보존 정책에 대 한 정보를 얻을 수 있습니다. 자세한 내용은 Office 365 개요 (영문) 보존 정책에서 "전체 조직 또는 특정 위치에 보존 정책 적용" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p105">**Organization-wide retention policies** - These are policies that are assigned to all content locations in your organization. You use the Get-OrganizationConfig cmdlet in Exchange Online PowerShell to get information about organization-wide retention policies. For more information, see the "Applying a retention policy to an entire organization or specific locations" section in Overview of Office 365 retention policies.</span></span>

<span data-ttu-id="7c38e-p106">보류에 있는 사서함을 관리 하려면 보류에 보존 기간을 변경, 일시적 또는 영구적으로 제거 보류를 또는 사서함을 제외 하 고 Office 365 보존 정책에서 등의 작업을 수행할 수 있도록 사서함에 배치 되는 형식을 식별 해야할 수 있습니다. 이러한 경우 첫 단계는 사서함에 배치 하는 보류의 형식을 식별 하기 위해입니다. 및 여러 보류 (및 다양 한 유형의 보류) 단일 사서함에 배치할 수, 하기 때문에 해야 하거나 제거 하거나 해당 보류를 변경 하려는 경우 사서함에 배치 하는 모든 보류를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p106">To manage mailboxes on hold, you may have to identify the type of hold that's placed on a mailbox so that you can perform tasks such as changing the hold duration, temporarily or permanently removing the hold, or excluding a mailbox from a Office 365 retention policy. In these cases, the first step is to identify the type of hold placed on the mailbox. And because multiple holds (and different types of holds) can be placed on a single mailbox, you'll have to identify all holds placed on a mailbox if you want to remove or change those holds.</span></span>

## <a name="step-1-obtaining-the-guid-for-holds-placed-on-a-mailbox"></a><span data-ttu-id="7c38e-122">1 단계: 사서함에 배치 보류에 대 한 GUID 가져오기</span><span class="sxs-lookup"><span data-stu-id="7c38e-122">Step 1: Obtaining the GUID for holds placed on a mailbox</span></span>

<span data-ttu-id="7c38e-p107">사서함에 배치 되는 보류의 GUID를 가져올 Exchange Online PowerShell에서 다음 두 cmdlet을 실행할 수 있습니다. GUID를 확인 한 후 2 단계에서에서 특정 보류를 식별 하는데 사용 합니다. GUID로 소송 보존을 포함 하 고는 식별 되지를 메모 합니다. 소송 보존 사용 하거나 사서함을 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p107">You can run the following two cmdlets in Exchange Online PowerShell to get the GUID of the holds that are placed on a mailbox. After you obtain a GUID, you use it to identify the specific hold in Step 2. Note that Litigation Holds are not identified by a GUID. Litigation Holds are either enabled or disabled for a mailbox.</span></span>

- <span data-ttu-id="7c38e-p108">**Get-mailbox** -사용 하 여 사서함에 대 한 소송 보존을 사용할지 여부를 확인 하 고 eDiscovery에 대 한 Guid를 가져오려면이 cmdlet을 포함 하 고, 원본 위치 유지 및 구체적으로 사서함에 할당 된 Office 365 보존 정책입니다. 또한 조직 전체의 보존 정책에서 사서함 명시적으로 제외 되었는지 하는 경우이 cmdlet의 출력을 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p108">**Get-Mailbox** - Use this cmdlet to determine whether Litigation Hold is enabled for a mailbox and to get the GUIDs for eDiscovery holds, In-Place Holds, and Office 365 retention policies that are specifically assigned to a mailbox. The output of this cmdlet will also indicate if a mailbox has been explicitly excluded from an organization-wide retention policy.</span></span>

- <span data-ttu-id="7c38e-129">**Get-organizationconfig** -조직 전체의 보존 정책에 대 한 Guid를 가져올이 cmdlet 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-129">**Get-OrganizationConfig** - Use this cmdlet to get the GUIDs for organization-wide retention policies.</span></span>

<span data-ttu-id="7c38e-130">Exchange Online PowerShell 연결할 [Connect to Exchange Online PowerShell를](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7c38e-130">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>

### <a name="get-mailbox"></a><span data-ttu-id="7c38e-131">Get-Mailbox</span><span class="sxs-lookup"><span data-stu-id="7c38e-131">Get-Mailbox</span></span>

<span data-ttu-id="7c38e-132">보류 및 사서함에 적용 하는 Office 365 보존 정책에 대 한 정보를 가져오려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-132">Run the following command to get information about the holds and Office 365 retention policies applied to a mailbox.</span></span>

```
Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
```

> [!TIP]
> <span data-ttu-id="7c38e-133">실행할 수 InPlaceHolds 속성에 너무 많은 값이 모두 하지 표시 하는 경우는 `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` 별도 줄에 각 GUID를 표시 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-133">If there are too many values in the InPlaceHolds property and not all of them are displayed, you can run the `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` command to display each GUID on a separate line.</span></span>

<span data-ttu-id="7c38e-134">다음 표에서 다양 한 유형의 **Get-mailbox** cmdlet을 실행 하는 경우 *InPlaceHolds* 속성의 값에 따라 보류를 식별 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-134">The following table describes how to identify different types of holds based on the values in the *InPlaceHolds* property when you run the **Get-Mailbox** cmdlet.</span></span>


|<span data-ttu-id="7c38e-135">종류를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-135">Hold type</span></span>  |<span data-ttu-id="7c38e-136">예제 값</span><span class="sxs-lookup"><span data-stu-id="7c38e-136">Example value</span></span>  |<span data-ttu-id="7c38e-137">보류를 식별 하는 방법</span><span class="sxs-lookup"><span data-stu-id="7c38e-137">How to identify the hold</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="7c38e-138">소송 보존</span><span class="sxs-lookup"><span data-stu-id="7c38e-138">Litigation Hold</span></span>     |    `True`     |     <span data-ttu-id="7c38e-139">*LitigationHoldEnabled* 속성이로 설정 된 경우 사서함에 대 한 소송 보존 상태가 `True`합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-139">Litigation Hold is enabled for a mailbox if the *LitigationHoldEnabled* property is set to `True`.</span></span>    |
|<span data-ttu-id="7c38e-140">eDiscovery 보류</span><span class="sxs-lookup"><span data-stu-id="7c38e-140">eDiscovery hold</span></span>     |  `UniH7d895d48-7e23-4a8d-8346-533c3beac15d`       |   <span data-ttu-id="7c38e-p109">*InPlaceHolds 속성* 은 보안 및 규정 준수 센터에서 eDiscovery 사례와 관련 된 모든 보류의 GUID를 포함 합니다. 이런 현상이 발생 eDiscovery 보류도 시작 하는 GUID를 알 수는 `UniH` 접두사 (하는 통합 유지 나타냅니다).</span><span class="sxs-lookup"><span data-stu-id="7c38e-p109">The *InPlaceHolds property* contains the GUID of any hold associated with an eDiscovery case in the Security & Compliance Center. You can tell this is an eDiscovery hold because the GUID starts with the `UniH` prefix (which denotes a Unified Hold).</span></span>      |
|<span data-ttu-id="7c38e-143">원본 위치 유지</span><span class="sxs-lookup"><span data-stu-id="7c38e-143">In-Place Hold</span></span>     |     `c0ba3ce811b6432a8751430937152491` <br/> <span data-ttu-id="7c38e-144">또는</span><span class="sxs-lookup"><span data-stu-id="7c38e-144">or</span></span> <br/> `cld9c0a984ca74b457fbe4504bf7d3e00de`  |     <span data-ttu-id="7c38e-p110">*InPlaceHolds* 속성의 사서함에 배치 되는 원본 위치 유지의 GUID를 포함 합니다. 이런 현상이 발생 한 원본 위치 유지 하거나 GUID를 접두사로 시작 되지 않으면 또는로 시작 하는 것을 알 수는 `cld` 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p110">The *InPlaceHolds* property contains the GUID of the In-Place Hold that's placed on the mailbox. You can tell this is an In-Place Hold because the GUID either doesn't start with a prefix or it starts with the `cld` prefix.</span></span>     |
|<span data-ttu-id="7c38e-147">구체적으로 사서함에 적용 되는 office 365 보존 정책</span><span class="sxs-lookup"><span data-stu-id="7c38e-147">Office 365 retention policy specifically applied to the mailbox</span></span>     |    `mbxcdbbb86ce60342489bff371876e7f224:1` <br/> <span data-ttu-id="7c38e-148">또는</span><span class="sxs-lookup"><span data-stu-id="7c38e-148">or</span></span> <br/> `skp127d7cf1076947929bf136b7a2a8c36f:3`     |     <span data-ttu-id="7c38e-p111">InPlaceHolds 속성에는 사서함에 적용 되는 모든 특정 위치 보존 정책의 guid가 포함 됩니다. 으로 시작 하는 GUID 때문에 보존 정책을 식별할 수는 `mbx` 또는 `skp` 접두사입니다. `skp` 접두사는 사용자의 사서함에서 비즈니스 대화에 대 한의 보존 정책 Skype 적용 되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p111">The InPlaceHolds property contains GUIDs of any specific location retention policy that's applied to the mailbox. You can identify retention policies because the GUID starts with the `mbx` or the `skp` prefix. The `skp` prefix indicates that the retention policy is applied to Skype for Business conversations in the user's mailbox.</span></span>    |
|<span data-ttu-id="7c38e-152">조직 전체의 Office 365 보존 정책에서 제외</span><span class="sxs-lookup"><span data-stu-id="7c38e-152">Excluded from an organization-wide Office 365 retention policy</span></span>     |   `-mbxe9b52bf7ab3b46a286308ecb29624696`      |     <span data-ttu-id="7c38e-153">사서함은 조직 전체의 Office 365 보존 정책에서 제외 하 고, 사서함에서 제외 보존 정책에 대 한 GUID InPlaceHolds 속성에 표시 되 고으로 식별 되는 `-mbx` 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-153">If a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy the mailbox is excluded from is displayed in the InPlaceHolds property and is identified by the `-mbx` prefix.</span></span>    |

### <a name="get-organizationconfig"></a><span data-ttu-id="7c38e-154">Get-organizationconfig</span><span class="sxs-lookup"><span data-stu-id="7c38e-154">Get-OrganizationConfig</span></span>
<span data-ttu-id="7c38e-p112">**Get-mailbox** cmdlet을 실행 하는 경우 *InPlaceHolds* 속성이 비어 있는 경우 발생할 수 있습니다 하나 이상의 조직 전체의 Office 365 보존 정책 사서함에 적용 합니다. 다음 명령을 실행 Exchange Online 조직 전체의 Office 365 보존 정책에 대 한 Guid의 목록을 표시 하려면 PowerShell 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p112">If the *InPlaceHolds* property is empty when you run the **Get-Mailbox** cmdlet, there still may be one or more organization-wide Office 365 retention policies applied to the mailbox. Run the following command in Exchange Online PowerShell to get a list of GUIDs for organization-wide Office 365 retention policies.</span></span>

```
Get-OrganizationConfig | FL InPlaceHolds
```

> [!TIP]
> <span data-ttu-id="7c38e-157">실행할 수 InPlaceHolds 속성에 너무 많은 값이 모두 하지 표시 하는 경우는 `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` 별도 줄에 각 GUID를 표시 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-157">If there are too many values in the InPlaceHolds property and not all of them are displayed, you can run the `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command to display each GUID on a separate line.</span></span>

<span data-ttu-id="7c38e-158">다음 표에서 다양 한 유형의 조직 전체의 보류 및 **Get-organizationconfig** cmdlet을 실행 하는 경우 *InPlaceHolds* 속성에 포함 된 Guid에 따라 각 유형을 식별 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-158">The following table describes the different types of organization-wide holds and how to identify each type based on the GUIDs contained in *InPlaceHolds* property when you run the **Get-OrganizationConfig** cmdlet.</span></span>


|<span data-ttu-id="7c38e-159">종류를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-159">Hold type</span></span>  |<span data-ttu-id="7c38e-160">예제 값</span><span class="sxs-lookup"><span data-stu-id="7c38e-160">Example value</span></span>  |<span data-ttu-id="7c38e-161">설명</span><span class="sxs-lookup"><span data-stu-id="7c38e-161">Description</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="7c38e-162">채팅을 통해 Exchange 사서함, Exchange 공용 폴더 및 팀에 office 365 보존 정책 적용</span><span class="sxs-lookup"><span data-stu-id="7c38e-162">Office 365 retention policies applied to Exchange mailboxes, Exchange public folders, and Teams chats</span></span>    |      `mbx7cfb30345d454ac0a989ab3041051209:2`   |   <span data-ttu-id="7c38e-p113">Exchange 사서함을 Exchange 공용 폴더에 적용 된 조직 전체의 보존 정책 및 Microsoft 팀의 1xN 채팅으로 시작 하는 Guid로 식별 됩니다는 `mbx` 접두사입니다. Note 1xN 채팅은 개별 채팅 참가자의 사서함에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p113">Organization-wide retention policies applied to Exchange mailboxes, Exchange public folders, and 1xN chats in Microsoft Teams are identified by GUIDs that start with the `mbx` prefix. Note that 1xN chats are stored in the mailbox of the individual chat participants.</span></span>      |
|<span data-ttu-id="7c38e-165">Office 365 그룹 및 팀에 해당 하는 채널의 메시지에 적용 되는 office 365 보존 정책</span><span class="sxs-lookup"><span data-stu-id="7c38e-165">Office 365 retention policy applied to Office 365 Groups and Teams channel messages</span></span>     |   `grp1a0a132ee8944501a4bb6a452ec31171:3`      |    <span data-ttu-id="7c38e-p114">Office 365 그룹과 팀이 Microsoft에서 채널 메시지에 적용 된 조직 전체의 보존 정책으로 시작 하는 Guid로 식별 됩니다는 `grp` 접두사입니다. Note는 채널 메시지 Microsoft 팀과 연결 된 그룹 사서함에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p114">Organization-wide retention policies applied to Office 365 groups and channel messages in Microsoft Teams are identified by GUIDs that start with the `grp` prefix. Note that channel messages are stored in the group mailbox that is associated with a Microsoft Team.</span></span>     |

<span data-ttu-id="7c38e-168">자세한 내용은 보존 정책 Microsoft 팀에 적용 된 [보존 정책 개요](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations)"팀 위치" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7c38e-168">For more information retention policies applied to Microsoft Teams, see the "Teams location" section [Overview of retention policies](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).</span></span>

### <a name="understanding-the-format-of-the-inplaceholds-value-for-retention-policies"></a><span data-ttu-id="7c38e-169">보존 정책에 대 한 InPlaceHolds 값의 형식을 이해 (영문)</span><span class="sxs-lookup"><span data-stu-id="7c38e-169">Understanding the format of the InPlaceHolds value for retention policies</span></span>

<span data-ttu-id="7c38e-p115">접두사 (mbx, skp, 또는 그룹)는 Office 365 보존 정책으로 InPlaceHolds 속성에서 항목을 식별 하는, 외에도 값도 정책에 대해 구성 된 보존 작업 유형을 식별 하는 접미사를 포함 합니다. 예, 작업 접미사는 다음 예제에서 굵은 글꼴로 강조 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p115">In addition to the prefix (mbx, skp, or grp) that identifies an item in the InPlaceHolds property as an Office 365 retention policy, the value also contains a suffix that identifies the type of retention action that's configured for the policy. For example, the action suffix is highlighted in bold type in the following examples:</span></span>

   <span data-ttu-id="7c38e-172">`skp127d7cf1076947929bf136b7a2a8c36f`**: 1**</span><span class="sxs-lookup"><span data-stu-id="7c38e-172">`skp127d7cf1076947929bf136b7a2a8c36f`**:1**</span></span>

   <span data-ttu-id="7c38e-173">`mbx7cfb30345d454ac0a989ab3041051209`**: 2**</span><span class="sxs-lookup"><span data-stu-id="7c38e-173">`mbx7cfb30345d454ac0a989ab3041051209`**:2**</span></span>

   <span data-ttu-id="7c38e-174">`grp1a0a132ee8944501a4bb6a452ec31171`**: 3**</span><span class="sxs-lookup"><span data-stu-id="7c38e-174">`grp1a0a132ee8944501a4bb6a452ec31171`**:3**</span></span>

<span data-ttu-id="7c38e-175">다음 표에서 세 가능한 보존 작업을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-175">The following table defines the three possible retention actions:</span></span>

|<span data-ttu-id="7c38e-176">값</span><span class="sxs-lookup"><span data-stu-id="7c38e-176">Value</span></span>  |<span data-ttu-id="7c38e-177">설명</span><span class="sxs-lookup"><span data-stu-id="7c38e-177">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="7c38e-178">**1**</span><span class="sxs-lookup"><span data-stu-id="7c38e-178">**1**</span></span>     | <span data-ttu-id="7c38e-179">보존 정책 항목을 삭제 하도록 구성 된를 나타냅니다. 정책 항목을 유지 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-179">Indicates the retention policy is configured to delete items; the policy doesn't retain items.</span></span>        |
|<span data-ttu-id="7c38e-180">**2**</span><span class="sxs-lookup"><span data-stu-id="7c38e-180">**2**</span></span>    |    <span data-ttu-id="7c38e-181">보존 정책 항목을 유지 하도록 구성 된를 나타냅니다. 보존 기간이 만료 후 정책 항목을 삭제 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-181">Indicates the retention policy is configured to hold items; the policy doesn't delete items after the retention period expires.</span></span>     |
|<span data-ttu-id="7c38e-182">**3**</span><span class="sxs-lookup"><span data-stu-id="7c38e-182">**3**</span></span>     |   <span data-ttu-id="7c38e-183">보존 정책 항목을 유지 하 고 다음 보존 기간이 만료 후 삭제 하도록 구성 된를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-183">Indicates the retention policy is configured to hold items and then delete them after the retention period expires.</span></span>      |

<span data-ttu-id="7c38e-184">보존 작업에 대 한 자세한 내용은 [보존 정책의 개요 (영문)](retention-policies.md#retaining-content-for-a-specific-period-of-time)의 "특정 기간에 대 한 콘텐츠 유지" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7c38e-184">For more information about retention actions, see the "Retaining content for a specific period of time" section in [Overview of retention policies](retention-policies.md#retaining-content-for-a-specific-period-of-time).</span></span>
   
## <a name="step-2-using-the-guid-to-identify-the-hold"></a><span data-ttu-id="7c38e-185">2 단계: 보류를 식별 하는 GUID를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="7c38e-185">Step 2: Using the GUID to identify the hold</span></span>

<span data-ttu-id="7c38e-p116">사서함에 적용 되는 보류에 대 한 GUID를 가져오려면 후 보류를 식별 하는 GUID를 사용 하 여 다음 단계가입니다. 다음 섹션에서는 보류 GUID를 사용 하 여 보류 (및 기타 정보)의 이름을 식별 하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p116">After you obtain the GUID for a hold that is applied to a mailbox, the next step is to use that GUID to identify the hold. The following sections show how to identify the name of the hold (and other information) by using the hold GUID.</span></span>

### <a name="ediscovery-holds"></a><span data-ttu-id="7c38e-188">eDiscovery 보류</span><span class="sxs-lookup"><span data-stu-id="7c38e-188">eDiscovery holds</span></span>

<span data-ttu-id="7c38e-p117">사서함에 적용 되는 eDiscovery 보류를 식별 하는 보안 및 규정 준수 센터 PowerShell에서 다음 명령을 실행 합니다. (UniH 접두사) 포함 하지 GUID를 사용 하 여 eDiscovery에 대 한 1 단계에서에서 확인 된를 보관 합니다. 첫번째 명령은 보류; 하는 방법에 대 한 정보가 포함 된 변수를 만듭니다. 이 변수는 다른 명령에서 사용 됩니다. 두번째 명령은 eDiscovery 대/소문자와 연결 된 보류의 이름을 표시 합니다. 세번째 명령은 보류를 적용 하는 사서함의 목록과 보류의 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p117">Run the following commands in Security & Compliance Center PowerShell to identify an eDiscovery hold that's applied to the mailbox. Use the GUID (not including the UniH prefix) for the eDiscovery hold that you identified in Step 1. The first command creates a variable that contains information about the hold; this variable is used in the other commands. The second command displays the name of the eDiscovery case the hold is associated with. The third command displays the name of the hold and a list of the mailboxes the hold applies to.</span></span>

```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold | FL Name,ExchangeLocation
```

<span data-ttu-id="7c38e-194">보안 및 규정 준수 센터 PowerShell에 연결할 [하 고 Office 365 보안 및 규정 준수 센터 PowerShell 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7c38e-194">To connect to Security & Compliance Center PowerShell, see  [Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

### <a name="in-place-holds"></a><span data-ttu-id="7c38e-195">원본 위치 유지</span><span class="sxs-lookup"><span data-stu-id="7c38e-195">In-Place Holds</span></span>

<span data-ttu-id="7c38e-p118">사서함에 적용 되는 원본 위치 유지를 식별 하는 Exchange Online PowerShell에서 다음 명령을 실행 합니다. 1 단계에서에서 식별 된 원본 위치 유지 하는 GUID를 사용 합니다. 명령은 보류를 적용 하는 사서함의 목록과 보류의 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p118">Run the following command in Exchange Online PowerShell to identify the In-Place Hold that's applied to the mailbox. Use the GUID for the In-Place Hold that you identified in Step 1. The command displays the name of the hold and a list of the mailboxes the hold applies to.</span></span>

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name,SourceMailboxes
```
<span data-ttu-id="7c38e-199">경우에는 GUID로 시작 하는 원본 위치 유지에 대 한 참고는 `cld` 접두사, 이전 명령을 실행할 때 접두사를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-199">Note that if the GUID for the In-Place Hold starts with the `cld` prefix, be sure to include the prefix when running the previous command.</span></span>

### <a name="office-365-retention-policies"></a><span data-ttu-id="7c38e-200">Office 365 보존 정책</span><span class="sxs-lookup"><span data-stu-id="7c38e-200">Office 365 retention policies</span></span>

<span data-ttu-id="7c38e-p119">다음 명령을 실행에서 보안 및 규정 준수 센터 PowerShell id에는 사서함에 적용 되는 Office 365 보존 정책 (조직 차원의 또는 특정 위치). 1 단계에서에서 식별 하는 GUID (포함 안 mbx, skp, 또는 그룹 접두사 또는 작업 접미사)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p119">Run the following command in Security & Compliance Center PowerShell to identity the Office 365 retention policy (organization-wide or specific location) that's applied to the mailbox. Use the GUID (not including the mbx, skp, or grp prefix or the action suffix) that you identified in Step 1.</span></span>

```
Get-RetentionCompliancePolicy <hold GUID without prefix or suffix> -DistributionDetail  | FL Name,*Location
```

## <a name="next-steps"></a><span data-ttu-id="7c38e-203">다음 단계</span><span class="sxs-lookup"><span data-stu-id="7c38e-203">Next steps</span></span>

<span data-ttu-id="7c38e-p120">사서함에 적용 되는 보류를 파악 한 후 비활성 사서함 정책에서 제외 하 고 작업 예: 일시적으로 보류를 기간을 변경 또는 보류를 영구적으로 제거 또는 Office 365 보존 정책의 경우 수행할 수 있습니다. 보류와 관련 된 작업을 수행 하는 방법에 대 한 자세한 내용은 다음 항목 중 하나를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p120">After you identify the holds that are applied to a mailbox, you can perform tasks such as changing the duration of the hold, temporarily or permanently removing the hold, or in the case of Office 365 retention policies, excluding an inactive mailbox from the policy. For more information about performing tasks related to holds, see the one of the following topics:</span></span>

- <span data-ttu-id="7c38e-p121">실행 하는 [집합 RetentionCompliancePolicy AddExchangeLocationException \<사용자 사서함 >](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/Set-RetentionCompliancePolicy?view=exchange-ps) 보안 및 규정 준수 센터 PowerShell 조직 전체의 Office 365 보존 정책에서 사서함을 제외 하도록 명령 합니다. 이 명령을 사용할 수 있도록만 보존 정책에 대 한 *ExchangeLocation* 속성에 대 한 값과 일치 하는 여기서 참고 `All`합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-p121">Run the [Set-RetentionCompliancePolicy -AddExchangeLocationException \<user mailbox>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/Set-RetentionCompliancePolicy?view=exchange-ps) command in Security & Compliance Center PowerShell to exclude a mailbox from an organization-wide Office 365 retention policy. Note that this command can only be used for retention policies where the value for the *ExchangeLocation* property equals `All`.</span></span>

- <span data-ttu-id="7c38e-208">실행 하는 [Set-mailbox ExcludeFromOrgHolds \<접두사 또는 접미사 하지 않고 GUID를 보유할 >](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox?view=exchange-ps) 는 조직 전체의 Office 365 보존 정책에서 비활성 사서함을 제외 하는 Exchange Online PowerShell에서 명령 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c38e-208">Run the [Set-Mailbox -ExcludeFromOrgHolds \<hold GUID without prefix or suffix>](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox?view=exchange-ps) command in Exchange Online PowerShell to exclude an inactive mailbox from an organization-wide Office 365 retention policy.</span></span>

- [<span data-ttu-id="7c38e-209">Office 365에서 비활성 사서함에 대 한 보존 기간 변경</span><span class="sxs-lookup"><span data-stu-id="7c38e-209">Change the hold duration for an inactive mailbox in Office 365</span></span>](change-the-hold-duration-for-an-inactive-mailbox.md)

- [<span data-ttu-id="7c38e-210">Office 365에서 비활성 사서함 삭제</span><span class="sxs-lookup"><span data-stu-id="7c38e-210">Delete an inactive mailbox in Office 365</span></span>](delete-an-inactive-mailbox.md)

- [<span data-ttu-id="7c38e-211">보류 중인 클라우드 기반 사서함의 복구 가능한 항목 폴더에서 항목 삭제</span><span class="sxs-lookup"><span data-stu-id="7c38e-211">Delete items in the Recoverable Items folder of cloud-based mailboxes on hold</span></span>](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md)
