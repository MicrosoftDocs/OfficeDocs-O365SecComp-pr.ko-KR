---
title: 스팸이 각 사용자의 정크 메일 폴더로 라우팅되는지 확인
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/16/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
description: EOP 고객을 위한 기본 스팸 방지 작업은 스팸 메시지를 받는 사람의 정크 메일 폴더로 이동 합니다. 온-프레미스 사서함을 사용 하도록이 작업에 대 한 순서로 EOP에서 추가 된 스팸 헤더를 감지 하 여 온-프레미스 Edge 또는 Hub 서버에서 Exchange 전송 규칙을 구성 해야 합니다. 이러한 전송 규칙은 신뢰도 scl (스팸) 스팸 각 사서함의 정크 메일 폴더로 이동 하는 Set-organizationconfig cmdlet의 합니다 속성에서 사용을 설정 합니다.
ms.openlocfilehash: 290a3cc6aed07cd4d91df65350fd49c9226a0d64
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026635"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a><span data-ttu-id="f86c5-105">스팸이 각 사용자의 정크 메일 폴더로 라우팅되는지 확인</span><span class="sxs-lookup"><span data-stu-id="f86c5-105">Ensure that spam is routed to each user's Junk Email folder</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f86c5-p102">이 항목은 온-프레미스 사서함 하이브리드 배포에서 호스트 하는 Exchange Online Protection (EOP) 고객에만 적용 됩니다. 사서함이 있는 Office 365에서 완벽 하 게 호스팅되는 Exchange Online 고객 이러한 명령을 실행할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f86c5-p102">This topic only applies to Exchange Online Protection (EOP) customers who host mailboxes on-premises in a hybrid deployment. Exchange Online customers whose mailboxes are fully-hosted in Office 365 do not need to run these commands.</span></span> 
  
<span data-ttu-id="f86c5-p103">EOP 고객을 위한 기본 스팸 방지 작업은 스팸 메시지를 받는 사람의 정크 메일 폴더로 이동 합니다. 온-프레미스 사서함을 사용 하도록이 작업에 대 한 순서로 EOP에서 추가 된 스팸 헤더를 감지 하 여 온-프레미스 Edge 또는 Hub 서버에서 Exchange 전송 규칙을 구성 해야 합니다. 이러한 전송 규칙은 신뢰도 scl (스팸) 스팸 각 사서함의 정크 메일 폴더로 이동 하는 Set-organizationconfig cmdlet의 합니다 속성에서 사용을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f86c5-p103">The default anti-spam action for EOP customers is to move spam messages to the recipients' Junk Email folder. In order for this action to work with on-premises mailboxes, you must configure Exchange Transport rules on your on-premises Edge or Hub servers to detect spam headers added by EOP. These Transport rules set the spam confidence level (SCL) used by the SclJunkThreshold property of the Set-OrganizationConfig cmdlet to move spam into the Junk Email folder of each mailbox.</span></span> 
  
### <a name="to-add-transport-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a><span data-ttu-id="f86c5-111">전송을 추가 하려면 규칙을 사용 스팸 이동 정크 메일 폴더로 Windows PowerShell을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="f86c5-111">To add transport rules to ensure spam is moved to the Junk Email folder by using Windows PowerShell</span></span>

1. <span data-ttu-id="f86c5-p104">온-프레미스 Exchange 서버에 대 한 Exchange 관리 셸 액세스할 수 있습니다. 온-프레미스 Exchange 조직에서 Exchange 관리 셸을 열려면 하는 방법을 알아보려면 **셸을 열**을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f86c5-p104">Access the Exchange Management Shell for your on-premises Exchange server. To learn how to open the Exchange Management Shell in your on-premises Exchange organization, see **Open the Shell**.</span></span>
    
2. <span data-ttu-id="f86c5-114">다음 명령을 실행하여 콘텐츠가 필터링된 스팸 메시지를 정크 메일 폴더로 라우팅합니다.</span><span class="sxs-lookup"><span data-stu-id="f86c5-114">Run the following command to route content-filtered spam messages to the Junk Email folder:</span></span>
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
  ```

    <span data-ttu-id="f86c5-115">여기서 _NameForRule_ 는 JunkContentFilteredMail 등 새 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f86c5-115">Where  _NameForRule_ is the name for the new rule, for example, JunkContentFilteredMail.</span></span> 
    
3. <span data-ttu-id="f86c5-116">다음 명령을 실행하여 스팸으로 표시된 메시지를 콘텐츠 필터에 도달하기 전에 정크 메일 폴더로 라우팅합니다.</span><span class="sxs-lookup"><span data-stu-id="f86c5-116">Run the following command to route messages marked as spam prior to reaching the content filter to the Junk Email folder:</span></span>
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
  ```

    <span data-ttu-id="f86c5-117">여기서 _NameForRule_ 는 JunkMailBeforeReachingContentFilter 등 새 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f86c5-117">Where  _NameForRule_ is the name for the new rule, for example, JunkMailBeforeReachingContentFilter.</span></span> 
    
4. <span data-ttu-id="f86c5-118">스팸 필터 정책 **보낸 사람이 차단** 목록 등의 차단 목록에 있는 사람이 보낸 메시지는 정크 메일 폴더로 라우팅되는지 확인 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f86c5-118">Run the following command to ensure that messages from senders in a block list in the spam filter policy, such as the **Sender block** list, are routed to the Junk Email folder:</span></span> 
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
  ```

    <span data-ttu-id="f86c5-119">여기서 _NameForRule_ 는 JunkMailInSenderBlockList 등 새 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f86c5-119">Where  _NameForRule_ is the name for the new rule, for example, JunkMailInSenderBlockList.</span></span> 
    
<span data-ttu-id="f86c5-p105">**정크 메일 폴더로 메시지 이동** 작업을 사용 하지 않을 경우에 Exchange 관리 센터에서 콘텐츠 필터 정책에 다른 작업을 선택할 수 있습니다. 자세한 내용은 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)을 참조 하십시오. 메시지 헤더에 이러한 필드에 대 한 자세한 내용은 [스팸 방지 메시지 헤더](anti-spam-message-headers.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f86c5-p105">If you do not want to use the **Move message to Junk Email folder** action, you can choose another action in your content filter policies in the Exchange admin center. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). For more information about these fields in the message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f86c5-123">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f86c5-123">See also</span></span>

[<span data-ttu-id="f86c5-124">New-transportrule cmdlet</span><span class="sxs-lookup"><span data-stu-id="f86c5-124">New-TransportRule cmdlet</span></span>](https://technet.microsoft.com/library/bb125138%28v=exchg.160%29.aspx)

