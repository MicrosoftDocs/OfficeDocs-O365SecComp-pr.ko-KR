---
title: IP를 그룹화하여 Office 365 Cloud App Security 관리를 단순화
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: b5e1471c-1ad6-4bc5-9e75-ce791aee283c
description: 집합의 실제 사무실 IP 주소를 사용 하 여 같은 Office 365 클라우드 응용 프로그램 보안에 사용할 IP 주소를 쉽게 식별할 수 IP 주소 범위는 그룹을 설정할 수 있습니다.
ms.openlocfilehash: 76cb9625a46d1f5eceaab696de5dcbb72f4d2b47
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532919"
---
# <a name="group-your-ip-addresses-to-simplify-management-in-office-365-cloud-app-security"></a><span data-ttu-id="79533-103">IP를 그룹화하여 Office 365 Cloud App Security 관리를 단순화</span><span class="sxs-lookup"><span data-stu-id="79533-103">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="79533-104">평가 * *\>**</span><span class="sxs-lookup"><span data-stu-id="79533-104">****Evaluation** \>**</span></span>|<span data-ttu-id="79533-105">계획 * *\>**</span><span class="sxs-lookup"><span data-stu-id="79533-105">****Planning** \>**</span></span>|<span data-ttu-id="79533-106">배포 * *\>**</span><span class="sxs-lookup"><span data-stu-id="79533-106">****Deployment** \>**</span></span>|<span data-ttu-id="79533-107">사용률 \* \* \*</span><span class="sxs-lookup"><span data-stu-id="79533-107">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="79533-108">평가 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="79533-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="79533-109">계획을 시작합니다</span><span class="sxs-lookup"><span data-stu-id="79533-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="79533-110">여기는!</span><span class="sxs-lookup"><span data-stu-id="79533-110">You are here!</span></span>  <br/> [<span data-ttu-id="79533-111">다음 단계</span><span class="sxs-lookup"><span data-stu-id="79533-111">Next steps</span></span>](#next-steps) <br/> |[<span data-ttu-id="79533-112">활용 하 여 시작</span><span class="sxs-lookup"><span data-stu-id="79533-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="79533-p101">집합의 실제 사무실 IP 주소를 사용 하 여 같은 Office 365 클라우드 응용 프로그램 보안에 사용할 IP 주소를 쉽게 식별할 수 IP 주소 범위는 그룹을 설정할 수 있습니다. 정의 이러한 범위 수 있음 태그를 지정 하 고, 분류 하 고 태그를 사용할 수 있습니다 및 작업 로그 및 경고 방법을 사용자 지정 하는 범주를 표시 하 고 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="79533-p101">To easily identify sets of IP addresses that you'll use in Office 365 Cloud App Security, such as your physical office IP addresses, you can set up groups of IP address ranges. Defining these ranges lets you tag and categorize them, and then you can use tags and categories to customize how your activity logs and alerts are displayed and investigated.</span></span>
  
<span data-ttu-id="79533-p102">IP 범위를 가진 각 그룹을 선택 하 고 다음 태그 분류할 수 있습니다 (예: 회사, 관리, Risky, 및 VPN) IP 범주의 기본 목록을 기반으로 하는 태그 이름으로 태그가 지정 된 수 있습니다. IPv4 및 IPv6 주소를 모두 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="79533-p102">Each group of IP ranges can be tagged with tag names that you choose, and then the tags can be categorized based on a default list of IP categories (such as Corporate, Administrative, Risky, and VPN). Both IPv4 and IPv6 addresses are supported.</span></span>
  
> [!NOTE]
> <span data-ttu-id="79533-p103">이 문서의 절차를 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다. 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="79533-p103">You must be a global administrator or security administrator to perform the procedures in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="to-set-up-an-ip-address-range-in-office-365-cloud-app-security"></a><span data-ttu-id="79533-119">Office 365 클라우드 응용 프로그램 보안의 IP 주소 범위를 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="79533-119">To set up an IP address range in Office 365 Cloud App Security</span></span>

1. <span data-ttu-id="79533-p104">전역 관리자 또는 보안 관리자로 이동 [https://protection.office.com](https://protection.office.com) 작업이 나 교육용 계정을 사용 하 여 로그인 하 고 있습니다. (이렇게 하면 보안 &amp; 준수 센터.)</span><span class="sxs-lookup"><span data-stu-id="79533-p104">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="79533-122">보안에서 &amp; 준수 센터 **알림** 선택 \> **관리 고급 알림**입니다.</span><span class="sxs-lookup"><span data-stu-id="79533-122">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="79533-123">**Office 365 클라우드 응용 프로그램 보안으로 이동**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="79533-123">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
    ![보안에서 &amp; 준수 센터 Office 365 클라우드 앱 보안으로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. <span data-ttu-id="79533-125">페이지의 오른쪽 위에서 **설정** 을 클릭 \> **IP 주소 범위**입니다.</span><span class="sxs-lookup"><span data-stu-id="79533-125">On the upper right of the page, click **Settings** \> **IP address ranges**.</span></span>
    
    ![O 365 클라우드 응용 프로그램 보안에서 시스템 및 데이터 설정에 액세스 하는 설정을 선택합니다](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)
  
5. <span data-ttu-id="79533-127">더하기 기호를 비슷한 새 단추를 클릭 ( **+**).</span><span class="sxs-lookup"><span data-stu-id="79533-127">Click the new button, which resembles a plus sign ( **+**).</span></span>
    
6. <span data-ttu-id="79533-128">**새 IP 주소 범위** 창에서 다음 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79533-128">In the **New IP address range** window, specify the following values:</span></span> 
    
|<span data-ttu-id="79533-129">**필드 또는 목록**</span><span class="sxs-lookup"><span data-stu-id="79533-129">**Field or list**</span></span>|<span data-ttu-id="79533-130">**수행할 작업**</span><span class="sxs-lookup"><span data-stu-id="79533-130">**What to do**</span></span>|
|:-----|:-----|
|<span data-ttu-id="79533-131">**이름**</span><span class="sxs-lookup"><span data-stu-id="79533-131">**Name**</span></span> <br/> |<span data-ttu-id="79533-p105">이 필드를 사용 하 여 IP 주소 범위 및 설정을 관리할 수 있습니다. (활동 로그에이 값을 표시 되지 않습니다.)</span><span class="sxs-lookup"><span data-stu-id="79533-p105">Use this field to manage your IP address range and settings. (You won't see this value in activities logs.)</span></span>  <br/> |
|<span data-ttu-id="79533-134">**IP 주소 범위**</span><span class="sxs-lookup"><span data-stu-id="79533-134">**IP address ranges**</span></span> <br/> |<span data-ttu-id="79533-p106">네트워크 접두사 표기법 (CIDR 표기법 라고도 함)를 사용 하 여 범위를 지정 합니다. 예, 192.168.1.0/27 192.168.1.31 (포함)을 통해 192.168.1.0 값의 범위를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="79533-p106">Specify a range, using network prefix notation (also known as CIDR notation). For example, 192.168.1.0/27 includes the range of values 192.168.1.0 through 192.168.1.31 (inclusive).</span></span>  <br/> |
|<span data-ttu-id="79533-137">**위치** 및 **ISP에 등록**</span><span class="sxs-lookup"><span data-stu-id="79533-137">**Location** and **Registered ISP**</span></span> <br/> |<span data-ttu-id="79533-p107">IP 주소 범위에 대 한 위치 및 인터넷 서비스 공급자 (ISP)를 지정 합니다. 와 같이 IP 주소는 공개적으로 아일랜드 될 것으로 간주 됩니다 이지만 실제로 미국에서의 경우에 대 한 유용한은 공용 필드의 주소에 대해 정의 된 재정의</span><span class="sxs-lookup"><span data-stu-id="79533-p107">Specify the location and Internet Service Provider (ISP) for the IP address range. This overrides the public fields defined for the addresses, which is helpful for cases, such as an IP address is that is considered publicly to be in Ireland but is actually in the U.S.</span></span>  <br/> |
|<span data-ttu-id="79533-140">**태그**</span><span class="sxs-lookup"><span data-stu-id="79533-140">**Tags**</span></span> <br/> |<span data-ttu-id="79533-p108">태그를 사용 하 여 IP 주소 그룹의 이름을 지정 합니다. (이름 필드와는 달리 태그의에서 나타납니다 기록을.) 단어 또는 구를 태그를 사용 하려는 입력 합니다. 각 IP 주소 범위에 대해 원하는 만큼의 태그를 추가할 수 있습니다. 및 태그를 이미 설정 했을 때이 IP 주소 범위를 추가 하려는 경우 입력을 시작 하면 표시 되는 현재 태그의 목록에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="79533-p108">Use tags to name your groups of IP addresses. (Unlike the Name field, you will see Tags in activity logs.) Type a word or phrase that you want to use for a tag. You can add as many tags as you like for each IP address range. And if you've already set up a tag and you want to add this IP address range to it, choose it from the list of current tags that appear as you start typing.</span></span>  <br/> |
|<span data-ttu-id="79533-145">**종류**</span><span class="sxs-lookup"><span data-stu-id="79533-145">**Category**</span></span> <br/> | <span data-ttu-id="79533-p109">특정 IP 주소에서 제공 하는 활동을 인식 하도록 쉽게 수행할 수 있도록 태그에 범주를 할당 합니다. 다음 옵션 중에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="79533-p109">Assign categories to your tags to make it easier to recognize activities that come from certain IP addresses. Choose from the following options:  </span></span><br/> <span data-ttu-id="79533-148">**관리** 모든 사용자 admins 그룹의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="79533-148">**Administrative** All of the IP addresses of your admins.</span></span>  <br/> <span data-ttu-id="79533-149">**클라우드 공급자** 클라우드에서 프록시의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="79533-149">**Cloud provider** The IP address of your proxy in the cloud.</span></span>  <br/> <span data-ttu-id="79533-150">**회사** 모든 IP 주소를 내부 네트워크, 지사에서 및 Wi-fi 로밍 주소.</span><span class="sxs-lookup"><span data-stu-id="79533-150">**Corporate** All of the IP addresses in your internal network, your branch offices, and your Wi-Fi roaming addresses.</span></span>  <br/> <span data-ttu-id="79533-p110">**Risky를 찾습니다.** 하면 의심 스러운 IP 주소와 같은 위험한, 수를 고려 하는 모든 IP 주소 경쟁 업체의 네트워크의 IP 주소에 이전에 본 하 고 등입니다. 기본적으로 위험한 범주에 포함 되어 두 IP 태그: **익명 프록시** 및 **에**</span><span class="sxs-lookup"><span data-stu-id="79533-p110">**Risky** Any IP addresses that you consider to be risky, such as suspicious IP addresses you've seen in the past, IP addresses in your competitors' networks, and so on. By default, the Risky categories includes two IP tags: **Anonymous proxy** and **Tor**</span></span> <br/> <span data-ttu-id="79533-153">**VPN** 원격 작업 자가 사용 하는 모든 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="79533-153">**VPN** Any IP addresses that your remote workers use.</span></span>  <br/> |
   
7. <span data-ttu-id="79533-154">**저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="79533-154">Choose **Save**.</span></span>
    
<span data-ttu-id="79533-155">IP 주소 범위를 설정 하면 염두에 향후 이벤트는 이러한 변경 내용에 영향을 합니다.</span><span class="sxs-lookup"><span data-stu-id="79533-155">After you set up your IP address ranges, keep in mind that only future events are affected by these changes.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="79533-156">다음 단계</span><span class="sxs-lookup"><span data-stu-id="79533-156">Next steps</span></span>

- [<span data-ttu-id="79533-157">활동 정책 및 알림</span><span class="sxs-lookup"><span data-stu-id="79533-157">Activity policies and alerts</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="79533-158">예외 탐지 정책</span><span class="sxs-lookup"><span data-stu-id="79533-158">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="79533-159">SIEM 서버 통합</span><span class="sxs-lookup"><span data-stu-id="79533-159">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="79533-160">검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행</span><span class="sxs-lookup"><span data-stu-id="79533-160">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    

