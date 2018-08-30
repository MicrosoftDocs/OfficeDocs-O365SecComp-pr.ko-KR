---
title: 감독 보고서
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 5/12/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2a762db5-e1c9-4c09-aa8e-bef49ce97209
description: 참조 하는 전자 메일을 보내는 감독 보고서를 사용 하 여 필요는 준수 검토 하 고 사용자는를 수행 해야 합니다.
ms.openlocfilehash: e18d083c0aad8be945c628516e593462da8e3898
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533096"
---
# <a name="supervision-reports"></a><span data-ttu-id="a82c3-103">감독 보고서</span><span class="sxs-lookup"><span data-stu-id="a82c3-103">Supervision reports</span></span>

<span data-ttu-id="a82c3-p101">감독 정책 정의 하는 조직에서 통신 준수를 위해 검토 필요 하 고 이러한 검토를 수행 하는 사용자입니다. 감독 보고서를 사용 하 여 정책 및 검토자 수준에서 검토 활동을 볼 수 있습니다. 각 정책에 대 한 검토 활동의 현재 상태에도 live 통계를 볼 수 있습니다. [감독 정책에 대 한 자세한 설명](configure-supervision-policies.md) 입니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-p101">Supervision policies define which communications in your organization need review for compliance, and who will perform those reviews. Use the supervision reports to see the review activity at the policy and reviewer level. For each policy, you can also view live statistics on the current state of review activity. [Learn more about supervision policies ](configure-supervision-policies.md) .</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a82c3-p102">감독 정책을 사용 하 여 조직에 대 한 Office 365 e 5를 구독을 해야 합니다. 해당 요금제에 가입한 상태 감독 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-p102">Using supervision policies requires an Office 365 E5 subscription for your organization. If you don't have that plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="a82c3-110">감독 보고서를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-110">You can use the supervision reports to:</span></span>
  
- <span data-ttu-id="a82c3-111">정책에 의도 한 대로 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-111">Verify that your policies are working as you intended.</span></span> 
    
- <span data-ttu-id="a82c3-112">검토를 위해 얼마나 많은 전자 메일을 식별 되는 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-112">Find out how many emails are being identified for review.</span></span>
    
- <span data-ttu-id="a82c3-p103">얼마나 많은 전자 메일이 없는 준수 확인 하 고 검토를 전달 하는 어떤 것입니다. 이 정보 정책에 세부적으로 조정 하거나 검토자의 수를 변경 하려면 여부를 결정 하는데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-p103">Find out how many emails aren't compliant and which ones are passing review. This information can help you decide whether to fine-tune your policies or change the number of reviewers.</span></span>
    
## <a name="view-the-supervision-report"></a><span data-ttu-id="a82c3-115">감독 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="a82c3-115">View the Supervision report</span></span>

1. <span data-ttu-id="a82c3-116">에 로그인 된 [보안 &amp; 준수 센터](https://protection.office.com/) 감독 보고서를 볼 수 있는 권한을 Office 365 조직에서 관리 계정에 대 한 자격 증명을 사용 하 여.</span><span class="sxs-lookup"><span data-stu-id="a82c3-116">Sign into the [Security &amp; Compliance Center](https://protection.office.com/) using the credentials for an admin account in your Office 365 organization that has permissions to view supervision reports..</span></span> 
    
2. <span data-ttu-id="a82c3-p104">**보고서** 로 이동 \> **대시보드**합니다. 감독에 대 한 보고 위젯을 확인 하 고 다른 보고서에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-p104">Go to **Reports** \> **Dashboard**. You'll see a reporting widget for supervision and other reports you have access to.</span></span>
    
3. <span data-ttu-id="a82c3-119">자세한 보고서 페이지를 열려면 **감독** 위젯을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-119">Click the **Supervision** widget to open the detailed report page.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="a82c3-p105">**보고서** 페이지에 액세스할 수 없는 경우 [조직에서 사용 가능한 감독 확인](configure-supervision-policies.md#SRavailable)의 설명에 따라를 자신이 감독 검토 역할 그룹의 구성원 있는지 확인 합니다. 이 역할 그룹 사용을 만들고 관리 감독에 포함 되 고 정책 및 보고서를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-p105">If you aren't able to access the **Reports** page, check that you're a member of the Supervisory Review role group, as described in [Make supervision available in your organization](configure-supervision-policies.md#SRavailable). Being included in this role group lets you create and manage supervision polices and run the report.</span></span> 
  
## <a name="how-to-use-the-report"></a><span data-ttu-id="a82c3-122">보고서를 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="a82c3-122">How to use the report</span></span>

<span data-ttu-id="a82c3-p106">Outlook 및 Outlook에서 검토자의 감독 폴더에는 전자 메일이 배달 감독 정책 검토를 위해 전자 메일을 식별 하는 경우 웹 응용 프로그램입니다. 이 보고서 검토 프로세스의 각 단계에서 각 정책의 이름 및 통신의 수를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-p106">When a supervision policy identifies an email for review, the email is delivered to the reviewer's Supervision folder in Outlook and Outlook web app. This report lists each policy's name and the number of communications at each stage in the review process.</span></span>
  
<span data-ttu-id="a82c3-125">보고서를 사용 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a82c3-125">Use the report to:</span></span>
  
- <span data-ttu-id="a82c3-126">모든 데이터를 볼 또는 특정 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-126">View data for all or specific policies.</span></span>
    
- <span data-ttu-id="a82c3-127">태그 유형 (예: 정책 준수, 명확 하지 않은 등), 검토자 또는 메시지 형식에 따라 그룹화 되는 데이터를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-127">View data grouped by tag type (such as Compliant, Questionable, etc.), reviewer, or message type.</span></span>
    
- <span data-ttu-id="a82c3-128">데이터를 CSV 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-128">Export data to a CSV file.</span></span>
    
- <span data-ttu-id="a82c3-129">검토 작업 날짜, 태그 유형, 검토자, 메시지 유형을 기준으로 데이터를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-129">Filter data based on review activity date, tag type, reviewer, message type.</span></span>
    
<span data-ttu-id="a82c3-130">**태그 유형** 열에 표시 될 값을 분석 하는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-130">Here's a breakdown of the values you might see in the **Tag type** column.</span></span> 
  
|<span data-ttu-id="a82c3-131">**태그 유형**</span><span class="sxs-lookup"><span data-stu-id="a82c3-131">**Tag type**</span></span>|<span data-ttu-id="a82c3-132">**의미**</span><span class="sxs-lookup"><span data-stu-id="a82c3-132">**What it means**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a82c3-133">검토 하지</span><span class="sxs-lookup"><span data-stu-id="a82c3-133">Not Reviewed</span></span>  <br/> |<span data-ttu-id="a82c3-p107">아직 검토 하지 않은 하는 전자 메일의 수입니다. 이러한 메일 기다리는 검토자의 감독 Outlook 폴더에 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-p107">The number of emails that have not been reviewed yet. These emails are awaiting review in the reviewer's supervision folder in Outlook.</span></span>  <br/> |
|<span data-ttu-id="a82c3-136">준수</span><span class="sxs-lookup"><span data-stu-id="a82c3-136">Compliant</span></span>  <br/> |<span data-ttu-id="a82c3-p108">전자 메일의 수를 검토 하 고 규격으로 표시 합니다. 없음 추가 작업이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-p108">The number of emails reviewed and marked as compliant. No further action is needed.</span></span>  <br/> |
|<span data-ttu-id="a82c3-139">의심 스러운</span><span class="sxs-lookup"><span data-stu-id="a82c3-139">Questionable</span></span>  <br/> |<span data-ttu-id="a82c3-p109">전자 메일의 수를 검토 하 고 의심 스러운 표시 합니다. 이것은 역할을 플래그입니다. 다른 검토자가 도움이 되는 전자 메일 규정 준수에 대 한 조사 해야 하는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-p109">The number of emails reviewed and marked questionable. This acts as a flag; other reviewers can help check whether an email needs investigation for compliance.</span></span>  <br/> |
|<span data-ttu-id="a82c3-142">비준수 (활성)</span><span class="sxs-lookup"><span data-stu-id="a82c3-142">Non-Compliant (Active)</span></span>  <br/> |<span data-ttu-id="a82c3-143">검토자를 조사 하는 현재는 비준수 전자 메일의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-143">The number of non-compliant emails that reviewers are currently investigating.</span></span>  <br/> |
|<span data-ttu-id="a82c3-144">비준수 (확인)</span><span class="sxs-lookup"><span data-stu-id="a82c3-144">Non-Compliant (Resolved)</span></span>  <br/> |<span data-ttu-id="a82c3-145">검토자를 조사 하 고 해결 하는 호환 이외의 전자 메일의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-145">The number of non-compliant emails that reviewers investigated and resolved.</span></span>  <br/> |
   
## <a name="more-details"></a><span data-ttu-id="a82c3-146">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="a82c3-146">More details</span></span>

- <span data-ttu-id="a82c3-147">감독 정책이이 보고서에 표시 되도록 하려면 프로 비전 먼저 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-147">Supervision policies must first be provisioned before they will appear in this report.</span></span>
    
- <span data-ttu-id="a82c3-p110">정책이 삭제 되 면 기록 데이터도 표시 됩니다. 그러나 중인 항목에 "존재 하지 않는 정책"으로 표시 된 및 **내보내기** 기능을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-p110">If policies are deleted, historical data is still shown. However, they're indicated as a "Non-existent policy", and the **Export** function isn't available.</span></span> 
    
- <span data-ttu-id="a82c3-p111">보고서는 기본적으로 모든 데이터를 표시 되지 않으면, 현재 날짜 범위에 표시할 데이터가 없으면 때문일 수 있습니다. 이러한 경우 날짜 범위를 변경 하려면 **필터** 컨트롤을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82c3-p111">If the report doesn't show any data by default, it might be because the current date range doesn't have any data to show. In these cases, use the **Filters** control to change the date range.</span></span> 
    

