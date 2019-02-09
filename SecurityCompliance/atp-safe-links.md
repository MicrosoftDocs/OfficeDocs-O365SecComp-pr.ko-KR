---
title: Office 365 ATP 안전한 링크
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.date: 02/05/2019
ms.topic: overview
f1_keywords:
- "197503"
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
- ZVO160
- ZXL160
- ZPP160
- ZWD160
ms.assetid: dd6a1fef-ec4a-4cf4-a25a-bb591c5811e3
description: 안전한 링크 기능은 다음 Office 문서 및 전자 메일 메시지에 하이퍼링크의 클릭 시간 확인 합니다. 피싱 및 기타 공격 으로부터 조직을 보호를 안전한 링크를 사용 합니다.
ms.openlocfilehash: 8c63de9e62e33dbca6dde5a5bb45a7f7875ab71f
ms.sourcegitcommit: c1c41744c2de89c9e172f817c8f73bb0ada81a58
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2019
ms.locfileid: "29792243"
---
# <a name="office-365-atp-safe-links"></a>Office 365 ATP 안전한 링크

## <a name="overview-of-office-365-atp-safe-links"></a>Office 365 ATP 안전 하 게 보호 링크의 개요 (영문)

> [!IMPORTANT]
> 이 문서는 기업 고객을 위한 것입니다. Outlook에서 안전한 링크에 대 한 정보에 대 한 자세한 내용은 홈 사용자 인 경우 [Outlook.com 고급 보안](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2)을 참조 하십시오.

Office 365 ATP 안전한 링크 ( [고급 위협 보호](office-365-atp.md)의 일부)는 클릭 시간 확인 [전자 메일 메시지](#how-atp-safe-links-works-with-email) 및 [Office 문서](#how-atp-safe-links-works-with-office-documents)에서 웹 주소 (Url)를 제공 하 여 조직을 보호할 수 있습니다. Office 365 보안 팀에 의해 설정 된 [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md) 을 통해 보호 정의 됩니다. 
  
ATP 안전한 링크 정책이 설정 되어, 되 면 Office 365 전역 관리자, 보안 관리자 및 보안 독자 [고급 위협 보호에 대 한 보고서 보기](view-reports-for-atp.md)수 있습니다. 이러한 보고서의 정보에는 조직을 보호 하거나 보안 문제를 조사 하는 추가 단계를 수행 하 여 보안 팀 데 도움이 됩니다.

[ATP에 새로운 기능이 추가 됩니다](office-365-atp.md#new-features-are-continually-being-added-to-atp)Office 365 보안 팀 추가 수 또는 조직의 ATP 안전한 링크 정책을 편집 합니다. 또한 변경 사항 및 향상 된 기능에서는 새로 수정 된 [경고 페이지](atp-safe-links-warning-pages.md) 및 Outlook에서 렌더링 되는 기본 링크와 같은 것을 알 수 있습니다.
         
## <a name="how-atp-safe-links-works-with-urls-in-email"></a>ATP 안전한 링크 Url이 포함 된 전자 메일에서 작동 하는 방법

높은 수준의 같습니다 ATP 안전한 링크 보호 Url에 대 한 전자 메일 (Office 365를 하지 온-프레미스에 호스트)에서 작동 하는 방법.
  
1. 사용자는 전자 메일 메시지, Url을 포함 하는 중 일부를 받습니다.
    
2. IP (인터넷 프로토콜) 및 봉투를 필터링 하는 Exchange Online Protection을 통해 이동 모든 전자 메일 서명 기반 맬웨어 방지, 스팸 방지 및 맬웨어 방지 필터 적용 됩니다. 
    
3. 전자 메일 사용자의 받은 편지함에 도착합니다.
    
4. 사용자는 Office 365에 로그인 하 고 자신의 전자 메일 받은 편지 함으로 이동 됩니다.
    
5. 사용자 전자 메일 메시지로 열리고 전자 메일 메시지에서 URL에 대해를 클릭 합니다.
    
6. ATP 안전한 링크 기능 웹사이트를 열기 전에 URL을 확인 하는 즉시 합니다. 악의적인, 또는 안전 차단 URL은 식별 합니다.
    
    - URL 인 사용자에 게 적용 되는 정책에 대 한 [사용자 지정 "rewrite 수행" Url 목록](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) 에 포함 된 사이트를 참조 하는 경우 웹사이트를 엽니다. 
    
    - 조직의 [차단 된 사용자 지정 Url 목록](set-up-a-custom-blocked-urls-list-wtih-atp.md)에 포함 된 웹사이트에 URL이 있는 경우 [경고 페이지가](atp-safe-links-warning-pages.md) 열립니다. 
    
    - 악성 코드가 포함 될으로 확인 된 사이트로 URL이 있는 경우 [경고 페이지가](atp-safe-links-warning-pages.md) 열립니다. 
    
    - 다운로드 가능한 파일에 URL 이동 하는 경우 조직의 [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md) 은 이러한 콘텐츠를 검사 하도록 구성 된 다운로드 파일을 검사 합니다. 
    
    - URL을 안전한 것으로 확인 하는 경우 웹사이트를 엽니다.
    
## <a name="how-atp-safe-links-works-with-urls-in-office-documents"></a>ATP 안전한 링크 Url이 포함 된 Office 문서에서 작동 하는 방법

높은 수준의 같습니다 ATP 안전한 링크 보호 Url에 대 한 Office 365 ProPlus 응용 프로그램 (Word, Excel 및 PowerPoint Windows 또는 Mac, iOS 또는 Android 장치, Windows, OneNote Online 및 Office Online에서 Visio에 Office 응용 프로그램에서의 현재 버전)에서 작동 하는 방법.
  
1. 사람들이 자신의 컴퓨터, smartphone 또는 태블릿에 Office 365 ProPlus를 설치 했습니다. (또는 자신의 브라우저에서 Office Online 사용 됩니다.)
    
2. 사용자가 Word, Excel, PowerPoint 또는 Visio를 열고 자신의 작업이 나 교육용 계정을 사용 하 여 Office 365 엔터프라이즈에 로그인 합니다. 다음은 문서 Url이 들어 있습니다.
    
3. 사용자가 문서에 URL을 클릭 하면 ATP 안전한 링크 서비스에 대 한 링크를 검사 합니다.
    
  - URL 인 사용자에 게 적용 되는 정책에 대 한 [사용자 지정 "rewrite 수행" Url 목록](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) 에 포함 된 사이트를 참조 하는 경우 해당 사용자는 웹사이트에 가져옵니다. 
    
  - 조직의 [차단 된 사용자 지정 Url 목록](set-up-a-custom-blocked-urls-list-wtih-atp.md)에 포함 된 웹사이트에 URL이 있는 경우 [경고 페이지](atp-safe-links-warning-pages.md)로 이동 합니다.
    
  - 악성 코드가 포함 될으로 확인 된 사이트로 URL이 있는 경우 [경고 페이지](atp-safe-links-warning-pages.md)로 이동 합니다.
    
  - URL 다운로드 가능한 파일에 들어가고 [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md) 은 이러한 다운로드를 검색 하도록 구성 된 경우 다운로드 파일을 검사 합니다. 
    
  - URL은 안전한으로 간주 하는 경우 사용자 웹사이트를 가져옵니다.

## <a name="how-to-get-atp-safe-links-protection"></a>ATP 안전한 링크 보호 하는 방법

먼저, 구독 [고급 위협 보호](office-365-atp.md)를 포함 해야 합니다. ATP에 [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home)"," [Microsoft 365 비즈니스](https://www.microsoft.com/microsoft-365/business)"," Office 365 엔터프라이즈 e 5 "," Office 365 교육 A5 "," 등의 구독에 포함 됩니다. 조직에 Office 365 ATP를 포함 하지 않는 한 Office 365 구독을 하는 경우에 추가 기능으로 ATP을 잠재적으로 구입할 수 있습니다. 자세한 내용은 [Office 365 고급 위협 보호 계획 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [Office 365 고급 위협 Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)을 참조 하십시오. 
  
다음으로, ATP 안전한 링크 정책에 정의 된 확인 합니다. ( [Office 365 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)참조). ATP 안전한 링크 기능은 현재 경우:
  
- Word, Excel, PowerPoint 및 Visio 문서 및 전자 메일에 대 한 **ATP 안전한 링크 정책을 설정** 합니다. ( [Office 365의 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)참조).

- **Office 365 클라이언트 앱 현대 인증을 사용 하도록 구성 된** (이것은 Office 문서에서 ATP 안전한 링크 보호를 위한)입니다. ( [Office 2016에 대 한 최신 인증](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016)참조). 
    
- 사용자의 작업이 나 교육용 계정을 사용 하 여 **사용자가 Office 365에 로그인 됩니다** . ( [Office 또는 Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426)참조).
    
- **조직의 전자 메일은 Office 365에서 호스팅됩니다**. 

ATP 정책, 정의 (또는 편집)를 할당 되어 있어야 다음 표에 설명 된 역할 중 하나:

|역할  |Where/방법 할당  |
|---------|---------|
|Office 365 전역 관리자 |Office 365를 구매 하 여를 로그인 하는 사람 이름은 기본적으로 전역 admin입니다. (자세한 내용은 [Office 365에 대 한 관리자 역할](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 참조 하십시오.)         |
|보안 관리자 |Azure Active Directory 관리 센터 ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Exchange Online 조직 관리 |Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>또는 <br>  PowerShell cmdlet (참조 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
## <a name="how-to-make-sure-atp-safe-links-protection-is-in-place"></a>원본 위치에는 있는지 ATP 안전한 링크 보호 하는 방법

전역 관리자 또는 보안 관리자, [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md)을 검토 해야 합니다. ATP 안전한 링크 정책은 여부 보호 적용 하는 전자 메일 메시지에 하이퍼링크에만, 또는 Url에 Office 문서에도에서 결정 합니다.

ATP 안전한 링크 정책이 설정 되어, 한 후에 조직의 보안 팀 볼 수 [고급 위협 보호에 대 한 보기 보고서](view-reports-for-atp.md)크기는 조직에 대 한 ATP 안전한 링크 보호가 작동 하는 방법을 참조 하십시오. 

## <a name="example-scenarios"></a>예제 시나리오
  
다음 표에서 일부 예제 시나리오를 ATP 안전한 링크 보호 수도 있고 전체에서 되지 않을 수 있습니다. (모든 이러한 경우 가정 조직에 Office 365 Enterprise e 5.)
  
|**시나리오 예**|**ATP 안전한 링크 보호는이 경우에 적용 여부**|
|:-----|:-----|
|Jean에 Url을 전자 메일 및 Office 문서에서 다루는 ATP 안전한 링크 정책이 있는 그룹의 구성원입니다. Jean은 PowerPoint 프레젠테이션, 보낸 사람이 열리고 프레젠테이션에서 URL을 클릭 합니다.  <br/> |예입니다. 정의 된는 ATP 안전한 링크 정책이 Jean의 그룹, Jean의 전자 메일 및 Jean 열리는 Jean 로그인을 Word, Excel, PowerPoint 또는 Visio 문서 및 Windows, iOS, 또는 Android 장치에서 Office 365 ProPlus를 사용 하 여 적용 됩니다.  <br/> |
|Chris의 조직, 더 전역 또는 보안 관리자에서 모든 ATP 안전한 링크 정책을 아직 정의 했습니다. Chris 악성 웹사이트에 대 한 URL을 포함 하는 전자 메일을 받습니다. Chris 인식 하지 않으며 URL은 악의적인 및 링크를 클릭 합니다.  <br/> |아니요. 원본 위치에 있는 것으로 보호 하기 위해에서 조직의 모든 사용자에 대 한 Url을 적용 하는 기본 정책 정의 되어야 합니다.  <br/> |
|Pat의 조직, 더 전역 또는 보안 관리자가 정의 했거나 아직 모든 ATP 안전한 링크 정책을 편집 합니다. Pat은 Word 문서를 열리고 파일의 URL을 클릭 합니다.  <br/> |원본 위치에 있는 것으로 보호 하기 위해에서 Office 문서를 포함 하는 아니요 A 정책 정의 되어야 합니다. [Office 365의 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)참조 하십시오.<br/> |
|백화점 ㈜의 조직에 포함 된 ATP 안전한 링크 정책이 `http://tailspintoys.com` 차단 된 웹사이트도 나열 합니다. Lee에 대 한 URL을 포함 하는 전자 메일 메시지를 수신 `http://tailspintoys.com/aboutus/trythispage`합니다. Lee가 URL을 클릭 합니다.<br/> |전체 사이트와 그 하위의 목록에 포함 된 모든 Url을 차단 여부에 따라 다릅니다. [ATP 안전 링크를 사용 하 여 차단 된 Url 목록 사용자 지정 설정](set-up-a-custom-blocked-urls-list-wtih-atp.md)을 참조 하십시오.<br/> |
|김 Jean의 동료, 전자 메일을 보내 Jean, 악성 URL이 전자 메일에 포함 된 정확히 모르는 합니다.  <br/> |ATP 안전한 링크 정책을 조직 내에서 보낸 전자 메일에 대해 정의 되는 여부에 따라 다릅니다. [Office 365의 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)참조 하십시오.<br/> |


  

