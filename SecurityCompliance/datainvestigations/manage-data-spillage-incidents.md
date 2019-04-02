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
ms.openlocfilehash: 93a98a4e01df011b789ba2453734f093ad8c19d6
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030387"
---
# <a name="manage-a-data-spillage-incident-in-microsoft-365"></a><span data-ttu-id="767c4-103">Microsoft 365에서 데이터 유출 인시던트 관리</span><span class="sxs-lookup"><span data-stu-id="767c4-103">Manage a data spillage incident in Microsoft 365</span></span>

<span data-ttu-id="767c4-104">데이터 유출 기밀, 중요 또는 악성 정보가 포함 된 문서가 신뢰할 수 없는 환경으로 릴리스되기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-104">Data spillage is when a document containing confidential, sensitive or malicious information is released into an untrusted environment.</span></span> <span data-ttu-id="767c4-105">데이터 유출 인시던트가 감지 되 면 환경을 빠르게 포함 하 고, 유출의 크기와 위치를 평가 하 고, 해당 사용자의 작업을 조사한 다음, 서비스에서 분산 된 데이터를 삭제 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-105">When a data spillage incident is detected, it's important to quickly contain the environment, assess the size and locations of the spillage, examine user activities around it, and then delete the spilled data from the service.</span></span> <span data-ttu-id="767c4-106">데이터 조사 (미리 보기) 도구를 사용 하 여 Office 365에서 중요 한 악의적 이거나 잘못 된 데이터를 검색 하 고, 발생 한 결과를 확인 한 다음 적절 한 조치를 취할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-106">Using the Data Investigations (Preview) tool, you can search for sensitive, malicious or misplaced data across Office 365, investigate to find out what happened, and then take appropriate actions.</span></span>  

## <a name="scope-of-this-article"></a><span data-ttu-id="767c4-107">이 문서의 범위</span><span class="sxs-lookup"><span data-stu-id="767c4-107">Scope of this article</span></span>

<span data-ttu-id="767c4-108">이 문서에서는 Office 365 사서함에서 항목을 영구적으로 삭제 하는 방법에 대 한 지침을 제공 하 여 사용자 또는 관리자가 더 이상 액세스할 수 없거나 복구할 수 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-108">This article provides a list of instructions on how to permanently delete items from Office 365 mailboxes so they are no longer accessible or recoverable by users or admins.</span></span> 

> [!NOTE]
> <span data-ttu-id="767c4-109">SharePoint 또는 비즈니스용 OneDrive 사이트에 있는 항목을 삭제 하면 원래 위치에서 삭제 한 시간부터 93 일 동안 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-109">When you delete items located in a SharePoint or OneDrive for Business site, they are retained for 93 days from the time you delete them from their original location.</span></span>

## <a name="scenario"></a><span data-ttu-id="767c4-110">시나리오</span><span class="sxs-lookup"><span data-stu-id="767c4-110">Scenario</span></span>

<span data-ttu-id="767c4-111">직원 들이 전자 메일을 통해 여러 사람과 고도로 기밀 문서를 공유 하는 데이터 유출 문제에 대 한 정보를 제공 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-111">You're informed of a data spillage incident where an employee unknowingly shared a highly-confidential document with multiple people through email.</span></span> <span data-ttu-id="767c4-112">조직 내부 및 외부 모두에서이 문서를 받은 사람을 빠르게 평가 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="767c4-112">You want to quickly assess who received this document, both inside and outside of your organization.</span></span> <span data-ttu-id="767c4-113">인시던트를 조사한 후에는 다른 investigators 검토를 위해 결과를 공유 하 고 Office 365에서 분산 된 데이터를 영구적으로 제거 하려는 경우를 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-113">After you've investigate the incident, you plan to share your findings with other investigators to review, and then permanently remove the spilled data from Office 365.</span></span> <span data-ttu-id="767c4-114">조사가 완료 되 면 모든 증거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-114">After the investigation is complete, you want to remove all evidence.</span></span> 

## <a name="workflow"></a><span data-ttu-id="767c4-115">워크플로</span><span class="sxs-lookup"><span data-stu-id="767c4-115">Workflow</span></span>

<span data-ttu-id="767c4-116">데이터 조사 (미리 보기)를 사용 하 여 데이터 유출 인시던트를 관리 하는 워크플로는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-116">Here's the workflow for using Data Investigations (Preview) to manage a data spillage incident:</span></span>

1.  <span data-ttu-id="767c4-117">데이터 조사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-117">Create a data investigation.</span></span>

2.  <span data-ttu-id="767c4-118">중요, 악성 또는 잘못 된 데이터를 검색 하 고이를 증거로 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-118">Search for sensitive, malicious, or misplaced data and collect them as evidence.</span></span>

3.  <span data-ttu-id="767c4-119">증거를 검토 하 고 조사 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-119">Review and investigate the evidence.</span></span>

4.  <span data-ttu-id="767c4-120">분산 된 데이터를 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-120">Permanently delete the spilled data.</span></span>

5.  <span data-ttu-id="767c4-121">조사를 닫거나 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-121">Close or delete the investigation.</span></span>


## <a name="before-you-begin"></a><span data-ttu-id="767c4-122">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="767c4-122">Before you begin</span></span>

- <span data-ttu-id="767c4-123">보안 & 준수 센터의 데이터 조사 (미리 보기) 도구를 사용 하 여 조사를 만들고, 분산 된 데이터를 검색 하 고, 검토 및 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-123">You'll use the Data Investigations (Preview) tool in the Security & Compliance Center to create an investigation, search for the spilled data, and review and analyze it.</span></span> <span data-ttu-id="767c4-124">그런 다음 Security & 준수 센터 PowerShell을 사용 하 여 Office 365에서 분산 된 데이터를 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-124">Then you'll use Security & Compliance Center PowerShell to permanently delete the spilled data from Office 365.</span></span> 

- <span data-ttu-id="767c4-125">조사를 만들려면 Security & 준수 센터에서 준수 관리자 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-125">To create an investigation, you have to be a member of the Compliance Administrator role group in the Security & Compliance Center.</span></span>

- <span data-ttu-id="767c4-126">메시지를 삭제 하려면 검색 및 삭제 역할이 할당 된 보안 & 준수 센터에서 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-126">To delete messages, you have to be a member of a role group in the Security & Compliance Center that's assigned the Search and Purge role.</span></span> <span data-ttu-id="767c4-127">기본적으로이 역할은 조직 관리 역할 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-127">By default, this role is assigned to the Organization Management role group.</span></span> <span data-ttu-id="767c4-128">역할 그룹에 사용자를 추가 하는 방법에 대 한 자세한 내용은 [Security & 준수 센터의 사용 권한을](../permissions-in-the-security-and-compliance-center.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="767c4-128">For information about adding users to a role group, see [Permissions in the Security & Compliance Center](../permissions-in-the-security-and-compliance-center.md).</span></span> 

- <span data-ttu-id="767c4-129">investigator에서 검색할 수 있는 사용자 사서함과 OneDrive 계정을 제어 하기 위해 조직에서 준수 경계를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-129">To control which user mailboxes and OneDrive accounts an investigator can search, your organization can set up compliance boundaries.</span></span> <span data-ttu-id="767c4-130">자세한 내용은 [eDiscovery 조사에 대 한 준수 경계를 설정](../set-up-compliance-boundaries.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-130">For more information, [Set up compliance boundaries for eDiscovery investigations](../set-up-compliance-boundaries.md).</span></span> 

## <a name="step-1-create-a-data-investigation"></a><span data-ttu-id="767c4-131">1 단계: 데이터 조사 만들기</span><span class="sxs-lookup"><span data-stu-id="767c4-131">Step 1: Create a data investigation</span></span>

<span data-ttu-id="767c4-132">데이터 조사 (미리 보기) 도구에서 조사를 만들려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-132">To create an investigation in the Data Investigations (Preview) tool:</span></span>

1. <span data-ttu-id="767c4-133">[https://compliance.microsoft.com](https://compliance.microsoft.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-133">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com).</span></span>
    
2. <span data-ttu-id="767c4-134">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-134">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="767c4-135">준수 센터에서 **데이터 조사**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-135">In the compliance center, click **Data Investigations**.</span></span>
 
4. <span data-ttu-id="767c4-136">**데이터 조사 (미리 보기)** 페이지에서 **새 조사 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-136">On the **Data Investigations (Preview)** page, click **Create new investigation**.</span></span>
    
5. <span data-ttu-id="767c4-137">**새 데이터 조사** 플라이 아웃 페이지에서 이름 (필수)을 확인 한 다음, 선택적 조사 번호 및 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-137">On the **New data investigation** flyout page, give the investigation a name (required), and then type an optional investigation number and description.</span></span> <span data-ttu-id="767c4-138">이름은 조직 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-138">Note that the name must be unique in your organization.</span></span>

6. <span data-ttu-id="767c4-139">**이 조사를 만든 후 추가 설정을 구성**하 시겠습니까?에서 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-139">Under **Do you want to configure additional settings after creating this investigation?**, do one of the following:</span></span>

    - <span data-ttu-id="767c4-140">**예** 를 클릭 하 여 조사를 만들고 새 사례에 **설정** 페이지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-140">Click **Yes** to create the investigation, and display the **Settings** page in the new case.</span></span> <span data-ttu-id="767c4-141">이를 통해 조사에 구성원을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-141">This allows you to add members to the investigation.</span></span>
    
    - <span data-ttu-id="767c4-142">조사를 만들고 **데이터 조사 (미리 보기)** 페이지의 사례 목록에 표시 하려면 **아니요** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-142">Click **No** to just create the investigation and display it in the list of cases on the **Data Investigations (Preview)** page.</span></span> <span data-ttu-id="767c4-143">이 옵션을 선택 하면 조사에 대 한 유일한 구성원으로 추가 되 고 기본 검색 및 분석 설정이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-143">If you choose this option, you will be added as the only member of the investigation and the default search and analytics settings will be used.</span></span> <span data-ttu-id="767c4-144">조사가 만들어진 후 언제 든 지 구성원을 추가 하거나 설정을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-144">You can add members or change settings any time after the investigation is created.</span></span>

7. <span data-ttu-id="767c4-145">**저장** 을 클릭 하 여 조사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-145">Click **Save** to create the investigation.</span></span>

    <span data-ttu-id="767c4-146">새 조사가 **데이터 조사 (미리 보기)** 페이지의 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-146">The new investigation is displayed in the list on the **Data Investigations (Preview)** page.</span></span> 

8. <span data-ttu-id="767c4-147">조사를 열려면 조사 이름을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-147">To open an investigation, click the name of the investigation.</span></span> 

    <span data-ttu-id="767c4-148">조사에 대 한 **홈** 탭이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-148">The **Home** tab for the investigation is displayed.</span></span> 

> [!TIP]
> <span data-ttu-id="767c4-149">조사에 대 한 명명 규칙을 설정 하 고 필요한 경우 나중에 찾고 참조할 수 있도록 이름 및 설명에 최대한 많은 정보를 제공 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-149">Consider establishing a naming convention for investigations and provide as much information as you can in the name and description so you can locate and refer to in the future if necessary.</span></span>
 
## <a name="step-2-search-for-the-spilled-data"></a><span data-ttu-id="767c4-150">2 단계: 분산 된 데이터 검색</span><span class="sxs-lookup"><span data-stu-id="767c4-150">Step 2: Search for the spilled data</span></span> 
 
<span data-ttu-id="767c4-151">연결 된 데이터를 검색할 사용자를 알고 있는 경우 해당 데이터 원본을 조사에 매핑하고 사서함 및 OneDrive 계정을 빠르게 검색 하는 데 필요한 사용자로이를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-151">If you know which users you want to search for spilled data, you can add them as people of interest to map their data sources to the investigation and quickly search their mailbox and OneDrive account.</span></span> <span data-ttu-id="767c4-152">조사에 관심이 있는 사람을 추가 하려면 **관심**있는 사용자를 클릭 한 다음 **관심 있는 사용자 추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-152">To add people of interest to the investigation, click **People of interest**, and then click **Add people of interest**.</span></span> <span data-ttu-id="767c4-153">자세한 내용은 [관심 있는 사용자 관리](manage-people-of-interest.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="767c4-153">For more information, see [Manage people of interest](manage-people-of-interest.md).</span></span>

<span data-ttu-id="767c4-154">검색 탭 \*\*\*\* 에서 검색을 만들어 분산 된 데이터를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-154">On the **Searches** tab, you can create searches to find the spilled data.</span></span> <span data-ttu-id="767c4-155">[4 단계](#step-4-delete-the-spilled-data)에서 같은 메시지를 삭제 하기 위해 데이터를 검색 하는 데 사용한 것과 동일한 검색 쿼리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-155">You will use the same search query that you used to find the spilled data to delete those same messages in [Step 4](#step-4-delete-the-spilled-data).</span></span> <span data-ttu-id="767c4-156">검색을 만드는 방법에 대 한 자세한 내용은 [조사에서 데이터 검색](search-for-data.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="767c4-156">For more information about creating searches, see [Search for data in an investigation](search-for-data.md).</span></span>

<span data-ttu-id="767c4-157">검색을 실행 한 후에는 검색 결과의 샘플을 미리 보고 검색 통계를 확인 하 여 검색 쿼리의 효율성을 평가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-157">After you run the search, you can preview samples of search results and view search statistics to evaluate the effectiveness of your search query.</span></span> <span data-ttu-id="767c4-158">Office 365에서 삭제할 항목을 확인 한 후에는 **증거** 탭을 클릭 한 다음 증거 세트를 만들고 해당 항목이 포함 된 검색 결과를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-158">Once you identify the items that you want to delete from Office 365, you can click the **Evidence** tab, and then create an evidence set and add search results that contain those items.</span></span> 

<span data-ttu-id="767c4-159">이렇게 하려면 조사할 검색을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-159">To do this, click the search that you want to investigate.</span></span> <span data-ttu-id="767c4-160">플라이 아웃 페이지에서 **결과를 증거에 추가** 를 클릭 하 고 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-160">On the flyout page, click **Add results to evidence** and follow the instructions.</span></span> <span data-ttu-id="767c4-161">그런 다음 증거에서 개별 문서를 검토 하 고, 문서에 액세스 한 사람을 조사 하 고, 문서를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-161">Then in the evidence, you can review individual documents, investigate who had access to documents, and export the documents.</span></span> <span data-ttu-id="767c4-162">문서를 검토 하는 대신 삭제 하려면 [4 단계로](#step-4-delete-the-spilled-data)이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-162">To simply delete the documents instead of reviewing them, go to [Step 4](#step-4-delete-the-spilled-data).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="767c4-163">검색 쿼리에 사용 하는 키워드에는 검색 중인 실제 데이터 데이터가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-163">The keywords that you use in the search query may contain the actual spilled data that you're searching for.</span></span> <span data-ttu-id="767c4-164">예를 들어 소셜 보안 번호가 포함 된 문서를 검색 쿼리에서 키워드로 사용 하는 경우에는 나중에 쿼리를 삭제 하 여 더 이상 유출을 방지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-164">For example, if you search for documents containing a social security number and you use it as a keyword in the search query, you must delete the query afterwards to avoid further spillage.</span></span> <span data-ttu-id="767c4-165">[5 단계](#step-5-close-or-delete-the-investigation)에서 검색을 삭제 하거나 전체 조사를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-165">You can delete the search or delete the entire investigation in [Step 5](#step-5-close-or-delete-the-investigation).</span></span> 

## <a name="step-3-review-and-investigate"></a><span data-ttu-id="767c4-166">3 단계: 검토 및 조사</span><span class="sxs-lookup"><span data-stu-id="767c4-166">Step 3: Review and investigate</span></span> 

<span data-ttu-id="767c4-167">조사에서 **증거** 탭으로 이동 하 여 이전 단계에서 만든 증명 정보 집합을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-167">In the investigation, go to **Evidence** tab and click on the evidence set that you created in the previous step.</span></span> <span data-ttu-id="767c4-168">처리 작업을 완료 하 고 검색 결과를 증명 정보에 추가한 후에는 개별 문서를 원시 형식, 텍스트 형식 또는 거의 기본 형식으로 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-168">After the processing job is completed and the search results are added to the evidence, you can review individual documents in their native format, text format, or a near-native format.</span></span> <span data-ttu-id="767c4-169">추가 쿼리를 만들어 문서 목록의 범위를 좁히거나 조사 결과를 나타내기 위해 문서에 태그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-169">You can create additional queries to narrow the list of documents, and tag documents to indicate findings from your investigation.</span></span> <span data-ttu-id="767c4-170">자세한 내용은 [증거 데이터를 검토](review-data-in-evidence.md) 하십시오.</span><span class="sxs-lookup"><span data-stu-id="767c4-170">For more information, see [Review data in evidence](review-data-in-evidence.md)</span></span>

<span data-ttu-id="767c4-171">문서를 그룹화 하 고 검토에 대 한 추가 지원을 받으려면 **증거 관리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-171">To group documents and get more assistance for your review, click **Manage evidence**.</span></span> <span data-ttu-id="767c4-172">**분석** 타일에서 **분석**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-172">In the **Analytics** tile, click **Analyze**.</span></span> <span data-ttu-id="767c4-173">이렇게 하면 중복 검색, 전자 메일 스레딩 및 테마 분석과 같은 고급 분석이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-173">This will run advanced analytics such as duplicate detection, email threading, and theme analysis.</span></span> <span data-ttu-id="767c4-174">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="767c4-174">For more information, see:</span></span>

- [<span data-ttu-id="767c4-175">분석을 실행 하 여 더 빠른 조사</span><span class="sxs-lookup"><span data-stu-id="767c4-175">Run analytics to investigate faster</span></span>](run-analytics-to-investigate-faster.md)
- [<span data-ttu-id="767c4-176">중복에 가까운 검색</span><span class="sxs-lookup"><span data-stu-id="767c4-176">Near duplicate detection</span></span>](near-duplicates.md)
- [<span data-ttu-id="767c4-177">전자 메일 스레드</span><span class="sxs-lookup"><span data-stu-id="767c4-177">Email threading</span></span>](email-threading.md)
- [<span data-ttu-id="767c4-178">테마</span><span class="sxs-lookup"><span data-stu-id="767c4-178">Themes</span></span>](themes.md)

<span data-ttu-id="767c4-179">데이터 유출와 관련 된 사용자를 확인 하려면 증거 집합에 새 쿼리를 만든 다음 보낸 사람/만든이 및 받는 사람 조건을 사용 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-179">To determine which users are involved in the data spillage, you can create a new query in the evidence set and then use the Sender/Author and Recipients conditions.</span></span> <span data-ttu-id="767c4-180">이렇게 하면 증명 정보에 추가 된 수집한 데이터에 있는 모든 보낸 사람, 받는 사람 및 작성자의 목록이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-180">This will create a list of all senders, recipients, and authors found in collected data that was added to the evidence.</span></span> <span data-ttu-id="767c4-181">외부 사용자가 있는지를 확인 하려면 목록을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="767c4-181">Be sure to examine the list to determine if there are any external users.</span></span> <span data-ttu-id="767c4-182">조건을 사용 하 여 검색 결과를 좁히는 방법에 대 한 자세한 내용은 [검색 조건](../keyword-queries-and-search-conditions.md#search-conditions)항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="767c4-182">For more information about using conditions to narrow search results, see [Search conditions](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>

## <a name="step-4-delete-the-spilled-data"></a><span data-ttu-id="767c4-183">4 단계: 데이터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-183">Step 4: Delete the spilled data</span></span>

### <a name="deleting-mailbox-items"></a><span data-ttu-id="767c4-184">사서함 항목 삭제</span><span class="sxs-lookup"><span data-stu-id="767c4-184">Deleting mailbox items</span></span>

<span data-ttu-id="767c4-185">검색 결과에 삭제 해야 하는 전자 메일 메시지만 포함 되어 있는지 검토 하 고 유효성을 검사 한 후에는 보안 & 규정 준수에서 **new-compliancesearchaction-PurgeType 하드 삭제** 명령을 실행 하 여이를 영구적으로 삭제할 수 있습니다. Center PowerShell</span><span class="sxs-lookup"><span data-stu-id="767c4-185">After you review and validate that the search results contain only the email messages that must be deleted, you can permanently delete them by running the **New-ComplianceSearchAction -Purge -PurgeType HardDelete** command in Security & Compliance Center PowerShell.</span></span> <span data-ttu-id="767c4-186">자세한 내용은 [전자 메일 메시지 검색 및 삭제](../search-for-and-delete-messages-in-your-organization.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="767c4-186">For instructions, see [Search for and delete email messages](../search-for-and-delete-messages-in-your-organization.md).</span></span> 

<span data-ttu-id="767c4-187">조직의 사서함에 대해 단일 항목 복구를 사용 하도록 설정 된 경우 삭제 된 항목 보존 기간이 종료 (기본값 14 일) 될 때까지 영구 삭제 된 항목이 사용자의 복구 가능한 항목 폴더 (관리자가 액세스할 수 있음)에 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-187">If single item recovery is enabled for mailboxes in your organization, permanently deleted items will be retained in the user's Recoverable items folder (and accessible by admins) until the deleted item retention period ends (the default is 14 days).</span></span> <span data-ttu-id="767c4-188">또한, 분산 된 데이터가 포함 된 사서함이 보존 정책에 할당 된 경우에는 항목의 보존 기간이 만료 될 때까지 제거 된 메시지가 복구 가능한 항목 폴더에 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-188">Additionally, if any mailbox that contains spilled data is on a legal hold or assigned to a retention policy, purged messages will be retained in the Recoverable items folder until the hold duration for the item expires.</span></span> <span data-ttu-id="767c4-189">메시지를 즉시 하드 삭제 하려면 추가 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-189">To hard delete messages immediately, you need to perform addition tasks.</span></span> <span data-ttu-id="767c4-190">자세한 내용은 [보류 중인 클라우드 기반 사서함의 복구 가능한 항목 폴더에서 항목 삭제](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="767c4-190">For instructions, see [Delete items in the Recoverable Items folder of cloud-based mailboxes on hold](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="767c4-191">보류 또는 보존 정책을 제거 하기 전에 레코드 관리 또는 법률 부서에 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="767c4-191">Check with your records management or legal departments before removing a hold or retention policy.</span></span> <span data-ttu-id="767c4-192">조직에 보류 중인 사서함 또는 데이터 유출 인시던트가 우선 하는지 여부를 정의 하는 정책이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-192">Your organization may have a policy that defines whether a mailbox on hold or a data spillage incident takes priority.</span></span> 

### <a name="deleting-site-items"></a><span data-ttu-id="767c4-193">사이트 항목 삭제</span><span class="sxs-lookup"><span data-stu-id="767c4-193">Deleting site items</span></span>

<span data-ttu-id="767c4-194">SharePoint 사이트 또는 OneDrive 계정에서 문서를 영구적으로 삭제 하려면 문서를 삭제 한 다음 사이트 휴지통에서 삭제 한 후에 사이트 모음 휴지통에서 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-194">To permanently delete a document from a SharePoint site or OneDrive account, you have to delete the document and then you have to delete from the site Recycle Bin and then delete it from the site collection Recycle Bin.</span></span> <span data-ttu-id="767c4-195">자세한 내용은 [SharePoint 및 OneDrive에서 문서 삭제](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="767c4-195">For more information, see [Delete documents in SharePoint and OneDrive](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business).</span></span>

<span data-ttu-id="767c4-196">또는, 분산 된 데이터가 포함 되어 있을 수 있는 전체 사이트 모음을 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-196">Alternatively, you can delete an entire site collection that might contained spilled data.</span></span> <span data-ttu-id="767c4-197">자세한 내용은 [사이트 모음 삭제](https://docs.microsoft.com/sharepoint/delete-site-collection)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="767c4-197">For instructions, see [Delete a site collection](https://docs.microsoft.com/sharepoint/delete-site-collection).</span></span>

## <a name="step-5-close-or-delete-the-investigation"></a><span data-ttu-id="767c4-198">5 단계: 조사 닫기 또는 삭제</span><span class="sxs-lookup"><span data-stu-id="767c4-198">Step 5: Close or delete the investigation</span></span>

<span data-ttu-id="767c4-199">라이브 서비스의 원본 콘텐츠 위치 (사서함 또는 사이트)에서 문서를 삭제 한 후에도 조사 과정에서 증거에 추가한 이러한 문서의 복사본을 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-199">After you delete documents in the source content locations (mailboxes or sites) in the live service, you will still have copies of these documents that you added to evidence as part of your investigation.</span></span> <span data-ttu-id="767c4-200">데이터 유출를 더 방지 하려면 조사 자체를 삭제 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-200">To avoid further data spillage, you should consider deleting the investigation itself.</span></span>

<span data-ttu-id="767c4-201">조사를 삭제 하려면:</span><span class="sxs-lookup"><span data-stu-id="767c4-201">To delete an investigation:</span></span>

1. <span data-ttu-id="767c4-202">**설정** 탭에서 **조사 정보**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-202">On the **Settings** tab, click **Investigation information**.</span></span>

2. <span data-ttu-id="767c4-203">**조사 삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-203">Click  **Delete investigation**.</span></span> 

<span data-ttu-id="767c4-204">조사를 삭제할 필요가 없거나 조사 중에 수집한 정보를 저장 하려는 경우에는 **대/소문자 닫기를**클릭 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-204">If you don't need to delete the investigation or if you want to save the information that you collected during the investigation, you can click **Close case**.</span></span> <span data-ttu-id="767c4-205">나중에 마감 된 조사를 다시 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="767c4-205">Then at a later date, you can re-open closed investigations.</span></span>