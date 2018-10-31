---
title: 제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/9/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
description: 0-시간 자동 삭제 (ZAP) 스팸 또는 맬웨어로와 사용자의 받은 편지함에 이미 배달 된 메시지를 검색 하는 전자 메일 보호 기능 및 다음 치명적이 지 악의적인 콘텐츠를 렌더링 합니다. 어떻게 ZAP이 작업을 수행 하는 작업은 감지 악의적인 콘텐츠 형식에 따라 다릅니다.
ms.openlocfilehash: dabe4caf8916d3f0de7a70cb3d056dd9a7fdcc3f
ms.sourcegitcommit: ceb70ea863d8b97afea077a04fc7ec612b870695
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25857246"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a>제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호

0-시간 자동 삭제 (ZAP) 스팸 또는 맬웨어로와 사용자의 받은 편지함에 이미 배달 된 메시지를 검색 하는 전자 메일 보호 기능 및 다음 치명적이 지 악의적인 콘텐츠를 렌더링 합니다. 어떻게 ZAP이 작업을 수행 하는 작업은 감지 악의적인 콘텐츠 형식에 따라 다릅니다.
  
ZAP은 Exchange Online 사서함이 포함 된 모든 Office 365 구독의 함께 제공 되는 Exchange Online Protection 기본 제공 됩니다.
  
## <a name="how-does-zap-work"></a>ZAP는 어떻게 작동 합니까?

Office 365에서 스팸 방지 엔진 및 맬웨어 서명 업데이트를 매일 실시간 합니다. 그러나 사용자에 게 다양 한 콘텐츠를 사용자에 게 처음 제공 된 후에 한번에 weaponized 다음을 수행할 때의 이유로 대 한 받은 편지함에 배달 된 악의적인 메시지를 계속 가져올 수 있습니다. Office 365 스팸 및 맬웨어로부터 서명을 업데이트 하는 계속 해 서를 모니터링 하 여이 주소 ZAP 하 고 따라서 찾아 수 받은 편지함에 이미 이전에 배달 된 메시지를 제거 합니다. 이미 스팸으로 식별 된 메일에 대 한 ZAP 읽지 않은 메시지를 사용자의 정크 메일 폴더로 이동 합니다. 새로 검색 된 맬웨어 ZAP 메일을 읽은 여부에 관계 없이 전자 메일 메시지에서 첨부 파일을 제거 합니다. 반대로 악성 소프트웨어로 하지 분류 잘못 된 메시지에 대 한 마찬가지입니다.
  
사서함 사용자, 자신이 통보 되지 않습니다 메일 옮긴 ZAP 함수는 원활 하 게 수행 해야 합니다.
  
목록, [메일 흐름 규칙](https://go.microsoft.com/fwlink/p/?LinkId=722755)및 최종 사용자 규칙을 허용 또는 추가 필터를 ZAP 보다 우선 합니다.
  
 **이 문서의 내용**
  
> [스팸 필터 정책 설정](zero-hour-auto-purge.md#BK_SetSpam)
    
> [ZAP 메시지를 이동 하는 경우를 참조 하십시오.](zero-hour-auto-purge.md#BK_DidZAPMove)
    
> [ZAP를 사용 하지 않도록 설정](zero-hour-auto-purge.md#BK_Posh)
    
> [FAQ](zero-hour-auto-purge.md#BK_FAQ)
    
## <a name="working-with-zap"></a>ZAP (영문)

기본적으로 ZAP 켜져 있지만 조건 관련 된 몇가지를 충족 하는지 확인 해야 합니다.
  
- 스팸 필터 정책은 [정크 메일 폴더로 메시지 이동](zero-hour-auto-purge.md#BK_SetSpam)으로 설정 됩니다.
    
    모든 사서함 ZAP으로 검사 하지 않으려면 사용자 집합에만 적용 되는 스팸 필터 정책을 새로 만들 수도 있습니다.
    
- 사용자의 [옵션 \> 정크 메일](https://support.office.com/article/068FA430-F8D7-4518-A8DA-8BC74958F05F)합니다.
    
[ZAP 메시지를 이동 하는 경우 확인](zero-hour-auto-purge.md#BK_DidZAPMove)하려는 경우에 Exchange Online 메시지 추적 도구를 사용할 수 있습니다.
  
관리자가 수도 [ZAP를 사용 하지 않도록 설정](zero-hour-auto-purge.md#BK_Posh) PowerShell을 사용 하 여. 
  
 **스팸 필터 정책을 설정 하려면**
  
1. [비즈니스를 위한 Office 365에 로그인 할 위치](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) 에 로그인 하 고 **보호** 선택 \> **스팸 필터**입니다. 
    
    ![EAC에서 보호를 선택 하 고 필터를 스팸](media/0463c879-63fa-4a6c-9b03-e980d5ef3954.PNG)
  
2. 조정 하려는 필터 정책을 선택 하거나 **추가**선택![추가 아이콘](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) 새 수신기를 만듭니다. 
    
    이전 스크린샷에서 정책 이름이 "기본" 있지만 추가 스팸 필터 정책을 만들 경우 있습니다 수에 다른 이름을 지정 합니다. 또한 제한 된 집합의 사용자에 정책을 적용할 수 있습니다.
    
3. 정책 창에서 **스팸 및 대량 작업**선택 하 고 **스팸** 이 **정크 메일 폴더로 메시지 이동으로**설정 되었는지 확인 합니다. 
    
    이 시점에서 **저장** 을 선택 하는 경우 Office 365 테 넌 트에 정책을 적용 합니다. 
    
    ![정크 메일 폴더로 메시지 이동 하기 위한 설정 스팸 및 대량 작업](media/4332cfb3-89e1-48ba-8da8-9286f2fa1089.PNG)
  
4. **받는 사람**, **도메인**또는 **그룹 구성원 자격** 메뉴 컨트롤 및 정책 필터 창에서 **적용** 섹션으로 스크롤한 선택 새 정책을 만든 경우 사용자의 하위 집합만에 정책을 적용 하려는 경우 정책에 적용 하려고 합니다. 추가 조건 및 예외를 설정할 수도 있습니다. 
    
    ![적용 된 주소 섹션에서 받는 사람을 선택](media/19ca10db-c0f4-432c-b3de-ad4101a23de6.PNG)
  
    선택한 사용자에 게 정책을 적용 하려면 **저장** 을 선택 합니다. 
    
 **ZAP 메시지를 이동 하는 경우를 확인 하려면**
  
- 메시지 ZAP 여 이동 된 경우 확인 하는 [찾기 및 비즈니스 관리자에 대 한 Office 365의 전자 메일 배달 문제를 해결](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) 을 사용할 수 있습니다. 
    
    ZAP 여 이동 된 메시지를 식별 하 여 추적 세부 정보에 "0 시간 자동 항목 지우기 (ZAP)" 텍스트를 찾습니다.
    
 **ZAP를 사용 하지 않도록 설정 하려면**
  
- 사용 하지 않도록 설정 하려는 경우 Office 365 테 넌 트에 대 한 ZAP 또는 사용자 집합을 [Set-hostedcontentfilterpolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), EOP cmdlet의 **ZapEnabled** 매개 변수를 사용 합니다.
    
    다음 예제에서는 ZAP은 "Test" 라는 콘텐츠 필터 정책에 대해 사용할 수 없습니다.
    
||
|:-----|
|
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

|
   
## <a name="faq"></a>FAQ
<a name="BK_FAQ"> </a>

 **합법적인 메시지는 정크 메일 폴더로 이동 하는 경우 어떻게 됩니까?**
  
False 양수에 대 한 일반 보고 프로세스를 따라야 합니다. 정크 메일 폴더로 메시지를 받은 편지함에서 이동할 수는 유일한 이유는 서비스에서 메시지 스팸 했음을 확인가 때문에 것 또는 악의적 합니다.
  
 **경우에 어떻게 정크 메일 폴더 대신 Office 365 격리를 사용 합니까?**
  
ZAP 지금은 메시지를 격리에 받은 편지함에서 이동 하지 않습니다.
  
 **사용자 지정 메일 흐름 규칙을 경우에 어떻게 해야 합니까 (차단 / 허용 규칙)?**
  
관리자 (메일 흐름 규칙) 또는 허용 및 차단 규칙에서 만든 규칙이 우선 합니다. 이러한 메시지 기능 조건에서 제외 됩니다.
  
## <a name="related-topics"></a>관련 항목
<a name="BK_FAQ"> </a>

[Office 365 전자 메일 스팸 방지 보호](anti-spam-protection.md)
  
[Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지](block-email-spam-to-prevent-false-negatives.md)
  

