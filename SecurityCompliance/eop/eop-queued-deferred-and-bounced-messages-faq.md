---
title: EOP 대기, 지연 및 반송 메시지 FAQ
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 9d015a0d-52a0-484d-9a08-121d04f973d3
description: 이 항목에서는 Microsoft EOP(Exchange Online Protection) 필터링 프로세스 중에 대기, 지연 또는 반송된 메시지에 대한 질문과 대답을 제공합니다.
ms.openlocfilehash: 17e5955195c4e38299712fb9161822984b2a643a
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026225"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a><span data-ttu-id="a3142-103">EOP 대기, 지연 및 반송 메시지 FAQ</span><span class="sxs-lookup"><span data-stu-id="a3142-103">EOP queued, deferred, and bounced messages FAQ</span></span>

<span data-ttu-id="a3142-104">이 항목에서는 Microsoft EOP(Exchange Online Protection) 필터링 프로세스 중에 대기, 지연 또는 반송된 메시지에 대한 질문과 대답을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a3142-104">This topic provides answers to frequently asked questions about messages that have been queued, deferred, or bounced during the Microsoft Exchange Online Protection (EOP) filtering process.</span></span>
  
 <span data-ttu-id="a3142-105">**Q. 메일이 큐에서 대기하는 이유는 무엇인가요?**</span><span class="sxs-lookup"><span data-stu-id="a3142-105">**Q. Why is mail queuing?**</span></span>
  
<span data-ttu-id="a3142-p101">A. 서비스에서 배달을 위해 받는 사람에 연결할 수 없는 경우 메시지가 큐에 대기하거나 지연됩니다. 받는 사람 네트워크에서 500 계열 오류가 반환되는 경우에는 메시지가 지연되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3142-p101">A. Messages are queued or deferred if the service is unable to make a connection to the recipient server for delivery. It will not defer messages if a 500-series error is returned from the recipient network.</span></span>
  
 <span data-ttu-id="a3142-109">**Q. 메시지는 어떤 방식으로 지연되나요?**</span><span class="sxs-lookup"><span data-stu-id="a3142-109">**Q. How does a message become deferred?**</span></span>
  
<span data-ttu-id="a3142-p102">A. 받는 사람 서버에 연결할 수 없고 받는 사람의 서버에서 연결 시간 초과, 연결 거부 또는 400 계열 오류와 같은 "일시적인 오류"를 반환하는 경우 메시지가 보류됩니다. 500 계열 오류와 같은 영구 오류가 발생한 경우에는 메시지가 보낸 사람에게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3142-p102">A. Messages will be held when a connection to the recipient server cannot be made and the recipient's server is returning a "temporary failure" such as a connection time-out, connection refused, or a 400-series error. If there is a permanent failure, such as a 500-series error, then the message will be returned to the sender.</span></span>
  
 <span data-ttu-id="a3142-113">**Q. 메시지가 지연 상태로 유지되는 기간 및 다시 시도 간격은 어떻게 되나요?**</span><span class="sxs-lookup"><span data-stu-id="a3142-113">**Q. How long does a message remain in deferral and what is the retry interval?**</span></span>
  
<span data-ttu-id="a3142-p103">A. 지연 메시지는 대기열에 2일 동안 유지됩니다. 메시지 다시 시도는 받는 사람의 메일 시스템에서 다시 수신된 오류를 기반으로 합니다. 평균적으로 메시지는 5분마다 다시 시도됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3142-p103">A. Messages in deferral will remain in our queues for 2 days. Message retry attempts are based on the error we get back from the recipient's mail system. On average, messages are retried every 5 minutes.</span></span>
  
 <span data-ttu-id="a3142-118">**Q. 전자 메일 서버가 복원된 경우 큐에 있는 메시지는 어떻게 배포되나요?**</span><span class="sxs-lookup"><span data-stu-id="a3142-118">**Q. After your email server is restored, how are queued messages distributed?**</span></span>
  
<span data-ttu-id="a3142-p104">A. 전자 메일 서버가 복원된 후 큐에 있는 모든 메시지는 받은 순서 및 서버를 사용할 수 없어 큐에 추가된 순서대로 자동으로 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3142-p104">A. After your email server is restored, all queued messages are automatically processed in the order in which they were received and queued when the server became unavailable.</span></span> 
  

