---
title: 장치 보안 정책 만들기 및 배포
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/9/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.NewDevicePolicy
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: d310f556-8bfb-497b-9bd7-fe3c36ea2fd6
description: '무단된 액세스 로부터 Office 365에 조직의 정보를 보호 하는 작성 및 도움이 되는 Office 365의 모바일 장치 관리에 대 한 보안 정책 배포 하는 단계입니다. '
ms.openlocfilehash: ab1fc1960a3e55eb3080dde7df0ec742c58b2cc7
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272073"
---
# <a name="create-and-deploy-device-security-policies"></a><span data-ttu-id="824eb-103">장치 보안 정책 만들기 및 배포</span><span class="sxs-lookup"><span data-stu-id="824eb-103">Create and deploy device security policies</span></span>

<span data-ttu-id="824eb-p101">무단된 액세스 로부터 Office 365에 조직의 정보를 보호 하는 데 도움이 되는 보안 정책을 만들 수 Office 365에 대 한 모바일 장치 관리를 사용할 수 있습니다. 여기서 장치의 사용자가 해당 Office 365 라이선스를가지고 하 고 Office 365에 대 한 MDM에서 장치를 등록 하는 조직에서 모든 모바일 장치에 정책을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-p101">You can use Mobile Device Management for Office 365 to create security policies that help protect your organization's information on Office 365 from unauthorized access. You can apply policies to any mobile device in your organization where the user of the device has an applicable Office 365 license and has enrolled the device in MDM for Office 365.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="824eb-106">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="824eb-106">Before you begin</span></span>

- <span data-ttu-id="824eb-p102">장치, 모바일 장치 앱 및 Office 365에 대 한 MDM 지 원하는 보안 설정에 알아봅니다. [Office 365에 대 한 모바일 장치 관리의 기능](capabilities-of-mobile-device-management.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="824eb-p102">Learn about the devices, mobile device apps, and security settings that MDM for Office 365 supports. See [Capabilities of Mobile Device Management for Office 365](capabilities-of-mobile-device-management.md).</span></span>
    
- <span data-ttu-id="824eb-p103">하는 정책을 배포 하려면 Office 365 사용자를 포함 하는 보안 그룹을 만들고 사용자를 위한 Office 365에 대 한 액세스를 차단 되 고에서 제외 하려는 수 있습니다. 새 정책을 조직에 배포 하기 전에 적은 수의 사용자를 배포 하 여 정책을 테스트 하는 것이 좋습니다. 만들 수 있으며 사용자가 직접 또는 하면 정책을 테스트할 수 있는 작은 숫자 Office 365 사용자만 포함 된 보안 그룹을 사용 하 여. 보안 그룹에 대 한 자세한 내용은, [만들기, 편집 또는 보안 그룹 삭제](https://go.microsoft.com/fwlink/p/?LinkId=518555)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="824eb-p103">Create security groups that include Office 365 users that you want to deploy policies to and for users that you might want to exclude from being blocked access to Office 365. We recommend that before you deploy a new policy to your organization, you test the policy by deploying it to a small number of users. You can create and use a security group that includes just yourself or a small number Office 365 users that can test the policy for you. To learn more about security groups, see [Create, edit, or delete a security group](https://go.microsoft.com/fwlink/p/?LinkId=518555).</span></span>
    
- <span data-ttu-id="824eb-p104">**중요:** 모바일 장치 정책을 만들 수 있습니다, 전에 활성화 하 고 Office 365에 대 한 MDM를 설정 해야 합니다. [Office 365에 대 한 모바일 장치 관리의 개요](overview-of-mdm.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="824eb-p104">**Important:** Before you can create a mobile device policy, you must activate and set up MDM for Office 365. See [Overview of Mobile Device Management for Office 365](overview-of-mdm.md).</span></span>
    
- <span data-ttu-id="824eb-115">Office 365 전역 관리자를 만들고 Office 365의 모바일 장치 관리 정책 배포 해야하는 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](https://support.office.com/article/d10608af-7934-490a-818e-e68f17d0e9c1)합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-115">To create and deploy mobile device management policies in Office 365, you need to be an Office 365 global admin. See [Permissions in the Office 365 Security &amp; Compliance Center](https://support.office.com/article/d10608af-7934-490a-818e-e68f17d0e9c1).</span></span>
    
- <span data-ttu-id="824eb-p105">정책을 배포 하기 전에 Office 365에 대 한 MDM에서 장치를 등록의 잠재적 영향을 알고 있는 조직 수 있도록 합니다. 정책 설정 방법에 따라 준수 하지 않는 장치는 Office 365에 액세스 하지 못하도록 차단 될 수 있습니다 및 설치 된 응용 프로그램, 사진 및는 등록 된 장치에 개인 정보를 비롯 하 여 데이터를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-p105">Before you deploy policies, let your organization know the potential impacts of enrolling a device in MDM for Office 365. Depending on how you set up the policies, noncompliant devices can be blocked from accessing Office 365 and data, including installed applications, photos, and personal information on an enrolled device, can be deleted.</span></span>
    
> [!NOTE]
> <span data-ttu-id="824eb-p106">정책 및 액세스 규칙을 Office 365에 대 한 MDM에서 만든 Exchange ActiveSync 모바일 장치 사서함 정책 및 Exchange 관리 센터에서 만든 장치 액세스 규칙을 재정의 합니다. 장치는 Office 365에 대 한 MDM에 등록 되, 후 Exchange ActiveSync 모바일 장치 사서함 정책 또는 장치 액세스 규칙을 모두 장치에 적용 되는 무시 됩니다. Exchange ActiveSync에 대 한 자세한 내용은, [Exchange Online의 Exchange ActiveSync](https://go.microsoft.com/fwlink/p/?LinkId=524380)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="824eb-p106">Policies and access rules created in MDM for Office 365 will override Exchange ActiveSync mobile device mailbox policies and device access rules created in the Exchange admin center. After a device is enrolled in MDM for Office 365, any Exchange ActiveSync mobile device mailbox policy or device access rule applied to the device will be ignored. To learn more about Exchange ActiveSync, see [Exchange ActiveSync in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=524380).</span></span> 
  
## <a name="step-1-create-a-security-policy-and-deploy-to-a-test-group"></a><span data-ttu-id="824eb-121">1 단계: 보안 정책 만들기 및 테스트 그룹에 배포</span><span class="sxs-lookup"><span data-stu-id="824eb-121">Step 1: Create a security policy and deploy to a test group</span></span>

<span data-ttu-id="824eb-p107">시작 하려면 먼저 활성화 하 고 Office 365에 대 한 MDM 설정가 있는지 확인 합니다. 지침에 대 한 [개요 (영문)의 모바일 장치에 대 한 관리 Office 365를](overview-of-mdm.md) 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="824eb-p107">Before you can start, make sure you have activated and set up MDM for Office 365. See [Overview of Mobile Device Management for Office 365](overview-of-mdm.md) for instructions.</span></span> 
  
1. <span data-ttu-id="824eb-124">보안에서 Office 365에서 &amp; 준수 센터, **데이터 손실 방지** 로 이동 \> **장치 보안 정책**입니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-124">In Office 365, in the Security &amp; Compliance Center, go to **Data loss prevention** \> **Device security policies**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="824eb-125">모바일 장치 관리를 활성화 한 후에 **장치 보안 정책** 메뉴에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-125">The **Device security policies** will appear in the menu only after you have activated Mobile device management.</span></span> 
  
2. <span data-ttu-id="824eb-126">**+ 정책 만들기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-126">Choose **+ Create a policy**.</span></span>
    
    ![장치 보안 정책에서 MDN 장치 정책 만들기](media/fbcdbecd-0016-42f1-81a9-9fbad610da90.png)
  
3. <span data-ttu-id="824eb-128">새 정책에 대 한 **이름** 및 **설명을** 지정 하 고 **** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-128">Specify a **Name** and **Description** for the new policy, and then choose **Next**.</span></span>
    
    ![장치 보안 정책에 대 한 이름을 설정 하는](media/d382e845-4a7f-4f72-8a09-813ea4cbd0c4.png)
  
4. <span data-ttu-id="824eb-130">**요구 사항을 장치에 있어야 하 시겠습니까?** 페이지 원하는 모바일 장치에 적용 된 조직 전체에서 요구 사항을 지정 하 고 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-130">On the **What requirements do you want to have on devices?** page, specify the requirements you want applied to mobile devices in your organization, and then choose **Next**.</span></span>
    
    ![장치 보안 정책에 설정 페이지](media/186b3bd5-5e3d-4059-978f-94113111a8ca.png)
  
5. <span data-ttu-id="824eb-132">에 **을 구성 하 시겠습니까?** 페이지 원하는 조직 전체에서 모바일 장치에 적용 된 모든 추가 요구 사항을 지정 하 고 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-132">On the **What do you want to configure?** page, specify any additional requirements you want applied to mobile devices in your organization, and then choose **Next**.</span></span>
    
6. <span data-ttu-id="824eb-133">**이제이 정책을 적용 하 시겠습니까?** 페이지, **예**를 선택 하 고 **+ 추가**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-133">On the **Do you want to apply this policy now?** page, choose **Yes**, and then choose **+ Add**.</span></span> 
    
    ![정책 추가](media/89ab7cab-1b7a-4c78-9aa6-3db7d7667f8e.png)
  
7. <span data-ttu-id="824eb-135">조직에 배포 하 고 **추가**선택 하기 전에 정책을 테스트 하는 사용자 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-135">Select the group(s) who will test the policy before you deploy it to your organization, and then choose **Add**.</span></span>
    
8. <span data-ttu-id="824eb-136">**다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-136">Choose **Next**.</span></span>
    
9. <span data-ttu-id="824eb-137">검토 하 고 새 장치 정책의 세부 정보를 확인 하 고 **이 정책 만들기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-137">Review and confirm the details of the new device policy, and then choose **Create this policy**.</span></span>
    
    ![이 정책을 사용 하는 장치 정책을 만드는 finsih 하려면 만들기를 선택 합니다.](media/e410bcf3-8a36-44ed-9fea-00e742db06fb.png)
  
10. <span data-ttu-id="824eb-139">**닫기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-139">Click **Close**.</span></span>
    
<span data-ttu-id="824eb-p108">정책에 적용 되는 각 사용자가 모바일 장치를 사용 하 여 Office 365에 로그인 할 다음에 해당 장치에 푸시 정책을 갖게 됩니다. 사용자가 하기 전에 모바일 장치에 적용 된 정책 하지 않은 경우, 다음 정책을 배포한 후 이러한 알림을 받게 됩니다 [등록 하 고 Office 365에 대 한 MDM을 활성화 하는 단계](https://go.microsoft.com/fwlink/?LinkId=615272)를 포함 하는 장치에서 합니다. 등록이 완료 될 때까지 전자 메일에 대 한 액세스, OneDrive 및 기타 서비스는 제한 됩니다. Intune 회사 포털 응용 프로그램을 사용 하 여 등록을 완료 한 후 서비스를 사용 하 여 수 및 정책을 장치에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-p108">Each user that the policy applies to will have the policy pushed to their device the next time they sign in to Office 365 using their mobile device. If users haven't had a policy applied to their mobile device before, then after you deploy the policy, they'll get a notification on their device that includes the [steps to enroll and activate MDM for Office 365](https://go.microsoft.com/fwlink/?LinkId=615272). Until they complete enrollment, access to email, OneDrive, and other services will be restricted. After they complete enrollment using the Intune Company Portal app, they'll be able to use the services and the policy will be applied to their device.</span></span>
  
## <a name="step-2-verify-your-policy-works"></a><span data-ttu-id="824eb-144">2 단계: 정책 작동 확인</span><span class="sxs-lookup"><span data-stu-id="824eb-144">Step 2: Verify your policy works</span></span>

<span data-ttu-id="824eb-145">보안 정책을 만든 후에 정책을 조직에 배포 하기 전에 예상 대로 작동 하는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-145">After you've created a security policy, you should check that the policy works as you expect before you deploy it to your organization.</span></span>
  
1. <span data-ttu-id="824eb-146">Office 365에서로 이동 **보안 &amp; 준수 센터** \> **데이터 손실 방지** \> **장치 관리**합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-146">In Office 365, go to **Security &amp; Compliance Center** \> **Data loss prevention** \> **Device management**.</span></span>
    
2. <span data-ttu-id="824eb-p109">**Office 365에 대 한 모바일 장치 관리** 페이지에서 정책이 적용 된 사용자 장치의 상태를 확인 합니다. 필터링 하거나 정렬할 수으로 **모든** 모든 장치, 또는 차단 된 장치를 보려면 **차단 됨** 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-p109">On the **Mobile Device Management for Office 365** page, Check the status of user devices that have the policy applied. You can filter or sort by **All** to view all devices, or **Blocked** to view blocked devices.</span></span> 
    
    ![MDM 하 여 관리 되는 장치 보기](media/5c9fd069-b716-40d8-9b36-f9cfeae2139f.png)
  
3. <span data-ttu-id="824eb-p110">장치에서 전체 또는 선택적 지우기 작업을 수행할 수도 있습니다. 자세한 내용은 [Office 365의 모바일 장치 지우기 시도](wipe-a-mobile-device.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="824eb-p110">You can also do a full or selective wipe on the device. For instructions, see [Wipe a mobile device in Office 365](wipe-a-mobile-device.md).</span></span>
    
## <a name="step-3-deploy-a-policy-to-your-organization"></a><span data-ttu-id="824eb-152">3 단계: 조직에는 정책을 배포합니다</span><span class="sxs-lookup"><span data-stu-id="824eb-152">Step 3: Deploy a policy to your organization</span></span>

<span data-ttu-id="824eb-153">모바일 장치 정책을 만들어 예상 대로 작동 하는지 확인 한 후 조직에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-153">After you've created a mobile device policy and verified that it works as expected, deploy it to your organization.</span></span>
  
1. <span data-ttu-id="824eb-154">Office 365에서로 이동 **보안 &amp; 준수 센터** \> **데이터 손실 방지** \> **장치 보안 정책**입니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-154">In Office 365, go to **Security &amp; Compliance Center** \> **Data loss prevention**\> **Device security policies**.</span></span>
    
2. <span data-ttu-id="824eb-155">배포 하려는 정책을 선택 하 고에서 **정책 편집** 을 선택 된 \< _정책 이름_ \> 패널입니다.  </span><span class="sxs-lookup"><span data-stu-id="824eb-155">Select the policy you want to deploy, and choose **Edit policy** in the \<  _policy name_\> panel.</span></span>
    
3. <span data-ttu-id="824eb-156">**배포** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-156">Select the **Deployment** tab.</span></span> 
    
4. <span data-ttu-id="824eb-157">**배포** 탭에서 **Yes** 위에 **하나를 선택 하려면이 정책을 적용 하려는 사용자를 포함 하는 자세한 보안 그룹 또는** 한 다음 **추가**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-157">In the **Deployment** tab, choose **Yes** above **Select one or more security groups that contain the people you want to apply this policy to** and then **Add**.</span></span>
    
  - <span data-ttu-id="824eb-p111">**그룹 선택** 패널에서 추가할 그룹을 검색할 수 있습니다, 별칭 또는 표시 이름으로 필터링 할 수 있습니다. **그룹** 목록에서 기존 그룹을 추가할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-p111">On the **Select Group** panel, you can search for a group to add, you can filter either by alias or by display name. You can also add an existing group from the **Groups** list.</span></span> 
    
    <span data-ttu-id="824eb-160">여러 그룹에 정책을 적용 하려면를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-160">You can add multiple groups to apply the policy to.</span></span>
    
    <span data-ttu-id="824eb-161">패널의 아래쪽에 **추가** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-161">Choose **Add** on the bottom of the panel.</span></span> 
    
5. <span data-ttu-id="824eb-162">**배포** 탭에서 **저장** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-162">Choose **Save** on the **Deployment** tab.</span></span> 
    
    ![MDM 정책을 조직에 배포 합니다.](media/dc3e7fe5-201a-4e45-abe3-fc93e0b59028.png)
  
<span data-ttu-id="824eb-p112">정책에 적용 되는 각 사용자가 모바일 장치에서 Office 365에 로그인 할 다음에 해당 장치에 푸시 정책을 갖게 됩니다. 사용자가 모바일 장치에 적용 된 정책 하지 않은 경우, 자신이 등록 하 고 Office 365에 대 한 MDM을 활성화 하는 단계와 [해당 장치에 알림이 표시](https://go.microsoft.com/fwlink/?LinkId=615272) 표시 됩니다. 등록을 완료 되기 후 정책이 해당 장치에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-p112">Each user that the policy applies to will have the policy pushed to their device the next time they sign in to Office 365 from their mobile device. If users haven't had a policy applied to their mobile device, they'll [get a notification on their device](https://go.microsoft.com/fwlink/?LinkId=615272) with steps to enroll and activate it for MDM for Office 365. After they've completed the enrollment, the policy will be applied to their device.</span></span> 
  
## <a name="step-4-block-email-access-for-unsupported-devices"></a><span data-ttu-id="824eb-167">4 단계: 지원 하지 않는 장치에 대 한 전자 메일 액세스 차단</span><span class="sxs-lookup"><span data-stu-id="824eb-167">Step 4: Block email access for unsupported devices</span></span>

<span data-ttu-id="824eb-p113">보안을 유지 하려면 조직의 정보를 차단 해야 MDM 하 여 Office 365에 대 한 지원 하지 않는 모바일 장치에 대 한 Office 365 전자 메일에 대 한 응용 프로그램 액세스 합니다. 지원 되는 장치 목록은 [Office 365에 대 한 기본 제공 모바일 장치 관리의 기능](capabilities-of-mobile-device-management.md) 을 참조 하십시오. 이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-p113">To help secure your organization's information, you should block app access to Office 365 email for mobile devices that are not supported by MDM for Office 365. See [Capabilities of built-in Mobile Device Management for Office 365](capabilities-of-mobile-device-management.md) for a list of devices that are supported. To do this:</span></span> 
  
1. <span data-ttu-id="824eb-171">보안으로 이동 &amp; 준수 센터\> **데이터 손실 방지** \> **장치 보안 정책**입니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-171">Go to Security &amp; Compliance Center\> **Data loss prevention**\> **Device security policies**.</span></span>
    
2. <span data-ttu-id="824eb-172">**조직 전체의 장치 액세스 설정 관리를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-172">Select **Manage organization-wide device access settings**.</span></span>
    
    ![규정 준수 센터로 이동 \> 장치 및 장치 액세스의 설정 관리 링크를 클릭 합니다.](media/b9f4da3c-dfa5-4913-8482-42a077cb4f56.png)
  
3. <span data-ttu-id="824eb-174">지원 하지 않는 장치를 차단 하기 위해 **장치 MDM Office 365에서 지원 되지않는 경우 시겠습니까** 에서 허용 하거나 차단할 조직의 전자 메일에 액세스 하는 Exchange 계정을 사용 하 여에서 해당 **블록** 선택 \> **저장**합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-174">To block unsupported devices, choose **Block** under **If a device isn't supported by MDM for Office 365, do you want to allow or block it from using an Exchange account to access your organization's email** \> **Save**.</span></span>
  
## <a name="step-5-choose-security-groups-to-be-excluded-from-conditional-access-checks"></a><span data-ttu-id="824eb-175">5단계: 조건부 액세스 검사에서 제외할 보안 그룹 선택</span><span class="sxs-lookup"><span data-stu-id="824eb-175">Step 5: Choose security groups to be excluded from conditional access checks</span></span>

<span data-ttu-id="824eb-p114">자신의 모바일 장치의 조건부 액세스 검사에서 제외하려는 일부 사용자에 대한 보안 그룹을 하나 이상 만든 경우 보안 그룹을 여기에 추가합니다. 이러한 그룹의 사용자는 지원되는 모바일 장치에 적용할 수 있는 정책 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-p114">If you want to exclude some people from conditional access checks on their mobile devices and you've created one or more security groups for those people, add the security groups here. The people in these groups will not have any policies enforced for their supported mobile devices.</span></span>
  
1. <span data-ttu-id="824eb-178">보안으로 이동 &amp; 준수 센터\> **데이터 손실 방지** \> **장치 보안 정책**입니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-178">Go to Security &amp; Compliance Center\> **Data loss prevention**\> **Device security policies**.</span></span>
    
2. <span data-ttu-id="824eb-179">**조직 전체의 장치 액세스 설정 관리를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-179">Select **Manage organization-wide device access settings**.</span></span>
    
    ![규정 준수 센터로 이동 \> 장치 및 장치 액세스의 설정 관리 링크를 클릭 합니다.](media/b9f4da3c-dfa5-4913-8482-42a077cb4f56.png)
  
3. <span data-ttu-id="824eb-p115">Office 365에 대 한 액세스를 차단 되 고에서 제외 하려는 하는 사용자가 포함 된 보안 그룹을 추가 하려면 **추가** 선택 합니다. 사용자가이 목록에 추가 되었습니다 지원 하지 않는 장치를 사용 하는 경우 Office 365 전자 메일에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-p115">Select **Add** to add the security group that has users that you'd like to exclude from being blocked access to Office 365. When a user has been added to this list, they'll be able to access Office 365 email when using an unsupported device.</span></span> 
    
4. <span data-ttu-id="824eb-183">**그룹을 선택** 패널에서 사용 하 여 사용할 보안 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-183">Select the security group you want to use in the **Select group** panel.</span></span> 
    
5. <span data-ttu-id="824eb-184">이름을 선택한 다음 **추가** 선택 \> **저장**합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-184">Select the name, and then **Add** \> **Save**.</span></span>
    
6. <span data-ttu-id="824eb-185">**조직 전체의 장치 액세스 설정** 패널에서 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-185">On the **Organization-wide device access settings** panel, choose **Save**.</span></span>
  
## <a name="what-is-the-impact-of-security-policies-on-different-device-types"></a><span data-ttu-id="824eb-186">보안 정책이 다른 장치 유형에 미치는 영향</span><span class="sxs-lookup"><span data-stu-id="824eb-186">What is the impact of security policies on different device types?</span></span>

<span data-ttu-id="824eb-p116">사용자 장치에 정책을 적용할 때 각 장치에 미치는 영향은 장치 유형마다 약간씩 다릅니다. 다양한 장치에 정책이 미치는 영향의 예를 보려면 다음 표를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="824eb-p116">When you apply a policy to user devices, the impact on each device varies somewhat between different device types. See the following table for examples of the impact of policies on different devices.</span></span>
  


|<span data-ttu-id="824eb-189">**보안 정책**</span><span class="sxs-lookup"><span data-stu-id="824eb-189">**Security Policy**</span></span>|<span data-ttu-id="824eb-190">**Windows Phone 8.1 +**</span><span class="sxs-lookup"><span data-stu-id="824eb-190">**Windows Phone 8.1+**</span></span>|<span data-ttu-id="824eb-191">**Android 4+**</span><span class="sxs-lookup"><span data-stu-id="824eb-191">**Android 4+**</span></span>|<span data-ttu-id="824eb-192">**삼성 Knox**</span><span class="sxs-lookup"><span data-stu-id="824eb-192">**Samsung Knox**</span></span>|<span data-ttu-id="824eb-193">**IOS 6 +**</span><span class="sxs-lookup"><span data-stu-id="824eb-193">**IOS 6+**</span></span>|<span data-ttu-id="824eb-194">**참고**</span><span class="sxs-lookup"><span data-stu-id="824eb-194">**Notes**</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="824eb-195">암호화된 백업 필요</span><span class="sxs-lookup"><span data-stu-id="824eb-195">Require encrypted backup</span></span>  <br/> |<span data-ttu-id="824eb-196">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-196">✖</span></span>  <br/> |<span data-ttu-id="824eb-197">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-197">✖</span></span>  <br/> |<span data-ttu-id="824eb-198">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-198">✔</span></span>  <br/> |<span data-ttu-id="824eb-199">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-199">✔</span></span>  <br/> |<span data-ttu-id="824eb-200">IOS 암호화 백업이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-200">IOS encrypted backup required.</span></span>  <br/> |
|<span data-ttu-id="824eb-201">클라우드 백업 차단</span><span class="sxs-lookup"><span data-stu-id="824eb-201">Block cloud backup</span></span>  <br/> |<span data-ttu-id="824eb-202">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-202">✖</span></span>  <br/> |<span data-ttu-id="824eb-203">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-203">✔</span></span>  <br/> |<span data-ttu-id="824eb-204">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-204">✔</span></span>  <br/> |<span data-ttu-id="824eb-205">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-205">✔</span></span>  <br/> |<span data-ttu-id="824eb-206">Android에서 Google 백업을 차단(회색으로 표시)하고 iOS에서 클라우드 백업을 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-206">Block Google backup on Android (grayed out), cloud backup on iOS.</span></span>  <br/> |
|<span data-ttu-id="824eb-207">문서 동기화 차단</span><span class="sxs-lookup"><span data-stu-id="824eb-207">Block document synchronization</span></span>  <br/> |<span data-ttu-id="824eb-208">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-208">✖</span></span>  <br/> |<span data-ttu-id="824eb-209">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-209">✖</span></span>  <br/> |<span data-ttu-id="824eb-210">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-210">✖</span></span>  <br/> |<span data-ttu-id="824eb-211">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-211">✔</span></span>  <br/> |<span data-ttu-id="824eb-212">iOS: 클라우드에서 문서를 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-212">iOS: Block documents in the cloud.</span></span>  <br/> |
|<span data-ttu-id="824eb-213">사진 동기화 차단</span><span class="sxs-lookup"><span data-stu-id="824eb-213">Block photo synchronization</span></span>  <br/> |<span data-ttu-id="824eb-214">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-214">✖</span></span>  <br/> |<span data-ttu-id="824eb-215">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-215">✖</span></span>  <br/> |<span data-ttu-id="824eb-216">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-216">✖</span></span>  <br/> |<span data-ttu-id="824eb-217">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-217">✔</span></span>  <br/> |<span data-ttu-id="824eb-218">iOS(기본): 사진 스트림을 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-218">iOS (native): Block Photo Stream.</span></span>  <br/> |
|<span data-ttu-id="824eb-219">화면 캡처 차단</span><span class="sxs-lookup"><span data-stu-id="824eb-219">Block screen capture</span></span>  <br/> |<span data-ttu-id="824eb-220">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-220">✔</span></span>  <br/> |<span data-ttu-id="824eb-221">X</span><span class="sxs-lookup"><span data-stu-id="824eb-221">X</span></span>  <br/> |<span data-ttu-id="824eb-222">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-222">✔</span></span>  <br/> |<span data-ttu-id="824eb-223">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-223">✔</span></span>  <br/> |<span data-ttu-id="824eb-224">시도 시 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-224">Blocked when attempted.</span></span>  <br/> |
|<span data-ttu-id="824eb-225">비디오 회의 차단</span><span class="sxs-lookup"><span data-stu-id="824eb-225">Block video conference</span></span>  <br/> |<span data-ttu-id="824eb-226">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-226">✖</span></span>  <br/> |<span data-ttu-id="824eb-227">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-227">✖</span></span>  <br/> |<span data-ttu-id="824eb-228">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-228">✖</span></span>  <br/> |<span data-ttu-id="824eb-229">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-229">✔</span></span>  <br/> |<span data-ttu-id="824eb-230">FaceTime이 Skype 또는 기타 프로그램이 아닌 iOS에서 차단됩니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-230">FaceTime blocked on iOS, not Skype or others.</span></span>  <br/> |
|<span data-ttu-id="824eb-231">진단 데이터 보내기 차단</span><span class="sxs-lookup"><span data-stu-id="824eb-231">Block sending diagnostic data</span></span>  <br/> |<span data-ttu-id="824eb-232">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-232">✖</span></span>  <br/> |<span data-ttu-id="824eb-233">X</span><span class="sxs-lookup"><span data-stu-id="824eb-233">X</span></span>  <br/> |<span data-ttu-id="824eb-234">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-234">✔</span></span>  <br/> |<span data-ttu-id="824eb-235">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-235">✔</span></span>  <br/> |<span data-ttu-id="824eb-236">Android의 Google 충돌 보고서 전송을 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-236">Block sending Google crash report on Android.</span></span>  <br/> |
|<span data-ttu-id="824eb-237">앱 저장소에 대한 액세스 차단</span><span class="sxs-lookup"><span data-stu-id="824eb-237">Block access to app store</span></span>  <br/> |<span data-ttu-id="824eb-238">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-238">✔</span></span>  <br/> |<span data-ttu-id="824eb-239">X</span><span class="sxs-lookup"><span data-stu-id="824eb-239">X</span></span>  <br/> |<span data-ttu-id="824eb-240">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-240">✔</span></span>  <br/> |<span data-ttu-id="824eb-241">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-241">✔</span></span>  <br/> |<span data-ttu-id="824eb-242">앱 저장소 아이콘이 Android 홈페이지에 없고, Windows에서 사용되지 않도록 설정되고, iOS에 없습니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-242">App store icon missing on Android home page, disabled on Windows, missing on iOS.</span></span>  <br/> |
|<span data-ttu-id="824eb-243">앱 저장소에 대한 암호 필요</span><span class="sxs-lookup"><span data-stu-id="824eb-243">Require password for app store</span></span>  <br/> |<span data-ttu-id="824eb-244">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-244">✖</span></span>  <br/> |<span data-ttu-id="824eb-245">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-245">✖</span></span>  <br/> |<span data-ttu-id="824eb-246">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-246">✖</span></span>  <br/> |<span data-ttu-id="824eb-247">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-247">✔</span></span>  <br/> |<span data-ttu-id="824eb-248">iOS: iTunes를 구입하는 데 암호가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-248">iOS: Password required for iTunes purchases.</span></span>  <br/> |
|<span data-ttu-id="824eb-249">이동식 저장소와의 연결 차단</span><span class="sxs-lookup"><span data-stu-id="824eb-249">Block connection to removable storage</span></span>  <br/> |<span data-ttu-id="824eb-250">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-250">✔</span></span>  <br/> |<span data-ttu-id="824eb-251">X</span><span class="sxs-lookup"><span data-stu-id="824eb-251">X</span></span>  <br/> |<span data-ttu-id="824eb-252">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-252">✔</span></span>  <br/> |<span data-ttu-id="824eb-253">NA</span><span class="sxs-lookup"><span data-stu-id="824eb-253">NA</span></span>  <br/> |<span data-ttu-id="824eb-254">Android: 설정에서 SD 카드는 회색으로 표시됩니다. Windows는 설치된 앱을 사용할 수 없음을 나타내는 알림이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-254">Android: SD card will be grayed out in settings, Windows notifies user, apps installed there are not available</span></span>  <br/> |
|<span data-ttu-id="824eb-255">Bluetooth 연결 차단</span><span class="sxs-lookup"><span data-stu-id="824eb-255">Block Bluetooth connection</span></span>  <br/> |<span data-ttu-id="824eb-256">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-256">✔</span></span>  <br/> |\*\*\*  <br/> |\*\*\*  <br/> |<span data-ttu-id="824eb-257">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-257">✖</span></span>  <br/> |<span data-ttu-id="824eb-p117">\*\*\*Android에서 설정으로 BlueTooth를 비활성화할 수 없습니다 했습니다. 대신,는 사용 하지 않도록 설정 BlueTooth를 필요로 하는 모든 트랜잭션에: 고급 음성 메일, 오디오/비디오 원격 제어, 핸 즈 프리 장치, 헤드셋, 전화번호부 액세스 및 직렬 포트입니다. 둘 중 하나라도 사용 되는 경우 페이지의 맨 아래에 작은 알림 메시지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-p117">\*\*\*We can't disable BlueTooth as a setting on Android. Instead, we disable all the transactions that require BlueTooth: Advanced Audio Distribution, Audio/Video Remote Control, hands-free devices, headset, Phone Book Access, and Serial Port. A small toast message appears at the bottom of the page when any of these are used.</span></span>  <br/> |
   
## <a name="what-happens-when-you-delete-a-policy-or-remove-a-user-from-the-policy"></a><span data-ttu-id="824eb-261">정책을 삭제하거나 정책에서 사용자를 제거하면 어떻게 되나요?</span><span class="sxs-lookup"><span data-stu-id="824eb-261">What happens when you delete a policy or remove a user from the policy?</span></span>

<span data-ttu-id="824eb-p118">정책을 삭제 하거나을 정책에 배포 된 그룹에서 사용자를 제거할 때 정책 설정, Office 365 전자 메일 프로필 및 캐시 된 전자 메일 사용자의 장치에서 제거할 수 있습니다. 각 장치 유형에 대 한 제거 된 기능을 참조 하려면 다음 표를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-p118">When you delete a policy or remove a user from a group to which the policy was deployed to, the policy settings, Office 365 email profile and cached emails may be removed from the user's device. See the following table to see what is removed for the different device types:</span></span>
  
|<span data-ttu-id="824eb-264">**제거되는 항목**</span><span class="sxs-lookup"><span data-stu-id="824eb-264">**What's removed**</span></span>|<span data-ttu-id="824eb-265">**Windows Phone 8.1 +**</span><span class="sxs-lookup"><span data-stu-id="824eb-265">**Windows Phone 8.1+**</span></span>|<span data-ttu-id="824eb-266">**iOS 6 +**</span><span class="sxs-lookup"><span data-stu-id="824eb-266">**iOS 6+**</span></span>|<span data-ttu-id="824eb-267">**Android 4 + (삼성 Knox 포함)**</span><span class="sxs-lookup"><span data-stu-id="824eb-267">**Android 4+ (including Samsung Knox)**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="824eb-268">관리 되는 전자 메일 프로필\*</span><span class="sxs-lookup"><span data-stu-id="824eb-268">Managed email profiles\*</span></span>  <br/> |<span data-ttu-id="824eb-269">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-269">✖</span></span>  <br/> |<span data-ttu-id="824eb-270">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-270">✔</span></span>  <br/> |<span data-ttu-id="824eb-271">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-271">✖</span></span>  <br/> |
|<span data-ttu-id="824eb-272">정책 설정</span><span class="sxs-lookup"><span data-stu-id="824eb-272">Policy settings</span></span>  <br/> |<span data-ttu-id="824eb-273">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-273">✔</span></span>  <br/>           <span data-ttu-id="824eb-274">예외: **장치에서 진단 데이터 전송 차단**</span><span class="sxs-lookup"><span data-stu-id="824eb-274">Except for **Block sending diagnostic data from device.**</span></span> <br/> |<span data-ttu-id="824eb-275">✔</span><span class="sxs-lookup"><span data-stu-id="824eb-275">✔</span></span>  <br/> |<span data-ttu-id="824eb-276">✖</span><span class="sxs-lookup"><span data-stu-id="824eb-276">✖</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="824eb-277">\*정책 옵션으로 배포 된 경우 **전자 메일 프로필 관리 되는** 다음 관리 되는 전자 메일 프로필을 선택 캐시 되 고 전자 메일이 하는 사용자의 장치에서 프로필을 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-277">\*If the policy was deployed with the option **Email profile is managed** selected, then the managed email profile and cached emails in that profile will be deleted from the user's device.</span></span> 
  
<span data-ttu-id="824eb-p119">제거 된 정책에 적용 하는 각 사용자가 모바일 장치를 MDM를 사용 하 여 Office 365에 대 한 확인 다음에 해당 장치에서 제거 하는 정책을 갖게 됩니다. 이러한 사용자의이 장치에 적용 되는 새 정책을 배포 하는 경우 Office 365에 대 한 MDM에 다시 등록 하 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-p119">Each user that the removed policy applied to will have the policy removed from their device the next time their mobile device checks in with MDM for Office 365 . If you deploy a new policy that applies to these users' devices, they'll be prompted to re-enroll in MDM for Office 365.</span></span>
  
<span data-ttu-id="824eb-280">또한 수 있습니다 [를 장치 지우기 시도](wipe-a-mobile-device.md), 하거나 완전히, 또는 선택적으로 닦아내기 장치에서 조직 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="824eb-280">You can also [wipe a device](wipe-a-mobile-device.md), either completely, or selectively wipe organizational information from the device.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="824eb-281">관련 항목</span><span class="sxs-lookup"><span data-stu-id="824eb-281">Related Topics</span></span>

[<span data-ttu-id="824eb-282">Office 365의 모바일 장치 관리 개요</span><span class="sxs-lookup"><span data-stu-id="824eb-282">Overview of Mobile Device Management for Office 365</span></span>](overview-of-mdm.md)
  
[<span data-ttu-id="824eb-283">Office 365의 모바일 장치 관리 기능</span><span class="sxs-lookup"><span data-stu-id="824eb-283">Capabilities of Mobile Device Management for Office 365</span></span>](capabilities-of-mobile-device-management.md)
  

