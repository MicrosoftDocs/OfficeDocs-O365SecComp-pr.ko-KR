---
title: 정보 장벽 개요
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: 정보 장애물을 사용 하 여 조직 내에서 Microsoft 팀을 사용 하 여 통신을 준수 하는지 확인 합니다.
ms.openlocfilehash: a2c202d08f1de60f92f13b2ac4c2b9d3c7f900e8
ms.sourcegitcommit: eeb51470d8996e93fac28d7f12c6117e2aeb0cf0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/14/2019
ms.locfileid: "34935940"
---
# <a name="information-barriers-preview"></a><span data-ttu-id="105e6-103">정보 장벽 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="105e6-103">Information barriers (Preview)</span></span>

## <a name="overview"></a><span data-ttu-id="105e6-104">개요</span><span class="sxs-lookup"><span data-stu-id="105e6-104">Overview</span></span>

<span data-ttu-id="105e6-105">Microsoft 클라우드 서비스에는 강력한 통신 및 공동 작업 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-105">Microsoft cloud services include powerful communication and collaboration capabilities.</span></span> <span data-ttu-id="105e6-106">하지만 조직에서 발생할 수 있는 충돌을 방지 하기 위해 두 그룹 간의 통신을 제한 하려는 경우를 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-106">But suppose that you want to restrict communications between two groups to avoid a conflict of interest from occurring in your organization.</span></span> <span data-ttu-id="105e6-107">아니면 내부 정보를 보호 하기 위해 조직 내부의 특정 사용자 간의 통신을 제한 하려는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-107">Or, perhaps you want to restrict communications between certain people inside your organization in order to safeguard internal information.</span></span> <span data-ttu-id="105e6-108">Microsoft 365을 사용 하면 그룹 및 조직에서 통신 및 공동 작업을 수행할 수 있으므로 필요한 경우 특정 사용자 그룹 간에 통신을 제한할 수 있는 방법이 있나요?</span><span class="sxs-lookup"><span data-stu-id="105e6-108">Microsoft 365 enables communication and collaboration across groups and organizations, so is there a way to restrict communications among specific groups of users when necessary?</span></span> <span data-ttu-id="105e6-109">정보 장벽에서는 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-109">With information barriers, you can!</span></span> 

<span data-ttu-id="105e6-110">정보 장애물은 지금 미리 볼 수 있습니다 (Microsoft 팀부터 시작).</span><span class="sxs-lookup"><span data-stu-id="105e6-110">Information barriers are in preview now, beginning with Microsoft Teams.</span></span> <span data-ttu-id="105e6-111">조직에서 이러한 기능을 사용할 수 있는 경우 준수 관리자 또는 정보 장벽 관리자는 Microsoft 팀의 사용자 그룹 간 통신을 허용 하거나 차단 하는 정책을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-111">When these features are available for your organization, a compliance administrator or information barriers administrator can define policies to allow or prevent communications between groups of users in Microsoft Teams.</span></span> <span data-ttu-id="105e6-112">정보 장벽 정책은 다음과 같은 경우에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-112">Information barrier policies can be used for situations like these:</span></span>

- <span data-ttu-id="105e6-113">하루 상인은 마케팅 팀에서 다른 사람에 게 전화를 걸 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-113">A day trader cannot call someone on the marketing team</span></span>
- <span data-ttu-id="105e6-114">기밀 회사 정보에 대 한 작업을 수행 하는 금융 직원은 조직 내의 특정 그룹에서 전화를 받을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-114">Finance personnel working on confidential company information cannot receive calls from certain groups within their organization</span></span>
- <span data-ttu-id="105e6-115">영업 비밀 자료가 있는 내부 팀이 조직 내의 특정 그룹에 있는 사용자와 통화 하거나 온라인으로 대화할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-115">An internal team with trade secret material cannot call or chat online with people in certain groups within their organization</span></span>
- <span data-ttu-id="105e6-116">연구 팀은 제품 개발 팀과 온라인 으로만 전화를 걸어 대화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-116">A research team can only call or chat online with a product development team</span></span>

<span data-ttu-id="105e6-117">이러한 모든 시나리오 (및 이상)에서 정보 장벽 정책은 Microsoft 팀의 통신을 방지 하거나 허용 하도록 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-117">For all of these example scenarios (and more), information barrier policies can be defined to prevent or allow communications in Microsoft Teams.</span></span> <span data-ttu-id="105e6-118">이러한 정책을 사용 하면 사용자가 전화를 걸 수도 있고 채팅을 할 수 없거나, 사용자가 Microsoft 팀의 특정 그룹과 통신 하는 것을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-118">Such policies can prevent people from calling or chatting with those they shouldn't, or enable people to communicate only with specific groups in Microsoft Teams.</span></span> <span data-ttu-id="105e6-119">정보 장벽 정책을 적용 하면 해당 정책에 포함 된 사용자가 Microsoft 팀의 다른 사람들과 통신을 시도할 때마다 정보 장벽 정책에 정의 된 대로 통신을 방지 하거나 허용 하기 위해 검사가 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-119">With information barrier policies in effect, whenever users who are covered by those policies attempt to communicate with others in Microsoft Teams, checks are done to prevent (or allow) communication (as defined by information barrier policies).</span></span> <span data-ttu-id="105e6-120">정보 장벽에 대 한 사용자 환경에 대 한 자세한 내용은 [Microsoft 팀의 정보 장벽](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="105e6-120">To learn more about the user experience with information barriers, see [information barriers in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).</span></span>

> [!NOTE]
> <span data-ttu-id="105e6-121">정보 장애물은 SharePoint Online 또는 OneDrive를 통한 전자 메일 통신 또는 파일 공유에는 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-121">Information barriers will not apply to email communications or to file sharing through SharePoint Online or OneDrive.</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="105e6-122">필요한 라이선스 및 사용 권한</span><span class="sxs-lookup"><span data-stu-id="105e6-122">Required licenses and permissions</span></span>

<span data-ttu-id="105e6-123">**현재 정보 장벽 기능은 개인 미리 보기에**있습니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-123">**Currently, the information barrier feature is in private preview**.</span></span> <span data-ttu-id="105e6-124">일반적으로 이러한 기능을 사용할 수 있는 경우 다음과 같은 구독에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-124">When these features are generally available, they'll be included in subscriptions, such as:</span></span>

- <span data-ttu-id="105e6-125">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="105e6-125">Microsoft 365 E5</span></span>
- <span data-ttu-id="105e6-126">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="105e6-126">Office 365 E5</span></span>
- <span data-ttu-id="105e6-127">Office 365 Advanced Compliance</span><span class="sxs-lookup"><span data-stu-id="105e6-127">Office 365 Advanced Compliance</span></span>
- <span data-ttu-id="105e6-128">Microsoft 365 E5 정보 보호 및 규정 준수</span><span class="sxs-lookup"><span data-stu-id="105e6-128">Microsoft 365 E5 Information Protection and Compliance</span></span>

<span data-ttu-id="105e6-129">자세한 내용은 [준수 솔루션](https://products.office.com/business/security-and-compliance/compliance-solutions)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="105e6-129">For more details, see [Compliance Solutions](https://products.office.com/business/security-and-compliance/compliance-solutions).</span></span>

<span data-ttu-id="105e6-130">[정보 장벽 정책을 정의 하거나 편집](information-barriers-policies.md)하려면 다음 역할 중 하나를 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-130">To [define or edit information barrier policies](information-barriers-policies.md), you must be assigned one of the following roles:</span></span>

- <span data-ttu-id="105e6-131">Microsoft 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="105e6-131">Microsoft 365 global administrator</span></span>
- <span data-ttu-id="105e6-132">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="105e6-132">Office 365 global administrator</span></span>
- <span data-ttu-id="105e6-133">준수 관리자</span><span class="sxs-lookup"><span data-stu-id="105e6-133">Compliance administrator</span></span>
- <span data-ttu-id="105e6-134">정보 장벽 관리자</span><span class="sxs-lookup"><span data-stu-id="105e6-134">Information barriers administrator</span></span>

<span data-ttu-id="105e6-135">정보 장벽 정책을 정의, 유효성 검사 또는 편집 하려면 PowerShell cmdlet을 잘 알고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-135">You must be familiar with PowerShell cmdlets in order to define, validate, or edit information barrier policies.</span></span> <span data-ttu-id="105e6-136">[방법 정보](information-barriers-policies.md)에 PowerShell cmdlet의 몇 가지 예를 제공 하지만, 조직에 대 한 매개 변수 등의 추가 정보를 파악 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="105e6-136">Although we provide several examples of PowerShell cmdlets in the [how-to information](information-barriers-policies.md), you'll need to know additional details, such as parameters, for your organization.</span></span>

## <a name="next-steps"></a><span data-ttu-id="105e6-137">다음 단계</span><span class="sxs-lookup"><span data-stu-id="105e6-137">Next steps</span></span>

- [<span data-ttu-id="105e6-138">Microsoft 팀의 정보 장벽에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="105e6-138">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)
- [<span data-ttu-id="105e6-139">정보 장벽 정책에 사용할 수 있는 특성 확인</span><span class="sxs-lookup"><span data-stu-id="105e6-139">See the attributes that can be used for information barrier policies</span></span>](information-barriers-attributes.md)
- [<span data-ttu-id="105e6-140">정보 장벽에 대 한 정책 정의</span><span class="sxs-lookup"><span data-stu-id="105e6-140">Define policies for information barriers</span></span>](information-barriers-policies.md) 

