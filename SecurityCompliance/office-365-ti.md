---
title: Office 365 위협 조사 및 응답
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 08/23/2019
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 32405da5-bee1-4a4b-82e5-8399df94c512
ms.collection:
- M365-security-compliance
description: Office 365 Advanced Threat Protection의 위협 인텔리전스 기능을 통해 조직에 대 한 위협을 파악 하 고, 맬웨어, 피싱 및 기타 공격에 대처 하 고 사용자를 대신 하 여 Office 365에서 검색 한 기타 공격과 위협을 검색할 수 있는 방법을 알아봅니다. 슬라이더.
ms.openlocfilehash: 1d31f3a464060f5b72730e15895d918e61aa09a1
ms.sourcegitcommit: 4a2bde56178609e75c1ad7ecad2db5e049fc0c45
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2019
ms.locfileid: "36761654"
---
# <a name="office-365-threat-investigation-and-response"></a><span data-ttu-id="61444-103">Office 365 위협 조사 및 응답</span><span class="sxs-lookup"><span data-stu-id="61444-103">Office 365 threat investigation and response</span></span>

<span data-ttu-id="61444-104">위협 조사 및 [Office 365 Advanced Threat Protection](office-365-atp.md) 의 응답 기능은 보안 분석가와 관리자가 조직의 Office 365 사용자를 보호 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61444-104">Threat investigation and response capabilities in [Office 365 Advanced Threat Protection](office-365-atp.md) help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
- <span data-ttu-id="61444-105">고 사이버 공격를 쉽게 식별, 모니터링 및 이해할 수 있도록 설정</span><span class="sxs-lookup"><span data-stu-id="61444-105">Making it easy to identify, monitor and understand cyberattacks</span></span>
    
- <span data-ttu-id="61444-106">Exchange Online, SharePoint Online, 비즈니스용 OneDrive 및 Microsoft 팀의 위협에 빠르게 문제를 해결 하는 데 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="61444-106">Helping to quickly address threats in Exchange Online, SharePoint Online, OneDrive for Business and Microsoft Teams</span></span>
    
- <span data-ttu-id="61444-107">보안 작업에 도움이 되는 통찰력 및 지식을 제공 하 여 조직에 대 한 고 사이버 공격 방지</span><span class="sxs-lookup"><span data-stu-id="61444-107">Providing insights and knowledge to help security operations prevent cyberattacks against their organization</span></span>

- <span data-ttu-id="61444-108">중요 전자 메일 기반 위협에 대 한 [자동화 된 조사 및 응답](automated-investigation-response-office.md) 채택</span><span class="sxs-lookup"><span data-stu-id="61444-108">Employing [automated investigation and response](automated-investigation-response-office.md) for critical email-based threats</span></span>
    
<span data-ttu-id="61444-109">위협 조사 및 응답 기능은 Office 365 보안 &amp; 및 준수 센터에서 사용할 수 있는 위협 및 관련 된 응답 작업에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-109">Threat investigation and response capabilities provide insights into threats and related response actions that are available in the Office 365 Security &amp; Compliance Center.</span></span> <span data-ttu-id="61444-110">이러한 정보를 활용 하면 조직의 보안 팀이 전자 메일 이나 파일 기반 공격 으로부터 Office 365 사용자를 보호 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61444-110">These insights can help your organization's security team protect Office 365 users from email- or file-based attacks.</span></span> <span data-ttu-id="61444-111">이 기능은 신호를 모니터링 하 고 사용자 활동, 인증, 전자 메일, 손상 된 Pc 및 보안 인시던트와 같은 여러 원본의 데이터를 수집 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61444-111">The capabilities help monitor signals and gathers data from multiple sources, such as user activity, authentication, email, compromised PCs, and security incidents.</span></span> <span data-ttu-id="61444-112">비즈니스 의사 결정권자 및 Office 365 전역 관리자, 보안 관리자 및 보안 분석가는이 정보를 사용 하 여 Office 365 사용자에 대 한 위협에 대 한 이해를 받고 지적 재산을 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61444-112">Business decision makers and Office 365 global administrators, security administrators, and security analysts can all use this information to understand and respond to threats against Office 365 users and protect intellectual property.</span></span>

## <a name="get-acquainted-with-threat-investigation-and-response-tools"></a><span data-ttu-id="61444-113">위협 조사 및 응답 도구 익히기</span><span class="sxs-lookup"><span data-stu-id="61444-113">Get acquainted with threat investigation and response tools</span></span>

<span data-ttu-id="61444-114">&amp; [위협 대시보드](#threat-dashboard), [탐색기](#threat-explorer), [인시던트](#incidents), [공격 시뮬레이터](#attack-simulator)를 비롯 한 도구 및 응답 워크플로 집합으로, 보안 및 준수 센터의 위협 조사 및 응답 기능 [자동화 된 조사 & 응답](automated-investigation-response-office.md)입니다.</span><span class="sxs-lookup"><span data-stu-id="61444-114">Threat investigation and response capabilities surface in the Security &amp; Compliance Center, as a set of tools and response workflows, including the [threat dashboard](#threat-dashboard), [Explorer](#threat-explorer), [Incidents](#incidents), [Attack Simulator](#attack-simulator), and [Automated Investigation & Response](automated-investigation-response-office.md).</span></span>
  
### <a name="threat-dashboard"></a><span data-ttu-id="61444-115">위협 대시보드</span><span class="sxs-lookup"><span data-stu-id="61444-115">Threat dashboard</span></span>

<span data-ttu-id="61444-116">위협 대시보드 ( [보안 대시보드](security-dashboard.md)라고도 함)를 사용 하 여 해결 된 위협을 빠르게 확인 하 고, Office 365 서비스가 비즈니스를 보호 하는 방법을 비즈니스 의사 결정권자에 게 보고 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-116">Use the Threat dashboard (this is also referred to as the [Security dashboard](security-dashboard.md)) to quickly see what threats have been addressed, and as a visual way to report to business decision makers how Office 365 services are securing your business.</span></span>
  
![위협 대시보드](media/ce013a31-3f80-4d09-bb95-bfb7623b8bc4.png)
  
<span data-ttu-id="61444-118">이 대시보드 &amp; 를 보고 사용 하려면 보안 및 준수 센터에서 **위협 관리** \> **대시보드로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-118">To view and use this dashboard, in the Security &amp; Compliance Center, go to **Threat management** \> **Dashboard**.</span></span>

<span data-ttu-id="61444-119">자세한 내용은</span><span class="sxs-lookup"><span data-stu-id="61444-119">To learn more about</span></span> 
  
### <a name="threat-explorer"></a><span data-ttu-id="61444-120">위협 탐색기</span><span class="sxs-lookup"><span data-stu-id="61444-120">Threat Explorer</span></span>

<span data-ttu-id="61444-121">위협 [탐색기 (및 실시간 검색)](threat-explorer.md) 를 사용 하 여 위협을 분석 하 고, 시간에 따른 공격 량을 확인 하 고, 위협 계열, 침입자 인프라 등을 기준으로 데이터를 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-121">Use [Threat Explorer (and real-time detections)](threat-explorer.md) to analyze threats, see the volume of attacks over time, and analyze data by threat families, attacker infrastructure, and more.</span></span> <span data-ttu-id="61444-122">위협 탐색기 (탐색기 라고도 함)는 모든 보안 분석가의 조사 워크플로에서 시작 되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="61444-122">Threat Explorer (also referred to as Explorer) is the starting place for any security analyst's investigation workflow.</span></span>
  
![위협 탐색기](media/7a7cecee-17f0-4134-bcb8-7cee3f3c3890.png)
  
<span data-ttu-id="61444-124">이 보고서 &amp; 를 보고 사용 하려면 보안 및 준수 센터에서 **위협 관리** \> **탐색기**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-124">To view and use this report, in the Security &amp; Compliance Center, go to **Threat management** \> **Explorer**.</span></span>
  
### <a name="incidents"></a><span data-ttu-id="61444-125">인시던트</span><span class="sxs-lookup"><span data-stu-id="61444-125">Incidents</span></span>

<span data-ttu-id="61444-126">문제 목록 (조사가 라고도 함)을 사용 하 여 비행 보안 인시던트 목록을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-126">Use the Incidents list (this is also called Investigations) to see a list of in flight security incidents.</span></span> <span data-ttu-id="61444-127">인시던트는 의심 스러운 전자 메일 메시지와 같은 위협을 추적 하 고 추가 조사 및 수정을 수행 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61444-127">Incidents are used to track threats such as suspicious email messages, and to conduct further investigation and remediation.</span></span>
  
![Office 365의 현재 위협 인시던트 목록](media/acadd4c7-d2de-4146-aeb8-90cfad805a9c.png)
  
<span data-ttu-id="61444-129">조직의 현재 인시던트 &amp; 목록을 보려면 보안 및 준수 센터에서 **위협 관리** \> **검토** \> **인시던트**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-129">To view the list of current incidents for your organization, in the Security &amp; Compliance Center, go to **Threat management** \> **Review** \> **Incidents**.</span></span>
  
![보안 &amp; 및 준수 센터에서 위협 관리 \> 검토를 선택 합니다.](media/e0f46454-fa38-40f0-a120-b595614d1d22.png)

### <a name="attack-simulator"></a><span data-ttu-id="61444-131">공격 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="61444-131">Attack Simulator</span></span>

<span data-ttu-id="61444-132">공격 시뮬레이터를 사용 하 여 조직에서 현실적인 고 사이버 공격를 설정 및 실행 하 고, 실제에서는 사이버 공격과 비즈니스에 영향을 주기 전에 취약 한 사용자를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-132">Use Attack Simulator to set up and run realistic cyberattacks in your organization, and identify vulnerable people before a real cyberattack affects your business.</span></span> <span data-ttu-id="61444-133">자세한 내용은 [Office 365의 Attack 시뮬레이터](attack-simulator.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="61444-133">To learn more, see [Attack Simulator in Office 365](attack-simulator.md).</span></span>

### <a name="automated-investigation-and-response"></a><span data-ttu-id="61444-134">자동화된 조사 및 응답</span><span class="sxs-lookup"><span data-stu-id="61444-134">Automated investigation and response</span></span>

<span data-ttu-id="61444-135">자동화 된 조사 및 응답 (AIR) 기능을 사용 하 여 조직의 위협 으로부터 발생 하는 콘텐츠, 장치 및 사용자와 관련 된 시간과 노력을 절감할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61444-135">Use automated investigation and response (AIR) capabilities to save time and effort correlating content, devices, and people at risk from threats in your organization.</span></span> <span data-ttu-id="61444-136">AIR 프로세스는 특정 알림이 트리거될 때 또는 보안 운영 팀이 시작 될 때 시작 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61444-136">AIR processes can begin whenever certain alerts are triggered, or when started by your security operations team.</span></span> <span data-ttu-id="61444-137">자세한 내용은 [Office 365의 자동화 된 조사 및 응답 (AIR)](automated-investigation-response-office.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="61444-137">To learn more, see [Automated Investigation and Response (AIR) with Office 365](automated-investigation-response-office.md).</span></span> 
  
## <a name="threat-intelligence-widgets"></a><span data-ttu-id="61444-138">위협 인텔리전스 위젯</span><span class="sxs-lookup"><span data-stu-id="61444-138">Threat intelligence widgets</span></span>

<span data-ttu-id="61444-139">보안 분석가는 Office 365 Advanced Threat Protection 계획 2 제공의 일부로 알려진 위협에 대 한 세부 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61444-139">As part of the Office 365 Advanced Threat Protection Plan 2 offering, security analysts can review details about a known threat.</span></span> <span data-ttu-id="61444-140">이 기능은 사용자가 안전 하 게 유지 하기 위해 수행할 수 있는 추가 예방 조치/단계가 있는지 여부를 확인 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-140">This is useful to determine whether there are additional preventative measures/steps that can be taken to keep users safe.</span></span>
  
![최근 위협에 대 한 정보를 보여 주는 보안 경향](media/11e7d40d-139b-4c56-8d52-c091c8654151.png) 
  
## <a name="how-do-we-get-these-capabilities"></a><span data-ttu-id="61444-142">이러한 기능은 어떻게 얻을 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="61444-142">How do we get these capabilities?</span></span>

<span data-ttu-id="61444-143">Office 365 위협 조사 및 응답 기능은 Office 365 Advanced Threat Protection 계획 2 및 Enterprise E5에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61444-143">Office 365 threat investigation and response capabilities are included in Office 365 Advanced Threat Protection Plan 2 and Enterprise E5.</span></span> 

> [!TIP]
> <span data-ttu-id="61444-144">조직에 이러한 위협 조사 및 응답 기능이 포함 되지 않은 Office 365 구독이 있는 경우 Office 365 Advanced Threat Protection 계획 2를 추가 기능으로 구입할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61444-144">If your organization has an Office 365 subscription that does not include these threat investigation and response capabilities, you can potentially purchase Office 365 Advanced Threat Protection Plan 2 as an add-on.</span></span> <span data-ttu-id="61444-145">계획 옵션에 대 한 자세한 내용은 [office 365 Advanced Threat Protection 서비스 설명](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) 및 [비즈니스용 office 365 용 추가 기능 구입 또는 편집](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="61444-145">For more information about plan options, see [Office 365 Advanced Threat Protection service description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) and [Buy or edit an add-on for Office 365 for business](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on).</span></span>
  
1. <span data-ttu-id="61444-146">Office 365 전역 관리자 인 경우로 이동 [https://admin.microsoft.com](https://admin.microsoft.com) 하 여 office 365에 대 한 회사 또는 학교 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-146">As an Office 365 global administrator, go to [https://admin.microsoft.com](https://admin.microsoft.com) and sign in using your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="61444-147">**관리자 \*\* \> \*\* 청구**을 선택하여 현재 구독에 포함된 내용을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-147">Choose **Admin** \> **Billing** to see what your current subscription includes.</span></span> 
    - <span data-ttu-id="61444-148">**Office 365 Enterprise**e 5가 표시 되 면 조직에 Office 365 Advanced Threat Protection 계획 2 (위협 조사 및 응답 기능 포함)가 있는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="61444-148">If you see **Office 365 Enterprise E5**, then your organization has Office 365 Advanced Threat Protection Plan 2 (which includes threat investigation and response capabilities).</span></span> 
    - <span data-ttu-id="61444-149">**Office 365 Enterprise E3** 또는 **Office 365 enterprise E1**과 같은 다른 구독이 표시 되는 경우 Office 365 Advanced Threat Protection 계획 2를 추가 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="61444-149">If you see a different subscription, such as **Office 365 Enterprise E3** or **Office 365 Enterprise E1**, consider adding Office 365 Advanced Threat Protection Plan 2.</span></span> <span data-ttu-id="61444-150">이 작업을 수행 하려면 **+ 구독 추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-150">(To do that, choose **+ Add subscription**.)</span></span>
    
3. <span data-ttu-id="61444-151">Microsoft 365 관리 센터에서 **사용자** \> **활성 사용자**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-151">In the Microsoft 365 admin center, choose **Users** \> **Active users**.</span></span>
    
4. <span data-ttu-id="61444-152">모든 활성 사용자에 게 Office 365 Advanced Threat Protection 계획 2 라이선스를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-152">Assign Office 365 Advanced Threat Protection Plan 2 licenses to all active users.</span></span> <span data-ttu-id="61444-153">(이에 대 한 라이선스가 있는 사용자만 탐색기와 같은 보고서에 표시 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="61444-153">(Only users who have a license for this will show up in reports, such as Explorer.)</span></span>
    
5. <span data-ttu-id="61444-154">Office 365 Advanced Threat Protection으로 작업할 조직의 사용자에 게 역할을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="61444-154">Assign roles to people in your organization who will be working with the Office 365 Advanced Threat Protection.</span></span> <span data-ttu-id="61444-155">[사용자에 게 Office 365 보안 &amp; 및 준수 센터에 대 한 액세스 권한을 부여](grant-access-to-the-security-and-compliance-center.md)하 고 다음 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="61444-155">See [Give users access to the Office 365 Security &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md), and refer to the following table:</span></span><br/>

  |<span data-ttu-id="61444-156">**이 작업을 수행 하려면 ...**</span><span class="sxs-lookup"><span data-stu-id="61444-156">**To do this activity...**</span></span> <br/> |<span data-ttu-id="61444-157">**다음 역할 중 하나가 있어야 합니다.**</span><span class="sxs-lookup"><span data-stu-id="61444-157">**You must have one of these roles**</span></span> <br/> |  
  |:-----|:-----|
  |<span data-ttu-id="61444-158">위협 대시보드 (또는 새 [보안 대시보드](security-dashboard.md)) 사용</span><span class="sxs-lookup"><span data-stu-id="61444-158">Use the Threat dashboard (or the new [Security dashboard](security-dashboard.md))</span></span><br/> <span data-ttu-id="61444-159">최근 또는 현재 위협에 대 한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="61444-159">View information about recent or current threats</span></span>  <br/> |<span data-ttu-id="61444-160">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="61444-160">Office 365 Global Administrator</span></span>  <br/> <span data-ttu-id="61444-161">보안 관리자 (보안 &amp; 및 준수 센터에서 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="61444-161">Security Administrator (assigned in the Security &amp; Compliance Center)</span></span>  <br/> <span data-ttu-id="61444-162">보안 독자 (보안 &amp; 및 준수 센터에서 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="61444-162">Security Reader (assigned in the Security &amp; Compliance Center)</span></span>  <br/> |
  |<span data-ttu-id="61444-163">[위협 탐색기 (및 실시간 검색)](threat-explorer.md) 를 사용 하 여 위협 분석</span><span class="sxs-lookup"><span data-stu-id="61444-163">Use [Threat Explorer (and real-time detections)](threat-explorer.md) to analyze threats</span></span>  <br/> |<span data-ttu-id="61444-164">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="61444-164">Office 365 Global Administrator</span></span>  <br/> <span data-ttu-id="61444-165">보안 관리자 (보안 &amp; 및 준수 센터에서 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="61444-165">Security Administrator (assigned in the Security &amp; Compliance Center)</span></span>  <br/> <span data-ttu-id="61444-166">보안 독자 (보안 &amp; 및 준수 센터에서 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="61444-166">Security Reader (assigned in the Security &amp; Compliance Center)</span></span>  <br/> |
  |<span data-ttu-id="61444-167">인시던트 보기 (조사가 라고도 함)</span><span class="sxs-lookup"><span data-stu-id="61444-167">View Incidents (also referred to as Investigations)</span></span> <br/> <span data-ttu-id="61444-168">인시던트에 전자 메일 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="61444-168">Add email messages to an incident</span></span>  <br/> |<span data-ttu-id="61444-169">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="61444-169">Office 365 Global Administrator</span></span>  <br/> <span data-ttu-id="61444-170">보안 관리자 (보안 &amp; 및 준수 센터에서 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="61444-170">Security Administrator (assigned in the Security &amp; Compliance Center)</span></span>  <br/> <span data-ttu-id="61444-171">보안 독자 (보안 &amp; 및 준수 센터에서 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="61444-171">Security Reader (assigned in the Security &amp; Compliance Center)</span></span>  <br/> |
  |<span data-ttu-id="61444-172">인시던트에서 전자 메일 작업 트리거</span><span class="sxs-lookup"><span data-stu-id="61444-172">Trigger email actions in an incident</span></span>  <br/> <span data-ttu-id="61444-173">의심 스러운 전자 메일 메시지 찾기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="61444-173">Find and delete suspicious email messages</span></span>  <br/> |<span data-ttu-id="61444-174">Office 365 전역 관리자 또는 보안 관리자</span><span class="sxs-lookup"><span data-stu-id="61444-174">Office 365 Global Administrator or Security Administrator</span></span>  <br/> <span data-ttu-id="61444-175">위 역할과 검색 및 제거 (보안 &amp; 및 준수 센터에서 할당 됨) 중 하나</span><span class="sxs-lookup"><span data-stu-id="61444-175">One of the roles above and Search and Purge (assigned in the Security &amp; Compliance Center)</span></span>  <br/> |
  |<span data-ttu-id="61444-176">Microsoft Defender ATP에 Office 365 Advanced Threat Protection 계획 2 통합</span><span class="sxs-lookup"><span data-stu-id="61444-176">Integrate Office 365 Advanced Threat Protection Plan 2 with Microsoft Defender ATP</span></span>  <br/> <span data-ttu-id="61444-177">SIEM 서버를 사용 하 여 Office 365 Advanced Threat Protection 계획 2 통합</span><span class="sxs-lookup"><span data-stu-id="61444-177">Integrate Office 365 Advanced Threat Protection Plan 2 with a SIEM server</span></span>  <br/> |<span data-ttu-id="61444-178">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="61444-178">Office 365 Global Administrator</span></span>  <br/> <span data-ttu-id="61444-179">보안 관리자 (보안 &amp; 및 준수 센터에서 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="61444-179">Security Administrator (assigned in the Security &amp; Compliance Center)</span></span>  <br/> <span data-ttu-id="61444-180">추가 응용 프로그램에서 할당 되는 적절 한 역할 (예: Microsoft Defender 보안 센터 또는 SIEM server)</span><span class="sxs-lookup"><span data-stu-id="61444-180">Appropriate role assigned in additional applications (such as Microsoft Defender Security Center or a SIEM server)</span></span>  <br/> |
   
<span data-ttu-id="61444-181">역할, 역할 그룹 및 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="61444-181">For information about roles, role groups, and permissions, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="61444-182">다음 단계</span><span class="sxs-lookup"><span data-stu-id="61444-182">Next steps</span></span>

- [<span data-ttu-id="61444-183">위협 추적기에 대해 알아보기-신규 및 중요</span><span class="sxs-lookup"><span data-stu-id="61444-183">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)
    
- [<span data-ttu-id="61444-184">배달 된 악성 전자 메일 찾기 및 조사 (Office 365 위협 조사 및 응답)</span><span class="sxs-lookup"><span data-stu-id="61444-184">Find and investigate malicious email that was delivered (Office 365 Threat Investigation and Response)</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="61444-185">Microsoft Defender Advanced Threat Protection을 사용 하 여 Office 365 위협 조사 및 응답 통합</span><span class="sxs-lookup"><span data-stu-id="61444-185">Integrate Office 365 Threat Investigation and Response with Microsoft Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
- [<span data-ttu-id="61444-186">공격 시뮬레이터에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="61444-186">Learn about Attack Simulator</span></span>](attack-simulator.md)
  

