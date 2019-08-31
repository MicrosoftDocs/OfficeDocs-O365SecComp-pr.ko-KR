---
title: Exchange Online에서 최종 사용자 스팸 알림 구성
ms.author: tracyp
author: MSFTTracyp
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: bfc91c73-a955-40e1-a95f-ad466624339a
ms.collection:
- M365-security-compliance
description: 회사 전체의 기본 스팸 필터 정책 또는 도메인에 적용 되는 사용자 지정 스팸 필터 정책에 대 한 최종 사용자 스팸 알림을 구성할 수 있습니다.
ms.openlocfilehash: 00ce151ab355efb419d483a17aaeeb26dfc71c0d
ms.sourcegitcommit: 769b506c828c475c713dbb337e115714dcc7f17c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/31/2019
ms.locfileid: "36699283"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a><span data-ttu-id="3a7e2-103">Exchange Online에서 최종 사용자 스팸 알림 구성</span><span class="sxs-lookup"><span data-stu-id="3a7e2-103">Configure end-user spam notifications in Exchange Online</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a7e2-104">이 항목은 클라우드 호스트 사서함을 보호 하는 Exchange Online 고객을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-104">This topic is for Exchange Online customers who are protecting cloud-hosted mailboxes.</span></span> <span data-ttu-id="3a7e2-105">EOP (Exchange Online Protection) 온-프레미스 사서함을 보호 하는 독립 실행형 고객은 [EOP에서 최종 사용자 스팸 알림 구성](configure-end-user-spam-notifications-in-eop.md)항목을 대신 읽어 보십시오.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-105">Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes should read the following topic instead: [Configure end-user spam notifications in EOP](configure-end-user-spam-notifications-in-eop.md).</span></span> 
  
<span data-ttu-id="3a7e2-106">회사 전체의 기본 스팸 필터 정책 또는 도메인에 적용 되는 사용자 지정 스팸 필터 정책에 대 한 최종 사용자 스팸 알림을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-106">You can configure end-user spam notifications for the default company-wide spam filter policy or for custom spam filter policies that are applied to domains.</span></span> <span data-ttu-id="3a7e2-107">최종 사용자 스팸 알림 메시지를 사용하도록 설정하면 최종 사용자가 스팸으로 격리된 메시지를 자체 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-107">Enabling end-user spam notification messages lets your end users self-manage their own spam-quarantined messages.</span></span> <span data-ttu-id="3a7e2-108">예외를 포함하여 사용자나 그룹 또는 정책에 적용된 정책과 함께 최종 사용자 스팸 알림을 사용할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-108">End-user spam notifications cannot be used with policies applied to users or groups, or to a policy with exceptions.</span></span>
  
<span data-ttu-id="3a7e2-p103">최종 사용자 스팸 알림에는 사용자가 구성한 기간(1일부터 15일 사이의 값을 지정할 수 있음)에 최종 사용자가 받은, 스팸으로 격리된 모든 메시지의 목록이 포함됩니다. 알림 메시지를 작성하는 언어도 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="3a7e2-111">최종 사용자는 알림 메시지를 받은 후 다음 옵션 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-111">After receiving a notification message, end users can choose from the following options:</span></span>

<span data-ttu-id="3a7e2-112">작업을 수행 하기 전에 콘텐츠나 머리글을 미리 보려면 메시지를 **미리 봅니다** .</span><span class="sxs-lookup"><span data-stu-id="3a7e2-112">**Preview** the message if you would like to preview the content or header prior to taking action.</span></span>

<span data-ttu-id="3a7e2-113">작업을 수행 하기 전에 장치에서 메시지와 첨부 파일 (있는 경우)을 검토 하려는 경우 메시지를 **다운로드** 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-113">**Download** the message if you would like to review the message and attachments (if any) on your device prior to taking action.</span></span>

<span data-ttu-id="3a7e2-114">메시지가 스팸으로 아니면 Office 365에서 사서함으로 메시지를 보내도록 하려면 **릴리스** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-114">**Release** if the message isn’t spam and you want Office 365 to send the message to your mailbox.</span></span>

<span data-ttu-id="3a7e2-115">**Release &** 메시지가 스팸으로 아니면 Office 365에서 다음 전자 메일에 대 한 수신 허용-보낸 사람 및 받는 사람 목록에 보낸 사람을 추가 하려는 경우 보낸 사람에 게 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-115">**Release & Allow Sender** if the message isn’t spam and you want Office 365 to add the sender to your safe senders and recipients list for future emails.</span></span> <span data-ttu-id="3a7e2-116">관리자에 게는 수신 허용-보낸 사람 목록을 다시 정의 하는 다른 조직 전체의 allow/block 구성이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-116">Keep in mind that your admin may have other organization wide allow/block configurations that override your safe sender list.</span></span>

<span data-ttu-id="3a7e2-117">**Release & Report**-메시지가 스팸으로가 아니며 메시지를 사서함으로 보내고 분석을 위해 Microsoft에 보고 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="3a7e2-117">**Release & Report**, if the message isn’t spam and you want to send the message to your mailbox and report it to Microsoft for analysis.</span></span>

<span data-ttu-id="3a7e2-118">Office 365에서 수신 거부 목록에 보낸 사람을 추가 하도록 하려면 **차단** 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-118">**Block** if you want Office 365 to add the sender to your blocked senders list.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="3a7e2-119">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="3a7e2-119">What do you need to know before you begin?</span></span>

<span data-ttu-id="3a7e2-120">예상 완료 시간: 2분</span><span class="sxs-lookup"><span data-stu-id="3a7e2-120">Estimated time to complete: 2 minutes</span></span>
  
<span data-ttu-id="3a7e2-121">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-121">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="3a7e2-122">필요한 사용 권한을 확인 하려면 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 항목에서 "스팸 방지" 항목을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-122">To see what permissions you need, see the "Anti-spam" entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
  
<span data-ttu-id="3a7e2-123">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대 한 자세한 내용은 [Exchange Online에서 exchange 관리 센터에 대 한 바로 가기 키](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-123">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="3a7e2-124">EAC를 통해 최종 사용자 스팸 알림 구성</span><span class="sxs-lookup"><span data-stu-id="3a7e2-124">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="3a7e2-125">EAC (Exchange 관리 센터)에서 **보호** \> **스팸 필터로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-125">In the Exchange admin center (EAC), navigate to **Protection** \> **Spam filter**.</span></span>
    
2. <span data-ttu-id="3a7e2-126">최종 사용자 스팸 알림을 사용 하도록 설정 하려는 스팸 필터 정책을 선택 합니다 (기본적으로 사용 하지 않도록 설정 됨).</span><span class="sxs-lookup"><span data-stu-id="3a7e2-126">Select the spam filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="3a7e2-127">정책 요약 정보가 표시되는 오른쪽 창에서 **최종 사용자 스팸 알림 구성** 링크를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-127">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="3a7e2-128">이후 표시되는 대화 상자에서 다음 옵션을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-128">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="3a7e2-p106">**최종 사용자 스팸 알림 사용** 해당 정책에 대한 최종 사용자 스팸 알림을 사용하도록 설정하려면 이 확인란을 선택합니다. 그러나 반대로 해당 정책이 사용하도록 설정되어 있으면 이 확인란을 선택 취소하여 해당 정책에 대한 최종 사용자 스팸 알림을 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-p106">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="3a7e2-p107">**최종 사용자 스팸 알림을 매번(매일) 전송** 최종 사용자 스팸 알림의 전송 빈도를 지정합니다. 기본값은 3일입니다. 1일부터 15일 사이의 값을 지정할 수 있습니다. 예를 들어 7일을 지정하면 스팸 격리 사서함으로 전송되는 대신 지난 7일 이내에 해당 사용자에게 보내려고 했던 모든 메시지의 목록이 알림에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-p107">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="3a7e2-135">**알림 언어** 드롭다운 목록을 사용하여 이 정책의 최종 사용자 스팸 알림에 작성할 언어를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-135">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="3a7e2-136">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-136">Click **save**.</span></span> <span data-ttu-id="3a7e2-137">최종 사용자 스팸 알림 설정을 비롯 한 스팸 필터 정책 설정에 대 한 요약이 오른쪽 창에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-137">A summary of your spam filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="3a7e2-138">최종 사용자 스팸 알림은 사용 하도록 설정 된 스팸 필터 정책에 대해서만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-138">End-user spam notifications will only be functional for spam filter policies that are enabled.</span></span> <span data-ttu-id="3a7e2-139">>  최종 사용자 스팸 알림은 하루에 한 번만 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-139">>  End-user spam notifications are only sent once per day.</span></span> <span data-ttu-id="3a7e2-140">특정 고객에 대한 알림 배달 시간을 보장하거나 구성할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-140">The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="3a7e2-141">**팁:** 최종 사용자 스팸 알림을 완전히 구현 하기 전에 제한 된 사용자 집합에 전송 하 여 테스트 하려면 사용자가 거주 하는 도메인에 대 한 최종 사용자 스팸 알림을 사용 하도록 설정 하는 사용자 지정 스팸 필터 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-141">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom spam filter policy that enables end-user spam notifications for the domains in which the users reside.</span></span> <span data-ttu-id="3a7e2-142">그런 다음 EAC의 **메일 흐름 \> 규칙**에서 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들어 quarantine@messaging.microsoft.com (알림 메시지를 보내는 전자 메일 주소)에서 원하는 사용자에 대 한 예외를 차단 합니다. 알림을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-142">Then, in the EAC, under **Mail flow \> rules**, create a mail flow rule (also known as a transport rule) to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications.</span></span> <span data-ttu-id="3a7e2-143">다음 그림은 Contoso.com 도메인의 두 사용자(SaraD 및 AlexD)에 대한 예외를 만드는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="3a7e2-143">The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![최종 사용자 스팸 알림을 테스트할 전송 규칙](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="3a7e2-145">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="3a7e2-145">For more information</span></span>

[<span data-ttu-id="3a7e2-146">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="3a7e2-146">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
