---
title: 위협 탐색기 (및 실시간 검색)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/22/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: 보안 &amp; 및 준수 센터의 Explorer (및 실시간 검색)에 대해 알아봅니다.
ms.openlocfilehash: 62ba70cb62b0c92cf65d77dfaf3eb7306e93fa98
ms.sourcegitcommit: 2b46fba650df8d252b1dd2b3c3f080a383183a06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/23/2019
ms.locfileid: "34415733"
---
# <a name="threat-explorer-and-real-time-detections"></a><span data-ttu-id="0ff7c-103">위협 탐색기 (및 실시간 검색)</span><span class="sxs-lookup"><span data-stu-id="0ff7c-103">Threat Explorer (and real-time detections)</span></span>

<span data-ttu-id="0ff7c-104">조직에 [office 365 Advanced Threat Protection](office-365-atp.md) (OFFICE 365 ATP)이 있고 [필요한 사용 권한이](#required-licenses-and-permissions)있는 경우에는 **Explorer** 또는 **실시간** 검색 (이전의 실시간 보고서)에서 [새로운 기능을 참조 하세요. ](#new-features-in-real-time-detections)!).</span><span class="sxs-lookup"><span data-stu-id="0ff7c-104">If your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (Office 365 ATP), and you have the [necessary permissions](#required-licenses-and-permissions), you have either **Explorer** or **real-time detections** (formerly real-time reports — [see what's new](#new-features-in-real-time-detections)!).</span></span> <span data-ttu-id="0ff7c-105">보안 & 준수 센터에서 **위협 관리**로 이동한 다음 **Explorer** 또는 **실시간**검색을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-105">In the Security & Compliance Center, go to **Threat management**, and then choose **Explorer** OR **Real-time detections**.</span></span> 

|<span data-ttu-id="0ff7c-106">ATP 계획 2를 사용 하는 경우 다음을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-106">With ATP Plan 2, you see:</span></span>  |<span data-ttu-id="0ff7c-107">ATP 계획 1을 사용 하는 경우 다음을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-107">With ATP Plan 1, you see:</span></span>  |
|---------|---------|
|![위협 탐색기](media/threatmgmt-explorer.png)      |![실시간 검색](media/threatmgmt-realtimedetections.png)         |

<span data-ttu-id="0ff7c-110">Explorer (또는 실시간 검색)를 사용 하는 경우 보안 운영 팀이 효과적이 고 효율적으로 위협을 조사 하 고 대응 하는 데 사용할 수 있는 강력한 보고서가 있으며 다음과 같은 이미지와 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-110">With Explorer (or real-time detections), you have a powerful report that enables your Security Operations team to investigate and respond to threats effectively and efficiently, and it resembles the following image:</span></span> 

![위협 관리 \> 탐색기로 이동](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

<span data-ttu-id="0ff7c-112">이 보고서를 사용 하 여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-112">With this report, you can:</span></span>
- [<span data-ttu-id="0ff7c-113">Office 365 보안 기능으로 검색 된 맬웨어를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-113">See malware detected by Office 365 security features</span></span>](#see-malware-detected-in-email-by-technology)
- [<span data-ttu-id="0ff7c-114">피싱 Url에 대 한 데이터를 확인 하 고 결과를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-114">View data about phishing URLs and click verdict</span></span>](#view-data-about-phishing-urls-and-click-verdict)
- <span data-ttu-id="0ff7c-115">[탐색기의 보기에서 자동화 된 조사 및 응답 프로세스 시작](#start-automated-investigation-and-response) (ATP 요금제 2에만 해당)</span><span class="sxs-lookup"><span data-stu-id="0ff7c-115">[Start an automated investigation and response process from a view in Explorer](#start-automated-investigation-and-response) (ATP Plan 2 only)</span></span>
- <span data-ttu-id="0ff7c-116">... [악성 전자 메일을 조사 하 고 더 많은 방법을 확인해](#more-ways-to-use-explorer-or-real-time-detections)보세요.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-116">... [Investigate malicious email, and more](#more-ways-to-use-explorer-or-real-time-detections)!</span></span>

## <a name="new-features-in-real-time-detections"></a><span data-ttu-id="0ff7c-117">실시간 검색의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="0ff7c-117">New features in real-time detections</span></span>

<span data-ttu-id="0ff7c-118">Office 365 ATP 계획 1 고객의 경우 이전에는 *실시간* 검색 보고서를 *실시간 보고서*라고 했습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-118">For Office 365 ATP Plan 1 customers, the *real-time detections* report was previously referred to as *real-time reports*.</span></span> <span data-ttu-id="0ff7c-119">이름 변경 외에도 다음과 같은 몇 가지 새로운 기능과 향상 된 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-119">In addition to the name change, several new features and enhancements are rolling out:</span></span>

- <span data-ttu-id="0ff7c-120">피싱 보기에서는 [ATP 안전한 링크](atp-safe-links.md)를 통해 검색 된 url에 대 한 자세한 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-120">In the Phish view, you can see more details about detected URLs through [ATP Safe Links](atp-safe-links.md).</span></span> <span data-ttu-id="0ff7c-121">새로운 세부 정보 및 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-121">New details and capabilities include:</span></span>
  - <span data-ttu-id="0ff7c-122">전자 메일 메시지의 Url</span><span class="sxs-lookup"><span data-stu-id="0ff7c-122">URLs in email messages</span></span>
  - <span data-ttu-id="0ff7c-123">URL 정보를 기반으로 필터링</span><span class="sxs-lookup"><span data-stu-id="0ff7c-123">Filtering based on URL information</span></span>
  - <span data-ttu-id="0ff7c-124">데이터 그래프로 표시 되는 URL 정보</span><span class="sxs-lookup"><span data-stu-id="0ff7c-124">URL information displayed in data graphs</span></span>
  - <span data-ttu-id="0ff7c-125">메시지의 클릭에 대 한 시간 클릭 데이터</span><span class="sxs-lookup"><span data-stu-id="0ff7c-125">Time-of-click data about clicks in messages</span></span>

- <span data-ttu-id="0ff7c-126">URL이 변경 될 때마다 결과를 클릭 하면 경고가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-126">Whenever there's a change in a URL click verdict, you'll see an alert.</span></span> <span data-ttu-id="0ff7c-127">URL URL 신뢰도가 샌드 박싱 verdicts 변경 될 수도 있고, ATP 안전한 링크를 통해 보호 되는 사용자가 [Atp 안전한 링크 경고](atp-safe-links-warning-pages.md)를 재정의 하는 경우에는이 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-127">URL click verdicts can change when a URL’s reputation changes post-detonation, or when a user who's protected by ATP Safe Links overrides an [ATP Safe Links warning](atp-safe-links-warning-pages.md).</span></span>  
 
<span data-ttu-id="0ff7c-128">이러한 향상 된 기능을 통해 조직의 보안 관리자는 이전 보다 더 많은 세부 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-128">These enhancements enable your organization's security administrators to view more details than before.</span></span> <span data-ttu-id="0ff7c-129">보안 관리자는 URL 도메인, 누락 된 Url에 대 한 정보를 보고, verdicts를 클릭 한 다음 Office 365 ATP 정책을 적절 하 게 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-129">Security administrators can view information about URL domains, missed URLs, click verdicts, and more, and then adjust Office 365 ATP policies appropriately.</span></span>

> [!NOTE]
> <span data-ttu-id="0ff7c-130">이러한 기능이 미리 보기에 있는 동안에는 제한 된 일 수 동안 URL 데이터를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-130">While these features are in preview, URL data will be available for a limited number of days.</span></span> 

## <a name="see-malware-detected-in-email-by-technology"></a><span data-ttu-id="0ff7c-131">기술 별로 전자 메일에서 발견 된 맬웨어를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-131">See malware detected in email by technology</span></span>

<span data-ttu-id="0ff7c-132">Office 365 기술을 통해 전자 메일로 검색 된 맬웨어를 확인 하려는 경우를 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-132">Suppose you want to see malware detected in email, by Office 365 technology.</span></span> <span data-ttu-id="0ff7c-133">이 작업을 수행 하려면 [전자 메일 _GT_ 맬웨어](threat-explorer-views.md#email--malware) 보기 Explorer (또는 실시간 검색)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-133">To do this, use the [Email > Malware](threat-explorer-views.md#email--malware) view of Explorer (or real-time detections).</span></span>

1. <span data-ttu-id="0ff7c-134">Security &[https://protection.office.com](https://protection.office.com)준수 센터 ()에서 **Threat management** > **Explorer** (또는 **실시간**검색)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-134">In the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), choose **Threat management** > **Explorer** (or **Real-time detections**).</span></span> <span data-ttu-id="0ff7c-135">(이 예제에서는 탐색기를 사용 합니다.)</span><span class="sxs-lookup"><span data-stu-id="0ff7c-135">(This example uses Explorer.)</span></span>

2. <span data-ttu-id="0ff7c-136">**보기** 메뉴에서 **전자 메일** > **맬웨어**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-136">In the **View** menu, choose **Email** > **Malware**.</span></span><br/><span data-ttu-id="0ff7c-137">![탐색기에 대 한 보기 메뉴](media/ExplorerViewEmailMalwareMenu.png)</span><span class="sxs-lookup"><span data-stu-id="0ff7c-137">![View menu for Explorer](media/ExplorerViewEmailMalwareMenu.png)</span></span><br/>

3. <span data-ttu-id="0ff7c-138">**보낸 사람**을 클릭 한 다음 **기본** > **검색 기술을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-138">Click **Sender**, and then choose **Basic** > **Detection technology**.</span></span><br/><span data-ttu-id="0ff7c-139">이제 검색 기술을 보고서에 대 한 필터로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-139">Your detection technologies are now available as filters for the report.</span></span><br/><span data-ttu-id="0ff7c-140">![맬웨어 검색 기술](media/ExplorerEmailMalwareDetectionTech.png)</span><span class="sxs-lookup"><span data-stu-id="0ff7c-140">![Malware detection technologies](media/ExplorerEmailMalwareDetectionTech.png)</span></span><br/> 

4. <span data-ttu-id="0ff7c-141">옵션을 선택한 다음 **새로 고침** 단추를 클릭 하 여 해당 필터를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-141">Select an option, and then click the **Refresh** button to apply that filter.</span></span><br/><span data-ttu-id="0ff7c-142">![선택한 검색 기술](media/ExplorerEmailMalwareDetectionTechATP.png)</span><span class="sxs-lookup"><span data-stu-id="0ff7c-142">![Selected detection technology](media/ExplorerEmailMalwareDetectionTechATP.png)</span></span><br/> 

<span data-ttu-id="0ff7c-143">선택한 기술 옵션을 사용 하 여 전자 메일로 검색 된 결과 맬웨어가 표시 되도록 보고서가 새로 고쳐집니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-143">The report refreshes to show the results malware detected in email, using the technology option you selected.</span></span> <span data-ttu-id="0ff7c-144">여기서는 추가 분석을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-144">From here, you can conduct further analysis.</span></span>

## <a name="view-data-about-phishing-urls-and-click-verdict"></a><span data-ttu-id="0ff7c-145">피싱 Url에 대 한 데이터를 확인 하 고 결과를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-145">View data about phishing URLs and click verdict</span></span>

<span data-ttu-id="0ff7c-146">허용, 차단 및 재정의 된 Url 목록을 비롯 하 여 전자 메일의 Url을 통한 피싱 시도를 확인 하려는 경우를 가정해 봅니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-146">Suppose that you want to see phishing attempts through URLs in email, including a list of URLs that were allowed, blocked, and overridden.</span></span> <span data-ttu-id="0ff7c-147">클릭 한 Url을 식별 하려면 [ATP 안전한 링크](atp-safe-links.md) 를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-147">Identifying URLs that were clicked requires [ATP Safe links](atp-safe-links.md) to be configured.</span></span> <span data-ttu-id="0ff7c-148">클릭 verdicts 보호 및 로깅에 대 한 [Atp Safe links 정책이](set-up-atp-safe-links-policies.md) 설정 되었는지 확인 합니다. Atp safe 링크를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-148">Make sure that you have set up [ATP Safe Links policies](set-up-atp-safe-links-policies.md) for time-of-click protection and logging of click verdicts by ATP Safe Links.</span></span> 

<span data-ttu-id="0ff7c-149">메시지에서 피싱 Url을 검토 하 고 피싱 메시지의 Url을 클릭 하려면 Explorer의 [전자 메일 _GT_ 피싱](threat-explorer-views.md#email--phish) 보기 (실시간 검색)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-149">To review phish URLs in messages and clicks on URLs in phish messages, use the [Email > Phish](threat-explorer-views.md#email--phish) view of Explorer (or real-time detections).</span></span>

1. <span data-ttu-id="0ff7c-150">Security &[https://protection.office.com](https://protection.office.com)준수 센터 ()에서 **Threat management** > **Explorer** (또는 **실시간**검색)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-150">In the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), choose **Threat management** > **Explorer** (or **Real-time detections**).</span></span> <span data-ttu-id="0ff7c-151">(이 예제에서는 탐색기를 사용 합니다.)</span><span class="sxs-lookup"><span data-stu-id="0ff7c-151">(This example uses Explorer.)</span></span>

2. <span data-ttu-id="0ff7c-152">**보기** 메뉴에서 **전자 메일** > **피싱**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-152">In the **View** menu, choose **Email** > **Phish**.</span></span><br/><span data-ttu-id="0ff7c-153">![탐색기에 대 한 보기 메뉴](media/ExplorerViewEmailPhishMenu.png)</span><span class="sxs-lookup"><span data-stu-id="0ff7c-153">![View menu for Explorer](media/ExplorerViewEmailPhishMenu.png)</span></span><br/>

3. <span data-ttu-id="0ff7c-154">**보낸 사람**을 클릭 한 다음 **url** > 을 선택 합니다**결과를 클릭**합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-154">Click **Sender**, and then choose **URLs** > **Click verdict**.</span></span>

4. <span data-ttu-id="0ff7c-155">**차단** 됨 및 **무시 된 블록과**같은 옵션을 하나 이상 선택 하 고 해당 필터를 적용 하는 옵션과 같은 줄에 있는 **새로 고침** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-155">Select one or more options, such as **Blocked** and **Block overridden**, and then click the **Refresh** button that is on the same line as the options to apply that filter.</span></span> <span data-ttu-id="0ff7c-156">(브라우저 창을 새로 고치지 않습니다.)</span><span class="sxs-lookup"><span data-stu-id="0ff7c-156">(Don't refresh your browser window.)</span></span><br/><span data-ttu-id="0ff7c-157">![Url을 선택 하 고 verdicts을 클릭 합니다.](media/ThreatExplorerEmailPhishClickVerdictOptions.png)</span><span class="sxs-lookup"><span data-stu-id="0ff7c-157">![URLs and click verdicts](media/ThreatExplorerEmailPhishClickVerdictOptions.png)</span></span><br/>

    <span data-ttu-id="0ff7c-158">보고서를 새로 고치면 보고서 아래의 URL 탭에 서로 다른 두 개의 URL 테이블이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-158">The report refreshes to show two different URL tables on the URL tab under the report:</span></span>

   1. <span data-ttu-id="0ff7c-159">**상위 url** 은 필터링 된 메시지에 포함 된 url 및 각 URL에 대 한 전자 메일 배달 작업 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-159">**Top URLs** are the URLs contained in the messages you have filtered down to, and the email delivery action counts for each URL.</span></span> <span data-ttu-id="0ff7c-160">피싱 전자 메일 보기에서 일반적으로이 목록에는 합법적인 Url이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-160">In the phish email view, this list typically will contain legitimate URLs.</span></span> <span data-ttu-id="0ff7c-161">공격자는 메시지에 효과적이 고 잘못 된 Url을 함께 사용 하 여 배달 하려고 할 수 있지만, 사용자가 클릭 하는 데 더 흥미로운 악성 링크를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-161">Attackers include a mix of good and bad URLs in their messages to try to get them delivered, but they will make the malicious links more interesting for the user to click.</span></span> <span data-ttu-id="0ff7c-162">Url의 테이블은 총 전자 메일 수를 기준으로 정렬 됩니다 (참고:이 열은 보기를 단순하게 하기 위해 표시 되지 않음).</span><span class="sxs-lookup"><span data-stu-id="0ff7c-162">The table of URLs is sorted by total email count (NOTE: This column is not shown to simplify the view).</span></span>

   2. <span data-ttu-id="0ff7c-163">**위쪽** 클릭은 클릭 한 안전한 링크 래핑된 url이 총 클릭 횟수에 따라 정렬 되며 보기를 단순화 하기 위해이 열도 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-163">**Top clicks** are the Safe Links wrapped URLs that were clicked, sorted by total click count (this column is also not shown to simplify the view).</span></span> <span data-ttu-id="0ff7c-164">총 개수 열에서 안전한 링크를 나타냅니다. 클릭 한 각 URL에 대해 결과 count를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-164">Total counts by column indicate the Safe Links click verdict count for each clicked URL.</span></span> <span data-ttu-id="0ff7c-165">피싱 email (전자 메일 보기)에서 이러한 메시지는 일반적으로 의심 되거나 악성 Url 이지만 피싱 메시지가 있는 깨끗 한 Url을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-165">In the phish email view, these are more often suspicious or malicious URLs, but could include clean URLs that are in phish messages.</span></span> <span data-ttu-id="0ff7c-166">래핑 해제 한 링크의 URL 클릭은 여기에 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-166">URL clicks on unwrapped links will not show up here.</span></span>
   
   <span data-ttu-id="0ff7c-167">두 개의 Url 테이블에는 배달 작업 및 위치로 피싱 전자 메일의 상위 Url이 표시 되며, 사용자가 잘못 된 링크를 받아 사용자가 상호 작용 한 잠재적 문제를 파악할 수 있는 URL 클릭이 표시 됩니다 (또는 경고와 상관 없이 방문 됨).</span><span class="sxs-lookup"><span data-stu-id="0ff7c-167">The two URLs tables show top URLs in phishing emails by delivery action and location, and they show URL clicks that were blocked (or visited despite a warning) so that you can understand what potential bad links were received by users and interacted with by users.</span></span> <span data-ttu-id="0ff7c-168">여기서는 추가 분석을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-168">From here, you can conduct further analysis.</span></span> <span data-ttu-id="0ff7c-169">예를 들어 차트 아래에서 조직의 환경에서 차단 된 전자 메일의 상위 Url을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-169">For example, below the chart, you can see the top URLs in emails that were blocked in your organization's environment.</span></span>
   
   ![차단 된 탐색기 Url](media/ExplorerPhishClickVerdictURLs.png)
   
   <span data-ttu-id="0ff7c-171">자세한 정보를 보려면 URL을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-171">Select a URL to view more detailed information.</span></span> <span data-ttu-id="0ff7c-172">URL 플라이 아웃 대화 상자에서 전자 메일에 대 한 필터링이 제거 되어 사용자 환경에 표시 되는 URL의 전체 보기를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-172">Note that in the URL flyout dialog, the filtering on emails is removed to show you the full view of the URL's exposure in your environment.</span></span> <span data-ttu-id="0ff7c-173">이를 통해 탐색기의 전자 메일을 관심 있는 항목으로 필터링 하 고, 잠재적인 위협이 되는 특정 Url을 찾은 다음, url 정보 대화 상자를 통해 해당 환경의 URL 노출에 대 한 이해를 확장 하 여 url 필터를 탐색기 보기 자체</span><span class="sxs-lookup"><span data-stu-id="0ff7c-173">This lets you filter down emails in Explorer to ones you are concerned about, find specific URLs that are potential threats, then expand your understanding of the URL exposure in your environment (via the URL details dialog) without having to add URL filters to the Explorer view itself.</span></span>

## <a name="review-email-messages-reported-by-users"></a><span data-ttu-id="0ff7c-174">사용자가 보고 한 전자 메일 메시지 검토</span><span class="sxs-lookup"><span data-stu-id="0ff7c-174">Review email messages reported by users</span></span>

<span data-ttu-id="0ff7c-175">조직의 사용자가 [outlook 및 웹용 outlook에 대 한 보고서 메시지 추가 기능](enable-the-report-message-add-in.md)을 사용 하 여 정크 메일 또는 피싱이 아닌 메시지를 보고 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-175">Suppose that you want to see email messages that users in your organization have reported as Junk, Not Junk, or Phishing by using the [Report Message add-in for Outlook and Outlook on the web](enable-the-report-message-add-in.md).</span></span> <span data-ttu-id="0ff7c-176">이렇게 하려면 [전자 메일 _GT_ 사용자가 보고](threat-explorer-views.md#email--user-reported) 하는 Explorer (또는 실시간 검색)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-176">To do this, use the [Email > User-reported](threat-explorer-views.md#email--user-reported) view of Explorer (or real-time detections).</span></span>

1. <span data-ttu-id="0ff7c-177">Security &[https://protection.office.com](https://protection.office.com)준수 센터 ()에서 **Threat management** > **Explorer** (또는 **실시간**검색)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-177">In the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), choose **Threat management** > **Explorer** (or **Real-time detections**).</span></span> <span data-ttu-id="0ff7c-178">(이 예제에서는 탐색기를 사용 합니다.)</span><span class="sxs-lookup"><span data-stu-id="0ff7c-178">(This example uses Explorer.)</span></span>

2. <span data-ttu-id="0ff7c-179">**보기** 메뉴에서**사용자가 보고 한** **전자 메일** > 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-179">In the **View** menu, choose **Email** > **User-reported**.</span></span><br/><span data-ttu-id="0ff7c-180">![탐색기에 대 한 보기 메뉴](media/ExplorerViewMenuEmailUserReported.png)</span><span class="sxs-lookup"><span data-stu-id="0ff7c-180">![View menu for Explorer](media/ExplorerViewMenuEmailUserReported.png)</span></span><br/>

3. <span data-ttu-id="0ff7c-181">**보낸 사람**을 클릭 한 다음 **기본** > **보고서 유형을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-181">Click **Sender**, and then choose **Basic** > **Report type**.</span></span>

4. <span data-ttu-id="0ff7c-182">**피싱**등의 옵션을 선택 하 고 **새로 고침** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-182">Select an option, such as **Phish**, and then click the **Refresh** button.</span></span> <br/><span data-ttu-id="0ff7c-183">![사용자가 보고 한 피싱](media/EmailUserReportedReportType.png)</span><span class="sxs-lookup"><span data-stu-id="0ff7c-183">![User-reported phish](media/EmailUserReportedReportType.png)</span></span><br/> 

<span data-ttu-id="0ff7c-184">보고서가 새로 고쳐지고 조직의 사용자가 피싱 시도로 보고 한 전자 메일 메시지에 대 한 데이터가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-184">The report refreshes to show data about email messages that people in your organization have reported as a phishing attempt.</span></span> <span data-ttu-id="0ff7c-185">이 정보를 사용 하 여 추가 분석을 수행 하 고, 필요한 경우 [ATP 피싱 방지 정책을](set-up-anti-phishing-policies.md)조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-185">You can use this information to conduct further analysis, and if necessary, adjust your [ATP anti-phishing policies](set-up-anti-phishing-policies.md).</span></span>

## <a name="start-automated-investigation-and-response"></a><span data-ttu-id="0ff7c-186">자동 조사 및 응답 시작</span><span class="sxs-lookup"><span data-stu-id="0ff7c-186">Start automated investigation and response</span></span>

> [!NOTE]
> <span data-ttu-id="0ff7c-187">자동화 된 조사 및 응답 기능은 **office 365 ATP 계획 2** 및 **Office 365 E5**에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-187">Automated investigation and response capabilities are available in **Office 365 ATP Plan 2** and **Office 365 E5**.</span></span>

<span data-ttu-id="0ff7c-188">(새로운 방법!) [자동화 된 조사 및 응답](automated-investigation-response-office.md) 은 사이버 공격을 조사 하 고 완화 하는 과정에서 보안 운영 팀을 훨씬 더 많은 시간과 노력으로 절감할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-188">(NEW!) [Automated investigation and response](automated-investigation-response-office.md) can save your security operations team much time and effort in investigating and mitigating cyber attacks.</span></span> <span data-ttu-id="0ff7c-189">보안 playbook 트리거될 수 있는 알림을 구성 하는 것 외에도 탐색기의 보기에서 자동화 된 조사 및 응답 프로세스를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-189">In addition to configuring alerts that can trigger a security playbook, you can start an automated investigation and response process from a view in Explorer.</span></span> 

<span data-ttu-id="0ff7c-190">이에 대 한 자세한 내용은 [예제: 보안 관리자가 탐색기에서 조사를 트리거하는 예](automated-investigation-response-office.md#example-a-security-administrator-triggers-an-investigation-from-threat-explorer)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-190">For details on this, see [Example: A security administrator triggers an investigation from Explorer](automated-investigation-response-office.md#example-a-security-administrator-triggers-an-investigation-from-threat-explorer).</span></span>

## <a name="more-ways-to-use-explorer-or-real-time-detections"></a><span data-ttu-id="0ff7c-191">Explorer (또는 실시간 검색)를 사용 하는 여러 방법</span><span class="sxs-lookup"><span data-stu-id="0ff7c-191">More ways to use Explorer (or real-time detections)</span></span>

<span data-ttu-id="0ff7c-192">이 문서에서 설명 하는 시나리오 외에도 Explorer (또는 실시간 검색)에서 사용할 수 있는 보고 옵션이 더 많이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-192">In addition to the scenarios outlined in this article, you have many more reporting options available with Explorer (or real-time detections).</span></span> 
- [<span data-ttu-id="0ff7c-193">배달된 악성 전자 메일 찾기 및 조사</span><span class="sxs-lookup"><span data-stu-id="0ff7c-193">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
- [<span data-ttu-id="0ff7c-194">SharePoint Online, OneDrive 및 Microsoft 팀에서 검색 된 악의적인 파일 보기</span><span class="sxs-lookup"><span data-stu-id="0ff7c-194">View malicious files detected in SharePoint Online, OneDrive, and Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
- [<span data-ttu-id="0ff7c-195">위협 탐색기 및 실시간 검색의 보기에 대 한 개요 보기</span><span class="sxs-lookup"><span data-stu-id="0ff7c-195">Get an overview of the views in Threat Explorer (and real-time detections)</span></span>](threat-explorer-views.md)

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="0ff7c-196">필요한 라이선스 및 사용 권한</span><span class="sxs-lookup"><span data-stu-id="0ff7c-196">Required licenses and permissions</span></span>

<span data-ttu-id="0ff7c-197">Explorer 또는 실시간 검색을 하려면 [Office 365 ATP](office-365-atp.md) 가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-197">You must have [Office 365 ATP](office-365-atp.md) to get Explorer or real-time detections.</span></span>
- <span data-ttu-id="0ff7c-198">Explorer는 Office 365 ATP 계획 2에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-198">Explorer is included in Office 365 ATP Plan 2.</span></span> 
- <span data-ttu-id="0ff7c-199">실시간 검색 보고서는 Office 365 ATP 계획 1에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-199">The real-time detections report is included in Office 365 ATP Plan 1.</span></span>

<span data-ttu-id="0ff7c-200">탐색기 또는 실시간 검색을 보고 사용 하려면 보안 관리자 또는 보안 판독기에 부여 된 것과 같은 적절 한 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-200">To view and use Explorer or real-time detections, you must have appropriate permissions, such as those granted to a security administrator or security reader.</span></span> 

- <span data-ttu-id="0ff7c-201">보안 &amp; 및 준수 센터에는 다음 역할 중 하나가 할당 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-201">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="0ff7c-202">조직 관리</span><span class="sxs-lookup"><span data-stu-id="0ff7c-202">Organization Management</span></span>
    - <span data-ttu-id="0ff7c-203">보안 관리자 (Azure Active Directory 관리 센터[https://aad.portal.azure.com](https://aad.portal.azure.com)에서 할당할 수 있음)</span><span class="sxs-lookup"><span data-stu-id="0ff7c-203">Security Administrator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com)))</span></span>
    - <span data-ttu-id="0ff7c-204">보안 독자</span><span class="sxs-lookup"><span data-stu-id="0ff7c-204">Security Reader</span></span>

- <span data-ttu-id="0ff7c-205">Exchange Online의 경우 Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) 또는 PowerShell Cmdlet ( [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조)에서 다음 역할 중 하나를 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-205">For Exchange Online, you must have one of the following roles assigned in either the Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) or with PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span></span>
    - <span data-ttu-id="0ff7c-206">조직 관리</span><span class="sxs-lookup"><span data-stu-id="0ff7c-206">Organization Management</span></span>
    - <span data-ttu-id="0ff7c-207">보기 전용 조직 관리</span><span class="sxs-lookup"><span data-stu-id="0ff7c-207">View-only Organization Management</span></span>
    - <span data-ttu-id="0ff7c-208">보기 권한만 있는 받는 사람 역할</span><span class="sxs-lookup"><span data-stu-id="0ff7c-208">View-Only Recipients role</span></span>
    - <span data-ttu-id="0ff7c-209">준수 관리</span><span class="sxs-lookup"><span data-stu-id="0ff7c-209">Compliance Management</span></span>

<span data-ttu-id="0ff7c-210">역할 및 사용 권한에 대 한 자세한 내용은 다음 리소스를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="0ff7c-210">To learn more about roles and permissions, see the following resources:</span></span>

- [<span data-ttu-id="0ff7c-211">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="0ff7c-211">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
- [<span data-ttu-id="0ff7c-212">Exchange Online의 기능 사용 권한</span><span class="sxs-lookup"><span data-stu-id="0ff7c-212">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
  
