---
title: Office 365의 고객 키를 사용한 서비스 암호화 관련 자주하는 질문
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/31/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 41ae293a-bd5c-4083-acd8-e1a2b4329da6
description: office 365에서는 BitLocker 및 DKM (분산 키 관리자)를 통해 사용 하도록 설정 되는 초기 볼륨 수준 암호화와 함께 Exchange의 데이터를 포함 하 여 office 365의 고객 콘텐츠에 대 한 응용 프로그램 수준에 추가 된 암호화 계층을 제공 합니다. 온라인, 비즈니스용 Skype, SharePoint Online 및 비즈니스용 OneDrive 이를 서비스 암호화 라고 합니다.
ms.openlocfilehash: 5e1acca69ccdd8acb986acb4d7a302d4ca3fbe8a
ms.sourcegitcommit: 8a65a29aa3bfe5dcad0ff152a7cd795e02877dd9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/28/2019
ms.locfileid: "30936768"
---
# <a name="service-encryption-with-customer-key-for-office-365-faq"></a>Office 365의 고객 키를 사용한 서비스 암호화 관련 자주하는 질문

office 365에서는 BitLocker 및 DKM (분산 키 관리자)를 통해 사용 하도록 설정 되는 초기 볼륨 수준 암호화와 함께 Exchange의 데이터를 포함 하 여 office 365의 고객 콘텐츠에 대 한 응용 프로그램 수준에 추가 된 암호화 계층을 제공 합니다. 온라인, 비즈니스용 Skype, SharePoint Online 및 비즈니스용 OneDrive 이를 서비스 암호화 라고 합니다.
  
고객 키는 서비스 암호화를 기반으로 하며, [OST (온라인 서비스 약관)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx)에 설명 된 대로 Office 365에서 휴지 상태의 데이터를 암호화 하는 데 사용 되는 키를 제공 하 고 제어할 수 있습니다. 고객 키를 사용하면 Office 365가 데이터의 암호를 해독하는 데 사용하는 암호화 키를 제어하므로 준수 의무를 이행할 수 있습니다.
  
설명서를 포함 하 여 고객 키에 대 한 의견을 제공 하려면 아이디어, 제안 사항 및 전망을 customerkeyfeedback@microsoft.com으로 전송 합니다.
  
## <a name="what-is-service-encryption-with-customer-key"></a>고객 키를 사용한 서비스 암호화 란?

고객 키를 사용 하면 클라우드 서비스 공급자와의 키 배치를 지정 하는 규정 준수 요구 사항을 충족 하는 조직의 기능을 향상 시킬 수 있습니다. 고객 키를 사용 하 여 응용 프로그램 수준에서 Office 365 데이터에 대 한 암호화 키를 제공 하 고 제어할 수 있습니다. 따라서 서비스 종료를 결정 해야 하는 경우 조직의 키를 제어 하 고 해지할 수 있습니다. 키를 해지 하면 서비스에서 데이터를 읽을 수 없게 됩니다. 키 해지가 데이터 삭제 경로에 대 한 첫 번째 단계입니다.

## <a name="what-office-365-data-at-rest-is-covered-by-customer-key"></a>나머지 Office 365 데이터는 고객 키에 따라 적용 됩니다.
<a name="WhatDataIsCoveredbyCustomerKey"> </a>

SharePoint Online 사이트 콘텐츠 및 해당 사이트에 저장 된 파일 및 비즈니스용 OneDrive에 업로드 된 파일에 대해 설명 합니다. Exchange Online 사서함 콘텐츠 (전자 메일 본문, 일정 항목 및 전자 메일 첨부 파일의 콘텐츠)에 대해 설명 합니다. 비즈니스용 skype의 텍스트 대화에 적용 되지만, skype 모임 브로드캐스트 기록과 skype 모임 콘텐츠 업로드에 대해서는 다루지 않습니다. skype 모임 브로드캐스트 및 skype 모임 콘텐츠 업로드는 Office 365의 다른 모든 콘텐츠와 함께 암호화 되지만 현재는 암호화 키에 대 한 고객 제어를 제공 하지 않습니다.
  
## <a name="what-is-the-difference-between-customer-key-and-bring-your-own-key-byok-with-azure-information-protection-for-exchange-online"></a>고객 키와 원격 키 (byok)를 사용 하 여 Exchange Online에 대 한 Azure Information Protection이 어떻게 다릅니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

두 옵션을 모두 사용 하면 자체 암호화 키를 제공 하 고 제어할 수 있습니다. 그러나 고객 키를 사용한 서비스 암호화는 rest의 Office 365 서버에 상주 하는 휴지 상태의 데이터를 암호화 하 고, Exchange Online에 대 한 Azure Information Protection을 사용 하는 경우에는 전송 된 데이터를 암호화 하 고 지속적인 온라인 및 오프 라인 기능을 제공 합니다. Office 365의 전자 메일 메시지 및 첨부 파일을 보호 합니다. 고객 키 및 Azure Information Protection with Exchange Online은 상호 보완적 이며 Microsoft의 서비스 관리 키 또는 자체 키를 사용 하도록 선택 하는 경우에는 rest 및 전송 중인 데이터를 암호화 하는 것이 추가 보호 기능을 제공할 수 있습니다. 악의적인 공격
  
Office 365 메시지 암호화 기능에서는 Exchange Online에 대 한 Azure Information Protection의 byok가 제공 됩니다.
  
## <a name="does-office-365-message-encryption-and-bring-your-own-key-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Office 365 메시지 암호화를 수행 하 고 Azure Information Protection을 사용 하 여 사용자의 키 가져오기 subpoenas와 같은 타사 데이터 요청에 대 한 Microsoft의 접근 방식을 변경 합니다.
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

아니요. Office 365 메시지 암호화 및 Azure Information Protection (aip)에 대 한 개인 키 (byok)를 제공 하 고 제어 하는 옵션은 사법 기관에 대응 하도록 설계 되지 않았습니다. Office 365 메시지 암호화 온-aip가 내부 또는 외부 규정 준수 의무를 충족 해야 하는 규정 준수 중심 고객을 위해 설계 되었습니다. Microsoft는 고객 데이터에 대 한 타사 요청을 매우 심각 하 게 수행 합니다. 클라우드 서비스 공급자는 항상 고객 데이터에 대 한 개인 정보를 제공 합니다. 소환장이 발생 하는 경우에는 항상 제 3 자가 고객에 게 리디렉션되어 정보를 얻도록 시도 합니다. (정부 Smith의 블로그에서 [고객 데이터 보호 스누핑](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/))를 읽어 보십시오. [여기](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data)에서 받은 요청의 세부 정보를 주기적으로 게시 합니다.
  
자세한 내용은 [온라인 서비스 약관 (OST) ](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx)의 "고객 데이터 공개" 및 타사 데이터 요청과 관련 된 [Microsoft 보안 센터](https://www.microsoft.com/en-us/trustcenter/default.aspx) 를 참조 하세요.
  
## <a name="does-service-encryption-with-customer-key-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>고객 키를 사용한 서비스 암호화는 subpoenas와 같은 타사 데이터 요청에 대 한 Microsoft의 접근 방식을 변경 합니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

아니요. 고객 키가 법률 집행 하위 poenas에 응답 하도록 설계 되지 않았습니다. 이는 규제 고객이 내부 또는 외부 규정 준수 의무를 충족 하도록 설계 되었습니다. Microsoft는 고객 데이터에 대 한 타사 요청을 매우 심각 하 게 수행 합니다. 클라우드 서비스 공급자는 항상 고객 데이터에 대 한 개인 정보를 제공 합니다. 소환장이 발생 하는 경우에는 항상 제 3 자가 고객에 게 리디렉션되어 정보를 얻도록 시도 합니다. (정부 Smith의 블로그에서 [고객 데이터 보호 스누핑](http://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/))를 읽어 보십시오. [여기](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data)에서 받은 요청의 세부 정보를 주기적으로 게시 합니다.
  
자세한 내용은 [온라인 서비스 약관 (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx) 의 "고객 데이터 공개" 및 타사 데이터 요청과 관련 된 [Microsoft 보안 센터](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data) 를 참조 하세요. 
  
## <a name="is-fasttrack-support-available-for-implementing-customer-key"></a>fasttrack에서 고객 키를 구현 하는 데 사용할 수 있나요?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

아니요. fasttrack은 고객 키를 등록 하는 데 필요한 테 넌 트 및 서비스 구성 정보를 수집 하는 경우에만 사용 됩니다. 고객 키 제공은 fasttrack을 통해 게시 되므로 고객 및 파트너가 동일한 방법을 사용 하 여 필요한 정보를 제출 하 고 고객이 제공 하는 데이터를 간편 하 게 보관할 수 있습니다.
  
설명서 외에 추가 지원이 필요한 경우에는 MCS (Microsoft 컨설팅 서비스), pfe (프리미어 현장 엔지니어링) 또는 Microsoft 파트너에 게 문의 하세요.
  
## <a name="if-my-keys-are-destroyed-how-can-i-recover"></a>내 키가 파괴 되 면 어떻게 복구할 수 있나요?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

가용성 키는 관리 하는 루트 키의 예기치 않은 손실에서 복구할 수 있는 기능을 제공 합니다. 루트 키가 손실 되 면 microsoft 지원 서비스에 문의 하 여 가용성 키를 사용 하도록 설정 하는 프로세스를 지원 해 드릴 수 있습니다. 가용성 키를 사용 하 여 사용자가 프로 비전 한 새 키를 사용 하 여 새 데이터 암호화 정책으로 마이그레이션합니다. 
  
## <a name="what-is-the-availability-key"></a>가용성 키는?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

가용성 키는 데이터 암호화 정책을 만들 때 프로 비전 되는 루트 키입니다. 가용성 키는 Office 365 내에서 저장 및 보호 되며, 고객 키에 대 한 서비스 암호화와 함께 사용 하기 위해 제공 되는 두 가지 루트 키와 기능적으로 비슷합니다. Azure 키 자격 증명 모음에서 제공 하 고 관리 하는 키와 달리 가용성 키에 직접 액세스할 수 없습니다. 가용성 키에 대 한 저장소 및 제어는 다음과 같은 세 가지 이유로 인해 고의적으로 azure 키 보관소와는 다릅니다. 먼저 가용성 키는 Office 365 서비스가 Azure 키에 호스트 되는 키에 연결할 수 없는 경우 고가용성 기능을 제공 합니다. 보관소가 둘째로, 두 Azure 키 자격 증명 모음 키가 손실 될 경우 가용성 키가 "중단 유리" 기능을 제공 합니다. 셋째, 논리 컨트롤을 분리 하면 단일 공격이 나 실패 지점에서 모든 키가 손실 되는 것을 방지 하 고 심층 방어를 제공할 수도 있습니다. 키를 보호 하는 데 있어 주요 관리를 위한 다양 한 보호 및 프로세스를 사용 하면서 모든 키 (즉, 데이터)가 손실 되거나 소멸 될 위험을 줄일 수 있습니다. Microsoft는 가용성 키가 소멸 되는 것을 단독으로 제공 합니다. Microsoft의 가용성 키에 대 한 액세스 권한이 있는 아무도 Office 365 서비스 코드 에서만 액세스할 수 있도록 디자인 되어 있습니다.
  
## <a name="how-many-data-encryption-policies-deps-can-i-create"></a>얼마나 많은 데이터 암호화 정책 (deps)을 만들 수 있나요?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online 및 비즈니스용 Skype:** 최대 50 deps를 만들 수 있습니다. 
  
 **SharePoint Online 및 비즈니스용 OneDrive:** DEP는 지리적 위치 (geo 라고도 함)의 데이터에 적용 됩니다. Office 365의 다중 지역 기능을 사용 하는 경우에는 각 지역에 따라 하나의 DEP를 만들 수 있습니다. 다중 geo를 사용 하지 않는 경우에는 하나의 DEP를 만들 수 있습니다.
  
## <a name="can-i-assign-a-data-encryption-policy-before-migrating-a-mailbox-to-the-cloud"></a>사서함을 클라우드로 마이그레이션하기 전에 데이터 암호화 정책을 할당할 수 있나요?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

예. Windows PowerShell cmdlet 설정-mailuser를 사용 하 여 사서함을 Office 365로 마이그레이션하기 전에 사용자에 게 DEP (데이터 암호화 정책)를 할당할 수 있습니다. 이렇게 하면 콘텐츠가 마이그레이션될 때 할당 된 DEP를 사용 하 여 사서함의 내용이 암호화 됩니다. 이 방법을 사용 하면 사서함이 이미 마이그레이션된 후에 DEP를 할당 하는 것 보다 더 효율적으로 수행할 수 있으며,이 경우 암호화가 수행 되기를 기다린 후 시간이 나 일이 걸릴 수 있습니다. 
  
## <a name="how-do-i-verify-that-encryption-with-customer-key-is-activated-and-office-365-has-finished-encrypting-with-customer-key"></a>고객 키를 사용한 암호화가 정품 인증 되 고 Office 365에서 고객 키 암호화가 완료 되었는지 확인 하는 방법은 무엇 인가요?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online 및 비즈니스용 Skype:** [원격 PowerShell을 사용 하 여 Exchange Online에 연결한](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) 다음 확인할 각 사서함에 대해 **[get-mailboxstatistics]** cmdlet을 사용할 수 있습니다. get-mailboxstatistics cmdlet의 출력에서 _IsEncrypted_ 속성은 사서함이 암호화 된 경우 **true** 값을 반환 하 고 그렇지 않은 경우 **false** 값으로 설정 합니다. 사서함이 암호화 된 경우 _dataencryptionpolicyid_ 속성에 대해 반환 되는 값은 사서함이 암호화 된 DEP의 GUID입니다. 이 cmdlet을 실행 하는 방법에 대 한 자세한 내용은 [Get-get-mailboxstatistics](https://technet.microsoft.com/en-us/library/bb124612%28v=exchg.160%29.aspx) 및 using PowerShell with Exchange Online을 참조 하세요. 
  
사서함이 DEP를 할당 한 시간부터 72 시간을 기다린 후 암호화 되지 않으면 사서함 이동을 시작 합니다. 이렇게 하려면 [원격 PowerShell을 사용 하 여 Exchange Online에 연결한](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) 다음 new-moverequest cmdlet을 사용 하 여 다음과 같이 사서함의 별칭을 제공 합니다. 
  
```
New-MoveRequest <alias>
```

 **SharePoint Online 및 비즈니스용 OneDrive:** [SharePoint Online PowerShell에 연결한](https://technet.microsoft.com/en-us/library/fp161372.aspx)다음 **[SPODataEncryptionPolicy]** cmdlet을 사용 하 여 테 넌 트의 상태를 확인할 수 있습니다. 고객 키 암호화가 사용 되 고 모든 사이트의 모든 파일이 암호화 된 경우 * * _State_* * 속성은 **등록** 값을 반환 합니다. 암호화가 아직 진행 중인 경우이 cmdlet은 완료 된 사이트 비율에 대 한 정보를 제공 합니다. 
  
## <a name="if-i-want-to-switch-to-a-different-set-of-keys-how-long-does-it-take-for-the-new-set-of-keys-to-protect-my-data"></a>다른 키 집합으로 전환 하려는 경우에는 데이터를 보호 하기 위해 새 키 집합에 어떤 시간이 걸립니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online 및 비즈니스용 Skype:** 새 dep가 사서함에 할당 된 시간부터 새 dep (데이터 암호화 정책)에 따라 사서함을 보호 하는 데 최대 72 시간이 걸릴 수 있습니다. 
  
 **SharePoint Online 및 비즈니스용 OneDrive:** 새 키가 할당 되 면 전체 테 넌 트를 다시 암호화 하는 데 최대 4 시간이 걸릴 수 있습니다. 
  
## <a name="is-my-existing-data-stored-without-encryption-at-any-time-while-it-is-decrypted-or-encrypted-with-customer-key"></a>고객 키를 사용 하 여 암호를 해독 하거나 암호화 한 경우 언제 든 지 기존 데이터를 암호화 없이 저장 합니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

아니요. 데이터는 항상 BitLocker 및 DKM를 사용 하는 Office 365 서비스의 나머지 부분에서 암호화 됩니다. 자세한 내용은 "Office 365의 보안, 개인 정보 및 준수 정보" 및 [Exchange Online에서 전자 메일 암호를 보호 하는 방법을](https://support.office.com/article/989BA10C-F73F-4EFB-AD1B-AF3322E5F376)참조 하세요.
  
## <a name="if-i-no-longer-want-to-use-customer-managed-encryption-keys-can-i-switch-to-microsoft-managed-keys"></a>고객 관리 암호화 키를 더 이상 사용 하지 않으려는 경우 Microsoft 관리 되는 키로 전환할 수 있나요?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online 및 비즈니스용 Skype:** 아직 아니에요. 이 기능은 Office 365에서 Microsoft 관리 키가 포함 된 서비스 암호화가 광범위 하 게 수행 되는 경우 지원 됩니다. 고객 키를 사용 하 여 서비스 암호화를 해제 한 후 서비스에서이를 롤아웃할 것으로 기대 합니다. 
  
 **SharePoint Online 및 비즈니스용 OneDrive:** 예로. 다중 지역 기능을 사용 하는 경우에는 각 지역에 대해 Microsoft 관리 키를 별도로 사용 하거나 단일 지리적에 있는 모든 데이터에 대해 개별적으로 되돌리기를 선택할 수 있습니다. 
  
## <a name="if-i-lose-my-keys-how-long-does-it-take-to-recover-service-availability-using-the-recovery-key"></a>키를 잃어 버리면 복구 키를 사용 하 여 서비스 가용성을 복구 하는 데 어느 정도의 시간이 걸립니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online 및 비즈니스용 Skype:** 가용성 키를 사용 하기 위해 전화를 걸려면 몇 분 내에 사서함에 액세스할 수 있습니다. 
  
 **SharePoint Online 및 비즈니스용 OneDrive:** 이 작업은 보유 하 고 있는 사이트 수에 비례 합니다. Microsoft에 전화를 걸어 가용성 키를 사용 하는 경우 약 4 시간 이내에 완벽 하 게 온라인 상태가 됩니다. 
  
## <a name="how-is-the-availability-key-used-with-exchange-online"></a>Exchange Online에서 가용성 키를 사용 하는 방법
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

가용성 키를 Exchange Online과 함께 사용 하는 방법에는 세 가지가 있습니다.
  
- Azure 키 자격 증명 모음 키에 연결할 수 없는 경우 서비스 가용성이 제공 됩니다.
    
- Office 365 서비스 코드에서 시작 된 작업 (예: 검색 인덱스 만들기 또는 사서함 이동)
    
- 단일 DEP와 연결 된 두 Azure 키 자격 증명 키 손실 같은 키 손실에서 복구 합니다.
    
 **Azure key Vault 키에서 서비스 가용성에 대 한 가용성 키를 사용할 수 없습니다.**
  
Office 365에서는 가용성 키를 사용 하 여 서비스 가용성과 Exchange Online에 대 한 비정상 고객 키 상태 로부터의 복구를 모두 지원 합니다. 고객 키에 사용 되는 키 계층 구조가 있습니다. 다음 그림에서는이 계층 구조를 보여 줍니다.
  
![](media/a760156b-737f-469a-80ab-c28b7a8b9160.png)
  
단일 DEP (데이터 암호화 정책)의 Azure 키 보관소 키를 모두 사용할 수 없으면 Office 365에서 가용성 키를 사용 하 여 새 dep로 변경할 수 있습니다. Office 365에서는 사용자가 시작한 활동 (예: 사용자가 Outlook 클라이언트에 전자 메일을 다운로드 하는 경우)이 든, 인덱싱 등의 시스템 시작 활동에 따라 서비스 가용성을 위해 가용성 키를 사용할지 여부를 결정 합니다. 사서함 콘텐츠 또는 eDiscovery 검색에 대해 프로세스를 트리거 했습니다.
  
사용자 사서함에 대 한 가용성 키를 사용할지 여부를 결정 하기 위해 사용자가 시작한 작업에 대 한 응답으로 Office 365에서이 프로세스를 팔 로우 합니다.
  
1. Office 365에서는 Azure 키 자격 증명 모음에서 두 고객 키의 위치를 확인 하기 위해 사서함이 할당 되는 DEP를 읽습니다.
    
2. Office 365은 dep에서 두 개의 고객 키 중 하나를 선택 하 고 Azure key Vault에 요청을 보내 고객 키를 사용 하 여 DEP 키를 래핑 해제 합니다.
    
3. 고객 키를 사용 하 여 DEP 키의 래핑을 해제 하는 요청이 실패 하 고 오류가 반환 되 면 Office 365에서 Azure 키 보관소에 두 번째 요청을 전송 하 여 대체 (두 번째) 고객 키를 사용 하도록 지시 합니다.
    
4. 고객 키를 사용 하 여 DEP 키의 래핑을 해제 하 라는 두 번째 요청이 실패 하 고 오류를 반환 하는 경우 Office 365에서 두 요청의 결과를 검사 합니다.
    
  - 검사 결과, 오류에 따라 고객 id의 명시적 동작이 반영 되지 않는 것으로 확인 되 면 Office 365에서 availability 키를 사용 하 여 DEP 키를 해독 합니다. 그런 다음이 DEP 키를 사용 하 여 사서함 키의 암호를 해독 하 고 사용자 요청을 완료 합니다.
    
    이 경우 Azure 키 자격 증명 모음이 어떤 이유로 든 응답할 수 없거나 연결이 불가능 합니다. Office 365에서는 고객이 키에 대 한 액세스를 의도적으로 취소 했는지 여부를 확인할 수 없습니다.
    
  - 조사 결과, 고객 키를 사용 하지 않도록 의도적으로 작업을 수행 했음을 나타내는 경우에는 가용성 키를 사용할 수 없으며 사용자 요청이 실패 하 고 사용자에 게 로그인 오류와 같은 오류 메시지가 표시 됩니다.
    
    이 경우 고객은 서비스가 영향을 받게 되 고 고객 키의 조건이 비정상 임을 알게 된다는 것을 알 수 있습니다. 예를 들어 고객이 조직의 모든 사서함에 대해 단일 DEP를 사용 하는 경우 고객이 사용자의 사서함에 액세스할 수 없는 경우 광범위 한 오류가 발생할 수 있습니다. 이렇게 하면 고객 키가 비정상 상태가 되 면 고객은 상황을 수정 하 고 서비스를 정상 상태로 복원할 필요성을 알게 됩니다.
    
 **Office 365 서비스 코드에서 시작 하는 작업에 대 한 가용성 키 사용**
  
Office 365 서비스 코드는 항상 유효한 로그인 토큰을 가지 며 차단 될 수 없습니다. 따라서 가용성 키가 삭제 될 때까지 검색 인덱스 만들기 또는 사서함 이동과 같은 Office 365 서비스 코드로 시작 되는 작업에 사용할 수 있습니다.
  
 **가용성 키를 사용 하 여 키 손실 복구**
  
가용성 키를 사용 하 여 FAQ 항목 "키가 소멸 됩니다."를 복구할 수 있습니까? "에 설명 된 것 처럼 동일한 DEP와 연결 된 두 Azure 키 자격 증명 키가 손실 되는 것을 복구할 수 있습니다.
  
## <a name="how-is-the-availability-key-used-with-sharepoint-online-and-onedrive-for-business"></a>SharePoint Online 및 비즈니스용 OneDrive에서 가용성 키를 사용 하는 방법은 무엇 인가요?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

고객 키 및 가용성 키에 대 한 SharePoint online 및 비즈니스용 OneDrive 아키텍처 및 구현은 Exchange online 및 비즈니스용 Skype와 다릅니다.
  
고객이 사용자가 관리 하는 키로 이동 하면 Office 365에서 테 넌 트 관련 중간 키 (tik)를 만듭니다. Office 365에서는 각 고객 키와 함께 tik를 두 번 암호화 하 고 두 가지 암호화 버전의 tik를 저장 합니다. 암호화 된 버전의 tik만 저장 되 고, tik는 customer 키로만 암호를 해독할 수 있습니다. 그런 다음 tik는 사이트 키를 암호화 하는 데 사용 되며, blob 키를 암호화 하는 데 사용 됩니다. blob는 Microsoft Azure Blob 저장소 서비스에 암호화 되 고 저장 됩니다.
  
Office 365에서 다음 프로세스를 수행 하 여 고객 파일 데이터가 있는 blob에 액세스 합니다.
  
1. 고객 키를 사용 하 여 tik의 암호를 해독 합니다.
    
2. 암호 해독 된 tik를 사용 하 여 사이트 키의 암호를 해독 합니다.
    
3. 암호 해독 된 사이트 키를 사용 하 여 blob 키를 해독 합니다.
    
4. 해독 된 blob 키를 사용 하 여 blob 암호를 해독 합니다.
    
tik를 해독할 때 Office 365은 약간의 오프셋을 사용 하 여 Azure 키 자격 증명 모음에 두 개의 암호 해독 요청을 보냅니다. 처음에는 검색을 완료 하 여 결과를 제공 다른 요청을 취소 합니다.
  
고객이 고객 키에 대 한 액세스 권한을 상실 하는 경우에도 Office 365에서 사용 가능한 키를 사용 하 여 tik를 암호화 하 고 각 고객 키로 암호화 된 tik와 함께이를 저장 합니다. 가용성 키를 사용 하 여 암호화 된 tik는 고객이 악의적으로 또는 실수로 키에 대 한 액세스 권한을 손실 했을 때 복구 경로를 등록 해야 하는 경우에만 사용 됩니다.
  
가용성 및 확장 상의 이유로, 암호 해독 된 tiks는 시간 제한 메모리 캐시에 캐시 됩니다. tik 캐시가 만료 되도록 설정 되기까지 두 시간이 소요 되 면 Office 365에서 각 tik를 해독 하려고 시도 합니다. tiks를 해독 하면 캐시의 수명이 연장 됩니다. tik 암호 해독에 실패 하는 경우, Office 365는 캐시 만료 전에 엔지니어링에 알리기 위한 경고를 생성 합니다. 고객이 microsoft에서 전화를 건 경우에만 Office 365에서 복구 작업을 시작 하며, microsoft는 암호 해독 된 tik 및 새 집합을 사용 하 여 해당 사용자의 비밀 저장소에 저장 된 가용성 키로 tik를 해독 하 고 테 넌 트를 다시 보 딩 합니다. 고객이 제공한 Azure 키 보관소 키
  
현재로 서는 고객 키가 Azure blob 저장소에 저장 된 sharepoint online 파일 데이터의 암호화 및 암호 해독 체인에 포함 되지만 sharepoint online 목록 항목이 나 SQL 데이터베이스에 저장 된 메타 데이터는 제외 됩니다. Office 365에서는 고객이 시작한 위에 설명 된 사례를 제외 하 고 SharePoint Online 또는 비즈니스용 OneDrive에 대 한 가용성 키를 사용 하지 않습니다. 고객 데이터에 대 한 사용자 액세스는 고객 Lockbox에 의해 보호 됩니다.
  
## <a name="how-is-customer-key-licensed"></a>고객 키의 사용이 허가 되는 이유
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

고객 키는 Office 365 Enterprise 제품군, "E5" 및 고급 규정 준수 SKU에서 제공 됩니다. 또한 고객은 Azure 키 자격 증명 모음을 사용 하 여 적절 한 라이선스를 구입 해야 합니다.
  
고객 키를 사용 하 여 고객 키를 포함 하려면 각 사용자에 게 benefiting를 부여 해야 합니다.
  
SharePoint Online의 경우, 설치 단계를 수행 하려면 고객 키를 구성 하는 Office 365 관리자에 게 라이선스가 부여 되어야 합니다. 또한이 기능을 사용 하 여 benefiting 사용자에 게 라이선스를 부여 해야 합니다. 여기에는 사이트 소유자 및 고객 키를 통해 암호화 된 하나 이상의 사이트에 있는 파일에 액세스 하는 사용자가 포함 됩니다. 외부 사용자는 고객 키를 사용 하 여 암호화 된 하나 이상의 사이트에 있는 파일에 액세스 하기 위해 사용이 허가 되지 않아도 됩니다.
  
Exchange Online의 경우 "사용자" 사서함 및 "메일 사용자" 사서함의 사용이 허가 되어야 합니다. 공유 사서함과 같은 다른 모든 사용자는 고객 키에 대 한 라이선스를 가질 필요가 없습니다. Exchange Online 사서함이 올바르게 사용이 허가 되었는지 확인 하려면 다음 cmdlet을 실행 합니다.
  
```
(Get-Mailbox <alias >).PersistedCapabilities
```

문자열 BPOS_S_EquivioAnalytics 있으면 사서함이 적절 하 게 사용 허가 된 것입니다. 그렇지 않은 경우에는이 사서함에 대 한 고객 키 기능을 사용 하기 위해 적절 한 라이선스를 적용 해야 합니다.
  
## <a name="can-i-enable-customer-key-for-a-trial-subscription"></a>평가판 구독에 대해 고객 키를 사용 하도록 설정할 수 있습니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

아니요. 정의에 따라 평가판 구독은 수명이 제한 됩니다. 평가판 구독에서 호스트 되는 암호화 키는 평가판 수명 종료 시 손실 될 수 있습니다. Microsoft는 고객이 중요 한 고객 데이터를 평가판 구독에 저장 하는 것을 허용 하거나 방지할 수 없기 때문에, 평가판 구독과 함께 고객 키를 사용 하는 것은 금지 됩니다.
  
## <a name="how-much-will-using-customer-key-cost"></a>고객 주요 비용을 얼마나 많이 사용 하나요?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

고객 키에 필요한 라이선스 외에도, 고객은 키 자격 증명 사용에 대 한 비용을 초래 하 게 됩니다. [Azure Key Vault 가격 세부 정보](https://azure.microsoft.com/en-us/pricing/details/key-vault/) 비용 모델을 기술 하 고 예측을 지원 합니다. 사용 패턴이 다르기 때문에 고객에 게 발생 하는 정확한 비용을 예측할 수 있는 방법은 없습니다. 이 비용은 비용이 매우 낮고, 일반적으로 매달 사용자 당 $0.005의 범위와 HSM에서 지 원하는 키 비용을 더한 것을 보여 줍니다. 이 비용은 고객이 선택한 로깅 구성과 azure 키 자격 증명 모음 로그에 사용 되는 azure 저장소의 크기에 따라 달라 집니다. 
  
## <a name="for-more-information"></a>자세한 내용
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

고객 키를 시작 하려면 [Office 365에서 고객 키를 사용 하 여 데이터 제어](controlling-your-data-using-customer-key.md)를 참조 하세요.
  

