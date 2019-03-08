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
ms.sourcegitcommit: 9f38ba72eba0b656e507860ca228726e4199f7ec
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/07/2019
ms.locfileid: "30475698"
---
# <a name="download-export-jobs"></a><span data-ttu-id="3fc37-102">내보내기 작업 다운로드</span><span class="sxs-lookup"><span data-stu-id="3fc37-102">Download export jobs</span></span>

<span data-ttu-id="3fc37-103">내보낸 모든 데이터는 Microsoft Azure blob에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3fc37-103">All exported data is added to a Microsoft Azure blob.</span></span> <span data-ttu-id="3fc37-104">이렇게 하면 데이터 다운스트림을 처리할 수 있는 여러 옵션이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3fc37-104">This provides multiple options to handle the data downstream.</span></span> <span data-ttu-id="3fc37-105">Azure blob에 액세스 하는 방법에는 여러 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3fc37-105">There are several ways to access an Azure blob.</span></span> <span data-ttu-id="3fc37-106">한 가지 방법은 Azure Storage Explorer를 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3fc37-106">One method is to use Azure Storage Explorer.</span></span> <span data-ttu-id="3fc37-107">이 메서드는 간단한 연결, 검색 및 다운로드를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fc37-107">This method supports simple connection, browsing and downloading.</span></span> <span data-ttu-id="3fc37-108">자세한 내용을 보려면<https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer></span><span class="sxs-lookup"><span data-stu-id="3fc37-108">For more information, visit <https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer></span></span>

1.  <span data-ttu-id="3fc37-109">내보내기 작업이 완료 된 후 콘텐츠를 다운로드 하려면 내보내기 탭으로 이동 하 여 export 작업을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fc37-109">To download content after an export job is complete, go to the Exports tab and select an export job.</span></span>

2.  <span data-ttu-id="3fc37-110">플라이 아웃의 "위치" 섹션에 있는 텍스트를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fc37-110">Copy the text in the “Locations” section of the flyout.</span></span>

![](../media/eDiscoExportJob.png)

3.  <span data-ttu-id="3fc37-111">Azure Storage Explorer를 열고 "연결" 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fc37-111">Open Azure Storage Explorer and click the “Connect” button</span></span>

![](../media/AzureStorageConnect.png)

4.  <span data-ttu-id="3fc37-112">"공유 액세스 서명 URI 사용"을 선택 하 고 다음을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fc37-112">Select “Use a shared access signature URI” and click next</span></span>

![](../media/AzureStorageConnect2.png)

5.  <span data-ttu-id="3fc37-113">URI 텍스트 상자에 위치 텍스트를 붙여넣고 다음을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fc37-113">Paste the Location text in the URI text box and click next</span></span>

![](../media/AzureStorageConnect3.png)

6.  <span data-ttu-id="3fc37-114">연결 클릭</span><span class="sxs-lookup"><span data-stu-id="3fc37-114">Click Connect</span></span>

![](../media/AzureStorageConnect4.png)

<span data-ttu-id="3fc37-115">이렇게 하면 저장소 계정/SAS 연결 서비스/Blob 컨테이너에서 내보내기 내용이 개체로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3fc37-115">This will add the export as an object in Storage Accounts/SAS-Attached Services/Blob Containers.</span></span> <span data-ttu-id="3fc37-116">내보내기를 탐색 하 고 내보내기 전체 또는 일부를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3fc37-116">You will be able to explore the export and download all or portions of the export.</span></span>

![](../media/AzureStorageConnect5.png)