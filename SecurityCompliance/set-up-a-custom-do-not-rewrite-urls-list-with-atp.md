---
title: Office 365 ATP 안전 링크를 사용 하 여 사용자 지정 안함-되지 않음-재작성 Url 목록 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
description: ATP 안전한 링크 정책에를 설정 하는 경우에 do not 재작성을 포함할 수 있습니다 ' 목록에 포함 된 사이트를 방문 하 여 조직에서 일부 사용자를 사용 하도록 설정 하는 Url의 목록입니다.
ms.openlocfilehash: 0ee9c87c90e6e30d6c43fb0de5291dd85b03be07
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782165"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a>Office 365 ATP 안전 링크를 사용 하 여 사용자 지정 안함-되지 않음-재작성 Url 목록 설정

[Office 365 고급 위협 보호](office-365-atp.md) ATP ()와 함께 조직을 가질 수 [차단 된 사용자 지정 Url](set-up-a-custom-blocked-urls-list-wtih-atp.md)을 웹에 사람들을 클릭 하는 경우 주소 (Url)는 전자 메일 메시지 또는 특정 Office 문서에는 이러한 Url 하려고에서 수 없습니다. 조직에서 특정 그룹에 대 한 사용자 지정 "rewrite 수행" 목록을 역시 조직입니다. "Rewrite 수행" 목록에는 그렇지 않은 경우 [Office 365의 ATP 안전 링크](atp-safe-links.md)에 의해 차단 되는 Url을 방문 하 여 일부 참가자 수 있습니다. 
  
이 문서에서는 ATP 안전 링크를 검색 하 고 몇가지 중요 한 사항을 염두에에서 제외 되는 Url의 목록을 지정 하는 방법에 설명 합니다.

## <a name="set-up-a-do-not-rewrite-list"></a>"Rewrite 수행" 목록 설정

ATP 안전한 링크 보호 조직의 차단된 Url 목록 및 예외에 대 한 "rewrite 수행" 목록을 포함 하 여 여러 목록을 사용 합니다. 필요한 사용 권한이 하는 경우에 "rewrite 수행" 사용자 지정 목록을 설정할 수 있습니다. 이렇게 하려면 추가 하거나 조직에서 특정 받는 사람에 게 적용 되는 안전한 링크 정책을 편집 합니다. 
  
1. 이동 [https://protection.office.com](https://protection.office.com) 와 작업이 나 교육용 계정 사용 하 여 로그인 합니다. 
    
2. 왼쪽 탐색 영역 **위협 관리** \> **정책** \> **안전 링크**입니다.
    
3. **특정 받는 사람에 게 적용 되는 정책** 섹션에서 **새로 만들기** 를 선택 (새로 만들기 단추 유사한 더하기 기호 ( **+**)) 새 정책을 만들 수 있습니다. (또는 편집할 수 있습니다 기존 정책을.)
    
    ![특정 전자 메일 받는 사람에 대 한 안전한 링크 정책을 추가 하려면 새로 만들기를 선택 합니다.](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
4. 이름 및 사용자 정책에 대 한 설명을 지정 합니다.
    
5. **다음 Url 다시 작성 하지 않는** 섹션에서 **유효한 URL 입력** 상자를 선택 하 고 URL을 입력 하 고 더하기 기호 (+)를 선택 합니다. 
    
6. **적용 된** 섹션에서 **받는 사람이의 구성원은**을 선택 하 고 정책에 포함 하려는 그룹을 선택 합니다. **추가**선택 하 고 **확인**을 선택 합니다.
    
7. 화면 오른쪽 아래 모서리에서 Url을 추가 (영문)이 끝나면 **저장**을 선택 합니다.
    
> [!NOTE]
> 차단 된 Url의 경우 조직의 사용자 지정 목록을 검토 했는지 확인 합니다. [ATP 안전 링크를 사용 하 여 차단 된 Url 목록 사용자 지정 설정](set-up-a-custom-blocked-urls-list-wtih-atp.md)을 참조 하십시오. 
  
## <a name="important-points-to-keep-in-mind"></a>중요 한 사항을 염두에

- "Rewrite 수행" 목록에서 지정 하는 모든 Url ATP 안전 링크를 지정 하는 받는 사람에 대 한 검사에서 제외 됩니다.
 
- ATP 안전한 링크 정책에 대 한 "rewrite 수행" 목록을 지정 하면 세 개까지 와일드 카드 별표를 포함할 수 있습니다 (\*). 와일드 카드 (\*)와 같은 항목에 대 한 가정 `contoso.com`는 포함 하지 않으면 명시적으로 접두사 또는 하위 도메인과 같은 `http://` 또는 `https://`합니다. 이 항목을는 같은 의미 `contoso.com` 하는 것과 비슷합니다 `\*contoso.com\*` 대화 "rewrite 수행" 목록에 대 한 합니다.

- "Rewrite 수행" 목록에 이미 Url의 목록을 하는 경우에 해당 그룹을 검토 하 고 적절 하 게 와일드 카드를 추가 하려면 해야 합니다. 예, 기존 목록에 있는 경우 항목 같은 `http://contoso.com/a` 와 같은 하위 경로 포함 하려는 `http://contoso.com/a/b` 정책에 따라 추가 와일드 카드를 입력 한 항목을 같이 되도록 `http://contoso.com/a\*`합니다.
    
- "Rewrite 수행" 목록에 지정 하는 Url에 슬래시 (/)를 포함 하지 마십시오. 예를 입력 하지 않고 `contoso.com/` 대화 "rewrite 수행" 목록에 입력 `contoso.com`합니다.
    
다음 표에서 목록 예제 입력할 수 및 이러한 항목이 어떤 영향 수 있으며
    
|**예제 항목**|**기능**|
|:-----|:-----|
|`\*contoso.com\*`  <br/> |같은 도메인, 하위 도메인, 및 경로 방문 하 여 특정 수신자에 게 허용 `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, 또는`http://www.contoso.com/a`  <br/> |
|`http://contoso.com/a`  <br/> |같은 사이트를 방문 하 여 특정 수신자에 게 허용 `http://contoso.com/a`, 하위 경로 하지 않지만`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a\*`  <br/> |같은 사이트를 방문 하 여 특정 수신자에 게 허용 `http://contoso.com/a` 하위 경로 같은 및`http://contoso.com/a/b`  <br/> |
   
  

## <a name="related-topics"></a>관련 항목

[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Office 365의에서 ATP 안전 하 게 보호 링크](atp-safe-links.md)
  
[Office 365의 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)
  
[ATP 안전 링크를 사용 하 여 차단 된 Url 목록 사용자 지정 설정](set-up-a-custom-blocked-urls-list-wtih-atp.md)

[Office 365 고급 위협 보호에 대 한 보고서 보기](view-reports-for-atp.md)

[Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)
  

