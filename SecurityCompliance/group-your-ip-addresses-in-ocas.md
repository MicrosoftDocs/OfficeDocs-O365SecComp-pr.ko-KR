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
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220448"
---
# <a name="group-your-ip-addresses-to-simplify-management-in-office-365-cloud-app-security"></a><span data-ttu-id="0e64c-103">IP를 그룹화하여 Office 365 Cloud App Security 관리를 단순화</span><span class="sxs-lookup"><span data-stu-id="0e64c-103">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="0e64c-104">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="0e64c-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="0e64c-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="0e64c-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="0e64c-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="0e64c-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="0e64c-107">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="0e64c-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="0e64c-108">평가 시작</span><span class="sxs-lookup"><span data-stu-id="0e64c-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="0e64c-109">계획 시작</span><span class="sxs-lookup"><span data-stu-id="0e64c-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="0e64c-110">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="0e64c-110">You are here!</span></span>  <br/> [<span data-ttu-id="0e64c-111">다음 단계</span><span class="sxs-lookup"><span data-stu-id="0e64c-111">Next steps</span></span>](#next-steps) <br/> |[<span data-ttu-id="0e64c-112">활용 시작</span><span class="sxs-lookup"><span data-stu-id="0e64c-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="0e64c-p101">실제 office IP 주소와 같은 Office 365 Cloud App Security에서 사용 하는 ip 주소 집합을 쉽게 식별 하려면 IP 주소 범위의 그룹을 설정할 수 있습니다. 이러한 범위를 정의 하면 태그를 지정 하 고 분류할 수 있으며 태그 및 범주를 사용 하 여 활동 로그 및 경고를 표시 하 고 조사 하는 방법을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-p101">To easily identify sets of IP addresses that you'll use in Office 365 Cloud App Security, such as your physical office IP addresses, you can set up groups of IP address ranges. Defining these ranges lets you tag and categorize them, and then you can use tags and categories to customize how your activity logs and alerts are displayed and investigated.</span></span>
  
<span data-ttu-id="0e64c-p102">각 ip 범위 그룹은 선택한 태그 이름으로 태그가 지정 될 수 있으며,이 태그는 기본 IP 범주 목록 (예: 회사, 관리, 위험 및 VPN)을 기반으로 분류할 수 있습니다. IPv4 및 IPv6 주소가 모두 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-p102">Each group of IP ranges can be tagged with tag names that you choose, and then the tags can be categorized based on a default list of IP categories (such as Corporate, Administrative, Risky, and VPN). Both IPv4 and IPv6 addresses are supported.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0e64c-p103">이 문서의 절차를 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e64c-p103">You must be a global administrator or security administrator to perform the procedures in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="to-set-up-an-ip-address-range-in-office-365-cloud-app-security"></a><span data-ttu-id="0e64c-119">Office 365 Cloud App Security에서 IP 주소 범위를 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="0e64c-119">To set up an IP address range in Office 365 Cloud App Security</span></span>

1. <span data-ttu-id="0e64c-120">전역 관리자 또는 보안 관리자로 이동 하 여 Cloud App security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동한 후 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-120">As a global administrator or security administrator, go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
    
2. <span data-ttu-id="0e64c-121">페이지 오른쪽 위에서 **설정** \> **IP 주소 범위**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-121">On the upper right of the page, click **Settings** \> **IP address ranges**.</span></span><br><span data-ttu-id="0e64c-122">![O365 Cloud App Security에서 시스템 및 데이터 설정에 액세스 하기 위한 설정을 선택 합니다.](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)</span><span class="sxs-lookup"><span data-stu-id="0e64c-122">![In O365 Cloud App Security, choose Settings to access your system and data settings](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)</span></span><br>
  
3. <span data-ttu-id="0e64c-123">더하기 기호 ( **+**)와 같은 새로 만들기 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-123">Click the new button, which resembles a plus sign ( **+**).</span></span>
    
4. <span data-ttu-id="0e64c-124">**새 IP 주소 범위** 창에서 다음 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-124">In the **New IP address range** window, specify the following values:</span></span> 
    
|<span data-ttu-id="0e64c-125">**필드 또는 목록**</span><span class="sxs-lookup"><span data-stu-id="0e64c-125">**Field or list**</span></span>|<span data-ttu-id="0e64c-126">**수행할 작업**</span><span class="sxs-lookup"><span data-stu-id="0e64c-126">**What to do**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0e64c-127">**이름**</span><span class="sxs-lookup"><span data-stu-id="0e64c-127">**Name**</span></span> <br/> |<span data-ttu-id="0e64c-p104">이 필드를 사용 하 여 IP 주소 범위 및 설정을 관리 합니다. (이 값은 활동 로그에 표시 되지 않습니다.)</span><span class="sxs-lookup"><span data-stu-id="0e64c-p104">Use this field to manage your IP address range and settings. (You won't see this value in activities logs.)</span></span>  <br/> |
|<span data-ttu-id="0e64c-130">**IP 주소 범위**</span><span class="sxs-lookup"><span data-stu-id="0e64c-130">**IP address ranges**</span></span> <br/> |<span data-ttu-id="0e64c-p105">네트워크 접두사 표기법 (CIDR 표기법이 라고도 함)을 사용 하 여 범위를 지정 합니다. 예를 들어 192.168.1.0/27에는 192.168.1.31 (포함) 사이의 값 192.168.1.0이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-p105">Specify a range, using network prefix notation (also known as CIDR notation). For example, 192.168.1.0/27 includes the range of values 192.168.1.0 through 192.168.1.31 (inclusive).</span></span>  <br/> |
|<span data-ttu-id="0e64c-133">**위치** 및 **등록 된 ISP**</span><span class="sxs-lookup"><span data-stu-id="0e64c-133">**Location** and **Registered ISP**</span></span> <br/> |<span data-ttu-id="0e64c-p106">IP 주소 범위에 대 한 위치 및 ISP (인터넷 서비스 공급자)를 지정 합니다. 이는 주소에 대해 정의 된 공용 필드를 재정의 하며, IP 주소는 일반적으로 아일랜드에 있는 것으로 간주 되지만 실제로는 미국에 있는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-p106">Specify the location and Internet Service Provider (ISP) for the IP address range. This overrides the public fields defined for the addresses, which is helpful for cases, such as an IP address is that is considered publicly to be in Ireland but is actually in the U.S.</span></span>  <br/> |
|<span data-ttu-id="0e64c-136">**태그**</span><span class="sxs-lookup"><span data-stu-id="0e64c-136">**Tags**</span></span> <br/> |<span data-ttu-id="0e64c-p107">태그를 사용 하 여 IP 주소 그룹의 이름을 합니다. 이름 필드와 달리 작업 로그에 태그가 표시 됩니다. 태그에 사용할 단어나 구를 입력 합니다. 각 IP 주소 범위에 대해 원하는 만큼 태그를 추가할 수 있습니다. 이미 태그를 설정 했으며이 IP 주소 범위를 추가 하려면 입력을 시작할 때 표시 되는 현재 태그 목록에서이를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-p107">Use tags to name your groups of IP addresses. (Unlike the Name field, you will see Tags in activity logs.) Type a word or phrase that you want to use for a tag. You can add as many tags as you like for each IP address range. And if you've already set up a tag and you want to add this IP address range to it, choose it from the list of current tags that appear as you start typing.</span></span>  <br/> |
|<span data-ttu-id="0e64c-141">**범주**</span><span class="sxs-lookup"><span data-stu-id="0e64c-141">**Category**</span></span> <br/> | <span data-ttu-id="0e64c-p108">특정 IP 주소에서 제공 되는 활동을 보다 쉽게 인식할 수 있도록 태그에 범주를 할당 합니다. 다음 옵션 중에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-p108">Assign categories to your tags to make it easier to recognize activities that come from certain IP addresses. Choose from the following options:  </span></span><br/> <span data-ttu-id="0e64c-144">**관리** 관리자의 모든 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-144">**Administrative** All of the IP addresses of your admins.</span></span>  <br/> <span data-ttu-id="0e64c-145">**클라우드 공급자** 클라우드의 프록시 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-145">**Cloud provider** The IP address of your proxy in the cloud.</span></span>  <br/> <span data-ttu-id="0e64c-146">**회사** 내부 네트워크의 모든 IP 주소, 지점 사무소 및 wi-fi 로밍 주소</span><span class="sxs-lookup"><span data-stu-id="0e64c-146">**Corporate** All of the IP addresses in your internal network, your branch offices, and your Wi-Fi roaming addresses.</span></span>  <br/> <span data-ttu-id="0e64c-p109">**위험** 이전에 보았던 의심 스러운 ip 주소, 경쟁사의 네트워크에 있는 ip 주소 등 위험할 수 있다고 생각 되는 모든 ip 주소입니다. 기본적으로 위험한 범주에는 두 개의 IP 태그 ( **익명 프록시** 및 \*\*\*\* 받는 사람)가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-p109">**Risky** Any IP addresses that you consider to be risky, such as suspicious IP addresses you've seen in the past, IP addresses in your competitors' networks, and so on. By default, the Risky categories includes two IP tags: **Anonymous proxy** and **Tor**</span></span> <br/> <span data-ttu-id="0e64c-149">**VPN** 원격 작업자 들이 사용 하는 모든 IP 주소</span><span class="sxs-lookup"><span data-stu-id="0e64c-149">**VPN** Any IP addresses that your remote workers use.</span></span>  <br/> |
   
7. <span data-ttu-id="0e64c-150">**Save(저장)** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-150">Choose **Save**.</span></span>
    
<span data-ttu-id="0e64c-151">IP 주소 범위를 설정한 후에는 이러한 변경으로 인해 앞으로 발생 하는 이벤트만 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="0e64c-151">After you set up your IP address ranges, keep in mind that only future events are affected by these changes.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="0e64c-152">다음 단계</span><span class="sxs-lookup"><span data-stu-id="0e64c-152">Next steps</span></span>

- [<span data-ttu-id="0e64c-153">활동 정책 및 알림</span><span class="sxs-lookup"><span data-stu-id="0e64c-153">Activity policies and alerts</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="0e64c-154">변칙 검색 정책</span><span class="sxs-lookup"><span data-stu-id="0e64c-154">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="0e64c-155">siem 서버 통합</span><span class="sxs-lookup"><span data-stu-id="0e64c-155">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="0e64c-156">검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행</span><span class="sxs-lookup"><span data-stu-id="0e64c-156">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    

