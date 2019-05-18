---
title: 보유자 데이터의 고급 인덱싱
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
description: ''
ms.openlocfilehash: be163d3272dbe027cb0f4b4b4fe379bf28fa5a85
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151760"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="1233e-102">보유자 데이터의 고급 인덱싱</span><span class="sxs-lookup"><span data-stu-id="1233e-102">Advanced indexing of custodian data</span></span>

<span data-ttu-id="1233e-103">고급 eDiscovery 사례에 custodian을 추가 하면 부분적으로 인덱싱된 것으로 간주 되는 Office 365의 콘텐츠가 완벽 하 게 검색 가능 하도록 다시 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1233e-103">When a custodian is added to an Advanced eDiscovery case, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.</span></span>  <span data-ttu-id="1233e-104">이 프로세스를 *고급 인덱싱*이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1233e-104">This process is called *Advanced indexing*.</span></span> <span data-ttu-id="1233e-105">이미지의 존재 여부, 지원 되지 않는 파일 형식 또는 파일 크기 제한에 도달 하는 경우에는 여러 가지 이유로 인해 콘텐츠를 부분적으로 인덱싱할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1233e-105">Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.</span></span>

<span data-ttu-id="1233e-106">Office 365 및 부분적으로 인덱싱된 항목의 처리 지원에 대 한 자세한 내용은 다음을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1233e-106">To learn more about processing support in Office 365 and partially indexed items, see:</span></span>

- [<span data-ttu-id="1233e-107">고급 eDiscovery에서 지원 되는 파일 형식</span><span class="sxs-lookup"><span data-stu-id="1233e-107">Supported file types in Advanced eDiscovery</span></span>](supported-filetypes-ediscovery20.md)
- [<span data-ttu-id="1233e-108">Office 365의 콘텐츠 검색에서 부분적으로 인덱싱된 항목</span><span class="sxs-lookup"><span data-stu-id="1233e-108">Partially indexed items in Content Search in Office 365</span></span>](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search)
- [<span data-ttu-id="1233e-109">Exchange 검색에서 인덱싱하는 파일 형식</span><span class="sxs-lookup"><span data-stu-id="1233e-109">File formats indexed by Exchange Search</span></span>](https://docs.microsoft.com/en-us/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)
- [<span data-ttu-id="1233e-110">SharePoint Server의 크롤링되는 기본 파일 이름 확장명 및 구문 분석되는 파일 형식</span><span class="sxs-lookup"><span data-stu-id="1233e-110">Default crawled file name extensions and parsed file types in SharePoint Server</span></span>](https://docs.microsoft.com/en-us/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="1233e-111">고급 인덱싱 결과 보기</span><span class="sxs-lookup"><span data-stu-id="1233e-111">Viewing Advanced indexing results</span></span>

<span data-ttu-id="1233e-112">고급 인덱싱 프로세스가 완료 되 면 다시 처리할 때의 효과를 이해 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1233e-112">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.</span></span>  <span data-ttu-id="1233e-113">Custodian 인덱싱 보기에서 그래프에는 *하이브리드 인덱스*에 추가 된 모든 항목이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1233e-113">In the Custodian Indexing view, the graph lists all items added to the *hybrid index*.</span></span>  <span data-ttu-id="1233e-114">하이브리드 인덱스는 고급 eDiscovery가 다시 처리 된 콘텐츠를 저장 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1233e-114">The hybrid index is where Advanced eDiscovery stores the re-processed content.</span></span>

<span data-ttu-id="1233e-115">또한 그래프에는 수정이 필요한 항목 수와 파일 형식별로 다른 오류 그래프가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1233e-115">The graph also includes the number of items that require remediation and another graph of errors by file type.</span></span> <span data-ttu-id="1233e-116">자세한 내용은 [데이터를 처리할 때 오류 수정을](error-remediation.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1233e-116">For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-custodians"></a><span data-ttu-id="1233e-117">Custodians에 대 한 고급 인덱스 업데이트</span><span class="sxs-lookup"><span data-stu-id="1233e-117">Updating Advanced indexes for custodians</span></span>

<span data-ttu-id="1233e-118">고급 eDiscovery 사례에 custodian을 추가 하면 부분적으로 인덱싱된 항목이 모두 다시 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1233e-118">When a custodian is added to an Advanced eDiscovery case, all partially indexed items are re-processed.</span></span> <span data-ttu-id="1233e-119">그러나 시간 경과에 따라 보다 부분적으로 인덱싱된 항목이 사용자의 사서함 또는 OneDrive 계정에 추가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1233e-119">However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.</span></span>  <span data-ttu-id="1233e-120">필요한 경우 인덱스를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1233e-120">When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="1233e-121">Custodian 인덱스를 업데이트 하는 과정은 장기 실행 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="1233e-121">Updating custodian indexes is a long running process.</span></span> <span data-ttu-id="1233e-122">인덱스를 하루에 한 번 이상 업데이트 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1233e-122">It's recommended that you don't update indexes more than once per day in a case.</span></span>
