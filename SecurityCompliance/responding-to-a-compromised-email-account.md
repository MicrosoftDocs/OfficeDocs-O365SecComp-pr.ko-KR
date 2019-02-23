---
title: Office 365에서 손상된 이메일 계정에 응답
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- Strat_O365_IP
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Office 365에서 손상 된 전자 메일 계정을 인식 하 고 응답 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 6692c63d6cf349af3f3debea10251880d8d1e16c
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223407"
---
# <a name="responding-to-a-compromised-email-account-in-office-365"></a>Office 365에서 손상된 이메일 계정에 응답

**요약** Office 365에서 손상 된 전자 메일 계정을 인식 하 고이에 대응 하는 방법에 대해 알아봅니다.

## <a name="what-is-a-compromised-email-account-in-office-365"></a>Office 365에서 손상 된 전자 메일 계정 이란?
Office 365 사서함, 데이터 및 기타 서비스에 대 한 액세스는 사용자 이름, 암호 또는 PIN과 같은 자격 증명을 사용 하 여 제어 합니다. 의도 하지 않은 사용자가 해당 자격 증명을 도용 하면 도난당 한 자격 증명이 손상 된 것으로 간주 됩니다. 이를 통해 공격자가 원래 사용자로 로그인 하 고 불법 작업을 수행할 수 있습니다. 도난 당한 자격 증명을 사용 하 여 공격자가 사용자의 Office 365 사서함, SharePoint 폴더 또는 사용자의 OneDrive에 있는 파일에 액세스할 수 있습니다. 일반적으로 공격자는 조직 내부 및 외부의 받는 사람에 게 전자 메일을 보내는 것으로 간주 됩니다. 공격자가 외부의 받는 사람에 게 데이터를 전자 메일로 보내는 경우이를 데이터 exfiltration 이라고 합니다.

## <a name="symptoms-of-a-compromised-office-365-email-account"></a>손상 된 Office 365 전자 메일 계정의 현상
사용자가 Office 365 사서함에서 이상한 활동을 확인 하 고 보고할 수 있습니다. 일반적인 몇 가지 증상은 다음과 같습니다.
- 누락 되었거나 삭제 된 전자 메일 같은 의심 스러운 활동입니다.
- 다른 사용자가 보낸 사람의 **보낸 편지함** 폴더에 해당 하는 전자 메일을 사용 하지 않고 손상 된 계정의 전자 메일을 받을 수 있습니다.
- 의도 한 사용자 또는 관리자가 만들지 않은 받은 편지함 규칙이 있는지 여부 이러한 규칙은 전자 메일을 알 수 없는 주소로 자동 전달 하거나 **Notes**, **정크 메일**또는 **RSS 구독** 폴더로 이동할 수 있습니다.
- 사용자의 표시 이름이 전체 주소 목록에서 변경 될 수 있습니다.
- 사용자의 사서함이 차단 된 전자 메일을 보낼 수 없습니다.
- Microsoft outlook 또는 웹용 outlook (이전의 outlook web App)에 있는 보낸 편지함 또는 지운 편지함 폴더에는 일반적인 해킹 당한 계정 메시지 (예: "London에 걸려 온 금액 보내기")가 포함 되어 있습니다.
- 이름, 전화 번호 또는 우편 번호와 같은 이상한 프로필 변경 내용이 업데이트 되었습니다.
- 암호를 여러 번 변경 하는 등의 예외적인 자격 증명을 변경 해야 합니다.
- 메일 전달이 최근에 추가 되었습니다.
- 가짜 은행 서명 또는) 마약 서명과 같은 이상한 서명이 최근에 추가 되었습니다.

사용자가 위의 증상 중 하나를 보고 하면 자세히 조사를 수행 해야 합니다. Office 365 Security & 준수 센터 및 Azure Portal은 손상 된 것으로 의심 되는 사용자 계정의 작업을 조사 하는 데 도움이 되는 도구를 제공 합니다.
- Office 365 보안 & 준수 센터의 통합 감사 로그-의심 스러운 활동이 발생 하기 직전부터 현재 날짜까지까지 영향을 받은 날짜 범위에 대 한 결과를 필터링 하 여 의심 스러운 계정에 대 한 모든 활동을 검토 합니다. 검색 중에는 작업을 필터링 하지 않습니다.
- azure ad 포털에서 사용할 수 있는 azure ad 로그인 로그 및 기타 위험 보고서를 사용 합니다. 다음 열에 있는 값을 검사 합니다.
    - IP 주소 검토
    - 로그인 위치
    - 로그인 시간
    - 로그인 성공 또는 실패

## <a name="how-to-secure-and-restore-email-function-to-a-suspected-compromised-office-365-account-and-mailbox"></a>의심 스러운 Office 365 계정 및 사서함으로 전자 메일 기능을 보호 하 고 복원 하는 방법

> [!VIDEO https://videoplayercdn.osi.office.net/hub/?csid=ux-cms-en-us-msoffice&uuid=RE2jvOb&AutoPlayVideo=false]

사용자의 계정에 대 한 액세스를 다시 받은 후에도 공격자가 백도어 항목을 추가 하 여 공격자가 계정에 대 한 제어권을 계속 해 서 제어할 수 있습니다.

hijacker에서 사용자의 계정을 계속 제어 하지 않도록 하려면 다음 단계를 모두 수행 하 여 계정에 다시 액세스 하는 것이 좋습니다. 이러한 단계는 hijacker에서 계정에 추가 했을 수 있는 모든 백도어 항목을 제거 하는 데 도움이 됩니다. 이러한 단계를 수행한 후에는 컴퓨터가 손상 되지 않았는지 확인 하기 위해 바이러스 검사를 실행 하는 것이 좋습니다.

### <a name="step-1-reset-the-users-password"></a>1 단계 사용자 암호 다시 설정
> [!WARNING]
> 지금은 공격자가 사서함에 액세스할 수 있으므로 전자 메일을 통해 원하는 사용자에 게 새 암호를 보내지 않습니다.

1. 관리자에 게 [office 365 business 암호 재설정](https://support.office.com/article/admins-reset-office-365-business-passwords-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c) 의 다른 사용자를 위해 office 365 business 암호 재설정을 따릅니다.

**참고:**
- 암호가 강력 하 고 암호에 대 문자와 소문자, 숫자가 하나 이상, 특수 문자가 하나 이상 포함 되어 있는지 확인 합니다. 
- 마지막 암호 5 개를 다시 사용 하지 마십시오. 암호 기록 요구 사항에 의해 더 최근 암호를 다시 사용할 수 있더라도 공격자가 추측할 수 없는 항목을 선택 해야 합니다.
- 온-프레미스 id가 Office 365에 페더레이션 되어 있는 경우 온-프레미스에 암호를 변경 해야 하며, 관리자에 게 해당 사용자의 손상을 알려야 합니다.

> [!TIP]
> 특히 관리 권한이 있는 계정에 대 한 손상을 방지 하기 위해 MFA (multi-factor Authentication)를 사용 하는 것이 좋습니다.  [여기](https://support.office.com/en-us/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6)에서 자세히 알아볼 수 있습니다.

### <a name="step-2-remove-suspicious-email-forwarding-addresses"></a>2 단계 의심 스러운 전자 메일 전달 주소 제거
1. **Office 365 관리 센터 > Active Users**를 엽니다.
2. 해당 하는 사용자 계정을 찾아 **메일 설정을**확장 합니다.
3. **전자 메일 전달**에 대해 **편집**을 클릭 합니다.
4. 의심 스러운 전달 주소를 제거 합니다.

### <a name="step-3-disable-any-suspicious-inbox-rules"></a>3 단계 의심 되는 받은 편지함 규칙을 사용 하지 않도록 설정
1. 웹용 Outlook을 사용 하 여 사용자의 사서함에 로그인 합니다.
2. 톱니 바퀴 아이콘을 클릭 하 고 **메일**을 클릭 합니다.
3. **받은 편지함 및 비우기 규칙** 을 클릭 하 고 규칙을 검토 합니다.
4. 의심 스러운 규칙을 사용 하지 않도록 설정 하거나 삭제 합니다.

### <a name="step-4-unblock-the-user-from-sending-mail"></a>4 단계 사용자의 메일 보내기 차단 해제
의심 스러운 사서함을 사용 하 여 스팸 전자 메일을 illicitly 경우 사서함이 메일을 보낼 수 없도록 차단 되었을 가능성이 있습니다.
1. 메일을 보내지 못하도록 사서함의 차단을 해제 하려면 [스팸 전자 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소 제거](https://docs.microsoft.com/Office365/SecurityCompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email )절차를 수행 합니다.

### <a name="step-5-optional-block-the-user-account-from-signing-in"></a>5 단계 옵션: 로그인에서 사용자 계정 차단
> [!IMPORTANT]
> 액세스를 다시 사용 하도록 설정 하는 것이 안전 하다 고 확신할 때까지 의심 스러운 손상 된 계정을 로그인에서 차단할 수 있습니다.

1. Office 365 관리 센터로 이동합니다.
2. Office 365 관리 센터에서 **사용자** 를 선택합니다.
3. 차단할 직원을 선택한 다음 사용자 창의 **로그인 상태** 옆에 있는 **편집** 을 선택 합니다.
4. **로그인 상태** 창에서 **로그인 차단됨** 을 선택한 다음 **저장** 을 선택합니다. 
5. Office 365 관리 센터의 왼쪽 아래 탐색 창에서 **관리 센터** 를 확장 하 고 **Exchange**를 선택 합니다.
6. Exchange 관리 센터에서 **받는 사람 > 사서함**으로 이동 합니다.
7. 사용자를 선택 하 고 사용자 속성 페이지의 **모바일 장치**에서 **Exchange activcsync 사용 안 함을** 클릭 하 고 **장치용 OWA를 사용 하지 않도록 설정** 하 고 두 가지 모두에 대해 **예** 로 대답 합니다.
8. **전자 메일 연결**에서 **예**를 **사용 하지 않도록 설정** 하 고 응답 합니다. 

### <a name="step-6-optional-remove-the-suspected-compromised-account-from-all-administrative-role-groups"></a>6 단계 (선택 사항): 모든 관리 역할 그룹에서 의심 스러운 계정 제거
> [!NOTE]
> 계정을 보호 한 후에는 관리 역할 그룹 구성원을 복원할 수 있습니다.

1. 전역 관리자 계정을 사용 하 여 Office 365 관리 센터에 로그인 하 고 **활성 사용자**를 엽니다.
2. 의심 스러운 계정의 손상 된 계정을 찾고 해당 계정에 할당 된 관리 역할이 있는지 수동으로 확인 합니다.
3. **Security & 준수 센터**를 엽니다.
4. **사용 권한을**클릭 합니다.
5. 역할 그룹을 수동으로 검토 하 여 의심 스러운 계정이 해당 계정의 구성원 인지 확인 합니다.  다음의 경우: 역할 그룹을 클릭 하 고 **역할 그룹 편집**을 클릭 합니다.  b. **선택한 구성원** 및 **편집** 을 클릭 하 여 역할 그룹에서 사용자를 제거 합니다.
6. **Exchange 관리 센터** 열기
7. **사용 권한을**클릭 합니다.
8. 역할 그룹을 수동으로 검토 하 여 의심 스러운 계정이 해당 계정의 구성원 인지 확인 합니다. If: a. 역할 그룹을 클릭 하 고 **편집**을 클릭 합니다.  b. **members** 섹션을 사용 하 여 역할 그룹에서 사용자를 제거 합니다.

### <a name="step-7-optional-additional-precautionary-steps"></a>7 단계 (선택 사항): 추가 준비 단계
1. 보낸 항목을 확인 해야 합니다. 사용자의 계정이 손상 되었음을 대화 상대 목록에 알려야 할 수도 있습니다. 예를 들어 공격자는 다른 국가에서 나 필요한 비용으로 남겨진 것을 요구 하거나 공격자가 바이러스를 보내 컴퓨터를 가로챌 수 있습니다.
2. 이 Exchange 계정을 대체 전자 메일 계정으로 사용한 다른 서비스가 손상 되었을 수 있습니다. 먼저 Office 365 구독에 대해 이러한 단계를 수행한 다음 다른 계정에 대해 이러한 단계를 수행 합니다.
3. 전화 번호, 주소 등의 연락처 정보가 올바른지 확인 합니다.

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>cybersecurity pro와 같은 Office 365 보호
Office 365 구독에는 데이터와 사용자를 보호 하는 데 사용할 수 있는 강력한 보안 기능 집합이 포함 되어 있습니다.  office 365 보안 로드맵: office 365 테 넌 트를 보호 하기 위한 Microsoft 권장 모범 사례를 구현 하는 데 [처음 30 일, 90 일 및 그 이상에 대 한 주요 우선 순위](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) 를 사용 합니다.
- 처음 30 일 이내에 수행 해야 하는 작업입니다.  이러한 설정은 즉시 영향을 미치며 사용자에 게 미치는 영향이 낮습니다.
- 90 일 이내에 수행할 작업입니다. 이러한 작업은 계획 하 고 구현 하는 데 다소 시간이 걸리고 보안 환경을 크게 향상 시킵니다.
- 90 일을 초과 합니다. 처음 90 일의 향상 된 기능 빌드는 다음과 같은 작업을 수행 합니다.

## <a name="see-also"></a>참고 항목:
- [Office 365에 대한 보안 모범 사례](https://support.office.com/article/Security-best-practices-for-Office-365-9295e396-e53d-49b9-ae9b-0b5828cdedc3)
- [Office 365에서 Outlook 규칙 및 사용자 지정 양식 주입 공격 감지 및 재구성](detect-and-remediate-outlook-rules-forms-attack.md)
- [인터넷 범죄 불만 센터](http://www.ic3.gov/preventiontips.aspx)
- [증권 및 Exchange 위원회-"피싱" 사기](http://www.sec.gov/investor/pubs/phishing.htm)
