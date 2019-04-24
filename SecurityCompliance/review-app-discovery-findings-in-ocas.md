---
title: Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: Office online의 앱 검색 보고서 검토 365 cloud app Security에서는 조직의 사용자가 클라우드 앱을 사용 하는 방법에 대해 자세히 알아볼 수 있습니다. 방화벽 및 프록시의 로그 파일을 사용 하 여 앱 검색 보고서를 만든 후에는 앱 검색 대시보드의 결과를 검토 하세요.
ms.openlocfilehash: f50ad372450b2a1404829eeb6f6964c1d954dccd
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264982"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a><span data-ttu-id="3160a-104">Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토</span><span class="sxs-lookup"><span data-stu-id="3160a-104">Review app discovery findings in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="3160a-105">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="3160a-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="3160a-106">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="3160a-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="3160a-107">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="3160a-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="3160a-108">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="3160a-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="3160a-109">평가 시작</span><span class="sxs-lookup"><span data-stu-id="3160a-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="3160a-110">계획 시작</span><span class="sxs-lookup"><span data-stu-id="3160a-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="3160a-111">배포 시작</span><span class="sxs-lookup"><span data-stu-id="3160a-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="3160a-112">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="3160a-112">You are here!</span></span>  <br/> [<span data-ttu-id="3160a-113">다음 단계</span><span class="sxs-lookup"><span data-stu-id="3160a-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="3160a-114">클라우드 검색 대시보드는 조직의 웹 트래픽 로그와 함께 작동 하 여 클라우드 앱 사용에 대 한 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-114">The Cloud Discovery dashboard works with your organization's web traffic logs to provide detailed information about cloud app usage.</span></span> <span data-ttu-id="3160a-115">전역 관리자, 보안 관리자 또는 보안 판독기이 고 조직에서 [Office 365 Cloud app security의 앱 검색 보고서를 만든](create-app-discovery-reports-in-ocas.md)경우 클라우드 검색 대시보드를 사용 하 여 사용자가 조직에서 Office 365 및 기타 클라우드 앱을 사용 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-115">If you're a global administrator, security administrator, or security reader, and your organization has [created app discovery reports in Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md), you can use the Cloud Discovery dashboard to gain insight into how people in your organization are using Office 365 and other cloud apps.</span></span> <span data-ttu-id="3160a-116">클라우드 검색 대시보드는 생산성 앱 검색으로도 알려져 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-116">(The Cloud Discovery dashboard is also known as Productivity App Discovery.)</span></span>
  
 <span data-ttu-id="3160a-117">클라우드 검색 대시보드를 사용 하 여 조직의 사용자가 Office 365 및 기타 앱을 사용 하는 방법에 대 한 자세한 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-117">The Cloud Discovery dashboard enables you to view detailed information about how people in your organization are using Office 365 and other apps.</span></span> 
  
![클라우드 검색 대시보드가 업데이트 되었습니다.](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a><span data-ttu-id="3160a-119">클라우드 검색 대시보드로 이동</span><span class="sxs-lookup"><span data-stu-id="3160a-119">Go to the Cloud Discovery dashboard</span></span>

1. <span data-ttu-id="3160a-120">Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-120">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
    
2. <span data-ttu-id="3160a-121">**클라우드 검색 대시보드** **검색** \> 으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-121">Go to **Discover** \> **Cloud Discovery dashboard**.</span></span>
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a><span data-ttu-id="3160a-122">상위 사용자, IP 주소, 앱 및 위험 수준 보기</span><span class="sxs-lookup"><span data-stu-id="3160a-122">See your top users, IP addresses, apps, and risk levels</span></span>

<span data-ttu-id="3160a-123">클라우드 검색 대시보드를 통해 조직의 Office 365, 열린 경고, 상위 사용자 및 위험 수준에 사용 되는 앱을 한눈에 파악할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-123">The Cloud Discovery dashboard gives you an at-a-glance overview of apps that are used with Office 365 in your organization, any open alerts, top users, and risk levels.</span></span>
  
![클라우드 검색 이점](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. <span data-ttu-id="3160a-125">**대시보드** 탭의 화면 위쪽에 있는 개요 섹션에서 조직에 사용 되는 전체 클라우드 앱을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-125">On the **Dashboard** tab, look at the overall cloud app use in your organization in the overview section across the top of the screen.</span></span> 
    
2. <span data-ttu-id="3160a-126">조직에서 사용 되는 앱에 대해서는 **Office 365 범주** 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3160a-126">See the **Office 365 categories** for apps that are used in your organization.</span></span> 
    
3. <span data-ttu-id="3160a-127">이 보기에서 Office 365 및 기타 앱을 사용 하는 방법을 확인 하려면 **검색 된 앱** 위젯을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="3160a-127">Look at the **Discovered apps** widget to see usage of Office 365 and other apps in this view.</span></span> 
    
4. <span data-ttu-id="3160a-128">**상위 사용자** 및 **상위 IP 주소** 위젯을 사용 하 여 조직에서 Office 365 및 클라우드 앱을 가장 많이 사용해 서 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-128">Look at the **Top users** and **Top IP addresses** widget to identify those who use Office 365 and cloud apps the most in your organization.</span></span> 
    
5. <span data-ttu-id="3160a-129">**앱 본사 위치** 맵을 사용 하 여 사용자가 사용 중인 앱이 지리적 위치를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-129">See where the apps people are using are by geographical location by using the **Apps headquarters location** map.</span></span> 
    
6. <span data-ttu-id="3160a-130">지도 영역 위에 표시 되는 **위험 수준** 개요에서 검색 된 앱의 위험 점수를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-130">Above the maps area, take a look at the risk score of the discovered apps in the **Risk levels** overview.</span></span> <span data-ttu-id="3160a-131">**검색 된 앱** 영역에서 사용한 것과 동일한 그룹 및 범주를 사용 하 여 위험을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-131">You can look at risks by the same groups and categories that you used in the **Discovered apps** area.</span></span> <span data-ttu-id="3160a-132">예를 들어, 상위, 중간 또는 낮은 위험 앱을 기준으로 각 그룹화의 트래픽 양을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-132">For example, you can see how much traffic in each grouping is from high, medium, or low risk apps.</span></span> 
    
## <a name="dive-deeper-into-the-information"></a><span data-ttu-id="3160a-133">정보에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="3160a-133">Dive deeper into the information</span></span>

<span data-ttu-id="3160a-134">클라우드 검색을 사용 하 여 앱, 하위 도메인, IP 주소 및 사용자에 대 한 자세한 내용을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-134">You can use Cloud Discovery to take a deeper look at apps, subdomains, IP addresses, and users.</span></span>
  
1. <span data-ttu-id="3160a-135">클라우드 검색 대시보드에서 **검색 된 앱** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-135">In the Cloud Discovery dashboard, choose the **Discovered apps** tab.</span></span> 
    
2. <span data-ttu-id="3160a-136">필터 섹션을 사용 하 여 이름, 범주, 사용 현황 수준 또는 마지막으로 본 날짜를 기준으로 앱을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-136">Use the filters section to view apps by name, category, usage level, or last seen date.</span></span>
    
3. <span data-ttu-id="3160a-137">결과 목록에서 응용 프로그램 이름을 가리켜 **하위 도메인 보기** 링크를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-137">In the list of results, hover by an app name to reveal the **View sub-domains** link.</span></span><br/> <span data-ttu-id="3160a-138">![하위 도메인 세부 정보를 볼 수 있는 링크를 나타내기 위해 앱 옆에 가리키기](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span><span class="sxs-lookup"><span data-stu-id="3160a-138">![Hover next to an app to reveal a link to view subdomain details](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span></span><br/><span data-ttu-id="3160a-139">선택한 앱에 대 한 자세한 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-139">Detailed information about the selected app will appear.</span></span>
    
4. <span data-ttu-id="3160a-140">ip 주소에 대 한 세부 정보를 보려면 **ip 주소** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-140">To view details about IP addresses, choose the **IP addresses** tab.</span></span><br/><span data-ttu-id="3160a-141">![클라우드 검색에서 IP 주소에 대 한 자세한 정보를 표시 합니다.](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span><span class="sxs-lookup"><span data-stu-id="3160a-141">![Cloud Discovery shows detailed information about IP addresses](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span></span><br/><span data-ttu-id="3160a-142">결과 목록에서 개별 IP 주소를 선택 하 여 더 자세한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-142">In the list of results, select an individual IP address to view more detailed information.</span></span>
    
5. <span data-ttu-id="3160a-143">조직 내 Office 365 사용자에 대 한 세부 정보를 보려면 **사용자** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-143">To view details about Office 365 users within your organization, choose the **Users** tab.</span></span><br/><span data-ttu-id="3160a-144">![클라우드 검색-사용자 정보](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span><span class="sxs-lookup"><span data-stu-id="3160a-144">![Cloud Discovery - users info](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span></span>
  
## <a name="exclude-entities"></a><span data-ttu-id="3160a-145">엔터티 제외</span><span class="sxs-lookup"><span data-stu-id="3160a-145">Exclude entities</span></span>

<span data-ttu-id="3160a-146">특정 시스템 사용자 또는 IP 주소를 제외 하 여 보다 구체적인 정보를 중점적으로 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-146">You can exclude certain system users or IP addresses in order to focus on more specific information.</span></span>
  
1. <span data-ttu-id="3160a-147">**설정** \> **클라우드 검색 설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-147">Choose **Settings** \> **Cloud Discovery settings**.</span></span>
    
2. <span data-ttu-id="3160a-148">**엔터티 제외**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-148">Choose **Exclude entities**.</span></span>
    
3. <span data-ttu-id="3160a-149">제외 된 **사용자** 또는 **제외 된 IP 주소**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-149">Choose either **Excluded users** or **Excluded IP addresses**.</span></span>
    
4. <span data-ttu-id="3160a-150">사용자 또는 ip 주소를 지정 하 고 **설명** 상자에 해당 사용자 또는 ip 주소를 제외 하는 이유에 대 한 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-150">Specify the users or IP addresses, and in the **Comments** box, type information about why you are excluding those users or IP addresses.</span></span> 
    
5. <span data-ttu-id="3160a-151">**추가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3160a-151">Choose **Add**.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="3160a-152">다음 단계</span><span class="sxs-lookup"><span data-stu-id="3160a-152">Next steps</span></span>

- [<span data-ttu-id="3160a-153">경고 검토 및 알림 작업 수행</span><span class="sxs-lookup"><span data-stu-id="3160a-153">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="3160a-154">앱 검색 보고서 만들기</span><span class="sxs-lookup"><span data-stu-id="3160a-154">Create app discovery reports</span></span>](create-app-discovery-reports-in-ocas.md)
    
- <span data-ttu-id="3160a-155">[Office 365 Cloud App Security에 대 한 사용률 작업](utilization-activities-for-ocas.md) 검토</span><span class="sxs-lookup"><span data-stu-id="3160a-155">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

