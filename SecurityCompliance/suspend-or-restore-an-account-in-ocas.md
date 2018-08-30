---
title: Office 365 Cloud App Security에서 사용자 계정 일시 중단 또는 복원
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'Office 365 클라우드 응용 프로그램 보안을 위해 수행할 수 있는 관리 작업은 일시 중단 또는 사용자 계정을 일시 수 있습니다. '
ms.openlocfilehash: a5c75edefc6ddb87b5676c4253aafe04817f6a1d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533091"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="96b78-103">Office 365 Cloud App Security에서 사용자 계정 일시 중단 또는 복원</span><span class="sxs-lookup"><span data-stu-id="96b78-103">Suspend or restore a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="96b78-104">Office 365 고급 보안 관리 Office 365 클라우드 응용 프로그램 보안 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="96b78-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="96b78-105">평가 * *\>**</span><span class="sxs-lookup"><span data-stu-id="96b78-105">****Evaluation** \>**</span></span>|<span data-ttu-id="96b78-106">계획 * *\>**</span><span class="sxs-lookup"><span data-stu-id="96b78-106">****Planning** \>**</span></span>|<span data-ttu-id="96b78-107">배포 * *\>**</span><span class="sxs-lookup"><span data-stu-id="96b78-107">****Deployment** \>**</span></span>|<span data-ttu-id="96b78-108">사용률 \* \* \*</span><span class="sxs-lookup"><span data-stu-id="96b78-108">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="96b78-109">평가 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b78-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="96b78-110">계획을 시작합니다</span><span class="sxs-lookup"><span data-stu-id="96b78-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="96b78-111">배포를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b78-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="96b78-112">여기는!</span><span class="sxs-lookup"><span data-stu-id="96b78-112">You are here!</span></span>  <br/> [<span data-ttu-id="96b78-113">다음 단계</span><span class="sxs-lookup"><span data-stu-id="96b78-113">Next steps</span></span>](suspend-or-restore-an-account-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="96b78-p101">손상 된 Office 365에 대 한 조직의 사용자 계정 중 하나는 알림을 수신 하는 경우를 가정해 보겠습니다. 또는 사용자 계정을 사용 하 여 잘못 된 것을 알려주는 알림을 받은 경우를 가정해 보겠습니다. Office 365 클라우드 응용 프로그램 보안 사용자 계정을 일시 중단 하 고 나중에 받으면 알림을 확인 한 후 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96b78-p101">Suppose that you receive an alert that one of your organization's user accounts for Office 365 has been compromised. Or, suppose that you've received an alert that indicates something is wrong with a user account. With Office 365 Cloud App Security, you can suspend a user account and later restore it after you have investigated the alerts you receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="96b78-p102">Office 365 클라우드 App 보안은 Office 365 Enterprise e 5에 사용할 수 있습니다. 조직의 다른 Office 365 Enterprise 등록을 사용 하는 경우 Office 365 클라우드 앱 보안 추가 기능으로 구입할 수 있습니다. (전역 관리자는 Office 365 관리 센터에서 선택 **대금 청구** \> **추가 구독**.) 자세한 내용은 참조 [Office 365 플랫폼 서비스 설명: Office 365 보안 &amp; 준수 센터](https://technet.microsoft.com/en-us/library/dn933793.aspx) [구입 또는 비즈니스를 위한 Office 365에 대 한 추가 기능을 편집](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6)하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96b78-p102">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="96b78-120">Office 365 클라우드 응용 프로그램 보안에 사용자 계정을 일시 중단</span><span class="sxs-lookup"><span data-stu-id="96b78-120">To suspend a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="96b78-p103">사용자 계정, 일시 중단 사용자 다시 로그인 되지 않도록 합니다. 해당 사용자 계정에 **로그인 차단 되는**로그인 상태를 설정 하려면 Office 365에서 직접 편집와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b78-p103">When you suspend a user account, you prevent the user from signing in again. It's the same as editing the user account directly in Office 365 to set the Sign-in status to **Sign-in blocked**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="96b78-p104">해당 일시 중단 하 여 또는 로그인 상태를 편집 하 여 Office 365에 로그인 한 사용자를 차단 하는 경우 모든 사용자의 장치 및 클라이언트 ([편집 또는 Office 365에서 사용자를 변경](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview))에 영향을 1 시간 정도 걸릴 수 있다는 유의 합니다. 사용자가 Office 365에 로그인 하는 경우 차단은 Office 365에 필요한 다시 로그인 할 때마다 적용이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96b78-p104">If you block a user from signing in to Office 365, either by suspending them or by editing their sign-in status, be aware that it can take an hour or so to take effect on all of the user's devices and clients ([Edit or change a user in Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)). If the user is signed in to Office 365, the block will take effect whenever Office 365 requires them to sign in again.</span></span> 
  
1. <span data-ttu-id="96b78-p105">[전역 관리자 또는 보안 관리자](permissions-in-the-security-and-compliance-center.md)로 이동 [https://protection.office.com](https://protection.office.com) 작업이 나 교육용 계정을 사용 하 여 로그인 하 고 있습니다. (이렇게 하면 보안 &amp; 준수 센터.)</span><span class="sxs-lookup"><span data-stu-id="96b78-p105">As a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="96b78-127">보안에서 &amp; 준수 센터 **알림** 선택 \> **관리 고급 알림**입니다.</span><span class="sxs-lookup"><span data-stu-id="96b78-127">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="96b78-128">**Office 365 클라우드 응용 프로그램 보안으로 이동**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b78-128">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
    ![보안에서 &amp; 준수 센터 Office 365 클라우드 앱 보안으로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. <span data-ttu-id="96b78-130">화면 위쪽 탐색 모음에서 **경고**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b78-130">In the navigation bar across the top of the screen, choose **Alerts**.</span></span>
    
5. <span data-ttu-id="96b78-131">**경고** 열에는 특정 사용자 계정에 관련 경고를 두번클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b78-131">In the **Alert** column, double-click an alert that pertains to a specific user account.</span></span> 
    
6. <span data-ttu-id="96b78-132">**계정**아래에서 **상태** 열에서 설정을 선택 ![설정 아이콘](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **일시 중단 사용자**입니다.</span><span class="sxs-lookup"><span data-stu-id="96b78-132">Under **Accounts**, in the **Status** column, choose Settings ![settings icon](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **Suspend user**.</span></span>
    
## <a name="to-restore-a-user-account"></a><span data-ttu-id="96b78-133">사용자 계정을 복원 하려면</span><span class="sxs-lookup"><span data-stu-id="96b78-133">To restore a user account</span></span>

<span data-ttu-id="96b78-134">[Office 365에서 사용자를 복원 합니다.](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="96b78-134">See [Restore a user in Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="96b78-135">다음 단계</span><span class="sxs-lookup"><span data-stu-id="96b78-135">Next steps</span></span>

- [<span data-ttu-id="96b78-136">검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행</span><span class="sxs-lookup"><span data-stu-id="96b78-136">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="96b78-137">Office 365 Cloud App Security을 사용하여 앱 사용 권한 관리</span><span class="sxs-lookup"><span data-stu-id="96b78-137">Manage app permissions using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
    
- <span data-ttu-id="96b78-138">[Office 365 클라우드 응용 프로그램 보안에 대 한 사용률 활동](utilization-activities-for-ocas.md) 을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b78-138">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

