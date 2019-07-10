---
title: Office 365 ATP 안전한 링크가 작동 하는 방식
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: Admin
ms.date: 05/19/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 안전한 링크 기능은 Office 문서 및 전자 메일 메시지에서 하이퍼링크를 클릭 하 여 확인할 시간을 제공 합니다. 이 문서를 읽으면 ATP 안전한 링크가 작동 하는 방식을 확인할 수 있습니다.
ms.openlocfilehash: 7570fd65a9831a6436eec8c402a2bc0c2ae09b40
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599184"
---
# <a name="how-office-365-atp-safe-links-works"></a>Office 365 ATP 안전한 링크가 작동 하는 방식
         
## <a name="how-atp-safe-links-works-with-urls-in-email"></a>ATP 안전한 링크가 전자 메일의 Url과 함께 작동 하는 방식

높은 수준에서 [ATP 안전한 링크](atp-safe-links.md) 보호는 전자 메일의 url 365 (온-프레미스 아님)에 따라 어떻게 작동 하는지 설명 합니다.
  
1. 사용자가 전자 메일 메시지를 받고, 그 중 일부는 Url을 포함 합니다.
    
2. 모든 전자 메일은 Exchange Online Protection을 통해 진행 되며, 인터넷 프로토콜 (IP) 및 봉투 필터, 서명 기반 맬웨어 방지, 스팸 방지 및 맬웨어 방지 필터가 적용 됩니다. 
    
3. 전자 메일이 사용자의 받은 편지함에 도착 합니다.
    
4. 사용자가 Office 365에 로그인 하 고 해당 전자 메일 받은 편지 함으로 이동 합니다.
    
5. 사용자가 전자 메일 메시지를 열고 전자 메일 메시지의 URL을 클릭 합니다.
    
6. ATP 안전한 링크 기능은 웹 사이트를 열기 전에 URL을 즉시 확인 합니다. URL이 차단, 악의적 또는 안전한 것으로 식별 됩니다.
    
    - 사용자에 게 적용 되는 정책에 대 한 [사용자 지정 "다시 쓰지 않음" url 목록](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) 에 포함 된 웹 사이트에 URL을 사용 하는 경우에는 웹 사이트가 열립니다. 
    
    - 조직의 [사용자 지정 차단 된 url 목록](set-up-a-custom-blocked-urls-list-wtih-atp.md)에 포함 된 웹 사이트에 대 한 URL 인 경우 [경고 페이지가](atp-safe-links-warning-pages.md) 열립니다. 
    
    - URL이 악성으로 확인 된 웹 사이트에 대 한 것 이면 [경고 페이지가](atp-safe-links-warning-pages.md) 열립니다. 
    
    - URL이 다운로드 가능한 파일로 이동 하 고 조직의 [ATP 안전한 링크 정책이](set-up-atp-safe-links-policies.md) 이러한 콘텐츠를 검색 하도록 구성 된 경우 다운로드 가능한 파일이 검사 됩니다. 
    
    - URL이 안전한 것으로 확인 되 면 웹 사이트가 열립니다.
    
## <a name="how-atp-safe-links-works-with-urls-in-office-documents"></a>ATP 안전한 링크가 Office 문서의 Url과 작동 하는 방식

높은 수준에서 [ATP 안전한 링크](atp-safe-links.md) 보호는 Office 365 ProPlus 응용 프로그램 (Windows 또는 Mac의 최신 버전의 Word, Excel 및 PowerPoint, IOS 또는 Android 장치의 office 앱, Windows의 Visio, OneNote Online 및 office)의 url에 대해 작동 합니다. 온라인):
  
1. 사용자가 컴퓨터, 스마트폰 또는 태블릿에서 Office 365 ProPlus를 설치 했습니다. 브라우저에서 Office Online을 사용 하 고 있습니다.
    
2. 사용자가 회사 또는 학교 계정을 사용 하 여 Word, Excel, PowerPoint 또는 Visio를 열고 Office 365 Enterprise에 로그인 합니다. 문서에 Url이 포함 되어 있습니다.
    
3. 사용자가 문서에서 URL을 클릭 하면 해당 링크는 ATP Safe Links service에 의해 확인 됩니다.
    
      - 사용자에 게 적용 되는 정책에 대 한 사용자 [지정 "다시 쓰지 않음" url 목록](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) 에 포함 된 웹 사이트에 대 한 url 인 경우 해당 사용자는 웹 사이트로 이동 됩니다. 
    
      - 조직의 [사용자 지정 차단 된 url 목록](set-up-a-custom-blocked-urls-list-wtih-atp.md)에 포함 된 웹 사이트에 대 한 URL 인 경우 사용자는 [경고 페이지로](atp-safe-links-warning-pages.md)이동 됩니다.
    
      - URL이 악성으로 확인 된 웹 사이트에 대 한 것 인 경우 사용자는 [경고 페이지로](atp-safe-links-warning-pages.md)이동 됩니다.
    
      - URL이 다운로드 가능한 파일로 이동 하 고 [ATP Safe Links 정책이](set-up-atp-safe-links-policies.md) 이러한 다운로드를 검색 하도록 구성 된 경우 다운로드 가능한 파일이 검사 됩니다. 
    
      - URL이 안전한 것으로 간주 되 면 사용자는 웹 사이트로 이동 됩니다.

