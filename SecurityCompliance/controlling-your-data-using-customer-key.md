---
title: 고객 키를 사용하여 Office 365에서 데이터 제어
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/1/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
description: 고객 키에 대 한 설정 Office 365 개발자를 위한 Exchange Online, Skype 비즈니스, SharePoint Online 및 비즈니스용 OneDrive에 대 한 하는 방법에 알아봅니다. 고객 키를 사용 하 컨트롤 조직의 암호화 키 및 Microsoft의 데이터 센터의 나머지 부분에서 데이터를 암호화 하 고 사용 하 여 Office 365를 구성 합니다.
ms.openlocfilehash: 3eeccd03b89aa5a79ceba536d3f13c7a881b6ca7
ms.sourcegitcommit: ef0bb05a0cf7974ae5083c7551ce3fe4ab7a9544
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/13/2018
ms.locfileid: "23965612"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a>고객 키를 사용하여 Office 365에서 데이터 제어

고객 키를 사용 하 컨트롤 조직의 암호화 키 및 Microsoft의 데이터 센터의 나머지 부분에서 데이터를 암호화 하 고 사용 하 여 Office 365를 구성 합니다. 보관 된 데이터에는 Exchange Online 및 사서함 및 SharePoint Online에 저장 된 파일에 저장 된 비즈니스를 위한 Skype 및 비즈니스용 OneDrive에서 데이터를 포함 합니다.
  
Office 365에 대 한 고객 키를 사용 하려면 먼저 Azure를 설정 해야 합니다. 이 항목을 만들고 필요한 Azure 리소스를 구성 하기 위해 수행 해야하는 단계를 설명 하 고 Office 365의 고객 키를 설정 하기 위한 단계를 제공 합니다. Azure 설치를 완료 한 후 어떤 정책 및 따라서 사서함과 조직의 파일에 할당 하는 키를 결정 합니다. 사서함 및 파일을 정책을 할당 하지 않은 제어 하 고 Microsoft가 관리 하는 암호화 정책을 사용 합니다. 고객 키에 대 한 자세한 내용은 또는 일반 개요에 대 한 [Office 365 FAQ에 대 한 고객 키](service-encryption-with-customer-key-faq.md)를 참조 하십시오.
  
> [!IMPORTANT]
> 이 항목의 모범 사례를 따르는 것이 좋습니다. 이러한 이라고 **팁** 및 **중요**합니다. 고객 키 사용 해당 범위 수 만큼 클 전체 조직 루트 암호화 키를 제어할 수 있습니다. 즉, 이러한 키를 사용 하 여 실수 광범위 한 영향을 줄 수 및 서비스 중단 또는 취소할 데이터 손실 될 수 있습니다. 
  
## <a name="before-you-begin-setting-up-customer-key"></a>고객 키를 설정 하기 전에
<a name="Beforeyoustart"> </a>

시작 하기 전에 조직에 대 한 적절 한 라이선스를 포함 해야 합니다. Office 365의 고객 키 Office 365 e 5 또는 고급 준수 SKU에서 제공 됩니다.
  
그런 다음, 개념 및이 항목의 절차를 이해 하려면 [Azure 키 추적용](https://azure.microsoft.com/en-us/documentation/services/key-vault/) 설명서를 검토 해야 합니다. 또한 Azure, [테 넌 트](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant)예에 사용 되는 용어에 익숙한 수 없습니다.
  
고객 키로 이동한 다음 설명서를 포함 하 여에 의견을 제공 하려면 customerkeyfeedback@microsoft.com를 아이디어, 제안 및 측면을 보냅니다.
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a>Office 365에 대 한 고객 키를 설정 하는 개요 (영문)
<a name="Overview"> </a>

고객 키를 설정 하려면 이러한 작업을 수행 합니다. 이 항목의 나머지 부분 각 작업 또는 프로세스의 각 단계에 대 한 자세한 내용은 아웃 링크에 대 한 자세한 지침을 제공 합니다.
  
**Azure 및 Microsoft FastTrack:**
  
Azure PowerShell 원격으로 연결 하 여 대부분의 이러한 작업을 완료 합니다. Azure PowerShell의 나중에 또는 최상의 결과 4.4.0 버전을 사용 합니다.
  
- [두 새로운 Azure 구독 만들기](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [필수 보존 기간을 사용 하 여 Azure 구독을 등록 합니다.](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    1 ~ 5 일 이내 등록 걸릴 수 있습니다.
    
- [Office 365에 대 한 고객 키를 정품 인증을 요청을 제출](controlling-your-data-using-customer-key.md#FastTrack)
    
    두 새로운 Azure 구독을 만든 후에 Microsoft FastTrack 포털에서 호스팅하는 웹 양식을 작성 하 여 적절 한 고객 키 제공 요청을 제출 하려면 필요 합니다. FastTrack 팀 고객 키 지원을 제공 하지 않습니다. 단순히 office FastTrack 포털을 사용 하 여 양식을 전송 하 고 관련 기능을 제공 하는 고객 키에 대 한 추적 하는 데 도움이 수 있도록 합니다.
  
고객 키 제공을 제출 하면 Microsoft에서 요청을 검토 하 고 있음을 알려줍니다 설치 작업의 나머지 부분을 진행할 수 있습니다. 이 프로세스에는 최대 5 개까지 비즈니스 일 걸릴 수 있습니다.
    
- [각 구독에 프리미엄 Azure 키 추적용 만들기](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [각 주요 추적용에 사용 권한 할당](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [설정 하 고 확인을 위해 주요 볼트 대화에서 일시 삭제](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [각 주요 추적용 중 하나를 만들거나 키를 가져오기 (영문) 하 여 키 추가](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [키의 복구 수준 확인](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [백업 Azure 키 볼트](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [Azure 키 추적용 구성 설정의 유효성을 검사합니다](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [각 Azure 키 추적용 키에 대 한 URI를 얻으려면](controlling-your-data-using-customer-key.md#GetKeyURI)
    
**Office 365:**
  
Exchange Online 및 비즈니스를 위한 Skype:
  
- [비즈니스를 위한 Exchange Online 및 Skype와 함께 사용에 대 한 데이터 암호화 정책 (DEP) 만들기](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [사서함에는 DEP 할당](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [사서함 암호화의 유효성을 검사합니다](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
SharePoint Online 및 비즈니스용 OneDrive:
  
- [비즈니스 지리적으로 분산에 대 한 각 SharePoint Online 및 OneDrive에 대 한 데이터 암호화 정책 (DEP) 만들기](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [암호화 그룹 사이트, 팀 사이트 및 비즈니스용 OneDrive의 유효성을 검사합니다](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a>고객 키에 대 한 Azure 키 추적용 및 Microsoft FastTrack에서 작업을 완료 합니다.
<a name="AzureSteps"> </a>

Office 365에 대 한 고객 키를 설정 하기 위해 Azure 키 볼트에 이러한 작업을 완료 합니다. 고객 키에 대 한 설정 Exchange Online 및 Skype 비즈니스 또는 SharePoint Online 및 OneDrive를 위한 Office 365에서 지원 되는 모든 서비스 또는 비즈니스에 대 한 하려는 여부에 관계 없이 다음이 단계를 완료 해야 합니다.
  
### <a name="create-two-new-azure-subscriptions"></a>두 새로운 Azure 구독 만들기
<a name="Create2newsubs"> </a>

두 Azure 구독은 고객 키에 필요 합니다. 최상의 방법으로 고객 키로 사용에 대 한 새 Azure 구독을 만드는 것이 좋습니다. Azure 키 추적용 키 동일한 Azure Active Directory (AAD) 테 넌 트의 응용 프로그램에 대 한 권한을 부여할 수만, Office 365 조직과 사용 되는 DEPs 할당 될 동일한 Azure AD 테 넌 트를 사용 하 여 새 구독을 만들어야 합니다. Office 365 조직에 대 한 전역 관리자 권한이 있는 사용자 작업이 나 교육용 계정을 사용 하 여 예입니다. 자세한 단계는 [조직으로 Azure에 등록](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/)을 참조 하십시오.
  
> [!IMPORTANT]
> 고객 키에는 각 데이터 암호화 정책 (DEP)에 대 한 두 키가 필요 합니다. 이 작업을 수행 하기 위해 두 Azure 구독 만들어야 합니다. 최상의 방법으로 별도 조직 구성원의 각 구독에 하나의 키를 구성 해야 하는 것이 좋습니다. 또한 이러한 Azure 구독 Office 365에 대 한 암호화 키 관리만 사용 해야 합니다. 이 경우 의도적으로, 실수로 또는 악의적으로 삭제 하 여 연산자 중 하나 또는 그렇지 않은 경우에 자신이 담당 하는 키를 mismanages 조직을 보호 합니다.<br/> 고객 키로 사용 하도록 Azure 키 추적용 리소스를 관리 하기 위한 전적으로 사용 되는 새로운 Azure 구독을 설정 하는 것이 좋습니다. 조직에 대해 만들 수 있는 Azure 구독 수에 실질적인 제한은 없습니다. 이러한 모범 사례를 따르는 고객 키로 사용 되는 리소스를 관리할 수 있게 하는 동안 실수에 따른 영향을 최소화 됩니다. 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a>Office 365에 대 한 고객 키를 정품 인증을 요청을 제출
<a name="FastTrack"> </a>

Azure 단계를 완료 한 후 [Microsoft FastTrack 포털](https://fasttrack.microsoft.com/)에서 제공 요청을 제출 하려면 필요 합니다. FastTrack 웹 포털을 통해 요청을 제출 하면 Microsoft는 사용자가 제공한 Azure 키 추적용 구성 데이터 및 연락처 정보를 확인 합니다. 선택한 항목 형태로 제공 권한이 부여 된 담당자에 대 한 조직에 중요 한 이며 고객 키 등록을 완료 하는데 필요한 됩니다. 양식에서 선택 하 여 조직의 담당자 해지 하 고 삭제 하는 고객 키 데이터 암호화 정책으로 사용 되는 모든 키에 대 한 요청이의 신뢰성을 확인 하는 데 사용 됩니다. Exchange Online 추가 및 Skype 비즈니스 범위 및 일정 시간이 내에 대 한 SharePoint Online 및 비즈니스용 OneDrive에 대 한 고객 키를 정품 인증에 대 한 고객 키를 활성화 하려면이 단계를 한번씩 수행 해야 합니다.
  
고객 키를 정품 인증을 제공 하는 서비스를 전송 하려면 다음이 단계를 완료 합니다.
  
1. [Microsoft FastTrack 포털](https://fasttrack.microsoft.com/)에 로그인 Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 합니다.
    
2. 로그인 할 때 되 면 **대시보드**를 찾습니다.
    
3. **제공**하는 선택 하 고 현재 제공 업체 목록을 검토 합니다.
    
4. 경우에 적용 되는 제품에 대 한 **추가 정보** 를 선택 합니다. 
    
  - **Exchange Online 및 비즈니스를 위한 Skype:** **Exchange에 대 한 고객 키** 제공에서 **추가 정보** 를 선택 합니다. 
    
  - **SharePoint Online 및 비즈니스용 OneDrive:** **SharePoint 및 비즈니스용 OneDrive에 대 한 고객 키** 제공에서 **추가 정보** 를 선택 했습니다. 
    
5. **세부 정보 제공** 페이지에서 **요청 만들기**를 선택 합니다.
    
6. 적용 가능한 모든 내용과 제공 폼에서 요청 된 정보를 입력 합니다. 암호화 키 및 데이터의 영구 및 복구할 수 없는 폐기 승인에 대 한 권한 부여 하려는 조직의 담당자에 대 한 선택 항목을 특정 주의 해야 합니다. 양식을 완료 했을 때 **전송**선택 합니다.
    
    이 프로세스에는 사용자의 요청을 Microsoft에 알렸습니다 되 면 최대 5 개까지 비즈니스 일 걸릴 수 있습니다.
    
7. 필수 보존 기간 섹션 아래에 로그온을 계속 합니다.
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a>필수 보존 기간을 사용 하 여 Azure 구독을 등록 합니다.
<a name="RegisterSubsforMRP"> </a>

루트 암호화 키의 임시 또는 영구 손실 경로일 수도 있고 매우 손상 된 서비스 작업에도 치명적인 및 데이터 손실이 발생할 수 있습니다. 이러한 이유로 고객 키로 사용 되는 리소스에 강력한 보호가 필요 합니다. 고객 키로 사용 되는 모든 Azure 자원의 기본 구성 외 보호 메커니즘을 제공 합니다. Azure 구독 태그가 지정 된 하거나 즉각적이 고 취소할 취소 되지 않게 하는 방식에서에 등록 될 수 있습니다. 필수 보존 기간에 대 한 등록 라고 합니다. 필수 보존 기간에 대 한 Azure 구독을 등록 하는 데 필요한 단계에는 Office 365 팀과 공동 작업이 필요 합니다. 1 ~ 5 비즈니스 일이 걸릴 수 있습니다. 이전에이 경우에 따라 용어가 "취소 하지 않으면" 합니다.
  
Office 365 팀에 연락, 하기 전에 고객 키로 사용 하는 각 Azure 구독에 대해 다음 단계를 수행 해야 합니다.
  
1. Azure PowerShell을 사용한 Azure 구독에 로그인 합니다. 자세한 내용은 [Azure PowerShell을 사용 하 여 로그](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1)를 참조 하십시오.
    
2. 필수 보존 기간을 사용 하 여 알림 신청을 등록 레지스터 AzureRmProviderFeature cmdlet을 실행 합니다.
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. 프로세스를 완료 하는 Microsoft에 문의 합니다. SharePoint 및 비즈니스 팀 비즈니스용 OneDrive, [spock@microsoft.com](mailto:spock@microsoft.com)에 문의 합니다. Exchange Online 및 비즈니스를 위한 Skype, [exock@microsoft.com](mailto:exock@microsoft.com)에 문의 합니다. 서비스 수준 계약 (SLA) 필수 보존 기간을 사용 하 여 알림 신청을 완료 되 면이이 과정은 5 비즈니스 일 Microsoft가 되 고 되 면 알림을 (확인)를 등록 합니다. 전자 메일에 다음을 포함 합니다.
    
    **제목**: 고객 키에 대 한 \< *테 넌 트의 정규화 된 도메인 이름*\> 
    
    **본문**: 기간 완료 필수 보존을 갖도록 하려는 구독 Id입니다. 
    
4. 등록 완료 되는 Microsoft에서 알림, 수신 되 면 다음과 같은 Get AzureRmProviderFeature cmdlet을 실행 하 여 등록의 상태를 확인 합니다.
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. Get AzureRmProviderFeature cmdlet에서 **등록 State** 속성 반환 값이 **등록 된**의 인지를 확인 한 후 프로세스를 완료 하려면 다음 명령을 실행 합니다.
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a>각 구독에 프리미엄 Azure 키 추적용 만들기
<a name="CreateKeyVault"> </a>

[Azure 키 추적용 시작](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), 설치 및 Azure PowerShell을 시작, Azure 구독에 연결, 자원 그룹 만들기 (영문) 및 주요 추적용 만들기 (영문)를 통해 하는 방법을 안내 하는에서 설명 하는 주요 추적용을 만드는 단계 자원 그룹입니다.
  
한 SKU를 선택 해야 키 추적용을 만들 때는: 표준 또는 프리미엄 합니다. 표준 SKU-보호 하는 기능이 없는 보안 모듈 HSM (하드웨어) 키-소프트웨어로 보호에 대 한 Azure 키 추적용 키를 허용 하 고 프리미엄 SKU 키 추적용 키의 보호를 위한 Hsm 사용을 허용 합니다. 고객 키 강력 하 게 것이 좋지만 프리미엄 SKU만 사용 하 여 두 SKU를 사용 하는 주요 볼트를 허용 합니다. 두 종류의 키와 작업의 비용 이므로 동일, 비용의 유일한 차이점은 각 HSM 암호로 보호 된 키에 대 한 월별 비용입니다. 자세한 내용은 [키 추적용 가격](https://azure.microsoft.com/pricing/details/key-vault/) 을 참조 하십시오. 
  
> [!IMPORTANT]
> 주요 볼트 프리미엄 SKU와 키 HSM 암호로 보호 된 프로덕션 데이터에 대 한 및 사용만 테스트 및 유효성 검사 목적을 위해 주요 볼트 표준 SKU와 키를 사용 합니다. 
  
사용 하는 각 Office 365 서비스에 대 한를 사용 하는 고객 키에서 만든 두 Azure 구독 각 주요 추적용을 만듭니다. 등 Exchange Online 및 비즈니스만 또는 SharePoint Online 용 Skype 및 비즈니스용만, 볼트 하나만 쌍을 만들가 있습니다. Exchange Online 및 SharePoint Online에 대 한 고객 키를 사용 하려면 주요 볼트의 두 쌍을 만듭니다.
  
볼트 연관 됩니다 DEP의 용도 반영 하는 주요 볼트에 대 한 명명 규칙을 사용 합니다. 명명 규칙 권장 사항 아래 모범 사례 섹션을 참조 하십시오.
  
각 데이터 암호화 정책에 대 한 볼트의 별도, 쌍으로 지정 된 집합을 만듭니다. Exchange Online에 대 한 데이터 암호화 정책의 범위 사서함에 정책을 할당 하는 경우에 사용자가 선택 됩니다. 사서함을 할당 하는 정책을 하나만 하 고 최대 50 정책을 만들 수 있습니다. SharePoint Online에 대 한 정책 범위 지리적 위치 또는 지리적으로 분산 조직 내에서 데이터를 모두 됩니다.
  
주요 볼트를 만들 키 볼트 (경우에 매우 작은) 저장 용량이 필요 하 고 키 추적용 로깅,이 옵션을 설정 하는 경우 저장 된 데이터 생성 수도 있으므로 Azure 리소스 그룹 만들기를도 필요 합니다. 최상의 방법으로 별도 관리자를 사용 하 여 모든 관련된 고객 키 리소스를 관리 하는 관리자의 집합으로 정렬 된 관리를 사용 하 여 각 자원 그룹을 관리 하는 것이 좋습니다.
  
> [!IMPORTANT]
> 가용성을 극대화 하려면 프로그램 주요 볼트 Office 365 서비스에 근접 한 영역에 있어야 합니다. 예, Exchange Online 조직 북미에 있으면 대화 주요 볼트를 북미에 배치 합니다. Exchange Online 조직 유럽의 경우 유럽의 주요 볼트에 놓습니다.<br/>주요 볼트에 대 한 공통 접두사를 사용 하 고 사용의 약어 및 주요 추적용 및 키의 범위를 포함 (예: 북미, 이름의 가능한 쌍에에서는 볼트가 위치할 Contoso SharePoint 서비스는 O365SP NA VaultA1 Contoso에 대 한 및 Contoso-O365SP-NA-VaultA2 합니다. 추적용 이름은 Azure, 내에서 전역적으로 고유 문자열 않으므로 다른 Azure 고객에서 원하는 이름을 요구 이미는 하는 경우에 원하는 이름의 변형 시도 해야할 수 있습니다. 년 7 월 2017 년 일 이후로 추적용 이름은 변경할 수 없으므로, 설치 프로그램에 대 한 계획을 작성된 하 고 계획 제대로 실행을 확인 하려면 두번째 사용자를 사용 하는 것이 좋습니다.<br/>가능한 경우 지역에 연결 된 비에서 여 볼트를 만듭니다. Azure 지역 쌍으로 지정 된 서비스 오류 도메인에서 고가용성을 제공 합니다. 따라서 다른 사용자의 백업 지역으로 지역 쌍의 생각할 수 있습니다. 즉, 한 영역에 저장 되는 Azure 자원 내결함성을 쌍으로 지정 된 영역을 통해 사용할 수 있는 자동으로 됩니다. 이러한 이유로 총 가용성의 두 지역에서에서 사용 하는 쌍으로 지정 된 의미를 지역이 여기서 DEP에 사용 되는 두 볼트에 대 한 영역을 선택 합니다. 대부분 지역만 없으므로 두 영역을 아직 선택 영역에 연결 된 비 수 없습니다. 가능한 경우 사용 하는 종속 된 두 볼트에 대 한 비에 연결 된 두 지역 선택 이 총 가용성의 네 영역에서에서 향상 시켜줍니다. 자세한 내용은 참조 [비즈니스 연속성 및 재해 복구 (BCDR): Azure 쌍 영역](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) 지역 쌍의 현재 목록에 대 한 합니다. 
  
### <a name="assign-permissions-to-each-key-vault"></a>각 주요 추적용에 사용 권한 할당
<a name="KeyVaultPerms"> </a>

각 주요 추적용에 대 한 구현에 따라 고객 키에 대 한 권한의 세 별도 집합을 정의 해야 합니다. 예, 하나는 다음의 각 항목에 대 한 사용 권한 집합을 정의 해야 합니다.
  
- **키 추적용 관리자가** 조직에 대 한 주요 추적용 대화의 일상적인 관리 작업을 수행 하는 합니다. 이러한 작업 백업 포함, 만들기, 가져오기, 가져오기, 목록, 및 복원 합니다. 
    
    > [!IMPORTANT]
    > 주요 추적용 관리자에 게 할당 된 권한 집합이 키를 삭제할 수 있는 권한이 포함 되지 않습니다. 이 의도적인 것 하 고는 중요 한 연습 합니다. 암호화 키를 삭제 하지 일반적으로 완료 되 면 데이터를 소멸 하므로 영구적으로 수행 하는 이후 합니다. 최상의 방법으로이 권한을 부여 하지 마십시오이 주요 추적용 관리자에 게 기본적으로 합니다. 대신, 주요 추적용 참가자 (영문)에 대 한이 예약 하 고만 결과 명확 하 게 이해 이해 되 면 단기간 별로 관리자에 게 할당 합니다. 
  
    Office 365 조직에서 사용자에 게 이러한 사용 권한을 할당할 Azure PowerShell을 사용한 Azure 구독에 로그인 합니다. 자세한 내용은 [Azure PowerShell을 사용 하 여 로그](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1)를 참조 하십시오.
    
- 필요한 사용 권한을 할당 하려면 집합 AzureRmKeyVaultAccessPolicy cmdlet을 실행 합니다.
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  예를 들면 다음과 같습니다.
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- **키 추적용 참가자 (영문)을** 변경할 수 있는 Azure 키 볼트에 대 한 권한을 자체 합니다. 직원 상태로 두거나, 팀에 참가 하거나 매우 드문 상황에서 키 볼트는 관리자가 합법적으로 필요가 삭제 또는 키를 복원 하는 권한이 따라 이러한 사용 권한을 변경 해야 합니다. 이 집합 키 추적용 대화에 **참가자** 역할을 부여할 주요 추적용 참가자 (영문) 요구 사항입니다. Azure 리소스 관리자를 사용 하 여이 역할을 할당할 수 있습니다. 자세한 단계에 대 한 [Azure 구독 리소스에 대 한 액세스를 관리 하려면 Use Role-Based 액세스 제어](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure)를 참조 합니다. 관리자가 구독을 만듭니다에 따라 다른 관리자가 참가자 역할에 할당 하는 기능과 함께이 액세스를 하는 암시적으로 부여 합니다.
    
- 비즈니스를 위한 Exchange Online 및 Skype와 고객 키를 사용 하려는 경우에 비즈니스를 위한 Exchange Online 및 Skype을 대신 하 여 주요 추적용을 사용 하 여 Office 365에 권한을 부여 해야 합니다. 마찬가지로, 비즈니스를 위한 SharePoint Online 및 OneDrive 고객 키를 사용 하 여 비즈니스를 위한 SharePoint Online 및 OneDrive을 대신 하 여 주요 추적용을 사용 하 여 Office 365에 대 한 사용 권한을 추가 해야 합니다. Office 365에 권한을 지정 하려면 다음 구문을 사용 하 여 **집합 AzureRmKeyVaultAccessPolicy** cmdlet를 실행 합니다. 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    여기서 각 부분이 나타내는 의미는 다음과 같습니다.
    
  - *vaultname* 은 만든 주요 추적용의 이름입니다. 
    
  - Exchange Online 및 비즈니스를 위한 Skype와 *Office 365 appID* 바꾸기`00000002-0000-0ff1-ce00-000000000000`
    
  - SharePoint Online 및 비즈니스용 OneDrive와 *Office 365 appID* 바꾸기`00000003-0000-0ff1-ce00-000000000000`
    
  예: Exchange Online 및 Skype 비즈니스에 대 한 권한 설정:
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  예: SharePoint Online 및 비즈니스용 OneDrive에 대 한 사용 권한 설정
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a>설정 하 고 확인을 위해 주요 볼트 대화에서 일시 삭제
<a name="SoftDelete"> </a>

신속 하 게 키를 복구할 수 있습니다 때 실수로 또는 악의적으로 삭제 된 키로 인해 확장 된 서비스 중단이 발생할 가능성이 적은 됩니다. 라고 소프트 삭제 고객 키를 사용 하면 키를 사용 하려면 먼저,이 구성을 사용 하도록 설정 해야 합니다. 부드러운 삭제를 사용 하도록 설정 백업에서 복원 하지 않고 삭제 90 일 이내 키 또는 볼트를 복구할 수 있습니다.
  
을 사용 하려면 소프트 삭제 하면 주요 볼트에서 다음이 단계를 완료 합니다.
  
1. Windows Powershell을 사용한 Azure 구독에 로그인 합니다. 자세한 내용은 [Azure PowerShell을 사용 하 여 로그](https://docs.microsoft.com/powershell/azure/authenticate-azureps)를 참조 하십시오.
    
2. [Get AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) cmdlet을 실행 합니다. 이 예제에서는 *vaultname* 의 이름인을 사용할 수 있도록 일시 삭제 하는 주요 추적용: 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. 일시 삭제 하도록 구성 된 주요 추적용 **Get AzureRmKeyVault** cmdlet을 실행 하 여 확인 합니다. 일시 삭제 제대로 키 볼트에 대 한 구성 하는 경우는 일시 삭제 사용 합니까? 속성의 **True**값을 반환 합니다. 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a>각 주요 추적용 중 하나를 만들거나 키를 가져오기 (영문) 하 여 키 추가
<a name="AddKeystoKeyVault"> </a>

두 가지 방법으로 Azure 키 추적용;에 키를 추가 하려면 키 추적용에서 직접 키를 만들거나 키를 가져올 수 있습니다. 키를 가져오기 (영문) 키가 생성 하는 방법을 통해 전체 제어를 제공 하는 동안 덜 복잡된 메서드는 키 볼트에 직접 키 만들기 (영문).
  
주요 추적용 프로그램에서 직접 키를 만들려면 [추가 AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) cmdlet를 다음과 같이 실행 합니다. 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

여기서 각 부분이 나타내는 의미는 다음과 같습니다.
  
-  *vaultname* 은 키를 만들려는 주요 추적용의 이름입니다. 
    
-  *키 이름* 에 새 키에 지정할 이름입니다. 
    
    > [!TIP]
    > 주요 볼트에 대해 설명한 것과 같이 유사한 명명 규칙을 사용 하 여 키 이름을 지정 합니다. 이와 같은 방식이으로 키 이름에만 표시 하는 도구에는 문자열은 자체를 설명 하는 합니다. 
  
- HSM 사용 하 여 키를 보호 하 려 한다고 지정 하는 **HSM** _대상_ 매개 변수의 값으로 지정 그렇지 않은 경우 **소프트웨어**를 확인 합니다.
    
예:
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

주요 추적용 대화에 직접 키를 가져오려면, Thales nShield 하드웨어 보안 모듈을 지정 해야 합니다.
  
일부 조직에서는이 방법을 자신의 키와이의 provenance을 설정 하는 것을 선호 메서드는 다음을 제공 합니다.
  
- 가져오기에 사용 되는 도구 세트를 생성할 키를 암호화 하는데 사용 되는 키 교환 키 (KEK) 내보낼 수 없는 Thales에서 대를 포함 하 고 Thales 하 여 제조 된는 정품 HSM 내 생성 됩니다.
    
- 도구 집합을 Azure 키 추적용 보안 세계 Thales에서 제조 프로그램 정품 HSM에도 생성 된 Thales에서 대를 포함 합니다. 이 증명 Microsoft 정품 Thales 하드웨어를 사용 하 고 하 게 증명 합니다.
    
위의 attestations 필요한 경우 확인 하 여 보안 그룹과 확인 합니다. 주요 온-프레미스를 만들고 여 키 추적용으로 가져올 하는 자세한 단계를 [생성 하 고 Azure 키 볼트에 대 한 HSM 암호로 보호 된 키를 전송 하는 방법](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/)을 참조 하십시오. Azure 지침을 사용 하 여 각 주요 볼트에 키를 만듭니다.
  
### <a name="check-the-recovery-level-of-your-keys"></a>키의 복구 수준 확인
<a name="CheckKeyRecoveryLevel"> </a>

Office 365 Azure 키 추적용 구독을 취소 하지 않으면 로설정하면 고객 키로 사용 되는 키가 사용 하도록 설정 하는 일시 삭제는 필요 합니다. 키에 복구 수준에서 조회 하 여이 확인할 수 있습니다.
  
복구에 대 한 수준의 Azure PowerShell에서 키를 확인 하려면 다음과 같이 입력 하는 Get AzureKeyVaultKey cmdlet를 실행 합니다.
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

이 항목을 검토 하 고 취소 하지 않으면 목록에 구독을 배치 하는 단계를 모두 수행 되었는지 확인 하려면 해야 _복구 수준_ 속성 값이 **복구할 수 있는 + ProtectedSubscription**아닌 다른를 반환 하 고 각 주요 볼트 프로그램에서 사용 하도록 설정 하는 일시 삭제 해야 합니다.
  
### <a name="backup-azure-key-vault"></a>백업 Azure 키 볼트
<a name="BackupAzureKeyVaultkeys"> </a>

즉시 키를 하려면 만들기 또는 변경에 따라 백업을 수행 하 고 온라인 및 오프 라인 백업 복사본을 저장 합니다. 오프 라인 복사본 하지 연결 되어야 합니다를 모든 네트워크와 같은 실제 안전 또는 상업용 저장소 시설에서. 하나 이상의 사본은 백업 재해 발생 시 액세스할 수 있는 위치에 저장 되어야 합니다. 백업 blob가 주요 자료 해야 키 추적용 키 수 영구적으로 삭제 또는 복원 그렇지 않은 경우 작동 하지 않는 렌더링 하는 유일한 방법입니다. Azure 키 추적용 외부 및 Azure 키 추적용 가져온는 키를 키를 사용 하 여 고객 키에 대 한 필요한 메타 데이터는 외부 키가 있는 존재 하지 않는 때문에 대 한 백업으로 해결할 수 없는 합니다. Azure 키 추적용에서 수행한 백업만 고객 키로 복원 작업에 대해 사용할 수 있습니다. 따라서 반드시 키가 업로드 하거나 만든 후 Azure 키 추적용의 백업을 수행할 수 있습니다.
  
Azure 키 추적용 키의 백업을 만들려면 다음과 같이 입력 하는 [백업 AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) cmdlet를 실행 합니다.
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

출력 파일 접미사를 사용 하는지 확인 `.backup`합니다.
  
이 cmdlet에서 발생 하는 출력 파일이 암호화 되 고 Azure 키 추적용 외부에서 사용할 수 없습니다. 백업을 수행한 Azure 구독에만 백업을 복원할 수 있습니다.
  
> [!TIP]
> 출력 파일에 대 한 추적용 이름과 키 이름의 조합을 선택 합니다. 이 파일 이름 자체를 설명 하는 변경 됩니다. 또한 백업 파일 이름 충돌 하지 않도록 확인 됩니다. 
  
예를 들면 다음과 같습니다.
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a>Azure 키 추적용 구성 설정의 유효성을 검사합니다
<a name="Validateconfiguration"> </a>

선택 사항 이지만 권장 되는 DEP에 키를 사용 하기 전에 유효성 검사를 수행 합니다. 특히를 설정 하 여 키와 볼트가이 항목에 설명 된 것 외에 다른 단계를 사용 하는 경우 고객 키를 구성 하기 전에 Azure 키 추적용 리소스 상태 고 있는지 확인 해야 합니다.
  
키를 사용 하도록 설정 하는 get, wrapKey, 및 unwrapKey 작업 있는지 확인.
  
다음과 같이 [Get AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) cmdlet를 실행 합니다. 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

출력에서을 적절 하 게 액세스 정책에 대 한와 Exchange Online id (GUID) 또는 SharePoint Online id (GUID)를 찾습니다. 위의 권한의 모든 3 키에 사용 권한에서 표시 되어야 합니다.
  
액세스 정책 구성 올바르지 않을 경우 다음과 같이 설정 AzureRmKeyVaultAccessPolicy cmdlet를 실행 합니다.
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

예: Exchange Online 및 비즈니스를 위한 Skype:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

예: SharePoint Online 및 비즈니스용 OneDrive:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

다음과 같이 [Get AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) cmdlet을 실행 하 여 키에 대 한 만료 날짜 설정 되어 있지 않은지 확인 합니다. 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

고객 키로는 만료 된 키를 사용할 수 없습니다 및 만료 된 키로 시도 하는 작업 실패 하 고 가능한 경우 서비스 중단을 초래할 됩니다. 고객 키로 사용 되는 키 만료 날짜를 갖지 않습니다 하는 것이 좋습니다. 만료 날짜, 집합을 제거할 수 없습니다 되지만 다른 날짜를 변경할 수 있습니다. 키를 설정 하는 만료 날짜가 있는 사용 해야을 하는 경우 만료 값을 12/31/9999로 변경 합니다. 만료 날짜와 함께 키 12/31/9999 Office 365 유효성 검사를 통과 하지 못합니다 외에 날짜를 설정 합니다.
  
12/31/9999이 아닌 값으로 설정 된 만료 날짜를 변경 하려면 다음과 같이 입력 하는 [집합 AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) cmdlet를 실행 합니다. 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> 고객 키로 사용 하 여 암호화 키에 대해 만료 날짜를 설정 하지 마십시오. 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a>각 Azure 키 추적용 키에 대 한 URI를 얻으려면
<a name="GetKeyURI"> </a>

한번에 주요 볼트를 설정 하는 Azure의 모든 단계를 완료 하 고 각 주요 볼트의 키에 대 한 URI를 가져오려면 다음 명령을 실행 하 여 키를 추가 합니다. 이러한 사용 해야하는 Uri를 만들고 각 DEP를 나중에 할당 하는 경우 안전한 위치에 있으므로이 정보를 저장 합니다. 각 주요 추적용에 대해 한번씩이 명령을 실행 해야 합니다.
  
Azure powershell:
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a>Office 365: Exchange Online 및 Skype 비즈니스를 위한 고객 키를 설정합니다.
<a name="AzureSteps"> </a>

시작 하기 전에 Azure 키 추적용을 설정 하는 데 필요한 작업을 완료 했는지 확인 합니다. 자세한 내용은 [Azure 키 추적용 및 고객 키에 대 한 Microsoft FastTrack에서 작업을 완료](controlling-your-data-using-customer-key.md#AzureSteps) 를 참조 합니다. 
  
Exchange Online 및 Skype 비즈니스를 위한 고객 키를 설정 하려면 원격 Windows PowerShell을 사용한 Exchange Online에 연결 하 여 이러한 단계를 수행 해야 합니다.
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a>비즈니스를 위한 Exchange Online 및 Skype와 함께 사용에 대 한 데이터 암호화 정책 (DEP) 만들기
<a name="CreateDEP4EXOSkype"> </a>

한 DEP Azure 키 볼트에 저장 된 키 집합으로 연결 됩니다. Office 365의 사서함에는 DEP를 할당 합니다. 다음 office 365 정책에서 식별 된 키를 사용 하 여 사서함을 암호화 됩니다. DEP를 만들려면 이전에 가져온 키 추적용 Uri 해야 합니다. 대 한 자세한 내용은 [가져오는 각 Azure 키 추적용 키에 대 한 URI를](controlling-your-data-using-customer-key.md#GetKeyURI) 참조 하십시오. 
  
기억! DEP를 만들 때 서로 다른 두 Azure 키 볼트에 있는 두 키를 지정 합니다. 이러한 키 지리적으로 분산 중복 되도록 별도 두 Azure 영역에 있는 있는지 확인 합니다.
  
DEP를 만들려면 다음이 단계를 따릅니다.
  
1. 로컬 컴퓨터에서 Windows PowerShell을 열고 다음 명령을 실행 하 여 [Exchange Online PowerShell에 연결](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) 하 여 Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 합니다. 
    
   ```
   $UserCredential = Get-Credential
   ```

2. Windows PowerShell 자격 증명 요청 대화 상자에서 작업 시간을 입력 또는 계정 정보를 학교, **확인**을 클릭 한 후 다음 명령을 입력 합니다. 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. 다음 명령을 실행합니다.
    
   ```
   Import-PSSession $Session
   ```

4. DEP를 만들려면 다음 명령을 입력 하 여 새로 DataEncryptionPolicy cmdlet을 사용 합니다.
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   여기서 각 부분이 나타내는 의미는 다음과 같습니다.
    
   -  *PolicyName* 은 정책에 대해 사용 하려는 이름입니다. 이름에 공백을 포함할 수 없습니다. 예: USA_mailboxes 합니다. 
    
   -  *PolicyDescription* 은 정책입니다 기억할 수 있는 정책 사용자가 친숙 한 설명입니다. 설명에 공백을 포함할 수 있습니다. 미국 및 해당 지역에서 사서함에 대 한 키를 루트 예입니다. 
    
   -  *KeyVaultURI1* 은 정책에서 첫번째 키에 대 한 URI입니다. 예, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01합니다. 
    
   -  *KeyVaultURI2* 은 정책에서 두번째 키에 대 한 URI입니다. 예, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02합니다. 쉼표 및 공백을 두 Uri를 구분 합니다. 
    
   예제:
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a>사서함에는 DEP 할당
<a name="assignDEPtomailbox"> </a>

Set-mailbox cmdlet을 사용 하 여 사서함에는 DEP를 할당 합니다. Office 365는 종속에 지정 된 키가 있는 사서함을 암호화할 수에 정책을 할당 한 후
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

여기서 *MailboxIdParameter* 사서함을 지정 합니다. Set-mailbox cmdlet에 대 한 자세한 내용은 [Set-mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx)를 참조 하십시오.
  
### <a name="validate-mailbox-encryption"></a>사서함 암호화의 유효성을 검사합니다
<a name="validatemailboxencryption"> </a>

사서함을 암호화 다소 시간이 걸릴 수 있습니다. 1 시간 정책 할당에 대 한 사서함도 완료 해야 하나의 데이터베이스에서 다른 위치로 이동 서비스의 사서함을 암호화할 수 있습니다. 72 시간 후는 DEP를 변경 하거나 사서함에는 DEP를 할당 처음으로 암호화의 유효성을 검사 하려고 하기 전에 대기 하는 것이 좋습니다.
  
Get-mailboxstatistics cmdlet을 사용 하 여 사서함 암호화 하는 경우를 결정할 수 있습니다.
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

IsEncrypted 속성은 사서함 암호화 되지 않은 경우 값이 **true** 이면 사서함은 암호화와 값이 **false** 를 반환 합니다. 

사서함 이동이 완료 시간으로는 처음에 대 한 DEP이 지정 된 사서함 수는 사서함의 크기에 따라 달라 집니다. DEP를 할당 하는 사서함 시간부터 1 주일 후 암호화 되지 않은 경우, New-moverequest cmdlet을 사용 하 여 암호화 되지 않은 사서함에 대 한 사서함 이동을 시작 합니다.

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a>Office 365: SharePoint Online 및 비즈니스용 OneDrive에 대 한 고객 키를 설정합니다.
<a name="AzureSteps"> </a>

시작 하기 전에 Azure 키 추적용을 설정 하는 데 필요한 작업을 완료 했는지 확인 합니다. 자세한 내용은 [Azure 키 추적용 및 고객 키에 대 한 Microsoft FastTrack에서 작업을 완료](controlling-your-data-using-customer-key.md#AzureSteps) 를 참조 합니다. 
  
SharePoint Online 및 비즈니스용 OneDrive에 대 한 고객 키를 설정 하려면 원격 Windows PowerShell을 사용한 SharePoint Online에 연결 하 여 이러한 단계를 수행 해야 합니다.
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a>비즈니스 지리적으로 분산에 대 한 각 SharePoint Online 및 OneDrive에 대 한 데이터 암호화 정책 (DEP) 만들기
<a name="CreateDEP4SPOODfB"> </a>

한 DEP Azure 키 볼트에 저장 된 키 집합으로 연결 됩니다. 지리적으로 분산이 라고도 하는 하나의 지리적 위치에 데이터를 모두에 DEP를 적용 합니다. (현재 미리 보기)에서 Office 365의 다중-지리적으로 분산 기능을 사용 하는 경우에 지리적으로 분산 당 하나의 DEP를 만들 수 있습니다. 다중-지리적으로 분산을 사용 하지 않는 경우에 비즈니스를 위한 SharePoint Online 및 OneDrive 사용 하기 위한 Office 365에서 하나의 DEP를 만들 수 있습니다. 다음 office 365는 DEP에서 식별 된 키를 사용 하 여 해당 지리적으로 분산에서 데이터를 암호화 됩니다. DEP를 만들려면 이전에 가져온 키 추적용 Uri 해야 합니다. 대 한 자세한 내용은 [가져오는 각 Azure 키 추적용 키에 대 한 URI를](controlling-your-data-using-customer-key.md#GetKeyURI) 참조 하십시오. 
  
기억! DEP를 만들 때 서로 다른 두 Azure 키 볼트에 있는 두 키를 지정 합니다. 이러한 키 지리적으로 분산 중복 되도록 별도 두 Azure 영역에 있는 있는지 확인 합니다.
  
DEP를 만들려면 Windows PowerShell을 사용 하 여 원격으로 SharePoint Online에 연결 해야 합니다.
  
1. 로컬 컴퓨터에서 [SharePoint Online Powershell에 연결](https://technet.microsoft.com/library/fp161372.aspx)하 여 Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 합니다.
    
2. Microsoft SharePoint Online 관리 셸에서 다음과 같이 [레지스터 SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) cmdlet을 실행 합니다. 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   DEP를 등록 하는 경우 암호화는 지리적으로 분산의 데이터를 시작 합니다. 이 다소 시간이 걸릴 수 있습니다.
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a>암호화 그룹 사이트, 팀 사이트 및 비즈니스용 OneDrive의 유효성을 검사합니다
<a name="validateencryptionSPO"> </a>

다음과 같이 Get SPODataEncryptionPolicy cmdlet을 실행 하 여 암호화의 상태를 확인할 수 있습니다.
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

이 cmdlet의 출력에는 다음이 포함 됩니다.
  
- 기본 키의 URI입니다.
    
- 보조 키의 URI입니다.
    
- 지리적으로 분산에 대 한 암호화 상태입니다. 가능한 상태에는 다음이 포함 됩니다.
    
  - **등록을 취소할:** 고객 키 암호화 아직 적용 되지 않았습니다. 
    
  - **등록:** 고객 키 암호화 적용 된 및 프로그램 파일을 암호화 하는 과정입니다. 프로그램 지리적으로 분산이이 상태에 있으면 화면이 표시 됩니다 정보에는 지리적으로 분산의 사이트는 몇 % 완료 암호화 진행 상태를 모니터링할 수 있도록 합니다. 
    
  - **등록:** 고객 키 암호화를 적용 하 고 모든 사이트의 모든 파일을 암호화 합니다. 
    
  - **롤링:** 주요 roll 진행중에서입니다. 프로그램 지리적으로 분산이이 상태에 있으면 화면이 표시 됩니다 정보 사이트는 몇 % 주요 roll 작업 진행 상태를 모니터링할 수 있도록 완료에 합니다. 
    
## <a name="managing-customer-key-for-office-365"></a>Office 365에 대 한 고객 키 관리
<a name="ManageCustomerKey"> </a>

고객 키에서 Office 365에 대 한 설정한 후에 이러한 추가 관리 작업을 수행할 수 있습니다.
  
- [Azure 키 추적용 키 복원](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [롤링 또는 고객 키로 사용 된 자격 증명 Azure 키 모음에서 키를 회전 합니다.](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [주요 추적용 사용 권한 관리](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [사서함에 할당 된 DEP를 결정 합니다.](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a>Azure 키 추적용 키 복원
<a name="RestoreAzureKeyVaultKeys"> </a>

복원을 수행 하기 전에 일시 삭제 하 여 제공 하는 복구 기능을 사용 합니다. 고객 키로 사용 되는 모든 키가 사용 하도록 설정 하는 일시 삭제 해야할 필요 합니다. 일시 삭제 휴지통 처럼 작동 하 고 복원할 필요 없이 최대 90 일에 대 한 복구를 허용 합니다. 복원 예: 키 또는 키 추적용 손실 되는 경우 아주 또는 특수 한 경우에서에 필요 해야 합니다. 고객 키로 사용에 대 한 키를 복원 해야 하는 경우 Azure powershell에서 cmdlet을 실행 복원 AzureKeyVaultKey 다음과 같습니다.
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

예를 들면 다음과 같습니다.
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

이름이 같은 키 키 볼트에 이미 존재 하는 경우 복원 작업이 실패 합니다. 복원 AzureKeyVaultKey 모든 주요 버전 및 키 이름을 포함 하는 키에 대 한 모든 메타 데이터를 복원 합니다.
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a>롤링 또는 고객 키로 사용 된 자격 증명 Azure 키 모음에서 키를 회전 합니다.
<a name="RollCKkey"> </a>

키 롤링 Azure 키 추적용 중 하나 또는 고객 키가 필요 하지 않습니다. 또한 HSM로 보호 되는 키를 위태롭게 할 가능성 거의 모든 수는 없습니다. 루트 키가 악의적인 작업자의 소유 하는 경우에 없는 적절 한 방법을 사용 하 여 Office 365 코드만 사용 하는 방법을 알고 있으므로 데이터를 암호 해독의 방법이 있습니다. 그러나 키 롤링 고객 키에 의해 지원 됩니다.
  
> [!CAUTION]
> 확인란의 선택을 취소 기술 이유 존재 하지 않거나 규정 준수 요구 사항을 규정 키 롤 해야할 때 고객 키를 사용 하는 암호화 키를 롤만 합니다. 또한 추가 되거나 정책과 연결 된 모든 키를 삭제 하지 마십시오. 키가 있는지를 배포할 때 콘텐츠 암호화 이전 키를 사용 합니다. 등 활성 사서함 다시 암호화 됩니다 자주, 비활성화 하는 동안 이전 키로는 암호화 끊어지고 비활성화 된 사서함 수 있습니다. SharePoint Online에서는 백업 콘텐츠 복원 및 복구 목적을 위해 계속 되는 경우도 있으므로 오래 된 키를 사용 하 여 보관 된 콘텐츠입니다.<br/> 데이터의 안전을 위해, SharePoint Online를 선택 하면 둘 이상의 키 롤 작업 한번에 진행에서 되도록 합니다. 첫번째 주요 roll 작업을 대기 해야 키 볼트에 키의 모두 롤 하려는 경우 완벽 하 게 완료 합니다. 중요 하지 않은 있도록 서로 다른 간격 주요 roll 작업을 분산 하는 것이 좋습니다. 
  
기존 키의 새 버전을 요청 하는 키를 배포할 때 합니다. 기존 키의 새 버전을 요청 하기 위해 키를 처음부터 만들 때 사용한 동일한 구문을 사용 하 여 [추가 AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey)동일한 cmdlet은를 사용 합니다.
  
예를 들면 다음과 같습니다.
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

이 예제에서는 **Contoso O365EX-NA VaultA1** 볼트에 이미 **Contoso-O365EX-NA-VaultA1-Key001** 라는 키 존재 하므로 새로운 주요 버전 생성 됩니다. 새 키 버전을 추가 하는 작업입니다. 이 작업 키의 버전 기록에서 이전 키 버전을 유지 하는 이전에 해당 키를 사용 하 여 암호화 된 데이터의 암호를 해독할 수 계속 되도록 합니다. 롤링는 DEP와 연결 된 모든 키를 완료 한 후 다음 고객 키 새 키를 사용 하 여 시작 되도록는 추가 cmdlet을 실행 해야 합니다. 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a>Exchange Online 및 비즈니스를 위한 Skype 롤 또는 Azure 키 볼트에 키를 회전 한 후 새 키를 사용 하 여 사용 하도록 설정

중 하나를 배포할 때 비즈니스를 위한 Exchange Online 및 Skype와 사용 되는 DEP와 관련 된 Azure 키 추적용 키는 DEP를 업데이트 하 고 새 키를 사용 하 여 시작 하려면 Office 365를 사용 하도록 설정 하려면 다음 명령을 실행 해야 합니다.
  
다음과 같이 설정 DataEncryptionPolicy cmdlet을 실행 하는 Office 365에서 사서함을 암호화 하려면 새 키를 사용 하 여 고객 키에 지시 합니다.
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

48 시간 내에서 활성 사서함이이 정책을 사용 하 여 암호화 된 업데이트 된 키와 관련 됩니다. 사서함에 대 한 DataEncryptionPolicyID 속성에 대 한 값을 확인 하 [는 사서함에 할당 된 DEP 결정](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) 의 단계에 따라 합니다. 이 속성에 대 한 값이 업데이트 된 키가 적용 된 후 변경 됩니다. 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a>SharePoint Online 및 비즈니스용 OneDrive 롤 또는 Azure 키 볼트에 키를 회전 한 후 새 키를 사용 하 여 사용 하도록 설정

중 하나를 배포할 때 비즈니스를 위한 SharePoint Online 및 OneDrive 사용 하는 한 DEP와 관련 된 Azure 키 추적용 키는 DEP를 업데이트 하 고 새 키를 사용 하 여 시작 하려면 Office 365를 사용 하도록 설정 하려면 [업데이트 SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) cmdlet을 실행 해야 합니다. 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

SharePoint Online 및 비즈니스용 OneDrive에 대 한 주요 roll 작업이 시작 됩니다. 이 작업은 직접 실행 하지 않습니다. 작업 롤 키의 진행률을 보려면 다음과 같이 입력 하는 Get SPODataEncryptionPolicy cmdlet를 실행 합니다.
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a>주요 추적용 사용 권한 관리
<a name="Managekeyvaultperms"> </a>

여러 cmdlet을 사용할 수 있는 확인 하 고 필요한 경우 제거 키 추적용 사용 권한 수 있도록 하는 합니다. 직원이 팀을 떠날 때 사용 권한, 예를 제거 해야 합니다.
  
주요 추적용 사용 권한을 보려면, Get-AzureRmKeyVault cmdlet을 실행 합니다.
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

예를 들면 다음과 같습니다.
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

관리자의 사용 권한을 제거 하려면 제거 AzureRmKeyVaultAccessPolicy cmdlet을 실행 합니다.
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

예를 들면 다음과 같습니다.
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a>사서함에 할당 된 DEP를 결정 합니다.
<a name="DeterminemailboxDEP"> </a>

사서함에 할당 된 DEP를 확인 하려면 Get-mailboxstatistics cmdlet을 사용 합니다. Cmdlet은 고유 식별자 (GUID)를 반환합니다.
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

여기서 *GeneralMailboxOrMailUserIdParameter* 사서함을 지정 합니다. Get-mailboxstatistics cmdlet에 대 한 자세한 내용은 [Get-mailboxstatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx)을 참조 하십시오.
  
다음 cmdlet를 실행 하 여 할당 된 사서함을 DEP의 이름을 확인 하는 GUID를 사용 합니다.
  
```
Get-DataEncryptionPolicy <GUID>
```

여기서 *GUID* 는 이전 단계에서 Get-mailboxstatistics cmdlet에 의해 반환 되는 GUID입니다. 
  

