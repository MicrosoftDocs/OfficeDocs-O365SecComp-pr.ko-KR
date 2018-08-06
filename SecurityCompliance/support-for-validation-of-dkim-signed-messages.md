---
title: DKIM으로 서명된 메시지의 유효성 검사 지원
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
description: EOP(Exchange Online Protection) 및 Exchange Online은 DKIM(Domain Keys Identified Mail)) 메시지의 인바운드 유효성 검사를 지원합니다. DKIM은 메시지를 전송한 도메인이 메시지에 표시된 도메인이 맞으며 다른 사람이 스푸핑하지 않았다는 유효성을 증명하는 방법으로, 전자 메일 메시지를 메시지 전송 조직에 연결합니다. DKIM 확인은 IPv6 통신을 통해 전송된 모든 메시지에 자동으로 사용됩니다. IPv6 지원에 대한 자세한 내용은 IPv6을 통한 익명 인바운드 전자 메일 메시지 지원을 참조하세요.
ms.openlocfilehash: 0fafc5a4754309f8f467a712f934fea3067b660d
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026155"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a><span data-ttu-id="0fd16-107">DKIM으로 서명된 메시지의 유효성 검사 지원</span><span class="sxs-lookup"><span data-stu-id="0fd16-107">Support for validation of DKIM signed messages</span></span>

<span data-ttu-id="0fd16-p102">EOP(Exchange Online Protection) 및 Exchange Online은 [DKIM(Domain Keys Identified Mail)](https://www.rfc-editor.org/rfc/rfc6376.txt)) 메시지의 인바운드 유효성 검사를 지원합니다. DKIM은 메시지를 전송한 도메인이 메시지에 표시된 도메인이 맞으며 다른 사람이 스푸핑하지 않았다는 유효성을 증명하는 방법으로, 전자 메일 메시지를 메시지 전송 조직에 연결합니다. DKIM 확인은 IPv6 통신을 통해 전송된 모든 메시지에 자동으로 사용됩니다. IPv6 지원에 대한 자세한 내용은 [IPv6을 통한 익명 인바운드 전자 메일 메시지 지원](support-for-anonymous-inbound-email-messages-over-ipv6.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0fd16-p102">Exchange Online Protection (EOP) and Exchange Online support inbound validation of Domain Keys Identified Mail ([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt)) messages. DKIM is a method for validating that a message was sent from the domain it says it originated from and that it was not spoofed by someone else. It ties an email message to the organization responsible for sending it. DKIM verification is automatically used for all messages sent over IPv6 communications. (For more information about IPv6 support, see [Support for anonymous inbound email messages over IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)</span></span>
  
<span data-ttu-id="0fd16-p103">DKIM은 메시지 헤더의 DKIM 서명 헤더에 표시되는 디지털 서명된 메시지의 유효성을 검사합니다. DKIM 서명 유효성 검사의 결과는 RFC 7001([메시지 인증 상태를 나타내는 메시지 헤더 필드](https://www.rfc-editor.org/rfc/rfc7001.txt))을 준수하는 Authentication-Results 헤더에 스탬프 처리됩니다. 메시지 헤더 텍스트는 다음과 같이 표시됩니다. 여기서는 contoso.com이 보낸 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="0fd16-p103">DKIM validates a digitally signed message that appears in the DKIM-Signature header in the message headers. The results of a DKIM-Signature validation is stamped in the Authentication-Results header which conforms with RFC 7001 ([Message Header Field for Indicating Message Authentication Status](https://www.rfc-editor.org/rfc/rfc7001.txt)). The message header text appears similar to the following (where contoso.com is the sender):</span></span>
  
 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`
  
<span data-ttu-id="0fd16-116">관리자는 DKIM 유효성 검사의 결과에 대해 Exchange [Transport Rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx)을 만들어 필요에 따라 메시지를 필터링하거나 라우팅할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fd16-116">Admins can create Exchange [Transport Rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) on the results of a DKIM validation to filter or route messages as needed.</span></span> 
  

