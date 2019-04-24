---
title: Office 365의 사용자 지정 도메인에서 dkim을 사용 하 여 전자 메일 보내기
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 56fee1c7-dc37-470e-9b09-33fff6d94617
ms.collection:
- M365-security-compliance
description: 요약:이 문서에서는 대상 전자 메일 시스템이 사용자 지정 도메인에서 보낸 메시지를 신뢰 하도록 하기 위해 Office 365에서 domainkeys 식별 메일 (dkim)을 사용 하는 방법에 대해 설명 합니다.
ms.openlocfilehash: fc2a509aacdaac0aeef22696d85512f91957502f
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263748"
---
# <a name="use-dkim-to-validate-outbound-email-sent-from-your-custom-domain-in-office-365"></a>dkim을 사용 하 여 Office 365의 사용자 지정 도메인에서 전송 되는 아웃 바운드 전자 메일의 유효성 검사

 **요약:** 이 문서에서는 사용자 지정 도메인에서 보낸 아웃 바운드 메시지를 대상 전자 메일 시스템에서 신뢰 하도록 하기 위해 Office 365의 dkim (domainkeys 확인 메일)을 사용 하는 방법에 대해 설명 합니다. 
  
SPF 및 DMARC 외에 dkim을 사용 하 여 spoofers가 도메인에서 오는 것 처럼 보이지만 메시지를 보내지 않도록 해야 합니다. dkim을 사용 하 여 메시지 헤더에 전자 메일 메시지에 디지털 서명을 추가할 수 있습니다. 복잡 하 게 들리지만 실제로는 그렇지 않습니다. dkim을 구성 하는 경우 암호화 인증을 사용 하 여 전자 메일 메시지에 해당 이름을 연결 하거나 서명 하도록 도메인에 권한을 부여 합니다. 도메인에서 전자 메일을 수신 하는 전자 메일 시스템은이 디지털 서명을 사용 하 여 받는 전자 메일이 합법적인 지 확인할 수 있습니다.
  
기본적으로 개인 키를 사용 하 여 도메인의 보내는 전자 메일에 있는 헤더를 암호화 합니다. 받는 서버에서 서명을 디코딩하는 데 사용할 수 있는 도메인의 DNS 레코드에 공개 키를 게시 합니다. 공개 키를 사용 하 여 메시지가 실제로 사용자 로부터 온 것이 고 사용자가 도메인을 위장 하지 못하게 하는 것을 확인 합니다.
  
Office 365에서는 초기 도메인에 대해 dkim을 자동으로 설정 합니다. 초기 도메인은 contoso.onmicrosoft.com과 같이 서비스에 등록 했을 때 Office 365에서 만든 도메인입니다. 초기 도메인에 대해 dkim을 설정 하는 작업은 필요 하지 않습니다. 도메인에 대 한 자세한 내용은 [도메인 FAQ](https://support.office.com/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조 하십시오.
  
사용자 지정 도메인에 대 한 dkim에 대해서도 작업을 수행 하지 않도록 선택할 수 있습니다. 사용자 지정 도메인에 대해 dkim을 설정 하지 않으면 office 365에서 개인 및 공개 키 쌍을 만들고 dkim 서명을 사용 하도록 설정한 다음 사용자 지정 도메인에 대해 Office 365 기본 정책을 구성 합니다. 대부분의 Office 365 고객에 게는 충분 한 범위를 제공 하지만 다음과 같은 상황에서는 사용자 지정 도메인에 대해 dkim을 수동으로 구성 해야 합니다.
  
- Office 365에 사용자 지정 도메인이 두 개 이상 있습니다.
    
- DMARC를 설정 하겠습니다 (권장).
    
- 개인 키를 제어할 수 있습니다.
    
- CNAME 레코드를 사용자 지정 하려는 경우
    
- 타사의 대량 메일 프로그램을 사용 하는 경우와 같이 타사 도메인에서 시작 되는 사용자에 대해 dkim 키를 설정 하려는 경우
    
이 문서의 내용
  
- [dkim이 SPF 단독으로 작동 하 여 Office 365에서 악의적인 스푸핑을 방지 하는 방법](use-dkim-to-validate-outbound-email.md#HowDKIMWorks)
    
- [Office 365에서 dkim을 수동으로 설정 하기 위해 수행 해야 하는 작업](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365)
    
- [Office 365에서 둘 이상의 사용자 지정 도메인에 대해 dkim을 구성 하려면](use-dkim-to-validate-outbound-email.md#DKIMMultiDomain)
    
- [Office 365에서 사용자 지정 도메인에 대해 dkim 서명 정책 사용 안 함](use-dkim-to-validate-outbound-email.md#DisableDKIMSigningPolicy)
    
- [dkim 및 Office 365에 대 한 기본 동작](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)
    
- [타사 서비스가 사용자 지정 도메인을 대신 하 여 전자 메일을 보내거나 스푸핑할 수 있도록 dkim을 설정 합니다.](use-dkim-to-validate-outbound-email.md#SetUp3rdPartyspoof)
    
- [다음 단계: Office 365에 대 한 dkim을 설정한 후](use-dkim-to-validate-outbound-email.md#DKIMNextSteps)
    
## <a name="how-dkim-works-better-than-spf-alone-to-prevent-malicious-spoofing-in-office-365"></a>dkim이 SPF 단독으로 작동 하 여 Office 365에서 악의적인 스푸핑을 방지 하는 방법
<a name="HowDKIMWorks"> </a>

SPF는 정보를 메시지 봉투에 추가 하지만 dkim은 메시지 헤더 내의 서명을 실제로 암호화 합니다. 메시지를 전달 하면 메시지 봉투의 일부를 전달 서버에서 제거할 수 있습니다. 디지털 서명이 전자 메일 헤더의 일부 이기 때문에 전자 메일 메시지에 남아 있으므로 다음 예제와 같이 메시지가 전달 된 경우에도 dkim은 작동 합니다.
  
![SPF 확인이 실패하는 경우 DKIM 인증을 제공하는 전달된 메시지를 보여주는 다이어그램](media/28f93b4c-97e7-4309-acc4-fd0d2e0e3377.jpg)
  
이 예에서는 도메인에 대 한 SPF TXT 레코드만 게시 했을 때 받는 사람의 메일 서버에서 전자 메일을 스팸으로 표시 했을 수 있고 가양성 결과를 생성 했습니다. 이 시나리오에서 dkim을 추가 하면 가양성 스팸 보고를 줄일 수 있습니다. dkim은 공개 키 암호화를 통해 IP 주소를 인증 하는 데 의존 하므로 dkim은 SPF 보다 더 강력한 형태의 인증으로 간주 됩니다. SPF 및 dkim과 DMARC을 모두 사용 하는 것이 좋습니다.
  
nitty 주요: dkim은 개인 키를 사용 하 여 메시지 헤더에 암호화 된 서명을 삽입 합니다. 서명 도메인 또는 아웃 바운드 도메인은 헤더에서 **d =** 필드의 값으로 삽입 됩니다. 확인 도메인 또는 받는 사람 도메인에서 **d =** 필드를 사용 하 여 DNS에서 공개 키를 조회 하 고 메시지를 인증 합니다. 메시지가 확인 되 면 dkim 검사가 통과 합니다. 
  
## <a name="what-you-need-to-do-to-manually-set-up-dkim-in-office-365"></a>Office 365에서 dkim을 수동으로 설정 하기 위해 수행 해야 하는 작업
<a name="SetUpDKIMO365"> </a>

dkim을 구성 하려면 다음 단계를 완료 합니다.
  
- [DNS에서 사용자 지정 도메인에 대 한 두 개의 CNAME 레코드 게시](use-dkim-to-validate-outbound-email.md#Publish2CNAME)
    
- [Office 365에서 사용자 지정 도메인에 대해 dkim 서명 사용](use-dkim-to-validate-outbound-email.md#EnableDKIMinO365)
    
### <a name="publish-two-cname-records-for-your-custom-domain-in-dns"></a>DNS에서 사용자 지정 도메인에 대 한 두 개의 CNAME 레코드 게시
<a name="Publish2CNAME"> </a>

DNS에서 dkim 서명을 추가 하려는 각 도메인에 대해 두 개의 CNAME 레코드를 게시 해야 합니다. DNS에서 CNAME 레코드를 사용 하 여 도메인의 정식 이름이 다른 도메인 이름의 별칭을 지정 합니다. 사용자 지정 된 도메인에 대해 공개적으로 사용 가능한 DNS 서버에 CNAME 레코드를 만들어야 합니다. dns의 CNAME 레코드는 이미 만들어진 Microsoft dns 서버 (Office 365 용)의 dns에 있는 레코드를 가리킵니다.
  
 Office 365에서는 설정한 두 레코드를 사용 하 여 자동 키 회전을 수행 합니다. Office 365의 초기 도메인 외에 사용자 지정 도메인을 프로 비전 한 경우에는 각 추가 도메인에 대해 두 개의 CNAME 레코드를 게시 해야 합니다. 따라서 도메인이 두 개 있는 경우 두 개의 추가 CNAME 레코드를 게시 해야 합니다.
  
CNAME 레코드에는 다음 형식을 사용 합니다.

> [!IMPORTANT]
> GCC High 고객 중 하나인 경우 _domainGuid_ 을 다르게 계산 합니다. _domainGuid_를 계산 하기 위해 _initialdomain_ 의 MX 레코드를 조회 하는 대신 사용자 지정 된 도메인에서 직접 계산 합니다. 예를 들어 사용자 지정 된 도메인이 "contoso.com" 이면 domainGuid가 "contoso-com"이 되 고 모든 기간은 대시로 바뀝니다. 따라서, initialdomain가 가리키는 MX 레코드에 관계 없이 항상 위의 메서드를 사용 하 여 CNAME 레코드에 사용할 domainGuid를 계산 합니다.

  
```
Host name:          selector1._domainkey
Points to address or value: selector1-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600

Host name:          selector2._domainkey
Points to address or value: selector2-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600
```

여기서 각 부분이 나타내는 의미는 다음과 같습니다.
  
- Office 365의 경우 선택기는 항상 "selector1" 또는 "selector2"입니다. 
    
- _domainGUID_ 는 mail.protection.outlook.com 앞에 표시 되는 사용자 지정 도메인에 대 한 사용자 정의 MX 레코드의 _domainGUID_ 과 동일 합니다. 예를 들어 contoso.com 도메인에 대 한 다음 MX 레코드에서 _domainGUID_ 는 contoso-com입니다. 
    
    ```
    contoso.com.  3600  IN  MX   5 contoso-com.mail.protection.outlook.com
    ```

- _initialdomain_ 은 Office 365에 등록할 때 사용한 도메인입니다. 초기 도메인은 항상 onmicrosoft.com으로 끝납니다. 초기 도메인을 결정 하는 방법에 대 한 자세한 내용은 [Domains FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조 하십시오.
    
예를 들어 cohovineyardandwinery.onmicrosoft.com의 초기 도메인과 두 개의 사용자 지정 도메인 cohovineyard.com 및 cohowinery.com가 있는 경우에는 각 추가 도메인에 대해 두 개의 cname 레코드를 설정 해야 하 고 총 4 개의 cname 레코드를 설정할 수 있습니다.
  
```
Host name:          selector1._domainkey
Points to address or value: **selector1-cohovineyard-com**._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:          selector2._domainkey
Points to address or value: **selector2-cohovineyard-com**._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:          selector1._domainkey
Points to address or value: **selector1-cohowinery-com**._domainkey.cohovineyardandwinery.onmicrosoft.com 
TTL:                3600
 
Host name:          selector2._domainkey
Points to address or value: **selector2-cohowinery-com**._domainkey.cohovineyardandwinery.onmicrosoft.com 
TTL:                3600
```

### <a name="enable-dkim-signing-for-your-custom-domain-in-office-365"></a>Office 365에서 사용자 지정 도메인에 대해 dkim 서명 사용
<a name="EnableDKIMinO365"> </a>

CNAME 레코드를 DNS에 게시 한 후에는 Office 365을 통해 dkim 서명을 사용 하도록 설정할 수 있습니다. Microsoft 365 관리 센터를 통해 또는 PowerShell을 사용 하 여이 작업을 수행할 수 있습니다.
  
#### <a name="to-enable-dkim-signing-for-your-custom-domain-through-the-admin-center"></a>관리 센터를 통해 사용자 지정 도메인에 대해 dkim 서명을 사용 하도록 설정 하려면

1. 회사 또는 학교 계정로 [Office 365에 로그인](https://support.office.microsoft.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4)합니다. 
    
2. 왼쪽 위에서 앱 시작 관리자 아이콘을 선택하고 **관리자**를 선택합니다.
    
3. 왼쪽 아래 탐색에서 **관리자** 를 확장 하 고 **Exchange**를 선택 합니다.
    
4. **보호** \> **dkim**으로 이동 합니다.
    
5. dkim을 사용 하도록 설정할 도메인을 선택 하 고 **이 도메인에 대해 dkim 서명을 사용 하 여 메시지를 서명**하려면 **사용**을 선택 합니다. 각 사용자 지정 도메인에 대해이 단계를 반복 합니다.
    
#### <a name="to-enable-dkim-signing-for-your-custom-domain-by-using-powershell"></a>PowerShell을 사용 하 여 사용자 지정 도메인에 대해 dkim 서명을 사용 하도록 설정 하려면

1. [Exchange Online PowerShell에 연결합니다](https://technet.microsoft.com/library/jj984289.aspx).
    
2. 다음 명령을 실행합니다.
    
    ```
    New-DkimSigningConfig -DomainName <domain> -Enabled $true
    ```

   여기서 _domain_ 은 dkim 서명을 사용 하도록 설정 하려는 사용자 지정 도메인의 이름입니다. 
    
   예를 들어 contoso.com 도메인의 경우 다음을 수행 합니다.
    
    ```
    New-DkimSigningConfig -DomainName contoso.com -Enabled $true
    ```

#### <a name="to-confirm-dkim-signing-is-configured-properly-for-office-365"></a>dkim 서명이 Office 365에 맞게 구성 되었는지 확인 하려면

이 단계를 수행 하 여 dkim을 올바르게 구성 했는지 확인 하려면 몇 분 정도 기다립니다. 이를 통해 도메인에 대 한 dkim 정보가 네트워크 전체에 분산 될 수 있습니다.
  
- Office 365 dkim을 사용 하는 도메인 내의 계정에서 outlook.com 또는 Hotmail.com 등의 다른 전자 메일 계정으로 메시지를 보냅니다.
    
- 테스트 목적으로 aol.com 계정을 사용 하지 마십시오. SPF 검사가 통과 하는 경우에는 AOL에서 dkim 검사를 건너뛸 수 있습니다. 이렇게 하면 테스트가 무효화 됩니다.
    
- 메시지를 열고 머리글을 확인 합니다. 메시지 헤더를 확인 하는 방법은 메시징 클라이언트에 따라 다릅니다. Outlook에서 메시지 헤더를 보는 방법에 대 한 자세한 내용은 [전자 메일 메시지 헤더 보기](https://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C)를 참조 하십시오.

  dkim 서명 된 메시지는 CNAME 항목을 게시할 때 정의한 호스트 이름과 도메인을 포함 합니다. 이 메시지는 다음과 같이 표시 됩니다. 
    
    ```
    From: Example User <example@contoso.com> 
    DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed; 
        s=selector1; d=contoso.com; t=1429912795; 
        h=From:To:Message-ID:Subject:MIME-Version:Content-Type; 
        bh=<body hash>; 
        b=<signed field>;
    ```

- 인증-결과 헤더를 찾습니다. 각 수신 서비스가 약간 다른 형식을 사용 하 여 받는 메일을 스탬프 처리 하지만이 결과에는 **dkim = pass** 또는 **dkim = OK**와 같은 내용이 포함 되어야 합니다. 
    
## <a name="to-configure-dkim-for-more-than-one-custom-domain-in-office-365"></a>Office 365에서 둘 이상의 사용자 지정 도메인에 대해 dkim을 구성 하려면
<a name="DKIMMultiDomain"> </a>

앞으로 다른 사용자 지정 도메인을 추가 하기로 결정 하 고 새 도메인에 대해 dkim을 사용 하도록 설정 하려는 경우에는 각 도메인에 대해이 문서의 단계를 완료 해야 합니다. 특히, [Office 365에서 dkim을 수동으로 설정 하기 위해 수행 해야](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365)하는 작업에 대 한 모든 단계를 완료 합니다.
  
## <a name="disabling-the-dkim-signing-policy-for-a-custom-domain-in-office-365"></a>Office 365에서 사용자 지정 도메인에 대해 dkim 서명 정책 사용 안 함
<a name="DisableDKIMSigningPolicy"> </a>

서명 정책을 사용 하지 않도록 설정 해도 dkim은 완전히 사용 하지 않도록 설정 되지 않습니다. 일정 시간 후에 office 365은 도메인에 대 한 기본 office 365 정책을 자동으로 적용 합니다. 자세한 내용은 [dkim 및 Office 365에 대 한 기본 동작](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)을 참조 하세요.
  
### <a name="to-disable-the-dkim-signing-policy-by-using-windows-powershell"></a>Windows PowerShell을 사용 하 여 dkim 서명 정책을 사용 하지 않도록 설정 하려면

1. [Exchange Online PowerShell에 연결합니다](https://technet.microsoft.com/library/jj984289.aspx).
    
2. dkim 서명을 사용 하지 않도록 설정할 각 도메인에 대해 다음 명령 중 하나를 실행 합니다.
    
    ```
    $p=Get-DkimSigningConfig -identity <domain>
    $p[0] | set-DkimSigningConfig -enabled $false
    ```

   예를 들면 다음과 같습니다.
    
    ```
    $p=Get-DkimSigningConfig -identity contoso.com
    $p[0] | set-DkimSigningConfig -enabled $false
    ```

   또는
    
    ```
    Set-DkimSigningConfig -identity $p[<number>].identity -enabled $false
    ```

    여기서 _number_ 는 정책의 인덱스입니다. 예를 들면 다음과 같습니다. 
    
    ```
    Set-DkimSigningConfig -identity $p[0].identity -enabled $false
    ```

## <a name="default-behavior-for-dkim-and-office-365"></a>dkim 및 Office 365에 대 한 기본 동작
<a name="DefaultDKIMbehavior"> </a>

dkim을 사용 하도록 설정 하지 않으면 Office 365에서 사용자 지정 도메인에 대 한 1024 비트 dkim 공개 키와 내부 데이터 센터에 저장 되는 연결 된 개인 키를 자동으로 만듭니다. 기본적으로 Office 365에서는 정책이 적용 되지 않은 도메인에 대해 기본 서명 구성을 사용 합니다. 즉, dkim을 직접 설정 하지 않으면 Office 365에서 도메인에 대해 dkim을 사용 하기 위해 만든 기본 정책과 키를 사용 합니다.
  
또한 dkim 서명을 사용 하지 않도록 설정한 후에는 일정 기간 후 office 365에서 도메인에 대 한 office 365 기본 정책을 자동으로 적용 합니다.
  
다음 예제에서는 도메인 관리자가 아니라 fabrikam.com에 대 한 dkim을 Office 365에서 사용 하도록 설정 했다고 가정 합니다. 이는 필수 cnames가 DNS에 없음을 의미 합니다. 이 도메인의 전자 메일에 대 한 dkim 서명이 다음과 같이 표시 됩니다.
  
```
From: Second Example <second.example@fabrikam.com> 
DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed; 
    s=selector1-fabrikam-com; d=contoso.onmicrosoft.com; t=1429912795; 
    h=From:To:Message-ID:Subject:MIME-Version:Content-Type; 
    bh=<body hash>; 
    b=<signed field>;
```

이 예에서 호스트 이름 및 도메인에는 fabrikam.com에 대 한 dkim 서명이 도메인 관리자에 의해 사용 하도록 설정 된 경우 CNAME이 가리킬 값이 포함 됩니다. 결국 Office 365에서 전송 되는 모든 단일 메시지는 dkim에 서명 됩니다. dkim을 직접 사용 하도록 설정 하는 경우 도메인은 From: 주소에서 도메인 (이 경우에는 fabrikam.com)과 동일 하 게 됩니다. 그렇지 않은 경우에는이를 정렬 하지 않고 조직의 초기 도메인을 대신 사용 합니다. 초기 도메인을 결정 하는 방법에 대 한 자세한 내용은 [Domains FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조 하십시오.
  
## <a name="set-up-dkim-so-that-a-third-party-service-can-send-or-spoof-email-on-behalf-of-your-custom-domain"></a>타사 서비스가 사용자 지정 도메인을 대신 하 여 전자 메일을 보내거나 스푸핑할 수 있도록 dkim을 설정 합니다.
<a name="SetUp3rdPartyspoof"> </a>

일부 대량 전자 메일 서비스 공급자 또는 a-a-서비스 공급자를 사용 하 여 서비스에서 보낸 전자 메일에 대해 dkim 키를 설정할 수 있습니다. 이를 위해서는 필요한 DNS 레코드를 설정 하기 위해 자신과 타사 간의 조정이 필요 합니다. 두 조직이 동일 하 게 똑같은 방식으로 작업을 수행 하지는 않습니다. 대신, 프로세스는 전적으로 조직에 따라 달라 집니다.
  
contoso.com 및 bulkemailprovider.com에 대해 올바르게 구성 된 dkim을 보여 주는 예제 메시지는 다음과 같습니다.
  
```
Return-Path: <communication@bulkemailprovider.com>
 From: <sender@contoso.com>
 DKIM-Signature: s=s1024; d=contoso.com
 Subject: Here is a message from Bulk Email Provider's infrastructure, but with a DKIM signature authorized by contoso.com
```

이 예에서는 다음과 같은 결과를 얻을 수 있습니다.
  
1. 대량 전자 메일 공급자는 Contoso에 공개 dkim 키를 제공 합니다.
    
2. Contoso는 dkim 키를 해당 DNS 레코드에 게시 했습니다.
    
3. 전자 메일을 보낼 때 대량 전자 메일 공급자는 해당 개인 키를 사용 하 여 키에 서명 합니다. 이렇게 하면 대량 전자 메일 공급자가 메시지 헤더에 dkim 서명을 첨부 합니다.
    
4. 수신 전자 메일 시스템 메시지의 보낸 사람: (5322.from 주소의) 주소에서 도메인에 대해\<dkim-Signature d = 도메인\> 값을 인증 하 여 dkim 검사를 수행 합니다. 이 예에서는 값이 다음과 같이 일치 합니다.
    
    보낸 사람 @**contoso.com**
    
    d =**contoso.com**
    
## <a name="next-steps-after-you-set-up-dkim-for-office-365"></a>다음 단계: Office 365에 대 한 dkim을 설정한 후
<a name="DKIMNextSteps"> </a>

dkim은 스푸핑을 방지 하기 위해 디자인 되었지만 SPF 및 DMARC에서는 dkim이 더 효율적으로 작동 합니다. dkim을 설정한 후에 SPF를 설정 하지 않은 경우에는이 작업을 수행 해야 합니다. spf에 대 한 간략 한 소개 및 신속한 구성에 대 한 자세한 내용은 [스푸핑을 방지 하기 위해 Office 365에서 spf를 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)합니다 .를 참조 하세요. office 365에서 spf를 사용 하는 방법과 하이브리드 배포와 같은 문제 해결 또는 비표준 배포를 자세히 이해 [하려면 office 365에서 spf (Sender Policy Framework)를 사용 하 여 스푸핑을 방지](how-office-365-uses-spf-to-prevent-spoofing.md)하는 방법을 시작 합니다. 그런 다음 [Office 365에서 DMARC을 사용 하 여 전자 메일의 유효성 검사를](use-dmarc-to-validate-email.md)참조 하세요. [스팸 방지 메시지 헤더](anti-spam-message-headers.md) 에는 dkim 검사에 대 한 Office 365에서 사용 하는 구문 및 헤더 필드가 포함 되어 있습니다. 
  

