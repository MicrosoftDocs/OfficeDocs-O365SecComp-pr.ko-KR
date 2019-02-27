---
title: 보낸 사람이 아웃 바운드 스팸을 보내는 것이 차단 된 경우의 예제 알림
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c33fd406-a4c8-4ac8-ad85-123996c5cded
ms.collection:
- M365-security-compliance
description: 아웃 바운드 스팸 보내기로 인해 서비스에서 보낸 사람이 차단 되는 경우 아웃 바운드 스팸 정책을 구성할 때 지정한 도메인 관리자는 다음과 같은 알림 전자 메일을 받게 됩니다.
ms.openlocfilehash: 94af965505f7541600a6cd7937ae881226a2ac79
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275478"
---
# <a name="sample-notification-when-a-sender-is-blocked-sending-outbound-spam"></a>보낸 사람이 아웃 바운드 스팸을 보내는 것이 차단 된 경우의 예제 알림

아웃 바운드 스팸 보내기로 인해 서비스에서 보낸 사람이 차단 되는 경우 [아웃 바운드 스팸 정책을 구성할](configure-the-outbound-spam-policy.md) 때 지정한 도메인 관리자는 다음과 같은 알림 전자 메일을 받게 됩니다. 
  
 **보낸 사람 주소:** spamalerts@microsoft.com 
  
 **제목:** 아웃 바운드 스팸 알림 \<-아웃 바운드 메일을 보낼 때 차단 되는 *계정 이름* \>     
  
 **본문:** 이 메시지는 Exchange Online Protection 스팸 분석 시스템에서 자동화 된 회신입니다. 
  
스팸으로 표시 된 대량의 전자 메일 또는 조직에서 보낸 기타 의심 스러운 동작을 검색 했기 때문에 연락을 받고 있습니다. 다음 전자 메일 계정이 전자 메일을 보내지 못하도록 차단 되었습니다 (전자 메일이 계속 수신 될 수 있음).
  
\<*계정 이름*  \> 
  
이 전자 메일 계정이 손상 되었을 가능성이 있습니다. 다음 단계를 수행 하세요.
  
1. 다음을 통해이 문제를 해결 합니다.
    
  - 계정의 암호 변경
    
  - 계정이 손상 된 방식을 확인 합니다.
    
  - 이 취약점이 다시 악용 되지 않도록 주의 해야 합니다.
    
  - 아웃 바운드 메일 큐가 모든 잘못 된 메시지를 지우도록 확인
    
2. 일반 연락처 채널을 사용 하 여 Microsoft 지원에 문의 합니다.
    
3. 메일을 보낼 수 없도록 차단 되 고 문제가 처리 되었음을 사용자에 게 설명 합니다.
    
4. 에이전트는 사용자가 제공한 정보를 사용 하 여 지원 티켓을 만들고이를 에스컬레이션 하 여 전자 메일 주소 또는 도메인이 차단 되지 않도록 합니다.
    
5. 주소가 차단 해제 되 고 다른 문제가 보류 되지 않은 후에는 연결 되 고 차단 해제에 대 한 경고가 표시 됩니다.
    
원치 않는 전자 메일 제어에 대 한 microsoft의 지원 주셔서 감사 합니다.
  
Exchange Online Protection
  
\*\*참고-이 전자 메일을 모니터링 되지 않은 주소로 전송 하 여이 이메일에 응답 하지 마세요.\*\*
  
> [!TIP]
> 또한 [도움말 및 EOP 지원](eop/help-and-support-for-eop.md)에서 설명 하는 옵션을 통해 지원에 문의할 수 있습니다. 
  

