---
title: 조직에 대한 감독 정책 구성
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 5/12/2017
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: 검토를 위해 직원 통신 캡처 감독 검토 정책을 설정 합니다.
ms.openlocfilehash: a919d65f5c0967a44ac12b7e02d477dac2113704
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534175"
---
# <a name="configure-supervision-policies-for-your-organization"></a><span data-ttu-id="bd517-103">조직에 대한 감독 정책 구성</span><span class="sxs-lookup"><span data-stu-id="bd517-103">Configure supervision policies for your organization</span></span>

<span data-ttu-id="bd517-104">감독 정책을 사용 하 여 내부 또는 외부 검토자가 검사에 대 한 직원 통신을 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-104">Use supervision policies to capture employee communications for examination by internal or external reviewers.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bd517-p101">감독 정책을 사용 하 여 조직에 대 한 Office 365 e 5를 구독을 해야 합니다. 해당 요금제에 가입한 상태 감독 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p101">Using supervision policies requires an Office 365 E5 subscription for your organization. If you don't have that plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="bd517-107">설정 하 고 감독을 사용 하 여 Office 365 조직에서 다음이 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-107">Follow these steps to set up and use supervision in your Office 365 organization:</span></span> 
  
- [<span data-ttu-id="bd517-108">감독에 대 한 그룹을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-108">Set up groups for Supervision</span></span>](configure-supervision-policies.md#exampledist)
    
    <span data-ttu-id="bd517-p102">감독 사용을 시작 하기 전에 사용자가 자신의 통신을 검토 하 고 이러한 검토를 수행 하는 사용자를 결정 합니다. 감독 작동 하는 방법을 보려면 소수의 사용자가 시작 하려는 경우에 지금에 대 한 그룹 설정을 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p102">Before you start using supervision, determine who will have their communications reviewed and who will perform those reviews. If you want to get started with just a few users to see how supervision works, you can skip setting up groups for now.</span></span>
    
- [<span data-ttu-id="bd517-111">감독을 조직에서 사용할 수 있도록</span><span class="sxs-lookup"><span data-stu-id="bd517-111">Make supervision available in your organization</span></span>](configure-supervision-policies.md#SRavailable)
    
    <span data-ttu-id="bd517-p103">정책을 설정할 수 있도록 사용자가 직접 감독 검토 역할 그룹에 추가 합니다. 보안에서 **데이터 관리 방식** **감독** 페이지에 액세스할 수이 역할이 할당 된 모든 사람이 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p103">Add yourself to the Supervisory Review role group so you can set up policies. Anyone who has this role assigned can access the **Supervision** page under **Data Governance** in the Security &amp; Compliance Center.</span></span> 
    
- [<span data-ttu-id="bd517-114">감독 정책 설정</span><span class="sxs-lookup"><span data-stu-id="bd517-114">Set up a supervision policy</span></span>](configure-supervision-policies.md#setupsuper)
    
    <span data-ttu-id="bd517-p104">보안에서 감독 정책 만들게 &amp; 준수 센터입니다. 이러한 정책은 어떤 통신은 조직 전체에서 검토 될 수 및 검토를 수행 해야 사용자 지정을 정의 합니다. 통신으로 전자 메일 타사 플랫폼 통신 (예: Facebook, Twitter 등)를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p104">You'll create supervision policies in the Security &amp; Compliance Center. These policies define which communications are subject to review in your organization, and specifies who should perform reviews. Communications include email as well as 3rd-party platform communications (such as Facebook, Twitter, etc.)</span></span>
    
- [<span data-ttu-id="bd517-118">Outlook web app를 사용 하 여 감독 정책에 의해 식별 된 통신을 검토 하려면</span><span class="sxs-lookup"><span data-stu-id="bd517-118">Use Outlook web app to review communications identified by a supervision policy</span></span>](configure-supervision-policies.md#UseOutlook)
    
    <span data-ttu-id="bd517-p105">감독에서 추가 기능에 액세스할 수 검토자가 Outlook web app 내의 오른쪽 감독 기능을 평가 하 고 각 항목을 분류 수 있도록 합니다. Outlook의 데스크톱 버전에 대 한 지원 출시 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p105">The Supervision add-in gives reviewers access to the supervision functionality right within Outlook web app so they can assess and categorize each item. Support for the desktop version of Outlook is coming soon.</span></span>
    
- <span data-ttu-id="bd517-121">**감독 보고서를 실행 합니다.**</span><span class="sxs-lookup"><span data-stu-id="bd517-121">**Run the supervision report**</span></span>
    
    <span data-ttu-id="bd517-p106">감독 보고서를 사용 하 여 정책 및 검토자 수준에서 검토 활동을 볼 수 있습니다. 각 정책에 대 한 검토 활동의 현재 상태에도 live 통계를 볼 수 있습니다. 자세한 내용은 [감독 보고서](supervision-reports.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bd517-p106">Use the supervision reports to see the review activity at the policy and reviewer level. For each policy, you can also view live statistics on the current state of review activity. For details, see [Supervision reports](supervision-reports.md).</span></span>
    
## <a name="set-up-groups-for-supervision"></a><span data-ttu-id="bd517-125">감독에 대 한 그룹을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-125">Set up groups for Supervision</span></span>
<span data-ttu-id="bd517-126"><a name="exampledist"> </a></span><span class="sxs-lookup"><span data-stu-id="bd517-126"></span></span>

 <span data-ttu-id="bd517-p107">감독 정책을 만들 때 사용자는 자신의 통신을 검토 하 고 이러한 검토를 수행 하는 사용자를 결정 합니다. 정책, 개인 또는 그룹에 사용자를 식별 하려면 전자 메일 주소를 사용 합니다. 설치 프로그램을 단순화 하려면 검토 자신의 통신을 가진 사용자에 대 한 그룹 및 이러한 통신을 검토 하는 사용자를 위해 그룹을 만듭니다. 그룹을 사용 하는 여러 필요할 수 있습니다-등 사용자의 고유한 두 그룹 간의 통신을 모니터링 하려면 또는 감독 수 없는 하려고 하는 그룹을 지정 하려는 경우. 이 작동 하는 방법에 대 한 자세한 내용은 [예제 메일 그룹](configure-supervision-policies.md#GroupExample) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bd517-p107">When you create a supervision policy, you'll determine who will have their communications reviewed and who will perform those reviews. In the policy, you'll use email addresses to identify individuals or groups of people. To simplify your setup, create groups for people who will have their communication reviewed and groups for people who will review those communications. If you're using groups, you might need several—for example, if you want to monitor communications between two distinct groups of people, or if you want to specify a group that isn't going to be supervised. See [Example distribution groups](configure-supervision-policies.md#GroupExample) for details about how this works.</span></span> 
  
<span data-ttu-id="bd517-p108">조직에서 그룹 내에서 또는 간의 통신을 감독를 Exchange 관리 센터에 메일 그룹을 설정할 ( **받는 사람** 에 게 이동 \> **그룹**). 메일 그룹을 설정 하는 방법에 대 한 자세한 내용은 [Manage 메일 그룹](http://go.microsoft.com/fwlink/?LinkId=613635) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bd517-p108">To supervise communications between or within groups in your organization, set up distribution groups in the Exchange admin center (go to **recipients** \> **groups**). For more information about setting up distribution groups, see [Manage distribution groups](http://go.microsoft.com/fwlink/?LinkId=613635)</span></span>
  
> [!NOTE]
> <span data-ttu-id="bd517-p109">원하는 경우 감독에 대 한 동적 메일 그룹 또는 보안 그룹을 사용할 수도 있습니다. 조직을 보다 적합 하는 경우 이러한 결정 하려면 요구, [메일 사용이 가능한 보안 그룹 관리](http://go.microsoft.com/fwlink/?LinkId=627033)및 [동적 메일 그룹 관리를](http://go.microsoft.com/fwlink/?LinkId=627058)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bd517-p109">You can also use dynamic distribution groups or security groups for supervision if you prefer. To help you decide if these better fit your organization needs, see [Manage mail-enabled security groups](http://go.microsoft.com/fwlink/?LinkId=627033), and [Manage dynamic distribution groups](http://go.microsoft.com/fwlink/?LinkId=627058).</span></span> 
  
### <a name="example-distribution-groups"></a><span data-ttu-id="bd517-136">예시 메일 그룹</span><span class="sxs-lookup"><span data-stu-id="bd517-136">Example distribution groups</span></span>
<span data-ttu-id="bd517-137"><a name="GroupExample"> </a></span><span class="sxs-lookup"><span data-stu-id="bd517-137"></span></span>

<span data-ttu-id="bd517-138">이 예에서는 Contoso 재무 국제를 호출 하는 재무 조직에 설정 된 메일 그룹을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-138">This example includes a distribution group that has been set up for a financial organization called Contoso Financial International.</span></span> 
  
<span data-ttu-id="bd517-p110">Contoso Financial International에서 미국에 있는 중개인 간 통신 샘플링을 감독해야 합니다. 하지만 해당 그룹 내에 있는 준수 관리자는 감독이 필요하지 않습니다. 이 예에서는 다음 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p110">In Contoso Financial International, a sampling of communications between brokers in the United States must be supervised. However, compliance officers within that group do not require supervision. For this example, we can create the following groups:</span></span>
  
|<span data-ttu-id="bd517-142">**이 메일 그룹 설정**</span><span class="sxs-lookup"><span data-stu-id="bd517-142">**Set up this distribution group**</span></span>|<span data-ttu-id="bd517-143">**그룹 주소(별칭)**</span><span class="sxs-lookup"><span data-stu-id="bd517-143">**Group address (alias)**</span></span>|<span data-ttu-id="bd517-144">**설명**</span><span class="sxs-lookup"><span data-stu-id="bd517-144">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bd517-145">모든 미국 중개인</span><span class="sxs-lookup"><span data-stu-id="bd517-145">All US brokers</span></span>  <br/> |<span data-ttu-id="bd517-146">US_Brokers@Contoso.com</span><span class="sxs-lookup"><span data-stu-id="bd517-146">US_Brokers@Contoso.com</span></span>  <br/> |<span data-ttu-id="bd517-147">이 그룹에는 Contoso에서 근무하는 모든 미국 중개인에 대한 전자 메일 주소가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-147">This group includes email addresses for all US-based brokers who work for Contoso.</span></span>  <br/> |
|<span data-ttu-id="bd517-148">모든 미국 준수 관리자</span><span class="sxs-lookup"><span data-stu-id="bd517-148">All US compliance officers</span></span>  <br/> |<span data-ttu-id="bd517-149">US_Compliance@Contoso.com</span><span class="sxs-lookup"><span data-stu-id="bd517-149">US_Compliance@Contoso.com</span></span>  <br/> |<span data-ttu-id="bd517-p111">이 그룹에는 Contoso에 대 한 작업 하는 모든 미국 기반 규정 준수 관리자에 대 한 전자 메일 주소가 포함 됩니다. 이 그룹이 모든 미국 기반 브로커의 하위 집합 이므로 감독 정책에서이 별칭 면제 규정 준수 관리자 등을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p111">This group includes email addresses for all US-based compliance officers who work for Contoso. Because this group is a subset of all US-based brokers, you can use this alias to exempt compliance officers from a supervision policy.</span></span>  <br/> |
   
<span data-ttu-id="bd517-152">[감독 정책 설정](configure-supervision-policies.md#setupsuper) 섹션에 정책을 구성 하는 경우 이러한 그룹을 사용 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-152">The [Set up a supervision policy](configure-supervision-policies.md#setupsuper) section describes how you can use these groups when you configure the policy.</span></span> 
  
## <a name="make-supervision-available-in-your-organization"></a><span data-ttu-id="bd517-153">감독을 조직에서 사용할 수 있도록</span><span class="sxs-lookup"><span data-stu-id="bd517-153">Make supervision available in your organization</span></span>
<span data-ttu-id="bd517-154"><a name="SRavailable"> </a></span><span class="sxs-lookup"><span data-stu-id="bd517-154"></span></span>

<span data-ttu-id="bd517-155">보안에서 **감독** 메뉴 옵션으로 사용할 수 있도록 &amp; 준수 센터 할당 되어 있어야 감독 검토 관리자 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-155">To make **Supervision** available as a menu option in the Security &amp; Compliance Center, you must be assigned the Supervisory Review Administrator role.</span></span> 
  
<span data-ttu-id="bd517-156">이 작업을 수행 하려면 추가 하거나 사용자가 직접 감독 검토 역할 그룹의 구성원으로 또는 새 역할 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-156">To do this, you can either add yourself as a member of the Supervisory Review role group, or you can create a new role group.</span></span>
  
### <a name="add-members-to-the-supervisory-review-role-group"></a><span data-ttu-id="bd517-157">감독 검토 역할 그룹에 구성원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-157">Add members to the Supervisory Review role group</span></span>

1. <span data-ttu-id="bd517-158">에 로그인 [https://protection.office.com](https://protection.office.com) Office 365 조직에서 관리 계정에 대 한 자격 증명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-158">Sign into [https://protection.office.com](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="bd517-159">보안에서 &amp; 준수 센터, **사용 권한 관리**로 이동 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bd517-159">In the Security &amp; Compliance Center, go to **Permissions**.</span></span>
    
3. <span data-ttu-id="bd517-160">**감독 검토** 역할 그룹을 선택 하 고 편집 아이콘을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-160">Select the **Supervisory Review** role group and then click the Edit icon.</span></span> 
    
4. <span data-ttu-id="bd517-161">**구성원** 섹션에서 조직에 대 한 감독 관리 하려는 사람을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-161">In the **Members** section, add the people who you want to manage supervision for your organization.</span></span> 
    
### <a name="create-a-new-role-group"></a><span data-ttu-id="bd517-162">새 역할 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="bd517-162">Create a new role group</span></span>

1. <span data-ttu-id="bd517-163">에 로그인 [https://protection.office.com](https://protection.office.com) Office 365 조직에서 관리 계정에 대 한 자격 증명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-163">Sign into [https://protection.office.com](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="bd517-164">보안에서 &amp; 준수 센터 **사용 권한 관리** 로 이동한 다음 추가 클릭 ( **+**).</span><span class="sxs-lookup"><span data-stu-id="bd517-164">In the Security &amp; Compliance Center, go to **Permissions** and then click Add ( **+**).</span></span>
    
3. <span data-ttu-id="bd517-p112">**역할** 섹션에서 추가 클릭 ( **+**) **감독 검토 관리자**까지 아래로 스크롤합니다. 이 역할을 역할 그룹을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p112">In the **Roles** section, click Add ( **+**) and scroll down to **Supervisory Review Administrator**. Add this role to the role group.</span></span>
    
4. <span data-ttu-id="bd517-167">**구성원** 섹션에서 조직에 대 한 감독 관리 하려는 사람을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-167">In the **Members** section, add the people who you want to manage supervision for your organization.</span></span> 
    
<span data-ttu-id="bd517-168">역할 그룹 및 사용 권한 하는 방법에 대 한 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터 ](permissions-in-the-security-and-compliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-168">For more information about role groups and permissions, see [Permissions in the Office 365 Security &amp; Compliance Center ](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="set-up-a-supervision-policy"></a><span data-ttu-id="bd517-169">감독 정책 설정</span><span class="sxs-lookup"><span data-stu-id="bd517-169">Set up a supervision policy</span></span>
<span data-ttu-id="bd517-170"><a name="setupsuper"> </a></span><span class="sxs-lookup"><span data-stu-id="bd517-170"></span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd517-171">감독 정책을 만들기 전에 모든 기존 감독 검토 정책을 먼저 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-171">Before creating a supervision policy, you must first remove any existing supervisory review policies.</span></span> 
  
1. <span data-ttu-id="bd517-172">에 로그인 [https://protection.office.com](https://protection.office.com) Office 365 조직에서 관리 계정에 대 한 자격 증명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-172">Sign into [https://protection.office.com](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="bd517-173">보안에서 &amp; 준수 센터를 클릭 하는 **데이터 관리 방식** 으로 이동 하십시오 \> **감독**합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-173">In the Security &amp; Compliance Center, go to click **Data governance** \> **Supervision**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="bd517-p113">이전 버전의 기능 **감독 검토 (회수 곧)** 으로 왼쪽 탐색 영역에 표시 될 수 있습니다. 곧이 버전을 사용 되지 않으며 제거 됩니다. **감독** 라는 새 버전에서 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p113">The previous version of the feature may show in the left-hand navigation as **Supervisory Review (retiring soon)**. This version will soon be deprecated and removed. The new version called **Supervision** will take its place.</span></span> 
  
3. <span data-ttu-id="bd517-177">**만들기** 를 클릭 하 고 정책의 다음 페이지를 설정 하는 마법사를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-177">Click **Create** and then follow the wizard to set up the following pages of the policy.</span></span> 
    
### <a name="policy-name-and-description"></a><span data-ttu-id="bd517-178">정책 이름 및 설명</span><span class="sxs-lookup"><span data-stu-id="bd517-178">Policy name and description</span></span>

<span data-ttu-id="bd517-p114">이름 및 사용자 정책에 대 한 설명을 입력 합니다. 예제 목적을 위해 정책 Contoso 미국 브로커 이름을 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p114">Enter a name and a description for your policy. For example purposes, we'll name the policy Contoso US Brokers.</span></span>
  
### <a name="choose-users-to-supervise"></a><span data-ttu-id="bd517-181">감독 하는 사용자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-181">Choose users to supervise</span></span>

- <span data-ttu-id="bd517-p115">**Supervise 이러한 사용자 또는 그룹** 상자에서 사용자를 선택 하거나 해당 통신 감독 하려는 그룹화 합니다. Contoso 미국 브로커에 대 한이 문서의 예제와 눌려 있거나, US_Brokers@Contoso.com 그룹 여기를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p115">In the **Supervise these users or groups** box, choose the users or groups whose communications your want to supervise. Sticking with our example for Contoso US Brokers, we'll choose the group US_Brokers@Contoso.com here.</span></span> 
    
- <span data-ttu-id="bd517-p116">감독에 그룹을 선택한 경우 감독에서 제외 된 그룹의 구성원을 선택 하려면 **해당이 사용자를 제외** 상자를 사용할 수 있습니다. 이 예제를 사용 하 여 그룹 US_Compliance@Contoso.com 여기을 배제 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p116">If you chose a group to supervise, you can use the **Exclude these users** box to choose members of the group who are exempt from supervision . Using the example , we'll exclude the group US_Compliance@Contoso.com here.</span></span> 
    
### <a name="choose-communications-to-review"></a><span data-ttu-id="bd517-186">검토에 대 한 통신을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-186">Choose communications to review</span></span>
<span data-ttu-id="bd517-187"><a name="CommsToReview"> </a></span><span class="sxs-lookup"><span data-stu-id="bd517-187"></span></span>

<span data-ttu-id="bd517-p117">기본적으로 **방향은** 조건은 표시 되 고 제거할 수 없습니다. 범위 (예: 특정 단어 또는 구를 포함 하는 콘텐츠를 검토만) 추가로 검토 하려는 경우 **조건 추가**클릭 합니다. 필요한 경우 여러 조건을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p117">By default, the **Direction is** condition is displayed and can't be removed. If you want to scope the review further (such as only reviewing content that contains certain words or phrases), click **Add a condition**. You can specify multiple conditions if needed.</span></span>
  
<span data-ttu-id="bd517-p118">선택 조건 (Facebook 또는 드롭 상자에서 같은) 조직에서 전자 메일 및 타사 모두 소스에서 통신에 적용 됩니다. Office 365 조직에 타사 통신 가져오기 (영문) 하는 방법에 대 한 자세한 내용은, [Office 365의 보관 제 3 자 데이터](https://technet.microsoft.com/EN-US/library/mt621583.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bd517-p118">The conditions you choose will apply to communications from both email and 3rd-party sources in your organization (like from Facebook or DropBox). For details about importing 3rd-party communications into your Office 365 organization, see [Archiving third-party data in Office 365](https://technet.microsoft.com/EN-US/library/mt621583.aspx).</span></span>
  
<span data-ttu-id="bd517-193">다음 표에서 각 조건에 대 한 자세히 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-193">The following table explains more about each condition.</span></span>
  
|<span data-ttu-id="bd517-194">**조건**</span><span class="sxs-lookup"><span data-stu-id="bd517-194">**Condition**</span></span>|<span data-ttu-id="bd517-195">**이 조건을 사용하는 방법**</span><span class="sxs-lookup"><span data-stu-id="bd517-195">**How to use this condition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bd517-196">방향이 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-196">Direction is</span></span>  <br/> |<span data-ttu-id="bd517-197">**인바운드** **하** **에서** 사용자를 감독 하도록 설정한 사용자 정책에 포함 되지 않은 전송 되는 통신을 검토 하려면 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-197">Choose **Inbound** to review communications that are sent **to** the people you chose to supervise **from** people not included in the policy.</span></span>  <br/> <span data-ttu-id="bd517-198">검토할 수 있는 통신 하는 경우 **아웃 바운드** 선택 감독 하도록 선택한 사용자에서 **** 보낸 * *를 * * 사용자 정책에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-198">Choose **Outbound** if you want to review communications that are sent **from** the people you chose to supervise ** to ** people not included in the policy.</span></span>  <br/> <span data-ttu-id="bd517-199">정책에서 **내부** **간에** 전달 되는 통신 검토를 식별 하는 사용자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-199">Choose **Internal** to review communications sent **between** the people you identified in the policy.</span></span>  <br/> |
|<span data-ttu-id="bd517-200">메시지에 다음 단어 포함</span><span class="sxs-lookup"><span data-stu-id="bd517-200">Message contains any of these words</span></span>  <br/> <span data-ttu-id="bd517-201">메시지에 포함 된 다음 단어 없음</span><span class="sxs-lookup"><span data-stu-id="bd517-201">Message contains none of these words</span></span>  <br/> |<span data-ttu-id="bd517-p119">특정 단어 또는 구를 포함 되거나 메시지에서 제외 하는 경우 정책을 적용할 별도 줄에 각 단어 또는 구를 입력 합니다. 입력 한 단어의 각 줄을 개별적으로 적용 됩니다 (메시지에 적용할 정책에 대 한 이러한 줄 중 하나에만 적용 해야). 단어 또는 구를 입력 하는 방법에 대 한 자세한 내용은 [일치 하는 단어와 구를 전자 메일 또는 첨부 파일에](configure-supervision-policies.md#Matchwords)다음 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bd517-p119">To apply the policy when certain words or phrases are included or excluded in a message, enter each word or phrase on a separate line. Each line of words you enter will be applied separately (only one of these lines must apply for the policy to apply to the message). For more information about entering words or phrases, see the next section [Matching words and phrases to emails or attachments](configure-supervision-policies.md#Matchwords).  </span></span><br/> |
|<span data-ttu-id="bd517-205">이러한 단어 중 하나라도 첨부 파일 포함</span><span class="sxs-lookup"><span data-stu-id="bd517-205">Attachment contains any of these words</span></span>  <br/> <span data-ttu-id="bd517-206">첨부 파일 모두 포함 되지 않은 다음 단어 포함</span><span class="sxs-lookup"><span data-stu-id="bd517-206">Attachment contains none of these words</span></span>  <br/> |<span data-ttu-id="bd517-p120">특정 단어 또는 구를 포함 되거나 메시지의 첨부 파일 (예: Word 문서)에서 제외 하는 경우 정책을 적용할 별도 줄에 각 단어 또는 구를 입력 합니다. 입력 한 단어의 각 줄을 개별적으로 적용 됩니다 (한 줄만 해야 첨부 파일에 적용할 정책에 대 한 적용 됨). 단어 또는 구를 입력 하는 방법에 대 한 자세한 내용은 [일치 하는 단어와 구를 전자 메일 또는 첨부 파일에](configure-supervision-policies.md#Matchwords)다음 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bd517-p120">To apply the policy when certain words or phrases are included or excluded in a message attachment (such as a Word document), enter each word or phrase on a separate line. Each line of words you enter will be applied separately (only one line must apply for the policy to apply to the attachment). For more information about entering words or phrases, see the next section [Matching words and phrases to emails or attachments](configure-supervision-policies.md#Matchwords).  </span></span><br/> |
|<span data-ttu-id="bd517-210">첨부 파일이 이러한 파일 형식 중 하나</span><span class="sxs-lookup"><span data-stu-id="bd517-210">Attachment is any of these file types</span></span>  <br/> <span data-ttu-id="bd517-211">첨부 파일 중 어느 것에 이러한 파일 형식</span><span class="sxs-lookup"><span data-stu-id="bd517-211">Attachment is none of these file types</span></span>  <br/> |<span data-ttu-id="bd517-p121">첨부 파일의 특정 형식 포함 또는 제외 되는 통신 내용을 감독, 파일 확장명 (예:.exe 또는.pdf)를 입력 합니다. 포함 하거나 여러 파일 확장명도 제외 하려는 경우 별도 줄에 이러한를 입력 합니다. 하나의 첨부 파일 확장명이 적용할 정책에 대 한 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p121">To supervise communications that include or exclude specific types of attachments, enter the file extensions (such as .exe or .pdf). If you want to include or exclude multiple file extensions, enter these on separate lines. Only one attachment extension needs to match for the policy to apply.</span></span>  <br/> |
|<span data-ttu-id="bd517-215">다음보다 큰 메시지 크기</span><span class="sxs-lookup"><span data-stu-id="bd517-215">Message size is larger than</span></span>  <br/> <span data-ttu-id="bd517-216">메시지 크기 보다 큰지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-216">Message size is not larger than</span></span>  <br/> |<span data-ttu-id="bd517-p122">특정 크기를 기준으로 메시지를 검토 하려면 이러한 조건을 사용 하 여 검토 적용 되기 전에 메시지 수 최대 또는 최소 크기를 지정 합니다. 예: **메시지 크기 보다 크면** 지정 하는 경우 \> **1.0 MB**, 1.01 MB 및 더 큰가 있는 모든 메시지를 검토를 따르게 됩니다. 바이트, 킬로바이트, 메가바이트, 또는이 조건에 대 한 기가바이트를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p122">To review messages based on a certain size, use these conditions to specify the maximum or minimum size a message can be before it is subject to review. For example, if you specify **Message size is larger than** \> **1.0 MB**, all messages that are 1.01 MB and larger will be subject to review. You can choose bytes, kilobytes, megabytes, or gigabytes for this condition.  </span></span><br/> |
|<span data-ttu-id="bd517-220">첨부 파일 보다 큽니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-220">Attachment is larger than</span></span>  <br/> <span data-ttu-id="bd517-221">첨부 파일이 보다 큰 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-221">Attachment is not larger than</span></span>  <br/> |<span data-ttu-id="bd517-p123">해당 첨부 파일의 크기를 기준으로 메시지를 검토 하려면 메시지 하기 전에 최대 또는 최소 크기는 첨부 파일 수 있고 해당 첨부 파일은 검토 될 수를 지정 합니다. 예: **보다 큰 첨부 파일이** 지정 하는 경우 \> **2.0 MB**, 첨부 파일이 있는 메시지를 모든 2.01 MB 하 고 조치 검토를 따르게 됩니다. 바이트, 킬로바이트, 메가바이트, 또는이 조건에 대 한 기가바이트를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p123">To review messages based on the size of their attachments, specify the maximum or minimum size an attachment can be before the message and its attachments are subject to review. For example, if you specify **Attachment is larger than** \> **2.0 MB**, all messages with attachments 2.01 MB and over will be subject to review. You can choose bytes, kilobytes, megabytes, or gigabytes for this condition.  </span></span><br/> |
   
#### <a name="matching-words-and-phrases-to-emails-or-attachments"></a><span data-ttu-id="bd517-225">단어 및 구를 전자 메일 또는 첨부 파일에 일치</span><span class="sxs-lookup"><span data-stu-id="bd517-225">Matching words and phrases to emails or attachments</span></span>
<span data-ttu-id="bd517-226"><a name="Matchwords"> </a></span><span class="sxs-lookup"><span data-stu-id="bd517-226"></span></span>

<span data-ttu-id="bd517-p124">입력 한 단어의 각 줄을 개별적으로 적용 됩니다 (한 줄만 해야 전자 메일 또는 첨부 파일에 적용할 정책 조건을 적용 됨). 예, 키워드 "은행 담당자" 및 "내부 인 거래" **메시지에 포함 된 이러한 단어 중 하나라도**, 상태을 사용 하 여 별도 줄에 보겠습니다. 정책 "은행 담당자" 단어 또는 구 "내부 인 거래"가 포함 된 모든 메시지에 적용 됩니다. 이 정책 조건을 적용 하려면이 단어 또는 구를 중 하나만 날짜 여야 합니다. 메시지 또는 첨부 파일에 있는 단어 입력 하면 정확히 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p124">Each line of words you enter will be applied separately (only one line must apply for the policy condition to apply to the email or attachment). For example, let's use the condition, **Message contains any of these words**, with the keywords "banker" and "insider trading" on separate lines. The policy will apply to any messages that includes the word "banker" or the phrase "insider trading". Only one of these words or phrases must occur for this policy condition to apply. Words in the message or attachment must exactly match what you enter.</span></span>
  
#### <a name="entering-multiple-conditions"></a><span data-ttu-id="bd517-232">여러 조건 입력</span><span class="sxs-lookup"><span data-stu-id="bd517-232">Entering multiple conditions</span></span>
<span data-ttu-id="bd517-233"><a name="Matchwords"> </a></span><span class="sxs-lookup"><span data-stu-id="bd517-233"></span></span>

<span data-ttu-id="bd517-p125">여러 조건, 입력 하는 경우 Office 365를 사용 하 여 모든 조건에 해당 함께 통신 항목에 정책을 적용 하는 시기를 결정 합니다. 여러 조건, 설정 하는 경우 자신이 모두 충족 되어야 합니다를 적용 하려면 정책에 대 한 예외를 입력 하지 않으면. 예, 메시지 "영업" 단어를 포함 하 고 2MB 보다 큰 경우에 적용 해야 하는 정책을 만들어야 할 가정해 보겠습니다. 그러나 메시지에는 "Contoso 재무 하 여 승인 됨" 라는 단어가 포함 된, 정책이 적용 되지 해야 합니다. 따라서이 경우 세 조건 수 다음과 같이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p125">If you enter multiple conditions, Office 365 uses all the conditions together to determine when to apply the policy to communication items. When you set up multiple conditions, they must all be met for the policy to apply, unless you enter an exception. For example, let's say you need to create a policy that should apply if a message contains the word "trade", and is larger than 2MB. However, if the message also contains the words "Approved by Contoso financial", the policy should not apply. Thus, in this case, the three conditions would be as follows:</span></span> 
  
- <span data-ttu-id="bd517-239">**메시지에 포함 된 다음 단어**를 "영업" 키워드와</span><span class="sxs-lookup"><span data-stu-id="bd517-239">**Message contains any of these words**, with the keywords "trade"</span></span>
    
- <span data-ttu-id="bd517-240">**메시지 크기 보다 크면**, 값을 가진 2MB</span><span class="sxs-lookup"><span data-stu-id="bd517-240">**Message size is larger than**, with the value 2 MB</span></span>
    
- <span data-ttu-id="bd517-241">**메시지에 포함 된 다음 단어 없음**, "Contoso 재무 팀에서 승인 됨" 키워드와 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-241">**Message contains none of these words**, with the keywords "Approved by Contoso financial team".</span></span>
    
### <a name="specify-percentage-to-review"></a><span data-ttu-id="bd517-242">검토에 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-242">Specify percentage to review</span></span>
<span data-ttu-id="bd517-243"><a name="CommsToReview"> </a></span><span class="sxs-lookup"><span data-stu-id="bd517-243"></span></span>

<span data-ttu-id="bd517-p126">검토 하는 콘텐츠의 양을 줄일 하려는 백분율을 지정 합니다. 임의로 선택한 조건과 일치 하는 전체에서 해당 콘텐츠의 양을 선택 합니다 했습니다. 검토자가 모든 항목을 검토를 **100%** 를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p126">If you want to reduce the amount of content to review, specify a percentage. We'll randomly select that amount of content from the total that matched the conditions you chose. If you want reviewers to review all items, enter **100%**.</span></span>
  
### <a name="choose-reviewers"></a><span data-ttu-id="bd517-247">검토자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-247">Choose reviewers</span></span>
<span data-ttu-id="bd517-248"><a name="CommsToReview"> </a></span><span class="sxs-lookup"><span data-stu-id="bd517-248"></span></span>

<span data-ttu-id="bd517-p127">사용자 및 그룹을 선택 하면 Outlook web app에서 감독 app를 사용 하 여이 정책에 의해 반환 되는 통신을 검사 하려면 됩니다. 내부 또는 외부 검토자에 대 한 전자 메일 주소를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p127">The users and groups you choose will use the Supervision app in Outlook web app to examine the communications that are returned by this policy. You can include email addresses for internal or external reviewers.</span></span> 
  
### <a name="review-your-settings"></a><span data-ttu-id="bd517-251">설정 검토</span><span class="sxs-lookup"><span data-stu-id="bd517-251">Review your settings</span></span>
<span data-ttu-id="bd517-252"><a name="CommsToReview"> </a></span><span class="sxs-lookup"><span data-stu-id="bd517-252"></span></span>

<span data-ttu-id="bd517-p128">감독 정책의 모든 섹션을 완료 한 후 설정을 검토 하 고을 클릭 **완료 날짜** 를 사용자 정책을 저장 합니다. 통신 캡처를 시작 하려면 정책에 대 한 몇 시간이 걸릴 수 있습니다. 감독은 검토자가 Outlook web app에서 액세스할 수 있는 공유 폴더에 검토를 위해 모든 통신을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p128">After you've completed all sections of the supervision policy, review your settings and then click **Finish** to save your policy. It might take a few hours for the policy to start capturing communications. Supervision delivers all communications for review into a shared folder that reviewers can access in Outlook web app.</span></span> 
  
## <a name="use-outlook-web-app-to-review-communications-identified-by-a-supervision-policy"></a><span data-ttu-id="bd517-256">Outlook web app를 사용 하 여 감독 정책에 의해 식별 된 통신을 검토 하려면</span><span class="sxs-lookup"><span data-stu-id="bd517-256">Use Outlook web app to review communications identified by a supervision policy</span></span>
<span data-ttu-id="bd517-257"><a name="UseOutlook"> </a></span><span class="sxs-lookup"><span data-stu-id="bd517-257"></span></span>

<span data-ttu-id="bd517-p129">검토자가 통신을 검토 하는 감독 용 추가 기능에 Outlook web app 사용 합니다. 추가 기능에 자동으로 설치 Outlook web app에서 정책에 지정 하는 모든 검토자에 대 한. Outlook의 데스크톱 버전에 대 한 지원 출시 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p129">Reviewers will use the Supervision add-in for Outlook web app to review communications. The add-in is installed automatically in Outlook web app for all reviewers you specified in the policy. Support for the desktop version of Outlook is coming soon.</span></span>
  
 <span data-ttu-id="bd517-261">**Outlook web app에서 통신을 검토합니다.**</span><span class="sxs-lookup"><span data-stu-id="bd517-261">**Reviewing communications in Outlook web app**</span></span>
  
1. <span data-ttu-id="bd517-262">Outlook web app에서 확장 된 **감독- \<정책 이름\> ** 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-262">In Outlook web app, expand the **Supervision - \<policy name\>** folder.</span></span> 
    
2. <span data-ttu-id="bd517-263">** \<정책 이름\> ** 하위 폴더, 검토자가 해당 감독 정책에 의해 식별 된 모든 통신 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-263">In the **\<policy name\>** subfolder, reviewers will see all the communications identified by that supervision policy.</span></span> 
    
    ![감독 추가 기능에서 선택한 감독 정책 하위 폴더를 표시 하는 Outlook web app에서](media/eef329bf-2bd0-477e-a715-76ca19b3347f.jpg)
  
3. <span data-ttu-id="bd517-265">항목을 검토 하 고 **감독** 추가 기능을 클릭을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-265">Open an item to review and click the **Supervision** add-in.</span></span> 
    
4. <span data-ttu-id="bd517-p130">추가 기능에 사용 하 여 항목 **정책 준수**, **비 정책 준수**, **명확 하지 않은,** 또는 **"해결 됨"** 으로 분류할 수 있습니다. 아래에서 해당 하위 폴더를 이동할 수는 항목을 분류 했을 때는 ** \<정책 이름\> ** 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="bd517-p130">Use the add-in to classify the item as **Compliant**, **Non-Compliant**, **Questionable,** or **Resolved**. After you've classified an item, it will be moved to the corresponding subfolder under the **\<policy name\>** folder.</span></span> 
    

