---
title: 여러 콘텐츠 검색 만들기, 보고하기 및 삭제
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
ms.assetid: 1d463dda-a3b5-4675-95d4-83db19c9c4a3
description: Office 365 보안 &amp; 및 준수 센터에서 PowerShell 스크립트를 통해 검색을 만들고 보고서를 실행 하는 등의 콘텐츠 검색 작업을 자동화 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 740f3384e5d4f26e09512cc846ad8779bcbc31ef
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670663"
---
# <a name="create-report-on-and-delete-multiple-content-searches"></a><span data-ttu-id="a3325-103">여러 콘텐츠 검색 만들기, 보고하기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="a3325-103">Create, report on, and delete multiple Content Searches</span></span>

 <span data-ttu-id="a3325-104">원본으로 사용 하는 데이터에 대 한 정보를 확인 하 고 검색의 다양성 및 품질을 확인할 때 검색 검색을 빠르게 만들고 보고 하는 것은 eDiscovery 및 조사에서 중요 한 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-104">Quickly creating and reporting discovery searches is often an important step in eDiscovery and investigations when you're trying to learn about the underlying data, and the richness and quality of your searches.</span></span> <span data-ttu-id="a3325-105">이를 위해 보안 &amp; 준수 센터는 시간이 오래 걸리는 콘텐츠 검색 작업을 자동화 하는 Windows PowerShell cmdlet 집합을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-105">To help you do this, the Security &amp; Compliance Center offers a set of Windows PowerShell cmdlets to automate time-consuming Content Search tasks.</span></span> <span data-ttu-id="a3325-106">이러한 스크립트를 통해 신속 하 고 간편 하 게 다양 한 검색을 만든 다음 해당 데이터의 양을 확인 하는 데 도움이 되는 예상 검색 결과의 보고서를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-106">These scripts provide a quick and easy way to create a number of searches, and then run reports of the estimated search results that can help you determine the quantity of data in question.</span></span> <span data-ttu-id="a3325-107">스크립트를 사용 하 여 각 검색 결과가 생성 되는 결과를 비교할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-107">You can also use the scripts to create different versions of searches to compare the results each one produces.</span></span> <span data-ttu-id="a3325-108">이러한 스크립트는 데이터를 빠르고 효율적으로 식별 하 고 cull 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-108">These scripts can help you to quickly and efficiently identify and cull your data.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="a3325-109">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="a3325-109">Before you begin</span></span>

- <span data-ttu-id="a3325-110">이 항목에서 설명 하는 스크립트를 실행 하려면 보안 &amp; 및 준수 센터에서 eDiscovery 관리자 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-110">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the scripts that are described in this topic.</span></span> 
    
- <span data-ttu-id="a3325-111">1 단계에서 CSV 파일에 추가할 수 있는 조직 내 비즈니스용 OneDrive 사이트의 url 목록을 수집 하려면 [조직에서 모든 OneDrive 위치 목록 만들기](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a3325-111">To collect a list of the URLs for the OneDrive for Business sites in your organization that you can add to the CSV file in Step 1, see [Create a list of all OneDrive locations in your organization](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a).</span></span> 
    
- <span data-ttu-id="a3325-112">이 항목에서 만드는 모든 파일을 동일한 폴더에 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-112">Be sure to save all the files that you create in this topic to the same folder.</span></span> <span data-ttu-id="a3325-113">이를 통해 스크립트를 보다 쉽게 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-113">That will make it easier to run the scripts.</span></span>
    
- <span data-ttu-id="a3325-114">스크립트에는 최소 오류 처리가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-114">The scripts include minimal error handling.</span></span> <span data-ttu-id="a3325-115">주요 목적은 여러 콘텐츠 검색을 빠르게 작성, 보고 및 삭제 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-115">Their primary purpose is to quickly create, report on, and delete multiple Content Searches.</span></span>
    
- <span data-ttu-id="a3325-p104">이 항목에서 제공된 샘플 스크립트는 Microsoft 표준 지원 프로그램 또는 서비스에서는 지원되지 않습니다. 샘플 스크립트는 어떠한 보증도 없이 "있는 그대로" 제공됩니다. Microsoft는 묵시적인 모든 보증(상품성 또는 특정 목적에의 적합성에 대한 묵시적인 보증을 포함하되 이에 제한되지 않음)을 부인합니다. 샘플 스크립트 및 문서의 사용 또는 수행으로 인해 발생하는 모든 위험은 사용자의 책임입니다. 어떠한 경우에도 Microsoft, 스크립트 작성자 또는 스크립트의 작성, 생산 또는 제공과 관련된 사람은 누구나 샘플 스크립트 또는 문서의 사용 또는 사용 불가능으로 인해 발생하는 모든 손해(수익에 대한 손실, 비즈니스 중단, 비즈니스 정보 손실 또는 기타 금전상의 손실을 포함하되 이에 제한되지 않음)에 대해 책임지지 않습니다. 이는 Microsoft가 이러한 손해가 발생할 가능성에 대해 알고 있었더라고 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-searches-you-want-to-run"></a><span data-ttu-id="a3325-121">1 단계: 실행할 검색에 대 한 정보가 포함 된 CSV 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="a3325-121">Step 1: Create a CSV file that contains information about the searches you want to run</span></span>

<span data-ttu-id="a3325-122">이 단계에서 만드는 CSV (쉼표로 구분 된 값) 파일에는 검색 하려는 각 사용자에 대 한 행이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-122">The comma separated value (CSV) file that you create in this step contains a row for each user that want to search.</span></span> <span data-ttu-id="a3325-123">사용자의 Exchange Online 사서함 (보관 사서함이 사용 하도록 설정 된 경우 포함) 및 해당 비즈니스용 OneDrive 사이트를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-123">You can search the user's Exchange Online mailbox (which includes the archive mailbox, if it's enabled) and their OneDrive for Business site.</span></span> <span data-ttu-id="a3325-124">또는 사서함 또는 비즈니스용 OneDrive 사이트를 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-124">Or you can search just the mailbox or the OneDrive for Business site.</span></span> <span data-ttu-id="a3325-125">SharePoint Online 조직의 모든 사이트를 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-125">You can also search any site in your SharePoint Online organization.</span></span> <span data-ttu-id="a3325-126">3 단계에서 실행 하는 스크립트는 CSV 파일의 각 행에 대해 별도의 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-126">The script that you run in Step 3 will create a separate search for each row in the CSV file.</span></span> 
  
1. <span data-ttu-id="a3325-127">메모장을 사용 하 여 다음 텍스트를 복사한 후 .txt 파일에 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-127">Copy and paste the following text into a .txt file using NotePad.</span></span> <span data-ttu-id="a3325-128">이 파일을 로컬 컴퓨터의 폴더에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-128">Save this file to a folder on your local computer.</span></span> <span data-ttu-id="a3325-129">다른 스크립트도이 폴더에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-129">You'll save the other scripts to this folder as well.</span></span>
    
    ```
    ExchangeLocation,SharePointLocation,ContentMatchQuery,StartDate,EndDate
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2000,12/31/2005
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2006,12/31/2010
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2011,3/21/2016
    ,https://contoso.sharepoint.com/sites/contoso,,,3/21/2016
    ,https://contoso-my.sharepoint.com/personal/davidl_contoso_onmicrosoft_com,,1/1/2015,
    ,https://contoso-my.sharepoint.com/personal/janets_contoso_onmicrosoft_com,,1/1/2015,
    ```

    <span data-ttu-id="a3325-130">파일의 첫 번째 행 또는 머리글 행에는 새 콘텐츠 검색을 만들기 위해 **ComplianceSearch** cmdlet (3 단계의 스크립트)에서 사용 하는 매개 변수가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-130">The first row, or header row, of the file lists the parameters that will be used by **New-ComplianceSearch** cmdlet (in the script in Step 3) to create a new Content Searches.</span></span> <span data-ttu-id="a3325-131">각 매개 변수 이름은 쉼표로 구분됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-131">Each parameter name is separated by a comma.</span></span> <span data-ttu-id="a3325-132">머리글 행에 공백이 없는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-132">Make sure there aren't any spaces in the header row.</span></span> <span data-ttu-id="a3325-133">머리글 행 아래의 각 행은 각 검색에 대 한 매개 변수 값을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-133">Each row under the header row represents the parameter values for each search.</span></span> <span data-ttu-id="a3325-134">CSV 파일의 자리 표시자 데이터를 실제 데이터로 바꿔야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-134">Be sure to replace the placeholder data in the CSV file with your actual data.</span></span> 
    
2. <span data-ttu-id="a3325-135">Excel에서 .txt 파일을 열고 다음 표의 정보를 사용 하 여 각 검색에 대 한 정보로 파일을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-135">Open the .txt file in Excel, and then use the information in the following table to edit the file with information for each search.</span></span> 
    
    |<span data-ttu-id="a3325-136">**매개 변수**</span><span class="sxs-lookup"><span data-stu-id="a3325-136">**Parameter**</span></span>|<span data-ttu-id="a3325-137">**설명**</span><span class="sxs-lookup"><span data-stu-id="a3325-137">**Description**</span></span>|
    |:-----|:-----|
    | `ExchangeLocation` <br/> |<span data-ttu-id="a3325-138">사용자 사서함의 SMTP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-138">The SMTP address of the user's mailbox.</span></span>  <br/> |
    | `SharePointLocation` <br/> |<span data-ttu-id="a3325-139">사용자의 비즈니스용 OneDrive 사이트 url 또는 조직의 모든 사이트에 대 한 url입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-139">The URL for the user's OneDrive for Business site or the URL for any site in your organization.</span></span> <span data-ttu-id="a3325-140">비즈니스용 OneDrive 사이트의 URL에 대해 다음 ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-140">For the URL for OneDrive for Business sites, use this format: ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `.</span></span> <span data-ttu-id="a3325-141">예:  `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.</span><span class="sxs-lookup"><span data-stu-id="a3325-141">For example,  `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.</span></span>  <br/> |
    | `ContentMatchQuery` <br/> |<span data-ttu-id="a3325-142">검색에 대 한 검색 쿼리</span><span class="sxs-lookup"><span data-stu-id="a3325-142">The search query for the search.</span></span> <span data-ttu-id="a3325-143">검색 쿼리를 만드는 방법에 대 한 자세한 내용은 [키워드 쿼리 및 검색 조건을](keyword-queries-and-search-conditions.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a3325-143">For more information about creating a search query, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>  <br/> |
    | `StartDate` <br/> |<span data-ttu-id="a3325-144">전자 메일의 경우 받는 사람이 또는 메시지를 받은 날짜나 보낸 사람이 보낸 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-144">For email, the date on or after a message was received by a recipient or sent by the sender.</span></span> <span data-ttu-id="a3325-145">SharePoint 또는 비즈니스용 OneDrive 사이트에 대 한 문서에는 문서를 마지막으로 수정한 날짜 또는 그 이후의 날짜가 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-145">For documents on SharePoint or OneDrive for Business sites, the date on or after a document was last modified.</span></span>  <br/> |
    | `EndDate` <br/> |<span data-ttu-id="a3325-146">전자 메일의 경우 사용자가 보낸 메시지를 보내거나 받은 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-146">For email, the date on or before a message was sent by a sent by the user.</span></span> <span data-ttu-id="a3325-147">SharePoint 또는 비즈니스용 OneDrive 사이트에 대 한 문서는 마지막으로 문서를 수정한 날짜 또는 그 전에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-147">For documents on SharePoint or OneDrive for Business sites, the date on or before a document was last modified.</span></span>  <br/> |
   
3. <span data-ttu-id="a3325-148">Excel 파일을 로컬 컴퓨터의 폴더에 CSV 파일로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-148">Save the Excel file as a CSV file to a folder on your local computer.</span></span> <span data-ttu-id="a3325-149">3 단계에서 만든 스크립트는이 CSV 파일의 정보를 사용 하 여 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-149">The script that you create in Step 3 will use the information in this CSV file to create the searches.</span></span> 
  
## <a name="step-2-connect-to-security--compliance-center-powershell"></a><span data-ttu-id="a3325-150">2 단계: 보안 & 준수 센터 PowerShell에 연결</span><span class="sxs-lookup"><span data-stu-id="a3325-150">Step 2: Connect to Security & Compliance Center PowerShell</span></span>

<span data-ttu-id="a3325-151">다음 단계는 Windows PowerShell을 조직의 보안 &amp; 및 준수 센터에 연결 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-151">The next step is to connect Windows PowerShell to the Security &amp; Compliance Center for your organization.</span></span>
  
1. <span data-ttu-id="a3325-152">파일 이름 접미사. p s 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예를 `ConnectSCC.ps1`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-152">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `ConnectSCC.ps1`.</span></span> <span data-ttu-id="a3325-153">CSV 파일을 저장 한 폴더와 동일한 파일을 1 단계에서 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-153">Save the file to the same folder that you saved the CSV file to in Step 1.</span></span>
    
    ```
    # Get login credentials 
    $UserCredential = Get-Credential 
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
    Import-PSSession $Session -AllowClobber -DisableNameChecking 
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. <span data-ttu-id="a3325-154">로컬 컴퓨터에서 Windows PowerShell을 열고, 이전 단계에서 만든 스크립트가 있는 폴더로 이동한 다음 스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="a3325-154">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\ConnectSCC.ps1
    ```
  
## <a name="step-3-run-the-script-to-create-and-start-the-searches"></a><span data-ttu-id="a3325-155">3 단계: 스크립트를 실행 하 여 검색 만들기 및 시작</span><span class="sxs-lookup"><span data-stu-id="a3325-155">Step 3: Run the script to create and start the searches</span></span>

<span data-ttu-id="a3325-156">이 단계의 스크립트에서는 1 단계에서 만든 CSV 파일의 각 행에 대해 별도의 콘텐츠 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-156">The script in this step will create a separate Content Search for each row in the CSV file that you created in Step 1.</span></span> <span data-ttu-id="a3325-157">이 스크립트를 실행 하면 다음 두 가지 값을 입력 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-157">When you run this script, you'll be prompted for two values:</span></span>
  
- <span data-ttu-id="a3325-158">**검색 그룹 ID** -이 이름은 CSV 파일에서 만든 검색을 쉽게 구성 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-158">**Search Group ID** - This name provides an easy way to organize the searches that are created from the CSV file.</span></span> <span data-ttu-id="a3325-159">만들어진 각 검색은 검색 그룹 ID를 사용 하 여 이름이 지정 되 고 검색 이름에 숫자가 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-159">Each search that's created is named with the Search Group ID, and then a number is appended to the search name.</span></span> <span data-ttu-id="a3325-160">예를 들어 검색 그룹 ID에 대해 **ContosoCase** 를 입력 하면 **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**등의 검색 이름이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-160">For example, if you enter **ContosoCase** for the Search Group ID, then the searches are named **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**, and so on.</span></span> <span data-ttu-id="a3325-161">입력 하는 이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-161">Note that the name you type is case sensitive.</span></span> <span data-ttu-id="a3325-162">4 단계와 5 단계에서 검색 그룹 ID를 사용 하는 경우에는이를 만들 때와 동일한 대/소문자를 함께 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-162">When you use the Search Group ID in Step 4 and Step 5, you have to use the same case as you did when you created it.</span></span> 
    
- <span data-ttu-id="a3325-163">**CSV file** -1 단계에서 만든 CSV 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-163">**CSV file** - The name of the CSV file that you created in Step 1.</span></span> <span data-ttu-id="a3325-164">전체 파일 이름 사용을 포함 하 고 .csv 파일 확장명을 포함 해야 합니다. 예를 `ContosoCase.csv`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-164">Be sure to include the use the full filename, include the .csv file extension; for example,  `ContosoCase.csv`.</span></span>
    
<span data-ttu-id="a3325-165">스크립트를 실행하려면</span><span class="sxs-lookup"><span data-stu-id="a3325-165">To run the script:</span></span>

1. <span data-ttu-id="a3325-166">파일 이름 접미사. p s 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예를 `CreateSearches.ps1`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-166">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CreateSearches.ps1`.</span></span> <span data-ttu-id="a3325-167">다른 파일을 저장 한 동일한 폴더에 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-167">Save the file to the same folder where you saved the other files.</span></span>
    
  ```Powershell
  # Get the Search Group ID and the location of the CSV input file
  $searchGroup = Read-Host 'Search Group ID'
  $csvFile = Read-Host 'Source CSV file'
    
  # Do a quick check to make sure our group name will not collide with other searches
  $searchCounter = 1
  import-csv $csvFile |
    ForEach-Object{
    
    $searchName = $searchGroup +'_' + $searchCounter
    $search = Get-ComplianceSearch $searchName -EA SilentlyContinue
    if ($search)
    {
        Write-Error "The Search Group ID conflicts with existing searches.  Please choose a search group name and restart the script."
        return
    }
    $searchCounter++
  }
    
  $searchCounter = 1
  import-csv $csvFile |
    ForEach-Object{
    
    # Create the query
    $query = $_.ContentMatchQuery
    if(($_.StartDate -or $_.EndDate))
    {
          # Add the appropriate date restrictions.  NOTE: Using the Date condition property here because it works across Exchange, SharePoint, and OneDrive for Business.
          # For Exchange, the Date condition property maps to the Sent and Received dates; for SharePoint and OneDrive for Business, it maps to Created and Modified dates.
          if($query)
          {
              $query += " AND"
          }
          $query += " ("
          if($_.StartDate)
          {
              $query += "Date >= " + $_.StartDate
          }
          if($_.EndDate)
          {
              if($_.StartDate)
              {
                  $query += " AND "
              }
              $query += "Date <= " + $_.EndDate
          }
          $query += ")"
    }
      
      # -ExchangeLocation can't be set to an empty string, set to null if there's no location.
      $exchangeLocation = $null
      if ( $_.ExchangeLocation)
      {
           $exchangeLocation = $_.ExchangeLocation
      }
    
    # Create and run the search        
    $searchName = $searchGroup +'_' + $searchCounter
    Write-Host "Creating and running search: " $searchName -NoNewline
    $search = New-ComplianceSearch -Name $searchName -ExchangeLocation $exchangeLocation -SharePointLocation $_.SharePointLocation -ContentMatchQuery $query
    
    # Start and wait for each search to complete
    Start-ComplianceSearch $search.Name
    while ((Get-ComplianceSearch $search.Name).Status -ne "Completed")
    {
        Write-Host " ." -NoNewline
        Start-Sleep -s 3
    }
    Write-Host ""
    
    $searchCounter++
  }
  ```

2. <span data-ttu-id="a3325-168">Windows PowerShell에서 이전 단계에서 스크립트를 저장 한 폴더로 이동한 후 스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="a3325-168">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```Powershell
    .\CreateSearches.ps1
    ```

3. <span data-ttu-id="a3325-169">**검색 그룹 ID** 프롬프트에 검색 그룹 이름을 입력 하 고 enter 키를 누릅니다. \*\*\*\* 예를 `ContosoCase`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-169">At the **Search Group ID** prompt, type a search group name, and then press **Enter**; for example,  `ContosoCase`.</span></span> <span data-ttu-id="a3325-170">이 이름은 대/소문자를 구분 하므로 이후 단계에서 동일한 방식으로 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-170">Remember that this name is case sensitive, so you'll have to type it the same way in the subsequent steps.</span></span>
    
4. <span data-ttu-id="a3325-171">**원본 csv 파일** 프롬프트에 .csv 파일 확장명을 포함 하 여 csv 파일의 이름을 입력 합니다. 예를 `ContosoCase.csv`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-171">At the **Source CSV file** prompt, type the name of the CSV file, including the .csv file extension; for example,  `ContosoCase.csv`.</span></span>
    
5. <span data-ttu-id="a3325-172">enter \*\*\*\* 키를 눌러 스크립트를 계속 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-172">Press **Enter** to continue running the script.</span></span> 
    
    <span data-ttu-id="a3325-173">이 스크립트는 검색 만들기 및 실행 진행률을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-173">The script displays the progress of creating and running the searches.</span></span> <span data-ttu-id="a3325-174">스크립트가 완료 되 면 프롬프트로 돌아옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-174">When the script is complete, it returns to the prompt.</span></span> 
    
    ![여러 규정 준수 검색을 만드는 스크립트를 실행한 경우의 샘플 출력](media/37d59b0d-5f89-4dbc-9e2d-0e88e2ed7b4c.png)
  
## <a name="step-4-run-the-script-to-report-the-search-estimates"></a><span data-ttu-id="a3325-176">4 단계: 스크립트를 실행 하 여 검색 예측 보고</span><span class="sxs-lookup"><span data-stu-id="a3325-176">Step 4: Run the script to report the search estimates</span></span>

<span data-ttu-id="a3325-177">검색을 만든 후에는 3 단계에서 만든 각 검색의 검색 적중 횟수에 대 한 간단한 보고서를 표시 하는 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-177">After you create the searches, the next step is to run a script that displays a simple report of the number of search hits for each search that was created in Step 3.</span></span> <span data-ttu-id="a3325-178">보고서에는 각 검색의 결과 크기와 모든 검색의 총 방문 횟수 및 전체 크기가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-178">The report also includes the size of results for each search, and the total number of hits and total size of all searches.</span></span> <span data-ttu-id="a3325-179">보고 스크립트를 실행 하면 검색 그룹 ID와 csv 파일에 보고서를 저장 하려는 경우 csv 파일 이름을 입력 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-179">When you run the reporting script, you'll be prompted for the Search Group ID, and a CSV filename if you want to save the report to a CSV file.</span></span>
  
1. <span data-ttu-id="a3325-180">파일 이름 접미사. p s 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예를 `SearchReport.ps1`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-180">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `SearchReport.ps1`.</span></span> <span data-ttu-id="a3325-181">다른 파일을 저장 한 동일한 폴더에 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-181">Save the file to the same folder where you saved the other files.</span></span>
    
  ```Powershell
  $searchGroup = Read-Host 'Search Group ID'
  $outputFile = Read-Host 'Enter a file name or file path to save the report to a .csv file. Leave blank to only display the report'
  $searches = Get-ComplianceSearch | ?{$_.Name -clike $searchGroup + "_*"}
  $allSearchStats = @()
  foreach ($partialObj in $searches)
  {
      $search = Get-ComplianceSearch $partialObj.Name
      $sizeMB = [System.Math]::Round($search.Size / 1MB, 2)
      $searchStatus = $search.Status
      if($search.Errors)
      {
          $searchStatus = "Failed"
      }elseif($search.NumFailedSources -gt 0)
      {
          $searchStatus = "Failed Sources"
      }
      $searchStats = New-Object PSObject
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Name -Value $search.Name
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name ContentMatchQuery -Value $search.ContentMatchQuery
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Status -Value $searchStatus
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Items -Value $search.Items
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name "Size" -Value $search.Size
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name "Size(MB)" -Value $sizeMB
      $allSearchStats += $searchStats
  }
  # Calculate the totals
  $allItems = ($allSearchStats | Measure-Object Items -Sum).Sum
  # Convert the total size to MB and round to the nearst 100th
  $allSize = ($allSearchStats | Measure-Object 'Size' -Sum).Sum
  $allSizeMB = [System.Math]::Round($allSize  / 1MB, 2)
  # Get the total successful searches and total of all searches
  $allSuccessCount = ($allSearchStats |?{$_.Status -eq "Completed"}).Count
  $allCount = $allSearchStats.Count
  $allStatus = [string]$allSuccessCount + " of " + [string]$allCount
  # Totals Row
  $totalSearchStats = New-Object PSObject
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Name -Value "Total"
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Status -Value $allStatus
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Items -Value $allItems
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name "Size(MB)" -Value $allSizeMB
  $allSearchStats += $totalSearchStats
  # Just get the columns we're interested in showing
  $allSearchStatsPrime = $allSearchStats | Select-Object Name, Status, Items, "Size(MB)", ContentMatchQuery
  # Print the results to the screen
  $allSearchStatsPrime |ft -AutoSize -Wrap
  # Save the results to a CSV file
  if ($outputFile)
  {
      $allSearchStatsPrime | Export-Csv -Path $outputFile -NoTypeInformation
  }
  ```

2. <span data-ttu-id="a3325-182">Windows PowerShell에서 이전 단계에서 스크립트를 저장 한 폴더로 이동한 후 스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="a3325-182">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```Powershell
    .\SearchReport.ps1
    ```

3. <span data-ttu-id="a3325-183">**검색 그룹 ID** 프롬프트에 검색 그룹 이름을 입력 하 고 enter 키를 누릅니다. \*\*\*\* 예를 `ContosoCase`들어</span><span class="sxs-lookup"><span data-stu-id="a3325-183">At the **Search Group ID** prompt, type a search group name, and then press **Enter**; for example  `ContosoCase`.</span></span> <span data-ttu-id="a3325-184">이 이름은 대/소문자를 구분 하므로 3 단계에서 스크립트를 실행할 때와 동일한 방식으로 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-184">Remember that this name is case sensitive, so you'll have to type it the same way you did when you ran the script in Step 3.</span></span>
    
4. <span data-ttu-id="a3325-185">보고서를 **csv 파일에 저장 하는 파일 경로 (보고서를 표시 하는 경우에는 비워 둠)** 를 선택 하 고 보고서를 csv 파일에 저장 하려면 전체 파일 이름 경로 (.csv 파일 확장명 포함)의 파일 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-185">At the **File path to save the report to a CSV file (leave blank to just display the report)** prompt, type a file name of complete filename path (including the .csv file extension) if you want to save the report to a CSV file.</span></span> <span data-ttu-id="a3325-186">.csv 파일 확장명을 포함 한 csv 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-186">name of the CSV file, including the .csv file extension.</span></span> <span data-ttu-id="a3325-187">예를 `ContosoCaseReport.csv` 들어 현재 디렉터리에 파일을 저장 하거나 다른 폴더에 저장 하도록 입력할 수 `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-187">For example, you could type  `ContosoCaseReport.csv` to save it to the current directory or you could type  `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` to save it to a different folder.</span></span> <span data-ttu-id="a3325-188">또한 메시지를 비워 두면 보고서를 표시 하지만 파일에 저장 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-188">You can also leave the prompt blank to display the report but not save it to a file.</span></span> 
    
5. <span data-ttu-id="a3325-189">**Enter** 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-189">Press **Enter**.</span></span>
    
    <span data-ttu-id="a3325-190">이 스크립트는 검색 만들기 및 실행 진행률을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-190">The script displays the progress of creating and running the searches.</span></span> <span data-ttu-id="a3325-191">스크립트가 완료 되 면 보고서가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-191">When the script is complete, the report is displayed.</span></span> 
    
    ![검색 보고서를 실행하여 검색 그룹에 대한 예상 결과 표시](media/3b5f2595-71d5-4a14-9214-fad156c981f8.png)
  
> [!NOTE]
> <span data-ttu-id="a3325-193">같은 사서함 이나 사이트가 검색 그룹에서 둘 이상의 검색에서 콘텐츠 위치로 지정 된 경우 보고서의 총 결과 (항목 수와 총 크기 모두)가 같은 항목에 대 한 결과를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-193">If the same mailbox or site is specified as a content location in more than one search in a search group, the total results estimate in the report (for both the number of items and the total size) might include results for the same items.</span></span> <span data-ttu-id="a3325-194">이는 검색 그룹의 서로 다른 검색에 대 한 쿼리와 일치 하는 경우 동일한 전자 메일 메시지나 문서가 두 번 이상 계산 되기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-194">That's because the same email message or document will be counted more than once if it matches the query for different searches in the search group.</span></span> 
  
## <a name="step-5-run-the-script-to-delete-the-searches"></a><span data-ttu-id="a3325-195">5 단계: 스크립트를 실행 하 여 검색 삭제</span><span class="sxs-lookup"><span data-stu-id="a3325-195">Step 5: Run the script to delete the searches</span></span>

<span data-ttu-id="a3325-196">검색을 많이 만들 수도 있으므로이 마지막 스크립트를 사용 하면 3 단계에서 만든 검색을 쉽게 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-196">Because you might be creating a lot of searches, this last script just makes it easy to quickly delete the searches you created in Step 3.</span></span> <span data-ttu-id="a3325-197">다른 스크립트와 마찬가지로이 방법 에서도 검색 그룹 ID를 입력 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-197">Like the other scripts, this one also prompts you for the Search Group ID.</span></span> <span data-ttu-id="a3325-198">이 스크립트를 실행 하면 검색 이름에 검색 그룹 ID가 있는 모든 검색은 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-198">All searches with the Search Group ID in the search name will be deleted when you run this script.</span></span> 
  
1. <span data-ttu-id="a3325-199">파일 이름 접미사. p s 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예를 `DeleteSearches.ps1`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-199">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `DeleteSearches.ps1`.</span></span> <span data-ttu-id="a3325-200">다른 파일을 저장 한 동일한 폴더에 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-200">Save the file to the same folder where you saved the other files.</span></span>
    
  ```Powershell
  # Delete all searches in a search group
  $searchGroup = Read-Host 'Search Group ID'
  Get-ComplianceSearch |
      ForEach-Object{
      # If the name matches the search group name pattern (case sensitive), delete the search
      if ($_.Name -cmatch $searchGroup + "_\d+")
      {
          Write-Host "Deleting search: " $_.Name
          Remove-ComplianceSearch $_.Name -Confirm:$false
      }
  }
  ```

2. <span data-ttu-id="a3325-201">Windows PowerShell에서 이전 단계에서 스크립트를 저장 한 폴더로 이동한 후 스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="a3325-201">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```Powershell
    .\DeleteSearches.ps1
    ```

3. <span data-ttu-id="a3325-202">**검색 그룹 ID** 프롬프트에 삭제할 검색의 검색 그룹 이름을 입력 한 다음 enter 키를 누릅니다. \*\*\*\* 예를 `ContosoCase`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-202">At the **Search Group ID** prompt, type a search group name for the searches that you want to delete, and then press **Enter**; for example,  `ContosoCase`.</span></span> <span data-ttu-id="a3325-203">이 이름은 대/소문자를 구분 하므로 3 단계에서 스크립트를 실행할 때와 동일한 방식으로 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-203">Remember that this name is case sensitive, so you'll have to type it the same way you did when you ran the script in Step 3.</span></span>
    
    <span data-ttu-id="a3325-204">스크립트에는 삭제 된 각 검색의 이름이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3325-204">The script displays the name of each search that's deleted.</span></span>
    
    ![검색 그룹에서 검색을 삭제하기 위한 스크립트 실행](media/9d97b9d6-a539-4d9b-a4e4-e99989144ec7.png)
