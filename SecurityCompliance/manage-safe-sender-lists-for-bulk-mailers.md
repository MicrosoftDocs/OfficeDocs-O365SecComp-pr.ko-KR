---
title: 대량 메일에 대해 수신 허용 - 보낸 사람 목록 관리
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d48db4a3-9fbe-45e2-bbaa-1017ffdf96f8
ms.collection:
- M365-security-compliance
description: '안전한 보낸 사람 목록을 사용 하려는 경우에는 EOP (Exchange Online Protection) 및 Outlook 처리가 서로 다르게 처리 된다는 사실을 알아야 합니다. 이 서비스는 rfc 5321 보낸 사람 주소와 rfc 5322.from 주소의을 검사 하 여 수신 허용-보낸 사람 및 도메인을 고려 하 고, Outlook에서는 rfc 5322.from 주소의 주소를 사용자의 수신 허용-발신자 목록에 추가 합니다. (참고: 서비스는 차단 된 보낸 사람 주소 및 도메인에 대 한 5321 주소와 5322.from 주소의 from address)를 모두 검사 합니다.'
ms.openlocfilehash: 006c2b9520f1e1f71f5ec745baaf84f906f31eb4
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259656"
---
# <a name="manage-safe-sender-lists-for-bulk-mailers"></a>대량 메일에 대해 수신 허용 - 보낸 사람 목록 관리

안전한 보낸 사람 목록을 사용 하려는 경우에는 EOP (Exchange Online Protection) 및 Outlook 처리가 서로 다르게 처리 된다는 사실을 알아야 합니다. Office 365 서비스는 rfc 5321 보낸 사람 주소 및 rfc 5322.from 주소의 from 주소를 조사 하 여 수신 허용-보낸 사람 및 도메인을 사용 하 고, Outlook에서는 rfc 5322.from 주소의 주소를 사용자의 수신 허용-발신자 목록에 추가 합니다. (참고: 서비스는 차단 된 보낸 사람 주소 및 도메인에 대 한 5321 주소와 5322.from 주소의 from address)를 모두 검사 합니다.
  
RFC 5321 라는 SMTP 메일 보낸 사람 주소는 SPF 검사를 수행 하는 데 사용 되는 전자 메일 주소이 고 메일을 배달할 수 없는 경우 반송 메시지가 배달 되는 경로입니다. 이 전자 메일 주소는 보낸 사람이 다른 반환 경로 주소를 지정할 수 있지만 메시지 헤더의 반환 경로에 기본적으로 포함 됩니다.
  
RFC 5322.from 주소의 라는 메시지 헤더에 보낸 사람: 주소는 Outlook과 같은 메일 클라이언트에 표시 되는 전자 메일 주소입니다.
  
대부분의 경우에는 5321 from 및 5322.from 주소의 from 주소가 동일 합니다. 이는 사용자 간 통신에 일반적으로 발생 합니다. 그러나 다른 사람을 대신 하 여 전자 메일을 보내는 경우에는 주소가 서로 다를 수 있습니다. 일반적으로 대량 전자 메일 메시지에서 가장 자주 발생 합니다.
  
예를 들어 비행기 용 파란 Yonder Airlines가 손 정 란 여행사가 전자 메일 광고를 보내도록 계약 했을 것으로 가정 합니다. 그런 다음 보낸 사람 blueyonder@news.blueyonderairlines.com에서 받은 편지함에 메시지를 받습니다. 이 경우 5321 보낸 사람 주소는 blueyonder.airlines@margiestravel.com이 고 blueyonder@news.blueyonderairlines.com은 5322.from 주소의입니다. 보낸 사람 주소는 Outlook에 표시 됩니다. 이 서비스는 rfc 5322.from 주소의를 사용 하 여이 메시지가 필터링 되지 않도록 하기 때문에 rfc 5322.from 주소의을 Outlook의 안전한 보낸 사람으로 추가할 수 있습니다 (사용자). 또는 관리자가 스팸 방지에 표시 된 메일 흐름 규칙을 설정 하는 경우 [ Protection](anti-spam-protection.md) 섹션
  

