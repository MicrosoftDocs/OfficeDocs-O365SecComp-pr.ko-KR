---
title: Office 365의 고객 키를 사용한 서비스 암호화 FAQ
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/31/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 41ae293a-bd5c-4083-acd8-e1a2b4329da6
description: 초기 계획 BitLocker 및 배포 된 키 관리자 (DKM)을 통해 사용할 수 있는 볼륨 수준 암호화 외에도 Office 365 제공 추가 Exchange에서 데이터를 포함 하 여 Office 365의 고객 콘텐츠에 대 한 응용 프로그램 수준에서 암호화 계층 온라인으로 비즈니스, SharePoint Online, 및 비즈니스용 OneDrive에 대 한 Skype 합니다. 이 서비스 암호화를 라고 합니다.
ms.openlocfilehash: ceba35233872bb65b7706ed4e11a263057adc6c1
ms.sourcegitcommit: 659b5f5b38ef7e838cdb44eaa38c18e48d922768
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2018
ms.locfileid: "25575332"
---
# <a name="service-encryption-with-customer-key-for-office-365-faq"></a>Office 365의 고객 키를 사용한 서비스 암호화 FAQ

초기 계획 BitLocker 및 배포 된 키 관리자 (DKM)을 통해 사용할 수 있는 볼륨 수준 암호화 외에도 Office 365 제공 추가 Exchange에서 데이터를 포함 하 여 Office 365의 고객 콘텐츠에 대 한 응용 프로그램 수준에서 암호화 계층 온라인으로 비즈니스, SharePoint Online, 및 비즈니스용 OneDrive에 대 한 Skype 합니다. 이 서비스 암호화를 라고 합니다.
  
고객 키는 서비스 암호화에 기반 하 고를 제공할 수 있습니다 및 [온라인 서비스 약관 (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx)의 설명에 따라 Office 365의 나머지 부분에서 데이터를 암호화 하는데 사용 되는 컨트롤 키를 활성화 합니다. 고객 키를 사용 하면 Office 365를 사용 하 여 데이터를 암호 해독의 암호화 키를 제어 하기 때문에 규정 준수 의무를 충족 합니다.
  
고객 키로 이동한 다음 설명서를 포함 하 여에 의견을 제공 하려면 customerkeyfeedback@microsoft.com를 아이디어, 제안, 및 측면을 보냅니다.
  
## <a name="what-is-service-encryption-with-customer-key"></a>고객 키를 사용 하 여 서비스 암호화 란?

고객 키의 주요 준비 클라우드 서비스 공급자를 지정 하는 규정 준수 요구 사항 요구 사항을 만족 하는 조직의의 기능을 향상 시킵니다. 고객 키를 사용 하 제공 하 고 프로그램 Office 365 데이터에서-나머지 응용 프로그램 수준에 대 한 암호화 키를 제어 합니다. 결과적으로 제어를 실행 하는 및 서비스를 종료 하려는 조직의 키를 취소할 수 있습니다. 키를 취소 하 여 데이터 서비스에 읽을 수 있는있지 않습니다. 주요 해지는 데이터 삭제 향해 경로에서 첫번째 단계입니다.

## <a name="what-office-365-data-at-rest-is-covered-by-customer-key"></a>고객 키에 포함 되는 나머지 부분에서 Office 365 데이터?
<a name="WhatDataIsCoveredbyCustomerKey"> </a>

SharePoint Online 사이트 콘텐츠 및 해당 사이트에 저장 된 파일 및 비즈니스용 OneDrive에 업로드 된 파일에 적용 됩니다. Exchange Online 사서함 콘텐츠 (전자 메일 본문, 일정 항목 및 전자 메일 첨부 파일의 콘텐츠) 다룹니다. 비즈니스를 위한 Skype에서 텍스트 대화를 처리 하지만 Skype 모임 브로드캐스트 녹음/녹화 및 Skype 모임 콘텐츠 업로드 다루지 않습니다. 파일이 Office 365의 다른 모든 콘텐츠와 함께 Skype 모임 브로드캐스트 및 Skype 모임 콘텐츠 업로드 암호화 되지만 현재 암호화 키의 고객 제어를 제공 하지 않습니다.
  
## <a name="what-is-the-difference-between-customer-key-and-bring-your-own-key-byok-with-azure-information-protection-for-exchange-online"></a>고객 키와 가져올 Your 고유한 키 (BYOK)와 Exchange Online에 대 한 정보 보호 Azure의 차이점은 무엇입니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

두 옵션을 사용 하면 제공 하 고 컨트롤 직접 암호화 키입니다. 그러나 고객 키를 사용 하 여 서비스 암호화 Exchange Online에 대 한 Azure 정보 보호와 BYOK 사용자 데이터-전송 중인을 암호화 하 고 온라인 및 오프 라인으로 영구를 제공 하는 동안 Office 365 서버에서-rest에 거주 하는 나머지 부분에서 데이터를 암호화 하는 전자 메일 메시지와 Office 365에 대 한 첨부 파일에 대 한 보호 합니다. 고객 키와 Exchange Online에 대 한 Azure 정보 보호와 BYOK는 보완 하는 및 나머지 부분에서 데이터 및 전송 중에 암호화에서 추가 된 보호를 제공할 수 Microsoft의 서비스 관리 되는 키 또는 고유한 키를 사용 하 든 악의적인 공격입니다.
  
Exchange Online에 대 한 Azure 정보 보호와 BYOK Office 365 메시지 암호화 기능에서 제공 됩니다.
  
## <a name="does-office-365-message-encryption-and-bring-your-own-key-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Office 365 메시지 암호화 및 Azure 정보 보호를 사용 하 여 사용자 고유의 키 가져오는 변경지 않습니다 Microsoft 방법을 subpoenas 예: 제 3 자 데이터 요청에?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

아니요. Office 365 메시지 암호화 및 옵션을 제공 하 고 Azure 정보 보호 (AIP)에 대 한 직접 암호화 키와 가져올 사용자 고유의 키 (BYOK)을 제어 하는 법률 적용 subpoenas에 응답 하도록 설계 되지 않았습니다. AIP에 대 한 BYOK 사용 하 여 office 365 메시지 암호화가 내부 또는 외부 규정 준수 의무를 충족 하는 준수 초점을 맞춘 고객을 위해 설계 되었습니다. Microsoft는 매우 심각 하 게 고객 데이터에 대 한 타사 요청을 수행합니다. 클라우드 서비스 공급자로 항상 담당 고객 데이터의 개인정보 보호 합니다. 이벤트는 이벤트에 모두를 소환장 적용 됩니까, 제 3 자 정보를 가져올 고객에 게 착신 전환 하려고 항상 했습니다. (Brad Smith의 블로그 (영문)를 참조 하십시오: [정부 스누핑의 고객 데이터를 보호](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). 접수 요청의 자세한 정보를 주기적으로 게시는 [여기](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data)합니다.
  
제 3 자 데이터 요청에 대 한 [Microsoft 보안 센터](https://www.microsoft.com/en-us/trustcenter/default.aspx) 및 "공개 고객에서에서 데이터의" 자세한 정보에 대 한 [온라인 서비스 약관 (OST)를 ](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx)참조 하십시오.
  
## <a name="does-service-encryption-with-customer-key-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>고객 키를 사용 하 여 서비스 암호화 subpoenas 예: 제 3 자 데이터 요청을 Microsoft의 접근 방식 변경 됩니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

아니요. 고객 키가 법률 적용 subpoenas에 응답 하도록 설계 되지 않았습니다. 자신의 내부 또는 외부 규정 준수 의무를 충족 하기 위해 규제 고객을 위해 설계 되었습니다. Microsoft는 매우 심각 하 게 고객 데이터에 대 한 타사 요청을 수행합니다. 클라우드 서비스 공급자로 항상 담당 고객 데이터의 개인정보 보호 합니다. 이벤트는 이벤트에 모두를 소환장 적용 됩니까, 제 3 자 정보를 가져올 고객에 게 착신 전환 하려고 항상 했습니다. (Brad Smith의 블로그 (영문)를 참조 하십시오: [정부 스누핑의 고객 데이터를 보호](http://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). 접수 요청의 자세한 정보를 주기적으로 게시는 [여기](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data)합니다.
  
제 3 자 데이터 요청에 대 한 [Microsoft 보안 센터](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data) 및 "공개 고객에서에서 데이터의" 자세한 정보에 대 한 [온라인 서비스 약관 (OST)를](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx) 참조 하십시오. 
  
## <a name="is-fasttrack-support-available-for-implementing-customer-key"></a>FastTrack 지원은 고객 키를 구현 하는데 사용할 수 있습니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

아니요. FastTrack만 고객 키에 대 한 등록에 필요한 테 넌 트 및 서비스 구성 정보를 수집 하는데 사용 됩니다. 고객 키 제공 하는 것이 편리 하 고 고객의 제안에 제공 하는 데이터를 보관 편의 위해 동일한 메서드를 사용 하 여이 필요한 정보를 전송 하는 고객 및 파트너에 대 한 FastTrack을 통해 게시 됩니다.
  
설명서 외 추가 지원이 필요 하면 Microsoft Consulting Services (MCS), 프리미어 필드 엔지니어링 (PFE), Microsoft 파트너에 문의 합니다.
  
## <a name="if-my-keys-are-destroyed-how-can-i-recover"></a>내 키 손상 된 경우 어떻게 합니까 복구할 수 있습니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

가용성 키를 관리 하는 루트 키의 예상 하지 못한 손실에서 복구 하는 기능을 제공 합니다. 루트 키를 분실 하면 연락처 Microsoft 기술 지원 서비스 및 Microsoft는 도움을 가용성 키를 사용 하도록 설정 하는 프로세스를 통해 합니다. 가용성 키를 사용 하 여 사용자가 프로 비전 하는 새 키를 사용 하 여 새 데이터 암호화 정책으로에 표시 됩니다. 
  
## <a name="what-is-the-availability-key"></a>가용성 키 란 무엇입니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

가용성 키는 데이터 암호화 정책을 만들 때 구축 되는 루트 키입니다. 가용성 키 저장 되 고 Office 365 내에서 보호 및 고객 키로 암호화 서비스와 함께 사용 하기 위해 사용자에 의해 제공 되는 두 루트 키와 기능적으로 비슷합니다. 제공 하 고 Azure 키 추적용에서 관리 하는 키와는 달리 가용성 키를 직접 액세스할 수 없습니다. 저장소 및 가용성 키의 컨트롤은 신중 하 게 다른 세 이유로 Azure 키 추적용 키: Office 365 서비스를 키 Azure 키에 호스트에 연결할 수 없습니다는 가용성 키 고가용성 기능을 제공 하는 첫째, 추적용; 두 Azure 키 추적용 키는 손실;는 가용성 키 "유리 중단" 기능을 제공 하는 둘째, 및 셋째, 논리적 컨트롤의 분리 심층 방어를 제공 하는 단일 공격에서 모든 키의 손실 또는 오류 지점으로를 보호 합니다. 모든 키 (및 따라서 데이터) 손실 되거나 될 소멸 위험을 줄일 수 궁극적으로 키 관리에 대 한 다양 한 보호와 프로세스를 사용 하는 동안 키를 보호 하기 위해 책임을 공유 합니다. Microsoft은 가용성 키의 폐기를 통해 유일한 인증 기관을 제공합니다. 설계상, 가용성 키에 대 한 액세스는 Microsoft에서 아무도-Office 365 서비스 코드에서 액세스할 수만 됩니다.
  
## <a name="how-many-data-encryption-policies-deps-can-i-create"></a>얼마나 많은 데이터 암호화 정책 (DEPs)을 만들 수 있나요?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online 및 비즈니스를 위한 Skype:** 최대 50 개의 DEPs를 만들 수 있습니다. 
  
 **SharePoint Online 및 비즈니스용 OneDrive:** 한 DEP를 지리적으로 분산이 라고도 하는 하나의 지리적 위치에 데이터에 적용 됩니다. Office 365의 다중-지리적으로 분산 기능을 사용 하는 경우에 지리적으로 분산 당 하나의 DEP를 만들 수 있습니다. 다중-지리적으로 분산을 사용 하지 않는 경우에 하나의 종속을 만들 수 있습니다.
  
## <a name="can-i-assign-a-data-encryption-policy-before-migrating-a-mailbox-to-the-cloud"></a>클라우드로 사서함을 마이그레이션하기 전에 데이터 암호화 정책 할당
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

예입니다. Office 365로 사서함을 마이그레이션하기 전에 사용자에 게 (DEP) 데이터 암호화 정책을 할당 하려면 Set-mailuser Windows PowerShell cmdlet을 사용할 수 있습니다. 이렇게 하면 콘텐츠를 마이그레이션할 때 할당 된 DEP를 사용 하 여 사서함의 내용에 암호화 됩니다. 이 사서함 이미 마이그레이션된 후에 DEP를 할당 하 고 다음을 수행할 수 시간 또는 걸릴 가능한 경우 일 하는 암호화 될 때까지 기다리지 보다 더 효율적일 수 있습니다. 
  
## <a name="how-do-i-verify-that-encryption-with-customer-key-is-activated-and-office-365-has-finished-encrypting-with-customer-key"></a>고객 키를 사용 하 여 암호화가 활성화 하 고 Office 365 고객 키로 암호화 완료를 확인을 수행 하는 방법
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online 및 비즈니스를 위한 Skype:** [원격 PowerShell을 사용 하는 Exchange Online에 연결할](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) 수 있는 한 다음 확인 하려는 각 사서함에 대 한 **[Get-mailboxstatistics]** cmdlet을 사용 합니다. Get-mailboxstatistics cmdlet의 출력에서 _IsEncrypted_ 속성 하지 않으면 값이 **true** 이면 사서함 암호화 하 고 **false** 값을 반환 합니다. 사서함을 암호화 하는 경우 _DataEncryptionPolicyID_ 속성에 대 한 반환 값은 사서함은 암호화 DEP의 GUID입니다. 이 cmdlet을 실행에 대 한 자세한 내용은 [Get-mailboxstatistics](https://technet.microsoft.com/en-us/library/bb124612%28v=exchg.160%29.aspx) 및 Exchange online PowerShell을 사용 하 여를 참조 하십시오. 
  
사서함은 DEP를 할당 하는 시간에서 72 시간을 기다린 후 암호화 되지 않은 경우에 사서함 이동을 시작 합니다. [원격 PowerShell을 사용 하는 Exchange Online에 연결](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) 이 작업을 수행 하 고 다음 New-moverequest cmdlet을 사용 하 고 사서함의 별칭을 다음과 같이 제공을: 
  
```
New-MoveRequest <alias>
```

 **SharePoint Online 및 비즈니스용 OneDrive:** [SharePoint Online PowerShell에 연결할](https://technet.microsoft.com/en-us/library/fp161372.aspx)수 있는 다음 **[Get-SPODataEncryptionPolicy]** cmdlet을 사용 하 여 테 넌 트의 상태를 확인 합니다. * * _상태_* * 속성 고객 키 암호화를 사용 하 고 모든 사이트의 모든 파일을 암호화 하는 경우 **등록** 값을 반환 합니다. 암호화는 계속 진행 하는 경우이 cmdlet의 사이트는 몇 % 완료 되에 정보를 제공 합니다. 
  
## <a name="if-i-want-to-switch-to-a-different-set-of-keys-how-long-does-it-take-for-the-new-set-of-keys-to-protect-my-data"></a>다른 키 집합으로 전환 원할 않습니다 걸리는 키의 새 집합에 대 한 내 데이터를 보호 하기 위해?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online 및 비즈니스를 위한 Skype:** 새 DEP 사서함에 할당 된 시간에서에 따라을 새 암호화 정책 DEP (데이터) 사서함을 보호 하기 위해 72 시간까지 걸릴 수 있습니다. 
  
 **SharePoint Online 및 비즈니스용 OneDrive:** 새 키가 할당 된 후 전체 테 넌 트를 다시 암호화 하려면 4 시간까지 걸릴 수 있습니다. 
  
## <a name="is-my-existing-data-stored-without-encryption-at-any-time-while-it-is-decrypted-or-encrypted-with-customer-key"></a>내 기존 데이터 저장 되어 언제 든 지를 암호화 하지 않고 암호를 해독 되었거나 고객 키를 사용 하 여 암호화 하는 동안 있습니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

아니요. 데이터는 BitLocker 및 DKM 사용 하 여 Office 365 서비스의 나머지 부분에서 항상 암호화 됩니다. 자세한 내용은 "보안, 개인 정보 및 Office 365에 대 한 준수 정보"를 참조 [방법을 Exchange Online 전자 메일 암호의 보안을 유지](https://support.office.com/article/989BA10C-F73F-4EFB-AD1B-AF3322E5F376)하 고 있습니다.
  
## <a name="if-i-no-longer-want-to-use-customer-managed-encryption-keys-can-i-switch-to-microsoft-managed-keys"></a>Microsoft에서 관리 하는 키를 더이상 고객 관리 되는 암호화 키를 사용 하 여 하려면 I를 전환할 수 있습니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online 및 비즈니스를 위한 Skype:** 아직 아니에요. Microsoft에서 관리 하는 키를 사용 하 여 Office 365에서 서비스 암호화 광범위 하 게 롤아웃 되 면이 지원 됩니다. 전체이 서비스의 고객 키가 있는 서비스 암호화를 해제 한 후 예정입니다. 
  
 **SharePoint Online 및 비즈니스용 OneDrive:** 예입니다. 사용 하 여 Microsoft에서 관리 하는 키 개별적으로 또는 모든 데이터 (다중-지리적으로 분산 기능을 사용 하는 경우) 하는 경우 각 지리적으로 분산에 대 한 단일 geo에 있으면 되돌릴 수 있습니다. 
  
## <a name="if-i-lose-my-keys-how-long-does-it-take-to-recover-service-availability-using-the-recovery-key"></a>내 키를 분실 I 않습니다 걸리는 복구 키를 사용 하 여 서비스 가용성을 복구 하 시겠습니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online 및 비즈니스를 위한 Skype:** 가용성 키를 사용 하 여 호출 되 면 사서함 액세스할 수 분 이내입니다. 
  
 **SharePoint Online 및 비즈니스용 OneDrive:** 이 작업은 있는 사이트 수에 비례 합니다. 가용성 키를 사용 하 여 Microsoft를 호출 하면 되 면 약 4 시간 내에서 완벽 하 게 온라인 수 있습니다. 
  
## <a name="how-is-the-availability-key-used-with-exchange-online"></a>Exchange Online과 가용성 키를 사용 하는 방법
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

세 가지 방법으로 가용성 키를 사용 하는 Exchange Online과:
  
- 서비스 가용성-는 Azure 키 추적용 키에 연결할 수 없습니다.
    
- Office 365 서비스 코드에 의해-검색 인덱스를 만드는 예: 작업 시작 또는 사서함 이동 합니다.
    
- 단일 종속와 연결 된 두 Azure 키 추적용 키 손실과 같은 주요 손실-에서 복구
    
 **Azure 키 추적용 키에 연결할 수 없는 이벤트에 가용성 키를 사용 하 여 서비스 가용성에 대 한 합니다.**
  
Office 365 모두 서비스 가용성 및 비정상 고객 키 상태에서 복구에 대 한 가용성 키를 사용 하 여 Exchange Online에 대 한 합니다. 고객 키로 사용 되는 키의 계층 구조가 있습니다. 이 계층 구조는 다음 그림에 나와 있습니다.
  
![](media/a760156b-737f-469a-80ab-c28b7a8b9160.png)
  
Office 365 사용 가능 여부를 사용할 수 두 Azure 키 추적용 키의 한 단일 암호화 정책 DEP (데이터)을 사용할 수 없는 경우 새 종속 Office 365로 변경 하는 키 여부에 따라 다르게 서비스 가용성에 대 한 가용성 키를 사용 하 여 여부를 결정 한 사용자 시작 작업 등 사용자 Outlook 클라이언트 또는 사서함 콘텐츠 인덱싱 등 또는 eDiscovery 검색에 대 한는 시스템 시작 된 활동에 게 전자 메일을 다운로드 하는 경우 트리거되는 프로세스입니다.
  
Office 365 사용자 사서함에 대 한 가용성 키를 사용 하 여 여부를 결정 하기 위한 사용자 시작 작업에 대 한 응답으로이 프로세스를 따릅니다.
  
1. Office 365 사서함 Azure 키 볼트의 두 고객 키의 위치를 결정 하기 위해 할당 하는 DEP를 읽습니다.
    
2. Office 365는 임의로 DEP에서 두 고객 키 중 하나를 선택 하 고 고객 키를 사용 하 여 DEP 키 래핑을 Azure 키 추적용 요청을 보냅니다.
    
3. Office 365 요청을 보냅니다 두번째 Azure 키 추적용이 이번에는 대체를 사용 하도록 지시, 실패 하 고 오류를 반환 하는 고객 키는 DEP 래핑을 요청 키를 사용 하는 경우 (2) 고객 키입니다.
    
4. 두번째 사용자 계정의 고객 키 실패를 사용 하 여 DEP 키 래핑 취소를 요청 하는 오류를 반환 하는 경우 Office 365의 두 요청 결과 검사:
    
  - 고객 id에 의해 명시적으로 조치를 반영 하 하지 않으면 오류를 확인 하는 검사, Office 365 DEP 키의 암호를 해독 하는 가용성 키를 사용 합니다. DEP 키는 사서함 키의 암호를 해독 하 고 사용자 요청을 완료 하는 사용 됩니다.
    
    이 경우 Azure 키 추적용은 어떠한 이유로 든 응답할 수 없는 이거나 연결할 수 없는 상태입니다. Office 365가 고객이 의도적으로 키에 대 한 액세스를 해지 하는 경우를 결정 하는 방법은 없습니다.
    
  - 검사 있음을 나타내는 경우 주의깊게 됩니까를 렌더링 하는 고객 키를 사용할 수 없도록 제거 되었습니다 다음 가용성 키 사용 되지 않습니다, 사용자 요청이 실패 하 고 예: 로그인 오류, 오류 메시지를 수신 하는 사용자.
    
    이 경우 고객 서비스에 영향을 받는, 하 고 고객 키 조건이 정상 인식 하 게 됩니다. 예, 고객을 사용 하는 단일 DEP 조직에서 모든 사서함에 대 한 고객 여기서 사용자가 자신의 사서함에 액세스할 수 없습니다는 광범위 한 실패를 경험할 수 있습니다. 이렇게 하면 두 고객 키는 정상 때 고객이의 상황을 수정 하 고 서비스 정상 상태를 복원 하려면 필요성을 인식 이루어집니다.
    
 **Office 365 서비스 코드에 의해 시작 되는 작업에 대 한 가용성 키를 사용 합니다.**
  
Office 365 서비스 코드 항상 유효한 로그인 토큰 있으며 차단할 수 없습니다. 따라서 가용성 키가 삭제 될 때까지 사용할 수에 대 한 작업에 의해 또는 검색 인덱스를 만드는 예: Office 365 서비스 코드를 내부 시작 또는 사서함을 이동 합니다.
  
 **가용성 키를 사용 하 여 주요 손실에서 복구 합니다.**
  
가용성 키와 연결 된 동일한 DEP 설명에 따라 FAQ 항목에 대 한 답에 "내 키 손상 된 경우 복구 하는 방법?" 두 Azure 키 추적용 키의 손실에서 복구를 사용할 수 있습니다.
  
## <a name="how-is-the-availability-key-used-with-sharepoint-online-and-onedrive-for-business"></a>가용성 키의 용도와 SharePoint Online OneDrive 비즈니스에 대 한 무엇입니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

SharePoint Online 및 비즈니스용 OneDrive 아키텍처 및 고객 키 및 가용성 키에 대 한 구현에는 Exchange Online 및 비즈니스를 위한 Skype와 다릅니다.
  
고객 고객 관리 되는 키를 이동 하는 경우 Office 365 테 넌 트 관련 중간 키 (TIK)를 만듭니다. Office 365 암호화는 TIK을 두번 한번 고객 키를 각각 사용 하 고는 TIK의 두 암호화 된 버전을 저장 합니다. TIK의 암호화 된 버전에만 저장 됩니다 하 고는 TIK 고객 키와 해독 될 수 있습니다. TIK blob 키 암호화를 사용 하 여 사이트 키를 암호화 하는데 사용 됩니다. 자체 blob가 암호화 되며 Microsoft Azure Blob 저장소 서비스에 저장 됩니다.
  
Office 365 고객 파일 데이터가 blob에 액세스 하려면이 프로세스를 따릅니다.
  
1. 고객 키를 사용 하 여 TIK 암호를 해독 합니다.
    
2. 해독 된 TIK를 사용 하 여 사이트 키의 암호를 해독 합니다.
    
3. 해독 된 사이트 키를 사용 하 여 blob 키를 암호 해독 합니다.
    
4. 해독 된 blob 키를 사용 하 여 blob를 암호 해독 합니다.
    
TIK의 암호를 해독 하는 경우 Office 365 두 암호 해독 요청 약간의 밑 Azure 키 추적용 발급 합니다. 종료 하려면 첫번째 계정을 다른 요청을 취소 하 고 결과 제공 합니다.
  
고객이 자신의 고객 키에 대 한 액세스를 잃을, 하는 경우 Office 365도 암호화는 TIK 가용성 키를 사용 하 고이 각 고객 키를 사용 하 여 암호화 TIKs와 함께 저장 합니다. 가용성 키를 사용 하 여 암호화 TIK 고객은 끊겼을 액세스 해당 키를 실수로 또는 악의적으로 하는 경우의 복구 경로 참여 하는 Microsoft를 호출 하는 경우에 사용 됩니다.
  
가용성 및 확장 이유로 암호가 해독 된 TIKs 시간-제한 된 메모리 캐시에 캐시 됩니다. Office 365 각 TIK 암호를 해독 하려고 TIK 캐시 만료 되 면 설정 될때까지 경우 2 시간입니다. 캐시 수명을 확장는 TIKs의 암호를 해독 합니다. 시간에 많은 시간에 대 한 TIK 암호 해독 실패 하는 경우 Office 365 캐시 만료 되기 전에 엔지니어링 알리도록 경고를 생성 합니다. 고객이 Microsoft를 호출 하는 경우에 Office 365 시작 TIK 하 고 새 집합이 Microsoft의 비밀 저장소와 온 보 딩 사용 하 여 다시는 암호가 해독 된 테 넌 트에 저장 된 가용성 키가 있는 TIK 암호 해독을 포함 하는 복구 작업 Azure 키 추적용 키 고객 제공 합니다.
  
현재로 서 Azure blob 저장소를 있지만 SharePoint Online 목록 항목이 아닌 또는 SQL 데이터베이스에 저장 된 메타 데이터에 저장 하는 SharePoint Online 파일 데이터의 암호화 및 암호 해독 체인에 고객 키는 작업이 포함 됩니다. Office 365 가용성 키 SharePoint Online 또는 비즈니스용 OneDrive에 대 한 대/소문자, 위에서 설명한 이외의 고객 시작 되는 사용 하지 않습니다. 고객 데이터에 대 한 휴먼 액세스 고객 Lockbox에 의해 보호 됩니다.
  
## <a name="how-is-customer-key-licensed"></a>고객 키는 어떠한 방법
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

고객 키 Office 365 Enterprise 제품군, "e", 5 및 고급 준수 SKU에서 제공 됩니다. 또한 고객은 Azure 키 추적용 사용 하기 위한 적절 한 라이선스를 구입도 해야 합니다.
  
고객 키에서 이점의 각 사용자는 고객 키에 의해 적용 되어야 하는 경우 사용이 허가 되도록 해야 합니다.
  
SharePoint Online에 대 한 고객 키를 구성 하는 Office 365 관리자는 또한 설치 단계를 수행 하려면 라이선스를 해야 합니다. 또한 기능을 통해 이점 되는 사용자 라이선스 필요가-사이트 소유자 및 고객 키를 사용 하 여 암호화 된 하나 이상의 사이트의 파일에 액세스 하는 모든 사용자 포함 됩니다. 외부 사용자는 고객 키를 사용 하 여 암호화 된 하나 이상의 사이트의 파일에 액세스 하려면 라이선스 필요가 없습니다.
  
Exchange Online에 대 한 "사용자" 사서함와 "사용자의 메일" 사서함 라이선스 해야 합니다. 고객 키에 대 한 라이선스가 않아도 모든 등의 다른 공유 사서함을 함께 제공 됩니다. Exchange Online 사서함 제대로 라이선스를 갖고 있는지를 확인 하려면 다음 cmdlet를 실행 합니다.
  
```
(Get-Mailbox <alias >).PersistedCapabilities
```

문자열 BPOS_S_EquivioAnalytics 존재 경우, 사서함 사용이 허가 됩니다. 그렇지 않은 경우에이 사서함에 대 한 고객 키 기능을 사용 하려면 적절 한 라이선스를 적용 해야 합니다.
  
## <a name="can-i-enable-customer-key-for-a-trial-subscription"></a>평가판 구독에 대 한 고객 키를 사용할 수 있습니까?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

아니요. 정의상, 평가판 구독 제한 수명이 합니다. 평가판 구독에서 호스팅되는 암호화 키 평가판 수명 끝날 때 손실 될 수 있습니다. Microsoft 수 없고 평가판 구독에 중요 한 고객 데이터를 보내는에서 고객 하더라도 하기 때문에 고객 키 평가판 구독 사용 금지 됩니다.
  
## <a name="how-much-will-using-customer-key-cost"></a>고객 키 비용을 사용 하는 얼마나?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

고객 키에 필요한 라이선스, 외에도 고객 키 추적용 사용 현황에 대 한 비용 지불 해야 합니다. [세부 정보를 가격 azure 키 추적용](https://azure.microsoft.com/en-us/pricing/details/key-vault/) 비용 모델을 설명 하 고 예측에 도움이 됩니다. 사용 패턴 다 있기 때문에 모든 고객 인해 발생 하는 정확한 비용을 예측 하는 방법은 있습니다. 경험은 비용이 매우 낮은 이며의 $0.002에 $0.005 한달간 사용자 당 범위와 HSM 백업 키의 비용에 들어가는 일반적으로 나타났습니다. 비용 고객 및 Azure 키 추적용 로그에 사용 되는 Azure 저장소의 양을에서 선택한 로깅 구성에 따라도 달라 집니다. 
  
## <a name="for-more-information"></a>자세한 내용
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

고객 키로 시작 [고객 키를 사용 하 여 Office 365에서 데이터를 제어](controlling-your-data-using-customer-key.md)를 참조 합니다.
  

