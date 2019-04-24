---
title: custodian 감사 작업 보기
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
description: ''
ms.openlocfilehash: defc89f1d54238e62f947fd197e7a866380ee601
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32241044"
---
# <a name="view-custodian-audit-activity"></a><span data-ttu-id="0bb99-102">custodian 감사 작업 보기</span><span class="sxs-lookup"><span data-stu-id="0bb99-102">View custodian audit activity</span></span>

<span data-ttu-id="0bb99-103">사용자가 특정 문서를 보거나 사서함에서 항목을 삭제 한 경우를 확인 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="0bb99-103">Need to find if a user viewed a specific document or purged an item from their mailbox?</span></span> <span data-ttu-id="0bb99-104">이제 Advanced eDiscovery (Preview)가 보안 & 준수 센터의 기존 감사 로그 검색 도구와 통합 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-104">Advanced eDiscovery (Preview) is now integrated with the existing audit log search tool in the Security & Compliance Center.</span></span> <span data-ttu-id="0bb99-105">이러한 임베디드 환경을 사용 하는 경우 Advanced eDiscovery (Preview) Custodian 관리 도구를 사용 하 여 사례 내에서 custodians에 대 한 작업을 쉽게 액세스 하 고 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-105">Using this embedded experience, you can use the Advanced eDiscovery (Preview) Custodian Management tool to facilitate your investigation by easily accessing and searching the activity for custodians within your case.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="0bb99-106">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="0bb99-106">Before you begin</span></span>

<span data-ttu-id="0bb99-107">Office 365 감사 로그를 검색 하려면 Exchange Online에서 보기 전용 감사 로그 또는 감사 로그 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-107">You have to be assigned the View-Only Audit Logs or Audit Logs role in Exchange Online to search the Office 365 audit log.</span></span> <span data-ttu-id="0bb99-108">기본적으로 이러한 역할은 Exchange 관리 센터의 사용 권한 페이지에 있는 준수 관리 및 조직 관리 역할 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-108">By default, these roles are assigned to the Compliance Management and Organization Management role groups on the Permissions page in the Exchange admin center.</span></span> <span data-ttu-id="0bb99-109">사용자에 게 최소 수준의 권한으로 Advanced eDiscovery (미리 보기) 감사 로그를 검색할 수 있는 기능을 제공 하려면 Exchange Online에서 사용자 지정 역할 그룹을 만들고 보기 전용 감사 로그 또는 감사 로그 역할을 추가한 다음 사용자를 새 역할 gr의 구성원으로 추가 하면 됩니다. oup</span><span class="sxs-lookup"><span data-stu-id="0bb99-109">To give a user the ability to search the Advanced eDiscovery (Preview) audit log with the minimum level of privileges, you can create a custom role group in Exchange Online, add the View-Only Audit Logs or Audit Logs role, and then add the user as a member of the new role group.</span></span> <span data-ttu-id="0bb99-110">자세한 내용은 Exchange Online에서 역할 그룹 관리를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0bb99-110">For more information, see Manage role groups in Exchange Online.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bb99-111">보안 & 준수 센터의 사용 권한 페이지에서 사용자에 게 보기 전용 감사 로그 또는 감사 로그 역할을 할당 하면 Office 365 감사 로그를 검색할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-111">If you assign a user the View-Only Audit Logs or Audit Logs role on the Permissions page in the Security & Compliance Center, they won't be able to search the Office 365 audit log.</span></span> <span data-ttu-id="0bb99-112">Exchange Online에서 사용 권한을 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-112">You have to assign the permissions in Exchange Online.</span></span> <span data-ttu-id="0bb99-113">이는 감사 로그를 검색 하는 데 사용 되는 기본 cmdlet이 Exchange Online cmdlet 이기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-113">This is because the underlying cmdlet used to search the audit log is an Exchange Online cmdlet.</span></span>

## <a name="step-1-create-an-advanced-ediscovery-preview-audit-log-search"></a><span data-ttu-id="0bb99-114">1 단계: 고급 eDiscovery (미리 보기) 감사 로그 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="0bb99-114">Step 1: Create an Advanced eDiscovery (Preview) audit log search</span></span>

   1. <span data-ttu-id="0bb99-115">**Security & 준수 센터 > Advanced eDiscovery (Preview)** 에서 기존 사례를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-115">Select an existing case from the **Security & Compliance Center > Advanced eDiscovery (Preview)**.</span></span>
   
   2. <span data-ttu-id="0bb99-116">**Custodians** 탭으로 이동 하 여 custodian을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-116">Navigate to the **Custodians** tab and select a custodian.</span></span>
   
   3. <span data-ttu-id="0bb99-117">custodian을 선택한 후</span><span class="sxs-lookup"><span data-stu-id="0bb99-117">Once you have selected a custodian, click</span></span>  ![Custodian 활동 보기](../media/ViewCustodianActivity.PNG)  <span data-ttu-id="0bb99-119">세부 정보 패널</span><span class="sxs-lookup"><span data-stu-id="0bb99-119">from the details panel.</span></span>
   
   4. <span data-ttu-id="0bb99-120">다음 검색 조건을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-120">Configure the following search criteria:</span></span>
      
      <span data-ttu-id="0bb99-121">위한.</span><span class="sxs-lookup"><span data-stu-id="0bb99-121">a.</span></span> <span data-ttu-id="0bb99-122">**활동** -드롭다운 목록을 클릭 하 여 검색할 수 있는 활동을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-122">**Activities** - Click the drop-down list to display the activities that you can search for.</span></span> <span data-ttu-id="0bb99-123">검색을 실행 한 후에는 선택한 활동에 대 한 감사 레코드만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-123">After you run the search, only the audit records for the selected activities are displayed.</span></span> <span data-ttu-id="0bb99-124">**모든 작업에 대해 결과 표시** 를 선택 하면 다른 검색 조건을 충족 하는 모든 작업에 대 한 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-124">Selecting **Show results for all activities** will display results for all activities that meet the other search criteria.</span></span>

      ![활동 목록](../media/CustodianActivityAudit.PNG)
      
      <span data-ttu-id="0bb99-126">b.</span><span class="sxs-lookup"><span data-stu-id="0bb99-126">b.</span></span> <span data-ttu-id="0bb99-127">**시작 날짜 및 종료 날짜** -해당 기간 내에 발생 한 이벤트를 표시 하려면 날짜 및 시간 범위를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-127">**Start date and End date** - Select a date and time range to display the events that occurred within that period.</span></span> <span data-ttu-id="0bb99-128">지난 7 일이 기본적으로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-128">The last seven days are selected by default.</span></span> <span data-ttu-id="0bb99-129">날짜와 시간은 utc (협정 세계시) 형식으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-129">The date and time are presented in Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="0bb99-130">지정할 수 있는 최대 날짜 범위는 1 년입니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-130">The maximum date range that you can specify is one year.</span></span>
      
      <span data-ttu-id="0bb99-131">&.</span><span class="sxs-lookup"><span data-stu-id="0bb99-131">c.</span></span> <span data-ttu-id="0bb99-132">이 상자를 **Custodians** 클릭 한 다음 특정 custodian을 선택 하 여 검색 결과를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-132">**Custodians** - Click in this box and then select a specific custodian to display search results for.</span></span> <span data-ttu-id="0bb99-133">이 상자에서 선택한 사용자가 수행한 선택한 작업에 대 한 감사 레코드가 결과 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-133">Audit records for the selected activity performed by the users you select in this box are displayed in the list of results.</span></span>
      
   5. <span data-ttu-id="0bb99-134">누른</span><span class="sxs-lookup"><span data-stu-id="0bb99-134">Click</span></span>   ![검색 단추](../media/SearchButton.PNG)  <span data-ttu-id="0bb99-136">검색 조건을 사용 하 여 검색을 실행 하려면</span><span class="sxs-lookup"><span data-stu-id="0bb99-136">to run the search using your search criteria.</span></span> <span data-ttu-id="0bb99-137">검색 결과가 로드 되 고 몇 분 후에 Custodian 작업 검색 페이지에서 결과 아래에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-137">The search results are loaded, and after a few moments they are displayed under Results on the Custodian Activities search page.</span></span> 

## <a name="step-2-view-the-audit-log-search-results"></a><span data-ttu-id="0bb99-138">2 단계: 감사 로그 검색 결과 보기</span><span class="sxs-lookup"><span data-stu-id="0bb99-138">Step 2: View the audit log search results</span></span>

<span data-ttu-id="0bb99-139">감사 로그 검색의 결과는 Custodian 감사 로그 페이지의 결과 아래에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-139">The results of an audit log search are displayed under Results on the Custodian Audit log page.</span></span> <span data-ttu-id="0bb99-140">최대 5000 (최신) 이벤트는 150 이벤트 단위로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-140">A maximum of 5,000 (newest) events are displayed in increments of 150 events.</span></span> <span data-ttu-id="0bb99-141">더 많은 이벤트를 표시 하려면 결과 창에서 스크롤 막대를 사용 하거나 Shift + End를 눌러 다음 150 이벤트를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-141">To display more events you can use the scroll bar in the Results pane or you can press Shift + End to display the next 150 events.</span></span>

<span data-ttu-id="0bb99-142">결과에는 검색에서 반환 된 각 이벤트에 대 한 다음과 같은 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-142">The results contain the following information about each event returned by the search.</span></span>
- <span data-ttu-id="0bb99-143">**date**: 이벤트가 발생 한 날짜 및 시간 (UTC 형식)입니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-143">**Date**: The date and time (in UTC format) when the event occurred.</span></span>

- <span data-ttu-id="0bb99-144">**IP 주소**: 활동을 로깅할 때 사용 된 장치의 ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-144">**IP address**: The IP address of the device that was used when the activity was logged.</span></span> <span data-ttu-id="0bb99-145">IP 주소는 IPv4 또는 IPv6 주소 형식으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-145">The IP address is displayed in either an IPv4 or IPv6 address format.</span></span>

- <span data-ttu-id="0bb99-146">**사용자**: 이벤트를 트리거한 작업을 수행한 사용자 또는 서비스 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-146">**User**: The user (or service account) who performed the action that triggered the event.</span></span>

- <span data-ttu-id="0bb99-147">**활동**: 사용자가 수행 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-147">**Activity**: The activity performed by the user.</span></span> <span data-ttu-id="0bb99-148">이 값은 활동 드롭다운 목록에서 선택한 활동에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-148">This value corresponds to the activities that you selected in the Activities drop down list.</span></span> <span data-ttu-id="0bb99-149">exchange 관리자 감사 로그의 이벤트에 대해이 열의 값은 exchange cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-149">For an event from the Exchange admin audit log, the value in this column is an Exchange cmdlet.</span></span>

- <span data-ttu-id="0bb99-150">**Item**: 해당 활동의 결과로 만들어지거나 수정 된 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-150">**Item**: The object that was created or modified as a result of the corresponding activity.</span></span> <span data-ttu-id="0bb99-151">예를 들어, 보거나 수정한 파일 또는 업데이트 된 사용자 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-151">For example, the file that was viewed or modified or the user account that was updated.</span></span> <span data-ttu-id="0bb99-152">모든 활동에이 열에 대 한 값이 있는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-152">Not all activities have a value in this column.</span></span>

- <span data-ttu-id="0bb99-153">**세부 정보**: 활동에 대 한 추가 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-153">**Detail**: Additional detail about an activity.</span></span> <span data-ttu-id="0bb99-154">다시 말하지만 모든 작업에는 값이 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-154">Again, not all activities will have a value.</span></span>

## <a name="step-3-filter-the-search-results"></a><span data-ttu-id="0bb99-155">3 단계: 검색 결과 필터링</span><span class="sxs-lookup"><span data-stu-id="0bb99-155">Step 3: Filter the search results</span></span>

<span data-ttu-id="0bb99-156">정렬 외에도 감사 로그 검색의 결과를 필터링 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-156">In addition to sorting, you can also filter the results of an audit log search.</span></span> <span data-ttu-id="0bb99-157">이를 통해 특정 사용자 또는 활동에 대 한 결과를 빠르게 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-157">This can help you quickly filter the results for a specific user or activity.</span></span> 

<span data-ttu-id="0bb99-158">결과를 필터링 하려면</span><span class="sxs-lookup"><span data-stu-id="0bb99-158">To filter the results:</span></span>

 1. <span data-ttu-id="0bb99-159">감사 로그 검색을 만들어 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-159">Create and run an audit log search.</span></span>
  
2. <span data-ttu-id="0bb99-160">결과가 표시 되 면 **필터 결과**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-160">When the results are displayed, click **Filter results**.</span></span>
 
3. <span data-ttu-id="0bb99-161">각 열 머리글 아래에 키워드 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-161">Keyword boxes are displayed under each column header.</span></span>
  
4. <span data-ttu-id="0bb99-162">필터링 하는 열에 따라 열 머리글 아래의 상자 중 하나를 클릭 하 고 단어 또는 구를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-162">Click one of the boxes under a column header and type a word or phrase, depending on the column you're filtering on.</span></span> <span data-ttu-id="0bb99-163">결과가 동적으로 readjust 필터와 일치 하는 이벤트가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-163">The results will dynamically readjust to display the events that match your filter.</span></span>
  
5. <span data-ttu-id="0bb99-164">필터를 지우려면 필터 상자에서 **X** 를 클릭 하거나 **필터링 숨기기**를 클릭 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-164">To clear a filter, click the **X** in the filter box or just click **Hide filtering**.</span></span>

## <a name="export-the-search-results-to-a-file"></a><span data-ttu-id="0bb99-165">검색 결과를 파일로 내보내기</span><span class="sxs-lookup"><span data-stu-id="0bb99-165">Export the search results to a file</span></span>

<span data-ttu-id="0bb99-166">감사 로그 검색 결과를 로컬 컴퓨터의 CSV (쉼표로 구분 된 값) 파일로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-166">You can export the results of an audit log search to a comma separated value (CSV) file on your local computer.</span></span> <span data-ttu-id="0bb99-167">Microsoft Excel에서이 파일을 열고, 검색, 정렬, 필터링, 다중 값 셀이 포함 된 단일 열을 여러 열로 분할 등의 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-167">You can open this file in Microsoft Excel and use features such as search, sorting, filtering, and splitting a single column (that contains multi-value cells) into multiple columns.</span></span>

1. <span data-ttu-id="0bb99-168">감사 로그 검색을 실행 한 다음 원하는 결과가 나올 때까지 검색 조건을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-168">Run an audit log search, and then revise the search criteria until you have the desired results.</span></span>
  
2. <span data-ttu-id="0bb99-169">결과 내보내기를 클릭 하 고 다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-169">Click Export results and select one of the following options:</span></span>

    - <span data-ttu-id="0bb99-170">**로드 된 결과 저장:** **Custodian 감사 로그 검색** 페이지의 **결과** 에 표시 되는 항목만 내보내려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-170">**Save loaded results:** Choose this option to export only the entries that are displayed under **Results** on the **Custodian Audit log search** page.</span></span> <span data-ttu-id="0bb99-171">다운로드 되는 CSV 파일에는 페이지 (날짜, 사용자, 작업, 항목 및 세부 정보)에 표시 되는 것과 동일한 열 (및 데이터)이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-171">The CSV file that is downloaded contains the same columns (and data) displayed on the page (Date, User, Activity, Item, and Details).</span></span> <span data-ttu-id="0bb99-172">CSV 파일에는 감사 로그 항목에서 더 많은 정보가 포함 된 추가 열 ( **더 자세히**)이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-172">An additional column (titled **More**) is included in the CSV file that contains more information from the audit log entry.</span></span> <span data-ttu-id="0bb99-173">감사 로그 검색 페이지에서 로드 되 고 볼 수 있는 것과 동일한 결과를 내보내기 때문에 최대 5000 개의 항목을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-173">Because you're exporting the same results that are loaded (and viewable) on the Audit log search page, a maximum of 5,000 entries are exported.</span></span>
        
    - <span data-ttu-id="0bb99-174">**모든 결과를 다운로드 합니다.** 검색 조건을 충족 하는 Office 365 감사 로그의 모든 항목을 내보내려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-174">**Download all results:** Choose this option to export all entries from the Office 365 audit log that meet the search criteria.</span></span> <span data-ttu-id="0bb99-175">많은 검색 결과 집합의 경우 **Custodian 감사 로그** 검색 페이지에 표시할 수 있는 5000 결과 외에도 감사 로그의 모든 항목을 다운로드 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-175">For a large set of search results, choose this option to download all entries from the audit log in addition to the 5,000 results that can be displayed on the **Custodian Audit log** search page.</span></span> <span data-ttu-id="0bb99-176">이 옵션은 감사 로그의 원시 데이터를 CSV 파일로 다운로드 하 고 감사 로그 항목에서 auditdata 라는 열에 대 한 추가 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-176">This option will download the raw data from the audit log to a CSV file, and contains additional information from the audit log entry in a column named AuditData.</span></span> <span data-ttu-id="0bb99-177">다른 옵션을 선택 하는 경우이 내보내기 옵션을 선택 하면 다운로드 한 파일 보다 훨씬 커질 수 있으므로 파일을 다운로드 하는 데 시간이 오래 걸릴 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-177">It may take longer to download the file if you choose this export option because the file may be much larger than the one that's downloaded if you choose the other option.</span></span>
    
      > [!IMPORTANT]
      > <span data-ttu-id="0bb99-178">단일 감사 로그 검색에서 최대 5만 개의 항목을 CSV 파일에 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-178">You can download a maximum of 50,000 entries to a CSV file from a single audit log search.</span></span> <span data-ttu-id="0bb99-179">5만 항목이 CSV 파일에 다운로드 되는 경우 검색 조건을 충족 하는 이벤트가 5만 개 보다 많은 것으로 간주할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-179">If 50,000 entries are downloaded to the CSV file, you can probably assume there are more than 50,000 events that met the search criteria.</span></span> <span data-ttu-id="0bb99-180">이 제한 보다 많은 시간을 내보내려면 날짜 범위를 사용 하 여 감사 로그 항목 수를 줄이십시오.</span><span class="sxs-lookup"><span data-stu-id="0bb99-180">To export more than this limit, try using a date range to reduce the number of audit log entries.</span></span> <span data-ttu-id="0bb99-181">5만 개 보다 많은 항목을 내보내려면 날짜 범위가 더 작은 검색을 여러 개 실행 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-181">You might have to run multiple searches with smaller date ranges to export more than 50,000 entries.</span></span>
        

3. <span data-ttu-id="0bb99-182">내보내기 옵션을 선택한 후에는 CSV 파일을 열거나 다운로드 폴더에 저장 하거나 특정 폴더에 저장 하 라는 메시지를 창 아래쪽에 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb99-182">After you select an export option, a message is displayed at the bottom of the window that prompts you to open the CSV file, save it to the Downloads folder, or save it to a specific folder</span></span>

<span data-ttu-id="0bb99-183">감사 로그 검색 결과를 보거나 필터링 하거나 내보내는 방법에 대 한 자세한 내용은 [search the audit log in the Office 365 Security & 준수 센터](../search-the-audit-log-in-security-and-compliance.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="0bb99-183">For more information about viewing, filtering, or exporting audit log search results, see [Search the audit log in the Office 365 Security & Compliance Center](../search-the-audit-log-in-security-and-compliance.md).</span></span>
