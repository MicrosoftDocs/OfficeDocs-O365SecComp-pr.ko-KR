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
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a>EOP 대기, 지연 및 반송 메시지 FAQ

이 항목에서는 Microsoft EOP(Exchange Online Protection) 필터링 프로세스 중에 대기, 지연 또는 반송된 메시지에 대한 질문과 대답을 제공합니다.
  
 **Q. 메일이 큐에서 대기하는 이유는 무엇인가요?**
  
A. 서비스에서 배달을 위해 받는 사람에 연결할 수 없는 경우 메시지가 큐에 대기하거나 지연됩니다. 받는 사람 네트워크에서 500 계열 오류가 반환되는 경우에는 메시지가 지연되지 않습니다.
  
 **Q. 메시지는 어떤 방식으로 지연되나요?**
  
A. 받는 사람 서버에 연결할 수 없고 받는 사람의 서버에서 연결 시간 초과, 연결 거부 또는 400 계열 오류와 같은 "일시적인 오류"를 반환하는 경우 메시지가 보류됩니다. 500 계열 오류와 같은 영구 오류가 발생한 경우에는 메시지가 보낸 사람에게 반환됩니다.
  
 **Q. 메시지가 지연 상태로 유지되는 기간 및 다시 시도 간격은 어떻게 되나요?**
  
A. 지연 메시지는 대기열에 2일 동안 유지됩니다. 메시지 다시 시도는 받는 사람의 메일 시스템에서 다시 수신된 오류를 기반으로 합니다. 평균적으로 메시지는 5분마다 다시 시도됩니다.
  
 **Q. 전자 메일 서버가 복원된 경우 큐에 있는 메시지는 어떻게 배포되나요?**
  
A. 전자 메일 서버가 복원된 후 큐에 있는 모든 메시지는 받은 순서 및 서버를 사용할 수 없어 큐에 추가된 순서대로 자동으로 처리됩니다. 
  

