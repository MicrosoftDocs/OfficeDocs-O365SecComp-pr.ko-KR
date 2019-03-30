---
title: eDiscovery 검색 결과를 내보낼 때 PST 파일 크기 변경
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 04e9de2d-765b-457b-a98a-d0f60bfb13f2
description: eDiscovery 검색 결과를 내보낼 때 컴퓨터로 다운로드 되는 PST 파일의 기본 크기를 변경할 수 있습니다.
ms.openlocfilehash: 98b543b6e34cb9cb075a765671def91742aee6c1
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999721"
---
# <a name="change-the-size-of-pst-files-when-exporting-ediscovery-search-results"></a>eDiscovery 검색 결과를 내보낼 때 PST 파일 크기 변경

Office 365 eDiscovery 내보내기 도구를 사용 하 여 다른 Microsoft eDiscovery 도구에서 eDiscovery 검색의 전자 메일 결과를 내보낼 때 내보낼 수 있는 PST 파일의 기본 크기는 10gb입니다. 이 기본 크기를 변경 하려는 경우 검색 결과를 내보내는 데 사용 하는 컴퓨터에서 Windows 레지스트리를 편집할 수 있습니다. 이 작업을 수행 하는 한 가지 이유는 PST 파일이 DVD, 컴팩트 디스크 또는 USB 드라이브 같은 이동식 미디어에 들어갈 수 있도록 하는 것입니다. 
  
> [!NOTE]
>  Office 365 eDiscovery 내보내기 도구는 보안 및 준수 센터의 콘텐츠 검색 도구, Exchange online의 원본 위치 eDiscovery 및 SharePoint online의 eDiscovery 센터를 사용 하는 경우 검색 결과를 내보내는 데 사용 됩니다.
  
## <a name="create-a-registry-setting-to-change-the-size-of-pst-files-when-you-export-ediscovery-search-results"></a>eDiscovery 검색 결과를 내보낼 때 PST 파일 크기를 변경 하는 레지스트리 설정 만들기

eDiscovery 검색의 결과를 내보내는 데 사용할 컴퓨터에서 다음 절차를 수행 합니다.
  
1. Office 365 eDiscovery 내보내기 도구가 열려 있는 경우 해당 도구를 닫습니다. 
    
2. 파일 이름 접미사를 사용 하 여 windows 레지스트리 파일에 다음 텍스트를 저장 합니다. 예: PstExportSize. 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "PstSizeLimitInBytes"="1073741824"
    ```

    위 예에서 `PstSizeLimitInBytes` 값은 1073741824 바이트 또는 약 1gb로 설정 됩니다. 다음은 `PstSizeLimitInBytes` 설정에 대 한 몇 가지 다른 예제 값입니다. 
    
    |**크기 (GB)**|**크기 (바이트)**|
    |:-----|:-----|
    |7g b (700 MB)  <br/> |751619277  <br/> |
    |2GB  <br/> |2147483648  <br/> |
    |4 GB  <br/> |4294967296  <br/> |
    |8GB  <br/> |8589934592  <br/> |
   
3. 검색 결과 `PstSizeLimitInBytes` 를 내보낼 때 값을 원하는 PST 파일의 최대 크기로 변경한 다음 파일을 저장 합니다. 
    
4. Windows 탐색기에서 이전 단계에서 만든 .reg 파일을 클릭 하거나 두 번 클릭 합니다.
    
5. 사용자 액세스 제어 창에서 **예** 를 클릭 하 여 레지스트리 편집기에서 변경 작업을 수행 하도록 합니다. 
    
6. 계속할지 묻는 메시지가 표시 되 면 **예**를 클릭 합니다.
    
    레지스트리 편집기에 설정이 레지스트리에 성공적으로 추가 되었다는 메시지가 표시 됩니다.
    
7. 3-6 단계를 반복 하 여 `PstSizeLimitInBytes` 레지스트리 설정 값을 변경할 수 있습니다. 
  
## <a name="frequently-asked-questions-about-changing-the-default-size-of-pst-files-when-you-export-ediscovery-search-results"></a>eDiscovery 검색 결과를 내보낼 때 PST 파일의 기본 크기를 변경 하는 방법에 대 한 질문과 대답

 **기본 크기가 10gb 인 이유는 무엇 인가요?**
  
기본 크기 10gb는 고객 의견을 기반으로 합니다. 10gb는 단일 PST에 있는 콘텐츠의 최적 정도와 파일 손상 가능성을 최소화 하는 것이 좋습니다.
  
 **PST 파일의 기본 크기를 늘리거나 줄여야 하나요?**
  
고객은 사용자가 조직의 다른 위치를 물리적으로 배송 하는 데 사용할 수 있는 이동식 미디어에 대 한 검색 결과에 맞게 크기 제한을 줄이는 경향이 있습니다. 10mb를 초과 하는 PST 파일에 손상 문제가 있을 수 있으므로 기본 크기를 늘리지 않는 것이 좋습니다.
  
 **어떤 컴퓨터에서이 작업을 수행 해야 하나요?**
  
Office 365 eDiscovery 내보내기 도구를 실행 하는 로컬 컴퓨터에서 레지스트리 설정을 변경 해야 합니다.
  
 **이 설정을 변경한 후에는 컴퓨터를 다시 부팅 해야 하나요?**
  
아니요, 컴퓨터를 다시 부팅할 필요가 없습니다. 그러나 Office 365 eDiscovery 내보내기 도구를 실행 하는 경우이 설정을 변경 하 고 나면이를 닫고 다시 시작 해야 합니다.
  
 **기존 레지스트리 키를 편집 하거나 새 키를 만들기 시작 합니까?**
  
이 절차에서 만든 .reg 파일을 처음 실행할 때 새 레지스트리 키가 만들어집니다. 그런 다음 .reg 편집 파일을 변경 하 고 다시 실행할 때마다 설정이 편집 됩니다.
