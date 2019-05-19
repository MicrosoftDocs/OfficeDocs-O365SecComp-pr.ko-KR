---
title: 규정 준수 점수 방법론
ms.author: robmazz
author: robmazz
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Microsoft 준수 관리자는 Microsoft Service Trust Portal의 무료 워크플로 기반 위험 평가 도구입니다. 준수 관리자를 사용 하면 Microsoft 클라우드 서비스와 관련 된 규정 준수 활동을 추적, 할당 및 확인할 수 있습니다.
ms.openlocfilehash: 5d59ef322fc9b5686d16230cb59ae141cd338090
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155260"
---
# <a name="compliance-score-methodology-preview"></a><span data-ttu-id="b6bb0-104">준수 점수 방법론 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="b6bb0-104">Compliance Score Methodology (Preview)</span></span>

> [!NOTE]
> <span data-ttu-id="b6bb0-p102">준수 점수는 특정 표준 및 규정에 대해 조직 차원의 규정 준수에 대한 절대 측정 결과를 나타내지 않습니다. 개인 데이터 및 개별 개인 정보 보호에 대한 위험을 줄일 수 있는 컨트롤 채택 수준을 나타냅니다. 사용자의 표준 또는 규정 준수를 보장하는 서비스는 없으며, 준수 점수는 어떤 경우든 준수 보장으로 해셕되면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-p102">The Compliance Score does not express an absolute measure of organizational compliance with any particular standard or regulation. It expresses the extent to which you have adopted controls which can reduce the risks to personal data and individual privacy. No service can guarantee that you are compliant with a standard or regulation, and the Compliance Score should not be interpreted as a guarantee in any way.</span></span>

<span data-ttu-id="b6bb0-108">준수 관리자 대시보드에는 각 평가 타일의 평가에 대 한 총 준수 점수가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-108">The Compliance Manager dashboard displays a total compliance score for Assessments in each Assessment tile.</span></span> <span data-ttu-id="b6bb0-109">이는 평가에 대 한 전반적인 준수 점수 이며 평가에서 각 구현 및 테스트 되는 제어에 대해 수신 되는 점수입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-109">This is the overall Compliance Score for the Assessment and is the accumulation of points received for each implemented and tested control in the Assessment.</span></span> <span data-ttu-id="b6bb0-110">새 평가를 위해 준수 점수에는 독립 타사에서 테스트 한 포함 된 Microsoft 관리 컨트롤에 대 한 초기 값이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-110">For a new Assessment, the Compliance Score has an initial value for the included Microsoft-managed controls tested by independent third parties.</span></span> <span data-ttu-id="b6bb0-111">규정 준수 점수는 전반적인 준수 상태를 개선 하기 위해 중점적으로 확인할 평가 및 제어에 대 한 우선 순위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-111">Compliance Score can help prioritize which Assessments and controls to focus on to improve your overall compliance posture.</span></span>

<span data-ttu-id="b6bb0-112">컨트롤에 대해 표시 되는 규정 준수 점수 값은 합격/불합격에 따라 전체 준수 점수에 *전체적* 으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-112">The displayed Compliance Score values for the control are applied *in their entirety* to the total Compliance Score on a pass/fail basis.</span></span> <span data-ttu-id="b6bb0-113">컨트롤이 구현 되 고 후속 평가 테스트를 통과 하거나 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-113">Either the control is implemented and passes the subsequent assessment test or it does not.</span></span> <span data-ttu-id="b6bb0-114">부분 시행에는 부분적인 크레딧이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-114">There is no partial credit for a partial implementation.</span></span> <span data-ttu-id="b6bb0-115">지정 된 점은 컨트롤의 준수 점수에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-115">Assigned points are added to the Compliance Score when the Control has:</span></span>

- <span data-ttu-id="b6bb0-116">**구현 상태** 는 **구현** 됨 또는 **대체 구현과** 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-116">**Implementation Status** equals **Implemented** or **Alternative Implementation** and,</span></span>
- <span data-ttu-id="b6bb0-117">**테스트 결과가** **통과**됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-117">**Test Result** equals **Passed**.</span></span>

## <a name="compliance-score"></a><span data-ttu-id="b6bb0-118">준수 점수</span><span class="sxs-lookup"><span data-stu-id="b6bb0-118">Compliance score</span></span>
  
<span data-ttu-id="b6bb0-119">준수 관리자에서는 초기 점수를 컨트롤 수준에서 작업 항목 수준으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-119">In Compliance Manager, baseline scores move from the Control level to the Action Item level.</span></span> <span data-ttu-id="b6bb0-120">점수는 작업 항목의 용도 (예방용 인지, 예방적 또는 정정) 및 적용 (임의 또는 필수)을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-120">Scores are based on the purpose (Detective, Preventative, or Corrective) and enforcement (Discretionary or Mandatory) of the Action Item.</span></span>

<span data-ttu-id="b6bb0-121">작업 항목은 컨트롤에 매핑되며, 컨트롤이 여러 작업 항목에 매핑되는 경우에는 작업 항목 점수의 합계가 컨트롤 점수에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-121">Action Items are mapped to Controls, and when a Control is mapped to multiple Action Items, the sum of the Action Item Scores is the Control Score.</span></span> <span data-ttu-id="b6bb0-122">지정 된 평가에서 모든 컨트롤의 컨트롤 점수를 합한 값은 평가 점수입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-122">The sum of the Control Score for all Controls in a given Assessment is the Assessment Score.</span></span> <span data-ttu-id="b6bb0-123">그룹에 있는 모든 평가의 평균 점수는 해당 그룹에 대 한 준수 점수입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-123">The average score of all Assessments in a Group is the Compliance Score for that group.</span></span>
  
### <a name="mandatory-or-discretionary-controls"></a><span data-ttu-id="b6bb0-124">필수 또는 임의 컨트롤</span><span class="sxs-lookup"><span data-stu-id="b6bb0-124">Mandatory or discretionary Controls</span></span>
  
 <span data-ttu-id="b6bb0-125">**필수 컨트롤** 은 고의적으로 또는 실수로 건너뛸 수 없는 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-125">**Mandatory Controls** are Controls that cannot be bypassed either intentionally or accidentally.</span></span> <span data-ttu-id="b6bb0-126">일반적인 필수 제어의 예로는 암호 길이, 복잡성 및 만료에 대 한 요구 사항을 설정 하는 중앙 집중식으로 관리 되는 암호 정책이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-126">An example of a common mandatory control is a centrally managed password policy that sets requirements for password length, complexity, and expiration.</span></span> <span data-ttu-id="b6bb0-127">사용자는 이러한 요구 사항을 준수 하 여 시스템에 액세스 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-127">Users must comply with these requirements to access the system.</span></span>
  
 <span data-ttu-id="b6bb0-128">사용자는 **임의 컨트롤** 을 사용 하 여 정책을 이해 하 고 그에 따라 조치를 취할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-128">**Discretionary Controls** rely upon users to understand policy and act accordingly.</span></span> <span data-ttu-id="b6bb0-129">예를 들어 사용자가 자신의 컴퓨터를 사용 하는 경우 사용자에 게 의존 하므로 임의의 컨트롤을 잠그려고 하는 정책이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-129">For example, a policy requiring users to lock their computer when they leave it is a discretionary control because it relies on the user.</span></span>
  
### <a name="preventative-detective-or-corrective-controls"></a><span data-ttu-id="b6bb0-130">예방적, 예방용 인지 또는 교정 제어</span><span class="sxs-lookup"><span data-stu-id="b6bb0-130">Preventative, detective, or corrective Controls</span></span>
  
 <span data-ttu-id="b6bb0-131">**예방적 컨트롤** 은 특정 위험을 방지 하는 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-131">**Preventative Controls** are Controls that prevent specific risks.</span></span> <span data-ttu-id="b6bb0-132">예를 들어 암호화를 사용 하 여 rest에서 정보를 보호 하는 것은 공격, 침해에 대 한 예방 통제입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-132">For example, protecting information at rest using encryption is a preventative control against attacks, breaches.</span></span> <span data-ttu-id="b6bb0-133">의무를 분리 하는 것은 중요 한 충돌을 관리 하 고 사기 로부터 보호 하는 예방 조치입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-133">Separation of duties is a preventative control to manage conflict of interest and to guard against fraud.</span></span>
  
 <span data-ttu-id="b6bb0-134">**예방용 인지 컨트롤** 은 시스템을 적극적으로 모니터링 하 여 위험을 나타내는 불규칙 한 조건이 나 행동을 식별 하거나 침입을 탐지 하거나 위반이 발생 했는지를 확인 하는 데 사용할 수 있는 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-134">**Detective Controls** are Controls that actively monitor systems to identify irregular conditions or behaviors that represent risk or that can be used to detect intrusions or determine if a breach has occurred.</span></span> <span data-ttu-id="b6bb0-135">시스템 액세스 감사 및 권한 있는 관리 작업 감사는 예방용 인지 모니터링 컨트롤의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-135">System access auditing and privileged administrative actions auditing are types of detective monitoring controls.</span></span> <span data-ttu-id="b6bb0-136">규정 준수 감사는 프로세스 문제를 찾는 데 사용 되는 예방용 인지 제어 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-136">Regulatory compliance audits are a type of detective control used to find process issues.</span></span>
  
<span data-ttu-id="b6bb0-137">**정정 컨트롤** 은 보안 사고의 부정적 영향을 최소로 유지 하 고, 정정 작업을 수행 하 여 즉각적인 영향을 줄이고, 가능한 경우 피해를 되돌리는 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-137">**Corrective Controls** are Controls that try to keep the adverse effects of a security incident to a minimum, take corrective action to reduce the immediate effect, and reverse the damage, if possible.</span></span> <span data-ttu-id="b6bb0-138">개인 정보 보호 인시던트 응답은 손상을 제한 하 고 위반 후 시스템을 작동 상태로 복원 하는 정정 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-138">Privacy incident response is a corrective control to limit damage and restore systems to an operational state after a breach.</span></span>
  
<span data-ttu-id="b6bb0-139">각 컨트롤은 표시 되는 위험에 따라 준수 관리자에 게 할당 된 값을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-139">Each Control has an assigned value in Compliance Manager based on the risk that it represents:</span></span>

|<span data-ttu-id="b6bb0-140">**유형**</span><span class="sxs-lookup"><span data-stu-id="b6bb0-140">**Type**</span></span>|<span data-ttu-id="b6bb0-141">**할당 된 점수**</span><span class="sxs-lookup"><span data-stu-id="b6bb0-141">**Assigned Score**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b6bb0-142">예방적 필수</span><span class="sxs-lookup"><span data-stu-id="b6bb0-142">Preventative Mandatory</span></span> | <span data-ttu-id="b6bb0-143">kb(56kbps</span><span class="sxs-lookup"><span data-stu-id="b6bb0-143">27</span></span> |
| <span data-ttu-id="b6bb0-144">예방적 임의</span><span class="sxs-lookup"><span data-stu-id="b6bb0-144">Preventative Discretionary</span></span> | <span data-ttu-id="b6bb0-145">9 </span><span class="sxs-lookup"><span data-stu-id="b6bb0-145">9</span></span> |
| <span data-ttu-id="b6bb0-146">예방용 인지 필수</span><span class="sxs-lookup"><span data-stu-id="b6bb0-146">Detective Mandatory</span></span> | <span data-ttu-id="b6bb0-147">3(sp3)</span><span class="sxs-lookup"><span data-stu-id="b6bb0-147">3</span></span> |
| <span data-ttu-id="b6bb0-148">예방용 인지 임의</span><span class="sxs-lookup"><span data-stu-id="b6bb0-148">Detective Discretionary</span></span> | <span data-ttu-id="b6bb0-149">개</span><span class="sxs-lookup"><span data-stu-id="b6bb0-149">1</span></span> |
| <span data-ttu-id="b6bb0-150">정정 필수</span><span class="sxs-lookup"><span data-stu-id="b6bb0-150">Corrective Mandatory</span></span> | <span data-ttu-id="b6bb0-151">3(sp3)</span><span class="sxs-lookup"><span data-stu-id="b6bb0-151">3</span></span> |
| <span data-ttu-id="b6bb0-152">정정 임의</span><span class="sxs-lookup"><span data-stu-id="b6bb0-152">Corrective Discretionary</span></span> | <span data-ttu-id="b6bb0-153">개</span><span class="sxs-lookup"><span data-stu-id="b6bb0-153">1</span></span> |
  
## <a name="action-item-workflow"></a><span data-ttu-id="b6bb0-154">작업 항목 워크플로</span><span class="sxs-lookup"><span data-stu-id="b6bb0-154">Action Item workflow</span></span>

<span data-ttu-id="b6bb0-155">일반적인 작업 항목에 대 한 기본 워크플로는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-155">Here's the basic workflow for a typical Action Item:</span></span>
  
1. <span data-ttu-id="b6bb0-156">조직의 준수, 위험, 개인 정보 및/또는 데이터 보호 담당자가 조직의 다른 사용자에 게 작업을 할당 하 여 컨트롤을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-156">The Compliance, Risk, Privacy, and/or Data Protection Officer of an organization assigns a task to someone in the organization to implement a control.</span></span> <span data-ttu-id="b6bb0-157">해당 사용자는 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-157">That person could be:</span></span>

    - <span data-ttu-id="b6bb0-158">비즈니스 정책 소유자</span><span class="sxs-lookup"><span data-stu-id="b6bb0-158">A business policy owner.</span></span>
    - <span data-ttu-id="b6bb0-159">IT 구현자</span><span class="sxs-lookup"><span data-stu-id="b6bb0-159">An IT implementer.</span></span>
    - <span data-ttu-id="b6bb0-160">작업 수행을 담당 하는 조직의 다른 개인</span><span class="sxs-lookup"><span data-stu-id="b6bb0-160">Another individual in the organization with responsibility to perform the task.</span></span>

2. <span data-ttu-id="b6bb0-161">해당 개별 항목은 컨트롤을 구현 하는 데 필요한 작업을 수행 하 고, 구현 증거를 준수 관리자로 업로드 하며, 컨트롤을 구현 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-161">That individual performs the tasks necessary to implement the control, uploads evidence of implementation into Compliance Manager, and marks the Control tied to the Action Item as implemented.</span></span> <span data-ttu-id="b6bb0-162">이러한 작업을 완료 하면 유효성 검사를 위해 평가자에 작업 항목을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-162">Once these tasks are completed, they assign the Action Item to an Assessor for validation.</span></span>

    <span data-ttu-id="b6bb0-163">평가자 수 있는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-163">Assessors can be:</span></span>

    - <span data-ttu-id="b6bb0-164">조직 내에서 컨트롤의 유효성 검사를 수행 하는 내부 평가자.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-164">Internal assessors that perform validation of controls within an organization.</span></span>
    - <span data-ttu-id="b6bb0-165">Microsoft의 클라우드 서비스를 감사 하는 타사 독립적인 조직과 같은 규정 준수를 조사, 확인 및 인증 하는 외부 평가자</span><span class="sxs-lookup"><span data-stu-id="b6bb0-165">External assessors that examine, verify, and certify compliance, such as the third-party independent organizations that audit Microsoft's cloud services.</span></span>

3. <span data-ttu-id="b6bb0-166">평가자에서 컨트롤의 유효성을 검사 하 고 증거를 검사 하 고 해당 컨트롤을 평가로 표시 하 고 확인 결과를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-166">The Assessor validates the control and examines the evidence and marks the control as assessed and the results of the assessment.</span></span>

<span data-ttu-id="b6bb0-167">평가와 연결 된 모든 컨트롤이 평가 되 면 평가가 완료 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-167">Once all the Controls associated with an Assessment are assessed, the Assessment is complete.</span></span>