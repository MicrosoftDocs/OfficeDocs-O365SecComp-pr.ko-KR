---
title: 보고서 메시지 추가 기능을 사용하도록 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/19/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
description: Outlook 및 Outlook에서 개별 사용자에 대 한 웹 또는 전체 조직에 대 한 보고서 메시지 추가 기능을 사용 하는 방법에 알아봅니다.
ms.openlocfilehash: f35899d3f0be9ee07cb6dae5c5fec40395948340
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706372"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="16bc2-103">보고서 메시지 추가 기능을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="16bc2-103">Enable the Report Message add-in</span></span>

## <a name="overview"></a><span data-ttu-id="16bc2-104">개요</span><span class="sxs-lookup"><span data-stu-id="16bc2-104">Overview</span></span>

<span data-ttu-id="16bc2-p101">보고서 메시지에서 추가 기능 Outlook 웹에서 Outlook에 대 한 사람들이 쉽게 misclassified 전자 메일 안전 또는 악의적인, 여부를 보고 Microsoft 및 그 계열사 분석을 위해 수 있도록 합니다. Microsoft의 전자 메일 보호 기술 효율성을 향상 시키기 위해 이러한 제출을 사용 합니다. 또한 사용자 조직에서 [Office 365 고급 위협 보호](office-365-atp.md) 또는 [Office 365 위협 인텔리전스](office-365-ti.md)를 사용 하는 경우 보고서 메시지에서 추가 기능을 제공 유용한 정보를 검토 하 여 업데이트를 사용할 수 있는 조직의 보안 팀 보안 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-p101">The Report Message add-in for Outlook and Outlook on the Web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis. Microsoft uses these submissions to improve the effectiveness of email protection technologies. In addition, if your organization is using [Office 365 Advanced Threat Protection](office-365-atp.md) or [Office 365 Threat Intelligence](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span> 

<span data-ttu-id="16bc2-p102">등 사용자가 피싱으로 많은 메시지를 보고 하는 것으로 가정 합니다. 이 정보는 [보안 대시보드](security-dashboard.md) 및 기타 보고서에서 월등 합니다. 조직의 보안 팀이이 정보를 사용 하 여 피싱 방지 정책 업데이트 해야할 수도 있음을으로 수 있습니다. 또는 사용자는 많은 보고서 메시지 추가 기능을 사용 하 여 정크 메일 아님으로 정크 메일으로 플래그가 지정 된 메시지를 보고, 조직의 보안 팀 [스팸 방지 정책](configure-the-anti-spam-policies.md)을 조정 하려면 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-p102">For example, suppose that people are reporting a lot of messages as phishing. This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports. Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated. Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span> 

<span data-ttu-id="16bc2-112">보고서 메시지 추가 기능에서 Office 365 구독 및 다음 제품 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-112">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="16bc2-113">웹에 있는 outlook</span><span class="sxs-lookup"><span data-stu-id="16bc2-113">Outlook on the Web</span></span>
 - <span data-ttu-id="16bc2-114">Outlook 2013 s p 1</span><span class="sxs-lookup"><span data-stu-id="16bc2-114">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="16bc2-115">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16bc2-115">Outlook 2016</span></span>
 - <span data-ttu-id="16bc2-116">Mac용 Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16bc2-116">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="16bc2-117">Office 365 ProPlus에 포함 된 outlook</span><span class="sxs-lookup"><span data-stu-id="16bc2-117">Outlook included with Office 365 ProPlus</span></span>
  
<span data-ttu-id="16bc2-118">개별 사용자 인 경우에 [자신에 대 한 보고서 메시지 추가 기능을 사용](#get-the-report-message-add-in-for-yourself)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-118">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span> 
  
<span data-ttu-id="16bc2-p103">Office 365 전역 관리자 또는 Exchange Online 관리자, 자신이 Exchange OAuth 인증을 사용 하도록 구성 된 경우에 [조직에 대 한 보고서 메시지 추가 기능을 사용](#get-and-enable-the-report-message-add-in-for-your-organization)할 수 있습니다. 보고서 메시지 추가 기능에 [중앙 집중화 배포](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins)를 통해 사용할 수 있는 이제 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-p103">If you're an Office 365 global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization). The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>
    
## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="16bc2-121">메시지가 표시 되는 보고서 추가 기능에서 자신에 대 한</span><span class="sxs-lookup"><span data-stu-id="16bc2-121">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="16bc2-122">[Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps) [보고서 메시지 추가 기능에](https://appsource.microsoft.com/product/office/wa104381180)대 한 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-122">In [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), search for the [Report Message add-in](https://appsource.microsoft.com/product/office/wa104381180).</span></span>
    
2. <span data-ttu-id="16bc2-123">선택 **가져올 이제 IT**합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-123">Choose **GET IT NOW**.</span></span><br/><span data-ttu-id="16bc2-124">![메시지를 보고-지금 신청](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="16bc2-124">![Report Message - Get It Now](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
3. <span data-ttu-id="16bc2-p104">사용 및 개인정보 보호 정책 약관을 검토 합니다. 다음 **계속**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-p104">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
4. <span data-ttu-id="16bc2-127">진행 중인 작업 또는 학교 계정 (업무용) 또는 Microsoft 계정 (개인용)를 사용 하 여 Office 365 전자 메일에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-127">Sign in to your Office 365 email using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>
    
<span data-ttu-id="16bc2-128">추가 기능에 설치 및 활성화, 후 다음과 같은 아이콘이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-128">After the add-in is installed and enabled, you'll see the following icons:</span></span> 

- <span data-ttu-id="16bc2-129">Outlook에서 아이콘은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-129">In Outlook the icon looks like this:</span></span> <br/> ![Outlook에 대 한 보고서에서 메시지 추가 아이콘](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="16bc2-131">Outlook Web App에서 아이콘은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-131">In Outlook Web App the icon looks like this:</span></span><br/>![Outlook에서 웹 보고서 메시지 추가 아이콘](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

<span data-ttu-id="16bc2-133">다음 단계에 대해 알아봅니다 [보고서 메시지 추가 기능을 사용](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-133">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="16bc2-134">조직에 대 한 보고서 메시지 추가 기능을 사용 하 고 확인</span><span class="sxs-lookup"><span data-stu-id="16bc2-134">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="16bc2-p105">이 작업을 완료 하려면 Office 365 전역 관리자 또는 Exchange Online 관리자 여야 합니다. 또한 Exchange 자세한 내용은 [Exchange 요구 사항 (추가 기능 배포에 집중)를](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements)참조 하십시오 OAuth 인증을 사용 하도록 구성 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-p105">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task. In addition, Exchange must be configured to use OAuth authentication To learn more, see [Exchange requirements (Centralized Deployment of add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span></span> 

1. <span data-ttu-id="16bc2-137">[서비스 및 추가 기능 페이지에서](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) 에서 새 Microsoft 365 관리 센터로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-137">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the new Microsoft 365 admin center.</span></span><br/><span data-ttu-id="16bc2-138">![새 Microsoft 365 관리 센터에서 서비스 및 추가 기능 페이지](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="16bc2-138">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/> 
    
2. <span data-ttu-id="16bc2-139">**+ 추가 기능 배포**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-139">Choose **+ Deploy Add-in**.</span></span><br/><span data-ttu-id="16bc2-140">![선택 추가 기능 배포](media/ServicesAddIns-ChooseDeployAddIn.png)</span><span class="sxs-lookup"><span data-stu-id="16bc2-140">![Choose Deploy Add-In](media/ServicesAddIns-ChooseDeployAddIn.png)</span></span><br/> 
    
3. <span data-ttu-id="16bc2-141">새 추가 기능에 화면에서 정보를 검토 하 고 \*\*\*\* 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-141">In the New Add-In screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="16bc2-142">![새 추가 기능에서 세부 정보](media/NewAddInScreen1.png)</span><span class="sxs-lookup"><span data-stu-id="16bc2-142">![New Add-In details](media/NewAddInScreen1.png)</span></span><br/>
    
4. <span data-ttu-id="16bc2-143">**Office 스토어에서 추가 기능을 추가 하려고 하는 경우**선택 하 고 \*\*\*\* 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-143">Select **I want to add an Add-In from the Office Store**, and then choose **Next**.</span></span><br/><span data-ttu-id="16bc2-144">![새 추가 기능을 추가 하려는 경우](media/NewAddInScreen2.png)</span><span class="sxs-lookup"><span data-stu-id="16bc2-144">![I want to add an new Add-In](media/NewAddInScreen2.png)</span></span><br/> 
    
5. <span data-ttu-id="16bc2-145">검색 보고서 메시지에 대 한 및 결과 얻으려면 옆에 있는 보고서 메시지에서 추가 기능 목록에서 추가 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-145">Search for Report Message, and in the list of results, next to the Report Message Add-In, choose Add.</span></span><br/>![보고서 메시지를 검색 하 고 추가 선택 합니다](media/NewAddInScreen3.png)<br/>
    
6. <span data-ttu-id="16bc2-147">보고서 메시지 화면에서 정보를 검토 하 고 \*\*\*\* 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-147">On the Report Message screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="16bc2-148">![메시지 세부 정보를 보고 합니다.](media/ReportMessageAdd-InNewScreen4.png)</span><span class="sxs-lookup"><span data-stu-id="16bc2-148">![Report Message details](media/ReportMessageAdd-InNewScreen4.png)</span></span><br/>

7. <span data-ttu-id="16bc2-149">Outlook에 대 한 사용자 기본 설정을 지정 하 고 \*\*\*\* 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-149">Specify the user default settings for Outlook, and  then choose **Next**.</span></span><br/><span data-ttu-id="16bc2-150">![Outlook에 대 한 기본 설정을 메시지를 보고 합니다.](media/ReportMessageOptionsScreen5.png)</span><span class="sxs-lookup"><span data-stu-id="16bc2-150">![Report Message default settings for Outlook](media/ReportMessageOptionsScreen5.png)</span></span><br/>

8. <span data-ttu-id="16bc2-151">보고서 메시지에서 추가 기능, 누가 지정 하 고 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-151">Specify who gets the Report Message Add-in, and then choose **Save**.</span></span> <br/><span data-ttu-id="16bc2-152">![인원 보고서 메시지의 추가 기능](media/ReportMessageOptionsScreen6.png)</span><span class="sxs-lookup"><span data-stu-id="16bc2-152">![Who gets the Report Message add-in](media/ReportMessageOptionsScreen6.png)</span></span><br/>

> [!TIP]
> <span data-ttu-id="16bc2-153">[사용자가 보고 하는 전자 메일 메시지의 복사본을 가져오시겠습니까 규칙 설정](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users) 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-153">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)</span></span>

<span data-ttu-id="16bc2-p106">어떤 사용자가 선택한 마법사를 사용 하 여를 따라 조직의 사용자는 [보고서 메시지 추가 기능에서](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) 사용할 수 있는 갖습니다. 조직의 사용자는 다음과 같은 아이콘이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-p106">Depending on what you selected using the wizard, people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available. People in your organization will see the following icons:</span></span> 

- <span data-ttu-id="16bc2-156">Outlook에서 아이콘은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-156">In Outlook the icon looks like this:</span></span> <br/> ![Outlook에 대 한 보고서에서 메시지 추가 아이콘](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="16bc2-158">Outlook Web App에서 아이콘은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-158">In Outlook Web App the icon looks like this:</span></span><br/>![Outlook에서 웹 보고서 메시지 추가 아이콘](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="16bc2-160">사용자가 보고 하는 전자 메일 메시지의 복사본을 가져오시겠습니까 규칙을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-160">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="16bc2-161">이 작업을 수행 하려면 Exchange Online 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-161">You must be an Exchange Online Administrator to perform this task.</span></span>
  
<span data-ttu-id="16bc2-p107">조직에서 사용자가 보고 하는 전자 메일 메시지의 복사본을 가져오시겠습니까 규칙을 설정할 수 있습니다. 다운로드 하 고 조직에 대 한 보고서 메시지 추가 기능을 활성화 한 후이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-p107">You can set up a rule to get a copy of email messages reported by users in your organization. You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>
  
1. <span data-ttu-id="16bc2-164">Exchange 관리 센터에서 **메일 흐름** 선택 \> **규칙**입니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-164">In the Exchange Admin Center, choose **mail flow** \> **rules**.</span></span> 
    
2. <span data-ttu-id="16bc2-165">선택 **+** \> **새 규칙 만들기**.</span><span class="sxs-lookup"><span data-stu-id="16bc2-165">Choose **+** \> **Create a new rule**.</span></span> 
    
3. <span data-ttu-id="16bc2-166">**이름** 상자에 제출 등의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-166">In the **Name** box, type a name, such as Submissions.</span></span>
    
4. <span data-ttu-id="16bc2-167">**이 규칙 적용 대상** 목록에서 **받는 사람 주소... 포함**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-167">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span> 
    
5. <span data-ttu-id="16bc2-168">**단어 또는 구 지정** 화면에서 추가 `junk@office365.microsoft.com` 및 `phish@office365.microsoft.com`을 선택한 다음 **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-168">In the **specify words or phrases** screen, add `junk@office365.microsoft.com` and `phish@office365.microsoft.com`, and then choose **OK**.</span></span><br/><span data-ttu-id="16bc2-169">![규칙에 대 한 정크 및 phish 전자 메일 주소를 지정 합니다.](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span><span class="sxs-lookup"><span data-stu-id="16bc2-169">![Specify the junk and phish email addresses for the rule](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span></span><br/>
  
6. <span data-ttu-id="16bc2-170">**다음 작업을 수행...** 목록에서 선택 **숨은 참조 메시지를...** 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-170">In the **Do the following...** list, choose **Bcc the message to...**.</span></span> 
    
7. <span data-ttu-id="16bc2-171">전역 관리자, 보안 관리자 및/또는 사용자를 Microsoft에 보고 하는 각 전자 메일 메시지의 복사본을 받고 다음 **확인**을 선택 해야 보안 읽기 권한자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-171">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span><br/><span data-ttu-id="16bc2-172">![보고 된 각 메시지의 복사본을 수신 하도록 글로벌 또는 보안 관리자 추가](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span><span class="sxs-lookup"><span data-stu-id="16bc2-172">![Add a global or security administrator to receive a copy of each reported message](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span></span><br/>
  
8. <span data-ttu-id="16bc2-173">**감사 심각도 수준으로이 규칙**선택 하 고 **미디어**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-173">Select **Audit this rule with severity level**, and choose **Medium**.</span></span> 
    
9. <span data-ttu-id="16bc2-174">**선택이 규칙에 대 한 모드** **적용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-174">Under **Choose a mode for this rule**, choose **Enforce**.</span></span><br/><span data-ttu-id="16bc2-175">![보고 된 각 메시지의 복사본을 가져오시겠습니까 규칙을 설정 합니다.](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span><span class="sxs-lookup"><span data-stu-id="16bc2-175">![Set up a rule to get a copy of each reported message](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span></span><br/>
  
10. <span data-ttu-id="16bc2-176">**Save(저장)** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-176">Choose **Save**.</span></span> 
    
<span data-ttu-id="16bc2-p108">현재 위치에서이 규칙을 사용할 경우 보고서 메시지에서 추가 기능을 사용 하 여 전자 메일 메시지를 보고 하는 다른 사용자가 조직에서 때마다에 전역 관리자, 보안 관리자 및/또는 보안 판독기 복사본을 받게 됩니다 해당 메시지의 합니다. 이 정보를 사용 하면 설정 또는 정책, 예: [Office 365 ATP 안전한 링크](atp-safe-links.md) 정책 조정 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-p108">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message. This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies.</span></span> 

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="16bc2-179">검토 또는 보고서 메시지 추가 기능에 대 한 설정 편집</span><span class="sxs-lookup"><span data-stu-id="16bc2-179">Review or edit settings for the Report Message add-in</span></span>

<span data-ttu-id="16bc2-180">검토 수 있으며는 보고서 메시지 추가 기능에 대 한 [서비스 및 추가 기능 페이지](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns)에서 기본 설정을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-180">You can review and edit the default settings for the Report Message Add-In in the [Services & Add-Ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="16bc2-181">이 작업을 완료 하려면 Office 365 전역 관리자 또는 Exchange Online 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-181">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>
    
1. <span data-ttu-id="16bc2-182">[서비스 및 추가 기능 페이지에서](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) 에서 새 Microsoft 365 관리 센터로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-182">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the new Microsoft 365 admin center.</span></span><br/><span data-ttu-id="16bc2-183">![새 Microsoft 365 관리 센터에서 서비스 및 추가 기능 페이지](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="16bc2-183">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/>

2. <span data-ttu-id="16bc2-184">찾기 및 보고서 메시지에서 추가 기능을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-184">Find and select the Report Message Add-In.</span></span><br/>![보고서 메시지 추가 기능을 선택 하 고 찾기](media/FindReportMessageAddIn.png)<br/> 
    
3. <span data-ttu-id="16bc2-186">보고서 메시지 화면을 검토 하 고 조직에 적절 하 게 설정 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-186">On the Report Message screen, review and edit settings as appropriate for your organization.</span></span><br/>![보고서 메시지 추가 기능에 대 한 설정](media/EditReportMessageAddIn.png)<br/> 

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="16bc2-188">보고서 메시지 추가 기능을 사용 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc2-188">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="16bc2-189">[보고서 메시지에서 추가 기능 사용](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="16bc2-189">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="16bc2-190">관련 항목</span><span class="sxs-lookup"><span data-stu-id="16bc2-190">Related topics</span></span>

[<span data-ttu-id="16bc2-191">보고서 메시지 추가 기능을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="16bc2-191">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[<span data-ttu-id="16bc2-192">보안에서 전자 메일 보안 보고서를 보려면 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="16bc2-192">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="16bc2-193">Office 365 고급 위협 보호에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="16bc2-193">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="16bc2-194">탐색기를 사용 하 여 보안에서 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="16bc2-194">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
  

