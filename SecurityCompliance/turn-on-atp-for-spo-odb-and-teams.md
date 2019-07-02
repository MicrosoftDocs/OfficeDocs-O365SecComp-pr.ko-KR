---
title: SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP 실행
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: ITPro
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
ms.collection:
- M365-security-compliance
description: 검색 된 파일에 대 한 알림을 설정 하는 방법을 포함 하 여 SharePoint, OneDrive 및 팀에 대 한 ATP를 설정 하는 방법을 알아봅니다.
ms.openlocfilehash: f3be5b3cf73a04de10185428b84b5862906c3db7
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34652671"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP 실행

> [!IMPORTANT]
> 이 문서는 [Office 365 Advanced Threat Protection](office-365-atp.md)을 사용 하는 비즈니스 고객을 위한 것입니다. Outlook의 안전한 링크에 대 한 정보를 검색 하는 개인 사용자는 [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2)를 참조 하십시오.

[Office 365 ATP For SharePoint, OneDrive 및 Microsoft 팀은](atp-for-spo-odb-and-teams.md) 악의적인 파일을 실수로 공유 하지 않도록 조직을 보호 합니다. 악성 파일이 검색 되 면 해당 파일이 차단 되므로 조직의 보안 팀이 추가 작업을 수행할 때까지 아무도 해당 파일을 열거나 복사 하거나 이동 하거나 공유할 수 없습니다. 이 문서를 읽으면 SharePoint, OneDrive 및 팀에 대 한 ATP를 켜고, 검색 된 파일에 대 한 알림을 받을 알림을 설정 하 고, 다음 단계를 수행 합니다. 
  
ATP 정책을 정의 하거나 편집 하려면 적절 한 역할이 할당 되어 있어야 합니다. 다음 표에서는 몇 가지 예를 설명 합니다.

|역할  |할당 된 위치/방법  |
|---------|---------|
|Office 365 전역 관리자 |Office 365을 구매 하기 위해 등록 하는 사람은 기본적으로 전역 관리자입니다. 자세한 내용은 [Office 365 관리자 역할 정보](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 를 참조 하세요.         |
|보안 관리자 |Azure Active Directory 관리 센터 ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Exchange Online 조직 관리 |Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>또는 <br>  PowerShell cmdlet ( [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조) |
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>SharePoint, OneDrive 및 Microsoft Teams에 대한 ATP 켜기

**이 절차를 시작 하기 전에 Office 365 환경에 대해 감사 로깅이 이미 설정 되어 있는지 확인**합니다. 이 작업은 일반적으로 Exchange Online에서 감사 로그 역할이 할당 된 사용자가 수행 합니다. 자세한 내용은 [Turn Office 365 감사 로그 검색 켜기 또는 끄기를](turn-audit-log-search-on-or-off.md)참조 하세요.
  
1. [https://protection.office.com](https://protection.office.com)으로 이동 하 여 회사 또는 학교 계정으로 로그인 합니다.
    
2. Office 365 보안 &amp; 및 준수 센터의 왼쪽 탐색 창에 있는 **위협 관리**에서 **정책** \> **안전한 첨부 파일**을 선택 합니다. <br/>![보안 &amp; 및 준수 센터에서 위협 관리 \> 정책을 선택 합니다.](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)
  
3. **SharePoint, OneDrive 및 Microsoft 팀에 대해 ATP 사용**을 선택 합니다.<br/>![SharePoint Online, 비즈니스용 OneDrive 및 Microsoft 팀에 대 한 Advanced Threat Protection 설정](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)
  
4. **저장**을 클릭합니다.
    
5. 조직의 [안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md) 및 [안전한 링크 정책을](set-up-atp-safe-links-policies.md)검토 하 고 적절 하 게 편집 합니다.
    
6. 는 전역 관리자 또는 SharePoint Online 관리자는 **DisallowInfectedFileDownload** 매개 변수를 *true*로 설정 하 여 **[set-spotenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet을 실행 합니다. <br/>
      - 이 매개 변수를 *true* 로 설정 하면 검색 된 파일에 대 한 모든 작업 (삭제 제외)이 차단 됩니다. 사용자가 검색 된 파일을 열거나, 이동 하거나, 복사 하거나, 공유할 수 없습니다.
      - 이 매개 변수를 *false* 로 설정 하면 삭제 및 다운로드를 제외한 모든 작업이 차단 됩니다. 사용자는 위험을 수락 하 고 검색 된 파일을 다운로드할 수 있습니다.  
   
7. 변경 내용이 모든 Office 365 데이터 센터에 전파 되는 데 최대 30 분 정도 걸릴 수 있습니다.
    
8. 는 검색 된 파일에 대 한 알림 설정으로 이동 합니다.
    
Office 365에서 PowerShell을 사용 하는 방법에 대 한 자세한 내용은 PowerShell을 사용 하 [여 office 365 관리](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell)를 참조 하세요. 

파일이 악성으로 검색 되었을 때의 사용자 환경에 대 한 자세한 내용은 [SharePoint Online, OneDrive 또는 Microsoft 팀에서 악의적인 파일을 찾은 경우 수행할](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)작업을 참조 하십시오. 
  
## <a name="set-up-alerts-for-detected-files"></a>검색 된 파일에 대 한 알림 설정

SharePoint Online의 파일 (비즈니스용 OneDrive 또는 Microsoft 팀)이 악성으로 식별 된 경우 알림을 받으려면 알림을 설정 하면 됩니다.
  
1. [Office 365 보안 &amp; 및 준수 센터](https://protection.office.com)에서 **경고** \> **관리 알림을**선택 합니다.
    
2. **새 경고 정책을**선택 합니다.
    
3. 알림의 이름을 지정 합니다. 예를 들어 라이브러리에 유해한 파일을 입력할 수 있습니다.
    
4. 경고에 대 한 설명을 입력 합니다. 예를 들어 SharePoint Online, OneDrive 또는 Microsoft 팀에서 악성 파일이 검색 되 면 관리자에 게 알림 메시지를 입력할 수 있습니다.
    
5. **알림 보내기** 위치 섹션에서 다음을 수행 합니다. 
    
    위한. **작업** 목록에서 **검색 된 맬웨어를 파일에서**선택 합니다.
    
    b. **Users** 필드는 비워 둡니다. 
    
6. **이 알림 보내기** ... 섹션에서 악의적인 파일이 검색 되 면 알림을 받을 전역 관리자, 보안 관리자 또는 보안 판독기를 하나 이상 선택 합니다. 
    
7. **저장**을 클릭합니다.
    
경고에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 활동 경고 만들기](create-activity-alerts.md)를 참조 하십시오. 
  
## <a name="next-steps"></a>다음 단계

1. [SharePoint, OneDrive 또는 Microsoft Teams에서 감지한 악성 파일에 대한 정보 보기](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [Office 365에서 격리 된 메시지 및 파일을 관리자 권한으로 관리](manage-quarantined-messages-and-files.md)
    

  

