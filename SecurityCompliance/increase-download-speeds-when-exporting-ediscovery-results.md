---
title: Office 365에서 eDiscovery 검색 결과를 내보낼 때 다운로드 속도 높이기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: c4c8f689-9d52-4e80-ae4b-1411ee9efc43
description: 검색 결과를 다운로드할 때 데이터 처리량을 높이도록 Windows 레지스트리를 구성 하는 방법과 Office 365의 보안 & 준수 센터 및 고급 eDiscovery에서 데이터를 검색 하는 방법을 알아봅니다.
ms.openlocfilehash: 10eff929d6b668d5e2bc22d8ee7f223da4943326
ms.sourcegitcommit: f0e3c9de0b545081a4d264f74559b941f6c71410
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/22/2019
ms.locfileid: "31958628"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a>Office 365에서 eDiscovery 검색 결과를 내보낼 때 다운로드 속도 높이기

office 365 eDiscovery 내보내기 도구를 사용 하 여 Security & 준수 센터에서 콘텐츠 검색 결과를 다운로드 하거나 office 365 Advanced eDiscovery에서 데이터를 다운로드 하면이 도구는 다운로드 하기 위해 특정 개수의 동시 내보내기 작업을 시작 합니다. 로컬 컴퓨터에 데이터를 추가할 수 있습니다. 기본적으로 동시 작업의 수는 데이터를 다운로드 하는 데 사용 하는 컴퓨터의 코어 수의 8 배로 설정 됩니다. 예를 들어 이중 코어 컴퓨터 (칩 하나에 두 개의 중앙 처리 장치)가 있는 경우 기본 동시 내보내기 작업 수는 16 개입니다. 데이터 전송 처리량을 늘리기 위해 다운로드 프로세스의 속도를 높이려면 검색 결과를 다운로드 하는 데 사용 하는 컴퓨터에서 Windows 레지스트리 설정을 구성 하 여 동시 작업 수를 늘릴 수 있습니다. 다운로드 프로세스의 속도를 향상 시키려면 24 개의 동시 작업을 설정 하는 것으로 시작 하는 것이 좋습니다.
  
낮은 대역폭의 네트워크를 통해 검색 결과를 다운로드 하는 경우이 설정을 높이면 부정적인 영향을 줄 수 있습니다. 또는 고대역폭 네트워크에서 24 개 보다 많은 동시 작업을 설정할 수 있습니다 (최대 동시 작업 수는 48). 이 레지스트리 설정을 구성한 후에는 환경에 대 한 최적의 동시 작업 수를 찾기 위해 변경 해야 할 수 있습니다.
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a>레지스트리 설정 만들기 데이터를 내보낼 때 동시 작업 수를 변경 하려면

보안 & 준수 센터에서 검색 결과를 다운로드 하는 데 사용 하는 컴퓨터에서 다음 절차를 수행 하거나 고급 eDiscovery에서 데이터를 확인 합니다.
  
1. Office 365 eDiscovery 내보내기 도구가 열려 있는 경우 해당 도구를 닫습니다. 
    
2. 파일 이름 접미사를 사용 하 여 windows 레지스트리 파일에 다음 텍스트를 저장 합니다. 예: ConcurrentOperations. 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    앞에서 설명한 것 처럼 24 개의 동시 작업을 시작 하 고 적절 하 게이 설정을 변경 하는 것이 좋습니다.
    
3. Windows 탐색기에서 이전 단계에서 만든 .reg 파일을 클릭 하거나 두 번 클릭 합니다.
    
4. 사용자 액세스 제어 창에서 **예** 를 클릭 하 여 레지스트리 편집기에서 변경 작업을 수행 하도록 합니다. 
    
5. 계속할지 묻는 메시지가 표시 되 면 **예**를 클릭 합니다.
    
    레지스트리 편집기에 설정이 레지스트리에 성공적으로 추가 되었다는 메시지가 표시 됩니다.
    
6. 2-5 단계를 반복 하 여 `DownloadConcurrency` 레지스트리 설정 값을 변경할 수 있습니다. 
    
    > [!IMPORTANT]
    > `DownloadConcurrency` 레지스트리 설정을 만들거나 변경한 후에는 새 내보내기 작업을 만들거나 다운로드 하려는 검색 결과 또는 데이터에 대 한 기존 내보내기 작업을 다시 시작 해야 합니다. 자세한 [내용은 추가 정보](#more-information) 섹션을 참조 하세요. 
  
## <a name="more-information"></a>추가 정보

- 이 절차에서 만든 .reg 파일을 처음 실행할 때 새 레지스트리 키가 만들어집니다. 그런 다음 `DownloadConcurrency` .reg 편집 파일을 변경 하 고 다시 실행할 때마다 레지스트리 설정이 편집 됩니다. 
    
- Office 365 eDiscovery 내보내기 도구는 [Azure AzCopy 유틸리티](https://go.microsoft.com/fwlink/?linkid=849949) 를 사용 하 여 보안 & 준수 센터 또는 고급 eDiscovery에서 검색 데이터를 다운로드 합니다. `DownloadConcurrency` 레지스트리 설정을 구성 하는 것은 AzCopy 유틸리티를 실행할 때 **/tnc** 매개 변수를 사용 하는 것과 비슷합니다. 따라서 레지스트리 설정은 `"DownloadConcurrency=24"` AzCopy 유틸리티 `/NC:24` 와 매개 변수 값을 함께 사용 하는 것과 같은 기능을 수행 합니다. 
    
- 현재 진행 중인 내보내기 다운로드를 중지 한 후 다시 시작 하 여 검색 결과를 다시 다운로드 하면 Office 365 eDiscovery 내보내기 도구가 동일한 다운로드를 다시 시작 하려고 시도 합니다. 따라서 다운로드를 시작 하 고, 중지 하 고, `DownloadConcurrency` 레지스트리 설정을 변경 하는 경우 **내보낸 결과 다운로드**를 클릭 하 여 다운로드를 다시 시작 하면 다운로드가 실패할 수 있습니다. 이는 내보내기 도구가 레지스트리 설정을 변경한 후에도 유효 하지 않은 설정을 사용 하 여 이전 다운로드를 다시 시작 하려고 하기 때문입니다.
    
    따라서 `DownloadConcurrency` 레지스트리 설정을 변경한 후에는 Security & 준수 센터에서 내보내기 **다시 시작**을 클릭 하 여 내보내기 작업을 다시 시작 해야 합니다. 그런 다음 내보낸 결과를 다운로드할 수 있습니다. 검색 결과 및 데이터를 내보내는 방법에 대 한 자세한 내용은 다음을 참조 하십시오.
    
  - [콘텐츠 검색 결과 내보내기](export-search-results.md)
    
  - [Office 365 Advanced eDiscovery에서 결과 내보내기](export-results-in-advanced-ediscovery.md)
    
