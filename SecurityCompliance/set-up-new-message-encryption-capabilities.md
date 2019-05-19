---
title: 새로운 Office 365 메시지 암호화 기능 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 새로운 Office 365 메시지 암호화 기능이 Azure Information Protection을 기반으로 구축 되 면 조직에서 조직 내부 및 외부 사용자와 보호 된 전자 메일 통신을 사용할 수 있습니다. 새로운 OME 기능은 다른 Office 365 조 직, Outlook.com, Gmail 및 기타 전자 메일 서비스와 함께 작동 합니다.
ms.openlocfilehash: 415e598a28033271b115aff639fb1ddd7a6345af
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156510"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a><span data-ttu-id="a0839-104">새로운 Office 365 메시지 암호화 기능 설정</span><span class="sxs-lookup"><span data-stu-id="a0839-104">Set up new Office 365 Message Encryption capabilities</span></span>

<span data-ttu-id="a0839-105">새 Office 365 메시지 암호화 (OME) 기능을 사용 하면 조직에서 모든 장치에 있는 모든 사용자와 보호 된 전자 메일을 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-105">The new Office 365 Message Encryption (OME) capabilities allow organizations to share protected email with anyone on any device.</span></span> <span data-ttu-id="a0839-106">사용자는 Outlook.com, Gmail 및 기타 전자 메일 서비스를 사용 하는 Office 365 고객 뿐만 아니라 다른 Office 365 조직과 보호 된 메시지를 교환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-106">Users can exchange protected messages with other Office 365 organizations, as well as non-Office 365 customers using Outlook.com, Gmail, and other email services.</span></span>

||
|:-----|
|<span data-ttu-id="a0839-107">이 문서는 Office 365 메시지 암호화에 대 한 보다 광범위 한 문서에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-107">This article is part of a larger series of articles about Office 365 Message Encryption.</span></span> <span data-ttu-id="a0839-108">이 문서는 관리자 및 IT 전문가를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-108">This article is intended for administrators and IT Pros.</span></span> <span data-ttu-id="a0839-109">암호화 된 메시지를 보내거나 받는 방법에 대 한 정보를 찾으려는 경우에는 [Office 365 메시지 암호화 (OME)](ome.md) 의 문서 목록을 참조 하 여 요구 사항에 가장 적합 한 문서를 검색 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0839-109">If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

<span data-ttu-id="a0839-110">Office 365 조직에서 새로운 OME 기능을 사용할 수 있도록 하려면 아래 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-110">Follow the steps below to ensure that the New OME capabilities are available in your Office 365 organization.</span></span>

## <a name="verify-that-azure-rights-management-is-active"></a><span data-ttu-id="a0839-111">Azure 권한 관리가 활성 상태 인지 확인</span><span class="sxs-lookup"><span data-stu-id="a0839-111">Verify that Azure Rights Management is active</span></span>

<span data-ttu-id="a0839-112">새로운 OME 기능은 azure [RMS (권한 관리 서비스)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection)의 보호 기능을 활용 하며, [azure Information protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) 에서 암호화 및 액세스 제어를 통해 전자 메일 및 문서를 보호 하는 데 사용 하는 기술입니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-112">The new OME capabilities leverage the protection features in [Azure Rights Management Services (Azure RMS)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), the technology used by [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) to protect emails and documents via encryption and access controls.</span></span>

<span data-ttu-id="a0839-113">새 OME 기능을 사용 하는 유일한 필수 구성 요소는 조직의 테 넌 트에서 [Azure 권한 관리](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) 를 활성화 해야 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-113">The only prerequisite for using the new OME capabilities is that [Azure Rights Management](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) must be activated in your organization's tenant.</span></span> <span data-ttu-id="a0839-114">이 경우에는 Office 365에서 새 OME 기능을 자동으로 활성화 하므로 작업을 수행할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-114">If it is, Office 365 activates the new OME capabilities automatically and you don't need to do anything.</span></span>

<span data-ttu-id="a0839-115">또한 가장 적합 한 요금제에 대해서도 Azure RMS가 자동으로 활성화 되므로, 어떤 작업을 수행 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-115">Azure RMS is also activated automatically for most eligible plans, so you probably don't have to do anything in this regard either.</span></span> <span data-ttu-id="a0839-116">자세한 내용은 [Azure 권한 관리 활성화](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0839-116">See [Activating Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) for more information.</span></span>

>[!IMPORTANT]
><span data-ttu-id="a0839-117">Exchange Online에서 AD RMS (Active Directory Rights Management service)를 사용 하는 경우 새 OME 기능을 사용 하려면 먼저 [Azure Information Protection로 마이그레이션해야](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-117">If you use Active Directory Rights Management service (AD RMS) with Exchange Online, you need to [migrate to Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) before you can use the new OME capabilities.</span></span> <span data-ttu-id="a0839-118">OME는 AD RMS와 호환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-118">OME is not compatible with AD RMS.</span></span>  

<span data-ttu-id="a0839-119">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a0839-119">For more information, see:</span></span>

- <span data-ttu-id="a0839-120">[새 OME 기능을 사용 하는 데 필요한 구독은 무엇입니까?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) 구독 계획에 azure RMS 기능을 포함 하는 Azure Information Protection이 포함 되어 있는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-120">[What subscriptions do I need to use the new OME capabilities?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) to check whether your subscription plan includes Azure Information Protection (which includes Azure RMS functionality).</span></span>
- <span data-ttu-id="a0839-121">[Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) 적격 구독 구입에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-121">[Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) for information about purchasing an eligible subscription.</span></span>  

### <a name="manually-activating-azure-rights-management"></a><span data-ttu-id="a0839-122">Azure 권한 관리 수동 활성화</span><span class="sxs-lookup"><span data-stu-id="a0839-122">Manually activating Azure Rights Management</span></span>

<span data-ttu-id="a0839-123">Azure RMS를 사용 하지 않도록 설정 했거나 어떤 이유로 자동으로 활성화 되지 않은 경우에서 다음에서 수동으로 활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-123">If you disabled Azure RMS, or if it was not automatically activated for any reason, you can activate it manually in the:</span></span>

- <span data-ttu-id="a0839-124">**Office 365 관리 센터**: 지침을 보려면 [office 365 관리 센터에서 Azure Rights Management를 활성화 하는 방법을](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0839-124">**Office 365 admin center**: See [How to activate Azure Rights Management from the Office 365 admin center](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) for instructions.</span></span>
- <span data-ttu-id="a0839-125">**Azure portal**: 지침을 보려면 [Azure Portal에서 azure Rights Management를 활성화 하는 방법을](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0839-125">**Azure portal**: See [How to activate Azure Rights Management from the Azure portal](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) for instructions.</span></span>

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a><span data-ttu-id="a0839-126">Azure Information Protection 테 넌 트 키 관리 구성</span><span class="sxs-lookup"><span data-stu-id="a0839-126">Configure management of your Azure Information Protection tenant key</span></span>

<span data-ttu-id="a0839-127">이 단계는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-127">This is an optional step.</span></span> <span data-ttu-id="a0839-128">Microsoft가 Azure Information Protection의 루트 키를 관리 하도록 허용 하는 것은 대부분의 Office 365 테 넌 트에 대 한 기본 설정 및 권장 되는 모범 사례입니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-128">Allowing Microsoft to manage the root key for Azure Information Protection is the default setting and recommended best practice for most Office 365 tenants.</span></span> <span data-ttu-id="a0839-129">이 경우에는 작업을 수행 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-129">If this is the case, you don't need to do anything.</span></span>

<span data-ttu-id="a0839-130">규정 준수 요구 사항 예를 들면, 고유한 루트 키를 생성 하 고 관리 하는 데 필요할 수 있는 몇 가지 이유가 있습니다 (사용자가 직접 키를 가져옵니다 (BYOK).</span><span class="sxs-lookup"><span data-stu-id="a0839-130">There are many reasons, for example compliance requirements, that may necessitate you generating and managing your own root key (also known as bring your own key (BYOK)).</span></span> <span data-ttu-id="a0839-131">이 경우 새 OME 기능을 설정 하기 전에 필요한 단계를 완료 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-131">If this is the case, we recommend that you complete the required steps before setting up the new OME capabilities.</span></span> <span data-ttu-id="a0839-132">자세한 내용은 [Azure Information Protection 테 넌 트 키 계획 및 구현](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0839-132">See [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) for more.</span></span>

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a><span data-ttu-id="a0839-133">Exchange Online PowerShell에서 새 OME 구성 확인</span><span class="sxs-lookup"><span data-stu-id="a0839-133">Verify new OME configuration in Exchange Online PowerShell</span></span>

<span data-ttu-id="a0839-134">Office 365 테 넌 트가 [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)의 새 OME 기능을 사용 하도록 올바르게 구성 되어 있는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-134">You can verify that your Office 365 tenant is properly configured to use the new OME capabilities in [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>
  
1. <span data-ttu-id="a0839-135">Office 365 테 넌 트에서 전역 관리자 권한이 있는 계정을 사용 하 여 [Exchange Online PowerShell에 연결](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-135">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="a0839-136">IRMConfiguration cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-136">Run the Get-IRMConfiguration cmdlet.</span></span>

     <span data-ttu-id="a0839-137">OME가 테 넌 트에 구성 되었음을 나타내는 AzureRMSLicensingEnabled 매개 변수에 대 한 $True 값이 표시 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-137">You should see a value of $True for the AzureRMSLicensingEnabled parameter, which indicates that OME is configured in your tenant.</span></span> <span data-ttu-id="a0839-138">그렇지 않으면 Set-IRMConfiguration을 사용 하 여 OME를 사용 하도록 AzureRMSLicensingEnabled의 값을 $True 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-138">If it is not, use Set-IRMConfiguration to set the value of AzureRMSLicensingEnabled to $True to enable OME.</span></span>

3. <span data-ttu-id="a0839-139">다음 구문을 사용 하 여 IRMConfiguration cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-139">Run the Test-IRMConfiguration cmdlet using the following syntax:</span></span>

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   <span data-ttu-id="a0839-140">**예제**:</span><span class="sxs-lookup"><span data-stu-id="a0839-140">**Example**:</span></span>

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - <span data-ttu-id="a0839-141">보낸 사람 전자 메일을 제공 하는 것은 선택 사항 이지만 시스템에서 추가 검사를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-141">Providing a sender email is optional, but forces the system to perform additional checks.</span></span> <span data-ttu-id="a0839-142">Office 365 테 넌 트에서 모든 사용자의 전자 메일 주소를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-142">Use the email address of any user in your Office 365 tenant.</span></span>

     <span data-ttu-id="a0839-143">결과는 다음과 비슷해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-143">Your results should be similar to:</span></span>

     ```text
    Results : Acquiring RMS Templates ...
                - PASS: RMS Templates acquired.  Templates available: Contoso  - Confidential View Only, Contoso  - Confidential, Do Not
            Forward.
            Verifying encryption ...
                - PASS: Encryption verified successfully.
            Verifying decryption ...
                - PASS: Decryption verified successfully.
            Verifying IRM is enabled ...
                - PASS: IRM verified successfully.

            OVERALL RESULT: PASS
    ```

   - <span data-ttu-id="a0839-144">Office 365 조직 이름이 *Contoso*를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-144">Your Office 365 organization name will replace *Contoso*.</span></span>

   - <span data-ttu-id="a0839-145">기본 서식 파일 이름은 위에 표시 된 이름과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-145">The default template names may be different from those displayed above.</span></span> <span data-ttu-id="a0839-146">자세한 내용은 [Azure Information Protection의 서식 파일 구성 및 관리](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0839-146">See [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) for more.</span></span>

4. <span data-ttu-id="a0839-147">Remove-PSSession cmdlet을 실행 하 여 권한 관리 서비스와의 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-147">Run the Remove-PSSession cmdlet to disconnect from the Rights Management service.</span></span>

     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-mail-flow-rules-to-use-new-ome-capabilities"></a><span data-ttu-id="a0839-148">다음 단계: 새 OME 기능을 사용 하는 메일 흐름 규칙 정의</span><span class="sxs-lookup"><span data-stu-id="a0839-148">Next steps: Define mail flow rules to use new OME capabilities</span></span>

<span data-ttu-id="a0839-149">Office 365 조 직에서 전자 메일을 암호화 하기 위해 이전에 구성 된 메일 흐름 규칙이 있는 경우 새 OME 기능을 사용 하도록 기존 규칙을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-149">If there are previously configured mail flow rules to encrypt email in your Office 365 organization, you need to update the existing rules to use the new OME capabilities.</span></span> <span data-ttu-id="a0839-150">새 배포의 경우 새 메일 흐름 규칙을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-150">For new deployments, you need to create new mail flow rules.</span></span>

>[!IMPORTANT]
><span data-ttu-id="a0839-151">기존 메일 흐름 규칙을 업데이트 하지 않으면 사용자는 새로운 매끄러운 OME 환경이 아닌 이전 HTML 첨부 파일 형식을 사용 하는 암호화 된 메일을 계속 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-151">If you do not update existing mail flow rules, your users will continue to receive encrypted mail that uses the previous HTML attachment format, instead of the new seamless OME experience.</span></span>

<span data-ttu-id="a0839-152">메일 흐름 규칙은 전자 메일 메시지를 암호화 해야 하는 조건 및 해당 암호화를 제거 하는 조건에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-152">Mail flow rules determine under what conditions email messages should be encrypted, as well as conditions for removing that encryption.</span></span> <span data-ttu-id="a0839-153">규칙에 대 한 동작을 설정 하면 규칙 조건과 일치 하는 모든 메시지가 전송 될 때 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-153">When you set an action for a rule, any messages that match the rule conditions are encrypted when they're sent.</span></span>
  
<span data-ttu-id="a0839-154">OME에 대 한 메일 흐름 규칙을 만드는 단계는 [Office 365에서 전자 메일 메시지를 암호화 하기 위한 메일 흐름 규칙 정의](define-mail-flow-rules-to-encrypt-email.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a0839-154">For steps on creating mail flow rules for OME, see [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md).</span></span>

<span data-ttu-id="a0839-155">새 OME 기능을 사용 하도록 기존 규칙을 업데이트 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-155">To update existing rules to use the new OME capabilities:</span></span>

1. <span data-ttu-id="a0839-156">Office 365 관리 센터에서 **관리 센터 _GT_ Exchange**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-156">In the Office 365 admin center, go to **Admin centers > Exchange**.</span></span>
2. <span data-ttu-id="a0839-157">Exchange 관리 센터에서 **메일 흐름 _GT_ 규칙**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-157">In the Exchange admin center, go to **Mail flow > Rules**.</span></span>
3. <span data-ttu-id="a0839-158">각 규칙에 대해 **다음을 수행 합니다**.</span><span class="sxs-lookup"><span data-stu-id="a0839-158">For each rule, in **Do the following**:</span></span>
    - <span data-ttu-id="a0839-159">**메시지 보안 수정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-159">Select **Modify the message security**.</span></span>
    - <span data-ttu-id="a0839-160">**Office 365 메시지 암호화 및 권한 보호 적용을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-160">Select **Apply Office 365 Message Encryption and rights protection**.</span></span>
    - <span data-ttu-id="a0839-161">목록에서 RMS 템플릿을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-161">Select an RMS template from the list.</span></span>
    - <span data-ttu-id="a0839-162">**저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-162">Select **Save**.</span></span>
    - <span data-ttu-id="a0839-163">**확인**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a0839-163">Select **OK**.</span></span>
