---
title: 메일 흐름 규칙을 사용하여 메시지의 스팸 신뢰 수준(SCL) 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 4ccab17a-6d49-4786-aa28-92fb28893e99
description: 신뢰도 scl (스팸)의 전자 메일 메시지를 설정 하는 전송 규칙을 만들 수 있습니다. SCL은 스팸일 가능성 메시지의 측정 됩니다. 스팸 원치 않는 (및 일반적으로 원치 않는) 전자 메일 메시지 수입니다. 서비스의 SCL 등급에 따라 메시지에 대해 다른 작업을 수행 합니다. 예, 다음 스팸 콘텐츠 동료에서 내부적으로 보내는 메시지 스팸을 신뢰할 수 있으므로 조직 내부에서 보낸 메시지에 대 한 필터링을 무시 하는 것이 좋습니다. 스팸 처리에 대 한 제어를 늘리기 제공 메시지의 SCL 값을 설정 하려면 전송 규칙을 사용 하 여 합니다.
ms.openlocfilehash: 7abd0d1881374b1f2a4bd32ee480445f7683d1b3
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002897"
---
# <a name="use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages"></a><span data-ttu-id="83a6b-108">메일 흐름 규칙을 사용하여 메시지의 스팸 신뢰 수준(SCL) 설정</span><span class="sxs-lookup"><span data-stu-id="83a6b-108">Use mail flow rules to set the spam confidence level (SCL) in messages</span></span>

<span data-ttu-id="83a6b-p102">신뢰도 scl (스팸)의 전자 메일 메시지를 설정 하는 전송 규칙을 만들 수 있습니다. SCL은 스팸일 가능성 메시지의 측정 됩니다. 스팸 원치 않는 (및 일반적으로 원치 않는) 전자 메일 메시지 수입니다. 서비스의 SCL 등급에 따라 메시지에 대해 다른 작업을 수행 합니다. 예, 다음 스팸 콘텐츠 동료에서 내부적으로 보내는 메시지 스팸을 신뢰할 수 있으므로 조직 내부에서 보낸 메시지에 대 한 필터링을 무시 하는 것이 좋습니다. 스팸 처리에 대 한 제어를 늘리기 제공 메시지의 SCL 값을 설정 하려면 전송 규칙을 사용 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="83a6b-p102">You can create a transport rule that sets the spam confidence level (SCL) of an email message. The SCL is a measure of how likely a message is to be spam. Spam is unsolicited (and typically unwanted) email messages. The service takes different action on a message depending on its SCL rating. For example, you might want to bypass spam content filtering for messages that are sent from people inside your organization because you trust that a message sent internally from a colleague isn't spam. Using transport rules to set the SCL value of a message gives you increased control in handling spam.</span></span> 
  
 <span data-ttu-id="83a6b-115">**시작하기 전에 알아야 할 내용**</span><span class="sxs-lookup"><span data-stu-id="83a6b-115">**What do you need to know before you begin?**</span></span>
  
- <span data-ttu-id="83a6b-116">예상이 절차를 완료 시간: 10 분.</span><span class="sxs-lookup"><span data-stu-id="83a6b-116">Estimated time to complete this procedure: 10 minutes.</span></span>
    
- <span data-ttu-id="83a6b-p103">이 절차를 수행 하기 전에 사용 권한을 할당 해야 합니다. 필요한 사용 권한을 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 또는 [EOP의 기능 사용 권한에서](eop/feature-permissions-in-eop.md)"전송 규칙" 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="83a6b-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) or [Feature permissions in EOP](eop/feature-permissions-in-eop.md).</span></span> 
    
- <span data-ttu-id="83a6b-119">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Exchange 관리 센터의 바로 가기 키**을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="83a6b-119">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
### <a name="to-create-a-transport-rule-that-sets-the-scl-of-a-message"></a><span data-ttu-id="83a6b-120">메시지의 SCL을 설정 하는 전송 규칙을 만들려면</span><span class="sxs-lookup"><span data-stu-id="83a6b-120">To create a transport rule that sets the SCL of a message</span></span>

1. <span data-ttu-id="83a6b-121">(EAC)의 Exchange 관리 센터에서 **메일 흐름** 선택 \> **규칙**입니다.</span><span class="sxs-lookup"><span data-stu-id="83a6b-121">In the Exchange admin center (EAC), choose **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="83a6b-122">**새로 만들기**를 선택![아이콘 추가](media/ITPro-EAC-AddIcon.gif), 한 다음 **새 규칙 만들기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="83a6b-122">Choose **New**![Add Icon](media/ITPro-EAC-AddIcon.gif), and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="83a6b-123">규칙 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83a6b-123">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="83a6b-124">**기타 옵션**을 선택 하 고 **하는 경우이 규칙 적용**에서 (이 SCL 값을 설정 하려면)이이 규칙에 대 한 설정 하겠습니다 하는 경우 작업을 트리거하는 조건의 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83a6b-124">Choose **More options**, and then under **Apply this rule if**, specify a condition that will trigger the action you'll be setting for this rule (which is to set the SCL value).</span></span>
    
    <span data-ttu-id="83a6b-125">예 **보낸** 를 설정할 수 있습니다 \> **내부/외부가**아니면 다음 **보낸사람 위치 선택** 대화 상자에서 선택 **조직 내부**, 하 고 **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="83a6b-125">For example, you can set **The sender** \> **is internal/external**, and then in the **select sender location** dialog box, select **Inside the organization**, and choose **ok**.</span></span></br>
    <span data-ttu-id="83a6b-126">![보낸 사람 위치 선택](media/EOP-ETR-SetSCL-1.jpg)</span><span class="sxs-lookup"><span data-stu-id="83a6b-126">![Select sender location](media/EOP-ETR-SetSCL-1.jpg)</span></span>
  
5. <span data-ttu-id="83a6b-127">**다음 작업 실행**에서 **메시지 속성 수정** \> **SCL(스팸 지수) 설정**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="83a6b-127">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
  
6. <span data-ttu-id="83a6b-128">**SCL 지정** 대화 상자에서 다음 값 중 하나를 선택 하 고 **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="83a6b-128">In the **specify SCL** dialog box, select one of the following values, and choose **ok**:</span></span>
    
  - <span data-ttu-id="83a6b-129">**바이패스 스팸 필터링** -이 집합을-1, 콘텐츠 필터링 한 SCL을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="83a6b-129">**Bypass spam filtering** - This sets the SCL to -1, which means that content filtering won't be performed.</span></span> 
    
  - <span data-ttu-id="83a6b-130">**0-4** -다음이 값 중 하나로 SCL을 설정 하는 경우, 메시지에 전달 됩니다를 따라 추가 처리에 대 한 콘텐츠 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="83a6b-130">**0-4** - When you set the SCL to one of these values, the message will be passed along to the content filter for additional processing.</span></span> 
    
  - <span data-ttu-id="83a6b-p104">**5, 6** -이러한 값을 해당 콘텐츠 필터 정책에서 **스팸** 에 대해 지정 된 작업 중 하나에 SCL을 설정 하는 경우 적용 됩니다. 기본적으로 작업 받는 사람의 정크 메일 폴더로 메시지를 보낼 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83a6b-p104">**5, 6** - When you set the SCL to one of these values, the action specified for **Spam** in the applicable content filter policies will be applied. By default, the action is to send the message to the recipient's Junk Email folder.</span></span> 
    
  - <span data-ttu-id="83a6b-p105">**7-9** -이러한 값을 해당 콘텐츠 필터 정책에 **높은 정확도 스팸** 에 대해 지정 된 작업 중 하나에 SCL을 설정 하는 경우 적용 됩니다. 기본적으로 작업 받는 사람의 정크 메일 폴더로 메시지를 보낼 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83a6b-p105">**7-9** - When you set the SCL to one of these values, the action specified for **High confidence spam** in the applicable content filter policies will be applied. By default, the action is to send the message to the recipient's Junk Email folder.</span></span> 
    
    <span data-ttu-id="83a6b-p106">콘텐츠 필터 정책을 구성 하는 방법에 대 한 자세한 내용은 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)을 참조 하십시오. 서비스의 SCL 값에 대 한 자세한 내용은 [Spam confidence levels](spam-confidence-levels.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="83a6b-p106">For more information about configuring your content filter policies, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
7. <span data-ttu-id="83a6b-137">규칙에 대 한 추가 속성을 지정 하 고 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="83a6b-137">Specify additional properties for the rule, and choose **save**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="83a6b-138">추가 속성을 선택 하거나이 규칙에 대 한 지정 하는 방법에 대 한 자세한 내용은 [전송 규칙을 만들려면 EAC를 사용 하 여](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx#CreateEAC)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="83a6b-138">For more information about the additional properties you can select or specify for this rule, see [Use the EAC to create a transport rule](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx#CreateEAC).</span></span> 
  
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="83a6b-139">작동 여부는 어떻게 확인합니까?</span><span class="sxs-lookup"><span data-stu-id="83a6b-139">How do you know this worked?</span></span>

<span data-ttu-id="83a6b-p107">이 절차는 올바르게 작동 하는지 확인 하려면 조직 내부의 다른 사람에 게 전자 메일 메시지 보내기 및 메시지에서 수행 되는 작업이 예상 대로 인지 확인 합니다. 예: 지정 된 받는 사람의 받은 편지함에 게 보내야 **바이패스 스팸 필터링**, 다음 메시지는 **신뢰도 scl (스팸)를 설정** 하는 경우. 그러나, **9**및 해당 콘텐츠 필터 정책에 대 한 **높은 정확도 스팸** 동작에 **는 신뢰도 scl (스팸)를 설정** 하려는 경우 정크 메일 폴더로 메시지 이동, 다음 메시지 보낼지를 지정 된 받는 사람의 정크 메일 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="83a6b-p107">To verify that this procedure is working correctly, send an email message to someone inside your organization, and verify that the action performed on the message is as expected. For example, if you **set the spam confidence level (SCL)** to **Bypass spam filtering**, then the message should be sent to the specified recipient's inbox. However, if you **set the spam confidence level (SCL)** to **9**, and the **High confidence spam** action for your applicable content filter policies is to move the message to the Junk Email folder, then the message should be sent to the specified recipient's Junk Email folder.</span></span> 
  

