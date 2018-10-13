---
title: Office 365 고급 위협 보호에 대 한 보고서 보기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
description: 찾기 및 보안에서 Office 365 고급 위협 보호에 대 한 보고서를 사용 하는 방법에 알아봅니다 &amp; 준수 센터입니다.
ms.openlocfilehash: 1a0ecb9a6722deb50a491a15f720481a5bb7b0a4
ms.sourcegitcommit: e0c6f99d5514d8da8a70d9bd3616d1a1c0851254
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2018
ms.locfileid: "25552336"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a><span data-ttu-id="ef2ea-103">Office 365 고급 위협 보호에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="ef2ea-103">View reports for Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="ef2ea-p101">조직에 [Office 365 고급 위협 보호](office-365-atp.md) (ATP) 하는 경우 [필요한 사용 권한](#what-permissions-are-needed-to-view-these-reports)을 가진 사용자는 보안에서 여러 ATP 보고서를 사용할 수 있습니다 &amp; 준수 센터입니다. ( **보고서** 로 이동 \> **대시보드**.)</span><span class="sxs-lookup"><span data-stu-id="ef2ea-p101">If your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) and you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can use several ATP reports in the Security &amp; Compliance Center. (Go to **Reports** \> **Dashboard**.)</span></span>
  
![보안 &amp; 준수 센터 대시보드 도울수 위협 보호 고급가 작동 하는 위치를 참조 하십시오.](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="ef2ea-p102">ATP 보고서 [위협 보호 상태 보고서](#threat-protection-status-report), [ATP 파일 형식 보고서](#atp-file-types-report)및 [ATP 메시지 처리 보고서](#atp-message-disposition-report)를 포함 합니다. 이 문서 ATP 보고서에 설명 하 고 [보려는 추가 보고서](#additional-reports-to-view)에 대 한 링크를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-p102">ATP reports include the [Threat Protection Status report](#threat-protection-status-report), the [ATP File Types report](#atp-file-types-report), and the [ATP Message Disposition report](#atp-message-disposition-report). This article describes the ATP reports and includes links to [additional reports to view](#additional-reports-to-view).</span></span>
  
## <a name="threat-protection-status-report"></a><span data-ttu-id="ef2ea-109">위협 보호 상태 보고서</span><span class="sxs-lookup"><span data-stu-id="ef2ea-109">Threat Protection Status report</span></span>

<span data-ttu-id="ef2ea-p103">**위협 보호 상태** 보고서에는 함께 악의적인 콘텐츠 및 악의적인 전자 메일 감지 및 [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) 및 [Office 365 ATP](office-365-atp.md)에 의해 차단 하는 방법에 대 한 정보를 제공 하는 단일 보기입니다. 보고서에서 제공 하는 집계 된 횟수가 악의적인 콘텐츠가 포함 된 (파일 또는 웹사이트 주소 (Url)) 맬웨어 방지 엔진, [0-시간 자동 삭제 (ZAP)](zero-hour-auto-purge.md), 및 [ATP 안전한 링크](atp-safe-links.md), [ATP 안전 하 게 보호 등의 ATP 기능에 의해 차단 되는 고유한 전자 메일 메시지 첨부 파일](atp-safe-attachments.md), [ATP 피싱 방지 기능](atp-anti-phishing.md)을 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-p103">The **Threat Protection Status** report is a single view that brings together information about malicious content and malicious email detected and blocked by [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) and [Office 365 ATP](office-365-atp.md). The report provides an aggregated count of unique email messages with malicious content (files or website addresses (URLs)) blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and ATP features, such as [ATP Safe Links](atp-safe-links.md), [ATP Safe Attachments](atp-safe-attachments.md), and [ATP anti-phishing capabilities](atp-anti-phishing.md).</span></span>

> [!NOTE]
> <span data-ttu-id="ef2ea-p104">위협 보호 상태 보고서는 고객에 게 [Office 365 ATP](office-365-atp.md) 또는 [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP);가 사용할 수 있는 그러나 ATP 고객에 대 한 위협 보호 상태 보고서에 표시 되는 정보 나타날 EOP 고객 보다 다양 한 데이터를 가능성이 포함 됩니다. 예, ATP 고객에 대 한 위협 보호 상태 보고서에는 [SharePoint Online, OneDrive, 또는 Microsoft 팀의 악의적인 파일을 검색](atp-for-spo-odb-and-teams.md)하는 방법에 대 한 정보가 포함 됩니다. 이러한 정보 ATP, 특정 이므로 고객은 EOP 하지만 ATP 하지는 자신의 위협 보호 상태 보고서에서 해당 정보를 표시 되지 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-p104">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see. For example, the Threat Protection Status report for ATP customers will contain information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md). Such information is specific to ATP, so customers who have EOP but not ATP will not see those details in their Threat Protection Status report.</span></span>
  
<span data-ttu-id="ef2ea-115">보안에 위협 보호 상태 보고서를 보려면 &amp; 준수 센터, **보고서** 로 이동 \> **대시보드** \> **위협 보호 상태**입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-115">To view the Threat Protection Status report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![ATP 위협 보호 상태 보고서](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
<span data-ttu-id="ef2ea-117">하루에 대 한 자세한 상태를 가져올, 그래프를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-117">To get detailed status for a day, hover over the graph.</span></span>
  
![하루에 대 한 ATP 위협 보호 상태 데이터](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
<span data-ttu-id="ef2ea-p105">기본적으로 위협 보호 상태 보고서는 지난 7 일간에 대 한 데이터를 표시 합니다. 그러나 **필터** 를 선택 하 고 최대 90 일 동안 데이터를 보려는 날짜 범위를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-p105">By default, the Threat Protection Status report shows data for the past seven days. However, you can choose **Filters** and change the date range to view data for up to 90 days.</span></span> 
  
![ATP 위협 보호 상태 필터입니다.](media/4f703369-642b-402b-9758-b9c828283410.png)
  
<span data-ttu-id="ef2ea-122">또한 보고서에 표시 되는 정보를 변경 하 **여 데이터 보기** 메뉴를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-122">You can also use the **View data by** menu to change what information is displayed in the report.</span></span> 
  
![ATP 위협 보호 상태 보고서에 대 한 표시 옵션](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a><span data-ttu-id="ef2ea-124">ATP 파일 형식 보고서</span><span class="sxs-lookup"><span data-stu-id="ef2ea-124">ATP File Types report</span></span>

<span data-ttu-id="ef2ea-125">**ATP 파일 형식** 보고서 [ATP 안전한 첨부](atp-safe-attachments.md)하 여 악의적으로 감지 하는 파일의 종류를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-125">The **ATP File Types** report shows you the type of files detected as malicious by [ATP Safe Attachments](atp-safe-attachments.md).</span></span>
  
<span data-ttu-id="ef2ea-126">보안에이 보고서를 보려면 &amp; 준수 센터, **보고서** 로 이동 \> **대시보드** \> **ATP 파일 형식**입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-126">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **ATP File Types**.</span></span>
  
![ATP 파일 형식 보고서](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
<span data-ttu-id="ef2ea-128">특정 일 위에 마우스를 가져가면 [ATP 안전한 첨부 파일](atp-safe-attachments.md) 에서 검색 된 악의적인 파일 형식 분석을 볼 수 있습니다 및 [스팸 방지 &amp; Office 365의 맬웨어 방지 보호 기능](anti-spam-and-anti-malware-protection.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-128">When you hover over a particular day, you can see the breakdown of types of malicious files that were detected by [ATP Safe Attachments](atp-safe-attachments.md) and [anti-spam &amp; anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
![하루에 대 한 데이터를 보고 하는 ATP 파일 형식](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a><span data-ttu-id="ef2ea-130">ATP 메시지 처리 보고서</span><span class="sxs-lookup"><span data-stu-id="ef2ea-130">ATP Message Disposition report</span></span>

<span data-ttu-id="ef2ea-131">**ATP 메시지 처리** 보고서가 악의적인 콘텐츠가 있는 것으로 검색 된 전자 메일 메시지에 대 한 수행 된는 작업을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-131">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span> 
  
<span data-ttu-id="ef2ea-132">보안에이 보고서를 보려면 &amp; 준수 센터, **보고서** 로 이동 \> **대시보드** \> **ATP 메시지 처리**합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-132">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **ATP Message Disposition**.</span></span>
  
![ATP 메시지 처리 보고서](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
<span data-ttu-id="ef2ea-134">다음은 차트에서 막대 위에 마우스를 가져가면 해당 날짜에 대 한 검색 된 전자 메일에 대해 어떤 작업을 수행을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-134">When you hover over a bar in the chart, you can see what actions were taken for detected email for that day.</span></span>
  
![하루에 대 한 ATP 메시지 처리 보고서 데이터](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a><span data-ttu-id="ef2ea-136">추가 보고서를 보려면</span><span class="sxs-lookup"><span data-stu-id="ef2ea-136">Additional reports to view</span></span>

<span data-ttu-id="ef2ea-137">다음 표에 설명 된 대로이 문서에 설명 된 ATP 보고서 외에도 다른 여러 보고서를를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-137">In addition to the ATP reports described in this article, several other reports are available, as described in the following table:</span></span>


|<span data-ttu-id="ef2ea-138">보고서 유형</span><span class="sxs-lookup"><span data-stu-id="ef2ea-138">Report type</span></span>  |<span data-ttu-id="ef2ea-139">자세한 정보</span><span class="sxs-lookup"><span data-stu-id="ef2ea-139">Learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="ef2ea-140">**전자 메일 보안 보고서**와 같은, 위쪽 보낸사람 및 받는 사람에 게 보고서, 스푸핑 메일 보고서 및 스팸이 감지 된 보고서입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-140">**Email security reports**, such as a Top Senders and Recipients report, a Spoof Mail report, and a Spam Detections report.</span></span> | [<span data-ttu-id="ef2ea-141">보안에서 전자 메일 보안 보고서를 보려면 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="ef2ea-141">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)        |
|<span data-ttu-id="ef2ea-142">**탐색기** (위협 탐색기 라고도 함,이에 포함 된 [Office 365 위협 인텔리전스](office-365-ti.md))</span><span class="sxs-lookup"><span data-stu-id="ef2ea-142">**Explorer** (also referred to as Threat Explorer, this is included in [Office 365 Threat Intelligence](office-365-ti.md))</span></span>     | [<span data-ttu-id="ef2ea-143">탐색기를 사용 하 여 보안에서 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="ef2ea-143">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)        |
|<span data-ttu-id="ef2ea-p106">**EOP 및 ATP 결과** (PowerShell을 사용 하 여 생성 하는 사용자 지정 보고서 임). 이 보고서에는 도메인, 날짜, 이벤트 유형, 방향, 동작 및 메시지 수와 같은 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-p106">**EOP and ATP results** (This is a custom report you generate by using PowerShell). This report contains information, such as Domain, Date, Event Type, Direction, Action, and Message Count.</span></span>  | [<span data-ttu-id="ef2ea-146">Get MailTrafficATPReport cmdlet 참조 (영문)</span><span class="sxs-lookup"><span data-stu-id="ef2ea-146">Get-MailTrafficATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|<span data-ttu-id="ef2ea-p107">**EOP 및 ATP 감지** (PowerShell을 사용 하 여 생성 하는 사용자 지정 보고서 임). 이 보고서는 악의적인 파일 또는 Url, 피싱 시도, 가장, 및 전자 메일 또는 파일에 대 한 기타 잠재적 위협에 대 한 세부 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-p107">**EOP and ATP detections** (This is a custom report you generate by using PowerShell). This report contains details about malicious files or URLs, phishing attempts, impersonation, and other potential threats in email or files.</span></span>   | [<span data-ttu-id="ef2ea-149">Get MailDetailATPReport cmdlet 참조 (영문)</span><span class="sxs-lookup"><span data-stu-id="ef2ea-149">Get-MailDetailATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a><span data-ttu-id="ef2ea-150">사용 권한은 ATP 보고서를 보려면 필요 합니까?</span><span class="sxs-lookup"><span data-stu-id="ef2ea-150">What permissions are needed to view the ATP reports?</span></span>

<span data-ttu-id="ef2ea-151">본이 문서에서 설명 하는 보고서를 사용 하기 위해 보안에서 할당 하는 적절 한 역할 있어야 &amp; 준수 센터 및 Exchange 관리 센터에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-151">In order to view and use the reports described in this article, you must have an appropriate role assigned in the Security &amp; Compliance Center and in the Exchange Admin Center.</span></span>
  
|<span data-ttu-id="ef2ea-152">**Default management role assignments for this role**</span><span class="sxs-lookup"><span data-stu-id="ef2ea-152">**Role group**</span></span>|<span data-ttu-id="ef2ea-153">**할당 된 경우**</span><span class="sxs-lookup"><span data-stu-id="ef2ea-153">**Where assigned**</span></span>|<span data-ttu-id="ef2ea-154">**자세한 정보**</span><span class="sxs-lookup"><span data-stu-id="ef2ea-154">**Learn more**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ef2ea-155">다음 중 하나가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-155">One of the following:</span></span>  <br/><br/><span data-ttu-id="ef2ea-156">-조직 관리</span><span class="sxs-lookup"><span data-stu-id="ef2ea-156">--Organization Management</span></span>  <br/><span data-ttu-id="ef2ea-157">--보안 관리자</span><span class="sxs-lookup"><span data-stu-id="ef2ea-157">--Security Administrator</span></span>  <br/><span data-ttu-id="ef2ea-158">--보안 읽기 권한자</span><span class="sxs-lookup"><span data-stu-id="ef2ea-158">--Security Reader</span></span>  <br/> |<span data-ttu-id="ef2ea-159">보안 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="ef2ea-159">Security &amp; Compliance Center</span></span>  <br/> |[<span data-ttu-id="ef2ea-160">Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="ef2ea-160">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md) <br/> |
| <span data-ttu-id="ef2ea-161">다음 중 하나가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-161">One of the following:</span></span>  <br/><br/><span data-ttu-id="ef2ea-162">-조직 관리</span><span class="sxs-lookup"><span data-stu-id="ef2ea-162">--Organization Management</span></span>  <br/><span data-ttu-id="ef2ea-163">-보기 전용 조직 관리</span><span class="sxs-lookup"><span data-stu-id="ef2ea-163">--View-only Organization Management</span></span>  <br/><span data-ttu-id="ef2ea-164">-역할인 받는 사람에 게 역할</span><span class="sxs-lookup"><span data-stu-id="ef2ea-164">--View-Only Recipients role</span></span>  <br/><span data-ttu-id="ef2ea-165">-규정 준수 관리</span><span class="sxs-lookup"><span data-stu-id="ef2ea-165">--Compliance Management</span></span>  <br/> |<span data-ttu-id="ef2ea-166">Exchange 관리 센터</span><span class="sxs-lookup"><span data-stu-id="ef2ea-166">Exchange Admin Center</span></span>  <br/> |[<span data-ttu-id="ef2ea-167">Exchange Online의 기능 사용 권한</span><span class="sxs-lookup"><span data-stu-id="ef2ea-167">Feature permissions in Exchange Online</span></span>](https://technet.microsoft.com/library/jj200673%28v=exchg.150%29.aspx) <br/> |
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="ef2ea-168">경우에 어떻게 보고서 데이터를 표시 하지?</span><span class="sxs-lookup"><span data-stu-id="ef2ea-168">What if the reports aren't showing data?</span></span>

<span data-ttu-id="ef2ea-p108">ATP 보고서의 데이터를 나타나지 않는 경우 정책에 올바르게 설정 하는 다시 확인 하십시오. 조직 전체에 포함 되도록 [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md) 및 ATP 보호에 대 한 순서에 정의 된 [ATP 안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md) 있어야 합니다. 또한 [Office 365의 스팸 방지 및 맬웨어 방지 보호 기능](anti-spam-and-anti-malware-protection.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ef2ea-p108">If you are not seeing data in your ATP reports, double-check that your policies are set up correctly. Your organization must have [ATP Safe Links policies](set-up-atp-safe-links-policies.md) and [ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for ATP protection to be in place. Also see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="ef2ea-172">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ef2ea-172">Related topics</span></span>

[<span data-ttu-id="ef2ea-173">보고서 및 Office 365 보안에 대 한 의견 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="ef2ea-173">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="ef2ea-174">보안에서 보고서에 대 한 일정을 만들 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="ef2ea-174">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="ef2ea-175">설정 및 보안에서 사용자 지정 보고서를 다운로드 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="ef2ea-175">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

