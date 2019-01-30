---
title: 고급 더불어 데이터의 색인
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 158af8acf4acdb8ad6650c377a23b44ed28c6f54
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608104"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="d3ac8-102">고급 더불어 데이터의 색인</span><span class="sxs-lookup"><span data-stu-id="d3ac8-102">Advanced indexing of custodian data</span></span>

<span data-ttu-id="d3ac8-p101">더불어 (미리 보기) 고급 eDiscovery 사례에 추가 되 면으로 것으로 간주 된는 Office 365에 있는 콘텐츠 부분적으로 인덱싱된 완벽 하 게 검색할 수 있도록 설정 하려면 다시 처리은입니다.  이 프로세스에는 *고급 색인*라고 합니다. 이미지, 지원 되지않는 파일 형식 또는 인덱싱 파일 크기 제한 발생 한 경우의 존재 여부를 포함 하는 이유 수에 대 한 콘텐츠를 부분적으로 인덱싱할 수 있습니다.  부분적으로 인덱싱된 항목에 대 한 자세한 내용은, [부분적으로 인덱싱된 되는 Office 365에서 콘텐츠 검색에서 항목을](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search)참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ac8-p101">When a custodian is added to an Advanced eDiscovery (Preview) case, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.  This process is called *Advanced indexing*. Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.  To learn more about partially indexed items, see [Partially indexed items in Content Search in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span></span>

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="d3ac8-107">고급 인덱싱 결과 보기</span><span class="sxs-lookup"><span data-stu-id="d3ac8-107">Viewing Advanced indexing results</span></span>

<span data-ttu-id="d3ac8-p102">고급 인덱싱 프로세스를 완료 한 후 다시 처리의 효과 대 한 이해를 얻을 수 있습니다.  더불어 인덱싱 보기 그래프 *하이브리드 인덱스*에 추가 하는 모든 항목을 나열 합니다.  하이브리드 인덱스가 고급 eDiscovery (미리 보기) 다시 처리 된 콘텐츠를 저장 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d3ac8-p102">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.  In the Custodian Indexing view, the graph lists all items added to the *hybrid index*.  The hybrid index is where Advanced eDiscovery (Preview) stores the re-processed content.</span></span>

<span data-ttu-id="d3ac8-p103">그래프에는 복구를 필요로 하는 항목 수 및 오류 파일 형식에 따라 다른 그래프도 포함 됩니다. 자세한 내용은 [데이터를 처리할 때 오류 수정](error-remediation.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d3ac8-p103">The graph also includes the number of items that require remediation and another graph of errors by file type. For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-custodians"></a><span data-ttu-id="d3ac8-113">Custodians에 대 한 고급 인덱스를 업데이트</span><span class="sxs-lookup"><span data-stu-id="d3ac8-113">Updating Advanced indexes for custodians</span></span>

<span data-ttu-id="d3ac8-p104">(미리 보기) 고급 eDiscovery 사례에는 더불어를 추가 하는 경우 모든 부분적으로 인덱싱된 항목을 다시 처리. 그러나 시간이 지남에 따라 부분적으로 더 인덱싱된 항목 사용자의 사서함 또는 OneDrive 계정에 추가 될 수 있습니다.  필요에 따라 인덱스를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3ac8-p104">When a custodian is added to an Advanced eDiscovery (Preview) case, all partially indexed items are re-processed. However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.  When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="d3ac8-p105">장기 실행 프로세스는 더불어 인덱스를 업데이트 합니다. 업데이트 하지 않으면 인덱스 두번 이상 경우에 하루 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d3ac8-p105">Updating custodian indexes is a long running process. It's recommended that you don't update indexes more than once per day in a case.</span></span>
