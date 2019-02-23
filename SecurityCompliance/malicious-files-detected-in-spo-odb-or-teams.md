---
title: SharePoint, OneDrive 또는 Microsoft Teams에서 감지한 악성 파일에 대한 정보 보기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
description: SharePoint, OneDrive 또는 팀에서 검색 된 악성 파일에 대 한 정보를 볼 수 있는 위치 및 해당 파일에 대해 작업을 수행 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 6f44cd82241b4cd883fbd80e1b1dc2ea115e10af
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219568"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a>SharePoint, OneDrive 또는 Microsoft Teams에서 감지한 악성 파일에 대한 정보 보기

[SharePoint, OneDrive 및 Microsoft 팀에서는 Office 365 ATP](atp-for-spo-odb-and-teams.md) 가 문서 라이브러리 및 팀 사이트의 악의적인 파일 로부터 조직을 보호 합니다. 악성 파일이 검색 되 면 해당 파일이 차단 되므로 조직의 보안 팀이 추가 작업을 수행할 때까지 아무도 해당 파일을 열거나 복사 하거나 이동 하거나 공유할 수 없습니다. 검색 된 파일에 대 한 정보 및 수행할 작업을 확인 하는 방법에 대 한 자세한 내용은이 문서를 참조 하세요. 

이 문서에서 설명 하는 작업을 수행 하려면 [Office 365 보안 &amp; 및 준수 센터에 필요한 권한이](permissions-in-the-security-and-compliance-center.md)있어야 합니다. 
  
## <a name="view-reports-with-information-about-detected-files"></a>검색 된 파일에 대 한 정보가 있는 보고서 보기

Office 365 ATP가 검색 한 파일에 대 한 상태 및 자세한 정보를 보려면 위협 방지 상태 보고서를 사용할 수 있습니다.
  
1. [Office 365 보안 &amp; 및 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드** \> **위협 보호 상태**를 선택 합니다.
    
2. 보고서의 오른쪽 위 모서리에서 **정보 테이블 보기**를 선택 합니다.
    
3. 보고서에서 검색 된 파일의 목록을 확인 합니다.
    
4. 수행 된 작업, 파일 이름, 파일 경로 등 자세한 정보를 보려면 목록에서 항목을 선택 합니다.
    
5. **고급 분석** 탭을 선택 하 여 관찰 된 동작 및 분석 세부 정보 등의 정보를 확인 합니다. 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a>격리에서 파일 보기 및 작업 수행

1. Office 365 보안 &amp; 및 준수 센터에서 **위협 관리** \> **검토** \> **격리**를 선택 합니다.
    
2. 왼쪽 위 모서리에서 **전자 메일** 에서 **콘텐트로**필터를 변경 합니다.
    
3. 파일의 URL을 포함 하 여 세부 정보를 보려면 목록에서 항목을 선택 합니다.
    
4. 사용 가능한 작업을 선택 합니다.
    
  - 파일 차단을 해제 하려면 **릴리스 &amp; 보고서** 를 선택 합니다. 
    
    microsoft **에 보고서 보내기를** 선택 하 여 파일을 가양성으로 microsoft에 보고 합니다. 
    
  - 파일 **다운로드** 를 선택 하 여 파일을 더 조사 합니다. 
    
  - **삭제** 를 선택 하 여 격리 된 항목 목록에서 파일을 제거 합니다. 이 옵션을 선택 하는 경우 SharePoint Online, 비즈니스용 OneDrive 또는 Microsoft 팀의 각 라이브러리 에서도 해당 파일을 삭제 해야 합니다. 이 옵션을 선택 해도 파일이 열리거나 공유 되지 않도록 차단 해제 되지 않습니다. 
    
5. **닫기를** 선택 하 여 선택한 항목에 대 한 세부 정보를 닫습니다. 
  
  

