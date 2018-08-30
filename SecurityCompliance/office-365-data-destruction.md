---
title: Office 365 데이터 파괴
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
description: Microsoft의 정책 재활용, 삭제, 또는 파괴 하면 Office 365 데이터 센터 디스크 드라이브와 서버에 대 한 개요입니다.
ms.openlocfilehash: c9950be4919520f2f46badaa4a7d4cfce5c55b45
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533240"
---
# <a name="office-365-data-destruction"></a>Office 365 데이터 파괴
Microsoft는 휴지통 및 디스크 드라이브와 사용 하지 않도록 설정 또는 실패 한 서버의 폐기를 해결 하는 데이터 처리 표준 정책을 있습니다. Microsoft은 Office 365 내에 모든 디스크 드라이브를 다시 사용 하기 전에 국가 Institute 표준 및 기술 특별 한 발행물 800-88 ([NIST SP 800 88 지침 미디어 정리에 대 한](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf) 일치 하는 실제 정리 프로세스를 수행 ). Office 365에 모든 디스크 드라이브 BitLocker 볼륨 수준 암호화를 사용 하 여 암호화 된 하므로 실제로 NIST SP 800 88 규격 지우지 필요 하지 않습니다. 그럼에도 불구 하 고 Microsoft가 수행 계속 됩니다.

Office 365 물리적으로 파괴 하 고 ISO 프로세스를 통해 감사 되는 데이터 센터 내에서 사용 되는 디스크에 실패 했습니다. 폐기 하는 적절 한 방법 자산 형식에 의해 결정 됩니다. 데이터 삭제 될 수 없는 하드 드라이브에 대 한 Microsoft를 사용 하 여 미디어를 손상 시키는 소멸 프로세스 (예: disintegrates, pulverizes, 또는 태 웁 니다) 하 고 정보의 복구 불가능 한 렌더링 합니다. 또한 Microsoft는 파괴의 모든 레코드를 유지합니다. Microsoft은 Office 365 내에서 다시 사용 되는 서버에는 비슷한 정리 프로세스를 수행 합니다. 이러한 지침 포함할 전자 및 실제 정리 합니다.

다시 사용할 수 없는 디스크 드라이브는 현장 소멸 되 고 디스크를 포함 하는 데이터 센터 내에서 수행 하는 물리적으로 파괴 프로세스를 사용 하 여 삭제 됩니다. 폐기 용으로 지정 된 저장소 미디어 데이터 센터의 각 영역에 있는 보안 저장소에 배치 됩니다. 각 보안 bin 스테이션 비디오 감시 하 여 모니터링 됩니다. 폐기 bin 약 50% 용량에 도달 하면 되 면 사이트 서비스 팀의 제거를 조정 하기 위해 물리적 보안 팀에 접속 합니다. 사이트 서비스 담당자 데이터 소멸 기다립니다 보안된 저장소 영역에 배치 됩니다 때까지 폐기 bin 호위 보안 책임자 아래에서 제거 합니다. 정책 및 폐기 하는 동안 장치를 가진 도형을 한 데이터를 처리 하는 방식을 제어 하는 절차 정기적으로 테스트 기계 소멸에 대 한 승인 상태를 확인 하는 절차를 포함 합니다.

데이터 소멸 프로세스에서 디스크에 먼저 NIST 800 88 (가능한 경우)과 호환 되는 방식으로 지워집니다 하 고는 산업 분쇄기에 배치 및 물리적으로 파괴 했 다음 합니다. Microsoft는 NIST SP 800 88 일관 된 정리/삭제, 자산 파괴, 암호화, 정확 하 게 인벤토리, 추적 및 전송 중에 대하여의 체인의 보호를 사용 하 여 데이터 센터에서 나가는 자산에 대 한 책임을 유지 합니다. 폐쇄 회로 텔레비전을 통해이 프로세스를 모니터링 하 고 완료 되 면 소멸 인증서 발급 됩니다.

Microsoft는 [아주 프로토콜 솔루션](http://www.enterprisedataerasure.com/) (EPS)에서 데이터 지우지 단위를 사용 합니다. EPS 소프트웨어 정리 하 고 삭제 하 고 보호 지우지 위한 NIST SP 800 88 요구 사항을 지원합니다. 정리 또는 파괴 하기 전에 인벤토리 Microsoft 자산 관리자가 만들어집니다. 공급 업체를 소멸 사용 하는 경우 공급 업체 자산 관리자에 의해 유효성이 검사 되는 소멸, 각 자산에 대 한 파괴의 인증서를 제공 합니다.