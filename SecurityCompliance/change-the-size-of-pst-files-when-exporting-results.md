---
title: EDiscovery 검색 결과 내보낼 때 PST 파일의 크기를 변경 합니다.
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 04e9de2d-765b-457b-a98a-d0f60bfb13f2
description: EDiscovery 검색 결과 내보낼 때 사용자 컴퓨터에 다운로드 하는 PST 파일의 기본 크기를 변경할 수 있습니다.
ms.openlocfilehash: c01f05a02fd94941eb2eb7a05b4c84ffecec9b39
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522249"
---
# <a name="change-the-size-of-pst-files-when-exporting-ediscovery-search-results"></a><span data-ttu-id="88825-103">EDiscovery 검색 결과 내보낼 때 PST 파일의 크기를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="88825-103">Change the size of PST files when exporting eDiscovery search results</span></span>

<span data-ttu-id="88825-p101">Office 365 eDiscovery 내보내기 도구를 사용 하 여 다양 한 Microsoft eDiscovery 도구에서 eDiscovery 검색의 전자 메일 결과 내보내려면를 내보낼 수 있는 PST 파일의 기본 크기는 10GB입니다. 이 기본 크기를 변경 하려는 경우에 검색 결과 내보내는 데 사용 하는 컴퓨터에서 Windows 레지스트리를 편집할 수 있습니다. PST 파일을 이동식 미디어, DVD를, 컴팩트 디스크 또는 USB 드라이브에 맞출 수 있는 이므로이 작업을 수행 하는 한 가지 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="88825-p101">When you use the Office 365 eDiscovery Export tool to export the email results of an eDiscovery search from the different Microsoft eDiscovery tools, the default size of a PST file that can be exported is 10 GB. If you want to change this default size, you can edit the Windows Registry on the computer that you use to export the search results. One reason to do this is so a PST file can fit on removable media, such a DVD, a compact disc, or a USB drive.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="88825-107">Office 365 eDiscovery 내보내기 도구는 Office 365 보안에서 콘텐츠 검색을 사용 하는 경우 검색 결과 내보내는 데 &amp; 준수 센터, Exchange Online에서 원본 위치 eDiscovery 및 SharePoint Online에서 eDiscovery 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="88825-107">The Office 365 eDiscovery Export tool is used to export the search results when using Content Search in the Office 365 Security &amp; Compliance Center, In-Place eDiscovery in Exchange Online, and the eDiscovery Center in SharePoint Online.</span></span> 
  
## <a name="create-a-registry-setting-to-change-the-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="88825-108">EDiscovery 검색 결과 내보낼 때 PST 파일의 크기를 변경 하는 레지스트리 설정을 만들기</span><span class="sxs-lookup"><span data-stu-id="88825-108">Create a registry setting to change the size of PST files when you export eDiscovery search results</span></span>

<span data-ttu-id="88825-109">EDiscovery 검색의 결과 내보내는 데 사용할 수 있는 컴퓨터에서 다음 절차를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="88825-109">Perform the following procedure on the computer that you'll use to export the results of an eDiscovery search.</span></span>
  
1. <span data-ttu-id="88825-110">열려 있으면 Office 365 eDiscovery 내보내기 도구를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="88825-110">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="88825-111">.Reg; filename 접미사를 사용 하 여 창 레지스트리 파일에 다음 텍스트를 저장 예: PstExportSize.reg 합니다.</span><span class="sxs-lookup"><span data-stu-id="88825-111">Save the following text to a Window registry file by using a filename suffix of .reg; for example, PstExportSize.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "PstSizeLimitInBytes"="1073741824"
    ```

    <span data-ttu-id="88825-p102">위의 예제는 `PstSizeLimitInBytes` 값이 1,073,741,824 바이트 또는 약 1GB로 설정 합니다. 다음에 대 한 다른 샘플 값은는 `PstSizeLimitInBytes` 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88825-p102">In the example above, the  `PstSizeLimitInBytes` value is set to 1,073,741,824 bytes or approximately 1 GB. Here are some other sample values for the  `PstSizeLimitInBytes` setting.</span></span> 
    
    |<span data-ttu-id="88825-114">**Gb에서 크기 조정 (약)**</span><span class="sxs-lookup"><span data-stu-id="88825-114">**Size in GB (approx.)**</span></span>|<span data-ttu-id="88825-115">**크기 (바이트)**</span><span class="sxs-lookup"><span data-stu-id="88825-115">**Size in bytes**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="88825-116">.7 G B (700 MB)</span><span class="sxs-lookup"><span data-stu-id="88825-116">.7 GB (700 MB)</span></span>  <br/> |<span data-ttu-id="88825-117">751619277</span><span class="sxs-lookup"><span data-stu-id="88825-117">751619277</span></span>  <br/> |
    |<span data-ttu-id="88825-118">2GB</span><span class="sxs-lookup"><span data-stu-id="88825-118">2 GB</span></span>  <br/> |<span data-ttu-id="88825-119">2147483648</span><span class="sxs-lookup"><span data-stu-id="88825-119">2147483648</span></span>  <br/> |
    |<span data-ttu-id="88825-120">4GB</span><span class="sxs-lookup"><span data-stu-id="88825-120">4 GB</span></span>  <br/> |<span data-ttu-id="88825-121">4294967296</span><span class="sxs-lookup"><span data-stu-id="88825-121">4294967296</span></span>  <br/> |
    |<span data-ttu-id="88825-122">8GB</span><span class="sxs-lookup"><span data-stu-id="88825-122">8 GB</span></span>  <br/> |<span data-ttu-id="88825-123">8589934592</span><span class="sxs-lookup"><span data-stu-id="88825-123">8589934592</span></span>  <br/> |
   
3. <span data-ttu-id="88825-124">변경 된 `PstSizeLimitInBytes` PST 파일로 검색 결과 내보내기 하 고 다음 파일을 저장 하는 경우의 원하는 최대 크기는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="88825-124">Change the `PstSizeLimitInBytes` value to the desired maximum size of a PST file when you export search results, and then save the file.</span></span> 
    
4. <span data-ttu-id="88825-125">Windows 탐색기에서를 클릭 하거나 이전 단계에서 만든.reg 파일을 두번클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="88825-125">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
5. <span data-ttu-id="88825-126">사용자 액세스 제어 창에서 **예** 는 변경 내용을 적용 하 여 레지스트리 편집기를 하도록 하려면이 옵션을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="88825-126">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
6. <span data-ttu-id="88825-127">를 계속 하 라는 메시지가 나타나면 **예**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="88825-127">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="88825-128">레지스트리 편집기 설정을 레지스트리에 성공적으로 추가 된 했다는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="88825-128">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
7. <span data-ttu-id="88825-129">에 대 한 값을 변경 하려면 3-6 단계를 반복 하 수는 `PstSizeLimitInBytes` 레지스트리 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88825-129">You can repeat steps 3 - 6 to change the value for the  `PstSizeLimitInBytes` registry setting.</span></span> 
  
## <a name="frequently-asked-questions-about-changing-the-default-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="88825-130">EDiscovery 검색 결과 내보낼 때 PST 파일의 기본 크기를 변경 하는 방법에 대 한 질문과 대답</span><span class="sxs-lookup"><span data-stu-id="88825-130">Frequently asked questions about changing the default size of PST files when you export eDiscovery search results</span></span>

 <span data-ttu-id="88825-131">**기본 이유는 크기 조정 10GB?**</span><span class="sxs-lookup"><span data-stu-id="88825-131">**Why is the default size 10 GB?**</span></span>
  
<span data-ttu-id="88825-132">고객 의견;에 10GB의 기본 크기를 기준 10GB 최적의 단일 PST 나 파일 손상의 최소 기회를 사용 하 여 콘텐츠의 양 간에 적절 한 균형입니다.</span><span class="sxs-lookup"><span data-stu-id="88825-132">The default size of 10 GB was based on customer feedback; 10 GB is a good balance between the optimal amount of content in a single PST and with a minimum chance of file corruption.</span></span>
  
 <span data-ttu-id="88825-133">**증가 또는 PST 파일의 기본 크기 줄이기 해야 합니까?**</span><span class="sxs-lookup"><span data-stu-id="88825-133">**Should I increase or decrease the default size of PST files?**</span></span>
  
<span data-ttu-id="88825-p103">고객 조직에서 다른 위치 제공 물리적으로 수 있는 이동식 미디어에 검색 결과 나타낼 수 있도록 크기 제한을 감소 하는 경향이 있습니다. PST 파일을 10GB 손상 문제가 있을 것 보다 더 큰 때문에 기본 크기를 늘리면 하지 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="88825-p103">Customers tend to decrease the size limit so that the search results will fit on removable media that they can physically ship other locations in their organization. We don't recommend that you increase the default size because PST files larger than 10 GB might have corruption issues.</span></span>
  
 <span data-ttu-id="88825-136">**이 작업을 수행에서 어떤 컴퓨터 해야 합니까?**</span><span class="sxs-lookup"><span data-stu-id="88825-136">**What computer do I have to do this on?**</span></span>
  
<span data-ttu-id="88825-137">Office 365 eDiscovery 내보내기 도구를 실행 하는 모든 로컬 컴퓨터에서 레지스트리 설정을 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="88825-137">You need to change the registry setting on any local computer that you run the Office 365 eDiscovery Export tool on.</span></span>
  
 <span data-ttu-id="88825-138">**이 설정은 변경 후 컴퓨터를 재부팅 해야 합니까?**</span><span class="sxs-lookup"><span data-stu-id="88825-138">**After I change this setting, do I have to reboot the computer?**</span></span>
  
<span data-ttu-id="88825-p104">아니요, 컴퓨터를 다시 부팅 필요가 없습니다. 하지만를 닫으려면 하 고 다시 시작 해야 Office 365 eDiscovery 내보내기 도구를 실행 하는 경우이 설정을 변경한 후 것입니다.</span><span class="sxs-lookup"><span data-stu-id="88825-p104">No, you don't have to reboot the computer. But, if the Office 365 eDiscovery Export tool is running, you'll have to close it and the restart it after you change this setting.</span></span>
  
 <span data-ttu-id="88825-141">**기존 레지스트리 키 편집 가져오기 또는 않는 새 키를 만든 가져올?**</span><span class="sxs-lookup"><span data-stu-id="88825-141">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="88825-p105">새 레지스트리 키에는이 절차에서 만든.reg 파일을 실행 하는 처음으로 만들어집니다. 다음 설정은 변경 하 고 편집.reg 파일을 다시 실행 때마다 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="88825-p105">A new registry key is created the first time you run the .reg file that you created in this procedure. Then the setting is edited each time you change and re-run the .reg edit file.</span></span>
