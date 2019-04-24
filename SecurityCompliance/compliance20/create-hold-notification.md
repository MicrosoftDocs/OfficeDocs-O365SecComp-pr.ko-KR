---
title: 법적 보존 알림 만들기
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
ms.openlocfilehash: acfa0c635b361426542e91a55c8d75c315bfb831
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242811"
---
# <a name="create-a-legal-hold-notice"></a><span data-ttu-id="bab5a-102">법적 보존 알림 만들기</span><span class="sxs-lookup"><span data-stu-id="bab5a-102">Create a legal hold notice</span></span>

<span data-ttu-id="bab5a-103">조직에서는 Advanced eDiscovery (Preview) custodian 통신을 사용 하 여 custodians와 통신 하는 방법에 대 한 워크플로를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-103">Using Advanced eDiscovery (Preview) custodian communications, organizations can manage their workflow around communicating with custodians.</span></span> <span data-ttu-id="bab5a-104">합법적인 팀은 통신 도구를 통해 법적 보존 알림을 체계적으로 전송, 수집 및 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-104">Through the Communications tool, legal teams can systematically send, collect, and track legal hold notifications.</span></span> <span data-ttu-id="bab5a-105">또한 유연한 만들기 프로세스를 사용 하면 팀에서 custodians로 전송 되는 알림의 콘텐츠 및 보존 알림 워크플로를 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-105">The flexible creation process also allows teams to customize the hold notification workflow and the content in the notices sent to custodians.</span></span> 

![통신 페이지](../media/CommunicationPage.PNG)

<span data-ttu-id="bab5a-107">이 문서에서는 보류 알림 워크플로의 단계를 간략하게 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-107">The article outlines the steps in the hold notification workflow.</span></span>

## <a name="step-1-specify-communication-details"></a><span data-ttu-id="bab5a-108">1 단계: 통신 정보 지정</span><span class="sxs-lookup"><span data-stu-id="bab5a-108">Step 1: Specify communication details</span></span>

<span data-ttu-id="bab5a-109">첫 번째 단계는 법적 보존 공지와 기타 custodian 통신에 대 한 적절 한 세부 정보를 지정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-109">The first step is to specify the appropriate details for legal hold notices or other custodian communications.</span></span> 

![이름 통신 페이지](../media/NameCommunication.PNG)

1. <span data-ttu-id="bab5a-111">보안 & 준수 센터에서 **eDiscovery > Advanced eDiscovery (Preview)** 로 이동 하 여 조직의 사례 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-111">In the Security & Compliance Center, go to **eDiscovery > Advanced eDiscovery (Preview)** to display the list of cases in your organization.</span></span>
   
2. <span data-ttu-id="bab5a-112">**통신** 탭을 클릭 한 다음 **새 통신**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-112">Click the **Communications** tab, and then click **New communication**.</span></span>
   
3. <span data-ttu-id="bab5a-113">**이름 통신** 페이지에서 다음 (필수) 통신 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-113">On the **Name communication** page, specify the following (required) communication details.</span></span>

    - <span data-ttu-id="bab5a-114">**Name**: 통신의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-114">**Name**: This is the name for the communication.</span></span>
    
    - <span data-ttu-id="bab5a-115">**발급**관리자: 드롭다운 목록에 사례 구성원 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-115">**Issuing officer**: The dropdown list displays a list of a case members.</span></span> <span data-ttu-id="bab5a-116">custodians로 전송 되는 각 알림은 지정 된 발급 관리자를 대신 하 여 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-116">Each notice sent to custodians will be sent on behalf of the specified issuing officer.</span></span>

4. <span data-ttu-id="bab5a-117">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-117">Click **Next**.</span></span>

## <a name="step-2-define-the-portal-content"></a><span data-ttu-id="bab5a-118">2 단계: 포털 콘텐츠 정의</span><span class="sxs-lookup"><span data-stu-id="bab5a-118">Step 2: Define the portal content</span></span>

<span data-ttu-id="bab5a-119">다음으로 보류 공지의 내용을 만들고 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-119">Next, you can create and add the content of the hold notice.</span></span> <span data-ttu-id="bab5a-120">**통신 만들기** 마법사의 **포털 콘텐츠 정의** 페이지에서 보류 주의 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-120">On the **Define portal content** page in the **Create communication** wizard, specify the contents of the hold notice.</span></span> <span data-ttu-id="bab5a-121">이 콘텐츠는 발급, 다시 발급, 미리 알림 및 에스컬레이션 공지에 자동으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-121">This content will be automatically appended to the Issuance, Re-Issue, Reminder, and Escalation notices.</span></span> <span data-ttu-id="bab5a-122">또한이 콘텐츠는 custodian의 준수 포털에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-122">Additionally, this content will appear in the custodian's Compliance Portal.</span></span> 

![포털 콘텐츠 페이지](../media/PortalContent.PNG)

<span data-ttu-id="bab5a-124">포털 콘텐츠를 만들려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-124">To create the portal content:</span></span>

1. <span data-ttu-id="bab5a-125">포털 콘텐츠의 텍스트 상자에 입력 하거나 다른 문서에서 잘라내어 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-125">Type (or cut and paste from another document) your hold notice in the textbox for the portal content.</span></span> 

2. <span data-ttu-id="bab5a-126">공지 사항에 merge 변수를 삽입 하 여 공지를 사용자 지정 하 고 Custodian 준수 포털을 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-126">Insert merge variables into your notice to customize the notice and share the Custodian Compliance Portal.</span></span>

3. <span data-ttu-id="bab5a-127">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-127">Click **Next**.</span></span>

  >[!Tip]
  ><span data-ttu-id="bab5a-128">포털 콘텐츠의 콘텐츠 및 형식을 사용자 지정 하는 방법에 대 한 자세한 내용은 [통신 편집기 사용](using-communications-editor.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bab5a-128">To learn more about how to can customize the content and format of the portal content, see [Use the Communications Editor](using-communications-editor.md).</span></span>

## <a name="step-3-set-the-required-notifications"></a><span data-ttu-id="bab5a-129">3 단계: 필요한 알림 설정</span><span class="sxs-lookup"><span data-stu-id="bab5a-129">Step 3: Set the required notifications</span></span>

<span data-ttu-id="bab5a-130">보존 공지의 내용을 정의한 후에는 알림 프로세스를 보내고 관리 하는 방법에 대 한 워크플로를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-130">After you've defined the contents of the hold notice, you can set up the workflows around sending and managing the notification process.</span></span> <span data-ttu-id="bab5a-131">알림은 custodians을 사용 하 여 알림 및 추가 작업으로 전송 되는 전자 메일 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-131">Notifications are email messages that are sent to notify and follow-up with custodians.</span></span> <span data-ttu-id="bab5a-132">통신에 추가 되는 모든 custodian에는 동일한 알림이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-132">Every custodian added to the communication will receive the same notification.</span></span> 

<span data-ttu-id="bab5a-133">보류 알림을 설정 하 고 보내려면 발급, 다시 발급, 릴리스 알림 등을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-133">To set up and send a hold notice, you must include Issuance, Re-Issuance, and Release notifications.</span></span>

### <a name="issuance-notification"></a><span data-ttu-id="bab5a-134">발급 알림</span><span class="sxs-lookup"><span data-stu-id="bab5a-134">Issuance notification</span></span> 

<span data-ttu-id="bab5a-135">통신을 만든 후에는 지정 된 발급 담당자가 **발급 알림을** 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-135">After the communication is created, the **Issuance Notification** is initiated by the specified Issuing Officer.</span></span> <span data-ttu-id="bab5a-136">이 발급 알림은 사용자에 게 보존 의무를 알리기 위해 custodian로 전송 되는 첫 번째 통신입니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-136">The Issuance notification is the first communication sent to the custodian to inform them about their preservation obligations.</span></span> 

<span data-ttu-id="bab5a-137">발급 알림을 만들려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-137">To create an issuance notification:</span></span>

1. <span data-ttu-id="bab5a-138">**발급** 타일에서 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-138">In the **Issuance** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="bab5a-139">필요한 경우 **참조** 및 **숨은** 참조 필드에 추가 사례 구성원 또는 직원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-139">If necessary, add additional case members or staff to the **Cc** and **Bcc** fields.</span></span> <span data-ttu-id="bab5a-140">이러한 필드에 여러 사용자를 추가 하려면 전자 메일 주소를 세미콜론으로 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-140">To add multiple users to these fields, separate email addresses with a semi-colon.</span></span>
   
3. <span data-ttu-id="bab5a-141">알림의 **제목을** 지정 합니다 (필수).</span><span class="sxs-lookup"><span data-stu-id="bab5a-141">Specify the **Subject** for the notice (required).</span></span>
   
4. <span data-ttu-id="bab5a-142">custodian에 제공할 콘텐츠 또는 추가 지침을 지정 합니다 (필수).</span><span class="sxs-lookup"><span data-stu-id="bab5a-142">Specify the contents or additional instructions that you would like to provide to the custodian (required).</span></span> <span data-ttu-id="bab5a-143">2 단계에서 정의한 포털 콘텐츠가 발급 알림의 끝에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-143">Note that the portal content you defined in Step 2 is added to the end of the issuance notice.</span></span> 
   
5. <span data-ttu-id="bab5a-144">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-144">Click **Save**</span></span> 

### <a name="re-issuance-notification"></a><span data-ttu-id="bab5a-145">재발급 알림</span><span class="sxs-lookup"><span data-stu-id="bab5a-145">Re-Issuance notification</span></span> 

<span data-ttu-id="bab5a-146">사례가 진행 됨에 따라 custodians는 이전에 지시 된 것 보다 더 많은 데이터를 보존 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-146">As the case progresses, custodians may be required to preserve additional or less data than was previously instructed.</span></span> <span data-ttu-id="bab5a-147">보존 공지의 내용을 업데이트 한 후에는 재 발급 알림을 통해 custodians에 게 보존 의무 변경 사항에 대 한 알림이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-147">After you update the contents of the hold notice, the re-issuance notification alerts the  custodians about the changes to their preservation obligations.</span></span>

<span data-ttu-id="bab5a-148">재 발급 알림을 만들려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-148">To create a re-issuance notification:</span></span> 

1. <span data-ttu-id="bab5a-149">**재발급** 타일에서 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-149">In the **Reissue** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="bab5a-150">필요한 경우 **참조** 및 **숨은** 참조 필드에 추가 사례 구성원 또는 직원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-150">If necessary, add additional case members or staff to the **Cc** and **Bcc** fields.</span></span> <span data-ttu-id="bab5a-151">이러한 필드에 여러 사용자를 추가 하려면 전자 메일 주소를 세미콜론으로 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-151">To add multiple users to these fields, separate email addresses with a semi-colon.</span></span>
   
3. <span data-ttu-id="bab5a-152">알림의 **제목을** 지정 합니다 (필수).</span><span class="sxs-lookup"><span data-stu-id="bab5a-152">Specify the **Subject** for the notice (required).</span></span>
   
4. <span data-ttu-id="bab5a-153">custodian에 제공할 콘텐츠 또는 추가 지침을 지정 합니다 (필수).</span><span class="sxs-lookup"><span data-stu-id="bab5a-153">Specify the contents or additional instructions that you would like to provide to the custodian (required).</span></span> <span data-ttu-id="bab5a-154">2 단계에서 정의한 포털 콘텐츠가 재발급 공지의 끝에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-154">Note that the portal content you defined in Step 2 is added to the end of the re-issuance notice.</span></span>
   
5. <span data-ttu-id="bab5a-155">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-155">Click **Save**.</span></span>

>[!Note]
><span data-ttu-id="bab5a-156">보존 알림을 수정 하면 재 발급 알림이 해당 공지에 할당 된 모든 custodians 자동으로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-156">If a hold notification is modified, the re-issuance notification will be automatically sent to all custodians assigned to the notice.</span></span> <span data-ttu-id="bab5a-157">알림을 보낸 후에는 custodians에 게 해당 보존 알림을 다시 승인할 것인지 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-157">After the notification is sent, custodians will be asked to re-acknowledge their hold notice.</span></span> <span data-ttu-id="bab5a-158">미리 알림 또는 단계적 워크플로를 설정한 경우에도 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-158">If you have set up any reminder or escalation workflows, these will also re-start.</span></span> 

### <a name="release-notification"></a><span data-ttu-id="bab5a-159">릴리스 알림</span><span class="sxs-lookup"><span data-stu-id="bab5a-159">Release notification</span></span>

<span data-ttu-id="bab5a-160">문제가 해결 된 후 또는 custodian이 더 이상 콘텐츠를 보존 하지 않는 경우 사례에서 custodian를 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-160">After a matter is resolved or if a custodian is no longer subject to preserve content, you can release the custodian from a case.</span></span> <span data-ttu-id="bab5a-161">이전에 custodian에서 보류 알림을 발급 한 경우 릴리스 알림을 사용 하 여 custodians에 게 해당 의무에서 출시 되었음을 알릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-161">If the custodian was previously issued a hold notice, the release notification can be used to alert custodians that they have been released from their obligation.</span></span>

<span data-ttu-id="bab5a-162">릴리스 알림을 만들려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-162">To create a release notification:</span></span> 

1. <span data-ttu-id="bab5a-163">**릴리스** 타일에서 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-163">In the **Release** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="bab5a-164">필요한 경우 **참조** 및 **숨은** 참조 필드에 추가 사례 구성원 또는 직원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-164">If necessary, add additional case members or staff to the **Cc** and **Bcc** fields.</span></span> <span data-ttu-id="bab5a-165">이러한 필드에 여러 사용자를 추가 하려면 전자 메일 주소를 세미콜론으로 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-165">To add multiple users to these fields, separate email addresses with a semi-colon.</span></span>
   
3. <span data-ttu-id="bab5a-166">알림의 **제목을** 지정 합니다 (필수).</span><span class="sxs-lookup"><span data-stu-id="bab5a-166">Specify the **Subject** for the notice (required).</span></span>
   
4. <span data-ttu-id="bab5a-167">custodian에 제공할 콘텐츠 또는 추가 지침을 지정 합니다 (필수).</span><span class="sxs-lookup"><span data-stu-id="bab5a-167">Specify the contents or additional instructions that you would like to provide to the custodian (required).</span></span>
   
5. <span data-ttu-id="bab5a-168">**저장** 을 클릭 하 고 다음 단계로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-168">Click **Save** and go to the next step.</span></span> 

## <a name="optional-step-4-set-the-optional-notifications"></a><span data-ttu-id="bab5a-169">반드시 4 단계: 선택적 알림 설정</span><span class="sxs-lookup"><span data-stu-id="bab5a-169">(Optional) Step 4: Set the optional notifications</span></span>

<span data-ttu-id="bab5a-170">선택적으로 자동화 된 미리 알림 및 에스컬레이션 알림을 만들고 예약 하 여 응답 하지 않는 custodians를 포함 하도록 워크플로를 단순화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-170">Optionally, you can simplify the workflow for following up with unresponsive custodians by creating and scheduling automated reminder and escalation notifications.</span></span>

![미리 알림/에스컬레이션 페이지](../media/ReminderEscalations.PNG)

### <a name="reminders"></a><span data-ttu-id="bab5a-172">기한이</span><span class="sxs-lookup"><span data-stu-id="bab5a-172">Reminders</span></span>

<span data-ttu-id="bab5a-173">보류 알림을 보낸 후에는 미리 알림 워크플로를 정의 하 여 응답 하지 않는 custodians를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-173">After you have sent a hold notification, you can follow-up with unresponsive custodians by defining a reminder workflow.</span></span> 

<span data-ttu-id="bab5a-174">미리 알림을 예약 하려면:</span><span class="sxs-lookup"><span data-stu-id="bab5a-174">To schedule reminders:</span></span>

1. <span data-ttu-id="bab5a-175">**미리 알림** 타일에서 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-175">In the **Reminder** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="bab5a-176">**상태** 전환 (필수)을 설정 하 여 **미리 알림** 워크플로를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-176">Enable the **Reminder** workflow by turning on the **Status** toggle (required).</span></span>
   
3. <span data-ttu-id="bab5a-177">**미리 알림 간격 (일)** 을 지정 합니다 (필수).</span><span class="sxs-lookup"><span data-stu-id="bab5a-177">Specify the **Reminder interval (in days)** (required).</span></span> <span data-ttu-id="bab5a-178">다음은 첫 번째 및 후속 미리 알림 알림을 보내기 전까지 기다릴 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-178">This is the number of days to wait before sending the first and follow-up reminder notifications.</span></span> <span data-ttu-id="bab5a-179">예를 들어 미리 알림 간격을 7 일로 설정한 경우 처음 알림을 처음에 발급 한 후 7 일 후에 첫 번째 미리 알림이 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-179">For example, if you set the reminder interval to 7 days, then the first reminder would be sent 7 days after the hold notification was initially issued.</span></span> <span data-ttu-id="bab5a-180">이후의 모든 미리 알림도 7 일 마다 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-180">All subsequent reminders would also be sent every 7 days.</span></span>
   
4. <span data-ttu-id="bab5a-181">**미리 알림 개수** 를 지정 합니다 (필수).</span><span class="sxs-lookup"><span data-stu-id="bab5a-181">Specify the **Number of reminders** (required).</span></span> <span data-ttu-id="bab5a-182">이 필드는 응답 하지 않는 custodians 보낼 미리 알림 개수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-182">This field specifies how many reminders to send to un-responsive custodians.</span></span> <span data-ttu-id="bab5a-183">예를 들어 미리 알림 수를 3으로 설정 하는 경우 custodian에 미리 알림이 최대 3 개 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-183">For example, if you set the number of reminders to 3, then a custodian would receive a maximum of 3 reminders.</span></span> <span data-ttu-id="bab5a-184">custodian가 보존 알림을 승인 하면 미리 알림이 해당 사용자에 게 더 이상 전송 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-184">After a custodian acknowledges the hold notification, reminders will no longer be sent to that user.</span></span>
   
5. <span data-ttu-id="bab5a-185">알림의 **제목을** 지정 합니다 (필수).</span><span class="sxs-lookup"><span data-stu-id="bab5a-185">Specify the **Subject** for the notice (required).</span></span> 
   
6. <span data-ttu-id="bab5a-186">custodian에 제공할 콘텐츠 또는 추가 지침을 지정 합니다 (필수).</span><span class="sxs-lookup"><span data-stu-id="bab5a-186">Specify the contents or additional instructions that you would like to provide to the custodian (required).</span></span> <span data-ttu-id="bab5a-187">2 단계에서 정의한 포털 콘텐츠가 미리 알림 알림의 끝에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-187">Note that the portal content you defined in Step 2 is added to the end of the reminder notice.</span></span>
   
7. <span data-ttu-id="bab5a-188">**저장** 을 클릭 하 고 다음 단계를 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-188">Click **Save** and go the the next step.</span></span>

### <a name="escalations"></a><span data-ttu-id="bab5a-189">에스컬레이션이</span><span class="sxs-lookup"><span data-stu-id="bab5a-189">Escalations</span></span> 

<span data-ttu-id="bab5a-190">경우에 따라 응답 하지 않는 custodians 추가 작업을 수행 해야 하는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-190">In some situations, you may need additional ways to follow-up with unresponsive custodians.</span></span> <span data-ttu-id="bab5a-191">custodian에서 지정 된 미리 알림 개수를 받은 후 보류 알림을 승인 하지 않으면 법적 팀이 워크플로를 지정 하 여 custodian 및 해당 관리자에 게 단계적으로 공지 알림을 보내도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-191">If a custodian doesn't acknowledge a hold notification after receiving the specified number of reminders, the legal team can specify a workflow to automatically send an escalation notice to the custodian and their manager.</span></span>

<span data-ttu-id="bab5a-192">에스컬레이션을 예약 하려면</span><span class="sxs-lookup"><span data-stu-id="bab5a-192">To schedule escalations:</span></span>

1. <span data-ttu-id="bab5a-193">**에스컬레이션** 타일에서 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-193">In the **Escalation** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="bab5a-194">**상태** 전환 기능을 설정 하 여 **에스컬레이션** 워크플로를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-194">Enable the **Escalation** workflow by turning on the **Status** toggle.</span></span>
   
3. <span data-ttu-id="bab5a-195">**에스컬레이션 간격 (일)** 을 지정 합니다 (필수).</span><span class="sxs-lookup"><span data-stu-id="bab5a-195">Specify the **Escalation interval (in days)** (required).</span></span> 
   
4. <span data-ttu-id="bab5a-196">**에스컬레이션 수** (필수)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-196">Specify the **Number of escalations** (required).</span></span> <span data-ttu-id="bab5a-197">이 필드는 응답 하지 않는 custodians 보낼 에스컬레이션 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-197">This field specifies how many escalations to send to un-responsive custodians.</span></span> <span data-ttu-id="bab5a-198">예를 들어 에스컬레이션 수를 3으로 설정 하는 경우 에스컬레이션 알림이 custodian로 전송 되 고 관리자에 게 최대 3 회 보내집니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-198">For example, if you set the number of escalations to 3, then an escalation notice would be sent to the custodian and their manager a maximum of 3 times.</span></span> <span data-ttu-id="bab5a-199">custodian가 보존 알림을 승인 하면 에스컬레이션이 더 이상 전송 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-199">After a custodian acknowledges the hold notification, escalations will no longer be sent.</span></span> 
   
5. <span data-ttu-id="bab5a-200">알림의 **제목을** 지정 합니다 (필수).</span><span class="sxs-lookup"><span data-stu-id="bab5a-200">Specify the **Subject** for the notice (required).</span></span> 
   
6. <span data-ttu-id="bab5a-201">custodian에 제공할 콘텐츠 또는 추가 지침을 지정 합니다 (필수).</span><span class="sxs-lookup"><span data-stu-id="bab5a-201">Specify the contents or additional instructions that you would like to provide to the custodian (required).</span></span> <span data-ttu-id="bab5a-202">2 단계에서 정의한 포털 콘텐츠가 에스컬레이션 알림의 끝에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-202">Note that the portal content you defined in Step 2 is added to the end of the escalation notice.</span></span>
   
7. <span data-ttu-id="bab5a-203">**저장** 을 클릭 하 고 다음 단계를 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-203">Click **Save** and go the the next step.</span></span>
   
## <a name="step-5-assign-custodians"></a><span data-ttu-id="bab5a-204">5 단계: custodians 할당</span><span class="sxs-lookup"><span data-stu-id="bab5a-204">Step 5: Assign custodians</span></span> 

<span data-ttu-id="bab5a-205">알림의 콘텐츠를 완성 한 후에는 알림을 보낼 custodians을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-205">After you have finalized the content for notifications, select the custodians that you would like to send the notifications.</span></span> 

![Custodians 선택 페이지](../media/SelectCustodians.PNG)

<span data-ttu-id="bab5a-207">custodians를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="bab5a-207">To add custodians:</span></span>

1. <span data-ttu-id="bab5a-208">이름 옆에 있는 확인란을 클릭 하 여 통신에 custodians를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-208">Assign custodians to the communication by clicking the checkbox next to their name.</span></span>

    <span data-ttu-id="bab5a-209">통신을 만든 후에는 알림 워크플로가 선택한 custodians에 자동으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-209">After the communication is created, the notification workflow will automatically apply to the selected custodians.</span></span>
   
2. <span data-ttu-id="bab5a-210">**다음** 을 클릭 하 여 통신 설정 및 세부 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-210">Click **Next** to review the communication settings and details.</span></span>
 
>[!NOTE]
><span data-ttu-id="bab5a-211">사례에 추가 된 custodians 및 사례 내에서 다른 알림을 보내지 않은 사용자만 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-211">You can only add custodians who have been added to the case and haven't been sent another notification within the case.</span></span>

## <a name="step-6-review-settings"></a><span data-ttu-id="bab5a-212">6 단계: 설정 검토</span><span class="sxs-lookup"><span data-stu-id="bab5a-212">Step 6: Review settings</span></span>

<span data-ttu-id="bab5a-213">설정을 검토 하 고 **보내기를** 클릭 하 여 통신을 완료 하면 시스템에서 발급 알림을 보내 통신 워크플로를 자동으로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bab5a-213">After you review the settings and click **Send** to complete the communication, the system will automatically start the communication workflow by sending the issuance notice.</span></span>
