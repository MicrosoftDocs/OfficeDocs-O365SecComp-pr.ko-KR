---
title: eDiscovery 워크플로에서 콘텐츠 검색 사용
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 55f31488-288a-473a-9b9e-831a11e3711a
description: 'PowerShell 스크립트를 사용 하 여 Office 365 보안 &amp; 및 준수 센터에서 만든 검색을 기반으로 Exchange Online의 원본 위치 eDiscovery 검색을 만들 수 있습니다. '
ms.openlocfilehash: fff50b7dcd89790c84bb2911f560ce1b061b8f17
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216048"
---
# <a name="use-content-search-in-your-ediscovery-workflow"></a><span data-ttu-id="9bf21-103">eDiscovery 워크플로에서 콘텐츠 검색 사용</span><span class="sxs-lookup"><span data-stu-id="9bf21-103">Use Content Search in your eDiscovery workflow</span></span>

<span data-ttu-id="9bf21-p101">Office 365 보안 &amp; 및 준수 센터의 콘텐츠 검색 기능을 사용 하 여 조직의 모든 사서함을 검색할 수 있습니다. Exchange Online의 원본 위치 eDiscovery (최대 1만 개의 사서함을 검색할 수 있음)와 달리 단일 검색의 대상 사서함 수에는 제한이 없습니다. 조직 전체 검색을 수행 해야 하는 시나리오의 경우 콘텐츠 검색을 사용 하 여 모든 사서함을 검색할 수 있습니다. 그런 다음 원본 위치 eDiscovery의 워크플로 기능을 사용 하 여 사서함을 보류 상태로 설정 하 고 검색 결과를 내보내는 등의 기타 ediscovery 관련 작업을 수행할 수 있습니다. 예를 들어 법적 사례에 대응 하는 특정 custodians을 식별 하기 위해 모든 사서함을 검색 해야 한다고 가정해 보겠습니다. 보안 &amp; 및 준수 센터에서 콘텐츠 검색을 사용 하 여 조직의 모든 사서함을 검색 하 여 해당 사례에 대해 응답 하는 사용자를 식별할 수 있습니다. 그런 다음 custodian 사서함 목록을 Exchange Online의 원본 위치 eDiscovery 검색에 대 한 소스 사서함으로 사용할 수 있습니다. 원본 위치 eDiscovery를 사용 하는 경우에도 해당 소스 사서함에 보류를 적용 하 고 검색 결과를 검색 사서함으로 복사 하 고 검색 결과를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p101">The Content Search feature in the Office 365 Security &amp; Compliance Center allows you to search all mailboxes in your organization. Unlike In-Place eDiscovery in Exchange Online (where you can search up to 10,000 mailboxes), there are no limits for the number of target mailboxes in a single search. For scenarios that require you to perform organization-wide searches, you can use Content Search to search all mailboxes. Then you can use the workflow features of In-Place eDiscovery to perform other eDiscovery-related tasks, such as placing mailboxes on hold and exporting search results. For example, let's say you have to search all mailboxes to identify specific custodians that are responsive to a legal case. You can use Content Search in the Security &amp; Compliance Center to search all mailboxes in your organization to identify those that are responsive to the case. Then you can use that list of custodian mailboxes as the source mailboxes for an In-Place eDiscovery search in Exchange Online. Using In-Place eDiscovery also allows you to put a hold on those source mailboxes, copy search results to a discovery mailbox, and export the search results.</span></span>
  
<span data-ttu-id="9bf21-p102">이 항목에는 보안 &amp; 및 준수 센터에서 생성 된 검색의 원본 사서함 및 검색 쿼리 목록을 사용 하 여 Exchange Online에서 현재 위치 eDiscovery 검색을 만들기 위해 실행할 수 있는 스크립트를 포함 합니다. 프로세스에 대 한 개요는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p102">This topic includes a script that you can run to create an In-Place eDiscovery search in Exchange Online by using the list of source mailboxes and search query from a search created in the Security &amp; Compliance Center. Here's an overview of the process:</span></span>
  
[<span data-ttu-id="9bf21-114">1단계: 조직의 모든 사서함을 검색하는 콘텐츠 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="9bf21-114">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>](#step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization)

[<span data-ttu-id="9bf21-115">2 단계: 단일 원격 PowerShell 세션 &amp; 에서 보안 및 준수 센터 및 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="9bf21-115">Step 2: Connect to the Security &amp; Compliance Center and Exchange Online in a single remote PowerShell session</span></span>](#step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session)
  
[<span data-ttu-id="9bf21-116">3단계: 스크립트를 실행하여 콘텐츠 검색에서 원본 위치 eDiscovery 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="9bf21-116">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>](#step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search)

[<span data-ttu-id="9bf21-117">4단계: 원본 위치 eDiscovery 검색 시작</span><span class="sxs-lookup"><span data-stu-id="9bf21-117">Step 4: Start the In-Place eDiscovery search</span></span>](#step-4-start-the-in-place-ediscovery-search)

## <a name="step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization"></a><span data-ttu-id="9bf21-118">1단계: 조직의 모든 사서함을 검색하는 콘텐츠 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="9bf21-118">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>

<span data-ttu-id="9bf21-p103">첫 번째 단계는 보안 &amp; 및 준수 센터 (또는 security & 준수 센터 PowerShell)를 사용 하 여 조직의 모든 사서함을 검색 하는 콘텐츠 검색을 만드는 것입니다. 단일 콘텐츠 검색의 사서함 수에는 제한이 없습니다. 검색에서 조사와 관련 된 원본 사서함만 반환 되도록 적절 한 키워드 쿼리 (또는 중요 한 정보 유형에 대 한 쿼리)를 지정 합니다. 필요한 경우 검색 쿼리를 구체화 하 여 반환 되는 검색 결과 및 원본 사서함의 범위를 좁힙니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p103">The first step is to use the Security &amp; Compliance Center (or Security & Compliance Center PowerShell) to create a Content Search that searches all mailboxes in your organization. There's no limit for the number of mailboxes for a single Content Search. Specify an appropriate keyword query (or a query for sensitive information types) so that the search returns only those source mailboxes that are relevant to your investigation. If necessary, refine the search query to narrow the scope of search results and source mailboxes that are returned.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9bf21-p104">원본 콘텐츠 검색으로 어떤 결과도 반환되지 않으면 3단계에서 스크립트를 실행할 때 원본 위치 eDiscovery가 만들어지지 않습니다. 검색 결과를 반환하려면 검색 쿼리를 수정한 후 콘텐츠 검색을 다시 실행해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p104">If the source Content Search doesn't return any results, an In-Place eDiscovery won't be created when you run the script in Step 3. You may have to revise the search query then rerun the Content Search to return search results.</span></span> 
  
### <a name="use-the-security-amp-compliance-center-to-search-all-mailboxes"></a><span data-ttu-id="9bf21-125">보안 &amp; 및 준수 센터를 사용 하 여 모든 사서함 검색</span><span class="sxs-lookup"><span data-stu-id="9bf21-125">Use the Security &amp; Compliance Center to search all mailboxes</span></span>

1. <span data-ttu-id="9bf21-126">[Office 365 보안 &amp; 및 준수 센터로 이동](go-to-the-securitycompliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-126">[Go to the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md).</span></span> 
    
2. <span data-ttu-id="9bf21-127">\*\* &amp; 검색\*\*검사를 클릭 하 **고 콘텐츠 검색**을 클릭 한 다음 **새** ![추가](media/O365-MDM-CreatePolicy-AddIcon.gif)아이콘를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-127">Click **Search &amp; investigation**, click **Content search**, and then click **New** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
3. <span data-ttu-id="9bf21-128">**새 검색** 페이지에서 콘텐츠 검색의 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-128">On the **New search** page, type a name for the Content Search.</span></span> 
    
4. <span data-ttu-id="9bf21-129">**어느 위치를 검색하시겠습니까?** 에서 **모든 사서함 검색**을 클릭하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-129">Under **Where do you want us to look?**, click **Search all mailboxes**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="9bf21-p105">**무엇을 확인**하 시겠습니까? 상자에 검색 쿼리를 입력 합니다. 키워드, 메시지 속성 (예: 보낸 날짜 및 수신 일자) 또는 문서 속성 (예: 파일 이름) 또는 문서를 마지막으로 변경한 날짜 등을 지정할 수 있습니다. AND, OR, NOT 또는 NEAR과 같은 부울 연산자를 사용 하는 보다 복잡 한 쿼리를 사용 하거나 메시지에서 주민 등록 번호와 같은 중요 한 정보를 검색할 수도 있습니다. 검색 쿼리를 만드는 방법에 대 한 자세한 내용은 [Keyword queries for Content search](keyword-queries-and-search-conditions.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p105">In the box under **What do you want us to look for?**, type a search query in the box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as AND, OR, NOT or NEAR, or you can also search for sensitive information (such as social security numbers) in messages. For more information about creating search queries, see [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).</span></span>
    
6. <span data-ttu-id="9bf21-134">**검색**을 클릭하여 검색 설정을 저장하고 검색을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-134">Click **Search** to save the search settings and start the search.</span></span> 
    
    <span data-ttu-id="9bf21-p106">잠시 후 세부 정보 창에 예상 되는 검색 결과가 표시 됩니다. 예상에는 검색 결과에 대 한 총 항목 크기 및 수가 포함 됩니다. 검색이 완료 되 면 검색 결과를 미리 볼 수 있습니다. 필요한 경우 새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로 고침**![을 클릭 하 여 세부 정보 창에서 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p106">After a while, an estimate of the search results displayed in the details pane. The estimate includes the total size and number of items for the search results. After the search is completed, you can preview the search results. If necessary, click **Refresh**![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
7.  <span data-ttu-id="9bf21-139">필요한 경우 검색 쿼리를 구체화하여 검색 결과의 범위를 좁히고 검색을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-139">If necessary, refine the search query to narrow the scope of search results and then restart the search.</span></span> 
    
### <a name="use-security--compliance-center-powershell-to-search-all-mailboxes"></a><span data-ttu-id="9bf21-140">Security & 준수 센터 PowerShell을 사용 하 여 모든 사서함 검색</span><span class="sxs-lookup"><span data-stu-id="9bf21-140">Use Security & Compliance Center PowerShell to search all mailboxes</span></span>

<span data-ttu-id="9bf21-p107">**ComplianceSearch** cmdlet을 사용 하 여 조직의 모든 사서함을 검색할 수도 있습니다. 첫 번째 단계는 [Office 365 보안 &amp; 및 준수 센터 PowerShell에 연결](https://go.microsoft.com/fwlink/p/?LinkID=627084)하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p107">You can also use the **New-ComplianceSearch** cmdlet to search all mailboxes in your organization. The first step is to [Connect to Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span></span>
  
<span data-ttu-id="9bf21-p108">다음은 PowerShell을 사용 하 여 조직의 모든 사서함을 검색 하는 예입니다. 검색 쿼리는 제목 줄에 "재무 보고서" 라는 구가 포함 되어 있고 2015 년 1 월 1 일부 터 2015 년 6 월 30 일 사이에 전송 된 모든 메시지를 반환 합니다. 첫 번째 명령은 검색을 만들고 두 번째 명령은 검색을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p108">Here's an example of using PowerShell to search all mailboxes in your organization. The search query returns all messages sent between January 1, 2015 and June 30, 2015 and that contain the phrase "financial report" in the subject line. The first command creates the search, and the second command runs the search.</span></span> 
  
```
New-ComplianceSearch -Name "Search All-Financial Report" -ExchangeLocation all -ContentMatchQuery 'sent>=01/01/2015 AND sent<=06/30/2015 AND subject:"financial report"'
```

```
Start-ComplianceSearch -Identity "Search All-Financial Report"
```

<span data-ttu-id="9bf21-146">자세한 내용은 [ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9bf21-146">For more information, see [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span></span>
  
### <a name="verify-the-number-of-source-mailboxes-in-the-content-search"></a><span data-ttu-id="9bf21-147">콘텐츠 검색에서 원본 사서함 수 확인</span><span class="sxs-lookup"><span data-stu-id="9bf21-147">Verify the number of source mailboxes in the Content Search</span></span>

<span data-ttu-id="9bf21-p109">콘텐츠 검색에서 검색 결과를 포함 하는 최대 1000 원본 사서함을 반환 합니다. 검색 쿼리와 일치 하는 콘텐츠가 포함 된 사서함이 1000 개 보다 많으면 검색 결과가 가장 높은 최상위 1000 사서함만 이전 단계에서 만든 콘텐츠 검색에 포함 됩니다. 따라서 1000 개 보다 많은 사서함에 검색 결과가 포함 되는 경우 이러한 사서함 중 일부는 3 단계에서 만든 새로운 원본 위치 eDiscovery 검색에 복사 된 소스 사서함 목록에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p109">A Content Search returns a maximum of 1,000 source mailboxes that contain search results. If there are more than 1,000 mailboxes that contain content that matches the search query, only the top 1,000 mailboxes with the most search results are included in the Content Search that you created in the previous step. So if more than 1,000 mailboxes contain search results, some of those mailboxes won't be included in the list of source mailboxes copied to the new In-Place eDiscovery search created in Step 3.</span></span> 
  
<span data-ttu-id="9bf21-151">원본 사서함이 1000 개 보다 많은 콘텐츠 검색을 만들려면 다음 단계를 수행 하 여 1 단계에서 만든 콘텐츠 검색에서 반환한 원본 사서함 수 (검색 결과 포함)를 표시 하는 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-151">To help you create a Content Search with no more than 1,000 source mailboxes, follow these steps to run a script that displays the number of source mailboxes (that contain search results) returned by the Content Search you created in Step 1.</span></span> 
  
1. <span data-ttu-id="9bf21-p110">filename 접미사. p s c 1을 사용 하 여 PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예를 들어 이름이 이라는 `SourceMailboxes.ps1`파일에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p110">Save the following text to a PowerShell script file by using a filename suffix of .ps1. For example, you could save it to a file named `SourceMailboxes.ps1`.</span></span>
    
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

2. <span data-ttu-id="9bf21-154">Security & 준수 센터 PowerShell에서 이전 단계에서 만든 스크립트가 있는 폴더로 이동한 다음 스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="9bf21-154">In Security & Compliance Center PowerShell, go to the folder where the script you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\SourceMailboxes.ps1
    ```

3. <span data-ttu-id="9bf21-155">스크립트가 1단계에서 만든 콘텐츠 검색의 이름을 입력하도록 요구하면 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-155">When prompted by the script, type the name of the Content Search that you created in Step 1.</span></span>
    
    <span data-ttu-id="9bf21-156">스크립트는 검색 결과를 포함하는 원본 사서함의 수를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-156">The script displays the number of source mailboxes that contain search results.</span></span>
    
<span data-ttu-id="9bf21-p111">원본 사서함이 1000 개 보다 많은 경우에는 두 개 이상의 콘텐츠 검색을 만들어 보세요. 예를 들어 한 콘텐츠 검색에서 다른 콘텐츠 검색의 나머지 절반에 해당 조직의 사서함 절반을 검색 합니다. 검색 조건을 변경 하 여 검색 결과를 포함 하는 사서함 수를 줄일 수도 있습니다. 예를 들어 날짜 범위를 포함 하거나 키워드 쿼리를 구체화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p111">If there are more than 1,000 source mailboxes, try creating two (or more) Content Searches. For example, search half of your organization's mailboxes in one Content Search and the other half in another Content Search. You could also change the search criteria to reduce the number of mailboxes that contain search results. For example, you could include a date range or refine the keyword query.</span></span>
  
## <a name="step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a><span data-ttu-id="9bf21-161">2 단계: 단일 원격 PowerShell 세션 &amp; 에서 보안 및 준수 센터 및 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="9bf21-161">Step 2: Connect to the Security &amp; Compliance Center and Exchange Online in a single remote PowerShell session</span></span>

<span data-ttu-id="9bf21-p112">다음 단계는 Windows PowerShell을 보안 &amp; 및 준수 센터와 Exchange Online 조직에 연결 하는 것입니다. 3 단계에서 실행 하는 스크립트에는 보안 &amp; 및 준수 센터의 콘텐츠 검색 cmdlet 및 Exchange Online의 원본 위치 eDiscovery cmdlet에 대 한 액세스 권한이 필요 하기 때문에이 작업이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p112">The next step is to connect Windows PowerShell to both the Security &amp; Compliance Center and to your Exchange Online organization. This is necessary because the script that you run in Step 3 requires access to the Content Search cmdlets in the Security &amp; Compliance Center and the In-Place eDiscovery cmdlets in Exchange Online.</span></span>
  
1. <span data-ttu-id="9bf21-p113">파일 이름 접미사. p s e c 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예를 들어 이름이 이라는 `ConnectEXO-CC.ps1`파일에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p113">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1. For example, you could save it to a file named `ConnectEXO-CC.ps1`.</span></span>
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. <span data-ttu-id="9bf21-166">로컬 컴퓨터에서 Windows PowerShell을 열고, 이전 단계에서 만든 스크립트가 있는 폴더로 이동한 다음 스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="9bf21-166">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\ConnectEXO-CC.ps1
    ```

<span data-ttu-id="9bf21-p114">작동 여부는 어떻게 확인 하나요? 스크립트를 실행 한 후에는 보안 &amp; 및 준수 센터 및 Exchange Online의 cmdlet을 로컬 PowerShell 세션으로 가져옵니다. 오류가 표시 되지 않으면 제대로 연결 된 것입니다. 빠른 테스트는 &amp; **UnifiedCompliancePrerequisite** 와 같은 보안 및 **사서함**같은 Exchange Online cmdlet을 실행 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p114">How do you know if this worked? After you run the script, cmdlets from the Security &amp; Compliance Center and Exchange Online are imported into your local PowerShell session. If you don't receive any errors, you connected successfully. A quick test is to run a Security &amp; Compliance Center cmdlet—for example, **Install-UnifiedCompliancePrerequisite** —and an Exchange Online cmdlet, such as **Get-Mailbox**.</span></span> 
  
## <a name="step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search"></a><span data-ttu-id="9bf21-171">3단계: 스크립트를 실행하여 콘텐츠 검색에서 원본 위치 eDiscovery 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="9bf21-171">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>

<span data-ttu-id="9bf21-p115">2 단계에서 이중 PowerShell 세션을 만든 후에는 기존 콘텐츠 검색을 원본 위치 eDiscovery 검색으로 변환 하는 스크립트를 실행 합니다. 스크립트가 수행 하는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p115">After you create the dual PowerShell session in Step 2, the next step is to run a script that will convert an existing Content Search to an In-Place eDiscovery search. Here's what the script does:</span></span>
  
- <span data-ttu-id="9bf21-174">변환할 콘텐츠 검색의 이름을 지정하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-174">Prompts you for the name of the Content Search to convert.</span></span>
    
- <span data-ttu-id="9bf21-p116">콘텐츠 검색의 실행이 완료되었는지 확인합니다. 콘텐츠 검색에서 결과가 반환되지 않으면 원본 위치 eDiscovery가 만들어지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p116">Verifies that the Content Search has completed running. If the Content Search doesn't return any results, and In-Place eDiscovery won't be created.</span></span>
    
- <span data-ttu-id="9bf21-177">검색 결과를 포함하는 콘텐츠 검색의 원본 사서함의 목록을 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-177">Saves a list of the source mailboxes from the Content Search that contain search results to a variable.</span></span>
    
- <span data-ttu-id="9bf21-p117">다음 속성을 사용하여 새 원본 위치 eDiscovery 검색을 만듭니다. 새 검색은 시작되지 않습니다. 4단계에서 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p117">Creates a new In-Place eDiscovery search, with the following properties. Note that the new search isn't started. You'll start it in step 4.</span></span>
    
  - <span data-ttu-id="9bf21-p118">**Name** -새 검색의 이름에 사용 되는 형식은 Content \<search\>_MBSearch1의 이름입니다. 스크립트를 다시 실행 하 여 동일한 원본 콘텐츠 검색을 사용 하는 경우에는 콘텐츠 검색 \<\>_MBSearch2 라는 이름이 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p118">**Name** - The name of the new search uses this format: \<Name of Content Search\>_MBSearch1. If you run the script again and use the same source Content Search, the search will be named \<Name of Content Search\>_MBSearch2.</span></span>
    
  - <span data-ttu-id="9bf21-183">**원본 사서함** -검색 결과를 포함 하는 콘텐츠 검색의 모든 사서함입니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-183">**Source mailboxes** - All mailboxes from the Content Search that contain search results.</span></span> 
    
  - <span data-ttu-id="9bf21-p119">**검색 쿼리** -새 검색에서는 콘텐츠 검색의 검색 쿼리를 사용 합니다. 콘텐츠 검색에 모든 콘텐츠가 포함 된 경우 (검색 쿼리가 비어 있는 경우) 새 검색에는 빈 검색 쿼리도 있으며 원본 사서함에 있는 모든 콘텐츠가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p119">**Search query** - The new search uses the search query from the Content Search. If the Content Search includes all content (where the search query is blank) the new search will also have a blank search query and will include all content found in the source mailboxes.</span></span> 
    
  - <span data-ttu-id="9bf21-p120">**검색만 예측** -새 검색이 예측 전용 검색으로 표시 됩니다. 검색 결과를 시작한 후 발견 사서함에 복사 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p120">**Estimate only search** - The new search is marked as an estimate-only search. It won't copy search results to a discovery mailbox after you start it.</span></span> 
    
1. <span data-ttu-id="9bf21-p121">ps1의 filename 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예를 들어 이름이 이라는 `CreateMBSearchFromComplianceSearch.ps1`파일에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p121">Save the following text to a Windows PowerShell script file by using a filename suffix of ps1. For example, you could save it to a file named `CreateMBSearchFromComplianceSearch.ps1`.</span></span>
    
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

2. <span data-ttu-id="9bf21-190">2 단계에서 만든 Windows PowerShell 세션에서 이전 단계에서 만든 스크립트가 있는 폴더로 이동한 다음 스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="9bf21-190">In the Windows PowerShell session that you created in Step 2, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\CreateMBSearchFromComplianceSearch.ps1
    ```

3. <span data-ttu-id="9bf21-191">스크립트에서 메시지가 표시 되 면 원본 위치 eDiscovery 검색 (예: 1 단계에서 만든 검색)으로 변환할 콘텐츠 검색의 이름을 입력 한 다음 enter 키를 누릅니다. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9bf21-191">When prompted by the script, type the name of the Content Search that you want to covert to an In-Place eDiscovery search (for example, the search that you created in Step 1), and then press **Enter**.</span></span>
    
    <span data-ttu-id="9bf21-p122">스크립트에 성공 하면 **NotStarted**상태를 사용 하 여 새로운 원본 위치 eDiscovery 검색을 만듭니다. 명령을 `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` 실행 하 여 새 검색의 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p122">If the script is successful, a new In-Place eDiscovery search is created with a status of **NotStarted**. Run the command  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` to display the properties of the new search.</span></span> 
  
## <a name="step-4-start-the-in-place-ediscovery-search"></a><span data-ttu-id="9bf21-194">4단계: 원본 위치 eDiscovery 검색 시작</span><span class="sxs-lookup"><span data-stu-id="9bf21-194">Step 4: Start the In-Place eDiscovery search</span></span>

<span data-ttu-id="9bf21-p123">3단계에서 실행하는 스크립트는 새 원본 위치 eDiscovery 검색을 만들지만 시작하지는 않습니다. 다음 단계는 예상 검색 결과를 가져올 수 있도록 검색을 시작하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p123">The script that you run in Step 3 creates a new In-Place eDiscovery search, but doesn't start it. The next step is to start the search so you can get an estimate of the search results.</span></span>
  
1. <span data-ttu-id="9bf21-197">EAC (Exchange 관리 센터)에서 **준수 관리** \> 원본 **위치 eDiscovery &amp; 유지**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-197">In the Exchange admin center (EAC), go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="9bf21-198">목록 보기에서 3단계에서 만든 원본 위치 eDiscovery 검색을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-198">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="9bf21-199">![검색 **** 검색 아이콘](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> \*\*\*\* 을 클릭 하 여 검색을 시작 하 고 검색에서 반환 된 항목의 전체 크기 및 개수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-199">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **Estimate search results** to start the search and return an estimate of the total size and number of items returned by the search.</span></span> 
    
    <span data-ttu-id="9bf21-p124">예측 내용이 세부 정보 창에 표시 됩니다. 새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로 고침** ![을 클릭 하 여 세부 정보 창에 표시 된 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p124">The estimates are displayed in the details pane. Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information displayed in the details pane.</span></span> 
    
4. <span data-ttu-id="9bf21-202">검색이 완료된 후 결과를 미리 보려면 세부 정보 창에서 **검색 결과 미리 보기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-202">To preview the results after the search is completed, click **Preview search results** in the details pane.</span></span>
  
## <a name="next-steps-after-creating-and-running-the-in-place-ediscovery-search"></a><span data-ttu-id="9bf21-203">원본 위치 eDiscovery 검색을 만들고 실행한 후의 다음 단계</span><span class="sxs-lookup"><span data-stu-id="9bf21-203">Next steps after creating and running the In-Place eDiscovery search</span></span>

<span data-ttu-id="9bf21-204">3단계에서 스크립트에 의해 만들어진 원본 위치 eDiscovery 검색을 시작한 후에는 일반적인 원본 위치 eDiscovery 워크플로를 사용하여 검색 결과에 대해 다른 eDiscovery 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-204">After you create and start the In-Place eDiscovery search that was created by the script in Step 3, you can use the normal In-Place eDiscovery workflow to perform different eDiscovery actions on the search results.</span></span>
  
### <a name="create-an-in-place-hold"></a><span data-ttu-id="9bf21-205">원본 위치 유지 만들기</span><span class="sxs-lookup"><span data-stu-id="9bf21-205">Create an In-Place Hold</span></span>

1. <span data-ttu-id="9bf21-206">EAC에서 **규정 준수 관리** \> 원본 \*\* &amp; 위치 eDiscovery 유지\*\*로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-206">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="9bf21-207">목록 보기에서 3 단계에서 만든 원본 위치 eDiscovery 검색을 선택 하 고 편집 아이콘](media/O365_MDM_CreatePolicy_EditIcon.gif) **편집** ![을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-207">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
3. <span data-ttu-id="9bf21-208">**원본 위치 유지** 페이지에서 **선택된 사서함에서 검색 쿼리에 일치하는 콘텐츠를 유지** 확인란을 선택하고 다음 옵션 중 하나를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-208">On the **In-Place Hold** page, select the **Place content matching the search query in selected mailboxes on hold** check box and then select one of the following options:</span></span> 
    
  - <span data-ttu-id="9bf21-p125">**무기한 유지** -검색에서 반환 되는 항목을 무한 보존 상태로 설정 하려면이 옵션을 선택 합니다. 보류 중인 항목은 검색에서 사서함을 제거 하거나 검색을 제거할 때까지 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p125">**Hold indefinitely** - Choose this option to place items returned by the search on an indefinite hold. Items on hold will be preserved until you remove the mailbox from the search or remove the search.</span></span> 
    
  - <span data-ttu-id="9bf21-p126">**받은 날짜를 기준으로 항목을 보관할 일 수 지정** -특정 기간에 대 한 항목을 포함 하려면이 옵션을 선택 합니다. 기간은 사서함 항목을 받거나 만든 날짜 로부터 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p126">**Specify number of days to hold items relative to their received date** - Choose this option to hold items for a specific period. The duration is calculated from the date a mailbox item is received or created.</span></span> 
    
4. <span data-ttu-id="9bf21-213">**저장**을 클릭하여 원본 위치 유지를 만들고 검색을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-213">Click **Save** to create the In-Place Hold and restart the search.</span></span> 
    
[<span data-ttu-id="9bf21-214">Return to top</span><span class="sxs-lookup"><span data-stu-id="9bf21-214">Return to top</span></span>](use-content-search-in-ediscovery.md#top)
  
### <a name="copy-the-search-results"></a><span data-ttu-id="9bf21-215">검색 결과 복사</span><span class="sxs-lookup"><span data-stu-id="9bf21-215">Copy the search results</span></span>

1. <span data-ttu-id="9bf21-216">EAC에서 **규정 준수 관리** \> 원본 \*\* &amp; 위치 eDiscovery 유지\*\*로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-216">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="9bf21-217">목록 보기에서 3단계에서 만든 원본 위치 eDiscovery 검색을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-217">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="9bf21-218">검색 검색 아이콘](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif)을 클릭 한 다음 드롭다운 목록에서 **검색 결과 복사** 를 클릭 합니다. \*\*\*\* ![</span><span class="sxs-lookup"><span data-stu-id="9bf21-218">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif), and then click **Copy search results** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="9bf21-219">**검색 결과 복사**의 다음 옵션 중에서 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-219">In **Copy Search Results**, select from the following options:</span></span>
    
    - <span data-ttu-id="9bf21-220">**검색 가능한 항목 포함** -검색할 수 없는 사서함 항목 (예: Exchange 검색에서 인덱싱할 수 없는 파일 형식이 첨부 된 메시지)을 포함 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-220">**Include unsearchable items** - Select this check box to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search).</span></span> 
    
    - <span data-ttu-id="9bf21-p127">중복 된 메시지를 제외 하려면 중복 제거를 **사용** 합니다 .를 선택 합니다. 단일 메시지 인스턴스만 검색 사서함에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p127">**Enable de-duplication** - Select this check box to exclude duplicate messages. Only a single instance of a message will be copied to the discovery mailbox.</span></span> 
    
    - <span data-ttu-id="9bf21-223">**전체 로깅 사용** -검색 결과에 전체 로그를 포함 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-223">**Enable full logging** - Select this check box to include a full log in search results.</span></span> 
    
    - <span data-ttu-id="9bf21-224">**복사가 완료 되 면 메일 보내기** -검색이 완료 될 때 전자 메일 알림을 받으려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-224">**Send me mail when the copy is completed** - Select this check box to get an email notification when the search is completed.</span></span> 
    
    - <span data-ttu-id="9bf21-225">**결과를이 검색 사서함에 복사** - **찾아보기를** 클릭 하 여 검색 결과를 복사할 검색 사서함을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-225">**Copy results to this discovery mailbox** - Click **Browse** to select the discovery mailbox where you want the search results copied to.</span></span> 
    
5. <span data-ttu-id="9bf21-226">**복사**를 클릭하여 검색 결과를 지정된 검색 사서함에 복사하는 프로세스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-226">Click **Copy** to start the process to copy the search results to the specified discovery mailbox.</span></span> 
    
6. <span data-ttu-id="9bf21-227">새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로 고침** ![을 클릭 하 여 세부 정보 창에 표시 된 복사 상태에 대 한 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-227">Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information about the copying status that is displayed in the details pane.</span></span> 
    
7. <span data-ttu-id="9bf21-228">복사가 완료되면 **열기**를 클릭하여 검색 사서함을 열고 검색 결과를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-228">When copying is complete, click **Open** to open the discovery mailbox to view the search results.</span></span> 
  
### <a name="export-the-search-results"></a><span data-ttu-id="9bf21-229">검색 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="9bf21-229">Export the search results</span></span>

1. <span data-ttu-id="9bf21-230">EAC에서 **규정 준수 관리** \> 원본 \*\* &amp; 위치 eDiscovery 유지\*\*로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-230">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="9bf21-231">목록 보기에서 3단계에서 만든 원본 위치 eDiscovery 검색을 선택하고 **PST 파일로 내보내기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-231">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Export to a PST file**.</span></span>
    
3. <span data-ttu-id="9bf21-232">**eDiscovery PST 내보내기 도구** 창에서 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-232">In the **eDiscovery PST Export Tool** window, do the following:</span></span> 
    
    - <span data-ttu-id="9bf21-233">**찾아보기**를 클릭하여 PST 파일을 다운로드하려는 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-233">Click **Browse** to specify the location where you want to download the PST file.</span></span> 
    
    - <span data-ttu-id="9bf21-p128">**중복 제거 사용** 확인란을 클릭하여 중복 메시지를 제외합니다. 단일 메시지 인스턴스만 PST 파일에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p128">Click the **Enable deduplication** checkbox to exclude duplicate messages. Only a single instance of a message will be included in the PST file.</span></span> 
    
    - <span data-ttu-id="9bf21-p129">**검색할 수 없는 항목 포함** 확인란을 클릭하여 검색할 수 없는 사서함 항목(예: Exchange 검색에서 인덱싱할 수 없는 파일 형식이 첨부된 메시지)을 포함합니다. 그러면 검색할 수 없는 항목이 별도의 PST 파일로 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-p129">Click the **Include unsearchable items** checkbox to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search). Unsearchable items are exported to a separate PST file.</span></span> 
    
4. <span data-ttu-id="9bf21-238">**시작**을 클릭하여 검색 결과를 PST 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-238">Click **Start** to export the search results to a PST file.</span></span> 
    
    <span data-ttu-id="9bf21-239">내보내기 프로세스에 대한 상태 정보가 포함된 창이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bf21-239">A window is displayed that contains status information about the export process.</span></span>
