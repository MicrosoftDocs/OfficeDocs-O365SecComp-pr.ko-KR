---
title: Office 365 보안에서 콘텐츠 검색을 복제 &amp; 준수 센터
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/26/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 7b40eeaa-544c-4534-b89b-9f79998e374c
description: 이 문서에서 Windows PowerShell 스크립트를 사용 하 여 신속 하 게 보안에서 기존 콘텐츠 검색을 복제 &amp; Compliane 센터 검색 합니다. 복제할 때 검색, 원래 검색 같은 속성을 포함 하는 새로운 검색 (새 이름) 만들어집니다. 그런 다음 (키워드 쿼리 또는 날짜 범위)을 변경 하 여 새 검색을 편집 하 고 스크립트를 실행 수 있습니다.
ms.openlocfilehash: a4f801e3de281e8caf8aeb7d1c2bd48f0facb77c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533370"
---
# <a name="clone-a-content-search-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="88c99-105">Office 365 보안에서 콘텐츠 검색을 복제 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="88c99-105">Clone a Content Search in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="88c99-p102">Office 365 보안에서 콘텐츠 검색을 만드는 &amp; 사서함 또는 SharePoint 많은 검색 하는 준수 센터와 비즈니스 사이트에 대 한 OneDrive 잠시 걸릴 수 있습니다. 검색 사이트 지정 될 수도 있습니다 오류가 발생할 가능성이 URL를 잘못 입력 하는 경우. 이러한 문제를 방지 하려면를 신속 하 게 기존 콘텐츠 검색을 복제 하려면이 문서에서 Windows PowerShell 스크립트를 사용할 수 있습니다. 복제할 때 검색, 원래 검색 동일한 속성 (예: 콘텐츠 위치 및 검색 쿼리)을 포함 하는 새로운 검색 (다른 이름) 만들어집니다. 그런 다음 (키워드 쿼리 또는 날짜 범위를 변경) 하 여 새 검색을 편집 하 고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-p102">Creating a Content Search in Office 365 Security &amp; Compliance Center that searches a lot of mailboxes or SharePoint and OneDrive for Business sites can take awhile. Specifying the sites to search can also be prone to errors if you mistype a URL. To avoid these issues, you can use the Windows PowerShell script in this article to quickly clone an existing Content Search. When a you clone a search, a new search (with a different name) is created that contains the same properties (such as the content locations and the search query) as the original search. Then you can edit the new search (by changing the keyword query or the date range) and run it.</span></span>
  
<span data-ttu-id="88c99-111">콘텐츠 검색을 복제 하는 이유</span><span class="sxs-lookup"><span data-stu-id="88c99-111">Why clone Content Searches?</span></span>
  
- <span data-ttu-id="88c99-112">다른 키워드의 결과 비교 하려면 검색 쿼리 동일한 콘텐츠 위치에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-112">To compare the results of different keyword search queries run on the same content locations.</span></span>
    
- <span data-ttu-id="88c99-113">새 검색을 만들 때 많은 콘텐츠 위치를 다시 입력 하지 않아도 수를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-113">To save you from having to re-enter a large number of content locations when you create a new search.</span></span>
    
- <span data-ttu-id="88c99-114">검색 결과;의 크기를 줄이려면 예를 내보내려면 너무 많은 결과 반환 하는 검색을 사용 하는 경우 검색을 복제 하 고 검색 결과의 수를 줄이는 날짜 범위를 기반으로 검색 조건을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-114">To decrease the size of the search results; for example, if you have a search that returns too many results to export, you can clone the search and then add a search condition based on a date range to reduce the number of search results.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="88c99-115">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="88c99-115">Before you begin</span></span>

- <span data-ttu-id="88c99-116">보안에서 eDiscovery 관리자 역할 그룹의 구성원 이어야 하는 &amp; 준수 센터가이 항목에 설명 된 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-116">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script described in this topic.</span></span>
    
- <span data-ttu-id="88c99-p103">이 스크립트는 최소한의 오류 처리를 포함합니다. 스크립트의 기본 목적은 신속 하 게 콘텐츠 검색을 복제 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-p103">The script includes minimal error handling. The primary purpose of the script is to quickly clone a content search.</span></span>
    
- <span data-ttu-id="88c99-119">스크립트 콘텐츠 검색을 새로 만들지만 시작 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-119">The script creates a new Content Search, but doesn't start it.</span></span>
    
- <span data-ttu-id="88c99-p104">이 스크립트 복제 하려는 콘텐츠 검색 eDiscovery 사례와 관련이 있는지 여부를 고려 합니다. 검색 사례와 연결 된 경우 새 검색은 대/소문자와 연결 됩니다. 기존 검색 아니면 사례와 연결 하는 경우 새 검색 보안에서 **콘텐츠 검색** 페이지에 나열 됩니다 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-p104">This script takes into account whether the Content Search that you're cloning is associated with an eDiscovery case. If the search is associated with a case, the new search will also be associated with the same case. If the existing search isn't associated with a case, the new search will be listed on the **Content search** page in the Security &amp; Compliance Center.</span></span> 
    
- <span data-ttu-id="88c99-p105">이 항목에 제공 된 샘플 스크립트는 Microsoft 표준 지원 프로그램이 나 서비스에서 지원 되지 않습니다. 샘플 스크립트는 어떠한 보증도 없이 있는 그대로 제공 됩니다. Microsoft 추가로 포함 하 여, 제한 되지 않고 하는 모든 묵시적된 보증을 부인 묵시적 보증 상품성 또는 특정 목적에의 적합성입니다. 사용 또는 성능 샘플 스크립트 및 설명서에 발생 하는 위험은 있습니다. 어떠한 이벤트에 Microsoft, 해당 작성자 또는 다른 만들기, 제작, 또는 스크립트의 배달에 참여 하는 모든 책임을 지지 모든 손해에 대해 (포함 하 되, 제한 되지 않고 비즈니스 이익, 영업 중단, 손실 손실에 대 한 손해 비즈니스 정보 또는 기타 금전적 손실을) Microsoft가 그와 같은 손해의 가능성을 사전에 알고 있었던 경우에 사용 또는 설명서를 확인 하는 샘플 스크립트를 사용 하 여 원인으로 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-p105">The sample script provided in this topic isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-clone-a-search"></a><span data-ttu-id="88c99-128">1 단계: 스크립트를 실행 하는 검색 복제</span><span class="sxs-lookup"><span data-stu-id="88c99-128">Step 1: Run the script to clone a search</span></span>

<span data-ttu-id="88c99-p106">이 단계에서는 스크립트 기존을 복제 하 여 새 콘텐츠 검색을 만듭니다. 이 스크립트를 실행 하면 다음 정보에 대 한 묻는 메시지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-p106">The script in this step will create a new Content Search by cloning an existing one. When you run this script, you'll be prompted for the following information:</span></span>
  
- <span data-ttu-id="88c99-p107">**사용자 자격 증명** -스크립트 자격 증명을 사용 하 여 보안에 연결할 &amp; Windows PowerShell을 사용한 Office 365 조직에 대 한 준수 센터입니다. 듯이 보안에서 eDiscovery 관리자 역할 그룹의 구성원 이어야 하는 &amp; 준수 센터 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-p107">**Your user credentials** - The script will use your credentials to connect to the Security &amp; Compliance Center for your Office 365 organization with Windows PowerShell. As previously stated, you have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script.</span></span> 
    
- <span data-ttu-id="88c99-133">**기존 검색의 이름** 을-복제 하려는 콘텐츠 검색입니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-133">**The name of the existing search** - This is the Content Search that you want to clone.</span></span> 
    
- <span data-ttu-id="88c99-134">**만들 수 있는 새 검색의 이름** -이 값이 입력 하지 않으면, 스크립트를 기반으로 복제 하려는 검색의 이름을 새 검색에 대 한 이름을 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-134">**The name of the new search that will be created** - If you leave this value blank, the script will create a name for the new search that is based on the name of the search that you're cloning.</span></span> 
    
<span data-ttu-id="88c99-135">검색을 복제 합니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-135">To clone a search:</span></span>
  
1. <span data-ttu-id="88c99-136">.Ps1 파일 이름 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 예, `CloneSearch.ps1`합니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-136">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CloneSearch.ps1`.</span></span>
    
  ```
  # This PowerShell script clones an existing Content Search in the Office 365 Security &amp; Compliance Center
  # Get login credentials from the user
  if(!$UserCredential)
  {
      $UserCredential = Get-Credential
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
      if (!$Session)
      {
          Write-Error "Couldn't create a remote PowerShell session."
          return
      }
      Import-PSSession $Session -AllowClobber -DisableNameChecking
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)"
  }
  # Ask for the name of the search you want to clone
  $searchName = Read-Host 'Enter the name of the search that you want to clone'
  # Ask for the name of the new search
  $newSearchName = Read-Host 'Enter a name for the new search [leave blank to automatically generate a name]'
  $originalSearch = Get-ComplianceSearch $searchName -EA SilentlyContinue
  # Make sure we have a valid search before continuing
  if(!$originalSearch)
  {
      Write-Error "Couldn't find search: $searchName"
      return
  }
  $searchNameCounter = 1
  # Find a suitable name for the new search
  while(!$newSearchName)
  {
      $newSearchName = $originalSearch.Name + "_" + $searchNameCounter
      $tempSearch = Get-ComplianceSearch $newSearchName -EA SilentlyContinue
      if ($tempSearch)
      {
          $newSearchName = $null
          $searchNameCounter++
      }
  }
  $caseName
  # Determine if the search is part of a case; if so get the case name
  if ($originalSearch.CaseId)
  {
      $searchCase = Get-ComplianceCase $originalSearch.CaseId
      $caseName = $searchCase.Name
  }
  # Need to cast this value as a Boolean the old fashion way
  $allowNotFoundExchangeLocationsEnabled = $false
  if ($originalSearch.AllowNotFoundExchangeLocationsEnabled)
  {
      $allowNotFoundExchangeLocationsEnabled = $true
  }
  $newSearch = New-ComplianceSearch -Name $newSearchName -AllowNotFoundExchangeLocationsEnabled $allowNotFoundExchangeLocationsEnabled -Case $caseName -ContentMatchQuery $originalSearch.ContentMatchQuery -Description $originalSearch.Description -ExchangeLocation $originalSearch.ExchangeLocation -ExchangeLocationExclusion $originalSearch.ExchangeLocationExclusion -Language $originalSearch.Language -SharePointLocation $originalSearch.SharePointLocation -SharePointLocationExclusion $originalSearch.SharePointLocationExclusion -PublicFolderLocation $originalSearch.PublicFolderLocation
  if ($newSearch)
  {
      Write-Host $newSearch.Name "was successfully created" -ForegroundColor Yellow
  }
  ```

2. <span data-ttu-id="88c99-137">Windows PowerShell을 열고 스크립트를 저장 한 위치로 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-137">Open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="88c99-138">스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="88c99-138">Run the script; for example:</span></span>
    
    ```
    .\CloneSearch.ps1
    ```

4. <span data-ttu-id="88c99-139">사용자의 자격 증명에 대 한 대화 상자가 나타나면 전자 메일 주소와 암호를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-139">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span>
    
5. <span data-ttu-id="88c99-p108">정보는 스크립트에 의해 대화 상자가 나타나면 다음을 입력 합니다. 각 부분의 정보를 입력 하 고 **Enter**키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-p108">Enter following information when prompted by the script. Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="88c99-142">기존 검색의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-142">The name of the existing search.</span></span>
    
    - <span data-ttu-id="88c99-143">새 검색의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-143">The name of the new search.</span></span>
    
    <span data-ttu-id="88c99-p109">스크립트는 새로운 콘텐츠 검색을 만들고 있지만 시작 되지 않습니다. 이렇게 하면 기회를 편집 하 고 다음 단계에서 검색을 실행 합니다. **Get ComplianceSearch** cmdlet을 실행 하 여 또는 보안에서 **콘텐츠 검색** 또는 **eDiscovery** 페이지로 이동 하 여 새 검색의 속성을 볼 수 &amp; 새 검색 인지 여부에 따라 준수 센터 사례와 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-p109">The script creates the new Content Search, but doesn't start it. This gives you a chance to edit and run the search in the next step. You can view the properties of the new search by running the **Get-ComplianceSearch** cmdlet or by going to the **Content search** or **eDiscovery** page in the Security &amp; Compliance Center, depending on whether or not the new search is associated with a case.</span></span> 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-security-amp-compliance-center"></a><span data-ttu-id="88c99-147">2 단계: 편집 하 고 보안에서 복제 된 검색을 실행 하 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="88c99-147">Step 2: Edit and run the cloned search in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="88c99-p110">다음 단계는 보안으로 이동 하는 것은 했을 때를 실행 한 후 기존 콘텐츠 검색을 복제 하는 스크립트, &amp; 준수 센터 편집 하 고 새 검색을 실행 합니다. 듯이 키워드 검색 쿼리를 변경 하 고 추가 하 여 검색을 편집할 수 또는 검색 조건을 제거 합니다. 자세한 내용은 다음을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="88c99-p110">After the you've run the script to clone an existing Content Search, the next step is to go to the Security &amp; Compliance Center to edit and run the new search. As previously stated, you can edit a search by changing the keyword search query and adding or removing search conditions. For more information, see:</span></span>
  
- [<span data-ttu-id="88c99-151">Office 365의에서 콘텐츠 검색</span><span class="sxs-lookup"><span data-stu-id="88c99-151">Content Search in Office 365</span></span>](content-search.md)
    
- [<span data-ttu-id="88c99-152">콘텐츠 검색에 대한 키워드 쿼리 및 검색 조건</span><span class="sxs-lookup"><span data-stu-id="88c99-152">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
    
- [<span data-ttu-id="88c99-153">Office 365 보안에서 eDiscovery 사례 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="88c99-153">eDiscovery cases in the Office 365 Security &amp; Compliance Center</span></span>](ediscovery-cases.md)
