---
title: Office 365 보안에서 콘텐츠 검색 결과 내보낼 때 보고서를 사용 하지 않도록 설정 &amp; 준수 센터
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9b0ff0c-282b-4a44-b43f-cfc5b96557f9
description: Office 365 보안에서 콘텐츠 검색의 결과 내보낼 때 보고서를 사용 하지 않도록 설정 하려면 로컬 컴퓨터에 Windows 레지스트리를 편집 &amp; Comliance 센터입니다. 이러한 보고서를 사용 하지 않도록 설정 다운로드 시간을 단축 하 고 디스크 공간을 절약할 수 있습니다.
ms.openlocfilehash: 3c09e0563ddd4469f21950dc3a698ce08b0014df
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534024"
---
# <a name="disable-reports-when-you-export-content-search-results-in-the-office-365-security-amp-compliance-center"></a>Office 365 보안에서 콘텐츠 검색 결과 내보낼 때 보고서를 사용 하지 않도록 설정 &amp; 준수 센터

보안에서 콘텐츠 검색의 결과를 내보내려면 Office 365 eDiscovery 내보내기 도구를 사용 하면 &amp; 준수 센터 도구가 자동으로 만들고 내보낸된 콘텐츠에 대 한 추가 정보를 포함 하는 두 보고서를 내보냅니다. 이러한 보고서는 Results.csv 파일과 Manifest.xml 파일 (이 항목에 대 한 자세한 설명은 이러한 보고서의 [질문과 대답 (영문) 내보내기 보고서를 사용 하지 않도록 설정 하는 방법에 대 한](#frequently-asked-questions-about-disabling-export-reports) 섹션 참조). 이러한 파일 매우 커질 수 있으므로 다운로드 시간을 단축할 수 있으며 내보내고에서 이러한 파일을 방지 하 여 디스크 공간을 절약할 수 있습니다. 검색 결과 내보내는 데 사용 하는 컴퓨터에서 Windows 레지스트리를 변경 하 여이 수행할 수 있습니다. 나중에는 보고서를 포함 하려는 경우에 레지스트리 설정을 편집할 수 있습니다. 
  
## <a name="create-registry-settings-to-disable-the-export-reports"></a>내보내기 보고서를 사용 하지 않도록 설정 하려면 레지스트리 설정을 만들려면

콘텐츠 검색 결과 내보내는 데 사용할 수 있는 컴퓨터에서 다음 절차를 수행 합니다.
  
1. 열려 있으면 Office 365 eDiscovery 내보내기 도구를 닫습니다.
    
2. 어떤 내보내기 보고서에 따라 사용 하지 않도록 설정 하려면 다음 단계 중 하나 또는 모두를 수행 합니다.
    
    - **Results.csv**
    
      .Reg; filename 접미사를 사용 하 여 Windows 레지스트리 파일에 다음 텍스트를 저장 예: DisableResultsCsv.reg 합니다.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d False 
      ```

    - **Manifest.xml**
    
      .Reg; filename 접미사를 사용 하 여 Windows 레지스트리 파일에 다음 텍스트를 저장 예: DisableManifestXml.reg 합니다.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d False 
      ```

3. Windows 탐색기에서를 클릭 하거나 이전 단계에서 만든.reg 파일을 두번클릭 합니다.
    
4. 사용자 액세스 제어 창에서 **예** 는 변경 내용을 적용 하 여 레지스트리 편집기를 하도록 하려면이 옵션을 클릭 합니다. 
    
5. 를 계속 하 라는 메시지가 나타나면 **예**를 클릭 합니다.
    
    레지스트리 편집기 설정을 레지스트리에 성공적으로 추가 된 했다는 메시지를 표시 합니다.
  
## <a name="edit-registry-settings-to-re-enable-the-export-reports"></a>레지스트리 설정을 다시 내보내기 보고서를 사용 하도록 설정 편집

이전 절차에서.reg 파일을 만들어서 Results.csv 및 Manifest.xml 보고서를 사용 하지 않도록 설정한 경우에 검색 결과 함께 내보낼 수 있도록 보고서를 다시 활성화 하려면 해당 파일을 편집할 수 있습니다. 다시, 콘텐츠 검색 결과 내보내는 데 사용할 수 있는 컴퓨터에서 다음 절차를 수행 합니다.
  
1. 열려 있으면 Office 365 eDiscovery 내보내기 도구를 닫습니다.
    
2. 이전 절차에서 만든.reg 편집 파일 중 하나 또는 모두를 편집 합니다.
    
    - **Results.csv**
    
        Open 메모장에서 DisableResultsCsv.reg 파일 값을 변경 `False` 에 `True`, 파일을 저장 합니다. 예, 파일을 편집한 후 다음과 같이 나타납니다.
    
        ```
        Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d True
        ```

    - **Manifest.xml**
    
        Open 메모장에서 DisableManifestXml.reg 파일 값을 변경 `False` 에 `True`, 파일을 저장 합니다. 예, 파일을 편집한 후 다음과 같이 나타납니다.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d True
      ```

3. Windows 탐색기에서를 클릭 하거나 이전 단계에서 편집 하는.reg 파일을 두번클릭 합니다.
    
4. 사용자 액세스 제어 창에서 **예** 는 변경 내용을 적용 하 여 레지스트리 편집기를 하도록 하려면이 옵션을 클릭 합니다. 
    
5. 를 계속 하 라는 메시지가 나타나면 **예**를 클릭 합니다.
    
    레지스트리 편집기 설정을 레지스트리에 성공적으로 추가 된 했다는 메시지를 표시 합니다.
  
## <a name="frequently-asked-questions-about-disabling-export-reports"></a>내보내기 보고서를 사용 하지 않도록 설정 하는 방법에 대 한 질문과 대답
<a name="faqs"> </a>

 **Results.csv 및 Manifest.xml 보고서는 무엇입니까?**
  
Results.csv 및 Manifest.xml 파일 내보낸 콘텐츠에 대 한 추가 정보를 포함 합니다.
  
- 검색 결과 다운로드 하는 각 항목에 대 한 정보가 포함 된 **Results.csv** Excel 문서입니다. 전자 메일, 결과 로그 각 메시지에 대 한 정보가 들어 포함 합니다. 
    
  - 원본 사서함에 있는 메시지의 위치 (포함 여부는 주 메시지는 보관 사서함 또는).
    
  - 메시지가 전송된 날짜
    
  - 메시지의 제목 줄입니다.
    
  - 보낸 사람 및 메시지 받는 사람입니다.
    
  - 있는지 여부는 메시지 검색 결과 내보낼 때 중복을 사용 하는 경우 중복 된 메시지입니다. 중복 된 메시지는 중복 된 것으로 메시지를 식별 하는 **상위 ItemId** 열에서 값을 갖게 됩니다. **부모 ItemId** 열에서 값은 내보낸 메시지의 **항목 DocumentId** 열에서 값과 같습니다. 
    
    SharePoint와 OneDrive에서 비즈니스 사이트에 대 한 문서에 대 한 결과 로그는 각 문서에 대 한 정보를 포함 포함 합니다.
    
  - 문서에 대 한 URL입니다.
    
  - 문서가 있는 사이트 모음의 URL입니다.
    
  - 문서를 마지막으로 수정한 날짜입니다.
    
  - 이름 (에 있는 제목 열 결과 로그에서) 문서입니다.
    
- **Manifest.xml** 매니페스트 파일 (XML 형식)에서 검색 결과에 포함 된 각 항목에 대 한 정보를 포함 하는입니다. 이 보고서의 정보는 Results.csv 보고서 같지만 지정 하 여는 참조 모델 EDRM (Electronic Discovery) 형식에서입니다. EDRM에 대 한 자세한 내용은 이동 [https://www.edrm.net](https://www.edrm.net)합니다.
    
 **이러한 보고서 내보내기 (영문)를 비활성화 해야는 경우**
  
특정 요구 사항에 따라 다릅니다. 대부분의 조직에서는 검색 결과 대 한 추가 정보를 필요 하지 않습니다 및 이러한 보고서를 필요로 하지 않습니다.
  
 **이 작업을 수행에서 어떤 컴퓨터 해야 합니까?**
  
 Office 365 eDiscovery 내보내기 도구를 실행 하는 모든 로컬 컴퓨터에서 레지스트리 설정을 변경 해야 합니다. 
  
 **이 설정은 변경 후 컴퓨터를 다시 시작 해야 합니까?**
  
아니요, 컴퓨터를 다시 시작할 필요가 없습니다. 하지만 Office 365 eDiscovery 내보내기 도구를 실행 하는 경우를 닫고 레지스트리 설정을 변경한 다음 다시 시작 해야 합니다.
  
 **기존 레지스트리 키 편집 가져오기 또는 않는 새 키를 만든 가져올?**
  
새 레지스트리 키에는이 항목의 절차에서 만든.reg 파일을 실행 하는 처음으로 만들어집니다. 다음 설정은 변경 하 고 편집.reg 파일을 다시 실행 때마다 편집 합니다.
