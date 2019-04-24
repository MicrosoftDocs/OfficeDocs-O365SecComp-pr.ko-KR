---
title: 내보내기 작업 다운로드
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 904bc5f8a6d6cef937d55336e8f383957713769a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32251924"
---
# <a name="download-export-jobs"></a>내보내기 작업 다운로드

내보낸 모든 데이터는 Microsoft Azure blob에 추가 됩니다. 이렇게 하면 데이터 다운스트림을 처리할 수 있는 여러 옵션이 제공 됩니다. Azure blob에 액세스 하는 방법에는 여러 가지가 있습니다. 한 가지 방법은 Azure Storage Explorer를 사용 하는 것입니다. 이 메서드는 간단한 연결, 검색 및 다운로드를 지원 합니다. 자세한 내용을 보려면<https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer>

1.  내보내기 작업이 완료 된 후 콘텐츠를 다운로드 하려면 내보내기 탭으로 이동 하 여 export 작업을 선택 합니다.

2.  플라이 아웃의 "위치" 섹션에 있는 텍스트를 복사 합니다.

![](../media/eDiscoExportJob.png)

3.  Azure Storage Explorer를 열고 "연결" 단추를 클릭 합니다.

![](../media/AzureStorageConnect.png)

4.  "공유 액세스 서명 URI 사용"을 선택 하 고 다음을 클릭 합니다.

![](../media/AzureStorageConnect2.png)

5.  URI 텍스트 상자에 위치 텍스트를 붙여넣고 다음을 클릭 합니다.

![](../media/AzureStorageConnect3.png)

6.  연결 클릭

![](../media/AzureStorageConnect4.png)

이렇게 하면 저장소 계정/SAS 연결 서비스/Blob 컨테이너에서 내보내기 내용이 개체로 추가 됩니다. 내보내기를 탐색 하 고 내보내기 전체 또는 일부를 다운로드할 수 있습니다.

![](../media/AzureStorageConnect5.png)