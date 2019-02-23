---
title: Office 365 Security & 준수 센터에서 콘텐츠 검색 결과 내보내기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExport
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: ed48d448-3714-4c42-85f5-10f75f6a4278
description: 'Office 365 Security & 준수 센터의 콘텐츠 검색에서 검색 결과를 로컬 컴퓨터로 내보냅니다. 전자 메일 결과를 PST 파일로 내보냅니다. SharePoint의 콘텐츠 및 비즈니스용 OneDrive 사이트는 기본 Office 문서로 내보내집니다. '
ms.openlocfilehash: 5ec1456c7d1a787a1ede70c15b109e7f0358f60a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219948"
---
# <a name="export-content-search-results-from-the-office-365-security--compliance-center"></a><span data-ttu-id="df5fb-105">Office 365 Security & 준수 센터에서 콘텐츠 검색 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="df5fb-105">Export Content Search results from the Office 365 Security & Compliance Center</span></span>

<span data-ttu-id="df5fb-p102">콘텐츠 검색을 성공적으로 실행 한 후에는 검색 결과를 로컬 컴퓨터로 내보낼 수 있습니다. 전자 메일 결과를 내보낼 때 사용자 컴퓨터로 PST 파일로 다운로드 됩니다. SharePoint 및 비즈니스용 OneDrive 사이트에서 콘텐츠를 내보낼 때 기본 Office 문서의 복사본을 내보냅니다. 내보낸 검색 결과에 포함 되는 추가 문서 및 보고서가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p102">After a Content Search is successfully run, you can export the search results to a local computer. When you export email results, they're downloaded to your computer as PST files. When you export content from SharePoint and OneDrive for Business sites, copies of native Office documents are exported. There are additional documents and reports that are included with the exported search results.</span></span>
  
<span data-ttu-id="df5fb-p103">또한 콘텐츠 검색 결과에 포함 된 모든 RMS 암호화 전자 메일 메시지를 개별 메시지로 내보낼 때 암호가 해독 됩니다. 이 암호 해독 기능은 eDiscovery 관리자 역할 그룹의 구성원에 대해 기본적으로 사용 하도록 설정 됩니다. RMS 암호 해독 관리 역할이이 역할 그룹에 할당 되었기 때문입니다. 검색 결과를 내보낼 때 RMS 암호 해독에 대 한 자세한 [내용은 추가 정보](#more-information) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p103">Additionally, any RMS-encrypted email messages that are included in the results of a Content Search will be decrypted when you export them (as individual messages). This decryption capability is enabled by default for members of the eDiscovery Manager role group. This is because the RMS Decrypt management role is assigned to this role group. See the [More information](#more-information) section for details about RMS decryption when you export search results.</span></span> 
  
<span data-ttu-id="df5fb-114">콘텐츠 검색 결과를 내보내면 결과가 준비 된 후 로컬 컴퓨터로 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-114">Exporting the results of a Content Search involves preparing the results, and then downloading them to a local computer.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="df5fb-115">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="df5fb-115">Before you begin</span></span>

- <span data-ttu-id="df5fb-p104">검색 결과를 내보내려면 Office 365 보안 &amp; 및 준수 센터에서 내보내기 관리 역할을 할당 받아야 합니다. 이 역할은 기본 제공 eDiscovery 관리자 역할 그룹에 할당 됩니다. 기본적으로 조직 관리 역할 그룹에 할당 되지 않습니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 사용 권한 할당](assign-ediscovery-permissions.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p104">To export search results, you have to be assigned the Export management role in the Office 365 Security &amp; Compliance Center. This role is assigned to the built-in eDiscovery Manager role group. It isn't assigned by default to the Organization Management role group. For more information, see [Assign eDiscovery permissions in the Office 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="df5fb-120">검색 결과를 PST 파일로 내보내는 데 사용하는 컴퓨터는 다음과 같은 시스템 요구 사항을 충족해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-120">The computer you use to export the search results has to meet the following system requirements:</span></span>
    
  - <span data-ttu-id="df5fb-121">32비트 및 64비트 버전의 Windows 7 이상 버전


</span><span class="sxs-lookup"><span data-stu-id="df5fb-121">32- or 64-bit versions of Windows 7 and later versions</span></span>
    
  - <span data-ttu-id="df5fb-122">Microsoft .net Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="df5fb-122">Microsoft .NET Framework 4.7</span></span>
    
  - <span data-ttu-id="df5fb-123">지원되는 브라우저:</span><span class="sxs-lookup"><span data-stu-id="df5fb-123">A supported browser:</span></span>
    
     - <span data-ttu-id="df5fb-124">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="df5fb-124">Microsoft Edge</span></span>
    
        <span data-ttu-id="df5fb-125">또는</span><span class="sxs-lookup"><span data-stu-id="df5fb-125">OR</span></span>
    
     - <span data-ttu-id="df5fb-126">Microsoft Internet Explorer 10 이상 버전</span><span class="sxs-lookup"><span data-stu-id="df5fb-126">Microsoft Internet Explorer 10 and later versions</span></span>
    
    <span data-ttu-id="df5fb-p105">**참고:** Microsoft는 ClickOnce 응용 프로그램에 대 한 타사 확장 또는 추가 기능을 제조 하지 않습니다. 타사 확장 또는 추가 기능에서 지원 되지 않는 브라우저를 사용 하 여 검색 결과를 내보낼 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p105">**Note:** Microsoft doesn't manufacture third-party extensions or add-ons for ClickOnce applications. Exporting search results using an unsupported browser with third-party extensions or add-ons isn't supported.</span></span> 
    
- <span data-ttu-id="df5fb-p106">2 단계에 설명 된 대로 검색 결과를 다운로드할 때 검색 결과를 내보내는 데 사용 하는 컴퓨터에서 Windows 레지스트리 설정을 구성 하 여 다운로드 속도를 높일 수 있습니다. 자세한 내용은 [Office 365에서 eDiscovery 검색 결과를 내보낼 때 다운로드 속도 높이기](increase-download-speeds-when-exporting-ediscovery-results.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p106">When you download search results (described in Step 2), you can increase the download speed by configuring a Windows Registry setting on the computer you use to export the search results. For more information, see [Increase the download speed when exporting eDiscovery search results from Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).</span></span>
    
- <span data-ttu-id="df5fb-p107">검색 결과를 내보낼 때 데이터가 로컬 컴퓨터로 다운로드 되기 전에 microsoft 클라우드의 고유한 microsoft Azure 저장소 위치에 임시로 저장 됩니다. 조직이 Azure의 끝점에 연결할 수 있는지 (와일드 카드는 내보내기에 대 한 고유 식별자를 나타냄) \*\* \*blob.core.windows.net 합니다\*\* . 검색 결과 데이터는 만들어진 후 2 주 후 Azure 저장소 위치에서 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p107">When you export search results, the data is temporarily stored in a unique Microsoft Azure storage location in the Microsoft cloud before it's downloaded to your local computer. Be sure your organization can connect to the endpoint in Azure, which is **\*.blob.core.windows.net** (the wildcard represents a unique identifier for your export). The search results data is deleted from the Azure storage location two weeks after it's created.</span></span> 
    
- <span data-ttu-id="df5fb-p108">조직에서 프록시 서버를 사용 하 여 인터넷에 통신 하는 경우 검색 결과를 내보내는 데 사용 하는 컴퓨터에서 프록시 서버 설정을 정의 해야 합니다 (따라서 내보내기 도구를 프록시 서버에서 인증할 수 있음). 이렇게 하려면 해당 버전의 Windows \*\* 와 일치 하는 위치에서 machine.config 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p108">If your organization uses a proxy server to communicate with the Internet, you need to define the proxy server settings on the computer that you use to export the search results (so the export tool can be authenticated by your proxy server). To do this, open the  *machine.config*  file in the location that matches your version of Windows.</span></span> 
    
  - <span data-ttu-id="df5fb-136">**32 비트** - `%windir%\Microsoft.NET\Framework\[version]\Config\machine.config`</span><span class="sxs-lookup"><span data-stu-id="df5fb-136">**32-bit** - `%windir%\Microsoft.NET\Framework\[version]\Config\machine.config`</span></span>
    
  - <span data-ttu-id="df5fb-137">**64 비트** - `%windir%\Microsoft.NET\Framework64\[version]\Config\machine.config`</span><span class="sxs-lookup"><span data-stu-id="df5fb-137">**64-bit** - `%windir%\Microsoft.NET\Framework64\[version]\Config\machine.config`</span></span>
    
    <span data-ttu-id="df5fb-p109">와 태그 사이에 있는 machine.config 파일에 다음 줄을 추가 합니다. \*\* `<configuration>` `</configuration>` 조직의 올바른 값을 `ProxyServer` 교체 `Port` 해야 합니다. 예를 `proxy01.contoso.com:80` 들면입니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p109">Add the following lines to the  *machine.config*  file somewhere between the  `<configuration>` and  `</configuration>` tags. Be sure to replace  `ProxyServer` and  `Port` with the correct values for your organization; for example,  `proxy01.contoso.com:80` .</span></span> 
    
    ```
    <system.net>
       <defaultProxy enabled="true" useDefaultCredentials="true">
         <proxy proxyaddress="http://ProxyServer :Port " 
                usesystemdefault="False" 
                bypassonlocal="True" 
                autoDetect="False" />
       </defaultProxy>
    </system.net>
    ```
    
## <a name="step-1-prepare-search-results-for-export"></a><span data-ttu-id="df5fb-140">1단계: 내보내기에 대 한 검색 결과 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-140">Step 1: Prepare search results for export</span></span>

<span data-ttu-id="df5fb-p110">첫 번째 단계는 검색 결과를 내보내기 위해 준비 하는 것입니다. 결과를 준비할 때 Microsoft 클라우드의 Azure 저장소 위치에 업로드 됩니다. 사서함 및 사이트의 콘텐츠는 시간당 최대 2gb로 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p110">The first step is to prepare the search results for exporting. When you prepare results, they are uploaded to an Azure storage location in the Microsoft cloud. Note that content from mailboxes and sites is uploaded at a maximum rate of 2 GB per hour.</span></span>
  
1. <span data-ttu-id="df5fb-144">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-144">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="df5fb-145">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-145">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="df5fb-146">보안 및 준수 센터의 왼쪽 창에서 **검색 및 조사** \> **콘텐츠 검색**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-146">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**.</span></span>
    
4. <span data-ttu-id="df5fb-147">**콘텐츠 검색** 페이지에서 검색을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-147">On the **Content search** page, select a search.</span></span> 
    
5. <span data-ttu-id="df5fb-148">세부 정보 창에서 **컴퓨터에 결과 내보내기** 아래의 **내보내기 시작**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-148">In the details pane, under **Export results to a computer**, click **Start export**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="df5fb-p111">검색 결과 7 일 보다 오래 된 경우 검색 결과 업데이트 하 라는 메시지가 표시. 이런 경우 내보내기를 취소 클릭 합니다 **업데이트 검색 결과** 선택한 검색 한 다음 시작 결과 후 다시 내보내기에 대 한 세부 정보 창에서 업데이트 됩니다. </span><span class="sxs-lookup"><span data-stu-id="df5fb-p111">If the results for a search are older than 7 days, you are prompted to update the search results. If this happens, cancel the export, click **Update search results** in the details pane for the selected search, and then start the export again after the results are updated.</span></span> 
  
6. <span data-ttu-id="df5fb-151">**검색 결과 내보내기** 페이지의 **출력 옵션**에서 다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-151">On the **Export the search results** page, under **Output options**, choose one of the following options:</span></span>
    
    - <span data-ttu-id="df5fb-152">형식을 인식할 수 없거나, 암호화 되거나, 다른 이유로 인덱싱되지 않은 모든 항목을 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-152">All items, excluding ones that have unrecognized format, are encrypted, or weren't indexed for other reasons</span></span>
    
    - <span data-ttu-id="df5fb-153">형식을 인식할 수 없거나 암호화 되었거나 다른 이유로 인덱싱되지 않은 모든 항목</span><span class="sxs-lookup"><span data-stu-id="df5fb-153">All items, including ones that have unrecognized format, are encrypted, or weren't indexed for other reasons</span></span>
    
    - <span data-ttu-id="df5fb-154">다른 이유로 인해 형식이 인식 되지 않거나 암호화 되거나 인덱싱되지 않은 항목만</span><span class="sxs-lookup"><span data-stu-id="df5fb-154">Only items that have an unrecognized format, are encrypted, or weren't indexed for other reasons</span></span>
    
    <span data-ttu-id="df5fb-p112">부분적으로 인덱싱된 항목을 내보내는 방법에 대 한 설명은 [추가 정보](#more-information) 섹션을 참조 하십시오. 부분적으로 인덱싱된 항목에 대 한 자세한 내용은 [콘텐츠 검색에서 부분적으로 인덱싱된 항목](partially-indexed-items-in-content-search.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p112">See the [More information](#more-information) section for a description about how partially indexed items are exported. For more information about partially indexed items, see [Partially indexed items in Content Search](partially-indexed-items-in-content-search.md).</span></span>
    
7. <span data-ttu-id="df5fb-157">**Exchange 콘텐츠를 다음으로 내보내기**에서 다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-157">Under **Export Exchange content as**, choose one of the following options:</span></span>
    
    - <span data-ttu-id="df5fb-p113">**각 사서함에 대 한 pst 파일 하나씩** 검색 결과를 포함 하는 각 사용자 사서함에 대해 pst 파일 하나를 내보냅니다. 사용자의 보관 사서함에 포함 된 모든 결과는 동일한 PST 파일에 들어 있습니다. 이 옵션은 원본 사서함에서 사서함 폴더 구조를 reproduces 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p113">**One PST file for each mailbox** - Exports one PST file for each user mailbox that contains search results. Any results from the user's archive mailbox are included in the same PST file. Note that this option reproduces the mailbox folder structure from the source mailbox.</span></span> 
    
    - <span data-ttu-id="df5fb-p114">**모든 메시지를 포함 하는 하나의 pst 파일** -검색에 포함 된 모든 원본 사서함의 검색 결과를 포함 하는 단일 pst 파일 (이름이 있는 *Exchange .pst* )을 내보냅니다. 이 옵션은 각 메시지에 대 한 사서함 폴더 구조를 reproduces 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p114">**One PST file containing all messages** - Exports a single PST file (named  *Exchange.pst*  ) that contains the search results from all source mailboxes included in the search. Note that this option reproduces the mailbox folder structure for each message.</span></span> 
    
    - <span data-ttu-id="df5fb-p115">**단일 폴더에 있는 모든 메시지를 포함 하는 하나의 pst 파일** 을 사용 하 여 모든 메시지가 하나의 최상위 폴더에 있는 단일 pst 파일로 검색 결과를 내보냅니다. 이 옵션을 사용 하면 검토자가 각 항목의 원래 사서함 폴더 구조를 탐색할 필요 없이 시간순으로 항목을 검토할 수 있습니다 (보낸 날짜별로 항목이 정렬 됨).</span><span class="sxs-lookup"><span data-stu-id="df5fb-p115">**One PST file containing all messages in a single folder** - Exports search results to a single PST file where all messages are located in a single, top-level folder. This option lets reviewers review items in chronological order (items are sorted by sent date) without having to navigate the original mailbox folder structure for each item.</span></span> 
    
    - <span data-ttu-id="df5fb-p116">**개별 메시지** -.msg 형식을 사용 하 여 검색 결과를 개별 전자 메일 메시지로 내보냅니다. 이 옵션을 선택 하면 전자 메일 검색 결과가 파일 시스템의 폴더로 내보내집니다. 개별 메시지에 대 한 폴더 경로는 결과를 PST 파일로 내보낸 경우 사용 하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p116">**Individual messages** - Exports search results as individual email messages, using the .msg format. If you select this option, email search results are exported to a folder in the file system. The folder path for individual messages is the same as the one used if you exported the results to PST files.</span></span> 
    
      > [!IMPORTANT]
      > <span data-ttu-id="df5fb-p117">RMS 암호화 메시지를 내보낼 때 암호를 해독 하려면 전자 메일 검색 결과를 개별 메시지로 내보내야 합니다. 검색 결과를 PST 파일로 내보내는 경우 암호화 된 메시지는 암호화 된 상태로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p117">To decrypt RMS-encrypted messages when they're exported, you must export email search results as individual messages. Encrypted messages will remain encrypted if you export the search results as a PST file.</span></span> 
  
8. <span data-ttu-id="df5fb-p118">중복 메시지를 제외 하려면 **중복 제거 사용** 확인란을 클릭 합니다. 이 옵션은 검색의 콘텐츠 원본에 Exchange 사서함 또는 공용 폴더가 포함 되어 있는 경우에만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p118">Click the **Enable de-duplication** checkbox to exclude duplicate messages. This option appears only if the content sources of the search includes Exchange mailboxes or public folders.</span></span> 
    
    <span data-ttu-id="df5fb-p119">이 옵션을 선택 하면 검색 된 사서함에서 같은 메시지의 복사본을 여러 개 찾은 경우에도 하나의 메시지 복사본만 내보내집니다. 중복 메시지의 복사본을 포함 하는 사서함 이나 공용 폴더를 식별할 수 있도록 내보내기 결과 보고서 (results)에는 중복 메시지의 모든 복사본에 대 한 행이 포함 됩니다. 복제 제거 및 중복 항목이 식별 되는 방식에 대 한 자세한 내용은 [eDiscovery 검색 결과의 중복](de-duplication-in-ediscovery-search-results.md)제거를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p119">If you select this option, only one copy of a message will be exported even if multiple copies of the same message are found in the mailboxes that were searched. The export results report (Results.csv) will contain a row for every copy of a duplicate message so that you can identify the mailboxes (or public folders) that contain a copy of the duplicate message. For more information about de-duplication and how duplicate items are identified, see [De-duplication in eDiscovery search results](de-duplication-in-ediscovery-search-results.md).</span></span>
    
9. <span data-ttu-id="df5fb-p120">**sharepoint 문서 버전 포함** 확인란을 클릭 하 여 모든 sharepoint 문서 버전을 내보냅니다. 이 옵션은 검색의 콘텐츠 원본에 SharePoint 또는 비즈니스용 OneDrive 사이트를 포함 하는 경우에만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p120">Click the **Include versions for SharePoint documents** checkbox to export all versions of SharePoint documents. This option appears only if the content sources of the search includes SharePoint or OneDrive for Business sites.</span></span> 
    
10. <span data-ttu-id="df5fb-p121">**압축 (zip) 폴더에서 파일 내보내기** 확인란을 클릭 하 여 검색 결과를 압축 된 폴더로 내보냅니다. 이 옵션은 Exchange 항목을 개별 메시지로 내보내도록 선택 하 고 검색 결과에 SharePoint 또는 OneDrive 문서가 포함 되어 있는 경우에만 사용할 수 있습니다. 이 옵션은 항목을 내보낼 때 Windows 파일 경로 이름의 260 문자 제한을 해결 하는 데 주로 사용 됩니다. [추가 정보](#more-information) 섹션에서 "내보낸 항목의 파일 이름"을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p121">Click the **Export files in a compressed (zipped) folder** checkbox to export search results to compressed folders. This option is available only when you choose to export Exchange items as individual messages and when the search results include SharePoint or OneDrive documents. This option is primarily used to work around the 260 character limit in Windows file path names when items are exported. See the "Filenames of exported items" in the [More information](#more-information) section.</span></span> 
    
11. <span data-ttu-id="df5fb-181">**내보내기 시작**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-181">Click **Start export**.</span></span>
    
    <span data-ttu-id="df5fb-p122">검색 결과를 다운로드 하기 위해 준비 중 이며,이는 Microsoft 클라우드의 Azure 저장소 위치에 업로드 되 고 있음을 의미 합니다. 검색 결과를 다운로드할 준비가 되 면 세부 정보 창에서 **컴퓨터로 결과 내보내기** 링크 아래에 **내보낸 결과 다운로드** 링크가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p122">The search results are prepared for downloading, which means they're being uploaded to the Azure storage location in the Microsoft cloud. When the search results are ready for download, the **Download exported results** link is displayed under **Export results to a computer** in the details pane.</span></span> 
  
## <a name="step-2-download-the-search-results"></a><span data-ttu-id="df5fb-184">2단계: 검색 결과 다운로드</span><span class="sxs-lookup"><span data-stu-id="df5fb-184">Step 2: Download the search results</span></span>

<span data-ttu-id="df5fb-185">다음 단계에서는 Azure 저장소 위치에서 로컬 컴퓨터로의 검색 결과를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-185">The next step is to download the search results from the Azure storage location to your local computer.</span></span>
  
<span data-ttu-id="df5fb-p123">앞에서 설명한 것 처럼 검색 결과를 내보내는 데 사용 하는 컴퓨터에서 Windows 레지스트리 설정을 구성 하 여 다운로드 속도를 높일 수 있습니다. 자세한 내용은 [Office 365에서 eDiscovery 검색 결과를 내보낼 때 다운로드 속도 높이기](increase-download-speeds-when-exporting-ediscovery-results.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p123">As previously explained, you can increase the download speed by configuring a Windows Registry setting on the computer you use to export the search results. For more information, see [Increase the download speed when exporting eDiscovery search results from Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).</span></span>
  
1. <span data-ttu-id="df5fb-188">내보내기를 시작한 검색에 대한 세부 정보 창의 **컴퓨터에 결과 내보내기**에서 **내보낸 결과 다운로드**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-188">In the details pane for the search that you started the export for, under **Export results to a computer**, click **Download exported results**.</span></span>
    
    <span data-ttu-id="df5fb-189">**내보낸 결과 다운로드** 창이 표시 되 고 컴퓨터로 다운로드 될 검색 결과에 대 한 다음 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-189">The **Download exported results** window is displayed and contains the following information about the search results that will be downloaded to your computer.</span></span> 
    
    - <span data-ttu-id="df5fb-190">다운로드될 항목의 수</span><span class="sxs-lookup"><span data-stu-id="df5fb-190">The number of items that will be downloaded.</span></span>
    
    - <span data-ttu-id="df5fb-191">다운로드될 항목의 예상 총 크기</span><span class="sxs-lookup"><span data-stu-id="df5fb-191">The estimated total size of the items that will be downloaded.</span></span>
    
    - <span data-ttu-id="df5fb-p124">인덱싱된 항목 또는 인덱싱되지 않은 항목을 내보낼지 여부 인덱싱되지 않은 항목은 인식되는 형식을 갖거나 암호화되었거나, 다른 이유로 인덱싱되지 않은 항목입니다. 자세한 내용은 [Unindexed items in Content Search](partially-indexed-items-in-content-search.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p124">Whether indexed or unindexed will be exported. Unindexed items are items that have an recognized format, are encrypted, or weren't indexed for other reasons. For more information, see [Unindexed items in Content Search](partially-indexed-items-in-content-search.md).</span></span>
    
    - <span data-ttu-id="df5fb-195">SharePoint 문서의 버전을 다운로드할지 여부</span><span class="sxs-lookup"><span data-stu-id="df5fb-195">Whether or not versions of SharePoint documents will be downloaded.</span></span>
    
    - <span data-ttu-id="df5fb-p125">내보내기 준비 프로세스의 상태 데이터 준비가 완료되지 않았더라도 검색 결과 다운로드를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p125">The status of the export preparation process. You can start downloading search results even if the preparation of the data isn't complete.</span></span>
    
2. <span data-ttu-id="df5fb-p126">**내보내기 키**에서 **클립보드로 복사**를 클릭합니다. 5단계에서 이 키를 사용하여 검색 결과를 다운로드하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p126">Under **Export key**, click **Copy to clipboard**. You will use this key in step 5 to download the search results.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="df5fb-200">누구나 eDiscovery 내보내기 도구를 설치하여 시작하고 이 키를 사용하여 검색 결과를 다운로드할 수 있으므로 암호나 기타 보안 관련 정보를 보호할 때처럼 이 키를 주의해서 보호해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-200">Because anyone can install and start the eDiscovery Export tool, and then use this key to download the search results, be sure to take precautions to protect this key just like you would protect passwords or other security-related information.</span></span> 
  
3. <span data-ttu-id="df5fb-201">**결과 다운로드**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-201">Click **Download results**.</span></span>
    
4. <span data-ttu-id="df5fb-202">**MicrosoftOffice 365 eDiscovery 내보내기 도구**를 설치 하 라는 메시지가 표시 되 면 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-202">If you're prompted to install the **MicrosoftOffice 365 eDiscovery Export Tool**, click **Install**.</span></span>
    
5. <span data-ttu-id="df5fb-203">**eDiscovery 내보내기 도구**에서 5단계에서 복사한 내보내기 키를 해당 상자에 붙여 넣습니다. </span><span class="sxs-lookup"><span data-stu-id="df5fb-203">In the **eDiscovery Export Tool**, paste the export key that you copied in step 2 in the appropriate box.</span></span>
    
6. <span data-ttu-id="df5fb-204">**찾아보기**를 클릭하여 검색 결과 파일을 다운로드하려는 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-204">Click **Browse** to specify the location where you want to download the search result files.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="df5fb-205">디스크 작업 양이 많은 경우 (읽기 및 쓰기), 검색 결과를 로컬 디스크 드라이브로 다운로드 해야 합니다. 매핑된 네트워크 드라이브 또는 다른 네트워크 위치로 다운로드 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="df5fb-205">Due to the high amount of disk activity (reads and writes), you should download search results to a local disk drive; don't download them to a mapped network drive or other network location.</span></span> 
  
1. <span data-ttu-id="df5fb-206">**시작**을 클릭하여 컴퓨터에 검색 결과를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-206">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="df5fb-p127">**eDiscovery 내보내기 도구** 는 다운로드 되는 나머지 항목의 번호 및 크기를 포함 하 여 내보내기 프로세스에 대 한 상태 정보를 표시 합니다. 내보내기 프로세스가 완료 되 면 다운로드 한 위치에서 파일에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p127">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded. When the export process is complete, you can access the files in the location where they were downloaded.</span></span> 
    

  
## <a name="more-information"></a><span data-ttu-id="df5fb-209">추가 정보</span><span class="sxs-lookup"><span data-stu-id="df5fb-209">More information</span></span>

<span data-ttu-id="df5fb-210">검색 결과를 내보내는 방법에 대 한 자세한 내용은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-210">Here's more information about exporting search results.</span></span>
  
[<span data-ttu-id="df5fb-211">내보내기 제한</span><span class="sxs-lookup"><span data-stu-id="df5fb-211">Export limits</span></span>](#export-limits)
  
[<span data-ttu-id="df5fb-212">보고서 내보내기</span><span class="sxs-lookup"><span data-stu-id="df5fb-212">Export reports</span></span>](#export-reports)
  
[<span data-ttu-id="df5fb-213">부분적으로 인덱싱된 항목 내보내기</span><span class="sxs-lookup"><span data-stu-id="df5fb-213">Exporting partially indexed items</span></span>](#exporting-partially-indexed-items)

[<span data-ttu-id="df5fb-214">개별 메시지 또는 PST 파일 내보내기</span><span class="sxs-lookup"><span data-stu-id="df5fb-214">Exporting individual messages or PST files</span></span>](#exporting-individual-messages-or-pst-files)
  
[<span data-ttu-id="df5fb-215">RMS 암호화 메시지 암호 해독</span><span class="sxs-lookup"><span data-stu-id="df5fb-215">Decrypting RMS-encrypted messages</span></span>](#decrypting-rms-encrypted-messages)

[<span data-ttu-id="df5fb-216">내보낸 항목의 파일 이름</span><span class="sxs-lookup"><span data-stu-id="df5fb-216">Filenames of exported items</span></span>](#filenames-of-exported-items)  
  
[<span data-ttu-id="df5fb-217">기타</span><span class="sxs-lookup"><span data-stu-id="df5fb-217">Miscellaneous</span></span>](#miscellaneous)
  
 ### <a name="export-limits"></a><span data-ttu-id="df5fb-218">내보내기 제한</span><span class="sxs-lookup"><span data-stu-id="df5fb-218">Export limits</span></span>
  
- <span data-ttu-id="df5fb-219">보안 &amp; 및 준수 센터에서 검색 결과를 내보낼 경우 다음과 같은 제한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-219">Exporting search results from the Security &amp; Compliance Center has the following limits:</span></span>
    
  - <span data-ttu-id="df5fb-p128">단일 콘텐츠 검색에서 최대 2tb 데이터를 내보낼 수 있습니다. 검색 결과가 2tb 보다 크면 날짜 범위 또는 기타 필터를 사용 하 여 검색 결과의 총 크기를 줄이는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p128">You can export a maximum of 2 TB of data from a single Content Search. If the search results are larger than 2 TB, consider using date ranges or other types of filters to decrease the total size of the search results.</span></span>
    
  - <span data-ttu-id="df5fb-222">조직은 하루 중 최대 2tb의 데이터를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-222">Your organization can export a maximum of 2 TB of data during a single day.</span></span>
    
  - <span data-ttu-id="df5fb-223">조직 내에서 동시에 최대 10개의 내보내기를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-223">You can have a maximum of 10 exports running at the same time within your organization.</span></span>
    
  - <span data-ttu-id="df5fb-224">단일 사용자가 동시에 최대 3 개의 내보내기를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-224">A single user can run a maximum of three exports at the same time.</span></span>

  > [!NOTE]
  > <span data-ttu-id="df5fb-225">또한 콘텐츠 검색에서 보고서를 내보낼 때 동시에 실행 되는 내보내기 수와 단일 사용자가 실행할 수 있는 내보내기 수에 대해 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-225">Exporting only the reports from a Content Search also counts against the number of exports running at the same time and the number of exports that a single user can run.</span></span>
    
- <span data-ttu-id="df5fb-226">앞에서 설명한 것 처럼 사서함 및 사이트의 검색 결과는 [1 단계: 내보내기에 대 한 검색 결과 준비](#step-1-prepare-search-results-for-export)에 설명 된 대로 Azure 저장소 위치로 업로드 되며, 한 시간에 최대 2gb에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-226">As previously stated, search results from mailboxes and sites are uploaded to the Azure storage location (as described in [Step 1: Prepare search results for export](#step-1-prepare-search-results-for-export)) at a maximum rate of 2 GB per hour.</span></span>
    
- <span data-ttu-id="df5fb-p129">내보낼 수 있는 최대 PST 파일 크기는 기본적으로 10gb입니다. 즉, 사용자 사서함의 검색 결과가 10gb 보다 크면 사서함에 대 한 검색 결과를 두 개 이상의 개별 PST 파일로 내보냅니다. 또한 모든 검색 결과를 단일 PST 파일에 내보내도록 선택한 경우 총 검색 결과 크기가 10gb 보다 크면 pst 파일이 추가 pst 파일로 spilt 됩니다. 이 기본 크기를 변경 하려는 경우 검색 결과를 내보내는 데 사용 하는 컴퓨터에서 Windows 레지스트리를 편집할 수 있습니다. [eDiscovery 검색 결과를 내보낼 때 PST 파일 크기 변경을](change-the-size-of-pst-files-when-exporting-results.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p129">The maximum size of a PST file that can be exported is 10 GB by default. That means if the search results from a user's mailbox are larger than 10 GB, the search results for the mailbox will be exported in two (or more) separate PST files. Additionally, if you choose to export all search results in a single PST file, the PST file will be spilt into additional PST files if the total size of the search results is larger than 10 GB. If you want to change this default size, you can edit the Windows Registry on the computer that you use to export the search results. See [Change the size of PST files when exporting eDiscovery search results](change-the-size-of-pst-files-when-exporting-results.md).</span></span>
    
    <span data-ttu-id="df5fb-p130">또한 단일 사서함의 콘텐츠가 10gb 보다 많은 경우 특정 사서함의 검색 결과는 여러 PST 파일로 분할 되지 않습니다. 단일 폴더에 있는 모든 메시지를 포함 하는 하나의 PST 파일로 검색 결과를 내보내고 검색 결과가 10gb 보다 크면 해당 항목은 계속 해 서 시간순으로 구성 되어 있으므로 전송 된 d에 따라 추가 PST 파일에 spilt 됩니다. 쇠.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p130">Additionally, the search results from a specific mailbox won't be divided among multiple PST files unless the content from a single mailbox is more than 10 GB. If you chose to export the search results in one PST file for that contains all messages in a single folder and the search results are larger than 10 GB, the items are still organized in chronological order, so they will be spilt into additional PST files based on the sent date.</span></span>
     
 ### <a name="export-reports"></a><span data-ttu-id="df5fb-234">보고서 내보내기</span><span class="sxs-lookup"><span data-stu-id="df5fb-234">Export reports</span></span>
  
- <span data-ttu-id="df5fb-235">검색 결과를 내보낼 때 검색 결과 외에 다음과 같은 보고서가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-235">When you export search results, the following reports are included in addition to the search results.</span></span>
    
  - <span data-ttu-id="df5fb-p131">**내보내기 요약** 내보내기에 대 한 요약이 포함 된 Excel 문서입니다. 여기에는 검색 된 콘텐츠 원본 수, 예상 및 다운로드 되는 search 결과 크기, 그리고 내보낸 항목의 예상 및 다운로드 된 항목과 같은 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p131">**Export Summary** An Excel document that contains a summary of the export. This includes information such as the number of content sources that were searched, the estimated and downloaded sizes of the search results, and the estimated and downloaded number of items that were exported.</span></span> 
    
  - <span data-ttu-id="df5fb-238">**매니페스트** 검색 결과에 포함 된 각 항목에 대 한 정보를 포함 하는 매니페스트 파일 (XML 형식)입니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-238">**Manifest** A manifest file (in XML format) that contains information about each item included in the search results.</span></span> 
    
  - <span data-ttu-id="df5fb-p132">**결과가** 검색 결과로 다운로드 되는 각 항목에 대 한 정보가 포함 된 Excel 문서입니다. 전자 메일의 경우 결과 로그에 다음을 비롯 한 각 메시지에 대 한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p132">**Results** An Excel document that contains information about each item that is download as a search result. For email, the result log contains information about each message, including:</span></span> 
    
      - <span data-ttu-id="df5fb-241">원본 사서함에 있는 메시지의 위치 (포함 여부는 주 메시지는 보관 사서함 또는).</span><span class="sxs-lookup"><span data-stu-id="df5fb-241">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
        
      - <span data-ttu-id="df5fb-242">메시지가 전송된 날짜</span><span class="sxs-lookup"><span data-stu-id="df5fb-242">The date the message was sent or received.</span></span>
        
      - <span data-ttu-id="df5fb-243">메시지의 제목 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-243">The Subject line from the message.</span></span>
        
      - <span data-ttu-id="df5fb-244">보낸 사람 및 메시지 받는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-244">The sender and recipients of the message.</span></span>
        
      - <span data-ttu-id="df5fb-p133">검색 결과를 내보낼 때 중복 제거 옵션을 사용 하도록 설정한 경우 메시지가 중복 메시지 인지 여부 중복 메시지의 경우 중복 된 메시지를 식별 하는 값이 중복 **항목** 열에 포함 됩니다. **중복 항목** 열에 있는 값은 내보낸 메시지의 항목 id를 포함 합니다. 자세한 내용은 [eDiscovery 검색 결과의 중복](de-duplication-in-ediscovery-search-results.md)제거를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p133">Whether the message is a duplicate message if you enabled the de-duplication option when exporting the search results. Duplicate messages will have a value in the **Duplicate to Item** column that identifies the message as a duplicate. The value in the **Duplicate to Item** column contains the item identity of the message that was exported. For more information, see [De-duplication in eDiscovery search results](de-duplication-in-ediscovery-search-results.md).</span></span>
        
      <span data-ttu-id="df5fb-249">SharePoint 및 비즈니스용 OneDrive 사이트의 문서에 대해 결과 로그에 다음을 비롯 한 각 문서에 대 한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-249">For documents from SharePoint and OneDrive for Business sites, the result log contains information about each document, including:</span></span>
        
      - <span data-ttu-id="df5fb-250">문서에 대 한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-250">The URL for the document.</span></span>
        
      - <span data-ttu-id="df5fb-251">문서가 있는 사이트 모음의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-251">The URL for the site collection where the document is located.</span></span>
        
      - <span data-ttu-id="df5fb-252">문서를 마지막으로 수정한 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-252">The date that the document was last modified.</span></span>
        
      - <span data-ttu-id="df5fb-253">이름 (에 있는 제목 열 결과 로그에서) 문서입니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-253">The name of the document (which is located in the Subject column in the result log).</span></span>
    
  - <span data-ttu-id="df5fb-p134">**인덱싱되지 않은 항목** 검색 결과에 포함 될 부분 인덱싱된 모든 항목에 대 한 정보가 포함 된 Excel 문서입니다. 검색 결과 보고서를 생성할 때 부분적으로 인덱싱된 항목을 포함 하지 않으면이 보고서는 계속 다운로드 되지만 비어 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p134">**Unindexed Items** An Excel document that contains information about any partially indexed items that would be included in the search results. If you don't include partially indexed items when you generate the search results report, this report will still be downloaded, but will be empty.</span></span> 
    
  - <span data-ttu-id="df5fb-p135">**오류 및 경고** 내보내는 동안 발생 한 파일에 대 한 오류 및 경고를 포함 합니다. 각 개별 오류 또는 경고와 관련 된 정보는 오류 세부 정보 열을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p135">**Errors and Warnings** Contains errors and warnings for files encountered during export. See the Error Details column for information specific to each individual error or warning.</span></span> 
    
  - <span data-ttu-id="df5fb-p136">**건너뛴 항목** SharePoint 및 비즈니스용 OneDrive 사이트에서 검색 결과를 내보낼 때는 일반적으로 건너뛴 항목 보고서 (대해 skippeditems)가 내보내기에 포함 됩니다. 이 보고서에 언급 된 항목은 일반적으로 폴더 또는 문서 집합과 같이 다운로드 되지 않는 항목입니다. 이 항목 유형을 내보내지 않는 것은 의도적으로 설계 된 것입니다. 건너뛴 다른 항목의 경우 건너뛴 항목 보고서의 ' 오류 유형 ' 및 ' 오류 세부 정보 ' 필드에는 항목이 생략 된 이유가 표시 되 고 다른 검색 결과와 함께 다운로드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p136">**Skipped Items** When you export search results from SharePoint and OneDrive for Business sites, the export will usually include a skipped items report (SkippedItems.csv). The items cited in this report are typically items that won't be downloaded, such as a folder or a document set. Not exporting this types of items is by design. For other items that were skipped, the 'Error Type' and 'Error Details' field in the skipped items report show the reason the item was skipped and wasn't download with the other search results.</span></span> 
    
  - <span data-ttu-id="df5fb-262">**추적 로그** 내보내기 프로세스에 대 한 자세한 로깅 정보와 내보내기 중 문제를 파악 하는 데 도움이 되는 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-262">**Trace Log** Contains detailed logging information about the export process and can help uncover issues during export.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="df5fb-p137">실제 검색 결과를 내보내지 않고도 이러한 문서를 내보낼 수 있습니다. [콘텐츠 검색 보고서 내보내기를](export-a-content-search-report.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p137">You can just export these documents without having to export the actual search results. See [Export a Content Search report](export-a-content-search-report.md).</span></span> 
  
 ### <a name="exporting-partially-indexed-items"></a><span data-ttu-id="df5fb-265">부분적으로 인덱싱된 항목 내보내기</span><span class="sxs-lookup"><span data-stu-id="df5fb-265">Exporting partially indexed items</span></span>
  
- <span data-ttu-id="df5fb-p138">검색 결과의 모든 사서함 항목을 반환 하는 콘텐츠 검색에서 사서함 항목을 내보내는 경우 (검색 쿼리에 포함 된 키워드가 없는 경우) 부분적으로 인덱싱된 항목이 인덱싱되지 않은 항목을 포함 하는 PST 파일에 복사 되지 않습니다. 이는 부분적으로 인덱싱된 항목을 비롯 한 모든 항목이 일반 검색 결과에 자동으로 포함 되기 때문입니다. 즉, 부분적으로 인덱싱된 항목은 인덱싱된 다른 항목을 포함 하는 PST 파일이 나 개별 메시지에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p138">If you're exporting mailbox items from a content search that returns all mailbox items in the search results (because no keywords where included in the search query), partially indexed items won't be copied to the PST file that contains the unindexed items. This is because all items, including any partially indexed items, are automatically included in the regular search results. This means that partially indexed items will be included in a PST file (or as individual messages) that contains the other, indexed items.</span></span>
    
    <span data-ttu-id="df5fb-p139">또한 인덱싱된 항목과 부분적으로 인덱싱된 항목을 모두 내보내는 경우 또는 모든 항목을 반환 하는 콘텐츠 검색에서 인덱싱된 항목만 내보내는 경우 같은 수의 항목이 다운로드 됩니다. 이는 콘텐츠 검색에 대 한 예상 검색 결과 (보안 &amp; 및 준수 센터의 검색 통계에 표시 됨)가 여전히 부분적으로 인덱싱된 항목의 수에 대 한 별도의 예측이 포함 되는 경우에도 마찬가지입니다. 예를 들어 검색 쿼리에 키워드가 없는 모든 항목을 포함 하는 검색에 대 한 예상은 1000 항목이 발견 되 고 해당 200 부분 인덱싱된 항목도 검색 되었음을 나타냅니다. 이 경우에는 검색에서 모든 항목이 반환 되므로 1000 항목에 부분적으로 인덱싱된 항목이 포함 되어 있습니다. 즉, 검색에서 반환 되는 총 항목은 1000, 1200 항목 (예상 대로)은 아닙니다. 이 검색의 결과를 내보내고 인덱싱된 항목과 부분 인덱싱된 항목 (또는 인덱싱된 항목만)을 내보내도록 선택 하면 1000 항목이 다운로드 됩니다. 다시 말하지만, 빈 검색 쿼리를 사용 하 여 모든 항목을 반환 하면 부분적으로 인덱싱된 항목이 일반 (인덱싱된) 결과에 포함 되기 때문입니다. 이 예에서 부분적으로 인덱싱된 항목만 내보내도록 선택한 경우 200 인덱싱되지 않은 항목만 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p139">Additionally, if you export both the indexed and partially indexed items or if you export only the indexed items from a content search that returns all items, the same number of items will be downloaded. This happens even though the estimated search results for the content search (displayed in the search statistics in the Security &amp; Compliance Center) will still include a separate estimate for the number of partially indexed items. For example, let's say that the estimate for a search that includes all items (no keywords in the search query) shows that 1,000 items were found and that 200 partially indexed items were also found. In this case, the 1,000 items include the partially indexed items because the search returns all items. In other words, there are 1,000 total items returned by the search, and not 1,200 items (as you might expect). If you export the results of this search and choose to export indexed and partially indexed items (or just indexed items), then 1,000 items will be downloaded. Again, that's because partially indexed items are included with the regular (indexed) results when you use a blank search query to return all items. In this same example, if you choose to export only partially indexed items, then only the 200 unindexed items would be downloaded.</span></span>
    
    <span data-ttu-id="df5fb-277">또한 이전 예제에서 인덱싱 및 부분적으로 인덱싱된 항목을 내보내거나 인덱싱된 항목만 내보내는 경우 내보낸 검색 결과에 포함 된 **내보내기 요약** 보고서에는 1000 개 항목, 즉 예상 대로 제공 되는 1000 항목이 나열 됩니다. 앞에서 설명한 것과 같은 이유로 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-277">Also note that in the previous example (when you export indexed and partially indexed items or you export only indexed items) , the **Export Summary** report included with the exported search results would list 1,000 items estimated items and 1,000 downloaded items for the same reasons as previously described.</span></span> 
    
- <span data-ttu-id="df5fb-p140">결과를 내보내려는 검색에서 특정 콘텐츠 위치나 조직의 모든 콘텐츠 위치를 검색 한 경우 검색 조건과 일치 하는 항목을 포함 하는 콘텐츠 위치의 부분적 항목만 내보내집니다. 즉, 사서함 이나 사이트에서 검색 결과가 발견 되지 않으면 해당 사서함 이나 사이트에서 부분적으로 인덱싱된 항목을 내보내지 않습니다. 이는 조직의 여러 위치에서 부분적으로 인덱싱된 항목을 내보낼 때 내보내기 오류가 발생할 가능성이 높아지고 검색 결과를 내보내고 다운로드 하는 데 걸리는 시간이 길어질 수 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p140">If the search that you're exporting results from was a search of specific content locations or all content locations in your organization, only the partially items from content locations that contain items that match the search criteria will be exported. In other words, if no search results are found in a mailbox or site, then any partially indexed items in that mailbox or site won't be exported. The reason for this is that exporting partially indexed items from lots of locations in the organization might increase the likelihood of export errors and increase the time it takes to export and download the search results.</span></span>
    
    <span data-ttu-id="df5fb-281">검색에 대 한 모든 콘텐츠 위치에서 부분적으로 인덱싱된 항목을 내보내려면 검색 쿼리에서 키워드를 제거 하 여 모든 항목을 반환 하도록 검색을 구성한 다음 검색 결과를 내보낼 때 부분적으로 인덱싱된 항목만 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-281">To export partially indexed items from all content locations for a search, configure the search to return all items (by removing any keywords from the search query) and then export only partially indexed items when you export the search results.</span></span>
    
    ![, 인덱싱되지 않은 항목만 내보내려면 thrid 내보내기 옵션을 사용 합니다.](media/5d7be338-a0e5-425f-8ba5-92769c24bf75.png)
  
- <span data-ttu-id="df5fb-p141">SharePoint 또는 비즈니스용 OneDrive 사이트에서 검색 결과를 내보낼 때에는 사용자가 선택한 내보내기 옵션 및 검색 된 사이트에 search 조건과 일치 하는 인덱싱된 항목이 포함 되어 있는지 여부에 따라 인덱싱되지 않은 항목을 내보낼 수 있습니다. 예를 들어 특정 SharePoint 또는 비즈니스용 OneDrive 사이트를 검색 하는 경우 검색 결과가 발견 되지 않으면 두 번째 내보내기 옵션을 선택 하 여 인덱싱된 항목과 인덱싱되지 않은 항목을 모두 내보내는 경우 해당 사이트에서 인덱싱되지 않은 항목을 내보내지 않습니다. 사이트의 인덱싱된 항목이 검색 조건과 일치 하는 경우 인덱싱된 항목과 인덱싱되지 않은 항목을 모두 내보낼 때 해당 사이트에서 인덱싱되지 않은 모든 항목을 내보냅니다. 다음 그림에서는 사이트에 검색 조건과 일치 하는 인덱싱된 항목이 포함 되어 있는지 여부에 따라 내보내기 옵션을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p141">When exporting search results from SharePoint or OneDrive for Business sites, the ability to export unindexed items also depends on the export option that you select and whether a site that was searched contains an indexed item that matches the search criteria. For example, if you search specific SharePoint or OneDrive for Business sites and no search results are found, then no unindexed items from those sites will be exported if you choose the second export option to export both indexed and unindexed items. If an indexed item from a site does match the search criteria, then all unindexed items from that site will be exported when exporting both indexed and unindexed items. The following illustration describes the export options based on whether or not a site contains an indexed item that matches the search criteria.</span></span>
    
    ![사이트에 검색 조건과 일치 하는 인덱싱된 항목이 포함 되어 있는지 여부에 따라 내보내기 옵션을 선택 합니다.](media/94f78786-c6bb-42fb-96b3-7ea3998bcd39.png)

    
    <span data-ttu-id="df5fb-p142">A-검색 조건과 일치 하는 인덱스 된 항목만 내보냅니다. 부분적으로 인덱싱되지 않은 항목은 내보내지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p142">A - Only indexed items that matches the search criteria are exported. No partially indexed items are exported.</span></span>
    
    <span data-ttu-id="df5fb-p143">B-검색 조건과 일치 하는 인덱스 된 항목이 사이트에서 하나도 없는 경우에는 해당 사이트에서 부분적으로 인덱싱된 항목을 내보내지 않습니다. 사이트의 인덱싱된 항목이 검색 결과에 반환 되 면 해당 사이트에서 부분적으로 인덱싱된 항목이 내보내집니다. 즉, 검색 조건과 일치 하는 항목을 포함 하는 사이트의 부분적으로 인덱싱된 항목만 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p143">B - If no indexed items from a site match the search criteria, then partially indexed items from that same site aren't exported. If indexed items from a site are returned in the search results, then the partially indexed items from that site are exported. In other words, only the partially indexed items from sites that contain items that match the search criteria are exported.</span></span>
    
    <span data-ttu-id="df5fb-293">C-사이트에 검색 조건과 일치 하는 항목이 포함 되어 있는지 여부에 관계 없이 검색 중인 모든 사이트에서 모든 부분적으로 인덱싱된 항목을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-293">C - All partially indexed items from all sites in the search are exported, regardless of whether a site contains items that match the search criteria.</span></span>
    
    <span data-ttu-id="df5fb-294">부분적으로 인덱싱된 항목을 내보내도록 선택 하는 경우에는 **Exchange 콘텐츠를 내보낼 때**선택한 옵션에 관계 없이 부분적으로 인덱싱된 사서함 항목이 별도의 PST 파일로 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-294">If you choose to export partially indexed items, partially indexed mailbox items are exported in a separate PST file regardless of the option that you choose under **Export Exchange content as**.</span></span>

- <span data-ttu-id="df5fb-p144">부분적으로 인덱싱된 항목이 검색 결과에 반환 되는 경우에는 부분적으로 인덱싱된 항목의 다른 속성은 search 조건과 일치 하므로, 해당 부분 인덱스는 일반 검색 결과와 함께 내보내집니다. 따라서 인덱싱된 항목과 부분적으로 인덱싱된 항목을 모두 선택 하는 경우 ( **형식을 인식할 수 없거나, 암호화 되거나, 다른 이유** 내보내기 옵션을 위해 인덱싱되지 않은 항목 포함)를 선택 하는 경우 내보낸 부분 인덱싱된 항목 결과 .csv 보고서에는 일반적인 결과가 표시 됩니다. 이는 인덱싱되지 않은 항목 .csv 보고서에 나열 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p144">If partially indexed items are returned in the search results (because other properties of an partially indexed items matched the search criteria), then those partially indexed are exported with the regular search results. So, if you choose to export both indexed items and partially indexed items (by selecting the **All items, including ones that have unrecognized format, are encrypted, or weren't indexed for other reasons** export option), the partially indexed items exported with the regular results will be listed in the Results.csv report. They will not be listed in the Unindexed items.csv report.</span></span>
    
 ### <a name="exporting-individual-messages-or-pst-files"></a><span data-ttu-id="df5fb-298">개별 메시지 또는 PST 파일 내보내기</span><span class="sxs-lookup"><span data-stu-id="df5fb-298">Exporting individual messages or PST files</span></span>
  
- <span data-ttu-id="df5fb-p145">메시지의 파일 경로 이름이 Windows의 최대 문자 제한을 초과 하는 경우 파일 경로 이름이 잘립니다. 하지만 원본 파일 경로 이름이 매니페스트 및 ResultsLog에 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p145">If the file path name of a message exceeds the maximum character limit for Windows, the file path name is truncated. But the original file path name will be listed in the Manifest and ResultsLog.</span></span>
    
- <span data-ttu-id="df5fb-p146">앞에서 설명한 것 처럼 전자 메일 검색 결과는 파일 시스템의 폴더로 내보내집니다. 개별 메시지의 폴더 경로는 사용자 사서함의 폴더 경로를 복제 합니다. 예를 들어 사용자의 받은 편지함에 있는 "ContosoCase101" 라는 검색 메시지는 폴더 경로 `~ContosoCase101\\<date of export\Exchange\user@contoso.com (Primary)\Top of Information Store\Inbox`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p146">As previously explained, email search results are exported to a folder in the file system. The folder path for individual messages would replicate the folder path in the user's mailbox. For example, for a search named "ContosoCase101" messages in a user's inbox would be located in the folder path  `~ContosoCase101\\<date of export\Exchange\user@contoso.com (Primary)\Top of Information Store\Inbox`.</span></span> 
    
- <span data-ttu-id="df5fb-p147">단일 폴더에 있는 모든 메시지를 포함 하는 하나의 pst 파일에 전자 메일 메시지를 내보내도록 선택한 경우 **지운** 편지함 폴더와 **검색 폴더** 폴더는 최상위 pst 폴더에 포함 됩니다. 이 폴더는 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p147">If you choose to export email messages in one PST file containing all messages in a single folder, a **Deleted Items** folder and a **Search Folders** folder are included in the top level of the PST folder. These folders will be empty.</span></span> 
  
 ### <a name="decrypting-rms-encrypted-messages"></a><span data-ttu-id="df5fb-306">RMS 암호화 메시지 암호 해독</span><span class="sxs-lookup"><span data-stu-id="df5fb-306">Decrypting RMS-encrypted messages</span></span>
  
- <span data-ttu-id="df5fb-p148">앞에서 설명한 것 처럼 내보낼 때 RMS 암호화 메시지를 해독 하려면 검색 결과를 개별 메시지로 내보내야 합니다. 검색 결과를 PST 파일로 내보내는 경우 RMS 암호화 메시지는 암호화 된 상태로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p148">As previously explained, to decrypt RMS-encrypted messages when you export them, you have to export the search results as individual messages. If you export search results to a PST file, RMS-encrypted messages will remain encrypted.</span></span>
    
- <span data-ttu-id="df5fb-p149">콘텐츠 검색의 RMS 암호 해독 기능은 검색 결과를 내보낼 때 Office 365 메시지 암호화 (OME)로 암호화 된 메시지를 해독 하지 않습니다. 그러나 OME로 암호화 된 메시지가 조직의 사용자에 게 전송 되는 경우 사용자의 보낸 폴더에 있는 메시지의 복사본은 암호화 되지 않으며 내보낸 후에도 볼 수 있습니다. 그러나 OME로 암호화 된 메시지를 조직의 사용자가 수신 하는 경우에는 해당 메시지가 내보낸 후 암호 해독 되지 않습니다. OME에 대 한 자세한 내용은 [Office 365 메시지 암호화](https://go.microsoft.com/fwlink/p/?linkid=844966)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p149">The RMS decryption feature in Content Search doesn't decrypt messages encrypted with Office 365 Message Encryption (OME) when you export search results. However, if a message encrypted with OME is sent by a user in your organization, the copy of the message in the user's Sent folder isn't encrypted and will be viewable after it's exported. However, if messages encrypted with OME are received by users in your organization, they won't be decrypted after they're exported. For more information about OME, see [Office 365 Message Encryption](https://go.microsoft.com/fwlink/p/?linkid=844966).</span></span>
    
- <span data-ttu-id="df5fb-p150">해독 된 메시지는 **ResultsLog** 보고서에서 식별 됩니다. 이 보고서에는 **디코드 상태**라는 열이 있으며이 열에서 **디코딩된** 값은 암호가 해독 된 메시지를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p150">Messages that are decrypted are identified in the **ResultsLog** report. This report contains a column named **Decode Status**, and a value of **Decoded** in this column identifies the messages the were decrypted.</span></span> 
    
- <span data-ttu-id="df5fb-p151">현재이 암호 해독 기능에는 SharePoint 및 비즈니스용 OneDrive 사이트의 암호화 된 콘텐츠가 포함 되지 않습니다. RMS 암호화 전자 메일 메시지만 내보낼 때 암호가 해독 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p151">Currently, this decryption capability doesn't include encrypted content from SharePoint and OneDrive for Business sites. Only RMS-encrypted email messages will be decrypted when you export them.</span></span>
    
- <span data-ttu-id="df5fb-317">RMS 암호화 전자 메일 메시지에 암호화 된 첨부 파일 (예: 문서 또는 다른 전자 메일 메시지)이 있는 경우 최상위 전자 메일 메시지만 해독 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-317">If an RMS-encrypted email message has an attachment (such as a document or another email message) that's also encrypted, only the top-level email message will be decrypted.</span></span>
    
- <span data-ttu-id="df5fb-p152">RMS 암호화 전자 메일 메시지를 미리 볼 수는 없습니다. 암호화 된 메시지를 보려면 내보내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p152">You can't preview an RMS-encrypted email message. To view an encrypted message, you have to export it.</span></span>
    
- <span data-ttu-id="df5fb-p153">누군가 RMS 암호화 메시지의 암호를 해독 하지 못하도록 하려면 기본 제공 eDiscovery 관리자 역할 그룹을 복사 하 여 사용자 지정 역할 그룹을 만든 다음 사용자 지정 역할 그룹에서 RMS 암호 해독 관리 역할을 제거 해야 합니다. 그런 다음 메시지의 암호를 해독 하지 않으려는 사용자를 사용자 지정 역할 그룹의 구성원으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p153">If you need to prevent someone from decrypting RMS-encrypted messages, you'll have to create a custom role group (by copying the built-in eDiscovery Manager role group) and then remove the RMS Decrypt management role from the custom role group. Then add the person who you don't want to decrypt messages as a member of the custom role group.</span></span>
  
 ### <a name="filenames-of-exported-items"></a><span data-ttu-id="df5fb-322">내보낸 항목의 파일 이름</span><span class="sxs-lookup"><span data-stu-id="df5fb-322">Filenames of exported items</span></span>
  
- <span data-ttu-id="df5fb-p154">로컬 컴퓨터로 내보낸 전자 메일 메시지 및 사이트 문서에 대 한 전체 경로 이름에는 260 자 제한이 있습니다 (운영 체제에 의해 부과 됨). 내보낸 항목의 전체 경로 이름에는 항목의 원래 위치와 검색 결과가 다운로드 되는 로컬 컴퓨터의 폴더 위치가 포함 됩니다. 예를 들어 eDiscovery 내보내기 도구에서 검색 결과를 `C:\Users\Admin\Desktop\SearchResults` 다운로드 하도록 지정 하는 경우 다운로드 한 전자 메일 항목의 전체 경로 이름은 `C:\Users\Admin\Desktop\SearchResults\ContentSearch1\03.15.2017-1242PM\Exchange\sarad@contoso.com (Primary)\Top of Information Store\Inbox\Insider trading investigation.msg`입니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p154">There is a 260-character limit (imposed by the operating system) for the full path name for email messages and site documents exported to your local computer. The full path name for exported items includes the item's original location and the folder location on the local computer where the search results are downloaded to. For example, if you specify to download the search results to  `C:\Users\Admin\Desktop\SearchResults` in the eDiscovery Export tool, then the full pathname for a downloaded email item would be  `C:\Users\Admin\Desktop\SearchResults\ContentSearch1\03.15.2017-1242PM\Exchange\sarad@contoso.com (Primary)\Top of Information Store\Inbox\Insider trading investigation.msg`.</span></span>
    
    <span data-ttu-id="df5fb-326">260 문자 제한이 초과 되는 경우에는 항목의 전체 경로 이름이 잘립니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-326">If the 260-character limit is exceeded, the full path name for an item will be truncated.</span></span>
    
  - <span data-ttu-id="df5fb-327">전체 경로 이름이 260 자를 넘으면 파일 이름이 제한 미만으로 단축 됩니다. 잘린 파일 이름 (확장명 제외)은 8 자 미만 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-327">If the full path name is longer than 260 characters, the file name will be shortened to get under the limit; note that the truncated filename (excluding the file extension) won't be less than 8 characters.</span></span>
    
  - <span data-ttu-id="df5fb-p155">파일 이름을 단축 하 고 전체 경로 이름이 여전히 너무 긴 경우에는 항목이 현재 위치에서 상위 폴더로 이동 됩니다. 경로 이름이 여전히 너무 길면 프로세스가 반복 되 고, 파일 이름을 짧게 줄인 다음 다시 상위 폴더로 이동 합니다. 이 프로세스는 전체 경로 이름이 260 문자 제한 미만으로 반복 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p155">If the full path name is still too long after shortening the file name, the item is moved from its current location to the parent folder. If the pathname is still too long, then the process is repeated: shorten the filename, and if necessary move again to the parent folder. This process is repeated until the full pathname is under the 260-character limit.</span></span>
    
  - <span data-ttu-id="df5fb-331">잘린 전체 경로 이름이 이미 있으면 파일 이름 끝에 버전 번호가 추가 됩니다. 예를 `statusmessage(2).msg`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-331">If a truncated full path name already exists, a version number will be added to the end of the filename; for example,  `statusmessage(2).msg`.</span></span>
    
    <span data-ttu-id="df5fb-332">이 문제를 완화 하려면 짧은 경로 이름을 사용 하 여 검색 결과를 위치에 다운로드 하는 것이 좋습니다. 예를 들어 이름이 이라는 `C:\Results` 폴더로 검색 결과를 다운로드 하는 것 보다 내보낸 항목의 경로 이름에 대 한 문자가 추가 됩니다. `C:\Users\Admin\Desktop\Results`</span><span class="sxs-lookup"><span data-stu-id="df5fb-332">To help mitigate this issue, consider downloading search results to a location with a short path name; for example, downloading search results to a folder named  `C:\Results` would add fewer characters to the path names of exported items than downloading them to a folder named  `C:\Users\Admin\Desktop\Results`.</span></span>
    
- <span data-ttu-id="df5fb-p156">사이트 문서를 내보낼 때 문서의 원래 파일 이름도 수정 될 수 있습니다. 이 작업은 보류 중인 SharePoint 또는 비즈니스용 OneDrive 사이트에서 삭제 된 문서에 대해 특별히 수행 됩니다. 보류 중인 사이트에 있는 문서를 삭제 하면 삭제 된 문서는 사이트에 대 한 보존 보류 라이브러리로 자동으로 이동 됩니다 (사이트가 보류 되었을 때 만들어짐). 삭제 된 문서를 보존 보류 라이브러리로 이동 하면 문서의 원래 파일 이름에 임의로 생성 된 고유 ID가 추가 됩니다. 예를 들어 문서에 대 한 파일 이름이 `FY2017Budget.xlsx` 있고 나중에 해당 문서를 삭제 하 여 보존 보류 라이브러리로 이동한 경우에는 보존 보류 라이브러리로 이동 된 문서의 파일 이름이 다음과 같이 `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx`수정 됩니다. 보존 보류 라이브러리의 문서가 콘텐츠 검색의 쿼리와 일치 하 고 해당 검색의 결과를 내보내는 경우 내보낸 파일의 파일 이름이 수정 됩니다. 이 예에서 내보낸 문서의 파일 이름은 `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx`입니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p156">When you export site documents, it's also possible that the original file name of a document will be modified. This happens specifically for documents that have been deleted from a SharePoint or OneDrive for Business site that's been placed on hold. After a document that's located on a site that's on hold is deleted, the deleted document is automatically moved to the Preservation Hold library for the site (which was created when the site was placed on hold). When the deleted document is moved to the Preservation Hold library, a randomly-generated and unique ID is appended to the original filename of the document. For example, if the filename for a document is  `FY2017Budget.xlsx` and that document is later deleted and moved to the Preservation Hold library, the filename of the document that is moved to the Preservation Hold library is modified to something like  `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx`. If a document in the Preservation Hold library matches the query of a Content Search and you export the results of that search, the exported file will have the modified filename; in this example, the filename of the exported document would be  `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx`.</span></span>
    
    <span data-ttu-id="df5fb-p157">또한 보류 중인 사이트에 있는 문서를 수정 하 고 사이트의 문서 라이브러리에 대 한 버전 관리를 사용 하도록 설정한 경우 파일의 복사본이 보존 보류 라이브러리에 자동으로 만들어집니다. 이 경우에는 보존 보류 라이브러리에 복사 되는 문서의 파일 이름에 임의로 생성 되는 고유 ID도 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p157">Additionally, when a document located on a site that's on hold is modified (and versioning for the document library in the site has been enabled), a copy of the file is automatically created in the Preservation Hold library. In this case, a randomly-generated and unique ID is also appended to the filename of the document that's copied to the Preservation Hold library.</span></span>
    
    <span data-ttu-id="df5fb-p158">보존 보류 라이브러리로 이동 되거나 복사 되는 문서의 파일 이름이 충돌 하는 것을 방지 하기 위한 이유는 다음과 같습니다. 사이트 및 보존 보류 라이브러리를 유지 하는 방법에 대 한 자세한 내용은 [SharePoint Server 2016의 원본 위치 유지 개요](https://support.office.com/article/5e400d68-cd51-444a-8fe6-e4df1d20aa95)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p158">The reason why filenames of documents that are moved or copied to the Preservation Hold library is to prevent conflicting filenames. For more information about placing a hold on sites and the Preservation Hold library, see [Overview of in-place hold in SharePoint Server 2016](https://support.office.com/article/5e400d68-cd51-444a-8fe6-e4df1d20aa95).</span></span>
    
 ### <a name="miscellaneous"></a><span data-ttu-id="df5fb-343">기타</span><span class="sxs-lookup"><span data-stu-id="df5fb-343">Miscellaneous</span></span>
  
- <span data-ttu-id="df5fb-p159">모든 검색 결과 및 내보내기 보고서는 콘텐츠 검색과 이름이 같은 폴더에 포함 됩니다. 내보낸 전자 메일 메시지는 **Exchange**라는 폴더에 있습니다. 문서는 **SharePoint**라는 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p159">All search results and the export reports are included in a folder that has the same name as the Content Search. The email messages that were exported are located in a folder named **Exchange**. Documents are located in a folder named **SharePoint**.</span></span> 
    
- <span data-ttu-id="df5fb-p160">SharePoint의 문서 및 비즈니스용 OneDrive 사이트에 대 한 파일 시스템 메타 데이터는 로컬 컴퓨터로 문서를 내보낼 때 유지 됩니다. 이는 문서를 내보낼 때 만든 날짜와 마지막으로 수정한 날짜가 아닌 문서 속성이 변경 되지 않음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p160">The file system metadata for documents on SharePoint and OneDrive for Business sites is maintained when documents are exported to your local computer. That means document properties, such as created and last modified dates, aren't changed when documents are exported.</span></span>

- <span data-ttu-id="df5fb-p161">검색 쿼리와 일치 하는 목록 항목이 SharePoint에서 검색 결과에 포함 되어 있으면 검색 쿼리와 일치 하는 항목 외에도 목록의 모든 행이 내보내집니다. 여기에는 목록의 모든 첨부 파일이 포함 됩니다. 이는 검색 결과에서 반환 되는 목록 항목에 대 한 컨텍스트를 제공 하기 위한 것입니다. 또한 추가 목록 항목 및 첨부 파일의 경우 내보낸 항목의 수가 검색 결과의 원래 예상 값과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df5fb-p161">If your search results include a list item from SharePoint that matches the search query, all rows in the list will be exported in addition to the item that matches the search query. This includes any attachments in the list. The reason for this is to provide a context for list items that are returned in the search results. Also note that the additional list items and attachments may cause the count of exported items to be different than the original estimate of search results.</span></span>
