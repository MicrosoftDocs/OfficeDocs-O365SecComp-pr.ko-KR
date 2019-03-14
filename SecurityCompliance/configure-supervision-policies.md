---
title: 조직의 감독 정책 구성
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: 검토할 직원 정보를 캡처하기 위해 관리 검토 정책을 설정 합니다.
ms.openlocfilehash: 2e321989934402b833d6190f65d696f4eb7919ca
ms.sourcegitcommit: 547a05da067a8f66fdaccf1cc399afcf863f5a87
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/07/2019
ms.locfileid: "30474159"
---
# <a name="configure-supervision-policies-for-your-organization"></a>조직의 감독 정책 구성

감독 정책을 사용 하 여 내부 또는 외부 검토자가 검사할 직원 통신을 캡처할 수 있습니다. 감독 정책을 통해 조직의 통신을 모니터링 하는 방법에 대 한 자세한 내용은 [Office 365의 감독 정책을](supervision-policies.md)참조 하세요.

> [!NOTE]
> 감독 정책에 따라 모니터링 되는 사용자에 게는 Microsoft 365 E5 규정 준수 라이선스, 고급 준수 추가 기능이 포함 된 office 365 enterprise E3 라이선스 또는 office 365 Enterprise E5 구독에 포함 되어 있어야 합니다.
기존 Enterprise e5 요금제가 없고, 감독을 려 고 하는 경우 [Office 365 Enterprise e 5의 평가판에 등록할](https://go.microsoft.com/fwlink/p/?LinkID=698279)수 있습니다.
  
Office 365 조직에서 감독을 설정 및 사용 하려면 다음 단계를 수행 합니다.
  
- **1 단계 (선택 사항)** - [감독을 위한 그룹 설정](configure-supervision-policies.md#exampledist)

    감독 사용을 시작 하기 전에 의사 소통을 검토 하 고 이러한 검토를 수행할 사용자를 결정 합니다. 소수의 사용자만을 시작 하 여 감독의 작동 방식을 확인 하려는 경우 지금 그룹 설정 건너뛰기를 건너뛸 수 있습니다.

- **2 단계 (필수)** - [조직에서 감독을 사용할 수 있도록 설정](configure-supervision-policies.md#MakeAvailable)

    정책을 설정할 수 있도록 자신을 관리 검토 역할 그룹에 추가 합니다. 이 역할이 할당 된 모든 사용자는 보안 & 준수 센터의 **데이터 거 버 넌 스** 에 있는 **감독** 페이지에 액세스할 수 있습니다. 검토할 전자 메일이 exchange online에서 호스트 되는 경우 각 검토자에 [게 exchange online에 대 한 원격 PowerShell 액세스](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell)권한도 있어야 합니다.

- **3 단계 (선택 사항)** - [사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전/lexicons 구성](configure-supervision-policies.md#sensitiveinfo)

    감독 정책에 대 한 사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전을 사용 해야 하는 경우에는 감독 마법사를 시작 하기 전에 만들어야 합니다.

- **4 단계 (필수)** - [감독 정책 설정](configure-supervision-policies.md#setupsuper)

    보안 & 준수 센터에서 감독 정책을 만듭니다. 이러한 정책은 조직에서 검토할 대상이 되는 통신을 정의 하 고 검토를 수행할 사용자를 지정 합니다. 통신에는 전자 메일 및 Microsoft 팀 통신과 타사 플랫폼 통신 (예: Facebook, Twitter 등)이 포함 됩니다.

- **5 단계-(선택 사항)** [새 감독 정책 테스트](configure-supervision-policies.md#TestPolicy)

    규정 준수 전략이 표준을 충족 하는지 확인 하는 것이 중요 한 역할을 하는 경우에는 감독 정책이 필요에 따라 작동 하도록 테스트 합니다.

- **6 단계-(선택 사항)** [outlook for Office 365 감독 대시보드 또는 웹용 outlook (이전의 outlook web App)을 사용 하지 않고 감독 된 통신을 검토 합니다](configure-supervision-policies.md#UseOutlook) .

    검토자가 outlook 클라이언트 내의 감독 기능에 액세스 하 여 각 항목을 평가 하 고 분류할 수 있도록 outlook을 구성할 수 있습니다.

<a name="exampledist"> </a>

## <a name="step-1---set-up-groups-for-supervision-optional"></a>1 단계-감독에 대 한 그룹 설정 (선택 사항)

 감독 정책을 만들 때 의사 소통을 검토 하 고 이러한 검토를 수행할 사용자를 결정 합니다. 정책에서는 전자 메일 주소를 사용 하 여 개인 이나 사용자 그룹을 식별 합니다. 설정을 단순화 하기 위해 통신을 검토 하 고 해당 통신을 검토할 사용자에 대 한 그룹을 확인할 사용자에 대 한 그룹을 만듭니다. 그룹을 사용 하는 경우에는 서로 다른 두 그룹 간의 통신을 모니터링 하려는 경우 또는 감독 하지 않을 그룹을 지정 하려는 경우에는 여러 가지 사항이 필요할 수도 있습니다. 이 작업 방법에 대 한 자세한 내용은 [예제 메일 그룹](configure-supervision-policies.md#GroupExample) 을 참조 하십시오.
  
조직의 그룹 간 또는 사이에서 통신을 감독할 Exchange 관리 센터에서 메일 그룹을 설정 합니다 ( **받는 사람** \> **그룹**으로 이동). 메일 그룹을 설정 하는 방법에 대 한 자세한 내용은 [메일 그룹 관리](http://go.microsoft.com/fwlink/?LinkId=613635) 를 참조 하세요.
  
> [!NOTE]
> 원하는 경우 동적 메일 그룹 또는 보안 그룹을 감독에 사용할 수도 있습니다. 조직의 요구 사항에 적합 한지 여부를 결정 하는 데 도움이 되도록 [메일 사용이 가능한 보안 그룹 관리](http://go.microsoft.com/fwlink/?LinkId=627033)및 [동적 메일 그룹 관리](http://go.microsoft.com/fwlink/?LinkId=627058)를 참조 하세요.
  
<a name="GroupExample"> </a>

### <a name="example-distribution-groups"></a>메일 그룹 예제

이 예에는 Contoso 재무 국제 지역 이라는 금융 조직에 대해 설정 된 메일 그룹이 포함 되어 있습니다.
  
Contoso 재무 국제에서는 미국의 브로커 간 통신에 대 한 샘플을 감독 해야 합니다. 그러나 해당 그룹 내의 규정 준수 관리자는 감독을 요구 하지 않습니다. 이 예에서는 다음 그룹을 만들 수 있습니다.
  
|**이 메일 그룹 설정**|**그룹 주소 (별칭)**|**설명**|
|:-----|:-----|:-----|
|모든 US 브로커 | US_Brokers@Contoso.com | 이 그룹에는 Contoso에 대해 작업 하는 모든 미국 기반 브로커의 전자 메일 주소가 포함 됩니다. |
| 모든 US 준수 직원 | US_Compliance@Contoso.com  | 이 그룹에는 Contoso에서 근무 하는 모든 미국 기반 규정 준수 관리자의 전자 메일 주소가 포함 됩니다. 이 그룹은 모든 미국 기반 브로커의 하위 집합 이므로이 별칭을 사용 하 여 감독 정책에서 규정 준수 관리자를 제외할 수 있습니다. |
  
<a name="MakeAvailable"> </a>

## <a name="step-2---make-supervision-available-in-your-organization-required"></a>2 단계-조직에서 감독을 사용할 수 있도록 설정 (필수)

보안 & 준수 센터에서 **감독** 을 메뉴 옵션으로 사용 하도록 설정 하려면 관리 검토 관리자 역할이 할당 되어야 합니다.
  
이렇게 하려면 자신을 관리 검토 역할 그룹의 구성원으로 추가 하거나 새 역할 그룹을 만들 수 있습니다.
  
### <a name="add-members-to-the-supervisory-review-role-group"></a>관리 검토 역할 그룹에 구성원 추가

1. Office 365 [https://protection.office.com](https://protection.office.com) 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.

2. 보안 & 준수 센터에서 **사용 권한**으로 이동 합니다.

3. **관리 검토** 역할 그룹을 선택한 다음 편집 아이콘을 클릭 합니다.

4. **구성원** 섹션에서 조직에 대 한 감독을 관리 하려는 사용자를 추가 합니다.

### <a name="create-a-new-role-group"></a>새 역할 그룹 만들기

1. Office 365 [https://protection.office.com](https://protection.office.com) 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.

2. 보안 & 준수 센터에서 **사용 권한** 으로 이동한 다음 추가 (**+**)를 클릭 합니다.

3. **역할** 섹션에서 추가 (**+**)를 클릭 하 고 아래로 스크롤하여 **관리 검토 관리자**를 선택 합니다. 이 역할을 역할 그룹에 추가 합니다.

4. **구성원** 섹션에서 조직에 대 한 감독을 관리 하려는 사용자를 추가 합니다.

역할 그룹 및 사용 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.

### <a name="enable-remote-powershell-access-for-reviewers-if-email-is-hosted-on-exchange-online"></a>검토자에 대해 원격 PowerShell 액세스 사용 (전자 메일이 Exchange Online에서 호스트 되는 경우)

1. [사용 또는 사용 안 함 Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell)에 대 한 지침을 따릅니다.

<a name="sensitiveinfo"> </a>
  
## <a name="step-3---create-custom-sensitive-information-types-or-custom-keyword-dictionaries-optional"></a>3 단계-사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전 만들기 (선택 사항)

감독 정책 마법사에서 기존 사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전을 선택 하려면 먼저 필요한 경우 이러한 항목을 만들어야 합니다.

### <a name="create-custom-sensitive-information-types"></a>사용자 지정 중요 한 정보 유형 만들기

1. Office 365 Security & 준수 센터에서 새 중요 한 정보 유형을 만듭니다. **중요 한 정보** 유형 **분류** \> 로 이동 하 여 **새 중요 한 정보 유형 마법사**의 단계를 따릅니다. 여기에서 다음을 수행 합니다.

    - 중요 한 정보 유형에 대 한 이름 및 설명 정의
    - 근접성, 신뢰 수준 및 주 패턴 요소 정의
    - 선택 항목 검토 및 중요 한 정보 유형 만들기

    자세한 내용은 [사용자 지정 중요 한 정보 유형 만들기](create-a-custom-sensitive-information-type.md)를 참조 하십시오.

### <a name="create-custom-keyword-dictionarylexicon"></a>사용자 지정 키워드 사전/어휘 만들기

1. 메모장과 같은 텍스트 편집기를 사용 하 여 감독 정책에서 모니터링할 키워드 용어를 포함 하는 새 파일을 만듭니다. 각 용어가 별도의 줄에 있는지 확인 하 고 파일을 **유니코드/u t f-16 (꼬마)** 형식으로 저장 합니다.
2. PowerShell을 사용 하 여 Office 365 테 넌 트에 키워드 파일을 가져옵니다. PowerShell을 사용 하 여 office 365에 연결 하려면 [connect to office 365 Security & 준수 센터 PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)를 참조 하세요.

    PowerShell을 사용 하 여 Office 365에 연결한 후에 키워드 사전을 가져오려면 다음 명령을 실행 합니다.

    ```
    $fileData = Get-Content "your keyword path and file name" -Encoding Byte -ReadCount 0

    New-DlpKeywordDictionary -Name "Name for your keyword dictionary" -Description "optional description for your keyword dictionary" -FileData $fileData
    ```
    자세한 내용은 [Create a keyword dictionary](create-a-keyword-dictionary.md)를 참조 하십시오.

3. Office 365 Security & 준수 센터에서 새 중요 한 정보 유형을 만듭니다. **중요 한 정보** 유형 **분류** \> 로 이동 하 여 **새 중요 한 정보 유형 마법사**의 단계를 따릅니다. 여기에서 다음을 수행 합니다.

    - 중요 한 정보 유형에 대 한 이름 및 설명 정의
    - 일치 요소에 대 한 요구 사항으로 사용자 지정 사전 추가
    - 선택 항목 검토 및 중요 한 정보 유형 만들기

    사용자 지정 사전/어휘를 만든 후에는 [DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/get-dlpkeyworddictionary) cmdlet을 사용 하 여 구성 된 키워드를 보거나 [DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpkeyworddictionary) cmdlet을 사용 하 여 용어를 추가 및 제거할 수 있습니다.

    자세한 내용은 [사용자 지정 중요 한 정보 유형 만들기](create-a-custom-sensitive-information-type.md)를 참조 하십시오.

<a name="setupsuper"> </a>

## <a name="step-4---set-up-a-supervision-policy-required"></a>4 단계-감독 정책 설정 (필수)
  
1. Office 365 [https://protection.office.com](https://protection.office.com) 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.

2. 보안 & 준수 센터에서 **감독**을 선택 합니다.
  
3. **만들기** 를 선택 하 고 마법사의 지시에 따라 다음과 같은 정책 페이지를 설정 합니다. 마법사를 사용 하 여 다음을 수행할 수 있습니다.

    - 정책에 이름과 설명을 지정 합니다.
    - 제외할 사용자 또는 그룹 선택을 비롯 하 여 감독할 사용자 또는 그룹을 선택 합니다.
    - 감독 정책 조건을 정의 합니다.
    - 중요 한 정보 유형을 포함 하 고 싶은 경우 선택 합니다. 여기에서 기본 및 사용자 지정 중요 한 정보 유형을 선택할 수 있습니다.
    - 검토할 통신의 비율을 정의 합니다.
    - 정책에 대 한 검토자를 선택 합니다. 검토자는 개별 사용자 또는 [메일 사용이 가능한 보안 그룹이](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups#create-a-mail-enabled-security-group)될 수 있습니다.
    - 정책 선택을 검토 하 고 정책을 만듭니다.

<a name="TestPolicy"> </a>

## <a name="step-5---test-your-supervision-policy-optional"></a>5 단계-감독 정책 테스트 (선택 사항)

감독 정책을 만든 후에는 테스트를 통해 정의한 조건이 정책에 의해 적절 하 게 적용 되는지 확인 하는 것이 좋습니다. 또한 감독 정책에 중요 한 정보 유형이 포함 되어 있는 경우 [DLP (데이터 손실 방지) 정책을 테스트할](create-test-tune-dlp-policy.md) 수도 있습니다. 다음 단계에 따라 감독 정책을 테스트 합니다.

1. 테스트할 정책에 정의 된 감독 된 사용자로 로그인 한 전자 메일 클라이언트 또는 Microsoft 팀을 엽니다.
2. 감독 정책에 정의한 기준을 충족 하는 전자 메일 또는 Microsoft 팀 채팅을 보냅니다. 키워드, 첨부 파일 크기, 도메인 등이 될 수 있습니다. 정책에서 구성 된 조건부 설정이 너무 제한적 이거나 너무 lenient 인지 확인 합니다.

    > [!Note]
    > 정의 된 정책이 적용 되는 전자 메일은 거의 실시간으로 처리 되며 정책이 구성 된 직후에 테스트할 수 있습니다. Microsoft 팀의 채팅에는 정책에서 전체 프로세스를 수행 하는 데 최대 24 시간이 걸릴 수 있습니다. 

3. 감독 정책에 지정 된 검토자로 Office 365 테 넌 트에 로그인 합니다. *사용자 지정 정책이* > **열려** 있는 **감독** > 을 탐색 하 여 정책에 대 한 보고서를 확인 합니다.

<a name="UseOutlook"> </a>

## <a name="step-6---configure-outlook-for-reviewers-optional"></a>6 단계-Outlook for 검토자별로 구성 (선택 사항)

Office 365에서 감독 대시보드를 사용 하 여 통신을 검토 하는 대신 outlook을 사용 하려는 검토자는 자신의 outlook 클라이언트를 구성 해야 합니다.

### <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a>1 단계: 감독 사서함의 주소 복사

웹용 outlook 데스크톱 또는 outlook에 대 한 검토를 구성 하려면 감독 정책 설정의 일부로 만들어진 감독 사서함의 주소가 필요 합니다.
  
> [!NOTE]
> 다른 사용자가 정책을 만든 경우이 주소에서 추가 기능을 설치 하도록 요청 받아야 합니다.

 **감독 사서함 주소를 찾으려면**
  
1. Office 365 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 [ &amp; 보안 및 준수 센터](https://protection.office.com) 에 로그인 합니다.

2. **감독**으로 이동 합니다.

3. 검토할 통신을 모으는 감독 정책을 클릭 합니다.

4. 정책 세부 정보 플라이 아웃의 **감독 사서함**에서 주소를 복사 합니다.<br/>![감독 사서함 주소가 강조 표시 된 감독 정책의 세부 정보 플라이 아웃의 ' 감독 사서함 ' 섹션](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
### <a name="step-2-configure-the-supervision-mailbox-for-outlook-access"></a>2 단계: Outlook 액세스를 위한 감독 사서함 구성

다음으로, Outlook을 메일 감독 사서함에 연결할 수 있도록 검토자가 몇 개의 Exchange Online PowerShell 명령을 실행 해야 합니다.
  
1. Exchange Online PowerShell에 연결합니다. [어떻게 해야 합니까?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)

2. 다음 명령을 실행 하면 *SupervisoryReview {GUID} @domain onmicrosoft.com* 는 위의 1 단계에서 복사한 주소이 고 *사용자* 는 3 단계에서 감독 사서함에 연결할 검토자의 이름입니다.

    ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```

    ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```

3. 아래 3 단계로 넘어가기 전까지 적어도 1 시간 이상 기다립니다.

### <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a>3 단계: Outlook 프로필을 만들어 감독 사서함에 연결

마지막 단계에서 검토자는 Outlook 프로필을 만들어 감독 사서함에 연결 해야 합니다.

> [!NOTE]
> 새 Outlook 프로필을 만들려면 Windows 제어판의 메일 설정을 사용 합니다. 이러한 설정에 액세스 하기 위해 수행 하는 경로는 사용 중인 windows 운영 체제 (windows 7, windows 8 또는 windows 10)와 설치 된 Outlook 버전에 따라 달라질 수 있습니다.
  
1. 제어판을 열고 창 위쪽의 **검색** 상자에 **Mail**을 입력 합니다.<br/>(제어판을 표시 하는 방법에 대 한 자세한 내용을 확인 하세요. [제어판은 무엇 인가요?](https://support.microsoft.com/help/13764/windows-where-is-control-panel)를 참조 하세요.
  
2. **메일** 앱을 엽니다.

3. **메일 설정-Outlook**에서 **프로필 보기**를 클릭 합니다.<br/>![' 프로필 표시 ' 단추가 강조 표시 된 상태로 ' 메일 설정-Outlook ' 대화 상자](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. **메일**에서 **추가**를 클릭 합니다. 그런 다음 **새 프로필**에 감독 사서함의 이름을 입력 합니다 (예: **감독**).<br/>![' 프로필 이름 ' 상자에 ' 감독 ' 이름을 표시 하는 ' 새 프로필 ' 대화 상자가 있습니다.](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. **Outlook을 Office 365에 연결**에서 **다른 계정에 연결**을 클릭 합니다.<br/>![' 다른 계정에 연결 ' 링크가 강조 표시 된 ' Outlook과 Office 365 연결 ' 메시지](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. **자동 계정 설정**에서 **수동 설치 또는 추가 서버 유형을**선택 하 고 **다음**을 클릭 합니다.

7. **계정 유형 선택**에서 **Office 365**을 선택 합니다. 그런 다음 **전자 메일 주소** 상자에 이전에 복사한 감독 사서함의 주소를 입력 합니다.<br/>![' 전자 메일 주소 ' 확인란이 강조 표시 된 Outlook의 ' 계정 추가 ' 대화 상자에서 ' 계정 유형 선택 ' 페이지입니다.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. 메시지가 나타나면 Office 365 자격 증명을 입력 합니다.

9. 성공 하면 Outlook의 폴더 목록 보기에 **감독 \<정책 이름\> ** 폴더가 표시 됩니다.

## <a name="powershell-reference"></a>PowerShell 참조

필요한 경우 다음 PowerShell cmdlet을 사용 하 여 감독 정책을 만들고 관리할 수 있습니다.

- [remove-supervisoryreviewpolicyv2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2?view=exchange-ps)
- [remove-supervisoryreviewpolicyv2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2?view=exchange-ps)
- [remove-supervisoryreviewpolicyv2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2?view=exchange-ps)
- [remove-supervisoryreviewpolicyv2을 제거 합니다.](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2?view=exchange-ps)
- [set-supervisoryreviewrule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule?view=exchange-ps)
- [set-supervisoryreviewrule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule?view=exchange-ps)
- [SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity)
- [SupervisoryReviewOverallProgressReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewoverallprogressreport)
- [SupervisoryReviewTopCasesReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewtopcasesreport)