---
title: Office 365에서 손상된 이메일 계정에 응답
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- M365-security-compliance
ms.custom: TopSMBIssues
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
description: Office 365에서 손상된 전자 메일 계정을 인식하고 응답하는 방법에 대해 알아봅니다.
ms.openlocfilehash: abb9cbae0d1df41f5513e7958aaf1dc04ce66154
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264840"
---
# <a name="responding-to-a-compromised-email-account-in-office-365"></a>Office 365에서 손상된 이메일 계정에 응답

**요약** Office 365에서 손상된 전자 메일 계정을 인식하고 응답하는 방법에 대해 알아봅니다.

## <a name="what-is-a-compromised-email-account-in-office-365"></a>Office 365에서 손상된 이메일 계정이란?
Office 365 사서함, 데이터 및 기타 서비스에 대한 액세스는 자격 증명 (예 : 사용자 이름 및 암호 또는 PIN)을 사용하여 제어됩니다. 의도된 사용자가 아닌 사용자가 해당 자격 증명을 도용하면 도난된 자격 증명이 손상된 것으로 간주됩니다. 도난된 자격 증명으로 공격자는 원래 사용자로 로그인하여 불법적인 행동을 수행할 수 있습니다.
도난된 자격 증명을 사용하여 공격자는 사용자의 Office 365 사서함, SharePoint 폴더 또는 사용자의 OneDrive에있는 파일에 액세스할 수 있습니다. 흔히 볼 수 있는 한 가지 조치는 침입자가 전자 메일을 원래 사용자로 보내 조직 내부와 외부의 받는 사람에게 보내는 것입니다. 공격자가 외부 수신자에게 데이터를 메일로 보낼 때 이것을 데이터 유출이라고 합니다.

## <a name="symptoms-of-a-compromised-office-365-email-account"></a>손상된 Office 365 전자 메일 계정의 증상
사용자는 Office 365 사서함에서 비정상적인 활동을 알아차리고 보고할 수 있습니다. 몇 가지 일반적인 증상은 다음과 같습니다.
- 이메일 누락 또는 삭제와 같은 의심스러운 활동
- 다른 사용자는 보낸 사람의 **보낸 편지함** 폴더에 해당 메일이 없어도 손상된 계정의 메일을 받을 수 있습니다.
- 의도된 사용자 또는 관리자가 생성하지 않은 받은 편지함 규칙이 있는지 여부 이러한 규칙은 메일을 알 수 없는 주소로 자동 전달하거나 **노트**, **정크 메일** 또는 **RSS 구독** 폴더로 이동시킬 수 있습니다.
- 전체 주소 목록에서 사용자의 표시 이름을 변경할 수 있습니다.
- 사용자의 사서함에서 메일 보내기가 차단됩니다.
- Microsoft Outlook 또는 웹용 Outlook (이전까지의 Outlook Web App)에있는 보낸 편지함 또는 지운 편지함 폴더에는 "런던에 묶여 있습니다. 돈을 보내주세요."와 같은 일반적인 해킹된 계정 메시지가 들어있습니다.
- 이름, 전화 번호 또는 우편 번호와 같은 비정상적인 프로필 변경 사항이 업데이트됩니다.
- 여러 암호 변경과 같은 비정상적인 자격 증명 변경이 요구됩니다.
- 최근에 메일 전달이 추가되었습니다.
- 가짜 은행 업무 서명이나 처방약 서명과 같은 비정상적인 서명이 최근 추가되었습니다.

사용자가 위의 증상 중 하나를 보고하면 추가 조사를 수행해야 합니다. Microsoft 365 보안 및 규정 준수 센터 및 Azure 포털은 손상되었을 가능성이 있는 것으로 의심되는 사용자 계정의 활동을 조사하는 데 유용한 도구를 제공합니다.
- 보안 및 규정 준수 센터의 Office 365 통합 감사 로그 - 의심스러운 활동이 발생한 직전부터 현재 날짜까지의 기간에 대한 결과를 필터링하여 의심되는 계정에 대한 모든 활동을 검토합니다. 검색 중에 활동을 필터링하지 마세요.
- Azure AD 포털에서 사용할 수있는 Azure AD 로그인 로그 및 기타 위험 보고서를 사용합니다. 다음 열에 있는 값을 확인합니다.
    - IP 주소 검토
    - 로그인 위치
    - 로그인 시간
    - 로그인 성공 또는 실패

## <a name="how-to-secure-and-restore-email-function-to-a-suspected-compromised-office-365-account-and-mailbox"></a>손상된 Office 365 계정 및 사서함으로 의심되는 메일 기능을 보안하고 복원하는 방법

> [!VIDEO https://videoplayercdn.osi.office.net/hub/?csid=ux-cms-en-us-msoffice&uuid=RE2jvOb&AutoPlayVideo=false]

계정에 대한 액세스 권한을 회복한 후에도 공격자는 백도어 항목을 추가하여 계정을 다시 제어하기 시작할 수 있습니다.

계정에 대한 액세스 권한을 다시 얻으려면 다음 단계를 모두 수행해야 합니다. 계정 도용자가 계정 제어를 재개하지 않는지 확인하는 것은 빠를수록 좋습니다. 이 단계는 계정 도용자가 귀하의 계정에 추가한 백도어 항목을 제거하는 데 도움이 됩니다. 이러한 단계를 수행한 후에는 컴퓨터가 손상되지 않았는지 확인하기 위해 바이러스 검사를 실행하는 것이 좋습니다.

### <a name="step-1-reset-the-users-password"></a>1단계 사용자의 암호 재설정하기
> [!WARNING]
> 이 시점에서 공격자가 여전히 사서함에 액세스할 수 있으므로 메일을 통해 의도한 사용자에게 새 암호를 보내지 않습니다.

1. 다른 사용자에 대 한 비즈니스 암호 다시 설정 Office 365에 따라 다른 절차에 [관리자: Office 365 재설정 business 암호](https://support.office.com/article/admins-reset-office-365-business-passwords-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c)

**참고:**
- 암호가 강하고 대문자, 소문자, 숫자 하나 이상 및 특수 문자가 하나 이상 포함되어 있는지 확인합니다. 
- 지난 마지막 5개의 암호를 다시 사용하지 않습니다. 암호 기록 요구 사항을 통해 최근 암호를 다시 사용할 수는 있지만 공격자가 추측할 수 없는 암호를 선택해야 합니다.
- 온 - 프레미스 ID가 Office 365와 페더레이션된 경우 온 - 프레미스 암호를 변경해야 하며 관리자에게 손상 사실을 알려야 합니다.

> [!TIP]
> 특히 관리자 권한이있는 계정의 경우에는 손상 방지를 위해 MFA(다중 요소 인증)를 사용하는 것이 좋습니다.  자세한 내용은 [여기](https://support.office.com/ko-KR/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6)에서 알아보세요.

### <a name="step-2-remove-suspicious-email-forwarding-addresses"></a>2단계 의심스러운 메일 전달 주소 제거하기
1. **Microsoft 365 관리 센터 > 활성 사용자**를 엽니다.
2. 문제가되는 사용자 계정을 찾아 **메일 설정**을 확장합니다.
3. **메일 전달**의 경우 **편집**을 클릭합니다.
4. 의심스러운 전달 주소를 모두 제거 합니다.

### <a name="step-3-disable-any-suspicious-inbox-rules"></a>3단계는 의심스러운 받은 편지함 규칙을 사용하지 않도록 설정하기
1. 웹용 Outlook을 사용하여 사용자의 사서함에 로그인합니다..
2. 기어 아이콘을 클릭하고 **메일**을 클릭합니다.
3. **받은 편지함 및 비우기 규칙**을 클릭하고 규칙을 검토합니다.
4. 의심러운 규칙을 사용하지 않도록 설정하거나 삭제합니다.

### <a name="step-4-unblock-the-user-from-sending-mail"></a>4단계 사용자 메일 보내기 차단을 해제하기
손상된 것으로 의심되는 사서함이 스팸 메일을 보내기 위해 불법적으로 사용된 경우 사서함이 메일을 보내지 못하도록 차단되었을 수 있습니다.
1. 사서함의 메일 보내기 차단을 해제하려면 스팸 메일을 보낸 후 차단 목록에서 [사용자, 도메인 또는 IP 주소 제거](https://docs.microsoft.com/Office365/SecurityCompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email )의 절차를 따릅니다.

### <a name="step-5-optional-block-the-user-account-from-signing-in"></a>5단계 선택 사항 : 사용자 계정 로그인을 차단하기
> [!IMPORTANT]
> 액세스가 다시 활성화되어도 안전하다고 판단될 때까지 손상된 것으로 의심되는 계정이 로그인하지 못하도록 차단할 수 있습니다.

1. Microsoft 365 관리 센터로 이동합니다.
2. Microsoft 365 관리 센터에서 **사용자**를 선택합니다.
3. 차단할 직원을 선택한 다음 사용자 창의 **로그인 상태** 옆에 있는 **편집** 을 선택합니다.
4. **로그인 상태** 창에서 **로그인 차단됨**을 선택한 다음 **저장**을 선택합니다. 
5. 관리 센터의 왼쪽 아래 탐색 창에서 **관리 센터**를 확장하고 **Exchange**를 선택합니다.
6. Exchange 관리 센터에서 **받는 사람 > 사서함**으로 이동합니다.
7. 사용자를 선택하고 사용자 속성 페이지의 **모바일 장치**에서 **Exchange ActiveSync 사용 안 함** 및 **장치용 OWA 사용 안 함**을 클릭하고 두 가지 모두에 대해 **예**라고 답변합니다.
8. **전자 메일 연결**에서 **사용 안 함**을 클릭하고 **예**라고 답변합니다. 

### <a name="step-6-optional-remove-the-suspected-compromised-account-from-all-administrative-role-groups"></a>6단계 선택 사항: 모든 관리 역할 그룹에서 손상된 것으로 의심되는 계정 제거하기
> [!NOTE]
> 관리 역할 그룹 구성원은 계정이 보안된 후에 복원할 수 있습니다.

1. 글로벌 관리자 계정을 사용하여 Microsoft 365 관리 센터에 로그인하고 **활성 사용자**를 엽니다.
2. 손상된 것으로 의심되는 계정을 찾고 계정에 할당된 관리 역할이 있는지 확인합니다.
3. **보안 및 규정 준수 센터**를 엽니다.
4. **권한**을 클릭합니다.
5. 역할 그룹을 수동으로 검토하여 손상된 것으로 의심되는 계정이 해당 그룹의 구성원인지 확인하십시오.  다음과 같은 경우 : a. 역할 그룹을 클릭하고 **역할 그룹 편집**을 클릭합니다.
    b. **구성원 선택** 및 **편집**을 클릭하여 역할 그룹에서 사용자를 제거합니다.
6. **Exchange 관리 센터**를 엽니다.
7. **권한**을 클릭합니다.
8. 역할 그룹을 수동으로 검토하여 손상된 것으로 의심되는 계정이 해당 그룹의 구성원인지 확인하십시오. 다음과 같은 경우 : a. 역할 그룹을 클릭하고 **편집**을 클릭합니다.
    b. **구성원** 및 섹션을 클릭하여 역할 그룹에서 사용자를 제거합니다.

### <a name="step-7-optional-additional-precautionary-steps"></a>7단계 선택 사항 : 추가 예비 단계
1. 보낸된 항목을 확인합니다. 연락처 목록에 있는 사람들에게 계정이 손상되었다는 사실을 알려야할 수도 있습니다. 공격자가 돈을 요구했을 수 있습니다. 예를 들어, 다른 국가에 묶여 돈이 필요하거나, 공격자가 컴퓨터를 도용하기 위해 바이러스를 보낼 수 있습니다.
2. 이 Exchange 계정을 대체 메일 계정으로 사용한 다른 서비스가 손상되었을 수 있습니다. 먼저 Office 365 구독에 대해 이러한 단계를 수행한 다음 다른 계정에 대해이 단계를 수행합니다.
3. 전화번호 및 주소와 같은 연락처 정보가 정확한지 확인합니다.

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>사이버 보안 전문가와 같은 Office 365 보안
Office 365 구독에는 데이터 및 사용자를 보호하는 데 사용할 수있는 강력한 보안 기능이 함께 제공됩니다.  [Office 365 보안 로드맵: 최초 30일, 90일 및 그 이후의 최우선 순위](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352)를 사용하여 Microsoft에서 권장하는 Office 365 테넌트 보안을 구현합니다.
- 처음 30일 이내에 수행 할 작업  이러한 작업들은 즉각적인 영향을 미치며 사용자에게 영향을 미치지 않습니다.
- 90일 이내에 수행해야 할 작업 이러한 작업들은 계획하고 구현하는 데 다소 시간이 걸리지만 보안 태세를 갖추는 데 큰 도움이 됩니다.
- 90일 초과 이러한 향상된 기능은 처음 90일간의 작업에서 구축됩니다.

## <a name="see-also"></a>참고 항목:
- [Office 365에 대한 보안 모범 사례](https://support.office.com/article/Security-best-practices-for-Office-365-9295e396-e53d-49b9-ae9b-0b5828cdedc3)
- [Office 365에서 Outlook 규칙 및 사용자 지정 양식 주입 공격 감지 및 재구성](detect-and-remediate-outlook-rules-forms-attack.md)
- [인터넷 범죄 불만 센터](http://www.ic3.gov/preventiontips.aspx)
- [증권 거래 위원회 - “피싱” 사기](http://www.sec.gov/investor/pubs/phishing.htm)
- Microsoft와 관리자에게 스팸 전자 메일을 직접 보고하려면 [보고서 메시지 추가 기능을 사용하세요](https://support.office.com/ko-KR/article/Use-the-Report-Message-add-in-b5caa9f1-cdf3-4443-af8c-ff724ea719d2).
