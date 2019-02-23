---
title: Office 365에서 소송 보존 만들기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: f2d3793eac84e8f80158842c833c30986b0549c5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218658"
---
# <a name="create-a-litigation-hold-in-office-365"></a><span data-ttu-id="329a4-102">Office 365에서 소송 보존 만들기</span><span class="sxs-lookup"><span data-stu-id="329a4-102">Create a Litigation Hold in Office 365</span></span>

<span data-ttu-id="329a4-p101">사서함에 대 한 소송 보존을 적용 하 여 삭제 된 항목을 비롯 한 모든 사서함 콘텐츠를 보존할 수 있습니다. 사용자 사서함에 소송 보존을 적용 하면 사용자의 보관 사서함에 있는 콘텐츠 (사용 하도록 설정 된 경우)도 유지 됩니다. 보류를 만들 때 삭제 및 수정 된 항목을 지정한 기간 동안 보존 하 고 사서함에서 영구적으로 삭제할 수 있도록 보존 기간 ( *시간 기반 보존*이 라고도 함)을 지정할 수도 있습니다. 또는 콘텐츠를 무기한 보존 ( *무기한 보류*라고 함) 하거나 소송 보존을 제거할 때까지 가능 합니다. 보존 기간을 지정 하는 경우에는 메시지가 수신 되거나 사서함 항목이 만들어진 날짜를 통해 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-p101">You can place a mailbox on Litigation Hold to retain all mailbox content, including deleted items and the original versions of modified items. When you place a user mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also retained. When you create a hold, you can specify a hold duration (also called a *time-based hold*) so that deleted and modified items are retained for a specified period and then permanently deleted from the mailbox. Or you can just retain content indefinitely (called an *infinite hold*) or until the Litigation Hold is removed. If you do specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> 
  
<span data-ttu-id="329a4-108">소송 보존을 만들 때 수행 되는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-108">Here's what happens when you create a Litigation Hold.</span></span>
  
- <span data-ttu-id="329a4-109">사용자가 영구적으로 삭제 한 항목은 보류 기간 동안 사용자의 사서함에 있는 복구할 수 있는 항목 폴더에 보관 됩니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-109">Items that are permanently deleted by the user are retained in the Recoverable Items folder in the user's mailbox for the duration of the hold.</span></span>
    
- <span data-ttu-id="329a4-110">사용자가 복구 가능한 항목 폴더에서 제거 된 항목은 보류 기간 동안 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-110">Items that are purged from the Recoverable Items folder by the user are retained for the duration of the hold.</span></span>
    
- <span data-ttu-id="329a4-111">복구 가능한 항목 폴더의 저장소 할당량은 30gb에서 110 GB로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-111">The storage quota for the Recoverable Items folder is increased from 30 GB to 110 GB.</span></span>
    
- <span data-ttu-id="329a4-112">사용자의 기본 및 보관 사서함에 있는 항목은 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-112">Items in the user's primary and the archive mailboxes are retained</span></span>
    
## <a name="before-you-begin"></a><span data-ttu-id="329a4-113">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="329a4-113">Before you begin</span></span>

- <span data-ttu-id="329a4-p102">exchange online 사서함에 소송 보존을 적용 하려면 exchange online 계획 2 라이선스를 할당 받아야 합니다. 사서함에 Exchange online 계획 1 라이선스가 할당 되는 경우이를 보류 상태로 설정 하려면 별도의 exchange online 보관 라이선스를 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-p102">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online Plan 2 license. If a mailbox is assigned an Exchange Online Plan 1 license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a><span data-ttu-id="329a4-116">Office 365 관리 센터에서 사서함에 소송 보존 설정</span><span class="sxs-lookup"><span data-stu-id="329a4-116">Place a mailbox on Litigation Hold in the Office 365 admin center</span></span>

<span data-ttu-id="329a4-117">다음은 Office 365 관리 센터를 사용 하 여 maibox에 소송 보존을 적용 하는 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-117">Here are the steps to place a maibox on Litigation Hold using the Office 365 admin center.</span></span>

1. <span data-ttu-id="329a4-118">로 이동 https://portal.office.com/adminportal/home 하 고 전역 관리자 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-118">Go to https://portal.office.com/adminportal/home and sign in using your global administrator account.</span></span>
2. <span data-ttu-id="329a4-119">왼쪽 탐색 창에서 **사용자** > **활성 사용자** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-119">Click **Users** > **Active users** in the left navigation pane.</span></span>
3. <span data-ttu-id="329a4-120">사서함에 소송 보존을 적용 하려는 사용자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-120">Select the user whose mailbox you want to place on Litigation Hold.</span></span>
4. <span data-ttu-id="329a4-121">플라이 아웃 페이지에서 **메일 설정을**클릭 한 다음 **소송 보존**옆의 **편집** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-121">On the fly-out page, click **Mail settings**, and then click **Edit** next to **Litigation hold**.</span></span>
5. <span data-ttu-id="329a4-122">**소송 보존** 페이지에서 설정/해제를 클릭 하 여 소송 보존을 설정 하 고 표시 되는 다음 선택적 설정을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-122">On the **Litigation hold** page, click the toggle to turn on Litigation Hold and complete the following optional settings that are displayed:</span></span>
 
    ![O365_LitigationHold1-.png](media/O365-LitigationHold1.png)

    <span data-ttu-id="329a4-p103">a: **보존 기간 (일)** -이 상자를 사용 하 여 시간 기반 보존을 만들고 사서함이 소송 보존 상태에 있을 때 사서함 항목이 보관 되는 기간을 지정 합니다. 기간은 사서함 항목을 받거나 만든 날짜 로부터 계산 됩니다. 이 상자를 비워 두면 항목이 무기한으로 또는 보존이 제거 될 때까지 유지 됩니다. 기간을 지정 하려면 days를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-p103">a. **Hold duration (days)** - Use this box to create a time-based hold and specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span>
    
    <span data-ttu-id="329a4-p104">b. **참고** -이 상자를 사용 하 여 사용자의 사서함이 소송 보존 상태에 있음을 알립니다. 메모는 Outlook 2010 이상 버전을 사용 중인 경우 사용자 사서함의 계정 정보 페이지에 표시 됩니다. 사용자는이 페이지에 액세스 하 여 Outlook에서 **파일** 을 클릭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-p104">b. **Note** - Use this box to inform the user their mailbox is on Litigation Hold. The note will appear on the Account Information page in the user's mailbox if they're using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
     
    <span data-ttu-id="329a4-p105">c. **웹 페이지** -소송 보존에 대 한 자세한 내용은이 상자를 사용 하 여 웹 사이트를 사용자에 게 안내 합니다. 이 URL은 사용자 사서함의 계정 정보 페이지에서 Outlook 2010 이상 버전을 사용 하는 경우에 표시 됩니다. 사용자는이 페이지에 액세스 하 여 Outlook에서 **파일** 을 클릭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-p105">c. **Web page** - Use this box to direct the user to a website for more information about Litigation Hold. This URL appears on the Account Information page in the user's mailbox if they are using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
 
6. <span data-ttu-id="329a4-137">**저장** 을 클릭 하 여 소송 보존을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-137">Click **Save** to create the Litigation Hold.</span></span>

<span data-ttu-id="329a4-138">보류를 만든 후에는 플라이 아웃 페이지의 메일 설정에 선택한 사용자에 대 한 소송 보류가 설정 된 것으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="329a4-138">After you create the hold, the mail settings on the fly-out page shows that Litigation Hold is turned on for the selected user.</span></span>

![O365_LitigationHold2-.png](media/O365-LitigationHold2.png)

<span data-ttu-id="329a4-140">소송 보존을 만들고 관리 하는 방법과 Exchange Online PowerShell을 사용 하 여 소송 보존을 대량으로 만드는 방법에 대 한 자세한 내용은 [사서함에 소송 보존](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="329a4-140">For more information about creating and managing Litigation Holds and using Exchange Online PowerShell to bulk-create Litigation Holds, see [Place a mailbox on Litigation Hold](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span></span>
