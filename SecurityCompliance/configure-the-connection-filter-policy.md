---
title: 연결 필터 정책 구성
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/24/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6ae78c12-7bbe-44fa-ab13-c3768387d0e3
description: 사람을 신뢰 하에서 보낸 전자 메일 차단 되지 않습니다 있는지 확인 하십시오로 알려져는 수신 허용-보낸사람, IP 주소 목록에 신뢰할 수 있는 허용 목록을 만들려면 연결 필터 정책을 사용할 수 있습니다. 수신된 거부 목록을 만들 수도 있습니다.
ms.openlocfilehash: 2f8ec3d01de4358d7394c68d0efae9222db08282
ms.sourcegitcommit: a07b91723bae9ecee2cb092bfbc5b208b30b11a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "25793563"
---
# <a name="configure-the-connection-filter-policy"></a>연결 필터 정책 구성
 
대부분의 경우 친구 및 비즈니스 파트너는 신뢰 스팸 필터에 의해 완전히 차단도 또는 전자 메일을 정크 메일 폴더, 찾으려고 실망 수 있습니다. 사람을 신뢰 하에서 보낸 전자 메일 차단 되지 않습니다, 연결 필터 정책을 사용 하 여 수신 허용-보낸사람 목록으로도 알려져 허용 목록을 만들려면 않았는지 확인 하려는 경우 ip 주소를 트러스트 하. 전자 메일 메시지를 받을 전혀 원하지 않는 알려진된 스팸 메일에서 일반적으로 IP 주소 목록에 해당 하는 수신된 거부 목록을 만들 수도 있습니다.
  
 조직 전체에 적용 하는 자세한 스팸 설정에 대 한 [메시지를 스팸으로 표시 되지 않습니다을 보장 하는 방법](https://go.microsoft.com/fwlink/p/?LinkId=534224) 또는 [false 이면 음수 문제를 방지 하기 위해 Office 365 스팸 필터와 스팸 차단 전자 메일](https://go.microsoft.com/fwlink/p/?LinkId=534225)에 대 한 정보를 수행 합니다. 다음은 관리자 수준의 제어 있고 가양성 또는 잘못 된 음수가 되지 않도록 하려는 경우에 유용 합니다.
  
다음 비디오에서는 연결 필터 정책의 구성 단계를 보여 줍니다.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/b2f5bea3-e1a7-44b3-b7e2-07fac0d0ca40?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용
<a name="sectionSection0"> </a>

- 예상 완료 시간: 15분
    
- 이 절차를 수행 하기 전에 사용 권한을 할당 해야 합니다. 필요한 사용 권한을 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 항목의 "스팸 방지" 항목을 참조 하십시오. 
    
- 보낸 사람이 메시지를 허용 하거나 차단할 IP 주소를 얻으려면 메시지의 인터넷 헤더를 확인할 수 있습니다. [스팸 방지 메시지 헤더](anti-spam-message-headers.md)에서 설명한 대로 CIP 헤더를 찾습니다. 다양 한 전자 메일 클라이언트에서 메시지 헤더를 확인 하는 방법에 대 한 정보를 [메시지 헤더 분석기](https://go.microsoft.com/fwlink/p/?LinkId=306583)를 참조 하십시오. 
    
- 스팸으로 표시도 하지 IP 차단 목록에 IP 주소에서 보내는 전자 메일 메시지는 거부 하 고 추가 필터링이 발생 합니다.
    
- 원격 PowerShell을 통해 다음 연결 필터 절차를 수행할 수도 있습니다. 검토 하 여 설정 하 고 연결 필터 정책 설정을 편집 하려면 [Set-hostedconnectionfilterpolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) [Get HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) cmdlet을 사용 합니다. Exchange Online Protection에 연결 하려면 Windows PowerShell을 사용 하는 방법을 알아보려면 [Connect to Exchange Online Protection PowerShell를](https://go.microsoft.com/fwlink/p/?linkid=627290)참조 하십시오. Exchange Online에 연결 하려면 Windows PowerShell을 사용 하는 방법을 알아보려면 [Exchange Online PowerShell 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조 하십시오.
    
## <a name="use-the-eac-to-edit-the-default-connection-filter-policy"></a>EAC를 사용하여 기본 연결 필터 정책 편집
<a name="sectionSection1"> </a>

EAC(Exchange 관리 센터)에서 연결 필터 정책을 편집하여 IP 허용 목록 또는 IP 차단 목록을 만듭니다. 연결 필터 정책 설정은 인바운드 메시지에만 적용됩니다.
  
1. EAC(Exchange 관리 센터)에서 **보호** \> **연결 필터**로 이동한 후 기본 정책을 두 번 클릭합니다.
    
2. **연결 필터링** 메뉴 항목을 클릭한 후 원하는 목록을 만듭니다. IP 허용 목록이나 IP 차단 목록 중 하나를 만들거나 두 목록을 모두 만들 수 있습니다. 
    
    이 목록을 만들려면 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif)를 클릭합니다. 이후 표시되는 대화 상자에서 IP 주소나 주소 범위를 지정한 후 **확인**을 클릭합니다. 주소를 추가하려면 이 프로세스를 반복합니다. 주소를 추가한 후 IP 주소를 편집하거나 제거할 수도 있습니다.
    
    > [!NOTE]
    >  두 목록에 IP 주소를 추가 하는 경우 해당 IP 주소에서 보낸 전자 메일 허용 됩니다. 

    여기서 nnn는 0에서 255 까지의 숫자 형식 nnn.nnn.nnn.nnn에서 IPV4 IP 주소를 지정 합니다. 여기서 rr는 24에서 32 사이의 숫자 형식 nnn.nnn.nnn.nnn/rr에서 도메인간 라우팅 CIDR (Classless) 범위를 지정할 수도 있습니다. 24-32 범위 외부의 범위를 지정 하려면 [IP 허용 구성 시 추가 고려 사항 목록](configure-the-connection-filter-policy.md#bkmk_addtionalconsiderationswhenconfiguringipallowlists)를 참조 합니다. 

    최대 1273 항목, 항목은 단일 IP 주소 또는 CIDR의 IP 주소 범위에서 /24/32 지정할 수 있습니다. > TLS 암호화 된 메시지를 보내는 경우 IPv6 주소 및 주소 범위가 지원 되지 않습니다. 
  
3. 필요한 경우를 방지 하기 위해 **수신 허용 목록 사용** 확인란을 선택 특정 잘 알려진 보낸에서 전자 메일이 누락 되었습니다. 어떻게 합니까? Microsoft의 신뢰할 수 있는 보낸사람 제 3 자 원본에 구독합니다. 수신 허용 목록에이 사용 하 여 이러한 신뢰할 수 있는 보낸사람 스팸으로 표시 실수로 되지 하는 것을 의미 합니다. 가양성 (스팸으로 분류 하는 효율적인 메일)의 수를 줄일 해야 하기 때문에이 옵션을 선택 하는 것이 좋습니다에 도입 된 합니다. 
    
4. **저장**을 클릭합니다. 기본 정책 설정에 대한 요약이 오른쪽 창에 표시됩니다.
    
## <a name="additional-considerations-when-configuring-ip-allow-lists"></a>IP 허용 목록 구성 시 추가 고려 사항
<a name="bkmk_addtionalconsiderationswhenconfiguringipallowlists"> </a>

다음은 IP 허용 목록 구성 시 고려해야 하거나 알고 있어야 하는 추가 고려 사항입니다.
  
### <a name="specifying-a-cidr-range-that-falls-outside-of-the-recommended-range"></a>권장되는 범위를 벗어나는 CIDR 범위 지정

**바이패스 스팸 필터링** (의미는이 IP 주소 범위 내에서 받은 모든 메시지를 포함 하는 신뢰도 scl (스팸)를 설정 하는 IP 주소 범위에서 작동 하는 메일 흐름 규칙을 생성 해야 하는 /23/1에서 CIDR IP 주소 범위를 지정 하려면 "스팸 하지"로 설정 된) 추가 필터링 하지 않고 서비스에 의해 수행 되 고). 그러나 이러한 IP 주소 중 하나에 표시 하는 경우 목록 Microsoft의 소유 블록의 일부 또는 모든 타사 차단 목록, 이러한 메시지를 차단 계속 됩니다. 따라서 강력 하 게 좋습니다 /24/32 IP 주소 범위를 사용 하는. 
  
이 메일 흐름 규칙을 만들려면 다음 단계를 수행 합니다.
  
1. EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.
    
2. ![아이콘 추가](media/ITPro-EAC-AddIcon.gif)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.
    
3. 규칙 이름을 지정하고 **기타 옵션**을 클릭합니다.
    
4. **다음의 경우 이 규칙 적용**에서 **보낸 사람**을 선택하고 **IP 주소가 이 범위에 속하거나 정확하게 일치함**을 선택합니다.
    
5. **IP 주소를 지정**하십시오에서 IP 주소 범위를 지정, **추가** 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif), **확인**을 클릭 하 고 있습니다.
    
6. **다음 작업 수행** 상자에서 **메시지 속성 수정**을 선택한 다음 **SCL(스팸 지수) 설정**을 선택하여 동작을 설정합니다. **SCL 지정** 상자에서 **스팸 필터링 무시**를 선택한 후 **확인**을 클릭합니다.
    
7. 원하는 경우에 감사 규칙, 규칙을 테스트, 특정 기간 동안 규칙 활성화를 선택 하 고 다른 선택 항목을 만들 수 있습니다. 적용 하기 전에 기간에 대 한 규칙을 테스트 하는 것이 좋습니다. [메일 흐름에 대 한 절차 규칙은 Exchange 서버](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) 이러한 선택 항목에 대 한 자세한 정보를 포함합니다. 
    
8. 규칙을 저장 하려면 **저장** 을 클릭 합니다. 규칙의 규칙 목록에 나타납니다. 
    
만들 규칙을 적용 하 고 서비스는 지정한 IP 주소 범위에 대해 스팸 필터링을 무시 합니다.
  
### <a name="scoping-an-ip-allow-list-exception-for-a-specific-domain"></a>특정 도메인에 대해 IP 허용 목록 예외 범위 지정

일반적으로 안전한 것으로 간주되는 모든 도메인에 대한 IP 주소(또는 IP 주소 범위)를 IP 허용 목록에 추가하는 것이 좋습니다. 그러나 IP 허용 목록 항목을 모든 도메인에 적용하지는 않으려면 특정 도메인을 제외하는 전송 규칙을 만들면 됩니다. 
  
예를 들어, 세 개의 도메인인 ContosoA.com, ContosoB.com 및 ContosoC.com이 있으며 IP 주소(단순하게 표현하기 위해 1.2.3.4 사용)를 추가하고 도메인 ContosoB.com에 대해서만 필터링을 건너뛰려 한다고 가정합니다. 모든 도메인에 대해 SCL(스팸 지수)을 -1(스팸이 아닌 것으로 분류됨을 의미함)로 설정하는 IP 허용 목록을 1.2.3.4에 대해 만듭니다. 그런 다음 모든 도메인(ContosoB.com 제외)에 대해 SCL을 0으로 설정하는 전송 규칙을 만들 수 있습니다. 그러면 ContosoB.com(규칙에서 예외로 나열되는 도메인)을 제외하고 IP 주소와 연결된 모든 도메인에 대해 메시지가 다시 검색됩니다. ContosoB.com의 SCL은 여전히 -1(필터링 건너뜀을 의미함)인 반면, ContosoA.com 및 ContosoC.com의 SCL은 0(콘텐츠 필터에 의해 다시 검색됨을 의미함)입니다.
  
이렇게 하려면 다음 단계를 수행합니다.
  
1. EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.
    
2. ![아이콘 추가](media/ITPro-EAC-AddIcon.gif)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.
    
3. 규칙 이름을 지정하고 **기타 옵션**을 클릭합니다.
    
4. **다음의 경우 이 규칙 적용**에서 **보낸 사람**을 선택하고 **IP 주소가 이 범위에 속하거나 정확하게 일치함**을 선택합니다.
    
5. **IP 주소 지정** 상자에서 IP 주소 또는 IP 허용 목록에 입력 한 IP 주소 범위 지정, **추가** 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif), **확인**을 클릭 하 고 있습니다.
    
6. **다음 작업 실행**에서 **메시지 속성 수정**을 선택한 후 **SCL(스팸 지수) 설정**을 선택하여 동작을 설정합니다. **SCL 지정** 상자에서 **0**을 선택한 후 **확인**을 클릭합니다.
    
7. **예외 추가**를 클릭하고 **다음의 경우 제외**에서 **보낸 사람**을 선택하고 **도메인**을 선택합니다. 
    
8. **도메인을 지정** 상자에서 **contosob.com**와 같은 스팸 필터링 무시 하려는 도메인을 입력 합니다. **추가** 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) 는 구 목록으로 이동 합니다. 예외 항목으로 추가 도메인을 추가 하 고 마쳤으면 **확인** 을 클릭 하려는 경우이 단계를 반복 합니다. 
    
9. 원하는 경우에 감사 규칙, 규칙을 테스트, 특정 기간 동안 규칙 활성화를 선택 하 고 다른 선택 항목을 만들 수 있습니다. 적용 하기 전에 기간에 대 한 규칙을 테스트 하는 것이 좋습니다. [메일 흐름에 대 한 절차 규칙은 Exchange 서버](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) 이러한 선택 항목에 대 한 자세한 정보를 포함합니다. 
    
10. 규칙을 저장 하려면 **저장** 을 클릭 합니다. 규칙의 규칙 목록에 나타납니다. 
    
규칙을 만들어 적용하고 나면 지정한 IP 주소 또는 IP 주소 범위에 대한 스팸 필터링이 입력한 도메인 예외에 대해서만 무시됩니다.
  
## <a name="new-to-office-365"></a>Office 365의 새로운 기능
<a name="sectionSection3"> </a>

||
|:-----|
|![LinkedIn Learning용 단축 아이콘](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Office 365를 처음 사용하시나요?**         LinkedIn Learning에서 제공하는 **Office 365 admins and IT pros**의 무료 비디오 과정을 확인해보세요. |
   
## <a name="for-more-information"></a>추가 정보
<a name="sectionSection4"> </a>

[수신 허용-보낸사람 및 수신된 거부 목록 Exchange Online](safe-sender-and-blocked-sender-lists-faq.md)
  
[스팸 필터 정책 구성](configure-your-spam-filter-policies.md)
  
[아웃바운드 스팸 정책 구성](configure-the-outbound-spam-policy.md)
  
[메시지가 스팸으로 표시되지 않는지 확인하는 방법](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  

