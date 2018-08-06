---
title: Exchange Online에서 최종 사용자 스팸 알림 구성
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: bfc91c73-a955-40e1-a95f-ad466624339a
description: 기본 회사 차원의 스팸 필터 정책에 대 한 또는 도메인에 적용 되는 사용자 지정 스팸 필터 정책에 대 한 최종 사용자 스팸 알림을 구성할 수 있습니다.
ms.openlocfilehash: 4a4c7c6b139fe0f8b0a1f6b69c1b95e321293af5
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027535"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a><span data-ttu-id="b14a8-103">Exchange Online에서 최종 사용자 스팸 알림 구성</span><span class="sxs-lookup"><span data-stu-id="b14a8-103">Configure end-user spam notifications in Exchange Online</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b14a8-p101">이 항목은 클라우드 호스팅 사서함을 보호 하는 Exchange Online 고객입니다. Exchange Online Protection (EOP) 독립 실행형 고객에 게 온-프레미스 사서함을 보호 하는 대신 다음 항목을 읽어야 할: [EOP에서 최종 사용자 스팸 알림 구성](configure-end-user-spam-notifications-in-eop.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="b14a8-p101">This topic is for Exchange Online customers who are protecting cloud-hosted mailboxes. Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes should read the following topic instead: [Configure end-user spam notifications in EOP](configure-end-user-spam-notifications-in-eop.md).</span></span> 
  
<span data-ttu-id="b14a8-p102">기본 회사 차원의 스팸 필터 정책에 대 한 또는 도메인에 적용 되는 사용자 지정 스팸 필터 정책에 대 한 최종 사용자 스팸 알림을 구성할 수 있습니다. 최종 사용자 스팸 알림 메시지를 사용 하면 최종 사용자에 게 자신의 스팸 격리 된 메시지를 자체 관리할 수 있습니다. 최종 사용자 스팸 알림 예외 사항과 함께 정책 또는 사용자 또는 그룹에 적용 되는 정책을 사용 하 여 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b14a8-p102">You can configure end-user spam notifications for the default company-wide spam filter policy or for custom spam filter policies that are applied to domains. Enabling end-user spam notification messages lets your end users self-manage their own spam-quarantined messages. End-user spam notifications cannot be used with policies applied to users or groups, or to a policy with exceptions.</span></span>
  
<span data-ttu-id="b14a8-p103">최종 사용자 스팸 알림에는 사용자가 구성한 기간(1일부터 15일 사이의 값을 지정할 수 있음)에 최종 사용자가 받은, 스팸으로 격리된 모든 메시지의 목록이 포함됩니다. 알림 메시지를 작성하는 언어도 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b14a8-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="b14a8-111">알림 메시지를 받은 후 최종 사용자가 자신의 받은 편지함에 스팸 전자 메일을 이동 하려면 클릭 하거나, 스팸 전자 메일을 정크 메일 아님으로 경우에 해당 보고서를 Microsoft 스팸 분석 팀에 게 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b14a8-111">After receiving a notification message, end users can click to move the spam email to their inbox, or report the spam email as Not Junk, in which case it will be sent to the Microsoft Spam Analysis Team.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="b14a8-112">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="b14a8-112">What do you need to know before you begin?</span></span>

<span data-ttu-id="b14a8-113">예상 완료 시간: 2분</span><span class="sxs-lookup"><span data-stu-id="b14a8-113">Estimated time to complete: 2 minutes</span></span>
  
<span data-ttu-id="b14a8-p104">이 절차를 수행 하기 전에 사용 권한을 할당 해야 합니다. 필요한 사용 권한을 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 항목의 "스팸 방지" 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b14a8-p104">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
  
<span data-ttu-id="b14a8-116">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Keyboard shortcuts in Exchange 2013**을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b14a8-116">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="b14a8-117">EAC를 통해 최종 사용자 스팸 알림 구성</span><span class="sxs-lookup"><span data-stu-id="b14a8-117">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="b14a8-118">Exchange 관리 센터 (EAC)에서 **보호** 로 이동 \> **스팸 필터**입니다.</span><span class="sxs-lookup"><span data-stu-id="b14a8-118">In the Exchange admin center (EAC), navigate to **Protection** \> **Spam filter**.</span></span>
    
2. <span data-ttu-id="b14a8-119">최종 사용자 스팸 알림 (그리고 사용할 기본적으로)를 사용 하도록 설정 하려는 스팸 필터 정책을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b14a8-119">Select the spam filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="b14a8-120">정책 요약 정보가 표시되는 오른쪽 창에서 **최종 사용자 스팸 알림 구성** 링크를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b14a8-120">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="b14a8-121">이후 표시되는 대화 상자에서 다음 옵션을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b14a8-121">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="b14a8-p105">**최종 사용자 스팸 알림 사용** 해당 정책에 대한 최종 사용자 스팸 알림을 사용하도록 설정하려면 이 확인란을 선택합니다. 그러나 반대로 해당 정책이 사용하도록 설정되어 있으면 이 확인란을 선택 취소하여 해당 정책에 대한 최종 사용자 스팸 알림을 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b14a8-p105">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="b14a8-p106">**최종 사용자 스팸 알림을 매번(매일) 전송** 최종 사용자 스팸 알림의 전송 빈도를 지정합니다. 기본값은 3일입니다. 1일부터 15일 사이의 값을 지정할 수 있습니다. 예를 들어 7일을 지정하면 스팸 격리 사서함으로 전송되는 대신 지난 7일 이내에 해당 사용자에게 보내려고 했던 모든 메시지의 목록이 알림에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="b14a8-p106">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="b14a8-128">**알림 언어** 드롭다운 목록을 사용하여 이 정책의 최종 사용자 스팸 알림에 작성할 언어를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b14a8-128">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="b14a8-p107">**저장**을 클릭 합니다. 오른쪽 창에서 최종 사용자 스팸 알림 설정을 포함 하 여 스팸 필터 정책 설정의 요약을 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b14a8-p107">Click **save**. A summary of your spam filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="b14a8-p108">최종 사용자 스팸 알림을 사용 하도록 설정 된 스팸 필터 정책에 대 한 기능 수만 있습니다. > 최종 사용자 스팸 알림 하루에 한번만 전송 됩니다. 알림 메시지의 배달 시간 특정 고객에 대 한을 보장할 수 없는 하 고 구성할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b14a8-p108">End-user spam notifications will only be functional for spam filter policies that are enabled. >  End-user spam notifications are only sent once per day. The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="b14a8-p109">**팁:** 완벽 하 게 구현 하기 전에 사용자의 제한 된 집합을 전송 하 여 최종 사용자 스팸 알림을 테스트 하려는 경우에 사용자가 거주 하는 도메인에 대 한 최종 사용자 스팸 알림을 사용 하도록 설정 하는 사용자 지정 스팸 필터 정책을 만듭니다. EAC에서 다음 아래에서 **메일 흐름 \> 규칙**, 알림의 받을 하려는 사용자에 대 한 예외를 제외 quarantine@messaging.microsoft.com (알림을 보내는 전자 메일 주소)에서 메시지를 차단 하려면 전송 규칙을 만듭니다. 다음 그림은 Contoso.com 도메인에서 두 명의 사용자가 (SaraD 및 AlexD)에 대 한 예외를 만드는 예:</span><span class="sxs-lookup"><span data-stu-id="b14a8-p109">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom spam filter policy that enables end-user spam notifications for the domains in which the users reside. Then, in the EAC, under **Mail flow \> rules**, create a transport rule to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications. The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![최종 사용자 스팸 알림을 테스트할 전송 규칙](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="b14a8-138">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="b14a8-138">For more information</span></span>

[<span data-ttu-id="b14a8-139">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="b14a8-139">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
