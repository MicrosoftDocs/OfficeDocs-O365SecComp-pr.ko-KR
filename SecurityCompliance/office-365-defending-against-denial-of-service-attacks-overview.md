---
title: Office 365에서에서 서비스 거부 공격을 방어
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 서비스 거부 (DoS) 공격을 간략하게 설명 합니다.
ms.openlocfilehash: b5a51ae332b32142d9ab993a29763b2160c3ce97
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532891"
---
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a>Office 365에서에서 서비스 거부 공격을 방어

## <a name="introduction"></a>소개
Microsoft는 200 개 이상의 클라우드 서비스에 대 한 Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype, 및 Xbox Live를 포함 하 여이 글로벌 클라우드에서 호스팅되는 신뢰할 수 있는 인프라를 제공 100 개가 넘는 데이터 센터의 인프라를 제공 합니다.

중요 한 인터넷 현재 상태 및 클라우드 서비스를 제공 하는 많은 많이 사용 되 인터넷 속성을 글로벌 조직으로 Microsoft에는 해커 및 기타 악성 개인에 대 한 대규모, 일반적인 대상이 됩니다. 네트워크--클라이언트와 Microsoft 클라우드-간의 통신 계층의 악의적인 공격 가장 큰 목표 중 하나입니다. 실제로 지난 수년간, Microsoft 되었고 지속적으로 영구적으로 네트워크 기반 cyberattack 형태의 아래 있습니다. 거의 항상 공격의 일종을 발생 하는 Microsoft의 인터넷 속성 중 하나 이상이 합니다. 이러한 공격 으로부터 방어 수 있는 안정적이 고 영구 완화 시스템을 하지 않고 Microsoft 클라우드 서비스는 오프 라인 및 고객에 게 사용할 수 없는 것입니다.

Microsoft의 클라우드 서비스 및 네트워크를 보호 하기 위해 심층 방어 보안 원칙을 사용 합니다. 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a>정 및 서비스 거부 공격 증상이 나타날 수 있습니다
네트워크 서비스 공격에 한 가지 방법은 네트워크 및 서버 합법적인 사용자에 게 서비스를 거부 하려면 발생 하는 서비스의 호스트에 대해 많은 요청을 만드는 것입니다. 이것은 서비스 거부 (DoS) 공격을 이라고 합니다. 공격 작업자, 끝점 및/또는 벡터 여러 하 여를 수행 하는 경우에 분산된 서비스 거부 (DDoS) 공격으로 참조 됩니다. 의미, 동기 및 목표에 따라, 다르기는 하지만 DoS 및 DDoS 공격 명 이상의 사용자의 활동을 정상적으로 작동 중에서 또는 모두를 일시적으로 또는 무기한에 인터넷 사이트 또는 서비스를 방지 하기 위해 일반적으로 구성 됩니다.

[미국, 대한민국 컴퓨터 응급 준비 팀](https://www.us-cert.gov/) (미국-CERT) 포함 하는 DoS 공격 증상이 나타날 수 있습니다를 정의 합니다.
- 네트워크 성능을 일반적으로 느린 (때 파일을 열 또는 인터넷 사이트에 액세스)
- 웹사이트의 사용할 수 없습니다.
- 웹사이트에 액세스할 수 없음
- 수신된 스팸에 급격 하 게 증가
- 유선 또는 무선 인터넷 연결의 연결 해제
- 웹 또는 인터넷 서비스에 대 한 액세스의 장기 손실

## <a name="related-topics"></a>관련 항목
- [서비스 거부 공격에 대한 보안 핵심 원칙](office-365-core-principles-of-defense-against-dos-attacks.md)
- [Microsoft의 서비스 거부 방어 전략](office-365-microsoft-dos-defense-strategy.md)
- [Microsoft 클라우드 서비스 서비스 거부 공격을 방어](office-365-defending-cloud-services-against-dos-attacks.md)
