---
title: 보유자 데이터의 고급 인덱싱
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: f8f1a92f001bf8f9e23f54bbb05fbbcf443bf4b9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218668"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="1f06a-102">보유자 데이터의 고급 인덱싱</span><span class="sxs-lookup"><span data-stu-id="1f06a-102">Advanced indexing of custodian data</span></span>

<span data-ttu-id="1f06a-p101">고급 eDiscovery (미리 보기) 사례에 custodian을 추가 하면 부분적으로 인덱싱된 것으로 간주 되는 Office 365의 콘텐츠가 완전히 검색 가능 하도록 다시 처리 됩니다.  이 프로세스를 *고급 인덱싱*이라고 합니다. 이미지의 존재 여부, 지원 되지 않는 파일 형식 또는 파일 크기 제한에 도달 하는 경우에는 여러 가지 이유로 인해 콘텐츠를 부분적으로 인덱싱할 수 있습니다.  부분적으로 인덱싱된 항목에 대 한 자세한 내용은 [Office 365의 콘텐츠 검색에서 부분적으로 인덱싱된 항목](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f06a-p101">When a custodian is added to an Advanced eDiscovery (Preview) case, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.  This process is called *Advanced indexing*. Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.  To learn more about partially indexed items, see [Partially indexed items in Content Search in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span></span>

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="1f06a-107">고급 인덱싱 결과 보기</span><span class="sxs-lookup"><span data-stu-id="1f06a-107">Viewing Advanced indexing results</span></span>

<span data-ttu-id="1f06a-p102">고급 인덱싱 프로세스가 완료 되 면 다시 처리할 때의 효과를 이해 하는 데 도움이 될 수 있습니다.  Custodian 인덱싱 보기에서 그래프에는 *하이브리드 인덱스*에 추가 된 모든 항목이 나열 됩니다.  하이브리드 인덱스는 고급 eDiscovery (미리 보기)에서 다시 처리 된 콘텐츠가 저장 되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1f06a-p102">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.  In the Custodian Indexing view, the graph lists all items added to the *hybrid index*.  The hybrid index is where Advanced eDiscovery (Preview) stores the re-processed content.</span></span>

<span data-ttu-id="1f06a-p103">또한 그래프에는 수정이 필요한 항목 수와 파일 형식별로 다른 오류 그래프가 포함 되어 있습니다. 자세한 내용은 [데이터를 처리할 때 오류 수정을](error-remediation.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1f06a-p103">The graph also includes the number of items that require remediation and another graph of errors by file type. For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-custodians"></a><span data-ttu-id="1f06a-113">custodians에 대 한 고급 인덱스 업데이트</span><span class="sxs-lookup"><span data-stu-id="1f06a-113">Updating Advanced indexes for custodians</span></span>

<span data-ttu-id="1f06a-p104">고급 eDiscovery (미리 보기) 케이스에 custodian을 추가 하면 부분적으로 인덱싱된 항목이 모두 다시 처리 됩니다. 그러나 시간 경과에 따라 보다 부분적으로 인덱싱된 항목이 사용자의 사서함 또는 OneDrive 계정에 추가 될 수 있습니다.  필요한 경우 인덱스를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f06a-p104">When a custodian is added to an Advanced eDiscovery (Preview) case, all partially indexed items are re-processed. However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.  When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="1f06a-p105">custodian 인덱스를 업데이트 하는 과정은 장기 실행 프로세스입니다. 인덱스를 하루에 한 번 이상 업데이트 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1f06a-p105">Updating custodian indexes is a long running process. It's recommended that you don't update indexes more than once per day in a case.</span></span>
