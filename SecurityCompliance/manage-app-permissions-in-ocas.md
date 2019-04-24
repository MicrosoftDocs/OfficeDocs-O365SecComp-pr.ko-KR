---
title: Office 365 Cloud App Security를 사용하여 OAuth 앱 관리
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: office 365의 OAuth 앱-Cloud App Security는 사용자가 Office 365 데이터와 함께 사용할 수 있도록 다운로드 하는 앱을 관리 하는 데 도움이 됩니다.
ms.openlocfilehash: 0d9916414d55abb73fd99eaf30c3b6df0648b191
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260204"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a><span data-ttu-id="efde8-103">Office 365 Cloud App Security를 사용하여 OAuth 앱 관리</span><span class="sxs-lookup"><span data-stu-id="efde8-103">Manage OAuth apps using Office 365 Cloud App Security</span></span>

|<span data-ttu-id="efde8-104">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="efde8-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="efde8-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="efde8-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="efde8-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="efde8-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="efde8-107">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="efde8-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="efde8-108">평가 시작</span><span class="sxs-lookup"><span data-stu-id="efde8-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="efde8-109">계획 시작</span><span class="sxs-lookup"><span data-stu-id="efde8-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="efde8-110">배포 시작</span><span class="sxs-lookup"><span data-stu-id="efde8-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="efde8-111">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="efde8-111">You are here!</span></span>  <br/> [<span data-ttu-id="efde8-112">다음 단계</span><span class="sxs-lookup"><span data-stu-id="efde8-112">Next steps</span></span>](#next-steps)<br/> |
   
<span data-ttu-id="efde8-113">사용자가 자주 사용 하는 앱을 선호 하며, 특히 회사 또는 학교 정보를 쉽게 확인할 수 있도록 하 여 시간을 절약 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-113">People love apps and they download them often, especially apps that people think will save time by making it easier to get at their work or school information.</span></span> <span data-ttu-id="efde8-114">그러나 일부 앱은 액세스 하는 정보 및 해당 정보를 처리 하는 방법에 따라 조직에 보안 위험이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-114">However, some apps could potentially be a security risk to your organization, depending on what information they access and how they handle that information.</span></span> <span data-ttu-id="efde8-115">[Office 365 Cloud App Security](office-365-cas-overview.md)를 사용 하 여 전역 또는 보안 관리자 인 경우 조직에 대 한 OAuth 앱을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-115">With [Office 365 Cloud App Security](office-365-cas-overview.md), if you are a global or security administrator, you can manage OAuth apps for your organization.</span></span> <span data-ttu-id="efde8-116">사용자가 Office 365 데이터와 함께 사용 하는 앱, 해당 앱에 포함 된 사용 권한 등을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-116">You can see the apps people are using with Office 365 data, what permissions those apps have, and more.</span></span> 
  
<span data-ttu-id="efde8-117">이 문서에서는 OAuth 앱 관리, 앱 승인, 금지 또는 보고 방법, 앱 쿼리를 만드는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-117">This article describes where to go to manage OAuth apps, how to approve, ban, or report an app, and how to create an app query.</span></span>
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a><span data-ttu-id="efde8-118">OAuth 앱 관리 페이지를 찾는 방법</span><span class="sxs-lookup"><span data-stu-id="efde8-118">How to find the Manage OAuth apps page</span></span>

> [!NOTE]
> <span data-ttu-id="efde8-119">OAuth 앱은 Office 365 Cloud App Security 포털에서 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-119">OAuth apps are managed in the Office 365 Cloud App Security portal.</span></span> <span data-ttu-id="efde8-120">다음 작업을 수행 하려면 전역 관리자 이거나 보안 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-120">You must be a global administrator or security administrator to perform the following task.</span></span> <span data-ttu-id="efde8-121">자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="efde8-121">To learn more see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
1. <span data-ttu-id="efde8-122">Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-122">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="efde8-123">**OAuth 앱** **조사** \> 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-123">Choose **Investigate** \> **OAuth apps**.</span></span><br/><span data-ttu-id="efde8-124">![O365 CAS 포털에서 조사를 선택 합니다.](media/OCAS-OAuthApps.png)</span><span class="sxs-lookup"><span data-stu-id="efde8-124">![In the O365 CAS portal, choose Investigate.](media/OCAS-OAuthApps.png)</span></span><br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a><span data-ttu-id="efde8-125">OAuth 앱 관리 페이지에 표시 되는 항목</span><span class="sxs-lookup"><span data-stu-id="efde8-125">What you'll see on the Manage OAuth apps page</span></span>

<span data-ttu-id="efde8-126">다음 표에서는 OAuth 앱 관리 페이지에서 사용할 수 있는 컨트롤 및 옵션에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-126">The following table describes the controls and options available on the Manage OAuth apps page.</span></span>
  
|<span data-ttu-id="efde8-127">**항목**</span><span class="sxs-lookup"><span data-stu-id="efde8-127">**Item**</span></span>|<span data-ttu-id="efde8-128">**설명**</span><span class="sxs-lookup"><span data-stu-id="efde8-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="efde8-129">앱 쿼리 표시줄의 기본 아이콘</span><span class="sxs-lookup"><span data-stu-id="efde8-129">Basic icon in the app query bar</span></span>  <br/> ![쿼리에 대 한 기본 쿼리 보기를 나타내는 아이콘](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|<span data-ttu-id="efde8-131">고급 보기로 전환 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-131">Select this to switch to the Advanced view.</span></span>  <br/> <span data-ttu-id="efde8-132">( **기본**을 참조 하는 경우 고급 보기를 사용 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="efde8-132">(If you see **Basic**, you are using the Advanced view)</span></span>  <br/> |
|<span data-ttu-id="efde8-133">앱 쿼리 모음의 고급 아이콘</span><span class="sxs-lookup"><span data-stu-id="efde8-133">Advanced icon in the app query bar</span></span>  <br/> ![쿼리에 대 한 고급 쿼리 보기를 나타내는 아이콘](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|<span data-ttu-id="efde8-135">기본 보기로 전환 하려면이를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-135">Select this to switch to the Basic view.</span></span>  <br/> <span data-ttu-id="efde8-136">**고급**을 표시 하는 경우 기본 보기를 사용 하 고 있는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-136">(If you see **Advanced**, you are using the Basic view.)</span></span>  <br/> |
|<span data-ttu-id="efde8-137">앱 목록에서 모든 세부 정보 아이콘 열기 또는 닫기</span><span class="sxs-lookup"><span data-stu-id="efde8-137">Open or close all details icon in the app list</span></span>  <br/> ![모든 앱에 대 한 모든 세부 정보를 열거나 닫으려면이 아이콘을 클릭 합니다.](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|<span data-ttu-id="efde8-139">각 앱에 대 한 세부 정보를 자세히 보거나 줄이려면이 아이콘을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-139">Select this icon to view more or fewer details about each app.</span></span>  <br/> |
|<span data-ttu-id="efde8-140">앱 목록의 내보내기 아이콘</span><span class="sxs-lookup"><span data-stu-id="efde8-140">Export icon in the app list</span></span>  <br/> ![모든 앱의 csv 파일을 내보내려면이 아이콘을 클릭 합니다.](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|<span data-ttu-id="efde8-142">앱 목록, 각 앱에 대 한 사용자 수, 앱, 사용 권한 수준, 앱 상태 및 커뮤니티 사용 수준에 연결 된 사용 권한을 포함 하는 CSV 파일을 내보내려면이 아이콘을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-142">Select this icon to export a CSV file that contains a list of apps, number of users for each app, permissions associated with the app, permissions level, app state, and community use level.</span></span>  <br/> |
|<span data-ttu-id="efde8-143">이름</span><span class="sxs-lookup"><span data-stu-id="efde8-143">Name</span></span>  <br/> |<span data-ttu-id="efde8-144">이를 사용 하 여 앱의 이름을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-144">Use this to see the name of an app.</span></span> <span data-ttu-id="efde8-145">설명, 게시자, 앱 웹 사이트 및 앱 ID와 같은 추가 정보를 보려면 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-145">Select the name to view more information, such as its description, publisher, app website and app ID.</span></span>  <br/> |
|<span data-ttu-id="efde8-146">권한 부여 기준</span><span class="sxs-lookup"><span data-stu-id="efde8-146">Authorized by</span></span>  <br/> |<span data-ttu-id="efde8-147">이 방법을 사용 하 여 Office 365 계정에 액세스 하기 위해 앱이 인증 된 사용자의 수를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-147">Use this to see how many users have authorized an app to access their Office 365 account.</span></span> <span data-ttu-id="efde8-148">사용자 계정 목록과 같은 자세한 정보를 보려면 번호를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-148">Select the number to view more information, such as a list of user accounts.</span></span>  <br/> |
|<span data-ttu-id="efde8-149">사용 권한 수준</span><span class="sxs-lookup"><span data-stu-id="efde8-149">Permissions Level</span></span>  <br/> ![앱에 대 한 permisiions 수준을 나타내는 아이콘](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|<span data-ttu-id="efde8-151">이를 통해 Office 365 데이터에 대 한 앱의 액세스 정도를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-151">Use this to see how much access an app has to Office 365 data.</span></span> <span data-ttu-id="efde8-152">사용 권한 수준은 **낮음**, **중간**또는 **높음을**지정 하며, \*\*\*\* 이는 앱이 사용자의 프로필 및 이름에만 액세스 함을 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-152">Permissions levels indicate **Low**, **Medium**, or **High**, where **Low** might indicate that the app only accesses a user's profile and name.</span></span> <span data-ttu-id="efde8-153">앱에 부여 된 사용 권한, 커뮤니티 사용 및 [거 버 넌 스 로그](suspend-or-restore-an-account-in-ocas.md)에서 관련 활동 등의 자세한 정보를 보려면 수준을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-153">Select the level to view more information, such as permissions granted to the app, community use, and related activity in the [Governance log](suspend-or-restore-an-account-in-ocas.md).</span></span>  <br/> |
|<span data-ttu-id="efde8-154">마지막 권한</span><span class="sxs-lookup"><span data-stu-id="efde8-154">Last authorized</span></span> <br/> |<span data-ttu-id="efde8-155">이 방법을 사용 하 여 OAuth 앱이 조직의 Office 365 데이터에 액세스 하기 위해 마지막으로 권한이 부여 된 날짜 및 시간을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-155">Use this to see the date and time an OAuth app was last authorized to access your organization's Office 365 data.</span></span> <br/>  |
|<span data-ttu-id="efde8-156">동작</span><span class="sxs-lookup"><span data-stu-id="efde8-156">Actions</span></span><br/>![OAuth 앱](media/OCAS-OAuthAppApproveBanReport.png)<br/> |<span data-ttu-id="efde8-158">앱을 승인 되거나 금지 된 상태로 표시 하거나, Microsoft에 OAuth 앱을 보고 하거나, 지정 하지 않은 상태로 두려면이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-158">Use this to see or to mark an app as Approved or Banned, report an OAuth app to Microsoft, or leave it as undetermined.</span></span>  <br/> |
   
## <a name="mark-an-app-as-approved"></a><span data-ttu-id="efde8-159">앱을 승인 된 것으로 표시</span><span class="sxs-lookup"><span data-stu-id="efde8-159">Mark an app as approved</span></span>

<span data-ttu-id="efde8-160">**OAuth 앱 관리** 페이지에서 승인할 앱을 찾은 다음 **앱을 승인 된 것으로 표시** 아이콘을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-160">On the **Manage OAuth apps** page, locate the app you want to approve, and choose the **Mark app as approved** icon.</span></span> 
  
![앱을 승인 된 것으로 표시 아이콘을 선택 합니다.](media/OCAS-MarkOAuthApproved.png)
  
<span data-ttu-id="efde8-162">아이콘이 녹색으로 바뀌고 앱이 모든 Office 365 사용자에 대해 승인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-162">The icon turns green, and the app is approved for all your Office 365 users.</span></span>
  
> [!NOTE]
> <span data-ttu-id="efde8-163">앱을 승인 된 것으로 표시 하면 최종 사용자에 게 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-163">When you mark an app as approved, there is no effect on the end user.</span></span> <span data-ttu-id="efde8-164">승인 된 앱을 시각적으로 표시 하면 아직 검토 하지 않은 앱과이를 분리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-164">Visually marking the apps that are approved helps to separate them from apps that haven't been reviewed yet.</span></span> 
  
## <a name="ban-an-app"></a><span data-ttu-id="efde8-165">앱 금지</span><span class="sxs-lookup"><span data-stu-id="efde8-165">Ban an app</span></span>

1. <span data-ttu-id="efde8-166">**OAuth 앱 관리** 페이지에서 금지 하려는 앱을 찾은 다음 **앱을 금지 된 것으로 표시** 아이콘을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-166">On the **Manage OAuth apps** page, locate the app you want to ban, and choose the **Mark app as banned** icon.</span></span><br/><span data-ttu-id="efde8-167">![앱을 차단 된 것으로 표시 아이콘을 선택 합니다.](media/OCAS-MarkOAuthBanned.png)</span><span class="sxs-lookup"><span data-stu-id="efde8-167">![Choose the Mark app as banned icon](media/OCAS-MarkOAuthBanned.png)</span></span>
  
2. <span data-ttu-id="efde8-168">알림 메시지 상자에서 기존 텍스트를 그대로 유지 하거나 텍스트를 사용자 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-168">In the notification message box, keep the existing text as it is, or customize the text.</span></span> <span data-ttu-id="efde8-169">사용자에 게 앱이 금지 되었음을 알리는 것을 허용할 것인지 여부를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-169">Choose whether to let users know that their app has been banned.</span></span> <br/>![금지 된 앱에 대 한 메일 서식 파일](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. <span data-ttu-id="efde8-171">**앱 금지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-171">Choose **Ban app**.</span></span>

## <a name="report-an-oauth-app-to-microsoft"></a><span data-ttu-id="efde8-172">Microsoft에 OAuth 앱 보고</span><span class="sxs-lookup"><span data-stu-id="efde8-172">Report an OAuth app to Microsoft</span></span>

<span data-ttu-id="efde8-173">분석을 위해 Microsoft에 OAuth 앱을 제출 하려면 해당 앱을 보고 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-173">If you want to submit an OAuth app to Microsoft for analysis, you can report that app.</span></span>

1. <span data-ttu-id="efde8-174">**OAuth 앱 관리** 페이지에서 분석을 위해 제출할 앱을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-174">On the **Manage OAuth apps** page, locate the app you want to submit for analysis.</span></span>

2. <span data-ttu-id="efde8-175">줄임표 (열)를 선택 하 고 **보고서 앱 ...** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-175">Choose the vertical ellipsis, and then choose **Report app...**.</span></span><br/><span data-ttu-id="efde8-176">![OAuth 앱 보고](media/OCAS-MarkOAuthReported.png)</span><span class="sxs-lookup"><span data-stu-id="efde8-176">![Report an OAuth app](media/OCAS-MarkOAuthReported.png)</span></span><br/>

3. <span data-ttu-id="efde8-177">**이 앱 보고서** 대화 상자에서 드롭다운 목록을 사용 하 여 관심 있는 사항을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-177">In the **Report this app** dialog box, use the drop-down list to indicate your concern.</span></span> <span data-ttu-id="efde8-178">기본적으로 **이 앱은 악성** 으로 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-178">By default, **This app is malicious** is selected.</span></span> <span data-ttu-id="efde8-179">그러나 사용할 수 있는 다른 옵션 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-179">However, you can choose on one of the other available options.</span></span> <br/><span data-ttu-id="efde8-180">![OAuth 앱 보고](media/OCAS-ReportOAuthApp.png)</span><span class="sxs-lookup"><span data-stu-id="efde8-180">![Report an OAuth app](media/OCAS-ReportOAuthApp.png)</span></span><br/>

4. <span data-ttu-id="efde8-181">는 선택한 대화 상대에 게 옵션을 유지 하 고 나열 된 전자 메일 주소를 확인 하거나 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-181">(Recommended) Keep the option to contact you selected, and confirm (or edit) the email address listed.</span></span>

5. <span data-ttu-id="efde8-182">Choose **Submit**.</span><span class="sxs-lookup"><span data-stu-id="efde8-182">Choose **Submit**.</span></span> 
    
## <a name="create-an-app-query"></a><span data-ttu-id="efde8-183">앱 쿼리 만들기</span><span class="sxs-lookup"><span data-stu-id="efde8-183">Create an app query</span></span>

<span data-ttu-id="efde8-184">다음과 같은 고급 보기를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-184">We recommend using the Advanced view, which looks like this:</span></span> 

![고급 보기](media/OCAS-OAuthAppsAdvQueryView.png)

<span data-ttu-id="efde8-186">앱 쿼리 표시줄에서 **Advanced**가 표시 되 면 기본 보기를 사용 하 고 있는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-186">In the app query bar, if you see **Advanced**, you're using the Basic view.</span></span> <span data-ttu-id="efde8-187">advanced를 클릭 하거나 탭 \*\*\*\* 하 여 고급 보기로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-187">Click (or tap) **Advanced** to go to the Advanced view.</span></span> 

![기본 보기](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. <span data-ttu-id="efde8-189">쿼리 모음에서 **필터 선택** 목록을 사용 하 여 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-189">In the query bar, use the **Select a filter** list to choose an option.</span></span> 
    - <span data-ttu-id="efde8-190">**앱** 특정 이름을 가진 앱</span><span class="sxs-lookup"><span data-stu-id="efde8-190">**App** Apps with certain names</span></span>
    - <span data-ttu-id="efde8-191">**앱 상태** 해당 상태를 기반으로 하는 앱 (승인, 금지 또는 결정 되지 않음)</span><span class="sxs-lookup"><span data-stu-id="efde8-191">**App state** Apps based on their state (Approved, Banned, or Undetermined)</span></span>
    - <span data-ttu-id="efde8-192">**커뮤니티 사용** 커뮤니티 사용 수준 (드문, 드문, 공용)을 기반으로 하는 앱</span><span class="sxs-lookup"><span data-stu-id="efde8-192">**Community use** Apps based on community use levels (Rare, Uncommon, or Common)</span></span>
    - <span data-ttu-id="efde8-193">**사용 권한 수준** 특정 권한 수준을 기반으로 하는 앱</span><span class="sxs-lookup"><span data-stu-id="efde8-193">**Permission level** Apps based on certain permission levels</span></span> 
    - <span data-ttu-id="efde8-194">**사용 권한** 특정 권한이 필요한 앱</span><span class="sxs-lookup"><span data-stu-id="efde8-194">**Permissions** Apps that require certain permissions</span></span>
    - <span data-ttu-id="efde8-195">**Publisher**  특정 게시자의 앱</span><span class="sxs-lookup"><span data-stu-id="efde8-195">**Publisher**  Apps from certain publishers</span></span>
    - <span data-ttu-id="efde8-196">**사용자** 특정 사용자가 권한을 부여 받은 앱</span><span class="sxs-lookup"><span data-stu-id="efde8-196">**User** Apps that a certain user authorized</span></span>
   
2. <span data-ttu-id="efde8-197">**같음** 또는 **같지**않음을 선택한 다음 필터에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-197">Select **equals** or **does not equal**, and then specify a value for your filter.</span></span>
    
3. <span data-ttu-id="efde8-198">필터를 더 추가 하려면 더하기 기호 (</span><span class="sxs-lookup"><span data-stu-id="efde8-198">To add more filters, select the plus sign (</span></span>![앱 쿼리를 위한 필터 아이콘 추가](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)<span data-ttu-id="efde8-200">)을 선택한 다음 2 단계와 3 단계로 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-200">), and then repeat steps 2 and 3.</span></span>
    
4. <span data-ttu-id="efde8-201">필터를 제거 하려면 x를 선택 합니다 (</span><span class="sxs-lookup"><span data-stu-id="efde8-201">To remove a filter, select the x (</span></span>![앱 쿼리를 위한 필터 아이콘 제거](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)<span data-ttu-id="efde8-203">)를 필터 이름 옆에 둘 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-203">) next to a filter name.</span></span>
    
<span data-ttu-id="efde8-204">필터는 자동으로 적용 되며 앱 목록은 그에 따라 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efde8-204">The filters are applied automatically, and the apps list is updated accordingly.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="efde8-205">다음 단계</span><span class="sxs-lookup"><span data-stu-id="efde8-205">Next steps</span></span>

- [<span data-ttu-id="efde8-206">경고 검토 및 알림 작업 수행</span><span class="sxs-lookup"><span data-stu-id="efde8-206">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="efde8-207">[Office 365 Cloud App Security에 대 한 웹 트래픽 로그 및 데이터 원본](web-traffic-logs-and-data-sources-for-ocas.md) 검토</span><span class="sxs-lookup"><span data-stu-id="efde8-207">Review your [Web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="efde8-208">[Office 365 Cloud App Security에 대 한 사용률 작업](utilization-activities-for-ocas.md) 검토</span><span class="sxs-lookup"><span data-stu-id="efde8-208">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

