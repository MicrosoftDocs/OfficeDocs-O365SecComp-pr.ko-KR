---
title: 새로운 Office 365 메시지 암호화 기능 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: 새로운 Office 365 메시지 암호화 Azure 정보 보호 조직의 위쪽에 구축 된 기능을 사용 하 여 수 내부 테두리와 조직 외부의 사용자와 전자 메일 통신을 보호 합니다. 다른 Office 365, Outlook.com, Gmail, 조직과 다른 전자 메일 서비스를 사용 하는 새 OME 기능입니다.
ms.openlocfilehash: a30054bf7b03a3e4fadf9a0e34537c682c10e217
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29696252"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a><span data-ttu-id="4b779-104">새로운 Office 365 메시지 암호화 기능 설정</span><span class="sxs-lookup"><span data-stu-id="4b779-104">Set up new Office 365 Message Encryption capabilities</span></span>

<span data-ttu-id="4b779-p102">Azure 정보 보호의 보호 기능을 활용 하는 새로운 Office 365 메시지 암호화 (OME) 기능을 사용 하면 조직 모든 장치에서 모든 사람과 보호 된 전자 메일을 쉽게 공유할 수 있습니다. 사용자가 보내고 Outlook.com, Gmail, 및 기타 전자 메일 서비스를 사용 하 여 Office 365가 아닌 고객은 물론 다른 Office 365 조직으로 보호 된 메시지를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-p102">With the new Office 365 Message Encryption (OME) capabilities, which leverage the protection features in Azure Information Protection, your organization can easily share protected email with anyone on any device. Users can send and receive protected messages with other Office 365 organizations as well as non-Office 365 customers using Outlook.com, Gmail, and other email services.</span></span>

||
|:-----|
|<span data-ttu-id="4b779-p103">이 문서는 Office 365 메시지 암호화에 대 한 문서를 더 큰 시리즈의 일부입니다. 이 문서는 관리자 및 ITPros 위한 것입니다. 방금 경우 보내거나 암호화 된 메시지를 받는 방법에 대 한 정보에 대 한 자세한 내용은 [Office 365 메시지 암호화 OME ()](ome.md) 의 문서 목록을 참조 하 고 요구 사항에 가장 적합 한 문서를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-p103">This article is part of a larger series of articles about Office 365 Message Encryption. This article is intended for administrators and ITPros. If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

## <a name="get-started-with-ome-by-activating-azure-rights-management-part-of-azure-information-protection"></a><span data-ttu-id="4b779-110">Azure 권한 관리, Azure 정보 보호의 일부를 활성화 하 여 OME 시작 하기</span><span class="sxs-lookup"><span data-stu-id="4b779-110">Get started with OME by activating Azure Rights Management, part of Azure Information Protection</span></span>

<span data-ttu-id="4b779-p104">이제 새 OME 기능을 사용 하는 것이 쉽습니다. 2 월 2018를 기준으로 자동으로 Office 365에는 데이터 센터 내에서 사용할 수 있는 조직에 대 한 새 OME 기능 수 있습니다. 새 Office 365 테 넌 트 이며 조직에 적합 한 구독 하는 경우 조직 대상이있지 않습니다. **하는 경우 Azure 권한 관리 (Azure RMS) 부분에서는 Azure 정보 보호를 사용 하도록 설정한 다음 Office 365 메시지 암호화 하면 자동으로 활성화 했습니다.** OME를 사용 하도록 설정 하려면 다른 작업을 수행할 필요가 없습니다. Azure 권한 관리를 활성화 하려면 [Azure 권한 관리 활성화](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service)를 참조 하십시오. 구독에 대 한 정보를 "어떤 구독 해야하는 새 OME capabilities?를 사용 하 여" [Office 365 메시지 암호화 FAQ](ome-faq.md)에서 참조 하십시오. Azure 정보 보호에 대 한 구독 구입 하는 방법에 대 한 정보를 [Azure 정보 보호](https://azure.microsoft.com/services/information-protection/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4b779-p104">It's now easy to get started with the new OME capabilities. As of February 2018, Office 365 automatically enables the new OME capabilities for eligible organizations within our datacenters. Your organization is eligible if it is a new Office 365 tenant and your organization has the appropriate subscriptions. **If you have enabled Azure Rights Management (Azure RMS), part of Azure Information Protection, then we automatically enable Office 365 Message Encryption for you.** You don't have to do anything else to enable OME. To activate Azure Rights Management, see [Activating Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). For information on subscriptions, see "What subscriptions do I need to use the new OME capabilities?" in the [Office 365 Message Encryption FAQ](ome-faq.md). For information about purchasing a subscription to Azure Information Protection, see [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>
  
<span data-ttu-id="4b779-p105">Exchange Online Active Directory Rights Management 서비스 (AD RMS)를 사용할 경우 즉시 이러한 새 기능을 활성화할 수 없습니다. 대신, 먼저 Azure 정보 보호 AD RMS에서 마이그레이션 해야 합니다. 마이그레이션 완료 했을 때, 다음이 단계를 성공적으로 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-p105">If you are using Exchange Online with Active Directory Rights Management service (AD RMS), you can't enable these new capabilities right away. Instead, you need to migrate from AD RMS to Azure Information Protection first. When you've finished the migration, you can successfully complete these steps.</span></span>
  
<span data-ttu-id="4b779-123">계속 사용 하려는 경우 온-프레미스 AD RMS Exchange Online과 Azure 정보 보호로 마이그레이션하는 대신, 됩니다 이러한 새 기능을 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-123">If you choose to continue to use on-premises AD RMS with Exchange Online instead of migrating to Azure Information Protection, you will not be able to use these new capabilities.</span></span>
  
## <a name="how-the-new-capabilities-for-ome-work"></a><span data-ttu-id="4b779-124">OME에 대 한 새로운 기능 작동 방식</span><span class="sxs-lookup"><span data-stu-id="4b779-124">How the new capabilities for OME work</span></span>

<span data-ttu-id="4b779-p106">새로운 Office 365 메시지 암호화 기능 Azure 정보 보호에서 Azure 권한 관리 (Azure RMS)이 라고도 하는 보호 기능을 사용 합니다. 이 전자 메일을 보호 하는 암호화, id 및 권한 부여 정책을 포함 됩니다. 권한 관리 템플릿, [전달 하지 않음 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)및 [암호화 전용 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 사용 하 여 메시지를 암호화할 수 있습니다. 사용자가 이러한 옵션을 사용 하 여 전자 메일 메시지와 다양 한 Office 365 첨부 파일에 암호화할 수 있습니다. 지원 되는 첨부 파일 형식 목록은 전체 [전자 메일 메시지에 대 한 IRM 사용 소개 "IRM 정책 메시지에 첨부 하는 경우에 파일 형식 포함"을](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM)참조 하십시오. 관리자로 서이 보호 기능을 적용 하는 메일 흐름 규칙을 정의할 수 있습니다. 예, 여기에서 특정 받는 사람에 게 해결 되는 또는 제목에 특정 단어가 포함 된 모든 보호 되지 않은 메시지 무단된 액세스 로부터 보호 되 고 받는 사람 복사 하거나 메시지의 내용을 인쇄할 수 없습니다는 규칙을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-p106">The new Office 365 Message Encryption capabilities use the protection capabilities, also called Azure Rights Management (Azure RMS), from Azure Information Protection. This includes encryption, identity, and authorization policies to help secure your email. You can encrypt messages by using rights management templates, the [Do Not Forward option](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails), and the [encrypt-only option](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails). Users can then encrypt email messages and a variety of Office 365 attachments by using these options. For a full list of supported attachment types, see ["File types covered by IRM policies when they are attached to messages" in Introduction to IRM for email messages](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM). As an administrator, you can also define mail flow rules to apply this protection. For example, you can define a rule where all unprotected messages that are addressed to a specific recipient or that contain specific words in the subject line are protected from unauthorized access, and the recipients can't copy or print the contents of the message.</span></span>
  
<span data-ttu-id="4b779-p107">OME은 이전 버전과 달리 이러한 새로운 기능은 조직 내부 또는 외부 Office 365의 받는 사람에 게 메일을 보낼 때 여부 통합된 발신자 경험을 제공 합니다. 또한 Outlook 2016 또는 웹에서 Outlook에서 Office 365 계정에 게 보낸 보호 된 전자 메일 메시지를 받을 사람의 메시지를 볼 수 있는 추가 조치를 취할 필요가 없습니다. 원활 하 게 작동합니다. 다른 전자 메일 클라이언트 및 전자 메일 서비스 공급자를도 사용 하 여 받는 사람에 게 향상된 된 환경을 포함 합니다. 내용은 [Office 365의 보호 된 메시지에 대 한 자세한 내용](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) 및 [보호 된 메시지를 열려면 어떻게](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4b779-p107">Unlike the previous version of OME, these new capabilities provide a unified sender experience whether you're sending mail inside your organization or to recipients outside of Office 365. In addition, recipients who receive a protected email message sent to an Office 365 account in Outlook 2016 or Outlook on the web, don't have to take any additional action to view the message. It works seamlessly. Recipients using other email clients and email service providers also have an improved experience. For information, see [Learn about protected messages in Office 365](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) and [How do I open a protected message](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098).</span></span>

<span data-ttu-id="4b779-137">OME의 이전 버전과 새 OME 기능 간의 차이점 목록이 자세한 [OME의 버전을 비교](ome-version-comparison.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4b779-137">For a detailed list of the differences between the previous version of OME and the new OME capabilities, see [Compare versions of OME](ome-version-comparison.md).</span></span>
  
## <a name="steps-to-manually-set-up-the-new-capabilities-for-ome"></a><span data-ttu-id="4b779-138">수동으로 OME에 대 한 새로운 기능을 설정 하는 단계</span><span class="sxs-lookup"><span data-stu-id="4b779-138">Steps to manually set up the new capabilities for OME</span></span>

<span data-ttu-id="4b779-p108">새 OME 기능 대부분의 Office 365 조직에 대해 자동으로 활성화 됩니다. 조직 자동으로 없는 OME이 옵션을 설정 또는 해제 새 OME 기능을 설정 하는 경우에 수동으로 OME에 대 한 새로운 기능을 설정 하려면 다음이 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-p108">The new OME capabilities are automatically enabled for most Office 365 organizations. If your organization does not automatically have OME enabled, or if you turned the new OME capabilities off, follow these steps to manually set up the new capabilities for OME.</span></span>
  
### <a name="to-manually-set-up-the-new-capabilities-for-ome"></a><span data-ttu-id="4b779-141">OME에 대 한 새로운 기능을 수동으로 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="4b779-141">To manually set up the new capabilities for OME</span></span>

1. <span data-ttu-id="4b779-p109">조직에 대 한 오른쪽 구독을 했는지 확인 합니다. 구독에 대 한 내용은 "어떤 구독 해야하는 새 OME capabilities?를 사용 하 여"에서 참조는 [Office 365 메시지 암호화 FAQ.](ome-faq.md)합니다. Azure 정보 보호에 대 한 구독 구입 하는 방법에 대 한 정보를 [Azure 정보 보호](https://azure.microsoft.com/services/information-protection/)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4b779-p109">Ensure you have the right subscription for your organization. For information on subscriptions, see "What subscriptions do I need to use the new OME capabilities?" in the [Office 365 Message Encryption FAQ.](ome-faq.md). For information about purchasing a subscription to Azure Information Protection, see [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

2. <span data-ttu-id="4b779-p110">Azure 정보 보호 (기본값)에 대 한 루트 키를 관리 하거나 생성 하 고 (직접 키로 이동한 다음 또는 BYOK 맨앞으로 알려진) 사용자가 직접이 키를 관리 하는 Microsoft 여부를 결정 합니다. 생성 하 고 사용자가 직접이 키를 관리 하려는 경우 OME에 대 한 새로운 기능을 설정 하기 전에 일부 단계를 완료 해야 합니다. 자세한 내용은 [계획 및 구현 하 여 Azure 정보 보호 테 넌 트 키를](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key)참조 하십시오. OME를 설정 하기 전에 다음이 단계를 완료 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-p110">Decide whether you want Microsoft to manage the root key for Azure Information Protection (the default), or generate and manage this key yourself (known as bring your own key, or BYOK). If you want to generate and manage this key yourself, you need to complete some steps before you set up the new capabilities for OME. For more information, see [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key). Microsoft recommends that you complete these steps before you set up OME.</span></span>

3. <span data-ttu-id="4b779-p111">Azure 권한 관리를 활성화 하 여 OME에 대 한 새로운 기능을 사용 합니다. 자세한 내용은 [Azure 권한 관리 활성화](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service)를 참조 하십시오. 자동이 위해 Office 365 하면 새 OME 기능을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-p111">Enable the new capabilities for OME by activating Azure Rights Management. For instructions, see [Activating Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). When you do this, Office 365 automatically enables the new OME capabilities for you.</span></span>

    > [!TIP]
    > <span data-ttu-id="4b779-p112">웹에 있는 outlook 하루에이 클라이언트를 사용 하 여 전자 메일 메시지에 OME에 대 한 새로운 기능을 적용 하기 전에 대기 하는 것이 좋습니다 하므로 해당 UI을 캐시 합니다. UI 새 구성을 반영 하도록 업데이트를 하기 전에는 OME에 대 한 새로운 기능을 사용할 수 없습니다. UI 업데이트 하 고 나면 사용자가 OME에 대 한 새로운 기능을 사용 하 여 전자 메일 메시지를 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-p112">Outlook on the Web caches its UI, so it's a good idea to wait a day before you try applying the new capabilities for OME to email messages using this client. Before the UI updates to reflect the new configuration, the new capabilities for OME won't be available. After the UI updates, users can protect email messages by using the new capabilities for OME.</span></span>
  
4. <span data-ttu-id="4b779-156">(선택 사항) 새 메일 흐름 규칙을 설정 하거나 조직에서 보낸 메시지를 암호화 하는 Office 365 시기와 방법을 정의 하는 기존 메일 흐름 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-156">(Optional) Set up new mail flow rules or update existing mail flow rules that define how and when you want Office 365 to encrypt messages sent from your organization.</span></span>

## <a name="verify-that-the-new-capabilities-for-ome-are-configured-properly-by-using-windows-powershell"></a><span data-ttu-id="4b779-157">Windows PowerShell을 사용 하 여 OME에 대 한 새 기능이 제대로 구성 되었는지 확인</span><span class="sxs-lookup"><span data-stu-id="4b779-157">Verify that the new capabilities for OME are configured properly by using Windows PowerShell</span></span>

<span data-ttu-id="4b779-158">Exchange Online PowerShell을 통해 OME에 대 한 새로운 기능을 사용 하 여 테 넌 트 제대로 구성 되었는지 확인 하려면 다음이 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-158">Follow these steps to verify that your tenant is properly configured to use the new capabilities for OME through Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="4b779-p113">Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 하는 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4b779-p113">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="4b779-161">다음 구문을 사용 하 여 Test-irmconfiguration cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-161">Run the Test-IRMConfiguration cmdlet using the following syntax:</span></span>

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   <span data-ttu-id="4b779-162">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-162">For example:</span></span>

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

    <span data-ttu-id="4b779-p114">여기서 전자 메일 주소는 Office 365 조직에 있는 사용자의 전자 메일 주소입니다. 옵션, 제공 하는 동안 보낸 전자 메일 주소를 추가 검사를 수행 하려면 시스템을 강제 합니다. 결과 다음과 같은 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-p114">Where email address is the email address of a user in your Office 365 organization. While optional, providing a sender email address forces the system to perform additional checks. Your results should look like these:</span></span>

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

    <span data-ttu-id="4b779-166">여기서 *Contoso* 는 Office 365 조직 이름으로 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-166">Where *Contoso* is replaced with the name of your Office 365 organization.</span></span>

    <span data-ttu-id="4b779-167">결과에 반환 하는 기본 서식 파일의 이름은 위의 결과에 표시 된 것과 다른 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-167">The names of the default templates returned in the results may be different from those displayed in the results above.</span></span>

    <span data-ttu-id="4b779-p115">서식 파일 및 기본 서식 파일에 대 한 정보에 대 한 소개를 [구성 하 고 Azure 정보 보호에 대 한 서식 파일 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오. 착신 전환 안함에 대 한 정보에 대 한 옵션을 암호화 전용 옵션을 및 방법을 만들려면 추가 서식 파일 또는 어떤 권한에 대해 알아봅니다 기존 서식 파일에 포함 된, 참조 [Azure 권한 관리에 대 한 사용 권한을 구성](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights)합니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-p115">For an introduction to templates and information about the default templates, see [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). For information about the Do Not Forward option, encrypt-only option, and how to create additional templates, or find out what rights are included in an existing template, see [Configuring usage rights for Azure Rights Management](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights).</span></span>

3. <span data-ttu-id="4b779-170">권한 관리 서비스에서 연결을 끊으려면 Remove-pssession cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-170">Run the Remove-PSSession cmdlet to disconnect from the Rights Management service.</span></span>
    
     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-new-mail-flow-rules-that-use-the-new-ome-capabilities"></a><span data-ttu-id="4b779-171">다음 단계: 새 OME 기능을 사용 하는 새 메일 흐름 규칙 정의</span><span class="sxs-lookup"><span data-stu-id="4b779-171">Next steps: Define new mail flow rules that use the new OME capabilities</span></span>

<span data-ttu-id="4b779-p116">그러나이 단계는 새 OME 배포에 대 한 선택적,이 단계는 메일 흐름 설정 된 규칙 최대 보내는 메일 암호화에 이미 있는 기존 OME 배포에 필요 합니다. 새 OME 기능을 활용 하려는 경우 기존 메일 흐름 규칙을 업데이트 해야 합니다. 그렇지 않은 경우 사용자에 게 새, 원활 하 게 OME 경험 하는 대신 이전 HTML 첨부 파일 형식을 사용 하는 암호화 된 메일을 받도록 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-p116">This step is optional for new OME deployments, however, this step is required for existing OME deployments that already have mail flow rules set up to encrypt outgoing mail. If you want to take advantage of the new OME capabilities, you must update your existing mail flow rules. Otherwise, your users will continue to receive encrypted mail that uses the previous HTML attachment format instead of the new, seamless OME experience.</span></span>
  
<span data-ttu-id="4b779-p117">메일 흐름 규칙에서 어떤 조건 전자 메일 메시지를 암호화 해야, 해당 암호화를 제거 하기 위한 조건, 결정 합니다. 규칙에 대 한 동작을 설정 하면는 보내면 규칙 조건에 맞는 모든 메시지는 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b779-p117">Mail flow rules determine under what conditions email messages should be encrypted, as well as conditions for removing that encryption. When you set an action for a rule, any messages that match the rule conditions are encrypted when they're sent.</span></span>
  
<span data-ttu-id="4b779-177">메일 흐름 규칙에 대 한 자세한 내용은 [Office 365에서 전자 메일 메시지를 암호화 메일 흐름 규칙 정의](define-mail-flow-rules-to-encrypt-email.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4b779-177">For more information about mail flow rules, see [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="4b779-178">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4b779-178">Related Topics</span></span>

[<span data-ttu-id="4b779-179">보내기, 보기 및 Outlook에서 암호화 된 메시지에 회신</span><span class="sxs-lookup"><span data-stu-id="4b779-179">Send, view, and reply to encrypted messages in Outlook</span></span>](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)
  
[<span data-ttu-id="4b779-180">Aadrm 사용</span><span class="sxs-lookup"><span data-stu-id="4b779-180">Enable-Aadrm</span></span>](https://docs.microsoft.com/powershell/module/aadrm/enable-aadrm?view=azureipps)
  
[<span data-ttu-id="4b779-181">원격 PowerShell을 사용하여 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="4b779-181">Connect to Exchange Online PowerShell</span></span>](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx)
  
[<span data-ttu-id="4b779-182">Office 365에서 전자 메일 메시지를 암호화하기 위한 메일의 흐름 규정을 정의</span><span class="sxs-lookup"><span data-stu-id="4b779-182">Define mail flow rules to encrypt email messages in Office 365</span></span>](define-mail-flow-rules-to-encrypt-email.md)
