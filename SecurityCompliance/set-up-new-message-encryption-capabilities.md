---
title: 새로운 Office 365 메시지 암호화 기능 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: 새로운 Office 365 메시지 암호화 기능이 Azure Information Protection을 기반으로 구축 되 면 조직에서 조직 내부 및 외부 사용자와 보호 된 전자 메일 통신을 사용할 수 있습니다. 새로운 OME 기능은 다른 Office 365 조 직, Outlook.com, Gmail 및 기타 전자 메일 서비스와 함께 작동 합니다.
ms.openlocfilehash: eddafca15fa4efdd3f929145e7933a3b7dfb5f27
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220648"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>새로운 Office 365 메시지 암호화 기능 설정

Azure Information protection의 보호 기능을 활용 하는 새로운 Office 365 메시지 암호화 (OME) 기능을 사용 하면 조직에서 모든 장치에 있는 모든 사용자와 보호 된 전자 메일을 쉽게 공유할 수 있습니다. 사용자는 Outlook.com, Gmail 및 기타 전자 메일 서비스를 사용 하는 office 365 이외의 다른 office 365 조직과 보호 된 메시지를 주고 받을 수 있습니다.

||
|:-----|
|이 문서는 Office 365 메시지 암호화에 대 한 보다 광범위 한 문서에 포함 되어 있습니다. 이 문서는 관리자와 itpros 전문가를 위한 것입니다. 암호화 된 메시지를 보내거나 받는 방법에 대 한 정보를 찾으려는 경우에는 [Office 365 메시지 암호화 (OME)](ome.md) 의 문서 목록을 참조 하 여 요구 사항에 가장 적합 한 문서를 검색 하세요. |
||

## <a name="get-started-with-ome-by-activating-azure-rights-management-part-of-azure-information-protection"></a>azure 권한 관리, azure Information Protection의 일부를 활성화 하 여 OME을 시작 합니다.

이제 새 OME 기능을 쉽게 시작할 수 있습니다. 2 월 2018 일 현재 Office 365에서는 데이터 센터 내에서 적합 한 조직의 새 OME 기능을 자동으로 사용 하도록 설정 합니다. 조직이 새 Office 365 테 넌 트이 고 조직에 적절 한 구독이 있는 경우에 적합 합니다. azure **Information Protection의 일부인 azure Rights Management (azure RMS)를 사용 하도록 설정한 경우 Office 365 메시지 암호화를 자동으로 사용 하도록 설정 합니다.** OME을 사용 하도록 설정 하기 위해 다른 작업을 수행할 필요가 없습니다. azure 권한 관리를 활성화 하려면 [azure 권한 관리 활성화](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service)를 참조 하세요. 구독에 대 한 자세한 내용은 [Office 365 메시지 암호화 FAQ](ome-faq.md)에서 "새 OME capabilities?을 사용 하려면 무엇을 해야 합니까?"를 참조 하십시오. azure information protection에 대 한 구독을 구입 하는 방법에 대 한 자세한 내용은 [azure information protection](https://azure.microsoft.com/services/information-protection/)을 참조 하세요.
  
AD RMS (Active Directory Rights Management services)와 함께 Exchange Online을 사용 하는 경우에는 이러한 새로운 기능을 즉시 사용 하도록 설정할 수 없습니다. 대신 AD RMS에서 Azure Information Protection로 마이그레이션을 수행 해야 합니다. 마이그레이션이 완료 되 면 다음 단계를 성공적으로 완료할 수 있습니다.
  
Azure Information Protection으로 마이그레이션하지 않고 Exchange Online에서 온-프레미스 AD RMS를 계속 사용 하도록 선택 하는 경우 이러한 새로운 기능을 사용할 수 없게 됩니다.
  
## <a name="how-the-new-capabilities-for-ome-work"></a>OME의 새로운 기능 작동 방식

새로운 Office 365 메시지 암호화 기능은 azure Information protection에서 azure RMS (azure 권한 관리) 라고도 하는 보호 기능을 사용 합니다. 여기에는 전자 메일을 보호 하는 데 도움이 되는 암호화, id 및 권한 부여 정책이 포함 됩니다. 권한 관리 템플릿, [전달 금지 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)및 [암호화 전용 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 사용 하 여 메시지를 암호화할 수 있습니다. 그러면 사용자가 이러한 옵션을 사용 하 여 전자 메일 메시지와 다양 한 Office 365 첨부 파일을 암호화할 수 있습니다. 지원 되는 첨부 파일 형식에 대 한 전체 목록은 [전자 메일 메시지에 대 한 irm 소개에서 "irm 정책이 메시지에 첨부 될 때 확인 되는 파일 형식"](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM)을 참조 하십시오. 관리자는이 보호를 적용 하는 메일 흐름 규칙을 정의할 수도 있습니다. 예를 들어 특정 받는 사람에 게 주소를 지정 하거나 제목 줄에 특정 단어가 포함 된 보호 되지 않는 모든 메시지가 무단으로 액세스 되지 않도록 보호 되며 받는 사람이 메시지 내용을 복사 하거나 인쇄할 수 없는 규칙을 정의할 수 있습니다.
  
이전 버전의 OME과 달리 이러한 새로운 기능은 조직 내부에서 메일을 보내는 지, 아니면 Office 365 외부의 받는 사람에 게 제공 되는지 여부에 관계 없이 통합 된 보낸 사람을 위한 것입니다. 또한 outlook 2016 또는 웹용 outlook에서 Office 365 계정으로 전송 되는 보호 된 전자 메일 메시지를 받는 받는 사람은 메시지를 확인 하기 위해 추가 작업을 수행할 필요가 없습니다. 완벽 하 게 작동 합니다. 다른 전자 메일 클라이언트와 전자 메일 서비스 공급자를 사용 하는 받는 사람도 향상 된 환경을 제공 합니다. 자세한 내용은 [Office 365의 보호 된 메시지에 대 한](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) 정보 및 [보호 된 메시지를 여는 방법](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098)를 참조 하십시오.

이전 버전의 OME와 새 OME 기능 간의 차이점에 대 한 자세한 목록은 [OME 버전 비교](ome-version-comparison.md)를 참조 하십시오.
  
## <a name="steps-to-manually-set-up-the-new-capabilities-for-ome"></a>OME에 대 한 새 기능을 수동으로 설정 하는 단계

대부분의 Office 365 조직에서는 새로운 OME 기능이 자동으로 사용 하도록 설정 됩니다. 조직에서 OME을 자동으로 사용 하도록 설정 하지 않았거나 새 OME 기능을 해제 한 경우에는 다음 단계에 따라 OME에 대 한 새 기능을 수동으로 설정 합니다.
  
### <a name="to-manually-set-up-the-new-capabilities-for-ome"></a>OME에 대 한 새 기능을 수동으로 설정 하려면

1. 조직에 적합 한 구독을 보유 하 고 있는지 확인 합니다. 구독에 대 한 자세한 내용은 [Office 365 메시지 암호화 FAQ](ome-faq.md)에서 "새 OME capabilities?을 사용 하려면 무엇을 해야 합니까?"를 참조 하세요. azure information protection에 대 한 구독을 구입 하는 방법에 대 한 자세한 내용은 [azure information protection](https://azure.microsoft.com/services/information-protection/)을 참조 하세요.

2. Microsoft에서 Azure Information Protection의 루트 키 (기본값)를 관리할 지, 아니면 직접 키를 가져오거나 확인을 통해이 키를 직접 생성 및 관리 하도록 할지 결정 합니다. 이 키를 직접 생성 하 고 관리 하려는 경우에는 OME에 대 한 새 기능을 설정 하기 전에 몇 가지 단계를 완료 해야 합니다. 자세한 내용은 [Azure information Protection 테 넌 트 키 계획 및 구현](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key)를 참조 하세요. OME를 설정 하기 전에이 단계를 완료 하는 것이 좋습니다.

3. Azure 권한 관리를 활성화 하 여 OME의 새 기능을 사용 하도록 설정 합니다. 자세한 내용은 [Azure 권한 관리 활성화](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service)를 참조 하세요. 이렇게 하면 Office 365에서 자동으로 새 OME 기능을 사용 하도록 설정 합니다.

    > [!TIP]
    > 웹용 Outlook은 해당 UI를 캐시 하므로이 클라이언트를 사용 하는 전자 메일 메시지에 OME에 대 한 새 기능을 적용 하기 전에 하루를 기다리는 것이 좋습니다. 새 구성을 반영 하기 위해 UI를 업데이트 하기 전에 OME의 새 기능을 사용할 수 없습니다. UI를 업데이트 한 후 사용자는 OME의 새 기능을 사용 하 여 전자 메일 메시지를 보호할 수 있습니다.
  
4. 반드시 새 메일 흐름 규칙을 설정 하거나 Office 365에서 조직 으로부터 보낸 메시지를 암호화 하는 방법 및 시기를 정의 하는 기존 메일 흐름 규칙을 업데이트 합니다.

## <a name="verify-that-the-new-capabilities-for-ome-are-configured-properly-by-using-windows-powershell"></a>Windows PowerShell을 사용 하 여 OME에 대 한 새 기능이 제대로 구성 되어 있는지 확인

Exchange Online PowerShell을 통해 OME의 새 기능을 사용 하도록 테 넌 트를 올바르게 구성 했는지 확인 하려면 다음 단계를 수행 합니다.
  
1. Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.

2. 다음 구문을 사용 하 여 irmconfiguration cmdlet을 실행 합니다.

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   예를 들면 다음과 같습니다.

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

    여기서 전자 메일 주소는 Office 365 조직에 있는 사용자의 전자 메일 주소입니다. 선택 사항 이지만 보낸 사람 전자 메일 주소를 제공 하면 시스템에서 추가 검사를 수행 합니다. 검색 결과는 다음과 같습니다.

     ```text
    Results : Acquiring RMS Templates ...
                - PASS: RMS Templates acquired.  Templates available: Contoso  - Confidential View Only, Contoso  - Confidential, Do Not 
            Forward.
            Verifying encryption ...
                - PASS: Encryption verified successfully.
            Verifying decryption ...
                - PASS: Decryption verified successfully.
            Verifying IRM is enabled ...
                - PASS: IRM verified successfully.

            OVERALL RESULT: PASS
    ```

    여기서 *Contoso* 는 Office 365 조직의 이름으로 대체 됩니다.

    결과에서 반환 되는 기본 서식 파일의 이름은 위의 결과에 표시 되는 것과 다를 수 있습니다.

    기본 서식 파일에 대 한 서식 파일 및 정보에 대 한 자세한 내용은 [Azure information Protection의 템플릿 구성 및 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오. 전달 금지 옵션, 암호화 전용 옵션 및 추가 템플릿을 만드는 방법에 대 한 자세한 내용은 [Azure 권한 관리에 대 한 사용 권한 구성을](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights)참조 하십시오.

3. Remove-PSSession cmdlet을 실행 하 여 권한 관리 서비스와의 연결을 끊습니다.
    
     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-new-mail-flow-rules-that-use-the-new-ome-capabilities"></a>다음 단계: 새 OME 기능을 사용 하는 새 메일 흐름 규칙 정의

새 OME 배포의 경우이 단계는 선택 사항 이지만,이 단계는 보내는 메일을 암호화 하기 위해 이미 메일 흐름 규칙이 설정 된 기존 OME 배포에 필요 합니다. 새 OME 기능을 활용 하려면 기존 메일 흐름 규칙을 업데이트 해야 합니다. 그렇지 않으면 사용자는 새로운 OME 환경이 아닌 이전 HTML 첨부 파일 형식을 사용 하는 암호화 된 메일을 계속 받게 됩니다.
  
메일 흐름 규칙은 전자 메일 메시지를 암호화 해야 하는 조건 및 해당 암호화를 제거 하는 조건에 따라 결정 됩니다. 규칙에 대 한 동작을 설정 하면 규칙 조건과 일치 하는 모든 메시지가 전송 될 때 암호화 됩니다.
  
메일 흐름 규칙에 대 한 자세한 내용은 [Office 365에서 전자 메일 메시지를 암호화 하는 메일 흐름 규칙 정의](define-mail-flow-rules-to-encrypt-email.md)를 참조 하십시오.
  
## <a name="related-topics"></a>관련 항목

[Outlook에서 암호화 된 메시지 보내기, 확인 및 회신](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)
  
[Enable-enable-aadrm](https://docs.microsoft.com/powershell/module/aadrm/enable-aadrm?view=azureipps)
  
[원격 PowerShell을 사용하여 Exchange Online에 연결](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx)
  
[Office 365에서 전자 메일 메시지를 암호화하기 위한 메일의 흐름 규정을 정의](define-mail-flow-rules-to-encrypt-email.md)
