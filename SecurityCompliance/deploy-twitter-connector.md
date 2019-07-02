---
title: Office 365에서 Twitter 데이터를 보관 하기 위한 커넥터 배포
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
description: 관리자는 Twitter 데이터를 가져와 Office 365에 보관 하는 기본 커넥터를 설정할 수 있습니다. 이 데이터를 Office 365로 가져온 후 법적 보존, 콘텐츠 검색 및 보존 정책과 같은 규정 준수 기능을 사용 하 여 조직의 Twitter 데이터에 대 한 관리를 관리할 수 있습니다.
ms.openlocfilehash: c3c5af0fc42057d9fc2e8b8e67423398d6ed0ddf
ms.sourcegitcommit: f2798d46acfbd56314e809cd3fe0350be807e420
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/17/2019
ms.locfileid: "35014777"
---
# <a name="deploy-a-connector-to-archive-twitter-data-in-office-365"></a><span data-ttu-id="ebc68-104">Office 365에서 Twitter 데이터를 보관 하기 위한 커넥터 배포</span><span class="sxs-lookup"><span data-stu-id="ebc68-104">Deploy a connector to archive Twitter data in Office 365</span></span>

<span data-ttu-id="ebc68-105">이 문서에는 Office 365 가져오기 서비스를 사용 하 여 조직의 Twitter 계정에서 Office 365로 데이터를 가져오는 커넥터를 배포 하는 단계별 프로세스가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-105">This article contains the step-by-step process to deploy a connector that uses the Office 365 Import service to import data from your organization's Twitter account to Office 365.</span></span> <span data-ttu-id="ebc68-106">이 프로세스에 대 한 간략 한 개요와 Twitter 커넥터를 배포 하는 데 필요한 필수 구성 요소 목록은 [예제 커넥터를 사용 하 여 Office 365 (미리 보기)에서 twitter 데이터를 보관](archive-twitter-data-with-sample-connector.md)합니다 .를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ebc68-106">For a high-level overview of this process and a list of prerequisites required to deploy a Twitter connector, see [Use a sample connector to archive Twitter data in Office 365 (Preview)](archive-twitter-data-with-sample-connector.md).</span></span> 

## <a name="step-1-download-the-package"></a><span data-ttu-id="ebc68-107">1 단계: 패키지 다운로드</span><span class="sxs-lookup"><span data-stu-id="ebc68-107">Step 1: Download the package</span></span>

<span data-ttu-id="ebc68-108">GitHub 리포지토리의 릴리스 섹션에서 미리 작성 된 패키지를 다운로드 [https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases)합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-108">Download the prebuilt package from the Release section in the GitHub repository at [https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases).</span></span> <span data-ttu-id="ebc68-109">최신 버전의 경우 **SampleConnector**라는 zip 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-109">Under the latest release, download the zip file named **SampleConnector.zip**.</span></span> <span data-ttu-id="ebc68-110">4 단계에서이 zip 파일을 Azure에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-110">You upload this zip file to Azure in Step 4.</span></span>

## <a name="step-2-create-an-app-in-azure-active-directory"></a><span data-ttu-id="ebc68-111">2 단계: Azure Active Directory에 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="ebc68-111">Step 2: Create an app in Azure Active Directory</span></span>

1. <span data-ttu-id="ebc68-112">으로 이동 <https://portal.azure.com> 하 고 Office 365 전역 관리자 계정의 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-112">Go to <https://portal.azure.com> and sign in using the credentials of an Office 365 global admin account.</span></span>

   ![](media/TCimage01.png)

2. <span data-ttu-id="ebc68-113">왼쪽 탐색 창에서 **Azure Active Directory**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-113">In the left navigation pane, click **Azure Active Directory**.</span></span>

   ![](media/TCimage02.png)

3. <span data-ttu-id="ebc68-114">왼쪽 탐색 창에서 **앱 등록 (미리 보기)** 을 클릭 하 고 **새 등록**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-114">In the left navigation pane, click **App registrations (Preview)** and then click **New registration**.</span></span>

   ![](media/TCimage03.png)

4. <span data-ttu-id="ebc68-115">응용 프로그램을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-115">Register the application.</span></span> <span data-ttu-id="ebc68-116">**Uri 리디렉션 (선택 사항)** 아래의 응용 프로그램 형식 드롭다운 목록에서 웹을 선택한 다음 URI <https://portal.azure.com> 에 대 한 상자에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-116">Under **Redirect URI (optional)**, select Web in the application type dropdown list and then type <https://portal.azure.com> in the box for the URI.</span></span>

   ![](media/TCimage04.png)

5. <span data-ttu-id="ebc68-117">**응용 프로그램 (클라이언트) id** 및 **디렉터리 (테 넌 트) id** 를 복사한 다음 텍스트 파일 또는 기타 안전한 위치에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-117">Copy the **Application (client) ID** and **Directory (tenant) ID** and save them to a text file or other safe location.</span></span> <span data-ttu-id="ebc68-118">이후 단계에서 이러한 Id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-118">You use these IDs in later steps.</span></span>

    ![](media/TCimage05.png)

6. <span data-ttu-id="ebc68-119">**새 앱에 대 한 인증서 & 비밀** 으로 이동 하 고 **클라이언트 암호** 에서 **새 클라이언트 암호**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-119">Go to **Certificates & secrets for the new app** and under **Client secrets** click **New client secret**.</span></span>

   ![](media/TCimage06.png)

7. <span data-ttu-id="ebc68-120">새 암호를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-120">Create a new secret.</span></span> <span data-ttu-id="ebc68-121">설명 상자에 암호를 입력 하 고 만료 기간을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-121">In the description box, type the secret and then choose an expiration period.</span></span> 

   ![](media/TCimage08.png)

8. <span data-ttu-id="ebc68-122">비밀 값을 복사 하 여 텍스트 파일 또는 기타 저장 위치에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-122">Copy the value of the secret and save it to a text file or other storage location.</span></span> <span data-ttu-id="ebc68-123">이는 이후 단계에서 사용 하는 AAD 응용 프로그램 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-123">This is the AAD application secret that you use in later steps.</span></span>

   ![](media/TCimage09.png)

9. <span data-ttu-id="ebc68-124">다음 스크린샷에 표시 된 대로 **매니페스트로** 이동 하 여 IDENTIFIERURIS (AAD 응용 프로그램 Uri 라고도 함)를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-124">Go to **Manifest** and copy the identifierUris (which is also called the AAD application Uri) as highlighted in the following screenshot.</span></span> <span data-ttu-id="ebc68-125">AAD 응용 프로그램 Uri를 텍스트 파일 또는 기타 저장 위치에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-125">Copy the AAD application Uri to a text file or other storage location.</span></span> <span data-ttu-id="ebc68-126">6 단계에서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-126">You use it in Step 6.</span></span>

    ![](media/TCimage10.png)

## <a name="step-3-create-an-azure-storage-account"></a><span data-ttu-id="ebc68-127">3 단계: Azure storage 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="ebc68-127">Step 3: Create an Azure storage account</span></span>

1.  <span data-ttu-id="ebc68-128">조직의 Azure 홈 페이지로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-128">Go to the Azure home page for your organization.</span></span>

    ![](media/TCimage11.png)

2. <span data-ttu-id="ebc68-129">**리소스 만들기** 를 클릭 하 고 검색 상자에 **저장소 계정을** 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-129">Click **Create a resource** and they type **storage account** in the search box.</span></span>

   ![](media/TCimage12.png)

3. <span data-ttu-id="ebc68-130">**저장소**를 클릭 한 다음 **저장소 계정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-130">Click **Storage**, and then click **Storage account**.</span></span>

   ![](media/TCimage13.png)

4. <span data-ttu-id="ebc68-131">**저장소 계정 만들기** 페이지의 구독 상자에서 사용 중인 Azure 구독 유형에 따라 **유료** 또는 **무료 평가판** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-131">On the **Create storage account** page, in the Subscription box, select **Pay-As-You-Go** or **Free Trial** depending on which type of Azure subscription you have.</span></span> 

   ![](media/TCimage14.png)

5. <span data-ttu-id="ebc68-132">리소스 그룹을 선택 하거나 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-132">Select or create a resource group.</span></span>

   ![](media/TCimage15.png)

6. <span data-ttu-id="ebc68-133">저장소 계정의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-133">Type a name for the storage account.</span></span>

   ![](media/TCimage16.png)

7. <span data-ttu-id="ebc68-134">검토 한 다음 **만들기** 를 클릭 하 여 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-134">Review and then click **Create** to create the storage account.</span></span>

   ![](media/TCimage17.png)

8. <span data-ttu-id="ebc68-135">잠시 후 **새로 고침** 을 클릭 하 고 **리소스로 이동을** 클릭 하 여 저장소 계정으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-135">After a few moments, click **Refresh** and then click **Go to resource** to navigate to the storage account.</span></span>

   ![](media/TCimage18.png)

9. <span data-ttu-id="ebc68-136">왼쪽 탐색 창에서 **Access 키** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-136">Click **Access keys** in the left navigation pane.</span></span>

   ![](media/TCimage19.png)

10. <span data-ttu-id="ebc68-137">**연결 문자열** 을 복사 하 여 텍스트 파일 또는 기타 저장 위치에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-137">Copy a **Connection string** and save it to a text file or other storage location.</span></span> <span data-ttu-id="ebc68-138">4 단계에서 웹 앱 리소스를 만들 때이 방법을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-138">You use this when creating a web app resource in Step 4.</span></span>

    ![](media/TCimage20.png)

## <a name="step-4-create-a-new-web-app-resource-in-azure"></a><span data-ttu-id="ebc68-139">4 단계: Azure에서 새 웹 앱 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="ebc68-139">Step 4: Create a new web app resource in Azure</span></span>

1. <span data-ttu-id="ebc68-140">Azure portal의 **홈** 페이지에서 **모든 \> \> 리소스 만들기 웹 앱**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-140">On the **Home** page in the Azure portal, click **Create a resource \> Everything \> Web app**.</span></span> <span data-ttu-id="ebc68-141">**웹 앱** 페이지에서 **만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-141">On the **Web app** page, click **Create**.</span></span>

   ![](media/TCimage21.png)

2. <span data-ttu-id="ebc68-142">아래와 같이 세부 정보를 입력 하 고 웹 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-142">Fill in the details (as shown below) and then create the Web app.</span></span> <span data-ttu-id="ebc68-143">**앱 이름** 상자에 입력 한 이름은 Azure 앱 서비스 URL을 만드는 데 사용 됩니다. 예: twitterconnector.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="ebc68-143">The name that you enter in the **App name** box is used to create the Azure app service URL; for example, twitterconnector.azurewebsites.net.</span></span>

   ![](media/TCimage22.png)

3. <span data-ttu-id="ebc68-144">새로 만든 웹 앱 리소스로 이동 하 여 왼쪽 탐색 창에서 **응용 프로그램 설정을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-144">Go to the newly created web app resource and click **Application Settings** in the left navigation pane.</span></span> <span data-ttu-id="ebc68-145">**응용 프로그램 설정**에서 **새 설정 추가** 를 클릭 하 고 다음 세 가지 설정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-145">Under **Application settings**, click **Add new setting** and add the following three settings.</span></span> <span data-ttu-id="ebc68-146">이전 단계의 텍스트 파일에 복사한 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-146">Use the values (that you copied to the text file from the previous steps):</span></span> 

    <span data-ttu-id="ebc68-147">-\* \* APISecretKey-모든 값을 비밀로 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-147">– \*\*APISecretKey — You can type any value as the secret.</span></span> <span data-ttu-id="ebc68-148">이는 7 단계에서 커넥터 웹 앱에 액세스 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-148">This is used to access the connector web app in Step 7.</span></span>

    <span data-ttu-id="ebc68-149">- **Storageaccountconnectionstring** -3 단계에서 Azure storage 계정을 만든 후 복사한 연결 문자열 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-149">– **StorageAccountConnectionString** – The connection string Uri that you copied after creating the Azure storage account in Step 3.</span></span>

    <span data-ttu-id="ebc68-150">- **tenantId** -2 단계에서 Azure Active Directory에 Twitter 커넥터 앱을 만든 후 복사한 Office 365 조직의 테 넌 트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-150">– **tenantId** – The tenant ID of your Office 365 organization that you copied after creating the Twitter connector app in Azure Active Directory in Step 2.</span></span>

    ![](media/TCimage23.png)

4. <span data-ttu-id="ebc68-151">**일반 설정**에서 Always ( \*\*\*\* **켜기**) 옆의을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-151">Under **General settings**, click **On** next to the **Always On**.</span></span> <span data-ttu-id="ebc68-152">페이지 맨 위에 있는 **저장** 을 클릭 하 여 응용 프로그램 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-152">Click **Save** at the top of the page to save the application settings.</span></span>

   ![](media/TCimage24.png)

5. <span data-ttu-id="ebc68-153">마지막 단계에서는 1 단계에서 다운로드 한 Azure에 커넥터 응용 프로그램 소스 코드를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-153">The final step is to upload the connector app source code to Azure that you downloaded in Step 1.</span></span> <span data-ttu-id="ebc68-154">웹 브라우저에서 scm.azurewebsites.net/ZipDeployUi로 이동 합니다.<AzureAppResourceName>https://.</span><span class="sxs-lookup"><span data-stu-id="ebc68-154">In a web browser, go to https://<AzureAppResourceName>.scm.azurewebsites.net/ZipDeployUi.</span></span> <span data-ttu-id="ebc68-155">예를 들어이 섹션의 2 단계에서 이름이 지정 된 Azure 앱 리소스의 이름이 **twitterconnector**인 경우로 https://twitterconnector.scm.azurewebsites.net/ZipDeployUi이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-155">For example, if the name of your Azure app resource (which you named in step 2 in this section) is **twitterconnector**, then you would go to https://twitterconnector.scm.azurewebsites.net/ZipDeployUi.</span></span>

6. <span data-ttu-id="ebc68-156">1 단계에서 다운로드 한 SampleConnector을이 페이지로 끌어서 놓습니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-156">Drag and drop the SampleConnector.zip (that you downloaded in Step 1) to this page.</span></span> <span data-ttu-id="ebc68-157">파일이 업로드 되 고 배포가 성공적으로 수행 되 면 페이지는 다음 스크린샷과 유사 하 게 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-157">After the files are uploaded and the deployment is successful, the page will look similar to the following screenshot:</span></span>

   ![](media/TCimage25.png)

## <a name="step-5-create-the-twitter-app"></a><span data-ttu-id="ebc68-158">5 단계: Twitter 응용 프로그램 만들기</span><span class="sxs-lookup"><span data-stu-id="ebc68-158">Step 5: Create the Twitter app</span></span>

1. <span data-ttu-id="ebc68-159">https://developer.twitter.com으로 이동 하 고 조직의 개발자 계정에 대 한 자격 증명을 사용 하 여 로그인 한 다음 **앱**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-159">Go to https://developer.twitter.com, log in using the credentials for the developer account for your organization, and then click **Apps**.</span></span>

   ![TCimage25-5-.png](media/TCimage25-5.png)
2. <span data-ttu-id="ebc68-161">**앱 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-161">Click **Create an app**.</span></span>
   
   ![](media/TCimage26.png)

3. <span data-ttu-id="ebc68-162">**앱 세부 정보**에서 응용 프로그램에 대 한 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-162">Under **App details**, add information about the application.</span></span>

   ![](media/TCimage27.png)

4. <span data-ttu-id="ebc68-163">Twitter 개발자 대시보드에서 방금 만든 앱을 선택 하 고 표시 된 앱 ID를 복사한 다음 텍스트 파일 또는 기타 저장 위치에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-163">On the Twitter developer dashboard, select the app that you just created and copy the App ID that's displayed  and save it to a text file or other storage location.</span></span> <span data-ttu-id="ebc68-164">그런 다음 **세부 정보**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-164">Then click **Details**.</span></span>
   
   ![](media/TCimage28.png)

5. <span data-ttu-id="ebc68-165">**키 및 토큰** 탭의 **Consumer api 키** 아래에서 API 비밀 키를 복사 하 여 텍스트 파일 또는 기타 저장 위치에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-165">On the **Keys and tokens** tab, under **Consumer API keys** copy the API secret key and save it to a text file or other storage location.</span></span> <span data-ttu-id="ebc68-166">그런 다음 **만들기** 를 클릭 하 여 액세스 토큰과 액세스 토큰 비밀을 생성 한 다음 텍스트 파일 또는 기타 저장소 위치로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-166">Then click **Create** to generate an access token and an access token secret, and copy these to a text file or other storage location.</span></span>
   
   ![](media/TCimage29.png)

   <span data-ttu-id="ebc68-167">그런 다음 **만들기** 를 클릭 하 여 액세스 토큰과 액세스 토큰 비밀을 생성 한 다음 텍스트 파일 또는 기타 저장소 위치로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-167">Then click **Create** to generate an access token and an access token secret, and copy these to a text file or other storage location.</span></span>

6. <span data-ttu-id="ebc68-168">**사용 권한** 탭을 클릭 하 고 다음 스크린샷에 표시 된 대로 사용 권한을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-168">Click the **Permissions** tab and configure the permissions as shown in the following screenshot:</span></span>

   ![](media/TCimage30.png)

7. <span data-ttu-id="ebc68-169">권한 설정을 저장 한 후에는 **앱 세부 정보** 탭을 클릭 한 다음 **세부 정보 편집 >** 편집을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-169">After you save the permission settings, click the **App details** tab, and then click **Edit > Edit details**.</span></span>

   ![](media/TCimage31.png)

8. <span data-ttu-id="ebc68-170">다음 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-170">Do the following tasks:</span></span>

   <span data-ttu-id="ebc68-171">-커넥터 앱이 Twitter에 로그인 하도록 허용 하는 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-171">– Select the checkbox to allow the connector app to sign in to Twitter.</span></span>
   
   <span data-ttu-id="ebc68-172">- *Connectorserviceuri* 의 값이 조직의 Azure app 서비스 URL 인 \*\* \<connectorserviceuri>/views/twitteroauth\*\*형식을 사용 하 여 OAuth 리디렉션 Uri를 추가 합니다. 예를 https://twitterconnector.azurewebsites.net/Views/TwitterOAuth들면입니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-172">– Add the OAuth redirect Uri using the following format: **\<connectorserviceuri>/Views/TwitterOAuth**, where the value of *connectorserviceuri* is the Azure app service URL for your organization; for example, https://twitterconnector.azurewebsites.net/Views/TwitterOAuth.</span></span>

   ![](media/TCimage32.png)

<span data-ttu-id="ebc68-173">이제 Twitter 개발자 앱을 사용할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-173">The Twitter developer app is now ready to use.</span></span>

## <a name="step-6-configure-the-connector-web-app"></a><span data-ttu-id="ebc68-174">6 단계: 커넥터 웹 응용 프로그램 구성</span><span class="sxs-lookup"><span data-stu-id="ebc68-174">Step 6: Configure the connector web app</span></span> 

1. <span data-ttu-id="ebc68-175">Https://\<AzureAppResourceName> azurewebsites.net (여기서 **AzureAppResourceName** 은 4 단계에서 명명 한 Azure 앱 리소스의 이름)으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-175">Go to https://\<AzureAppResourceName>.azurewebsites.net (where **AzureAppResourceName** is the name of your Azure app resource that you named in Step 4).</span></span> <span data-ttu-id="ebc68-176">예를 들어 이름이 **twitterconnector**인 경우로 https://twitterconnector.azurewebsites.net이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-176">For example, if the name is **twitterconnector**, go to https://twitterconnector.azurewebsites.net.</span></span> <span data-ttu-id="ebc68-177">이 앱의 홈 페이지는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-177">The home page of the app looks like the following screenshot:</span></span>

   ![](media/FBCimage41.png)

2. <span data-ttu-id="ebc68-178">**구성을** 클릭 하 여 로그인 페이지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-178">Click **Configure** to display a sign in page.</span></span>

   ![](media/FBCimage42.png)

3. <span data-ttu-id="ebc68-179">테 넌 트 Id 상자에 2 단계에서 받은 테 넌 트 Id를 입력 하거나 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-179">In the Tenant Id box, type or paste your tenant Id (that you obtained in Step 2).</span></span> <span data-ttu-id="ebc68-180">암호 상자에 2 단계에서 구한 APISecretKey를 입력 하거나 붙여 넣은 다음 **구성 설정 설정을** 클릭 하 여 **구성 세부 정보** 페이지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-180">In the password box, type or paste the APISecretKey (that you obtained in Step 2), and then click **Set Configuration Settings** to display the **Configuration Details** page.</span></span>

   ![](media/TCimage35.png)

4. <span data-ttu-id="ebc68-181">**구성 세부 정보**에서 다음 구성 설정을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-181">Under **Configuration Details**, enter the following configuration settings</span></span> 

   <span data-ttu-id="ebc68-182">– **Twitter Api 키** -5 단계에서 만든 Twitter 응용 프로그램의 앱 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-182">– **Twitter Api Key** – The app ID for the Twitter application that you created in Step 5.</span></span>
   <span data-ttu-id="ebc68-183">– **Twitter Api 비밀 키** -5 단계에서 만든 Twitter 응용 프로그램에 대 한 api 비밀 키입니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-183">– **Twitter Api Secret Key** – The API secret key for the Twitter application that you created in Step 5.</span></span>
   <span data-ttu-id="ebc68-184">- **Twitter 액세스 토큰** -5 단계에서 만든 액세스 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-184">– **Twitter Access Token** – The access token that you created in Step 5.</span></span>
   <span data-ttu-id="ebc68-185">- **Twitter 액세스 토큰 비밀** -5 단계에서 만든 액세스 토큰 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-185">– **Twitter Access Token Secret** – The access token secret that you created in Step 5.</span></span>
   <span data-ttu-id="ebc68-186">- **Aad 응용 프로그램 id** -2 단계- **Aad 응용 프로그램 비밀** 번호에서 만든 Azure Active Directory 앱의 응용 프로그램 ID-4 단계에서 만든 APISecretKey 암호의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-186">– **AAD Application ID** – The application ID for the Azure Active Directory app that you created in Step 2 – **AAD Application Secret** – The value for the APISecretKey secret that you created in Step 4.</span></span>
   <span data-ttu-id="ebc68-187">– **Aad 응용 프로그램 uri** -2 단계에서 가져온 aad 응용 프로그램 uri 예를 https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213들면입니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-187">– **AAD Application Uri** – The AAD application Uri obtained in Step 2; for example, https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213.</span></span>
   <span data-ttu-id="ebc68-188">- **App Insights Instrumentation 키** -이 상자를 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-188">– **App Insights Instrumentation Key** – Leave this box blank.</span></span>

5. <span data-ttu-id="ebc68-189">**저장** 을 클릭 하 여 커넥터 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-189">Click **Save** to save the connector settings.</span></span>

## <a name="step-7-set-up-a-custom-connector-in-the-security-and-compliance-center"></a><span data-ttu-id="ebc68-190">7 단계: 보안 및 준수 센터에서 사용자 지정 커넥터 설정</span><span class="sxs-lookup"><span data-stu-id="ebc68-190">Step 7: Set up a custom connector in the security and compliance center</span></span>

1.  <span data-ttu-id="ebc68-191">로 이동한 <https://protection.office.com> 후 **데이터 거 버 넌 \> 스 \> 가져오기 보관 타사 데이터**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-191">Go to <https://protection.office.com> and then click **Data governance \> Import \> Archive third-party data**.</span></span>

    ![](media/TCimage36.png)

2. <span data-ttu-id="ebc68-192">**커넥터 추가** 를 클릭 한 다음 **Twitter**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-192">Click **Add a connector** and then click **Twitter**.</span></span>

   ![](media/TCimage37.png)

3. <span data-ttu-id="ebc68-193">**커넥터 앱 추가** 페이지에서 다음 정보를 입력 하 고 **커넥터 유효성 검사**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-193">On the **Add Connector App** page, enter the following information and then click **Validate connector**.</span></span>

    <span data-ttu-id="ebc68-194">-첫 번째 상자에 **Twitter**와 같은 커넥터의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-194">– In the first box, type a name for the connector, such as **Twitter**.</span></span>
    <span data-ttu-id="ebc68-195">-두 번째 상자에서 4 단계에서 추가한 APISecretKey의 값을 입력 하거나 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-195">– In the second box, type or paste the value of the APISecretKey that you added in Step 4.</span></span>
    <span data-ttu-id="ebc68-196">-세 번째 상자에 Azure 앱 서비스 URL을 입력 하거나 붙여넣습니다. 예를 **https://twitterconnector.azurewebsites.net**들면입니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-196">– In the third box, type or paste the Azure app service URL; for example, **https://twitterconnector.azurewebsites.net**.</span></span>

   <span data-ttu-id="ebc68-197">커넥터 유효성 검사가 완료 되 면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-197">After the connector is successfully validated, click **Next**.</span></span>

   ![](media/TCimage38.png)

4. <span data-ttu-id="ebc68-198">**커넥터 앱을 사용 하 여 로그인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-198">Click **Login with Connector App**.</span></span>

   ![](media/TCimage39.png)

5. <span data-ttu-id="ebc68-199">APISecretKey를 다시 입력 하거나 붙여 넣은 다음 **커넥터 서비스에 로그인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-199">Type or paste the APISecretKey again and then click  **Login to Connector Service**.</span></span>

   ![](media/TCimage40.png)


6. <span data-ttu-id="ebc68-200">**Twitter를 사용 하 여 계속을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-200">Click **Continue with Twitter**.</span></span>

7. <span data-ttu-id="ebc68-201">Twitter 로그인 페이지에서 조직의 Twitter 계정에 대 한 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-201">On the Twitter sign in page, sign in using the credentials for the account for your organization’s Twitter account.</span></span>

   ![](media/TCimage42.png)

   <span data-ttu-id="ebc68-202">로그인 하면 Twitter 페이지에 "Twitter 커넥터 작업을 설정 했습니다." 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-202">After you sign in, the Twitter page will display the following message, "Twitter Connector Job Successfully set up."</span></span>

8. <span data-ttu-id="ebc68-203">**마침을** 클릭 하 여 Twitter 커넥터 설정을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-203">Click **Finish** to complete setting up the Twitter connector.</span></span>

9. <span data-ttu-id="ebc68-204">**필터 설정** 페이지에서 특정 연령 인 항목을 가져오고 보관 하는 필터를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-204">On the **Set Filters** page, you can apply a filter to import (and archive) items that are a certain age.</span></span> <span data-ttu-id="ebc68-205">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-205">Click **Next**.</span></span>

   ![](media/TCimage44.png)

10. <span data-ttu-id="ebc68-206">**저장소 계정 설정** 페이지에서 Twitter 항목을 가져올 Office 365 사서함의 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-206">On the **Set Storage Account** page, type the email address of an Office 365 mailbox that the Twitter items will be imported to.</span></span>

    ![](media/TCimage45.png)

11. <span data-ttu-id="ebc68-207">설정을 검토 하 고 **마침을** 클릭 하 여 보안 & 준수 센터에서 커넥터 설정을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-207">Review your settings and then click **Finish** to complete the connector setup in the Security & Compliance Center.</span></span>

    ![](media/TCimage46.png)

    ![](media/TCimage47.png)

12. <span data-ttu-id="ebc68-208">**타사 데이터 보관** 페이지로 이동 하 여 가져오기 프로세스의 진행 상황을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc68-208">Go to the **Archive third-party data** page to see the progress of the import process.</span></span>

    ![](media/TCimage48.png)
