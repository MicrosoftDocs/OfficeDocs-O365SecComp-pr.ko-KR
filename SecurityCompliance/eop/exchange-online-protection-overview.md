---
title: Exchange Online Protection 개요
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 1270a65f-ddc3-4430-b500-4d3a481efb1e
description: Microsoft EOP(Exchange Online Protection)는 스팸 및 맬웨어로부터 조직을 보호하는 클라우드 기반 전자 메일 필터링 서비스로, 메시징 정책 위반으로부터 조직을 보호하는 기능을 포함합니다.
ms.openlocfilehash: 89852c7ba211ccb266c8b231b00d3d83987a5f20
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026695"
---
# <a name="exchange-online-protection-overview"></a>Exchange Online Protection 개요

Microsoft EOP(Exchange Online Protection)는 스팸 및 맬웨어로부터 조직을 보호하는 클라우드 기반 전자 메일 필터링 서비스로, 메시징 정책 위반으로부터 조직을 보호하는 기능을 포함합니다. EOP를 사용하면 메시징 환경을 간편하게 관리할 수 있으며 온-프레미스 하드웨어와 소프트웨어 유지 관리 시의 작업 부담을 상당 부분 덜 수 있습니다.
  
기본적으로 다음과 같은 방식을 통해 메시징 보호에 EOP를 사용할 수 있습니다.
  
- **독립 실행형 시나리오에서** EOP는 클라우드 기반 전자 메일 보호 온-프레미스 Microsoft Exchange Server 2013 환경, 레거시 Exchange Server 버전에 대해 또는 모든 기타 온-프레미스에 대 한 SMTP 전자 메일 솔루션을 제공합니다. 
    
- **Microsoft Exchange Online의 일부로** 기본적으로 EOP는 Microsoft Exchange Online 클라우드 호스팅 사서함을 보호합니다. 
    
- **하이브리드 배포에서** 온-프레미스 사서함과 클라우드 사서함을 함께 사용하는 경우 메시징 환경을 보호하고 메일 라우팅을 제어하도록 EOP를 구성할 수 있습니다. 
    
## <a name="how-eop-works"></a>EOP의 작동 방식

EOP가 받는 전자 메일을 처리하는 방법을 확인하면 EOP의 작동 방식을 이해하는 데 도움이 됩니다.
  
![EOP 전자 메일 처리](../media/EOP-email-processing.png)
  
처음 들어오는 메시지 보낸 사람의 신뢰도 검사 하 고 맬웨어에 대 한 메시지를 검사 하는 연결 필터링을 통해 전달 합니다. 대부분의 스팸이 시점에서 중지 이며 EOP에 의해 삭제 됩니다. 정책 필터링 메시지를 만들거나 서식 파일에서 적용 하는 사용자 지정 전송 규칙에 대해 계산 되는 위치를 통해 메시지를 계속 합니다. 예, 특정 사용자가 보낸에서 메일 도착 했을 때 관리자에 게 알림을 전송 하는 규칙을 가질 수 있습니다. (데이터 손실 방지 검사에도 발생할이 시점 기능, 기능 사용 가능 여부에 대 한 정보를 [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619)을 참조 하는 경우.) 다음으로 메시지를 전달 콘텐츠 필터링을 통해 콘텐츠를 스팸에 용어 또는 공통 된 속성에 대 한 검사 합니다. 메시지가 스팸 콘텐츠 필터에 의해 사용자의 정크 메일 폴더로 또는 설정에 따라 다른 옵션 중에서 격리를 보낼 수를 결정 합니다. 지나면 메시지 이러한 보호 계층의 모든 성공적으로 받는 사람에 게 배달 됩니다.
  
### <a name="eop-datacenters"></a>EOP 데이터 센터

EOP는 최고 수준의 사용 가능성을 제공하도록 설계된 전 세계 데이터 센터 네트워크에서 실행됩니다. 예를 들어 데이터 센터를 사용할 수 없더라도 서비스 중단 없이 전자 메일 메시지가 다른 데이터 센터에 자동으로 라우팅됩니다. 각 데이터 센터의 서버는 사용자 대신 메시지를 수락하여 조직과 인터넷을 분리하는 계층을 제공함으로써 서버의 부하를 줄여 줍니다. 이처럼 가용성이 뛰어난 네트워크를 통해 Microsoft는 전자 메일이 제때에 조직으로 배달되도록 할 수 있습니다. 
  
EOP는 특정 지역 내에서만 데이터 센터 간 부하 분산을 수행합니다. 단일 지역에서 프로비전되는 경우에는 해당 영역에 대한 메일 라우팅을 사용하여 모든 메시지가 처리됩니다. 다음 목록에는 EOP 데이터 센터에 대한 영역 메일 라우팅의 작동 방식이 나와 있습니다.
  
- 미국 내에서 모든 Exchange Online 데이터 센터 브라질 및 칠레에서 사용 하는 및 캐나다의 데이터 센터 캐나다에서 사용 되는 위치 남아메리카를 제외 하 고 미국 데이터 센터에서 사서함이 있어야 합니다. 모든 전자 메일 메시지, 남아메리카 및 캐나다의 경우에 고객에 대 한 메시지를 포함 하 여 EOP 필터링;에 대 한 미국 데이터 센터를 통해 라우팅됩니다. 그러나 quaratined 전자 메일 테 넌 트 위치한 데이터 센터에 저장 됩니다.
    
- EMEA(유럽, 중동 및 아프리카)에서는 모든 Exchange Online 사서함이 EMEA 데이터 센터에 있으며 모든 메시지가 EOP 필터링용으로 EMEA 데이터 센터를 통해 라우팅됩니다.
    
- APAC(아시아 태평양)에서는 모든 Exchange Online 사서함이 APAC 데이터 센터에 있으나 메시지는 현재 EOP 필터링용으로 EMEA 데이터 센터를 통해 라우팅됩니다. 이러한 라우팅은 2014년 4분기에 변경될 예정이며, 그러면 메시지가 EOP 필터링용으로 APAC 데이터 센터를 통해 라우팅됩니다.
    
- GCC(정부 커뮤니티 클라우드)의 경우에는 모든 Exchange Online 사서함이 미국 데이터 센터에 있으며 모든 메시지는 EOP 필터링용으로 미국 데이터 센터를 통해 라우팅됩니다.
    
## <a name="eop-plans-and-features"></a>EOP 계획 및 기능

다음은 사용 가능한 EOP 구독 계획입니다.
  
- **EOP 독립 실행형** EOP가 온-프레미스 사서함을 보호합니다. 
    
- **Exchange Online의 EOP 기능** EOP가 Exchange Online 클라우드 호스팅 사서함을 보호합니다. 
    
- **Exchange Enterprise CAL with Services** EOP가 EOP 독립 실행형과 마찬가지로 온-프레미스 사서함을 보호하고 웹 서비스를 사용한 DLP(데이터 손실 방지) 및 보고 기능이 포함됩니다. 
    
모든 EOP 구독 계획의 요구 사항, 중요 제한 및 기능 가용성에 대한 자세한 내용은 [Exchange Online Protection 서비스 설명](https://go.microsoft.com/fwlink/p/?LinkId=320619)을 참조하세요.
  
## <a name="setting-up-eop"></a>EOP 설정

EOP는 간단하게 설정할 수 있으며, 특히 준수 규칙이 많지 않은 소규모 조직의 경우에는 더욱 그렇습니다. 그러나 도메인이 여러 개이거나 사용자 지정 준수 규칙 또는 하이브리드 메일 흐름을 사용하는 대규모 조직의 경우에는 EOP 설정에 더 많은 시간과 계획이 필요할 수 있습니다.
  
EOP를 이미 구입한 경우 [EOP 서비스 설정](set-up-your-eop-service.md)을 참조하여 메시징 환경을 보호하도록 EOP를 구성하는 데 필요한 모든 단계를 완료하십시오. 
  
## <a name="for-more-information"></a>자세한 내용

[EOP 기능](eop-features.md)
  
[EOP 시작을 위한 비디오](videos-for-getting-started-with-eop.md)
  
[EOP 관련 일반 FAQ(질문과 대답)](eop-general-faq.md)
  
[EOP 대기, 지연 및 반송 메시지 FAQ](eop-queued-deferred-and-bounced-messages-faq.md)
  
[위임된 관리 FAQ](delegated-administration-faq.md)
  
[EOP 조직 간에 도메인 및 설정 이동](move-domains-and-settings-from-one-eop-organization-to-another-eop-organization.md)
  

