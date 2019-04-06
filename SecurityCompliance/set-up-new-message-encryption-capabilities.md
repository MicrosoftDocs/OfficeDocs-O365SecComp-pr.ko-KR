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
ms.openlocfilehash: fd237e537aa1ff961d2d975b3b30f4a51744ba7c
ms.sourcegitcommit: e24f70699021c4f4ba56508ad0afb6f65010c357
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/05/2019
ms.locfileid: "31479654"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>새로운 Office 365 메시지 암호화 기능 설정

새 Office 365 메시지 암호화 (OME) 기능을 사용 하면 조직에서 모든 장치에 있는 모든 사용자와 보호 된 전자 메일을 공유할 수 있습니다. 사용자는 Outlook.com, Gmail 및 기타 전자 메일 서비스를 사용 하는 office 365 고객 뿐만 아니라 다른 office 365 조직과 보호 된 메시지를 교환할 수 있습니다.


>[!NOTE]
>이 문서는 관리자 및 IT 전문가를 위한 것입니다. 최종 사용자 인 경우 [Office 365 메시지 암호화 (OME)](ome.md) 에서 해당 솔루션에 대 한 문서 목록을 참조 하세요.

Office 365 테 넌 트에서 새로운 OME 기능을 사용할 수 있도록 하려면 아래 단계를 수행 합니다.

## <a name="verify-azure-rights-management-arm-is-active"></a>ARM (Azure 권한 관리)이 활성화 되어 있는지 확인

>[!NOTE]
>새로운 OME 기능을 사용 하 여 azure [Information protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection)의 보호 기능 [(ARM (azure Rights Management)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms)에서 사용한 기술)을 활용할 있습니다.

새 OME 기능을 사용 하는 유일한 필수 구성 요소는 Office 365 테 넌 트에서 [ARM (Azure 권한 관리)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) 을 활성화 해야 한다는 것입니다. 이 경우에는 Office 365에서 새 OME 기능을 자동으로 활성화 하므로 작업을 수행할 필요가 없습니다.

또한 ARM은 가장 적합 한 요금제에 대해서도 자동으로 활성화 되므로이 두 가지 측면에서 어떤 작업을 수행 하지 않아도 됩니다. 자세한 내용은 [Azure 권한 관리 정품 인증](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) 을 참조 하세요.

>[!IMPORTANT]
>Exchange Online에서 AD RMS (Active Directory Rights Management service)를 사용 하는 경우 새 OME 기능을 사용 하려면 먼저 [Azure Information Protection로 마이그레이션해야](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) 합니다. AD RMS는 ARM과 호환 되지 않습니다.  

자세한 내용은 다음을 참조 하세요.

- [새 OME 기능을 사용 하는 데 필요한 구독은 무엇입니까?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) 구독 계획에 ARM이 포함 된 Azure Information Protection이 포함 되어 있는지 여부를 확인할 수 있습니다.
- [Azure information Protection](https://azure.microsoft.com/en-us/services/information-protection/) 적격 구독 구입에 대 한 정보입니다.  

### <a name="manually-activating-arm"></a>ARM을 수동으로 활성화

ARM을 사용 하지 않도록 설정 했거나 어떤 이유로 자동으로 활성화 되지 않은 경우에서 다음 위치에서 수동으로 정품 인증을 수행할 수 있습니다.

- **office 365 관리 센터**: 지침을 보려면 [office 365 관리 센터에서 Azure Rights Management를 활성화 하는 방법을](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) 참조 하세요.
- **azure portal**: 지침을 보려면 [azure portal에서 azure Rights Management를 활성화 하는 방법을](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) 참조 하세요.

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a>Azure Information Protection 테 넌 트 키 관리 구성

이 단계는 선택 사항입니다. Microsoft가 Azure Information Protection의 루트 키를 관리 하도록 허용 하는 것은 대부분의 Office 365 테 넌 트에 대 한 기본 설정 및 권장 되는 모범 사례입니다. 이 경우에는 작업을 수행 하지 않아도 됩니다.

규정 준수 요구 사항 예를 들면, 고유한 루트 키를 생성 하 고 관리 하는 데 필요할 수 있는 몇 가지 이유가 있습니다 (사용자가 직접 키를 가져옵니다 (byok). 이 경우 새 OME 기능을 설정 하기 전에 필요한 단계를 완료 하는 것이 좋습니다. 자세한 내용은 [Azure Information Protection 테 넌 트 키 계획 및 구현](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) 를 참조 하세요.

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a>Exchange Online PowerShell에서 새 OME 구성 확인

Office 365 테 넌 트가 [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)의 새 OME 기능을 사용 하도록 올바르게 구성 되어 있는지 확인할 수 있습니다.
  
1. Office 365 테 넌 트에서 전역 관리자 권한이 있는 계정을 사용 하 여 [Exchange Online PowerShell에 연결](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) 합니다.

2. 다음 구문을 사용 하 여 irmconfiguration cmdlet을 실행 합니다.

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   **예제**:

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - 보낸 사람 전자 메일을 제공 하는 것은 선택 사항 이지만 시스템에서 추가 검사를 수행 합니다. Office 365 테 넌 트에서 모든 사용자의 전자 메일 주소를 사용 합니다. 

     결과는 다음과 비슷해야 합니다.

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

   - Office 365 조직 이름이 *Contoso*를 대체 합니다.

   - 기본 서식 파일 이름은 위에 표시 된 이름과 다를 수 있습니다. 자세한 내용은 [Azure Information Protection의 서식 파일 구성 및 관리](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) 를 참조 하세요.

3. Remove-PSSession cmdlet을 실행 하 여 권한 관리 서비스와의 연결을 끊습니다.

     ```powershell
     Remove-PSSession $session
     ```

## <a name="update-mail-flow-rules-to-use-new-ome-capabilities"></a>메일 흐름 규칙을 업데이트 하 여 새 OME 기능 사용

Office 365 테 넌 트에서 [전자 메일을 암호화 하기 위해](define-mail-flow-rules-to-encrypt-email.md) 이전에 구성 된 메일 흐름 규칙이 있는 경우 이러한 기존 규칙을 업데이트 하 여 새 OME 기능을 사용 해야 합니다. 새 배포의 경우에는이 단계를 수행 하지 않아도 됩니다.   

>[!Note]
>메일 흐름 규칙은 전자 메일 메시지를 암호화 하는 조건 및 암호화를 제거 해야 하는 경우를 정의 합니다. 자세한 내용은 [Office 365에서 전자 메일 메시지를 암호화 하기 위한 메일 흐름 규칙 정의를](define-mail-flow-rules-to-encrypt-email.md) 참조 하세요.

새 OME 기능을 사용 하도록 기존 규칙을 업데이트 하려면 다음을 수행 합니다.

1. Office 365 관리 센터에서 **관리 센터 > Exchange**로 이동 합니다.

2. Exchange 관리 센터에서 **메일 흐름 > 규칙**으로 이동 합니다. 
3. 각 규칙에 대해 **다음을 수행 합니다**.
    - **메시지 보안 수정을**선택 합니다.
    - **Office 365 메시지 암호화 및 권한 보호 적용을**선택 합니다.
    - 목록에서 RMS 템플릿을 선택 합니다.
    - **저장**을 선택합니다.
    - **확인**을 선택합니다.
  
>[!IMPORTANT]
>기존 메일 흐름 규칙을 업데이트 하지 않으면 사용자는 새 OME 기능 대신 이전 HTML 첨부 파일 형식을 사용 하는 암호화 된 메일을 계속 수신 합니다.
