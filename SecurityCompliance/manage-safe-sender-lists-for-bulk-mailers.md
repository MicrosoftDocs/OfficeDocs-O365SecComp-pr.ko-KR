---
title: 대량 메일에 대해 수신 허용 - 보낸 사람 목록 관리
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
ms.assetid: d48db4a3-9fbe-45e2-bbaa-1017ffdf96f8
ms.collection:
- M365-security-compliance
description: '안전한 보낸 사람 목록을 사용 하려는 경우에는 EOP (Exchange Online Protection) 및 Outlook 처리가 서로 다르게 처리 된다는 사실을 알아야 합니다. 이 서비스는 rfc 5321 보낸 사람 주소와 RFC 5322.from 주소의을 검사 하 여 수신 허용-보낸 사람 및 도메인을 고려 하 고, Outlook에서는 RFC 5322.from 주소의 주소를 사용자의 수신 허용-발신자 목록에 추가 합니다. (참고: 서비스는 차단 된 보낸 사람 주소 및 도메인에 대 한 5321 주소와 5322.from 주소의 from address)를 모두 검사 합니다.'
ms.openlocfilehash: f73cc3fc88318c4f625bf5579f73d92625624fd5
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598794"
---
# <a name="manage-safe-sender-lists-for-bulk-mailers"></a><span data-ttu-id="093fa-105">대량 메일에 대해 수신 허용 - 보낸 사람 목록 관리</span><span class="sxs-lookup"><span data-stu-id="093fa-105">Manage safe sender lists for bulk mailers</span></span>

<span data-ttu-id="093fa-106">안전한 보낸 사람 목록을 사용 하려는 경우에는 EOP (Exchange Online Protection) 및 Outlook 처리가 서로 다르게 처리 된다는 사실을 알아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-106">If you want to use safe sender lists, you should know that Exchange Online Protection (EOP) and Outlook handle processing differently.</span></span> <span data-ttu-id="093fa-107">Office 365 서비스는 rfc 5321 보낸 사람 주소 및 RFC 5322.from 주소의 From 주소를 조사 하 여 수신 허용-보낸 사람 및 도메인을 사용 하 고, Outlook에서는 RFC 5322.from 주소의 주소를 사용자의 수신 허용-발신자 목록에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-107">The Office 365 service respects safe senders and domains by inspecting the RFC 5321.MailFrom address and the RFC 5322.From address, while Outlook adds the RFC 5322.From address to a user's safe sender list.</span></span> <span data-ttu-id="093fa-108">(참고: 서비스는 차단 된 보낸 사람 주소 및 도메인에 대 한 5321 주소와 5322.from 주소의 from address)를 모두 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-108">(Note: The service inspects both the 5321.MailFrom address and 5322.From address for blocked senders and domains.)</span></span>
  
<span data-ttu-id="093fa-109">RFC 5321 라는 SMTP 메일 보낸 사람 주소는 SPF 검사를 수행 하는 데 사용 되는 전자 메일 주소이 고 메일을 배달할 수 없는 경우 반송 메시지가 배달 되는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-109">The SMTP MAIL FROM address, otherwise known as the RFC 5321.MailFrom address, is the email address that's used to perform SPF checks, and if the mail can't be delivered, the path to which the bounced message is delivered.</span></span> <span data-ttu-id="093fa-110">이 전자 메일 주소는 보낸 사람이 다른 반환 경로 주소를 지정할 수 있지만 메시지 헤더의 반환 경로에 기본적으로 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-110">It's this email address that is placed into the Return-Path in the message headers by default, though it's possible for the sender to designate a different Return-Path address.</span></span>
  
<span data-ttu-id="093fa-111">RFC 5322.from 주소의 라는 메시지 헤더에 보낸 사람: 주소는 Outlook과 같은 메일 클라이언트에 표시 되는 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-111">The From: address in the message headers, otherwise known as the RFC 5322.From address, is the email address that is displayed in the mail client such as Outlook.</span></span>
  
<span data-ttu-id="093fa-112">대부분의 경우에는 5321 From 및 5322.from 주소의 From 주소가 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-112">Much of the time, the 5321.MailFrom and 5322.From addresses are the same.</span></span> <span data-ttu-id="093fa-113">이는 사용자 간 통신에 일반적으로 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-113">This is typical for person-to-person communication.</span></span> <span data-ttu-id="093fa-114">그러나 다른 사람을 대신 하 여 전자 메일을 보내는 경우에는 주소가 서로 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-114">However, when email is sent on behalf of someone else, the addresses are frequently different.</span></span> <span data-ttu-id="093fa-115">일반적으로 대량 전자 메일 메시지에서 가장 자주 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-115">This usually happens most often for bulk email messages.</span></span>
  
<span data-ttu-id="093fa-116">예를 들어 비행기 용 파란 Yonder Airlines가 손 정 란 여행사가 전자 메일 광고를 보내도록 계약 했을 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-116">For example, suppose that the airline Blue Yonder Airlines has contracted out Margie's Travel to send out its email advertising.</span></span> <span data-ttu-id="093fa-117">그런 다음 보낸 사람 blueyonder@news.blueyonderairlines.com에서 받은 편지함에 메시지를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-117">You then get a message in your inbox from sender blueyonder@news.blueyonderairlines.com.</span></span> <span data-ttu-id="093fa-118">이 경우 5321 보낸 사람 주소는 blueyonder.airlines@margiestravel.com이 고 blueyonder@news.blueyonderairlines.com은 5322.from 주소의입니다. 보낸 사람 주소는 Outlook에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-118">In this case, 5321.MailFrom address is blueyonder.airlines@margiestravel.com, and blueyonder@news.blueyonderairlines.com is the 5322.From address which is the one, you see in Outlook.</span></span> <span data-ttu-id="093fa-119">이 서비스는 RFC 5322.from 주소의를 사용 하 여이 메시지가 필터링 되지 않도록 하기 때문에 RFC 5322.from 주소의을 Outlook의 안전한 보낸 사람으로 추가할 수 있습니다 (사용자). 또는 관리자가 스팸 방지에 표시 된 메일 흐름 규칙을 설정 하는 경우 [ Protection](anti-spam-protection.md) 섹션</span><span class="sxs-lookup"><span data-stu-id="093fa-119">Because the service respects the RFC 5322.From address, to prevent this message from getting filtered, you can add the RFC 5322.From address as a safe sender in Outlook (as a user) or, if you're an administrator set up a mailflow rule as shown on the [Anti-spam Protection](anti-spam-protection.md) section.</span></span>
  

