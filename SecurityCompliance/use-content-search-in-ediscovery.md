---
title: eDiscovery 워크플로에서 콘텐츠 검색 사용
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 55f31488-288a-473a-9b9e-831a11e3711a
description: 'PowerShell 스크립트를 사용 하 여 Office 365 보안에서 만든 검색 결과에 따라 Exchange Online에서 원본 위치 eDiscovery 검색 만들기 &amp; 준수 센터입니다. '
ms.openlocfilehash: 42af94ce850736dede52e619c240bb9e0a6f7031
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038071"
---
# <a name="use-content-search-in-your-ediscovery-workflow"></a><span data-ttu-id="73d63-103">eDiscovery 워크플로에서 콘텐츠 검색 사용</span><span class="sxs-lookup"><span data-stu-id="73d63-103">Use Content Search in your eDiscovery workflow</span></span>

<span data-ttu-id="73d63-p101">Office 365 보안에서 콘텐츠 검색 기능 &amp; 준수 센터를 사용 하 여 조직의 모든 사서함을 검색할 수 있습니다. Exchange Online (검색할 수 있는 최대 10, 000 사서함)의 원본 위치 eDiscovery, 달리 단일 검색에서 대상 사서함 수에 대 한 제한이 있습니다. 조직 전체에 걸쳐 검색을 수행할 수 있습니다 필요로 하는 시나리오에 대 한 모든 사서함을 검색 하려면 콘텐츠 검색을 사용할 수 있습니다. 그런 다음에 배치할 사서함 유지 및 내보내기의 검색 결과 같은 다른 eDiscovery 관련 작업을 수행 하려면 원본 위치 eDiscovery의 워크플로 기능을 사용할 수 있습니다. 예, 법적 사례에 응답 하는 특정 custodians를 식별 하는 모든 사서함을 검색할 수 있는 가정해 보겠습니다. 콘텐츠 검색을 사용 하 여 보안에서 수 &amp; 준수 센터는 대/소문자에 응답 하는 것을 식별 하 여 조직의 모든 사서함을 검색할 수 있습니다. 그런 다음 Exchange Online에서 원본 위치 eDiscovery 검색에 대 한 원본 사서함으로 해당 목록이 더불어 사서함을 사용할 수 있습니다. 또한를 사용 하 여 원본 위치 eDiscovery을 사용 하면 해당 원본 사서함을 보류, 검색 결과 검색 사서함으로 복사 하 고 검색 결과 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p101">The Content Search feature in the Office 365 Security &amp; Compliance Center allows you to search all mailboxes in your organization. Unlike In-Place eDiscovery in Exchange Online (where you can search up to 10,000 mailboxes), there are no limits for the number of target mailboxes in a single search. For scenarios that require you to perform organization-wide searches, you can use Content Search to search all mailboxes. Then you can use the workflow features of In-Place eDiscovery to perform other eDiscovery-related tasks, such as placing mailboxes on hold and exporting search results. For example, let's say you have to search all mailboxes to identify specific custodians that are responsive to a legal case. You can use Content Search in the Security &amp; Compliance Center to search all mailboxes in your organization to identify those that are responsive to the case. Then you can use that list of custodian mailboxes as the source mailboxes for an In-Place eDiscovery search in Exchange Online. Using In-Place eDiscovery also allows you to put a hold on those source mailboxes, copy search results to a discovery mailbox, and export the search results.</span></span>
  
<span data-ttu-id="73d63-p102">이 항목에는 원본 사서함 및 보안에서 만든 검색에서 검색 쿼리 목록을 사용 하 여 Exchange Online에서 원본 위치 eDiscovery 검색을 만들기 위해 실행할 수 있는 스크립트 &amp; 준수 센터입니다. 프로세스에 대 한 개요는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p102">This topic includes a script that you can run to create an In-Place eDiscovery search in Exchange Online by using the list of source mailboxes and search query from a search created in the Security &amp; Compliance Center. Here's an overview of the process:</span></span>
  
[<span data-ttu-id="73d63-114">1단계: 조직의 모든 사서함을 검색하는 콘텐츠 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="73d63-114">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>](#step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization)

[<span data-ttu-id="73d63-115">2 단계: 보안 연결할 &amp; 준수 센터 및 단일 원격 PowerShell 세션에서 Exchange Online</span><span class="sxs-lookup"><span data-stu-id="73d63-115">Step 2: Connect to the Security &amp; Compliance Center and Exchange Online in a single remote PowerShell session</span></span>](#step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session)
  
[<span data-ttu-id="73d63-116">3단계: 스크립트를 실행하여 콘텐츠 검색에서 원본 위치 eDiscovery 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="73d63-116">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>](#step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search)

[<span data-ttu-id="73d63-117">4단계: 원본 위치 eDiscovery 검색 시작</span><span class="sxs-lookup"><span data-stu-id="73d63-117">Step 4: Start the In-Place eDiscovery search</span></span>](#step-4-start-the-in-place-ediscovery-search)

## <a name="step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization"></a><span data-ttu-id="73d63-118">1단계: 조직의 모든 사서함을 검색하는 콘텐츠 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="73d63-118">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>

<span data-ttu-id="73d63-p103">첫번째 단계는 보안을 사용 하는 &amp; 준수 센터 (또는 보안 및 규정 준수 센터 PowerShell) 조직에서 모든 사서함을 검색 하는 콘텐츠 검색을 만듭니다. 단일 콘텐츠 검색에 대 한 사서함 수에 대 한 제한이 없습니다. 검색에서 반환 하면 조사와 관련 된 원본 사서함만 있도록 적절 한 키워드 쿼리 (또는 중요 한 정보 형식에 대 한 쿼리)을 지정 합니다. 필요한 경우 검색 결과 반환 되는 원본 사서함의 범위를 좁히기 위해 검색 쿼리를 구체화 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p103">The first step is to use the Security &amp; Compliance Center (or Security & Compliance Center PowerShell) to create a Content Search that searches all mailboxes in your organization. There's no limit for the number of mailboxes for a single Content Search. Specify an appropriate keyword query (or a query for sensitive information types) so that the search returns only those source mailboxes that are relevant to your investigation. If necessary, refine the search query to narrow the scope of search results and source mailboxes that are returned.</span></span>
  
> [!NOTE]
> <span data-ttu-id="73d63-p104">원본 콘텐츠 검색으로 어떤 결과도 반환되지 않으면 3단계에서 스크립트를 실행할 때 원본 위치 eDiscovery가 만들어지지 않습니다. 검색 결과를 반환하려면 검색 쿼리를 수정한 후 콘텐츠 검색을 다시 실행해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p104">If the source Content Search doesn't return any results, an In-Place eDiscovery won't be created when you run the script in Step 3. You may have to revise the search query then rerun the Content Search to return search results.</span></span> 
  
### <a name="use-the-security-amp-compliance-center-to-search-all-mailboxes"></a><span data-ttu-id="73d63-125">보안을 사용 하 여 &amp; 모든 사서함을 검색 하려면 준수 센터</span><span class="sxs-lookup"><span data-stu-id="73d63-125">Use the Security &amp; Compliance Center to search all mailboxes</span></span>

1. <span data-ttu-id="73d63-126">[Office 365 보안으로 이동 &amp; 준수 센터](go-to-the-securitycompliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-126">[Go to the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md).</span></span> 
    
2. <span data-ttu-id="73d63-127">클릭 **검색 &amp; 조사** **콘텐츠 검색**을 클릭 하 고 **새로 만들기** 를 클릭 한 다음, ![추가 아이콘](media/O365-MDM-CreatePolicy-AddIcon.gif)합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-127">Click **Search &amp; investigation**, click **Content search**, and then click **New** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
3. <span data-ttu-id="73d63-128">**새 검색** 페이지에서 콘텐츠 검색의 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-128">On the **New search** page, type a name for the Content Search.</span></span> 
    
4. <span data-ttu-id="73d63-129">**어느 위치를 검색하시겠습니까?** 에서 **모든 사서함 검색**을 클릭하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-129">Under **Where do you want us to look?**, click **Search all mailboxes**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="73d63-p105">아래에 있는 상자에서 **수행할를 찾도록 우리?**, 상자에 검색 쿼리를 입력 합니다. 키워드, 메시지 전송 및 받은 날짜 또는 파일 이름 등의 문서 속성 또는 문서를 마지막으로 변경한 날짜와 같은 속성을 지정할 수 있습니다. 근거리, 또는 하지 AND, OR 등의 부울 연산자를 사용 하는 보다 복잡 한 쿼리를 사용할 수 또는 메시지에 중요 한 정보 (예: 주민등록 번호)을 검색할 수도 있습니다. 검색 쿼리 만들기 (영문) 하는 방법에 대 한 자세한 내용은 [콘텐츠 검색에 대 한 키워드 쿼리](keyword-queries-and-search-conditions.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="73d63-p105">In the box under **What do you want us to look for?**, type a search query in the box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as AND, OR, NOT or NEAR, or you can also search for sensitive information (such as social security numbers) in messages. For more information about creating search queries, see [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).</span></span>
    
6. <span data-ttu-id="73d63-134">**검색**을 클릭하여 검색 설정을 저장하고 검색을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-134">Click **Search** to save the search settings and start the search.</span></span> 
    
    <span data-ttu-id="73d63-p106">잠시 후 검색 결과 예상 세부 정보 창에 표시 합니다. 예상 전체 크기 및 검색 결과 대 한 항목 수를 포함합니다. 검색 완료 된 후에 검색 결과 미리볼 수 있습니다. 필요한 경우 **새로 고칠**을 클릭![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) 세부 정보 창에 대 한 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p106">After a while, an estimate of the search results displayed in the details pane. The estimate includes the total size and number of items for the search results. After the search is completed, you can preview the search results. If necessary, click **Refresh**![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
7.  <span data-ttu-id="73d63-139">필요한 경우 검색 쿼리를 구체화하여 검색 결과의 범위를 좁히고 검색을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-139">If necessary, refine the search query to narrow the scope of search results and then restart the search.</span></span> 
    
### <a name="use-security--compliance-center-powershell-to-search-all-mailboxes"></a><span data-ttu-id="73d63-140">보안 및 규정 준수 센터 PowerShell을 사용 하 여 모든 사서함을 검색 하려면</span><span class="sxs-lookup"><span data-stu-id="73d63-140">Use Security & Compliance Center PowerShell to search all mailboxes</span></span>

<span data-ttu-id="73d63-p107">또한 조직에서 모든 사서함을 검색할 수 **새로 ComplianceSearch** cmdlet을 사용할 수 있습니다. 첫번째 단계에서는 [Office 365 보안 연결 &amp; 준수 센터 PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084)합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p107">You can also use the **New-ComplianceSearch** cmdlet to search all mailboxes in your organization. The first step is to [Connect to Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span></span>
  
<span data-ttu-id="73d63-p108">다음은 조직에서 모든 사서함을 검색 하려면 PowerShell을 사용 하는 예제입니다. 검색 쿼리 2015 년 1 월 1, 및 2015 년 6 월 30, 간에 전송 되는 모든 메시지가 고 포함 된 구를 제목줄에 "재무 보고서"를 반환 합니다. 첫번째 명령에서 검색을 만들고 두번째 명령에서 검색을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p108">Here's an example of using PowerShell to search all mailboxes in your organization. The search query returns all messages sent between January 1, 2015 and June 30, 2015 and that contain the phrase "financial report" in the subject line. The first command creates the search, and the second command runs the search.</span></span> 
  
```
New-ComplianceSearch -Name "Search All-Financial Report" -ExchangeLocation all -ContentMatchQuery 'sent>=01/01/2015 AND sent<=06/30/2015 AND subject:"financial report"'
```

```
Start-ComplianceSearch -Identity "Search All-Financial Report"
```

<span data-ttu-id="73d63-146">자세한 내용은 [ComplianceSearch 새로 만들기를](https://go.microsoft.com/fwlink/p/?LinkId=517935)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="73d63-146">For more information, see [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span></span>
  
### <a name="verify-the-number-of-source-mailboxes-in-the-content-search"></a><span data-ttu-id="73d63-147">콘텐츠 검색에서 원본 사서함 수 확인</span><span class="sxs-lookup"><span data-stu-id="73d63-147">Verify the number of source mailboxes in the Content Search</span></span>

<span data-ttu-id="73d63-p109">콘텐츠 검색 최대 검색 결과 포함 하는 1, 000 원본 사서함을 반환 합니다. 1, 000 개 이상의 사서함 검색 쿼리와 일치 하는 콘텐츠를 포함 하는 경우 대부분의 검색 결과와 위에서 1, 000 개 사서함만 이전 단계에서 만든 콘텐츠 검색에 포함 됩니다. 따라서 1000 개 이상의 사서함 검색 결과 포함 하는 경우의 3 단계에서에서 만든 새 원본 위치 eDiscovery 검색에 복사 하는 원본 사서함 목록에서 해당 사서함의 일부를 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p109">A Content Search returns a maximum of 1,000 source mailboxes that contain search results. If there are more than 1,000 mailboxes that contain content that matches the search query, only the top 1,000 mailboxes with the most search results are included in the Content Search that you created in the previous step. So if more than 1,000 mailboxes contain search results, some of those mailboxes won't be included in the list of source mailboxes copied to the new In-Place eDiscovery search created in Step 3.</span></span> 
  
<span data-ttu-id="73d63-151">를 1, 000 원본 사서함 미만의 콘텐츠 검색을 만들 수 있도록 1 단계에서에서 만든 콘텐츠 검색에 의해 반환 됩니다 (포함 하는 검색 결과) 원본 사서함 수를 표시 하는 스크립트를 실행 하려면 다음이 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-151">To help you create a Content Search with no more than 1,000 source mailboxes, follow these steps to run a script that displays the number of source mailboxes (that contain search results) returned by the Content Search you created in Step 1.</span></span> 
  
1. <span data-ttu-id="73d63-p110">.Ps1 파일 이름 접미사를 사용 하 여 PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예 라는 파일을 저장할 수 `SourceMailboxes.ps1`합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p110">Save the following text to a PowerShell script file by using a filename suffix of .ps1. For example, you could save it to a file named `SourceMailboxes.ps1`.</span></span>
    
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

2. <span data-ttu-id="73d63-154">보안 및 규정 준수 센터 PowerShell에서 이전 단계에서 만든 스크립트 있는 폴더를 이동 하 고, 스크립트를 실행 하는 다음 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="73d63-154">In Security & Compliance Center PowerShell, go to the folder where the script you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\SourceMailboxes.ps1
    ```

3. <span data-ttu-id="73d63-155">스크립트가 1단계에서 만든 콘텐츠 검색의 이름을 입력하도록 요구하면 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-155">When prompted by the script, type the name of the Content Search that you created in Step 1.</span></span>
    
    <span data-ttu-id="73d63-156">스크립트는 검색 결과를 포함하는 원본 사서함의 수를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-156">The script displays the number of source mailboxes that contain search results.</span></span>
    
<span data-ttu-id="73d63-p111">1, 000 개 이상의 원본 사서함이 있는 경우 두 (또는 그 이상) 콘텐츠 검색을 만들어 보십시오. 하나의 콘텐츠 검색 및 다른 콘텐츠 검색의 나머지 절반에 조직의 사서함의 절반 검색 예입니다. 검색 결과 포함 하는 사서함의 수를 줄이는 검색 조건을 변경할 수도 있습니다. 예, 날짜 범위를 포함 하거나 키워드 쿼리를 구체화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p111">If there are more than 1,000 source mailboxes, try creating two (or more) Content Searches. For example, search half of your organization's mailboxes in one Content Search and the other half in another Content Search. You could also change the search criteria to reduce the number of mailboxes that contain search results. For example, you could include a date range or refine the keyword query.</span></span>
  
## <a name="step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a><span data-ttu-id="73d63-161">2 단계: 보안 연결할 &amp; 준수 센터 및 단일 원격 PowerShell 세션에서 Exchange Online</span><span class="sxs-lookup"><span data-stu-id="73d63-161">Step 2: Connect to the Security &amp; Compliance Center and Exchange Online in a single remote PowerShell session</span></span>

<span data-ttu-id="73d63-p112">다음 단계는 모두 보안을 Windows PowerShell에 연결 하는 &amp; 준수 센터 및 Exchange Online 조직에 있습니다. 이 작업을 3 단계에서에서 실행 하는 스크립트 보안에서 콘텐츠 검색 cmdlet에 대 한 액세스 해야 하기 때문에 &amp; 준수 센터 및 Exchange Online에서 원본 위치 eDiscovery cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p112">The next step is to connect Windows PowerShell to both the Security &amp; Compliance Center and to your Exchange Online organization. This is necessary because the script that you run in Step 3 requires access to the Content Search cmdlets in the Security &amp; Compliance Center and the In-Place eDiscovery cmdlets in Exchange Online.</span></span>
  
1. <span data-ttu-id="73d63-p113">.Ps1 파일 이름 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예 라는 파일을 저장할 수 `ConnectEXO-CC.ps1`합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p113">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1. For example, you could save it to a file named `ConnectEXO-CC.ps1`.</span></span>
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. <span data-ttu-id="73d63-166">로컬 컴퓨터에서 Windows PowerShell, 이전 단계에서 만든 스크립트 위치한 폴더로 이동한 다음 열고 실행 스크립트입니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="73d63-166">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\ConnectEXO-CC.ps1
    ```

<span data-ttu-id="73d63-p114">이 작동 하는 경우 어떻게 알 수 있습니까? Cmdlet은 보안에서 스크립트를 실행 하 고 나면 &amp; 준수 센터 및 Exchange Online 사용자의 로컬 PowerShell 세션으로 가져옵니다. 모든 오류가 하지 않으면 하는 경우 성공적으로 연결한 합니다. 빠른 테스트를 실행 하는 유가 증권를 &amp; 준수 센터 cmdlet- **설치 UnifiedCompliancePrerequisite** 예-및 **Get-mailbox**등의 Exchange Online cmdlet을 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p114">How do you know if this worked? After you run the script, cmdlets from the Security &amp; Compliance Center and Exchange Online are imported into your local PowerShell session. If you don't receive any errors, you connected successfully. A quick test is to run a Security &amp; Compliance Center cmdlet—for example, **Install-UnifiedCompliancePrerequisite** —and an Exchange Online cmdlet, such as **Get-Mailbox**.</span></span> 
  
## <a name="step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search"></a><span data-ttu-id="73d63-171">3단계: 스크립트를 실행하여 콘텐츠 검색에서 원본 위치 eDiscovery 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="73d63-171">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>

<span data-ttu-id="73d63-p115">2 단계에서에서 이중 PowerShell 세션을 만든 후 다음 단계에서 원본 위치 eDiscovery 검색에 기존 콘텐츠 검색을 변환 하는 스크립트를 실행 하는 것입니다. 스크립트에서 수행 하는 작업 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p115">After you create the dual PowerShell session in Step 2, the next step is to run a script that will convert an existing Content Search to an In-Place eDiscovery search. Here's what the script does:</span></span>
  
- <span data-ttu-id="73d63-174">변환할 콘텐츠 검색의 이름을 지정하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-174">Prompts you for the name of the Content Search to convert.</span></span>
    
- <span data-ttu-id="73d63-p116">콘텐츠 검색의 실행이 완료되었는지 확인합니다. 콘텐츠 검색에서 결과가 반환되지 않으면 원본 위치 eDiscovery가 만들어지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p116">Verifies that the Content Search has completed running. If the Content Search doesn't return any results, and In-Place eDiscovery won't be created.</span></span>
    
- <span data-ttu-id="73d63-177">검색 결과를 포함하는 콘텐츠 검색의 원본 사서함의 목록을 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-177">Saves a list of the source mailboxes from the Content Search that contain search results to a variable.</span></span>
    
- <span data-ttu-id="73d63-p117">다음 속성을 사용하여 새 원본 위치 eDiscovery 검색을 만듭니다. 새 검색은 시작되지 않습니다. 4단계에서 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p117">Creates a new In-Place eDiscovery search, with the following properties. Note that the new search isn't started. You'll start it in step 4.</span></span>
    
  - <span data-ttu-id="73d63-p118">**이름** -새 검색의 이름이을이 형식을 사용: \<콘텐츠 검색의 이름을\>_MBSearch1 합니다. 검색을 라는 스크립트를 다시 실행 하 고 동일한 원본 콘텐츠 검색을 사용 하는 경우 \<콘텐츠 검색의 이름을\>_MBSearch2 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p118">**Name** - The name of the new search uses this format: \<Name of Content Search\>_MBSearch1. If you run the script again and use the same source Content Search, the search will be named \<Name of Content Search\>_MBSearch2.</span></span>
    
  - <span data-ttu-id="73d63-183">**원본 사서함** -콘텐츠 검색에서 검색 결과 포함 하는 모든 사서함입니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-183">**Source mailboxes** - All mailboxes from the Content Search that contain search results.</span></span> 
    
  - <span data-ttu-id="73d63-p119">**검색 쿼리** -새 검색 콘텐츠 검색에서 검색 쿼리를 사용합니다. (여기서는 검색 쿼리는 빈) 하는 모든 콘텐츠를 포함 하는 콘텐츠 검색 새 검색 빈 검색 쿼리를 수도 있고 원본 사서함에 있는 모든 콘텐츠가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p119">**Search query** - The new search uses the search query from the Content Search. If the Content Search includes all content (where the search query is blank) the new search will also have a blank search query and will include all content found in the source mailboxes.</span></span> 
    
  - <span data-ttu-id="73d63-p120">**검색만 예측** -새 검색은 예측 전용 검색으로 표시 됩니다. 시작 된 후 검색 결과 검색 사서함으로 복사 되지 않습니다 것입니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p120">**Estimate only search** - The new search is marked as an estimate-only search. It won't copy search results to a discovery mailbox after you start it.</span></span> 
    
1. <span data-ttu-id="73d63-p121">Ps1 filename 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예 라는 파일을 저장할 수 `CreateMBSearchFromComplianceSearch.ps1`합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p121">Save the following text to a Windows PowerShell script file by using a filename suffix of ps1. For example, you could save it to a file named `CreateMBSearchFromComplianceSearch.ps1`.</span></span>
    
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

2. <span data-ttu-id="73d63-190">2 단계에서에서 만든 Windows PowerShell 세션에서는 이전 단계에서 만든 스크립트 위치한 폴더로 이동 하 고; 스크립트를 실행 하는 다음 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="73d63-190">In the Windows PowerShell session that you created in Step 2, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\CreateMBSearchFromComplianceSearch.ps1
    ```

3. <span data-ttu-id="73d63-191">스크립트에 의해 대화 상자가 나타나면 (예: 검색 1 단계에서에서 만든), 원본 위치 eDiscovery 검색을 프로젝트로 변환 하려는 콘텐츠 검색의 이름을 입력 하 고 **Enter**키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-191">When prompted by the script, type the name of the Content Search that you want to covert to an In-Place eDiscovery search (for example, the search that you created in Step 1), and then press **Enter**.</span></span>
    
    <span data-ttu-id="73d63-p122">이 스크립트는 성공, 경우에 새로운 원본 위치 eDiscovery 검색 **notstarted**상태로 만들어집니다. 명령을 실행 하 여 `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` 새 검색의 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p122">If the script is successful, a new In-Place eDiscovery search is created with a status of **NotStarted**. Run the command  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` to display the properties of the new search.</span></span> 
  
## <a name="step-4-start-the-in-place-ediscovery-search"></a><span data-ttu-id="73d63-194">4단계: 원본 위치 eDiscovery 검색 시작</span><span class="sxs-lookup"><span data-stu-id="73d63-194">Step 4: Start the In-Place eDiscovery search</span></span>

<span data-ttu-id="73d63-p123">3단계에서 실행하는 스크립트는 새 원본 위치 eDiscovery 검색을 만들지만 시작하지는 않습니다. 다음 단계는 예상 검색 결과를 가져올 수 있도록 검색을 시작하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p123">The script that you run in Step 3 creates a new In-Place eDiscovery search, but doesn't start it. The next step is to start the search so you can get an estimate of the search results.</span></span>
  
1. <span data-ttu-id="73d63-197">Exchange 관리 센터 (EAC)에서 **준수 관리** 로 이동 \> **원본 위치 eDiscovery &amp; 유지**합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-197">In the Exchange admin center (EAC), go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="73d63-198">목록 보기에서 3단계에서 만든 원본 위치 eDiscovery 검색을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-198">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="73d63-199">**검색** 을 클릭 ![검색 아이콘](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **예상 검색 결과** 의 예상 전체 크기 및 검색에 의해 반환 되는 항목의 수를 반환 하 고 검색을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-199">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **Estimate search results** to start the search and return an estimate of the total size and number of items returned by the search.</span></span> 
    
    <span data-ttu-id="73d63-p124">예측 세부 정보 창에 표시 됩니다. **새로 고칠** 을 클릭 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) 세부 정보 창에 표시 되는 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p124">The estimates are displayed in the details pane. Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information displayed in the details pane.</span></span> 
    
4. <span data-ttu-id="73d63-202">검색이 완료된 후 결과를 미리 보려면 세부 정보 창에서 **검색 결과 미리 보기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-202">To preview the results after the search is completed, click **Preview search results** in the details pane.</span></span>
  
## <a name="next-steps-after-creating-and-running-the-in-place-ediscovery-search"></a><span data-ttu-id="73d63-203">원본 위치 eDiscovery 검색을 만들고 실행한 후의 다음 단계</span><span class="sxs-lookup"><span data-stu-id="73d63-203">Next steps after creating and running the In-Place eDiscovery search</span></span>

<span data-ttu-id="73d63-204">3단계에서 스크립트에 의해 만들어진 원본 위치 eDiscovery 검색을 시작한 후에는 일반적인 원본 위치 eDiscovery 워크플로를 사용하여 검색 결과에 대해 다른 eDiscovery 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-204">After you create and start the In-Place eDiscovery search that was created by the script in Step 3, you can use the normal In-Place eDiscovery workflow to perform different eDiscovery actions on the search results.</span></span>
  
### <a name="create-an-in-place-hold"></a><span data-ttu-id="73d63-205">원본 위치 유지 만들기</span><span class="sxs-lookup"><span data-stu-id="73d63-205">Create an In-Place Hold</span></span>

1. <span data-ttu-id="73d63-206">EAC에서 **규정 준수 관리** 로 이동 \> **원본 위치 eDiscovery &amp; 유지**합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-206">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="73d63-207">목록 보기에서 3 단계에서에서 만든 원본 위치 eDiscovery 검색을 선택 하 고 **편집** 을 클릭 한 다음 ![편집 아이콘](media/O365_MDM_CreatePolicy_EditIcon.gif)합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-207">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
3. <span data-ttu-id="73d63-208">**원본 위치 유지** 페이지에서 **선택된 사서함에서 검색 쿼리에 일치하는 콘텐츠를 유지** 확인란을 선택하고 다음 옵션 중 하나를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-208">On the **In-Place Hold** page, select the **Place content matching the search query in selected mailboxes on hold** check box and then select one of the following options:</span></span> 
    
  - <span data-ttu-id="73d63-p125">**무기한 보존** -에 무기한 보존 설정 검색에 의해 반환 되는 항목을 배치 하려면이 옵션을 선택 합니다. 보류 중인 항목은 검색에서 사서함을 제거 하거나 검색을 제거할 때까지 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p125">**Hold indefinitely** - Choose this option to place items returned by the search on an indefinite hold. Items on hold will be preserved until you remove the mailbox from the search or remove the search.</span></span> 
    
  - <span data-ttu-id="73d63-p126">**자신의 받은 날짜를 기준으로 항목을 보관할 일 번호 지정** -특정 기간에 대 한 항목을 유지 하려면이 옵션을 선택 합니다. 사서함 항목을 받거나 만든 날짜에서 기간 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p126">**Specify number of days to hold items relative to their received date** - Choose this option to hold items for a specific period. The duration is calculated from the date a mailbox item is received or created.</span></span> 
    
4. <span data-ttu-id="73d63-213">**저장**을 클릭하여 원본 위치 유지를 만들고 검색을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-213">Click **Save** to create the In-Place Hold and restart the search.</span></span> 
    
[<span data-ttu-id="73d63-214">Return to top</span><span class="sxs-lookup"><span data-stu-id="73d63-214">Return to top</span></span>](use-content-search-in-ediscovery.md#top)
  
### <a name="copy-the-search-results"></a><span data-ttu-id="73d63-215">검색 결과 복사</span><span class="sxs-lookup"><span data-stu-id="73d63-215">Copy the search results</span></span>

1. <span data-ttu-id="73d63-216">EAC에서 **규정 준수 관리** 로 이동 \> **원본 위치 eDiscovery &amp; 유지**합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-216">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="73d63-217">목록 보기에서 3단계에서 만든 원본 위치 eDiscovery 검색을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-217">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="73d63-218">**검색** 을 클릭 ![검색 아이콘](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif), 한 다음 드롭다운 목록에서 **검색 결과 복사를** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-218">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif), and then click **Copy search results** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="73d63-219">**검색 결과 복사**의 다음 옵션 중에서 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-219">In **Copy Search Results**, select from the following options:</span></span>
    
    - <span data-ttu-id="73d63-220">**검색할 수 없는 항목 포함** -사서함 항목 (예: Exchange 검색을 통해 인덱싱할 수 없는 파일 형식 첨부 파일이 있는 메시지) 검색할 수 없으며을 포함 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-220">**Include unsearchable items** - Select this check box to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search).</span></span> 
    
    - <span data-ttu-id="73d63-p127">**중복을 사용 하도록 설정** -중복 된 메시지를 제외 하려면이 확인란을 선택 합니다. 메시지의 인스턴스를 단일 검색 사서함으로 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p127">**Enable de-duplication** - Select this check box to exclude duplicate messages. Only a single instance of a message will be copied to the discovery mailbox.</span></span> 
    
    - <span data-ttu-id="73d63-223">**전체 로깅을 사용 하도록 설정** -검색 결과에 전체 로그를 포함 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-223">**Enable full logging** - Select this check box to include a full log in search results.</span></span> 
    
    - <span data-ttu-id="73d63-224">**복사본 완료 되 면 메일을 보내** -검색이 완료 되 면 전자 메일 알림을 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-224">**Send me mail when the copy is completed** - Select this check box to get an email notification when the search is completed.</span></span> 
    
    - <span data-ttu-id="73d63-225">**이 검색 사서함에 결과 복사** -클릭에 복사 **찾아보기** 검색 결과 추가할 검색 사서함을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-225">**Copy results to this discovery mailbox** - Click **Browse** to select the discovery mailbox where you want the search results copied to.</span></span> 
    
5. <span data-ttu-id="73d63-226">**복사**를 클릭하여 검색 결과를 지정된 검색 사서함에 복사하는 프로세스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-226">Click **Copy** to start the process to copy the search results to the specified discovery mailbox.</span></span> 
    
6. <span data-ttu-id="73d63-227">**새로 고칠** 을 클릭 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) 세부 정보 창에 표시 되는 복사 상태에 대 한 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-227">Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information about the copying status that is displayed in the details pane.</span></span> 
    
7. <span data-ttu-id="73d63-228">복사가 완료되면 **열기**를 클릭하여 검색 사서함을 열고 검색 결과를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-228">When copying is complete, click **Open** to open the discovery mailbox to view the search results.</span></span> 
  
### <a name="export-the-search-results"></a><span data-ttu-id="73d63-229">검색 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="73d63-229">Export the search results</span></span>

1. <span data-ttu-id="73d63-230">EAC에서 **규정 준수 관리** 로 이동 \> **원본 위치 eDiscovery &amp; 유지**합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-230">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="73d63-231">목록 보기에서 3단계에서 만든 원본 위치 eDiscovery 검색을 선택하고 **PST 파일로 내보내기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-231">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Export to a PST file**.</span></span>
    
3. <span data-ttu-id="73d63-232">**eDiscovery PST 내보내기 도구** 창에서 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-232">In the **eDiscovery PST Export Tool** window, do the following:</span></span> 
    
    - <span data-ttu-id="73d63-233">**찾아보기**를 클릭하여 PST 파일을 다운로드하려는 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-233">Click **Browse** to specify the location where you want to download the PST file.</span></span> 
    
    - <span data-ttu-id="73d63-p128">**중복 제거 사용** 확인란을 클릭하여 중복 메시지를 제외합니다. 단일 메시지 인스턴스만 PST 파일에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p128">Click the **Enable deduplication** checkbox to exclude duplicate messages. Only a single instance of a message will be included in the PST file.</span></span> 
    
    - <span data-ttu-id="73d63-p129">**검색할 수 없는 항목 포함** 확인란을 클릭하여 검색할 수 없는 사서함 항목(예: Exchange 검색에서 인덱싱할 수 없는 파일 형식이 첨부된 메시지)을 포함합니다. 그러면 검색할 수 없는 항목이 별도의 PST 파일로 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-p129">Click the **Include unsearchable items** checkbox to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search). Unsearchable items are exported to a separate PST file.</span></span> 
    
4. <span data-ttu-id="73d63-238">**시작**을 클릭하여 검색 결과를 PST 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-238">Click **Start** to export the search results to a PST file.</span></span> 
    
    <span data-ttu-id="73d63-239">내보내기 프로세스에 대한 상태 정보가 포함된 창이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="73d63-239">A window is displayed that contains status information about the export process.</span></span>
