---
title: SharePoint, OneDrive, 또는 팀이 Microsoft에서 감지 된 악의적인 파일에 대 한 정보 보기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
description: SharePoint, OneDrive, 또는 팀에서 감지 된 악의적인 파일에 대 한 정보를 보려면 이동할 위치를 하 고 해당 파일에서 작업을 수행 하는 방법에 알아봅니다.
ms.openlocfilehash: ba1dc3551e66800213a9cb988ebe9fc5e03e31f2
ms.sourcegitcommit: 147768bbe44c8c98c02fa29ae9d882cee4ec2d6b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/09/2018
ms.locfileid: "26238510"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a>SharePoint, OneDrive, 또는 팀이 Microsoft에서 감지 된 악의적인 파일에 대 한 정보 보기

문서 라이브러리 및 팀 사이트의 악의적인 파일을 통해 조직을 보호 하는 [SharePoint, OneDrive 및 팀이 Microsoft office 365 ATP](atp-for-spo-odb-and-teams.md) 입니다. 악의적인 파일 감지 되 면 해당 파일 열기, 복사, 이동 또는 조직의 보안 팀에 의해 추가 조치가 때까지 공유할 수 있는 아무도 있도록 차단 됩니다. 검색 된 파일에 대 한 정보를 확인 하는 방법 및 수행할 동작을 자세히 알아보려면이 문서를 읽어보십시오. 

이 문서에서 설명 하는 작업을 수행 하기 위해 필요한 있어야 [Office 365 보안에 할당 된 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다. 
  
## <a name="view-reports-with-information-about-detected-files"></a>검색 된 파일에 대 한 정보가 포함 된 보고서 보기

상태 및 Office 365 ATP 하 여 검색 된 파일에 대 한 자세한 정보를 보려면 위협 보호 상태 보고서를 사용할 수 있습니다.
  
1. Office 365 보안에서 &amp; 준수 센터 **보고서** 선택 \> **대시보드** \> **위협 보호 상태**입니다.
    
2. 다음은 보고서의 오른쪽 위 모서리에서 **보기 세부 정보 테이블**을 선택 합니다.
    
3. 다음은 보고서에서 검색 된 파일의 목록을 봅니다.
    
4. 자세한 내용은 다음을 수행 하는 작업을 포함 하 여, 파일 이름, 파일 경로 등을 보려면 목록에서 항목을 선택 합니다.
    
5. 같은 관찰 된 동작 및 분석 세부 정보를 보려면 **고급 분석** 탭을 선택 합니다. 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a>격리에서 파일에 대해 조치를 취할 및 보기

1. Office 365 보안에서 &amp; 준수 센터 **위협 관리** 를 선택 \> **검토** \> **격리**합니다.
    
2. 왼쪽된 위 모서리에서 필터 **전자 메일** 에서 **콘텐츠**를 변경 합니다.
    
3. 파일의 URL을 포함 하 여 자세한 정보를 보려면 목록에서 항목을 선택 합니다.
    
4. 사용 가능한 동작을 선택 합니다.
    
  - 선택 **릴리스 &amp; 보고서** 파일 차단을 해제 해야 합니다. 
    
    파일을 Microsoft에 가양성으로 보고를 **Microsoft에 보고서 보내기** 를 선택 합니다. 
    
  - **파일을 다운로드** 하 여 파일을 추가 조사를 선택 합니다. 
    
  - 격리 된 항목의 목록에서 파일을 제거 하려면 **삭제** 를 선택 합니다. 이 옵션을 선택 하는 경우 비즈니스, 또는 Microsoft 팀의 SharePoint Online, OneDrive에서 해당 라이브러리에서 파일을도 삭제 해야 있습니다. 이 옵션 못 파일 차단을 해제 하지 열거나 공유 합니다. 
    
5. 선택한 항목에 대 한 세부 정보를 닫으려면 **닫기** 를 선택 합니다. 
  
  

