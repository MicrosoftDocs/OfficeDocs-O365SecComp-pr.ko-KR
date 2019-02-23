---
title: SharePoint Online의 바이러스 검색
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 01/14/2019
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
description: Office 365은 사용자가 SharePoint Online에 업로드 하는 파일에서 바이러스를 검색 하 여 맬웨어 로부터 환경을 보호 하는 데 도움이 됩니다. 업로드 후 파일에서 바이러스를 검사 합니다. 파일이 감염 된 것으로 확인 되 면 사용자가 파일을 다운로드 하거나 동기화 할 수 없도록 속성이 설정 됩니다.
ms.openlocfilehash: d39a5be525e25de8206e8d4219d9c83bfa6eaae0
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212968"
---
# <a name="virus-detection-in-sharepoint-online"></a>SharePoint Online의 바이러스 검색

Office 365은 사용자가 SharePoint Online에 업로드 하는 파일에서 바이러스를 검색 하 여 맬웨어 로부터 환경을 보호 하는 데 도움이 됩니다. 업로드 후 파일에서 바이러스를 검사 합니다. 파일이 감염 된 것으로 확인 되 면 사용자가 파일을 다운로드 하거나 동기화 할 수 없도록 속성이 설정 됩니다.
  
> [!IMPORTANT]
> SharePoint Online의 이러한 바이러스 백신 기능은 바이러스를 포함 하는 방법입니다. 사용자 환경에 대 한 맬웨어를 방어 하기 위한 단일 방어선이 아닙니다. 모든 고객은 다양 한 계층에서 맬웨어 방지 보호 기능을 평가 및 구현 하 고 엔터프라이즈 인프라를 보호 하기 위한 모범 사례를 적용할 것을 권장 합니다. 전략 및 모범 사례에 대 한 자세한 내용은 [Office 365에 대 한 보안 모범 사례](security-best-practices.md)를 참조 하세요. 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a>감염 된 파일을 SharePoint Online에 업로드 한 경우 어떻게 되나요?

Office 365에서는 일반적인 바이러스 검색 엔진을 사용 합니다. 엔진이 SharePoint Online 내에서 비동기적으로 실행 되며 업로드 된 후 파일을 검사 합니다. 바이러스를 포함 하는 파일을 찾으면 다시 다운로드할 수 없도록 플래그가 지정 됩니다. 2018 년 4 월에는 검색 된 파일에 대 한 250mb 제한이 제거 되었습니다.
  
수행 되는 작업은 다음과 같습니다.
  
1. 사용자가 파일을 SharePoint Online에 업로드 합니다.
    
2. 바이러스 검색 엔진이 파일을 검사 합니다.
    
3. 바이러스가 발견 되 면 바이러스 엔진은 파일에서 감염 되었음을 나타내는 속성을 설정 합니다.
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a>사용자가 브라우저를 사용 하 여 감염 된 파일을 다운로드 하려고 하면 어떻게 되나요?

파일이 바이러스에 감염 된 경우 사용자는 브라우저를 사용 하 여 SharePoint Online에서 파일을 다운로드할 수 없습니다.
  
수행 되는 작업은 다음과 같습니다.
  
1. 사용자가 웹 브라우저를 열고 SharePoint Online에서 감염 된 파일을 다운로드 하려고 합니다.
    
2. 사용자에 게 바이러스가 감지 되었음을 알리는 경고가 표시 됩니다. 사용자에 게 파일을 다운로드 하 고 자체 바이러스 백신 소프트웨어를 사용 하 여 복구를 시도할 수 있는 옵션이 제공 됩니다.

> [!NOTE]
> **DisallowInfectedFileDownload** 매개 변수와 함께 set-spotenant cmdlet을 사용 하 여 바이러스 백신 경고 창 에서도 검색 된 파일을 다운로드할 수 없습니다. [DisallowInfectedFileDownload] (https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant)를 참조 하세요.
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a>OneDrive 동기화 클라이언트가 감염 된 파일을 동기화 하려고 할 때 수행 되는 작업

사용자가 새 onedrive 동기화 클라이언트 (excel.exe) 또는 이전 비즈니스용 onedrive 동기화 클라이언트 (Groove)를 사용 하 여 파일을 동기화 하는지 여부에 관계 없이 파일에 바이러스가 포함 되어 있으면 동기화 클라이언트에서 다운로드 하지 않습니다. 동기화 클라이언트에서는 파일을 동기화 할 수 없다는 알림을 표시 합니다.
  

