---
title: 'EOP에서 관리자 역할 그룹 보고서 실행 '
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 23b47b57-0eec-46a3-a03b-366ea014ab31
description: 관리자가 구성원을 관리자 역할 그룹에 추가하거나 그룹에서 제거하면 Microsoft EOP(Exchange Online Protection)에서 각 작업을 기록합니다.
ms.openlocfilehash: 5004851ec08afba7fcb26cbaefbe18f8c14e629a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153050"
---
# <a name="run-an-administrator-role-group-report-in-eop"></a><span data-ttu-id="0c2dd-103">EOP에서 관리자 역할 그룹 보고서 실행</span><span class="sxs-lookup"><span data-stu-id="0c2dd-103">Run an administrator role group report in EOP</span></span> 

 <span data-ttu-id="0c2dd-p101">관리자가 구성원을 관리자 역할 그룹에 추가하거나 그룹에서 제거하면 Microsoft EOP(Exchange Online Protection)에서 각 작업을 기록합니다. Exchange 관리 센터에서 관리자 역할 그룹 보고서를 실행하면 항목은 검색 결과로 표시되며 해당하는 역할 그룹, 역할 그룹 구성원을 변경한 사람과 시간, 그리고 구성원 업데이트 내용이 포함됩니다. 이 보고서를 사용하여 조직의 사용자에게 할당된 관리 권한의 변경을 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c2dd-p101">When an administrator adds members to or removes members from administrator role groups, Microsoft Exchange Online Protection (EOP) logs each occurrence. When you run an administrator role group report in the Exchange admin center, entries are displayed as search results and include the role groups affected, who changed the role group membership and when, and what membership updates were made. Use this report to monitor changes to the administrative permissions assigned to users in your organization.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="0c2dd-107">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="0c2dd-107">What do you need to know before you begin?</span></span>

- <span data-ttu-id="0c2dd-108">예상 완료 시간: 2분</span><span class="sxs-lookup"><span data-stu-id="0c2dd-108">Estimated time to complete: 2 minutes</span></span>
    
- <span data-ttu-id="0c2dd-p102">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인하려면 다음을 참조하세요. [EOP의 기능 사용 권한](feature-permissions-in-eop.md)의 "보고서" 섹션</span><span class="sxs-lookup"><span data-stu-id="0c2dd-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Reports" section of the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
    
- <span data-ttu-id="0c2dd-111">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Keyboard shortcuts in Exchange 2013**을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0c2dd-111">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="0c2dd-p103">문제가 있습니까? Exchange 포럼에서 도움을 요청하세요. 포럼 주소는 다음과 같습니다.[Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), 또는 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351)</span><span class="sxs-lookup"><span data-stu-id="0c2dd-p103">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="use-the-eac-to-run-an-administrator-role-group-report"></a><span data-ttu-id="0c2dd-115">EAC를 사용하여 관리자 역할 그룹 보고서 실행</span><span class="sxs-lookup"><span data-stu-id="0c2dd-115">Use the EAC to run an administrator role group report</span></span>

<span data-ttu-id="0c2dd-116">관리자 역할 그룹 보고서를 실행하여 특정 시간대 내 조직의 관리 역할 그룹 변경 내용을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c2dd-116">Run the administrator role group report to find the changes to management role groups in your organization within a particular timeframe.</span></span>
  
1. <span data-ttu-id="0c2dd-117">EAC에서 **준수 관리** \> **감사**로 이동한 후 **관리자 역할 그룹 보고서 실행**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0c2dd-117">In the EAC, navigate to **Compliance management** \> **Auditing**, and choose **Run an administrator role group report**.</span></span>
    
2. <span data-ttu-id="0c2dd-p104">**시작 날짜**와 **끝 날짜**를 선택합니다. 기본적으로 보고서는 지난 2주 동안의 관리자 역할 그룹 변경 내용을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0c2dd-p104">Choose the **Start date** and **End date**. By default, the report searches for changes made to administrator role groups in the past two weeks.</span></span>
    
3. <span data-ttu-id="0c2dd-p105">특정 역할 그룹에 대한 변경 내용을 보려면 **역할 그룹 선택**을 클릭합니다. 그러면 표시되는 대화 상자에서 역할 그룹을 하나 이상 선택하고 **확인**을 클릭합니다. 변경된 모든 역할 그룹을 찾으려는 경우에는 해당 필드를 비워 두면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c2dd-p105">To view the changes for a specific role group, click **Select role groups**. Select the role group (or groups) in the subsequent dialog box, and click **OK**. You can also leave the field blank to find all changed role groups.</span></span>
    
4. <span data-ttu-id="0c2dd-123">**검색**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="0c2dd-123">Click **Search**.</span></span>
    
<span data-ttu-id="0c2dd-p106">지정한 조건을 사용하여 찾은 변경 내용은 결과 창에 표시됩니다. 검색 결과에서 역할 그룹을 클릭하여 세부 정보 창에서 변경 내용을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="0c2dd-p106">If any changes are found using the criteria you specified, they will appear in the results pane. Click a role group in the search results to see the changes in the details pane.</span></span>
  
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="0c2dd-126">작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="0c2dd-126">How do you know this worked?</span></span>

<span data-ttu-id="0c2dd-p107">관리자 역할 그룹 보고서를 성공적으로 실행한 경우 날짜 범위 내에서 변경된 역할 그룹은 검색 결과 창에 표시됩니다. 결과가 표시되지 않으면 지정된 날짜 범위 내에서 역할 그룹이 변경되지 않은 것입니다. 표시할 결과가 있다고 생각되면 날짜 범위를 변경한 다음 보고서를 다시 실행하십시오.</span><span class="sxs-lookup"><span data-stu-id="0c2dd-p107">If you've successfully run an administrator role group report, role groups that have been changed within the date range are displayed in the search results pane. If there are no results, then no changes to role groups have taken place within the specified date range. If you think there should be results, change the date range and then run the report again.</span></span>
  
## <a name="monitor-changes-to-role-group-membership"></a><span data-ttu-id="0c2dd-130">역할 그룹 구성원의 변경 모니터링</span><span class="sxs-lookup"><span data-stu-id="0c2dd-130">Monitor changes to role group membership</span></span>

<span data-ttu-id="0c2dd-p108">구성원이 역할 그룹에서 추가되거나 제거되면 세부 정보 창에 표시되는 검색 결과에서 역할 그룹 구성원이 업데이트되었음이 표시되고 현재 구성원이 표시됩니다. 이 결과에서는 추가되거나 제거된 사용자가 명시적으로 나타나지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c2dd-p108">When members are added to or removed from a role group, the search results displayed in the details pane indicate that the role group membership was updated and lists the current members. The results don't explicitly state which user was added or removed.</span></span>
  
<span data-ttu-id="0c2dd-p109">사용자가 추가되었거나 제거되었는지 확인하려면 보고서에서 두 가지 항목을 비교해야 합니다. 예를 들어 **HelpDesk** 역할 그룹에 대한 다음 로그 항목을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="0c2dd-p109">To determine if a user was added or removed, you have to compare two separate entries in the report. For example, let's look at the following log entries for the **HelpDesk** role group:</span></span> 
  
 <span data-ttu-id="0c2dd-135">**2013/1/27 오후 4:43**</span><span class="sxs-lookup"><span data-stu-id="0c2dd-135">**1/27/2013 4:43 PM**</span></span>
  
 <span data-ttu-id="0c2dd-136">**관리자**</span><span class="sxs-lookup"><span data-stu-id="0c2dd-136">**Administrator**</span></span>
  
 <span data-ttu-id="0c2dd-137">**업데이트된 구성원: Administrator;annb,florencef;pilarp**</span><span class="sxs-lookup"><span data-stu-id="0c2dd-137">**Updated members: Administrator;annb,florencef;pilarp**</span></span>
  
 <span data-ttu-id="0c2dd-138">**2013/2/06 오전 10:09**</span><span class="sxs-lookup"><span data-stu-id="0c2dd-138">**2/06/2013 10:09 AM**</span></span>
  
 <span data-ttu-id="0c2dd-139">**관리자**</span><span class="sxs-lookup"><span data-stu-id="0c2dd-139">**Administrator**</span></span>
  
 <span data-ttu-id="0c2dd-140">**업데이트된 구성원: Administrator;annb;florencef;pilarp;tonip**</span><span class="sxs-lookup"><span data-stu-id="0c2dd-140">**Updated members: Administrator;annb;florencef;pilarp;tonip**</span></span>
  
 <span data-ttu-id="0c2dd-141">**2013/2/19 오후 2:12**</span><span class="sxs-lookup"><span data-stu-id="0c2dd-141">**2/19/2013 2:12 PM**</span></span>
  
 <span data-ttu-id="0c2dd-142">**관리자**</span><span class="sxs-lookup"><span data-stu-id="0c2dd-142">**Administrator**</span></span>
  
 <span data-ttu-id="0c2dd-143">**업데이트된 구성원: Administrator;annb;florencef;tonip**</span><span class="sxs-lookup"><span data-stu-id="0c2dd-143">**Updated members: Administrator;annb;florencef;tonip**</span></span>
  
<span data-ttu-id="0c2dd-144">이 예에서는 관리자 사용자 계정이 다음과 같은 변경을 수행했습니다.</span><span class="sxs-lookup"><span data-stu-id="0c2dd-144">In this example, the Administrator user account made the following changes:</span></span>
  
- <span data-ttu-id="0c2dd-145">2013년 2월 6일에 사용자 tonip을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="0c2dd-145">On 2/06/2013, it added the user tonip.</span></span>
    
- <span data-ttu-id="0c2dd-146">2013년 2월 19일에 사용자 pilarp를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="0c2dd-146">On 2/19/2013, it removed the user pilarp.</span></span>
    

