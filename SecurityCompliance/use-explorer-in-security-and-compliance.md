---
title: 보안 &amp; 및 준수 센터에서 위협 탐색기 사용
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/21/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: 보안 &amp; 및 준수 센터의 Explorer (위협 탐색기 라고도 함)에 대해 알아봅니다.
ms.openlocfilehash: 202898873bb9611c747aed335d295c749c7cd0fa
ms.sourcegitcommit: a56128c7be5d59e976851c27301031e19fa1997d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30732261"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a><span data-ttu-id="958f7-103">보안 &amp; 및 준수 센터에서 위협 탐색기 사용</span><span class="sxs-lookup"><span data-stu-id="958f7-103">Use Threat Explorer in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="958f7-104">조직에 [Office 365 Advanced Threat Protection 계획 2](office-365-ti.md)가 있고 필요한 사용 권한이 있는 경우 위협 탐색기를 사용 하 여 위협을 식별 하 고 분석할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-104">If your organization has [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md), and you have the necessary permissions, you can use Threat Explorer to identify and analyze threats.</span></span> <span data-ttu-id="958f7-105">예를 들어 배달 된 악성 전자 메일을 식별 하 고 삭제할 수 있으며, Office 365 보안 기능으로 인해 발견 된 맬웨어를 볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-105">For example, you can identify and delete malicious email that was delivered, or see malware that was caught by Office 365 security features.</span></span> <span data-ttu-id="958f7-106">위협 탐색기 (탐색기 라고도 함)는 보안 운영 팀에서 보안 &amp; 및 준수 센터의 위협에 대해 조사 하 고 대응 하는 데 도움이 되는 강력한 거의 실시간 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-106">Threat Explorer (also referred to as Explorer) is a powerful near real-time tool to help Security Operations teams investigate and respond to threats in the Security &amp; Compliance Center.</span></span>
  
![위협 관리 \> 탐색기로 이동](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="958f7-108">Explorer를 &amp; 사용 하려면 보안 및 준수 센터에서 **위협 관리** \> **탐색기**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-108">To use Explorer, in the Security &amp; Compliance Center, go to **Threat management** \> **Explorer**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="958f7-109">office 365 위협 인텔리전스는 이제 추가 위협 방지 기능과 함께 office 365 Advanced Threat protection 계획 2를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-109">Office 365 Threat Intelligence is now Office 365 Advanced Threat Protection Plan 2, along with additional threat protection capabilities.</span></span> <span data-ttu-id="958f7-110">자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="958f7-110">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
      
## <a name="explorer-overview"></a><span data-ttu-id="958f7-111">탐색기 개요</span><span class="sxs-lookup"><span data-stu-id="958f7-111">Explorer overview</span></span>

<span data-ttu-id="958f7-112">조직에 [Office 365 위협 조사 및 응답 기능이](office-365-ti.md) 있고 (ATP 계획 2에 포함 되어 있음) 필요한 권한이 있는 경우 위협 탐색기 (탐색기 라고도 함)를 사용 하 여 위협을 식별 하 고 분석할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-112">If your organization has [Office 365 Threat investigation and response capabilities](office-365-ti.md) (this is included in ATP Plan 2), and you have the necessary permissions, you can use Threat Explorer (also referred to as Explorer) to identify and analyze threats.</span></span> <span data-ttu-id="958f7-113">보안 &amp; 및 준수 센터에서 **위협 관리** \> **탐색기**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-113">(In the Security &amp; Compliance Center, go to **Threat management** \> **Explorer**.)</span></span>

![위협 관리 \> 탐색기로 이동](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

<span data-ttu-id="958f7-115">이 문서에서는 Explorer를 사용 하 여 수행할 수 있는 몇 가지 방법에 대해 설명 합니다 (더 많은 가능성이 있음).</span><span class="sxs-lookup"><span data-stu-id="958f7-115">This article describes a few things you can do with Explorer (there are many more possibilities):</span></span>

- <span data-ttu-id="958f7-116">[전자 메일에서 검색 된 맬웨어 종류](#see-malware-detected-in-email-by-technology)및 위협 보호 기술 (맬웨어 방지 보호, ATP 안전한 첨부 파일 등)을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-116">[See what kinds of malware were detected in email](#see-malware-detected-in-email-by-technology), and by threat protection technology (anti-malware protection, ATP Safe Attachments, etc.)</span></span>

- <span data-ttu-id="958f7-117">[피싱 링크 (url)에 대 한 데이터를 보고](#view-data-about-phishing-urls-and-click-verdict), 클릭 verdicts의 용도 (경고 발생 시에는 url 차단, 허용 또는 방문 함)에 대 한 정보</span><span class="sxs-lookup"><span data-stu-id="958f7-117">[View data about phishing links (URLs)](#view-data-about-phishing-urls-and-click-verdict), and what the click verdicts were (URLs blocked, allowed, or visited despite warnings)</span></span>

- <span data-ttu-id="958f7-118">정크 메일로 [보고 되거나, 정크 메일 이나 피싱이 아닌](#review-email-messages-reported-by-users)모든 경향을 식별 하 고, 모든 추세 (예: 피싱로 보고 되는 일반적인 메시지 수를 초과 하는 경우)를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-118">[Review email messages that were reported as Junk, Not Junk, or Phishing](#review-email-messages-reported-by-users), and identify any trends (such as a larger than usual number of messages reported as Phish)</span></span> 

## <a name="see-malware-detected-in-email-by-technology"></a><span data-ttu-id="958f7-119">기술 별로 전자 메일에서 발견 된 맬웨어를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="958f7-119">See malware detected in email by technology</span></span>

<span data-ttu-id="958f7-120">전자 메일에서 검색 된 맬웨어 및 Office 365의 기술에 대해 확인 하려는 경우를 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-120">Suppose you want to see malware that was detected in email, and by what technology in Office 365.</span></span> <span data-ttu-id="958f7-121">이 작업을 수행 하려면 [전자 메일 > 맬웨어](threat-explorer-views.md#email--malware) 보기 탐색기를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-121">To do this, use the [Email > Malware](threat-explorer-views.md#email--malware) view of Explorer.</span></span>

1. <span data-ttu-id="958f7-122">[https://protection.office.com](https://protection.office.com)Office 365 Security & 준수 센터 ()에서 **Threat management** > **Explorer**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-122">In the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), choose **Threat management** > **Explorer**.</span></span>
2. <span data-ttu-id="958f7-123">**보기** 메뉴에서 **전자 메일** > **맬웨어**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-123">In the **View** menu, choose **Email** > **Malware**.</span></span><br/><span data-ttu-id="958f7-124">![탐색기에 대 한 보기 메뉴](media/ExplorerViewEmailMalwareMenu.png)</span><span class="sxs-lookup"><span data-stu-id="958f7-124">![View menu for Explorer](media/ExplorerViewEmailMalwareMenu.png)</span></span><br/>
3. <span data-ttu-id="958f7-125">**보낸 사람**을 클릭 한 다음 **기본** > **검색 기술을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-125">Click **Sender**, and then choose **Basic** > **Detection technology**.</span></span><br/><span data-ttu-id="958f7-126">이제 검색 기술을 보고서에 대 한 필터로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-126">Your detection technologies are now available as filters for the report.</span></span><br/><span data-ttu-id="958f7-127">![맬웨어 검색 기술](media/ExplorerEmailMalwareDetectionTech.png)</span><span class="sxs-lookup"><span data-stu-id="958f7-127">![Malware detection technologies](media/ExplorerEmailMalwareDetectionTech.png)</span></span><br/> 
4. <span data-ttu-id="958f7-128">옵션을 선택한 다음 새로 고침 단추를 클릭 하 여 해당 필터를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-128">Select an option, and then click the Refresh button to apply that filter.</span></span><br/>![선택한 검색 기술](media/ExplorerEmailMalwareDetectionTechATP.png)<br/> 

<span data-ttu-id="958f7-130">선택한 기술 옵션을 사용 하 여 전자 메일로 검색 된 결과 맬웨어가 표시 되도록 보고서가 새로 고쳐집니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-130">The report refreshes to show the results malware detected in email, using the technology option you selected.</span></span> <span data-ttu-id="958f7-131">여기서는 추가 분석을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-131">From here, you can conduct further analysis.</span></span>

## <a name="view-data-about-phishing-urls-and-click-verdict"></a><span data-ttu-id="958f7-132">피싱 url에 대 한 데이터를 확인 하 고 결과를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-132">View data about phishing URLs and click verdict</span></span>

<span data-ttu-id="958f7-133">허용, 차단 및 재정의 된 url 목록을 비롯 하 여 전자 메일의 url을 통한 피싱 시도를 확인 하려는 경우를 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-133">Suppose you want to see phishing attempts through URLs in email, including a list of URLs that were allowed, blocked, and overridden.</span></span> <span data-ttu-id="958f7-134">이 작업을 수행 하려면 [전자 메일 > 피싱](threat-explorer-views.md#email--phish) Explorer 보기를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-134">To do this, use the [Email > Phish](threat-explorer-views.md#email--phish) view of Explorer.</span></span>

1. <span data-ttu-id="958f7-135">[https://protection.office.com](https://protection.office.com)Office 365 Security & 준수 센터 ()에서 **Threat management** > **Explorer**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-135">In the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), choose **Threat management** > **Explorer**.</span></span>
2. <span data-ttu-id="958f7-136">**보기** 메뉴에서 **전자 메일** > **피싱**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-136">In the **View** menu, choose **Email** > **Phish**.</span></span><br/><span data-ttu-id="958f7-137">![탐색기에 대 한 보기 메뉴](media/ExplorerViewEmailPhishMenu.png)</span><span class="sxs-lookup"><span data-stu-id="958f7-137">![View menu for Explorer](media/ExplorerViewEmailPhishMenu.png)</span></span><br/>
3. <span data-ttu-id="958f7-138">**보낸 사람**을 클릭 한 다음 **url** > 을 선택 합니다**결과를 클릭**합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-138">Click **Sender**, and then choose **URLs** > **Click verdict**.</span></span>
4. <span data-ttu-id="958f7-139">**차단** 됨 및 **무시 된 블록과**같은 옵션을 하나 이상 선택 하 고 **새로 고침** 단추를 클릭 하 여 해당 필터를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-139">Select one or more options, such as **Blocked** and **Block overridden**, and then click the **Refresh** button to apply that filter.</span></span><br/><span data-ttu-id="958f7-140">![url을 선택 하 고 verdicts을 클릭 합니다.](media/ThreatExplorerEmailPhishClickVerdictOptions.png)</span><span class="sxs-lookup"><span data-stu-id="958f7-140">![URLs and click verdicts](media/ThreatExplorerEmailPhishClickVerdictOptions.png)</span></span><br/>

<span data-ttu-id="958f7-141">보고서가 새로 고쳐지고 전자 메일 배달 상태와 함께 차단 (또는 경고가 발생 하더라도 방문) 된 전자 메일에 검색 된 피싱 url이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-141">The report refreshes to show detected phishing URLs in email that were blocked (or visited despite a warning), along with email delivery status.</span></span> <span data-ttu-id="958f7-142">여기서는 추가 분석을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-142">From here, you can conduct further analysis.</span></span> <span data-ttu-id="958f7-143">예를 들어 차트 아래에서 조직의 전자 메일에서 차단 된 최상위 url을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-143">For example, below the chart, you can see the top URLs that were blocked in your organization's email.</span></span> 

![차단 된 탐색기 url](media/ExplorerPhishClickVerdictURLs.png) 

<span data-ttu-id="958f7-145">자세한 정보를 보려면 URL을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-145">Select a URL to view more detailed information.</span></span>

## <a name="review-email-messages-reported-by-users"></a><span data-ttu-id="958f7-146">사용자가 보고 한 전자 메일 메시지 검토</span><span class="sxs-lookup"><span data-stu-id="958f7-146">Review email messages reported by users</span></span>

<span data-ttu-id="958f7-147">조직의 사용자가 [outlook 및 웹용 outlook에 대 한 보고서 메시지 추가 기능](enable-the-report-message-add-in.md)을 사용 하 여 정크 메일 또는 피싱이 아닌 메시지를 보고 했다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-147">Suppose you want to see email messages that users in your organization have reported as Junk, Not Junk, or Phishing by using the [Report Message add-in for Outlook and Outlook on the web](enable-the-report-message-add-in.md).</span></span> <span data-ttu-id="958f7-148">이 작업을 수행 하려면 [전자 메일 > 사용자가 보고](threat-explorer-views.md#email--user-reported) 한 탐색기 보기를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-148">To do this, use the [Email > User-reported](threat-explorer-views.md#email--user-reported) view of Explorer.</span></span>

1. <span data-ttu-id="958f7-149">[https://protection.office.com](https://protection.office.com)Office 365 Security & 준수 센터 ()에서 **Threat management** > **Explorer**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-149">In the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), choose **Threat management** > **Explorer**.</span></span>
2. <span data-ttu-id="958f7-150">**보기** 메뉴에서**사용자가 보고 한** **전자 메일** > 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-150">In the **View** menu, choose **Email** > **User-reported**.</span></span><br/><span data-ttu-id="958f7-151">![탐색기에 대 한 보기 메뉴](media/ExplorerViewMenuEmailUserReported.png)</span><span class="sxs-lookup"><span data-stu-id="958f7-151">![View menu for Explorer](media/ExplorerViewMenuEmailUserReported.png)</span></span><br/>
3. <span data-ttu-id="958f7-152">**보낸 사람**을 클릭 한 다음 **기본** > **보고서 유형을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-152">Click **Sender**, and then choose **Basic** > **Report type**.</span></span>
4. <span data-ttu-id="958f7-153">**피싱**등의 옵션을 선택 하 고 **새로 고침** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-153">Select an option, such as **Phish**, and then click the **Refresh** button.</span></span> <br/><span data-ttu-id="958f7-154">![사용자가 보고 한 피싱](media/EmailUserReportedReportType.png)</span><span class="sxs-lookup"><span data-stu-id="958f7-154">![User-reported phish](media/EmailUserReportedReportType.png)</span></span><br/> 

<span data-ttu-id="958f7-155">보고서가 새로 고쳐지고 조직의 사용자가 피싱 시도로 보고 한 전자 메일 메시지에 대 한 데이터가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-155">The report refreshes to show data about email messages that people in your organization have reported as a phishing attempt.</span></span> <span data-ttu-id="958f7-156">이 정보를 사용 하 여 추가 분석을 수행 하 고, 필요한 경우 [ATP 피싱 방지 정책을](set-up-anti-phishing-policies.md)조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-156">You can use this information to conduct further analysis, and if necessary, adjust your [ATP anti-phishing policies](set-up-anti-phishing-policies.md).</span></span>

## <a name="theres-more"></a><span data-ttu-id="958f7-157">거기 더 있어!</span><span class="sxs-lookup"><span data-stu-id="958f7-157">There's more!</span></span>

<span data-ttu-id="958f7-158">이 문서에서 설명 하는 세 가지 시나리오 외에도 Explorer에서 사용할 수 있는 보고 시나리오가 많이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-158">In addition to the three scenarios outlined in this article, you have many reporting scenarios available with Explorer.</span></span> <span data-ttu-id="958f7-159">몇 가지 추가 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-159">Here are a few more examples:</span></span>

- [<span data-ttu-id="958f7-160">배달된 악성 전자 메일 찾기 및 조사</span><span class="sxs-lookup"><span data-stu-id="958f7-160">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)

- [<span data-ttu-id="958f7-161">SharePoint Online, OneDrive 및 Microsoft 팀에서 검색 된 악의적인 파일 보기</span><span class="sxs-lookup"><span data-stu-id="958f7-161">View malicious files detected in SharePoint Online, OneDrive, and Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)

- [<span data-ttu-id="958f7-162">위협 탐색기의 보기에 대 한 개요 가져오기</span><span class="sxs-lookup"><span data-stu-id="958f7-162">Get an overview of the views in Threat Explorer</span></span>](threat-explorer-views.md)

## <a name="how-to-get-explorer"></a><span data-ttu-id="958f7-163">탐색기를 가져오는 방법</span><span class="sxs-lookup"><span data-stu-id="958f7-163">How to get Explorer</span></span>

<span data-ttu-id="958f7-164">Explorer는 [Office 365 Advanced Threat Protection 계획 2](office-365-ti.md)에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-164">Explorer is included in [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md).</span></span> 

<span data-ttu-id="958f7-165">탐색기를 보고 사용 하려면 보안 관리자 또는 보안 판독기에 부여 된 것과 같은 적절 한 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-165">To view and use Explorer, you must have appropriate permissions, such as those granted to a security administrator or security reader.</span></span> 

- <span data-ttu-id="958f7-166">보안 &amp; 및 준수 센터에는 다음 역할 중 하나가 할당 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-166">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="958f7-167">조직 관리</span><span class="sxs-lookup"><span data-stu-id="958f7-167">Organization Management</span></span>
    - <span data-ttu-id="958f7-168">보안 관리자 (Azure Active Directory 관리 센터[https://aad.portal.azure.com](https://aad.portal.azure.com)에서 할당할 수 있음)</span><span class="sxs-lookup"><span data-stu-id="958f7-168">Security Administrator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com)))</span></span>
    - <span data-ttu-id="958f7-169">보안 독자</span><span class="sxs-lookup"><span data-stu-id="958f7-169">Security Reader</span></span>

- <span data-ttu-id="958f7-170">exchange online의 경우 exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) 또는 PowerShell cmdlet ( [exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조)에서 다음 역할 중 하나를 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="958f7-170">For Exchange Online, you must have one of the following roles assigned in either the Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) or with PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span></span>
    - <span data-ttu-id="958f7-171">조직 관리</span><span class="sxs-lookup"><span data-stu-id="958f7-171">Organization Management</span></span>
    - <span data-ttu-id="958f7-172">보기 전용 조직 관리</span><span class="sxs-lookup"><span data-stu-id="958f7-172">View-only Organization Management</span></span>
    - <span data-ttu-id="958f7-173">보기 권한만 있는 받는 사람 역할</span><span class="sxs-lookup"><span data-stu-id="958f7-173">View-Only Recipients role</span></span>
    - <span data-ttu-id="958f7-174">준수 관리</span><span class="sxs-lookup"><span data-stu-id="958f7-174">Compliance Management</span></span>

<span data-ttu-id="958f7-175">자세한 내용은 다음 리소스를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="958f7-175">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="958f7-176">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="958f7-176">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="958f7-177">Exchange Online의 기능 사용 권한</span><span class="sxs-lookup"><span data-stu-id="958f7-177">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
  
## <a name="related-topics"></a><span data-ttu-id="958f7-178">관련 항목</span><span class="sxs-lookup"><span data-stu-id="958f7-178">Related topics</span></span>

- [<span data-ttu-id="958f7-179">자동 조사 및 대응 (AIR)</span><span class="sxs-lookup"><span data-stu-id="958f7-179">Automated Investigation and Response (AIR)</span></span>](automated-investigation-response-office.md)

- [<span data-ttu-id="958f7-180">위협 탐색기 보기</span><span class="sxs-lookup"><span data-stu-id="958f7-180">Threat Explorer views</span></span>](threat-explorer-views.md)

- [<span data-ttu-id="958f7-181">Office 365 Advanced Threat Protection에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="958f7-181">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
