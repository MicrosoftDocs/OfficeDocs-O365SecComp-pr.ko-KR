---
title: 새로운 Office 365 메시지 암호화 기능 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/19/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: 새로운 Office 365 메시지 암호화 Azure 정보 보호 조직의 위쪽에 구축 된 기능을 사용 하 여 수 내부 테두리와 조직 외부의 사용자와 전자 메일 통신을 보호 합니다. 다른 Office 365, Outlook.com, Gmail, 조직과 다른 전자 메일 서비스를 사용 하는 새 OME 기능입니다.
ms.openlocfilehash: c24b2f9b612b863217df8afd951424d1a89295c9
ms.sourcegitcommit: d89c24258123a3ffde574a391d59afd3aea8470d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2018
ms.locfileid: "23955420"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>새로운 Office 365 메시지 암호화 기능 설정

Azure 정보 보호의 보호 기능을 활용 하는 새로운 Office 365 메시지 암호화 (OME) 기능을 사용 하면 조직 모든 장치에서 모든 사람과 보호 된 전자 메일을 쉽게 공유할 수 있습니다. 사용자가 보내고 Outlook.com, Gmail, 및 기타 전자 메일 서비스를 사용 하 여 Office 365가 아닌 고객은 물론 다른 Office 365 조직으로 보호 된 메시지를 받을 수 있습니다.
  
## <a name="get-started-with-ome-by-activating-azure-rights-management-part-of-azure-information-protection"></a>Azure 권한 관리, Azure 정보 보호의 일부를 활성화 하 여 OME 시작 하기

이제 새 OME 기능을 사용 하는 것이 쉽습니다. 2 월 2018를 기준으로 자동으로 Office 365에는 데이터 센터 내에서 사용할 수 있는 조직에 대 한 새 OME 기능 수 있습니다. 새 Office 365 테 넌 트 이며 조직에 적합 한 구독 하는 경우 조직 대상이있지 않습니다. **하는 경우 Azure 권한 관리 (Azure RMS) 부분에서는 Azure 정보 보호를 사용 하도록 설정한 다음 Office 365 메시지 암호화 하면 자동으로 활성화 했습니다.** OME를 사용 하도록 설정 하려면 다른 작업을 수행할 필요가 없습니다. Azure 권한 관리를 활성화 하려면 [Azure 권한 관리 활성화](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service)를 참조 하십시오. 구독에 대 한 정보를 "어떤 구독 해야하는 새 OME capabilities?를 사용 하 여" [Office 365 메시지 암호화 FAQ](ome-faq.md)에서 참조 하십시오. Azure 정보 보호에 대 한 구독 구입 하는 방법에 대 한 정보를 [Azure 정보 보호](https://azure.microsoft.com/services/information-protection/)를 참조 하십시오.
  
Exchange Online Active Directory Rights Management 서비스 (AD RMS)를 사용할 경우 즉시 이러한 새 기능을 활성화할 수 없습니다. 대신, 먼저 Azure 정보 보호 AD RMS에서 마이그레이션 해야 합니다. 마이그레이션 완료 했을 때, 다음이 단계를 성공적으로 완료할 수 있습니다.
  
계속 사용 하려는 경우 온-프레미스 AD RMS Exchange Online과 Azure 정보 보호로 마이그레이션하는 대신, 됩니다 이러한 새 기능을 사용할 수 없게 됩니다.
  
## <a name="how-the-new-capabilities-for-ome-work"></a>OME에 대 한 새로운 기능 작동 방식

새로운 Office 365 메시지 암호화 기능 Azure 정보 보호에서 Azure 권한 관리 (Azure RMS)이 라고도 하는 보호 기능을 사용 합니다. 이 전자 메일을 보호 하는 암호화, id 및 권한 부여 정책을 포함 됩니다. 권한 관리 템플릿, [전달 하지 않음 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)및 [암호화 전용 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 사용 하 여 메시지를 암호화할 수 있습니다. 사용자가 이러한 옵션을 사용 하 여 전자 메일 메시지와 다양 한 Office 365 첨부 파일에 암호화할 수 있습니다. 지원 되는 첨부 파일 형식 목록은 전체 [전자 메일 메시지에 대 한 IRM 사용 소개 "IRM 정책 메시지에 첨부 하는 경우에 파일 형식 포함"을](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM)참조 하십시오. 관리자로 서이 보호 기능을 적용 하는 메일 흐름 규칙을 정의할 수 있습니다. 예, 여기에서 특정 받는 사람에 게 해결 되는 또는 제목에 특정 단어가 포함 된 모든 보호 되지 않은 메시지 무단된 액세스 로부터 보호 되 고 받는 사람 복사 하거나 메시지의 내용을 인쇄할 수 없습니다는 규칙을 정의할 수 있습니다.
  
OME은 이전 버전과 달리 이러한 새로운 기능은 조직 내부 또는 외부 Office 365의 받는 사람에 게 메일을 보낼 때 여부 통합된 발신자 경험을 제공 합니다. 또한 Outlook 2016 또는 웹에서 Outlook에서 Office 365 계정에 게 보낸 보호 된 전자 메일 메시지를 받을 사람의 메시지를 볼 수 있는 추가 조치를 취할 필요가 없습니다. 원활 하 게 작동합니다. 다른 전자 메일 클라이언트 및 전자 메일 서비스 공급자를도 사용 하 여 받는 사람에 게 향상된 된 환경을 포함 합니다. 내용은 [Office 365의 보호 된 메시지에 대 한 자세한 내용](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) 및 [보호 된 메시지를 열려면 어떻게](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098)를 참조 하십시오.
  
## <a name="steps-to-manually-set-up-the-new-capabilities-for-ome"></a>수동으로 OME에 대 한 새로운 기능을 설정 하는 단계

조직 자동으로 없는 OME이 옵션을 설정 또는 해제 OME를 설정 하는 경우에 수동으로 OME에 대 한 새로운 기능을 설정 하려면 다음이 단계를 수행 합니다.
  
### <a name="to-manually-set-up-the-new-capabilities-for-ome"></a>OME에 대 한 새로운 기능을 수동으로 설정 하려면

1. 조직에 대 한 오른쪽 구독을 했는지 확인 합니다. 구독에 대 한 내용은 "어떤 구독 해야하는 새 OME capabilities?를 사용 하 여"에서 참조는 [Office 365 메시지 암호화 FAQ.](ome-faq.md) Azure 정보 보호에 대 한 구독 구입 하는 방법에 대 한 정보를 [Azure 정보 보호](https://azure.microsoft.com/services/information-protection/)를 참조 하십시오.
    
2. Azure 정보 보호 (기본값)에 대 한 루트 키를 관리 하거나 생성 하 고 (직접 키로 이동한 다음 또는 BYOK 맨앞으로 알려진) 사용자가 직접이 키를 관리 하는 Microsoft 여부를 결정 합니다. 생성 하 고 사용자가 직접이 키를 관리 하려는 경우 OME에 대 한 새로운 기능을 설정 하기 전에 일부 단계를 완료 해야 합니다. 자세한 내용은 [계획 및 구현 하 여 Azure 정보 보호 테 넌 트 키를](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key)참조 하십시오. OME를 설정 하기 전에 다음이 단계를 완료 하는 것이 좋습니다.
    
3. Azure 권한 관리를 활성화 하 여 OME에 대 한 새로운 기능을 사용 합니다. 자세한 내용은 [Azure 권한 관리 활성화](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service)를 참조 하십시오. 자동이 위해 Office 365 하면 새 OME 기능을 설정 합니다.
    
    > [!TIP]
    > 웹에 있는 outlook 하루에이 클라이언트를 사용 하 여 전자 메일 메시지에 OME에 대 한 새로운 기능을 적용 하기 전에 대기 하는 것이 좋습니다 하므로 해당 UI을 캐시 합니다. UI 새 구성을 반영 하도록 업데이트를 하기 전에는 OME에 대 한 새로운 기능을 사용할 수 없습니다. UI 업데이트 하 고 나면 사용자가 OME에 대 한 새로운 기능을 사용 하 여 전자 메일 메시지를 보호할 수 있습니다. 
  
4. (선택 사항) 새 메일 흐름 규칙을 설정 하거나 조직에서 보낸 메시지를 암호화 하는 Office 365 시기와 방법을 정의 하는 기존 메일 흐름 규칙을 업데이트 합니다.
    
## <a name="verify-that-the-new-capabilities-for-ome-are-configured-properly-by-using-windows-powershell"></a>Windows PowerShell을 사용 하 여 OME에 대 한 새 기능이 제대로 구성 되었는지 확인

Exchange Online PowerShell을 통해 OME에 대 한 새로운 기능을 사용 하 여 테 넌 트 제대로 구성 되었는지 확인 하려면 다음이 단계를 수행 합니다.
  
1. Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 하는 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)참조 하십시오.
    
2. 다음 구문을 사용 하 여 Test-irmconfiguration cmdlet을 실행 합니다.
    
    ```Test-IRMConfiguration [-Sender <email address >]```  

   예를 들면 다음과 같습니다.
    
    ```Test-IRMConfiguration -Sender securityadmin@contoso.com```

    여기서 전자 메일 주소는 Office 365 조직에 있는 사용자의 전자 메일 주소입니다. 옵션, 제공 하는 동안 보낸 전자 메일 주소를 추가 검사를 수행 하려면 시스템을 강제 합니다.
    
    결과 다음과 같은 같아야 합니다.
    
    ```
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

    여기서 *Contoso* 는 Office 365 조직 이름으로 대체 됩니다. 
    
    결과에 반환 하는 기본 서식 파일의 이름은 위의 결과에 표시 된 것과 다른 수 있습니다.
    
    서식 파일 및 기본 서식 파일에 대 한 정보에 대 한 소개를 [구성 하 고 Azure 정보 보호에 대 한 서식 파일 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오. 착신 전환 안함에 대 한 정보에 대 한 옵션을 암호화 전용 옵션을 및 방법을 만들려면 추가 서식 파일 또는 어떤 권한에 대해 알아봅니다 기존 서식 파일에 포함 된, 참조 [Azure 권한 관리에 대 한 사용 권한을 구성](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights)합니다.
    
3. 권한 관리 서비스에서 연결을 끊으려면 Remove-pssession cmdlet을 실행 합니다.
    
    ```Remove-PSSession $session```

## <a name="next-steps-define-new-mail-flow-rules-that-use-the-new-ome-capabilities"></a>다음 단계: 새 OME 기능을 사용 하는 새 메일 흐름 규칙 정의
<a name="Rules_1"> </a>

그러나이 단계는 새 OME 배포에 대 한 선택적,이 단계는 메일 흐름 설정 된 규칙 최대 보내는 메일 암호화에 이미 있는 기존 OME 배포에 필요 합니다. 새 OME 기능을 활용 하려는 경우 기존 메일 흐름 규칙을 업데이트 해야 합니다. 그렇지 않은 경우 사용자에 게 새, 원활 하 게 OME 경험 하는 대신 이전 HTML 첨부 파일 형식을 사용 하는 암호화 된 메일을 받도록 계속 됩니다.
  
메일 흐름 규칙에서 어떤 조건 전자 메일 메시지를 암호화 해야, 해당 암호화를 제거 하기 위한 조건, 결정 합니다. 규칙에 대 한 동작을 설정 하면는 보내면 규칙 조건에 맞는 모든 메시지는 암호화 됩니다.
  
메일 흐름 규칙에 대 한 자세한 내용은 [Office 365에서 전자 메일 메시지를 암호화 메일 흐름 규칙 정의](define-mail-flow-rules-to-encrypt-email.md)참조 하십시오.
  
## <a name="related-topics"></a>관련 항목
<a name="Rules_1"> </a>

[보내기, 보기 및 Outlook에서 암호화 된 메시지에 회신](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)
  
[Aadrm 사용](https://docs.microsoft.com/powershell/module/aadrm/enable-aadrm?view=azureipps)
  
[원격 PowerShell을 사용하여 Exchange Online에 연결](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx)
  
[Office 365에서 전자 메일 메시지를 암호화 하는 메일 흐름 규칙 정의](define-mail-flow-rules-to-encrypt-email.md)
  

