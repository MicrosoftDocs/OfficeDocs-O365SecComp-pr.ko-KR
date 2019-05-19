---
title: 샘플 커넥터를 사용 하 여 Office 365에서 Twitter 데이터 보관 (미리 보기)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: 관리자는 네이티브 커넥터를 설정 하 여 Twitter 데이터를 Office 365로 가져올 수 있습니다. 이를 통해 Office 365의 타사 데이터 원본에서 데이터를 보관할 수 있으므로 법적 보존, 콘텐츠 검색 및 보존 정책과 같은 규정 준수 기능을 사용 하 여 조직의 타사 데이터를 관리 하는 것을 관리할 수도 있습니다.
ms.openlocfilehash: b53d882a66ba30a0c4c90389253689a9fe1fb457
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155620"
---
# <a name="use-a-sample-connector-to-archive-twitter-data-in-office-365-preview"></a><span data-ttu-id="f1d20-104">샘플 커넥터를 사용 하 여 Office 365에서 Twitter 데이터 보관 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="f1d20-104">Use a sample connector to archive Twitter data in Office 365 (Preview)</span></span>

<span data-ttu-id="f1d20-105">Office 365에서 Twitter 데이터를 보관 하는 샘플 커넥터 기능은 미리 보기에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-105">The sample connector feature to archive Twitter data in Office 365 is in Preview.</span></span>

<span data-ttu-id="f1d20-106">Office 365의 Security & 준수 센터에 있는 샘플 커넥터를 사용 하 여 Twitter에서 데이터를 가져오고 보관 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-106">Use a sample connector in the Security & Compliance Center in Office 365 to import and archive data from Twitter.</span></span> <span data-ttu-id="f1d20-107">샘플 커넥터를 설정 하 고 구성한 후에는 예약 된 방식으로 조직의 Twitter 계정에 연결 하 고, 항목의 콘텐츠를 전자 메일 메시지 형식으로 변환한 다음 해당 항목을 Office 365의 사서함으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-107">After you set up and configure a sample connector, it connects to your organization's Twitter account (on a scheduled basis), converts the content of an item to an email message format, and then imports those items to a mailbox in Office 365.</span></span>

<span data-ttu-id="f1d20-108">Twitter 데이터를 가져온 후에는 사서함에 저장 된 데이터에 소송 보존, 콘텐츠 검색, 원본 위치 보관, 감사, 감독 및 Office 365 고정 정책 등의 Office 365 준수 기능을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-108">After Twitter data is imported, you can apply Office 365 compliance features such as Litigation Hold, Content Search, In-Place Archiving, Auditing, Supervision, and Office 365 retention policies to the data stored in the mailbox.</span></span> <span data-ttu-id="f1d20-109">예를 들어 콘텐츠 검색을 사용 하 여 타사 데이터를 검색 하거나, 고급 eDiscovery 사례에서 custodian과 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-109">For example,you can search third-party data using Content Search or associate it with a custodian in an Advanced eDiscovery case.</span></span> <span data-ttu-id="f1d20-110">샘플 커넥터를 사용 하 여 Office 365에서 Twitter 데이터를 가져오고 보관 하면 조직이 정부 및 규정 정책을 준수 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-110">Using sample connectors to import and archive Twitter data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>

> [!NOTE]
> <span data-ttu-id="f1d20-111">현재로 서는 Twitter 및 [Facebook Business 페이지](archive-facebook-data-with-sample-connector.md) 에 대 한 샘플 커넥터만 미리 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-111">Currently, only the sample connectors for Twitter and [Facebook Business pages](archive-facebook-data-with-sample-connector.md) are available for Preview.</span></span> <span data-ttu-id="f1d20-112">더 많은 샘플 커넥터가 곧 제공 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-112">More sample connectors are coming soon.</span></span>


## <a name="prerequisites-for-setting-up-a-connector-for-twitter"></a><span data-ttu-id="f1d20-113">Twitter에 대 한 커넥터를 설정 하기 위한 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="f1d20-113">Prerequisites for setting up a connector for Twitter</span></span>

<span data-ttu-id="f1d20-114">보안 & 준수 센터에서 샘플 커넥터를 설정 및 구성 하 여 조직의 Twitter 계정에서 데이터를 가져오고 보관 하려면 먼저 다음 필수 구성 요소를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-114">You must complete the following prerequisites before you can set up and configure a sample connector in the Security & Compliance Center to import and archive data from your organization's Twitter account.</span></span> 

- <span data-ttu-id="f1d20-115">조직에 대 한 Twitter 계정이 필요 합니다. 커넥터를 설정 하는 경우이 계정에 로그인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-115">You need a Twitter account for your organization; you'll need to sign in to this account when setting up the connector.</span></span>

- <span data-ttu-id="f1d20-116">조직에 유효한 Azure 구독이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-116">Your organization must have a valid Azure subscription.</span></span> <span data-ttu-id="f1d20-117">기존 Azure 구독이 없는 경우 다음 옵션 중 하나를 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-117">If you don't have an existing Azure subscription, you can sign up for one of these options:</span></span>

    - [<span data-ttu-id="f1d20-118">무료 1 년 Azure 구독 등록</span><span class="sxs-lookup"><span data-stu-id="f1d20-118">Sign up for a free 1 year Azure subscription</span></span>](https://azure.microsoft.com/free) 

    - [<span data-ttu-id="f1d20-119">방문 비용 청구 Azure 구독에 등록</span><span class="sxs-lookup"><span data-stu-id="f1d20-119">Sign up for a Pay-As-You-Go Azure subscription</span></span>](https://azure.microsoft.com/pricing/purchase-options/pay-as-you-go/)

    > [!NOTE]
    > <span data-ttu-id="f1d20-120">Office 365 구독에 포함 된 [무료 Azure Active Directory 구독은](use-your-free-azure-ad-subscription-in-office-365.md) 보안 _AMP_ 준수 센터의 예제 커넥터를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-120">The [free Azure Active Directory subscription](use-your-free-azure-ad-subscription-in-office-365.md) that's included with your Office 365 subscription doesn't support the sample connectors in the Security & Compliance Center.</span></span>

- <span data-ttu-id="f1d20-121">조직에서는 Office 365 가져오기 서비스가 조직의 사서함 데이터에 액세스할 수 있도록 허용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-121">Your organization must consent to allow the Office 365 Import service to access mailbox data in your organization.</span></span> <span data-ttu-id="f1d20-122">이 요청에 동의 하려면 [이 페이지로](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent)이동 하 여 Office 365 전역 관리자의 자격 증명으로 로그인 한 다음 요청을 수락 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-122">To consent to this request, go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), sign in with the credentials of an Office 365 global admin, and then accept the request.</span></span>

- <span data-ttu-id="f1d20-123">보안 & 준수 (7 단계)에서 사용자 지정 커넥터를 설정 하는 사용자에 게 Exchange Online의 사서함 가져오기 내보내기 역할이 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-123">The user who sets up the custom connector in the Security & Compliance (in Step 7) must be assigned the Mailbox Import Export role in Exchange Online.</span></span> <span data-ttu-id="f1d20-124">기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-124">By default, this role isn't assigned to any role group in Exchange Online.</span></span> <span data-ttu-id="f1d20-125">Exchange Online의 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-125">You can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> <span data-ttu-id="f1d20-126">또는 새 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 해당 사용자를 구성원으로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-126">Or you can create a new role group, assign the Mailbox Import Export role, and then add the appropriate users as members.</span></span> <span data-ttu-id="f1d20-127">자세한 내용은 "Exchange Online에서 역할 그룹 관리" 문서의 [역할 그룹 만들기](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) 또는 [역할 그룹 수정](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f1d20-127">For more information, see the  [Create role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) or [Modify role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) sections in the article "Manage role groups in Exchange Online".</span></span>

## <a name="step-1-download-the-pre-built-connector-app-package-from-github"></a><span data-ttu-id="f1d20-128">1 단계: Github에서 미리 작성 된 커넥터 앱 패키지 다운로드</span><span class="sxs-lookup"><span data-stu-id="f1d20-128">Step 1: Download the pre-built connector app package from Github</span></span>

<span data-ttu-id="f1d20-129">첫 번째 단계는 twitter API를 사용 하 여 twitter 계정에 연결 하 고 데이터를 추출 하 여 Office 365로 가져올 수 있는 Twitter 샘플 커넥터 응용 프로그램에 대 한 소스 코드를 다운로드 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-129">The first step is to download the source code for the Twitter sample connector app that will use a Twitter API to connect to your Twitter account and extract data so you can import it to Office 365.</span></span>

1. <span data-ttu-id="f1d20-130">[이 GitHub 사이트로](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases)이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-130">Go to [this GitHub site](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases).</span></span> 
2. <span data-ttu-id="f1d20-131">최신 버전에서 **SampleConnector** 파일을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-131">Under the latest release, click the **SampleConnector.zip** file.</span></span>
3. <span data-ttu-id="f1d20-132">로컬 컴퓨터의 위치에 ZIP 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-132">Save the ZIP file to a location on your local computer.</span></span> <span data-ttu-id="f1d20-133">4 단계에서이 zip 파일을 Azure에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-133">You'll upload this zip file to Azure in Step 4.</span></span>

## <a name="step-2-create-an-app-in-azure-active-directory"></a><span data-ttu-id="f1d20-134">2 단계: Azure Active Directory에 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="f1d20-134">Step 2: Create an app in Azure Active Directory</span></span>

<span data-ttu-id="f1d20-135">다음 단계에서는 AAD (Azure Active Directory)에서 새 앱을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-135">The next step is to register a new app in Azure Active Directory (AAD).</span></span> <span data-ttu-id="f1d20-136">이 앱은 Twitter 커넥터에 대해 4 단계에서 구현 하는 웹 앱 리소스에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-136">This app will correspond to the web app resource that you'll implement in Step 4 for the Twitter connector.</span></span> 

<span data-ttu-id="f1d20-137">단계별 지침은 [2 단계: Azure Active Directory에서 앱 만들기](deploy-twitter-connector.md#step-2-create-an-app-in-azure-active-directory)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f1d20-137">For step-by-step instructions, see [Step 2: Create an app in Azure Active Directory](deploy-twitter-connector.md#step-2-create-an-app-in-azure-active-directory).</span></span>

<span data-ttu-id="f1d20-138">단계별 지침에 따라이 단계를 완료 하는 동안 다음 정보를 텍스트 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-138">During the completion of this step (by following the step-by-step instructions), you'll save the following information to a text file.</span></span> <span data-ttu-id="f1d20-139">이러한 값은 배포 프로세스의 이후 단계에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-139">The values for these will be used in later steps in the deployment process.</span></span>

- <span data-ttu-id="f1d20-140">AAD 응용 프로그램 ID</span><span class="sxs-lookup"><span data-stu-id="f1d20-140">AAD application ID</span></span>
- <span data-ttu-id="f1d20-141">AAD 응용 프로그램 비밀</span><span class="sxs-lookup"><span data-stu-id="f1d20-141">AAD application secret</span></span>
- <span data-ttu-id="f1d20-142">AAD 응용 프로그램 Uri</span><span class="sxs-lookup"><span data-stu-id="f1d20-142">AAD application Uri</span></span>
- <span data-ttu-id="f1d20-143">테 넌 트 Id</span><span class="sxs-lookup"><span data-stu-id="f1d20-143">Tenant Id</span></span>

## <a name="step-3-create-an-azure-storage-account"></a><span data-ttu-id="f1d20-144">3 단계: Azure storage 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="f1d20-144">Step 3: Create an Azure storage account</span></span>

<span data-ttu-id="f1d20-145">조직에 대해 배포 하는 Twitter 커넥터는 Twitter에서이 단계에서 만든 Azure 저장소 위치로 항목을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-145">The Twitter connector that you deploy for your organization will upload the items from Twitter to the Azure storage location that you create in this step.</span></span> <span data-ttu-id="f1d20-146">보안 & 준수 센터 (7 단계)에서 사용자 지정 커넥터를 만든 후에는 Office 365 가져오기 서비스에서 Azure storage 위치에 있는 Twitter 데이터를 Office 365의 사서함으로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-146">After you create a custom connector in the Security & Compliance Center (in Step 7), the Office 365 Import service will copy the Twitter data from the Azure storage location to a mailbox in Office 365.</span></span> <span data-ttu-id="f1d20-147">앞에서 설명한 것 처럼 [필수 구성 요소](#prerequisites-for-setting-up-a-connector-for-twitter) 섹션에서 azure storage 계정을 만들려면 유효한 azure 구독이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-147">As previous explained in the [Prerequisites](#prerequisites-for-setting-up-a-connector-for-twitter) section, you must have a valid Azure subscription to create an Azure storage account.</span></span>

<span data-ttu-id="f1d20-148">단계별 지침은 [3 단계: Azure storage Account 만들기](deploy-twitter-connector.md#step-3-create-an-azure-storage-account)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f1d20-148">For step-by-step instructions, see [Step 3: Create an Azure storage account](deploy-twitter-connector.md#step-3-create-an-azure-storage-account).</span></span>

<span data-ttu-id="f1d20-149">단계별 지침에 따라이 단계를 완료 하는 동안 생성 되는 연결 문자열 Uri를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-149">During the completion of this step (by following the step-by-step instructions) you'll save the connection string Uri that is generated.</span></span> <span data-ttu-id="f1d20-150">이 문자열을 사용 하 여 4 단계에서 Azure에서 웹 앱 리소스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-150">You'll use this string when creating a web app resource in Azure in Step 4.</span></span>

## <a name="step-4-create-a-web-app-resource-in-azure"></a><span data-ttu-id="f1d20-151">4 단계: Azure에서 웹 앱 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="f1d20-151">Step 4: Create a web app resource in Azure</span></span>

<span data-ttu-id="f1d20-152">다음 단계는 Twitter 커넥터용 Azure에서 웹 앱 리소스를 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-152">The next step is to create a web app resource in Azure for the Twitter connector.</span></span> 

<span data-ttu-id="f1d20-153">단계별 지침은 [4 단계: Azure에서 새 웹 앱 리소스 만들기](deploy-twitter-connector.md#step-4-create-a-new-web-app-resource-in-azure)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f1d20-153">For step-by-step instructions, see [Step 4: Create a new web app resource in Azure](deploy-twitter-connector.md#step-4-create-a-new-web-app-resource-in-azure).</span></span>

<span data-ttu-id="f1d20-154">이 단계를 완료 하는 동안 단계별 지침을 따라 웹 앱 리소스를 만들 때 다음 정보 (이전 단계를 완료 한 후에 텍스트 파일로 복사)를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-154">During the completion of this step (by following the step-by-step instructions), you'll provide the following information (that you've copied to a text file after completing the previous steps) when creating the web app resource.</span></span>

- <span data-ttu-id="f1d20-155">APISecretKey –이 단계를 완료 하는 동안이 비밀을 만듭니다. 7 단계에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-155">APISecretKey – You will create this secret during the completion of this step; it will be used in Step 7.</span></span>
- <span data-ttu-id="f1d20-156">StorageAccountConnectionString-3 단계에서 Azure storage 계정을 만든 후 복사한 연결 문자열 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-156">StorageAccountConnectionString – The connection string Uri that you copied after creating the Azure storage account in Step 3.</span></span>
- <span data-ttu-id="f1d20-157">tenantId-2 단계에서 Azure Active Directory에 Twitter 커넥터 앱을 만든 후 복사한 Office 365 조직의 테 넌 트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-157">tenantId – The tenant ID of your Office 365 organization that you copied after creating the Twitter connector app in Azure Active Directory in Step 2.</span></span>

<span data-ttu-id="f1d20-158">또한이 단계에서 1 단계에서 다운로드 한 SampleConnector 파일을 업로드 하 여 Twitter 커넥터 응용 프로그램에 대 한 소스 코드를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-158">Additionally, you will upload the SampleConnector.zip file (that you downloaded in Step 1) in this step to deploy the source code for the Twitter connector app.</span></span>

<span data-ttu-id="f1d20-159">이 단계를 완료 한 후 Azure 앱 서비스 URL (예:을 https://twitterconnector.azurewebsites.net)복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-159">After completing this step, be sure to copy the Azure app service URL (for example, https://twitterconnector.azurewebsites.net).</span></span> <span data-ttu-id="f1d20-160">이를 사용 하 여 5 단계, 6 단계 및 7 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-160">You'll need to use this to complete Step 5, Step 6, and Step 7).</span></span>

## <a name="step-5-create-developer-app-on-twitter"></a><span data-ttu-id="f1d20-161">5 단계: Twitter에서 개발자 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="f1d20-161">Step 5: Create developer app on Twitter</span></span>

<span data-ttu-id="f1d20-162">다음 단계에서는 Twitter에서 개발자 앱을 만들고 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-162">The next step is to create and configure a developer app on Twitter.</span></span> <span data-ttu-id="f1d20-163">7 단계에서 만든 사용자 지정 커넥터는 twitter 앱을 사용 하 여 Twitter API와 상호 작용 하 여 조직의 Twitter 계정에서 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-163">The custom connector that you create in Step 7 will use the Twitter app to interact with the Twitter API to obtain data from your organization's Twitter account.</span></span>

<span data-ttu-id="f1d20-164">단계별 지침은 [5 단계: Twitter 앱 만들기](deploy-twitter-connector.md#step-5-create-the-twitter-app)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f1d20-164">For step-by-step instructions, see [Step 5: Create the Twitter app](deploy-twitter-connector.md#step-5-create-the-twitter-app).</span></span>

<span data-ttu-id="f1d20-165">단계별 지침에 따라이 단계를 완료 하는 동안 다음 정보를 텍스트 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-165">During the completion of this step (by following the step-by-step instructions), you'll save the following information to a text file.</span></span> <span data-ttu-id="f1d20-166">이러한 값은 6 단계에서 Twitter 커넥터 응용 프로그램을 구성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-166">The values for these will be used to configure the Twitter connector app in Step 6.</span></span>

- <span data-ttu-id="f1d20-167">Twitter 응용 프로그램 ID</span><span class="sxs-lookup"><span data-stu-id="f1d20-167">Twitter application ID</span></span>
- <span data-ttu-id="f1d20-168">Twitter 응용 프로그램 비밀 (API 비밀 키)</span><span class="sxs-lookup"><span data-stu-id="f1d20-168">Twitter application secret (API secret key)</span></span>
- <span data-ttu-id="f1d20-169">Twitter 클라이언트 토큰</span><span class="sxs-lookup"><span data-stu-id="f1d20-169">Twitter client token</span></span>
- <span data-ttu-id="f1d20-170">Twitter 클라이언트 토큰 암호</span><span class="sxs-lookup"><span data-stu-id="f1d20-170">Twitter client token secret</span></span>

## <a name="step-6-configure-the-twitter-connector-app"></a><span data-ttu-id="f1d20-171">6 단계: Twitter 커넥터 응용 프로그램 구성</span><span class="sxs-lookup"><span data-stu-id="f1d20-171">Step 6: Configure the Twitter connector app</span></span>

<span data-ttu-id="f1d20-172">다음 단계에서는 4 단계에서 Azure web app 리소스를 만들 때 업로드 한 Twitter 커넥터 앱에 구성 설정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-172">The next step is to add configurations settings to the Twitter connector app that you uploaded when you created the Azure web app resource in Step 4.</span></span> <span data-ttu-id="f1d20-173">이렇게 하려면 커넥터 응용 프로그램의 홈 페이지로 이동 하 여 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-173">You'll do this by going to the home page of your connector app and configuring it.</span></span>

<span data-ttu-id="f1d20-174">단계별 지침은 [6 단계: 커넥터 웹 앱 구성을](deploy-twitter-connector.md#step-6-configure-the-connector-web-app)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f1d20-174">For step-by-step instructions, see [Step 6: Configure the connector web app](deploy-twitter-connector.md#step-6-configure-the-connector-web-app).</span></span>

<span data-ttu-id="f1d20-175">단계별 지침에 따라이 단계를 완료 하는 동안 이전 단계를 완료 한 후에 텍스트 파일로 복사한 다음 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-175">During the completion of this step (by following the step-by-step instructions), you'll provide the following information (that you've copied to a text file after completing the previous steps):</span></span>

- <span data-ttu-id="f1d20-176">Twitter 응용 프로그램 ID (5 단계에서 가져옴)</span><span class="sxs-lookup"><span data-stu-id="f1d20-176">Twitter application ID (obtained in Step 5)</span></span>
- <span data-ttu-id="f1d20-177">Twitter 응용 프로그램 비밀 (5 단계에서 가져옴)</span><span class="sxs-lookup"><span data-stu-id="f1d20-177">Twitter application secret (obtained in Step 5)</span></span>
- <span data-ttu-id="f1d20-178">Twitter 클라이언트 토큰 (5 단계에서 가져옴)</span><span class="sxs-lookup"><span data-stu-id="f1d20-178">Twitter client token (obtained in Step 5)</span></span>
- <span data-ttu-id="f1d20-179">Twitter 클라이언트 토큰 암호 (5 단계에서 가져옴)</span><span class="sxs-lookup"><span data-stu-id="f1d20-179">Twitter client token secret (obtained in Step 5)</span></span>
- <span data-ttu-id="f1d20-180">Azure Active Directory 응용 프로그램 ID (2 단계에서 가져온 AAD 응용 프로그램 ID)</span><span class="sxs-lookup"><span data-stu-id="f1d20-180">Azure Active Directory application ID (the AAD application ID obtained in Step 2)</span></span>
- <span data-ttu-id="f1d20-181">Azure Active Directory 응용 프로그램 비밀 (2 단계에서 얻은 AAD 응용 프로그램 암호)</span><span class="sxs-lookup"><span data-stu-id="f1d20-181">Azure Active Directory application secret (the AAD application secret obtained in Step 2)</span></span>
- <span data-ttu-id="f1d20-182">Azure Active Directory 응용 프로그램 Uri (2 단계에서 가져온 AAD 응용 프로그램 Uri (예:https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213)</span><span class="sxs-lookup"><span data-stu-id="f1d20-182">Azure Active Directory application Uri (the AAD application Uri obtained in Step 2; for example, https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213)</span></span>

## <a name="step-7-set-up-a-custom-connector-in-the-security--compliance-center"></a><span data-ttu-id="f1d20-183">7 단계: 보안 & 준수 센터에서 사용자 지정 커넥터 설정</span><span class="sxs-lookup"><span data-stu-id="f1d20-183">Step 7: Set up a custom connector in the Security & Compliance Center</span></span>

<span data-ttu-id="f1d20-184">마지막 단계는 조직의 Twitter 계정에서 Office 365의 지정 된 사서함으로 데이터를 가져올 사용자 지정 커넥터를 보안 & 준수 센터에 설정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-184">The final step is to set up the custom connector in the Security & Compliance Center that will import data from your organization's Twitter account to a specified mailbox in Office 365.</span></span> <span data-ttu-id="f1d20-185">이 단계를 성공적으로 완료 하면 Office 365 가져오기 서비스가 Twitter에서 Office 365로 데이터를 가져오는 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d20-185">After you successfully complete this step, the Office 365 Import service will start the process of importing data from Twitter to Office 365.</span></span> 

<span data-ttu-id="f1d20-186">단계별 지침은 [보안 및 준수 센터에서 7 단계: 사용자 지정 커넥터 설정](deploy-twitter-connector.md#step-7-set-up-a-custom-connector-in-the-security-and-compliance-center)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f1d20-186">For step-by-step instructions, see [Step 7: Set up a custom connector in the security and compliance center](deploy-twitter-connector.md#step-7-set-up-a-custom-connector-in-the-security-and-compliance-center).</span></span> 

<span data-ttu-id="f1d20-187">단계별 지침에 따라이 단계를 완료 하는 동안 다음 정보를 제공 합니다 (단계 완료 후 텍스트 파일로 복사).</span><span class="sxs-lookup"><span data-stu-id="f1d20-187">During the completion of this step (by following the step-by-step instructions), you'll provide the following information (that you've copied to a text file after completing the steps).</span></span>

- <span data-ttu-id="f1d20-188">4 단계에서 얻은 Azure app service URL (예:https://twitterconnector.azurewebsites.net)</span><span class="sxs-lookup"><span data-stu-id="f1d20-188">Azure app service URL (obtained in Step 4; for example https://twitterconnector.azurewebsites.net)</span></span>
- <span data-ttu-id="f1d20-189">APISecretKey (4 단계에서 만든 것)</span><span class="sxs-lookup"><span data-stu-id="f1d20-189">APISecretKey (that you created in Step 4)</span></span>
