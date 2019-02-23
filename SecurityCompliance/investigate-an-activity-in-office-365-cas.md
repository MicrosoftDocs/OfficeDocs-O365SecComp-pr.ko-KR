---
title: Office 365 Cloud App Security에서 활동 조사
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 15fa4545-28b4-4dd4-bf85-88e0926bd5fc
description: 'office 365 Cloud App Security를 사용 하 여 office 365 환경에서 활동과 계정을 확인 하 여 어떤 일이 일어나는지 볼 수 있습니다. '
ms.openlocfilehash: 0cc3860d953b40b0b0c247af6fb2b157d1abb235
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218968"
---
# <a name="investigate-an-activity-in-office-365-cloud-app-security"></a><span data-ttu-id="b5f60-103">Office 365 Cloud App Security에서 활동 조사</span><span class="sxs-lookup"><span data-stu-id="b5f60-103">Investigate an activity in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="b5f60-104">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b5f60-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="b5f60-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b5f60-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="b5f60-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b5f60-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="b5f60-107">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b5f60-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="b5f60-108">평가 시작</span><span class="sxs-lookup"><span data-stu-id="b5f60-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="b5f60-109">계획 시작</span><span class="sxs-lookup"><span data-stu-id="b5f60-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="b5f60-110">배포 시작</span><span class="sxs-lookup"><span data-stu-id="b5f60-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="b5f60-111">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="b5f60-111">You are here!</span></span>  <br/> [<span data-ttu-id="b5f60-112">다음 단계</span><span class="sxs-lookup"><span data-stu-id="b5f60-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="b5f60-p101">office 365 Cloud App Security는 [office 365 감사 로그](detailed-properties-in-the-office-365-audit-log.md)에서 작동 합니다. 전역 관리자 또는 보안 관리자 인 Office 365 Cloud App Security를 사용 하 여 조직에서 Office 365을 사용 하는 방법에 대 한 잠재적인 문제를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5f60-p101">Office 365 Cloud App Security works with your [Office 365 audit log](detailed-properties-in-the-office-365-audit-log.md). With Office 365 Cloud App Security, as a global administrator or security administrator, you can use the Activity log page to see potential issues in how your organization is using Office 365.</span></span>
  
## <a name="how-to-get-to-the-activity-log-page"></a><span data-ttu-id="b5f60-115">활동 로그 페이지에 액세스 하는 방법</span><span class="sxs-lookup"><span data-stu-id="b5f60-115">How to get to the Activity log page</span></span>

1. <span data-ttu-id="b5f60-116">Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5f60-116">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="b5f60-117">화면 위쪽의 탐색 모음에서 **작업 로그** **조사** \> 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5f60-117">In the navigation bar across the top of the screen, choose **Investigate** \> **Activity log**.</span></span><br/><span data-ttu-id="b5f60-118">![O365 CAS 포털에서 조사를 선택 합니다.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span><span class="sxs-lookup"><span data-stu-id="b5f60-118">![In the O365 CAS portal, choose Investigate.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span></span>
  
## <a name="review-and-investigate-activities"></a><span data-ttu-id="b5f60-119">활동 검토 및 조사</span><span class="sxs-lookup"><span data-stu-id="b5f60-119">Review and investigate activities</span></span>

<span data-ttu-id="b5f60-p102">활동 로그 페이지에서는 Office 365을 사용 하 여 조직 내에서 수행 되는 다양 한 활동 목록을 볼 수 있습니다. 화면 맨 위에 필터를 사용 하 여 특정 유형의 활동 또는 특정 사용자에 집중할 수 있습니다. 예를 들어 다음 이미지에는 조직의 Office 365 관리자 계정의 암호 변경에 대 한 정보가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5f60-p102">On the Activity log page, you can see a list of various activities that are taking place within your organization using Office 365. You can use filters across the top of the screen to focus on a specific type of activity or a specific user. For example, the following image shows information about an organization's Office 365 admin account's password change:</span></span>
  
![Office 365 Cloud App Security에서 활동 로그 조사 \> 를 선택 합니다.](media/5d54600c-59cd-4f33-b4f0-29b75c37baae.png)
  
<span data-ttu-id="b5f60-p103">활동 로그의 각 항목을 살펴보면 줄임표를 클릭 하 여 기타 관련 활동을 찾을 수 있습니다. 예를 들어 동일한 IP 주소 또는 동일한 국가/지역에서 같은 유형의 다른 활동을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5f60-p103">As you look at each item in the Activity log, you can click the ellipses to find other related activities. For example, you can view other activities of the same type, from the same IP address, or from the same country/region.</span></span>
  
<span data-ttu-id="b5f60-p104">다른 여러 종류의 작업에 대 한 정보도 볼 수 있습니다. 예를 들어 다음은 활동 로그에서 확인할 수 있는 몇 가지 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b5f60-p104">You can view information about many other kinds of activities, too. For example, here are some of the activities you can view in the Activity log:</span></span>
  
- <span data-ttu-id="b5f60-128">그룹에서 추가 되거나 제거 된 구성원</span><span class="sxs-lookup"><span data-stu-id="b5f60-128">Members added to or removed from groups</span></span>
    
- <span data-ttu-id="b5f60-129">사용자 라이선스 변경 사항</span><span class="sxs-lookup"><span data-stu-id="b5f60-129">Changes in user licenses</span></span>
    
- <span data-ttu-id="b5f60-130">내부 또는 외부적으로 공유 되는 파일 또는 폴더</span><span class="sxs-lookup"><span data-stu-id="b5f60-130">Files or folders shared internally or externally</span></span>
    
- <span data-ttu-id="b5f60-131">만들거나 삭제 한 사이트 또는 사이트 모음</span><span class="sxs-lookup"><span data-stu-id="b5f60-131">Created or deleted sites or site collections</span></span>
    
- <span data-ttu-id="b5f60-132">전자 메일 전달 규칙</span><span class="sxs-lookup"><span data-stu-id="b5f60-132">Email forwarding rules</span></span>
    
<span data-ttu-id="b5f60-133">활동 로그 페이지를 사용 하 여 조직의 사용자가 Office 365를 사용 하는 방법 및 해당 방식에 따라 발생할 수 있는 문제를 파악 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5f60-133">Use the Activity log page to get acquainted with how people in your organization are using Office 365 and what issues they might be having along the way.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="b5f60-134">다음 단계</span><span class="sxs-lookup"><span data-stu-id="b5f60-134">Next steps</span></span>

- [<span data-ttu-id="b5f60-135">검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행</span><span class="sxs-lookup"><span data-stu-id="b5f60-135">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="b5f60-136">[Office 365 Cloud App Security에 대 한 사용률 작업](utilization-activities-for-ocas.md) 검토</span><span class="sxs-lookup"><span data-stu-id="b5f60-136">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

