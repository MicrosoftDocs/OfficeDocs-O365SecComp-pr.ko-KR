---
title: Office 365 위협 인텔리전스 시작하기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 38e9b67f-d188-490f-bc91-a1ae4b270441
ms.collection:
- M365-security-compliance
description: Office 365 위협 인텔리전스 및 시작 방법에 대해 알아봅니다.
ms.openlocfilehash: f116b7a01ab3b27760b597527cc1e5a4440a6586
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217858"
---
# <a name="get-started-with-threat-intelligence"></a><span data-ttu-id="2ce20-103">위협 인텔리전스 시작</span><span class="sxs-lookup"><span data-stu-id="2ce20-103">Get started with Threat Intelligence</span></span>

<span data-ttu-id="2ce20-p101">조직의 보안 팀에 속해 있는 경우 위협 인텔리전스 기능을 사용 하 여 공격 으로부터 사용자를 보호할 수 있습니다. office 365 Advanced threat Protection 계획 2 (이전의 office 365 위협 인텔리전스)에서는 보안 분석가와 관리자가 사용자에 게 정보를 버블링 하 고 Office 365 환경에서 발생 하는 작업을 식별 하는 방법을 제공 하는 방법을 제공 합니다. 이러한 정보는 위협 인텔리전스 데이터 및 시스템에 대 한 포괄적인 리포지토리를 기반으로 공격 동작과 의심 스러운 활동에 해당 하는 패턴을 강조 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ce20-p101">If you are part of your organization's security team, you can use Threat Intelligence capabilities to protect your users from attacks. Office 365 Advanced Threat Protection Plan 2 (formerly Office 365 Threat Intelligence) helps security analysts and administrators keep users safe by bubbling up insights and identifying action based on what is happening in their your Office 365 environment. These insights are based on a comprehensive repository of threat intelligence data and systems to spot patterns that correspond to attack behaviors and suspicious activity.</span></span>
  
<span data-ttu-id="2ce20-107">이 문서를 읽으면 위협 인텔리전스 및 시작 방법에 대해 자세히 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ce20-107">Read this article to learn more about Threat Intelligence and how to get started.</span></span>
  
## <a name="what-is-threat-intelligence"></a><span data-ttu-id="2ce20-108">위협 인텔리전스 란?</span><span class="sxs-lookup"><span data-stu-id="2ce20-108">What is Threat Intelligence?</span></span>

<span data-ttu-id="2ce20-p102">위협 인텔리전스는 Office 365 보안 &amp; 및 준수 센터에서 제공 되는 정보 활용 및 정보의 모음입니다. 이러한 통찰력은 조직의 보안 팀이 공격 으로부터 Office 365 사용자를 보호 하는 데 도움이 될 수 있습니다. 위협 인텔리전스 모니터는 사용자 활동, 인증, 전자 메일, 손상 된 pc 및 보안 인시던트와 같은 여러 원본의 데이터를 신호 및 수집 합니다. 비즈니스 의사 결정권자 및 office 365 전역 관리자, 보안 관리자 및 보안 분석가는 office 365 위협 인텔리전스가 제공 하는 모든 정보를 사용 하 여 office 365 사용자 및 지적에 대 한 위협을 이해 하 고 대응 시킬 수 있습니다. property.</span><span class="sxs-lookup"><span data-stu-id="2ce20-p102">Threat Intelligence is a collection of insights and information available in the Office 365 Security &amp; Compliance Center. These insights can help your organization's security team protect Office 365 users from attacks. Threat Intelligence monitors signals and gathers data from multiple sources, such as user activity, authentication, email, compromised PCs, and security incidents. Business decision makers and Office 365 global administrators, security administrators, and security analysts can all use the information Office 365 Threat Intelligence provides to understand and respond to threats against Office 365 users and intellectual property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ce20-p103">2019 년 2 월에 시작 해 서 향후 몇 개월 동안 롤아웃 되는 office 365 위협 인텔리전스는 추가 위협 방지 기능을 사용 하 여 office 365 Advanced threat protection 계획 2가 됩니다. 자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ce20-p103">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
## <a name="get-acquainted-with-the-threat-dashboard-explorer-and-incidents"></a><span data-ttu-id="2ce20-115">위협 대시보드, 탐색기 및 인시던트 숙지</span><span class="sxs-lookup"><span data-stu-id="2ce20-115">Get acquainted with the Threat dashboard, Explorer, and Incidents</span></span>

<span data-ttu-id="2ce20-116">보안 &amp; 및 준수 센터의 위협 인텔리전스 화면 [위협 대시보드](get-started-with-ti.md#dashboard), [위협 탐색기](get-started-with-ti.md#explorer)및 [인시던트](get-started-with-ti.md#incidents)를 포함 한 도구 및 보고서 집합으로,</span><span class="sxs-lookup"><span data-stu-id="2ce20-116">Threat Intelligence surfaces in the Security &amp; Compliance Center, as a set of tools and reports, including the [Threat dashboard](get-started-with-ti.md#dashboard), [Threat Explorer](get-started-with-ti.md#explorer), and [Incidents](get-started-with-ti.md#incidents).</span></span>
  
### <a name="threat-dashboard"></a><span data-ttu-id="2ce20-117">위협 대시보드</span><span class="sxs-lookup"><span data-stu-id="2ce20-117">Threat dashboard</span></span>

<span data-ttu-id="2ce20-118">위협 대시보드 ( [보안 대시보드](security-dashboard.md)라고도 함)를 사용 하 여 해결 된 위협을 빠르게 확인 하 고, Office 365 서비스가 비즈니스를 보호 하는 방법을 비즈니스 의사 결정권자에 게 보고 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ce20-118">Use the Threat dashboard (this is also referred to as the [Security dashboard](security-dashboard.md)) to quickly see what threats have been addressed, and as a visual way to report to business decision makers how Office 365 services are securing your business.</span></span>
  
![위협 인텔리전스 대시보드](media/ce013a31-3f80-4d09-bb95-bfb7623b8bc4.png)
  
<span data-ttu-id="2ce20-120">이 대시보드 &amp; 를 보고 사용 하려면 보안 및 준수 센터에서 **위협 관리** \> **대시보드로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ce20-120">To view and use this dashboard, in the Security &amp; Compliance Center, go to **Threat management** \> **Dashboard**.</span></span>
  
### <a name="threat-explorer"></a><span data-ttu-id="2ce20-121">위협 탐색기</span><span class="sxs-lookup"><span data-stu-id="2ce20-121">Threat Explorer</span></span>

<span data-ttu-id="2ce20-p104">위협 탐색기 (이 라고도 함)를 사용 하 여 위협을 분석 하 고, 시간에 따른 공격 량을 확인 하 고, 위협 계열, 침입자 인프라 등을 기준으로 데이터를 분석 합니다. 위협 탐색기는 모든 보안 분석가의 조사 워크플로에서 시작 되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2ce20-p104">Use the Threat Explorer (this is also called Explorer) to analyze threats, see the volume of attacks over time, and analyze data by threat families, attacker infrastructure, and more. Threat Explorer is the starting place for any security analyst's investigation workflow.</span></span>
  
![위협 탐색기](media/7a7cecee-17f0-4134-bcb8-7cee3f3c3890.png)
  
<span data-ttu-id="2ce20-125">이 보고서 &amp; 를 보고 사용 하려면 보안 및 준수 센터에서 **위협 관리** \> **탐색기**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ce20-125">To view and use this report, in the Security &amp; Compliance Center, go to **Threat management** \> **Explorer**.</span></span>
  
 ### <a name="incidents"></a><span data-ttu-id="2ce20-126">인시던트</span><span class="sxs-lookup"><span data-stu-id="2ce20-126">Incidents</span></span>

<span data-ttu-id="2ce20-p105">문제 목록 (조사가 라고도 함)을 사용 하 여 비행 보안 인시던트 목록을 확인 합니다. 인시던트는 의심 스러운 전자 메일 메시지와 같은 위협을 추적 하 고 추가 조사 및 수정을 수행 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ce20-p105">Use the Incidents list (this is also called Investigations) to see a list of in flight security incidents. Incidents are used to track threats such as suspicious email messages, and to conduct further investigation and remediation.</span></span>
  
![Office 365 위협 인텔리전스의 현재 인시던트 목록](media/acadd4c7-d2de-4146-aeb8-90cfad805a9c.png)
  
<span data-ttu-id="2ce20-130">조직의 현재 인시던트 &amp; 목록을 보려면 보안 및 준수 센터에서 **위협 관리** \> **검토** \> **인시던트**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ce20-130">To view the list of current incidents for your organization, in the Security &amp; Compliance Center, go to **Threat management** \> **Review** \> **Incidents**.</span></span>
  
![보안 &amp; 및 준수 센터에서 위협 관리 \> 검토를 선택 합니다.](media/e0f46454-fa38-40f0-a120-b595614d1d22.png)
  
## <a name="learn-more-about-malware-amp-threats"></a><span data-ttu-id="2ce20-132">맬웨어 &amp; 위협에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="2ce20-132">Learn more about Malware &amp; Threats</span></span>

<span data-ttu-id="2ce20-p106">보안 분석가는 Office 365 Advanced Threat Protection 계획 2 제공의 일부로 알려진 위협에 대 한 세부 정보를 검토할 수 있습니다. 이 기능은 사용자가 안전 하 게 유지 하기 위해 수행할 수 있는 추가 예방 조치/단계가 있는지 여부를 확인 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ce20-p106">As part of the Office 365 Advanced Threat Protection Plan 2 offering, security analysts can review details about a known threat. This is useful to determine whether there are additional preventative measures/steps that can be taken to keep users safe.</span></span>
  
![최근 위협에 대 한 정보를 보여 주는 보안 경향](media/11e7d40d-139b-4c56-8d52-c091c8654151.png) 
  
## <a name="how-do-we-get-threat-intelligence"></a><span data-ttu-id="2ce20-136">위협 인텔리전스를 어떻게 얻을 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="2ce20-136">How do we get Threat Intelligence?</span></span>

<span data-ttu-id="2ce20-p107">위협 인텔리전스는 이제 [microsoft 365 enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), office 365 Enterprise E5, office 365과 같은 특정 구독에 포함 된 **Office 365 Advanced Threat Protection 계획 2의 일부**입니다. 교육 A5 등 조직에서 Office 365 ATP를 포함 하지 않는 구독을 사용 하는 경우 ATP를 추가 기능으로 구입할 수 있습니다. 자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ce20-p107">**Threat Intelligence is now part of in Office 365 Advanced Threat Protection Plan 2**, which is included in in certain subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on. For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span>
  
1. <span data-ttu-id="2ce20-139">office 365 전역 관리자 인 경우로 이동 [https://portal.office.com](https://portal.office.com) 하 여 office 365에 대 한 회사 또는 학교 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ce20-139">As an Office 365 global administrator, go to [https://portal.office.com](https://portal.office.com) and sign in using your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="2ce20-140">**관리자 \*\* \> \*\* 청구**을 선택하여 현재 구독에 포함된 내용을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="2ce20-140">Choose **Admin** \> **Billing** to see what your current subscription includes.</span></span> 

    - <span data-ttu-id="2ce20-141">**office 365 Enterprise**e 5가 표시 되 면 조직에 위협 인텔리전스를 포함 하는 Office 365 Advanced Threat Protection 계획 2가 있는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="2ce20-141">If you see **Office 365 Enterprise E5**, then your organization has Office 365 Advanced Threat Protection Plan 2, which includes Threat Intelligence.</span></span> 
    - <span data-ttu-id="2ce20-p108">**office 365 enterprise E3** 또는 **office 365 enterprise E1**과 같은 다른 구독이 표시 되는 경우 Advanced Threat Protection 계획 2를 추가 하는 것이 좋습니다. 이 작업을 수행 하려면 **+ 구독 추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ce20-p108">If you see a different subscription, such as **Office 365 Enterprise E3** or **Office 365 Enterprise E1**, consider adding Advanced Threat Protection Plan 2. (To do that, choose **+ Add subscription**.)</span></span>
    
3. <span data-ttu-id="2ce20-144">Office 365 관리 센터에서 **사용자** \> **활성 사용자**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2ce20-144">In the Office 365 admin center, choose **Users** \> **Active users**.</span></span>
    
5. <span data-ttu-id="2ce20-p109">모든 활성 사용자에 게 Office 365 Advanced Threat Protection 라이선스를 할당 합니다. (위협 인텔리전스 기능에 대 한 라이선스가 있는 사용자만 보고서 (예: Explorer)에 표시 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="2ce20-p109">Assign Office 365 Advanced Threat Protection licenses to all active users. (Only users who have a license for Threat Intelligence capabilities will show up in reports, such as Explorer.)</span></span>
    
6. <span data-ttu-id="2ce20-p110">Office 365 Advanced Threat Protection으로 작업할 조직의 사용자에 게 역할을 할당 합니다. [사용자에 게 Office 365 보안 &amp; 및 준수 센터에 대 한 액세스 권한을 부여](grant-access-to-the-security-and-compliance-center.md)하 고 다음 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ce20-p110">Assign roles to people in your organization who will be working with the Office 365 Advanced Threat Protection. See [Give users access to the Office 365 Security &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md), and refer to the following table:</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="2ce20-149">**이 작업을 수행 하려면 ...**</span><span class="sxs-lookup"><span data-stu-id="2ce20-149">**To do this activity...**</span></span> <br/> |<span data-ttu-id="2ce20-150">**다음 역할 중 하나가 있어야 합니다.**</span><span class="sxs-lookup"><span data-stu-id="2ce20-150">**You must have one of these roles**</span></span> <br/> |
|<span data-ttu-id="2ce20-151">위협 대시보드 (또는 새 [보안 대시보드](security-dashboard.md)) 사용</span><span class="sxs-lookup"><span data-stu-id="2ce20-151">Use the Threat dashboard (or the new [Security dashboard](security-dashboard.md))</span></span>  <br/> <span data-ttu-id="2ce20-152">최근 또는 현재 위협에 대 한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="2ce20-152">View information about recent or current threats</span></span>  <br/> |<span data-ttu-id="2ce20-153">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="2ce20-153">Office 365 Global Administrator</span></span>  <br/> <span data-ttu-id="2ce20-154">보안 관리자 (Azure Active Directory 관리 센터에서 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="2ce20-154">Security Administrator (assigned in the Azure Active Directory admin center)</span></span>  <br/> <span data-ttu-id="2ce20-155">보안 독자 (Azure Active Directory 관리 센터에서 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="2ce20-155">Security Reader (assigned in the Azure Active Directory admin center)</span></span>  <br/> |
|<span data-ttu-id="2ce20-156">위협 탐색기 (탐색기 라고도 함) 사용</span><span class="sxs-lookup"><span data-stu-id="2ce20-156">Use Threat Explorer (also referred to as Explorer)</span></span>  <br/> <span data-ttu-id="2ce20-157">위협 분석</span><span class="sxs-lookup"><span data-stu-id="2ce20-157">Analyze threats</span></span>  <br/> |<span data-ttu-id="2ce20-158">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="2ce20-158">Office 365 Global Administrator</span></span>  <br/> <span data-ttu-id="2ce20-159">보안 관리자 (보안 &amp; 및 준수 센터에서 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="2ce20-159">Security Administrator (assigned in the Security &amp; Compliance Center)</span></span>  <br/> <span data-ttu-id="2ce20-160">보안 독자 (보안 &amp; 및 준수 센터에서 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="2ce20-160">Security Reader (assigned in the Security &amp; Compliance Center)</span></span>  <br/> |
|<span data-ttu-id="2ce20-161">인시던트 보기 (조사가 라고도 함)</span><span class="sxs-lookup"><span data-stu-id="2ce20-161">View Incidents (also referred to as Investigations)</span></span> <br/> <span data-ttu-id="2ce20-162">인시던트에 전자 메일 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="2ce20-162">Add email messages to an incident</span></span>  <br/> |<span data-ttu-id="2ce20-163">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="2ce20-163">Office 365 Global Administrator</span></span>  <br/> <span data-ttu-id="2ce20-164">보안 관리자 (보안 &amp; 및 준수 센터에서 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="2ce20-164">Security Administrator (assigned in the Security &amp; Compliance Center)</span></span>  <br/> <span data-ttu-id="2ce20-165">보안 독자 (보안 &amp; 및 준수 센터에서 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="2ce20-165">Security Reader (assigned in the Security &amp; Compliance Center)</span></span>  <br/> |
|<span data-ttu-id="2ce20-166">인시던트에서 전자 메일 작업 트리거</span><span class="sxs-lookup"><span data-stu-id="2ce20-166">Trigger email actions in an incident</span></span>  <br/> <span data-ttu-id="2ce20-167">의심 스러운 전자 메일 메시지 찾기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="2ce20-167">Find and delete suspicious email messages</span></span>  <br/> |<span data-ttu-id="2ce20-168">Office 365 전역 관리자 또는 보안 관리자</span><span class="sxs-lookup"><span data-stu-id="2ce20-168">Office 365 Global Administrator or Security Administrator</span></span>  <br/> <span data-ttu-id="2ce20-169">위 역할과 검색 및 제거 (보안 &amp; 및 준수 센터에서 할당 됨) 중 하나</span><span class="sxs-lookup"><span data-stu-id="2ce20-169">One of the roles above and Search and Purge (assigned in the Security &amp; Compliance Center)</span></span>  <br/> |
|<span data-ttu-id="2ce20-170">Office 365 위협 인텔리전스와 Windows Defender Advanced Threat Protection 통합</span><span class="sxs-lookup"><span data-stu-id="2ce20-170">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>  <br/> <span data-ttu-id="2ce20-171">siem 서버에 Office 365 위협 인텔리전스 통합</span><span class="sxs-lookup"><span data-stu-id="2ce20-171">Integrate Office 365 Threat Intelligence with a SIEM server</span></span>  <br/> |<span data-ttu-id="2ce20-172">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="2ce20-172">Office 365 Global Administrator</span></span>  <br/> <span data-ttu-id="2ce20-173">보안 관리자 (보안 &amp; 및 준수 센터에서 할당 됨)</span><span class="sxs-lookup"><span data-stu-id="2ce20-173">Security Administrator (assigned in the Security &amp; Compliance Center)</span></span>  <br/> <span data-ttu-id="2ce20-174">추가 응용 프로그램에서 할당 되는 적절 한 역할 (예: Windows Defender Advanced Threat Protection portal 또는 siem server)</span><span class="sxs-lookup"><span data-stu-id="2ce20-174">Appropriate role assigned in additional applications (such as Windows Defender Advanced Threat Protection portal or a SIEM server)</span></span>  <br/> |
   
<span data-ttu-id="2ce20-175">역할, 역할 그룹 및 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ce20-175">For information about roles, role groups, and permissions, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="2ce20-176">다음 단계</span><span class="sxs-lookup"><span data-stu-id="2ce20-176">Next steps</span></span>

- [<span data-ttu-id="2ce20-177">위협 추적기에 대해 알아보기-신규 및 중요</span><span class="sxs-lookup"><span data-stu-id="2ce20-177">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)
    
- [<span data-ttu-id="2ce20-178">배달 된 악성 전자 메일 찾기 및 조사 (Office 365 위협 인텔리전스)</span><span class="sxs-lookup"><span data-stu-id="2ce20-178">Find and investigate malicious email that was delivered (Office 365 Threat Intelligence)</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="2ce20-179">Office 365 위협 인텔리전스와 Windows Defender Advanced Threat Protection 통합</span><span class="sxs-lookup"><span data-stu-id="2ce20-179">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
- [<span data-ttu-id="2ce20-180">공격 시뮬레이터에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="2ce20-180">Learn about Attack Simulator</span></span>](attack-simulator.md)
  

