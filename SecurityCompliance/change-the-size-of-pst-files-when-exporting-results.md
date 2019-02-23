---
title: eDiscovery 검색 결과를 내보낼 때 PST 파일 크기 변경
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 04e9de2d-765b-457b-a98a-d0f60bfb13f2
description: eDiscovery 검색 결과를 내보낼 때 컴퓨터로 다운로드 되는 PST 파일의 기본 크기를 변경할 수 있습니다.
ms.openlocfilehash: 8a956091f29ec1b564d3194c7e3ca2680fdeb564
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214628"
---
# <a name="change-the-size-of-pst-files-when-exporting-ediscovery-search-results"></a><span data-ttu-id="4d1cb-103">eDiscovery 검색 결과를 내보낼 때 PST 파일 크기 변경</span><span class="sxs-lookup"><span data-stu-id="4d1cb-103">Change the size of PST files when exporting eDiscovery search results</span></span>

<span data-ttu-id="4d1cb-p101">Office 365 eDiscovery 내보내기 도구를 사용 하 여 다른 Microsoft eDiscovery 도구에서 eDiscovery 검색의 전자 메일 결과를 내보낼 때 내보낼 수 있는 PST 파일의 기본 크기는 10gb입니다. 이 기본 크기를 변경 하려는 경우 검색 결과를 내보내는 데 사용 하는 컴퓨터에서 Windows 레지스트리를 편집할 수 있습니다. 이 작업을 수행 하는 한 가지 이유는 PST 파일이 DVD, 컴팩트 디스크 또는 USB 드라이브 같은 이동식 미디어에 들어갈 수 있도록 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-p101">When you use the Office 365 eDiscovery Export tool to export the email results of an eDiscovery search from the different Microsoft eDiscovery tools, the default size of a PST file that can be exported is 10 GB. If you want to change this default size, you can edit the Windows Registry on the computer that you use to export the search results. One reason to do this is so a PST file can fit on removable media, such a DVD, a compact disc, or a USB drive.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="4d1cb-107">office 365 eDiscovery 내보내기 도구는 office 365 보안 &amp; 준수 센터, Exchange online의 원본 위치 eDiscovery 및 SharePoint online의 eDiscovery 센터에서 콘텐츠 검색을 사용 하는 경우 검색 결과를 내보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-107">The Office 365 eDiscovery Export tool is used to export the search results when using Content Search in the Office 365 Security &amp; Compliance Center, In-Place eDiscovery in Exchange Online, and the eDiscovery Center in SharePoint Online.</span></span> 
  
## <a name="create-a-registry-setting-to-change-the-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="4d1cb-108">eDiscovery 검색 결과를 내보낼 때 PST 파일 크기를 변경 하는 레지스트리 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="4d1cb-108">Create a registry setting to change the size of PST files when you export eDiscovery search results</span></span>

<span data-ttu-id="4d1cb-109">eDiscovery 검색의 결과를 내보내는 데 사용할 컴퓨터에서 다음 절차를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-109">Perform the following procedure on the computer that you'll use to export the results of an eDiscovery search.</span></span>
  
1. <span data-ttu-id="4d1cb-110">Office 365 eDiscovery 내보내기 도구가 열려 있는 경우 해당 도구를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-110">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="4d1cb-111">파일 이름 접미사를 사용 하 여 windows 레지스트리 파일에 다음 텍스트를 저장 합니다. 예: PstExportSize.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-111">Save the following text to a Window registry file by using a filename suffix of .reg; for example, PstExportSize.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "PstSizeLimitInBytes"="1073741824"
    ```

    <span data-ttu-id="4d1cb-p102">위 예에서 `PstSizeLimitInBytes` 값은 1073741824 바이트 또는 약 1gb로 설정 됩니다. 다음은 `PstSizeLimitInBytes` 설정에 대 한 몇 가지 다른 예제 값입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-p102">In the example above, the  `PstSizeLimitInBytes` value is set to 1,073,741,824 bytes or approximately 1 GB. Here are some other sample values for the  `PstSizeLimitInBytes` setting.</span></span> 
    
    |<span data-ttu-id="4d1cb-114">**크기 (GB)**</span><span class="sxs-lookup"><span data-stu-id="4d1cb-114">**Size in GB (approx.)**</span></span>|<span data-ttu-id="4d1cb-115">**크기 (바이트)**</span><span class="sxs-lookup"><span data-stu-id="4d1cb-115">**Size in bytes**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="4d1cb-116">7g b (700 MB)</span><span class="sxs-lookup"><span data-stu-id="4d1cb-116">.7 GB (700 MB)</span></span>  <br/> |<span data-ttu-id="4d1cb-117">751619277</span><span class="sxs-lookup"><span data-stu-id="4d1cb-117">751619277</span></span>  <br/> |
    |<span data-ttu-id="4d1cb-118">2GB</span><span class="sxs-lookup"><span data-stu-id="4d1cb-118">2 GB</span></span>  <br/> |<span data-ttu-id="4d1cb-119">2147483648</span><span class="sxs-lookup"><span data-stu-id="4d1cb-119">2147483648</span></span>  <br/> |
    |<span data-ttu-id="4d1cb-120">4GB</span><span class="sxs-lookup"><span data-stu-id="4d1cb-120">4 GB</span></span>  <br/> |<span data-ttu-id="4d1cb-121">4294967296</span><span class="sxs-lookup"><span data-stu-id="4d1cb-121">4294967296</span></span>  <br/> |
    |<span data-ttu-id="4d1cb-122">8GB</span><span class="sxs-lookup"><span data-stu-id="4d1cb-122">8 GB</span></span>  <br/> |<span data-ttu-id="4d1cb-123">8589934592</span><span class="sxs-lookup"><span data-stu-id="4d1cb-123">8589934592</span></span>  <br/> |
   
3. <span data-ttu-id="4d1cb-124">검색 결과 `PstSizeLimitInBytes` 를 내보낼 때 값을 원하는 PST 파일의 최대 크기로 변경한 다음 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-124">Change the `PstSizeLimitInBytes` value to the desired maximum size of a PST file when you export search results, and then save the file.</span></span> 
    
4. <span data-ttu-id="4d1cb-125">Windows 탐색기에서 이전 단계에서 만든 .reg 파일을 클릭 하거나 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-125">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
5. <span data-ttu-id="4d1cb-126">사용자 액세스 제어 창에서 **예** 를 클릭 하 여 레지스트리 편집기에서 변경 작업을 수행 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-126">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
6. <span data-ttu-id="4d1cb-127">계속할지 묻는 메시지가 표시 되 면 **예**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-127">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="4d1cb-128">레지스트리 편집기에 설정이 레지스트리에 성공적으로 추가 되었다는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-128">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
7. <span data-ttu-id="4d1cb-129">3-6 단계를 반복 하 여 `PstSizeLimitInBytes` 레지스트리 설정 값을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-129">You can repeat steps 3 - 6 to change the value for the  `PstSizeLimitInBytes` registry setting.</span></span> 
  
## <a name="frequently-asked-questions-about-changing-the-default-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="4d1cb-130">eDiscovery 검색 결과를 내보낼 때 PST 파일의 기본 크기를 변경 하는 방법에 대 한 질문과 대답</span><span class="sxs-lookup"><span data-stu-id="4d1cb-130">Frequently asked questions about changing the default size of PST files when you export eDiscovery search results</span></span>

 <span data-ttu-id="4d1cb-131">**기본 크기가 10gb 인 이유는 무엇 인가요?**</span><span class="sxs-lookup"><span data-stu-id="4d1cb-131">**Why is the default size 10 GB?**</span></span>
  
<span data-ttu-id="4d1cb-132">기본 크기 10gb는 고객 의견을 기반으로 합니다. 10gb는 단일 PST에 있는 콘텐츠의 최적 정도와 파일 손상 가능성을 최소화 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-132">The default size of 10 GB was based on customer feedback; 10 GB is a good balance between the optimal amount of content in a single PST and with a minimum chance of file corruption.</span></span>
  
 <span data-ttu-id="4d1cb-133">**PST 파일의 기본 크기를 늘리거나 줄여야 하나요?**</span><span class="sxs-lookup"><span data-stu-id="4d1cb-133">**Should I increase or decrease the default size of PST files?**</span></span>
  
<span data-ttu-id="4d1cb-p103">고객은 사용자가 조직의 다른 위치를 물리적으로 배송 하는 데 사용할 수 있는 이동식 미디어에 대 한 검색 결과에 맞게 크기 제한을 줄이는 경향이 있습니다. 10mb를 초과 하는 PST 파일에 손상 문제가 있을 수 있으므로 기본 크기를 늘리지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-p103">Customers tend to decrease the size limit so that the search results will fit on removable media that they can physically ship other locations in their organization. We don't recommend that you increase the default size because PST files larger than 10 GB might have corruption issues.</span></span>
  
 <span data-ttu-id="4d1cb-136">**어떤 컴퓨터에서이 작업을 수행 해야 하나요?**</span><span class="sxs-lookup"><span data-stu-id="4d1cb-136">**What computer do I have to do this on?**</span></span>
  
<span data-ttu-id="4d1cb-137">Office 365 eDiscovery 내보내기 도구를 실행 하는 로컬 컴퓨터에서 레지스트리 설정을 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-137">You need to change the registry setting on any local computer that you run the Office 365 eDiscovery Export tool on.</span></span>
  
 <span data-ttu-id="4d1cb-138">**이 설정을 변경한 후에는 컴퓨터를 다시 부팅 해야 하나요?**</span><span class="sxs-lookup"><span data-stu-id="4d1cb-138">**After I change this setting, do I have to reboot the computer?**</span></span>
  
<span data-ttu-id="4d1cb-p104">아니요, 컴퓨터를 다시 부팅할 필요가 없습니다. 그러나 Office 365 eDiscovery 내보내기 도구를 실행 하는 경우이 설정을 변경 하 고 나면이를 닫고 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-p104">No, you don't have to reboot the computer. But, if the Office 365 eDiscovery Export tool is running, you'll have to close it and the restart it after you change this setting.</span></span>
  
 <span data-ttu-id="4d1cb-141">**기존 레지스트리 키를 편집 하거나 새 키를 만들기 시작 합니까?**</span><span class="sxs-lookup"><span data-stu-id="4d1cb-141">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="4d1cb-p105">이 절차에서 만든 .reg 파일을 처음 실행할 때 새 레지스트리 키가 만들어집니다. 그런 다음 .reg 편집 파일을 변경 하 고 다시 실행할 때마다 설정이 편집 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-p105">A new registry key is created the first time you run the .reg file that you created in this procedure. Then the setting is edited each time you change and re-run the .reg edit file.</span></span>
