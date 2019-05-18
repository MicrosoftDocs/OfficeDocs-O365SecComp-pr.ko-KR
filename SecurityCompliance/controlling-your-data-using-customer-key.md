---
title: 고객 키를 사용하여 Office 365에서 데이터 제어
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/1/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
ms.collection:
- M365-security-compliance
description: Exchange Online, 비즈니스용 Skype, SharePoint Online 및 비즈니스용 OneDrive에 대 한 Office 365의 고객 키를 설정 하는 방법을 알아봅니다. 고객 키를 사용 하 여 조직의 암호화 키를 제어 하 고 Office 365을 구성 하 여 Microsoft의 데이터 센터에 있는 휴지 상태에 있는 사용자에 대 한 정보를 암호화 합니다.
ms.openlocfilehash: 839d0b56b3748e2ab4ccecc30a084447f22131aa
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153720"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a>고객 키를 사용하여 Office 365에서 데이터 제어

고객 키를 사용 하 여 조직의 암호화 키를 제어 하 고 Microsoft 데이터 센터의 휴지 상태에서 데이터를 암호화 하는 데 사용 하도록 Office 365를 구성 합니다. 즉, 고객 키를 사용 하 여 고객은 해당 키를 포함 하는 암호화 계층을 추가할 수 있습니다. 미사용 데이터에는 SharePoint Online 및 비즈니스용 OneDrive에 저장되어 있는 사서함과 파일에 저장된 Exchange Online 및 비즈니스용 Skype의 데이터를 포함합니다.
  
Office 365에 대해 고객 키를 사용 하려면 먼저 Azure를 설정 해야 합니다. 이 항목에서는 필요한 Azure 리소스를 만들고 구성 하기 위해 수행 해야 하는 단계를 설명 하 고 Office 365에서 고객 키를 설정 하는 단계를 제공 합니다. Azure 설치를 완료 한 후에는 조직의 사서함과 파일에 할당할 정책 및 키를 결정 합니다. 정책을 할당 하지 않을 사서함과 파일은 Microsoft에서 제어 및 관리 하는 암호화 정책을 사용 합니다. 고객 키에 대 한 자세한 내용은 또는 일반 개요를 보려면 [Customer key For Office 365 FAQ](service-encryption-with-customer-key-faq.md)를 참조 하세요.
  
> [!IMPORTANT]
> 이 항목의 모범 사례를 따르는 것이 좋습니다. 이를 **팁** 및 **중요**로 지칭 합니다. 고객 키를 사용 하 여 전체 조직에 해당 하는 범위를 갖는 루트 암호화 키를 제어할 수 있습니다. 즉, 이러한 키를 사용한 실수에 큰 영향을 줄 수 있으며 서비스 중단 또는 irrevocable 데이터 손실을 초래할 수 있습니다. 
  
## <a name="before-you-begin-setting-up-customer-key"></a>Customer 키 설정을 시작 하기 전에
<a name="Beforeyoustart"> </a>

시작 하기 전에 조직에 적합 한 라이선스를가지고 있는지 확인 합니다. Office 365의 고객 키가 Office 365 E5 또는 Advanced 준수 SKU에 제공 됩니다.
  
그런 다음이 항목의 개념과 절차를 이해 하려면 [Azure 키 보관소](https://azure.microsoft.com/en-us/documentation/services/key-vault/) 설명서를 검토 해야 합니다. 또한 Azure에서 사용 되는 용어 (예: [테 넌 트](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant))에 익숙해지는 것이 좋습니다.
  
설명서를 포함 하 여 고객 키에 대 한 의견을 제공 하려면 아이디어, 제안 사항 및 전망을 customerkeyfeedback@microsoft.com에 게 보냅니다.
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a>Office 365에 대 한 고객 키 설정 개요
<a name="Overview"> </a>

고객 키를 설정 하려면 다음 작업을 완료 합니다. 이 항목의 나머지 부분에서는 각 작업에 대 한 자세한 지침을 제공 하거나 프로세스의 각 단계에 대 한 추가 정보로 연결 되는 링크에 대해 설명 합니다.
  
**Azure 및 Microsoft FastTrack:**
  
이러한 작업의 대부분은 Azure PowerShell에 원격으로 연결 하 여 완료 합니다. 최상의 결과를 위해 Azure PowerShell의 버전 4.4.0 이상을 사용 합니다.
  
- [두 개의 새 Azure 구독을 만듭니다.](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [필수 보존 기간을 사용 하도록 Azure 구독 등록](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    등록에는 영업일 중 근무일까지 소요 될 수 있습니다.
    
- [Office 365에 대 한 고객 키를 정품 인증 하기 위한 요청 제출](controlling-your-data-using-customer-key.md#FastTrack)
    
    새로운 두 Azure 구독을 만든 후에는 Microsoft FastTrack 포털에서 호스팅되는 웹 양식을 완료 하 여 해당 하는 고객 키 제공 요청을 제출 해야 합니다. **FastTrack 팀은 고객 키에 대 한 지원을 제공 하지 않습니다. Office는 FastTrack 포털을 사용 하 여 양식을 전송 하 고 고객 키에 대 한 관련 서비스를 추적 하는 데 도움이 됩니다**.
  
고객 키 제안을 제출 하면 Microsoft에서 요청을 검토 하 고 나머지 설치 작업을 계속 진행할 수 있을 때 사용자에 게이를 알립니다. 이 프로세스에는 최대 5 일이 소요 될 수 있습니다.
    
- [각 구독에 프리미엄 Azure 키 자격 증명 모음 만들기](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [각 키 자격 증명 모음에 사용 권한 할당](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [키 자격 증명 모음에서 일시 삭제를 사용 하도록 설정 하 고 확인](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [키를 만들거나 가져오는 방법으로 각 키 보관소에 키를 추가 합니다.](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [키의 복구 수준 확인](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [Azure 키 자격 증명 모음 백업](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [Azure 키 자격 증명 모음 구성 설정 확인](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [각 Azure Key Vault 키에 대 한 URI 가져오기](controlling-your-data-using-customer-key.md#GetKeyURI)
    
**Office 365에서 다음을 수행 합니다.**
  
Exchange Online 및 비즈니스용 Skype:
  
- [Exchange Online 및 비즈니스용 Skype에서 사용 하기 위한 DEP (데이터 암호화 정책) 만들기](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [사서함에 DEP 할당](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [사서함 암호화 유효성 검사](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
SharePoint Online 및 비즈니스용 OneDrive:
  
- [각 SharePoint Online 및 비즈니스용 OneDrive 지역에 대 한 DEP (데이터 암호화 정책)를 만듭니다.](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [그룹 사이트, 팀 사이트 및 비즈니스용 OneDrive의 암호화 확인](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a>Azure Key Vault의 완료 작업 및 고객 키 용 Microsoft FastTrack
<a name="AzureSteps"> </a>

Office 365에 대 한 고객 키를 설정 하려면 Azure Key Vault에서 이러한 작업을 완료 합니다. Exchange Online 및 비즈니스용 Skype 또는 SharePoint Online 및 비즈니스용 OneDrive에 대해 고객 키를 설정 하려는 지, 아니면 Office 365에서 지원 되는 모든 서비스에 대해이 단계를 수행 해야 합니다.
  
### <a name="create-two-new-azure-subscriptions"></a>두 개의 새 Azure 구독을 만듭니다.
<a name="Create2newsubs"> </a>

고객 키에는 두 개의 Azure 구독이 필요 합니다. 최상의 방법으로는 고객 키와 함께 사용할 새로운 Azure 구독을 만드는 것이 좋습니다. Azure Key Vault 키에는 동일한 AAD (Azure Active Directory) 테 넌 트의 응용 프로그램에 대해서만 권한을 부여할 수 있으며, DEPs가 할당 되는 Office 365 조직에 사용 되는 것과 동일한 Azure AD 테 넌 트를 사용 하 여 새 구독을 만들어야 합니다. 예를 들어 Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 자세한 단계는 [Azure for](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/)a a a a a a a a a a a as를 참조 하세요.
  
> [!IMPORTANT]
> 고객 키에는 각 DEP (데이터 암호화 정책)에 대 한 두 개의 키가 필요 합니다. 이를 위해서는 두 개의 Azure 구독을 만들어야 합니다. 조직의 개별 구성원이 각 구독에서 하나의 키를 구성 하는 것이 가장 좋은 방법입니다. 또한 이러한 Azure 구독은 Office 365의 암호화 키를 관리 하는 데에만 사용 해야 합니다. 이렇게 하면 운영자 중 한 명에 게 실수로 또는 악의적으로 삭제 되거나 자신이 담당 하는 키를 잘못 관리 하는 경우를 대비해 조직이 보호 됩니다. <br/> Azure Key Vault 리소스를 관리 하는 데에만 사용 되는 새 Azure 구독을 고객 키와 함께 사용 하도록 설정 하는 것이 좋습니다. 조직에 대해 만들 수 있는 Azure 구독 수에는 실질적인 제한이 없습니다. 이러한 모범 사례를 따르면 고객 키에서 사용 하는 리소스를 관리 하는 동안 인간 오류가 발생 하는 영향은 최소화할 수 있습니다. 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a>Office 365에 대 한 고객 키를 정품 인증 하기 위한 요청 제출
<a name="FastTrack"> </a>

Azure 단계를 완료 한 후에는 [Microsoft FastTrack 포털](https://fasttrack.microsoft.com/)에서 제공 요청을 제출 해야 합니다. FastTrack 웹 포털을 통해 요청을 제출 하면 Microsoft는 Azure 키 자격 증명 모음 구성 데이터와 사용자가 제공한 연락처 정보를 확인 합니다. 조직의 승인 된 관리자와 관련 하 여 제안 양식에서 선택한 항목은 고객 키 등록을 완료 하는 데 필수적이 고 필수적입니다. 양식에서 선택한 조직의 직원은 고객 키 데이터 암호화 정책에 사용 되는 모든 키를 해지 하 고 파기 하기 위한 요청의 신뢰성을 보장 하는 데 사용 됩니다. 이 단계를 한 번 수행 하 여 Exchange Online 및 비즈니스용 Skype를 위한 고객 키를 정품 인증 하 고 SharePoint Online 및 비즈니스용 OneDrive에 대 한 고객 키를 활성화 해야 합니다.
  
고객 키를 정품 인증 하기 위한 제안을 제출 하려면 다음 단계를 완료 합니다.
  
1. Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 여 [Microsoft FastTrack 포털](https://fasttrack.microsoft.com/)에 로그인 합니다.
    
2. 로그인 한 후 **대시보드로**이동 합니다.
    
3. **서비스**를 선택 하 고 현재 서비스 목록을 검토 합니다.
    
4. 사용자에 게 제공 되는 혜택에 대 한 **자세한 정보** 를 선택 합니다. 
    
  - **Exchange Online 및 비즈니스용 Skype:** **고객 키에서 Exchange 제공에 대 한** **자세한 정보** 를 선택 합니다. 
    
  - **SharePoint Online 및 비즈니스용 OneDrive:** **SharePoint 용 고객 키 및 비즈니스용 OneDrive** 제공에 대 한 **자세한 정보** 를 선택 합니다. 
    
5. **제공 세부 정보** 페이지에서 **요청 만들기**를 선택 합니다.
    
6. 제공 양식에서 해당 하는 모든 정보 및 요청 된 정보를 입력 합니다. 인증을 승인할 조직의 관리자가 선택한 사항에 특별히 주의 하 여 암호화 키와 데이터의 영구 및 복구할 수 없는 소멸을 승인 해야 합니다. 양식을 완료 했으면 **제출을**선택 합니다.
    
    Microsoft에 요청을 알렸습니다 하면이 프로세스는 최대 5 영업일까지 걸릴 수 있습니다.
    
7. 아래의 필수 보존 기간 섹션을 계속 진행 합니다.
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a>필수 보존 기간을 사용 하도록 Azure 구독 등록
<a name="RegisterSubsforMRP"> </a>

루트 암호화 키의 임시 또는 영구 손실은 매우 방해가 되거나 서비스 작업에 치명적이 될 수 있으며 데이터 손실이 발생할 수 있습니다. 이러한 이유로, 고객 키와 함께 사용 되는 리소스에는 강력한 보호가 필요 합니다. 고객 키와 함께 사용 되는 모든 Azure 리소스는 기본 구성 외에도 보호 메커니즘을 제공 합니다. 즉시 및 irrevocable 취소를 방지 하는 방식으로 Azure 구독에 태그를 지정 하거나 등록할 수 있습니다. 이를 필수 보존 기간 등록 이라고 합니다. 필수 보존 기간 동안 Azure 구독을 등록 하는 데 필요한 단계에 따라 Office 365 팀과 공동 작업이 필요 합니다. 이 프로세스는 영업일 이하의 근무일까지 소요 될 수 있습니다. 이전에는이를 "취소 안 함"이 라고도 합니다.
  
Office 365 팀에 연락 하기 전에 고객 키와 함께 사용 하는 각 Azure 구독에 대해 다음 단계를 수행 해야 합니다.
  
1. Azure PowerShell을 사용 하 여 Azure 구독에 로그인 합니다. 자세한 내용은 [Azure PowerShell을 사용 하 여 로그인](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1)을 참조 하십시오.
    
2. AzureRmProviderFeature cmdlet을 실행 하 여 구독을 등록 하 고 필수 보존 기간을 사용 합니다.
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. Microsoft에 문의 하 여 해당 프로세스를 완료 합니다. SharePoint 및 비즈니스용 OneDrive 팀의 경우 [spock@microsoft.com](mailto:spock@microsoft.com)에 문의 하세요. Exchange Online 및 비즈니스용 Skype에 대 한 자세한 내용은 [exock@microsoft.com](mailto:exock@microsoft.com)에 문의 하세요. 이 프로세스를 완료 하는 데 필요한 SLA (서비스 수준 계약)는 Microsoft가 구독을 등록 하 여 필수 보존 기간을 사용 하도록 공지를 받은 경우 5 일 이내입니다. 전자 메일에 다음을 포함 합니다.
    
    **제목**: \< *테 넌 트의 정규화 된 도메인 이름* 에 대 한 고객 키\> 
    
    **Body**: 필수 보존 기간을 완료 하려는 구독 id입니다. 
    
4. Microsoft에서 등록이 완료 되었음을 알리는 알림을 받으면 다음과 같이 AzureRmProviderFeature cmdlet을 실행 하 여 등록 상태를 확인 합니다.
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. AzureRmProviderFeature cmdlet의 **등록 상태** 속성이 **등록**된 값을 반환 하는지 확인 한 후 다음 명령을 실행 하 여 프로세스를 완료 합니다.
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a>각 구독에 프리미엄 Azure 키 자격 증명 모음 만들기
<a name="CreateKeyVault"> </a>

키 자격 증명 모음을 만드는 단계는 azure [키 자격 증명 모음을 시작](https://azure.microsoft.com/documentation/articles/key-vault-get-started/)하는 과정을 안내 하는 azure PowerShell을 설치 및 시작 하 고, azure 구독에 연결 하 고, 리소스 그룹을 만들고, 해당 키 자격 증명을 만드는 방법을 설명 합니다. 리소스 그룹
  
키 자격 증명 모음을 만들 때는 SKU: Standard 또는 Premium 중 하나를 선택 해야 합니다. Standard SKU를 사용 하면 HSM (하드웨어 보안 모듈) 키 보호가 제공 되지 않으며 프리미엄 SKU는 키 자격 증명 키 보호를 위해 Hsm을 사용할 수 있습니다. 고객 키가 SKU를 사용 하는 키 보관소를 허용 하지만, Microsoft에서는 프리미엄 SKU만 사용 하는 것이 좋습니다. 두 가지 유형의 키를 사용한 작업 비용은 같으므로, 각 HSM 보호 키에 대 한 월별 비용은 비용의 차이입니다. 자세한 내용은 [키 자격 증명 모음 가격 산정](https://azure.microsoft.com/pricing/details/key-vault/) 을 참조 하세요. 
  
> [!IMPORTANT]
> 프로덕션 데이터에 대해 Premium SKU 키 보관소 및 HSM으로 보호 된 키를 사용 하 고 테스트 및 유효성 검사를 위해 Standard SKU 키 보관소와 키만 사용 합니다. 
  
고객 키를 사용 하는 각 Office 365 서비스에 대해 사용자가 만든 두 가지 Azure 구독 각각에 키 자격 증명 모음을 만듭니다. 예를 들어 Exchange Online 및 비즈니스용 Skype 전용 또는 SharePoint Online 및 비즈니스용 OneDrive 전용의 경우에는 하나의 자격 증명 모음만 만듭니다. Exchange Online 및 SharePoint Online 둘 다에 대해 고객 키를 사용 하도록 설정 하기 위해 두 쌍의 키 자격 증명 모음을 만듭니다.
  
자격 증명 모음을 연결 하는 데 사용할 DEP의 용도를 반영 하는 키 보관소에 대 한 명명 규칙을 사용 합니다. 명명 규칙 추천을 보려면 아래에서 모범 사례 섹션을 참조 하세요.
  
각 데이터 암호화 정책에 대해 쌍을 이룬 별도의 자격 증명 모음을 만듭니다. Exchange Online의 경우 사서함에 정책을 할당할 때 사용자가 데이터 암호화 정책의 범위를 선택 합니다. 사서함에는 정책이 하나만 할당 될 수 있으며 최대 50 개의 정책을 만들 수 있습니다. SharePoint Online의 경우 정책의 범위는 지리적 위치 또는 지리적으로 조직 내의 모든 데이터입니다.
  
또한 키 보관소에는 저장소 용량 (매우 작음)과 키 보관소 로깅이 필요 하기 때문에 (키 보관소를 만드는 경우) 저장 된 데이터도 생성 해야 하므로 Azure 리소스 그룹을 만들어야 합니다. Microsoft는 별도의 관리자를 사용 하 여 각 리소스 그룹을 관리할 것을 권장 하 고, 관리를 모든 관련 고객 키 리소스를 관리 하는 관리자 집합과 맞추고 있습니다.
  
> [!IMPORTANT]
> 가용성을 최대화 하려면 키 보관소가 Office 365 서비스에 가까운 지역에 있어야 합니다. 예를 들어 Exchange Online 조직이 북미에 있는 경우 북미에 키 자격 증명 모음을 배치 합니다. Exchange Online 조직이 유럽에 있는 경우 키 보관소를 유럽에 배치 합니다.<br/>키 자격 증명에 대 한 공통 접두사를 사용 하 고, 키 보관소와 키의 사용 및 범위 약어를 포함 하 고 (예: 해당 보관소가 북미에 있는 Contoso SharePoint 서비스의 경우) 가능한 이름 쌍은 Contoso-O365SP-VaultA1 및 Contoso-O365SP-VaultA2. 자격 증명 이름은 Azure 내의 전역적으로 고유한 문자열이 되므로 필요한 이름이 다른 Azure 고객의 요청을 받아야 하는 경우에 대비 하 여 원하는 이름의 변형을 시도해 야 할 수 있습니다. 7 월 2017 볼트 이름은 변경할 수 없으므로 설정 계획을 수립 하 고 두 번째 사용자를 사용 하 여 계획이 올바르게 실행 되는지 확인 하는 것이 좋습니다.<br/>가능 하면 페어링되지 않은 지역에 자격 증명 모음을 만듭니다. 쌍을 이룬 Azure 지역에서 서비스 장애 도메인 별로 고가용성을 제공 합니다. 따라서 지역 쌍을 서로의 백업 지역으로 간주할 수 있습니다. 즉, 한 지역에 배치 된 Azure 리소스가 연결 된 지역을 통과 하는 내결함성을 자동으로 획득 합니다. 이러한 이유 때문에 지역이 쌍을 이루는 DEP에서 사용 되는 두 개의 자격 증명 영역을 선택 하면 사용 가능한 영역의 총 두 영역만 사용할 수 있습니다. 대부분의 지역에는 두 지역이 있으므로 아직 연결 되지 않은 영역을 선택할 수는 없습니다. 가능한 경우 DEP와 함께 사용 되는 두 개의 보관소에 대해 쌍이 없는 두 개의 영역을 선택 합니다. 이는 가용성의 총 4 지역에서 혜택을 제공 합니다. 자세한 내용은 [Business 연속성 및 재해 복구 (BCDR):](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) 현재 지역 쌍 목록의 Azure 연결 된 지역을 참조 하세요. 
  
### <a name="assign-permissions-to-each-key-vault"></a>각 키 자격 증명 모음에 사용 권한 할당
<a name="KeyVaultPerms"> </a>

각 키 보관소에 대해 구현에 따라 고객 키에 대해 세 가지 개별 사용 권한 집합을 정의 해야 합니다. 예를 들어 다음 각 항목에 대해 하나의 권한 집합을 정의 해야 합니다.
  
- 조직에 대 한 주요 자격 증명 모음을 일상적인 관리 하는 데 사용할 수 있는 **주요 자격 증명 모음 관리자** 이러한 작업에는 백업, 만들기, 가져오기, 가져오기, 목록, 복원 등이 있습니다. 
    
    > [!IMPORTANT]
    > 키 자격 증명 모음 관리자에 게 할당 된 사용 권한 집합에는 키를 삭제할 수 있는 권한이 포함 되어 있지 않습니다. 이는 의도적인 것이 고 중요 한 방법입니다. 일반적으로 암호화 키 삭제는 데이터를 영구적으로 소멸 하기 때문에 수행 되지 않습니다. 주요 자격 증명 모음 관리자에 게 기본적으로이 사용 권한을 부여 하지 않는 것이 좋습니다. 대신 주요 자격 증명 참가자에 대해이를 예약 하 고, 결과에 대 한 확실 한 이해가 이해 되 면 짧은 기간 동안 관리자 에게만 할당 합니다. 
  
    Office 365 조직의 사용자에 게 이러한 권한을 할당 하려면 Azure PowerShell을 사용 하 여 Azure 구독에 로그인 합니다. 자세한 내용은 [Azure PowerShell을 사용 하 여 로그인](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1)을 참조 하십시오.
    
- AzureRmKeyVaultAccessPolicy cmdlet을 실행 하 여 필요한 권한을 할당 합니다.
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  예를 들면 다음과 같습니다.
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- Azure 키 자격 증명 모음 자체에 대 한 사용 권한을 변경할 수 있는 **키 보관소 참가자** 직원은 팀에 탈퇴 하거나 참가할 때 이러한 권한을 변경 해야 하며, 키 보관소 관리자가 키를 삭제 하거나 복원 하는 데 필요한 권한을 갖는 것이 아주 드문 경우입니다. 이 키 보관소 참가자 집합에는 해당 키 자격 증명 모음에 대 한 **참가자** 역할이 부여 되어야 합니다. Azure Resource Manager를 사용 하 여이 역할을 할당할 수 있습니다. 자세한 단계는 [역할 기반 액세스 제어를 사용 하 여 Azure 구독 리소스에 대 한 액세스를 관리 하](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure)는 방법을 참조 하세요. 구독을 만드는 관리자는이 액세스 권한 뿐만 아니라 다른 관리자에 게 참가자 역할을 할당할 수 있는 권한도 제공 됩니다.
    
- Exchange Online 및 비즈니스용 Skype와 함께 고객 키를 사용 하려는 경우에는 Office 365에 대 한 권한을 부여 하 여 Exchange Online 및 비즈니스용 Skype를 대신 하 여 키 자격 증명 모음을 사용 해야 합니다. 마찬가지로, SharePoint Online 및 비즈니스용 OneDrive에서 고객 키를 사용 하려는 경우에는 Office 365에 대 한 권한을 추가 하 여 SharePoint Online 및 비즈니스용 OneDrive를 대신 하 여 키 자격 증명 모음을 사용 해야 합니다. Office 365에 대 한 사용 권한을 부여 하려면 다음 구문을 사용 하 여 **AzureRmKeyVaultAccessPolicy** cmdlet을 실행 합니다. 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    여기서 각 부분이 나타내는 의미는 다음과 같습니다.
    
  - *vaultname* 은 만든 키 보관소의 이름입니다. 
    
  - Exchange Online 및 비즈니스용 Skype의 경우 *Office 365 appID* 를 다음으로 바꾸기`00000002-0000-0ff1-ce00-000000000000`
    
  - SharePoint Online 및 비즈니스용 OneDrive의 경우 *Office 365 appID* 를 다음으로 바꾸기`00000003-0000-0ff1-ce00-000000000000`
    
  예: Exchange Online 및 비즈니스용 Skype에 대 한 사용 권한 설정:
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  예: SharePoint Online 및 비즈니스용 OneDrive에 대 한 사용 권한 설정
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a>키 자격 증명 모음에서 일시 삭제를 사용 하도록 설정 하 고 확인
<a name="SoftDelete"> </a>

키를 신속 하 게 복구할 수 있으면 실수로 또는 악의적으로 삭제 된 키로 인해 확장 서비스 중단을 경험할 가능성이 줄어듭니다. 사용자 키에 키를 사용할 수 있으려면 먼저 소프트 삭제 라고 하는이 구성을 사용 하도록 설정 해야 합니다. 소프트 삭제를 사용 하도록 설정 하면 백업에서 복원 하지 않고도 90 일 내에 키 또는 자격 증명 모음을 복구할 수 있습니다.
  
키 자격 증명 모음에서 일시 삭제를 사용 하도록 설정 하려면 다음 단계를 완료 합니다.
  
1. Windows Powershell을 사용 하 여 Azure 구독에 로그인 합니다. 자세한 내용은 [Azure PowerShell을 사용 하 여 로그인](https://docs.microsoft.com/powershell/azure/authenticate-azureps)을 참조 하십시오.
    
2. [AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) cmdlet을 실행 합니다. 이 예에서 *vaultname* 은 소프트 삭제를 활성화할 수 있는 키 보관소의 이름입니다. 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. **AzureRmKeyVault** cmdlet을 실행 하 여 키 자격 증명 모음에 대해 소프트 삭제가 구성 되었는지 확인 합니다. 키 자격 증명 모음에 대해 소프트 삭제가 올바르게 구성 된 경우 소프트 삭제를 사용할 수 있나요? 속성은 **True**값을 반환 합니다. 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a>키를 만들거나 가져오는 방법으로 각 키 보관소에 키를 추가 합니다.
<a name="AddKeystoKeyVault"> </a>

Azure 키 보관소에는 두 가지 방법으로 키를 추가할 수 있습니다. 키 보관소에 직접 키를 만들거나 키를 가져올 수 있습니다. 키 보관소에서 직접 키를 만드는 것은 다소 복잡 한 방법 이지만 키를 가져오면 키가 생성 되는 방식을 보다 강력 하 게 제어할 수 있습니다.
  
키 보관소에 직접 키를 만들려면 다음과 같이 [AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) cmdlet을 실행 합니다. 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

여기서 각 부분이 나타내는 의미는 다음과 같습니다.
  
-  *vaultname* 은 키를 만들 키 자격 증명 모음의 이름입니다. 
    
-  *keyname* 은 새 키에 지정할 이름입니다. 
    
    > [!TIP]
    > 키 보관소에 대해 위에서 설명한 유사 명명 규칙을 사용 하 여 이름 키 이러한 방식으로 키 이름만 표시 되는 도구에서 문자열은 자체 설명입니다. 
  
- HSM을 사용 하 여 키를 보호 하려면 _대상_ 매개 변수의 값으로 **HSM** 을 지정 하 고, 그렇지 않으면 **소프트웨어**를 지정 해야 합니다.
    
For example,
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

키 보관소로 바로 키를 가져오려면 Thales nShield 하드웨어 보안 모듈이 있어야 합니다.
  
일부 조직에서는이 방법을 선호 하 여 키의 provenance을 설정 하 고,이 방법 역시 다음을 제공 합니다.
  
- 가져오기에 사용 되는 도구 집합에는 Thales에서 생성 한 키를 암호화 하는 데 사용 되는 KEK (키 교환 키)가 내보낼 수 없으며 Thales에서 제조한 정품 HSM 내에서 생성 된다는 것이 포함 되어 있습니다.
    
- 도구 집합에는 Thales에서 제조한 정품 HSM에도 Azure 키 자격 증명 모음 보안 세계가 생성 된 Thales의 증명이 포함 되어 있습니다. 이 증명은 Microsoft가 정품 Thales 하드웨어를 사용 하 고 있음을 증명 합니다.
    
보안 그룹을 확인 하 여 위의 attestations 필요한 지 확인 합니다. 온-프레미스 키를 만들고 키 보관소로 가져오는 자세한 단계 [는 Azure Key vault에 대해 HSM 보호 키를 생성 하 고 전송 하는 방법을](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/)참조 하세요. Azure 지침을 사용 하 여 각 키 자격 증명 모음에 키를 만듭니다.
  
### <a name="check-the-recovery-level-of-your-keys"></a>키의 복구 수준 확인
<a name="CheckKeyRecoveryLevel"> </a>

Office 365을 사용 하려면 Azure 키 자격 증명 모음 구독이 취소 되지 않도록 설정 되 고, 고객 키에 사용 되는 키에 소프트 삭제가 사용 되도록 되어 있어야 합니다. 키의 복구 수준을 확인 하 여이를 확인할 수 있습니다.
  
키의 복구 수준을 확인 하려면 Azure PowerShell에서 다음과 같이 AzureKeyVaultKey cmdlet을 실행 합니다.
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

_복구 수준_ 속성에서 복구 **가능한 + ProtectedSubscription**값이 아닌 다른 항목을 반환 하는 경우에는이 항목을 검토 하 여 구독을 취소 하지 않음 목록에 추가 하는 모든 단계를 따랐는지 확인 해야 합니다. 각 키 보관소에 소프트 삭제를 사용 하도록 설정 되어 있는지 여부
  
### <a name="backup-azure-key-vault"></a>Azure 키 자격 증명 모음 백업
<a name="BackupAzureKeyVaultkeys"> </a>

키를 만들거나 변경 하는 즉시 백업 및 오프 라인 복사본을 백업 및 저장 합니다. 오프 라인 복사본은 실제 안전 또는 상업적 저장소 기능과 같은 네트워크에 연결 해서는 안 됩니다. 재해 발생 시 액세스할 수 있는 위치에 백업 복사본을 하나 이상 저장 해야 합니다. 백업 blob은 키 자료를 복원 하는 유일한 방법으로 키 자격 증명 키를 영구적으로 제거 하거나 작동 하지 않는 방식으로 렌더링 해야 합니다. Azure 키 자격 증명 모음에 대 한 외부 키를 가져오고 Azure 키 보관소로 가져온 키는 해당 키를 사용 하는 데 필요한 메타 데이터가 외부 키가 없기 때문에 백업으로 한정 되지 않습니다. Azure Key Vault에서 가져온 백업만 고객 키를 사용한 복원 작업에 사용할 수 있습니다. 따라서 키가 업로드 되거나 생성 되 면 Azure 키 자격 증명 모음을 백업 하는 것이 중요 합니다.
  
Azure 키 자격 증명 키의 백업을 만들려면 다음과 같이 [AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) cmdlet을 실행 합니다.
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

출력 파일이 접미사 `.backup`를 사용 하는지 확인 합니다.
  
이 cmdlet에서 생성 된 출력 파일은 암호화 되며 Azure 키 자격 증명 모음 외부에서 사용할 수 없습니다. 백업은 백업을 수행한 Azure 구독에만 복원할 수 있습니다.
  
> [!TIP]
> 출력 파일의 경우 자격 증명 모음 이름 및 키 이름을 조합 하 여 선택 합니다. 이렇게 하면 파일 이름이 자체 설명 됩니다. 또한 백업 파일 이름이 충돌 하지 않도록 해야 합니다. 
  
예를 들면 다음과 같습니다.
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a>Azure 키 자격 증명 모음 구성 설정 확인
<a name="Validateconfiguration"> </a>

DEP에서 키를 사용 하기 전에 유효성 검사를 수행 하는 것은 선택 사항 이지만 가급적 권장 됩니다. 특히이 항목에서 설명 하는 것과 다른 키 및 보관소를 설정 하는 단계를 사용 하는 경우에는 고객 키를 구성 하기 전에 Azure Key Vault 리소스의 상태를 확인 해야 합니다.
  
키가 get, wrapKey 및 unwrapKey 작업을 사용 하도록 설정 되었는지 확인 하려면 다음을 수행 합니다.
  
다음과 같이 [AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) cmdlet을 실행 합니다. 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

출력에서 액세스 정책 및 Exchange Online id (guid) 또는 SharePoint Online id (GUID)를 적절 하 게 찾습니다. 위의 세 가지 사용 권한 중 일부는 키 사용 권한 아래에 표시 되어야 합니다.
  
액세스 정책 구성이 올바르지 않으면 다음과 같이 AzureRmKeyVaultAccessPolicy cmdlet을 실행 합니다.
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

예를 들어 Exchange Online 및 비즈니스용 Skype의 경우:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

예를 들어 SharePoint Online 및 비즈니스용 OneDrive:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

키에 대해 만료 날짜가 설정 되지 않았는지 확인 하려면 다음과 같이 [AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) cmdlet을 실행 합니다. 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

만료 된 키는 고객 키에서 사용할 수 없으며 만료 된 키로 시도한 작업은 실패 하 고 서비스 중단으로 인해 발생할 수도 있습니다. 고객 키와 함께 사용 되는 키에는 만료 날짜가 없을 것을 적극 권장 합니다. 만료 날짜를 설정한 후에는 제거할 수 없지만 다른 날짜로 변경할 수는 있습니다. 만료 날짜가 설정 된 키를 사용 해야 하는 경우 만료 값을 12/31/9999로 변경 합니다. 만료 날짜가 12/31/9999 이외의 날짜로 설정 된 키는 Office 365 유효성 검사를 통과 하지 못합니다.
  
12/31/9999 이외의 값으로 설정 된 만료 날짜를 변경 하려면 다음과 같이 [AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) cmdlet을 실행 합니다. 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> 고객 키와 함께 사용 하는 암호화 키에 대해 만료 날짜를 설정 하지 마십시오. 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a>각 Azure Key Vault 키에 대 한 URI 가져오기
<a name="GetKeyURI"> </a>

Azure의 모든 단계를 완료 하 여 키 자격 증명 모음을 설정 하 고 키를 추가한 후에는 다음 명령을 실행 하 여 각 키 자격 증명 모음에서 키에 대 한 URI를 가져옵니다. 나중에 각 DEP를 만들고 할당할 때 이러한 Uri를 사용 해야 하므로이 정보를 안전한 장소에 저장 합니다. 각 키 자격 증명 모음에 대해 한 번씩이 명령을 실행 해야 합니다.
  
Azure PowerShell:
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a>Office 365: Exchange Online 및 비즈니스용 Skype에 대 한 고객 키 설정
<a name="AzureSteps"> </a>

시작 하기 전에 Azure 키 자격 증명 모음을 설정 하는 데 필요한 작업을 완료 했는지 확인 합니다. 자세한 내용은 [Azure Key Vault의 전체 작업 및 Microsoft FastTrack For Customer key](controlling-your-data-using-customer-key.md#AzureSteps) 를 참조 하세요. 
  
Exchange Online 및 비즈니스용 Skype에 대 한 고객 키를 설정 하려면 Windows PowerShell을 사용 하 여 Exchange Online에 원격으로 연결 하 여 다음 단계를 수행 해야 합니다.
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a>Exchange Online 및 비즈니스용 Skype에서 사용 하기 위한 DEP (데이터 암호화 정책) 만들기
<a name="CreateDEP4EXOSkype"> </a>

DEP는 Azure Key Vault에 저장 된 키 집합과 연결 됩니다. Office 365에서 사서함에 DEP를 할당 합니다. 그런 다음 Office 365에서는 정책에 식별 된 키를 사용 하 여 사서함을 암호화 합니다. DEP를 만들려면 이전에 가져온 키 보관소 Uri가 필요 합니다. 지침은 [각 Azure 키 자격 증명 모음 키의 URI 가져오기를](controlling-your-data-using-customer-key.md#GetKeyURI) 참조 하세요. 
  
항상! DEP를 만들 때 서로 다른 두 Azure 키 자격 증명 모음에 있는 두 개의 키를 지정 합니다. 이러한 키가 지리적 중복을 보장 하기 위해 별도의 두 Azure 지역에 위치 하는지 확인 합니다.
  
DEP를 만들려면 다음 단계를 수행 합니다.
  
1. 로컬 컴퓨터에서 Office 365 조직에 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 여 Windows PowerShell을 열고 다음 명령을 실행 하 여 [Exchange Online PowerShell에 연결](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) 합니다. 
    
   ```
   $UserCredential = Get-Credential
   ```

2. Windows PowerShell 자격 증명 요청 대화 상자에서 회사 또는 학교 계정 정보를 입력 하 고 **확인**을 클릭 한 후에 다음 명령을 입력 합니다. 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. 다음 명령을 실행합니다.
    
   ```
   Import-PSSession $Session
   ```

4. DEP를 만들려면 다음 명령을 입력 하 여 새-DataEncryptionPolicy cmdlet을 사용 합니다.
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   여기서 각 부분이 나타내는 의미는 다음과 같습니다.
    
   -  *PolicyName* 는 정책에 사용 하려는 이름입니다. 이름에 공백을 포함할 수 없습니다. 예: USA_mailboxes. 
    
   -  *Policydescription* 은 정책에 대 한 정보를 파악 하는 데 도움이 되는 정책에 대 한 사용자 친숙 한 설명입니다. 설명에 공백을 포함할 수 있습니다. 예를 들어 미국 및 지역의 사서함에 대 한 루트 키를 예로 들 있습니다. 
    
   -  *KeyVaultURI1* 는 정책의 첫 번째 키에 대 한 URI입니다. 예를 들면 https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01와 같습니다. 
    
   -  *KeyVaultURI2* 은 정책의 두 번째 키에 대 한 URI입니다. 예를 들면 https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02와 같습니다. 두 Uri를 쉼표와 공백으로 구분 합니다. 
    
   예제:
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a>사서함에 DEP 할당
<a name="assignDEPtomailbox"> </a>

사서함 cmdlet을 사용 하 여 사서함에 DEP를 할당 합니다. 정책을 할당 하 고 나면 Office 365에서 DEP에 지정 된 키를 사용 하 여 사서함을 암호화할 수 있습니다.
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

여기서 *MailboxIdParameter* 는 사서함을 지정 합니다. 사서함 cmdlet에 대 한 자세한 내용은 [set-mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx)를 참조 하십시오.
  
### <a name="validate-mailbox-encryption"></a>사서함 암호화 유효성 검사
<a name="validatemailboxencryption"> </a>

사서함을 암호화 하는 데 다소 시간이 걸릴 수 있습니다. 처음 정책 할당의 경우에는 서비스에서 사서함을 암호화 하기 전에 사서함에서 다른 데이터베이스로의 이동도 완료 해야 합니다. DEP를 변경한 후 또는 사서함에 DEP를 처음 할당할 때 암호화 유효성 검사를 시도 하기 전에 72 시간을 기다리는 것이 좋습니다.
  
Get-mailboxstatistics cmdlet을 사용 하 여 사서함이 암호화 되어 있는지 여부를 확인할 수 있습니다.
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

사서함이 암호화 된 경우 IsEncrypted 속성은 **true** 값을 반환 하 고 사서함이 암호화 되지 않은 경우에는 **false** 로 설정 합니다. 

사서함 이동을 완료 하는 데 걸리는 시간은 처음에 DEP를 할당 하는 사서함 수와 사서함 크기에 따라 달라 집니다. 사서함이 DEP를 할당 한 시간 이후로 암호화 되지 않은 경우 New-moverequest cmdlet을 사용 하 여 암호화 되지 않은 사서함에 대 한 사서함 이동을 시작 합니다.

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a>Office 365: SharePoint Online 및 비즈니스용 OneDrive에 대 한 고객 키 설정
<a name="AzureSteps"> </a>

시작 하기 전에 Azure 키 자격 증명 모음을 설정 하는 데 필요한 작업을 완료 했는지 확인 합니다. 자세한 내용은 [Azure Key Vault의 전체 작업 및 Microsoft FastTrack For Customer key](controlling-your-data-using-customer-key.md#AzureSteps) 를 참조 하세요. 
  
SharePoint Online 및 비즈니스용 OneDrive에 대 한 고객 키를 설정 하려면 Windows PowerShell을 사용 하 여 SharePoint Online에 원격으로 연결 하 여 다음 단계를 수행 해야 합니다.
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a>각 SharePoint Online 및 비즈니스용 OneDrive 지역에 대 한 DEP (데이터 암호화 정책)를 만듭니다.
<a name="CreateDEP4SPOODfB"> </a>

DEP는 Azure Key Vault에 저장 된 키 집합과 연결 됩니다. 한 지리적 위치에 있는 모든 데이터에 DEP를 적용 합니다 (geo 라고도 함). Office 365 (현재 미리 보기)의 다중 지역 기능을 사용 하는 경우에는 각 지역에 따라 하나의 DEP를 만들 수 있습니다. 다중 geo를 사용 하지 않는 경우에는 SharePoint Online 및 비즈니스용 OneDrive와 함께 사용 하기 위해 Office 365에서 DEP를 하나씩 만들 수 있습니다. 그러면 Office 365에서 DEP에 식별 된 키를 사용 하 여 해당 지역에서 데이터를 암호화 합니다. DEP를 만들려면 이전에 가져온 키 보관소 Uri가 필요 합니다. 지침은 [각 Azure 키 자격 증명 모음 키의 URI 가져오기를](controlling-your-data-using-customer-key.md#GetKeyURI) 참조 하세요. 
  
항상! DEP를 만들 때 서로 다른 두 Azure 키 자격 증명 모음에 있는 두 개의 키를 지정 합니다. 이러한 키가 지리적 중복을 보장 하기 위해 별도의 두 Azure 지역에 위치 하는지 확인 합니다.
  
DEP를 만들려면 Windows PowerShell을 사용 하 여 SharePoint Online에 원격으로 연결 해야 합니다.
  
1. 로컬 컴퓨터에서 Office 365 조직에 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 여 [SharePoint Online Powershell에 연결](https://technet.microsoft.com/library/fp161372.aspx)합니다.
    
2. Microsoft SharePoint Online 관리 셸에서 다음과 같이 [SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) cmdlet을 실행 합니다. 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   DEP를 등록 하면 geo의 데이터에 대 한 암호화가 시작 됩니다. 이 작업은 다소 시간이 걸릴 수 있습니다.
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a>그룹 사이트, 팀 사이트 및 비즈니스용 OneDrive의 암호화 확인
<a name="validateencryptionSPO"> </a>

다음과 같이 SPODataEncryptionPolicy cmdlet을 실행 하 여 암호화 상태를 확인할 수 있습니다.
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

이 cmdlet의 출력은 다음과 같습니다.
  
- 기본 키의 URI입니다.
    
- 보조 키의 URI입니다.
    
- Geo의 암호화 상태입니다. 가능한 상태는 다음과 같습니다.
    
  - **등록 취소 됨:** 고객 키 암호화가 아직 적용 되지 않았습니다. 
    
  - **등록:** 고객 키 암호화가 적용 되었으며 파일을 암호화 하 고 있습니다. Geo가이 상태에 있는 경우에는 지리적으로 완료 되는 사이트 비율에 대 한 정보도 함께 확인 하 여 암호화 진행 상태를 모니터링할 수 있습니다. 
    
  - **등록 된 경우:** 고객 키 암호화가 적용 되었으며 모든 사이트의 모든 파일이 암호화 되었습니다. 
    
  - **롤링:** 키 롤이 진행 중입니다. Geo가이 상태 이면 진행 상태를 모니터링할 수 있도록 키 롤 작업을 완료 한 사이트 비율에 대 한 정보도 함께 표시 됩니다. 
    
## <a name="managing-customer-key-for-office-365"></a>Office 365에 대 한 고객 키 관리
<a name="ManageCustomerKey"> </a>

Office 365에 대 한 고객 키를 설정한 후에는 다음 추가 관리 작업을 수행할 수 있습니다.
  
- [Azure 키 자격 증명 모음 키 복원](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [고객 키와 함께 사용 하는 Azure 키 보관소에서 키 롤링 또는 회전](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [키 보관소 사용 권한 관리](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [사서함에 할당 된 DEP 확인](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a>Azure 키 자격 증명 모음 키 복원
<a name="RestoreAzureKeyVaultKeys"> </a>

복원을 수행 하기 전에 일시 삭제로 제공 되는 복구 기능을 사용 합니다. 사용자 키와 함께 사용 되는 모든 키는 소프트 삭제를 사용 하도록 설정 해야 합니다. 일시 삭제는 휴지통 처럼 작동 하며 복원할 필요 없이 최대 90 일 동안 복구를 허용 합니다. 복구는 키 또는 키 보관소가 손실 된 경우와 같이 극단적인 상황 또는 예외적인 경우에만 필요 합니다. 고객 키와 함께 사용 하기 위해 키를 복원 해야 하는 경우 Azure PowerShell에서 다음과 같이 AzureKeyVaultKey cmdlet을 실행 합니다.
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

예를 들면 다음과 같습니다.
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

키 보관소에 같은 이름의 키가 이미 있으면 복원 작업을 수행할 수 없습니다. AzureKeyVaultKey는 키 이름을 포함 하 여 키에 대 한 모든 키 버전 및 메타 데이터를 복원 합니다.
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a>고객 키와 함께 사용 하는 Azure 키 보관소에서 키 롤링 또는 회전
<a name="RollCKkey"> </a>

Azure 키 자격 증명 모음 또는 고객 키에 따라 롤링 키가 필요 하지는 않습니다. 또한 HSM을 사용 하 여 보호 되는 키의 경우 사실상 손상을 불가능해 집니다. 루트 키가 악의적인 행위자가 소유 하 고 있는 경우에도 Office 365 코드 에서만 사용 하는 방법을 아는 것이 좋습니다. 그러나 키를 롤백하는 것은 고객 키를 통해 지원 됩니다.
  
> [!CAUTION]
> 명확한 기술 이유가 있는 경우 고객 키와 함께 사용 하는 암호화 키를 롤백하거나 키를 롤 포워드 해야 하는 규정 준수 요구 사항을 명시 해야 합니다. 또한 정책과 연결 된 키를 삭제 하지 마십시오. 키를 롤포워드할 때 이전 키로 암호화 된 콘텐츠가 제공 됩니다. 예를 들어 활성 사서함은 자주 다시 암호화 되 고 비활성, 연결 해제 및 사용 하지 않도록 설정 된 사서함은 여전히 이전 키를 사용 하 여 암호화 될 수 있습니다. SharePoint Online은 복원 및 복구를 위해 콘텐츠 백업을 수행 하므로 이전 키를 사용 하 여 계속 콘텐츠를 보관할 수 있습니다. <br/> 데이터의 안전을 보장 하기 위해 SharePoint Online은 한 번에 두 개 이상의 키 롤 작업을 진행 하는 것을 허용 하지 않습니다. 키 자격 증명 모음의 두 키를 롤 포워드 하려면 첫 번째 키 롤 작업이 완전히 완료 될 때까지 기다려야 합니다. 여기서는 키 롤업 작업을 다른 간격으로 엇갈리게 배치 하 여 문제가 되지 않도록 하는 것이 좋습니다. 
  
키를 롤 포워드 하면 기존 키의 새 버전을 요청 하 게 됩니다. 기존 키의 새 버전을 요청 하려면 첫 번째 위치에서 키를 만드는 데 사용한 구문과 동일한 cmdlet, [AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey)을 사용 합니다.
  
예를 들면 다음과 같습니다.
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

이 예에서는 contoso **-O365EX-VaultA1-Key001** 이라는 키가 **contoso-O365EX-VaultA1** 자격 증명 모음에 이미 있으므로 새 키 버전이 생성 됩니다. 이 작업을 수행 하면 새 키 버전이 추가 됩니다. 이 작업은 키의 버전 기록에서 이전 키 버전을 유지 하므로 이전에 해당 키로 암호화 된 데이터의 암호를 해독할 수 있습니다. DEP와 연결 된 키를 모두 만들었으면 추가 cmdlet을 실행 하 여 고객 키가 새 키를 사용 하 여 시작 되도록 해야 합니다. 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a>Azure 키 자격 증명 모음에서 키를 롤백하거나 회전 한 후에 Exchange Online 및 비즈니스용 Skype에서 새 키를 사용 하도록 설정

Exchange Online 및 비즈니스용 Skype와 함께 사용 되는 DEP와 연결 된 Azure 키 자격 증명 키 중 하나를 롤 포워드 하려면 다음 명령을 실행 하 여 DEP를 업데이트 하 고 Office 365에서 새 키를 사용 하 여 시작 해야 합니다.
  
Office 365에서 사서함을 암호화 하기 위해 새 키를 사용 하도록 고객 키에 지시 하려면 다음과 같이 Set-DataEncryptionPolicy cmdlet을 실행 합니다.
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

48 시간 이내에이 정책을 사용 하 여 암호화 된 활성 사서함은 업데이트 된 키와 연결 됩니다. [사서함에 할당 된 DEP 결정](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) 의 단계를 사용 하 여 사서함의 DataEncryptionPolicyID 속성 값을 확인 합니다. 이 속성의 값은 업데이트 된 키가 적용 된 후에 변경 됩니다. 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a>Azure 키 자격 증명 모음에서 키를 롤백하거나 회전 한 후에 SharePoint Online 및 비즈니스용 OneDrive에서 새 키를 사용 하도록 설정

SharePoint Online 및 비즈니스용 OneDrive와 함께 사용 되는 DEP와 연결 된 Azure Key 자격 증명 키 중 하나를 롤 포워드 하려면 [SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) cmdlet을 실행 하 여 DEP를 업데이트 하 고 Office 365에서 새 키를 사용 하 여 시작 해야 합니다. 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

이렇게 하면 SharePoint Online 및 비즈니스용 OneDrive에 대 한 키 롤 작업이 시작 됩니다. 이 작업은 즉시 수행 되지 않습니다. 키 롤 작업의 진행률을 확인 하려면 다음과 같이 SPODataEncryptionPolicy cmdlet을 실행 합니다.
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a>키 보관소 사용 권한 관리
<a name="Managekeyvaultperms"> </a>

키 보관소 권한을 확인 하 고 제거 하는 데 사용할 수 있는 몇 가지 cmdlet이 제공 됩니다. 예를 들어 직원이 팀을 떠날 때 사용 권한을 제거 해야 할 수 있습니다.
  
키 보관소 권한을 확인 하려면 AzureRmKeyVault cmdlet을 실행 합니다.
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

예를 들면 다음과 같습니다.
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

관리자의 사용 권한을 제거 하려면 AzureRmKeyVaultAccessPolicy cmdlet을 실행 합니다.
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

예를 들면 다음과 같습니다.
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a>사서함에 할당 된 DEP 확인
<a name="DeterminemailboxDEP"> </a>

사서함에 할당 된 DEP를 확인 하려면 Get-mailboxstatistics cmdlet을 사용 합니다. Cmdlet은 고유 식별자 (GUID)를 반환 합니다.
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

여기서 *GeneralMailboxOrMailUserIdParameter* 는 사서함을 지정 합니다. Get-mailboxstatistics cmdlet에 대 한 자세한 내용은 [get-get-mailboxstatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx)을 참조 하십시오.
  
GUID를 사용 하 여 다음 cmdlet을 실행 하 여 사서함이 할당 된 DEP의 대화명을 확인할 수 있습니다.
  
```
Get-DataEncryptionPolicy <GUID>
```

여기서 *GUID* 는 이전 단계의 get-mailboxstatistics cmdlet에서 반환 하는 guid입니다. 
  

