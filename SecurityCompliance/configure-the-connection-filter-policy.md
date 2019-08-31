---
title: 연결 필터 정책, 허용 목록, 차단 목록 구성
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 8/27/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6ae78c12-7bbe-44fa-ab13-c3768387d0e3
ms.collection:
- M365-security-compliance
description: 사용자가 신뢰 하는 사람이 보낸 전자 메일이 차단 되지 않도록 하려면 연결 필터 정책을 사용 하 여 신뢰할 수 있는 보낸 사람 목록이 라고도 하는 허용 목록을 만든 IP 주소를 만듭니다. 수신 거부 목록도 만들 수 있습니다.
ms.openlocfilehash: 71dd34ea822324936713380e557d2341e1e389c0
ms.sourcegitcommit: 769b506c828c475c713dbb337e115714dcc7f17c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/31/2019
ms.locfileid: "36699263"
---
# <a name="configure-the-connection-filter-policy"></a>연결 필터 정책 구성

누구에게나 대부분 신뢰할 수 있는 친구와 비즈니스 파트너가 있습니다. 그리고 이러한 사용자들로부터 받은 전자 메일이 스팸 메일 폴더로 가거나 스팸 필터를 통해 완전히 차단되는 난처한 경우가 생길 수 있습니다. 사용자가 신뢰 하는 사람이 보낸 전자 메일이 차단 되지 않도록 하려면 연결 필터 정책을 사용 하 여 신뢰할 수 있는 보낸 사람 목록이 라고도 하는 허용 목록을 만든 IP 주소를 만들 수 있습니다. 그리고 앞으로는 전자 메일 메시지를 받지 않을 IP 주소 목록(대개 알려진 스패머의 주소로 구성)인 수신 거부 목록도 만들 수 있습니다.
  
- *[허용 목록](create-safe-sender-lists-in-office-365.md)* 에 대해 생각 하는 경우 연결 필터 정책에 따라 필터에서 허용 하는 *신뢰할 수 있는 계정을* 사용 하는 것이 중요 합니다. 이 작업은 신뢰할 수 없거나 신뢰할 수 없는 우편물을 보다 정확 하 게 필터링 하기 위해 필요 합니다. 연결 필터 정책 허용 목록은 훨씬 더 큰 계정 및 Ip 풀에서 몇 가지 신뢰할 수 있는 Ip로 필터링 하 고 신뢰할 수 있는 메일 사용이 쉬운 액세스를 보장 하는 것입니다.

- 차단 목록을 만드는 연결 필터 정책에는 대신, 필터에서 더 적은 수의 계정 또는 신뢰 되지 않는 계정이 표시 됩니다.

 [전체 조직에 적용되는 추가 스팸 설정은 메시지가 스팸으로 표시되지 않는지 확인하는 방법](https://go.microsoft.com/fwlink/p/?LinkId=534224) 또는 [Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지](https://go.microsoft.com/fwlink/p/?LinkId=534225)를 참조하세요. 사용자가 관리자 수준 제어를 가지고 있고 가양성이나 거짓 부정을 방지하려고 할 때 유용합니다.

> [!TIP]
> [허용 (또는 안전한 보낸 사람) 목록과](create-safe-sender-lists-in-office-365.md) [차단 목록을](create-block-sender-lists-in-office-365.md)만드는 방법을 일시 중지 하 고 확인할 수 있습니다.
  
다음 비디오에서는 연결 필터 정책의 구성 단계를 보여 줍니다.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/b2f5bea3-e1a7-44b3-b7e2-07fac0d0ca40?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용

- 예상 완료 시간: 15분

- 이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인 하려면 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 항목에서 "스팸 방지" 항목을 참조 하세요.

- 해당 메시지를 허용하거나 차단할 보낸 사람의 IP 주소를 가져오려면 메시지의 인터넷 머리글을 확인합니다. [스팸 방지 메시지 헤더](anti-spam-message-headers.md)에 설명된 대로 CIP 머리글을 찾습니다. 다양 한 전자 메일 클라이언트에서 메시지 헤더를 보는 방법에 대 한 자세한 내용은 [메시지 헤더 분석기](https://go.microsoft.com/fwlink/p/?LinkId=306583)를 참조 하십시오.

- IP 차단 목록의 IP 주소에서 보낸 전자 메일 메시지는 거부 되며 스팸으로 표시 되지 않으며 추가 필터링이 수행 되지 않습니다.

- 또한 원격 PowerShell을 통해 다음 연결 필터 절차를 수행할 수 있습니다. [Get-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) cmdlet을 사용하여 설정을 검토하고 [Set-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) cmdlet을 사용하여 연결 필터 정책 설정을 편집할 수 있습니다. Windows PowerShell을 사용 하 여 Exchange Online Protection에 연결 하는 방법에 대 한 자세한 내용은 [connect To Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290)을 참조 하십시오. Windows PowerShell을 사용하여 Exchange Online에 연결하는 방법에 대한 자세한 내용은 [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.

## <a name="use-the-eac-to-edit-the-default-connection-filter-policy"></a>EAC를 사용하여 기본 연결 필터 정책 편집

EAC(Exchange 관리 센터)에서 연결 필터 정책을 편집하여 IP 허용 목록 또는 IP 차단 목록을 만듭니다. 연결 필터 정책 설정은 인바운드 메시지에만 적용됩니다.
  
1. EAC(Exchange 관리 센터)에서 **보호** \> **연결 필터**로 이동한 후 기본 정책을 두 번 클릭합니다.

2. **연결 필터링** 메뉴 항목을 클릭한 후 원하는 목록을 만듭니다. IP 허용 목록이나 IP 차단 목록 중 하나를 만들거나 두 목록을 모두 만들 수 있습니다.

   이 목록을 만들려면 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif)를 클릭합니다. 이후 표시되는 대화 상자에서 IP 주소나 주소 범위를 지정한 후 **확인**을 클릭합니다. 주소를 추가하려면 이 프로세스를 반복합니다. 주소를 추가한 후 IP 주소를 편집하거나 제거할 수도 있습니다.

   Nnn은 0에서 255 사이의 숫자로 IPV4 IP 주소를 지정 합니다. nnn 또한 a r t. nnn/rr 형식으로 클래스 간 라우팅 (CIDR) 범위를 지정할 수 있습니다 (여기서 rr은 24에서 32 사이의 숫자). 24 ~ 32 범위를 벗어나는 범위를 지정 하려면 다음 섹션인 [IP 허용 목록 구성 시 추가 고려 사항을](#additional-considerations-when-configuring-ip-allow-lists)참조 하십시오.

   > [!NOTE]
   > 두 목록에 IP 주소를 추가 하는 경우 해당 IP 주소에서 보낸 전자 메일을 사용할 수 있습니다. <br/><br/> 최대 1273 개의 항목을 지정할 수 있는데,이 항목은 단일 IP 주소 이거나 IP 주소의 CIDR 범위/24 ~/32입니다. <br/><br/> TLS 암호화 메시지를 보내는 경우 IPv6 주소 및 주소 범위는 지원 되지 않습니다.
  
3. 원하는 경우 수신 허용 **목록 사용** 확인란을 선택 하 여 잘 알려진 특정 보낸 사람의 전자 메일이 손실 되지 않도록 합니다. 미치는? Microsoft는 신뢰할 수 있는 보낸 사람에 대 한 타사 소스를 구독 합니다. 이 수신 허용 목록을 사용 하는 것은 해당 신뢰할 수 있는 보낸 사람이 실수로 스팸으로 표시 되지 않았음을 의미 합니다. 이 옵션을 선택 하는 것이 좋습니다 (스팸으로 분류 되는 가짜 메일) 수를 줄여야 하기 때문입니다. 

4. **저장**을 클릭합니다. 기본 정책 설정에 대한 요약이 오른쪽 창에 표시됩니다.

## <a name="additional-considerations-when-configuring-ip-allow-lists"></a>IP 허용 목록 구성 시 추가 고려 사항

다음은 IP 허용 목록 구성 시 고려해야 하거나 알고 있어야 하는 추가 고려 사항입니다.
  
### <a name="specifying-a-cidr-range-that-falls-outside-of-the-recommended-range"></a>권장되는 범위를 벗어나는 CIDR 범위 지정

/1에서/23 까지의 CIDR IP 주소 범위를 지정 하려면 SCL (스팸 지 수)이이 IP 주소 범위 내에서 수신 되는 모든 메시지를 **무시** 하도록 설정 하는 ip 주소 범위에서 작동 하는 메일 흐름 규칙을 만들어야 합니다. "스팸 아님"으로 설정 되 고 서비스에서 추가 필터링을 수행 하지 않습니다. 하지만 Microsoft 전용 차단 목록이나 타사의 차단 목록에 이러한 IP 주소가 표시된 경우 이러한 메시지는 계속해서 차단됩니다. 따라서/24 ~/32 IP 주소 범위를 사용 하는 것이 좋습니다.
  
이 메일 흐름 규칙을 만들려면 다음 단계를 수행 합니다.
  
1. EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.

2. ![아이콘 추가](media/ITPro-EAC-AddIcon.gif)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.

3. 규칙 이름을 지정하고 **기타 옵션**을 클릭합니다.

4. **다음의 경우 이 규칙 적용**에서 **보낸 사람**을 선택하고 **IP 주소가 이 범위에 속하거나 정확하게 일치함**을 선택합니다.

5. **Ip 주소 지정**에서 ip 주소 범위를 지정 하 고 추가 아이콘 **** ![](media/ITPro-EAC-AddIcon.gif)추가를 클릭 한 다음 **확인**을 클릭 합니다.

6. **다음 작업 수행** 상자에서 **메시지 속성 수정**을 선택한 다음 **SCL(스팸 지수) 설정**을 선택하여 동작을 설정합니다. **SCL 지정** 상자에서 **스팸 필터링 무시**를 선택한 후 **확인**을 클릭합니다.

7. 원하는 경우 규칙을 감사하고 규칙을 테스트하며 특정 기간 동안 규칙을 활성화하는 등 기타 옵션을 지정할 수 있습니다. 옵션을 적용하기 전에 규칙을 테스트하는 것이 좋습니다. [Exchange Server의 메일 흐름 규칙에 대 한 절차에는](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) 이러한 선택 항목에 대 한 자세한 정보가 포함 되어 있습니다.

8. **저장** 을 클릭 하 여 규칙을 저장 합니다. 규칙이 규칙 목록에 표시 됩니다.

규칙을 만들고 적용 한 후에는 서비스에서 지정한 IP 주소 범위에 대 한 스팸 필터링을 무시 합니다.

### <a name="scoping-an-ip-allow-list-exception-for-a-specific-domain"></a>특정 도메인에 대해 IP 허용 목록 예외 범위 지정

일반적으로 안전한 것으로 간주되는 모든 도메인에 대한 IP 주소(또는 IP 주소 범위)를 IP 허용 목록에 추가하는 것이 좋습니다. 그러나 IP 허용 목록 항목을 모든 도메인에 적용 하지 않으려면 특정 도메인을 제외 하는 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들 수 있습니다.
  
예를 들어, 세 개의 도메인인 ContosoA.com, ContosoB.com 및 ContosoC.com이 있으며 IP 주소(단순하게 표현하기 위해 1.2.3.4 사용)를 추가하고 도메인 ContosoB.com에 대해서만 필터링을 건너뛰려 한다고 가정합니다. 모든 도메인에 대해 SCL(스팸 지수)을 -1(스팸이 아닌 것으로 분류됨을 의미함)로 설정하는 IP 허용 목록을 1.2.3.4에 대해 만듭니다. 그런 다음 ContosoB.com를 제외한 모든 도메인에 대해 SCL을 설정 하는 메일 흐름 규칙을 만들 수 있습니다. 그러면 ContosoB.com(규칙에서 예외로 나열되는 도메인)을 제외하고 IP 주소와 연결된 모든 도메인에 대해 메시지가 다시 검색됩니다. ContosoB.com의 SCL은 여전히 -1(필터링 건너뜀을 의미함)인 반면, ContosoA.com 및 ContosoC.com의 SCL은 0(콘텐츠 필터에 의해 다시 검색됨을 의미함)입니다.
  
이렇게 하려면 다음 단계를 수행합니다.
  
1. EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.

2. ![아이콘 추가](media/ITPro-EAC-AddIcon.gif)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.

3. 규칙 이름을 지정하고 **기타 옵션**을 클릭합니다.

4. **다음의 경우 이 규칙 적용**에서 **보낸 사람**을 선택하고 **IP 주소가 이 범위에 속하거나 정확하게 일치함**을 선택합니다.

5. **Ip 주소 지정** 상자에서 ip 허용 목록에 입력 한 ip 주소 또는 ip 주소 범위를 지정 하 고 추가 아이콘](media/ITPro-EAC-AddIcon.gif) **추가** ![를 클릭 한 다음 **확인**을 클릭 합니다.

6. **다음 작업 실행**에서 **메시지 속성 수정을** 선택한 다음 **SCL (스팸 지 수) 설정을**선택 하 여 작업을 설정 합니다. **SCL 지정** 상자에서 **0**을 선택 하 고 **확인**을 클릭 합니다.

7. **예외 추가**를 클릭 하 고 다음의 **경우 제외**에서 **보낸 사람** 을 선택 하 고 **도메인을**선택 합니다.

8. **도메인 지정** 상자에 **contosob.com**과 같은 스팸 필터링을 무시할 도메인을 입력 합니다. 추가 아이콘](media/ITPro-EAC-AddIcon.gif) 추가를 클릭 하 여 구 목록으로 이동 합니다. **** ![ 도메인을 예외로 더 추가하려면 이 단계를 반복하고 완료되면 **확인**을 클릭합니다. 

9. 원하는 경우 규칙을 감사하고 규칙을 테스트하며 특정 기간 동안 규칙을 활성화하는 등 기타 옵션을 지정할 수 있습니다. 옵션을 적용하기 전에 규칙을 테스트하는 것이 좋습니다. [Exchange Server의 메일 흐름 규칙에 대 한 절차에는](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) 이러한 선택 항목에 대 한 자세한 정보가 포함 되어 있습니다.

10. **저장** 을 클릭 하 여 규칙을 저장 합니다. 규칙이 규칙 목록에 표시 됩니다.

규칙을 만들어 적용하고 나면 지정한 IP 주소 또는 IP 주소 범위에 대한 스팸 필터링이 입력한 도메인 예외에 대해서만 무시됩니다.

### <a name="scenarios-where-allowed-ip-addresses-are-still-filtered"></a>허용 된 IP 주소가 계속 필터링 되는 시나리오

연결 필터 정책에서 구성한 허용 IP 주소에서 보낸 메시지는 여전히 다음과 같은 경우에 스팸 필터링이 적용 됩니다.

- 연결 필터 정책의 원본 IP 주소도 *모든* 테 넌 트의 온-프레미스, ip 기반 인바운드 커넥터 (이 테 넌 트 a 호출), 테 넌 트 a 및 Exchange Online **** Protection 서버에서 구성 됩니다. Office 365의 메시지가 Microsoft 데이터 센터의 동일한 Active Directory 포리스트에 있어야 합니다. 이 시나리오에서는 **IPV: CAL** 이 메시지의 [스팸 방지 메시지 헤더](anti-spam-message-headers.md) (스팸 필터링 바이패스 메시지를 나타냄)에 추가 되지만 메시지에 여전히 스팸 필터링이 적용 됩니다.

- 테 넌 트 (연결 필터 정책을 구성한 위치) 및 Exchange Online Protection 서버가 Office 365에서 메시지를 처음으로 실행 하는 경우 두 가지 모두 Microsoft 데이터 센터의 서로 다른 Active Directory 포리스트에 있어야 합니다. 이 시나리오에서는 **IPV: CAL** 이 메시지 헤더에 추가 되지 않으므로 메시지에 여전히 스팸 필터링이 적용 됩니다.

이러한 시나리오 중 하나가 발생 하면 다음 설정에 따라 EAC에서 메일 흐름 규칙을 만들어 IP 주소 또는 주소에서 보낸 메시지가 스팸 필터링을 우회 하도록 할 수 있습니다.

- 규칙 조건: \> **보낸 사람** \> **ip 주소가 이러한 범위에 있거나 정확히 일치** \> 하는 경우 (IP 주소 또는 주소) **이 규칙을 적용** 합니다.

- 규칙 동작: **메시지 속성** \> 수정 **SCL (스팸** \> 지 수) 사용 **안 함 스팸 필터링**을 설정 합니다.

이 절차는 기본적으로 [특정 도메인의 IP 허용 목록 예외 범위에서 이전 범위가 지정](#scoping-an-ip-allow-list-exception-for-a-specific-domain) 된 규칙 만들기 프로시저와 동일 합니다.

## <a name="new-to-office-365"></a>Office 365의 새로운 기능

||
|:-----|
|![LinkedIn Learning용 단축 아이콘](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Office 365를 처음 사용하시나요?** LinkedIn Learning에서 제공하는 **Office 365 admins and IT pros**의 무료 비디오 과정을 확인해보세요.|

## <a name="for-more-information"></a>자세한 내용

[Exchange Online의 수신 허용-보낸 사람 및 수신 거부 목록](safe-sender-and-blocked-sender-lists-faq.md)
  
[스팸 필터 정책 구성](configure-your-spam-filter-policies.md)
  
[아웃바운드 스팸 정책 구성](configure-the-outbound-spam-policy.md)
  
[메시지가 스팸으로 표시되지 않는지 확인하는 방법](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지](https://go.microsoft.com/fwlink/p/?LinkId=534225)
