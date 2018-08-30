---
title: 고객 키를 사용하여 Office 365에서 데이터 제어
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
description: 고객 키에 대 한 설정 Office 365 개발자를 위한 Exchange Online, Skype 비즈니스, SharePoint Online 및 비즈니스용 OneDrive에 대 한 하는 방법에 알아봅니다. 고객 키를 사용 하 컨트롤 조직의 암호화 키 및 Microsoft의 데이터 센터의 나머지 부분에서 데이터를 암호화 하 고 사용 하 여 Office 365를 구성 합니다.
ms.openlocfilehash: f8d7c12c32ca74b842f676f4a2ccde4d1c758361
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22559233"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a><span data-ttu-id="75718-104">고객 키를 사용하여 Office 365에서 데이터 제어</span><span class="sxs-lookup"><span data-stu-id="75718-104">Controlling your data in Office 365 using Customer Key</span></span>

<span data-ttu-id="75718-p102">고객 키를 사용 하 컨트롤 조직의 암호화 키 및 Microsoft의 데이터 센터의 나머지 부분에서 데이터를 암호화 하 고 사용 하 여 Office 365를 구성 합니다. 보관 된 데이터에는 Exchange Online 및 사서함 및 SharePoint Online에 저장 된 파일에 저장 된 비즈니스를 위한 Skype 및 비즈니스용 OneDrive에서 데이터를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p102">With Customer Key, you control your organization's encryption keys and then configure Office 365 to use them to encrypt your data at rest in Microsoft's data centers. Data at rest includes data from Exchange Online and Skype for Business that is stored in mailboxes and files that are stored in SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="75718-p103">Office 365에 대 한 고객 키를 사용 하려면 먼저 Azure를 설정 해야 합니다. 이 항목을 만들고 필요한 Azure 리소스를 구성 하기 위해 수행 해야하는 단계를 설명 하 고 Office 365의 고객 키를 설정 하기 위한 단계를 제공 합니다. Azure 설치를 완료 한 후 어떤 정책 및 따라서 사서함과 조직의 파일에 할당 하는 키를 결정 합니다. 사서함 및 파일을 정책을 할당 하지 않은 제어 하 고 Microsoft가 관리 하는 암호화 정책을 사용 합니다. 고객 키에 대 한 자세한 내용은 또는 일반 개요에 대 한 [Office 365 FAQ에 대 한 고객 키](service-encryption-with-customer-key-faq.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75718-p103">You must set up Azure before you can use Customer Key for Office 365. This topic describes the steps you need to follow to create and configure the required Azure resources and then provides the steps for setting up Customer Key in Office 365. After you have completed Azure setup, you determine which policy, and therefore, which keys, to assign to mailboxes and files in your organization. Mailboxes and files for which you don't assign a policy will use encryption policies that are controlled and managed by Microsoft. For more information about Customer Key, or for a general overview, see the [Customer Key for Office 365 FAQ](service-encryption-with-customer-key-faq.md).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="75718-p104">이 항목의 모범 사례를 따르는 것이 좋습니다. 이러한 이라고 **팁** 및 **중요**합니다. 고객 키 사용 해당 범위 수 만큼 클 전체 조직 루트 암호화 키를 제어할 수 있습니다. 즉, 이러한 키를 사용 하 여 실수 광범위 한 영향을 줄 수 및 서비스 중단 또는 취소할 데이터 손실 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p104">We strongly recommend that you follow the best practices in this topic. These are called out as **TIP** and **IMPORTANT**. Customer Key gives you control over root encryption keys whose scope can be as large as your entire organization. This means that mistakes made with these keys can have a broad impact and may result in service interruptions or irrevocable loss of your data.</span></span> 
  
## <a name="before-you-begin-setting-up-customer-key"></a><span data-ttu-id="75718-116">고객 키를 설정 하기 전에</span><span class="sxs-lookup"><span data-stu-id="75718-116">Before you begin setting up Customer Key</span></span>
<span data-ttu-id="75718-117"><a name="Beforeyoustart"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-117"></span></span>

<span data-ttu-id="75718-p105">시작 하기 전에 조직에 대 한 적절 한 라이선스를 포함 해야 합니다. Office 365의 고객 키 Office 365 e 5 또는 고급 준수 SKU에서 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p105">Before you get started, be sure you have the appropriate licensing for your organization. Customer Key in Office 365 is offered in Office 365 E5 or the Advanced Compliance SKU.</span></span>
  
<span data-ttu-id="75718-p106">그런 다음, 개념 및이 항목의 절차를 이해 하려면 [Azure 키 추적용](https://azure.microsoft.com/en-us/documentation/services/key-vault/) 설명서를 검토 해야 합니다. 또한 Azure, [테 넌 트](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant)예에 사용 되는 용어에 익숙한 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p106">Then, to understand the concepts and procedures in this topic, you should review the [Azure Key Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) documentation. Also, become familiar with the terms used in Azure, for example, [tenant](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span></span>
  
<span data-ttu-id="75718-122">고객 키로 이동한 다음 설명서를 포함 하 여에 의견을 제공 하려면 customerkeyfeedback@microsoft.com를 아이디어, 제안 및 측면을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="75718-122">To provide feedback on Customer Key, including the documentation, send your ideas, suggestions and perspectives to customerkeyfeedback@microsoft.com.</span></span>
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a><span data-ttu-id="75718-123">Office 365에 대 한 고객 키를 설정 하는 개요 (영문)</span><span class="sxs-lookup"><span data-stu-id="75718-123">Overview of setting up Customer Key for Office 365</span></span>
<span data-ttu-id="75718-124"><a name="Overview"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-124"></span></span>

<span data-ttu-id="75718-p107">고객 키를 설정 하려면 이러한 작업을 수행 합니다. 이 항목의 나머지 부분 각 작업 또는 프로세스의 각 단계에 대 한 자세한 내용은 아웃 링크에 대 한 자세한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p107">To set up Customer Key you will complete these tasks. The rest of this topic provides detailed instructions for each task, or links out to more information for each step in the process.</span></span>
  
<span data-ttu-id="75718-127">**Azure 및 Microsoft FastTrack:**</span><span class="sxs-lookup"><span data-stu-id="75718-127">**In Azure and Microsoft FastTrack:**</span></span>
  
<span data-ttu-id="75718-p108">Azure PowerShell 원격으로 연결 하 여 대부분의 이러한 작업을 완료 합니다. Azure PowerShell의 나중에 또는 최상의 결과 4.4.0 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p108">You will complete most of these tasks by remotely connecting to Azure PowerShell. For best results, use version 4.4.0 or later of Azure PowerShell.</span></span>
  
- [<span data-ttu-id="75718-130">두 새로운 Azure 구독 만들기</span><span class="sxs-lookup"><span data-stu-id="75718-130">Create two new Azure subscriptions</span></span>](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [<span data-ttu-id="75718-131">필수 보존 기간을 사용 하 여 Azure 구독을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-131">Register Azure subscriptions to use a mandatory retention period</span></span>](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    <span data-ttu-id="75718-132">1 ~ 5 일 이내 등록 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-132">Registration can take from one to five business days.</span></span>
    
- [<span data-ttu-id="75718-133">Office 365에 대 한 고객 키를 정품 인증을 요청을 제출</span><span class="sxs-lookup"><span data-stu-id="75718-133">Submit a request to activate Customer Key for Office 365</span></span>](controlling-your-data-using-customer-key.md#FastTrack)
    
    <span data-ttu-id="75718-p109">두 새로운 Azure 구독을 만든 후에 Microsoft FastTrack 포털에서 호스팅하는 웹 양식을 작성 하 여 적절 한 고객 키 제공 요청을 제출 하려면 필요 합니다. FastTrack 팀 고객 키 지원을 제공 하지 않습니다. 단순히 office FastTrack 포털을 사용 하 여 양식을 전송 하 고 관련 기능을 제공 하는 고객 키에 대 한 추적 하는 데 도움이 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p109">Once you've created the two new Azure subscriptions, you'll need to submit the appropriate Customer Key offer request by completing a web form that is hosted in the Microsoft FastTrack portal. The FastTrack team doesn't provide assistance with Customer Key. Office simply uses the FastTrack portal to allow you to submit the form and to help us track the relevant offers for Customer Key.</span></span>
  
<span data-ttu-id="75718-p110">고객 키 제공을 제출 하면 Microsoft에서 요청을 검토 하 고 있음을 알려줍니다 설치 작업의 나머지 부분을 진행할 수 있습니다. 이 프로세스에는 최대 5 개까지 비즈니스 일 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p110">Once you have submitted a Customer Key offer, Microsoft reviews your request and notifies you when you can proceed with the rest of the setup tasks. This process can take up to five business days.</span></span>
    
- [<span data-ttu-id="75718-139">각 구독에 프리미엄 Azure 키 추적용 만들기</span><span class="sxs-lookup"><span data-stu-id="75718-139">Create a premium Azure Key Vault in each subscription</span></span>](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [<span data-ttu-id="75718-140">각 주요 추적용에 사용 권한 할당</span><span class="sxs-lookup"><span data-stu-id="75718-140">Assign permissions to each key vault</span></span>](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [<span data-ttu-id="75718-141">설정 하 고 확인을 위해 주요 볼트 대화에서 일시 삭제</span><span class="sxs-lookup"><span data-stu-id="75718-141">Enable and then confirm soft delete on your key vaults</span></span>](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [<span data-ttu-id="75718-142">각 주요 추적용 중 하나를 만들거나 키를 가져오기 (영문) 하 여 키 추가</span><span class="sxs-lookup"><span data-stu-id="75718-142">Add a key to each key vault either by creating or importing a key</span></span>](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [<span data-ttu-id="75718-143">키의 복구 수준 확인</span><span class="sxs-lookup"><span data-stu-id="75718-143">Check the recovery level of your keys</span></span>](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [<span data-ttu-id="75718-144">백업 Azure 키 볼트</span><span class="sxs-lookup"><span data-stu-id="75718-144">Backup Azure Key Vault</span></span>](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [<span data-ttu-id="75718-145">Azure 키 추적용 구성 설정의 유효성을 검사합니다</span><span class="sxs-lookup"><span data-stu-id="75718-145">Validate Azure Key Vault configuration settings</span></span>](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [<span data-ttu-id="75718-146">각 Azure 키 추적용 키에 대 한 URI를 얻으려면</span><span class="sxs-lookup"><span data-stu-id="75718-146">Obtain the URI for each Azure Key Vault key</span></span>](controlling-your-data-using-customer-key.md#GetKeyURI)
    
<span data-ttu-id="75718-147">**Office 365:**</span><span class="sxs-lookup"><span data-stu-id="75718-147">**In Office 365:**</span></span>
  
<span data-ttu-id="75718-148">Exchange Online 및 비즈니스를 위한 Skype:</span><span class="sxs-lookup"><span data-stu-id="75718-148">Exchange Online and Skype for Business:</span></span>
  
- [<span data-ttu-id="75718-149">비즈니스를 위한 Exchange Online 및 Skype와 함께 사용에 대 한 데이터 암호화 정책 (DEP) 만들기</span><span class="sxs-lookup"><span data-stu-id="75718-149">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [<span data-ttu-id="75718-150">사서함에는 DEP 할당</span><span class="sxs-lookup"><span data-stu-id="75718-150">Assign a DEP to a mailbox</span></span>](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [<span data-ttu-id="75718-151">사서함 암호화의 유효성을 검사합니다</span><span class="sxs-lookup"><span data-stu-id="75718-151">Validate mailbox encryption</span></span>](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
<span data-ttu-id="75718-152">SharePoint Online 및 비즈니스용 OneDrive:</span><span class="sxs-lookup"><span data-stu-id="75718-152">SharePoint Online and OneDrive for Business:</span></span>
  
- [<span data-ttu-id="75718-153">비즈니스 지리적으로 분산에 대 한 각 SharePoint Online 및 OneDrive에 대 한 데이터 암호화 정책 (DEP) 만들기</span><span class="sxs-lookup"><span data-stu-id="75718-153">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [<span data-ttu-id="75718-154">암호화 그룹 사이트, 팀 사이트 및 비즈니스용 OneDrive의 유효성을 검사합니다</span><span class="sxs-lookup"><span data-stu-id="75718-154">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a><span data-ttu-id="75718-155">고객 키에 대 한 Azure 키 추적용 및 Microsoft FastTrack에서 작업을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-155">Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key</span></span>
<span data-ttu-id="75718-156"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-156"></span></span>

<span data-ttu-id="75718-p111">Office 365에 대 한 고객 키를 설정 하기 위해 Azure 키 볼트에 이러한 작업을 완료 합니다. 고객 키에 대 한 설정 Exchange Online 및 Skype 비즈니스 또는 SharePoint Online 및 OneDrive를 위한 Office 365에서 지원 되는 모든 서비스 또는 비즈니스에 대 한 하려는 여부에 관계 없이 다음이 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p111">Complete these tasks in Azure Key Vault in order to set up Customer Key for Office 365. You will need to complete these steps regardless of whether you intend to set up Customer Key for Exchange Online and Skype for Business or SharePoint Online and OneDrive for Business or for all supported services in Office 365.</span></span>
  
### <a name="create-two-new-azure-subscriptions"></a><span data-ttu-id="75718-159">두 새로운 Azure 구독 만들기</span><span class="sxs-lookup"><span data-stu-id="75718-159">Create two new Azure subscriptions</span></span>
<span data-ttu-id="75718-160"><a name="Create2newsubs"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-160"></span></span>

<span data-ttu-id="75718-p112">두 Azure 구독은 고객 키에 필요 합니다. 최상의 방법으로 고객 키로 사용에 대 한 새 Azure 구독을 만드는 것이 좋습니다. Azure 키 추적용 키 동일한 Azure Active Directory (AAD) 테 넌 트의 응용 프로그램에 대 한 권한을 부여할 수만, Office 365 조직과 사용 되는 DEPs 할당 될 동일한 Azure AD 테 넌 트를 사용 하 여 새 구독을 만들어야 합니다. Office 365 조직에 대 한 전역 관리자 권한이 있는 사용자 작업이 나 교육용 계정을 사용 하 여 예입니다. 자세한 단계는 [조직으로 Azure에 등록](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75718-p112">Two Azure subscriptions are required for Customer Key. As a best practice, Microsoft recommends that you create new Azure subscriptions for use with Customer Key. Azure Key Vault keys can only be authorized for applications in the same Azure Active Directory (AAD) tenant, you must create the new subscriptions using the same Azure AD tenant used with your Office 365 organization where the DEPs will be assigned. For example, using your work or school account that has global administrator privileges in your Office 365 organization. For detailed steps, see [Sign up for Azure as an organization](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="75718-p113">고객 키에는 각 데이터 암호화 정책 (DEP)에 대 한 두 키가 필요 합니다. 이 작업을 수행 하기 위해 두 Azure 구독 만들어야 합니다. 최상의 방법으로 별도 조직 구성원의 각 구독에 하나의 키를 구성 해야 하는 것이 좋습니다. 또한 이러한 Azure 구독 Office 365에 대 한 암호화 키 관리만 사용 해야 합니다. 이 경우 의도적으로, 실수로 또는 악의적으로 삭제 하 여 연산자 중 하나 또는 그렇지 않은 경우에 자신이 담당 하는 키를 mismanages 조직을 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p113">Customer Key requires two keys for each data encryption policy (DEP). In order to achieve this, you must create two Azure subscriptions. As a best practice, Microsoft recommends that you have separate members of your organization configure one key in each subscription. In addition, these Azure subscriptions should only be used to administer encryption keys for Office 365. This protects your organization in case one of your operators accidentally, intentionally, or maliciously deletes or otherwise mismanages the keys for which they are responsible. </span></span><br/> <span data-ttu-id="75718-p114">고객 키로 사용 하도록 Azure 키 추적용 리소스를 관리 하기 위한 전적으로 사용 되는 새로운 Azure 구독을 설정 하는 것이 좋습니다. 조직에 대해 만들 수 있는 Azure 구독 수에 실질적인 제한은 없습니다. 이러한 모범 사례를 따르는 고객 키로 사용 되는 리소스를 관리할 수 있게 하는 동안 실수에 따른 영향을 최소화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p114">We recommend that you set up new Azure subscriptions that are solely used for managing Azure Key Vault resources for use with Customer Key. There is no practical limit to the number of Azure subscriptions that you can create for your organization. Following these best practices will minimize the impact of human error while helping to manage the resources used by Customer Key.</span></span> 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a><span data-ttu-id="75718-174">Office 365에 대 한 고객 키를 정품 인증을 요청을 제출</span><span class="sxs-lookup"><span data-stu-id="75718-174">Submit a request to activate Customer Key for Office 365</span></span>
<span data-ttu-id="75718-175"><a name="FastTrack"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-175"></span></span>

<span data-ttu-id="75718-p115">Azure 단계를 완료 한 후 [Microsoft FastTrack 포털](https://fasttrack.microsoft.com/)에서 제공 요청을 제출 하려면 필요 합니다. FastTrack 웹 포털을 통해 요청을 제출 하면 Microsoft는 사용자가 제공한 Azure 키 추적용 구성 데이터 및 연락처 정보를 확인 합니다. 선택한 항목 형태로 제공 권한이 부여 된 담당자에 대 한 조직에 중요 한 이며 고객 키 등록을 완료 하는데 필요한 됩니다. 양식에서 선택 하 여 조직의 담당자 해지 하 고 삭제 하는 고객 키 데이터 암호화 정책으로 사용 되는 모든 키에 대 한 요청이의 신뢰성을 확인 하는 데 사용 됩니다. Exchange Online 추가 및 Skype 비즈니스 범위 및 일정 시간이 내에 대 한 SharePoint Online 및 비즈니스용 OneDrive에 대 한 고객 키를 정품 인증에 대 한 고객 키를 활성화 하려면이 단계를 한번씩 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p115">Once you've completed the Azure steps, you'll need to submit an offer request in the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/). Once you have submitted a request through the FastTrack web portal, Microsoft verifies the Azure Key Vault configuration data and contact information you provided. The selections that you make in the offer form regarding the authorized officers of your organization is critical and necessary for completion of Customer Key registration. The officers of your organization that you select in the form will be the used to ensure the authenticity of any request to revoke and destroy all keys used with a Customer Key data encryption policy. You'll need to do this step once to activate Customer Key for Exchange Online and Skype for Business coverage and a second time to activate Customer Key for SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="75718-181">고객 키를 정품 인증을 제공 하는 서비스를 전송 하려면 다음이 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-181">To submit an offer to activate Customer Key, complete these steps:</span></span>
  
1. <span data-ttu-id="75718-182">[Microsoft FastTrack 포털](https://fasttrack.microsoft.com/)에 로그인 Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-182">Using a work or school account that has global administrator permissions in your Office 365 organization, log in to the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/).</span></span>
    
2. <span data-ttu-id="75718-183">로그인 할 때 되 면 **대시보드**를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-183">Once you're logged in, browse to the **Dashboard**.</span></span>
    
3. <span data-ttu-id="75718-184">**제공**하는 선택 하 고 현재 제공 업체 목록을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-184">Choose **Offers**, and review the list of current offers.</span></span>
    
4. <span data-ttu-id="75718-185">경우에 적용 되는 제품에 대 한 **추가 정보** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-185">Choose **Learn More** for the offer that applies to you:</span></span> 
    
  - <span data-ttu-id="75718-186">**Exchange Online 및 비즈니스를 위한 Skype:** **Exchange에 대 한 고객 키** 제공에서 **추가 정보** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-186">**Exchange Online and Skype for Business:** Choose **Learn More** on the **Customer Key for Exchange** offer.</span></span> 
    
  - <span data-ttu-id="75718-187">**SharePoint Online 및 비즈니스용 OneDrive:** **SharePoint 및 비즈니스용 OneDrive에 대 한 고객 키** 제공에서 **추가 정보** 를 선택 했습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-187">**SharePoint Online and OneDrive for Business:** Chose **Learn More** on the **Customer Key for SharePoint and OneDrive for Business** offer.</span></span> 
    
5. <span data-ttu-id="75718-188">**세부 정보 제공** 페이지에서 **요청 만들기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-188">On the **Offer details** page, choose **Create Request**.</span></span>
    
6. <span data-ttu-id="75718-p116">적용 가능한 모든 내용과 제공 폼에서 요청 된 정보를 입력 합니다. 암호화 키 및 데이터의 영구 및 복구할 수 없는 폐기 승인에 대 한 권한 부여 하려는 조직의 담당자에 대 한 선택 항목을 특정 주의 해야 합니다. 양식을 완료 했을 때 **전송**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p116">Fill out all applicable details and requested information on the offer form. Pay particular attention to your selections for which officers of your organization you want to authorize to approve the permanent and irreversible destruction of encryption keys and data. Once you've completed the form, choose **Submit**.</span></span>
    
    <span data-ttu-id="75718-192">이 프로세스에는 사용자의 요청을 Microsoft에 알렸습니다 되 면 최대 5 개까지 비즈니스 일 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-192">This process can take up to five business days once Microsoft has been notified of your request.</span></span>
    
7. <span data-ttu-id="75718-193">필수 보존 기간 섹션 아래에 로그온을 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-193">Continue on to the mandatory retention period section below.</span></span>
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a><span data-ttu-id="75718-194">필수 보존 기간을 사용 하 여 Azure 구독을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-194">Register Azure subscriptions to use a mandatory retention period</span></span>
<span data-ttu-id="75718-195"><a name="RegisterSubsforMRP"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-195"></span></span>

<span data-ttu-id="75718-p117">루트 암호화 키의 임시 또는 영구 손실 경로일 수도 있고 매우 손상 된 서비스 작업에도 치명적인 및 데이터 손실이 발생할 수 있습니다. 이러한 이유로 고객 키로 사용 되는 리소스에 강력한 보호가 필요 합니다. 고객 키로 사용 되는 모든 Azure 자원의 기본 구성 외 보호 메커니즘을 제공 합니다. Azure 구독 태그가 지정 된 하거나 즉각적이 고 취소할 취소 되지 않게 하는 방식에서에 등록 될 수 있습니다. 필수 보존 기간에 대 한 등록 라고 합니다. 필수 보존 기간에 대 한 Azure 구독을 등록 하는 데 필요한 단계에는 Office 365 팀과 공동 작업이 필요 합니다. 1 ~ 5 비즈니스 일이 걸릴 수 있습니다. 이전에이 경우에 따라 용어가 "취소 하지 않으면" 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p117">The temporary or permanent loss of root encryption keys can be very disruptive or even catastrophic to service operation and can result in data loss. For this reason, the resources used with Customer Key require strong protection. All the Azure resources that are used with Customer Key offer protection mechanisms beyond the default configuration. Azure subscriptions can be tagged or registered in a way that will prevent immediate and irrevocable cancellation. This is referred to as registering for a mandatory retention period. The steps required to register Azure subscriptions for a mandatory retention period require collaboration with the Office 365 team. This process can take from one to five business days. Previously, this was sometimes referred to as "Do Not Cancel".</span></span>
  
<span data-ttu-id="75718-204">Office 365 팀에 연락, 하기 전에 고객 키로 사용 하는 각 Azure 구독에 대해 다음 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-204">Before contacting the Office 365 team, you must perform the following steps for each Azure subscription that you use with Customer Key:</span></span>
  
1. <span data-ttu-id="75718-p118">Azure PowerShell을 사용한 Azure 구독에 로그인 합니다. 자세한 내용은 [Azure PowerShell을 사용 하 여 로그](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75718-p118">Log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
2. <span data-ttu-id="75718-207">필수 보존 기간을 사용 하 여 알림 신청을 등록 레지스터 AzureRmProviderFeature cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-207">Run the Register-AzureRmProviderFeature cmdlet to register your subscriptions to use a mandatory retention period.</span></span>
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. <span data-ttu-id="75718-p119">프로세스를 완료 하는 Microsoft에 문의 합니다. SharePoint 및 비즈니스 팀 비즈니스용 OneDrive, [spock@microsoft.com](mailto:spock@microsoft.com)에 문의 합니다. Exchange Online 및 비즈니스를 위한 Skype, [exock@microsoft.com](mailto:exock@microsoft.com)에 문의 합니다. 서비스 수준 계약 (SLA) 필수 보존 기간을 사용 하 여 알림 신청을 완료 되 면이이 과정은 5 비즈니스 일 Microsoft가 되 고 되 면 알림을 (확인)를 등록 합니다. 전자 메일에 다음을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p119">Contact Microsoft to have the process finalized. For the SharePoint and OneDrive for Business team, contact [spock@microsoft.com](mailto:spock@microsoft.com). For Exchange Online and Skype for Business, contact [exock@microsoft.com](mailto:exock@microsoft.com). The Service Level Agreement (SLA) for completion of this process is five business days once Microsoft has been notified (and verified) that you have registered your subscriptions to use a mandatory retention period. Include the following in your email:</span></span>
    
    <span data-ttu-id="75718-213">**제목**: 고객 키에 대 한 \< *테 넌 트의 정규화 된 도메인 이름*\></span><span class="sxs-lookup"><span data-stu-id="75718-213">**Subject**: Customer Key for \<*Your tenant's fully-qualified domain name*\></span></span> 
    
    <span data-ttu-id="75718-214">**본문**: 기간 완료 필수 보존을 갖도록 하려는 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="75718-214">**Body**: Subscription IDs for which you want to have the mandatory retention period finalized.</span></span> 
    
4. <span data-ttu-id="75718-215">등록 완료 되는 Microsoft에서 알림, 수신 되 면 다음과 같은 Get AzureRmProviderFeature cmdlet을 실행 하 여 등록의 상태를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-215">Once you receive notification from Microsoft that registration is complete, verify the status of your registration by running the Get-AzureRmProviderFeature cmdlet as follows:</span></span>
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. <span data-ttu-id="75718-216">Get AzureRmProviderFeature cmdlet에서 **등록 State** 속성 반환 값이 **등록 된**의 인지를 확인 한 후 프로세스를 완료 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-216">After verifying that the **Registration State** property from the Get-AzureRmProviderFeature cmdlet returns a value of **Registered**, run the following command to complete the process:</span></span>
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a><span data-ttu-id="75718-217">각 구독에 프리미엄 Azure 키 추적용 만들기</span><span class="sxs-lookup"><span data-stu-id="75718-217">Create a premium Azure Key Vault in each subscription</span></span>
<span data-ttu-id="75718-218"><a name="CreateKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-218"></span></span>

<span data-ttu-id="75718-219">[Azure 키 추적용 시작](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), 설치 및 Azure PowerShell을 시작, Azure 구독에 연결, 자원 그룹 만들기 (영문) 및 주요 추적용 만들기 (영문)를 통해 하는 방법을 안내 하는에서 설명 하는 주요 추적용을 만드는 단계 자원 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="75718-219">The steps to create a key vault are documented in [Getting Started with Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), which guides you through installing and launching Azure PowerShell, connecting to your Azure subscription, creating a resource group, and creating a key vault in that resource group.</span></span>
  
<span data-ttu-id="75718-p120">한 SKU를 선택 해야 키 추적용을 만들 때는: 표준 또는 프리미엄 합니다. 표준 SKU-보호 하는 기능이 없는 보안 모듈 HSM (하드웨어) 키-소프트웨어로 보호에 대 한 Azure 키 추적용 키를 허용 하 고 프리미엄 SKU 키 추적용 키의 보호를 위한 Hsm 사용을 허용 합니다. 고객 키 강력 하 게 것이 좋지만 프리미엄 SKU만 사용 하 여 두 SKU를 사용 하는 주요 볼트를 허용 합니다. 두 종류의 키와 작업의 비용 이므로 동일, 비용의 유일한 차이점은 각 HSM 암호로 보호 된 키에 대 한 월별 비용입니다. 자세한 내용은 [키 추적용 가격](https://azure.microsoft.com/pricing/details/key-vault/) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75718-p120">When you create a key vault, you must choose a SKU: either Standard or Premium. The Standard SKU allows Azure Key Vault keys to be protected with software - there is no Hardware Security Module (HSM) key protection - and the Premium SKU allows the use of HSMs for protection of Key Vault keys. Customer Key accepts key vaults that use either SKU, though Microsoft strongly recommends that you use only the Premium SKU. The cost of operations with keys of either type is the same, so the only difference in cost is the cost per month for each HSM-protected key. See [Key Vault pricing](https://azure.microsoft.com/pricing/details/key-vault/) for details.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="75718-225">주요 볼트 프리미엄 SKU와 키 HSM 암호로 보호 된 프로덕션 데이터에 대 한 및 사용만 테스트 및 유효성 검사 목적을 위해 주요 볼트 표준 SKU와 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-225">Use the Premium SKU key vaults and HSM-protected keys for production data, and only use Standard SKU key vaults and keys for testing and validation purposes.</span></span> 
  
<span data-ttu-id="75718-p121">사용 하는 각 Office 365 서비스에 대 한를 사용 하는 고객 키에서 만든 두 Azure 구독 각 주요 추적용을 만듭니다. 등 Exchange Online 및 비즈니스만 또는 SharePoint Online 용 Skype 및 비즈니스용만, 볼트 하나만 쌍을 만들가 있습니다. Exchange Online 및 SharePoint Online에 대 한 고객 키를 사용 하려면 주요 볼트의 두 쌍을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p121">For each Office 365 service with which you will use Customer Key, create a key vault in each of the two Azure subscriptions that you created. For example, for Exchange Online and Skype for Business only or SharePoint Online and OneDrive for Business only, you will create only one pair of vaults. To enable Customer Key for both Exchange Online and SharePoint Online, you will create two pairs of key vaults.</span></span>
  
<span data-ttu-id="75718-p122">볼트 연관 됩니다 DEP의 용도 반영 하는 주요 볼트에 대 한 명명 규칙을 사용 합니다. 명명 규칙 권장 사항 아래 모범 사례 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75718-p122">Use a naming convention for key vaults that reflects the intended use of the DEP with which you will associate the vaults. See the Best Practices section below for naming convention recommendations.</span></span>
  
<span data-ttu-id="75718-p123">각 데이터 암호화 정책에 대 한 볼트의 별도, 쌍으로 지정 된 집합을 만듭니다. Exchange Online에 대 한 데이터 암호화 정책의 범위 사서함에 정책을 할당 하는 경우에 사용자가 선택 됩니다. 사서함을 할당 하는 정책을 하나만 하 고 최대 50 정책을 만들 수 있습니다. SharePoint Online에 대 한 정책 범위 지리적 위치 또는 지리적으로 분산 조직 내에서 데이터를 모두 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p123">Create a separate, paired set of vaults for each data encryption policy. For Exchange Online, the scope of a data encryption policy is chosen by you when you assign the policy to mailbox. A mailbox can have only one policy assigned, and you can create up to fifty policies. For SharePoint Online the scope of a policy is all of the data within an organization in a geographic location, or geo.</span></span>
  
<span data-ttu-id="75718-p124">주요 볼트를 만들 키 볼트 (경우에 매우 작은) 저장 용량이 필요 하 고 키 추적용 로깅,이 옵션을 설정 하는 경우 저장 된 데이터 생성 수도 있으므로 Azure 리소스 그룹 만들기를도 필요 합니다. 최상의 방법으로 별도 관리자를 사용 하 여 모든 관련된 고객 키 리소스를 관리 하는 관리자의 집합으로 정렬 된 관리를 사용 하 여 각 자원 그룹을 관리 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p124">The creation of key vaults also requires the creation of Azure resource groups, since key vaults need storage capacity (though very small) and Key Vault logging, if enabled, also generates stored data. As a best practice Microsoft recommends using separate administrators to manage each resource group, with the administration aligned with the set of administrators that will manage all related Customer Key resources.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="75718-p125">가용성을 극대화 하려면 프로그램 주요 볼트 Office 365 서비스에 근접 한 영역에 있어야 합니다. 예, Exchange Online 조직 북미에 있으면 대화 주요 볼트를 북미에 배치 합니다. Exchange Online 조직 유럽의 경우 유럽의 주요 볼트에 놓습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p125">To maximize availability, your key vaults should be in regions close to your Office 365 service. For example, if your Exchange Online organization is in North America, place your key vaults in North America. If your Exchange Online organization is in Europe, place your key vaults in Europe.</span></span><br/><span data-ttu-id="75718-p126">주요 볼트에 대 한 공통 접두사를 사용 하 고 사용의 약어 및 주요 추적용 및 키의 범위를 포함 (예: 북미, 이름의 가능한 쌍에에서는 볼트가 위치할 Contoso SharePoint 서비스는 O365SP NA VaultA1 Contoso에 대 한 및 Contoso-O365SP-NA-VaultA2 합니다. 추적용 이름은 Azure, 내에서 전역적으로 고유 문자열 않으므로 다른 Azure 고객에서 원하는 이름을 요구 이미는 하는 경우에 원하는 이름의 변형 시도 해야할 수 있습니다. 년 7 월 2017 년 일 이후로 추적용 이름은 변경할 수 없으므로, 설치 프로그램에 대 한 계획을 작성된 하 고 계획 제대로 실행을 확인 하려면 두번째 사용자를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p126">Use a common prefix for key vaults, and include an abbreviation of the use and scope of the key vault and keys (e.g., for the Contoso SharePoint service where the vaults will be located in North America, a possible pair of names is Contoso-O365SP-NA-VaultA1 and Contoso-O365SP-NA-VaultA2. Vault names are globally unique strings within Azure, so you may need to try variations of your desired names in case the desired names are already claimed by other Azure customers. As of July 2017 vault names cannot be changed, so a best practice is to have a written plan for setup and use a second person to verify the plan is executed correctly.</span></span><br/><span data-ttu-id="75718-p127">가능한 경우 지역에 연결 된 비에서 여 볼트를 만듭니다. Azure 지역 쌍으로 지정 된 서비스 오류 도메인에서 고가용성을 제공 합니다. 따라서 다른 사용자의 백업 지역으로 지역 쌍의 생각할 수 있습니다. 즉, 한 영역에 저장 되는 Azure 자원 내결함성을 쌍으로 지정 된 영역을 통해 사용할 수 있는 자동으로 됩니다. 이러한 이유로 총 가용성의 두 지역에서에서 사용 하는 쌍으로 지정 된 의미를 지역이 여기서 DEP에 사용 되는 두 볼트에 대 한 영역을 선택 합니다. 대부분 지역만 없으므로 두 영역을 아직 선택 영역에 연결 된 비 수 없습니다. 가능한 경우 사용 하는 종속 된 두 볼트에 대 한 비에 연결 된 두 지역 선택 이 총 가용성의 네 영역에서에서 향상 시켜줍니다. 자세한 내용은 참조 [비즈니스 연속성 및 재해 복구 (BCDR): Azure 쌍 영역](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) 지역 쌍의 현재 목록에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p127">If possible, create your vaults in non-paired regions. Paired Azure regions provide high availability across service failure domains. Therefore, regional pairs can be thought of as each other's backup region. This means that an Azure resource that is placed in one region is automatically gaining fault tolerance through the paired region. For this reason, choosing regions for two vaults used in a DEP where the regions are paired means that only a total of two regions of availability are in use. Most geographies only have two regions, so it's not yet possible to select non-paired regions. If possible, choose two non-paired regions for the two vaults used with a DEP. This benefits from a total of four regions of availability. For more information, see [Business continuity and disaster recovery (BCDR): Azure Paired Regions](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) for a current list of regional pairs.</span></span> 
  
### <a name="assign-permissions-to-each-key-vault"></a><span data-ttu-id="75718-252">각 주요 추적용에 사용 권한 할당</span><span class="sxs-lookup"><span data-stu-id="75718-252">Assign permissions to each key vault</span></span>
<span data-ttu-id="75718-253"><a name="KeyVaultPerms"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-253"></span></span>

<span data-ttu-id="75718-p128">각 주요 추적용에 대 한 구현에 따라 고객 키에 대 한 권한의 세 별도 집합을 정의 해야 합니다. 예, 하나는 다음의 각 항목에 대 한 사용 권한 집합을 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p128">For each key vault, you will need to define three separate sets of permissions for Customer Key, depending on your implementation. For example, you will need to define one set of permissions for each of the following:</span></span>
  
- <span data-ttu-id="75718-p129">**키 추적용 관리자가** 조직에 대 한 주요 추적용 대화의 일상적인 관리 작업을 수행 하는 합니다. 이러한 작업 백업 포함, 만들기, 가져오기, 가져오기, 목록, 및 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p129">**Key vault administrators** that will perform day-to-day management of your key vault for your organization. These tasks include backup, create, get, import, list, and restore.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="75718-p130">주요 추적용 관리자에 게 할당 된 권한 집합이 키를 삭제할 수 있는 권한이 포함 되지 않습니다. 이 의도적인 것 하 고는 중요 한 연습 합니다. 암호화 키를 삭제 하지 일반적으로 완료 되 면 데이터를 소멸 하므로 영구적으로 수행 하는 이후 합니다. 최상의 방법으로이 권한을 부여 하지 마십시오이 주요 추적용 관리자에 게 기본적으로 합니다. 대신, 주요 추적용 참가자 (영문)에 대 한이 예약 하 고만 결과 명확 하 게 이해 이해 되 면 단기간 별로 관리자에 게 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p130">The set of permissions assigned to key vault administrators does not include the permission to delete keys. This is intentional and an important practice. Deleting encryption keys is not typically done, since doing so permanently destroys data. As a best practice, do not grant this permission to key vault administrators by default. Instead, reserve this for key vault contributors and only assign it to an administrator on a short term basis once a clear understanding of the consequences is understood.</span></span> 
  
    <span data-ttu-id="75718-p131">Office 365 조직에서 사용자에 게 이러한 사용 권한을 할당할 Azure PowerShell을 사용한 Azure 구독에 로그인 합니다. 자세한 내용은 [Azure PowerShell을 사용 하 여 로그](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75718-p131">To assign these permissions to a user in your Office 365 organization, log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
- <span data-ttu-id="75718-265">필요한 사용 권한을 할당 하려면 집합 AzureRmKeyVaultAccessPolicy cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-265">Run the Set-AzureRmKeyVaultAccessPolicy cmdlet to assign the necessary permissions.</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  <span data-ttu-id="75718-266">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-266">For example:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- <span data-ttu-id="75718-p132">**키 추적용 참가자 (영문)을** 변경할 수 있는 Azure 키 볼트에 대 한 권한을 자체 합니다. 직원 상태로 두거나, 팀에 참가 하거나 매우 드문 상황에서 키 볼트는 관리자가 합법적으로 필요가 삭제 또는 키를 복원 하는 권한이 따라 이러한 사용 권한을 변경 해야 합니다. 이 집합 키 추적용 대화에 **참가자** 역할을 부여할 주요 추적용 참가자 (영문) 요구 사항입니다. Azure 리소스 관리자를 사용 하 여이 역할을 할당할 수 있습니다. 자세한 단계에 대 한 [Azure 구독 리소스에 대 한 액세스를 관리 하려면 Use Role-Based 액세스 제어](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure)를 참조 합니다. 관리자가 구독을 만듭니다에 따라 다른 관리자가 참가자 역할에 할당 하는 기능과 함께이 액세스를 하는 암시적으로 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p132">**Key vault contributors** that can change permissions on the Azure Key Vault itself. You'll need to change these permissions as employees leave or join your team, or in the extremely rare situation that the key vault administrators legitimately need permission to delete or restore a key. This set of key vault contributors needs to be granted the **Contributor** role on your key vault. You can assign this role by using Azure Resource Manager. For detailed steps, see [Use Role-Based Access Control to manage access to your Azure subscription resources](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). The administrator who creates a subscription has this access implicitly, as well as the ability to assign other administrators to the Contributor role.</span></span>
    
- <span data-ttu-id="75718-p133">비즈니스를 위한 Exchange Online 및 Skype와 고객 키를 사용 하려는 경우에 비즈니스를 위한 Exchange Online 및 Skype을 대신 하 여 주요 추적용을 사용 하 여 Office 365에 권한을 부여 해야 합니다. 마찬가지로, 비즈니스를 위한 SharePoint Online 및 OneDrive 고객 키를 사용 하 여 비즈니스를 위한 SharePoint Online 및 OneDrive을 대신 하 여 주요 추적용을 사용 하 여 Office 365에 대 한 사용 권한을 추가 해야 합니다. Office 365에 권한을 지정 하려면 다음 구문을 사용 하 여 **집합 AzureRmKeyVaultAccessPolicy** cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p133">If you intend to use Customer Key with Exchange Online and Skype for Business, you need to give permission to Office 365 to use the key vault on behalf of Exchange Online and Skype for Business. Likewise, if you intend to use Customer Key with SharePoint Online and OneDrive for Business, you need to add permission for the Office 365 to use the key vault on behalf of SharePoint Online and OneDrive for Business. To give permission to Office 365, run the **Set-AzureRmKeyVaultAccessPolicy** cmdlet using the following syntax:</span></span> 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    <span data-ttu-id="75718-276">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-276">Where:</span></span>
    
  - <span data-ttu-id="75718-277">*vaultname* 은 만든 주요 추적용의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75718-277">*vaultname* is the name of the key vault you created.</span></span> 
    
  - <span data-ttu-id="75718-278">Exchange Online 및 비즈니스를 위한 Skype와 *Office 365 appID* 바꾸기`00000002-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="75718-278">For Exchange Online and Skype for Business, replace  *Office 365 appID* with `00000002-0000-0ff1-ce00-000000000000`</span></span>
    
  - <span data-ttu-id="75718-279">SharePoint Online 및 비즈니스용 OneDrive와 *Office 365 appID* 바꾸기`00000003-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="75718-279">For SharePoint Online and OneDrive for Business, replace  *Office 365 appID* with `00000003-0000-0ff1-ce00-000000000000`</span></span>
    
  <span data-ttu-id="75718-280">예: Exchange Online 및 Skype 비즈니스에 대 한 권한 설정:</span><span class="sxs-lookup"><span data-stu-id="75718-280">Example: Setting permissions for Exchange Online and Skype for Business:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  <span data-ttu-id="75718-281">예: SharePoint Online 및 비즈니스용 OneDrive에 대 한 사용 권한 설정</span><span class="sxs-lookup"><span data-stu-id="75718-281">Example: Setting permissions for SharePoint Online and OneDrive for Business</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a><span data-ttu-id="75718-282">설정 하 고 확인을 위해 주요 볼트 대화에서 일시 삭제</span><span class="sxs-lookup"><span data-stu-id="75718-282">Enable and then confirm soft delete on your key vaults</span></span>
<span data-ttu-id="75718-283"><a name="SoftDelete"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-283"></span></span>

<span data-ttu-id="75718-p134">신속 하 게 키를 복구할 수 있습니다 때 실수로 또는 악의적으로 삭제 된 키로 인해 확장 된 서비스 중단이 발생할 가능성이 적은 됩니다. 라고 소프트 삭제 고객 키를 사용 하면 키를 사용 하려면 먼저,이 구성을 사용 하도록 설정 해야 합니다. 부드러운 삭제를 사용 하도록 설정 백업에서 복원 하지 않고 삭제 90 일 이내 키 또는 볼트를 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p134">When you can quickly recover your keys, you are less likely to experience an extended service outage due to accidentally or maliciously deleted keys. You need to enable this configuration, referred to as Soft Delete, before you can use your keys with Customer Key. Enabling Soft Delete allows you to recover keys or vaults within 90 days of deletion without having to restore them from backup.</span></span>
  
<span data-ttu-id="75718-287">을 사용 하려면 소프트 삭제 하면 주요 볼트에서 다음이 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-287">To enable Soft Delete on your key vaults, complete these steps:</span></span>
  
1. <span data-ttu-id="75718-p135">Windows Powershell을 사용한 Azure 구독에 로그인 합니다. 자세한 내용은 [Azure PowerShell을 사용 하 여 로그](https://docs.microsoft.com/powershell/azure/authenticate-azureps)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75718-p135">Log in to your Azure subscription with Windows Powershell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span></span>
    
2. <span data-ttu-id="75718-p136">[Get AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) cmdlet을 실행 합니다. 이 예제에서는 *vaultname* 의 이름인을 사용할 수 있도록 일시 삭제 하는 주요 추적용:</span><span class="sxs-lookup"><span data-stu-id="75718-p136">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) cmdlet. In this example, *vaultname* is the name of the key vault for which you are enabling soft delete:</span></span> 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. <span data-ttu-id="75718-p137">일시 삭제 하도록 구성 된 주요 추적용 **Get AzureRmKeyVault** cmdlet을 실행 하 여 확인 합니다. 일시 삭제 제대로 키 볼트에 대 한 구성 하는 경우는 일시 삭제 사용 합니까? 속성의 **True**값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p137">Confirm soft delete is configured for the key vault by running the **Get-AzureRmKeyVault** cmdlet. If soft delete is configured properly for the key vault, then the  Soft Delete Enabled? property returns a value of **True**:</span></span> 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a><span data-ttu-id="75718-294">각 주요 추적용 중 하나를 만들거나 키를 가져오기 (영문) 하 여 키 추가</span><span class="sxs-lookup"><span data-stu-id="75718-294">Add a key to each key vault either by creating or importing a key</span></span>
<span data-ttu-id="75718-295"><a name="AddKeystoKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-295"></span></span>

<span data-ttu-id="75718-p138">두 가지 방법으로 Azure 키 추적용;에 키를 추가 하려면 키 추적용에서 직접 키를 만들거나 키를 가져올 수 있습니다. 키를 가져오기 (영문) 키가 생성 하는 방법을 통해 전체 제어를 제공 하는 동안 덜 복잡된 메서드는 키 볼트에 직접 키 만들기 (영문).</span><span class="sxs-lookup"><span data-stu-id="75718-p138">There are two ways to add keys to an Azure Key Vault; you can create a key directly in Key Vault, or you can import a key. Creating a key directly in Key Vault is the less complicated method, while importing a key provides total control over how the key is generated.</span></span>
  
<span data-ttu-id="75718-298">주요 추적용 프로그램에서 직접 키를 만들려면 [추가 AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) cmdlet를 다음과 같이 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-298">To create a key directly in your key vault, run the [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="75718-299">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-299">Where:</span></span>
  
-  <span data-ttu-id="75718-300">*vaultname* 은 키를 만들려는 주요 추적용의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75718-300">*vaultname*  is the name of the key vault in which you want to create the key.</span></span> 
    
-  <span data-ttu-id="75718-301">*키 이름* 에 새 키에 지정할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75718-301">*keyname*  is the name you want to give the new key.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="75718-p139">주요 볼트에 대해 설명한 것과 같이 유사한 명명 규칙을 사용 하 여 키 이름을 지정 합니다. 이와 같은 방식이으로 키 이름에만 표시 하는 도구에는 문자열은 자체를 설명 하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p139">Name keys using a similar naming convention as described above for key vaults. This way, in tools that show only the key name, the string is self-describing.</span></span> 
  
- <span data-ttu-id="75718-304">HSM 사용 하 여 키를 보호 하 려 한다고 지정 하는 **HSM** _대상_ 매개 변수의 값으로 지정 그렇지 않은 경우 **소프트웨어**를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-304">If you intend to protect the key with an HSM, ensure that you specify **HSM** as the value of the  _Destination_ parameter, otherwise, specify **Software**.</span></span>
    
<span data-ttu-id="75718-305">예:</span><span class="sxs-lookup"><span data-stu-id="75718-305">For example,</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="75718-306">주요 추적용 대화에 직접 키를 가져오려면, Thales nShield 하드웨어 보안 모듈을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-306">To import a key directly into your key vault, you need to have a Thales nShield Hardware Security Module.</span></span>
  
<span data-ttu-id="75718-307">일부 조직에서는이 방법을 자신의 키와이의 provenance을 설정 하는 것을 선호 메서드는 다음을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-307">Some organizations prefer this approach to establish the provenance of their keys, and the this method also provides the following:</span></span>
  
- <span data-ttu-id="75718-308">가져오기에 사용 되는 도구 세트를 생성할 키를 암호화 하는데 사용 되는 키 교환 키 (KEK) 내보낼 수 없는 Thales에서 대를 포함 하 고 Thales 하 여 제조 된는 정품 HSM 내 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75718-308">The toolset used for import includes attestation from Thales that the Key Exchange Key (KEK) that is used to encrypt the key you generate is not exportable and is generated inside a genuine HSM that was manufactured by Thales.</span></span>
    
- <span data-ttu-id="75718-p140">도구 집합을 Azure 키 추적용 보안 세계 Thales에서 제조 프로그램 정품 HSM에도 생성 된 Thales에서 대를 포함 합니다. 이 증명 Microsoft 정품 Thales 하드웨어를 사용 하 고 하 게 증명 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p140">The toolset includes attestation from Thales that the Azure Key Vault security world was also generated on a genuine HSM manufactured by Thales. This attestation proves to you that Microsoft is also using genuine Thales hardware.</span></span>
    
<span data-ttu-id="75718-p141">위의 attestations 필요한 경우 확인 하 여 보안 그룹과 확인 합니다. 주요 온-프레미스를 만들고 여 키 추적용으로 가져올 하는 자세한 단계를 [생성 하 고 Azure 키 볼트에 대 한 HSM 암호로 보호 된 키를 전송 하는 방법](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/)을 참조 하십시오. Azure 지침을 사용 하 여 각 주요 볼트에 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p141">Check with your security group to determine if the above attestations are required. For detailed steps to create a key on-premises and import it into your key vault, see [How to generate and transfer HSM-protected keys for Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Use the Azure instructions to create a key in each key vault.</span></span>
  
### <a name="check-the-recovery-level-of-your-keys"></a><span data-ttu-id="75718-314">키의 복구 수준 확인</span><span class="sxs-lookup"><span data-stu-id="75718-314">Check the recovery level of your keys</span></span>
<span data-ttu-id="75718-315"><a name="CheckKeyRecoveryLevel"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-315"></span></span>

<span data-ttu-id="75718-p142">Office 365 Azure 키 추적용 구독을 취소 하지 않으면 로설정하면 고객 키로 사용 되는 키가 사용 하도록 설정 하는 일시 삭제는 필요 합니다. 키에 복구 수준에서 조회 하 여이 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p142">Office 365 requires that the Azure Key Vault subscription is set to Do Not Cancel and that the keys used by Customer Key have soft delete enabled. You can confirm this by looking at the recovery level on your keys.</span></span>
  
<span data-ttu-id="75718-318">복구에 대 한 수준의 Azure PowerShell에서 키를 확인 하려면 다음과 같이 입력 하는 Get AzureKeyVaultKey cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-318">To check the recovery level of a key, in Azure PowerShell, run the Get-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

<span data-ttu-id="75718-319">이 항목을 검토 하 고 취소 하지 않으면 목록에 구독을 배치 하는 단계를 모두 수행 되었는지 확인 하려면 해야 _복구 수준_ 속성 값이 **복구할 수 있는 + ProtectedSubscription**아닌 다른를 반환 하 고 각 주요 볼트 프로그램에서 사용 하도록 설정 하는 일시 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-319">If the  _Recovery Level_ property returns anything other than a value of **Recoverable+ProtectedSubscription**, you will need to review this topic and ensure that you have followed all of the steps to put the subscription on the Do Not Cancel list and that you have soft delete enabled on each of your key vaults.</span></span>
  
### <a name="backup-azure-key-vault"></a><span data-ttu-id="75718-320">백업 Azure 키 볼트</span><span class="sxs-lookup"><span data-stu-id="75718-320">Backup Azure Key Vault</span></span>
<span data-ttu-id="75718-321"><a name="BackupAzureKeyVaultkeys"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-321"></span></span>

<span data-ttu-id="75718-p143">즉시 키를 하려면 만들기 또는 변경에 따라 백업을 수행 하 고 온라인 및 오프 라인 백업 복사본을 저장 합니다. 오프 라인 복사본 하지 연결 되어야 합니다를 모든 네트워크와 같은 실제 안전 또는 상업용 저장소 시설에서. 하나 이상의 사본은 백업 재해 발생 시 액세스할 수 있는 위치에 저장 되어야 합니다. 백업 blob가 주요 자료 해야 키 추적용 키 수 영구적으로 삭제 또는 복원 그렇지 않은 경우 작동 하지 않는 렌더링 하는 유일한 방법입니다. Azure 키 추적용 외부 및 Azure 키 추적용 가져온는 키를 키를 사용 하 여 고객 키에 대 한 필요한 메타 데이터는 외부 키가 있는 존재 하지 않는 때문에 대 한 백업으로 해결할 수 없는 합니다. Azure 키 추적용에서 수행한 백업만 고객 키로 복원 작업에 대해 사용할 수 있습니다. 따라서 반드시 키가 업로드 하거나 만든 후 Azure 키 추적용의 백업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p143">Immediately following creation or any change to a key, perform a backup and store copies of the backup, both online and offline. Offline copies should not be connected to any network, such as in a physical safe or commercial storage facility. At least one copy of the backup should be stored in a location that will be accessible in the event of a disaster. The backup blobs are the sole means of restoring key material should a Key Vault key be permanently destroyed or otherwise rendered inoperable. Keys that are external to Azure Key Vault and were imported to Azure Key Vault do not qualify as a backup because the metadata necessary for Customer Key to use the key does not exist with the external key. Only a backup taken from Azure Key Vault can be used for restore operations with Customer Key. Therefore, it is essential that a backup of Azure Key Vault be made once a key is uploaded or created.</span></span>
  
<span data-ttu-id="75718-329">Azure 키 추적용 키의 백업을 만들려면 다음과 같이 입력 하는 [백업 AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-329">To create a backup of an Azure Key Vault key, run the [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) cmdlet as follows:</span></span>
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

<span data-ttu-id="75718-330">출력 파일 접미사를 사용 하는지 확인 `.backup`합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-330">Ensure that your output file uses the suffix  `.backup`.</span></span>
  
<span data-ttu-id="75718-p144">이 cmdlet에서 발생 하는 출력 파일이 암호화 되 고 Azure 키 추적용 외부에서 사용할 수 없습니다. 백업을 수행한 Azure 구독에만 백업을 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p144">The output file resulting from this cmdlet is encrypted and cannot be used outside of Azure Key Vault. The backup can be restored only to the Azure subscription from which the backup was taken.</span></span>
  
> [!TIP]
> <span data-ttu-id="75718-p145">출력 파일에 대 한 추적용 이름과 키 이름의 조합을 선택 합니다. 이 파일 이름 자체를 설명 하는 변경 됩니다. 또한 백업 파일 이름 충돌 하지 않도록 확인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p145">For the output file, choose a combination of your vault name and key name. This will make the file name self-describing. It will also ensure that backup file names do not collide.</span></span> 
  
<span data-ttu-id="75718-336">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-336">For example:</span></span>
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a><span data-ttu-id="75718-337">Azure 키 추적용 구성 설정의 유효성을 검사합니다</span><span class="sxs-lookup"><span data-stu-id="75718-337">Validate Azure Key Vault configuration settings</span></span>
<span data-ttu-id="75718-338"><a name="Validateconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-338"></span></span>

<span data-ttu-id="75718-p146">선택 사항 이지만 권장 되는 DEP에 키를 사용 하기 전에 유효성 검사를 수행 합니다. 특히를 설정 하 여 키와 볼트가이 항목에 설명 된 것 외에 다른 단계를 사용 하는 경우 고객 키를 구성 하기 전에 Azure 키 추적용 리소스 상태 고 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p146">Performing validation before using keys in a DEP is optional, but highly recommended. In particular, if you use steps to set up your keys and vaults other than the ones described in this topic, you should validate the health of your Azure Key Vault resources before you configure Customer Key.</span></span>
  
<span data-ttu-id="75718-341">키를 사용 하도록 설정 하는 get, wrapKey, 및 unwrapKey 작업 있는지 확인.</span><span class="sxs-lookup"><span data-stu-id="75718-341">To verify that your keys have get, wrapKey, and unwrapKey operations enabled:</span></span>
  
<span data-ttu-id="75718-342">다음과 같이 [Get AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-342">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) cmdlet as follows:</span></span> 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

<span data-ttu-id="75718-p147">출력에서을 적절 하 게 액세스 정책에 대 한와 Exchange Online id (GUID) 또는 SharePoint Online id (GUID)를 찾습니다. 위의 권한의 모든 3 키에 사용 권한에서 표시 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p147">In the output, look for the Access Policy and for the Exchange Online identity (GUID) or the SharePoint Online identity (GUID) as appropriate. All three of the above permissions must be shown under Permissions to Keys.</span></span>
  
<span data-ttu-id="75718-345">액세스 정책 구성 올바르지 않을 경우 다음과 같이 설정 AzureRmKeyVaultAccessPolicy cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-345">If the access policy configuration is incorrect, run the Set-AzureRmKeyVaultAccessPolicy cmdlet as follows:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

<span data-ttu-id="75718-346">예: Exchange Online 및 비즈니스를 위한 Skype:</span><span class="sxs-lookup"><span data-stu-id="75718-346">For example, for Exchange Online and Skype for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

<span data-ttu-id="75718-347">예: SharePoint Online 및 비즈니스용 OneDrive:</span><span class="sxs-lookup"><span data-stu-id="75718-347">For example, for SharePoint Online and OneDrive for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

<span data-ttu-id="75718-348">다음과 같이 [Get AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) cmdlet을 실행 하 여 키에 대 한 만료 날짜 설정 되어 있지 않은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-348">To verify that an expiration date is not set for your keys run the [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

<span data-ttu-id="75718-p148">고객 키로는 만료 된 키를 사용할 수 없습니다 및 만료 된 키로 시도 하는 작업 실패 하 고 가능한 경우 서비스 중단을 초래할 됩니다. 고객 키로 사용 되는 키 만료 날짜를 갖지 않습니다 하는 것이 좋습니다. 만료 날짜, 집합을 제거할 수 없습니다 되지만 다른 날짜를 변경할 수 있습니다. 키를 설정 하는 만료 날짜가 있는 사용 해야을 하는 경우 만료 값을 12/31/9999로 변경 합니다. 만료 날짜와 함께 키 12/31/9999 Office 365 유효성 검사를 통과 하지 못합니다 외에 날짜를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p148">An expired key cannot be used by Customer Key and operations attempted with an expired key will fail, and possibly result in a service outage. We strongly recommend that keys used with Customer Key do not have an expiration date. An expiration date, once set, cannot be removed, but can be changed to a different date. If a key must be used that has an expiration date set, change the expiration value to 12/31/9999. Keys with an expiration date set to a date other than 12/31/9999 will not pass Office 365 validation.</span></span>
  
<span data-ttu-id="75718-354">12/31/9999이 아닌 값으로 설정 된 만료 날짜를 변경 하려면 다음과 같이 입력 하는 [집합 AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-354">To change an expiration date that has been set to any value other than 12/31/9999, run the [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) cmdlet as follows:</span></span> 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> <span data-ttu-id="75718-355">고객 키로 사용 하 여 암호화 키에 대해 만료 날짜를 설정 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="75718-355">Don't set expiration dates on encryption keys you use with Customer Key.</span></span> 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a><span data-ttu-id="75718-356">각 Azure 키 추적용 키에 대 한 URI를 얻으려면</span><span class="sxs-lookup"><span data-stu-id="75718-356">Obtain the URI for each Azure Key Vault key</span></span>
<span data-ttu-id="75718-357"><a name="GetKeyURI"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-357"></span></span>

<span data-ttu-id="75718-p149">한번에 주요 볼트를 설정 하는 Azure의 모든 단계를 완료 하 고 각 주요 볼트의 키에 대 한 URI를 가져오려면 다음 명령을 실행 하 여 키를 추가 합니다. 이러한 사용 해야하는 Uri를 만들고 각 DEP를 나중에 할당 하는 경우 안전한 위치에 있으므로이 정보를 저장 합니다. 각 주요 추적용에 대해 한번씩이 명령을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p149">Once you have completed all the steps in Azure to set up your key vaults and added your keys, run the following command to get the URI for the key in each key vault. You will need to use these URIs when you create and assign each DEP later, so save this information in a safe place. Remember to run this command once for each key vault.</span></span>
  
<span data-ttu-id="75718-361">Azure powershell:</span><span class="sxs-lookup"><span data-stu-id="75718-361">In Azure PowerShell:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="75718-362">Office 365: Exchange Online 및 Skype 비즈니스를 위한 고객 키를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-362">Office 365: Setting up Customer Key for Exchange Online and Skype for Business</span></span>
<span data-ttu-id="75718-363"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-363"></span></span>

<span data-ttu-id="75718-p150">시작 하기 전에 Azure 키 추적용을 설정 하는 데 필요한 작업을 완료 했는지 확인 합니다. 자세한 내용은 [Azure 키 추적용 및 고객 키에 대 한 Microsoft FastTrack에서 작업을 완료](controlling-your-data-using-customer-key.md#AzureSteps) 를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p150">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="75718-366">Exchange Online 및 Skype 비즈니스를 위한 고객 키를 설정 하려면 원격 Windows PowerShell을 사용한 Exchange Online에 연결 하 여 이러한 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-366">To set up Customer Key for Exchange Online and Skype for Business, you will need to perform these steps by remotely connecting to Exchange Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a><span data-ttu-id="75718-367">비즈니스를 위한 Exchange Online 및 Skype와 함께 사용에 대 한 데이터 암호화 정책 (DEP) 만들기</span><span class="sxs-lookup"><span data-stu-id="75718-367">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>
<span data-ttu-id="75718-368"><a name="CreateDEP4EXOSkype"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-368"></span></span>

<span data-ttu-id="75718-p151">한 DEP Azure 키 볼트에 저장 된 키 집합으로 연결 됩니다. Office 365의 사서함에는 DEP를 할당 합니다. 다음 office 365 정책에서 식별 된 키를 사용 하 여 사서함을 암호화 됩니다. DEP를 만들려면 이전에 가져온 키 추적용 Uri 해야 합니다. 대 한 자세한 내용은 [가져오는 각 Azure 키 추적용 키에 대 한 URI를](controlling-your-data-using-customer-key.md#GetKeyURI) 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75718-p151">A DEP is associated with a set of keys stored in Azure Key Vault. You assign a DEP to a mailbox in Office 365. Office 365 will then use the keys identified in the policy to encrypt the mailbox. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="75718-p152">기억! DEP를 만들 때 서로 다른 두 Azure 키 볼트에 있는 두 키를 지정 합니다. 이러한 키 지리적으로 분산 중복 되도록 별도 두 Azure 영역에 있는 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p152">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="75718-377">DEP를 만들려면 다음이 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="75718-377">To create the DEP, follow these steps:</span></span>
  
1. <span data-ttu-id="75718-378">로컬 컴퓨터에서 Windows PowerShell을 열고 다음 명령을 실행 하 여 [Exchange Online PowerShell에 연결](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) 하 여 Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-378">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [connect to Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) by opening Windows PowerShell and running the following command.</span></span> 
    
   ```
   $UserCredential = Get-Credential
   ```

2. <span data-ttu-id="75718-379">Windows PowerShell 자격 증명 요청 대화 상자에서 작업 시간을 입력 또는 계정 정보를 학교, **확인**을 클릭 한 후 다음 명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-379">In the Windows PowerShell Credential Request dialog box, enter your work or school account information, click **OK**, and then enter the following command.</span></span> 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. <span data-ttu-id="75718-380">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-380">Run the following command.</span></span>
    
   ```
   Import-PSSession $Session
   ```

4. <span data-ttu-id="75718-381">DEP를 만들려면 다음 명령을 입력 하 여 새로 DataEncryptionPolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-381">To create a DEP, use the New-DataEncryptionPolicy cmdlet by typing the following command.</span></span>
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   <span data-ttu-id="75718-382">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-382">Where:</span></span>
    
   -  <span data-ttu-id="75718-p153">*PolicyName* 은 정책에 대해 사용 하려는 이름입니다. 이름에 공백을 포함할 수 없습니다. 예: USA_mailboxes 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p153">*PolicyName*  is the name you want to use for the policy. Names cannot contain spaces. For example, USA_mailboxes.</span></span> 
    
   -  <span data-ttu-id="75718-p154">*PolicyDescription* 은 정책입니다 기억할 수 있는 정책 사용자가 친숙 한 설명입니다. 설명에 공백을 포함할 수 있습니다. 미국 및 해당 지역에서 사서함에 대 한 키를 루트 예입니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p154">*PolicyDescription*  is a user friendly description of the policy that will help you remember what the policy is for. You can include spaces in the description. For example, Root key for mailboxes in USA and its territories.</span></span> 
    
   -  <span data-ttu-id="75718-p155">*KeyVaultURI1* 은 정책에서 첫번째 키에 대 한 URI입니다. 예, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p155">*KeyVaultURI1*  is the URI for the first key in the policy. For example, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span></span> 
    
   -  <span data-ttu-id="75718-p156">*KeyVaultURI2* 은 정책에서 두번째 키에 대 한 URI입니다. 예, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02합니다. 쉼표 및 공백을 두 Uri를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p156">*KeyVaultURI2*  is the URI for the second key in the policy. For example, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Separate the two URIs by a comma and a space.</span></span> 
    
   <span data-ttu-id="75718-394">예제:</span><span class="sxs-lookup"><span data-stu-id="75718-394">Example:</span></span>
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a><span data-ttu-id="75718-395">사서함에는 DEP 할당</span><span class="sxs-lookup"><span data-stu-id="75718-395">Assign a DEP to a mailbox</span></span>
<span data-ttu-id="75718-396"><a name="assignDEPtomailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-396"></span></span>

<span data-ttu-id="75718-p157">Set-mailbox cmdlet을 사용 하 여 사서함에는 DEP를 할당 합니다. Office 365는 종속에 지정 된 키가 있는 사서함을 암호화할 수에 정책을 할당 한 후</span><span class="sxs-lookup"><span data-stu-id="75718-p157">Assign the DEP to a mailbox by using the Set-Mailbox cmdlet. Once you assign the policy, Office 365 can encrypt the mailbox with the key designated in the DEP.</span></span>
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

<span data-ttu-id="75718-p158">여기서 *MailboxIdParameter* 사서함을 지정 합니다. Set-mailbox cmdlet에 대 한 자세한 내용은 [Set-mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75718-p158">Where *MailboxIdParameter* specifies a mailbox. For more information about the Set-Mailbox cmdlet, see [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span></span>
  
### <a name="validate-mailbox-encryption"></a><span data-ttu-id="75718-401">사서함 암호화의 유효성을 검사합니다</span><span class="sxs-lookup"><span data-stu-id="75718-401">Validate mailbox encryption</span></span>
<span data-ttu-id="75718-402"><a name="validatemailboxencryption"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-402"></span></span>

<span data-ttu-id="75718-p159">사서함을 암호화 다소 시간이 걸릴 수 있습니다. 1 시간 정책 할당에 대 한 사서함도 완료 해야 하나의 데이터베이스에서 다른 위치로 이동 서비스의 사서함을 암호화할 수 있습니다. 72 시간 후는 DEP를 변경 하거나 사서함에는 DEP를 할당 처음으로 암호화의 유효성을 검사 하려고 하기 전에 대기 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p159">Encrypting a mailbox can take some time. For first time policy assignment, the mailbox must also complete the move from one database to another before the service can encrypt the mailbox. We recommend that you wait 72 hours before you attempt to validate encryption after you change a DEP or the first time you assign a DEP to a mailbox.</span></span>
  
<span data-ttu-id="75718-406">Get-mailboxstatistics cmdlet을 사용 하 여 사서함 암호화 하는 경우를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-406">Use the Get-MailboxStatistics cmdlet to determine if a mailbox is encrypted.</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

<span data-ttu-id="75718-407">IsEncrypted 속성은 사서함 암호화 되지 않은 경우 값이 **true** 이면 사서함은 암호화와 값이 **false** 를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-407">The IsEncrypted property returns a value of **true** if the mailbox is encrypted and a value of **false** if the mailbox is not encrypted.</span></span> 

<span data-ttu-id="75718-p160">사서함 이동이 완료 시간으로는 처음에 대 한 DEP이 지정 된 사서함 수는 사서함의 크기에 따라 달라 집니다. DEP를 할당 하는 사서함 시간부터 1 주일 후 암호화 되지 않은 경우, New-moverequest cmdlet을 사용 하 여 암호화 되지 않은 사서함에 대 한 사서함 이동을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p160">The time to complete mailbox moves depends on the number of mailboxes to which you assign a DEP for the first time, as well as the size of the mailboxes. If the mailboxes have not been encrypted after a week from the time you assigned the DEP, initiate a mailbox move for the unencrypted mailboxes by using the New-MoveRequest cmdlet.</span></span>

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a><span data-ttu-id="75718-410">Office 365: SharePoint Online 및 비즈니스용 OneDrive에 대 한 고객 키를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-410">Office 365: Setting up Customer Key for SharePoint Online and OneDrive for Business</span></span>
<span data-ttu-id="75718-411"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-411"></span></span>

<span data-ttu-id="75718-p161">시작 하기 전에 Azure 키 추적용을 설정 하는 데 필요한 작업을 완료 했는지 확인 합니다. 자세한 내용은 [Azure 키 추적용 및 고객 키에 대 한 Microsoft FastTrack에서 작업을 완료](controlling-your-data-using-customer-key.md#AzureSteps) 를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p161">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="75718-414">SharePoint Online 및 비즈니스용 OneDrive에 대 한 고객 키를 설정 하려면 원격 Windows PowerShell을 사용한 SharePoint Online에 연결 하 여 이러한 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-414">To set up Customer Key for SharePoint Online and OneDrive for Business, you will need to perform these steps by remotely connecting to SharePoint Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a><span data-ttu-id="75718-415">비즈니스 지리적으로 분산에 대 한 각 SharePoint Online 및 OneDrive에 대 한 데이터 암호화 정책 (DEP) 만들기</span><span class="sxs-lookup"><span data-stu-id="75718-415">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>
<span data-ttu-id="75718-416"><a name="CreateDEP4SPOODfB"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-416"></span></span>

<span data-ttu-id="75718-p162">한 DEP Azure 키 볼트에 저장 된 키 집합으로 연결 됩니다. 지리적으로 분산이 라고도 하는 하나의 지리적 위치에 데이터를 모두에 DEP를 적용 합니다. (현재 미리 보기)에서 Office 365의 다중-지리적으로 분산 기능을 사용 하는 경우에 지리적으로 분산 당 하나의 DEP를 만들 수 있습니다. 다중-지리적으로 분산을 사용 하지 않는 경우에 비즈니스를 위한 SharePoint Online 및 OneDrive 사용 하기 위한 Office 365에서 하나의 DEP를 만들 수 있습니다. 다음 office 365는 DEP에서 식별 된 키를 사용 하 여 해당 지리적으로 분산에서 데이터를 암호화 됩니다. DEP를 만들려면 이전에 가져온 키 추적용 Uri 해야 합니다. 대 한 자세한 내용은 [가져오는 각 Azure 키 추적용 키에 대 한 URI를](controlling-your-data-using-customer-key.md#GetKeyURI) 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75718-p162">A DEP is associated with a set of keys stored in Azure Key Vault. You apply a DEP to all of your data in one geographic location, also called a geo. If you use the multi-geo feature of Office 365 (currently in Preview), you can create one DEP per geo. If you are not using multi-geo, you can create one DEP in Office 365 for use with SharePoint Online and OneDrive for Business. Office 365 will then use the keys identified in the DEP to encrypt your data in that geo. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="75718-p163">기억! DEP를 만들 때 서로 다른 두 Azure 키 볼트에 있는 두 키를 지정 합니다. 이러한 키 지리적으로 분산 중복 되도록 별도 두 Azure 영역에 있는 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p163">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="75718-427">DEP를 만들려면 Windows PowerShell을 사용 하 여 원격으로 SharePoint Online에 연결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-427">To create a DEP, you need to remotely connect to SharePoint Online by using Windows PowerShell.</span></span>
  
1. <span data-ttu-id="75718-428">로컬 컴퓨터에서 [SharePoint Online Powershell에 연결](https://technet.microsoft.com/library/fp161372.aspx)하 여 Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-428">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [Connect to SharePoint Online Powershell](https://technet.microsoft.com/library/fp161372.aspx).</span></span>
    
2. <span data-ttu-id="75718-429">Microsoft SharePoint Online 관리 셸에서 다음과 같이 [레지스터 SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-429">In the Microsoft SharePoint Online Management Shell, run the [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) cmdlet as follows:</span></span> 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   <span data-ttu-id="75718-p164">DEP를 등록 하는 경우 암호화는 지리적으로 분산의 데이터를 시작 합니다. 이 다소 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p164">When you register the DEP, encryption begins on the data in the geo. This can take some time.</span></span>
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a><span data-ttu-id="75718-432">암호화 그룹 사이트, 팀 사이트 및 비즈니스용 OneDrive의 유효성을 검사합니다</span><span class="sxs-lookup"><span data-stu-id="75718-432">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>
<span data-ttu-id="75718-433"><a name="validateencryptionSPO"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-433"></span></span>

<span data-ttu-id="75718-434">다음과 같이 Get SPODataEncryptionPolicy cmdlet을 실행 하 여 암호화의 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-434">You can check on the status of encryption by running the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

<span data-ttu-id="75718-435">이 cmdlet의 출력에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75718-435">The output from this cmdlet includes:</span></span>
  
- <span data-ttu-id="75718-436">기본 키의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="75718-436">The URI of the primary key.</span></span>
    
- <span data-ttu-id="75718-437">보조 키의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="75718-437">The URI of the secondary key.</span></span>
    
- <span data-ttu-id="75718-p165">지리적으로 분산에 대 한 암호화 상태입니다. 가능한 상태에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p165">The encryption status for the geo. Possible states include:</span></span>
    
  - <span data-ttu-id="75718-440">**등록을 취소할:** 고객 키 암호화 아직 적용 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-440">**Unregistered:** Customer Key encryption has not yet been applied.</span></span> 
    
  - <span data-ttu-id="75718-p166">**등록:** 고객 키 암호화 적용 된 및 프로그램 파일을 암호화 하는 과정입니다. 프로그램 지리적으로 분산이이 상태에 있으면 화면이 표시 됩니다 정보에는 지리적으로 분산의 사이트는 몇 % 완료 암호화 진행 상태를 모니터링할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p166">**Registering:** Customer Key encryption has been applied and your files are in the process of being encrypted. If your geo is in this state, you'll also be shown information on what percentage of sites in the geo are complete so that you can monitor encryption progress.</span></span> 
    
  - <span data-ttu-id="75718-443">**등록:** 고객 키 암호화를 적용 하 고 모든 사이트의 모든 파일을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-443">**Registered:** Customer Key encryption has been applied, and all files in all sites have been encrypted.</span></span> 
    
  - <span data-ttu-id="75718-p167">**롤링:** 주요 roll 진행중에서입니다. 프로그램 지리적으로 분산이이 상태에 있으면 화면이 표시 됩니다 정보 사이트는 몇 % 주요 roll 작업 진행 상태를 모니터링할 수 있도록 완료에 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p167">**Rolling:** A key roll is in progress. If your geo is in this state, you'll also be shown information on what percentage of sites have completed the key roll operation so that you can monitor progress.</span></span> 
    
## <a name="managing-customer-key-for-office-365"></a><span data-ttu-id="75718-446">Office 365에 대 한 고객 키 관리</span><span class="sxs-lookup"><span data-stu-id="75718-446">Managing Customer Key for Office 365</span></span>
<span data-ttu-id="75718-447"><a name="ManageCustomerKey"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-447"></span></span>

<span data-ttu-id="75718-448">고객 키에서 Office 365에 대 한 설정한 후에 이러한 추가 관리 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-448">After you've set up Customer Key for Office 365, you can perform these additional management tasks.</span></span>
  
- [<span data-ttu-id="75718-449">Azure 키 추적용 키 복원</span><span class="sxs-lookup"><span data-stu-id="75718-449">Restore Azure Key Vault keys</span></span>](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [<span data-ttu-id="75718-450">롤링 또는 고객 키로 사용 된 자격 증명 Azure 키 모음에서 키를 회전 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-450">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [<span data-ttu-id="75718-451">주요 추적용 사용 권한 관리</span><span class="sxs-lookup"><span data-stu-id="75718-451">Manage key vault permissions</span></span>](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [<span data-ttu-id="75718-452">사서함에 할당 된 DEP를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-452">Determine the DEP assigned to a mailbox</span></span>](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a><span data-ttu-id="75718-453">Azure 키 추적용 키 복원</span><span class="sxs-lookup"><span data-stu-id="75718-453">Restore Azure Key Vault keys</span></span>
<span data-ttu-id="75718-454"><a name="RestoreAzureKeyVaultKeys"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-454"></span></span>

<span data-ttu-id="75718-p168">복원을 수행 하기 전에 일시 삭제 하 여 제공 하는 복구 기능을 사용 합니다. 고객 키로 사용 되는 모든 키가 사용 하도록 설정 하는 일시 삭제 해야할 필요 합니다. 일시 삭제 휴지통 처럼 작동 하 고 복원할 필요 없이 최대 90 일에 대 한 복구를 허용 합니다. 복원 예: 키 또는 키 추적용 손실 되는 경우 아주 또는 특수 한 경우에서에 필요 해야 합니다. 고객 키로 사용에 대 한 키를 복원 해야 하는 경우 Azure powershell에서 cmdlet을 실행 복원 AzureKeyVaultKey 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p168">Before performing a restore, use the recovery capabilities provided by soft delete. All keys that are used with Customer Key are required to have soft delete enabled. Soft delete acts like a recycle bin and allows recovery for up to 90 days without the need to restore. Restore should only be required in extreme or unusual circumstances, for example if the key or key vault is lost. If you must restore a key for use with Customer Key, in Azure PowerShell, run the Restore-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

<span data-ttu-id="75718-460">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-460">For example:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

<span data-ttu-id="75718-p169">이름이 같은 키 키 볼트에 이미 존재 하는 경우 복원 작업이 실패 합니다. 복원 AzureKeyVaultKey 모든 주요 버전 및 키 이름을 포함 하는 키에 대 한 모든 메타 데이터를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p169">If a key with the same name already exists in the key vault, the restore operation will fail. Restore-AzureKeyVaultKey restores all key versions and all metadata for the key including the key name.</span></span>
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a><span data-ttu-id="75718-463">롤링 또는 고객 키로 사용 된 자격 증명 Azure 키 모음에서 키를 회전 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-463">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>
<span data-ttu-id="75718-464"><a name="RollCKkey"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-464"></span></span>

<span data-ttu-id="75718-p170">키 롤링 Azure 키 추적용 중 하나 또는 고객 키가 필요 하지 않습니다. 또한 HSM로 보호 되는 키를 위태롭게 할 가능성 거의 모든 수는 없습니다. 루트 키가 악의적인 작업자의 소유 하는 경우에 없는 적절 한 방법을 사용 하 여 Office 365 코드만 사용 하는 방법을 알고 있으므로 데이터를 암호 해독의 방법이 있습니다. 그러나 키 롤링 고객 키에 의해 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p170">Rolling keys is not required by either Azure Key Vault or by Customer Key. In addition, keys that are protected with an HSM are virtually impossible to compromise. Even if a root key were in the possession of a malicious actor there is no feasible means of using it to decrypt data, since only Office 365 code knows how to use it. However, rolling a key is supported by Customer Key.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="75718-p171">확인란의 선택을 취소 기술 이유 존재 하지 않거나 규정 준수 요구 사항을 규정 키 롤 해야할 때 고객 키를 사용 하는 암호화 키를 롤만 합니다. 또한 추가 되거나 정책과 연결 된 모든 키를 삭제 하지 마십시오. 키가 있는지를 배포할 때 콘텐츠 암호화 이전 키를 사용 합니다. 등 활성 사서함 다시 암호화 됩니다 자주, 비활성화 하는 동안 이전 키로는 암호화 끊어지고 비활성화 된 사서함 수 있습니다. SharePoint Online에서는 백업 콘텐츠 복원 및 복구 목적을 위해 계속 되는 경우도 있으므로 오래 된 키를 사용 하 여 보관 된 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p171">Only roll an encryption key that you use with Customer Key when a clear technical reason exists or a compliance requirement dictates that you have to roll the key. In addition, do not delete any keys that are or were associated with policies. When you roll your keys, there will be content encrypted with the previous keys. For example, while active mailboxes will be re-encrypted frequently, inactive, disconnected, and disabled mailboxes may still be encrypted with the previous keys. SharePoint Online performs backup of content for restore and recovery purposes, so there may still be archived content using older keys. </span></span><br/> <span data-ttu-id="75718-p172">데이터의 안전을 위해, SharePoint Online를 선택 하면 둘 이상의 키 롤 작업 한번에 진행에서 되도록 합니다. 첫번째 주요 roll 작업을 대기 해야 키 볼트에 키의 모두 롤 하려는 경우 완벽 하 게 완료 합니다. 중요 하지 않은 있도록 서로 다른 간격 주요 roll 작업을 분산 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p172">To ensure the safety of your data, SharePoint Online will allow no more than one Key Roll operation to be in progress at a time. If you want to roll both of the keys in a key vault, you'll need to wait for the first key roll operation to fully complete. Our recommendation is to stagger your key roll operations at different intervals, so that this is not an issue.</span></span> 
  
<span data-ttu-id="75718-p173">기존 키의 새 버전을 요청 하는 키를 배포할 때 합니다. 기존 키의 새 버전을 요청 하기 위해 키를 처음부터 만들 때 사용한 동일한 구문을 사용 하 여 [추가 AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey)동일한 cmdlet은를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p173">When you roll a key, you are requesting a new version of an existing key. In order to request a new version of an existing key, you use the same cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), with the same syntax that you used to create the key in the first place.</span></span>
  
<span data-ttu-id="75718-479">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-479">For example:</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

<span data-ttu-id="75718-p174">이 예제에서는 **Contoso O365EX-NA VaultA1** 볼트에 이미 **Contoso-O365EX-NA-VaultA1-Key001** 라는 키 존재 하므로 새로운 주요 버전 생성 됩니다. 새 키 버전을 추가 하는 작업입니다. 이 작업 키의 버전 기록에서 이전 키 버전을 유지 하는 이전에 해당 키를 사용 하 여 암호화 된 데이터의 암호를 해독할 수 계속 되도록 합니다. 롤링는 DEP와 연결 된 모든 키를 완료 한 후 다음 고객 키 새 키를 사용 하 여 시작 되도록는 추가 cmdlet을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p174">In this example, since a key named **Contoso-O365EX-NA-VaultA1-Key001** already exists in the **Contoso-O365EX-NA-VaultA1** vault, a new key version will be created. The operation adds a new key version. This operation preserves the previous key versions in the key's version history, so that data previously encrypted with that key can still be decrypted. Once you have completed rolling any key that is associated with a DEP, you must then run an additional cmdlet to ensure Customer Key begins using the new key.</span></span> 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="75718-484">Exchange Online 및 비즈니스를 위한 Skype 롤 또는 Azure 키 볼트에 키를 회전 한 후 새 키를 사용 하 여 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="75718-484">Enable Exchange Online and Skype for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="75718-485">중 하나를 배포할 때 비즈니스를 위한 Exchange Online 및 Skype와 사용 되는 DEP와 관련 된 Azure 키 추적용 키는 DEP를 업데이트 하 고 새 키를 사용 하 여 시작 하려면 Office 365를 사용 하도록 설정 하려면 다음 명령을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-485">When you roll either of the Azure Key Vault keys associated with a DEP used with Exchange Online and Skype for Business, you must run the following command to update the DEP and enable Office 365 to start using the new key.</span></span>
  
<span data-ttu-id="75718-486">다음과 같이 설정 DataEncryptionPolicy cmdlet을 실행 하는 Office 365에서 사서함을 암호화 하려면 새 키를 사용 하 여 고객 키에 지시 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-486">To instruct Customer Key to use the new key to encrypt mailboxes in Office 365 run the Set-DataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

<span data-ttu-id="75718-p175">48 시간 내에서 활성 사서함이이 정책을 사용 하 여 암호화 된 업데이트 된 키와 관련 됩니다. 사서함에 대 한 DataEncryptionPolicyID 속성에 대 한 값을 확인 하 [는 사서함에 할당 된 DEP 결정](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) 의 단계에 따라 합니다. 이 속성에 대 한 값이 업데이트 된 키가 적용 된 후 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p175">Within 48 hours, the active mailboxes encrypted using this policy will become associated with the updated key. Use the steps in [Determine the DEP assigned to a mailbox](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) to check the value for the DataEncryptionPolicyID property for the mailbox. The value for this property will change once the updated key has been applied.</span></span> 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="75718-490">SharePoint Online 및 비즈니스용 OneDrive 롤 또는 Azure 키 볼트에 키를 회전 한 후 새 키를 사용 하 여 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="75718-490">Enable SharePoint Online and OneDrive for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="75718-491">중 하나를 배포할 때 비즈니스를 위한 SharePoint Online 및 OneDrive 사용 하는 한 DEP와 관련 된 Azure 키 추적용 키는 DEP를 업데이트 하 고 새 키를 사용 하 여 시작 하려면 Office 365를 사용 하도록 설정 하려면 [업데이트 SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) cmdlet을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-491">When you roll either of the Azure Key Vault keys associated with a DEP used with SharePoint Online and OneDrive for Business, you must run the [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) cmdlet to update the DEP and enable Office 365 to start using the new key.</span></span> 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

<span data-ttu-id="75718-p176">SharePoint Online 및 비즈니스용 OneDrive에 대 한 주요 roll 작업이 시작 됩니다. 이 작업은 직접 실행 하지 않습니다. 작업 롤 키의 진행률을 보려면 다음과 같이 입력 하는 Get SPODataEncryptionPolicy cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p176">This will start the key roll operation for SharePoint Online and OneDrive for Business. This action is not immediate. To see the progress of the key roll operation, run the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a><span data-ttu-id="75718-495">주요 추적용 사용 권한 관리</span><span class="sxs-lookup"><span data-stu-id="75718-495">Manage key vault permissions</span></span>
<span data-ttu-id="75718-496"><a name="Managekeyvaultperms"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-496"></span></span>

<span data-ttu-id="75718-p177">여러 cmdlet을 사용할 수 있는 확인 하 고 필요한 경우 제거 키 추적용 사용 권한 수 있도록 하는 합니다. 직원이 팀을 떠날 때 사용 권한, 예를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p177">Several cmdlets are available that enable you to view and, if necessary, remove key vault permissions. You might need to remove permissions, for example, when an employee leaves the team.</span></span>
  
<span data-ttu-id="75718-499">주요 추적용 사용 권한을 보려면, Get-AzureRmKeyVault cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-499">To view key vault permissions, run the Get-AzureRmKeyVault cmdlet:</span></span>
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

<span data-ttu-id="75718-500">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-500">For example:</span></span>
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

<span data-ttu-id="75718-501">관리자의 사용 권한을 제거 하려면 제거 AzureRmKeyVaultAccessPolicy cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-501">To remove an administrator's permissions, run the Remove-AzureRmKeyVaultAccessPolicy cmdlet:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

<span data-ttu-id="75718-502">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="75718-502">For example:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a><span data-ttu-id="75718-503">사서함에 할당 된 DEP를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-503">Determine the DEP assigned to a mailbox</span></span>
<span data-ttu-id="75718-504"><a name="DeterminemailboxDEP"> </a></span><span class="sxs-lookup"><span data-stu-id="75718-504"></span></span>

<span data-ttu-id="75718-p178">사서함에 할당 된 DEP를 확인 하려면 Get-mailboxstatistics cmdlet을 사용 합니다. Cmdlet은 고유 식별자 (GUID)를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-p178">To determine the DEP assigned to a mailbox, use the Get-MailboxStatistics cmdlet. The cmdlet returns a unique identifier (GUID).</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

<span data-ttu-id="75718-p179">여기서 *GeneralMailboxOrMailUserIdParameter* 사서함을 지정 합니다. Get-mailboxstatistics cmdlet에 대 한 자세한 내용은 [Get-mailboxstatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75718-p179">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox. For more information about the Get-MailboxStatistics cmdlet, see [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span></span>
  
<span data-ttu-id="75718-509">다음 cmdlet를 실행 하 여 할당 된 사서함을 DEP의 이름을 확인 하는 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75718-509">Use the GUID to find out the friendly name of the DEP to which the mailbox is assigned by running the following cmdlet.</span></span>
  
```
Get-DataEncryptionPolicy <GUID>
```

<span data-ttu-id="75718-510">여기서 *GUID* 는 이전 단계에서 Get-mailboxstatistics cmdlet에 의해 반환 되는 GUID입니다.</span><span class="sxs-lookup"><span data-stu-id="75718-510">Where *GUID* is the GUID returned by the Get-MailboxStatistics cmdlet in the previous step.</span></span> 
  

