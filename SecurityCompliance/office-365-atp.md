---
title: Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/08/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
description: Office 365 Advanced Threat Protection에는 스푸핑 인텔리전스, 안전한 링크, 안전한 첨부 파일 및 고급 피싱 방지 기능이 포함되어 있습니다. Advanced Threat Protection은 SharePoint Online, 비즈니스용 OneDrive 및 Microsoft Teams 파일로도 확장됩니다.
ms.openlocfilehash: 6cdbdde2c91f8a9a77eb688ae27d509163da42a1
ms.sourcegitcommit: 03e64ead7805f3dfa9149252be8606efe50375df
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27769802"
---
# <a name="office-365-advanced-threat-protection"></a><span data-ttu-id="78fbc-104">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="78fbc-104">Office 365 Advanced Threat Protection</span></span>

## <a name="overview"></a><span data-ttu-id="78fbc-105">개요</span><span class="sxs-lookup"><span data-stu-id="78fbc-105">Overview</span></span>

<span data-ttu-id="78fbc-106">Office 365 ATP(Advanced Threat Protection)는 다음을 통해 악의적인 공격으로부터 조직을 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="78fbc-106">Office 365 Advanced Threat Protection (ATP) helps to protect your organization from malicious attacks by:</span></span>
  
- <span data-ttu-id="78fbc-107">[ATP 안전한 첨부 파일](atp-safe-attachments.md)로 맬웨어에 대해 전자 메일 첨부 파일 스캔</span><span class="sxs-lookup"><span data-stu-id="78fbc-107">Scanning email attachments for malware with [ATP Safe Attachments](atp-safe-attachments.md)</span></span>
    
- <span data-ttu-id="78fbc-108">[ATP 안전한 링크](atp-safe-links.md)로 전자 메일 메시지 및 Office 문서의 웹 주소(URL) 스캔</span><span class="sxs-lookup"><span data-stu-id="78fbc-108">Scanning web addresses (URLs) in email messages and Office documents with [ATP Safe Links](atp-safe-links.md)</span></span>
    
- <span data-ttu-id="78fbc-109">[SharePoint, OneDrive 및 Microsoft Teams에 대한 ATP](atp-for-spo-odb-and-teams.md)로 온라인 라이브러리의 악성 파일 식별 및 차단</span><span class="sxs-lookup"><span data-stu-id="78fbc-109">Identifying and blocking malicious files in online libraries with [ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md)</span></span>
    
- <span data-ttu-id="78fbc-110">[스푸핑 인텔리전스](learn-about-spoof-intelligence.md)로 권한이 없는 스푸핑에 대한 전자 메일 메시지 확인</span><span class="sxs-lookup"><span data-stu-id="78fbc-110">Checking email messages for unauthorized spoofing with [spoof intelligence](learn-about-spoof-intelligence.md)</span></span>
    
- <span data-ttu-id="78fbc-111">[Office 365의 ATP 피싱 방지 기능](atp-anti-phishing.md)으로 다른 사람이 사용자 및 조직의 사용자 지정 도메인을 대리 실행하려는 시도 감지</span><span class="sxs-lookup"><span data-stu-id="78fbc-111">Detecting when someone attempts to impersonate your users and your organization's custom domains with [ATP anti-phishing capabilities in Office 365](atp-anti-phishing.md)</span></span>
    
<span data-ttu-id="78fbc-p102">**Office 365 ATP를 통해 보호 조직의 보안 팀 안전한 링크, 안전한 첨부 파일 및 피싱 방지에 대 한 정의 하는 정책에 의해 결정 됩니다**. 업그레이드를 주기적으로 검토 하 고 최신 상태로 유지 하 고 서비스에 추가 되는 새로운 기능을 수행 하 여 정책 수정을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78fbc-p102">**Protection through Office 365 ATP is determined by policies that your organization's security team defines for Safe Links, Safe Attachments, and Anti-Phishing**. It's important to periodically review and revise your policies to keep them up to date and to take advantages of new features that are added to the service.</span></span> 

<span data-ttu-id="78fbc-p103">[보고서는 사용할 수](view-reports-for-atp.md) 조직에 대 한 ATP가 작동 하는 방법을 표시 합니다. 또한 이러한 보고서를 검토 하 고 정책에 업데이트할 필요할 영역을 보여줄 수 있습니다. 및 [분석을 위해 Microsoft에 파일을 전송할](#submit-a-suspicious-file-to-microsoft-for-analysis)수 있는 파일 또는 되지 않아야 하는 맬웨어를 검사 하는 Microsoft 구매할 것으로 표시 되는 파일을 설치한 경우.</span><span class="sxs-lookup"><span data-stu-id="78fbc-p103">[Reports are available](view-reports-for-atp.md) to show how ATP is working for your organization. These reports can also show you areas where you might need to review and update your policies. And, if you have files that are marked as malware that shouldn't be, or files you'd like Microsoft to examine, you can [submit a file to Microsoft for analysis](#submit-a-suspicious-file-to-microsoft-for-analysis).</span></span>

## <a name="new-features-are-continually-being-added-to-atp"></a><span data-ttu-id="78fbc-117">ATP에 계속 새로운 기능 추가</span><span class="sxs-lookup"><span data-stu-id="78fbc-117">New features are continually being added to ATP</span></span>

<span data-ttu-id="78fbc-p104">Office 365에 ATP가 포함된 새로운 기능을 계속 추가하고 있습니다. 다음은 몇 가지 새로운 기능의 목록으로, 일부 기능에서는 ATP 정책을 검토하고 업데이트합니다. ATP(또는 Microsoft 365)에 제공되는 새 기능에 대한 자세한 내용은 [Microsoft 365 로드맵](https://www.microsoft.com/microsoft-365/roadmap?filters=O365)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78fbc-p104">We are continuing to add new features to Office 365, and that includes ATP. Below is a list of several new features, some of which call for an ATP policy to be reviewed and updated. To learn more about new features coming to ATP (or Microsoft 365 in general), visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=O365).</span></span>


|<span data-ttu-id="78fbc-121">기능 업데이트</span><span class="sxs-lookup"><span data-stu-id="78fbc-121">Feature updates</span></span>  |<span data-ttu-id="78fbc-122">작업 항목</span><span class="sxs-lookup"><span data-stu-id="78fbc-122">Action items</span></span>  |
|---------|---------|
|<span data-ttu-id="78fbc-p105">2018년 10월과 이후 몇 개월에 걸쳐 사용자가 OWA(Outlook Web Application) 또는 Outlook을 사용할 때 ATP 안전한 링크에서 다시 작성한 URL이 아닌 원래 URL을 렌더링합니다. (이 기본 링크를 표시 유형이라고 합니다.)</span><span class="sxs-lookup"><span data-stu-id="78fbc-p105">Beginning in October 2018 and rolling out over the next several months, when people are using Outlook Web Application (OWA) or Outlook, ATP Safe Links renders original URLs, not rewritten URLs. (We call this native link visibility.)</span></span>|<span data-ttu-id="78fbc-125">없음</span><span class="sxs-lookup"><span data-stu-id="78fbc-125">None</span></span>         |
|<span data-ttu-id="78fbc-126">2018년 9월부터 [Office 365 ATP 경고 페이지](atp-safe-links-warning-pages.md)에 새 색 구성표, 자세한 내용 및 기존 경고 및 권장 사항에도 불구하고 사이트를 계속 유지하는 기능이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="78fbc-126">Beginning in September 2018, [Office 365 ATP warning pages](atp-safe-links-warning-pages.md) feature a new color scheme, more details, and the ability to continue to a site despite given warnings and recommendations.</span></span> |<span data-ttu-id="78fbc-127">없음</span><span class="sxs-lookup"><span data-stu-id="78fbc-127">None</span></span>         |
|<span data-ttu-id="78fbc-128">2018의 후반부에서 시작, ATP 안전한 링크 보호 Office Online (Word 온라인, Excel, PowerPoint 온라인 온라인과 OneNote 온라인) 및 Mac.에서 Office 365 ProPlus의 Url에 적용 하기 위해 확장</span><span class="sxs-lookup"><span data-stu-id="78fbc-128">Beginning in the second half of 2018, ATP Safe Links protection is extended to apply to URLs in Office Online (Word Online, Excel Online, PowerPoint Online, and OneNote Online) and Office 365 ProPlus on Mac.</span></span>   |[<span data-ttu-id="78fbc-129">검토 하 고 ATP 안전한 링크 정책 편집</span><span class="sxs-lookup"><span data-stu-id="78fbc-129">Review and edit your ATP Safe Links policies</span></span>](set-up-atp-safe-links-policies.md)  |
|<span data-ttu-id="78fbc-130">2018년 5월 말부터 보안 &amp; 규정 준수 센터의 [검역](quarantine-email-messages.md) 기능이 [SharePoint Online, 비즈니스용 OneDrive 및 Microsoft Teams 를 위한 ATP](atp-for-spo-odb-and-teams.md)로 확장됩니다.</span><span class="sxs-lookup"><span data-stu-id="78fbc-130">Beginning in late May 2018, [quarantine](quarantine-email-messages.md) capabilities in the Security &amp; Compliance Center are being extended to [ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams](atp-for-spo-odb-and-teams.md).</span></span> |[<span data-ttu-id="78fbc-131">검토 하 고 ATP 안전한 첨부 파일 정책 편집</span><span class="sxs-lookup"><span data-stu-id="78fbc-131">Review and edit your ATP Safe Attachments policies</span></span>](set-up-atp-safe-attachments-policies.md) |
|<span data-ttu-id="78fbc-132">년 3 월 2018 부터는 ATP 안전한 링크 보호 조직의 사용자 간에 보낸 전자 메일에 적용할까지 확장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78fbc-132">Beginning in March 2018, ATP Safe Links protection is extended to apply to email sent between people within an organization.</span></span> |[<span data-ttu-id="78fbc-133">검토 하 고 ATP 안전한 링크 정책 편집</span><span class="sxs-lookup"><span data-stu-id="78fbc-133">Review and edit your ATP Safe Links policies</span></span>](set-up-atp-safe-links-policies.md) |
|<span data-ttu-id="78fbc-134">가능한 가장 늦은 년 10 월 2017 부터는 ATP 안전한 링크 보호에 적용할 Url Url를 비롯 하 여 전자 메일에 Office 365 ProPlus 문서, Word, Excel, PowerPoint, Visio 등의 Office와 함께 Windows, iOS 및 Android 장치에서 앱까지 확장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78fbc-134">Beginning in late October 2017, ATP Safe Links protection is extended to apply to URLs in email as well as URLs in Office 365 ProPlus documents, such as Word, Excel, PowerPoint, and Visio on Windows, as well as Office apps on iOS and Android devices.</span></span>  |<span data-ttu-id="78fbc-135">[Office에 대 한 최신 인증](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) 을 사용 하는 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="78fbc-135">Make sure you're using [Modern Authentication for Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016)</span></span> |

      
## <a name="get-office-365-atp"></a><span data-ttu-id="78fbc-136">Office 365 ATP 받기</span><span class="sxs-lookup"><span data-stu-id="78fbc-136">Get Office 365 ATP</span></span>

<span data-ttu-id="78fbc-p106">Office 365 ATP 예: [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 비즈니스](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, 및 Office 365 교육 A5 구독에 포함 됩니다. 조직에 Office 365 ATP를 포함 하지 않는 한 Office 365 구독을 하는 경우에 추가 기능으로 ATP을 잠재적으로 구입할 수 있습니다. 자세한 내용은 [Office 365 고급 위협 Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="78fbc-p106">Office 365 ATP is included in subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, and Office 365 Education A5. If your organization has an Office 365 subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on. For more information, see [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span> 

## <a name="define-policies-for-atp"></a><span data-ttu-id="78fbc-140">ATP에 대한 정책 정의</span><span class="sxs-lookup"><span data-stu-id="78fbc-140">Define policies for ATP</span></span>

- <span data-ttu-id="78fbc-141">신뢰할 수 있는 사람 또는 도메인에서 온 것처럼 표시하는 전자 메일 메시지를 보내는 공격자로부터 보호하기 위한 가장 기반 공격을 포함하여 **[Office 365에서 ATP 피싱 방지 정책 설정](set-up-anti-phishing-policies.md)**</span><span class="sxs-lookup"><span data-stu-id="78fbc-141">**[Set up ATP anti-phishing policies in Office 365](set-up-anti-phishing-policies.md)** including impersonation-based attacks to protect against attackers who send email messages that appear to be from trusted people or domains</span></span> 

- <span data-ttu-id="78fbc-142">조직의 [차단한 URL 목록 사용자 지정](set-up-a-custom-blocked-urls-list-wtih-atp.md) 및 ["URL 다시 쓰지 않음" 목록 사용자 지정](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)을 포함하여 **[Office 365에서 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)**</span><span class="sxs-lookup"><span data-stu-id="78fbc-142">**[Set up ATP Safe Links policies in Office 365](set-up-atp-safe-links-policies.md)** including your organization's [custom blocked URLs list](set-up-a-custom-blocked-urls-list-wtih-atp.md) and [custom "Do not rewrite" URLs list](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)</span></span>
    
- <span data-ttu-id="78fbc-143">**[Office 365에서 ATP 안전한 첨부 파일 정책을 설정](set-up-atp-safe-attachments-policies.md)** 하 고 [동적 배달 하 고 미리 보는](dynamic-delivery-and-previewing.md) 등의 여러 옵션 중에서 선택</span><span class="sxs-lookup"><span data-stu-id="78fbc-143">**[Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md)** and choose from several options, such as [Dynamic Delivery and previewing](dynamic-delivery-and-previewing.md)</span></span>
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a><span data-ttu-id="78fbc-144">보고서를 확인하여 ATP 작동 방식 보기</span><span class="sxs-lookup"><span data-stu-id="78fbc-144">See how ATP is working by viewing reports</span></span>

<span data-ttu-id="78fbc-145">ATP 정책이 적용된 후에는 서비스 작동 방식을 표시하는 보고서를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78fbc-145">After your ATP policies are in place, reports are available to show how the service is working.</span></span>

<span data-ttu-id="78fbc-146">[![보안&amp; 규정 준수 센터 대시보드는 Advanced Threat Protection이 작업 중인 위치를 확인할 수 있도록 도와줍니다](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)</span><span class="sxs-lookup"><span data-stu-id="78fbc-146">[![The Security &amp; Compliance Center dashboard can help you see where Advanced Threat Protection is working](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)</span></span>
  
1. <span data-ttu-id="78fbc-p107">Office 365 전역 관리자, 보안 관리자 또는 보안 독자인지 확인합니다 ([Office 365 보안 &amp; 규정 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)을 참조하세요.)</span><span class="sxs-lookup"><span data-stu-id="78fbc-p107">Make sure that you are an Office 365 global administrator, security administrator, or security reader. (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).)</span></span>
    
2. <span data-ttu-id="78fbc-149">[Advanced Threat Protection 보고서를 봅니다](view-reports-for-atp.md).</span><span class="sxs-lookup"><span data-stu-id="78fbc-149">[View reports for Advanced Threat Protection](view-reports-for-atp.md).</span></span>
    
3. <span data-ttu-id="78fbc-p108">필요에 따라 보안 정책을 조정합니다. 다음 리소스를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78fbc-p108">If needed, make adjustments to your security policies. See the following resources:</span></span>
      - [<span data-ttu-id="78fbc-152">Office 365 ATP 피싱 방지 정책</span><span class="sxs-lookup"><span data-stu-id="78fbc-152">ATP anti-phishing policies in Office 365</span></span>](set-up-anti-phishing-policies.md)
      - [<span data-ttu-id="78fbc-153">Office 365 ATP 안전한 링크 정책</span><span class="sxs-lookup"><span data-stu-id="78fbc-153">ATP Safe Links policies in Office 365</span></span>](set-up-atp-safe-links-policies.md)
      - [<span data-ttu-id="78fbc-154">Office 365 ATP 안전한 첨부 파일 정책</span><span class="sxs-lookup"><span data-stu-id="78fbc-154">ATP Safe Attachments policies in Office 365</span></span>](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a><span data-ttu-id="78fbc-155">분석을 위해 Microsoft에 의심스러운 파일 제출</span><span class="sxs-lookup"><span data-stu-id="78fbc-155">Submit a suspicious file to Microsoft for analysis</span></span>

- <span data-ttu-id="78fbc-p109">맬웨어라고 의심되는 파일을 가져온 경우 분석을 위해 해당 파일을 Microsoft에 제출할 수 있습니다. [Windows Defender 보안 인텔리전스 제출 포털](https://go.microsoft.com/fwlink/?linkid=857185)을 방문합니다.</span><span class="sxs-lookup"><span data-stu-id="78fbc-p109">If you get a file that you suspect could be malware, you can submit that file to Microsoft for analysis. Visit the [Windows Defender Security Intelligence submission portal](https://go.microsoft.com/fwlink/?linkid=857185).</span></span>

- <span data-ttu-id="78fbc-158">분석을 위해 Microsoft에 제출하려는 전자 메일 메시지(첨부 파일 포함 또는 제외)가 있는 경우 [보고서 메시지 추가 기능](enable-the-report-message-add-in.md)을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78fbc-158">If you get an email message (with or without an attachment) that you'd like to submit to Microsoft for analysis, use the [Report Message add-in](enable-the-report-message-add-in.md).</span></span> 
  

