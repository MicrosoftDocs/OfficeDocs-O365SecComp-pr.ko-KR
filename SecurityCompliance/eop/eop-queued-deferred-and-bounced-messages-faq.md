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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256266"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a>EOP 대기, 지연 및 반송 메시지 FAQ

이 항목에서는 Microsoft EOP(Exchange Online Protection) 필터링 프로세스 중에 대기, 지연 또는 반송된 메시지에 대한 질문과 대답을 제공합니다.
  
 **Q. 메일이 큐에서 대기하는 이유는 무엇인가요?**
  
A. 서비스에서 배달을 위해 받는 사람에 연결할 수 없는 경우 메시지가 큐에 대기하거나 지연됩니다. 받는 사람 네트워크에서 500 계열 오류가 반환되는 경우에는 메시지가 지연되지 않습니다.
  
 **Q. 메시지는 어떤 방식으로 지연되나요?**
  
A. 받는 사람 서버에 연결할 수 없고 받는 사람의 서버에서 연결 시간 초과, 연결 거부 또는 400 계열 오류와 같은 "일시적인 오류"를 반환하는 경우 메시지가 보류됩니다. 500 계열 오류와 같은 영구 오류가 발생한 경우에는 메시지가 보낸 사람에게 반환됩니다.
  
 **Q. 메시지가 지연 상태로 유지되는 기간 및 다시 시도 간격은 어떻게 되나요?**
  
A. 지연 메시지는 대기열에 2일 동안 유지됩니다. 메시지 다시 시도는 받는 사람의 메일 시스템에서 다시 수신된 오류를 기반으로 합니다. 처음 몇 개의 deferrals은 15 분 이내 이며 이후 다시 시도 (앞으로 1 ~ 6 일 이상 경과 함)가 경과 하는 간격을 최대 60 분까지 증가 시킵니다. 간격 기간 확장은 동적으로 큐 크기 및 내부 메시지 우선 순위와 같은 여러 가지 변수를 고려 하 여 수행 됩니다. 기본적으로 시작 하는 데 15 분 (이 하)이 소요 되며, 다음 몇 시간 동안 간격으로 확장 하 여 최대 60 분까지 진행 합니다.
  
 **Q. 전자 메일 서버가 복원된 경우 큐에 있는 메시지는 어떻게 배포되나요?**
  
A. 전자 메일 서버가 복원된 후 큐에 있는 모든 메시지는 받은 순서 및 서버를 사용할 수 없어 큐에 추가된 순서대로 자동으로 처리됩니다. 
  

