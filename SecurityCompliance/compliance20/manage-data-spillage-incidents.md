---
title: Microsoft 365에서 데이터 액체 엎질렀는지 여부 문제를 관리 합니다.
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 이 문서에서는 Office 365 보안 & 준수 센터의에서 새 데이터 조사 (미리 보기) 도구를 사용 하 여 데이터 액체 엎질렀는지 여부 문제를 관리 하에 대해 설명 합니다.
ms.openlocfilehash: d7adc17d01a0ae2ad6b7bfb7052862a5a6419882
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706179"
---
# <a name="manage-a-data-spillage-incident-in-microsoft-365"></a><span data-ttu-id="ea224-103">Microsoft 365에서 데이터 액체 엎질렀는지 여부 문제를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-103">Manage a data spillage incident in Microsoft 365</span></span> 

<span data-ttu-id="ea224-p101">신뢰할 수 없는 환경에 기밀 문서를 놓을 때 데이터 액체 엎질렀는지 여부 하 게 합니다. 데이터 액체 엎질렀는지 여부 문제를 검색 하는 경우에, 크기 및 위치는 액체 엎질렀는지 여부의 신속 하 게 평가 하 고,와 관련 된 사용자 활동을 검사 하 고, 다음 시스템에서 spilled 데이터를 영구적으로 제거 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p101">Data spillage is when a confidential document is released into an untrusted environment. When a data spillage incident is detected, it's important to quickly assess the size and locations of the spillage, examine user activities around it, and then permanently purge the spilled data from the system.</span></span>

## <a name="scope-of-this-article"></a><span data-ttu-id="ea224-106">이 문서의 범위</span><span class="sxs-lookup"><span data-stu-id="ea224-106">Scope of this article</span></span>

<span data-ttu-id="ea224-107">이 문서에서는 중이거나 응답할 더이상 액세스할 수 있는 사용자 또는 관리자가 복구할 수 있도록 Office 365 사서함에서 항목을 영구적으로 제거 하는 방법에 지침의 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-107">This article provides a list of instructions on how to permanently remove items from Office 365 mailboxes so they are no longer accessible or recoverable by users or admins.</span></span> 

> [!NOTE]
> <span data-ttu-id="ea224-108">비즈니스 사이트에 대 한 SharePoint 또는 OneDrive에 있는 항목을 삭제 하면 원래 위치에서 삭제할 시간부터 93 일 동안 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-108">When you delete items located in a SharePoint or OneDrive for Business site, they are retained for 93 days from the time you delete them from their original location.</span></span>

## <a name="scenario"></a><span data-ttu-id="ea224-109">시나리오</span><span class="sxs-lookup"><span data-stu-id="ea224-109">Scenario</span></span>

<span data-ttu-id="ea224-p102">여기서 직원 모른 매우 기밀 문서와 공유 전자 메일을 통해 여러 사용자 데이터 액체 엎질렀는지 여부 문제를 확인할는 있습니다. 내부 및 외부 조직에서이 문서를 받은 사람을 신속 하 게 평가 하려고 합니다. 인시던트를 조사 했을 때 후 그 결과 검토 하 고 다음 Office 365에서에서 spilled 데이터를 영구적으로 제거 하려면 다른 수 사관와 공유를 계획 합니다. 조사가 완료 되 면 모든 증거를 제거 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p102">You're informed of a data spillage incident where an employee unknowingly shared a highly-confidential document with multiple people through email. You want to quickly assess who received this document, both inside and outside of your organization. After you've investigate the incident, you plan to share your findings with other investigators to review, and then permanently remove the spilled data from Office 365. After the investigation is complete, you want to remove all evidence.</span></span> 

## <a name="workflow"></a><span data-ttu-id="ea224-114">워크플로</span><span class="sxs-lookup"><span data-stu-id="ea224-114">Workflow</span></span>

<span data-ttu-id="ea224-115">데이터 조사 (미리 보기)를 사용 하 여 데이터 액체 엎질렀는지 여부 문제를 관리 하는 것에 대 한 워크플로 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-115">Here's the workflow for using Data Investigations (Preview) to manage a data spillage incident:</span></span>

1.  <span data-ttu-id="ea224-116">데이터 조사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-116">Create a data investigation.</span></span>

2.  <span data-ttu-id="ea224-117">Spilled 데이터를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-117">Search for the spilled data.</span></span>

3.  <span data-ttu-id="ea224-118">검토 하 고 문제를 조사 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-118">Review and investigate the incident.</span></span>

4.  <span data-ttu-id="ea224-119">Spilled 데이터를 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-119">Permanently delete the spilled data.</span></span>

5.  <span data-ttu-id="ea224-120">닫거나 조사를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-120">Close or delete the investigation.</span></span>


## <a name="before-you-begin"></a><span data-ttu-id="ea224-121">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="ea224-121">Before you begin</span></span>

- <span data-ttu-id="ea224-p103">Office 365 보안 & 준수 센터의에서 데이터 조사 (미리 보기) 도구를 사용 하 여 조사 만들기, spilled 데이터를 검색 하 고 검토 하 고 분석 합니다. 그런 다음 Office 365에서 spilled 데이터를 영구적으로 삭제 하는 보안 & 준수 센터 PowerShell을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p103">You'll use the Data Investigations (Preview) tool in the Office 365 Security & Compliance Center to create an investigation, search for the spilled data, and review and analyze it. Then you'll use Security & Compliance Center PowerShell to permanently delete the spilled data from Office 365.</span></span> 

- <span data-ttu-id="ea224-124">조사를 만들려면 보안 & 준수 센터의에서 규정 준수 관리자 역할 그룹의 구성원 이어야 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-124">To create an investigation, you have to be a member of the Compliance Administrator role group in the Security & Compliance Center.</span></span>

- <span data-ttu-id="ea224-p104">메시지를 삭제 하려면 보안 & 준수 센터에서에서 조직 관리 역할 그룹의 구성원 이거나 검색 및 삭제 역할을 할당 해야 합니다. 역할 그룹에 사용자를 추가 하는 방법에 대 한 정보를 [보안 & 준수 센터에 대 한 사용자 액세스를 제공](../grant-access-to-the-security-and-compliance-center.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ea224-p104">To delete messages, you have to be a member of the Organization Management role group in the Security & Compliance Center or be assigned the Search and Purge role. For information about adding users to a role group, see [Give users access to the Security & Compliance Center](../grant-access-to-the-security-and-compliance-center.md).</span></span> 

- <span data-ttu-id="ea224-p105">어떤 사용자 사서함 및 OneDrive 계정을 조사 하는 사람을 검색할 수를 제어 하려면 조직 준수 경계와 설정할 수 있습니다. 자세한 내용은 [eDiscovery 조사에 대 한 준수 경계를 설정](../set-up-compliance-boundaries.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p105">To control which user mailboxes and OneDrive accounts an investigator can search, your organization can set up compliance boundaries. For more information, [Set up compliance boundaries for eDiscovery investigations](../set-up-compliance-boundaries.md).</span></span> 

## <a name="step-1-create-a-data-investigation"></a><span data-ttu-id="ea224-129">1 단계: 데이터 조사 만들기</span><span class="sxs-lookup"><span data-stu-id="ea224-129">Step 1: Create a data investigation</span></span>

<span data-ttu-id="ea224-130">데이터 조사를 만들려면:</span><span class="sxs-lookup"><span data-stu-id="ea224-130">To create a data investigation:</span></span>

1. <span data-ttu-id="ea224-131">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-131">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="ea224-132">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-132">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="ea224-133">보안 & 준수 센터에서에서 **데이터 조사**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-133">In the Security & Compliance Center, click **Data Investigations**.</span></span>
 
4. <span data-ttu-id="ea224-134">**데이터 조사 (미리 보기)** 페이지에서 **새 조사 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-134">On the **Data Investigations (Preview)** page, click **Create a new investigation**.</span></span>
    
5. <span data-ttu-id="ea224-p106">**새 데이터 조사** 플라이 아웃 페이지 (필수) 이름을 조사를 지정 하 고는 선택적 조사 번호와 설명을 입력 합니다. 참고 이름은 조직 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p106">On the **New data investigation** flyout page, give the investigation a name (required), and then type an optional investigation number and description. Note that the name must be unique in your organization.</span></span>

6. <span data-ttu-id="ea224-137">아래에서 **이 조사를 만든 후 추가 설정을 구성 하 시겠습니까?**, 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-137">Under **Do you want to configure additional settings after creating this investigation?**, do one of the following:</span></span>

    - <span data-ttu-id="ea224-p107">**예** 를 조사, 만들기를 클릭 하 고 새 경우에서 **설정** 페이지를 표시 합니다. 이 옵션을 사용 하면 조사에 구성원을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p107">Click **Yes** to create the investigation, and display the **Settings** page in the new case. This allows you to add members to the investigation.</span></span>
    
    - <span data-ttu-id="ea224-p108">방금 조사를 만들고 **데이터 조사 (미리 보기)** 페이지의 경우 목록에서 표시 하려면 **아니요** 클릭 합니다. 이 옵션을 선택 하면 추가 될 경우 조사 하 고 기본 검색 및 분석 설정의 유일한 구성원 사용 됩니다. 구성원을 추가 또는 조사를 만든 후 언제 든 지 설정을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p108">Click **No** to just create the investigation and display it in the list of cases on the **Data Investigations (Preview)** page. If you choose this option, you will be added as the only member of the investigation and the default search and analytics settings will be used. You can add members or change settings any time after the investigation is created.</span></span>

7. <span data-ttu-id="ea224-143">조사를 만들려면 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-143">Click **Save** to create the investigation.</span></span>

    <span data-ttu-id="ea224-144">새 조사 **데이터 조사 (미리 보기)** 페이지의 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-144">The new investigation is displayed in the list on the **Data Investigations (Preview)** page.</span></span> 

8. <span data-ttu-id="ea224-145">조사를 열려면 조사의 이름을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-145">To open an investigation, click the name of the investigation.</span></span> 

    <span data-ttu-id="ea224-146">**홈** 탭의 조사를 위해 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-146">The **Home** tab for the investigation is displayed.</span></span> 

> [!TIP]
> <span data-ttu-id="ea224-147">조사에 대 한 명명 규칙을 설정 하는 것이 좋습니다. 하 고 찾을 하 고 필요한 경우를 나중에 참조할 수 있도록 이름 및 설명 수 만큼 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-147">Consider establishing a naming convention for investigations and provide as much information as you can in the name and description so you can locate and refer to in the future if necessary.</span></span>
 
## <a name="step-2-search-for-the-spilled-data"></a><span data-ttu-id="ea224-148">Spilled 데이터에 대 한 2 단계: 검색</span><span class="sxs-lookup"><span data-stu-id="ea224-148">Step 2: Search for the spilled data</span></span> 
 
<span data-ttu-id="ea224-p109">넘어가 데이터에 대 한 검색 하려는 사용자를 알고 있는 경우에 조사 해당 데이터 원본에 매핑한 빠르게 검색 하 여 자신의 사서함 및 OneDrive 계정에 관심 있는 사람으로 추가할 수 있습니다. 경우 조사 관심 있는 사람을 추가 하려면 **관심 있는 사람**클릭 하 고 **관심 사람에 추가**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p109">If you know which users you want to search for spilled data, you can add them as people of interest to map their data sources to the investigation and quickly search their mailbox and OneDrive account. To add people of interest to the investigation, click **People of interest**, and then click **Add people of interest**.</span></span> 

<span data-ttu-id="ea224-p110">**검색** 탭을 찾으려면 spilled 데이터 검색을 만들 수 있습니다. [4 단계에서](##step-4:-permanently-delete-the-spilled-data)에서 이러한 같은 메시지를 삭제 하려면 spilled 데이터를 찾는 데 사용 하는 동일한 검색 쿼리를 사용 합니다. 만들기 검색 하는 방법에 대 한 자세한 내용은 [만들기 데이터 수집에 대 한 검색을](create-search-to-collect-data.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ea224-p110">On the **Searches** tab, you can create searches to find the spilled data. You will use the same search query that you used to find the spilled data to delete those same messages in [Step 4](##step-4:-permanently-delete-the-spilled-data). For more information about creating searches, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="ea224-p111">검색을 실행 하면 검색 결과 및 보기 검색 통계 검색 쿼리와의 효율성을 평가 하는 예제를 미리볼 수 있습니다. Office 365에서 삭제 하려는 항목을 식별 한 후 수 **사고** 탭을 클릭 하 고 인시던트를 만들고 해당 항목을 포함 하는 검색 결과 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p111">After you run the search, you can preview samples of search results and view search statistics to evaluate the effectiveness of your search query. Once you identify the items that you want to delete from Office 365, you can click the **Incidents** tab, and then create an incident and add search results that contain those items.</span></span> 

<span data-ttu-id="ea224-p112">이 작업을 수행 하 게 조사 하려는 검색을 클릭 합니다. 플라이 아웃 페이지에서 **인시던트를 추가 결과** 클릭 하 고 지시를 따릅니다. 다음 사고, 개별 문서를 검토, 문서에 대 한 액세스를 있었을 조사 하 고 수는 문서를 내보냅니다. 단순히 검토 하는 대신 문서를 삭제 하려면 4 [단계로](##step-4:-permanently-delete-the-spilled-data)이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p112">To do this, click the search that you want to investigate. On the flyout page, click **Add results to incident** and follow the instructions. Then in the incident, you can review individual documents, investigate who had access to documents, and export the documents. To simply delete the documents instead of reviewing them, go to [Step 4](##step-4:-permanently-delete-the-spilled-data).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="ea224-p113">검색 쿼리에 사용 하 여 키워드에 대 한 검색 하는 실제 spilled 데이터를 포함할 수 있습니다. 예를 사회보장 번호와 사용자를 포함 하는 문서에 대 한 검색 검색 쿼리에 키워드도이 옵션을 사용할 경우에 액체 엎질렀는지 여부를 방지 하려면 나중에 쿼리를 삭제 해야 합니다. 검색을 삭제 하거나 [5 단계에서](##step-5:-close-or-delete-investigation)에서 전체 조사를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p113">The keywords that you use in the search query may contain the actual spilled data that you're searching for. For example, if you searching for documents containing a social security number and you use it as a keyword in the search query, you must delete the query afterwards to avoid further spillage. You can delete search or delete the entire investigation in [Step 5](##step-5:-close-or-delete-investigation).</span></span> 

## <a name="step-3-review-and-investigate"></a><span data-ttu-id="ea224-163">3 단계: 검토 하 고 조사</span><span class="sxs-lookup"><span data-stu-id="ea224-163">Step 3: Review and investigate</span></span> 

<span data-ttu-id="ea224-p114">조사에 **사고** 탭으로 이동 하 고 이전 단계에서 만든 인시던트를 클릭 합니다. 처리 작업이 완료 되 고 검색 결과 사고에 추가 된, 후에 원시 형식으로, 텍스트 형식 또는 네이티브 근처 형식에서 개별 문서를 검토할 수 있습니다. 문서 및 사용자 조사에 대 한 결과 나타내기 위해 태그 문서 목록 범위를 더 좁힐 추가 쿼리를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p114">In the investigation, go to **Incidents** tab and click on the incident that you created in the previous step. After the processing job is completed and the search results are added to the incident, you can review individual documents in their native format, text format, or a near-native format. You can create additional queries to further narrow the list of documents, and tag documents to indicate findings from your investigation.</span></span>

<span data-ttu-id="ea224-p115">문서를 그룹화 하 고 검토를 위해 더 많은 도움을 받을 하려면 **관리 인시던트**를 클릭 합니다. **분석** 타일에서 **분석**을 클릭 합니다. 중복 검색, 스레딩, 전자 메일 및 테마 분석와 같은 고급 분석을 실행 됩니다. 자세한 내용은 다음을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p115">To group documents and get more assistance for your review, click **Manage incident**. In the **Analytics** tile, click **Analyze**. This will run advanced analytics such as duplicate detection, email threading, and theme analysis. For more information, see:</span></span>

- [<span data-ttu-id="ea224-171">중복에 가까운 검색</span><span class="sxs-lookup"><span data-stu-id="ea224-171">Near duplicate detection</span></span>](near-duplicates.md)
- [<span data-ttu-id="ea224-172">전자 메일 스레드</span><span class="sxs-lookup"><span data-stu-id="ea224-172">Email threading</span></span>](email-threading.md)
- [<span data-ttu-id="ea224-173">테마</span><span class="sxs-lookup"><span data-stu-id="ea224-173">Themes</span></span>](themes.md)

<span data-ttu-id="ea224-p116">데이터 액체 엎질렀는지 여부에 관련 된 사용자를 확인 하려면 사고에서 새 쿼리를 만들 수 있으며 보낸사람/작성자 및 받는 사람 조건을 사용 하 여 다음 키를 누릅니다. 이렇게 하면 모든 보낸사람, 받는 사람 및 사고에 추가 된 수집 된 데이터에 있는 작성자 목록이 만들어집니다. 목록에 외부 사용자는 모두 있는지 확인 하려면 목록을 검토 해야 합니다. 자세한 내용은 [검색 조건](../keyword-queries-and-search-conditions.md#search-conditions)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ea224-p116">To determine which users are involved in the data spillage, you can create a new query in the incident and then use the Sender/Author and Recipients conditions. This will create a list of all senders, recipients and authors found in collected data that was added to the incident. Be sure to examine the list to determine if there are any external users in the list. For more information, see [Search conditions](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>

## <a name="step-4-permanently-delete-the-spilled-data"></a><span data-ttu-id="ea224-178">4 단계: spilled 데이터를 영구적으로 삭제</span><span class="sxs-lookup"><span data-stu-id="ea224-178">Step 4: Permanently delete the spilled data</span></span>

### <a name="deleting-mailbox-items"></a><span data-ttu-id="ea224-179">사서함 항목을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-179">Deleting mailbox items</span></span>

<span data-ttu-id="ea224-p117">검토 하 고 검색 결과 삭제 해야 하는 전자 메일 메시지를 포함 하는 유효성 검사 후 있습니다 영구적으로 삭제할 수를 실행 하 여는 **새로 ComplianceSearchAction--PurgeType HardDelete 항목 지우기** 보안 & 준수에에서 명령 센터 PowerShell 합니다. 자세한 내용은 [대 한 검색 및 삭제 전자 메일 메시지를](../search-for-and-delete-messages-in-your-organization.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ea224-p117">After you review and validate that the search results contain only the email messages that must be deleted, you can permanently delete them by running the **New-ComplianceSearchAction -Purge -PurgeType HardDelete** command in Security & Compliance Center PowerShell. For instructions, see [Search for and delete email messages](../search-for-and-delete-messages-in-your-organization.md).</span></span> 

<span data-ttu-id="ea224-p118">사용자의 복구 가능한 항목 폴더에 보관 함 (및 관리자가 액세스할 수 있는) 하면 조직에서 사서함에 대 한 단일 항목 복구를 사용 하는 경우 항목을 영구적으로 삭제 하는 내용의 됩니다 (기본값은 14 일) 삭제 된 항목 보존 기간 끝까지 합니다. 또한 넘어가 데이터를 포함 하는 사서함의 법적 보존 또는 보존 정책에 할당 된, 하는 경우 제거 된 메시지에에서 유지 됩니다 복구 가능한 항목 폴더 보존이 제거 시키거나 사서함 보존 정책에서 제외 됩니다. 하드 삭제 메시지에 즉시 추가 작업을 수행 해야 합니다. 자세한 내용은 [폴더에 있는 클라우드 기반 사서함의 대기 복구 가능한 항목에서 항목을 삭제 ](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p118">Note that if single item recovery is enabled for mailboxes in your organization, permanently deleted items will be retained in the user's Recoverable items folder (and accessible by admins) until the deleted item retention period ends (default is 14 days). Additionally, if any of the mailboxes that contain spilled data are on a legal hold or assigned to a retention policy, purged message will be retained in Recoverable items folder until the hold is removed or the mailbox is excluded from retention policies. To hard delete messages immediately, you need to perform addition tasks. For instructions, see [Delete items in the Recoverable Items folder of cloud-based mailboxes on hold ](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="ea224-p119">보류 또는 보존 정책을 제거 하기 전에 레코드 관리 또는 법률 부서를 확인 합니다. 조직에서 사서함에 보존 여부를 정의 하는 정책을 이미 또는 데이터 액체 엎질렀는지 여부 문제가 발생 한 설정이 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p119">Check with your records management or legal departments before removing a hold or retention policy. Your organization may have a policy that defines whether a mailbox on hold or a data spillage incident takes priority.</span></span> 

### <a name="deleting-site-items"></a><span data-ttu-id="ea224-188">사이트 항목 삭제</span><span class="sxs-lookup"><span data-stu-id="ea224-188">Deleting site items</span></span>

<span data-ttu-id="ea224-p120">비즈니스 계정에 대 한 OneDrive 또는 SharePoint 사이트에서 문서를 영구적으로 삭제를 삭제 해야 하 고 사이트에서 삭제 한 다음 사이트 모음 휴지통에서에서 삭제 해야 합니다. 자세한 내용은 [SharePoint와 OneDrive에서 문서를 삭제](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business)합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p120">To permanently delete a document from a SharePoint site or OneDrive for Business account, you have to delete it and then you have to delete from the site and then delete it from the site collection Recycle Bin. For instructions, see [Delete documents in SharePoint and OneDrive](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business).</span></span>

<span data-ttu-id="ea224-p121">또는 넘어가 데이터를 포함 수 있는 전체 사이트 모음을 삭제할 수 있습니다. 자세한 내용은 [사이트 모음을 삭제](https://docs.microsoft.com/sharepoint/delete-site-collection)합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p121">Alternatively, you can delete an entire site collection that might contained spilled data. For instructions, see [Delete a site collection](https://docs.microsoft.com/sharepoint/delete-site-collection).</span></span>

## <a name="step-5-close-or-delete-the-investigation"></a><span data-ttu-id="ea224-193">5 단계:을 닫거나 조사를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-193">Step 5: Close or delete the investigation</span></span>

<span data-ttu-id="ea224-p122">원본 콘텐츠 위치 (사서함 또는 사이트)에서 문서를 삭제 한 후에 조사 보안 문제에 추가 된 이러한 문서의 복사본 여전히 해야 합니다. 추가 데이터 액체 엎질렀는지 여부를 방지 하려면 조사 삭제 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p122">After you delete documents in the source content locations (mailboxes or sites), you will still have copies of these documents that you added to incidents as part of your investigation. To avoid further data spillage, you should consider deleting the investigation.</span></span>

<span data-ttu-id="ea224-196">조사를 삭제 하는 방법:</span><span class="sxs-lookup"><span data-stu-id="ea224-196">To delete an investigation:</span></span>

1. <span data-ttu-id="ea224-197">**설정** 탭에서 **조사 정보**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-197">On the **Settings** tab, click **Investigation information**.</span></span>

2. <span data-ttu-id="ea224-198">**대/소문자를 삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-198">Click  **Delete case**.</span></span> 

<span data-ttu-id="ea224-p123">조사를 삭제할 필요가 없습니다 조사 중에 수집 된 정보를 저장 하려는 경우 **사례 닫기**을 클릭 합니다. 나중에 닫힌된 조사를 다시 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea224-p123">If you don't need to delete the investigation or if you want to save the information that you collected during the investigation, you can click **Close case**. At a later date, you can re-open closed investigations.</span></span>