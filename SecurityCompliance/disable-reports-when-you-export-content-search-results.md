---
title: Office 365 보안에서 콘텐츠 검색 결과 내보낼 때 보고서를 사용 하지 않도록 설정 &amp; 준수 센터
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: c9b0ff0c-282b-4a44-b43f-cfc5b96557f9
description: Office 365 보안에서 콘텐츠 검색의 결과 내보낼 때 보고서를 사용 하지 않도록 설정 하려면 로컬 컴퓨터에 Windows 레지스트리를 편집 &amp; Comliance 센터입니다. 이러한 보고서를 사용 하지 않도록 설정 다운로드 시간을 단축 하 고 디스크 공간을 절약할 수 있습니다.
ms.openlocfilehash: 62782c472adca892e1dcf239a45fe80f0fa7251b
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037981"
---
# <a name="disable-reports-when-you-export-content-search-results-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="19080-104">Office 365 보안에서 콘텐츠 검색 결과 내보낼 때 보고서를 사용 하지 않도록 설정 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="19080-104">Disable reports when you export Content Search results in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="19080-p102">보안에서 콘텐츠 검색의 결과를 내보내려면 Office 365 eDiscovery 내보내기 도구를 사용 하면 &amp; 준수 센터 도구가 자동으로 만들고 내보낸된 콘텐츠에 대 한 추가 정보를 포함 하는 두 보고서를 내보냅니다. 이러한 보고서는 Results.csv 파일과 Manifest.xml 파일 (이 항목에 대 한 자세한 설명은 이러한 보고서의 [질문과 대답 (영문) 내보내기 보고서를 사용 하지 않도록 설정 하는 방법에 대 한](#frequently-asked-questions-about-disabling-export-reports) 섹션 참조). 이러한 파일 매우 커질 수 있으므로 다운로드 시간을 단축할 수 있으며 내보내고에서 이러한 파일을 방지 하 여 디스크 공간을 절약할 수 있습니다. 검색 결과 내보내는 데 사용 하는 컴퓨터에서 Windows 레지스트리를 변경 하 여이 수행할 수 있습니다. 나중에는 보고서를 포함 하려는 경우에 레지스트리 설정을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19080-p102">When you use the Office 365 eDiscovery Export tool to export the results of a Content Search in the Security &amp; Compliance Center, the tool automatically creates and exports two reports that contain additional information about the exported content. These reports are the Results.csv file and the Manifest.xml file (see the [Frequently asked questions about disabling export reports](#frequently-asked-questions-about-disabling-export-reports) section in this topic for detailed descriptions of these reports). Because these files can be very large, you can speed up the download time and save disk space by preventing these files from being exported. You can do this by changing the Windows Registry on the computer that you use to export the search results. If you want to include the reports at a later time, you can edit the registry setting.</span></span> 
  
## <a name="create-registry-settings-to-disable-the-export-reports"></a><span data-ttu-id="19080-110">내보내기 보고서를 사용 하지 않도록 설정 하려면 레지스트리 설정을 만들려면</span><span class="sxs-lookup"><span data-stu-id="19080-110">Create registry settings to disable the export reports</span></span>

<span data-ttu-id="19080-111">콘텐츠 검색 결과 내보내는 데 사용할 수 있는 컴퓨터에서 다음 절차를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-111">Perform the following procedure on the computer that you'll use to export the results a content search.</span></span>
  
1. <span data-ttu-id="19080-112">열려 있으면 Office 365 eDiscovery 내보내기 도구를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="19080-112">Close the Office 365 eDiscovery Export tool if it's open.</span></span>
    
2. <span data-ttu-id="19080-113">어떤 내보내기 보고서에 따라 사용 하지 않도록 설정 하려면 다음 단계 중 하나 또는 모두를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-113">Perform one or both of the following steps, depending on which export report you want to disable.</span></span>
    
    - <span data-ttu-id="19080-114">**Results.csv**</span><span class="sxs-lookup"><span data-stu-id="19080-114">**Results.csv**</span></span>
    
      <span data-ttu-id="19080-115">.Reg; filename 접미사를 사용 하 여 Windows 레지스트리 파일에 다음 텍스트를 저장 예: DisableResultsCsv.reg 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-115">Save the following text to a Windows registry file by using a filename suffix of .reg; for example, DisableResultsCsv.reg.</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d False 
      ```

    - <span data-ttu-id="19080-116">**Manifest.xml**</span><span class="sxs-lookup"><span data-stu-id="19080-116">**Manifest.xml**</span></span>
    
      <span data-ttu-id="19080-117">.Reg; filename 접미사를 사용 하 여 Windows 레지스트리 파일에 다음 텍스트를 저장 예: DisableManifestXml.reg 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-117">Save the following text to a Windows registry file by using a filename suffix of .reg; for example, DisableManifestXml.reg.</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d False 
      ```

3. <span data-ttu-id="19080-118">Windows 탐색기에서를 클릭 하거나 이전 단계에서 만든.reg 파일을 두번클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-118">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
4. <span data-ttu-id="19080-119">사용자 액세스 제어 창에서 **예** 는 변경 내용을 적용 하 여 레지스트리 편집기를 하도록 하려면이 옵션을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-119">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="19080-120">를 계속 하 라는 메시지가 나타나면 **예**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-120">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="19080-121">레지스트리 편집기 설정을 레지스트리에 성공적으로 추가 된 했다는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-121">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
  
## <a name="edit-registry-settings-to-re-enable-the-export-reports"></a><span data-ttu-id="19080-122">레지스트리 설정을 다시 내보내기 보고서를 사용 하도록 설정 편집</span><span class="sxs-lookup"><span data-stu-id="19080-122">Edit registry settings to re-enable the export reports</span></span>

<span data-ttu-id="19080-p103">이전 절차에서.reg 파일을 만들어서 Results.csv 및 Manifest.xml 보고서를 사용 하지 않도록 설정한 경우에 검색 결과 함께 내보낼 수 있도록 보고서를 다시 활성화 하려면 해당 파일을 편집할 수 있습니다. 다시, 콘텐츠 검색 결과 내보내는 데 사용할 수 있는 컴퓨터에서 다음 절차를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-p103">If you disabled the Results.csv and Manifest.xml reports by creating the .reg files in the previous procedure, you can edit those files to re-enable a report so that it's exported with the search results. Again, perform the following procedure on the computer that you'll use to export the results a content search.</span></span>
  
1. <span data-ttu-id="19080-125">열려 있으면 Office 365 eDiscovery 내보내기 도구를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="19080-125">Close the Office 365 eDiscovery Export tool if it's open.</span></span>
    
2. <span data-ttu-id="19080-126">이전 절차에서 만든.reg 편집 파일 중 하나 또는 모두를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-126">Edit one or both of the .reg edit files that you created in the previous procedure.</span></span>
    
    - <span data-ttu-id="19080-127">**Results.csv**</span><span class="sxs-lookup"><span data-stu-id="19080-127">**Results.csv**</span></span>
    
        <span data-ttu-id="19080-p104">Open 메모장에서 DisableResultsCsv.reg 파일 값을 변경 `False` 에 `True`, 파일을 저장 합니다. 예, 파일을 편집한 후 다음과 같이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="19080-p104">Open the DisableResultsCsv.reg file in Notepad, change the value  `False` to  `True`, and then save the file. For example, after you edit the file, it looks like this:</span></span>
    
        ```
        Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d True
        ```

    - <span data-ttu-id="19080-130">**Manifest.xml**</span><span class="sxs-lookup"><span data-stu-id="19080-130">**Manifest.xml**</span></span>
    
        <span data-ttu-id="19080-p105">Open 메모장에서 DisableManifestXml.reg 파일 값을 변경 `False` 에 `True`, 파일을 저장 합니다. 예, 파일을 편집한 후 다음과 같이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="19080-p105">Open the DisableManifestXml.reg file in Notepad, change the value  `False` to  `True`, and then save the file. For example, after you edit the file, it looks like this:</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d True
      ```

3. <span data-ttu-id="19080-133">Windows 탐색기에서를 클릭 하거나 이전 단계에서 편집 하는.reg 파일을 두번클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-133">In Windows Explorer, click or double-click a .reg file that you edited in the previous step.</span></span>
    
4. <span data-ttu-id="19080-134">사용자 액세스 제어 창에서 **예** 는 변경 내용을 적용 하 여 레지스트리 편집기를 하도록 하려면이 옵션을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-134">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="19080-135">를 계속 하 라는 메시지가 나타나면 **예**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-135">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="19080-136">레지스트리 편집기 설정을 레지스트리에 성공적으로 추가 된 했다는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-136">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
  
## <a name="frequently-asked-questions-about-disabling-export-reports"></a><span data-ttu-id="19080-137">내보내기 보고서를 사용 하지 않도록 설정 하는 방법에 대 한 질문과 대답</span><span class="sxs-lookup"><span data-stu-id="19080-137">Frequently asked questions about disabling export reports</span></span>
<span data-ttu-id="19080-138"><a name="faqs"> </a></span><span class="sxs-lookup"><span data-stu-id="19080-138"></span></span>

 <span data-ttu-id="19080-139">**Results.csv 및 Manifest.xml 보고서는 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="19080-139">**What are the Results.csv and Manifest.xml reports?**</span></span>
  
<span data-ttu-id="19080-140">Results.csv 및 Manifest.xml 파일 내보낸 콘텐츠에 대 한 추가 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-140">The Results.csv and Manifest.xml files contain additional information about the content that was exported.</span></span>
  
- <span data-ttu-id="19080-p106">검색 결과 다운로드 하는 각 항목에 대 한 정보가 포함 된 **Results.csv** Excel 문서입니다. 전자 메일, 결과 로그 각 메시지에 대 한 정보가 들어 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-p106">**Results.csv** An Excel document that contains information about each item that is download as a search result. For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="19080-143">원본 사서함에 있는 메시지의 위치 (포함 여부는 주 메시지는 보관 사서함 또는).</span><span class="sxs-lookup"><span data-stu-id="19080-143">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="19080-144">메시지가 전송된 날짜</span><span class="sxs-lookup"><span data-stu-id="19080-144">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="19080-145">메시지의 제목 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="19080-145">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="19080-146">보낸 사람 및 메시지 받는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="19080-146">The sender and recipients of the message.</span></span>
    
  - <span data-ttu-id="19080-p107">있는지 여부는 메시지 검색 결과 내보낼 때 중복을 사용 하는 경우 중복 된 메시지입니다. 중복 된 메시지는 중복 된 것으로 메시지를 식별 하는 **상위 ItemId** 열에서 값을 갖게 됩니다. **부모 ItemId** 열에서 값은 내보낸 메시지의 **항목 DocumentId** 열에서 값과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="19080-p107">Whether the message is a duplicate message if you enabled de-duplication when exporting the search results. Duplicate messages will have a value in the **Parent ItemId** column that identifies the message as a duplicate. The value in the **Parent ItemId** column is the same as the value in the **Item DocumentId** column of the message that was exported.</span></span> 
    
    <span data-ttu-id="19080-150">SharePoint와 OneDrive에서 비즈니스 사이트에 대 한 문서에 대 한 결과 로그는 각 문서에 대 한 정보를 포함 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-150">For documents from SharePoint and OneDrive for Business sites, the result log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="19080-151">문서에 대 한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="19080-151">The URL for the document.</span></span>
    
  - <span data-ttu-id="19080-152">문서가 있는 사이트 모음의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="19080-152">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="19080-153">문서를 마지막으로 수정한 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="19080-153">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="19080-154">이름 (에 있는 제목 열 결과 로그에서) 문서입니다.</span><span class="sxs-lookup"><span data-stu-id="19080-154">The name of the document (which is located in the Subject column in the result log).</span></span>
    
- <span data-ttu-id="19080-p108">**Manifest.xml** 매니페스트 파일 (XML 형식)에서 검색 결과에 포함 된 각 항목에 대 한 정보를 포함 하는입니다. 이 보고서의 정보는 Results.csv 보고서 같지만 지정 하 여는 참조 모델 EDRM (Electronic Discovery) 형식에서입니다. EDRM에 대 한 자세한 내용은 이동 [https://www.edrm.net](https://www.edrm.net)합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-p108">**Manifest.xml** A manifest file (in XML format) that contains information about each item included in the search results. The information in this report is the same as the Results.csv report, but it's in the format specified by the Electronic Discovery Reference Model (EDRM). For more information about EDRM, go to [https://www.edrm.net](https://www.edrm.net).</span></span>
    
 <span data-ttu-id="19080-158">**이러한 보고서 내보내기 (영문)를 비활성화 해야는 경우**</span><span class="sxs-lookup"><span data-stu-id="19080-158">**When should I disable exporting these reports?**</span></span>
  
<span data-ttu-id="19080-p109">특정 요구 사항에 따라 다릅니다. 대부분의 조직에서는 검색 결과 대 한 추가 정보를 필요 하지 않습니다 및 이러한 보고서를 필요로 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19080-p109">It depends on your specific needs. Many organizations don't require additional information about search results, and don't need these reports.</span></span>
  
 <span data-ttu-id="19080-161">**이 작업을 수행에서 어떤 컴퓨터 해야 합니까?**</span><span class="sxs-lookup"><span data-stu-id="19080-161">**What computer do I have to do this on?**</span></span>
  
 <span data-ttu-id="19080-162">Office 365 eDiscovery 내보내기 도구를 실행 하는 모든 로컬 컴퓨터에서 레지스트리 설정을 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-162">You have to change the registry setting on any local computer that you run the Office 365 eDiscovery Export tool on.</span></span> 
  
 <span data-ttu-id="19080-163">**이 설정은 변경 후 컴퓨터를 다시 시작 해야 합니까?**</span><span class="sxs-lookup"><span data-stu-id="19080-163">**After I change this setting, do I have to restart the computer?**</span></span>
  
<span data-ttu-id="19080-p110">아니요, 컴퓨터를 다시 시작할 필요가 없습니다. 하지만 Office 365 eDiscovery 내보내기 도구를 실행 하는 경우를 닫고 레지스트리 설정을 변경한 다음 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-p110">No, you don't have to restart the computer. But if the Office 365 eDiscovery Export tool is running, you have to close it and then restart it after you change the registry setting.</span></span>
  
 <span data-ttu-id="19080-166">**기존 레지스트리 키 편집 가져오기 또는 않는 새 키를 만든 가져올?**</span><span class="sxs-lookup"><span data-stu-id="19080-166">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="19080-p111">새 레지스트리 키에는이 항목의 절차에서 만든.reg 파일을 실행 하는 처음으로 만들어집니다. 다음 설정은 변경 하 고 편집.reg 파일을 다시 실행 때마다 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="19080-p111">A new registry key is created the first time you run the .reg file that you created in the procedure in this topic. Then the setting is edited each time you change and re-run the .reg edit file.</span></span>
