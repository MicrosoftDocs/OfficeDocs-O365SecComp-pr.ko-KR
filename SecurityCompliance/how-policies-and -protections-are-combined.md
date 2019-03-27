---
title: 메일을 빨간색으로 플래그 지정 했을 때 정책 및 보호 기능 결합 방법
description: 전자 메일이 맬웨어, 스팸, 높은 신뢰도 스팸, 피싱, EOP 및/또는 ATP에 의해 대량으로 표시 될 때 적용 되는 정책 및 수행 해야 하는 작업을 설명 합니다.
keywords: 보안, 맬웨어, Microsoft 365, M365, 보안 센터, ATP, Windows Defender atp, Office 365 atp, Azure ATP
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.date: 03/26/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.openlocfilehash: 7aa0f89eed379273cb069cd65c083749a9552e91
ms.sourcegitcommit: a79eb9907759d4cd849c3f948695a9ff890b19bf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/26/2019
ms.locfileid: "30926473"
---
# <a name="what-policy-applies-when-multiple-protection-methods-and-detection-scans-run-on-your-email"></a><span data-ttu-id="a3eae-104">전자 메일에 대해 여러 보호 방법 및 검색 검사가 실행 될 때 적용 되는 정책</span><span class="sxs-lookup"><span data-stu-id="a3eae-104">What policy applies when multiple protection methods and detection scans run on your email</span></span>

<span data-ttu-id="a3eae-105">받는 메일에는 여러 형태의 보호 (예: EOP *및* ATP)가 플래그 지정 되어 있을 수 있으며, 스팸 *및* 피싱 등의 여러 검색 검사를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3eae-105">Potentially, your incoming mail may be flagged by multiple forms of protection (for example both EOP *and* ATP), and multiple detection scans (such as spam *and* phishing).</span></span> <span data-ttu-id="a3eae-106">atp 고객에 게는 atp 피싱 방지 정책, EOP 고객을 위한 EOP 피싱 방지 정책 등이 있기 때문에 이러한 일이 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3eae-106">This is possible because there are ATP Anti-phishing policies for ATP customers, and EOP Anti-phishing policies for EOP customers.</span></span> <span data-ttu-id="a3eae-107">또한이는 메시지가 맬웨어, 피싱 및 사용자 가장을 위해 여러 검색 검색을 탐색할 수도 있음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3eae-107">This also means the message may navigate multiple detection scans for malware, phishing, and user-impersonation, for example.</span></span> <span data-ttu-id="a3eae-108">이 모든 활동이 제공 되 면 어떤 정책이 적용 되는지 약간의 혼동이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3eae-108">Given all this activity, there may be some confusion as to which policy applies.</span></span>

<span data-ttu-id="a3eae-109">일반적으로 메시지에 적용 되는 정책은 **CAT (Category)** 속성의 **스팸 방지-Report** 헤더에서 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3eae-109">In general, the policy applied to a message is identified in the **X-Forefront-Antispam-Report** header in the **CAT (Category)** property.</span></span> <span data-ttu-id="a3eae-110">피싱 방지 정책이 여러 개 있는 경우 우선 순위가 가장 높은 정책 중 하나가 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3eae-110">If you have multiple Anti-phishing policies, the one at the highest priority will apply.</span></span>

<span data-ttu-id="a3eae-111">아래 정책은 _모든 조직_에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3eae-111">The Policies below apply to _all organizations_.</span></span>

|<span data-ttu-id="a3eae-112">우선 순위</span><span class="sxs-lookup"><span data-stu-id="a3eae-112">Priority</span></span> |<span data-ttu-id="a3eae-113">정책</span><span class="sxs-lookup"><span data-stu-id="a3eae-113">Policy</span></span>  |<span data-ttu-id="a3eae-114">범주</span><span class="sxs-lookup"><span data-stu-id="a3eae-114">Category</span></span>  |<span data-ttu-id="a3eae-115">관리 되는 위치</span><span class="sxs-lookup"><span data-stu-id="a3eae-115">Where Managed</span></span> |
|---------|---------|---------|---------|
|<span data-ttu-id="a3eae-116">개</span><span class="sxs-lookup"><span data-stu-id="a3eae-116">1</span></span>     | <span data-ttu-id="a3eae-117">맬웨어</span><span class="sxs-lookup"><span data-stu-id="a3eae-117">Malware</span></span>      | <span data-ttu-id="a3eae-118">MALW</span><span class="sxs-lookup"><span data-stu-id="a3eae-118">MALW</span></span>      | <span data-ttu-id="a3eae-119">맬웨어 정책</span><span class="sxs-lookup"><span data-stu-id="a3eae-119">Malware policy</span></span>   |
|<span data-ttu-id="a3eae-120">2</span><span class="sxs-lookup"><span data-stu-id="a3eae-120">2</span></span>     | <span data-ttu-id="a3eae-121">피싱</span><span class="sxs-lookup"><span data-stu-id="a3eae-121">Phishing</span></span>     | <span data-ttu-id="a3eae-122">PHSH</span><span class="sxs-lookup"><span data-stu-id="a3eae-122">PHSH</span></span>     | <span data-ttu-id="a3eae-123">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="a3eae-123">Configure your spam filter policies</span></span>     |
|<span data-ttu-id="a3eae-124">3(sp3)</span><span class="sxs-lookup"><span data-stu-id="a3eae-124">3</span></span>     | <span data-ttu-id="a3eae-125">높은 정확도 스팸</span><span class="sxs-lookup"><span data-stu-id="a3eae-125">High confidence spam</span></span>      | <span data-ttu-id="a3eae-126">HSPM</span><span class="sxs-lookup"><span data-stu-id="a3eae-126">HSPM</span></span>        | <span data-ttu-id="a3eae-127">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="a3eae-127">Configure your spam filter policies</span></span>        |
|<span data-ttu-id="a3eae-128">1-4</span><span class="sxs-lookup"><span data-stu-id="a3eae-128">4</span></span>     | <span data-ttu-id="a3eae-129">스푸핑</span><span class="sxs-lookup"><span data-stu-id="a3eae-129">Spoofing</span></span>        | <span data-ttu-id="a3eae-130">스푸핑</span><span class="sxs-lookup"><span data-stu-id="a3eae-130">SPOOF</span></span>        | <span data-ttu-id="a3eae-131">피싱 방지 정책, 스푸핑 인텔리전스</span><span class="sxs-lookup"><span data-stu-id="a3eae-131">Anti-phishing policy, spoof intelligence</span></span>        |
|<span data-ttu-id="a3eae-132">2-5</span><span class="sxs-lookup"><span data-stu-id="a3eae-132">5</span></span>     | <span data-ttu-id="a3eae-133">스팸</span><span class="sxs-lookup"><span data-stu-id="a3eae-133">Spam</span></span>         | <span data-ttu-id="a3eae-134">SPM</span><span class="sxs-lookup"><span data-stu-id="a3eae-134">SPM</span></span>         | <span data-ttu-id="a3eae-135">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="a3eae-135">Configure your spam filter policies</span></span>         |
|<span data-ttu-id="a3eae-136">번</span><span class="sxs-lookup"><span data-stu-id="a3eae-136">6</span></span>     | <span data-ttu-id="a3eae-137">대량</span><span class="sxs-lookup"><span data-stu-id="a3eae-137">Bulk</span></span>         | <span data-ttu-id="a3eae-138">대량</span><span class="sxs-lookup"><span data-stu-id="a3eae-138">BULK</span></span>        | <span data-ttu-id="a3eae-139">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="a3eae-139">Configure your spam filter policies</span></span>         |

<span data-ttu-id="a3eae-140">또한 이러한 정책은 _ATP가 있는 조직_에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3eae-140">In addition, these policies apply to _organizations with ATP_.</span></span>

|<span data-ttu-id="a3eae-141">우선 순위</span><span class="sxs-lookup"><span data-stu-id="a3eae-141">Priority</span></span> |<span data-ttu-id="a3eae-142">정책</span><span class="sxs-lookup"><span data-stu-id="a3eae-142">Policy</span></span>  |<span data-ttu-id="a3eae-143">범주</span><span class="sxs-lookup"><span data-stu-id="a3eae-143">Category</span></span>  |<span data-ttu-id="a3eae-144">관리 되는 위치</span><span class="sxs-lookup"><span data-stu-id="a3eae-144">Where Managed</span></span> |
|---------|---------|---------|---------|
|<span data-ttu-id="a3eae-145">연중</span><span class="sxs-lookup"><span data-stu-id="a3eae-145">7</span></span>     | <span data-ttu-id="a3eae-146">도메인 가장</span><span class="sxs-lookup"><span data-stu-id="a3eae-146">Domain Impersonation</span></span>         | <span data-ttu-id="a3eae-147">DIMP</span><span class="sxs-lookup"><span data-stu-id="a3eae-147">DIMP</span></span>         | <span data-ttu-id="a3eae-148">Office 365 ATP 피싱 방지 및 피싱 방지 정책 설정</span><span class="sxs-lookup"><span data-stu-id="a3eae-148">Set up Office 365 ATP anti-phishing and anti-phishing policies</span></span>        |
|<span data-ttu-id="a3eae-149">8</span><span class="sxs-lookup"><span data-stu-id="a3eae-149">8</span></span>     | <span data-ttu-id="a3eae-150">사용자 가장</span><span class="sxs-lookup"><span data-stu-id="a3eae-150">User Impersonation</span></span>        | <span data-ttu-id="a3eae-151">UIMP</span><span class="sxs-lookup"><span data-stu-id="a3eae-151">UIMP</span></span>         | <span data-ttu-id="a3eae-152">Office 365 ATP 피싱 방지 및 피싱 방지 정책 설정</span><span class="sxs-lookup"><span data-stu-id="a3eae-152">Set up Office 365 ATP anti-phishing and anti-phishing policies</span></span>         |

<span data-ttu-id="a3eae-153">예를 들어 두 개의 정책이 있는 경우 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3eae-153">As an example, if you have two policies:</span></span>

|<span data-ttu-id="a3eae-154">정책</span><span class="sxs-lookup"><span data-stu-id="a3eae-154">Policy</span></span>  |<span data-ttu-id="a3eae-155">우선 순위</span><span class="sxs-lookup"><span data-stu-id="a3eae-155">Priority</span></span>  |<span data-ttu-id="a3eae-156">사용자/도메인 가장</span><span class="sxs-lookup"><span data-stu-id="a3eae-156">User/Domain Impersonation</span></span>  |<span data-ttu-id="a3eae-157">스푸핑 방지</span><span class="sxs-lookup"><span data-stu-id="a3eae-157">Anti-spoofing</span></span>  |
|---------|---------|---------|---------|
|<span data-ttu-id="a3eae-158">A</span><span class="sxs-lookup"><span data-stu-id="a3eae-158">A</span></span>     | <span data-ttu-id="a3eae-159">개</span><span class="sxs-lookup"><span data-stu-id="a3eae-159">1</span></span>        | <span data-ttu-id="a3eae-160">켜짐</span><span class="sxs-lookup"><span data-stu-id="a3eae-160">On</span></span>        |<span data-ttu-id="a3eae-161">해제</span><span class="sxs-lookup"><span data-stu-id="a3eae-161">Off</span></span>         |
|<span data-ttu-id="a3eae-162">B</span><span class="sxs-lookup"><span data-stu-id="a3eae-162">B</span></span>     | <span data-ttu-id="a3eae-163">2</span><span class="sxs-lookup"><span data-stu-id="a3eae-163">2</span></span>        | <span data-ttu-id="a3eae-164">해제</span><span class="sxs-lookup"><span data-stu-id="a3eae-164">Off</span></span>        | <span data-ttu-id="a3eae-165">켜짐</span><span class="sxs-lookup"><span data-stu-id="a3eae-165">On</span></span>        |

<span data-ttu-id="a3eae-166">메시지가 _사용자 가장_ 및 _스푸핑_ (위의 표에 나오는 스푸핑 방지 참조)으로 식별 되 고 정책 a로 범위가 지정 된 동일한 사용자 집합에 정책 B가 적용 되 면 해당 메시지의 플래그를 설정 하 고 _위장_로 취급 하지만이는 그렇지 않습니다. 스푸핑 방지 기능이 해제 되어 있고 **스푸핑이 보다 높은 우선 순위 (8)에서 실행**되므로 작업이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3eae-166">If a message comes in identified as both _user impersonation_ and _spoofing_ (see anti-spoofing in the table above), and the same set of users scoped to policy A is scoped to policy B, then the message is flagged and treated as a _spoof_, but no action is applied since Anti-spoofing is turned off, and because **spoof runs at a higher priority (4) than User Impersonation (8)**.</span></span>

<span data-ttu-id="a3eae-167">다른 유형의 피싱 정책이 적용 되도록 하려면 다양 한 정책이 적용 되는 사용자의 설정을 조정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3eae-167">To make other types of phishing policy apply, you will need to adjust the settings of who the various policies apply to.</span></span>



