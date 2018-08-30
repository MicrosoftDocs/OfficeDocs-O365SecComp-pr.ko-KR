---
title: 정책 만들기 및 정보 관리 정책 적용
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/16/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 8ccac9e4-3a50-49fa-a95b-d186032a6ee3
description: 정보 관리 정책 사용자 콘텐츠를 수행할 작업을 감사 하 고 바코드를 추가 하려면 콘텐츠를 보존 기간을 제어 하 여 조직 또는 문서에 레이블을 사용 합니다. 정책을 내부 비즈니스 프로세스 또는 법률 및 정부 규정을 준수 하는 데 도움이 됩니다. 관리자로 설정할 수 있습니다는 정책을 문서를 추적 하는 방법을 제어 하 고 문서 보존 기간을 합니다.
ms.openlocfilehash: cc15b7d830e6c13e00045f7e4b672ac4a755a70e
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533184"
---
# <a name="create-and-apply-information-management-policies"></a><span data-ttu-id="4eae6-105">정책 만들기 및 정보 관리 정책 적용</span><span class="sxs-lookup"><span data-stu-id="4eae6-105">Create and apply information management policies</span></span>

<span data-ttu-id="4eae6-p102">정보 관리 정책 사용자 콘텐츠를 수행할 작업을 감사 하 고 바코드를 추가 하려면 콘텐츠를 보존 기간을 제어 하 여 조직 또는 문서에 레이블을 사용 합니다. 정책을 내부 비즈니스 프로세스 또는 법률 및 정부 규정을 준수 하는 데 도움이 됩니다. 관리자로 설정할 수 있습니다는 정책을 문서를 추적 하는 방법을 제어 하 고 문서 보존 기간을 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p102">Information management policies enable your organization to control how long to retain content, to audit what people do with content, and to add barcodes or labels to documents. A policy can help enforce compliance with legal and governmental regulations or internal business processes. As an administrator, you can set up a policy to control how to track documents and how long to retain documents.</span></span>
  
<span data-ttu-id="4eae6-109">광범위 한 사이트 계층 구조에서 서로 다른 세 위치에서 정보 관리 정책 수 있습니다를 만들 수는 가장 좁은에:</span><span class="sxs-lookup"><span data-stu-id="4eae6-109">You can create an information management policy can at three different locations in the site hierarchy, from the broadest to the narrowest:</span></span>
  
- <span data-ttu-id="4eae6-110">사이트 모음 내에서 여러 콘텐츠 형식을 사용 하 여 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-110">Create a policy to use on multiple content types within a site collection.</span></span>
    
- <span data-ttu-id="4eae6-111">사이트 콘텐츠 형식에 대 한 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-111">Create a policy for a site content type.</span></span>
    
- <span data-ttu-id="4eae6-112">목록 또는 라이브러리에 대 한 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-112">Create a policy for a list or library.</span></span>
    
<span data-ttu-id="4eae6-113">자세한 내용은 [정보 관리 정책 소개](intro-to-info-mgmt-policies.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4eae6-113">For more information, see [Introduction to information management policies](intro-to-info-mgmt-policies.md).</span></span>
  
## <a name="create-a-policy-for-multiple-content-types-within-a-site-collection"></a><span data-ttu-id="4eae6-114">사이트 모음 내에서 여러 콘텐츠 형식에 대 한 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="4eae6-114">Create a policy for multiple content types within a site collection</span></span>
<span data-ttu-id="4eae6-115"><a name="__toc261001590"> </a></span><span class="sxs-lookup"><span data-stu-id="4eae6-115"></span></span>

<span data-ttu-id="4eae6-p103">사이트 모음 내에서 특정 종류의 모든 문서에 적용 되는 정보 정책이 되도록 사이트 모음 수준에서 정책을 만드는 것이 좋습니다 하 고 콘텐츠 형식에 정책을 나중에 적용 합니다. 이 사이트 모음 정책 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p103">To ensure that an information policy is applied to all documents of a certain type within a site collection, consider creating the policy at the site collection level and then later apply the policy to content types. These are referred to as site collection policies.</span></span> 
  
1. <span data-ttu-id="4eae6-p104">사이트 모음 홈페이지에서 \> **설정**![제목 표시줄에서 SharePoint 2016 설정 단추입니다. ](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **사이트 설정**합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p104">On the site collection home page \> **Settings**![SharePoint 2016 Settings button on title bar.](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **Site Settings**.</span></span>
    
    <span data-ttu-id="4eae6-120">SharePoint 그룹에 연결 된 사이트에서 **설정**을 클릭 하 고 **사이트 콘텐츠**를 클릭 한 다음 **사이트 설정**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-120">In a SharePoint group-connected site, click **Settings**, click **Site Contents**, and then click **Site Settings**.</span></span> 
    
2. <span data-ttu-id="4eae6-121">사이트 설정 페이지의 **사이트 모음 관리** 에서 \> **콘텐츠 형식에 대 한 정책 서식 파일**입니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-121">On the Site Settings page, under **Site Collection Administration** \> **Content Type Policy Templates**.</span></span> 
  
![사이트 설정 페이지에서 콘텐츠 형식 정책 서식 파일 링크](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. <span data-ttu-id="4eae6-123">정책 페이지에서 \> **만들기**.</span><span class="sxs-lookup"><span data-stu-id="4eae6-123">On the Policies page \> **Create**.</span></span> 
    
4. <span data-ttu-id="4eae6-124">이름 및 정책에 대 한 설명을 입력 하 고에 대 한 란 정책을 사용자에 게 설명 하는 간단한 정책 설명을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-124">Enter a name and description for the policy, and then write a brief policy statement that explains to users what the policy is for.</span></span>
    
5. <span data-ttu-id="4eae6-125">정책을 사용 하 여 연결 하려는 기능을 설정 하는 방법을 설명 하는 사이트 콘텐츠 형식에 대 한 정책을 만드는 방법에 대해 다음 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4eae6-125">See the next section on creating policies for a site content type to learn how to set up the features you want to associate with the policy.</span></span> 
    
6. <span data-ttu-id="4eae6-126">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-126">Choose **OK**.</span></span>
    
## <a name="create-a-policy-for-a-site-content-type"></a><span data-ttu-id="4eae6-127">사이트 콘텐츠 형식에 대 한 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="4eae6-127">Create a policy for a site content type</span></span>
<span data-ttu-id="4eae6-128"><a name="__create_a_policy"> </a></span><span class="sxs-lookup"><span data-stu-id="4eae6-128"></span></span>

<span data-ttu-id="4eae6-p105">콘텐츠 형식에 정보 관리 정책을 추가 (영문)을 통해 손쉽게 여러 목록이 나 라이브러리에 정책 기능을 연결 합니다. 기존 정보 관리 정책을 콘텐츠 형식에 추가 하거나 고유한 정책을 개별 콘텐츠 형식에 특정 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p105">Adding an information management policy to a content type makes it easy to associate policy features with multiple lists or libraries. You can choose to add an existing information management policy to a content type or create a unique policy specific to an individual content type.</span></span>
  
 <span data-ttu-id="4eae6-p106">또한 목록에 관련 된 콘텐츠 형식에 정보 관리 정책에 추가할 수 있습니다. 콘텐츠 형식을 사용 하는 해당 목록에 있는 항목에만 해당 정책을 적용 하는 효과가이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p106">You can also add an information management policy to a content type that is specific to lists. This has the effect of applying the policy only to items in that list that are using the content type.</span></span> 
  
1. <span data-ttu-id="4eae6-p107">사이트 모음 홈페이지에서 \> **설정**![제목 표시줄에서 SharePoint 2016 설정 단추입니다. ](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **사이트 설정**합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p107">On the site collection home page \> **Settings**![SharePoint 2016 Settings button on title bar.](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **Site Settings**.</span></span>
    
    <span data-ttu-id="4eae6-135">SharePoint 그룹에 연결 된 사이트에서 **설정**을 클릭 하 고 **사이트 콘텐츠**를 클릭 한 다음 **사이트 설정**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-135">In a SharePoint group-connected site, click **Settings**, click **Site Contents**, and then click **Site Settings**.</span></span> 
    
2. <span data-ttu-id="4eae6-136">사이트 설정 페이지의 **웹 디자이너 갤러리** 에서 \> **사이트 콘텐츠 형식**입니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-136">On the Site Settings page, under **Web Designer Galleries** \> **Site content types**.</span></span>
  
![사이트 설정 페이지에서 사이트 콘텐츠 형식 링크](media/6f6fa51f-15d7-4782-b06f-a7b36e874cd3.png)
  
3. <span data-ttu-id="4eae6-138">사이트 콘텐츠 형식 설정 페이지에서 하기 위한 정책을 추가 하려는 콘텐츠 형식을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-138">On the Site Content Type Settings page, select the content type that you want to add a policy to.</span></span>
    
4. <span data-ttu-id="4eae6-139">사이트 콘텐츠 형식 페이지의 **설정** 에서 \> **정보 관리 정책 설정**합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-139">On the Site Content Type page, under **Settings** \> **Information management policy settings**.</span></span>
    
5. <span data-ttu-id="4eae6-140">정책 편집 페이지에서 이름 및 정책에 대 한 설명을 입력 하 고에 대 한 란 정책을 사용자에 게 설명 하는 한 간략 한 설명을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-140">On the Edit Policy page, enter a name and description for the policy, and then write a brief description that explains to users what the policy is for.</span></span>
    
6. <span data-ttu-id="4eae6-141">다음 섹션에서는 사용자의 정보 관리 정책에 추가 하려는 개별 정책 기능을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-141">In the next sections, select the individual policy features that you want to add to your information management policy.</span></span> 
  
![콘텐츠 정책 유형](media/19fcb8a3-974b-40d3-a13f-b76088d122f8.png)
  
7. <span data-ttu-id="4eae6-143">이 정책이 적용 되는 문서와 항목에 대 한 보존 기간을 지정 하려면 **보존 사용**을 선택 하 고 보존 기간 및 항목이 만료 될 때 발생 시킬 수 있는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-143">To specify a retention period for documents and items that are subject to this policy, choose **Enable Retention**, and then specify the retention period and the actions that you want to occur when the items expire.</span></span>
    
    <span data-ttu-id="4eae6-144">보존 기간을 지정 하려면</span><span class="sxs-lookup"><span data-stu-id="4eae6-144">To specify a retention period</span></span>
    
||||||<span data-ttu-id="4eae6-145">**1입니다.**</span><span class="sxs-lookup"><span data-stu-id="4eae6-145">**1.**</span></span>|<span data-ttu-id="4eae6-146">\* \* 선택 \* \* 레코드에 대 한 보존 스테이지 추가 하려면... \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4eae6-146">**Choose **Add a retention stage for records…****</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||<span data-ttu-id="4eae6-147">2.</span><span class="sxs-lookup"><span data-stu-id="4eae6-147">2.</span></span>  <br/> | <span data-ttu-id="4eae6-p108">문서 또는 항목에 만료 되도록 설정 하는 시간을 지정 하는 보존 기간 옵션을 선택 합니다. 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p108">Select a retention period option to specify when documents or items are set to expire. Do one of the following:  </span></span><br/>  <span data-ttu-id="4eae6-150">**이벤트** 에서 날짜 속성을 기준으로 만료 날짜를 설정 하려면 \> **이 단계는 항목의 날짜 속성을 해제 기반**, 및 문서 또는 항목 작업 (예 작성 또는 수정)을 선택 합니다 및이 동작 (후 시간 예, 일, 월 또는 년 수) 항목이 만료 하려는 경우.</span><span class="sxs-lookup"><span data-stu-id="4eae6-150">To set the expiration date based on a date property, under **Event** \> **This stage is based off a date property on the item**, and then select the document or item action (for example, Created or Modified) and the increment of time after this action (for example, the number of days, months, or years) when you want the item to expire.</span></span>  <br/>  <span data-ttu-id="4eae6-151">만료를 결정 하려면 사용자 지정 보존 수식을 사용 하 **여이 서버에 설치 사용자 지정 보존 수식을 설정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-151">To use a custom retention formula to determine expiration, choose **Set by a custom retention formula installed on this server**.</span></span>  <br/> <span data-ttu-id="4eae6-152">> [!NOTE]>이 옵션은 관리자에 게 문의 하 여 사용자 지정 수식 설정 된 경우에 사용할 수만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-152">> [!NOTE]>  This option is only available if a custom formula has been set up by your administrator.</span></span>           |
||||||<span data-ttu-id="4eae6-153">3.</span><span class="sxs-lookup"><span data-stu-id="4eae6-153">3.</span></span>  <br/> |<span data-ttu-id="4eae6-p109">**워크플로 시작** 옵션은 목록, 라이브러리 또는 연결 된 워크플로가 이미 콘텐츠 형식에 대 한 정책을 정의 하는 경우에 사용할 수 있습니다. 워크플로 선택 중에서 선택할 제공 다음 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p109">The **Start a workflow** option is available only if you are defining a policy for a list, library, or content type that already has a workflow associated with it. You will then be given a choice of workflows to choose from.  </span></span><br/> |
||||||<span data-ttu-id="4eae6-156">4.</span><span class="sxs-lookup"><span data-stu-id="4eae6-156">4.</span></span>  <br/> |<span data-ttu-id="4eae6-157">**되풀이 방법** 섹션에서 **이 단계 작업...을 반복** 을 선택합니다 및 작업을 다시 발생 빈도 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-157">In the **Recurrence** section, select **Repeat this stage's action…** and enter how often you want the action to reoccur.</span></span>  <br/> <span data-ttu-id="4eae6-p110">> [!NOTE]>이 옵션은 사용자가 선택한 작업을 반복 될 수 있는 경우에 사용할 수만 있습니다. 예 **를 영구적으로 삭제**하는 작업에 대 한 되풀이 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p110">> [!NOTE]>  This option is only available if the action you selected can be repeated. For example, you cannot set recurrence for the action **Permanently Delete**.</span></span>           |
||||||<span data-ttu-id="4eae6-160">5.</span><span class="sxs-lookup"><span data-stu-id="4eae6-160">5.</span></span>  <br/> |<span data-ttu-id="4eae6-161">**확인**을 선택 했습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-161">Chose **OK**.</span></span>  <br/> |
   
1. <span data-ttu-id="4eae6-162">문서 및이 정책이 적용 되는 항목에 대 한 감사를 활성화 하려면 **감사 사용**을 선택 하 고 감사할 이벤트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-162">To enable auditing for the documents and items that are subject to this policy, choose **Enable Auditing**, and then specify the events you want to audit.</span></span>
    
    <span data-ttu-id="4eae6-163">감사를 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="4eae6-163">To enable auditing</span></span>
    
||||||<span data-ttu-id="4eae6-164">1.\* \* \*</span><span class="sxs-lookup"><span data-stu-id="4eae6-164">****1.****</span></span>|<span data-ttu-id="4eae6-165">정책 편집 페이지에서 \* \* **아래에서** **감사** **\>** **감사 활성화** \* *, 다음 선택 감사를 유지 하려는 이벤트 옆에 있는 확인란 후행 for.* \* \* 및</span><span class="sxs-lookup"><span data-stu-id="4eae6-165">****On the Edit Policy page,** **under** **Auditing** **\>** **Enable auditing** **, and then select the check boxes next to the events you want to keep an audit trail for.****</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||<span data-ttu-id="4eae6-166">**2입니다.**</span><span class="sxs-lookup"><span data-stu-id="4eae6-166">**2.**</span></span> <br/> |<span data-ttu-id="4eae6-167">**문서에 이러한 바코드 삽입 여부를 확인 하려면** **선택** **저장 또는 인쇄 전에 바코드 삽입를 묻는 메시지를 사용자** **.**</span><span class="sxs-lookup"><span data-stu-id="4eae6-167">**To prompt users to insert these barcodes into documents,** **choose** **Prompt users to insert a barcode before saving or printing** **.**</span></span> <br/> |
||||||<span data-ttu-id="4eae6-168">**3입니다.**</span><span class="sxs-lookup"><span data-stu-id="4eae6-168">**3.**</span></span> <br/> |<span data-ttu-id="4eae6-169">**선택** **확인** * * 정책에 감사 기능을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-169">**Choose** **OK** ** to apply the auditing feature to the policy.</span></span> ** <br/> |
|||||||<span data-ttu-id="4eae6-p111">감사 정책 기능에는 조직에서는을 만들고 작업 목록, 문제점 목록, 토론 그룹 및 달력 등의 목록 항목 및 문서에 대 한 감사 내역을 분석할 수 있습니다. 이 정책 기능은 콘텐츠 표시, 편집 또는 삭제와 같은 이벤트를 기록 하는 감사 로그를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p111">The Auditing Policy feature enables organizations to create and analyze audit trails for documents and to list items such as task lists, issues lists, discussion groups, and calendars. This policy feature provides an audit log that records events, such as when content is viewed, edited, or deleted.</span></span>  <br/> |
|||||||<span data-ttu-id="4eae6-p112">감사 사용 하는 경우 정보 관리 정책의 일부로 관리자는 Microsoft Excel에 기반 하 고 현재 사용 현황 요약 하는 정책 사용 현황 보고서에서 감사 데이터를 볼 수 있습니다. 관리자는 이러한 보고서를 사용 하 여 조직 내에서 정보가 사용 되는 방식을 결정 수 있습니다. 이러한 보고서는 조직에서 시스템을 확인 및 규정 준수 문서화 하거나 잠재적인 문제를 조사에 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p112">When auditing is enabled as part of an information management policy, administrators can view the audit data in policy usage reports that are based in Microsoft Excel and that summarize current usage. Administrators can use these reports to determine how information is being used within the organization. These reports can also help organizations to verify and document their regulatory compliance or to investigate potential concerns.</span></span>  <br/> |
|||||||<span data-ttu-id="4eae6-175">감사 로그에는 이벤트 이름, 이벤트의 날짜 및 시간, 해당 작업을 수행한 사용자의 시스템 이름과 같은 정보가 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-175">The audit log records the following information: event name, date and time of the event, and system name of the user who performed the action.</span></span>  <br/> |
   
1. <span data-ttu-id="4eae6-p113">바코드 정책의 일부로 사용 하는 경우 문서 속성에 추가 하 고 바코드 적용 되는 문서의 머리글 영역에 표시 되는 있습니다. 레이블, 마찬가지로 바코드도 수동으로에서 제거할 수 문서입니다. 사용자에 게를 인쇄 하거나 항목을 저장 하는 경우 바코드를 포함할지 묻는 또는 바코드를 수동으로 삽입 해야 하는 경우에 2010 년 **삽입** 탭을 사용 하 여 Office 릴리스 프로그램 있는지 여부를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p113">When barcodes are enabled as part of a policy, they are added to document properties and displayed in the header area of the document to which the barcode is applied. Like labels, barcodes can also be manually removed from a document. You can specify whether users should be prompted to include the barcode when printing or saving an item or if the barcode should be inserted manually using the **Insert** tab in 2010 Office release programs.</span></span> 
    
    <span data-ttu-id="4eae6-179">바코드를 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="4eae6-179">To enable barcodes</span></span>
    
||||||<span data-ttu-id="4eae6-180">1.\* \* \*</span><span class="sxs-lookup"><span data-stu-id="4eae6-180">****1.****</span></span>|<span data-ttu-id="4eae6-181">**정책 편집 페이지의 **바코드** 아래에서\> **바코드 사용**합니다.**</span><span class="sxs-lookup"><span data-stu-id="4eae6-181">**On the Edit Policy page, under **Barcodes**\> **Enable Barcodes**.**</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||<span data-ttu-id="4eae6-182">**2입니다.**</span><span class="sxs-lookup"><span data-stu-id="4eae6-182">**2.**</span></span> <br/> |<span data-ttu-id="4eae6-183">사용자가 문서에 이러한 바코드를 삽입할 수의 메시지를 표시 하려면 **저장 또는 인쇄 전에 바코드 삽입 여부 확인 사용자**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-183">To prompt users to insert these barcodes into documents, choose **Prompt users to insert a barcode before saving or printing**.</span></span>  <br/> |
||||||<span data-ttu-id="4eae6-184">**3입니다.**</span><span class="sxs-lookup"><span data-stu-id="4eae6-184">**3.**</span></span> <br/> |<span data-ttu-id="4eae6-185">정책에 바코드 기능을 적용 하려면 **확인** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-185">Choose **OK** to apply the barcode feature to the policy.</span></span>  <br/> |
|||||||
 <span data-ttu-id="4eae6-p114">바코드 정책 코드 39 표준 바코드를 생성 합니다. 각 바코드 이미지 바코드 값을 나타내는 바코드 기호 아래에 텍스트를 포함 합니다. 이렇게 하면 바코드 데이터를 사용할 수 없는 하드웨어를 검사 하는 경우에 사용할 수 있습니다. 사용자가 사이트에서 항목을 찾을 수 있는 검색 상자에 바코드 번호를 수동으로 입력 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p114">The barcode policy generates Code 39 standard barcodes. Each barcode image includes text below the barcode symbol that represents the barcode value. This enables the barcode data to be used even when scanning hardware is not available. Users can manually type the barcode number into the search box to locate the item on a site.</span></span>  <br/> |
   
1. <span data-ttu-id="4eae6-190">이 정책이 적용 되는 문서에 레이블을 포함 하려면, **레이블 사용**선택 하 고 레이블에 대 한 원하는 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-190">To require that documents that are subject to this policy have labels, choose **Enable Labels**, and then specify the settings that you want for the labels.</span></span>
    
    <span data-ttu-id="4eae6-191">레이블을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="4eae6-191">To enable labels</span></span>
    
||||||<span data-ttu-id="4eae6-192">**1입니다.**</span><span class="sxs-lookup"><span data-stu-id="4eae6-192">**1.**</span></span>|<span data-ttu-id="4eae6-193">* * 문서에 레이블을 추가 하는 사용자를 요구 하는 경우 하려면 **저장 또는 인쇄 전에 레이블 삽입를 묻는 메시지를 사용자**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-193">**To require users to add a label to a document, choose **Prompt users to insert a label before saving or printing**.</span></span>  <br/> <span data-ttu-id="4eae6-194">> [!NOTE]> 레이블을 선택적으로 하려는 경우에이 확인란을 선택 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="4eae6-194">> [!NOTE]>  If you want labels to be optional, do not select this check box.</span></span>        **|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||<span data-ttu-id="4eae6-195">2.</span><span class="sxs-lookup"><span data-stu-id="4eae6-195">2.</span></span>  <br/> |<span data-ttu-id="4eae6-196">삽입 한 후에 변경할 수 없도록 레이블을 잠그려면, **레이블 추가 후 변경 금지를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-196">To lock a label so that it cannot be changed after it has been inserted, choose **Prevent changes to labels after they are added**.</span></span>  <br/>  <span data-ttu-id="4eae6-p115">이 설정은 Word, Excel, PowerPoint 등 클라이언트 응용 프로그램 내에 있는 항목에 레이블을 삽입 한 후 업데이트에서 레이블 텍스트를 방지 합니다. 업데이트할 때이 문서 또는 항목에 대 한 속성은 업데이트 레이블을 하려는 경우에이 확인란을 선택 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p115">This setting prevents the label text from updating once the label has been inserted into an item within a client application such as Word, Excel, or PowerPoint. If you want the label to be updated when the properties for this document or item are updated, do not select this check box.  </span></span><br/> |
||||||<span data-ttu-id="4eae6-199">3.</span><span class="sxs-lookup"><span data-stu-id="4eae6-199">3.</span></span>  <br/> |<span data-ttu-id="4eae6-p116">레이블 형식 상자에서 표시할 원하는대로 % 레이블에 대 한 텍스트를 입력 합니다. 레이블 길이 최대 255 자 수 있으며 각 최대 10 개의 열 참조, 포함 될 수 있습니다. 레이블 형식을 만들려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p116">In the Label format box, enter the text for the label as you want it to be displayed. Labels can contain up to 10 column references, each of which can be up to 255 characters long. To create the format for your label, do the following:</span></span>  <br/> <span data-ttu-id="4eae6-p117">레이블 표시 하도록 하려면 순서에서에 포함할 열의 이름을 입력 합니다. 열 이름을 중괄호 묶습니다 ({}) 정책 편집 페이지에서 예제와 같이, 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p117">Type the names of the columns that you want to include in the label in the order in which you want them to appear. Enclose the column names in curly brackets ({}), as shown in the example on the Edit Policy page.</span></span>  <br/> <span data-ttu-id="4eae6-205">정책 편집 페이지에서 예제와 같이 중괄호 바깥쪽 열을 식별 하는 단어를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-205">Type words to identify the columns outside the brackets, as shown in the example on the Edit Policy page.</span></span>  <br/> |
||||||<span data-ttu-id="4eae6-206">4.</span><span class="sxs-lookup"><span data-stu-id="4eae6-206">4.</span></span>  <br/> |<span data-ttu-id="4eae6-207">줄바꿈을 추가 하려면 추가할 나타나려면 줄바꿈 **\n** 를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-207">To add a line break, enter **\n** where you want the line break to appear.</span></span>  <br/> |
||||||<span data-ttu-id="4eae6-208">5.</span><span class="sxs-lookup"><span data-stu-id="4eae6-208">5.</span></span>  <br/> |<span data-ttu-id="4eae6-209">글꼴 크기 및 받고 왼쪽, 가운데 또는 오른쪽 문서 내에서 레이블을 배치할 위치를 지정 하는 스타일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-209">Select the font size and style that you want, and specify whether you want the label positioned left, center, or right within the document.</span></span>  <br/>  <span data-ttu-id="4eae6-p118">글꼴 및 사용자의 컴퓨터에서 사용할 수 있는 스타일을 선택 합니다. 글꼴 크기 얼마나 많은 텍스트 레이블을 표시 하는 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p118">Select a font and style that are available on the users' computers. The size of the font affects how much text can be displayed on the label.</span></span>  <br/> |
||||||<span data-ttu-id="4eae6-212">6.</span><span class="sxs-lookup"><span data-stu-id="4eae6-212">6.</span></span>  <br/> |<span data-ttu-id="4eae6-p119">레이블의 너비와 높이 입력 합니다. 20 인치를 인치에서 까지입니다 레이블 높이 및 20 인치 레이블 너비를 인치에서 사이의 수 있습니다. 레이블 텍스트는 항상 세로 레이블 이미지 내에서 가운데에 맞춥니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p119">Enter the height and width of the label. Label height can range from .25 inches to 20 inches, and label width can range from .25 inches to 20 inches. Label text is always vertically centered within the label image.</span></span>  <br/> |
||||||<span data-ttu-id="4eae6-216">7.</span><span class="sxs-lookup"><span data-stu-id="4eae6-216">7.</span></span>  <br/> |<span data-ttu-id="4eae6-217">레이블 콘텐츠를 미리보려면 **새로고침** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-217">Choose **Refresh** to preview the label content.</span></span>  <br/> |
   
1. <span data-ttu-id="4eae6-218">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-218">Choose **OK**.</span></span>
    
## <a name="create-a-policy-for-a-list-library-or-folder-location-based-retention-policy"></a><span data-ttu-id="4eae6-219">목록, 라이브러리 또는 폴더에 대한 정책(위치 기반 보존 정책) 만들기</span><span class="sxs-lookup"><span data-stu-id="4eae6-219">Create a policy for a list, library or folder (location-based retention policy)</span></span>
<span data-ttu-id="4eae6-220"><a name="__create_a_policy"> </a></span><span class="sxs-lookup"><span data-stu-id="4eae6-220"></span></span>

<span data-ttu-id="4eae6-p120">특정 목록, 라이브러리 또는 폴더에만 적용 되는 보존 정책을 정의할 수 있습니다. 그러나 이러한 방식으로 보존 정책을 만들면이 정책을 다른 목록, 라이브러리, 폴더 또는 사이트에서 다시 사용할 수 없습니다 및 사이트 모음 정책 기반 위치 정책을 적용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p120">You can define a retention policy that applies only to a specific list, library or folder. However, if you create a retention policy this way, you cannot reuse this policy on other lists, libraries, folders or sites, and you cannot apply a site collection policy to a location based policy.</span></span>
  
<span data-ttu-id="4eae6-p121">모든 유형의 단일 위치에서 콘텐츠를 단일 보존 정책을 적용 하려는 경우 위치 기반 보존을 사용 하려는 가능성이 높습니다. 대부분의 경우 모든 콘텐츠 형식에 대 한 보존 정책을 지정 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p121">If you want to apply a single retention policy to all types of content in a single location, you will most likely want to use location-based retention. In most other cases, you will want to verify that a retention policy is specified for all content types.</span></span>
  
 <span data-ttu-id="4eae6-225">각 하위 폴더 상속 및 하위 수준에서 새 보존 정책을 정의 하도록 선택 하지 않으면 부모 보존 정책을 상속 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-225">Each subfolder inherits the retention policy of its parent, unless you choose to break inheritance and define a new retention policy at the child level.</span></span> 
  
<span data-ttu-id="4eae6-226">목록 또는 라이브러리에 정보 관리 정책 보존 이외의 정의 하려는 경우 해당 목록이 나 라이브러리와 연결 된 각 개별 목록 콘텐츠 형식에 대 한 정보 관리 정책을 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-226">If you want to define an information management policy other than retention to a list or library, you need to define an information management policy for each individual list content type associated with that list or library.</span></span>
  
 <span data-ttu-id="4eae6-p122">언제 든 지 목록 또는 라이브러리에 대 한 정책을 위치를 기반으로 콘텐츠 형식에서 전환 하려는 경우에 보존 정책에만 위치 기반 정책으로 사용 됩니다. 다른 모든 관리 정책 (감사, 바코드, 및 바코드) 연결 된 콘텐츠 형식에서 상속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p122">If at any point you decide to switch from content type to location-based policies for a list or library, only the retention policy will be used as the location-based policy. All other management policies (audits, barcodes, and barcodes) will be inherited from the associated content types.</span></span> 
  
 <span data-ttu-id="4eae6-p123">위치를 기반으로 정책은 라이브러리 및 폴더 기반 보존 기능을 비활성화 하 여 사이트 모음에 대 한 비활성화할 수 있습니다. 이 통해 사이트 모음 관리자가 해당 콘텐츠 형식 정책 목록 관리자의 기준 위치 정책에 의해 재정의 되지 않도록 할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p123">Location based policies can be disabled for a site collection by deactivating the Library and Folder Based Retention feature. This enables site collection administrators to ensure that their content type policies are not overridden by a list administrator's location based policies.</span></span> 
  
<span data-ttu-id="4eae6-231">목록 또는 라이브러리에 대 한 정보 관리 정책 설정을 변경 하려면 목록 관리 권한이 최소한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-231">You need at least the Manage Lists permission to change the information management policy settings for a list or library.</span></span>
  
1. <span data-ttu-id="4eae6-232">정보 관리 정책을 지정 하려면 목록 또는 라이브러리로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-232">Navigate to the list or library for which you want to specify an information management policy.</span></span> 
    
2. <span data-ttu-id="4eae6-233">리본 메뉴에서 **라이브러리** 또는 **목록** 탭을 선택 \> **라이브러리 설정** 또는 **목록 설정**합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-233">On the ribbon, choose the **Library** or **List** tab \> **Library Settings** or **List Settings**.</span></span>
    
    <span data-ttu-id="4eae6-234">SharePoint Online에서 **설정** 을 클릭 한 다음 **목록 설정** 또는 **라이브러리 설정**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-234">In SharePoint Online, click **Settings** and then click **List settings** or **Library settings**.</span></span> 
    
3. <span data-ttu-id="4eae6-235">**사용 권한 및 관리에서** \> **정보 관리 정책 설정**합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-235">Under **Permissions and Management**\> **Information management policy settings**.</span></span>
  
![문서 라이브러리에 대 한 설정 페이지에서 정보 관리 정책 링크](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. <span data-ttu-id="4eae6-237">정보 관리 정책 설정 페이지에서 목록 또는 라이브러리에 대 한 보존의 원본 라이브러리 및 폴더에 설정 되어있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-237">On the Information Management Policy Settings page, make sure that the source of retention for the list or library is set to Library and Folders.</span></span> 
  
<span data-ttu-id="4eae6-p124">**콘텐츠 형식** 은 원본으로 표시 하는 경우 **원본 변경을**클릭 하 고 **라이브러리 및 폴더를**클릭 합니다. 콘텐츠 형식 보존 정책이 무시 된다는 경고가 표시 됩니다. **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p124">If **Content Type** appears as the source, click **Change Source**, and then click **Library and Folders**. You are alerted that content type retention policies will be ignored. Choose **OK**.</span></span> 
    
5. <span data-ttu-id="4eae6-241">**라이브러리 기반 보존 일정**정책 편집 페이지에서 만들려는 정책에 대 한 간략 한 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-241">On the Edit Policy page, under **Library Based Retention Schedule**, enter a brief description for the policy you are creating.</span></span> 
    
6. <span data-ttu-id="4eae6-242">**추가 보존 단계...** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-242">Choose **Add a retention stage…**</span></span>
    
     <span data-ttu-id="4eae6-243">레코드를 선택할 수 있습니다 레코드 옵션에 대 한 정의 다른 보존 단계를 선택 하 여 레코드에 대 한 서로 다른 보존 정책 정의를 메모 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-243">Note that under Records, you can choose to define different retention policies for records by selecting the Define different retention stages for records option.</span></span> 
    
7. <span data-ttu-id="4eae6-p125">단계 속성 대화 상자에서 문서 또는 항목 만료 되도록 설정 되는 시기를 지정 하려면 보존 기간 옵션을 선택 합니다. 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p125">In the Stage properties dialog, select a retention period option to specify when documents or items are set to expire. Do one of the following:</span></span>
    
  - <span data-ttu-id="4eae6-246">**이벤트** 에서 날짜 속성을 기준으로 만료 날짜를 설정 하려면 \> **이 단계는 항목의 날짜 속성을 해제 기반**, 및 문서 또는 항목 작업 (예 작성 또는 수정)을 선택 합니다 및이 동작 (후 시간 예, 일, 월 또는 년 수) 항목이 만료 하려는 경우.</span><span class="sxs-lookup"><span data-stu-id="4eae6-246">To set the expiration date based on a date property, under **Event** \> **This stage is based off a date property on the item**, and then select the document or item action (for example, Created or Modified) and the increment of time after this action (for example, the number of days, months, or years) when you want the item to expire.</span></span> 
    
  - <span data-ttu-id="4eae6-247">만료를 결정 하려면 사용자 지정 보존 수식을 사용 하 **여이 서버에 설치 사용자 지정 보존 수식을 설정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-247">To use a custom retention formula to determine expiration, choose **Set by a custom retention formula installed on this server**.</span></span> 
    
    > [!NOTE]
    >  <span data-ttu-id="4eae6-248">이 옵션은 관리자에 게 문의 하 여 사용자 지정 수식 설정 된 경우에 사용할 수만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-248">This option is only available if a custom formula has been set up by your administrator.</span></span> 
  
  - <span data-ttu-id="4eae6-p126">**동작**문서나 항목이 만료 될 때 원하는 항목을 지정 합니다. 특정 동작을 문서 또는 항목 (예: 삭제) 수행을 사용 하려면 목록에서 동작을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p126">Under **Action**, specify what you want to happen when the document or item expires. To enable a specific action to happen to the document or item (such as deletion), select an action from the list.</span></span> 
    
8. <span data-ttu-id="4eae6-p127">**워크플로 시작** 옵션은 목록, 라이브러리 또는 연결 된 워크플로가 이미 콘텐츠 형식에 대 한 정책을 정의 하는 경우에 사용할 수 있습니다. 워크플로 선택 중에서 선택할 제공 다음 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p127">The **Start a workflow** option is available only if you are defining a policy for a list, library, or content type that already has a workflow associated with it. You will then be given a choice of workflows to choose from.</span></span> 
    
9. <span data-ttu-id="4eae6-253">**되풀이**에서 **이 단계 작업...을 반복** 선택 및 작업을 다시 발생 빈도 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-253">Under **Recurrence**, choose **Repeat this stage's action…** and enter how often you want the action to reoccur.</span></span> 
    
    > [!NOTE]
    >  <span data-ttu-id="4eae6-p128">이 옵션은 사용자가 선택한 작업을 반복 될 수 있는 경우에 사용할 수만 있습니다. 예 **를 영구적으로 삭제**하는 작업에 대 한 되풀이 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p128">This option is only available if the action you selected can be repeated. For example, you cannot set recurrence for the action **Permanently Delete**.</span></span> 
  
10. <span data-ttu-id="4eae6-256">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-256">Choose **OK**.</span></span>
    
## <a name="apply-a-site-collection-policy-to-a-content-type"></a><span data-ttu-id="4eae6-257">콘텐츠 형식에 사이트 모음 정책 적용</span><span class="sxs-lookup"><span data-stu-id="4eae6-257">Apply a site collection policy to a content type</span></span>
<span data-ttu-id="4eae6-258"><a name="__apply_a_site"> </a></span><span class="sxs-lookup"><span data-stu-id="4eae6-258"></span></span>

<span data-ttu-id="4eae6-p129">정보 관리 정책을 이미 만들어진 사이트에 대 한 사이트 모음 정책으로 콘텐츠 형식에 정책 중 하나를 적용할 수 있습니다. 이 작업을 수행 하 여 동일한 상위 콘텐츠 형식 공유 하지 않는 사이트 모음에서 여러 콘텐츠 형식에 동일한 정책을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p129">If information management policies have already been created for your site as site collection policies, you can apply one of the policies to a content type. By doing this, you can apply the same policy to multiple content types in a site collection that do not share the same parent content type.</span></span>
  
 <span data-ttu-id="4eae6-p130">사이트 모음에서 여러 콘텐츠 형식에 정책을 적용 하려는 하 고 관리 되는 메타 데이터 서비스를 구성 해야, 수 있는 콘텐츠 형식 게시를 게시할 때 사용할 수행 하는 경우 여러 사이트 모음에 정보 관리 정책입니다. 자세한 내용은 [사이트 모음 전체에서 콘텐츠 형식에 정책을 적용](create-info-mgmt-policies.md#__apply_a_policy) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p130">If you want to apply policies to multiple content types in a site collection, and you have a Managed Metadata Service configured, you can use Content Type Publishing to publish out information management polices to multiple site collections. See the section [Apply a policy to content types across site collections](create-info-mgmt-policies.md#__apply_a_policy) for more information.</span></span> 
  
1. <span data-ttu-id="4eae6-263">정책을 적용 하려면 콘텐츠 형식이 포함 라이브러리 또는 목록으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-263">Navigate to the list or library that contains the content type to which you want to apply a policy.</span></span>
    
2. <span data-ttu-id="4eae6-264">리본 메뉴에서 **라이브러리** 또는 **목록** 탭을 선택 \> **라이브러리 설정** 또는 **목록 설정**합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-264">On the ribbon, choose the **Library** or **List** tab \> **Library Settings** or **List Settings**.</span></span>
    
    <span data-ttu-id="4eae6-265">SharePoint Online에서 **설정** 을 클릭 한 다음 **목록 설정** 또는 **라이브러리 설정**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-265">In SharePoint Online, click **Settings** and then click **List settings** or **Library settings**.</span></span> 
    
3. <span data-ttu-id="4eae6-266">**사용 권한 및 관리에서** \> **정보 관리 정책 설정**합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-266">Under **Permissions and Management** \> **Information management policy settings**.</span></span>
  
![문서 라이브러리에 대 한 설정 페이지에서 정보 관리 정책 링크](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. <span data-ttu-id="4eae6-268">정책 소스 설정 되어있는지 확인 하 고 **콘텐츠 형식 정책** 을 선택 아래에서 **콘텐츠 형식**정책을 적용 하려면 콘텐츠 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-268">Verify that the policy source is set to **Content Types**, and under **Content Type Policies** select the content type you want to apply the policy to.</span></span> 
    
5. <span data-ttu-id="4eae6-269">**정책 지정** 에서 \> **사이트 모음 정책 사용**을 클릭 한 다음 선택 목록에서 적용 하려는 하는 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-269">Under **Specify the Policy** \> **Use a site collection policy**, and then select the policy that you want to apply from the list.</span></span> 
    
    > [!NOTE]
    >  <span data-ttu-id="4eae6-270">**사이트 모음 정책 사용** 옵션을 사용할 수 없는 경우 사이트 모음 정책이 사이트 모음에 대해 정의 된 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-270">If the **Use a site collection policy** option is not available, no site collection policies have been defined for the site collection.</span></span> 
  
6. <span data-ttu-id="4eae6-271">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-271">Choose **OK**.</span></span>
    
     <span data-ttu-id="4eae6-p131">목록 또는 라이브러리를 사용 하는 여러 콘텐츠 형식 관리를 지 원하는 경우 **콘텐츠 형식** 에서 정보 관리 정책 지정 하려는 콘텐츠 형식을 선택할 수 있습니다. 이 위의 단계 5로 직접 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p131">If the list or library you are working with supports the management of multiple content types, under **Content Types** you can choose the content type for which you want to specify an information management policy. This will take you directly to Step 5 above.</span></span> 
    
## <a name="apply-a-policy-across-site-collections"></a><span data-ttu-id="4eae6-274">사이트 모음 전체에서 정책 적용</span><span class="sxs-lookup"><span data-stu-id="4eae6-274">Apply a policy across site collections</span></span>
<span data-ttu-id="4eae6-275"><a name="__toc260646789"> </a></span><span class="sxs-lookup"><span data-stu-id="4eae6-275"></span></span>

<span data-ttu-id="4eae6-p132">콘텐츠 형식 게시를 설정 하는 관리 되는 메타 데이터 서비스 응용 프로그램을 사용 하 여 사이트 모음 전체에서 콘텐츠 형식을 공유 합니다. 콘텐츠 형식 게시를 사용 하면 관리 콘텐츠 및 메타 데이터 일관성 있게 사이트 전체에서 여러 구독 사이트 모음 또는 웹 응용 프로그램에 확장 업데이트를 게시할 수 및 콘텐츠 형식을 생성 하 고 중앙에서 업데이트할 수 있으므로 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p132">Share content types across site collections by using a Managed Metadata service application to set up content type publishing. Content type publishing helps you manage content and metadata consistently across your sites because content types can be created and updated centrally, and updates can be published out to multiple subscribing site collections or Web applications.</span></span>
  
## <a name="create-a-template-from-an-existing-policy-to-use-across-site-collections"></a><span data-ttu-id="4eae6-278">사이트 모음 전체에서 사용 하 여 기존 정책을에서 서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="4eae6-278">Create a template from an existing policy to use across site collections</span></span>
<span data-ttu-id="4eae6-279"><a name="__toc262125409"> </a></span><span class="sxs-lookup"><span data-stu-id="4eae6-279"></span></span>

<span data-ttu-id="4eae6-p133">정보 관리 정책 정의 다음에서 여러 사이트 모음 전체에서 필요에 따라 사용 하도록 서식 파일을 만들 수 있습니다. 정보 정책에 백업 하려면 또는 콘텐츠 형식 게시를 사용 하 여 사이트 모음 전체에서 하나의 정책을 적용 하기 위한 대체 방법으로 사용할 수도 있습니다 하는 경우이 메서드를 사용할 수 있습니다. 하나의 사이트 모음에서 정책을 내보내기 (영문) 한 다음 저장 된 위치에 또는 가져와서 다른 사이트 모음에 서식 파일 또는 정책의 백업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p133">You can define an information management policy and then create a template from it to use as needed across multiple site collections. This method can be used if you want to have a backup of your information policies, or it can also be used as an alternate method to using content type publishing for applying one policy across site collections. You create a template or backup of the policy by exporting the policy from one site collection and then importing it to a saved location or to another site collection.</span></span>
  
> [!IMPORTANT]
>  <span data-ttu-id="4eae6-p134">정책 서식 파일의 집합을 확인 하는 방법으로 기능 내보내기/가져오기를 사용 하 여 하는 경우 염두에 정책.xml 파일에 있는 고유 식별자입니다. 이 때문에 가져올 수는 없습니다 해당 정책을 사이트에 여러 번이 고유 식별자를 변경 하지 않고 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p134">If you using the export/import feature as a way to make a set of policy templates, keep in mind that a unique identifier exists in the policy .xml file. Because of this, you cannot import that policy into a site more than once without changing this unique identifier.</span></span> 
  
### <a name="export-a-policy"></a><span data-ttu-id="4eae6-285">정책 내보내기</span><span class="sxs-lookup"><span data-stu-id="4eae6-285">Export a policy</span></span>
<span data-ttu-id="4eae6-286"><a name="__toc260646790"> </a></span><span class="sxs-lookup"><span data-stu-id="4eae6-286"></span></span>

1. <span data-ttu-id="4eae6-287">사이트 모음 홈페이지에서 **설정**을 선택![는 사이트 설정의 전체에 수행한 작은 설정 기어 합니다. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) \> **사이트 설정**합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-287">On the site collection home page, choose **Settings**![Small Settings gear that took the place of Site Settings.](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png)\> **Site Settings**.</span></span>
    
    <span data-ttu-id="4eae6-288">SharePoint 그룹에 연결 된 사이트에서 **설정**을 클릭 하 고 **사이트 콘텐츠**를 클릭 한 다음 **사이트 설정**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-288">In a SharePoint group-connected site, click **Settings**, click **Site Contents**, and then click **Site Settings**.</span></span> 
    
2. <span data-ttu-id="4eae6-289">사이트 설정 페이지의 **사이트 모음 관리** 에서 \> **콘텐츠 형식에 대 한 정책 서식 파일**입니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-289">On the Site Settings page, under **Site Collection Administration** \> **Content Type Policy Templates**.</span></span> 
  
![사이트 설정 페이지에서 콘텐츠 형식 정책 서식 파일 링크](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. <span data-ttu-id="4eae6-291">내보낼 정책을 선택 \> 아래쪽으로 스크롤 \> **내보냅니다**.</span><span class="sxs-lookup"><span data-stu-id="4eae6-291">Choose the policy you want to export \> scroll to the bottom \> **Export**.</span></span>
    
4. <span data-ttu-id="4eae6-p135">파일을 열거나 저장 하려면 프롬프트 **저장**을 선택 하 고 파일을 저장할 위치를 선택 합니다. 정책을 가져오는 사이트 모음을 사용할 수 있는 위치를 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p135">At the prompt to save or open the file, choose **Save**, and then select a location to save the file to. Be sure to select a location that is available to the site collections that are importing the policy.</span></span>
    
5. <span data-ttu-id="4eae6-294">다운로드 완료 대화 상자 표시 되 면 **닫기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-294">When the Download Complete dialog is displayed, choose **Close**.</span></span>
    
### <a name="import-a-policy-to-a-different-site-collection"></a><span data-ttu-id="4eae6-295">다른 사이트 모음에 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="4eae6-295">Import a policy to a different site collection</span></span>
<span data-ttu-id="4eae6-296"><a name="__toc260646791"> </a></span><span class="sxs-lookup"><span data-stu-id="4eae6-296"></span></span>

<span data-ttu-id="4eae6-p136">정보 관리 정책 가져오기 (영문)를 사용 하면 모든 특정된 사이트 모음 내에서 사이트 또는 목록 수준에서 여러 콘텐츠 형식에 적용할 수 있습니다. 이 작업의 장점: 다시 정의 하 고 각 콘텐츠 형식에 정책을 적용할 필요가 없으며 한 위치에서 정책 변경 작업을 수행 하 여 정책에 대 한 수정 내용을 보다 쉽게 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-p136">Importing an information management policy enables you to apply it to multiple content types at the site or list level within any given site collection. The benefits of doing this are twofold: you don't have to re-define and apply the policy on each content type, and you can more easily manage policy modifications by making changes to the policy in just one place.</span></span>
  
1. <span data-ttu-id="4eae6-299">정책을 적용할 사이트 모음의 홈 페이지에서 **설정**을 선택![는 사이트 설정의 전체에 수행한 작은 설정 기어 합니다. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) \> **사이트 설정**합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-299">On the home page of the site collection to which you want to apply the policy, choose **Settings**![Small Settings gear that took the place of Site Settings.](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png)\> **Site Settings**.</span></span>
    
    <span data-ttu-id="4eae6-300">SharePoint 그룹에 연결 된 사이트에서 **설정**을 클릭 하 고 **사이트 콘텐츠**를 클릭 한 다음 **사이트 설정**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-300">In a SharePoint group-connected site, click **Settings**, click **Site Contents**, and then click **Site Settings**.</span></span> 
    
2. <span data-ttu-id="4eae6-301">사이트 설정 페이지의 **사이트 모음 관리** 에서 \> **콘텐츠 형식에 대 한 정책 서식 파일**입니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-301">On the Site Settings page, under **Site Collection Administration** \> **Content Type Policy Templates**.</span></span>
    
3. <span data-ttu-id="4eae6-302">정책 페이지에서 \> **가져오기** \> 정책에 대 한 XML 파일을 찾고이를 **이동** 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-302">On the Policies page \> **Import** \> **Browse** to find the XML file for the policy.</span></span> 
    
4. <span data-ttu-id="4eae6-303">정책이 저장 된 XML 파일을 선택 \> **열려**있습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-303">Select the XML file in which the policy has been saved \> **Open**.</span></span> 
    
5. <span data-ttu-id="4eae6-304">사이트 모음 정책 가져오기 페이지 \> **가져오기** 정책을 사이트 모음에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-304">On the Import a Site Collection Policy page \> **Import** to add the policy to the site collection.</span></span> 
    
<span data-ttu-id="4eae6-305">이제 사이트 또는 목록 수준 하나 또는 여러 콘텐츠 형식에 가져온된 정책에 따라을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4eae6-305">Your imported policy can now be applied to one or many content types at the site or list level.</span></span> 
  
[<span data-ttu-id="4eae6-306">정보 관리 정책 사용자 콘텐츠를 수행할 작업을 감사 하 고 바코드를 추가 하려면 콘텐츠를 보존 기간을 제어 하 여 조직 또는 문서에 레이블을 사용 합니다. 정책을 내부 비즈니스 프로세스 또는 법률 및 정부 규정을 준수 하는 데 도움이 됩니다. 관리자로 설정할 수 있습니다는 정책을 문서를 추적 하는 방법을 제어 하 고 문서 보존 기간을 합니다. 광범위 한 사이트 계층 구조에서 서로 다른 세 위치에서 정보 관리 정책 수 있습니다를 만들 수 있습니다는 가장 좁은에: 사이트 모음 내에서 여러 콘텐츠 형식을 사용 하는 정책을 만듭니다. 사이트 콘텐츠 형식에 대 한 정책을 만듭니다. 목록 또는 라이브러리에 대 한 정책을 만듭니다. 자세한 내용은 정보 관리 정책 소개를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4eae6-306">Information management policies enable your organization to control how long to retain content, to audit what people do with content, and to add barcodes or labels to documents. A policy can help enforce compliance with legal and governmental regulations or internal business processes. As an administrator, you can set up a policy to control how to track documents and how long to retain documents.You can create an information management policy can at three different locations in the site hierarchy, from the broadest to the narrowest:Create a policy to use on multiple content types within a site collection.Create a policy for a site content type.Create a policy for a list or library.For more information, see Introduction to information management policies.</span></span>](create-info-mgmt-policies.md#__top)
  

