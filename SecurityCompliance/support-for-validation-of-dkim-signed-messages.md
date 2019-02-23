---
title: DKIM으로 서명된 메시지의 유효성 검사 지원
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
description: exchange online Protection 및 exchange online에서 dkim 서명 된 메시지의 유효성 검사에 대해 자세히 알아보기
ms.openlocfilehash: 7b40769e18c01199669043c42031987695bba639
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223327"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a><span data-ttu-id="75242-103">DKIM으로 서명된 메시지의 유효성 검사 지원</span><span class="sxs-lookup"><span data-stu-id="75242-103">Support for validation of DKIM signed messages</span></span>

<span data-ttu-id="75242-p101">EOP(Exchange Online Protection) 및 Exchange Online은 [DKIM(Domain Keys Identified Mail)](https://www.rfc-editor.org/rfc/rfc6376.txt)) 메시지의 인바운드 유효성 검사를 지원합니다. DKIM은 메시지를 전송한 도메인이 메시지에 표시된 도메인이 맞으며 다른 사람이 스푸핑하지 않았다는 유효성을 증명하는 방법으로, 전자 메일 메시지를 메시지 전송 조직에 연결합니다. DKIM 확인은 IPv6 통신을 통해 전송된 모든 메시지에 자동으로 사용됩니다. IPv6 지원에 대한 자세한 내용은 [IPv6을 통한 익명 인바운드 전자 메일 메시지 지원](support-for-anonymous-inbound-email-messages-over-ipv6.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="75242-p101">Exchange Online Protection (EOP) and Exchange Online support inbound validation of Domain Keys Identified Mail ([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt)) messages. DKIM is a method for validating that a message was sent from the domain it says it originated from and that it was not spoofed by someone else. It ties an email message to the organization responsible for sending it. DKIM verification is automatically used for all messages sent over IPv6 communications. (For more information about IPv6 support, see [Support for anonymous inbound email messages over IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)</span></span>
  
<span data-ttu-id="75242-p102">DKIM은 메시지 헤더의 DKIM 서명 헤더에 표시되는 디지털 서명된 메시지의 유효성을 검사합니다. DKIM 서명 유효성 검사의 결과는 RFC 7001([메시지 인증 상태를 나타내는 메시지 헤더 필드](https://www.rfc-editor.org/rfc/rfc7001.txt))을 준수하는 Authentication-Results 헤더에 스탬프 처리됩니다. 메시지 헤더 텍스트는 다음과 같이 표시됩니다. 여기서는 contoso.com이 보낸 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="75242-p102">DKIM validates a digitally signed message that appears in the DKIM-Signature header in the message headers. The results of a DKIM-Signature validation is stamped in the Authentication-Results header which conforms with RFC 7001 ([Message Header Field for Indicating Message Authentication Status](https://www.rfc-editor.org/rfc/rfc7001.txt)). The message header text appears similar to the following (where contoso.com is the sender):</span></span>
  
 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`
  
<span data-ttu-id="75242-112">관리자는 dkim 유효성 검사의 결과에 Exchange [메일 흐름 규칙](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) (전송 규칙이 라고도 함)을 만들어 필요에 따라 메시지를 필터링 하거나 라우팅할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75242-112">Admins can create Exchange [mail flow rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) (also known as transport rules) on the results of a DKIM validation to filter or route messages as needed.</span></span> 
  

