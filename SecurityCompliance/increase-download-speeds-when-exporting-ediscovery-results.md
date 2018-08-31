---
title: Office 365에서 eDiscovery 검색 결과 내보낼 때 다운로드 속도를 높입니다 합니다.
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c4c8f689-9d52-4e80-ae4b-1411ee9efc43
description: 검색 결과 다운로드할 때 데이터 처리량을 늘리려면 Windows 레지스트리를 구성 하는 방법을 설명 하 고 Office 365 보안에서 데이터를 검색 &amp; 준수 센터 및 Office 365 고급 eDiscovery 합니다.
ms.openlocfilehash: 3f456f5ee0312d4d4d7b95f868520e6756a90fd1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534157"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a>Office 365에서 eDiscovery 검색 결과 내보낼 때 다운로드 속도를 높입니다 합니다.

Office 365 보안에서 콘텐츠 검색의 결과 다운로드 하려면 Office 365 eDiscovery 내보내기 도구를 사용 하면 &amp; 동시 내보내기의 특정 번호를 시작 하는 Office 365 고급 eDiscovery로 설정 하는 도구에서 준수 센터 또는 다운로드 데이터 로컬 컴퓨터에 데이터를 다운로드 하는 작업입니다. 기본적으로 동시 작업 수는 데이터를 다운로드 하는 사용 하는 컴퓨터의 코어 수가 8 시간에 설정 됩니다. 예, 이중 코어 컴퓨터를 (누구나 칩이 둘의 두 중앙 처리 장치)를 설치한 경우 동시 내보내기 작업의 기본 번호는 16입니다. 데이터 전송 처리량과 인해 물거품이 다운로드 프로세스를 늘리려면 검색 결과 다운로드 하려면 사용 하는 컴퓨터에서 Windows 레지스트리 설정을 구성 하 여 동시 작업 수를 늘릴 수 있습니다. 인해 물거품이 다운로드 프로세스, 하려면 24 동시 작업의 설정을 사용 하 여 시작 하는 것이 좋습니다.
  
대역폭이 낮은 네트워크를 통해 검색 결과 다운로드 하는 경우이 설정을 늘리면는 저하 될 수 있습니다. 또는 (동시 작업의 최대 수는 512는) 고대역폭 네트워크에서 24 개 이상의 동시 작업을 하는 설정을 늘릴 수 있습니다. 이 레지스트리 설정을 구성한 후 최적의 사용자 환경에 대 한 동시 작업 수를 찾으려고 변경 해야할 수 있습니다.
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a>레지스트리 데이터를 내보낼 때 동시 작업 수를 변경 하려면 설정을 만들기

보안에서 검색 결과 다운로드 하려면 사용 하는 컴퓨터에서 다음 절차를 수행 &amp; 준수 센터 또는 고급 eDiscovery의 데이터입니다.
  
1. 열려 있으면 Office 365 eDiscovery 내보내기 도구를 닫습니다. 
    
2. .Reg; filename 접미사를 사용 하 여 창 레지스트리 파일에 다음 텍스트를 저장 예: ConcurrentOperations.reg 합니다. 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    같이 이전 설명, 24 동시 작업 시작 후에이 설정을 변경할 적절 하 게 하는 것이 좋습니다.
    
3. Windows 탐색기에서를 클릭 하거나 이전 단계에서 만든.reg 파일을 두번클릭 합니다.
    
4. 사용자 액세스 제어 창에서 **예** 는 변경 내용을 적용 하 여 레지스트리 편집기를 하도록 하려면이 옵션을 클릭 합니다. 
    
5. 를 계속 하 라는 메시지가 나타나면 **예**를 클릭 합니다.
    
    레지스트리 편집기 설정을 레지스트리에 성공적으로 추가 된 했다는 메시지를 표시 합니다.
    
6. 에 대 한 값을 변경 하려면 2 ~ 5 단계를 반복 하 수는 `DownloadConcurrency` 레지스트리 설정 합니다. 
    
    > [!IMPORTANT]
    > 만들기 또는 변경 후의 `DownloadConcurrency` 레지스트리 설정, 새 내보내기 작업을 만들거나 다운로드 하려는 데이터 나 검색 결과 대 한 기존 내보내기 작업을 다시 시작 해야 합니다. 자세한 내용은 [자세한 정보](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) 섹션을 참조 하십시오. 
  
## <a name="more-information"></a>추가 정보

- 새 레지스트리 키에는이 절차에서 만든.reg 파일을 실행 하는 처음으로 만들어집니다. 그런 다음 `DownloadConcurrency` 레지스트리 설정을 편집 하면 각 시간을 변경 하 고 편집.reg 파일을 다시 실행 합니다. 
    
- Office 365 eDiscovery 내보내기 도구는 [Azure AzCopy 유틸리티](https://go.microsoft.com/fwlink/?linkid=849949) 를 사용 하 여 보안에서 검색 데이터를 다운로드 하려면 &amp; 준수 센터 또는 고급 eDiscovery에서 합니다. 구성 된 `DownloadConcurrency` 레지스트리 설정은 AzCopy 유틸리티를 실행 하는 경우 **/NC** 매개 변수를 사용 하는 것과 비슷합니다. 따라서의 레지스트리 설정을 `"DownloadConcurrency=24"` 매개 변수 값을 사용 하는 것과 같습니다 떨어지기 `/NC:24` AzCopy 유틸리티를 사용 합니다. 
    
- 현재 진행 중인 하 고 다음 (검색 결과 다시 다운로드 하는 동안)가 다시 시작 하는 내보내기 다운로드를 중지 하는 경우 Office 365 eDiscovery 내보내기 도구는 동일한 다운로드를 다시 시작 하려고 합니다. 다운로드를 시작 하는 경우를 중지 하 고 다음 변경 등의 `DownloadConcurrency` 레지스트리 설정, 다운로드 실패할 수 있습니다 ( **다운로드 내보낸 결과**클릭) 하 여 다시 시작 하는 경우. 이 내보내기 도구는 레지스트리 설정을 변경 하기 때문에 유효 하지 않은 설정을 사용 하 여 이전 다운로드를 다시 시작 하려고 합니다.
    
    변경한 후에 따라서는 `DownloadConcurrency` 레지스트리 설정, 보안에서 ( **내보내기를 다시 시작**을 클릭) 하 여 내보내기 작업을 다시 시작 해야 &amp; 준수 센터입니다. 그런 다음 내보낸된 결과 다운로드할 수 있습니다. 검색 결과 데이터 내보내기 하는 방법에 대 한 자세한 내용은 다음을 참조 합니다.
    
  - [Office 365 보안에서 콘텐츠 검색 결과 내보낼 &amp; 준수 센터](export-search-results.md)
    
  - [Office 365 Advanced eDiscovery 결과 내보내기](export-results-in-advanced-ediscovery.md)
    
