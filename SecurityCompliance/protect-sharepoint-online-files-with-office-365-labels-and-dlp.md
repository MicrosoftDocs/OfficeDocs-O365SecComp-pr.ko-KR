---
title: 보존 레이블 및 DLP를 사용하여 SharePoint Online 파일 보호
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/29/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: c9f837af-8d71-4df1-a285-dedb1c5618b3
description: '요약: 다양한 정보 보호 수준을 통해 SharePoint Online 팀 사이트에 보존 레이블 및 DLP(데이터 손실 방지) 정책을 적용합니다.'
ms.openlocfilehash: 81173e96ce6e67ee3b513abce4424686abe79e02
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261670"
---
# <a name="protect-sharepoint-online-files-with-retention-labels-and-dlp"></a><span data-ttu-id="f7ae3-103">보존 레이블 및 DLP를 사용하여 SharePoint Online 파일 보호</span><span class="sxs-lookup"><span data-stu-id="f7ae3-103">Protect SharePoint Online files with retention labels and DLP</span></span>

 <span data-ttu-id="f7ae3-104">**요약:** 다양한 정보 보호 수준을 통해 SharePoint Online 팀 사이트에 보존 레이블 및 DLP(데이터 손실 방지) 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-104">**Summary:** Apply retention labels and data loss prevention (DLP) policies for SharePoint Online team sites with various levels of information protection.</span></span>
  
<span data-ttu-id="f7ae3-105">이 문서의 단계를 사용하여 초기, 중요 및 극비 SharePoint Online 팀 사이트에 대한 레이블 및 DLP 정책을 디자인하고 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-105">Use the steps in this article to design and deploy retention labels and DLP policies for baseline, sensitive, and highly confidential SharePoint Online team sites.</span></span> <span data-ttu-id="f7ae3-106">이러한 3계층 보호에 대한 자세한 내용은 [SharePoint Online 사이트 및 파일 보호](secure-sharepoint-online-sites-and-files.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-106">For more information about these three tiers of protection, see [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md).</span></span>
  
## <a name="how-this-works"></a><span data-ttu-id="f7ae3-107">작동 방식</span><span class="sxs-lookup"><span data-stu-id="f7ae3-107">How this works</span></span>
1. <span data-ttu-id="f7ae3-108">원하는 보존 레이블을 만들고 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-108">Create the desired retention labels and publish these.</span></span> <span data-ttu-id="f7ae3-109">게시하는데 최대 12시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-109">It can take up to 12 hours for these to be published.</span></span>
2. <span data-ttu-id="f7ae3-110">원하는 SharePoint 사이트에서 문서 라이브러리 설정을 편집하여 원하는 보존 레이블을 라이브러리의 항목에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-110">For the desired SharePoint sites, edit the document library settings to apply the desired retention labels to items in the library.</span></span>
3. <span data-ttu-id="f7ae3-111">보존 레이블을 기반으로 작업을 수행하는 DLP 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-111">Create DLP policies to take action based on the retention labels.</span></span>

<span data-ttu-id="f7ae3-112">사용자가 라이브러리에 문서를 추가하면 기본적으로 문서에 할당된 보존 레이블이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-112">When users add a document to the library, the document will receive the assigned retention label by default.</span></span> <span data-ttu-id="f7ae3-113">사용자는 필요한 경우 레이블을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-113">Users can change the label, if needed.</span></span> <span data-ttu-id="f7ae3-114">사용자가 조직 외부에 문서를 공유하면 DLP는 레이블이 할당되었는지 확인하고 DLP 정책이 레이블과 일치하면 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-114">When a user shares a document outside the organization, DLP will check to see if a label is assigned and take action if a DLP policy matches the label.</span></span> <span data-ttu-id="f7ae3-115">DLP는 이러한 유형의 정책이 구성되어 있는 경우 신용 카드 번호로 파일을 보호하는 것과 같은 다른 정책 일치도 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-115">DLP will look for other policy matches as well, such as protecting files with credit card numbers if this type of policy is configured.</span></span> 

## <a name="retention-labels-for-your-sharepoint-online-sites"></a><span data-ttu-id="f7ae3-116">SharePoint Online 사이트에 대한 보존 레이블</span><span class="sxs-lookup"><span data-stu-id="f7ae3-116">Retention labels for your SharePoint Online sites</span></span>

<span data-ttu-id="f7ae3-117">SharePoint Online 팀 사이트에 보존 레이블을 만들고 할당하는 경우 다음 세 가지 단계를 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-117">There are three phases to creating and then assigning retention labels to SharePoint Online team sites.</span></span>
  
### <a name="phase-1-determine-the-retention-label-names"></a><span data-ttu-id="f7ae3-118">1단계: 보존 레이블 이름 결정</span><span class="sxs-lookup"><span data-stu-id="f7ae3-118">Phase 1: Determine the retention label names</span></span>

<span data-ttu-id="f7ae3-119">이 단계에서는 SharePoint Online 팀 사이트에 적용되는 네 가지 정보 보호 수준에 대한 보존 레이블의 이름을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-119">In this phase, you determine the names of your retention labels for the four levels of information protection applied to SharePoint Online team sites.</span></span> <span data-ttu-id="f7ae3-120">다음 표에는 각 수준에 권장되는 이름이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-120">The following table lists the recommended names for each level.</span></span>
  
|<span data-ttu-id="f7ae3-121">**SharePoint Online 팀 사이트 보호 수준**</span><span class="sxs-lookup"><span data-stu-id="f7ae3-121">**SharePoint Online team site protection level**</span></span>|<span data-ttu-id="f7ae3-122">**레이블 이름**</span><span class="sxs-lookup"><span data-stu-id="f7ae3-122">**Label name**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f7ae3-123">초기 공용</span><span class="sxs-lookup"><span data-stu-id="f7ae3-123">Baseline-Public</span></span>  <br/> |<span data-ttu-id="f7ae3-124">내부 공용</span><span class="sxs-lookup"><span data-stu-id="f7ae3-124">Internal public</span></span>  <br/> |
|<span data-ttu-id="f7ae3-125">초기 개인</span><span class="sxs-lookup"><span data-stu-id="f7ae3-125">Baseline-Private</span></span>  <br/> |<span data-ttu-id="f7ae3-126">개인</span><span class="sxs-lookup"><span data-stu-id="f7ae3-126">Private</span></span>  <br/> |
|<span data-ttu-id="f7ae3-127">중요</span><span class="sxs-lookup"><span data-stu-id="f7ae3-127">Sensitive</span></span>  <br/> |<span data-ttu-id="f7ae3-128">중요</span><span class="sxs-lookup"><span data-stu-id="f7ae3-128">Sensitive</span></span>  <br/> |
|<span data-ttu-id="f7ae3-129">극비</span><span class="sxs-lookup"><span data-stu-id="f7ae3-129">Highly Confidential</span></span>  <br/> |<span data-ttu-id="f7ae3-130">극비</span><span class="sxs-lookup"><span data-stu-id="f7ae3-130">Highly Confidential</span></span>  <br/> |
   
### <a name="phase-2-create-the-retention-labels"></a><span data-ttu-id="f7ae3-131">2 단계: 보존 레이블 만들기</span><span class="sxs-lookup"><span data-stu-id="f7ae3-131">Phase 2: Create the retention labels</span></span>

<span data-ttu-id="f7ae3-132">이 단계에서는 서로 다른 수준의 정보 보호를 위해 결정한 레이블을 만들어 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-132">In this phase, you create and then publish your determined labels for the different levels of information protection.</span></span>
  
1. <span data-ttu-id="f7ae3-133">보안 관리자 또는 회사 관리자 역할이 있는 계정으로 [Microsoft 365 규정 준수 포털](https://compliance.microsoft.com)에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-133">Sign in to the [Microsoft 365 compliance portal](https://compliance.microsoft.com) with an account that has the Security Administrator or Company Administrator role.</span></span>
    
2. <span data-ttu-id="f7ae3-134">브라우저의 **홈 - Microsoft 365 규정 준수** 탭에서 **분류 > 레이블**을 차례로 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-134">From the **Home - Microsoft 365 Security** tab of your browser, click **Classifications > Labels**.</span></span>
    
3. <span data-ttu-id="f7ae3-135">**보존 레이블 > 레이블 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-135">Click **Retention labels > Create a label**.</span></span>
    
4. <span data-ttu-id="f7ae3-136">**레이블 명칭 만들기** 창에서 레이블 이름과 관리자 및 사용자에 대한 설명을 입력하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-136">On the **Name your label** pane, type the name of the label and a description for admins and users, and then click **Next**.</span></span>

5. <span data-ttu-id="f7ae3-137">**파일 계획 설명자** 창에서 필요에 따라 작성한 다음, **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-137">On the **File plan descriptors** pane, fill in as needed, and then click **Next**.</span></span>
    
6. <span data-ttu-id="f7ae3-138">필요에 따라 **레이블 설정** 창에서 **보존**을 **켜기**로 설정하고 보존 설정을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-138">On the **Label settings** pane, if needed, set **Retention** to **On** and configure retention settings.</span></span> <span data-ttu-id="f7ae3-139">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-139">Click **Next**.</span></span>
    
7. <span data-ttu-id="f7ae3-140">**설정 검토** 창에서 **레이블 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-140">On the **Review your settings** pane, click **Create the label**.</span></span>
    
8. <span data-ttu-id="f7ae3-141">추가 레이블의 경우 **레이블 만들기**를 클릭한 다음, 필요에 따라 3~7단계를 반복합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-141">For your additional labels, click **Create a label**, and then repeat steps 4-7..</span></span>
    

### <a name="publish-your-new-labels"></a><span data-ttu-id="f7ae3-142">새 레이블을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-142">Publish your new labels</span></span>

<span data-ttu-id="f7ae3-143">그리고 나서 다음의 단계를 사용하여 새 보존 레이블을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-143">Next, use these steps to publish the new retention labels.</span></span>
  
1. <span data-ttu-id="f7ae3-144">**레이블** 창에서 **레이블 보존**탭을 클릭한 다음 **레이블 게시**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-144">From the **Labels** pane, click the **Retention labels** tab, and then click **Publish labels**.</span></span>
    
2. <span data-ttu-id="f7ae3-145">**게시할 레이블 선택** 창에서 **게시할 레이블 선택**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-145">On the **Choose labels to publish** pane, click **Choose labels to publish**.</span></span>
    
3. <span data-ttu-id="f7ae3-146">**레이블 선택** 창에서 **추가**를 클릭하고 네 개의 레이블을 모두 선택하고 **추가**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-146">On the **Choose labels** pane, click **Add**, select all four labels, click **Add**.</span></span>
    
4. <span data-ttu-id="f7ae3-147">**완료**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-147">Click **Done**.</span></span>
    
5. <span data-ttu-id="f7ae3-148">**게시할 레이블 선택** 창에서 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-148">On the **Choose labels to publish** pane, click **Next**.</span></span>
    
6. <span data-ttu-id="f7ae3-149">**위치 선택** 창에서 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-149">On the **Choose locations** pane, click **Next**.</span></span>
    
7. <span data-ttu-id="f7ae3-150">**정책 이름 지정** 창의 **이름**에서 레이블 집합 이름을 입력하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-150">On the **Name your policy** pane, type a name for your set of labels in **Name**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="f7ae3-151">**설정 검토** 창에서 **레이블 게시**, **닫기**를 차례로 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-151">On the **Review your settings** pane, click **Publish labels**, and then click **Close**.</span></span>

    
### <a name="phase-3-apply-the-retention-labels-to-your-sharepoint-online-sites"></a><span data-ttu-id="f7ae3-152">3단계: SharePoint Online 사이트에 보존 레이블 적용하기</span><span class="sxs-lookup"><span data-stu-id="f7ae3-152">Phase 3: Apply the retention labels to your SharePoint Online sites</span></span>

<span data-ttu-id="f7ae3-153">다음 단계에 따라 보존 레이블을 SharePoint Online 팀 사이트의 문서 폴더에 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-153">Use these steps to apply the retention labels to the documents folders of your SharePoint Online team sites.</span></span>
  
1. <span data-ttu-id="f7ae3-154">[Office 365 포털](https://www.office.com)에 로그인하고 **SharePoint** 앱을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-154">Sign in to the [Office 365 portal](https://www.office.com), click the **SharePoint** app.</span></span>
    
2. <span data-ttu-id="f7ae3-155">브라우저의 새 **SharePoint** 탭에서 할당된 보존 레이블이 필요한 사이트를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-155">On the new **SharePoint** tab in your browser, click a site that needs a retention label assigned.</span></span>
    
3. <span data-ttu-id="f7ae3-156">브라우저의 새 SharePoint 사이트 탭에서 **문서**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-156">In the new SharePoint site tab of your browser, click **Documents**.</span></span>
    
4. <span data-ttu-id="f7ae3-157">설정 아이콘을 클릭한 다음 **라이브러리 설정**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-157">Click the settings icon, and then click **Library settings**.</span></span>
    
5. <span data-ttu-id="f7ae3-158">**권한 및 관리** 아래에서 **이 라이브러리의 항목에 레이블 적용**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-158">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
6. <span data-ttu-id="f7ae3-159">**설정 - 레이블 적용**에서 적절한 레이블을 선택하고 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-159">In **Settings-Apply Label**, select the appropriate retention label, and then click **Save**.</span></span>
    
7. <span data-ttu-id="f7ae3-160">SharePoint Online 사이트의 탭을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-160">Close the tab for the SharePoint Online site.</span></span>
    
8. <span data-ttu-id="f7ae3-161">2-8단계를 반복하여 추가 SharePoint Online 사이트에 보존 레이블을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-161">Repeat steps 2-8 to assign retention labels to your additional SharePoint Online sites.</span></span>
    
<span data-ttu-id="f7ae3-162">구성 결과는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-162">Here is your resulting configuration.</span></span>
  
![SharePoint Online 팀 사이트의 네 가지 유형에 대한 보존 레이블입니다.](media/e0a4fdd2-1c30-4d93-8af4-a6f0c6c29966.png)
  
## <a name="dlp-policies-for-your-sharepoint-online-sites"></a><span data-ttu-id="f7ae3-164">SharePoint Online 사이트에 대한 DLP 정책</span><span class="sxs-lookup"><span data-stu-id="f7ae3-164">DLP policies for your SharePoint Online sites</span></span>

<span data-ttu-id="f7ae3-165">다음 단계를 사용하여 사용자가 조직 외부의 중요 SharePoint Online 팀 사이트에서 문서를 공유할 때 다른 사용자에게 알려주는 DLP 정책을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-165">Use these steps to configure a DLP policy that notifies users when they share a document on a SharePoint Online sensitive team site outside the organization.</span></span>

1. <span data-ttu-id="f7ae3-166">보안 관리자 또는 회사 관리자 역할이 있는 계정으로 [Microsoft 365 규정 준수 포털](https://compliance.microsoft.com/)에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-166">Sign in to the [Microsoft 365 compliance portal](https://compliance.microsoft.com/) with an account that has the Security Administrator or Company Administrator role.</span></span>
    
2. <span data-ttu-id="f7ae3-167">브라우저의 새 **Microsoft 365 규정 준수** 탭에서 **정책 > 데이터 손실 방지**를 차례로 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-167">On the new **Microsoft 365 compliance** tab in your browser, click **Policies > Data loss prevention**.</span></span>
    
3. <span data-ttu-id="f7ae3-168">**홈 > 데이터 손실 방지** 창에서 **정책 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-168">In the **Home > Data loss prevention** pane, click **Create a policy**.</span></span>
    
4. <span data-ttu-id="f7ae3-169">**서식 파일로 시작하거나 사용자 지정 정책 만들기** 창에서 **사용자 지정**, **다음**을 차례로 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-169">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="f7ae3-170">**정책 이름 지정** 창의 **이름**에서 중요 수준 DLP 정책의 이름을 입력하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-170">In the **Name your policy** pane, type the name for the sensitive level DLP policy in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="f7ae3-171">**위치 선택** 창에서 **특정 위치 선택 허용**을 선택하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-171">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="f7ae3-172">위치 목록에서 **Exchange 전자 메일**, **OneDrive 계정** 및 **팀 채팅 및 채널 메시지** 를 사용하지 않도록 설정하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-172">In the list of locations, disable the **Exchange email**, **OneDrive accounts**, and **Teams chat and channel messages** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="f7ae3-173">**보호할 콘텐츠 유형 사용자 지정** 창에서 **편집**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-173">In the **Customize the type of content you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="f7ae3-174">**보호할 콘텐츠 유형 선택** 창의 드롭다운 상자에서 **추가**, **보존 레이블**을 차례로 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-174">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Retention labels**.</span></span>
    
10. <span data-ttu-id="f7ae3-175">**보존 레이블** 창에서 **+추가**를 클릭하고, **중요** 레이블을 선택하고, **추가**를 클릭한 다음, **완료**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-175">In the **Retention labels** pane, click **Add**, select the **Sensitive** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="f7ae3-176">**보호할 콘텐츠 유형 선택** 창에서 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-176">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="f7ae3-177">**보호할 콘텐츠 유형 사용자 지정** 창에서 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-177">In the **Customize the type of content you want to protect** pane, click **Next**.</span></span>

13. <span data-ttu-id="f7ae3-178">\*\*중요한 정보를 발견하면 \*\* 창에서 **팁 및 전자 메일 사용자 지정**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-178">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="f7ae3-179">**정책 팁 및 전자 메일 알림 사용자 지정** 창에서 **정책 팁 텍스트 사용자 지정**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-179">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="f7ae3-180">Azure Information Protection에서 극비 파일을 보호하도록 구현했는지에 따라 텍스트 상자에 다음 팁 중 하나를 입력하거나 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-180">In the text box, type or paste in one of the following tips, depending on if you implemented Azure Information Protection to protect highly confidential files:</span></span>
    
  - <span data-ttu-id="f7ae3-p106">조직 외부의 사용자와 공유하려면 파일을 다운로드한 다음 파일을 엽니다. 파일, 문서 보호, 암호 설정을 차례로 클릭한 다음 강력한 암호를 지정합니다. 암호를 별도의 전자 메일 또는 다른 통신 수단으로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-p106">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
  - <span data-ttu-id="f7ae3-p107">극비 파일은 암호화를 통해 보호됩니다. IT 부서에서 사용 권한을 부여받은 외부 사용자만 극비 파일을 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-p107">Highly confidential files are protected with encryption. Only external users who are granted permissions to these files by your IT department can read them.</span></span>
    
    <span data-ttu-id="f7ae3-186">또는 조직 외부에 파일을 공유하는 방법을 사용자에게 지시하는 사용자 고유의 정책 팁을 입력하거나 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-186">Alternately, type or paste in your own policy tip that instructs users on how to share a file outside your organization.</span></span>
    
16. <span data-ttu-id="f7ae3-187">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-187">Click **OK**.</span></span>
    
17. <span data-ttu-id="f7ae3-188">**중요한 정보를 발견 시 어떠한 작업을 수행하시겠습니까?** 창에서 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-188">In the **What do you want to do if we detect sensitive info?** pane, click **Next**.</span></span>
    
18. <span data-ttu-id="f7ae3-189">**정책을 켤까요 아니면 먼저 테스트를 수행할까요?** 창에서 **예, 지금 켜겠습니다.** 를 클릭하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-189">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="f7ae3-190">**설정 검토 창**에서 **만들기**, **닫기**를 차례로 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-190">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
<span data-ttu-id="f7ae3-191">결과적으로 중요 SharePoint Online 팀 사이트에 대한 구성은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-191">Here is your resulting configuration for sensitive SharePoint Online team sites.</span></span>
  
![중요한 보존 레이블을 사용하는 격리된 SharePoint Online 팀 사이트의 DLP 정책입니다.](media/2ff4cc53-87a8-43e3-b637-3068d88409f3.png)
  
<span data-ttu-id="f7ae3-193">그리고 나서 다음 단계를 사용하여 사용자가 조직 외부의 극비 SharePoint Online 팀 사이트에서 문서를 공유할 때 다른 사용자를 차단하는 DLP 정책을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-193">Next, use these steps to configure a DLP policy that blocks users when they share a document on a SharePoint Online highly confidential team site outside the organization.</span></span>
  
1. <span data-ttu-id="f7ae3-194">브라우저의 새 **Microsoft 365 규정 준수** 탭에서 **정책 > 데이터 손실 방지**를 차례로 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-194">On the new **Microsoft 365 compliance** tab in your browser, click **Policies > Data loss prevention**.</span></span>
    
2. <span data-ttu-id="f7ae3-195">**데이터 손실 방지** 창에서 **정책 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-195">In the **Data loss prevention** pane, click **Create a policy**.</span></span>
    
3. <span data-ttu-id="f7ae3-196">**서식 파일로 시작하거나 사용자 지정 정책 만들기** 창에서 **사용자 지정**, **다음**을 차례로 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-196">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="f7ae3-197">**정책 이름 지정** 창의 **이름**에서 이름에 극비 수준 DLP 정책의 이름을 입력하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-197">In the **Name your policy** pane, type the name for the highly sensitive level DLP policy in **Name**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="f7ae3-198">**위치 선택** 창에서 **특정 위치 선택 허용**을 선택하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-198">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="f7ae3-199">위치 목록에서 **Exchange 전자 메일**, **OneDrive 계정** 및 **팀 채팅 및 채널 메시지** 를 사용하지 않도록 설정하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-199">In the list of locations, disable the **Exchange email**, **OneDrive accounts**, and **Teams chat and channel messages** locations, and then click **Next**.</span></span>
    
7. <span data-ttu-id="f7ae3-200">**보호할 중요 정보의 유형 사용자 지정** 창에서 **편집**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-200">In the **Customize the types of sensitive info you want to protect** pane, click **Edit**.</span></span>
    
8. <span data-ttu-id="f7ae3-201">**보호할 콘텐츠 유형 선택** 창의 드롭다운 상자에서 **추가**, **보존 레이블**을 차례로 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-201">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Retention labels**.</span></span>
    
9. <span data-ttu-id="f7ae3-202">**레이블** 창에서 **추가**를 클릭하고, **극비** 레이블을 선택하고, **추가**를 클릭한 다음, **완료**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-202">In the **Retention labels** pane, click **Add**, select the **Highly Confidential** label, click **Add**, and then click **Done**.</span></span>
    
10. <span data-ttu-id="f7ae3-203">**보호할 콘텐츠 유형 선택** 창에서 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-203">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="f7ae3-204">**Customize the types of sensitive info you want to protect(보호할 중요 정보 유형 사용자 지정)** 창에서 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-204">In the **Customize the types of sensitive info you want to protect** pane, click **Next**.</span></span>
    
13. <span data-ttu-id="f7ae3-205">\*\*중요한 정보를 발견하면 \*\* 창에서 **팁 및 전자 메일 사용자 지정**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-205">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="f7ae3-206">**Customize policy tips and email notifications(정책 팁 및 전자 메일 알림 사용자 지정)** 창에서 **Customize the policy tip text(정책 팁 텍스트 사용자 지정)** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-206">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="f7ae3-207">텍스트 상자에 다음을 입력하거나 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-207">In the text box, type or paste in the following:</span></span>
    
  - <span data-ttu-id="f7ae3-p108">조직 외부의 사용자와 공유하려면 파일을 다운로드한 다음 파일을 엽니다. 파일, 문서 보호, 암호 설정을 차례로 클릭한 다음 강력한 암호를 지정합니다. 암호를 별도의 전자 메일 또는 다른 통신 수단으로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-p108">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
    
    <span data-ttu-id="f7ae3-211">또는 조직 외부의 파일을 공유하는 방법을 사용자에게 지시하는 사용자 고유의 정책 팁을 입력하거나 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-211">Alternately, type or paste in your own policy tip that instructs users on how to share a file outside your organization.</span></span>
    
16. <span data-ttu-id="f7ae3-212">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-212">Click **OK**.</span></span>
    
17. <span data-ttu-id="f7ae3-213">**중요한 정보를 발견 시 어떠한 작업을 수행하시겠습니까?** 창에서 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-213">In the **What do you want to do if we detect sensitive info?** pane, click **Next**.</span></span>
    
18. <span data-ttu-id="f7ae3-214">**정책을 켤까요 아니면 먼저 테스트를 수행할까요?** 창에서 **예, 지금 켜겠습니다.** 를 클릭하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-214">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="f7ae3-215">**설정 검토 창**에서 **만들기**, **닫기**를 차례로 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-215">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
<span data-ttu-id="f7ae3-216">결과적으로 극비 SharePoint Online 팀 사이트에 대한 구성은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-216">Here is your resulting configuration for high confidentiality SharePoint Online team sites.</span></span>
  
![높은 수준의 기밀 보존 레이블을 사용하는 격리된 SharePoint Online 팀 사이트의 DLP 정책입니다.](media/f705d3d0-23c9-4333-8b70-ad3b91f835ea.png)
  
## <a name="next-step"></a><span data-ttu-id="f7ae3-218">다음 단계</span><span class="sxs-lookup"><span data-stu-id="f7ae3-218">Next step</span></span>

[<span data-ttu-id="f7ae3-219">Azure Information Protection을 사용한 SharePoint Online 파일 보호</span><span class="sxs-lookup"><span data-stu-id="f7ae3-219">Protect SharePoint Online files with Azure Information Protection</span></span>](protect-sharepoint-online-files-with-azure-information-protection.md)
    
## <a name="see-also"></a><span data-ttu-id="f7ae3-220">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f7ae3-220">See Also</span></span>

[<span data-ttu-id="f7ae3-221">SharePoint Online 사이트 및 파일 보호</span><span class="sxs-lookup"><span data-stu-id="f7ae3-221">Secure SharePoint Online sites and files</span></span>](secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="f7ae3-222">정치적 캠페인, 비영리 조직 및 기타 기밀 조직을 위한 Microsoft 보안 지침</span><span class="sxs-lookup"><span data-stu-id="f7ae3-222">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="f7ae3-223">클라우드 도입 및 하이브리드 솔루션</span><span class="sxs-lookup"><span data-stu-id="f7ae3-223">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)


