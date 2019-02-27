---
title: 새로운 Office 365 메시지 암호화 기능 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: 새로운 Office 365 메시지 암호화 기능이 Azure Information Protection을 기반으로 구축 되 면 조직에서 조직 내부 및 외부 사용자와 보호 된 전자 메일 통신을 사용할 수 있습니다. 새로운 OME 기능은 다른 Office 365 조 직, Outlook.com, Gmail 및 기타 전자 메일 서비스와 함께 작동 합니다.
ms.openlocfilehash: 90247a7e3cd7e5978eb144a2b6f66a9de21a8f96
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296191"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a><span data-ttu-id="ea291-104">새로운 Office 365 메시지 암호화 기능 설정</span><span class="sxs-lookup"><span data-stu-id="ea291-104">Set up new Office 365 Message Encryption capabilities</span></span>

<span data-ttu-id="ea291-p102">새 Office 365 메시지 암호화 (OME) 기능을 사용 하면 조직에서 모든 장치에 있는 모든 사용자와 보호 된 전자 메일을 공유할 수 있습니다. 사용자는 Outlook.com, Gmail 및 기타 전자 메일 서비스를 사용 하는 office 365 고객 뿐만 아니라 다른 office 365 조직과 보호 된 메시지를 교환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-p102">The new Office 365 Message Encryption (OME) capabilities allow organizations to share protected email with anyone on any device. Users can exchange protected messages with other Office 365 organizations, as well as non-Office 365 customers using Outlook.com, Gmail, and other email services.</span></span>


>[!NOTE]
><span data-ttu-id="ea291-p103">이 문서는 관리자 및 IT 전문가를 위한 것입니다. 최종 사용자 인 경우 [Office 365 메시지 암호화 (OME)](ome.md) 에서 해당 솔루션에 대 한 문서 목록을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea291-p103">This article is intended for administrators and IT professionals. If you're an end-user, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) for appropriate solutions.</span></span>

<span data-ttu-id="ea291-109">Office 365 테 넌 트에서 새로운 OME 기능을 사용할 수 있도록 하려면 아래 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-109">Follow the steps below to ensure that the New OME capabilities are available in your Office 365 tenant.</span></span> 

## <a name="verify-azure-rights-management-arm-is-active"></a><span data-ttu-id="ea291-110">ARM (Azure 권한 관리)이 활성화 되어 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="ea291-110">Verify Azure Rights Management (ARM) is active</span></span>

>[!NOTE]
><span data-ttu-id="ea291-111">새로운 OME 기능을 사용 하 여 azure [Information protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection)의 보호 기능 [(ARM (azure Rights Management)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms)에서 사용한 기술)을 활용할 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-111">The new OME capabilities leverage the protection features in [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), the technology used by [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms).</span></span>

<span data-ttu-id="ea291-p104">새 OME 기능을 사용 하는 유일한 필수 구성 요소는 Office 365 테 넌 트에서 [ARM (Azure 권한 관리)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) 을 활성화 해야 한다는 것입니다. 이 경우에는 Office 365에서 새 OME 기능을 자동으로 활성화 하므로 작업을 수행할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-p104">The only prerequisite for using the new OME capabilities is that [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) must be activated in your Office 365 tenant. If it is, Office 365 activates the new OME capabilities automatically and you don't need to do anything.</span></span> 

<span data-ttu-id="ea291-p105">또한 ARM은 가장 적합 한 요금제에 대해서도 자동으로 활성화 되므로이 두 가지 측면에서 어떤 작업을 수행 하지 않아도 됩니다. 자세한 내용은 [Azure 권한 관리 정품 인증](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea291-p105">ARM is also activated automatically for most eligible plans, so you probably don't have to do anything in this regard either. See [Activating Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) for more.</span></span>

>[!IMPORTANT]
><span data-ttu-id="ea291-p106">Exchange Online에서 AD RMS (Active Directory Rights Management service)를 사용 하는 경우 새 OME 기능을 사용 하려면 먼저 [Azure Information Protection로 마이그레이션해야](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) 합니다. AD RMS는 ARM과 호환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-p106">If you use Active Directory Rights Management service (AD RMS) with Exchange Online, you need to [migrate to Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) before you can use the new OME capabilities. AD RMS is not compatible with ARM.</span></span>  

<span data-ttu-id="ea291-118">자세한 내용은 다음을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea291-118">For more, see:</span></span>

- <span data-ttu-id="ea291-119">[새 OME 기능을 사용 하는 데 필요한 구독은 무엇입니까?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) 구독 계획에 ARM이 포함 된 Azure Information Protection이 포함 되어 있는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-119">[What subscriptions do I need to use the new OME capabilities?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) to check whether your subscription plan includes Azure Information Protection (which includes ARM).</span></span>   
-  <span data-ttu-id="ea291-120">[Azure information Protection](https://azure.microsoft.com/en-us/services/information-protection/) 적격 구독 구입에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-120">[Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) for information about purchasing an eligible subscription.</span></span>  

### <a name="manually-activating-arm"></a><span data-ttu-id="ea291-121">ARM을 수동으로 활성화</span><span class="sxs-lookup"><span data-stu-id="ea291-121">Manually activating ARM</span></span>

<span data-ttu-id="ea291-122">ARM을 사용 하지 않도록 설정 했거나 어떤 이유로 자동으로 활성화 되지 않은 경우에서 다음 위치에서 수동으로 정품 인증을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-122">If you disabled ARM, or if it was not automatically activated for any reason, you can activated it manually in the :</span></span>

- <span data-ttu-id="ea291-123">**office 365 관리 센터**: 지침은 [office 365 관리 센터에서 Azure Rights Management를 활성화 하는 방법를](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea291-123">**Office 365 admin center**: See [How to activate Azure Rights Management from the Office 365 admin center](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) for instructions</span></span>
- <span data-ttu-id="ea291-124">**azure portal**: 지침을 보려면 [azure portal에서 azure Rights Management를 활성화 하는 방법을](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea291-124">**Azure portal**: See [How to activate Azure Rights Management from the Azure portal](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) for instructions.</span></span> 


## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a><span data-ttu-id="ea291-125">Azure Information Protection 테 넌 트 키 관리 구성</span><span class="sxs-lookup"><span data-stu-id="ea291-125">Configure management of your Azure Information Protection tenant key</span></span>

<span data-ttu-id="ea291-p107">이 단계는 선택 사항입니다. Microsoft가 Azure Information Protection의 루트 키를 관리 하도록 허용 하는 것은 대부분의 Office 365 테 넌 트에 대 한 기본 설정 및 권장 되는 모범 사례입니다. 이 경우에는 작업을 수행 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-p107">This is an optional step. Allowing Microsoft to manage the root key for Azure Information Protection is the default setting and recommended best practice for most Office 365 tenants. If this is the case, you don't need to do anything.</span></span> 

<span data-ttu-id="ea291-p108">규정 준수 요구 사항 예를 들면, 고유한 루트 키를 생성 하 고 관리 하는 데 필요할 수 있는 몇 가지 이유가 있습니다 (사용자가 직접 키를 가져옵니다 (byok). 이 경우 새 OME 기능을 설정 하기 전에 필요한 단계를 완료 하는 것이 좋습니다. 자세한 내용은 [Azure Information Protection 테 넌 트 키 계획 및 구현](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea291-p108">There are many reasons, for example compliance requirements, that may necessitate you generating and managing your own root key (also known as bring your own key (BYOK)). If this is the case, we recommend that you complete the required steps before setting up the new OME capabilities. See [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) for more.</span></span> 


## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a><span data-ttu-id="ea291-132">Exchange Online PowerShell에서 새 OME 구성 확인</span><span class="sxs-lookup"><span data-stu-id="ea291-132">Verify new OME configuration in Exchange Online PowerShell</span></span>

<span data-ttu-id="ea291-133">Office 365 테 넌 트가 [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)의 새 OME 기능을 사용 하도록 올바르게 구성 되어 있는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-133">You can verify that your Office 365 tenant is properly configured to use the new OME capabilities in [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>
  
1. <span data-ttu-id="ea291-134">Office 365 테 넌 트에서 전역 관리자 권한이 있는 계정을 사용 하 여 [Exchange Online PowerShell에 연결](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-134">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="ea291-135">다음 구문을 사용 하 여 irmconfiguration cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-135">Run the Test-IRMConfiguration cmdlet using the following syntax:</span></span>

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   <span data-ttu-id="ea291-136">**예**:</span><span class="sxs-lookup"><span data-stu-id="ea291-136">**Example**:</span></span> 
   
     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```
     
     - <span data-ttu-id="ea291-p109">보낸 사람 전자 메일을 제공 하는 것은 선택 사항 이지만 시스템에서 추가 검사를 수행 합니다. Office 365 테 넌 트에서 모든 사용자의 전자 메일 주소를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-p109">Providing a sender email is optional, but forces the system to perform additional checks. Use the email address of any user in your Office 365 tenant.</span></span> 
     
    <span data-ttu-id="ea291-139">결과는 다음과 비슷해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-139">Your results should be similar to:</span></span>

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

   - <span data-ttu-id="ea291-140">Office 365 조직 이름이 *Contoso*를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-140">Your Office 365 organization name will replace *Contoso*.</span></span>

   - <span data-ttu-id="ea291-p110">기본 서식 파일 이름은 위에 표시 된 이름과 다를 수 있습니다. 자세한 내용은 [Azure Information Protection의 서식 파일 구성 및 관리](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea291-p110">The default template names may be different from those displayed above. See [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) for more.</span></span>

3. <span data-ttu-id="ea291-143">Remove-PSSession cmdlet을 실행 하 여 권한 관리 서비스와의 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-143">Run the Remove-PSSession cmdlet to disconnect from the Rights Management service.</span></span>
    
     ```powershell
     Remove-PSSession $session
     ```

## <a name="update-mail-flow-rules-to-use-new-ome-capabilities"></a><span data-ttu-id="ea291-144">메일 흐름 규칙을 업데이트 하 여 새 OME 기능 사용</span><span class="sxs-lookup"><span data-stu-id="ea291-144">Update mail flow rules to use new OME capabilities</span></span>

<span data-ttu-id="ea291-p111">Office 365 테 넌 트에서 [전자 메일을 암호화 하기 위해](define-mail-flow-rules-to-encrypt-email.md) 이전에 구성 된 메일 흐름 규칙이 있는 경우 이러한 기존 규칙을 업데이트 하 여 새 OME 기능을 사용 해야 합니다. 새 배포의 경우에는이 단계를 수행 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-p111">If there are previously configured [mail flow rules to encrypt email](define-mail-flow-rules-to-encrypt-email.md) in your Office 365 tenant, you need to update these existing rules to use the new OME capabilities. For new deployments, this step is unnecessary at this stage.</span></span>   

>[!Note]
><span data-ttu-id="ea291-p112">메일 흐름 규칙은 전자 메일 메시지를 암호화 하는 조건 및 암호화를 제거 해야 하는 경우를 정의 합니다. 자세한 내용은 [Office 365에서 전자 메일 메시지를 암호화 하기 위한 메일 흐름 규칙 정의를](define-mail-flow-rules-to-encrypt-email.md) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea291-p112">Mail flow rules define the conditions under which email messages are encrypted, and when encryption should be removed. See [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md) for more.</span></span>

<span data-ttu-id="ea291-149">새 OME 기능을 사용 하도록 기존 규칙을 업데이트 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-149">To update existing rules to use the new OME capabilities:</span></span>

1. <span data-ttu-id="ea291-150">Office 365 관리 센터에서 **관리 센터 > Exchange**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-150">In the Office 365 admin center, go to **Admin centers > Exchange**.</span></span>

2. <span data-ttu-id="ea291-151">Exchange 관리 센터에서 **메일 흐름 > 규칙**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-151">In the Exchange admin center, go to **Mail flow > Rules**.</span></span> 
3. <span data-ttu-id="ea291-152">각 규칙에 대해 **다음을 수행 합니다**.</span><span class="sxs-lookup"><span data-stu-id="ea291-152">For each rule, in **Do the following**:</span></span>
    - <span data-ttu-id="ea291-153">**메시지 보안 수정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-153">Select **Modify the message security**.</span></span>
    - <span data-ttu-id="ea291-154">**Office 365 메시지 암호화 및 권한 보호 적용을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-154">Select **Apply Office 365 Message Encryption and rights protection**.</span></span>
    - <span data-ttu-id="ea291-155">목록에서 RMS 템플릿을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-155">Select an RMS template from the list</span></span>
    - <span data-ttu-id="ea291-156">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-156">Select **Save**.</span></span>
    - <span data-ttu-id="ea291-157">**확인**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-157">Select **OK**.</span></span>
  
>[!IMPORTANT]
><span data-ttu-id="ea291-158">기존 메일 흐름 규칙을 업데이트 하지 않으면 사용자는 새 OME 기능 대신 이전 HTML 첨부 파일 형식을 사용 하는 암호화 된 메일을 계속 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea291-158">If you do not update existing mail flow rules, your users will continue to receive encrypted mail that uses the previous HTML attachment format, instead of the new OME capabilities.</span></span>
