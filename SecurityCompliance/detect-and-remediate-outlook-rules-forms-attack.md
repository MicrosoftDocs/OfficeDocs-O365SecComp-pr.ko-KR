---
title: Office 365에서 Outlook 규칙 및 사용자 지정 양식 주입 공격 감지 및 재구성
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 04/23/2018
ms.audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- Strat_O365_IP
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Office 365에서 Outlook 규칙 및 사용자 지정 양식 주입 공격을 인식 하 고 수정 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 214be3e8492c2896d2a4010c30768e41bc149078
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215238"
---
# <a name="detect-and-remediate-outlook-rules-and-custom-forms-injections-attacks-in-office-365"></a>Office 365에서 Outlook 규칙 및 사용자 지정 양식 주입 공격 감지 및 재구성

**요약** Office 365에서 Outlook 규칙 및 사용자 지정 양식 주입 공격을 인식 하 고 수정 하는 방법에 대해 알아봅니다.

## <a name="what-is-the-outlook-rules-and-custom-forms-injection-attack"></a>Outlook 규칙 및 사용자 지정 양식 주입 공격 이란?
공격자가 테 넌 시의 계정을 위반 하 고를 가져온 후에는이를 검색 하 고 제거 하는 방법을 시도해 야 합니다. 이를 지 속성 메커니즘을 설정 하는 것 이라고 합니다. outlook 규칙을 이용 하거나 outlook에 사용자 지정 양식을 삽입 하면 두 가지 방법으로이 작업을 수행할 수 있습니다. 두 경우 모두에서 규칙이 나 양식은 클라우드 서비스에서 데스크톱 클라이언트로 동기화 되므로 클라이언트 소프트웨어의 전체 포맷 및 다시 설치로 인해 주입 메커니즘이 제거 되지 않습니다. 이는 Outlook 클라이언트 소프트웨어가 클라우드의 사서함에 다시 연결 하는 경우 클라우드에서 규칙 및 양식을 다운로드 하기 때문입니다. 규칙 및 양식을 사용 하 고 나면 공격자가 원격 또는 사용자 지정 코드를 실행 하 여 일반적으로 로컬 컴퓨터에 맬웨어를 설치 합니다. 그런 다음 맬웨어가 자격 증명을 다시 도용 하거나 기타 불법 활동을 수행 합니다. 여기서는 클라이언트를 최신 버전으로 패치를 유지 하는 경우 현재 Outlook 클라이언트 기본값이 두 메커니즘을 모두 차단 함에 따라 위협에 취약 하지 않게 된다는 것이 좋습니다. 

공격은 일반적으로 다음 패턴을 따릅니다.

규칙 악용
1. 공격자가 사용자 사용자의 이름과 암호를 도용 합니다.
2. 그러면 공격자가 해당 사용자에 게 Exchange 사서함에 로그인 합니다. 사서함은 exchange online에 있거나 exchange 온-프레미스에 있을 수 있습니다.
3. 그러면 공격자는 사서함에서 규칙 조건과 일치 하는 전자 메일을 받을 때 트리거되는 전달 규칙을 사서함에 만듭니다. 규칙의 조건 및 트리거 전자 메일의 내용은 서로의 내용에 맞게 구성 됩니다.
4. 공격자가 자신의 사서함을 정상적으로 사용 하는 사용자에 게 트리거 전자 메일을 보냅니다.
5. 전자 메일을 받으면 규칙이 트리거됩니다. 규칙의 동작은 일반적으로 원격 (WebDAV) 서버에서 응용 프로그램을 시작 하는 것입니다.
6. 일반적으로 응용 프로그램은 사용자 컴퓨터에 로컬로 [Powershell 제국](https://www.powershellempire.com/)과 같은 맬웨어를 설치 합니다.
7. 공격자는 악성 프로그램을 사용 하 여 로컬 컴퓨터에서 사용자 이름 및 암호 또는 기타 자격 증명을 다시 도용 하 고 다른 악성 작업을 수행할 수 있습니다.

Forms 익스플로잇
1. 공격자가 사용자 사용자의 이름과 암호를 도용 합니다.
2. 그러면 공격자가 해당 사용자에 게 Exchange 사서함을 로그인 합니다. 사서함은 exchange online에 있거나 exchange 온-프레미스에 있을 수 있습니다.
3. 공격자는 사용자 지정 메일 양식 서식 파일을 만들어 사용자의 사서함에 삽입 합니다.  사용자 지정 양식은 사서함이 사용자 지정 양식을 로드 해야 하는 전자 메일을 받을 때 트리거됩니다. 사용자 지정 양식 및 전자 메일 형식은 각각에 맞게 구성 됩니다.
4. 공격자가 사용자에 게 자신의 사서함을 정상적으로 사용 하는 트리거 전자 메일을 보냅니다.
5. 전자 메일을 받으면 양식이 로드 된 것입니다. 폼이 원격 (WebDAV) 서버의 응용 프로그램을 시작 합니다.
6. 일반적으로 응용 프로그램은 사용자 컴퓨터에 로컬로 [Powershell 제국](https://www.powershellempire.com/)과 같은 맬웨어를 설치 합니다.
7. 공격자는 악성 프로그램을 사용 하 여 로컬 컴퓨터에서 사용자 이름 및 암호 또는 기타 자격 증명을 다시 도용 하 고 다른 악성 작업을 수행할 수 있습니다.


## <a name="what-a-rules-and-custom-forms-injection-attack-might-look-like-office-365"></a>규칙 및 사용자 지정 양식 주입 공격이 Office 365 처럼 보일 수 있는 것은 무엇 인가요?

이러한 유지 메커니즘은 사용자가 발견할 가능성이 없으며 일부 경우에도 표시 되지 않을 수도 있습니다.  이 문서에서는 아래 나열 된 7 가지 기호 (손상 징후)를 찾는 방법을 설명 합니다. 이러한 항목 중 하나라도 발견 되 면 업데이트 관리 단계를 수행 해야 합니다.

- 규칙 손상의 지표
    - 응용 프로그램 시작
    - 규칙에서 EXE, ZIP 또는 URL을 참조 합니다.
    - 로컬 컴퓨터에서 Outlook PID 로부터 온 새 프로세스 시작을 찾습니다.
- 사용자 지정 양식 손상 표시기 
    - 사용자 지정 양식이 자체 메시지 클래스로 저장 되어 있어야 합니다.
    - 메시지 클래스에 실행 코드가 포함 되어 있습니다.
    - 일반적으로 개인 양식 라이브러리 또는 받은 편지함 폴더에 저장 됩니다.
    - 양식의 이름을 IPM. 참고. [사용자 지정 이름]

## <a name="steps-for-finding-signs-of-this-attack-and-confirming-it"></a>이 공격의 신호를 찾고 확인 하기 위한 단계
이러한 두 방법 중 하나를 사용 하 여 공격을 확인할 수 있습니다.
- Outlook 클라이언트를 사용 하 여 각 사서함의 규칙과 양식을 수동으로 검사 합니다.  이 방법은 완벽 하지만 확인 해야 하는 사용자가 많은 경우 사서함 사용자에 게 시간이 오래 걸릴 수 있습니다.  또한 확인을 실행 하는 컴퓨터를 위반할 수도 있습니다.
- [Get-AllTenantRulesAndForms](https://github.com/OfficeDev/O365-InvestigationTooling/blob/master/Get-AllTenantRulesAndForms.ps1) PowerShell 스크립트를 사용 하 여 테 넌 시의 모든 사용자에 대 한 모든 메일 전달 규칙 및 사용자 지정 양식을 자동으로 덤프 합니다. 이 방법은 오버 헤드가 가장 빠르고 가장 안전한 방법입니다.


### <a name="confirm-the-rules-attack-using-the-outlook-client"></a>규칙 공격이 Outlook 클라이언트를 사용 하 여 공격 하는지 확인
1. 사용자로 사용자 Outlook 클라이언트를 엽니다.  사용자가 자신의 사서함에 대 한 규칙을 검사 해야 할 수 있습니다.
2. Outlook의 2007, 2010 또는 2013 버전에서 규칙 인터페이스를 여는 방법에 대 한 절차를 보려면 rules 문서를 [사용 하 여 전자 메일 메시지 관리](https://support.office.com/article/manage-email-messages-by-using-rules-c24f5dea-9465-4df4-ad17-a50704d66c59#ID0EAABAAA=2010) 를 참조 하세요.
3. 사용자가 만들지 않은 규칙 또는 의심 스러운 이름이 있는 규칙 또는 규칙을 찾습니다.
4. 규칙 설명에서 시작 및 응용 프로그램에 대 한 규칙 작업을 확인 하거나를 참조 하세요. EXE,를 차례로 실행 합니다. ZIP 파일을 찾거나 URL을 시작할 수 없습니다.
5. Outlook 프로세스 ID를 사용 하 여 시작 되는 새 프로세스를 찾습니다.  [프로세스 ID 찾기를](https://docs.microsoft.com/windows-hardware/drivers/debugger/finding-the-process-id)참조 합니다.

### <a name="steps-to-confirm-the-forms-attack-using-the-outlook-client"></a>Outlook 클라이언트를 사용 하 여 폼 공격을 확인 하는 단계
1. 사용자로 사용자 Outlook 클라이언트를 엽니다.
2. 사용자 버전의 Outlook에 대 한 [개발 도구 탭 표시](https://support.office.com/article/show-the-developer-tab-e1192344-5e56-4d45-931b-e5fd9bea2d45) 의 단계를 수행 합니다.
3. Outlook에서 지금 볼 수 있는 개발자 탭을 열고 **양식 디자인을**클릭 합니다.
4. **찾는** 출처 목록에서 **받은 편지함** 을 선택 합니다. 사용자 지정 폼을 찾습니다.  사용자 지정 폼은 더 이상 사용할 수 없지만 사용자 지정 폼이 있는 경우에는 보다 깊이 있는 모양으로 볼 수 있습니다.
5. 사용자 지정 양식, 특히 숨김으로 표시 된 폼을 조사 합니다.
6. 사용자 지정 양식을 열고 **양식** 그룹에서 **코드 보기** 를 클릭 하 여 양식이 로드 될 때 실행 되는 작업을 확인 합니다.

### <a name="steps-to-confirm-the-rules-and-forms-attack-using-powershell"></a>PowerShell을 사용 하 여 규칙 및 폼 공격을 확인 하는 단계
규칙 또는 사용자 지정 양식 공격을 확인 하는 가장 간단한 방법은 Get-AllTenantRulesAndForms PowerShell 스크립트를 실행 하는 것입니다 [.](https://github.com/OfficeDev/O365-InvestigationTooling/blob/master/Get-AllTenantRulesAndForms.ps1)  이 스크립트는 테 넌 트의 모든 사서함에 연결 되며 모든 규칙과 양식을 두 개의 .csv 파일로 덤프 합니다.

#### <a name="pre-requisites"></a>필수 조건
스크립트에서 규칙 및 양식을 읽기 위해 테 넌 트의 모든 사서함에 연결 하므로 스크립트를 실행 하려면 전역 관리자 권한이 필요 합니다.

1. 로컬 관리자 권한이 있는 스크립트를 실행 하는 컴퓨터에 로그인 합니다.
2. GitHub에서 Get-AllTenantRulesAndForms 스크립트를 실행 하는 데 사용할 폴더에 다운로드 하거나 복사 합니다.  이 스크립트는이 폴더, MailboxFormsExport-yyyy-mm-dd 및 MailboxRulesExport-yyyy-mm-dd에 대해 두 개의 날짜 스탬프가 찍힌 파일을 만듭니다.
3. 관리자로 PowerShell 인스턴스를 열고 스크립트를 저장 한 폴더를 엽니다.
4. `.\Get-AllTenantRulesAndForms.ps1`.\Get-AllTenantRulesAndForms.ps1와 같이이 PowerShell 명령줄을 실행 합니다.

#### <a name="interpreting-the-output"></a>출력 해석

MailboxRulesExport-** yyyy-mm-dd – 응용 프로그램 또는 실행 파일이 포함 된 작업 조건에 대해 행 당 하나씩 규칙을 검사 합니다.
- ActionType (A 열)-"ID_ACTION_CUSTOM" 값이 표시 되는 경우이 규칙은 악성 것일 수 있습니다.
- IsPotentiallyMalicious (열 D)-이 값이 "TRUE" 인 경우 규칙은 악성이 될 수 있습니다.
- actioncommand (column G)-.exe, .zip 확장명을 가진 파일이 나 URL을 참조 하는 항목을 나열 하는 경우 해당 규칙이 악성 인 것 같습니다.

MailboxFormsExport-** yyyy-mm-dd-.csv-일반적으로 사용자 지정 양식을 사용 하는 것은 드문 일입니다.  이 통합 문서에서 찾을 수 있으면 해당 사용자의 사서함을 열고 양식 자체를 검사 합니다.  조직에서 의도적으로 고의로 추가 하지 않은 경우 악성이 될 수 있습니다.



## <a name="how-to-stop-and-remediate-the-outlook-rules-and-forms-attack"></a>Outlook 규칙 및 폼 공격을 중지 하 고 수정 하는 방법
이러한 공격 중 하나에 대 한 증거를 발견 하면 관리가 간단해 지 며 사서함에서 규칙이 나 양식을 삭제 하기만 하면 됩니다. Outlook 클라이언트에서이 작업을 수행 하거나 원격 PowerShell을 사용 하 여 규칙을 제거할 수 있습니다.

### <a name="using-outlook"></a>Outlook 사용
1. 사용자가 Outlook과 함께 사용한 모든 장치를 확인 합니다.  모든 사용자는 잠재적인 맬웨어를 청소 해야 합니다.  모든 장치를 청소할 때까지 사용자가 로그온 하 고 전자 메일을 사용할 수 없도록 합니다.
2. 각 장치에 대 한 [규칙 삭제](https://support.office.com/article/Delete-a-rule-2F0E7139-F696-4422-8498-44846DB9067F) 의 단계를 수행 합니다.
3. 다른 맬웨어가 있는지 확실 하지 않은 경우에는 장치에 모든 소프트웨어를 포맷 하 고 다시 설치할 수 있습니다.  모바일 장치의 경우 제조업체의 단계에 따라 장치를 공장 이미지로 다시 설정할 수 있습니다.
4. 최신 버전의 Outlook을 설치 합니다.  현재 Outlook 버전에서는 두 가지 유형의 공격을 기본적으로 차단 합니다.
5. 사서함의 모든 오프 라인 복사본을 제거한 후에는 사용자의 암호를 다시 설정 하 고 (고품질 1 사용), MFA를 사용 하도록 설정 하지 않은 경우 [Office 365 사용자를 위해 다단계 인증 설치](https://support.office.com/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6) 의 단계를 수행 합니다. 이렇게 하면 사용자의 자격 증명이 다른 방법 (예: 피싱 또는 암호 다시 사용)을 통해 노출 되지 않습니다.

### <a name="using-powershell"></a>PowerShell 사용
위험한 규칙을 제거 하거나 사용 하지 않도록 설정 하는 데 사용할 수 있는 두 가지 원격 PowerShell cmdlet이 있습니다. 단계를 수행 하세요.
 
Exchange 서버에 있는 사서함에 대 한 단계

1. 원격 PowerShell을 사용 하 여 Exchange 서버에 연결 합니다. [원격 PowerShell을 사용 하 여 Exchange server에 연결](https://docs.microsoft.com/powershell/exchange/exchange-server/connect-to-exchange-servers-using-remote-powershell?view=exchange-ps)의 단계를 수행 합니다.
2. 단일 규칙, 여러 규칙 또는 사서함의 모든 규칙을 완전히 제거 하려면 [받은 편지함 제거 규칙 cmdlet ](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Remove-InboxRule?view=exchange-ps)을 사용 하 여 사서함에서 하나, 여러 개 또는 모든 규칙을 완전히 제거 합니다.
3. 자세히 조사를 위해 규칙 및 해당 내용을 유지 하려면 [disable-inboxrule cmdlet](https://technet.microsoft.com/en-us/library/dd298120(v=exchg.160).aspx)을 사용 합니다. 

Exchange Online의 사서함에 대 한 단계
1. [PowerShell을 사용 하 여 Exchange Online에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)의 단계를 수행 합니다.
2.  단일 규칙, 여러 규칙 또는 사서함의 모든 규칙을 완전히 제거 하려는 경우 [받은 편지함 제거 규칙 cmdlet](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Remove-InboxRule?view=exchange-ps)을 사용 합니다.
3.  자세히 조사를 위해 규칙 및 해당 내용을 유지 하려면 [disable-inboxrule cmdlet](https://technet.microsoft.com/en-us/library/dd298120(v=exchg.160).aspx)을 사용 합니다. 

## <a name="how-to-minimize-future-attacks"></a>향후 공격을 최소화 하는 방법

### <a name="first-protect-your-accounts"></a>1: 계정 보호

규칙 및 양식 익스플로잇은 사용자 계정 중 하나를 도용 하거나 침해 한 후에만 공격자에 의해 사용 됩니다. 따라서 조직에 대해 이러한 악용을 사용 하는 것을 방지 하는 첫 번째 단계는 사용자 계정을 적극적으로 보호 하는 것입니다.  계정이 침해 되는 가장 일반적인 몇 가지 방법은 피싱 또는 [암호 spraying](http://www.dabcc.com/microsoft-defending-against-password-spray-attacks/) 공격을 통해 발생 합니다.



사용자 계정을 보호 하는 가장 좋은 방법은 특히 관리자 계정을 사용 하는 것이 [Office 365 사용자에 대해 multi-factor authentication을 설정](https://support.office.com/article/set-up-multi-factor-authentication-for-office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6)하는 것입니다.  다음 작업도 수행 해야 합니다.
<ol>
    <li>사용자 계정을 <a href="https://docs.microsoft.com/azure/active-directory/active-directory-view-access-usage-reports">액세스 하 고 사용</a>하는 방법을 모니터링 합니다. 초기 위반을 막을 수는 없지만 위반의 기간과 영향을 더 일찍 검색 하는 것은 단축 됩니다. 다음을 사용할 수 있습니다. <a href="https://support.office.com/article/overview-of-office-365-cloud-app-security-81f0ee9a-9645-45ab-ba56-de9cbccab475">Office 365 Cloud App Security 정책을</a> 사용 하 여 계정을 모니터링 하 고 비정상적인 활동에 대 한 경고를 할 수도 있습니다.<ol type="a">
            <li><b>여러 번 실패 한 로그인 시도</b> 이 정책은 사용자의 환경에 프로필을 지정 하 고 알려진 기준에 따라 단일 세션에서 여러 로그인 작업을 수행 하는 경우 경고를 트리거합니다.</li>
            <li><b>불가능 한 여행</b> - 이 정책은 작업 환경에 프로 파일을 만들고, 두 위치 사이의 예상 이동 시간 보다 짧은 기간 동안 서로 다른 위치에 있는 동일한 사용자가 활동을 검색 하는 경우 경고를 트리거합니다. 이는 다른 사용자가 동일한 자격 증명을 사용 하 고 있음을 나타낼 수 있습니다. 이 비정상적인 동작을 검색 하는 경우 초기 학습 기간이 7 일 동안 새 사용자의 작업 패턴을 학습 하는 데 사용 됩니다.</li>
            <li><b>비정상적으로 가장 된 활동 (사용자에 의해)</b> - 이 정책은 사용자가 사용 하는 환경의 프로필을 지정 하 고 배운 기준에 따라 단일 세션에서 여러 개의 가장 된 활동을 수행할 때 경고를 트리거합니다.</li>
        </ol>
    </li>
    <li><a href="https://securescore.office.com/">Office 365 보안 점수</a> 와 같은 도구를 활용 하 여 계정 보안 구성 및 동작을 관리 합니다. 
    </li>
</ol> 

### <a name="second-keep-your-outlook-clients-current"></a>두 번째: Outlook 클라이언트를 최신 상태로 유지
Outlook 2013의 전체 업데이트 및 패치 버전 및 2016 "응용 프로그램 시작" 규칙/양식 작업을 기본적으로 사용 하지 않도록 설정 합니다.  이를 통해 공격자가 계정을 위반 하더라도 규칙 및 양식 동작이 차단 되는 것을 확인할 수 있습니다.  [Office 업데이트 설치](https://support.office.com/article/Install-Office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)의 단계에 따라 최신 업데이트 및 보안 패치를 설치할 수 있습니다.

다음은 Outlook 2013 및 2016 클라이언트용 패치 버전입니다.
- Outlook 2013:15.0.4937.1000 이상
- Outlook 2016:16.0.4534.1001 이상

개별 보안 패치에 대 한 자세한 내용은 다음 항목을 참조 하십시오.

- [Outlook 2013 보안 패치](https://support.microsoft.com/en-us/help/3191938) 
- [Outlook 2016 보안 패치](https://support.microsoft.com/en-us/help/3191883)

### <a name="third-monitor-your-outlook-clients"></a>세 번째: Outlook 클라이언트 모니터링
패치와 업데이트가 설치 된 경우에도 공격자가 로컬 컴퓨터 구성을 변경 하 여 "응용 프로그램 시작" 동작을 다시 사용 하도록 설정할 수 있습니다. [고급 그룹 정책 관리](https://docs.microsoft.com/microsoft-desktop-optimization-pack/agpm/) 를 사용 하 여 클라이언트에서 로컬 컴퓨터 정책을 모니터링 하 고 적용할 수 있습니다.  
[64 비트 버전의 Windows를 사용 하 여 시스템 레지스트리를 보는 방법](https://support.microsoft.com/en-us/help/305097/how-to-view-the-system-registry-by-using-64-bit-versions-of-windows)의 정보를 사용 하 여 "시작 응용 프로그램"이 레지스트리의 재정의를 통해 다시 사용 하도록 설정 되었는지 확인할 수 있습니다.  다음 하위 키를 확인 합니다. 

- Outlook 2016: HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Outlook\Security\
- Outlook 2013: HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Outlook\Security\

EnableUnsafeClientMailRules 키를 찾습니다. 이 설정이 있고 1로 설정 되어 있으면 Outlook 보안 패치가 재정의 되 고 컴퓨터가 폼/규칙 공격에 취약할 수 있습니다. 값이 0 이면 "응용 프로그램 시작" 작업을 사용할 수 없습니다.  업데이트 되 고 패치가 적용 된 Outlook 버전이 설치 되어 있고이 레지스트리 키가 없으면 시스템이 이러한 공격에 취약 하지 않습니다.

온-프레미스 Exchange 설치를 사용 하는 고객은 패치가 사용 가능 하지 않은 이전 버전의 Outlook을 차단 하는 것이 좋습니다. 이 프로세스에 대 한 자세한 내용은 [Configure Outlook client 블로킹이](https://technet.microsoft.com/en-us/library/dd335207(v=exchg.150).aspx)문서에 나와 있습니다.

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>cybersecurity pro와 같은 Office 365 보호
Office 365 구독에는 데이터와 사용자를 보호 하는 데 사용할 수 있는 강력한 보안 기능 집합이 포함 되어 있습니다.  office 365 보안 로드맵: office 365 테 넌 트를 보호 하기 위한 Microsoft 권장 모범 사례를 구현 하는 데 [처음 30 일, 90 일 및 그 이상에 대 한 주요 우선 순위](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) 를 사용 합니다.
- 처음 30 일 이내에 수행 해야 하는 작업입니다.  이러한 설정은 즉시 영향을 미치며 사용자에 게 미치는 영향이 낮습니다.
- 90 일 이내에 수행할 작업입니다. 이러한 작업은 계획 하 고 구현 하는 데 다소 시간이 걸리고 보안 환경을 크게 향상 시킵니다.
- 90 일을 초과 합니다. 처음 90 일의 향상 된 기능 빌드는 다음과 같은 작업을 수행 합니다.

## <a name="see-also"></a>참고 항목:
- [악의적인 outlook 규칙](https://silentbreaksecurity.com/malicious-outlook-rules/) SilentBreak 보안 게시물 규칙 벡터에 대 한 자세한 내용은 Outlook 규칙에 대 한 자세한 검토를 제공 합니다. 
- [MAPI over HTTP 및 mailrule](https://sensepost.com/blog/2016/mapi-over-http-and-mailrule-pwnage/) pwnage 온 mailrule pwnage는 Outlook 규칙을 통해 사서함을 사용할 수 있도록 하는 눈금자 라는 도구에 대해 설명 합니다.
- 양식 위협 벡터에 대 한 \에 대 한 [Outlook 양식 및 셸](https://sensepost.com/blog/2017/outlook-forms-and-shells/) 
- [눈금자 코드 베이스](https://github.com/sensepost/ruler)
- [손상 된 눈금자 표시기](https://github.com/sensepost/notruler/blob/master/iocs.md)