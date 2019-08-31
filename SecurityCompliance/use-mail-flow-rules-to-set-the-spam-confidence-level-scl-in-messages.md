---
title: 메일 흐름 규칙을 사용하여 메시지의 스팸 신뢰 수준(SCL) 설정
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 4ccab17a-6d49-4786-aa28-92fb28893e99
ms.collection:
- M365-security-compliance
description: 관리자는 Exchange Online Protection에서 메시지의 SCL을 설정 하는 방법을 확인할 수 있습니다.
ms.openlocfilehash: 91252932671ec81d7269bb4e5e5c7680baa13580
ms.sourcegitcommit: 769b506c828c475c713dbb337e115714dcc7f17c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/31/2019
ms.locfileid: "36699159"
---
# <a name="use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages"></a><span data-ttu-id="599ad-103">메일 흐름 규칙을 사용하여 메시지의 스팸 신뢰 수준(SCL) 설정</span><span class="sxs-lookup"><span data-stu-id="599ad-103">Use mail flow rules to set the spam confidence level (SCL) in messages</span></span>

<span data-ttu-id="599ad-104">전자 메일 메시지의 SCL (스팸 지 수)을 설정 하는 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-104">You can create a mail flow rule (also known as a transport rule) that sets the spam confidence level (SCL) of an email message.</span></span> <span data-ttu-id="599ad-105">SCL은 메시지의 스팸 가능성을 측정 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-105">The SCL is a measure of how likely a message is to be spam.</span></span> <span data-ttu-id="599ad-106">스팸은 요청되지 않은(일반적으로 원치 않는) 전자 메일 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-106">Spam is unsolicited (and typically unwanted) email messages.</span></span> <span data-ttu-id="599ad-107">서비스는 SCL 등급에 따라 메시지에서 다른 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-107">The service takes different action on a message depending on its SCL rating.</span></span> <span data-ttu-id="599ad-108">예를 들어 동료 로부터 내부에 보낸 메시지가 스팸이 아닌 것을 신뢰 하기 때문에 조직 내부의 사용자가 보낸 메시지에 대해서는 스팸 콘텐츠 필터링을 무시 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-108">For example, you might want to bypass spam content filtering for messages that are sent from people inside your organization because you trust that a message sent internally from a colleague isn't spam.</span></span> <span data-ttu-id="599ad-109">메일 흐름 규칙을 사용 하 여 메시지의 SCL 값을 설정 하면 스팸을 보다 쉽게 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-109">Using mail flow rules to set the SCL value of a message gives you increased control in handling spam.</span></span> 
  
 <span data-ttu-id="599ad-110">**시작하기 전에 알아야 할 내용**</span><span class="sxs-lookup"><span data-stu-id="599ad-110">**What do you need to know before you begin?**</span></span>
  
- <span data-ttu-id="599ad-111">이 절차의 예상 완료 시간: 10 분.</span><span class="sxs-lookup"><span data-stu-id="599ad-111">Estimated time to complete this procedure: 10 minutes.</span></span>
    
- <span data-ttu-id="599ad-112">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-112">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="599ad-113">필요한 사용 권한을 확인 하려면 [Feature permissions In Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 또는 [FEATURE permissions in EOP에서](eop/feature-permissions-in-eop.md)"메일 흐름 규칙" 항목을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="599ad-113">To see what permissions you need, see the "Mail flow rules" entry in [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) or [Feature permissions in EOP](eop/feature-permissions-in-eop.md).</span></span> 
    
- <span data-ttu-id="599ad-114">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대 한 자세한 내용은 [Exchange Online에서 exchange 관리 센터에 대 한 바로 가기 키](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="599ad-114">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>
    
### <a name="to-create-a-mail-flow-rule-that-sets-the-scl-of-a-message"></a><span data-ttu-id="599ad-115">메시지의 SCL을 설정 하는 메일 흐름 규칙을 만들려면</span><span class="sxs-lookup"><span data-stu-id="599ad-115">To create a mail flow rule that sets the SCL of a message</span></span>

1. <span data-ttu-id="599ad-116">EAC (Exchange 관리 센터)에서 **메일 흐름** \> **규칙**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-116">In the Exchange admin center (EAC), choose **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="599ad-117">**새로**![만들기 아이콘](media/ITPro-EAC-AddIcon.gif)을 선택한 다음 **새 규칙 만들기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-117">Choose **New**![Add Icon](media/ITPro-EAC-AddIcon.gif), and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="599ad-118">규칙 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-118">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="599ad-119">**기타 옵션**을 선택한 다음 다음의 **경우이 규칙 적용**에서이 규칙에 대해 설정할 작업을 트리거할 조건을 지정 합니다 (SCL 값 설정).</span><span class="sxs-lookup"><span data-stu-id="599ad-119">Choose **More options**, and then under **Apply this rule if**, specify a condition that will trigger the action you'll be setting for this rule (which is to set the SCL value).</span></span>
    
    <span data-ttu-id="599ad-120">예를 들어 **보낸 사람이** \> **내부/외부 인지**설정할 수 있으며, **보낸 사람 위치 선택** 대화 상자에서 **조직 내부**를 선택 하 고 **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-120">For example, you can set **The sender** \> **is internal/external**, and then in the **select sender location** dialog box, select **Inside the organization**, and choose **ok**.</span></span><br/>
    <span data-ttu-id="599ad-121">![보낸 사람 위치 선택](media/EOP-ETR-SetSCL-1.jpg)</span><span class="sxs-lookup"><span data-stu-id="599ad-121">![Select sender location](media/EOP-ETR-SetSCL-1.jpg)</span></span>
  
5. <span data-ttu-id="599ad-122">**다음 작업 실행**에서 **메시지 속성 수정** \> **SCL(스팸 지수) 설정**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-122">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
  
6. <span data-ttu-id="599ad-123">**SCL 지정** 대화 상자에서 다음 값 중 하나를 선택 하 고 **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-123">In the **specify SCL** dialog box, select one of the following values, and choose **ok**:</span></span>
    
  - <span data-ttu-id="599ad-124">**스팸 필터링 무시** -SCL을-1로 설정 하므로 콘텐츠 필터링이 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-124">**Bypass spam filtering** - This sets the SCL to -1, which means that content filtering won't be performed.</span></span> 
    
  - <span data-ttu-id="599ad-125">**0-4** -SCL을 이러한 값 중 하나로 설정 하면 메시지가 추가 처리를 위해 콘텐츠 필터와 함께 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-125">**0-4** - When you set the SCL to one of these values, the message will be passed along to the content filter for additional processing.</span></span> 
    
  - <span data-ttu-id="599ad-126">**5, 6** -SCL을 이러한 값 중 하나로 설정 하면 해당 콘텐츠 필터 정책의 **스팸** 에 대해 지정 된 작업이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-126">**5, 6** - When you set the SCL to one of these values, the action specified for **Spam** in the applicable content filter policies will be applied.</span></span> <span data-ttu-id="599ad-127">기본적으로 받는 사람의 정크 메일 폴더로 메시지를 전송 하는 작업이 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-127">By default, the action is to send the message to the recipient's Junk Email folder.</span></span> 
    
  - <span data-ttu-id="599ad-128">**7-9** -SCL을 이러한 값 중 하나로 설정 하면 해당 콘텐츠 필터 정책의 **신뢰도가 높은 스팸** 에 대해 지정 된 작업이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-128">**7-9** - When you set the SCL to one of these values, the action specified for **High confidence spam** in the applicable content filter policies will be applied.</span></span> <span data-ttu-id="599ad-129">기본적으로 받는 사람의 정크 메일 폴더로 메시지를 전송 하는 작업이 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-129">By default, the action is to send the message to the recipient's Junk Email folder.</span></span> 
    
    <span data-ttu-id="599ad-130">콘텐츠 필터 정책 구성에 대 한 자세한 내용은 [스팸 필터 정책 구성을](configure-your-spam-filter-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="599ad-130">For more information about configuring your content filter policies, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span> <span data-ttu-id="599ad-131">서비스의 SCL 값에 대한 자세한 내용은 [스팸 신뢰 수준](spam-confidence-levels.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="599ad-131">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
7. <span data-ttu-id="599ad-132">규칙에 대 한 추가 속성을 지정 하 고 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-132">Specify additional properties for the rule, and choose **save**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="599ad-133">이 규칙에 대해 선택 하거나 지정할 수 있는 추가 속성에 대 한 자세한 내용은 [EAC를 사용 하 여 메일 흐름 규칙 만들기](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures#use-the-eac-to-create-mail-flow-rules)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="599ad-133">For more information about the additional properties you can select or specify for this rule, see [Use the EAC to create mail flow rules](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures#use-the-eac-to-create-mail-flow-rules).</span></span> 
  
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="599ad-134">작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="599ad-134">How do you know this worked?</span></span>

<span data-ttu-id="599ad-135">이 프로시저가 제대로 작동 하는지 확인 하려면 조직 내부의 사람에 게 전자 메일 메시지를 보내고 메시지에 대해 수행 된 작업이 예상 대로 진행 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-135">To verify that this procedure is working correctly, send an email message to someone inside your organization, and verify that the action performed on the message is as expected.</span></span> <span data-ttu-id="599ad-136">예를 들어 **SCL (스팸** 지 수)이 **스팸 필터링을 무시**하도록 설정 하는 경우 메시지를 지정 된 받는 사람의 받은 편지 함으로 보내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-136">For example, if you **set the spam confidence level (SCL)** to **Bypass spam filtering**, then the message should be sent to the specified recipient's inbox.</span></span> <span data-ttu-id="599ad-137">그러나 **SCL (스팸** 지 수)을 **9**로 설정 하 고 해당 콘텐츠 필터 정책에 대 한 **신뢰도가 높은 스팸** 작업을 정크 메일 폴더로 이동 하는 경우에는 지정 된 사용자에 게 메시지를 전송 해야 합니다. 받는 사람의 정크 메일 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="599ad-137">However, if you **set the spam confidence level (SCL)** to **9**, and the **High confidence spam** action for your applicable content filter policies is to move the message to the Junk Email folder, then the message should be sent to the specified recipient's Junk Email folder.</span></span> 
  

