---
title: 법적 보유 알림 만들기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 8db5a21f60a1d73c11e28bc2765a95c23646115d
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706079"
---
# <a name="create-a-legal-hold-notice"></a><span data-ttu-id="692cb-102">법적 보유 알림 만들기</span><span class="sxs-lookup"><span data-stu-id="692cb-102">Create a legal hold notice</span></span>

<span data-ttu-id="692cb-p101">고급 eDiscovery (미리 보기) 더불어 통신을 사용 하 여, 조직에서는 custodians와의 통신 주위가 워크플로 관리할 수 있습니다. 통신 도구를 통해 법적 팀 수 체계적으로 보내기, 수집 및 법적 보유 알림을 추적 합니다. 유연한 만들기 프로세스에는 팀을 보류 알림 워크플로 custodians에 보내는 알림 메시지의 콘텐츠를 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p101">Using Advanced eDiscovery (Preview) custodian communications, organizations can manage their workflow around communicating with custodians. Through the Communications tool, legal teams can systematically send, collect, and track legal hold notifications. The flexible creation process also allows teams to customize the hold notification workflow and the content in the notices sent to custodians.</span></span> 

<span data-ttu-id="692cb-106">문서에서 보류 알림 워크플로 단계를 간략히 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-106">The article outlines the steps in the hold notification workflow.</span></span>

## <a name="step-1-specify-communication-details"></a><span data-ttu-id="692cb-107">1 단계: 통신 세부 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-107">Step 1: Specify communication details</span></span>

<span data-ttu-id="692cb-108">첫번째 단계에서는 법적 보유 통지에 대 한 적절 한 세부 정보 또는 기타 더불어 통신을 지정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-108">The first step is to specify the appropriate details for legal hold notices or other custodian communications.</span></span> 

1. <span data-ttu-id="692cb-109">보안 & 준수 센터에서에서 조직에 사례의 목록을 표시 하려면 **eDiscovery gt_ 고급 eDiscovery (미리 보기)** 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-109">In the Security & Compliance Center, go to **eDiscovery > Advanced eDiscovery (Preview)** to display the list of cases in your organization.</span></span>
   
2. <span data-ttu-id="692cb-110">**통신** 탭을 클릭 한 다음 **새 통신**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-110">Click the **Communications** tab, and then click **New communication**.</span></span>
   
3. <span data-ttu-id="692cb-111">**이름 통신** 페이지에서 다음 (필수) 통신 세부 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-111">On the **Name communication** page, specify the following (required) communication details.</span></span>

    - <span data-ttu-id="692cb-112">**이름**: 통신에 대 한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-112">**Name**: This is the name for the communication.</span></span>
    
    - <span data-ttu-id="692cb-p102">**발급 하는 담당자가**: 사례 구성원 목록을 표시 하는 드롭다운 목록입니다. Custodians로 전송 하는 각 통지 지정한 발급 책임자를 대신 하 여 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p102">**Issuing officer**: The dropdown list displays a list of a case members. Each notice sent to custodians will be sent on behalf of the specified issuing officer.</span></span>

4. <span data-ttu-id="692cb-115">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-115">Click **Next**.</span></span>

## <a name="step-2-define-the-portal-content"></a><span data-ttu-id="692cb-116">2 단계: 포털 콘텐츠를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-116">Step 2: Define the portal content</span></span>

<span data-ttu-id="692cb-p103">다음으로 만들 수 있으며, 보류 알림의 콘텐츠를 추가. **Create 통신** 마법사에서 **정의 포털 콘텐츠** 페이지에서 보류 주의 표시의 내용을 지정 합니다. 이 콘텐츠는 발급, 다시 실행, 알림 및 에스컬레이션 통지를 자동으로 추가 됩니다. 또한이 콘텐츠는 더불어의 규정 준수 포털에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p103">Next, you can create and add the content of the hold notice. On the **Define portal content** page in the **Create communication** wizard, specify the contents of the hold notice. This content will be automatically appended to the Issuance, Re-Issue, Reminder, and Escalation notices. Additionally, this content will appear in the custodian's Compliance Portal.</span></span> 

<span data-ttu-id="692cb-121">포털 콘텐츠를 만들려면:</span><span class="sxs-lookup"><span data-stu-id="692cb-121">To create the portal content:</span></span>

1. <span data-ttu-id="692cb-122">유형 (또는 잘라내기 및 다른 문서에서 paster) 보류 상태가 포털 콘텐츠를 위한 텍스트 상자에 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-122">Type (or cut and paster from another document) your hold notice in the textbox for the portal content.</span></span> 

2. <span data-ttu-id="692cb-123">해당 통지를 사용자 지정 하 고 더불어 준수 포털을 공유 하 여 통지에 병합 변수를 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-123">Insert merge variables into your notice to customize the notice and share the Custodian Compliance Portal.</span></span>

3. <span data-ttu-id="692cb-124">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-124">Click **Next**.</span></span>

  >[!Tip]
  ><span data-ttu-id="692cb-125">포털 콘텐츠 형식과 콘텐츠를 사용자 지정할 수 하는 방법에 대 한 자세한 내용을 보려면, [통신 편집기 사용](using-communications-editor.md)을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-125">To learn more about how to can customize the content and format of the portal content, see [Use the Communications Editor](using-communications-editor.md).</span></span>

## <a name="step-3-set-the-required-notifications"></a><span data-ttu-id="692cb-126">3 단계: 필요한 알림 설정</span><span class="sxs-lookup"><span data-stu-id="692cb-126">Step 3: Set the required notifications</span></span>

<span data-ttu-id="692cb-p104">보류 주의 표시의 내용을 정의한 후 중심으로 보내는 알림 프로세스를 관리 및 워크플로 설정할 수 있습니다. 알림은 알리도록 전송 되는 전자 메일 메시지와 함께 custodians 사후 점검 합니다. 통신에 추가 된 모든 더불어 같은 알림을 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p104">After you've defined the contents of the hold notice, you can set up the workflows around sending and managing the notification process. Notifications are email messages that are sent to notify and follow-up with custodians. Every custodian added to the communication will receive the same notification.</span></span> 

<span data-ttu-id="692cb-130">설정 하 고 대기 알림을 보내, 발급, Re-발급을 포함 하 고 알림을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-130">To set up and send a hold notice, you must include Issuance, Re-Issuance, and Release notifications.</span></span>

### <a name="issuance-notification"></a><span data-ttu-id="692cb-131">발급 알림</span><span class="sxs-lookup"><span data-stu-id="692cb-131">Issuance notification</span></span> 

<span data-ttu-id="692cb-p105">통신을 만든 후 **발급 알림** 는 지정 된 발급 담당자가 시작 됩니다. 발급 알림 더불어 자신의 보존 의무 하는 방법에 대 한 알리고로 전송 하는 첫번째 통신입니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p105">After the communication is created, the **Issuance Notification** is initiated by the specified Issuing Officer. The Issuance notification is the first communication sent to the custodian to inform them about their preservation obligations.</span></span> 

<span data-ttu-id="692cb-134">발급 알림 만들기:</span><span class="sxs-lookup"><span data-stu-id="692cb-134">To create an issuance notification:</span></span>

1. <span data-ttu-id="692cb-135">**발급** 타일에서 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-135">In the **Issuance** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="692cb-p106">필요한 경우, **참조** 및 **숨은 참조** 필드에 추가 사례 구성원 또는 직원을 추가 합니다. 이러한 필드에 여러 사용자를 추가 하려면 전자 메일 주소를 세미콜론으로 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p106">If necessary, add additional case members or staff to the **Cc** and **Bcc** fields. To add multiple users to these fields, separate email addresses with a semi-colon.</span></span>
   
3. <span data-ttu-id="692cb-138">**제목** 에 대 한 (필수) 통지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-138">Specify the **Subject** for the notice (required).</span></span>
   
4. <span data-ttu-id="692cb-p107">내용이 나 더불어 (필수)에 게 제공 하려는 추가 지침을 지정 합니다. 2 단계에서에서 정의 된 포털 콘텐츠 발급 주의 표시의 끝에 추가 되는 note 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p107">Specify the contents or additional instructions that you would like to provide to the custodian (required). Note that the portal content you defined in Step 2 is added to the end of the issuance notice.</span></span> 
   
5. <span data-ttu-id="692cb-141">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-141">Click **Save**</span></span> 

### <a name="re-issuance-notification"></a><span data-ttu-id="692cb-142">다시 발급 알림</span><span class="sxs-lookup"><span data-stu-id="692cb-142">Re-Issuance notification</span></span> 

<span data-ttu-id="692cb-p108">사례 진행 됨에 따라 custodians 이전에 지시 된 것 보다 추가 또는 데이터를 유지 하기 위해 필요할 수 있습니다. 보류 주의 표시의 내용을 업데이트 한 후 다시 발급 알림 custodians를 자신의 보존 의무를 변경 하는 방법에 대 한 경고를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p108">As the case progresses, custodians may be required to preserve additional or less data than was previously instructed. After you update the contents of the hold notice, the re-issuance notification alerts the  custodians about the changes to their preservation obligations.</span></span>

<span data-ttu-id="692cb-145">다시 발급 알림 만들기:</span><span class="sxs-lookup"><span data-stu-id="692cb-145">To create a re-issuance notification:</span></span> 

1. <span data-ttu-id="692cb-146">**다시 실행 하십시오** 타일에서 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-146">In the **Reissue** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="692cb-p109">필요한 경우, **참조** 및 **숨은 참조** 필드에 추가 사례 구성원 또는 직원을 추가 합니다. 이러한 필드에 여러 사용자를 추가 하려면 전자 메일 주소를 세미콜론으로 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p109">If necessary, add additional case members or staff to the **Cc** and **Bcc** fields. To add multiple users to these fields, separate email addresses with a semi-colon.</span></span>
   
3. <span data-ttu-id="692cb-149">**제목** 에 대 한 (필수) 통지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-149">Specify the **Subject** for the notice (required).</span></span>
   
4. <span data-ttu-id="692cb-p110">내용이 나 더불어 (필수)에 게 제공 하려는 추가 지침을 지정 합니다. Note 된 2 단계에서에서 정의 된 포털 콘텐츠를 다시 발급 표시의 끝에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p110">Specify the contents or additional instructions that you would like to provide to the custodian (required). Note that the portal content you defined in Step 2 is added to the end of the re-issuance notice.</span></span>
   
5. <span data-ttu-id="692cb-152">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-152">Click **Save**.</span></span>

>[!Note]
><span data-ttu-id="692cb-p111">보류 알림 수정 되 면 다시 발급 알림, 알림을에 할당 된 모든 custodians에 자동으로 전송 됩니다. 알림을 보낸 후 custodians 묻는 메시지가 나타납니다를 다시 자신의 보류 주의 표시를 확인 합니다. 미리 알림 또는 에스컬레이션 워크플로 설정 하는 경우 이러한도 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p111">If a hold notification is modified, the re-issuance notification will be automatically sent to all custodians assigned to the notice. After the notification is sent, custodians will be asked to re-acknowledge their hold notice. If you have set up any reminder or escalation workflows, these will also re-start.</span></span> 

### <a name="release-notification"></a><span data-ttu-id="692cb-156">릴리스 알림</span><span class="sxs-lookup"><span data-stu-id="692cb-156">Release notification</span></span>

<span data-ttu-id="692cb-p112">문제를 해결 한 후 또는 더불어 더이상 적용 하는 경우 콘텐츠 보존, 사례에서 더불어를 해제할 수 없습니다. 더불어 보류 알림을 이전에 게시 하는 경우 릴리스 알림 자신의 의무에서 발표 된 custodians 경고 메시지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p112">After a matter is resolved or if a custodian is no longer subject to preserve content, you can release the custodian from a case. If the custodian was previously issued a hold notice, the release notification can be used to alert custodians that they have been released from their obligation.</span></span>

<span data-ttu-id="692cb-159">릴리스 알림 만들기:</span><span class="sxs-lookup"><span data-stu-id="692cb-159">To create a release notification:</span></span> 

1. <span data-ttu-id="692cb-160">**릴리스** 타일에서 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-160">In the **Release** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="692cb-p113">필요한 경우, **참조** 및 **숨은 참조** 필드에 추가 사례 구성원 또는 직원을 추가 합니다. 이러한 필드에 여러 사용자를 추가 하려면 전자 메일 주소를 세미콜론으로 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p113">If necessary, add additional case members or staff to the **Cc** and **Bcc** fields. To add multiple users to these fields, separate email addresses with a semi-colon.</span></span>
   
3. <span data-ttu-id="692cb-163">**제목** 에 대 한 (필수) 통지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-163">Specify the **Subject** for the notice (required).</span></span>
   
4. <span data-ttu-id="692cb-164">내용이 나 더불어 (필수)에 게 제공 하려는 추가 지침을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-164">Specify the contents or additional instructions that you would like to provide to the custodian (required).</span></span>
   
5. <span data-ttu-id="692cb-165">**저장** 을 클릭 하 고 단계로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-165">Click **Save** and go to the next step.</span></span> 

## <a name="optional-step-4-set-the-optional-notifications"></a><span data-ttu-id="692cb-166">(선택 사항) 4 단계: 선택적 알림 설정</span><span class="sxs-lookup"><span data-stu-id="692cb-166">(Optional) Step 4: Set the optional notifications</span></span>

<span data-ttu-id="692cb-167">필요에 따라 다음에 대 한 응답 하지 않는 custodians와 자동화 된 미리 알림 만들기 및 예약 및 에스컬레이션 하 여 알림 워크플로 간소화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-167">Optionally, you can simplify the workflow for following up with unresponsive custodians by creating and scheduling automated reminder and escalation notifications.</span></span>

### <a name="reminders"></a><span data-ttu-id="692cb-168">미리 알림</span><span class="sxs-lookup"><span data-stu-id="692cb-168">Reminders</span></span>

<span data-ttu-id="692cb-169">보류 알림을 보낸 후 수 사후 점검 응답 하지 않는 custodians 미리 알림 워크플로 정의 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-169">After you have sent a hold notification, you can follow-up with unresponsive custodians by defining a reminder workflow.</span></span> 

<span data-ttu-id="692cb-170">미리 알림 예약 하려면:</span><span class="sxs-lookup"><span data-stu-id="692cb-170">To schedule reminders:</span></span>

1. <span data-ttu-id="692cb-171">**미리 알림** 타일에서 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-171">In the **Reminder** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="692cb-172">(필수) 표시/숨기기 **상태** 를 설정 하 여 **미리 알림** 워크플로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-172">Enable the **Reminder** workflow by turning on the **Status** toggle (required).</span></span>
   
3. <span data-ttu-id="692cb-p114">**미리 알림 간격 (일)** (필수)를 지정 합니다. 첫번째와 후속 미리 알림을 보내기 전에 기다릴 날짜 수입니다. 예, 7 일이를 미리 알림 간격을 설정 하는 경우 다음 첫번째 미리 알림의 보낼 보류 알림을 처음 발급 한 후 7 일. 모든 후속 미리 7 일 마다 전송도 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p114">Specify the **Reminder interval (in days)** (required). This is the number of days to wait before sending the first and follow-up reminder notifications. For example, if you set the reminder interval to 7 days, then the first reminder would be sent 7 days after the hold notification was initially issued. All subsequent reminders would also be sent every 7 days.</span></span>
   
4. <span data-ttu-id="692cb-p115">**미리 알림 수** (필수)를 지정 합니다. 이 필드는 얼마나 많은 미리 응답 되지 않은 custodians를 보낼 수를 지정 합니다. 예 3 미리 알림 개수를 설정 하는 경우 다음을 더불어 수신 하 게 3 미리 최대 합니다. 한 더불어 승인 보류 알림, 후 미리 더이상 해당 사용자에 게 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p115">Specify the **Number of reminders** (required). This field specifies how many reminders to send to un-responsive custodians. For example, if you set the number of reminders to 3, then a custodian would receive a maximum of 3 reminders. After a custodian acknowledges the hold notification, reminders will no longer be sent to that user.</span></span>
   
5. <span data-ttu-id="692cb-181">**제목** 에 대 한 (필수) 통지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-181">Specify the **Subject** for the notice (required).</span></span> 
   
6. <span data-ttu-id="692cb-p116">내용이 나 더불어 (필수)에 게 제공 하려는 추가 지침을 지정 합니다. Note 된 2 단계에서에서 정의 된 포털 콘텐츠를 미리 알림 표시의 끝에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p116">Specify the contents or additional instructions that you would like to provide to the custodian (required). Note that the portal content you defined in Step 2 is added to the end of the reminder notice.</span></span>
   
7. <span data-ttu-id="692cb-184">**저장** 을 클릭 하 고 이동은 다음 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-184">Click **Save** and go the the next step.</span></span>

### <a name="escalations"></a><span data-ttu-id="692cb-185">에스컬레이션</span><span class="sxs-lookup"><span data-stu-id="692cb-185">Escalations</span></span> 

<span data-ttu-id="692cb-p117">일부 경우에 응답 하지 않는 custodians와 사후 점검 하는 또다른 방법을 할 수도 있습니다. 더불어 미리 지정 된 수를 확인 한 후 보류 알림 승인 하지, 법적 팀 더불어와 해당 관리자에 게 에스컬레이션 통지를 자동으로 보내도록 워크플로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p117">In some situations, you may need additional ways to follow-up with unresponsive custodians. If a custodian doesn't acknowledge a hold notification after receiving the specified number of reminders, the legal team can specify a workflow to automatically send an escalation notice to the custodian and their manager.</span></span>

<span data-ttu-id="692cb-188">에스컬레이션을 예약 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-188">To schedule escalations:</span></span>

1. <span data-ttu-id="692cb-189">**에스컬레이션** 타일에서 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-189">In the **Escalation** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="692cb-190">**상태** 토글 설정 하 여 **에스컬레이션** 워크플로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-190">Enable the **Escalation** workflow by turning on the **Status** toggle.</span></span>
   
3. <span data-ttu-id="692cb-191">(필수) **에스컬레이션 간격 (일)을** 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-191">Specify the **Escalation interval (in days)** (required).</span></span> 
   
4. <span data-ttu-id="692cb-p118">(필수) **에스컬레이션의 수** 를 지정 합니다. 이 필드는 얼마나 많은 에스컬레이션 되지 않은 응답 custodians를 보낼 수를 지정 합니다. 예 3으로 에스컬레이션의 수를 설정 하는 경우 다음 에스컬레이션 통지는 전송 더불어와 해당 관리자에 게 최대 3 번. 한 더불어 승인 보류 알림, 후 에스컬레이션 더이상 보낼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p118">Specify the **Number of escalations** (required). This field specifies how many escalations to send to un-responsive custodians. For example, if you set the number of escalations to 3, then an escalation notice would be sent to the custodian and their manager a maximum of 3 times. After a custodian acknowledges the hold notification, escalations will no longer be sent.</span></span> 
   
5. <span data-ttu-id="692cb-196">**제목** 에 대 한 (필수) 통지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-196">Specify the **Subject** for the notice (required).</span></span> 
   
6. <span data-ttu-id="692cb-p119">내용이 나 더불어 (필수)에 게 제공 하려는 추가 지침을 지정 합니다. 2 단계에서에서 정의 된 포털 콘텐츠 에스컬레이션 주의 표시의 끝에 추가 되는 note 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-p119">Specify the contents or additional instructions that you would like to provide to the custodian (required). Note that the portal content you defined in Step 2 is added to the end of the escalation notice.</span></span>
   
7. <span data-ttu-id="692cb-199">**저장** 을 클릭 하 고 이동은 다음 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-199">Click **Save** and go the the next step.</span></span>
   
## <a name="step-5-assign-custodians"></a><span data-ttu-id="692cb-200">5 단계: custodians 할당</span><span class="sxs-lookup"><span data-stu-id="692cb-200">Step 5: Assign custodians</span></span> 

<span data-ttu-id="692cb-201">알림에 대 한 콘텐츠를 완료 한을 한 후에 알림을 보내도록 custodians을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-201">After you have finalized the content for notifications, select the custodians to send the notifications to.</span></span> 

<span data-ttu-id="692cb-202">Custodians를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-202">To add custodians:</span></span>

1. <span data-ttu-id="692cb-203">자신의 이름 옆에 있는 확인란을 클릭 하 여 통신에 custodians를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-203">Assign custodians to the communication by clicking the checkbox next to their name.</span></span>

    <span data-ttu-id="692cb-204">통신을 만든 후 알림 워크플로 선택한 custodians에 자동으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-204">After the communication is created, the notification workflow will automatically apply to the selected custodians.</span></span>
   
2. <span data-ttu-id="692cb-205">**다음** 통신 설정 및 세부 정보를 검토를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-205">Click **Next** to review the communication settings and details.</span></span>
 
>[!NOTE]
><span data-ttu-id="692cb-206">Custodians 대/소문자에 추가 된 및 하지 않은 경우 내에서 다른 알림 전송 된 사용자만 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-206">You can only add custodians who have been added to the case and haven't been sent another notification within the case.</span></span>

## <a name="step-6-review-settings"></a><span data-ttu-id="692cb-207">6 단계: 설정 검토</span><span class="sxs-lookup"><span data-stu-id="692cb-207">Step 6: Review settings</span></span>

<span data-ttu-id="692cb-208">설정을 검토 하 고 통신을 완료 하려면 **보내기** 를 클릭 한 후 시스템, 발급 알림을 보내 통신 워크플로 자동으로 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="692cb-208">After you review the settings and click **Send** to complete the communication, the system will automatically start the communication workflow by sending the issuance notice.</span></span>