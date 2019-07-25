---
title: 스푸핑을 방지할 수 있도록 Office 365에서 SPF 설정
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 2/19/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 71373291-83d2-466f-86ea-fc61493743a6
ms.collection:
- M365-security-compliance
description: 요약:이 문서에서는 Office 365의 사용자 지정 도메인과 함께 SPF (보낸 사람 정책 프레임 워크)를 사용할 수 있도록 DNS (도메인 이름 서비스) 레코드를 업데이트 하는 방법을 설명 합니다. SPF를 사용 하면 사용자 지정 도메인에서 전송 되는 아웃 바운드 전자 메일의 유효성을 검사할 수 있습니다.
ms.openlocfilehash: 15472900986a367e084c6126580cef85d286a94b
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854792"
---
# <a name="set-up-spf-in-office-365-to-help-prevent-spoofing"></a>스푸핑을 방지할 수 있도록 Office 365에서 SPF 설정

 **요약:** 이 문서에서는 Office 365의 사용자 지정 도메인과 함께 SPF (보낸 사람 정책 프레임 워크)를 사용할 수 있도록 DNS (도메인 이름 서비스) 레코드를 업데이트 하는 방법을 설명 합니다. SPF를 사용 하면 사용자 지정 도메인에서 전송 되는 아웃 바운드 전자 메일의 유효성을 검사할 수 있습니다. 
  
사용자 지정 도메인을 사용 하려면 Office 365에서 스푸핑을 방지 하는 데 도움이 되도록 SPF (Sender Policy Framework) TXT 레코드를 DNS 레코드에 추가 해야 합니다. SPF는 사용자를 대신 하 여 메일을 보낼 수 있는 메일 서버를 식별 합니다. 기본적으로 SPF는 DKIM, DMARC 및 Office 365에서 지 원하는 기타 기술과 함께 스푸핑 및 피싱 방지를 지원 합니다. SPF는 DNS에서 사용자 지정 도메인을 대신 하 여 메일을 보낼 수 있는 메일 서버를 식별 하는 데 사용 되는 TXT 레코드로 추가 됩니다. 받는 사람 메일 시스템은 SPF TXT 레코드를 참조 하 여 사용자 지정 도메인의 메시지가 권한 있는 메시징 서버에서 온 것인지를 확인 합니다.
  
예를 들어 사용자 지정 도메인 contoso.com가 Office 365을 사용 한다고 가정해 보겠습니다. Office 365 메시징 서버가 도메인의 합법적인 메일 서버로 나열 되는 SPF TXT 레코드를 추가 합니다. 수신 메시징 서버가 joe@contoso.com에서 메시지를 받는 경우 서버는 contoso.com에 대 한 SPF TXT 레코드를 조회 하 고 메시지가 유효한 지 여부를 확인 합니다. 받는 서버가 SPF 레코드에 나열 된 Office 365 메시징 서버가 아닌 다른 서버에서 보낸 메시지를 발견 하면 받는 메일 서버에서 해당 메시지를 스팸으로 거부 하도록 선택할 수 있습니다.
  
또한 사용자 지정 도메인에 SPF TXT 레코드가 없는 경우 일부 받는 서버에서 메시지를 전혀 거부할 수 있습니다. 이는 받는 서버가 승인 된 메시징 서버에서 보낸 메시지를 확인할 수 없기 때문입니다.
  
이미 Office 365에 대 한 메일을 설정한 경우 Microsoft의 메시징 서버가 이미 SPF TXT 레코드로 DNS에 포함 되어 있습니다. 그러나 DNS에서 SPF TXT 레코드를 업데이트 해야 하는 경우도 있습니다. 예를 들면 다음과 같습니다.
  
- 이전에는 SharePoint Online을 사용 하는 경우 다른 SPF TXT 레코드를 사용자 지정 도메인에 추가 해야 했습니다. 이제 이 작업은 필요하지 않습니다. 이렇게 변경 하면 SharePoint Online 알림 메시지가 정크 메일 폴더에서 끝나는 위험을 줄일 것입니다. 10 개의 조회 제한 및 "조회 제한 초과" 및 "너무 많은 홉"을 표시 하는 오류를 수신 하는 경우 SPF TXT 레코드를 업데이트 합니다.
    
- Office 365 및 Exchange 온-프레미스를 사용 하는 하이브리드 환경에서는
    
- DKIM 및 DMARC을 설정 하려고 합니다 (권장).
    
## <a name="updating-your-spf-txt-record-for-office-365"></a>Office 365에 대 한 SPF TXT 레코드 업데이트

DNS에서 TXT 레코드를 업데이트 하기 전에 몇 가지 정보를 수집 하 고 레코드 형식을 확인 해야 합니다. 이를 통해 DNS 오류를 생성 하지 못할 수 있습니다. 지원 되는 SPF 구문에 대 한 자세한 내용은 [spf이 작동 하 여 Office 365에서 스푸핑 및 피싱 방지 방법을](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks)참조 하세요.
  
다음 정보를 수집 합니다.
  
- 사용자 지정 도메인에 대 한 현재 SPF TXT 레코드입니다. 자세한 내용은 [Office 365 DNS 레코드를 만드는 데 필요한 정보 수집](https://support.office.microsoft.com/en-us/article/Gather-the-information-you-need-to-create-Office-365-DNS-records-77f90d4a-dc7f-4f09-8972-c1b03ea85a67)을 참조 하십시오.
    
- 모든 온-프레미스 메시징 서버의 IP 주소 예를 들면 **192.168.0.1**입니다.
    
- SPF TXT 레코드에 포함 해야 하는 모든 타사 도메인에 사용할 도메인 이름입니다. 일부 대량 메일 공급자는 고객에 게 사용할 하위 도메인을 설정 했습니다. 예를 들어 회사 MailChimp에는 **servers.mcsv.net**이 설정 되어 있습니다.
    
- SPF TXT 레코드에 사용할 적용 규칙을 결정 합니다. **-All**이 권장 됩니다. 다른 구문 옵션에 대 한 자세한 내용은 [SPF TXT record 구문만 For Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFSyntaxO365)을 참조 하십시오.
    
### <a name="to-add-or-update-your-spf-txt-record"></a>SPF TXT 레코드를 추가 하거나 업데이트 하려면

1. 아직 수행 하지 않은 경우 다음 표의 구문을 사용 하 여 SPF TXT 레코드를 구성 합니다.
    
||**사용 중인 경우 ...**|**Office 365 고객에 대 한 일반적인 사항**|**추가할 추가 ...**|
|:-----|:-----|:-----|:-----|
|1   <br/> |모든 전자 메일 시스템 (필수)  <br/> |대개. 이 값으로 시작 하는 모든 SPF TXT 레코드  <br/> |v=spf1  <br/> |
|2   <br/> |Exchange Online  <br/> |대개  <br/> |포함:spf.protection.outlook.com  <br/> |
|3   <br/> |Exchange Online 전용  <br/> |공통 아님  <br/> |ip4:23.103.224.0/19 ip4:206.191.224.0/19 ip4:40.103.0.0/16 include.  <br/> |
|4   <br/> |Office 365 독일, Microsoft 클라우드 독일에만 해당  <br/> |공통 아님  <br/> |다음을 포함 합니다.  <br/> |
|5   <br/> |타사 전자 메일 시스템  <br/> |공통 아님  <br/> |포함:\<도메인 이름\>  <br/> 여기서 도메인 이름은 타사 전자 메일 시스템의 도메인 이름입니다.  <br/> |
|6   <br/> |온-프레미스 메일 시스템 예를 들어 Exchange Online Protection과 다른 메일 시스템  <br/> |공통 아님  <br/> | 각각의 추가 메일 시스템에 대해 다음 중 하나를 사용 합니다.  <br/>  ip4:\<  _IP 주소_\>  <br/>  ip6:\<  _IP 주소_\>  <br/>  포함:\<  _도메인 이름_\>  <br/>  여기서 \< _ip 주소_ \> 값은 다른 메일 시스템의 ip 주소이 고 \< 도메인 _이름은_ \> 도메인을 대신 하 여 메일을 전송 하는 다른 메일 시스템의 도메인 이름입니다.    <br/> |
|7   <br/> |모든 전자 메일 시스템 (필수)  <br/> |대개. 모든 SPF TXT 레코드가이 값으로 끝납니다.  <br/> |\<_적용 규칙_\>  <br/> 여러 값 중 하나일 수 있습니다. **-All**을 사용 하는 것이 좋습니다.  <br/> |
   
1.1 예를 들어, Office 365에서 완전히 호스트 되는 경우, 즉 온-프레미스 메일 서버가 없는 경우 SPF TXT 레코드에는 1, 2, 7 행이 포함 되며 다음과 같이 표시 됩니다.
    
  ```
   v=spf1 include:spf.protection.outlook.com -all
  ```

1.2이는 가장 일반적인 Office 365 SPF TXT 레코드입니다. 이 레코드는 Office 365 datacenter가 미국에 있는지, 유럽 (독일 포함) 중 어디에 있든, 다른 위치에 있든 관계 없이 모든 사용자에 대해서만 작동 합니다.
    
1.3 그러나 Microsoft Cloud 전라남도 일부를 365 구매한 경우에는 line 2 대신 4 행에서 include 문을 사용 해야 합니다. 예를 들어, Office 365 독일에서 완전히 호스트 되는 경우, 즉 온-프레미스 메일 서버가 없는 경우 SPF TXT 레코드에는 1, 4, 7 행이 포함 되며 다음과 같이 표시 됩니다.
    
  ```
   v=spf1 include:spf.protection.outlook.de -all
  ```

1.4 Office 365에서 이미 배포 되었으며 사용자 지정 도메인에 대 한 SPF TXT 레코드를 설정 했으며 Office 365 독일으로 마이그레이션 중인 경우 SPF TXT 레코드를 업데이트 해야 합니다. 이렇게 하려면 다음을 수행 하 여 spf.. c a d .를 **포함**하는. **|**
    
2. SPF TXT 레코드를 구성한 후에는 DNS에서 레코드를 업데이트 해야 합니다. 하나의 도메인에 대해서만 SPF TXT 레코드를 하나만 사용할 수 있습니다. 새 레코드를 추가 하는 대신 SPF TXT 레코드가 있으면 기존 레코드를 업데이트 해야 합니다. [Office 365에 대 한 dns 레코드 만들기](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider?view=o365-worldwide)로 이동 하 고 dns 호스트에 대 한 링크를 클릭 합니다. 
    
3. SPF TXT 레코드를 테스트 합니다.
    
## <a name="more-information-about-spf"></a>SPF에 대 한 추가 정보

고급 예제를 보려면 지원 되는 SPF 구문, 스푸핑, 문제 해결 및 Office 365에서 SPF를 지 원하는 방법에 대 한 자세한 내용은 [spf works를 통해 office 365에서 스푸핑 및 피싱 방지](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks)를 참조 하세요.
  
## <a name="next-steps-after-you-set-up-spf-for-office-365"></a>다음 단계: Office 365에 대 한 SPF를 설정한 후

SPF TXT 레코드에 문제가 있나요? [문제 해결 방법: Office 365에서 SPF에 대 한 모범 사례](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot)를 제공 합니다.
  
 SPF는 스푸핑을 방지 하기 위해 설계 되었지만 SPF에서 보호할 수 없는 스푸핑 기법이 있습니다. 이를 방지 하기 위해 SPF를 설정한 후에는 Office 365에 대해 DKIM 및 DMARC도 구성 해야 합니다. 시작 하려면 [DKIM을 사용 하 여 Office 365의 사용자 지정 도메인에서 전송 되는 아웃 바운드 전자 메일의 유효성 검사](use-dkim-to-validate-outbound-email.md)를 참조 하세요. 그런 다음 [Office 365에서 DMARC을 사용 하 여 전자 메일의 유효성 검사를](use-dmarc-to-validate-email.md)참조 하세요.
  

