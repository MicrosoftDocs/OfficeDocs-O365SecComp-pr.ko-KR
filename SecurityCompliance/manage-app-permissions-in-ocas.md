---
title: Office 365 Cloud App Security를 사용하여 OAuth 앱 관리
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: Office 365 클라우드 응용 프로그램 보안에서 OAuth 앱 사용자에 게 Office 365 데이터에 사용 하기 위한 다운로드 앱을 관리 하는 데 도움이
ms.openlocfilehash: 2e3c6d9d42b22aa8bb666211431197744471e84f
ms.sourcegitcommit: 25f72d20e76463c2f0a075dfc0116f00c934bd77
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/27/2018
ms.locfileid: "27447046"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a><span data-ttu-id="e3852-103">Office 365 Cloud App Security를 사용하여 OAuth 앱 관리</span><span class="sxs-lookup"><span data-stu-id="e3852-103">Manage OAuth apps using Office 365 Cloud App Security</span></span>

|<span data-ttu-id="e3852-104">평가 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="e3852-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="e3852-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="e3852-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="e3852-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="e3852-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="e3852-107">사용률 \* \* \*</span><span class="sxs-lookup"><span data-stu-id="e3852-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="e3852-108">평가 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="e3852-109">계획을 시작합니다</span><span class="sxs-lookup"><span data-stu-id="e3852-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="e3852-110">배포를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="e3852-111">여기는!</span><span class="sxs-lookup"><span data-stu-id="e3852-111">You are here!</span></span>  <br/> [<span data-ttu-id="e3852-112">다음 단계</span><span class="sxs-lookup"><span data-stu-id="e3852-112">Next steps</span></span>](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="e3852-p101">사용자 선호 앱 하 고 자주 다운로드 자신이, 사용자가 대기 하는 앱 특히 간편 하 게 자신의 직장 가져오거나 정보 학교 하 여 시간을 절약 됩니다. 그러나 일부 응용 프로그램에는 조직에 보안 위험 가능성이, 정보에 따라 자신이 액세스 하 고 해당 정보를 처리 하는 방법입니다. [Office 365 클라우드 응용 프로그램 보안](office-365-cas-overview.md), 전역 또는 보안 관리자 인 경우 관리할 수 있습니다 OAuth 앱 조직에 대 한. 앱 사용자를 사용 하는 것을 볼 수 있습니다 Office 365 데이터와 사용 권한을 해당 앱이 등입니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-p101">People love apps and they download them often, especially apps that people think will save time by making it easier to get at their work or school information. However, some apps could potentially be a security risk to your organization, depending on what information they access and how they handle that information. With [Office 365 Cloud App Security](office-365-cas-overview.md), if you are a global or security administrator, you can manage OAuth apps for your organization. You can see the apps people are using with Office 365 data, what permissions those apps have, and more.</span></span> 
  
<span data-ttu-id="e3852-117">이 문서에서는 OAuth 앱을 관리로 이동 하는 위치, 승인, 금지, 또는 응용 프로그램을 보고 하는 방법 및 app 쿼리를 만드는 방법에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-117">This article describes where to go to manage OAuth apps, how to approve, ban, or report an app, and how to create an app query.</span></span>
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a><span data-ttu-id="e3852-118">OAuth 관리 앱 페이지를 찾는 방법</span><span class="sxs-lookup"><span data-stu-id="e3852-118">How to find the Manage OAuth apps page</span></span>

> [!NOTE]
> <span data-ttu-id="e3852-p102">OAuth apps Office 365 클라우드 응용 프로그램 보안 포털에서 관리 됩니다. 다음 작업을 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다. 더 많은 참조 내용을 알아보려면 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-p102">OAuth apps are managed in the Office 365 Cloud App Security portal. You must be a global administrator or security administrator to perform the following task. To learn more see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
1. <span data-ttu-id="e3852-p103">이동 [https://protection.office.com](https://protection.office.com) 및 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다. (이렇게 하면 보안 &amp; 준수 센터.)</span><span class="sxs-lookup"><span data-stu-id="e3852-p103">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="e3852-124">**경고** 로 이동 \> **관리 고급 알림**입니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-124">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="e3852-125">클릭 (또는 누릅니다) **Office 365 클라우드 응용 프로그램 보안으로 이동**합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-125">Click (or tap) **Go to Office 365 Cloud App Security**.</span></span><br/><span data-ttu-id="e3852-126">![보안에서 &amp; 준수 센터 Office 365 클라우드 앱 보안으로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="e3852-126">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br/><span data-ttu-id="e3852-p104">**참고**: Office 365 클라우드 App 보안은 아직 설정 하지 않으면, 수행할 수 있는이 페이지에 있습니다. [Office 365 클라우드 응용 프로그램 보안에 대 한 준비](get-ready-for-office-365-cas.md)를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-p104">**NOTE**: If Office 365 Cloud App Security is not turned on yet, you can do that on this page. See [Get ready for Office 365 Cloud App Security](get-ready-for-office-365-cas.md).</span></span> 
  
4. <span data-ttu-id="e3852-129">**조사** 선택 \> **OAuth 앱**입니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-129">Choose **Investigate** \> **OAuth apps**.</span></span><br/><span data-ttu-id="e3852-130">![O365 CAS 포털에서 조사를 선택 합니다.](media/OCAS-OAuthApps.png)</span><span class="sxs-lookup"><span data-stu-id="e3852-130">![In the O365 CAS portal, choose Investigate.](media/OCAS-OAuthApps.png)</span></span><br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a><span data-ttu-id="e3852-131">OAuth 관리 앱 페이지에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-131">What you'll see on the Manage OAuth apps page</span></span>

<span data-ttu-id="e3852-132">다음 표에서 OAuth 관리 앱 페이지에서 컨트롤 및 사용할 수 있는 옵션을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-132">The following table describes the controls and options available on the Manage OAuth apps page.</span></span>
  
|<span data-ttu-id="e3852-133">**항목**</span><span class="sxs-lookup"><span data-stu-id="e3852-133">**Item**</span></span>|<span data-ttu-id="e3852-134">**설명**</span><span class="sxs-lookup"><span data-stu-id="e3852-134">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3852-135">App 쿼리 모음에서 기본 아이콘</span><span class="sxs-lookup"><span data-stu-id="e3852-135">Basic icon in the app query bar</span></span>  <br/> ![쿼리를 위한 기본 쿼리 보기를 나타내는 아이콘](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|<span data-ttu-id="e3852-137">고급 보기로 전환 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-137">Select this to switch to the Advanced view.</span></span>  <br/> <span data-ttu-id="e3852-138">( **기본**표시 되 면 사용 하는 고급 보기)</span><span class="sxs-lookup"><span data-stu-id="e3852-138">(If you see **Basic**, you are using the Advanced view)</span></span>  <br/> |
|<span data-ttu-id="e3852-139">앱 쿼리 바에서 고급 아이콘</span><span class="sxs-lookup"><span data-stu-id="e3852-139">Advanced icon in the app query bar</span></span>  <br/> ![쿼리를 위한 고급 쿼리 보기를 나타내는 아이콘](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|<span data-ttu-id="e3852-141">기본 보기로 전환 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-141">Select this to switch to the Basic view.</span></span>  <br/> <span data-ttu-id="e3852-142">( **고급**를 참조 하는 경우 사용 하는 기본 보기입니다.)</span><span class="sxs-lookup"><span data-stu-id="e3852-142">(If you see **Advanced**, you are using the Basic view.)</span></span>  <br/> |
|<span data-ttu-id="e3852-143">열거나 닫으려면 응용 프로그램 목록에서 모든 세부 정보 아이콘</span><span class="sxs-lookup"><span data-stu-id="e3852-143">Open or close all details icon in the app list</span></span>  <br/> ![이 아이콘을 열거나 닫으려면 모든 앱에 대 한 모든 세부 정보를 클릭 합니다.](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|<span data-ttu-id="e3852-145">각 응용 프로그램에 대 한 더 많이 또는 적게 세부 정보를 보려면이 아이콘을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-145">Select this icon to view more or fewer details about each app.</span></span>  <br/> |
|<span data-ttu-id="e3852-146">응용 프로그램 목록에서 내보내기 아이콘</span><span class="sxs-lookup"><span data-stu-id="e3852-146">Export icon in the app list</span></span>  <br/> ![모든 앱의 csv 파일을 내보내려면이 아이콘을 클릭 합니다.](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|<span data-ttu-id="e3852-148">응용 프로그램, 응용 프로그램, 사용 권한 수준, 응용 프로그램 상태 및 수준을 사용 하는 커뮤니티와 관련 된 사용 권한 각 응용 프로그램에 대 한 사용자 수가 목록이 포함 된 CSV 파일을 내보내려면이 아이콘을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-148">Select this icon to export a CSV file that contains a list of apps, number of users for each app, permissions associated with the app, permissions level, app state, and community use level.</span></span>  <br/> |
|<span data-ttu-id="e3852-149">Name</span><span class="sxs-lookup"><span data-stu-id="e3852-149">Name</span></span>  <br/> |<span data-ttu-id="e3852-p105">이를 사용 하는 app. 선택의 이름을 보려면 설명, publisher, app 웹사이트 및 응용 프로그램 id입니다.와 같은 자세한 정보를 보려면 이름</span><span class="sxs-lookup"><span data-stu-id="e3852-p105">Use this to see the name of an app. Select the name to view more information, such as its description, publisher, app website and app ID.</span></span>  <br/> |
|<span data-ttu-id="e3852-152">에 의해 권한이 부여</span><span class="sxs-lookup"><span data-stu-id="e3852-152">Authorized by</span></span>  <br/> |<span data-ttu-id="e3852-p106">이 사용 하 여 얼마나 많은 사용자가 Office 365 계정에 액세스 하는 응용 프로그램 권한이 부여 된를 참조 하십시오. 사용자 계정의 목록 등의 자세한 정보를 볼 수를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-p106">Use this to see how many users have authorized an app to access their Office 365 account. Select the number to view more information, such as a list of user accounts.</span></span>  <br/> |
|<span data-ttu-id="e3852-155">사용 권한 수준</span><span class="sxs-lookup"><span data-stu-id="e3852-155">Permissions Level</span></span>  <br/> ![응용 프로그램에 대 한 permisiions 수준을 나타내는 아이콘](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|<span data-ttu-id="e3852-p107">이 사용 하 여 app 횟수나가 Office 365 데이터를 볼 수 있습니다. 사용 권한 수준을 **낮음**, **보통**또는 **높음**여기서는 앱만 액세스 하는 사용자의 프로필 및 이름 **낮은** 나타낼 수를 나타냅니다. App, 커뮤니티 사용 및 [관리 방식 로그](suspend-or-restore-an-account-in-ocas.md)에서 관련된 작업을 부여 된 사용 권한 등의 자세한 정보를 보려면 수준을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-p107">Use this to see how much access an app has to Office 365 data. Permissions levels indicate **Low**, **Medium**, or **High**, where **Low** might indicate that the app only accesses a user's profile and name. Select the level to view more information, such as permissions granted to the app, community use, and related activity in the [Governance log](suspend-or-restore-an-account-in-ocas.md).  </span></span><br/> |
|<span data-ttu-id="e3852-160">권한이 부여 된 마지막</span><span class="sxs-lookup"><span data-stu-id="e3852-160">Last authorized</span></span> <br/> |<span data-ttu-id="e3852-161">이 사용 하 여 날짜 및 시간 OAuth 앱 조직의 Office 365 데이터에 액세스할 수 있는 권한을 부여 마지막 받았습니다를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="e3852-161">Use this to see the date and time an OAuth app was last authorized to access your organization's Office 365 data.</span></span> <br/>  |
|<span data-ttu-id="e3852-162">동작</span><span class="sxs-lookup"><span data-stu-id="e3852-162">Actions</span></span><br/>![OAuth 앱](media/OCAS-OAuthAppApproveBanReport.png)<br/> |<span data-ttu-id="e3852-164">이 사용 하 여를 표시 하거나 승인 됨 또는 Banned, 응용 프로그램을 표시 하려면 OAuth 응용 프로그램을 Microsoft에 보고 또는 지정 되지 않은 상태로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-164">Use this to see or to mark an app as Approved or Banned, report an OAuth app to Microsoft, or leave it as undetermined.</span></span>  <br/> |
   
## <a name="mark-an-app-as-approved"></a><span data-ttu-id="e3852-165">응용 프로그램을 승인 된 것으로 표시</span><span class="sxs-lookup"><span data-stu-id="e3852-165">Mark an app as approved</span></span>

<span data-ttu-id="e3852-166">**OAuth 관리 앱** 페이지에서 승인 하려는 앱 찾은 **Mark 응용 프로그램으로 승인 된** 아이콘을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-166">On the **Manage OAuth apps** page, locate the app you want to approve, and choose the **Mark app as approved** icon.</span></span> 
  
![승인 된 아이콘으로 표시 응용 프로그램을 선택 합니다.](media/OCAS-MarkOAuthApproved.png)
  
<span data-ttu-id="e3852-168">아이콘, 녹색으로 바뀌고 응용 프로그램은 모든 Office 365 사용자에 대 한 승인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-168">The icon turns green, and the app is approved for all your Office 365 users.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e3852-p108">응용 프로그램을 승인 된 것으로 표시 하면 때 최종 사용자에 대 한 영향을 주지 않습니다. 승인 된 응용 프로그램을 시각적으로 표시 하는 작업은 아직 검토 하지 않은 된 응용 프로그램에서 구분 하는데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-p108">When you mark an app as approved, there is no effect on the end user. Visually marking the apps that are approved helps to separate them from apps that haven't been reviewed yet.</span></span> 
  
## <a name="ban-an-app"></a><span data-ttu-id="e3852-171">응용 프로그램을 금지합니다</span><span class="sxs-lookup"><span data-stu-id="e3852-171">Ban an app</span></span>

1. <span data-ttu-id="e3852-172">**OAuth 관리 앱** 페이지에서 금지 하려면 응용 프로그램 찾은 **으로 Mark app 금지** 아이콘을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-172">On the **Manage OAuth apps** page, locate the app you want to ban, and choose the **Mark app as banned** icon.</span></span><br/><span data-ttu-id="e3852-173">![금지 된 아이콘으로 표시 app를 선택 합니다.](media/OCAS-MarkOAuthBanned.png)</span><span class="sxs-lookup"><span data-stu-id="e3852-173">![Choose the Mark app as banned icon](media/OCAS-MarkOAuthBanned.png)</span></span>
  
2. <span data-ttu-id="e3852-p109">알림 메시지 상자에 그대로, 기존 텍스트를 그대로 사용 하거나 텍스트를 사용자 지정 합니다. 사용자가 응용 프로그램을 통해 금지 되었습니다 알고 있도록 여부를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-p109">In the notification message box, keep the existing text as it is, or customize the text. Choose whether to let users know that their app has been banned.</span></span> <br/>![금지 된 응용 프로그램에 대 한 메일 서식 파일](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. <span data-ttu-id="e3852-177">**Ban 응용 프로그램**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-177">Choose **Ban app**.</span></span>

## <a name="report-an-oauth-app-to-microsoft"></a><span data-ttu-id="e3852-178">OAuth 응용 프로그램을 Microsoft에 보고</span><span class="sxs-lookup"><span data-stu-id="e3852-178">Report an OAuth app to Microsoft</span></span>

<span data-ttu-id="e3852-179">분석을 위해 Microsoft에 OAuth 앱 전송 하려는 경우에 해당 응용 프로그램을 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-179">If you want to submit an OAuth app to Microsoft for analysis, you can report that app.</span></span>

1. <span data-ttu-id="e3852-180">**OAuth 관리 앱** 페이지에서 분석을 위해 제출 하려는 앱을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-180">On the **Manage OAuth apps** page, locate the app you want to submit for analysis.</span></span>

2. <span data-ttu-id="e3852-181">세로 줄임표 (...)를 선택 하 고 **보고서 app...** 선택 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-181">Choose the vertical ellipsis, and then choose **Report app...**.</span></span><br/><span data-ttu-id="e3852-182">![OAuth 응용 프로그램을 보고 합니다.](media/OCAS-MarkOAuthReported.png)</span><span class="sxs-lookup"><span data-stu-id="e3852-182">![Report an OAuth app](media/OCAS-MarkOAuthReported.png)</span></span><br/>

3. <span data-ttu-id="e3852-p110">**이 app 보고서** 대화 상자에서 드롭다운 목록에 관심을 나타내기 위해 사용 합니다. **이 응용 프로그램은 악의적인** 기본적으로 선택 됩니다. 그러나 다른 사용 가능한 옵션 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-p110">In the **Report this app** dialog box, use the drop-down list to indicate your concern. By default, **This app is malicious** is selected. However, you can choose on one of the other available options. </span></span><br/><span data-ttu-id="e3852-186">![OAuth 응용 프로그램을 보고 합니다.](media/OCAS-ReportOAuthApp.png)</span><span class="sxs-lookup"><span data-stu-id="e3852-186">![Report an OAuth app](media/OCAS-ReportOAuthApp.png)</span></span><br/>

4. <span data-ttu-id="e3852-187">(권장) 이 옵션을 선택 하는 사용자에 게 연락 하는 옵션을 그대로 유지 하 고 나열 된 전자 메일 주소를 확인 (또는 편집).</span><span class="sxs-lookup"><span data-stu-id="e3852-187">(Recommended) Keep the option to contact you selected, and confirm (or edit) the email address listed.</span></span>

5. <span data-ttu-id="e3852-188">**Submit(전송)** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-188">Choose **Submit**.</span></span> 
    
## <a name="create-an-app-query"></a><span data-ttu-id="e3852-189">App 쿼리 만들기</span><span class="sxs-lookup"><span data-stu-id="e3852-189">Create an app query</span></span>

<span data-ttu-id="e3852-190">그러면 다음과 같은 고급 보기를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-190">We recommend using the Advanced view, which looks like this:</span></span> 

![고급 보기](media/OCAS-OAuthAppsAdvQueryView.png)

<span data-ttu-id="e3852-p111">App 쿼리 표시줄에서 **고급**을 참조 하는 경우 사용 하는 기본 보기입니다. 클릭 (또는 누릅니다) **고급** 고급 보기로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-p111">In the app query bar, if you see **Advanced**, you're using the Basic view. Click (or tap) **Advanced** to go to the Advanced view.</span></span> 

![기본 보기](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. <span data-ttu-id="e3852-195">쿼리 표시줄에서 **필터를 선택** 목록을 사용 하 여 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-195">In the query bar, use the **Select a filter** list to choose an option.</span></span> 
    - <span data-ttu-id="e3852-196">**응용 프로그램** 특정 이름의 앱</span><span class="sxs-lookup"><span data-stu-id="e3852-196">**App** Apps with certain names</span></span>
    - <span data-ttu-id="e3852-197">**응용 프로그램 상태** (승인 됨, Banned, 또는 Undetermined) 상태에 따라 앱</span><span class="sxs-lookup"><span data-stu-id="e3852-197">**App state** Apps based on their state (Approved, Banned, or Undetermined)</span></span>
    - <span data-ttu-id="e3852-198">**커뮤니티 사용** 커뮤니티에 따라 앱 수준 (Rare, Uncommon, 또는 공통)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-198">**Community use** Apps based on community use levels (Rare, Uncommon, or Common)</span></span>
    - <span data-ttu-id="e3852-199">**사용 권한 수준** 특정 권한 수준에 따라 앱</span><span class="sxs-lookup"><span data-stu-id="e3852-199">**Permission level** Apps based on certain permission levels</span></span> 
    - <span data-ttu-id="e3852-200">**사용 권한** 특정 사용 권한이 필요로 하는 앱</span><span class="sxs-lookup"><span data-stu-id="e3852-200">**Permissions** Apps that require certain permissions</span></span>
    - <span data-ttu-id="e3852-201">**Publisher**  특정 게시자 로부터 앱</span><span class="sxs-lookup"><span data-stu-id="e3852-201">**Publisher**  Apps from certain publishers</span></span>
    - <span data-ttu-id="e3852-202">**사용자** 특정 사용자 권한이 부여 된 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="e3852-202">**User** Apps that a certain user authorized</span></span>
   
2. <span data-ttu-id="e3852-203">**같음** 또는 **같지 않음**, 선택한 다음 필터에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-203">Select **equals** or **does not equal**, and then specify a value for your filter.</span></span>
    
3. <span data-ttu-id="e3852-204">더 많은 필터를 추가 하려면 더하기 기호 (선택</span><span class="sxs-lookup"><span data-stu-id="e3852-204">To add more filters, select the plus sign (</span></span>![앱을 쿼리 하기 위한 필터 아이콘 추가](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)<span data-ttu-id="e3852-206">)를 한 다음 2-3 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-206">), and then repeat steps 2 and 3.</span></span>
    
4. <span data-ttu-id="e3852-207">필터를 제거 하는 x (를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-207">To remove a filter, select the x (</span></span>![앱을 쿼리 하기 위한 필터 아이콘 제거](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)<span data-ttu-id="e3852-209">) 필터 이름 옆에 있는 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-209">) next to a filter name.</span></span>
    
<span data-ttu-id="e3852-210">필터는 자동으로 적용 하 고 앱 목록 적절 하 게 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-210">The filters are applied automatically, and the apps list is updated accordingly.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="e3852-211">다음 단계</span><span class="sxs-lookup"><span data-stu-id="e3852-211">Next steps</span></span>

- [<span data-ttu-id="e3852-212">검토 및 알림 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-212">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="e3852-213">검토 하 여 [웹 트래픽 로그 및 Office 365 클라우드 응용 프로그램 보안에 대 한 데이터 원본](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="e3852-213">Review your [Web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="e3852-214">[Office 365 클라우드 응용 프로그램 보안에 대 한 사용률 활동](utilization-activities-for-ocas.md) 을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3852-214">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

