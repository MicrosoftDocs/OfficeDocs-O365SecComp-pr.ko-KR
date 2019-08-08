---
title: 내보내기 작업 다운로드
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Advanced eDiscovery의 검토 집합에서 내보낸 문서를 Azure 저장소 탐색기를 설치 하 고 사용 하 여 다운로드 합니다.
ms.openlocfilehash: f236f53be9dda88fe5b8448011aa651603e38182
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36231035"
---
# <a name="download-export-jobs"></a>내보내기 작업 다운로드

고급 eDiscovery 사례의 검토 집합에서 문서를 내보낼 때 문서는 Microsoft에서 제공한 Azure 저장소 위치 또는 조직에서 관리 하는 Azure 저장소 위치에 업로드 됩니다. 사용 되는 Azure Storage location 유형은 문서를 내보낼 때 선택한 옵션에 따라 달라 집니다. 

이 문서에서는 Microsoft Azure Storage Explorer를 사용 하 여 Azure 저장소 위치에 연결 하 여 내보낸 문서를 찾아보고 다운로드 하는 방법에 대 한 지침을 제공 합니다. Azure Storage Explorer에 대 한 자세한 내용은 [빠른 시작: Azure Storage Explorer 사용](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer)을 참조 하십시오.

## <a name="step-1-install-the-azure-storage-explorer"></a>1 단계: Azure Storage Explorer 설치

첫 번째 단계는 Azure Storage Explorer를 다운로드 하 여 설치 하는 것입니다. 자세한 내용은 [Azure Storage Explorer 도구](https://go.microsoft.com/fwlink/p/?LinkId=544842)를 참조 하십시오. 이 도구를 사용 하 여 3 단계에서 내보낸 문서에 연결 하 고 다운로드 합니다.

## <a name="step-2-obtain-the-sas-url-from-the-export-job"></a>2 단계: 내보내기 작업에서 SAS URL 가져오기

다음 단계에서는 [검토 집합에서 문서를 내보내기](export-documents-from-review-set.md)위해 내보내기 작업을 만들 때 생성 되는 SAS (공유 액세스 서명) URL을 가져옵니다. Microsoft에서 제공한 Azure 저장소 위치 또는 조직에서 관리 하는 Azure 저장소 위치에 업로드 된 문서에 대 한 SAS URL을 복사할 수 있습니다. 두 경우 모두 SAS URL을 사용 하 여 3 단계에서 Azure 저장소 위치에 연결 합니다.

1. **고급 eDiscovery** 페이지에서 사례로 이동한 후 **내보내기** 탭을 클릭 합니다.

2. 내보내기 탭 **** 에서 다운로드 하려는 내보내기 작업을 클릭 합니다.

3. 플라이 아웃 페이지의 **위치**아래에 표시 된 SAS URL을 복사 합니다. 필요한 경우 3 단계에서 액세스할 수 있도록 파일을 파일로 저장할 수 있습니다.
 
   ![위치 아래에 표시 된 SAS URL 복사](../media/eDiscoExportJob.png)

## <a name="step-3-connect-to-the-azure-storage-location"></a>3 단계: Azure 저장소 위치에 연결

마지막 단계에서는 Azure Storage Explorer와 SAS URL을 사용 하 여 Azure 저장소 위치에 연결 하 고 내보낸 문서를 로컬 컴퓨터로 다운로드 합니다.

1.  1 단계에서 설치한 Azure Storage Explorer를 엽니다.

2. **계정 추가** 아이콘을 클릭 합니다. 또는 **저장소 계정을**마우스 오른쪽 단추로 클릭 해도 됩니다.

   ![계정 추가 아이콘을 클릭 합니다.](../media/AzureStorageConnect.png)

3.  **Azure Storage에 연결** 페이지에서 **SAS (공유 액세스 서명) URI 사용** 을 클릭 한 후 **다음**을 클릭 합니다.

    ![SAS (공유 액세스 서명) URI 사용을 클릭 한 후 다음을 클릭 합니다.](../media/AzureStorageConnect2.png)

4.  **SAS URI로 연결** 페이지에서 URI 상자를 클릭 한 다음 2 단계에서 얻은 SAS URL을 붙여 넣습니다. 

    ![URI 상자에 SAS URL을 붙여 넣습니다.](../media/AzureStorageConnect3.png)

    **표시 이름** 상자에 SAS URL의 일부가 표시 됩니다. 이 이름은 저장소 위치에 연결한 후 **저장소 계정** 에 만들어지는 컨테이너의 표시 이름으로 사용 됩니다. 이 이름은 Advanced eDiscovery 사례의 ID와 고유 식별자로 구성 됩니다. 기본 표시 이름을 그대로 유지 하거나 변경할 수 있습니다. 이름을 변경 하는 경우에는 표시 이름이 고유 해야 합니다.

5.  **다음**을 클릭합니다.

    **연결 요약** 페이지가 표시 됩니다.
   
    ![연결 요약 페이지에서 연결을 클릭 하 여 Azure 저장소 위치에 연결 합니다.](../media/AzureStorageConnect4.png)

6. **연결 요약** 페이지에서 연결 정보를 검토 한 다음 **연결**을 클릭 합니다. 

    **Blob 컨테이너** 노드 ( **저장소 계정** > **(연결 된 컨테이너))** \> 가 열립니다. 

    ![](../media/AzureStorageConnect5.png)

    여기에는 4 단계의 표시 이름으로 이름이 지정 된 컨테이너가 포함 되어 있습니다. 이 컨테이너에는 사용자가 만든 각 내보내기 작업에 대 한 폴더가 포함 됩니다. 이러한 폴더는 내보내기 작업의 ID에 해당 하는 ID로 이름이 지정 됩니다. **작업** 탭에 나열 된 각 **내보내기 데이터 준비** 작업에 대 한 플라이 아웃 페이지의 **지원 정보** 아래에서 이러한 내보내기 id와 내보내기 이름을 찾을 수 있습니다.

7. 내보내기 작업 폴더를 두 번 클릭 하 여 엽니다.

   폴더 및 내보내기 보고서 목록이 표시 됩니다.
   
    ![내보내기 폴더에는 내보낸 파일 및 내보내기 보고서가 포함 되어 있습니다.](../media/AzureStorageConnect6.png)

   내보내기 작업 폴더에는 다음과 같은 항목이 포함 됩니다. 내보내기 폴더의 실제 항목은 내보내기 작업을 만들 때 구성 된 내보내기 옵션에 따라 결정 됩니다. 자세한 내용은 [문서를 검토 집합에서 내보내기를](export-documents-from-review-set.md)참조 하십시오.

    - Export_load_file:이 CSV 파일은 내보낸 각 문서에 대 한 정보를 포함 하는 세부 내보내기 보고서입니다. 이 파일은 문서에 대 한 각 metadata 속성의 열로 구성 됩니다. 이 보고서에 포함 된 메타 데이터의 목록 및 설명에 대 한 자세한 내용은 [Advanced eDiscovery의 문서 메타 데이터 필드](document-metadata-fields.md)에 있는 표에서 **내보낸 필드 이름** 열을 참조 하십시오.
    
    - 요약 .txt: 내보내기 통계를 포함 하 여 내보내기 요약이 포함 된 텍스트 파일입니다.
    
    - Extracted_text_files:이 폴더에는 내보낸 각 문서의 텍스트 파일 버전이 들어 있습니다.
     
    - NativeFiles:이 폴더에는 내보낸 각 문서의 네이티브 파일 버전이 포함 되어 있습니다.
    
    - Error_files:이 폴더에는 내보내기 작업에 오류 파일이 포함 된 경우 다음 항목이 포함 됩니다. 
        
      - ExtractionError. csv:이 CSV 파일에는 부모 항목에서 제대로 추출 되지 않은 파일에 대 한 사용 가능한 메타 데이터가 포함 됩니다.
        
      - ProcessingError:이 폴더에는 처리 오류가 있는 문서가 포함 되어 있습니다. 이 콘텐츠는 항목 수준으로, 첨부 파일에 처리 오류가 있는 경우 첨부 파일이 들어 있는 문서도이 폴더에 포함 됩니다.
 
8. 내보내기에서 모든 콘텐츠를 내보내려면 내보내기 폴더를 선택 하 고 **다운로드**를 클릭 합니다.

9. 내보낸 파일을 다운로드 하려는 위치를 지정 하 고 폴더 선택을 클릭 합니다.

    Azure Storage Explorer가 내보내기 프로세스를 시작 합니다. 내보낸 항목을 다운로드 하는 상태가 **활동** 창에 표시 됩니다. 다운로드가 완료 되 면 메시지가 표시 됩니다.

    ![다운로드가 완료 되 면 메시지가 표시 됨](../media/AzureStorageConnect8.png)

> [!NOTE]
> 전체 내보내기 작업을 다운로드 하는 대신 특정 항목을 선택 하 여 다운로드할 수 있습니다. 항목을 다운로드 하는 대신 항목을 두 번 클릭 하 여 볼 수 있습니다.