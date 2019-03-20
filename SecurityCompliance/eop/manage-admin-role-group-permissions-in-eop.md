---
title: EOP에서 관리자 역할 그룹 권한 관리
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 125834f4-1024-4325-ad5a-d2573cfb005e
description: Microsoft EOP(Exchange Online Protection)에서는 EAC(Exchange 관리 센터)를 통해 사용자를 하나 이상의 역할 그룹 구성원으로 지정하여 해당 그룹에 특정 관리 작업을 수행하기 위한 권한을 할당할 수 있습니다. 또한 EAC를 사용하여 하나 이상의 역할 그룹에서 사용자를 제거할 수도 있습니다.
ms.openlocfilehash: aed32c8a9224bc60ef3e4a1ac9be9d797e61bda8
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693427"
---
# <a name="manage-admin-role-group-permissions-in-eop"></a><span data-ttu-id="e7f16-104">EOP에서 관리자 역할 그룹 권한 관리</span><span class="sxs-lookup"><span data-stu-id="e7f16-104">Manage admin role group permissions in EOP</span></span>
  
<span data-ttu-id="e7f16-p102">Microsoft EOP(Exchange Online Protection)에서는 EAC(Exchange 관리 센터)를 통해 사용자를 하나 이상의 역할 그룹 구성원으로 지정하여 해당 그룹에 특정 관리 작업을 수행하기 위한 권한을 할당할 수 있습니다. 또한 EAC를 사용하여 하나 이상의 역할 그룹에서 사용자를 제거할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7f16-p102">In Microsoft Exchange Online Protection (EOP), you can use the Exchange admin center (EAC) to make a user a member of a role group or groups in order to assign them permissions to perform specific administrative tasks. You can also remove a user from a role group or groups by using the EAC.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="e7f16-107">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="e7f16-107">What do you need to know before you begin?</span></span>

- <span data-ttu-id="e7f16-108">예상 완료 시간: 5~10분</span><span class="sxs-lookup"><span data-stu-id="e7f16-108">Estimated time to complete: 5-10 minutes</span></span>
    
- <span data-ttu-id="e7f16-p103">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인하려면 다음을 참조하세요. [EOP의 기능 사용 권한](feature-permissions-in-eop.md)의 "사용자, 연락처 및 역할 그룹" 항목</span><span class="sxs-lookup"><span data-stu-id="e7f16-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
    
- <span data-ttu-id="e7f16-p104">Office 365의 특정 사용 권한은 EPO 관리자 역할 그룹 사용 권한으로 매핑됩니다. 자세한 내용은 [관리자 역할 지정](https://go.microsoft.com/fwlink/p/?LinkId=286708)의 "사용자의 Office 365 권한으로 확장되는 서비스에는 무엇이 있습니까?" 섹션에서 "Exchange Online 역할" 열을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="e7f16-p104">Certain permissions in Office 365 map to EOP admin role group permissions. For more information, see the "Role in Exchange Online" column in the "Which services do my Office 365 permissions extend to?" section in [Assigning Admin Roles](https://go.microsoft.com/fwlink/p/?LinkId=286708).</span></span>
    
- <span data-ttu-id="e7f16-114">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Keyboard shortcuts in Exchange 2013**을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e7f16-114">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="e7f16-p105">문제가 있습니까? Exchange 포럼에서 도움을 요청하세요. 포럼 주소는 다음과 같습니다.[Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), 또는 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351)</span><span class="sxs-lookup"><span data-stu-id="e7f16-p105">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="what-do-you-want-to-do"></a><span data-ttu-id="e7f16-118">무슨 작업을 하고 싶으십니까?</span><span class="sxs-lookup"><span data-stu-id="e7f16-118">What do you want to do?</span></span>

### <a name="use-the-eac-to-assign-members-to-admin-role-groups"></a><span data-ttu-id="e7f16-119">EAC를 사용하여 관리자 역할 그룹에 구성원 할당</span><span class="sxs-lookup"><span data-stu-id="e7f16-119">Use the EAC to assign members to admin role groups</span></span>

1. <span data-ttu-id="e7f16-120">EAC에서 **사용 권한** \> **관리자 역할로**이동 하 여 사용자를 추가 하려는 역할 그룹을 클릭 한 다음 편집 아이콘 \*\*\*\* ![](../media/ITPro-EAC-EditIcon.gif)편집을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f16-120">In the EAC, navigate to **Permissions** \> **Admin Roles**, click the role group that you want to add the user or users to, and then click **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif).</span></span>
    
2. <span data-ttu-id="e7f16-p106">구성원에서 **추가**![아이콘 추가](../media/ITPro-EAC-AddIcon.gif)를 클릭합니다. 구성원 선택 창이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="e7f16-p106">Under Members, click **Add**![Add Icon](../media/ITPro-EAC-AddIcon.gif). The Select Members window will appear.</span></span>
    
3. <span data-ttu-id="e7f16-123">추가할 사용자를 한 명 이상 검색하거나 목록에서 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f16-123">Search for the user or users that you wish to add, or select them from the list.</span></span>
    
4. <span data-ttu-id="e7f16-p107">추가할 사용자를 한 명 이상 선택한 후 **추가**, **확인**을 차례로 클릭합니다. 그러면 구성원 선택 창이 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="e7f16-p107">When you have selected the user or users that you want to add, click **Add**, and then click **OK**. The Select Members window will close.</span></span>
    
5. <span data-ttu-id="e7f16-p108">사용자가 **구성원** 창에 추가된 것을 확인할 수 있습니다. **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f16-p108">You will see that the user has been added to the **Members** pane. Click **Save**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e7f16-128">구성원을 역할 그룹에 추가하거나 역할 그룹에서 제거한 후 사용자가 관리 권한 변경 내용을 확인하려면 로그아웃했다가 다시 로그인해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7f16-128">Users may have to sign out and sign in again to see the change in their administrative rights after you add or remove members from the role group.</span></span> 
  
### <a name="use-the-eac-to-remove-members-from-admin-role-groups"></a><span data-ttu-id="e7f16-129">EAC를 사용하여 관리자 역할 그룹에서 구성원 제거</span><span class="sxs-lookup"><span data-stu-id="e7f16-129">Use the EAC to remove members from admin role groups</span></span>

1. <span data-ttu-id="e7f16-130">EAC에서 **사용 권한** \> **관리자 역할로**이동 하 여 사용자를 제거할 역할 그룹을 클릭 한 다음 편집 아이콘 \*\*\*\* ![](../media/ITPro-EAC-EditIcon.gif)편집을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f16-130">In the EAC, navigate to **Permissions** \> **Admin Roles**, click the role group that you want to remove a user or users from, and then click **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif).</span></span>
    
2. <span data-ttu-id="e7f16-131">구성원에서 제거할 사용자를 한 명 이상 선택하고 **제거**![아이콘 제거](../media/ITPro-EAC-RemoveIcon.gif)를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f16-131">Under Members, select the user or users that you want to remove and click **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.gif).</span></span>
    
3. <span data-ttu-id="e7f16-p109">**저장**을 클릭하여 역할 그룹의 변경 내용을 저장하고 **관리자 역할** 페이지로 돌아갑니다. 사용자가 관리자 역할 그룹에서 제거되었는지 확인하려면 해당 구성원이 선택한 역할 그룹의 세부 정보 창에서 구성원 아래에 더 이상 표시되지 않는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f16-p109">Click **Save** to save the change to the role group and return to the **Admin Roles** page. To verify that you've successfully removed the user from the administrator role group, make sure the member is no longer displayed under Members in the details pane for the selected role group.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="e7f16-134">구성원을 역할 그룹에 추가하거나 역할 그룹에서 제거한 후 사용자가 관리 권한 변경 내용을 확인하려면 로그아웃했다가 다시 로그인해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7f16-134">Users may have to sign out and sign in again to see the change in their administrative rights after you add or remove members from the role group.</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="e7f16-135">추가 정보</span><span class="sxs-lookup"><span data-stu-id="e7f16-135">For more information</span></span>

[<span data-ttu-id="e7f16-136">EOP의 기능 사용 권한</span><span class="sxs-lookup"><span data-stu-id="e7f16-136">Feature permissions in EOP</span></span>](feature-permissions-in-eop.md)
  

