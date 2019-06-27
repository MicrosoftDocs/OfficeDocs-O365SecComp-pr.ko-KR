---
title: 정보 장벽 개요
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/26/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: 정보 장애물을 사용 하 여 조직 내에서 Microsoft 팀을 사용 하 여 통신을 준수 하는지 확인 합니다.
ms.openlocfilehash: 6565fc28d70ac6ff9a6f4df6edc75b89d19ae29a
ms.sourcegitcommit: 1c254108c522d0cb44023565268b5041d07748aa
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/27/2019
ms.locfileid: "35279476"
---
# <a name="information-barriers-preview"></a><span data-ttu-id="98d66-103">정보 장벽 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="98d66-103">Information barriers (Preview)</span></span>

## <a name="overview"></a><span data-ttu-id="98d66-104">개요</span><span class="sxs-lookup"><span data-stu-id="98d66-104">Overview</span></span>

<span data-ttu-id="98d66-105">Microsoft 클라우드 서비스에는 강력한 통신 및 공동 작업 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-105">Microsoft cloud services include powerful communication and collaboration capabilities.</span></span> <span data-ttu-id="98d66-106">하지만 조직에서 발생할 수 있는 충돌을 방지 하기 위해 두 그룹 간의 통신을 제한 하려는 경우를 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-106">But suppose that you want to restrict communications between two groups to avoid a conflict of interest from occurring in your organization.</span></span> <span data-ttu-id="98d66-107">아니면 내부 정보를 보호 하기 위해 조직 내부의 특정 사용자 간의 통신을 제한 하려는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-107">Or, perhaps you want to restrict communications between certain people inside your organization in order to safeguard internal information.</span></span> <span data-ttu-id="98d66-108">Microsoft 365을 사용 하면 그룹 및 조직에서 통신 및 공동 작업을 수행할 수 있으므로 필요한 경우 특정 사용자 그룹 간에 통신을 제한할 수 있는 방법이 있나요?</span><span class="sxs-lookup"><span data-stu-id="98d66-108">Microsoft 365 enables communication and collaboration across groups and organizations, so is there a way to restrict communications among specific groups of users when necessary?</span></span> <span data-ttu-id="98d66-109">정보 장벽에서는 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-109">With information barriers, you can!</span></span> 

<span data-ttu-id="98d66-110">정보 장애물은 지금 미리 볼 수 있습니다 (Microsoft 팀부터 시작).</span><span class="sxs-lookup"><span data-stu-id="98d66-110">Information barriers are in preview now, beginning with Microsoft Teams.</span></span> <span data-ttu-id="98d66-111">조직에서 이러한 기능을 사용할 수 있는 경우 준수 관리자 또는 정보 장벽 관리자는 Microsoft 팀의 사용자 그룹 간 통신을 허용 하거나 차단 하는 정책을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-111">When these features are available for your organization, a compliance administrator or information barriers administrator can define policies to allow or prevent communications between groups of users in Microsoft Teams.</span></span> <span data-ttu-id="98d66-112">정보 장벽 정책은 다음과 같은 경우에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-112">Information barrier policies can be used for situations like these:</span></span>

- <span data-ttu-id="98d66-113">하루 상인은 마케팅 팀에서 다른 사람에 게 전화를 걸 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-113">A day trader cannot call someone on the marketing team</span></span>
- <span data-ttu-id="98d66-114">기밀 회사 정보에 대 한 작업을 수행 하는 금융 직원은 조직 내의 특정 그룹에서 전화를 받을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-114">Finance personnel working on confidential company information cannot receive calls from certain groups within their organization</span></span>
- <span data-ttu-id="98d66-115">영업 비밀 자료가 있는 내부 팀이 조직 내의 특정 그룹에 있는 사용자와 통화 하거나 온라인으로 대화할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-115">An internal team with trade secret material cannot call or chat online with people in certain groups within their organization</span></span>
- <span data-ttu-id="98d66-116">연구 팀은 제품 개발 팀과 온라인 으로만 전화를 걸어 대화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-116">A research team can only call or chat online with a product development team</span></span>

<span data-ttu-id="98d66-117">이러한 모든 시나리오 (및 이상)에서 정보 장벽 정책은 Microsoft 팀의 통신을 방지 하거나 허용 하도록 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-117">For all of these example scenarios (and more), information barrier policies can be defined to prevent or allow communications in Microsoft Teams.</span></span> <span data-ttu-id="98d66-118">이러한 정책을 사용 하면 사용자가 전화를 걸 수도 있고 채팅을 할 수 없거나, 사용자가 Microsoft 팀의 특정 그룹과 통신 하는 것을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-118">Such policies can prevent people from calling or chatting with those they shouldn't, or enable people to communicate only with specific groups in Microsoft Teams.</span></span> <span data-ttu-id="98d66-119">정보 장벽 정책을 적용 하면 해당 정책에 포함 된 사용자가 Microsoft 팀의 다른 사람들과 통신을 시도할 때마다 정보 장벽 정책에 정의 된 대로 통신을 방지 하거나 허용 하기 위해 검사가 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-119">With information barrier policies in effect, whenever users who are covered by those policies attempt to communicate with others in Microsoft Teams, checks are done to prevent (or allow) communication (as defined by information barrier policies).</span></span> <span data-ttu-id="98d66-120">정보 장벽에 대 한 사용자 환경에 대 한 자세한 내용은 [Microsoft 팀의 정보 장벽](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="98d66-120">To learn more about the user experience with information barriers, see [information barriers in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).</span></span>

> [!NOTE]
> <span data-ttu-id="98d66-121">정보 장애물은 SharePoint Online 또는 OneDrive를 통한 전자 메일 통신 또는 파일 공유에는 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-121">Information barriers do not apply to email communications or to file sharing through SharePoint Online or OneDrive.</span></span> <span data-ttu-id="98d66-122">또한 정보 장애물은 [준수 경계](set-up-compliance-boundaries.md)와는 별개입니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-122">In addition, information barriers are independent from [compliance boundaries](set-up-compliance-boundaries.md).</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="98d66-123">필요한 라이선스 및 사용 권한</span><span class="sxs-lookup"><span data-stu-id="98d66-123">Required licenses and permissions</span></span>

<span data-ttu-id="98d66-124">**현재 정보 장벽 기능은 개인 미리 보기에**있습니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-124">**Currently, the information barrier feature is in private preview**.</span></span> <span data-ttu-id="98d66-125">일반적으로 이러한 기능을 사용할 수 있는 경우 다음과 같은 구독에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-125">When these features are generally available, they'll be included in subscriptions, such as:</span></span>

- <span data-ttu-id="98d66-126">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="98d66-126">Microsoft 365 E5</span></span>
- <span data-ttu-id="98d66-127">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="98d66-127">Office 365 E5</span></span>
- <span data-ttu-id="98d66-128">Office 365 Advanced Compliance</span><span class="sxs-lookup"><span data-stu-id="98d66-128">Office 365 Advanced Compliance</span></span>
- <span data-ttu-id="98d66-129">Microsoft 365 E5 정보 보호 및 규정 준수</span><span class="sxs-lookup"><span data-stu-id="98d66-129">Microsoft 365 E5 Information Protection and Compliance</span></span>

<span data-ttu-id="98d66-130">자세한 내용은 [준수 솔루션](https://products.office.com/business/security-and-compliance/compliance-solutions)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="98d66-130">For more details, see [Compliance Solutions](https://products.office.com/business/security-and-compliance/compliance-solutions).</span></span>

<span data-ttu-id="98d66-131">[정보 장벽 정책을 정의 하거나 편집](information-barriers-policies.md)하려면 다음 역할 중 하나를 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-131">To [define or edit information barrier policies](information-barriers-policies.md), you must be assigned one of the following roles:</span></span>

- <span data-ttu-id="98d66-132">Microsoft 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="98d66-132">Microsoft 365 global administrator</span></span>
- <span data-ttu-id="98d66-133">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="98d66-133">Office 365 global administrator</span></span>
- <span data-ttu-id="98d66-134">준수 관리자</span><span class="sxs-lookup"><span data-stu-id="98d66-134">Compliance administrator</span></span>
- <span data-ttu-id="98d66-135">정보 장벽 관리자</span><span class="sxs-lookup"><span data-stu-id="98d66-135">Information barriers administrator</span></span>

<span data-ttu-id="98d66-136">정보 장벽 정책을 정의, 유효성 검사 또는 편집 하려면 PowerShell cmdlet을 잘 알고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-136">You must be familiar with PowerShell cmdlets in order to define, validate, or edit information barrier policies.</span></span> <span data-ttu-id="98d66-137">[방법 정보](information-barriers-policies.md)에 PowerShell cmdlet의 몇 가지 예를 제공 하지만, 조직에 대 한 매개 변수 등의 추가 정보를 파악 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-137">Although we provide several examples of PowerShell cmdlets in the [how-to information](information-barriers-policies.md), you'll need to know additional details, such as parameters, for your organization.</span></span>

## <a name="concepts-of-information-barrier-policies"></a><span data-ttu-id="98d66-138">정보 장벽 정책의 개념</span><span class="sxs-lookup"><span data-stu-id="98d66-138">Concepts of information barrier policies</span></span>

<span data-ttu-id="98d66-139">정보 장벽 정책의 기본 개념을 이해 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-139">It's helpful to know the underlying concepts of information barrier policies:</span></span>

- <span data-ttu-id="98d66-140">**사용자 계정 특성** 은 Azure Active Directory (또는 Exchange Online)에서 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-140">**User account attributes** are defined in Azure Active Directory (or Exchange Online).</span></span> <span data-ttu-id="98d66-141">이러한 특성에는 부서, 직함, 위치, 팀 이름 및 기타 작업 프로필 정보가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-141">These attributes can include department, job title, location, team name, and other job profile details.</span></span> 

- <span data-ttu-id="98d66-142">**세그먼트** 는 선택한 **사용자 계정 특성**을 사용 하 여 Office 365 보안 & 준수 센터에 정의 된 사용자 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-142">**Segments** are sets of users that are defined in the Office 365 Security & Compliance Center using a selected **user account attribute**.</span></span> <span data-ttu-id="98d66-143">( [지원 되는 특성 목록](information-barriers-attributes.md)참조)</span><span class="sxs-lookup"><span data-stu-id="98d66-143">(See the [list of supported attributes](information-barriers-attributes.md).)</span></span> 

- <span data-ttu-id="98d66-144">**정보 장벽 정책** 에 따라 통신 제한 또는 제한이 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-144">**Information barrier policies** determine communication limits or restrictions.</span></span> <span data-ttu-id="98d66-145">정보 장벽 정책을 정의할 때는 두 가지 정책 유형 중에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-145">When you define information barrier policies, you choose from two kinds of policies:</span></span>
    - <span data-ttu-id="98d66-146">"차단" 정책은 한 세그먼트가 다른 세그먼트와 통신 하지 못하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-146">"Block" policies prevent one segment from communicating with another segment.</span></span>
    - <span data-ttu-id="98d66-147">"허용" 정책은 한 세그먼트가 다른 특정 세그먼트와도 통신할 수 있도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-147">"Allow" policies allow one segment to communicate with only certain other segments.</span></span>

- <span data-ttu-id="98d66-148">**정책 응용 프로그램** 은 모든 정보 장벽 정책이 정의 된 후에 수행 되며, 조직에 적용할 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="98d66-148">**Policy application** is done after all information barrier policies are defined, and you are ready to apply them in your organization.</span></span>

## <a name="next-steps"></a><span data-ttu-id="98d66-149">다음 단계</span><span class="sxs-lookup"><span data-stu-id="98d66-149">Next steps</span></span>

- [<span data-ttu-id="98d66-150">Microsoft 팀의 정보 장벽에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="98d66-150">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)
- [<span data-ttu-id="98d66-151">정보 장벽 정책에 사용할 수 있는 특성 확인</span><span class="sxs-lookup"><span data-stu-id="98d66-151">See the attributes that can be used for information barrier policies</span></span>](information-barriers-attributes.md)
- [<span data-ttu-id="98d66-152">정보 장벽에 대 한 정책 정의</span><span class="sxs-lookup"><span data-stu-id="98d66-152">Define policies for information barriers</span></span>](information-barriers-policies.md) 

