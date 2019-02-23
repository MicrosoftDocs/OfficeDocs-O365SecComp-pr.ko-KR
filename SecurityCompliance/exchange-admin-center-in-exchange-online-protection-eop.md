---
title: 'Exchange Online Protection의 Exchange 관리 센터 '
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 97921f0e-832f-40c7-b56d-414faede5191
ms.collection:
- M365-security-compliance
description: EAC(Exchange 관리 센터)는 Microsoft EOP(Exchange Online Protection)의 웹 기반 관리 콘솔입니다.
ms.openlocfilehash: 0d1e56b85afe6655b5c6d08df51d4607df92d1d5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220468"
---
# <a name="exchange-admin-center-in-exchange-online-protection"></a><span data-ttu-id="1a18f-103">Exchange Online Protection의 Exchange 관리 센터</span><span class="sxs-lookup"><span data-stu-id="1a18f-103">Exchange admin center in Exchange Online Protection</span></span> 

<span data-ttu-id="1a18f-104">EAC(Exchange 관리 센터)는 Microsoft EOP(Exchange Online Protection)의 웹 기반 관리 콘솔입니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-104">The Exchange admin center (EAC) is the web-based management console for Microsoft Exchange Online Protection (EOP).</span></span> 
  
<span data-ttu-id="1a18f-p101">이 항목의 Exchange 2013 버전은 [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1a18f-p101">Looking for the Exchange 2013 version of this topic? See [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span></span>
  
<span data-ttu-id="1a18f-p102">이 항목의 Exchange Online 버전은 [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1a18f-p102">Looking for the Exchange Online version of this topic? See [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span></span>
  
## <a name="accessing-the-eac"></a><span data-ttu-id="1a18f-109">EAC 액세스</span><span class="sxs-lookup"><span data-stu-id="1a18f-109">Accessing the EAC</span></span>

<span data-ttu-id="1a18f-p103">대부분의 경우 EOP 고객은 Office 365 관리 센터를 통해 EAC에 액세스합니다. **내 소식** 타일 옆에 있는 **관리** 타일의 드롭다운 메뉴에 EOP에 대한 링크가 있습니다. **관리** 타일을 클릭하고 드롭다운 메뉴에서 **Exchange Online Protection**를 선택하여 EAC로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-p103">In most cases, EOP customers will access the EAC through the Office 365 admin center. You can find a link to EOP in the drop-down menu in the **Admin** tile, which is next to the **Me** tile. Click the **Admin** tile and select **Exchange Online Protection** from the drop down menu to be taken to the EAC.</span></span> 
  
<span data-ttu-id="1a18f-p104">다음 URL https://admin.protection.outlook.com/ecp/\<companydomain\>을 통해 EAC 로그인 페이지에 직접 액세스할 수도 있습니다. 예를 https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com들면입니다. 사용자 자격 증명을 지정 하 고 나면 EAC로 직접 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-p104">You can also access the EAC sign in page directly via the following URL: https://admin.protection.outlook.com/ecp/\<companydomain\>. For example, https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com. After specifying your user credentials you will be taken directly into the EAC.</span></span>
  
## <a name="common-user-interface-elements-in-the-eac"></a><span data-ttu-id="1a18f-116">EAC의 공통 사용자 인터페이스 요소</span><span class="sxs-lookup"><span data-stu-id="1a18f-116">Common user interface elements in the EAC</span></span>

<span data-ttu-id="1a18f-117">이 섹션에서는 EMC에 있는 사용자 인터페이스 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-117">This section describes the user interface elements that are found in the EAC.</span></span>
  
![EOP-admincenter](media/EOP-AdminCenter.png)
  
### <a name="feature-pane"></a><span data-ttu-id="1a18f-119">기능 창</span><span class="sxs-lookup"><span data-stu-id="1a18f-119">Feature Pane</span></span>

<span data-ttu-id="1a18f-p105">이 창은 EAC에서 수행할 대부분의 작업에 대한 첫 번째 탐색 수준으로, 기능 영역별로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-p105">This is the first level of navigation for most of the tasks you'll perform in the EAC. The feature pane is organized by feature areas.</span></span>
  
1. <span data-ttu-id="1a18f-122">**받는 사람** 내부 사용자와 외부 연락처를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-122">**Recipients** This is where you'll view internal users and external contacts.</span></span> 
    
2. <span data-ttu-id="1a18f-123">**사용 권한** 관리자 역할을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-123">**Permissions** This where you'll manage administrator roles.</span></span> 
    
3. <span data-ttu-id="1a18f-124">**준수 관리** 관리자 역할 그룹 보고서와 같은 보고서, 감사 로그 등을 찾아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-124">**Compliance Management** This is where you'll find audit logs and reports, such as the administrator role group report.</span></span> 
    
4. <span data-ttu-id="1a18f-125">**보호** 조직에 대해 맬웨어 방지 및 스팸 방지 보호 기능을 관리하고 격리된 메시지를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-125">**Protection** This is where you'll manage anti-malware and anti-spam protection for your organization, as well as manage messages in quarantine.</span></span> 
    
5. <span data-ttu-id="1a18f-126">**메일 흐름** 규칙, 허용 도메인 및 커넥터를 관리하고 메시지 추적을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-126">**Mail Flow** This is where you'll manage rules, accepted domains, and connectors, as well as where you'll go to perform message trace.</span></span> 
    
### <a name="tabs"></a><span data-ttu-id="1a18f-127">탭</span><span class="sxs-lookup"><span data-stu-id="1a18f-127">Tabs</span></span>

<span data-ttu-id="1a18f-p106">탭은 두 번째 탐색 수준입니다. 각 기능 영역에는 각각의 기능을 나타내는 다양한 탭이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-p106">The tabs are your second level of navigation. Each of the feature areas contains various tabs, each representing a feature.</span></span>
  
### <a name="toolbar"></a><span data-ttu-id="1a18f-130">도구 모음</span><span class="sxs-lookup"><span data-stu-id="1a18f-130">Toolbar</span></span>

<span data-ttu-id="1a18f-p107">대부분의 탭은 클릭하면 도구 모음이 표시됩니다. 도구 모음에는 특정 작업을 수행하는 아이콘이 있습니다. 다음 표에서는 아이콘과 그 작업에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-p107">When you click most tabs, you'll see a toolbar. The toolbar has icons that perform a specific action. The following table describes the icons and their actions.</span></span>
  
|<span data-ttu-id="1a18f-134">**아이콘**</span><span class="sxs-lookup"><span data-stu-id="1a18f-134">**Icon**</span></span>|<span data-ttu-id="1a18f-135">**이름**</span><span class="sxs-lookup"><span data-stu-id="1a18f-135">**Name**</span></span>|<span data-ttu-id="1a18f-136">**작업**</span><span class="sxs-lookup"><span data-stu-id="1a18f-136">**Action**</span></span>|
|:-----|:-----|:-----|
|![아이콘 추가](media/ITPro-EAC-AddIcon.gif)           <br/> |<span data-ttu-id="1a18f-138">추가, 새로 만들기</span><span class="sxs-lookup"><span data-stu-id="1a18f-138">Add, New</span></span>  <br/> |<span data-ttu-id="1a18f-p108">이 아이콘을 사용하면 새 개체를 만들 수 있습니다. 일부 아이콘에는 아래쪽 화살표가 있으며 이 화살표를 클릭하면 만들 수 있는 추가 개체가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-p108">Use this icon to create a new object. Some of these icons have an associated down arrow you can click to show additional objects you can create.</span></span>  <br/> |
|![편집 아이콘](media/ITPro-EAC-EditIcon.gif)           <br/> |<span data-ttu-id="1a18f-142">편집</span><span class="sxs-lookup"><span data-stu-id="1a18f-142">Edit</span></span>  <br/> |<span data-ttu-id="1a18f-143">이 아이콘을 사용하면 개체를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-143">Use this icon to edit an object.</span></span>  <br/> |
|![삭제 아이콘](media/ITPro-EAC-DeleteIcon.gif)           <br/> |<span data-ttu-id="1a18f-145">삭제</span><span class="sxs-lookup"><span data-stu-id="1a18f-145">Delete</span></span>  <br/> |<span data-ttu-id="1a18f-p109">이 아이콘을 사용하면 개체를 삭제할 수 있습니다. 일부 삭제 아이콘에는 아래쪽 화살표가 있으며 이 화살표를 클릭하면 추가 옵션이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-p109">Use this icon to delete an object. Some delete icons have a down arrow you can click to show additional options.</span></span>  <br/> |
|![검색 아이콘](media/ITPro-EAC-.gif)           <br/> |<span data-ttu-id="1a18f-149">검색</span><span class="sxs-lookup"><span data-stu-id="1a18f-149">Search</span></span>  <br/> |<span data-ttu-id="1a18f-150">이 아이콘을 사용하면 찾으려는 개체에 대한 검색어를 입력할 수 있는 검색 상자가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-150">Use this icon to open a search box in which you can type the search phrase for an object you want to find.</span></span>  <br/> |
|![새로 고침 아이콘](media/ITPro-EAC-RefreshIcon.gif)           <br/> |<span data-ttu-id="1a18f-152">새로 고침</span><span class="sxs-lookup"><span data-stu-id="1a18f-152">Refresh</span></span>  <br/> |<span data-ttu-id="1a18f-153">이 아이콘을 사용하면 목록 보기를 새로 고칠 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-153">Use this icon to refresh the list view.</span></span>  <br/> |
|![기타 옵션 아이콘](media/ITPro-EAC-MoreOptionsIcon.gif)           <br/> |<span data-ttu-id="1a18f-155">기타 옵션</span><span class="sxs-lookup"><span data-stu-id="1a18f-155">More options</span></span>  <br/> |<span data-ttu-id="1a18f-p110">이 아이콘을 사용하면 해당 탭의 개체에 대해 수행할 수 있는 기타 작업을 볼 수 있습니다. 예를 들어 **받는 사람 \> 사용자**에서 이 아이콘을 클릭하면 **고급 검색**을 수행할 수 있는 옵션이 표시됩니다.  </span><span class="sxs-lookup"><span data-stu-id="1a18f-p110">Use this icon to view more actions you can perform for that tab's objects. For example, in **Recipients \> Users** clicking this icon shows the option to perform an **Advanced Search**.  </span></span><br/> |
|![위쪽 화살표 아이콘](media/ITPro-EAC-UpArrowIcon.gif)![아래쪽 화살표 아이콘](media/ITPro-EAC-DownArrowIcon.gif)           <br/> |<span data-ttu-id="1a18f-160">위쪽 화살표와 아래쪽 화살표</span><span class="sxs-lookup"><span data-stu-id="1a18f-160">Up arrow and down arrow</span></span>  <br/> |<span data-ttu-id="1a18f-161">이 아이콘을 사용하면 개체 우선 순위를 위나 아래로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-161">Use these icons to move an object's priority up or down.</span></span>  <br/> |
|![아이콘 제거](media/ITPro-EAC-RemoveIcon.gif)           <br/> |<span data-ttu-id="1a18f-163">제거</span><span class="sxs-lookup"><span data-stu-id="1a18f-163">Remove</span></span>  <br/> |<span data-ttu-id="1a18f-164">이 아이콘을 사용하면 목록에서 개체를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-164">Use this icon to remove objects from a list.</span></span>  <br/> |
   
### <a name="list-view"></a><span data-ttu-id="1a18f-165">목록 보기</span><span class="sxs-lookup"><span data-stu-id="1a18f-165">List View</span></span>

<span data-ttu-id="1a18f-p111">탭을 선택하면 대부분의 경우 목록 보기가 표시됩니다. EAC 목록 보기 내에서 약 10,000개의 개체를 볼 수 있습니다. 또한 결과로 페이징할 수 있도록 페이징이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-p111">When you select a tab, in most cases you'll see a list view. The viewable limit with the EAC list view is approximately 10,000 objects. In addition, paging is included so that you can page to results.</span></span>
  
### <a name="details-pane"></a><span data-ttu-id="1a18f-169">세부 정보 창</span><span class="sxs-lookup"><span data-stu-id="1a18f-169">Details Pane</span></span>

<span data-ttu-id="1a18f-p112">목록 보기에서 개체를 선택하면 해당 개체에 대한 정보가 세부 정보 창에 표시됩니다. 세부 정보 창에 관리 작업이 포함된 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-p112">When you select an object from the list view, information about that object is displayed in the details pane. In some cases the details pane includes management tasks.</span></span>
  
### <a name="me-tile-and-help"></a><span data-ttu-id="1a18f-172">내 소식 타일 및 도움말</span><span class="sxs-lookup"><span data-stu-id="1a18f-172">Me tile and Help</span></span>

<span data-ttu-id="1a18f-p113">**내 소식** 타일을 통해 EAC에서 로그아웃하고 다른 사용자로 로그인할 수 있습니다. **도움말**![도움말 아이콘](media/ITPro-EAC-HelpIcon.gif) 드롭다운 메뉴에서 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-p113">The **Me** tile allows you to sign out the EAC and sign in as a different user. From the **Help**![Help Icon](media/ITPro-EAC-HelpIcon.gif) drop-down menu, you can perform the following actions:</span></span> 
  
1. <span data-ttu-id="1a18f-175">**도움말** 온라인 도움말 내용을 보려면 ![도움말 아이콘](media/ITPro-EAC-HelpIcon.gif)을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-175">**Help** Click ![Help Icon](media/ITPro-EAC-HelpIcon.gif) to view the online help content.</span></span> 
    
2. <span data-ttu-id="1a18f-p114">**풍선형 도움말 사용 안 함** 풍선형 도움말에는 개체를 만들거나 편집할 때 필드에 대한 상황에 맞는 도움말이 표시됩니다. 풍선형 도움말을 끌 수 있으며, 풍선형 도움말을 사용하지 않도록 설정한 경우에는 켤 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-p114">**Disable Help bubble** The Help bubble displays contextual help for fields when you create or edit an object. You can turn off the Help bubble or turn it on if it has been disabled.</span></span> 
    
3. <span data-ttu-id="1a18f-178">**저작권**Exchange Online Protection에 대한 저작권 표시를 보려면 이 링크를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-178">**Copyright** Click this link to read the copyright notice for Exchange Online Protection.</span></span> 
    
4. <span data-ttu-id="1a18f-179">**개인 정보 보호 정책**Exchange Online Protection의 개인 정보 보호 정책을 보려면 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-179">**Privacy** Click to read the privacy policy for Exchange Online Protection.</span></span> 
    
## <a name="supported-browsers"></a><span data-ttu-id="1a18f-180">지원되는 브라우저</span><span class="sxs-lookup"><span data-stu-id="1a18f-180">Supported Browsers</span></span>

<span data-ttu-id="1a18f-p115">최상의 EAC 사용 환경을 위해 항상 최신 브라우저, Office 클라이언트 및 앱을 사용하는 것이 좋습니다. 또한 소프트웨어 업데이트가 제공되면 이를 설치하는 것이 좋습니다. 서비스의 지원되는 브라우저 및 시스템 요구 사항에 대한 자세한 내용은 [Office 365 시스템 요구 사항](https://go.microsoft.com/fwlink/p/?LinkID=402699)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1a18f-p115">For the best experience using the EAC, we recommend that you always use the latest browsers, Office clients, and apps. We also recommend that you install software updates when they become available. For more information about the supported browsers and system requirements for the service, see [Office 365 System Requirements](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span></span> 
  
## <a name="supported-languages-in-eop"></a><span data-ttu-id="1a18f-184">EOP에서 지원되는 언어</span><span class="sxs-lookup"><span data-stu-id="1a18f-184">Supported languages in EOP</span></span>

<span data-ttu-id="1a18f-185">Exchange Online Protection에서 지원되고 사용할 수 있는 언어는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1a18f-185">The following languages are supported and available for Exchange Online Protection.</span></span>
  
- <span data-ttu-id="1a18f-186">암하라어</span><span class="sxs-lookup"><span data-stu-id="1a18f-186">Amharic</span></span>
    
- <span data-ttu-id="1a18f-187">아랍어</span><span class="sxs-lookup"><span data-stu-id="1a18f-187">Arabic</span></span>
    
- <span data-ttu-id="1a18f-188">바스크어(바스크)</span><span class="sxs-lookup"><span data-stu-id="1a18f-188">Basque (Basque)</span></span>
    
- <span data-ttu-id="1a18f-189">뱅골어(인도)</span><span class="sxs-lookup"><span data-stu-id="1a18f-189">Bengali (India)</span></span>
    
- <span data-ttu-id="1a18f-190">불가리아어</span><span class="sxs-lookup"><span data-stu-id="1a18f-190">Bulgarian</span></span>
    
- <span data-ttu-id="1a18f-191">카탈로니아어</span><span class="sxs-lookup"><span data-stu-id="1a18f-191">Catalan</span></span>
    
- <span data-ttu-id="1a18f-192">중국어(간체)</span><span class="sxs-lookup"><span data-stu-id="1a18f-192">Chinese (Simplified)</span></span>
    
- <span data-ttu-id="1a18f-193">중국어(번체)</span><span class="sxs-lookup"><span data-stu-id="1a18f-193">Chinese (Traditional)</span></span>
    
- <span data-ttu-id="1a18f-194">크로아티아어</span><span class="sxs-lookup"><span data-stu-id="1a18f-194">Croatian</span></span>
    
- <span data-ttu-id="1a18f-195">체코어</span><span class="sxs-lookup"><span data-stu-id="1a18f-195">Czech</span></span>
    
- <span data-ttu-id="1a18f-196">덴마크어</span><span class="sxs-lookup"><span data-stu-id="1a18f-196">Danish</span></span>
    
- <span data-ttu-id="1a18f-197">네덜란드어</span><span class="sxs-lookup"><span data-stu-id="1a18f-197">Dutch</span></span>
    
- <span data-ttu-id="1a18f-198">네덜란드어</span><span class="sxs-lookup"><span data-stu-id="1a18f-198">Dutch</span></span>
    
- <span data-ttu-id="1a18f-199">영어</span><span class="sxs-lookup"><span data-stu-id="1a18f-199">English</span></span>
    
- <span data-ttu-id="1a18f-200">에스토니아어</span><span class="sxs-lookup"><span data-stu-id="1a18f-200">Estonian</span></span>
    
- <span data-ttu-id="1a18f-201">필리핀어(필리핀)</span><span class="sxs-lookup"><span data-stu-id="1a18f-201">Filipino (Philippines)</span></span>
    
- <span data-ttu-id="1a18f-202">핀란드어</span><span class="sxs-lookup"><span data-stu-id="1a18f-202">Finnish</span></span>
    
- <span data-ttu-id="1a18f-203">프랑스어</span><span class="sxs-lookup"><span data-stu-id="1a18f-203">French</span></span>
    
- <span data-ttu-id="1a18f-204">갈리시아어</span><span class="sxs-lookup"><span data-stu-id="1a18f-204">Galician</span></span>
    
- <span data-ttu-id="1a18f-205">독일어</span><span class="sxs-lookup"><span data-stu-id="1a18f-205">German</span></span>
    
- <span data-ttu-id="1a18f-206">그리스어</span><span class="sxs-lookup"><span data-stu-id="1a18f-206">Greek</span></span>
    
- <span data-ttu-id="1a18f-207">구자라트어</span><span class="sxs-lookup"><span data-stu-id="1a18f-207">Gujarati</span></span>
    
- <span data-ttu-id="1a18f-208">히브리어</span><span class="sxs-lookup"><span data-stu-id="1a18f-208">Hebrew</span></span>
    
- <span data-ttu-id="1a18f-209">힌디어</span><span class="sxs-lookup"><span data-stu-id="1a18f-209">Hindi</span></span>
    
- <span data-ttu-id="1a18f-210">헝가리어</span><span class="sxs-lookup"><span data-stu-id="1a18f-210">Hungarian</span></span>
    
- <span data-ttu-id="1a18f-211">아이슬란드어</span><span class="sxs-lookup"><span data-stu-id="1a18f-211">Icelandic</span></span>
    
- <span data-ttu-id="1a18f-212">인도네시아어</span><span class="sxs-lookup"><span data-stu-id="1a18f-212">Indonesian</span></span>
    
- <span data-ttu-id="1a18f-213">이탈리아어</span><span class="sxs-lookup"><span data-stu-id="1a18f-213">Italian</span></span>
    
- <span data-ttu-id="1a18f-214">일본어</span><span class="sxs-lookup"><span data-stu-id="1a18f-214">Japanese</span></span>
    
- <span data-ttu-id="1a18f-215">카나다어</span><span class="sxs-lookup"><span data-stu-id="1a18f-215">Kannada</span></span>
    
- <span data-ttu-id="1a18f-216">카자흐어</span><span class="sxs-lookup"><span data-stu-id="1a18f-216">Kazakh</span></span>
    
- <span data-ttu-id="1a18f-217">스와힐리어</span><span class="sxs-lookup"><span data-stu-id="1a18f-217">Kiswahili</span></span>
    
- <span data-ttu-id="1a18f-218">한국어</span><span class="sxs-lookup"><span data-stu-id="1a18f-218">Korean</span></span>
    
- <span data-ttu-id="1a18f-219">라트비아어</span><span class="sxs-lookup"><span data-stu-id="1a18f-219">Latvian</span></span>
    
- <span data-ttu-id="1a18f-220">리투아니아어</span><span class="sxs-lookup"><span data-stu-id="1a18f-220">Lithuanian</span></span>
    
- <span data-ttu-id="1a18f-221">말레이어(브루나이)</span><span class="sxs-lookup"><span data-stu-id="1a18f-221">Malay (Brunei Darussalam)</span></span>
    
- <span data-ttu-id="1a18f-222">말레이어(말레이시아)</span><span class="sxs-lookup"><span data-stu-id="1a18f-222">Malay (Malaysia)</span></span>
    
- <span data-ttu-id="1a18f-223">말라얄람어</span><span class="sxs-lookup"><span data-stu-id="1a18f-223">Malayalam</span></span>
    
- <span data-ttu-id="1a18f-224">마라티어</span><span class="sxs-lookup"><span data-stu-id="1a18f-224">Marathi</span></span>
    
- <span data-ttu-id="1a18f-225">노르웨이어(복말)</span><span class="sxs-lookup"><span data-stu-id="1a18f-225">Norwegian (Bokmål)</span></span>
    
- <span data-ttu-id="1a18f-226">노르웨이어(니노르스크)</span><span class="sxs-lookup"><span data-stu-id="1a18f-226">Norwegian (Nynorsk)</span></span>
    
- <span data-ttu-id="1a18f-227">오리야어</span><span class="sxs-lookup"><span data-stu-id="1a18f-227">Oriya</span></span>
    
- <span data-ttu-id="1a18f-228">페르시아어</span><span class="sxs-lookup"><span data-stu-id="1a18f-228">Persian</span></span>
    
- <span data-ttu-id="1a18f-229">폴란드어</span><span class="sxs-lookup"><span data-stu-id="1a18f-229">Polish</span></span>
    
- <span data-ttu-id="1a18f-230">포르투갈어(브라질)</span><span class="sxs-lookup"><span data-stu-id="1a18f-230">Portuguese (Brazil)</span></span>
    
- <span data-ttu-id="1a18f-231">포르투갈어(포르투갈)</span><span class="sxs-lookup"><span data-stu-id="1a18f-231">Portuguese (Portugal)</span></span>
    
- <span data-ttu-id="1a18f-232">루마니아어</span><span class="sxs-lookup"><span data-stu-id="1a18f-232">Romanian</span></span>
    
- <span data-ttu-id="1a18f-233">러시아어</span><span class="sxs-lookup"><span data-stu-id="1a18f-233">Russian</span></span>
    
- <span data-ttu-id="1a18f-234">세르비아어(키릴 자모, 세르비아)</span><span class="sxs-lookup"><span data-stu-id="1a18f-234">Serbian (Cyrillic, Serbia)</span></span>
    
- <span data-ttu-id="1a18f-235">세르비아어(라틴 문자)</span><span class="sxs-lookup"><span data-stu-id="1a18f-235">Serbian (Latin)</span></span>
    
- <span data-ttu-id="1a18f-236">슬로바키아어</span><span class="sxs-lookup"><span data-stu-id="1a18f-236">Slovak</span></span>
    
- <span data-ttu-id="1a18f-237">슬로베니아어</span><span class="sxs-lookup"><span data-stu-id="1a18f-237">Slovenian</span></span>
    
- <span data-ttu-id="1a18f-238">스페인어</span><span class="sxs-lookup"><span data-stu-id="1a18f-238">Spanish</span></span>
    
- <span data-ttu-id="1a18f-239">스웨덴어</span><span class="sxs-lookup"><span data-stu-id="1a18f-239">Swedish</span></span>
    
- <span data-ttu-id="1a18f-240">타밀어</span><span class="sxs-lookup"><span data-stu-id="1a18f-240">Tamil</span></span>
    
- <span data-ttu-id="1a18f-241">텔루구어</span><span class="sxs-lookup"><span data-stu-id="1a18f-241">Telugu</span></span>
    
- <span data-ttu-id="1a18f-242">태국어</span><span class="sxs-lookup"><span data-stu-id="1a18f-242">Thai</span></span>
    
- <span data-ttu-id="1a18f-243">터키어</span><span class="sxs-lookup"><span data-stu-id="1a18f-243">Turkish</span></span>
    
- <span data-ttu-id="1a18f-244">우크라이나어</span><span class="sxs-lookup"><span data-stu-id="1a18f-244">Ukrainian</span></span>
    
- <span data-ttu-id="1a18f-245">우르두어</span><span class="sxs-lookup"><span data-stu-id="1a18f-245">Urdu</span></span>
    
- <span data-ttu-id="1a18f-246">베트남어</span><span class="sxs-lookup"><span data-stu-id="1a18f-246">Vietnamese</span></span>
    
- <span data-ttu-id="1a18f-247">웨일스어</span><span class="sxs-lookup"><span data-stu-id="1a18f-247">Welsh</span></span>
    

