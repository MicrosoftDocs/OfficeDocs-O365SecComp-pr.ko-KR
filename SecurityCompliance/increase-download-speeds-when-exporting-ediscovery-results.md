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
ms.openlocfilehash: 36a4f1766f3ac0108d1829c93cfca63bc5cf09f5
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000921"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a><span data-ttu-id="f4f9c-103">Office 365에서 eDiscovery 검색 결과를 내보낼 때 다운로드 속도 높이기</span><span class="sxs-lookup"><span data-stu-id="f4f9c-103">Increase the download speed when exporting eDiscovery search results from Office 365</span></span>

<span data-ttu-id="f4f9c-104">office 365 eDiscovery 내보내기 도구를 사용 하 여 Security & 준수 센터에서 콘텐츠 검색 결과를 다운로드 하거나 office 365 Advanced eDiscovery에서 데이터를 다운로드 하면이 도구는 다운로드 하기 위해 특정 개수의 동시 내보내기 작업을 시작 합니다. 로컬 컴퓨터에 데이터를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-104">When you use the Office 365 eDiscovery Export tool to download the results of a Content Search in the Security & Compliance Center or download data from Office 365 Advanced eDiscovery, the tool starts a certain number of concurrent export operations to download the data to your local computer.</span></span> <span data-ttu-id="f4f9c-105">기본적으로 동시 작업의 수는 데이터를 다운로드 하는 데 사용 하는 컴퓨터의 코어 수의 8 배로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-105">By default, the number of concurrent operations is set to 8 times the number of cores in the computer you're using to download the data.</span></span> <span data-ttu-id="f4f9c-106">예를 들어 이중 코어 컴퓨터 (칩 하나에 두 개의 중앙 처리 장치)가 있는 경우 기본 동시 내보내기 작업 수는 16 개입니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-106">For example, if you have a dual core computer (meaning two central processing units on one chip), the default number of concurrent export operations is 16.</span></span> <span data-ttu-id="f4f9c-107">데이터 전송 처리량을 늘리기 위해 다운로드 프로세스의 속도를 높이려면 검색 결과를 다운로드 하는 데 사용 하는 컴퓨터에서 Windows 레지스트리 설정을 구성 하 여 동시 작업 수를 늘릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-107">To increase the data transfer throughput and speed-up the download process, you can increase the number of concurrent operations by configuring a Windows Registry setting on the computer that you use to download the search results.</span></span> <span data-ttu-id="f4f9c-108">다운로드 프로세스의 속도를 향상 시키려면 24 개의 동시 작업을 설정 하는 것으로 시작 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-108">To speed-up the download process, we recommend that you start with a setting of 24 concurrent operations.</span></span>
  
<span data-ttu-id="f4f9c-109">낮은 대역폭의 네트워크를 통해 검색 결과를 다운로드 하는 경우이 설정을 높이면 부정적인 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-109">If you download search results over a low-bandwidth network, increasing this setting might have a negative impact.</span></span> <span data-ttu-id="f4f9c-110">또는 고대역폭 네트워크에서 24 개 보다 많은 동시 작업을 설정할 수 있습니다 (최대 동시 작업 수는 512).</span><span class="sxs-lookup"><span data-stu-id="f4f9c-110">Alternatively, you might be able to increase the setting to more than 24 concurrent operations in a high-bandwidth network (the maximum number of concurrent operations is 512).</span></span> <span data-ttu-id="f4f9c-111">이 레지스트리 설정을 구성한 후에는 환경에 대 한 최적의 동시 작업 수를 찾기 위해 변경 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-111">After you configure this registry setting, you might have to change it to find the optimal number of concurrent operations for your environment.</span></span>
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a><span data-ttu-id="f4f9c-112">레지스트리 설정 만들기 데이터를 내보낼 때 동시 작업 수를 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="f4f9c-112">Create a registry setting to change the number of concurrent operations when exporting data</span></span>

<span data-ttu-id="f4f9c-113">보안 & 준수 센터에서 검색 결과를 다운로드 하는 데 사용 하는 컴퓨터에서 다음 절차를 수행 하거나 고급 eDiscovery에서 데이터를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-113">Perform the following procedure on the computer that you'll use to download search results from the Security & Compliance Center or data from Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="f4f9c-114">Office 365 eDiscovery 내보내기 도구가 열려 있는 경우 해당 도구를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-114">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="f4f9c-115">파일 이름 접미사를 사용 하 여 windows 레지스트리 파일에 다음 텍스트를 저장 합니다. 예: ConcurrentOperations.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-115">Save the following text to a Window registry file by using a filename suffix of .reg; for example, ConcurrentOperations.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    <span data-ttu-id="f4f9c-116">앞에서 설명한 것 처럼 24 개의 동시 작업을 시작 하 고 적절 하 게이 설정을 변경 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-116">As previous explained, we recommend that you start with 24 concurrent operations, and then change this setting as appropriate.</span></span>
    
3. <span data-ttu-id="f4f9c-117">Windows 탐색기에서 이전 단계에서 만든 .reg 파일을 클릭 하거나 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-117">In Windows Explorer, click or double-click the .reg file that you created in the previous step.</span></span>
    
4. <span data-ttu-id="f4f9c-118">사용자 액세스 제어 창에서 **예** 를 클릭 하 여 레지스트리 편집기에서 변경 작업을 수행 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-118">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="f4f9c-119">계속할지 묻는 메시지가 표시 되 면 **예**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-119">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="f4f9c-120">레지스트리 편집기에 설정이 레지스트리에 성공적으로 추가 되었다는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-120">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
6. <span data-ttu-id="f4f9c-121">2-5 단계를 반복 하 여 `DownloadConcurrency` 레지스트리 설정 값을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-121">You can repeat steps 2 - 5 to change the value for the  `DownloadConcurrency` registry setting.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="f4f9c-122">`DownloadConcurrency` 레지스트리 설정을 만들거나 변경한 후에는 새 내보내기 작업을 만들거나 다운로드 하려는 검색 결과 또는 데이터에 대 한 기존 내보내기 작업을 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-122">After you create or change the  `DownloadConcurrency` registry setting, be sure to create a new export job or restart an existing export job for the search results or data that you want to download.</span></span> <span data-ttu-id="f4f9c-123">자세한 [내용은 추가 정보](#more-information) 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-123">See the [More information](#more-information) section for more details.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="f4f9c-124">추가 정보</span><span class="sxs-lookup"><span data-stu-id="f4f9c-124">More information</span></span>

- <span data-ttu-id="f4f9c-125">이 절차에서 만든 .reg 파일을 처음 실행할 때 새 레지스트리 키가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-125">A new registry key is created the first time you run the .reg file that you created in this procedure.</span></span> <span data-ttu-id="f4f9c-126">그런 다음 `DownloadConcurrency` .reg 편집 파일을 변경 하 고 다시 실행할 때마다 레지스트리 설정이 편집 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-126">Then the  `DownloadConcurrency` registry setting is edited each time you change and re-run the .reg edit file.</span></span> 
    
- <span data-ttu-id="f4f9c-127">Office 365 eDiscovery 내보내기 도구는 [Azure AzCopy 유틸리티](https://go.microsoft.com/fwlink/?linkid=849949) 를 사용 하 여 보안 & 준수 센터 또는 고급 eDiscovery에서 검색 데이터를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-127">The Office 365 eDiscovery Export tool uses the [Azure AzCopy utility](https://go.microsoft.com/fwlink/?linkid=849949) to download search data from the Security & Compliance Center or from Advanced eDiscovery.</span></span> <span data-ttu-id="f4f9c-128">`DownloadConcurrency` 레지스트리 설정을 구성 하는 것은 AzCopy 유틸리티를 실행할 때 **/tnc** 매개 변수를 사용 하는 것과 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-128">Configuring the  `DownloadConcurrency` registry setting is similar to using the **/NC** parameter when running the AzCopy utility.</span></span> <span data-ttu-id="f4f9c-129">따라서 레지스트리 설정은 `"DownloadConcurrency=24"` AzCopy 유틸리티 `/NC:24` 와 매개 변수 값을 함께 사용 하는 것과 같은 기능을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-129">So the registry setting of  `"DownloadConcurrency=24"` would have the same effect as using the parameter value of  `/NC:24` with the AzCopy utility.</span></span> 
    
- <span data-ttu-id="f4f9c-130">현재 진행 중인 내보내기 다운로드를 중지 한 후 다시 시작 하 여 검색 결과를 다시 다운로드 하면 Office 365 eDiscovery 내보내기 도구가 동일한 다운로드를 다시 시작 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-130">If you stop an export download that's currently in progress and then restart it (by trying to download the search results again), the Office 365 eDiscovery Export tool will attempt to resume the same download.</span></span> <span data-ttu-id="f4f9c-131">따라서 다운로드를 시작 하 고, 중지 하 고, `DownloadConcurrency` 레지스트리 설정을 변경 하는 경우 **내보낸 결과 다운로드**를 클릭 하 여 다운로드를 다시 시작 하면 다운로드가 실패할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-131">So, if you start a download, stop it, and then change the  `DownloadConcurrency` registry setting, the download will probably fail if you restart it (by clicking **Download exported results**).</span></span> <span data-ttu-id="f4f9c-132">이는 내보내기 도구가 레지스트리 설정을 변경한 후에도 유효 하지 않은 설정을 사용 하 여 이전 다운로드를 다시 시작 하려고 하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-132">This is because the export tool will attempt to resume the previous download using settings that aren't valid because you changed the registry setting.</span></span>
    
    <span data-ttu-id="f4f9c-133">따라서 `DownloadConcurrency` 레지스트리 설정을 변경한 후에는 Security & 준수 센터에서 내보내기 **다시 시작**을 클릭 하 여 내보내기 작업을 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-133">Therefore, after you change the  `DownloadConcurrency` registry setting, be sure to restart the export job (by clicking **Restart export**) in the Security & Compliance Center.</span></span> <span data-ttu-id="f4f9c-134">그런 다음 내보낸 결과를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-134">Then you can download the exported results.</span></span> <span data-ttu-id="f4f9c-135">검색 결과 및 데이터를 내보내는 방법에 대 한 자세한 내용은 다음을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f4f9c-135">For more information about exporting search results and data, see:</span></span>
    
  - [<span data-ttu-id="f4f9c-136">콘텐츠 검색 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="f4f9c-136">Export Content Search results</span></span>](export-search-results.md)
    
  - [<span data-ttu-id="f4f9c-137">Office 365 Advanced eDiscovery에서 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="f4f9c-137">Export results in Office 365 Advanced eDiscovery</span></span>](export-results-in-advanced-ediscovery.md)
    
