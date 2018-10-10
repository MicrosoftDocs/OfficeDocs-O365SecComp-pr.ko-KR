---
title: Office 365 ATP 안전한 첨부 정책 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 078eb946-819a-4e13-8673-fe0c0ad3a775
description: 조직에서 전자 메일의 악의적인 파일 보호 하기 위해 안전한 첨부 파일 정책을 정의 합니다.
ms.openlocfilehash: c57f9320c7cd2b8b75bc2dc58d1f72ce136acbb6
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454285"
---
# <a name="set-up-office-365-atp-safe-attachments-policies"></a><span data-ttu-id="d754a-103">Office 365 ATP 안전한 첨부 정책 설정</span><span class="sxs-lookup"><span data-stu-id="d754a-103">Set up Office 365 ATP Safe Attachments policies</span></span>

<span data-ttu-id="d754a-p101">사용자가 정기적으로 보내기, 수신, 및 문서, 프레젠테이션, 스프레드시트, 등의 첨부 파일을 공유 합니다. 항상 쉽게 첨부 파일이 안전 또는 악의적인 전자 메일 메시지를 확인 하 여 방금 인지 여부를 알 수 있는 것은 아닙니다. 하며 원하는 마지막으로 성능을 저하 시키는 조직에 대 한 프로그램을 통과해 서, 악의적인 첨부 파일입니다. 놓기만 [Office 365 고급 위협 보호](office-365-atp.md) (ATP) 데 도움이 됩니다. 조직은 저작권법과 공격 으로부터 안전 하지 않은 전자 메일 첨부 파일을 보장 하기 [ATP 안전한 첨부 파일](atp-safe-attachments.md) 정책을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-p101">People regularly send, receive, and share attachments, such as documents, presentations, spreadsheets, and more. It's not always easy to tell whether an attachment is safe or malicious just by looking at an email message. And the last thing you want is a malicious attachment to get through, wreaking havoc for your organization. Fortunately, [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) can help. You can set up [ATP Safe Attachments](atp-safe-attachments.md) policies to help ensure that your organization is protected against attacks by unsafe email attachments.</span></span> 
  
## <a name="what-to-do"></a><span data-ttu-id="d754a-109">수행할 작업</span><span class="sxs-lookup"><span data-stu-id="d754a-109">What to do</span></span> 
  
1. [<span data-ttu-id="d754a-110">필수 구성 요소를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-110">Review the prerequisites</span></span>](#review-the-prerequisites)
    
2. [<span data-ttu-id="d754a-111">ATP 안전한 첨부 파일 정책 설정</span><span class="sxs-lookup"><span data-stu-id="d754a-111">Set up an ATP Safe Attachments policy</span></span>](#set-up-an-atp-safe-attachments-policy)
    
3. [<span data-ttu-id="d754a-112">ATP 안전한 첨부 파일 정책 옵션에 알아보기</span><span class="sxs-lookup"><span data-stu-id="d754a-112">Learn about ATP Safe Attachments policy options</span></span>](#learn-about-atp-safe-attachments-policy-options)
    
## <a name="step-1-review-the-prerequisites"></a><span data-ttu-id="d754a-113">1 단계: 필수 구성 요소를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-113">Step 1: Review the prerequisites</span></span>

- <span data-ttu-id="d754a-114">조직에 [Office 365 고급 위협 보호](office-365-atp.md)있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-114">Make sure that your organization has [Office 365 Advanced Threat Protection](office-365-atp.md).</span></span>
    
- <span data-ttu-id="d754a-115">필요한 되어있는지 확인 [Office 365 보안에 할당 된 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-115">Make sure that you have the necessary [permissions assigned in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    
- <span data-ttu-id="d754a-p102">[ATP 안전한 첨부 파일 정책 옵션에 대 한 설명](#learn-about-atp-safe-attachments-policy-options) (이 문서의). 모니터] 또는 [바꾸기 옵션 등의 일부 옵션 첨부 파일 검사 하는 동안 전자 메일의 약간 지연 될 수 있습니다. 메시지 지연을 방지 하려면 [동적 배달 및 미리 보기](dynamic-delivery-and-previewing.md)를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-p102">[Learn about ATP Safe Attachments policy options](#learn-about-atp-safe-attachments-policy-options) (in this article). Some options, such as the Monitor or Replace options, can result in a minor delay of email while attachments are scanned. To avoid message delays, consider using [dynamic delivery and previewing](dynamic-delivery-and-previewing.md).</span></span>
    
- <span data-ttu-id="d754a-119">모든 Office 365 데이터 센터에 분산 하 여 신규 또는 업데이트 된 정책에 대 한 최대 30 분을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-119">Allow up to 30 minutes for your new or updated policy to spread to all Office 365 datacenters.</span></span>
    
## <a name="step-2-set-up-or-edit-an-atp-safe-attachments-policy"></a><span data-ttu-id="d754a-120">2 단계: 설정 (또는 편집) ATP 안전한 첨부 파일 정책</span><span class="sxs-lookup"><span data-stu-id="d754a-120">Step 2: Set up (or edit) an ATP Safe Attachments policy</span></span>
  
1. <span data-ttu-id="d754a-121">전역 관리자 또는 보안 관리자로 이동 [https://protection.office.com](https://protection.office.com) 와 작업이 나 교육용 계정 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-121">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="d754a-122">Office 365 보안에서 &amp; 준수 센터 왼쪽된 탐색 창의 **위협 관리** **정책** 을 선택 \> **안전한 첨부 파일**입니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-122">In the Office 365 Security &amp; Compliance Center, in the left navigation pane, under **Threat management**, choose **Policy** \> **Safe Attachments**.</span></span>
    
3. <span data-ttu-id="d754a-p103">**SharePoint, OneDrive 및 Microsoft 팀의 ATP를 설정**하는 것이 표시를 하는 경우에이 옵션을 선택 하는 것이 좋습니다. 이렇게 하면 Office 365 환경에 대 한 [SharePoint, OneDrive 및 팀이 Microsoft Office 365 고급 위협 보호](atp-for-spo-odb-and-teams.md) 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-p103">If you see **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**, we recommend that you select this option. This will enable [Office 365 Advanced Threat Protection for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) for your Office 365 environment.</span></span> 
    
4. <span data-ttu-id="d754a-125">**새로 만들기** 를 선택 (새로 만들기 단추 유사한 더하기 기호 ( **+**)) 정책 만들기를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-125">Choose **New** (the New button resembles a plus sign ( **+**)) to start creating your policy.</span></span>
    
5. <span data-ttu-id="d754a-126">이름, 설명 및 정책에 대 한 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-126">Specify the name, description, and settings for the policy.</span></span>
    
    <span data-ttu-id="d754a-127">**예제:** 모든 사람의 메시지를 즉시 배달 하 고 검사는 자신이 후 첨부 파일을 다음가 다시 연결 하는 "지연 없음" 이라는 정책을 설정 하려면 다음 설정을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-127">**Example:** To set up a policy called "no delays" that delivers everyone's messages immediately and then reattaches attachments after they're scanned, you might specify the following settings:</span></span> 
    
      - <span data-ttu-id="d754a-128">**이름** 상자에 없는 지연을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-128">In the **Name** box, type no delays.</span></span>
    
      - <span data-ttu-id="d754a-129">**설명** 상자에 검색 한 후 바로 제공 메시지와 첨부 파일이 다시 연결 같은 대 한 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-129">In the **Description** box, type a description like, Delivers messages immediately and reattaches attachments after scanning.</span></span>
    
      - <span data-ttu-id="d754a-p104">응답 섹션에서 **동적 배달** 옵션을 선택 합니다. ([동적 배달 하 고 ATP 안전한 첨부 파일 미리 보기에 대해 자세히 알아보십시오](dynamic-delivery-and-previewing.md).)</span><span class="sxs-lookup"><span data-stu-id="d754a-p104">In the response section, choose the **Dynamic Delivery** option. ([Learn more about dynamic delivery and previewing with ATP Safe Attachments](dynamic-delivery-and-previewing.md).)</span></span>
    
      - <span data-ttu-id="d754a-132">**리디렉션 첨부 파일** 섹션에서 리디렉션을 사용 하도록 설정 하 고 Office 365 전역 관리자, 보안 관리자 또는 보안 분석가 악의적인 첨부 파일을 조사 하는 사용자의 전자 메일 주소를 입력 하는 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-132">In the **Redirect attachment** section, select the option to enable redirect and type the email address of your Office 365 global administrator, security administrator, or security analyst who will investigate malicious attachments.</span></span> 
    
      - <span data-ttu-id="d754a-p105">**적용 된** 섹션에서 **받는 사람 도메인은**선택 하 고 도메인을 선택 합니다. **추가**선택 하 고 **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-p105">In the **Applied To** section, choose **The recipient domain is**, and then select your domain. Choose **Add**, and then choose **OK**.</span></span>
    
6. <span data-ttu-id="d754a-135">**저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-135">Choose **Save**.</span></span>
    
<span data-ttu-id="d754a-p106">조직에 대 한 여러 ATP 안전한 첨부 파일 정책 설정을 것이 좋습니다. 이러한 정책은 **ATP 안전한 첨부 파일** 페이지에 나열 된 순서 대로 적용 됩니다. 정책을 정의 했거나 편집한 후 허용에 대 한 최소 30 분의 전체 Microsoft 데이터 센터에서 적용 하려면 정책을 합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-p106">Consider setting up multiple ATP Safe Attachments policies for your organization. These policies will be applied in the order they're listed on the **ATP Safe Attachments** page. After a policy has been defined or edited, allow at least 30 minutes for the polices to take effect throughout Microsoft datacenters.</span></span> 
  
## <a name="step-3-learn-about-atp-safe-attachments-policy-options"></a><span data-ttu-id="d754a-139">3 단계: ATP 안전한 첨부 파일 정책 옵션에 알아보기</span><span class="sxs-lookup"><span data-stu-id="d754a-139">Step 3: Learn about ATP Safe Attachments policy options</span></span>

<span data-ttu-id="d754a-p107">ATP 안전한 첨부 파일 정책에 설정 하면 모니터, 차단, 바꾸기, 동적 배달 및 등을 비롯 한 여러 옵션 중에서 선택 합니다. 이러한 옵션 기능을 수행 하는 방법에 대 한 궁금할 하는 경우 다음 표에 각 하 고 영향을 주기 합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-p107">As you set up your ATP Safe Attachments policies, you choose from among many options, including Monitor, Block, Replace, Dynamic Delivery, and so on. In case you're wondering about what these options do, the following table summarizes each and its effect.</span></span>
  
|<span data-ttu-id="d754a-142">**옵션**</span><span class="sxs-lookup"><span data-stu-id="d754a-142">**Option**</span></span>|<span data-ttu-id="d754a-143">**영향**</span><span class="sxs-lookup"><span data-stu-id="d754a-143">**Effect**</span></span>|<span data-ttu-id="d754a-144">**사용 하려는 경우:**</span><span class="sxs-lookup"><span data-stu-id="d754a-144">**Use when you want to:**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d754a-145">**Off**</span><span class="sxs-lookup"><span data-stu-id="d754a-145">**Off**</span></span> <br/> |<span data-ttu-id="d754a-146">맬웨어에 대 한 첨부 파일을 검색 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-146">Does not scan attachments for malware</span></span>  <br/> <span data-ttu-id="d754a-147">메시지 배달이 연기 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-147">Does not delay message delivery</span></span>  <br/> |<span data-ttu-id="d754a-148">내부 보낸사람, 스캐너, 팩스, 또는 알려진, 좋은 첨부 파일을 보내기만 됩니다 스마트 호스트에 대 한 검색을 해제합니다</span><span class="sxs-lookup"><span data-stu-id="d754a-148">Turn scanning off for internal senders, scanners, faxes, or smart hosts that will only send known, good attachments</span></span>  <br/> <span data-ttu-id="d754a-149">내부 메일을 라우팅하도록 불필요 한 지연을 방지합니다</span><span class="sxs-lookup"><span data-stu-id="d754a-149">Prevent unnecessary delays in routing internal mail</span></span>  <br/> <span data-ttu-id="d754a-150">**이 옵션은 대부분의 사용자에 대 한 권장 되지 않습니다. 내부 보낸 사람의 소규모 그룹에 대해 ATP 안전한 첨부 파일 검사를 해제 수 있습니다.**</span><span class="sxs-lookup"><span data-stu-id="d754a-150">**This option is not recommended for most users. It enables you to turn ATP Safe Attachments scanning off for a small group of internal senders.**</span></span>           |
|<span data-ttu-id="d754a-151">**모니터링**</span><span class="sxs-lookup"><span data-stu-id="d754a-151">**Monitor**</span></span> <br/> |<span data-ttu-id="d754a-152">첨부 파일이 있는 메시지를 전달 하 고 검색 된 맬웨어와 수행 하는 작업을 추적합니다</span><span class="sxs-lookup"><span data-stu-id="d754a-152">Delivers messages with attachments and then tracks what happens with detected malware</span></span>  <br/> |<span data-ttu-id="d754a-153">조직에서 검색 된 맬웨어 이동 하는 위치를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d754a-153">See where detected malware goes in your organization</span></span>  <br/> |
|<span data-ttu-id="d754a-154">**블록**</span><span class="sxs-lookup"><span data-stu-id="d754a-154">**Block**</span></span> <br/> |<span data-ttu-id="d754a-155">시계에서 검색 된 맬웨어 첨부 파일이 있는 메시지를 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-155">Prevents messages with detected malware attachments from proceeding</span></span>  <br/> <span data-ttu-id="d754a-156">[Office 365의 격리](manage-quarantined-messages-and-files.md) 여기에서 보안 관리자 또는 분석가 수를 검토 하 고 릴리스 (또는 삭제) 해당 메시지를 검색 된 맬웨어가 포함 된 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-156">Sends messages with detected malware to [quarantine in Office 365](manage-quarantined-messages-and-files.md) where a security administrator or analyst can review and release (or delete) those messages</span></span>  <br/> <span data-ttu-id="d754a-157">향후 메시지와 첨부 파일을 자동으로 차단</span><span class="sxs-lookup"><span data-stu-id="d754a-157">Blocks future messages and attachments automatically</span></span>  <br/> |<span data-ttu-id="d754a-158">조직 동일한 맬웨어 첨부 파일을 사용 하 여 반복 해 서 공격 으로부터 보호</span><span class="sxs-lookup"><span data-stu-id="d754a-158">Safeguard your organization from repeated attacks using the same malware attachments</span></span>  <br/> |
|<span data-ttu-id="d754a-159">**바꾸기**</span><span class="sxs-lookup"><span data-stu-id="d754a-159">**Replace**</span></span> <br/> |<span data-ttu-id="d754a-160">제거는 맬웨어 첨부 파일 검색</span><span class="sxs-lookup"><span data-stu-id="d754a-160">Removes detected malware attachments</span></span>  <br/> <span data-ttu-id="d754a-161">첨부 파일이 제거 된 받는 사람에 게 알리는</span><span class="sxs-lookup"><span data-stu-id="d754a-161">Notifies recipients that attachments have been removed</span></span>  <br/> <span data-ttu-id="d754a-162">[Office 365의 격리](manage-quarantined-messages-and-files.md) 여기에서 보안 관리자 또는 분석가 수를 검토 하 고 릴리스 (또는 삭제) 해당 메시지를 검색 된 맬웨어가 포함 된 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-162">Sends messages with detected malware to [quarantine in Office 365](manage-quarantined-messages-and-files.md) where a security administrator or analyst can review and release (or delete) those messages</span></span>  <br/> |<span data-ttu-id="d754a-163">받는 사람에 게 검색 된 맬웨어로 인해 제거 된 첨부 파일에 대 한 가시성을 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-163">Raise visibility to recipients that attachments were removed because of detected malware</span></span>  <br/> |
|<span data-ttu-id="d754a-164">**동적 배달**</span><span class="sxs-lookup"><span data-stu-id="d754a-164">**Dynamic Delivery**</span></span> <br/> |<span data-ttu-id="d754a-165">메시지를 바로 전달</span><span class="sxs-lookup"><span data-stu-id="d754a-165">Delivers messages immediately</span></span>  <br/> <span data-ttu-id="d754a-166">검색 완료 되며 없는 맬웨어가 탐지 되는 경우 첨부 파일을 다음가 다시 연결 될 때까지 개체 틀 파일 첨부 파일을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-166">Replaces attachments with a placeholder file until scanning is complete, and then reattaches the attachments if no malware is detected</span></span>  <br/> <span data-ttu-id="d754a-167">대부분의 Pdf 및 Office에 대 한 기능을 미리 보는 첨부 파일 포함 파일 검사 중</span><span class="sxs-lookup"><span data-stu-id="d754a-167">Includes attachment previewing capabilities for most PDFs and Office files during scanning</span></span>  <br/> <span data-ttu-id="d754a-168">검색 된 맬웨어 있는 메시지를 격리 여기에서 보안 관리자 또는 분석가 수를 검토 하 고 릴리스 (또는 삭제) 해당 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-168">Sends messages with detected malware to Quarantine where a security administrator or analyst can review and release (or delete) those messages</span></span>  <br/> [<span data-ttu-id="d754a-169">동적 배달 하 고 ATP 안전한 첨부 파일 미리 보기에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="d754a-169">Learn about dynamic delivery and previewing with ATP Safe Attachments</span></span>](dynamic-delivery-and-previewing.md) <br/> |<span data-ttu-id="d754a-170">악의적인 파일에서 받는 사람을 보호 하는 동안 메시지 지연을 방지합니다</span><span class="sxs-lookup"><span data-stu-id="d754a-170">Avoid message delays while protecting recipients from malicious files</span></span>  <br/> <span data-ttu-id="d754a-171">받는 사람에 게 검사를 수행 하는 동안 안전 모드에서 첨부 파일 미리 보기를 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d754a-171">Enable recipients to preview attachments in safe mode while scanning is taking place</span></span>  <br/> |
|<span data-ttu-id="d754a-172">**리디렉션 사용**</span><span class="sxs-lookup"><span data-stu-id="d754a-172">**Enable redirect**</span></span> <br/> |<span data-ttu-id="d754a-173">적용 하는 모니터, 차단 또는 바꾸기 옵션을 선택 하는 경우</span><span class="sxs-lookup"><span data-stu-id="d754a-173">Applies when the Monitor, Block, or Replace option is chosen</span></span>  <br/> <span data-ttu-id="d754a-174">보안 관리자 또는 분석가 조사할 수의 첨부 파일을 지정 된 전자 메일 주소를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="d754a-174">Sends attachments to a specified email address where security administrators or analysts can investigate</span></span>  <br/> |<span data-ttu-id="d754a-175">보안 관리자 및 분석가 의심 스러운 첨부 파일 조사를 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d754a-175">Enable security administrators and analysts to research suspicious attachments</span></span>  <br/> |
   
## <a name="related-topics"></a><span data-ttu-id="d754a-176">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d754a-176">Related topics</span></span>

[<span data-ttu-id="d754a-177">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="d754a-177">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="d754a-178">Office 365의에서 ATP 안전 하 게 보호 첨부 파일</span><span class="sxs-lookup"><span data-stu-id="d754a-178">ATP Safe Attachments in Office 365</span></span>](atp-safe-attachments.md)
  
[<span data-ttu-id="d754a-179">Office 365의에서 ATP 안전 하 게 보호 링크</span><span class="sxs-lookup"><span data-stu-id="d754a-179">ATP Safe Links in Office 365</span></span>](atp-safe-links.md)
  
[<span data-ttu-id="d754a-180">Office 365의 ATP 안전한 링크 정책 설정</span><span class="sxs-lookup"><span data-stu-id="d754a-180">Set up ATP Safe Links policies in Office 365</span></span>](set-up-atp-safe-links-policies.md)
  
[<span data-ttu-id="d754a-181">고급 위협 보호에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="d754a-181">View the reports for Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="d754a-182">Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="d754a-182">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

