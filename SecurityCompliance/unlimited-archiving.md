---
title: Office 365 무제한 보관의 개요 (영문)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 37cdbb02-a24a-4093-8bdb-2a7f0b3a19ee
description: 자동 확장 하는 방법에 대 한 설명 무제한 보관 저장소 Exchange Online 사서함에 대 한 제공 Office 365의 보관,입니다.
ms.openlocfilehash: 83eb49b3f2a7da418b61e509f44023809ed396c3
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29740820"
---
# <a name="overview-of-unlimited-archiving-in-office-365"></a><span data-ttu-id="ad6ca-103">Office 365 무제한 보관의 개요 (영문)</span><span class="sxs-lookup"><span data-stu-id="ad6ca-103">Overview of unlimited archiving in Office 365</span></span>

<span data-ttu-id="ad6ca-p101">Office 365의 보관 사서함 추가 사서함 저장 공간을 사용 하는 사용자를 제공합니다. 사용자의 보관 사서함을 사용 하도록 설정한 후 최대 100GB 추가 저장소를 사용할 수 있습니다. 100GB 저장소 할당량에 도달 하면 조직에서는 보관 사서함에 대 한 요청 추가 저장 공간을 Microsoft에 문의 해야 했습니다. 않는 경우 나타나지 않습니다. ( *보관 자동 확장*라고 함)는 Office 365의 새로운 무제한으로 보관 기능은의 보관 사서함에 저장 무제한 금액을 제공 합니다. 이제, 보관 사서함에 저장 용량 할당량에 도달 하면 Office 365 자동으로의 크기를 늘리는 사용자 사서함 저장 공간 부족 실행 되지 않음 하 고 관리자가 보관 사서함에 대 한 추가 저장소 요청 하지 않아도 즉 보관 .</span><span class="sxs-lookup"><span data-stu-id="ad6ca-p101">In Office 365, archive mailboxes provide users with additional mailbox storage space. After a user's archive mailbox is enabled, up to 100 GB of additional storage is available. When the 100 GB storage quota is reached, organizations had to contact Microsoft to request additional storage space for an archive mailbox. That's no longer the case. The new unlimited archiving feature in Office 365 (called *auto-expanding archiving*) provides an unlimited amount of storage in archive mailboxes. Now, when the storage quota in the archive mailbox is reached, Office 365 automatically increases the size of the archive, which means that users won't run out of mailbox storage space and administrators won't have to request additional storage for archive mailboxes.</span></span>
  
<span data-ttu-id="ad6ca-110">자동 확장 설정에 대 한 단계별 지침은 [Office 365 무제한 보관을 사용 하도록 설정](enable-unlimited-archiving.md)참조 보관 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-110">For step-by-step instructions for turning on auto-expanding archiving, see [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ad6ca-p102">또한 보관 자동 확장 공유 사서함을 지원 합니다. 공유 사서함에 대 한 보관을 사용 하려면 Exchange Online 계획 2 라이선스 또는 Exchange Online 보관 라이선스를 사용 하 여 Exchange Online 계획 1 라이선스가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-p102">Auto-expanding archiving also supports shared mailboxes. To enable the archive for a shared mailbox, an Exchange Online Plan 2 license or an Exchange Online Plan 1 license with an Exchange Online Archiving license is required.</span></span> 
  
## <a name="how-auto-expanding-archiving-works"></a><span data-ttu-id="ad6ca-113">보관 작동 방식 자동 확장</span><span class="sxs-lookup"><span data-stu-id="ad6ca-113">How auto-expanding archiving works</span></span>

<span data-ttu-id="ad6ca-p103">앞에서 설명한 것, 추가 사서함으로 사용자의 보관 사서함을 사용 하는 경우 저장 공간이 만들어집니다. 보관 자동 확장을 사용 하도록 설정한 경우 Office 365의 보관 사서함의 크기를 주기적으로 확인 합니다. 보관 사서함의 저장소 제한에 근접 한 가져오면 Office 365 보관 사서함에 대 한 추가 저장 공간을 자동으로 만듭니다. 사용자가이 추가 저장 공간 부족 실행 하는 경우 Office 365 사용자의 보관에 더 많은 저장 공간을 추가 합니다. 이 프로세스를 추가로 보관 저장소를 요청 하거나 보관 자동 확장 관리 관리자가 없는 것을 의미 하는 자동으로 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-p103">As previously explained, additional mailbox storage space is created when a user's archive mailbox is enabled. When auto-expanding archiving is enabled, Office 365 periodically checks the size of the archive mailbox. When an archive mailbox gets close to its storage limit, Office 365 automatically creates additional storage space for the archive. If the user runs out of this additional storage space, Office 365 adds more storage space to the user's archive. This process happens automatically, which means administrators don't have to request additional archive storage or manage auto-expanding archiving.</span></span> 
  
<span data-ttu-id="ad6ca-119">프로세스에 대 한 빠른 개요는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-119">Here's a quick overview of the process.</span></span>
  
![자동 확장 하는 보관 프로세스의 개요 (영문)](media/74355385-d990-44fe-8a87-6c3639d1f63f.png)
  
1. <span data-ttu-id="ad6ca-p104">사용자 사서함 또는 공유 사서함에 대 한 보관이 사용 됩니다. 저장 공간에 100GB 함께 보관 사서함 만들고 보관 사서함에 대 한 경고 할당량 90 g B로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-p104">Archiving is enabled for a user mailbox or a shared mailbox. An archive mailbox with 100 GB of storage space is created, and the warning quota for the archive mailbox is set to 90 GB.</span></span>
    
2. <span data-ttu-id="ad6ca-p105">관리자는 사서함에 대 한 보관 자동을 확장할 수 있습니다. 그런 다음, (복구 가능한 항목 폴더 포함)의 보관 사서함 90 g B에 도달 하면 자동 확장 보관 파일로 변환 됩니다 하 고 보관 사서함으로 저장 공간을 추가 하는 Office 365 합니다. 프로 비전 할 추가 저장 공간에 대 한 최대 30 일이 걸릴 수 있습니다를 메모 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-p105">An administrator enables auto-expanding archiving for the mailbox. Then, when the archive mailbox (including the Recoverable Items folder) reaches 90 GB, it's converted to an auto-expanding archive, and Office 365 adds storage space to the archive. Note that it can take up to 30 days for the additional storage space to be provisioned.</span></span>
    
3. <span data-ttu-id="ad6ca-126">Office 365 필요할 때 보관 사서함으로 더 많은 저장 공간을 추가 하는 자동으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-126">Office 365 automatically adds more storage space to the archive when necessary.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ad6ca-p106">사서함은 대기 상태에 놓일 또는 Office 365 보존 정책에 할당 된 경우 보관 자동 확장을 사용 하는 경우 보관 사서함에 대 한 저장소 할당량 110 g B로 증가 되었습니다. 마찬가지로, 보관 경고 할당량은 100GB로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-p106">If a mailbox is placed on hold or assigned to an Office 365 retention policy, the storage quota for the archive maibox is increased to 110 GB when auto-expanding archiving is enabled. Similarly, the archive warning quota is increased to 100 GB.</span></span>

## <a name="what-gets-moved-to-the-additional-archive-storage-space"></a><span data-ttu-id="ad6ca-129">추가 보관 저장소 공간으로 이동 가져옵니다 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="ad6ca-129">What gets moved to the additional archive storage space?</span></span>

<span data-ttu-id="ad6ca-p107">자동 확장 보관 저장소를 효율적으로 이용할 폴더 이동 가져올 수 있습니다. Office 365 추가 저장소 보관 사서함에 추가 되 면 폴더 이동를 결정 합니다. 폴더를 이동할 때 Outlook에서 폴더 목록 보관 부분에 원래 폴더 아래의 하위 폴더를 자동으로 만들어집니다. 이 새 하위 폴더에 이동 된 항목을 가리킵니다. Office 365를 사용 하 여이 폴더의 이름을 지정 하는 명명 규칙은 \*\* \<폴더 이름\>_yyyy (에서 만든 음 dd, yyyy h_mm)\*\*, 여기서:</span><span class="sxs-lookup"><span data-stu-id="ad6ca-p107">To make efficient use of auto-expanding archive storage, folders might get moved. Office 365 determines which folders get moved when additional storage is added to the archive. When a folder is moved, a subfolder is automatically created under the original folder in the archive portion of the folder list in Outlook. This new subfolder points to the items that were moved. The naming convention that Office 365 uses to name this folder is **\<folder name\>_yyyy (Created on mmm dd, yyyy h_mm)**, where:</span></span> 
  
- <span data-ttu-id="ad6ca-135">**yyyy** 는 연도 폴더에 메시지를 받았습니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-135">**yyyy** is the year the messages in the folder were received.</span></span> 
    
- <span data-ttu-id="ad6ca-136">**음 dd, yyyy h_m** 는 날짜 및 시간에서 UTC 형식으로 사용자의 표준 시간대 및 Outlook에서 국가별 설정에 따라 하위 폴더를 Office 365에서 만든입니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-136">**mmm dd, yyyy h_m** is the date and time that the subfolder was created by Office 365, in UTC format, based on the user's time zone and regional settings in Outlook.</span></span> 
    
<span data-ttu-id="ad6ca-137">다음 스크린샷에서 전에 하 고 자동 확장 보관 위치에 있는 메시지를 이동한 후 폴더 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-137">The following screen shots show a folder list before and after messages are moved in an auto-expanded archive.</span></span>
  
 <span data-ttu-id="ad6ca-138">**추가 저장소를 추가 하기 전에**</span><span class="sxs-lookup"><span data-stu-id="ad6ca-138">**Before additional storage is added**</span></span>
  
![자동 확장 보관 구축 하기 전에 보관 사서함의 폴더 목록](media/5d6d6420-e562-4912-aaab-1c111762b3f6.png)
  
 <span data-ttu-id="ad6ca-140">**추가 저장소를 추가한 후**</span><span class="sxs-lookup"><span data-stu-id="ad6ca-140">**After additional storage is added**</span></span>
  
![자동 확장 보관 프로 비전 한 후에 보관 사서함의 폴더 목록](media/c03c5f51-23fa-4fc2-b887-7e7e5cce30da.png)
  
## <a name="outlook-requirements-for-accessing-items-in-an-auto-expanded-archive"></a><span data-ttu-id="ad6ca-142">자동 확장 보관 위치에 있는 항목에 액세스할 수 있도록 outlook 요구 사항</span><span class="sxs-lookup"><span data-stu-id="ad6ca-142">Outlook requirements for accessing items in an auto-expanded archive</span></span>

<span data-ttu-id="ad6ca-143">자동 확장 보관 저장소에 저장 된 메시지에 액세스 하려면 사용자가 Outlook 클라이언트 중 하나를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-143">To access messages that are stored in an auto-expanded archive, users have to use one of the following Outlook clients:</span></span>
  
- <span data-ttu-id="ad6ca-144">Outlook 2016 또는 Windows 용 Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="ad6ca-144">Outlook 2016 or Outlook 2019 for Windows</span></span>
    
- <span data-ttu-id="ad6ca-145">웹용 Outlook</span><span class="sxs-lookup"><span data-stu-id="ad6ca-145">Outlook on the web</span></span> 
    
- <span data-ttu-id="ad6ca-146">Outlook 2016 또는 Mac 용 Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="ad6ca-146">Outlook 2016 or Outlook 2019 for Mac</span></span> 
    
> [!NOTE]
> <span data-ttu-id="ad6ca-p108">Outlook 2013 사용자가 원래 보관 사서함에 저장 된 액세스 항목만 수 있습니다. 추가 보관 저장소로 이동 되는 항목에 액세스 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-p108">Outlook 2013 users can only access items that were originally stored in their archive mailbox. They won't be able to access items that are moved to additional archive storage.</span></span> 
  
<span data-ttu-id="ad6ca-149">다음은 Outlook 또는 Outlook 웹에 있는 자동 확장 보관 저장소에 저장 된 메시지 액세스를 사용할 때 고려 해야할 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-149">Here are some things to consider when using Outlook or Outlook on the web to access messages stored in an auto-expanded archive.</span></span>
  
- <span data-ttu-id="ad6ca-150">자동 확장 저장소 영역으로 이동 된 원본을 비롯 하 여 보관 사서함에 있는 모든 폴더에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-150">You can access any folder in your archive mailbox, including ones that were moved to the auto-expanded storage area.</span></span>
    
- <span data-ttu-id="ad6ca-p109">추가 저장소 영역에만 폴더 자체를 검색 하 여 이동 된 항목을 검색할 수 있습니다. 즉, 검색 범위와 **현재 폴더** 옵션을 선택 하려면 폴더 목록에 보관 폴더를 선택 해야 합니다. 마찬가지로, 저장소 자동 확장 영역에서 폴더에 하위 폴더가 있는 경우 각 하위 폴더를 개별적으로 검색 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-p109">You can search for items that were moved to an additional storage area only by searching the folder itself. This means you have to select the archive folder in the folder list to select the **Current Folder** option as the search scope. Similarly, if a folder in an auto-expanded storage area contains subfolders, you have to search each subfolder separately.</span></span> 
    
- <span data-ttu-id="ad6ca-154">Outlook에서 항목을 계산 하 고 자동 확장 보관 위치에 있는 Outlook 및 웹에 있는 Outlook) (에서 읽기/읽지 않음 개수 정확 하 게 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-154">Item counts in Outlook and Read/Unread counts (in Outlook and Outlook on the web ) in an auto-expanded archive might not be accurate.</span></span>
    
- <span data-ttu-id="ad6ca-155">자동 확장 저장소 영역을 가리키는 하위 폴더의 항목은 삭제할 수 있지만 폴더 자체를 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-155">You can delete items in a subfolder that points to an auto-expanded storage area, but the folder itself can't be deleted.</span></span>
    
- <span data-ttu-id="ad6ca-156">자동 확장 저장소 영역에서 삭제 된 항목을 복구 하는 지운 편지함 복구 기능을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-156">You can't use the Recover Deleted Items feature to recover an item that was deleted from an auto-expanded storage area.</span></span>
  
## <a name="auto-expanding-archiving-and-other-office-365-compliance-features"></a><span data-ttu-id="ad6ca-157">보관 자동 확장 하 고 다른 Office 365 규정 준수 기능</span><span class="sxs-lookup"><span data-stu-id="ad6ca-157">Auto-expanding archiving and other Office 365 compliance features</span></span>

<span data-ttu-id="ad6ca-158">이 섹션에서는 보관 자동 확장 하 고 다른 Office 365 규정 준수 및 데이터 관리 방식 기능 간의 기능에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-158">This section explains the functionality between auto-expanding archiving and other Office 365 compliance and data governance features.</span></span>
  
- <span data-ttu-id="ad6ca-159">**eDiscovery** -콘텐츠 검색 하거나 원본 위치 eDiscovery, 자동 확장 보관 위치에 있는 별도 저장소 영역와 같은 Office 365 eDiscovery 도구를 사용 하는 경우 검색도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-159">**eDiscovery** - When you use an Office 365 eDiscovery tool, such as Content Search or In-Place eDiscovery, the additional storage areas in an auto-expanded archive are also searched.</span></span>
    
- <span data-ttu-id="ad6ca-160">**보존** -사서함을 놓을 때 대기 Exchange 소송 보존으로 설정 하는 등의 도구를 사용 하 여 온라인 또는 eDiscovery 사례를 포함 하 고 있으며 자동 확장 보관 저장소에 있는 Office 365 보안 & 콘텐츠 준수 센터의에서 보존 정책 보류에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-160">**Retention** - When you put a mailbox on hold by using tools such as Litigation Hold in Exchange Online or eDiscovery case holds and retention policies in the Office 365 Security & Compliance Center, content located in an auto-expanded archive is also placed on hold.</span></span>
    
- <span data-ttu-id="ad6ca-161">**메시징 레코드 관리 (MRM)** -자동 확장 보관 사서함에 있는 만료 된 항목을 만료 된 사서함 항목을 영구적으로 삭제 하려면 Exchange Online에서 MRM 삭제 정책을 사용 하는 경우도 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-161">**Messaging records management (MRM)** - If you use MRM deletion policies in Exchange Online to permanently delete expired mailbox items, expired items located in the auto-expanded archive will also be deleted.</span></span>
    
- <span data-ttu-id="ad6ca-p110">**가져올 서비스** -사용자의 자동 확장 보관을 PST 파일을 가져오려면 Office 365를 가져올 서비스를 사용할 수 있습니다. 사용자의 보관 사서함을 PST 파일의 최대 100GB의 데이터를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-p110">**Import service** - You can use the Office 365 Import service to import PST files to a user's auto-expanded archive. You can import up to 100 GB of data from PST files to the user's archive mailbox.</span></span> 

## <a name="more-information"></a><span data-ttu-id="ad6ca-164">추가 정보</span><span class="sxs-lookup"><span data-stu-id="ad6ca-164">More information</span></span>

<span data-ttu-id="ad6ca-165">보관, 참조 자동 확장 하는 방법에 대 한 자세한 기술 정보에 대 한 [Office 365: 보관 FAQ 자동 확장](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/)합니다.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-165">For more technical details about auto-expanding archiving, see [Office 365: Auto-Expanding Archives FAQ](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/).</span></span>