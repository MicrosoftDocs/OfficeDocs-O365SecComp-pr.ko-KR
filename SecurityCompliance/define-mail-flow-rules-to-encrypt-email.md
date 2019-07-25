---
title: Office 365에서 전자 메일 메시지를 암호화하기 위한 메일의 흐름 규정을 정의
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 9b7daf19-d5f2-415b-bc43-a0f5f4a585e8
ms.collection:
- M365-security-compliance
description: 관리자는 Office 365 메시지 암호화를 사용 하 여 메시지를 암호화 하 고 암호를 해독 하는 메일 흐름 규칙 (전송 규칙)을 만드는 방법을 알 수 있습니다.
ms.openlocfilehash: 75b8e3c977a2708eb1edb8e2b94f555aa54045ca
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854692"
---
# <a name="define-mail-flow-rules-to-encrypt-email-messages-in-office-365"></a><span data-ttu-id="ded9f-103">Office 365에서 전자 메일 메시지를 암호화하기 위한 메일의 흐름 규정을 정의</span><span class="sxs-lookup"><span data-stu-id="ded9f-103">Define mail flow rules to encrypt email messages in Office 365</span></span>

<span data-ttu-id="ded9f-104">Office 365 전역 관리자는 보내는 전자 메일 메시지를 보호 하는 데 도움이 되는 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-104">As an Office 365 global administrator, you can create mail flow rules (also known as transport rules) to help protect email messages you send and receive.</span></span> <span data-ttu-id="ded9f-105">규칙을 설정 하 여 보내는 전자 메일 메시지를 암호화 하 고 조직 내부에서 전송 되는 암호화 된 메시지에서 또는 조직이 보낸 암호화 된 메시지에 대 한 암호화를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-105">You can set up rules to encrypt any outgoing email messages and remove encryption from encrypted messages coming from inside your organization or from replies to encrypted messages sent from your organization.</span></span> <span data-ttu-id="ded9f-106">EAC (Exchange 관리 센터) 또는 Exchange Online PowerShell을 사용 하 여 이러한 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-106">You can use the Exchange admin center (EAC) or Exchange Online PowerShell to create these rules.</span></span> <span data-ttu-id="ded9f-107">전체 암호화 규칙 외에도 최종 사용자에 대한 개별 메시지 암호화 옵션을 사용할지 여부를 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-107">In addition to overall encryption rules, you can also choose to enable or disable individual message encryption options for end-users.</span></span>

||
|:-----|
|<span data-ttu-id="ded9f-108">이 문서는 Office 365 메시지 암호화에 대 한 보다 광범위 한 문서에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-108">This article is part of a larger series of articles about Office 365 Message Encryption.</span></span> <span data-ttu-id="ded9f-109">이 문서는 관리자와 ITPros 전문가를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-109">This article is intended for administrators and ITPros.</span></span> <span data-ttu-id="ded9f-110">암호화 된 메시지를 보내거나 받는 방법에 대 한 정보를 찾으려는 경우에는 [Office 365 메시지 암호화 (OME)](ome.md) 의 문서 목록을 참조 하 여 요구 사항에 가장 적합 한 문서를 검색 하세요.</span><span class="sxs-lookup"><span data-stu-id="ded9f-110">If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

<span data-ttu-id="ded9f-111">최근에 AD RMS에서 Azure Information Protection으로 마이그레이션한 경우 기존 메일 흐름 규칙을 검토 하 여 새 환경에서 계속 작동 하는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-111">If you recently migrated from AD RMS to Azure Information Protection, you'll need to review your existing mail flow rules to ensure that they continue to work in your new environment.</span></span> <span data-ttu-id="ded9f-112">또한 Azure Information Protection을 통해 새 Office 365 메시지 암호화 (OME) 기능을 활용 하려는 경우 기존 메일 흐름 규칙을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-112">Additionally, if you want to take advantage of the new Office 365 Message Encryption (OME) capabilities available to you through Azure Information Protection, you need to update your existing mail flow rules.</span></span> <span data-ttu-id="ded9f-113">그렇지 않으면 사용자는 새로운 OME 환경이 아닌 이전 HTML 첨부 파일 형식을 사용 하는 암호화 된 메일을 계속 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-113">Otherwise, your users will continue to receive encrypted mail that uses the previous HTML attachment format instead of the new, seamless OME experience.</span></span> <span data-ttu-id="ded9f-114">아직 OME을 설정 하지 않은 경우 정보를 보려면 [새 Office 365 메시지 암호화 기능 설정을](set-up-new-message-encryption-capabilities.md) 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ded9f-114">If you haven't set up OME yet, see [Set up new Office 365 Message Encryption capabilities](set-up-new-message-encryption-capabilities.md) for information.</span></span>

<span data-ttu-id="ded9f-115">메일 흐름 규칙을 만드는 구성 요소와 메일 흐름 규칙의 작동 방식에 대 한 자세한 내용은 [메일 흐름 규칙 (전송 규칙)에서 Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ded9f-115">For information about the components that make up mail flow rules and how mail flow rules work, see [Mail flow rules (transport rules) in Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules).</span></span> <span data-ttu-id="ded9f-116">메일 흐름 규칙이 Azure Information Protection과 함께 작동 하는 방식에 대 한 자세한 내용은 [Azure Information protection 레이블에 대 한 Exchange Online 메일 흐름 규칙 구성을](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-exo-rules)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ded9f-116">For additional information about how mail flow rules work with Azure Information Protection, see [Configuring Exchange Online mail flow rules for Azure Information Protection labels](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-exo-rules).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ded9f-117">하이브리드 Exchange 환경에서는 온-프레미스 사용자가 Exchange Online을 통해 전자 메일을 라우팅하는 경우에만 OME를 사용 하 여 암호화 된 메일을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-117">For hybrid Exchange environments, on-premises users can send encrypted mail using OME only if email is routed through Exchange Online.</span></span> <span data-ttu-id="ded9f-118">하이브리드 Exchange 환경에서 OME을 구성 하려면 먼저 [하이브리드 구성 마법사를 사용 하 여 하이브리드를 구성한](https://docs.microsoft.com/Exchange/exchange-hybrid) 다음 [전자 메일 서버에서 Office 365로 메일이 전송 되도록 구성](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365)해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-118">To configure OME in a hybrid Exchange environment, you need to first [configure hybrid using the Hybrid Configuration wizard](https://docs.microsoft.com/Exchange/exchange-hybrid) and then [configure mail to flow from your email server to Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365).</span></span> <span data-ttu-id="ded9f-119">Office 365를 통해 메일이 전송 되도록 구성한 후에는이 지침을 사용 하 여 OME에 대 한 메일 흐름 규칙을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-119">Once you've configured mail to flow through Office 365, then you can configure mail flow rules for OME by using this guidance.</span></span>

## <a name="create-mail-flow-rules-to-encrypt-email-messages-with-the-new-ome-capabilities"></a><span data-ttu-id="ded9f-120">새 OME 기능을 사용 하 여 전자 메일 메시지를 암호화 하는 메일 흐름 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="ded9f-120">Create mail flow rules to encrypt email messages with the new OME capabilities</span></span>

<span data-ttu-id="ded9f-121">EAC를 사용 하 여 새 OME 기능으로 메시지 암호화를 트리거하는 메일 흐름 규칙을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-121">You can define mail flow rules for triggering message encryption with the new OME capabilities by using the EAC.</span></span>

### <a name="use-the-eac-to-create-a-rule-for-encrypting-email-messages-with-the-new-ome-capabilities"></a><span data-ttu-id="ded9f-122">EAC를 사용 하 여 새 OME 기능을 사용 하 여 전자 메일 메시지를 암호화 하는 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="ded9f-122">Use the EAC to create a rule for encrypting email messages with the new OME capabilities</span></span>

1. <span data-ttu-id="ded9f-123">웹 브라우저에서 전역 관리자 권한이 부여 된 회사 또는 학교 계정을 사용 하 여 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-123">In a web browser, using a work or school account that has been granted global administrator permissions, [sign in to Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).</span></span>

2. <span data-ttu-id="ded9f-124">**관리** 타일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-124">Choose the **Admin** tile.</span></span>

3. <span data-ttu-id="ded9f-125">Microsoft 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-125">In the Microsoft 365 admin center, choose **Admin centers** \> **Exchange**.</span></span>

4. <span data-ttu-id="ded9f-126">EAC \*\*\*\* ![에서](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **메일 흐름** \> **규칙** 으로 이동 하 고 새로 만들기 아이콘을 선택 하 여 **새 규칙을 만듭니다**.</span><span class="sxs-lookup"><span data-stu-id="ded9f-126">In the EAC, go to **Mail flow** \> **Rules** and select **New** ![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **Create a new rule**.</span></span> <span data-ttu-id="ded9f-127">EAC를 사용 하는 방법에 대 한 자세한 내용은 exchange [Online의 exchange 관리 센터](https://docs.microsoft.com/exchange/exchange-admin-center)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ded9f-127">For more information about using the EAC, see [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span></span>

5. <span data-ttu-id="ded9f-128">**이름**에 DrToniRamos@hotmail.com에 대 한 메일 암호화와 같은 규칙의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-128">In **Name**, type a name for the rule, such as Encrypt mail for DrToniRamos@hotmail.com.</span></span>

6. <span data-ttu-id="ded9f-p107">**다음의 경우 이 규칙 적용**에서 조건을 선택하고 필요한 경우 값을 입력합니다. 예를 들어 DrToniRamos@hotmail.com에 보내는 메시지를 암호화하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-p107">In **Apply this rule if** select a condition, and enter a value if necessary. For example, to encrypt messages going to DrToniRamos@hotmail.com:</span></span>

   1. <span data-ttu-id="ded9f-131">**다음의 경우 이 규칙 적용**에서 **받는 사람이 다음과 같음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-131">In **Apply this rule if**, select **the recipient is**.</span></span>

   2. <span data-ttu-id="ded9f-132">연락처 목록에서 기존 이름을 선택하거나 **이름 확인** 상자에 새 전자 메일 주소를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-132">Select an existing name from the contact list or type a new email address in the **check names** box.</span></span>

      - <span data-ttu-id="ded9f-133">기존 이름을 선택하려면 목록에서 이름을 선택한 다음 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-133">To select an existing name, select it from the list and then click **OK**.</span></span>

      - <span data-ttu-id="ded9f-134">새 이름을 입력 하려면 **이름 확인** 상자에 전자 메일 주소를 입력 하 고 **이름** \> 확인 **을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-134">To enter a new name, type an email address in the **check names** box and then select **check names** \> **OK**.</span></span>

7. <span data-ttu-id="ded9f-135">조건을 더 추가 하려면 **기타 옵션** 을 선택한 다음 **조건 추가** 를 선택 하 고 목록에서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-135">To add more conditions, choose **More options** and then choose **add condition** and select from the list.</span></span>

   <span data-ttu-id="ded9f-136">예를 들어 받는 사람이 조직 외부에 있는 경우에만이 규칙을 적용 하려면 **조건 추가** 를 선택한 다음 받는 사람이 **조직** \> \*\*\*\* 외부에 있는 **외부/내부** \> 에 있습니다 .를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-136">For example, to apply the rule only if the recipient is outside your organization, select **add condition** and then select **The recipient is external/internal** \> **Outside the organization** \> **OK**.</span></span>

8. <span data-ttu-id="ded9f-137">새 OME 기능을 사용 하 여 암호화를 사용 하도록 설정 하려면 **다음 작업을 수행**하 고 **메시지 보안 수정을** 선택한 다음 **Office 365 메시지 암호화 및 권한 보호 적용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-137">To enable encryption using the new OME capabilities, from **Do the following**, select **Modify the message security** and then choose **Apply Office 365 Message Encryption and rights protection**.</span></span> <span data-ttu-id="ded9f-138">목록에서 RMS 템플릿을 선택 하 고 **저장**을 선택한 다음 **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-138">Select an RMS template from the list, choose **Save**, and then choose **OK**.</span></span>
  
  <span data-ttu-id="ded9f-139">서식 파일 목록에는 모든 기본 서식 파일 및 옵션 뿐 아니라 Office 365에서 사용 하기 위해 만든 사용자 지정 서식 파일도 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-139">The list of templates includes all default templates and options as well as any custom templates you've created for use by Office 365.</span></span> <span data-ttu-id="ded9f-140">목록이 비어 있으면 [새 office 365 메시지 암호화 기능 설정](set-up-new-message-encryption-capabilities.md)에 설명 된 대로 Office 365 메시지 암호화를 새로운 기능으로 설정 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-140">If the list is empty, ensure that you have set up Office 365 Message Encryption with the new capabilities as described in [Set up new Office 365 Message Encryption capabilities](set-up-new-message-encryption-capabilities.md).</span></span> <span data-ttu-id="ded9f-141">기본 서식 파일에 대 한 자세한 내용은 [Azure Information Protection의 템플릿 구성 및 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ded9f-141">For information about the default templates, see [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates).</span></span> <span data-ttu-id="ded9f-142">**전달 하지** 않음 옵션에 대 한 자세한 내용은 [전자 메일에 대 한 전달 옵션 안 함](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ded9f-142">For information about the **Do Not Forward** option, see [Do Not Forward option for emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails).</span></span> <span data-ttu-id="ded9f-143">**암호화 전용** 옵션에 대 한 자세한 내용은 [전자 메일에 대 한 암호화 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ded9f-143">For information about the **encrypt only** option, see [Encrypt Only option for emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).</span></span>

  <span data-ttu-id="ded9f-144">다른 작업을 지정 하려는 경우 **작업 추가** 를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-144">You can choose **add action** if you want to specify another action.</span></span>

### <a name="use-the-eac-to-update-an-existing-mail-flow-rule-to-use-the-new-ome-capabilities"></a><span data-ttu-id="ded9f-145">EAC를 사용 하 여 새 OME 기능을 사용 하도록 기존 메일 흐름 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="ded9f-145">Use the EAC to update an existing mail flow rule to use the new OME capabilities</span></span>

1. <span data-ttu-id="ded9f-146">웹 브라우저에서 전역 관리자 권한이 부여 된 회사 또는 학교 계정을 사용 하 여 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-146">In a web browser, using a work or school account that has been granted global administrator permissions, [sign in to Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).</span></span>

2. <span data-ttu-id="ded9f-147">**관리** 타일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-147">Choose the **Admin** tile.</span></span>

3. <span data-ttu-id="ded9f-148">Microsoft 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-148">In the Microsoft 365 admin center, choose **Admin centers** \> **Exchange**.</span></span>

4. <span data-ttu-id="ded9f-149">EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-149">In the EAC, go to **Mail flow** \> **Rules**.</span></span>

5. <span data-ttu-id="ded9f-150">메일 흐름 규칙 목록에서 새 OME 기능을 사용 하도록 수정할 규칙을 선택 하 고 편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) **편집** ![을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-150">In the list of mail flow rules, select the rule you want to modify to use the new OME capabilities and then choose **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>

6. <span data-ttu-id="ded9f-151">새 OME 기능을 사용 하 여 암호화를 사용 하도록 설정 하려면 **다음 작업을 수행**하 고 **메시지 보안 수정을** 선택한 다음 **Office 365 메시지 암호화 및 권한 보호 적용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-151">To enable encryption using the new OME capabilities, from **Do the following**, choose **Modify the message security** and then choose **Apply Office 365 Message Encryption and rights protection**.</span></span> <span data-ttu-id="ded9f-152">목록에서 RMS 템플릿을 선택 하 고 **저장** 을 선택한 다음 **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-152">Select an RMS template from the list, choose **Save** and then choose **OK**.</span></span>

   <span data-ttu-id="ded9f-153">서식 파일 목록에는 모든 기본 서식 파일 및 옵션 뿐 아니라 Office 365에서 사용 하기 위해 만든 사용자 지정 서식 파일도 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-153">The list of templates includes all default templates and options as well as any custom templates you've created for use by Office 365.</span></span> <span data-ttu-id="ded9f-154">목록이 비어 있으면 Office 365 메시지 암호화가 [Azure Information Protection의 새로운 office 365 메시지 암호화 기능 설정](set-up-new-message-encryption-capabilities.md)에 설명 된 대로 새로운 기능을 사용 하 여 설정 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-154">If the list is empty, ensure that you have set up Office 365 Message Encryption with the new capabilities as described in [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection](set-up-new-message-encryption-capabilities.md).</span></span> <span data-ttu-id="ded9f-155">기본 서식 파일에 대 한 자세한 내용은 [Azure Information Protection의 템플릿 구성 및 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ded9f-155">For information about the default templates, see [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates).</span></span> <span data-ttu-id="ded9f-156">**전달 하지** 않음 옵션에 대 한 자세한 내용은 [전자 메일에 대 한 전달 옵션 안 함](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ded9f-156">For information about the **Do Not Forward** option, see [Do Not Forward option for emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails).</span></span> <span data-ttu-id="ded9f-157">**암호화 전용** 옵션에 대 한 자세한 내용은 [전자 메일에 대 한 암호화 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ded9f-157">For information about the **encrypt only** option, see [Encrypt Only option for emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).</span></span>

   <span data-ttu-id="ded9f-158">다른 작업을 지정 하려는 경우 **작업 추가** 를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-158">You can choose **add action** if you want to specify another action.</span></span>

7. <span data-ttu-id="ded9f-159">다음 작업 **수행** 목록에서 **메시지 보안** \> 을 수정 하도록 할당 된 모든 작업을 제거 하 **여 이전 버전의 OME을 적용**합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-159">From the **Do the following** list, remove any actions that are assigned to **Modify the message security** \> **Apply the previous version of OME**.</span></span>

8. <span data-ttu-id="ded9f-160">**저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-160">Choose **Save**.</span></span>

## <a name="create-mail-flow-rules-for-office-365-message-encryption-without-the-new-capabilities"></a><span data-ttu-id="ded9f-161">새 기능 없이 Office 365 메시지 암호화에 대 한 메일 흐름 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="ded9f-161">Create mail flow rules for Office 365 Message Encryption without the new capabilities</span></span>

<span data-ttu-id="ded9f-162">아직 Office 365 조 직을 새 OME 기능으로 이동 하지 않은 경우 다음 작업을 사용 하 여 조직에 대 한 메시지를 암호화 하는 메일 흐름 규칙을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-162">If you haven't yet moved your Office 365 organization to the new OME capabilities, use these tasks to define mail flow rules to encrypt messages for your organization.</span></span> <span data-ttu-id="ded9f-163">조직에 적합 한 시기에 새 OME 기능으로 바로 이동 하는 계획을 수립 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-163">Microsoft recommends that you make a plan to move to the new OME capabilities as soon as it is reasonable for your organization.</span></span> <span data-ttu-id="ded9f-164">자세한 내용은 [Azure Information Protection 기반으로 구축 된 새 Office 365 메시지 암호화 기능 설치](set-up-new-message-encryption-capabilities.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ded9f-164">For instructions, see [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection](set-up-new-message-encryption-capabilities.md).</span></span>

### <a name="use-the-eac-to-create-a-mail-flow-rule-for-encrypting-email-messages-without-the-new-ome-capabilities"></a><span data-ttu-id="ded9f-165">EAC를 사용 하 여 새 OME 기능 없이 전자 메일 메시지를 암호화 하기 위한 메일 흐름 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="ded9f-165">Use the EAC to create a mail flow rule for encrypting email messages without the new OME capabilities</span></span>

1. <span data-ttu-id="ded9f-166">웹 브라우저에서 전역 관리자 권한이 부여 된 회사 또는 학교 계정을 사용 하 여 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-166">In a web browser, using a work or school account that has been granted global administrator permissions, [sign in to Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).</span></span>

2. <span data-ttu-id="ded9f-167">**관리** 타일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-167">Choose the **Admin** tile.</span></span>

3. <span data-ttu-id="ded9f-168">Microsoft 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-168">In the Microsoft 365 admin center, choose **Admin centers** \> **Exchange**.</span></span>

4. <span data-ttu-id="ded9f-169">EAC \*\*\*\* ![에서](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **메일 흐름** \> **규칙** 으로 이동 하 고 새로 만들기 아이콘을 선택 하 여 **새 규칙을 만듭니다**.</span><span class="sxs-lookup"><span data-stu-id="ded9f-169">In the EAC, go to **Mail flow** \> **Rules** and select **New** ![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **Create a new rule**.</span></span> <span data-ttu-id="ded9f-170">EAC를 사용 하는 방법에 대 한 자세한 내용은 exchange [Online의 exchange 관리 센터](https://docs.microsoft.com/exchange/exchange-admin-center)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ded9f-170">For more information about using the EAC, see [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span></span>

5. <span data-ttu-id="ded9f-171">**이름**에 DrToniRamos@hotmail.com에 대 한 메일 암호화와 같은 규칙의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-171">In **Name**, type a name for the rule, such as Encrypt mail for DrToniRamos@hotmail.com.</span></span>

6. <span data-ttu-id="ded9f-p114">**다음의 경우 이 규칙 적용**에서 조건을 선택하고 필요한 경우 값을 입력합니다. 예를 들어 DrToniRamos@hotmail.com에 보내는 메시지를 암호화하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-p114">In **Apply this rule if** select a condition, and enter a value if necessary. For example, to encrypt messages going to DrToniRamos@hotmail.com:</span></span>

   1. <span data-ttu-id="ded9f-174">**다음의 경우 이 규칙 적용**에서 **받는 사람이 다음과 같음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-174">In **Apply this rule if**, select **the recipient is**.</span></span>

   2. <span data-ttu-id="ded9f-175">연락처 목록에서 기존 이름을 선택하거나 **이름 확인** 상자에 새 전자 메일 주소를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-175">Select an existing name from the contact list or type a new email address in the **check names** box.</span></span>

      - <span data-ttu-id="ded9f-176">기존 이름을 선택하려면 목록에서 이름을 선택한 다음 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-176">To select an existing name, select it from the list and then click **OK**.</span></span>

      - <span data-ttu-id="ded9f-177">새 이름을 입력 하려면 **이름 확인** 상자에 전자 메일 주소를 입력 하 고 **이름** \> 확인 **을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-177">To enter a new name, type an email address in the **check names** box and then select **check names** \> **OK**.</span></span>

7. <span data-ttu-id="ded9f-178">조건을 더 추가 하려면 **기타 옵션** 을 선택한 다음 **조건 추가** 를 선택 하 고 목록에서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-178">To add more conditions, choose **More options** and then select **add condition** and select from the list.</span></span>

   <span data-ttu-id="ded9f-179">예를 들어 받는 사람이 조직 외부에 있는 경우에만이 규칙을 적용 하려면 **조건 추가** 를 선택한 다음 받는 사람이 **조직** \> \*\*\*\* 외부에 있는 **외부/내부** \> 에 있습니다 .를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-179">For example, to apply the rule only if the recipient is outside your organization, select **add condition** and then select **The recipient is external/internal** \> **Outside the organization** \> **OK**.</span></span>

8. <span data-ttu-id="ded9f-180">새 OME 기능을 사용 하지 않고 암호화를 사용 하도록 설정 하려면 **다음 작업**에서 **메시지 보안** \> 수정을 선택 하 여 **이전 버전의 OME를 적용**한 다음 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-180">To enable encryption without using the new OME capabilities, in **Do the following**, select **Modify the message security** \> **Apply the previous version of OME**, and then choose **Save**.</span></span>

  <span data-ttu-id="ded9f-181">IRM 라이선싱을 사용할 수 없다는 오류가 표시 되는 경우에는 조직에 대 한 OME를 아직 설정 하지 않은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-181">If you receive an error that IRM licensing isn't enabled, then you haven't set up OME for your organization yet.</span></span> <span data-ttu-id="ded9f-182">지금 OME을 설정 하려면 새 OME 기능을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-182">If you'd like to set up OME now, you must set it up to use the new OME capabilities.</span></span> <span data-ttu-id="ded9f-183">자세한 내용은 [Azure Information Protection 기반으로 구축 된 새 Office 365 메시지 암호화 기능](set-up-new-message-encryption-capabilities.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ded9f-183">For information, see [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection](set-up-new-message-encryption-capabilities.md).</span></span> <span data-ttu-id="ded9f-184">Microsoft에서는 새 기능 없이는 OME의 새 배포를 설정 하는 것이 더 이상 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-184">Microsoft no longer supports setting up new deployments of OME without the new capabilities.</span></span>

  <span data-ttu-id="ded9f-185">다른 작업을 지정 하려는 경우 **작업 추가** 를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-185">You can choose **add action** if you want to specify another action.</span></span>

### <a name="use-exchange-online-powershell-to-create-a-mail-flow-rule-for-encrypting-email-messages-without-the-new-ome-capabilities"></a><span data-ttu-id="ded9f-186">Exchange Online PowerShell을 사용 하 여 새 OME 기능 없이 전자 메일 메시지를 암호화 하기 위한 메일 흐름 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="ded9f-186">Use Exchange Online PowerShell to create a mail flow rule for encrypting email messages without the new OME capabilities</span></span>

1. <span data-ttu-id="ded9f-187">Exchange Online PowerShell에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-187">Connect to Exchange Online PowerShell.</span></span> <span data-ttu-id="ded9f-188">자세한 내용은 [원격 PowerShell을 사용하여 Exchange Online에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ded9f-188">For more information, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="ded9f-189">**New-transportrule** cmdlet을 사용 하 여 규칙을 만들고 _ApplyOME_ 매개 변수를로 `$true`설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-189">Create a rule by using the **New-TransportRule** cmdlet and set the _ApplyOME_ parameter to `$true`.</span></span>

   <span data-ttu-id="ded9f-190">이 예에서는 DrToniRamos@hotmail.com으로 전송 되는 모든 전자 메일 메시지를 암호화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-190">This example requires that all email messages sent to DrToniRamos@hotmail.com must be encrypted.</span></span>

   ```powershell
   New-TransportRule -Name "Encrypt rule for Dr Toni Ramos" -SentTo "DrToniRamos@hotmail.com" -SentToScope "NotinOrganization" -ApplyOME $true
   ```

   <span data-ttu-id="ded9f-191">**참고:**</span><span class="sxs-lookup"><span data-stu-id="ded9f-191">**Notes**:</span></span>

   - <span data-ttu-id="ded9f-192">새 규칙의 고유한 이름은 "Dr Toni에 대 한 암호화 규칙"입니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-192">The unique name of the new rule is "Encrypt rule for Dr Toni Ramos".</span></span>

   - <span data-ttu-id="ded9f-193">_SentTo_ 매개 변수는 메시지 받는 사람 (이름, 전자 메일 주소, 고유 이름 등으로 식별 됨)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-193">The _SentTo_ parameter specifies the message recipients (identified by name, email address, distinguished name, etc.).</span></span> <span data-ttu-id="ded9f-194">이 예에서는 받는 사람이 전자 메일 주소 "DrToniRamos@hotmail.com"로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-194">In this example, the recipient is identified by the email address "DrToniRamos@hotmail.com".</span></span>

   - <span data-ttu-id="ded9f-195">_SentToScope_ 매개 변수는 메시지 받는 사람의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-195">The _SentToScope_ parameter specifies the location of the message recipients.</span></span> <span data-ttu-id="ded9f-196">이 예에서는 받는 사람의 사서함이 hotmail에 있고 Office 365 조직의 일부가 아니므로 값 `NotInOrganization` 이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-196">In this example, the recipient's mailbox is in hotmail and is not part of the Office 365 organization, so the value `NotInOrganization` is used.</span></span>

   <span data-ttu-id="ded9f-197">구문과 매개 변수에 대한 자세한 내용은 [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="ded9f-197">For detailed syntax and parameter information, see [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule).</span></span>

### <a name="remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a><span data-ttu-id="ded9f-198">새 OME 기능을 사용 하지 않고 암호화 된 전자 메일 회신에서 암호화 제거</span><span class="sxs-lookup"><span data-stu-id="ded9f-198">Remove encryption from email replies encrypted without the new OME capabilities</span></span>

<span data-ttu-id="ded9f-199">전자 메일 사용자가 암호화된 메시지를 보내면 해당 메시지의 받는 사람은 암호화된 회신을 통해 응답을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-199">When your email users send encrypted messages, recipients of those messages can respond with encrypted replies.</span></span> <span data-ttu-id="ded9f-200">메일 흐름 규칙을 만들면 조직의 전자 메일 사용자가 암호화 포털에 로그인 하 여 메시지를 볼 필요가 없도록 자동으로 회신에서 암호화를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-200">You can create mail flow rules to automatically remove encryption from replies so email users in your organization don't have to sign in to the encryption portal to view them.</span></span> <span data-ttu-id="ded9f-201">EAC 또는 Windows PowerShell cmdlet을 사용 하 여 이러한 규칙을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-201">You can use the EAC or Windows PowerShell cmdlets to define these rules.</span></span> <span data-ttu-id="ded9f-202">아직 새 OME 기능을 사용 하지 않는 경우 조직 내에서 전송 되거나 조직 내에서 전송 된 메시지에 회신 하는 메시지의 암호를 해독 하는 것만 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-202">If you are not yet using the new OME capabilities, you can only decrypt messages that are either sent from within your organization or messages that are replies to messages sent from within your organization.</span></span> <span data-ttu-id="ded9f-203">조직 외부에서 보낸 암호화 된 메시지의 암호를 해독할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-203">You cannot decrypt encrypted messages originating from outside of your organization.</span></span>

#### <a name="use-the-eac-to-create-a-rule-for-removing-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a><span data-ttu-id="ded9f-204">EAC를 사용 하 여 새 OME 기능 없이 암호화 된 전자 메일 응답에서 암호화를 제거 하는 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="ded9f-204">Use the EAC to create a rule for removing encryption from email replies encrypted without the new OME capabilities</span></span>

1. <span data-ttu-id="ded9f-205">웹 브라우저에서 관리자 권한이 부여 된 회사 또는 학교 계정을 사용 하 여 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-205">In a web browser, using a work or school account that has been granted admin permissions, [sign in to Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).</span></span>

2. <span data-ttu-id="ded9f-206">**관리** 타일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-206">Choose the **Admin** tile.</span></span>

3. <span data-ttu-id="ded9f-207">Microsoft 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-207">In the Microsoft 365 admin center, choose **Admin centers** \> **Exchange**.</span></span>

4. <span data-ttu-id="ded9f-208">EAC \*\*\*\* ![에서](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **메일 흐름** \> **규칙** 으로 이동 하 고 새로 만들기 아이콘을 선택 하 여 **새 규칙을 만듭니다**.</span><span class="sxs-lookup"><span data-stu-id="ded9f-208">In the EAC, go to **Mail flow** \> **Rules** and select **New** ![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **Create a new rule**.</span></span> <span data-ttu-id="ded9f-209">EAC를 사용 하는 방법에 대 한 자세한 내용은 exchange [Online의 exchange 관리 센터](https://docs.microsoft.com/exchange/exchange-admin-center)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ded9f-209">For more information about using the EAC, see [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span></span>

5. <span data-ttu-id="ded9f-210">**이름**에 규칙의 이름을 입력 합니다 (예: 받는 메일에서 암호화 제거).</span><span class="sxs-lookup"><span data-stu-id="ded9f-210">In **Name**, type a name for the rule, such as Remove encryption from incoming mail.</span></span>

6. <span data-ttu-id="ded9f-211">**다음의 경우이 규칙 적용** 에서 **받는 사람이** \> **조직 내부**에 있는 것과 같이 메시지에서 암호화를 제거 해야 하는 조건을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-211">In **Apply this rule if** select the conditions where encryption should be removed from messages, such as **The recipient is located** \> **Inside the organization**.</span></span>

7. <span data-ttu-id="ded9f-212">**다음 작업 실행**에서 **메시지 보안** \> 수정을 선택 하 여 **이전 버전의 OME을 제거**합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-212">In **Do the following**, select **Modify the message security** \> **Remove the previous version of OME**.</span></span>

8. <span data-ttu-id="ded9f-213">**저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-213">Select **Save**.</span></span>

#### <a name="use-exchange-online-powershell-to-create-a-rule-to-remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a><span data-ttu-id="ded9f-214">Exchange Online PowerShell을 사용 하 여 새 OME 기능 없이 암호화 된 전자 메일 응답에서 암호화를 제거 하는 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="ded9f-214">Use Exchange Online PowerShell to create a rule to remove encryption from email replies encrypted without the new OME capabilities</span></span>

1. <span data-ttu-id="ded9f-215">Exchange Online PowerShell에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-215">Connect to Exchange Online PowerShell.</span></span> <span data-ttu-id="ded9f-216">자세한 내용은 [원격 PowerShell을 사용하여 Exchange Online에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ded9f-216">For more information, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="ded9f-217">**New-transportrule** cmdlet을 사용 하 여 규칙을 만들고 _RemoveOME_ 매개 변수를로 `$true`설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-217">Create a rule by using the **New-TransportRule** cmdlet and set the _RemoveOME_ parameter to `$true`.</span></span>

   <span data-ttu-id="ded9f-218">이 예에서는 Office 365 조직의 받는 사람에 게 전송 되는 모든 메일에서 암호화를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-218">This example removes the encryption from all mail sent to recipients in the Office 365 organization.</span></span>

   ```powershell
   New-TransportRule -Name "Remove encryption from incoming mail" -SentToScope "InOrganization" -RemoveOME $true
   ```

   <span data-ttu-id="ded9f-219">**참고:**</span><span class="sxs-lookup"><span data-stu-id="ded9f-219">**Notes**:</span></span>

   - <span data-ttu-id="ded9f-220">새 규칙의 고유한 이름은 "받는 메일에서 암호화 제거"입니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-220">The unique name of the new rule is "Remove encryption from incoming mail".</span></span>

   - <span data-ttu-id="ded9f-221">_SentToScope_ 매개 변수는 메시지 받는 사람의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-221">The _SentToScope_ parameter specifies the location of the message recipients.</span></span> <span data-ttu-id="ded9f-222">이 예제에서는 다음을 나타내는 `InOrganization` 값 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded9f-222">In this example, the value `InOrganization` value is used, which indicates:</span></span>

     - <span data-ttu-id="ded9f-223">받는 사람이 조직의 사서함, 메일 사용자, 그룹 또는 메일 사용이 가능한 공용 폴더인 경우</span><span class="sxs-lookup"><span data-stu-id="ded9f-223">The recipient is a mailbox, mail user, group, or mail-enabled public folder in your organization.</span></span>

       <span data-ttu-id="ded9f-224">또는</span><span class="sxs-lookup"><span data-stu-id="ded9f-224">or</span></span>

     - <span data-ttu-id="ded9f-225">받는 사람의 전자 메일 주소가 신뢰할 수 있는 도메인 이나 조직의 내부 릴레이 도메인으로 구성 된 허용 도메인에 _있으며_ , 인증 된 연결을 통해 메시지를 보내거나 받은 경우</span><span class="sxs-lookup"><span data-stu-id="ded9f-225">The recipient's email address is in an accepted domain that's configured as an authoritative domain or an internal relay domain in your organization, _and_ the message was sent or received over an authenticated connection.</span></span>

<span data-ttu-id="ded9f-226">구문과 매개 변수에 대한 자세한 내용은 [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="ded9f-226">For detailed syntax and parameter information, see [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ded9f-227">관련 주제</span><span class="sxs-lookup"><span data-stu-id="ded9f-227">Related Topics</span></span>

[<span data-ttu-id="ded9f-228">Office 365의 암호화</span><span class="sxs-lookup"><span data-stu-id="ded9f-228">Encryption in Office 365</span></span>](encryption.md)

[<span data-ttu-id="ded9f-229">새로운 Office 365 메시지 암호화 기능 설정</span><span class="sxs-lookup"><span data-stu-id="ded9f-229">Set up new Office 365 Message Encryption capabilities</span></span>](set-up-new-message-encryption-capabilities.md)

[<span data-ttu-id="ded9f-230">암호화된 메시지에 브랜딩 추가</span><span class="sxs-lookup"><span data-stu-id="ded9f-230">Add branding to encrypted messages</span></span>](add-your-organization-brand-to-encrypted-messages.md)

[<span data-ttu-id="ded9f-231">Exchange Online의 메일 흐름 규칙 (전송 규칙)</span><span class="sxs-lookup"><span data-stu-id="ded9f-231">Mail flow rules (transport rules) in Exchange Online</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=506707)

[<span data-ttu-id="ded9f-232">Exchange Online Protection의 메일 흐름 규칙(전송 규칙)</span><span class="sxs-lookup"><span data-stu-id="ded9f-232">Mail flow rules (transport rules) in Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=506708)
