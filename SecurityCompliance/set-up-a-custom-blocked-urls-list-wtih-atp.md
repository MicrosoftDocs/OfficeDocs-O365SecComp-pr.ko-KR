---
title: Office 365 ATP 안전 링크를 사용 하 여 차단 된 Url 목록 사용자 지정 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 12/11/2018
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: Office 365 고급 위협 보호를 사용 하 여 조직에 대 한 차단 된 Url의 목록을 설정 하는 방법에 알아봅니다. 차단 된 Url ATP 안전한 링크 정책에 따라 Office 문서 및 전자 메일 메시지에 적용 됩니다.
ms.openlocfilehash: 25f01b767726ebf02d5da5d18444fa0428f144ac
ms.sourcegitcommit: 031781d0eecf33baabcd03ea53546d41076062b4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/12/2018
ms.locfileid: "27240531"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a>Office 365 ATP 안전 링크를 사용 하 여 차단 된 Url 목록 사용자 지정 설정

[Office 365 고급 위협 보호](office-365-atp.md) ATP (), 조직 웹사이트 주소 (Url) 차단 되는 사용자 지정 목록을 할 수 있습니다. URL을 차단 되 면 차단 된 URL에 대 한 링크를 클릭 하는 사람 된 다음 이미지 유사한 [경고 페이지](atp-safe-links-warning-pages.md) 로 이동 합니다. 
  
![이 사이트는 차단](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
차단 된 Url 목록 조직의 Office 365 보안 팀에 의해 정의 된 하 고 해당 목록은 Office 365 ATP 안전한 링크 정책에 포함 되는 사용자 조직에서 모든 사용자에 게 적용 됩니다. 
  
[Office 365의 ATP 안전 링크](atp-safe-links.md)에 대 한 조직의 사용자 지정 차단된 Url 목록을 설정 하는 방법은이 문서를 읽어보십시오.
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a>차단 된 Url의 사용자 지정 목록을 편집 또는 보기

[Office 365의 ATP 안전한 링크](atp-safe-links.md) 여러 목록, 조직의 사용자 지정 차단된 Url 목록 포함을 사용 합니다. 필요한 사용 권한이 하는 경우에 조직의 사용자 지정 목록을 설정할 수 있습니다. 조직의 기본 안전한 링크 정책을 편집 하 여이 작업을 수행 합니다.
  
1. 이동 [https://security.microsoft.com](https://security.microsoft.com) 와 작업이 나 교육용 계정 사용 하 여 로그인 합니다. 
    
2. 왼쪽 탐색 영역 **위협 관리**, **정책** 선택 \> **안전 링크**입니다.
    
3. **조직 전체에 적용 되는 정책** 섹션에서 **기본**을 선택 하 고 **편집** (편집 단추는 연필 유사)를 선택 합니다.<br/>![안전한 링크 보호에 대 한 기본 정책을 편집 하려면 편집을 클릭 합니다.](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)<br/>이 옵션을 사용 하면 차단 된 Url의 목록을 볼 수 있습니다. 처음에 어떤 Url도 여기에 나열 된 없을 수도 있습니다.<br/>![차단 되는 기본 안전한 링크 정책에서 Url 목록](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)
  
4. 선택 **유효한 URL 입력** 상자에 URL을 입력 하 고 더하기 기호를 선택 합니다 (**+**). 

5. 화면 오른쪽 아래 모서리에서 Url을 추가 (영문)이 끝나면 **저장**을 선택 합니다.
    
## <a name="a-few-things-to-keep-in-mind"></a>주의 해야할 사항

대화 목록에 Url을 추가 하는 동안 다음과 같은 사항을 사항에 유의 해야 합니다. 

- 슬래시를 포함 하지 마십시오 ( **/**) URL의 끝에 있습니다. 입력 하는 대신 등 `http://www.contoso.com/`, 입력 `http://www.contoso.com`합니다.
    
- 한 도메인에만 나타나는 URL을 지정할 수 있습니다 (같은 `contoso.com` 또는 `tailspintoys.com`). 이것은 클릭 차단 도메인을 포함 하는 모든 URL에 있습니다.

- 하위 도메인을 지정할 수 있습니다 (같은 `toys.contoso.com*`) 전체 도메인을 차단 하지 않고 (같은 `contoso.com`). 이는 블록의 하위 도메인이 포함 하는 모든 URL 하지만 클릭을 차단 되지 않습니다 전체 도메인을 포함 하는 url입니다.  
    
- 세 개까지 와일드 카드 별표를 포함할 수 있습니다 (\*) URL 당 합니다. 입력할 수 및 이러한 항목이 어떤 영향에 대 한 예가 다음 표에 나와 있습니다.
    
|**예제 항목**|**기능**|
|:-----|:-----|
|`contoso.com`또는`*contoso.com*`  <br/> |도메인, 하위 도메인, 및 경로 같은 차단 `https://www.contoso.com`, `http://sub.contoso.com`, 및`http://contoso.com/abc`  <br/> |
|`http://contoso.com/a`  <br/> |사이트를 차단 `http://contoso.com/a` 이지만 하지 추가 하위 경로`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a*`  <br/> |사이트를 차단 `http://contoso.com/a` 추가 하위 경로 같은 및`http://contoso.com/a/b`  <br/> |
|`http://toys.contoso.com*`  <br/> |하위 도메인 (이 경우 "상사")를 차단 하지만 다른 도메인 Url 클릭을 허용 (같은 `http://contoso.com` 또는 `http://home.contoso.com`).  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a>조직에서 특정 사용자에 대 한 예외를 정의 하는 방법

다른 사용자에 대 한 차단 되었을 수 있는 Url을 볼 수 있도록 특정 그룹을 하려는 경우에 특정 받는 사람에 게 적용 되는 ATP 안전한 링크 정책을 지정할 수 있습니다. [ATP 안전 링크를 사용 하는 사용자 지정 "rewrite 수행" Url 목록 설정](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)을 참조 하십시오.
  

