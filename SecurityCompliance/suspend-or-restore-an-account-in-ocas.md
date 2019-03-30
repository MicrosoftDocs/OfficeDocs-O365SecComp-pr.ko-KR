---
title: Office 365 Cloud App Security에서 사용자 계정 일시 중단 또는 복원
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/03/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'Office 365 Cloud App Security를 사용 하는 경우 사용자 계정을 일시 중단 하거나 대기 취소 하는 거 버 넌 스 작업을 수행할 수 있습니다. '
ms.openlocfilehash: d162be9d4e5382c6c03c63ae1b30043edbf0295b
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30998871"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="429d4-103">Office 365 Cloud App Security에서 사용자 계정 일시 중단 또는 복원</span><span class="sxs-lookup"><span data-stu-id="429d4-103">Suspend or restore a user account in Office 365 Cloud App Security</span></span>

|<span data-ttu-id="429d4-104">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="429d4-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="429d4-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="429d4-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="429d4-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="429d4-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="429d4-107">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="429d4-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="429d4-108">평가 시작</span><span class="sxs-lookup"><span data-stu-id="429d4-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="429d4-109">계획 시작</span><span class="sxs-lookup"><span data-stu-id="429d4-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="429d4-110">배포 시작</span><span class="sxs-lookup"><span data-stu-id="429d4-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="429d4-111">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="429d4-111">You are here!</span></span>  <br/> [<span data-ttu-id="429d4-112">다음 단계</span><span class="sxs-lookup"><span data-stu-id="429d4-112">Next steps</span></span>](#next-steps)<br/> |
   
<span data-ttu-id="429d4-113">조직의 Office 365에 대 한 사용자 계정 중 하나가 손상 되었음을 알리는 경고가 표시 되는 경우를 가정해 봅니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-113">Suppose that you receive an alert that one of your organization's user accounts for Office 365 has been compromised.</span></span> <span data-ttu-id="429d4-114">또는 사용자 계정에 문제가 있음을 나타내는 경고를 받았다고 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-114">Or, suppose that you've received an alert that indicates something is wrong with a user account.</span></span> <span data-ttu-id="429d4-115">Office 365 Cloud App Security를 사용 하 여 사용자 계정을 일시 중단 하 고 나중에 수신한 알림을 조사한 후에 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-115">With Office 365 Cloud App Security, you can suspend a user account and later restore it after you have investigated the alerts you receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="429d4-116">office 365 Cloud App Security는 office 365 Enterprise E5에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-116">Office 365 Cloud App Security is available in Office 365 Enterprise E5.</span></span> <span data-ttu-id="429d4-117">조직에서 다른 office 365 Enterprise 구독을 사용 하는 경우 office 365 Cloud App Security를 추가 기능으로 구입할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-117">If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on.</span></span> <span data-ttu-id="429d4-118">(전역 관리자 인 경우 Microsoft 365 관리 센터에서 **청구** \> **구독 추가**를 선택 합니다.) 자세한 내용은 [office 365 플랫폼 서비스 설명: office 365 보안 &amp; 및 준수 센터](https://technet.microsoft.com/en-us/library/dn933793.aspx) 및 [비즈니스용 office 365 용 추가 기능 구입 또는 편집](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="429d4-118">(As a global administrator, in the Microsoft 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="429d4-119">Office 365 Cloud App Security에서 사용자 계정을 일시 중단 하려면</span><span class="sxs-lookup"><span data-stu-id="429d4-119">To suspend a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="429d4-120">사용자 계정을 일시 중단 하면 사용자가 다시 로그인 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-120">When you suspend a user account, you prevent the user from signing in again.</span></span> <span data-ttu-id="429d4-121">Office 365에서 직접 사용자 계정을 편집 하 여 로그인 상태를 **로그인 차단**으로 설정 하는 것과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-121">It's the same as editing the user account directly in Office 365 to set the Sign-in status to **Sign-in blocked**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="429d4-122">사용자가 Office 365에 로그인 하지 못하도록 차단 하거나 (또는 로그인 상태를 편집 하 여), 사용자의 모든 장치 및 클라이언트에 적용 되도록 ([office 365에서 사용자 편집 또는 변경](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)), 한 시간 정도 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-122">If you block a user from signing in to Office 365, either by suspending them or by editing their sign-in status, be aware that it can take an hour or so to take effect on all of the user's devices and clients ([Edit or change a user in Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)).</span></span> <span data-ttu-id="429d4-123">사용자가 office 365에 로그인 되어 있으면 office 365에서 다시 로그인 해야 할 때마다 차단이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-123">If the user is signed in to Office 365, the block will take effect whenever Office 365 requires them to sign in again.</span></span> 
  
1. <span data-ttu-id="429d4-124">[전역 관리자 또는 보안 관리자로](permissions-in-the-security-and-compliance-center.md)이동 [https://protection.office.com](https://protection.office.com) 하 여 회사 또는 학교 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-124">As a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account.</span></span> <span data-ttu-id="429d4-125">(보안 &amp; 및 준수 센터로 이동 합니다.)</span><span class="sxs-lookup"><span data-stu-id="429d4-125">(This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="429d4-126">보안 &amp; 및 준수 센터에서 **경고** \> **고급 알림 관리**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-126">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="429d4-127">**Office 365 Cloud App Security로 이동을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-127">Choose **Go to Office 365 Cloud App Security**.</span></span><br><span data-ttu-id="429d4-128">![보안 &amp; 및 준수 센터에서 Office 365 Cloud App Security로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="429d4-128">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br>
  
4. <span data-ttu-id="429d4-129">화면 위쪽의 탐색 모음에서 **경고**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-129">In the navigation bar across the top of the screen, choose **Alerts**.</span></span>
    
5. <span data-ttu-id="429d4-130">**알림** 열에서 특정 사용자 계정과 관련 된 알림을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-130">In the **Alert** column, double-click an alert that pertains to a specific user account.</span></span> 
    
6. <span data-ttu-id="429d4-131">**계정**아래의 **상태** 열 ![에서](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **사용자 일시 중단**설정 아이콘을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="429d4-131">Under **Accounts**, in the **Status** column, choose Settings ![settings icon](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **Suspend user**.</span></span>
    
## <a name="to-restore-a-user-account"></a><span data-ttu-id="429d4-132">사용자 계정을 복원 하려면</span><span class="sxs-lookup"><span data-stu-id="429d4-132">To restore a user account</span></span>

<span data-ttu-id="429d4-133">[Office 365에서 사용자 복원](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1) 참조</span><span class="sxs-lookup"><span data-stu-id="429d4-133">See [Restore a user in Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="429d4-134">다음 단계</span><span class="sxs-lookup"><span data-stu-id="429d4-134">Next steps</span></span>

- [<span data-ttu-id="429d4-135">검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행</span><span class="sxs-lookup"><span data-stu-id="429d4-135">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="429d4-136">Office 365 Cloud App Security를 사용하여 OAuth 앱 관리</span><span class="sxs-lookup"><span data-stu-id="429d4-136">Manage OAuth apps using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
    
- <span data-ttu-id="429d4-137">[Office 365 Cloud App Security에 대 한 사용률 작업](utilization-activities-for-ocas.md) 검토</span><span class="sxs-lookup"><span data-stu-id="429d4-137">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

