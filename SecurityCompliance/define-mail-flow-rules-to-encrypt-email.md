---
title: Office 365에서 전자 메일 메시지를 암호화하기 위한 메일의 흐름 규정을 정의
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 9b7daf19-d5f2-415b-bc43-a0f5f4a585e8
ms.collection:
- M365-security-compliance
description: 관리자는 Office 365 메시지 암호화를 사용 하 여 메시지를 암호화 하 고 암호를 해독 하는 메일 흐름 규칙 (전송 규칙)을 만드는 방법을 알 수 있습니다.
ms.openlocfilehash: 75b8e3c977a2708eb1edb8e2b94f555aa54045ca
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854692"
---
# <a name="define-mail-flow-rules-to-encrypt-email-messages-in-office-365"></a>Office 365에서 전자 메일 메시지를 암호화하기 위한 메일의 흐름 규정을 정의

Office 365 전역 관리자는 보내는 전자 메일 메시지를 보호 하는 데 도움이 되는 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들 수 있습니다. 규칙을 설정 하 여 보내는 전자 메일 메시지를 암호화 하 고 조직 내부에서 전송 되는 암호화 된 메시지에서 또는 조직이 보낸 암호화 된 메시지에 대 한 암호화를 제거할 수 있습니다. EAC (Exchange 관리 센터) 또는 Exchange Online PowerShell을 사용 하 여 이러한 규칙을 만들 수 있습니다. 전체 암호화 규칙 외에도 최종 사용자에 대한 개별 메시지 암호화 옵션을 사용할지 여부를 선택할 수도 있습니다.

||
|:-----|
|이 문서는 Office 365 메시지 암호화에 대 한 보다 광범위 한 문서에 포함 되어 있습니다. 이 문서는 관리자와 ITPros 전문가를 위한 것입니다. 암호화 된 메시지를 보내거나 받는 방법에 대 한 정보를 찾으려는 경우에는 [Office 365 메시지 암호화 (OME)](ome.md) 의 문서 목록을 참조 하 여 요구 사항에 가장 적합 한 문서를 검색 하세요. |
||

최근에 AD RMS에서 Azure Information Protection으로 마이그레이션한 경우 기존 메일 흐름 규칙을 검토 하 여 새 환경에서 계속 작동 하는지 확인 해야 합니다. 또한 Azure Information Protection을 통해 새 Office 365 메시지 암호화 (OME) 기능을 활용 하려는 경우 기존 메일 흐름 규칙을 업데이트 해야 합니다. 그렇지 않으면 사용자는 새로운 OME 환경이 아닌 이전 HTML 첨부 파일 형식을 사용 하는 암호화 된 메일을 계속 받게 됩니다. 아직 OME을 설정 하지 않은 경우 정보를 보려면 [새 Office 365 메시지 암호화 기능 설정을](set-up-new-message-encryption-capabilities.md) 참조 하십시오.

메일 흐름 규칙을 만드는 구성 요소와 메일 흐름 규칙의 작동 방식에 대 한 자세한 내용은 [메일 흐름 규칙 (전송 규칙)에서 Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)을 참조 하십시오. 메일 흐름 규칙이 Azure Information Protection과 함께 작동 하는 방식에 대 한 자세한 내용은 [Azure Information protection 레이블에 대 한 Exchange Online 메일 흐름 규칙 구성을](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-exo-rules)참조 하세요.

> [!IMPORTANT]
> 하이브리드 Exchange 환경에서는 온-프레미스 사용자가 Exchange Online을 통해 전자 메일을 라우팅하는 경우에만 OME를 사용 하 여 암호화 된 메일을 보낼 수 있습니다. 하이브리드 Exchange 환경에서 OME을 구성 하려면 먼저 [하이브리드 구성 마법사를 사용 하 여 하이브리드를 구성한](https://docs.microsoft.com/Exchange/exchange-hybrid) 다음 [전자 메일 서버에서 Office 365로 메일이 전송 되도록 구성](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365)해야 합니다. Office 365를 통해 메일이 전송 되도록 구성한 후에는이 지침을 사용 하 여 OME에 대 한 메일 흐름 규칙을 구성할 수 있습니다.

## <a name="create-mail-flow-rules-to-encrypt-email-messages-with-the-new-ome-capabilities"></a>새 OME 기능을 사용 하 여 전자 메일 메시지를 암호화 하는 메일 흐름 규칙 만들기

EAC를 사용 하 여 새 OME 기능으로 메시지 암호화를 트리거하는 메일 흐름 규칙을 정의할 수 있습니다.

### <a name="use-the-eac-to-create-a-rule-for-encrypting-email-messages-with-the-new-ome-capabilities"></a>EAC를 사용 하 여 새 OME 기능을 사용 하 여 전자 메일 메시지를 암호화 하는 규칙 만들기

1. 웹 브라우저에서 전역 관리자 권한이 부여 된 회사 또는 학교 계정을 사용 하 여 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)합니다.

2. **관리** 타일을 선택 합니다.

3. Microsoft 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택 합니다.

4. EAC **** ![에서](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **메일 흐름** \> **규칙** 으로 이동 하 고 새로 만들기 아이콘을 선택 하 여 **새 규칙을 만듭니다**. EAC를 사용 하는 방법에 대 한 자세한 내용은 exchange [Online의 exchange 관리 센터](https://docs.microsoft.com/exchange/exchange-admin-center)를 참조 하세요.

5. **이름**에 DrToniRamos@hotmail.com에 대 한 메일 암호화와 같은 규칙의 이름을 입력 합니다.

6. **다음의 경우 이 규칙 적용**에서 조건을 선택하고 필요한 경우 값을 입력합니다. 예를 들어 DrToniRamos@hotmail.com에 보내는 메시지를 암호화하려면 다음을 수행합니다.

   1. **다음의 경우 이 규칙 적용**에서 **받는 사람이 다음과 같음**을 선택합니다.

   2. 연락처 목록에서 기존 이름을 선택하거나 **이름 확인** 상자에 새 전자 메일 주소를 입력합니다.

      - 기존 이름을 선택하려면 목록에서 이름을 선택한 다음 **확인**을 클릭합니다.

      - 새 이름을 입력 하려면 **이름 확인** 상자에 전자 메일 주소를 입력 하 고 **이름** \> 확인 **을**선택 합니다.

7. 조건을 더 추가 하려면 **기타 옵션** 을 선택한 다음 **조건 추가** 를 선택 하 고 목록에서를 선택 합니다.

   예를 들어 받는 사람이 조직 외부에 있는 경우에만이 규칙을 적용 하려면 **조건 추가** 를 선택한 다음 받는 사람이 **조직** \> **** 외부에 있는 **외부/내부** \> 에 있습니다 .를 선택 합니다.

8. 새 OME 기능을 사용 하 여 암호화를 사용 하도록 설정 하려면 **다음 작업을 수행**하 고 **메시지 보안 수정을** 선택한 다음 **Office 365 메시지 암호화 및 권한 보호 적용**을 선택 합니다. 목록에서 RMS 템플릿을 선택 하 고 **저장**을 선택한 다음 **확인**을 선택 합니다.
  
  서식 파일 목록에는 모든 기본 서식 파일 및 옵션 뿐 아니라 Office 365에서 사용 하기 위해 만든 사용자 지정 서식 파일도 포함 됩니다. 목록이 비어 있으면 [새 office 365 메시지 암호화 기능 설정](set-up-new-message-encryption-capabilities.md)에 설명 된 대로 Office 365 메시지 암호화를 새로운 기능으로 설정 했는지 확인 합니다. 기본 서식 파일에 대 한 자세한 내용은 [Azure Information Protection의 템플릿 구성 및 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오. **전달 하지** 않음 옵션에 대 한 자세한 내용은 [전자 메일에 대 한 전달 옵션 안 함](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)을 참조 하십시오. **암호화 전용** 옵션에 대 한 자세한 내용은 [전자 메일에 대 한 암호화 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 참조 하십시오.

  다른 작업을 지정 하려는 경우 **작업 추가** 를 선택할 수 있습니다.

### <a name="use-the-eac-to-update-an-existing-mail-flow-rule-to-use-the-new-ome-capabilities"></a>EAC를 사용 하 여 새 OME 기능을 사용 하도록 기존 메일 흐름 규칙 업데이트

1. 웹 브라우저에서 전역 관리자 권한이 부여 된 회사 또는 학교 계정을 사용 하 여 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)합니다.

2. **관리** 타일을 선택 합니다.

3. Microsoft 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택 합니다.

4. EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.

5. 메일 흐름 규칙 목록에서 새 OME 기능을 사용 하도록 수정할 규칙을 선택 하 고 편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) **편집** ![을 선택 합니다.

6. 새 OME 기능을 사용 하 여 암호화를 사용 하도록 설정 하려면 **다음 작업을 수행**하 고 **메시지 보안 수정을** 선택한 다음 **Office 365 메시지 암호화 및 권한 보호 적용**을 선택 합니다. 목록에서 RMS 템플릿을 선택 하 고 **저장** 을 선택한 다음 **확인**을 선택 합니다.

   서식 파일 목록에는 모든 기본 서식 파일 및 옵션 뿐 아니라 Office 365에서 사용 하기 위해 만든 사용자 지정 서식 파일도 포함 됩니다. 목록이 비어 있으면 Office 365 메시지 암호화가 [Azure Information Protection의 새로운 office 365 메시지 암호화 기능 설정](set-up-new-message-encryption-capabilities.md)에 설명 된 대로 새로운 기능을 사용 하 여 설정 했는지 확인 합니다. 기본 서식 파일에 대 한 자세한 내용은 [Azure Information Protection의 템플릿 구성 및 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오. **전달 하지** 않음 옵션에 대 한 자세한 내용은 [전자 메일에 대 한 전달 옵션 안 함](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)을 참조 하십시오. **암호화 전용** 옵션에 대 한 자세한 내용은 [전자 메일에 대 한 암호화 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 참조 하십시오.

   다른 작업을 지정 하려는 경우 **작업 추가** 를 선택할 수 있습니다.

7. 다음 작업 **수행** 목록에서 **메시지 보안** \> 을 수정 하도록 할당 된 모든 작업을 제거 하 **여 이전 버전의 OME을 적용**합니다.

8. **저장**을 선택합니다.

## <a name="create-mail-flow-rules-for-office-365-message-encryption-without-the-new-capabilities"></a>새 기능 없이 Office 365 메시지 암호화에 대 한 메일 흐름 규칙 만들기

아직 Office 365 조 직을 새 OME 기능으로 이동 하지 않은 경우 다음 작업을 사용 하 여 조직에 대 한 메시지를 암호화 하는 메일 흐름 규칙을 정의 합니다. 조직에 적합 한 시기에 새 OME 기능으로 바로 이동 하는 계획을 수립 하는 것이 좋습니다. 자세한 내용은 [Azure Information Protection 기반으로 구축 된 새 Office 365 메시지 암호화 기능 설치](set-up-new-message-encryption-capabilities.md)를 참조 하세요.

### <a name="use-the-eac-to-create-a-mail-flow-rule-for-encrypting-email-messages-without-the-new-ome-capabilities"></a>EAC를 사용 하 여 새 OME 기능 없이 전자 메일 메시지를 암호화 하기 위한 메일 흐름 규칙 만들기

1. 웹 브라우저에서 전역 관리자 권한이 부여 된 회사 또는 학교 계정을 사용 하 여 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)합니다.

2. **관리** 타일을 선택 합니다.

3. Microsoft 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택 합니다.

4. EAC **** ![에서](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **메일 흐름** \> **규칙** 으로 이동 하 고 새로 만들기 아이콘을 선택 하 여 **새 규칙을 만듭니다**. EAC를 사용 하는 방법에 대 한 자세한 내용은 exchange [Online의 exchange 관리 센터](https://docs.microsoft.com/exchange/exchange-admin-center)를 참조 하세요.

5. **이름**에 DrToniRamos@hotmail.com에 대 한 메일 암호화와 같은 규칙의 이름을 입력 합니다.

6. **다음의 경우 이 규칙 적용**에서 조건을 선택하고 필요한 경우 값을 입력합니다. 예를 들어 DrToniRamos@hotmail.com에 보내는 메시지를 암호화하려면 다음을 수행합니다.

   1. **다음의 경우 이 규칙 적용**에서 **받는 사람이 다음과 같음**을 선택합니다.

   2. 연락처 목록에서 기존 이름을 선택하거나 **이름 확인** 상자에 새 전자 메일 주소를 입력합니다.

      - 기존 이름을 선택하려면 목록에서 이름을 선택한 다음 **확인**을 클릭합니다.

      - 새 이름을 입력 하려면 **이름 확인** 상자에 전자 메일 주소를 입력 하 고 **이름** \> 확인 **을**선택 합니다.

7. 조건을 더 추가 하려면 **기타 옵션** 을 선택한 다음 **조건 추가** 를 선택 하 고 목록에서를 선택 합니다.

   예를 들어 받는 사람이 조직 외부에 있는 경우에만이 규칙을 적용 하려면 **조건 추가** 를 선택한 다음 받는 사람이 **조직** \> **** 외부에 있는 **외부/내부** \> 에 있습니다 .를 선택 합니다.

8. 새 OME 기능을 사용 하지 않고 암호화를 사용 하도록 설정 하려면 **다음 작업**에서 **메시지 보안** \> 수정을 선택 하 여 **이전 버전의 OME를 적용**한 다음 **저장**을 선택 합니다.

  IRM 라이선싱을 사용할 수 없다는 오류가 표시 되는 경우에는 조직에 대 한 OME를 아직 설정 하지 않은 것입니다. 지금 OME을 설정 하려면 새 OME 기능을 사용 하도록 설정 해야 합니다. 자세한 내용은 [Azure Information Protection 기반으로 구축 된 새 Office 365 메시지 암호화 기능](set-up-new-message-encryption-capabilities.md)을 참조 하세요. Microsoft에서는 새 기능 없이는 OME의 새 배포를 설정 하는 것이 더 이상 지원 되지 않습니다.

  다른 작업을 지정 하려는 경우 **작업 추가** 를 선택할 수 있습니다.

### <a name="use-exchange-online-powershell-to-create-a-mail-flow-rule-for-encrypting-email-messages-without-the-new-ome-capabilities"></a>Exchange Online PowerShell을 사용 하 여 새 OME 기능 없이 전자 메일 메시지를 암호화 하기 위한 메일 흐름 규칙 만들기

1. Exchange Online PowerShell에 연결합니다. 자세한 내용은 [원격 PowerShell을 사용하여 Exchange Online에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)을 참조하세요.

2. **New-transportrule** cmdlet을 사용 하 여 규칙을 만들고 _ApplyOME_ 매개 변수를로 `$true`설정 합니다.

   이 예에서는 DrToniRamos@hotmail.com으로 전송 되는 모든 전자 메일 메시지를 암호화 해야 합니다.

   ```powershell
   New-TransportRule -Name "Encrypt rule for Dr Toni Ramos" -SentTo "DrToniRamos@hotmail.com" -SentToScope "NotinOrganization" -ApplyOME $true
   ```

   **참고:**

   - 새 규칙의 고유한 이름은 "Dr Toni에 대 한 암호화 규칙"입니다.

   - _SentTo_ 매개 변수는 메시지 받는 사람 (이름, 전자 메일 주소, 고유 이름 등으로 식별 됨)을 지정 합니다. 이 예에서는 받는 사람이 전자 메일 주소 "DrToniRamos@hotmail.com"로 식별 됩니다.

   - _SentToScope_ 매개 변수는 메시지 받는 사람의 위치를 지정 합니다. 이 예에서는 받는 사람의 사서함이 hotmail에 있고 Office 365 조직의 일부가 아니므로 값 `NotInOrganization` 이 사용 됩니다.

   구문과 매개 변수에 대한 자세한 내용은 [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule)를 참조하십시오.

### <a name="remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a>새 OME 기능을 사용 하지 않고 암호화 된 전자 메일 회신에서 암호화 제거

전자 메일 사용자가 암호화된 메시지를 보내면 해당 메시지의 받는 사람은 암호화된 회신을 통해 응답을 할 수 있습니다. 메일 흐름 규칙을 만들면 조직의 전자 메일 사용자가 암호화 포털에 로그인 하 여 메시지를 볼 필요가 없도록 자동으로 회신에서 암호화를 제거할 수 있습니다. EAC 또는 Windows PowerShell cmdlet을 사용 하 여 이러한 규칙을 정의할 수 있습니다. 아직 새 OME 기능을 사용 하지 않는 경우 조직 내에서 전송 되거나 조직 내에서 전송 된 메시지에 회신 하는 메시지의 암호를 해독 하는 것만 가능 합니다. 조직 외부에서 보낸 암호화 된 메시지의 암호를 해독할 수 없습니다.

#### <a name="use-the-eac-to-create-a-rule-for-removing-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a>EAC를 사용 하 여 새 OME 기능 없이 암호화 된 전자 메일 응답에서 암호화를 제거 하는 규칙 만들기

1. 웹 브라우저에서 관리자 권한이 부여 된 회사 또는 학교 계정을 사용 하 여 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)합니다.

2. **관리** 타일을 선택 합니다.

3. Microsoft 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택 합니다.

4. EAC **** ![에서](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **메일 흐름** \> **규칙** 으로 이동 하 고 새로 만들기 아이콘을 선택 하 여 **새 규칙을 만듭니다**. EAC를 사용 하는 방법에 대 한 자세한 내용은 exchange [Online의 exchange 관리 센터](https://docs.microsoft.com/exchange/exchange-admin-center)를 참조 하세요.

5. **이름**에 규칙의 이름을 입력 합니다 (예: 받는 메일에서 암호화 제거).

6. **다음의 경우이 규칙 적용** 에서 **받는 사람이** \> **조직 내부**에 있는 것과 같이 메시지에서 암호화를 제거 해야 하는 조건을 선택 합니다.

7. **다음 작업 실행**에서 **메시지 보안** \> 수정을 선택 하 여 **이전 버전의 OME을 제거**합니다.

8. **저장**을 선택합니다.

#### <a name="use-exchange-online-powershell-to-create-a-rule-to-remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a>Exchange Online PowerShell을 사용 하 여 새 OME 기능 없이 암호화 된 전자 메일 응답에서 암호화를 제거 하는 규칙 만들기

1. Exchange Online PowerShell에 연결합니다. 자세한 내용은 [원격 PowerShell을 사용하여 Exchange Online에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)을 참조하세요.

2. **New-transportrule** cmdlet을 사용 하 여 규칙을 만들고 _RemoveOME_ 매개 변수를로 `$true`설정 합니다.

   이 예에서는 Office 365 조직의 받는 사람에 게 전송 되는 모든 메일에서 암호화를 제거 합니다.

   ```powershell
   New-TransportRule -Name "Remove encryption from incoming mail" -SentToScope "InOrganization" -RemoveOME $true
   ```

   **참고:**

   - 새 규칙의 고유한 이름은 "받는 메일에서 암호화 제거"입니다.

   - _SentToScope_ 매개 변수는 메시지 받는 사람의 위치를 지정 합니다. 이 예제에서는 다음을 나타내는 `InOrganization` 값 값을 사용 합니다.

     - 받는 사람이 조직의 사서함, 메일 사용자, 그룹 또는 메일 사용이 가능한 공용 폴더인 경우

       또는

     - 받는 사람의 전자 메일 주소가 신뢰할 수 있는 도메인 이나 조직의 내부 릴레이 도메인으로 구성 된 허용 도메인에 _있으며_ , 인증 된 연결을 통해 메시지를 보내거나 받은 경우

구문과 매개 변수에 대한 자세한 내용은 [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule)를 참조하십시오.

## <a name="related-topics"></a>관련 주제

[Office 365의 암호화](encryption.md)

[새로운 Office 365 메시지 암호화 기능 설정](set-up-new-message-encryption-capabilities.md)

[암호화된 메시지에 브랜딩 추가](add-your-organization-brand-to-encrypted-messages.md)

[Exchange Online의 메일 흐름 규칙 (전송 규칙)](https://go.microsoft.com/fwlink/p/?LinkId=506707)

[Exchange Online Protection의 메일 흐름 규칙(전송 규칙)](https://go.microsoft.com/fwlink/p/?LinkId=506708)
