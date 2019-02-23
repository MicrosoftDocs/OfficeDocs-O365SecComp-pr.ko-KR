---
title: 고객 키를 사용하여 Office 365에서 데이터 제어
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 8/1/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
ms.collection:
- M365-security-compliance
description: Exchange Online, 비즈니스용 Skype, SharePoint Online 및 비즈니스용 OneDrive에 대 한 Office 365의 고객 키를 설정 하는 방법을 알아봅니다. 고객 키를 사용 하 여 조직의 암호화 키를 제어 하 고 Office 365을 구성 하 여 Microsoft의 데이터 센터에 있는 휴지 상태에 있는 사용자에 대 한 정보를 암호화 합니다.
ms.openlocfilehash: a14a213951bc87e4106e150c88c6b1461a5e685e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218758"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a><span data-ttu-id="2ecad-104">고객 키를 사용하여 Office 365에서 데이터 제어</span><span class="sxs-lookup"><span data-stu-id="2ecad-104">Controlling your data in Office 365 using Customer Key</span></span>

<span data-ttu-id="2ecad-p102">고객 키를 사용 하 여 조직의 암호화 키를 제어 하 고 Microsoft 데이터 센터의 휴지 상태에서 데이터를 암호화 하는 데 사용 하도록 Office 365를 구성 합니다. 휴지 상태의 데이터에는 SharePoint online 및 비즈니스용 OneDrive에 저장 된 사서함 및 파일에 저장 되는 Exchange Online 및 비즈니스용 Skype의 데이터가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p102">With Customer Key, you control your organization's encryption keys and then configure Office 365 to use them to encrypt your data at rest in Microsoft's data centers. Data at rest includes data from Exchange Online and Skype for Business that is stored in mailboxes and files that are stored in SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="2ecad-p103">Office 365에 대해 고객 키를 사용 하려면 먼저 Azure를 설정 해야 합니다. 이 항목에서는 필요한 Azure 리소스를 만들고 구성 하기 위해 수행 해야 하는 단계를 설명 하 고 Office 365에서 고객 키를 설정 하는 단계를 제공 합니다. Azure 설치를 완료 한 후에는 조직의 사서함과 파일에 할당할 정책 및 키를 결정 합니다. 정책을 할당 하지 않을 사서함과 파일은 Microsoft에서 제어 및 관리 하는 암호화 정책을 사용 합니다. 고객 키에 대 한 자세한 내용은 또는 일반 개요를 보려면 [customer key for Office 365 FAQ](service-encryption-with-customer-key-faq.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p103">You must set up Azure before you can use Customer Key for Office 365. This topic describes the steps you need to follow to create and configure the required Azure resources and then provides the steps for setting up Customer Key in Office 365. After you have completed Azure setup, you determine which policy, and therefore, which keys, to assign to mailboxes and files in your organization. Mailboxes and files for which you don't assign a policy will use encryption policies that are controlled and managed by Microsoft. For more information about Customer Key, or for a general overview, see the [Customer Key for Office 365 FAQ](service-encryption-with-customer-key-faq.md).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2ecad-p104">이 항목의 모범 사례를 따르는 것이 좋습니다. 이를 **팁** 및 **중요**로 지칭 합니다. 고객 키를 사용 하 여 전체 조직에 해당 하는 범위를 갖는 루트 암호화 키를 제어할 수 있습니다. 즉, 이러한 키를 사용한 실수에 큰 영향을 줄 수 있으며 서비스 중단 또는 irrevocable 데이터 손실을 초래할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p104">We strongly recommend that you follow the best practices in this topic. These are called out as **TIP** and **IMPORTANT**. Customer Key gives you control over root encryption keys whose scope can be as large as your entire organization. This means that mistakes made with these keys can have a broad impact and may result in service interruptions or irrevocable loss of your data.</span></span> 
  
## <a name="before-you-begin-setting-up-customer-key"></a><span data-ttu-id="2ecad-116">Customer 키 설정을 시작 하기 전에</span><span class="sxs-lookup"><span data-stu-id="2ecad-116">Before you begin setting up Customer Key</span></span>
<span data-ttu-id="2ecad-117"><a name="Beforeyoustart"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-117"></span></span>

<span data-ttu-id="2ecad-p105">시작 하기 전에 조직에 적합 한 라이선스를가지고 있는지 확인 합니다. office 365의 고객 키가 office 365 E5 또는 Advanced 준수 SKU에 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p105">Before you get started, be sure you have the appropriate licensing for your organization. Customer Key in Office 365 is offered in Office 365 E5 or the Advanced Compliance SKU.</span></span>
  
<span data-ttu-id="2ecad-p106">그런 다음이 항목의 개념과 절차를 이해 하려면 [Azure 키 보관소](https://azure.microsoft.com/en-us/documentation/services/key-vault/) 설명서를 검토 해야 합니다. 또한 Azure에서 사용 되는 용어 (예: [테 넌 트](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant))에 익숙해지는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p106">Then, to understand the concepts and procedures in this topic, you should review the [Azure Key Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) documentation. Also, become familiar with the terms used in Azure, for example, [tenant](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span></span>
  
<span data-ttu-id="2ecad-122">설명서를 포함 하 여 고객 키에 대 한 의견을 제공 하려면 아이디어, 제안 사항 및 전망을 customerkeyfeedback@microsoft.com에 게 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-122">To provide feedback on Customer Key, including the documentation, send your ideas, suggestions and perspectives to customerkeyfeedback@microsoft.com.</span></span>
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a><span data-ttu-id="2ecad-123">Office 365에 대 한 고객 키 설정 개요</span><span class="sxs-lookup"><span data-stu-id="2ecad-123">Overview of setting up Customer Key for Office 365</span></span>
<span data-ttu-id="2ecad-124"><a name="Overview"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-124"></span></span>

<span data-ttu-id="2ecad-p107">고객 키를 설정 하려면 다음 작업을 완료 합니다. 이 항목의 나머지 부분에서는 각 작업에 대 한 자세한 지침을 제공 하거나 프로세스의 각 단계에 대 한 추가 정보로 연결 되는 링크에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p107">To set up Customer Key you will complete these tasks. The rest of this topic provides detailed instructions for each task, or links out to more information for each step in the process.</span></span>
  
<span data-ttu-id="2ecad-127">**Azure 및 Microsoft fasttrack:**</span><span class="sxs-lookup"><span data-stu-id="2ecad-127">**In Azure and Microsoft FastTrack:**</span></span>
  
<span data-ttu-id="2ecad-p108">이러한 작업의 대부분은 Azure PowerShell에 원격으로 연결 하 여 완료 합니다. 최상의 결과를 위해 Azure PowerShell의 버전 4.4.0 이상을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p108">You will complete most of these tasks by remotely connecting to Azure PowerShell. For best results, use version 4.4.0 or later of Azure PowerShell.</span></span>
  
- [<span data-ttu-id="2ecad-130">두 개의 새 Azure 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-130">Create two new Azure subscriptions</span></span>](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [<span data-ttu-id="2ecad-131">필수 보존 기간을 사용 하도록 Azure 구독 등록</span><span class="sxs-lookup"><span data-stu-id="2ecad-131">Register Azure subscriptions to use a mandatory retention period</span></span>](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    <span data-ttu-id="2ecad-132">등록에는 영업일 중 근무일까지 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-132">Registration can take from one to five business days.</span></span>
    
- [<span data-ttu-id="2ecad-133">Office 365에 대 한 고객 키를 정품 인증 하기 위한 요청 제출</span><span class="sxs-lookup"><span data-stu-id="2ecad-133">Submit a request to activate Customer Key for Office 365</span></span>](controlling-your-data-using-customer-key.md#FastTrack)
    
    <span data-ttu-id="2ecad-p109">새로운 두 Azure 구독을 만든 후에는 Microsoft fasttrack 포털에서 호스팅되는 웹 양식을 완료 하 여 해당 하는 고객 키 제공 요청을 제출 해야 합니다. **fasttrack 팀은 고객 키에 대 한 지원을 제공 하지 않습니다. Office는 fasttrack 포털을 사용 하 여 양식을 전송 하 고 고객 키에 대 한 관련 서비스를 추적 하는 데 도움이 됩니다**.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p109">Once you've created the two new Azure subscriptions, you'll need to submit the appropriate Customer Key offer request by completing a web form that is hosted in the Microsoft FastTrack portal. **The FastTrack team doesn't provide assistance with Customer Key. Office simply uses the FastTrack portal to allow you to submit the form and to help us track the relevant offers for Customer Key**.</span></span>
  
<span data-ttu-id="2ecad-p110">고객 키 제안을 제출 하면 Microsoft에서 요청을 검토 하 고 나머지 설치 작업을 계속 진행할 수 있을 때 사용자에 게이를 알립니다. 이 프로세스에는 최대 5 일이 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p110">Once you have submitted a Customer Key offer, Microsoft reviews your request and notifies you when you can proceed with the rest of the setup tasks. This process can take up to five business days.</span></span>
    
- [<span data-ttu-id="2ecad-138">각 구독에 프리미엄 Azure 키 자격 증명 모음 만들기</span><span class="sxs-lookup"><span data-stu-id="2ecad-138">Create a premium Azure Key Vault in each subscription</span></span>](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [<span data-ttu-id="2ecad-139">각 키 자격 증명 모음에 사용 권한 할당</span><span class="sxs-lookup"><span data-stu-id="2ecad-139">Assign permissions to each key vault</span></span>](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [<span data-ttu-id="2ecad-140">키 자격 증명 모음에서 일시 삭제를 사용 하도록 설정 하 고 확인</span><span class="sxs-lookup"><span data-stu-id="2ecad-140">Enable and then confirm soft delete on your key vaults</span></span>](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [<span data-ttu-id="2ecad-141">키를 만들거나 가져오는 방법으로 각 키 보관소에 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-141">Add a key to each key vault either by creating or importing a key</span></span>](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [<span data-ttu-id="2ecad-142">키의 복구 수준 확인</span><span class="sxs-lookup"><span data-stu-id="2ecad-142">Check the recovery level of your keys</span></span>](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [<span data-ttu-id="2ecad-143">Azure 키 자격 증명 모음 백업</span><span class="sxs-lookup"><span data-stu-id="2ecad-143">Backup Azure Key Vault</span></span>](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [<span data-ttu-id="2ecad-144">Azure 키 자격 증명 모음 구성 설정 확인</span><span class="sxs-lookup"><span data-stu-id="2ecad-144">Validate Azure Key Vault configuration settings</span></span>](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [<span data-ttu-id="2ecad-145">각 Azure key Vault 키에 대 한 URI 가져오기</span><span class="sxs-lookup"><span data-stu-id="2ecad-145">Obtain the URI for each Azure Key Vault key</span></span>](controlling-your-data-using-customer-key.md#GetKeyURI)
    
<span data-ttu-id="2ecad-146">**Office 365에서 다음을 수행 합니다.**</span><span class="sxs-lookup"><span data-stu-id="2ecad-146">**In Office 365:**</span></span>
  
<span data-ttu-id="2ecad-147">Exchange Online 및 비즈니스용 Skype:</span><span class="sxs-lookup"><span data-stu-id="2ecad-147">Exchange Online and Skype for Business:</span></span>
  
- [<span data-ttu-id="2ecad-148">Exchange Online 및 비즈니스용 Skype에서 사용 하기 위한 DEP (데이터 암호화 정책) 만들기</span><span class="sxs-lookup"><span data-stu-id="2ecad-148">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [<span data-ttu-id="2ecad-149">사서함에 DEP 할당</span><span class="sxs-lookup"><span data-stu-id="2ecad-149">Assign a DEP to a mailbox</span></span>](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [<span data-ttu-id="2ecad-150">사서함 암호화 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="2ecad-150">Validate mailbox encryption</span></span>](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
<span data-ttu-id="2ecad-151">SharePoint Online 및 비즈니스용 OneDrive:</span><span class="sxs-lookup"><span data-stu-id="2ecad-151">SharePoint Online and OneDrive for Business:</span></span>
  
- [<span data-ttu-id="2ecad-152">각 SharePoint Online 및 비즈니스용 OneDrive 지역에 대 한 DEP (데이터 암호화 정책)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-152">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [<span data-ttu-id="2ecad-153">그룹 사이트, 팀 사이트 및 비즈니스용 OneDrive의 암호화 확인</span><span class="sxs-lookup"><span data-stu-id="2ecad-153">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a><span data-ttu-id="2ecad-154">Azure key Vault의 완료 작업 및 고객 키 용 Microsoft fasttrack</span><span class="sxs-lookup"><span data-stu-id="2ecad-154">Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key</span></span>
<span data-ttu-id="2ecad-155"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-155"></span></span>

<span data-ttu-id="2ecad-p111">Office 365에 대 한 고객 키를 설정 하려면 Azure key Vault에서 이러한 작업을 완료 합니다. Exchange Online 및 비즈니스용 Skype 또는 SharePoint online 및 비즈니스용 OneDrive에 대해 고객 키를 설정 하려는 지, 아니면 Office 365에서 지원 되는 모든 서비스에 대해이 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p111">Complete these tasks in Azure Key Vault in order to set up Customer Key for Office 365. You will need to complete these steps regardless of whether you intend to set up Customer Key for Exchange Online and Skype for Business or SharePoint Online and OneDrive for Business or for all supported services in Office 365.</span></span>
  
### <a name="create-two-new-azure-subscriptions"></a><span data-ttu-id="2ecad-158">두 개의 새 Azure 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-158">Create two new Azure subscriptions</span></span>
<span data-ttu-id="2ecad-159"><a name="Create2newsubs"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-159"></span></span>

<span data-ttu-id="2ecad-p112">고객 키에는 두 개의 Azure 구독이 필요 합니다. 최상의 방법으로는 고객 키와 함께 사용할 새로운 Azure 구독을 만드는 것이 좋습니다. azure Key Vault 키에는 동일한 AAD (azure Active Directory) 테 넌 트의 응용 프로그램에 대해서만 권한을 부여할 수 있으며, deps가 할당 되는 Office 365 조직에 사용 되는 것과 동일한 Azure AD 테 넌 트를 사용 하 여 새 구독을 만들어야 합니다. 예를 들어 Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 자세한 단계는 [Azure for](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/)a a a a a a a a a a a as를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p112">Two Azure subscriptions are required for Customer Key. As a best practice, Microsoft recommends that you create new Azure subscriptions for use with Customer Key. Azure Key Vault keys can only be authorized for applications in the same Azure Active Directory (AAD) tenant, you must create the new subscriptions using the same Azure AD tenant used with your Office 365 organization where the DEPs will be assigned. For example, using your work or school account that has global administrator privileges in your Office 365 organization. For detailed steps, see [Sign up for Azure as an organization](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2ecad-p113">고객 키에는 각 DEP (데이터 암호화 정책)에 대 한 두 개의 키가 필요 합니다. 이를 위해서는 두 개의 Azure 구독을 만들어야 합니다. 조직의 개별 구성원이 각 구독에서 하나의 키를 구성 하는 것이 가장 좋은 방법입니다. 또한 이러한 Azure 구독은 Office 365의 암호화 키를 관리 하는 데에만 사용 해야 합니다. 이렇게 하면 운영자 중 한 명에 게 실수로 또는 악의적으로 삭제 되거나 자신이 담당 하는 키를 잘못 관리 하는 경우를 대비해 조직이 보호 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p113">Customer Key requires two keys for each data encryption policy (DEP). In order to achieve this, you must create two Azure subscriptions. As a best practice, Microsoft recommends that you have separate members of your organization configure one key in each subscription. In addition, these Azure subscriptions should only be used to administer encryption keys for Office 365. This protects your organization in case one of your operators accidentally, intentionally, or maliciously deletes or otherwise mismanages the keys for which they are responsible. </span></span><br/> <span data-ttu-id="2ecad-p114">azure key Vault 리소스를 관리 하는 데에만 사용 되는 새 azure 구독을 고객 키와 함께 사용 하도록 설정 하는 것이 좋습니다. 조직에 대해 만들 수 있는 Azure 구독 수에는 실질적인 제한이 없습니다. 이러한 모범 사례를 따르면 고객 키에서 사용 하는 리소스를 관리 하는 동안 인간 오류가 발생 하는 영향은 최소화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p114">We recommend that you set up new Azure subscriptions that are solely used for managing Azure Key Vault resources for use with Customer Key. There is no practical limit to the number of Azure subscriptions that you can create for your organization. Following these best practices will minimize the impact of human error while helping to manage the resources used by Customer Key.</span></span> 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a><span data-ttu-id="2ecad-173">Office 365에 대 한 고객 키를 정품 인증 하기 위한 요청 제출</span><span class="sxs-lookup"><span data-stu-id="2ecad-173">Submit a request to activate Customer Key for Office 365</span></span>
<span data-ttu-id="2ecad-174"><a name="FastTrack"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-174"></span></span>

<span data-ttu-id="2ecad-p115">Azure 단계를 완료 한 후에는 [Microsoft fasttrack 포털](https://fasttrack.microsoft.com/)에서 제공 요청을 제출 해야 합니다. fasttrack 웹 포털을 통해 요청을 제출 하면 Microsoft는 Azure 키 자격 증명 모음 구성 데이터와 사용자가 제공한 연락처 정보를 확인 합니다. 조직의 승인 된 관리자와 관련 하 여 제안 양식에서 선택한 항목은 고객 키 등록을 완료 하는 데 필수적이 고 필수적입니다. 양식에서 선택한 조직의 직원은 고객 키 데이터 암호화 정책에 사용 되는 모든 키를 해지 하 고 파기 하기 위한 요청의 신뢰성을 보장 하는 데 사용 됩니다. 이 단계를 한 번 수행 하 여 Exchange online 및 비즈니스용 Skype를 위한 고객 키를 정품 인증 하 고 SharePoint Online 및 비즈니스용 OneDrive에 대 한 고객 키를 활성화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p115">Once you've completed the Azure steps, you'll need to submit an offer request in the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/). Once you have submitted a request through the FastTrack web portal, Microsoft verifies the Azure Key Vault configuration data and contact information you provided. The selections that you make in the offer form regarding the authorized officers of your organization is critical and necessary for completion of Customer Key registration. The officers of your organization that you select in the form will be the used to ensure the authenticity of any request to revoke and destroy all keys used with a Customer Key data encryption policy. You'll need to do this step once to activate Customer Key for Exchange Online and Skype for Business coverage and a second time to activate Customer Key for SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="2ecad-180">고객 키를 정품 인증 하기 위한 제안을 제출 하려면 다음 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-180">To submit an offer to activate Customer Key, complete these steps:</span></span>
  
1. <span data-ttu-id="2ecad-181">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 여 [Microsoft fasttrack 포털](https://fasttrack.microsoft.com/)에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-181">Using a work or school account that has global administrator permissions in your Office 365 organization, log in to the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/).</span></span>
    
2. <span data-ttu-id="2ecad-182">로그인 한 후 **대시보드로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-182">Once you're logged in, browse to the **Dashboard**.</span></span>
    
3. <span data-ttu-id="2ecad-183">**서비스**를 선택 하 고 현재 서비스 목록을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-183">Choose **Offers**, and review the list of current offers.</span></span>
    
4. <span data-ttu-id="2ecad-184">사용자에 게 제공 되는 혜택에 대 한 **자세한 정보** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-184">Choose **Learn More** for the offer that applies to you:</span></span> 
    
  - <span data-ttu-id="2ecad-185">**Exchange Online 및 비즈니스용 Skype:** **고객 키에서 Exchange 제공에 대 한** **자세한 정보** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-185">**Exchange Online and Skype for Business:** Choose **Learn More** on the **Customer Key for Exchange** offer.</span></span> 
    
  - <span data-ttu-id="2ecad-186">**SharePoint Online 및 비즈니스용 OneDrive:** **SharePoint 용 고객 키 및 비즈니스용 OneDrive** 제공에 대 한 **자세한 정보** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-186">**SharePoint Online and OneDrive for Business:** Chose **Learn More** on the **Customer Key for SharePoint and OneDrive for Business** offer.</span></span> 
    
5. <span data-ttu-id="2ecad-187">**제공 세부 정보** 페이지에서 **요청 만들기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-187">On the **Offer details** page, choose **Create Request**.</span></span>
    
6. <span data-ttu-id="2ecad-p116">제공 양식에서 해당 하는 모든 정보 및 요청 된 정보를 입력 합니다. 인증을 승인할 조직의 관리자가 선택한 사항에 특별히 주의 하 여 암호화 키와 데이터의 영구 및 복구할 수 없는 소멸을 승인 해야 합니다. 양식을 완료 했으면 **제출을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p116">Fill out all applicable details and requested information on the offer form. Pay particular attention to your selections for which officers of your organization you want to authorize to approve the permanent and irreversible destruction of encryption keys and data. Once you've completed the form, choose **Submit**.</span></span>
    
    <span data-ttu-id="2ecad-191">Microsoft에 요청을 알렸습니다 하면이 프로세스는 최대 5 영업일까지 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-191">This process can take up to five business days once Microsoft has been notified of your request.</span></span>
    
7. <span data-ttu-id="2ecad-192">아래의 필수 보존 기간 섹션을 계속 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-192">Continue on to the mandatory retention period section below.</span></span>
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a><span data-ttu-id="2ecad-193">필수 보존 기간을 사용 하도록 Azure 구독 등록</span><span class="sxs-lookup"><span data-stu-id="2ecad-193">Register Azure subscriptions to use a mandatory retention period</span></span>
<span data-ttu-id="2ecad-194"><a name="RegisterSubsforMRP"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-194"></span></span>

<span data-ttu-id="2ecad-p117">루트 암호화 키의 임시 또는 영구 손실은 매우 방해가 되거나 서비스 작업에 치명적이 될 수 있으며 데이터 손실이 발생할 수 있습니다. 이러한 이유로, 고객 키와 함께 사용 되는 리소스에는 강력한 보호가 필요 합니다. 고객 키와 함께 사용 되는 모든 Azure 리소스는 기본 구성 외에도 보호 메커니즘을 제공 합니다. 즉시 및 irrevocable 취소를 방지 하는 방식으로 Azure 구독에 태그를 지정 하거나 등록할 수 있습니다. 이를 필수 보존 기간 등록 이라고 합니다. 필수 보존 기간 동안 Azure 구독을 등록 하는 데 필요한 단계에 따라 Office 365 팀과 공동 작업이 필요 합니다. 이 프로세스는 영업일 이하의 근무일까지 소요 될 수 있습니다. 이전에는이를 "취소 안 함"이 라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p117">The temporary or permanent loss of root encryption keys can be very disruptive or even catastrophic to service operation and can result in data loss. For this reason, the resources used with Customer Key require strong protection. All the Azure resources that are used with Customer Key offer protection mechanisms beyond the default configuration. Azure subscriptions can be tagged or registered in a way that will prevent immediate and irrevocable cancellation. This is referred to as registering for a mandatory retention period. The steps required to register Azure subscriptions for a mandatory retention period require collaboration with the Office 365 team. This process can take from one to five business days. Previously, this was sometimes referred to as "Do Not Cancel".</span></span>
  
<span data-ttu-id="2ecad-203">Office 365 팀에 연락 하기 전에 고객 키와 함께 사용 하는 각 Azure 구독에 대해 다음 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-203">Before contacting the Office 365 team, you must perform the following steps for each Azure subscription that you use with Customer Key:</span></span>
  
1. <span data-ttu-id="2ecad-p118">azure PowerShell을 사용 하 여 azure 구독에 로그인 합니다. 자세한 내용은 [Azure PowerShell을 사용 하 여 로그인](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p118">Log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
2. <span data-ttu-id="2ecad-206">AzureRmProviderFeature cmdlet을 실행 하 여 구독을 등록 하 고 필수 보존 기간을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-206">Run the Register-AzureRmProviderFeature cmdlet to register your subscriptions to use a mandatory retention period.</span></span>
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. <span data-ttu-id="2ecad-p119">Microsoft에 문의 하 여 해당 프로세스를 완료 합니다. SharePoint 및 비즈니스용 OneDrive 팀의 경우 [spock@microsoft.com](mailto:spock@microsoft.com)에 문의 하세요. Exchange Online 및 비즈니스용 Skype에 대 한 자세한 내용은 [exock@microsoft.com](mailto:exock@microsoft.com)에 문의 하세요. 이 프로세스를 완료 하는 데 필요한 SLA (서비스 수준 계약)는 Microsoft가 구독을 등록 하 여 필수 보존 기간을 사용 하도록 공지를 받은 경우 5 일 이내입니다. 전자 메일에 다음을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p119">Contact Microsoft to have the process finalized. For the SharePoint and OneDrive for Business team, contact [spock@microsoft.com](mailto:spock@microsoft.com). For Exchange Online and Skype for Business, contact [exock@microsoft.com](mailto:exock@microsoft.com). The Service Level Agreement (SLA) for completion of this process is five business days once Microsoft has been notified (and verified) that you have registered your subscriptions to use a mandatory retention period. Include the following in your email:</span></span>
    
    <span data-ttu-id="2ecad-212">**제목**: \< *테 넌 트의 정규화 된 도메인 이름* 에 대 한 고객 키\></span><span class="sxs-lookup"><span data-stu-id="2ecad-212">**Subject**: Customer Key for \<*Your tenant's fully-qualified domain name*\></span></span> 
    
    <span data-ttu-id="2ecad-213">**Body**: 필수 보존 기간을 완료 하려는 구독 id입니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-213">**Body**: Subscription IDs for which you want to have the mandatory retention period finalized.</span></span> 
    
4. <span data-ttu-id="2ecad-214">Microsoft에서 등록이 완료 되었음을 알리는 알림을 받으면 다음과 같이 AzureRmProviderFeature cmdlet을 실행 하 여 등록 상태를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-214">Once you receive notification from Microsoft that registration is complete, verify the status of your registration by running the Get-AzureRmProviderFeature cmdlet as follows:</span></span>
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. <span data-ttu-id="2ecad-215">AzureRmProviderFeature cmdlet의 **등록 상태** 속성이 **등록**된 값을 반환 하는지 확인 한 후 다음 명령을 실행 하 여 프로세스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-215">After verifying that the **Registration State** property from the Get-AzureRmProviderFeature cmdlet returns a value of **Registered**, run the following command to complete the process:</span></span>
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a><span data-ttu-id="2ecad-216">각 구독에 프리미엄 Azure 키 자격 증명 모음 만들기</span><span class="sxs-lookup"><span data-stu-id="2ecad-216">Create a premium Azure Key Vault in each subscription</span></span>
<span data-ttu-id="2ecad-217"><a name="CreateKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-217"></span></span>

<span data-ttu-id="2ecad-218">키 자격 증명 모음을 만드는 단계는 azure [키 자격 증명 모음을 시작](https://azure.microsoft.com/documentation/articles/key-vault-get-started/)하는 과정을 안내 하는 azure PowerShell을 설치 및 시작 하 고, azure 구독에 연결 하 고, 리소스 그룹을 만들고, 해당 키 자격 증명을 만드는 방법을 설명 합니다. 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="2ecad-218">The steps to create a key vault are documented in [Getting Started with Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), which guides you through installing and launching Azure PowerShell, connecting to your Azure subscription, creating a resource group, and creating a key vault in that resource group.</span></span>
  
<span data-ttu-id="2ecad-p120">키 자격 증명 모음을 만들 때는 SKU: Standard 또는 Premium 중 하나를 선택 해야 합니다. Standard SKU를 사용 하면 hsm (하드웨어 보안 모듈) 키 보호가 제공 되지 않으며 프리미엄 SKU는 키 자격 증명 키 보호를 위해 hsm을 사용할 수 있습니다. 고객 키가 sku를 사용 하는 키 보관소를 허용 하지만, Microsoft에서는 프리미엄 sku만 사용 하는 것이 좋습니다. 두 가지 유형의 키를 사용한 작업 비용은 같으므로, 각 HSM 보호 키에 대 한 월별 비용은 비용의 차이입니다. 자세한 내용은 [키 자격 증명 모음 가격 산정](https://azure.microsoft.com/pricing/details/key-vault/) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p120">When you create a key vault, you must choose a SKU: either Standard or Premium. The Standard SKU allows Azure Key Vault keys to be protected with software - there is no Hardware Security Module (HSM) key protection - and the Premium SKU allows the use of HSMs for protection of Key Vault keys. Customer Key accepts key vaults that use either SKU, though Microsoft strongly recommends that you use only the Premium SKU. The cost of operations with keys of either type is the same, so the only difference in cost is the cost per month for each HSM-protected key. See [Key Vault pricing](https://azure.microsoft.com/pricing/details/key-vault/) for details.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="2ecad-224">프로덕션 데이터에 대해 Premium sku 키 보관소 및 HSM으로 보호 된 키를 사용 하 고 테스트 및 유효성 검사를 위해 Standard sku 키 보관소와 키만 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-224">Use the Premium SKU key vaults and HSM-protected keys for production data, and only use Standard SKU key vaults and keys for testing and validation purposes.</span></span> 
  
<span data-ttu-id="2ecad-p121">고객 키를 사용 하는 각 Office 365 서비스에 대해 사용자가 만든 두 가지 Azure 구독 각각에 키 자격 증명 모음을 만듭니다. 예를 들어 Exchange Online 및 비즈니스용 Skype 전용 또는 SharePoint Online 및 비즈니스용 OneDrive 전용의 경우에는 하나의 자격 증명 모음만 만듭니다. Exchange online 및 SharePoint online 둘 다에 대해 고객 키를 사용 하도록 설정 하기 위해 두 쌍의 키 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p121">For each Office 365 service with which you will use Customer Key, create a key vault in each of the two Azure subscriptions that you created. For example, for Exchange Online and Skype for Business only or SharePoint Online and OneDrive for Business only, you will create only one pair of vaults. To enable Customer Key for both Exchange Online and SharePoint Online, you will create two pairs of key vaults.</span></span>
  
<span data-ttu-id="2ecad-p122">자격 증명 모음을 연결 하는 데 사용할 DEP의 용도를 반영 하는 키 보관소에 대 한 명명 규칙을 사용 합니다. 명명 규칙 추천을 보려면 아래에서 모범 사례 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p122">Use a naming convention for key vaults that reflects the intended use of the DEP with which you will associate the vaults. See the Best Practices section below for naming convention recommendations.</span></span>
  
<span data-ttu-id="2ecad-p123">각 데이터 암호화 정책에 대해 쌍을 이룬 별도의 자격 증명 모음을 만듭니다. Exchange Online의 경우 사서함에 정책을 할당할 때 사용자가 데이터 암호화 정책의 범위를 선택 합니다. 사서함에는 정책이 하나만 할당 될 수 있으며 최대 50 개의 정책을 만들 수 있습니다. SharePoint Online의 경우 정책의 범위는 지리적 위치 또는 지리적으로 조직 내의 모든 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p123">Create a separate, paired set of vaults for each data encryption policy. For Exchange Online, the scope of a data encryption policy is chosen by you when you assign the policy to mailbox. A mailbox can have only one policy assigned, and you can create up to fifty policies. For SharePoint Online the scope of a policy is all of the data within an organization in a geographic location, or geo.</span></span>
  
<span data-ttu-id="2ecad-p124">또한 키 보관소에는 저장소 용량 (매우 작음)과 키 보관소 로깅이 필요 하기 때문에 (키 보관소를 만드는 경우) 저장 된 데이터도 생성 해야 하므로 Azure 리소스 그룹을 만들어야 합니다. Microsoft는 별도의 관리자를 사용 하 여 각 리소스 그룹을 관리할 것을 권장 하 고, 관리를 모든 관련 고객 키 리소스를 관리 하는 관리자 집합과 맞추고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p124">The creation of key vaults also requires the creation of Azure resource groups, since key vaults need storage capacity (though very small) and Key Vault logging, if enabled, also generates stored data. As a best practice Microsoft recommends using separate administrators to manage each resource group, with the administration aligned with the set of administrators that will manage all related Customer Key resources.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2ecad-p125">가용성을 최대화 하려면 키 보관소가 Office 365 서비스에 가까운 지역에 있어야 합니다. 예를 들어 Exchange Online 조직이 북미에 있는 경우 북미에 키 자격 증명 모음을 배치 합니다. Exchange Online 조직이 유럽에 있는 경우 키 보관소를 유럽에 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p125">To maximize availability, your key vaults should be in regions close to your Office 365 service. For example, if your Exchange Online organization is in North America, place your key vaults in North America. If your Exchange Online organization is in Europe, place your key vaults in Europe.</span></span><br/><span data-ttu-id="2ecad-p126">키 자격 증명에 대 한 공통 접두사를 사용 하 고, 키 보관소와 키의 사용 및 범위 약어를 포함 하 고 (예: 해당 보관소가 북미에 있는 contoso SharePoint 서비스의 경우) 가능한 이름 쌍은 contoso-O365SP-VaultA1 및 Contoso-O365SP-VaultA2. 자격 증명 이름은 Azure 내의 전역적으로 고유한 문자열이 되므로 필요한 이름이 다른 Azure 고객의 요청을 받아야 하는 경우에 대비 하 여 원하는 이름의 변형을 시도해 야 할 수 있습니다. 7 월 2017 볼트 이름은 변경할 수 없으므로 설정 계획을 수립 하 고 두 번째 사용자를 사용 하 여 계획이 올바르게 실행 되는지 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p126">Use a common prefix for key vaults, and include an abbreviation of the use and scope of the key vault and keys (e.g., for the Contoso SharePoint service where the vaults will be located in North America, a possible pair of names is Contoso-O365SP-NA-VaultA1 and Contoso-O365SP-NA-VaultA2. Vault names are globally unique strings within Azure, so you may need to try variations of your desired names in case the desired names are already claimed by other Azure customers. As of July 2017 vault names cannot be changed, so a best practice is to have a written plan for setup and use a second person to verify the plan is executed correctly.</span></span><br/><span data-ttu-id="2ecad-p127">가능 하면 페어링되지 않은 지역에 자격 증명 모음을 만듭니다. 쌍을 이룬 Azure 지역에서 서비스 장애 도메인 별로 고가용성을 제공 합니다. 따라서 지역 쌍을 서로의 백업 지역으로 간주할 수 있습니다. 즉, 한 지역에 배치 된 Azure 리소스가 연결 된 지역을 통과 하는 내결함성을 자동으로 획득 합니다. 이러한 이유 때문에 지역이 쌍을 이루는 DEP에서 사용 되는 두 개의 자격 증명 영역을 선택 하면 사용 가능한 영역의 총 두 영역만 사용할 수 있습니다. 대부분의 지역에는 두 지역이 있으므로 아직 연결 되지 않은 영역을 선택할 수는 없습니다. 가능한 경우 DEP와 함께 사용 되는 두 개의 보관소에 대해 쌍이 없는 두 개의 영역을 선택 합니다. 이는 가용성의 총 4 지역에서 혜택을 제공 합니다. 자세한 내용은 [Business 연속성 및 재해 복구 (BCDR):](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) 현재 지역 쌍 목록의 Azure 연결 된 지역을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p127">If possible, create your vaults in non-paired regions. Paired Azure regions provide high availability across service failure domains. Therefore, regional pairs can be thought of as each other's backup region. This means that an Azure resource that is placed in one region is automatically gaining fault tolerance through the paired region. For this reason, choosing regions for two vaults used in a DEP where the regions are paired means that only a total of two regions of availability are in use. Most geographies only have two regions, so it's not yet possible to select non-paired regions. If possible, choose two non-paired regions for the two vaults used with a DEP. This benefits from a total of four regions of availability. For more information, see [Business continuity and disaster recovery (BCDR): Azure Paired Regions](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) for a current list of regional pairs.</span></span> 
  
### <a name="assign-permissions-to-each-key-vault"></a><span data-ttu-id="2ecad-251">각 키 자격 증명 모음에 사용 권한 할당</span><span class="sxs-lookup"><span data-stu-id="2ecad-251">Assign permissions to each key vault</span></span>
<span data-ttu-id="2ecad-252"><a name="KeyVaultPerms"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-252"></span></span>

<span data-ttu-id="2ecad-p128">각 키 보관소에 대해 구현에 따라 고객 키에 대해 세 가지 개별 사용 권한 집합을 정의 해야 합니다. 예를 들어 다음 각 항목에 대해 하나의 권한 집합을 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p128">For each key vault, you will need to define three separate sets of permissions for Customer Key, depending on your implementation. For example, you will need to define one set of permissions for each of the following:</span></span>
  
- <span data-ttu-id="2ecad-p129">조직에 대 한 주요 자격 증명 모음을 일상적인 관리 하는 데 사용할 수 있는 **주요 자격 증명 모음 관리자** 이러한 작업에는 백업, 만들기, 가져오기, 가져오기, 목록, 복원 등이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p129">**Key vault administrators** that will perform day-to-day management of your key vault for your organization. These tasks include backup, create, get, import, list, and restore.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="2ecad-p130">키 자격 증명 모음 관리자에 게 할당 된 사용 권한 집합에는 키를 삭제할 수 있는 권한이 포함 되어 있지 않습니다. 이는 의도적인 것이 고 중요 한 방법입니다. 일반적으로 암호화 키 삭제는 데이터를 영구적으로 소멸 하기 때문에 수행 되지 않습니다. 주요 자격 증명 모음 관리자에 게 기본적으로이 사용 권한을 부여 하지 않는 것이 좋습니다. 대신 주요 자격 증명 참가자에 대해이를 예약 하 고, 결과에 대 한 확실 한 이해가 이해 되 면 짧은 기간 동안 관리자 에게만 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p130">The set of permissions assigned to key vault administrators does not include the permission to delete keys. This is intentional and an important practice. Deleting encryption keys is not typically done, since doing so permanently destroys data. As a best practice, do not grant this permission to key vault administrators by default. Instead, reserve this for key vault contributors and only assign it to an administrator on a short term basis once a clear understanding of the consequences is understood.</span></span> 
  
    <span data-ttu-id="2ecad-p131">Office 365 조직의 사용자에 게 이러한 권한을 할당 하려면 azure PowerShell을 사용 하 여 azure 구독에 로그인 합니다. 자세한 내용은 [Azure PowerShell을 사용 하 여 로그인](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p131">To assign these permissions to a user in your Office 365 organization, log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
- <span data-ttu-id="2ecad-264">AzureRmKeyVaultAccessPolicy cmdlet을 실행 하 여 필요한 권한을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-264">Run the Set-AzureRmKeyVaultAccessPolicy cmdlet to assign the necessary permissions.</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  <span data-ttu-id="2ecad-265">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-265">For example:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- <span data-ttu-id="2ecad-p132">Azure 키 자격 증명 모음 자체에 대 한 사용 권한을 변경할 수 있는 **키 보관소 참가자** 직원은 팀에 탈퇴 하거나 참가할 때 이러한 권한을 변경 해야 하며, 키 보관소 관리자가 키를 삭제 하거나 복원 하는 데 필요한 권한을 갖는 것이 아주 드문 경우입니다. 이 키 보관소 참가자 집합에는 해당 키 자격 증명 모음에 대 한 **참가자** 역할이 부여 되어야 합니다. Azure Resource Manager를 사용 하 여이 역할을 할당할 수 있습니다. 자세한 단계는 [역할 기반 액세스 제어를 사용 하 여 Azure 구독 리소스에 대 한 액세스를 관리 하](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure)는 방법을 참조 하세요. 구독을 만드는 관리자는이 액세스 권한 뿐만 아니라 다른 관리자에 게 참가자 역할을 할당할 수 있는 권한도 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p132">**Key vault contributors** that can change permissions on the Azure Key Vault itself. You'll need to change these permissions as employees leave or join your team, or in the extremely rare situation that the key vault administrators legitimately need permission to delete or restore a key. This set of key vault contributors needs to be granted the **Contributor** role on your key vault. You can assign this role by using Azure Resource Manager. For detailed steps, see [Use Role-Based Access Control to manage access to your Azure subscription resources](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). The administrator who creates a subscription has this access implicitly, as well as the ability to assign other administrators to the Contributor role.</span></span>
    
- <span data-ttu-id="2ecad-p133">exchange online 및 비즈니스용 skype와 함께 고객 키를 사용 하려는 경우에는 Office 365에 대 한 권한을 부여 하 여 exchange online 및 비즈니스용 skype를 대신 하 여 키 자격 증명 모음을 사용 해야 합니다. 마찬가지로, sharepoint online 및 비즈니스용 onedrive에서 고객 키를 사용 하려는 경우에는 Office 365에 대 한 권한을 추가 하 여 sharepoint online 및 비즈니스용 onedrive를 대신 하 여 키 자격 증명 모음을 사용 해야 합니다. Office 365에 대 한 사용 권한을 부여 하려면 다음 구문을 사용 하 여 **AzureRmKeyVaultAccessPolicy** cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p133">If you intend to use Customer Key with Exchange Online and Skype for Business, you need to give permission to Office 365 to use the key vault on behalf of Exchange Online and Skype for Business. Likewise, if you intend to use Customer Key with SharePoint Online and OneDrive for Business, you need to add permission for the Office 365 to use the key vault on behalf of SharePoint Online and OneDrive for Business. To give permission to Office 365, run the **Set-AzureRmKeyVaultAccessPolicy** cmdlet using the following syntax:</span></span> 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    <span data-ttu-id="2ecad-275">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-275">Where:</span></span>
    
  - <span data-ttu-id="2ecad-276">*vaultname* 은 만든 키 보관소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-276">*vaultname* is the name of the key vault you created.</span></span> 
    
  - <span data-ttu-id="2ecad-277">Exchange Online 및 비즈니스용 Skype의 경우 *Office 365 appID* 를 다음으로 바꾸기`00000002-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="2ecad-277">For Exchange Online and Skype for Business, replace  *Office 365 appID* with `00000002-0000-0ff1-ce00-000000000000`</span></span>
    
  - <span data-ttu-id="2ecad-278">SharePoint Online 및 비즈니스용 OneDrive의 경우 *Office 365 appID* 를 다음으로 바꾸기`00000003-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="2ecad-278">For SharePoint Online and OneDrive for Business, replace  *Office 365 appID* with `00000003-0000-0ff1-ce00-000000000000`</span></span>
    
  <span data-ttu-id="2ecad-279">예: Exchange Online 및 비즈니스용 Skype에 대 한 사용 권한 설정:</span><span class="sxs-lookup"><span data-stu-id="2ecad-279">Example: Setting permissions for Exchange Online and Skype for Business:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  <span data-ttu-id="2ecad-280">예: SharePoint Online 및 비즈니스용 OneDrive에 대 한 사용 권한 설정</span><span class="sxs-lookup"><span data-stu-id="2ecad-280">Example: Setting permissions for SharePoint Online and OneDrive for Business</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a><span data-ttu-id="2ecad-281">키 자격 증명 모음에서 일시 삭제를 사용 하도록 설정 하 고 확인</span><span class="sxs-lookup"><span data-stu-id="2ecad-281">Enable and then confirm soft delete on your key vaults</span></span>
<span data-ttu-id="2ecad-282"><a name="SoftDelete"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-282"></span></span>

<span data-ttu-id="2ecad-p134">키를 신속 하 게 복구할 수 있으면 실수로 또는 악의적으로 삭제 된 키로 인해 확장 서비스 중단을 경험할 가능성이 줄어듭니다. 사용자 키에 키를 사용할 수 있으려면 먼저 소프트 삭제 라고 하는이 구성을 사용 하도록 설정 해야 합니다. 소프트 삭제를 사용 하도록 설정 하면 백업에서 복원 하지 않고도 90 일 내에 키 또는 자격 증명 모음을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p134">When you can quickly recover your keys, you are less likely to experience an extended service outage due to accidentally or maliciously deleted keys. You need to enable this configuration, referred to as Soft Delete, before you can use your keys with Customer Key. Enabling Soft Delete allows you to recover keys or vaults within 90 days of deletion without having to restore them from backup.</span></span>
  
<span data-ttu-id="2ecad-286">키 자격 증명 모음에서 일시 삭제를 사용 하도록 설정 하려면 다음 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-286">To enable Soft Delete on your key vaults, complete these steps:</span></span>
  
1. <span data-ttu-id="2ecad-p135">Windows Powershell을 사용 하 여 Azure 구독에 로그인 합니다. 자세한 내용은 [Azure PowerShell을 사용 하 여 로그인](https://docs.microsoft.com/powershell/azure/authenticate-azureps)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p135">Log in to your Azure subscription with Windows Powershell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span></span>
    
2. <span data-ttu-id="2ecad-p136">[AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) cmdlet을 실행 합니다. 이 예에서 *vaultname* 은 소프트 삭제를 활성화할 수 있는 키 보관소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p136">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) cmdlet. In this example, *vaultname* is the name of the key vault for which you are enabling soft delete:</span></span> 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. <span data-ttu-id="2ecad-p137">**AzureRmKeyVault** cmdlet을 실행 하 여 키 자격 증명 모음에 대해 소프트 삭제가 구성 되었는지 확인 합니다. 키 자격 증명 모음에 대해 소프트 삭제가 올바르게 구성 된 경우 소프트 삭제를 사용할 수 있나요? 속성은 **True**값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p137">Confirm soft delete is configured for the key vault by running the **Get-AzureRmKeyVault** cmdlet. If soft delete is configured properly for the key vault, then the  Soft Delete Enabled? property returns a value of **True**:</span></span> 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a><span data-ttu-id="2ecad-293">키를 만들거나 가져오는 방법으로 각 키 보관소에 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-293">Add a key to each key vault either by creating or importing a key</span></span>
<span data-ttu-id="2ecad-294"><a name="AddKeystoKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-294"></span></span>

<span data-ttu-id="2ecad-p138">Azure 키 보관소에는 두 가지 방법으로 키를 추가할 수 있습니다. 키 보관소에 직접 키를 만들거나 키를 가져올 수 있습니다. 키 보관소에서 직접 키를 만드는 것은 다소 복잡 한 방법 이지만 키를 가져오면 키가 생성 되는 방식을 보다 강력 하 게 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p138">There are two ways to add keys to an Azure Key Vault; you can create a key directly in Key Vault, or you can import a key. Creating a key directly in Key Vault is the less complicated method, while importing a key provides total control over how the key is generated.</span></span>
  
<span data-ttu-id="2ecad-297">키 보관소에 직접 키를 만들려면 다음과 같이 [AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-297">To create a key directly in your key vault, run the [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="2ecad-298">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-298">Where:</span></span>
  
-  <span data-ttu-id="2ecad-299">*vaultname* 은 키를 만들 키 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-299">*vaultname*  is the name of the key vault in which you want to create the key.</span></span> 
    
-  <span data-ttu-id="2ecad-300">*keyname* 은 새 키에 지정할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-300">*keyname*  is the name you want to give the new key.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="2ecad-p139">키 보관소에 대해 위에서 설명한 유사 명명 규칙을 사용 하 여 이름 키 이러한 방식으로 키 이름만 표시 되는 도구에서 문자열은 자체 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p139">Name keys using a similar naming convention as described above for key vaults. This way, in tools that show only the key name, the string is self-describing.</span></span> 
  
- <span data-ttu-id="2ecad-303">hsm을 사용 하 여 키를 보호 하려면 _대상_ 매개 변수의 값으로 **HSM** 을 지정 하 고, 그렇지 않으면 **소프트웨어**를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-303">If you intend to protect the key with an HSM, ensure that you specify **HSM** as the value of the  _Destination_ parameter, otherwise, specify **Software**.</span></span>
    
<span data-ttu-id="2ecad-304">예:</span><span class="sxs-lookup"><span data-stu-id="2ecad-304">For example,</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="2ecad-305">키 보관소로 바로 키를 가져오려면 Thales nshield 하드웨어 보안 모듈이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-305">To import a key directly into your key vault, you need to have a Thales nShield Hardware Security Module.</span></span>
  
<span data-ttu-id="2ecad-306">일부 조직에서는이 방법을 선호 하 여 키의 provenance을 설정 하 고,이 방법 역시 다음을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-306">Some organizations prefer this approach to establish the provenance of their keys, and the this method also provides the following:</span></span>
  
- <span data-ttu-id="2ecad-307">가져오기에 사용 되는 도구 집합에는 Thales에서 생성 한 키를 암호화 하는 데 사용 되는 KEK (키 교환 키)가 내보낼 수 없으며 Thales에서 제조한 정품 HSM 내에서 생성 된다는 것이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-307">The toolset used for import includes attestation from Thales that the Key Exchange Key (KEK) that is used to encrypt the key you generate is not exportable and is generated inside a genuine HSM that was manufactured by Thales.</span></span>
    
- <span data-ttu-id="2ecad-p140">도구 집합에는 Thales에서 제조한 정품 HSM에도 Azure 키 자격 증명 모음 보안 세계가 생성 된 Thales의 증명이 포함 되어 있습니다. 이 증명은 Microsoft가 정품 Thales 하드웨어를 사용 하 고 있음을 증명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p140">The toolset includes attestation from Thales that the Azure Key Vault security world was also generated on a genuine HSM manufactured by Thales. This attestation proves to you that Microsoft is also using genuine Thales hardware.</span></span>
    
<span data-ttu-id="2ecad-p141">보안 그룹을 확인 하 여 위의 attestations 필요한 지 확인 합니다. 온-프레미스 키를 만들고 키 보관소로 가져오는 자세한 단계 [는 Azure key vault에 대해 HSM 보호 키를 생성 하 고 전송 하는 방법을](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/)참조 하세요. Azure 지침을 사용 하 여 각 키 자격 증명 모음에 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p141">Check with your security group to determine if the above attestations are required. For detailed steps to create a key on-premises and import it into your key vault, see [How to generate and transfer HSM-protected keys for Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Use the Azure instructions to create a key in each key vault.</span></span>
  
### <a name="check-the-recovery-level-of-your-keys"></a><span data-ttu-id="2ecad-313">키의 복구 수준 확인</span><span class="sxs-lookup"><span data-stu-id="2ecad-313">Check the recovery level of your keys</span></span>
<span data-ttu-id="2ecad-314"><a name="CheckKeyRecoveryLevel"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-314"></span></span>

<span data-ttu-id="2ecad-p142">Office 365을 사용 하려면 Azure 키 자격 증명 모음 구독이 취소 되지 않도록 설정 되 고, 고객 키에 사용 되는 키에 소프트 삭제가 사용 되도록 되어 있어야 합니다. 키의 복구 수준을 확인 하 여이를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p142">Office 365 requires that the Azure Key Vault subscription is set to Do Not Cancel and that the keys used by Customer Key have soft delete enabled. You can confirm this by looking at the recovery level on your keys.</span></span>
  
<span data-ttu-id="2ecad-317">키의 복구 수준을 확인 하려면 Azure PowerShell에서 다음과 같이 AzureKeyVaultKey cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-317">To check the recovery level of a key, in Azure PowerShell, run the Get-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

<span data-ttu-id="2ecad-318">_복구 수준_ 속성에서 복구 **가능한 + ProtectedSubscription**값이 아닌 다른 항목을 반환 하는 경우에는이 항목을 검토 하 여 구독을 취소 하지 않음 목록에 추가 하는 모든 단계를 따랐는지 확인 해야 합니다. 각 키 보관소에 소프트 삭제를 사용 하도록 설정 되어 있는지 여부</span><span class="sxs-lookup"><span data-stu-id="2ecad-318">If the  _Recovery Level_ property returns anything other than a value of **Recoverable+ProtectedSubscription**, you will need to review this topic and ensure that you have followed all of the steps to put the subscription on the Do Not Cancel list and that you have soft delete enabled on each of your key vaults.</span></span>
  
### <a name="backup-azure-key-vault"></a><span data-ttu-id="2ecad-319">Azure 키 자격 증명 모음 백업</span><span class="sxs-lookup"><span data-stu-id="2ecad-319">Backup Azure Key Vault</span></span>
<span data-ttu-id="2ecad-320"><a name="BackupAzureKeyVaultkeys"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-320"></span></span>

<span data-ttu-id="2ecad-p143">키를 만들거나 변경 하는 즉시 백업 및 오프 라인 복사본을 백업 및 저장 합니다. 오프 라인 복사본은 실제 안전 또는 상업적 저장소 기능과 같은 네트워크에 연결 해서는 안 됩니다. 재해 발생 시 액세스할 수 있는 위치에 백업 복사본을 하나 이상 저장 해야 합니다. 백업 blob은 키 자료를 복원 하는 유일한 방법으로 키 자격 증명 키를 영구적으로 제거 하거나 작동 하지 않는 방식으로 렌더링 해야 합니다. azure 키 자격 증명 모음에 대 한 외부 키를 가져오고 azure 키 보관소로 가져온 키는 해당 키를 사용 하는 데 필요한 메타 데이터가 외부 키가 없기 때문에 백업으로 한정 되지 않습니다. Azure key Vault에서 가져온 백업만 고객 키를 사용한 복원 작업에 사용할 수 있습니다. 따라서 키가 업로드 되거나 생성 되 면 Azure 키 자격 증명 모음을 백업 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p143">Immediately following creation or any change to a key, perform a backup and store copies of the backup, both online and offline. Offline copies should not be connected to any network, such as in a physical safe or commercial storage facility. At least one copy of the backup should be stored in a location that will be accessible in the event of a disaster. The backup blobs are the sole means of restoring key material should a Key Vault key be permanently destroyed or otherwise rendered inoperable. Keys that are external to Azure Key Vault and were imported to Azure Key Vault do not qualify as a backup because the metadata necessary for Customer Key to use the key does not exist with the external key. Only a backup taken from Azure Key Vault can be used for restore operations with Customer Key. Therefore, it is essential that a backup of Azure Key Vault be made once a key is uploaded or created.</span></span>
  
<span data-ttu-id="2ecad-328">Azure 키 자격 증명 키의 백업을 만들려면 다음과 같이 [AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-328">To create a backup of an Azure Key Vault key, run the [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) cmdlet as follows:</span></span>
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

<span data-ttu-id="2ecad-329">출력 파일이 접미사 `.backup`를 사용 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-329">Ensure that your output file uses the suffix  `.backup`.</span></span>
  
<span data-ttu-id="2ecad-p144">이 cmdlet에서 생성 된 출력 파일은 암호화 되며 Azure 키 자격 증명 모음 외부에서 사용할 수 없습니다. 백업은 백업을 수행한 Azure 구독에만 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p144">The output file resulting from this cmdlet is encrypted and cannot be used outside of Azure Key Vault. The backup can be restored only to the Azure subscription from which the backup was taken.</span></span>
  
> [!TIP]
> <span data-ttu-id="2ecad-p145">출력 파일의 경우 자격 증명 모음 이름 및 키 이름을 조합 하 여 선택 합니다. 이렇게 하면 파일 이름이 자체 설명 됩니다. 또한 백업 파일 이름이 충돌 하지 않도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p145">For the output file, choose a combination of your vault name and key name. This will make the file name self-describing. It will also ensure that backup file names do not collide.</span></span> 
  
<span data-ttu-id="2ecad-335">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-335">For example:</span></span>
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a><span data-ttu-id="2ecad-336">Azure 키 자격 증명 모음 구성 설정 확인</span><span class="sxs-lookup"><span data-stu-id="2ecad-336">Validate Azure Key Vault configuration settings</span></span>
<span data-ttu-id="2ecad-337"><a name="Validateconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-337"></span></span>

<span data-ttu-id="2ecad-p146">DEP에서 키를 사용 하기 전에 유효성 검사를 수행 하는 것은 선택 사항 이지만 가급적 권장 됩니다. 특히이 항목에서 설명 하는 것과 다른 키 및 보관소를 설정 하는 단계를 사용 하는 경우에는 고객 키를 구성 하기 전에 Azure key Vault 리소스의 상태를 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p146">Performing validation before using keys in a DEP is optional, but highly recommended. In particular, if you use steps to set up your keys and vaults other than the ones described in this topic, you should validate the health of your Azure Key Vault resources before you configure Customer Key.</span></span>
  
<span data-ttu-id="2ecad-340">키가 get, wrapKey 및 unwrapKey 작업을 사용 하도록 설정 되었는지 확인 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-340">To verify that your keys have get, wrapKey, and unwrapKey operations enabled:</span></span>
  
<span data-ttu-id="2ecad-341">다음과 같이 [AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-341">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) cmdlet as follows:</span></span> 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

<span data-ttu-id="2ecad-p147">출력에서 액세스 정책 및 Exchange online id (guid) 또는 SharePoint online id (guid)를 적절 하 게 찾습니다. 위의 세 가지 사용 권한 중 일부는 키 사용 권한 아래에 표시 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p147">In the output, look for the Access Policy and for the Exchange Online identity (GUID) or the SharePoint Online identity (GUID) as appropriate. All three of the above permissions must be shown under Permissions to Keys.</span></span>
  
<span data-ttu-id="2ecad-344">액세스 정책 구성이 올바르지 않으면 다음과 같이 AzureRmKeyVaultAccessPolicy cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-344">If the access policy configuration is incorrect, run the Set-AzureRmKeyVaultAccessPolicy cmdlet as follows:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

<span data-ttu-id="2ecad-345">예를 들어 Exchange Online 및 비즈니스용 Skype의 경우:</span><span class="sxs-lookup"><span data-stu-id="2ecad-345">For example, for Exchange Online and Skype for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

<span data-ttu-id="2ecad-346">예를 들어 SharePoint Online 및 비즈니스용 OneDrive:</span><span class="sxs-lookup"><span data-stu-id="2ecad-346">For example, for SharePoint Online and OneDrive for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

<span data-ttu-id="2ecad-347">키에 대해 만료 날짜가 설정 되지 않았는지 확인 하려면 다음과 같이 [AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-347">To verify that an expiration date is not set for your keys run the [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

<span data-ttu-id="2ecad-p148">만료 된 키는 고객 키에서 사용할 수 없으며 만료 된 키로 시도한 작업은 실패 하 고 서비스 중단으로 인해 발생할 수도 있습니다. 고객 키와 함께 사용 되는 키에는 만료 날짜가 없을 것을 적극 권장 합니다. 만료 날짜를 설정한 후에는 제거할 수 없지만 다른 날짜로 변경할 수는 있습니다. 만료 날짜가 설정 된 키를 사용 해야 하는 경우 만료 값을 12/31/9999로 변경 합니다. 만료 날짜가 12/31/9999 이외의 날짜로 설정 된 키는 Office 365 유효성 검사를 통과 하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p148">An expired key cannot be used by Customer Key and operations attempted with an expired key will fail, and possibly result in a service outage. We strongly recommend that keys used with Customer Key do not have an expiration date. An expiration date, once set, cannot be removed, but can be changed to a different date. If a key must be used that has an expiration date set, change the expiration value to 12/31/9999. Keys with an expiration date set to a date other than 12/31/9999 will not pass Office 365 validation.</span></span>
  
<span data-ttu-id="2ecad-353">12/31/9999 이외의 값으로 설정 된 만료 날짜를 변경 하려면 다음과 같이 [AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-353">To change an expiration date that has been set to any value other than 12/31/9999, run the [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) cmdlet as follows:</span></span> 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> <span data-ttu-id="2ecad-354">고객 키와 함께 사용 하는 암호화 키에 대해 만료 날짜를 설정 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="2ecad-354">Don't set expiration dates on encryption keys you use with Customer Key.</span></span> 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a><span data-ttu-id="2ecad-355">각 Azure key Vault 키에 대 한 URI 가져오기</span><span class="sxs-lookup"><span data-stu-id="2ecad-355">Obtain the URI for each Azure Key Vault key</span></span>
<span data-ttu-id="2ecad-356"><a name="GetKeyURI"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-356"></span></span>

<span data-ttu-id="2ecad-p149">Azure의 모든 단계를 완료 하 여 키 자격 증명 모음을 설정 하 고 키를 추가한 후에는 다음 명령을 실행 하 여 각 키 자격 증명 모음에서 키에 대 한 URI를 가져옵니다. 나중에 각 DEP를 만들고 할당할 때 이러한 uri를 사용 해야 하므로이 정보를 안전한 장소에 저장 합니다. 각 키 자격 증명 모음에 대해 한 번씩이 명령을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p149">Once you have completed all the steps in Azure to set up your key vaults and added your keys, run the following command to get the URI for the key in each key vault. You will need to use these URIs when you create and assign each DEP later, so save this information in a safe place. Remember to run this command once for each key vault.</span></span>
  
<span data-ttu-id="2ecad-360">Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="2ecad-360">In Azure PowerShell:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="2ecad-361">Office 365: Exchange Online 및 비즈니스용 Skype에 대 한 고객 키 설정</span><span class="sxs-lookup"><span data-stu-id="2ecad-361">Office 365: Setting up Customer Key for Exchange Online and Skype for Business</span></span>
<span data-ttu-id="2ecad-362"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-362"></span></span>

<span data-ttu-id="2ecad-p150">시작 하기 전에 Azure 키 자격 증명 모음을 설정 하는 데 필요한 작업을 완료 했는지 확인 합니다. 자세한 내용은 [Azure key Vault의 전체 작업 및 Microsoft fasttrack for Customer key](controlling-your-data-using-customer-key.md#AzureSteps) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p150">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="2ecad-365">exchange online 및 비즈니스용 Skype에 대 한 고객 키를 설정 하려면 Windows PowerShell을 사용 하 여 exchange online에 원격으로 연결 하 여 다음 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-365">To set up Customer Key for Exchange Online and Skype for Business, you will need to perform these steps by remotely connecting to Exchange Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a><span data-ttu-id="2ecad-366">Exchange Online 및 비즈니스용 Skype에서 사용 하기 위한 DEP (데이터 암호화 정책) 만들기</span><span class="sxs-lookup"><span data-stu-id="2ecad-366">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>
<span data-ttu-id="2ecad-367"><a name="CreateDEP4EXOSkype"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-367"></span></span>

<span data-ttu-id="2ecad-p151">DEP는 Azure Key Vault에 저장 된 키 집합과 연결 됩니다. Office 365에서 사서함에 DEP를 할당 합니다. 그런 다음 Office 365에서는 정책에 식별 된 키를 사용 하 여 사서함을 암호화 합니다. DEP를 만들려면 이전에 가져온 키 보관소 uri가 필요 합니다. 지침은 [각 Azure 키 자격 증명 모음 키의 URI 가져오기를](controlling-your-data-using-customer-key.md#GetKeyURI) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p151">A DEP is associated with a set of keys stored in Azure Key Vault. You assign a DEP to a mailbox in Office 365. Office 365 will then use the keys identified in the policy to encrypt the mailbox. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="2ecad-p152">항상! DEP를 만들 때 서로 다른 두 Azure 키 자격 증명 모음에 있는 두 개의 키를 지정 합니다. 이러한 키가 지리적 중복을 보장 하기 위해 별도의 두 Azure 지역에 위치 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p152">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="2ecad-376">DEP를 만들려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-376">To create the DEP, follow these steps:</span></span>
  
1. <span data-ttu-id="2ecad-377">로컬 컴퓨터에서 Office 365 조직에 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 여 Windows powershell을 열고 다음 명령을 실행 하 여 [Exchange Online PowerShell에 연결](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-377">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [connect to Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) by opening Windows PowerShell and running the following command.</span></span> 
    
   ```
   $UserCredential = Get-Credential
   ```

2. <span data-ttu-id="2ecad-378">Windows PowerShell 자격 증명 요청 대화 상자에서 회사 또는 학교 계정 정보를 입력 하 고 **확인**을 클릭 한 후에 다음 명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-378">In the Windows PowerShell Credential Request dialog box, enter your work or school account information, click **OK**, and then enter the following command.</span></span> 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. <span data-ttu-id="2ecad-379">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-379">Run the following command.</span></span>
    
   ```
   Import-PSSession $Session
   ```

4. <span data-ttu-id="2ecad-380">DEP를 만들려면 다음 명령을 입력 하 여 새-dataencryptionpolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-380">To create a DEP, use the New-DataEncryptionPolicy cmdlet by typing the following command.</span></span>
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   <span data-ttu-id="2ecad-381">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-381">Where:</span></span>
    
   -  <span data-ttu-id="2ecad-p153">*PolicyName* 는 정책에 사용 하려는 이름입니다. 이름에 공백을 포함할 수 없습니다. 예: USA_mailboxes.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p153">*PolicyName*  is the name you want to use for the policy. Names cannot contain spaces. For example, USA_mailboxes.</span></span> 
    
   -  <span data-ttu-id="2ecad-p154">*policydescription* 은 정책에 대 한 정보를 파악 하는 데 도움이 되는 정책에 대 한 사용자 친숙 한 설명입니다. 설명에 공백을 포함할 수 있습니다. 예를 들어 미국 및 지역의 사서함에 대 한 루트 키를 예로 들 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p154">*PolicyDescription*  is a user friendly description of the policy that will help you remember what the policy is for. You can include spaces in the description. For example, Root key for mailboxes in USA and its territories.</span></span> 
    
   -  <span data-ttu-id="2ecad-p155">*KeyVaultURI1* 는 정책의 첫 번째 키에 대 한 URI입니다. 예를 https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01들면입니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p155">*KeyVaultURI1*  is the URI for the first key in the policy. For example, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span></span> 
    
   -  <span data-ttu-id="2ecad-p156">*KeyVaultURI2* 은 정책의 두 번째 키에 대 한 URI입니다. 예를 https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02들면입니다. 두 uri를 쉼표와 공백으로 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p156">*KeyVaultURI2*  is the URI for the second key in the policy. For example, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Separate the two URIs by a comma and a space.</span></span> 
    
   <span data-ttu-id="2ecad-393">예제:</span><span class="sxs-lookup"><span data-stu-id="2ecad-393">Example:</span></span>
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a><span data-ttu-id="2ecad-394">사서함에 DEP 할당</span><span class="sxs-lookup"><span data-stu-id="2ecad-394">Assign a DEP to a mailbox</span></span>
<span data-ttu-id="2ecad-395"><a name="assignDEPtomailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-395"></span></span>

<span data-ttu-id="2ecad-p157">사서함 cmdlet을 사용 하 여 사서함에 DEP를 할당 합니다. 정책을 할당 하 고 나면 Office 365에서 DEP에 지정 된 키를 사용 하 여 사서함을 암호화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p157">Assign the DEP to a mailbox by using the Set-Mailbox cmdlet. Once you assign the policy, Office 365 can encrypt the mailbox with the key designated in the DEP.</span></span>
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

<span data-ttu-id="2ecad-p158">여기서 *MailboxIdParameter* 는 사서함을 지정 합니다. 사서함 cmdlet에 대 한 자세한 내용은 [set-mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p158">Where *MailboxIdParameter* specifies a mailbox. For more information about the Set-Mailbox cmdlet, see [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span></span>
  
### <a name="validate-mailbox-encryption"></a><span data-ttu-id="2ecad-400">사서함 암호화 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="2ecad-400">Validate mailbox encryption</span></span>
<span data-ttu-id="2ecad-401"><a name="validatemailboxencryption"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-401"></span></span>

<span data-ttu-id="2ecad-p159">사서함을 암호화 하는 데 다소 시간이 걸릴 수 있습니다. 처음 정책 할당의 경우에는 서비스에서 사서함을 암호화 하기 전에 사서함에서 다른 데이터베이스로의 이동도 완료 해야 합니다. dep를 변경한 후 또는 사서함에 dep를 처음 할당할 때 암호화 유효성 검사를 시도 하기 전에 72 시간을 기다리는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p159">Encrypting a mailbox can take some time. For first time policy assignment, the mailbox must also complete the move from one database to another before the service can encrypt the mailbox. We recommend that you wait 72 hours before you attempt to validate encryption after you change a DEP or the first time you assign a DEP to a mailbox.</span></span>
  
<span data-ttu-id="2ecad-405">get-mailboxstatistics cmdlet을 사용 하 여 사서함이 암호화 되어 있는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-405">Use the Get-MailboxStatistics cmdlet to determine if a mailbox is encrypted.</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

<span data-ttu-id="2ecad-406">사서함이 암호화 된 경우 IsEncrypted 속성은 **true** 값을 반환 하 고 사서함이 암호화 되지 않은 경우에는 **false** 로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-406">The IsEncrypted property returns a value of **true** if the mailbox is encrypted and a value of **false** if the mailbox is not encrypted.</span></span> 

<span data-ttu-id="2ecad-p160">사서함 이동을 완료 하는 데 걸리는 시간은 처음에 DEP를 할당 하는 사서함 수와 사서함 크기에 따라 달라 집니다. 사서함이 DEP를 할당 한 시간 이후로 암호화 되지 않은 경우 new-moverequest cmdlet을 사용 하 여 암호화 되지 않은 사서함에 대 한 사서함 이동을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p160">The time to complete mailbox moves depends on the number of mailboxes to which you assign a DEP for the first time, as well as the size of the mailboxes. If the mailboxes have not been encrypted after a week from the time you assigned the DEP, initiate a mailbox move for the unencrypted mailboxes by using the New-MoveRequest cmdlet.</span></span>

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a><span data-ttu-id="2ecad-409">Office 365: SharePoint Online 및 비즈니스용 OneDrive에 대 한 고객 키 설정</span><span class="sxs-lookup"><span data-stu-id="2ecad-409">Office 365: Setting up Customer Key for SharePoint Online and OneDrive for Business</span></span>
<span data-ttu-id="2ecad-410"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-410"></span></span>

<span data-ttu-id="2ecad-p161">시작 하기 전에 Azure 키 자격 증명 모음을 설정 하는 데 필요한 작업을 완료 했는지 확인 합니다. 자세한 내용은 [Azure key Vault의 전체 작업 및 Microsoft fasttrack for Customer key](controlling-your-data-using-customer-key.md#AzureSteps) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p161">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="2ecad-413">sharepoint online 및 비즈니스용 OneDrive에 대 한 고객 키를 설정 하려면 Windows PowerShell을 사용 하 여 sharepoint online에 원격으로 연결 하 여 다음 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-413">To set up Customer Key for SharePoint Online and OneDrive for Business, you will need to perform these steps by remotely connecting to SharePoint Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a><span data-ttu-id="2ecad-414">각 SharePoint Online 및 비즈니스용 OneDrive 지역에 대 한 DEP (데이터 암호화 정책)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-414">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>
<span data-ttu-id="2ecad-415"><a name="CreateDEP4SPOODfB"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-415"></span></span>

<span data-ttu-id="2ecad-p162">DEP는 Azure Key Vault에 저장 된 키 집합과 연결 됩니다. 한 지리적 위치에 있는 모든 데이터에 DEP를 적용 합니다 (geo 라고도 함). Office 365 (현재 미리 보기)의 다중 지역 기능을 사용 하는 경우에는 각 지역에 따라 하나의 DEP를 만들 수 있습니다. 다중 geo를 사용 하지 않는 경우에는 SharePoint Online 및 비즈니스용 OneDrive와 함께 사용 하기 위해 Office 365에서 DEP를 하나씩 만들 수 있습니다. 그러면 Office 365에서 DEP에 식별 된 키를 사용 하 여 해당 지역에서 데이터를 암호화 합니다. DEP를 만들려면 이전에 가져온 키 보관소 uri가 필요 합니다. 지침은 [각 Azure 키 자격 증명 모음 키의 URI 가져오기를](controlling-your-data-using-customer-key.md#GetKeyURI) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p162">A DEP is associated with a set of keys stored in Azure Key Vault. You apply a DEP to all of your data in one geographic location, also called a geo. If you use the multi-geo feature of Office 365 (currently in Preview), you can create one DEP per geo. If you are not using multi-geo, you can create one DEP in Office 365 for use with SharePoint Online and OneDrive for Business. Office 365 will then use the keys identified in the DEP to encrypt your data in that geo. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="2ecad-p163">항상! DEP를 만들 때 서로 다른 두 Azure 키 자격 증명 모음에 있는 두 개의 키를 지정 합니다. 이러한 키가 지리적 중복을 보장 하기 위해 별도의 두 Azure 지역에 위치 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p163">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="2ecad-426">DEP를 만들려면 Windows PowerShell을 사용 하 여 SharePoint Online에 원격으로 연결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-426">To create a DEP, you need to remotely connect to SharePoint Online by using Windows PowerShell.</span></span>
  
1. <span data-ttu-id="2ecad-427">로컬 컴퓨터에서 Office 365 조직에 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 여 [SharePoint Online Powershell에 연결](https://technet.microsoft.com/library/fp161372.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-427">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [Connect to SharePoint Online Powershell](https://technet.microsoft.com/library/fp161372.aspx).</span></span>
    
2. <span data-ttu-id="2ecad-428">Microsoft SharePoint Online 관리 셸에서 다음과 같이 [SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-428">In the Microsoft SharePoint Online Management Shell, run the [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) cmdlet as follows:</span></span> 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   <span data-ttu-id="2ecad-p164">DEP를 등록 하면 geo의 데이터에 대 한 암호화가 시작 됩니다. 이 작업은 다소 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p164">When you register the DEP, encryption begins on the data in the geo. This can take some time.</span></span>
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a><span data-ttu-id="2ecad-431">그룹 사이트, 팀 사이트 및 비즈니스용 OneDrive의 암호화 확인</span><span class="sxs-lookup"><span data-stu-id="2ecad-431">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>
<span data-ttu-id="2ecad-432"><a name="validateencryptionSPO"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-432"></span></span>

<span data-ttu-id="2ecad-433">다음과 같이 SPODataEncryptionPolicy cmdlet을 실행 하 여 암호화 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-433">You can check on the status of encryption by running the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

<span data-ttu-id="2ecad-434">이 cmdlet의 출력은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-434">The output from this cmdlet includes:</span></span>
  
- <span data-ttu-id="2ecad-435">기본 키의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-435">The URI of the primary key.</span></span>
    
- <span data-ttu-id="2ecad-436">보조 키의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-436">The URI of the secondary key.</span></span>
    
- <span data-ttu-id="2ecad-p165">geo의 암호화 상태입니다. 가능한 상태는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p165">The encryption status for the geo. Possible states include:</span></span>
    
  - <span data-ttu-id="2ecad-439">**등록 취소 됨:** 고객 키 암호화가 아직 적용 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-439">**Unregistered:** Customer Key encryption has not yet been applied.</span></span> 
    
  - <span data-ttu-id="2ecad-p166">**등록:** 고객 키 암호화가 적용 되었으며 파일을 암호화 하 고 있습니다. geo가이 상태에 있는 경우에는 지리적으로 완료 되는 사이트 비율에 대 한 정보도 함께 확인 하 여 암호화 진행 상태를 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p166">**Registering:** Customer Key encryption has been applied and your files are in the process of being encrypted. If your geo is in this state, you'll also be shown information on what percentage of sites in the geo are complete so that you can monitor encryption progress.</span></span> 
    
  - <span data-ttu-id="2ecad-442">**등록 된 경우:** 고객 키 암호화가 적용 되었으며 모든 사이트의 모든 파일이 암호화 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-442">**Registered:** Customer Key encryption has been applied, and all files in all sites have been encrypted.</span></span> 
    
  - <span data-ttu-id="2ecad-p167">**롤링:** 키 롤이 진행 중입니다. geo가이 상태 이면 진행 상태를 모니터링할 수 있도록 키 롤 작업을 완료 한 사이트 비율에 대 한 정보도 함께 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p167">**Rolling:** A key roll is in progress. If your geo is in this state, you'll also be shown information on what percentage of sites have completed the key roll operation so that you can monitor progress.</span></span> 
    
## <a name="managing-customer-key-for-office-365"></a><span data-ttu-id="2ecad-445">Office 365에 대 한 고객 키 관리</span><span class="sxs-lookup"><span data-stu-id="2ecad-445">Managing Customer Key for Office 365</span></span>
<span data-ttu-id="2ecad-446"><a name="ManageCustomerKey"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-446"></span></span>

<span data-ttu-id="2ecad-447">Office 365에 대 한 고객 키를 설정한 후에는 다음 추가 관리 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-447">After you've set up Customer Key for Office 365, you can perform these additional management tasks.</span></span>
  
- [<span data-ttu-id="2ecad-448">Azure 키 자격 증명 모음 키 복원</span><span class="sxs-lookup"><span data-stu-id="2ecad-448">Restore Azure Key Vault keys</span></span>](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [<span data-ttu-id="2ecad-449">고객 키와 함께 사용 하는 Azure 키 보관소에서 키 롤링 또는 회전</span><span class="sxs-lookup"><span data-stu-id="2ecad-449">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [<span data-ttu-id="2ecad-450">키 보관소 사용 권한 관리</span><span class="sxs-lookup"><span data-stu-id="2ecad-450">Manage key vault permissions</span></span>](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [<span data-ttu-id="2ecad-451">사서함에 할당 된 DEP 확인</span><span class="sxs-lookup"><span data-stu-id="2ecad-451">Determine the DEP assigned to a mailbox</span></span>](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a><span data-ttu-id="2ecad-452">Azure 키 자격 증명 모음 키 복원</span><span class="sxs-lookup"><span data-stu-id="2ecad-452">Restore Azure Key Vault keys</span></span>
<span data-ttu-id="2ecad-453"><a name="RestoreAzureKeyVaultKeys"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-453"></span></span>

<span data-ttu-id="2ecad-p168">복원을 수행 하기 전에 일시 삭제로 제공 되는 복구 기능을 사용 합니다. 사용자 키와 함께 사용 되는 모든 키는 소프트 삭제를 사용 하도록 설정 해야 합니다. 일시 삭제는 휴지통 처럼 작동 하며 복원할 필요 없이 최대 90 일 동안 복구를 허용 합니다. 복구는 키 또는 키 보관소가 손실 된 경우와 같이 극단적인 상황 또는 예외적인 경우에만 필요 합니다. 고객 키와 함께 사용 하기 위해 키를 복원 해야 하는 경우 Azure PowerShell에서 다음과 같이 AzureKeyVaultKey cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p168">Before performing a restore, use the recovery capabilities provided by soft delete. All keys that are used with Customer Key are required to have soft delete enabled. Soft delete acts like a recycle bin and allows recovery for up to 90 days without the need to restore. Restore should only be required in extreme or unusual circumstances, for example if the key or key vault is lost. If you must restore a key for use with Customer Key, in Azure PowerShell, run the Restore-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

<span data-ttu-id="2ecad-459">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-459">For example:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

<span data-ttu-id="2ecad-p169">키 보관소에 같은 이름의 키가 이미 있으면 복원 작업을 수행할 수 없습니다. AzureKeyVaultKey는 키 이름을 포함 하 여 키에 대 한 모든 키 버전 및 메타 데이터를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p169">If a key with the same name already exists in the key vault, the restore operation will fail. Restore-AzureKeyVaultKey restores all key versions and all metadata for the key including the key name.</span></span>
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a><span data-ttu-id="2ecad-462">고객 키와 함께 사용 하는 Azure 키 보관소에서 키 롤링 또는 회전</span><span class="sxs-lookup"><span data-stu-id="2ecad-462">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>
<span data-ttu-id="2ecad-463"><a name="RollCKkey"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-463"></span></span>

<span data-ttu-id="2ecad-p170">Azure 키 자격 증명 모음 또는 고객 키에 따라 롤링 키가 필요 하지는 않습니다. 또한 HSM을 사용 하 여 보호 되는 키의 경우 사실상 손상을 불가능해 집니다. 루트 키가 악의적인 행위자가 소유 하 고 있는 경우에도 Office 365 코드 에서만 사용 하는 방법을 아는 것이 좋습니다. 그러나 키를 롤백하는 것은 고객 키를 통해 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p170">Rolling keys is not required by either Azure Key Vault or by Customer Key. In addition, keys that are protected with an HSM are virtually impossible to compromise. Even if a root key were in the possession of a malicious actor there is no feasible means of using it to decrypt data, since only Office 365 code knows how to use it. However, rolling a key is supported by Customer Key.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="2ecad-p171">명확한 기술 이유가 있는 경우 고객 키와 함께 사용 하는 암호화 키를 롤백하거나 키를 롤 포워드 해야 하는 규정 준수 요구 사항을 명시 해야 합니다. 또한 정책과 연결 된 키를 삭제 하지 마십시오. 키를 롤포워드할 때 이전 키로 암호화 된 콘텐츠가 제공 됩니다. 예를 들어 활성 사서함은 자주 다시 암호화 되 고 비활성, 연결 해제 및 사용 하지 않도록 설정 된 사서함은 여전히 이전 키를 사용 하 여 암호화 될 수 있습니다. SharePoint Online은 복원 및 복구를 위해 콘텐츠 백업을 수행 하므로 이전 키를 사용 하 여 계속 콘텐츠를 보관할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p171">Only roll an encryption key that you use with Customer Key when a clear technical reason exists or a compliance requirement dictates that you have to roll the key. In addition, do not delete any keys that are or were associated with policies. When you roll your keys, there will be content encrypted with the previous keys. For example, while active mailboxes will be re-encrypted frequently, inactive, disconnected, and disabled mailboxes may still be encrypted with the previous keys. SharePoint Online performs backup of content for restore and recovery purposes, so there may still be archived content using older keys. </span></span><br/> <span data-ttu-id="2ecad-p172">데이터의 안전을 보장 하기 위해 SharePoint Online은 한 번에 두 개 이상의 키 롤 작업을 진행 하는 것을 허용 하지 않습니다. 키 자격 증명 모음의 두 키를 롤 포워드 하려면 첫 번째 키 롤 작업이 완전히 완료 될 때까지 기다려야 합니다. 여기서는 키 롤업 작업을 다른 간격으로 엇갈리게 배치 하 여 문제가 되지 않도록 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p172">To ensure the safety of your data, SharePoint Online will allow no more than one Key Roll operation to be in progress at a time. If you want to roll both of the keys in a key vault, you'll need to wait for the first key roll operation to fully complete. Our recommendation is to stagger your key roll operations at different intervals, so that this is not an issue.</span></span> 
  
<span data-ttu-id="2ecad-p173">키를 롤 포워드 하면 기존 키의 새 버전을 요청 하 게 됩니다. 기존 키의 새 버전을 요청 하려면 첫 번째 위치에서 키를 만드는 데 사용한 구문과 동일한 cmdlet, [AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p173">When you roll a key, you are requesting a new version of an existing key. In order to request a new version of an existing key, you use the same cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), with the same syntax that you used to create the key in the first place.</span></span>
  
<span data-ttu-id="2ecad-478">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-478">For example:</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

<span data-ttu-id="2ecad-p174">이 예에서는 contoso **-O365EX-VaultA1-Key001** 이라는 키가 **contoso-O365EX-VaultA1** 자격 증명 모음에 이미 있으므로 새 키 버전이 생성 됩니다. 이 작업을 수행 하면 새 키 버전이 추가 됩니다. 이 작업은 키의 버전 기록에서 이전 키 버전을 유지 하므로 이전에 해당 키로 암호화 된 데이터의 암호를 해독할 수 있습니다. DEP와 연결 된 키를 모두 만들었으면 추가 cmdlet을 실행 하 여 고객 키가 새 키를 사용 하 여 시작 되도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p174">In this example, since a key named **Contoso-O365EX-NA-VaultA1-Key001** already exists in the **Contoso-O365EX-NA-VaultA1** vault, a new key version will be created. The operation adds a new key version. This operation preserves the previous key versions in the key's version history, so that data previously encrypted with that key can still be decrypted. Once you have completed rolling any key that is associated with a DEP, you must then run an additional cmdlet to ensure Customer Key begins using the new key.</span></span> 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="2ecad-483">Azure 키 자격 증명 모음에서 키를 롤백하거나 회전 한 후에 Exchange Online 및 비즈니스용 Skype에서 새 키를 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="2ecad-483">Enable Exchange Online and Skype for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="2ecad-484">Exchange Online 및 비즈니스용 Skype와 함께 사용 되는 dep와 연결 된 Azure 키 자격 증명 키 중 하나를 롤 포워드 하려면 다음 명령을 실행 하 여 dep를 업데이트 하 고 Office 365에서 새 키를 사용 하 여 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-484">When you roll either of the Azure Key Vault keys associated with a DEP used with Exchange Online and Skype for Business, you must run the following command to update the DEP and enable Office 365 to start using the new key.</span></span>
  
<span data-ttu-id="2ecad-485">Office 365에서 사서함을 암호화 하기 위해 새 키를 사용 하도록 고객 키에 지시 하려면 다음과 같이 Set-dataencryptionpolicy cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-485">To instruct Customer Key to use the new key to encrypt mailboxes in Office 365 run the Set-DataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

<span data-ttu-id="2ecad-p175">48 시간 이내에이 정책을 사용 하 여 암호화 된 활성 사서함은 업데이트 된 키와 연결 됩니다. [사서함에 할당 된 DEP 결정](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) 의 단계를 사용 하 여 사서함의 dataencryptionpolicyid 속성 값을 확인 합니다. 이 속성의 값은 업데이트 된 키가 적용 된 후에 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p175">Within 48 hours, the active mailboxes encrypted using this policy will become associated with the updated key. Use the steps in [Determine the DEP assigned to a mailbox](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) to check the value for the DataEncryptionPolicyID property for the mailbox. The value for this property will change once the updated key has been applied.</span></span> 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="2ecad-489">Azure 키 자격 증명 모음에서 키를 롤백하거나 회전 한 후에 SharePoint Online 및 비즈니스용 OneDrive에서 새 키를 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="2ecad-489">Enable SharePoint Online and OneDrive for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="2ecad-490">SharePoint Online 및 비즈니스용 OneDrive와 함께 사용 되는 dep와 연결 된 Azure Key 자격 증명 키 중 하나를 롤 포워드 하려면 [SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) cmdlet을 실행 하 여 DEP를 업데이트 하 고 Office 365에서 새 키를 사용 하 여 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-490">When you roll either of the Azure Key Vault keys associated with a DEP used with SharePoint Online and OneDrive for Business, you must run the [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) cmdlet to update the DEP and enable Office 365 to start using the new key.</span></span> 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

<span data-ttu-id="2ecad-p176">이렇게 하면 SharePoint Online 및 비즈니스용 OneDrive에 대 한 키 롤 작업이 시작 됩니다. 이 작업은 즉시 수행 되지 않습니다. 키 롤 작업의 진행률을 확인 하려면 다음과 같이 SPODataEncryptionPolicy cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p176">This will start the key roll operation for SharePoint Online and OneDrive for Business. This action is not immediate. To see the progress of the key roll operation, run the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a><span data-ttu-id="2ecad-494">키 보관소 사용 권한 관리</span><span class="sxs-lookup"><span data-stu-id="2ecad-494">Manage key vault permissions</span></span>
<span data-ttu-id="2ecad-495"><a name="Managekeyvaultperms"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-495"></span></span>

<span data-ttu-id="2ecad-p177">키 보관소 권한을 확인 하 고 제거 하는 데 사용할 수 있는 몇 가지 cmdlet이 제공 됩니다. 예를 들어 직원이 팀을 떠날 때 사용 권한을 제거 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p177">Several cmdlets are available that enable you to view and, if necessary, remove key vault permissions. You might need to remove permissions, for example, when an employee leaves the team.</span></span>
  
<span data-ttu-id="2ecad-498">키 보관소 권한을 확인 하려면 AzureRmKeyVault cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-498">To view key vault permissions, run the Get-AzureRmKeyVault cmdlet:</span></span>
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

<span data-ttu-id="2ecad-499">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-499">For example:</span></span>
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

<span data-ttu-id="2ecad-500">관리자의 사용 권한을 제거 하려면 AzureRmKeyVaultAccessPolicy cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-500">To remove an administrator's permissions, run the Remove-AzureRmKeyVaultAccessPolicy cmdlet:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

<span data-ttu-id="2ecad-501">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-501">For example:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a><span data-ttu-id="2ecad-502">사서함에 할당 된 DEP 확인</span><span class="sxs-lookup"><span data-stu-id="2ecad-502">Determine the DEP assigned to a mailbox</span></span>
<span data-ttu-id="2ecad-503"><a name="DeterminemailboxDEP"> </a></span><span class="sxs-lookup"><span data-stu-id="2ecad-503"></span></span>

<span data-ttu-id="2ecad-p178">사서함에 할당 된 DEP를 확인 하려면 get-mailboxstatistics cmdlet을 사용 합니다. cmdlet은 고유 식별자 (GUID)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p178">To determine the DEP assigned to a mailbox, use the Get-MailboxStatistics cmdlet. The cmdlet returns a unique identifier (GUID).</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

<span data-ttu-id="2ecad-p179">여기서 *GeneralMailboxOrMailUserIdParameter* 는 사서함을 지정 합니다. get-mailboxstatistics cmdlet에 대 한 자세한 내용은 [get-get-mailboxstatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2ecad-p179">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox. For more information about the Get-MailboxStatistics cmdlet, see [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span></span>
  
<span data-ttu-id="2ecad-508">GUID를 사용 하 여 다음 cmdlet을 실행 하 여 사서함이 할당 된 DEP의 대화명을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-508">Use the GUID to find out the friendly name of the DEP to which the mailbox is assigned by running the following cmdlet.</span></span>
  
```
Get-DataEncryptionPolicy <GUID>
```

<span data-ttu-id="2ecad-509">여기서 *GUID* 는 이전 단계의 get-mailboxstatistics cmdlet에서 반환 하는 guid입니다.</span><span class="sxs-lookup"><span data-stu-id="2ecad-509">Where *GUID* is the GUID returned by the Get-MailboxStatistics cmdlet in the previous step.</span></span> 
  

