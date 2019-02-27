---
title: Office 365 조 직에서 전자 메일 메시지 검색 및 삭제-관리자 도움말
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 3526fd06-b45f-445b-aed4-5ebd37b3762a
description: Office 365 보안 &amp; 및 준수 센터의 검색 및 제거 기능을 사용 하 여 조직의 모든 사서함에서 전자 메일 메시지를 검색 하 고 삭제 합니다.
ms.openlocfilehash: 15d67e42e4bdc63838f7ec1701d643391fa5c552
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296861"
---
# <a name="search-for-and-delete-email-messages-in-your-office-365-organization---admin-help"></a><span data-ttu-id="69b37-103">Office 365 조 직에서 전자 메일 메시지 검색 및 삭제-관리자 도움말</span><span class="sxs-lookup"><span data-stu-id="69b37-103">Search for and delete email messages in your Office 365 organization - Admin Help</span></span>

<span data-ttu-id="69b37-104">**이 문서는 관리자를 위한 것입니다. 삭제 하려는 사서함의 항목을 찾으려고 하나요? [빠른 검색을 사용 하 여 메시지 또는 항목 찾기](https://support.office.com/article/69748862-5976-47b9-98e8-ed179f1b9e4d) 참조**|</span><span class="sxs-lookup"><span data-stu-id="69b37-104">**This article is for administrators. Are you trying to find items in your mailbox that you want to delete? See [Find a message or item with Instant Search](https://support.office.com/article/69748862-5976-47b9-98e8-ed179f1b9e4d)**|</span></span>
   
<span data-ttu-id="69b37-p101">Office 365의 콘텐츠 검색 기능을 사용 하 여 조직의 모든 사서함에서 전자 메일 메시지를 검색 하 고 삭제할 수 있습니다. 이를 통해 다음과 같은 잠재적으로 유해 하거나 위험성이 높은 전자 메일을 찾고 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-p101">You can use the Content Search feature in Office 365 to search for and delete an email message from all mailboxes in your organization. This can help you find and remove potentially harmful or high-risk email, such as:</span></span>
  
- <span data-ttu-id="69b37-107">위험한 첨부 파일 또는 바이러스를 포함 하는 메시지</span><span class="sxs-lookup"><span data-stu-id="69b37-107">Messages that contain dangerous attachments or viruses</span></span>
    
- <span data-ttu-id="69b37-108">피싱 메시지</span><span class="sxs-lookup"><span data-stu-id="69b37-108">Phishing messages</span></span>
    
- <span data-ttu-id="69b37-109">중요한 데이터가 포함된 메시지</span><span class="sxs-lookup"><span data-stu-id="69b37-109">Messages that contain sensitive data</span></span>
    
> [!CAUTION]
> <span data-ttu-id="69b37-110">검색 및 삭제는 필요한 권한이 할당 된 모든 사용자가 조직의 사서함에서 전자 메일 메시지를 삭제할 수 있도록 하는 강력한 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-110">Search and purge is a powerful feature that allows anyone that is assigned the necessary permissions to delete email messages from mailboxes in your organization.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="69b37-111">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="69b37-111">Before you begin</span></span>

- <span data-ttu-id="69b37-p102">콘텐츠 검색을 만들고 실행 하려면 **eDiscovery 관리자** 역할 그룹의 구성원 이거나 **준수 검색** 관리 역할을 할당 받아야 합니다. 메시지를 삭제 하려면 **조직 관리** 역할 그룹의 구성원 이거나 **검색 및 삭제** 관리 역할을 할당 받아야 합니다. 역할 그룹에 사용자를 추가 하는 방법에 대 한 자세한 내용은 [사용자에 게 Office 365 보안 & 준수 센터에 대 한 액세스 권한을 부여](grant-access-to-the-security-and-compliance-center.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="69b37-p102">To create and run a Content Search, you have to be a member of the **eDiscovery Manager** role group or be assigned the **Compliance Search** management role. To delete messages, you have to be a member of the **Organization Management** role group or be assigned the **Search And Purge** management role. For information about adding users to a role group, see [Give users access to the Office 365 Security & Compliance Center](grant-access-to-the-security-and-compliance-center.md).</span></span>
    
- <span data-ttu-id="69b37-p103">메시지를 삭제 하려면 Security & 준수 센터 PowerShell을 사용 해야 합니다. 연결 방법에 대 한 지침은 [2 단계](#step-2-connect-to-security-amp-compliance-center-powershell) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="69b37-p103">You have to use Security & Compliance Center PowerShell to delete messages. See [Step 2](#step-2-connect-to-security-amp-compliance-center-powershell) for instructions about how to connect.</span></span>
    
- <span data-ttu-id="69b37-p104">한 번에 최대 10 개의 항목을 제거할 수 있습니다. 메시지를 검색 하 고 제거 하는 기능은 인시던트 응답 도구인 것 이므로이 제한을 통해 메시지를 사서함에서 빠르게 제거할 수 있습니다. 이 기능은 사용자 사서함을 정리 하기 위한 것이 아닙니다. 10 개 보다 많은 항목을 삭제 하려면 Exchange Online PowerShell에서 **검색-DeleteContent** 명령을 사용 하면 됩니다. [메시지 검색 및 삭제-관리자 도움말](search-for-and-delete-messagesadmin-help.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69b37-p104">A maximum of 10 items per mailbox can be removed at one time. Because the capability to search for and remove messages is intended to be an incident-response tool, this limit helps ensure that messages are quickly removed from mailboxes. This feature isn't intended to clean up user mailboxes. To delete more than 10 items, you can use the **Search-Mailbox -DeleteContent** command in Exchange Online PowerShell. See [Search for and delete messages - Admin help](search-for-and-delete-messagesadmin-help.md).</span></span>
    
- <span data-ttu-id="69b37-p105">검색 및 삭제 작업을 수행 하 여 항목을 삭제할 수 있는 콘텐츠 검색의 최대 사서함 수는 5만입니다. [1 단계](#step-1-create-a-content-search-to-find-the-message-to-delete)에서 만든 콘텐츠 검색에 원본 사서함이 5만 개 보다 많은 경우에는 제거 작업 (3 단계에서 생성)이 실패 합니다. 5만 개 이상의 사서함에서 검색 및 제거 작업을 수행 하는 방법에 대 한 [자세한 내용은 추가 정보](#more-information) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="69b37-p105">The maximum number of mailboxes in a Content Search that you can delete items in by doing a search and purge action is 50,000. If the Content Search (that you create in [Step 1](#step-1-create-a-content-search-to-find-the-message-to-delete)) has more than 50,000 source mailboxes, the purge action (that you create in Step 3) will fail. See the [More information](#more-information) section for a tip on performing a search and purge operation on more than 50,000 mailboxes.</span></span> 
    
- <span data-ttu-id="69b37-p106">이 문서의 절차는 Exchange Online 사서함 및 공용 폴더의 항목을 삭제 하는 데에만 사용할 수 있습니다. SharePoint 또는 비즈니스용 OneDrive 사이트에서 콘텐츠를 삭제 하는 데 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-p106">The procedure in this article can only be used to delete items in Exchange Online mailboxes and public folders. You can't use it to delete content from SharePoint or OneDrive for Business sites.</span></span>
    
## <a name="step-1-create-a-content-search-to-find-the-message-to-delete"></a><span data-ttu-id="69b37-127">1단계: 삭제할 메시지를 찾는 콘텐츠 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="69b37-127">Step 1: Create a Content Search to find the message to delete</span></span>

<span data-ttu-id="69b37-p107">첫 번째 단계는 콘텐츠 검색을 만들고 실행 하 여 조직의 사서함에서 제거 하려는 메시지를 찾는 것입니다. 보안 &amp; 및 준수 센터를 사용 하거나 **ComplianceSearch** 및 **ComplianceSearch** cmdlet을 실행 하 여 검색을 만들 수 있습니다. 이 검색의 쿼리와 일치 하는 메시지는 [3 단계](#step-3-delete-the-message)에서 **new-compliancesearchaction 새로 만들기** 명령을 실행 하 여 삭제 됩니다. 콘텐츠 검색을 만들고 검색 쿼리를 구성 하는 방법에 대 한 자세한 내용은 다음 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="69b37-p107">The first step is to create and run a Content Search to find the message that you want to remove from mailboxes in your organization. You can create the search by using the Security &amp; Compliance Center or by running the **New-ComplianceSearch** and **Start-ComplianceSearch** cmdlets. The messages that match the query for this search will be deleted by running the **New-ComplianceSearchAction -Purge** command in [Step 3](#step-3-delete-the-message). For information about creating a Content Search and configuring search queries, see the following topics:</span></span> 
  
- [<span data-ttu-id="69b37-132">Office 365의 콘텐츠 검색</span><span class="sxs-lookup"><span data-stu-id="69b37-132">Content Search in Office 365</span></span>](content-search.md)
    
- [<span data-ttu-id="69b37-133">콘텐츠 검색에 대 한 키워드 쿼리</span><span class="sxs-lookup"><span data-stu-id="69b37-133">Keyword queries for Content Search</span></span>](keyword-queries-and-search-conditions.md)
    
- [<span data-ttu-id="69b37-134">New-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="69b37-134">New-ComplianceSearch</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearch)
    
- [<span data-ttu-id="69b37-135">Start-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="69b37-135">Start-ComplianceSearch</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/Start-ComplianceSearch)
    
> [!NOTE]
> <span data-ttu-id="69b37-p108">이 단계에서 만든 콘텐츠 검색에서 검색 되는 콘텐츠 위치에는 SharePoint 또는 비즈니스용 OneDrive 사이트를 포함할 수 없습니다. 전자 메일 메시지에 사용 되는 콘텐츠 검색에 사서함과 공용 폴더만 포함할 수 있습니다. 콘텐츠 검색에 사이트를 포함 하는 경우 **new-compliancesearchaction** cmdlet을 실행 하면 3 단계에서 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-p108">The content locations that are searched in the Content Search that you create in this step can't include SharePoint or OneDrive for Business sites. You can include only mailboxes and public folders in a Content Search that will be used to email messages. If the Content Search includes sites, you'll receive an error in Step 3 when you run the **New-ComplianceSearchAction** cmdlet.</span></span> 
  
### <a name="tips-for-finding-messages-to-remove"></a><span data-ttu-id="69b37-139">제거할 메시지를 찾기 위한 팁</span><span class="sxs-lookup"><span data-stu-id="69b37-139">Tips for finding messages to remove</span></span>

<span data-ttu-id="69b37-p109">검색 쿼리의 목적은 검색의 결과 범위를 제거할 메시지로만 좁히는 것입니다. 다음 팁을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="69b37-p109">The goal of the search query is to narrow the results of the search to only the message or messages that you want to remove. Here are some tips:</span></span>
  
- <span data-ttu-id="69b37-142">메시지의 제목 줄에 사용 된 정확한 텍스트나 구를 알고 있으면 검색 쿼리에 **subject** 속성을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-142">If you know the exact text or phrase used in the subject line of the message, use the **Subject** property in the search query.</span></span> 
    
- <span data-ttu-id="69b37-143">메시지의 정확한 날짜(또는 날짜 범위)를 알고 있으면 검색 쿼리에 **Received** 속성을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-143">If you know that exact date (or date range) of the message, include the **Received** property in the search query.</span></span> 
    
- <span data-ttu-id="69b37-144">메시지를 보낸 사람을 알고 있으면 검색 쿼리에 **From** 속성을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-144">If you know who sent the message, include the **From** property in the search query.</span></span> 
    
- <span data-ttu-id="69b37-145">검색 결과를 미리 확인 하 여 검색에서 삭제 하려는 메시지를 반환 하는 것이 올바른지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-145">Preview the search results to verify that the search returned only the message (or messages) that you want to delete.</span></span>
    
- <span data-ttu-id="69b37-146">보안 &amp; 및 준수 센터의 검색 세부 정보 창에 표시 되는 검색 예측 통계를 사용 하거나, [ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517934) cmdlet을 사용 하 여 총 결과 수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-146">Use the search estimate statistics (displayed in the details pane of the search in the Security &amp; Compliance Center or by using the [Get-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517934) cmdlet) to get a count of the total number of results.</span></span> 
    
<span data-ttu-id="69b37-147">다음은 의심스러운 전자 메일 메시지를 찾는 쿼리의 두 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-147">Here are two examples of queries to find suspicious email messages.</span></span>
  
- <span data-ttu-id="69b37-148">이 쿼리는 2016년 4월 13일과 2016년 4월 14일 사이에 사용자가 받은 메시지 중에서 제목 줄에 "action" 및 "required"가 포함된 메시지를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-148">This query returns messages that were received by users between April 13, 2016 and April 14, 2016 and that contain the words "action" and "required" in the subject line.</span></span>
    
    ```
    (Received:4/13/2016..4/14/2016) AND (Subject:'Action required')
    ```
   
- <span data-ttu-id="69b37-149">이 쿼리는 chatsuwloginsset12345@outlook.com에서 보낸 메시지 중에서 제목 줄에 "Update your account information"이 포함된 메시지를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-149">This query returns messages that were sent by chatsuwloginsset12345@outlook.com and that contain the exact phrase "Update your account information" in the subject line.</span></span>
    
    ```
    (From:chatsuwloginsset12345@outlook.com) AND (Subject:"Update your account information")
    ```

## <a name="step-2-connect-to-security--compliance-center-powershell"></a><span data-ttu-id="69b37-150">2 단계: 보안 & 준수 센터 PowerShell에 연결</span><span class="sxs-lookup"><span data-stu-id="69b37-150">Step 2: Connect to Security & Compliance Center PowerShell</span></span>

<span data-ttu-id="69b37-p110">다음 단계는 조직의 보안 & 준수 센터 PowerShell에 연결 하는 것입니다. 단계별 지침은 [Connect to Office 365 Security &amp; 준수 센터 PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69b37-p110">The next step is to connect to Security & Compliance Center PowerShell for your organization. For step-by-step instructions, see [Connect to Office 365 Security &amp; Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>
  
<span data-ttu-id="69b37-p111">Office 365 계정에서 MFA (multi-factor authentication) 또는 페더레이션 인증을 사용 하는 경우에는 Security & 준수 센터 PowerShell에 연결 하는 경우 이전 항목의 지침을 사용할 수 없습니다. 대신 [다단계 인증을 사용 하 여 Office 365 보안 & 준수 센터 PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell)항목의 지침을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="69b37-p111">If your Office 365 account uses multi-factor authentication (MFA) or federated authentication, you can't use the instructions in the previous topic on connecting to Security & Compliance Center PowerShell. Instead, see the instructions in the topic [Connect to Office 365 Security & Compliance Center PowerShell using multi-factor authentication](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell).</span></span>
  
## <a name="step-3-delete-the-message"></a><span data-ttu-id="69b37-155">3 단계: 메시지 삭제</span><span class="sxs-lookup"><span data-stu-id="69b37-155">Step 3: Delete the message</span></span>

<span data-ttu-id="69b37-p112">제거 하 고 보안 &amp; 준수 센터 PowerShell에 연결 된 메시지를 반환 하도록 콘텐츠 검색을 만들고 구체화 한 후에는 **new-compliancesearchaction** cmdlet을 실행 하 여 메시지를 삭제 하는 것이 마지막 단계입니다. 메시지를 일시 삭제 하거나 영구적으로 삭제할 수 있습니다. 일시 삭제 된 메시지는 사용자의 복구 가능한 항목 폴더로 이동 되며, 삭제 된 항목 보존 기간이 만료 될 때까지 보존 됩니다. 영구 삭제 된 메시지는 사서함에서 영구적으로 제거 되도록 표시 되며 다음에 관리 되는 폴더 도우미가 사서함을 처리할 때 영구적으로 제거 됩니다. 사서함에 대해 단일 항목 복구를 사용 하도록 설정 하면 삭제 된 항목 보존 기간이 만료 된 후에 영구 삭제 된 항목이 영구적으로 제거 됩니다. 사서함을 보류 중인 경우에는 항목의 보존 기간이 만료 되거나 사서함에서 보류가 제거 될 때까지 삭제 된 메시지가 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-p112">After you've created and refined a Content Search to return the message that you want to remove and are connected to Security &amp; Compliance Center PowerShell, the final step is to run the **New-ComplianceSearchAction** cmdlet to delete the message. You can soft- or hard-delete the message. A soft-deleted message is moved to a user's Recoverable Items folder and retained until the deleted item retention period expires. Hard-deleted messages are marked for permanent removal from the mailbox and will be permanently removed the next time the mailbox is processed by the Managed Folder Assistant. If single item recovery is enabled for the mailbox, hard-deleted items will be permanently removed after the deleted item retention period expires. If a mailbox is placed on hold, deleted messages are preserved until the hold duration for the item expires or until the hold is removed from the mailbox.</span></span>
  
<span data-ttu-id="69b37-162">다음 예제에서는 "피싱 메시지 제거" 라는 콘텐츠 검색에서 반환 되는 검색 결과를 명령에서 일시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-162">In the following example, the command will soft-delete the search results returned by a Content Search named "Remove Phishing Message".</span></span> 

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType SoftDelete
```

<span data-ttu-id="69b37-163">"피싱 메시지 제거" 콘텐츠 검색에서 반환 된 항목을 하드 삭제 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-163">To hard-deleted the items returned by the  "Remove Phishing Message" content search, you would run this command:</span></span>

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType HardDelete
```

<span data-ttu-id="69b37-164">이전 명령을 실행 하 여 메시지를 일시 또는 영구적으로 삭제 하는 경우 *searchname* 매개 변수로 지정 된 검색은 1 단계에서 만든 콘텐츠 검색입니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-164">Note that when you run the previous command to soft- or hard-delete messages, the search specified by the  *SearchName*  parameter is the Content Search that you created in Step 1.</span></span> 
  
<span data-ttu-id="69b37-165">자세한 내용은 [new-compliancesearchaction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearchAction)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="69b37-165">For more information, see [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearchAction).</span></span>

## <a name="more-information"></a><span data-ttu-id="69b37-166">추가 정보</span><span class="sxs-lookup"><span data-stu-id="69b37-166">More information</span></span>

- <span data-ttu-id="69b37-167">**검색 및 제거 작업의 상태를 확인 하려면 어떻게 해야 합니까?**</span><span class="sxs-lookup"><span data-stu-id="69b37-167">**How do you get status on the search and remove operation?**</span></span>

    <span data-ttu-id="69b37-p113">**new-compliancesearchaction** 를 실행 하 여 삭제 작업의 상태를 가져옵니다. **new-compliancesearchaction** cmdlet을 실행할 때 만들어지는 개체는 다음 `<name of Content Search>_Purge`형식을 사용 하 여 이름이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-p113">Run the **Get-ComplianceSearchAction** to get the status on the delete operation. Note that the object that is created when you run the **New-ComplianceSearchAction** cmdlet is named using this format:  `<name of Content Search>_Purge`.</span></span> 
    
- <span data-ttu-id="69b37-170">**메시지를 삭제 한 후에 수행 되는 작업**</span><span class="sxs-lookup"><span data-stu-id="69b37-170">**What happens after you delete a message?**</span></span>

   <span data-ttu-id="69b37-p114">`New-ComplianceSearchAction -Purge -PurgeType HardDelete` 명령을 사용 하 여 삭제 된 메시지는 제거 폴더로 이동 되며 사용자가 액세스할 수 없습니다. 메시지가 제거 폴더로 이동 되 면 사서함에 대해 단일 항목 복구를 사용할 수 있는 경우 삭제 된 항목 보존 기간 동안 메시지가 보존 됩니다. (Office 365에서 새 사서함을 만들 때 기본적으로 단일 항목 복구를 사용 하도록 설정 됩니다.) 삭제 된 항목 보존 기간이 만료 되 면 메시지가 영구적으로 삭제 되도록 표시 되 고 다음 번에 관리 되는 폴더 도우미가 사서함을 처리할 때 Office 365에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-p114">A message that's deleted with the  `New-ComplianceSearchAction -Purge -PurgeType HardDelete` command is moved to the Purges folder and can't be accessed by the user. After the message is moved to the Purges folder, the message is retained for the duration of the deleted item retention period if single item recovery is enabled for the mailbox. (In Office 365, single item recovery is enabled by default when a new mailbox is created.) After the deleted item retention period expires, the message is marked for permanent deletion and will be purged from Office 365 the next time the mailbox is processed by the Managed Folder assistant.</span></span> 

   <span data-ttu-id="69b37-p115">`New-ComplianceSearchAction -Purge -PurgeType SoftDelete` 명령을 사용 하는 경우 사용자의 복구 가능한 항목 폴더에 있는 삭제 폴더로 메시지가 이동 됩니다. Office 365에서 즉시 제거 되지는 않습니다. 사용자는 사서함에 대해 구성 된 삭제 된 항목 보존 기간을 기준으로 기간에 대해 지운 편지함 폴더의 메시지를 복구할 수 있습니다. 이 보존 기간이 만료 되거나 사용자가 만료 되기 전에 메시지를 제거 하면 메시지가 제거 폴더로 이동 되며 사용자가 더 이상 액세스할 수 없습니다. 제거 폴더에는 사서함에 대해 단일 항목 복구를 사용할 수 있는 경우 사서함에 대해 구성 된 삭제 된 항목 보존 기간을 기준으로 메시지가 보존 됩니다. (Office 365에서 새 사서함을 만들 때 기본적으로 단일 항목 복구를 사용 하도록 설정 됩니다.) 삭제 된 항목 보존 기간이 만료 되 면 메시지가 영구적으로 삭제 되도록 표시 되 고 다음 번에 관리 되는 폴더 도우미가 사서함을 처리할 때 Office 365에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-p115">If you use the `New-ComplianceSearchAction -Purge -PurgeType SoftDelete` command, messages are moved to the Deletions folder in the user's Recoverable Items folder. It isn't immediately purged from Office 365. The user can recover messages in the Deleted Items folder for the duration based on the deleted item retention period configured for the mailbox. After this retention period expires (or if user purges the message before it expires), the message is moved to the Purges folder and can no longer be accessed by the user. Once in the Purges folder, the message is retained for the duration based on the deleted item retention period configured for the mailbox if single items recovery is enabled for the mailbox. (In Office 365, single item recovery is enabled by default when a new mailbox is created.) After the deleted item retention period expires, the message is marked for permanent deletion and will be purged from Office 365 the next time that the mailbox is processed by the Managed Folder assistant.</span></span> 
    
- <span data-ttu-id="69b37-180">**5만 개 이상의 사서함에서 메시지를 삭제 해야 하는 경우는 어떻게 하나요?**</span><span class="sxs-lookup"><span data-stu-id="69b37-180">**What if you have to delete a message from more than 50,000 mailboxes?**</span></span>

    <span data-ttu-id="69b37-p116">앞에서 설명한 것 처럼, 최대 5만 개의 사서함에서 검색 및 제거 작업을 수행할 수 있습니다. 5만 개 이상의 사서함에서 검색 및 제거 작업을 수행 해야 하는 경우 5만 사서함 보다 적게 검색 되는 사서함 수를 줄일 수 있는 임시 검색 권한 필터를 만드는 것이 좋습니다. 예를 들어 조직에 여러 부서, 주 또는 국가의 사서함이 포함 되어 있는 경우 이러한 사서함 속성 중 하나를 기반으로 사서함 검색 권한 필터를 만들어 조직의 사서함 하위 집합을 검색할 수 있습니다. 검색 권한 필터를 만든 후 1 단계에서 설명 하는 검색을 만든 다음 3 단계에서 설명 하는 메시지를 삭제 합니다. 그런 다음 필터를 편집 하 여 다른 사서함 집합에서 메시지를 검색 하 고 제거할 수 있습니다. 검색 권한 필터를 만드는 방법에 대 한 자세한 내용은 [콘텐츠 검색에 대 한 사용 권한 필터링 구성을](permissions-filtering-for-content-search.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="69b37-p116">As previously stated, you can perform a search and purge operation on a maximum of 50,000 mailboxes. If you have to do a search and purge operation on more than 50,000 mailboxes, consider creating temporary search permissions filters that would reduce the number of mailboxes that would be searched to less than 50,000 mailboxes. For example, if your organization contains mailboxes in different departments, states, or countries, you can create a mailbox search permissions filter based on one of those mailbox properties to search a subset of mailboxes in your organization. After you create the search permissions filter, you would create the search (described in Step 1) and then delete the message (described in Step 3). Then you can edit the filter to search for and purge messages in a different set of mailboxes. For more information about creating search permissions filters, see [Configure permissions filtering for Content Search](permissions-filtering-for-content-search.md).</span></span>
    
- <span data-ttu-id="69b37-187">**인덱싱되지 않은 항목이 검색 결과에 포함 되도록 삭제 됩니까?**</span><span class="sxs-lookup"><span data-stu-id="69b37-187">**Will unindexed items included in the search results be deleted?**</span></span>

    <span data-ttu-id="69b37-188">아니요, ' new-compliancesearchaction-Purge 명령에서는 인덱싱되지 않은 항목을 삭제 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-188">No, the  \`New-ComplianceSearchAction -Purge command doesn't delete unindexed items.</span></span> 
    
- <span data-ttu-id="69b37-189">**원본 위치 유지 또는 소송 보존 상태에 있는 사서함에서 메시지를 삭제 했거나 Office 365 보관 정책에 할당 된 경우는 어떻게 되나요?**</span><span class="sxs-lookup"><span data-stu-id="69b37-189">**What happens if a message is deleted from a mailbox that has been placed on In-Place Hold or Litigation Hold or is assigned to an Office 365 retention policy?**</span></span>

    <span data-ttu-id="69b37-p117">메시지가 제거 된 후 제거 폴더로 이동 되 면 해당 메시지는 보존 기간이 만료 될 때까지 유지 됩니다. 보존 기간을 무제한으로 설정한 경우에는 보류가 제거 되거나 보존 기간이 변경 될 때까지 항목이 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-p117">After the message is purged and moved to the Purges folder, the message is retained until the hold duration expires. If the hold duration is unlimited, then items are retained until the hold is removed or the hold duration is changed.</span></span>
    
- <span data-ttu-id="69b37-192">**서로 다른 보안 & 준수 센터 역할 그룹 간에 검색 및 제거 워크플로가 구분 되는 이유는 무엇 인가요?**</span><span class="sxs-lookup"><span data-stu-id="69b37-192">**Why is the search and remove workflow divided among different Security & Compliance Center role groups?**</span></span>

    <span data-ttu-id="69b37-p118">앞에서 설명한 것 처럼, 사용자가 eDiscovery 관리자 역할 그룹의 구성원 이거나 검색 사서함에 준수 검색 관리 역할을 할당 받아야 합니다. 메시지를 삭제 하려면 사용자가 조직 관리 역할 그룹의 구성원 이거나 검색 및 삭제 관리 역할을 할당 받아야 합니다. 이를 통해 조직의 사서함을 검색 하 고 메시지를 삭제할 수 있는 사람을 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69b37-p118">As previously explained, a person has to be a member of the eDiscovery Manager role group or be assigned the Compliance Search management role to search mailboxes. To delete messages, a person has to be a member of the Organization Management role group or be assigned the Search And Purge management role. This makes it possible to control who can search mailboxes in the organization and who can delete messages.</span></span> 
