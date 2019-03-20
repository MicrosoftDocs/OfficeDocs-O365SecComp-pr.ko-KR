---
title: 메시지 검색 및 삭제 - 관리자 도움말
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/20/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8c36bb03-e716-4fdd-9958-4aa7a2a1db42
description: 관리자는 검색 사서함 cmdlet을 사용 하 여 사용자 사서함을 검색 한 다음 사서함에서 메시지를 삭제할 수 있습니다.
ms.openlocfilehash: abf7e7f39fe719ecc6c23565e284c01aed8822ee
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693487"
---
# <a name="search-for-and-delete-messages---admin-help"></a><span data-ttu-id="4656a-103">메시지 검색 및 삭제 - 관리자 도움말</span><span class="sxs-lookup"><span data-stu-id="4656a-103">Search for and delete messages - Admin help</span></span>
  
<span data-ttu-id="4656a-104">관리자는 **검색 사서함** cmdlet을 사용 하 여 사용자 사서함을 검색 한 다음 사서함에서 메시지를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-104">Administrators can use the **Search-Mailbox** cmdlet to search user mailboxes and then delete messages from a mailbox.</span></span> 
  
<span data-ttu-id="4656a-p101">한 번에 메시지를 검색하여 삭제하려면  **DeleteContent** 스위치와 함께 _Search-Mailbox_ cmdlet을 실행합니다. 하지만, 이 경우 검색 결과를 미리 보거나 검색에 의해 반환되는 메시지 로그를 생성할 수 없으며, 삭제하면 안 되는 메시지를 실수로 삭제할 수 있습니다. 메시지를 삭제하기 전에 검색되는 메시지에 대한 로그를 미리 보려면  **LogOnly** 스위치와 함께 _Search-Mailbox_ cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-p101">To search and delete messages in one step, run the **Search-Mailbox** cmdlet with the  _DeleteContent_ switch. However, when you do this, you can't preview search results or generate a log of messages that will be returned by the search, and you may inadvertently delete messages that you didn't intend to. To preview a log of the messages found in the search before they're deleted, run the **Search-Mailbox** cmdlet with the  _LogOnly_ switch.</span></span> 
  
<span data-ttu-id="4656a-p102">추가적인 안전 장치로서,  _TargetMailbox_ 및  _TargetFolder_ 매개 변수를 사용하여 먼저 메시지를 다른 사서함에 복사할 수 있습니다. 이렇게 하면 삭제되는 메시지의 복사본을 보관하여 필요할 때 다시 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-p102">As an additional safeguard, you can first copy the messages to another mailbox by using the  _TargetMailbox_ and  _TargetFolder_ parameters. By doing this, you retain a copy of the deleted messages in case you need to access them again.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="4656a-110">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="4656a-110">Before you begin</span></span>

- <span data-ttu-id="4656a-111">예상 완료 시간: 10분.</span><span class="sxs-lookup"><span data-stu-id="4656a-111">Estimated time to complete: 10 minutes.</span></span> <span data-ttu-id="4656a-112">실제 시간은 사서함 및 검색 쿼리의 크기에 따라 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-112">The actual time may vary depending on the size of the mailbox and the search query.</span></span>
    
- <span data-ttu-id="4656a-113">이 절차를 수행하는 데 EAC(Exchange 관리 센터)를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-113">You can't use the Exchange admin center (EAC) to perform these procedures.</span></span> <span data-ttu-id="4656a-114">셸을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-114">You must use the Shell.</span></span>
    
- <span data-ttu-id="4656a-115">사용자 사서함에서 메시지를 검색 및 삭제 하려면 다음 관리 역할을 둘 다 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-115">You need to be assigned both of the following management roles to search for and delete messages in users' mailboxes:</span></span>
    
  - <span data-ttu-id="4656a-116">**사서함 검색**-이 역할을 사용 하면 조직의 여러 사서함에서 메시지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-116">**Mailbox Search**- This role allows you to search for messages across multiple mailboxes in your organization.</span></span> <span data-ttu-id="4656a-117">관리자에게는 기본적으로 이 역할이 할당되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-117">Administrators aren't assigned this role by default.</span></span> <span data-ttu-id="4656a-118">사서함을 검색할 수 있도록 이 역할을 자신에게 할당하려면 자신을 검색 관리 역할 그룹의 구성원으로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-118">To assign yourself this role so that you can search mailboxes, add yourself as a member of the Discovery Management role group.</span></span> <span data-ttu-id="4656a-119">[Add a User to the Discovery Management Role Group](http://technet.microsoft.com/library/729e09d8-614b-431f-ae04-ae41fb4c628e.aspx)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4656a-119">See [Add a User to the Discovery Management Role Group](http://technet.microsoft.com/library/729e09d8-614b-431f-ae04-ae41fb4c628e.aspx).</span></span>
    
  - <span data-ttu-id="4656a-120">**사서함 가져오기 내보내기** -이 역할을 사용 하면 사용자 사서함에서 메시지를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-120">**Mailbox Import Export** - This role allows you to delete messages from a user's mailbox.</span></span> <span data-ttu-id="4656a-121">기본적으로 이 역할은 역할 그룹에 할당되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-121">By default, this role isn't assigned to any role group.</span></span> <span data-ttu-id="4656a-122">사용자 사서함에서 메시지를 삭제하려면 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-122">To delete messages from users' mailboxes, you can add the Mailbox Import Export role to the Organization Management role group.</span></span> <span data-ttu-id="4656a-123">자세한 내용은 [역할 그룹 관리](http://technet.microsoft.com/library/ab9b7a3b-bf67-4ba1-bde5-8e6ac174b82c.aspx) 의 "역할 그룹에 역할 추가" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4656a-123">For more information, see the "Add a role to a role group" section in [Manage Role Groups](http://technet.microsoft.com/library/ab9b7a3b-bf67-4ba1-bde5-8e6ac174b82c.aspx) .</span></span> 
    
- <span data-ttu-id="4656a-124">메시지를 삭제하려는 사서함에서 단일 항목 복구를 사용하는 경우 먼저 이 기능을 사용하지 않도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-124">If the mailbox from which you want to delete messages has single item recovery enabled, you must first disable the feature.</span></span> <span data-ttu-id="4656a-125">자세한 내용은 [사서함에 대한 단일 항목을 사용하거나 사용하지 않도록 설정](http://technet.microsoft.com/library/2e7f1bcd-8395-45ad-86ce-22868bd46af0.aspx)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4656a-125">For more information, see [Enable or disable single item recovery for a mailbox](http://technet.microsoft.com/library/2e7f1bcd-8395-45ad-86ce-22868bd46af0.aspx).</span></span>
    
- <span data-ttu-id="4656a-126">메시지를 삭제 하려는 사서함이 보존 상태에 있는 경우 보존을 제거 하 고 사서함 콘텐츠를 삭제 하기 전에 레코드 관리 또는 법률 부서를 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-126">If the mailbox from which you want to delete messages is placed on hold, we recommend that you check with your records management or legal department before removing the hold and deleting the mailbox content.</span></span> <span data-ttu-id="4656a-127">승인을 받은 후에 [는 복구 가능한 항목 폴더 정리](http://technet.microsoft.com/library/82c310f8-de2f-46f2-8e1a-edb6055d6e69.aspx)항목에 나와 있는 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-127">After you obtain approval, follow the steps listed in the topic [Clean Up the Recoverable Items Folder](http://technet.microsoft.com/library/82c310f8-de2f-46f2-8e1a-edb6055d6e69.aspx).</span></span>
    
- <span data-ttu-id="4656a-128">**검색 사서함** cmdlet을 사용 하 여 최대 1만 개의 사서함을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-128">You can search a maximum of 10,000 mailboxes using the **Search-Mailbox** cmdlet.</span></span> <span data-ttu-id="4656a-129">Exchange Online 조직이 고 사서함이 1만 개 보다 많은 경우 준수 검색 기능 (또는 해당 **ComplianceSearch** cmdlet)을 사용 하 여 사서함 수를 무제한으로 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-129">If you're an Exchange Online organization and have more than 10,000 mailboxes, you can use the Compliance Search feature (or the corresponding **New-ComplianceSearch** cmdlet) to search an unlimited number of mailboxes.</span></span> <span data-ttu-id="4656a-130">그런 다음 **new-compliancesearchaction** cmdlet을 사용 하 여 준수 검색에서 반환 된 메시지를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-130">Then you can use the **New-ComplianceSearchAction** cmdlet to delete the messages returned by a compliance search.</span></span> <span data-ttu-id="4656a-131">자세한 내용은 [Office 365 조 직에서 전자 메일 메시지 검색 및 삭제](https://go.microsoft.com/fwlink/p/?LinkId=786856)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4656a-131">For more information, see [Search for and delete email messages from your Office 365 organization](https://go.microsoft.com/fwlink/p/?LinkId=786856).</span></span>
    
- <span data-ttu-id="4656a-132">*searchquery* 매개 변수를 사용 하 여 검색 쿼리를 포함 하는 경우 검색 **사서함** cmdlet은 최대 1만 개의 항목을 검색 결과에 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-132">If you include a search query (by using the  *SearchQuery*  parameter), the **Search-Mailbox** cmdlet will return a maximum of 10,000 items in the search results.</span></span> <span data-ttu-id="4656a-133">따라서 검색 쿼리를 포함 하는 경우 1만 개 보다 많은 항목을 삭제 하려면 **검색 사서함** 명령을 여러 번 실행 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-133">Therefore if you include a search query, you might have to run the **Search-Mailbox** command multiple times to delete more than 10,000 items.</span></span> 
    
- <span data-ttu-id="4656a-134">또한 **검색 사서함** cmdlet을 실행 하면 사용자의 보관 사서함도 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-134">The user's archive mailbox will also be searched when you run the **Search-Mailbox** cmdlet.</span></span> <span data-ttu-id="4656a-135">마찬가지로, _DeleteContent_ 스위치와 함께 **검색 사서함** cmdlet을 사용 하면 기본 보관 사서함의 항목이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-135">Similarly, items in the primary archive mailbox will be deleted when you use the **Search-Mailbox** cmdlet with the  _DeleteContent_ switch.</span></span> <span data-ttu-id="4656a-136">이를 방지 하기 위해 *만드는 경우 donotincludearchive* 스위치를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-136">To prevent this, you can include the  *DoNotIncludeArchive*  switch.</span></span> <span data-ttu-id="4656a-137">또한 예기치 않은 데이터 손실이 발생할 수 있으므로 _DeleteContent_ 스위치를 사용 하 여 자동 확장 기능을 사용 하는 Exchange Online 사서함의 메시지를 삭제 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-137">Also, we recommend that you don't use the  _DeleteContent_ switch to delete messages in Exchange Online mailboxes that have auto-expanding archiving enabled because unexpected data loss may occur.</span></span> 
    
## <a name="search-messages-and-log-the-search-results"></a><span data-ttu-id="4656a-138">메시지 검색 및 검색 결과 기록</span><span class="sxs-lookup"><span data-stu-id="4656a-138">Search messages and log the search results</span></span>

<span data-ttu-id="4656a-p112">이 예에서는 April Stewart의 사서함에서 제목에 "Your bank statement" 구가 포함된 메시지를 검색하고 관리자 사서함의 SearchAndDeleteLog 폴더에 검색 결과를 기록합니다. 메시지는 대상 사서함에 복사되거나 대상 사서함에서 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-p112">This example searches April Stewart's mailbox for messages that contain the phrase "Your bank statement" in the Subject field and logs the search results in the SearchAndDeleteLog folder of the administrator's mailbox. Messages aren't copied to or deleted from the target mailbox.</span></span>
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

<span data-ttu-id="4656a-141">이 예에서는 조직의 모든 사서함에서 파일 이름에 "트로이" 라는 단어가 포함 된 모든 유형의 첨부 파일이 있는 메시지를 검색 하 고 관리자의 사서함에 로그 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-141">This example searches all mailboxes in the organization for messages that have any type of attached file that contains the word "Trojan" in the filename and sends a log message to the administrator's mailbox.</span></span>
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery attachment:trojan* -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

<span data-ttu-id="4656a-142">구문과 매개 변수에 대한 자세한 내용은 [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="4656a-142">For detailed syntax and parameter information, see [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).</span></span>
  
 
## <a name="search-and-delete-messages"></a><span data-ttu-id="4656a-143">메시지 검색 및 삭제</span><span class="sxs-lookup"><span data-stu-id="4656a-143">Search and delete messages</span></span>

<span data-ttu-id="4656a-p113">이 예에서는 April Stewart의 사서함에서 제목 필드에 "Your bank statement" 구가 포함된 메시지를 검색하고 검색 결과를 다른 폴더에 복사하지 않고 원본 사서함에서 메시지를 삭제합니다. 앞에서 설명한 것처럼 사용자 사서함에서 메시지를 삭제하려면 사서함 가져오기 내보내기 관리 역할이 할당되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-p113">This example searches April Stewart's mailbox for messages that contain the phrase "Your bank statement" in the Subject field and deletes the messages from the source mailbox without copying the search results to another folder. As previously explained, you need to be assigned the Mailbox Import Export management role to delete messages from a user's mailbox.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="4656a-p114">**DeleteContent** 스위치와 함께 _Search-Mailbox_ cmdlet을 사용할 경우 메시지는 원본 사서함에서 영구 삭제됩니다. 영구히 메시지를 삭제하기 전에  _LogOnly_ 스위치를 사용하여 검색으로 찾은 메시지에 대해 로그를 생성한 후 삭제하거나 해당 메시지를 다른 사서함에 복사한 후 원본 사서함에서 삭제하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-p114">When you use the **Search-Mailbox** cmdlet with the  _DeleteContent_ switch, messages are permanently deleted from the source mailbox. Before you permanently delete messages, we recommend that you either use the  _LogOnly_ switch to generate a log of the messages found in the search before they're deleted or copy the messages to another mailbox before deleting them from the source mailbox.</span></span> 
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -DeleteContent
```

<span data-ttu-id="4656a-148">이 예에서는 April Stewart의 사서함에서 제목 필드에 "Your bank statement" 구가 포함된 메시지를 검색하고 BackupMailbox 사서함의 AprilStewart-DeletedMessages 폴더에 검색 결과를 복사한 후 April 사서함에서 메시지를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-148">This example searches April Stewart's mailbox for messages that contain the phrase "Your bank statement" in the Subject field, copies the search results to the folder AprilStewart-DeletedMessages in the mailbox BackupMailbox, and deletes the messages from April's mailbox.</span></span>
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox "BackupMailbox" -TargetFolder "AprilStewart-DeletedMessages" -LogLevel Full -DeleteContent
```

<span data-ttu-id="4656a-149">이 예에서는 조직의 모든 사서함에서 제목이 "이 파일을 다운로드 합니다." 라는 메시지를 검색 한 다음이를 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-149">This example searches all mailboxes in the organization for messages with the subject line "Download this file", and then permanently deletes them.</span></span> 
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery 'Subject:"Download this file"' -DeleteContent
```

<span data-ttu-id="4656a-150">구문과 매개 변수에 대한 자세한 내용은 [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="4656a-150">For detailed syntax and parameter information, see [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).</span></span>

## <a name="using-the--loglevel-full-parameter"></a><span data-ttu-id="4656a-151">-LogLevel Full 매개 변수 사용</span><span class="sxs-lookup"><span data-stu-id="4656a-151">Using the -LogLevel Full parameter</span></span>

<span data-ttu-id="4656a-152">위 예제 중 일부는이 `Full` 값을 포함 하는 _LogLevel_ 매개 변수를 사용 하 여 **검색 사서함** cmdlet에서 반환 되는 결과에 대 한 자세한 정보를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-152">In some of the previous examples, the  _LogLevel_ parameter, with the  `Full` value is used to log detailed information about the results returned by the **Search-Mailbox** cmdlet.</span></span> <span data-ttu-id="4656a-153">이 매개 변수를 포함 하면 전자 메일 메시지가 만들어지고 _targetmailbox_ 매개 변수로 지정 된 사서함으로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-153">When you included this parameter, an email message is created and sent to the mailbox specified by the  _TargetMailbox_ parameter.</span></span> <span data-ttu-id="4656a-154">이 전자 메일 메시지에는 로그 파일 (검색 결과인 .csv 이라는 csv 파일)이 첨부 되며 _targetfolder_ 매개 변수에 지정 된 폴더에 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-154">The log file (which is a CSV-formatted file named Search Results.csv) is attached to this email message, and will be located in the folder specified by the  _TargetFolder_ parameter.</span></span> <span data-ttu-id="4656a-155">로그 파일에는 **검색 사서함** cmdlet을 실행할 때 검색 결과에 포함 된 각 메시지에 대 한 행이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4656a-155">The log file contains a row for each message that's included in the search results when you run the **Search-Mailbox** cmdlet.</span></span> 
