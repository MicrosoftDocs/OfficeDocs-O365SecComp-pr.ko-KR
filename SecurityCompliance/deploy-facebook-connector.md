---
title: Office 365에서 Facebook 데이터를 보관 하기 위한 커넥터 배포
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
ROBOTS: NOINDEX, NOFOLLOW
description: 관리자는 Facebook Business 페이지를 가져와 Office 365에 보관 하는 기본 커넥터를 설정할 수 있습니다. 이 데이터를 Office 365로 가져온 후 법적 보존, 콘텐츠 검색 및 보존 정책과 같은 규정 준수 기능을 사용 하 여 조직의 Facebook 데이터를 관리할 수 있습니다.
ms.openlocfilehash: b0ec46cea2dd5722633e7fc302cdd0d03cd5d56d
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150560"
---
# <a name="deploy-a-connector-to-archive-facebook-data-in-office-365"></a><span data-ttu-id="f79d7-104">Office 365에서 Facebook 데이터를 보관 하기 위한 커넥터 배포</span><span class="sxs-lookup"><span data-stu-id="f79d7-104">Deploy a connector to archive Facebook data in Office 365</span></span>

<span data-ttu-id="f79d7-105">이 문서에서는 Office 365 가져오기 서비스를 사용 하 여 Facebook Business 페이지의 데이터를 Office 365로 가져오는 커넥터를 배포 하는 단계별 프로세스를 소개 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-105">This article contains the step-by-step process to deploy a connector that uses the Office 365 Import service to import data from Facebook Business pages to Office 365.</span></span> <span data-ttu-id="f79d7-106">이 프로세스에 대 한 간략 한 개요와 Facebook 커넥터를 배포 하는 데 필요한 필수 구성 요소 목록은 [샘플 커넥터를 사용 하 여 Office 365의 facebook 데이터 보관 (미리 보기)](archive-facebook-data-with-sample-connector.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f79d7-106">For a high-level overview of this process and a list of prerequisites required to deploy a Facebook connector, see [Use a sample connector to archive Facebook data in Office 365 (Preview)](archive-facebook-data-with-sample-connector.md).</span></span> 

## <a name="step-1-download-the-package"></a><span data-ttu-id="f79d7-107">1 단계: 패키지 다운로드</span><span class="sxs-lookup"><span data-stu-id="f79d7-107">Step 1: Download the package</span></span>

<span data-ttu-id="f79d7-108">GitHub 리포지토리의 Release (at <https://github.com/Microsoft/m365-sample-connector-csharp-aspnet/releases>) 섹션에서 미리 작성 된 패키지를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-108">Download the prebuilt package from the Release section in the GitHub repository at at <https://github.com/Microsoft/m365-sample-connector-csharp-aspnet/releases>.</span></span> <span data-ttu-id="f79d7-109">최신 버전의 경우 **SampleConnector**라는 zip 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-109">Under the latest release, download the zip file named **SampleConnector.zip**.</span></span> <span data-ttu-id="f79d7-110">4 단계에서이 zip 파일을 Azure에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-110">You will upload this zip file to Azure in Step 4.</span></span>

## <a name="step-2-create-an-app-in-azure-active-directory"></a><span data-ttu-id="f79d7-111">2 단계: Azure Active Directory에 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="f79d7-111">Step 2: Create an app in Azure Active Directory</span></span>

1. <span data-ttu-id="f79d7-112">으로 이동 <https://portal.azure.com> 하 고 Office 365 전역 관리자 계정의 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-112">Go to <https://portal.azure.com> and sign in using the credentials of an Office 365 global admin account.</span></span>

    ![AAD에서 앱 만들기](media/FBCimage1.png)

2. <span data-ttu-id="f79d7-114">왼쪽 탐색 창에서 **Azure Active Directory**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-114">In the left navigation pane, click **Azure Active Directory**.</span></span>

    ![](media/FBCimage2.png)

3. <span data-ttu-id="f79d7-115">왼쪽 탐색 창에서 **앱 등록 (미리 보기)** 을 클릭 하 고 **새 등록**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-115">In the left navigation pane, click **App registrations (Preview)** and then click **New registration**.</span></span>

    ![](media/FBCimage3.png)

4. <span data-ttu-id="f79d7-116">응용 프로그램을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-116">Register the application.</span></span> <span data-ttu-id="f79d7-117">리디렉션 URI의 응용 프로그램 형식 드롭다운 목록에서 웹을 선택한 다음 URI에 <https://portal.azure.com> 대 한 상자에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-117">Under Redirect URI, select Web in the application type dropdown list and then type <https://portal.azure.com> in the box for the URI.</span></span>

   ![](media/FBCimage4.png)

5. <span data-ttu-id="f79d7-118">**응용 프로그램 (클라이언트) id** 및 **디렉터리 (테 넌 트) id** 를 복사한 다음 텍스트 파일 또는 기타 안전한 위치에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-118">Copy the **Application (client) ID** and **Directory (tenant) ID** and save them to a text file or other safe location.</span></span> <span data-ttu-id="f79d7-119">이러한 Id는 이후 단계에서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-119">You’ll use these IDs in later steps.</span></span>

   ![](media/FBCimage5.png)

6. <span data-ttu-id="f79d7-120">**새 앱에 대 한 인증서 & 비밀으로 이동 합니다.**</span><span class="sxs-lookup"><span data-stu-id="f79d7-120">Go to **Certificates & secrets for the new app.**</span></span>

   ![](media/FBCimage6.png)

7. <span data-ttu-id="f79d7-121">**새 클라이언트 암호** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-121">Click **New client secret**</span></span>

   ![](media/FBCimage7.png)

8. <span data-ttu-id="f79d7-122">새 암호를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-122">Create a new secret.</span></span> <span data-ttu-id="f79d7-123">설명 상자에 암호를 입력 하 고 만료 기간을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-123">In the description box, type the secret and then choose an expiration period.</span></span> 

    ![](media/FBCimage8.png)

9. <span data-ttu-id="f79d7-124">비밀 값을 복사 하 여 텍스트 파일 또는 기타 저장 위치에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-124">Copy the value of the secret and save it to a text file or other storage location.</span></span> <span data-ttu-id="f79d7-125">이는 이후 단계에서 사용할 AAD 응용 프로그램 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-125">This is the AAD application secret that you will use in later steps.</span></span>

   ![](media/FBCimage9.png)

10. <span data-ttu-id="f79d7-126">다음 스크린샷에 표시 된 대로 **매니페스트로** 이동 하 여 IDENTIFIERURIS (AAD 응용 프로그램 Uri 라고도 함)를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-126">Go to **Manifest** and copy the identifierUris (which is also called the AAD application Uri) as highlighted in the following screenshot.</span></span> <span data-ttu-id="f79d7-127">AAD 응용 프로그램 Uri를 텍스트 파일 또는 기타 저장 위치에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-127">Copy the AAD application Uri to a text file or other storage location.</span></span> <span data-ttu-id="f79d7-128">6 단계에서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-128">You’ll use it in Step 6.</span></span>

   ![](media/FBCimage10.png)

## <a name="step-3-create-an-azure-storage-account"></a><span data-ttu-id="f79d7-129">3 단계: Azure storage 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="f79d7-129">Step 3: Create an Azure storage account</span></span>

1. <span data-ttu-id="f79d7-130">조직의 Azure 홈 페이지로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-130">Go to the Azure home page for your organization.</span></span>

    ![](media/FBCimage11.png)

2. <span data-ttu-id="f79d7-131">**리소스 만들기** 를 클릭 하 고 검색 상자에 **저장소 계정을** 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-131">Click **Create a resource** and they type **storage account** in the search box.</span></span>

    ![](media/FBCimage12.png)

3. <span data-ttu-id="f79d7-132">**저장소**를 클릭 한 다음 **저장소 계정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-132">Click **Storage**, and then click **Storage account**.</span></span>

    ![](media/FBCimage13.png)

4. <span data-ttu-id="f79d7-133">**저장소 계정 만들기** 페이지의 구독 상자에서 사용 중인 Azure 구독 유형에 따라 **유료** 또는 **무료 평가판** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-133">On the **Create storage account** page, in the Subscription box, select **Pay-As-You-Go** or **Free Trial** depending on which type of Azure subscription you have.</span></span> <span data-ttu-id="f79d7-134">그런 다음 리소스 그룹을 선택 하거나 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-134">Then select or create a resource group.</span></span>

    ![](media/FBCimage14.png)

5. <span data-ttu-id="f79d7-135">저장소 계정의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-135">Type a name for the storage account.</span></span>

    ![](media/FBCimage15.png)

6. <span data-ttu-id="f79d7-136">검토 한 다음 **만들기** 를 클릭 하 여 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-136">Review and then click **Create** to create the storage account.</span></span>

    ![](media/FBCimage16.png)

7. <span data-ttu-id="f79d7-137">잠시 후 **새로 고침** 을 클릭 하 고 **리소스로 이동을** 클릭 하 여 저장소 계정으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-137">After a few moments, click **Refresh** and then click **Go to resource** to navigate to the storage account.</span></span>

    ![](media/FBCimage17.png)

8. <span data-ttu-id="f79d7-138">왼쪽 탐색 창에서 **Access 키** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-138">Click **Access keys** in the left navigation pane.</span></span>

    ![](media/FBCimage18.png)

9. <span data-ttu-id="f79d7-139">**연결 문자열** 을 복사 하 여 텍스트 파일 또는 기타 저장 위치에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-139">Copy a **Connection string** and save it to a text file or other storage location.</span></span> <span data-ttu-id="f79d7-140">이를 사용 하 여 웹 앱 리소스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-140">You’ll use this when creating a web app resource.</span></span>

    ![](media/FBCimage19.png)

## <a name="step-4-create-a-new-web-app-resource-in-azure"></a><span data-ttu-id="f79d7-141">4 단계: Azure에서 새 웹 앱 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="f79d7-141">Step 4: Create a new web app resource in Azure</span></span>

1. <span data-ttu-id="f79d7-142">Azure portal의 **홈** 페이지에서 **모든 \> \> 리소스 만들기 웹 앱**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-142">On the **Home** page in the Azure portal, click **Create a resource \> Everything \> Web app**.</span></span> <span data-ttu-id="f79d7-143">**웹 앱** 페이지에서 **만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-143">On the **Web app** page, click **Create**.</span></span> 

   ![](media/FBCimage20.png)

2. <span data-ttu-id="f79d7-144">아래와 같이 세부 정보를 입력 하 고 웹 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-144">Fill in the details (as shown below) and then create the Web app.</span></span> <span data-ttu-id="f79d7-145">**앱 이름** 상자에 입력 하는 이름은 Azure 앱 서비스 URL을 만드는 데 사용 됩니다. 예: fbconnector.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="f79d7-145">Note that the name that you enter in the **App name** box will be used to create the Azure app service URL; for example fbconnector.azurewebsites.net.</span></span>

   ![](media/FBCimage21.png)

3. <span data-ttu-id="f79d7-146">새로 만든 웹 앱 리소스로 이동 하 여 왼쪽 탐색 창에서 **응용 프로그램 설정을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-146">Go to the newly created web app resource, click **Application Settings** in the left navigation pane.</span></span> <span data-ttu-id="f79d7-147">응용 프로그램 설정에서 새 설정 추가를 클릭 하 고 다음 세 가지 설정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-147">Under Application settings, click Add new setting and add the following three settings.</span></span> <span data-ttu-id="f79d7-148">이전 단계의 텍스트 파일에 복사한 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-148">Use the values (that you copied to the text file from the previous steps):</span></span> 

    - <span data-ttu-id="f79d7-149">**APISecretKey** – 임의의 값을 비밀로 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-149">**APISecretKey** – You can type any value as the secret.</span></span> <span data-ttu-id="f79d7-150">이는 7 단계에서 커넥터 웹 앱에 액세스 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-150">This will be used to access the connector web app in Step 7.</span></span>

    - <span data-ttu-id="f79d7-151">**Storageaccountconnectionstring** -3 단계에서 Azure storage 계정을 만든 후 복사한 연결 문자열 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-151">**StorageAccountConnectionString** – The connection string Uri that you copied after creating the Azure storage account in Step 3.</span></span>

    - <span data-ttu-id="f79d7-152">**tenantId** -2 단계에서 Azure Active Directory에 Facebook 커넥터 앱을 만든 후 복사한 Office 365 조직의 테 넌 트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-152">**tenantId** – The tenant ID of your Office 365 organization that you copied after creating the Facebook connector app in Azure Active Directory in Step 2.</span></span>

    ![](media/FBCimage22.png)

4. <span data-ttu-id="f79d7-153">**일반 설정**에서 Always ( \*\*\*\* **켜기**) 옆의을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-153">Under **General settings**, click **On** next to the **Always On**.</span></span> <span data-ttu-id="f79d7-154">페이지 맨 위에 있는 **저장** 을 클릭 하 여 응용 프로그램 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-154">Click **Save** at the top of the page to save application settings.</span></span>

   ![](media/FBCimage23.png)

5. <span data-ttu-id="f79d7-155">마지막 단계에서는 1 단계에서 다운로드 한 Azure에 커넥터 응용 프로그램 소스 코드를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-155">The final step is to upload the connector app source code to Azure that you downloaded in Step 1.</span></span> <span data-ttu-id="f79d7-156">웹 브라우저에서 scm.azurewebsites.net/ZipDeployUi로 이동 합니다.<AzureAppResourceName>https://.</span><span class="sxs-lookup"><span data-stu-id="f79d7-156">In a web browser, go to https://<AzureAppResourceName>.scm.azurewebsites.net/ZipDeployUi.</span></span> <span data-ttu-id="f79d7-157">예를 들어이 섹션의 2 단계에서 이름이 지정 된 Azure 앱 리소스의 이름이 **fbconnector**인 경우로 https://fbconnector.scm.azurewebsites.net/ZipDeployUi이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-157">For example, if the name of your Azure app resource (which you named in step 2 in this section) is **fbconnector**, then you would go to https://fbconnector.scm.azurewebsites.net/ZipDeployUi.</span></span> 

6. <span data-ttu-id="f79d7-158">1 단계에서 다운로드 한 SampleConnector을이 페이지로 끌어서 놓습니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-158">Drag and drop the SampleConnector.zip (that you downloaded in Step 1) to this page.</span></span> <span data-ttu-id="f79d7-159">파일이 업로드 되 고 배포가 성공 하면 페이지는 다음 스크린샷과 유사 하 게 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-159">After the files are uploaded and the deployment is successful, the page will look similar to the following screenshot.</span></span>

   ![](media/FBCimage24.png)

## <a name="step-5-register-the-facebook-app"></a><span data-ttu-id="f79d7-160">5 단계: Facebook 앱 등록</span><span class="sxs-lookup"><span data-stu-id="f79d7-160">Step 5: Register the Facebook app</span></span>

1. <span data-ttu-id="f79d7-161"><https://developers.facebook.com> 으로 이동 하 고 조직의 Facebook Business 페이지의 계정에 대 한 자격 증명을 사용 하 여 로그인 한 다음 **새 앱 추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-161">Go to <https://developers.facebook.com> , log in using the credentials for the account for your organization’s Facebook Business pages, and then click **Add New App**.</span></span>

   ![](media/FBCimage25.png)

2. <span data-ttu-id="f79d7-162">새 앱 ID를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-162">Create a new app ID.</span></span>

   ![](media/FBCimage26.png)

3. <span data-ttu-id="f79d7-163">왼쪽 탐색 창에서 **제품 추가** 를 클릭 한 다음 **Facebook 로그인** 타일에서 **설정을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-163">In the left navigation pane, click **Add Products** and then click **Set Up** in the **Facebook Login** tile.</span></span>

   ![](media/FBCimage27.png)

4. <span data-ttu-id="f79d7-164">Facebook 로그온 페이지에서 **웹**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-164">On the Integrate Facebook Login page, click **Web**.</span></span>

   ![](media/FBCimage28.png)

5. <span data-ttu-id="f79d7-165">Azure 앱 서비스 URL을 추가 합니다. 예를 https://fbconnector.azurewebsites.net들어</span><span class="sxs-lookup"><span data-stu-id="f79d7-165">Add the Azure app service URL; for example https://fbconnector.azurewebsites.net.</span></span>

   ![](media/FBCimage29.png)

6. <span data-ttu-id="f79d7-166">Facebook 로그인 설정의 퀵 스타트 섹션을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-166">Complete the QuickStart section of the Facebook Login setup.</span></span>

   ![](media/FBCimage30.png)

7. <span data-ttu-id="f79d7-167">**Facebook 로그인**아래의 왼쪽 탐색 창에서 **설정을**클릭 하 고 **유효한 OAuth 리디렉션 URI** 상자에 OAuth 리디렉션 URI를 추가 합니다. connectorserviceuri에 대 한 값이 조직의 Azure app 서비스 URL 인 \*\* \<connectorserviceuri>/Views/FacebookOAuth\*\*형식을 사용 합니다. 예를 https://fbconnector.azurewebsites.net들어</span><span class="sxs-lookup"><span data-stu-id="f79d7-167">In the left navigation pane under **Facebook Login**, click **Settings**, and add the OAuth redirect URI in the **Valid OAuth Redirect URIs** box; use the format **\<connectorserviceuri>/Views/FacebookOAuth**, where the value for connectorserviceuri is the Azure app service URL for your organization; for example https://fbconnector.azurewebsites.net.</span></span>

   ![](media/FBCimage31.png)

8. <span data-ttu-id="f79d7-168">왼쪽 탐색 창에서 **제품 추가** 를 클릭 한 다음 **webhooks를 클릭 합니다.**</span><span class="sxs-lookup"><span data-stu-id="f79d7-168">In the left navigation pane, click **Add Products** and then click **Webhooks.**</span></span> <span data-ttu-id="f79d7-169">**페이지** 풀 다운 메뉴에서 **페이지**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-169">In the **Page** pull-down menu, click **Page**.</span></span> 

   ![](media/FBCimage32.png)

9. <span data-ttu-id="f79d7-170">Webhooks 콜백 URL을 추가 하 고 verify token을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-170">Add Webhooks Callback URL and add a verify token.</span></span> <span data-ttu-id="f79d7-171">콜백 URL의 형식은 \*\* <connectorserviceuri>/api/FbPageWebhook\*\*형식을 사용 하며, 여기서 connectorserviceuri의 값은 조직의 Azure 앱 서비스 URL입니다. 예를 https://fbconnector.azurewebsites.net들어</span><span class="sxs-lookup"><span data-stu-id="f79d7-171">The format of the callback URL, use the format **<connectorserviceuri>/api/FbPageWebhook**, where the value for connectorserviceuri is the Azure app service URL for your organization; for example https://fbconnector.azurewebsites.net.</span></span> 

    <span data-ttu-id="f79d7-172">Verify 토큰은 강력한 암호와 비슷해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-172">The verify token should similar to a strong password.</span></span> <span data-ttu-id="f79d7-173">텍스트 파일 또는 기타 저장소 위치에 verify 토큰을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-173">Copy the verify token to a text file or other storage location.</span></span>

     ![](media/FBCimage33.png)

10. <span data-ttu-id="f79d7-174">테스트 하 고 피드의 끝점을 구독 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-174">Test and subscribe to the endpoint for feed.</span></span>

    ![](media/FBCimage34.png)

11. <span data-ttu-id="f79d7-175">개인 정보 URL, 앱 아이콘 및 비즈니스 사용을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-175">Add a privacy URL, app icon, and business use.</span></span> <span data-ttu-id="f79d7-176">또한 앱 ID 및 앱 암호를 텍스트 파일 또는 기타 저장 위치에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-176">Also, copy the app ID and app secret to a text file or other storage location.</span></span>

    ![](media/FBCimage35.png)

12. <span data-ttu-id="f79d7-177">앱을 공용으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-177">Make the app public.</span></span>

    ![](media/FBCimage36.png)

13. <span data-ttu-id="f79d7-178">관리자 또는 테스터 역할에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-178">Add user to the admin or tester role.</span></span>

    ![](media/FBCimage37.png)

14. <span data-ttu-id="f79d7-179">**페이지 공용 콘텐츠 액세스** 권한을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-179">Add the **Page Public Content Access** permission.</span></span>

    ![](media/FBCimage38.png)

15. <span data-ttu-id="f79d7-180">페이지 관리 권한을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-180">Add Manage Pages permission.</span></span>

    ![](media/FBCimage39.png)

16. <span data-ttu-id="f79d7-181">Facebook에서 검토 한 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-181">Get the application reviewed by Facebook.</span></span>

    ![](media/FBCimage40.png)

## <a name="step-6-configure-the-connector-web-app"></a><span data-ttu-id="f79d7-182">6 단계: 커넥터 웹 응용 프로그램 구성</span><span class="sxs-lookup"><span data-stu-id="f79d7-182">Step 6: Configure the connector web app</span></span>

1. <span data-ttu-id="f79d7-183">Https://\<AzureAppResourceName> (여기서 AzureAppResourceName은 4 단계에서 이름이 지정 된 Azure 앱 리소스의 이름)으로 이동 합니다 (예: 이름이 **fbconnector**이면로 https://fbconnector.azurewebsites.net이동).</span><span class="sxs-lookup"><span data-stu-id="f79d7-183">Go to https://\<AzureAppResourceName>.azurewebsites.net (where AzureAppResourceName is the name of your Azure app resource that you named in Step 4) For example, if the name is **fbconnector**, go to https://fbconnector.azurewebsites.net.</span></span> <span data-ttu-id="f79d7-184">앱의 홈 페이지는 다음 스크린샷 처럼 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-184">The home page of the app will look like the following screenshot.</span></span>


   ![](media/FBCimage41.png)

2. <span data-ttu-id="f79d7-185">**구성을** 클릭 하 여 로그인 페이지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-185">Click **Configure** to display a sign in page.</span></span>
 
   ![](media/FBCimage42.png)

3. <span data-ttu-id="f79d7-186">테 넌 트 Id 상자에 2 단계에서 받은 테 넌 트 Id를 입력 하거나 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-186">In the Tenant Id box, type or paste your tenant Id (that you obtained in Step 2).</span></span> <span data-ttu-id="f79d7-187">암호 상자에 2 단계에서 구한 APISecretKey를 입력 하거나 붙여 넣은 다음 **구성 설정 설정을** 클릭 하 여 **구성 세부 정보** 페이지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-187">In the password box, type or paste the APISecretKey (that you obtained in Step 2), and then click **Set Configuration Settings** to display the **Configuration Details** page.</span></span>

    ![](media/FBCimage43.png)


4. <span data-ttu-id="f79d7-188">**구성 세부 정보**에서 다음 구성 설정을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-188">Under **Configuration Details**, enter the following configuration settings</span></span> 

   - <span data-ttu-id="f79d7-189">**Facebook 응용 프로그램 id** -5 단계에서 가져온 facebook 응용 프로그램의 앱 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-189">**Facebook application ID** - The app ID for the Facebook application that you obtained in Step 5.</span></span>
   - <span data-ttu-id="f79d7-190">**Facebook 응용 프로그램 비밀** -5 단계에서 얻은 facebook 응용 프로그램에 대 한 앱 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-190">**Facebook application secret** - The app secret for the Facebook application that you obtained in Step 5.</span></span>
   - <span data-ttu-id="f79d7-191">**Facebook webhook 확인 토큰** -5 단계에서 만든 verify 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-191">**Facebook webhooks verify token** - The verify token that you created in Step 5.</span></span>
   - <span data-ttu-id="f79d7-192">**AAD 응용 프로그램 id** -2 단계에서 만든 Azure Active Directory 앱의 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-192">**AAD application ID** - The application ID for the Azure Active Directory app that you created in Step 2.</span></span>
   - <span data-ttu-id="f79d7-193">**AAD 응용 프로그램 비밀** -4 단계에서 만든 APISecretKey 암호의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-193">**AAD application secret** - The value for the APISecretKey secret that you created in Step 4.</span></span>
   - <span data-ttu-id="f79d7-194">**Aad 응용 프로그램 uri** -2 단계에서 가져온 aad 응용 프로그램 uri 예를 https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213들면입니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-194">**AAD application Uri** - The AAD application Uri obtained in Step 2; for example, https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213.</span></span>
   - <span data-ttu-id="f79d7-195">**App insights instrumentation 키** -이 상자를 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-195">**App insights instrumentation key** - Leave this box blank.</span></span>

5. <span data-ttu-id="f79d7-196">**저장** 을 클릭 하 여 커넥터 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-196">Click **Save** to save the connector settings.</span></span>

## <a name="step-7-set-up-a-custom-connector-in-the-security--compliance-center"></a><span data-ttu-id="f79d7-197">7 단계: 보안 & 준수 센터에서 사용자 지정 커넥터 설정</span><span class="sxs-lookup"><span data-stu-id="f79d7-197">Step 7: Set up a custom connector in the Security & Compliance Center</span></span>

1. <span data-ttu-id="f79d7-198">로 이동한 <https://protection.office.com> 후 **데이터 거 버 넌 \> 스 \> 가져오기 보관 타사 데이터**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-198">Go to <https://protection.office.com> and then click **Data governance \> Import \> Archive third-party data**.</span></span>

   ![](media/FBCimage44.png)

2.  <span data-ttu-id="f79d7-199">**커넥터 추가** 를 클릭 한 다음 **Facebook 페이지**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-199">Click **Add a connector** and then click **Facebook pages**.</span></span>

    ![](media/FBCimage46.png)

3.  <span data-ttu-id="f79d7-200">**커넥터 앱 추가** 페이지에서 다음 정보를 입력 하 고 **커넥터 유효성 검사**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-200">On the **Add Connector App** page, enter the following information and then click **Validate connector**.</span></span>

    - <span data-ttu-id="f79d7-201">첫 번째 상자에 **Facebook**과 같은 커넥터의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-201">In the first box, type a name for the connector, such as **Facebook**.</span></span>
    - <span data-ttu-id="f79d7-202">두 번째 상자에 4 단계에서 추가한 APISecretKey의 값을 입력 하거나 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-202">In the second box, type or paste the value of the APISecretKey that you added in Step 4.</span></span>
    - <span data-ttu-id="f79d7-203">세 번째 상자에 Azure 앱 서비스 URL을 입력 하거나 붙여넣습니다. 예를 **https://fbconnector.azurewebsites.net**들어</span><span class="sxs-lookup"><span data-stu-id="f79d7-203">In the third box, type or paste the Azure app service URL; for example **https://fbconnector.azurewebsites.net**.</span></span>
 
    <span data-ttu-id="f79d7-204">커넥터 유효성 검사가 완료 되 면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-204">After the connector is successfully validated, click **Next**.</span></span>
    
    ![](media/FBCimage47.png)

4.  <span data-ttu-id="f79d7-205">**커넥터 앱을 사용 하 여 로그인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-205">Click **Login with Connector App**.</span></span>

    ![](media/FBCimage45.png)

5. <span data-ttu-id="f79d7-206">APISecretKey를 다시 입력 하거나 붙여 넣은 다음 **커넥터 서비스에 로그인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-206">Type or paste the APISecretKey again and then click  **Login to Connector Service**.</span></span>

   ![](media/FBCimage48.png)


6. <span data-ttu-id="f79d7-207">**Facebook을 사용 하 여 로그인을 클릭 합니다.**</span><span class="sxs-lookup"><span data-stu-id="f79d7-207">Click **Login with Facebook.**</span></span>

   ![](media/FBCimage49.png)

7. <span data-ttu-id="f79d7-208">**Facebook에 로그인** 페이지에서 조직의 Facebook Business 페이지에 대 한 계정의 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-208">On the **Log in to Facebook** page, log in using the credentials for the account for your organization’s Facebook Business pages.</span></span> <span data-ttu-id="f79d7-209">로그인 한 Facebook 계정에 조직의 Facebook Business 페이지에 대 한 관리자 역할이 할당 되었는지 확인</span><span class="sxs-lookup"><span data-stu-id="f79d7-209">Make sure the Facebook account you logged in to is assigned the admin role for your organization’s Facebook Business pages</span></span>

   ![](media/FBCimage50.png)

8. <span data-ttu-id="f79d7-210">**페이지 선택을** 클릭 하 여 Office 365에서 보관 하려는 조직의 비즈니스 페이지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-210">Click **Select Pages** to choose your organization’s business pages that you want to archive in Office 365.</span></span>

   ![](media/FBCimage51.png)

9. <span data-ttu-id="f79d7-211">로그인 한 Facebook 계정으로 관리 되는 비즈니스 페이지 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-211">A list of the Business pages managed by the Facebook account that you logged in to is displayed.</span></span> <span data-ttu-id="f79d7-212">보관할 페이지를 선택 하 고 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-212">Select the page to archive and then click **Save**.</span></span>

    ![](media/FBCimage52.png)

10. <span data-ttu-id="f79d7-213">**마침** 을 클릭 하 여 커넥터 서비스 앱의 설정을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-213">Click **Finish** to exit the setup of the connector service app.</span></span>

    ![](media/FBCimage53.png)

11. <span data-ttu-id="f79d7-214">**필터 설정** 페이지에서 특정 연령 인 항목을 가져오고 보관 하는 필터를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-214">On the **Set Filters** page, you can apply a filter to import (and archive) items that are a certain age.</span></span> <span data-ttu-id="f79d7-215">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-215">Click **Next**.</span></span>

    ![](media/FBCimage54.png)

12. <span data-ttu-id="f79d7-216">**저장소 계정 설정** 페이지에서 이전에 선택한 Facebook 비즈니스 페이지의 항목을 가져올 Office 365 사서함을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-216">On the **Set Storage Account** page, select the Office 365 mailbox that the items from the Facebook Business pages that you previously selected will be imported to.</span></span>

    ![](media/FBCimage55.png)

13. <span data-ttu-id="f79d7-217">설정을 검토 하 고 **마침을** 클릭 하 여 Security _AMP_ 준수 센터에서 커넥터 설정을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-217">Review your settings and then click **Finish** to complete the connector setup in the Security & Compliance Center.</span></span>

    ![](media/FBCimage56.png)

14. <span data-ttu-id="f79d7-218">**타사 데이터 보관** 페이지로 이동 하 여 가져오기 프로세스의 진행 상황을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79d7-218">Go to the **Archive third-party data** page to see the progress of the import process.</span></span>

    ![](media/FBCimage58.png)
