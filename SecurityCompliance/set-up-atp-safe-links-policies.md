---
title: Office 365 ATP 안전한 링크 정책 설정
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
ms.assetid: bdd5372d-775e-4442-9c1b-609627b94b5d
description: Word, Excel, PowerPoint 및 Visio 파일에는 물론 전자 메일 메시지에 악의적인 링크를 통해 조직을 보호 하기 위해 안전한 링크 정책을 설정 합니다.
ms.openlocfilehash: 145e8998637756d204171f64021d6ad783b367f3
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28015060"
---
# <a name="set-up-office-365-atp-safe-links-policies"></a>Office 365 ATP 안전한 링크 정책 설정

[ATP 안전한 링크](atp-safe-links.md) , [Office 365 고급 위협 보호](office-365-atp.md) (ATP)의 기능으로는 피싱 및 기타 공격에 사용 되는 악의적인 링크를 통해 조직을 보호할 수 있습니다. 필요한 경우 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md), 않도록 하기 위한 사용자 웹 주소 (Url)를 클릭 하는 경우 ATP 안전한 링크 정책을 설정할 수 있습니다, 조직 보호 됩니다. ATP 안전한 링크 정책에는 전자 메일에 Url 및 Office 문서에서 Url을 검사 하도록 구성할 수 있습니다.
  
[새로운 기능 ATP에 추가 되 고 지속적으로 됩니다](office-365-atp.md#new-features-are-continually-being-added-to-atp). 새로운 기능 추가 될 때 기존 ATP 안전한 링크 정책에 따라 조정 해야할 수 있습니다.

## <a name="what-to-do"></a>수행할 작업 
  
1. [필수 구성 요소를 검토](#review-the-prerequisites)합니다.
    
2. [검토 하 고, 모든 사용자에 게 적용 되는 기본 ATP 안전한 링크 정책 편집](#define-an-atp-safe-links-policy-that-applies-to-everyone)합니다. 예, [ATP 안전한 링크에 대 한 차단 된 사용자 지정 Url 목록을 설정할](set-up-a-custom-blocked-urls-list-wtih-atp.md)수 있습니다.
    
3. [특정 전자 메일 받는 사람에 대 한 정책 추가 또는 편집을](#add-a-policy-for-specific-email-recipients)포함 한 [ATP 안전한 링크에 대 한 사용자 지정 "rewrite 수행" Url 목록 설정](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)합니다.
    
4. [ATP 안전한 링크 정책 옵션에 대 한 설명](#learn-about-atp-safe-links-policy-options) (이 문서의), 최근 변경 내용에 대 한 설정을 포함 하 여
    
## <a name="step-1-review-the-prerequisites"></a>1 단계: 필수 구성 요소를 검토 합니다.

- 조직에 [Office 365 고급 위협 보호](office-365-atp.md)있는지 확인 합니다.
    
- 정의 하거나 ATP 정책을 편집 하려면 필요한 권한이 있는지 확인 합니다. 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.

- Office 클라이언트 (Office 문서에서 ATP 안전한 링크 보호를 위한 임) [현대 인증](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) 을 사용 하도록 구성 되었는지 확인 합니다.
    
- [ATP 안전한 링크 정책 옵션에 대 한 설명](#learn-about-atp-safe-links-policy-options) (이 문서의). 

- 모든 Office 365 데이터 센터에 분산 하 여 신규 또는 업데이트 된 정책에 대 한 최대 30 분을 허용 합니다.
    
## <a name="step-2-define-or-review-the-atp-safe-links-policy-that-applies-to-everyone"></a>2 단계: 정의 (또는 검토) 모든 사람에 게 적용 되는 ATP 안전한 링크 정책

[Office 365 고급 위협 보호 기능](office-365-atp.md)을 사용 하는 조직에서 모든 사용자에 게 적용 되는 기본 ATP 안전한 링크 정책을 해야 합니다. 검토 하려면 다음을 확인 하 고 필요한 경우 기본 정책 편집 합니다.
  
1. 이동 [https://protection.office.com](https://protection.office.com) 와 작업이 나 교육용 계정 사용 하 여 로그인 합니다. 
    
2. **위협 관리**의 왼쪽된 탐색 영역에서 선택 **정책 \> ** **안전 링크**입니다.
    
3. **조직 전체에 적용 되는 정책** 섹션에서 **기본**을 선택 하 고 **편집** (편집 단추는 연필 유사)를 선택 합니다.<br/>![안전한 링크 보호에 대 한 기본 정책을 편집 하려면 편집을 클릭 합니다.](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
4. **차단 하는 다음 Url** 섹션에서 방문에서 조직에서 사람들이 것을 방지 하려는 하나 이상의 Url을 지정 합니다. ( [ATP 안전 링크를 사용 하 여 차단 된 Url 목록 사용자 지정 설정](set-up-a-custom-blocked-urls-list-wtih-atp.md)참조).
    
5. **전자 메일을 제외 하 고 콘텐츠에 적용 되는 설정** 섹션에서 선택 (또는 선택 취소) 원하는 옵션을 사용 하 여 합니다. (좋습니다 모든 옵션을 선택 하는.) 
    
6. **Save(저장)** 를 선택합니다.
    
## <a name="step-3-add-or-edit-atp-safe-links-policies-that-apply-to-specific-email-recipients"></a>3 단계: 추가 (또는 편집) 특정 전자 메일 받는 사람에 게 적용 되는 ATP 안전한 링크 정책

하거나 한 후 검토 (편집) 모든 사람에 게 적용 되는 기본 ATP 안전한 링크 정책, 특정 받는 사람에 게 적용 되는 추가 정책을 정의 하 여 다음 단계가입니다. 예, 추가 정책을 정의 하 여 기본 정책 예외를 지정할 수 있습니다. 
  
1. 이동 [https://protection.office.com](https://protection.office.com) 와 작업이 나 교육용 계정 사용 하 여 로그인 합니다. 
    
2. 왼쪽 탐색 영역 **위협 관리** **정책**을 선택 합니다.
    
3. **안전한 링크**를 선택 합니다.
    
4. **특정 받는 사람에 게 적용 되는 정책** 섹션에서 **새로 만들기** 를 선택 (새로 만들기 단추 유사한 더하기 기호 ( **+**)).<br/>![특정 전자 메일 받는 사람에 대 한 안전한 링크 정책을 추가 하려면 새로 만들기를 선택 합니다.](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
5. 정책에 대한 이름, 설명 및 설정을 지정합니다.<br/>**예제:** ATP 안전한 링크 보호 하지 않고 특정 웹사이트를 통해 클릭 하 여 조직에서 특정 그룹에 사용자를 허용 하지 않는 "를 통해 직접 클릭 없음" 이라는 정책을 설정 하려면 지정할 수 있습니다는 다음과 같은 권장 설정: 
    
  - **이름** 상자에 없는 직접 클릭 방문을 입력 합니다.
    
  - **설명** 상자에 같은 못하게의 대화 상대 ATP 안전한 링크 확인 하지 않고 웹사이트를 통해 클릭 하 여에서 특정 그룹에 대 한 설명을 입력 합니다.
    
  - **작업 선택** 섹션에서 **에서**선택 합니다.
    
  - **다운로드 가능한 콘텐츠를 검사 하려면 안전한 첨부 파일 사용을**선택 합니다.
    
  - 이 옵션을 사용할 수 있는 경우 **조직 내에서 보내는 메시지에 적용 안전 링크**를 선택 합니다.
    
  - **사용자를 클릭 하 여 원래 URL을 허용 하지 않습니다**를 선택 합니다.
    
  - (선택 사항 임) **다음 Url 다시 작성 하지 않는** 섹션에서 조직에 대 한 안전한 것으로 간주 되는 하나 이상의 Url을 지정 합니다. ( [ATP 안전 링크를 사용 하는 사용자 지정 "rewrite 수행" Url 목록 설정](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)참조)
    
  - **적용 된** 섹션에서 **받는 사람이의 구성원은**을 선택 하 고 정책에 포함 하려는 그룹을 선택 합니다. **추가**선택 하 고 **확인**을 선택 합니다.
    
6. **Save(저장)** 를 선택합니다.
    
## <a name="step-4-learn-about-atp-safe-links-policy-options"></a>4 단계: ATP 안전한 링크 정책 옵션에 알아보기

를 설정 하거나 ATP 안전한 링크 정책을 편집 하는 사용할 수 있는 여러 옵션이 표시 됩니다. 이러한 옵션을 모르는 경우 다음 표에 각 하나 및 영향을 주기를 설명 합니다. 다음과 같은 두가지 주요 유형의 ATP 안전한 링크 정책 정의 하거나 편집 하려면 기억 하십시오.
- 모든 사용자에 게 적용 되는 [기본 정책](#default-policy-options) 
- 추가 [하는 특정 받는 사람에 대해 정의 된 정책](#policies-that-apply-to-specific-email-recipients) 

### <a name="default-policy-options"></a>기본 정책 옵션

기본 정책 옵션은 조직에서 모든 사용자에 게 적용 됩니다.

|이 옵션  |기능  |
|---------|---------|
| **다음 Url을 차단 합니다.** <br/>    | 조직에는 사용자 지정 목록이 자동으로 차단 되는 Url 사용 하도록 설정 합니다. 사용자가이 목록의 URL을 클릭 하는 경우이 수행 하는 URL이 차단 하는 이유를 설명 하는 [경고 페이지](atp-safe-links-warning-pages.md) 에 합니다.<br/> 자세한 내용은 참조 [ATP 안전 링크를 사용 하 여 차단 된 Url 목록 사용자 지정을 설정 합니다.      |
| **Office 365 ProPlus, iOS에 대 한 Office 및 Android** <br/>    | 이 옵션을 선택 하면 보호 된 문서에서 Url에 적용 되는 ATP 안전한 링크 Office 365 ProPlus (Word, Excel 및 PowerPoint Windows 또는 Mac OS)에서 Office 문서 열기 iOS, 또는 Android 장치, Windows 및 Office Online (Word에서 Visio 2016 온라인, PowerPoint, Excel 온라인 온라인과 OneNote 온라인), 사용자가 Office 365에 로그인 제공 합니다. <br/><br/>**Windows에서 Office 2016**만 표시 되 면 다음 기능 업데이트에 도달 하지 Office 365 환경 아직 (하 고 이러한이 출시 예정). 그때까지 ATP 안전한 링크 보호는 Word 2016, 2016 Excel, PowerPoint 2016 또는 Windows에서 실행 되는 Visio 2016에 적용 됩니다.            |
| **사용자가 ATP 안전 링크를 클릭할 때 추적 하지 마십시오** <br/>  | 이 옵션을 선택 하는 경우 Url Word, Excel, PowerPoint 및 Visio 문서에 저장 되지 않은 대 한 데이터를 클릭 합니다.  <br/> |
|**사용자가 원래 URL에 대 한 ATP 안전 링크를 통해 클릭 수 없어** <br/> |이 옵션을 선택 하면 사용자가 악의적인 것으로 판단 되는 URL로 과거의 [경고 페이지](atp-safe-links-warning-pages.md) 를 진행할 수 없습니다.  <br/> |

### <a name="policies-that-apply-to-specific-email-recipients"></a>특정 전자 메일 받는 사람에 게 적용 되는 정책

|이 옵션  |기능  |
|---------|---------|
|**Off** <br/> |전자 메일 메시지에 Url을 검색 하지 않습니다.  <br/> 받는 사람에 게의 특정 그룹에 대 한 전자 메일 메시지에 Url 검색 하지 않는 규칙 등의 예외 규칙을 정의할 수 있습니다.  <br/> |
|**에서** <br/> |사용자가 전자 메일 메시지에 Url을 클릭할 때 ATP 안전한 링크 보호 기능을 통해 경로 사용자에 게 Url을 다시 생성 합니다.  <br/> 차단 된 또는 악성 Url의 목록에 대해 클릭 했을 때 URL을 확인 합니다.  <br/> |
|**안전한 첨부 파일을 사용 하 여 다운로드 가능한 콘텐츠를 검색 합니다.** <br/> |이 옵션을 선택 하는 경우에 다운로드 가능한 콘텐츠를 가리키는 Url은 검색 됩니다.  <br/> |
|**안전한 링크 조직 내에서 보내는 메시지에 적용** <br/> | 이 옵션을 사용 가능 하 고 선택한 경우 ATP 안전한 링크 보호 조직의 전자 메일 계정을 제공 된 사용자 간에 보낸 메시지는 Office 365에서 호스팅되는 전자 메일에 적용 됩니다.  <br/> |
|**사용자 클릭을 추적 하지 않습니다** <br/> |이 옵션을 선택 하면 외부 보낸에서 전자 메일에 Url이 저장 되지 않은 대 한 데이터를 클릭 합니다. 조직 내에서 보내는 전자 메일 메시지에 포함 된 링크에 대 한 추적 하는 URL 클릭 현재 지원 되지 않습니다.  <br/> |
|**사용자가 클릭 하 여 원래 URL을을 허용 하지 않습니다** <br/> |이 옵션을 선택 하면 사용자가 악의적인 것으로 판단 되는 URL로 과거의 [경고 페이지](atp-safe-links-warning-pages.md) 를 진행할 수 없습니다.  <br/> |
|**다음 Url 다시 작성 하지 않습니다** <br/> |그대로 Url을 의미 합니다. 조직에서 전자 메일 받는 사람에 게의 특정 그룹에 대 한 검사 하지 않아도 안전한 Url의 사용자 지정 목록을 유지 합니다.  와일드 카드 별표에 대 한 지원 하기 위해 최근 변경 내용을 포함 하는 더 자세한 [ATP 안전 링크를 사용 하는 사용자 지정 "rewrite 수행" Url 목록 설정](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) 참조 (\*).<br/> |
   
## <a name="next-steps"></a>다음 단계

ATP 안전한 링크 정책이 설정 되어, 되 면 사용자 orgnization에 대 한 보고서를 확인 하 여 ATP가 작동 하는 방법을 확인할 수 있습니다. 자세한 내용은 다음 리소스를 참조 하십시오.

- [Office 365 고급 위협 보호에 대 한 보고서 보기](view-reports-for-atp.md)

- [탐색기를 사용 하 여 보안에서 &amp; 준수 센터](use-explorer-in-security-and-compliance.md) 