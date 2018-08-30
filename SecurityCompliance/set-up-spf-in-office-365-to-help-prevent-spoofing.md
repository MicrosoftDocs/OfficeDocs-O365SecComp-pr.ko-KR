---
title: 스푸핑을 방지할 수 있도록 Office 365에서 SPF 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 2/19/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 71373291-83d2-466f-86ea-fc61493743a6
description: 요약:이 문서에서는 Office 365에서 사용자 지정 도메인으로 보낸 사람이 정책 프레임 워크 (SPF)를 사용할 수 있도록 서비스 DNS (Domain Name) 레코드를 업데이트 하는 방법에 설명 합니다. SPF을 사용 하면 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사 합니다.
ms.openlocfilehash: 9c03f69cfd0c962214a3adc722690a4288940541
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002887"
---
# <a name="set-up-spf-in-office-365-to-help-prevent-spoofing"></a>스푸핑을 방지할 수 있도록 Office 365에서 SPF 설정

 **요약:** 이 문서에서는 Office 365에서 사용자 지정 도메인으로 보낸 사람이 정책 프레임 워크 (SPF)를 사용할 수 있도록 서비스 DNS (Domain Name) 레코드를 업데이트 하는 방법에 설명 합니다. SPF을 사용 하면 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사 합니다. 
  
사용자 지정 도메인을 사용 하려면 Office 365를 스푸핑 방지 하려면 DNS 레코드의 보낸 사람이 정책 프레임 워크 (SPF) TXT 레코드를 추가 해야 합니다. SPF 사용자를 대신 하 여 메일을 보낼 수 있는 메일 서버를 식별 합니다. DKIM, DMARC, 및 기타 함께 SPF 기본적으로, Office 365에서 지 원하는 기술 도움말 스푸핑 및 피싱 방지 합니다. SPF 사용자 지정 도메인을 대신 하 여 메일을 보낼 수 있는 메일 서버를 식별 하려면 DNS에 사용 되는 TXT 레코드를으로 추가 됩니다. 권한이 부여 된 메시징 서버에서 받는 사람 메일 시스템을 사용자 지정 도메인에서 메시지 있는지 여부를 확인 하려면 SPF TXT 레코드를 참조를 가져옵니다.
  
예, 사용자 지정 도메인 contoso.com에서는 Office 365 사용 되는 가정해 보겠습니다. 도메인의 합법적인 메일 서버로 Office 365 메시징 서버를 나열 하는 SPF TXT 레코드를 추가 합니다. 수신 메시징 서버 joe@contoso.com에서 메시지를 받으면 서버가 contoso.com에 대 한 SPF TXT 레코드를 조회 하 고는 메시지가 유효한 지 여부를 찾습니다. 받는 서버 Office 365 이외의 다른 서버에서 메시지 나오도록 SPF 레코드에 나열 된 서버를 메시징 데이터를 찾으면 받는 메일 서버는 스팸 메시지를 거부 하 하도록 선택할 수 있습니다.
  
또한, 사용자 지정 도메인 SPF TXT 레코드를이 없는 경우 일부 받는 서버 완전 한 메시지를 거부할 수 있습니다. 즉, 받는 서버에서 권한이 부여 된 메시징 서버에서 메시지 나오도록를 확인할 수 없습니다.
  
했을 때 이미 설정한 경우 메일을 Office 365에 대 한 SPF TXT 레코드를으로 DNS에 Microsoft의 메시징 서버를 이미 포함 합니다. 그러나 DNS의 프로그램 SPF TXT 레코드를 업데이트 해야 경우도 있습니다. 예를 들어:
  
- 이전에 SharePoint Online 사용 중이 던 하는 경우 사용자 지정 도메인에 다른 SPF TXT 레코드를 추가 했습니다. 이 더이상 필요 합니다. 이 변경의 정크 메일 폴더에서 종료 하는 SharePoint Online 알림 메시지의 위험을 줄이려면 해야 합니다. 10 조회 한계 고 등, "제한을 초과 했습니다. 조회" 라고 표시 하는 오류를 수신 하는 경우 SPF TXT 레코드를 업데이트 하 고 "홉이 너무 많습니다." 합니다.
    
- Office 365 하이브리드 환경을 사용 하는 및 Exchange 온-프레미스 하는 경우
    
- DKIM 및 DMARC (권장)를 설정 하 려 한다고 합니다.
    
## <a name="updating-your-spf-txt-record-for-office-365"></a>Office 365에 대 한 SPF TXT 레코드를 업데이트합니다.
<a name="sectionSection0"> </a>

DNS에서 TXT 레코드를 업데이트 하기 전에 일부 정보를 수집 하 고 레코드의 형식을 결정 해야 합니다. DNS 오류가 일시적 오류로 생성 (영문)에서 차단 하는 데 도움이 됩니다. 고급 예제에 대 한 지원 되는 SPF 구문에 대 한 자세한 내용은 [스푸핑을 방지 하기 위해 SPF 어떻게 작동 하 고 Office 365의 피싱을](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks)참조 합니다.
  
이 정보를 수집 합니다.
  
- 사용자 지정 도메인에 대 한 현재 SPF TXT 레코드를 지정 합니다. 자세한 내용은 [Office 365 DNS 레코드를 만들어야 할 정보를 수집](https://support.office.microsoft.com/en-us/article/Gather-the-information-you-need-to-create-Office-365-DNS-records-77f90d4a-dc7f-4f09-8972-c1b03ea85a67)합니다.
    
- 모든 IP 주소 온-프레미스 메시징 서버. 예: **192.168.0.1**합니다.
    
- SPF TXT 레코드를 포함 하는 모든 타사 도메인에 대해 사용 하 여 도메인 이름입니다. 일부 대량 메일 공급자가 고객을 위해 사용 하 여 하위 도메인을 설정 합니다. 예, 회사 MailChimp 설정한 **servers.mcsv.net**합니다.
    
- SPF TXT 레코드에 대해 사용 하려는 어떤 적용 규칙을 결정 합니다. 것이 좋습니다 **-모든**합니다. 다른 구문 옵션에 대 한 자세한 내용은 [Office 365에 대 한 SPF TXT 레코드 syntax](how-office-365-uses-spf-to-prevent-spoofing.md#SPFSyntaxO365)를 참조 하십시오.
    
### <a name="to-add-or-update-your-spf-txt-record"></a>추가 하거나 SPF TXT 레코드를 업데이트 하려면

1. 이미 수행 하는 경우 다음 표에 나와있는 구문을 사용 하 여 SPF TXT 레코드를 형성 합니다.
    
||**사용 중인 경우...**|**Office 365 고객을 위한 일반적인?**|**이 추가...**|
|:-----|:-----|:-----|:-----|
|1  <br/> |용도  <br/> |일반적인 합니다. 이 값을 가진 모든 SPF TXT 레코드 시작  <br/> |v = spf1  <br/> |
|2   <br/> |Exchange Online  <br/> |일반  <br/> |include:spf.protection.outlook.com  <br/> |
|3  <br/> |Exchange Online만 전용  <br/> |일반적으로 해당 되지  <br/> |ip4:23.103.224.0/19 ip4:206.191.224.0/19 ip4:40.103.0.0/16 include:spf.protection.outlook.com  <br/> |
|4  <br/> |Office 365 독일, Microsoft 클라우드 독일만  <br/> |일반적으로 해당 되지  <br/> |include:spf.protection.outlook.de  <br/> |
|5  <br/> |타사 전자 메일 시스템  <br/> |일반적으로 해당 되지  <br/> |포함:\<도메인 이름\>  <br/> 여기서 도메인 이름은 타사 전자 메일 시스템의 도메인 이름입니다.  <br/> |
|6  <br/> |온-프레미스 메일 시스템입니다. 예, Exchange Online Protection와 다른 메일 시스템  <br/> |일반적으로 해당 되지  <br/> | 각 추가 메일 시스템에 대 한 둘 중 하나를 사용 합니다.  <br/>  ip4:\<  _IP 주소_\>  <br/>  i p 6:\<  _IP 주소_\>  <br/>  포함:\<  _도메인 이름_\>  <br/>  위치에 대 한 값 \< _IP 주소_ \> 는 다른 메일 시스템의 IP 주소 및 \< _도메인 이름_ \> 메일을 보내는 도메인을 대신 하 여 다른 메일 시스템의 도메인 이름입니다.    <br/> |
|7   <br/> |include:<mail.contoso.com>  <br/> |일반적인 합니다. 이 값으로 끝나는 모든 SPF TXT 레코드  <br/> |\<_적용 규칙_\>  <br/> 여러 값 중 하나일 수 있습니다이 있습니다. 사용 하는 것이 좋습니다 **-모든**합니다.<br/> |
   
1.1 등 인 경우 Office 365에서 완벽 하 게 호스트 하는 경우, 즉 해야 온-프레미스 메일 서버 없음 대화 SPF TXT 레코드 1, 2, 7 행에는 포함 하 고은 다음과 같습니다.
    
  ```
   v=spf1 include:spf.protection.outlook.com -all
  ```

1.2 가장 일반적인 Office 365 SPF TXT 레코드입니다. 이 레코드에 대해 모든 사용자를 위한 여부에 관계 없이 Office 365 데이터 센터 위치는 미국 또는 유럽 (독일 포함) 또는 다른 위치에 사용할 수 있습니다.
    
그러나 1.3 Office 365 독일, Microsoft 클라우드 독일의 일부를 구입한 경우 선 4에서에서 include 문을 줄 2 하는 대신 사용 해야 합니다. 예 인 경우 Office 365 독일에 완벽 하 게 호스트 하는 경우, 즉 해야 온-프레미스 메일 서버 없음 대화 SPF TXT 레코드 1, 4, 7 행에는 포함 하 고은 다음과 같습니다.
    
  ```
   v=spf1 include:spf.protection.outlook.de -all
  ```

1.4 하는 경우 Office 365에서 이미 배포 된 하 고 사용자 지정 도메인에 대 한 SPF TXT 레코드를 설정 하 고 Office 365 독일으로 마이그레이션하는, SPF TXT 레코드를 업데이트 해야 합니다. 이 작업을 수행 하려면 **include:spf.protection.outlook.com** **include.spf.protection.outlook.de**로 변경 합니다.
    
2. SPF TXT 레코드를 세운 후에 dns에서 레코드를 업데이트 해야 합니다. 도메인에 대 한 SPF TXT 레코드를 하나만 사용할 수 있습니다. 새 레코드를 추가 하는 대신 하는 SPF TXT 레코드 존재 하는 경우 기존 레코드를 업데이트 해야 합니다. [Office 365 용 DNS 레코드 만들기](https://support.office.microsoft.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23)이동 하 고 DNS 호스트에 대 한 링크를 클릭 합니다. (DNS 호스트가 없으면 링크 페이지에서 할 수 있습니다 레코드를 추가 하거나 도움말에 대 한 DNS 호스트에 게 문의에 대 한 [일반적인 지침을 따릅니다](https://support.office.microsoft.com/article/7b7b075d-79f9-4e37-8a9e-fb60c1d95166) .) 
    
3. SPF TXT 레코드를 테스트 합니다.
    
## <a name="more-information-about-spf"></a>SPF 하는 방법에 대 한 자세한 내용
<a name="sectionSection1"> </a>

고급 예제에 대 한 지원 되는 SPF 구문을, 스푸핑, 문제를 해결 하 고 SPF, Office 365를 지 원하는 방법에 대 한 자세한 내용은 [위조 및 Office 365의 피싱 방지 하기 위해 작동 하는 방법을 SPF](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks)참조 하십시오.
  
## <a name="next-steps-after-you-set-up-spf-for-office-365"></a>다음 단계: Office 365에 대 한 SPF를 설정한 후
<a name="sectionSection2"> </a>

SPF TXT 레코드와 함께 문제가 있습니까? 읽기 [문제해결: Office 365에서 SPF에 대 한 모범 사례](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot)합니다.
  
 SPF 위조를 방지 하려면 디자인 하지만 스푸핑 기술에 SPF를 보호할 수 없습니다. SPF를 설정 하 고 나면 이러한 경우에 대해 보호 하기 위해도 구성 해야 DKIM 및 DMARC Office 365에 대 한 합니다. 시작 하기 위해 [Office 365에서 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사를 사용 하 여 DKIM](use-dkim-to-validate-outbound-email.md)를 참조 합니다. 다음으로, [Office 365의 전자 메일의 유효성을 검사를 사용 하 여 DMARC](use-dmarc-to-validate-email.md)를 참조 하십시오.
  

