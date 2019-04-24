---
title: IP를 그룹화하여 Office 365 Cloud App Security 관리를 단순화
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: b5e1471c-1ad6-4bc5-9e75-ce791aee283c
description: 실제 office IP 주소와 같은 Office 365 Cloud App Security에서 사용 하는 ip 주소 집합을 쉽게 식별 하려면 IP 주소 범위의 그룹을 설정할 수 있습니다.
ms.openlocfilehash: b8f5c1dd46b2e3990d53a65881d12ca8f3961b16
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254864"
---
# <a name="group-your-ip-addresses-to-simplify-management-in-office-365-cloud-app-security"></a><span data-ttu-id="4967e-103">IP를 그룹화하여 Office 365 Cloud App Security 관리를 단순화</span><span class="sxs-lookup"><span data-stu-id="4967e-103">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="4967e-104">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="4967e-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="4967e-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="4967e-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="4967e-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="4967e-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="4967e-107">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4967e-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="4967e-108">평가 시작</span><span class="sxs-lookup"><span data-stu-id="4967e-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="4967e-109">계획 시작</span><span class="sxs-lookup"><span data-stu-id="4967e-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="4967e-110">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="4967e-110">You are here!</span></span>  <br/> [<span data-ttu-id="4967e-111">다음 단계</span><span class="sxs-lookup"><span data-stu-id="4967e-111">Next steps</span></span>](#next-steps) <br/> |[<span data-ttu-id="4967e-112">활용 시작</span><span class="sxs-lookup"><span data-stu-id="4967e-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="4967e-113">실제 office IP 주소와 같은 Office 365 Cloud App Security에서 사용 하는 ip 주소 집합을 쉽게 식별 하려면 IP 주소 범위의 그룹을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-113">To easily identify sets of IP addresses that you'll use in Office 365 Cloud App Security, such as your physical office IP addresses, you can set up groups of IP address ranges.</span></span> <span data-ttu-id="4967e-114">이러한 범위를 정의 하면 태그를 지정 하 고 분류할 수 있으며 태그 및 범주를 사용 하 여 활동 로그 및 경고를 표시 하 고 조사 하는 방법을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-114">Defining these ranges lets you tag and categorize them, and then you can use tags and categories to customize how your activity logs and alerts are displayed and investigated.</span></span>
  
<span data-ttu-id="4967e-115">각 ip 범위 그룹은 선택한 태그 이름으로 태그가 지정 될 수 있으며,이 태그는 기본 IP 범주 목록 (예: 회사, 관리, 위험 및 VPN)을 기반으로 분류할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-115">Each group of IP ranges can be tagged with tag names that you choose, and then the tags can be categorized based on a default list of IP categories (such as Corporate, Administrative, Risky, and VPN).</span></span> <span data-ttu-id="4967e-116">IPv4 및 IPv6 주소가 모두 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-116">Both IPv4 and IPv6 addresses are supported.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4967e-117">이 문서의 절차를 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-117">You must be a global administrator or security administrator to perform the procedures in this article.</span></span> <span data-ttu-id="4967e-118">자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4967e-118">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="to-set-up-an-ip-address-range-in-office-365-cloud-app-security"></a><span data-ttu-id="4967e-119">Office 365 Cloud App Security에서 IP 주소 범위를 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="4967e-119">To set up an IP address range in Office 365 Cloud App Security</span></span>

1. <span data-ttu-id="4967e-120">전역 관리자 또는 보안 관리자로 이동 하 여 Cloud App security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동한 후 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-120">As a global administrator or security administrator, go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
    
2. <span data-ttu-id="4967e-121">페이지 오른쪽 위에서 **설정** \> **IP 주소 범위**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-121">On the upper right of the page, click **Settings** \> **IP address ranges**.</span></span><br><span data-ttu-id="4967e-122">![O365 Cloud App Security에서 시스템 및 데이터 설정에 액세스 하기 위한 설정을 선택 합니다.](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)</span><span class="sxs-lookup"><span data-stu-id="4967e-122">![In O365 Cloud App Security, choose Settings to access your system and data settings](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)</span></span><br>
  
3. <span data-ttu-id="4967e-123">더하기 기호 ( **+**)와 같은 새로 만들기 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-123">Click the new button, which resembles a plus sign ( **+**).</span></span>
    
4. <span data-ttu-id="4967e-124">**새 IP 주소 범위** 창에서 다음 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-124">In the **New IP address range** window, specify the following values:</span></span> 
    
|<span data-ttu-id="4967e-125">**필드 또는 목록**</span><span class="sxs-lookup"><span data-stu-id="4967e-125">**Field or list**</span></span>|<span data-ttu-id="4967e-126">**수행할 작업**</span><span class="sxs-lookup"><span data-stu-id="4967e-126">**What to do**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4967e-127">**이름**</span><span class="sxs-lookup"><span data-stu-id="4967e-127">**Name**</span></span> <br/> |<span data-ttu-id="4967e-128">이 필드를 사용 하 여 IP 주소 범위 및 설정을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-128">Use this field to manage your IP address range and settings.</span></span> <span data-ttu-id="4967e-129">(이 값은 활동 로그에 표시 되지 않습니다.)</span><span class="sxs-lookup"><span data-stu-id="4967e-129">(You won't see this value in activities logs.)</span></span>  <br/> |
|<span data-ttu-id="4967e-130">**IP 주소 범위**</span><span class="sxs-lookup"><span data-stu-id="4967e-130">**IP address ranges**</span></span> <br/> |<span data-ttu-id="4967e-131">네트워크 접두사 표기법 (CIDR 표기법이 라고도 함)을 사용 하 여 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-131">Specify a range, using network prefix notation (also known as CIDR notation).</span></span> <span data-ttu-id="4967e-132">예를 들어 192.168.1.0/27에는 192.168.1.31 (포함) 사이의 값 192.168.1.0이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-132">For example, 192.168.1.0/27 includes the range of values 192.168.1.0 through 192.168.1.31 (inclusive).</span></span>  <br/> |
|<span data-ttu-id="4967e-133">**위치** 및 **등록 된 ISP**</span><span class="sxs-lookup"><span data-stu-id="4967e-133">**Location** and **Registered ISP**</span></span> <br/> |<span data-ttu-id="4967e-134">IP 주소 범위에 대 한 위치 및 ISP (인터넷 서비스 공급자)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-134">Specify the location and Internet Service Provider (ISP) for the IP address range.</span></span> <span data-ttu-id="4967e-135">이는 주소에 대해 정의 된 공용 필드를 재정의 하며, IP 주소는 일반적으로 아일랜드에 있는 것으로 간주 되지만 실제로는 미국에 있는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-135">This overrides the public fields defined for the addresses, which is helpful for cases, such as an IP address is that is considered publicly to be in Ireland but is actually in the U.S.</span></span>  <br/> |
|<span data-ttu-id="4967e-136">**사이**</span><span class="sxs-lookup"><span data-stu-id="4967e-136">**Tags**</span></span> <br/> |<span data-ttu-id="4967e-137">태그를 사용 하 여 IP 주소 그룹의 이름을 합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-137">Use tags to name your groups of IP addresses.</span></span> <span data-ttu-id="4967e-138">이름 필드와 달리 작업 로그에 태그가 표시 됩니다. 태그에 사용할 단어나 구를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-138">(Unlike the Name field, you will see Tags in activity logs.) Type a word or phrase that you want to use for a tag.</span></span> <span data-ttu-id="4967e-139">각 IP 주소 범위에 대해 원하는 만큼 태그를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-139">You can add as many tags as you like for each IP address range.</span></span> <span data-ttu-id="4967e-140">이미 태그를 설정 했으며이 IP 주소 범위를 추가 하려면 입력을 시작할 때 표시 되는 현재 태그 목록에서이를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-140">And if you've already set up a tag and you want to add this IP address range to it, choose it from the list of current tags that appear as you start typing.</span></span>  <br/> |
|<span data-ttu-id="4967e-141">**종류**</span><span class="sxs-lookup"><span data-stu-id="4967e-141">**Category**</span></span> <br/> | <span data-ttu-id="4967e-142">특정 IP 주소에서 제공 되는 활동을 보다 쉽게 인식할 수 있도록 태그에 범주를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-142">Assign categories to your tags to make it easier to recognize activities that come from certain IP addresses.</span></span> <span data-ttu-id="4967e-143">다음 옵션 중에서 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-143">Choose from the following options:</span></span>  <br/> <span data-ttu-id="4967e-144">**관리** 관리자의 모든 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-144">**Administrative** All of the IP addresses of your admins.</span></span>  <br/> <span data-ttu-id="4967e-145">**클라우드 공급자** 클라우드의 프록시 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-145">**Cloud provider** The IP address of your proxy in the cloud.</span></span>  <br/> <span data-ttu-id="4967e-146">**회사** 내부 네트워크의 모든 IP 주소, 지점 사무소 및 wi-fi 로밍 주소</span><span class="sxs-lookup"><span data-stu-id="4967e-146">**Corporate** All of the IP addresses in your internal network, your branch offices, and your Wi-Fi roaming addresses.</span></span>  <br/> <span data-ttu-id="4967e-147">**위험** 이전에 보았던 의심 스러운 ip 주소, 경쟁사의 네트워크에 있는 ip 주소 등 위험할 수 있다고 생각 되는 모든 ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-147">**Risky** Any IP addresses that you consider to be risky, such as suspicious IP addresses you've seen in the past, IP addresses in your competitors' networks, and so on.</span></span> <span data-ttu-id="4967e-148">기본적으로 위험한 범주에는 두 개의 IP 태그 ( **익명 프록시** 및 \*\*\*\* 받는 사람)가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-148">By default, the Risky categories includes two IP tags: **Anonymous proxy** and **Tor**</span></span> <br/> <span data-ttu-id="4967e-149">**VPN** 원격 작업자 들이 사용 하는 모든 IP 주소</span><span class="sxs-lookup"><span data-stu-id="4967e-149">**VPN** Any IP addresses that your remote workers use.</span></span>  <br/> |
   
7. <span data-ttu-id="4967e-150">**저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-150">Choose **Save**.</span></span>
    
<span data-ttu-id="4967e-151">IP 주소 범위를 설정한 후에는 이러한 변경으로 인해 앞으로 발생 하는 이벤트만 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="4967e-151">After you set up your IP address ranges, keep in mind that only future events are affected by these changes.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="4967e-152">다음 단계</span><span class="sxs-lookup"><span data-stu-id="4967e-152">Next steps</span></span>

- [<span data-ttu-id="4967e-153">활동 정책 및 알림</span><span class="sxs-lookup"><span data-stu-id="4967e-153">Activity policies and alerts</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="4967e-154">변칙 검색 정책</span><span class="sxs-lookup"><span data-stu-id="4967e-154">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="4967e-155">siem 서버 통합</span><span class="sxs-lookup"><span data-stu-id="4967e-155">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="4967e-156">검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행</span><span class="sxs-lookup"><span data-stu-id="4967e-156">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    

