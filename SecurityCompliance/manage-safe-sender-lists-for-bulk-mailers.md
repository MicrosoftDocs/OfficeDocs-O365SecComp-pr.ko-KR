---
title: 대량 메일에 대해 수신 허용 - 보낸 사람 목록 관리
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d48db4a3-9fbe-45e2-bbaa-1017ffdf96f8
description: '수신 허용-보낸사람 목록 사용 하려는 경우에 Exchange Online Protection (EOP) 하 고 Outlook으로 처리 다르게 처리 알고 있어야 합니다. Outlook 사용자의 수신 허용-보낸사람 목록에 RFC 5322.From 주소를 추가 하는 동안 RFC 5321.MailFrom 주소와 RFC 5322.From 주소를 검사 하 여 수신 허용-보낸사람 및 도메인 고려 하는 서비스입니다. (참고: 수신된 거부 하 고 도메인에 대 한 5321.MailFrom 주소와 5322.From 주소를 검사 하는 서비스입니다.)'
ms.openlocfilehash: 9442bb39e15b9db9a826472dd6110a8fa14130c6
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002997"
---
# <a name="manage-safe-sender-lists-for-bulk-mailers"></a>대량 메일에 대해 수신 허용 - 보낸 사람 목록 관리

수신 허용-보낸사람 목록 사용 하려는 경우에 Exchange Online Protection (EOP) 하 고 Outlook으로 처리 다르게 처리 알고 있어야 합니다. Outlook 사용자의 수신 허용-보낸사람 목록에 RFC 5322.From 주소를 추가 하는 동안 RFC 5321.MailFrom 주소와 RFC 5322.From 주소를 검사 하 여 수신 허용-보낸사람 및 도메인 고려 하는 서비스입니다. (참고: 수신된 거부 하 고 도메인에 대 한 5321.MailFrom 주소와 5322.From 주소를 검사 하는 서비스입니다.)
  
RFC 5321.MailFrom 주소 라고도 MAIL FROM SMTP 주소는 SPF 검사를 수행 하는데 사용 되는 전자 메일 주소는 메일 배달할 수 없는 경우, 반송 됨된 메시지가 배달 되는 경로 하 고 있습니다. 이것이 보낸 사람이 다른 수익 경로 주소를 지정 하는 경우에 기본적으로 메시지 헤더의 수익 경로에 남아 있는이 전자 메일 주소입니다.
  
From: 주소 RFC 5322.From 주소 라고도 하는 메시지 헤더에는 Outlook과 같은 메일 클라이언트에 표시 되는 전자 메일 주소입니다.
  
대부분의 시간, 5321.MailFrom 및 5322.From 주소는 동일 합니다. 개인 간 통신에 대 한 일반적인입니다. 그러나 다른 사람을 대신 하 여 전자 메일을 보내면 주소는 다른 경우가 많습니다. 일반적으로 이러한 발생 가장 자주 대량 전자 메일 메시지에 대 한 합니다.
  
예, 항공 Blue Yonder Airlines의 전자 메일 알림을 보낼 Margie의 여행을 계약에 경우를 가정해 보겠습니다. 그런 다음 메시지가 받은 편지함에 보낸 blueyonder@news.blueyonderairlines.com에서 합니다. 이 경우 5321.MailFrom 주소 blueyonder.airlines@margiestravel.com, 이며 blueyonder@news.blueyonderairlines.com 중 Outlook에서 참조 하는 하는 5322.From 주소입니다. 서비스 문자의 RFC 5322.From 주소가이 메시지 필터링 시작 하지 못하도록 하기 때문에 Outlook의 수신 허용-보낸사람으로 간단히 RFC 5322.From 주소를 추가할 수 있습니다.
  

