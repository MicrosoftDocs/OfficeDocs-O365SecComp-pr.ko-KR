---
title: Office 365 고급 위협 보호에 대 한 보고서 보기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 08/06/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
description: 찾기 및 보안에서 Office 365 고급 위협 보호에 대 한 보고서를 사용 하는 방법에 알아봅니다 &amp; 준수 센터입니다.
ms.openlocfilehash: bd02989711629cc67f7a7d5e061862a1146ff21b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533330"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a><span data-ttu-id="a6e14-103">Office 365 고급 위협 보호에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="a6e14-103">View reports for Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="a6e14-p101">보안에서 여러 ATP 보고서를 사용할 수 조직에 [Office 365 고급 위협 보호](office-365-atp.md) (ATP) 하는 경우 필요한 권한을 &amp; 준수 센터입니다. ( **보고서** 로 이동 \> **대시보드**.)</span><span class="sxs-lookup"><span data-stu-id="a6e14-p101">If your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) and you have the necessary permissions, you can use several ATP reports in the Security &amp; Compliance Center. (Go to **Reports** \> **Dashboard**.)</span></span>
  
![보안 &amp; 준수 센터 대시보드 도울수 위협 보호 고급가 작동 하는 위치를 참조 하십시오.](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="a6e14-p102">ATP 보고서 [위협 보호 상태 보고서](view-reports-for-atp.md#advancedthreats), [ATP 파일 형식 보고서](view-reports-for-atp.md#atpfiletypes)및 [ATP 메시지 처리 보고서](view-reports-for-atp.md#atpmessagedisp)를 포함 합니다. 이 문서 ATP 보고서에 설명 하 고 [보려는 추가 보고서](view-reports-for-atp.md#addl)에 대 한 링크를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-p102">ATP reports include the [Threat protection status report](view-reports-for-atp.md#advancedthreats), the [ATP File Types report](view-reports-for-atp.md#atpfiletypes), and the [ATP Message Disposition report](view-reports-for-atp.md#atpmessagedisp). This article describes the ATP reports and includes links to [Additional reports to view](view-reports-for-atp.md#addl).</span></span>
  
## <a name="threat-protection-status-report"></a><span data-ttu-id="a6e14-109">위협 보호 상태 보고서</span><span class="sxs-lookup"><span data-stu-id="a6e14-109">Threat protection status report</span></span>

<span data-ttu-id="a6e14-p103">**위협 보호 상태** 보고서에는 함께 악의적인 콘텐츠 및 악의적인 전자 메일 감지 및 Exchange Online 및 고급 위협 보호에 의해 차단 하는 방법에 대 한 정보를 제공 하는 단일 보기입니다. 보고서에서 제공 하는 집계 된 횟수가 악의적인 콘텐츠가 포함 된 (파일 또는 Url) 맬웨어 방지 엔진, [0-시간 자동 삭제 (ZAP)](zero-hour-auto-purge.md), 및 [ATP 안전한 링크](atp-safe-links.md), [ATP 등의 고급 위협 보호 기능에 의해 차단 되는 고유한 전자 메일 메시지 안전한 첨부 파일](atp-safe-attachments.md), 및 [Office 365의 ATP 피싱 방지 기능](atp-anti-phishing.md)입니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-p103">The **Threat protection status** report is a single view that brings together information about malicious content and malicious email detected and blocked by Exchange Online and Advanced Threat Protection. The report provides an aggregated count of unique email messages with malicious content (files or URLs) blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and Advanced Threat Protection features, such as [ATP Safe Links](atp-safe-links.md), [ATP Safe Attachments](atp-safe-attachments.md), and [ATP anti-phishing capabilities in Office 365](atp-anti-phishing.md).</span></span>
  
<span data-ttu-id="a6e14-112">보안에서 위협 보호 상태 보고서를 보려면 &amp; 준수 센터, **보고서** 로 이동 \> **대시보드** \> **위협 보호 상태**입니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-112">To view the Threat protection status report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **Threat protection status**.</span></span>
  
![ATP 위협 보호 상태 보고서](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
<span data-ttu-id="a6e14-114">하루에 대 한 자세한 상태를 가져올, 그래프를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-114">To get detailed status for a day, hover over the graph.</span></span>
  
![하루에 대 한 ATP 위협 보호 상태 데이터](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
<span data-ttu-id="a6e14-p104">기본적으로 위협 보호 상태 보고서는 지난 7 일간에 대 한 데이터를 표시 합니다. 그러나 **필터** 를 선택 하 고 최대 90 일 동안 데이터를 보려는 날짜 범위를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-p104">By default, the Threat protection status report shows data for the past seven days. However, you can choose **Filters** and change the date range to view data for up to 90 days.</span></span> 
  
![ATP 위협 보호 상태 필터입니다.](media/4f703369-642b-402b-9758-b9c828283410.png)
  
<span data-ttu-id="a6e14-119">또한 보고서에 표시 되는 정보를 변경 하 **여 데이터 보기** 메뉴를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-119">You can also use the **View data by** menu to change what information is displayed in the report.</span></span> 
  
![ATP 위협 보호 상태 보고서에 대 한 표시 옵션](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a><span data-ttu-id="a6e14-121">ATP 파일 형식 보고서</span><span class="sxs-lookup"><span data-stu-id="a6e14-121">ATP File Types report</span></span>

<span data-ttu-id="a6e14-122">**ATP 파일 형식** 보고서 [ATP 안전한 첨부](atp-safe-attachments.md)하 여 악의적으로 감지 하는 파일의 종류를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-122">The **ATP File Types** report shows you the type of files detected as malicious by [ATP Safe Attachments](atp-safe-attachments.md).</span></span>
  
<span data-ttu-id="a6e14-123">보안에이 보고서를 보려면 &amp; 준수 센터, **보고서** 로 이동 \> **대시보드** \> **ATP 파일 형식**입니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-123">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **ATP File Types**.</span></span>
  
![ATP 파일 형식 보고서](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
<span data-ttu-id="a6e14-125">특정 일 위에 마우스를 가져가면 [ATP 안전한 첨부 파일](atp-safe-attachments.md) 에서 검색 된 악의적인 파일 형식 분석을 볼 수 있습니다 및 [스팸 방지 &amp; Office 365의 맬웨어 방지 보호 기능](anti-spam-and-anti-malware-protection.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-125">When you hover over a particular day, you can see the breakdown of types of malicious files that were detected by [ATP Safe Attachments](atp-safe-attachments.md) and [anti-spam &amp; anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
![하루에 대 한 데이터를 보고 하는 ATP 파일 형식](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a><span data-ttu-id="a6e14-127">ATP 메시지 처리 보고서</span><span class="sxs-lookup"><span data-stu-id="a6e14-127">ATP Message Disposition report</span></span>

<span data-ttu-id="a6e14-128">**ATP 메시지 처리** 보고서가 악의적인 콘텐츠가 있는 것으로 검색 된 전자 메일 메시지에 대 한 수행 된는 작업을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-128">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span> 
  
<span data-ttu-id="a6e14-129">보안에이 보고서를 보려면 &amp; 준수 센터, **보고서** 로 이동 \> **대시보드** \> **ATP 메시지 처리**합니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-129">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **ATP Message Disposition**.</span></span>
  
![ATP 메시지 처리 보고서](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
<span data-ttu-id="a6e14-131">다음은 차트에서 막대 위에 마우스를 가져가면 해당 날짜에 대 한 검색 된 전자 메일에 대해 어떤 작업을 수행을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-131">When you hover over a bar in the chart, you can see what actions were taken for detected email for that day.</span></span>
  
![하루에 대 한 ATP 메시지 처리 보고서 데이터](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a><span data-ttu-id="a6e14-133">추가 보고서를 보려면</span><span class="sxs-lookup"><span data-stu-id="a6e14-133">Additional reports to view</span></span>

<span data-ttu-id="a6e14-p105">이 문서에 설명 된 ATP 보고서 외에도 [전자 메일 보안 보고서](view-email-security-reports.md) 는 보안에서 사용할 수 있는 &amp; 준수 센터입니다. 전자 메일 보안 보고서에는 [위쪽 보낸사람 및 받는 사람에 게 보고서](view-email-security-reports.md#top-senders-and-recipients-report), [스푸핑 메일 보고서](view-email-security-reports.md#spoof-mail-report), [스팸 감지 보고서](view-email-security-reports.md#spam-detections-report)등의 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-p105">In addition to the ATP reports described in this article, [email security reports](view-email-security-reports.md) are available in the Security &amp; Compliance Center. Email security reports include a [Top Senders and Recipients report](view-email-security-reports.md#top-senders-and-recipients-report), a [Spoof Mail report](view-email-security-reports.md#spoof-mail-report), a [Spam Detections report](view-email-security-reports.md#spam-detections-report), and more.</span></span>
  
<span data-ttu-id="a6e14-136">및 조직에 [Office 365 위협 인텔리전스](office-365-ti.md)있으면 수도 있습니다 [보안에서 사용 하 여 탐색기 &amp; 준수 센터](use-explorer-in-security-and-compliance.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-136">And, if your organization has [Office 365 Threat Intelligence](office-365-ti.md), you can also [Use Explorer in the Security &amp; Compliance Center](use-explorer-in-security-and-compliance.md).</span></span>
  
## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="a6e14-137">이러한 보고서를 보려면 사용 권한은 필요 합니까?</span><span class="sxs-lookup"><span data-stu-id="a6e14-137">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="a6e14-138">본이 문서에서 설명 하는 전자 메일 보안 보고서를 사용 하기 위해 보안에서 할당 하는 적절 한 역할 있어야 &amp; 준수 센터 및 Exchange 관리 센터에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-138">In order to view and use the email security reports described in this article, you must have an appropriate role assigned in the Security &amp; Compliance Center and in the Exchange Admin Center.</span></span>
  
|<span data-ttu-id="a6e14-139">**Default management role assignments for this role**</span><span class="sxs-lookup"><span data-stu-id="a6e14-139">**Role group**</span></span>|<span data-ttu-id="a6e14-140">**할당 된 경우**</span><span class="sxs-lookup"><span data-stu-id="a6e14-140">**Where assigned**</span></span>|<span data-ttu-id="a6e14-141">**자세한 정보**</span><span class="sxs-lookup"><span data-stu-id="a6e14-141">**Learn more**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a6e14-142">다음 중 하나가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-142">One of the following:</span></span>  <br/>  <span data-ttu-id="a6e14-143">조직 관리</span><span class="sxs-lookup"><span data-stu-id="a6e14-143">Organization Management</span></span>  <br/>  <span data-ttu-id="a6e14-144">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="a6e14-144">Security Administrator</span></span>  <br/>  <span data-ttu-id="a6e14-145">보안 읽기 권한자</span><span class="sxs-lookup"><span data-stu-id="a6e14-145">Security Reader</span></span>  <br/> |<span data-ttu-id="a6e14-146">보안 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="a6e14-146">Security &amp; Compliance Center</span></span>  <br/> |[<span data-ttu-id="a6e14-147">Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="a6e14-147">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md) <br/> |
| <span data-ttu-id="a6e14-148">다음 중 하나가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a6e14-148">One of the following:</span></span>  <br/>  <span data-ttu-id="a6e14-149">조직 관리</span><span class="sxs-lookup"><span data-stu-id="a6e14-149">Organization Management</span></span>  <br/>  <span data-ttu-id="a6e14-150">보기 전용 조직 관리</span><span class="sxs-lookup"><span data-stu-id="a6e14-150">View-only Organization Management</span></span>  <br/>  <span data-ttu-id="a6e14-151">보기 전용 받는 사람에 게 역할</span><span class="sxs-lookup"><span data-stu-id="a6e14-151">View-Only Recipients role</span></span>  <br/>  <span data-ttu-id="a6e14-152">Compliance Management</span><span class="sxs-lookup"><span data-stu-id="a6e14-152">Compliance Management</span></span>  <br/> |<span data-ttu-id="a6e14-153">Exchange 관리 센터</span><span class="sxs-lookup"><span data-stu-id="a6e14-153">Exchange Admin Center</span></span>  <br/> |[<span data-ttu-id="a6e14-154">Exchange Online의 기능 사용 권한</span><span class="sxs-lookup"><span data-stu-id="a6e14-154">Feature permissions in Exchange Online</span></span>](https://technet.microsoft.com/library/jj200673%28v=exchg.150%29.aspx) <br/> |
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="a6e14-155">경우에 어떻게 보고서 데이터를 표시 하지?</span><span class="sxs-lookup"><span data-stu-id="a6e14-155">What if the reports aren't showing data?</span></span>

<span data-ttu-id="a6e14-p106">보고서에서 데이터를 나타나지 않는 경우 정책에 올바르게 설정 하는 다시 확인 하십시오. 조직 전체에 포함 되도록 [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md) 및 ATP 보호에 대 한 순서에 정의 된 [ATP 안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md) 있어야 합니다. 또한 [Office 365의 스팸 방지 및 맬웨어 방지 보호 기능](anti-spam-and-anti-malware-protection.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a6e14-p106">If you are not seeing data in your reports, double-check that your policies are set up correctly. Your organization must have [ATP Safe Links policies](set-up-atp-safe-links-policies.md) and [ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for ATP protection to be in place. Also see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="a6e14-159">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a6e14-159">Related topics</span></span>

[<span data-ttu-id="a6e14-160">보고서 및 Office 365 보안에 대 한 의견 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="a6e14-160">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="a6e14-161">보안에서 보고서에 대 한 일정을 만들 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="a6e14-161">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="a6e14-162">설정 및 보안에서 사용자 지정 보고서를 다운로드 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="a6e14-162">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

