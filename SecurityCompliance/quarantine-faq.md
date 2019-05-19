---
title: 격리 FAQ
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/16/2017
audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c440b2ac-cafa-4be5-ba4c-14278a7990ae
ms.collection:
- M365-security-compliance
description: 이 항목에서는 호스팅되는 격리에 대한 질문과 대답을 제공합니다.
ms.openlocfilehash: a8e4c8ba67e94c5c61da6c88f8086d780081d1a6
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157220"
---
# <a name="quarantine-faq"></a><span data-ttu-id="c3a00-103">격리 FAQ</span><span class="sxs-lookup"><span data-stu-id="c3a00-103">Quarantine FAQ</span></span>

<span data-ttu-id="c3a00-p101">이 항목에서는 호스팅되는 격리에 대한 질문과 대답을 제공합니다. 대답은 Microsoft Exchange Online 및 Exchange Online Protection 고객에게 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-p101">This topic provides frequently asked questions and answers about the hosted quarantine. Answers are applicable for Microsoft Exchange Online and Exchange Online Protection customers.</span></span>
  
 <span data-ttu-id="c3a00-106">**Q. 격리에서 맬웨어 격리 메시지를 관리 하려면 어떻게 해야 하나요?**</span><span class="sxs-lookup"><span data-stu-id="c3a00-106">**Q. How do I manage malware-quarantined messages in quarantine?**</span></span>
  
<span data-ttu-id="c3a00-107">격리로 전송 된 메시지를 &amp; 보고 작업 하려면 보안 준수 센터를 사용 해야 합니다 (맬웨어 포함).</span><span class="sxs-lookup"><span data-stu-id="c3a00-107">You need to use the Security &amp; Compliance Center in order to view and work with messages that were sent to quarantine because they contain malware.</span></span> <span data-ttu-id="c3a00-108">자세한 내용은 [Office 365에서 전자 메일 메시지 격리](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3a00-108">For more information, see [Quarantine email messages in Office 365](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).</span></span>
  
 <span data-ttu-id="c3a00-109">**질문. 스팸으로 격리된 메시지를 격리로 보내도록 서비스를 구성하려면 어떻게 해야 합니까?**</span><span class="sxs-lookup"><span data-stu-id="c3a00-109">**Q. How do I configure the service to send spam-quarantined messages to the quarantine?**</span></span>
  
<span data-ttu-id="c3a00-110">대답.</span><span class="sxs-lookup"><span data-stu-id="c3a00-110">A.</span></span> <span data-ttu-id="c3a00-111">기본적으로 콘텐츠가 필터링된 메시지는 받는 사람의 정크 메일 폴더로 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-111">By default, content-filtered messages are sent to the recipients Junk Email folder.</span></span> <span data-ttu-id="c3a00-112">그러나 관리자는 스팸으로 격리된 메시지를 격리로 대신 보내도록 콘텐츠 필터 정책을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-112">However, admins can configure content filter policies to send spam-quarantined messages to the quarantine instead.</span></span> <span data-ttu-id="c3a00-113">콘텐츠가 필터링 된 메시지에 대해 수행할 수 있는 다양 한 작업에 대 한 자세한 내용은 [스팸 필터 정책 구성을](configure-your-spam-filter-policies.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3a00-113">For more information about the different actions that can be performed on content-filtered messages, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
 <span data-ttu-id="c3a00-114">**질문. 서비스에서 스팸으로 격리된 메시지를 관리자 및 최종 사용자가 관리할 수 있는 기능을 제공합니까?**</span><span class="sxs-lookup"><span data-stu-id="c3a00-114">**Q. Does the service have administrator and end user management of spam-quarantined messages?**</span></span>
  
<span data-ttu-id="c3a00-p104">A. 관리자는 EAC(Exchange 관리 센터)에서 격리된 모든 전자 메일 메시지에 대한 세부 정보를 검색하고 볼 수 있습니다. 메시지를 찾은 후 특정 사용자에게 릴리스하고 원하는 경우 Microsoft 스팸 분석 팀에 가양성(정크 메일 아님)으로 보고할 수 있습니다. 자세한 내용은 [관리자로 격리된 메시지 찾기 및 릴리스](find-and-release-quarantined-messages-as-an-administrator.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c3a00-p104">A. As an administrator, you can search for and view details about all quarantined email messages in the Exchange admin center (EAC). After locating the message, you can release it to specific users and optionally report it as a false positive (not junk) to the Microsoft Spam Analysis Team. For more information, see [Find and release quarantined messages as an administrator](find-and-release-quarantined-messages-as-an-administrator.md).</span></span>
  
<span data-ttu-id="c3a00-119">최종 사용자는 다음을 통해 스팸 격리된 메시지를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-119">As an end user, you can manage your own spam-quarantined messages via:</span></span> 
  
- <span data-ttu-id="c3a00-120">스팸 격리 사용자 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-120">The spam quarantine user interface.</span></span> <span data-ttu-id="c3a00-121">자세한 내용은 [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c3a00-121">For more information, see [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx).</span></span>
        
 <span data-ttu-id="c3a00-122">**Q. 최종 사용자에게 스팸 격리소에 대한 액세스 권한을 부여하려면 어떻게 합니까?**</span><span class="sxs-lookup"><span data-stu-id="c3a00-122">**Q. How do I grant access to the spam quarantine for my end users?**</span></span>
  
<span data-ttu-id="c3a00-123">대답.</span><span class="sxs-lookup"><span data-stu-id="c3a00-123">A.</span></span> <span data-ttu-id="c3a00-124">최종 사용자 스팸 격리에 액세스 하려면 최종 사용자에 게 유효한 Office 365 사용자 ID 및 암호가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-124">In order to access the end user spam quarantine, end users must have a valid Office 365 user ID and password.</span></span> <span data-ttu-id="c3a00-125">온-프레미스 사서함을 보호 하는 EOP 고객은 디렉터리 동기화 또는 EAC를 통해 만든 유효한 전자 메일 사용자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-125">EOP customers protecting on-premises mailboxes must be valid email users created via directory synchronization or the EAC.</span></span> <span data-ttu-id="c3a00-126">사용자를 관리 하는 방법에 대 한 자세한 내용은 EOP 관리자가 [EOP에서 메일 사용자 관리](eop/manage-mail-users-in-eop.md)를 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-126">For more information about managing users, EOP admins can refer to [Manage mail users in EOP](eop/manage-mail-users-in-eop.md).</span></span> <span data-ttu-id="c3a00-127">EOP 독립 실행형 고객의 경우 디렉터리 동기화 및 디렉터리 기반 Edge 차단을 사용 하는 것이 좋습니다. 자세한 내용은 [디렉터리 기반 Edge 차단을 사용 하 여 잘못 된 받는 사람에 게 보낸 메시지 거부](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3a00-127">For EOP standalone customers, we recommend using directory synchronization and enabling Directory Based Edge Blocking; for more information, see [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span></span>
  
 <span data-ttu-id="c3a00-128">**질문. 스팸 이외의 항목을 격리로 보낼 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="c3a00-128">**Q. Can anything other than spam be sent to the quarantine?**</span></span>
  
<span data-ttu-id="c3a00-129">대답.</span><span class="sxs-lookup"><span data-stu-id="c3a00-129">A.</span></span> <span data-ttu-id="c3a00-130">메일 흐름 규칙 (전송 규칙이 라고도 함)과 일치 하는 메시지는 구성 된 작업 인 경우에도 관리자 격리로 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-130">Messages that match a mail flow rule (also known as a transport rule) can also be sent to the administrator quarantine, if that's the configured action.</span></span> <span data-ttu-id="c3a00-131">최종 사용자 격리는 스팸 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-131">The end user quarantine is for spam only.</span></span>
  
 <span data-ttu-id="c3a00-132">**질문. 메시지는 얼마 동안 격리에 보관됩니까?**</span><span class="sxs-lookup"><span data-stu-id="c3a00-132">**Q. For how long are messages kept in the quarantine?**</span></span>
  
<span data-ttu-id="c3a00-133">대답.</span><span class="sxs-lookup"><span data-stu-id="c3a00-133">A.</span></span> <span data-ttu-id="c3a00-134">기본적으로 스팸 격리 메시지는 30 일 동안 격리 된 상태로 유지 되 고, 메일 흐름 규칙과 일치 하는 격리 된 메시지는 7 일 동안 격리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-134">By default, spam-quarantined messages are kept in the quarantine for 30 days, while quarantined messages that matched a mail flow rule are kept in the quarantine for 7 days.</span></span> <span data-ttu-id="c3a00-135">이 기간 후에 메시지는 삭제되며 검색할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-135">After this period of time the messages are deleted and are not retrievable.</span></span> <span data-ttu-id="c3a00-136">메일 흐름 규칙과 일치 하는 격리 된 메시지의 보존 기간은 구성할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-136">The retention period for quarantined messages that matched a mail flow rule is not configurable.</span></span> <span data-ttu-id="c3a00-137">그렇지만 스팸 격리 메시지의 보존 기간은 콘텐츠 필터 정책의 **스팸 보존 기간(일)** 설정을 통해 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-137">However, the retention period for spam-quarantined messages can be lowered via the **Retain spam for (days)** setting in your content filter policies.</span></span> <span data-ttu-id="c3a00-138">자세한 내용은 [스팸 필터 정책 구성을](configure-your-spam-filter-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3a00-138">For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
 <span data-ttu-id="c3a00-139">**Q. 한 번에 2개 이상의 격리된 메시지를 해제하거나 보고할 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="c3a00-139">**Q. Can I release or report more than one quarantined message at a time?**</span></span>
  
<span data-ttu-id="c3a00-140">A.</span><span class="sxs-lookup"><span data-stu-id="c3a00-140">A.</span></span> <span data-ttu-id="c3a00-141">한 번에 여러 메시지를 릴리스 하거나 보고 하는 기능은 현재 EAC 또는 최종 사용자 스팸 격리에서 제공 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-141">The ability to release or report multiple messages at once is not currently available in the EAC or the end user spam quarantine.</span></span> <span data-ttu-id="c3a00-142">그렇지만 관리자는 이 작업을 수행하는 원격 Windows PowerShell 스크립트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-142">However, admins can create a remote Windows PowerShell script to accomplish this task.</span></span> <span data-ttu-id="c3a00-143">[Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet을 사용하여 메시지를 검색하고 [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet을 사용하여 메시지를 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-143">Use the [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet to search for messages, and the [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet to release them.</span></span> 
  
 <span data-ttu-id="c3a00-144">**질문. 격리된 메시지 검색 시 와일드카드가 지원됩니까? 특정 도메인에 대해 격리된 메시지를 검색할 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="c3a00-144">**Q. Are wildcards supported when searching for quarantined messages? Can I search for quarantined messages for a specific domain?**</span></span>
  
<span data-ttu-id="c3a00-p110">대답. Exchange 관리 센터에서 검색 조건을 지정할 때는 와일드카드가 지원되지 않습니다. 예를 들어 보낸 사람을 검색할 때는 전체 전자 메일 주소를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-p110">A. Wildcards are not supported when specifying search criteria in the Exchange admin center. For example, when searching for a sender, you must specify the full email address.</span></span>
  
<span data-ttu-id="c3a00-148">원격 Windows PowerShell을 통해 관리자는 [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet을 지정하여 contoso.com과 같은 특정 도메인에 대해 격리된 메시지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-148">Using remote Windows PowerShell, admins can specify the [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet to search for quarantined messages for a specific domain (for example, contoso.com):</span></span> 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```

<span data-ttu-id="c3a00-p111">이 결과는 [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet으로 전달될 수 있습니다. 메시지를 모든 받는 사람에게 릴리스하려면 -ReleaseToAll 매개 변수를 포함합니다. 메시지를 릴리스한 후에는 다시 릴리스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c3a00-p111">The results can be passed to the [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet. Include the -ReleaseToAll parameter to release the message to all recipients. Once a message is released, it can't be released again.</span></span> 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```


