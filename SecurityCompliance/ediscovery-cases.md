---
title: Office 365 보안 &amp; 및 준수 센터의 eDiscovery 사례
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 8dd335ab-29d0-41c3-8dd8-9f7c7481e60c
description: Office 365 보안 &amp; 및 준수 센터를 사용 하 여 조직에서 eDiscovery 사례를 만들고 관리 합니다. 사례에 멤버를 할당 하 고, 콘텐츠 위치를 유지 하 고, 사례와 연결 된 콘텐츠 searchs를 실행 하 고, 검색 결과를 내보낼 수 있습니다. 고급 eDiscovery에서 추가 분석을 위해 사례 데이터를 준비할 수도 있습니다.
ms.openlocfilehash: 92ef00bbdd8de5b1ba6bdae40bce96720ac46089
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214018"
---
# <a name="ediscovery-cases-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="032a8-105">Office 365 보안 &amp; 및 준수 센터의 eDiscovery 사례</span><span class="sxs-lookup"><span data-stu-id="032a8-105">eDiscovery cases in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="032a8-p102">Office 365 보안 &amp; 및 준수 센터에서 ediscovery 사례를 사용 하 여 조직에서 ediscovery 사례를 만들고, 액세스 하 고, 관리할 수 있는 사람을 제어할 수 있습니다. 조직에 office 365 E5 구독이 있는 경우 eDiscovery 사례를 사용 하 여 office 365 Advanced eDiscovery를 사용 하 여 검색 결과를 분석할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p102">You can use eDiscovery cases in the Office 365 Security &amp; Compliance Center to control who can create, access, and manage eDiscovery cases in your organization. If your organization has an Office 365 E5 subscription, you can also use eDiscovery cases to analyze search results by using Office 365 Advanced eDiscovery.</span></span>
  
<span data-ttu-id="032a8-p103">eDiscovery 사례를 사용 하면 사례에 구성원을 추가 하 고, 특정 사례 구성원이 수행할 수 있는 작업 유형을 제어 하 고, 법적 사례와 관련 된 콘텐츠 위치에 보류를 적용 하 고, 여러 콘텐츠 검색을 단일 사례와 연결 하는 기능을 제어할 수 있습니다. 사례와 연결 된 콘텐츠 검색의 결과를 내보내거나 고급 eDiscovery에서 분석을 위한 검색 결과를 준비할 수도 있습니다. eDiscovery 사례는 조직에서 특정 법률 사례에 대 한 콘텐츠 검색 및 검색 결과에 액세스할 수 있는 사용자를 제한 하는 좋은 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p103">An eDiscovery case allows you to add members to a case, control what types of actions that specific case members can perform, place a hold on content locations relevant to a legal case, and associate multiple Content Searches with a single case. You can also export the results of any Content Search that is associated with a case or prepare search results for analysis in Advanced eDiscovery. eDiscovery cases are a good way to limit who has access to Content Searches and search results for a specific legal case in your organization.</span></span>
  
<span data-ttu-id="032a8-111">다음 워크플로를 사용 하 여 보안 &amp; 및 준수 센터 및 고급 eDiscovery에서 eDiscovery 사례를 설정 하 고 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-111">Use the following workflow to set up and use eDiscovery cases in the Security &amp; Compliance Center and Advanced eDiscovery.</span></span>

[<span data-ttu-id="032a8-112">1단계: 잠재적인 사례 구성원에게 eDiscovery 권한 할당</span><span class="sxs-lookup"><span data-stu-id="032a8-112">Step 1: Assign eDiscovery permissions to potential case members</span></span>](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[<span data-ttu-id="032a8-113">2 단계: 새 사례 만들기</span><span class="sxs-lookup"><span data-stu-id="032a8-113">Step 2: Create a new case</span></span>](#step-2-create-a-new-case)

[<span data-ttu-id="032a8-114">3 단계: 사례에 구성원 추가</span><span class="sxs-lookup"><span data-stu-id="032a8-114">Step 3: Add members to a case</span></span>](#step-3-add-members-to-a-case)

[<span data-ttu-id="032a8-115">4 단계: 콘텐츠 위치를 보류에 배치</span><span class="sxs-lookup"><span data-stu-id="032a8-115">Step 4: Place content locations on hold</span></span>](#step-4-place-content-locations-on-hold)

[<span data-ttu-id="032a8-116">5 단계: 사례와 연결 된 콘텐츠 검색 만들기 및 실행</span><span class="sxs-lookup"><span data-stu-id="032a8-116">Step 5: Create and run a Content Search associated with a case</span></span>](#step-5-create-and-run-a-content-search-associated-with-a-case)

[<span data-ttu-id="032a8-117">6 단계: 사례와 연결 된 콘텐츠 검색 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="032a8-117">Step 6: Export the results of a Content Search associated with a case</span></span>](#step-6-export-the-results-of-a-content-search-associated-with-a-case)

[<span data-ttu-id="032a8-118">7 단계: 고급 eDiscovery에 대 한 검색 결과 준비</span><span class="sxs-lookup"><span data-stu-id="032a8-118">Step 7: Prepare search results for Advanced eDiscovery</span></span>](#step-7-prepare-search-results-for-advanced-ediscovery)

[<span data-ttu-id="032a8-119">8 단계: Advanced eDiscovery의 사례로 이동</span><span class="sxs-lookup"><span data-stu-id="032a8-119">Step 8: Go to the case in Advanced eDiscovery</span></span>](#step-8-go-to-the-case-in-advanced-ediscovery)

[<span data-ttu-id="032a8-120">반드시 9 단계: 사례 닫기</span><span class="sxs-lookup"><span data-stu-id="032a8-120">(Optional) Step 9: Close a case</span></span>](#optional-step-9-close-a-case)

[<span data-ttu-id="032a8-121">반드시 10 단계: 닫힌 사례 다시 열기</span><span class="sxs-lookup"><span data-stu-id="032a8-121">(Optional) Step 10: Re-open a closed case</span></span>](#optional-step-10-re-open-a-closed-case)

[<span data-ttu-id="032a8-122">추가 정보</span><span class="sxs-lookup"><span data-stu-id="032a8-122">More information</span></span>](#more-information)
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a><span data-ttu-id="032a8-123">1단계: 잠재적인 사례 구성원에게 eDiscovery 권한 할당</span><span class="sxs-lookup"><span data-stu-id="032a8-123">Step 1: Assign eDiscovery permissions to potential case members</span></span>

<span data-ttu-id="032a8-p104">첫 번째 단계는 사용자에 게 적절 한 ediscovery 관련 사용 권한을 할당 하 여 2 단계에서 ediscovery 사례에 추가할 수 있도록 하는 것입니다. eDiscovery 권한을 할당 하려면 Office 365 보안 &amp; 준수 센터에서 조직 관리 역할 그룹의 구성원 이거나 역할 관리 역할을 할당 받아야 합니다. 다음 목록에서는 보안 &amp; 및 준수 센터의 eDiscovery 관련 역할 그룹에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p104">The first step is to assign the appropriate eDiscovery-related permissions to people so you can add them to an eDiscovery case in Step 2. You have to be a member of the Organization Management role group (or be assigned the Role Management role) in the Office 365 Security &amp; Compliance Center to assign eDiscovery permissions. The following list describes the eDiscovery-related role groups in the Security &amp; Compliance Center.</span></span> 
  
- <span data-ttu-id="032a8-p105">**검토자** -이 역할 그룹은 가장 제한적인 eDiscovery 관련 사용 권한을 가집니다. 이 역할 그룹의 기본 목적은 구성원이 Office 365 Advanced eDiscovery에서 대/소문자 데이터를 보고 액세스 하도록 허용 하는 것입니다. 이 그룹의 구성원은 보안 &amp; 준수 센터에서 구성원 인 **eDiscovery** 페이지의 사례 목록만 보고 열 수 있습니다. 사용자가 Security & 준수 센터의 사례에 액세스 한 후 advanced **ediscovery로 전환을** 클릭 하 여 advanced ediscovery에서 사례 데이터에 액세스 하 고 분석할 수 있습니다. 사례를 만들고, 사례에 구성원을 추가 하 고, 보류를 만들거나, 검색 결과를 미리 보거나, 검색 결과를 내보내거나, 고급 eDiscovery를 위한 준비 결과를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p105">**Reviewer** - This role group has the most restrictive eDiscovery-related permissions. The primary purpose of this role group is to allow members to view and access case data in Office 365 Advanced eDiscovery. Members of this group can only see and open the list of the cases on the **eDiscovery** page in the Security &amp; Compliance Center that they are members of. After the user accesses a case in the Security & Compliance Center, they can click **Switch to Advanced eDiscovery** to access and analyze the case data in Advanced eDiscovery. They can't create cases, add members to a case, create holds, create searches, preview search results, export search results, or prepare results for Advanced eDiscovery.</span></span> 
    
- <span data-ttu-id="032a8-p106">**ediscovery 관리자** -이 역할 그룹의 구성원은 ediscovery 사례를 만들고 관리할 수 있습니다. 구성원을 추가 및 제거 하 고, 콘텐츠 위치를 보류 상태로 설정 하 고, 사례와 연결 된 콘텐츠 검색을 만들고 편집 하 고, 콘텐츠 검색 결과를 내보내고, 고급 eDiscovery에서 분석을 위한 검색 결과를 준비할 수 있습니다. 이 역할 그룹에는 두 개의 하위 그룹이 있습니다. 이러한 하위 그룹의 차이점은 범위를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p106">**eDiscovery Manager** - Members of this role group can create and manage eDiscovery cases. They can add and remove members, place content locations on hold, create and edit Content Searches associated with a case, export the results of a Content Search, and prepare search results for analysis in Advanced eDiscovery. There are two sub-groups in this role group. The difference between these subgroups is based on scope.</span></span>
    
  - <span data-ttu-id="032a8-p107">**ediscovery 관리자** -자신이 만들거나 구성원 인 ediscovery 사례를 보고 관리할 수 있습니다. 다른 ediscovery 관리자가 사례를 만들지만 두 번째 ediscovery 관리자를 해당 사례 구성원으로 추가 하지 않는 경우 두 번째 ediscovery 관리자는 보안 &amp; 및 준수 센터에서 **ediscovery** 페이지의 사례를 보거나 열 수 없습니다. eDiscovery 관리자는 고급 eDiscovery의 사례에 액세스 하 여 분석 작업을 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p107">**eDiscovery Manager** - Can view and manage the eDiscovery cases they create or are a member of. If another eDiscovery Manager creates a case but doesn't add a second eDiscovery Manager as a member of that case, the second eDiscovery Manager won't be able to view or open the case on the **eDiscovery** page in the Security &amp; Compliance Center. eDiscovery Managers can also access their cases in Advanced eDiscovery to perform analysis tasks.</span></span> 
    
  - <span data-ttu-id="032a8-p108">**ediscovery 관리자** -ediscovery 관리자가 수행할 수 있는 모든 사례 관리 작업을 수행할 수 있습니다. 또한 eDiscovery 관리자는 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p108">**eDiscovery Administrator** - Can perform all case management tasks that an eDiscovery Manager can do. Additionally, an eDiscovery Administrator can:</span></span>
    
    - <span data-ttu-id="032a8-141">**eDiscovery** 페이지에 나열된 모든 사례를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-141">View all cases that are listed on the **eDiscovery** page.</span></span> 
    
    - <span data-ttu-id="032a8-142">조직의 대/소문자를 구성원으로 추가한 후 조직에서 모든 사례를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-142">Manage any case in the organization after they add themself as a member of the case.</span></span>
    
    - <span data-ttu-id="032a8-143">조직의 모든 경우에 대 한 고급 eDiscovery의 사례 데이터 액세스</span><span class="sxs-lookup"><span data-stu-id="032a8-143">Access case data in Advanced eDiscovery for any case in the organization.</span></span>
    
    <span data-ttu-id="032a8-144">사용자가 조직에서 eDiscovery 관리자가 되려고 하는 이유에 자세한 내용은 [More information](#more-information)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="032a8-144">See the [More information](#more-information) section for reasons why you may want an eDiscovery Administrator in your organization.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="032a8-145">사용자가 이러한 ediscovery 관련 역할 그룹 중 하나의 구성원이 아니거나 검토자 역할이 할당 된 역할 그룹의 구성원이 아닌 경우 ediscovery 사례의 구성원으로 추가할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-145">If a person isn't a member of one of these eDiscovery-related role groups, or isn't a member of a role group that's assigned the Reviewer role, you can't add them as a member of an eDiscovery case.</span></span> 

<span data-ttu-id="032a8-146">ediscovery 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 ediscovery 사용 권한 할당](assign-ediscovery-permissions.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="032a8-146">For more information about eDiscovery permissions, see [Assign eDiscovery permissions in the Office 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
  
 <span data-ttu-id="032a8-147">**eDiscovery 권한을 할당하려면**</span><span class="sxs-lookup"><span data-stu-id="032a8-147">**To assign eDiscovery permissions:**</span></span>
  
1. <span data-ttu-id="032a8-148">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-148">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="032a8-149">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-149">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="032a8-150">보안 &amp; 및 준수 센터에서 **사용 권한을**클릭 하 고 할당 하려는 eDiscovery 권한에 따라 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-150">In the Security &amp; Compliance Center, click **Permissions**, and then do one of the following based on the eDiscovery permissions that you want to assign.</span></span>
    
    - <span data-ttu-id="032a8-p109">검토자 권한을 할당 하려면 **검토자** 역할 그룹을 선택 하 고 **구성원**옆의 **편집**을 클릭 합니다. **구성원 선택을**클릭 하 고 **편집**을 클릭 ![한 다음](media/ITPro-EAC-AddIcon.gif) 아이콘 **추가**를 클릭 하 고 검토자 역할 그룹에 추가할 사용자를 선택한 다음 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p109">To assign Reviewer permissions, select the **Reviewer** role group, and then next to **Members**, click **Edit**. Click **Choose members**, click **Edit**, click ![Add Icon](media/ITPro-EAC-AddIcon.gif) **Add**, select the user that you want to add to the Reviewer role group, and then click **Add**.</span></span>
    
    - <span data-ttu-id="032a8-p110">ediscovery 관리자 권한을 할당 하려면 **ediscovery 관리자** 역할 그룹을 선택한 다음 **ediscovery 관리자**옆에 있는 **편집**을 클릭 합니다. **ediscovery 관리자 선택을**클릭 하 고 **편집**을 클릭 ![한 다음](media/ITPro-EAC-AddIcon.gif) add Icon \* \* add \* \*를 클릭 하 고 eDiscovery 관리자로 추가할 사용자를 선택한 다음 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p110">To assign eDiscovery Manager permissions, select the **eDiscovery Manager** role group, and then next to **eDiscovery Manager**, click **Edit**. Click **Choose eDiscovery Manager**, click **Edit**, click ![Add Icon](media/ITPro-EAC-AddIcon.gif) \*\* Add \*\*, select the user that you want to add as an eDiscovery Manager, and then click **Add**.</span></span>
    
    - <span data-ttu-id="032a8-p111">ediscovery 관리자 권한을 할당 하려면 **ediscovery 관리자** 역할 그룹을 선택한 다음 **ediscovery 관리자**옆에 있는 **편집**을 클릭 합니다. **ediscovery 관리자 선택을**클릭 하 고 **편집**, 아이콘 ![](media/ITPro-EAC-AddIcon.gif) \*\*\*\* 추가를 차례로 클릭 한 다음 eDiscovery 관리자로 추가할 사용자를 선택 하 고 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p111">To assign eDiscovery Administrator permissions, select the **eDiscovery Manager** role group, and then next to **eDiscovery Administrator**, click **Edit**. Click **Choose eDiscovery Administrator**, click **Edit**, click ![Add Icon](media/ITPro-EAC-AddIcon.gif) **Add**, select the user that you want to add as an eDiscovery Administrator, and then click **Add**.</span></span>
    
4. <span data-ttu-id="032a8-157">모든 사용자를 추가한 후에는 **완료**를 클릭 하 고 **저장** 을 클릭 하 여 역할 그룹에 대 한 변경 내용을 저장 한 다음 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-157">After you've added all the users, click **Done**, click **Save** to save the changes to the role group, and then click **Close**.</span></span>

## <a name="step-2-create-a-new-case"></a><span data-ttu-id="032a8-158">2 단계: 새 사례 만들기</span><span class="sxs-lookup"><span data-stu-id="032a8-158">Step 2: Create a new case</span></span>

<span data-ttu-id="032a8-p112">다음 단계에서는 새 eDiscovery 사례를 만듭니다. ediscovery 사례를 만들려면 ediscovery 관리자 역할 그룹의 구성원 이어야 합니다. 앞에서 설명한 것 처럼 보안 &amp; 및 준수 센터에서 새 사례를 만든 후에는 조직에서 Office 365 E5 구독을 사용 하는 경우에도 고급 eDiscovery에서 동일한 사례에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p112">The next step is to create a new eDiscovery case. You must be a member of the eDiscovery Managers role group to create eDiscovery cases. As previously explained, after you create a new case in the Security &amp; Compliance Center, you (and other case members) will be able to access that same case in Advanced eDiscovery if you're organization has an Office 365 E5 subscription.</span></span>
  
1. <span data-ttu-id="032a8-162">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-162">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="032a8-163">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-163">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="032a8-164">&amp; 보안 및 준수 센터에서 \*\* &amp; 검색 조사\*\* ](media/ITPro-EAC-AddIcon.gif) \> **eDiscovery**를 클릭 한 다음 아이콘 추가 ![( **사례 만들기**)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-164">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery**, and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif) **Create a case**.</span></span>
    
4. <span data-ttu-id="032a8-p113">**새 사례** 페이지에서 사례 이름을 지정 하 고, 선택적 설명을 입력 한 다음 **저장**을 클릭 합니다. 사례 이름은 조직 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p113">On the **New Case** page, give the case a name, type an optional description, and then click **Save**. Note that the case name must be unique in your organization.</span></span>
    
    ![새 사례 만들기](media/7f78f83b-1525-4c77-9888-4b6bda1e148d.png)
  
    <span data-ttu-id="032a8-p114">새 사례가 **eDiscovery** 페이지의 사례 목록에 표시 됩니다. 케이스의 상태 ( **활성** 또는 **닫힘**), 사례에 대 한 설명 (이전 단계에서 만들어짐), 사례를 마지막으로 변경 하는 시기 등을 포함 하 여 케이스에 대 한 정보를 표시 하려면 커서를 사례 이름 위에 가리킵니다. 누가 변경 했습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p114">The new case is displayed in the list of cases on the **eDiscovery** page. Note that you can hover the cursor over a case name to display information about the case, including the status of the case ( **Active** or **Closed**), the description of the case (that was created in the previous step), and when the case was changed last and who changed it.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="032a8-p115">새 사례를 만든 후에는 언제 든 지 이름을 바꿀 수 있습니다. **eDiscovery** 페이지에서 사례 이름을 클릭 하면 됩니다. **이 사례** 플라이 아웃 관리 페이지에서 **이름**아래의 상자에 표시 되는 이름을 변경 하 고 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p115">After you create a new case, you can rename it anytime. Just click the name of the case on the **eDiscovery** page. On the **Manage this case** flyout page, change the name displayed in the box under **Name**, and then save the change.</span></span> 
  
## <a name="step-3-add-members-to-a-case"></a><span data-ttu-id="032a8-173">3 단계: 사례에 구성원 추가</span><span class="sxs-lookup"><span data-stu-id="032a8-173">Step 3: Add members to a case</span></span>

<span data-ttu-id="032a8-p116">새 사례를 만든 후 다음 단계에서는 사례에 구성원을 추가 합니다. 앞에서 설명한 것 처럼 검토자 또는 eDiscovery 관리자 역할 그룹의 구성원 인 사용자만 사례 구성원으로 추가할 수 있습니다. 사례를 만든 eDiscovery 관리자는 구성원으로 자동 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p116">After you create a new case, the next step is to add members to the case. As previous explained, only users who are members of the Reviewer or eDiscovery Manager role groups can be added as members of the case. Note that the eDiscovery Manager who created the case is automatically added as a member.</span></span>
  
1. <span data-ttu-id="032a8-177">보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-177">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
2. <span data-ttu-id="032a8-178">구성원을 추가 하려는 사례 이름을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-178">Click the name of the case that you want to add members to.</span></span>
    
    <span data-ttu-id="032a8-179">**이 사례** 플라이 아웃 관리 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-179">The **Manage this case** flyout page is displayed.</span></span> 
    
    ![사례 플라이 아웃 관리 페이지](media/11f35ceb-6c98-4580-a3bc-ad688e9c7af9.png)
  
3. <span data-ttu-id="032a8-181">**구성원 관리**에서 add Icon ![](media/ITPro-EAC-AddIcon.gif) **추가** 를 클릭 하 여 서비스 케이스에 구성원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-181">Under **Manage members**, click ![Add Icon](media/ITPro-EAC-AddIcon.gif) **Add** to add members to the case.</span></span> 
    
    <span data-ttu-id="032a8-p117">또한 사례에 역할 그룹을 추가 하도록 선택할 수 있습니다. **역할 그룹 관리**에서 add 아이콘 ![](media/ITPro-EAC-AddIcon.gif) **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p117">You can also choose to add a role group to the case. Under **Manage role groups**, click ![Add Icon](media/ITPro-EAC-AddIcon.gif) **Add**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="032a8-p118">역할 그룹은 eDiscovery 사례에 구성원을 할당할 수 있는 사용자를 제어 합니다. 즉, 사용자가 구성원으로 속해 있는 역할 그룹을 사례에만 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p118">Role groups control who can assign members to an eDiscovery case. That means you can only assign the role groups that you are a member of to a case.</span></span>
    
4. <span data-ttu-id="032a8-186">사례 구성원으로 추가할 수 있는 사용자 또는 역할 그룹의 목록에서 추가할 사용자 또는 역할 그룹의 이름 옆에 있는 확인란을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-186">In the list of people or role groups that can be added as members of the case, click the check box next to the names of the people or role groups that you want to add.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="032a8-187">구성원으로 추가할 수 있는 사용자 목록이 많은 경우에는 **검색** 상자를 사용 하 여 목록에서 특정 사용자를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-187">If you have a large list of people who can added as members, use the **Search** box to search for a specific person in the list.</span></span> 
  
5. <span data-ttu-id="032a8-188">그룹의 구성원으로 추가할 사용자 또는 역할 그룹을 선택한 후 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-188">After you've selected the people or role groups to add as members of the group, click **Add**.</span></span>
    
    <span data-ttu-id="032a8-189">**이 사례 관리**에서 **저장** 을 클릭 하 여 사례 구성원의 새 목록을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-189">In **Manage this case**, click **Save** to save the new list of case members.</span></span> 
    
6. <span data-ttu-id="032a8-190">**저장** 을 클릭 하 여 사례 구성원의 새 목록을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-190">Click **Save** to save the new list of case members.</span></span> 
  
## <a name="step-4-place-content-locations-on-hold"></a><span data-ttu-id="032a8-191">4 단계: 콘텐츠 위치를 보류에 배치</span><span class="sxs-lookup"><span data-stu-id="032a8-191">Step 4: Place content locations on hold</span></span>

<span data-ttu-id="032a8-p119">eDiscovery 사례를 사용 하 여 사례와 관련이 있을 수 있는 콘텐츠를 보존 하는 보류를 만들 수 있습니다. 대/소문자를 custodians 하는 사용자의 사서함 및 비즈니스용 OneDrive 사이트에 대해 보류를 배치할 수 있습니다. 또한 Office 365 그룹의 그룹 사서함, SharePoint 사이트 및 비즈니스용 OneDrive 사이트에 보류할 수 있습니다. 마찬가지로 Microsoft 팀과 연결 된 사서함 및 사이트를 유지할 수 있습니다. 콘텐츠 위치를 보존 상태로 설정 하는 경우 콘텐츠 위치에서 보류를 제거 하거나 보류를 삭제할 때까지 콘텐츠가 보관 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p119">You can use an eDiscovery case to create holds to preserve content that might be relevant to the case. You can place a hold on the mailboxes and OneDrive for Business sites of people who are custodians in the case. You can also place a hold on the group mailbox, SharePoint site, and OneDrive for Business site for an Office 365 Group. Similarly, you can place a hold on the mailbox and site that are associated with Microsoft Teams. When you place content locations on hold, content is held until you remove the hold from the content location or until you delete the hold.</span></span>

> [!NOTE]
> <span data-ttu-id="032a8-197">콘텐츠 위치를 보존 상태로 설정 하 고 나면 보존을 적용 하는 데 최대 24 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-197">After you place a content location on hold, it takes up to 24 hours for the hold to take effect.</span></span> 
>   
<span data-ttu-id="032a8-198">보류를 만들 때 지정 된 콘텐츠 위치에 보관 되는 콘텐츠의 범위를 지정할 수 있는 옵션은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-198">When you create a hold, you have the following options to scope the content that is held in the specified content locations:</span></span>
  
- <span data-ttu-id="032a8-p120">모든 콘텐츠가 보류 되는 영구 보존을 만듭니다. 또는 검색 쿼리와 일치 하는 콘텐츠만 보존 되는 쿼리 기반 보류를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p120">You create an infinite hold where all content is placed on hold. Alternatively, you can create a query-based hold where only content that matches a search query is placed on hold.</span></span>
    
- <span data-ttu-id="032a8-p121">해당 날짜 범위 내에서 전송, 수신 또는 만든 콘텐츠만 저장 하는 날짜 범위를 지정할 수 있습니다. 또는 보내기, 수신 또는 만든 시기에 관계 없이 모든 콘텐츠를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p121">You can specify a date range to hold only the content that was sent, received, or created within that date range. Alternatively, you can hold all content regardless of when it was sent, received, or created.</span></span>
    
> [!NOTE]
> <span data-ttu-id="032a8-203">조직의 모든 eDiscovery 사례에 대해 최대 1만 개의 보존 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-203">You can have a maximum of 10,000 hold policies across all eDiscovery cases in your organization.</span></span> 
  
<span data-ttu-id="032a8-204">eDiscovery 사례에 대 한 보류를 만들려면</span><span class="sxs-lookup"><span data-stu-id="032a8-204">To create a hold for an eDiscovery case:</span></span>
  
1. <span data-ttu-id="032a8-205">보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-205">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
2. <span data-ttu-id="032a8-206">보류를 만들려는 사례 옆에 있는 **열기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-206">Click **Open** next to the case that you want to create the holds in.</span></span> 
    
3. <span data-ttu-id="032a8-207">이 사례에 대 한 **홈** 페이지에서 **보류** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-207">On the **Home** page for the case, click the **Hold** tab.</span></span> 
    
    ![보류 탭을 클릭 합니다.](media/3fef2db4-36de-4517-a34d-82f47b82d9bf.png)
  
4. <span data-ttu-id="032a8-209">**보류** ![페이지에서 아이콘](media/ITPro-EAC-AddIcon.gif) **만들기**추가를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-209">On the **Hold** page, click ![Add Icon](media/ITPro-EAC-AddIcon.gif) **Create**.</span></span>
    
5. <span data-ttu-id="032a8-p122">**보존 이름** 페이지에서 보류 이름을 지정 합니다. 보류의 이름은 조직 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p122">On the **Name your hold** page, give the hold a name. The name of the hold must be unique in your organization.</span></span> 
    
    ![보존에 고유한 이름을 지정 합니다.](media/7e15ea63-abd1-4f14-a29c-7ecfb9571d2c.png)
  
6. <span data-ttu-id="032a8-213">반드시 **설명** 상자에 보류에 대 한 설명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-213">(Optional) In the **Description** box, add a description of the hold.</span></span> 
    
7. <span data-ttu-id="032a8-214">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-214">Click **Next**.</span></span>
    
8. <span data-ttu-id="032a8-p123">보류 상태로 설정할 콘텐츠 위치를 선택 합니다. 사서함, 사이트 및 공용 폴더를 보류에 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p123">Choose the content locations that you want to place on hold. You can place mailboxes, sites, and public folders on hold.</span></span>
    
    ![보류 시킬 콘텐츠 위치 선택](media/a59e4265-9151-4dbf-913f-6a4ab8db06b4.png)
  
   <span data-ttu-id="032a8-p124">**전자 메일 교환** - **사용자, 그룹 또는 팀 선택을** 클릭 한 다음 **사용자, 그룹 또는 팀** 선택을 클릭 합니다. 보류할 사서함을 지정 합니다. 검색 상자를 사용 하 여 사용자 사서함과 메일 그룹 (그룹 구성원의 사서함을 보류)을 보류 상태로 설정 합니다. Office 365 그룹 또는 Microsoft 팀에 대 한 연결 된 사서함을 보류할 수도 있습니다. 사용자, 그룹, 팀 확인란을 선택 하 고 **선택을**클릭 한 후 **완료**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p124">a. **Exchange email** - Click **Choose users, groups, or teams** and then click **Choose users, groups, or teams** again. to specify mailboxes to place on hold. Use the search box to find user mailboxes and distribution groups (to place a hold on the mailboxes of group members) to place on hold. You can also place a hold on the associated mailbox for an Office 365 Group or a Microsoft Team. Select the user, group, team check box, click **Choose**, and then click **Done**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="032a8-p125">**사용자, 그룹 또는 팀 선택을** 클릭 하 여 보류 중인 사서함을 지정 하는 경우 표시 되는 사서함 선택은 비어 있습니다. 이는 성능 향상을 위해 설계 된 것입니다. 이 목록에 사용자를 추가 하려면 검색 상자에 이름 (최소 3 자)을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p125">When you click **Choose users, groups, or teams** to specify mailboxes to place on hold, the mailbox picker that's displayed is empty. This is by design to enhance performance. To add people to this list, type a name (a minimum of 3 characters) in the search box.</span></span> 
  
   <span data-ttu-id="032a8-p126">b. **sharepoint 사이트** - **사이트 선택을** 클릭 한 다음 **사이트 선택을** 다시 클릭 하 여 SharePoint 및 비즈니스용 OneDrive 사이트를 보류로 지정 합니다. 보류 하도록 설정할 각 사이트의 URL을 입력 합니다. 또한 Office 365 그룹 또는 Microsoft 팀에 대 한 SharePoint 사이트의 URL을 추가할 수 있습니다. **선택을**클릭 하 고 **완료**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p126">b. **SharePoint Sites** - Click **Choose sites** and then click **Choose sites** again to specify SharePoint and OneDrive for Business sites to place on hold. Type the URL for each site that you want to place on hold. You can also add the URL for the SharePoint site for an Office 365 Group or a Microsoft Team. Click **Choose**, and then click **Done**.</span></span>
    
    <span data-ttu-id="032a8-232">Office 365 그룹 및 Microsoft 팀을 보류 하는 방법에 대 한 팁을 보려면 [추가 정보](#more-information) 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="032a8-232">See the [More information](#more-information) section for tips on putting Office 365 Groups and Microsoft Teams on hold.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="032a8-p127">드문 경우 이지만 사용자의 upn (사용자 계정 이름)이 변경 되는 경우에는 해당 OneDrive 계정에 대 한 URL도 새 UPN을 통합 하도록 변경 됩니다. 이 경우에는 사용자의 새 OneDrive URL을 추가 하 고 이전 항목을 제거 하 여 보류를 수정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p127">In the rare case that a person's user principal name (UPN) is changed, the URL for their OneDrive account will also be changed to incorporate the new UPN. If this happens, you'll have to modify the hold by adding the user's new OneDrive URL and removing the old one.</span></span> 
  
   <span data-ttu-id="032a8-p128">c. **exchange 공용 폴더** -exchange Online 조직의 모든 공용 ![폴더를](media/963dfcd0-1765-4306-bcce-c3008c4406b9.png) 보류 상태로 전환 하려면 toggle switch toggle control을 **all** 위치로 이동 합니다. 특정 공용 폴더를 선택 하 여 보류 상태로 설정할 수는 없습니다. 공용 폴더를 보존 하지 않으려면 toggle 스위치를 **"없음"** 으로 설정 된 상태로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p128">c. **Exchange public folders** - Move the toggle switch ![Toggle control](media/963dfcd0-1765-4306-bcce-c3008c4406b9.png) to the **All** position to put all public folders in your Exchange Online organization on hold. Note that you can't choose specific public folders to put on hold. Leave the toggle switch set to **None** if you don't want to put a hold on public folders.</span></span>
    
9. <span data-ttu-id="032a8-239">보류에 콘텐츠 위치를 모두 추가한 후에 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-239">When you're done adding content locations to the hold, click **Next**.</span></span>
    
10. <span data-ttu-id="032a8-p129">조건을 사용 하 여 쿼리 기반 보존을 만들려면 다음을 완료 합니다. 그렇지 않고 **다음** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p129">To create a query-based hold with conditions, complete the following. Otherwise, just click **Next**</span></span>
    
    ![조건을 사용 하 여 쿼리 기반 보류 만들기](media/d587b58e-d05c-4ac0-b0fe-09019e4f1063.png)
  
    
       <span data-ttu-id="032a8-p130">a: **키워드**아래의 상자에 검색 조건을 충족 하는 콘텐츠만 저장 되도록 상자에 검색 쿼리를 입력 합니다. 키워드, 메시지 속성 또는 문서 속성 (예: 파일 이름)을 지정할 수 있습니다. **AND**, **OR**, **NOT**등의 부울 연산자를 사용 하 여 보다 복잡 한 쿼리를 사용할 수도 있습니다. 키워드 상자를 비워 두면 지정 된 콘텐츠 위치에 있는 모든 콘텐츠가 보류 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p130">a. In the box under **Keywords**, type a search query in the box so that only the content that meets the search criteria is placed on hold. You can specify keywords, message properties, or document properties, such as file names. You can also use more complex queries that use a Boolean operator, such as **AND**, **OR**, or **NOT**. If you leave the keyword box empty, then all content located in the specified content locations will be placed on hold.</span></span>
    
    <span data-ttu-id="032a8-p131">b. 아이콘](media/ITPro-EAC-AddIcon.gif) 추가 ![ **조건** 추가를 클릭 하 여 보류에 대 한 검색 쿼리 범위를 좁히는 조건을 하나 이상 추가 합니다. 각 조건은 보류를 만들 때 만들어지고 실행 되는 KQL 검색 쿼리에 절을 추가 합니다. 예를 들어 날짜 범위를 지정 하 여 원거리 시간 내에 만들어진 전자 메일 또는 사이트 문서를 보류할 수 있습니다. 조건은 **AND** 연산자에 의해 키워드 상자에 지정 된 키워드 쿼리에 논리적으로 연결 됩니다. 즉, 항목이 유지 되도록 키워드 쿼리와 조건을 모두 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p131">b. Click ![Add Icon](media/ITPro-EAC-AddIcon.gif) **Add conditions** to add one or more conditions to narrow the search query for the hold. Each condition adds a clause to the KQL search query that is created and run when you create the hold. For example you can specify a date range so that email or site documents that were created within the date ranged are placed on hold. A condition is logically connected to the keyword query (specified in the keyword box) by the **AND** operator. That means that items have to satisfy both the keyword query and the condition to be placed on hold.</span></span>

    <span data-ttu-id="032a8-254">검색 쿼리를 만들고 조건을 사용 하는 방법에 대 한 자세한 내용은 [키워드 쿼리 및 검색 조건을](keyword-queries-and-search-conditions.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="032a8-254">For more information about creating a search query and using conditions, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
    
11. <span data-ttu-id="032a8-255">쿼리 기반 보존을 구성한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-255">After configuring a query-based hold, click **Next**.</span></span>
    
12. <span data-ttu-id="032a8-256">설정을 검토 하 고 **이 보류 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-256">Review your settings, and then click **Create this hold**.</span></span>
    
### <a name="hold-statistics"></a><span data-ttu-id="032a8-257">보류 통계</span><span class="sxs-lookup"><span data-stu-id="032a8-257">Hold statistics</span></span>

<span data-ttu-id="032a8-p132">잠시 후 새로 보존에 대 한 정보는 선택 된 보류에 대 한 **보류** 페이지의 세부 정보 창에 표시 됩니다. 이 정보에는 보류 중인 사서함 및 사이트의 수와 보류 중인 항목의 총 수와 크기, 보류 통계가 계산 된 마지막 시간 등이 포함 됩니다. 이러한 보존 통계를 통해 eDiscovery 사례와 관련 된 콘텐츠의 양에 대 한 정보를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p132">After a while, information about the new hold is displayed in the details pane on the **Holds** page for the selected hold. This information includes the number of mailboxes and sites on hold and statistics about the content that was placed on hold, such as the total number and size of items placed on hold and the last time the hold statistics were calculated. These hold statistics help you identify how much content that's related to the eDiscovery case is being held.</span></span> 
  
![보류 통계](media/575cfe0a-9210-4ae4-8df8-65665d66712e.png)
  
<span data-ttu-id="032a8-262">보류 통계에 대해서는 다음 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-262">Keep the following things in mind about hold statistics:</span></span>
  
- <span data-ttu-id="032a8-p133">보류 중인 총 항목 수는 보류 된 모든 콘텐츠 원본의 항목 수를 나타냅니다. 쿼리 기반 보존을 만든 경우이 통계는 쿼리와 일치 하는 항목의 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p133">The total number of items on hold indicates the number of items from all content sources that are placed on hold. If you've created a query-based hold, this statistic indicates the number of items that match the query.</span></span>
    
- <span data-ttu-id="032a8-p134">보류 중인 항목 수에는 콘텐츠 위치에 있는 인덱싱되지 않은 항목도 포함 됩니다. 쿼리 기반 보존을 만드는 경우에는 콘텐츠 위치에 있는 모든 인덱싱되지 않은 항목이 보류에 저장 됩니다. 여기에는 날짜 범위 조건 외부에 있을 수 있는 쿼리 기반 보류 및 인덱싱되지 않은 항목의 검색 조건과 일치 하지 않는 인덱싱되지 않은 항목이 포함 됩니다. 이는 검색 쿼리와 일치 하지 않거나 날짜 범위에서 제외 된 인덱싱되지 않은 항목이 검색 결과에 포함 되지 않는 콘텐츠 검색을 실행할 때 일어나는 것과는 다릅니다. 인덱싱되지 않은 항목에 대 한 자세한 내용은 [Office 365의 콘텐츠 검색에서 부분적으로 인덱싱된 항목](partially-indexed-items-in-content-search.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="032a8-p134">The number of items on hold also includes unindexed items found in the content locations. Note that if you create a query-based hold, all unindexed items in the content locations are placed on hold. This includes unindexed items that don't match the search criteria of a query-based hold and unindexed items that might fall outside of a date range condition. This is different than what happens when you run a Content Search, in which unindexed items that don't match the search query or are excluded by a date range condition aren't included in the search results. For more information about unindexed items, see [Partially indexed items in Content Search in Office 365](partially-indexed-items-in-content-search.md).</span></span>
    
- <span data-ttu-id="032a8-p135">**통계 업데이트** 를 클릭 하 여 보류 중인 항목 수를 계산 하는 검색 예측을 다시 실행 하 여 최신 보존 통계를 가져올 수 있습니다. 필요한 경우 도구 모음에서 새로 고침](media/O365-MDM-Policy-RefreshIcon.gif) **새로 고침**![아이콘을 클릭 하 여 세부 정보 창에서 보류 통계를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p135">You can get the latest hold statistics by clicking **Update statistics** to re-run a search estimate that calculates the current number of items on hold. If necessary, click **Refresh**![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) in the toolbar to update the hold statistics in the details pane.</span></span> 
    
- <span data-ttu-id="032a8-272">사서함 이나 사이트가 보류 중인 사용자가 새 전자 메일 메시지를 보내거나 받고 새 SharePoint 및 비즈니스용 OneDrive 문서를 만드는 경우에는 보존 되는 항목의 수가 시간에 따라 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-272">It's normal for the number of items on hold to increase over time because users whose mailbox or site is on hold are typically sending or receiving new email message and creating new SharePoint and OneDrive for Business documents.</span></span>
    
> [!NOTE]
> <span data-ttu-id="032a8-p136">SharePoint 사이트 또는 OneDrive 계정을 다중 지리적 환경에서 다른 지역으로 이동 하는 경우 해당 사이트에 대 한 통계가 보존 통계에 포함 되지 않습니다. 하지만 사이트의 콘텐츠는 계속 유지 됩니다. 또한 사이트가 다른 지역으로 이동 되는 경우 보류에 표시 되는 URL은 업데이트 되지 않습니다. 보류를 편집 하 고 URL을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p136">If a SharePoint site or OneDrive account is moved to a different region in a multi-geo environment, the statistics for that site won't be included in the hold statistics. However, the content in the site will still be on hold. Also, if a site is moved to a different region the URL that's displayed in the hold will not be updated. You'll have to edit the hold and update the URL.</span></span> 
  
## <a name="step-5-create-and-run-a-content-search-associated-with-a-case"></a><span data-ttu-id="032a8-277">5 단계: 사례와 연결 된 콘텐츠 검색 만들기 및 실행</span><span class="sxs-lookup"><span data-stu-id="032a8-277">Step 5: Create and run a Content Search associated with a case</span></span>

<span data-ttu-id="032a8-p137">eDiscovery 사례를 만들고 사례와 관련 된 모든 custodians 보존 상태로 설정 되 면 사례와 연결 된 콘텐츠 검색을 하나 이상 만들고 실행할 수 있습니다. 사례와 연결 된 콘텐츠 검색은 보안 &amp; 및 준수 센터의 **검색** 페이지에 표시 되지 않습니다. 즉, 사례와 연결 된 콘텐츠 검색은 eDiscovery 관리자 역할 그룹의 구성원 인 경우에만 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p137">After an eDiscovery case is created and any custodians related to the case are placed on hold, you can create and run one or more Content Searches that are associated with the case. Content Searches associated with a case aren't listed on the **Search** page in the Security &amp; Compliance Center. This means that Content Searches associated with a case can only be accessed by case members who are also members of the eDiscovery Manager role group.</span></span> 
  
1. <span data-ttu-id="032a8-281">보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-281">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
2. <span data-ttu-id="032a8-282">콘텐츠 검색을 만들려는 사례 옆에 있는 **열기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-282">Click **Open** next to the case that you want to create a Content Search in.</span></span> 
    
3. <span data-ttu-id="032a8-283">사례에 대 한 **홈** 페이지에서 **검색** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-283">On the **Home** page for the case, click the **Search** tab.</span></span> 
    
    ![검색 탭](media/2e15fe32-1a2e-4588-ad0b-5d96f77cece9.png)
  
4. <span data-ttu-id="032a8-285">**검색** 페이지에서 ![](media/ITPro-EAC-AddIcon.gif) **새 검색**아이콘 추가를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-285">On the **Search** page, click ![Add Icon](media/ITPro-EAC-AddIcon.gif) **New search**.</span></span> 
    
5. <span data-ttu-id="032a8-286">**새 검색** 페이지에서 키워드 및 조건을 추가하여 검색 쿼리를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-286">On the **New search** page, you can add keywords and conditions to create the search query.</span></span> 
    
    ![새 검색](media/0e9954e7-c0ea-4e05-820b-e4b81dc5f81d.png)
  
6. <span data-ttu-id="032a8-p138">키워드, 메시지 속성 (예: 보낸 날짜 및 받은 날짜가) 또는 문서 속성 (예: 파일 이름 또는 문서를 마지막으로 변경한 날짜)을 지정할 수 있습니다. **AND**, **OR**, **NOT**, **NEAR**또는 **onear**와 같은 부울 연산자를 사용 하는 보다 복잡 한 쿼리를 사용할 수 있습니다. 문서에서 중요 한 정보 (예: 주민 등록 번호)를 검색 하거나 외부에서 공유한 문서를 검색할 수도 있습니다. 키워드 상자를 비워 두면 지정 된 콘텐츠 위치에 있는 모든 콘텐츠가 검색 결과에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p138">You can specify keywords, message properties, such as sent and received dates, or document properties, such as file names or the date that a document was last changed. You can use more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, **NEAR**, or **ONEAR**. You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally. If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span> 
    
7. <span data-ttu-id="032a8-p139">**키워드 목록 표시** 확인란을 클릭 하 고 각 행에 키워드를 입력할 수 있습니다. 이 경우 각 행의 키워드는 생성 된 검색 쿼리의 **OR** 연산자로 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p139">You can click the **Show keyword list** check box and the type a keyword in each row. If you do this, the keywords on each row are connected by the **OR** operator in the search query that's created.</span></span> 
    
    ![키워드 목록](media/29cceb5d-2817-4fc4-b91a-ced1c5824a17.png)
  
    <span data-ttu-id="032a8-p140">키워드 목록을 사용 하는 이유 각 키워드와 일치 하는 항목의 수를 보여 주는 통계를 가져올 수 있습니다. 이를 통해 가장 효과적이 고 효과적인 키워드를 빠르게 확인할 수 있습니다. 행에 괄호를 사용 하 여 키워드로 묶은 키워드 구를 사용할 수도 있습니다. 검색 통계에 대 한 자세한 내용은 [콘텐츠 검색 결과에 대 한 키워드 통계 보기](view-keyword-statistics-for-content-search.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="032a8-p140">Why use the keyword list? You can get statistics that show how many items match each keyword. This can help you quickly identify which keywords are the most (and least) effective. You can also use a keyword phrase (surrounded by parentheses) in a row. For more information about search statistics, see [View keyword statistics for Content Search results](view-keyword-statistics-for-content-search.md).</span></span>
    
    <span data-ttu-id="032a8-300">키워드 목록을 사용 하는 방법에 대 한 자세한 내용은 [검색 쿼리 작성](content-search.md#building-a-search-query)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="032a8-300">For more information about using the keywords list, see [Building a search query](content-search.md#building-a-search-query).</span></span>
    
8. <span data-ttu-id="032a8-p141">**조건**에서 검색 쿼리에 조건을 추가 하 여 검색 범위를 좁히고 보다 구체화 된 결과 집합을 반환 합니다. 각 조건은 검색을 시작할 때 만들어지고 실행 되는 KQL 검색 쿼리에 절을 추가 합니다. 조건은 **AND** 연산자에 의해 키워드 상자에 지정 된 키워드 쿼리에 논리적으로 연결 됩니다. 즉, 항목은 결과에 포함할 키워드 쿼리와 조건을 모두 만족 해야 합니다. 조건에 따라 결과의 범위를 좁히는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p141">Under **Conditions**, add conditions to a search query to narrow a search and return a more refined set of results. Each condition adds a clause to the KQL search query that is created and run when you start the search. A condition is logically connected to the keyword query (specified in the keyword box) by the **AND** operator. That means that items have to satisfy both the keyword query and the condition to be included in the results. This is how conditions help to narrow your results.</span></span> 
    
    <span data-ttu-id="032a8-306">검색 쿼리를 만들고 조건을 사용하는 방법에 대한 자세한 내용은 [Keyword queries for Content Search](keyword-queries-and-search-conditions.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="032a8-306">For more information about creating a search query and using conditions, see [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).</span></span>
    
9. <span data-ttu-id="032a8-p142">**위치: 보류 중인 위치**에서 검색 하려는 콘텐츠 위치를 선택 합니다. 같은 검색에서 사서함, 사이트 및 공용 폴더를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p142">Under **Locations: locations on hold**, choose the content locations that you want to search. You can search mailboxes, sites, and public folders in the same search.</span></span>
    
    ![위치, 보류 중인 위치](media/d56398aa-0b20-4500-8e26-494eab92a99f.png)
  
    - <span data-ttu-id="032a8-p143">**모든 위치** -조직의 모든 콘텐츠 위치를 검색 하려면이 옵션을 선택 합니다. 이 옵션을 선택 하면 모든 office 365 그룹 및 microsoft 팀의 사서함을 포함 하는 모든 Exchange 사서함, 모든 SharePoint 및 비즈니스용 OneDrive 사이트 (모든 office 365 그룹 및 Microsoft의 사이트 포함)를 검색 하도록 선택할 수 있습니다. 팀) 및 모든 공용 폴더</span><span class="sxs-lookup"><span data-stu-id="032a8-p143">**All locations** - Select this option to search all content locations in your organization. When you select this option, you can choose to search all Exchange mailboxes (which includes the mailboxes for all Office 365 Groups and Microsoft Teams), all SharePoint and OneDrive for Business sites (which includes the sites for all Office 365 Groups and Microsoft Teams), and all public folders.</span></span>
    
    - <span data-ttu-id="032a8-p144">**보류의 모든 위치** -사례에서 보류 된 모든 콘텐츠 위치를 검색 하려면이 옵션을 선택 합니다. 사례에 여러 보류가 포함 되어 있는 경우이 옵션을 선택 하면 모든 보류의 콘텐츠 위치가 검색 됩니다. 또한 콘텐츠 위치가 쿼리 기반 유지로 설정 된 경우에는이 단계에서 만드는 콘텐츠 검색을 실행할 때 보류 중인 항목만 검색 됩니다. 예를 들어 특정 날짜 이전에 보내거나 만든 항목을 보존 하는 쿼리 기반 사례 보류에 사용자를 추가한 경우 콘텐츠 검색의 검색 조건을 사용 하 여 해당 항목만 검색 됩니다. 이 작업은 사례 보류 쿼리와 콘텐츠 검색 쿼리를 **and** 연산자로 연결 하 여 수행 됩니다. 사례 콘텐츠를 검색 하는 방법에 대 한 자세한 내용은이 문서 끝부분의 [추가 정보](ediscovery-cases.md#moreinfo_1) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="032a8-p144">**All locations on hold** - Select this option to search all the content locations that have been placed on hold in the case. If the case contains multiple holds, the content locations from all holds will be searched when you select this option. Additionally, if a content location was placed on a query-based hold, only the items that are on hold will be searched when you run the content search that you're creating in this step. For example, if a user was placed on query-based case hold that preserves items that were sent or created before a specific date, only those items would be searched by using the search criteria of the content search. This is accomplished by connecting the case hold query and the content search query by an **AND** operator. See the [More information](ediscovery-cases.md#moreinfo_1) section at the end of this article for more details about searching case content.</span></span> 
    
    - <span data-ttu-id="032a8-p145">**특정 위치** -검색 하려는 사서함 및 사이트를 선택 하려면이 옵션을 선택 합니다. 이 옵션을 선택 하 고 **수정을**클릭 하면 위치 목록이 표시 됩니다. 모든 사용자, 그룹, 팀 또는 사이트 위치를 검색 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p145">**Specific locations** - Select this option to select the mailboxes and sites that you want to search. When you select this option and click **Modify**, a list of locations appears. You can choose to search any or all users, groups, teams, or site locations.</span></span>
    
      ![특정 위치 선택](media/97469b15-7be1-4aee-be27-f8343636152c.png)
  
      <span data-ttu-id="032a8-p146">조직의 모든 공용 폴더를 검색 하도록 선택할 수도 있지만이 옵션을 선택 하 고 보류 중인 모든 콘텐츠 위치를 검색 하는 경우 쿼리 기반 사례 보류의 쿼리는 검색 쿼리에 적용 되지 않습니다. 즉, 쿼리 기반 사례 보류에 의해 보존 되는 콘텐츠 뿐 아니라 위치에 있는 모든 콘텐츠가 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p146">You can also choose to search all public folders in your organization, but if you select this option and search any content location that's on hold, any query from a query-based case hold won't be applied to the search query. In other words, all content in a location is searched, not just the content that is preserved by a query-based case hold.</span></span>
    
      <span data-ttu-id="032a8-p147">미리 채워진 사례 콘텐츠 위치를 제거 하거나 새를 추가할 수 있습니다. 이 옵션을 선택 하면 모든 Exchange 사서함을 검색 하는 등 특정 서비스에 대 한 모든 콘텐츠 위치를 검색 하거나 특정 콘텐츠 위치를 서비스에 대해 검색할 수 있습니다. 또한 조직의 공용 폴더 검색 여부를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p147">You can remove the pre-populated case content locations or add new ones. If you choose this option, you also have flexibility to search all content locations for a specific service (such as searching all Exchange mailboxes) or you can search specific content locations for a service. You can also choose whether or not to search the public folders in your organization.</span></span>
    
      <span data-ttu-id="032a8-327">검색할 콘텐츠 위치를 추가할 때는 다음 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-327">Keep these things in mind when adding content locations to search:</span></span>
    
      - <span data-ttu-id="032a8-p148">**사용자, 그룹 또는 팀 선택을** 클릭 하 여 검색할 사서함을 지정 하는 경우 표시 되는 사서함 선택은 비어 있습니다. 이는 성능 향상을 위해 설계 된 것입니다. 이 목록에 받는 사람을 추가 하려면 **사용자, 그룹 또는 팀 선택을**클릭 하 고 검색 상자에 이름 (최소 3 자)을 입력 한 후에 이름 옆의 확인란을 선택 하 고 **선택을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p148">When you click **Choose users, groups, or teams** to specify mailboxes to search, the mailbox picker that's displayed is empty. This is by design to enhance performance. To add recipients to this list, click **Choose users, groups, or teams**, type a name (a minimum of 3 characters) in the search box, select the check box next to the name, and then click **Choose**.</span></span> 
    
      - <span data-ttu-id="032a8-p149">비활성 사서함, Office 365 그룹, Microsoft 팀 및 메일 그룹을 검색할 사서함 목록에 추가할 수 있습니다. 동적 메일 그룹은 지원 되지 않습니다. Office 365 그룹 또는 Microsoft 팀을 추가 하는 경우 그룹 또는 팀 사서함이 검색 됩니다. 그룹 구성원의 사서함이 검색 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p149">You can add inactive mailboxes, Office 365 Groups, Microsoft Teams, and distribution groups to the list of mailboxes to search. Dynamic distribution groups aren't supported. If you add Office 365 Groups or Microsoft Teams, the group or team mailbox is searched; the mailboxes of the group members aren't searched.</span></span>
    
      - <span data-ttu-id="032a8-p150">사이트를 추가 하려면 **사이트 선택을**클릭 하 고 **사이트 선택을** 다시 클릭 한 다음 검색할 각 사이트에 대 한 URL을 입력 합니다. Office 365 그룹 및 Microsoft 팀의 SharePoint 사이트에 대 한 URL을 추가할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p150">To add sites click **Choose sites**, click **Choose sites** again, and then type the URL for each site that you want to search. You can also add the URL for the SharePoint site for Office 365 Groups and Microsoft Teams.</span></span> 
    
10. <span data-ttu-id="032a8-336">검색할 콘텐츠 위치를 선택한 후 **완료** 를 클릭 하 고 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-336">After you select the content locations to search, click **Done** and then click **Save**.</span></span>
    
11. <span data-ttu-id="032a8-p151">**새 검색** 페이지에서 **저장** 을 클릭 하 고 검색의 이름을 입력 합니다. 사례와 연결 된 콘텐츠 검색은 Office 365 조직 내에서 고유한 이름을 가져야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p151">On the **New search** page, click **Save** and then type a name for the search. Content Searches associated with a case must have names that are unique within your Office 365 organization.</span></span> 
    
12. <span data-ttu-id="032a8-339">\*\*실행 저장 &amp; \*\* 을 클릭 하 여 검색 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-339">Click **Save &amp; run** to save the search settings.</span></span> 
    
13. <span data-ttu-id="032a8-340">검색을 위한 고유한 이름을 입력 하 고 **저장** 을 클릭 하 여 검색을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-340">Enter a unique name for the search, and click **Save** to start the search.</span></span> 
    
    <span data-ttu-id="032a8-p152">검색이 시작 됩니다. 잠시 후 세부 정보 창에 검색 결과가 예상 대로 표시 됩니다. 예상에는 검색 조건과 일치 하는 항목의 총 크기와 개수가 포함 됩니다. 검색 예측에는 검색 된 콘텐츠 위치에 있는 인덱싱되지 않은 항목의 수도 포함 됩니다. 검색 조건을 충족 하지 않는 인덱싱되지 않은 항목의 수는 세부 정보 창에 표시 되는 검색 통계에 포함 됩니다. 인덱싱되지 않은 항목이 검색 쿼리와 일치 하는 경우 (다른 메시지 또는 문서 속성이 검색 조건을 충족 함) 해당 항목은 초과 된 인덱싱되지 않은 항목 수에 포함 되지 않습니다. 인덱싱되지 않은 항목이 검색 기준으로 제외 되는 경우 인덱싱되지 않은 항목의 추정값에도 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p152">The search begins. After a while, an estimate of the search results is displayed in the details pane. The estimate includes the total size and number of items that matched the search criteria. The search estimate also includes the number of unindexed items in the content locations that were searched. The number of unindexed items that don't meet the search criteria will be included in the search statistics displayed in the details pane. If an unindexed item matches the search query (because other message or document properties meet the search criteria), it won't be included in the estimated number of unindexed items. If an unindexed item is excluded by the search criteria, it also won't be included in the estimate of unindexed items.</span></span>
    
  <span data-ttu-id="032a8-p153">검색이 완료 되 면 검색 결과를 미리 볼 수 있습니다. 필요한 경우 새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로 고침**![을 클릭 하 여 세부 정보 창에서 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p153">After the search is completed, you can preview the search results. If necessary, click **Refresh**![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
## <a name="step-6-export-the-results-of-a-content-search-associated-with-a-case"></a><span data-ttu-id="032a8-350">6 단계: 사례와 연결 된 콘텐츠 검색 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="032a8-350">Step 6: Export the results of a Content Search associated with a case</span></span>

<span data-ttu-id="032a8-p154">검색을 성공적으로 실행 한 후에는 검색 결과를 내보낼 수 있습니다. 검색 결과를 내보낼 때 사서함 항목은 PST 파일이 나 개별 메시지로 다운로드 됩니다. SharePoint 및 비즈니스용 OneDrive 사이트에서 콘텐츠를 내보낼 때 기본 Office 문서 및 기타 문서의 복사본이 내보내집니다. 모든 검색 결과에 대 한 정보를 포함 하는 매니페스트 파일 (XML 형식)도 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p154">After a search is successfully run, you can export the search results. When you export search results, mailbox items are downloaded in PST files or as individual messages. When you export content from SharePoint and OneDrive for Business sites, copies of native Office documents and other documents are exported. A manifest file (in XML format) that contains information about every search result is also exported.</span></span>
  
<span data-ttu-id="032a8-355">[사례와 연결 된 단일 검색](ediscovery-cases.md#singlesearch_1) 결과 내보내기 결과를 내보내거나 [사례와 연결 된 여러 검색의](ediscovery-cases.md#multiplesearches_1)결과를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-355">You can export the results of a [Export the results of a single search associated with a case](ediscovery-cases.md#singlesearch_1) or you can export the results of [Export the results of multiple searches associated with a case](ediscovery-cases.md#multiplesearches_1).</span></span>
  
### <a name="export-the-results-of-a-single-search-associated-with-a-case"></a><span data-ttu-id="032a8-356">사례와 연결 된 단일 검색 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="032a8-356">Export the results of a single search associated with a case</span></span>

1. <span data-ttu-id="032a8-357">보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-357">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
2. <span data-ttu-id="032a8-358">검색을 내보내려는 사례 옆에 있는 **열기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-358">Click **Open** next to the case that you want to export search from.</span></span> 
    
3. <span data-ttu-id="032a8-359">사례에 대 한 **홈** 페이지에서 **검색**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-359">On the **Home** page for the case, click **Search**.</span></span>
    
4. <span data-ttu-id="032a8-360">사례에 대 한 검색 목록에서 검색 결과를 내보내려는 검색을 클릭 하 고 검색 결과 내보내기 아이콘 ![](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \*\*\*\* 을 클릭 한 다음 드롭다운 목록에서 **결과 내보내기를** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-360">In the list of searches for the case, click the search that you want to export search results from, click ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **More**, and then select **Export results** from the drop-down list.</span></span> 
    
    <span data-ttu-id="032a8-361">**결과 내보내기** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-361">The **Export results** page is displayed.</span></span> 
    
    ![내보내기 결과 페이지](media/ab0bb46d-310b-4374-8644-717146df6676.png)
  
    <span data-ttu-id="032a8-p155">사례와 연결 된 콘텐츠 검색 결과를 내보낼 워크플로는 **콘텐츠 검색** 페이지에서 검색에 대 한 검색 결과를 내보내는 것과 같습니다. 단계별 지침은 [Office 365 보안 &amp; 및 준수 센터에서 콘텐츠 검색 결과 내보내기를](export-search-results.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="032a8-p155">The workflow to export the results from a Content Search associated with a case is that same as exporting the search results for a search on the **Content search** page. For step-by-step instructions, see [Export Content Search results from the Office 365 Security &amp; Compliance Center](export-search-results.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="032a8-p156">검색 결과를 내보낼 때는 검색 된 사서함에서 같은 메시지의 인스턴스가 여러 개 발견 된 경우에도 전자 메일 메시지의 복사본 하나만 내보내도록 하는 옵션을 사용할 수 있습니다. 복제 제거 및 중복 항목이 식별 되는 방식에 대 한 자세한 내용은 [eDiscovery 검색 결과의 중복](de-duplication-in-ediscovery-search-results.md)제거를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="032a8-p156">When you export search results, you have the option to enable de-duplication so that only one copy of an email message is exported even though multiple instances of the same message might have been found in the mailboxes that were searched. For more information about de-duplication and how duplicate items are identified, see [De-duplication in eDiscovery search results](de-duplication-in-ediscovery-search-results.md).</span></span> 
  
5. <span data-ttu-id="032a8-367">**내보내기** 탭을 클릭 하 여 해당 사례에 대해 존재 하는 내보내기 작업 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-367">Click the **Export** tab to display the list of export jobs that exist for that case.</span></span> 
    
    ![내보내기 탭](media/1b84c45e-4ec9-4ecd-9e07-eaf8fc4cc307.png)
  
    <span data-ttu-id="032a8-p157">새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로 고침**![을 클릭 하 여 방금 만든 내보내기 작업이 표시 되도록 내보내기 작업 목록을 업데이트 해야 할 수 있습니다. 내보내기 작업의 이름은 검색의 끝에 추가 하는 **export** 가 포함 된 해당 콘텐츠 검색과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p157">You might have to click **Refresh**![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the list of export jobs so that it shows the export job that you just created. Note that export jobs have the same name as the corresponding Content Search with **_Export** appended to the end of search name.</span></span> 
    
6. <span data-ttu-id="032a8-p158">방금 만든 내보내기 작업을 클릭 하 여 세부 정보 창에 상태 정보를 표시 합니다. 이 정보에는 Microsoft 클라우드에서 Azure 저장소 영역으로 전송 된 항목의 백분율이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p158">Click the export job that you just created to display status information in the details pane. This information includes the percentage of items that have been transferred to an Azure storage area in the Microsoft cloud.</span></span>
    
    <span data-ttu-id="032a8-p159">모든 항목을 전송 하 고 나면 **결과 다운로드** 를 클릭 하 여 로컬 컴퓨터에 검색 결과를 다운로드 합니다. 자세한 내용은 [Export Content Search results from the Office 365 보안 &amp; 및 준수 센터](export-search-results.md) 의 2 단계를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="032a8-p159">After all items have been transferred, click **Download results** to download the search results to your local computer. For more information, see Step 2 in [Export Content Search results from the Office 365 Security &amp; Compliance Center](export-search-results.md)</span></span>
    
### <a name="export-the-results-of-multiple-searches-associated-with-a-case"></a><span data-ttu-id="032a8-375">사례와 연결 된 여러 검색 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="032a8-375">Export the results of multiple searches associated with a case</span></span>

<span data-ttu-id="032a8-p160">사례와 관련 된 단일 콘텐츠 검색 결과를 내보내는 대신 단일 내보내기에서 여러 검색의 결과를 동일한 대/소문자로 내보낼 수 있습니다. 결과를 한 번에 하나씩 내보내는 것 보다 여러 검색의 결과를 내보낼 때 보다 빠르고 쉽게 작업할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p160">As an alternative to exporting the results of a single Content Search associated with a case, you can export the results of multiple searches from the same case in a single export. Exporting the results of multiple searches is faster and easier than exporting the results one search at a time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="032a8-p161">검색 중 하나가 모든 케이스 콘텐츠를 검색 하도록 구성 된 경우에는 여러 검색의 결과를 내보낼 수 없습니다. eDiscovery 사례와 연결 된 검색에 대해서만 여러 검색의 결과를 내보냅니다. 보안 &amp; 및 준수 센터의 **콘텐츠 검색** 페이지에 나열 된 여러 검색 결과를 내보낼 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p161">You can't export the results of multiple searches if one of those searches was configured to search all case content. only export the results of multiple searches for searches that are associated with an eDiscovery case. You can't export the results of multiple searches listed on the **Content search** page in the Security &amp; Compliance Center.</span></span> 
  
1. <span data-ttu-id="032a8-381">보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-381">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
2. <span data-ttu-id="032a8-382">검색 결과를 내보내려는 사례 옆에 있는 **열기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-382">Click **Open** next to the case that you want to export search results from.</span></span> 
    
3. <span data-ttu-id="032a8-383">사례에 대 한 **홈** 페이지에서 **검색**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-383">On the **Home** page for the case, click **Search**.</span></span>
    
4. <span data-ttu-id="032a8-384">사례에 대 한 검색 목록에서 검색 결과를 내보내려는 검색을 두 개 이상 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-384">In the list of searches for the case, select two or more searches that you want to export search results from.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="032a8-p162">여러 검색을 선택 하려면 ctrl 키를 누른 상태로 각 검색을 클릭 합니다. 또는 첫 번째 검색을 클릭 하 고 Shift 키를 누른 채 마지막 검색을 클릭 하 여 인접 검색을 여러 개 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p162">To select multiple searches, press Ctrl as you click each search. Or you can select multiple adjacent searches by clicking the first search, holding down the Shift key, and then clicking the last search.</span></span> 
  
5. <span data-ttu-id="032a8-387">검색을 선택한 후 **대량 작업** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-387">After you select the searches, the **Bulk actions** page appears.</span></span> 
    
    ![대량 작업 페이지에서 결과 내보내기 클릭](media/f34e3707-a9c1-494f-91a4-da1165aa730a.png)
  
    
6. <span data-ttu-id="032a8-389">검색 ![결과 내보내기 아이콘](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **결과**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-389">Click ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Export results**.</span></span>

7. <span data-ttu-id="032a8-p163">**내보내기 결과** 페이지에서 내보내기의 고유한 이름을 지정 하 고, 출력 옵션을 선택한 다음 콘텐츠를 내보낼 방법을 선택 합니다. **내보내기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p163">On the **Export results** page, give the export a unique name, select output options, and choose how your content will be exported. Click **Export**.</span></span>
    
    <span data-ttu-id="032a8-p164">사례와 연결 된 여러 콘텐츠 검색 결과를 내보내는 워크플로는 단일 검색에 대 한 검색 결과를 내보내는 것과 같습니다. 단계별 지침은 [Office 365 보안 &amp; 및 준수 센터에서 콘텐츠 검색 결과 내보내기를](export-search-results.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="032a8-p164">The workflow to export the results from multiple content searches associated with a case is the same as exporting the search results for a single search. For step-by-step instructions, see [Export Content Search results from the Office 365 Security &amp; Compliance Center](export-search-results.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="032a8-p165">사례와 연결 된 여러 검색에서 검색 결과를 내보낼 때 동일한 메시지의 인스턴스가 여러 개 있는 경우에도 중복 제거를 사용 하도록 설정 하 여 전자 메일 메시지의 복사본을 하나만 내보낼 수 있도록 하는 옵션도 있습니다. 하나 이상의 검색에서 검색 된 사서함입니다. 복제 제거 및 중복 항목이 식별 되는 방식에 대 한 자세한 내용은 [eDiscovery 검색 결과의 중복](de-duplication-in-ediscovery-search-results.md)제거를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="032a8-p165">When you export search results from multiple searches associated with a case, you also have the option to enable de-duplication so that only one copy of an email message is exported even though multiple instances of the same message might have been found in the mailboxes that were searched in one or more of the searches. For more information about de-duplication and how duplicate items are identified, see [De-duplication in eDiscovery search results](de-duplication-in-ediscovery-search-results.md).</span></span> 
  
8. <span data-ttu-id="032a8-396">내보내기를 시작한 후 **내보내기** 탭을 클릭 하 여 해당 사례에 대 한 내보내기 작업 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-396">After you start the export, click the **Export** tab to display the list of export jobs for that case.</span></span> 
    
    ![내보내기 탭, 여러 검색](media/b9505e1b-559f-4a8c-96b3-a3f734753926.png)
  
    <span data-ttu-id="032a8-p166">새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로 고침** ![을 클릭 하 여 방금 만든 내보내기 작업을 표시 하도록 내보내기 작업 목록을 업데이트 해야 할 수 있습니다. 내보내기 작업에 포함 된 검색은 **검색** 열에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p166">You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the list of export jobs to display the export job that you just created. Note that the searches that were included in the export job are listed in the **Searches** column.</span></span> 
    
8. <span data-ttu-id="032a8-p167">방금 만든 내보내기 작업을 클릭 하 여 세부 정보 창에 상태 정보를 표시 합니다. 이 정보에는 Microsoft 클라우드에서 Azure 저장소 영역으로 전송 된 항목의 백분율이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p167">Click the export job that you just created to display status information in the details pane. This information includes the percentage of items that have been transferred to an Azure storage area in the Microsoft cloud.</span></span>
    
9. <span data-ttu-id="032a8-p168">모든 항목을 전송 하 고 나면 **결과 다운로드** 를 클릭 하 여 로컬 컴퓨터에 검색 결과를 다운로드 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 검색 결과 내보내기](export-search-results.md) 의 2 단계를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="032a8-p168">After all items have been transferred, click **Download results** to download the search results to your local computer. For more information, see Step 2 in [Export search results from the Office 365 Security &amp; Compliance Center](export-search-results.md)</span></span>
    
#### <a name="more-information-about-exporting-the-results-of-multiple-searches"></a><span data-ttu-id="032a8-404">여러 검색 결과 내보내기에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="032a8-404">More information about exporting the results of multiple searches</span></span>

- <span data-ttu-id="032a8-p169">여러 검색의 결과를 내보낼 때 모든 검색의 검색 쿼리를 사용 하 여 **OR** 연산자를 결합 한 다음 결합 된 검색을 시작 합니다. 결합 된 검색의 예상 결과가 선택한 내보내기 작업의 세부 정보 창에 표시 됩니다. 검색 결과가 Microsoft 클라우드의 Azure storage 영역으로 전송 됩니다. 전송 상태는 세부 정보 창에도 표시 됩니다. 앞에서 설명한 것 처럼 모든 검색 결과를 전송한 후 로컬 컴퓨터로 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p169">When you export the results of multiple searches, the search queries from all the searches are combined by using **OR** operators, and then the combined search is started. The estimated results of the combined search are displayed in the details pane of the selected export job. The search results are then transferred to the Azure storage area in the Microsoft cloud. The status of the transfer is also displayed in the details pane. As previously stated, after all the search results have been transferred, you can download them to your local computer.</span></span> 
    
- <span data-ttu-id="032a8-p170">내보낼 모든 검색에 대 한 검색 쿼리의 최대 키워드 수는 500입니다. 이 값은 단일 콘텐츠 검색의 경우와 동일 합니다. 내보내기 작업은 **OR** 연산자를 사용 하 여 모든 검색 쿼리를 결합 하기 때문입니다. 이 제한을 초과 하면 오류가 반환 됩니다. 이 경우에는 검색 결과를 줄이고 내보내려는 검색의 검색 쿼리를 단순화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p170">The maximum number of keywords from the search queries for all searches that you want to export is 500. (this is the same limit for a single Content Search). That's because the export job combines all the search queries by using the **OR** operator. If you exceed this limit, an error will be returned. In this case, you'll have to export the results from fewer searches or simplify the search queries of the searches that you want to export.</span></span> 
    
- <span data-ttu-id="032a8-p171">내보낸 검색 결과는 항목을 찾은 콘텐츠 원본에 따라 구성 됩니다. 즉, 내보내기 결과의 콘텐츠 원본에 여러 검색에서 반환 되는 항목이 있을 수 있습니다. 예를 들어 각 사서함에 대해 한 pst 파일에 전자 메일 메시지를 내보내도록 선택한 경우 pst 파일에 여러 검색 결과가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p171">The search results that are exported are organized by the content source the item was found in. That means a content source in the export results might have items returned by different searches. For example, if you chose to export email messages in one PST file for each mailbox, the PST file might have results from multiple searches.</span></span>
    
- <span data-ttu-id="032a8-418">내보낸 검색 중 둘 이상에서 동일한 콘텐츠 위치에 있는 동일한 전자 메일 항목 또는 문서를 반환 하는 경우에는 항목의 복사본을 하나만 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-418">If the same email item or document from the same content location is returned by more than one of the searches that you export, only one copy of the item will be exported.</span></span>
    
- <span data-ttu-id="032a8-p172">여러 검색을 만든 후에는 해당 내보내기를 편집할 수 없습니다. 예를 들어 내보내기에서 검색을 추가 하거나 제거할 수 없습니다. 내보낼 검색 결과를 변경 하려면 새 내보내기 작업을 만들어야 합니다. 내보내기 작업을 만든 후에는 결과를 컴퓨터로 다운로드 하거나, 내보내기를 다시 시작 하거나, 내보내기 작업을 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p172">You can't edit an export for multiple searches after you create it. For example, you can't add or remove searches from the export. You'll have to create a new export job to change which search results are exported. After a export job is created, you only can download the results to a computer, restart the export, or delete the export job.</span></span>
    
- <span data-ttu-id="032a8-p173">내보내기를 다시 시작 하면 내보내기 작업을 구성 하는 검색 쿼리에 대 한 모든 변경 내용이 검색 결과에 영향을 주지 않습니다. 내보내기를 다시 시작 하면 내보내기 작업을 만들 때 실행 된 것과 동일한 결합 된 검색 쿼리 작업이 다시 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p173">If you restart the export, any changes to the queries of the searches that make up the export job won't affect the search results that will be retrieved. When you restart an export, the same combined search query job that was run when the export job was created will be run again.</span></span>
    
- <span data-ttu-id="032a8-425">eDiscovery 사례의 내보내기 페이지에서 내보내기를 다시 \*\*\*\* 시작 하면 Azure 저장소 영역으로 전송 되는 검색 결과가 이전 결과를 덮어쓰게 됩니다. 이전에 전송 된 결과는 다운로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-425">If you restart an export from the **Exports** page in an eDiscovery case, the search results that are transferred to the Azure storage area will overwrite the previous results; the previous results there were transferred won't be available to be downloaded.</span></span> 
    
- <span data-ttu-id="032a8-p174">고급 eDiscovery에서 분석에 대 한 여러 검색의 결과를 준비 하는 것은 사용할 수 없습니다. 고급 eDiscovery에서 분석에 대 한 단일 검색 결과만 준비할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p174">Preparing the results of multiple searches for analysis in Advanced eDiscovery isn't available. You can only prepare the results of a single search for analysis in Advanced eDiscovery.</span></span>

## <a name="step-7-prepare-search-results-for-advanced-ediscovery"></a><span data-ttu-id="032a8-428">7 단계: 고급 eDiscovery에 대 한 검색 결과 준비</span><span class="sxs-lookup"><span data-stu-id="032a8-428">Step 7: Prepare search results for Advanced eDiscovery</span></span>

<span data-ttu-id="032a8-p175">조직에 Office 365 E5 구독이 있는 경우 고급 eDiscovery에서 분석을 위해 사례와 연결 된 콘텐츠 검색의 결과를 준비할 수 있습니다. 검색 결과를 준비한 후에는 고급 ediscovery로 이동 하 고 ( [8 단계: 고급 ediscovery의 사례 이동](#step-8-go-to-the-case-in-advanced-ediscovery)참조) 검색 결과 데이터를 처리 하 여 고급 ediscovery에서 추가 분석을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p175">If your organization has an Office 365 E5 subscription, you can prepare the results of Content Searches associated with a case for analysis in Advanced eDiscovery. After you prepare search results, you can go to Advanced eDiscovery (see [Step 8: Go to the case in Advanced eDiscovery](#step-8-go-to-the-case-in-advanced-ediscovery)) and process the search result data for further analysis in Advanced eDiscovery.</span></span>
  
<span data-ttu-id="032a8-p176">고급 eDiscovery에 대 한 검색 결과를 준비할 때 OCR (광학 인식) 기능은 이미지에서 텍스트를 자동으로 추출 합니다. OCR은 느슨한 파일, 전자 메일 첨부 파일 및 포함 된 이미지에 대해 지원 됩니다. 이렇게 하면 고급 eDiscovery (근거리 복제, 전자 메일 스레딩, 테마 및 예측 코딩)의 텍스트 분석 기능을 이미지 파일의 모든 텍스트에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p176">When you prepare search results for Advanced eDiscovery, optical character recognition (OCR) functionality automatically extracts text from images. OCR is supported for loose files, email attachments, and embedded images. This allows you to apply the text analytic capabilities of Advanced eDiscovery (near-duplicates, email threading, themes, and predictive coding) to any text in image files.</span></span>
  
> [!NOTE]
> <span data-ttu-id="032a8-p177">고급 eDiscovery를 사용 하 여 사용자 데이터를 분석 하려면 데이터의 custodian 사용자에 게 Office 365 E5 라이선스를 할당 해야 합니다. 또는 Office 365 E1 또는 E3 라이선스를 사용 하는 사용자에 게 고급 eDiscovery 독립 실행형 라이선스를 할당할 수 있습니다. 서비스 케이스에 할당 되 고 고급 eDiscovery를 사용 하 여 데이터를 분석 하는 관리자 및 규정 준수 직원은 E5 라이선스가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p177">To analyze a user's data using Advanced eDiscovery, the user (the custodian of the data) must be assigned an Office 365 E5 license. Alternatively, users with an Office 365 E1 or E3 license can be assigned an Advanced eDiscovery standalone license. Administrators and compliance officers who are assigned to cases and use Advanced eDiscovery to analyze data don't need an E5 license.</span></span> 
  
1. <span data-ttu-id="032a8-437">보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-437">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
2. <span data-ttu-id="032a8-438">고급 eDiscovery에서 분석에 대 한 검색 결과를 준비 하려는 사례 옆에 있는 **열기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-438">Click **Open** next to the case that you want to prepare search results for analysis in Advanced eDiscovery.</span></span> 
    
3. <span data-ttu-id="032a8-439">사례에 대 한 **홈** 페이지에서 **검색**을 클릭 하 고 검색을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-439">On the **Home** page for the case, click **Search**, and then select the search.</span></span>
    
4. <span data-ttu-id="032a8-440">세부 정보 창에서 검색 결과 ![아이콘](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **더**내보내기를 클릭 한 다음 **고급 eDiscovery 준비를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-440">In the details pane, click ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **More**, and then click **Prepare for Advanced eDiscovery**.</span></span>
    
    ![고급 eDiscovery에 대 한 결과 준비](media/b6548ff0-a6e9-42b1-9ae4-5c15146f5690.png)
  
5. <span data-ttu-id="032a8-442">**Advanced eDiscovery 준비** 페이지에서 다음 중 하나를 준비 하도록 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-442">On the **Prepare for Advanced eDiscovery** page, choose to prepare one of the following:</span></span> 
    
    - <span data-ttu-id="032a8-443">형식이 인식 되지 않거나 인식할 수 없는 형식을 제외한 모든 항목은 암호화 되거나 다른 이유로 인덱싱되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-443">All items, excluding those with unrecognized format, are encrypted, or weren't indexed for other reasons.</span></span>
    
    - <span data-ttu-id="032a8-444">형식을 인식할 수 없거나, 암호화 되거나, 다른 이유로 인덱싱되지 않은 항목을 비롯 한 모든 항목이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-444">All items, including those that have unrecognized format, are encrypted, or weren't indexed for other reasons.</span></span>
    
    - <span data-ttu-id="032a8-445">형식을 인식할 수 없거나 암호화 되거나 다른 이유로 인해 인덱싱되지 않은 항목만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-445">Only items that have an unrecognizable format, are encrypted, or weren't indexed for other reasons.</span></span>
    
6. <span data-ttu-id="032a8-446">반드시 **SharePoint 파일의 버전 포함** 확인란을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-446">(Optional) Click the **Include versions for SharePoint files** check box.</span></span> 
    
7. <span data-ttu-id="032a8-447">**준비**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-447">Click **Prepare**.</span></span>
    
    <span data-ttu-id="032a8-448">고급 eDiscovery를 사용 하 여 분석을 위해 검색 결과를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-448">The search results are prepared for analysis with Advanced eDiscovery.</span></span>
    
8. <span data-ttu-id="032a8-449">**닫기를** 클릭 하 여 세부 정보 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-449">Click **Close** to close the details pane.</span></span> 
    
## <a name="step-8-go-to-the-case-in-advanced-ediscovery"></a><span data-ttu-id="032a8-450">8 단계: Advanced eDiscovery의 사례로 이동</span><span class="sxs-lookup"><span data-stu-id="032a8-450">Step 8: Go to the case in Advanced eDiscovery</span></span>

<span data-ttu-id="032a8-451">보안 &amp; 및 준수 센터에서 사례를 만든 후에는 Advanced eDiscovery에서 같은 사례로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-451">After you create a case in the Security &amp; Compliance Center, you can go to the same case in Advanced eDiscovery.</span></span>
  
<span data-ttu-id="032a8-452">Advanced eDiscovery에서 사례로 이동하려면</span><span class="sxs-lookup"><span data-stu-id="032a8-452">To go to a case in Advanced eDiscovery:</span></span>
  
1. <span data-ttu-id="032a8-453">보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-453">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
2. <span data-ttu-id="032a8-454">고급 eDiscovery로 이동 하려는 사례 옆에 있는 **열기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-454">Click **Open** next to the case that you want to go to in Advanced eDiscovery.</span></span> 
    
3. <span data-ttu-id="032a8-455">사례에 대 한 **홈** 페이지에서 **Advanced eDiscovery로 전환을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-455">On the **Home** page for the case, click **Switch to Advanced eDiscovery**.</span></span>
    
    ![Advanced eDiscovery로 전환을 선택 합니다.](media/d7e31558-e79c-4782-b841-2b735568a576.png)
  
    <span data-ttu-id="032a8-p178">**고급 eDiscovery 진행률 표시줄에 연결 하** 는 중입니다. 고급 eDiscovery에 연결 되 면 컨테이너 목록이 페이지에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p178">The **Connecting to Advanced eDiscovery** progress bar is displayed. When you're connected to Advanced eDiscovery, a list of containers is displayed on the page.</span></span> 
    
    ![고급 eDiscorvery 진행률 표시줄](media/4a84273d-765b-44b8-9006-c20e810ea393.png)
  
    <span data-ttu-id="032a8-p179">이러한 컨테이너는 7 단계에서 고급 eDiscovery 분석을 위해 준비한 검색 결과를 나타냅니다. 컨테이너의 이름은 보안 &amp; 및 준수 센터의 사례에 있는 콘텐츠 검색과 이름이 같습니다. 이 목록에는 사용자가 준비한 컨테이너 들이 나열 됩니다. 다른 사용자가 고급 eDiscovery를 위해 준비 된 검색 결과를 사용 하는 경우 해당 컨테이너가 목록에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p179">These containers represent the search results that you prepared for analysis in Advanced eDiscovery in Step 7. Note that the name of the container has the same name as Content Search in the case in the Security &amp; Compliance Center. The containers in the list are the ones that you prepared. If a different user prepared search results for Advanced eDiscovery, the corresponding containers won't be included in the list.</span></span>
    
4. <span data-ttu-id="032a8-464">컨테이너에서 고급 eDiscovery의 사례에 대 한 검색 결과 데이터를 로드 하려면 컨테이너를 선택 하 고 **프로세스**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-464">To load the search result data from a container to the case in Advanced eDiscovery, select a container and click **Process**.</span></span>
    
    <span data-ttu-id="032a8-465">컨테이너를 처리 하는 방법에 대 한 자세한 내용은 [Office 365 Advanced eDiscovery에서 프로세스 모듈 실행 및 데이터 로드](run-the-process-module-and-load-data-in-advanced-ediscovery.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="032a8-465">For information about how to process containers, see [Run the Process module and load data in Office 365 Advanced eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md).</span></span>
    
> [!TIP]
> <span data-ttu-id="032a8-466">**eDiscovery로 전환을** 클릭 하 여 보안 &amp; 및 준수 센터에서 동일한 사례로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-466">Click **Switch to eDiscovery** to go back to the same case in the Security &amp; Compliance Center.</span></span> 
  
## <a name="optional-step-9-close-a-case"></a><span data-ttu-id="032a8-467">반드시 9 단계: 사례 닫기</span><span class="sxs-lookup"><span data-stu-id="032a8-467">(Optional) Step 9: Close a case</span></span>

<span data-ttu-id="032a8-p180">eDiscovery 사례에서 지 원하는 법적 사례 또는 조사가 완료 되 면 사례를 닫을 수 있습니다. 사례를 닫을 때 수행 되는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p180">When the legal case or investigation supported by an eDiscovery case is completed, you can close the case. Here's what happens when you close a case:</span></span>
  
- <span data-ttu-id="032a8-p181">대/소문자에 보류 중인 콘텐츠 위치가 포함 되어 있으면 해당 보류를 해제 합니다. 이로 인해 사용자 또는 자동화 된 프로세스 (예: 삭제 정책)에 의해 콘텐츠가 영구적으로 삭제 되거나 제거 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p181">If the case contains any content locations on hold, those holds will be turned off. This might result in content being permanently deleted or purged, either by the user or by an automated process, such as a deletion policy.</span></span>
    
- <span data-ttu-id="032a8-p182">사례를 닫으면 해당 사례와 연결 된 보류만 해제 됩니다. 다른 보류가 콘텐츠 위치 (예: 소송 보존)에 있는 경우 보존 정책 또는 다른 eDiscovery 사례의 보존 등은 계속 유지 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p182">Closing a case only turns off the holds that are associated with that case. If other holds are place on a content location (such as a Litigation Hold. a Preservation Policy, or a hold from a different eDiscovery case) those holds will still be maintained.</span></span>
    
- <span data-ttu-id="032a8-p183">이 사례는 여전히 보안 &amp; 및 준수 센터의 eDiscovery 페이지에 나열 됩니다. 닫힌 사례에 대 한 세부 정보, 보류, 검색 및 구성원은 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p183">The case is still listed on the eDiscovery page in the Security &amp; Compliance Center. The details, holds, searches, and members of a closed case are retained.</span></span>
    
- <span data-ttu-id="032a8-p184">해당 사례가 닫힌 후에 대/소문자를 편집할 수 있습니다. 예를 들어 고급 eDiscovery에서 구성원을 추가 하거나 제거 하 고, 검색을 만들고, 검색 결과를 내보내고, 검색 결과를 준비할 수 있습니다. 활성 사례와 닫힌 사례의 주요 차이점은 사례를 닫을 때 보류가 해제 된다는 점입니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p184">You can edit a case after it's closed. For example, you can add or removing members, create searches, export search results, and prepare search result for analysis in Advanced eDiscovery. The primary difference between active and closed cases is that holds are turned off when a case is closed.</span></span>
    
<span data-ttu-id="032a8-480">사례를 닫으려면:</span><span class="sxs-lookup"><span data-stu-id="032a8-480">To close a case:</span></span>
  
1. <span data-ttu-id="032a8-481">보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-481">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
2. <span data-ttu-id="032a8-482">닫으려는 case의 이름을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-482">Click the name of the case that you want to close.</span></span>
    
    <span data-ttu-id="032a8-483">**이 사례** 플라이 아웃 관리 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-483">The **Manage this case** flyout page is displayed.</span></span> 
    
3. <span data-ttu-id="032a8-484">**사례 관리 상태**에서 미리 보기 ![단추](media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) **닫기의 경우**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-484">Under **Manage case status**, click ![Remove the peek button](media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) **Close case**.</span></span>
    
    <span data-ttu-id="032a8-485">사례와 연결 된 보류가 해제 됨을 나타내는 경고가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-485">A warning is displayed saying that the holds associated with the case will be turned off.</span></span>
    
4. <span data-ttu-id="032a8-486">**예** 를 클릭 하 여 사례를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-486">Click **Yes** to close the case.</span></span> 
    
    <span data-ttu-id="032a8-487">**이 사례** 플라이 아웃 관리 페이지의 상태가 **활성** 에서 **종료**로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-487">The status on the **Manage this case** flyout page is changed from **Active** to **Closing**.</span></span>
    
5. <span data-ttu-id="032a8-488">**이 사례 관리** 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-488">Close the **Manage this case** page.</span></span> 
    
6. <span data-ttu-id="032a8-p185">**eDiscovery** 페이지에서 새로고침 아이콘 ![](media/O365-MDM-Policy-RefreshIcon.gif) \*\*\*\* 새로 고침을 클릭 하 여 종료 된 사례의 상태를 업데이트 합니다. 닫기 프로세스를 완료 하는 데 최대 60 분이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p185">On the **eDiscovery** page, click ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) **Refresh** to update the status of the closed case. It might take up to 60 minutes for the closing process to complete.</span></span> 
    
    <span data-ttu-id="032a8-p186">프로세스가 완료 되 면 **eDiscovery** 페이지에서 사례의 상태가 **닫힘으로** 변경 됩니다. 케이스의 이름을 다시 클릭 하 여 사례를 닫은 사람과 닫은 사람에 대 한 정보가 포함 된 **이 사례** 플라이 아웃 관리 페이지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p186">When the process is complete, the status of the case is changed to **Closed** on the **eDiscovery** page. Click the name of the case again to display the **Manage this case** flyout page, which contains information about when the case was closed and who closed it.</span></span> 
     
## <a name="optional-step-10-re-open-a-closed-case"></a><span data-ttu-id="032a8-493">반드시 10 단계: 닫힌 사례 다시 열기</span><span class="sxs-lookup"><span data-stu-id="032a8-493">(Optional) Step 10: Re-open a closed case</span></span>

<span data-ttu-id="032a8-p187">사례를 다시 열면 서비스 케이스가 종료 될 때 적용 된 모든 보류는 자동으로 복원 되지 않습니다. 사례를 다시 연 후에는 **보류** 페이지로 이동 하 여 이전 보류를 켜야 합니다. 보류를 설정 하려면 해당 항목을 선택 하 고 세부 정보 창에서 **설정을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p187">When you reopen a case, any holds that were in place when the case was closed won't be automatically reinstated. After the case is reopened, you'll have to go to the **Hold** page and turn on the previous holds. To turn a hold on, select it and click **Turn it on** in the details pane.</span></span> 
  
1. <span data-ttu-id="032a8-497">보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-497">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
2. <span data-ttu-id="032a8-498">다시 열 사례 이름을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-498">Click the name of the case that you want to reopen.</span></span>
    
    <span data-ttu-id="032a8-499">**이 사례** 플라이 아웃 관리 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-499">The **Manage this case** flyout page is displayed.</span></span> 
    
3. <span data-ttu-id="032a8-500">**사례 관리 상태**에서 **대/소문자 다시 열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-500">Under **Manage case status**, click **Reopen case**.</span></span>
    
    <span data-ttu-id="032a8-501">닫힌 경우 케이스와 연결 된 보류를 자동으로 설정 하지 않으면 경고가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-501">A warning is displayed saying that the holds that were associated with the case when it was closed won't be turned on automatically.</span></span>
    
4. <span data-ttu-id="032a8-502">**예** 를 클릭 하 여 사례를 다시 엽니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-502">Click **Yes** to reopen the case.</span></span> 
    
    <span data-ttu-id="032a8-503">**이 사례** 플라이 아웃 관리 페이지의 상태가 **닫힘** 에서 **활성**으로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-503">The status on the **Manage this case** flyout page is changed from **Closed** to **Active**.</span></span>
    
5. <span data-ttu-id="032a8-504">**이 사례 관리** 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-504">Close the **Manage this case** page.</span></span> 
    
6. <span data-ttu-id="032a8-p188">**eDiscovery** 페이지에서 새로고침 아이콘 ![](media/O365-MDM-Policy-RefreshIcon.gif) \*\*\*\* 새로 고침을 클릭 하 여 다시 연 사례의 상태를 업데이트 합니다. 다시 여는 프로세스를 완료 하는 데 최대 60 분이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p188">On the **eDiscovery** page, click ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) **Refresh** to update the status of the reopened case. It might take up to 60 minutes for the reopening process to complete.</span></span> 
    
    <span data-ttu-id="032a8-507">프로세스가 완료 되 면 **eDiscovery** 페이지에서 사례 상태가 **활성** 으로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-507">When the process is complete, the status of the case is changed to **Active** on the **eDiscovery** page.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="032a8-508">추가 정보</span><span class="sxs-lookup"><span data-stu-id="032a8-508">More information</span></span>

- <span data-ttu-id="032a8-p189">ediscovery 사례 **와 연관 된 ediscovery 사례 또는 보류에 대 한 제한이 있습니까?** 다음 표에는 eDiscovery 사례 및 사례 보존에 대 한 한계가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p189">**Are there any limits for eDiscovery cases or holds associated with an eDiscovery case?** The following table lists the limits for eDiscovery cases and case holds.</span></span>
    
  |<span data-ttu-id="032a8-511">**제한 설명**</span><span class="sxs-lookup"><span data-stu-id="032a8-511">**Description of limit**</span></span>|<span data-ttu-id="032a8-512">**제한 유형**</span><span class="sxs-lookup"><span data-stu-id="032a8-512">**Limit**</span></span>|
  |:-----|:-----|
  |<span data-ttu-id="032a8-513">조직의 최대 사례 수</span><span class="sxs-lookup"><span data-stu-id="032a8-513">Maximum number of cases for an organization</span></span>  <br/> |<span data-ttu-id="032a8-514">제한 없음</span><span class="sxs-lookup"><span data-stu-id="032a8-514">No limit</span></span>  <br/> |
  |<span data-ttu-id="032a8-515">조직에 대 한 최대 사례 보존 수</span><span class="sxs-lookup"><span data-stu-id="032a8-515">Maximum number of case holds for an organization</span></span>  <br/> |<span data-ttu-id="032a8-516">10,000</span><span class="sxs-lookup"><span data-stu-id="032a8-516">10,000</span></span>  <br/> |
  |<span data-ttu-id="032a8-517">단일 케이스 보류의 최대 사서함 수</span><span class="sxs-lookup"><span data-stu-id="032a8-517">Maximum number of mailboxes in a single case hold</span></span>  <br/> |<span data-ttu-id="032a8-518">1,000</span><span class="sxs-lookup"><span data-stu-id="032a8-518">1,000</span></span>  <br/> |
  |<span data-ttu-id="032a8-519">단일 케이스 보류에서의 최대 SharePoint 및 비즈니스용 OneDrive 사이트 수</span><span class="sxs-lookup"><span data-stu-id="032a8-519">Maximum number of SharePoint and OneDrive for Business sites in a single case hold</span></span>  <br/> |<span data-ttu-id="032a8-520">100</span><span class="sxs-lookup"><span data-stu-id="032a8-520">100</span></span>  <br/> |
   
- <span data-ttu-id="032a8-p190">**고급 eDiscovery의 사례 관리 페이지에서 만든 사례는 어떻습니까?** 보안 &amp; 및 준수 센터에서 **eDiscovery** 페이지 아래쪽에 있는 링크를 클릭 하 여 이전 고급 eDiscovery 사례 목록에 액세스할 수 있습니다. 그러나 이전 상황에서 작업을 수행 하려면 Office 365 지원 서비스에 문의 하 여 보안 &amp; 및 준수 센터에서 새 eDiscovery 사례에 대 한 사례를 이동 하도록 요청 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p190">**What about cases that were created on the case management page in Advanced eDiscovery?** You can access a list of older Advanced eDiscovery cases by clicking the link at the bottom on the **eDiscovery** page in the Security &amp; Compliance Center. However, to do any work in an older case, you have to contact Office 365 Support and request that the case be moved to a new eDiscovery case in the Security &amp; Compliance Center.</span></span> 
    
- <span data-ttu-id="032a8-p191">**eDiscovery 관리자를 만드는 이유는 무엇 인가요?** 앞에서 설명한 것 처럼 ediscovery 관리자는 조직의 모든 ediscovery 사례를 보고 액세스할 수 있는 ediscovery 관리자 역할 그룹의 구성원 이어야 합니다. 모든 eDiscovery 사례에 액세스할 수 있는 이러한 기능에는 다음과 같은 두 가지 중요 한 용도가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p191">**Why create an eDiscovery Administrator?** As previously explained, an eDiscovery Administrator is member of the eDiscovery Manager role group who can view and access all eDiscovery cases in your organization. This ability to access all the eDiscovery cases has two important purposes:</span></span>
    
  - <span data-ttu-id="032a8-p192">ediscovery 사례의 유일한 구성원 인 사용자가 조직을 벗어나면 조직 관리 역할 그룹의 구성원이 나 ediscovery 관리자 역할 그룹의 구성원을 포함 하는 아무도 구성원이 아니므로 ediscovery 사례에 액세스할 수 없습니다. 사례입니다. 이 경우에는 대/소문자에서 데이터에 액세스할 수 있는 방법이 없습니다. 그러나 ediscovery 관리자가 조직의 모든 eDiscovery 사례에 액세스할 수 있으므로 해당 사용자는 보안 &amp; 및 준수 센터에서 사례를 보고 케이스의 구성원으로 자신 또는 다른 eDiscovery 관리자를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p192">If a person who is the only member of an eDiscovery case leaves your organization, no one (including members of the Organization Management role group or another member of the eDiscovery Manager role group) can access that eDiscovery case because they aren't a member of a case. In this situation, there would be no way to access the data in the case. But because an eDiscovery Administrator can access all eDiscovery cases in the organization, they can view the case in the Security &amp; Compliance Center and add themselves or another eDiscovery manager as a member of the case.</span></span>
    
  - <span data-ttu-id="032a8-p193">ediscovery 관리자는 모든 ediscovery 사례를 보고 액세스할 수 있으므로 모든 사례 및 관련 콘텐츠 검색을 감사 하 고 감독 할 수 있습니다. 이를 통해 콘텐츠 검색 또는 eDiscovery 사례를 오용 하지 못하게 할 수 있습니다. 또한 ediscovery 관리자는 콘텐츠 검색 결과에서 잠재적으로 중요 한 정보에 액세스할 수 있으므로 ediscovery 관리자 인 사용자 수를 제한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p193">Because an eDiscovery Administrator can view and access all eDiscovery cases, they can audit and oversee all cases and associated Content Searches. This can help to prevent any misuse of Content Searches or eDiscovery cases. And because eDiscovery Administrators can access potentially sensitive information in the results of a Content Search, you should limit the number of people who are eDiscovery Administrators.</span></span>
    
    <span data-ttu-id="032a8-p194">마지막으로, 이전에 설명한 것 처럼 보안 &amp; 및 준수 센터의 eDiscovery 관리자는 고급 eDiscovery의 관리자에 게 자동으로 추가 됩니다. 즉, eDiscovery 관리자 인 사람은 사용자 설정, 사례 만들기 및 사례에 데이터 추가와 같은 고급 eDiscovery에서 관리 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p194">Finally, as previous explained, eDiscovery Administrators in the Security &amp; Compliance Center are automatically added as administrators in Advanced eDiscovery. That means a person who is an eDiscovery Administrator can perform administrative tasks in Advanced eDiscovery, such as setting up users, creating cases, and adding data to cases.</span></span>
    
- <span data-ttu-id="032a8-p195">**콘텐츠 위치를 보류 상태로 설정 하기 위한 라이선스 요구 사항은 무엇 인가요?** 일반적으로 조직에서는 콘텐츠 위치를 보존 하려면 Office 365 E3 구독 이상이 필요 합니다. 사서함을 보류 상태로 설정 하려면 보류 중인 사서함에 대해 Exchange Online 계획 2 라이선스가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p195">**What are the licensing requirements to place content locations on hold?** In general, organizations require an Office 365 E3 subscription or higher to place content locations on hold. To place mailboxes on hold, an Exchange Online Plan 2 license is required for the mailbox you want to place on hold.</span></span>
    
- <span data-ttu-id="032a8-p196">**5 단계에서 모든 사례 콘텐츠를 검색 하는 방법에 대해 알아야 할 기타 정보** 앞에서 설명한 것 처럼 사례에서 보류 되었던 콘텐츠 위치를 검색할 수 있습니다. 이렇게 하면 보류 기준과 일치 하는 콘텐츠만 검색 됩니다. 보존 기준이 없으면 모든 콘텐츠를 검색 합니다. 콘텐츠가 쿼리 기반 보존 상태에 있는 경우에는 보류 조건과 일치 하는 콘텐츠 (4 단계에 있는 보류)와 검색 조건 (5 단계에서 검색)이 검색 결과와 함께 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p196">**What else should you know about searching all case content in Step 5?** As previously explained, you can search the content locations that have been placed on hold in the case. When you do this, only the content that matches the hold criteria is search. If there is no hold criteria, all content is searched. If contents are on a query-based hold, only the content that matches both hold criteria (from the hold placed in Step 4) and the search criteria (from the search in Step 5) is returned with the search results.</span></span>
    
    <span data-ttu-id="032a8-543">다음은 모든 케이스 콘텐츠를 검색할 때 주의 해야 할 몇 가지 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-543">Here are some other things to keep in mind when searching all case content:</span></span>
    
  - <span data-ttu-id="032a8-p197">콘텐츠 위치가 같은 경우에 여러 보류의 일부인 경우 모든 사례 콘텐츠 옵션을 사용 하 여 해당 콘텐츠 위치를 검색할 때 고정 쿼리를 **OR** 연산자로 결합 합니다. 마찬가지로 콘텐츠 위치가 서로 다른 두 보류의 일부인 반면, 하나는 쿼리를 기반으로 하며 나머지는 무한 유지 (모든 콘텐츠가 보류 되는 위치) 인 경우 무제한 보존으로 인해 모든 콘텐츠가 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p197">If a content location is part of multiple holds within the same case, the hold queries are combined by an **OR** operator when you search that content location using the all case content option. Similarly, if a content location is part of two different holds, where one is query-based and the other is an infinite hold (where all content is placed on hold), then all content will be search because of the infinite hold.</span></span> 
    
  - <span data-ttu-id="032a8-p198">콘텐츠 검색이 사례에 대 한 것이 고 모든 사례 콘텐츠를 검색 하도록 구성한 후에 콘텐츠 위치를 추가 또는 제거 하거나 보류 쿼리를 변경 하 여 보류를 변경 하면 검색 구성이 해당 변경 내용으로 업데이트 됩니다. 그러나 검색 결과를 업데이트 하려면 보류가 변경 된 후에 검색을 다시 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p198">If a content search is for a case and you've configured it to search all case content and then you change a hold (by adding or removing a content location or changing the hold query), the search configuration is updated with those changes. However, you have to re-run the search after the hold is changed to update the search results.</span></span>
    
  - <span data-ttu-id="032a8-p199">여러 대/소문자가 eDiscovery 사례의 콘텐츠 위치에 배치 되 고 모든 사례 콘텐츠를 검색 하도록 선택한 경우 해당 검색 쿼리에 대 한 최대 키워드 수는 500입니다. 이는 콘텐츠 검색에 **OR** 연산자를 사용 하 여 쿼리 기반 보류가 모두 포함 되기 때문입니다. 결합 된 보류 쿼리와 콘텐츠 검색 쿼리에 모두 500 개 보다 많은 키워드가 있으면 쿼리 기반 사례와 일치 하는 콘텐츠 뿐 아니라 사서함에 포함 된 모든 콘텐츠가 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p199">If multiple case holds are placed on a content location in an eDiscovery case and you select to search all case content, the maximum number of keywords for that search query is 500. That's because the content search combines all the query-based holds by using the **OR** operator. If there are more than 500 keywords in the combined hold queries and the content search query, then all content in the mailbox is searched, not just that content that matches the any of query-based case holds.</span></span> 
    
  - <span data-ttu-id="032a8-551">서비스 케이스 보류 상태가 **on**으로 설정 된 경우에도 보류를 설정 하는 동안 사례 콘텐츠 위치를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-551">If a case hold has a status of **Turning on**, you can still search the case content locations while the hold is being turned on.</span></span>
    
  - <span data-ttu-id="032a8-p200">앞에서 설명한 것 처럼 검색에서 모든 사례 콘텐츠를 검색 하도록 구성 된 경우 여러 검색의 결과를 내보내려는 경우 해당 검색을 포함할 수 없습니다. 모든 사례 콘텐츠를 검색 하도록 검색을 구성한 경우에는 해당 단일 검색의 결과를 내보내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p200">As previously stated, if a search is configured to search all case content, then you can't include that search if you want to export the results of multiple searches. If a search is configured to search all case content, then you'll have to export the results of that single search.</span></span>
    
- <span data-ttu-id="032a8-p201">**보류 중인 사서함, SharePoint 사이트 또는 OneDrive 계정이 다중 지리적 환경에서 다른 지역으로 이동 되는 경우 계속 해 서 적용 됩니까?** 모든 경우에 사서함, 사이트 또는 OneDrive 계정의 콘텐츠는 계속 유지 됩니다. 그러나 보존 통계에는 다른 지역으로 이동한 콘텐츠 위치의 항목이 더 이상 포함 되지 않습니다. 이동 된 콘텐츠 위치에 대 한 보존 통계를 포함 하려면 보류를 편집 하 고 URL (또는 사서함의 SMTP 주소)을 업데이트 하 여 콘텐츠 위치가 보존 통계에 다시 포함 되도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p201">**If a mailbox, SharePoint site, or OneDrive account that is on hold is moved to a different region in a multi-geo environment, will the hold still apply?** In all cases, the content in a mailbox, site, or OneDrive account will still be retained. However, the hold statistics will no longer include items from a content location that's been moved to a different region. To include hold statistics for a content location that's been moved, you'll have to edit the hold and update the URL (or SMTP address of a mailbox) so that the content location is once again included in the hold statistics.</span></span> 
    
- <span data-ttu-id="032a8-p202">**Office 365 그룹 및 Microsoft 팀을 유지 하는 방법은 무엇 인가요?** Microsoft 팀은 Office 365 그룹을 기반으로 작성 됩니다. 따라서 eDiscovery 사례에서 보류를 설정 하는 것은 매우 유사 합니다. Office 365 그룹과 Microsoft 팀을 보류할 때 다음과 같은 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p202">**What about placing a hold on Office 365 Groups and Microsoft Teams?** Microsoft Teams are built on Office 365 Groups. Therefore, placing them on hold in an eDiscovery case is very similar. Keep the following things in mind when placing Office 365 Groups and Microsoft Teams on hold.</span></span> 
    
  - <span data-ttu-id="032a8-562">보류 중인 Office 365 그룹 및 Microsoft 팀에 있는 콘텐츠를 배치 하려면 그룹 또는 팀과 연결 된 사서함 및 SharePoint 사이트를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-562">To place content located in Office 365 Groups and Microsoft Teams on hold, you have to specify the mailbox and SharePoint site that associated with a group or team.</span></span>
    
  - <span data-ttu-id="032a8-p203">Exchange Online에서 **remove-unifiedgroup** cmdlet을 실행 하 여 Office 365 그룹 또는 Microsoft Team의 속성을 볼 수 있습니다. 이를 통해 Office 365 그룹 또는 Microsoft 팀에 연결 된 사이트의 URL을 가져올 수 있습니다. 예를 들어 다음 명령은 선임 리더십 팀 이라는 Office 365 그룹에 대해 선택 된 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p203">Run the **Get-UnifiedGroup** cmdlet in Exchange Online to view properties for an Office 365 Group or Microsoft Team. This is a good way to get the URL for the site that's associated with an Office 365 Group or a Microsoft Team. For example, the following command displays selected properties for an Office 365 Group named Senior Leadership Team:</span></span> 
    
     ```
    Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl

     DisplayName            : Senior Leadership Team
     Alias                  : seniorleadershipteam
     PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
     SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
    ```

    > [!NOTE]
    > <span data-ttu-id="032a8-566">**remove-unifiedgroup** cmdlet을 실행 하려면 Exchange Online에서 보기 전용 받는 사람 역할을 할당 받거나 보기 전용 받는 사람 역할이 할당 된 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-566">To run the **Get-UnifiedGroup** cmdlet, you have to be assigned the View-Only Recipients role in Exchange Online or be a member of a role group that's assigned the View-Only Recipients role.</span></span> 
  
  - <span data-ttu-id="032a8-p204">사용자의 사서함이 검색 되 면 사용자가 구성원으로 속해 있는 모든 Office 365 그룹 또는 Microsoft 팀이 검색 되지 않습니다. 마찬가지로, Office 365 그룹 또는 Microsoft 팀을 유지 하면 그룹 사서함과 그룹 사이트만 보존 됩니다. 그룹 구성원의 사서함 및 비즈니스용 OneDrive 사이트를 보류에 명시적으로 추가 하지 않으면 해당 사이트가 보류 되지 않습니다. 따라서 법적 이유로 Office 365 그룹 또는 Microsoft 팀을 유지 해야 하는 경우 그룹 및 팀 구성원에 대 한 비즈니스용 OneDrive 사이트를 동일한 보류에 추가 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p204">When a user's mailbox is searched, any Office 365 Group or Microsoft Team that the user is a member of won't be searched. Similarly, when you place an Office 365 Group or Microsoft Team hold, only the group mailbox and group site are placed on hold; the mailboxes and OneDrive for Business sites of group members aren't placed on hold unless you explicitly add them to the hold. Therefore, if you the need to place an Office 365 Group or Microsoft Team on hold for a legal reasons, consider adding the mailboxes and OneDrive for Business sites for group and team members on the same hold.</span></span>
    
  - <span data-ttu-id="032a8-p205">office 365 그룹 또는 Microsoft Team의 구성원 목록을 가져오려면 office 365 관리 센터의 **홈 \> 그룹** 페이지에서 속성을 볼 수 있습니다. 또는 Exchange Online PowerShell에서 다음 명령을 실행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p205">To get a list of the members of a Office 365 Group or Microsoft Team, you can view the properties on the **Home \> Groups** page in the Office 365 admin center. Alternatively, you can run the following command in Exchange Online PowerShell:</span></span> 
    
      ```
      Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
      ```

    > [!NOTE]
    > <span data-ttu-id="032a8-572">**add-unifiedgrouplinks** cmdlet을 실행 하려면 Exchange Online에서 보기 전용 받는 사람 역할을 할당 받거나 보기 전용 받는 사람 역할이 할당 된 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-572">To run the **Get-UnifiedGroupLinks** cmdlet, you have to be assigned the View-Only Recipients role in Exchange Online or be a member of a role group that's assigned the View-Only Recipients role.</span></span> 
  
  - <span data-ttu-id="032a8-p206">microsoft 팀 채널의 일부인 대화는 microsoft 팀과 연결 된 사서함에 저장 됩니다. 마찬가지로 팀 구성원이 채널에서 공유 하는 파일은 팀의 SharePoint 사이트에 저장 됩니다. 따라서 대화 및 파일을 채널에 유지 하려면 Microsoft 팀 사서함 및 SharePoint 사이트를 보류 상태로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p206">Conversations that are part of a Microsoft Teams channel are stored in the mailbox that's associated with the Microsoft Team. Similarly, files that team members share in a channel are stored on the team's SharePoint site. Therefore, you have to place the Microsoft Team mailbox and SharePoint site on hold to retain conversations and files in a channel.</span></span>
    
    <span data-ttu-id="032a8-p207">또는 Microsoft 팀의 채팅 목록에 포함 된 대화는 채팅에 참가 하는 사용자의 사서함에 저장 됩니다. 사용자가 채팅 대화에서 공유 하는 파일은 해당 파일을 공유 하는 사용자의 비즈니스용 OneDrive 사이트에 저장 됩니다. 따라서 채팅 목록에 있는 대화 및 파일을 유지 하려면 개별 사용자 사서함과 비즈니스용 OneDrive 사이트를 보존 해야 합니다. 이 때문에 팀 사서함 (및 사이트)을 유지 하는 것 외에도 Microsoft 팀 구성원의 사서함을 유지 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p207">Alternatively, conversations that are part of the Chat list in Microsoft Teams are stored in the mailbox of the user's who participate in the chat. And files that a user shares in Chat conversations are stored in the OneDrive for Business site of the user who shares the file. Therefore, you have to place the individual user mailboxes and OneDrive for Business sites on hold to retain conversations and files in the Chat list. That's why it's a good idea to place a hold on the mailboxes of members of a Microsoft Team in addition to placing the team mailbox (and site) on hold.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="032a8-p208">Microsoft 팀에서 채팅 목록의 일부인 대화에 참여 한 사용자는 사서함이 eDiscovery 보류에 있을 때 채팅 대화를 계속 하려면 Exchange Online (클라우드 기반) 사서함을 사용 해야 합니다. 채팅 목록의 일부인 대화는 채팅 참가자의 클라우드 기반 사서함에 저장 되기 때문입니다. 채팅 참가자에 게 Exchange Online 사서함이 없으면 채팅 대화를 유지할 수 없습니다. 예를 들어 Exchange 하이브리드 배포에서 온-프레미스 사서함이 있는 사용자는 Microsoft 팀의 채팅 목록에 속하는 대화에 참가할 수 있습니다. 그러나이 경우 사용자에 게 클라우드 기반 사서함이 없으므로 이러한 대화의 콘텐츠를 보존할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p208">Users who participate in conversations that are part of the Chat list in Microsoft Teams must have an Exchange Online (cloud-based) mailbox in order to retain chat conversations when the mailbox is placed on an eDiscovery hold. That's because conversations that are part of the Chat list are stored in the cloud-based mailboxes of the chat participants. If a chat participant doesn't have an Exchange Online mailbox, you won't be able to retain chat conversations. For example, in an Exchange hybrid deployment, users with an on-premises mailbox might be able to participate in conversations that are part of the Chat list in Microsoft Teams. However in this case, content from these conversation can't be retained because the users don't have cloud-based mailboxes.</span></span> 
  
  - <span data-ttu-id="032a8-p209">모든 Microsoft 팀 또는 팀 채널에는 노트 기록 및 공동 작업을 위한 Wiki가 포함 되어 있습니다. Wiki 콘텐츠가 .mht 형식의 파일에 자동으로 저장 됩니다. 이 파일은 팀의 SharePoint 사이트에 있는 팀 위 키 데이터 문서 라이브러리에 저장 됩니다. 팀의 SharePoint 사이트를 보류 하 여 해당 콘텐츠를 Wiki에 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p209">Every Microsoft Team or team channel contains a Wiki for note-taking and collaboration. The Wiki content is automatically saved to a file with a .mht format. This file is stored in the Teams Wiki Data document library on the team's SharePoint site. You can place the content in the Wiki on hold by placing the team's SharePoint site on hold.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="032a8-p210">Microsoft 팀 또는 팀 채널에 대 한 Wiki 콘텐츠를 보존 하는 기능 (팀의 SharePoint 사이트를 보류할 때)은 6 월 22 일에 릴리스 되었습니다. 팀 사이트를 보류 중인 경우에는 해당 날짜에 대해 Wiki 콘텐츠가 유지 됩니다. 그러나 팀 사이트가 유지 되 고 wiki 콘텐츠가 6 월 22 일 이전에 삭제 된 경우에는 wiki 콘텐츠가 보존 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p210">The capability to retain Wiki content for a Microsoft Team or team channel (when you place the team's SharePoint site on hold) was released on June 22, 2017. If a team site is on hold, the Wiki content will be retained starting on that date. However, if a team site is on hold and the Wiki content was deleted before June 22, 2017, the Wiki content was not retained.</span></span> 
  
- <span data-ttu-id="032a8-p211">**비즈니스용 OneDrive 사이트의 URL을 찾는 방법은 무엇 인가요?** eDiscovery 사례와 연결 된 보류 또는 검색에 추가할 수 있도록 조직의 비즈니스용 onedrive 사이트에 대 한 url 목록을 수집 하려면 [조직의 모든 OneDrive 위치 목록 만들기](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a)를 참조 하십시오. 이 문서에 나와 있는 스크립트는 모든 OneDrive 사이트의 목록이 포함 된 텍스트 파일을 만듭니다. 이 스크립트를 실행 하려면 SharePoint Online 관리 셸을 설치 하 고 사용 해야 합니다. 조직의 내 사이트 도메인에 대 한 URL을 검색 하려는 각 OneDrive 사이트로 추가 해야 합니다. 모든 OneDrive를 포함 하는 도메인입니다. 예를 `https://contoso-my.sharepoint.com`들면입니다. 다음은 사용자의 OneDrive 사이트에 대 한 URL의 예 `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`입니다.</span><span class="sxs-lookup"><span data-stu-id="032a8-p211">**How do I find the URL for OneDrive for Business sites?** To collect a list of the URLs for the OneDrive for Business sites in your organization so you can add them to a hold or search associated with an eDiscovery case, see [Create a list of all OneDrive locations in your organization](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). This script in this article creates a text file that contains a list of all OneDrive sites. To run this script, you'll have to install and use the SharePoint Online Management Shell. Be sure to append the URL for your organization's MySite domain to each OneDrive site that you want to search. This is the domain that contains all your OneDrive; for example,  `https://contoso-my.sharepoint.com`. Here's an example of a URL for a user's OneDrive site:  `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`.</span></span>
