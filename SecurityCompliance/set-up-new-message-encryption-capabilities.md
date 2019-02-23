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
ms.openlocfilehash: eddafca15fa4efdd3f929145e7933a3b7dfb5f27
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220648"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a><span data-ttu-id="bdffa-104">새로운 Office 365 메시지 암호화 기능 설정</span><span class="sxs-lookup"><span data-stu-id="bdffa-104">Set up new Office 365 Message Encryption capabilities</span></span>

<span data-ttu-id="bdffa-p102">Azure Information protection의 보호 기능을 활용 하는 새로운 Office 365 메시지 암호화 (OME) 기능을 사용 하면 조직에서 모든 장치에 있는 모든 사용자와 보호 된 전자 메일을 쉽게 공유할 수 있습니다. 사용자는 Outlook.com, Gmail 및 기타 전자 메일 서비스를 사용 하는 office 365 이외의 다른 office 365 조직과 보호 된 메시지를 주고 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p102">With the new Office 365 Message Encryption (OME) capabilities, which leverage the protection features in Azure Information Protection, your organization can easily share protected email with anyone on any device. Users can send and receive protected messages with other Office 365 organizations as well as non-Office 365 customers using Outlook.com, Gmail, and other email services.</span></span>

||
|:-----|
|<span data-ttu-id="bdffa-p103">이 문서는 Office 365 메시지 암호화에 대 한 보다 광범위 한 문서에 포함 되어 있습니다. 이 문서는 관리자와 itpros 전문가를 위한 것입니다. 암호화 된 메시지를 보내거나 받는 방법에 대 한 정보를 찾으려는 경우에는 [Office 365 메시지 암호화 (OME)](ome.md) 의 문서 목록을 참조 하 여 요구 사항에 가장 적합 한 문서를 검색 하세요.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p103">This article is part of a larger series of articles about Office 365 Message Encryption. This article is intended for administrators and ITPros. If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

## <a name="get-started-with-ome-by-activating-azure-rights-management-part-of-azure-information-protection"></a><span data-ttu-id="bdffa-110">azure 권한 관리, azure Information Protection의 일부를 활성화 하 여 OME을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-110">Get started with OME by activating Azure Rights Management, part of Azure Information Protection</span></span>

<span data-ttu-id="bdffa-p104">이제 새 OME 기능을 쉽게 시작할 수 있습니다. 2 월 2018 일 현재 Office 365에서는 데이터 센터 내에서 적합 한 조직의 새 OME 기능을 자동으로 사용 하도록 설정 합니다. 조직이 새 Office 365 테 넌 트이 고 조직에 적절 한 구독이 있는 경우에 적합 합니다. azure **Information Protection의 일부인 azure Rights Management (azure RMS)를 사용 하도록 설정한 경우 Office 365 메시지 암호화를 자동으로 사용 하도록 설정 합니다.** OME을 사용 하도록 설정 하기 위해 다른 작업을 수행할 필요가 없습니다. azure 권한 관리를 활성화 하려면 [azure 권한 관리 활성화](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service)를 참조 하세요. 구독에 대 한 자세한 내용은 [Office 365 메시지 암호화 FAQ](ome-faq.md)에서 "새 OME capabilities?을 사용 하려면 무엇을 해야 합니까?"를 참조 하십시오. azure information protection에 대 한 구독을 구입 하는 방법에 대 한 자세한 내용은 [azure information protection](https://azure.microsoft.com/services/information-protection/)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p104">It's now easy to get started with the new OME capabilities. As of February 2018, Office 365 automatically enables the new OME capabilities for eligible organizations within our datacenters. Your organization is eligible if it is a new Office 365 tenant and your organization has the appropriate subscriptions. **If you have enabled Azure Rights Management (Azure RMS), part of Azure Information Protection, then we automatically enable Office 365 Message Encryption for you.** You don't have to do anything else to enable OME. To activate Azure Rights Management, see [Activating Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). For information on subscriptions, see "What subscriptions do I need to use the new OME capabilities?" in the [Office 365 Message Encryption FAQ](ome-faq.md). For information about purchasing a subscription to Azure Information Protection, see [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>
  
<span data-ttu-id="bdffa-p105">AD RMS (Active Directory Rights Management services)와 함께 Exchange Online을 사용 하는 경우에는 이러한 새로운 기능을 즉시 사용 하도록 설정할 수 없습니다. 대신 AD RMS에서 Azure Information Protection로 마이그레이션을 수행 해야 합니다. 마이그레이션이 완료 되 면 다음 단계를 성공적으로 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p105">If you are using Exchange Online with Active Directory Rights Management service (AD RMS), you can't enable these new capabilities right away. Instead, you need to migrate from AD RMS to Azure Information Protection first. When you've finished the migration, you can successfully complete these steps.</span></span>
  
<span data-ttu-id="bdffa-123">Azure Information Protection으로 마이그레이션하지 않고 Exchange Online에서 온-프레미스 AD RMS를 계속 사용 하도록 선택 하는 경우 이러한 새로운 기능을 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-123">If you choose to continue to use on-premises AD RMS with Exchange Online instead of migrating to Azure Information Protection, you will not be able to use these new capabilities.</span></span>
  
## <a name="how-the-new-capabilities-for-ome-work"></a><span data-ttu-id="bdffa-124">OME의 새로운 기능 작동 방식</span><span class="sxs-lookup"><span data-stu-id="bdffa-124">How the new capabilities for OME work</span></span>

<span data-ttu-id="bdffa-p106">새로운 Office 365 메시지 암호화 기능은 azure Information protection에서 azure RMS (azure 권한 관리) 라고도 하는 보호 기능을 사용 합니다. 여기에는 전자 메일을 보호 하는 데 도움이 되는 암호화, id 및 권한 부여 정책이 포함 됩니다. 권한 관리 템플릿, [전달 금지 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)및 [암호화 전용 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 사용 하 여 메시지를 암호화할 수 있습니다. 그러면 사용자가 이러한 옵션을 사용 하 여 전자 메일 메시지와 다양 한 Office 365 첨부 파일을 암호화할 수 있습니다. 지원 되는 첨부 파일 형식에 대 한 전체 목록은 [전자 메일 메시지에 대 한 irm 소개에서 "irm 정책이 메시지에 첨부 될 때 확인 되는 파일 형식"](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM)을 참조 하십시오. 관리자는이 보호를 적용 하는 메일 흐름 규칙을 정의할 수도 있습니다. 예를 들어 특정 받는 사람에 게 주소를 지정 하거나 제목 줄에 특정 단어가 포함 된 보호 되지 않는 모든 메시지가 무단으로 액세스 되지 않도록 보호 되며 받는 사람이 메시지 내용을 복사 하거나 인쇄할 수 없는 규칙을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p106">The new Office 365 Message Encryption capabilities use the protection capabilities, also called Azure Rights Management (Azure RMS), from Azure Information Protection. This includes encryption, identity, and authorization policies to help secure your email. You can encrypt messages by using rights management templates, the [Do Not Forward option](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails), and the [encrypt-only option](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails). Users can then encrypt email messages and a variety of Office 365 attachments by using these options. For a full list of supported attachment types, see ["File types covered by IRM policies when they are attached to messages" in Introduction to IRM for email messages](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM). As an administrator, you can also define mail flow rules to apply this protection. For example, you can define a rule where all unprotected messages that are addressed to a specific recipient or that contain specific words in the subject line are protected from unauthorized access, and the recipients can't copy or print the contents of the message.</span></span>
  
<span data-ttu-id="bdffa-p107">이전 버전의 OME과 달리 이러한 새로운 기능은 조직 내부에서 메일을 보내는 지, 아니면 Office 365 외부의 받는 사람에 게 제공 되는지 여부에 관계 없이 통합 된 보낸 사람을 위한 것입니다. 또한 outlook 2016 또는 웹용 outlook에서 Office 365 계정으로 전송 되는 보호 된 전자 메일 메시지를 받는 받는 사람은 메시지를 확인 하기 위해 추가 작업을 수행할 필요가 없습니다. 완벽 하 게 작동 합니다. 다른 전자 메일 클라이언트와 전자 메일 서비스 공급자를 사용 하는 받는 사람도 향상 된 환경을 제공 합니다. 자세한 내용은 [Office 365의 보호 된 메시지에 대 한](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) 정보 및 [보호 된 메시지를 여는 방법](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p107">Unlike the previous version of OME, these new capabilities provide a unified sender experience whether you're sending mail inside your organization or to recipients outside of Office 365. In addition, recipients who receive a protected email message sent to an Office 365 account in Outlook 2016 or Outlook on the web, don't have to take any additional action to view the message. It works seamlessly. Recipients using other email clients and email service providers also have an improved experience. For information, see [Learn about protected messages in Office 365](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) and [How do I open a protected message](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098).</span></span>

<span data-ttu-id="bdffa-137">이전 버전의 OME와 새 OME 기능 간의 차이점에 대 한 자세한 목록은 [OME 버전 비교](ome-version-comparison.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bdffa-137">For a detailed list of the differences between the previous version of OME and the new OME capabilities, see [Compare versions of OME](ome-version-comparison.md).</span></span>
  
## <a name="steps-to-manually-set-up-the-new-capabilities-for-ome"></a><span data-ttu-id="bdffa-138">OME에 대 한 새 기능을 수동으로 설정 하는 단계</span><span class="sxs-lookup"><span data-stu-id="bdffa-138">Steps to manually set up the new capabilities for OME</span></span>

<span data-ttu-id="bdffa-p108">대부분의 Office 365 조직에서는 새로운 OME 기능이 자동으로 사용 하도록 설정 됩니다. 조직에서 OME을 자동으로 사용 하도록 설정 하지 않았거나 새 OME 기능을 해제 한 경우에는 다음 단계에 따라 OME에 대 한 새 기능을 수동으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p108">The new OME capabilities are automatically enabled for most Office 365 organizations. If your organization does not automatically have OME enabled, or if you turned the new OME capabilities off, follow these steps to manually set up the new capabilities for OME.</span></span>
  
### <a name="to-manually-set-up-the-new-capabilities-for-ome"></a><span data-ttu-id="bdffa-141">OME에 대 한 새 기능을 수동으로 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="bdffa-141">To manually set up the new capabilities for OME</span></span>

1. <span data-ttu-id="bdffa-p109">조직에 적합 한 구독을 보유 하 고 있는지 확인 합니다. 구독에 대 한 자세한 내용은 [Office 365 메시지 암호화 FAQ](ome-faq.md)에서 "새 OME capabilities?을 사용 하려면 무엇을 해야 합니까?"를 참조 하세요. azure information protection에 대 한 구독을 구입 하는 방법에 대 한 자세한 내용은 [azure information protection](https://azure.microsoft.com/services/information-protection/)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p109">Ensure you have the right subscription for your organization. For information on subscriptions, see "What subscriptions do I need to use the new OME capabilities?" in the [Office 365 Message Encryption FAQ.](ome-faq.md). For information about purchasing a subscription to Azure Information Protection, see [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

2. <span data-ttu-id="bdffa-p110">Microsoft에서 Azure Information Protection의 루트 키 (기본값)를 관리할 지, 아니면 직접 키를 가져오거나 확인을 통해이 키를 직접 생성 및 관리 하도록 할지 결정 합니다. 이 키를 직접 생성 하 고 관리 하려는 경우에는 OME에 대 한 새 기능을 설정 하기 전에 몇 가지 단계를 완료 해야 합니다. 자세한 내용은 [Azure information Protection 테 넌 트 키 계획 및 구현](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key)를 참조 하세요. OME를 설정 하기 전에이 단계를 완료 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p110">Decide whether you want Microsoft to manage the root key for Azure Information Protection (the default), or generate and manage this key yourself (known as bring your own key, or BYOK). If you want to generate and manage this key yourself, you need to complete some steps before you set up the new capabilities for OME. For more information, see [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key). Microsoft recommends that you complete these steps before you set up OME.</span></span>

3. <span data-ttu-id="bdffa-p111">Azure 권한 관리를 활성화 하 여 OME의 새 기능을 사용 하도록 설정 합니다. 자세한 내용은 [Azure 권한 관리 활성화](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service)를 참조 하세요. 이렇게 하면 Office 365에서 자동으로 새 OME 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p111">Enable the new capabilities for OME by activating Azure Rights Management. For instructions, see [Activating Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). When you do this, Office 365 automatically enables the new OME capabilities for you.</span></span>

    > [!TIP]
    > <span data-ttu-id="bdffa-p112">웹용 Outlook은 해당 UI를 캐시 하므로이 클라이언트를 사용 하는 전자 메일 메시지에 OME에 대 한 새 기능을 적용 하기 전에 하루를 기다리는 것이 좋습니다. 새 구성을 반영 하기 위해 UI를 업데이트 하기 전에 OME의 새 기능을 사용할 수 없습니다. UI를 업데이트 한 후 사용자는 OME의 새 기능을 사용 하 여 전자 메일 메시지를 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p112">Outlook on the Web caches its UI, so it's a good idea to wait a day before you try applying the new capabilities for OME to email messages using this client. Before the UI updates to reflect the new configuration, the new capabilities for OME won't be available. After the UI updates, users can protect email messages by using the new capabilities for OME.</span></span>
  
4. <span data-ttu-id="bdffa-156">반드시 새 메일 흐름 규칙을 설정 하거나 Office 365에서 조직 으로부터 보낸 메시지를 암호화 하는 방법 및 시기를 정의 하는 기존 메일 흐름 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-156">(Optional) Set up new mail flow rules or update existing mail flow rules that define how and when you want Office 365 to encrypt messages sent from your organization.</span></span>

## <a name="verify-that-the-new-capabilities-for-ome-are-configured-properly-by-using-windows-powershell"></a><span data-ttu-id="bdffa-157">Windows PowerShell을 사용 하 여 OME에 대 한 새 기능이 제대로 구성 되어 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="bdffa-157">Verify that the new capabilities for OME are configured properly by using Windows PowerShell</span></span>

<span data-ttu-id="bdffa-158">Exchange Online PowerShell을 통해 OME의 새 기능을 사용 하도록 테 넌 트를 올바르게 구성 했는지 확인 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-158">Follow these steps to verify that your tenant is properly configured to use the new capabilities for OME through Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="bdffa-p113">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p113">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="bdffa-161">다음 구문을 사용 하 여 irmconfiguration cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-161">Run the Test-IRMConfiguration cmdlet using the following syntax:</span></span>

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   <span data-ttu-id="bdffa-162">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-162">For example:</span></span>

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

    <span data-ttu-id="bdffa-p114">여기서 전자 메일 주소는 Office 365 조직에 있는 사용자의 전자 메일 주소입니다. 선택 사항 이지만 보낸 사람 전자 메일 주소를 제공 하면 시스템에서 추가 검사를 수행 합니다. 검색 결과는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p114">Where email address is the email address of a user in your Office 365 organization. While optional, providing a sender email address forces the system to perform additional checks. Your results should look like these:</span></span>

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

    <span data-ttu-id="bdffa-166">여기서 *Contoso* 는 Office 365 조직의 이름으로 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-166">Where *Contoso* is replaced with the name of your Office 365 organization.</span></span>

    <span data-ttu-id="bdffa-167">결과에서 반환 되는 기본 서식 파일의 이름은 위의 결과에 표시 되는 것과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-167">The names of the default templates returned in the results may be different from those displayed in the results above.</span></span>

    <span data-ttu-id="bdffa-p115">기본 서식 파일에 대 한 서식 파일 및 정보에 대 한 자세한 내용은 [Azure information Protection의 템플릿 구성 및 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오. 전달 금지 옵션, 암호화 전용 옵션 및 추가 템플릿을 만드는 방법에 대 한 자세한 내용은 [Azure 권한 관리에 대 한 사용 권한 구성을](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p115">For an introduction to templates and information about the default templates, see [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). For information about the Do Not Forward option, encrypt-only option, and how to create additional templates, or find out what rights are included in an existing template, see [Configuring usage rights for Azure Rights Management](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights).</span></span>

3. <span data-ttu-id="bdffa-170">Remove-PSSession cmdlet을 실행 하 여 권한 관리 서비스와의 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-170">Run the Remove-PSSession cmdlet to disconnect from the Rights Management service.</span></span>
    
     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-new-mail-flow-rules-that-use-the-new-ome-capabilities"></a><span data-ttu-id="bdffa-171">다음 단계: 새 OME 기능을 사용 하는 새 메일 흐름 규칙 정의</span><span class="sxs-lookup"><span data-stu-id="bdffa-171">Next steps: Define new mail flow rules that use the new OME capabilities</span></span>

<span data-ttu-id="bdffa-p116">새 OME 배포의 경우이 단계는 선택 사항 이지만,이 단계는 보내는 메일을 암호화 하기 위해 이미 메일 흐름 규칙이 설정 된 기존 OME 배포에 필요 합니다. 새 OME 기능을 활용 하려면 기존 메일 흐름 규칙을 업데이트 해야 합니다. 그렇지 않으면 사용자는 새로운 OME 환경이 아닌 이전 HTML 첨부 파일 형식을 사용 하는 암호화 된 메일을 계속 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p116">This step is optional for new OME deployments, however, this step is required for existing OME deployments that already have mail flow rules set up to encrypt outgoing mail. If you want to take advantage of the new OME capabilities, you must update your existing mail flow rules. Otherwise, your users will continue to receive encrypted mail that uses the previous HTML attachment format instead of the new, seamless OME experience.</span></span>
  
<span data-ttu-id="bdffa-p117">메일 흐름 규칙은 전자 메일 메시지를 암호화 해야 하는 조건 및 해당 암호화를 제거 하는 조건에 따라 결정 됩니다. 규칙에 대 한 동작을 설정 하면 규칙 조건과 일치 하는 모든 메시지가 전송 될 때 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bdffa-p117">Mail flow rules determine under what conditions email messages should be encrypted, as well as conditions for removing that encryption. When you set an action for a rule, any messages that match the rule conditions are encrypted when they're sent.</span></span>
  
<span data-ttu-id="bdffa-177">메일 흐름 규칙에 대 한 자세한 내용은 [Office 365에서 전자 메일 메시지를 암호화 하는 메일 흐름 규칙 정의](define-mail-flow-rules-to-encrypt-email.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bdffa-177">For more information about mail flow rules, see [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="bdffa-178">관련 항목</span><span class="sxs-lookup"><span data-stu-id="bdffa-178">Related Topics</span></span>

[<span data-ttu-id="bdffa-179">Outlook에서 암호화 된 메시지 보내기, 확인 및 회신</span><span class="sxs-lookup"><span data-stu-id="bdffa-179">Send, view, and reply to encrypted messages in Outlook</span></span>](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)
  
[<span data-ttu-id="bdffa-180">Enable-enable-aadrm</span><span class="sxs-lookup"><span data-stu-id="bdffa-180">Enable-Aadrm</span></span>](https://docs.microsoft.com/powershell/module/aadrm/enable-aadrm?view=azureipps)
  
[<span data-ttu-id="bdffa-181">원격 PowerShell을 사용하여 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="bdffa-181">Connect to Exchange Online PowerShell</span></span>](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx)
  
[<span data-ttu-id="bdffa-182">Office 365에서 전자 메일 메시지를 암호화하기 위한 메일의 흐름 규정을 정의</span><span class="sxs-lookup"><span data-stu-id="bdffa-182">Define mail flow rules to encrypt email messages in Office 365</span></span>](define-mail-flow-rules-to-encrypt-email.md)
