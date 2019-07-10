---
title: EOP에서 그룹 관리
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 212e68ac-6330-47e9-a169-6cf5e2f21e13
description: EOP(Exchange Online Protection)를 사용하여 Exchange 조직에 메일 사용 가능 그룹을 만들 수 있습니다. 또한 구성원 자격, 전자 메일 주소 및 그룹의 기타 측면을 지정하는 그룹 속성을 정의하거나 업데이트할 수도 있습니다.
ms.openlocfilehash: 2763ca35456bb40b5b11e38eb2e7497934115d5f
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599644"
---
# <a name="manage-groups-in-eop"></a><span data-ttu-id="6f4aa-104">EOP에서 그룹 관리</span><span class="sxs-lookup"><span data-stu-id="6f4aa-104">Manage groups in EOP</span></span>

 <span data-ttu-id="6f4aa-p102">EOP(Exchange Online Protection)를 사용하여 Exchange 조직에 메일 사용 가능 그룹을 만들 수 있습니다. 또한 구성원 자격, 전자 메일 주소 및 그룹의 기타 측면을 지정하는 그룹 속성을 정의하거나 업데이트할 수도 있습니다. 필요에 따라 메일 그룹 및 보안 그룹을 만들 수 있습니다. 이러한 그룹은 EAC(Exchange 관리 센터)를 사용하거나 원격 Windows PowerShell을 통해 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p102">You can use Exchange Online Protection (EOP) to create mail-enabled groups for an Exchange organization. You can also use EOP to define or update group properties that specify membership, email addresses, and other aspects of groups. You can create distribution groups and security groups, depending on your needs. These groups can be created by using the Exchange admin center (EAC) or via remote Windows PowerShell.</span></span> 
  
## <a name="types-of-mail-enabled-groups"></a><span data-ttu-id="6f4aa-109">메일 사용 가능 그룹의 유형</span><span class="sxs-lookup"><span data-stu-id="6f4aa-109">Types of mail-enabled groups</span></span>

<span data-ttu-id="6f4aa-110">Exchange 조직에 대해 다음과 같은 두 가지 유형의 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-110">You can create two types of groups for your Exchange organization:</span></span>
  
- <span data-ttu-id="6f4aa-p103">메일 그룹이라고도 하는 [EAC에서 그룹 만들기](manage-groups-in-eop.md)은 특정 관심 영역과 관련하여 전자 메일을 보내거나 받아야 하는 팀 또는 임시 그룹과 같은 전자 메일 사용자 집합입니다. 메일 그룹은 전자 메일 메시지 배포 전용으로 사용됩니다. EOP에서 메일 그룹은 보안 컨텍스트 유무에 관계없이 모든 메일 사용 가능 그룹을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p103">[Create a group in the EAC](manage-groups-in-eop.md) (also known as distribution groups) are collections of email users, such as a team or other ad hoc group, who need to receive or send email regarding a common area of interest. Distribution groups are exclusively for distributing email messages. In EOP, a distribution group refers to any mail-enabled group, whether or not it has a security context.</span></span>
    
- <span data-ttu-id="6f4aa-p104">보안 그룹이라고도 하는 [EAC에서 그룹 편집 또는 제거](manage-groups-in-eop.md)은 관리자 역할에 대한 액세스 권한이 있어야 하는 전자 메일 사용자 집합입니다. 예를 들어 특정 사용자 그룹에게 스팸 방지 및 맬웨어 방지 설정을 구성할 수 있도록 관리자 역할 권한을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p104">[Edit or remove a group in the EAC](manage-groups-in-eop.md) (also known as security groups) are collections of email users who need access permissions for Admin roles. For example, you might want to give specific group of users admin role permissions so they can configure anti-spam and anti-malware settings.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6f4aa-p105">기본적으로 모든 새로운 메일 사용이 가능한 보안 그룹을 사용하려면 모든 보낸 사람에 대한 인증이 필요합니다. 따라서 외부 보낸 사람은 메일 사용이 가능한 보안 그룹에 메시지를 보낼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p105">By default, all new mail-enabled security groups require that all senders be authenticated. This prevents external senders from sending messages to mail-enabled security groups.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="6f4aa-118">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="6f4aa-118">Before you begin</span></span>

- <span data-ttu-id="6f4aa-p106">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인하려면 다음을 참조하세요. [EOP의 기능 사용 권한](feature-permissions-in-eop.md) 항목의 "메일 그룹 및 보안 그룹" 항목</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p106">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Distribution Groups and Security Groups" entry in the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
    
- <span data-ttu-id="6f4aa-121">원격 PowerShell cmdlet을 사용하여 그룹을 만들고 관리할 경우 제한에 도달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-121">Be aware that when creating and managing groups by using remote PowerShell cmdlets, you may encounter throttling.</span></span>
    
- <span data-ttu-id="6f4aa-122">이 cmdlet은 일괄 처리 방법을 사용하므로 cmdlet 결과가 보이기 몇 분 전에 전파 지연이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-122">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span>
    
- <span data-ttu-id="6f4aa-123">Windows PowerShell을 사용하여 Exchange Online Protection에 연결하는 방법에 대한 자세한 내용은 [원격 PowerShell을 사용하여 Exchange Online Protection에 연결](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-123">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).</span></span>
    
- <span data-ttu-id="6f4aa-124">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Keyboard shortcuts in Exchange 2013**을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-124">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="6f4aa-p107">문제가 있습니까? Exchange 포럼에서 도움을 요청하세요. 포럼 주소는 다음과 같습니다.[Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), 또는 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351)</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p107">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="create-a-group-in-the-eac"></a><span data-ttu-id="6f4aa-128">EAC에서 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="6f4aa-128">Create a group in the EAC</span></span>

1. <span data-ttu-id="6f4aa-129">EAC(Exchange 관리 센터)에서 **받는 사람** \> **그룹**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-129">In the Exchange admin center (EAC), go to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="6f4aa-p108">**새로 만들기**![아이콘 추가](../media/ITPro-EAC-AddIcon.gif)를 클릭한 다음 필요에 따라 **메일 그룹** 또는 **보안 그룹**을 클릭합니다. 두 그룹의 차이점은 [메일 사용 가능 그룹의 유형](manage-groups-in-eop.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p108">Click **New**![Add Icon](../media/ITPro-EAC-AddIcon.gif), and then click **Distribution group** or **Security group**, depending on your needs. See [Types of mail-enabled groups](manage-groups-in-eop.md) for the distinction.</span></span> 
    
3. <span data-ttu-id="6f4aa-132">**새 메일 그룹** 또는 **새 보안 그룹** 페이지에서 다음 필드에 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-132">On the **New distribution group** or **New security group** page, complete the following fields:</span></span> 
    
  - <span data-ttu-id="6f4aa-p109">**표시 이름** 조직에서 고유하며 EOP 사용자에게 의미가 있는 표시 이름을 입력합니다. 표시 이름은 필수 입력 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p109">**Display name** Type a display name that's unique to your organization and meaningful to EOP users. The display name is required.</span></span> 
    
  - <span data-ttu-id="6f4aa-p110">**별칭** 조직에서 고유한 그룹 별칭을 64자까지 입력합니다. EOP 사용자가 전자 메일 메시지의 받는 사람: 줄에 입력하는 별칭은 그룹의 표시 이름으로 확인됩니다. 별칭을 변경하는 경우 그룹의 기본 SMTP 주소도 변경되며 새 별칭이 포함됩니다. 별칭은 필수 입력 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p110">**Alias** Type a group alias of up to 64 characters that's unique to your organization. EOP users type the alias in the To: line of email messages and the alias resolves to the group's display name. If you change the alias, the primary SMTP address for the group also changes and will contain the new alias. The alias is required.</span></span> 
    
  - <span data-ttu-id="6f4aa-139">**설명** 다른 사람들이 그룹의 용도를 파악할 수 있도록 그룹 설명을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-139">**Description** Type a description of the group so that people will know the purpose of the group.</span></span> 
    
  - <span data-ttu-id="6f4aa-p111">**소유자** 기본적으로 그룹을 만든 사람이 소유자입니다. **추가**![아이콘 추가](../media/ITPro-EAC-AddIcon.gif)를 선택하여 소유자를 추가할 수 있습니다. 모든 그룹에는 한 명 이상의 소유자가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p111">**Owners** By default, the person who creates the group is the owner. You can add an owner by choosing **Add**![Add Icon](../media/ITPro-EAC-AddIcon.gif). All groups must have at least one owner.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6f4aa-143">소유자는 그룹의 구성원이 아니어도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-143">Owners don't have to be members of the group.</span></span> 
  
  - <span data-ttu-id="6f4aa-p112">**구성원** 이 섹션을 사용하면 그룹 구성원을 추가하고 그룹에 구독하거나 그룹에서 탈퇴하려는 사용자에 대해 승인이 필요한지 여부를 지정할 수 있습니다. 그룹에 구성원을 추가하려면 **추가**![아이콘 추가](../media/ITPro-EAC-AddIcon.gif)를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p112">**Members** Use this section to add group members and to specify whether approval is required for people to join or leave the group. To add members to the group, click **Add**![Add Icon](../media/ITPro-EAC-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="6f4aa-146">**확인**을 클릭하여 원래 페이지로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-146">Click **OK** to return to the original page.</span></span> 
    
5. <span data-ttu-id="6f4aa-p113">작업을 마치면 **저장**을 클릭하여 그룹을 만듭니다. 그러면 새 그룹이 그룹 목록에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p113">When you've finished, click **Save** to create the group. The new group should appear in the list of groups.</span></span> 
    
## <a name="edit-or-remove-a-group-in-the-eac"></a><span data-ttu-id="6f4aa-149">EAC에서 그룹 편집 또는 제거</span><span class="sxs-lookup"><span data-stu-id="6f4aa-149">Edit or remove a group in the EAC</span></span>

1. <span data-ttu-id="6f4aa-150">EAC에서 **받는 사람** \> **그룹**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-150">In the EAC, navigate to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="6f4aa-151">다음 중 하나를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-151">Do one of the following:</span></span>
    
  - <span data-ttu-id="6f4aa-152">그룹을 편집 하려면 그룹 목록에서 보거나 변경할 배포 또는 보안 그룹을 클릭 한 다음 편집 아이콘](../media/ITPro-EAC-EditIcon.gif) **편집** ![을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-152">To edit a group: In the list of groups, click the distribution or security group that you want to view or change, and then click **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif).</span></span> <span data-ttu-id="6f4aa-153">필요에 따라 일반 설정을 업데이트하고 그룹 소유자 및 그룹 구성원을 추가하거나 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-153">You can update general settings, add or remove group owners, and add or remove group members, as needed.</span></span>
    
  - <span data-ttu-id="6f4aa-154">그룹을 제거하려면 그룹을 선택하고 **제거**![아이콘 제거](../media/ITPro-EAC-RemoveIcon.gif)를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-154">To remove a group: Select the group and click **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.gif).</span></span>
    
3. <span data-ttu-id="6f4aa-155">변경을 마치면 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-155">When you're finished making your changes, click **Save**.</span></span>
    
## <a name="create-edit-or-remove-a-group-using-remote-windows-powershell"></a><span data-ttu-id="6f4aa-156">원격 Windows PowerShell을 사용하여 그룹 만들기, 편집 또는 제거</span><span class="sxs-lookup"><span data-stu-id="6f4aa-156">Create, edit, or remove a group using remote Windows PowerShell</span></span>

<span data-ttu-id="6f4aa-p115">이 섹션에서는 원격 Windows PowerShell을 사용하여 그룹을 만들고 속성을 변경하는 방법에 대한 정보가 제공됩니다. 또한 기존 그룹을 제거하는 방법도 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p115">This section provides information about creating groups and changing their properties by using remote Windows PowerShell. It also shows how to remove an existing group.</span></span> 
  
 <span data-ttu-id="6f4aa-159">**원격 Windows PowerShell을 사용하여 그룹을 만들려면**</span><span class="sxs-lookup"><span data-stu-id="6f4aa-159">**To create a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="6f4aa-p116">이 예제에서는 [New-EOPDistributionGroup](http://technet.microsoft.com/library/4610dfe5-fca8-4ba8-be3c-535d1753e0f4.aspx) cmdlet을 사용하여 별칭이 itadmin이고 이름이 IT Administrators인 메일 그룹을 만듭니다. 또한 사용자를 그룹의 구성원으로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p116">This example uses the [New-EOPDistributionGroup](http://technet.microsoft.com/library/4610dfe5-fca8-4ba8-be3c-535d1753e0f4.aspx) cmdlet to create a distribution group with an alias of itadmin and the name IT Administrators. It also adds users as members of the group.</span></span> 
  
```Powershell
New-EOPDistributionGroup -Type "Distribution" -Name "IT Administrators" -Alias itadmin -Members @("Member1","Member2","Member3") -ManagedBy "Member1"

```

<span data-ttu-id="6f4aa-162">메일 그룹 대신 보안 그룹을 만들려면  `-Type "Security"`를 대신 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-162">To create a security group instead of a distribution group, specify  `-Type "Security"` instead.</span></span> 
  
<span data-ttu-id="6f4aa-163">IT Administrators 그룹을 성공적으로 만들었는지 확인하려면 [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet을 실행하여 새 그룹에 대한 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-163">To verify that you've successfully created the IT Administrators group, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to display information about the new group:</span></span> 
  
```Powershell
Get-Recipient "IT Administrators" | Format-List

```

<span data-ttu-id="6f4aa-164">그룹의 구성원 목록을 표시하려면 다음과 같이 [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-164">To get a list of members in the group, run the [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) cmdlet as follows:</span></span> 
  
```Powershell
Get-DistributionGroupMember "IT Administrators"

```

<span data-ttu-id="6f4aa-165">모든 그룹의 전체 목록을 표시하려면 다음과 같이 [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-165">To get a full list of all your groups, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows:</span></span> 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup" | FT | more

```

 <span data-ttu-id="6f4aa-166">**원격 Windows PowerShell을 사용하여 그룹의 속성을 변경하려면**</span><span class="sxs-lookup"><span data-stu-id="6f4aa-166">**To change the properties of a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="6f4aa-p117">[Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) 및 [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) cmdlet을 사용하여 그룹의 속성을 보고 변경합니다. EAC 대신 원격 PowerShell을 사용할 때의 한 가지 이점은 여러 그룹의 속성을 변경할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p117">Use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) and [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) cmdlets to view and change properties for groups. An advantage of using remote PowerShell instead of the EAC is the ability to change properties for multiple groups.</span></span> 
  
<span data-ttu-id="6f4aa-169">다음은 원격 Windows PowerShell을 사용하여 그룹 속성을 변경하는 방법의 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-169">Here are some examples of using remote Windows PowerShell to change group properties.</span></span>
  
<span data-ttu-id="6f4aa-170">이 예제에서는 [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) cmdlet을 사용하여 Seattle Employees 그룹의 기본 SMTP 주소(회신 주소라고도 함)를 sea.employees@contoso.com으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-170">This example uses the [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) cmdlet to change the primary SMTP address (also called the reply address) for the Seattle Employees group to sea.employees@contoso.com.</span></span> 
  
```Powershell
Set-EOPDistributionGroup "Seattle Employees" -PrimarysmptAddress "sea.employees@contoso.com"

```

<span data-ttu-id="6f4aa-p118">그룹의 속성을 성공적으로 변경했는지 확인하려면 [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet을 사용하여 변경 내용을 검토합니다. 원격 PowerShell을 사용할 때 얻을 수 있는 한 가지 이점은 여러 그룹의 여러 속성을 볼 수 있다는 것입니다. 기본 SMTP 주소 그룹을 변경한 위의 예에서는 다음 명령을 실행하여 새 값을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p118">To verify that you've successfully changed the properties for a group, use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to verify the changes. One advantage of using remote PowerShell is that you can view multiple properties for multiple groups. In the previous example where the primary SMTP address group was changed, run the following command to verify the new value:</span></span> 
  
```Powershell
Get-Recipient "Seattle Employees" | FL "PrimarySmtpAddress"

```

<span data-ttu-id="6f4aa-p119">이 예제에서는 [Update-EOPDistributionGroupMember](http://technet.microsoft.com/library/a6d4f790-1b94-42f8-af6f-fa79c504d8ec.aspx) cmdlet을 사용하여 Seattle Employees 그룹의 모든 구성원을 업데이트합니다. 모든 구성원은 쉼표로 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-p119">This example uses the [Update-EOPDistributionGroupMember](http://technet.microsoft.com/library/a6d4f790-1b94-42f8-af6f-fa79c504d8ec.aspx) cmdlet to update all the members of the Seattle Employees group. Use a comma to separate all members.</span></span> 
  
```Powershell
Update-EOPDistributionGroupMember -Identity "Seattle Employees" -Members @("Member1","Member2","Member3","Member4","Member5")

```

<span data-ttu-id="6f4aa-176">Seattle Employees 그룹의 모든 구성원 목록을 표시하려면 다음과 같이 [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-176">To get the list of all the members in the group Seattle Employees, use the [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) cmdlet as follows:</span></span> 
  
```Powershell
Get-DistributionGroupMember "Seattle Employees"

```

 <span data-ttu-id="6f4aa-177">**원격 Windows PowerShell을 사용하여 그룹을 제거하려면**</span><span class="sxs-lookup"><span data-stu-id="6f4aa-177">**To remove a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="6f4aa-178">이 예제에서는 [Remove-EOPDistributionGroup](http://technet.microsoft.com/library/a17b1307-3187-40b0-a438-c7b35a34c002.aspx) cmdlet을 사용하여 IT Administrators라는 메일 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-178">This example uses the [Remove-EOPDistributionGroup](http://technet.microsoft.com/library/a17b1307-3187-40b0-a438-c7b35a34c002.aspx) cmdlet to remove a distribution group named IT Administrators.</span></span> 
  
```Powershell
Remove-EOPDistributionGroup -Identity "IT Administrators" 

```

<span data-ttu-id="6f4aa-179">그룹이 제거되었는지 확인하려면 다음과 같이 [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet을 실행하고 그룹(이 경우 "It Administrators")이 삭제되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="6f4aa-179">To verify that the group was removed, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows, and confirm that the group (in this case "It Administrators") was deleted.</span></span> 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup"

```


