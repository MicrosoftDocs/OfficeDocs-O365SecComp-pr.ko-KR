---
title: 데이터 손실 방지에 대한 보고서 보기
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
description: Office 365의 dlp 보고서를 사용 하 여 dlp 정책 일치, 재정의 또는 가양성의 수를 빠르게 확인할 수 있습니다. 시간이 경과 함에 따라 작업 시간을 초과 하 고 있는지 여부를 확인할 수 있습니다. 다양 한 방법으로 보고서를 필터링 합니다. 그래프의 선에서 점을 선택 하 여 추가 세부 정보를 확인 합니다.
ms.openlocfilehash: 6f97a29b5a80eeff60b13ba4467d44e3ef87b028
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454850"
---
# <a name="view-the-reports-for-data-loss-prevention"></a><span data-ttu-id="8916f-103">데이터 손실 방지에 대한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="8916f-103">View the reports for data loss prevention</span></span>

<span data-ttu-id="8916f-104">DLP (데이터 손실 방지) 정책을 만든 후에는 해당 정책이 의도 한 대로 작동 하 고 준수 상태를 유지 하는 데 도움을 주려는 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-104">After you create your data loss prevention (DLP) policies, you'll want to verify that they're working as you intended and helping you to stay compliant.</span></span> <span data-ttu-id="8916f-105">Office 365 보안 &amp; 및 준수 센터의 DLP 보고서를 사용 하 여 다음을 빠르게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-105">With the DLP reports in the Office 365 Security &amp; Compliance Center, you can quickly view:</span></span>
  
- <span data-ttu-id="8916f-106">**DLP 정책 일치 항목** 이 보고서는 시간에 따른 DLP 정책 일치 항목의 수를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-106">**DLP policy matches** This report shows the count of DLP policy matches over time.</span></span> <span data-ttu-id="8916f-107">날짜, 위치, 정책 또는 작업을 기준으로 보고서를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-107">You can filter the report by date, location, policy, or action.</span></span> <span data-ttu-id="8916f-108">이 보고서를 사용 하 여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-108">You can use this report to:</span></span> 
    
  - <span data-ttu-id="8916f-109">테스트 모드에서 실행 하면서 DLP 정책을 조정 하거나 구체화 합니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-109">Tune or refine your DLP policies as you run them in test mode.</span></span> <span data-ttu-id="8916f-110">콘텐츠와 일치 하는 특정 규칙을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-110">You can view the specific rule that matched the content.</span></span>
    
  - <span data-ttu-id="8916f-111">특정 기간에 초점을 맞추고 스파이크 및 추세의 이유를 이해합니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-111">Focus on specific time periods and understand the reasons for spikes and trends.</span></span>
    
  - <span data-ttu-id="8916f-112">조직의 DLP 정책을 위반 하는 비즈니스 프로세스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-112">Discover business processes that violate your organization's DLP policies.</span></span>
    
  - <span data-ttu-id="8916f-113">콘텐츠에 적용 되는 작업을 확인 하 여 DLP 정책의 모든 업무상 영향을 이해 합니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-113">Understand any business impact of the DLP policies by seeing what actions are being applied to content.</span></span>
    
  - <span data-ttu-id="8916f-114">해당 정책에 대한 일치 항목을 표시하여 특정 DLP 정책에 대한 준수를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-114">Verify compliance with a specific DLP policy by showing any matches for that policy.</span></span>
    
  - <span data-ttu-id="8916f-115">상위 사용자 목록을 확인 하 고 조직의 사건에 기여 하는 사용자를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-115">View a list of top users and repeat users who are contributing to incidents in your organization.</span></span>
    
  - <span data-ttu-id="8916f-116">조직에서 가장 중요 한 정보 유형 목록을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-116">View a list of the top types of sensitive information in your organization.</span></span>
    
- <span data-ttu-id="8916f-117">**DLP 인시던트** 이 보고서에는 정책 일치 보고서와 같은 시간에 따른 정책 일치도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-117">**DLP incidents** This report also shows policy matches over time, like the policy matches report.</span></span> <span data-ttu-id="8916f-118">그러나 정책이 규칙 수준에서 일치 하는 항목을 표시 하는 것은 아닙니다. 예를 들어 전자 메일이 세 가지 다른 규칙과 일치 하는 경우 정책 일치 보고서에는 세 가지 다른 줄 항목이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-118">However, the policy matches report shows matches at a rule level; for example, if an email matched three different rules, the policy matches report shows three different line items.</span></span> <span data-ttu-id="8916f-119">반면 문제 보고서에는 항목 수준에서 일치 하는 항목이 표시 됩니다. 예를 들어 전자 메일이 세 가지 다른 규칙과 일치 하는 경우 문제 보고서에는 해당 콘텐츠에 대 한 단일 행 항목이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-119">By contrast, the incidents report shows matches at an item level; for example, if an email matched three different rules, the incidents report shows a single line item for that piece of content.</span></span> 
    
  <span data-ttu-id="8916f-120">보고서 개수가 서로 다르게 집계 되므로 정책 일치 보고서는 특정 규칙과 일치 하는 항목을 식별 하 고 DLP 정책을 세부적으로 조정 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-120">Because the report counts are aggregated differently, the policy matches report is better for identifying matches with specific rules and fine tuning DLP policies.</span></span> <span data-ttu-id="8916f-121">문제 보고서는 DLP 정책에 문제가 있는 특정 콘텐츠를 식별 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-121">The incidents report is better for identifying specific pieces of content that are problematic for your DLP policies.</span></span>
    
- <span data-ttu-id="8916f-122">**DLP 가양성 및 재정의** DLP 정책을 사용 하 여 사용자가이를 재정의 하거나 가양성을 보고할 수 있는 경우이 보고서에는 시간에 따른 이러한 인스턴스의 개수가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-122">**DLP false positives and overrides** If your DLP policy allows users to override it or report a false positive, this report shows a count of such instances over time.</span></span> <span data-ttu-id="8916f-123">날짜, 위치 또는 정책을 기준으로 보고서를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-123">You can filter the report by date, location, or policy.</span></span> <span data-ttu-id="8916f-124">이 보고서를 사용 하 여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-124">You can use this report to:</span></span> 
    
  - <span data-ttu-id="8916f-125">가양성을 많이 발생 하는 정책을 확인 하 여 DLP 정책을 조정 하거나 구체화 합니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-125">Tune or refine your DLP policies by seeing which policies incur a high number of false positives.</span></span>
    
  - <span data-ttu-id="8916f-126">사용자가 정책을 재정의 하 여 정책 팁을 확인할 때 제출한 근거를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-126">View the justifications submitted by users when they resolve a policy tip by overriding the policy.</span></span>
    
  - <span data-ttu-id="8916f-127">많은 수의 사용자 재정의를 발생 시켜 서 DLP 정책이 유효한 비즈니스 프로세스와 충돌 하는 위치를 파악 합니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-127">Discover where DLP policies conflict with valid business processes by incurring a high number of user overrides.</span></span>
    
<span data-ttu-id="8916f-128">모든 DLP 보고서는 최근 4 개월 동안의 데이터를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-128">All DLP reports can show data from the most recent four-month time period.</span></span> <span data-ttu-id="8916f-129">가장 최근 데이터가 보고서에 표시 되는 데 최대 24 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-129">The most recent data can take up to 24 hours to appear in the reports.</span></span>
  
<span data-ttu-id="8916f-130">보안 &amp; 및 준수 센터 \> **보고서** \> **대시보드에서**이러한 보고서를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-130">You can find these reports in the Security &amp; Compliance Center \> **Reports** \> **Dashboard**.</span></span>
  
![DLP 정책 일치 보고서](media/117d20c9-d379-403f-ad68-1f5cd6c4e5cf.png)
  
## <a name="view-the-justification-submitted-by-a-user-for-an-override"></a><span data-ttu-id="8916f-132">재정의를 위해 사용자가 전송한 사유 보기</span><span class="sxs-lookup"><span data-stu-id="8916f-132">View the justification submitted by a user for an override</span></span>

<span data-ttu-id="8916f-133">사용자가 DLP 정책에서이를 재정의할 수 있도록 허용 하는 경우 false 긍정 및 override 보고서를 사용 하 여 정책 설명에서 사용자가 전송한 텍스트를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-133">If your DLP policy allows users to override it, you can use the false positive and override report to view the text submitted by users in the policy tip.</span></span>
  
![DLP 거짓 긍정 및 재정의 보고서의 세부 정보에 있는 사유 필드](media/e11e3126-026d-4e77-a16d-74a0686d1fa3.png)
  
## <a name="take-action-on-insights-and-recommendations"></a><span data-ttu-id="8916f-135">정보 제공 및 권장 사항에 대 한 조치 수행</span><span class="sxs-lookup"><span data-stu-id="8916f-135">Take action on insights and recommendations</span></span>

<span data-ttu-id="8916f-136">보고서는 위험 경고 아이콘을 클릭 하 여 잠재적 문제에 대 한 세부 정보를 확인 하 고 해결 가능한 조치를 취할 수 있는 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-136">Reports can show insights and recommendations where you can click the red warning icon to see details about potential issues and take possible remedial action.</span></span>
  
![수행할 세부 정보 및 작업을 확인 하는 insights 아이콘 클릭](media/51782036-7299-4960-8175-75c2b1637159.png)
  
## <a name="find-the-cmdlets-for-the-dlp-reports"></a><span data-ttu-id="8916f-138">DLP 보고서용 cmdlet 찾기</span><span class="sxs-lookup"><span data-stu-id="8916f-138">Find the cmdlets for the DLP reports</span></span>

<span data-ttu-id="8916f-139">보안 &amp; 및 준수 센터에 대 한 cmdlet을 대부분 사용 하려면 다음 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-139">To use most of the cmdlets for the Security &amp; Compliance Center, you need to:</span></span>
  
1. [<span data-ttu-id="8916f-140">원격 PowerShell을 사용하여 Office 365 보안 및 준수 센터에 연결</span><span class="sxs-lookup"><span data-stu-id="8916f-140">Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell</span></span>](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. <span data-ttu-id="8916f-141">다음 [Office 365 보안 &amp; 및 준수 센터 cmdlet](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409) 사용</span><span class="sxs-lookup"><span data-stu-id="8916f-141">Use any of these [Office 365 Security &amp; Compliance Center cmdlets](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)</span></span>
    
<span data-ttu-id="8916f-142">그러나 DLP 보고서는 Exchange Online을 포함 하 여 Office 365 간에 데이터를 가져올 필요가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-142">However, DLP reports need pull data from across Office 365, including Exchange Online.</span></span> <span data-ttu-id="8916f-143">이러한 이유로 DLP 보고서용 cmdlet은 보안 &amp; 및 준수 센터 powershell이 아닌 Exchange Online Powershell에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-143">For this reason, the cmdlets for the DLP reports are available in Exchange Online Powershell—not in Security &amp; Compliance Center Powershell.</span></span> <span data-ttu-id="8916f-144">따라서 DLP 보고서에 대해 cmdlet을 사용 하려면 다음을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-144">Therefore, to use the cmdlets for the DLP reports, you need to:</span></span>
  
1. <span data-ttu-id="8916f-145">[Connect to Exchange Online using remote PowerShell](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)(원격 PowerShell을 사용하여 Exchange Online에 연결)</span><span class="sxs-lookup"><span data-stu-id="8916f-145">[Connect to Exchange Online using remote PowerShell](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)</span></span>
    
2. <span data-ttu-id="8916f-146">DLP 보고서에 대해 다음 cmdlet 중 하나를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8916f-146">Use any of these cmdlets for the DLP reports:</span></span>
    
      - [<span data-ttu-id="8916f-147">get-dlpdetectionsreport</span><span class="sxs-lookup"><span data-stu-id="8916f-147">Get-DlpDetectionsReport</span></span>](http://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
      - [<span data-ttu-id="8916f-148">get-dlpdetailreport</span><span class="sxs-lookup"><span data-stu-id="8916f-148">Get-DlpDetailReport</span></span>](http://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    

