---
title: 스팸이 각 사용자의 정크 메일 폴더로 라우팅되는지 확인
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 7/16/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
ms.collection:
- M365-security-compliance
description: 관리자는 Exchange Online Protection에서 스팸을 사용자 정크 메일 폴더로 라우팅하는 방법을 알 수 있습니다.
ms.openlocfilehash: dc37f2428e009f00a2d6d9dd15d5d2cd505f267a
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599854"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a><span data-ttu-id="bd368-103">스팸이 각 사용자의 정크 메일 폴더로 라우팅되는지 확인</span><span class="sxs-lookup"><span data-stu-id="bd368-103">Ensure that spam is routed to each user's Junk Email folder</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd368-104">이 항목은 하이브리드 배포에서 온-프레미스에 사서함을 호스트 하는 EOP (Exchange Online Protection) 고객 에게만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd368-104">This topic only applies to Exchange Online Protection (EOP) customers who host mailboxes on-premises in a hybrid deployment.</span></span> <span data-ttu-id="bd368-105">해당 사서함이 Office 365에서 완전히 호스트 되는 Exchange Online 고객은 이러한 명령을 실행할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bd368-105">Exchange Online customers whose mailboxes are fully-hosted in Office 365 do not need to run these commands.</span></span> 
  
<span data-ttu-id="bd368-106">EOP 고객의 기본 스팸 방지 작업은 스팸 메시지를 받는 사람의 정크 메일 폴더로 이동하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="bd368-106">The default anti-spam action for EOP customers is to move spam messages to the recipients' Junk Email folder.</span></span> <span data-ttu-id="bd368-107">이 작업을 온-프레미스 사서함에서 작동 하려면 온-프레미스에 지 또는 허브 서버에서 Exchange 메일 흐름 규칙 (전송 규칙이 라고도 함)을 구성 하 여 EOP에서 추가한 스팸 헤더를 검색 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd368-107">In order for this action to work with on-premises mailboxes, you must configure Exchange mail flow rules (also known as transport rules) on your on-premises Edge or Hub servers to detect spam headers added by EOP.</span></span> <span data-ttu-id="bd368-108">이러한 메일 흐름 규칙은 스팸을 각 사서함의 정크 메일 폴더로 이동 하도록 Set-organizationconfig cmdlet의 SclJunkThreshold 속성에서 사용 하는 SCL (스팸 지 수)을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd368-108">These mail flow rules set the spam confidence level (SCL) used by the SclJunkThreshold property of the Set-OrganizationConfig cmdlet to move spam into the Junk Email folder of each mailbox.</span></span> 
  
### <a name="to-add-mail-flow-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a><span data-ttu-id="bd368-109">Windows PowerShell을 사용 하 여 스팸이 정크 메일 폴더로 이동 되도록 메일 흐름 규칙을 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="bd368-109">To add mail flow rules to ensure spam is moved to the Junk Email folder by using Windows PowerShell</span></span>

1. <span data-ttu-id="bd368-110">온-프레미스 Exchange 서버의 Exchange 관리 셸에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="bd368-110">Access the Exchange Management Shell for your on-premises Exchange server.</span></span> <span data-ttu-id="bd368-111">온-프레미스 Exchange 조직에서 Exchange 관리 셸을 여는 방법을 확인하려면 organization, see **Open the Shell** 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bd368-111">To learn how to open the Exchange Management Shell in your on-premises Exchange organization, see **Open the Shell**.</span></span>
    
2. <span data-ttu-id="bd368-112">다음 명령을 실행하여 콘텐츠가 필터링된 스팸 메시지를 정크 메일 폴더로 라우팅합니다.</span><span class="sxs-lookup"><span data-stu-id="bd368-112">Run the following command to route content-filtered spam messages to the Junk Email folder:</span></span>
    
  ```Powershell
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
  ```

    <span data-ttu-id="bd368-113">여기서 _Nameforrule_ 은 새 규칙의 이름 (예: JunkContentFilteredMail)입니다.</span><span class="sxs-lookup"><span data-stu-id="bd368-113">Where  _NameForRule_ is the name for the new rule, for example, JunkContentFilteredMail.</span></span> 
    
3. <span data-ttu-id="bd368-114">다음 명령을 실행하여 스팸으로 표시된 메시지를 콘텐츠 필터에 도달하기 전에 정크 메일 폴더로 라우팅합니다.</span><span class="sxs-lookup"><span data-stu-id="bd368-114">Run the following command to route messages marked as spam prior to reaching the content filter to the Junk Email folder:</span></span>
    
  ```Powershell
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
  ```

    <span data-ttu-id="bd368-115">여기서 _Nameforrule_ 은 새 규칙의 이름 (예: JunkMailBeforeReachingContentFilter)입니다.</span><span class="sxs-lookup"><span data-stu-id="bd368-115">Where  _NameForRule_ is the name for the new rule, for example, JunkMailBeforeReachingContentFilter.</span></span> 
    
4. <span data-ttu-id="bd368-116">다음 명령을 실행 하 여 **보낸 사람 차단** 목록과 같은 스팸 필터 정책의 차단 목록에 있는 보낸 사람의 메시지가 정크 메일 폴더로 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd368-116">Run the following command to ensure that messages from senders in a block list in the spam filter policy, such as the **Sender block** list, are routed to the Junk Email folder:</span></span> 
    
  ```Powershell
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
  ```

    <span data-ttu-id="bd368-117">여기서 _Nameforrule_ 은 새 규칙의 이름 (예: JunkMailInSenderBlockList)입니다.</span><span class="sxs-lookup"><span data-stu-id="bd368-117">Where  _NameForRule_ is the name for the new rule, for example, JunkMailInSenderBlockList.</span></span> 
    
<span data-ttu-id="bd368-118">**정크 메일 폴더로 메시지 이동** 작업을 사용 하지 않으려면 Exchange 관리 센터에서 콘텐츠 필터 정책에서 다른 작업을 선택 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd368-118">If you do not want to use the **Move message to Junk Email folder** action, you can choose another action in your content filter policies in the Exchange admin center.</span></span> <span data-ttu-id="bd368-119">자세한 내용은 [스팸 필터 정책 구성을](configure-your-spam-filter-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bd368-119">For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span> <span data-ttu-id="bd368-120">메시지 헤더의 이러한 필드에 대 한 자세한 내용은 [스팸 방지 메시지 헤더](anti-spam-message-headers.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bd368-120">For more information about these fields in the message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span>
  

> [!TIP]
> <span data-ttu-id="bd368-121">**정크 메일 폴더로 메시지 이동** 작업을 사용 하지 않으려면 Exchange 관리 센터에서 콘텐츠 필터 정책에서 다른 작업을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd368-121">If you don't want to use the **Move message to Junk Email folder** action, you can choose another action in your content filter policies in the Exchange admin center.</span></span> <span data-ttu-id="bd368-122">자세한 내용은 [스팸 필터 정책 구성을](configure-your-spam-filter-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bd368-122">For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span> <span data-ttu-id="bd368-123">메시지 헤더의 이러한 필드에 대 한 자세한 내용은 [스팸 방지 메시지 헤더](anti-spam-message-headers.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bd368-123">For more information about these fields in the message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span>
> 
## <a name="see-also"></a><span data-ttu-id="bd368-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="bd368-124">See also</span></span>

[<span data-ttu-id="bd368-125">New-transportrule cmdlet</span><span class="sxs-lookup"><span data-stu-id="bd368-125">New-TransportRule cmdlet</span></span>](https://technet.microsoft.com/library/bb125138%28v=exchg.160%29.aspx)

