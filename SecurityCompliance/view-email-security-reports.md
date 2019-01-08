---
title: 보안에서 전자 메일 보안 보고서를 보려면 &amp; 준수 센터
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/07/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3a137e28-1174-42d5-99af-f18868b43e86
description: 찾기 및 Office 365 엔터프라이즈와 조직에 대 한 전자 메일 보안 보고서를 사용 하는 방법에 알아봅니다. 전자 메일 보안 보고서는 보안에서 사용할 수 있는 &amp; 준수 센터입니다.
ms.openlocfilehash: 670317707c5695161f23615fb87fe93258e8d95b
ms.sourcegitcommit: 30faa3ba91cab4c36e3d8d8ed5858d5269ea8a56
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27749332"
---
# <a name="view-email-security-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="ea595-104">보안에서 전자 메일 보안 보고서를 보려면 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="ea595-104">View email security reports in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="ea595-p102">다양 한 전자 메일 보안 보고서에서 사용할 수는 [보안 &amp; 준수 센터](https://security.microsoft.com) 를 Office 365의 스팸 방지 및 맬웨어 방지 기능 조직을 보호 하는 방법을 확인할 수 있도록 합니다. 보안에서 이러한 보고서를 볼 수는 [필요한 사용 권한](#what-permissions-are-needed-to-view-these-reports)을가 &amp; **보고서** 로 이동 하 여 준수 센터 \> **대시보드**합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-p102">A variety of email security reports are available in the [Security &amp; Compliance Center](https://security.microsoft.com) to help you see how anti-spam and anti-malware features in Office 365 are protecting your organization. If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the Security &amp; Compliance Center by going to **Reports** \> **Dashboard**.</span></span>
  
![보안&amp; 규정 준수 센터 대시보드는 Advanced Threat Protection이 작업 중인 위치를 확인할 수 있도록 도와줍니다](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="ea595-108">전자 메일 보안 보고서는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-108">Your email security reports include the following:</span></span>
  
- [<span data-ttu-id="ea595-109">위협 보호 상태 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-109">Threat Protection Status report</span></span>](view-email-security-reports.md#tps) 
    
- [<span data-ttu-id="ea595-110">맬웨어 감지 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-110">Malware Detections report</span></span>](view-email-security-reports.md#maldet)
    
- [<span data-ttu-id="ea595-111">상위 맬웨어 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-111">Top Malware report</span></span>](#top-malware-report)
    
- [<span data-ttu-id="ea595-112">주요 보낸사람 및 받는 사람에 게 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-112">Top Senders and Recipients report</span></span>](view-email-security-reports.md#topsenders)
    
- [<span data-ttu-id="ea595-113">스푸핑 메일 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-113">Spoof Mail report</span></span>](#spoof-mail-report)
    
- [<span data-ttu-id="ea595-114">스팸 감지 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-114">Spam Detections report</span></span>](#spam-detections-report)
    
- [<span data-ttu-id="ea595-115">보내고 받은 메일 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-115">Sent and received email report</span></span>](view-email-security-reports.md#sentreceivedemail)
    
- <span data-ttu-id="ea595-116">[사용자가 보고 메시지 보고서](view-email-security-reports.md#userreported) (새!)</span><span class="sxs-lookup"><span data-stu-id="ea595-116">[User-reported messages report](view-email-security-reports.md#userreported) (new!)</span></span> 
    
## <a name="threat-protection-status-report"></a><span data-ttu-id="ea595-117">위협 보호 상태 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-117">Threat Protection Status report</span></span>

<span data-ttu-id="ea595-p103">새로운 **위협 보호 상태** 보고서가 감지 및 Exchange Online Protection에 의해 차단 된 악의적인 전자 메일을 표시 하는 스마트 보고서입니다. 이 보고서는 맬웨어 또는 피싱 시도로 식별 된 전자 메일에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-p103">The new **Threat Protection Status** report is a smart report that shows malicious email that was detected and blocked by Exchange Online Protection. This report shows information about email identified as malware or a phishing attempt.</span></span> 

> [!NOTE]
> <span data-ttu-id="ea595-p104">위협 보호 상태 보고서는 고객에 게 [Office 365 ATP](office-365-atp.md) 또는 [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP);가 사용할 수 있는 그러나 ATP 고객에 대 한 위협 보호 상태 보고서에 표시 되는 정보 나타날 EOP 고객 보다 다양 한 데이터를 가능성이 포함 됩니다. 예, EOP 고객 맬웨어 전자 메일, 하지만 하지 [SharePoint Online, OneDrive, 또는 Microsoft 팀의 악의적인 파일을 검색](atp-for-spo-odb-and-teams.md)하는 방법에 대 한 정보, ATP 관련 기능에서 검색 하는 방법에 대 한 정보를 볼 수 있습니다. ([ATP 보고서에 대 한 자세한 설명](view-reports-for-atp.md)입니다.)</span><span class="sxs-lookup"><span data-stu-id="ea595-p104">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see. For example, EOP customers can view information about malware detected in email, but not information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md), an ATP-specific capability. ([Learn more about ATP reports](view-reports-for-atp.md).)</span></span>
  
<span data-ttu-id="ea595-123">이 보고서를 보려면는 [보안 &amp; 준수 센터](https://security.microsoft.com), **보고서** 로 이동 \> **대시보드** \> **위협 보호 상태**입니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-123">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![위협 보호 상태 보고서](media/0ff86e12-c2b2-4d89-92a5-cefb054dc070.png)
  
<span data-ttu-id="ea595-p105">처음으로 위협 보호 상태 보고서를 열 때 보고서 데이터 지난 7 일간 기본적으로 표시 합니다. 그러나 **필터** 를 클릭 수 있으며 최대 90 일 분의 세부 정보에 대 한 날짜 범위를 변경할 수 있습니다. 이 보고서는 장기적인 추세 및 효율성 및 조직의 Exchange Online 보호 기능에 미치는 영향을 보기에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-p105">When you first open the Threat Protection Status report, the report shows data for the past seven days by default; however, you can click **Filters** and change the date range for up to 90 days of detail. This report is useful for viewing the effectiveness and impact of your organization's Exchange Online Protection features, and for longer-term trending.</span></span> 
  
![위협 보호 상태 보고서 필터](media/ab6b6b8d-e97a-4c3a-8fb1-c4940dcb7a07.png)
  
<span data-ttu-id="ea595-128">여부 악의적인로 식별 된 전자 메일에 대 한 데이터를 보려면 피싱 시도 식별 된 전자 메일 또는 전자 메일으로 식별 된 맬웨어를 포함 된 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-128">You can also choose whether to view data for email identified as malicious, email identified as a phishing attempts, or email identified as containing malware.</span></span>
  
![위협 보호 상태 보고서 보기 옵션](media/d429ecd7-cb7a-4c99-8d27-79a2832cf467.png)
  
## <a name="malware-detections-report"></a><span data-ttu-id="ea595-130">맬웨어 감지 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-130">Malware Detections report</span></span>

<span data-ttu-id="ea595-131">**맬웨어 감지** 보고서에는 조직에 대 한 맬웨어를 포함 하는으로 얼마나 많은 들어오고 나가는 메시지 검색 된 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-131">The **Malware Detections** report shows how many incoming and outgoing messages were detected as containing malware for your organization.</span></span> 
  
<span data-ttu-id="ea595-132">이 보고서를 보려면는 [보안 &amp; 준수 센터](https://security.microsoft.com), **보고서** 로 이동 \> **대시보드** \> **맬웨어 감지**합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-132">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Malware Detections**.</span></span>
  
![맬웨어 감지 보고서 예제](media/a1ba61a3-565a-46d6-b0d5-6a6cff6b31d7.png)
  
<span data-ttu-id="ea595-p106">위협 보호 상태 보고서와 같은 다른 보고서와 비슷한 보고서를 표시 하는 데이터는 지난 7 일간 기본적으로 합니다. 그러나 날짜 범위를 변경 하려면 **필터** 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-p106">Similar to other reports, like the Threat Protection Status report, the report displays data for the past seven days by default. However, you can choose **Filters** to change the date range.</span></span> 
  
## <a name="top-malware-report"></a><span data-ttu-id="ea595-136">상위 맬웨어 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-136">Top Malware report</span></span>

<span data-ttu-id="ea595-137">**상위 맬웨어** 보고서에는 Exchange Online에서 검색 된 맬웨어의 다양 한 종류를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-137">The **Top Malware** report shows the various kinds of malware that was detected by Exchange Online.</span></span> 
  
<span data-ttu-id="ea595-138">이 보고서를 보려면는 [보안 &amp; 준수 센터](https://security.microsoft.com), **보고서** 로 이동 \> **대시보드** \> **상위 맬웨어**입니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-138">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Top Malware**.</span></span>
  
![SCC-EOP 상위 맬웨어](media/763330b3-f56e-4ba4-b0bb-051500ae950a.png)
  
<span data-ttu-id="ea595-140">원형 차트에 웨지 위에 마우스를 가져가면 맬웨어 및 얼마나 많은 메시지는 맬웨어 있는 것으로 검색 된 종류의 이름을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-140">When you hover over a wedge in the pie chart, you can see the name of a kind of malware and how many messages were detected as having that malware.</span></span>
  
<span data-ttu-id="ea595-141">보고서를 보고서의 상세 보기를 확인할 수 있는 새 브라우저 창에서 엽니다를 클릭 (또는 누릅니다).</span><span class="sxs-lookup"><span data-stu-id="ea595-141">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
![이 보고서는 조직에 대 한 검색 상위 맬웨어 표시](media/3fded224-fb31-4713-86f2-8afce5ce2991.png)
  
<span data-ttu-id="ea595-143">다음은 차트 아래 검색 된 맬웨어 및 얼마나 많은 메시지는 맬웨어 있는 것으로 검색 된 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-143">Below the chart, you'll see a list of detected malware and how many messages were detected as having that malware.</span></span>
  
## <a name="top-senders-and-recipients-report"></a><span data-ttu-id="ea595-144">주요 보낸사람 및 받는 사람에 게 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-144">Top Senders and Recipients report</span></span>

<span data-ttu-id="ea595-145">**위쪽 보낸사람 및 받는 사람에 게** 보고서가 위쪽 전자 메일 보낸사람을 표시 하는 원형 차트입니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-145">The **Top Senders and Recipients** report is a pie chart showing your top email senders.</span></span> 
  
<span data-ttu-id="ea595-146">이 보고서를 보려면는 [보안 &amp; 준수 센터](https://security.microsoft.com), **보고서** 로 이동 \> **대시보드** \> **위쪽 보낸사람 및 받는 사람**입니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-146">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Top Senders and Recipients**.</span></span>
  
![보안에이 보고서를 보려면 &amp; 준수 센터, 보고서로 이동 \> 대시보드 \> 위쪽 보낸사람 및 받는 사람](media/b5506b5c-2420-4a5a-9ea3-d654294ac838.png)
  
<span data-ttu-id="ea595-148">원형 차트에 웨지 위에 마우스를 가져가면 보내거나 받은 메시지의 수를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-148">When you hover over a wedge in the pie chart, you can see a count of messages sent or received.</span></span>
  
<span data-ttu-id="ea595-149">보고서를 보고서의 상세 보기를 확인할 수 있는 새 브라우저 창에서 엽니다를 클릭 (또는 누릅니다).</span><span class="sxs-lookup"><span data-stu-id="ea595-149">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
<span data-ttu-id="ea595-p107">**에 대 한 데이터를 표시** 목록을 사용 하 여 맬웨어 받는 사람, 수신기, 스팸 받는 사람 및 보낸사람에 대 한 데이터를 볼 것인지를 선택 합니다. 고급 위협 보호 하 여 검색 된 맬웨어를 받은 사람을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-p107">Use the **Show data for** list to choose whether to view data for top senders, receivers, spam recipients, and malware recipients. You can also see who received malware that was detected by Advanced Threat Protection.</span></span> 
  
![표시 데이터에 대 한 목록을 사용 하 여 특정 정보를 보려면](media/bd91449f-7d42-4749-8666-7b44044049b8.png)
  
<span data-ttu-id="ea595-153">다음은 차트 아래가 위쪽 전자 메일 보낸 사람의 볼 수 있습니다 또는 주어진된 기간에 대 한 보내거나 받는 메시지와 함께 받는 사람에 게 했습니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-153">Below the chart, you'll see who the top email senders or recipients were, along with a count of messages sent or received for the given time period.</span></span>
  
## <a name="spoof-mail-report"></a><span data-ttu-id="ea595-154">스푸핑 메일 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-154">Spoof Mail report</span></span>

<span data-ttu-id="ea595-155">얼마나 많은 스푸핑 메일 메시지 검색 된 **스푸핑 메일** 보고서에 표시 하 고 그 중 어떤 것 된 것으로 간주 "좋음" (스푸핑 메일 합법적인 업무상의 이유로 수행).</span><span class="sxs-lookup"><span data-stu-id="ea595-155">The **Spoof Mail** report shows how many spoof mail messages were detected, and of those, which ones were considered "good" (spoof mail done for legitimate business reasons).</span></span> 
  
<span data-ttu-id="ea595-156">이 보고서를 보려면는 [보안 &amp; 준수 센터](https://security.microsoft.com), **보고서** 로 이동 \> **대시보드** \> **스푸핑 메일**입니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-156">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Spoof Mail**.</span></span>
  
![보안에이 보고서를 보려면 &amp; 준수 센터, 보고서로 이동 \> 대시보드 \> 스푸핑 메일](media/0427e85c-9e40-4225-a0f0-e21a4e8b0e44.png)
  
<span data-ttu-id="ea595-158">다음은 차트에는 하루 위에 올려 놓으면 얼마나 많은 스푸핑 메일 메시지를 통해 사람이 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-158">When you hover over a day in the chart, you can see how many spoof mail messages came through.</span></span>
  
<span data-ttu-id="ea595-159">보고서를 보고서의 상세 보기를 확인할 수 있는 새 브라우저 창에서 엽니다를 클릭 (또는 누릅니다).</span><span class="sxs-lookup"><span data-stu-id="ea595-159">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
## <a name="spam-detections-report"></a><span data-ttu-id="ea595-160">스팸 감지 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-160">Spam Detections report</span></span>

<span data-ttu-id="ea595-161">**스팸 감지** 보고서에는 Exchange Online에 의해 차단 되는 모든 스팸 콘텐츠를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-161">The **Spam Detections** report shows all the spam content blocked by Exchange Online.</span></span> 
  
<span data-ttu-id="ea595-162">이 보고서를 보려면는 [보안 &amp; 준수 센터](https://security.microsoft.com), **보고서** 로 이동 \> **대시보드** \> **스팸 감지**합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-162">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Spam Detections**.</span></span>
  
![보안에이 보고서를 보려면 &amp; 준수 센터, 보고서로 이동 \> 대시보드 \> EOP 스팸 감지](media/028cff3c-79ce-4ec0-8f0f-ec32ac28243a.png)
  
<span data-ttu-id="ea595-p108">다음은 차트에는 하루 위에 올려 놓으면 해당 항목은 분류 하는 방법에 따라 해당 날짜를 차단 된 항목 수를 볼 수 있습니다. 예, 얼마나 많은 스팸 메시지 필터링 된 및 차단 된 IP (인터넷 프로토콜) 주소에서 보낸 항목 수를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-p108">When you hover over a day in the chart, you can see how many items were blocked that day, as well as how those items are categorized. For example, you can see how many spam messages were filtered, and how many items came from a blocked Internet Protocol (IP) address.</span></span>
  
<span data-ttu-id="ea595-166">보고서를 보고서의 상세 보기를 확인할 수 있는 새 브라우저 창에서 엽니다를 클릭 (또는 누릅니다).</span><span class="sxs-lookup"><span data-stu-id="ea595-166">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
![얼마나 많은 스팸 메시지 차단 또는 필터링 된 스팸 감지 보고서 지시 하기](media/370ec67d-eb30-4863-bfcf-68a41be02295.png)
  
<span data-ttu-id="ea595-p109">다음은 차트 아래 검색 된 스팸 항목 목록이 표시 됩니다. 인바운드 또는 아웃 바운드 스팸 항목의 했는지 여부, 해당 메시지 ID 및 해당 받는 사람 등의 추가 정보를 보려면 항목을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-p109">Below the chart, you'll see a list of spam items that were detected. Select an item to view additional information, such as whether the spam item was inbound or outbound, its message ID, and its recipient.</span></span>
  
## <a name="sent-and-received-email-report"></a><span data-ttu-id="ea595-170">보내고 받은 메일 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-170">Sent and received email report</span></span>

<span data-ttu-id="ea595-171">**송신 및 수신된 전자 메일** 보고서가 수신 및 발신 전자 메일을 스팸이 감지 된, 맬웨어 및 "양호한."로 식별 된 전자 메일을 포함 하는 방법에 대 한 정보를 표시 하는 스마트 보고서</span><span class="sxs-lookup"><span data-stu-id="ea595-171">The **Sent and received email** report is a smart report that shows information about incoming and outgoing email, including spam detections, malware, and email identified as "good."</span></span> 
  
<span data-ttu-id="ea595-172">이 보고서를 보려면는 [보안 &amp; 준수 센터](https://security.microsoft.com), **보고서** 로 이동 \> **대시보드** \> **송신 및 수신된 전자 메일**입니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-172">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Sent and received email**.</span></span>
  
![보안에이 보고서를 보려면 &amp; 준수 센터, 보고서로 이동 \> 대시보드 \> 송신 및 수신된 전자 메일](media/0e710ed0-1b0e-4dac-8796-94a01a710f3a.png)
  
<span data-ttu-id="ea595-p110">다음은 차트에는 하루 위에 올려 놓으면 얼마나 많은 메시지에서 제공 하 고 해당 메시지를 분류 하는 방법을 볼 수 있습니다. 예, 얼마나 많은 메시지 맬웨어를 가진 것으로 발견 되 고 스팸으로 식별 된 수를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-p110">When you hover over a day in the chart, you can see how many messages came in, and how those messages are categorized. For example, you can see how many messages were detected as containing malware, and how many were identified as spam.</span></span>
  
<span data-ttu-id="ea595-176">보고서를 보고서의 상세 보기를 확인할 수 있는 새 브라우저 창에서 엽니다를 클릭 (또는 누릅니다).</span><span class="sxs-lookup"><span data-stu-id="ea595-176">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
<span data-ttu-id="ea595-177">유형별 또는 방향 (수신 및 발신) 하 여 정보를 보려면 **별로 구분** 목록을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-177">You can use the **Break down by** list to view information by type or by direction (incoming and outgoing).</span></span> 
  
![Break 다운 하 여 목록을 사용 하 여 형식 또는 방향을 하 여 정보를 보려면](media/a5b30c94-d75f-4bfc-851a-cb155685b177.png)
  
<span data-ttu-id="ea595-p111">다음은 차트 아래 **GoodMail**, **SpamContentFiltered**등의 전자 메일 종류 목록이 표시 됩니다. 맬웨어를 취한 조치 등의 추가 정보를 보려면 및 전자 메일 여부를 범주를 선택 들어오거나 나가는 했습니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-p111">Below the chart, you'll see a list of email categories, such as **GoodMail**, **SpamContentFiltered**, and so on. Select a category to view additional information, such as actions that were taken for malware, and whether email was incoming or outgoing.</span></span>
  
![이 보고서-맬웨어, 스팸 방지 및 기타 메시지 감지 하는 방법에 대 한 알려줍니다 메시지를 표시 합니다.](media/9ea4b606-f27a-46ee-97a7-be018e2b839c.png)
  
## <a name="user-reported-messages-report-new"></a><span data-ttu-id="ea595-182">사용자가 보고 메시지 보고서 (새!)</span><span class="sxs-lookup"><span data-stu-id="ea595-182">User-reported messages report (new!)</span></span>

<span data-ttu-id="ea595-183">다음은 **사용자가 보고 메시지** 보고서는 [보고서 메시지의 추가 기능](enable-the-report-message-add-in.md)을 사용 하 여 사용자가 정크, 피싱 시도 또는 정상 메일으로 보고 있는 전자 메일 메시지에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-183">The **User-reported messages** report shows information about email messages that users have reported as junk, phishing attempts, or good mail by using the [Report Message add-in](enable-the-report-message-add-in.md).</span></span>
  
<span data-ttu-id="ea595-p112">배달 이유, 이러한 스팸 정책 예외 또는 조직에 대해 구성 된 메일 흐름 규칙을 포함 한 각 메시지에 대 한 자세한 내용은 수 있습니다. 세부 정보를 보려면 사용자 보고서 목록에서 항목을 선택 하 고 **요약** 및 **세부 정보** 탭에서 정보를 볼 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-p112">Details are available for each message, including the delivery reason, such a spam policy exception or mail flow rule configured for your organization. To view details, select an item in the user-reports list, and then view the information on the **Summary** and **Details** tabs.</span></span> 
  
![User-Reported 메시지 보고서 시도 정크, 하지 정크, 또는 피싱으로 표시 된 메시지 사용자를 표시 합니다.](media/ad5e9a3d-b833-419c-bcc9-3425d9604ead.png)
  
<span data-ttu-id="ea595-187">이 보고서를 보려면는 [보안 &amp; 준수 센터](https://security.microsoft.com), 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-187">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), do one of the following:</span></span>
  
- <span data-ttu-id="ea595-188">**위협 관리** 로 이동 \> **대시보드** \> **메시지 사용자가 보고**합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-188">Go to **Threat management** \> **Dashboard** \> **User-reported messages**.</span></span>
    
- <span data-ttu-id="ea595-189">**위협 관리** 로 이동 \> **검토** \> **메시지 사용자가 보고**합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-189">Go to **Threat management** \> **Review** \> **User-reported messages**.</span></span>
    
![보안에서 &amp; 준수 센터 위협 관리를 선택 \> 검토 \> 사용자가 메시지 보고](media/e372c57c-1414-4616-957b-bc933b8c8711.png)
  
> [!IMPORTANT]
> <span data-ttu-id="ea595-p113">순서로 올바로 작동 하는 사용자가 보고 메시지 보고서에 대 한 Office 365 환경에 대 한 **감사 로깅을 설정 해야** 합니다. 이 Exchange Online 할당 된 감사 로그 역할을 가진 사용자가 일반적으로 수행 됩니다. 자세한 내용은 [Office 365 설정 또는 해제 로그 검색 감사](turn-audit-log-search-on-or-off.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ea595-p113">In order for the User-reported messages report to work correctly, **audit logging must be turned on** for your Office 365 environment. This is typically done by someone who has the Audit Logs role assigned in Exchange Online. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span> 
  
## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="ea595-194">이러한 보고서를 보려면 사용 권한은 필요 합니까?</span><span class="sxs-lookup"><span data-stu-id="ea595-194">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="ea595-195">이 문서에 설명 된 보고서 보기 및 사용 하기 위해 **모두 보안에서 할당 하는 적절 한 역할을 해야 &amp; 준수 센터 및 Exchange 관리 센터**합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-195">In order to view and use the reports described in this article, **you must have an appropriate role assigned in both the Security &amp; Compliance Center and the Exchange Admin Center**.</span></span>

- <span data-ttu-id="ea595-196">보안을 위해 &amp; 준수 센터 있어야 할당 된 다음 역할 중 하나:</span><span class="sxs-lookup"><span data-stu-id="ea595-196">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="ea595-197">조직 관리</span><span class="sxs-lookup"><span data-stu-id="ea595-197">Organization Management</span></span>
    - <span data-ttu-id="ea595-198">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="ea595-198">Security Administrator</span></span>
    - <span data-ttu-id="ea595-199">보안 읽기 권한자</span><span class="sxs-lookup"><span data-stu-id="ea595-199">Security Reader</span></span>

- <span data-ttu-id="ea595-200">Exchange Online에 대 한 할당 된 다음 역할 중 하나가 있어야 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-200">For Exchange Online, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="ea595-201">조직 관리</span><span class="sxs-lookup"><span data-stu-id="ea595-201">Organization Management</span></span>
    - <span data-ttu-id="ea595-202">보기 전용 조직 관리</span><span class="sxs-lookup"><span data-stu-id="ea595-202">View-only Organization Management</span></span>
    - <span data-ttu-id="ea595-203">보기 권한만 있는 받는 사람 역할</span><span class="sxs-lookup"><span data-stu-id="ea595-203">View-Only Recipients role</span></span>
    - <span data-ttu-id="ea595-204">준수 관리</span><span class="sxs-lookup"><span data-stu-id="ea595-204">Compliance Management</span></span>

<span data-ttu-id="ea595-205">자세한 내용은 다음 리소스를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-205">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="ea595-206">Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="ea595-206">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="ea595-207">Exchange Online의 기능 사용 권한</span><span class="sxs-lookup"><span data-stu-id="ea595-207">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="ea595-208">경우에 어떻게 보고서 데이터를 표시 하지?</span><span class="sxs-lookup"><span data-stu-id="ea595-208">What if the reports aren't showing data?</span></span>

<span data-ttu-id="ea595-p114">보고서에서 데이터를 나타나지 않는 경우 정책에 올바르게 설정 하는 다시 확인 하십시오. 자세한 내용은 [Office 365의 스팸 방지 및 맬웨어 방지 보호 기능](anti-spam-and-anti-malware-protection.md)을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea595-p114">If you are not seeing data in your reports, double-check that your policies are set up correctly. To learn more, see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="ea595-211">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ea595-211">Related topics</span></span>

[<span data-ttu-id="ea595-212">Office 365 전자 메일 스팸 방지 보호</span><span class="sxs-lookup"><span data-stu-id="ea595-212">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="ea595-213">보고서 및 Office 365 보안에 대 한 의견 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="ea595-213">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="ea595-214">보안에서 보고서에 대 한 일정을 만들 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="ea595-214">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="ea595-215">설정 및 보안에서 사용자 지정 보고서를 다운로드 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="ea595-215">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

