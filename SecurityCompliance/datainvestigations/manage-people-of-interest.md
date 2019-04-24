---
title: 데이터 조사에 관심이 있는 사용자 관리 (미리 보기)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d06dde60ae75cfea1bf1d79f445b613d20a76363
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32257676"
---
# <a name="manage-people-of-interest-in-data-investigations-preview"></a><span data-ttu-id="ccd19-102">데이터 조사에 관심이 있는 사용자 관리 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="ccd19-102">Manage people of interest in Data Investigations (Preview)</span></span>

<span data-ttu-id="ccd19-103">데이터 조사에는 관심 있는 사용자가 포함 되는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-103">Data investigations often involve people of interest.</span></span> <span data-ttu-id="ccd19-104">일반적으로 사용자는 조사 하거나 수정 하려는 잘못 된 데이터를 소유 하 고 있거나, 중요 하거나 악의적으로 검토 하는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-104">Usually they are people who own the misplaced, sensitive or malicious data that you're investigating or looking to remediate.</span></span> <span data-ttu-id="ccd19-105">**데이터 조사 (미리 보기)** 에서는 검색 범위를 지정 하는 데 사용할 데이터 원본을 검색 하거나 연락처, 위치 및 활동 로그 등의 추가 정보를 볼 수 있도록 추가 작업을 추가할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-105">In **Data Investigations (Preview)**, you can add them to discover their data sources to use in scoping your search or view additional information such as contact, location and activity logs.</span></span> 


## <a name="add-people-of-interest"></a><span data-ttu-id="ccd19-106">관심 있는 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="ccd19-106">Add people of interest</span></span>

<span data-ttu-id="ccd19-107">**관심 있는 사용자** 탭에서는 관심 있는 사용자를 추가 하 고 Exchange 사서함 또는 비즈니스용 OneDrive 사이트와 같은 데이터 원본을 검색 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-107">In **People of interest** tab, you can add people of interest and discover their data sources such as Exchange mailboxes or OneDrive for Business site that you can use to scope your search.</span></span> <span data-ttu-id="ccd19-108">관심 있는 사용자가 범위를 지정 하는 경우 도구에서 이미지 또는 지원 되지 않는 파일 형식 등의 인덱싱되지 않은 데이터를 다시 처리 하기 때문에 검색 성능이 더욱 향상 되 고 정확 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-108">When scoped down by people of interest, searches are more performant and accurate because the tool re-processes any unindexed data such as images or unsupported file types.</span></span> <span data-ttu-id="ccd19-109">또한 통신을 시작 하거나 활동을 보다 자세히 조사 하는 데 사용할 수 있는 연락처 정보, 위치 정보 및 활동 로그도 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-109">You can also see their contact information, location information and activity logs that you can use to initiate communications or further investigate their activities.</span></span> 

<span data-ttu-id="ccd19-110">조사에 관심 있는 사용자를 추가 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-110">To add people of interest to an investigation:</span></span>

1. <span data-ttu-id="ccd19-111">**데이터 조사 (미리 보기)** 페이지에서 조사로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-111">From the **Data Investigations (Preview)** page, go to your investigation.</span></span>
 
2. <span data-ttu-id="ccd19-112">조사를 선택한 후 **관심 있는 사람** 탭으로 이동 하 여 **원하는 사용자 추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-112">After you have selected a investigation, go to the **People of interest** tab and click **+ Add people of interest**.</span></span> 
 
3. <span data-ttu-id="ccd19-113">조사에 추가 하려는 사용자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-113">Choose people that you want to add to the investigation.</span></span> <span data-ttu-id="ccd19-114">입력을 시작 하 여 조직의 Azure Active Directory에서 사용자를 검색 하 고 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-114">You can start by typing to search and select the users from your organization's Azure Active Directory.</span></span>
 
4. <span data-ttu-id="ccd19-115">관심 있는 사용자 목록을 완성 한 후에는 **다음** 을 클릭 하 여 해당 데이터 원본을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-115">After you have finalized the list of people of interest, click **Next** to map their data sources.</span></span> 

5. <span data-ttu-id="ccd19-116">반드시 각 사용자에 대해 **Exchange** 를 선택 하 여 사용자의 기본 Exchange 사서함을 추가 하 고 **onedrive** 에서 사용자의 기본 비즈니스용 onedrive 사이트를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-116">[Optional] For each person, select **Exchange** to add person's primary Exchange mailbox, and **OneDrive** to add person's primary OneDrive for Business site.</span></span>

6. <span data-ttu-id="ccd19-117">반드시 **다음** 을 클릭 하 여 원하는 사용자와 연결할 추가 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-117">[Optional] Click **Next** to add any additional data sources that you want to associate with your people of interest.</span></span>

7. <span data-ttu-id="ccd19-118">반드시 사용자에 게 사서함, 사이트 및 팀과 같은 콘텐츠 위치를 할당 하려면 **업데이트** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-118">[Optional] Select **Update** to assign content locations, like mailboxes, sites, and Teams to a person.</span></span> 

8. <span data-ttu-id="ccd19-119">반드시 플라이 아웃:</span><span class="sxs-lookup"><span data-stu-id="ccd19-119">[Optional] In the flyout:</span></span>
   
    -  <span data-ttu-id="ccd19-120">**Exchange 사서함** - **사용자, 그룹 또는 팀 선택을** 클릭 한 다음 **사용자, 그룹 또는 팀** 선택을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-120">**Exchange Mailboxes** - Click **Choose users, groups, or Teams** and then click **Choose users, groups, or teams** again.</span></span> <span data-ttu-id="ccd19-121">더 많은 사서함을 추가 하려면 검색 상자를 사용 하 여 사용자 사서함과 메일 그룹을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-121">To add more mailboxes, use the search box to find user mailboxes and distribution groups.</span></span> <span data-ttu-id="ccd19-122">또한 Office 365 그룹 또는 Microsoft 팀 정보를 저장 하는 데 사용 되는 사서함을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-122">You can also add mailboxes used to store an Office 365 Group or a Microsoft Team information.</span></span> <span data-ttu-id="ccd19-123">사용자, 그룹, 팀 확인란을 선택 하 고 **선택을**클릭 한 후 **완료**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-123">Select the user, group, team check box, click **Choose**, and then click **Done**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ccd19-124">사용자, 그룹 또는 팀 선택을 클릭 하 여 사서함을 지정 하는 경우 표시 되는 사서함 선택은 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-124">When you click Choose users, groups, or teams to specify mailboxes, the mailbox picker that's displayed is empty.</span></span> <span data-ttu-id="ccd19-125">이것은 성능을 향상시키기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-125">This is by design to enhance performance.</span></span> <span data-ttu-id="ccd19-126">이 목록에 사용자를 추가 하려면 검색 상자에 이름 (최소 3 자)을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-126">To add people to this list, type a name (a minimum of 3 characters) in the search box.</span></span>
     
     - <span data-ttu-id="ccd19-127">**SharePoint 사이트** - **사이트 선택을** 클릭 한 다음 **사이트 선택을** 클릭 하 여 사용자에 게 추가 하려는 SharePoint 및 비즈니스용 OneDrive 사이트를 추가로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-127">**SharePoint Sites** - Click **Choose sites** and then click **Choose sites** again to specify additional SharePoint and OneDrive for Business sites that you wwant to add to a person.</span></span> <span data-ttu-id="ccd19-128">또한 Office 365 그룹 또는 Microsoft 팀에 대 한 SharePoint 사이트의 URL을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-128">You can also add the URL for the SharePoint site for an Office 365 Group or a Microsoft Team.</span></span> <span data-ttu-id="ccd19-129">할당 하려는 각 사이트의 URL을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-129">Type the URL for each site that you want to assign.</span></span> <span data-ttu-id="ccd19-130">**선택을**클릭 하 고 **완료**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-130">Click **Choose**, and then click **Done**.</span></span>
     - <span data-ttu-id="ccd19-131">**microsoft 팀** - **팀 선택을** 클릭 한 다음 **팀 선택을** 다시 클릭 하 여 해당 사용자가 현재 구성원 인 Microsoft 팀 그룹의 목록을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-131">**Microsoft Teams** – Click **Choose Teams** and then click **Choose Teams** again to view a list of Microsoft Team groups that the person is a member of today.</span></span> <span data-ttu-id="ccd19-132">사용자에 게 추가 하려는 팀을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-132">Select the Teams that you want to add to the person.</span></span> <span data-ttu-id="ccd19-133">선택한 후에는 시스템에서 자동으로 &를 확인 하 여 해당 Microsoft 팀과 연결 된 SharePoint 사이트 및 그룹 사서함을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-133">Once selected, the system will automatically identify & select the associated SharePoint site and Group Mailbox associated to that Microsoft Team.</span></span> <span data-ttu-id="ccd19-134">**선택을**클릭 하 고 **완료**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-134">Click **Choose**, and then click **Done**.</span></span>
        
      > [!NOTE]
      > <span data-ttu-id="ccd19-135">Microsoft 팀을 더 추가 하려면 위에 표시 된 대로 사서함 및 SharePoint 사이트를 별도로 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-135">To add additional Microsoft Teams, you will need to separately add the mailbox and SharePoint site as shown above.</span></span>

<span data-ttu-id="ccd19-136">관심 있는 사용자에 게 데이터 원본을 매핑한 후에는 방금 추가한 전체 사서함, 사이트 및 팀에 대 한 요약 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-136">After you have finished mapping data sources to people of interest, you can see the summary of total mailboxes, sites, and Teams that you just added.</span></span> <span data-ttu-id="ccd19-137">관심 있는 사용자에 게 추가 데이터 원본을 매핑하고 관심 있는 사용자를 기준으로 검색 범위를 결정 하는 경우, 조사 전체에서 해당 사용자에 게 문서를 매핑하면 정보를 보다 쉽게 구성 하거나 관심 있는 사용자 별로 보고서를 생성할 수 있습니다. .</span><span class="sxs-lookup"><span data-stu-id="ccd19-137">If you map any additional data sources to people of interest and scope your search by people of interest, the mapping of document to people of interest persist throughout the investigation, making it easier to organize evidence or generate report by people of interest.</span></span> 

## <a name="view-additional-people-of-interest-information"></a><span data-ttu-id="ccd19-138">자세한 정보를 볼 만한 추가 사용자 보기</span><span class="sxs-lookup"><span data-stu-id="ccd19-138">View additional people of interest information</span></span>

<span data-ttu-id="ccd19-139">**관심 있는 사용자** 탭에서 adeed 하는 사람을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-139">In **People of interest** tab, click on a person that you adeed.</span></span> <span data-ttu-id="ccd19-140">플라이 아웃에서 다음을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-140">In a flyout, you'll see:</span></span>

- <span data-ttu-id="ccd19-141">연락처 정보</span><span class="sxs-lookup"><span data-stu-id="ccd19-141">Contact information</span></span>

  - <span data-ttu-id="ccd19-142">**표시 이름**: 주소록에 표시 되는 peron의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-142">**Display Name**: The peron's name displayed in the address book.</span></span> <span data-ttu-id="ccd19-143">일반적으로 이름, 중간 이니셜 및 성의 조합이 여기에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-143">This is usually the combination of first name, middle initial and last name.</span></span>
  - <span data-ttu-id="ccd19-144">**메일/SMTP**: jeff@contoso.onmicrosoft.com와 같은 사람의 SMTP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-144">**Mail/SMTP**: The SMTP address of the person, for example, jeff@contoso.onmicrosoft.com.</span></span>  
  - <span data-ttu-id="ccd19-145">**제목**: 직함</span><span class="sxs-lookup"><span data-stu-id="ccd19-145">**Title**: Job title.</span></span>
  - <span data-ttu-id="ccd19-146">**부서**: 담당자가 근무 하는 부서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-146">**Department**: The name of the department in which the person works.</span></span>
  - <span data-ttu-id="ccd19-147">**관리자**: 사용자의 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-147">**Manager**: The person's manager.</span></span> <span data-ttu-id="ccd19-148">관리자가이 사용자에 대 한 에스컬레이션 통신을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-148">Manager receives any escalation communications for this person.</span></span>
  
- <span data-ttu-id="ccd19-149">위치 정보</span><span class="sxs-lookup"><span data-stu-id="ccd19-149">Location information</span></span>

  - <span data-ttu-id="ccd19-150">**구/군/** 시: 사용자가 거주 하는 구/군/시입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-150">**City**: The city in which the person is located.</span></span>
  - <span data-ttu-id="ccd19-151">**상태**: 개인이 거주 하는 시/도입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-151">**State**: The state or province in which the person is located.</span></span>
  - <span data-ttu-id="ccd19-152">**국가/지역**: 개인이 거주 하는 국가/지역입니다. 예를 들어 "US" 또는 "영국"을 예로 들 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-152">**Country/Region**: The country/region in which the person is located; for example, “US” or “UK”.</span></span>
  - <span data-ttu-id="ccd19-153">**office**: 사용자의 사무실 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-153">**Office**: The office location of the person.</span></span>

- <span data-ttu-id="ccd19-154">처리 상태</span><span class="sxs-lookup"><span data-stu-id="ccd19-154">Processing status</span></span>

  - <span data-ttu-id="ccd19-155">**인덱싱 상태**: 데이터 원본에 대 한 전체 인덱싱 상태</span><span class="sxs-lookup"><span data-stu-id="ccd19-155">**Indexing status**: Status of deep indexing the data sources</span></span>
  - <span data-ttu-id="ccd19-156">**인덱싱 마지막 업데이트 시간**: 딥 Indexing 작업이 마지막으로 트리거된 시간의 타임 스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-156">**Indexing Last Updated Time**: Timestamp of when the deep indexing job was last triggered.</span></span>
  - <span data-ttu-id="ccd19-157">**데이터 원본**: 사용자에 게 매핑된 사서함, 사이트 및 팀의 수를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-157">**Data sources**: Shows the count of mailboxes, sites, and Teams mapped to the person</span></span>

- <span data-ttu-id="ccd19-158">인덱스 업데이트</span><span class="sxs-lookup"><span data-stu-id="ccd19-158">Update index</span></span>
    - <span data-ttu-id="ccd19-159">이 사용자의 데이터 원본을 다시 인덱싱할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-159">You can re-index this person's data sources.</span></span> 

- <span data-ttu-id="ccd19-160">활동 보기</span><span class="sxs-lookup"><span data-stu-id="ccd19-160">View activity</span></span> 

    - <span data-ttu-id="ccd19-161">사용자의 활동 로그를 보고 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd19-161">You can view and search user's activity logs.</span></span> <span data-ttu-id="ccd19-162">자세한 내용은 [관심 있는 사용자 활동 보기](view-people-of-interest-activity.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ccd19-162">For more information, see [View people of interest activity](view-people-of-interest-activity.md)</span></span> 
