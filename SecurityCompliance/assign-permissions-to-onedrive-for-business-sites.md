---
title: 비즈니스용 OneDrive 사이트에 eDiscovery 사용 권한 할당
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/27/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: 422858ff-917b-46d4-9e5b-3397f60eee4d
description: 특정 키워드, 중요 한 정보 및 기타 검색 조건에 대 한 조직에서 비즈니스 사이트에 대 한 모든 OneDrive를 검색 하려면 SharePoint Online에서 eDiscovery 센터를 사용할 수 있습니다. 조직에서 각 사용자가 자신의 OneDrive 이름이 지정 된 사이트 모음에 있는 비즈니스 사이트의 소유자 https://domain-my.sharepoint.com합니다. 기본적으로 Office 365 전역 관리자 또는 규정 준수 관리자는 비즈니스 사이트에 대 한 모든 OneDrive를 검색 하려면 SharePoint Online에서 eDiscovery 센터를 사용할 수 없습니다. 비즈니스 사이트, 관리자 또는 규정 준수 관리자에 대 한 OneDrive를 검색 하려면 해당 onedrive 비즈니스 사이트에 대 한 사이트 모음 관리자 여야 합니다.
ms.openlocfilehash: 48f84dfe21f0f99913ba2c27123d6c0e1f8bc03f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533520"
---
# <a name="assign-ediscovery-permissions-to-onedrive-for-business-sites"></a><span data-ttu-id="28ba9-106">비즈니스용 OneDrive 사이트에 eDiscovery 사용 권한 할당</span><span class="sxs-lookup"><span data-stu-id="28ba9-106">Assign eDiscovery permissions to OneDrive for Business sites</span></span>

<span data-ttu-id="28ba9-p102">특정 키워드, 중요 한 정보 및 기타 검색 조건에 대 한 조직에서 비즈니스 사이트에 대 한 모든 OneDrive를 검색 하려면 SharePoint Online에서 eDiscovery 센터를 사용할 수 있습니다. 조직에서 각 사용자가 자신의 OneDrive 이름이 지정 된 사이트 모음에 있는 비즈니스 사이트의 소유자 https://domain-my.sharepoint.com합니다. 기본적으로 Office 365 전역 관리자 또는 규정 준수 관리자는 비즈니스 사이트에 대 한 모든 OneDrive를 검색 하려면 SharePoint Online에서 eDiscovery 센터를 사용할 수 없습니다. 비즈니스 사이트, 관리자 또는 규정 준수 관리자에 대 한 OneDrive를 검색 하려면 해당 onedrive 비즈니스 사이트에 대 한 사이트 모음 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p102">You can use the eDiscovery Center in SharePoint Online to search all OneDrive for Business sites in your organization for certain keywords, sensitive information, and other search criteria. Each user in your organization is the owner of their OneDrive for Business site, which is located in the site collection named https://domain-my.sharepoint.com. By default, an Office 365 global administrator or compliance manager can't use the eDiscovery Center in SharePoint Online to search any OneDrive for Business sites. To search a OneDrive for Business site, administrators or compliance managers must be a site collection administrator for that OneDrive for Business site.</span></span> 
  
<span data-ttu-id="28ba9-111">이 문서에서는 조직에서 관리자 또는 규정 준수 관리자 비즈니스 사이트에 대 한 모든 OneDrive에 대 한 사이트 모음 관리자를 확인 하는 단계를 안내 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-111">This article guides you through the steps to make an administrator or compliance manager a site collection administrator for every OneDrive for Business site in your organization.</span></span> 
  
<span data-ttu-id="28ba9-112">이 문서에서는 비즈니스 사이트에 대 한 사이트 모음 관리자로 OneDrive에서 사용자를 제거 하려면 3 단계에서에서 스크립트를 수정 하는 포함 하 여 스크립트를 사용 하는 방법에 대 한 팁에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="28ba9-112">See the [More information](#more-information) section for tips about using the script in this article, including revising the script in Step 3 to remove a user as a site collection administrator from OneDrive for Business sites.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="28ba9-113">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="28ba9-113">Before you begin</span></span>

- <span data-ttu-id="28ba9-p103">SharePoint Online 관리 셸을 설치 합니다. 내용은 [SharePoint Online 관리 셸 Windows PowerShell 환경 설정](https://go.microsoft.com/fwlink/p/?LinkID=286318)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p103">Install the SharePoint Online Management Shell. For information, see [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318).</span></span>
    
- <span data-ttu-id="28ba9-116">조직에서 비즈니스 사이트에 대 한 모든 OneDrive에 사이트 모음 관리자 권한으로 사용자를 할당 하려는 때마다 3 단계에서에서 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-116">Run the script in Step 3 each time you want to assign a user as a site collection administrator to any OneDrive for Business sites in your organization.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="28ba9-p104">관리자 또는 규정 준수 관리자에 게 OneDrive에 대 한 사이트 모음 관리자는 비즈니스 사이트 수 있는 비즈니스 문서 라이브러리에 대 한 사용자의 OneDrive 열고 소유자와 동일한 작업을 수행 하기 위한 합니다. 제어 하 고 사용자가 할당 된 사용 권한을 eDiscovery OneDrive 조직에서 비즈니스 사이트에 대 한 모니터링을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p104">An administrator or compliance manager who is a site collection administrator for OneDrive for Business sites can open users' OneDrive for Business document libraries and perform the same tasks as the owner. It's important to control and monitor who has been assigned eDiscovery permissions to OneDrive for Business sites in your organization.</span></span> 
  
- <span data-ttu-id="28ba9-p105">이 문서에서 제공 되는 샘플 스크립트는 Microsoft 표준 지원 프로그램이 나 서비스에서 지원 되지 않습니다. 샘플 스크립트는 어떠한 보증도 없이 있는 그대로 제공 됩니다. Microsoft 추가로 포함 하 여, 제한 되지 않고 하는 모든 묵시적된 보증을 부인 묵시적 보증 상품성 또는 특정 목적에의 적합성입니다. 사용 또는 성능 샘플 스크립트 및 설명서에 발생 하는 위험은 있습니다. 어떠한 이벤트에 Microsoft, 해당 작성자 또는 다른 만들기, 제작, 또는 스크립트의 배달에 참여 하는 모든 책임을 지지 모든 손해에 대해 (포함 하 되, 제한 되지 않고 비즈니스 이익, 영업 중단, 손실 손실에 대 한 손해 비즈니스 정보 또는 기타 금전적 손실을) Microsoft가 그와 같은 손해의 가능성을 사전에 알고 있었던 경우에 사용 또는 설명서를 확인 하는 샘플 스크립트를 사용 하 여 원인으로 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p105">The sample script provided in this article isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the script be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample script or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-collect-a-list-of-all-onedrive-for-business-sites"></a><span data-ttu-id="28ba9-124">1 단계: 비즈니스 사이트에 대 한 모든 OneDrive 목록이 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-124">Step 1: Collect a list of all OneDrive for Business sites</span></span>

<span data-ttu-id="28ba9-p106">먼저 조직에서 비즈니스 사이트에 대 한 모든 OneDrive의 목록을 만드는 것입니다. 자세한 내용은 [조직에서 모든 OneDrive 위치 목록을 만들기](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a)를 참조 합니다. 이 문서에서이 스크립트는 모든 OneDrive 사이트의 목록을 포함 하는 텍스트 파일을 만듭니다. 3 단계에서에서 실행 하는 스크립트는이 단계에서 만든 텍스트 파일에 나열 된 비즈니스 사이트에 대 한 각 OneDrive에 사이트 모음 관리자로 지정 된 사용자를 할당 합니다. 다음 텍스트에는이 파일에는 사이트의 목록 서식 지정 방법의 예가 나와 있습니다. 필요한 경우이 파일에서 사이트를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p106">The first step is to create a list of all OneDrive for Business sites in your organization. For instructions, see [Create a list of all OneDrive locations in your organization](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). This script in this article creates a text file that contains a list of all OneDrive sites. The script that you run in Step 3 assigns a specified user as a site collection administrator to each OneDrive for Business site listed in the text file that's created in this step. The following text provides an example of how the list of sites in this file should be formatted. You can remove sites from this file if necessary.</span></span>

```
/personal/annb_contoso_onmicrosoft_com/
/personal/carolt_contoso_onmicrosoft_com/
/personal/esterv_contoso_onmicrosoft_com/
/personal/hollyh_contoso_onmicrosoft_com/
/personal/jeffl_contoso_onmicrosoft_com/
/personal/joeh_contoso_onmicrosoft_com/
/personal/kaia_contoso_onmicrosoft_com/
```

## <a name="step-2-connect-sharepoint-online-management-shell-to-your-organization"></a><span data-ttu-id="28ba9-131">2 단계: SharePoint Online 관리 셸을 조직에 연결</span><span class="sxs-lookup"><span data-stu-id="28ba9-131">Step 2: Connect SharePoint Online Management Shell to your organization</span></span>

1. <span data-ttu-id="28ba9-132">로컬 컴퓨터에서 SharePoint Online 관리 셸을 열고 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-132">On your local computer, open the SharePoint Online Management Shell, and run the following command:</span></span>

    ```
    $credentials = Get-Credential
    ```

2. <span data-ttu-id="28ba9-133">**Windows PowerShell 자격 증명 요청** 대화 상자에서 Office 365 전역 관리자 계정의 사용자 이름 및 암호를 입력한 다음 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-133">In the **Windows PowerShell Credential Request** dialog box, type the user name and password for your Office 365 global administrator account, and then click **OK**.</span></span>
    
3. <span data-ttu-id="28ba9-134">다음 명령을 실행하여 SharePoint Online 조직에 셸을 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-134">Run the following command to connect the Shell to your SharePoint Online organization:</span></span>
    
    ```
    Connect-SPOService -Url https://<your organization name>-admin.sharepoint.com -credential $credentials
    ```
   
4. <span data-ttu-id="28ba9-135">SharePoint Online 조직에 연결되었는지 확인하려면 다음 명령을 실행하여 조직의 모든 사이트 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-135">To verify that you are connected to your SharePoint Online organization, run the following command to get a list of all the sites in your organization:</span></span>
    
    ```
    Get-SPOSite
    ```

## <a name="step-3-assign-a-user-as-a-site-collection-administrator-to-onedrive-for-business-sites"></a><span data-ttu-id="28ba9-136">3단계: 사용자를 비즈니스용 OneDrive 사이트에 사이트 모음 관리자로 할당</span><span class="sxs-lookup"><span data-stu-id="28ba9-136">Step 3: Assign a user as a site collection administrator to OneDrive for Business sites</span></span>

<span data-ttu-id="28ba9-p107">다음 단계에서는 조직에서 비즈니스 사이트에 대 한 모든 OneDrive에서 사이트 모음 관리자로 지정 된 사용자를 할당 하는 스크립트를 실행 하는 것입니다. 이 스크립트는 1 단계에서에서 만든 비즈니스 사이트에 대 한 OneDrive 목록이 사용 합니다. 앞서 설명한 것 처럼 비즈니스 사이트에 대 한 사용자를 사이트 모음 관리자로 OneDrive 할당 하려는 때마다가이 스크립트를 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p107">The next step is to run a script that assigns a specified user as a site collection administrator in every OneDrive for Business site in your organization. This script uses the list of OneDrive for Business sites that you created in Step 1. As previously stated, you have to run this script each time that you want to assign a user as a site collection administrator to OneDrive for Business sites.</span></span>
  
1. <span data-ttu-id="28ba9-p108">다음 텍스트를 텍스트 파일로 저장합니다. 예를 들어 OD4BAssignSCA.txt 파일로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p108">Save the following text to a text file. For example, you could save it to a file named OD4BAssignSCA.txt.</span></span>

    ```
    # Start logging, so if this script fails, you can look at the last successful change,
    # remove any OneDrive for Business paths that worked it from the input file, and then rerun the script.

    Start-Transcript

    # URL for your organization's SPO admin service

    $AdminURI = "https://<your organization name>-admin.sharepoint.com"

    # User account for an Office 365 global admin in your organization

    $AdminAccount = "<global admin account>"

    # Compliance manager to be made site collection admin on each MySite

    $eDiscoveryUser = "<eDiscovery user account>"

    # URL for your tenant's MySite domain

    $MySitePrefix = "https://<your organization name>-my.sharepoint.com"

    # Where should we read the list of MySites?
    # This file should contain partial MySite paths formatted as follows, one per line; for example
    # /personal/junminh_contoso_onmicrosoft_com/

    $MySiteListFile = 'C:\Users\<youralias>\Desktop\ListOfMysites.txt'

    # Begin by connecting to the service
    Connect-SPOService -Url $AdminURI -Credential $AdminAccount

    # Make a reader for our list of MySites

    $reader = [System.IO.File]::OpenText($MySiteListFile)

    try {
      for(;;) {

    # Read a line
          $line = $reader.ReadLine()
    # Stop if it doesn't exist
          if ($line -eq $null) { break }

    # Turn the line into a complete SharePoint site path by merging $MySitePrefix
    # Formatted like this: "https://contoso-my.sharepoint.com"
    # ...with each partial MySite path in the file, formatted like this:
    # "/personal/junminh_contoso_onmicrosoft_com/"

          $fullsitepath = "$MySitePrefix$line"

    Write-Host "Operating on $fullsitepath "

    # We need to remove the last "/" to work around an issue.
    # "/personal/junminh_contoso_onmicrosoft_com/"
    # becomes "/personal/junminh_contoso_onmicrosoft_com"

    $fullsitepath = $fullsitepath.trimend("/")

    # Make the specified eDiscovery user a site collection admin on the OneDrive for Business site
    Write-Host "Making $eDiscoveryUser a Site Collection Admin"
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
      }
    }
    finally {
      $reader.Close()
    }
    Write-Host "Done!"
    Stop-Transcript
    Write-Host "Log written."
    ```

2. <span data-ttu-id="28ba9-p109">스크립트 파일의 시작 부분에서 다음 변수를 편집 하 고 조직에 관련 된 정보를 사용 합니다. 다음 예제에서는 조직의 도메인 이름을 contoso.onmicrosoft.com 형식으로 가정 합니다. 주위에 큰따옴표를 사용 하 여 변수에 대 한 값을 확인 ("").</span><span class="sxs-lookup"><span data-stu-id="28ba9-p109">Edit the following variables in the beginning of the script file, and use information that's specific to your organization. The following examples assume that the domain name of your organization is contoso.onmicrosoft.com. Be sure to surround the values for the variables with double-quotation marks (" ").</span></span>
    
    - <span data-ttu-id="28ba9-145">**$AdminURI** -이 URI를 지정 하면 SharePoint Online 관리 서비스에 대 한 예 `"https://contoso-admin.sharepoint.com"`합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-145">**$AdminURI** - This specifies the URI for your SharePoint Online admin service, for example,  `"https://contoso-admin.sharepoint.com"`.</span></span>
    
    - <span data-ttu-id="28ba9-146">**$AdminAccount** -이 전역 관리자 계정을 지정 Office 365 조직에서 예, `"admin@contoso.onmicrosoft.com"`합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-146">**$AdminAccount** - This specifies a global administrator account in your Office 365 organization, for example,  `"admin@contoso.onmicrosoft.com"`.</span></span>
    
    - <span data-ttu-id="28ba9-147">관리자의 사용자 계정을 지정 **$eDiscoveryUser** -또는 규정 준수 관리자 등 조직 전체에서 비즈니스 사이트에 대 한 모든 OneDrive에 대 한 사이트 모음 관리자로 할당 받을 `"annb@contoso.onmicrosoft.com"`합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-147">**$eDiscoveryUser** - This specifies the user account of an administrator or compliance manager who will be assigned as a site collection administrator for every OneDrive for Business site in your organization, for example,  `"annb@contoso.onmicrosoft.com"`.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="28ba9-148">**$EDiscoveryUser** 변수에 지정 된 사용자 계정을 변경 하 고 다시 **$MySiteListFile** 변수에서 지정 된 비즈니스 사이트에 대 한 OneDrive에 사이트 모음 관리자 권한으로 다른 사용자를 할당 하려면 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-148">Change the user account specified by the **$eDiscoveryUser** variable and re-run the script to assign a different user as a site collection administrator to the OneDrive for Business sites that are specified by the **$MySiteListFile** variable.</span></span> 
  
    - <span data-ttu-id="28ba9-p110">**$MySitePrefix** 이 경우 조직의 내 사이트 도메인에 대 한 URL을 지정 합니다. 이것은 등 조직 전체에서 비즈니스 사이트에 대 한 모든 OneDrive를 포함 하는 도메인 `"https://contoso-my.sharepoint.com"`합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p110">**$MySitePrefix**This specifies the URL for your organization's MySite domain. This is the domain that contains all the OneDrive for Business sites in your organization, for example,  `"https://contoso-my.sharepoint.com"`.</span></span>
    
    - <span data-ttu-id="28ba9-p111">**$MySiteListFile** 1 단계에서에서 만든 텍스트 파일의 전체 경로 지정 합니다. 이 파일의 목록이 표시 OneDrive 조직 전체에서 비즈니스 사이트에 대 한 예 `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`합니다. 단일 따옴표로이 변수에 대 한 값을 묶지 확인 (' '). Note 1 단계에서에서 텍스트 파일을 저장 하는 위치를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p111">**$MySiteListFile**This specifies the full path of the text file that you created in Step 1. This file contains a list of OneDrive for Business sites in your organization, for example,  `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`. Be sure to surround the value for this variable with single-quotation marks (' '). Note that you should specify the location that you saved the text file to in Step 1.</span></span>
    
3. <span data-ttu-id="28ba9-p112">파일 이름 접미사를 .ps1로 변경하여 텍스트 파일을 PowerShell 스크립트 파일로 저장합니다. 예를 들어 OD4BAssignSCA.txt 파일을 OD4BAssignSCA.ps1로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p112">Save the text file as a PowerShell script file by changing the file name suffix to .ps1. For example, save the file OD4BAssignSCA.txt as OD4BAssignSCA.ps1.</span></span>
    
4. <span data-ttu-id="28ba9-157">SharePoint Online 관리 셸에서 이전 단계에서 만든 PowerShell 스크립트가 포함된 폴더로 이동한 다음 스크립트를 실행합니다. 예:</span><span class="sxs-lookup"><span data-stu-id="28ba9-157">In SharePoint Online Management Shell, go to the folder that contains the PowerShell script that you created in the previous step, and then run the script, for example:</span></span>
    
    ```
    .\OD4BAssignSCA.ps1
    ```

    <span data-ttu-id="28ba9-p113">스크립트에 지정 된 관리자 계정의 암호를 입력 하 라는 메시지가 표시 됩니다. 스크립트를 메시지 성공적으로 실행 하는 경우 `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` **$MySiteListFile**하 여 지정한 입력된 파일에 나열 된 비즈니스 사이트에 대 한 각 onedrive 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p113">You will be prompted to enter the password for the administrator account that you specified in the script. If the script runs successfully, the message `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` is displayed for each OneDrive for Business site that's listed in the input file specified by **$MySiteListFile**.</span></span>

## <a name="more-information"></a><span data-ttu-id="28ba9-160">추가 정보</span><span class="sxs-lookup"><span data-stu-id="28ba9-160">More information</span></span>

- <span data-ttu-id="28ba9-p114">3 단계에서에서 실행 되는 스크립트 **Set-spouser** cmdlet를 사용 하 여 **$MySiteListFile** 변수에 지정 된 파일에 나열 된 비즈니스에 대 한 모든 OneDrive에 사이트 모음 관리자로 지정된 된 사용자를 할당 합니다. 다양 한 사용자에 게 매우 큰 조직을 설정한 경우에 할당 eDiscovery 사용 권한 관리를 쉽게 수행할 수 있도록 다음을 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p114">The script that you ran in Step 3 uses the **Set-SPOUser** cmdlet to assign the specified user as a site collection administrator to every OneDrive for Business that's listed in the file specified by the **$MySiteListFile** variable. If you have a very large organization with thousands of users, consider doing the following to make it easier to manage assigning eDiscovery permissions.</span></span> 
    
  - <span data-ttu-id="28ba9-163">사용자가 현재 법적 경우에서 관여에 대 한 사이트에만 포함 되도록 비즈니스 사이트에 대 한 OneDrive 목록이 포함 된 1 단계에서에서 만든 파일을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-163">Edit the file that you created in Step 1 that contains the list of OneDrive for Business sites so that it includes only the sites for users are that are involved in active legal cases.</span></span>
    
  - <span data-ttu-id="28ba9-p115">2, 500 개 이하의 OneDrive 하루 비즈니스 사이트에 대 한 권한을 할당 합니다. 예, 비즈니스 사이트에 대 한 10, 000 OneDrive 조직에 있는 가정해 보겠습니다. 모든 사이트를 수집 하려면 1 단계에서에서 목록을 만들 수 있습니다. 다음 해당 파일을 사용 하 여 2, 500 사용자를 포함 하는 4 개의 파일을 만들 수 있습니다. 첫번째 날에 처음 2, 500 OneDrive 비즈니스 사이트에 대 한 사용 권한을 할당 하려면 3 단계에서에서 스크립트를 실행 합니다. 두 번째 날에 비즈니스 사이트에 대 한 다음 2, 500 onedrive 스크립트를 실행 하는 등입니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p115">Assign permissions to no more than 2,500 OneDrive for Business sites per day. For example, let's say you have 10,000 OneDrive for Business sites in your organization. You could create the list in Step 1 to collect all the sites. Then you could use that file to create four files that each contain 2,500 users. On the first day, you would run the script in Step 3 to assign permissions to the first 2,500 OneDrive for Business sites. On the second day, you would run the script for the next 2,500 OneDrive for Business sites, and so on.</span></span>
    
- <span data-ttu-id="28ba9-p116">EDiscovery 사용 권한 및 사이트 모음 관리자로 할당 된 사용자에 할당 된 비즈니스 사이트에 대 한 OneDrive의 레코드를 유지 합니다. 예, 사용 권한을 할당한 후 비즈니스 사이트에 대 한 OneDrive 목록이 포함 된 텍스트 파일을 저장 하 고 하 여 사이트 모음 관리자로 할당 된 사용자를 식별 하는 줄을 추가 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p116">Keep a record of the OneDrive for Business sites that were assigned eDiscovery permissions and the user who is assigned as the site collection administrator. For example, after you assign permissions, you can save the text file that contains the list of OneDrive for Business sites and add a line to it that identifies the user who is assigned as the site collection administrator.</span></span>
    
- <span data-ttu-id="28ba9-p117">사용자는 자신의 onedrive 비즈니스 사이트에 대 한 사이트 모음 administators 목록이 볼 수 있습니다. 사용자가 자신의 onedrive 비즈니스 사이트에 대 한 사이트 모음 관리자는 이기 때문에 사이트 모음 관리자를 제거할 수 있습니다. EDiscovery 권한을 비즈니스 사이트에 대 한의 OneDrive에 할당 된 사용자를 제거 하는 사용자의 가능성을 완화 하기 위해 다음을 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p117">Users can view the list of site collection administators for their OneDrive for Business site. Because users are site collection administrator for their own OneDrive for Business site, they can remove site collection administrators. Consider doing the following to mitigate the chance of users removing the user who is assigned eDiscovery permissions to OneDrive for Business sites.</span></span>
    
  - <span data-ttu-id="28ba9-175">eDiscovery 및 규정 준수 목적을 위해 규정 준수 관리자가 할당 된 사이트 모음 관리자로 OneDrive 조직에서 비즈니스 사이트에 대 한 사용자에 게 알려야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-175">Communicate to users that for eDiscovery and compliance purposes, a compliance officer has been assigned as a site collection administrator to OneDrive for Business sites in your organization.</span></span>
    
  - <span data-ttu-id="28ba9-176">사이트 모음 관리자로 OneDrive에 대 한 비즈니스 사이트에 대 한 사용자를 다시 할당 하려면 필요한 경우 3 단계에서에서 스크립트를 다시 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-176">Re-run the script in Step 3, if necessary, to re-assign a user as the site collection administrator for OneDrive for Business sites.</span></span>
    
- <span data-ttu-id="28ba9-p118">3 단계에서에서 실행 되는 스크립트를 사용할 수도 있습니다 비즈니스 사이트에 대 한 사이트 모음 관리자로 OneDrive에서 사용자를 제거 해야 합니다. 사이트 모음 관리자 권한으로 사용자를 제거 하려면 (의 끝부분 스크립트)에 다음 명령을에서 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-p118">You can also use the script that you ran in Step 3 to remove a user as the site collection administrator from OneDrive for Business sites. To remove a user as a site collection administrator, you have to change the following command (near the end of the script) from:</span></span> 

    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
    ```

    <span data-ttu-id="28ba9-179">다음으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-179">to:</span></span>
    
    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $false
    ```

    <span data-ttu-id="28ba9-180">스크립트의 다음 행을</span><span class="sxs-lookup"><span data-stu-id="28ba9-180">You can also change the following line in the script from:</span></span>

    ```
    "Making $eDiscoveryUser a Site Collection Admin"
    ```

    <span data-ttu-id="28ba9-181">다음으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-181">to:</span></span>
    
    ```
    "Removing $eDiscoveryUser as a Site Collection Admin"
    ```

    <span data-ttu-id="28ba9-182">이러한 변경을 수행한 후 OD4BRemoveSCA.ps1, 등의 다른 이름으로 스크립트를 저장 하 고를 사용 하 여 사이트 모음 관리자로 비즈니스 사이트에 대 한 OneDrive의 그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba9-182">After you make these changes, save the script with a different name, such as OD4BRemoveSCA.ps1, and then use it to remove a user as a site collection administrator from a group of OneDrive for Business sites.</span></span>
