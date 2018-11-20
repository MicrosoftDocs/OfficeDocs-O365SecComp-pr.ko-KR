---
title: SharePoint, OneDrive 및 팀이 Microsoft Office 365 ATP 설정
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
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
description: SharePoint, OneDrive 및 검색 된 파일에 대 한 알림을 설정 하는 방법을 포함 하 여 팀에 대 한 ATP를 설정 하는 방법에 알아봅니다.
ms.openlocfilehash: d70c574f002ca7e70ab6f9a4abad3ea5ef21a20f
ms.sourcegitcommit: 147768bbe44c8c98c02fa29ae9d882cee4ec2d6b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/09/2018
ms.locfileid: "26238420"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>SharePoint, OneDrive 및 팀이 Microsoft Office 365 ATP 설정

[SharePoint, OneDrive 및 팀이 Microsoft office 365 ATP](atp-for-spo-odb-and-teams.md) 실수로 악의적인 파일 공유에서 조직을 보호 합니다. 악의적인 파일 감지 되 면 해당 파일 열기, 복사, 이동 또는 조직의 보안 팀에 의해 추가 조치가 때까지 공유할 수 있는 아무도 있도록 차단 됩니다. SharePoint에 대 한 ATP를 설정 하는이 문서를 읽기, OneDrive 및 팀 검색 된 파일에 대 한 알림을 받으려면 경고를 설정 하 고에서는 다음 단계를 수행 합니다. 
  
이 문서에서 설명 하는 작업을 수행 하기 위해 필요한 사용 권한을 보안 및 Office 365에 할당 된 있어야 &amp; 준수 센터입니다.
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>SharePoint, OneDrive 및 Microsoft Teams에 대한 ATP 켜기

 **이 절차를 시작 하기 전에 Office 365 환경에 대 한 감사 로깅이 이미 설정 되어있는지 확인**하십시오. 이 Exchange Online 할당 된 감사 로그 역할을 가진 사용자가 일반적으로 수행 됩니다. 자세한 내용은 [Office 365 설정 또는 해제 로그 검색 감사](turn-audit-log-search-on-or-off.md)를 참조 하십시오.
  
1. 전역 관리자 또는 보안 관리자로 이동 [https://protection.office.com](https://protection.office.com)와 작업이 나 교육용 계정 사용 하 여 로그인 합니다.
    
2. Office 365 보안에서 &amp; 준수 센터 왼쪽된 탐색 창의 **위협 관리** **정책** 을 선택 \> **안전한 첨부 파일**입니다. <br/>![보안에서 &amp; 준수 센터 위협 관리를 선택 \> 정책](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)
  
3. **SharePoint, OneDrive 및 Microsoft 팀의 ATP 설정**을 선택 합니다.<br/>![온라인으로 비즈니스용 OneDrive, Microsoft 팀의 SharePoint에 대 한 고급 위협 보호 설정](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)
  
4. **저장**을 클릭합니다.
    
5. 검토 (하 고 적절 하 게 편집) 조직의 [안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md) 및 [안전 링크 정책](set-up-atp-safe-links-policies.md).
    
6. (권장) 전역 관리자 또는 SharePoint Online 관리자가 *true*로 설정 하는 **DisallowInfectedFileDownload** 매개 변수와 함께 **[Set-spotenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet을 실행 합니다. <br/>
  - 파일을 검색 매개 변수를 *true로* 블록 (삭제)을 제외한 모든 작업에 대 한 설정 합니다. 사용자 수는 없습니다 열, 이동, 복사 또는 검색 된 파일을 공유 합니다.
  - 삭제 및 다운로드를 제외 하 고 모든 작업을 차단 매개 변수를 *false로* 설정 합니다. 사용자는 위험을 수용 하 고 발견 된 파일을 다운로드 하도록 선택할 수 있습니다.  
   
7. 모든 Office 365 데이터 센터에 분산 하 여 변경 내용 최대 30 분까지를 허용 합니다.
    
8. (권장) 검색 된 파일에 대 한 알림을 설정으로 이동 합니다.
    
PowerShell을 사용 하 여 Office 365를 사용 하는 방법에 대 한 자세한 내용은, [PowerShell 사용 하 여 Office 365 관리](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell)를 참조 하십시오. > 자세히 알아보려면 사용자 환경에 대 한 악의적인으로 파일에서 발견 하는 경우, [악의적인 파일을 SharePoint Online, OneDrive, 또는 팀이 Microsoft에서 발견 되 면 수행할 작업을](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)참조 합니다. 
  
## <a name="set-up-alerts-for-detected-files"></a>검색 된 파일에 대 한 알림 설정

회사 또는 팀이 Microsoft에 대 한 SharePoint Online, OneDrive에서 파일을 악의적으로 식별 된 때 알림을 받으려면, 알림을 설정할 수 있습니다.
  
1. Office 365 보안에서 &amp; 준수 센터 **알림** 을 선택 \> **알림을 관리**합니다.
    
2. **새 경고 정책**을 선택 합니다.
    
3. 경고에 대 한 이름을 지정 합니다. 예, 라이브러리의 악의적인 파일을 입력할 수 있습니다.
    
4. 경고에 대 한 설명을 입력 합니다. 예, SharePoint Online, OneDrive, 또는 Microsoft 팀의 악의적인 파일을 감지 되 면 관리자에 게 알리는 입력할 수 있습니다.
    
5. **... 때이 경고 보내기** 섹션에서 다음을 수행 합니다. 
    
  - **작업** 목록에서 **파일에 감지 맬웨어**를 선택 합니다.
    
  - **사용자가** 필드를 비워두십시오. 
    
6. **이 경고를 보내기...** 섹션에서 하나 이상의 전역 관리자, 보안 관리자 또는 악의적인 파일을 감지 하는 경우 알림을 받을 보안 독자를 선택 합니다. 
    
7. **저장**을 클릭합니다.
    
경고에 대 한 자세한 내용은 참조 하십시오. [Office 365 보안에서 활동 알림을 만들 &amp; 준수 센터](create-activity-alerts.md)합니다. 
  
## <a name="next-steps"></a>다음 단계

1. [SharePoint, OneDrive, 또는 팀이 Microsoft에서 감지 된 악의적인 파일에 대 한 정보 보기](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [Office 365에서 관리자 권한으로 격리 된 메시지와 파일을 관리 합니다.](manage-quarantined-messages-and-files.md)
    

  

