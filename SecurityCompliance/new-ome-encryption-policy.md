---
title: 중요 한 정보에 대 한 새 Office 365 메시지 암호화 정책
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 12/13/2018
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: '요약: 새 Office 365 메시지 암호화 정책에 대 한 중요 한 정보입니다.'
ms.openlocfilehash: 180050d1bf9303f6d29bc126e66ac53211c2fb34
ms.sourcegitcommit: 3aae959ea1ac5ef61a9942c681d334831e6b6038
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/14/2018
ms.locfileid: "27271094"
---
# <a name="new-office-365-message-encryption-policy-for-sensitive-information"></a>중요 한 정보에 대 한 새 Office 365 메시지 암호화 정책

우리를 작성할 새 자동 정책을 중요 한 정보를 포함 하 고 조직 외부에 전송 되 고 있는 모든 전자 메일을 Office 365 메시지 암호화 적용 되는 Office 365 테 넌 트의 합니다. 기본적으로 조직 보호 됩니다 되도록이 새 Exchange 메일 흐름 규칙 Office 365 테 넌 트에 자동으로 생성 됩니다.

## <a name="how-will-this-work"></a>이 회사는 어떻게 합니까?

조직에는 자동이 정책을 테 넌 트에 작성 되는 날짜를 알리는 Office 365 메시지 센터에는 알림을 받게 됩니다. 30 일 알림의 부여 하 고 옵션 옵트아웃을 갖습니다. 잠재적으로 옵트아웃할 하려면 하는 시나리오를 위한 타사 데이터 손실 방지 솔루션 이미 중요 한 형식에 대 한 검색을 하는 경우 것입니다.

## <a name="new-policy-details"></a>새 정책 세부 정보

새 Exchange 메일 흐름 규칙을 사용 하 여 조직의 외부로 나가는 전자 메일을 자동으로 암호화 하는 조직에서 만들어질는 *암호화 전용* 정책 다음과 같은 중요 한 정보 형식을 포함 하는 경우:

- ABA 라우팅 번호
- 신용 카드 번호
- 약물 적용 기관 (DEA) 번호
- 미국 / 영국 여권 번호
- 미국 은행 계좌 번호
- 미국 ITIN(개인 납세자 번호)
- 미국 SSN(사회 보험 번호)

> [!Note]
> 정확 하 게 중요 한 형식 조직의 로캘에 의해 다를 수 있습니다 및 메시지 센터 알림 영역에서 전달 됩니다.

## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a>준비 하기 위해이 변경을 수행 어떻게 해야 합니까?

업데이트 하거나이 새로운 변경 하기 전에 모든 기존 Office 365 구성 설정을 수정할 필요가 없습니다. 그러나 다음 모든 해당 최종 사용자 설명서 및 교육 자료 (영문)이이 변경에 대 한 조직의 사용자에 게 준비를 업데이트 하는 것이 좋습니다.

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a>이 변경 내용을 표시 되는 방법을 감사 로그에 있습니까?

이 작업은 감사 및 고객에 게 표시 됩니다.  이 작업은 ' New-transportrule ' 이며 보안 및 규정 준수 센터의 감사 로그 검색에서 예제 감사 항목의 코드 조각을 아래:

|     |
| --- |
| *{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345", "RecordType": 월 1 일, "ResultStatus": "True", "UserKey": "Microsoft 연산자"," UserType": 3,"버전": 월 1 일,"작업":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":""," UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX ( 15.20.1382.008)","Parameters": {"Name":"조직","값":" 123456 221 d-12346"{"Name":"ApplyRightsProtectionTemplate","값":"암호화"}, {"Name":"이름","값":"(로그 아웃 상자 규칙) 중요 한 아웃 바운드 전자 메일이 암호화"}, {"Name":" MessageContainsDataClassifications"등입니다.*
 |

## <a name="how-do-i-opt-out"></a>어떻게 수행 합니까 옵트아웃?

옵트아웃이 변경 하려는 경우에 다음이 단계를 수행 하십시오.

1. 전역 관리자 역할을 가진 사용자로 [Exchange Online PowerShell](https://aka.ms/exopowershell) 에 연결 합니다.
2.  인증 한 후 다음 코드를 실행 합니다.

    ```
    Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
    ```

## <a name="how-do-i-disable-the-automatic-policy"></a>자동 정책의 비활성화 하려면 어떻게 합니까?

하면 하지 않았으므로 옵트아웃이 변경 하 고 Exchange 메일 규칙을 이미 만든 경우 있습니다 수 [규칙을 사용 하지 않도록 설정](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) **메일 흐름**으로 이동 하 여 > **규칙** 에서 Exchange 관리 센터 (EAC) 및 "*암호화 아웃 바운드 규칙을 사용 하지 않도록 설정 중요 한 전자 메일 상자 규칙) (부재중*"입니다.
