---
title: Office 365의 자동화 된 조사 및 응답 (AIR)
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 06/25/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Office 365 Advanced Threat Protection의 자동화 된 조사 및 응답 기능에 대해 알아봅니다.
ms.openlocfilehash: 3e74fd7a12727880164797f076d254416325713a
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598524"
---
# <a name="automated-investigation-and-response-air-with-office-365"></a><span data-ttu-id="d3776-103">Office 365의 자동화 된 조사 및 응답 (AIR)</span><span class="sxs-lookup"><span data-stu-id="d3776-103">Automated Investigation and Response (AIR) with Office 365</span></span>

<span data-ttu-id="d3776-104">자동 조사 및 응답 (AIR) (현재 공개 미리 보기는 많은 [Office 365 위협 조사 및 응답 기능](office-365-ti.md)중 하나로 제공 됨)을 통해 오늘 존재 하는 잘 알려진 위협에 대해 자동화 된 조사 및 수정을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-104">Automated Investigation and Response (AIR) (currently in public preview as one of many [Office 365 Threat investigation and response capabilities](office-365-ti.md)) enables you to run automated investigation and remediation to well-known threats that exist today.</span></span> <span data-ttu-id="d3776-105">이 문서를 읽으면 AIR의 개요를 확인 하 고 조직 및 보안 운영 팀이 위협을 보다 효율적이 고 효율적으로 완화 하는 데 도움을 주는 방법을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-105">Read this article to get an overview of AIR and how it can help your organization and security operations teams mitigate threats more effectively and efficiently.</span></span> 

<span data-ttu-id="d3776-106">AIR 기능을 사용할 수 있는 경우에 대 한 자세한 내용은 [Microsoft 365 로드맵](https://www.microsoft.com/microsoft-365/roadmap)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d3776-106">To learn more about when  AIR features will be available, see the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>

## <a name="alerts"></a><span data-ttu-id="d3776-107">경고</span><span class="sxs-lookup"><span data-stu-id="d3776-107">Alerts</span></span>

<span data-ttu-id="d3776-108">[경고](alert-policies.md#viewing-alerts) 는 보안 운영 팀 워크플로에서 문제를 대응 하기 위한 트리거를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-108">[Alerts](alert-policies.md#viewing-alerts) represent triggers for security operations team workflows for incident response.</span></span> <span data-ttu-id="d3776-109">확인을 위해 적절 한 경고 집합에 우선 순위를 지정 하는 동시에, 주소가 지정 되지 않은 위협에 대 한 해결 방법은 어렵습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-109">Prioritizing the right set of alerts for investigation, while making sure no threats are unaddressed is challenging.</span></span> <span data-ttu-id="d3776-110">경고에 대 한 조사가 수동으로 수행 되 면 보안 운영 팀이 엔터티 (예: 콘텐츠, 장치 및 사용자)를 위협 으로부터 찾아서 상호 연결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-110">When investigations into alerts are performed manually, Security Operations teams must hunt and correlate entities (e.g. content, devices and users) at risk from threats.</span></span> <span data-ttu-id="d3776-111">이러한 작업과 워크플로는 시간을 많이 소비 하며 여러 도구와 시스템을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-111">Such tasks and workflows are very time consuming and involve multiple tools and systems.</span></span> <span data-ttu-id="d3776-112">AIR을 사용 하는 경우 조사 및 응답은 보안 대응 playbook 자동으로 트리거하는 주요 보안 및 위협 관리 경고로 자동화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-112">With AIR, investigation and response are automated into key security and threat management alerts that trigger your security response playbooks automatically.</span></span> 

<span data-ttu-id="d3776-113">2019 년 4 월 초기 릴리스에서는 다음 단일 이벤트에서 생성 된 경고에 대 한 경고 정책이 자동으로 조사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-113">In the initial release of AIR in April 2019, alerts generated from following single events alert policies will be auto-investigated.</span></span> 

1. <span data-ttu-id="d3776-114">잠재적으로 악의적인 URL 클릭이 검색 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-114">A potentially malicious URL click was detected</span></span>
2. <span data-ttu-id="d3776-115">사용자가 피싱으로 보고 한 전자 메일</span><span class="sxs-lookup"><span data-stu-id="d3776-115">Email reported by user as phish\*</span></span>
3. <span data-ttu-id="d3776-116">배달 후 제거 된 맬웨어를 포함 하는 전자 메일 메시지 \*</span><span class="sxs-lookup"><span data-stu-id="d3776-116">Email messages containing malware removed after delivery\*</span></span>
4. <span data-ttu-id="d3776-117">배달 후 제거 된 피싱 Url을 포함 하는 전자 메일 메시지 \*</span><span class="sxs-lookup"><span data-stu-id="d3776-117">Email messages containing phish URLs removed after delivery\*</span></span>

> [!NOTE]
> <span data-ttu-id="d3776-118">이 경고에는 전자 메일 알림이 해제 된 보안 & 준수 센터 내의 각 경고 정책에 "정보" 심각도가 할당 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-118">These alerts have been assigned an "Informational" severity in the respective alert policies within the Security & Compliance Center with email notifications turned off.</span></span> <span data-ttu-id="d3776-119">이러한 구성은 경고 정책 구성을 통해 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-119">These can be turned on through the Alert policy configuration.</span></span>

<span data-ttu-id="d3776-120">알림을 보려면 보안 & 준수 센터에서 경고 \*\*\*\* > **보기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-120">To view alerts, in the Security & Compliance Center, choose **Alerts** > **View alerts**.</span></span> <span data-ttu-id="d3776-121">알림을 선택 하 여 세부 정보를 확인 하 고, **보기 조사** 링크를 사용 하 여 해당 [조사](#investigation-graph)로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-121">Select an alert to view its details, and from there, use the **View investigation** link to go to the corresponding [investigation](#investigation-graph).</span></span> <span data-ttu-id="d3776-122">정보 알림은 기본적으로 경고 보기에 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-122">Note that informational alerts are hidden in the alert view by default.</span></span> <span data-ttu-id="d3776-123">이러한 항목을 보려면 알림 필터링을 변경 하 여 정보 알림을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-123">To see them, you need to change the alert filtering to include informational alerts.</span></span>

<span data-ttu-id="d3776-124">조직에서 경고 관리 시스템, 서비스 관리 시스템 또는 SIEM (보안 정보 및 이벤트 관리) 시스템을 통해 보안 경고를 관리 하는 경우 전자 메일 알림을 통해 또는 다음을 통해 [해당 시스템에 Office 365 알림 메시지를 보낼 수 있습니다. Office 365 관리 활동 API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)</span><span class="sxs-lookup"><span data-stu-id="d3776-124">If your organization manages your security alerts through a alert management system, service management system, or Security Information and Event Management (SIEM) system, you can send Office 365 alerts to that system via either email notification or via the [Office 365 Management Activity API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> <span data-ttu-id="d3776-125">전자 메일 또는 API를 통한 조사 경고 알림에는 보안 & 준수 센터의 경고에 액세스 하 여 할당 된 보안 관리자가 조사를 빠르게 탐색할 수 있도록 하는 링크가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-125">The investigation alert notifications via email or API will include links to access the alerts in the Security & Compliance Center, enabling the assigned security administrator to navigate quickly to the investigation.</span></span>

![조사로 연결 되는 경고](media/air-alerts-page-details.png) 


## <a name="security-playbooks"></a><span data-ttu-id="d3776-127">보안 playbook</span><span class="sxs-lookup"><span data-stu-id="d3776-127">Security playbooks</span></span>

<span data-ttu-id="d3776-128">보안 playbook는 Microsoft Threat Protection의 자동화 핵심에 있는 백 엔드 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-128">Security playbooks are back-end policies that are at the heart of automation in Microsoft Threat Protection.</span></span> <span data-ttu-id="d3776-129">AIR에서 제공 되는 보안 playbook은 일반적인 실제 보안 시나리오를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-129">The security playbooks provided in AIR are based on common real-world security scenarios.</span></span> <span data-ttu-id="d3776-130">조직 내에서 경고가 트리거될 때 보안 playbook 자동으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-130">A security playbook is launched automatically when an alert is triggered within your organization.</span></span> <span data-ttu-id="d3776-131">알림이 트리거되어 연결 된 playbook 자동으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-131">Once the alert triggers, the associated playbook is run automatically.</span></span> <span data-ttu-id="d3776-132">Playbook에서는 조사를 실행 하 여 연결 된 모든 메타 데이터 (전자 메일 메시지, 사용자, 제목, 보낸 사람 등)를 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-132">The playbook runs an investigation, looking at all the associated metadata (including email messages, users, subjects, senders, etc.).</span></span> <span data-ttu-id="d3776-133">Playbook의 결과에 따라 AIR에서는 조직의 보안 팀이 위협을 제어 하 고 완화 하기 위해 수행할 수 있는 일련의 작업을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-133">Based on the playbook's findings, AIR recommends a set of actions that your organization's security team can take to control and mitigate the threat.</span></span> 

<span data-ttu-id="d3776-134">AIR에서 제공 하는 보안 playbook은 조직이 현재 직면 하 고 있는 가장 빈번한 위협을 처리 하도록 설계 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-134">The security playbooks you'll get with AIR are designed to tackle the most frequent threats that organizations face today.</span></span> <span data-ttu-id="d3776-135">Microsoft 및 고객 자산을 보호 하는 데 도움이 되는 사용자를 비롯 하 여 보안 작업 및 사건 대응 팀의 입력을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-135">They're based on input from Security Operations and Incident Response teams, including those who help defend Microsoft and our customers assets.</span></span>

### <a name="security-playbooks-are-rolling-out-in-phases"></a><span data-ttu-id="d3776-136">보안 playbook가 단계별로 롤아웃 됨</span><span class="sxs-lookup"><span data-stu-id="d3776-136">Security playbooks are rolling out in phases</span></span>

<span data-ttu-id="d3776-137">AIR의 일환으로 보안 playbook가 단계별로 배포 됨</span><span class="sxs-lookup"><span data-stu-id="d3776-137">As part of AIR, security playbooks are rolling out in phases</span></span>

- <span data-ttu-id="d3776-138">**1 단계 (2019 년 4 월)**: playbooks에는 보안 관리자가 검토 하 고 승인할 작업에 대 한 권장 사항이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-138">**Phase 1 (April 2019)**: Playbooks include recommendations for actions that security administrators review and approve.</span></span> <span data-ttu-id="d3776-139">1 단계에는 다음과 같은 playbooks가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-139">Phase 1 will include the following playbooks:</span></span>
    - <span data-ttu-id="d3776-140">사용자가 보고 한 피싱 메시지</span><span class="sxs-lookup"><span data-stu-id="d3776-140">User-reported phish message</span></span>
    - <span data-ttu-id="d3776-141">URL 결과 변경 클릭</span><span class="sxs-lookup"><span data-stu-id="d3776-141">URL click verdict change</span></span> 
    - <span data-ttu-id="d3776-142">맬웨어 배달 후 검색 (맬웨어 ZAP)</span><span class="sxs-lookup"><span data-stu-id="d3776-142">Malware detected post-delivery (Malware ZAP)</span></span>
    - <span data-ttu-id="d3776-143">피싱 검색 된 배달 후 ZAP (피싱 ZAP)</span><span class="sxs-lookup"><span data-stu-id="d3776-143">Phish detected post-delivery ZAP (Phish ZAP)</span></span>
    - <span data-ttu-id="d3776-144">위협 탐색기를 사용 하 여 수동 전자 메일 조사</span><span class="sxs-lookup"><span data-stu-id="d3776-144">Manual e-mail investigations (using Threat Explorer)</span></span>

- <span data-ttu-id="d3776-145">**2 단계 (2019 초 중 1 분)**: 보안 관리자가 몇 가지 새로운 playbook 및 playbook 향상 되었으며, 관리 상호 작용 없이 몇 가지 작업을 자동으로 수행 하는 보안 관리자로 security playbook를 구성 하는 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-145">**Phase 2 (second half of 2019)**: Several new playbooks and playbook improvements, plus the option for security administrators to configure security playbooks to take some actions automatically without administrative interaction.</span></span> 

### <a name="playbooks-include-investigation-and-recommendations"></a><span data-ttu-id="d3776-146">Playbooks에는 조사 및 권장 사항이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-146">Playbooks include investigation and recommendations</span></span>

<span data-ttu-id="d3776-147">각 playbook에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-147">Each playbook includes:</span></span> 
- <span data-ttu-id="d3776-148">루트 조사를</span><span class="sxs-lookup"><span data-stu-id="d3776-148">a root investigation,</span></span> 
- <span data-ttu-id="d3776-149">다른 잠재적 위협을 식별 및 상호 연결 하기 위해 수행 되는 단계</span><span class="sxs-lookup"><span data-stu-id="d3776-149">steps taken to identify and correlate other potential threats, and</span></span> 
- <span data-ttu-id="d3776-150">권장 되는 위협 재구성 작업</span><span class="sxs-lookup"><span data-stu-id="d3776-150">recommended threat remediation actions.</span></span>

<span data-ttu-id="d3776-151">각 상위 단계에는 위협에 대 한 심층적이 고 자세한 응답을 제공 하기 위해 실행 되는 여러 하위 단계가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-151">Each high-level step includes many sub-steps that are executed to provide a deep, detailed, and exhaustive response to threats.</span></span>

## <a name="example-a-user-reported-phish-message-launches-an-investigation-playbook"></a><span data-ttu-id="d3776-152">예: 사용자가 보고 한 피싱 메시지가 조사 playbook를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-152">Example: A user-reported phish message launches an investigation playbook</span></span>

<span data-ttu-id="d3776-153">조직의 사용자가 전자 메일 메시지를 전송 하 고 [outlook 또는 Outlook Web Access 용 보고서 메시지 추가 기능](enable-the-report-message-add-in.md)을 사용 하 여 Microsoft에 보고 하는 경우 보고서도 시스템에 전송 되며 사용자가 보고 한 보기의 탐색기에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-153">When a user in your organization submits an email message and reports it to Microsoft by using the [Report Message add-in for Outlook or Outlook Web Access](enable-the-report-message-add-in.md), the report is also sent to your system and is visible in Explorer in the User-reported view.</span></span> <span data-ttu-id="d3776-154">이 사용자가 보고 한이 메시지는 이제 조사 playbook를 자동으로 시작 하는 시스템 기반 정보 알림을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-154">This user-reported message now triggers a system-based informational alert, which automatically launches the investigation playbook.</span></span>

<span data-ttu-id="d3776-155">루트 조사 단계에서는 전자 메일의 다양 한 측면을 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-155">During the root investigation phase, various aspects of the email are assessed.</span></span> <span data-ttu-id="d3776-156">다음과 같은 다양한 알고리즘과 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-156">These include:</span></span>
- <span data-ttu-id="d3776-157">사용할 수 있는 위협의 유형에 대 한 결정</span><span class="sxs-lookup"><span data-stu-id="d3776-157">A determination about what type of threat it might be;</span></span>
- <span data-ttu-id="d3776-158">보낸 사람</span><span class="sxs-lookup"><span data-stu-id="d3776-158">Who sent it;</span></span>
- <span data-ttu-id="d3776-159">전자 메일이 전송 되는 위치 (보내는 인프라)</span><span class="sxs-lookup"><span data-stu-id="d3776-159">Where the email was sent from (sending infrastructure);</span></span>
- <span data-ttu-id="d3776-160">전자 메일의 다른 인스턴스가 배달 되거나 차단 되었는지 여부</span><span class="sxs-lookup"><span data-stu-id="d3776-160">Whether other instances of the email were delivered or blocked;</span></span>
- <span data-ttu-id="d3776-161">분석가의 평가</span><span class="sxs-lookup"><span data-stu-id="d3776-161">An assessment from our analysts;</span></span>
- <span data-ttu-id="d3776-162">전자 메일이 알려진 캠페인과 연결 되어 있는지 여부</span><span class="sxs-lookup"><span data-stu-id="d3776-162">Whether the email is associated with any known campaigns;</span></span>
- <span data-ttu-id="d3776-163">등이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-163">and more.</span></span>

<span data-ttu-id="d3776-164">루트 조사가 완료 되 면 playbook는 원래 전자 메일 및 해당 항목과 연결 된 엔터티에 대해 수행할 권장 작업 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-164">After the root investigation is complete, the playbook provides a list of recommended actions to take on the original email and entities associated with it.</span></span>
  
<span data-ttu-id="d3776-165">다음으로 몇 가지 위협 조사 및 사냥 단계가 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-165">Next, several threat investigation and hunting steps are executed:</span></span>

- <span data-ttu-id="d3776-166">다른 전자 메일 클러스터의 유사한 전자 메일 메시지가 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-166">Similar email messages in other email clusters are searched.</span></span>
- <span data-ttu-id="d3776-167">신호가 [Microsoft DEFENDER ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)와 같은 다른 플랫폼과 공유 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-167">The signal is shared with other platforms, such as [Microsoft Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection).</span></span>
- <span data-ttu-id="d3776-168">의심 스러운 전자 메일 메시지에서 모든 사용자가 악의적인 링크를 클릭 했는지 여부가 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-168">A determination is made on whether any users have clicked through any malicious links in suspicious email messages.</span></span>
- <span data-ttu-id="d3776-169">확인은 Office 365 Exchange Online Protection ([EOP](eop/exchange-online-protection-eop.md)) 및 Office 365 Advanced Threat Protection ([ATP](office-365-atp.md))을 통해 사용자가 보고 하는 다른 유사한 메시지가 있는지를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-169">A check is done across Office 365 Exchange Online Protection ([EOP](eop/exchange-online-protection-eop.md)) and Office 365 Advanced Threat Protection ([ATP](office-365-atp.md)) to see if there are any other similar messages reported by users.</span></span>
- <span data-ttu-id="d3776-170">사용자가 손상 되었는지 확인 하는 검사를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-170">A check is done to see if a user has been compromised.</span></span> <span data-ttu-id="d3776-171">이 검사는 [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security) 및 [Azure Active Directory](https://docs.microsoft.com/azure/active-directory)간의 신호를 활용 하 여 관련 된 사용자 활동에 대 한 예외를 모두 연관 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-171">This check leverages signals across [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security) and [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), correlating any related user activity anomalies.</span></span> 

<span data-ttu-id="d3776-172">사냥 단계에서는 위험과 위협이 다양 한 구하기 단계에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-172">During the hunting phase, risks and threats are assigned to various hunting steps.</span></span> 

<span data-ttu-id="d3776-173">재구성은 playbook의 마지막 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-173">Remediation is the final phase of the playbook.</span></span> <span data-ttu-id="d3776-174">이 단계에서는 조사 및 구하기 단계를 기반으로 재구성 단계가 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-174">During this phase, remediation steps are taken, based on the investigation and hunting phases.</span></span> 

## <a name="example-a-security-administrator-triggers-an-investigation-from-threat-explorer"></a><span data-ttu-id="d3776-175">예: 보안 관리자가 위협 탐색기에서 조사를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-175">Example: A security administrator triggers an investigation from Threat Explorer</span></span>

<span data-ttu-id="d3776-176">알림을 통해 트리거되는 자동 조사 외에 조직의 보안 운영 팀은 [위협 탐색기](use-explorer-in-security-and-compliance.md)의 보기에서 자동 조사를 트리거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-176">In addition to automatic investigations that are triggered by an alert, your organization's security operations team can trigger an automatic investigation from a view in [Threat Explorer](use-explorer-in-security-and-compliance.md).</span></span>

<span data-ttu-id="d3776-177">예를 들어 Explorer에서 사용자가 보고 한 메시지에 대 한 데이터를 보고 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-177">For example, suppose that you are viewing data in Explorer about user-reported messages.</span></span> <span data-ttu-id="d3776-178">결과 목록에서 항목을 선택한 다음 **조사**를 클릭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-178">You can select an item in the list of results, and then click **Investigate**.</span></span>

![검사 단추를 사용 하 여 탐색기에서 사용자가 보고 한 메시지](media/Explorer-UserReported-Investigate.png)

<span data-ttu-id="d3776-180">또 다른 예로, 맬웨어를 포함 하는 것으로 검색 된 전자 메일 메시지에 대 한 데이터를 보고 있는 경우 맬웨어가 있는 전자 메일 메시지를 여러 개 검색 한다고 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-180">As another example, suppose you are viewing data about email messages detected as containing malware, and there are several email messages detected as containing malware.</span></span> <span data-ttu-id="d3776-181">**전자 메일** 탭을 선택 하 고 전자 메일 메시지를 하나 이상 선택 하 고 **작업** 메뉴에서 **조사**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-181">You can select the **Email** tab, select one or more email messages, and then, on the **Actions** menu, select **Investigate**.</span></span> 

![탐색기에서 맬웨어 조사 시작](media/Explorer-Malware-Email-ActionsInvestigate.png)

<span data-ttu-id="d3776-183">경고로 트리거되는 playbook와 마찬가지로, 탐색기의 보기에서 트리거되는 자동 조사에는 루트 조사, 위협의 식별 및 상관 지정, 위협 완화를 위한 권장 작업 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-183">Similar to playbooks triggered by an alert, automatic investigations that are triggered from a view in Explorer include a root investigation, steps to identify and correlate threats, and recommended actions to mitigate those threats.</span></span>

## <a name="get-started"></a><span data-ttu-id="d3776-184">시작</span><span class="sxs-lookup"><span data-stu-id="d3776-184">Get started</span></span>

<span data-ttu-id="d3776-185">Office 365 전역 관리자, 보안 관리자 또는 보안 읽기 권한자로 조사에 액세스 하려면 Security & 준수 센터 ([https://protection.office.com](https://protection.office.com))로 이동 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-185">To access your investigations, as an Office 365 global administrator, security administrator, or security reader, go to the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)) and sign in.</span></span> <span data-ttu-id="d3776-186">다음 중 하나를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-186">Then, do one of the following:</span></span>

- <span data-ttu-id="d3776-187">왼쪽 탐색 창에서 **알림** > **보기로**이동 하 고, 조사 관련 알림 중 하나를 연 다음, 알림 플라이 아웃의 아래쪽에 있는 **보기 확인** 링크를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-187">In the left navigation, go to **Alerts** > **View alerts**, open one of the investigation related alerts, then click the **View investigation** link at the bottom of the alert flyout.</span></span> 

    <span data-ttu-id="d3776-188">또는</span><span class="sxs-lookup"><span data-stu-id="d3776-188">or</span></span>

- <span data-ttu-id="d3776-189">왼쪽 탐색에서 **위협 관리** > **조사**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-189">In the left navigation, go to **Threat management** > **Investigations**.</span></span>

    <span data-ttu-id="d3776-190">또는</span><span class="sxs-lookup"><span data-stu-id="d3776-190">or</span></span>

- <span data-ttu-id="d3776-191">보안 & 준수 센터에서 **위협 관리** > **대시보드로**이동 하 여 위협 관리 대시보드를 방문 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-191">Visit the Threat management dashboard (In the Security & Compliance Center, go to **Threat management** > **Dashboard**).</span></span>

![AIR 위젯](media/air-widgets.png)

<span data-ttu-id="d3776-193">무선 위젯은 [보안 대시보드의](security-dashboard.md)위쪽에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-193">Your AIR widgets will appear across the top of the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="d3776-194">시작 하려면 위젯을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-194">Select a widget to get started.</span></span>

<span data-ttu-id="d3776-195">관련 경고에서 직접 조사에 액세스할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-195">You may also access an investigation directly from the related Alerts.</span></span>

### <a name="automated-investigations"></a><span data-ttu-id="d3776-196">자동화 된 조사</span><span class="sxs-lookup"><span data-stu-id="d3776-196">Automated investigations</span></span>

<span data-ttu-id="d3776-197">자동화 된 조사 페이지에 조직의 조사 및 현재 상태가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-197">The automated investigations page shows your organization's investigations and their current states.</span></span>

![AIR의 주 조사 페이지](media/air-maininvestigationpage.png) 
  
<span data-ttu-id="d3776-199">예를 들어 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-199">You can:</span></span>
- <span data-ttu-id="d3776-200">조사로 직접 이동 합니다 ( **조사 ID**선택).</span><span class="sxs-lookup"><span data-stu-id="d3776-200">Navigate directly to an investigation (select an **Investigation ID**).</span></span>
- <span data-ttu-id="d3776-201">필터를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-201">Apply filters.</span></span> <span data-ttu-id="d3776-202">**조사 유형**, **시간 범위**, **상태**또는 이들의 조합 중에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-202">Choose from **Investigation Type**, **Time range**, **Status**, or a combination of these.</span></span>
- <span data-ttu-id="d3776-203">데이터를 CSV 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-203">Export the data to a CSV file.</span></span>

<span data-ttu-id="d3776-204">조사 상태는 분석 및 작업의 진행률을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-204">The investigation status indicates the progress of the analysis and actions.</span></span> <span data-ttu-id="d3776-205">조사가 실행 되 면 상태가 변경 되어 위협이 있는지 여부를 나타내고 작업이 승인 되었는지 여부도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-205">As the investigation runs, the status will change to indicate whether threats were found, as well as indicate whether actions have been approved.</span></span> 
- <span data-ttu-id="d3776-206">**시작**: 조사가 곧 시작 되기 위해 대기 중입니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-206">**Starting**: The investigation is queued to begin soon</span></span>
- <span data-ttu-id="d3776-207">**실행**중: 조사가 시작 되었으며 ' analysis '를 수행 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-207">**Running**: The investigation has started and is conducting its' analysis</span></span>
- <span data-ttu-id="d3776-208">**발견 된 위협이 없음**: 조사가 ' 분석 '을 완료 했으며 위협이 발견 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-208">**No Threats Found**: The investigation has completed its' analysis and no threats were found</span></span>
- <span data-ttu-id="d3776-209">**시스템 종료**: 7 일 후에 조사가 종료 및 만료 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-209">**Terminated By System**: The investigation was not closed and expired after 7 days</span></span>
- <span data-ttu-id="d3776-210">**보류 중인 작업**: 조사에서 권장 되는 작업을 발견 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-210">**Pending Action**: The investigation found threats with actions recommended</span></span>
- <span data-ttu-id="d3776-211">**발견 된 위협**: 조사에서 위협이 발견 되었지만 해당 위협이 AIR 내에서 사용할 수 있는 작업을 포함 하지 않음</span><span class="sxs-lookup"><span data-stu-id="d3776-211">**Threats Found**: The investigation found threats, but the threats do not have actions available within AIR</span></span>
- <span data-ttu-id="d3776-212">**재구성**됨: investgation가 완료 되었으며 완전히 재구성 되었습니다 (모든 작업이 승인 됨).</span><span class="sxs-lookup"><span data-stu-id="d3776-212">**Remediated**: The investgation finished and was fully remediated (all actions were approved)</span></span>
- <span data-ttu-id="d3776-213">**부분적으로 재구성**됨: 조사가 완료 되었으며 일부 권장 작업을 승인 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-213">**Partially Remediated**: The investigation finished and some of the recommended actions were approved</span></span>
- <span data-ttu-id="d3776-214">**종료**됨: 관리자가 조사를 종료 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-214">**Terminated By User**: An admin terminated the investigation</span></span>
- <span data-ttu-id="d3776-215">**실패**: 조사 중에 위협의 결론에 도달 하지 못하도록 차단 하는 동안 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-215">**Failed**: An error occurred during the investigation that prevented it from reaching a conclusion on threats</span></span>
- <span data-ttu-id="d3776-216">**제한 대기**: 시스템 처리 제한 (서비스 성능 보호)을 통해 조사가 분석을 기다리는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-216">**Queued By Throttling**: The investigation is waiting for analysis due to system processing limitations (to protect service performance)</span></span>
- <span data-ttu-id="d3776-217">**종료 된 제한**: 조사 볼륨 및 시스템 처리 제한으로 인해 조사를 충분 한 시간 내에 완료할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-217">**Terminated By Throttling**: The investigation could not be completed in sufficient time due to investigation volume and system processing limitations.</span></span> <span data-ttu-id="d3776-218">탐색기에서 전자 메일을 선택 하 고 조사 작업을 선택 하 여 조사를 다시 트리거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-218">You can re-trigger the investigation by selecting the email in Explorer and selecting the Investigate action.</span></span>

### <a name="investigation-graph"></a><span data-ttu-id="d3776-219">조사 그래프</span><span class="sxs-lookup"><span data-stu-id="d3776-219">Investigation graph</span></span>

<span data-ttu-id="d3776-220">특정 조사를 열면 조사 그래프 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-220">When you open a specific investigation, you see the investigation graph page.</span></span> <span data-ttu-id="d3776-221">이 페이지에는 전자 메일 메시지, 사용자 (및 해당 활동), 트리거된 알림의 일부로 자동 조사 되는 장치 등의 다양 한 엔터티가 모두 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-221">This page shows all the different entities: email messages, users (and their activities), and devices that were automatically investigated as part of the alert that was triggered.</span></span>

![AIR 조사 그래프 페이지](media/air-investigationgraphpage.png)

<span data-ttu-id="d3776-223">예를 들어 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-223">You can:</span></span>
- <span data-ttu-id="d3776-224">현재 조사에 대 한 시각적 개요를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-224">Get a visual overview of the current investigation.</span></span>
- <span data-ttu-id="d3776-225">조사 기간에 대 한 요약을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-225">View a summary of the investigation duration.</span></span>
- <span data-ttu-id="d3776-226">시각화에서 노드를 선택 하 여 해당 노드의 세부 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-226">Select a node in the visualization to view details for that node.</span></span>
- <span data-ttu-id="d3776-227">위쪽에서 탭을 선택 하 여 해당 탭의 세부 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-227">Select a tab across the top to view details for that tab.</span></span>

### <a name="alert-investigation"></a><span data-ttu-id="d3776-228">경고 조사</span><span class="sxs-lookup"><span data-stu-id="d3776-228">Alert investigation</span></span>

<span data-ttu-id="d3776-229">조사에 대 한 **알림** 탭에서 조사와 관련 된 경고를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-229">On the **Alerts** tab for an investigation, you can see alerts relevant to the investigation.</span></span> <span data-ttu-id="d3776-230">세부 정보에는 조사를 트리거한 경고와 확인에 상관 된 위험한 로그인, 대량 다운로드 등의 기타 알림이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-230">Details include the alert that triggered the investigation and other alerts, such as risky sign-in, mass download, etc., that are correlated to the investigation.</span></span> <span data-ttu-id="d3776-231">이 페이지에서는 보안 분석가가 개별 경고에 대 한 추가 세부 정보를 볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-231">From this page, a security analyst can also view additional details on individual alerts.</span></span>

![AIR 알림 페이지](media/air-investigationalertspage.png)

<span data-ttu-id="d3776-233">예를 들어 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-233">You can:</span></span>
- <span data-ttu-id="d3776-234">현재 트리거하는 경고 및 관련 경고에 대 한 시각적 개요를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-234">Get a visual overview of the current triggering alert and any associated alerts.</span></span>
- <span data-ttu-id="d3776-235">목록에서 알림을 선택 하 여 전체 알림 세부 정보를 표시 하는 플라이 아웃 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-235">Select an alert in the list to open a fly-out page that shows full alert details.</span></span>

### <a name="email-investigation"></a><span data-ttu-id="d3776-236">전자 메일 조사</span><span class="sxs-lookup"><span data-stu-id="d3776-236">Email investigation</span></span>

<span data-ttu-id="d3776-237">조사를 위해 **전자 메일** 탭에서 조사 중에 식별 된 전자 메일의 모든 클러스터를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-237">On the **Email** tab for an investigation, you can see all the clusters of email identified as part of the investigation.</span></span> 

<span data-ttu-id="d3776-238">조직의 사용자가 보내고 받는 전자 메일 양이 주어 지 면</span><span class="sxs-lookup"><span data-stu-id="d3776-238">Given the sheer volume of email that users in an organization send and receive, the process of</span></span> 
- <span data-ttu-id="d3776-239">메시지 헤더, 본문, URL 및 첨부 파일의 유사 특성에 따라 전자 메일 메시지를 클러스터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-239">clustering email messages based on similar attributes from a message header, body, URL and attachments;</span></span> 
- <span data-ttu-id="d3776-240">악성 전자 메일과 좋은 전자 메일을 구분 합니다. 한</span><span class="sxs-lookup"><span data-stu-id="d3776-240">separating malicious email from the good email; and</span></span> 
- <span data-ttu-id="d3776-241">악성 전자 메일 메시지에 대 한 작업 수행</span><span class="sxs-lookup"><span data-stu-id="d3776-241">taking action on malicious email messages</span></span> 

<span data-ttu-id="d3776-242">몇 시간 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-242">can take many hours.</span></span> <span data-ttu-id="d3776-243">이제 AIR에서이 프로세스를 자동화 하 여 조직의 보안 팀 시간과 노력을 절약 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-243">AIR now automates this process, saving your organization's security team time and effort.</span></span> 

<span data-ttu-id="d3776-244">전자 메일 분석 단계에서 두 가지 유형의 전자 메일 클러스터, 즉 유사성 클러스터와 지표 클러스터를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-244">Two different types of email clusters may be identified during the email analysis step: similarity clusters, and indicator clusters.</span></span> 
- <span data-ttu-id="d3776-245">유사성 클러스터는 비슷한 보낸 사람 및 콘텐츠 특성을 포함 하는 전자 메일 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-245">Similarity clusters are email messages that contain similar sender and content attributes.</span></span> <span data-ttu-id="d3776-246">이러한 클러스터는 원래 검색 결과를 기반으로 악의적인 콘텐츠를 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-246">These clusters are evaluated for malicious content based on the original detection findings.</span></span> <span data-ttu-id="d3776-247">충분 한 악의적인 검색을 포함 하는 전자 메일 클러스터가 악성으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-247">Email clusters that contain enough malicious detections will be considered malicious.</span></span>
- <span data-ttu-id="d3776-248">지표 클러스터는 원본 전자 메일의 동일한 지표 엔터티 (파일 해시 또는 URL)가 포함 된 전자 메일 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-248">Indicator clusters are email messages that contain the same indicator entity (file hash or URL) from the original email.</span></span> <span data-ttu-id="d3776-249">원본 파일/URL 엔터티가 악성으로 식별 되 면 AIR은 해당 엔터티를 포함 하는 전자 메일 메시지의 전체 클러스터에 결과 지표를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-249">When the original file/URL entity is identified as malicious, AIR will apply the indicator verdict to the entire cluster of email messages containing that entity.</span></span> <span data-ttu-id="d3776-250">맬웨어로 식별 된 파일은 해당 파일을 포함 하는 전자 메일 메시지의 클러스터가 맬웨어 전자 메일 메시지로 취급 됨을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-250">As a file identified as malware will mean that the cluster of email messages containing that file will be treated as malware email messages.</span></span>

<span data-ttu-id="d3776-251">클러스터링의 목표는 공격이 나 캠페인의 일부로 동일한 보낸 사람이 보낸 다른 관련 전자 메일 메시지를 찾는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-251">The goal of clustering is to find other related email messages that are sent by the same sender as part of an attack or a campaign.</span></span>

<span data-ttu-id="d3776-252">**전자 메일** 탭에는 사용자가 보고 한 전자 메일 세부 정보, 보고 된 원래 전자 메일, 맬웨어/피싱로 인 한 전자 메일 메시지 등 조사와 관련 된 전자 메일 항목도 표시 됩니다 zapped.</span><span class="sxs-lookup"><span data-stu-id="d3776-252">The **Email** tab will also show email items related to the investigation, such as the user-reported email details, the original email reported, the email message(s) zapped due to malware/phish, etc.</span></span>

<span data-ttu-id="d3776-253">전자 메일 탭에 식별 된 전자 메일 개수는 현재 **전자 메일** 탭에 표시 되는 모든 전자 메일 메시지의 총 합계를 나타냅니다. 전자 메일 메시지는 여러 클러스터에 표시 되므로 식별 되 고 수정 작업의 영향을 받는 전자 메일 메시지의 실제 총 수는 모든 클러스터 및 원래 받는 사람의 전자 메일에 있는 고유한 전자 메일 메시지의 수입니다. 보내는.</span><span class="sxs-lookup"><span data-stu-id="d3776-253">The email count identified on the email tab currently represents the sum total of all email messages shown on the **Email** tab. Since email messages will be present in multiple clusters, the actual total count of email messages identified (and affected by remediation actions) will be the count of unique email messages present across all of the clusters and original recipients' email messages.</span></span> 

<span data-ttu-id="d3776-254">보안 verdicts, 작업 및 배달 위치는 받는 사람 기준 마다 다르므로, 각 받는 사람에 대 한 전자 메일 메시지의 수는 두 가지입니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-254">Both Explorer and AIR count email messages on a per recipient basis, since the security verdicts, actions, and delivery locations will vary on a per recipient basis.</span></span> <span data-ttu-id="d3776-255">따라서 세 명의 사용자에 게 전송 되는 원래 전자 메일은 전자 메일 하나가 아닌 총 3 개의 전자 메일 메시지를 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-255">Thus an original email sent to three users will count as a total of three email messages instead of one email.</span></span> <span data-ttu-id="d3776-256">참고 전자 메일이 여러 작업을 수행할 수 있고 모든 작업이 수행 되 면 전자 메일의 복사본이 여러 개 있을 수도 있으므로 전자 메일이 두 번 이상 계산 되는 경우가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-256">Note there may be cases where an email gets counted two or more times, since the email may have multiple actions on it and there may be multiple copies of the email once all actions occur.</span></span> <span data-ttu-id="d3776-257">예를 들어 배달 중에 검색 되는 맬웨어 전자 메일은 차단 된 (격리 된) 전자 메일과 바뀐 전자 메일 (위협 파일을 경고 파일로 교체 하 고 사용자의 사서함으로 전달)이 모두 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-257">For example a malware email that is detected at delivery may result in both a blocked (quarantined) email and a replaced email (threat file replaced with an warning file, then delivered to user's mailbox).</span></span> <span data-ttu-id="d3776-258">시스템에 전자 메일의 복사본이 두 개 있기 때문에 이러한 복사본은 클러스터 수에서 모두 계산 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-258">Since there are literally two copies of the email in the system - these may both be counted in cluster counts.</span></span> 

<span data-ttu-id="d3776-259">전자 메일 개수는 조사 시 계산 되며, 기본 쿼리를 기반으로 하 여 조사 flyouts를 열 때 일부 개수가 다시 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-259">Email counts are calculated at the time of the investigation and some counts are re-calculated when you open investigation flyouts (based on an underlying query).</span></span> <span data-ttu-id="d3776-260">전자 메일 탭의 전자 메일 클러스터에 대해 표시 되는 전자 메일 수와 클러스터 플라이 아웃에 표시 되는 전자 메일 수량 값은 조사 시점에 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-260">The email counts shown for the email clusters on the email tab and the email quantity value shown on cluster flyout are calculated at the time of investigation.</span></span> <span data-ttu-id="d3776-261">클러스터 플라이 아웃의 전자 메일 탭 아래쪽에 표시 되는 전자 메일 수와 Explorer에 표시 되는 전자 메일 메시지의 수에는 조사 초기 분석 후에 받은 전자 메일 메시지가 반영 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-261">The email count shown at the bottom of the email tab of the cluster flyout, as well as the count of email messages shown in Explorer will reflect email messages received after the investigation's initial analysis.</span></span> <span data-ttu-id="d3776-262">따라서 조사 분석 단계와 관리자가 조사를 검토 하는 시간 사이에 도착 하는 전자 메일 메시지가 5 번 더 표시 되 면 전자 메일 메시지의 원래 양이 10 개를 보여주는 전자 메일 클러스터가 총 15가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-262">Thus an email cluster that shows an original quantity of 10 email messages would show an email list total of 15 when 5 more email messages arrive between the investigation analysis phase and when the admin reviews the investigation.</span></span> <span data-ttu-id="d3776-263">각 보기에서 두 수를 모두 표시 하는 것은 조사 당시에 전자 메일 영향을 나타내고 수정이 실행 될 때까지 현재 영향을 나타내도록 하기 위해 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-263">Showing both counts in different views is done to indicate the email impact at the time of investigation and the current impact up until the time that remediation is run.</span></span>

<span data-ttu-id="d3776-264">예를 들어 다음과 같은 시나리오를 가정해 봅니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-264">As an example, consider the following scenario.</span></span> <span data-ttu-id="d3776-265">세 개의 전자 메일 메시지 중 첫 번째 클러스터는 피싱 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-265">The first cluster of three email messages were deemed to be phish.</span></span> <span data-ttu-id="d3776-266">이러한 항목 중 일부는 초기 검색을 수행 하는 동안 피싱으로 식별 되었기 때문에 같은 IP 및 주체를 포함 하는 비슷한 메시지의 다른 클러스터가 발견 되어 악성으로 간주 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-266">Another cluster of similar messages with the same IP and subject was found and considered malicious, as some of them were identified as phish during initial detection.</span></span> 

![AIR 전자 메일 조사 페이지](media/air-investigationemailpage.png)

<span data-ttu-id="d3776-268">예를 들어 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-268">You can:</span></span>
- <span data-ttu-id="d3776-269">현재 클러스터링 결과 및 발견 된 위협에 대 한 시각적 개요를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-269">Get a visual overview of the current clustering results and threats found.</span></span>
- <span data-ttu-id="d3776-270">클러스터 엔터티 또는 위협 목록을 클릭 하 여 전체 알림 세부 정보를 표시 하는 플라이 아웃 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-270">Click a cluster entity or a threat list to open a fly-out page that shows the full alert details.</span></span>
- <span data-ttu-id="d3776-271">' 전자 메일 클러스터 세부 정보 ' 탭 맨 위에 있는 ' 탐색기에서 열기 ' 링크를 클릭 하 여 전자 메일 클러스터를 자세히 조사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-271">Further investigate the email cluster by clicking the 'Open in Explorer' link at the top of the 'Email cluster details' tab</span></span>

![플라이 아웃 세부 정보를 사용한 AIR 조사 전자 메일](media/air-investigationemailpageflyoutdetails.png)

<span data-ttu-id="d3776-273">\* 참고: 전자 메일 컨텍스트에서 조사 중에 볼륨 변칙 위협 표면을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-273">\*Note: In the context of email, you may see a volume anomaly threat surface as part of the investigation.</span></span> <span data-ttu-id="d3776-274">볼륨 변칙은 이전 기간에 비해 조사 이벤트에 대 한 유사한 전자 메일 메시지의 스파이크를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-274">A volume anomaly indicates a spike in similar email messages around the investigation event time compared to earlier timeframes.</span></span> <span data-ttu-id="d3776-275">전자 메일 트래픽 (예: 제목 및 보낸 사람 도메인, 본문 유사성 및 보낸 사람 IP)이 비슷한 방식으로 전자 메일을 사용 하는 것이 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-275">This spike in email traffic with similar characteristics (e.g. subject and sender domain, body similarity and sender IP) is typical of the start of email campaigns or attacks.</span></span> <span data-ttu-id="d3776-276">그러나 일반적으로 대량, 스팸 및 합법적인 전자 메일 캠페인은 이러한 특성을 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-276">However, bulk, spam, and legitimate email campaigns commonly share these characteristics.</span></span> <span data-ttu-id="d3776-277">볼륨 예외는 잠재적 위협을 나타내므로, 바이러스 백신 엔진, 샌드 박싱 또는 악의적인 평판을 사용 하 여 식별 된 맬웨어 또는 피싱 위협과 비교 하는 것이 더 심각 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-277">Volume anomalies represent a potential threat, and accordingly could be less severe compared to malware or phish threats that are identified using anti-virus engines, detonation or malicious reputation.</span></span>

### <a name="user-investigation"></a><span data-ttu-id="d3776-278">사용자 조사</span><span class="sxs-lookup"><span data-stu-id="d3776-278">User investigation</span></span>

<span data-ttu-id="d3776-279">**사용자** 탭에서는 조사의 일부로 식별 된 모든 사용자를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-279">On the **Users** tab, you can see all the users identified as part of the investigation.</span></span> <span data-ttu-id="d3776-280">사용자에 게 영향을 줄 수 있거나 해당 이벤트가 발생할 수 있는 이벤트 또는 표시가 있으면 조사에 사용자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-280">Users will appear in the investigation when there is an event or indication that the user may be affected or compromised.</span></span>

<span data-ttu-id="d3776-281">예를 들어 다음 이미지에서 AIR은 생성 된 새 받은 편지함 규칙을 기반으로 하는 손상 및 예외 표시등을 식별 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-281">For example, in the following image, AIR has identified indicators of compromise and anomalies based on a new inbox rule that was created.</span></span> <span data-ttu-id="d3776-282">조사에 대 한 자세한 내용은이 탭 내의 자세한 보기를 통해 확인할 수 있습니다. 손상 및 변칙에 대 한 표시기에는 [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security)의 변칙 검색이 포함 될 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-282">Additional details (evidence) of the investigation are available through detailed views within this tab. Indicators of compromise and anomalies may also include anomaly detections from [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security).</span></span>

![AIR 조사 사용자 페이지](media/air-investigationuserspage.png)

<span data-ttu-id="d3776-284">예를 들어 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-284">You can:</span></span>
- <span data-ttu-id="d3776-285">발견 된 사용자 결과 및 위험에 대 한 시각적 개요를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="d3776-285">Get a visual overview of identified user results and risks found.</span></span>
- <span data-ttu-id="d3776-286">전체 알림 세부 정보를 표시 하는 플라이 아웃 페이지를 열 사용자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-286">Select a user to open a fly-out page that shows the full alert details.</span></span>

### <a name="machine-investigation"></a><span data-ttu-id="d3776-287">컴퓨터 조사</span><span class="sxs-lookup"><span data-stu-id="d3776-287">Machine investigation</span></span>

<span data-ttu-id="d3776-288">**컴퓨터** 탭에서 조사 과정으로 식별 된 모든 컴퓨터를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-288">On the **Machines** tab, you can see all the machines identified as part of the investigation.</span></span> 

![AIR 조사 컴퓨터 페이지](media/air-investigationmachinepage.png)

<span data-ttu-id="d3776-290">조사 과정에서 AIR은 전자 메일 위협의 상관 관계를 장치에 맞게 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-290">As part of the investigation, AIR correlates email threats to devices.</span></span> <span data-ttu-id="d3776-291">예를 들어 조사를 통해 조사를 위해 [Microsoft DEFENDER ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection
) 에 게 악성 파일 해시를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-291">For example, an investigation passes a malicious file hash across to [Microsoft Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection
) to investigate.</span></span> <span data-ttu-id="d3776-292">이렇게 하면 사용자에 대 한 관련 시스템을 자동으로 조사 하 여 위협이 클라우드 및 끝점에서 모두 해결 되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-292">This allows for automated investigation of relevant machines for your users, to help ensure that threats are addressed both in the cloud and across your endpoints.</span></span> 

<span data-ttu-id="d3776-293">예를 들어 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-293">You can:</span></span>
- <span data-ttu-id="d3776-294">발견 된 현재 컴퓨터 및 위협에 대 한 시각적 개요를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-294">Get a visual overview of the current machines and threats found.</span></span>
- <span data-ttu-id="d3776-295">컴퓨터를 선택 하 여 Microsoft Defender 보안 센터에서 관련 [Microsoft DEFENDER ATP 조사](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations) 로 연결 되는 보기를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-295">Select a machine to open a view that into the related [Microsoft Defender ATP investigations](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations) in the Microsoft Defender Security Center.</span></span>

### <a name="entity-investigation"></a><span data-ttu-id="d3776-296">엔터티 조사</span><span class="sxs-lookup"><span data-stu-id="d3776-296">Entity investigation</span></span>

<span data-ttu-id="d3776-297">**엔터티** 탭에서 조사 중에 식별 된 모든 엔터티를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-297">On the **Entities** tab, you can see all the entities identified as part of the investigation.</span></span> 

<span data-ttu-id="d3776-298">여기서는 전자 메일 메시지, 클러스터, IP 주소, 사용자 등의 엔터티 유형에 대 한 조사 된 엔터티 및 세부 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-298">Here, you can see the investigated entities and details of the types of entities, such as email messages, clusters, IP addresses, users, and more.</span></span> <span data-ttu-id="d3776-299">또한 분석 된 엔터티 수와 각 엔터티가 연결 된 위협을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-299">You can also see how many entities were analyzed, and the threats that were associated with each.</span></span> 

![AIR 조사 엔터티 페이지](media/air-investigationentitiespage.png)

<span data-ttu-id="d3776-301">예를 들어 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-301">You can:</span></span>
- <span data-ttu-id="d3776-302">발견 된 조사 엔터티 및 위협에 대 한 시각적 개요를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="d3776-302">Get a visual overview of the investigation entities and threats found.</span></span>
- <span data-ttu-id="d3776-303">엔터티를 선택 하 여 관련 엔터티 세부 정보를 표시 하는 플라이 아웃 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-303">Select an entity to open a fly-out page that shows the related entity details.</span></span>

![AIR 조사 엔터티 세부 정보](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a><span data-ttu-id="d3776-305">Playbook 로그</span><span class="sxs-lookup"><span data-stu-id="d3776-305">Playbook log</span></span>

<span data-ttu-id="d3776-306">**로그** 탭에서는 조사 중에 발생 한 모든 playbook 단계를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-306">On the **Log** tab, you can see all the playbook steps that have occurred during the investigation.</span></span> <span data-ttu-id="d3776-307">로그에는 AIR의 일부로 서 Office 365 자동 조사 기능을 통해 완료 된 모든 작업의 전체 인벤토리가 캡처됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-307">The log captures a complete inventory of all actions completed by Office 365 auto-investigation capabilities as part of AIR.</span></span> <span data-ttu-id="d3776-308">작업 자체, 설명, 실제 시작 날짜를 포함 하 여 수행 된 모든 단계를 명확 하 게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-308">It provides a clear view of all the steps taken, including the action itself, a description, and the duration of the actual from start to finish.</span></span> 

![AIR 조사 로그 페이지](media/air-investigationlogpage.png)

<span data-ttu-id="d3776-310">예를 들어 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-310">You can:</span></span>
- <span data-ttu-id="d3776-311">Playbook 수행 된 단계에 대 한 시각적 개요를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d3776-311">Get see a visual overview of the playbook steps taken.</span></span>
- <span data-ttu-id="d3776-312">결과를 CSV 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-312">Export the results to a CSV file.</span></span>
- <span data-ttu-id="d3776-313">보기를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-313">Filter the view.</span></span>

### <a name="recommended-actions"></a><span data-ttu-id="d3776-314">권장 작업</span><span class="sxs-lookup"><span data-stu-id="d3776-314">Recommended actions</span></span>

<span data-ttu-id="d3776-315">조사가 완료 된 후에 수정이 권장 되는 모든 playbook 작업을 **작업** 탭에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-315">On the **Actions** tab, you can see all the playbook actions that are recommended for remediation after the investigation has completed.</span></span> 

<span data-ttu-id="d3776-316">작업 조사를 마칠 때까지 수행 하는 것이 권장 되는 단계를 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-316">Actions capture the steps Microsoft recommends you take at the end of a investigation.</span></span> <span data-ttu-id="d3776-317">하나 이상의 작업을 선택 하 여 여기에서 수정 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-317">You can take remediation actions here by selecting one or more actions.</span></span> <span data-ttu-id="d3776-318">**승인을** 클릭 하면 재구성을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-318">Clicking **Approve** will allow remediation to begin.</span></span> <span data-ttu-id="d3776-319">(적절 한 사용 권한이 필요 함-탐색기 및 AIR에서 작업을 실행 하려면 ' 검색 및 제거 ' 역할이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-319">(Appropriate permissions are needed - the 'Search And Purge' role is required to run actions from Explorer and AIR).</span></span> <span data-ttu-id="d3776-320">예를 들어 보안 독자는 작업을 볼 수 있지만 승인 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-320">For example, a Security Reader can view actions but not approve them.</span></span> <span data-ttu-id="d3776-321">참고-모든 작업을 승인할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-321">Note - you do not have to approve every action.</span></span> <span data-ttu-id="d3776-322">권장 작업에 동의 하지 않거나 조직에서 특정 유형의 작업을 선택 하지 않은 경우에는 작업을 **거부** 하거나 무시 하 고 작업을 수행 하지 않도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-322">If you do not agree with the recommended action or your organization does not choose certain types of actions - then you can either choose to **Reject** the actions or simply ignore them and take no action.</span></span> <span data-ttu-id="d3776-323">모든 작업을 승인 및/또는 거부 하면 조사가 완전히 종료 되지만 일부 작업은 완료 되지 않으면 조사 상태가 부분 재구성 됨 상태로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-323">Approving and/or rejecting all actions will let the investigation fully close, while leaving some actions incomplete will result in the investigation status changing to a partially remediated state.</span></span>

![AIR 조사 작업 페이지](media/air-investigationactionspage.png)

<span data-ttu-id="d3776-325">예를 들어 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-325">You can:</span></span>
- <span data-ttu-id="d3776-326">Playbook 권장 작업에 대 한 시각적 개요를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-326">Get a visual overview of the playbook-recommended actions.</span></span>
- <span data-ttu-id="d3776-327">단일 작업 또는 여러 작업을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-327">Select a single action or multiple actions.</span></span>
- <span data-ttu-id="d3776-328">설명으로 권장 작업을 승인 하거나 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-328">Approve or reject recommended actions with comments.</span></span>
- <span data-ttu-id="d3776-329">결과를 CSV 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-329">Export the results to a CSV file.</span></span>
- <span data-ttu-id="d3776-330">보기를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-330">Filter the view.</span></span>

## <a name="how-to-get-air"></a><span data-ttu-id="d3776-331">공기를 얻는 방법</span><span class="sxs-lookup"><span data-stu-id="d3776-331">How to get AIR</span></span>

<span data-ttu-id="d3776-332">현재 Office 365 AIR 기능은 미리 보기에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-332">Currently, Office 365 AIR features are in preview.</span></span> <span data-ttu-id="d3776-333">일반적으로 사용할 수 있는 경우 Office 365 AIR 기능은 다음 구독에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3776-333">When generally available, Office 365 AIR features will be included in the following subscriptions:</span></span>

- <span data-ttu-id="d3776-334">Microsoft 365 Enterprise E5</span><span class="sxs-lookup"><span data-stu-id="d3776-334">Microsoft 365 Enterprise E5</span></span>
- <span data-ttu-id="d3776-335">Office 365 Enterprise E5</span><span class="sxs-lookup"><span data-stu-id="d3776-335">Office 365 Enterprise E5</span></span>
- <span data-ttu-id="d3776-336">Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="d3776-336">Microsoft Threat Protection</span></span>
- <span data-ttu-id="d3776-337">Office 365 Advanced Threat Protection 계획 2</span><span class="sxs-lookup"><span data-stu-id="d3776-337">Office 365 Advanced Threat Protection Plan 2</span></span>

<span data-ttu-id="d3776-338">기능 가용성에 대 한 자세한 내용은 [Microsoft 365 로드맵](https://www.microsoft.com/microsoft-365/roadmap)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d3776-338">To learn more about feature availability, visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>
