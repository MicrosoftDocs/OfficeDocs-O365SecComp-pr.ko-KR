---
title: EDiscovery 검색 결과 내보낼 때 PST 파일의 크기를 변경 합니다.
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 04e9de2d-765b-457b-a98a-d0f60bfb13f2
description: 변경할 수는 eDiscovery 검색 결과 내보낼 때 서버 컴퓨터에 있는 PST 파일의 기본 크기입니다.
ms.openlocfilehash: 1479db72117729d2e5cfa6feec1d9a0d9a60ffb5
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037991"
---
# <a name="change-the-size-of-pst-files-when-exporting-ediscovery-search-results"></a>EDiscovery 검색 결과 내보낼 때 PST 파일의 크기를 변경 합니다.

Office 365 eDiscovery 내보내기 도구를 사용 하 여 다양 한 Microsoft eDiscovery 도구에서 eDiscovery 검색의 전자 메일 결과 내보내려면를 내보낼 수 있는 PST 파일의 기본 크기는 10GB입니다. 이 기본 크기를 변경 하려는 경우에 검색 결과 내보내는 데 사용 하는 컴퓨터에서 Windows 레지스트리를 편집할 수 있습니다. PST 파일을 이동식 미디어, DVD를, 컴팩트 디스크 또는 USB 드라이브에 맞출 수 있는 이므로이 작업을 수행 하는 한 가지 이유입니다. 
  
> [!NOTE]
>  Office 365 eDiscovery 내보내기 도구는 Office 365 보안에서 콘텐츠 검색을 사용 하는 경우 검색 결과 내보내는 데 &amp; 준수 센터, Exchange Online에서 원본 위치 eDiscovery 및 SharePoint Online에서 eDiscovery 센터입니다. 
  
## <a name="create-a-registry-setting-to-change-the-size-of-pst-files-when-you-export-ediscovery-search-results"></a>EDiscovery 검색 결과 내보낼 때 PST 파일의 크기를 변경 하는 레지스트리 설정을 만들기

EDiscovery 검색의 결과 내보내는 데 사용할 수 있는 컴퓨터에서 다음 절차를 수행 합니다.
  
1. 열려 있으면 Office 365 eDiscovery 내보내기 도구를 닫습니다. 
    
2. .Reg; filename 접미사를 사용 하 여 창 레지스트리 파일에 다음 텍스트를 저장 예: PstExportSize.reg 합니다. 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "PstSizeLimitInBytes"="1073741824"
    ```

    위의 예제는 `PstSizeLimitInBytes` 값이 1,073,741,824 바이트 또는 약 1GB로 설정 합니다. 다음에 대 한 다른 샘플 값은는 `PstSizeLimitInBytes` 설정 합니다. 
    
    |**Gb에서 크기 조정 (약)**|**크기 (바이트)**|
    |:-----|:-----|
    |.7 G B (700 MB)  <br/> |751619277  <br/> |
    |2GB  <br/> |2147483648  <br/> |
    |4GB  <br/> |4294967296  <br/> |
    |8GB  <br/> |8589934592  <br/> |
   
3. 변경 된 `PstSizeLimitInBytes` PST 파일로 검색 결과 내보내기 하 고 다음 파일을 저장 하는 경우의 원하는 최대 크기는 값입니다. 
    
4. Windows 탐색기에서를 클릭 하거나 이전 단계에서 만든.reg 파일을 두번클릭 합니다.
    
5. 사용자 액세스 제어 창에서 **예** 는 변경 내용을 적용 하 여 레지스트리 편집기를 하도록 하려면이 옵션을 클릭 합니다. 
    
6. 를 계속 하 라는 메시지가 나타나면 **예**를 클릭 합니다.
    
    레지스트리 편집기 설정을 레지스트리에 성공적으로 추가 된 했다는 메시지를 표시 합니다.
    
7. 에 대 한 값을 변경 하려면 3-6 단계를 반복 하 수는 `PstSizeLimitInBytes` 레지스트리 설정 합니다. 
  
## <a name="frequently-asked-questions-about-changing-the-default-size-of-pst-files-when-you-export-ediscovery-search-results"></a>EDiscovery 검색 결과 내보낼 때 PST 파일의 기본 크기를 변경 하는 방법에 대 한 질문과 대답

 **기본 이유는 크기 조정 10GB?**
  
고객 의견;에 10GB의 기본 크기를 기준 10GB 최적의 단일 PST 나 파일 손상의 최소 기회를 사용 하 여 콘텐츠의 양 간에 적절 한 균형입니다.
  
 **증가 또는 PST 파일의 기본 크기 줄이기 해야 합니까?**
  
고객 조직에서 다른 위치 제공 물리적으로 수 있는 이동식 미디어에 검색 결과 나타낼 수 있도록 크기 제한을 감소 하는 경향이 있습니다. PST 파일을 10GB 손상 문제가 있을 것 보다 더 큰 때문에 기본 크기를 늘리면 하지 것이 좋습니다.
  
 **이 작업을 수행에서 어떤 컴퓨터 해야 합니까?**
  
Office 365 eDiscovery 내보내기 도구를 실행 하는 모든 로컬 컴퓨터에서 레지스트리 설정을 변경 해야 합니다.
  
 **이 설정은 변경 후 컴퓨터를 재부팅 해야 합니까?**
  
아니요, 컴퓨터를 다시 부팅 필요가 없습니다. 하지만를 닫으려면 하 고 다시 시작 해야 Office 365 eDiscovery 내보내기 도구를 실행 하는 경우이 설정을 변경한 후 것입니다.
  
 **기존 레지스트리 키 편집 가져오기 또는 않는 새 키를 만든 가져올?**
  
새 레지스트리 키에는이 절차에서 만든.reg 파일을 실행 하는 처음으로 만들어집니다. 다음 설정은 변경 하 고 편집.reg 파일을 다시 실행 때마다 편집 합니다.
