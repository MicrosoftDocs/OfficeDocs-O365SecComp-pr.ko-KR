---
title: 일반적인 시나리오 문제를 해결 하는 Office 365 감사 로그를 검색 합니다.
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
description: 조사 손상 된 계정 또는 사용자 사서함에 대 한 전자 메일 전달을 설정 확인 같은 일반적인 문제를 해결 하는데 도움이 되는 Office 365 감사 로그 검색 도구를 사용할 수 있습니다.
ms.openlocfilehash: 930e311712e49214ca2a51e256c29e5f959deab8
ms.sourcegitcommit: c34f1a0d560117153fc9a7b8da8994bc6fc53791
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2018
ms.locfileid: "27123901"
---
# <a name="search-the-office-365-audit-log-to-troubleshoot-common-scenarios"></a><span data-ttu-id="5e360-103">일반적인 시나리오 문제를 해결 하는 Office 365 감사 로그를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-103">Search the Office 365 audit log to troubleshoot common scenarios</span></span>

<span data-ttu-id="5e360-p101">이 문서에서는 일반적인 지원 시나리오 문제를 해결 하는데 도움이 되는 Office 365 감사 로그 검색 도구를 사용 하는 방법에 설명 합니다. 감사 로그를 사용 하 여은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p101">This article describes how to use the Office 365 audit log search tool to help you troubleshoot common support scenarios. This includes using the audit log to:</span></span>

- <span data-ttu-id="5e360-106">손상 된 계정에 액세스 하는 데 사용 하는 컴퓨터의 IP 주소를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-106">Find the IP address of the computer used to access a compromised account</span></span>
- <span data-ttu-id="5e360-107">사용자 사서함에 대 한 전자 메일 전달을 설정 결정</span><span class="sxs-lookup"><span data-stu-id="5e360-107">Determine who set up email forwarding for a mailbox</span></span>
- <span data-ttu-id="5e360-108">사용자가 사서함의 전자 메일 항목을 삭제 하는 경우 결정</span><span class="sxs-lookup"><span data-stu-id="5e360-108">Determine if a user deleted email items in their mailbox</span></span>
- <span data-ttu-id="5e360-109">사용자는 받은 편지함 규칙을 만든 경우 결정</span><span class="sxs-lookup"><span data-stu-id="5e360-109">Determine if a user created an inbox rule</span></span>

## <a name="using-the-office-365-audit-log-search-tool"></a><span data-ttu-id="5e360-110">Office 365 감사 로그 검색 도구를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="5e360-110">Using the Office 365 audit log search tool</span></span>

<span data-ttu-id="5e360-p102">이 문서에서 설명 하는 문제해결 시나리오의 각 옵션은 Office 365 보안 및 규정 준수 센터의 감사 로그 검색 도구를 사용 하 여에 따라 다릅니다. 이 섹션 감사 로그를 검색 하는 데 필요한 사용 권한을 나열 하 고 액세스 하 고 감사 로그 검색을 실행 하는 단계에 설명 합니다. 각 시나리오 섹션에서는 감사 로그 검색 쿼리를 구성 하는 방법 및 검색 조건과 일치 하는 감사 레코드의 세부 정보에서 찾을 대상을 하는 방법에 대 한 특정 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p102">Each of the troubleshooting scenarios described in this article are based on using the audit log search tool in the Office 365 Security & Compliance Center. This section lists the permissions required to search the audit log and describes the steps to access and run audit log searches. Each scenario section provides specific guidance about how to configure an audit log search query and what to look for in the detailed information in the audit records that match the search criteria.</span></span>

### <a name="permissions-required-to-use-the-audit-log-search-tool"></a><span data-ttu-id="5e360-114">감사 로그 검색 도구를 사용 하 여 필요한 사용 권한</span><span class="sxs-lookup"><span data-stu-id="5e360-114">Permissions required to use the audit log search tool</span></span>

<span data-ttu-id="5e360-p103">보기 전용 감사 로그 또는 감사 로그 역할 Exchange Online에 할당할 Office 365 감사 로그를 검색 해야 합니다. 기본적으로 이러한 역할은 Exchange 관리 센터에서 **사용 권한** 페이지에서 준수 관리 및 조직 관리 역할 그룹에 할당 됩니다. 자세한 내용은 [관리 역할 그룹 Exchange Online을](https://go.microsoft.com/fwlink/p/?LinkID=730688)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="5e360-p103">You have to be assigned the View-Only Audit Logs or Audit Logs role in Exchange Online to search the Office 365 audit log. By default, these roles are assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. For more information, see [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).</span></span>

### <a name="running-audit-log-searches"></a><span data-ttu-id="5e360-118">실행 중인 감사 로그 검색</span><span class="sxs-lookup"><span data-stu-id="5e360-118">Running audit log searches</span></span>

<span data-ttu-id="5e360-p104">이 섹션에서는 만들고 감사 로그 검색을 실행 하기 위한 기본 사항에 설명 합니다. 이 문서의 각 문제해결 시나리오에 대 한 시작 지점으로 이러한 지침을 따르십시오. 보다 자세한 단계별 지침은 [Office 365 보안 및 규정 준수 센터에서 감사 로그 검색 ](search-the-audit-log-in-security-and-compliance.md#step-1-run-an-audit-log-search)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="5e360-p104">This section describes the basics for creating and running audit log searches. Use these instructions as a starting point for each troubleshooting scenario in this article. For more detailed step-by-step instructions, see [Search the audit log in the Office 365 Security & Compliance Center ](search-the-audit-log-in-security-and-compliance.md#step-1-run-an-audit-log-search).</span></span>

1. <span data-ttu-id="5e360-122">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-122">Go to [https://protection.office.com](https://protection.office.com).</span></span>
  
2. <span data-ttu-id="5e360-123">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-123">Sign in to Office 365 using your work or school account.</span></span>

3. <span data-ttu-id="5e360-124">보안 및 규정 준수 센터의 왼쪽된 창에서 **검색 및 조사**클릭 > **감사 로그 검색**합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-124">In the left pane of the Security & Compliance Center, click **Search & investigation** > **Audit log search**.</span></span>
    
    <span data-ttu-id="5e360-125">**감사 로그 검색** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-125">The **Audit log search** page is displayed.</span></span> 
    
    ![조건을 구성 하 고 검색을 실행 하는 검색을 클릭](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
4. <span data-ttu-id="5e360-p105">다음 검색 조건을 구성할 수 있습니다. 참고가 문서의 각 문제해결 시나리오 이러한 필드를 구성 하는 구체적인 지침을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p105">You can configure the following search criteria. Note that each troubleshooting scenario in this article will recommend specific guidance for configuring these fields.</span></span>
    
    <span data-ttu-id="5e360-p106">a. **활동** -를 검색할 수 있는 작업을 표시 하려면 드롭다운 목록을 클릭 합니다. 검색을 실행 하 고 나면 선택한 작업에 대 한 감사 레코드에만 표시 됩니다. **모든 작업에 대 한 결과 표시** 를 선택 하면 다른 검색 조건을 만족 하는 모든 작업에 대 한 결과가 표시 됩니다. 또한이 필드는 비워둡니다 문제해결 시나리오 중 일부에 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p106">a. **Activities** - Click the drop-down list to display the activities that you can search for. After you run the search, only the audit records for the selected activities are displayed. Selecting **Show results for all activities** will display results for all activities that meet the other search criteria. You'll also have to leave this field blank in some of the troubleshooting scenarios.</span></span>
    
    <span data-ttu-id="5e360-p107">b. **시작 날짜** 및 **종료 날짜** -기간 내에 발생 한 이벤트를 표시 하려면 날짜 및 시간 범위를 선택 합니다. 지난 7 일간 기본적으로 선택 됩니다. 날짜 및 시간에서 utc (협정 세계시) 형식 나와 있습니다. 지정할 수 있는 최대 날짜 범위에는 90 일입니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p107">b. **Start date** and **End date** - Select a date and time range to display the events that occurred within that period. The last seven days are selected by default. The date and time are presented in Coordinated Universal Time (UTC) format. The maximum date range that you can specify is 90 days.</span></span>

    <span data-ttu-id="5e360-p108">c. **사용자** -검색을 표시 하려면이 상자에 다음 선택 된 하나 이상의 사용자가 클릭에 대 한 결과입니다. 이 상자에서 선택한 사용자에 의해 수행 선택된 된 작업에 대 한 감사 레코드는 결과의 목록에 표시 됩니다. 이 상자는 조직에서 모든 사용자 (및 서비스 계정)에 대 한 항목을 반환 하려면 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p108">c. **Users** - Click in this box and then select one or more users to display search results for. Audit records for the selected activity performed by the users you select in this box are displayed in the list of results. Leave this box blank to return entries for all users (and service accounts) in your organization.</span></span>
    
    <span data-ttu-id="5e360-p109">d. **파일, 폴더 또는 사이트** -지정된 된 키워드를 포함 하는 폴더의 파일에 관련 된 작업에 대 한 검색 파일 또는 폴더 이름 중 일부 또는 전부를 입력 합니다. 파일 또는 폴더의 URL을 지정할 수도 있습니다. URL을 사용 하는 경우 전체 URL 경로 입력 해야 하거나 방금는 URL의 일부를 입력 하는 경우 모든 특수 문자나 공백을 포함 하지 마십시오. 이 상자는 조직에서 모든 파일 및 폴더에 대 한 항목을 반환 하려면 비워 둡니다. 이 필드는 비워 문제 해결 하는 모든 시나리오에서이 문서에 유의 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p109">d. **File, folder, or site** - Type some or all of a file or folder name to search for activity related to the file of folder that contains the specified keyword. You can also specify a URL of a file or folder. If you use a URL, be sure the type the full URL path or if you just type a portion of the URL, don't include any special characters or spaces. Leave this box blank to return entries for all files and folders in your organization. Note that this field is left blank in all the troubleshooting scenarios in this article.</span></span>
    
5. <span data-ttu-id="5e360-149">검색 조건을 사용 하 여 검색을 실행 하려면 **검색** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-149">Click **Search** to run the search using your search criteria.</span></span> 
    
    <span data-ttu-id="5e360-p110">검색 결과 로드 하 고 잠시 후에 표시 하는 **결과** 아래에서 **감사 로그 검색** 페이지입니다. 각각 다음 섹션을 특정 문제해결 시나리오에 대 한 확인 해야할 사항에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p110">The search results are loaded, and after a few moments they are displayed under **Results** on the **Audit log search** page. Each to the following sections will provide guidance about things to look for the specific troubleshooting scenario.</span></span>

    <span data-ttu-id="5e360-152">보기, 필터링 또는 감사 로그 검색 결과 내보내기 (영문) 하는 방법에 대 한 자세한 내용은 다음을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-152">For more information about viewing, filtering, or exporting audit log search results, see:</span></span>

    - [<span data-ttu-id="5e360-153">검색 결과 보기</span><span class="sxs-lookup"><span data-stu-id="5e360-153">View search results</span></span>](search-the-audit-log-in-security-and-compliance.md#step-2-view-the-search-results)
    - [<span data-ttu-id="5e360-154">검색 결과 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-154">Filter search results</span></span>](search-the-audit-log-in-security-and-compliance.md#step-3-filter-the-search-results)
    - [<span data-ttu-id="5e360-155">검색 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="5e360-155">Export search results</span></span>](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file)

## <a name="finding-the-ip-address-of-the-computer-used-to-access-a-compromised-account"></a><span data-ttu-id="5e360-156">손상 된 계정에 액세스 하는 데 사용 하는 컴퓨터의 IP 주소 찾기 (영문)</span><span class="sxs-lookup"><span data-stu-id="5e360-156">Finding the IP address of the computer used to access a compromised account</span></span>

<span data-ttu-id="5e360-p111">모든 사용자에 의해 수행 되는 활동에 해당 하는 IP 주소는 대부분의 감사 레코드에 포함 됩니다. 사용 하는 클라이언트에 대 한 정보는 감사 레코드에도 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p111">The IP address corresponding to an activity performed by any user is included in most audit records. Information about the client used is also included in the audit record.</span></span>

<span data-ttu-id="5e360-159">이 시나리오에 대 한 감사 로그 검색 쿼리를 구성 하는 방법을 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-159">Here's how to configure an audit log search query for this scenario:</span></span>

<span data-ttu-id="5e360-p112">**활동** -사용자 사례와 관련 하는 경우에 특정 활동에 대 한 검색을 선택 합니다. 문제해결 손상 된 계정에 대 한 **Exchange 사서함 작업**아래에서 **사용자가 사서함에 로그인** 하는 작업을 선택 하는 것이 좋습니다. 이 사서함에 로그인 할 때 사용 된 IP 주소를 표시 하는 감사 레코드 반환 됩니다. 그렇지 않은 경우이 필드를 비워 모든 활동에 대 한 감사 레코드를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p112">**Activities** - If relevant to your case, select a specific activity to search for. For troubleshooting compromised accounts, consider selecting the **User signed in to mailbox** activity under **Exchange mailbox activities**. This will return auditing records showing the IP address that was use when signing in to the mailbox. Otherwise, leave this field blank to return audit records for all activities.</span></span> 

> [!TIP]
> <span data-ttu-id="5e360-p113">이 필드를 비워 되돌아옵니다 **UserLoggedIn** 활동은 다른 사용자가 로그인 Office 365 사용자 계정을 나타내는 Azure Active Directory 활동은. 검색 결과에서 필터링을 사용 하 여 **UserLoggedIn** 감사 레코드를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p113">Leaving this field blank will  return **UserLoggedIn** activities, which is an Azure Active Directory activity that indicates that someone has signed in to an Office 365 user account. Use filtering in the search results to display the **UserLoggedIn** audit records.</span></span>

<span data-ttu-id="5e360-166">**시작 날짜와** **종료 날짜** -사용자 조사 적용 되는 날짜 범위를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-166">**Start date** and **End date** - Select a date range that's applicable to your investigation.</span></span>

<span data-ttu-id="5e360-p114">**사용자가** -손상 된 계정을 조사 하는 경우 해당 계정이 손상 된 사용자를 선택 합니다. 그러면 해당 사용자 계정에 의해 수행 되는 작업에 대 한 감사 레코드 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p114">**Users** - If you're investigating a compromised account, select the user whose account was compromised. This will return audit records for activities performed by that user account.</span></span>

<span data-ttu-id="5e360-169">**파일, 폴더 또는 사이트** -이 필드를 공백으로 열어둡니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-169">**File, folder, or site** - Leave this field blank.</span></span>

<span data-ttu-id="5e360-p115">검색을 실행 한 후 각 작업에 대 한 IP 주소는 검색 결과에서 **IP 주소** 열에 표시 됩니다. 플라이 아웃 페이지에서 자세한 정보를 보려면 검색 결과에서 레코드를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p115">After you run the search, the IP address for each activity is displayed in the **IP address** column in the search results. Click the record in the search results to view more detailed information on the flyout page.</span></span>

## <a name="determining-who-set-up-email-forwarding-for-a-mailbox"></a><span data-ttu-id="5e360-172">사용자 사서함에 대 한 전자 메일 전달을 설정 결정</span><span class="sxs-lookup"><span data-stu-id="5e360-172">Determining who set up email forwarding for a mailbox</span></span>

<span data-ttu-id="5e360-p116">전자 메일 전달을 사서함에 대해 구성 되 면 사서함으로 전송 되는 전자 메일 메시지는 다른 사서함에 전달 됩니다. 내부 또는 조직 외부의 사용자에 게 메시지를 전달할 수 있습니다. 전자 메일 전달을 사서함에 설정 하는 경우 사용 되는 기본 Exchange Online cmdlet은 **Set-mailbox**입니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p116">When email forwarding is configured for a mailbox, email messages that are sent to the mailbox are forwarded to another mailbox. Messages can be forwarded to users inside or outside of your organization. When email forwarding is set up on a mailbox, the underlying Exchange Online cmdlet that's used is **Set-Mailbox**.</span></span>

<span data-ttu-id="5e360-176">이 시나리오에 대 한 감사 로그 검색 쿼리를 구성 하는 방법을 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-176">Here's how to configure an audit log search query for this scenario:</span></span>

<span data-ttu-id="5e360-p117">**활동** -이 필드는 모든 작업에 대 한 감사 레코드를 반환 하는 검색 되도록 빈 열어둡니다. 이 작업을 모두 반환 하려면 **Set-mailbox** cmdlet에 관련 된 레코드를 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p117">**Activities** - Leave this field blank so that the search returns audit records for all activities. This is necessary to return any audit records related to the **Set-Mailbox** cmdlet.</span></span>

<span data-ttu-id="5e360-179">**시작 날짜와** **종료 날짜** -사용자 조사 적용 되는 날짜 범위를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-179">**Start date** and **End date** - Select a date range that's applicable to your investigation.</span></span>

<span data-ttu-id="5e360-p118">**사용자가** -특정 사용자에 대 한 문제를 전달 하는 전자 메일을를 조사 하는 경우가 아니면이 필드를 비워 둡니다. 모든 사용자에 대 한 전자 메일 전달을 설정 된 경우를 식별 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p118">**Users** - Unless you're investigating a email forwarding issue for a specific user, leave this field blank. This will help you identify if email forwarding was set up for any user.</span></span>

<span data-ttu-id="5e360-182">**파일, 폴더 또는 사이트** -이 필드를 공백으로 열어둡니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-182">**File, folder, or site** - Leave this field blank.</span></span>

<span data-ttu-id="5e360-p119">검색을 실행 하면 검색 결과 페이지에서 **결과 필터링** 을 클릭 합니다. **작업** 열 머리글 아래에 있는 상자를 **Set-mailbox** cmdlet와 관련 된 감사 레코드만 표시 되도록 **Set-mailbox** 를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p119">After you run the search, click **Filter results** on the search results page. In the box under **Activity** column header, type **Set-Mailbox** so that only audit records related to the **Set-Mailbox** cmdlet are displayed.</span></span>

![감사 로그 검색의 결과 필터링합니다.](media/emailforwarding1.png)

<span data-ttu-id="5e360-p120">이 시점에서 전자 메일을 전달 하는 작업은 관련이 있는지 확인 하려면 각 감사 레코드의 세부 정보를 확인 해야 합니다. **세부 정보** 플라이 아웃 페이지를 표시 하려면 감사 레코드를 클릭 한 다음 **자세한 정보**를 클릭 합니다. 다음 스크린샷 및 설명 중요 한 정보는 사서함에서 전자 메일 전달을 나타내는 정보 설정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p120">At this point, you have to look at the details of each audit record to determine if the activity is related to email forwarding. Click the audit record to display the **Details** flyout page, and then click **More information**. The following screenshot and descriptions highlights the information that indicates email forwarding was set on the mailbox.</span></span>

![감사 레코드에서 자세한 정보](media/emailforwarding2.png)

<span data-ttu-id="5e360-p121">a. 전자 메일을 전달 하는 사서함의 별칭 설정 된 **ObjectId** 필드에 표시 됩니다. 이 사서함의 검색 결과 페이지에 있는 **항목** 열에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p121">a. In the **ObjectId** field, the alias of the mailbox that email forwarding was set on is displayed. This mailbox is also displayed on the **Item** column in the search results page.</span></span>

<span data-ttu-id="5e360-p122">b. **매개 변수** 필드에 값 *ForwardingSmtpAddress* 사서함에서 전자 메일을 앞으로 설정 되어 있는지를 나타냅니다. 이 예제에서는 alpinehouse.onmicrosoft.com 조직 외부에 있는 전자 메일 주소 mike@contoso.com에 메일을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p122">b. In the **Parameters** field, The value *ForwardingSmtpAddress* indicates that email forward has been set on the mailbox. In this example, mail is being forwarded to the email address mike@contoso.com, which is outside of the alpinehouse.onmicrosoft.com organization.</span></span>

<span data-ttu-id="5e360-p123">*DeliverToMailboxAndForward* 매개 변수에 대 한 c. 값이 *True* 이면 sarad@alpinehouse.onmicrosoft.com *및* 배달 된 메시지의 복사본을 \*ForwardingSmtpAddress 하 여 지정 된 전자 메일 주소로 전달 하 \*매개 변수는이 예제의 mike@contoso.com 합니다. *DeliverToMailboxAndForward* 매개 변수 값은 *False*로 설정 하는 경우 *ForwardingSmtpAddress* 매개 변수에 의해 지정 된 주소로 전자 메일 전달만 됩니다. **ObjectId** 필드에 지정 된 사서함에 배달 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p123">c. The *True* value for the *DeliverToMailboxAndForward* parameter indicates that a copy of message delivered to sarad@alpinehouse.onmicrosoft.com *and* is forwarded to the email address specified by the *ForwardingSmtpAddress* parameter, which in this example is mike@contoso.com. If the value for the *DeliverToMailboxAndForward* parameter is set to *False*, then email is only forwarded to the address specified by the *ForwardingSmtpAddress* parameter. It's not delivered to the mailbox specified in the **ObjectId** field.</span></span>

<span data-ttu-id="5e360-p124">d. **UserId** 필드 **ObjectId** 필드 필드에 지정 된 사서함에서 전자 메일 전달을 설정 하는 사용자를 나타냅니다. 이 사용자가 검색 결과 페이지에서 **사용자** 열에도 표시 됩니다. 이 경우에 사서함의 소유자의 사서함에서 전자 메일 전달을 설정 되어있는지 보입니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p124">d. The **UserId** field indicates the user who set email forwarding on the mailbox specified in the **ObjectId** field field. This user is also displayed in the **User** column on the search results page. In this case, it seems that the owner of the mailbox set email forwarding on her mailbox.</span></span>

<span data-ttu-id="5e360-204">사서함에서 전자 메일 전달을 설정 해서는 안됩니다 있는지를 확인 하는 경우에 Exchange Online PowerShell에서 다음 명령을 실행 하 여 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-204">If you determine that email forwarding shouldn't be set on the mailbox, you can remove it by running the following command in Exchange Online PowerShell:</span></span>

```
Set-Mailbox <mailbox alias> -ForwardingSmtpAddress $null 
```

<span data-ttu-id="5e360-205">착신 전환으로 전자 메일을 관련 된 매개 변수에 대 한 자세한 내용은 [Set-mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox) 문서를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="5e360-205">See the [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox) article for more information about the parameters related to email forwarding.</span></span>

## <a name="determining-if-a-user-deleted-email-items"></a><span data-ttu-id="5e360-206">사용자 전자 메일 항목을 삭제 하는 경우 결정</span><span class="sxs-lookup"><span data-stu-id="5e360-206">Determining if a user deleted email items</span></span>

<span data-ttu-id="5e360-p125">에 대 한 감사 로그 기록 삭제 하기 전에 전자 메일 항목은 Office 365 감사 로그에 저장 된, 조직에서 각 사용자 사서함에 대해 사용 하도록 설정 하는 사서함 감사 합니다. 또한, SoftDelete 및 HardDelete 사서함 작업 감사에 대해 사용 하도록 설정 해야 합니다. 자세한 내용은 [Office 365의 감사 사서함 사용](enable-mailbox-auditing.md)을 참조 하십시오. 사서함 감사 활성화 된 사용자에 대해 다음 단계를 사용 하 여 삭제 된 전자 메일 항목에 관련 된 이벤트에 대 한 감사 로그를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p125">Before audit log records about deleted email items are saved to the Office 365 audit log, mailbox auditing has to be enabled for each user mailbox in your organization. Additionally, the SoftDelete and HardDelete mailbox actions have to be enabled for auditing. For instructions, see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md). If mailbox auditing is already enabled for users, use the following steps to search the audit log for events related to deleted email items.</span></span>

<span data-ttu-id="5e360-211">이 시나리오에 대 한 감사 로그 검색 쿼리를 구성 하는 방법을 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-211">Here's how to configure an audit log search query for this scenario:</span></span>

<span data-ttu-id="5e360-212">**활동** -아래에서 **Exchange 사서함 활동**을 하나 또는 둘 모두 다음과 같은 작업을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-212">**Activities** - Under **Exchange mailbox activities**, select one or both of the following activities:</span></span>

- <span data-ttu-id="5e360-p126">**지운 편지함 폴더에서 삭제 된 메시지** -이 활동 작업을 감사 하는 **SoftDelete** 사서함에 해당 합니다. 사용자 선택 하 고 **Shift + Delete**키를 눌러 하 여 항목을 영구적으로 삭제 하는 경우에이 작업 기록 됩니다. 항목이 영구적으로 삭제 한 후 사용자를 복구할 수 것 삭제 된 항목 보존 기간이 만료 될 때까지.</span><span class="sxs-lookup"><span data-stu-id="5e360-p126">**Deleted messages from Deleted Items folder** -  This activity corresponds to the **SoftDelete** mailbox auditing action. This activity is also logged when a user permanently deletes an item by selecting it and pressing **Shift+Delete**. After an item is permanently deleted, the user can recover it until the deleted item retention period expires.</span></span>

- <span data-ttu-id="5e360-p127">**사서함에서 메시지를 Purged** -이 활동 작업을 감사 하는 **HardDelete** 사서함에 해당 합니다. 이 사용자가 복구 가능한 항목 폴더에서 항목을 제거 하는 경우에 기록 됩니다. Admins Office 365 보안 및 규정 준수 센터의 콘텐츠 검색 도구를 사용 하 여 검색할 수 및 사용자의 사서함이 보류에 삭제 된 항목 보존 기간이 만료 될 때까지 경과한 복구 항목 또는 더 긴 경우.</span><span class="sxs-lookup"><span data-stu-id="5e360-p127">**Purged messages from mailbox** - This activity corresponds to the **HardDelete** mailbox auditing action. This is logged when a user purges an item from the Recoverable Items folder. Admins can use the Content Search tool in the Office 365 Security & Compliance Center to search for and recover purged items until the deleted item retention period expires or longer if the user's mailbox is on hold.</span></span>

<span data-ttu-id="5e360-219">**시작 날짜와** **종료 날짜** -사용자 조사 적용 되는 날짜 범위를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-219">**Start date** and **End date** - Select a date range that's applicable to your investigation.</span></span>

<span data-ttu-id="5e360-p128">**사용자가** -이 필드에 사용자를 선택 하는 경우, 감사 로그 검색 도구 지정 하면 사용자가 삭제 된 (SoftDeleted 또는 HardDeleted)에 있던 전자 메일 항목에 대 한 감사 레코드를 반환 합니다. 경우에 따라 사용자에 게 전자 메일을 삭제 아닐 수 있습니다는 사서함 소유자.</span><span class="sxs-lookup"><span data-stu-id="5e360-p128">**Users** - If you select a user in this field, the audit log search tool will return audit records for email items that were deleted (SoftDeleted or HardDeleted) by the user you specify. In some cases, the user who deletes an email might not be the mailbox owner.</span></span>

<span data-ttu-id="5e360-222">**파일, 폴더 또는 사이트** -이 필드를 공백으로 열어둡니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-222">**File, folder, or site** - Leave this field blank.</span></span>

<span data-ttu-id="5e360-p129">검색을 실행 하 고 나면 일시 삭제 된 항목에 대 한 또는 하드 삭제 된 항목에 대 한 감사 레코드를 표시 하려면 검색 결과 필터링 할 수 있습니다. **세부 정보** 플라이 아웃 페이지를 표시 하려면 감사 레코드를 클릭 한 다음 **자세한 정보**를 클릭 합니다. 예: 제목 줄 및 삭제 된 경우 해당 항목의 위치는 삭제 된 항목에 대 한 자세한 내용은 **AffectedItems** 필드에 표시 됩니다. 다음 스크린샷 일시 삭제 된 항목 및 하드 삭제 된 항목에서 **AffectedItems** 필드의 예를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p129">After you run the search, you can filter the search results to display the audit records for soft-deleted items or for hard-deleted items. Click the audit record to display the **Details** flyout page, and then click **More information**. Additional information about the deleted item, such as the subject line and the location of the item when it was deleted, is displayed in the **AffectedItems** field. The following screenshots show an example of the **AffectedItems** field from a soft-deleted item and a hard-deleted item.</span></span>

<span data-ttu-id="5e360-227">**일시 삭제 된 항목에 대 한 AffectedItems 필드의 예**</span><span class="sxs-lookup"><span data-stu-id="5e360-227">**Example of AffectedItems field for soft-deleted item**</span></span>

![일시 삭제 된 항목에 대 한 감사 레코드](media/softdeleteditem.png)

<span data-ttu-id="5e360-229">**하드 삭제 된 항목에 대 한 AffectedItems 필드의 예**</span><span class="sxs-lookup"><span data-stu-id="5e360-229">**Example of AffectedItems field for hard-deleted item**</span></span>

![하드 삭제 된 전자 메일 항목에 대 한 감사 레코드](media/harddeleteditem.png)

### <a name="recovering-deleted-email-items"></a><span data-ttu-id="5e360-231">삭제 된 전자 메일 항목 복구</span><span class="sxs-lookup"><span data-stu-id="5e360-231">Recovering deleted email items</span></span>

<span data-ttu-id="5e360-p130">사용자가 삭제 된 항목 보존 기간이 만료 되지 않은 경우 일시 삭제 된 항목을 복구할 수 있습니다. Exchange Online의 기본 삭제 된 항목 보존 기간 14 일 이지만 관리자가이 설정을 최대 30 일에을 높일 수 있습니다. 사용자가 삭제 된 항목을 복구 하는 중에 대 한 지침은 [삭제 된 항목 또는 Outlook Web App에서 전자 메일을 복구](https://support.office.com/article/Recover-deleted-items-or-email-in-Outlook-Web-App-C3D8FC15-EEEF-4F1C-81DF-E27964B7EDD4) 문서를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p130">Users can recover soft-deleted items if the deleted items retention period has not expired. In Exchange Online, the default deleted items retention period is 14 days, but admins can increase this setting to a maximum of 30 days. Point users to the [Recover deleted items or email in Outlook Web App](https://support.office.com/article/Recover-deleted-items-or-email-in-Outlook-Web-App-C3D8FC15-EEEF-4F1C-81DF-E27964B7EDD4) article for instructions on recovering deleted items.</span></span>

<span data-ttu-id="5e360-p131">앞에서 설명한 것 처럼 관리자가 삭제 된 항목 보존 기간 만료 되지 않은 경우 하드 삭제 된 항목을 복구 하거나 기다리는 경우에이 사서함은 수, 항목은 보존 기간이 만료 될 때까지 유지 되는 경우. 콘텐츠 검색을 실행 하면 검색 쿼리와 일치 하는 경우의 복구 가능한 항목 폴더에서 일시 삭제 하 고 하드 삭제 된 항목 검색 결과에 반환 됩니다. 콘텐츠 검색을 실행 하는 방법에 대 한 자세한 내용은 [Office 365의 콘텐츠 검색](content-search.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="5e360-p131">As previously explained, admins might be able to recover hard-deleted items if the deleted item retention period has not expired or if the mailbox is on hold, in which case items are retained until the hold duration expires. When you run a content search, soft-deleted and hard-deleted items in the Recoverable Items folder are returned in the search results if they match the search query. For more information about running content searches, see [Content Search in Office 365](content-search.md).</span></span>

> [!TIP]
> <span data-ttu-id="5e360-238">삭제 된 전자 메일 항목을 검색 하려면 감사 레코드의 **AffectedItems** 필드에 표시 되는 제목 줄의 일부 또는 전체를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-238">To search for deleted email items, search for all or part of the subject line that's displayed in the **AffectedItems** field in the audit record.</span></span>

## <a name="determining-if-a-user-created-an-inbox-rule"></a><span data-ttu-id="5e360-239">사용자는 받은 편지함 규칙을 만든 경우 결정</span><span class="sxs-lookup"><span data-stu-id="5e360-239">Determining if a user created an inbox rule</span></span>

<span data-ttu-id="5e360-p132">사용자가 Exchange Online 사서함에 대 한 받은 편지함 규칙을 만들 때 해당 감사 레코드 감사 로그에 저장 됩니다. 받은 편지함 규칙에 대 한 자세한 내용은 다음을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p132">When users create an inbox rule for their Exchange Online mailbox, a corresponding audit record is saved to the audit log. For more information about inbox rules, see:</span></span>

- [<span data-ttu-id="5e360-242">받은 편지함 규칙을 사용 하 여 웹에 있는 Outlook에서</span><span class="sxs-lookup"><span data-stu-id="5e360-242">Use inbox rules in Outlook on the web</span></span>](https://support.office.com/article/use-inbox-rules-in-outlook-on-the-web-8400435c-f14e-4272-9004-1548bb1848f2)
- [<span data-ttu-id="5e360-243">규칙을 사용 하 여 Outlook에서 전자 메일 메시지를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-243">Manage email messages in Outlook by using rules</span></span>](https://support.office.com/article/Manage-email-messages-by-using-rules-C24F5DEA-9465-4DF4-AD17-A50704D66C59)

<span data-ttu-id="5e360-244">이 시나리오에 대 한 감사 로그 검색 쿼리를 구성 하는 방법을 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-244">Here's how to configure an audit log search query for this scenario:</span></span>

<span data-ttu-id="5e360-245">**활동** - **Exchange 사서함 활동**을 선택 아래에서 **New-inboxrule 만들기/수정/를 사용 하도록 설정/받은 편지함 규칙을 사용 하지 않도록 설정**합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-245">**Activities** - Under **Exchange mailbox activities**, select **New-InboxRule Create/modify/enable/disable inbox rule**.</span></span>

<span data-ttu-id="5e360-246">**시작 날짜와** **종료 날짜** -사용자 조사 적용 되는 날짜 범위를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-246">**Start date** and **End date** - Select a date range that's applicable to your investigation.</span></span>

<span data-ttu-id="5e360-p133">**사용자가** -특정 사용자를 조사 하는 경우가 아니면이 필드를 비워 둡니다. 모든 사용자에 의해 설정 된 새 받은 편지함 규칙을 식별 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p133">**Users** - Unless you're investigating a specific user, leave this field blank. This will help you identify new inbox rules set up by any user.</span></span>

<span data-ttu-id="5e360-249">**파일, 폴더 또는 사이트** -이 필드를 공백으로 열어둡니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-249">**File, folder, or site** - Leave this field blank.</span></span>

<span data-ttu-id="5e360-p134">검색을 실행 하 고 나면이 활동에 대 한 모든 감사 레코드 검색 결과에 표시 됩니다. **세부 정보** 플라이 아웃 페이지를 표시 하는 감사 레코드를 클릭 한 다음 **자세한 정보**를 클릭 합니다. 받은 편지함 규칙 설정에 대 한 정보는 **매개 변수** 필드에 표시 됩니다. 다음 스크린샷 및 설명 받은 편지함 규칙에 대 한 정보를 강조 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p134">After you run the search, any audit records for this activity are displayed in the search results. Click an audit record to display the **Details** flyout page, and then click **More information**. Information about the inbox rule settings are displayed in the **Parameters** field. The following screenshot and descriptions highlights the information about inbox rules.</span></span>

![새 받은 편지함 규칙에 대 한 감사 레코드](media/NewInboxRuleRecord.png)

<span data-ttu-id="5e360-p135">a. **ObjectId** 필드에는 받은 편지함 규칙의 전체 이름이 표시 됩니다. 이 이름은 사용자의 사서함 (예: SaraD)의 별칭 및 받은 편지함 규칙 (예 "메시지 이동 관리에서")의 이름이 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p135">a. In the **ObjectId** field, the full name of the inbox rule is displayed. This name includes the alias of the user's mailbox (for example, SaraD) and the name of the inbox rule (for example, "Move messages from admin").</span></span>

<span data-ttu-id="5e360-p136">b. **매개 변수** 필드에는 받은 편지함 규칙의 조건이 표시 됩니다. 이 예제에서는 조건에서 \*\* 매개 변수에 의해 지정 됩니다. *From* 매개 변수에 대해 정의 된 값 admin@alpinehouse.onmicrosoft.com가 보낸 전자 메일에서 작동 하는 받은 편지함 규칙을 나타냅니다. 받은 편지함 규칙의 조건을 정의 하는데 사용할 수 있는 매개 변수 전체 목록 [New-inboxrule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) 문서를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="5e360-p136">b. In the **Parameters** field, the condition of the inbox rule is displayed. In this example, the condition is specified by the *From* parameter. The value defined for the *From* parameter indicates that the inbox rule acts on email sent by admin@alpinehouse.onmicrosoft.com. For a complete list of the parameters that can be used to define conditions of inbox rules, see the [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) article.</span></span>

<span data-ttu-id="5e360-p137">c. *MoveToFolder* 매개 변수는 받은 편지함 규칙;에 대 한 작업을 지정합니다. 이 예제에서는 admin@alpinehouse.onmicrosoft.com에서 받은 메시지 *AdminSearch*라는 폴더로 이동 합니다. 또한 매개 변수는 받은 편지함 규칙의 동작을 정의 하는 데 수의 전체 목록은 [New-inboxrule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) 문서를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p137">c. The *MoveToFolder* parameter specifies the action for the inbox rule; in this example, messages received from admin@alpinehouse.onmicrosoft.com are moved to the folder named *AdminSearch*. Also see the [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) article for a complete list of parameters that can used to define the action of an inbox rule.</span></span>

<span data-ttu-id="5e360-p138">d. **UserId** 필드 **ObjectId** 필드에 지정 된 받은 편지함 규칙을 만든 사용자를 나타냅니다. 이 사용자가 검색 결과 페이지에서 **사용자** 열에도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e360-p138">d. The **UserId** field indicate the user who created the inbox rule specified in the **ObjectId** field. This user is also displayed in the **User** column on the search results page.</span></span>