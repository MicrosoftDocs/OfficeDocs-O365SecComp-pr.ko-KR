---
title: 관리자로 격리된 메시지 찾기 및 릴리스
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 06/16/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ab95bf17-bb09-4dd1-9990-ddd02ddecf05
ms.collection:
- M365-security-compliance
description: 이 항목에서는 Exchange Online 및 exchange Online Protection (EOP) 관리자가 EAC (exchange 관리 센터)에서 격리 된 메시지를 찾아서 해제 하 고 보고 하는 방법에 대해 설명 합니다.
ms.openlocfilehash: 9bf821885ad8d4ec89aa3c349a6c072f78f6c57a
ms.sourcegitcommit: 769b506c828c475c713dbb337e115714dcc7f17c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/31/2019
ms.locfileid: "36699353"
---
# <a name="find-and-release-quarantined-messages-as-an-administrator"></a><span data-ttu-id="95bb8-103">관리자로 격리된 메시지 찾기 및 릴리스</span><span class="sxs-lookup"><span data-stu-id="95bb8-103">Find and release quarantined messages as an administrator</span></span>

<span data-ttu-id="95bb8-104">이 항목에서는 Exchange Online 및 exchange Online Protection (EOP) 관리자가 EAC (exchange 관리 센터)에서 격리 된 메시지를 찾아서 해제 하 고 보고 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-104">This topic describes how Exchange Online and Exchange Online Protection (EOP) admins can find, release, and report on quarantined messages in the Exchange admin center (EAC).</span></span> <span data-ttu-id="95bb8-105">Office 365에서는 메시지가 스팸으로 식별 되었거나 메일 흐름 규칙 (전송 규칙이 라고도 함)과 일치 하기 때문에 메시지를 격리로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-105">Office 365 directs messages to quarantine either because they were identified as spam or they matched a mail flow rule (also known as a transport rule).</span></span> 
  
<span data-ttu-id="95bb8-106">EAC 대신 보안 &amp; 및 준수 센터를 사용 하 여 이러한 작업을 완료 하 고, 맬웨어가 포함 되어 있어 격리로 전송 된 메시지를 보고 작업 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-106">Use the Security &amp; Compliance Center instead of the EAC to complete any of these tasks as well as view and work with messages that were sent to quarantine because they contain malware.</span></span> <span data-ttu-id="95bb8-107">자세한 내용은 [Office 365에서 전자 메일 메시지 격리](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95bb8-107">For more information, see [Quarantine email messages in Office 365](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).</span></span>
  
<span data-ttu-id="95bb8-108">격리 된 메시지는 EAC의 **격리** 페이지에 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-108">Quarantined messages are listed on the **quarantine** page in EAC.</span></span> <span data-ttu-id="95bb8-109">기본적으로 메시지는 **받은 날짜** 필드에서 가장 오래 된 항목 순으로 정렬 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-109">By default, messages are sorted from newest to oldest on the **RECEIVED** field.</span></span> <span data-ttu-id="95bb8-110">각 메시지에 대해 **보낸 사람**, **제목** 및 **만료 날짜** 값도 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-110">**SENDER**, **SUBJECT**, and **EXPIRES** values are also listed for each message.</span></span> <span data-ttu-id="95bb8-111">이러한 필드의 머리글을 클릭하여 각 필드를 정렬할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-111">You can sort on any of these fields by clicking their headers.</span></span> <span data-ttu-id="95bb8-112">열 머리글을 두 번 클릭 하면 정렬 순서가 반전 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-112">If you click a column header a second time, the sort order reverses.</span></span> <span data-ttu-id="95bb8-113">**격리** 페이지에 최대 500 개의 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-113">The **quarantine** page displays a maximum of 500 messages.</span></span> 
  
<span data-ttu-id="95bb8-114">격리 된 모든 메시지의 목록을 보거나, 필터 조건을 지정 하 여 특정 메시지를 검색할 수 있습니다 (필터링은 메시지 수가 500 개를 초과 하는 경우에도 결과 집합을 줄이는 데 도움이 됩니다).</span><span class="sxs-lookup"><span data-stu-id="95bb8-114">You can view a list of all quarantined messages, or you can search for specific messages by specifying filter criteria (filtering can also help reduce your result set if you have more than 500 messages).</span></span> <span data-ttu-id="95bb8-115">격리된 특정 메시지를 검색하여 찾은 후에는 메시지에 대한 세부 정보를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-115">After searching for and locating a specific quarantined message, you can view details about the message.</span></span> <span data-ttu-id="95bb8-116">다음 작업도 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-116">You can also:</span></span>
  
- <span data-ttu-id="95bb8-117">메시지를 한 명 이상의 받는 사람에 게 놓은 다음, 필요에 따라 메시지를 평가 하 고 분석할 Microsoft 스팸 분석 팀에 가양성 (정크 메일 아님) 메시지로 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-117">Release the message to one or more recipients, and optionally report it as a false positive (not junk) message to the Microsoft Spam Analysis Team, who will evaluate and analyze the message.</span></span> <span data-ttu-id="95bb8-118">분석 결과에 따라 메시지 통과를 허용하도록 서비스 전체적으로 스팸 콘텐츠 필터 규칙이 조정될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-118">Depending on the results of the analysis, the service-wide spam content filter rules may be adjusted to allow the message through.</span></span>
    
- <span data-ttu-id="95bb8-119">메시지를 해제 하 고 앞으로 해당 하는 해당 보낸 사람의 메시지를 모두 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-119">Release the message and allow all future messages from that sender.</span></span>
    
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="95bb8-120">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="95bb8-120">What do you need to know before you begin?</span></span>
<span data-ttu-id="95bb8-121"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="95bb8-121"></span></span>

- <span data-ttu-id="95bb8-122">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-122">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="95bb8-123">필요한 사용 권한을 확인 하려면 [Feature permissions In Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 항목의 "격리" 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="95bb8-123">To see what permissions you need, see the "Quarantine" entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
    
- <span data-ttu-id="95bb8-124">**격리** 페이지에서 한 번에 여러 메시지를 릴리스 하거나 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-124">You can release or report multiple messages at once on the **quarantine** page.</span></span> <span data-ttu-id="95bb8-125">또는이 작업을 수행 하는 원격 Windows PowerShell 스크립트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-125">Alternatively you can create a remote Windows PowerShell script to accomplish this task.</span></span> <span data-ttu-id="95bb8-126">[Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet을 사용하여 메시지를 검색하고 [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet을 사용하여 메시지를 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-126">Use the [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet to search for messages, and the [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet to release them.</span></span> 
    
- <span data-ttu-id="95bb8-127">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대 한 자세한 내용은 [Exchange Online에서 exchange 관리 센터에 대 한 바로 가기 키](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="95bb8-127">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>
    
> [!TIP]
> <span data-ttu-id="95bb8-128">문제가 있습니까?</span><span class="sxs-lookup"><span data-stu-id="95bb8-128">Having problems?</span></span> <span data-ttu-id="95bb8-129">Exchange 포럼에서 도움을 요청하세요.</span><span class="sxs-lookup"><span data-stu-id="95bb8-129">Ask for help in the Exchange forums.</span></span> <span data-ttu-id="95bb8-130">포럼 주소는 다음과 같습니다.[Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), 또는 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351)</span><span class="sxs-lookup"><span data-stu-id="95bb8-130">Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="use-advanced-search-to-filter-and-locate-quarantined-messages"></a><span data-ttu-id="95bb8-131">고급 검색을 사용하여 격리된 메시지 필터링 및 찾기</span><span class="sxs-lookup"><span data-stu-id="95bb8-131">Use advanced search to filter and locate quarantined messages</span></span>
<span data-ttu-id="95bb8-132"><a name="BKMK_UseAdvancedSearchtoFilterMessages"> </a></span><span class="sxs-lookup"><span data-stu-id="95bb8-132"></span></span>

<span data-ttu-id="95bb8-p109">EAC(Exchange 관리 센터)에서 고급 검색을 사용하여 여러 조건에 따라 격리된 항목을 필터링할 수 있습니다. 이러한 조건은 따로 사용할 수도 있고 조합하여 사용할 수도 있습니다. 검색에서는 모든 필터 조건을 충족하는 메시지 목록이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-p109">In the Exchange admin center (EAC), you can filter quarantined items based on several different conditions using advanced search. You can use these conditions separately or in combination with one another. The search will provide a list of messages that meet all your filter criteria.</span></span>
  
1. <span data-ttu-id="95bb8-136">EAC에서 **보호** \> **격리**로 이동한 다음 **고급 검색**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-136">In EAC, navigate to **Protection** \> **quarantine**, and then click **Advanced search**.</span></span>
    
2. <span data-ttu-id="95bb8-137">**고급 검색** 창에서 다음 조건의 조합을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-137">In the **Advanced search** window, select any combination of the following conditions.</span></span> <span data-ttu-id="95bb8-138">연결 된 확인란을 선택 하 여 각 조건을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-138">Select the associated check box to enable each condition.</span></span> <span data-ttu-id="95bb8-139">와일드카드는 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-139">Wildcards aren't supported.</span></span> 
    
1. <span data-ttu-id="95bb8-140">**메시지 ID** 이 매개 변수를 사용하여 특정 메시지를 대상으로 하는 검색을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-140">**Message ID** You can use this parameter to perform a targeted search for a specific message.</span></span> <span data-ttu-id="95bb8-141">예를 들어 메시지 추적 기능을 사용하면 조직의 특정 사용자가 보냈거나 받아야 하는데 대상에 도착하지 않은 메시지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-141">For example, if a specific message is sent by, or intended for, a user in your organization, but it never reaches its destination, you can search for the message using the message trace feature.</span></span> <span data-ttu-id="95bb8-142">자세한 내용은 [메시지 추적 실행 및 결과 보기](http://technet.microsoft.com/library/74a9fc59-7e0e-4832-baf9-2a86418b0079.aspx)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="95bb8-142">For details, see [Run a Message Trace and View Results](http://technet.microsoft.com/library/74a9fc59-7e0e-4832-baf9-2a86418b0079.aspx).</span></span> <span data-ttu-id="95bb8-143">규칙과 일치하거나 스팸으로 확인되어 격리로 전송된 메시지가 있으면 해당 메시지 ID를 지정하여 격리에서 메시지를 쉽게 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-143">If you discover that the message was sent to the quarantine, perhaps because it matched a rule or was identified as spam, you can then easily find this message in the quarantine by specifying its Message ID.</span></span> <span data-ttu-id="95bb8-144">이때 전체 메시지 ID 문자열을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-144">Be sure to include the full Message ID string.</span></span> <span data-ttu-id="95bb8-145">여기에는 꺾쇠 괄호 (\<\>)가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-145">This might include angle brackets (\<\>).</span></span> 
    
2. <span data-ttu-id="95bb8-146">**보낸 사람 전자 메일 주소** 메시지를 보낸 사람의 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-146">**Sender email address** Specify the email address of the person who sent the message.</span></span> 
    
3. <span data-ttu-id="95bb8-147">**받는 사람 전자 메일 주소** 메시지를 받는 사람의 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-147">**Recipient email address** Specify the email address of the intended recipient of the message.</span></span> 
    
4. <span data-ttu-id="95bb8-148">**제목** 메시지의 제목 줄 텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-148">**Subject** Specify the subject line text of the message.</span></span> 
    
5. <span data-ttu-id="95bb8-149">**받은 날짜** 지난 24 시간 이내 ( **오늘**), 지난 48 시간 ( **지난 2 일**), 지난 주 ( **지난 7 일**) 내에 격리를 통해 메시지가 수신 되었음을 선택 하거나, 메시지를 표시할 사용자 지정 시간 간격을 선택할 수 있습니다. 격리에 의해 수신 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-149">**Received** You can select that the message was received by quarantine within the past 24 hours ( **Today**), within the past 48 hours ( **Last 2 days**), within the past week ( **Last 7 days**), or you can select a custom time interval during which the message was received by the quarantine.</span></span> 
    
6. <span data-ttu-id="95bb8-150">**만료** 다음 24 시간 이내 ( **오늘**), 다음 48 시간 ( **다음 2 일**), 다음 주 (다음 **7 일**) 이내에 메시지가 격리에서 삭제 되는 것을 선택 하거나 메시지를 표시할 사용자 지정 시간 간격을 선택할 수 있습니다. 격리에서 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-150">**Expires** You can select that the message will be deleted from quarantine within the next 24 hours ( **Today**), within the next 48 hours ( **Next 2 days**), within the next week ( **Next 7 days**), or you can select a custom time interval during which the message will be deleted from quarantine.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="95bb8-151">기본적으로 스팸 격리 메시지는 15 일 동안 격리 된 상태로 유지 되 고, 메일 흐름 규칙과 일치 하는 격리 된 메시지는 7 일 동안 격리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-151">By default, spam-quarantined messages are kept in quarantine for 15 days, while quarantined messages that matched a mail flow rule are kept in the quarantine for 7 days.</span></span> <span data-ttu-id="95bb8-152">이 기간 후에 Office 365에서 메시지를 삭제 하며 이러한 시간을 검색할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-152">After this period of time Office 365 deletes the messages and they are not retrievable.</span></span> <span data-ttu-id="95bb8-153">메일 흐름 규칙과 일치 하는 격리 된 메시지의 보존 기간은 구성할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-153">The retention period for quarantined messages that matched a mail flow rule is not configurable.</span></span> <span data-ttu-id="95bb8-154">그렇지만 스팸 격리 메시지의 보존 기간은 콘텐츠 필터 정책의 **스팸 보존 기간(일)** 설정을 통해 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-154">However, the retention period for spam-quarantined messages can be lowered via the **Retain spam for (days)** setting in your content filter policies.</span></span> <span data-ttu-id="95bb8-155">자세한 내용은 [스팸 필터 정책 구성을](configure-your-spam-filter-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95bb8-155">For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span> 
  
7. <span data-ttu-id="95bb8-156">**입력** **스팸으로**확인 된 격리 된 메시지를 검색할지 아니면 메일 흐름 규칙 (**전송 규칙**)과 일치 하는 메시지를 검색할지를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-156">**Type** You can specify whether to search for quarantined messages that have been identified as **Spam**, or whether to search for messages that matched a mail flow rule (**Transport rule**).</span></span>
    
3. <span data-ttu-id="95bb8-157">**확인**을 클릭하여 고급 검색 실행을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-157">Click **OK** to start running the advanced search.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="95bb8-158">검색 조건을 지우고 격리의 모든 메시지를 보려면 **고급 검색** 창에서 모든 확인란의 선택을 취소하고 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-158">To clear your search criteria and view all messages in the quarantine, clear all the check boxes in the **Advanced search** window, and then click **OK**.</span></span> 
  
<span data-ttu-id="95bb8-p113">메시지를 검색하고 나면 지정한 조건과 일치하는 결과가 사용자 인터페이스에 표시됩니다. EAC에서는 메시지를 500개까지 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-p113">After searching for messages, the results that match your specified criteria will display in the user interface. A maximum of 500 messages can be displayed in the EAC.</span></span> 
  
## <a name="view-details-about-a-specific-quarantined-message"></a><span data-ttu-id="95bb8-161">격리된 특정 메시지에 대한 세부 정보 보기</span><span class="sxs-lookup"><span data-stu-id="95bb8-161">View details about a specific quarantined message</span></span>
<span data-ttu-id="95bb8-162"><a name="BKMK_ViewDetailsAboutaSpecificQuarantinedMessage"> </a></span><span class="sxs-lookup"><span data-stu-id="95bb8-162"></span></span>

<span data-ttu-id="95bb8-163">격리 페이지에서 격리 된 특정 메시지를 \*\*\*\* 찾은 후에는이에 대 한 세부 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-163">After locating a specific quarantined message on the **quarantine** page, you can view details about it.</span></span> 
  
1. <span data-ttu-id="95bb8-164">**격리** 페이지에서 특정 메시지를 선택 하 고 화면 오른쪽의 세부 정보 창에 해당 메시지의 속성에 대 한 요약을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-164">On the **quarantine** page, select a specific message and a summary of the properties of that message appear in the details pane on the right side of the screen.</span></span> 
    
    <span data-ttu-id="95bb8-165">**메시지 상태** 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-165">The **Message status** values are as follows:</span></span> 
    
  - <span data-ttu-id="95bb8-166">**입력** 메시지가 **스팸으로** 식별 되었는지 아니면 메일 흐름 규칙 (**전송 규칙**)과 일치 했는지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-166">**Type** Denotes whether the message has been identified as **Spam** or matched a mail flow rule (**Transport rule**).</span></span>
    
  - <span data-ttu-id="95bb8-167">**만료 날짜** 메시지가 격리에서 삭제되는 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-167">**Expires** The date when the message will be deleted from the quarantine.</span></span> 
    
    <span data-ttu-id="95bb8-168">**메시지 정보** 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-168">The **Message details** values are as follows:</span></span> 
    
  - <span data-ttu-id="95bb8-169">**보낸 사람** 메시지를 보낸 사람의 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-169">**Sender** The email address of the person who sent the message.</span></span> 
    
  - <span data-ttu-id="95bb8-170">**제목** 메시지의 제목 줄 텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-170">**Subject** The subject line text of the message.</span></span> 
    
  - <span data-ttu-id="95bb8-171">**받은 날짜** 격리에서 메시지를 받은 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-171">**Received** The date on which the message was received by the quarantine.</span></span> 
    
  - <span data-ttu-id="95bb8-172">**크기** 메시지의 크기입니다. 단위는 KB 또는 MB(메시지 크기가 999KB를 초과하는 경우)입니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-172">**Size** The size of the message, in kilobytes (KB), or, if the message size is greater than 999 KBs, in megabytes (MB).</span></span> 
    
  - <span data-ttu-id="95bb8-p114">**메시지 헤더 보기** 메시지 헤더 텍스트를 확인할 수 있는 **메시지 헤더** 대화 상자를 열려면 이 링크를 클릭합니다. 메시지 헤더 텍스트를 클립보드에 복사한 다음 [메시지 헤더 분석기](https://testconnectivity.microsoft.com/?tabid=mha)에 붙여 넣을 수도 있습니다. 메시지 헤더 분석기 도구가 표시되면 **헤더 분석**을 클릭하여 헤더에 대한 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-p114">**View message header** Click this link to open the **message header** dialog box, which lets you view the message header text. You can also copy the message header text to your clipboard and paste it into the [Message Header Analyzer](https://testconnectivity.microsoft.com/?tabid=mha). Once in the Message Header Analyzer tool, click **Analyze headers** in order to retrieve information about the header.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="95bb8-176">서비스에서 삽입하는 특정 스팸 방지 메시지 헤더 필드에 대한 자세한 내용은 [스팸 방지 메시지 헤더](anti-spam-message-headers.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="95bb8-176">For information about specific anti-spam message header fields inserted by the service, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span> 
  
  - <span data-ttu-id="95bb8-177">**전자 메일 메시지 미리 보기** 메시지 텍스트를 검토 하려면이 링크를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-177">**Preview email message** Click this link to review the text of the message.</span></span> 
    
2. <span data-ttu-id="95bb8-178">격리된 메시지를 두 번 클릭하면 **격리된 메시지** 창이 열리고 다음 정보가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-178">If you double-click a quarantined message, the **Quarantined message** window opens and displays the following information:</span></span> 
    
  - <span data-ttu-id="95bb8-179">**릴리스됨** 메시지가 릴리스된 사용자(있는 경우)의 모든 전자 메일 주소가 포함된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-179">**Released to** A list of all email addresses to whom the message has been released, if any.</span></span> 
    
  - <span data-ttu-id="95bb8-p115">**아직 릴리스되지 않음** 메시지가 아직 릴리스되지 않은 사용자(있는 경우)의 모든 전자 메일 주소가 포함된 목록입니다. **릴리스됨** 링크를 클릭하면 메시지를 릴리스할 수 있습니다. 메시지 릴리스에 대한 자세한 내용은 다음 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="95bb8-p115">**Not yet released to** A list of all email addresses to whom the message has not been released, if any. You can click the **Release to** link in order to release the message; for more information about releasing a message, see the next section.</span></span> 
    
  - <span data-ttu-id="95bb8-182">**메시지 ID** 메시지 헤더에 있는 인터넷 메시지 ID(클라이언트 ID라고도 함)입니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-182">**Message ID** The Internet Message ID (also known as the Client ID) found in the header of the message.</span></span> 
    
    <span data-ttu-id="95bb8-183">**닫기**를 클릭하여 기본 격리 창으로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-183">Click **Close** to return to the main quarantine pane.</span></span> 
    
## <a name="release-messages-from-quarantine"></a><span data-ttu-id="95bb8-184">격리에서 메시지 릴리스</span><span class="sxs-lookup"><span data-stu-id="95bb8-184">Release messages from quarantine</span></span>
<span data-ttu-id="95bb8-185"><a name="sectionSection3"> </a></span><span class="sxs-lookup"><span data-stu-id="95bb8-185"></span></span>

<span data-ttu-id="95bb8-186">받는 사람에 게 메시지를 릴리스하기 위해 다음 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-186">If you want to release messages to recipients, your options are:</span></span>
  
- [<span data-ttu-id="95bb8-187">격리 된 메시지 릴리스 및 보낸 사람의 향후 메시지 허용</span><span class="sxs-lookup"><span data-stu-id="95bb8-187">Release a quarantined message and allow future messages from the sender</span></span>](find-and-release-quarantined-messages-as-an-administrator.md#Releasequarantinedmessageallowfuturemessagesfromsender)
    
- [<span data-ttu-id="95bb8-188">격리 된 메시지를 가양성으로 보고 하지 않고 특정 받는 사람에 게 릴리스</span><span class="sxs-lookup"><span data-stu-id="95bb8-188">Release a quarantined message to specific recipients without reporting it as a false positive</span></span>](find-and-release-quarantined-messages-as-an-administrator.md#Releasequarantinedmessagetospecificrecipientswithoutreportingasfalsepositive)
    
- [<span data-ttu-id="95bb8-189">모든 받는 사람에 게 격리 된 메시지를 하나 이상 릴리스</span><span class="sxs-lookup"><span data-stu-id="95bb8-189">Release one or more quarantined messages to all recipients</span></span>](find-and-release-quarantined-messages-as-an-administrator.md#Releaseoneormorequarantinedmessagestoallrecipients)
    
- [<span data-ttu-id="95bb8-190">하나 이상의 격리 된 메시지를 모든 받는 사람에 게 릴리스하고 가양성 보고</span><span class="sxs-lookup"><span data-stu-id="95bb8-190">Release one or more quarantined messages to all recipients and report false positives</span></span>](find-and-release-quarantined-messages-as-an-administrator.md#Releaseoneormorequarantinedmessagestoallrecipientsandreportfalsepositives)
    
### <a name="release-a-quarantined-message-and-allow-future-messages-from-the-sender"></a><span data-ttu-id="95bb8-191">격리 된 메시지 릴리스 및 보낸 사람의 향후 메시지 허용</span><span class="sxs-lookup"><span data-stu-id="95bb8-191">Release a quarantined message and allow future messages from the sender</span></span>
<span data-ttu-id="95bb8-192"><a name="Releasequarantinedmessageallowfuturemessagesfromsender"> </a></span><span class="sxs-lookup"><span data-stu-id="95bb8-192"></span></span>

1. <span data-ttu-id="95bb8-193">EAC에서 **보호** \> **격리**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-193">In EAC, navigate to **Protection** \> **quarantine**.</span></span>
    
2. <span data-ttu-id="95bb8-194">메시지를 클릭 하 여 선택 하 고 다음 스크린샷과 같이 **메시지 릴리스** 아이콘을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-194">Click on a message to select it and then click the **Release Message** icon as shown in the following screen shot.</span></span> 
  
![강조 표시된 메시지 릴리스 아이콘 및 표시된 릴리스 옵션이 포함된 격리 페이지를 보여줍니다.](media/36ee081f-3e30-40c9-8ce3-240cee1970cc.png)
  
<span data-ttu-id="95bb8-196">드롭다운 목록에서 **선택한 메시지 릴리스 및 보낸 사람 허용** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-196">Click **Release selected message and allow sender** from the drop-down list.</span></span> 
    
3. <span data-ttu-id="95bb8-197">**메시지 릴리스 및 보낸 사람 허용** 대화 상자가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-197">The **release message and allow sender** dialog box opens.</span></span> <span data-ttu-id="95bb8-198">필요한 경우 Microsoft에 메시지를 보고할지 선택한 다음 **릴리스 및 허용**을 클릭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-198">Optionally, you can choose to report the message to Microsoft, then click **release and allow**.</span></span> <span data-ttu-id="95bb8-199">메시지가 주소가 지정 된 모든 받는 사람에 게 전달 되 고 앞으로이 보낸 사람에 게 보내는 모든 메시지가 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-199">The message will be released to all recipients it's addressed to and all future messages from this sender will be allowed.</span></span> <span data-ttu-id="95bb8-200">그러나 메일 흐름 규칙 또는 수신 거부로 인해이 메시지가 격리 된 경우에는 이후 메시지에 대 한 보낸 사람을 계속 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-200">However, if this message was quarantined because of a mail flow rule or blocked sender, the sender will continue to be blocked for future messages.</span></span> 
    
### <a name="release-a-quarantined-message-to-specific-recipients-without-reporting-it-as-a-false-positive"></a><span data-ttu-id="95bb8-201">격리 된 메시지를 가양성으로 보고 하지 않고 특정 받는 사람에 게 릴리스</span><span class="sxs-lookup"><span data-stu-id="95bb8-201">Release a quarantined message to specific recipients without reporting it as a false positive</span></span>
<span data-ttu-id="95bb8-202"><a name="Releasequarantinedmessagetospecificrecipientswithoutreportingasfalsepositive"> </a></span><span class="sxs-lookup"><span data-stu-id="95bb8-202"></span></span>

1. <span data-ttu-id="95bb8-203">EAC에서 **보호** \> **격리**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-203">In EAC, navigate to **Protection** \> **quarantine**.</span></span>
    
2. <span data-ttu-id="95bb8-204">메시지를 선택 하 고 **메시지 릴리스** 아이콘을 클릭 한 다음 드롭다운 목록에서 **메시지를 특정 받는 사람에 게 릴리스를** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-204">Select a message, click the **Release Message** icon, and then click **Release message to specific recipients** from the drop-down list.</span></span> 
    
3. <span data-ttu-id="95bb8-205">**메시지 릴리스** 대화 상자에서 다음 옵션 중 하나를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-205">In the **release message** dialog box, select one of the following options:</span></span> 
    
  - <span data-ttu-id="95bb8-p117">**모든 받는 사람에게 메시지 릴리스** 이 옵션을 선택하면 메시지를 동일한 받는 사람에게 두 번 이상 릴리스할 수 없습니다. 받는 사람이 이 메시지를 이전에 수신한 경우 메시지가 해당 받는 사람에게 다시 릴리스되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-p117">**Release message to all recipients** When you select this option, be aware that a message cannot be released more than once to the same recipient. If a recipient has previously received the message, it will not be released again to that recipient.</span></span> 
    
  - <span data-ttu-id="95bb8-208">**지정한 받는 사람에 게 메시지 릴리스** 메시지를 해제할 수 있는 받는 사람을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-208">**Release message to specified recipients** Select the recipient(s) to whom the message can be released.</span></span> <span data-ttu-id="95bb8-209">메시지는 받는 사람 모두에 게 한 번만 릴리스될 수 있으므로이 목록에는 해당 받는 사람을 해제할 수 있는 사용자만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-209">Because a message can only be released once to each recipient, only recipients to whom it can be released appear in this list.</span></span> <span data-ttu-id="95bb8-210">여러 항목을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-210">Multi-selection is supported.</span></span> <span data-ttu-id="95bb8-211">받는 사람을 선택한 후 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-211">After making your recipient selections, click **add**.</span></span>
    
4. <span data-ttu-id="95bb8-212">**릴리스**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-212">Click **release**.</span></span> 
    
<span data-ttu-id="95bb8-213">새로 고침 아이콘](media/ITPro-EAC-RefreshIcon.gif) **새로**![고침 아이콘을 클릭 하 여 데이터를 새로 고친 다음 해당 메시지를 두 번 클릭 하면 해당 받는 사람에 게 해당 메시지가 해제 된 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-213">If you click the **Refresh**![Refresh Icon](media/ITPro-EAC-RefreshIcon.gif) icon to refresh your data, and then double-click the message, you should see that it's been released to the intended recipients.</span></span> 
  
### <a name="release-one-or-more-quarantined-messages-to-all-recipients"></a><span data-ttu-id="95bb8-214">모든 받는 사람에 게 격리 된 메시지를 하나 이상 릴리스</span><span class="sxs-lookup"><span data-stu-id="95bb8-214">Release one or more quarantined messages to all recipients</span></span>
<span data-ttu-id="95bb8-215"><a name="Releaseoneormorequarantinedmessagestoallrecipients"> </a></span><span class="sxs-lookup"><span data-stu-id="95bb8-215"></span></span>

1. <span data-ttu-id="95bb8-216">EAC에서 **보호** \> **격리**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-216">In EAC, navigate to **Protection** \> **quarantine**.</span></span>
    
2. <span data-ttu-id="95bb8-217">메시지를 클릭 하 여 선택 하거나 shift 키를 사용 하 여 여러 메시지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-217">Click on a message to select it, or use the shift key to select multiple messages.</span></span> <span data-ttu-id="95bb8-218">그런 다음 **메시지 릴리스** 아이콘을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-218">Then click the **Release Message** icon.</span></span> 
    
3. <span data-ttu-id="95bb8-219">드롭다운 목록에서 **모든 받는 사람에 대해 선택한 메시지 릴리스를** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-219">Click **Release selected message(s) to ALL recipients** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="95bb8-220">경고 대화 상자가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-220">The warning dialog box opens.</span></span> <span data-ttu-id="95bb8-221">경고를 읽고 계속 진행 하려면 **예** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-221">Read the warning and select **Yes** if you want to proceed.</span></span> <span data-ttu-id="95bb8-222">이 옵션을 선택 하면 메시지를 동일한 받는 사람에 게 두 번 이상 릴리스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-222">When you select this option, be aware that a message cannot be released more than once to the same recipient.</span></span> <span data-ttu-id="95bb8-223">받는 사람이 이 메시지를 이전에 수신한 경우 메시지가 해당 받는 사람에게 다시 릴리스되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-223">If a recipient has previously received the message, it will not be released again to that recipient.</span></span> 
    
### <a name="release-one-or-more-quarantined-messages-to-all-recipients-and-report-false-positives"></a><span data-ttu-id="95bb8-224">하나 이상의 격리 된 메시지를 모든 받는 사람에 게 릴리스하고 가양성 보고</span><span class="sxs-lookup"><span data-stu-id="95bb8-224">Release one or more quarantined messages to all recipients and report false positives</span></span>
<span data-ttu-id="95bb8-225"><a name="Releaseoneormorequarantinedmessagestoallrecipientsandreportfalsepositives"> </a></span><span class="sxs-lookup"><span data-stu-id="95bb8-225"></span></span>

1. <span data-ttu-id="95bb8-226">EAC에서 **보호** \> **격리**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-226">In EAC, navigate to **Protection** \> **quarantine**.</span></span>
    
2. <span data-ttu-id="95bb8-227">메시지를 클릭 하 여 선택 하거나 shift 키를 사용 하 여 여러 메시지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-227">Click on a message to select it, or use the shift key to select multiple messages.</span></span> <span data-ttu-id="95bb8-228">그런 다음 **메시지 릴리스** 아이콘을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-228">Then click the **Release Message** icon.</span></span> 
    
3. <span data-ttu-id="95bb8-229">**선택한 메시지 릴리스를 클릭 하 고 드롭다운 목록에서 가양성으로 보고** 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-229">Click **Release selected message(s) and report as false positive** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="95bb8-230">경고 대화 상자가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-230">The warning dialog box opens.</span></span> <span data-ttu-id="95bb8-231">경고를 읽고 계속 진행 하려면 **예** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-231">Read the warning and select **Yes** if you want to proceed.</span></span> <span data-ttu-id="95bb8-232">이 옵션을 선택 하면 메시지를 동일한 받는 사람에 게 두 번 이상 릴리스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-232">When you select this option, be aware that a message cannot be released more than once to the same recipient.</span></span> <span data-ttu-id="95bb8-233">받는 사람이 이 메시지를 이전에 수신한 경우 메시지가 해당 받는 사람에게 다시 릴리스되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-233">If a recipient has previously received the message, it will not be released again to that recipient.</span></span> 
    
     <span data-ttu-id="95bb8-234">스팸으로 격리된 메시지는 Microsoft 스팸 분석 팀에도 보고됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-234">When you choose this option, the message will be released to all recipients who have not yet received it.</span></span> <span data-ttu-id="95bb8-235">스팸 격리 된 메시지는 메시지를 평가 및 분석 하는 Microsoft 스팸 분석 팀에도 보고 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-235">If it's a spam-quarantined message, it will also be reported to the Microsoft Spam Analysis Team, who will evaluate and analyze the message.</span></span> <span data-ttu-id="95bb8-236">분석 결과에 따라 메시지 통과를 허용하도록 서비스 전체적으로 스팸 콘텐츠 필터 규칙이 조정될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-236">Depending on the results of the analysis, the service-wide spam content filter rules may be adjusted to allow the message through.</span></span> 
    
> [!TIP]
> <span data-ttu-id="95bb8-237">[메시지가 스팸으로 표시 되지](how-to-help-ensure-that-a-message-isn-t-marked-as-spam.md)않도록 하는 방법의 단계에 따라 메시지가 스팸으로 표시 되지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-237">Help ensure that a message isn't marked as spam by following the steps in [How to help ensure that a message isn't marked as spam](how-to-help-ensure-that-a-message-isn-t-marked-as-spam.md).</span></span> 
  
<span data-ttu-id="95bb8-238">새로 고침 아이콘](media/ITPro-EAC-RefreshIcon.gif) **새로**![고침 아이콘을 클릭 하 여 데이터를 새로 고친 다음 해당 메시지를 두 번 클릭 하면 해당 받는 사람에 게 해당 메시지가 해제 된 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bb8-238">If you click the **Refresh**![Refresh Icon](media/ITPro-EAC-RefreshIcon.gif) icon to refresh your data, and then double-click the message, you should see that it's been released to the intended recipients.</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="95bb8-239">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="95bb8-239">For more information</span></span>
<span data-ttu-id="95bb8-240"><a name="sectionSection4"> </a></span><span class="sxs-lookup"><span data-stu-id="95bb8-240"></span></span>

[<span data-ttu-id="95bb8-241">격리 FAQ</span><span class="sxs-lookup"><span data-stu-id="95bb8-241">Quarantine FAQ</span></span>](quarantine-faq.md)
  

