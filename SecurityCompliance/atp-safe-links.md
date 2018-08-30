---
title: Office 365 ATP 안전한 링크
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
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
ms.openlocfilehash: dcb5f681d8d7c2ff92aeecb46388e59c406fa0f9
ms.sourcegitcommit: ddfa0ac1f8ef95a78dcc1468241ef29363d56b5b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/30/2018
ms.locfileid: "23520137"
---
# <a name="office-365-atp-safe-links"></a>Office 365 ATP 안전한 링크

Office 365 ATP 안전한 링크 (ATP 안전 링크) (과 함께 [Office 365 ATP 안전한 첨부 파일](atp-safe-attachments.md))은 엔터프라이즈 조직에 대 한 [Office 365 고급 위협 보호](office-365-atp.md) 의 일부분으로 제공 되는 보안 기능 집합입니다. ATP 안전한 링크 보호 하는 조직 클릭 시간 확인의 웹 주소 (Url)를 제공 하 여 Office 문서 및 전자 메일 메시지에 있습니다. Office 365 보안 팀에 의해 설정 된 [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md) 을 통해 보호 정의 됩니다. 
  
ATP 안전한 링크 정책이 설정 되어, 되 면 Office 365 전역 관리자, 보안 관리자 및 보안 독자 [고급 위협 보호에 대 한 보고서 보기](view-reports-for-atp.md)수 있습니다. 이러한 보고서의 정보에는 조직을 보호 하거나 보안 문제를 조사 하는 추가 단계를 수행 하 여 보안 팀 데 도움이 됩니다.
  
새로운 기능 ATP 안전 링크를 지속적으로 추가 되 고 됩니다.
  
- 가능한 가장 늦은 년 10 월 2017 부터는 ATP 안전한 링크 보호에 적용할 Url Url를 비롯 하 여 전자 메일에 Office 365 ProPlus 문서, Word, Excel, PowerPoint, Visio 등의 Office와 함께 Windows, iOS 및 Android 장치에서 앱까지 확장 됩니다.
    
- 3 월 2018 부터는 ATP 안전한 링크 보호 조직의 구성원 사이 전송 하는 전자 메일에 적용할까지 확장 됩니다.
    
- 2018의 후반부에서 시작, ATP 안전한 링크 보호 Office Online (Word 온라인, Excel, PowerPoint 온라인 온라인과 OneNote 온라인) 및 Mac.에서 Office 365 ProPlus의 Url에 적용 하기 위해 확장
    
- 년 9 월 2018에서 시작 하는 "," [Office 365 ATP 경고 페이지](atp-safe-links-warning-pages.md) 기능 새 색 구성표를 "," 자세한 내용은 "및" 불구 하 고 사이트에 계속 하는 기능 제공 경고 및 권장 사항. 
         
## <a name="how-atp-safe-links-in-email-works"></a>전자 메일에 대 한 ATP 안전한 링크의 작동 방식

높은 수준의 같습니다 ATP 안전한 링크 보호 Url에 대 한 전자 메일 (Office 365를 하지 온-프레미스에 호스트)에서 작동 하는 방법.
  
1. 사용자는 Url이 들어 있는 전자 메일 메시지를 받습니다.
    
2. 모든 전자 메일 서명 기반 맬웨어 방지 IP 및 봉투를 필터링 하는 Exchange Online Protection을 통해 이동, 스팸 방지 및 맬웨어 방지 필터 적용 됩니다.
    
3. 전자 메일 사용자의 받은 편지함에 도착합니다.
    
4. 사용자는 Office 365에 로그인 하 고 자신의 전자 메일 받은 편지 함으로 이동 됩니다.
    
5. 사용자 전자 메일 메시지를 여는 하 고 전자 메일 메시지에서 URL에 대해 다음 클릭 합니다.
    
6. ATP 안전한 링크 기능 웹사이트를 열기 전에 URL을 확인 하는 즉시 합니다. 악의적인, 또는 안전 차단 URL은 식별 합니다.
    
1. URL 인 사용자에 게 적용 되는 정책에 대 한 [사용자 지정 "rewrite 수행" Url 목록](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) 에 포함 된 사이트를 참조 하는 경우 웹사이트를 엽니다. 
    
2. 조직의 [차단 된 사용자 지정 Url 목록](set-up-a-custom-blocked-urls-list-wtih-atp.md)에 포함 된 웹사이트에 URL이 있는 경우 [경고 페이지가](atp-safe-links-warning-pages.md) 열립니다. 
    
3. 악성 코드가 포함 될으로 확인 된 사이트로 URL이 있는 경우 [경고 페이지가](atp-safe-links-warning-pages.md) 열립니다. 
    
4. 다운로드 가능한 파일에 URL 이동 하는 경우 조직의 [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md) 은 이러한 콘텐츠를 검사 하도록 구성 된 다운로드 파일을 검사 합니다. 
    
5. URL을 안전한 것으로 확인 하는 경우 웹사이트를 엽니다.
    
## <a name="how-atp-safe-links-in-office-documents-works"></a>Office 문서에서 ATP 안전한 링크의 작동 방식

높은 수준의 같습니다 ATP 안전한 링크 보호 Url에 대 한 Office 365 ProPlus 응용 프로그램 (Word, Excel 및 PowerPoint Windows 또는 Mac, iOS 또는 Android 장치에서 Office 응용 프로그램에서 Windows에 Visio의 현재 버전)에서 작동 하는 방법.
  
1. 사람들이 자신의 컴퓨터, smartphone 또는 태블릿에 Office 365 ProPlus를 설치 했습니다.
    
2. 사용자는 Word, Excel, PowerPoint 또는 Visio를 열고 해당 작업이 나 교육용 계정을 사용 하 여 Office 365 엔터프라이즈에 로그인 합니다. 다음은 문서 Url이 들어 있습니다.
    
3. 사용자가 문서에 URL을 클릭 하면 ATP 안전한 링크 서비스에 대 한 링크를 검사 합니다.
    
  - URL 인 사용자에 게 적용 되는 정책에 대 한 [사용자 지정 "rewrite 수행" Url 목록](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) 에 포함 된 사이트를 참조 하는 경우 해당 사용자는 웹사이트에 가져옵니다. 
    
  - 조직의 [차단 된 사용자 지정 Url 목록](set-up-a-custom-blocked-urls-list-wtih-atp.md)에 포함 된 웹사이트에 URL이 있는 경우 [경고 페이지](atp-safe-links-warning-pages.md)로 이동 합니다.
    
  - 악성 코드가 포함 될으로 확인 된 사이트로 URL이 있는 경우 [경고 페이지](atp-safe-links-warning-pages.md)로 이동 합니다.
    
  - URL 다운로드 가능한 파일에 들어가고 [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md) 은 이러한 다운로드를 검색 하도록 구성 된 경우 다운로드 파일을 검사 합니다. 
    
  - URL은 안전한으로 간주 하는 경우 사용자 웹사이트를 가져옵니다.
    
## <a name="how-to-get-atp-safe-links-protection"></a>ATP 안전한 링크 보호 하는 방법

ATP 안전한 링크 기능에는 Office 365 Enterprise e 5에 포함 된 고급 위협 보호의 일부입니다. 조직의 다른 Office 365 Enterprise 등록을 사용 하는 경우 고급 위협 보호 추가 기능으로 구입할 수 있습니다. (전역 관리자도 Office 365 관리 센터에서 선택 **대금 청구** \> **추가 구독**.) 자세한 내용은 참조 [Office 365 플랫폼 서비스 설명: Office 365 보안 &amp; 준수 센터](https://technet.microsoft.com/en-us/library/dn933793.aspx) [구입 또는 비즈니스를 위한 Office 365에 대 한 추가 기능을 편집](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6)하 고 있습니다.
  
ATP 안전한 링크 기능은 다음 경우에 현재:
  
- Word, Excel, PowerPoint 및 Visio 문서 및 전자 메일에 대 한 **ATP 안전한 링크 정책을 설정** 합니다. ( [Office 365의 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)참조).
    
- 사용자의 작업이 나 교육용 계정을 사용 하 여 **사용자가 Office 365에 로그인 됩니다** . ( [Office 또는 Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426)참조).
    
- **Office 365에서 호스팅되는 조직의 전자 메일을**온-프레미스 서버에 없는 합니다. 
    
## <a name="make-sure-atp-safe-links-protection-is-in-place"></a>ATP 안전한 링크 보호 원본 위치에 있는지 확인

조직에 대 한 ATP 안전한 링크 보호가 작동 하는 방법을 보려면 하나 좋은 방법은 [고급 위협 보호에 대 한 보고서를 확인](view-reports-for-atp.md)하 여는 것입니다. 또한 전역 또는 보안 관리자 [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md)을 검토 해야 합니다. ATP 안전한 링크 정책은 또는 Office 문서에도에 전자 메일 메시지에 하이퍼링크를 보호 적용 되는지 여부를 결정 합니다.
  
다음 표에서 일부 예제 시나리오를 ATP 안전한 링크 보호 수도 있고 전체에서 되지 않을 수 있습니다. 모든이 경우에는 조직에는 고급 위협 보호를 포함 하는 Office 365 Enterprise E5 가정 합니다.
  
|**시나리오 예**|**ATP 안전한 링크 보호는이 경우에 적용 여부**|
|:-----|:-----|
|Jean에 Url을 전자 메일 및 Office 문서에서 다루는 ATP 안전한 링크 정책이 있는 그룹의 구성원입니다. Jean 프레젠테이션을 PowerPoint 2016에서 보낸 사람이 열고 프레젠테이션에서 URL을 클릭 합니다.  <br/> |예입니다. 정의 된는 ATP 안전한 링크 정책이 Jean의 그룹, Jean의 전자 메일 및 Jean 열리는 Jean 로그인을 Word, Excel, PowerPoint 또는 Visio 문서 및 Windows, iOS, 또는 Android 장치에서 Office 365 ProPlus를 사용 하 여 적용 됩니다.  <br/> |
|Chris의 조직, 더 전역 또는 보안 관리자에서 모든 ATP 안전한 링크 정책을 아직 정의 했습니다. Chris 악성 웹사이트에 대 한 URL을 포함 하는 전자 메일을 받습니다. Chris 인식 하지 않으며 URL은 악의적인 및 링크를 클릭 합니다.  <br/> |아니요. 원본 위치에 있는 것으로 보호 하기 위해에서 조직의 모든 사용자에 대 한 Url을 적용 하는 기본 정책 정의 되어야 합니다.  <br/> |
|Pat의 조직, 더 전역 또는 보안 관리자가 정의 했거나 아직 모든 ATP 안전한 링크 정책을 편집 합니다. Pat은 Word 문서를 열리고 파일의 URL을 클릭 합니다.  <br/> |원본 위치에 있는 것으로 보호 하기 위해에서 Office 문서를 포함 하는 아니요 A 정책 정의 되어야 합니다. [Office 365의 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)참조 하십시오.<br/> |
|백화점 ㈜의 조직에 포함 된 ATP 안전한 링크 정책이 `http://tailspintoys.com` 차단 된 웹사이트도 나열 합니다. Lee에 대 한 URL을 포함 하는 전자 메일 메시지를 수신 `http://tailspintoys.com/aboutus/trythispage`합니다. Lee가 URL을 클릭 합니다.<br/> |전체 사이트와 그 하위의 목록에 포함 된 모든 Url을 차단 여부에 따라 다릅니다. [ATP 안전 링크를 사용 하 여 차단 된 Url 목록 사용자 지정 설정](set-up-a-custom-blocked-urls-list-wtih-atp.md)을 참조 하십시오.<br/> |
|김 Jean의 동료, 전자 메일을 보내 Jean, 악성 URL이 전자 메일에 포함 된 정확히 모르는 합니다.  <br/> |ATP 안전한 링크 정책을 조직 내에서 보낸 전자 메일에 대해 정의 되는 여부에 따라 다릅니다. [Office 365의 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)참조 하십시오.<br/> |
   
## <a name="related-topics"></a>관련 항목
<a name="howtosee"> </a>

[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Office 365의 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)
  
[Office 365의에서 ATP 안전 하 게 보호 첨부 파일](atp-safe-attachments.md)
  
[Office 365의 ATP 피싱 방지 기능](atp-anti-phishing.md)
  
[고급 위협 보호에 대 한 보고서 보기](view-reports-for-atp.md)
  

