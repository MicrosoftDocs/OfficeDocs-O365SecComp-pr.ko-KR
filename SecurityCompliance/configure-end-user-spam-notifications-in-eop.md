---
title: EOP에서 최종 사용자 스팸 알림 구성
ms.author: tracyp
author: MSFTTracyp
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: e9947db5-1dd1-4493-872d-7362b24c7ba0
ms.collection:
- M365-security-compliance
description: 도메인에 적용되는 사용자 지정 콘텐츠 필터 정책 또는 기본 회사 차원의 콘텐츠 필터 정책에 대해 최종 사용자 스팸 알림을 구성할 수 있습니다.
ms.openlocfilehash: 761f8660dc19f2626ecb5331370f87e0f4c3963a
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600204"
---
# <a name="configure-end-user-spam-notifications-in-eop"></a><span data-ttu-id="e86c2-103">EOP에서 최종 사용자 스팸 알림 구성</span><span class="sxs-lookup"><span data-stu-id="e86c2-103">Configure end-user spam notifications in EOP</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e86c2-104">이 항목은 온-프레미스 사서함을 보호 하는 EOP (Exchange Online Protection) 독립 실행형 고객을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-104">This topic is for Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes.</span></span> <span data-ttu-id="e86c2-105">클라우드 호스트 사서함을 보호 하는 exchange Online 고객은 다음 항목을 대신 사용 하 여 [Exchange online에서 최종 사용자 스팸 알림을 구성](configure-end-user-spam-notifications-in-exchange-online.md)해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-105">Exchange Online customers who are protecting cloud-hosted mailboxes should read the following topic instead: [Configure end-user spam notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md).</span></span> 
  
<span data-ttu-id="e86c2-p102">도메인에 적용되는 사용자 지정 콘텐츠 필터 정책 또는 기본 회사 차원의 콘텐츠 필터 정책에 대해 최종 사용자 스팸 알림을 구성할 수 있습니다. 최종 사용자 스팸 알림 메시지를 사용하도록 설정하면 최종 사용자가 스팸으로 격리된 메시지를 자체 관리할 수 있습니다. 예외를 포함하여 사용자나 그룹 또는 정책에 적용된 정책과 함께 최종 사용자 스팸 알림을 사용할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-p102">You can configure end-user spam notifications for the default company-wide content filter policy or for custom content filter policies that are applied to domains. Enabling end-user spam notification messages lets your end users self-manage their own spam-quarantined messages. End-user spam notifications cannot be used with policies applied to users or groups, or to a policy with exceptions.</span></span>
  
<span data-ttu-id="e86c2-p103">최종 사용자 스팸 알림에는 사용자가 구성한 기간(1일부터 15일 사이의 값을 지정할 수 있음)에 최종 사용자가 받은, 스팸으로 격리된 모든 메시지의 목록이 포함됩니다. 알림 메시지를 작성하는 언어도 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="e86c2-111">최종 사용자는 알림 메시지를 받은 후 다음 옵션 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-111">After receiving a notification message, end users can choose from the following options:</span></span>

<span data-ttu-id="e86c2-112">작업을 수행 하기 전에 콘텐츠나 머리글을 미리 보려면 메시지를 **미리 봅니다** .</span><span class="sxs-lookup"><span data-stu-id="e86c2-112">**Preview** the message if you would like to preview the content or header prior to taking action.</span></span>

<span data-ttu-id="e86c2-113">작업을 수행 하기 전에 장치에서 메시지와 첨부 파일 (있는 경우)을 검토 하려는 경우 메시지를 **다운로드** 합니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-113">**Download** the message if you would like to review the message and attachments (if any) on your device prior to taking action.</span></span>

<span data-ttu-id="e86c2-114">메시지가 스팸으로 아니면 Office 365에서 사서함으로 메시지를 보내도록 하려면 **릴리스** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-114">**Release** if the message isn’t spam and you want Office 365 to send the message to your mailbox.</span></span>

<span data-ttu-id="e86c2-115">**Release &** 메시지가 스팸으로 아니면 Office 365에서 다음 전자 메일에 대 한 수신 허용-보낸 사람 및 받는 사람 목록에 보낸 사람을 추가 하려는 경우 보낸 사람에 게 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-115">**Release & Allow Sender** if the message isn’t spam and you want Office 365 to add the sender to your safe senders and recipients list for future emails.</span></span> <span data-ttu-id="e86c2-116">관리자에 게는 수신 허용-보낸 사람 목록을 다시 정의 하는 다른 조직 전체의 allow/block 구성이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-116">Keep in mind that your admin may have other organization wide allow/block configurations that override your safe sender list.</span></span>

<span data-ttu-id="e86c2-117">**Release & Report**-메시지가 스팸으로가 아니며 메시지를 사서함으로 보내고 분석을 위해 Microsoft에 보고 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="e86c2-117">**Release & Report**, if the message isn’t spam and you want to send the message to your mailbox and report it to Microsoft for analysis.</span></span>

<span data-ttu-id="e86c2-118">Office 365에서 수신 거부 목록에 보낸 사람을 추가 하도록 하려면 **차단** 합니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-118">**Block** if you want Office 365 to add the sender to your blocked senders list.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="e86c2-119">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="e86c2-119">What do you need to know before you begin?</span></span>
<span data-ttu-id="e86c2-120"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="e86c2-120"></span></span>

<span data-ttu-id="e86c2-121">예상 완료 시간: 5분</span><span class="sxs-lookup"><span data-stu-id="e86c2-121">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="e86c2-p105">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인하려면 다음을 참조하세요. [EOP의 기능 사용 권한](eop/feature-permissions-in-eop.md)의 "스팸 방지" 항목</span><span class="sxs-lookup"><span data-stu-id="e86c2-p105">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature permissions in EOP](eop/feature-permissions-in-eop.md) topic.</span></span> 
  
<span data-ttu-id="e86c2-124">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Keyboard shortcuts in Exchange 2013**을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e86c2-124">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="e86c2-125">EAC를 통해 최종 사용자 스팸 알림 구성</span><span class="sxs-lookup"><span data-stu-id="e86c2-125">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="e86c2-126">EAC (Exchange 관리 센터)에서 **보호** > **스팸 필터로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-126">In the Exchange Admin Center (EAC), navigate to **Protection** > **Spam filter**.</span></span>
    
2. <span data-ttu-id="e86c2-127">최종 사용자 스팸 알림(기본적으로 사용하지 않도록 설정됨)을 사용하도록 설정할 콘텐츠 필터 정책을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-127">Select the content filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="e86c2-128">정책 요약 정보가 표시되는 오른쪽 창에서 **최종 사용자 스팸 알림 구성** 링크를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-128">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="e86c2-129">이후 표시되는 대화 상자에서 다음 옵션을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-129">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="e86c2-p106">**최종 사용자 스팸 알림 사용** 해당 정책에 대한 최종 사용자 스팸 알림을 사용하도록 설정하려면 이 확인란을 선택합니다. 그러나 반대로 해당 정책이 사용하도록 설정되어 있으면 이 확인란을 선택 취소하여 해당 정책에 대한 최종 사용자 스팸 알림을 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-p106">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="e86c2-p107">**최종 사용자 스팸 알림을 매번(매일) 전송** 최종 사용자 스팸 알림의 전송 빈도를 지정합니다. 기본값은 3일입니다. 1일부터 15일 사이의 값을 지정할 수 있습니다. 예를 들어 7일을 지정하면 스팸 격리 사서함으로 전송되는 대신 지난 7일 이내에 해당 사용자에게 보내려고 했던 모든 메시지의 목록이 알림에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-p107">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="e86c2-136">**알림 언어** 드롭다운 목록을 사용하여 이 정책의 최종 사용자 스팸 알림에 작성할 언어를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-136">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="e86c2-p108">**저장**을 클릭합니다. 최종 사용자 스팸 알림 설정을 비롯한 콘텐츠 필터 정책 설정의 요약이 오른쪽 창에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-p108">Click **save**. A summary of your content filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="e86c2-p109">최종 사용자 스팸 알림은 사용하도록 설정된 콘텐츠 필터 정책에 대해서만 작동합니다. >  최종 사용자 스팸 알림은 하루에 한 번만 전송됩니다. 특정 고객에 대한 알림 배달 시간을 보장하거나 구성할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-p109">End-user spam notifications will only be functional for content filter policies that are enabled. >  End-user spam notifications are only sent once per day. The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="e86c2-142">**팁:** 최종 사용자 스팸 알림을 완전히 구현하기 전에 제한된 사용자 집합으로 보내 테스트하려면 해당 사용자가 속해 있는 도메인에 최종 사용자 스팸 알림을 사용하는 사용자 지정 콘텐츠 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-142">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom content filter policy that enables end-user spam notifications for the domains in which the users reside.</span></span> <span data-ttu-id="e86c2-143">그런 다음 EAC의 **메일 흐름 \> 규칙**에서 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들어 quarantine@messaging.microsoft.com (알림 메시지를 보내는 전자 메일 주소)에서 원하는 사용자에 대 한 예외를 차단 합니다. 알림을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-143">Then, in the EAC, under **Mail flow \> rules**, create a mail flow rule (also known as a transport rule) to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications.</span></span> <span data-ttu-id="e86c2-144">다음 그림은 Contoso.com 도메인의 두 사용자(SaraD 및 AlexD)에 대한 예외를 만드는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="e86c2-144">The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![최종 사용자 스팸 알림을 테스트할 전송 규칙](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="e86c2-146">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="e86c2-146">For more information</span></span>

[<span data-ttu-id="e86c2-147">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="e86c2-147">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
