---
title: Microsoft 365에서 데이터 유출 인시던트 관리
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 이 문서에서는 보안 & 준수 센터의 새 데이터 조사 (미리 보기) 도구를 사용 하 여 데이터 유출 인시던트를 관리 하는 방법을 설명 합니다.
ms.openlocfilehash: 93199ad1f548e999dce9ad79ab311a57345b8772
ms.sourcegitcommit: 3962de88a143f0eb416b5cfdfd777d731f560ec8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2019
ms.locfileid: "36649931"
---
# <a name="manage-a-data-spillage-incident-in-microsoft-365"></a><span data-ttu-id="756b8-103">Microsoft 365에서 데이터 유출 인시던트 관리</span><span class="sxs-lookup"><span data-stu-id="756b8-103">Manage a data spillage incident in Microsoft 365</span></span>

<span data-ttu-id="756b8-104">데이터 유출 기밀, 중요 또는 악성 정보가 포함 된 문서가 신뢰할 수 없는 환경에서 릴리스될 때</span><span class="sxs-lookup"><span data-stu-id="756b8-104">Data spillage is when a document containing confidential, sensitive, or malicious information is released in an untrusted environment.</span></span> <span data-ttu-id="756b8-105">데이터 유출 인시던트가 감지 되 면 환경을 빠르게 포함 하 고, 유출의 크기와 위치를 평가 하 고, 해당 사용자의 작업을 조사한 다음, 서비스에서 분산 된 데이터를 삭제 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-105">When a data spillage incident is detected, it's important to quickly contain the environment, assess the size and locations of the spillage, examine user activities around it, and then delete the spilled data from the service.</span></span> <span data-ttu-id="756b8-106">데이터 조사 (미리 보기) 도구를 사용 하 여 Office 365에서 중요, 악성 또는 잘못 된 데이터를 검색 하 고, 발생 한 결과를 확인 한 다음 적절 한 조치를 취할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-106">Using the Data Investigations (Preview) tool, you can search for sensitive, malicious, or misplaced data across Office 365, investigate to find out what happened, and then take appropriate actions.</span></span>  

## <a name="scope-of-this-article"></a><span data-ttu-id="756b8-107">이 문서의 범위</span><span class="sxs-lookup"><span data-stu-id="756b8-107">Scope of this article</span></span>

<span data-ttu-id="756b8-108">이 문서에서는 Office 365 사서함에서 항목을 영구적으로 삭제 하는 방법에 대 한 지침을 제공 하 여 사용자 또는 관리자가 더 이상 액세스할 수 없거나 복구할 수 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-108">This article provides a list of instructions on how to permanently delete items from Office 365 mailboxes so they are no longer accessible or recoverable by users or admins.</span></span> 

> [!NOTE]
> <span data-ttu-id="756b8-109">SharePoint 또는 비즈니스용 OneDrive 사이트에 있는 항목을 삭제 하면 원래 위치에서 삭제 한 시간부터 93 일 동안 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-109">When you delete items located in a SharePoint or OneDrive for Business site, they are retained for 93 days from the time you delete them from their original location.</span></span>

## <a name="scenario"></a><span data-ttu-id="756b8-110">시나리오</span><span class="sxs-lookup"><span data-stu-id="756b8-110">Scenario</span></span>

<span data-ttu-id="756b8-111">직원 들이 전자 메일을 통해 여러 사용자와 고도로 기밀 문서를 공유 하는 데이터 유출 문제에 대 한 정보를 제공 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-111">You're informed of a data spillage incident where an employee unknowingly shared a highly confidential document with multiple people through email.</span></span> <span data-ttu-id="756b8-112">조직 내부 및 외부 모두에서이 문서를 받은 사람을 빠르게 평가 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="756b8-112">You want to quickly assess who received this document, both inside and outside of your organization.</span></span> <span data-ttu-id="756b8-113">인시던트를 조사한 후에는 다른 investigators 검토를 위해 결과를 공유 하 고 Office 365 조직에서 분산 된 데이터를 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-113">After you've investigate the incident, you plan to share your findings with other investigators to review, and then permanently remove the spilled data from your Office 365 organization.</span></span> <span data-ttu-id="756b8-114">조사가 완료 되 면 모든 증거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-114">After the investigation is complete, you want to remove all evidence.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="756b8-115">조직 내에서 분산 된 데이터를 영구적으로 제거할 수 있지만 조직 외부에 분산 된 데이터는 이러한 기능을 사용 하 여 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-115">While you'll be able to permanently remove the spilled data within your own organization, any data spilled outside your organization can't be removed with these capabilities.</span></span>

## <a name="workflow"></a><span data-ttu-id="756b8-116">워크플로</span><span class="sxs-lookup"><span data-stu-id="756b8-116">Workflow</span></span>

<span data-ttu-id="756b8-117">데이터 조사 (미리 보기)를 사용 하 여 데이터 유출 인시던트를 관리 하는 워크플로는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-117">Here's the workflow for using Data Investigations (Preview) to manage a data spillage incident:</span></span>

1.  <span data-ttu-id="756b8-118">데이터 조사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-118">Create a data investigation.</span></span>

2.  <span data-ttu-id="756b8-119">중요, 악성 또는 잘못 된 데이터를 검색 하 고이를 증거로 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-119">Search for sensitive, malicious, or misplaced data and collect them as evidence.</span></span>

3.  <span data-ttu-id="756b8-120">증거를 검토 하 고 조사 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-120">Review and investigate the evidence.</span></span>

4.  <span data-ttu-id="756b8-121">분산 된 데이터를 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-121">Permanently delete the spilled data.</span></span>

5.  <span data-ttu-id="756b8-122">조사를 닫거나 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-122">Close or delete the investigation.</span></span>


## <a name="before-you-begin"></a><span data-ttu-id="756b8-123">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="756b8-123">Before you begin</span></span>

- <span data-ttu-id="756b8-124">데이터 조사를 만들고, 콘텐츠를 검색 하 고, 분산 된 데이터를 삭제 하려면 보안 & 준수 센터에서 Data Investigator 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-124">To create a data investigation, search for content, and delete spilled data, you have to be a member of the Data Investigator role group in the Security & Compliance Center.</span></span>

- <span data-ttu-id="756b8-125">Investigator에서 검색할 수 있는 사용자 사서함과 OneDrive 계정을 제어 하기 위해 조직에서 준수 경계를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-125">To control which user mailboxes and OneDrive accounts an investigator can search, your organization can set up compliance boundaries.</span></span> <span data-ttu-id="756b8-126">자세한 내용은 [eDiscovery 조사에 대 한 준수 경계를 설정](../set-up-compliance-boundaries.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-126">For more information, [Set up compliance boundaries for eDiscovery investigations](../set-up-compliance-boundaries.md).</span></span> 

## <a name="step-1-create-a-data-investigation"></a><span data-ttu-id="756b8-127">1 단계: 데이터 조사 만들기</span><span class="sxs-lookup"><span data-stu-id="756b8-127">Step 1: Create a data investigation</span></span>

<span data-ttu-id="756b8-128">데이터 조사 (미리 보기) 도구에서 조사를 만들려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-128">To create an investigation in the Data Investigations (Preview) tool:</span></span>

1. <span data-ttu-id="756b8-129">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-129">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="756b8-130">Data Investigator 역할 그룹의 구성원 인 계정을 사용 하 여 Office 365에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-130">Sign in to Office 365 using an account that is a member of the Data Investigator role group.</span></span>
    
3. <span data-ttu-id="756b8-131">보안 및 준수 센터에서 **데이터 조사**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-131">In the security and compliance center, click **Data Investigations**.</span></span>
 
4. <span data-ttu-id="756b8-132">**데이터 조사 (미리 보기)** 페이지에서 **새 조사 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-132">On the **Data Investigations (Preview)** page, click **Create new investigation**.</span></span>
    
5. <span data-ttu-id="756b8-133">**새 데이터 조사** 플라이 아웃 페이지에서 이름 (필수)을 확인 한 다음, 선택적 조사 번호 및 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-133">On the **New data investigation** flyout page, give the investigation a name (required), and then type an optional investigation number and description.</span></span> <span data-ttu-id="756b8-134">이름은 조직 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-134">The name must be unique in your organization.</span></span>

6. <span data-ttu-id="756b8-135">**이 조사를 만든 후 추가 설정을 구성**하 시겠습니까?에서 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-135">Under **Do you want to configure additional settings after creating this investigation?**, do one of the following:</span></span>

    - <span data-ttu-id="756b8-136">**예** 를 클릭 하 여 조사를 만들고 새 사례에 **설정** 페이지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-136">Click **Yes** to create the investigation, and display the **Settings** page in the new case.</span></span> <span data-ttu-id="756b8-137">이를 통해 조사에 구성원을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-137">This allows you to add members to the investigation.</span></span>
    
    - <span data-ttu-id="756b8-138">조사를 만들고 **데이터 조사 (미리 보기)** 페이지의 사례 목록에 표시 하려면 **아니요** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-138">Click **No** to create the investigation and display it in the list of cases on the **Data Investigations (Preview)** page.</span></span> <span data-ttu-id="756b8-139">이 옵션을 선택 하면 조사에 대 한 유일한 구성원으로 추가 되 고 기본 검색 및 분석 설정이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-139">If you choose this option, you will be added as the only member of the investigation and the default search and analytics settings will be used.</span></span> <span data-ttu-id="756b8-140">조사가 만들어진 후 언제 든 지 구성원을 추가 하거나 설정을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-140">You can add members or change settings anytime after the investigation is created.</span></span>

7. <span data-ttu-id="756b8-141">**저장** 을 클릭 하 여 조사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-141">Click **Save** to create the investigation.</span></span>

    <span data-ttu-id="756b8-142">새 조사가 **데이터 조사 (미리 보기)** 페이지의 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-142">The new investigation is displayed in the list on the **Data Investigations (Preview)** page.</span></span> 

8. <span data-ttu-id="756b8-143">조사를 열려면 조사 이름을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-143">To open an investigation, click the name of the investigation.</span></span> 

    <span data-ttu-id="756b8-144">조사에 대 한 **홈** 탭이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-144">The **Home** tab for the investigation is displayed.</span></span> 

> [!TIP]
> <span data-ttu-id="756b8-145">조사에 대 한 명명 규칙을 설정 하 고, 필요한 경우 나중에 검색 하 고 참조할 수 있도록 이름 및 설명에 최대한 많은 정보를 제공 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-145">Consider establishing a naming convention for investigations and provide as much information as you can in the name and description so you can locate and refer to them in the future if necessary.</span></span>
 
## <a name="step-2-search-for-the-spilled-data"></a><span data-ttu-id="756b8-146">2 단계: 분산 된 데이터 검색</span><span class="sxs-lookup"><span data-stu-id="756b8-146">Step 2: Search for the spilled data</span></span> 
 
<span data-ttu-id="756b8-147">연결 된 데이터를 검색할 사용자를 알고 있는 경우 해당 데이터 원본을 조사에 매핑하고 사서함 및 OneDrive 계정을 빠르게 검색 하는 데 필요한 사용자로이를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-147">If you know which users you want to search for spilled data, you can add them as people of interest to map their data sources to the investigation and quickly search their mailbox and OneDrive account.</span></span> <span data-ttu-id="756b8-148">조사에 관심이 있는 사람을 추가 하려면 **관심**있는 사용자를 클릭 한 다음 **관심 있는 사용자 추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-148">To add people of interest to the investigation, click **People of interest**, and then click **Add people of interest**.</span></span> <span data-ttu-id="756b8-149">자세한 내용은 [관심 있는 사용자 관리](manage-people-of-interest.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="756b8-149">For more information, see [Manage people of interest](manage-people-of-interest.md).</span></span>

<span data-ttu-id="756b8-150">검색 탭 \*\*\*\* 에서 검색을 만들어 분산 된 데이터를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-150">On the **Searches** tab, you can create searches to find the spilled data.</span></span> <span data-ttu-id="756b8-151">검색을 만드는 방법에 대 한 자세한 내용은 [조사에서 데이터 검색](search-for-data.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="756b8-151">For more information about creating searches, see [Search for data in an investigation](search-for-data.md).</span></span>

<span data-ttu-id="756b8-152">검색을 실행 한 후에는 검색 결과의 샘플을 미리 보고 검색 통계를 확인 하 여 검색 쿼리의 효율성을 평가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-152">After you run the search, you can preview samples of search results and view search statistics to evaluate the effectiveness of your search query.</span></span> <span data-ttu-id="756b8-153">Office 365에서 삭제할 항목을 확인 한 후에는 검색 결과를 증거 집합에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-153">After you identify the items that you want to delete from Office 365, you can add the search results to an evidence set.</span></span> <span data-ttu-id="756b8-154">이렇게 하려면 조사할 검색을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-154">To do this, click the search that you want to investigate.</span></span> <span data-ttu-id="756b8-155">플라이 아웃 페이지에서 **결과를 증거에 추가** 를 클릭 하 고 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-155">On the flyout page, click **Add results to evidence** and follow the instructions.</span></span> <span data-ttu-id="756b8-156">그런 다음 증명 정보 집합에서 개별 문서를 검토 하 고, 문서에 액세스 한 사람을 조사 하 고, 문서를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-156">Then in the evidence set, you can review individual documents, investigate who had access to documents, and export the documents.</span></span> <span data-ttu-id="756b8-157">문서 또는 문서를 검토 하는 대신 하위 집합을 삭제 하려면 [4 단계로](#step-4-delete-the-spilled-data)이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-157">To delete the documents (or a subset of documents) instead of reviewing them, go to [Step 4](#step-4-delete-the-spilled-data).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="756b8-158">검색 쿼리에 사용 하는 키워드에는 검색 중인 실제 데이터 데이터가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-158">The keywords that you use in the search query may contain the actual spilled data that you're searching for.</span></span> <span data-ttu-id="756b8-159">예를 들어 소셜 보안 번호가 포함 된 문서를 검색 쿼리에서 키워드로 사용 하는 경우에는 나중에 쿼리를 삭제 하 여 더 이상 유출을 방지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-159">For example, if you search for documents containing a social security number and you use it as a keyword in the search query, you must delete the query afterwards to avoid further spillage.</span></span> <span data-ttu-id="756b8-160">[5 단계](#step-5-close-or-delete-the-investigation)에서 검색을 삭제 하거나 전체 조사를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-160">You can delete the search or delete the entire investigation in [Step 5](#step-5-close-or-delete-the-investigation).</span></span> 

## <a name="step-3-review-and-investigate"></a><span data-ttu-id="756b8-161">3 단계: 검토 및 조사</span><span class="sxs-lookup"><span data-stu-id="756b8-161">Step 3: Review and investigate</span></span> 

<span data-ttu-id="756b8-162">조사에서 **증거** 탭으로 이동 하 여 이전 단계에서 만든 증거 집합을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-162">In the investigation, go to the **Evidence** tab and click the evidence set that you created in the previous step.</span></span> <span data-ttu-id="756b8-163">처리 작업을 완료 하 고 검색 결과를 증명 정보에 추가한 후에는 개별 문서를 원시 형식, 텍스트 형식 또는 거의 기본 형식으로 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-163">After the processing job is completed and the search results are added to the evidence, you can review individual documents in their native format, text format, or a near-native format.</span></span> <span data-ttu-id="756b8-164">추가 쿼리를 만들어 문서 목록의 범위를 좁히거나 조사 결과를 나타내기 위해 문서에 태그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-164">You can create additional queries to narrow the list of documents, and tag documents to indicate findings from your investigation.</span></span> <span data-ttu-id="756b8-165">자세한 내용은 [증거 데이터를 검토](review-data-in-evidence.md) 하십시오.</span><span class="sxs-lookup"><span data-stu-id="756b8-165">For more information, see [Review data in evidence](review-data-in-evidence.md)</span></span>

<span data-ttu-id="756b8-166">문서를 그룹화 하 고 검토에 대 한 추가 지원을 받으려면 **증거 관리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-166">To group documents and get more assistance for your review, click **Manage evidence**.</span></span> <span data-ttu-id="756b8-167">**분석** 타일에서 **분석**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-167">In the **Analytics** tile, click **Analyze**.</span></span> <span data-ttu-id="756b8-168">이렇게 하면 중복 검색, 전자 메일 스레딩 및 테마 분석과 같은 고급 분석이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-168">This runs advanced analytics such as duplicate detection, email threading, and theme analysis.</span></span> <span data-ttu-id="756b8-169">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="756b8-169">For more information, see:</span></span>

- [<span data-ttu-id="756b8-170">신속한 조사를 위한 분석 실행</span><span class="sxs-lookup"><span data-stu-id="756b8-170">Run analytics to investigate faster</span></span>](run-analytics-to-investigate-faster.md)
- [<span data-ttu-id="756b8-171">중복에 가까운 검색</span><span class="sxs-lookup"><span data-stu-id="756b8-171">Near duplicate detection</span></span>](near-duplicates.md)
- [<span data-ttu-id="756b8-172">전자 메일 스레드</span><span class="sxs-lookup"><span data-stu-id="756b8-172">Email threading</span></span>](email-threading.md)
- [<span data-ttu-id="756b8-173">테마</span><span class="sxs-lookup"><span data-stu-id="756b8-173">Themes</span></span>](themes.md)

<span data-ttu-id="756b8-174">데이터 유출와 관련 된 사용자를 확인 하려면 증거 집합에서 쿼리를 만든 다음 보낸 사람/만든이 및 받는 사람 조건을 사용 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-174">To determine which users are involved in the data spillage, you can create a query in the evidence set and then use the Sender/Author and Recipients conditions.</span></span> <span data-ttu-id="756b8-175">이렇게 하면 증명 정보에 추가 된 수집한 데이터에 있는 모든 보낸 사람, 받는 사람 및 작성자의 목록이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-175">This creates a list of all senders, recipients, and authors found in collected data that was added to the evidence.</span></span> <span data-ttu-id="756b8-176">외부 사용자가 있는지를 확인 하려면 목록을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="756b8-176">Be sure to examine the list to determine if there are any external users.</span></span> <span data-ttu-id="756b8-177">조건을 사용 하 여 검색 결과를 좁히는 방법에 대 한 자세한 내용은 [검색 조건](../keyword-queries-and-search-conditions.md#search-conditions)항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="756b8-177">For more information about using conditions to narrow search results, see [Search conditions](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>

## <a name="step-4-delete-the-spilled-data"></a><span data-ttu-id="756b8-178">4 단계: 데이터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-178">Step 4: Delete the spilled data</span></span>

<span data-ttu-id="756b8-179">데이터 조사 도구를 사용 하 여 원래 위치에서 항목을 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-179">Using the data investigations tool, you can delete items from their original locations.</span></span> <span data-ttu-id="756b8-180">예를 들어 조직 전체에서 사서함, SharePoint 사이트 및 OneDrive 계정에 있는 항목을 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-180">For example, you can delete items from mailboxes, SharePoint sites, and OneDrive accounts across your organization.</span></span> <span data-ttu-id="756b8-181">항목을 증거로, 즉 2 단계에 있는 증명 정보 집합에 검색 결과를 추가 하 여 증명 정보 집합에 있는 항목의 복사본을 추가 하 여 조사 하거나 보존할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-181">Keep in mind that because you collected items as evidence (by adding the search results to the evidence set in Step 2), you have copies of the items in the evidence set to further investigate or preserve them.</span></span>

<span data-ttu-id="756b8-182">원래 위치에서 항목을 삭제 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-182">To delete items from their original locations:</span></span>

1. <span data-ttu-id="756b8-183">증거 집합에서 삭제 하려는 항목을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-183">In the evidence set, select the items that you want to delete.</span></span> <span data-ttu-id="756b8-184">전자 메일 메시지에 첨부 된 항목을 선택 하는 경우 상위 전자 메일 메시지도 선택 및 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-184">If you select items that are attached to an email message, the parent email message will also be selected and deleted.</span></span> 
 
2. <span data-ttu-id="756b8-185">**동작** 을 클릭 한 다음 **원래 위치에서 항목 삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-185">Click **Action** and then click **Delete items from original locations**.</span></span>

   ![동작을 클릭 한 다음 원래 위치에서 항목 삭제를 클릭 합니다.](../media/DataInvestigationsDeleteItems1.png)

3. <span data-ttu-id="756b8-187">플라이 아웃 페이지에서 삭제할 항목 및 관련 하위 문서 수를 확인 하 고 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-187">On the flyout page, verify the number of items and related child documents that will be deleted, and then click **Delete**.</span></span>

<span data-ttu-id="756b8-188">이 때 원래 위치에서 항목을 삭제 하면 항목이 일시 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-188">At this time, when you delete items from their original location, the items are soft-deleted.</span></span> <span data-ttu-id="756b8-189">즉, 삭제 된 항목은 항목에 대 한 삭제 된 항목 복구 기간이 만료 될 때까지 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-189">This means that the deleted items will be retained until the deleted item recovery period for the item expires.</span></span> <span data-ttu-id="756b8-190">이는 또한 사용자가 이러한 항목을 복구할 수 있다는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-190">This also means it's possible for users to recover these items.</span></span> <span data-ttu-id="756b8-191">사서함 및 사이트에서 항목을 삭제할 때 수행 되는 작업에 대 한 자세한 내용은 [원래 위치에서 항목 삭제](delete-items-from-original-locations.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="756b8-191">For more information about what happens when items are deleted from mailboxes and sites, see [Delete items from their original location](delete-items-from-original-locations.md).</span></span>

## <a name="step-5-close-or-delete-the-investigation"></a><span data-ttu-id="756b8-192">5 단계: 조사 닫기 또는 삭제</span><span class="sxs-lookup"><span data-stu-id="756b8-192">Step 5: Close or delete the investigation</span></span>

<span data-ttu-id="756b8-193">라이브 서비스의 원본 콘텐츠 위치 (사서함 또는 사이트)에서 문서를 삭제 한 후에도 조사 과정에서 증거에 추가한 이러한 문서의 복사본을 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-193">After you delete documents in the source content locations (mailboxes or sites) in the live service, you will still have copies of these documents that you added to evidence as part of your investigation.</span></span> <span data-ttu-id="756b8-194">데이터 유출를 더 방지 하려면 조사 자체를 삭제 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-194">To avoid further data spillage, you should consider deleting the investigation itself.</span></span>

<span data-ttu-id="756b8-195">조사를 삭제 하려면:</span><span class="sxs-lookup"><span data-stu-id="756b8-195">To delete an investigation:</span></span>

1. <span data-ttu-id="756b8-196">**설정** 탭에서 **조사 정보**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-196">On the **Settings** tab, click **Investigation information**.</span></span>

2. <span data-ttu-id="756b8-197">**조사 삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-197">Click  **Delete investigation**.</span></span> 

<span data-ttu-id="756b8-198">조사를 삭제할 필요가 없거나 조사 중에 수집한 정보를 저장 하려는 경우에는 **대/소문자 닫기를**클릭 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-198">If you don't need to delete the investigation or if you want to save the information that you collected during the investigation, you can click **Close case**.</span></span> <span data-ttu-id="756b8-199">나중에 닫은 조사를 다시 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756b8-199">Then later, you can reopen closed investigations.</span></span>
