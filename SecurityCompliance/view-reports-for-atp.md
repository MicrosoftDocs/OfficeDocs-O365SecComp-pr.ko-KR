---
title: Office 365 Advanced Threat Protection에 대 한 보고서 보기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 04/01/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
ms.collection:
- M365-security-compliance
description: 보안 &amp; 및 준수 센터에서 Office 365 Advanced Threat Protection에 대 한 보고서를 찾아서 사용 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: ff80191ae75a37994d1ad08f587fa07f72b88f24
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32267556"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a><span data-ttu-id="477bd-103">Office 365 Advanced Threat Protection에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="477bd-103">View reports for Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="477bd-104">조직에 [Office 365 ATP (Advanced Threat Protection](office-365-atp.md) )가 있고 [필요한 사용 권한이](#what-permissions-are-needed-to-view-the-atp-reports)있는 경우 보안 &amp; 및 준수 센터에서 여러 ATP 보고서를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-104">If your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) and you have the [necessary permissions](#what-permissions-are-needed-to-view-the-atp-reports), you can use several ATP reports in the Security &amp; Compliance Center.</span></span> <span data-ttu-id="477bd-105">( **보고서** \> **대시보드로**이동 합니다.)</span><span class="sxs-lookup"><span data-stu-id="477bd-105">(Go to **Reports** \> **Dashboard**.)</span></span>
  
![보안&amp; 규정 준수 센터 대시보드는 Advanced Threat Protection이 작업 중인 위치를 확인할 수 있도록 도와줍니다](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="477bd-107">atp 보고서에는 [위협 보호 상태 보고서](#threat-protection-status-report), [atp 파일 형식 보고서](#atp-file-types-report)및 [ATP 메시지 처리 보고서](#atp-message-disposition-report)가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-107">ATP reports include the [Threat Protection Status report](#threat-protection-status-report), the [ATP File Types report](#atp-file-types-report), and the [ATP Message Disposition report](#atp-message-disposition-report).</span></span> <span data-ttu-id="477bd-108">이 문서에서는 ATP 보고서에 대해 설명 하 고 [확인할 추가 보고서](#additional-reports-to-view)에 대 한 링크를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-108">This article describes the ATP reports and includes links to [additional reports to view](#additional-reports-to-view).</span></span>
  
## <a name="threat-protection-status-report"></a><span data-ttu-id="477bd-109">위협 방지 상태 보고서</span><span class="sxs-lookup"><span data-stu-id="477bd-109">Threat Protection Status report</span></span>

<span data-ttu-id="477bd-110">**위협 방지 상태** 보고서는 EOP ( [Exchange Online Protection](eop/exchange-online-protection-overview.md) ) 및 [Office 365 ATP](office-365-atp.md)에 의해 감지 되어 차단 된 악의적인 콘텐츠와 악성 전자 메일에 대 한 정보를 함께 가져오는 단일 보기입니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-110">The **Threat Protection Status** report is a single view that brings together information about malicious content and malicious email detected and blocked by [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) and [Office 365 ATP](office-365-atp.md).</span></span> <span data-ttu-id="477bd-111">이 보고서는 맬웨어 방지 엔진, [0 시간 자동 제거 (ZAP)](zero-hour-auto-purge.md)및 atp (전송 안전한 [링크](atp-safe-links.md), [atp 안전)에 의해 차단 되는 악의적인 콘텐츠 (파일 또는 웹 사이트 주소 (url))의 집계 된 고유 전자 메일 메시지 수를 제공 합니다. 첨부 파일](atp-safe-attachments.md)및 [ATP 피싱 방지 기능](atp-anti-phishing.md)</span><span class="sxs-lookup"><span data-stu-id="477bd-111">The report provides an aggregated count of unique email messages with malicious content (files or website addresses (URLs)) blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and ATP features, such as [ATP Safe Links](atp-safe-links.md), [ATP Safe Attachments](atp-safe-attachments.md), and [ATP anti-phishing capabilities](atp-anti-phishing.md).</span></span>

> [!NOTE]
> <span data-ttu-id="477bd-112">[Office 365 ATP](office-365-atp.md) 또는 [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP)이 있는 고객은 위협 보호 상태 보고서를 사용할 수 있습니다. 그러나 ATP 고객에 대 한 위협 방지 상태 보고서에 표시 되는 정보에는 고객에 게 표시 될 수 있는 것과 다른 데이터가 포함 될 가능성이 EOP.</span><span class="sxs-lookup"><span data-stu-id="477bd-112">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see.</span></span> <span data-ttu-id="477bd-113">예를 들어 ATP 고객에 대 한 위협 방지 상태 보고서에는 [SharePoint Online, OneDrive 또는 Microsoft 팀에서 검색 된 악성 파일](atp-for-spo-odb-and-teams.md)에 대 한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-113">For example, the Threat Protection Status report for ATP customers will contain information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md).</span></span> <span data-ttu-id="477bd-114">이러한 정보는 atp와 관련 된 것 이므로, EOP가 아닌 고객은 위협 보호 상태 보고서에 해당 세부 정보를 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-114">Such information is specific to ATP, so customers who have EOP but not ATP will not see those details in their Threat Protection Status report.</span></span>
  
<span data-ttu-id="477bd-115">위협 방지 상태 보고서를 보려면 [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드** \> **위협 보호 상태로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-115">To view the Threat Protection Status report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![ATP 위협 방지 상태 보고서](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
<span data-ttu-id="477bd-117">하루 동안 자세한 상태를 보려면 그래프를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-117">To get detailed status for a day, hover over the graph.</span></span>
  
![ATP 위협 방지 상태 데이터 (일)](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
<span data-ttu-id="477bd-119">기본적으로 위협 방지 상태 보고서에는 최근 7 일간의 데이터가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-119">By default, the Threat Protection Status report shows data for the past seven days.</span></span> <span data-ttu-id="477bd-120">그러나 **필터** 를 선택 하 고 날짜 범위를 변경 하 여 데이터를 최대 90 일까 지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-120">However, you can choose **Filters** and change the date range to view data for up to 90 days.</span></span> 
  
![ATP 위협 방지 상태 필터](media/4f703369-642b-402b-9758-b9c828283410.png)
  
<span data-ttu-id="477bd-122">**데이터 보기 기준** 메뉴를 사용 하 여 보고서에 표시 되는 정보를 변경할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-122">You can also use the **View data by** menu to change what information is displayed in the report.</span></span> 
  
![ATP 위협 방지 상태 보고서에 대 한 옵션 보기](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a><span data-ttu-id="477bd-124">ATP 파일 형식 보고서</span><span class="sxs-lookup"><span data-stu-id="477bd-124">ATP File Types report</span></span>

<span data-ttu-id="477bd-125">**atp 파일 형식** 보고서에는 [atp 안전한 첨부 파일](atp-safe-attachments.md)에 의해 악의적으로 검색 된 파일 유형이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-125">The **ATP File Types** report shows you the type of files detected as malicious by [ATP Safe Attachments](atp-safe-attachments.md).</span></span>
  
<span data-ttu-id="477bd-126">이 보고서를 보려면 [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드** \> **ATP 파일 형식**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-126">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP File Types**.</span></span>
  
![ATP 파일 형식 보고서](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
<span data-ttu-id="477bd-128">특정 날짜를 마우스로 가리키면 [ATP 수신 허용 첨부 파일](atp-safe-attachments.md) 및 [Office 365의 스팸 &amp; 방지 바이러스 백신 보호 기능](anti-spam-and-anti-malware-protection.md)에서 검색 된 악의적인 파일의 유형을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-128">When you hover over a particular day, you can see the breakdown of types of malicious files that were detected by [ATP Safe Attachments](atp-safe-attachments.md) and [anti-spam &amp; anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
![ATP 파일 형식 하루에 대 한 보고서 데이터](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a><span data-ttu-id="477bd-130">ATP 메시지 처리 보고서</span><span class="sxs-lookup"><span data-stu-id="477bd-130">ATP Message Disposition report</span></span>

<span data-ttu-id="477bd-131">**ATP 메시지 처리** 보고서에는 악성 콘텐츠가 있는 것으로 검색 된 전자 메일 메시지에 대해 수행 된 작업이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-131">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span> 
  
<span data-ttu-id="477bd-132">이 보고서를 보려면 [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드** \> **ATP 메시지 처리**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-132">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP Message Disposition**.</span></span>
  
![ATP 메시지 처리 보고서](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
<span data-ttu-id="477bd-134">차트의 막대 위에 마우스를 올리면 해당 요일의 검색 된 전자 메일에 대해 수행한 작업을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-134">When you hover over a bar in the chart, you can see what actions were taken for detected email for that day.</span></span>
  
![ATP 메시지 처리 보고서 데이터 (일)](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a><span data-ttu-id="477bd-136">볼 수 있는 추가 보고서</span><span class="sxs-lookup"><span data-stu-id="477bd-136">Additional reports to view</span></span>

<span data-ttu-id="477bd-137">이 문서에서 설명 하는 ATP 보고서 외에도 다음 표에 설명 된 것 처럼 다른 몇 가지 보고서를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-137">In addition to the ATP reports described in this article, several other reports are available, as described in the following table:</span></span>

|<span data-ttu-id="477bd-138">보고서</span><span class="sxs-lookup"><span data-stu-id="477bd-138">Report(s)</span></span>  |<span data-ttu-id="477bd-139">세부 정보</span><span class="sxs-lookup"><span data-stu-id="477bd-139">Details</span></span>  |
|---------|---------|
|<span data-ttu-id="477bd-140">**ATP 안전한 링크 URL 추적** (PowerShell을 사용 하 여 생성 하는 보고서입니다.) 이 보고서는 지난 7 일 동안 ATP 안전한 링크 작업의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-140">**ATP Safe Links URL trace** (This is a report you generate by using PowerShell.) This report shows the results of ATP Safe Links actions over the past seven (7) days.</span></span> |[<span data-ttu-id="477bd-141">Get-urltrace cmdlet 참조</span><span class="sxs-lookup"><span data-stu-id="477bd-141">Get-UrlTrace cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-urltrace?view=exchange-ps) |
|<span data-ttu-id="477bd-142">상위 보낸 사람 및 받는 사람 보고서, 스푸핑 메일 보고서, 스팸 감지 보고서 등의 **전자 메일 보안 보고서**</span><span class="sxs-lookup"><span data-stu-id="477bd-142">**Email security reports**, such as a Top Senders and Recipients report, a Spoof Mail report, and a Spam Detections report.</span></span> | [<span data-ttu-id="477bd-143">보안 &amp; 및 준수 센터의 전자 메일 보안 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="477bd-143">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)        |
|<span data-ttu-id="477bd-144">**탐색기** (위협 탐색기 라고도 하며,이는 [Office 365 Advanced Threat Protection 계획 2](office-365-ti.md)에 포함 되어 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="477bd-144">**Explorer** (also referred to as Threat Explorer, this is included in [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md))</span></span>     | [<span data-ttu-id="477bd-145">보안 &amp; 및 준수 센터에서 탐색기 사용</span><span class="sxs-lookup"><span data-stu-id="477bd-145">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)        |
|<span data-ttu-id="477bd-146">**EOP 및 ATP 결과** (PowerShell을 사용 하 여 생성 하는 사용자 지정 보고서입니다.)</span><span class="sxs-lookup"><span data-stu-id="477bd-146">**EOP and ATP results** (This is a custom report you generate by using PowerShell).</span></span> <span data-ttu-id="477bd-147">이 보고서에는 도메인, 날짜, 이벤트 유형, 방향, 동작 및 메시지 수와 같은 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-147">This report contains information, such as Domain, Date, Event Type, Direction, Action, and Message Count.</span></span>  | [<span data-ttu-id="477bd-148">MailTrafficATPReport cmdlet 참조</span><span class="sxs-lookup"><span data-stu-id="477bd-148">Get-MailTrafficATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|<span data-ttu-id="477bd-149">**EOP 및 ATP** 검색 (PowerShell을 사용 하 여 생성 하는 사용자 지정 보고서입니다.)</span><span class="sxs-lookup"><span data-stu-id="477bd-149">**EOP and ATP detections** (This is a custom report you generate by using PowerShell).</span></span> <span data-ttu-id="477bd-150">이 보고서에는 악성 파일 또는 url, 피싱 시도, 가장 및 기타 잠재적 위협 (전자 메일 또는 파일)에 대 한 자세한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-150">This report contains details about malicious files or URLs, phishing attempts, impersonation, and other potential threats in email or files.</span></span>   | [<span data-ttu-id="477bd-151">MailDetailATPReport cmdlet 참조</span><span class="sxs-lookup"><span data-stu-id="477bd-151">Get-MailDetailATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a><span data-ttu-id="477bd-152">ATP 보고서를 표시 하는 데 필요한 사용 권한은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="477bd-152">What permissions are needed to view the ATP reports?</span></span>

<span data-ttu-id="477bd-153">이 문서에서 설명 하는 보고서를 보고 사용 하려면 **보안 &amp; 및 준수 센터와 Exchange 관리 센터 둘 다에 대해 적절 한 역할이 할당 되어 있어야 합니다**.</span><span class="sxs-lookup"><span data-stu-id="477bd-153">In order to view and use the reports described in this article, **you must have an appropriate role assigned for both the Security &amp; Compliance Center and the Exchange admin center**.</span></span>

- <span data-ttu-id="477bd-154">보안 &amp; 및 준수 센터에는 다음 역할 중 하나가 할당 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-154">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="477bd-155">조직 관리</span><span class="sxs-lookup"><span data-stu-id="477bd-155">Organization Management</span></span>
    - <span data-ttu-id="477bd-156">보안 관리자 (Azure Active Directory 관리 센터[https://aad.portal.azure.com](https://aad.portal.azure.com)에서 할당할 수 있음)</span><span class="sxs-lookup"><span data-stu-id="477bd-156">Security Administrator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com)))</span></span>
    - <span data-ttu-id="477bd-157">보안 독자</span><span class="sxs-lookup"><span data-stu-id="477bd-157">Security Reader</span></span>

- <span data-ttu-id="477bd-158">exchange online의 경우 exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) 또는 PowerShell cmdlet ( [exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조)에서 다음 역할 중 하나를 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-158">For Exchange Online, you must have one of the following roles assigned in either the Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) or with PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span></span>
    - <span data-ttu-id="477bd-159">조직 관리</span><span class="sxs-lookup"><span data-stu-id="477bd-159">Organization Management</span></span>
    - <span data-ttu-id="477bd-160">보기 전용 조직 관리</span><span class="sxs-lookup"><span data-stu-id="477bd-160">View-only Organization Management</span></span>
    - <span data-ttu-id="477bd-161">보기 권한만 있는 받는 사람 역할</span><span class="sxs-lookup"><span data-stu-id="477bd-161">View-Only Recipients role</span></span>
    - <span data-ttu-id="477bd-162">준수 관리</span><span class="sxs-lookup"><span data-stu-id="477bd-162">Compliance Management</span></span>

<span data-ttu-id="477bd-163">자세한 내용은 다음 리소스를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="477bd-163">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="477bd-164">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="477bd-164">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="477bd-165">Exchange Online의 기능 사용 권한</span><span class="sxs-lookup"><span data-stu-id="477bd-165">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="477bd-166">보고서에 데이터가 표시 되지 않으면 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="477bd-166">What if the reports aren't showing data?</span></span>

<span data-ttu-id="477bd-167">ATP 보고서에 데이터가 표시 되지 않는 경우 정책이 올바르게 설정 되어 있는지 다시 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-167">If you are not seeing data in your ATP reports, double-check that your policies are set up correctly.</span></span> <span data-ttu-id="477bd-168">조직에 atp 보호 기능을 적용 하려면 atp [안전한 링크 정책](set-up-atp-safe-links-policies.md) 및 [atp 안전 첨부 파일 정책이](set-up-atp-safe-attachments-policies.md) 정의 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="477bd-168">Your organization must have [ATP Safe Links policies](set-up-atp-safe-links-policies.md) and [ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for ATP protection to be in place.</span></span> <span data-ttu-id="477bd-169">또한 [Office 365에서 스팸 방지 및 맬웨어 방지 보호 기능을](anti-spam-and-anti-malware-protection.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="477bd-169">Also see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="477bd-170">관련 항목</span><span class="sxs-lookup"><span data-stu-id="477bd-170">Related topics</span></span>

[<span data-ttu-id="477bd-171">Office 365 보안 &amp; 및 준수 센터의 보고서 및 정보</span><span class="sxs-lookup"><span data-stu-id="477bd-171">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="477bd-172">보안 &amp; 및 준수 센터에서 보고서 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="477bd-172">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="477bd-173">보안 &amp; 및 준수 센터에서 사용자 지정 보고서 설정 및 다운로드</span><span class="sxs-lookup"><span data-stu-id="477bd-173">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

