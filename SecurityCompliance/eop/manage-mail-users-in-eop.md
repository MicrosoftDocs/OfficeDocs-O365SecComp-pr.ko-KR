---
title: EOP에서 메일 사용자 관리
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: 메일 사용자 정의는 EOP(Exchange Online Protection) 서비스 관리의 중요한 부분입니다.
ms.openlocfilehash: 48d530be17a7e75f6e179a50067b1b9526606cb0
ms.sourcegitcommit: 361aab46b1bb295ed2dcc1a417ac81f699b8ff78
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/30/2019
ms.locfileid: "36676718"
---
# <a name="manage-mail-users-in-eop"></a><span data-ttu-id="b134d-103">EOP에서 메일 사용자 관리</span><span class="sxs-lookup"><span data-stu-id="b134d-103">Manage mail users in EOP</span></span>

<span data-ttu-id="b134d-p101">메일 사용자 정의는 EOP(Exchange Online Protection) 서비스 관리의 중요한 부분입니다. EOP에서는 여러 가지 방식으로 사용자를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-p101">Defining mail users is an important part of managing the Exchange Online Protection (EOP) service. There are several ways that you can manage users in EOP:</span></span>
  
- <span data-ttu-id="b134d-106">디렉터리 동기화를 사용 하 여 메일 사용자 관리: 회사의 온-프레미스 Active Directory 환경에 기존 사용자 계정이 있는 경우 해당 계정을 Azure AD (Active Directory)와 동기화 하 여 계정 복사본을 클라우드에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-106">Use directory synchronization to manage mail users: If your company has existing user accounts in an on-premises Active Directory environment, you can synchronize those accounts to Azure Active Directory (AD), where a copy of the accounts is stored in the cloud.</span></span> <span data-ttu-id="b134d-107">기존 사용자 계정을 Azure Active Directory에 동기화 할 때 EAC (Exchange 관리 센터)의 **받는 사람** 창에서 해당 사용자를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-107">When you synchronize your existing user accounts to Azure Active Directory, you can view those users in the **Recipients** pane of the Exchange admin center (EAC).</span></span> <span data-ttu-id="b134d-108">디렉터리 동기화를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-108">Using directory synchronization is recommended.</span></span> 

- <span data-ttu-id="b134d-109">EAC를 사용하여 메일 사용자 관리: EAC에서 메일 사용자를 직접 추가하고 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-109">Use the EAC to manage mail users: Add and manage mail users directly in the EAC.</span></span> <span data-ttu-id="b134d-110">이 방법이 메일 사용자를 추가하는 가장 쉬운 방법이며 한 번에 한 명의 사용자를 추가하는 데 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-110">This is the easiest way to add mail users and is useful for adding one user at a time.</span></span>

- <span data-ttu-id="b134d-111">원격 Windows PowerShell을 사용하여 메일 사용자 관리: 원격 Windows PowerShell을 실행하여 메일 사용자를 추가하고 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-111">Use remote Windows PowerShell to manage mail users: Add and manage mail users by running remote Windows PowerShell.</span></span> <span data-ttu-id="b134d-112">이 방법은 여러 레코드를 추가하고 스크립트를 만드는 데 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-112">This method is useful for adding multiple records and creating scripts.</span></span>

> [!NOTE]
> <span data-ttu-id="b134d-113">Microsoft 365 관리 센터에서 사용자를 추가할 수 있지만 이러한 사용자는 메일 받는 사람으로 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-113">You can add users in the Microsoft 365 admin center, however these users can't be used as mail recipients.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="b134d-114">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="b134d-114">Before you begin</span></span>

- <span data-ttu-id="b134d-115">Exchange 관리 센터를 열려면 exchange [Online Protection의 exchange 관리 센터](../exchange-admin-center-in-exchange-online-protection-eop.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b134d-115">To open the Exchange admin center, see [Exchange admin center in Exchange Online Protection](../exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="b134d-p105">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인하려면 다음을 참조하세요. [EOP의 기능 사용 권한](feature-permissions-in-eop.md)의 "사용자, 연락처 및 역할 그룹" 항목</span><span class="sxs-lookup"><span data-stu-id="b134d-p105">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in [Feature permissions in EOP](feature-permissions-in-eop.md).</span></span>

- <span data-ttu-id="b134d-118">Exchange Online Protection PowerShell cmdlet을 사용 하 여 메일 사용자를 만들 때 제한이 발생할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-118">Be aware that when creating mail users by using Exchange Online Protection PowerShell cmdlets, you may encounter throttling.</span></span>

- <span data-ttu-id="b134d-119">이 항목의 PowerShell 명령에서는 일괄 처리 방법을 사용 하 여 명령 결과가 표시 되기까지 몇 분 정도 전파 지연을 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-119">The PowerShell commands in this topic use a batch processing method that results in a propagation delay of a few minutes before the results of the commands are visible.</span></span>

- <span data-ttu-id="b134d-120">Windows PowerShell을 사용 하 여 Exchange Online Protection에 연결 하는 방법에 대 한 자세한 내용은 [connect To Exchange Online Protection PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b134d-120">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span></span>

- <span data-ttu-id="b134d-121">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대 한 자세한 내용은 [Exchange Online에서 exchange 관리 센터에 대 한 바로 가기 키](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b134d-121">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="b134d-122">문제가 있습니까?</span><span class="sxs-lookup"><span data-stu-id="b134d-122">Having problems?</span></span> <span data-ttu-id="b134d-123">[Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) 포럼에서 도움을 요청 하세요.</span><span class="sxs-lookup"><span data-stu-id="b134d-123">Ask for help in the [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) forum.</span></span>
  
## <a name="use-directory-synchronization-to-manage-mail-users"></a><span data-ttu-id="b134d-124">디렉터리 동기화를 사용하여 메일 사용자 관리</span><span class="sxs-lookup"><span data-stu-id="b134d-124">Use directory synchronization to manage mail users</span></span>

<span data-ttu-id="b134d-125">이 섹션에서는 디렉터리 동기화를 사용하여 전자 메일 사용자를 관리하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-125">This section provides information about managing email users by using directory synchronization.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b134d-126">디렉터리 동기화를 사용 하 여 받는 사람을 관리 하는 경우에도 Microsoft 365 관리 센터에서 사용자를 추가 및 관리할 수 있지만 온-프레미스 Active Directory와 동기화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-126">If you use directory synchronization to manage your recipients, you can still add and manage users in the Microsoft 365 admin center, but they will not be synchronized with your on-premises Active Directory.</span></span> <span data-ttu-id="b134d-127">디렉터리 동기화는 온-프레미스 Active Directory의 받는 사람만 클라우드로 동기화 하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-127">This is because directory synchronization only syncs recipients from your on-premises Active Directory to the cloud.</span></span> <br/><br/> <span data-ttu-id="b134d-128">디렉터리 동기화는 다음과 같은 기능을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-128">Directory synchronization is recommended for use with the following features:</span></span> <br/><br/><span data-ttu-id="b134d-129">• **Outlook 수신 허용-보낸 사람 및 수신 거부 목록**: 서비스에 동기화 할 때 이러한 목록이 서비스의 스팸 필터링 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-129">• **Outlook safe sender and blocked sender lists**: When synchronized to the service, these lists will take precedence over spam filtering in the service.</span></span> <span data-ttu-id="b134d-130">이를 통해 사용자는 사용자 또는 도메인 기준으로 수신 허용 및 수신 거부 보낸 사람 목록을 자체적으로 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-130">This lets users manage their own safe sender and blocked sender lists on a per-user or per-domain basis.</span></span> <br/><br/><span data-ttu-id="b134d-131">• **Dbeb (디렉터리 기반 Edge 차단)**: dbeb에 대 한 자세한 내용은 [Use Directory Based Edge 차단은 잘못 된 받는 사람에 게 보낸 메시지를 거부](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b134d-131">• **Directory Based Edge Blocking (DBEB)**: For more information about DBEB, see [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span></span> <br/><br/><span data-ttu-id="b134d-132">• **최종 사용자 스팸 격리**: 최종 사용자 스팸 격리에 액세스 하려면 최종 사용자에 게 유효한 Office 365 사용자 ID 및 암호가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-132">• **End user spam quarantine**: In order to access the end user spam quarantine, end users must have a valid Office 365 user ID and password.</span></span> <span data-ttu-id="b134d-133">온-프레미스 사서함을 보호하는 EOP 고객은 유효한 전자 메일 사용자여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-133">EOP customers protecting on-premises mailboxes must be valid email users.</span></span> <br/><br/><span data-ttu-id="b134d-134">• **메일 흐름 규칙**: 디렉터리 동기화를 사용 하는 경우 기존 Active directory 사용자 및 그룹이 클라우드로 자동 업로드 되 고 특정 사용자를 대상으로 하는 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들 수 있습니다. EAC 또는 Exchange Online Protection PowerShell을 통해 그룹을 수동으로 추가 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-134">• **Mail flow rules**: When you use directory synchronization, your existing Active Directory users and groups are automatically uploaded to the cloud, and you can then create mail flow rules (also known as transport rules) that target specific users and/or groups without having to manually add them via the the EAC or Exchange Online Protection PowerShell.</span></span> <span data-ttu-id="b134d-135">[동적 메일 그룹](https://go.microsoft.com/fwlink/?LinkId=507569) 은 디렉터리 동기화를 통해 동기화 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-135">Note that [dynamic distribution groups](https://go.microsoft.com/fwlink/?LinkId=507569) can't be synchronized via directory synchronization.</span></span>
  
<span data-ttu-id="b134d-136">[디렉터리 동기화 준비](https://go.microsoft.com/fwlink/p/?LinkId=308908)의 설명에 따라 필요한 사용 권한을 얻고 디렉터리 동기화를 준비합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-136">Get the necessary permissions and prepare for directory synchronization, as described in [Prepare for directory synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308908).</span></span>
  
### <a name="to-synchronize-user-directories-with-azure-active-directory-connect-aad-connect"></a><span data-ttu-id="b134d-137">사용자 디렉터리를 Azure Active Directory Connect (AAD 연결)와 동기화 하려면</span><span class="sxs-lookup"><span data-stu-id="b134d-137">To synchronize user directories with Azure Active Directory Connect (AAD Connect)</span></span>

<span data-ttu-id="b134d-138">사용자를 Azure Active Directory (AAD)로 동기화 하려면 먼저 [디렉터리 동기화 활성화](https://go.microsoft.com/fwlink/p/?LinkId=308909)에 설명 된 대로 **디렉터리 동기화를 활성화**해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-138">To synchronize users to Azure Active Directory (AAD) you first have to **activate directory synchronization**, as described in [Activate directory synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308909).</span></span>

<span data-ttu-id="b134d-139">다음은 AAD 연결을 실행 하는 온-프레미스 컴퓨터를 설치 및 구성 하는 것입니다 (아직 한 번 확인 해야 할 사항이 없는 경우).</span><span class="sxs-lookup"><span data-stu-id="b134d-139">Next is the installation and configuration of an on-premises computer to run AAD Connect (if you don't already have one -- something worth checking ahead of time).</span></span> <span data-ttu-id="b134d-140">[Aad 연결 설정에 대 한 빠른 방법](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express) 항목에는 aad connect를 사용 하 여 온-프레미스에서 Azure AD로 계정을 설정 하 고 동기화 하는 방법에 대 한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-140">The [Setting up AAD Connect, the express way](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express) topic tells you how to setup and synchronize your accounts from on-premises to Azure AD with AAD Connect.</span></span>

<span data-ttu-id="b134d-141">그러나이 작업을 수행 하기 전에 [필수 구성 요소를 충족](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites)하는지 확인 하 고 [설치 유형을 선택](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-select-installation)합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-141">But before you do that work, make certain [you meet prerequisites](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites), and [choose your installation type](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-select-installation).</span></span> <span data-ttu-id="b134d-142">위의 링크는 빠른 설치를 위한 짧은 문서에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-142">The earlier link is to a short article for express installs.</span></span> <span data-ttu-id="b134d-143">또한 [사용자 지정 설치](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-custom)또는 필요한 경우 [통과 인증](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-pta-quick-start) 에 대 한 문서를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-143">You can also find articles on [custom installations](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-custom), or [pass-through authentication](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-pta-quick-start) if they're needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b134d-p114">Azure Active Directory 동기화 도구 구성 마법사를 완료하면 Active Directory 포리스트에 **MSOL_AD_SYNC** 계정이 만들어집니다. 이 계정을 사용하여 온-프레미스 Active Directory 정보를 읽고 동기화합니다. 디렉터리 동기화가 정상적으로 작동하도록 하려면 로컬 디렉터리 동기화 서버의 TCP 443이 열려 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-p114">When you finish the Azure Active Directory Sync Tool Configuration Wizard, the **MSOL_AD_SYNC** account is created in your Active Directory forest. This account is used to read and synchronize your on-premises Active Directory information. In order for directory synchronization to work correctly, make sure that TCP 443 on your local directory synchronization server is open.</span></span>

<span data-ttu-id="b134d-147">동기화를 구성한 후에는 EOP가 올바르게 동기화 되는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-147">After configuring your sync, be sure to verify that EOP is synchronizing correctly.</span></span> <span data-ttu-id="b134d-148">이렇게 하려면 EAC에서 **받는 사람** \> **연락처**로 이동한 다음 온-프레미스 환경에서 사용자 목록이 올바르게 동기화되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-148">In the EAC, go to **Recipients** \> **Contacts** and view that the list of users was correctly synchronized from your on-premises environment.</span></span>

## <a name="use-the-eac-to-manage-mail-users"></a><span data-ttu-id="b134d-149">EAC를 사용하여 메일 사용자 관리</span><span class="sxs-lookup"><span data-stu-id="b134d-149">Use the EAC to manage mail users</span></span>

<span data-ttu-id="b134d-150">이 섹션에서는 전자 메일 사용자를 EAC에서 직접 추가 및 관리하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-150">This section provides information about adding and managing email users directly in the EAC.</span></span>
  
### <a name="use-the-eac-to-add-a-mail-user"></a><span data-ttu-id="b134d-151">EAC를 사용 하 여 메일 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="b134d-151">Use the EAC to add a mail user</span></span>

1. <span data-ttu-id="b134d-152">EAC에서 **받는 사람** \> **연락처**로 이동한 다음 **새로 만들기 +** 를 클릭하여 전자 메일 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-152">Create an email user by going to go to **Recipients** \> **Contacts** in the EAC, and then clicking **New +**.</span></span>

2. <span data-ttu-id="b134d-153">**새 메일 사용자** 페이지에서 다음을 비롯한 사용자의 정보를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-153">On the **New mail user** page, enter the user's information, including the following:</span></span> 

   ****

   |<span data-ttu-id="b134d-154">**메일 사용자 속성**</span><span class="sxs-lookup"><span data-stu-id="b134d-154">**Mail user property**</span></span>|<span data-ttu-id="b134d-155">**설명**</span><span class="sxs-lookup"><span data-stu-id="b134d-155">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="b134d-156">**이름**, **이니셜**, **성**</span><span class="sxs-lookup"><span data-stu-id="b134d-156">**First name**, **Initials**, and **Last name**</span></span>|<span data-ttu-id="b134d-157">해당 상자에 사용자의 전체 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-157">Type the user's full name in the appropriate boxes.</span></span>|
   |<span data-ttu-id="b134d-158">**표시 이름**</span><span class="sxs-lookup"><span data-stu-id="b134d-158">**Display name**</span></span>|<span data-ttu-id="b134d-p116">이름을 64자까지 입력합니다. 기본적으로 이 상자에는 **이름**, **이니셜** 및 **성** 상자의 이름(있는 경우)이 표시됩니다. 표시 이름은 필수 입력 필드입니다.  </span><span class="sxs-lookup"><span data-stu-id="b134d-p116">Type a name, using up to 64 characters. By default, this box shows the names in the **First name**, **Initials**, and **Last name** boxes if any. The display name is required.</span></span>|
   |<span data-ttu-id="b134d-162">**별칭**</span><span class="sxs-lookup"><span data-stu-id="b134d-162">**Alias**</span></span>|<span data-ttu-id="b134d-p117">사용자의 고유한 별칭을 64자까지 입력합니다. 별칭은 필수 입력 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-p117">Type a unique alias, using up to 64 characters, for the user. The alias is required.</span></span>|
   |<span data-ttu-id="b134d-165">**외부 전자 메일 주소**</span><span class="sxs-lookup"><span data-stu-id="b134d-165">**External email address**</span></span>|<span data-ttu-id="b134d-166">사용자의 외부 전자 메일 주소를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-166">Type the external email address of the user.</span></span>|
   |<span data-ttu-id="b134d-167">**사용자 ID**</span><span class="sxs-lookup"><span data-stu-id="b134d-167">**User id**</span></span>|<span data-ttu-id="b134d-p118">사용자가 서비스에 로그인하는 데 사용할 이름을 입력합니다. 사용자 로그인 이름은 @ 기호 왼쪽의 사용자 이름과 오른쪽의 접미사로 구성됩니다. 일반적으로 접미사는 사용자 계정이 있는 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-p118">Type the name that the mail user will use to sign in to the service. The user sign-in name consists of a user name on the left side of the at (@) symbol and a suffix on the right side. Typically, the suffix is the domain name in which the user account resides.</span></span>|
   |<span data-ttu-id="b134d-171">**새 암호**</span><span class="sxs-lookup"><span data-stu-id="b134d-171">**New password**</span></span>|<span data-ttu-id="b134d-p119">사용자가 서비스에 로그인하는 데 사용할 암호를 입력합니다. 제공하는 암호는 사용자 계정을 만들 도메인의 암호 길이, 복잡성 및 내역 요구 사항을 준수해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-p119">Type the password that the mail user will use to sign in to the service. Make sure that the password you supply complies with the password length, complexity, and history requirements of the domain in which you're creating the user account.</span></span>|
   |<span data-ttu-id="b134d-174">**암호 확인**</span><span class="sxs-lookup"><span data-stu-id="b134d-174">**Confirm password**</span></span>|<span data-ttu-id="b134d-175">암호를 다시 입력하여 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-175">Retype the password to confirm it.</span></span>|

3. <span data-ttu-id="b134d-p120">**저장**을 클릭하여 새 전자 메일 사용자를 만듭니다. 그러면 새 사용자가 사용자 목록에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-p120">Click **Save** to create the new email user. The new user should appear in the list of users.</span></span>

### <a name="use-the-eac-to-edit-or-remove-a-mail-user"></a><span data-ttu-id="b134d-178">EAC를 사용 하 여 메일 사용자 편집 또는 제거</span><span class="sxs-lookup"><span data-stu-id="b134d-178">Use the EAC to edit or remove a mail user</span></span>

- <span data-ttu-id="b134d-179">EAC에서 **받는 사람** \> **연락처**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-179">In the EAC, go to **Recipients** \> **Contacts**.</span></span> <span data-ttu-id="b134d-180">사용자 목록에서 보거나 변경 하려는 사용자를 클릭 한 다음 편집 아이콘](../media/ITPro-EAC-EditIcon.gif) **편집** ![을 선택 하 여 사용자 설정을 필요에 따라 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-180">In the list of users, click the user that you want to view or change, and then select **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif) to update the user settings as needed.</span></span> <span data-ttu-id="b134d-181">사용자 이름, 별칭 또는 연락처 정보를 변경할 수 있으며 조직에서 사용자의 역할에 대한 상세 정보를 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-181">You can change the user's name, alias, or contact information, and you can record detailed information about the user's role in the organization.</span></span> <span data-ttu-id="b134d-182">사용자를 선택한 다음 제거 아이콘](../media/ITPro-EAC-RemoveIcon.gif) **제거** ![를 선택 하 여 삭제를 삭제할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-182">You can also select a user and then choose **Remove** ![Remove icon](../media/ITPro-EAC-RemoveIcon.gif) to delete it.</span></span> 

## <a name="use-exchange-online-protection-powershell-to-manage-mail-users"></a><span data-ttu-id="b134d-183">Exchange Online Protection PowerShell을 사용 하 여 메일 사용자 관리</span><span class="sxs-lookup"><span data-stu-id="b134d-183">Use Exchange Online Protection PowerShell to manage mail users</span></span>

<span data-ttu-id="b134d-184">이 섹션에서는 원격 Windows PowerShell을 사용하여 메일 사용자를 추가하고 관리하는 방법에 대한 정보가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-184">This section provides information about adding and managing mail users by using remote Windows PowerShell.</span></span>
  
### <a name="use-eop-powershell-to-add-a-mail-user"></a><span data-ttu-id="b134d-185">EOP PowerShell을 사용 하 여 메일 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="b134d-185">Use EOP PowerShell to add a mail user</span></span>
  
<span data-ttu-id="b134d-186">이 예제에서는 다음 세부 정보를 사용하여 [New-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/new-eopmailuser) cmdlet을 통해 EOP에서 Jeffrey Zeng에 대한 메일 사용이 가능한 사용자 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-186">This example uses the [New-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/new-eopmailuser) cmdlet to create a mail-enabled user account for Jeffrey Zeng in EOP with the following details:</span></span>
  
- <span data-ttu-id="b134d-187">이름은 Jeffrey고 성은 Zeng입니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-187">The first name is Jeffrey and the last name is Zeng.</span></span>

- <span data-ttu-id="b134d-188">이름은 Jeffrey이고 표시 이름은 Jeffrey Zeng입니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-188">The name is Jeffrey and the display name is Jeffrey Zeng.</span></span>

- <span data-ttu-id="b134d-189">별칭은 jeffreyz입니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-189">The alias is jeffreyz.</span></span>

- <span data-ttu-id="b134d-190">외부 전자 메일 주소는 jzeng@tailspintoys.com입니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-190">The external email address is jzeng@tailspintoys.com.</span></span>

- <span data-ttu-id="b134d-191">Office 365 로그인 이름은 jeffreyz@contoso.onmicrosoft.com입니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-191">The Office 365 sign in name is jeffreyz@contoso.onmicrosoft.com.</span></span>

- <span data-ttu-id="b134d-192">암호는 Pa$$word1입니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-192">The password is Pa$$word1.</span></span>

```Powershell
New-EOPMailUser -LastName Zeng -FirstName Jeffrey -DisplayName "Jeffrey Zeng" -Name Jeffrey -Alias jeffreyz -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -ExternalEmailAddress jeffreyz@tailspintoys.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force)
```

<span data-ttu-id="b134d-193">이 작업이 제대로 수행 되었는지 확인 하려면 다음 명령을 실행 하 여 새 메일 사용자 Jeffrey Zeng에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-193">To verify that this worked, run the following command to display information about new mail user Jeffrey Zeng:</span></span>
  
```Powershell
Get-User -Identity "Jeffrey Zeng"
```

<span data-ttu-id="b134d-194">구문 및 매개 변수에 대 한 자세한 내용은 [get-help](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-user)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b134d-194">For detailed syntax and parameter information, see [Get-User](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-user).</span></span>

### <a name="use-eop-powershell-to-edit-the-properties-of-a-mail-user"></a><span data-ttu-id="b134d-195">EOP PowerShell을 사용 하 여 메일 사용자의 속성 편집</span><span class="sxs-lookup"><span data-stu-id="b134d-195">Use EOP PowerShell to edit the properties of a mail user</span></span>
  
<span data-ttu-id="b134d-196">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) 및 [Set-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/set-eopmailuser) cmdlet을 사용하여 메일 사용자의 속성을 보거나 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-196">Use the [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) and [Set-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/set-eopmailuser) cmdlets to view or change properties for mail users.</span></span>
  
<span data-ttu-id="b134d-197">다음 예에서는 Pilar Pinilla의 외부 전자 메일 주소를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-197">This example sets the external email address for Pilar Pinilla.</span></span>
  
```Powershell
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

<span data-ttu-id="b134d-198">다음 예에서는 모든 메일 사용자의 Company 속성을 Contoso로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-198">This example sets the Company property for all mail users to Contoso.</span></span>
  
```Powershell
$Recip = Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')}
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}
```
  
<span data-ttu-id="b134d-199">이 작업이 제대로 수행 되었는지 확인 하려면 [받는 사람](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) cmdlet을 사용 하 여 변경 내용을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-199">To verify that this worked, use the [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) cmdlet to verify the changes.</span></span> <span data-ttu-id="b134d-200">여러 메일 연락처의 여러 속성을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-200">(Note that you can view multiple properties for multiple mail contacts.)</span></span>
  
```Powershell
Get-Recipient -Identity "Pilar Pinilla" | Format-List
```

<span data-ttu-id="b134d-201">모든 메일 사용자에 대한 Company 속성이 Contoso로 설정된 이전 예제에서 변경 사항을 확인하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-201">In the previous example where the Company property was set to Contoso for all mail users, run the following command to verify the changes:</span></span>
  
```Powershell
Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')} | Format-List Name,Company
```

> [!IMPORTANT]
> <span data-ttu-id="b134d-202">이 cmdlet은 일괄 처리 방법을 사용하므로 cmdlet 결과가 보이기 몇 분 전에 전파 지연이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-202">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span>
  
### <a name="use-eop-powershell-to-remove-a-mail-user"></a><span data-ttu-id="b134d-203">EOP PowerShell을 사용 하 여 메일 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="b134d-203">Use EOP PowerShell to remove a mail user</span></span>
  
<span data-ttu-id="b134d-204">이 예제에서는 [Remove-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient/remove-eopmailuser) cmdlet을 사용하여 사용자 Jeffrey Zeng을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-204">This example uses the [Remove-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient/remove-eopmailuser) cmdlet to delete user Jeffrey Zeng:</span></span>
  
```Powershell
Remove-EOPMailUser -Identity Jeffrey
```

 <span data-ttu-id="b134d-205">**결과에 문제가 없는지 확인하려면**</span><span class="sxs-lookup"><span data-stu-id="b134d-205">**To verify that this worked**</span></span>
  
<span data-ttu-id="b134d-206">이 작업이 제대로 수행 되었는지 확인 하려면 [받는 사람](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) cmdlet을 실행 하 여 메일 사용자가 더 이상 존재 하지 않는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b134d-206">To verify that this worked, run the [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) cmdlet to verify that the mail user no longer exists.</span></span>
  
```Powershell
Get-Recipient Jeffrey | Format-List
```
