---
title: 중요 한 정보에 대 한 새 Office 365 메시지 암호화 정책
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/7/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 요약:는 자동으로 모든 테 넌 트에 제공 하는 중요 한 정보 형식에 대 한 Office 365 메시지 암호화 정책을 적용 합니다.
ms.openlocfilehash: f5996707d1cafe8dc1bf90856878de0a4fb7b77b
ms.sourcegitcommit: 30faa3ba91cab4c36e3d8d8ed5858d5269ea8a56
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27752092"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a>중요 한 정보에 대 한 office 365 메시지 암호화 정책

우리를 작성할 새 자동 정책을 중요 한 정보를 포함 하 고 조직 외부에 전송 되 고 있는 모든 전자 메일을 Office 365 메시지 암호화 적용 되는 Office 365 테 넌 트의 합니다. 기본적으로 조직 보호 됩니다 되도록이 새 Exchange 메일 흐름 규칙 Office 365 테 넌 트에 자동으로 생성 됩니다.

## <a name="when-to-expect-the-update-for-your-tenant"></a>테 넌 트에 대 한 업데이트를 것으로 예상 되는 경우

조직에는 자동이 정책을 테 넌 트에 작성 되는 날짜를 알리는 Office 365 메시지 센터에는 알림을 받게 됩니다. 30 일 알림의 부여 하 고 옵션 옵트아웃을 갖습니다. 잠재적으로 옵트아웃할 하려면 하는 시나리오를 위한 타사 데이터 손실 방지 솔루션 이미 중요 한 형식에 대 한 검색을 하는 경우 것입니다. 옵트아웃 하는 방법에 대 한 자세한 내용은이 문서의 뒷부분에 사용할 수 있습니다.

## <a name="sensitive-information-type-policy-details"></a>중요 한 정보 유형 정책 세부 정보

조직에서 사용 하 여 조직의 외부로 나가는 전자 메일을 자동으로 암호화 하는 Exchange 메일 흐름 규칙을 만들는 *암호화 전용* 정책 다음과 같은 중요 한 정보 형식을 포함 하는 경우:

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

업데이트 하거나이 새로운 변경 하기 전에 모든 기존 Office 365 구성 설정을 수정할 필요가 없습니다. 그러나 다음 모든 해당 최종 사용자 설명서 및 교육 자료 (영문)이이 변경에 대 한 조직의 사용자에 게 준비를 업데이트 하는 것이 좋습니다. 필요에 따라 사용자와 이러한 Office 365 메시지 암호화 리소스를 공유 합니다.

- [전송 하 고, 보고, PC에 대 한 Outlook에서 암호화 된 메시지에 회신](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [Office 365 Essentials 비디오: Office 메시지 암호화](https://youtu.be/CQR0cG_iEUc)

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a>이 변경 내용을 표시 되는 방법을 감사 로그에 있습니까?

이 작업은 감사 및 고객에 게 표시 됩니다.  이 작업은 ' New-transportrule ' 이며 보안 및 규정 준수 센터의 감사 로그 검색에서 예제 감사 항목의 코드 조각을 아래:

|     |
| --- |
| *{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345", "RecordType": 월 1 일, "ResultStatus": "True", "UserKey": "Microsoft 연산자"," UserType": 3,"버전": 월 1 일,"작업":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":""," UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX ( 15.20.1382.008)","Parameters": {"Name":"조직","값":" 123456 221 d-12346"{"Name":"ApplyRightsProtectionTemplate","값":"암호화"}, {"Name":"이름","값":"(로그 아웃 상자 규칙) 중요 한 아웃 바운드 전자 메일이 암호화"}, {"Name":" MessageContainsDataClassifications"등입니다.*
 |

## <a name="how-do-i-opt-out"></a>어떻게 수행 합니까 옵트아웃?

옵트아웃이 변경 하려는 경우에 다음이 단계를 수행 하십시오.

1. Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 하는 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://aka.ms/exopowershell)참조 하십시오.
2. 다음과 같이 Set-irmconfiguration cmdlet를 실행 합니다.

   ```
   Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
   ```

## <a name="how-do-i-disable-the-automatic-policy"></a>자동 정책의 비활성화 하려면 어떻게 합니까?

하면 하지 않았으므로 옵트아웃이 변경 하 고 Exchange 메일 규칙을 이미 만든 경우 있습니다 수 [규칙을 사용 하지 않도록 설정](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) **메일 흐름**으로 이동 하 여 > **규칙** 에서 Exchange 관리 센터 (EAC) 및 "*암호화 아웃 바운드 규칙을 사용 하지 않도록 설정 중요 한 전자 메일 상자 규칙) (부재중*"입니다.
