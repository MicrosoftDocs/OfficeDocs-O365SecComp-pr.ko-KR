---
title: Office 365에서 전자 메일 메시지를 암호화하기 위한 메일의 흐름 규정을 정의
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 9b7daf19-d5f2-415b-bc43-a0f5f4a585e8
description: 관리자가 수를 메일 흐름 규칙 만들기 (전송 규칙이 라고도 함)를 암호화 하 여 Office 365 메시지 암호화 OME ()를 사용 하 여 메시지의 암호를 해독 하는 방법을 알아봅니다.
ms.openlocfilehash: ce6b1ce60abb58c5f4e217c66bca013101af5f91
ms.sourcegitcommit: 30faa3ba91cab4c36e3d8d8ed5858d5269ea8a56
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27749362"
---
# <a name="define-mail-flow-rules-to-encrypt-email-messages-in-office-365"></a><span data-ttu-id="8c086-103">Office 365에서 전자 메일 메시지를 암호화하기 위한 메일의 흐름 규정을 정의</span><span class="sxs-lookup"><span data-stu-id="8c086-103">Define mail flow rules to encrypt email messages in Office 365</span></span>

<span data-ttu-id="8c086-p101">Office 365 전역 관리자 권한으로 전자 메일 메시지 보내기 및 받기 보호를 메일에 흐름 규칙 (전송 규칙이 라고도 함) 만들 수 있습니다. 모든 보내는 전자 메일 메시지를 암호화 하 고 조직 내부에서 연결 되는 암호화 된 메시지 또는 조직에서 보낸 암호화 된 메시지에 대 한 회신에서 암호화를 제거 하는 규칙을 설정할 수 있습니다. 이러한 규칙을 만들 수는 Exchange 관리 센터 (EAC) 또는 Exchange Online PowerShell를 사용할 수 있습니다. 전체 암호화 규칙 외에도 최종 사용자를 위한 개별 메시지 암호화 옵션을 사용할지 여부를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-p101">As an Office 365 global administrator, you can create mail flow rules (also known as transport rules) to help protect email messages you send and receive. You can set up rules to encrypt any outgoing email messages and remove encryption from encrypted messages coming from inside your organization or from replies to encrypted messages sent from your organization. You can use the Exchange admin center (EAC) or Exchange Online PowerShell to create these rules. In addition to overall encryption rules, you can also choose to enable or disable individual message encryption options for end-users.</span></span>

<span data-ttu-id="8c086-p102">최근에 AD RMS에서 Azure 정보 보호를 마이그레이션한 경우 새 환경에서 작업을 계속 하 여 기존 메일 흐름 규칙을 검토 하려면 필요 합니다. 또한 활용 하기 위해 사용할 수 있는 새로운 Office 365 메시지 암호화 (OME) 기능을 Azure 정보 보호 기능을 통해 하려는 경우 기존 메일 흐름 규칙을 업데이트 해야 합니다. 그렇지 않은 경우 사용자에 게 새, 원활 하 게 OME 경험 하는 대신 이전 HTML 첨부 파일 형식을 사용 하는 암호화 된 메일을 받도록 계속 됩니다. 아직 OME를 설정 하지 않은 경우, 정보에 대 한 [Azure 정보 보호 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md) 을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-p102">If you recently migrated from AD RMS to Azure Information Protection, you'll need to review your existing mail flow rules to ensure that they continue to work in your new environment. Additionally, if you want to take advantage of the new Office 365 Message Encryption (OME) capabilities available to you through Azure Information Protection, you need to update your existing mail flow rules. Otherwise, your users will continue to receive encrypted mail that uses the previous HTML attachment format instead of the new, seamless OME experience. If you haven't set up OME yet, see [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection](set-up-new-message-encryption-capabilities.md) for information.</span></span>

<span data-ttu-id="8c086-p103">메일 흐름 규칙 및 메일 흐름 규칙 작업은 어떻게 구성 하는 구성 요소에 대 한 정보를 [Exchange Online에서 흐름 규칙 (전송 규칙) 메일](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)을 참조 하십시오. 메일 흐름 규칙 Azure 정보 보호와 함께 작동 하는 방법에 대 한 자세한 내용은 [Azure 정보 보호 레이블에 대 한 Exchange Online 구성 메일 흐름 규칙](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-exo-rules)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8c086-p103">For information about the components that make up mail flow rules and how mail flow rules work, see [Mail flow rules (transport rules) in Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules). For additional information about how mail flow rules work with Azure Information Protection, see [Configuring Exchange Online mail flow rules for Azure Information Protection labels](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-exo-rules).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c086-p104">하이브리드 Exchange 환경에 대 한 온-프레미스 사용자 전자 메일을 Exchange Online을 통해 라우팅되는 경우에 OME를 사용 하 여 암호화 된 메일을 보낼 수 있습니다. 하이브리드 Exchange 환경에서 OME를 구성 하려면 첫번째 [하이브리드 구성 마법사를 사용 하 여 하이브리드 구성](https://docs.microsoft.com/Exchange/exchange-hybrid) 및 [메일 Office 365로 전자 메일 서버에서 흐름을 구성](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365)해야 합니다. 한번 구성한 메일이 Office 365를 통해 전달이 지침을 사용 하 여 OME에 대 한 메일 흐름 규칙을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-p104">For hybrid Exchange environments, on-premises users can send encrypted mail using OME only if email is routed through Exchange Online. To configure OME in a hybrid Exchange environment, you need to first [configure hybrid using the Hybrid Configuration wizard](https://docs.microsoft.com/Exchange/exchange-hybrid) and then [configure mail to flow from your email server to Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365). Once you've configured mail to flow through Office 365, then you can configure mail flow rules for OME by using this guidance.</span></span>

## <a name="create-mail-flow-rules-to-encrypt-email-messages-with-the-new-ome-capabilities"></a><span data-ttu-id="8c086-117">메일 흐름 새 OME 기능으로 전자 메일 메시지를 암호화 하는 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="8c086-117">Create mail flow rules to encrypt email messages with the new OME capabilities</span></span>

<span data-ttu-id="8c086-118">EAC를 사용 하 여 새 OME 기능을 사용 하 여 메시지 암호화를 트리거하는 것에 대 한 메일 흐름 규칙을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-118">You can define mail flow rules for triggering message encryption with the new OME capabilities by using the EAC.</span></span>

### <a name="use-the-eac-to-create-a-rule-for-encrypting-email-messages-with-the-new-ome-capabilities"></a><span data-ttu-id="8c086-119">EAC를 사용 하 여 새 OME 기능으로 전자 메일 메시지를 암호화 하는 것에 대 한 규칙을 만들려면</span><span class="sxs-lookup"><span data-stu-id="8c086-119">Use the EAC to create a rule for encrypting email messages with the new OME capabilities</span></span>

1. <span data-ttu-id="8c086-120">웹 브라우저에서 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)전역 관리자 권한을 부여 하는 작업이 나 교육용 계정을 사용 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-120">In a web browser, using a work or school account that has been granted global administrator permissions, [sign in to Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).</span></span>

2. <span data-ttu-id="8c086-121">**Admin** 타일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-121">Choose the **Admin** tile.</span></span>

3. <span data-ttu-id="8c086-122">Office 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-122">In the Office 365 admin center, choose **Admin centers** \> **Exchange**.</span></span>

4. <span data-ttu-id="8c086-p105">EAC에서 **메일 흐름** 으로 이동 \> **규칙** 및 선택 **새로** ![새 아이콘](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **새 규칙 만들기**. EAC를 사용 하는 방법에 대 한 자세한 내용은 [Exchange Online의 Exchange 관리 센터](https://docs.microsoft.com/exchange/exchange-admin-center)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8c086-p105">In the EAC, go to **Mail flow** \> **Rules** and select **New** ![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **Create a new rule**. For more information about using the EAC, see [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span></span>

5. <span data-ttu-id="8c086-125">**이름**Encrypt mail for DrToniRamos@hotmail.com와 같은 규칙에 대 한 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-125">In **Name**, type a name for the rule, such as Encrypt mail for DrToniRamos@hotmail.com.</span></span>

6. <span data-ttu-id="8c086-p106">**다음의 경우 이 규칙 적용**에서 조건을 선택하고 필요한 경우 값을 입력합니다. 예를 들어 DrToniRamos@hotmail.com에 보내는 메시지를 암호화하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-p106">In **Apply this rule if** select a condition, and enter a value if necessary. For example, to encrypt messages going to DrToniRamos@hotmail.com:</span></span>

   1. <span data-ttu-id="8c086-128">**다음의 경우 이 규칙 적용**에서 **받는 사람이 다음과 같음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-128">In **Apply this rule if**, select **the recipient is**.</span></span>

   2. <span data-ttu-id="8c086-129">연락처 목록에서 기존 이름을 선택하거나 **이름 확인** 상자에 새 전자 메일 주소를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-129">Select an existing name from the contact list or type a new email address in the **check names** box.</span></span>
    
      - <span data-ttu-id="8c086-130">기존 이름을 선택하려면 목록에서 이름을 선택한 다음 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-130">To select an existing name, select it from the list and then click **OK**.</span></span>

      - <span data-ttu-id="8c086-131">새 이름을 입력 하 고 **이름 확인** 상자에 전자 메일 주소를 입력 한 다음 **이름 확인** 을 선택 하려면 \> **확인**합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-131">To enter a new name, type an email address in the **check names** box and then select **check names** \> **OK**.</span></span>

7. <span data-ttu-id="8c086-132">조건을 더 추가할 **기타 옵션** 을 선택 하 고 **조건 추가** 선택 하 고 목록에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-132">To add more conditions, choose **More options** and then choose **add condition** and select from the list.</span></span>

   <span data-ttu-id="8c086-133">예, 받는 사람이 조직 외부에 있을 경우에이 규칙을 적용 하려면 **조건 추가** 선택한 다음 선택 **받는 사람이 외부/내부** \> **조직 외부의** \> **확인**합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-133">For example, to apply the rule only if the recipient is outside your organization, select **add condition** and then select **The recipient is external/internal** \> **Outside the organization** \> **OK**.</span></span>

8. <span data-ttu-id="8c086-p107">**다음을 수행**하십시오에서 새 OME 기능을 사용 하 여 암호화를 사용 하도록 설정 하려면 **메시지 보안 수정** 을 선택 하 고 **Office 365 메시지 암호화 적용 및 권한 보호를**선택 합니다. 목록에서 RMS 템플릿을 선택, **저장**을 선택 하 고 **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-p107">To enable encryption using the new OME capabilities, from **Do the following**, select **Modify the message security** and then choose **Apply Office 365 Message Encryption and rights protection**. Select an RMS template from the list, choose **Save**, and then choose **OK**.</span></span>
  
  <span data-ttu-id="8c086-p108">모든 기본 서식 파일을 포함 하는 서식 파일 목록이 및 Office 365에서으로 옵션에 대해 만든 모든 사용자 지정 서식 파일을 사용 합니다. 목록이 비어 있으면 설정 되었는지 확인 하면가 Office 365 메시지 암호화 새 기능을 함께 [Azure 정보 보호의 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md)의 설명에 따라 합니다. 기본 서식 파일에 대 한 정보를 [구성 하 고 Azure 정보 보호에 대 한 서식 파일 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오. **전달 하지 않음** 옵션에 대 한 정보를 [전자 메일 전달 하지 않음 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)을 참조 하십시오. **만 암호화** 옵션에 대 한 정보를 [전자 메일만 암호화 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8c086-p108">The list of templates includes all default templates and options as well as any custom templates you've created for use by Office 365. If the list is empty, ensure that you have set up Office 365 Message Encryption with the new capabilities as described in [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection](set-up-new-message-encryption-capabilities.md). For information about the default templates, see [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). For information about the **Do Not Forward** option, see [Do Not Forward option for emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). For information about the **encrypt only** option, see [Encrypt Only option for emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).</span></span>

  <span data-ttu-id="8c086-141">다른 작업을 지정 하려면 **작업 추가** 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-141">You can choose **add action** if you want to specify another action.</span></span>

### <a name="use-the-eac-to-update-an-existing-mail-flow-rule-to-use-the-new-ome-capabilities"></a><span data-ttu-id="8c086-142">EAC를 사용 하 여 새 OME 기능을 사용 하 여 기존 메일 흐름 규칙을 업데이트 하려면</span><span class="sxs-lookup"><span data-stu-id="8c086-142">Use the EAC to update an existing mail flow rule to use the new OME capabilities</span></span>

1. <span data-ttu-id="8c086-143">웹 브라우저에서 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)전역 관리자 권한을 부여 하는 작업이 나 교육용 계정을 사용 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-143">In a web browser, using a work or school account that has been granted global administrator permissions, [sign in to Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).</span></span>

2. <span data-ttu-id="8c086-144">**Admin** 타일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-144">Choose the **Admin** tile.</span></span>

3. <span data-ttu-id="8c086-145">Office 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-145">In the Office 365 admin center, choose **Admin centers** \> **Exchange**.</span></span>

4. <span data-ttu-id="8c086-146">EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-146">In the EAC, go to **Mail flow** \> **Rules**.</span></span>

5. <span data-ttu-id="8c086-147">메일 흐름 규칙 목록에서 새 OME 기능을 사용 하 고 **편집** 을 선택 합니다를 수정 하려는 규칙을 선택 ![편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-147">In the list of mail flow rules, select the rule you want to modify to use the new OME capabilities and then choose **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>

6. <span data-ttu-id="8c086-p109">**다음을 수행**하십시오에서 새 OME 기능을 사용 하 여 암호화를 사용 하도록 설정 하려면 **메시지 보안 수정** 을 선택 하 고 **Office 365 메시지 암호화 적용 및 권한 보호를**선택 합니다. 목록에서 RMS 템플릿을 선택 하 고 **저장** 을 선택 하 고 **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-p109">To enable encryption using the new OME capabilities, from **Do the following**, choose **Modify the message security** and then choose **Apply Office 365 Message Encryption and rights protection**. Select an RMS template from the list, choose **Save** and then choose **OK**.</span></span>

   <span data-ttu-id="8c086-p110">모든 기본 서식 파일을 포함 하는 서식 파일 목록이 및 Office 365에서으로 옵션에 대해 만든 모든 사용자 지정 서식 파일을 사용 합니다. 목록이 비어 있으면 설정 되었는지 확인 하면가 Office 365 메시지 암호화 새 기능을 함께 [Azure 정보 보호의 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md)의 설명에 따라 합니다. 기본 서식 파일에 대 한 정보를 [구성 하 고 Azure 정보 보호에 대 한 서식 파일 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오. **전달 하지 않음** 옵션에 대 한 정보를 [전자 메일 전달 하지 않음 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)을 참조 하십시오. **만 암호화** 옵션에 대 한 정보를 [전자 메일만 암호화 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8c086-p110">The list of templates includes all default templates and options as well as any custom templates you've created for use by Office 365. If the list is empty, ensure that you have set up Office 365 Message Encryption with the new capabilities as described in [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection](set-up-new-message-encryption-capabilities.md). For information about the default templates, see [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). For information about the **Do Not Forward** option, see [Do Not Forward option for emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). For information about the **encrypt only** option, see [Encrypt Only option for emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).</span></span>

   <span data-ttu-id="8c086-155">다른 작업을 지정 하려면 **작업 추가** 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-155">You can choose **add action** if you want to specify another action.</span></span>

7. <span data-ttu-id="8c086-156">**다음을 수행** 목록에서 **메시지 보안 수정** 에 할당 된 모든 작업을 제거 \> **OME의 이전 버전을 적용**합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-156">From the **Do the following** list, remove any actions that are assigned to **Modify the message security** \> **Apply the previous version of OME**.</span></span>

8. <span data-ttu-id="8c086-157">**Save(저장)** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-157">Choose **Save**.</span></span>

## <a name="create-mail-flow-rules-for-office-365-message-encryption-without-the-new-capabilities"></a><span data-ttu-id="8c086-158">메일 흐름 규칙 만들기 Office 365 메시지 암호화에 대 한 새로운 기능 없이</span><span class="sxs-lookup"><span data-stu-id="8c086-158">Create mail flow rules for Office 365 Message Encryption without the new capabilities</span></span>

<span data-ttu-id="8c086-p111">Office 365 조직 새 OME 기능을 이동한 아직 하지 않은 경우 이러한 작업을 사용 하 여 조직에 대 한 메시지를 암호화 하는 메일 흐름 규칙을 정의할 수 있습니다. 것이 조직에 대 한 적당 하 게 하는 즉시 새 OME 기능으로 이동 하는 계획을 확인 하는 것이 좋습니다. 자세한 내용은 [Azure 정보 보호 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-p111">If you haven't yet moved your Office 365 organization to the new OME capabilities, use these tasks to define mail flow rules to encrypt messages for your organization. Microsoft recommends that you make a plan to move to the new OME capabilities as soon as it is reasonable for your organization. For instructions, see [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection](set-up-new-message-encryption-capabilities.md).</span></span>

### <a name="use-the-eac-to-create-a-mail-flow-rule-for-encrypting-email-messages-without-the-new-ome-capabilities"></a><span data-ttu-id="8c086-162">EAC를 사용 하 여 새 OME 기능 없이 전자 메일 메시지를 암호화 하는 것에 대 한 메일 흐름 규칙을 만들려면</span><span class="sxs-lookup"><span data-stu-id="8c086-162">Use the EAC to create a mail flow rule for encrypting email messages without the new OME capabilities</span></span>

1. <span data-ttu-id="8c086-163">웹 브라우저에서 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)전역 관리자 권한을 부여 하는 작업이 나 교육용 계정을 사용 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-163">In a web browser, using a work or school account that has been granted global administrator permissions, [sign in to Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).</span></span>

2. <span data-ttu-id="8c086-164">**Admin** 타일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-164">Choose the **Admin** tile.</span></span>

3. <span data-ttu-id="8c086-165">Office 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-165">In the Office 365 admin center, choose **Admin centers** \> **Exchange**.</span></span>

4. <span data-ttu-id="8c086-p112">EAC에서 **메일 흐름** 으로 이동 \> **규칙** 및 선택 **새로** ![새 아이콘](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **새 규칙 만들기**. EAC를 사용 하는 방법에 대 한 자세한 내용은 [Exchange 관리 센터의 Exchange Online을](https://docs.microsoft.com/exchange/exchange-admin-center)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8c086-p112">In the EAC, go to **Mail flow** \> **Rules** and select **New** ![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **Create a new rule**. For more information about using the EAC, see [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span></span>

5. <span data-ttu-id="8c086-168">**이름**Encrypt mail for DrToniRamos@hotmail.com와 같은 규칙에 대 한 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-168">In **Name**, type a name for the rule, such as Encrypt mail for DrToniRamos@hotmail.com.</span></span>

6. <span data-ttu-id="8c086-p113">**다음의 경우 이 규칙 적용**에서 조건을 선택하고 필요한 경우 값을 입력합니다. 예를 들어 DrToniRamos@hotmail.com에 보내는 메시지를 암호화하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-p113">In **Apply this rule if** select a condition, and enter a value if necessary. For example, to encrypt messages going to DrToniRamos@hotmail.com:</span></span> 

   1. <span data-ttu-id="8c086-171">**다음의 경우 이 규칙 적용**에서 **받는 사람이 다음과 같음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-171">In **Apply this rule if**, select **the recipient is**.</span></span>

   2. <span data-ttu-id="8c086-172">연락처 목록에서 기존 이름을 선택하거나 **이름 확인** 상자에 새 전자 메일 주소를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-172">Select an existing name from the contact list or type a new email address in the **check names** box.</span></span>

      - <span data-ttu-id="8c086-173">기존 이름을 선택하려면 목록에서 이름을 선택한 다음 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-173">To select an existing name, select it from the list and then click **OK**.</span></span>

      - <span data-ttu-id="8c086-174">새 이름을 입력 하 고 **이름 확인** 상자에 전자 메일 주소를 입력 한 다음 **이름 확인** 을 선택 하려면 \> **확인**합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-174">To enter a new name, type an email address in the **check names** box and then select **check names** \> **OK**.</span></span>

7. <span data-ttu-id="8c086-175">조건을 더 추가, **기타 옵션** 을 선택 하 고 **조건 추가** 선택 하 고 목록에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-175">To add more conditions, choose **More options** and then select **add condition** and select from the list.</span></span>

   <span data-ttu-id="8c086-176">예, 받는 사람이 조직 외부에 있을 경우에이 규칙을 적용 하려면 **조건 추가** 선택한 다음 선택 **받는 사람이 외부/내부** \> **조직 외부의** \> **확인**합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-176">For example, to apply the rule only if the recipient is outside your organization, select **add condition** and then select **The recipient is external/internal** \> **Outside the organization** \> **OK**.</span></span>

8. <span data-ttu-id="8c086-177">암호화를 사용 하려면 **다음을 수행**하는에서 새 OME 기능을 사용 하지 않고, **메시지 보안 수정** \> **OME의 이전 버전을 적용**하 고 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-177">To enable encryption without using the new OME capabilities, in **Do the following**, select **Modify the message security** \> **Apply the previous version of OME**, and then choose **Save**.</span></span>

  <span data-ttu-id="8c086-p114">오류가 발생 하는 경우 해당 IRM 라이선스를 사용할 수 없는, 다음 아직 조직에 대 한 OME을 설정 하지 않은 합니다. 지금 OME를 설정 하려는 경우 새 OME 기능을 사용 하 여를 설정 해야 있습니다. 내용은 [Azure 정보 보호 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md)을 참조 하십시오. Microsoft는 더이상 설정의 새 기능 없이 OME의 새 배포를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-p114">If you receive an error that IRM licensing isn't enabled, then you haven't set up OME for your organization yet. If you'd like to set up OME now, you must set it up to use the new OME capabilities. For information, see [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection](set-up-new-message-encryption-capabilities.md). Microsoft no longer supports setting up new deployments of OME without the new capabilities.</span></span>

  <span data-ttu-id="8c086-182">다른 작업을 지정 하려면 **작업 추가** 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-182">You can choose **add action** if you want to specify another action.</span></span>

### <a name="use-exchange-online-powershell-to-create-a-mail-flow-rule-for-encrypting-email-messages-without-the-new-ome-capabilities"></a><span data-ttu-id="8c086-183">Exchange Online PowerShell을 사용 하 여 새 OME 기능 없이 전자 메일 메시지를 암호화 하는 것에 대 한 메일 흐름 규칙을 만들려면</span><span class="sxs-lookup"><span data-stu-id="8c086-183">Use Exchange Online PowerShell to create a mail flow rule for encrypting email messages without the new OME capabilities</span></span>

1. <span data-ttu-id="8c086-p115">Exchange Online PowerShell에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8c086-p115">Connect to Exchange Online PowerShell. For more information, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="8c086-186">**New-transportrule** cmdlet을 사용 하 여 규칙을 만들고 _ApplyOME_ 매개 변수를 설정 `$true`합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-186">Create a rule by using the **New-TransportRule** cmdlet and set the _ApplyOME_ parameter to `$true`.</span></span>

   <span data-ttu-id="8c086-187">이 예제를 실행 하려면 DrToniRamos@hotmail.com에 보내는 모든 전자 메일 메시지를 암호화할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-187">This example requires that all email messages sent to DrToniRamos@hotmail.com must be encrypted.</span></span>

   ```
   New-TransportRule -Name "Encrypt rule for Dr Toni Ramos" -SentTo "DrToniRamos@hotmail.com" -SentToScope "NotinOrganization" -ApplyOME $true
   ```

   <span data-ttu-id="8c086-188">**참고:**</span><span class="sxs-lookup"><span data-stu-id="8c086-188">**Notes**:</span></span>

   - <span data-ttu-id="8c086-189">새 규칙의 고유 이름은 "Dr 박찬식을 Ramos에 대 한 암호화 규칙"입니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-189">The unique name of the new rule is "Encrypt rule for Dr Toni Ramos".</span></span>

   - <span data-ttu-id="8c086-p116">_SentTo_ 매개 변수는 메시지를 받는 사람 (이름, 전자 메일 주소, 고유 이름으로 식별 합니다.)를 지정 합니다. 이 예제에서는 받는 전자 메일 주소 "DrToniRamos@hotmail.com" 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-p116">The _SentTo_ parameter specifies the message recipients (identified by name, email address, distinguished name, etc.). In this example, the recipient is identified by the email address "DrToniRamos@hotmail.com".</span></span>

   - <span data-ttu-id="8c086-p117">_SentToScope_ 매개 변수는 메시지 받는 사람의 위치를 지정 합니다. 이 예제에서는 받는 사람의 사서함 hotmail에 및 Office 365 조직에 속해 있으므로 없는 값 `NotInOrganization` 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-p117">The _SentToScope_ parameter specifies the location of the message recipients. In this example, the recipient's mailbox is in hotmail and is not part of the Office 365 organization, so the value `NotInOrganization` is used.</span></span>

   <span data-ttu-id="8c086-194">자세한 구문 및 매개변수 정보 [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8c086-194">For detailed syntax and parameter information, see [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule).</span></span>

### <a name="remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a><span data-ttu-id="8c086-195">새 OME 기능 없이 암호화 된 전자 메일 회신에서 암호화를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-195">Remove encryption from email replies encrypted without the new OME capabilities</span></span>

<span data-ttu-id="8c086-p118">전자 메일 사용자에 게 암호화 된 메시지를 보낼 때 해당 메시지의 받는 사람에 게 암호화 된 회신으로 응답할 수 있습니다. 메일 흐름 규칙 하므로 조직에서 전자 메일 사용자를 로그 항목을 볼 암호화 포털에 로그인 필요가 없습니다 회신에서 암호화를 자동으로 제거을 만들 수 있습니다. 이러한 규칙을 정의 하려면 EAC 또는 Windows PowerShell cmdlet을 사용할 수 있습니다. 아직 새 OME 기능을 사용 하지 않는 경우에 하나 조직 또는 조직 내에서 보낸 메시지에 대 한 회신 메시지 내에서 전송 된 메시지를 해독할만. 조직 외부에서 발생 하는 암호화 된 메시지의 암호를 해독할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-p118">When your email users send encrypted messages, recipients of those messages can respond with encrypted replies. You can create mail flow rules to automatically remove encryption from replies so email users in your organization don't have to sign in to the encryption portal to view them. You can use the EAC or Windows PowerShell cmdlets to define these rules. If you are not yet using the new OME capabilities, you can only decrypt messages that are either sent from within your organization or messages that are replies to messages sent from within your organization. You cannot decrypt encrypted messages originating from outside of your organization.</span></span>

#### <a name="use-the-eac-to-create-a-rule-for-removing-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a><span data-ttu-id="8c086-201">EAC를 사용 하 여 새 OME 기능 없이 암호화 된 전자 메일 회신에서 암호화를 제거 하기 위한 규칙을 만들려면</span><span class="sxs-lookup"><span data-stu-id="8c086-201">Use the EAC to create a rule for removing encryption from email replies encrypted without the new OME capabilities</span></span>

1. <span data-ttu-id="8c086-202">웹 브라우저에서 관리자 권한, [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)부여 된 작업이 나 교육용 계정을 사용 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-202">In a web browser, using a work or school account that has been granted admin permissions, [sign in to Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).</span></span>

2. <span data-ttu-id="8c086-203">**Admin** 타일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-203">Choose the **Admin** tile.</span></span>

3. <span data-ttu-id="8c086-204">Office 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-204">In the Office 365 admin center, choose **Admin centers** \> **Exchange**.</span></span>

4. <span data-ttu-id="8c086-p119">EAC에서 **메일 흐름** 으로 이동 \> **규칙** 및 선택 **새로** ![새 아이콘](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **새 규칙 만들기**. EAC를 사용 하는 방법에 대 한 자세한 내용은 [Exchange 관리 센터의 Exchange Online을](https://docs.microsoft.com/exchange/exchange-admin-center)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8c086-p119">In the EAC, go to **Mail flow** \> **Rules** and select **New** ![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **Create a new rule**. For more information about using the EAC, see [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span></span>

5. <span data-ttu-id="8c086-207">**이름**받는 메일에서 제거 암호화와 같은 규칙에 대 한 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-207">In **Name**, type a name for the rule, such as Remove encryption from incoming mail.</span></span>

6. <span data-ttu-id="8c086-208">**하는 경우이 규칙 적용** 에서 등 **의 받는 사람이 있는** 메시지에서 암호화를 제거할 조건을 선택 \> **조직 내부**합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-208">In **Apply this rule if** select the conditions where encryption should be removed from messages, such as **The recipient is located** \> **Inside the organization**.</span></span>

7. <span data-ttu-id="8c086-209">**다음을 수행**을 선택 **메시지 보안 수정** \> **OME의 이전 버전을 제거**합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-209">In **Do the following**, select **Modify the message security** \> **Remove the previous version of OME**.</span></span>

8. <span data-ttu-id="8c086-210">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-210">Select **Save**.</span></span>

#### <a name="use-exchange-online-powershell-to-create-a-rule-to-remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a><span data-ttu-id="8c086-211">Exchange Online PowerShell을 사용 하 여 새 OME 기능 없이 암호화 된 전자 메일 회신에서 암호화를 제거 하려면 규칙을 만들려면</span><span class="sxs-lookup"><span data-stu-id="8c086-211">Use Exchange Online PowerShell to create a rule to remove encryption from email replies encrypted without the new OME capabilities</span></span>

1. <span data-ttu-id="8c086-p120">Exchange Online PowerShell에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8c086-p120">Connect to Exchange Online PowerShell. For more information, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="8c086-214">_RemoveOME_ 매개 변수를 설정 하 고 **New-transportrule** cmdlet을 사용 하 여 규칙을 만들 `$true`합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-214">Create a rule by using the **New-TransportRule** cmdlet and set the _RemoveOME_ parameter to `$true`.</span></span>

   <span data-ttu-id="8c086-215">Office 365 조직에 받는 사람에 게 보내진 모든 메일에서 암호화를 제거 하는이 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-215">This example removes the encryption from all mail sent to recipients in the Office 365 organization.</span></span>

   ```
   New-TransportRule -Name "Remove encryption from incoming mail" -SentToScope "InOrganization" -RemoveOME $true
   ```

   <span data-ttu-id="8c086-216">**참고:**</span><span class="sxs-lookup"><span data-stu-id="8c086-216">**Notes**:</span></span>

   - <span data-ttu-id="8c086-217">새 규칙의 고유 이름은 "받는 메일에서 암호화 제거"입니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-217">The unique name of the new rule is "Remove encryption from incoming mail".</span></span>

   - <span data-ttu-id="8c086-p121">_SentToScope_ 매개 변수는 메시지 받는 사람의 위치를 지정 합니다. 이 예제에서는 값 `InOrganization` 값을 나타내는 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-p121">The _SentToScope_ parameter specifies the location of the message recipients. In this example, the value `InOrganization` value is used, which indicates:</span></span> 

     - <span data-ttu-id="8c086-220">받는 사람 사서함, 메일 사용자, 그룹 또는 조직에서 메일 사용이 가능한 공용 폴더는 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-220">The recipient is a mailbox, mail user, group, or mail-enabled public folder in your organization.</span></span>

       <span data-ttu-id="8c086-221"> 선택하거나 </span><span class="sxs-lookup"><span data-stu-id="8c086-221">or</span></span>

     - <span data-ttu-id="8c086-222">신뢰할 수 있는 도메인 또는 조직 _및_ 메시지를 보내거나 인증 된 연결을 통해 받은에서 내부 릴레이 도메인으로 구성 된 허용된 도메인에서 받는 사람의 전자 메일 주소는 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c086-222">The recipient's email address is in an accepted domain that's configured as an authoritative domain or an internal relay domain in your organization, _and_ the message was sent or received over an authenticated connection.</span></span>

<span data-ttu-id="8c086-223">자세한 구문 및 매개변수 정보 [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8c086-223">For detailed syntax and parameter information, see [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c086-224">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8c086-224">Related Topics</span></span>

[<span data-ttu-id="8c086-225">Office 365의 암호화</span><span class="sxs-lookup"><span data-stu-id="8c086-225">Encryption in Office 365</span></span>](encryption.md)

[<span data-ttu-id="8c086-226">Azure 정보 보호 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능 설정</span><span class="sxs-lookup"><span data-stu-id="8c086-226">Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection</span></span>](set-up-new-message-encryption-capabilities.md)

[<span data-ttu-id="8c086-227">암호화된 메시지에 브랜딩 추가</span><span class="sxs-lookup"><span data-stu-id="8c086-227">Add branding to encrypted messages</span></span>](add-your-organization-brand-to-encrypted-messages.md)

[<span data-ttu-id="8c086-228">Exchange Online에서 흐름 규칙 (전송 규칙) 메일</span><span class="sxs-lookup"><span data-stu-id="8c086-228">Mail flow rules (transport rules) in Exchange Online</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=506707)

[<span data-ttu-id="8c086-229">Exchange Online Protection의 메일 흐름 규칙(전송 규칙)</span><span class="sxs-lookup"><span data-stu-id="8c086-229">Mail flow rules (transport rules) in Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=506708)
