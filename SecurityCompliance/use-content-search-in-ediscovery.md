---
title: eDiscovery 워크플로에서 콘텐츠 검색 사용
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 55f31488-288a-473a-9b9e-831a11e3711a
description: 'PowerShell 스크립트를 사용 하 여 보안 & 준수 센터에서 만든 검색을 기반으로 Exchange Online의 원본 위치 eDiscovery 검색을 만듭니다. '
ms.openlocfilehash: d021836a735d5c5dd12124e16e348729d88e6022
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157980"
---
# <a name="use-content-search-in-your-ediscovery-workflow"></a><span data-ttu-id="0f914-103">eDiscovery 워크플로에서 콘텐츠 검색 사용</span><span class="sxs-lookup"><span data-stu-id="0f914-103">Use Content Search in your eDiscovery workflow</span></span>

<span data-ttu-id="0f914-104">Security & 준수 센터의 콘텐츠 검색 기능을 사용 하 여 조직의 모든 사서함을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-104">The Content Search feature in the Security & Compliance Center allows you to search all mailboxes in your organization.</span></span> <span data-ttu-id="0f914-105">Exchange Online의 원본 위치 eDiscovery (최대 1만 개의 사서함을 검색할 수 있음)와 달리 단일 검색의 대상 사서함 수에는 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-105">Unlike In-Place eDiscovery in Exchange Online (where you can search up to 10,000 mailboxes), there are no limits for the number of target mailboxes in a single search.</span></span> <span data-ttu-id="0f914-106">조직 전체 검색을 수행 해야 하는 시나리오의 경우 콘텐츠 검색을 사용 하 여 모든 사서함을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-106">For scenarios that require you to perform organization-wide searches, you can use Content Search to search all mailboxes.</span></span> <span data-ttu-id="0f914-107">그런 다음 원본 위치 eDiscovery의 워크플로 기능을 사용 하 여 사서함을 보류 상태로 설정 하 고 검색 결과를 내보내는 등의 기타 eDiscovery 관련 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-107">Then you can use the workflow features of In-Place eDiscovery to perform other eDiscovery-related tasks, such as placing mailboxes on hold and exporting search results.</span></span> <span data-ttu-id="0f914-108">예를 들어 법적 사례에 대응 하는 특정 custodians을 식별 하기 위해 모든 사서함을 검색 해야 한다고 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-108">For example, let's say you have to search all mailboxes to identify specific custodians that are responsive to a legal case.</span></span> <span data-ttu-id="0f914-109">보안 & 준수 센터에서 콘텐츠 검색을 사용 하 여 조직의 모든 사서함을 검색 하 여 사례에 대응 되는 사용자를 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-109">You can use Content Search in the Security & Compliance Center to search all mailboxes in your organization to identify those that are responsive to the case.</span></span> <span data-ttu-id="0f914-110">그런 다음 custodian 사서함 목록을 Exchange Online의 원본 위치 eDiscovery 검색에 대 한 소스 사서함으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-110">Then you can use that list of custodian mailboxes as the source mailboxes for an In-Place eDiscovery search in Exchange Online.</span></span> <span data-ttu-id="0f914-111">원본 위치 eDiscovery를 사용 하는 경우에도 해당 소스 사서함에 보류를 적용 하 고 검색 결과를 검색 사서함으로 복사 하 고 검색 결과를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-111">Using In-Place eDiscovery also allows you to put a hold on those source mailboxes, copy search results to a discovery mailbox, and export the search results.</span></span>
  
<span data-ttu-id="0f914-112">이 항목에는 Security & 준수 센터에서 만든 검색의 원본 사서함 및 검색 쿼리 목록을 사용 하 여 Exchange Online에서 현재 위치 eDiscovery 검색을 만들기 위해 실행할 수 있는 스크립트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-112">This topic includes a script that you can run to create an In-Place eDiscovery search in Exchange Online by using the list of source mailboxes and search query from a search created in the Security & Compliance Center.</span></span> <span data-ttu-id="0f914-113">프로세스에 대 한 개요는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-113">Here's an overview of the process:</span></span>
  
[<span data-ttu-id="0f914-114">1 단계: 조직의 모든 사서함을 검색 하는 콘텐츠 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="0f914-114">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>](#step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization)

[<span data-ttu-id="0f914-115">2 단계: 단일 원격 PowerShell 세션 \& 에서 보안 및 준수 센터 및 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="0f914-115">Step 2: Connect to the Security \& Compliance Center and Exchange Online in a single remote PowerShell session</span></span>](#step-2-connect-to-the-security--compliance-center-and-exchange-online-in-a-single-remote-powershell-session)
  
[<span data-ttu-id="0f914-116">3 단계: 스크립트를 실행 하 여 콘텐츠 검색에서 원본 위치 eDiscovery 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="0f914-116">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>](#step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search)

[<span data-ttu-id="0f914-117">4 단계: 원본 위치 eDiscovery 검색 시작</span><span class="sxs-lookup"><span data-stu-id="0f914-117">Step 4: Start the In-Place eDiscovery search</span></span>](#step-4-start-the-in-place-ediscovery-search)

## <a name="step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization"></a><span data-ttu-id="0f914-118">1 단계: 조직의 모든 사서함을 검색 하는 콘텐츠 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="0f914-118">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>

<span data-ttu-id="0f914-119">첫 번째 단계는 Security & 준수 센터 (또는 Security & 준수 센터 PowerShell)를 사용 하 여 조직의 모든 사서함을 검색 하는 콘텐츠 검색을 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-119">The first step is to use the Security & Compliance Center (or Security & Compliance Center PowerShell) to create a Content Search that searches all mailboxes in your organization.</span></span> <span data-ttu-id="0f914-120">단일 콘텐츠 검색의 사서함 수에는 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-120">There's no limit for the number of mailboxes for a single Content Search.</span></span> <span data-ttu-id="0f914-121">검색에서 조사와 관련 된 원본 사서함만 반환 되도록 적절 한 키워드 쿼리 (또는 중요 한 정보 유형에 대 한 쿼리)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-121">Specify an appropriate keyword query (or a query for sensitive information types) so that the search returns only those source mailboxes that are relevant to your investigation.</span></span> <span data-ttu-id="0f914-122">필요한 경우 검색 쿼리를 구체화 하 여 반환 되는 검색 결과 및 원본 사서함의 범위를 좁힙니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-122">If necessary, refine the search query to narrow the scope of search results and source mailboxes that are returned.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0f914-123">원본 콘텐츠 검색 결과 아무 결과도 반환 되지 않으면 3 단계에서 스크립트를 실행할 때 전체 위치 eDiscovery가 만들어지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-123">If the source Content Search doesn't return any results, an In-Place eDiscovery won't be created when you run the script in Step 3.</span></span> <span data-ttu-id="0f914-124">검색 쿼리를 수정한 다음 콘텐츠 검색을 다시 실행 하 여 검색 결과를 반환 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-124">You may have to revise the search query then rerun the Content Search to return search results.</span></span> 
  
### <a name="use-the-security--compliance-center-to-search-all-mailboxes"></a><span data-ttu-id="0f914-125">보안 & 준수 센터를 사용 하 여 모든 사서함 검색</span><span class="sxs-lookup"><span data-stu-id="0f914-125">Use the Security & Compliance Center to search all mailboxes</span></span>

1. <span data-ttu-id="0f914-126">[Security _AMP_ 준수 센터로 이동](go-to-the-securitycompliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-126">[Go to the Security & Compliance Center](go-to-the-securitycompliance-center.md).</span></span> 
    
2. <span data-ttu-id="0f914-127"> > *\*콘텐츠 검색*\*검색을 클릭 한 다음 *\*새 검색** ![추가 아이콘](media/O365-MDM-CreatePolicy-AddIcon.gif)을 클릭 합니다. \*\*\**</span><span class="sxs-lookup"><span data-stu-id="0f914-127">Click **Search** > **Content search**, and then click **New search** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
3. <span data-ttu-id="0f914-128">**새 검색** 페이지에서 콘텐츠 검색의 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-128">On the **New search** page, type a name for the Content Search.</span></span> 
    
4. <span data-ttu-id="0f914-129">어떤 **위치를 확인**하 시겠습니까?에서 **모든 사서함 검색**을 클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-129">Under **Where do you want us to look?**, click **Search all mailboxes**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="0f914-130">**무엇을 검색하시겠습니까?** 아래의 상자에 검색 쿼리를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-130">In the box under **What do you want us to look for?**, type a search query in the box.</span></span> <span data-ttu-id="0f914-131">키워드, 메시지 속성(보낸 날짜 및 받은 날짜) 또는 문서 속성(예: 파일 이름 또는 문서를 마지막으로 변경한 날짜)을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-131">You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed.</span></span> <span data-ttu-id="0f914-132">AND, OR, NOT 또는 NEAR과 같은 부울 연산자를 사용 하는 보다 복잡 한 쿼리를 사용 하거나 메시지에서 주민 등록 번호와 같은 중요 한 정보를 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-132">You can use a more complex queries that use a Boolean operator, such as AND, OR, NOT or NEAR, or you can also search for sensitive information (such as social security numbers) in messages.</span></span> <span data-ttu-id="0f914-133">검색 쿼리를 만드는 방법에 대 한 자세한 내용은 [Keyword queries For Content search](keyword-queries-and-search-conditions.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="0f914-133">For more information about creating search queries, see [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).</span></span>
    
6. <span data-ttu-id="0f914-134">**검색**을 클릭하여 검색 설정을 저장하고 검색을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-134">Click **Search** to save the search settings and start the search.</span></span> 
    
    <span data-ttu-id="0f914-135">잠시 후 세부 정보 창에 예상 되는 검색 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-135">After a while, an estimate of the search results displayed in the details pane.</span></span> <span data-ttu-id="0f914-136">예상 결과에는 검색 결과의 전체 크기 및 항목 수가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-136">The estimate includes the total size and number of items for the search results.</span></span> <span data-ttu-id="0f914-137">검색이 완료된 후에 검색 결과를 미리 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-137">After the search is completed, you can preview the search results.</span></span> <span data-ttu-id="0f914-138">필요한 경우 새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로 고침**![을 클릭 하 여 세부 정보 창에서 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-138">If necessary, click **Refresh**![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
7.  <span data-ttu-id="0f914-139">필요한 경우 검색 쿼리를 구체화 하 여 검색 결과의 범위를 좁히고 검색을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-139">If necessary, refine the search query to narrow the scope of search results and then restart the search.</span></span> 
    
### <a name="use-security--compliance-center-powershell-to-search-all-mailboxes"></a><span data-ttu-id="0f914-140">Security & 준수 센터 PowerShell을 사용 하 여 모든 사서함 검색</span><span class="sxs-lookup"><span data-stu-id="0f914-140">Use Security & Compliance Center PowerShell to search all mailboxes</span></span>

<span data-ttu-id="0f914-141">**ComplianceSearch** cmdlet을 사용 하 여 조직의 모든 사서함을 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-141">You can also use the **New-ComplianceSearch** cmdlet to search all mailboxes in your organization.</span></span> <span data-ttu-id="0f914-142">첫 번째 단계는 [Security _AMP_ 준수 센터 PowerShell에 연결](https://go.microsoft.com/fwlink/p/?LinkID=627084)하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-142">The first step is to [Connect to Security & Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span></span>
  
<span data-ttu-id="0f914-143">다음은 PowerShell을 사용 하 여 조직의 모든 사서함을 검색 하는 예입니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-143">Here's an example of using PowerShell to search all mailboxes in your organization.</span></span> <span data-ttu-id="0f914-144">검색 쿼리는 제목 줄에 "재무 보고서" 라는 구가 포함 되어 있고 2015 년 1 월 1 일부 터 2015 년 6 월 30 일 사이에 전송 된 모든 메시지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-144">The search query returns all messages sent between January 1, 2015 and June 30, 2015 and that contain the phrase "financial report" in the subject line.</span></span> <span data-ttu-id="0f914-145">첫 번째 명령은 검색을 만들고 두 번째 명령은 검색을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-145">The first command creates the search, and the second command runs the search.</span></span> 
  
```
New-ComplianceSearch -Name "Search All-Financial Report" -ExchangeLocation all -ContentMatchQuery 'sent>=01/01/2015 AND sent<=06/30/2015 AND subject:"financial report"'
```

```
Start-ComplianceSearch -Identity "Search All-Financial Report"
```

<span data-ttu-id="0f914-146">자세한 내용은 [ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="0f914-146">For more information, see [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span></span>
  
### <a name="verify-the-number-of-source-mailboxes-in-the-content-search"></a><span data-ttu-id="0f914-147">콘텐츠 검색에서 원본 사서함 수 확인</span><span class="sxs-lookup"><span data-stu-id="0f914-147">Verify the number of source mailboxes in the Content Search</span></span>

<span data-ttu-id="0f914-148">콘텐츠 검색에서 검색 결과를 포함 하는 최대 1000 원본 사서함을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-148">A Content Search returns a maximum of 1,000 source mailboxes that contain search results.</span></span> <span data-ttu-id="0f914-149">검색 쿼리와 일치 하는 콘텐츠가 포함 된 사서함이 1000 개 보다 많으면 검색 결과가 가장 높은 최상위 1000 사서함만 이전 단계에서 만든 콘텐츠 검색에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-149">If there are more than 1,000 mailboxes that contain content that matches the search query, only the top 1,000 mailboxes with the most search results are included in the Content Search that you created in the previous step.</span></span> <span data-ttu-id="0f914-150">따라서 1000 개 보다 많은 사서함에 검색 결과가 포함 되는 경우 이러한 사서함 중 일부는 3 단계에서 만든 새로운 원본 위치 eDiscovery 검색에 복사 된 소스 사서함 목록에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-150">So if more than 1,000 mailboxes contain search results, some of those mailboxes won't be included in the list of source mailboxes copied to the new In-Place eDiscovery search created in Step 3.</span></span> 
  
<span data-ttu-id="0f914-151">원본 사서함이 1000 개 보다 많은 콘텐츠 검색을 만들려면 다음 단계를 수행 하 여 1 단계에서 만든 콘텐츠 검색에서 반환한 원본 사서함 수 (검색 결과 포함)를 표시 하는 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-151">To help you create a Content Search with no more than 1,000 source mailboxes, follow these steps to run a script that displays the number of source mailboxes (that contain search results) returned by the Content Search you created in Step 1.</span></span> 
  
1. <span data-ttu-id="0f914-152">Filename 접미사. p s c 1을 사용 하 여 PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-152">Save the following text to a PowerShell script file by using a filename suffix of .ps1.</span></span> <span data-ttu-id="0f914-153">예를 들어 이름이 이라는 `SourceMailboxes.ps1`파일에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-153">For example, you could save it to a file named `SourceMailboxes.ps1`.</span></span>
    
  ```
  [CmdletBinding()]
  Param(
      [Parameter(Mandatory=$True,Position=1)]
      [string]$SearchName
  )
  $search = Get-ComplianceSearch $SearchName
  if ($search.Status -ne "Completed")
  {
                  "Please wait until the search finishes.";
                  break;
  }
  $results = $search.SuccessResults;
  if (($search.Items -le 0) -or ([string]::IsNullOrWhiteSpace($results)))
  {
                  "The Content Search " + $SearchName + " didn't return any useful results.";
                  break;
  }
  $mailboxes = @();
  $lines = $results -split '[\r\n]+';
  foreach ($line in $lines)
  {
      if ($line -match 'Location: (\S+),.+Item count: (\d+)' -and $matches[2] -gt 0)
      {
          $mailboxes += $matches[1];
      }
  }
  "Number of mailboxes that have search hits: " + $mailboxes.Count
  ```

2. <span data-ttu-id="0f914-154">Security & 준수 센터 PowerShell에서 이전 단계에서 만든 스크립트가 있는 폴더로 이동한 다음 스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="0f914-154">In Security & Compliance Center PowerShell, go to the folder where the script you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\SourceMailboxes.ps1
    ```

3. <span data-ttu-id="0f914-155">스크립트에서 메시지를 표시 하는 경우 1 단계에서 만든 콘텐츠 검색의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-155">When prompted by the script, type the name of the Content Search that you created in Step 1.</span></span>
    
    <span data-ttu-id="0f914-156">이 스크립트는 검색 결과를 포함 하는 원본 사서함의 수를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-156">The script displays the number of source mailboxes that contain search results.</span></span>
    
<span data-ttu-id="0f914-157">원본 사서함이 1000 개 보다 많은 경우에는 두 개 이상의 콘텐츠 검색을 만들어 보세요.</span><span class="sxs-lookup"><span data-stu-id="0f914-157">If there are more than 1,000 source mailboxes, try creating two (or more) Content Searches.</span></span> <span data-ttu-id="0f914-158">예를 들어 한 콘텐츠 검색에서 다른 콘텐츠 검색의 나머지 절반에 해당 조직의 사서함 절반을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-158">For example, search half of your organization's mailboxes in one Content Search and the other half in another Content Search.</span></span> <span data-ttu-id="0f914-159">검색 조건을 변경 하 여 검색 결과를 포함 하는 사서함 수를 줄일 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-159">You could also change the search criteria to reduce the number of mailboxes that contain search results.</span></span> <span data-ttu-id="0f914-160">예를 들어 날짜 범위를 포함 하거나 키워드 쿼리를 구체화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-160">For example, you could include a date range or refine the keyword query.</span></span>
  
## <a name="step-2-connect-to-the-security--compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a><span data-ttu-id="0f914-161">2 단계: 단일 원격 PowerShell 세션 \& 에서 보안 및 준수 센터 및 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="0f914-161">Step 2: Connect to the Security \& Compliance Center and Exchange Online in a single remote PowerShell session</span></span>

<span data-ttu-id="0f914-162">다음 단계에서는 Windows PowerShell을 보안 & 준수 센터와 Exchange Online 조직 모두에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-162">The next step is to connect Windows PowerShell to both the Security & Compliance Center and to your Exchange Online organization.</span></span> <span data-ttu-id="0f914-163">3 단계에서 실행 하는 스크립트에는 보안 & 준수 센터의 콘텐츠 검색 cmdlet과 Exchange Online의 원본 위치 eDiscovery cmdlet에 대 한 액세스 권한이 필요 하기 때문에이 작업이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-163">This is necessary because the script that you run in Step 3 requires access to the Content Search cmdlets in the Security & Compliance Center and the In-Place eDiscovery cmdlets in Exchange Online.</span></span>
  
1. <span data-ttu-id="0f914-164">파일 이름 접미사. p s e c 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-164">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1.</span></span> <span data-ttu-id="0f914-165">예를 들어 이름이 이라는 `ConnectEXO-CC.ps1`파일에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-165">For example, you could save it to a file named `ConnectEXO-CC.ps1`.</span></span>
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. <span data-ttu-id="0f914-166">로컬 컴퓨터에서 Windows PowerShell을 열고, 이전 단계에서 만든 스크립트가 있는 폴더로 이동한 다음 스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="0f914-166">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\ConnectEXO-CC.ps1
    ```

<span data-ttu-id="0f914-167">작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="0f914-167">How do you know if this worked?</span></span> <span data-ttu-id="0f914-168">스크립트를 실행 한 후 Security & 준수 센터 및 Exchange Online의 cmdlet은 로컬 PowerShell 세션으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-168">After you run the script, cmdlets from the Security & Compliance Center and Exchange Online are imported into your local PowerShell session.</span></span> <span data-ttu-id="0f914-169">오류가 발생하지 않으면 정상적으로 연결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-169">If you don't receive any errors, you connected successfully.</span></span> <span data-ttu-id="0f914-170">빠른 테스트는 & 및 Exchange Online cmdlet (예: **Install-UnifiedCompliancePrerequisite** )을 사용 하 여 보안을 준수 하는 것이 좋습니다. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0f914-170">A quick test is to run a Security & Compliance Center cmdlet—for example, **Install-UnifiedCompliancePrerequisite** —and an Exchange Online cmdlet, such as **Get-Mailbox**.</span></span> 
  
## <a name="step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search"></a><span data-ttu-id="0f914-171">3 단계: 스크립트를 실행 하 여 콘텐츠 검색에서 원본 위치 eDiscovery 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="0f914-171">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>

<span data-ttu-id="0f914-172">2 단계에서 이중 PowerShell 세션을 만든 후에는 기존 콘텐츠 검색을 원본 위치 eDiscovery 검색으로 변환 하는 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-172">After you create the dual PowerShell session in Step 2, the next step is to run a script that will convert an existing Content Search to an In-Place eDiscovery search.</span></span> <span data-ttu-id="0f914-173">스크립트가 수행 하는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-173">Here's what the script does:</span></span>
  
- <span data-ttu-id="0f914-174">변환할 콘텐츠 검색의 이름을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-174">Prompts you for the name of the Content Search to convert.</span></span>
    
- <span data-ttu-id="0f914-175">콘텐츠 검색의 실행이 완료 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-175">Verifies that the Content Search has completed running.</span></span> <span data-ttu-id="0f914-176">콘텐츠 검색에서 결과가 반환 되지 않는 경우 원본 위치 eDiscovery가 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-176">If the Content Search doesn't return any results, and In-Place eDiscovery won't be created.</span></span>
    
- <span data-ttu-id="0f914-177">검색 결과를 포함 하는 콘텐츠 검색의 원본 사서함 목록을 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-177">Saves a list of the source mailboxes from the Content Search that contain search results to a variable.</span></span>
    
- <span data-ttu-id="0f914-178">다음 속성을 사용 하 여 새로운 원본 위치 eDiscovery 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-178">Creates a new In-Place eDiscovery search, with the following properties.</span></span> <span data-ttu-id="0f914-179">새 검색이 시작 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-179">Note that the new search isn't started.</span></span> <span data-ttu-id="0f914-180">이 문서는 4 단계에서 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-180">You'll start it in step 4.</span></span>
    
  - <span data-ttu-id="0f914-181">**Name** -새 검색의 이름에 사용 되는 형식은 Content \<search\>_MBSearch1의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-181">**Name** - The name of the new search uses this format: \<Name of Content Search\>_MBSearch1.</span></span> <span data-ttu-id="0f914-182">스크립트를 다시 실행 하 여 동일한 원본 콘텐츠 검색을 사용 하는 경우에는 콘텐츠 검색 \<\>_MBSearch2 라는 이름이 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-182">If you run the script again and use the same source Content Search, the search will be named \<Name of Content Search\>_MBSearch2.</span></span>
    
  - <span data-ttu-id="0f914-183">**원본 사서함** -검색 결과를 포함 하는 콘텐츠 검색의 모든 사서함입니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-183">**Source mailboxes** - All mailboxes from the Content Search that contain search results.</span></span> 
    
  - <span data-ttu-id="0f914-184">**검색 쿼리** -새 검색에서는 콘텐츠 검색의 검색 쿼리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-184">**Search query** - The new search uses the search query from the Content Search.</span></span> <span data-ttu-id="0f914-185">콘텐츠 검색에 모든 콘텐츠가 포함 된 경우 (검색 쿼리가 비어 있는 경우) 새 검색에는 빈 검색 쿼리도 있으며 원본 사서함에 있는 모든 콘텐츠가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-185">If the Content Search includes all content (where the search query is blank) the new search will also have a blank search query and will include all content found in the source mailboxes.</span></span> 
    
  - <span data-ttu-id="0f914-186">**검색만 예측** -새 검색이 예측 전용 검색으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-186">**Estimate only search** - The new search is marked as an estimate-only search.</span></span> <span data-ttu-id="0f914-187">검색 결과를 시작한 후 발견 사서함에 복사 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-187">It won't copy search results to a discovery mailbox after you start it.</span></span> 
    
1. <span data-ttu-id="0f914-188">Ps1의 filename 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-188">Save the following text to a Windows PowerShell script file by using a filename suffix of ps1.</span></span> <span data-ttu-id="0f914-189">예를 들어 이름이 이라는 `CreateMBSearchFromComplianceSearch.ps1`파일에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-189">For example, you could save it to a file named `CreateMBSearchFromComplianceSearch.ps1`.</span></span>
    
  ```
  [CmdletBinding()]
  Param(
      [Parameter(Mandatory=$True,Position=1)]
      [string]$SearchName,
      [switch]$original,
      [switch]$restoreOriginal
  )
  $search = Get-ComplianceSearch $SearchName
  if ($search.Status -ne "Completed")
  {
    "Please wait until the search finishes";
    break;
  }
  $results = $search.SuccessResults;
  if (($search.Items -le 0) -or ([string]::IsNullOrWhiteSpace($results)))
  {
    "The Content Search " + $SearchName + " didn't return any useful results";
    "A mailbox search object wasn't created";
    break;
  }
  $mailboxes = @();
  $lines = $results -split '[\r\n]+';
  foreach ($line in $lines)
  {
      if ($line -match 'Location: (\S+),.+Item count: (\d+)' -and $matches[2] -gt 0)
      {
          $mailboxes += $matches[1];
      }
  }
  $msPrefix = $SearchName + "_MBSearch";
  $I = 1;
  $mbSearches = Get-MailboxSearch;
  while ($true)
  {
      $found = $false;
      $mbsName = "$msPrefix$I";
      foreach ($mbs in $mbSearches)
      {
          if ($mbs.Name -eq $mbsName)
          {
              $found = $true;
              break;
          }
      }
      if (!$found)
      {
          break;
      }
      $I++;
  }
  $query = $search.KeywordQuery;
  if ([string]::IsNullOrWhiteSpace($query))
  {
      $query = $search.ContentMatchQuery;
  }
  if ([string]::IsNullOrWhiteSpace($query))
  {
    New-MailboxSearch "$msPrefix$i" -SourceMailboxes $mailboxes -EstimateOnly;
  }
  else
  {
    New-MailboxSearch "$msPrefix$i" -SourceMailboxes $mailboxes -SearchQuery $query -EstimateOnly;
  }
  
  ```

2. <span data-ttu-id="0f914-190">2 단계에서 만든 Windows PowerShell 세션에서 이전 단계에서 만든 스크립트가 있는 폴더로 이동한 다음 스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="0f914-190">In the Windows PowerShell session that you created in Step 2, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\CreateMBSearchFromComplianceSearch.ps1
    ```

3. <span data-ttu-id="0f914-191">스크립트에서 메시지가 표시 되 면 원본 위치 eDiscovery 검색 (예: 1 단계에서 만든 검색)으로 변환할 콘텐츠 검색의 이름을 입력 한 다음 enter 키를 누릅니다. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0f914-191">When prompted by the script, type the name of the Content Search that you want to covert to an In-Place eDiscovery search (for example, the search that you created in Step 1), and then press **Enter**.</span></span>
    
    <span data-ttu-id="0f914-192">스크립트에 성공 하면 **NotStarted**상태를 사용 하 여 새로운 원본 위치 eDiscovery 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-192">If the script is successful, a new In-Place eDiscovery search is created with a status of **NotStarted**.</span></span> <span data-ttu-id="0f914-193">명령을 `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` 실행 하 여 새 검색의 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-193">Run the command  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` to display the properties of the new search.</span></span> 
  
## <a name="step-4-start-the-in-place-ediscovery-search"></a><span data-ttu-id="0f914-194">4 단계: 원본 위치 eDiscovery 검색 시작</span><span class="sxs-lookup"><span data-stu-id="0f914-194">Step 4: Start the In-Place eDiscovery search</span></span>

<span data-ttu-id="0f914-195">3 단계에서 실행 하는 스크립트는 새로운 원본 위치 eDiscovery 검색을 만들지만이를 시작 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-195">The script that you run in Step 3 creates a new In-Place eDiscovery search, but doesn't start it.</span></span> <span data-ttu-id="0f914-196">다음 단계에서는 예상 되는 검색 결과를 얻을 수 있도록 검색을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-196">The next step is to start the search so you can get an estimate of the search results.</span></span>
  
1. <span data-ttu-id="0f914-197">EAC (Exchange 관리 센터)에서 **준수 관리** \> 원본 **위치 eDiscovery &amp; 유지**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-197">In the Exchange admin center (EAC), go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="0f914-198">목록 보기에서 3 단계에서 만든 원본 위치 eDiscovery 검색을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-198">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="0f914-199">![검색 **** 검색 아이콘](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> \*\*\*\* 을 클릭 하 여 검색을 시작 하 고 검색에서 반환 된 항목의 전체 크기 및 개수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-199">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **Estimate search results** to start the search and return an estimate of the total size and number of items returned by the search.</span></span> 
    
    <span data-ttu-id="0f914-200">예측 내용이 세부 정보 창에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-200">The estimates are displayed in the details pane.</span></span> <span data-ttu-id="0f914-201">새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로 고침** ![을 클릭 하 여 세부 정보 창에 표시 된 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-201">Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information displayed in the details pane.</span></span> 
    
4. <span data-ttu-id="0f914-202">검색이 완료 된 후 결과를 미리 보려면 세부 정보 창에서 **검색 결과 미리 보기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-202">To preview the results after the search is completed, click **Preview search results** in the details pane.</span></span>
  
## <a name="next-steps-after-creating-and-running-the-in-place-ediscovery-search"></a><span data-ttu-id="0f914-203">원본 위치 eDiscovery 검색을 만들고 실행 한 후의 다음 단계</span><span class="sxs-lookup"><span data-stu-id="0f914-203">Next steps after creating and running the In-Place eDiscovery search</span></span>

<span data-ttu-id="0f914-204">3 단계에서 스크립트로 만든 원본 위치 eDiscovery 검색을 만들고 시작한 후 일반적인 원본 위치 eDiscovery 워크플로를 사용 하 여 검색 결과에 대해 서로 다른 eDiscovery 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-204">After you create and start the In-Place eDiscovery search that was created by the script in Step 3, you can use the normal In-Place eDiscovery workflow to perform different eDiscovery actions on the search results.</span></span>
  
### <a name="create-an-in-place-hold"></a><span data-ttu-id="0f914-205">원본 위치 유지 만들기</span><span class="sxs-lookup"><span data-stu-id="0f914-205">Create an In-Place Hold</span></span>

1. <span data-ttu-id="0f914-206">EAC에서 **규정 준수 관리** \> 원본 \*\* &amp; 위치 eDiscovery 유지\*\*로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-206">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="0f914-207">목록 보기에서 3 단계에서 만든 원본 위치 eDiscovery 검색을 선택 하 고 편집 아이콘](media/O365_MDM_CreatePolicy_EditIcon.gif) **편집** ![을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-207">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
3. <span data-ttu-id="0f914-208">원본 **위치 유지** 페이지에서 **선택한 사서함의 검색 쿼리와 일치 하는 콘텐츠를 보류에 저장** 확인란을 선택 하 고 다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-208">On the **In-Place Hold** page, select the **Place content matching the search query in selected mailboxes on hold** check box and then select one of the following options:</span></span> 
    
  - <span data-ttu-id="0f914-209">**무기한 유지** -검색에서 반환 되는 항목을 무한 보존 상태로 설정 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-209">**Hold indefinitely** - Choose this option to place items returned by the search on an indefinite hold.</span></span> <span data-ttu-id="0f914-210">보류 중인 항목은 검색에서 사서함을 제거하거나 검색을 제거할 때까지 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-210">Items on hold will be preserved until you remove the mailbox from the search or remove the search.</span></span> 
    
  - <span data-ttu-id="0f914-211">**받은 날짜를 기준으로 항목을 보관할 일 수 지정** -특정 기간에 대 한 항목을 포함 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-211">**Specify number of days to hold items relative to their received date** - Choose this option to hold items for a specific period.</span></span> <span data-ttu-id="0f914-212">기간은 사서함 항목이 수신되거나 만들어진 날짜부터 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-212">The duration is calculated from the date a mailbox item is received or created.</span></span> 
    
4. <span data-ttu-id="0f914-213">**저장** 을 클릭 하 여 원본 위치 유지를 만들고 검색을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-213">Click **Save** to create the In-Place Hold and restart the search.</span></span> 
    
[<span data-ttu-id="0f914-214">Return to top</span><span class="sxs-lookup"><span data-stu-id="0f914-214">Return to top</span></span>](use-content-search-in-ediscovery.md#top)
  
### <a name="copy-the-search-results"></a><span data-ttu-id="0f914-215">검색 결과 복사</span><span class="sxs-lookup"><span data-stu-id="0f914-215">Copy the search results</span></span>

1. <span data-ttu-id="0f914-216">EAC에서 **규정 준수 관리** \> 원본 \*\* &amp; 위치 eDiscovery 유지\*\*로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-216">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="0f914-217">목록 보기에서 3 단계에서 만든 원본 위치 eDiscovery 검색을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-217">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="0f914-218">검색 검색 아이콘](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif)을 클릭 한 다음 드롭다운 목록에서 **검색 결과 복사** 를 클릭 합니다. \*\*\*\* ![</span><span class="sxs-lookup"><span data-stu-id="0f914-218">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif), and then click **Copy search results** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="0f914-219">**검색 결과 복사**의 다음 옵션 중에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-219">In **Copy Search Results**, select from the following options:</span></span>
    
    - <span data-ttu-id="0f914-220">**검색 가능한 항목 포함** -검색할 수 없는 사서함 항목 (예: Exchange 검색에서 인덱싱할 수 없는 파일 형식이 첨부 된 메시지)을 포함 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-220">**Include unsearchable items** - Select this check box to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search).</span></span> 
    
    - <span data-ttu-id="0f914-221">중복 된 메시지를 제외 하려면 중복 제거를 **사용** 합니다 .를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-221">**Enable de-duplication** - Select this check box to exclude duplicate messages.</span></span> <span data-ttu-id="0f914-222">단일 메시지 인스턴스만 검색 사서함에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-222">Only a single instance of a message will be copied to the discovery mailbox.</span></span> 
    
    - <span data-ttu-id="0f914-223">**전체 로깅 사용** -검색 결과에 전체 로그를 포함 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-223">**Enable full logging** - Select this check box to include a full log in search results.</span></span> 
    
    - <span data-ttu-id="0f914-224">**복사가 완료 되 면 메일 보내기** -검색이 완료 될 때 전자 메일 알림을 받으려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-224">**Send me mail when the copy is completed** - Select this check box to get an email notification when the search is completed.</span></span> 
    
    - <span data-ttu-id="0f914-225">**결과를이 검색 사서함에 복사** - **찾아보기를** 클릭 하 여 검색 결과를 복사할 검색 사서함을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-225">**Copy results to this discovery mailbox** - Click **Browse** to select the discovery mailbox where you want the search results copied to.</span></span> 
    
5. <span data-ttu-id="0f914-226">**복사** 를 클릭 하 여 검색 결과를 지정 된 검색 사서함에 복사 하는 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-226">Click **Copy** to start the process to copy the search results to the specified discovery mailbox.</span></span> 
    
6. <span data-ttu-id="0f914-227">새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로 고침** ![을 클릭 하 여 세부 정보 창에 표시 된 복사 상태에 대 한 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-227">Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information about the copying status that is displayed in the details pane.</span></span> 
    
7. <span data-ttu-id="0f914-228">복사가 완료 되 면 **열기** 를 클릭 하 여 검색 결과를 볼 수 있는 검색 사서함을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-228">When copying is complete, click **Open** to open the discovery mailbox to view the search results.</span></span> 
  
### <a name="export-the-search-results"></a><span data-ttu-id="0f914-229">검색 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="0f914-229">Export the search results</span></span>

1. <span data-ttu-id="0f914-230">EAC에서 **규정 준수 관리** \> 원본 \*\* &amp; 위치 eDiscovery 유지\*\*로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-230">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="0f914-231">목록 보기에서 3 단계에서 만든 원본 위치 eDiscovery 검색을 선택 하 고 **PST 파일로 내보내기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-231">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Export to a PST file**.</span></span>
    
3. <span data-ttu-id="0f914-232">**eDiscovery PST 내보내기 도구** 창에서 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-232">In the **eDiscovery PST Export Tool** window, do the following:</span></span> 
    
    - <span data-ttu-id="0f914-233">**찾아보기**를 클릭하여 PST 파일을 다운로드하려는 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-233">Click **Browse** to specify the location where you want to download the PST file.</span></span> 
    
    - <span data-ttu-id="0f914-p128">**중복 제거 사용** 확인란을 클릭하여 중복 메시지를 제외합니다. 단일 메시지 인스턴스만 PST 파일에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-p128">Click the **Enable deduplication** checkbox to exclude duplicate messages. Only a single instance of a message will be included in the PST file.</span></span> 
    
    - <span data-ttu-id="0f914-p129">**검색할 수 없는 항목 포함** 확인란을 클릭하여 검색할 수 없는 사서함 항목(예: Exchange 검색에서 인덱싱할 수 없는 파일 형식이 첨부된 메시지)을 포함합니다. 그러면 검색할 수 없는 항목이 별도의 PST 파일로 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-p129">Click the **Include unsearchable items** checkbox to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search). Unsearchable items are exported to a separate PST file.</span></span> 
    
4. <span data-ttu-id="0f914-238">**시작**을 클릭하여 검색 결과를 PST 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-238">Click **Start** to export the search results to a PST file.</span></span> 
    
    <span data-ttu-id="0f914-239">내보내기 프로세스에 대한 상태 정보가 포함된 창이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f914-239">A window is displayed that contains status information about the export process.</span></span>
