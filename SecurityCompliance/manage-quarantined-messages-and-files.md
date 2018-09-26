---
title: Office 365에서 관리자 권한으로 격리 된 메시지와 파일을 관리 합니다.
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/05/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 065cc2cf-2f3a-47fd-a434-2a20b8f51d0c
description: '관리 권한으로 볼, 릴리스, 및 Office 365에서 가양성 격리 된 메시지를 보고 수 있습니다. Office 365 메시지를 필터링 하 고 다음과 같은 몇가지 이유로 격리로 보냅니다 되도록 정책을 설정할 수: 스팸, 대량, 피싱, 맬웨어, 확인 된 대로 수 있으므로 또는 메일 흐름 규칙 일치 합니다. '
ms.openlocfilehash: 67fb4ac8e3a5fd443efb04d4f74e9844d2fa8c86
ms.sourcegitcommit: f7fff49ae0b1c3056faa58d73c1070cb4e638fbf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25018882"
---
# <a name="manage-quarantined-messages-and-files-as-an-administrator-in-office-365"></a><span data-ttu-id="7bf76-104">Office 365에서 관리자 권한으로 격리 된 메시지와 파일을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-104">Manage quarantined messages and files as an administrator in Office 365</span></span>

<span data-ttu-id="7bf76-p102">관리 권한으로 보기, 릴리스, 및 격리 된 메시지 및 보고서 가양성 격리 된 메시지 Office 365에서 삭제 수 있습니다. 보고 하 고 다운로드, 다음 비즈니스, 및 Microsoft 팀의 개발자를 위한 SharePoint Online, OneDrive 사전 위협 보호 (ATP) 하 여 캡처한 격리 된 파일을 삭제도 합니다. Office 365 메시지를 필터링 하 고 다음과 같은 몇가지 이유로 격리로 보냅니다 되도록 정책을 설정할 수: 스팸, 대량 메일 피싱 메일, 맬웨어, 포함 된 확인 된 대로 수 있으므로 또는 메일 흐름 규칙 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p102">As an admin, you can view, release, and delete quarantined messages, and report false positive quarantined messages in Office 365. You can also view, download, and delete quarantined files captured by Advance Threat Protection (ATP) for SharePoint Online, OneDrive for Business, and Microsoft Teams. You can set up policies so that Office 365 filters messages and sends them to quarantine for several reasons: Because they were identified as spam, bulk mail, phishing mail, containing malware, or because they matched a mail flow rule.</span></span>
  
<span data-ttu-id="7bf76-p103">기본적으로 Office 365 피싱 메시지와 격리로 직접 맬웨어를 포함 하는 메시지를 보냅니다. 다른 필터링 된 메시지는 격리로 전송할 정책을 설정 하지 않으면 사용자의 정크 메일 폴더로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p103">By default, Office 365 sends phishing messages and messages containing malware directly to quarantine. Other filtered messages are sent to users' Junk Email folder unless you set up a policy to send them to quarantine.</span></span>
  
<span data-ttu-id="7bf76-110">다른 사용자에 게 전송 된 격리 된 메시지와 함께 작동 하도록 하 고 격리 된 파일을 사용 하도록 Office 365에서 관리자 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-110">You must have admin permissions in Office 365 to work with quarantined messages that were sent to other users and to work with quarantined files.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="7bf76-p104">기본적으로 스팸, 대량, 맬웨어, 피싱, 및 일치 하는 메일 흐름 규칙 격리 된 메시지에에서 보관 되 격리 30 일 동안 합니다. 보안에서 스팸 방지 설정에서 격리 시간을 사용자 지정할 수 &amp; 준수 센터입니다. 격리에서 메시지를 삭제 하는 Office 365 때 다시 가져올 수 없습니다. 원하는 경우 스팸 방지 필터 정책에서 격리 된 메시지에 대 한 보존 기간을 변경할 수 있습니다. 자세한 내용은이 문서의 [격리 보존 기간을 설정](manage-quarantined-messages-and-files.md#BKMK_ModQuarantineTime) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p104">By default, spam, bulk, malware, phishing, and messages that were quarantined because they matched a mail flow rule are kept in quarantine for 30 days. You can customize the quarantine time in anti-spam settings in the Security &amp; Compliance Center. When Office 365 deletes a message from quarantine, you can't get it back. If you like, you can change the retention period for quarantined messages in your anti-spam filter policies. For more information, see [Setting the quarantine retention period](manage-quarantined-messages-and-files.md#BKMK_ModQuarantineTime) in this article.</span></span> 
  
## <a name="view-your-organizations-quarantined-messages"></a><span data-ttu-id="7bf76-116">조직의 격리 된 메시지 보기</span><span class="sxs-lookup"><span data-stu-id="7bf76-116">View your organization's quarantined messages</span></span>

1. <span data-ttu-id="7bf76-117">Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 하 여, [보안 및 규정 준수 센터로 이동](go-to-the-securitycompliance-center.md)하 고 Office 365에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-117">Using a work or school account that has global administrator privileges in your Office 365 organization, sign into Office 365 and [go to the Security and Compliance Center](go-to-the-securitycompliance-center.md).</span></span>
    
2. <span data-ttu-id="7bf76-118">왼쪽에 있는 목록의 **위협 관리**를 확장 하 고 **검토**를 선택한 다음 **격리**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-118">In the list on the left, expand **Threat Management**, choose **Review**, and then choose **Quarantine**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="7bf76-119">보안에서 **격리** 페이지로 바로 이동 하려면 &amp; 준수 센터가이 URL을 사용 하 여: >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)</span><span class="sxs-lookup"><span data-stu-id="7bf76-119">To go directly to the **Quarantine** page in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)</span></span>
  
    <span data-ttu-id="7bf76-p105">기본적으로 보안 &amp; 준수 센터 스팸으로 격리 된 모든 전자 메일 메시지를 표시 합니다. 메시지의 메시지를 받은 **날짜** 에 따라 내림차순 정렬 됩니다. 각 메시지에 대 한 **보낸사람**, **주제**및 만료 날짜 **만료** ) (아래 표시 됩니다. 해당 열 머리글;를 클릭 하 여 필드에 정렬할 수 있습니다. 정렬 순서를 바꾸려면 열 머리글을 2 시간을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p105">By default, the Security &amp; Compliance Center displays all email messages that have been quarantined as spam. The messages are sorted from newest to oldest based on the **Date** the message was received. **Sender**, **Subject**, and the expiration date (under **Expires** ) are also displayed for each message. You can sort on a field by clicking the corresponding column header; click a column header a second time to reverse the sort order.</span></span> 
    
3. <span data-ttu-id="7bf76-p106">모든 격리 된 메시지의 목록을 보거나 필터링 하 여 결과 집합을 줄일 수 있습니다. 만 수행할 수 최대 100 개의 항목에 대 한 작업 대량으로 필터링 수도 줄일 수 사용자의 결과 더 많은 경우 집합 있으므로 합니다. 신속 하 게 페이지의 위쪽에 필터에서 옵션을 선택 하 여 단일 격리 이유 때문에 메시지를 필터링 할 수 있습니다. 옵션은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p106">You can view a list of all quarantined messages, or you can reduce the result set by filtering. You can only do bulk operations on up to 100 items, so filtering can also help reduce your result set if you have more than that. You can quickly filter messages for a single quarantine reason by choosing an option from the filter at the top of the page. Options include:</span></span>
    
  - <span data-ttu-id="7bf76-128">스팸으로 확인 된 메일</span><span class="sxs-lookup"><span data-stu-id="7bf76-128">Mail identified as spam</span></span>
    
  - <span data-ttu-id="7bf76-129">메일 흐름 규칙 (전송 규칙 라고도 함)에 의해 설정 하는 정책을 일치 하기 때문에 메일 격리</span><span class="sxs-lookup"><span data-stu-id="7bf76-129">Mail quarantined because it matched a policy set by a mail flow rule (also called a transport rule)</span></span>
    
  - <span data-ttu-id="7bf76-130">대량 메일에 대해 확인 된 메일</span><span class="sxs-lookup"><span data-stu-id="7bf76-130">Mail identified as bulk mail</span></span>
    
  - <span data-ttu-id="7bf76-131">피싱 메일에 대해 확인 된 메일</span><span class="sxs-lookup"><span data-stu-id="7bf76-131">Mail identified as phishing mail</span></span>
    
  - <span data-ttu-id="7bf76-132">맬웨어를 포함 하기 때문에 격리 된 메일</span><span class="sxs-lookup"><span data-stu-id="7bf76-132">Mail quarantined because it contains malware</span></span>
    
<span data-ttu-id="7bf76-p107">또한 관리자, 사용자가 보낸 메시지에만 또는 조직에 대 한 모든 메시지 필터링을 선택할 수 있습니다. 사용자 수 있는 유일한 보기를 종료 하 고 항목에 보낸 메시지와 함께 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p107">In addition, as an admin, you can choose to filter all messages for your organization or only messages sent to you. End users can only view and work with messages sent to them.</span></span>
  
<span data-ttu-id="7bf76-p108">또한 특정 메시지를 확인 하기 위해 결과 필터링 할 수 있습니다. 팁에 대 한이 문서의 [결과 필터링 하 고 격리 된 메시지를 찾아 파일을](manage-quarantined-messages-and-files.md#BKMK_AdvSearch) 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p108">You can also filter your results to find specific messages. For tips, see [To filter results and find quarantined messages and files](manage-quarantined-messages-and-files.md#BKMK_AdvSearch) in this article.</span></span> 
  
<span data-ttu-id="7bf76-137">격리 된 특정 메시지를 찾은 후,에 대 한 세부 정보를 보려면 메시지를 클릭 하 고 다른 사용자의 사서함에 메시지를 해제 하는 다음과 같은 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-137">After you find a specific quarantined message, click the message to view details about it, and take actions, like releasing the message to someone's mailbox.</span></span>
  
## <a name="view-your-organizations-quarantined-files"></a><span data-ttu-id="7bf76-138">조직의 격리 된 파일을 보려면</span><span class="sxs-lookup"><span data-stu-id="7bf76-138">View your organization's quarantined files</span></span>

1. <span data-ttu-id="7bf76-139">[보안 및 규정 준수 센터로 이동](go-to-the-securitycompliance-center.md)하 고 Office 365에 로그인 Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-139">Using a work or school account that has global administrator privileges in your Office 365 organization, sign in to Office 365 and [go to the Security and Compliance Center](go-to-the-securitycompliance-center.md).</span></span>
    
2. <span data-ttu-id="7bf76-140">왼쪽에서 **위협 관리**를 확장 하 고 **검토**를 선택한 다음 **격리**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-140">On the left, expand **Threat Management**, choose **Review**, and then choose **Quarantine**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="7bf76-141">보안에서 **격리** 페이지로 바로 이동 하려면 &amp; 준수 센터가이 URL을 사용 하 여: >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)</span><span class="sxs-lookup"><span data-stu-id="7bf76-141">To go directly to the **Quarantine** page in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)</span></span>
  
3. <span data-ttu-id="7bf76-p109">기본적으로 페이지에는 격리 된 전자 메일 메시지를 표시 합니다. 격리 된 파일을 보려면 표시 하려면 **파일** **맬웨어**으로 인해 격리 된 페이지의 위쪽에 필터를 설정 합니다. 격리 된 파일을 사용 하도록 Office 365에서 관리자 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p109">By default, the page displays quarantined email messages. To view quarantined files, set the filters at the top of the page to show **files**, quarantined due to **malware**. You must have admin permissions in Office 365 to work with quarantined files.</span></span> 
    
4. <span data-ttu-id="7bf76-p110">파일 따라 정렬 됩니다에서 가장 오래 된 최신 파일 격리 된 날짜입니다. **사용자** 마지막으로 수정한 파일을 **서비스** 파일이 게시 된 **파일 이름**, **위치**, **파일 크기**및 만료 날짜 ( **만료**)도 나와 각 파일에 대 한 합니다. 머리글을 클릭 하 여 필드에 정렬할 수 있습니다. 정렬 순서를 바꾸려면 열 머리글을 2 시간을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p110">The files are sorted from newest to oldest based on the date the file was quarantined. The **User** who last modified the file, the **Service** to which the file was posted, the **File Name**, **Location**, **File Size**, and the expiration date ( **Expires**) are also listed for each file. You can sort on a field by clicking a header; click a column header a second time to reverse the sort order.</span></span>
    
<span data-ttu-id="7bf76-p111">모든 격리 된 파일의 목록을 보거나을 필터링 하 여 특정 파일을 검색할 수 있습니다. 메시지와 마찬가지로 할 수 있는 대량으로 최대 100 개의 항목에 대 한 작업입니다. 현재 보안 &amp; 준수 센터를 사용 하면 보고 하 고 맬웨어를 가진 것으로 식별 되어 있으므로 격리에 있는 파일을 관리 합니다. 팁에 대 한이 문서의 [결과 필터링 하 고 격리 된 메시지를 찾아 파일을](manage-quarantined-messages-and-files.md#BKMK_AdvSearch) 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p111">You can view a list of all quarantined files, or you can search for specific files by filtering. Just like messages, you can only do bulk operations on up to 100 items. Currently, the Security &amp; Compliance Center lets you view and manage files that are in quarantine because they have been identified as containing malware. For tips, see [To filter results and find quarantined messages and files](manage-quarantined-messages-and-files.md#BKMK_AdvSearch) in this article.</span></span> 
  
## <a name="to-filter-results-and-find-quarantined-messages-and-files"></a><span data-ttu-id="7bf76-152">결과 필터링 하 고 격리 된 메시지 및 파일을 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="7bf76-152">To filter results and find quarantined messages and files</span></span>
<span data-ttu-id="7bf76-153"><a name="BKMK_AdvSearch"> </a></span><span class="sxs-lookup"><span data-stu-id="7bf76-153"></span></span>

<span data-ttu-id="7bf76-p112">사용자 설정에 따라 격리 된 메시지 및 파일을 많이 있을 수 있습니다. 특정 메시지 또는 파일 또는 메시지 또는 파일 집합을 찾으려면 다양 한 추가 정보에 따라 격리 된 항목을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p112">Depending on your settings, there may be a lot of quarantined messages and files. To find a specific message or file or set of messages or files, you can filter quarantined items based on a variety of additional information.</span></span>
  
1. <span data-ttu-id="7bf76-156">**격리** 페이지에서 필터의 위쪽 행을 적절 하 게 메시지 또는 파일을 표시 하도록 설정 되어 있는지를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-156">On the **Quarantine** page, ensure that the top row of filters is set to display messages or files as appropriate:</span></span> 
    
  - <span data-ttu-id="7bf76-157">파일을 검색 하려면 **맬웨어**으로 인해 격리 된 **파일** 을 표시 하도록 필터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-157">To search for files, set the filters to show **files** quarantined due to **malware**.</span></span>
    
    <span data-ttu-id="7bf76-158">격리 된 파일에 대 한 페이지에는 표시를 알 수에 관계 없이 자신의 it 뿐아니라 격리 된 모든 파일을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-158">For quarantined files, the page displays all quarantined files, not just your own, regardless of what you tell it to show.</span></span>
    
  - <span data-ttu-id="7bf76-p113">격리 된 메시지를 검색 하려면 **모두** 표시 하는 필터를 설정 또는 **만 내** **전자 메일**입니다. 마지막 필터가 선택 격리 된 메시지의 종류를 찾는 합니다. **스팸**메일 흐름 또는 **전송 규칙**, **대량** 메일, **피싱** 메일 또는 **맬웨어**를 포함 하는 메일 일치 하는 메시지에 대 한 식별 되어 격리 된 메시지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p113">To search for quarantined messages, set filters to show **all** or **only my** **email**. For the last filter choose the type of quarantined message that you're looking for. You can search for quarantined messages that have been identified as **spam**, for messages that matched a mail flow or **transport rule**, **bulk** mail, **phishing** mail, or mail that contains **malware**.</span></span>
    
2. <span data-ttu-id="7bf76-p114">**결과 정렬 기준**아래에서 필터 또는 드롭다운 목록에서 검색을 사용 하 여 원하는 필터를 선택 합니다. 옵션 파일 또는 메시지에 대 한 검색 하는 여부에 따라 다릅니다. 이 이번에 와일드 카드 검색 필드에 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p114">Under **Sort results by**, choose the filter or filters you want to use to search from the drop-down lists. The options vary based on whether you are searching for files or messages. Wildcards are not supported in search fields at this time.</span></span>
    
    <span data-ttu-id="7bf76-p115">파일 및 메시지 모두에 대 한 메시지를 날짜 기준으로 필터링 하도록 선택할 수 있습니다 또는 파일 격리로 전송 되었습니다. 날짜 또는 시간을 포함 하 여 날짜 범위를 지정할 수 있습니다. 만료 날짜에 파일이 나 메시지 격리에서 삭제 됩니다 또는 필터의 조합을 사용할 수 있습니다 하 여 검색 결과 필터링 할 수도 있습니다. 만료 날짜를 검색 하려면 **고급 필터**를 선택 합니다. **만료 날짜**를 아래에서 다음 24 시간 내 ( **오늘**), 다음 주 ( **다음 7 일**) 내에서 다음 48 시간 ( **다음 2 일**) 내에서 격리에서 삭제 하는 메시지를 선택할 수 또는 사용자가 지정한 시간 간격을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p115">For both files and messages, you can choose to filter by the date the message or file was sent to quarantine. You can specify the date or a date range, including the time. You can also filter your search results by the expiration date on which the file or message will be deleted from quarantine, or you can use a combination of filters. To search by expiration date, choose **Advanced filter**. Under **Expires**, you can select messages that will be deleted from quarantine within the next 24 hours ( **Today**), within the next 48 hours ( **Next 2 days**), within the next week ( **Next 7 days**), or you can select a custom time interval.</span></span>
    
    <span data-ttu-id="7bf76-170">메시지에는 다음과 같은 추가 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-170">For messages, you have the following additional options:</span></span>
    
  - <span data-ttu-id="7bf76-p116">**메시지 ID**입니다. 이 사용 하 여 메시지 ID를 알고 있는 경우에 특정 메시지를 식별 하기 위해</span><span class="sxs-lookup"><span data-stu-id="7bf76-p116">**Message ID**. Use this to identify a specific message when you know the message ID.</span></span> 
    
    <span data-ttu-id="7bf76-p117">예, 경우에 의해 특정 메시지를 보내거나 이용 하 여 조직에서 사용자 하 고 해당 대상 수준에 도달 하지를 검색할 수 있습니다는 메시지에 대 한 메시지 추적을 사용 하 여 ( [메시지 추적 및 결과 보기 실행](https://go.microsoft.com/fwlink/?LinkId=799737)참조). 메일 흐름 규칙 일치 하거나 스팸으로 식별 된 때문에 아마도 격리로 메시지를 보낸 있는지를 발견 하는 경우 다음 쉽게 찾을 수이 메시지가 격리에서 메시지 ID를 지정 하 여 전체 메시지 ID 문자열을 포함 해야 합니다. 여기에 꺾쇠 괄호 포함 될 수 있습니다 (\<\>), 예:</span><span class="sxs-lookup"><span data-stu-id="7bf76-p117">For example, if a specific message is sent by, or intended for, a user in your organization, but it never reached its destination, you can search for the message by using a message trace (see [Run a Message trace and View Results](https://go.microsoft.com/fwlink/?LinkId=799737)). If you discover that the message was sent to quarantine, perhaps because it matched a mail flow rule or was identified as spam, you can then easily find this message in quarantine by specifying its message ID. Be sure to include the full message ID string. This might include angle brackets (\<\>), for example:</span></span>
    
    <span data-ttu-id="7bf76-177">\<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com\></span><span class="sxs-lookup"><span data-stu-id="7bf76-177">\<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com\></span></span>
    
  - <span data-ttu-id="7bf76-p118">**보낸 전자 메일 주소**입니다. 단일 보낸 전자 메일 주소를 필터링 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p118">**Sender email address**. Choose to filter by a single sender email address.</span></span> 
    
  - <span data-ttu-id="7bf76-p119">**받는 전자 메일 주소**입니다. 단일 받는 사람 전자 메일 주소를 필터링 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p119">**Recipient email address**. Choose to filter by a single recipient email address.</span></span> 
    
  - <span data-ttu-id="7bf76-p120">**제목**입니다. 찾으려는 전자 메일 주소의 제목을 입력 합니다. 와일드 카드를 검색 하는 것은 지원 되지, 이후 결과에 메시지를 반환 하도록 검색에 대 한 순서 대로 메시지의 전체 제목을 사용 해야 합니다. 검색은 대/소문자 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p120">**Subject**. Enter the subject of an email address you want to find. Since wildcard searching is not supported, you must use the entire subject of the message in order for search to return the message in the results. The search is not case-sensitive.</span></span> 
    
## <a name="view-details-about-quarantined-messages-and-files"></a><span data-ttu-id="7bf76-186">격리 된 메시지 및 파일에 대 한 세부 정보 보기</span><span class="sxs-lookup"><span data-stu-id="7bf76-186">View details about quarantined messages and files</span></span>
<span data-ttu-id="7bf76-187"><a name="BKMK_ViewDetails"> </a></span><span class="sxs-lookup"><span data-stu-id="7bf76-187"></span></span>

<span data-ttu-id="7bf76-188">보안의 오른쪽에 **세부 정보** 창에서 해당 속성의 요약을 표시 됩니다 격리 목록에 표시 된 항목을 선택 하면 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-188">When you select an item displayed in the quarantine list, you'll see a summary of its properties in the **Details** pane on the right side of the Security &amp; Compliance Center.</span></span> 
  
 <span data-ttu-id="7bf76-189">**격리 된 메시지에 대해 표시 되는 세부 정보**</span><span class="sxs-lookup"><span data-stu-id="7bf76-189">**Details displayed for quarantined messages**</span></span>
  
- <span data-ttu-id="7bf76-p121">**메시지 ID**입니다. 메시지에 대 한 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p121">**Message ID**. The unique identifier for the message.</span></span> 
    
- <span data-ttu-id="7bf76-p122">**보낸사람 주소**입니다. 메시지를 보낸 사람은 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p122">**Sender Address**. Who sent the message.</span></span> 
    
- <span data-ttu-id="7bf76-p123">**수신**합니다. 날짜 및 시간 메시지를 받았습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p123">**Received**. The date and time the message was received.</span></span> 
    
- <span data-ttu-id="7bf76-p124">**제목**입니다. 메시지의 제목줄 텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p124">**Subject**. The text of the subject line of the message.</span></span> 
    
- <span data-ttu-id="7bf76-p125">**유형**입니다. 메시지가 **스팸**, **대량**, **Phish**일치 하는 메일 흐름 규칙 ( **전송 규칙**) 또는 **맬웨어**를 가진 것으로 식별 된 것으로 표시 되었습니다 하는 경우를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p125">**Type**. Shows if a message has been identified as **Spam**, **Bulk**, **Phish**, matched a mail flow rule ( **Transport rule**), or was identified as containing **Malware**.</span></span>
    
- <span data-ttu-id="7bf76-p126">**만료 됩니다**. 날짜 및 시간 격리에서 메시지 자동으로 삭제 됩니다 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p126">**Expires**. The date and time when the message will automatically be deleted from quarantine.</span></span> 
    
- <span data-ttu-id="7bf76-p127">**현재까지 출시**합니다. 모든 전자 메일 주소 (해당 되는 경우) 메시지 해제 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p127">**Released to**. All email addresses (if any) to which the message has been released.</span></span> 
    
- <span data-ttu-id="7bf76-p128">**아직를 해제**합니다. 모든을 전자 메일 주소 (해당 되는 경우) 하는 메시지가 아직 출시 하지 않은 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p128">**Not yet released to**. All email addresses (if any) to which the message has not yet been released.</span></span> 
    
 <span data-ttu-id="7bf76-206">**격리 된 파일에 대해 표시 되는 세부 정보**</span><span class="sxs-lookup"><span data-stu-id="7bf76-206">**Details displayed for quarantined files**</span></span>
  
- <span data-ttu-id="7bf76-207">**파일 이름** 격리에 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-207">**File Name** The name of the file in quarantine.</span></span> 
    
- <span data-ttu-id="7bf76-208">**사이트 경로** Office 365에서 파일의 위치를 정의 하는 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-208">**Site path** URL that defines the location of the file in Office 365.</span></span> 
    
- <span data-ttu-id="7bf76-209">**감지 날짜 / 시간** 날짜 및 파일 격리 된 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-209">**Detected Date / Time** The date and time the file was quarantined.</span></span> 
    
- <span data-ttu-id="7bf76-210">**만료** 격리에서 메시지를 삭제 하는 경우 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-210">**Expires** The date when the message will be deleted from quarantine.</span></span> 
    
- <span data-ttu-id="7bf76-p129">**하 여 검색 된** 파일에 맬웨어가 감지를 사용 하는 방법입니다. 이 ATP (고급 위협 보호) 또는 Microsoft의 맬웨어 방지 엔진 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p129">**Detected By** The method used to detect the malware in the file. This can be either ATP (Advanced Threat Protection) or Microsoft's anti-malware engine.</span></span> 
    
- <span data-ttu-id="7bf76-213">**릴리스** 파일 릴리스 되었습니다 여부에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-213">**Released** Describes whether or not the file has been released.</span></span> 
    
- <span data-ttu-id="7bf76-214">**맬웨어 이름** 제품군 및 파일에서 감지 된 맬웨어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-214">**Malware Name** Family and name of the malware detected in the file.</span></span> 
    
- <span data-ttu-id="7bf76-215">**문서 ID** 다음은 문서에 대 한 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-215">**Document ID** A unique identifier for the document.</span></span> 
    
- <span data-ttu-id="7bf76-216">**파일 크기** KB에 있는 파일의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-216">**File Size** The size of the file in KB.</span></span> 
    
- <span data-ttu-id="7bf76-217">**조직** 조직의 Office 365의 고유 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-217">**Organization** Your organization's unique ID in Office 365.</span></span> 
    
- <span data-ttu-id="7bf76-218">**수정한 사람** 파일을 마지막으로 수정한 사용자의 작업이 나 교육용 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-218">**Modified By** The work or school account of the user who last modified the file.</span></span> 
    
- <span data-ttu-id="7bf76-219">**파일 크기** KB에 있는 파일의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-219">**File Size** The size of the file in KB.</span></span> 
    
- <span data-ttu-id="7bf76-p130">**SHA256 해시** 파일의 해시를 지정 합니다. 다른 신뢰도 저장소 했거나 환경의 파일 수 있는 다른 조사할 수를 확인 하려면 다음과 같이 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p130">**SHA256 Hash** The hash of the file. You can use this to look up other reputation stores you may have or investigate where else the file might be in your environment.</span></span> 
    
## <a name="managing-messages-and-files-in-quarantine"></a><span data-ttu-id="7bf76-222">격리에서 메시지 및 파일 관리</span><span class="sxs-lookup"><span data-stu-id="7bf76-222">Managing messages and files in quarantine</span></span>
<span data-ttu-id="7bf76-223"><a name="BKMK_ManageQuarantinedItem"> </a></span><span class="sxs-lookup"><span data-stu-id="7bf76-223"></span></span>

<span data-ttu-id="7bf76-224">메시지 또는 메시지의 그룹을 선택한 후 격리에서 메시지를 관리 하기 위한 몇가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-224">After you select a message or group of messages you have several options for managing messages in quarantine.</span></span>
  
- <span data-ttu-id="7bf76-p131">아무 작업도 수행 합니다. 아무 작업도 수행 하지 않으려는 경우 메시지 삭제 됩니다 Office 365에서 자동으로 만료 되 면. 기본적으로 스팸, 대량, 맬웨어, 피싱, 및 일치 하는 메일 흐름 규칙 격리 된 메시지에에서 보관 되 격리 30 일 동안 합니다. 격리에서 메시지를 삭제 하는 Office 365 때 다시 가져올 수 없습니다. 원하는 경우 스팸 방지 정책에서 **보관 스팸 (일)에 대 한** 설정을 구성 하 여 격리 된 메시지에 대 한 보존 기간을 변경할 수 있습니다. 자세한 내용은이 문서의 [격리 보존 기간을 설정](manage-quarantined-messages-and-files.md#BKMK_ModQuarantineTime) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p131">Do nothing. If you choose to do nothing, the message will be deleted by Office 365 automatically upon expiration. By default, spam, bulk, malware, phishing, and messages quarantined because they matched a mail flow rule are kept in quarantine for 30 days. When Office 365 deletes a message from quarantine, you can't get it back. If you like, you can change the retention period for quarantined messages by configuring the **Retain spam for (days)** setting in your anti-spam policies. For more information, see [Setting the quarantine retention period](manage-quarantined-messages-and-files.md#BKMK_ModQuarantineTime) in this article.</span></span> 
    
- <span data-ttu-id="7bf76-p132">**메시지 헤더 보기** 메시지 머리글 텍스트를 보려면이 링크를 선택 합니다. 깊이의 헤더를 분석 하려면 메시지 머리글 텍스트를 클립보드에 복사 하 고 다음 원격 연결 분석기로 이동 하려면 **Microsoft 메시지 헤더 분석기** 선택 (마우스 오른쪽 단추로 클릭 하 고 Office를 유지 하지 않을 경우에 **새 탭에서 열기** 를 선택 이 작업을 완료 365)입니다. 메시지 헤더 분석기 섹션에서 페이지로 메시지 헤더를 붙여넣은 **분석 머리글**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p132">**View message header** Choose this link to see the message header text. To analyze the header in depth, copy the message header text to your clipboard, and then choose **Microsoft Message Header Analyzer** to go to the Remote Connectivity Analyzer (right-click and choose **Open in a new tab** if you don't want to leave Office 365 to complete this task).Paste the message header onto the page in the Message Header Analyzer section, and choose **Analyze headers**.</span></span>
    
- <span data-ttu-id="7bf76-p133">**메시지 미리 보기** 메시지 본문의 HTML 버전 되거나 원시 볼 수 있습니다. HTML 보기에 대 한 링크는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p133">**Preview message** Lets you see raw or HTML versions of the message body text. In the HTML view, links are disabled.</span></span> 
    
- <span data-ttu-id="7bf76-p134">**메시지를 다운로드** 하거나 **파일을 다운로드**합니다. 로컬 장치로 메시지 또는 파일의 복사본을 다운로드 하려면이 옵션을 선택 합니다. 되도록 허용 하는 전에 격리에서 항목을 다운로드와 관련 된 위험에 알고 있는지 확인 해야 합니다. 메시지는 사용자가 지정한 폴더에.eml 형식으로 저장 됩니다. 격리 된 파일은 원래 형식으로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p134">**Download message** or **Download file**. Choose this option to download a copy of the message or file to your local device. You'll need to confirm that you understand the risks associated with downloading items from quarantine before you'll be allowed to do so. Messages are saved in .eml format to a folder you specify. Quarantined files are saved in their original format.</span></span>
    
- <span data-ttu-id="7bf76-p135">**삭제** 원할 경우 격리 된 항목 (또는 항목의 집합) Office 365가 설정한 만료 날짜를 기다리지 않고 즉시 삭제할 수 있습니다. 메시지 또는 격리 목록에서 파일을 삭제 하려면 항목을 선택 하 고 **삭제**를 선택 합니다. 한번에 여러 항목을 삭제 하려면 격리 목록에서 항목의 왼쪽에 있는 확인란을 선택 하 고 **대량 작업** 페이지가 표시 되 면 **선택한 메시지를 삭제** 또는 **선택한 파일을 삭제**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p135">**Delete** If you want, you can immediately delete a quarantined item (or set of items) instead of waiting for the expiration date set by Office 365. To delete a message or file, in the quarantine list, select the item and then choose **Delete**. To delete multiple items at once, select the checkbox to the left of the items in the quarantine list, and then on the **Bulk actions** page that appears, choose **Delete selected messages** or **Delete selected files**.</span></span>
    
- <span data-ttu-id="7bf76-243">**릴리스** 격리 된 항목 (또는 항목의 집합) 릴리스하고 Microsoft를 실수로 격리 된 (가양성으로) 항목을 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-243">**Release** Release a quarantined item (or set of items) and report the items as falsely quarantined (false positives) to Microsoft.</span></span> 
    
    <span data-ttu-id="7bf76-p136">해제 하 고 단일 메시지 또는 격리 목록에서 파일을 보고 항목을 선택, **파일 버전** 또는 **메시지 릴리스**를 선택 합니다. 다음 페이지에서 **분석을 위해 Microsoft에 보고서 메시지** 또는 **보고서 파일을 분석을 위해 Microsoft가** 선택 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p136">To release and report a single message or file, in the quarantine list, select the item, choose **Release file** or **Release message**. On the next page, ensure that **report messages to Microsoft for analysis** or **report files to Microsoft for analysis** is selected.</span></span> 
    
    <span data-ttu-id="7bf76-p137">여러 항목을 한번에 해제 하 격리 목록에서 항목의 왼쪽에 있는 확인란을 선택 하 고 **대량 작업** 페이지가 표시 되 면 **릴리스 파일** 또는 **메시지**를 선택 합니다. 다음 페이지에서 **분석을 위해 Microsoft에 보고서 메시지** 또는 **보고서 파일을 분석을 위해 Microsoft가** 선택 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p137">To release multiple items at once, select the checkbox to the left of the items in the quarantine list, and then on the **Bulk actions** page that appears, choose **Release files** or **Release messages**. On the next page, ensure that **report messages to Microsoft for analysis** or **report files to Microsoft for analysis** is selected.</span></span> 
    
<span data-ttu-id="7bf76-248">메시지를 해제 하는 경우에 다음의 유의 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-248">When you're releasing messages, be aware of the following:</span></span>
  
- <span data-ttu-id="7bf76-p138">여러 메시지의 대량 릴리스를 한번에 수행 하는 경우 메시지는 원래 식별 된 모든 받는 사람에 게 해제 됩니다. 메시지를 특정 수신자에 게에만 하려는 경우 한번에 하나씩 메시지를 릴리스하고, 받는 사람을 개별적으로 식별 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p138">When you perform a bulk release of multiple messages at once, the messages are released to all originally identified recipients. If you only want to release messages only to specific recipients, you need to release the messages one at a time and identify the recipients individually.</span></span>
    
- <span data-ttu-id="7bf76-251">동일한 받는 사람에 게 메시지를 여러 번 해제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-251">A message cannot be released more than once to the same recipient.</span></span>
    
- <span data-ttu-id="7bf76-252">둘 이상의 받는 사람에 게 메시지를 해제 하는 경우 이전에 메시지를 받지 못한 받는 사람만 잠재적인 받는 사람 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-252">When you're releasing a message to more than one recipient, only recipients who have not previously received the message will appear in the list of potential recipients.</span></span>
    
- <span data-ttu-id="7bf76-p139">스팸, 대량, 피싱, 또는 맬웨어를 포함 하는 메시지 또는 메시지를 릴리스할 격리 된 경우 가양성을 보고 하도록 선택 하면 메시지도 Microsoft 스팸 분석 팀에 보고 됩니다. 및 팀이 평가 하 고 메시지를 분석 하는 분석의 결과 따라 서비스 수준 스팸 콘텐츠 필터 규칙을 통해 메시지를 허용 하도록 조정 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p139">When you choose to report false positives, if the message or messages you release were quarantined as spam, bulk, phishing, or as containing malware, the message will also be reported to the Microsoft Spam Analysis Team. The team will evaluate and analyze the message, and, depending on the results of the analysis, the service-wide spam content filter rules may be adjusted to allow the message through.</span></span>
    
## <a name="setting-the-quarantine-retention-period"></a><span data-ttu-id="7bf76-255">격리 보존 기간을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-255">Setting the quarantine retention period</span></span>
<span data-ttu-id="7bf76-256"><a name="BKMK_ModQuarantineTime"> </a></span><span class="sxs-lookup"><span data-stu-id="7bf76-256"></span></span>

<span data-ttu-id="7bf76-p140">얼마나 오래 메시지를 구성할 수 있으며, 만료 되기 전에 파일 격리에 남아 있게 됩니다. 기본적으로 격리 된 항목은 30 일 동안 보관 됩니다. 만들어야 하는 각 정책에 대 한이 설정을 구성 하면 됩니다. 또한이 문서의 설명에 따라 기본 정책에 대 한 값을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p140">You can configure how long messages and files will remain in quarantine before they expire. By default, quarantined items are kept for 30 days. You configure this setting for each policy that you create. You can also modify the value for the default policy as described in this article.</span></span> 
  
### <a name="to-modify-the-quarantine-retention-period-for-the-default-spam-filter-policy-in-the-security-and-compliance-center"></a><span data-ttu-id="7bf76-261">보안 및 규정 준수 센터의 기본 스팸 필터 정책에 대 한 격리 보존 기간을 수정 하려면</span><span class="sxs-lookup"><span data-stu-id="7bf76-261">To modify the quarantine retention period for the default spam filter policy in the Security and Compliance Center</span></span>

1. <span data-ttu-id="7bf76-262">[보안 및 규정 준수 센터로 이동](go-to-the-securitycompliance-center.md)하 고 Office 365에 로그인 Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-262">Using a work or school account that has global administrator privileges in your Office 365 organization, sign in to Office 365 and [go to the Security and Compliance Center](go-to-the-securitycompliance-center.md).</span></span>
    
2. <span data-ttu-id="7bf76-263">왼쪽에서 **위협 관리**, **정책**, 선택 및 **스팸 방지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-263">On the left, expand **Threat Management**, choose **Policy**, and then choose **Anti-spam**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="7bf76-264">보안에서 **스팸 방지** 페이지로 바로 이동 하려면 &amp; 준수 센터가이 URL을 사용 하 여: >[https://protection.office.com/?hash=/antispam](https://protection.office.com/?hash=/antispam)</span><span class="sxs-lookup"><span data-stu-id="7bf76-264">To go directly to the **anti-spam** page in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/antispam](https://protection.office.com/?hash=/antispam)</span></span>
  
3. <span data-ttu-id="7bf76-265">**사용자 정의 설정** 탭을 표시할 **사용자 지정** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-265">Choose **Custom** to display the **Custom settings** tab.</span></span> 
    
4. <span data-ttu-id="7bf76-266">**기본 스팸 필터 정책 (항상 ON)** 행을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-266">Expand the **Default spam filter policy (always ON)** row.</span></span> 
    
5. <span data-ttu-id="7bf76-p141">**정책 편집**을 선택 합니다. 기본 스팸 필터 정책에 대 한 설정을 새 페이지에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p141">Choose **Edit policy**. The settings for the default spam filter policy appear in a new page.</span></span>
    
6. <span data-ttu-id="7bf76-269">확장 하 고 **스팸 및 대량 작업**합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-269">Expand **Spam and bulk actions**.</span></span>
    
7. <span data-ttu-id="7bf76-p142">**격리** **(일)에 대 한 보관 스팸** 텍스트 상자에는 Office 365 격리의 메시지 및 파일을 유지 하려면 원하는 시간을 입력 합니다. 기본값은 30 일입니다. 최대 이기도합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-p142">Under **Quarantine**, in the **Retain spam for (days)** text box, enter the amount of time you want Office 365 to retain messages and files in quarantine. The default is 30 days. This is also the maximum.</span></span> 
    
8. <span data-ttu-id="7bf76-273">**저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf76-273">Choose **Save**.</span></span>
    

