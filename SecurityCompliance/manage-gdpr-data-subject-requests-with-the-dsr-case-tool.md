---
title: Office 365 보안 DSR 사례 도구로 GDPR 데이터 제목 요청 관리 &amp; 준수 센터
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/25/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.assetid: ce9eb942-3589-42cb-88fd-1576ecb09c5c
description: GDPR 제공 EU (데이터 주제 라고 함) 시민 특정 권한을 자신의 개인 데이터입니다. 이러한 권리의 복사본을 획득, 하 여 변경 요청, 처리에 대 한 제한, 삭제, 또는 전자 형식에서 수신를 포함 합니다. 라인 될 수 있는 데이터에 의해 공식 요청 자신의 개인 데이터에 대 한 작업 데이터 제목 요청 또는 DSR 라고 합니다. Office 365 보안에서 DSR 사례를 사용 하 여 &amp; 준수 센터 조직의 DSR 조사를 관리 합니다.
ms.openlocfilehash: c8edee8d377865d46662ebbd7f18a5a6f3015192
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533596"
---
# <a name="manage-gdpr-data-subject-requests-with-the-dsr-case-tool-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="354d4-105">Office 365 보안 DSR 사례 도구로 GDPR 데이터 제목 요청 관리 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="354d4-105">Manage GDPR data subject requests with the DSR case tool in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="354d4-p102">EU 일반적인 데이터 보호 규정 (GDPR)를 보호 하 고 개인의 정보 공개 권한 유럽 연합 (EU) 내부를 사용 하도록 설정 하는 방법에 대 한 됩니다. 유럽 연합의 GDPR 제공 개인 (라고도 함 제목에 데이터)에 액세스, 검색, 수정, 지우기 또는 자신의 개인 데이터의 처리를 제한할 수 있는 권한이 있습니다. 개인 데이터는 GDPR에서 식별 된 또는 식별할 수 있는 자연 스러운 사용자와 관련 된 모든 정보를 의미 합니다. 조직에 사용자가 자신의 개인 데이터에 대 한 작업을 수행할 수 공식 요청 데이터 제목 요청 또는 DSR 라고 합니다. Office 365의 데이터에 대 한 DSRs에 대 한 응답 하는 방법에 대 한 자세한 내용은 [Office 365 데이터 제목 요청 가이드](https://go.microsoft.com/fwlink/?linkid=871169 )를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p102">The EU General Data Protection Regulation (GDPR) is about protecting and enabling individuals' privacy rights inside the European Union (EU). The GDPR gives individuals in the European Union (known as data subjects) the right to access, retrieve, correct, erase, and restrict processing of their personal data. Under the GDPR, personal data means any information relating to an identified or identifiable natural person. A formal request by a person to their organization to take an action on their personal data is called a Data Subject Request or DSR. For detailed information about responding to DSRs for data in Office 365, see [Office 365 Data Subject Request Guide](https://go.microsoft.com/fwlink/?linkid=871169 ).</span></span>
  
<span data-ttu-id="354d4-111">조사 하면 조직에서 사용자가 제출한 DSR에 대 한 응답에서을 관리 하려면 Office 365 보안에서 DSR 사례 도구를 사용할 수 &amp; 준수 센터에 저장 된 콘텐츠를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-111">To manage investigations in response to a DSR submitted by a person in your organization, you can use the DSR case tool in the Office 365 Security &amp; Compliance Center to find content stored in:</span></span>
  
- <span data-ttu-id="354d4-p103">조직에서 모든 사용자 사서함입니다. 비즈니스 대화 및 팀이 Microsoft에서 일대일 채팅에 대 한 Skype 포함</span><span class="sxs-lookup"><span data-stu-id="354d4-p103">Any user mailbox in your organization. This includes Skype for Business conversations and one-to-one chats in Microsoft Teams</span></span>
    
- <span data-ttu-id="354d4-114">Office 365 그룹과 Microsoft 팀의 모든 팀 사서함와 관련 된 모든 사서함</span><span class="sxs-lookup"><span data-stu-id="354d4-114">All mailboxes associated with an Office 365 Group and all team mailboxes in Microsoft Teams</span></span>
    
- <span data-ttu-id="354d4-115">조직의 모든 SharePoint Online 사이트 및 비즈니스용 OneDrive 계정</span><span class="sxs-lookup"><span data-stu-id="354d4-115">All SharePoint Online sites and OneDrive for Business accounts in your organization</span></span>
    
- <span data-ttu-id="354d4-116">모든 팀 사이트 및 조직에서 Office 365 그룹 사이트</span><span class="sxs-lookup"><span data-stu-id="354d4-116">All Teams sites and Office 365 Group sites in your organization</span></span>
    
- <span data-ttu-id="354d4-117">Exchange Online의 모든 공용 폴더</span><span class="sxs-lookup"><span data-stu-id="354d4-117">All public folders in Exchange Online</span></span>
    
<span data-ttu-id="354d4-118">DSR 사례 도구를 사용 하 여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-118">Using the DSR case tool you can:</span></span>
  
- <span data-ttu-id="354d4-119">각 DSR 조사에 대한 별도의 사례를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-119">Create a separate case for each DSR investigation.</span></span>
    
- <span data-ttu-id="354d4-p104">대/소문자;의 구성원으로 사용자를 추가 하 여 DSR 대/소문자에 액세스할 수 있는 사용자 제어 구성원만 대/소문자에 액세스할 수 있으며을 보려면 사례 목록에서 자신의 경우 **DSR의 경우** 페이지의 보안에서 &amp; 준수 센터입니다. 또한 동일한 대/소문자의 다른 구성원에 게 다른 사용 권한을 할당할 수 있습니다. 예, 일부 구성원만 대/소문자와 검색 결과 확인 하 고 다른 구성원이 검색을 만들고 검색 결과 내보낼 수 있도록 허용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p104">Control who has access to the DSR case by adding people as members of the case; only members can access the case and can only see their cases in the list of cases on the **DSR cases** page in the Security &amp; Compliance Center. Additionally, you can assign different permissions to different members of the same case. For example, you can allow some members to only view the case and search results and allow other members to create searches and export search results.</span></span> 
    
- <span data-ttu-id="354d4-123">모든 콘텐츠에 대 한 기본 제공 검색에 사용 하 여 만든 또는 특정 데이터 제목별으로 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-123">Use the built-in search to search for all content created or uploaded by a specific data subject.</span></span>
    
- <span data-ttu-id="354d4-124">필요에 따라 기본 제공 검색 쿼리를 수정 하 고 검색 결과 범위를 좁힐 수 검색을 다시 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-124">Optionally revise the built-in search query and re-run the search to narrow the search results.</span></span>
    
- <span data-ttu-id="354d4-p105">DSR 사례와 관련 된 추가 콘텐츠 검색을 추가 합니다. 이 부분적으로 인덱싱된 항목 및 시스템에서 생성 된 로그 내 분석 및 Office 로밍 서비스에서 반환 하는 검색 만들기 (영문)을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p105">Add additional content searches associated with the DSR case. This includes creating searches that return partially indexed items and system-generated logs from My Analytics and the Office Roaming Service.</span></span>
    
- <span data-ttu-id="354d4-127">DSR 액세스에 대 한 응답에 데이터를 수출 또는 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-127">Export data in response to a DSR access or export request.</span></span>
    
- <span data-ttu-id="354d4-128">DSR 조사 프로세스가 끝나면; 경우 삭제 모든 검색을 제거 그러면 되 고 대/소문자와 관련 된 작업을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-128">Delete cases when the DSR investigation process is complete; this will remove all searches and export jobs associated with the case.</span></span>
    
<span data-ttu-id="354d4-129">DSR 사례 도구를 사용 하 여 DSR 조사를 관리 하는 것에 대 한 높은 수준의 프로세스는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-129">Here's the high-level process for using the DSR case tool to manage DSR investigations:</span></span>
  
[<span data-ttu-id="354d4-130">1단계: 잠재적인 사례 구성원에게 eDiscovery 권한 할당</span><span class="sxs-lookup"><span data-stu-id="354d4-130">Step 1: Assign eDiscovery permissions to potential case members</span></span>](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[<span data-ttu-id="354d4-131">2 단계: DSR 사례를 만들고 구성원 추가</span><span class="sxs-lookup"><span data-stu-id="354d4-131">Step 2: Create a DSR case and add members</span></span>](#step-2-create-a-dsr-case-and-add-members)

[<span data-ttu-id="354d4-132">3 단계: 검색 쿼리를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-132">Step 3: Run the search query</span></span>](#step-3-run-the-search-query)

[<span data-ttu-id="354d4-133">4 단계: 데이터를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-133">Step 4: Export the data</span></span>](#step-4-export-the-data)

[<span data-ttu-id="354d4-134">(선택 사항) 5 단계: 기본 제공 검색 쿼리를 수정.</span><span class="sxs-lookup"><span data-stu-id="354d4-134">(Optional) Step 5: Revise the built-in search query</span></span>](#optional-step-5-revise-the-built-in-search-query)

[<span data-ttu-id="354d4-135">DSR 사례 도구를 사용 하는 방법에 대 한 자세한 내용</span><span class="sxs-lookup"><span data-stu-id="354d4-135">More information about using the DSR case tool</span></span>](#more-information-about-using-the-dsr-case-tool)
  
> [!IMPORTANT]
> <span data-ttu-id="354d4-p106">이 도구는 관리자 또는 DSR 액세스를 수행 하는 기본 제공 검색을 활용 하 고 내보내기 DSR 사례 도구에 있는 기능을 사용 하 여 내보내기 요청 수 있습니다. 이 도구를 데이터 제목별으로 전송 하는 DSR 요청에 관련 된 데이터를 내보내려면 최상의 메서드를 용이 하 게 하는데 도움이 됩니다. 그러나 것이 중요 데이터 제목에 따라 검색 결과가 달라질 수 또는 내보내기 목적을 위해 "개인 데이터"로 간주는 항목이 있는지 여부는 발생 하는 관리 작업 성능이 떨어질 수 있습니다. 예, 데이터 제목 파일을 수정 하도록 마지막 사용자가 자신이 만들지 않은, 파일 검색 결과에 반환 될 수 있습니다. 마찬가지로, 관리자는 부분적으로 인덱싱된 항목 또는 모든 SharePoint 문서 버전을 포함 하지 않고 데이터를 내보낼 수 있습니다. 따라서 제공 하는 도구에 액세스 하 고 데이터 요청; 내보내기 (영문)를 용이 하 게 도움이 수 있습니다. 그러나 결과 특정 관리 및 데이터 제목 사용 시나리오에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p106">Our tools can help admins perform DSR access or export requests by enabling them to utilize the built-in search and export functionality found in the DSR case tool. The tool helps to facilitate a best-effort method to export data that's relevant to a DSR request submitted by a data subject. However, it's important to note that search results can vary based on the data subject or the admin actions taken that may impact whether or not an item would be deemed as "personal data" for export purposes. For example, if the data subject was the last person to modify a file they didn't create, the file might not be returned in the search results. Similarly, an admin could export data without including partially indexed items or all versions of SharePoint documents. Therefore, the tools provided can help facilitate accessing and exporting data requests; however, the results are subject to specific admin and data subject usage scenarios.</span></span> 
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a><span data-ttu-id="354d4-142">1단계: 잠재적인 사례 구성원에게 eDiscovery 권한 할당</span><span class="sxs-lookup"><span data-stu-id="354d4-142">Step 1: Assign eDiscovery permissions to potential case members</span></span>

<span data-ttu-id="354d4-p107">기본적으로 Office 365 전역 관리자 보안에서 DSR 사례 도구에 액세스할 수 &amp; 준수 센터입니다. 하 여 디자인, 데이터 개인 정보 관리자, 인적 자원 관리자, 예: 다른 사용자 또는 DSR 조사에 참여 하는 다른 사람들 DSR 사례 도구에 액세스할 수 없는 및 도구에 액세스 하려면 적절 한 사용 권한을 할당 해야 합니다. 이 작업을 수행 하는 것이 가장 편리 방법은 보안에서 **사용 권한** 페이지로 이동 하는 &amp; 준수 센터 eDiscovery 관리자 역할 그룹에 사용자를 추가 합니다. 또한 한다고 2 단계에서에서 만든 DSR 대/소문자의 구성원으로 추가할 수 있도록 이러한 사용 권한을 할당 하려면 note 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p107">By default, an Office 365 global administrator can access the DSR case tool in the Security &amp; Compliance Center. By design, other users such as a data privacy officer, a human resources manager, or other people involved in DSR investigations don't have access to the DSR case tool and will have to be assigned the appropriate permissions to access the tool. The easiest way to do this is to go to the **Permissions** page in the Security &amp; Compliance Center and add users to the eDiscovery Manager role group. Note that you also have to assign these permissions so you can add them as members of the DSR case that you create in Step 2.</span></span> 
  
<span data-ttu-id="354d4-147">단계별 지침은 참조 [Office 365 보안에서 eDiscovery 사용 권한을 할당 &amp; 준수 센터](assign-ediscovery-permissions.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-147">For step-by-step instructions, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="354d4-p108">기본적으로 Office 365 전역 관리자 (또는 보안에서 조직 관리 역할 그룹의 다른 구성원 &amp; 준수 센터 (이 문서에서 4 단계 참조) 콘텐츠 검색 결과를 내보내려면 필요한 권한이 없습니다. 이 문제를 해결 하려면 관리자 수 있는 추가 자신 eDiscovery 관리자 역할 그룹의 구성원으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p108">By default, an Office 365 global administrator (or other members of the Organization Management role group in the Security &amp; Compliance Center don't have the necessary permissions to export Content Search results (see Step 4 in this article). To address this, an admin can add themselves as a member of the eDiscovery Manager role group.</span></span> 
  
## <a name="step-2-create-a-dsr-case-and-add-members"></a><span data-ttu-id="354d4-150">2 단계: DSR 사례를 만들고 구성원 추가</span><span class="sxs-lookup"><span data-stu-id="354d4-150">Step 2: Create a DSR case and add members</span></span>

<span data-ttu-id="354d4-p109">다음 단계에서는 DSR 사례를 만드는 것입니다. 사례를 만들 때 기본 제공 검색을 시작 하도록 선택할 수 있습니다 또는 검색을 시작 하지 않고 대/소문자를 만들 수 있습니다. 다음 절차는 검색을 시작 하지 않고 대/소문자를 만들고 다음 대/소문자에 구성원을 추가 하는 방법을 보여주는 하도록 안내 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p109">The next step is to create a DSR case. When you create a case, you can choose to start the built-in search or you can create the case without starting the search. The following procedure will instruct you to create the case without starting the search and then show you how to add members to the case.</span></span>
  
1. <span data-ttu-id="354d4-154">이동 [https://protection.office.com](https://protection.office.com) 작업이 나 교육용 계정을 사용 하 여 Office 365에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-154">Go to [https://protection.office.com](https://protection.office.com) and sign in to Office 365 using your work or school account.</span></span> 
    
2. <span data-ttu-id="354d4-155">보안에서 &amp; 준수 센터 **데이터 프라이버시** 를 클릭 \> **데이터 주체 요청**을 하 고 다음을 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **새 DSR 사례**입니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-155">In the Security &amp; Compliance Center, click **Data privacy** \> **Data subject requests**, and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif) **New DSR case**.</span></span>
    
3. <span data-ttu-id="354d4-p110">**새 DSR 사례** 플라이 아웃 페이지에서 프로그램 이름을 지정 하는 경우, 대 한 선택적 설명을 입력 하 고 **** 을 클릭 합니다. 참고 이름의 대/소문자를 조직 내에서 고유 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p110">On the **New DSR case** flyout page, give the case a name, type an optional description, and then click **Next**. Note that the name of the case must be unique in your organization.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="354d4-p111">이름에 조사 중인 DSR 요청을 제출한 사용자의 이름 및/또는 새 대/소문자에 이르는 추가 하는 것이 좋습니다. Note이 대/소문자 (및 eDiscovery 관리자)의 구성원만 **데이터 제목 요청** 페이지에서의 경우의 목록에서 대/소문자를 볼 수 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p111">Consider adding the name of the person who submitted the DSR request that you're investigating in the name and/or description of the new case. Note that only members of this case (and eDiscovery Administrators) will be able to see the case in the list of cases on the **Data subject requests** page.</span></span> 
  
4. <span data-ttu-id="354d4-160">**데이터 주체 (사용자가이 요청 보관 된)** **요청 세부 정보** 페이지에서 찾기 및에 대 한 데이터를 내보내려면 **다음**을 클릭 하 고 원하는 사람을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-160">On the **Request details** page, under **Data subject (the person who filed this request)**, select the person that you want to find and export data for and then click **Next**.</span></span>
    
5. <span data-ttu-id="354d4-p112">**사례 설정을 확인** 페이지에서 사례 이름 및 설명을 변경할 수 있으며 서로 다른 데이터 주제를 선택 키를 누릅니다. 그렇지 않은 경우 방금 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p112">On the **Confirm your case settings** page, you can change the case name and description, and select a different data subject. Otherwise, just click **Save**.</span></span>
    
    <span data-ttu-id="354d4-163">페이지에는 새 DSR 사례 생성 된 것인지 확인 하는 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-163">A page is displayed that confirms the new DSR case has been created.</span></span>
    
    ![검색을 시작 하거나 새 DSR 사례 페이지 닫습니다](media/b5e62c2c-cafe-4a8d-a38c-789ed9f9ccbd.png)
  
    <span data-ttu-id="354d4-165">이제 두 작업 중 하나를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-165">At this point, you can do one of two things:</span></span>
    
    <span data-ttu-id="354d4-p113">a. **나에 게 검색 결과 표시** 를 클릭 하는 검색을 시작 합니다. 이 옵션은 기본 선택 합니다. 이 옵션을 선택 하면 실행 되는 기본 제공 검색 및 반환 되는 결과 3 단계에에서 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p113">a. Clicking **Show me search results** starts the search. This is the default selection. The built-in search that is run when you select this option and the results that are returned are discussed in Step 3.</span></span>
    
    <span data-ttu-id="354d4-p114">b. **완료** 를 클릭 하는 기본 제공 검색을 시작 하지 않고 새 DSR 대/소문자를 닫습니다. 이 옵션을 선택 하는 경우 **데이터 주체 요청** 페이지에서 새 DSR 대/소문자 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p114">b. Clicking **Finish** closes the new DSR case without starting the built-in search. When you select this option, the new DSR case is displayed on the **Data subject requests** page.</span></span>
    
6. <span data-ttu-id="354d4-173">새 DSR 대/소문자 이동 하 고에 구성원을 추가할 수 있도록 **완료** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-173">Click **Finish** so that you can go in to the new DSR case and add members to it.</span></span> 
    
7. <span data-ttu-id="354d4-174">**데이터 주체 요청** 페이지에서 방금 만든 DSR 대/소문자의 이름을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-174">On the **Data subject requests** page, click the name of the DSR case that you just created.</span></span> 
    
8. <span data-ttu-id="354d4-175">**이 경우 관리** 플라이 아웃 페이지에서 **관리 구성원**아래에서 **추가**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-175">On the **Manage this case** flyout page, under **Manage members**, click **Add**.</span></span> 
    
    <span data-ttu-id="354d4-p115">**사용자가**아래에서 적절 한 eDiscovery 사용 권한을 할당 된 사용자 목록이 표시 됩니다. 메모는 사람 있습니다 eDiscovery 사용 권한을 할당 하려면 1 단계에서에서이 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p115">Under **Users**, a list of people that have been assigned the appropriate eDiscovery permissions is displayed. Note that the people you assigned eDiscovery permissions to in Step 1 will be displayed in this list.</span></span> 
    
9. <span data-ttu-id="354d4-178">DSR 대/소문자의 구성원으로 추가, **추가**클릭 한 다음 변경 내용을 저장 하려면 사용자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-178">Select the people to add as members of the DSR case, click **Add**, and then save your changes.</span></span>
    
    <span data-ttu-id="354d4-179">추가할 수 있습니다 또한 역할 그룹 DSR 사례의 구성원으로 **관리 역할 그룹에서** **추가** 클릭 하 여 note 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-179">Note that you can also add role groups as members of DSR case by clicking **Add** under **Manage role groups**.</span></span> 
    
## <a name="step-3-run-the-search-query"></a><span data-ttu-id="354d4-180">3 단계: 검색 쿼리를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-180">Step 3: Run the search query</span></span>

<span data-ttu-id="354d4-p116">DSR 사례를 만들고 구성원을 추가 하는 후 다음 단계에서는 대/소문자와 관련 된 기본 제공 검색을 실행 하는 것입니다. 이 기본 검색 쿼리는 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p116">After you create a DSR case and add members, the next step is to run the built-in search that's associated with the case. This default search query does the following:</span></span>
  
- <span data-ttu-id="354d4-p117">보내거나 데이터 제목별으로 수신 하는 모든 전자 메일 항목에 대 한 조직에서 모든 사서함을 검색 합니다. 이 작업은 전자 메일 메시지의 모든 사용자 필드에서 데이터 주제를 검색 하는 *참가자가* 전자 메일 속성을 사용 하 여 수행 됩니다. 이 속성에서 **** **받는**사람, **참조**및 **숨은 참조** 필드에 데이터 주제는 항목을 반환 합니다. Exchange Online의 공용 폴더 데이터 제목별으로 보내거나 받는 메시지에 대 한 검색도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p117">Searches all mailboxes in your organization for all email items that were sent or received by the data subject. This is accomplished by using the  *Participants*  email property, which searches for the data subject in all the people fields in an email message. This property returns items in which the data subject is in the **From**, **To**, **CC**, and **BCC** fields. Public folders in Exchange Online are also searched for messages sent or received by the data subject.</span></span> 
    
- <span data-ttu-id="354d4-p118">문서 및 만들거나 데이터 제목별으로 업로드 하는 항목에 대 한 조직에서 모든 사이트를 검색 합니다. 이 작업은 다음과 같은 사이트 속성을 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p118">Searches all sites in your organization for documents and items that were created or uploaded by the data subject. This is accomplished by using the following site properties:</span></span>
    
  - <span data-ttu-id="354d4-p119">*만든이* 속성은 데이터 제목 Office 문서에서 만든이 필드는 목록의 항목을 반환 합니다. 이 값은 문서를 복사 하 여 다른 사용자가 업로드 하는 경우에 계속 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p119">The  *Author*  property returns items where the data subject is listed in the author field in Office documents. This value persists, even if the document is copied and uploaded by someone else.</span></span> 
    
  - <span data-ttu-id="354d4-191">*CreatedBy* 속성 항목을 만들거나 데이터 제목별으로 업로드를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-191">The  *CreatedBy*  property returns items that were created or uploaded by the data subject.</span></span> 
    
<span data-ttu-id="354d4-192">DSR 사례를 만들 때 자동으로 만들어지는 기본 제공 검색에 대 한 키워드 쿼리 모습 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-192">Here's what the keyword query looks like for the built-in search that gets automatically created when you create a DSR case.</span></span>
  
```
participants:"<email address>" OR author:"<display name>" OR createdby:"<display name>"
```

<span data-ttu-id="354d4-193">예, 데이터 주체 이름에서 Leonte 있으면 키워드 쿼리는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-193">For example, if the name of the data subject is Ina Leonte, the keyword query would look like this:</span></span>
  
```
participants:"ina@contoso.com" OR author:"Ina Leonte" OR createdby:"Ina Leonte"
```

 <span data-ttu-id="354d4-194">**DSR 사례에 대 한 기본 제공 검색을 실행 합니다.**</span><span class="sxs-lookup"><span data-stu-id="354d4-194">**To run the built-in search for a DSR case:**</span></span>
  
1. <span data-ttu-id="354d4-195">보안에서 &amp; 준수 센터 **데이터 프라이버시** 를 클릭 \> **데이터 주체 요청**을 한 후 2 단계에서에서 만든 DSR 사례 옆에 있는 **열기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-195">In the Security &amp; Compliance Center, click **Data privacy** \> **Data subject requests**, and then click **Open** next to the DSR case that you created in Step 2.</span></span> 
    
    <span data-ttu-id="354d4-p120">페이지의 맨 아래에 있는 **검색** 탭을 클릭 한 다음 새 DSR 대/소문자를 만들 때 만들어진 기본 제공 검색 옆에 있는 확인란을 클릭 합니다. 참고 검색 DSR 대/소문자 이름이 같은 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p120">Click the **Search** tab at the top of the page, and then click the checkbox next to the built-in search that was created when you created the new DSR case. Note the search has the same name as the DSR case.</span></span> 
    
2. <span data-ttu-id="354d4-198">검색 플라이 아웃 페이지에서 **쿼리 열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-198">In the search flyout page, click **Open query**.</span></span>
    
    <span data-ttu-id="354d4-199">쿼리를 열 때 검색 시작 되 고 잠시에 완료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-199">When you open the query, the search is started and will complete in a few moments.</span></span> 
    
3. <span data-ttu-id="354d4-p121">검색 완료 되 면 검색 결과를 미리보려면 **결과 미리 보기** 클릭 합니다. 자세한 내용은 [검색 결과 미리 보기를](content-search.md#preview-search-results)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="354d4-p121">When the search is complete, click **Preview results** to preview the search results. For more information, see [Preview search results](content-search.md#preview-search-results).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="354d4-p122">사서함 및 사이트의 검색을 통해 반환 되는 항목과의 검색 쿼리와 일치 하는 항목이 포함 된 상위 콘텐츠 위치 번호를 보려면 검색 쿼리 통계를 볼 수 있습니다. 자세한 내용은 참조, [정보 및 검색에 대 한 통계를 확인](content-search.md#view-information-and-statistics-about-a-search)합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p122">You can also view the search query statistics to see the number of mailbox and site items that are returned by the search, and the top content locations that contain items that match the search query. For more information see, [View information and statistics about a search](content-search.md#view-information-and-statistics-about-a-search).</span></span> 
  
<span data-ttu-id="354d4-p123">기본 제공 검색 쿼리를 편집 하 고, 검색 되는 콘텐츠 위치를 변경 하 고, 검색을 다시 실행 수 있습니다. 자세한 내용은 [5 단계를](#optional-step-5-revise-the-built-in-search-query) 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="354d4-p123">You can edit the built-in search query, change the content locations that are searched, and then re-run the search. See [Step 5](#optional-step-5-revise-the-built-in-search-query) for more information.</span></span> 
  
## <a name="step-4-export-the-data"></a><span data-ttu-id="354d4-206">4 단계: 데이터를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-206">Step 4: Export the data</span></span>

<span data-ttu-id="354d4-p124">기본 제공 검색을 실행 하면 검색 결과 내보낼 수 있습니다. 또는 데이터를 내보내기 전에 검색 결과의 수를 줄이는 쿼리를 수정 하는 것이 좋습니다. 검색 결과 축소 하는 방법에 대 한 자세한 내용은 5 단계를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="354d4-p124">After you run the built-in search, you can export the search results. Alternatively, before you export the data, you may want to revise the query to reduce the number of search results. See Step 5 for more information about narrowing the search results.</span></span>
  
<span data-ttu-id="354d4-p125">검색 결과 내보낼 때에 PST 파일 또는 개별 메시지도 사서함 항목을 다운로드할 수 있습니다. SharePoint 및 OneDrive 계정에서 콘텐츠를 내보낼 때의 기본 Office 문서 및 기타 문서 복사본 내보냅니다. 내보낸 되는 모든 항목에 대 한 정보를 포함 하는 결과 파일 검색 결과 함께 포함 됩니다. 내보내기 (영문)에 대 한 정보를 자세한 참조 [Office 365 보안에서 내보내기의 콘텐츠 검색 결과 &amp; 준수 센터](export-search-results.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p125">When you export search results, mailbox items can be downloaded in PST files or as individual messages. When you export content from SharePoint and OneDrive accounts, copies of native Office documents and other documents are exported. A results file that contains information about every item that is exported is also included with the search results. For more detailed information about exporting, see [Export Content Search results from the Office 365 Security &amp; Compliance Center](export-search-results.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="354d4-p126">기본적으로 Office 365 전역 관리자 (또는 보안에서 조직 관리 역할 그룹의 다른 구성원 &amp; 준수 센터) 콘텐츠 검색 결과를 내보내려면 필요한 권한이 없습니다. 이 문제를 해결 하려면 관리자 수 있는 추가 자신 eDiscovery 관리자 역할 그룹의 구성원으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p126">By default, an Office 365 global administrator (or other members of the Organization Management role group in the Security &amp; Compliance Center) don't have the necessary permissions to export Content Search results. To address this, an admin can add themselves as a member of the eDiscovery Manager role group.</span></span> 
  
<span data-ttu-id="354d4-216">다음과 같은 시스템 요구 사항에 맞게 데이터를 사용 하는 컴퓨터에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-216">The computer you use to export data has to meet the following system requirements:</span></span>
  
- <span data-ttu-id="354d4-217">32비트 및 64비트 버전의 Windows 7 이상 버전


</span><span class="sxs-lookup"><span data-stu-id="354d4-217">32- or 64-bit versions of Windows 7 and later versions</span></span>
    
- <span data-ttu-id="354d4-218">Microsoft.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="354d4-218">Microsoft .NET Framework 4.7</span></span>
    
- <span data-ttu-id="354d4-219">지원되는 브라우저:</span><span class="sxs-lookup"><span data-stu-id="354d4-219">A supported browser:</span></span>
    
  - <span data-ttu-id="354d4-220">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="354d4-220">Microsoft Edge</span></span>
    
    <span data-ttu-id="354d4-221">또는</span><span class="sxs-lookup"><span data-stu-id="354d4-221">Or</span></span>
    
  - <span data-ttu-id="354d4-222">Microsoft Internet Explorer 10 및 그 이후 버전</span><span class="sxs-lookup"><span data-stu-id="354d4-222">Microsoft Internet Explorer 10 and later versions</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="354d4-p127">ClickOnce 응용 프로그램에 대 한 추가 기능 사용 또는 제 3 자 확장 Microsoft 제조 하지 않습니다. 제 3 자 확장 또는 추가 기능 지원 되지않는 브라우저를 사용 하 여 데이터를 내보낼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p127">Microsoft doesn't manufacture third-party extensions or add-ons for ClickOnce applications. Exporting data using an unsupported browser with third-party extensions or add-ons isn't supported.</span></span> 
  
 <span data-ttu-id="354d4-225">**DSR 경우에는 기본 제공 검색을 통해 데이터를 내보내려면:**</span><span class="sxs-lookup"><span data-stu-id="354d4-225">**To export data from the built-in search in a DSR case:**</span></span>
  
1. <span data-ttu-id="354d4-226">보안에서 &amp; 준수 센터 **데이터 프라이버시** 를 클릭 \> **데이터 주체 요청**을 다음 데이터를 내보낼 DSR 사례 옆에 있는 **열기** 를 클릭 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-226">In the Security &amp; Compliance Center, click **Data privacy** \> **Data subject requests**, and then click **Open** next to the DSR case that you want to export data from.</span></span> 
    
2. <span data-ttu-id="354d4-p128">페이지의 맨 아래에 있는 **검색** 탭을 클릭 하 고 DSR 대/소문자를 만들 때 만들어진 기본 제공 검색 옆에 있는 확인란을 클릭 합니다. 또는 해당 검색에서 데이터를 내보내려면 다른 검색을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p128">Click the **Search** tab at the top of the page, and then click the checkbox next to the built-in search that was created when you created the DSR case. Or click another search to export data from that search.</span></span> 
    
3. <span data-ttu-id="354d4-229">검색 플라이 아웃 페이지에서 다음을 클릭 ![내보내기 검색 결과 아이콘](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **더 많은**, 하 고 드롭다운 목록에서 **검색 결과 내보내기 결과** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-229">On the search flyout page, click ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **More**, and then select **Export results** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="354d4-230">**결과 내보내기** 페이지에서 다음과 같은 권장 DSR 내보내기 요청에 대 한 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-230">On the **Export results** page, select the following recommended options for DSR export requests.</span></span> 
    
    ![내보내기 설정 구성](media/25416b79-57da-46a1-ae07-e640602a8fa4.png)
  
    <span data-ttu-id="354d4-p129">a. **출력 옵션**인덱싱된 항목에만 내보낼 첫번째 옵션 ( **모든 항목을 보유 하는 인식할 수 없는 형식, 암호화 된 되었거나 다른 이유로 인덱싱된 받지를 포함 하는 것을 제외**)을 선택 합니다. 기본 제공 검색에서 부분적으로 인덱싱된 항목 내보내기 하지 않을 이유는 다른 사용자가 부분적으로 인덱싱된 항목 내보낼 때문입니다. 부분적으로 인덱싱된 항목에만 데이터 주제에 대 한 내보내려는 별도 검색을 만들어야 하는 것이 좋습니다. 자세한 내용은 "DSR 사례 도구를 사용 하는 방법에 대 한 자세한 내용은" 섹션에서 [내보내기 부분적으로 인덱싱된 항목](manage-gdpr-data-subject-requests-with-the-dsr-case-tool.md#exportunindexeditems) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="354d4-p129">a. Under **Output options**, select the first option ( **All items, excluding ones that have ones that have an unrecognized format, are encrypted, or weren't indexed for other reasons**) to export indexed items only. The reason you don't want to export partially indexed items from the built-in search is because partially indexed items from other users will be exported. To export only the partially indexed items for the data subject, we recommend that you create a separate search. For more information, see [Exporting partially indexed items](manage-gdpr-data-subject-requests-with-the-dsr-case-tool.md#exportunindexeditems) in the "More information about using the DSR case tool" section.</span></span>
    
    <span data-ttu-id="354d4-p130">b. **내보내기 Exchange 콘텐츠**를에서 세번째 옵션을 **단일 폴더에 있는 모든 메시지를 포함 하는 하나의 PST 파일**을 선택 합니다. 결과 중 일부는 다른 사용자의 사서함에서 발생 하는 항목에 대 한 될 수 있습니다, 때문에이 옵션 방금 실제 사서함을 나타내지 않고 단일 폴더에 있는 항목을 나열 하 고 항목에서 권장 하는 대로 결과 해제 복제할 때 사용 하 여 가장 적합 한 옵션은 . 이 옵션에는 각 항목에 대 한 원래 사서함 폴더 구조를 탐색 하지 않고도 시간순 (항목이 보낸된 날짜순으로 정렬 됩니다.) 항목을 검토 하는 데이터 제목 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p130">b. Under **Export Exchange content as**, select the third option, **One PST file containing all messages in a single folder**. Because some of the results may be for items that originated in another user's mailbox, this option just lists the item in a single folder without indicating the actual mailbox and is the best option to use when you de-duplicate the results as recommended in the next item. This option also lets the data subject review items in chronological order (items are sorted by sent date) without having to navigate the original mailbox folder structure for each item.</span></span>
    
    <span data-ttu-id="354d4-p131">c.는 중복 된 전자 메일 메시지를 제외 하려면 **중복을 사용 하도록 설정** 옵션을 선택 합니다. 조직에서 모든 사서함을 검색 하는 기본 제공 검색 하기 때문에이 옵션을 좋습니다. 하므로 동일한 메시지의 복사본을 여러개 검색 된 사서함에서 발견 되 면이 옵션은 메시지의 복사본을 하나만 내보낼를 나타냅니다. 이 옵션을 함께 DSR에 대 한 최상의 사용자 환경에 단일 폴더에서 PST 파일을 사용 하면 하나에서 내보내는 메시지 내보내는 데 요청 합니다. 메모는 Results.csv 보고서 내보내기는 중복 된 메시지를 찾을 수 있는 위치를 모두 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p131">c. Select **Enable de-duplication** option to excludes duplicate email messages. We recommend this option because the built-in search searches all mailboxes in your organization. So if multiple copies of the same message are found in the mailboxes that were searched, this option means only one copy of a message will be exported. This option, together will exporting messages in one PST file in a single folder results in the best user experience for DSR export requests. Note that the Results.csv export report will list all locations where duplicate messages were found.</span></span>
    
    <span data-ttu-id="354d4-p132">필요에 따라 모든 버전의 SharePoint 및 OneDrive 문서를 내보낼 **포함 버전 SharePoint 문서에 대 한** 옵션을 선택할 수 있습니다. 이 문서 라이브러리에 대 한 해당 버전 관리 켜져 있어야 합니다. 모든 관련 데이터를 내보낼 되었는지 확인 하려면이 옵션을 사용 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p132">Optionally, you can select **Include versions for SharePoint documents** option to export all versions of SharePoint and OneDrive documents. This requires that versioning is turned on for document libraries. This option helps to ensure that all relevant data is exported.</span></span>
    
5. <span data-ttu-id="354d4-250">내보내기 설정을 선택 하면 후 **내보내기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-250">After you choose the export settings, click **Export**.</span></span>
    
    <span data-ttu-id="354d4-p133">검색 결과 Microsoft 클라우드에서 조직에 대 한 Azure 저장소 영역 업로드는 것을 의미 하는를 다운로드 하기 위한 준비 됩니다. 다음 단계는 로컬 컴퓨터에이 데이터를 다운로드 하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p133">The search results are prepared for downloading, which means they're uploaded to the Azure storage area for your organization in the Microsoft cloud. The next steps show you how to download this data to your local computer.</span></span>
    
6. <span data-ttu-id="354d4-p134">방금 만든 내보내기 작업을 표시 하려면 **내보내기** 탭을 클릭 합니다. Note는 내보내기 작업 이름이 같은 해당으로 **_Export** 검색 이름 끝에 추가 된를 사용 하 여 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p134">Click the **Export** tab to display the export job you just created. Note that export jobs have the same name as the corresponding search with **_Export** appended to the end of search name.</span></span> 
    
7. <span data-ttu-id="354d4-p135">방금 만든 내보내기 플라이 아웃 페이지를 표시 하려면 내보내기 작업을 클릭 합니다. 이 페이지를 내보낼 수 있는 항목의 총 크기 등의 검색 하 고 Azure 저장소 영역으로 전송 된 항목의 비율에 대 한 정보를 표시 합니다. 업로드 상태 정보를 업데이트 하려면 **Refresh** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p135">Click the export job that you just created to display the export flyout page. This page shows information about the search, such as the size and total number of items to be exported, and the percentage of the items that have been transferred to an Azure storage area. Click **Refresh** to update the upload status information.</span></span> 
    
8. <span data-ttu-id="354d4-p136">**키를 내보낼**에서 **클립보드에 복사**를 클릭 합니다. 11 단계에서이 키를 사용 하 여 검색 결과 다운로드 하려면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p136">Under **Export key**, click **Copy to clipboard**. You will use this key in step 11 to download the search results.</span></span>
    
9. <span data-ttu-id="354d4-260">클릭 ![내보내기 검색 결과 아이콘](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) 내보내기 플라이 아웃 페이지의 위쪽에 **결과 다운로드** 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-260">Click ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Download results** at the top of the export flyout page.</span></span> 
    
10. <span data-ttu-id="354d4-p137">페이지의 맨 아래에 팝업 창에서 **Microsoft Office 365 eDiscovery 내보내기 도구를**열려면 **열기** 를 클릭 합니다. **EDiscovery 내보내기 도구는** 검색 결과 다운로드 하는 처음으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p137">In the pop-up window at the bottom of the page, click **Open** to open the **Microsoft Office 365 eDiscovery Export Tool**. The **eDiscovery Export Tool** will be installed the first time you download search results.</span></span> 
    
11. <span data-ttu-id="354d4-263">**EDiscovery 내보내기 도구**해당 상자에는 8 단계에서 복사한 내보내기 키를 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-263">In the **eDiscovery Export Tool**, paste the export key that you copied in step 8 in the appropriate box.</span></span>
    
12. <span data-ttu-id="354d4-264">**찾아보기**를 클릭하여 검색 결과 파일을 다운로드하려는 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-264">Click **Browse** to specify the location where you want to download the search result files.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="354d4-265">디스크 작업 (읽기 및 쓰기) 양의 높은으로 인해 로컬 디스크 드라이브;에 검색 결과 다운로드 해야 매핑된 네트워크 드라이브 또는 기타 네트워크 위치에는 해당 다운로드 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="354d4-265">Due to the high amount of disk activity (reads and writes), you should download search results to a local disk drive; don't download them to a mapped network drive or other network location.</span></span> 
  
13. <span data-ttu-id="354d4-266">**시작**을 클릭하여 컴퓨터에 검색 결과를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-266">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="354d4-p138">**EDiscovery 내보내기 도구** 수 (및 크기)의 나머지 항목을 다운로드할 수 있는 예상을 포함 하는 내보내기 프로세스에 대 한 상태 정보를 표시 합니다. 내보내기 프로세스가 완료 되 면 파일 다운로드 한 있는 위치에 액세스할 수 있습니다. 콘텐츠 검색 결과 다운로드 하는 경우를 포함 하는 보고서에 대 한 자세한 내용은에서 [자세한 정보](export-search-results.md#more-information) 섹션을 참조 하십시오. "Office 365 보안에서 내보내기 콘텐츠 검색 결과가 &amp; 준수 센터" 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p138">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded. When the export process is complete, you can access the files in the location where they were downloaded. For more information about the reports that included when you download Content Search results, see the [More information](export-search-results.md#more-information) section in "Export Content Search results from the Office 365 Security &amp; Compliance Center".</span></span> 
    
<span data-ttu-id="354d4-p139">데이터를 내보낸 후 검색 결과 및 내보내기 보고서 DSR 대/소문자와 같은 이름을 가진 폴더에 있습니다. 사서함의 항목이 포함 된 PST 파일 **Exchange**라는 하위 폴더에 있습니다. 문서 및 사이트에서 다른 항목은 **SharePoint**라는 하위 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p139">After the data is exported, the search results and export reports are located in a folder that has the same name as the DSR case. The PST files that contain mailbox items are located in a subfolder named **Exchange**. Documents and other items from sites are located in a subfolder named **SharePoint**.</span></span> 
  
## <a name="optional-step-5-revise-the-built-in-search-query"></a><span data-ttu-id="354d4-273">(선택 사항) 5 단계: 기본 제공 검색 쿼리를 수정.</span><span class="sxs-lookup"><span data-stu-id="354d4-273">(Optional) Step 5: Revise the built-in search query</span></span>

<span data-ttu-id="354d4-p140">기본 제공 검색을 실행 하면 더 적은 수의 검색 결과 반환 하는 범위를 좁히기 위해 수정할 수 있습니다. 쿼리에 조건을 추가 하 여이 수행할 수 있습니다. 조건에 **AND** 연산자가 키워드 쿼리를 논리적으로 연결 됩니다. 즉 검색 결과에 반환 될 항목 키워드 쿼리 및 추가한 모든 조건을 모두 충족 해야 합니다. 결과 범위를 좁힐 수 조건 도움이 되는 방식입니다. 검색 쿼리 (서로 다른 속성을 지정 하는 조건)에 둘 이상의 고유한 조건을 추가 하는 경우 이러한 조건은 **AND** 연산자에서 논리적으로 연결 됩니다. 즉, (키워드 쿼리) 외에도 모든 조건에 맞는 항목만 반환 됩니다. 단일 조건에 여러 값 (쉼표 또는 세미콜론으로 구분)를 추가 하는 경우 해당 값 **또는** 연산자로 연결 됩니다. 즉, 조건에는 속성에 지정 된 값 중 하나를 포함 하는 경우 항목이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p140">After you run the built-in search, you can revise it to narrow the scope to return fewer search results. You can do this by adding conditions to the query. A condition is logically connected to the keyword query by the **AND** operator. That means to be returned in the search results, items must satisfy both the keyword query and any conditions you add. This is how conditions help to narrow the results. If you add two or more unique conditions to a search query (conditions that specify different properties), those conditions are logically connected by the **AND** operator. That means only items that satisfy all the conditions (in addition to the keyword query) are returned. If you add multiple values (separated by commas or semi-colons) to a single condition, those values are connected by the **OR** operator. That means items are returned if they contain any of the specified values for the property in the condition.</span></span> 
  
<span data-ttu-id="354d4-p141">다음은 DSR 사례의 기본 제공 검색 쿼리를 추가할 수 있는 조건 몇가지 예입니다. 검색 쿼리에 사용 되는 실제 속성의 이름에는 괄호 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p141">Here are some examples of the conditions that you can add to the built-in search query of a DSR case. The name of the actual property used in a search query is shown parentheses.</span></span>
  
- <span data-ttu-id="354d4-p142">**파일 형식 ( `filetype`)** -문서 또는 파일의 확장명을 지정 합니다. 이 조건을 사용 하 여 문서 및 Word, Excel, OneNote 등 특정 Office 응용 프로그램에서 만든 파일을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p142">**File type ( `filetype`)** - Specifies the extension of a document or file. Use this condition to search for documents and files created by specific Office applications, such as Word, Excel, and OneNote.</span></span> 
    
- <span data-ttu-id="354d4-p143">**메시지 형식 ( `kind`)** -검색에 대 한 전자 메일 항목의 종류를 지정 합니다. 구문을 사용 하 여 수 등 `kind:email OR kind:im` 비즈니스 대화 또는 팀이 Microsoft에서 일대일 채팅에 대 한 전자 메일 메시지 및 Skype를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p143">**Message type ( `kind`)** - Specifies the type of email item to search for. For example, you can use the syntax  `kind:email OR kind:im` to return only email messages and Skype for Business conversations or one-to-one chats in Microsoft Teams.</span></span> 
    
- <span data-ttu-id="354d4-p144">**규정 준수 태그 (`compliancetag`)** -전자 메일 메시지 또는 문서에 할당 된 레이블을 지정 합니다. 이 조건은 특정 레이블이 있는 분류 된 항목을 반환 합니다. 레이블은은 레이블으로 정의 된 분류에 따라 보존 규칙을 적용 하 고 전자 메일 및 데이터 관리 방식에 대 한 문서를 분류에 사용 됩니다. 조직 사용 레이블을 데이터 개인정보와 관련 된 콘텐츠를 분류할 중이거나 개인 데이터 또는 중요 한 정보를 포함 하는 때문에 DSR 조사에 대 한 유용한 조건입니다. 이 조건 값에 대 한 와일드 카드를 함께 전체 레이블 이름 또는 레이블 이름의 첫번째 부분을 사용 합니다. 자세한 내용은 [Office 365의 레이블 개요](labels.md)를 참고 하십시오.</span><span class="sxs-lookup"><span data-stu-id="354d4-p144">**Compliance tag (`compliancetag`)** - Specifies a label assigned to an email message or a document. This condition will return items that are classified with a specific label. Labels are used to classify email and documents for data governance and enforce retention rules based on the classification defined by the label. This is a useful condition for DSR investigations because your organization may be using labels to classify content related to data privacy or that contains personal data or sensitive information. For the value of this condition, use the complete label name or the first part of the label name with a wildcard. For more information, see [Overview of labels in Office 365](labels.md).</span></span>
    
<span data-ttu-id="354d4-295">목록과 DSR 사례 도구에서 사용할 수 있는 모든 조건에 이르는 대 한 "키워드 쿼리 및 콘텐츠 검색에 대 한 검색 조건을" 문서에서 [검색 조건](keyword-queries-and-search-conditions.md#search-conditions) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="354d4-295">For a list and description of all the conditions available in the DSR case tool, see [Search conditions](keyword-queries-and-search-conditions.md#search-conditions) in the "Keyword queries and search conditions for Content Search" article.</span></span> 
  
### <a name="changing-the-content-locations-that-are-searched"></a><span data-ttu-id="354d4-296">검색 되는 콘텐츠 위치 변경</span><span class="sxs-lookup"><span data-stu-id="354d4-296">Changing the content locations that are searched</span></span>

<span data-ttu-id="354d4-p145">DSR 사례에 대 한 기본 제공 검색을 수정 하는 것 외에도 검색 되는 콘텐츠 위치를 변경할 수 있습니다. 앞에서 설명한 것 처럼 기본 제공 검색 조직과 Exchange Online 모든 공용 폴더의 모든 사서함 및 사이트 검색합니다. 예,만 데이터 주체의 사서함 및 OneDrive 계정을 검색 하려면 검색의 범위를 좁힐 수 및 SharePoint 사이트를 선택 합니다. 특정 사이트를 검색 하는 경우를 검색 하려면 각 사이트에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p145">In addition to revising the built-in search for a DSR case, you can also change the content locations that are searched. As previously explained, the built-in search searches every mailbox and site in the organization, and any Exchange Online public folders. For example, you could narrow the search to only search the data subject's mailbox and OneDrive account and selected SharePoint sites. If you choose to search specific sites, you'll have to add each site that you want to search.</span></span>
  
<span data-ttu-id="354d4-301">위치를 수정 하려면는 콘텐츠를 검색 하려면:</span><span class="sxs-lookup"><span data-stu-id="354d4-301">To modify the content locations to search:</span></span>
  
1. <span data-ttu-id="354d4-302">기본 제공 검색에 대 한 콘텐츠 위치를 변경 하려면을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-302">Open the built-in search that you want to change the content locations for.</span></span>
    
2. <span data-ttu-id="354d4-303">검색 쿼리에서 **위치** **특정 위치** 옵션 옆에 있는 **수정** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-303">In the search query, under **Locations**, click **Modify** next to the **Specific locations** option.</span></span> 
    
    ![기본 제공 검색 쿼리의 콘텐츠 위치를 변경 하려면 수정을 클릭 합니다.](media/d66f7ba7-b71f-4ff5-a030-460ff02e3123.png)
  
    <span data-ttu-id="354d4-p146">**위치 수정** 플라이 아웃 페이지가 표시 됩니다. 기본 제공 검색 및 검색 되는 위치를 수정 하는 방법에 대 한 일부 정보에서 콘텐츠 위치에 대 한 설명은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p146">The **Modify locations** flyout page is displayed. Here's a description of the content locations in the built-in search and some information about modifying the locations that are searched.</span></span> 
    
    ![위치 플라이 아웃 페이지를 수정 합니다.](media/56c033f6-6735-46ba-abb2-a263a2b79836.png)
  
    <span data-ttu-id="354d4-p147">a. 토글 플라이 아웃 페이지의 위쪽에 사서함 섹션에서 **모두 선택** 아래에서 모든 사서함 검색 되는 것이 나타내는 선택 됩니다. 검색 범위를 좁힐 하을 선택 취소 합니다. 하 고 다음 **선택 사용자, 그룹 또는 팀을** 클릭 하 고 특정 사서함 검색을 선택 설정/해제를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p147">a. The toggle under **Select all** in mailbox section at the top of the flyout page is selected, which indicates that all mailboxes are searched. To narrow the scope of the search, click the toggle to unselect it, and then click **Choose users, groups, or teams** and choose specific mailboxes to search.</span></span>
    
    <span data-ttu-id="354d4-p148">b.는 토글 플라이 아웃 페이지의 가운데 사이트 섹션에서 **모두 선택** 아래에서 모든 사이트 검색 되 임을 나타내는 선택 됩니다. 선택한 사이트에 검색의 범위를 좁힐 수의 표시/숨기기를 선택 취소 합니다. 하는 다음 **선택 사이트**를 클릭 합니다. 해야 검색 하려는 각 특정 사이트에 추가할 데이터 주체의 OneDrive 계정 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p148">b. The toggle under **Select all** in the sites section in the middle of the flyout page is selected, which indicates that all sites are searched. To narrow the search to selected sites, you would unselect the toggle and then click **Choose sites**. You'll have to add each specific site that you want to search, including the data subject's OneDrive account.</span></span>
    
    <span data-ttu-id="354d4-p149">모든 Exchange 공용 폴더를 검색 하는 것을 의미 하는 Exchange 공용 폴더 섹션에서 c. 토글 선택 됩니다. 참고만 모든 Exchange 공용 폴더 또는 그 중 검색할 수 있습니다. 검색 하는 특정 이벤트를 선택할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p149">c. The toggle in the Exchange public folders section is selected, which means all Exchange public folders are searched. Note that you can only search all Exchange public folders or none of them. You can't choose specific ones to search.</span></span>
    
3. <span data-ttu-id="354d4-319">기본 제공 검색에서 콘텐츠 위치를 수정 하는 경우를 클릭 **저장 &amp; 실행** 다시 검색을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-319">If you modify the content locations in the built-in search, click **Save &amp; run** to re-start the search.</span></span> 
  
## <a name="more-information-about-using-the-dsr-case-tool"></a><span data-ttu-id="354d4-320">DSR 사례 도구를 사용 하는 방법에 대 한 자세한 내용</span><span class="sxs-lookup"><span data-stu-id="354d4-320">More information about using the DSR case tool</span></span>

<span data-ttu-id="354d4-321">다음 섹션에서는 DSR 사례 도구를 사용 하 여 DSR 내보내기 요청에 응답 하는 방법에 대 한 자세한 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-321">The following sections contain more information about using the DSR case tool to respond to DSR export requests.</span></span>
  
[<span data-ttu-id="354d4-322">MyAnalytics 및 Office 로밍 서비스에서 데이터 내보내기 (영문)</span><span class="sxs-lookup"><span data-stu-id="354d4-322">Exporting data from MyAnalytics and the Office Roaming Service</span></span>](#exporting-data-from-myanalytics-and-the-office-roaming-service)

[<span data-ttu-id="354d4-323">부분적으로 인덱싱된 항목 내보내기 (영문)</span><span class="sxs-lookup"><span data-stu-id="354d4-323">Exporting partially indexed items</span></span>](#exporting-partially-indexed-items)

[<span data-ttu-id="354d4-324">검색 및 팀이 Microsoft 및 Office 365 그룹에서 데이터 내보내기 (영문)</span><span class="sxs-lookup"><span data-stu-id="354d4-324">Searching and exporting data from Microsoft Teams and Office 365 Groups</span></span>](#searching-and-exporting-data-from-microsoft-teams-and-office-365-groups)

[<span data-ttu-id="354d4-325">Exchange 공용 폴더를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-325">Searching Exchange public folders</span></span>](#searching-exchange-public-folders)
  
### <a name="exporting-data-from-myanalytics-and-the-office-roaming-service"></a><span data-ttu-id="354d4-326">MyAnalytics 및 Office 로밍 서비스에서 데이터 내보내기 (영문)</span><span class="sxs-lookup"><span data-stu-id="354d4-326">Exporting data from MyAnalytics and the Office Roaming Service</span></span>

<span data-ttu-id="354d4-p150">DSR 사례 도구를 사용 하 여 검색 하 고 MyAnalytics 및 Office 로밍 서비스에 의해 생성 되는 사용 현황 데이터를 내보낼 수 있습니다. 이러한 서비스를 어떤 대 한 설명은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p150">You can use the DSR case tool to search for and export usage data that's generated by MyAnalytics and the Office Roaming Service. Here's a description of what these services do:</span></span>
  
- <span data-ttu-id="354d4-p151">**MyAnalytics** -사용자에 게 자신의 사서함에 메일 및 일정 데이터를 기반으로 자신의 시간 하는데 드는 방법에 대 한 정보를 제공 합니다. 모든 MyAnalytics 정보는 사용자의 사서함에서 전자 메일 및 모임 머리글에서 파생 됩니다. MyAnalytics 라이선스를 할당 되는 사용자는 Office 365에 로그인 수 있으며 해당 시간 하는데 드는 방법에 대 한 정보를 보려면 MyAnalytics 대시보드로 이동 수 있습니다. (사용자가 이러한 정보는 DSR 액세스 요청에 대 한 응답으로의 샷 화면 수)입니다. DSR 경우에는 기본 제공 검색으로 MyAnalytics 인 사이트를 생성 하는데 사용 되는 데이터를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p151">**MyAnalytics** - Provides users with insights about how they spend their time based on the mail and calendar data in their mailbox. All MyAnalytics insights are derived from email and meeting headers in the user's mailbox. Users that are assigned a MyAnalytics license can sign in to Office 365 and go to the MyAnalytics dashboard to view the insights about how they spend their time. (Users can screen shots of these insights in response to a DSR access request). The built-in search in a DSR case will export the data that's used to generate MyAnalytics insights.</span></span> 
    
- <span data-ttu-id="354d4-334">**Office 로밍 서비스** -로밍은 Office 테마, 사용자 지정 사전, 언어 설정, 개발자 모드 및 자동 고침 등의 Office와 관련 된 설정을 저장 하는 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-334">**Office Roaming Service** - Roaming is a service that stores Office-related settings, such as Office theme, custom dictionary, language settings, developer mode, and auto correct.</span></span> 
    
<span data-ttu-id="354d4-p152">MyAnalytics 및 Office 로밍 서비스에서 데이터는 Exchange Online 사서함의 아닌 개인 간 메시지 (IPM이 아닌) 하위에 있는 숨겨진된 폴더에 데이터 주체의 사서함에 저장 됩니다. 즉, 자신의 사서함에 액세스 하려면 Outlook 또는 다른 메일 클라이언트를 사용할 때 사용자의 보기에서 데이터 숨겨집니다. 숨겨진된 폴더에 대 한 자세한 내용은 [MAPI 숨겨진 폴더](https://go.microsoft.com/fwlink/?linkid=872758)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="354d4-p152">The data from MyAnalytics and the Office Roaming service is stored in a data subject's mailbox in hidden folders located in a non-interpersonal message (non-IPM) subtree of Exchange Online mailboxes. This means the data is hidden from the user's view when they use Outlook or other mail clients to access their mailbox. For more information about hidden folders, see [MAPI Hidden Folders](https://go.microsoft.com/fwlink/?linkid=872758).</span></span>
  
<span data-ttu-id="354d4-p153">별도 콘텐츠 검색 (만들고 수 DSR 사례와 연결)는 MyAnalytics 반환 하 고 데이터의 제목에 사서함에 있는 Office 로밍 서비스 사용 현황 데이터입니다. 이 데이터는 검색 통계에 포함 되지 않습니다 및 미리 보기를 위해 사용할 수 없습니다. 하지만 인증서를 내보내려는 하 고 DSR 내보내기 요청에 대 한 응답으로 데이터 주제를 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p153">You can create a separate content search (and associate it with a DSR case) that returns the MyAnalytics and the Office Roaming Service usage data in the data's subjects mailbox. This data isn't included in the search statistics and it won't be available for preview. But you can export it and then give it to the data subject in response to a DSR export request.</span></span>
  
<span data-ttu-id="354d4-p154">MyAnalytics 및 Office 로밍 서비스에서 데이터를 내보낼 때 데이터 데이터 주체의 전자 메일 주소를 가진 이름을 나타내는 폴더 아래에 있는 **ApplicationDataRoot** 폴더에 있는 각 응용 프로그램에 대 한 별도 폴더에 저장 됩니다. 이 데이터는 사용자를 읽을 수 있는 텍스트 파일을 전자 메일 메시지에 연결 된 XML 또는 TXT 파일 비슷합니다 JSON 파일로 내보내집니다. 현재는 이러한 폴더는 다음 표에 나열 된 MyAnalytics 및 Office 로밍 서비스에 할당 된 전역적으로 고유 식별자 (GUID)로 이름이 지정 됩니다. DSR 사례 도구의 이후 버전에서 GUID는 실제 응용 프로그램의 이름으로 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p154">When you export data from MyAnalytics and the Office Roaming Service, the data is saved to a separate folder for each application that's located in the **ApplicationDataRoot** folder, which is under a folder that is name with the data subject's email address. This data is exported as JSON files, which are human-readable text files similar to XML or TXT files, that are attached to email messages. Currently, these folders are named with a globally unique identifier (GUID) that's assigned to MyAnalytics and the Office Roaming Service, which are listed in the following table. In future versions of the DSR case tool, the GUID will be replaced with the name of the actual application.</span></span> 
  
|<span data-ttu-id="354d4-345">**응용 프로그램**</span><span class="sxs-lookup"><span data-stu-id="354d4-345">**Application**</span></span>|<span data-ttu-id="354d4-346">**GUID/폴더 이름**</span><span class="sxs-lookup"><span data-stu-id="354d4-346">**GUID/folder name**</span></span>|
|:-----|:-----|
|<span data-ttu-id="354d4-347">MyAnalytics</span><span class="sxs-lookup"><span data-stu-id="354d4-347">MyAnalytics</span></span>  <br/> |<span data-ttu-id="354d4-348">3c896ded-22c5-450f-91f6-3d1ef0848f6e</span><span class="sxs-lookup"><span data-stu-id="354d4-348">3c896ded-22c5-450f-91f6-3d1ef0848f6e</span></span>  <br/> |
|<span data-ttu-id="354d4-349">Office 로밍 서비스</span><span class="sxs-lookup"><span data-stu-id="354d4-349">Office Roaming Service</span></span>  <br/> |<span data-ttu-id="354d4-350">1caee58f-eb14-4a6b-9339-1fe2ddf6692b</span><span class="sxs-lookup"><span data-stu-id="354d4-350">1caee58f-eb14-4a6b-9339-1fe2ddf6692b</span></span>  <br/> |
   
 <span data-ttu-id="354d4-351">**검색 하 고 MyAnalytics 및 Office 로밍 서비스 데이터를 내보냅니다.**</span><span class="sxs-lookup"><span data-stu-id="354d4-351">**To search for and export MyAnalytics and Office Roaming Service data:**</span></span>
  
1. <span data-ttu-id="354d4-352">보안에서 &amp; 준수 센터 **데이터 프라이버시** 를 클릭 \> **데이터 주체 요청**을 한 다음 **열기** 를 클릭 DSR 대/소문자 옆에 대 한 사용 현황 데이터를 내보낼 원본 데이터 제목에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-352">In the Security &amp; Compliance Center, click **Data privacy** \> **Data subject requests**, and then click **Open** next to the DSR case for the data subject that you want to export usage data for.</span></span> 
    
2. <span data-ttu-id="354d4-353">페이지의 맨 아래에 있는 **검색** 탭을 클릭 하 고 다음을 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **안내 검색**합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-353">Click the **Search** tab at the top of the page, and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif) **Guided search**.</span></span>
    
3. <span data-ttu-id="354d4-354">**사용자 검색 이름** 지정 페이지에서 **취소** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-354">Click **Cancel** on the **Name your search** page.</span></span> 
    
4. <span data-ttu-id="354d4-355">**검색 쿼리** **유형** 조건에서 **MyAnalytics** 및 **Office 로밍 서비스**옆에 있는 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-355">Under **Search query**, in the **Type** condition, select the check boxes next to **MyAnalytics** and **Office Roaming Service**.</span></span> 
    
    ![사용 현황 데이터를 내보낼 MyAnalytics Office 로밍 서비스 확인란을 선택](media/3dacbc7a-c314-492c-828c-6757fda84963.png)
  
    <span data-ttu-id="354d4-p155">Note (하는 전자 메일 메시지 클래스는) **종류** 조건을 검색 쿼리에 항목만 되도록 합니다. **키워드** 상자를 삭제 하거나는 비워둡니다 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p155">Note that the **Type** condition (which are email message classes) should be the only item in the search query. You can delete the **Keywords** box or leave it blank.</span></span> 
    
5. <span data-ttu-id="354d4-359">**위치** **특정 위치** 선택 되어있는지 확인 하 고 한 다음 **수정**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-359">Under **Locations**, make sure **Specific locations** is selected and then click **Modify**.</span></span>
    
6. <span data-ttu-id="354d4-360">**위치 수정** 플라이 아웃 페이지 (사서함 섹션)의 위쪽 부분에서 **선택 사용자, 그룹 또는 팀을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-360">On top part of the **Modify locations** flyout page (the mailbox section), click **Choose users, groups, or teams**.</span></span>
    
7. <span data-ttu-id="354d4-361">**위치 편집** 페이지에서 **선택 사용자, 그룹 또는 팀이**를 클릭 하 고 데이터 주체의 사서함을 선택한 다음 선택 항목을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-361">On the **Edit locations** page, click **Choose users, groups, or teams**, choose the data subject's mailbox, and then save your selection.</span></span> 
    
8. <span data-ttu-id="354d4-362">클릭 **저장 &amp; 실행**, 하 고 다음 이름을 검색 하 고 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-362">Click **Save &amp; run**, and then name the search and save it.</span></span>
    
    <span data-ttu-id="354d4-363">검색 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-363">The search is started.</span></span>
    
 <span data-ttu-id="354d4-364">**데이터를 내보낼 MyAnalytics 및 Office 로밍 서비스:**</span><span class="sxs-lookup"><span data-stu-id="354d4-364">**To export MyAnalytics and Office Roaming Service data:**</span></span>
  
1. <span data-ttu-id="354d4-p156">이전 단계에서 만든 검색 완료 되 면 페이지의 맨 아래에 있는 **검색** 탭을 클릭 한 다음 검색 옆에 있는 확인란을 클릭 합니다. 눌러야 할 수도 ![새로고침](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) **새로고침** 검색을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p156">When the search that you created in the previous step is complete, click the **Search** tab at the top of the page, and then click the checkbox next to the search. You may have to click ![refresh](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) **Refresh** to display the search.</span></span> 
    
2. <span data-ttu-id="354d4-367">검색 플라이 아웃 페이지에서 다음을 클릭 ![내보내기 검색 결과 아이콘](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **더 많은**, 하 고 드롭다운 목록에서 **검색 결과 내보내기 결과** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-367">On the search flyout page, click ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **More**, and then select **Export results** from the drop-down list.</span></span> 
    
3. <span data-ttu-id="354d4-368">**결과 내보내기** 페이지에서 이러한 권장 사용 현황 데이터를 내보내려면 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-368">On the **Export results** page, select the these recommended options to export usage data.</span></span> 
    
    ![MyAnalytics 및 Office 로밍 서비스 사용 현황 데이터를 내보낼 때 내보내기 옵션](media/470a7d1e-eeae-4b42-95aa-15cb82ce2f68.png)
  
    <span data-ttu-id="354d4-p157">a. **출력 옵션**인덱싱된 항목에만 내보낼 첫번째 옵션 ( **모든 항목을 보유 하는 인식할 수 없는 형식, 암호화 된 되었거나 다른 이유로 인덱싱된 받지를 포함 하는 것을 제외**)을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p157">a. Under **Output options**, select the first option ( **All items, excluding ones that have ones that have an unrecognized format, are encrypted, or weren't indexed for other reasons**) to export indexed items only.</span></span>
    
    <span data-ttu-id="354d4-p158">b. **내보내기 Exchange 콘텐츠**를에서 두번째 옵션을 **모든 메시지를 포함 하는 하나의 PST 파일**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p158">b. Under **Export Exchange content as**, select the second option, **One PST file containing all messages**.</span></span>
    
    <span data-ttu-id="354d4-p159">c. 옵션의 선택을 취소 하는 나머지 내보내기 옵션을 그대로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p159">c. Leave the remaining export options unselected.</span></span>
    
4. <span data-ttu-id="354d4-376">내보내기 설정을 선택 하면 후 **내보내기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-376">After you choose the export settings, click **Export**.</span></span>
    
    <span data-ttu-id="354d4-p160">검색 결과 Microsoft 클라우드에서 조직에 대 한 Azure 저장소 영역 업로드는 것을 의미 하는를 다운로드 하기 위한 준비 됩니다. 다음 단계는 로컬 컴퓨터에이 데이터를 다운로드 하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p160">The search results are prepared for downloading, which means they're uploaded to the Azure storage area for your organization in the Microsoft cloud. The next steps show you how to download this data to your local computer.</span></span>
    
5. <span data-ttu-id="354d4-p161">방금 만든 내보내기 작업을 표시 하려면 **내보내기** 탭을 클릭 합니다. Note는 내보내기 작업 이름이 같은 해당으로 **_Export** 검색 이름 끝에 추가 된를 사용 하 여 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p161">Click the **Export** tab to display the export job you just created. Note that export jobs have the same name as the corresponding search with **_Export** appended to the end of search name.</span></span> 
    
6. <span data-ttu-id="354d4-381">방금 만든 내보내기 플라이 아웃 페이지를 표시 하려면 내보내기 작업을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-381">Click the export job that you just created to display the export flyout page.</span></span> 
    
7. <span data-ttu-id="354d4-p162">**키를 내보낼**에서 **클립보드에 복사**를 클릭 합니다. 10 단계에서이 키를 사용 하 여 검색 결과 다운로드 하려면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p162">Under **Export key**, click **Copy to clipboard**. You will use this key in step 10 to download the search results.</span></span>
    
8. <span data-ttu-id="354d4-384">클릭 ![내보내기 검색 결과 아이콘](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) 내보내기 플라이 아웃 페이지의 위쪽에 **결과 다운로드** 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-384">Click ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Download results** at the top of the export flyout page.</span></span> 
    
9. <span data-ttu-id="354d4-p163">페이지의 맨 아래에 팝업 창에서 **Microsoft Office 365 eDiscovery 내보내기 도구를**열려면 **열기** 를 클릭 합니다. **EDiscovery 내보내기 도구는** 검색 결과 다운로드 하는 처음으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p163">In the pop-up window at the bottom of the page, click **Open** to open the **Microsoft Office 365 eDiscovery Export Tool**. The **eDiscovery Export Tool** will be installed the first time you download search results.</span></span> 
    
10. <span data-ttu-id="354d4-387">**eDiscovery 내보내기 도구**에서 7단계에서 복사한 내보내기 키를 해당 상자에 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-387">In the **eDiscovery Export Tool**, paste the export key that you copied in step 7 in the appropriate box.</span></span>
    
11. <span data-ttu-id="354d4-388">**찾아보기**를 클릭하여 검색 결과 파일을 다운로드하려는 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-388">Click **Browse** to specify the location where you want to download the search result files.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="354d4-389">디스크 작업 (읽기 및 쓰기) 양의 높은으로 인해 로컬 디스크 드라이브;에 검색 결과 다운로드 해야 매핑된 네트워크 드라이브 또는 기타 네트워크 위치에는 해당 다운로드 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="354d4-389">Due to the high amount of disk activity (reads and writes), you should download search results to a local disk drive; don't download them to a mapped network drive or other network location.</span></span> 
  
12. <span data-ttu-id="354d4-390">**시작**을 클릭하여 컴퓨터에 검색 결과를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-390">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="354d4-p164">**EDiscovery 내보내기 도구** 수 (및 크기)의 나머지 항목을 다운로드할 수 있는 예상을 포함 하는 내보내기 프로세스에 대 한 상태 정보를 표시 합니다. 내보내기 프로세스가 완료 되 면 Outlook에서 Exchange PST 파일을 열고 하 고 MyAnalytics와 로밍 서비스에 하위 폴더에 액세스 하려면 **ApplicationDataRoot** 폴더로 이동 하는 다음 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p164">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded. When the export process is complete, you can open the Exchange PST file in Outlook and then go to the **ApplicationDataRoot** folder to access the subfolders to MyAnalytics and Roaming service.</span></span> 
    
    <span data-ttu-id="354d4-p165">앞에서 설명한 것 처럼 사용 현황 데이터를 포함 하는 JSON 파일은 메시지에 첨부 됩니다. JSON 파일을 보려면 메시지를 클릭 한 다음 연결 된 JSON 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p165">As previously explained, the JSON files that contains usage data are attached to messages. To view a JSON file, click a message and then open the attached JSON file.</span></span> 
  
### <a name="exporting-partially-indexed-items"></a><span data-ttu-id="354d4-395">부분적으로 인덱싱된 항목 내보내기 (영문)</span><span class="sxs-lookup"><span data-stu-id="354d4-395">Exporting partially indexed items</span></span>

<span data-ttu-id="354d4-p166">새 DSR 사례를 만들 때 만들어지는 기본 제공 검색에서 부분적으로 인덱싱된 항목 (인덱싱되지 않은 항목 라고도 함)를 내보내지 마십시오 하는 것이 좋습니다. 없기 때문입니다 결과 부분적으로 포함 이상 될 가능성이 높습니다 검색 인덱스 조직 전체에서 다른 사용자에 대 한 항목 하지 방금 부분적으로 데이터 주제에 대 한 인덱스 항목). 대신, 데이터 주제와 관련 된 부분적으로 인덱싱된 항목을 내보낼 내도록 설계 된다 DSR 대/소문자와 관련 된 별도 콘텐츠 검색을 만들어야 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p166">We recommend that you don't export partially indexed items (also called unindexed items) from the built-in search that's created when you create a new DSR case. That's because the search results will more than likely include partially indexed items for other users in your organization, and not just partially indexed items for the data subject). Instead, we recommend that you create a separate Content Search that's associated with the DSR case that's designed to export only the partially indexed items related to the data subject.</span></span> 
  
<span data-ttu-id="354d4-p167">부분적으로 인덱싱된 항목을 내보내는 데 높은 수준의 프로세스는 다음과 같습니다. 내보내기를 놓은 후는 항목은 DSR access에 응답 하는 경우를 확인 하려면 해당 오류를 검토할 수도 있고 요청을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p167">Here's a high-level process to export partially indexed items. After they're export, you can review them to determine if an items is responsive to a DSR access or export request.</span></span>
  
1. <span data-ttu-id="354d4-401">DSR 대/소문자를 열고 **검색** 페이지에서 새 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-401">Open the DSR case and create a new search on the **Search** page.</span></span> 
    
2. <span data-ttu-id="354d4-402">검색 쿼리 및 콘텐츠 위치를 구성 하기 위한 다음 조건을 사용 하 여 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-402">Use the following criteria for configuring the search query and the content locations to search:</span></span>
    
    - <span data-ttu-id="354d4-p168">비어 있지/빈 키워드 쿼리를 사용 합니다. 이 검색 되는 콘텐츠 위치에 모든 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p168">Use an empty/blank keyword query. This will return all items in the content locations that are searched.</span></span>
    
    - <span data-ttu-id="354d4-405">데이터 주체의 Exchange Online 사서함만 하 고 자신의 OneDrive 계정을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-405">Search only the data subject's Exchange Online mailbox and their OneDrive account.</span></span>
    
3. <span data-ttu-id="354d4-p169">검색을 실행 하 고 완료 한 후에 내보낼 수 있으며 ( [4 단계에서](#step-4-export-the-data)에서 설명)에 따라 검색 결과 다운로드할 수 있습니다. 부분적으로 인덱싱된 항목을 내보내려면 다음 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p169">After you run the search and it completes, you can export and download the search results (as described in [Step 4](#step-4-export-the-data)). Use the following settings to export partially indexed items.</span></span> 
    
    - <span data-ttu-id="354d4-408">**출력 옵션**부분적으로 인덱싱된 항목에만 내보내려면 세번째 옵션 ( **인식할 수 없는 형식이 있는 항목에 대해서만 암호화 된 또는 다른 이유로 인덱싱된 받지**)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-408">Under **Output options**, select the third option ( **Only items that have an unrecognized format, are encrypted, or weren't indexed for other reasons**) to export partially indexed items only.</span></span>
    
    - <span data-ttu-id="354d4-409">**내보내기 Exchange 콘텐츠를**사용자의 기본 설정에 따라 모든 옵션을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-409">Under **Export Exchange content as**, you can select any option based on your preferences.</span></span> 
    
    - <span data-ttu-id="354d4-410">**SharePoint 문서에 대 한 포함 버전** 옵션을 선택 하는 버전은 인덱싱됩니다 부분적으로 하는 경우 문서 버전 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-410">Selecting the **Include versions for SharePoint documents** option will export versions of documents if a version is partially indexed.</span></span> 
    
<span data-ttu-id="354d4-411">부분적으로 인덱싱된 항목에 대 한 자세한 내용은 다음을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-411">For more information about partially indexed items, see:</span></span> 
  
- [<span data-ttu-id="354d4-412">Office 365의 콘텐츠 검색에서 부분적으로 인덱싱된 항목</span><span class="sxs-lookup"><span data-stu-id="354d4-412">Partially indexed items in Content Search in Office 365</span></span>](partially-indexed-items-in-content-search.md)

- [<span data-ttu-id="354d4-413">부분적으로 인덱싱된 항목 내보내기 (영문)</span><span class="sxs-lookup"><span data-stu-id="354d4-413">Exporting partially indexed items</span></span>](export-search-results.md#exporting-partially-indexed-items)
    
### <a name="searching-and-exporting-data-from-microsoft-teams-and-office-365-groups"></a><span data-ttu-id="354d4-414">검색 및 팀이 Microsoft 및 Office 365 그룹에서 데이터 내보내기 (영문)</span><span class="sxs-lookup"><span data-stu-id="354d4-414">Searching and exporting data from Microsoft Teams and Office 365 Groups</span></span>

<span data-ttu-id="354d4-p170">Microsoft 팀의 (팀 채팅 또는 일대일 채팅 라고 함)에서 채팅 목록에 포함 된 대화의 채팅에 참가 한 사용자의 Exchange Online 사서함에 저장 됩니다. 또한 사용자를 일대일 채팅에서 공유 파일의 파일을 공유 하는 사람 OneDrive 계정에 저장 됩니다. 조직에서 모든 사서함 및 OneDrive 계정을 검색 하는 기본 제공 검색, 때문에 팀 채팅, 채팅 세션 (즉 데이터 제목으로 만들거나 업로드할)에서 공유 문서 DSR 경우에서 기본 제공 검색을 통해 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p170">Conversations that are part of the Chat list in Microsoft Teams (called Team chats or one-to-one chats) are stored in the Exchange Online mailbox of the users who participate in the chats. Also, the files a person shares in a one-to-one chat are stored in the OneDrive account of the person who shares the file. Because the built-in search searches all mailboxes and OneDrive accounts in the organization, team chats and documents shared in a chat session (that the data subject created or uploaded) will be returned by built-in search in a DSR case.</span></span>
  
<span data-ttu-id="354d4-p171">또는 (채널 메시지 라고도 함)는 팀이 채널의 일부인 대화 팀과 연결 된 사서함에 저장 됩니다. 이러한 유형의 대화에 참가 한 데이터 주제는 Microsoft 팀과 연관 된 모든 사서함은 검색 하기 때문에 기본 제공 검색에 의해 반환 됩니다. 또한 데이터 제목 팀 채널에 공유는 수 타일 팀의 SharePoint 사이트에 저장 됩니다. 파일 작성 또는 uploadedby 데이터 제목 반환 됩니다 DSR 경우에는 기본 제공 검색 하 여 Microsoft 팀과 연관 된 사이트 검색에 포함 되어 있으므로 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p171">Alternatively, conversations that are part of a Teams channel (also called channel messages) are stored in the mailbox that's associated with a team. These types of conversations that the data subject participated in are also returned by the built-in search because all mailboxes associated with Microsoft Teams are searched. Additionally, tiles that a data subject might have shared in a Teams channel are stored on the team's SharePoint site. Files created or uploadedby the data subject will be returned by the built-in search in a DSR case because sites associated with Microsoft Teams are included in the search.</span></span>
  
<span data-ttu-id="354d4-p172">마찬가지로, 사서함 및 SharePoint 사이트는 Office 365 그룹에 해당 하는 기본 제공 검색에도 포함 됩니다. 즉, 데이터 제목별으로 보내거나 받는 경우 전자 메일 메시지를 작성 하거나 데이터 제목별으로 업로드 한 파일이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p172">Similarly, mailboxes and SharePoint sites that correspond to an Office 365 Group are also included in the built-in search. This means that email messages that where sent or received by the data subject and files created or uploaded by the data subject will be returned.</span></span> 
  
<span data-ttu-id="354d4-424">콘텐츠 검색을 사용 하 여 Microsoft 팀의 및 Office 365 그룹에서 항목을 검색 하거나 한 구성원의 목록을 가져오려면 하는 방법을 확인 하는 방법에 대 한 자세한 내용은 [Office 365에서 콘텐츠 검색](content-search.md#searching-microsoft-teams-and-office-365-groups)에서 "검색 Microsoft 팀 및 Office 365 그룹" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="354d4-424">For more information about using Content Search to search for items in Microsoft Teams and Office 365 Groups or to see how to get a list of a members, see the "Searching Microsoft Teams and Office 365 Groups" section in [Content Search in Office 365](content-search.md#searching-microsoft-teams-and-office-365-groups).</span></span> 
  
### <a name="searching-exchange-public-folders"></a><span data-ttu-id="354d4-425">Exchange 공용 폴더를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-425">Searching Exchange public folders</span></span>

<span data-ttu-id="354d4-p173">DSR 경우에는 기본 제공 검색이만 반환 전자 메일 메시지를 메일 사용이 가능한 공용 폴더 또는 공용 폴더로 전송 다른 사용자와 데이터 주제를 복사 하는 메시지에는 데이터 제목 보내지는지 합니다. 공용 폴더에 데이터 제목 수 게시 된 메시지를 반환 하지 않습니다. 공용 폴더에 게시 된 데이터 제목 항목을 검색 하려면 별도 만들 수 있습니다 데이터 제목별 공용 폴더에 게시 된 모든 항목을 검색 하는 별도 콘텐츠 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p173">The built-in search in a DSR case will only return email messages that the data subject sent to a mail-enabled public folder or messages that someone else sent to a public folder and also copied the data subject . It will not return message that the data subject might have posted to a public folder. To search for items that the data subject posted to a public folder, you can create a separate create a separate Content Search that searches for any item posted to a public folder by the data subject.</span></span>
  
<span data-ttu-id="354d4-429">데이터 제목 공용 폴더에 게시 된 수 있는 항목에 대 한 검색을 높은 수준의 프로세스는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-429">Here's a high-level process to search for items that the data subject might have posted to a public folder.</span></span> 
  
1. <span data-ttu-id="354d4-430">DSR 대/소문자를 열고 **검색** 페이지에서 새 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-430">Open the DSR case and create a new search on the **Search** page.</span></span> 
    
2. <span data-ttu-id="354d4-431">검색 쿼리 및 콘텐츠 위치를 구성 하기 위한 다음 조건을 사용 하 여 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-431">Use the following criteria for configuring the search query and the content locations to search:</span></span>
    
  - <span data-ttu-id="354d4-432">**키워드** 상자에 다음과 같은 검색 쿼리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-432">In the **Keywords** box, use the following search query:</span></span> 
    
    ```
    itemclass:ipm.post AND "<email address of the data subject>"
    ```

  - <span data-ttu-id="354d4-433">모든 Exchange 공용 폴더를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-433">Search all Exchange public folders</span></span>
    
  - <span data-ttu-id="354d4-p174">검색을 실행 하 고 완료 한 후에 내보낼 수 있으며 ( [4 단계에서](manage-gdpr-data-subject-requests-with-the-dsr-case-tool.md#step4)에서 설명)에 따라 검색 결과 다운로드할 수 있습니다. 부분적으로 인덱싱된 항목을 내보내려면 다음 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="354d4-p174">After you run the search and it completes, you can export and download the search results (as described in [Step 4](manage-gdpr-data-subject-requests-with-the-dsr-case-tool.md#step4)). Use the following settings to export partially indexed items.</span></span> 
