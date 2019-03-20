---
title: EOP 대기, 지연 및 반송 메시지 FAQ
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 9d015a0d-52a0-484d-9a08-121d04f973d3
description: 이 항목에서는 Microsoft EOP(Exchange Online Protection) 필터링 프로세스 중에 대기, 지연 또는 반송된 메시지에 대한 질문과 대답을 제공합니다.
ms.openlocfilehash: e8fdb07d11a1f540e94b82730eb848a97f51523a
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693207"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a><span data-ttu-id="42983-103">EOP 대기, 지연 및 반송 메시지 FAQ</span><span class="sxs-lookup"><span data-stu-id="42983-103">EOP queued, deferred, and bounced messages FAQ</span></span>

<span data-ttu-id="42983-104">이 항목에서는 Microsoft EOP(Exchange Online Protection) 필터링 프로세스 중에 대기, 지연 또는 반송된 메시지에 대한 질문과 대답을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="42983-104">This topic provides answers to frequently asked questions about messages that have been queued, deferred, or bounced during the Microsoft Exchange Online Protection (EOP) filtering process.</span></span>
  
 <span data-ttu-id="42983-105">**Q. 메일이 큐에서 대기하는 이유는 무엇인가요?**</span><span class="sxs-lookup"><span data-stu-id="42983-105">**Q. Why is mail queuing?**</span></span>
  
<span data-ttu-id="42983-p101">A. 서비스에서 배달을 위해 받는 사람에 연결할 수 없는 경우 메시지가 큐에 대기하거나 지연됩니다. 받는 사람 네트워크에서 500 계열 오류가 반환되는 경우에는 메시지가 지연되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42983-p101">A. Messages are queued or deferred if the service is unable to make a connection to the recipient server for delivery. It will not defer messages if a 500-series error is returned from the recipient network.</span></span>
  
 <span data-ttu-id="42983-109">**Q. 메시지는 어떤 방식으로 지연되나요?**</span><span class="sxs-lookup"><span data-stu-id="42983-109">**Q. How does a message become deferred?**</span></span>
  
<span data-ttu-id="42983-p102">A. 받는 사람 서버에 연결할 수 없고 받는 사람의 서버에서 연결 시간 초과, 연결 거부 또는 400 계열 오류와 같은 "일시적인 오류"를 반환하는 경우 메시지가 보류됩니다. 500 계열 오류와 같은 영구 오류가 발생한 경우에는 메시지가 보낸 사람에게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="42983-p102">A. Messages will be held when a connection to the recipient server cannot be made and the recipient's server is returning a "temporary failure" such as a connection time-out, connection refused, or a 400-series error. If there is a permanent failure, such as a 500-series error, then the message will be returned to the sender.</span></span>
  
 <span data-ttu-id="42983-113">**Q. 메시지가 지연 상태로 유지되는 기간 및 다시 시도 간격은 어떻게 되나요?**</span><span class="sxs-lookup"><span data-stu-id="42983-113">**Q. How long does a message remain in deferral and what is the retry interval?**</span></span>
  
<span data-ttu-id="42983-114">A.</span><span class="sxs-lookup"><span data-stu-id="42983-114">A.</span></span> <span data-ttu-id="42983-115">지연 메시지는 대기열에 2일 동안 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="42983-115">Messages in deferral will remain in our queues for 2 days.</span></span> <span data-ttu-id="42983-116">메시지 다시 시도는 받는 사람의 메일 시스템에서 다시 수신된 오류를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="42983-116">Message retry attempts are based on the error we get back from the recipient's mail system.</span></span> <span data-ttu-id="42983-117">처음 몇 개의 deferrals은 15 분 이내 이며 이후 다시 시도 (앞으로 1 ~ 6 일 이상 경과 함)가 경과 하는 간격을 최대 60 분까지 증가 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="42983-117">The first few deferrals are 15 minutes or less, with subsequent retries (over the next half dozen or so) increasing the interval over multiple retries to a max of 60 minutes.</span></span> <span data-ttu-id="42983-118">간격 기간 확장은 동적으로 큐 크기 및 내부 메시지 우선 순위와 같은 여러 가지 변수를 고려 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42983-118">The interval duration expansion is dynamic, taking into consideration multiple variables like queue sizes and internal message priority.</span></span> <span data-ttu-id="42983-119">기본적으로 시작 하는 데 15 분 (이 하)이 소요 되며, 다음 몇 시간 동안 간격으로 확장 하 여 최대 60 분까지 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="42983-119">In basic, it's 15 minutes (or less) to start, then expanding from there over the next few hours to 60 mins max.</span></span>
  
 <span data-ttu-id="42983-120">**Q. 전자 메일 서버가 복원된 경우 큐에 있는 메시지는 어떻게 배포되나요?**</span><span class="sxs-lookup"><span data-stu-id="42983-120">**Q. After your email server is restored, how are queued messages distributed?**</span></span>
  
<span data-ttu-id="42983-p104">A. 전자 메일 서버가 복원된 후 큐에 있는 모든 메시지는 받은 순서 및 서버를 사용할 수 없어 큐에 추가된 순서대로 자동으로 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="42983-p104">A. After your email server is restored, all queued messages are automatically processed in the order in which they were received and queued when the server became unavailable.</span></span> 
  

