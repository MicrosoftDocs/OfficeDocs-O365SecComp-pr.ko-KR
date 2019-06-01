---
title: 정보 장벽 개요
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: 정보 장애물을 사용 하 여 조직 내에서 Microsoft 팀을 사용 하 여 통신을 준수 하는지 확인 합니다.
ms.openlocfilehash: e52a62ca0b80aed577be1978b81c8a01ac2371b9
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668324"
---
# <a name="information-barriers-preview"></a><span data-ttu-id="9f4e0-103">정보 장벽 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="9f4e0-103">Information barriers (Preview)</span></span>

<span data-ttu-id="9f4e0-104">Microsoft 클라우드 서비스에는 강력한 통신 및 공동 작업 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-104">Microsoft cloud services include powerful communication and collaboration capabilities.</span></span> <span data-ttu-id="9f4e0-105">하지만 조직에서 발생할 수 있는 충돌을 방지 하기 위해 두 그룹 간의 통신을 제한 하려는 경우를 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-105">But suppose that you want to restrict communications between two groups to avoid a conflict of interest from occurring in your organization.</span></span> <span data-ttu-id="9f4e0-106">아니면 내부 정보를 보호 하기 위해 조직 내부의 특정 사용자 간의 통신을 제한 하려는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-106">Or, perhaps you want to restrict communications between certain people inside your organization in order to safeguard internal information.</span></span> <span data-ttu-id="9f4e0-107">Microsoft 365을 사용 하면 그룹 및 조직에서 통신 및 공동 작업을 수행할 수 있으므로 필요한 경우 특정 사용자 그룹 간에 통신을 제한할 수 있는 방법이 있나요?</span><span class="sxs-lookup"><span data-stu-id="9f4e0-107">Microsoft 365 enables communication and collaboration across groups and organizations, so is there a way to restrict communications among specific groups of users when necessary?</span></span> <span data-ttu-id="9f4e0-108">정보 장벽에서는 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-108">With information barriers, you can!</span></span> 

<span data-ttu-id="9f4e0-109">정보 장애물은 지금 미리 볼 수 있습니다 (Microsoft 팀부터 시작).</span><span class="sxs-lookup"><span data-stu-id="9f4e0-109">Information barriers are in preview now, beginning with Microsoft Teams.</span></span> <span data-ttu-id="9f4e0-110">조직에서 이러한 기능을 사용할 수 있는 경우 준수 관리자 또는 정보 장벽 관리자는 Microsoft 팀의 사용자 그룹 간 통신을 허용 하거나 차단 하는 정책을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-110">When these features are available for your organization, a compliance administrator or information barriers administrator can define policies to allow or prevent communications between groups of users in Microsoft Teams.</span></span> <span data-ttu-id="9f4e0-111">정보 장벽 정책은 다음과 같은 경우에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-111">Information barrier policies can be used for situations like these:</span></span>

- <span data-ttu-id="9f4e0-112">하루 상인은 마케팅 팀에서 다른 사람에 게 전화를 걸 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-112">A day trader cannot call someone on the marketing team</span></span>
- <span data-ttu-id="9f4e0-113">기밀 회사 정보에 대 한 작업을 수행 하는 금융 직원은 조직 내의 특정 그룹에서 전화를 받을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-113">Finance personnel working on confidential company information cannot receive calls from certain groups within their organization</span></span>
- <span data-ttu-id="9f4e0-114">영업 비밀 자료가 있는 내부 팀이 조직 내의 특정 그룹에 있는 사용자와 통화 하거나 온라인으로 대화할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-114">An internal team with trade secret material cannot call or chat online with people in certain groups within their organization</span></span>
- <span data-ttu-id="9f4e0-115">연구 팀은 제품 개발 팀과 온라인 으로만 전화를 걸어 대화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-115">A research team can only call or chat online with a product development team</span></span>

<span data-ttu-id="9f4e0-116">이러한 모든 시나리오 (및 이상)에서 정보 장벽 정책은 Microsoft 팀의 통신을 방지 하거나 허용 하도록 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-116">For all of these example scenarios (and more), information barrier policies can be defined to prevent or allow communications in Microsoft Teams.</span></span> <span data-ttu-id="9f4e0-117">이러한 정책을 사용 하면 사용자가 전화를 걸 수도 있고 채팅을 할 수 없거나, 사용자가 Microsoft 팀의 특정 그룹과 통신 하는 것을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-117">Such policies can prevent people from calling or chatting with those they shouldn't, or enable people to communicate only with specific groups in Microsoft Teams.</span></span> <span data-ttu-id="9f4e0-118">정보 장벽 정책을 적용 하면 해당 정책에 포함 된 사용자가 Microsoft 팀의 다른 사람들과 통신을 시도할 때마다 정보 장벽 정책에 정의 된 대로 통신을 방지 하거나 허용 하기 위해 검사가 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-118">With information barrier policies in effect, whenever users who are covered by those policies attempt to communicate with others in Microsoft Teams, checks are done to prevent (or allow) communication (as defined by information barrier policies).</span></span> 

> [!NOTE]
> <span data-ttu-id="9f4e0-119">정보 장애물은 SharePoint Online 또는 OneDrive를 통한 전자 메일 통신 또는 파일 공유에는 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-119">Information barriers will not apply to email communications or to file sharing through SharePoint Online or OneDrive.</span></span>

<span data-ttu-id="9f4e0-120">정보 장벽 정책은 다음과 같은 유형의 통신 작업에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-120">Information barrier policies apply to the following kinds of communication activities:</span></span>

- <span data-ttu-id="9f4e0-121">사용자 검색</span><span class="sxs-lookup"><span data-stu-id="9f4e0-121">Searching for user</span></span>
- <span data-ttu-id="9f4e0-122">팀에 구성원 추가</span><span class="sxs-lookup"><span data-stu-id="9f4e0-122">Adding a member to a team</span></span>
- <span data-ttu-id="9f4e0-123">다른 사용자와의 채팅 세션 시작</span><span class="sxs-lookup"><span data-stu-id="9f4e0-123">Starting a chat session with someone</span></span>
- <span data-ttu-id="9f4e0-124">그룹 채팅 시작</span><span class="sxs-lookup"><span data-stu-id="9f4e0-124">Starting a group chat</span></span> 
- <span data-ttu-id="9f4e0-125">다른 사용자에 게 모임 참가 초대</span><span class="sxs-lookup"><span data-stu-id="9f4e0-125">Inviting someone to join a meeting</span></span>
- <span data-ttu-id="9f4e0-126">화면 공유</span><span class="sxs-lookup"><span data-stu-id="9f4e0-126">Sharing a screen</span></span> 
- <span data-ttu-id="9f4e0-127">전화 걸기</span><span class="sxs-lookup"><span data-stu-id="9f4e0-127">Placing a call</span></span>

<span data-ttu-id="9f4e0-128">관련 된 사용자가 활동을 방지 하는 정보 장벽 정책에 포함 되어 있는 경우에는 작업을 계속할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-128">If the people involved are included in an information barrier policy that prevents the activity, they will not be able to proceed.</span></span> <span data-ttu-id="9f4e0-129">정보 장벽에 대 한 사용자 환경에 대 한 자세한 내용은 [Microsoft 팀의 정보 장벽](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-129">To learn more about the user experience with information barriers, see [information barriers in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).</span></span>

<span data-ttu-id="9f4e0-130">현재 정보 장벽 정책은 PowerShell cmdlet을 사용 하 여 Office 365에서 정의 되 고 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-130">Currently, information barrier policies are defined and managed in Office 365 by using PowerShell cmdlets.</span></span> <span data-ttu-id="9f4e0-131">이 작업은 일반적으로 준수 관리자 또는 전역 관리자가 수행 하며 PowerShell cmdlet 및 매개 변수에 친숙 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-131">This is typically done by a compliance administrator or a global administrator, and requires familiarity with PowerShell cmdlets (and parameters).</span></span> <span data-ttu-id="9f4e0-132">자세한 내용은 [PowerShell (정보 장벽 정의)](information-barriers-policies.md#powershell)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-132">To learn more, see [PowerShell (for defining information barriers)](information-barriers-policies.md#powershell).</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="9f4e0-133">필요한 라이선스 및 사용 권한</span><span class="sxs-lookup"><span data-stu-id="9f4e0-133">Required licenses and permissions</span></span>

<span data-ttu-id="9f4e0-134">**현재 정보 장벽 기능은 개인 미리 보기에**있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-134">**Currently, the information barrier feature is in private preview**.</span></span> <span data-ttu-id="9f4e0-135">일반적으로 이러한 기능을 사용할 수 있는 경우 다음과 같은 구독에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-135">When these features are generally available, they'll be included in subscriptions, such as:</span></span>

- <span data-ttu-id="9f4e0-136">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="9f4e0-136">Microsoft 365 E5</span></span>
- <span data-ttu-id="9f4e0-137">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="9f4e0-137">Office 365 E5</span></span>
- <span data-ttu-id="9f4e0-138">Office 365 Advanced Compliance</span><span class="sxs-lookup"><span data-stu-id="9f4e0-138">Office 365 Advanced Compliance</span></span>
- <span data-ttu-id="9f4e0-139">Microsoft 365 E5 정보 보호 및 규정 준수</span><span class="sxs-lookup"><span data-stu-id="9f4e0-139">Microsoft 365 E5 Information Protection and Compliance</span></span>

<span data-ttu-id="9f4e0-140">자세한 내용은 [준수 솔루션](https://products.office.com/business/security-and-compliance/compliance-solutions)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-140">For more details, see [Compliance Solutions](https://products.office.com/business/security-and-compliance/compliance-solutions).</span></span>

<span data-ttu-id="9f4e0-141">[정보 장벽 정책을 정의 하거나 편집](information-barriers-policies.md)하려면 다음 역할 중 하나를 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-141">To [define or edit information barrier policies](information-barriers-policies.md), you must be assigned one of the following roles:</span></span>

- <span data-ttu-id="9f4e0-142">Microsoft 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="9f4e0-142">Microsoft 365 global administrator</span></span>
- <span data-ttu-id="9f4e0-143">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="9f4e0-143">Office 365 global administrator</span></span>
- <span data-ttu-id="9f4e0-144">준수 관리자</span><span class="sxs-lookup"><span data-stu-id="9f4e0-144">Compliance administrator</span></span>
- <span data-ttu-id="9f4e0-145">정보 장벽 관리자</span><span class="sxs-lookup"><span data-stu-id="9f4e0-145">Information barriers administrator</span></span>

<span data-ttu-id="9f4e0-146">정보 장벽 정책을 정의, 유효성 검사 또는 편집 하려면 PowerShell cmdlet을 잘 알고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-146">You must be familiar with PowerShell cmdlets in order to define, validate, or edit information barrier policies.</span></span> <span data-ttu-id="9f4e0-147">[방법 정보](information-barriers-policies.md)에 PowerShell cmdlet의 몇 가지 예를 제공 하지만, 조직에 대 한 매개 변수 등의 추가 정보를 파악 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f4e0-147">Although we provide several examples of PowerShell cmdlets in the [how-to information](information-barriers-policies.md), you'll need to know additional details, such as parameters, for your organization.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9f4e0-148">다음 단계</span><span class="sxs-lookup"><span data-stu-id="9f4e0-148">Next steps</span></span>

- [<span data-ttu-id="9f4e0-149">Microsoft 팀의 정보 장벽에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="9f4e0-149">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)
- [<span data-ttu-id="9f4e0-150">정보 장벽 정책에 사용할 수 있는 특성 확인</span><span class="sxs-lookup"><span data-stu-id="9f4e0-150">See the attributes that can be used for information barrier policies</span></span>](information-barriers-attributes.md)
- [<span data-ttu-id="9f4e0-151">정보 장벽에 대 한 정책 정의</span><span class="sxs-lookup"><span data-stu-id="9f4e0-151">Define policies for information barriers</span></span>](information-barriers-policies.md) 

