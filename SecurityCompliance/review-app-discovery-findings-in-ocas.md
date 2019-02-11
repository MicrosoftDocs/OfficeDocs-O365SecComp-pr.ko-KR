---
title: Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: 고급 보안 관리에서 응용 프로그램 검색 보고서를 검토 하면 조직에서 사람들이 클라우드 앱을 사용 하는 방법에 대 한 자세한 내용은 할 수 있습니다. 로그 파일에서 방화벽 및 프록시를 사용 하 여 응용 프로그램 검색 보고서를 만든 후 app 검색 대시보드에서 결과 검토 합니다.
ms.openlocfilehash: 6195c9aae7ae5e398ac555cc820de04dee05d4fd
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603749"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a><span data-ttu-id="75601-104">Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토</span><span class="sxs-lookup"><span data-stu-id="75601-104">Review app discovery findings in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="75601-105">평가 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="75601-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="75601-106">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="75601-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="75601-107">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="75601-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="75601-108">사용률 \* \* \*</span><span class="sxs-lookup"><span data-stu-id="75601-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="75601-109">평가 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="75601-110">계획을 시작합니다</span><span class="sxs-lookup"><span data-stu-id="75601-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="75601-111">배포를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="75601-112">여기는!</span><span class="sxs-lookup"><span data-stu-id="75601-112">You are here!</span></span>  <br/> [<span data-ttu-id="75601-113">다음 단계</span><span class="sxs-lookup"><span data-stu-id="75601-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="75601-p102">클라우드 검색 대시보드 클라우드 앱 사용 현황에 대 한 자세한 정보를 제공 하려면 조직의 웹 트래픽 로그 작동 합니다. 전역 관리자, 보안 관리자 또는 보안 판독기 자신이 하 고 조직에 [Office 365 클라우드 응용 프로그램 보안에서 app 검색 보고서를 만든](create-app-discovery-reports-in-ocas.md), 클라우드 검색 대시보드를 사용 하에 대 한 정보를 얻을 수 하는 경우 어떻게 구성원 들이 프로그램 조직에는 Office 365 및 기타 클라우드 앱 사용 하는 합니다. (클라우드 검색 대시보드는로 알려져 생산성 응용 프로그램 검색 합니다.)</span><span class="sxs-lookup"><span data-stu-id="75601-p102">The Cloud Discovery dashboard works with your organization's web traffic logs to provide detailed information about cloud app usage. If you're a global administrator, security administrator, or security reader, and your organization has [created app discovery reports in Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md), you can use the Cloud Discovery dashboard to gain insight into how people in your organization are using Office 365 and other cloud apps. (The Cloud Discovery dashboard is also known as Productivity App Discovery.)</span></span>
  
 <span data-ttu-id="75601-117">클라우드 검색 대시보드를 사용 하면 조직에서 사람들이 Office 365 및 다른 응용 프로그램 사용 하는 방법에 대 한 자세한 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75601-117">The Cloud Discovery dashboard enables you to view detailed information about how people in your organization are using Office 365 and other apps.</span></span> 
  
![클라우드 검색 대시보드는 업데이트 된](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a><span data-ttu-id="75601-119">클라우드 검색 대시보드로 이동</span><span class="sxs-lookup"><span data-stu-id="75601-119">Go to the Cloud Discovery dashboard</span></span>

1. <span data-ttu-id="75601-120">클라우드 응용 프로그램 보안 포털에 이동 ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))에 로그인 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75601-120">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
    
2. <span data-ttu-id="75601-121">**검색** 으로 이동 \> **클라우드 검색 대시보드**합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-121">Go to **Discover** \> **Cloud Discovery dashboard**.</span></span>
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a><span data-ttu-id="75601-122">상위 사용자, IP 주소, 앱 및 위험 수준을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75601-122">See your top users, IP addresses, apps, and risk levels</span></span>

<span data-ttu-id="75601-123">클라우드 검색 대시보드 조직, open 알림, 상위 사용자 및 위험 수준에서 Office 365와 함께 사용 되는 응용 프로그램에서 한 눈 개요를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-123">The Cloud Discovery dashboard gives you an at-a-glance overview of apps that are used with Office 365 in your organization, any open alerts, top users, and risk levels.</span></span>
  
![클라우드 검색 dashboaard](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. <span data-ttu-id="75601-125">**대시보드** 탭에서 전체 화면의 위쪽에서 개요 섹션에 조직에서 전체 클라우드 응용 프로그램 사용에서 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="75601-125">On the **Dashboard** tab, look at the overall cloud app use in your organization in the overview section across the top of the screen.</span></span> 
    
2. <span data-ttu-id="75601-126">조직에서 사용 되는 응용 프로그램에 대 한 **Office 365 범주** 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75601-126">See the **Office 365 categories** for apps that are used in your organization.</span></span> 
    
3. <span data-ttu-id="75601-127">Office 365 및이 보기에 다른 응용 프로그램의 사용을 참조 하려면 **Discovered 앱** 위젯을 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="75601-127">Look at the **Discovered apps** widget to see usage of Office 365 and other apps in this view.</span></span> 
    
4. <span data-ttu-id="75601-128">Office 365를 사용 하 여 사서함과 클라우드 조직에 가장 앱 사용자에 게 식별 하는 **상위 사용자** 및 **위쪽 IP 주소** 위젯을 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="75601-128">Look at the **Top users** and **Top IP addresses** widget to identify those who use Office 365 and cloud apps the most in your organization.</span></span> 
    
5. <span data-ttu-id="75601-129">**앱 본사 위치** 맵을 사용 하 여 지리적 위치에 따라 사용자를 사용 하는 앱이 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75601-129">See where the apps people are using are by geographical location by using the **Apps headquarters location** map.</span></span> 
    
6. <span data-ttu-id="75601-p103">지도 영역 위에 **위험 수준** 개요에 포함 된 검색 된 앱의 위험 점수를 살펴보겠습니다. 동일한 그룹 및 범주 **Discovered 앱** 영역에서 사용 하 여 위험 볼 수 있습니다. 예, 높음, 중간 규모 또는 낮은 위험 앱에서 각 그룹화에서 트래픽 양과 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75601-p103">Above the maps area, take a look at the risk score of the discovered apps in the **Risk levels** overview. You can look at risks by the same groups and categories that you used in the **Discovered apps** area. For example, you can see how much traffic in each grouping is from high, medium, or low risk apps.</span></span> 
    
## <a name="dive-deeper-into-the-information"></a><span data-ttu-id="75601-133">정보 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="75601-133">Dive deeper into the information</span></span>

<span data-ttu-id="75601-134">앱, 하위 도메인, IP 주소 및 사용자에 대 한 상세한 정보를 적용 하려면 클라우드 검색을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75601-134">You can use Cloud Discovery to take a deeper look at apps, subdomains, IP addresses, and users.</span></span>
  
1. <span data-ttu-id="75601-135">클라우드 검색 대시보드에서 **Discovered 앱** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-135">In the Cloud Discovery dashboard, choose the **Discovered apps** tab.</span></span> 
    
2. <span data-ttu-id="75601-136">필터 섹션을 사용 하 여 앱 이름, 범주, 사용 현황 수준 또는 마지막으로 발생된 한 날짜를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75601-136">Use the filters section to view apps by name, category, usage level, or last seen date.</span></span>
    
3. <span data-ttu-id="75601-137">결과 목록에서 **하위 도메인 보기** 링크를 표시 하는 응용 프로그램 이름으로 가져갑니다.</span><span class="sxs-lookup"><span data-stu-id="75601-137">In the list of results, hover by an app name to reveal the **View sub-domains** link.</span></span><br/> <span data-ttu-id="75601-138">![하위 도메인 세부 정보를 보려면 링크를 표시 하는 응용 프로그램 옆에 있는 가리키기](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span><span class="sxs-lookup"><span data-stu-id="75601-138">![Hover next to an app to reveal a link to view subdomain details](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span></span><br/><span data-ttu-id="75601-139">선택한 응용 프로그램에 대 한 자세한 정보 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75601-139">Detailed information about the selected app will appear.</span></span>
    
4. <span data-ttu-id="75601-140">IP 주소에 대 한 세부 정보를 보려면 **IP 주소** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-140">To view details about IP addresses, choose the **IP addresses** tab.</span></span><br/><span data-ttu-id="75601-141">![IP 주소에 대 한 자세한 정보를 표시 하는 클라우드 검색](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span><span class="sxs-lookup"><span data-stu-id="75601-141">![Cloud Discovery shows detailed information about IP addresses](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span></span><br/><span data-ttu-id="75601-142">결과 목록에서 자세한 정보를 보려면 개별 IP 주소를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-142">In the list of results, select an individual IP address to view more detailed information.</span></span>
    
5. <span data-ttu-id="75601-143">조직 내에서 Office 365 사용자에 대 한 세부 정보를 보려면 **사용자** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-143">To view details about Office 365 users within your organization, choose the **Users** tab.</span></span><br/><span data-ttu-id="75601-144">![클라우드 검색-사용자가 정보](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span><span class="sxs-lookup"><span data-stu-id="75601-144">![Cloud Discovery - users info](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span></span>
  
## <a name="exclude-entities"></a><span data-ttu-id="75601-145">엔터티를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-145">Exclude entities</span></span>

<span data-ttu-id="75601-146">보다 구체적인 정보를 중점적으로 하기 위해 특정 사용자가 시스템 또는 IP 주소를 제외할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75601-146">You can exclude certain system users or IP addresses in order to focus on more specific information.</span></span>
  
1. <span data-ttu-id="75601-147">**설정** 을 선택 \> **클라우드 검색 설정**합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-147">Choose **Settings** \> **Cloud Discovery settings**.</span></span>
    
2. <span data-ttu-id="75601-148">**엔터티를 제외**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-148">Choose **Exclude entities**.</span></span>
    
3. <span data-ttu-id="75601-149">**제외 된 사용자** 또는 **제외 된 IP 주소**중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-149">Choose either **Excluded users** or **Excluded IP addresses**.</span></span>
    
4. <span data-ttu-id="75601-150">사용자 또는 IP 주소를 지정 하 고 **설명** 상자에 해당 사용자 또는 IP 주소를 제외한는 이유에 대 한 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-150">Specify the users or IP addresses, and in the **Comments** box, type information about why you are excluding those users or IP addresses.</span></span> 
    
5. <span data-ttu-id="75601-151">**Add(추가)** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-151">Choose **Add**.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="75601-152">다음 단계</span><span class="sxs-lookup"><span data-stu-id="75601-152">Next steps</span></span>

- [<span data-ttu-id="75601-153">검토 및 알림 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-153">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="75601-154">응용 프로그램 검색 보고서 만들기</span><span class="sxs-lookup"><span data-stu-id="75601-154">Create app discovery reports</span></span>](create-app-discovery-reports-in-ocas.md)
    
- <span data-ttu-id="75601-155">[Office 365 클라우드 응용 프로그램 보안에 대 한 사용률 활동](utilization-activities-for-ocas.md) 을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="75601-155">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

