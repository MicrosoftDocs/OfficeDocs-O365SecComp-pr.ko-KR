---
title: Office 365 보안 &amp; 및 준수 센터에서 콘텐츠 검색 결과를 내보낼 때 보고서를 사용 하지 않도록 설정
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: c9b0ff0c-282b-4a44-b43f-cfc5b96557f9
description: 로컬 컴퓨터에서 Windows 레지스트리를 편집 하 여 Office 365 Security &amp; Comliance Center에서 콘텐츠 검색 결과를 내보낼 때 보고서를 사용 하지 않도록 설정 합니다. 이러한 보고서를 사용 하지 않도록 설정 하면 다운로드 시간을 단축 하 고 디스크 공간을 절약할 수 있습니다.
ms.openlocfilehash: f08f5e7143022591d38bda787301e71ae80fb3d3
ms.sourcegitcommit: 8a65a29aa3bfe5dcad0ff152a7cd795e02877dd9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/28/2019
ms.locfileid: "30936718"
---
# <a name="disable-reports-when-you-export-content-search-results-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="13770-104">Office 365 보안 &amp; 및 준수 센터에서 콘텐츠 검색 결과를 내보낼 때 보고서를 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="13770-104">Disable reports when you export Content Search results in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="13770-105">Office 365 eDiscovery 내보내기 도구를 사용 하 여 보안 &amp; 및 준수 센터에서 콘텐츠 검색 결과를 내보낼 때이 도구는 내보낸 콘텐츠에 대 한 추가 정보가 포함 된 두 개의 보고서를 자동으로 만들고 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="13770-105">When you use the Office 365 eDiscovery Export tool to export the results of a Content Search in the Security &amp; Compliance Center, the tool automatically creates and exports two reports that contain additional information about the exported content.</span></span> <span data-ttu-id="13770-106">이러한 보고서는 결과. .csv 파일 및 manifest.xml 파일 (이러한 보고서에 대 한 자세한 설명을 보려면이 항목의 [보고서 내보내기 비활성화에 대 한 질문과 대답](#frequently-asked-questions-about-disabling-export-reports) 섹션 참조)이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13770-106">These reports are the Results.csv file and the Manifest.xml file (see the [Frequently asked questions about disabling export reports](#frequently-asked-questions-about-disabling-export-reports) section in this topic for detailed descriptions of these reports).</span></span> <span data-ttu-id="13770-107">이러한 파일은 매우 커질 수 있으므로 다운로드 시간을 단축 하 고 이러한 파일을 내보내지 못하게 하 여 디스크 공간을 절약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13770-107">Because these files can be very large, you can speed up the download time and save disk space by preventing these files from being exported.</span></span> <span data-ttu-id="13770-108">검색 결과를 내보내는 데 사용 하는 컴퓨터에서 Windows 레지스트리를 변경 하 여이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13770-108">You can do this by changing the Windows Registry on the computer that you use to export the search results.</span></span> <span data-ttu-id="13770-109">나중에 보고서를 포함 하려면 레지스트리 설정을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13770-109">If you want to include the reports at a later time, you can edit the registry setting.</span></span> 
  
## <a name="create-registry-settings-to-disable-the-export-reports"></a><span data-ttu-id="13770-110">레지스트리 설정을 만들어 내보내기 보고서를 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="13770-110">Create registry settings to disable the export reports</span></span>

<span data-ttu-id="13770-111">결과를 콘텐츠 검색으로 내보내기 위해 사용 하는 컴퓨터에서 다음 절차를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-111">Perform the following procedure on the computer that you'll use to export the results a content search.</span></span>
  
1. <span data-ttu-id="13770-112">Office 365 eDiscovery 내보내기 도구가 열려 있는 경우 해당 도구를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="13770-112">Close the Office 365 eDiscovery Export tool if it's open.</span></span>
    
2. <span data-ttu-id="13770-113">사용 하지 않도록 설정할 내보내기 보고서에 따라 다음 단계 중 하나 또는 두 가지를 모두 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-113">Perform one or both of the following steps, depending on which export report you want to disable.</span></span>
    
    - <span data-ttu-id="13770-114">**결과 .csv**</span><span class="sxs-lookup"><span data-stu-id="13770-114">**Results.csv**</span></span>
    
      <span data-ttu-id="13770-115">파일 이름 접미사를 사용 하 여 Windows 레지스트리 파일에 다음 텍스트를 저장 합니다. 예: DisableResultsCsv.</span><span class="sxs-lookup"><span data-stu-id="13770-115">Save the following text to a Windows registry file by using a filename suffix of .reg; for example, DisableResultsCsv.reg.</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d False 
      ```

    - <span data-ttu-id="13770-116">**manifest.xml**</span><span class="sxs-lookup"><span data-stu-id="13770-116">**Manifest.xml**</span></span>
    
      <span data-ttu-id="13770-117">파일 이름 접미사를 사용 하 여 Windows 레지스트리 파일에 다음 텍스트를 저장 합니다. 예: DisableManifestXml.</span><span class="sxs-lookup"><span data-stu-id="13770-117">Save the following text to a Windows registry file by using a filename suffix of .reg; for example, DisableManifestXml.reg.</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d False 
      ```

3. <span data-ttu-id="13770-118">Windows 탐색기에서 이전 단계에서 만든 .reg 파일을 클릭 하거나 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-118">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
4. <span data-ttu-id="13770-119">사용자 액세스 제어 창에서 **예** 를 클릭 하 여 레지스트리 편집기에서 변경 작업을 수행 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-119">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="13770-120">계속할지 묻는 메시지가 표시 되 면 **예**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-120">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="13770-121">레지스트리 편집기에 설정이 레지스트리에 성공적으로 추가 되었다는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13770-121">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
  
## <a name="edit-registry-settings-to-re-enable-the-export-reports"></a><span data-ttu-id="13770-122">레지스트리 설정을 편집 하 여 내보내기 보고서를 다시 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="13770-122">Edit registry settings to re-enable the export reports</span></span>

<span data-ttu-id="13770-123">이전 절차에서 .reg 파일을 만들어 결과 .csv 및 manifest.xml 보고서를 사용 하지 않도록 설정한 경우에는 해당 파일을 편집 하 여 검색 결과와 함께 내보낼 수 있도록 보고서를 다시 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-123">If you disabled the Results.csv and Manifest.xml reports by creating the .reg files in the previous procedure, you can edit those files to re-enable a report so that it's exported with the search results.</span></span> <span data-ttu-id="13770-124">결과를 콘텐츠 검색으로 내보내기 위해 사용 하는 컴퓨터에서 다음 절차를 다시 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-124">Again, perform the following procedure on the computer that you'll use to export the results a content search.</span></span>
  
1. <span data-ttu-id="13770-125">Office 365 eDiscovery 내보내기 도구가 열려 있는 경우 해당 도구를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="13770-125">Close the Office 365 eDiscovery Export tool if it's open.</span></span>
    
2. <span data-ttu-id="13770-126">이전 절차에서 만든 .reg 편집 파일 하나 또는 둘 다를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-126">Edit one or both of the .reg edit files that you created in the previous procedure.</span></span>
    
    - <span data-ttu-id="13770-127">**결과 .csv**</span><span class="sxs-lookup"><span data-stu-id="13770-127">**Results.csv**</span></span>
    
        <span data-ttu-id="13770-128">메모장에서 DisableResultsCsv 파일을 열고 값 `False` 을로 `True`변경한 다음 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-128">Open the DisableResultsCsv.reg file in Notepad, change the value  `False` to  `True`, and then save the file.</span></span> <span data-ttu-id="13770-129">예를 들어 파일을 편집한 후에는 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13770-129">For example, after you edit the file, it looks like this:</span></span>
    
        ```
        Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d True
        ```

    - <span data-ttu-id="13770-130">**manifest.xml**</span><span class="sxs-lookup"><span data-stu-id="13770-130">**Manifest.xml**</span></span>
    
        <span data-ttu-id="13770-131">메모장에서 DisableManifestXml 파일을 열고 값 `False` 을로 `True`변경한 다음 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-131">Open the DisableManifestXml.reg file in Notepad, change the value  `False` to  `True`, and then save the file.</span></span> <span data-ttu-id="13770-132">예를 들어 파일을 편집한 후에는 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13770-132">For example, after you edit the file, it looks like this:</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d True
      ```

3. <span data-ttu-id="13770-133">Windows 탐색기에서 이전 단계에서 편집한 .reg 파일을 클릭 하거나 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-133">In Windows Explorer, click or double-click a .reg file that you edited in the previous step.</span></span>
    
4. <span data-ttu-id="13770-134">사용자 액세스 제어 창에서 **예** 를 클릭 하 여 레지스트리 편집기에서 변경 작업을 수행 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-134">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="13770-135">계속할지 묻는 메시지가 표시 되 면 **예**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-135">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="13770-136">레지스트리 편집기에 설정이 레지스트리에 성공적으로 추가 되었다는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13770-136">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
  
## <a name="frequently-asked-questions-about-disabling-export-reports"></a><span data-ttu-id="13770-137">보고서 내보내기를 사용 하지 않도록 설정 하는 방법에 대 한 질문과 대답</span><span class="sxs-lookup"><span data-stu-id="13770-137">Frequently asked questions about disabling export reports</span></span>
<span data-ttu-id="13770-138"><a name="faqs"> </a></span><span class="sxs-lookup"><span data-stu-id="13770-138"></span></span>

 <span data-ttu-id="13770-139">**결과는 무엇입니까? .csv 및 manifest.xml 보고서?**</span><span class="sxs-lookup"><span data-stu-id="13770-139">**What are the Results.csv and Manifest.xml reports?**</span></span>
  
<span data-ttu-id="13770-140">결과 .csv 및 manifest.xml 파일에는 내보낸 콘텐츠에 대 한 추가 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13770-140">The Results.csv and Manifest.xml files contain additional information about the content that was exported.</span></span>
  
- <span data-ttu-id="13770-141">**Results** -검색 결과로 다운로드 되는 각 항목에 대 한 정보가 포함 된 Excel 문서입니다.</span><span class="sxs-lookup"><span data-stu-id="13770-141">**Results.csv** An Excel document that contains information about each item that is download as a search result.</span></span> <span data-ttu-id="13770-142">전자 메일의 경우 결과 로그에 다음을 비롯 한 각 메시지에 대 한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13770-142">For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="13770-143">원본 사서함에 있는 메시지의 위치 (포함 여부는 주 메시지는 보관 사서함 또는).</span><span class="sxs-lookup"><span data-stu-id="13770-143">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="13770-144">메시지가 전송된 날짜</span><span class="sxs-lookup"><span data-stu-id="13770-144">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="13770-145">메시지의 제목 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="13770-145">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="13770-146">보낸 사람 및 메시지 받는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="13770-146">The sender and recipients of the message.</span></span>
    
  - <span data-ttu-id="13770-147">검색 결과를 내보낼 때 중복 제거를 사용 하도록 설정한 경우 메시지가 중복 메시지 인지 여부</span><span class="sxs-lookup"><span data-stu-id="13770-147">Whether the message is a duplicate message if you enabled de-duplication when exporting the search results.</span></span> <span data-ttu-id="13770-148">중복 메시지는 메시지를 중복 된 것으로 식별 하는 **부모 ItemId** 열에 값을 갖게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13770-148">Duplicate messages will have a value in the **Parent ItemId** column that identifies the message as a duplicate.</span></span> <span data-ttu-id="13770-149">**부모 ItemId** 열의 값은 내보낸 메시지의 **Item DocumentId** 열에 있는 값과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="13770-149">The value in the **Parent ItemId** column is the same as the value in the **Item DocumentId** column of the message that was exported.</span></span> 
    
    <span data-ttu-id="13770-150">SharePoint 및 비즈니스용 OneDrive 사이트의 문서에 대해 결과 로그에 다음을 비롯 한 각 문서에 대 한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13770-150">For documents from SharePoint and OneDrive for Business sites, the result log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="13770-151">문서에 대 한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="13770-151">The URL for the document.</span></span>
    
  - <span data-ttu-id="13770-152">문서가 있는 사이트 모음의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="13770-152">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="13770-153">문서를 마지막으로 수정한 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="13770-153">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="13770-154">이름 (에 있는 제목 열 결과 로그에서) 문서입니다.</span><span class="sxs-lookup"><span data-stu-id="13770-154">The name of the document (which is located in the Subject column in the result log).</span></span>
    
- <span data-ttu-id="13770-155">**manifest.xml** -검색 결과에 포함 된 각 항목에 대 한 정보를 포함 하는 매니페스트 파일 (xml 형식)입니다.</span><span class="sxs-lookup"><span data-stu-id="13770-155">**Manifest.xml** A manifest file (in XML format) that contains information about each item included in the search results.</span></span> <span data-ttu-id="13770-156">이 보고서의 정보는 결과 .csv 보고서와 동일 하지만 edrm (전자식 Discovery Reference Model)에 지정 된 형식으로 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13770-156">The information in this report is the same as the Results.csv report, but it's in the format specified by the Electronic Discovery Reference Model (EDRM).</span></span> <span data-ttu-id="13770-157">edrm에 대 한 자세한 내용은로 [https://www.edrm.net](https://www.edrm.net)이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-157">For more information about EDRM, go to [https://www.edrm.net](https://www.edrm.net).</span></span>
    
 <span data-ttu-id="13770-158">**이러한 보고서 내보내기를 사용 하지 않도록 설정 해야 하는 경우**</span><span class="sxs-lookup"><span data-stu-id="13770-158">**When should I disable exporting these reports?**</span></span>
  
<span data-ttu-id="13770-159">특정 요구 사항에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="13770-159">It depends on your specific needs.</span></span> <span data-ttu-id="13770-160">대부분의 조직에는 검색 결과에 대 한 추가 정보가 필요 하지 않으며 이러한 보고서가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13770-160">Many organizations don't require additional information about search results, and don't need these reports.</span></span>
  
 <span data-ttu-id="13770-161">**어떤 컴퓨터에서이 작업을 수행 해야 하나요?**</span><span class="sxs-lookup"><span data-stu-id="13770-161">**What computer do I have to do this on?**</span></span>
  
 <span data-ttu-id="13770-162">Office 365 eDiscovery 내보내기 도구를 실행 하는 로컬 컴퓨터에서 레지스트리 설정을 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-162">You have to change the registry setting on any local computer that you run the Office 365 eDiscovery Export tool on.</span></span> 
  
 <span data-ttu-id="13770-163">**이 설정을 변경한 후 컴퓨터를 다시 시작 해야 하나요?**</span><span class="sxs-lookup"><span data-stu-id="13770-163">**After I change this setting, do I have to restart the computer?**</span></span>
  
<span data-ttu-id="13770-164">아니요, 컴퓨터를 다시 시작할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="13770-164">No, you don't have to restart the computer.</span></span> <span data-ttu-id="13770-165">그러나 Office 365 eDiscovery 내보내기 도구가 실행 되 고 있으면 닫은 후 레지스트리 설정을 변경한 후에 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="13770-165">But if the Office 365 eDiscovery Export tool is running, you have to close it and then restart it after you change the registry setting.</span></span>
  
 <span data-ttu-id="13770-166">**기존 레지스트리 키를 편집 하거나 새 키를 만들기 시작 합니까?**</span><span class="sxs-lookup"><span data-stu-id="13770-166">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="13770-167">이 항목의 절차에서 만든 .reg 파일을 처음 실행할 때 새 레지스트리 키가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="13770-167">A new registry key is created the first time you run the .reg file that you created in the procedure in this topic.</span></span> <span data-ttu-id="13770-168">그런 다음 .reg 편집 파일을 변경 하 고 다시 실행할 때마다 설정이 편집 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13770-168">Then the setting is edited each time you change and re-run the .reg edit file.</span></span>
