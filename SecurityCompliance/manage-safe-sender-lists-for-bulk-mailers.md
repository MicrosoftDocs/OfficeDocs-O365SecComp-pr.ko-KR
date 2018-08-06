---
title: 대량 우편물에 대 한 수신 허용-보낸사람 목록 관리
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: d48db4a3-9fbe-45e2-bbaa-1017ffdf96f8
description: '수신 허용-보낸사람 목록 사용 하려는 경우에 Exchange Online Protection (EOP) 하 고 Outlook으로 처리 다르게 처리 알고 있어야 합니다. Outlook 사용자의 수신 허용-보낸사람 목록에 RFC 5322.From 주소를 추가 하는 동안 RFC 5321.MailFrom 주소와 RFC 5322.From 주소를 검사 하 여 수신 허용-보낸사람 및 도메인 고려 하는 서비스입니다. (참고: 수신된 거부 하 고 도메인에 대 한 5321.MailFrom 주소와 5322.From 주소를 검사 하는 서비스입니다.)'
ms.openlocfilehash: e5d6f8440281d527e7ea1846416b785beda25f1c
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026545"
---
# <a name="manage-safe-sender-lists-for-bulk-mailers"></a><span data-ttu-id="8eebf-105">대량 우편물에 대 한 수신 허용-보낸사람 목록 관리</span><span class="sxs-lookup"><span data-stu-id="8eebf-105">Manage safe sender lists for bulk mailers</span></span>

<span data-ttu-id="8eebf-p102">수신 허용-보낸사람 목록 사용 하려는 경우에 Exchange Online Protection (EOP) 하 고 Outlook으로 처리 다르게 처리 알고 있어야 합니다. Outlook 사용자의 수신 허용-보낸사람 목록에 RFC 5322.From 주소를 추가 하는 동안 RFC 5321.MailFrom 주소와 RFC 5322.From 주소를 검사 하 여 수신 허용-보낸사람 및 도메인 고려 하는 서비스입니다. (참고: 수신된 거부 하 고 도메인에 대 한 5321.MailFrom 주소와 5322.From 주소를 검사 하는 서비스입니다.)</span><span class="sxs-lookup"><span data-stu-id="8eebf-p102">If you want to use safe sender lists, you should know that Exchange Online Protection (EOP) and Outlook handle processing differently. The service respects safe senders and domains by inspecting the RFC 5321.MailFrom address and the RFC 5322.From address, while Outlook adds the RFC 5322.From address to a user's safe sender list. (Note: The service inspects both the 5321.MailFrom address and 5322.From address for blocked senders and domains.)</span></span>
  
<span data-ttu-id="8eebf-p103">RFC 5321.MailFrom 주소 라고도 MAIL FROM SMTP 주소는 SPF 검사를 수행 하는데 사용 되는 전자 메일 주소는 메일 배달할 수 없는 경우, 반송 됨된 메시지가 배달 되는 경로 하 고 있습니다. 이것이 보낸 사람이 다른 수익 경로 주소를 지정 하는 경우에 기본적으로 메시지 헤더의 수익 경로에 남아 있는이 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="8eebf-p103">The SMTP MAIL FROM address, otherwise known as the RFC 5321.MailFrom address, is the email address that's used to perform SPF checks, and if the mail can't be delivered, the path to which the bounced message is delivered. It's this email address that is placed into the Return-Path in the message headers by default, though it's possible for the sender to designate a different Return-Path address.</span></span>
  
<span data-ttu-id="8eebf-111">From: 주소 RFC 5322.From 주소 라고도 하는 메시지 헤더에는 Outlook과 같은 메일 클라이언트에 표시 되는 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="8eebf-111">The From: address in the message headers, otherwise known as the RFC 5322.From address, is the email address that is displayed in the mail client such as Outlook.</span></span>
  
<span data-ttu-id="8eebf-p104">대부분의 시간, 5321.MailFrom 및 5322.From 주소는 동일 합니다. 개인 간 통신에 대 한 일반적인입니다. 그러나 다른 사람을 대신 하 여 전자 메일을 보내면 주소는 다른 경우가 많습니다. 일반적으로 이러한 발생 가장 자주 대량 전자 메일 메시지에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eebf-p104">Much of the time, the 5321.MailFrom and 5322.From addresses are the same. This is typical for person-to-person communication. However, when email is sent on behalf of someone else, the addresses are frequently different. This usually happens most often for bulk email messages.</span></span>
  
<span data-ttu-id="8eebf-p105">예, 항공 Blue Yonder Airlines의 전자 메일 알림을 보낼 Margie의 여행을 계약에 경우를 가정해 보겠습니다. 그런 다음 메시지가 받은 편지함에 보낸 blueyonder@news.blueyonderairlines.com에서 합니다. 이 경우 5321.MailFrom 주소 blueyonder.airlines@margiestravel.com, 이며 blueyonder@news.blueyonderairlines.com 중 Outlook에서 참조 하는 하는 5322.From 주소입니다. 서비스 문자의 RFC 5322.From 주소가이 메시지 필터링 시작 하지 못하도록 하기 때문에 Outlook의 수신 허용-보낸사람으로 간단히 RFC 5322.From 주소를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8eebf-p105">For example, suppose that the airline Blue Yonder Airlines has contracted out Margie's Travel to send out its email advertising. You then get a message in your inbox from sender blueyonder@news.blueyonderairlines.com. In this case, the 5321.MailFrom address is blueyonder.airlines@margiestravel.com, and blueyonder@news.blueyonderairlines.com is the 5322.From address which is the one you see in Outlook. Because the service respects the RFC 5322.From address, to prevent this message from getting filtered, you can simply add the RFC 5322.From address as a safe sender in Outlook.</span></span>
  

