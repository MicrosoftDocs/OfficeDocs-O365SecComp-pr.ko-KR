---
title: Office 365의 사용자 지정 도메인에서 전자 메일에 DKIM 사용
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 56fee1c7-dc37-470e-9b09-33fff6d94617
ms.collection:
- M365-security-compliance
description: '요약: 이 문서에서는 대상 전자 메일 시스템에서 사용자 지정 도메인에서 보낸 메시지를 신뢰하는지 확인하기 위해 Office 365에서 DomainKeys 식별 메일 (DKIM)을 사용하는 방법을 설명합니다.'
ms.openlocfilehash: 40b7505b18db697ffb47932fba0f10c6a53b340c
ms.sourcegitcommit: 6122eb026c558a5126c40845e656fbb0c40cb32a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2019
ms.locfileid: "36222748"
---
# <a name="use-dkim-to-validate-outbound-email-sent-from-your-custom-domain-in-office-365"></a>DKIM을 사용하여 Office 365의 사용자 지정 도메인에서 전송한 아웃바운드 전자 메일의 유효성을 검사합니다.

 **요약:** 이 문서에서는 대상 전자 메일 시스템에서 사용자 지정 도메인에서 보낸 아웃바운드 메시지를 신뢰하는지 확인하기 위해 Office 365에서 DomainKeys 식별 메일 (DKIM)을 사용하는 방법을 설명합니다. 
  
SPF 및 DMARC와 함께 DKIM을 사용하여 spoofer로 하여금 사용자의 도메인에서 오는 것처럼 보이는 메시지를 보내지 못하도록 해야 합니다. DKIM을 사용하면 메시지 머리글에 있는 전자 메일 메시지에 디지털 서명을 첨부할 수 있습니다. 복잡해 보이지만 실제로는 그렇지 않습니다. DKIM을 구성할 때 암호화 인증을 사용하여 전자 메일 메시지에 해당 이름을 연결하거나 서명할 수 있는 권한을 도메인에 부여합니다. 사용자의 도메인으로부터 전자 메일을 수신하는 전자 메일 시스템에서는 이 디지털 서명을 사용하여 수신하는 전자 메일이 합법적인지 확인할 수 있습니다.
  
기본적으로 개인 키를 사용하여 사용자의 도메인의 보내는 전자 메일에서 머리글을 암호화 합니다. 사용자의 DNS 레코드에 공개 키를 게시하면 수신하는 서버에서 이를 이용하여 서명을 디코딩하는 데 사용할 수 있습니다. 공개 키를 사용하여 메시지가 실제로 사용자로부터 온 것인지 도메인을 스푸핑한 사람에게서 온 것이 아닌지 확인합니다.
  
Office 365는 초기 도메인에 대해 DKIM을 자동으로 설정합니다. 초기 도메인은 서비스에 가입할 때 Office 365가 사용자를 위해 만든 도메인입니다 (예: contoso.onmicrosoft.com). 초기 도메인에 대해 DKIM을 설정하기 위해 별도의 작업을 수행할 필요가 없습니다. 도메인에 대한 자세한 내용은 [도메인 FAQ](https://support.office.com/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조하세요.
  
사용자 지정 도메인의 DKIM에 대해서 아무 것도 수행하지 않도록 선택할 수 있습니다. 사용자 지정 도메인에 DKIM을 설정하지 않으면 Office 365는 개인 및 공개 키 쌍을 만들고 DKIM 서명을 사용하도록 설정 한 다음 사용자 지정 도메인에 대한 Office 365 기본 정책을 구성합니다. 대부분의 Office 365 고객에게는 이 기능으로 충분하지만 다음과 같은 경우에는 사용자 지정 도메인에 대해 DKIM을 수동으로 구성해야 합니다.
  
- Office 365에 두 개 이상의 사용자 지정 도메인이 있는 경우
    
- DMARC 또한 설정하려는 경우 (권장됨)
    
- 개인 키를 제어하려는 경우
    
- CNAME 레코드를 사용자 지정하려는 경우
    
- 타사 대량 메일 프로그램을 사용하는 경우와 같이 타사 도메인에서 시작되는 전자 메일에 대해 DKIM 키를 설정하려는 경우
    
이 문서의 내용:
  
- [Office 365에서 악의적인 스푸핑을 방지하기 위해 DKIM이 SPF 단독보다 더욱 효율적인 방식인 이유](use-dkim-to-validate-outbound-email.md#HowDKIMWorks)
    
- [Office 365에서 DKIM을 직접 설정하는 데 필요한 사항](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365)
    
- [Office 365에서 두 개 이상의 사용자 지정 도메인에 대해 DKIM을 구성](use-dkim-to-validate-outbound-email.md#DKIMMultiDomain)
    
- [Office 365에서 사용자 지정 도메인에 대해 DKIM 서명 정책을 사용 하지 않도록 설정](use-dkim-to-validate-outbound-email.md#DisableDKIMSigningPolicy)
    
- [DKIM 및 Office 365의 기본 동작](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)
    
- [타사 서비스에서 사용자 지정 도메인을 대신하여 이메일을 보내거나 스푸핑할 수 있도록 DKIM을 설정](use-dkim-to-validate-outbound-email.md#SetUp3rdPartyspoof)
    
- [다음 단계: Office 365에 대한 DKIM을 설정한 후](use-dkim-to-validate-outbound-email.md#DKIMNextSteps)
    
## <a name="how-dkim-works-better-than-spf-alone-to-prevent-malicious-spoofing-in-office-365"></a>Office 365에서 악의적인 스푸핑을 방지하기 위해 DKIM이 SPF 단독보다 더욱 효율적인 방식인 이유
<a name="HowDKIMWorks"> </a>

SPF는 메시지 봉투에 정보를 추가하지만 DKIM은 실제로 메시지 머리글 내에서 서명을 암호화 합니다. 메시지를 전달할 때 메시지의 봉투 일부가 전달 서버에서 제거될 수 있습니다. 디지털 서명은 전자 메일 머리글의 일부이기 때문에 전자 메일 메시지와 함께 유지되므로 DKIM은 다음 예제와 같이 메시지가 전달된 경우에도 작동합니다.
  
![SPF 확인이 실패하는 경우 DKIM 인증을 제공하는 전달된 메시지를 보여주는 다이어그램](media/28f93b4c-97e7-4309-acc4-fd0d2e0e3377.jpg)
  
이 예제에서 도메인에 대한 SPF TXT 레코드만 게시한 경우 받는 사람의 메일 서버에서 전자 메일을 스팸으로 표시하고 가양성 결과를 생성할 수 있습니다. 이 시나리오에 DKIM을 추가하면 가양성 스팸 보고를 줄일 수가 있습니다. DKIM은 IP 주소뿐만 아니라 인증을 위해 공개 키 암호화를 사용하기 때문에 DKIM은 SPF보다 훨씬 강력한 인증 형식으로 간주됩니다. 배포시 SPF 및 DKIM과 DMARC를 모두 사용하는 것이 좋습니다.
  
핵심: DKIM은 개인 키를 사용하여 암호화 된 서명을 메시지 머리글에 삽입합니다. 서명 도메인 또는 아웃 바운드 도메인이 머리글의 **d =** 필드 값으로 삽입됩니다. 확인 도메인 또는 수신자 도메인은 **d =** 필드를 사용하여 DNS에서 공개 키를 조회하고 메시지를 인증합니다. 메시지를 확인하면 DKIM 검사가 통과됩니다. 
  
## <a name="what-you-need-to-do-to-manually-set-up-dkim-in-office-365"></a>Office 365에서 DKIM을 직접 설정하는 데 필요한 사항
<a name="SetUpDKIMO365"> </a>

DKIM을 구성하려면 다음 단계를 수행합니다.
  
- [DNS에서 사용자 지정 도메인에 대해 두 개의 CNAME 레코드 게시](use-dkim-to-validate-outbound-email.md#Publish2CNAME)
    
- [Office 365에서 사용자 지정 도메인에 DKIM 서명 사용](use-dkim-to-validate-outbound-email.md#EnableDKIMinO365)
    
### <a name="publish-two-cname-records-for-your-custom-domain-in-dns"></a>DNS에서 사용자 지정 도메인에 대해 두 개의 CNAME 레코드 게시
<a name="Publish2CNAME"> </a>

DNS에 DKIM 서명을 추가하려는 각 도메인에 대해 두 개의 CNAME 레코드를 게시해야 합니다. 

다음 명령을 실행합니다.    
   
    New-DkimSigningConfig -DomainName <domain> -Enabled $false
       
    Get-DkimSigningConfig -DomainName domain | fl Selector1CNAME, Selector2CNAME
    
Get-DkimSigningConfig 출력에서 참조되는 CNAME 만들기
    
    Set-DkimSigningConfig -DomainName domain -Enabled $true
    
DNS의 CNAME 레코드는 Office 365용 Microsoft DNS 서버의 DNS에 생성되어 이미 존재하는 A 레코드를 가리킵니다.
  
Office 365는 사용자가 설정한 두 개의 레코드를 사용하여 자동 키 순환을 수행합니다. Office 365의 초기 도메인 외에 사용자 지정 도메인을 프로비저닝한 경우에는 추가 도메인마다 두 개의 CNAME 레코드를 게시해야 합니다. 따라서 두 개의 도메인이 있는 경우 두 개의 CNAME 레코드를 모두 게시해야 합니다.
  
CNAME 레코드에는 다음 형식을 사용합니다.

> [!IMPORTANT]
> 사용자가 GCC High 고객인 경우 _domainGuid_를 다르게 계산합니다! _domainGuid_를 계산하기 위해 _initialDomain_에 대한 MX 레코드를 조회하는 대신 사용자 정의된 도메인에서 직접 계산합니다. 예를 들어, 사용자 지정 도메인이 "contoso.com"인 경우 domainGuid는 "contoso-com"이되고 마침표는 대시로 바뀝니다. 따라서 initialDomain이 가리키는 MX 레코드와 상관없이 항상 위의 방법을 사용하여 CNAME 레코드에서 사용할 domainGuid를 계산합니다.

  
```
Host name:          selector1._domainkey
Points to address or value: selector1-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600

Host name:          selector2._domainkey
Points to address or value: selector2-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600
```

여기서,
  
- Office 365의 경우 셀렉터는 항상 "selector1" 또는 "selector2"입니다. 
    
- _domainGUID_는 mail.protection.outlook.com 이전에 표시되는 사용자 정의 도메인에 대한 사용자 정의된 MX 레코드의 _domainGUID_와 동일합니다. 예를 들어 도메인 contoso.com에 대한 다음 MX 레코드에서 _domainGUID_는 contoso-com입니다. 
    
    ```
    contoso.com.  3600  IN  MX   5 contoso-com.mail.protection.outlook.com
    ```

- _initialdomain_ 은 Office 365에 등록할 때 사용한 도메인입니다. 초기 도메인은 항상 onmicrosoft.com으로 끝납니다. 초기 도메인을 확인하는 방법에 대한 자세한 내용은 [도메인 FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조하세요.
    
예를 들어 cohovineyardandwinery.onmicrosoft.com이라는 초기 도메인과 cohovineyard.com 및 cohowinery.com이라는 두 개의 사용자 지정 도메인이 있는 경우 추가 도메인마다 총 두 개의 CNAME 레코드를 설정해야 합니다 (총 네 개의 CNAME 레코드).
  
```
Host name:          selector1._domainkey
Points to address or value: selector1-cohovineyard-com._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:          selector2._domainkey
Points to address or value: selector2-cohovineyard-com._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:          selector1._domainkey
Points to address or value: selector1-cohowinery-com._domainkey.cohovineyardandwinery.onmicrosoft.com 
TTL:                3600
 
Host name:          selector2._domainkey
Points to address or value: selector2-cohowinery-com._domainkey.cohovineyardandwinery.onmicrosoft.com 
TTL:                3600
```

### <a name="enable-dkim-signing-for-your-custom-domain-in-office-365"></a>Office 365에서 사용자 지정 도메인에 DKIM 서명 사용
<a name="EnableDKIMinO365"> </a>

CNAME 레코드를 DNS에 게시하면 Office 365를 통해 DKIM 서명을 사용할 수 있습니다. Microsoft 365 관리 센터 또는 PowerShell을 사용하여 이 작업을 수행할 수 있습니다.
  
#### <a name="to-enable-dkim-signing-for-your-custom-domain-through-the-admin-center"></a>관리 센터를 통해 사용자 지정 도메인에 DKIM 서명 사용

1. 회사 또는 학교 계정으로 [Office 365에 로그인](https://support.office.microsoft.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4)합니다. 
    
2. 왼쪽 위에서 앱 시작 관리자 아이콘을 선택하고 **관리자**를 선택합니다.
    
3. 왼쪽 아래 탐색에서 **관리자**를 확장하고 **Exchange**를 선택합니다.
    
4. **보호**\>**dkim**으로 이동합니다.
    
5. DKIM을 활성화 할 도메인을 선택한 다음 **DKIM 서명을 사용하여 이 도메인의 메시지 서명**에 대해 **활성화**를 선택합니다. 각 사용자 지정 도메인에 대해 이 단계를 반복합니다.
    
#### <a name="to-enable-dkim-signing-for-your-custom-domain-by-using-powershell"></a>PowerShell을 사용하여 사용자 지정 도메인에 DKIM 서명 사용

1. [Exchange Online PowerShell에 연결합니다](https://technet.microsoft.com/library/jj984289.aspx).
    
2. 다음 명령을 실행합니다.
    
    ```
    New-DkimSigningConfig -DomainName <domain> -Enabled $true
    ```

   여기서 _도메인_은 DKIM 서명을 활성화하려는 사용자 지정 도메인의 이름입니다. 
    
   예를 들어 contoso.com 도메인의 경우
    
    ```
    New-DkimSigningConfig -DomainName contoso.com -Enabled $true
    ```

#### <a name="to-confirm-dkim-signing-is-configured-properly-for-office-365"></a>Office 365에 DKIM 서명이 올바르게 구성되어 있는지 확인하려면

다음 단계를 수행하여 DKIM을 올바르게 구성했는지 확인하기 전에 몇 분 정도 기다립니다. 이를 통해 도메인에 대한 DKIM 정보가 네트워크 전체에 전파될 수 있습니다.
  
- Office 365 DKIM 사용 가능한 도메인 내의 계정에서 outlook.com 또는 Hotmail.com과 같은 다른 전자 메일 계정으로 메시지를 보냅니다.
    
- 테스트 목적으로 aol.com 계정을 사용하지 마세요. SPF 검사가 통과되면 AOL에서 DKIM 검사를 건너뛸 수 있습니다. 이렇게 하면 테스트가 무효화 됩니다.
    
- 메시지를 열고 머리글을 확인합니다. 메시지 머리글 보기에 대한 지침은 메시징 클라이언트에 따라 다릅니다. Outlook에서 메시지 머리글을 보는 방법은 [전자 메일 메시지 머리글보기](https://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C)를 참조하세요.

  DKIM 서명 메시지에는 CNAME 항목을 게시할 때 정의한 호스트 이름과 도메인이 포함됩니다. 메시지가 다음 예제와 같이 표시됩니다.  
    
    ```
    From: Example User <example@contoso.com> 
    DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed; 
        s=selector1; d=contoso.com; t=1429912795; 
        h=From:To:Message-ID:Subject:MIME-Version:Content-Type; 
        bh=<body hash>; 
        b=<signed field>;
    ```

- Authentication-Results 머리글을 찾습니다. 각 수신 서비스는 수신 메일을 스탬프 처리하기 위해 약간씩 다른 형식을 사용하지만 결과에는 **DKIM=pass** 또는 **DKIM=OK**가 포함되어야 합니다. 
    
## <a name="to-configure-dkim-for-more-than-one-custom-domain-in-office-365"></a>Office 365에서 두 개 이상의 사용자 지정 도메인에 대해 DKIM을 구성
<a name="DKIMMultiDomain"> </a>

나중에 다른 사용자 지정 도메인을 추가하기로 결정하고 새 도메인에 대해 DKIM을 활성화하려는 경우 각 도메인에 대해 이 문서의 단계를 완료해야 합니다. 특히 [Office 365에서 DKIM을 수동으로 설정하려면 수행해야 할 작업](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365)의 모든 단계를 완료합니다.
  
## <a name="disabling-the-dkim-signing-policy-for-a-custom-domain-in-office-365"></a>Office 365에서 사용자 지정 도메인에 대해 DKIM 서명 정책을 사용 하지 않도록 설정
<a name="DisableDKIMSigningPolicy"> </a>

서명 정책을 비활성화해도 DKIM이 완전히 비활성화되지는 않습니다. 일정 시간이 지나면 Office 365는 도메인에 대한 기본 Office 365 정책을 자동으로 적용합니다. 자세한 내용은 [DKIM 및 Office 365의 기본 동작](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)을 참조합니다.
  
### <a name="to-disable-the-dkim-signing-policy-by-using-windows-powershell"></a>Windows PowerShell을 사용하여 DKIM 서명 정책을 비활성화하려면

1. [Exchange Online PowerShell에 연결합니다](https://technet.microsoft.com/library/jj984289.aspx).
    
2. DKIM 서명을 비활성화하려는 각 도메인에 대해 다음 명령 중 하나를 실행합니다.
    
    ```
    $p=Get-DkimSigningConfig -identity <domain>
    $p[0] | set-DkimSigningConfig -enabled $false
    ```

   예:
    
    ```
    $p=Get-DkimSigningConfig -identity contoso.com
    $p[0] | set-DkimSigningConfig -enabled $false
    ```

   또는
    
    ```
    Set-DkimSigningConfig -identity $p[<number>].identity -enabled $false
    ```

    여기에서 _numbe_r는 정책의 인덱스입니다. 예: 
    
    ```
    Set-DkimSigningConfig -identity $p[0].identity -enabled $false
    ```

## <a name="default-behavior-for-dkim-and-office-365"></a>DKIM 및 Office 365의 기본 동작
<a name="DefaultDKIMbehavior"> </a>

DKIM을 사용하지 않도록 설정하면 Office 365는 기본 도메인에 대해 1024 비트 DKIM 공개 키와 데이터 센터에 내부적으로 저장되는 관련 개인 키를 자동으로 만듭니다. 기본적으로 Office 365는 정책이 없는 도메인에 대해 기본 서명 구성을 사용합니다. 즉, DKIM을 직접 설정하지 않으면 Office 365는 도메인에 DKIM을 사용하기 위해 만든 기본 정책과 키를 사용합니다.
  
또한 DKIM 서명을 사용하도록 설정 한 후 다시 사용하지 않도록 설정할 경우 일정 시간이 지나면 Office 365가 도메인에 대해 Office 365 기본 정책을 자동으로 적용합니다.
  
다음 예제에서는 fabrikam.com용 DKIM이 도메인 관리자가 아닌 Office 365에서 활성화되었다고 가정합니다. 이는 필수적인 CNAME이 DNS에 존재하지 않음을 의미합니다. 이 도메인의 전자 메일에 대한 DKIM 서명은 다음과 같습니다.
  
```
From: Second Example <second.example@fabrikam.com> 
DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed; 
    s=selector1-fabrikam-com; d=contoso.onmicrosoft.com; t=1429912795; 
    h=From:To:Message-ID:Subject:MIME-Version:Content-Type; 
    bh=<body hash>; 
    b=<signed field>;
```

이 예제에서 도메인 관리자가 fabrikam.com에 대한 DKIM 서명을 활성화한 경우 호스트 이름과 도메인에는 CNAME이 가리키는 값이 포함됩니다. 결국 Office 365에서 보낸 모든 단일 메시지는 DKIM 서명됩니다. DKIM을 직접 활성화하는 경우 도메인은 보낸 사람:주소의 도메인 (이 경우 fabrikam.com)과 동일합니다. 직접 활성화하지 않는 경우 맞추는 대신 사용자 조직의 초기 도메인을 사용합니다. 초기 도메인을 확인하는 방법에 대한 자세한 내용은 [도메인 FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조하세요.
  
## <a name="set-up-dkim-so-that-a-third-party-service-can-send-or-spoof-email-on-behalf-of-your-custom-domain"></a>타사 서비스에서 사용자 지정 도메인을 대신하여 이메일을 보내거나 스푸핑할 수 있도록 DKIM을 설정
<a name="SetUp3rdPartyspoof"> </a>

일부 대량 전자 메일 서비스 공급자 또는 소프트웨어를 서비스로 제공하는 공급자는 서비스에서 보낸 전자 메일에 대해 DKIM 키를 설정할 수 있습니다. 따라서 필수 DNS 레코드를 설정하기 위해 본인과 타사 간의 조정이 필요합니다. 두 조직이 정확히 동일한 방식으로 이 작업을 수행할 수 없습니다. 그 대신 프로세스는 전적으로 조직에 따라 다릅니다.
  
contoso.com 및 bulkemailprovider.com에 대해 올바르게 구성된 DKIM을 보여주는 메시지의 예는 다음과 같습니다.
  
```
Return-Path: <communication@bulkemailprovider.com>
 From: <sender@contoso.com>
 DKIM-Signature: s=s1024; d=contoso.com
 Subject: Here is a message from Bulk Email Provider's infrastructure, but with a DKIM signature authorized by contoso.com
```

이 예제에서는 이 결과를 얻기 위해 다음과 같이 합니다.
  
1. 대량 전자 메일 공급자가 Contoso에 공개 DKIM 키를 제공합니다.
    
2. Contoso는 DKIM 키를 해당 DNS 레코드에 게시합니다.
    
3. 전자 메일을 보낼 때 대량 전자 메일 공급자는 해당하는 개인 키로 키에 서명합니다. 이렇게하면 대량 전자 메일 공급자가 메시지 머리글에 DKIM 서명을 첨부합니다.
    
4. 수신 이메일 시스템은 메시지의 From:(5322.From) 주소에서 도메인에 대해 DKIM-Signature d= \<도메인\> 값을 인증하여 DKIM 확인을 수행합니다. 이 예제에서 값은 다음과 일치합니다.
    
    sender@**contoso.com**
    
    d=**contoso.com**
    
## <a name="next-steps-after-you-set-up-dkim-for-office-365"></a>다음 단계: Office 365에 대한 DKIM을 설정한 후
<a name="DKIMNextSteps"> </a>

DKIM은 스푸핑을 방지하도록 설계되었지만 SPF 및 DMARC에서 더 잘 작동합니다. DKIM을 설정한 후에 SPF를 아직 설정하지 않은 경우 설정을 수행해야합니다. SPF를 빠르게 도입하여 신속하게 구성하려면 [스푸핑 방지를 위해 Office 365에서 SPF 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)을 참조하세요. Office 365에서 SPF를 사용하는 방법이나 문제 해결 또는 비표준 배포(예: 하이브리드 배포)에 대한 자세한 내용은 [Office 365에서 SPF(Sender Policy Framework)를 사용하여 스푸핑을 차단하는 방법](how-office-365-uses-spf-to-prevent-spoofing.md)을 참조하세요. 다음으로 [DMARC를 사용하여 Office 365에서 전자 메일 유효성 검사](use-dmarc-to-validate-email.md)를 참조하세요. [스팸 방지 메시지 헤드](anti-spam-message-headers.md)에는 Office 365에서 DKIM 검사에 사용하는 구문 및 헤드 필드가 포함됩니다. 
  

