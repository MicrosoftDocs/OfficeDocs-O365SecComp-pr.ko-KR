---
title: 스팸 메일을 보낸 후 제한된 사용자 포털에서 사용자 제거
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 03/12/2019
audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: 사용자가 스팸으로 분류 된 Office 365에서 전자 메일을 계속 보내면 더 이상 메시지를 보낼 수 없게 됩니다.
ms.openlocfilehash: 7a44ff7f2bcf88f2132ee4c372cc11b9657dd16a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157250"
---
# <a name="removing-a-user-from-the-restricted-users-portal-after-sending-spam-email"></a><span data-ttu-id="d14c7-103">스팸 메일을 보낸 후 제한된 사용자 포털에서 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="d14c7-103">Removing a user from the Restricted Users portal after sending spam email</span></span>

<span data-ttu-id="d14c7-104">사용자가 스팸으로 분류 된 Office 365에서 전자 메일을 계속 보내는 경우 아웃 바운드 메시지를 더 이상 보낼 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-104">If a user continuously sends emails from Office 365 that are classified as spam, they will be restricted from sending any more messages outbound.</span></span> <span data-ttu-id="d14c7-105">사용자는 잘못 된 아웃 바운드 보낸 사람으로 서비스에 나열 되며 다음과 같은 경우 배달 못 함 보고서 (NDR)를 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-105">The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="d14c7-106">유효한 보낸 사람으로 인식 되지 않아 메시지를 배달할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-106">Your message couldn't be delivered because you weren't recognized as a valid sender.</span></span> <span data-ttu-id="d14c7-107">가장 일반적인 이유는 전자 메일 주소가 스팸을 보낼 때 의심 되며, 더 이상 조직 외부에서 메시지를 보낼 수 없게 되기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-107">The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send messages outside of your organization.</span></span> <span data-ttu-id="d14c7-108">도움이 필요 하면 전자 메일 관리자에 게 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="d14c7-108">Contact your email admin for assistance.</span></span> <span data-ttu-id="d14c7-109">원격 서버에서 ' 550 5.1.8 액세스 거부, 잘못 된 아웃 바운드 보낸 사람 '을 반환 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-109">Remote Server returned '550 5.1.8 Access denied, bad outbound sender'</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="d14c7-110">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="d14c7-110">What do you need to know before you begin?</span></span>
<span data-ttu-id="d14c7-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="d14c7-111"></span></span>

<span data-ttu-id="d14c7-112">예상 완료 시간: 5분</span><span class="sxs-lookup"><span data-stu-id="d14c7-112">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="d14c7-113">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-113">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="d14c7-114">필요한 사용 권한을 확인 하려면 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 에서 "스팸 방지 항목" 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d14c7-114">To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span>

<span data-ttu-id="d14c7-115">또한 원격 PowerShell을 통해 다음 절차를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-115">The following procedure can also be performed via remote PowerShell.</span></span> <span data-ttu-id="d14c7-116">BlockedSenderAddress cmdlet을 사용 하 여 제한 된 사용자 목록을 가져오고, BlockedSenderAddress를 제거 하 여 제한을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-116">Use the Get-BlockedSenderAddress cmdlet to get the list of restricted users and Remove-BlockedSenderAddress to remove the restriction.</span></span> <span data-ttu-id="d14c7-117">Windows PowerShell을 사용하여 Exchange Online에 연결하는 방법에 대한 자세한 내용은 [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d14c7-117">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a><span data-ttu-id="d14c7-118">차단 된 Office 365 전자 메일 계정에 대 한 제한 제거</span><span class="sxs-lookup"><span data-stu-id="d14c7-118">Remove restrictions for a blocked Office 365 email account</span></span>

<span data-ttu-id="d14c7-119">SCC (Security & 준수 센터)에서이 작업을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-119">You complete this task in the Security & Compliance Center (SCC).</span></span> <span data-ttu-id="d14c7-120">SCC에 대 한 자세한 내용은 [Security _AMP_ 준수 센터를](go-to-the-securitycompliance-center.md) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d14c7-120">[Go to the Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span> <span data-ttu-id="d14c7-121">이러한 기능을 수행 하려면 **조직 관리** 또는 **보안 관리자** 역할 그룹에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-121">You need to be in the **Organization Management** or the **Security Administrator** role group in order to perform these functions.</span></span> <span data-ttu-id="d14c7-122">SCC 역할 그룹에 대 한 자세한 내용은 [Security _AMP_ 준수 센터의 사용 권한으로 이동](permissions-in-the-security-and-compliance-center.md) 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d14c7-122">[Go to Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) for more details about SCC role groups.</span></span>

1. <span data-ttu-id="d14c7-123">Office 365 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 여 Office 365 보안 및 준수 센터에 로그인 하 고 왼쪽에 있는 목록에서 **위협 관리**를 확장 한 다음 **검토**를 선택 하 고 제한 됨을 선택 합니다. \*\* 사용자\*\*입니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-123">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="d14c7-124">보안 &amp; 및 준수 센터에서 **제한 된 사용자** 페이지 (이전에는 알림 센터로 알려짐)로 바로 이동 하려면 다음 URL을 사용 합니다. >[https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="d14c7-124">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="d14c7-125">이 페이지에는 조직 외부로 메일을 보낼 수 없도록 차단 된 사용자 목록이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-125">This page will contain the list of users that have been blocked from sending mail to outside of your organization.</span></span>  <span data-ttu-id="d14c7-126">제한을 제거할 사용자를 찾은 다음 **차단을 해제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-126">Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="d14c7-127">플라이 아웃은 송신이 제한 된 계정에 대 한 세부 정보로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-127">A fly-out will go into the details about the account whose sending is restricted.</span></span> <span data-ttu-id="d14c7-128">이 권장 사항을 확인 하 여 계정이 실제로 손상 되는 경우 적절 한 조치를 취해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-128">You should go through the recommendations to ensure you're taking the proper actions in case the account is actually compromised.</span></span> <span data-ttu-id="d14c7-129">완료 되 면 **다음** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-129">Click **Next** when done.</span></span>

4. <span data-ttu-id="d14c7-130">다음 화면에서는 나중에 손상을 방지 하기 위한 권장 사항을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-130">The next screen has recommendations to help prevent future compromise.</span></span> <span data-ttu-id="d14c7-131">MFA (multi-factor authentication)를 사용 하도록 설정 하 고 암호를 변경 하는 것이 적절 한 방어 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-131">Enabling multi-factor authentication (MFA) and changing the passwords are a good defense.</span></span> <span data-ttu-id="d14c7-132">완료 시 **사용자 차단 해제** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-132">Click **Unblock user** when done.</span></span>

5. <span data-ttu-id="d14c7-133">**예** 를 클릭 하 여 변경 내용을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-133">Click **Yes** to confirm the change.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d14c7-134">제한이 제거 될 때까지 최대 30 분이 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-134">It may take up to 30 minutes before restrictions are removed.</span></span> 

## <a name="making-sure-admins-are-alerted-when-this-happens"></a><span data-ttu-id="d14c7-135">이 경우 관리자에 게 경고 합니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-135">Making sure admins are alerted when this happens</span></span>

<span data-ttu-id="d14c7-136">또한 테 넌 트 관리자는 사용자가 더 이상 아웃 바운드 메시지를 보내지 못하도록 제한 되었다는 경고도 수신 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-136">The tenant admins will also receive an alert stating that the user has been restricted from sending any more outbound messages.</span></span> <span data-ttu-id="d14c7-137">이 알림은 모든 테 넌 트에 대해 제공 되며, "전자 메일을 보내는 사용자 제한" 이라는 SCC 경고 정책 페이지에 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d14c7-137">It is a default alert that is provided for all tenants and is listed in the SCC Alert policies page, titled "User restricted from sending email".</span></span> <span data-ttu-id="d14c7-138">경고에 대 한 자세한 내용은 [Security _AMP_ 준수 센터의 경고 정책](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies) 으로 이동 하세요.</span><span class="sxs-lookup"><span data-stu-id="d14c7-138">Go to [Alert policies in the Security & Compliance Center](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies) for more information on the alert.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="d14c7-139">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="d14c7-139">For more information</span></span>

[<span data-ttu-id="d14c7-140">손상 된 전자 메일 계정에 응답</span><span class="sxs-lookup"><span data-stu-id="d14c7-140">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="d14c7-141">전자 메일 알림을 보내는 것이 제한 된 사용자 이해</span><span class="sxs-lookup"><span data-stu-id="d14c7-141">Understanding the User restricted from sending email alert</span></span>](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)

[<span data-ttu-id="d14c7-142">아웃 바운드 메시지에 대 한 위험성이 높은 배달 풀</span><span class="sxs-lookup"><span data-stu-id="d14c7-142">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="d14c7-143">보안 및 준수 센터의 사용 권한</span><span class="sxs-lookup"><span data-stu-id="d14c7-143">Permissions in the Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
