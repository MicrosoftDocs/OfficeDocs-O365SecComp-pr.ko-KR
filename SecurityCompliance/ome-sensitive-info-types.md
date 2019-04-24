---
title: 중요 한 정보에 대 한 Office 365 메시지 암호화 정책
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/31/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: '요약: 중요 한 정보 유형에 대 한 Office 365 메시지 암호화 정책을 지금 사용할 수 있습니다.'
ms.openlocfilehash: 99cb7a9f94c9cf4036c11b74a5208ddf0e819ceb
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261266"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a>중요 한 정보에 대 한 Office 365 메시지 암호화 정책

업데이트 (1/30/19): 10 월 2018에서는 특정 중요 한 정보 유형을 기반으로 중요 한 전자 메일을 자동으로 암호화 하 여 보호를 단순화할 수 있는지를 이해 하기 위한 소수의 고객 예제로 노력 했습니다. 이 샘플의 긍정적인 피드백을 기반으로 하 여 12 월 2018에 보다 다양 한 테 넌 트 프로필을 확장 하기로 결정 했습니다. 다음 롤오버를 통신 하 여 테 넌 트를 선택 하면 사용자 의견을 수렴 하 고 복잡 한 환경이 있는 고객이 규칙을 보다 주의 깊게 구현 하기를 원했습니다.

조직이 롤업을 사용 하도록 선택한 경우 2019 년 1 월 15 일부터 시작 하는 경우 자동 정책이 배포 되지 않습니다. 대신이 문서에서 롤아웃 yourselves을 완료 하는 방법에 대 한 지침을 제공 합니다. 정보를 계속 확인 하 여 방법을 알아봅니다.

||
|:-----|
|이 문서는 Office 365 메시지 암호화에 대 한 보다 광범위 한 문서에 포함 되어 있습니다. 이 문서는 관리자와 itpros 전문가를 위한 것입니다. 암호화 된 메시지를 보내거나 받는 방법에 대 한 정보를 찾으려는 경우에는 [Office 365 메시지 암호화 (OME)](ome.md) 의 문서 목록을 참조 하 여 요구 사항에 가장 적합 한 문서를 검색 하세요. |
||

## <a name="how-to-create-the-sensitive-information-type-policy-for-your-tenant"></a>테 넌 트에 대 한 중요 한 정보 유형 정책을 만드는 방법

Exchange 메일 흐름 규칙 또는 Office 365 DLP (데이터 손실 방지)를 사용 하 여 중요 한 정보 유형 정책을 만들 수 있습니다. exchange 메일 흐름 규칙을 만들려면 EAC (exchange 관리 센터) 또는 PowerShell을 사용할 수 있습니다.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a>EAC에서 메일 흐름 규칙을 사용 하 여 정책을 만들려면

EAC (Exchange 관리 센터)에 로그인 하 고 **메일 흐름** > **규칙**으로 이동 합니다. 여기에는 메시지 또는 첨부 파일에 특정 키워드나 중요 한 정보 유형이 존재 하는 등의 조건에 따라 Office 365 메시지 암호화를 적용 하는 규칙이 작성 됩니다.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a>PowerShell에서 메일 흐름 규칙을 사용 하 여 정책을 만들려면

Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오. TransporRule cmdlet을 사용 하 여 정책을 만듭니다.

### <a name="example-mail-flow-rule-created-with-powershell"></a>PowerShell로 만든 메일 흐름 규칙 예제

PowerShell에서 다음 명령을 실행 하 여 전자 메일 또는 첨부 파일에 다음과 같은 중요 한 정보가 포함 되어 있는 경우 *암호화 전용* 정책을 사용 하 여 조직 외부의 전자 메일을 자동으로 암호화 하는 Exchange 메일 흐름 규칙 만들기 정보 유형:

- ABA 라우팅 번호
- 신용 카드 번호
- DEA (약품 집행 기관) 번호
- 미국/영국 passport number
- 미국 은행 계좌 번호
- 미국 ITIN(개인 납세자 번호)
- 미국 SSN(사회 보험 번호)

```powershell
Set-IRMConfiguration -DecryptAttachmentsForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

## <a name="how-recipients-access-attachments"></a>받는 사람이 첨부 파일에 액세스 하는 방법

메시지가 암호화 되 면 받는 사람은 액세스 하 여 암호화 된 전자 메일을 여는 경우 첨부 파일에 무제한으로 액세스할 수 있습니다.

## <a name="to-prepare-for-this-change"></a>이 변경 내용을 준비 하려면

해당 하는 최종 사용자 설명서 및 교육 자료를 업데이트 하 여 조직의 사용자가이 변경 내용을 준비할 수 있습니다. 다음 Office 365 메시지 암호화 리소스를 사용자와 적절 하 게 공유 합니다.

- [PC 용 Outlook에서 암호화 된 메시지 보내기, 확인 및 회신](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [office 365 Essentials 동영상: office 메시지 암호화](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a>감사 로그에서 이러한 변경 내용을 확인 합니다.

이 활동은 감사 되며 Office 365 관리자가 사용할 수 있습니다. 이 작업은 ' New-new-transportrule ' 이며, 보안 & 준수 센터의 감사 로그 검색의 예제 감사 항목의 코드 조각이 아래에 있습니다.

|     |
| --- |
| *{"CreationTime": "2018-11-28t23:35:01", "Id": "a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c", "Operation": "New-new-transportrule", "조직 id": "123456-221d-12345", "RecordType": 1, "resultstatus": "True", "userkey": "Microsoft Operator", " UserType ": 3," Version ": 1," 작업 부하 ":" Exchange "," ClientIP ":" 123.456.147.68:17584 "," ObjectId ":" "," UserId ":" Microsoft Operator","OrganizationName":"contoso ":" OriginatingServer ( 15.20.1382.008) "," 매개 변수 ": {" Name ":" 조직 "," 값 ":" 123456-221d-"ApplyRightsProtectionTemplate", "value", "12346": "", "" name "," value ":" 아웃 바운드 중요 한 전자 메일을 암호화 합니다 (box 규칙을 벗어났습니다. "}, {" Name ":" MessageContainsDataClassifications "... 기타.* |
| |

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a>중요 한 정보 유형 정책을 사용 하지 않도록 설정 하거나 사용자 지정 하려면

exchange 메일 흐름 규칙을 만든 후에는 EAC (exchange 관리 센터)의 **메일 흐름** > **규칙** 으로 이동 하 여 [규칙을 사용 하지 않도록 설정 하거나 편집할](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) 수 있으며 "*아웃 바운드 중요 한 전자 메일 암호화 (box 규칙을 초과* 함" 규칙을 사용 하지 않도록 설정 합니다. ".
