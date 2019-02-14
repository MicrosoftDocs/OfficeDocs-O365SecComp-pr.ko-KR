---
title: Office 365 고급 위협 보호에 대 한 보고서 보기
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
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
ms.collection: M365-security-compliance
description: 찾기 및 보안에서 Office 365 고급 위협 보호에 대 한 보고서를 사용 하는 방법에 알아봅니다 &amp; 준수 센터입니다.
ms.openlocfilehash: a27fdf6c7d04a2526873047d4e2a33bb283878b3
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995229"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a><span data-ttu-id="93f6f-103">Office 365 고급 위협 보호에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="93f6f-103">View reports for Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="93f6f-p101">조직에 [Office 365 고급 위협 보호](office-365-atp.md) (ATP) 하는 경우 [필요한 사용 권한](#what-permissions-are-needed-to-view-these-reports)을 가진 사용자는 보안에서 여러 ATP 보고서를 사용할 수 있습니다 &amp; 준수 센터입니다. ( **보고서** 로 이동 \> **대시보드**.)</span><span class="sxs-lookup"><span data-stu-id="93f6f-p101">If your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) and you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can use several ATP reports in the Security &amp; Compliance Center. (Go to **Reports** \> **Dashboard**.)</span></span>
  
![보안&amp; 규정 준수 센터 대시보드는 Advanced Threat Protection이 작업 중인 위치를 확인할 수 있도록 도와줍니다](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="93f6f-p102">ATP 보고서 [위협 보호 상태 보고서](#threat-protection-status-report), [ATP 파일 형식 보고서](#atp-file-types-report)및 [ATP 메시지 처리 보고서](#atp-message-disposition-report)를 포함 합니다. 이 문서 ATP 보고서에 설명 하 고 [보려는 추가 보고서](#additional-reports-to-view)에 대 한 링크를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-p102">ATP reports include the [Threat Protection Status report](#threat-protection-status-report), the [ATP File Types report](#atp-file-types-report), and the [ATP Message Disposition report](#atp-message-disposition-report). This article describes the ATP reports and includes links to [additional reports to view](#additional-reports-to-view).</span></span>
  
## <a name="threat-protection-status-report"></a><span data-ttu-id="93f6f-109">위협 보호 상태 보고서</span><span class="sxs-lookup"><span data-stu-id="93f6f-109">Threat Protection Status report</span></span>

<span data-ttu-id="93f6f-p103">**위협 보호 상태** 보고서에는 함께 악의적인 콘텐츠 및 악의적인 전자 메일 감지 및 [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) 및 [Office 365 ATP](office-365-atp.md)에 의해 차단 하는 방법에 대 한 정보를 제공 하는 단일 보기입니다. 보고서에서 제공 하는 집계 된 횟수가 악의적인 콘텐츠가 포함 된 (파일 또는 웹사이트 주소 (Url)) 맬웨어 방지 엔진, [0-시간 자동 삭제 (ZAP)](zero-hour-auto-purge.md), 및 [ATP 안전한 링크](atp-safe-links.md), [ATP 안전 하 게 보호 등의 ATP 기능에 의해 차단 되는 고유한 전자 메일 메시지 첨부 파일](atp-safe-attachments.md), [ATP 피싱 방지 기능](atp-anti-phishing.md)을 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-p103">The **Threat Protection Status** report is a single view that brings together information about malicious content and malicious email detected and blocked by [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) and [Office 365 ATP](office-365-atp.md). The report provides an aggregated count of unique email messages with malicious content (files or website addresses (URLs)) blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and ATP features, such as [ATP Safe Links](atp-safe-links.md), [ATP Safe Attachments](atp-safe-attachments.md), and [ATP anti-phishing capabilities](atp-anti-phishing.md).</span></span>

> [!NOTE]
> <span data-ttu-id="93f6f-p104">위협 보호 상태 보고서는 고객에 게 [Office 365 ATP](office-365-atp.md) 또는 [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP);가 사용할 수 있는 그러나 ATP 고객에 대 한 위협 보호 상태 보고서에 표시 되는 정보 나타날 EOP 고객 보다 다양 한 데이터를 가능성이 포함 됩니다. 예, ATP 고객에 대 한 위협 보호 상태 보고서에는 [SharePoint Online, OneDrive, 또는 Microsoft 팀의 악의적인 파일을 검색](atp-for-spo-odb-and-teams.md)하는 방법에 대 한 정보가 포함 됩니다. 이러한 정보 ATP, 특정 이므로 고객은 EOP 하지만 ATP 하지는 자신의 위협 보호 상태 보고서에서 해당 정보를 표시 되지 것입니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-p104">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see. For example, the Threat Protection Status report for ATP customers will contain information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md). Such information is specific to ATP, so customers who have EOP but not ATP will not see those details in their Threat Protection Status report.</span></span>
  
<span data-ttu-id="93f6f-115">에 위협 보호 상태 보고서를 보려면는 [보안 &amp; 준수 센터](https://protection.office.com), **보고서** 로 이동 \> **대시보드** \> **위협 보호 상태**입니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-115">To view the Threat Protection Status report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![ATP 위협 보호 상태 보고서](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
<span data-ttu-id="93f6f-117">하루에 대 한 자세한 상태를 가져올, 그래프를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-117">To get detailed status for a day, hover over the graph.</span></span>
  
![하루에 대 한 ATP 위협 보호 상태 데이터](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
<span data-ttu-id="93f6f-p105">기본적으로 위협 보호 상태 보고서는 지난 7 일간에 대 한 데이터를 표시 합니다. 그러나 **필터** 를 선택 하 고 최대 90 일 동안 데이터를 보려는 날짜 범위를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-p105">By default, the Threat Protection Status report shows data for the past seven days. However, you can choose **Filters** and change the date range to view data for up to 90 days.</span></span> 
  
![ATP 위협 보호 상태 필터입니다.](media/4f703369-642b-402b-9758-b9c828283410.png)
  
<span data-ttu-id="93f6f-122">또한 보고서에 표시 되는 정보를 변경 하 **여 데이터 보기** 메뉴를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-122">You can also use the **View data by** menu to change what information is displayed in the report.</span></span> 
  
![ATP 위협 보호 상태 보고서에 대 한 표시 옵션](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a><span data-ttu-id="93f6f-124">ATP 파일 형식 보고서</span><span class="sxs-lookup"><span data-stu-id="93f6f-124">ATP File Types report</span></span>

<span data-ttu-id="93f6f-125">**ATP 파일 형식** 보고서 [ATP 안전한 첨부](atp-safe-attachments.md)하 여 악의적으로 감지 하는 파일의 종류를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-125">The **ATP File Types** report shows you the type of files detected as malicious by [ATP Safe Attachments](atp-safe-attachments.md).</span></span>
  
<span data-ttu-id="93f6f-126">이 보고서를 보려면는 [보안 &amp; 준수 센터](https://protection.office.com), **보고서** 로 이동 \> **대시보드** \> **ATP 파일 형식**입니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-126">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP File Types**.</span></span>
  
![ATP 파일 형식 보고서](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
<span data-ttu-id="93f6f-128">특정 일 위에 마우스를 가져가면 [ATP 안전한 첨부 파일](atp-safe-attachments.md) 에서 검색 된 악의적인 파일 형식 분석을 볼 수 있습니다 및 [스팸 방지 &amp; Office 365의 맬웨어 방지 보호 기능](anti-spam-and-anti-malware-protection.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-128">When you hover over a particular day, you can see the breakdown of types of malicious files that were detected by [ATP Safe Attachments](atp-safe-attachments.md) and [anti-spam &amp; anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
![하루에 대 한 데이터를 보고 하는 ATP 파일 형식](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a><span data-ttu-id="93f6f-130">ATP 메시지 처리 보고서</span><span class="sxs-lookup"><span data-stu-id="93f6f-130">ATP Message Disposition report</span></span>

<span data-ttu-id="93f6f-131">**ATP 메시지 처리** 보고서가 악의적인 콘텐츠가 있는 것으로 검색 된 전자 메일 메시지에 대 한 수행 된는 작업을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-131">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span> 
  
<span data-ttu-id="93f6f-132">이 보고서를 보려면는 [보안 &amp; 준수 센터](https://protection.office.com), **보고서** 로 이동 \> **대시보드** \> **ATP 메시지 처리**합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-132">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP Message Disposition**.</span></span>
  
![ATP 메시지 처리 보고서](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
<span data-ttu-id="93f6f-134">다음은 차트에서 막대 위에 마우스를 가져가면 해당 날짜에 대 한 검색 된 전자 메일에 대해 어떤 작업을 수행을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-134">When you hover over a bar in the chart, you can see what actions were taken for detected email for that day.</span></span>
  
![하루에 대 한 ATP 메시지 처리 보고서 데이터](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a><span data-ttu-id="93f6f-136">추가 보고서를 보려면</span><span class="sxs-lookup"><span data-stu-id="93f6f-136">Additional reports to view</span></span>

<span data-ttu-id="93f6f-137">다음 표에 설명 된 대로이 문서에 설명 된 ATP 보고서 외에도 다른 여러 보고서를를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-137">In addition to the ATP reports described in this article, several other reports are available, as described in the following table:</span></span>

|<span data-ttu-id="93f6f-138">보고서 유형</span><span class="sxs-lookup"><span data-stu-id="93f6f-138">Report type</span></span>  |<span data-ttu-id="93f6f-139">자세한 정보</span><span class="sxs-lookup"><span data-stu-id="93f6f-139">Learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="93f6f-140">**전자 메일 보안 보고서**와 같은, 위쪽 보낸사람 및 받는 사람에 게 보고서, 스푸핑 메일 보고서 및 스팸이 감지 된 보고서입니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-140">**Email security reports**, such as a Top Senders and Recipients report, a Spoof Mail report, and a Spam Detections report.</span></span> | [<span data-ttu-id="93f6f-141">보안에서 전자 메일 보안 보고서를 보려면 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="93f6f-141">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)        |
|<span data-ttu-id="93f6f-142">**탐색기** (위협 탐색기 라고도 함,이에 포함 된 [Office 365 위협 인텔리전스](office-365-ti.md))</span><span class="sxs-lookup"><span data-stu-id="93f6f-142">**Explorer** (also referred to as Threat Explorer, this is included in [Office 365 Threat Intelligence](office-365-ti.md))</span></span>     | [<span data-ttu-id="93f6f-143">탐색기를 사용 하 여 보안에서 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="93f6f-143">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)        |
|<span data-ttu-id="93f6f-p106">**EOP 및 ATP 결과** (PowerShell을 사용 하 여 생성 하는 사용자 지정 보고서 임). 이 보고서에는 도메인, 날짜, 이벤트 유형, 방향, 동작 및 메시지 수와 같은 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-p106">**EOP and ATP results** (This is a custom report you generate by using PowerShell). This report contains information, such as Domain, Date, Event Type, Direction, Action, and Message Count.</span></span>  | [<span data-ttu-id="93f6f-146">Get MailTrafficATPReport cmdlet 참조 (영문)</span><span class="sxs-lookup"><span data-stu-id="93f6f-146">Get-MailTrafficATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|<span data-ttu-id="93f6f-p107">**EOP 및 ATP 감지** (PowerShell을 사용 하 여 생성 하는 사용자 지정 보고서 임). 이 보고서는 악의적인 파일 또는 Url, 피싱 시도, 가장, 및 전자 메일 또는 파일에 대 한 기타 잠재적 위협에 대 한 세부 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-p107">**EOP and ATP detections** (This is a custom report you generate by using PowerShell). This report contains details about malicious files or URLs, phishing attempts, impersonation, and other potential threats in email or files.</span></span>   | [<span data-ttu-id="93f6f-149">Get MailDetailATPReport cmdlet 참조 (영문)</span><span class="sxs-lookup"><span data-stu-id="93f6f-149">Get-MailDetailATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a><span data-ttu-id="93f6f-150">사용 권한은 ATP 보고서를 보려면 필요 합니까?</span><span class="sxs-lookup"><span data-stu-id="93f6f-150">What permissions are needed to view the ATP reports?</span></span>

<span data-ttu-id="93f6f-151">이 문서에 설명 된 보고서 보기 및 사용 하기 위해 **모두 보안을 위해 할당 되는 적절 한 역할을 해야 &amp; 준수 센터 및 Exchange 관리 센터**합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-151">In order to view and use the reports described in this article, **you must have an appropriate role assigned for both the Security &amp; Compliance Center and the Exchange Admin Center**.</span></span>

- <span data-ttu-id="93f6f-152">보안을 위해 &amp; 준수 센터 있어야 할당 된 다음 역할 중 하나:</span><span class="sxs-lookup"><span data-stu-id="93f6f-152">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="93f6f-153">조직 관리</span><span class="sxs-lookup"><span data-stu-id="93f6f-153">Organization Management</span></span>
    - <span data-ttu-id="93f6f-154">보안 관리자 (Azure Active Directory 관리 센터에서이 할당할 수 있습니다 ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span><span class="sxs-lookup"><span data-stu-id="93f6f-154">Security Administrator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>
    - <span data-ttu-id="93f6f-155">보안 읽기 권한자</span><span class="sxs-lookup"><span data-stu-id="93f6f-155">Security Reader</span></span>

- <span data-ttu-id="93f6f-156">Exchange Online에 대 한 있어야 Exchange 관리 센터에 할당 된 다음 역할 중 하나 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) 또는 PowerShell cmdlet (참조 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-156">For Exchange Online, you must have one of the following roles assigned in either the Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) or with PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span></span>
    - <span data-ttu-id="93f6f-157">조직 관리</span><span class="sxs-lookup"><span data-stu-id="93f6f-157">Organization Management</span></span>
    - <span data-ttu-id="93f6f-158">보기 전용 조직 관리</span><span class="sxs-lookup"><span data-stu-id="93f6f-158">View-only Organization Management</span></span>
    - <span data-ttu-id="93f6f-159">보기 권한만 있는 받는 사람 역할</span><span class="sxs-lookup"><span data-stu-id="93f6f-159">View-Only Recipients role</span></span>
    - <span data-ttu-id="93f6f-160">준수 관리</span><span class="sxs-lookup"><span data-stu-id="93f6f-160">Compliance Management</span></span>

<span data-ttu-id="93f6f-161">자세한 내용은 다음 리소스를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6f-161">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="93f6f-162">Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="93f6f-162">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="93f6f-163">Exchange Online의 기능 사용 권한</span><span class="sxs-lookup"><span data-stu-id="93f6f-163">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="93f6f-164">경우에 어떻게 보고서 데이터를 표시 하지?</span><span class="sxs-lookup"><span data-stu-id="93f6f-164">What if the reports aren't showing data?</span></span>

<span data-ttu-id="93f6f-p108">ATP 보고서의 데이터를 나타나지 않는 경우 정책에 올바르게 설정 하는 다시 확인 하십시오. 조직 전체에 포함 되도록 [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md) 및 ATP 보호에 대 한 순서에 정의 된 [ATP 안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md) 있어야 합니다. 또한 [Office 365의 스팸 방지 및 맬웨어 방지 보호 기능](anti-spam-and-anti-malware-protection.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="93f6f-p108">If you are not seeing data in your ATP reports, double-check that your policies are set up correctly. Your organization must have [ATP Safe Links policies](set-up-atp-safe-links-policies.md) and [ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for ATP protection to be in place. Also see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="93f6f-168">관련 항목</span><span class="sxs-lookup"><span data-stu-id="93f6f-168">Related topics</span></span>

[<span data-ttu-id="93f6f-169">보고서 및 Office 365 보안에 대 한 의견 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="93f6f-169">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="93f6f-170">보안에서 보고서에 대 한 일정을 만들 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="93f6f-170">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="93f6f-171">설정 및 보안에서 사용자 지정 보고서를 다운로드 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="93f6f-171">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

