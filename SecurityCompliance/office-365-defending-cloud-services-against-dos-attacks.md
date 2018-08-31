---
title: Office 365 방어 클라우드 서비스 서비스 거부 공격
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
description: 어떻게 Microsoft 클라우드 서비스 서비스 거부 (DoS) 공격을 방어 합니다.
ms.openlocfilehash: f11a4293a35de4d36fd38fce892a4e59919111cc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533610"
---
# <a name="defending-microsoft-cloud-services-against-denial-of-service-attacks"></a>Microsoft 클라우드 서비스 서비스 거부 공격을 방어

## <a name="introduction"></a>소개
Microsoft 데이터 센터 경계 펜스, 비디오 카메라, 보안 담당자 및 생체 인식, 스마트 카드, 및 다단계 인증을 사용 하는 보안 출입구를 포함 하는 유가 증권 방어에 의해 보호 됩니다. 심층 방어 보안 기능 및 각 실제 서버 단위에 모든 영역을 통해 계속 진행합니다. [Microsoft 클라우드 인프라 및 작업 그룹은](https://www.microsoft.com/en-us/cloud-platform/global-datacenters) 클라우드 서비스에 대 한 기본적인 기술과 핵심 인프라를 제공합니다. 데이터 센터 물리적 보안 및 안정성에 대 한 업계 표준을 준수 하 고 관리 하는, 모니터링 되며 Microsoft 작업 담당자가 관리 합니다.

클라우드 서비스를 추가로 보호 하려면 Microsoft Microsoft Azure 연속 모니터링 및 통과 테스트 프로세스의 일부인 DDoS 방어 시스템을 제공 합니다. Azure DDoS 방어 시스템은 외부의 하지만 다른 Azure 테 넌 트의 공격에 대응 하는 데에이 아니라 설계 됩니다. Azure는 DDoS 공격 으로부터 보호 하기 위해 표준 검색 및 단축 기술 SYN 쿠키, 제한, 속도 및 연결 제한 등을 사용 합니다.

Microsoft의 클라우드 서비스는 여러 소스의 공격의 위협에 따라 달라 집니다. 완화 및 높은 확장 가능성 및 동적 Azure 기반 위협 검색 및 완화 다양 한 DoS 위협 으로부터 보호 하려면 시스템 개발 및 구현 된 DoS 공격 으로부터 기반이 되는 인프라를 보호 하는 기본 목표와 및 클라우드를 위한 서비스 중단을 방지 하기 위해 돕는 고객 서비스. 인바운드, 아웃 바운드 및 지역-트래픽을 보호 하는 DoS Azure 완화 시스템입니다.

대부분의 DoS 공격 [Open 시스템 간 상호 연결](https://docs.microsoft.com/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) (OSI) 모델의 (L4) 계층 (l 3) 네트워크 및 전송에서 목표를 충족 하는지 시작 합니다. L 3 및 L4 레이어를 요청 하는 공격은 네트워크 인터페이스 또는 서비스 리소스 과부하 및 거부 합법적인 트래픽에 응답 하는 기능에 대 한 공격 트래픽이와 대량의 설계 되었습니다. 특히, l 3 및 L4 공격 하려고 네트워크 링크, 장치, 또는 서비스의 용량을 완전히 포화 또는 서버 또는 응용 프로그램을 지 원하는 가상 컴퓨터의 cpu가 발생 합니다.

Microsoft는 설계, 개발, 하 고 배포 솔루션을 3 및 L4 공격 으로부터 목표로 특히 이러한 레이어를 보호 함으로써 공격을 받고 비추도록 인프라 및 고객 목표를 보호 합니다. 인프라를 보호 한 고객을 위한 공격 트래픽 참고 자료 수 없는 손상이 발생 하지 않습니다 보장 또는 다른 고객을 위한 서비스의 네트워크 품질은 감소 합니다. 솔루션은 데이터 센터 라우터에서 트래픽 샘플링 데이터를 사용 합니다. 네트워크 공격을 감지 하는 서비스를 모니터링 하 여이 데이터를 분석 합니다. 공격이 감지 되 면 자동화 방어 메커니즘 퇴장 시킵니다.

## <a name="application-level-defenses"></a>응용 프로그램 수준 방어
Microsoft 엔지니어링 팀의 고객 데이터를 보호 하려면 [Microsoft 운영 보안을 보장](https://www.microsoft.com/en-us/SDL/OperationalSecurityAssurance) 하 여 설정 하는 엄격한 표준을 따릅니다. Microsoft의 클라우드 서비스는 의도적으로 보호 하 고 응용 프로그램 수준 DoS 공격을 완화에 대 한도 매우 높은 부하를 지원 하기 위해 제작 됩니다. 지역 격리 및 작업의 일부 기능을 제한 하는 여러 글로벌 데이터 센터 서비스는 분산 수평 확장 된 아키텍처를 구현 했습니다.

각 고객의 국가 또는 지역 고객의 관리자는 서비스의 초기 설치 하는 동안를 식별 하는 해당 고객의 데이터에 대 한 기본 저장소 위치를 결정 합니다. 고객 데이터는 주/백업 전략에 따라 중복 데이터 센터 간에 복제 됩니다. 기본 데이터 센터는 소프트웨어에서 실행 되는 모든 기본 고객 데이터와 함께 응용 프로그램 소프트웨어를 호스팅합니다. 백업 데이터 센터 자동 장애 조치를 제공합니다. 기본 데이터 센터에서 어떤 이유로 든 작동 하지, 백업 데이터 센터의 소프트웨어 및 고객 데이터의 복사본을 요청이 리디렉션됩니다. 언제 든 지 기본 또는 백업 데이터 센터에서 고객 데이터를 처리할 수 있습니다. 하나의 데이터 센터는 공격을 하는 경우 영향을 받는 노출 영역을 축소 여러 데이터 센터에서 데이터를 배포 합니다. 또한 영향을 받는 데이터 센터의 서비스는 신속 하 게 리디렉션될 수 보조 데이터 센터에 대 한 복구 메커니즘 및 그 중 하나로 (서비스 복원 되 면 다시 기본 데이터 센터로 리디렉션됩니다) 반대의 경우도 마찬가지입니다.

개별 작업 리소스 사용률을 관리 하는 기본 제공 기능을 포함 합니다. 예는 Exchange Online 메커니즘을 제한 하 고 SharePoint Online에 다중 계층된 접근 방법 DoS 공격에 대 한 방어에 포함 됩니다. 자원은 Active Directory, Exchange Online 정보 저장소 또는 다른 곳에 있는지 여부는 최종 사용자가 사용 되는 리소스 수준에 따라은 Exchange Online 사용자에 대 한 제한 합니다. 사용자가 사용 하는 리소스를 제한 하려면 각 클라이언트에 할당 되는 예산입니다. Exchange Online 사용자 활동 및 시스템 구성 요소에 대 한 제한 기반으로 [작업 부하 관리](http://technet.microsoft.com/en-us/library/jj150503(v=exchg.150).aspx)합니다. Exchange Online 작업에는 Exchange Online 기능, 프로토콜, 또는 Exchange Online 시스템 리소스 관리 하기 위해 명시적으로 정의 하는 서비스입니다. CPU, 사서함 데이터베이스 작업 같은 시스템 리소스를 필요로 하는 Exchange Online의 각 작업 또는 Active Directory 작업 배경 또는 사용자 요청을 수행 하도록 요청 합니다. Exchange Online 작업의 예는 웹 서버, Exchange ActiveSync, 사서함 마이그레이션 및 사서함 도우미에서 Outlook을 포함합니다. 테 넌 트 관리자는 Exchange 작업 부하 관리 제한 Exchange 관리 셸을 사용 하 여 사용자에 대 한 설정을 관리할 수 있습니다. Exchange Online PowerShell, Exchange 웹 서비스 및 POP 및 IMAP, Exchange ActiveSync, 모바일 장치 연결, 받는 사람, 등을 포함 하 여 내에서 구현 된 하는 제한 하는 다양 한 형태의 있습니다. 온-프레미스 Exchange 배포의 관리자 수 제한 정책, 구성 하는 동안 관리자가 Exchange Online에 대 한 제한 정책을 구성할 수 없습니다.

SharePoint Online에서 제한에 대 한 가장 일반적인 트리거는 너무 많음 주파수에서 너무 많은 작업을 수행 하는 클라이언트쪽 개체 모델 (CSOM) 코드입니다. CSOM을 함께 사용 한도 초과 하 고 사용자 당 제한 발생할 수 있는 단일 요청을 많은 작업을 수행할 수 있습니다.

활동에 관계 없이 사용자 같은 추가 요청 해당 사용자 계정에서 일반적으로 짧은 기간에 대 한 SharePoint Online 제한 하 여 사용 현황 제한을 초과 하는 경우 제한 될 수 있습니다. 사용자 제한을 적용 하는 동안 다음 조건에 따라 스로틀 만료 될 때까지 해당 사용자가 모든 작업 제한 됩니다.
- 브라우저에서 직접 사용자에 의해 수행 하는 요청에 대 한 제한 정보 페이지에 SharePoint Online에서 리디렉션합니다 및 된 요청이 실패 합니다.
- CSOM 통화를 포함 하 여 다른 모든 요청에 대 한 SharePoint Online HTTP 상태 코드 429 ("너무 많은 요청")를 반환 하 고는 요청에 실패 합니다.

사용 현황 제한을 초과 하는 문제를 일으키는 프로세스 계속 되 면 SharePoint Online 될 수 있습니다 완전히 하는 프로세스를 차단 하 고 HTTP 상태 코드 503 ("서비스 사용할 수 없음")를 반환 합니다.

## <a name="vulnerability-and-penetration-testing"></a>취약점 및 통과 테스트
Microsoft는 다양 한 [보안 기술과 사례](https://www.microsoft.com/en-us/trustcenter/security/threatmanagement) 맬웨어 방지 구성 요소 및 가상 클라우드 서비스에 대 한 서비스를 사용 하는 등의 현대, 정교한 위협에 대 한 [해당 클라우드 인프라를 보호](https://blogs.technet.microsoft.com/hybridcloud/2015/05/05/protecting-your-datacenter-and-cloud-from-emerging-threats/) 하 고 온-프레미스 네트워크로 컴퓨터 (Vm) 및 기타 시스템입니다. 네트워크, 시스템 및 사용자에 대 한 기본 사용 패턴을 모니터링 하 고 테스트 하는 일반, 및 일반 통과 활용 하는 모든 동작에 플래그를 지정 하려면 학습 하는 컴퓨터에서 사용 하는 고급 위협 분석 합니다.

통과 테스트를 수행 하 고 고객에 게 제공 하는 [Microsoft 클라우드 통합 통과 테스트 프로그램](https://technet.microsoft.com/en-us/mt784683)외에 또한 관여할의 일반 취약점 평가 수행 하는 타사 보안 전문가 및 클라우드 서비스에 대 한 테스트를 통과 합니다. 이러한 타사 취약점 평가에서 보고서에서 사용할 수 있도록 다운로드에 대 한 [서비스를 신뢰](https://aka.ms/STP) 하 고 [서비스 보증](https://aka.ms/ServiceAssurance) 포털.
