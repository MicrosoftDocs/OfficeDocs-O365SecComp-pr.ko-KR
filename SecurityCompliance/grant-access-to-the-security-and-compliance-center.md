---
title: 사용자에 게 Office 365 보안 &amp; 및 준수 센터에 대 한 액세스 권한 부여
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/18/2017
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: 사용자는 보안 또는 규정 준수 기능을 관리 하기 전에 &amp; Office 365 보안 및 준수 센터에서 사용 권한을 할당 받아야 합니다.
ms.openlocfilehash: 0a3f0d1ddde7d269a0f8f9596c5c3de14e94429d
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216308"
---
# <a name="give-users-access-to-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="57595-103">사용자에 게 Office 365 보안 &amp; 및 준수 센터에 대 한 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="57595-103">Give users access to the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="57595-p101">사용자는 보안 또는 규정 준수 기능을 관리 하기 전에 &amp; Office 365 보안 및 준수 센터에서 사용 권한을 할당 받아야 합니다. 보안 &amp; 및 준수 센터에서 Office 365 전역 관리자 또는 OrganizationManagement 역할 그룹의 구성원으로 사용자에 게 이러한 사용 권한을 부여할 수 있습니다. 사용자는 액세스 권한을 부여 하는 보안 또는 규정 준수 기능만 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57595-p101">Users need to be assigned permissions in the Office 365 Security &amp; Compliance Center before they can manage any of its security or compliance features. As an Office 365 global admin or member of the OrganizationManagement role group in the Security &amp; Compliance Center, you can give these permissions to users. Users will only be able to manage the security or compliance features that you give them access to.</span></span> 
  
<span data-ttu-id="57595-107">보안 &amp; 및 준수 센터에서 사용자에 게 부여할 수 있는 다양 한 사용 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57595-107">For more information about the different permissions you can give to users in the Security &amp; Compliance Center, check out [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="57595-108">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="57595-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="57595-109">이 문서의 단계를 완료 하려면 Office 365 전역 관리자 이거나 보안 &amp; 및 준수 센터의 OrganizationManagement 역할 그룹 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="57595-109">You need to be an Office 365 global admin, or a member of the OrganizationManagement role group in the Security &amp; Compliance Center, to complete the steps in this article.</span></span>
    
- <span data-ttu-id="57595-110">보안 &amp; 및 준수 센터의 역할 그룹은 Exchange Online의 역할 그룹과 유사한 이름을 사용할 수 있지만 동일 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57595-110">Role groups for the Security &amp; Compliance Center might have similar names to the role groups in Exchange Online, but they're not the same.</span></span> 
    
- <span data-ttu-id="57595-111">역할 그룹 구성원 자격은 Exchange Online과 보안 &amp; 및 준수 센터 간에 공유 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57595-111">Role group memberships aren't shared between Exchange Online and the Security &amp; Compliance Center.</span></span>
    
## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security-amp-compliance-center"></a><span data-ttu-id="57595-112">Office 365 관리 센터를 사용 하 여 다른 사용자에 게 보안 &amp; 및 준수 센터에 대 한 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="57595-112">Use the Office 365 admin center to give another user access to the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="57595-113">[Office 365에 로그인 하 고 관리 센터로 이동](https://go.microsoft.com/fwlink/p/?LinkId=525275)합니다.</span><span class="sxs-lookup"><span data-stu-id="57595-113">[Sign in to Office 365 and go to the Admin center](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span></span>
    
2. <span data-ttu-id="57595-114">Office 365 관리 센터에서 **관리 센터** 를 열고 **보안 &amp; 준수**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="57595-114">In the Office 365 admin center, open **Admin centers** and then click **Security &amp; Compliance**.</span></span> 
    
3. <span data-ttu-id="57595-115">보안 &amp; 및 준수 센터에서 **사용 권한**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="57595-115">In the Security &amp; Compliance Center, go to **Permissions**.</span></span>
    
4. <span data-ttu-id="57595-116">목록에서 사용자를 추가 하려는 역할 그룹을 선택 하 고 편집 아이콘](media/O365_MDM_CreatePolicy_EditIcon.gif) **편집** ![을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="57595-116">From the list, choose the role group that you want to add the user to and click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
5. <span data-ttu-id="57595-117">역할 그룹의 속성 페이지 **구성원**아래에 있는 추가 아이콘 \*\*\*\*![](media/ITPro-EAC-AddIcon.gif) 추가를 클릭 하 고 추가 하려는 사용자의 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="57595-117">In the role group's properties page under **Members**, click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and select the name of the user (or users) you want to add.</span></span> 
    
6. <span data-ttu-id="57595-118">역할 그룹에 추가 하려는 모든 사용자를 선택 했으면 \*\*추가\> \*\* 를 클릭 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="57595-118">When you've selected all of the users you want to add to the role group, click **add-\>** and then **OK**.</span></span>
    
7. <span data-ttu-id="57595-119">**저장**을 클릭하여 역할 그룹에 대한 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="57595-119">Click **Save** to save the changes to the role group.</span></span> 
    
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="57595-120">작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="57595-120">How do you know this worked?</span></span>

1. <span data-ttu-id="57595-121">보안 &amp; 및 준수 센터에서 **사용 권한**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="57595-121">In the Security &amp; Compliance Center, go to **Permissions**.</span></span>
    
2. <span data-ttu-id="57595-122">목록에서 구성원을 볼 역할 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="57595-122">From the list, select the role group to view the members.</span></span>
    
3. <span data-ttu-id="57595-123">역할 그룹 세부 정보의 오른쪽에서 역할 그룹의 구성원을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57595-123">On the right, in the role group details, you can view the members of the role group.</span></span>
    
## <a name="use-powershell-to-give-another-user-access-to-the-security-amp-compliance-center"></a><span data-ttu-id="57595-124">PowerShell을 사용 하 여 다른 사용자에 게 보안 &amp; 및 준수 센터에 대 한 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="57595-124">Use PowerShell to give another user access to the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="57595-125">[Office 365 Security & 준수 센터 PowerShell에 연결](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)합니다.</span><span class="sxs-lookup"><span data-stu-id="57595-125">[Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>
    
2. <span data-ttu-id="57595-126">다음 예와 같이 **Add-RoleGroupMember** 명령을 사용하여 사용자를 조직 관리 역할에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="57595-126">Use the **Add-RoleGroupMember** command to add a user to the Organization Management Role, as shown in the following example.</span></span> 
    
  ```
  Add-RoleGroupMember -Identity "OrganizationManagement" -Member MatildaS
  
  ```

 <span data-ttu-id="57595-127">**매개 변수**</span><span class="sxs-lookup"><span data-stu-id="57595-127">**Parameters**</span></span>
  
- <span data-ttu-id="57595-128">_-Identity_는 구성원을 추가할 역할 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="57595-128">_-Identity_ is the role group to add a member to.</span></span> 
    
- <span data-ttu-id="57595-p102">_구성원_ 은 역할 그룹에 추가할 사서함, USG (유니버설 보안 그룹) 또는 컴퓨터입니다. 구성원을 한 번에 하나만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57595-p102">_Member_ is the mailbox, universal security group (USG), or computer to add to the role group. You can specify only one member at a time.</span></span> 
    
<span data-ttu-id="57595-131">구문 및 매개 변수에 대 한 자세한 내용은 [추가-rolegroupmember](https://go.microsoft.com/fwlink/p/?LinkId=510859)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="57595-131">For detailed information on syntax and parameters, see [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span></span>
  
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="57595-132">작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="57595-132">How do you know this worked?</span></span>

<span data-ttu-id="57595-133">사용자에 게 보안 &amp; 준수 센터에 대 한 액세스 권한을 부여 했는지 확인 하려면 다음 예제와 같이 **Get-rolegroupmember** cmdlet을 사용 하 여 조직 관리 역할 그룹의 구성원을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="57595-133">To verify that you've given users access to the Security &amp; Compliance Center, use the **Get-RoleGroupMember** cmdlet to view the members in the Organization Management role group, as shown in the following example.</span></span> 
  
```
Get-RoleGroupMember -Identity "OrganizationManagement"

```

<span data-ttu-id="57595-134">구문 및 매개 변수에 대 한 자세한 내용은 [Get-rolegroupmember](https://go.microsoft.com/fwlink/p/?LinkId=510860)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="57595-134">For detailed information on syntax and parameters, see [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span></span>
  

