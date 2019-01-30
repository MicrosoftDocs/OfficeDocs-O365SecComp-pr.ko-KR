---
title: 스팸 전자 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소를 제거
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/01/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
description: 사용자는 계속 해 서 스팸으로 분류 하는 Office 365에서 전자 메일 메시지를 보내는, 모든 자세한 메시지를 보내지 못하도록 차단 됩니다.
ms.openlocfilehash: 6f6f4504a9c79463aadc21f2eaeadcd769e8b151
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614402"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="81251-103">스팸 전자 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소를 제거</span><span class="sxs-lookup"><span data-stu-id="81251-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="81251-p101">사용자는 계속 해 서 스팸으로 분류 하는 Office 365에서 전자 메일 메시지를 보내는, 모든 자세한 메시지를 보내지 못하도록 차단 됩니다. 사용자 잘못 된 아웃 바운드 보낸사람으로 서비스에 나열 하 고 배달 못함 보고서 (NDR) 없다는 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="81251-p101">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages. The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="81251-p102">유효한 보낸사람으로 인식 되지 않은 메시지를 배달할 수 수 없습니다. 이 대 한 가장 일반적인 이유는 스팸 보내는 전자 메일 주소 의심 되는 더이상 사용할 수 조직 외부에 있는 메시지를 보낼 수 있었습니다. 전자 메일 관리자에 게 문의 합니다.  원격 서버 '550 5.1.8 액세스 거부, 잘못 된 아웃 바운드 보낸' 반환</span><span class="sxs-lookup"><span data-stu-id="81251-p102">Your message couldn't be delivered because you weren't recognized as a valid sender. The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send messages outside of your organization. Contact your email admin for assistance.  Remote Server returned '550 5.1.8 Access denied, bad outbound sender'</span></span>

<span data-ttu-id="81251-110">테 넌 트 관리자도 모든 이상의 아웃 바운드 메시지를 보내지 못하도록 사용자를 제한 하는 알림을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="81251-110">The tenant admins will also receive an alert stating that the user has been restricted from sending any more outbound messages.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="81251-111">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="81251-111">What do you need to know before you begin?</span></span>
<span data-ttu-id="81251-112"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="81251-112"></span></span>

<span data-ttu-id="81251-113">예상 완료 시간: 5분</span><span class="sxs-lookup"><span data-stu-id="81251-113">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="81251-p103">이 절차를 수행 하기 전에 사용 권한을 할당 해야 합니다. 필요한 사용 권한을 참조 하십시오 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 항목의 스팸 방지 항목".</span><span class="sxs-lookup"><span data-stu-id="81251-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span>

<span data-ttu-id="81251-p104">원격 PowerShell을 통해 다음 절차를 수행할 수도 있습니다. Get BlockedSenderAddress cmdlet를 사용 하 여 제한 된 사용자 및 제한을 제거 하려면 제거 BlockedSenderAddress의 목록을 가져옵니다. Exchange Online에 연결 하려면 Windows PowerShell을 사용 하는 방법을 알아보려면 [Exchange Online PowerShell 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="81251-p104">The following procedure can also be performed via remote PowerShell. Use the Get-BlockedSenderAddress cmdlet to get the list of restricted users and Remove-BlockedSenderAddress to remove the restriction. To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a><span data-ttu-id="81251-119">차단 된 Office 365 전자 메일 계정에 대 한 제한을 제거합니다</span><span class="sxs-lookup"><span data-stu-id="81251-119">Remove restrictions for a blocked Office 365 email account</span></span>

<span data-ttu-id="81251-p105">Office 365 보안 & 준수 센터 (SCC)에서이 작업을 완료 합니다. 소스 코드 제어에 대 한 자세한 내용은 [Office 365 보안 & 준수 센터로 이동](go-to-the-securitycompliance-center.md) 합니다. 이러한 기능을 수행 하기 위해 **조직 관리** 또는 **보안 관리자** 역할 그룹에 포함 되도록 해야 합니다. SCC 역할 그룹에 대 한 자세한 내용은 [Office 365 보안 & 준수 센터의에서 사용 권한 관리로 이동](permissions-in-the-security-and-compliance-center.md) 합니다.</span><span class="sxs-lookup"><span data-stu-id="81251-p105">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC. You need to be in the **Organization Management** or the **Security Administrator** role group in order to perform these functions. [Go to Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) for more details about SCC role groups.</span></span>

1. <span data-ttu-id="81251-124">Office 365 전역 관리자 권한, Office 365 보안 및 규정 준수 센터에 로그인 한 왼쪽에 있는 목록의 **위협 관리**를 확장 하 고, **검토**, 선택 하 고 다음 **제한 된 사이트를 선택 된 작업이 나 교육용 계정을 사용 하 여 사용자가**합니다.</span><span class="sxs-lookup"><span data-stu-id="81251-124">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="81251-125">보안에서 (이전의 관리 센터) **제한 된 사용자** 페이지로 이동 하려면 &amp; 준수 센터가이 URL을 사용 하 여: gt_[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="81251-125">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="81251-p106">이 페이지에는 조직 외부에 있는 메일을 보내지 못하도록 차단 된 사용자 목록이 포함 됩니다.  **차단 해제**에 제한을 제거 하 고 다음을 클릭 하 고 싶지 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81251-p106">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="81251-128">**예** 하 여 변경 내용을 확인을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="81251-128">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="81251-p107">테 넌 트 관리자 계정을 차단을 해제 수 있는 횟수에 제한이 사용자에 대 한 제한을 초과 되 면 오류 메시지가 나타납니다. 다음은 사용자의 차단을 해제 하는 지원 서비스에 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="81251-p107">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span></br></br> <span data-ttu-id="81251-131">사용자가 차단 하지 전에 1 시간까지 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81251-131">It may take up to 1 hour before the user is unblocked.</span></span>
  
## <a name="third-party-block-lists"></a><span data-ttu-id="81251-132">타사 차단 목록</span><span class="sxs-lookup"><span data-stu-id="81251-132">Third-party block lists</span></span>

<span data-ttu-id="81251-p108">Exchange Online Protection 제 3 자 차단 목록을 사용 하 여 스팸 필터링 (영문) 결정을 내릴 수 있도록 합니다. 스팸 메시지에 나타나는 위한 목록을 차단 하는 사용자, 웹사이트, 도메인 및 IP 주소를 추가할 수 있습니다. Office 365 관리자에 속해 있는 경우 타사 목록 공급자에서 제거 하는 이러한 개체를 가져올 하려고 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="81251-p108">Exchange Online Protection also uses third-party block lists to help make decisions in spam filtering. Users, websites, domains, and IP addresses can be added to block lists just for appearing in a spam message. As the Office 365 admin, you should try to get these objects removed from the third-party list providers if they belong to you.</span></span>

> [!NOTE]
> <span data-ttu-id="81251-p109">Office 365 계정에 메시지를 보낼 수 없는 Office 365 외부 사용자, 외부 수신된 거부 목록에 사용자의 계정 수 있습니다. Office 365 외부 사용자가 [목록 삭제 포털 자가 서비스](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis)를 사용 하 여 자신을 제거 하려면 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81251-p109">If someone outside Office 365 cannot send messages to your Office 365 account, their account may be on the external blocked senders list. Users outside Office 365 can try to remove themselves by using the [self-service delisting portal](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span></span> 

## <a name="for-more-information"></a><span data-ttu-id="81251-138">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="81251-138">For more information</span></span>

[<span data-ttu-id="81251-139">손상 된 전자 메일 계정에 대 한 응답</span><span class="sxs-lookup"><span data-stu-id="81251-139">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="81251-140">아웃바운드 스팸 정책 구성</span><span class="sxs-lookup"><span data-stu-id="81251-140">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="81251-141">아웃 바운드 메시지 용 위험성이 높은 배달 풀</span><span class="sxs-lookup"><span data-stu-id="81251-141">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="81251-142">Office 365 보안 & 준수 센터의 사용 권한</span><span class="sxs-lookup"><span data-stu-id="81251-142">Permissions in the Office 365 Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

  

