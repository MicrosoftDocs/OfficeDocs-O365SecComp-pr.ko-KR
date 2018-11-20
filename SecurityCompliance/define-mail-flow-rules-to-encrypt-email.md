---
title: Office 365에서 전자 메일 메시지를 암호화 하는 메일 흐름 규칙 정의
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 9b7daf19-d5f2-415b-bc43-a0f5f4a585e8
description: Office 365 전역 관리자의 경우 메일 흐름 Office 365 메시지 암호화 OME ()를 사용 하도록 설정 하는 규칙을 만들 수 있습니다. 모든 보내는 전자 메일 메시지를 암호화할 수 있으며 조직에서 보낸 암호화 된 메시지에 대 한 회신 또는 내부 메시지에서 암호화 제거 수 있습니다.
ms.openlocfilehash: 0ed112e216060cdd56afa2dfd08cdebd5740621d
ms.sourcegitcommit: d7e87ce4b1579ac47af2e853ef59ef058c40191f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/16/2018
ms.locfileid: "26547270"
---
# <a name="define-mail-flow-rules-to-encrypt-email-messages-in-office-365"></a>Office 365에서 전자 메일 메시지를 암호화 하는 메일 흐름 규칙 정의

메일 흐름 규칙로 알려져 전송 규칙을 보내고 받는 전자 메일 메시지를 안전 하 게 보호 하는 Office 365 전역 관리자 권한으로 만들 수 있습니다. 모든 보내는 전자 메일 메시지를 암호화 하 고 조직 내부에서 연결 되는 암호화 된 메시지 또는 조직에서 보낸 암호화 된 메시지에 대 한 회신에서 암호화를 제거 하는 규칙을 설정할 수 있습니다. 이러한 규칙을 만들 수는 Exchange 관리 센터 (EAC) 또는 Exchange Online 용 Windows PowerShell cmdlet을 사용할 수 있습니다.  전체 암호화 규칙 외에도 최종 사용자를 위한 개별 메시지 암호화 옵션을 사용할지 여부를 선택할 수 있습니다.
  
최근에 AD RMS에서 Azure 정보 보호를 마이그레이션한 경우 새 환경에서 작업을 계속 하 여 기존 메일 흐름 규칙을 검토 하려면 필요 합니다. 또한 활용 하기 위해 사용할 수 있는 새로운 Office 365 메시지 암호화 (OME) 기능을 Azure 정보 보호 기능을 통해 하려는 경우 기존 메일 흐름 규칙을 업데이트 해야 합니다. 그렇지 않은 경우 사용자에 게 새, 원활 하 게 OME 경험 하는 대신 이전 HTML 첨부 파일 형식을 사용 하는 암호화 된 메일을 받도록 계속 됩니다. 아직 OME를 설정 하지 않은 경우, 정보에 대 한 [Azure 정보 보호 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md) 을 참조 합니다. 
  
메일 흐름 규칙 및 메일 흐름 규칙 작업은 어떻게 구성 하는 구성 요소에 대 한 정보를 [Exchange Online에서 흐름 규칙 (전송 규칙) 메일](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)을 참조 하십시오. 메일 흐름 규칙 Azure 정보 보호와 함께 작동 하는 방법에 대 한 자세한 내용은 [Azure 정보 보호 레이블에 대 한 Exchange Online 구성 메일 흐름 규칙](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-exo-rules)을 참조 하십시오.
  
> [!IMPORTANT]
> 하이브리드 Exchange 환경에 대 한 온-프레미스 사용자 전자 메일을 Exchange Online을 통해 라우팅되는 경우에 OME를 사용 하 여 암호화 된 메일을 보낼 수 있습니다. 하이브리드 Exchange 환경에서 OME를 구성 하려면 첫번째 [하이브리드 구성 마법사를 사용 하 여 하이브리드 구성](https://docs.microsoft.com/Exchange/exchange-hybrid) 및 [메일 Office 365로 전자 메일 서버에서 흐름을 구성](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365)해야 합니다. 한번 구성한 메일이 Office 365를 통해 전달이 지침을 사용 하 여 OME에 대 한 메일 흐름 규칙을 구성 합니다.

## <a name="create-a-mail-flow-rule-to-encrypt-email-messages-with-the-new-ome-capabilities"></a>새 OME 기능으로 전자 메일 메시지를 암호화 하는 메일 흐름 규칙 만들기

EAC를 사용 하 여 새 OME 기능을 사용 하 여 메시지 암호화를 트리거하는 것에 대 한 메일 흐름 규칙을 정의할 수 있습니다.
  
### <a name="to-create-a-rule-for-encrypting-email-messages-with-the-new-ome-capabilities-by-using-the-eac"></a>EAC를 사용 하 여 새 OME 기능으로 전자 메일 메시지를 암호화 하는 것에 대 한 규칙을 만들려면

1. 웹 브라우저에서 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)전역 관리자 권한을 부여 하는 작업이 나 교육용 계정을 사용 하 여 합니다.
    
2. **Admin** 타일을 선택 합니다. 
    
3. Office 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택합니다.
    
4. EAC에서 **메일 흐름** 으로 이동 \> **규칙** \> ![새 아이콘](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) ( **새로 만들기**) \> **새 규칙 만들기**. EAC를 사용 하는 방법에 대 한 자세한 내용은 [Exchange Online의 Exchange 관리 센터](https://docs.microsoft.com/exchange/exchange-admin-center)를 참조 하십시오.
    
5. **이름**Encrypt mail for DrToniRamos@hotmail.com와 같은 규칙에 대 한 이름을 입력 합니다.
    
6. **다음의 경우 이 규칙 적용**에서 조건을 선택하고 필요한 경우 값을 입력합니다. 예를 들어 DrToniRamos@hotmail.com에 보내는 메시지를 암호화하려면 다음을 수행합니다.

  1. **다음의 경우 이 규칙 적용**에서 **받는 사람이 다음과 같음**을 선택합니다.

  2. 연락처 목록에서 기존 이름을 선택하거나 **이름 확인** 상자에 새 전자 메일 주소를 입력합니다. 
    
    기존 이름을 선택하려면 목록에서 이름을 선택한 다음 **확인**을 클릭합니다.
    
    새 이름을 입력 하 고 **이름 확인** 상자에 전자 메일 주소를 입력 한 다음 **이름 확인** 을 선택 하려면 \> **확인**합니다.
    
7. 조건을 더 추가할 **기타 옵션** 을 선택 하 고 **조건 추가** 선택 하 고 목록에서 선택 합니다. 
    
  예, 받는 사람이 조직 외부에 있을 경우에이 규칙을 적용 하려면 **조건 추가** 선택한 다음 선택 **받는 사람이 외부/내부** \> **조직 외부의** \> **확인**합니다.
    
8. **다음을 수행**하십시오에서 새 OME 기능을 사용 하 여 암호화를 사용 하도록 설정 하려면 **메시지 보안 수정** 을 선택 하 고 **Office 365 메시지 암호화 적용 및 권한 보호를**선택 합니다. 목록에서 RMS 템플릿을 선택, **저장**을 선택 하 고 **확인**을 선택 합니다.
    
  모든 기본 서식 파일을 포함 하는 서식 파일 목록이 및 Office 365에서으로 옵션에 대해 만든 모든 사용자 지정 서식 파일을 사용 합니다. 목록이 비어 있으면 설정 되었는지 확인 하면가 Office 365 메시지 암호화 새 기능을 함께 [Azure 정보 보호의 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md)의 설명에 따라 합니다. 기본 서식 파일에 대 한 정보를 [구성 하 고 Azure 정보 보호에 대 한 서식 파일 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오. **전달 하지 않음** 옵션에 대 한 정보를 [전자 메일 전달 하지 않음 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)을 참조 하십시오. **만 암호화** 옵션에 대 한 정보를 [전자 메일만 암호화 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 참조 하십시오.
    
    다른 작업을 지정 하려면 **작업 추가** 선택할 수 있습니다. 
    
### <a name="to-update-an-existing-mail-flow-rule-to-use-the-new-ome-capabilities-by-using-the-eac"></a>EAC를 사용 하 여 새 OME 기능을 사용 하 여 기존 메일 흐름 규칙을 업데이트 하려면

1. 웹 브라우저에서 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)전역 관리자 권한을 부여 하는 작업이 나 교육용 계정을 사용 하 여 합니다.
    
2. **Admin** 타일을 선택 합니다. 
    
3. Office 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택합니다.
    
4. EAC에서 **메일 흐름** 으로 이동 \> **규칙**입니다.
    
5. 메일 흐름 규칙 목록에서 새 OME 기능을 사용 하 고 다음을 선택 하려면 수정할 규칙을 선택 ![편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) ( **편집**).
    
6. **다음을 수행**하십시오에서 새 OME 기능을 사용 하 여 암호화를 사용 하도록 설정 하려면 **메시지 보안 수정** 을 선택 하 고 **Office 365 메시지 암호화 적용 및 권한 보호를**선택 합니다. 목록에서 RMS 템플릿을 선택 하 고 **저장** 을 선택 하 고 **확인**을 선택 합니다.
    
    모든 기본 서식 파일을 포함 하는 서식 파일 목록이 및 Office 365에서으로 옵션에 대해 만든 모든 사용자 지정 서식 파일을 사용 합니다. 목록이 비어 있으면 설정 되었는지 확인 하면가 Office 365 메시지 암호화 새 기능을 함께 [Azure 정보 보호의 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md)의 설명에 따라 합니다. 기본 서식 파일에 대 한 정보를 [구성 하 고 Azure 정보 보호에 대 한 서식 파일 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오. **전달 하지 않음** 옵션에 대 한 정보를 [전자 메일 전달 하지 않음 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)을 참조 하십시오. **만 암호화** 옵션에 대 한 정보를 [전자 메일만 암호화 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 참조 하십시오.
    
    다른 작업을 지정 하려면 **작업 추가** 선택할 수 있습니다. 
    
7. **다음을 수행** 목록에서 **메시지 보안 수정** 에 할당 된 모든 작업을 제거 \> **OME의 이전 버전을 적용**합니다.
    
8. **Save(저장)** 를 선택합니다.
    
## <a name="creating-rules-for-office-365-message-encryption-without-the-new-capabilities"></a>새로운 기능 없이 Office 365 메시지 암호화에 대 한 규칙 만들기

Office 365 조직 새 OME 기능을 이동한 아직 하지 않은 경우 이러한 작업을 사용 하 여 조직에 대 한 메시지를 암호화 하는 메일 흐름 규칙을 정의할 수 있습니다. 것이 조직에 대 한 적당 하 게 하는 즉시 새 OME 기능으로 이동 하는 계획을 확인 하는 것이 좋습니다. 자세한 내용은 [Azure 정보 보호 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md)합니다.
  
### <a name="to-create-a-rule-for-encrypting-email-messages-without-the-new-ome-capabilities-by-using-the-eac"></a>EAC를 사용 하 여 새 OME 기능 없이 전자 메일 메시지를 암호화 하는 것에 대 한 규칙을 만들려면

1. 웹 브라우저에서 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)전역 관리자 권한을 부여 하는 작업이 나 교육용 계정을 사용 하 여 합니다.
    
2. **Admin** 타일을 선택 합니다. 
    
3. Office 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택합니다.
    
4. EAC에서 **메일 흐름** 으로 이동 \> **규칙** \> **+** ( **새로 만들기**) \> **새 규칙 만들기**. EAC를 사용 하는 방법에 대 한 자세한 내용은 [Exchange 관리 센터의 Exchange Online을](https://docs.microsoft.com/exchange/exchange-admin-center)참조 하십시오.
    
5. **이름**Encrypt mail for DrToniRamos@hotmail.com와 같은 규칙에 대 한 이름을 입력 합니다.
    
6. **다음의 경우 이 규칙 적용**에서 조건을 선택하고 필요한 경우 값을 입력합니다. 예를 들어 DrToniRamos@hotmail.com에 보내는 메시지를 암호화하려면 다음을 수행합니다. 
    
  1. **다음의 경우 이 규칙 적용**에서 **받는 사람이 다음과 같음**을 선택합니다.
    
  2. 연락처 목록에서 기존 이름을 선택하거나 **이름 확인** 상자에 새 전자 메일 주소를 입력합니다. 
    
    - 기존 이름을 선택하려면 목록에서 이름을 선택한 다음 **확인**을 클릭합니다.
    
    - 새 이름을 입력 하 고 **이름 확인** 상자에 전자 메일 주소를 입력 한 다음 **이름 확인** 을 선택 하려면 \> **확인**합니다.
    
  7. 조건을 더 추가, **기타 옵션** 을 선택 하 고 **조건 추가** 선택 하 고 목록에서 선택 합니다. 
    
    예, 받는 사람이 조직 외부에 있을 경우에이 규칙을 적용 하려면 **조건 추가** 선택한 다음 선택 **받는 사람이 외부/내부** \> **조직 외부의** \> **확인**합니다.
    
  8. 암호화를 사용 하려면 **다음을 수행**하는에서 새 OME 기능을 사용 하지 않고, **메시지 보안 수정** \> **OME의 이전 버전을 적용**하 고 **저장**을 선택 합니다.
    
    오류가 발생 하는 경우 해당 IRM 라이선스를 사용할 수 없는, 다음 아직 조직에 대 한 OME을 설정 하지 않은 합니다. 지금 OME를 설정 하려는 경우 새 OME 기능을 사용 하 여를 설정 해야 있습니다. 내용은 [Azure 정보 보호 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md)을 참조 하십시오. Microsoft는 더이상 설정의 새 기능 없이 OME의 새 배포를 지원합니다.
    
    다른 작업을 지정 하려면 **작업 추가** 선택할 수 있습니다. 
    
### <a name="to-create-a-rule-for-encrypting-email-messages-without-the-new-ome-capabilities-by-using-windows-powershell-for-exchange-online"></a>Exchange Online 용 Windows PowerShell을 사용 하 여 새 OME 기능 없이 전자 메일 메시지를 암호화 하는 것에 대 한 규칙을 만들려면

1. Exchange Online PowerShell에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)참조 하십시오.
    
2. **New-transportrule** cmdlet을 사용 하 여 규칙을 만들고 _ApplyOME_ 매개 변수를 설정 `$true`합니다.
    
예, DrToniRamos@hotmail.com에 게 보내는 모든 전자 메일 메시지를 암호화할 수 있어야를 요구 하려면 다음을 입력 합니다.
    
```
New-TransportRule -Name "Encrypt rule for Dr Toni Ramos" -SentTo "DrToniRamos@hotmail.com" -SentToScope "NotinOrganization" -ApplyOME $true
```

이 예제의 특징은 다음과 같습니다.
    
- 새 규칙의 이름은 "Dr 박찬식을 Ramos에 대 한 암호화 규칙"입니다.
    
- _SentTo_ 매개 변수는 전자 메일 메시지의 받는 사람을 찾고 하는 조건을 지정 합니다. 전자 메일 주소, 이름, DN (고유 이름), 등 예: 받는 사람을 고유 하 게 식별 하는 모든 값을 사용할 수 있습니다. 이 예제에서는 받는 전자 메일 주소 "DrToniRamos@hotmail.com" 식별 됩니다. 
    
- _SentToScope_ 매개 변수는 받는 사람 위치에 대 한 조회 하는 조건을 지정 합니다. 이 예제에서는 받는 사람의 사서함 hotmail 이므로 "NotInOrganization" 값이 사용 하는 Office 365 조직에 속하지 않습니다. 
    
이 cmdlet를 사용 하 여 메일 흐름 규칙에서 설정할 수 있는 조건에 대 한 자세한 내용은 [New-transportrule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule)을 참조 하십시오.
    
### <a name="remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a>새 OME 기능 없이 암호화 된 전자 메일 회신에서 암호화를 제거 합니다.

전자 메일 사용자에 게 암호화 된 메시지를 보낼 때 해당 메시지의 받는 사람에 게 암호화 된 회신으로 응답할 수 있습니다. 메일 흐름 규칙 하므로 조직에서 전자 메일 사용자를 로그 항목을 볼 암호화 포털에 로그인 필요가 없습니다 회신에서 암호화를 자동으로 제거을 만들 수 있습니다. 이러한 규칙을 정의 하려면 EAC 또는 Windows PowerShell cmdlet을 사용할 수 있습니다. 아직 새 OME 기능을 사용 하지 않는 경우에 하나 조직 또는 조직 내에서 보낸 메시지에 대 한 회신 메시지 내에서 전송 된 메시지를 해독할만. 조직 외부에서 발생 하는 암호화 된 메시지의 암호를 해독할 수는 없습니다.
  
#### <a name="create-a-rule-for-removing-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities-by-using-the-eac"></a>EAC를 사용 하 여 새 OME 기능 없이 암호화 된 전자 메일 회신에서 암호화를 제거 하기 위한 규칙 만들기
<a name="DecryptruleEACNoNewOME"> </a>

1. 웹 브라우저에서 관리자 권한, [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)부여 된 작업이 나 교육용 계정을 사용 하 여 합니다.
    
2. **Admin** 타일을 선택 합니다. 
    
3. Office 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택합니다.
    
4. EAC에서 **메일 흐름** 으로 이동 \> **규칙** \> **+** ( **새로 만들기**) \> **새 규칙 만들기**. EAC를 사용 하는 방법에 대 한 자세한 내용은 [Exchange 관리 센터의 Exchange Online을](https://docs.microsoft.com/exchange/exchange-admin-center)참조 하십시오.
    
5. **이름**받는 메일에서 제거 암호화와 같은 규칙에 대 한 이름을 입력 합니다.
    
6. **하는 경우이 규칙 적용** 에서 등 **의 받는 사람이 있는** 메시지에서 암호화를 제거할 조건을 선택 \> **조직 내부**합니다.
    
7. **다음을 수행**을 선택 **메시지 보안 수정** \> **OME의 이전 버전을 제거**합니다.
    
8. **저장** 을 선택합니다.
    
#### <a name="create-a-rule-to-remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities-by-using-exchange-online-powershell"></a>Exchange Online PowerShell을 사용 하 여 새 OME 기능 없이 암호화 된 전자 메일 회신에서 암호화를 제거 하는 규칙 만들기
<a name="DecryptrulePShellNoNewOME"> </a>

1. Exchange Online PowerShell에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)참조 하십시오.
    
2. _RemoveOME_ 매개 변수를 설정 하 고 **New-transportrule** cmdlet을 사용 하 여 규칙을 만들 `$true`합니다.
    
등을 Office 365 조직의 받는 사람에에서 게 보내진 모든 메일에서 암호화를 제거 하려면 다음을 입력 합니다.
    
```
New-TransportRule -Name "Remove encryption from incoming mail" -SentToScope "InOrganization" -RemoveOME $true
```

이 예제의 특징은 다음과 같습니다.

- 새 규칙의 이름은 "받는 메일에서 암호화 제거" 합니다.

- _SentToScope_ 매개 변수는 받는 사람 위치에 대 한 조회 하는 조건을 지정 합니다. 이 예제에서는 "InOrganization" 값 것임을 나타내는 사용 됩니다. 

  - 받는 사람 사서함, 메일 사용자, 그룹 또는 조직에서 메일 사용이 가능한 공용 폴더는 합니다.

  또는

  - 신뢰할 수 있는 도메인 또는 내부 릴레이 도메인으로 구성 된 허용된 도메인에서 받는 사람의 전자 메일 주소는 하 고 메시지를 보내거나 인증 된 연결을 통해 받은 합니다.
    
이 cmdlet를 사용 하 여 메일 흐름 규칙에서 설정할 수 있는 조건에 대 한 자세한 내용은 [New-transportrule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule)을 참조 하십시오.
    
## <a name="related-topics"></a>관련 항목

[Office 365의 암호화](encryption.md)
  
[Azure 정보 보호 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능 설정](set-up-new-message-encryption-capabilities.md)
  
[암호화된 메시지에 브랜딩 추가](add-your-organization-brand-to-encrypted-messages.md)
  
[Exchange Online에서 흐름 규칙 (전송 규칙) 메일](https://go.microsoft.com/fwlink/p/?LinkId=506707)
  
[Exchange Online Protection의 메일 흐름 규칙(전송 규칙)](https://go.microsoft.com/fwlink/p/?LinkId=506708)
  

