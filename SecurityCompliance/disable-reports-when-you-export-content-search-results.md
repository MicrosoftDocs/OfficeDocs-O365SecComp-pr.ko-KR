---
title: 콘텐츠 검색 결과를 내보낼 때 보고서를 사용하지 않도록 설정
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: c9b0ff0c-282b-4a44-b43f-cfc5b96557f9
description: 로컬 컴퓨터에서 Windows 레지스트리를 편집 하 여 Office 365의 보안 & 준수 센터에서 콘텐츠 검색 결과를 내보낼 때 보고서를 사용 하지 않도록 설정 합니다. 이러한 보고서를 사용 하지 않도록 설정 하면 다운로드 시간을 단축 하 고 디스크 공간을 절약할 수 있습니다.
ms.openlocfilehash: 19d97bbc95be5db6540e6822721752ca62adebfc
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256856"
---
# <a name="disable-reports-when-you-export-content-search-results"></a>콘텐츠 검색 결과를 내보낼 때 보고서를 사용하지 않도록 설정

Office 365 eDiscovery 내보내기 도구를 사용 하 여 보안 & 준수 센터에서 콘텐츠 검색 결과를 내보낼 때이 도구는 내보낸 콘텐츠에 대 한 추가 정보가 포함 된 두 개의 보고서를 자동으로 만들고 내보냅니다. 이러한 보고서는 결과. .csv 파일 및 manifest.xml 파일 (이러한 보고서에 대 한 자세한 설명을 보려면이 항목의 [보고서 내보내기 비활성화에 대 한 질문과 대답](#frequently-asked-questions-about-disabling-export-reports) 섹션 참조)이 있습니다. 이러한 파일은 매우 커질 수 있으므로 다운로드 시간을 단축 하 고 이러한 파일을 내보내지 못하게 하 여 디스크 공간을 절약할 수 있습니다. 검색 결과를 내보내는 데 사용 하는 컴퓨터에서 Windows 레지스트리를 변경 하 여이 작업을 수행할 수 있습니다. 나중에 보고서를 포함 하려면 레지스트리 설정을 편집할 수 있습니다. 
  
## <a name="create-registry-settings-to-disable-the-export-reports"></a>레지스트리 설정을 만들어 내보내기 보고서를 사용 하지 않도록 설정

결과를 콘텐츠 검색으로 내보내기 위해 사용 하는 컴퓨터에서 다음 절차를 수행 합니다.
  
1. Office 365 eDiscovery 내보내기 도구가 열려 있는 경우 해당 도구를 닫습니다.
    
2. 사용 하지 않도록 설정할 내보내기 보고서에 따라 다음 단계 중 하나 또는 두 가지를 모두 수행 합니다.
    
    - **결과 .csv**
    
      파일 이름 접미사를 사용 하 여 Windows 레지스트리 파일에 다음 텍스트를 저장 합니다. 예: DisableResultsCsv.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d False 
      ```

    - **manifest.xml**
    
      파일 이름 접미사를 사용 하 여 Windows 레지스트리 파일에 다음 텍스트를 저장 합니다. 예: DisableManifestXml.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d False 
      ```

3. Windows 탐색기에서 이전 단계에서 만든 .reg 파일을 클릭 하거나 두 번 클릭 합니다.
    
4. 사용자 액세스 제어 창에서 **예** 를 클릭 하 여 레지스트리 편집기에서 변경 작업을 수행 하도록 합니다. 
    
5. 계속할지 묻는 메시지가 표시 되 면 **예**를 클릭 합니다.
    
    레지스트리 편집기에 설정이 레지스트리에 성공적으로 추가 되었다는 메시지가 표시 됩니다.
  
## <a name="edit-registry-settings-to-re-enable-the-export-reports"></a>레지스트리 설정을 편집 하 여 내보내기 보고서를 다시 사용 하도록 설정

이전 절차에서 .reg 파일을 만들어 결과 .csv 및 manifest.xml 보고서를 사용 하지 않도록 설정한 경우에는 해당 파일을 편집 하 여 검색 결과와 함께 내보낼 수 있도록 보고서를 다시 활성화 합니다. 결과를 콘텐츠 검색으로 내보내기 위해 사용 하는 컴퓨터에서 다음 절차를 다시 수행 합니다.
  
1. Office 365 eDiscovery 내보내기 도구가 열려 있는 경우 해당 도구를 닫습니다.
    
2. 이전 절차에서 만든 .reg 편집 파일 하나 또는 둘 다를 편집 합니다.
    
    - **결과 .csv**
    
        메모장에서 DisableResultsCsv 파일을 열고 값 `False` 을로 `True`변경한 다음 파일을 저장 합니다. 예를 들어 파일을 편집한 후에는 다음과 같이 표시 됩니다.
    
        ```
        Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d True
        ```

    - **manifest.xml**
    
        메모장에서 DisableManifestXml 파일을 열고 값 `False` 을로 `True`변경한 다음 파일을 저장 합니다. 예를 들어 파일을 편집한 후에는 다음과 같이 표시 됩니다.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d True
      ```

3. Windows 탐색기에서 이전 단계에서 편집한 .reg 파일을 클릭 하거나 두 번 클릭 합니다.
    
4. 사용자 액세스 제어 창에서 **예** 를 클릭 하 여 레지스트리 편집기에서 변경 작업을 수행 하도록 합니다. 
    
5. 계속할지 묻는 메시지가 표시 되 면 **예**를 클릭 합니다.
    
    레지스트리 편집기에 설정이 레지스트리에 성공적으로 추가 되었다는 메시지가 표시 됩니다.
  
## <a name="frequently-asked-questions-about-disabling-export-reports"></a>보고서 내보내기를 사용 하지 않도록 설정 하는 방법에 대 한 질문과 대답
<a name="faqs"> </a>

 **결과는 무엇입니까? .csv 및 manifest.xml 보고서?**
  
결과 .csv 및 manifest.xml 파일에는 내보낸 콘텐츠에 대 한 추가 정보가 포함 되어 있습니다.
  
- **Results** -검색 결과로 다운로드 되는 각 항목에 대 한 정보가 포함 된 Excel 문서입니다. 전자 메일의 경우 결과 로그에 다음을 비롯 한 각 메시지에 대 한 정보가 포함 됩니다. 
    
  - 원본 사서함에 있는 메시지의 위치 (포함 여부는 주 메시지는 보관 사서함 또는).
    
  - 메시지가 전송된 날짜
    
  - 메시지의 제목 줄입니다.
    
  - 보낸 사람 및 메시지 받는 사람입니다.
    
  - 검색 결과를 내보낼 때 중복 제거를 사용 하도록 설정한 경우 메시지가 중복 메시지 인지 여부 중복 메시지는 메시지를 중복 된 것으로 식별 하는 **부모 ItemId** 열에 값을 갖게 됩니다. **부모 ItemId** 열의 값은 내보낸 메시지의 **Item DocumentId** 열에 있는 값과 같습니다. 
    
    SharePoint 및 비즈니스용 OneDrive 사이트의 문서에 대해 결과 로그에 다음을 비롯 한 각 문서에 대 한 정보가 포함 됩니다.
    
  - 문서에 대 한 URL입니다.
    
  - 문서가 있는 사이트 모음의 URL입니다.
    
  - 문서를 마지막으로 수정한 날짜입니다.
    
  - 이름 (에 있는 제목 열 결과 로그에서) 문서입니다.
    
- **manifest.xml** -검색 결과에 포함 된 각 항목에 대 한 정보를 포함 하는 매니페스트 파일 (xml 형식)입니다. 이 보고서의 정보는 결과 .csv 보고서와 동일 하지만 edrm (전자식 Discovery Reference Model)에 지정 된 형식으로 되어 있습니다. edrm에 대 한 자세한 내용은로 [https://www.edrm.net](https://www.edrm.net)이동 합니다.
    
 **이러한 보고서 내보내기를 사용 하지 않도록 설정 해야 하는 경우**
  
특정 요구 사항에 따라 달라 집니다. 대부분의 조직에는 검색 결과에 대 한 추가 정보가 필요 하지 않으며 이러한 보고서가 필요 하지 않습니다.
  
 **어떤 컴퓨터에서이 작업을 수행 해야 하나요?**
  
 Office 365 eDiscovery 내보내기 도구를 실행 하는 로컬 컴퓨터에서 레지스트리 설정을 변경 해야 합니다. 
  
 **이 설정을 변경한 후 컴퓨터를 다시 시작 해야 하나요?**
  
아니요, 컴퓨터를 다시 시작할 필요가 없습니다. 그러나 Office 365 eDiscovery 내보내기 도구가 실행 되 고 있으면 닫은 후 레지스트리 설정을 변경한 후에 다시 시작 해야 합니다.
  
 **기존 레지스트리 키를 편집 하거나 새 키를 만들기 시작 합니까?**
  
이 항목의 절차에서 만든 .reg 파일을 처음 실행할 때 새 레지스트리 키가 만들어집니다. 그런 다음 .reg 편집 파일을 변경 하 고 다시 실행할 때마다 설정이 편집 됩니다.
