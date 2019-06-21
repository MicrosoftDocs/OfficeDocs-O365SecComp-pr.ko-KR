---
title: Office 365 ATP 안전한 링크 정책 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: Admin
ms.topic: article
ms.date: 02/26/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: bdd5372d-775e-4442-9c1b-609627b94b5d
ms.collection:
- M365-security-compliance
description: 안전한 링크 정책을 설정 하 여 Word, Excel, PowerPoint, Visio 파일 및 전자 메일 메시지의 악의적인 링크 로부터 조직을 보호 합니다.
ms.openlocfilehash: 505508771ae1e630d7d34fde9ee1525d19bd5039
ms.sourcegitcommit: b00c8fe1827d24f055a3076c10f284ff9ee3e04b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/20/2019
ms.locfileid: "35113262"
---
# <a name="set-up-office-365-atp-safe-links-policies"></a>Office 365 ATP 안전한 링크 정책 설정

> [!IMPORTANT]
> 이 문서는 [Office 365 Advanced Threat Protection](office-365-atp.md)을 사용 하는 비즈니스 고객을 위한 것입니다. Outlook의 안전한 링크에 대 한 정보를 검색 하는 개인 사용자는 [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2)를 참조 하십시오.

[Atp 안전한 링크](atp-safe-links.md)( [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP)의 기능)는 피싱 및 기타 공격에 사용 되는 악의적인 링크 로부터 조직을 보호 하는 데 도움이 될 수 있습니다. [Office 365 보안 &amp; 및 준수 센터에 대 한 필요한 권한이](permissions-in-the-security-and-compliance-center.md)있는 경우 ATP 안전한 링크 정책을 설정 하 여 사용자가 웹 주소 (url)를 클릭할 때 조직이 보호 되는지 확인할 수 있습니다. Office 문서에서 전자 메일 및 Url의 url을 검색 하도록 ATP 안전한 링크 정책을 구성할 수 있습니다.
  
[새 기능은 ATP에 계속 추가 됩니다](office-365-atp.md#new-features-in-office-365-atp). 새 기능을 추가 하면 기존 ATP 안전한 링크 정책을 조정 해야 할 수 있습니다.

## <a name="what-to-do"></a>수행할 작업 
  
1. 필수 구성 요소를 검토 합니다.
    
2. 모든 사용자에 게 적용 되는 기본 ATP 안전한 링크 정책을 검토 하 고 편집 합니다. 예를 들어 [ATP 안전한 링크에 대해 차단 된 사용자 지정 url 목록을 설정할](set-up-a-custom-blocked-urls-list-wtih-atp.md)수 있습니다.
    
3. [ATP 안전한 링크에 대 한 사용자 지정 "재작성 금지" url 목록 설정을](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)비롯 하 여 특정 전자 메일 받는 사람에 대 한 정책을 추가 하거나 편집 합니다.
    
4. 최근 변경 내용에 대 한 설정을 포함 하 여이 문서의 ATP 안전한 링크 정책 옵션에 대해 알아봅니다.
    
## <a name="step-1-review-the-prerequisites"></a>1 단계: 필수 구성 요소 검토

- 조직에 [Office 365 Advanced Threat Protection](office-365-atp.md)이 있는지 확인 합니다.
    
- 필요한 사용 권한이 있는지 확인 합니다. ATP 정책을 정의 하거나 편집 하려면 적절 한 역할이 할당 되어 있어야 합니다. 다음 표에서는 몇 가지 예를 설명 합니다. <br>

    |역할  |할당 된 위치/방법  |
    |---------|---------|
    |Office 365 전역 관리자 |Office 365을 구매 하기 위해 등록 하는 사람은 기본적으로 전역 관리자입니다. 자세한 내용은 [Office 365 관리자 역할 정보](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 를 참조 하세요.         |
    |보안 관리자 |Azure Active Directory 관리 센터 ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
    |Exchange Online 조직 관리 |Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>또는 <br>  PowerShell cmdlet ( [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조) |

    역할 및 사용 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.

- Office 클라이언트가 [최신 인증](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) 을 사용 하도록 구성 되어 있는지 확인 합니다 (office 문서에서 ATP 안전한 링크 보호를 위한 기능).
    
- [ATP 안전한 링크 정책 옵션에 대 한 자세한](#step-4-learn-about-atp-safe-links-policy-options) 정보 이 문서에서 설명 합니다. 

- 새 정책이 나 업데이트 된 정책을 모든 Office 365 데이터 센터에 전파 하는 데 최대 30 분 정도 걸릴 수 있습니다.
    
## <a name="step-2-define-or-review-the-atp-safe-links-policy-that-applies-to-everyone"></a>2 단계: 모든 사용자에 게 적용 되는 ATP 안전한 링크 정책 정의 또는 검토

[Office 365 Advanced Threat Protection](office-365-atp.md)이 있으면 조직의 모든 사용자에 게 적용 되는 기본 ATP 안전한 링크 정책이 제공 됩니다. 기본 정책을 검토 하 고 필요에 따라 편집 합니다.
  
1. [https://protection.office.com](https://protection.office.com) 으로 이동 하 여 회사 또는 학교 계정으로 로그인 합니다. 
    
2. 왼쪽 탐색 창의 **위협 관리**에서 ** \> 정책** **안전한 링크**를 선택 합니다.
    
3. **전체 조직에 적용 되는 정책** 섹션에서 **기본값**을 선택 하 고 **편집** (편집 단추는 연필과 유사)을 선택 합니다.<br/>![안전한 링크 보호에 대 한 기본 정책을 편집 하려면 편집을 클릭 합니다.](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
4. **다음 Url 차단** 섹션에서 조직의 사용자가 방문 하지 못하도록 할 url을 하나 이상 지정 합니다. ( [ATP 안전한 링크를 사용 하 여 사용자 지정 차단 된 url 목록 설정](set-up-a-custom-blocked-urls-list-wtih-atp.md)참조)
    
5. **전자 메일을 제외한 콘텐츠에 적용 되는 설정** 섹션에서 사용할 옵션을 선택 하거나 선택을 취소 합니다. (모든 옵션을 선택 하는 것이 좋습니다.) 
    
6. **저장**을 선택합니다.
    
## <a name="step-3-add-or-edit-atp-safe-links-policies-that-apply-to-specific-email-recipients"></a>3 단계: 특정 전자 메일 받는 사람에 게 적용 되는 ATP 안전한 링크 정책 추가 (또는 편집)

모든 사용자에 게 적용 되는 기본 ATP 안전 링크 정책을 검토 하거나 편집한 후에는 특정 받는 사람에 게 적용 되는 추가 정책을 정의 합니다. 예를 들어 추가 정책을 정의 하 여 기본 정책에 대 한 예외를 지정할 수 있습니다. 
  
1. [https://protection.office.com](https://protection.office.com) 으로 이동 하 여 회사 또는 학교 계정으로 로그인 합니다. 
    
2. 왼쪽 탐색 창의 **위협 관리**에서 **정책을**선택 합니다.
    
3. **안전한 링크**를 선택 합니다.
    
4. **특정 받는 사람에 게 적용 되는 정책** 섹션에서 **새로 만들기** (새로 만들기 단추는 더하기 기호 ( **+**)와 유사)를 선택 합니다.<br/>![특정 전자 메일 받는 사람에 대 한 안전한 링크 정책을 추가 하려면 새로 만들기를 선택 합니다.](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
5. 정책에 대한 이름, 설명 및 설정을 지정합니다.<br/>**예:** 조직에 있는 특정 그룹의 사용자가 안전한 링크 보호를 사용 하지 않고 특정 웹 사이트로 이동할 수 없도록 하는 "직접 클릭 없음" 정책을 설정 하려면 다음과 같은 권장 설정을 지정 하면 됩니다. 
    
  - **이름** 상자에 직접 클릭 안 함을 입력 합니다.
    
  - **설명** 상자에 설명 (예)을 입력 하 여 특정 그룹의 사용자가 안전한 링크 확인을 수행 하지 않고 웹 사이트로 이동 하는 것을 방지할 수 있습니다.
    
  - **작업 선택** 섹션에서 **설정**를 선택 합니다.
    
  - **다운로드 가능한 콘텐츠를 검색 하려면 안전한 첨부 파일 사용을**선택 합니다.
    
  - 이 옵션을 사용할 수 있는 경우 **조직 내에서 보낸 메시지에 안전한 링크 적용**을 선택 합니다.
    
  - **사용자가 원래 URL을 클릭 하도록 허용 안 함을**선택 합니다.
    
  - (선택 사항) **다음 url을 다시 쓰지** 않음 섹션에서 조직에 안전한 것으로 간주 되는 하나 이상의 url을 지정 합니다. ( [ATP 안전한 링크를 사용 하 여 사용자 지정 "재작성 금지" url 목록 설정](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)참조)
    
  - **적용 대상** 섹션에서 **받는 사람**을 선택 하 고 정책에 포함할 그룹을 선택 합니다. **추가**를 선택한 다음 **확인**을 선택 합니다.
    
6. **저장**을 선택합니다.
    
## <a name="step-4-learn-about-atp-safe-links-policy-options"></a>4 단계: ATP 안전한 링크 정책 옵션 알아보기

ATP 안전한 링크 정책을 설정 하거나 편집할 때 몇 가지 옵션을 사용할 수 있습니다. 이러한 옵션이 무엇 인지 궁금할 경우 다음 표에서는 각 옵션에 대해 설명 합니다. 두 가지 주요 유형의 ATP 안전한 링크 정책을 정의 하거나 편집할 수 있습니다.
- 모든 사용자에 게 적용 되는 [기본 정책](#default-policy-options) 입니다. 한  
- [특정 받는 사람에 대 한 추가 정책](#policies-that-apply-to-specific-email-recipients) 

### <a name="default-policy-options"></a>기본 정책 옵션

기본 정책 옵션은 조직의 모든 사용자에 게 적용 됩니다.

|이 옵션  |기능  |
|---------|---------|
| **다음 Url 차단** <br/>    | 조직에서 자동으로 차단 되는 Url의 사용자 지정 목록을 사용할 수 있도록 합니다. 사용자가이 목록에서 URL을 클릭 하면 URL이 차단 되는 이유를 설명 하는 [경고 페이지가](atp-safe-links-warning-pages.md) 표시 됩니다. 자세한 내용은 [Office 365 ATP 안전한 링크를 사용 하 여 사용자 지정 차단 된 url 목록 설정](set-up-a-custom-blocked-urls-list-wtih-atp.md)를 참조 하세요. |
| **Office 365 ProPlus, iOS 및 Android 용 Office** <br/>    | 이 옵션을 선택 하면 ATP Safe Links 보호는 Word, Excel 및 PowerPoint 파일의 Windows 또는 Mac OS, iOS 또는 Android 장치의 Office 문서, Windows의 Visio 2016, 웹 버전의 Office 앱 (Word, PowerPoint, Excel 및 OneNote)-사용자가 Office 365에 로그인 했습니다. |
| **사용자가 ATP 안전한 링크 클릭 시기 추적 안 함** <br/>  | 이 옵션을 선택 하면 Word, Excel, PowerPoint 및 Visio 문서의 Url에 대 한 데이터를 클릭 해도 저장 되지 않습니다.  <br/> |
|**사용자가 ATP 안전한 링크를 원본 URL로 클릭할 수 없도록 합니다.** <br/> |이 옵션을 선택 하면 사용자가 [경고 페이지](atp-safe-links-warning-pages.md) 를 지 나 악의적인 것으로 확인 된 URL로 계속할 수 없습니다.  <br/> |

### <a name="policies-that-apply-to-specific-email-recipients"></a>특정 전자 메일 받는 사람에 게 적용 되는 정책

|이 옵션  |기능  |
|---------|---------|
|**해제** <br/> |전자 메일 메시지의 Url을 검사 하지 않습니다.  <br/> 특정 받는 사람 그룹에 대 한 전자 메일 메시지의 Url을 검색 하지 않는 규칙과 같은 예외 규칙을 정의할 수 있습니다.  <br/> |
|**켜짐** <br/> |사용자가 전자 메일 메시지의 Url을 클릭할 때 ATP 안전한 링크 보호를 통해 사용자를 라우팅하기 위해 Url을 다시 작성 합니다.  <br/> 차단 되거나 악성 Url 목록에서 URL을 클릭 하 여 확인 합니다.  <br/> |
|**다운로드 가능한 콘텐츠를 검색 하기 위해 안전한 첨부 파일 사용** <br/> |이 옵션을 선택 하면 다운로드 가능한 콘텐츠를 가리키는 Url이 검색 됩니다.  <br/> |
|**조직 내에서 전송 된 메시지에 안전한 링크 적용** <br/> | 이 옵션을 사용할 수 있고 선택 하면 전자 메일 계정이 Office 365에서 호스팅되는 경우 ATP 안전한 링크 보호가 조직의 사용자 간에 전송 된 전자 메일 메시지에 적용 됩니다.  <br/> |
|**사용자 클릭 추적 안 함** <br/> |이 옵션을 선택 하면 외부 보낸 사람 으로부터 온 전자 메일의 Url에 대 한 데이터가 저장 되지 않습니다 .를 클릭 합니다. URL이 조직 내에서 전송 된 전자 메일 메시지 내의 링크에 대 한 추적을 클릭 하는 것은 현재 지원 되지 않습니다.  <br/> |
|**사용자가 원래 URL로 클릭 하도록 허용 안 함** <br/> |이 옵션을 선택 하면 사용자가 [경고 페이지](atp-safe-links-warning-pages.md) 를 지 나 악의적인 것으로 확인 된 URL로 계속할 수 없습니다.  <br/> |
|**다음 Url을 다시 쓰지 않습니다.** <br/> |Url은 그대로 둡니다. 조직의 특정 전자 메일 받는 사람 그룹에 대해 검색이 필요 없는 안전한 Url의 사용자 지정 목록을 보관 합니다.  최근 변경 내용을 와일드 카드 별표 (\*)를 포함 하 여 자세한 내용을 보려면 [ATP Safe 링크를 사용 하 여 사용자 지정 "재작성 금지" url 목록을 설정](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) 합니다 .를 참조 하세요.  <br/> |
   
## <a name="next-steps"></a>다음 단계

ATP 안전한 링크 정책이 마련 되 면 보고서를 확인 하 여 ATP가 어떻게 작동 하는지 볼 수 있습니다. 자세히 알아보려면 다음 리소스를 참조 하세요.

- [Office 365 Advanced Threat Protection에 대 한 보고서 보기](view-reports-for-atp.md)

- [보안 &amp; 및 준수 센터에서 탐색기 사용](use-explorer-in-security-and-compliance.md)

ATP에 게 제공 되는 새로운 기능에 대해서는 계속 제공 합니다. [Microsoft 365 로드맵을](https://www.microsoft.com/microsoft-365/roadmap?filters=O365) 방문 하 여 [ATP에 추가 되는 새로운 기능](office-365-atp.md#new-features-in-office-365-atp)에 대해 알아보세요.