---
title: 더불어 감사 활동 보기
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
description: ''
ms.openlocfilehash: 34e3fe207cf440c5992cdba7186e919a3968db22
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706149"
---
# <a name="view-custodian-audit-activity"></a><span data-ttu-id="20048-102">더불어 감사 활동 보기</span><span class="sxs-lookup"><span data-stu-id="20048-102">View custodian audit activity</span></span>

<span data-ttu-id="20048-p101">사용자는 특정 문서를 볼 또는 자신의 사서함에서 항목을 제거 하는 경우를 찾이 필요가 있습니까? 고급 eDiscovery (미리 보기) 보안 & 준수 센터의에서 기존 감사 로그 검색 도구와 통합 되었습니다. 이 포함 된 경험을 사용 하 여 쉽게 액세스 하 고 케이스 내에서 custodians에 대 한 활동을 검색 하 여 검사를 수행할 수 있도록 고급 eDiscovery (미리 보기) 더불어 관리 도구를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p101">Need to find if a user viewed a specific document or purged an item from their mailbox? Advanced eDiscovery (Preview) is now integrated with the existing audit log search tool in the Security & Compliance Center. Using this embedded experience, you can use the Advanced eDiscovery (Preview) Custodian Management tool to facilitate your investigation by easily accessing and searching the activity for custodians within your case.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="20048-106">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="20048-106">Before you begin</span></span>

<span data-ttu-id="20048-p102">보기 전용 감사 로그 또는 감사 로그 역할 Exchange Online에 할당할 Office 365 감사 로그를 검색 해야 합니다. 기본적으로 이러한 역할은 규정 준수 관리 및 Exchange 관리 센터에서 사용 권한 페이지에서 조직 관리 역할 그룹에 할당 됩니다. 사용자 최소 수준의 권한 사용 하 여 고급 eDiscovery (미리 보기) 감사 로그를 검색 하는 기능을 부여 하려면 Exchange Online에서 사용자 지정 역할 그룹을 만들, 보기 전용 감사 로그 또는 감사 로그 역할을 추가한 다음 새 역할이 구성원으로 사용자를 추가 oup 합니다. 자세한 내용은 Exchange Online의 관리 역할 그룹을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="20048-p102">You have to be assigned the View-Only Audit Logs or Audit Logs role in Exchange Online to search the Office 365 audit log. By default, these roles are assigned to the Compliance Management and Organization Management role groups on the Permissions page in the Exchange admin center. To give a user the ability to search the Advanced eDiscovery (Preview) audit log with the minimum level of privileges, you can create a custom role group in Exchange Online, add the View-Only Audit Logs or Audit Logs role, and then add the user as a member of the new role group. For more information, see Manage role groups in Exchange Online.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20048-p103">사용자 보안 & 준수 센터의에서 사용 권한 페이지에서 보기 전용 감사 로그 또는 감사 로그 역할을 할당 하는 경우 Office 365 감사 로그를 검색할 수 있도록 할 수 없습니다. Exchange Online에서 사용 권한을 할당 해야 합니다. 감사 로그를 검색 하는 데 사용 하는 원본으로 사용 cmdlet은 Exchange Online cmdlet 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p103">If you assign a user the View-Only Audit Logs or Audit Logs role on the Permissions page in the Security & Compliance Center, they won't be able to search the Office 365 audit log. You have to assign the permissions in Exchange Online. This is because the underlying cmdlet used to search the audit log is an Exchange Online cmdlet.</span></span>

## <a name="step-1-create-an-advanced-ediscovery-preview-audit-log-search"></a><span data-ttu-id="20048-114">1 단계: 고급 eDiscovery (미리 보기) 감사 로그 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="20048-114">Step 1: Create an Advanced eDiscovery (Preview) audit log search</span></span>

   1. <span data-ttu-id="20048-115">**보안 & 준수 센터 gt_ 고급 eDiscovery (미리 보기)** 에서 기존 사례를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-115">Select an existing case from the **Security & Compliance Center > Advanced eDiscovery (Preview)**.</span></span>
   
   2. <span data-ttu-id="20048-116">**Custodians** 탭으로 이동를 더불어를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-116">Navigate to the **Custodians** tab and select a custodian.</span></span>
   
   3. <span data-ttu-id="20048-117">더불어를 선택한 후 세부 정보 패널에서 **더불어 활동 보기를** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-117">Once you have selected a custodian, click **View Custodian Activity** from the details panel.</span></span>
   
   4. <span data-ttu-id="20048-118">다음 검색 조건을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-118">Configure the following search criteria:</span></span>
      
      <span data-ttu-id="20048-p104">a. **활동** -를 검색할 수 있는 작업을 표시 하려면 드롭다운 목록을 클릭 합니다. 검색을 실행 하 고 나면 선택한 작업에 대 한 감사 레코드에만 표시 됩니다. **모든 작업에 대 한 결과 표시** 를 선택 하면 다른 검색 조건을 만족 하는 모든 작업에 대 한 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p104">a. **Activities** - Click the drop-down list to display the activities that you can search for. After you run the search, only the audit records for the selected activities are displayed. Selecting **Show results for all activities** will display results for all activities that meet the other search criteria.</span></span>
      
      <span data-ttu-id="20048-p105">**시작 날짜 및 종료 날짜** -b. 기간 내에 발생 한 이벤트를 표시 하려면 날짜 및 시간 범위를 선택 합니다. 지난 7 일간 기본적으로 선택 됩니다. 날짜 및 시간에서 utc (협정 세계시) 형식 나와 있습니다. 지정할 수 있는 최대 날짜 범위는 1 년입니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p105">b. **Start date and End date** - Select a date and time range to display the events that occurred within that period. The last seven days are selected by default. The date and time are presented in Coordinated Universal Time (UTC) format. The maximum date range that you can specify is one year.</span></span>
      
      <span data-ttu-id="20048-p106">c. **Custodians** -에서이 상자를 선택 합니다 검색을 표시 하는 특정 더불어 클릭에 대 한 결과입니다. 이 상자에서 선택한 사용자에 의해 수행 선택된 된 작업에 대 한 감사 레코드는 결과의 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p106">c. **Custodians** - Click in this box and then select a specific custodian to display search results for. Audit records for the selected activity performed by the users you select in this box are displayed in the list of results.</span></span>
    
    1. <span data-ttu-id="20048-p107">검색 조건을 사용 하 여 검색을 실행 하려면 **검색** 클릭 합니다. 검색 결과 로드 하 고 잠시 후에 표시 하는 결과 아래에서 더불어 활동 검색 페이지입니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p107">Click **Search** to run the search using your search criteria. The search results are loaded, and after a few moments they are displayed under Results on the Custodian Activities search page.</span></span> 

## <a name="step-2-view-the-audit-log-search-results"></a><span data-ttu-id="20048-133">2 단계: 감사 로그 검색 결과 보려면</span><span class="sxs-lookup"><span data-stu-id="20048-133">Step 2: View the audit log search results</span></span>

<span data-ttu-id="20048-p108">감사 로그 검색의 결과 관리자 감사 로그 페이지에서 결과 아래에서 표시 됩니다. 5, 000 (가장 최근) 이벤트의 최대 150 이벤트의 증가에 표시 됩니다. 더 많은 이벤트를 표시 하려면 결과 창에서 스크롤 막대를 사용할 수 또는 다음 150 이벤트를 표시 하려면 Shift + End 키를 눌러 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p108">The results of an audit log search are displayed under Results on the Custodian Audit log page. A maximum of 5,000 (newest) events are displayed in increments of 150 events. To display more events you can use the scroll bar in the Results pane or you can press Shift + End to display the next 150 events.</span></span>

<span data-ttu-id="20048-137">결과 검색에 의해 반환 된 각 이벤트에 대 한 다음 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-137">The results contain the following information about each event returned by the search.</span></span>
- <span data-ttu-id="20048-138">**날짜**: 날짜 및 시간 (UTC 형식) 이벤트가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-138">**Date**: The date and time (in UTC format) when the event occurred.</span></span>

- <span data-ttu-id="20048-p109">**IP 주소**: 활동을 기록 하는 경우에 사용 된 장치의 IP 주소입니다. IP 주소는 IPv4 또는 IPv6 주소 형식으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p109">**IP address**: The IP address of the device that was used when the activity was logged. The IP address is displayed in either an IPv4 or IPv6 address format.</span></span>

- <span data-ttu-id="20048-141">**사용자**: 사용자 (또는 서비스 계정) 이벤트를 트리거한 해당 작업을 수행한 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="20048-141">**User**: The user (or service account) who performed the action that triggered the event.</span></span>

- <span data-ttu-id="20048-p110">**작업**: 사용자에 의해 수행 되는 활동입니다. 이 값은 활동에 대 한 드롭다운 목록에서에서 선택한 작업에 해당 합니다. Exchange 관리자 감사 로그에서 이벤트,이 속성 값이이 열에은 Exchange cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p110">**Activity**: The activity performed by the user. This value corresponds to the activities that you selected in the Activities drop down list. For an event from the Exchange admin audit log, the value in this column is an Exchange cmdlet.</span></span>

- <span data-ttu-id="20048-p111">**항목**: 만들어지거나 해당 하는 활동의 결과 수정 하는 개체입니다. 예: 볼 수 없거나 수정 된 파일 또는 업데이트 된 사용자 계정입니다. 일부 활동이이 열에서 값을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p111">**Item**: The object that was created or modified as a result of the corresponding activity. For example, the file that was viewed or modified or the user account that was updated. Not all activities have a value in this column.</span></span>

- <span data-ttu-id="20048-p112">**세부 정보**: 활동에 대 한 추가 정보입니다. 다시, 일부 활동 값을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p112">**Detail**: Additional detail about an activity. Again, not all activities will have a value.</span></span>

## <a name="step-3-filter-the-search-results"></a><span data-ttu-id="20048-150">3 단계: 검색 결과 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-150">Step 3: Filter the search results</span></span>

<span data-ttu-id="20048-p113">정렬, 외에도 감사 로그 검색의 결과 필터링 할 수 있습니다. 이렇게 하면 신속 하 게 특정 사용자 또는 활동에 대 한 결과 필터링 하는데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p113">In addition to sorting, you can also filter the results of an audit log search. This can help you quickly filter the results for a specific user or activity.</span></span> 

<span data-ttu-id="20048-153">결과 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-153">To filter the results:</span></span>

 1. <span data-ttu-id="20048-154">페이지를 만들고 감사 로그 검색을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-154">Create and run an audit log search.</span></span>
  
2. <span data-ttu-id="20048-155">결과가 표시 되 면 **결과 필터링**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-155">When the results are displayed, click **Filter results**.</span></span>
 
3. <span data-ttu-id="20048-156">키워드 상자는 각 열 머리글 아래에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20048-156">Keyword boxes are displayed under each column header.</span></span>
  
4. <span data-ttu-id="20048-p114">열 머리글 아래 상자 중 하나를 클릭 하 고 단어 또는 구를 필터링 하는 열에 따라 입력 합니다. 필터와 일치 하는 이벤트를 표시 하는 결과 다시 조정할 동적으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p114">Click one of the boxes under a column header and type a word or phrase, depending on the column you're filtering on. The results will dynamically readjust to display the events that match your filter.</span></span>
  
5. <span data-ttu-id="20048-159">필터를 지우려면 필터 상자에 있는 **X** 를 클릭 하거나 **필터링 숨기기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-159">To clear a filter, click the **X** in the filter box or just click **Hide filtering**.</span></span>

## <a name="export-the-search-results-to-a-file"></a><span data-ttu-id="20048-160">검색 결과 파일로 내보내기</span><span class="sxs-lookup"><span data-stu-id="20048-160">Export the search results to a file</span></span>

<span data-ttu-id="20048-p115">감사 로그 검색의 결과 로컬 컴퓨터의 쉼표로 구분 된 값 (CSV) 파일로 내보낼 수 있습니다. Microsoft Excel에서이 파일을 열 있으며 여러 열으로 정렬, 필터링 및 (여러 값 셀이 포함)이 표시 된 단일 열 분할 검색 등의 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p115">You can export the results of an audit log search to a comma separated value (CSV) file on your local computer. You can open this file in Microsoft Excel and use features such as search, sorting, filtering, and splitting a single column (that contains multi-value cells) into multiple columns.</span></span>

1. <span data-ttu-id="20048-163">감사 로그 검색을 실행 하 고 원하는 결과 있을 때까지 다음 검색 조건을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-163">Run an audit log search, and then revise the search criteria until you have the desired results.</span></span>
  
2. <span data-ttu-id="20048-164">내보내기 결과 클릭 하 고 다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-164">Click Export results and select one of the following options:</span></span>

    - <span data-ttu-id="20048-p116">**저장 로드 결과:** **결과** 아래에서 **더불어 감사 로그 검색** 페이지에 표시 되는 항목만 내보내려면이 옵션을 선택 합니다. 다운로드 된 CSV 파일 (날짜, 사용자, 작업, 항목 및 세부 정보) 페이지에서 표시 된 동일한 열 (및 데이터)를 포함 합니다. 추가 열 ( **더 많은**참조)는 감사 로그 항목에서 더 많은 정보를 포함 하는 CSV 파일에 포함 됩니다. 로드 된 (및 볼 수 있는)는 동일한 결과 내보내려는 때문에 감사 로그 검색 페이지에서 최대 5, 000 항목의 최대 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p116">**Save loaded results:** Choose this option to export only the entries that are displayed under **Results** on the **Custodian Audit log search** page. The CSV file that is downloaded contains the same columns (and data) displayed on the page (Date, User, Activity, Item, and Details). An additional column (titled **More**) is included in the CSV file that contains more information from the audit log entry. Because you're exporting the same results that are loaded (and viewable) on the Audit log search page, a maximum of 5,000 entries are exported.</span></span>
        
    - <span data-ttu-id="20048-p117">**모든 결과 다운로드:** 검색 조건을 만족 하는 Office 365 감사 로그에서 모든 항목을 내보내려면이 옵션을 선택 합니다. 검색 결과 집합이 많은 대 한 **관리자 감사 로그** 검색 페이지에 표시 될 수 있는 최대 5, 000 결과 외에도 감사 로그에서 모든 항목을 다운로드 하려면이 옵션을 선택 합니다. 이 CSV 파일로 감사 로그에서의 원시 데이터를 다운로드 합니다 옵션과 AuditData 라는 열에서 감사 로그 항목에서 추가 정보를 포함 합니다. 파일을 다른 옵션을 선택 하는 경우 다운로드 하는 것 보다 훨씬 더 큰 수 있기 때문에이 내보내기 옵션을 선택 하는 경우 파일을 다운로드 하려면 시간이 오래 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p117">**Download all results:** Choose this option to export all entries from the Office 365 audit log that meet the search criteria. For a large set of search results, choose this option to download all entries from the audit log in addition to the 5,000 results that can be displayed on the **Custodian Audit log** search page. This option will download the raw data from the audit log to a CSV file, and contains additional information from the audit log entry in a column named AuditData. It may take longer to download the file if you choose this export option because the file may be much larger than the one that's downloaded if you choose the other option.</span></span>
    
      > [!IMPORTANT]
      > <span data-ttu-id="20048-p118">단일 감사 로그 검색에서 50, 000 항목의 최대 CSV 파일을 다운로드할 수 있습니다. 50, 000 항목은 CSV 파일을 다운로드 하는 경우 검색 조건을 충족 하는 50, 000 개 이상의 이벤트는 잠재적인 가정할 수 있습니다. 이 제한 보다 많은 내보내려는 날짜 범위를 사용 하 여 감사 로그 항목의 수를 줄일 수를 시도 합니다. 50, 000 개 이상의 항목을 내보내는 더 작은 날짜 범위를 사용 하 여 여러 검색을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-p118">You can download a maximum of 50,000 entries to a CSV file from a single audit log search. If 50,000 entries are downloaded to the CSV file, you can probably assume there are more than 50,000 events that met the search criteria. To export more than this limit, try using a date range to reduce the number of audit log entries. You might have to run multiple searches with smaller date ranges to export more than 50,000 entries.</span></span>
        

3. <span data-ttu-id="20048-177">내보내기 옵션을 선택 하면 CSV 파일을 열거나 다운로드 폴더에 저장, 특정 폴더에 저장 하 라는 메시지가 표시 되는 창 맨 아래에 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20048-177">After you select an export option, a message is displayed at the bottom of the window that prompts you to open the CSV file, save it to the Downloads folder, or save it to a specific folder</span></span>

<span data-ttu-id="20048-178">필터링 또는 감사 로그 검색 결과 내보내기 (영문) 보기에 대 한 자세한 내용은 [Office 365 보안 & 준수 센터에서에서 감사 로그 검색](../search-the-audit-log-in-security-and-compliance.md)을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="20048-178">For more information about viewing, filtering, or exporting audit log search results, see [Search the audit log in the Office 365 Security & Compliance Center](../search-the-audit-log-in-security-and-compliance.md).</span></span>