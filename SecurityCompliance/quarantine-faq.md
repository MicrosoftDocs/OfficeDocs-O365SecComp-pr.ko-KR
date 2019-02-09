---
title: 격리 FAQ
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/16/2017
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c440b2ac-cafa-4be5-ba4c-14278a7990ae
description: 이 항목에서는 호스팅되는 격리에 대한 질문과 대답을 제공합니다.
ms.openlocfilehash: 1473e682faab0471f5a6356e8d54a65a9baf291a
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2019
ms.locfileid: "29792499"
---
# <a name="quarantine-faq"></a><span data-ttu-id="ca9b7-103">격리 FAQ</span><span class="sxs-lookup"><span data-stu-id="ca9b7-103">Quarantine FAQ</span></span>

<span data-ttu-id="ca9b7-p101">이 항목에서는 호스팅되는 격리에 대한 질문과 대답을 제공합니다. 대답은 Microsoft Exchange Online 및 Exchange Online Protection 고객에게 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca9b7-p101">This topic provides frequently asked questions and answers about the hosted quarantine. Answers are applicable for Microsoft Exchange Online and Exchange Online Protection customers.</span></span>
  
 <span data-ttu-id="ca9b7-106">**질문: 격리에서 맬웨어 격리 된 메시지를 관리 하려면는 어떻게**</span><span class="sxs-lookup"><span data-stu-id="ca9b7-106">**Q. How do I manage malware-quarantined messages in quarantine?**</span></span>
  
<span data-ttu-id="ca9b7-p102">보안을 사용 하 여 필요한 &amp; 보고 맬웨어를 포함 하기 때문에 격리로 전송 된 메시지와 함께 작업을 수행 하기 위해 준수 센터입니다. 자세한 내용은 [Office 365에서 전자 메일 메시지를 격리를](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ca9b7-p102">You need to use the Security &amp; Compliance Center in order to view and work with messages that were sent to quarantine because they contain malware. For more information, see [Quarantine email messages in Office 365](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).</span></span>
  
 <span data-ttu-id="ca9b7-109">**질문. 스팸으로 격리된 메시지를 격리로 보내도록 서비스를 구성하려면 어떻게 해야 합니까?**</span><span class="sxs-lookup"><span data-stu-id="ca9b7-109">**Q. How do I configure the service to send spam-quarantined messages to the quarantine?**</span></span>
  
<span data-ttu-id="ca9b7-p103">A. 기본적으로 콘텐츠 필터링 된 메시지의 받는 사람에 게 정크 메일 폴더로 전송 됩니다. 그러나 관리자는 대신 격리로 스팸 격리 된 메시지를 보낼 콘텐츠 필터 정책을 구성할 수 있습니다. 콘텐츠 필터링 된 메시지에서 수행할 수 있는 다른 작업에 대 한 자세한 내용은 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ca9b7-p103">A. By default, content-filtered messages are sent to the recipients Junk Email folder. However, admins can configure content filter policies to send spam-quarantined messages to the quarantine instead. For more information about the different actions that can be performed on content-filtered messages, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
 <span data-ttu-id="ca9b7-114">**질문. 서비스에서 스팸으로 격리된 메시지를 관리자 및 최종 사용자가 관리할 수 있는 기능을 제공합니까?**</span><span class="sxs-lookup"><span data-stu-id="ca9b7-114">**Q. Does the service have administrator and end user management of spam-quarantined messages?**</span></span>
  
<span data-ttu-id="ca9b7-p104">A. 관리자는 EAC(Exchange 관리 센터)에서 격리된 모든 전자 메일 메시지에 대한 세부 정보를 검색하고 볼 수 있습니다. 메시지를 찾은 후 특정 사용자에게 릴리스하고 원하는 경우 Microsoft 스팸 분석 팀에 가양성(정크 메일 아님)으로 보고할 수 있습니다. 자세한 내용은 [관리자로 격리된 메시지 찾기 및 릴리스](find-and-release-quarantined-messages-as-an-administrator.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ca9b7-p104">A. As an administrator, you can search for and view details about all quarantined email messages in the Exchange admin center (EAC). After locating the message, you can release it to specific users and optionally report it as a false positive (not junk) to the Microsoft Spam Analysis Team. For more information, see [Find and release quarantined messages as an administrator](find-and-release-quarantined-messages-as-an-administrator.md).</span></span>
  
<span data-ttu-id="ca9b7-119">최종 사용자는 다음을 통해 스팸 격리된 메시지를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca9b7-119">As an end user, you can manage your own spam-quarantined messages via:</span></span> 
  
- <span data-ttu-id="ca9b7-p105">스팸 격리 사용자 인터페이스입니다. 자세한 내용은 [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ca9b7-p105">The spam quarantine user interface. For more information, see [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx).</span></span>
        
 <span data-ttu-id="ca9b7-122">**Q. 최종 사용자에게 스팸 격리소에 대한 액세스 권한을 부여하려면 어떻게 합니까?**</span><span class="sxs-lookup"><span data-stu-id="ca9b7-122">**Q. How do I grant access to the spam quarantine for my end users?**</span></span>
  
<span data-ttu-id="ca9b7-p106">A. 하려면 최종 사용자 스팸 격리에 액세스, 최종 사용자에 게 유효한 Office 365 사용자 ID와 암호가 있어야 합니다. 온-프레미스 사서함을 보호 하는 EOP 고객 디렉터리 동기화 또는 EAC를 통해 만든 유효한 전자 메일 사용자 여야 합니다. 사용자를 관리 하는 방법에 대 한 자세한 내용은 EOP 관리자의 [EOP의 메일 사용자 관리를](eop/manage-mail-users-in-eop.md)참조할 수 있습니다. EOP 독립 실행형 고객을 위한 것이 좋습니다 디렉터리 동기화를 사용 하 고 디렉터리 기반 Edge 차단; 사용 하도록 설정 자세한 내용은 다음을 [사용 하 여 디렉터리 기반 Edge 차단 거부 잘못 된 받는 사람에 게 보낸 메시지를](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ca9b7-p106">A. In order to access the end user spam quarantine, end users must have a valid Office 365 user ID and password. EOP customers protecting on-premises mailboxes must be valid email users created via directory synchronization or the EAC. For more information about managing users, EOP admins can refer to [Manage mail users in EOP](eop/manage-mail-users-in-eop.md). For EOP standalone customers, we recommend using directory synchronization and enabling Directory Based Edge Blocking; for more information, see [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span></span>
  
 <span data-ttu-id="ca9b7-128">**질문. 스팸 이외의 항목을 격리로 보낼 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="ca9b7-128">**Q. Can anything other than spam be sent to the quarantine?**</span></span>
  
<span data-ttu-id="ca9b7-p107">대답. 전송 규칙과 일치하는 메시지도 관리자 격리로 보낼 수 있습니다(격리로 보내기가 구성된 작업인 경우). 최종 사용자 격리는 스팸 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="ca9b7-p107">A. Messages that match a transport rule can also be sent to the administrator quarantine, if that's the configured action. The end user quarantine is for spam only.</span></span>
  
 <span data-ttu-id="ca9b7-132">**질문. 메시지는 얼마 동안 격리에 보관됩니까?**</span><span class="sxs-lookup"><span data-stu-id="ca9b7-132">**Q. For how long are messages kept in the quarantine?**</span></span>
  
<span data-ttu-id="ca9b7-p108">A. 기본적으로 스팸 격리 메시지를 전송 규칙과 일치 하는 격리 된 메시지는 7 일이에 대 한 사용자를 격리에 보관 되는 동안 30 일 동안 격리에 보관 됩니다. 이 기간 후 메시지가 삭제 되 고 검색할 수 없습니다. 전송 규칙과 일치 하는 격리 된 메시지에 대 한 보존 기간을 구성할 수는 없습니다. 그러나 콘텐츠 필터 정책에서 **보관 스팸 (일)에 대 한** 설정을 통해 스팸 격리 된 메시지에 대 한 보존 기간을 낮출 수 있습니다. 자세한 내용은 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ca9b7-p108">A. By default, spam-quarantined messages are kept in the quarantine for 30 days, while quarantined messages that matched a transport rule are kept in the quarantine for 7 days. After this period of time the messages are deleted and are not retrievable. The retention period for quarantined messages that matched a transport rule is not configurable. However, the retention period for spam-quarantined messages can be lowered via the **Retain spam for (days)** setting in your content filter policies. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
 <span data-ttu-id="ca9b7-139">**Q. 한 번에 2개 이상의 격리된 메시지를 해제하거나 보고할 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="ca9b7-139">**Q. Can I release or report more than one quarantined message at a time?**</span></span>
  
<span data-ttu-id="ca9b7-p109">A.를 해제 하거나 한번에 여러 메시지를 보고 기능을 EAC 또는 최종 사용자 스팸 격리에서 현재 사용할 수 없는 경우 그러나 관리자가이 작업을 수행 하기 위해 원격 Windows PowerShell 스크립트를 만들 수 있습니다. 메시지를 검색 하려면 [Get-quarantinemessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet 및 해제 하는 [릴리스 QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca9b7-p109">A. The ability to release or report multiple messages at once is not currently available in the EAC or the end user spam quarantine. However, admins can create a remote Windows PowerShell script to accomplish this task. Use the [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet to search for messages, and the [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet to release them.</span></span> 
  
 <span data-ttu-id="ca9b7-144">**질문. 격리된 메시지 검색 시 와일드카드가 지원됩니까? 특정 도메인에 대해 격리된 메시지를 검색할 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="ca9b7-144">**Q. Are wildcards supported when searching for quarantined messages? Can I search for quarantined messages for a specific domain?**</span></span>
  
<span data-ttu-id="ca9b7-p110">대답. Exchange 관리 센터에서 검색 조건을 지정할 때는 와일드카드가 지원되지 않습니다. 예를 들어 보낸 사람을 검색할 때는 전체 전자 메일 주소를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca9b7-p110">A. Wildcards are not supported when specifying search criteria in the Exchange admin center. For example, when searching for a sender, you must specify the full email address.</span></span>
  
<span data-ttu-id="ca9b7-148">원격 Windows PowerShell을 통해 관리자는 [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet을 지정하여 contoso.com과 같은 특정 도메인에 대해 격리된 메시지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca9b7-148">Using remote Windows PowerShell, admins can specify the [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet to search for quarantined messages for a specific domain (for example, contoso.com):</span></span> 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```

<span data-ttu-id="ca9b7-p111">이 결과는 [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet으로 전달될 수 있습니다. 메시지를 모든 받는 사람에게 릴리스하려면 -ReleaseToAll 매개 변수를 포함합니다. 메시지를 릴리스한 후에는 다시 릴리스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ca9b7-p111">The results can be passed to the [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet. Include the -ReleaseToAll parameter to release the message to all recipients. Once a message is released, it can't be released again.</span></span> 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```


