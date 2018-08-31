---
title: 관리자로 격리된 메시지 찾기 및 릴리스
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/16/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ab95bf17-bb09-4dd1-9990-ddd02ddecf05
description: 이 항목 방법에 대해 설명 Exchange Online 및 Exchange Online Protection (EOP) 관리자 수, 릴리스, Exchange 관리 센터 (EAC)에서 격리 된 메시지를 보고 합니다.
ms.openlocfilehash: a8c450471d2fe627346b5bea8db50b91d67ffd3f
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003277"
---
# <a name="find-and-release-quarantined-messages-as-an-administrator"></a><span data-ttu-id="1daa9-103">관리자로 격리된 메시지 찾기 및 릴리스</span><span class="sxs-lookup"><span data-stu-id="1daa9-103">Find and release quarantined messages as an administrator</span></span>

<span data-ttu-id="1daa9-p101">이 항목 방법에 대해 설명 Exchange Online 및 Exchange Online Protection (EOP) 관리자 수, 릴리스, Exchange 관리 센터 (EAC)에서 격리 된 메시지를 보고 합니다. Office 365 중 하나를 격리로 메시지를 전달 스팸으로 식별 된 대로 또는 일치 하는 전송 규칙 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p101">This topic describes how Exchange Online and Exchange Online Protection (EOP) admins can find, release, and report on quarantined messages in the Exchange admin center (EAC). Office 365 directs messages to quarantine either because they were identified as spam or they matched a transport rule.</span></span> 
  
<span data-ttu-id="1daa9-p102">보안을 사용 하 여 &amp; EAC 보기 뿐 아니라 이러한 작업 중 하나를 완료 하 고 맬웨어를 포함 하기 때문에 격리로 전송 된 메시지와 함께 작동 하는 대신 준수 센터입니다. 자세한 내용은 [Office 365에서 전자 메일 메시지를 격리를](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p102">Use the Security &amp; Compliance Center instead of the EAC to complete any of these tasks as well as view and work with messages that were sent to quarantine because they contain malware. For more information, see [Quarantine email messages in Office 365](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).</span></span>
  
<span data-ttu-id="1daa9-p103">격리 된 메시지는 EAC에서 **격리** 페이지에 나열 됩니다. 기본적으로 메시지를 **받은 날짜** 에서 가장 오래 된 최신 필드에서 정렬 됩니다. 각 메시지에 대 한 **보낸사람**, **주제**및 **만료 날짜** 값도 표시 됩니다. 이러한 필드 중 하나에 해당 머리글을 클릭 하 여 정렬할 수 있습니다. 두번째 시간, 열 머리글을 클릭 하는 경우 정렬 순서를 반대로 바꿉니다. **격리** 페이지에는 최대 500 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p103">Quarantined messages are listed on the **quarantine** page in EAC. By default, messages are sorted from newest to oldest on the **RECEIVED** field. **SENDER**, **SUBJECT**, and **EXPIRES** values are also listed for each message. You can sort on any of these fields by clicking their headers. If you click a column header a second time, the sort order reverses. The **quarantine** page displays a maximum of 500 messages.</span></span> 
  
<span data-ttu-id="1daa9-p104">모든 격리 된 메시지의 목록을 볼 수 또는 필터 조건을 지정 하 여 특정 메시지를 검색할 수 있습니다 (필터링 수도 줄일 수 사용자의 결과 집합 500 개가 넘는 메시지가 있는 경우). 에 대 한 검색 하 고 격리 된 특정 메시지를 찾은 후 메시지에 대 한 세부 정보를 볼 수 있습니다. 또한 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p104">You can view a list of all quarantined messages, or you can search for specific messages by specifying filter criteria (filtering can also help reduce your result set if you have more than 500 messages). After searching for and locating a specific quarantined message, you can view details about the message. You can also:</span></span>
  
- <span data-ttu-id="1daa9-p105">하나 이상의 받는 사람에 게 메시지를 해제 하 고 필요에 따라 평가 하 고 메시지를 분석 Microsoft 스팸 분석 팀에 false 가양성 (정크 아님) 메시지로 보고할 합니다. 분석의 결과 따라 서비스 수준 스팸 콘텐츠 필터 규칙을 통해 메시지를 허용 하도록 조정 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p105">Release the message to one or more recipients, and optionally report it as a false positive (not junk) message to the Microsoft Spam Analysis Team, who will evaluate and analyze the message. Depending on the results of the analysis, the service-wide spam content filter rules may be adjusted to allow the message through.</span></span>
    
- <span data-ttu-id="1daa9-119">메시지를 해제 하 고 해당 보낸에서 이후의 모든 메시지를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-119">Release the message and allow all future messages from that sender.</span></span>
    
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="1daa9-120">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="1daa9-120">What do you need to know before you begin?</span></span>
<span data-ttu-id="1daa9-121"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="1daa9-121"></span></span>

- <span data-ttu-id="1daa9-p106">이 절차를 수행 하기 전에 사용 권한을 할당 해야 합니다. 필요한 사용 권한을 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 항목의 "격리" 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p106">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Quarantine" entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
    
- <span data-ttu-id="1daa9-p107">릴리스 수도 있고 **격리** 페이지에서 한번에 여러 메시지를 보고할 수 있습니다. 또는이 작업을 수행 하기 위해 원격 Windows PowerShell 스크립트를 만들 수 있습니다. 메시지를 검색 하려면 [Get-quarantinemessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet 및 해제 하는 [릴리스 QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p107">You can release or report multiple messages at once on the **quarantine** page. Alternatively you can create a remote Windows PowerShell script to accomplish this task. Use the [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet to search for messages, and the [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet to release them.</span></span> 
    
- <span data-ttu-id="1daa9-127">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Exchange 관리 센터의 바로 가기 키**을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1daa9-127">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="1daa9-p108">문제가 있습니까? Exchange 포럼에서 도움을 요청하세요. 포럼 주소는 다음과 같습니다.[Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), 또는 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351)</span><span class="sxs-lookup"><span data-stu-id="1daa9-p108">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="use-advanced-search-to-filter-and-locate-quarantined-messages"></a><span data-ttu-id="1daa9-131">고급 검색을 사용하여 격리된 메시지 필터링 및 찾기</span><span class="sxs-lookup"><span data-stu-id="1daa9-131">Use advanced search to filter and locate quarantined messages</span></span>
<span data-ttu-id="1daa9-132"><a name="BKMK_UseAdvancedSearchtoFilterMessages"> </a></span><span class="sxs-lookup"><span data-stu-id="1daa9-132"></span></span>

<span data-ttu-id="1daa9-p109">EAC(Exchange 관리 센터)에서 고급 검색을 사용하여 여러 조건에 따라 격리된 항목을 필터링할 수 있습니다. 이러한 조건은 따로 사용할 수도 있고 조합하여 사용할 수도 있습니다. 검색에서는 모든 필터 조건을 충족하는 메시지 목록이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p109">In the Exchange admin center (EAC), you can filter quarantined items based on several different conditions using advanced search. You can use these conditions separately or in combination with one another. The search will provide a list of messages that meet all your filter criteria.</span></span>
  
1. <span data-ttu-id="1daa9-136">EAC에서 **보호** 로 이동 \> **격리**, **고급 검색**을 클릭 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-136">In EAC, navigate to **Protection** \> **quarantine**, and then click **Advanced search**.</span></span>
    
2. <span data-ttu-id="1daa9-p110">**고급 검색** 창에서 다음 조건 중 임의의 조합 하 여 선택 합니다. 각 조건을 사용 하도록 설정 하려면 연결된 확인란을 선택 합니다. 와일드 카드가 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p110">In the **Advanced search** window, select any combination of the following conditions. Select the associated check box to enable each condition. Wildcards aren't supported.</span></span> 
    
1. <span data-ttu-id="1daa9-p111">**메시지 ID** 특정 메시지에 대 한 대상으로 지정 된 검색을 수행 하려면이 매개 변수를 사용할 수 있습니다. 예, 하 여 특정 메시지를 보내거나 이용 하 여 조직에서 사용자 하 고 해당 대상에 도달 하면 하지를 하는 경우 메시지 추적 기능을 사용 하 여 메시지에 대 한 검색할 수 있습니다. 세부 정보를 [실행 하는 메시지 추적 및 결과 보기를](http://technet.microsoft.com/library/74a9fc59-7e0e-4832-baf9-2a86418b0079.aspx)참조 하십시오. 사용자를 격리에 보낸 메시지를 발견 한 경우 아마도 규칙과 일치 하거나, 스팸으로 확인 되었습니다 때문에 다음 쉽게 찾을 수이 메시지를 격리에 id. 해당 메시지를 지정 하 여 전체 메시지 ID 문자열을 포함 해야 합니다. 여기에 꺾쇠 괄호 포함 될 수 있습니다 (\<\>).</span><span class="sxs-lookup"><span data-stu-id="1daa9-p111">**Message ID** You can use this parameter to perform a targeted search for a specific message. For example, if a specific message is sent by, or intended for, a user in your organization, but it never reaches its destination, you can search for the message using the message trace feature. For details, see [Run a Message Trace and View Results](http://technet.microsoft.com/library/74a9fc59-7e0e-4832-baf9-2a86418b0079.aspx). If you discover that the message was sent to the quarantine, perhaps because it matched a rule or was identified as spam, you can then easily find this message in the quarantine by specifying its Message ID. Be sure to include the full Message ID string. This might include angle brackets (\<\>).</span></span> 
    
2. <span data-ttu-id="1daa9-146">**보낸 사람 전자 메일 주소** 메시지를 보낸 사람의 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-146">**Sender email address** Specify the email address of the person who sent the message.</span></span> 
    
3. <span data-ttu-id="1daa9-147">**받는 사람 전자 메일 주소** 메시지를 받는 사람의 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-147">**Recipient email address** Specify the email address of the intended recipient of the message.</span></span> 
    
4. <span data-ttu-id="1daa9-148">**제목** 메시지의 제목 줄 텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-148">**Subject** Specify the subject line text of the message.</span></span> 
    
5. <span data-ttu-id="1daa9-149">**수신** 지난 24 시간 내 ( **오늘**), 지난 주 ( **지난 7 일**) 내에 속하는 지난 48 시간 ( **마지막 2 일**) 내에서 격리 하 여 받은 메시지를 선택 하거나 메시지를 하는 동안 사용자가 지정한 시간 간격을 선택할 수 있습니다. 사용자를 격리 하 여 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-149">**Received** You can select that the message was received by quarantine within the past 24 hours ( **Today**), within the past 48 hours ( **Last 2 days**), within the past week ( **Last 7 days**), or you can select a custom time interval during which the message was received by the quarantine.</span></span> 
    
6. <span data-ttu-id="1daa9-150">**만료** 다음 24 시간 내 ( **오늘**), 다음 주 ( **다음 7 일**) 내에서 다음 48 시간 ( **다음 2 일**) 내에서 메시지가 격리에서 삭제 또는 하는 동안 사용자가 지정한 시간 간격을 선택할 수 있습니다를 선택할 수 있습니다는 메시지 격리에서 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-150">**Expires** You can select that the message will be deleted from quarantine within the next 24 hours ( **Today**), within the next 48 hours ( **Next 2 days**), within the next week ( **Next 7 days**), or you can select a custom time interval during which the message will be deleted from quarantine.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="1daa9-p112">기본적으로 스팸 격리 메시지를 전송 규칙과 일치 하는 격리 된 메시지는 7 일이에 대 한 사용자를 격리에 보관 되는 동안 15 일 동안 격리에 보관 됩니다. Office 365이이 기간 후 메시지를 삭제 하 고 검색할 수 없습니다. 전송 규칙과 일치 하는 격리 된 메시지에 대 한 보존 기간을 구성할 수는 없습니다. 그러나 콘텐츠 필터 정책에서 **보관 스팸 (일)에 대 한** 설정을 통해 스팸 격리 된 메시지에 대 한 보존 기간을 낮출 수 있습니다. 자세한 내용은 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p112">By default, spam-quarantined messages are kept in quarantine for 15 days, while quarantined messages that matched a transport rule are kept in the quarantine for 7 days. After this period of time Office 365 deletes the messages and they are not retrievable. The retention period for quarantined messages that matched a transport rule is not configurable. However, the retention period for spam-quarantined messages can be lowered via the **Retain spam for (days)** setting in your content filter policies. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span> 
  
7. <span data-ttu-id="1daa9-156">**유형** **스팸**으로 식별되어 격리된 메시지를 검색할지 아니면 **전송 규칙**과 일치한 메시지를 검색할지를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-156">**Type** You can specify whether to search for quarantined messages that have been identified as **Spam**, or whether to search for messages that matched a **Transport rule**.</span></span>
    
3. <span data-ttu-id="1daa9-157">**확인**을 클릭하여 고급 검색 실행을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-157">Click **OK** to start running the advanced search.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="1daa9-158">검색 조건을 지우고 격리의 모든 메시지를 보려면 **고급 검색** 창에서 모든 확인란의 선택을 취소하고 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-158">To clear your search criteria and view all messages in the quarantine, clear all the check boxes in the **Advanced search** window, and then click **OK**.</span></span> 
  
<span data-ttu-id="1daa9-p113">메시지를 검색하고 나면 지정한 조건과 일치하는 결과가 사용자 인터페이스에 표시됩니다. EAC에서는 메시지를 500개까지 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p113">After searching for messages, the results that match your specified criteria will display in the user interface. A maximum of 500 messages can be displayed in the EAC.</span></span> 
  
## <a name="view-details-about-a-specific-quarantined-message"></a><span data-ttu-id="1daa9-161">격리된 특정 메시지에 대한 세부 정보 보기</span><span class="sxs-lookup"><span data-stu-id="1daa9-161">View details about a specific quarantined message</span></span>
<span data-ttu-id="1daa9-162"><a name="BKMK_ViewDetailsAboutaSpecificQuarantinedMessage"> </a></span><span class="sxs-lookup"><span data-stu-id="1daa9-162"></span></span>

<span data-ttu-id="1daa9-163">**격리** 페이지에서 특정 격리 된 메시지를 찾은 후에 대 한 세부 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-163">After locating a specific quarantined message on the **quarantine** page, you can view details about it.</span></span> 
  
1. <span data-ttu-id="1daa9-164">**격리** 페이지에서 특정 메시지를 선택 하 고 해당 메시지의 속성 요약이 화면 오른쪽의 세부 정보 창에 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-164">On the **quarantine** page, select a specific message and a summary of the properties of that message appear in the details pane on the right side of the screen.</span></span> 
    
    <span data-ttu-id="1daa9-165">**메시지 상태** 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-165">The **Message status** values are as follows:</span></span> 
    
  - <span data-ttu-id="1daa9-166">**유형** 메시지가 **스팸**으로 식별되었는지 아니면 **전송 규칙**과 일치했는지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-166">**Type** Denotes whether the message has been identified as **Spam** or matched a **Transport rule**.</span></span>
    
  - <span data-ttu-id="1daa9-167">**만료 날짜** 메시지가 격리에서 삭제되는 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-167">**Expires** The date when the message will be deleted from the quarantine.</span></span> 
    
    <span data-ttu-id="1daa9-168">**메시지 정보** 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-168">The **Message details** values are as follows:</span></span> 
    
  - <span data-ttu-id="1daa9-169">**보낸 사람** 메시지를 보낸 사람의 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-169">**Sender** The email address of the person who sent the message.</span></span> 
    
  - <span data-ttu-id="1daa9-170">**제목** 메시지의 제목 줄 텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-170">**Subject** The subject line text of the message.</span></span> 
    
  - <span data-ttu-id="1daa9-171">**받은 날짜** 격리에서 메시지를 받은 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-171">**Received** The date on which the message was received by the quarantine.</span></span> 
    
  - <span data-ttu-id="1daa9-172">**크기** 메시지의 크기입니다. 단위는 KB 또는 MB(메시지 크기가 999KB를 초과하는 경우)입니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-172">**Size** The size of the message, in kilobytes (KB), or, if the message size is greater than 999 KBs, in megabytes (MB).</span></span> 
    
  - <span data-ttu-id="1daa9-p114">**메시지 헤더 보기** 메시지 헤더 텍스트를 확인할 수 있는 **메시지 헤더** 대화 상자를 열려면 이 링크를 클릭합니다. 메시지 헤더 텍스트를 클립보드에 복사한 다음 [메시지 헤더 분석기](https://testconnectivity.microsoft.com/?tabid=mha)에 붙여 넣을 수도 있습니다. 메시지 헤더 분석기 도구가 표시되면 **헤더 분석**을 클릭하여 헤더에 대한 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p114">**View message header** Click this link to open the **message header** dialog box, which lets you view the message header text. You can also copy the message header text to your clipboard and paste it into the [Message Header Analyzer](https://testconnectivity.microsoft.com/?tabid=mha). Once in the Message Header Analyzer tool, click **Analyze headers** in order to retrieve information about the header.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="1daa9-176">서비스에서 삽입하는 특정 스팸 방지 메시지 헤더 필드에 대한 자세한 내용은 [스팸 방지 메시지 헤더](anti-spam-message-headers.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1daa9-176">For information about specific anti-spam message header fields inserted by the service, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span> 
  
  - <span data-ttu-id="1daa9-177">**전자 메일 메시지 미리 보기** 메시지의 텍스트를 검토 하려면이 링크를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-177">**Preview email message** Click this link to review the text of the message.</span></span> 
    
2. <span data-ttu-id="1daa9-178">격리된 메시지를 두 번 클릭하면 **격리된 메시지** 창이 열리고 다음 정보가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-178">If you double-click a quarantined message, the **Quarantined message** window opens and displays the following information:</span></span> 
    
  - <span data-ttu-id="1daa9-179">**릴리스됨** 메시지가 릴리스된 사용자(있는 경우)의 모든 전자 메일 주소가 포함된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-179">**Released to** A list of all email addresses to whom the message has been released, if any.</span></span> 
    
  - <span data-ttu-id="1daa9-p115">**아직 릴리스되지 않음** 메시지가 아직 릴리스되지 않은 사용자(있는 경우)의 모든 전자 메일 주소가 포함된 목록입니다. **릴리스됨** 링크를 클릭하면 메시지를 릴리스할 수 있습니다. 메시지 릴리스에 대한 자세한 내용은 다음 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p115">**Not yet released to** A list of all email addresses to whom the message has not been released, if any. You can click the **Release to** link in order to release the message; for more information about releasing a message, see the next section.</span></span> 
    
  - <span data-ttu-id="1daa9-182">**메시지 ID** 메시지 헤더에 있는 인터넷 메시지 ID(클라이언트 ID라고도 함)입니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-182">**Message ID** The Internet Message ID (also known as the Client ID) found in the header of the message.</span></span> 
    
    <span data-ttu-id="1daa9-183">**닫기**를 클릭하여 기본 격리 창으로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-183">Click **Close** to return to the main quarantine pane.</span></span> 
    
## <a name="release-messages-from-quarantine"></a><span data-ttu-id="1daa9-184">격리에서 릴리스 메시지</span><span class="sxs-lookup"><span data-stu-id="1daa9-184">Release messages from quarantine</span></span>
<span data-ttu-id="1daa9-185"><a name="sectionSection3"> </a></span><span class="sxs-lookup"><span data-stu-id="1daa9-185"></span></span>

<span data-ttu-id="1daa9-186">받는 사람에 게 메시지를 해제 하려면 사용자 옵션은 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-186">If you want to release messages to recipients, your options are:</span></span>
  
- [<span data-ttu-id="1daa9-187">격리 된 메시지 릴리스 및 이후 메시지를 보낸 사람에 게 허용</span><span class="sxs-lookup"><span data-stu-id="1daa9-187">Release a quarantined message and allow future messages from the sender</span></span>](find-and-release-quarantined-messages-as-an-administrator.md#Releasequarantinedmessageallowfuturemessagesfromsender)
    
- [<span data-ttu-id="1daa9-188">특정 받는 사람에 게 격리 된 메시지를 가양성으로 보고 하지 않고 릴리스</span><span class="sxs-lookup"><span data-stu-id="1daa9-188">Release a quarantined message to specific recipients without reporting it as a false positive</span></span>](find-and-release-quarantined-messages-as-an-administrator.md#Releasequarantinedmessagetospecificrecipientswithoutreportingasfalsepositive)
    
- [<span data-ttu-id="1daa9-189">모든 받는 사람에 게 하나 이상의 격리 된 메시지 릴리스</span><span class="sxs-lookup"><span data-stu-id="1daa9-189">Release one or more quarantined messages to all recipients</span></span>](find-and-release-quarantined-messages-as-an-administrator.md#Releaseoneormorequarantinedmessagestoallrecipients)
    
- [<span data-ttu-id="1daa9-190">모든 받는 사람 및 보고서 가양성을 하나 이상의 격리 된 메시지 릴리스</span><span class="sxs-lookup"><span data-stu-id="1daa9-190">Release one or more quarantined messages to all recipients and report false positives</span></span>](find-and-release-quarantined-messages-as-an-administrator.md#Releaseoneormorequarantinedmessagestoallrecipientsandreportfalsepositives)
    
### <a name="release-a-quarantined-message-and-allow-future-messages-from-the-sender"></a><span data-ttu-id="1daa9-191">격리 된 메시지 릴리스 및 이후 메시지를 보낸 사람에 게 허용</span><span class="sxs-lookup"><span data-stu-id="1daa9-191">Release a quarantined message and allow future messages from the sender</span></span>
<span data-ttu-id="1daa9-192"><a name="Releasequarantinedmessageallowfuturemessagesfromsender"> </a></span><span class="sxs-lookup"><span data-stu-id="1daa9-192"></span></span>

1. <span data-ttu-id="1daa9-193">EAC에서 **보호** 로 이동 \> **격리**합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-193">In EAC, navigate to **Protection** \> **quarantine**.</span></span>
    
2. <span data-ttu-id="1daa9-194">메시지를 선택한 다음 화면에 표시 된 대로 **메시지 릴리스** 아이콘을 클릭 합니다를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-194">Click on a message to select it and then click the **Release Message** icon as shown in the following screen shot.</span></span> 
  
![강조 표시된 메시지 릴리스 아이콘 및 표시된 릴리스 옵션이 포함된 격리 페이지를 보여줍니다.](media/36ee081f-3e30-40c9-8ce3-240cee1970cc.png)
  
<span data-ttu-id="1daa9-196">드롭다운 목록에서 **선택한 메시지를 릴리스하고 보낸사람 허용** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-196">Click **Release selected message and allow sender** from the drop-down list.</span></span> 
    
3. <span data-ttu-id="1daa9-p116">**메시지 릴리스 및 보낸사람 허용** 대화 상자가 열립니다. 필요에 따라 **해제 하 고 허용**을 클릭 한 다음 메시지를 Microsoft에 보고를 선택할 수 있습니다. 메시지를 발표 될 예정에 게 배달 되 모든 받는 사람에 게 하 고이 보낸 이후의 모든 메시지를 허용 됩니다. 그러나이 메시지는 전송 규칙으로 인해 격리 된 보낸 사람이 차단 되는 경우를 앞으로 메시지를 차단 하도록 보낸사람 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p116">The **release message and allow sender** dialog box opens. Optionally, you can choose to report the message to Microsoft, then click **release and allow**. The message will be released to all recipients it's addressed to and all future messages from this sender will be allowed. However, if this message was quarantined because of a transport rule or blocked sender, the sender will continue to be blocked for future messages.</span></span> 
    
### <a name="release-a-quarantined-message-to-specific-recipients-without-reporting-it-as-a-false-positive"></a><span data-ttu-id="1daa9-201">특정 받는 사람에 게 격리 된 메시지를 가양성으로 보고 하지 않고 릴리스</span><span class="sxs-lookup"><span data-stu-id="1daa9-201">Release a quarantined message to specific recipients without reporting it as a false positive</span></span>
<span data-ttu-id="1daa9-202"><a name="Releasequarantinedmessagetospecificrecipientswithoutreportingasfalsepositive"> </a></span><span class="sxs-lookup"><span data-stu-id="1daa9-202"></span></span>

1. <span data-ttu-id="1daa9-203">EAC에서 **보호** 로 이동 \> **격리**합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-203">In EAC, navigate to **Protection** \> **quarantine**.</span></span>
    
2. <span data-ttu-id="1daa9-204">메시지를 선택 하 고 **메시지 릴리스** 아이콘을 클릭 한 다음 드롭다운 목록에서 **특정 받는 사람에 게 메시지 릴리스를** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-204">Select a message, click the **Release Message** icon, and then click **Release message to specific recipients** from the drop-down list.</span></span> 
    
3. <span data-ttu-id="1daa9-205">**메시지 릴리스** 대화 상자에서 다음 옵션 중 하나를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-205">In the **release message** dialog box, select one of the following options:</span></span> 
    
  - <span data-ttu-id="1daa9-p117">**모든 받는 사람에게 메시지 릴리스** 이 옵션을 선택하면 메시지를 동일한 받는 사람에게 두 번 이상 릴리스할 수 없습니다. 받는 사람이 이 메시지를 이전에 수신한 경우 메시지가 해당 받는 사람에게 다시 릴리스되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p117">**Release message to all recipients** When you select this option, be aware that a message cannot be released more than once to the same recipient. If a recipient has previously received the message, it will not be released again to that recipient.</span></span> 
    
  - <span data-ttu-id="1daa9-p118">**지정 된 받는 사람에 게 메시지 릴리스** 누구에 게 메시지를 해제할 수 있는 받는 사람을 선택 합니다. 하므로 메시지 각 받는 사람에 게 적용할에 해제 될 수 받는 사람에만이 목록에 표시 한 후에 해제할 수 있습니다. 다중 선택이 지원 됩니다. 받는 사람 선택 항목에 확인 한 후 **추가**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p118">**Release message to specified recipients** Select the recipient(s) to whom the message can be released. Because a message can only be released once to each recipient, only recipients to whom it can be released appear in this list. Multi-selection is supported. After making your recipient selections, click **add**.</span></span>
    
4. <span data-ttu-id="1daa9-212">**릴리스**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-212">Click **release**.</span></span> 
    
<span data-ttu-id="1daa9-213">**새로고침**단추를 누르면![새로고침 아이콘](media/ITPro-EAC-RefreshIcon.gif) 데이터를 새로 고치고, 메시지를 두번클릭 한 다음 아이콘 것 릴리스된 의도 한 받는 사람에 게 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-213">If you click the **Refresh**![Refresh Icon](media/ITPro-EAC-RefreshIcon.gif) icon to refresh your data, and then double-click the message, you should see that it's been released to the intended recipients.</span></span> 
  
### <a name="release-one-or-more-quarantined-messages-to-all-recipients"></a><span data-ttu-id="1daa9-214">모든 받는 사람에 게 하나 이상의 격리 된 메시지 릴리스</span><span class="sxs-lookup"><span data-stu-id="1daa9-214">Release one or more quarantined messages to all recipients</span></span>
<span data-ttu-id="1daa9-215"><a name="Releaseoneormorequarantinedmessagestoallrecipients"> </a></span><span class="sxs-lookup"><span data-stu-id="1daa9-215"></span></span>

1. <span data-ttu-id="1daa9-216">EAC에서 **보호** 로 이동 \> **격리**합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-216">In EAC, navigate to **Protection** \> **quarantine**.</span></span>
    
2. <span data-ttu-id="1daa9-p119">선택 하거나 여러 메시지를 선택 하려면 shift 키를 사용 하 여 메시지를 클릭 합니다. **메시지 릴리스** 아이콘을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p119">Click on a message to select it, or use the shift key to select multiple messages. Then click the **Release Message** icon.</span></span> 
    
3. <span data-ttu-id="1daa9-219">드롭다운 목록에서 **모든 받는 사람에 게 선택 된 메시지 릴리스를** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-219">Click **Release selected message(s) to ALL recipients** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="1daa9-p120">경고 대화 상자가 열립니다. 이 경고를 읽고 진행 하려는 경우 **예** 를 선택 합니다. 이 옵션을 선택 하는 경우 유의 동일한 받는 사람에 게 메시지를 여러 번 해제할 수 없습니다. 받는 사람이 메시지를 받은 이전에 하는 경우 하지 발표 될 예정 다시 해당 받는 사람에 게 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p120">The warning dialog box opens. Read the warning and select **Yes** if you want to proceed. When you select this option, be aware that a message cannot be released more than once to the same recipient. If a recipient has previously received the message, it will not be released again to that recipient.</span></span> 
    
### <a name="release-one-or-more-quarantined-messages-to-all-recipients-and-report-false-positives"></a><span data-ttu-id="1daa9-224">모든 받는 사람 및 보고서 가양성을 하나 이상의 격리 된 메시지 릴리스</span><span class="sxs-lookup"><span data-stu-id="1daa9-224">Release one or more quarantined messages to all recipients and report false positives</span></span>
<span data-ttu-id="1daa9-225"><a name="Releaseoneormorequarantinedmessagestoallrecipientsandreportfalsepositives"> </a></span><span class="sxs-lookup"><span data-stu-id="1daa9-225"></span></span>

1. <span data-ttu-id="1daa9-226">EAC에서 **보호** 로 이동 \> **격리**합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-226">In EAC, navigate to **Protection** \> **quarantine**.</span></span>
    
2. <span data-ttu-id="1daa9-p121">선택 하거나 여러 메시지를 선택 하려면 shift 키를 사용 하 여 메시지를 클릭 합니다. **메시지 릴리스** 아이콘을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p121">Click on a message to select it, or use the shift key to select multiple messages. Then click the **Release Message** icon.</span></span> 
    
3. <span data-ttu-id="1daa9-229">드롭다운 목록에서 **릴리스 선택한 메시지와 가양성으로 보고서를** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-229">Click **Release selected message(s) and report as false positive** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="1daa9-p122">경고 대화 상자가 열립니다. 이 경고를 읽고 진행 하려는 경우 **예** 를 선택 합니다. 이 옵션을 선택 하는 경우 유의 동일한 받는 사람에 게 메시지를 여러 번 해제할 수 없습니다. 받는 사람이 메시지를 받은 이전에 하는 경우 하지 발표 될 예정 다시 해당 받는 사람에 게 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p122">The warning dialog box opens. Read the warning and select **Yes** if you want to proceed. When you select this option, be aware that a message cannot be released more than once to the same recipient. If a recipient has previously received the message, it will not be released again to that recipient.</span></span> 
    
     <span data-ttu-id="1daa9-p123">이 옵션을 선택 하는 경우 모든 받는 사람에 게 아직 수신 되지 않은 메시지 발표 될 예정입니다. 스팸 격리 된 메시지를 평가 하 고 메시지를 분석 Microsoft 스팸 분석 팀에도 보고 됩니다. 분석의 결과 따라 서비스 수준 스팸 콘텐츠 필터 규칙을 통해 메시지를 허용 하도록 조정 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-p123">When you choose this option, the message will be released to all recipients who have not yet received it. If it's a spam-quarantined message, it will also be reported to the Microsoft Spam Analysis Team, who will evaluate and analyze the message. Depending on the results of the analysis, the service-wide spam content filter rules may be adjusted to allow the message through.</span></span> 
    
> [!TIP]
> <span data-ttu-id="1daa9-237">보장 [메시지가 스팸으로 표시 되지 않음 되었는지 보장 하는 방법](how-to-help-ensure-that-a-message-isn-t-marked-as-spam.md)의 단계를 수행 하 여 메시지가 스팸으로 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-237">Help ensure that a message isn't marked as spam by following the steps in [How to help ensure that a message isn't marked as spam](how-to-help-ensure-that-a-message-isn-t-marked-as-spam.md).</span></span> 
  
<span data-ttu-id="1daa9-238">**새로고침**단추를 누르면![새로고침 아이콘](media/ITPro-EAC-RefreshIcon.gif) 데이터를 새로 고치고, 메시지를 두번클릭 한 다음 아이콘 것 릴리스된 의도 한 받는 사람에 게 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1daa9-238">If you click the **Refresh**![Refresh Icon](media/ITPro-EAC-RefreshIcon.gif) icon to refresh your data, and then double-click the message, you should see that it's been released to the intended recipients.</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="1daa9-239">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="1daa9-239">For more information</span></span>
<span data-ttu-id="1daa9-240"><a name="sectionSection4"> </a></span><span class="sxs-lookup"><span data-stu-id="1daa9-240"></span></span>

[<span data-ttu-id="1daa9-241">격리 FAQ</span><span class="sxs-lookup"><span data-stu-id="1daa9-241">Quarantine FAQ</span></span>](quarantine-faq.md)
  

