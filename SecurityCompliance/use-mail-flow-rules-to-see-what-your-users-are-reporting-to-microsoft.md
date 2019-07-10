---
title: 메일 흐름 규칙을 사용하여 사용자가 Microsoft에 보고한 내용 확인
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
ms.collection:
- M365-security-compliance
description: 사용자가 분석을 위해 Microsoft에 전자 메일 메시지를 보내지 못하도록 하 고 자체 보안 프로세스에서 사용 하는 것을 방지 하는 Exchange 메일 흐름 규칙을 만들 수 있습니다.
ms.openlocfilehash: 7308de8e3f23a7c210d4d8a4e6ec5e322d40055f
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600434"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a><span data-ttu-id="37d92-103">메일 흐름 규칙을 사용하여 사용자가 Microsoft에 보고한 내용 확인</span><span class="sxs-lookup"><span data-stu-id="37d92-103">Use mail flow rules to see what your users are reporting to Microsoft</span></span>

<span data-ttu-id="37d92-104">여러 가지 방법으로 오판정 및 거짓 부정 메시지를 분석용으로 Microsoft에 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-104">There are multiple ways you can send false positive and false negative messages to Microsoft for analysis.</span></span> <span data-ttu-id="37d92-105">관리자는 메일 흐름 규칙을 사용 하 여 사용자가 Microsoft에 스팸, 비 스팸 및 피싱 사기를 보고 하는 항목을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-105">As an administrator, you can use mail flow rules to see what your users are reporting to Microsoft as spam, non-spam, and phishing scams.</span></span> <span data-ttu-id="37d92-106">자세한 내용은 [분석을 위해 Microsoft에 스팸 및 스팸이 아닌 메시지 제출을](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="37d92-106">For more information, see [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span></span> <span data-ttu-id="37d92-107">반대로 Exchange 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들어 사용자가 분석을 위해 Microsoft에 전자 메일 메시지를 보내지 못하도록 하 고 자체 보안 프로세스에서 사용 하는 것을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-107">Conversely, you can create an Exchange mail flow rule (also known as a transport rule) to prevent your users from sending email messages to Microsoft for analysis and use them in your own security processes.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="37d92-108">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="37d92-108">What do you need to know before you begin?</span></span>

<span data-ttu-id="37d92-109">예상 완료 시간: 5분</span><span class="sxs-lookup"><span data-stu-id="37d92-109">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="37d92-110">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-110">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="37d92-111">필요한 사용 권한을 확인 하려면 [클라이언트 및 모바일 장치 사용 권한](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) 항목의 [메시징 정책 및 준수 권한](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) 항목과 "웹 사서함 정책의 Outlook" 항목의 "메일 흐름 규칙" 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="37d92-111">To see what permissions you need, see the "Mail flow rules" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic and the "Outlook on the web mailbox policies" entry in the [Clients and mobile devices permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) topic.</span></span> 
  
<span data-ttu-id="37d92-112">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Exchange 관리 센터의 바로 가기 키**을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="37d92-112">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a><span data-ttu-id="37d92-113">EAC를 사용 하 여 메일 흐름 규칙을 만들어 사용자의 수동 정크, 피싱 및 정크가 아닌 보고서를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-113">Use the EAC to create a mail flow rule to view users' manual junk, phishing, and not junk reports</span></span>

1. <span data-ttu-id="37d92-114">EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-114">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="37d92-115">![아이콘 추가](media/ITPro-EAC-AddIcon.gif)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-115">Click ![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="37d92-116">규칙 이름을 지정하고 **기타 옵션**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-116">Give the rule a name and then click **More options**.</span></span>
    
4. <span data-ttu-id="37d92-117">**다음의 경우 이 규칙 적용**에서 **받는 사람**을 선택하고 **주소에 다음 단어 포함**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-117">Under **Apply this rule if**, select **The recipient** and then choose **address includes any of these words**.</span></span>
    
5. <span data-ttu-id="37d92-118">**단어 또는 구 지정** 상자에 다음을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-118">In the **specify words or phrases** box, do the following:</span></span> 
    - <span data-ttu-id="37d92-119">를 `abuse@messaging.microsoft.com` 입력 하 고 ![아이콘](media/ITPro-EAC-AddIcon.gif)추가를 클릭 한 다음 `junk@office365.microsoft.com` 아이콘](media/ITPro-EAC-AddIcon.gif)추가를 ![클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-119">Type `abuse@messaging.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif), and then type `junk@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span> <span data-ttu-id="37d92-120">이러한 전자 메일 주소는 Microsoft에 거짓 부정 메시지를 전송하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-120">These email addresses are used to submit false negative messages to Microsoft.</span></span>
    - <span data-ttu-id="37d92-121">를 `phish@office365.microsoft.com` 입력 하 고 ![아이콘](media/ITPro-EAC-AddIcon.gif)추가를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-121">Type `phish@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span> <span data-ttu-id="37d92-122">이 전자 메일 주소는 부재 중 피싱 메시지를 Microsoft에 제출 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-122">This email address is used to submit missed phishing messages to Microsoft.</span></span>
    - <span data-ttu-id="37d92-123">를 `false_positive@messaging.microsoft.com` 입력 하 고 ![아이콘](media/ITPro-EAC-AddIcon.gif)추가를 클릭 한 다음 `not_junk@office365.microsoft.com` 아이콘](media/ITPro-EAC-AddIcon.gif)추가를 ![클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-123">Type `false_positive@messaging.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif), and then type `not_junk@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span> <span data-ttu-id="37d92-124">이러한 전자 메일 주소는 Microsoft에 오판정 메시지를 전송하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-124">These email addresses are used to submit false positive messages to Microsoft.</span></span>
    - <span data-ttu-id="37d92-125">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-125">Click **ok**.</span></span>
    
6. <span data-ttu-id="37d92-126">**다음 작업 실행**에서 **메시지를 받는 사람** ...을 선택한 후 메시지를 받을 사서함을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-126">Under **Do the following**, select **Bcc the message to...** and then and then select the mailboxes where you'd like to receive the messages.</span></span> 
    
7. <span data-ttu-id="37d92-127">원하는 경우 규칙을 감사하고 규칙을 테스트하며 특정 기간 동안 규칙을 활성화하는 등 기타 옵션을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-127">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections.</span></span> <span data-ttu-id="37d92-128">옵션을 적용하기 전에 규칙을 테스트하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-128">We recommend testing the rule for a period before you enforce it.</span></span> <span data-ttu-id="37d92-129">[메일 흐름 규칙에 대 한 절차를](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="37d92-129">See [Procedures for mail flow rules](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures).</span></span> 
    
8. <span data-ttu-id="37d92-130">**저장** 단추를 클릭하여 규칙을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-130">Click the **save** button to save the rule.</span></span> <span data-ttu-id="37d92-131">규칙이 규칙 목록에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-131">It appears in your list of rules.</span></span> 
    
<span data-ttu-id="37d92-132">규칙을 만들어 적용 하 고 나면 조직에서 지정 된 전자 메일 주소로 보내는 모든 메시지가 지정 된 사서함에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37d92-132">After you create and enforce the rule, any messages that are sent from your organization to specified email addresses will be copied to the specified mailbox.</span></span>
  

