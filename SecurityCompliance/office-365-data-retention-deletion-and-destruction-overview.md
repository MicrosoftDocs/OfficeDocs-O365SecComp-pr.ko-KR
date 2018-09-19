---
title: Office 365에서 데이터 보존, 삭제 및 폐기
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 데이터 보존 기간, 삭제 및 폐기에 대 한 Office 365에 대 한 Microsoft의 정책 개요입니다.
ms.openlocfilehash: bb038f8bd8e3f0286ea7d673e5e286bdc4a9677d
ms.sourcegitcommit: 1bccdaacf358505604c9cf422cb1e272aefae19d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "23999149"
---
# <a name="data-retention-deletion-and-destruction-in-office-365"></a>Office 365에서 데이터 보존, 삭제 및 폐기

## <a name="introduction"></a>소개
Microsoft에는 데이터 처리 표준 정책이 삭제 되 고 후 고객 데이터를 보존 하는 기간을 지정 하는 Office 365에 대 한 사용 합니다. 일반적으로 내 Office 365에는 고객 데이터를 삭제 하는 두 시나리오:
- 데이터를 삭제 하는 **현재 삭제** -사용자 또는 사용자에 게 개인 데이터를 현재 테 넌 트 관리자가 해당 사용자가 삭제 한 후 삭제 됩니다.
- **수동 삭제** -테 넌 트 구독을 종료합니다.

Office 365에 대 한 Microsoft의 데이터 처리 표준 정책 이러한 각 시나리오에 데이터를 유지 하는 기간을 지정 합니다. 다음 섹션에서는 범주 (Microsoft의 Office 365 자산 분류 표준에 따라) 데이터와 활성 및 수동 삭제 시나리오에 대 한 보존 기간에 설명 합니다.

## <a name="active-deletion-retention"></a>활성 삭제 보존

| 데이터 범주 | 적어도 유지 | 이하로 유지 |
|---------------------------------------|:-----------------:|:-----------------:|:----------------------------------:|:-------------------------------:|
| 액세스 제어 데이터 | 해당 없음 | 해당 없음 |
| 고객 콘텐츠 | 7일 | 30일 |
| 최종 사용자 식별 가능 정보 | 90일 | 180일 |
| 계정 데이터 | 1년 | 3 년 |
| 조직 식별 정보 | 90일 | 180일 |
| 시스템 메타 데이터 | 보안 로그를 참조 하십시오. | 보안 로그를 참조 하십시오. |
| 보안 로그 | Min 1 년 후 | 최대 1 년 |
| Exchange Online 보관 로그 | Min 3 년 | 최대 3 년 |

## <a name="passive-deletion-retention"></a>수동 삭제 보존

| 데이터 범주 | 적어도 유지 | 이하로 유지 |
|---------------------------------------|:-----------------:|:-----------------:|:----------------------------------:|:-------------------------------:|
| 액세스 제어 데이터 | 90 일 (복구를 위한 콘텐츠) | 180 일 (복구를 위한 콘텐츠) |
| 고객 콘텐츠 | 90 일 (제한 된 기능의 계정) | 180일 |
| 최종 사용자 식별 가능 정보 | 90일 | 180일 |
| 계정 데이터 | 1년 | 3 년 |
| 조직 식별 정보 | 90일 | 180일 |
| 시스템 메타 데이터 | 보안 로그를 참조 하십시오. | 보안 로그를 참조 하십시오. |
| 보안 로그 | Min 1 년 후 | 최대 1 년 |
| Exchange Online 보관 로그 | Min 3 년 | 최대 3 년 |

## <a name="subscription-rentention"></a>구독 고정

Exchange Online 사서함 콘텐츠 고객 콘텐츠 정의 됩니다 (전자 메일 본문, 일정 항목 및 전자 메일 첨부 파일의 콘텐츠 및 해당 되는 경우 비즈니스 콘텐츠 용 Skype), SharePoint Online 사이트 콘텐츠 및 사이트, 내에 저장 된 파일 및 파일 비즈니스 또는 Skype 비즈니스용 OneDrive에 업로드 합니다.

항상 용어 중 구독 at 구독자 수에 액세스 하 고 Office 365에 저장 된 고객 데이터를 추출 합니다. 무료 평가판 (영문) 및 LinkedIn 서비스를 제외 하 고 Microsoft 고객에 저장 된 데이터 Office 365의 제한 된 기능의 계정 90 일 동안 만료 또는 데이터를 추출 하는 구독자를 사용 하도록 설정 하려면 구독 종료 후 유지 합니다. (무료 평가판의 경우 평가판 만료 되 면 안으로 이동 유예 기간, Office 365를 구입 (대부분의 국가 및 지역에는 대부분 trials)에 대 한 일을 지정 합니다. Office 365를 구매 하지 않도록 결정 하는 경우에 프로그램 평가판 만료 하도록 수도 있고 프로세스를 취소할 수 있습니다. 30 일의 유예 기간 후 곧 평가판 계정 정보 및 데이터 영구적으로 삭제 됩니다.)

90 일 보존 기간 종료 된 후 Microsoft 계정을 비활성화 하 고 고객 데이터를 삭제 합니다. 180 일 개 이하의 만료 또는 Office 365에 대 한 구독의 종료 후 Microsoft는 계정을 사용 하지 않도록 설정 하 고 계정에서 모든 고객 데이터를 삭제 합니다. 모든 데이터에 대 한 최대 보존 기간 경과 된 후에 데이터 통상적으로 복구할 수 없는 렌더링 됩니다.

Microsoft는 재활용 및 폐기 디스크 드라이브 및 실패 한 또는 사용 하지 않도록 설정 하는 서버를 해결 하는 데이터 처리 표준 정책을 있습니다. Office 365 내에 모든 디스크 드라이브를 다시 사용 하기 전에 Microsoft NIST SP 800 88과 호환 되는 실제 정리 프로세스를 수행 합니다. 다시 사용할 수 없는 디스크 드라이브는 현장 소멸 되 고 디스크를 포함 하는 데이터 센터 내에서 수행 하는 물리적으로 파괴 프로세스를 사용 하 여 삭제 됩니다. Microsoft 클라우드 인프라 및 작업 (MCIO) 하 여 이러한 절차를 수행 합니다. 자세한 내용은 [서비스를 신뢰 미리 보기](https://aka.ms/STP)에 대 한 보고서를 감사 MCIO을 참조 하십시오.

## <a name="expedited-deletion"></a>긴급된 삭제
항상 용어 중 구독 at 구독자는 Microsoft 기술 지원 서비스 및 긴급 요청 구독 프로 비전 해제 문의할 수 있습니다. 이 프로세스에서 데이터를 포함 하 여 SharePoint online에서 Exchange Online에서 될 수 있는 모든 사용자 데이터를 유지 또는 관리자가 Microsoft에서 제공 하는 잠금 코드를 입력 한 후 삭제 된 3 일은 비활성 사서함에 저장 합니다. 긴급 프로 비전 해제에 대 한 자세한 내용은 [Office 365 취소](https://support.office.com/article/Cancel-Office-365-for-business-b1bc0bef-4608-4601-813a-cdd9f746709a)를 참조 하십시오.

## <a name="related-links"></a>관련된 링크
- [Exchange Online 데이터 삭제](office-365-exchange-online-data-deletion.md)
- [SharePoint Online 데이터 삭제](office-365-sharepoint-online-data-deletion.md)
- [비즈니스용 Skype 데이터 삭제](office-365-skype-data-deletion.md)
- [Office 365의 불변성](office-365-data-immutability.md)
- [데이터 폐기](office-365-data-destruction.md)