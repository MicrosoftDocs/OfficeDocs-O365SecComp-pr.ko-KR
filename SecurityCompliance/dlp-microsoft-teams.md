---
title: 데이터 손실 방지 및 Microsoft 팀
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 07/01/2019
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
description: 이제 Microsoft 팀 채팅 및 채널에 DLP 정책을 적용할 수 있습니다. 이 문서를 읽으면 작동 방식에 대해 자세히 알아볼 수 있습니다.
ms.openlocfilehash: 3792fd6919749510ea20d4ff84b0249b16165a9f
ms.sourcegitcommit: cc1b0281fa594cbb7c09f3e419df21aec9557831
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35417400"
---
# <a name="data-loss-prevention-and-microsoft-teams"></a><span data-ttu-id="eda04-104">데이터 손실 방지 및 Microsoft 팀</span><span class="sxs-lookup"><span data-stu-id="eda04-104">Data loss prevention and Microsoft Teams</span></span>

> [!NOTE]
> <span data-ttu-id="eda04-105">데이터 손실 방지 기능은 최근 Office 365 E5 및 Office 365 고급 규정 준수의 Microsoft 팀에 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-105">Data loss prevention capabilities were recently added to Microsoft Teams in Office 365 E5 and Office 365 Advanced Compliance.</span></span> <span data-ttu-id="eda04-106">기능 가용성에 대 한 자세한 내용은 [office 365 서비스 설명: office 365 보안 & 준수 센터](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eda04-106">To learn more about feature availability, see [Office 365 Service Descriptions: Office 365 Security & Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center).</span></span>

## <a name="overview-of-dlp-for-microsoft-teams"></a><span data-ttu-id="eda04-107">Microsoft 팀의 DLP 개요</span><span class="sxs-lookup"><span data-stu-id="eda04-107">Overview of DLP for Microsoft Teams</span></span>

<span data-ttu-id="eda04-108">최근에 DLP ( [데이터 손실 방지](data-loss-prevention-policies.md) ) 기능이 Microsoft 팀을 포함 하도록 확장 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-108">Recently, [data loss prevention](data-loss-prevention-policies.md) (DLP) capabilities were extended to include Microsoft Teams.</span></span> <span data-ttu-id="eda04-109">조직에 DLP가 있는 경우에는 사용자가 Microsoft 팀 채널 또는 채팅 세션에서 중요 한 정보를 공유 하지 못하도록 하는 정책을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-109">If your organization has DLP, you can now define policies that prevent people from sharing sensitive information in a Microsoft Teams channel or chat session.</span></span> <span data-ttu-id="eda04-110">다음은 이러한 보호의 작동 방식에 대 한 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-110">Here are some examples of how this protection works:</span></span>

- <span data-ttu-id="eda04-111">**예 1: 메시지의 중요 한 정보 보호**</span><span class="sxs-lookup"><span data-stu-id="eda04-111">**Example 1: Protecting sensitive information in messages**.</span></span> <span data-ttu-id="eda04-112">다른 사용자가 guests (외부 사용자)를 사용 하 여 팀 채팅 이나 채널에서 중요 한 정보를 공유 하려고 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-112">Suppose that someone attempts to share sensitive information in a Teams chat or channel with guests (external users).</span></span> <span data-ttu-id="eda04-113">이를 방지 하기 위해 DLP 정책이 정의 된 경우 외부 사용자에 게 전송 되는 중요 한 정보가 포함 된 메시지가 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-113">If you have a DLP policy defined to prevent this, messages with sensitive information that are sent to external users are deleted.</span></span> <span data-ttu-id="eda04-114">이 작업은 DLP 정책이 구성 되는 방식에 따라 자동으로 몇 초 이내에 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-114">This happens automatically, and within seconds, according to how your DLP policy is configured.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eda04-115">Microsoft 팀의 DLP는 팀 및 채널에서 [게스트 액세스](https://docs.microsoft.com/MicrosoftTeams/guest-access) 권한이 있는 사용자와 모임 및 채팅 세션에서 [외부 액세스](https://docs.microsoft.com/MicrosoftTeams/manage-external-access) 권한이 있는 사용자와 공유 하는 경우 중요 한 콘텐츠를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-115">DLP for Microsoft Teams blocks sensitive content when shared with users who have [guest access](https://docs.microsoft.com/MicrosoftTeams/guest-access) in teams and channels, and with users who have [external access](https://docs.microsoft.com/MicrosoftTeams/manage-external-access) in meetings and chat sessions.</span></span> <span data-ttu-id="eda04-116">[Microsoft 팀과 비즈니스용 Skype를 함께](https://docs.microsoft.com/microsoftteams/migration-interop-guidance-for-teams-with-skype)사용 하는 경우에는 팀의 DLP가 interop 또는 페더레이션 채팅 세션에서 메시지를 차단 하지 않는다는 점을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-116">If you are using [Microsoft Teams together with Skype for Business](https://docs.microsoft.com/microsoftteams/migration-interop-guidance-for-teams-with-skype), keep in mind that DLP for Teams does not block messages in interop or federated chat sessions.</span></span>

- <span data-ttu-id="eda04-117">**예 2: 문서에서 중요 한 정보를 보호**하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-117">**Example 2: Protecting sensitive information in documents**.</span></span> <span data-ttu-id="eda04-118">다른 사용자가 Microsoft 팀 채널 또는 채팅에서 게스트와 문서를 공유 하려고 하지만 문서에 중요 한 정보가 포함 되어 있다고 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-118">Suppose that someone attempts to share a document with guests in a Microsoft Teams channel or chat, and the document contains sensitive information.</span></span> <span data-ttu-id="eda04-119">이를 방지 하기 위해 DLP 정책을 정의 하는 경우 해당 사용자에 대 한 문서가 열리지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-119">If you have a DLP policy defined to prevent this, the document won't open for those users.</span></span> <span data-ttu-id="eda04-120">이 경우에는 보호 기능을 적용 하기 위해 DLP 정책에 SharePoint 및 OneDrive가 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-120">Note that in this case, your DLP policy must include SharePoint and OneDrive in order for protection to be in place.</span></span> <span data-ttu-id="eda04-121">이는 Microsoft 팀에 표시 되는 SharePoint 용 DLP의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-121">(This is an example of DLP for SharePoint that shows up in Microsoft Teams.)</span></span>

## <a name="policy-tips-help-educate-users"></a><span data-ttu-id="eda04-122">사용자를 교육 하는 데 도움이 되는 정책 팁</span><span class="sxs-lookup"><span data-stu-id="eda04-122">Policy tips help educate users</span></span>

<span data-ttu-id="eda04-123">[웹에서의 Exchange, outlook 및 outlook](data-loss-prevention-policies.md#policy-evaluation-in-exchange-online-outlook-and-outlook-on-the-web), [SharePoint 및 비즈니스용 OneDrive 사이트](data-loss-prevention-policies.md#policy-evaluation-in-onedrive-for-business-and-sharepoint-online-sites), [Office 데스크톱 클라이언트](data-loss-prevention-policies.md#policy-evaluation-in-the-office-desktop-programs)에서 dlp가 작동 하는 방식과 마찬가지로, 작업이 DLP 정책과 충돌할 때 정책 팁이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-123">Similar to how DLP works in [Exchange, Outlook, and Outlook on the web](data-loss-prevention-policies.md#policy-evaluation-in-exchange-online-outlook-and-outlook-on-the-web), [SharePoint and OneDrive for Business sites](data-loss-prevention-policies.md#policy-evaluation-in-onedrive-for-business-and-sharepoint-online-sites), and [Office desktop clients](data-loss-prevention-policies.md#policy-evaluation-in-the-office-desktop-programs), policy tips appear when an action conflicts with a DLP policy.</span></span> <span data-ttu-id="eda04-124">정책 팁의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-124">Here's an example of a policy tip:</span></span>

![팀의 차단 된 메시지 알림](media/dlp-teams-blockedmessage-notification.png)

<span data-ttu-id="eda04-126">이 경우 보낸 사람은 Microsoft 팀 채널에서 주민 등록 번호를 공유 하려고 했습니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-126">In this case, the sender attempted to share a social security number in a Microsoft Teams channel.</span></span> <span data-ttu-id="eda04-127">어떤 작업을 **수행할 수 있나요?** link에서는이 문제를 해결 하기 위한 옵션을 제공 하는 대화 상자를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-127">The **What can I do?** link opens a dialog box that provides options for the sender to resolve the issue.</span></span> <span data-ttu-id="eda04-128">이 경우 보낸 사람은 정책을 재정의 하도록 선택 하거나 관리자에 게 문의 하 여 검토 하 고 해결 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-128">Notice that in this case, the sender can opt to override the policy, or notify an admin to review and resolve it.</span></span>

![차단 된 메시지 해결 옵션](media/dlp-teams-blockedmessage-possibleactions.png)

<span data-ttu-id="eda04-130">조직에서는 사용자가 DLP 정책을 재정의 하도록 허용할지 여부를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-130">In your organization, you can choose whether to allow users to override a DLP policy, or not.</span></span> <span data-ttu-id="eda04-131">그리고 DLP 정책을 구성할 때 기본 정책 팁을 사용 하거나 조직에 대 한 [정책 팁을 사용자 지정할](#to-customize-policy-tips) 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-131">And, when you configure your DLP policies, you can use the default policy tips, or [customize policy tips](#to-customize-policy-tips) for your organization.</span></span> 

<span data-ttu-id="eda04-132">예를 들어 보낸 사람이 팀 채널에서 주민 등록 번호를 공유 하는 경우, 받는 사람에 게 표시 되는 결과는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-132">Returning to our example, where a sender shared a social security number in a Teams channel, here's what the recipient saw:</span></span>

![메시지 차단 됨](media/dlp-teams-blockedmessage-notification-to-user.png)

<span data-ttu-id="eda04-134">" **설명** 합니다." 링크를 선택 하면 메시지가 차단 된 이유를 설명 하는 DLP 정책에 대 한 [문서](data-loss-prevention-policies.md) 를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-134">The **What's this?** link opens an [article](data-loss-prevention-policies.md) about DLP policies, which helps explain why the message was blocked.</span></span>

### <a name="to-customize-policy-tips"></a><span data-ttu-id="eda04-135">정책 팁을 사용자 지정 하려면</span><span class="sxs-lookup"><span data-stu-id="eda04-135">To customize policy tips</span></span>

<span data-ttu-id="eda04-136">이 작업을 수행 하려면 DLP 정책을 편집할 수 있는 권한이 있는 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-136">To perform this task, you must be assigned a role that has permissions to edit DLP policies.</span></span> <span data-ttu-id="eda04-137">자세한 내용은 [사용 권한을](data-loss-prevention-policies.md#permissions)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="eda04-137">To learn more, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

1. <span data-ttu-id="eda04-138">Office 365 Security & 준수 센터 ([https://protection.office.com](https://protection.office.com))로 이동 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-138">Go to the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)) and sign in.</span></span>

2. <span data-ttu-id="eda04-139">**데이터 손실 방지** > **정책을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-139">Choose **Data loss prevention** > **Policy**.</span></span> 

3. <span data-ttu-id="eda04-140">정책을 선택 하 고 **정책 설정**옆에서 **편집**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-140">Select a policy, and next to **Policy settings**, choose **Edit**.</span></span>

4. <span data-ttu-id="eda04-141">새 규칙을 만들거나 정책에 대 한 기존 규칙을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-141">Either create a new rule, or edit an existing rule for the policy.</span></span><br/>![정책에 대 한 규칙 편집](media/dlp-teams-editrule.png)<br/>

5. <span data-ttu-id="eda04-143">**사용자 알림** 탭에서 **전자 메일 텍스트 사용자 지정** 및/또는 **정책 팁 텍스트 옵션 사용자 지정** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-143">On the **User notifications** tab, select **Customize the email text** and/or **Customize the policy tip text** options.</span></span><br/><span data-ttu-id="eda04-144">![사용자 알림 및 정책 팁 사용자 지정](media/dlp-teams-editrule-usernotifications.png)</span><span class="sxs-lookup"><span data-stu-id="eda04-144">![Customize user notifications and policy tips](media/dlp-teams-editrule-usernotifications.png)</span></span><br/>  

6. <span data-ttu-id="eda04-145">전자 메일 알림 및/또는 정책 팁에 사용할 텍스트를 지정 하 고 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-145">Specify the text you want to use for email notifications and/or policy tips, and then choose **Save**.</span></span> 

7. <span data-ttu-id="eda04-146">**정책 설정** 탭에서 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-146">On the **Policy settings** tab, choose **Save**.</span></span>

<span data-ttu-id="eda04-147">변경 내용이 데이터 센터를 통해 작동 하 고 사용자 계정과 동기화 되도록 약 1 시간을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-147">Allow approximately one hour for your changes to work their way through your data center and sync to user accounts.</span></span>
 
## <a name="add-microsoft-teams-as-a-location-to-existing-dlp-policies"></a><span data-ttu-id="eda04-148">Microsoft 팀을 기존 DLP 정책에 대 한 위치로 추가</span><span class="sxs-lookup"><span data-stu-id="eda04-148">Add Microsoft Teams as a location to existing DLP policies</span></span>

<span data-ttu-id="eda04-149">이 작업을 수행 하려면 DLP 정책을 편집할 수 있는 권한이 있는 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-149">To perform this task, you must be assigned a role that has permissions to edit DLP policies.</span></span> <span data-ttu-id="eda04-150">자세한 내용은 [사용 권한을](data-loss-prevention-policies.md#permissions)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="eda04-150">To learn more, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

1. <span data-ttu-id="eda04-151">Office 365 Security & 준수 센터 ([https://protection.office.com](https://protection.office.com))로 이동 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-151">Go to the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)) and sign in.</span></span>

2. <span data-ttu-id="eda04-152">**데이터 손실 방지** > **정책을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-152">Choose **Data loss prevention** > **Policy**.</span></span> 

3. <span data-ttu-id="eda04-153">정책을 선택 하 고 **위치**아래의 값을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-153">Select a policy, and look at the values under **Locations**.</span></span> <span data-ttu-id="eda04-154">**팀 채팅 및 채널 메시지가**표시 되 면 모든 설정이 완료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-154">If you see **Teams chat and channel messages**, you're all set.</span></span> <span data-ttu-id="eda04-155">그렇지 않으면 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-155">If you don't, click **Edit**.</span></span><br/><span data-ttu-id="eda04-156">![기존 정책에 대 한 위치](media/dlp-teams-editexistingpolicy.png)</span><span class="sxs-lookup"><span data-stu-id="eda04-156">![Locations for existing policy](media/dlp-teams-editexistingpolicy.png)</span></span><br/>

4. <span data-ttu-id="eda04-157">**상태** 열에서 **팀 채팅 및 채널 메시지**에 대 한 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-157">In the **Status** column, turn the policy on for **Teams chat and channel messages**.</span></span><br/><span data-ttu-id="eda04-158">![팀 채팅 및 채널에 대 한 DLP](media/dlp-teams-addteamschatschannels.png)</span><span class="sxs-lookup"><span data-stu-id="eda04-158">![DLP for Teams chats and channels](media/dlp-teams-addteamschatschannels.png)</span></span><br/>

5. <span data-ttu-id="eda04-159">모든 계정의 기본 설정을 유지 하거나 포함 하거나 제외할 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-159">Keep the default settings of all accounts, or specify which accounts to include or exclude.</span></span>

6. <span data-ttu-id="eda04-160">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-160">Click **Save**.</span></span>

<span data-ttu-id="eda04-161">변경 내용이 데이터 센터를 통해 작동 하 고 사용자 계정과 동기화 되도록 약 1 시간을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-161">Allow approximately one hour for your changes to work their way through your data center and sync to user accounts.</span></span>

## <a name="define-a-new-dlp-policy-for-microsoft-teams"></a><span data-ttu-id="eda04-162">Microsoft 팀에 대 한 새 DLP 정책 정의</span><span class="sxs-lookup"><span data-stu-id="eda04-162">Define a new DLP policy for Microsoft Teams</span></span>

<span data-ttu-id="eda04-163">이 작업을 수행 하려면 DLP 정책을 편집할 수 있는 권한이 있는 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-163">To perform this task, you must be assigned a role that has permissions to edit DLP policies.</span></span> <span data-ttu-id="eda04-164">자세한 내용은 [사용 권한을](data-loss-prevention-policies.md#permissions)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="eda04-164">To learn more, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

1. <span data-ttu-id="eda04-165">Office 365 Security & 준수 센터 ([https://protection.office.com](https://protection.office.com))로 이동 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-165">Go to the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)) and sign in.</span></span>

2. <span data-ttu-id="eda04-166">**데이터 손실 방지** > **정책** > 및**정책 만들기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-166">Choose **Data loss prevention** > **Policy** > **+ Create a policy**.</span></span> 

3. <span data-ttu-id="eda04-167">[서식 파일](data-loss-prevention-policies.md#dlp-policy-templates)을 선택 하 고 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-167">Choose a [template](data-loss-prevention-policies.md#dlp-policy-templates), and then choose **Next**.</span></span><br/><span data-ttu-id="eda04-168">이 예제에서는 미국 개인 식별이 가능한 정보 데이터 서식 파일을 선택 했습니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-168">In our example, we chose the U.S. Personally Identifiable Information Data template.</span></span><br/><span data-ttu-id="eda04-169">![DLP 정책에 대 한 개인 정보 서식 파일](media/dlp-teams-createnewpolicy-template.png)</span><span class="sxs-lookup"><span data-stu-id="eda04-169">![Privacy template for DLP policy](media/dlp-teams-createnewpolicy-template.png)</span></span><br/>

4. <span data-ttu-id="eda04-170">**정책 이름** 지정 탭에서 정책의 이름과 설명을 입력 하 고 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-170">On the **Name your policy** tab, specify a name and description for the policy, and then choose **Next**.</span></span> 

5. <span data-ttu-id="eda04-171">**위치 선택** 탭에서 모든 위치의 기본 설정을 유지 하거나, **특정 위치 선택 허용**을 선택 하 고 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-171">On the **Choose locations** tab, keep the default setting of all locations, or select **Let me choose specific locations**, and then choose **Next**.</span></span><br/><span data-ttu-id="eda04-172">특정 위치를 선택 하도록 선택한 경우 DLP 정책에 대 한 위치를 선택 하 고 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-172">If you opted to choose specific locations, select the locations for your DLP policy, and then choose **Next**.</span></span><br/><span data-ttu-id="eda04-173">![DLP 정책 위치](media/dlp-teams-selectlocationsnewpolicy.png)</span><span class="sxs-lookup"><span data-stu-id="eda04-173">![DLP policy locations](media/dlp-teams-selectlocationsnewpolicy.png)</span></span><br/>
    > [!NOTE]
    > <span data-ttu-id="eda04-174">중요 한 정보가 포함 된 문서가 잘못 공유 되지 않도록 하려면 **팀 채팅 및 채널 메시지**와 함께 **SharePoint 사이트** 와 **OneDrive 계정이** 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-174">If you want to make sure documents that contain sensitive information are not shared inappropriately, make sure **SharePoint sites** and **OneDrive accounts** are turned on, along with **Teams chat and channel messages**.</span></span>
<br/>

6. <span data-ttu-id="eda04-175">**정책 설정** 탭의 **보호 하려는 콘텐츠 형식 사용자 지정**에서 기본 설정을 유지 하거나 **고급 설정 사용**을 선택 하 고 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-175">On the **Policy settings** tab, under **Customize the type of content you want to protect**, keep the default simple settings, or choose **Use advanced settings**, and then choose **Next**.</span></span> <span data-ttu-id="eda04-176">고급 설정을 선택 하는 경우 정책에 대 한 규칙을 만들거나 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-176">If you choose advanced settings, you can create or edit rules for your policy.</span></span> <span data-ttu-id="eda04-177">이에 대 한 도움말을 보려면 [단순 설정 및 고급 설정을](data-loss-prevention-policies.md#simple-settings-vs-advanced-settings)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eda04-177">(To get help with this, see [Simple settings vs. advanced settings](data-loss-prevention-policies.md#simple-settings-vs-advanced-settings).)</span></span>

7.  <span data-ttu-id="eda04-178">**정책 설정** 탭의 **중요 한 정보를 검색 하는 경우 어떤**작업을 수행 하 시겠습니까?에서 설정을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-178">On the **Policy settings** tab, under **What do you want to do if we detect sensitive info?**, review the settings.</span></span> <span data-ttu-id="eda04-179">(여기에서 기본 [정책 팁과 전자 메일 알림을](use-notifications-and-policy-tips.md)유지 하거나 사용자 지정할 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="eda04-179">(Here's where you can choose to keep default [policy tips and email notifications](use-notifications-and-policy-tips.md), or customize them.)</span></span><br/><span data-ttu-id="eda04-180">![팁 및 알림이 포함 된 DLP 정책 설정](media/dlp-teams-policysettings-tipsemails.png)</span><span class="sxs-lookup"><span data-stu-id="eda04-180">![DLP policy settings with tips and notifications](media/dlp-teams-policysettings-tipsemails.png)</span></span><br/><span data-ttu-id="eda04-181">설정 검토 또는 편집을 마친 후 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-181">When you're finished reviewing or editing settings, choose **Next**.</span></span>

8. <span data-ttu-id="eda04-182">**정책 설정** 탭의 정책을 **설정 하거나 먼저 테스트를 수행**하 시겠습니까?에서 정책을 켤 지, [먼저](data-loss-prevention-policies.md#roll-out-dlp-policies-gradually-with-test-mode)테스트를 시작할지, 지금은 해제를 선택 하 고 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-182">On the **Policy settings** tab, under **Do you want to turn on the policy or test things out first?**, choose whether to turn the policy on, [test it first](data-loss-prevention-policies.md#roll-out-dlp-policies-gradually-with-test-mode), or keep it turned off for now, and then choose **Next**.</span></span><br/><span data-ttu-id="eda04-183">![정책을 켤 지 여부를 지정 합니다.](media/dlp-teams-policysettings-turnonnow.png)</span><span class="sxs-lookup"><span data-stu-id="eda04-183">![Specify whether to turn the policy on](media/dlp-teams-policysettings-turnonnow.png)</span></span><br/>

9. <span data-ttu-id="eda04-184">**설정 검토** 탭에서 새 정책에 대 한 설정을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-184">On the **Review your settings** tab, review the settings for your new policy.</span></span> <span data-ttu-id="eda04-185">**편집** 을 선택 하 여 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-185">Choose **Edit** to make changes.</span></span> <span data-ttu-id="eda04-186">작업이 완료 되 면 **만들기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-186">When you're finished, choose **Create**.</span></span> 

<span data-ttu-id="eda04-187">새 정책이 데이터 센터를 통해 작동 하 고 사용자 계정과 동기화 되도록 약 1 시간을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda04-187">Allow approximately one hour for your new policy to work its way through your data center and sync to user accounts.</span></span>

## <a name="related-articles"></a><span data-ttu-id="eda04-188">관련 문서</span><span class="sxs-lookup"><span data-stu-id="eda04-188">Related articles</span></span>

[<span data-ttu-id="eda04-189">DLP 정책 만들기, 테스트 및 조정</span><span class="sxs-lookup"><span data-stu-id="eda04-189">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)

[<span data-ttu-id="eda04-190">DLP 정책에 대한 전자 메일 알림 보내기 및 정책 팁 표시</span><span class="sxs-lookup"><span data-stu-id="eda04-190">Send email notifications and show policy tips for DLP policies</span></span>](use-notifications-and-policy-tips.md)
