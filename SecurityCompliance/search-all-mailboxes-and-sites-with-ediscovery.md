---
title: eDiscovery 센터를 사용하여 모든 사서함 및 사이트 검색
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 56e2978f-71b6-4141-b769-ad856d31bbec
description: Office 365에서 eDiscovery 센터를 단일 eDiscovery 검색에서 비즈니스 사이트에 대 한 모든 Exchange Online 사서함, SharePoint Online 사이트 및 OneDrive을 검색할 수 있습니다. 조직에서 모든 콘텐츠 원본을 검색 하려면 eDiscovery 관리자 각 콘텐츠 원본에 대 한 적절 한 eDiscovery 권한은 할당 받아야 합니다.
ms.openlocfilehash: b3508d5929ca2b5b7a937eb2dccf677a2968cbbc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533339"
---
# <a name="search-all-mailboxes-and-sites-using-the-ediscovery-center"></a>eDiscovery 센터를 사용하여 모든 사서함 및 사이트 검색

Office 365에서 eDiscovery 센터를 단일 eDiscovery 검색에서 비즈니스 사이트에 대 한 모든 Exchange Online 사서함, SharePoint Online 사이트 및 OneDrive을 검색할 수 있습니다. 조직에서 모든 콘텐츠 원본을 검색 하려면 eDiscovery 관리자 각 콘텐츠 원본에 대 한 적절 한 eDiscovery 권한은 할당 받아야 합니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- eDiscovery 관리자에게는 콘텐츠 원본을 검색하기 위한 적절한 권한이 할당되어야 합니다. 사서함 및 사이트에 eDiscovery 사용 권한을 할당하는 방법에 대한 자세한 내용은 다음을 참조하세요. 
    
  - [검색 관리 역할 그룹의 구성원에 게 Exchange 설치를 통해 만들어진 검색 사서함에 대 한 전체 액세스 사서함 권한이 합니다.](https://go.microsoft.com/fwlink/p/?LinkId=526886)
    
  - [SharePoint Online에서 eDiscovery 권한 할당](https://go.microsoft.com/fwlink/p/?LinkId=526885)
    
  - [비즈니스용 OneDrive 사이트에 eDiscovery 사용 권한 할당](assign-permissions-to-onedrive-for-business-sites.md)
    
- 최대 10, 000 사서함 및 비즈니스 사이트에 대 한 SharePoint Online 및 OneDrive 무제한 단일 eDiscovery 검색 쿼리에서 검색할 수 있습니다. 그러나 검색 하려면 특정 사이트를 지정 하는 경우의 제한은 사이트 수가 100입니다.
    
- 모든 사서함 및 사이트를 검색 하는 경우의 결과 볼 때 제한의 설명에 대 한 [자세한 내용](search-all-mailboxes-and-sites-with-ediscovery.md#moreinfo) 은 섹션을 참조 하십시오. 
    
- EDiscovery 센터에서 검색 쿼리 만들기 (영문) 하는 방법에 대 한 자세한 내용은 [만들기 및 실행된 eDiscovery 쿼리를](https://go.microsoft.com/fwlink/p/?LinkID=404032)참조 하십시오.
    
## <a name="search-all-locations"></a>모든 위치 검색

1. eDiscovery 센터에서 검색 쿼리를 실행하려는 eDiscovery 사례를 엽니다.
    
2. **검색 및 내보내기**, 아래에서 기존 쿼리를 클릭 하거나 새 검색 쿼리를 만들려면 **새 항목** 클릭 합니다. 
    
3. 검색 쿼리 페이지의 **원본** 섹션에서 **쿼리 범위 수정**을 클릭합니다.
    
4. **쿼리 범위 수정** 페이지에서 **모든 항목 검색**을 클릭한 후 검색할 콘텐츠 위치를 선택합니다.
    
  - 모든 사서함을 검색할 수 있는 **Exchange** 를 선택 합니다. 
    
  - **SharePoint** 비즈니스 사이트에 대 한 모든 SharePoint Online 및 OneDrive를 검색 하려면 선택 합니다. 
    
  - 조직에서 모든 콘텐츠 위치를 검색 하려면 **Exchange** 및 **SharePoint** 모두를 선택 합니다. 
    
![모든 사서함 및 사이트 검색](media/e1f919ab-5596-43bb-a3c9-626cd41067b3.gif)
  
5. **확인**을 클릭하여 변경 내용을 저장합니다. 
    
6. 검색 쿼리 페이지에서 키워드 쿼리, 날짜 범위 또는 검색할 특정 유형의 콘텐츠 범위 좁히기 등과 같은 기타 정보를 완성하거나 수정합니다. 쿼리를 실행할 준비가 되면 **검색**을 클릭합니다. 
    
## <a name="more-information"></a>추가 정보
<a name="moreinfo"> </a>

- 최근 결과를 포함하는 상위 500개 사서함 및 상위 500개 사이트는 **쿼리** 페이지의 **원본**에 표시됩니다. 
    
- 모든 콘텐츠 원본에 포함된 총 항목 수와 전체 크기는 **쿼리** 페이지의 **원본**에 표시됩니다. 
 
    
- Exchange 사서함 또는 **쿼리** 페이지의 SharePoint 사이트에서 가장 최근의 200개 검색 결과를 미리 볼 수 있습니다. 
    
    다음 스크린 샷에는 모든 사서함 및 사이트를 검색할 때 **쿼리** 페이지에 표시되는 검색 결과의 예를 보여 줍니다. 
    
    ![모든 위치를 검색할 때의 결과 스크린 샷](media/4bf430f6-41ab-4bf6-afa9-33c3f6fd8b16.gif)
  

