---
title: Office 365 BitLocker 암호화에 대 한
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
description: '클라우드에서 암호화에 대 한 BitLocker 하는 방법에 대 한 요약: 정보입니다.'
ms.openlocfilehash: 86c6bc9282d7c2b0a7d4e08d4636c8f9c2fa5db8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533514"
---
# <a name="bitlocker-and-distributed-key-manager-dkm-for-encryption"></a>암호화에 대한 BitLocker 및 분산 키 관리자(DKM)
BitLocker를 사용 하 여 볼륨 수준에서 보관 된 고객 데이터를 포함 하는 디스크 드라이브를 암호화 하는 office 365 서버. BitLocker 암호화는 Windows에서 기본 제공 되는 데이터 보호 기능입니다. BitLocker에서 다른 프로세스 또는 고객 데이터를 포함 하는 디스크에 대 한 실제 액세스를 사용할 수 있는 사람에 게 발생할 수 있는 컨트롤 (예: 액세스 제어 또는 하드웨어의 재활용)에서 여행 있을 경우 위협 으로부터 보호 하기 위해 사용 되는 기술 중 하나입니다. 이 경우 BitLocker는 분실, 도난 또는 부적절 하 게 폐기 된 컴퓨터와 디스크 인해 데이터 도난 또는 노출 가능성을 제거합니다.

BitLocker는 Exchange Online 고객 데이터를 포함 하는 디스크, SharePoint Online 및 Skype 비즈니스에 대 한 암호화 표준 AES (고급) 256 비트 암호화와 함께 배포 됩니다. 디스크 섹터와 볼륨 암호화 키 (FVEK 전체), 암호화 된 볼륨 마스터 키 (VMK)에 신뢰할 수 있는 플랫폼 모듈 (TPM) 서버에서 차례 대로 바인딩되는 암호화 됩니다. FVEK를 직접 보호 하는 VMK 하 고 있으므로, 중요 한는 VMK 보호 됩니다. 다음 그림에서는 (이 경우 Exchange Online 서버를 사용 하 여)에 지정 된 서버에 대 한 BitLocker 키 보호 체인의 예를 보여줍니다.

다음 표에서 (이 경우 Exchange 온라인 서버)에 지정 된 서버에 대 한 BitLocker 키 보호 체인을 설명합니다.

| 키 보호 기능 | 세분성 | 생성 된 어떻게 합니까? | 여기서 저장 되어 있습니까? | 보호 |
|--------------------------------------------------------------------------------|-------------------------------------------------|----------------|-------------------------|--------------------------------------------------------------------------------------------------|
| AES 256 비트 외부 키 | 서버당 | BitLocker api (영문) | TPM 또는 비밀 안전 하 게 보호 | Lockbox / 액세스 제어 |
|  |  |  | 사서함 서버 레지스트리 | TPM 암호화 |
| 48 자리 숫자 암호 | 디스크당 | BitLocker api (영문) | Active Directory | Lockbox / 액세스 제어 |
| X.509 인증서로 데이터 복구 에이전트 (DRA)이 라고도 공용 키 보호 기능 | 환경 (예: Exchange Online 넌) | Microsoft CA | 시스템 구축 | 없음 한 사용자에 게 개인 키에 전체 암호가 합니다. 암호가 실제 보호 합니다. |


BitLocker 키 관리는 Office 365 데이터 센터에서 암호화 된 디스크의 잠금을 해제/복구 하는데 사용 되는 복구 키의 관리를 포함 합니다. Office 365에서 개별 스크린 및 승인 된 사용자만 액세스할 수 있는 보안된 공유에 마스터 키를 저장 합니다. 키에 대 한 자격 증명 (기능 호출 "secret 저장소"), 액세스 제어 데이터에 대 한 보안된 저장소에 저장 된 수준이 높은 지 적시에 대 한 액세스 권한 상승 도구를 사용 하 여 액세스 권한 상승 및 관리 승인 필요 합니다.

BitLocker는 두 관리 범주로 구분 하는 키를 지원 합니다.
- BitLocker 관리 되는 키를 일반적으로 단기 하 고 서버에 설치 된 운영 체제 인스턴스 수명에 또는 지정한 디스크에 연결 합니다. 이러한 키 삭제 하 고 서버 다시 설치 또는 디스크 서식 중에 다시 설정 됩니다.
- BitLocker 외부의 관리 되 디스크 암호 해독에 사용 되는 BitLocker 복구 키입니다. BitLocker는 운영 체제를 다시 설치 하 고 암호화 된 데이터 디스크 이미 존재 하는 시나리오에 대 한 복구 키를 사용 합니다. 복구 키를 디스크의 잠금을 해제 하려면 모니터링 프로브 Exchange 온라인 응답자를 할 수 있는 관리 되는 상태별으로도 사용 됩니다.

볼륨 마스터 키로 암호화 되는 전체 볼륨 암호화 키를 사용 하는 BitLocker로 보호 된 볼륨 암호화 됩니다. BitLocker는 FIPS 호환 알고리즘을 사용 하 여 암호화 키는 저장 되지 않거나 일반 텍스트로 전송 되도록 합니다. Office 365를 구현 하 고객 데이터에서-나머지-보호 기본 BitLocker 구현에서 파생 하는 것 않습니다 하지 않습니다.