---
title: 정보 관리 정책 만들기 및 적용
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/16/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 8ccac9e4-3a50-49fa-a95b-d186032a6ee3
ms.collection:
- M365-security-compliance
description: 정보 관리 정책을 사용 하면 조직이 콘텐츠를 보존 하는 기간을 제어 하 고, 사용자가 콘텐츠를 사용 하는 작업을 감사 하 고, 문서에 바코드 또는 레이블을 추가할 수 있습니다. 정책은 법적 및 정부 규정 또는 내부 비즈니스 프로세스에 대 한 준수를 보장 하는 데 도움이 될 수 있습니다. 관리자는 문서 추적 방법 및 문서 보존 기간을 제어 하는 정책을 설정할 수 있습니다.
ms.openlocfilehash: d4161ad3684a006f0e4b2b9e0e856ea0a8aa67fc
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214698"
---
# <a name="create-and-apply-information-management-policies"></a><span data-ttu-id="690a9-105">정보 관리 정책 만들기 및 적용</span><span class="sxs-lookup"><span data-stu-id="690a9-105">Create and apply information management policies</span></span>

<span data-ttu-id="690a9-p102">정보 관리 정책을 사용 하면 조직이 콘텐츠를 보존 하는 기간을 제어 하 고, 사용자가 콘텐츠를 사용 하는 작업을 감사 하 고, 문서에 바코드 또는 레이블을 추가할 수 있습니다. 정책은 법적 및 정부 규정 또는 내부 비즈니스 프로세스에 대 한 준수를 보장 하는 데 도움이 될 수 있습니다. 관리자는 문서 추적 방법 및 문서 보존 기간을 제어 하는 정책을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p102">Information management policies enable your organization to control how long to retain content, to audit what people do with content, and to add barcodes or labels to documents. A policy can help enforce compliance with legal and governmental regulations or internal business processes. As an administrator, you can set up a policy to control how to track documents and how long to retain documents.</span></span>
  
<span data-ttu-id="690a9-109">사이트 계층 구조에서 가장 광범위 하 게 세 가지 위치에 있는 정보 관리 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-109">You can create an information management policy can at three different locations in the site hierarchy, from the broadest to the narrowest:</span></span>
  
- <span data-ttu-id="690a9-110">사이트 모음 내의 여러 콘텐츠 형식에 사용할 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-110">Create a policy to use on multiple content types within a site collection.</span></span>
    
- <span data-ttu-id="690a9-111">사이트 콘텐츠 형식에 대 한 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-111">Create a policy for a site content type.</span></span>
    
- <span data-ttu-id="690a9-112">목록 또는 라이브러리에 대 한 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-112">Create a policy for a list or library.</span></span>
    
<span data-ttu-id="690a9-113">자세한 내용은 [정보 관리 정책 소개를](intro-to-info-mgmt-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="690a9-113">For more information, see [Introduction to information management policies](intro-to-info-mgmt-policies.md).</span></span>
  
## <a name="create-a-policy-for-multiple-content-types-within-a-site-collection"></a><span data-ttu-id="690a9-114">사이트 모음 내에서 여러 콘텐츠 형식에 대 한 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="690a9-114">Create a policy for multiple content types within a site collection</span></span>
<span data-ttu-id="690a9-115"><a name="__toc261001590"> </a></span><span class="sxs-lookup"><span data-stu-id="690a9-115"></span></span>

<span data-ttu-id="690a9-p103">사이트 모음 내에서 특정 유형의 모든 문서에 정보 정책이 적용 되도록 하려면 사이트 모음 수준에서 정책을 만든 후 나중에 콘텐츠 형식에 정책을 적용 하는 것이 좋습니다. 이러한 정책을 사이트 모음 정책 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p103">To ensure that an information policy is applied to all documents of a certain type within a site collection, consider creating the policy at the site collection level and then later apply the policy to content types. These are referred to as site collection policies.</span></span> 
  
1. <span data-ttu-id="690a9-p104">제목 표시줄의 사이트 모음 홈 \> 페이지 **설정**![SharePoint 2016 설정 단추 ](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **사이트 설정**</span><span class="sxs-lookup"><span data-stu-id="690a9-p104">On the site collection home page \> **Settings**![SharePoint 2016 Settings button on title bar.](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **Site Settings**.</span></span>
    
    <span data-ttu-id="690a9-120">SharePoint 그룹에 연결 된 사이트에서 **설정을**클릭 하 고 **사이트 콘텐츠**를 클릭 한 다음 **사이트 설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-120">In a SharePoint group-connected site, click **Settings**, click **Site Contents**, and then click **Site Settings**.</span></span> 
    
2. <span data-ttu-id="690a9-121">사이트 설정 페이지의 **사이트 모음 관리** \> **콘텐츠 형식 정책 서식 파일**에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-121">On the Site Settings page, under **Site Collection Administration** \> **Content Type Policy Templates**.</span></span> 
  
![사이트 설정 페이지의 콘텐츠 형식 정책 서식 파일 링크](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. <span data-ttu-id="690a9-123">정책 페이지 \> 를 **만듭니다**.</span><span class="sxs-lookup"><span data-stu-id="690a9-123">On the Policies page \> **Create**.</span></span> 
    
4. <span data-ttu-id="690a9-124">정책에 대 한 이름 및 설명을 입력 한 다음 사용자에 게 정책에 대해 설명 하는 간단한 정책 문을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-124">Enter a name and description for the policy, and then write a brief policy statement that explains to users what the policy is for.</span></span>
    
5. <span data-ttu-id="690a9-125">정책과 연결할 기능을 설정 하는 방법에 대 한 자세한 내용은 사이트 콘텐츠 형식에 대 한 정책 만들기의 다음 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="690a9-125">See the next section on creating policies for a site content type to learn how to set up the features you want to associate with the policy.</span></span> 
    
6. <span data-ttu-id="690a9-126">**확인**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-126">Choose **OK**.</span></span>
    
## <a name="create-a-policy-for-a-site-content-type"></a><span data-ttu-id="690a9-127">사이트 콘텐츠 형식에 대 한 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="690a9-127">Create a policy for a site content type</span></span>
<span data-ttu-id="690a9-128"><a name="__create_a_policy"> </a></span><span class="sxs-lookup"><span data-stu-id="690a9-128"></span></span>

<span data-ttu-id="690a9-p105">콘텐츠 형식에 정보 관리 정책을 추가 하면 정책 기능을 여러 목록 또는 라이브러리에 쉽게 연결할 수 있습니다. 기존 정보 관리 정책을 콘텐츠 형식에 추가 하거나 개별 콘텐츠 형식에 따라 고유한 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p105">Adding an information management policy to a content type makes it easy to associate policy features with multiple lists or libraries. You can choose to add an existing information management policy to a content type or create a unique policy specific to an individual content type.</span></span>
  
 <span data-ttu-id="690a9-p106">목록에 해당 하는 콘텐츠 형식에 정보 관리 정책을 추가할 수도 있습니다. 이는 콘텐츠 형식을 사용 하는 해당 목록의 항목에만 정책을 적용 하는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p106">You can also add an information management policy to a content type that is specific to lists. This has the effect of applying the policy only to items in that list that are using the content type.</span></span> 
  
1. <span data-ttu-id="690a9-p107">제목 표시줄의 사이트 모음 홈 \> 페이지 **설정**![SharePoint 2016 설정 단추 ](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **사이트 설정**</span><span class="sxs-lookup"><span data-stu-id="690a9-p107">On the site collection home page \> **Settings**![SharePoint 2016 Settings button on title bar.](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **Site Settings**.</span></span>
    
    <span data-ttu-id="690a9-135">SharePoint 그룹에 연결 된 사이트에서 **설정을**클릭 하 고 **사이트 콘텐츠**를 클릭 한 다음 **사이트 설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-135">In a SharePoint group-connected site, click **Settings**, click **Site Contents**, and then click **Site Settings**.</span></span> 
    
2. <span data-ttu-id="690a9-136">사이트 설정 페이지의 **웹 디자이너 갤러리** \> **사이트 콘텐츠 형식**아래에서</span><span class="sxs-lookup"><span data-stu-id="690a9-136">On the Site Settings page, under **Web Designer Galleries** \> **Site content types**.</span></span>
  
![사이트 설정 페이지의 사이트 콘텐츠 형식 링크](media/6f6fa51f-15d7-4782-b06f-a7b36e874cd3.png)
  
3. <span data-ttu-id="690a9-138">사이트 콘텐츠 형식 설정 페이지에서 정책을 추가 하려는 콘텐츠 형식을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-138">On the Site Content Type Settings page, select the content type that you want to add a policy to.</span></span>
    
4. <span data-ttu-id="690a9-139">사이트 콘텐츠 형식 페이지의 **설정** \> **정보 관리 정책 설정**아래에서</span><span class="sxs-lookup"><span data-stu-id="690a9-139">On the Site Content Type page, under **Settings** \> **Information management policy settings**.</span></span>
    
5. <span data-ttu-id="690a9-140">정책 편집 페이지에서 정책의 이름과 설명을 입력 한 다음 사용자에 게 정책에 대해 설명 하는 간략 한 설명을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-140">On the Edit Policy page, enter a name and description for the policy, and then write a brief description that explains to users what the policy is for.</span></span>
    
6. <span data-ttu-id="690a9-141">다음 섹션에서 정보 관리 정책에 추가 하려는 개별 정책 기능을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-141">In the next sections, select the individual policy features that you want to add to your information management policy.</span></span> 
  
![콘텐츠 정책 유형](media/19fcb8a3-974b-40d3-a13f-b76088d122f8.png)
  
7. <span data-ttu-id="690a9-143">이 정책이 적용 되는 문서 및 항목에 대 한 보존 기간을 지정 하려면 **보존 사용**을 선택 하 고 보존 기간 및 항목이 만료 될 때 발생 시킬 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-143">To specify a retention period for documents and items that are subject to this policy, choose **Enable Retention**, and then specify the retention period and the actions that you want to occur when the items expire.</span></span>
    
    <span data-ttu-id="690a9-144">보존 기간을 지정 하려면</span><span class="sxs-lookup"><span data-stu-id="690a9-144">To specify a retention period</span></span>
    
||||||<span data-ttu-id="690a9-145">**1.**</span><span class="sxs-lookup"><span data-stu-id="690a9-145">**1.**</span></span>|<span data-ttu-id="690a9-146">\* \* 선택 \* \* 레코드에 대 한 보존 스테이지 추가 ... \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="690a9-146">\*\*Choose \*\*Add a retention stage for records…\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||<span data-ttu-id="690a9-147">2.</span><span class="sxs-lookup"><span data-stu-id="690a9-147">2.</span></span>  <br/> | <span data-ttu-id="690a9-p108">문서 또는 항목의 만료 기한을 지정 하려면 보존 기간 옵션을 선택 합니다. 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p108">Select a retention period option to specify when documents or items are set to expire. Do one of the following:  </span></span><br/>  <span data-ttu-id="690a9-150">날짜 속성에 따라 만료 날짜를 설정 하려면 **이벤트** \> 에서 **이 스테이지는 항목의 date 속성을 기준으로**하며, 작성 또는 수정한 날짜와 같은 문서 또는 항목 작업을 선택한 다음이 작업 후의 시간 간격을 선택 합니다 ( 예를 들어 항목이 만료 되도록 하려면 일, 월 또는 년 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-150">To set the expiration date based on a date property, under **Event** \> **This stage is based off a date property on the item**, and then select the document or item action (for example, Created or Modified) and the increment of time after this action (for example, the number of days, months, or years) when you want the item to expire.</span></span>  <br/>  <span data-ttu-id="690a9-151">사용자 지정 보존 수식을 사용 하 여 만료를 결정 하려면 **이 서버에 설치 된 사용자 지정 보존 수식으로 설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-151">To use a custom retention formula to determine expiration, choose **Set by a custom retention formula installed on this server**.</span></span>  <br/> <span data-ttu-id="690a9-152">> [!NOTE]>이 옵션은 관리자가 사용자 지정 수식을 설정한 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-152">> [!NOTE]>  This option is only available if a custom formula has been set up by your administrator.</span></span>           |
||||||<span data-ttu-id="690a9-153">3.</span><span class="sxs-lookup"><span data-stu-id="690a9-153">3.</span></span>  <br/> |<span data-ttu-id="690a9-p109">**워크플로 시작** 옵션은 워크플로가 이미 연결 된 목록, 라이브러리 또는 콘텐츠 형식의 정책을 정의 하는 경우에만 사용할 수 있습니다. 그러면 선택할 수 있는 워크플로 선택이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p109">The **Start a workflow** option is available only if you are defining a policy for a list, library, or content type that already has a workflow associated with it. You will then be given a choice of workflows to choose from.  </span></span><br/> |
||||||<span data-ttu-id="690a9-156">4.</span><span class="sxs-lookup"><span data-stu-id="690a9-156">4.</span></span>  <br/> |<span data-ttu-id="690a9-157">**되풀이** 섹션에서 **이 단계의 작업 반복 실행** 을 선택 합니다. 작업을 다시 실행할 빈도를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-157">In the **Recurrence** section, select **Repeat this stage's action…** and enter how often you want the action to reoccur.</span></span>  <br/> <span data-ttu-id="690a9-p110">> [!NOTE]>이 옵션은 선택한 작업을 반복할 수 있는 경우에만 사용할 수 있습니다. 예를 들어 작업에 대 한 되풀이를 **영구적으로 삭제**하도록 설정할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p110">> [!NOTE]>  This option is only available if the action you selected can be repeated. For example, you cannot set recurrence for the action **Permanently Delete**.</span></span>           |
||||||<span data-ttu-id="690a9-160">5.</span><span class="sxs-lookup"><span data-stu-id="690a9-160">5.</span></span>  <br/> |<span data-ttu-id="690a9-161">**확인을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-161">Chose **OK**.</span></span>  <br/> |
   
1. <span data-ttu-id="690a9-162">이 정책이 적용 되는 문서 및 항목에 대 한 감사를 사용 하도록 설정 하려면 **감사 사용**을 선택 하 고 감사 하려는 이벤트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-162">To enable auditing for the documents and items that are subject to this policy, choose **Enable Auditing**, and then specify the events you want to audit.</span></span>
    
    <span data-ttu-id="690a9-163">감사를 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="690a9-163">To enable auditing</span></span>
    
||||||<span data-ttu-id="690a9-164">1. \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="690a9-164">\*\*\*\*1.\*\*\*\*</span></span>|<span data-ttu-id="690a9-165">정책 편집 페이지의 \* \* \*\*\*\* \*\*\*\* **\>** 감사 **사용** \* \*을 선택한 다음 감사 내역을 유지할 이벤트 옆에 있는 확인란을 선택 합니다. \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="690a9-165">\*\*\*\*On the Edit Policy page,\*\* **under** **Auditing** **\>** **Enable auditing** \*\*, and then select the check boxes next to the events you want to keep an audit trail for.\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||<span data-ttu-id="690a9-166">**2.**</span><span class="sxs-lookup"><span data-stu-id="690a9-166">**2.**</span></span> <br/> |<span data-ttu-id="690a9-167">**사용자에 게 이러한 바코드를 문서에 삽입 하 라는 메시지를 표시 하려면** **선택** **저장 또는 인쇄 하기 전에 바코드 삽입 여부 확인** **.**</span><span class="sxs-lookup"><span data-stu-id="690a9-167">**To prompt users to insert these barcodes into documents,** **choose** **Prompt users to insert a barcode before saving or printing** **.**</span></span> <br/> |
||||||<span data-ttu-id="690a9-168">**3.**</span><span class="sxs-lookup"><span data-stu-id="690a9-168">**3.**</span></span> <br/> |<span data-ttu-id="690a9-169">**선택** **확인** \* \* 감사 기능을 정책에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-169">**Choose** **OK** \*\* to apply the auditing feature to the policy.</span></span> ** <br/> |
|||||||<span data-ttu-id="690a9-p111">감사 정책 기능을 사용 하면 조직에서 문서에 대 한 감사 내역 및 작업 목록, 문제점 목록, 토론 그룹, 일정 등의 목록 항목을 만들고 분석할 수 있습니다. 이 정책 기능은 콘텐츠를 보거나 편집 하거나 삭제 하는 경우와 같은 이벤트를 기록 하는 감사 로그를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p111">The Auditing Policy feature enables organizations to create and analyze audit trails for documents and to list items such as task lists, issues lists, discussion groups, and calendars. This policy feature provides an audit log that records events, such as when content is viewed, edited, or deleted.</span></span>  <br/> |
|||||||<span data-ttu-id="690a9-p112">정보 관리 정책의 일부로 감사가 사용 되도록 설정 된 경우 관리자는 Microsoft Excel을 기반으로 하며 현재 사용 현황을 요약 하는 정책 사용 현황 보고서에서 감사 데이터를 볼 수 있습니다. 관리자는 이러한 보고서를 사용 하 여 조직 내에서 정보가 사용 되는 방식을 결정할 수 있습니다. 이러한 보고서는 조직에서 규정 준수 여부를 확인 하 고 문서화 하는 데도 도움이 되거나 잠재적으로 발생할 수 있는 문제를 조사 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p112">When auditing is enabled as part of an information management policy, administrators can view the audit data in policy usage reports that are based in Microsoft Excel and that summarize current usage. Administrators can use these reports to determine how information is being used within the organization. These reports can also help organizations to verify and document their regulatory compliance or to investigate potential concerns.</span></span>  <br/> |
|||||||<span data-ttu-id="690a9-175">감사 로그에는 이벤트 이름, 이벤트의 날짜 및 시간, 해당 작업을 수행한 사용자의 시스템 이름과 같은 정보가 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-175">The audit log records the following information: event name, date and time of the event, and system name of the user who performed the action.</span></span>  <br/> |
   
1. <span data-ttu-id="690a9-p113">정책의 일부로 바코드를 사용 하도록 설정 하면 문서 속성에 바코드가 추가 되 고 바코드가 적용 되는 문서의 머리글 영역에 표시 됩니다. 레이블과 마찬가지로 문서 에서도 바코드를 수동으로 제거할 수 있습니다. 2010 Office 릴리스 프로그램의 **삽입** 탭을 사용 하 여 항목을 인쇄 하거나 저장할 때 바코드를 포함할지, 아니면 수동으로 삽입 해야 하는지 여부를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p113">When barcodes are enabled as part of a policy, they are added to document properties and displayed in the header area of the document to which the barcode is applied. Like labels, barcodes can also be manually removed from a document. You can specify whether users should be prompted to include the barcode when printing or saving an item or if the barcode should be inserted manually using the **Insert** tab in 2010 Office release programs.</span></span> 
    
    <span data-ttu-id="690a9-179">바코드를 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="690a9-179">To enable barcodes</span></span>
    
||||||<span data-ttu-id="690a9-180">1. \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="690a9-180">\*\*\*\*1.\*\*\*\*</span></span>|<span data-ttu-id="690a9-181">**정책 편집 페이지의 **바코드** \> 에서 **바코드를 사용**합니다.**</span><span class="sxs-lookup"><span data-stu-id="690a9-181">**On the Edit Policy page, under **Barcodes**\> **Enable Barcodes**.**</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||<span data-ttu-id="690a9-182">**2.**</span><span class="sxs-lookup"><span data-stu-id="690a9-182">**2.**</span></span> <br/> |<span data-ttu-id="690a9-183">사용자에 게 이러한 바코드를 문서에 삽입할지 묻는 메시지를 표시 하려면 **저장 또는 인쇄 하기 전에 바코드 삽입 여부 확인을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-183">To prompt users to insert these barcodes into documents, choose **Prompt users to insert a barcode before saving or printing**.</span></span>  <br/> |
||||||<span data-ttu-id="690a9-184">**3.**</span><span class="sxs-lookup"><span data-stu-id="690a9-184">**3.**</span></span> <br/> |<span data-ttu-id="690a9-185">**확인** 을 선택 하 여 바코드 기능을 정책에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-185">Choose **OK** to apply the barcode feature to the policy.</span></span>  <br/> |
|||||||
 <span data-ttu-id="690a9-p114">바코드 정책은 코드 39 표준 바코드를 생성 합니다. 바코드 기호 아래에 바코드 값을 나타내는 텍스트가 포함 됩니다. 그러면 스캔 하드웨어를 사용할 수 없는 경우에도 바코드 데이터를 사용할 수 있습니다. 사용자는 검색 상자에 바코드 번호를 직접 입력 하 여 사이트의 항목을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p114">The barcode policy generates Code 39 standard barcodes. Each barcode image includes text below the barcode symbol that represents the barcode value. This enables the barcode data to be used even when scanning hardware is not available. Users can manually type the barcode number into the search box to locate the item on a site.</span></span>  <br/> |
   
1. <span data-ttu-id="690a9-190">이 정책이 적용 되는 문서에 레이블이 포함 되도록 하려면 레이블 **사용**을 선택 하 고 레이블에 대해 원하는 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-190">To require that documents that are subject to this policy have labels, choose **Enable Labels**, and then specify the settings that you want for the labels.</span></span>
    
    <span data-ttu-id="690a9-191">레이블을 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="690a9-191">To enable labels</span></span>
    
||||||<span data-ttu-id="690a9-192">**1.**</span><span class="sxs-lookup"><span data-stu-id="690a9-192">**1.**</span></span>|<span data-ttu-id="690a9-193">\* \* 사용자가 문서에 레이블을 추가 하도록 하려면 **저장 또는 인쇄 하기 전에 레이블 삽입 여부 확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-193">\*\*To require users to add a label to a document, choose **Prompt users to insert a label before saving or printing**.</span></span>  <br/> <span data-ttu-id="690a9-194">> [!NOTE]> 레이블을 선택 사항으로 지정 하려면이 확인란을 선택 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-194">> [!NOTE]>  If you want labels to be optional, do not select this check box.</span></span>        **|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||<span data-ttu-id="690a9-195">2.</span><span class="sxs-lookup"><span data-stu-id="690a9-195">2.</span></span>  <br/> |<span data-ttu-id="690a9-196">레이블이 삽입 된 후에 변경할 수 없도록 레이블을 잠그려면 **레이블 추가 후 변경 금지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-196">To lock a label so that it cannot be changed after it has been inserted, choose **Prevent changes to labels after they are added**.</span></span>  <br/>  <span data-ttu-id="690a9-p115">이 설정은 Word, Excel 또는 PowerPoint와 같은 클라이언트 응용 프로그램의 항목에 레이블을 삽입 한 후에 레이블 텍스트를 업데이트 하지 않도록 합니다. 이 문서나 항목의 속성이 업데이트 될 때 레이블을 업데이트 하려면이 확인란을 선택 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p115">This setting prevents the label text from updating once the label has been inserted into an item within a client application such as Word, Excel, or PowerPoint. If you want the label to be updated when the properties for this document or item are updated, do not select this check box.  </span></span><br/> |
||||||<span data-ttu-id="690a9-199">3.</span><span class="sxs-lookup"><span data-stu-id="690a9-199">3.</span></span>  <br/> |<span data-ttu-id="690a9-p116">레이블 형식 상자에 표시 하려는 레이블의 텍스트를 입력 합니다. 레이블에는 열 참조가 최대 10 개까지 포함 될 수 있으며, 각 참조에는 최대 255 자까지 사용할 수 있습니다. 레이블에 대 한 형식을 만들려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p116">In the Label format box, enter the text for the label as you want it to be displayed. Labels can contain up to 10 column references, each of which can be up to 255 characters long. To create the format for your label, do the following:</span></span>  <br/> <span data-ttu-id="690a9-p117">표시 되도록 할 순서 대로 레이블에 포함할 열의 이름을 입력 합니다 (선택 항목). 정책 편집 페이지의 예와 같이 열 이름을{}중괄호 ()로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p117">Type the names of the columns that you want to include in the label in the order in which you want them to appear. Enclose the column names in curly brackets ({}), as shown in the example on the Edit Policy page.</span></span>  <br/> <span data-ttu-id="690a9-205">정책 편집 페이지의 예와 같이 대괄호 외부의 열을 식별 하는 단어를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-205">Type words to identify the columns outside the brackets, as shown in the example on the Edit Policy page.</span></span>  <br/> |
||||||<span data-ttu-id="690a9-206">4.</span><span class="sxs-lookup"><span data-stu-id="690a9-206">4.</span></span>  <br/> |<span data-ttu-id="690a9-207">줄 바꿈을 추가 하려면 줄 바꿈을 표시할 위치에 **\n** 을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-207">To add a line break, enter **\n** where you want the line break to appear.</span></span>  <br/> |
||||||<span data-ttu-id="690a9-208">5.</span><span class="sxs-lookup"><span data-stu-id="690a9-208">5.</span></span>  <br/> |<span data-ttu-id="690a9-209">원하는 글꼴 크기와 스타일을 선택 하 고 문서 내에서 레이블을 배치할 위치 (왼쪽, 가운데 또는 오른쪽)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-209">Select the font size and style that you want, and specify whether you want the label positioned left, center, or right within the document.</span></span>  <br/>  <span data-ttu-id="690a9-p118">사용자 컴퓨터에서 사용할 수 있는 글꼴 및 스타일을 선택 합니다. 글꼴 크기는 레이블에 표시할 수 있는 텍스트의 양에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p118">Select a font and style that are available on the users' computers. The size of the font affects how much text can be displayed on the label.</span></span>  <br/> |
||||||<span data-ttu-id="690a9-212">6.</span><span class="sxs-lookup"><span data-stu-id="690a9-212">6.</span></span>  <br/> |<span data-ttu-id="690a9-p119">레이블의 높이와 너비를 입력 합니다. 레이블 높이는 0.25 인치에서 20cm 사이 이며, 레이블 너비의 범위는 0.25 인치에서 20 인치 사이입니다. 레이블 텍스트는 항상 레이블 이미지의 가운데에 맞춥니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p119">Enter the height and width of the label. Label height can range from .25 inches to 20 inches, and label width can range from .25 inches to 20 inches. Label text is always vertically centered within the label image.</span></span>  <br/> |
||||||<span data-ttu-id="690a9-216">7.</span><span class="sxs-lookup"><span data-stu-id="690a9-216">7.</span></span>  <br/> |<span data-ttu-id="690a9-217">**새로 고침** 을 선택 하 여 레이블 콘텐츠를 미리 봅니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-217">Choose **Refresh** to preview the label content.</span></span>  <br/> |
   
1. <span data-ttu-id="690a9-218">**확인**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-218">Choose **OK**.</span></span>
    
## <a name="create-a-policy-for-a-list-library-or-folder-location-based-retention-policy"></a><span data-ttu-id="690a9-219">목록, 라이브러리 또는 폴더에 대한 정책(위치 기반 보존 정책) 만들기</span><span class="sxs-lookup"><span data-stu-id="690a9-219">Create a policy for a list, library or folder (location-based retention policy)</span></span>
<span data-ttu-id="690a9-220"><a name="__create_a_policy"> </a></span><span class="sxs-lookup"><span data-stu-id="690a9-220"></span></span>

<span data-ttu-id="690a9-p120">특정 목록, 라이브러리 또는 폴더에만 적용 되는 보존 정책을 정의할 수 있습니다. 그러나 이러한 방식으로 보존 정책을 만드는 경우에는 다른 목록, 라이브러리, 폴더 또는 사이트에 대해이 정책을 다시 사용할 수 없으며 위치 기반 정책에는 사이트 모음 정책을 적용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p120">You can define a retention policy that applies only to a specific list, library or folder. However, if you create a retention policy this way, you cannot reuse this policy on other lists, libraries, folders or sites, and you cannot apply a site collection policy to a location based policy.</span></span>
  
<span data-ttu-id="690a9-p121">단일 위치의 모든 콘텐츠 형식에 단일 보존 정책을 적용 하려는 경우에는 위치 기반 보존을 사용 하는 것이 좋습니다. 대부분의 경우에는 보존 정책이 모든 콘텐츠 형식에 대해 지정 되어 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p121">If you want to apply a single retention policy to all types of content in a single location, you will most likely want to use location-based retention. In most other cases, you will want to verify that a retention policy is specified for all content types.</span></span>
  
 <span data-ttu-id="690a9-225">상속을 중단 하 고 하위 수준에서 새 보존 정책을 정의 하는 경우를 제외 하 고 각 하위 폴더는 부모의 보존 정책을 상속 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-225">Each subfolder inherits the retention policy of its parent, unless you choose to break inheritance and define a new retention policy at the child level.</span></span> 
  
<span data-ttu-id="690a9-226">목록 또는 라이브러리에 대 한 보존 이외의 정보 관리 정책을 정의 하려면 해당 목록이 나 라이브러리에 연결 된 각 개별 목록 콘텐츠 형식에 대 한 정보 관리 정책을 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-226">If you want to define an information management policy other than retention to a list or library, you need to define an information management policy for each individual list content type associated with that list or library.</span></span>
  
 <span data-ttu-id="690a9-p122">콘텐츠 형식에서 목록 또는 라이브러리에 대 한 위치 기반 정책으로 전환 하기로 결정 한 경우에는 보존 정책만 위치 기반 정책으로 사용 됩니다. 기타 모든 관리 정책 (감사, 바코드 및 바코드)은 연결 된 콘텐츠 형식에서 상속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p122">If at any point you decide to switch from content type to location-based policies for a list or library, only the retention policy will be used as the location-based policy. All other management policies (audits, barcodes, and barcodes) will be inherited from the associated content types.</span></span> 
  
 <span data-ttu-id="690a9-p123">라이브러리 및 폴더 기반 보존 기능을 비활성화 하 여 사이트 모음에 대해 위치 기반 정책을 사용 하지 않도록 설정할 수 있습니다. 이렇게 하면 사이트 모음 관리자가 목록 관리자의 위치 기반 정책에 의해 해당 콘텐츠 형식 정책이 재정의 되지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p123">Location based policies can be disabled for a site collection by deactivating the Library and Folder Based Retention feature. This enables site collection administrators to ensure that their content type policies are not overridden by a list administrator's location based policies.</span></span> 
  
<span data-ttu-id="690a9-231">목록 또는 라이브러리에 대 한 정보 관리 정책 설정을 변경 하려면 최소한 목록 관리 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-231">You need at least the Manage Lists permission to change the information management policy settings for a list or library.</span></span>
  
1. <span data-ttu-id="690a9-232">정보 관리 정책을 지정 하려는 목록 또는 라이브러리로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-232">Navigate to the list or library for which you want to specify an information management policy.</span></span> 
    
2. <span data-ttu-id="690a9-233">리본 메뉴에서 **라이브러리** 또는 **목록** 탭 \> **라이브러리 설정** 또는 **목록 설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-233">On the ribbon, choose the **Library** or **List** tab \> **Library Settings** or **List Settings**.</span></span>
    
    <span data-ttu-id="690a9-234">SharePoint Online에서 **설정을** 클릭 한 다음 **목록 설정** 또는 **라이브러리 설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-234">In SharePoint Online, click **Settings** and then click **List settings** or **Library settings**.</span></span> 
    
3. <span data-ttu-id="690a9-235">**사용 권한 및 관리** \> **정보 관리 정책 설정**아래에서</span><span class="sxs-lookup"><span data-stu-id="690a9-235">Under **Permissions and Management**\> **Information management policy settings**.</span></span>
  
![문서 라이브러리에 대 한 설정 페이지의 정보 관리 정책 링크](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. <span data-ttu-id="690a9-237">정보 관리 정책 설정 페이지에서 목록 또는 라이브러리에 대 한 보존 원본이 라이브러리 및 폴더로 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-237">On the Information Management Policy Settings page, make sure that the source of retention for the list or library is set to Library and Folders.</span></span> 
  
<span data-ttu-id="690a9-p124">**콘텐츠 형식이** 원본으로 표시 되 면 **원본 변경을**클릭 한 다음 **라이브러리 및 폴더**를 클릭 합니다. 콘텐츠 형식 보존 정책이 무시 된다는 경고가 표시 됩니다. **확인을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p124">If **Content Type** appears as the source, click **Change Source**, and then click **Library and Folders**. You are alerted that content type retention policies will be ignored. Choose **OK**.</span></span> 
    
5. <span data-ttu-id="690a9-241">정책 편집 페이지의 **라이브러리 기반 보존 일정**에 만들려는 정책에 대 한 간략 한 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-241">On the Edit Policy page, under **Library Based Retention Schedule**, enter a brief description for the policy you are creating.</span></span> 
    
6. <span data-ttu-id="690a9-242">**보존 단계 추가 ...** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-242">Choose **Add a retention stage…**</span></span>
    
     <span data-ttu-id="690a9-243">레코드에서 레코드에 다른 보존 단계 정의 옵션을 선택 하 여 레코드에 대해 서로 다른 보존 정책을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-243">Note that under Records, you can choose to define different retention policies for records by selecting the Define different retention stages for records option.</span></span> 
    
7. <span data-ttu-id="690a9-p125">스테이지 속성 대화 상자에서 보존 기간 옵션을 선택 하 여 문서나 항목이 만료 되도록 설정 된 경우를 지정 합니다. 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p125">In the Stage properties dialog, select a retention period option to specify when documents or items are set to expire. Do one of the following:</span></span>
    
  - <span data-ttu-id="690a9-246">날짜 속성에 따라 만료 날짜를 설정 하려면 **이벤트** \> 에서 **이 스테이지는 항목의 date 속성을 기준으로**하며, 작성 또는 수정한 날짜와 같은 문서 또는 항목 작업을 선택한 다음이 작업 후의 시간 간격을 선택 합니다 ( 예를 들어 항목이 만료 되도록 하려면 일, 월 또는 년 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-246">To set the expiration date based on a date property, under **Event** \> **This stage is based off a date property on the item**, and then select the document or item action (for example, Created or Modified) and the increment of time after this action (for example, the number of days, months, or years) when you want the item to expire.</span></span> 
    
  - <span data-ttu-id="690a9-247">사용자 지정 보존 수식을 사용 하 여 만료를 결정 하려면 **이 서버에 설치 된 사용자 지정 보존 수식으로 설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-247">To use a custom retention formula to determine expiration, choose **Set by a custom retention formula installed on this server**.</span></span> 
    
    > [!NOTE]
    >  <span data-ttu-id="690a9-248">이 옵션은 관리자가 사용자 지정 수식을 설정한 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-248">This option is only available if a custom formula has been set up by your administrator.</span></span> 
  
  - <span data-ttu-id="690a9-p126">**동작**에서 문서나 항목이 만료 될 때 수행 되는 작업을 지정 합니다. 문서 또는 항목 (예: 삭제)에 대해 특정 작업을 수행 하도록 설정 하려면 목록에서 동작을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p126">Under **Action**, specify what you want to happen when the document or item expires. To enable a specific action to happen to the document or item (such as deletion), select an action from the list.</span></span> 
    
8. <span data-ttu-id="690a9-p127">**워크플로 시작** 옵션은 워크플로가 이미 연결 된 목록, 라이브러리 또는 콘텐츠 형식의 정책을 정의 하는 경우에만 사용할 수 있습니다. 그러면 선택할 수 있는 워크플로 선택이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p127">The **Start a workflow** option is available only if you are defining a policy for a list, library, or content type that already has a workflow associated with it. You will then be given a choice of workflows to choose from.</span></span> 
    
9. <span data-ttu-id="690a9-253">**되풀이**에서 **이 단계의 작업 반복** 에서를 선택 합니다. 작업을 다시 실행할 빈도를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-253">Under **Recurrence**, choose **Repeat this stage's action…** and enter how often you want the action to reoccur.</span></span> 
    
    > [!NOTE]
    >  <span data-ttu-id="690a9-p128">이 옵션은 선택한 작업을 반복할 수 있는 경우에만 사용할 수 있습니다. 예를 들어 작업에 대 한 되풀이를 **영구적으로 삭제**하도록 설정할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p128">This option is only available if the action you selected can be repeated. For example, you cannot set recurrence for the action **Permanently Delete**.</span></span> 
  
10. <span data-ttu-id="690a9-256">**확인**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-256">Choose **OK**.</span></span>
    
## <a name="apply-a-site-collection-policy-to-a-content-type"></a><span data-ttu-id="690a9-257">콘텐츠 형식에 사이트 모음 정책 적용</span><span class="sxs-lookup"><span data-stu-id="690a9-257">Apply a site collection policy to a content type</span></span>
<span data-ttu-id="690a9-258"><a name="__apply_a_site"> </a></span><span class="sxs-lookup"><span data-stu-id="690a9-258"></span></span>

<span data-ttu-id="690a9-p129">사이트에 대 한 정보 관리 정책을 사이트 모음 정책으로 이미 만든 경우에는 콘텐츠 형식에 정책 중 하나를 적용할 수 있습니다. 이렇게 하면 동일한 상위 콘텐츠 형식을 공유 하지 않는 사이트 모음의 여러 콘텐츠 형식에 동일한 정책을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p129">If information management policies have already been created for your site as site collection policies, you can apply one of the policies to a content type. By doing this, you can apply the same policy to multiple content types in a site collection that do not share the same parent content type.</span></span>
  
 <span data-ttu-id="690a9-p130">사이트 모음의 여러 콘텐츠 형식에 정책을 적용 하 고 관리 되는 메타 데이터 서비스가 구성 되어 있는 경우 콘텐츠 형식 게시를 사용 하 여 정보 관리 정책을 여러 사이트 모음에 게시할 수 있습니다. 자세한 내용은 [사이트 모음에서 콘텐츠 형식에 정책 적용](create-info-mgmt-policies.md#__apply_a_policy) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="690a9-p130">If you want to apply policies to multiple content types in a site collection, and you have a Managed Metadata Service configured, you can use Content Type Publishing to publish out information management polices to multiple site collections. See the section [Apply a policy to content types across site collections](create-info-mgmt-policies.md#__apply_a_policy) for more information.</span></span> 
  
1. <span data-ttu-id="690a9-263">정책을 적용 하려는 콘텐츠 형식이 포함 된 목록 또는 라이브러리로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-263">Navigate to the list or library that contains the content type to which you want to apply a policy.</span></span>
    
2. <span data-ttu-id="690a9-264">리본 메뉴에서 **라이브러리** 또는 **목록** 탭 \> **라이브러리 설정** 또는 **목록 설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-264">On the ribbon, choose the **Library** or **List** tab \> **Library Settings** or **List Settings**.</span></span>
    
    <span data-ttu-id="690a9-265">SharePoint Online에서 **설정을** 클릭 한 다음 **목록 설정** 또는 **라이브러리 설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-265">In SharePoint Online, click **Settings** and then click **List settings** or **Library settings**.</span></span> 
    
3. <span data-ttu-id="690a9-266">**사용 권한 및 관리** \> **정보 관리 정책 설정**아래에서</span><span class="sxs-lookup"><span data-stu-id="690a9-266">Under **Permissions and Management** \> **Information management policy settings**.</span></span>
  
![문서 라이브러리에 대 한 설정 페이지의 정보 관리 정책 링크](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. <span data-ttu-id="690a9-268">정책 원본이 **콘텐츠 형식**으로 설정 되어 있는지 확인 하 고 **콘텐츠 형식 정책** 에서 정책을 적용할 콘텐츠 형식을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-268">Verify that the policy source is set to **Content Types**, and under **Content Type Policies** select the content type you want to apply the policy to.</span></span> 
    
5. <span data-ttu-id="690a9-269">**정책** \> 에 **사이트 모음 사용 정책을**지정 합니다 .에서 목록에서 적용할 정책을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-269">Under **Specify the Policy** \> **Use a site collection policy**, and then select the policy that you want to apply from the list.</span></span> 
    
    > [!NOTE]
    >  <span data-ttu-id="690a9-270">사이트 모음 **정책 사용** 옵션을 사용할 수 없는 경우 사이트 모음에 대해 사이트 모음 정책이 정의 되지 않은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-270">If the **Use a site collection policy** option is not available, no site collection policies have been defined for the site collection.</span></span> 
  
6. <span data-ttu-id="690a9-271">**확인**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-271">Choose **OK**.</span></span>
    
     <span data-ttu-id="690a9-p131">작업 중인 목록 또는 라이브러리에서 여러 콘텐츠 형식의 관리를 지 원하는 경우 **콘텐츠 형식** 에서 정보 관리 정책을 지정할 콘텐츠 형식을 선택할 수 있습니다. 이렇게 하면 위의 5 단계로 바로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p131">If the list or library you are working with supports the management of multiple content types, under **Content Types** you can choose the content type for which you want to specify an information management policy. This will take you directly to Step 5 above.</span></span> 
    
## <a name="apply-a-policy-across-site-collections"></a><span data-ttu-id="690a9-274">사이트 모음에 대해 정책 적용</span><span class="sxs-lookup"><span data-stu-id="690a9-274">Apply a policy across site collections</span></span>
<span data-ttu-id="690a9-275"><a name="__toc260646789"> </a></span><span class="sxs-lookup"><span data-stu-id="690a9-275"></span></span>

<span data-ttu-id="690a9-p132">관리 되는 메타 데이터 서비스 응용 프로그램을 사용 하 여 콘텐츠 형식 게시를 설정 하 여 사이트 모음 간에 콘텐츠 형식을 공유 합니다. 콘텐츠 형식 게시는 콘텐츠 형식을 중앙에서 만들고 업데이트할 수 있으며, 업데이트를 여러 구독 사이트 모음 또는 웹 응용 프로그램에 게시할 수 있으므로 사이트 전체에서 일관 되 게 콘텐츠 및 메타 데이터를 관리 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p132">Share content types across site collections by using a Managed Metadata service application to set up content type publishing. Content type publishing helps you manage content and metadata consistently across your sites because content types can be created and updated centrally, and updates can be published out to multiple subscribing site collections or Web applications.</span></span>
  
## <a name="create-a-template-from-an-existing-policy-to-use-across-site-collections"></a><span data-ttu-id="690a9-278">사이트 모음에서 사용 하는 기존 정책에서 템플릿 만들기</span><span class="sxs-lookup"><span data-stu-id="690a9-278">Create a template from an existing policy to use across site collections</span></span>
<span data-ttu-id="690a9-279"><a name="__toc262125409"> </a></span><span class="sxs-lookup"><span data-stu-id="690a9-279"></span></span>

<span data-ttu-id="690a9-p133">정보 관리 정책을 정의한 다음 여러 사이트 모음에서 필요에 따라 사용할 서식 파일을 만들 수 있습니다. 이 방법은 정보 정책을 백업 하려는 경우에 사용 하거나, 콘텐츠 형식 게시를 사용 하 여 사이트 모음 간에 하나의 정책을 적용 하는 대체 방법으로 사용할 수도 있습니다. 한 사이트 모음에서 정책을 내보낸 다음 저장 된 위치 또는 다른 사이트 모음으로 가져오는 방법으로 정책 템플릿 또는 백업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p133">You can define an information management policy and then create a template from it to use as needed across multiple site collections. This method can be used if you want to have a backup of your information policies, or it can also be used as an alternate method to using content type publishing for applying one policy across site collections. You create a template or backup of the policy by exporting the policy from one site collection and then importing it to a saved location or to another site collection.</span></span>
  
> [!IMPORTANT]
>  <span data-ttu-id="690a9-p134">정책 템플릿 집합을 만드는 방법으로 내보내기/가져오기 기능을 사용 하는 경우에는 정책 .xml 파일에 고유한 식별자가 있다는 것을 염두에 두어야 합니다. 따라서이 고유 식별자를 변경 하지 않고 정책을 사이트에 두 번 이상 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p134">If you using the export/import feature as a way to make a set of policy templates, keep in mind that a unique identifier exists in the policy .xml file. Because of this, you cannot import that policy into a site more than once without changing this unique identifier.</span></span> 
  
### <a name="export-a-policy"></a><span data-ttu-id="690a9-285">정책 내보내기</span><span class="sxs-lookup"><span data-stu-id="690a9-285">Export a policy</span></span>
<span data-ttu-id="690a9-286"><a name="__toc260646790"> </a></span><span class="sxs-lookup"><span data-stu-id="690a9-286"></span></span>

1. <span data-ttu-id="690a9-287">사이트 모음 홈 페이지에서 사이트 설정 위치를 수행한 **설정**![작은 설정 기어를 선택 합니다. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) \> **사이트 설정**</span><span class="sxs-lookup"><span data-stu-id="690a9-287">On the site collection home page, choose **Settings**![Small Settings gear that took the place of Site Settings.](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png)\> **Site Settings**.</span></span>
    
    <span data-ttu-id="690a9-288">SharePoint 그룹에 연결 된 사이트에서 **설정을**클릭 하 고 **사이트 콘텐츠**를 클릭 한 다음 **사이트 설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-288">In a SharePoint group-connected site, click **Settings**, click **Site Contents**, and then click **Site Settings**.</span></span> 
    
2. <span data-ttu-id="690a9-289">사이트 설정 페이지의 **사이트 모음 관리** \> **콘텐츠 형식 정책 서식 파일**에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-289">On the Site Settings page, under **Site Collection Administration** \> **Content Type Policy Templates**.</span></span> 
  
![사이트 설정 페이지의 콘텐츠 형식 정책 서식 파일 링크](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. <span data-ttu-id="690a9-291">내보내려는 \> 정책을 하위 \> **내보내기**로 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-291">Choose the policy you want to export \> scroll to the bottom \> **Export**.</span></span>
    
4. <span data-ttu-id="690a9-p135">파일을 저장 하거나 열 것인지 묻는 메시지가 표시 되 면 **저장**을 선택한 다음 파일을 저장할 위치를 선택 합니다. 정책을 가져오는 사이트 모음에서 사용할 수 있는 위치를 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p135">At the prompt to save or open the file, choose **Save**, and then select a location to save the file to. Be sure to select a location that is available to the site collections that are importing the policy.</span></span>
    
5. <span data-ttu-id="690a9-294">다운로드 완료 대화 상자가 표시 되 면 **닫기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-294">When the Download Complete dialog is displayed, choose **Close**.</span></span>
    
### <a name="import-a-policy-to-a-different-site-collection"></a><span data-ttu-id="690a9-295">다른 사이트 모음으로 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="690a9-295">Import a policy to a different site collection</span></span>
<span data-ttu-id="690a9-296"><a name="__toc260646791"> </a></span><span class="sxs-lookup"><span data-stu-id="690a9-296"></span></span>

<span data-ttu-id="690a9-p136">정보 관리 정책을 가져오면 지정 된 사이트 모음 내의 사이트 또는 목록 수준에서 여러 콘텐츠 형식에 적용할 수 있습니다. 이 작업을 수행 하는 경우의 이점은 twofold을 사용 하 여 정책을 다시 정의 하 고 적용할 필요가 없으며, 정책을 한 곳에서 변경 하 여 정책 수정 작업을 보다 쉽게 관리할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-p136">Importing an information management policy enables you to apply it to multiple content types at the site or list level within any given site collection. The benefits of doing this are twofold: you don't have to re-define and apply the policy on each content type, and you can more easily manage policy modifications by making changes to the policy in just one place.</span></span>
  
1. <span data-ttu-id="690a9-299">정책을 적용 하려는 사이트 모음의 홈 페이지에서 사이트 설정의 위치를 선택한 **설정**![작은 설정 기어를 선택 합니다. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) \> **사이트 설정**</span><span class="sxs-lookup"><span data-stu-id="690a9-299">On the home page of the site collection to which you want to apply the policy, choose **Settings**![Small Settings gear that took the place of Site Settings.](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png)\> **Site Settings**.</span></span>
    
    <span data-ttu-id="690a9-300">SharePoint 그룹에 연결 된 사이트에서 **설정을**클릭 하 고 **사이트 콘텐츠**를 클릭 한 다음 **사이트 설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-300">In a SharePoint group-connected site, click **Settings**, click **Site Contents**, and then click **Site Settings**.</span></span> 
    
2. <span data-ttu-id="690a9-301">사이트 설정 페이지의 **사이트 모음 관리** \> **콘텐츠 형식 정책 서식 파일**에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-301">On the Site Settings page, under **Site Collection Administration** \> **Content Type Policy Templates**.</span></span>
    
3. <span data-ttu-id="690a9-302">정책 페이지 \> \*\*\*\* \> 에서 **찾아보기를** 클릭 하 여 정책의 XML 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-302">On the Policies page \> **Import** \> **Browse** to find the XML file for the policy.</span></span> 
    
4. <span data-ttu-id="690a9-303">정책이 저장 \> \*\*\*\* 된 XML 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-303">Select the XML file in which the policy has been saved \> **Open**.</span></span> 
    
5. <span data-ttu-id="690a9-304">사이트 모음 정책 가져오기 페이지 \> \*\*\*\* 에서 사이트 모음의 정책을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-304">On the Import a Site Collection Policy page \> **Import** to add the policy to the site collection.</span></span> 
    
<span data-ttu-id="690a9-305">이제 사이트 또는 목록 수준에서 하나 이상의 콘텐츠 형식에 가져온 정책을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="690a9-305">Your imported policy can now be applied to one or many content types at the site or list level.</span></span> 
  
[<span data-ttu-id="690a9-306">정보 관리 정책을 사용 하면 조직이 콘텐츠를 보존 하는 기간을 제어 하 고, 사용자가 콘텐츠를 사용 하는 작업을 감사 하 고, 문서에 바코드 또는 레이블을 추가할 수 있습니다. 정책은 법적 및 정부 규정 또는 내부 비즈니스 프로세스에 대 한 준수를 보장 하는 데 도움이 될 수 있습니다. 관리자는 문서 추적 방법 및 문서 보존 기간을 제어 하는 정책을 설정할 수 있습니다. 사이트 계층 구조에서 사이트 모음 내의 여러 콘텐츠 형식에 사용할 정책 만들기의 세 가지 위치에서 정보 관리 정책을 만들 수 있습니다. 사이트 콘텐츠 형식에 대 한 정책을 만듭니다. 목록 또는 라이브러리에 대 한 정책을 만듭니다. 자세한 내용은 정보 관리 정책 소개를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="690a9-306">Information management policies enable your organization to control how long to retain content, to audit what people do with content, and to add barcodes or labels to documents. A policy can help enforce compliance with legal and governmental regulations or internal business processes. As an administrator, you can set up a policy to control how to track documents and how long to retain documents.You can create an information management policy can at three different locations in the site hierarchy, from the broadest to the narrowest:Create a policy to use on multiple content types within a site collection.Create a policy for a site content type.Create a policy for a list or library.For more information, see Introduction to information management policies.</span></span>](create-info-mgmt-policies.md#__top)
  

