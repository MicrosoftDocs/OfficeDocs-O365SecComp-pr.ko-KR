---
title: 일반적인 시나리오 문제를 해결 하기 위해 Office 365 감사 로그 검색
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
description: Office 365 감사 로그 검색 도구를 사용 하면 손상 된 계정을 조사 하거나, 사서함에 대 한 전자 메일 전달을 설정 하는 사람을 찾거나, 외부 사용자가 사용자에 게 로그인 할 수 있던 이유를 확인 하는 등의 일반적인 문제를 해결 하는 데 도움이 될 수 있습니다. 조직.
ms.openlocfilehash: 255fd323ca08dd4ea759648fbe0673f5e5254c22
ms.sourcegitcommit: 1947ad3c0dde9163ba9b6834d8b38bd04b4264a5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2019
ms.locfileid: "36643294"
---
# <a name="search-the-office-365-audit-log-to-troubleshoot-common-scenarios"></a>일반적인 시나리오 문제를 해결 하기 위해 Office 365 감사 로그 검색

이 문서에서는 일반적인 지원 시나리오를 해결 하는 데 도움이 되는 Office 365 감사 로그 검색 도구를 사용 하는 방법에 대해 설명 합니다. 여기에는 다음에 대 한 감사 로그 사용이 포함 됩니다.

- 손상 된 계정에 액세스 하는 데 사용 되는 컴퓨터의 IP 주소 찾기
- 사서함에 대 한 전자 메일 전달을 설정한 사람 결정
- 사용자가 사서함에서 전자 메일 항목을 삭제 했는지 확인 합니다.
- 사용자가 받은 편지함 규칙을 만들었는지 확인
- 조직 외부의 사용자가 성공적으로 로그인 한 이유 조사

## <a name="using-the-office-365-audit-log-search-tool"></a>Office 365 감사 로그 검색 도구 사용

이 문서에서 설명 하는 각 문제 해결 시나리오는 Office 365 보안 및 준수 센터의 감사 로그 검색 도구를 사용 하는 방법에 따라 달라 집니다. 이 섹션에서는 감사 로그를 검색 하는 데 필요한 사용 권한을 나열 하 고 감사 로그 검색에 액세스 하 고 실행 하는 단계를 설명 합니다. 각 시나리오 섹션에서는 감사 로그 검색 쿼리를 구성 하는 방법과 검색 조건과 일치 하는 감사 레코드의 자세한 정보에서 찾을 항목에 대 한 구체적인 지침을 제공 합니다.

### <a name="permissions-required-to-use-the-audit-log-search-tool"></a>감사 로그 검색 도구를 사용 하는 데 필요한 사용 권한

Office 365 감사 로그를 검색 하려면 Exchange Online에서 보기 전용 감사 로그 또는 감사 로그 역할을 할당 받아야 합니다. 기본적으로 이러한 역할은 Exchange 관리 센터의 **사용 권한** 페이지에 있는 준수 관리 및 조직 관리 역할 그룹에 할당 됩니다. Office 365 및 Microsoft 365의 전역 관리자는 Exchange Online에서 조직 관리 역할 그룹의 구성원으로 자동 추가 됩니다. 자세한 내용은 [Exchange Online에서 역할 그룹 관리](https://go.microsoft.com/fwlink/p/?LinkID=730688)를 참조 하세요.

### <a name="running-audit-log-searches"></a>감사 로그 검색 실행

이 섹션에서는 감사 로그 검색을 만들고 실행 하는 기본 사항에 대해 설명 합니다. 이러한 지침을이 문서의 각 문제 해결 시나리오를 위한 시작 점으로 사용 합니다. 단계별 지침에 대 한 자세한 내용은 [Search the audit log](search-the-audit-log-in-security-and-compliance.md#step-1-run-an-audit-log-search)을 참조 하십시오.

1. [https://protection.office.com/unifiedauditlog](https://protection.office.com/unifiedauditlog) 으로 이동 하 여 회사 또는 학교 계정을 사용 하 여 로그인 합니다.
    
    **감사 로그 검색** 페이지가 표시 됩니다. 
    
    ![조건을 구성한 다음 검색을 클릭 하 여 검색을 실행 합니다.](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
4. 다음 검색 조건을 구성할 수 있습니다. 이 문서의 각 문제 해결 시나리오에서는 이러한 필드를 구성 하기 위한 구체적인 지침을 제공 합니다.
    
    위한. **활동:** 드롭다운 목록을 클릭 하 여 검색할 수 있는 활동을 표시 합니다. 검색을 실행 한 후에는 선택한 활동에 대 한 감사 레코드만 표시 됩니다. **모든 작업에 대해 결과 표시** 를 선택 하면 다른 검색 조건을 충족 하는 모든 작업에 대 한 결과가 표시 됩니다. 일부 문제 해결 시나리오에서는이 필드를 비워 두어야 합니다.
    
    b. **시작 날짜** 및 **종료 날짜:** 해당 기간 내에 발생 한 이벤트를 표시 하려면 날짜 및 시간 범위를 선택 합니다. 지난 7 일이 기본적으로 선택 됩니다. 날짜와 시간은 UTC (협정 세계시) 형식으로 표시 됩니다. 지정할 수 있는 최대 날짜 범위는 90 일입니다.

    &. **사용자:** 이 상자를 클릭 하 고 검색 결과를 표시할 사용자를 한 명 이상 선택 합니다. 이 상자에서 선택한 사용자가 수행한 선택한 작업에 대 한 감사 레코드가 결과 목록에 표시 됩니다. 조직의 모든 사용자 및 서비스 계정에 대 한 항목을 반환 하려면이 상자를 비워 둡니다.
    
    &. **파일, 폴더 또는 사이트:** 지정한 키워드를 포함 하는 폴더의 파일에 관련 된 작업을 검색 하려면 파일 또는 폴더 이름을 일부 또는 모두 입력 합니다. 파일 또는 폴더의 URL을 지정할 수도 있습니다. URL을 사용 하는 경우에는 전체 URL 경로를 입력 하거나 URL의 일부만 입력 해야 하며 특수 문자나 공백은 포함 하지 않습니다. 조직의 모든 파일 및 폴더에 대 한 항목을 반환 하려면이 상자를 비워 둡니다. 이 문서에서 설명 하는 모든 문제 해결 시나리오에서는이 필드를 비워 둡니다.
    
5. 검색 **** 을 클릭 하 여 검색 조건을 사용 하 여 검색을 실행 합니다. 
    
    검색 결과가 로드 되 고 몇 분 후에 **감사 로그 검색** 페이지의 **결과** 아래에 표시 됩니다. 이 문서의 각 섹션에서는 특정 문제 해결 시나리오의 컨텍스트에서 확인 해야 하는 사항에 대 한 지침을 제공 합니다.

    감사 로그 검색 결과를 보거나 필터링 하거나 내보내는 방법에 대 한 자세한 내용은 다음을 참조 하십시오.

    - [검색 결과 보기](search-the-audit-log-in-security-and-compliance.md#step-2-view-the-search-results)
    - [검색 결과 필터링](search-the-audit-log-in-security-and-compliance.md#step-3-filter-the-search-results)
    - [검색 결과 내보내기](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file)

## <a name="find-the-ip-address-of-the-computer-used-to-access-a-compromised-account"></a>손상 된 계정에 액세스 하는 데 사용 되는 컴퓨터의 IP 주소 찾기

모든 사용자가 수행한 활동에 해당 하는 IP 주소가 대부분의 감사 레코드에 포함 됩니다. 사용 된 클라이언트에 대 한 정보는 감사 레코드에도 포함 됩니다.

이 시나리오에 대 한 감사 로그 검색 쿼리를 구성 하는 방법은 다음과 같습니다.

**활동:** 해당 사례와 관련 된 경우 검색할 특정 활동을 선택 합니다. 손상 된 계정 문제를 해결 하려면 **Exchange 사서함 활동**아래에서 **사서함에 로그인 한 사용자** 를 선택 하는 것이 좋습니다. 사서함에 로그인 할 때 사용 되는 IP 주소를 보여 주는 감사 레코드를 반환 합니다. 그렇지 않은 경우에는이 필드를 비워 두어 모든 활동에 대 한 감사 레코드를 반환 합니다. 

> [!TIP]
> 이 필드를 비워 두면 누군가가 Office 365 사용자 계정에 로그인 했음을 나타내는 Azure Active Directory 활동 인 **UserLoggedIn** 활동이 반환 됩니다. 검색 결과에서 필터링을 사용 하 여 **UserLoggedIn** 감사 레코드를 표시 합니다.

**시작 날짜** 및 **종료 날짜:** 조사에 적용할 수 있는 날짜 범위를 선택 합니다.

**사용자:** 손상 된 계정을 조사 하 고 있는 경우 계정이 손상 된 사용자를 선택 합니다. 이렇게 하면 해당 사용자 계정에 의해 수행 된 작업에 대 한 감사 레코드가 반환 됩니다.

**파일, 폴더 또는 사이트:** 이 필드는 비워 둡니다.

검색을 실행 하 고 나면 각 활동의 IP 주소가 검색 결과의 **ip 주소** 열에 표시 됩니다. 검색 결과의 레코드를 클릭 하 여 플라이 아웃 페이지에서 자세한 정보를 볼 수 있습니다.

## <a name="determine-who-set-up-email-forwarding-for-a-mailbox"></a>사서함에 대 한 전자 메일 전달을 설정한 사람 결정

사서함에 대해 전자 메일 전달이 구성 되 면 사서함으로 전송 되는 전자 메일 메시지가 다른 사서함으로 전달 됩니다. 조직 내부 또는 외부의 사용자에 게 메시지를 전달할 수 있습니다. 사서함에 전자 메일 전달이 설정 되 면 사용 되는 기본 Exchange Online cmdlet이 설정 된 **사서함**이 됩니다.

이 시나리오에 대 한 감사 로그 검색 쿼리를 구성 하는 방법은 다음과 같습니다.

**활동:** 검색에서 모든 활동에 대 한 감사 레코드를 반환 하도록이 필드를 비워 둡니다. 이는 **사서함** cmdlet과 관련 된 모든 감사 레코드를 반환 하는 데 필요 합니다.

**시작 날짜** 및 **종료 날짜:** 조사에 적용할 수 있는 날짜 범위를 선택 합니다.

**사용자:** 특정 사용자에 대 한 전자 메일 전달 문제를 조사 하 고 있지 않은 경우이 필드를 비워 둡니다. 이렇게 하면 사용자에 대해 전자 메일 전달이 설정 되었는지 쉽게 확인할 수 있습니다.

**파일, 폴더 또는 사이트:** 이 필드는 비워 둡니다.

검색을 실행 한 후 검색 결과 페이지에서 **결과 필터링** 을 클릭 합니다. **활동** 열 헤더 아래의 상자에 사서함 cmdlet과 관련 된 감사 레코드만 표시 되도록 **설정 사서함** 을 입력 합니다 **** .

![감사 로그 검색 결과 필터링](media/emailforwarding1.png)

이때 각 감사 레코드의 세부 정보를 확인 하 여 활동이 전자 메일 전달과 관련이 있는지 확인 해야 합니다. 감사 레코드를 클릭 하 여 **세부 정보** 플라이 아웃 페이지를 표시 하 고 **추가 정보**를 클릭 합니다. 다음 스크린샷 및 설명은 사서함에 대해 전자 메일 전달이 설정 되었음을 나타내는 정보를 강조 표시 합니다.

![감사 레코드에서 자세한 정보](media/emailforwarding2.png)

위한. **ObjectId** 필드에는 전자 메일 전달이 설정 된 사서함의 별칭이 표시 됩니다. 이 사서함은 검색 결과 페이지의 **항목** 열에도 표시 됩니다.

b. **매개 변수** 필드에서 *ForwardingSmtpAddress* 값은 사서함에 대해 전자 메일 전달이 설정 되었음을 나타냅니다. 이 예에서는 메일이 alpinehouse.onmicrosoft.com 조직 외부에 있는 전자 메일 주소 mike@contoso.com 전달 됩니다.

&. *DeliverToMailboxAndForward* 매개 변수의 값이 *True 이면* sarad@alpinehouse.onmicrosoft.com에 배달 된 메시지의 복사본이 ** *ForwardingSmtpAddress에서 지정한 전자 메일 주소로 전달 됨을 나타냅니다. *이 예제에서는 mike@contoso.com에 해당 하는 매개 변수를 사용할 수 있습니다. *DeliverToMailboxAndForward* 매개 변수의 값이 *False*로 설정 된 경우 전자 메일은 *ForwardingSmtpAddress* 매개 변수로 지정 된 주소로만 전달 됩니다. 이는 **ObjectId** 필드에 지정 된 사서함으로 배달 되지 않습니다.

&. **UserId** 필드에는 **ObjectId** 필드에 지정 된 사서함에 대해 전자 메일 전달을 설정한 사용자가 표시 됩니다. 이 사용자는 검색 결과 페이지의 **사용자** 열에도 표시 됩니다. 이 경우 사서함 소유자가 사서함에서 전자 메일을 전달 하는 것으로 보입니다.

사서함에 대해 전자 메일 전달이 설정 되어 있지 않은 것으로 확인 되 면 Exchange Online PowerShell에서 다음 명령을 실행 하 여 제거할 수 있습니다.

```
Set-Mailbox <mailbox alias> -ForwardingSmtpAddress $null 
```

전자 메일 전달과 관련 된 매개 변수에 대 한 자세한 내용은 [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox) 문서를 참조 하십시오.

## <a name="determine-if-a-user-deleted-email-items"></a>사용자가 전자 메일 항목을 삭제 했는지 확인

1 월 2019 부터는 Microsoft에서 모든 Office 365 및 Microsoft 조직에 대해 기본적으로 사서함 감사 로깅을 설정 하 고 있습니다. 즉, 사서함 소유자가 수행 하는 특정 작업이 자동으로 기록 되며 사서함 감사 로그에서 해당 사서함을 검색 하면 해당 레코드 감사 레코드도 사용할 수 있습니다. 사서함 감사를 기본적으로 설정 하기 전에 조직의 모든 사용자 사서함에 대해이 기능을 수동으로 사용 하도록 설정 해야 했습니다. 

기본적으로 기록 되는 사서함 작업에는 사서함 소유자가 수행한 소프트 삭제 및 하드 삭제 사서함 작업이 포함 됩니다. 즉, 다음 단계를 사용 하 여 삭제 된 전자 메일 항목에 대 한 감사 로그를 검색할 수 있습니다. 기본적으로 사서함 감사에 대 한 자세한 내용은 [사서함 감사 관리](enable-mailbox-auditing.md)를 참조 하십시오.

이 시나리오에 대 한 감사 로그 검색 쿼리를 구성 하는 방법은 다음과 같습니다.

**활동:** **Exchange 사서함 활동**에서 다음 작업 중 하나 또는 둘 다를 선택 합니다.

- **지운 편지함 폴더에서 삭제 된 메시지:** 이 활동은 **소프트 삭제** 사서함 감사 작업에 해당 합니다. 이 작업은 사용자가 항목을 선택 하 고 **Shift + Delete**키를 눌러 영구적으로 삭제 한 경우에도 기록 됩니다. 항목이 영구적으로 삭제 된 후에는 삭제 된 항목 보존 기간이 만료 될 때까지 사용자가 해당 항목을 복구할 수 있습니다.

- **사서함에서 메시지 제거 됨:** 이 작업은 사서함 감사 기능 **하드 삭제** 작업에 해당 합니다. 사용자가 복구 가능한 항목 폴더에서 항목을 제거 하면이 로그를 기록 합니다. 관리자는 보안 및 준수 센터의 콘텐츠 검색 도구를 사용 하 여 삭제 된 항목 보존 기간이 만료 되거나 사용자의 사서함이 대기 중인 경우 더 오래 된 항목을 검색 하 고 복구할 수 있습니다.

**시작 날짜** 및 **종료 날짜:** 조사에 적용할 수 있는 날짜 범위를 선택 합니다.

**사용자:** 이 필드에서 사용자를 선택 하면 감사 로그 검색 도구는 지정한 사용자가 삭제 한 전자 메일 항목에 대 한 감사 레코드 (소프트 삭제 또는 하드 삭제 됨)를 반환 합니다. 전자 메일을 삭제 하는 사용자가 사서함 소유자가 아닐 수도 있습니다.

**파일, 폴더 또는 사이트:** 이 필드는 비워 둡니다.

검색을 실행 한 후에는 검색 결과를 필터링 하 여 일시 삭제 된 항목에 대 한 감사 레코드를 표시 하거나 일시적으로 삭제 한 항목의 경우이를 표시할 수 있습니다. 감사 레코드를 클릭 하 여 **세부 정보** 플라이 아웃 페이지를 표시 하 고 **추가 정보**를 클릭 합니다. 제목 줄과 삭제 된 항목의 위치와 같은 삭제 된 항목에 대 한 추가 정보는 **AffectedItems** 필드에 표시 됩니다. 다음 스크린샷에서는 일시 삭제 된 항목의 **AffectedItems** 필드와 영구 삭제 된 항목의 예를 보여 줍니다.

**일시 삭제 된 항목에 대 한 AffectedItems 필드의 예**

![일시 삭제 된 항목에 대 한 감사 레코드](media/softdeleteditem.png)

**영구 삭제 된 항목에 대 한 AffectedItems 필드의 예**

![하드 삭제 된 전자 메일 항목에 대 한 감사 레코드](media/harddeleteditem.png)

### <a name="recover-deleted-email-items"></a>삭제 된 전자 메일 항목 복구

사용자는 삭제 된 항목 보존 기간이 만료 되지 않은 경우 일시 삭제 된 항목을 복구할 수 있습니다. Exchange Online에서 삭제 된 기본 항목 보존 기간은 14 일 이지만 관리자는이 설정을 최대 30 일로 높일 수 있습니다. 삭제 된 항목을 복구 하는 방법에 대 한 지침은 사용자가 [웹 문서의 Outlook에서 지운 편지함 복구 또는 전자 메일](https://support.office.com/article/Recover-deleted-items-or-email-in-Outlook-Web-App-C3D8FC15-EEEF-4F1C-81DF-E27964B7EDD4) 을 가리킵니다.

앞에서 설명한 것 처럼, 삭제 된 항목 보존 기간이 만료 되거나 사서함이 보류 중인 경우에는 영구 삭제 된 항목을 복구할 수 있으며,이 경우 보존 기간이 만료 될 때까지 항목이 보존 됩니다. 콘텐츠 검색을 실행 하면 복구 가능한 항목 폴더에서 일시 삭제 되 고 영구 삭제 된 항목이 검색 쿼리와 일치 하는 경우 검색 결과에 반환 됩니다. 콘텐츠 검색을 실행 하는 방법에 대 한 자세한 내용은 [Office 365의 콘텐츠 검색](content-search.md)을 참조 하세요.

> [!TIP]
> 삭제 된 전자 메일 항목을 검색 하려면 감사 레코드의 **AffectedItems** 필드에 표시 되는 제목 줄 전체 또는 일부를 검색 합니다.

## <a name="determine-if-a-user-created-an-inbox-rule"></a>사용자가 받은 편지함 규칙을 만들었는지 확인

사용자가 자신의 Exchange Online 사서함에 대 한 받은 편지함 규칙을 만들면 해당 하는 감사 레코드가 감사 로그에 저장 됩니다. 받은 편지함 규칙에 대 한 자세한 내용은 다음 항목을 참조 하십시오.

- [웹용 Outlook에서 받은 편지함 규칙 사용](https://support.office.com/article/use-inbox-rules-in-outlook-on-the-web-8400435c-f14e-4272-9004-1548bb1848f2)
- [규칙을 사용 하 여 Outlook에서 전자 메일 메시지 관리](https://support.office.com/article/Manage-email-messages-by-using-rules-C24F5DEA-9465-4DF4-AD17-A50704D66C59)

이 시나리오에 대 한 감사 로그 검색 쿼리를 구성 하는 방법은 다음과 같습니다.

**활동:** **Exchange 사서함 활동**에서 **disable-inboxrule 만들기/수정/사용/사용 안 함 규칙**을 선택 합니다.

**시작 날짜** 및 **종료 날짜:** 조사에 적용할 수 있는 날짜 범위를 선택 합니다.

**사용자:** 특정 사용자를 조사 하는 경우가 아니면이 필드를 비워 둡니다. 이렇게 하면 모든 사용자가 설정한 새 받은 편지함 규칙을 식별 하는 데 도움이 됩니다.

**파일, 폴더 또는 사이트:** 이 필드는 비워 둡니다.

검색을 실행 한 후에는이 작업에 대 한 감사 레코드가 검색 결과에 표시 됩니다. 감사 레코드를 클릭 하 여 **세부 정보** 플라이 아웃 페이지를 표시 하 고 **추가 정보**를 클릭 합니다. 받은 편지함 규칙 설정에 대 한 정보는 **매개 변수** 필드에 표시 됩니다. 다음 스크린샷 및 설명은 받은 편지함 규칙에 대 한 정보를 강조 합니다.

![새 받은 편지함 규칙에 대 한 감사 레코드](media/NewInboxRuleRecord.png)

위한. **ObjectId** 필드에 받은 편지함 규칙의 전체 이름이 표시 됩니다. 이 이름에는 사용자 사서함의 별칭 (예: SaraD)과 받은 편지함 규칙 이름 (예: "관리자 로부터 메시지 이동")이 포함 됩니다.

b. **매개 변수** 필드에 받은 편지함 규칙의 조건이 표시 됩니다. 이 예제에서는 *From* 매개 변수를 통해 조건을 지정 합니다. *From* 매개 변수에 대해 정의 된 값은 받은 편지함 규칙이 admin@alpinehouse.onmicrosoft.com에서 보내는 전자 메일을 작동 함을 나타냅니다. 받은 편지함 규칙의 조건을 정의 하는 데 사용할 수 있는 매개 변수의 전체 목록은 [disable-inboxrule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) 문서를 참조 하십시오.

&. *MoveToFolder* 매개 변수는 받은 편지함 규칙에 대 한 동작을 지정 합니다. 이 예에서는 admin@alpinehouse.onmicrosoft.com에서 받은 메시지가 *Adminsearch*라는 폴더로 이동 됩니다. 또한 받은 편지함 규칙의 동작을 정의 하는 데 사용할 수 있는 매개 변수의 전체 목록은 [disable-inboxrule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) 문서를 참조 하십시오.

&. **UserId** 필드에는 **ObjectId** 필드에 지정 된 받은 편지함 규칙을 만든 사용자가 표시 됩니다. 이 사용자는 검색 결과 페이지의 **사용자** 열에도 표시 됩니다.

## <a name="investigate-why-there-was-a-successful-login-by-a-user-outside-your-organization"></a>조직 외부의 사용자가 성공적으로 로그인 한 이유 조사

Office 365 감사 로그에서 감사 레코드를 검토할 때 외부 사용자가 Azure Active Directory에서 인증 되었으며 조직에 성공적으로 로그인 되었음을 나타내는 레코드가 표시 될 수 있습니다. 예를 들어 contoso.onmicrosoft.com의 관리자는 다른 Office 365 조직 (예: fabrikam.onmicrosoft.com)의 사용자가 contoso.onmicrosoft.com에 성공적으로 로그인 한 것을 보여 주는 감사 레코드를 볼 수 있습니다. 마찬가지로 Outlook.com 또는 Live.com와 같은 Microsoft 계정 (MSA)을 사용 하는 사용자에 게 조직에 로그인 했을 나타내는 감사 레코드가 표시 될 수 있습니다. 이러한 상황에서 감사 된 활동은 **사용자가 로그인 한**것입니다. 

이 동작은 의도적으로 설계 되었습니다. Office 365의 디렉터리 서비스인 azure Active Directory (Azure AD)는 외부 사용자가 조직의 SharePoint 사이트 또는 OneDrive 위치에 액세스 하려고 할 때 *통과 인증* 을 통해 수행할 수 있도록 합니다. 외부 사용자가이 작업을 수행 하려고 하면 해당 Office 365 자격 증명을 입력 하 라는 메시지가 표시 됩니다. Azure AD는 자격 증명을 사용 하 여 사용자를 인증 하며, Azure AD는 사용자가 누구 인지를 확인 합니다. 감사 레코드에 성공한 로그인을 나타내는 것은 Azure AD 사용자 인증의 결과입니다. 로그인이 성공 해도 사용자가 조직에서 모든 리소스에 액세스 하거나 다른 작업을 수행할 수 있는 것은 아닙니다. 사용자가 Azure AD에서 인증 되었음을 나타냅니다. 통과 사용자가 SharePoint 또는 OneDrive 리소스에 액세스 하기 위해 조직의 사용자는 공유 초대 또는 익명 공유 링크를 보내 해당 리소스를 외부 사용자와 명시적으로 공유 해야 합니다. 

> [!NOTE]
> Azure AD에서는 SharePoint Online 및 비즈니스용 OneDrive와 같은 *첫 번째 타사 응용 프로그램*에 대해서만 통과 인증을 허용 합니다. 다른 타사 응용 프로그램에는 허용 되지 않습니다.

다음은 통과 인증의 결과로 발생 하는 **사용자 로그인** 이벤트에 대 한 감사 레코드의 관련 속성에 대 한 예 및 설명입니다. 감사 레코드를 클릭 하 여 **세부 정보** 플라이 아웃 페이지를 표시 하 고 **추가 정보**를 클릭 합니다.

![성공적인 통과 인증에 대 한 감사 레코드의 예](media/PassThroughAuth1.png)

   위한. 이 필드는 조직의 Azure AD에서 조직에 있는 리소스에 액세스 하려고 한 사용자를 찾을 수 없음을 나타냅니다.

   b. 이 필드에는 조직의 리소스에 액세스 하려고 한 외부 사용자의 UPN이 표시 됩니다. 이 사용자 ID는 감사 레코드의 **사용자** 및 **UserId** 속성 에서도 식별 됩니다.

   &. **ApplicationId** 속성은 로그온 요청을 트리거한 응용 프로그램을 식별 합니다. 이 감사 레코드의 ApplicationId 속성에 표시 되는 00000003-0000-0ff1-ce00-000000000000의 값은 SharePoint Online을 나타냅니다. 비즈니스용 OneDrive에도 동일한 ApplicationId가 있습니다.

   &. 통과 인증이 성공 했음을 의미 합니다. 즉, 사용자가 Azure AD에서 인증 되었습니다. 

   e-learning. **RecordType** 값이 **15** 이면 감사 된 작업 (USERLOGGEDIN)은 Azure AD의 STS (보안 토큰 서비스) 로그온 이벤트입니다.

UserLoggedIn 감사 레코드에 표시 되는 다른 속성에 대 한 자세한 내용은 [Office 365 관리 활동 API 스키마](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#azure-active-directory-base-schema)의 Azure AD 관련 스키마 정보를 참조 하십시오.

다음은 통과 인증으로 인해 **사용자가** 감사 작업을 성공적으로 로그인 한 경우의 두 가지 예입니다. 

  - Microsoft 계정 (예: SaraD@outlook.com)이 있는 사용자가 fourthcoffee.onmicrosoft.com의 비즈니스용 OneDrive 계정에 있는 문서에 액세스 하려고 했지만 SaraD@outlook.com의 해당 guest 사용자 계정이 아닙니다. fourthcoffee.onmicrosoft.com

  - Office 365 조직에서 회사 또는 학교 계정 (예: pilarp@fabrikam.onmicrosoft.com)을 가진 사용자가 contoso.onmicrosoft.com에서 SharePoint 사이트에 액세스 하려고 했지만 pilarp@fabrikam.com의 해당 guest 사용자 계정이 아닙니다. contoso.onmicrosoft.com


### <a name="tips-for-investigating-successful-logins-resulting-from-pass-through-authentication"></a>통과 인증의 성공한 로그인을 조사 하기 위한 팁

- **사용자가 로그인 한** 감사 레코드에서 식별 된 외부 사용자가 수행한 활동에 대 한 감사 로그를 검색 합니다. **사용자** 상자에 외부 사용자에 대 한 UPN을 입력 하 고 시나리오와 관련이 있는 경우 날짜 범위를 사용 합니다. 예를 들어 다음과 같은 검색 조건을 사용 하 여 검색을 만들 수 있습니다.

   ![외부 사용자가 수행한 모든 작업을 검색 합니다.](media/PassThroughAuth2.png)

    **사용자가 로그인** 한 활동 외에, 외부 사용자와 조직 내의 사용자를 표시 하는 다른 감사 레코드가 반환 되거나 외부 사용자가 해당 문서에 액세스, 수정 또는 다운로드를 수행할 수 있습니다. 과 (와) 공유 되었습니다.

- **사용자가 로그인** 한 감사 레코드에 의해 식별 된 외부 사용자와 파일이 공유 되었음을 나타내는 SharePoint 공유 활동을 검색 합니다. 자세한 내용은 [Office 365 감사 로그에서 공유 감사 사용](use-sharing-auditing.md)을 참조 하십시오.

- Excel을 사용 하 여 외부 사용자와 관련 된 다른 작업을 검색할 수 있도록 조사와 관련 된 레코드를 포함 하는 감사 로그 검색 결과를 내보냅니다. 자세한 내용은 [감사 로그 기록 내보내기, 구성 및 보기](export-view-audit-log-records.md)를 참조 하세요.
