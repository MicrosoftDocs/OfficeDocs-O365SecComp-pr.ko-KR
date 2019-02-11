---
title: 조직의 감독 정책 구성
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: 검토를 위해 직원 통신 캡처 감독 검토 정책을 설정 합니다.
ms.openlocfilehash: 898ef9951ea20dec1e0cc6c28ad1ed6f9a0ded6e
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29768039"
---
# <a name="configure-supervision-policies-for-your-organization"></a>조직의 감독 정책 구성

감독 정책을 사용 하 여 내부 또는 외부 검토자가 검사에 대 한 직원 통신을 캡처합니다. 감독 정책 하는 방법 조직에서 통신을 모니터링 하는 방법에 대 한 자세한 내용은 [Office 365의 감독 정책](supervision-policies.md)을 참조 하십시오.

> [!NOTE]
> 감독 정책에 의해 모니터링 하는 사용자가 고급 준수 추가 기능으로 Office 365 Enterprise E3 라이선스가 있어야 하거나 Office 365 Enterprise E5 구독에 포함 되어야 합니다. 기존 엔터프라이즈 e 5 플랜이 감독 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.
  
설정 하 고 감독을 사용 하 여 Office 365 조직에서 다음이 단계를 수행 합니다.
  
- **(선택 사항) 1 단계** - [감독에 대 한 그룹 설정](configure-supervision-policies.md#exampledist)

    감독 사용을 시작 하기 전에 사용자가 자신의 통신을 검토 하 고 이러한 검토를 수행 하는 사용자를 결정 합니다. 감독 작동 하는 방법을 보려면 소수의 사용자가 시작 하려는 경우에 지금에 대 한 그룹 설정을 건너뛸 수 있습니다.

- **2 단계 (필수)** - [감독 조직에서 사용할 수 있는 확인](configure-supervision-policies.md#MakeAvailable)

    정책을 설정할 수 있도록 사용자가 직접 감독 검토 역할 그룹에 추가 합니다. 보안 & 준수 센터의에서 **데이터 관리 방식** 에서 **감독** 페이지에 액세스할 수이 역할이 할당 된 모든 사람이 합니다. 전자 메일을 검토 하는 Exchange Online에서 호스팅되는, 각 검토자 [Exchange Online에 대 한 원격 PowerShell 액세스](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell)도 있어야 합니다.

- **(선택 사항) 3 단계** - [구성 사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전/사전을](configure-supervision-policies.md#sensitiveinfo)

    감독 정책에 대 한 중요 한 정보를 사용자 지정 형식 또는 키워드를 사용자 지정 사전을 사용 하 여 필요한 경우 감독 마법사를 시작 하기 전에 만들려는 필요 합니다.

- **4 단계 (필수)** - [감독 정책 설정](configure-supervision-policies.md#setupsuper)

    보안 & 준수 센터의에서 감독 정책을 만들 수 있습니다. 이러한 정책은 어떤 통신은 조직에서 검토 될 수 및 검토를 수행 해야 사용자 지정을 정의 합니다. 통신에는 전자 메일 및 Microsoft 팀의 통신을 위한 타사 플랫폼 통신 (예: Facebook, Twitter 등) 더불어 포함

- **5 단계-(선택 사항)** [새 감독 정책에 따라 테스트](configure-supervision-policies.md#TestPolicy)

    필요에 따라 작동 중인지 확인 하 여 감독 정책을 테스트 규정 준수 전략을 표준을 충족 하는지 확인의 중요 한 부분입니다.

- **6 단계-(선택 사항)** [Outlook 용 추가 기능에 Office 365 감독 대시보드 또는 관리 된 통신을 검토 하려면 OWA를 사용 하지 않으려는 게 검토자를 설정](configure-supervision-policies.md#UseOutlook)

    감독 용 추가 기능에 Outlook에 액세스할 수 검토자가 Outlook 클라이언트 내에서 감독 기능 오른쪽을 평가 하 고 각 항목을 분류 수 있도록 합니다.

<a name="exampledist"> </a>

## <a name="step-1---set-up-groups-for-supervision-optional"></a>1 단계-그룹에 대 한 설정 감독 (선택 사항)

 감독 정책을 만들 때 사용자는 자신의 통신을 검토 하 고 이러한 검토를 수행 하는 사용자를 결정 합니다. 정책, 개인 또는 그룹에 사용자를 식별 하려면 전자 메일 주소를 사용 합니다. 설치 프로그램을 단순화 하려면 검토 자신의 통신을 가진 사용자에 대 한 그룹 및 이러한 통신을 검토 하는 사용자를 위해 그룹을 만듭니다. 그룹을 사용 하는 여러 필요할 수 있습니다-등 사용자의 고유한 두 그룹 간의 통신을 모니터링 하려면 또는 감독 수 없는 하려고 하는 그룹을 지정 하려는 경우. 이 작동 하는 방법에 대 한 자세한 내용은 [예제 메일 그룹](configure-supervision-policies.md#GroupExample) 을 참조 하십시오.
  
조직에서 그룹 내에서 또는 간의 통신을 감독를 Exchange 관리 센터에 메일 그룹을 설정할 ( **받는 사람** 에 게 이동 \> **그룹**). 메일 그룹을 설정 하는 방법에 대 한 자세한 내용은 [Manage 메일 그룹](http://go.microsoft.com/fwlink/?LinkId=613635) 을 참조 하십시오.
  
> [!NOTE]
> 원하는 경우 감독에 대 한 동적 메일 그룹 또는 보안 그룹을 사용할 수도 있습니다. 조직을 보다 적합 하는 경우 이러한 결정 하려면 요구, [메일 사용이 가능한 보안 그룹 관리](http://go.microsoft.com/fwlink/?LinkId=627033)및 [동적 메일 그룹 관리를](http://go.microsoft.com/fwlink/?LinkId=627058)참조 하십시오.
  
<a name="GroupExample"> </a>

### <a name="example-distribution-groups"></a>예시 메일 그룹

이 예에서는 Contoso 재무 국제를 호출 하는 재무 조직에 설정 된 메일 그룹을 포함 합니다.
  
Contoso Financial International에서 미국에 있는 중개인 간 통신 샘플링을 감독해야 합니다. 하지만 해당 그룹 내에 있는 준수 관리자는 감독이 필요하지 않습니다. 이 예에서는 다음 그룹을 만들 수 있습니다.
  
|**이 메일 그룹 설정**|**그룹 주소(별칭)**|**설명**|
|:-----|:-----|:-----|
|모든 미국 중개인 | US_Brokers@Contoso.com | 이 그룹에는 Contoso에서 근무하는 모든 미국 중개인에 대한 전자 메일 주소가 포함되어 있습니다. |
| 모든 미국 준수 관리자 | US_Compliance@Contoso.com  | 이 그룹에는 Contoso에 대 한 작업 하는 모든 미국 기반 규정 준수 관리자에 대 한 전자 메일 주소가 포함 됩니다. 이 그룹이 모든 미국 기반 브로커의 하위 집합 이므로 감독 정책에서이 별칭 면제 규정 준수 관리자 등을 사용할 수 있습니다. |
  
<a name="MakeAvailable"> </a>

## <a name="step-2---make-supervision-available-in-your-organization-required"></a>단계 2-(필수) 조직에서 사용할 수 있는 확인 감독

하려면 **감독** 메뉴 옵션으로 사용할 수 있는 보안 & 준수 센터의에서 감독 검토 관리자 역할을 할당 합니다.
  
이 작업을 수행 하려면 추가 하거나 사용자가 직접 감독 검토 역할 그룹의 구성원으로 또는 새 역할 그룹을 만들 수 있습니다.
  
### <a name="add-members-to-the-supervisory-review-role-group"></a>감독 검토 역할 그룹에 구성원을 추가 합니다.

1. 에 로그인 [https://protection.office.com](https://protection.office.com) Office 365 조직에서 관리 계정에 대 한 자격 증명을 사용 합니다.

2. 보안 & 준수 센터에서에서 **사용 권한 관리**로 이동 합니다.

3. **감독 검토** 역할 그룹을 선택 하 고 편집 아이콘을 클릭 합니다.

4. **구성원** 섹션에서 조직에 대 한 감독 관리 하려는 사람을 추가 합니다.

### <a name="create-a-new-role-group"></a>새 역할 그룹 만들기

1. 에 로그인 [https://protection.office.com](https://protection.office.com) Office 365 조직에서 관리 계정에 대 한 자격 증명을 사용 합니다.

2. 보안 & 준수 센터에서에서 **사용 권한 관리** 로 이동 하 고 추가 클릭 합니다 (**+**).

3. **역할** 섹션에서 추가 클릭 (**+**) **감독 검토 관리자**까지 아래로 스크롤합니다. 이 역할을 역할 그룹을 추가 합니다.

4. **구성원** 섹션에서 조직에 대 한 감독 관리 하려는 사람을 추가 합니다.

역할 그룹 및 사용 권한 하는 방법에 대 한 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.

### <a name="enable-remote-powershell-access-for-reviewers-if-email-is-hosted-on-exchange-online"></a>(전자 메일은 Exchange Online에서 호스팅되는) 하는 경우 검토자에 대 한 원격 PowerShell 액세스를 사용 하도록 설정

1. [Exchange Online PowerShell에 대 한 액세스를 사용 하지 않도록 설정 하거나 사용](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell)에 대 한 지침을 따릅니다.

<a name="sensitiveinfo"> </a>
  
## <a name="step-3---create-custom-sensitive-information-types-or-custom-keyword-dictionaries-optional"></a>3 단계-사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전 (선택 사항) 만들기

기존 사용자 지정 중요 한 정보 유형 또는 감독 정책 마법사에서 사용자 지정 키워드 사전에서를 선택 하기 위해 먼저 필요한 경우 이러한 항목을 만들 필요가 있습니다.

### <a name="create-custom-sensitive-information-types"></a>사용자 지정 중요 한 정보 유형 만들기

1. Office 365 보안 & 준수 센터의에서 새로운 중요 한 정보 유형 만들기 **분류** 로 이동 \> **중요 한 정보 유형** 및 **새 중요 한 정보 유형 마법사**의 단계를 수행 합니다. 다음 사항을 준수 해야합니다.

    - 이름 및 중요 한 정보 형식에 대 한 설명을 정의합니다
    - 근접, 신뢰 수준 및 기본 패턴 요소를 정의 합니다.
    - 선택 항목을 검토 하 고 중요 한 정보 유형 만들기

    자세한 내용은 [사용자 지정 중요 한 정보 유형 만들기](create-a-custom-sensitive-information-type.md)를 참조 합니다.

### <a name="create-custom-keyword-dictionarylexicon"></a>사용자 지정 키워드 사전/사전 만들기

1. 텍스트 편집기 (예: 메모장)를 사용 하 여 감독 정책에서 모니터링 하려는 키워드 용어를 포함 하는 새 파일을 만듭니다. 각 용어는 별도 줄 켜져 있는지 확인 하 고 **유니코드/u t F-16 (거의 Endian)** 형식으로 파일을 저장 합니다.
2. PowerShell을 사용 하 여 Office 365 테 넌 트에 키워드 파일을 가져옵니다. PowerShell 사용 하 여 Office 365에 연결할 [Office 365 보안 & 준수 센터 PowerShell 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)을 참조 하십시오.

    PowerShell 사용 하 여 Office 365에 연결한 후에 키워드 사전을 가져오려면 다음 명령을 실행 합니다.

    ```
    $fileData = Get-Content "your keyword path and file name" -Encoding Byte -ReadCount 0

    New-DlpKeywordDictionary -Name "Name for your keyword dictionary" -Description "optional description for your keyword dictionary" -FileData $fileData
    ```
    자세한 내용은 [키워드 사전 만들기](create-a-keyword-dictionary.md)를 참조 합니다.

3. Office 365 보안 & 준수 센터의에서 새로운 중요 한 정보 유형 만들기 **분류** 로 이동 \> **중요 한 정보 유형** 및 **새 중요 한 정보 유형 마법사**의 단계를 수행 합니다. 다음 사항을 준수 해야합니다.

    - 이름 및 중요 한 정보 형식에 대 한 설명을 정의합니다
    - 일치 하는 요소에 대 한 요구 사항으로 사용자 지정 사전 추가
    - 선택 항목을 검토 하 고 중요 한 정보 유형 만들기

    사용자 지정 사전/용어를 만든 후 [Get DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/get-dlpkeyworddictionary) cmdlet을 사용 하 여 구성 된 키워드를 보고 하 고 또는 추가 하 고, 용어 [집합 DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpkeyworddictionary) cmdlet을 사용 하 여 제거할 수 있습니다.

    자세한 내용은 [사용자 지정 중요 한 정보 유형 만들기](create-a-custom-sensitive-information-type.md)를 참조 합니다.

<a name="setupsuper"> </a>

## <a name="step-4---set-up-a-supervision-policy-required"></a>단계 4-(필수) 감독 정책 설정
  
1. 에 로그인 [https://protection.office.com](https://protection.office.com) Office 365 조직에서 관리 계정에 대 한 자격 증명을 사용 합니다.

2. 보안 & 준수 센터에서에서 **감독**을 선택 합니다.
  
3. **만들기** 를 선택 하 고 정책의 다음 페이지를 설정 하는 마법사를 따릅니다. 마법사를 사용 합니다.

    - 이름 및 설명 정책을 부여 합니다.
    - 사용자 또는 그룹 제외 하려는 선택 포함 하 여 사용자 또는 그룹, 감독을 선택 합니다.
    - 감독 정책 조건을 정의 합니다.
    - 중요 한 정보 유형을 포함 하려는 경우를 선택 합니다. 이것이 기본 및 중요 한 정보를 사용자 지정 항목을 선택할 수 있습니다.
    - 검토 하기 위해 통신의 백분율을 정의 합니다.
    - 정책에 대 한 검토자를 선택 합니다. 개별 사용자 또는 [메일 사용이 가능한 보안 그룹](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups#create-a-mail-enabled-security-group)검토자가 될 수 있습니다.
    - 정책 선택 항목을 검토 하 고 정책을 만듭니다.

<a name="TestPolicy"> </a>

## <a name="step-5---test-your-supervision-policy-optional"></a>5 단계-(선택 사항) 감독 정책에 따라 테스트

감독 정책을 만든 후 것이 사용자가 정의한 조건은 정책에 의해 제대로 적용 되 고 있는지 확인 하는 테스트 하는 것이 좋습니다. 수도 [테스트](create-test-tune-dlp-policy.md) 하려는 데이터 손실 방지 (DLP) 정책에 감독 정책에 중요 한 정보 형식을 포함 하는 경우. 감독 정책을 테스트 하려면 다음 단계를 수행 합니다.

1. 열린 전자 메일 클라이언트 또는 Microsoft 팀의 로그인을 테스트 하려면 정책에 정의 된 관리 된 사용자로 합니다.
2. 전자 메일 또는 감독 정책에서 정의한 조건을 충족 하는 Microsoft 팀의 채팅을 보냅니다. 이 키워드, 첨부 파일 크기, 도메인 등 수 있습니다. 정책에 구성 된 조건부 설정을 너무 제한적 또는 너무 융통성이 인지를 확인 하 고 있는지 확인 하십시오.

    > [!Note]
    > 전자 메일이 정의 된 정책에 따라 달라 집니다 거의 실시간이에서 처리 되 고이 정책을 구성 하는 후에 즉시 테스트할 수 있습니다. Microsoft 팀의 채팅 정책에서 완벽 하 게 처리 하는 데 24 시간까지 걸릴 수 있습니다. 

3. 감독 정책에서 지정 된 검토자도 Office 365 테 넌 트에 로그인 합니다. **감독**이동 > *Your 사용자 지정 정책* > **열기** 정책에 대 한 보고서를 볼 수 있습니다.

<a name="UseOutlook"> </a>

## <a name="step-6---set-up-outlook-add-in-for-reviewers-optional"></a>단계 6-설정 Outlook 추가 기능에서 검토자에 대 한 (선택 사항)

통신을 검토 하려면 Office 365 또는 웹에 있는 Outlook에서 감독 대시보드를 사용 하는 대신 Outlook을 사용 하 여 원하는 검토자 감독 추가 기능을 자신의 Outlook 클라이언트에 대 한 설치 해야 합니다.

### <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a>1 단계: 감독 사서함에 대 한 주소를 복사 합니다.

Outlook 데스크톱 용 추가 기능에서 설치를 사용 하 여 감독 정책 설치의 일부로 만들어진 감독 사서함에 대 한 주소가 필요 합니다.
  
> [!NOTE]
> 다른 사람이 만든 정책, 하는 경우이 주소를 추가 기능을 설치 하도록 받이 필요 합니다.

 **감독 사서함 주소를 찾으려면**
  
1. 에 로그인은 [보안 &amp; 준수 센터](https://protection.office.com) Office 365 조직에서 관리 계정에 대 한 자격 증명을 사용 합니다.

2. **감독**로 이동 합니다.

3. 수집 하 고 검토 하려는 통신 감독 정책을 클릭 합니다.

4. 정책 세부 정보 플라이 아웃 **감독 사서함**주소를 복사 합니다.<br/>![강조 표시 된 감독 사서함 주소를 표시 한 감독 정책 세부 정보 플라이 아웃의 ' 감독 사서함 ' 섹션](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
### <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a>2 단계: Outlook 데스크톱 액세스에 대 한 감독 사서함 구성

다음으로, 검토자는 두 Exchange Online PowerShell 명령을 실행 하 여 Outlook 감독 사서함에 연결할 수 있도록 해야 합니다.
  
1. Exchange Online PowerShell에 연결 합니다. [어떻게 해야 합니까?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)

2. 여기서 *SupervisoryReview{GUID}@domain.onmicrosoft.com* 는 위의 1 단계에서에서 복사한 주소가 고 *사용자* 가 3 단계에서에서 감독 사서함에 연결 하는 검토자의 이름에 다음 명령을 실행 합니다.

    ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```

    ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```

3. 대기 아래 3 단계로 이동 하기 전에 1 시간 이상입니다.

### <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a>3 단계: 감독 사서함에 연결 하 여 Outlook 프로필 만들기

마지막 단계에 대 한 검토자 감독 사서함에 연결 하는 Outlook 프로필을 만들려면 해야 합니다.

> [!NOTE]
> 새 Outlook 프로필을 만들려면 Windows 제어판의 메일 설정을 사용 합니다. 이러한 설정으로 이동 하기 위해 취할 경로 사용 하는 Windows 운영 체제 (Windows 7, Windows 8 또는 Windows 10) 하 고 설치 된 outlook 버전에 따라 달라질 수 있습니다.
  
1. 제어판을 열고 위쪽 창에 **검색** 상자에서 **메일**을 입력 합니다.<br/>(확실 하지 않은 경우 제어판으로 이동 하는 방법? 참조 [제어판이?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))
  
2. **메일** 앱을 엽니다.

3. **메일 설정-Outlook** **프로필 보기**를 클릭 합니다.<br/>![' 메일 설정-Outlook'' 프로필 보기 ' 단추를 강조 표시 된 대화 상자](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. **메일** **추가**클릭 합니다. 그런 다음, **새 프로필**(예: **감독**) 감독 사서함에 대 한 이름을 입력 합니다.<br/>![' 프로 파일 이름 ' 상자에 대화명 '감독' ' 새 프로필 ' 대화 상자](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. **Office 365에 연결 Outlook** **다른 계정으로 연결**을 클릭 합니다.<br/>![강조 표시 한 '다른 계정으로 연결' 링크와 함께 ' Office 365로 Outlook에 연결 ' 메시지](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. **자동 계정 설정**,에서 **수동 설치 또는 추가 서버 유형**, 선택 하 고 **** 을 클릭 합니다.

7. **계정 유형 선택** **Office 365**를 선택 합니다. 그런 다음, **전자 메일 주소** 상자에서 이전에 복사한 감독 사서함의 주소를 입력 합니다.<br/>![강조 표시 하 고 ' 전자 메일 주소 ' 상자를 표시 하는 Outlook에서 계정 추가 ' 대화의 ' 계정 유형 선택 ' 페이지입니다.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. 대화 상자가 나타나면 Office 365 자격 증명을 입력 합니다.

9. 성공적인를 볼 수 있습니다는 **감독- \<정책 이름\> ** Outlook에서 폴더 목록 보기에 나열 된 폴더입니다.

## <a name="powershell-reference"></a>PowerShell 참조 (영문)

필요한 경우 만들고 수 감독 정책에서 다음 PowerShell cmdlet을 사용 하 여 관리 합니다.

- [새 SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2?view=exchange-ps)
- [Get-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2?view=exchange-ps)
- [집합 SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2?view=exchange-ps)
- [SupervisoryReviewPolicyV2 제거](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2?view=exchange-ps)
- [새 SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule?view=exchange-ps)
- [집합 SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule?view=exchange-ps)
- [Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity)
- [Get-SupervisoryReviewOverallProgressReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewoverallprogressreport)
- [Get-SupervisoryReviewTopCasesReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewtopcasesreport)