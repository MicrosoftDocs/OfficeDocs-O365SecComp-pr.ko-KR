---
title: Office 365 ATP 안전한 링크를 사용 하 여 사용자 지정 하 여 재작성 되지 않는 url 목록 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
ms.collection:
- M365-security-compliance
description: ATP 안전한 링크 정책을 설정 하는 경우 조직의 일부 사용자가 목록에 포함 된 사이트를 방문할 수 있도록 하기 위해 다음 url 목록을 포함 하 여이를 재작성 합니다.
ms.openlocfilehash: 006dab44054f9cb707bb13d158588ab6606fab5c
ms.sourcegitcommit: 1c73c2f83703af0a30a5b0633db00d8e0e6b39b5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/25/2019
ms.locfileid: "30241980"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a>Office 365 ATP 안전한 링크를 사용 하 여 사용자 지정 하 여 재작성 되지 않는 url 목록 설정

> [!IMPORTANT]
> 이 문서는 비즈니스 고객을 위한 것입니다. Outlook의 안전한 링크에 대 한 정보를 검색 하는 개인 사용자는 [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2)를 참조 하십시오.

[Office 365 ATP (Advanced Threat Protection](office-365-atp.md) )를 사용 하는 경우 조직에 [사용자 지정 차단 된 url](set-up-a-custom-blocked-urls-list-wtih-atp.md)이 있을 수 있으며, 사용자가 전자 메일 메시지 또는 특정 Office 문서에서 웹 주소 (url)를 클릭할 때 이러한 url로 이동 하는 것이 방지 됩니다. 조직에서 조직의 특정 그룹에 대해 사용자 지정 "다시 쓰지 않음" 목록을 사용할 수도 있습니다. "다시 쓰지 않음" 목록을 사용 하면 일부 사용자가 [Office 365의 ATP 안전한 링크](atp-safe-links.md)에 의해 차단 되는 url을 방문할 수 있습니다. 
  
이 문서에서는 ATP 안전한 링크 검색에서 제외 되는 url 목록과 몇 가지 중요 한 사항을 염두에 두고 있는지를 지정 하는 방법에 대해 설명 합니다.

## <a name="set-up-a-do-not-rewrite-list"></a>"다시 쓰지 않음" 목록 설정

ATP 안전한 링크 보호에서는 조직의 차단 된 url 목록과 "다시 쓰지 않음" 목록 등 여러 목록을 사용 합니다. 필요한 사용 권한이 있는 경우 사용자 지정 "다시 쓰지 않음" 목록을 설정할 수 있습니다. 조직의 특정 받는 사람에 게 적용 되는 안전 링크 정책을 추가 하거나 편집할 때이 작업을 수행 합니다. 

ATP 정책을 편집 하거나 정의 하려면 다음 표에 설명 된 역할 중 하나를 할당 받아야 합니다.

|역할  |할당 된 위치/방법  |
|---------|---------|
|Office 365 전역 관리자 |Office 365을 구매 하기 위해 등록 하는 사람은 기본적으로 전역 관리자입니다. 자세한 내용은 [Office 365 관리자 역할 정보](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 를 참조 하세요.         |
|보안 관리자 |Azure Active Directory 관리 센터 ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Exchange Online 조직 관리 |Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>또는 <br>  PowerShell cmdlet ( [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조) |

> [!TIP]
> 역할 및 사용 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.

### <a name="to-view-or-edit-a-custom-do-not-rewrite-urls-list"></a>사용자 지정 "다시 쓰지 않음" url 목록을 보거나 편집 하려면
  
1. [https://protection.office.com](https://protection.office.com) 으로 이동 하 여 회사 또는 학교 계정으로 로그인 합니다. 
    
2. 왼쪽 탐색 창의 **위협 관리** \> **정책** \> **안전한 링크**아래에 있습니다.
    
3. **특정 받는 사람에 게 적용 되는 정책** 섹션에서 **새로** 만들기 (새로 만들기 단추를 더하기 기호 ( **+**)와 유사)를 선택 하 여 새 정책을 만듭니다. 또는 기존 정책을 편집할 수 있습니다.<br/>![특정 전자 메일 받는 사람에 대 한 안전한 링크 정책을 추가 하려면 새로 만들기를 선택 합니다.](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
4. 정책에 대 한 이름 및 설명을 지정 합니다.
    
5. **다음 url을 다시 쓰지** 않음 구역에서 **올바른 url 입력** 상자를 선택 하 고 url을 입력 한 다음 더하기 기호 (+)를 선택 합니다. 
    
6. **적용 대상** 섹션에서 **받는 사람**을 선택 하 고 정책에 포함할 그룹을 선택 합니다. **추가**를 선택한 다음 **확인**을 선택 합니다.
    
7. url 추가가 완료 되 면 화면의 오른쪽 아래 모서리에서 **저장**을 선택 합니다.
    
> [!NOTE]
> 조직의 차단 된 url의 사용자 지정 목록을 검토 해야 합니다. [ATP 안전한 링크를 사용 하 여 차단 된 사용자 지정 url 목록 설정를](set-up-a-custom-blocked-urls-list-wtih-atp.md)참조 하세요. 
  
## <a name="important-points-to-keep-in-mind"></a>염두에 두어야 할 중요 사항

- "다시 쓰지 않음" 목록에서 지정 하는 url은 지정 된 받는 사람에 대 한 ATP 안전한 링크 검색에서 제외 됩니다.
 
- ATP 안전한 링크 정책에 대해 "다시 쓰지 않음" 목록을 지정 하는 경우 최대 3 개의 와일드 카드 별표 (\*)를 포함할 수 있습니다. 와일드 카드\*()는 `http://` or `https://`와 같은 접두사 `contoso.com`또는 하위 도메인을 명시적으로 포함 하지 않는 등의 항목에 대해 가정 됩니다. 즉, `contoso.com` "다시 쓰지 않음" 목록과 비슷한 `*contoso.com*` 항목을 의미 합니다.

- "다시 쓰지 않음" 목록에 이미 url 목록이 있는 경우 해당 목록을 검토 하 고 와일드 카드를 적절 하 게 추가 해야 합니다. 예를 들어 기존 목록에 항목이 `http://contoso.com/a` 있는 경우 정책 `http://contoso.com/a/b` 에 하위 경로를 포함 하려면 항목에 와일드 카드를 추가 하 여 표시 `http://contoso.com/a*`합니다.
    
- "다시 쓰지 않음" 목록에 지정한 url에 슬래시 (/)를 포함 하지 마십시오. 예를 들어 "다시 쓰지 `contoso.com/` 않음" 목록에 입력 하는 대신 enter 키 `contoso.com`를 누르십시오.
    
다음 표에는 입력 가능한 항목과 해당 항목이 갖는 영향에 대 한 예가 나와 있습니다.
    
|**예제 항목**|**수행 하는 작업**|
|:-----|:-----|
|`*contoso.com*`  <br/> |특정 받는 사람이 도메인, 하위 사이트 및 경로 (예: `http://www.contoso.com` `https://www.contoso.com` `https://maps.contoso.com`, 또는)를 사용할 수 있습니다.`http://www.contoso.com/a`  <br/> |
|`http://contoso.com/a`  <br/> |특정 받는 사람이 같은 사이트를 방문 하 `http://contoso.com/a`되 하위 경로는 볼 수 없습니다.`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a*`  <br/> |특정 받는 사람이 같은 사이트 `http://contoso.com/a` 와 같은 하위 경로를 방문할 수 있도록 허용`http://contoso.com/a/b`  <br/> |
   
 