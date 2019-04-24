---
title: Office 365 ATP 안전한 링크를 사용 하 여 차단 된 사용자 지정 url 목록 설정
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
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
ms.collection:
- M365-security-compliance
description: Office 365 Advanced Threat Protection을 사용 하 여 조직에 대해 차단 된 url 목록을 설정 하는 방법을 알아봅니다. 차단 된 url은 ATP 안전한 링크 정책에 따라 전자 메일 메시지 및 Office 문서에 적용 됩니다.
ms.openlocfilehash: c5444e644a35688ea626004fbc6865df4ae645f9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264526"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a>Office 365 ATP 안전한 링크를 사용 하 여 차단 된 사용자 지정 url 목록 설정

> [!IMPORTANT]
> 이 문서는 비즈니스 고객을 위한 것입니다. Outlook의 안전한 링크에 대 한 정보를 검색 하는 개인 사용자는 [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2)를 참조 하십시오.

[Office 365 ATP (Advanced Threat Protection](office-365-atp.md) )를 사용 하는 경우 조직에는 차단 된 웹 사이트 주소 (url)의 사용자 지정 목록이 있을 수 있습니다. url이 차단 되 면 차단 된 url에 대 한 링크를 클릭 하는 사용자는 다음 이미지와 비슷한 [경고 페이지로](atp-safe-links-warning-pages.md) 이동 합니다. 
  
![이 사이트는 차단 됨](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
차단 된 url 목록은 조직의 Office 365 보안 팀에서 정의 되며,이 목록은 office 365 ATP 안전한 링크 정책에서 다루는 조직의 모든 사용자에 게 적용 됩니다. 
  
이 문서를 읽으면 [Office 365에서 ATP 안전한 링크](atp-safe-links.md)에 대 한 조직의 사용자 지정 차단 된 url 목록을 설정 하는 방법에 대해 알아봅니다.
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a>차단 된 url의 사용자 지정 목록 보기 또는 편집

[Office 365의 ATP 안전한 링크](atp-safe-links.md) 는 조직의 사용자 지정 차단 된 url 목록을 포함 하 여 여러 목록을 사용 합니다. 필요한 사용 권한이 있는 경우 조직의 사용자 지정 목록을 설정할 수 있습니다. 조직의 기본 안전 링크 정책을 편집 하 여이 작업을 수행 합니다.

ATP 정책을 편집 하거나 정의 하려면 다음 표에 설명 된 역할 중 하나를 할당 받아야 합니다. 

|역할  |할당 된 위치/방법  |
|---------|---------|
|Office 365 전역 관리자 |Office 365을 구매 하기 위해 등록 하는 사람은 기본적으로 전역 관리자입니다. 자세한 내용은 [Office 365 관리자 역할 정보](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 를 참조 하세요.         |
|보안 관리자 |Azure Active Directory 관리 센터 ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Exchange Online 조직 관리 |Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br> 선택하거나  <br>  PowerShell cmdlet ( [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조) |

> [!TIP]
> 역할 및 사용 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.

### <a name="to-view-or-edit-a-custom-blocked-urls-list"></a>사용자 지정 차단 된 url 목록을 보거나 편집 하려면
  
1. [https://protection.office.com](https://protection.office.com) 으로 이동 하 여 회사 또는 학교 계정으로 로그인 합니다. 
    
2. 왼쪽 탐색 창의 **위협 관리**에서 **정책** \> **안전한 링크**를 선택 합니다.
    
3. **전체 조직에 적용 되는 정책** 섹션에서 **기본값**을 선택 하 고 **편집** (편집 단추는 연필과 유사)을 선택 합니다.<br/>![안전한 링크 보호에 대 한 기본 정책을 편집 하려면 편집을 클릭 합니다.](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)<br/>이렇게 하면 차단 된 url 목록을 볼 수 있습니다. 처음에는 여기에 나열 된 url이 없을 수도 있습니다.<br/>![기본 안전 링크 정책의 차단 된 url 목록](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)
  
4. **올바른 url 입력** 상자를 선택 하 고 URL을 입력 한 다음 더하기 기호 (**+**)를 선택 합니다. 

5. url 추가가 완료 되 면 화면의 오른쪽 아래 모서리에서 **저장**을 선택 합니다.
    
## <a name="a-few-things-to-keep-in-mind"></a>염두에 두어야 할 몇 가지 사항

목록에 url을 추가 하는 동안 다음 사항을 염두에 두어야 합니다. 

- URL의 끝에 슬래시 ( **/**)를 포함 하지 마십시오. 예를 들어 `http://www.contoso.com/`를 입력 하는 대신 `http://www.contoso.com`를 입력 합니다.
    
- 도메인 전용 URL (like `contoso.com` 또는 `tailspintoys.com`)을 지정할 수 있습니다. 이렇게 하면 도메인을 포함 하는 모든 URL의 클릭이 차단 됩니다.

- 전체 도메인 `contoso.com`을 차단 하지 않고 하위 `toys.contoso.com*`도메인을 지정할 수 있습니다 (like). 하위 도메인이 포함 된 url을 클릭 하는 것을 차단 하지만 전체 도메인이 포함 된 url을 클릭 하는 것을 차단 하지는 않습니다.  
    
- URL 당 최대 3 개의 와일드 카드 별표 (\*)를 포함할 수 있습니다. 다음 표에는 입력 가능한 항목과 해당 항목이 갖는 영향에 대 한 몇 가지 예가 나와 있습니다.
    
|**예제 항목**|**수행 하는 작업**|
|:-----|:-----|
|`contoso.com`사용자나`*contoso.com*`  <br/> |는과 같은 `https://www.contoso.com` `http://sub.contoso.com`도메인, 하위 도메인과 경로를 차단 하며`http://contoso.com/abc`  <br/> |
|`http://contoso.com/a`  <br/> |사이트 `http://contoso.com/a` 를 차단 하지만 추가 하위 경로는 제외 합니다.`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a*`  <br/> |사이트 `http://contoso.com/a` 및 추가 하위 경로를 차단 합니다.`http://contoso.com/a/b`  <br/> |
|`http://toys.contoso.com*`  <br/> |하위 도메인 (이 경우 "장난감")을 차단 하지만 클릭은 다른 도메인 url (예 `http://contoso.com` , 또는 `http://home.contoso.com`)을 허용 합니다.  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a>조직의 특정 사용자에 대 한 예외를 정의 하는 방법

특정 그룹에서 다른 사용자에 대해 차단 될 수 있는 url을 볼 수 있도록 하려면 특정 받는 사람에 게 적용 되는 ATP 안전한 링크 정책을 지정 하면 됩니다. [ATP 안전한 링크를 사용 하 여 사용자 지정 "재작성 금지" url 목록 설정를](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)참조 하세요.
  

