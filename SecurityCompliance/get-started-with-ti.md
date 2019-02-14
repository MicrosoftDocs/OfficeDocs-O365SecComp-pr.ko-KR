---
title: Office 365 위협 인텔리전스 시작하기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 38e9b67f-d188-490f-bc91-a1ae4b270441
ms.collection:
- M365-security-compliance
description: Office 365 위협 인텔리전스 및 시작 하는 방법에 알아봅니다.
ms.openlocfilehash: f4480e6cdf5a845f591ad118858703dee4d4e631
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995239"
---
# <a name="get-started-with-office-365-advanced-threat-protection-plan-2-formerly-office-365-threat-intelligence"></a><span data-ttu-id="1d620-103">Office 365 고급 위협 보호 계획 2 (이전 Office 365 위협 인텔리전스) 시작 하기</span><span class="sxs-lookup"><span data-stu-id="1d620-103">Get started with Office 365 Advanced Threat Protection Plan 2 (formerly Office 365 Threat Intelligence)</span></span>

<span data-ttu-id="1d620-p101">조직의 보안 팀의 일부인 경우에 공격 으로부터 사용자를 보호 하기 위해 위협 인텔리전스 기능을 사용할 수 있습니다. Office 365 고급 위협 보호 계획 2 (이전 Office 365 위협 인텔리전스)를 사용 하면 보안 분석가 관리자 인 사이트를 버블링 하 여 사용자를 안전 하 게 유지 하 고에서 발생 하는 기능에 따라 작업을 식별 하는 Office 365 환경입니다. 이러한 정보는 위협 인텔리전스 데이터 및 동작 및 의심 스러운 활동 공격에 해당 하는 별색 패턴에는 시스템의 포괄적인 리포지토리를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-p101">If you are part of your organization's security team, you can use Threat Intelligence capabilities to protect your users from attacks. Office 365 Advanced Threat Protection Plan 2 (formerly Office 365 Threat Intelligence) helps security analysts and administrators keep users safe by bubbling up insights and identifying action based on what is happening in their your Office 365 environment. These insights are based on a comprehensive repository of threat intelligence data and systems to spot patterns that correspond to attack behaviors and suspicious activity.</span></span>
  
<span data-ttu-id="1d620-107">위협 인텔리전스 및 시작 하는 방법에 대 한 자세한 내용은이 문서를 읽어보십시오.</span><span class="sxs-lookup"><span data-stu-id="1d620-107">Read this article to learn more about Threat Intelligence and how to get started.</span></span>
  
## <a name="what-is-threat-intelligence"></a><span data-ttu-id="1d620-108">위협 인텔리전스 란?</span><span class="sxs-lookup"><span data-stu-id="1d620-108">What is Threat Intelligence?</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d620-p102">2019 년 2 월에에서 시작 하 고 향후 몇 개월 동안 롤아웃, Office 365 위협 인텔리전스는 되 고 Office 365 고급 위협 보호 계획 2, 추가 위협 보호 기능을 사용 합니다. 자세한 내용은 [Office 365 고급 위협 보호 계획 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [Office 365 고급 위협 Protection 서비스 설명](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1d620-p102">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>

<span data-ttu-id="1d620-p103">위협 인텔리전스는 insights (영문) 및 Office 365 보안에서 사용할 수 있는 정보의 모음 &amp; 준수 센터입니다. 이러한 정보는 공격 으로부터 Office 365 사용자를 보호 하는 조직의 보안 팀 데 도움이 됩니다. 위협 인텔리전스 신호를 모니터링 및 사용자 작업, 인증, 전자 메일, 손상 된 Pc 및 보안 문제 등의 여러 원본에서 데이터를 수집 합니다. 비즈니스 의사 결정권자 및 Office 365 전역 관리자, 보안 관리자 및 보안 분석가 모든 정보를 사용 하려면 Office 365 위협 인텔리전스 제공을 이해 하 고 Office 365의 사용자 및 지적에 대 한 위협을에 응답 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-p103">Threat Intelligence is a collection of insights and information available in the Office 365 Security &amp; Compliance Center. These insights can help your organization's security team protect Office 365 users from attacks. Threat Intelligence monitors signals and gathers data from multiple sources, such as user activity, authentication, email, compromised PCs, and security incidents. Business decision makers and Office 365 global administrators, security administrators, and security analysts can all use the information Office 365 Threat Intelligence provides to understand and respond to threats against Office 365 users and intellectual property.</span></span>
  
## <a name="get-acquainted-with-the-threat-dashboard-explorer-and-incidents"></a><span data-ttu-id="1d620-115">위협 대시보드, 탐색기 및 사고에 익숙해질</span><span class="sxs-lookup"><span data-stu-id="1d620-115">Get acquainted with the Threat dashboard, Explorer, and Incidents</span></span>

<span data-ttu-id="1d620-116">보안에서 인텔리전스 월등 위협 &amp; 도구 및 [위협 대시보드](get-started-with-ti.md#dashboard), [위협 탐색기](get-started-with-ti.md#explorer)및 [보안 문제](get-started-with-ti.md#incidents)를 포함 하 여 보고서의 집합으로 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-116">Threat Intelligence surfaces in the Security &amp; Compliance Center, as a set of tools and reports, including the [Threat dashboard](get-started-with-ti.md#dashboard), [Threat Explorer](get-started-with-ti.md#explorer), and [Incidents](get-started-with-ti.md#incidents).</span></span>
  
### <a name="threat-dashboard"></a><span data-ttu-id="1d620-117">위협 대시보드</span><span class="sxs-lookup"><span data-stu-id="1d620-117">Threat dashboard</span></span>

<span data-ttu-id="1d620-118">어떤 위협 사용할 수 있나요을 빠르게 살펴보려면 (이것은 라고도 [보안 대시보드](security-dashboard.md)) 위협 대시보드를 사용 하 고 비즈니스 의사 결정자를 보고서에는 시각적 방법으로 어떻게 Office 365 서비스를 보호 하 고 비즈니스 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-118">Use the Threat dashboard (this is also referred to as the [Security dashboard](security-dashboard.md)) to quickly see what threats have been addressed, and as a visual way to report to business decision makers how Office 365 services are securing your business.</span></span>
  
![위협 인텔리전스 대시보드](media/ce013a31-3f80-4d09-bb95-bfb7623b8bc4.png)
  
<span data-ttu-id="1d620-120">보고 하 여 보안에서이 대시보드를 사용 하 여 &amp; 준수 센터, **위협 관리로** 이동 \> **대시보드**합니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-120">To view and use this dashboard, in the Security &amp; Compliance Center, go to **Threat management** \> **Dashboard**.</span></span>
  
### <a name="threat-explorer"></a><span data-ttu-id="1d620-121">위협 탐색기</span><span class="sxs-lookup"><span data-stu-id="1d620-121">Threat Explorer</span></span>

<span data-ttu-id="1d620-p104">(이 라고도 탐색기) 위협 탐색기를 사용 하 여 위협 분석, 시간이 지남에 따라 공격의 볼륨을 참조 및 위협 제품군을 공격자가 인프라 하 여 데이터를 분석 합니다. 위협 탐색기는 모든 보안 분석가 조사 워크플로에 대 한 시작 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-p104">Use the Threat Explorer (this is also called Explorer) to analyze threats, see the volume of attacks over time, and analyze data by threat families, attacker infrastructure, and more. Threat Explorer is the starting place for any security analyst's investigation workflow.</span></span>
  
![위협 탐색기](media/7a7cecee-17f0-4134-bcb8-7cee3f3c3890.png)
  
<span data-ttu-id="1d620-125">보고 하 여이 보고서를 사용 하 여 보안에서 &amp; 준수 센터, **위협 관리로** 이동 \> **탐색기**입니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-125">To view and use this report, in the Security &amp; Compliance Center, go to **Threat management** \> **Explorer**.</span></span>
  
 ### <a name="incidents"></a><span data-ttu-id="1d620-126">보안 문제</span><span class="sxs-lookup"><span data-stu-id="1d620-126">Incidents</span></span>

<span data-ttu-id="1d620-p105">항공편 보안 문제에의 목록을 보려면 (라고도 조사) 인시던트 목록을 사용 합니다. 인시던트 의심 스러운 전자 메일 메시지와 같은 위협 요소를 추적 하 고 조사 및 수정 추가로 수행 하는 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-p105">Use the Incidents list (this is also called Investigations) to see a list of in flight security incidents. Incidents are used to track threats such as suspicious email messages, and to conduct further investigation and remediation.</span></span>
  
![Office 365 위협 인텔리전스에 현재 사고 목록](media/acadd4c7-d2de-4146-aeb8-90cfad805a9c.png)
  
<span data-ttu-id="1d620-130">보안에는 조직에 대 한 현재 사고 목록을 보려면 &amp; 준수 센터, **위협 관리로** 이동 \> **검토** \> **사고**합니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-130">To view the list of current incidents for your organization, in the Security &amp; Compliance Center, go to **Threat management** \> **Review** \> **Incidents**.</span></span>
  
![보안에서 &amp; 준수 센터 위협 관리를 선택 \> 검토](media/e0f46454-fa38-40f0-a120-b595614d1d22.png)
  
## <a name="learn-more-about-malware-amp-threats"></a><span data-ttu-id="1d620-132">맬웨어 하는 방법에 대 한 자세한 내용은 &amp; 위협</span><span class="sxs-lookup"><span data-stu-id="1d620-132">Learn more about Malware &amp; Threats</span></span>

<span data-ttu-id="1d620-p106">Office 365 고급 위협 보호 계획 2 구축의 일부로, 보안 분석가 알려진된 위협에 대 한 세부 정보를 검토할 수 있습니다. 추가 예방 조치/단계 사용자가 안전 하 게 유지를 수행할 수 있는 상태 인지 확인할 때 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-p106">As part of the Office 365 Advanced Threat Protection Plan 2 offering, security analysts can review details about a known threat. This is useful to determine whether there are additional preventative measures/steps that can be taken to keep users safe.</span></span>
  
![최근 위협에 대 한 정보를 표시 하는 보안 추세](media/11e7d40d-139b-4c56-8d52-c091c8654151.png) 
  
## <a name="how-do-we-get-threat-intelligence"></a><span data-ttu-id="1d620-136">위협 인텔리전스를 어떻게 얻을 수는?</span><span class="sxs-lookup"><span data-stu-id="1d620-136">How do we get Threat Intelligence?</span></span>

<span data-ttu-id="1d620-p107">**위협 인텔리전스 지금의 일부인 Office 365 고급 위협 보호 계획 2에**,이에 포함 된 [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 비즈니스](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, 예: 특정 구독에서 Office 365 교육 A5 등입니다. 조직에 Office 365 ATP 포함 되지 않은 구독을 하는 경우에 추가 기능으로 ATP을 잠재적으로 구입할 수 있습니다. 자세한 내용은 [Office 365 고급 위협 보호 계획 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [Office 365 고급 위협 Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1d620-p107">**Threat Intelligence is now part of in Office 365 Advanced Threat Protection Plan 2**, which is included in in certain subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on. For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span>
  
1. <span data-ttu-id="1d620-139">로 이동 하는 Office 365 전역 관리자 권한으로 [https://portal.office.com](https://portal.office.com) 및 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-139">As an Office 365 global administrator, go to [https://portal.office.com](https://portal.office.com) and sign in using your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="1d620-140">**관리자 \*\* \> \*\* 청구**을 선택하여 현재 구독에 포함된 내용을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-140">Choose **Admin** \> **Billing** to see what your current subscription includes.</span></span> 

    - <span data-ttu-id="1d620-141">**Office 365 Enterprise e 5**를 참조 하는 경우 조직에 Office 365 고급 위협 보호 계획 2, 위협 인텔리전스를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-141">If you see **Office 365 Enterprise E5**, then your organization has Office 365 Advanced Threat Protection Plan 2, which includes Threat Intelligence.</span></span> 
    - <span data-ttu-id="1d620-p108">**Office 365 엔터프라이즈 E3** 또는 **Office 365 Enterprise E1**등의 다른 구독을 참조 하는 경우에 위협 보호 계획 2 고급를 추가 하는 것이 좋습니다. (이 위해 선택 **+ 추가 구독**.)</span><span class="sxs-lookup"><span data-stu-id="1d620-p108">If you see a different subscription, such as **Office 365 Enterprise E3** or **Office 365 Enterprise E1**, consider adding Advanced Threat Protection Plan 2. (To do that, choose **+ Add subscription**.)</span></span>
    
3. <span data-ttu-id="1d620-144">Office 365 관리 센터에서 **사용자** \> **활성 사용자**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-144">In the Office 365 admin center, choose **Users** \> **Active users**.</span></span>
    
5. <span data-ttu-id="1d620-p109">모든 활성 사용자에 게 Office 365 고급 위협 보호 라이선스를 할당 합니다. (위협 인텔리전스 기능에 대 한 라이선스를 가진 사용자만 표시 탐색기와 같은 보고서, 합니다.)</span><span class="sxs-lookup"><span data-stu-id="1d620-p109">Assign Office 365 Advanced Threat Protection licenses to all active users. (Only users who have a license for Threat Intelligence capabilities will show up in reports, such as Explorer.)</span></span>
    
6. <span data-ttu-id="1d620-p110">Office 365 고급 위협 보호 사용 하면 조직에서 사람에 게 역할을 할당 합니다. 참조 [Office 365 보안에 사용자가 액세스할 수 있도록 &amp; 준수 센터](grant-access-to-the-security-and-compliance-center.md), 다음 표를 참조 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-p110">Assign roles to people in your organization who will be working with the Office 365 Advanced Threat Protection. See [Give users access to the Office 365 Security &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md), and refer to the following table:</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="1d620-149">**이 작업을 수행 하려면...**</span><span class="sxs-lookup"><span data-stu-id="1d620-149">**To do this activity...**</span></span> <br/> |<span data-ttu-id="1d620-150">**이러한 역할 중 하나가 필요**</span><span class="sxs-lookup"><span data-stu-id="1d620-150">**You must have one of these roles**</span></span> <br/> |
|<span data-ttu-id="1d620-151">위협 대시보드 (또는 새 [보안 대시보드](security-dashboard.md))를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="1d620-151">Use the Threat dashboard (or the new [Security dashboard](security-dashboard.md))</span></span>  <br/> <span data-ttu-id="1d620-152">최근 또는 현재 위협에 대 한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="1d620-152">View information about recent or current threats</span></span>  <br/> |<span data-ttu-id="1d620-153">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="1d620-153">Office 365 Global Administrator</span></span>  <br/> <span data-ttu-id="1d620-154">보안 관리자 (Azure Active Directory 관리 센터에 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="1d620-154">Security Administrator (assigned in the Azure Active Directory admin center)</span></span>  <br/> <span data-ttu-id="1d620-155">보안 판독기 (Azure Active Directory 관리 센터에 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="1d620-155">Security Reader (assigned in the Azure Active Directory admin center)</span></span>  <br/> |
|<span data-ttu-id="1d620-156">위협 탐색기 (탐색기 라고도 함)를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="1d620-156">Use Threat Explorer (also referred to as Explorer)</span></span>  <br/> <span data-ttu-id="1d620-157">위협 분석</span><span class="sxs-lookup"><span data-stu-id="1d620-157">Analyze threats</span></span>  <br/> |<span data-ttu-id="1d620-158">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="1d620-158">Office 365 Global Administrator</span></span>  <br/> <span data-ttu-id="1d620-159">보안 관리자 (보안에서 할당 된 &amp; 준수 센터)</span><span class="sxs-lookup"><span data-stu-id="1d620-159">Security Administrator (assigned in the Security &amp; Compliance Center)</span></span>  <br/> <span data-ttu-id="1d620-160">보안 판독기 (보안에서 할당 된 &amp; 준수 센터)</span><span class="sxs-lookup"><span data-stu-id="1d620-160">Security Reader (assigned in the Security &amp; Compliance Center)</span></span>  <br/> |
|<span data-ttu-id="1d620-161">보기 사고 (조사 라고도 함)</span><span class="sxs-lookup"><span data-stu-id="1d620-161">View Incidents (also referred to as Investigations)</span></span> <br/> <span data-ttu-id="1d620-162">인시던트를 전자 메일 메시지를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-162">Add email messages to an incident</span></span>  <br/> |<span data-ttu-id="1d620-163">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="1d620-163">Office 365 Global Administrator</span></span>  <br/> <span data-ttu-id="1d620-164">보안 관리자 (보안에서 할당 된 &amp; 준수 센터)</span><span class="sxs-lookup"><span data-stu-id="1d620-164">Security Administrator (assigned in the Security &amp; Compliance Center)</span></span>  <br/> <span data-ttu-id="1d620-165">보안 판독기 (보안에서 할당 된 &amp; 준수 센터)</span><span class="sxs-lookup"><span data-stu-id="1d620-165">Security Reader (assigned in the Security &amp; Compliance Center)</span></span>  <br/> |
|<span data-ttu-id="1d620-166">인시던트의 트리거 전자 메일 작업</span><span class="sxs-lookup"><span data-stu-id="1d620-166">Trigger email actions in an incident</span></span>  <br/> <span data-ttu-id="1d620-167">찾기 및 의심 스러운 전자 메일 메시지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-167">Find and delete suspicious email messages</span></span>  <br/> |<span data-ttu-id="1d620-168">Office 365 전역 관리자 또는 보안 관리자</span><span class="sxs-lookup"><span data-stu-id="1d620-168">Office 365 Global Administrator or Security Administrator</span></span>  <br/> <span data-ttu-id="1d620-169">위의 역할 및 검색 및 삭제 중 하나 (보안에서 할당 된 &amp; 준수 센터)</span><span class="sxs-lookup"><span data-stu-id="1d620-169">One of the roles above and Search and Purge (assigned in the Security &amp; Compliance Center)</span></span>  <br/> |
|<span data-ttu-id="1d620-170">Office 365 위협 인텔리전스와 Windows Defender Advanced Threat Protection 통합</span><span class="sxs-lookup"><span data-stu-id="1d620-170">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>  <br/> <span data-ttu-id="1d620-171">Office 365 위협 인텔리전스 SIEM 서버와 통합</span><span class="sxs-lookup"><span data-stu-id="1d620-171">Integrate Office 365 Threat Intelligence with a SIEM server</span></span>  <br/> |<span data-ttu-id="1d620-172">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="1d620-172">Office 365 Global Administrator</span></span>  <br/> <span data-ttu-id="1d620-173">보안 관리자 (보안에서 할당 된 &amp; 준수 센터)</span><span class="sxs-lookup"><span data-stu-id="1d620-173">Security Administrator (assigned in the Security &amp; Compliance Center)</span></span>  <br/> <span data-ttu-id="1d620-174">추가 응용 프로그램 (예: Windows Defender 고급 위협 보호 포털 또는 SIEM 서버)에 할당 된 적절 한 역할</span><span class="sxs-lookup"><span data-stu-id="1d620-174">Appropriate role assigned in additional applications (such as Windows Defender Advanced Threat Protection portal or a SIEM server)</span></span>  <br/> |
   
<span data-ttu-id="1d620-175">역할, 역할 그룹 및 권한을 하는 방법에 대 한 정보를 참조 하십시오. [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="1d620-175">For information about roles, role groups, and permissions, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="1d620-176">다음 단계</span><span class="sxs-lookup"><span data-stu-id="1d620-176">Next steps</span></span>

- [<span data-ttu-id="1d620-177">위협 추적기-새로 추가 되거나 주목할 만한 하는 방법에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="1d620-177">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)
    
- [<span data-ttu-id="1d620-178">찾기 및 악의적인 전자 메일 (Office 365 위협 인텔리전스) 지정 된 배달 하 게 조사</span><span class="sxs-lookup"><span data-stu-id="1d620-178">Find and investigate malicious email that was delivered (Office 365 Threat Intelligence)</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="1d620-179">Office 365 위협 인텔리전스와 Windows Defender Advanced Threat Protection 통합</span><span class="sxs-lookup"><span data-stu-id="1d620-179">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
- [<span data-ttu-id="1d620-180">공격 시뮬레이터 하는 방법에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="1d620-180">Learn about Attack Simulator</span></span>](attack-simulator.md)
  

