---
title: 사용자에게 Office 365 보안 및 준수 센터에 대한 액세스 권한 부여
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
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
description: 사용자는 보안 또는 규정 준수 기능을 관리 하기 전에 Office 365 보안 & 준수 센터에서 사용 권한을 할당 받아야 합니다.
ms.openlocfilehash: 7963a8c3db64e83566960abe9298b9a2d636ae53
ms.sourcegitcommit: 6302a43d947a908dd10a8e40550b806f491692fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/13/2019
ms.locfileid: "35645123"
---
# <a name="give-users-access-to-the-office-365-security--compliance-center"></a><span data-ttu-id="47cef-103">사용자에게 Office 365 보안 및 준수 센터에 대한 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="47cef-103">Give users access to the Office 365 Security & Compliance Center</span></span>

<span data-ttu-id="47cef-104">사용자는 보안 또는 규정 준수 기능을 관리 하기 전에 Office 365 보안 & 준수 센터에서 사용 권한을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-104">Users need to be assigned permissions in the Office 365 Security & Compliance Center before they can manage any of its security or compliance features.</span></span> <span data-ttu-id="47cef-105">보안 & 준수 센터에서 Office 365 전역 관리자 또는 OrganizationManagement 역할 그룹의 구성원으로 사용자에 게 이러한 사용 권한을 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-105">As an Office 365 global admin or member of the OrganizationManagement role group in the Security & Compliance Center, you can give these permissions to users.</span></span> <span data-ttu-id="47cef-106">사용자는 액세스 권한을 부여 받은 보안 또는 규정 준수 기능만 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-106">Users will only be able to manage the security or compliance features that you give them access to.</span></span> 
  
<span data-ttu-id="47cef-107">보안 & 준수 센터에서 사용자에 게 부여할 수 있는 다양 한 사용 권한에 대 한 자세한 내용은 [Office 365 보안 & 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="47cef-107">For more information about the different permissions you can give to users in the Security & Compliance Center, check out [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="47cef-108">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="47cef-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="47cef-109">이 문서의 단계를 완료 하려면 Office 365 전역 관리자 이거나 보안 & 준수 센터에서 OrganizationManagement 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-109">You need to be an Office 365 global admin, or a member of the OrganizationManagement role group in the Security & Compliance Center, to complete the steps in this article.</span></span>

- <span data-ttu-id="47cef-110">보안 & 준수 센터의 역할 그룹은 Exchange Online의 역할 그룹과 유사한 이름을 사용할 수 있지만 동일 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-110">Role groups for the Security & Compliance Center might have similar names to the role groups in Exchange Online, but they're not the same.</span></span>

- <span data-ttu-id="47cef-111">역할 그룹 구성원 자격은 Exchange Online과 보안 & 준수 센터 간에 공유 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-111">Role group memberships aren't shared between Exchange Online and the Security & Compliance Center.</span></span>

- <span data-ttu-id="47cef-112">(AOBO) 권한이 있는 DAP (위임 된 액세스 권한) 사용 권한을 사용 하는 경우에는 보안 & 준수 센터에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-112">Delegated Access Permission (DAP) partners with Administer On Behalf Of (AOBO) permissions can't access the Security & Compliance Center.</span></span>

## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security--compliance-center"></a><span data-ttu-id="47cef-113">Office 365 관리 센터를 사용 하 여 다른 사용자에 게 보안 & 준수 센터에 대 한 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="47cef-113">Use the Office 365 admin center to give another user access to the Security & Compliance Center</span></span>

1. <span data-ttu-id="47cef-114">[Office 365에 로그인 하 고 관리 센터로 이동](https://go.microsoft.com/fwlink/p/?LinkId=525275)합니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-114">[Sign in to Office 365 and go to the Admin center](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span></span>

2. <span data-ttu-id="47cef-115">Office 365 관리 센터에서 **관리 센터** 를 열고 **보안 & 준수**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-115">In the Office 365 admin center, open **Admin centers** and then click **Security & Compliance**.</span></span>

3. <span data-ttu-id="47cef-116">보안 & 준수 센터에서 **사용 권한**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-116">In the Security & Compliance Center, go to **Permissions**.</span></span>

4. <span data-ttu-id="47cef-117">목록에서 사용자를 추가 하려는 역할 그룹을 선택 하 고 편집 아이콘](media/O365-MDM-CreatePolicy-EditIcon.gif) **편집** ![을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-117">From the list, choose the role group that you want to add the user to and click **Edit** ![Edit icon](media/O365-MDM-CreatePolicy-EditIcon.gif).</span></span>

5. <span data-ttu-id="47cef-118">역할 그룹의 속성 페이지 **구성원**아래에 있는 추가 아이콘 \*\*\*\*![](media/ITPro-EAC-AddIcon.gif) 추가를 클릭 하 고 추가 하려는 사용자의 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-118">In the role group's properties page under **Members**, click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and select the name of the user (or users) you want to add.</span></span>

6. <span data-ttu-id="47cef-119">역할 그룹에 추가 하려는 모든 사용자를 선택 했으면 \*\*추가\> \*\* 를 클릭 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-119">When you've selected all of the users you want to add to the role group, click **add-\>** and then **OK**.</span></span>

7. <span data-ttu-id="47cef-120">**저장**을 클릭하여 역할 그룹에 대한 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-120">Click **Save** to save the changes to the role group.</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="47cef-121">작동 여부는 어떻게 확인합니까?</span><span class="sxs-lookup"><span data-stu-id="47cef-121">How do you know this worked?</span></span>

1. <span data-ttu-id="47cef-122">보안 & 준수 센터에서 **사용 권한**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-122">In the Security & Compliance Center, go to **Permissions**.</span></span>

2. <span data-ttu-id="47cef-123">목록에서 구성원을 볼 역할 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-123">From the list, select the role group to view the members.</span></span>

3. <span data-ttu-id="47cef-124">역할 그룹 세부 정보의 오른쪽에서 역할 그룹의 구성원을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-124">On the right, in the role group details, you can view the members of the role group.</span></span>

## <a name="use-powershell-to-give-another-user-access-to-the-security--compliance-center"></a><span data-ttu-id="47cef-125">PowerShell을 사용 하 여 다른 사용자에 게 보안 & 준수 센터에 대 한 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="47cef-125">Use PowerShell to give another user access to the Security & Compliance Center</span></span>

1. <span data-ttu-id="47cef-126">[Office 365 보안 & 준수 센터 PowerShell에 연결](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)합니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-126">[Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

2. <span data-ttu-id="47cef-127">다음 예와 같이 **Add-RoleGroupMember** 명령을 사용하여 사용자를 조직 관리 역할에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-127">Use the **Add-RoleGroupMember** command to add a user to the Organization Management Role, as shown in the following example.</span></span>

   ```
   Add-RoleGroupMember -Identity "Organization Management" -Member MatildaS
   ```

   <span data-ttu-id="47cef-128">**매개 변수**:</span><span class="sxs-lookup"><span data-stu-id="47cef-128">**Parameters**:</span></span>
  
   - <span data-ttu-id="47cef-129">_Identity_ 는 구성원을 추가할 역할 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-129">_Identity_ is the role group to add a member to.</span></span>

   - <span data-ttu-id="47cef-130">_구성원_ 은 역할 그룹에 추가할 사서함, USG (유니버설 보안 그룹) 또는 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-130">_Member_ is the mailbox, universal security group (USG), or computer to add to the role group.</span></span> <span data-ttu-id="47cef-131">구성원은 한 번에 하나만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-131">You can specify only one member at a time.</span></span>

<span data-ttu-id="47cef-132">구문 및 매개 변수에 대 한 자세한 내용은 [추가-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="47cef-132">For detailed information on syntax and parameters, see [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span></span>
  
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="47cef-133">작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="47cef-133">How do you know this worked?</span></span>

<span data-ttu-id="47cef-134">사용자에 게 보안 & 준수 센터에 대 한 액세스 권한이 있는지 확인 하려면 다음 예제와 같이 **Get-RoleGroupMember** cmdlet을 사용 하 여 조직 관리 역할 그룹의 구성원을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="47cef-134">To verify that you've given users access to the Security & Compliance Center, use the **Get-RoleGroupMember** cmdlet to view the members in the Organization Management role group, as shown in the following example.</span></span>
  
```
Get-RoleGroupMember -Identity "Organization Management"
```

<span data-ttu-id="47cef-135">구문 및 매개 변수에 대 한 자세한 내용은 [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="47cef-135">For detailed information on syntax and parameters, see [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span></span>
