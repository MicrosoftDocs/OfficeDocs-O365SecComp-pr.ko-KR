---
title: DKIM으로 서명된 메시지의 유효성 검사 지원
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
ms.collection:
- M365-security-compliance
description: Exchange Online Protection 및 Exchange Online에서 DKIM 서명 된 메시지의 유효성 검사에 대해 자세히 알아보기
ms.openlocfilehash: 0538158d052afb632dc0adbb14a88aa9766e6322
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156450"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a>DKIM으로 서명된 메시지의 유효성 검사 지원

EOP(Exchange Online Protection) 및 Exchange Online은 [DKIM(Domain Keys Identified Mail)](https://www.rfc-editor.org/rfc/rfc6376.txt)) 메시지의 인바운드 유효성 검사를 지원합니다. DKIM은 메시지를 전송한 도메인이 메시지에 표시된 도메인이 맞으며 다른 사람이 스푸핑하지 않았다는 유효성을 증명하는 방법으로, 전자 메일 메시지를 메시지 전송 조직에 연결합니다. DKIM 확인은 IPv6 통신을 통해 전송된 모든 메시지에 자동으로 사용됩니다. IPv6 지원에 대한 자세한 내용은 [IPv6을 통한 익명 인바운드 전자 메일 메시지 지원](support-for-anonymous-inbound-email-messages-over-ipv6.md)을 참조하세요.
  
DKIM은 메시지 헤더의 DKIM 서명 헤더에 표시되는 디지털 서명된 메시지의 유효성을 검사합니다. DKIM 서명 유효성 검사의 결과는 RFC 7001([메시지 인증 상태를 나타내는 메시지 헤더 필드](https://www.rfc-editor.org/rfc/rfc7001.txt))을 준수하는 Authentication-Results 헤더에 스탬프 처리됩니다. 메시지 헤더 텍스트는 다음과 같이 표시됩니다. 여기서는 contoso.com이 보낸 사람입니다.
  
 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`
  
관리자는 DKIM 유효성 검사의 결과에 Exchange [메일 흐름 규칙](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) (전송 규칙이 라고도 함)을 만들어 필요에 따라 메시지를 필터링 하거나 라우팅할 수 있습니다. 
  

