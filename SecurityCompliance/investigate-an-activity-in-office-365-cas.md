---
title: Office 365 Cloud App Security에서 활동 조사
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 15fa4545-28b4-4dd4-bf85-88e0926bd5fc
description: 'Office 365 클라우드 응용 프로그램 보안을을 찾고 조사 하는 데 활동 및 계정 하 여 Office 365 환경에서 소식을 볼 수 있습니다. '
ms.openlocfilehash: e463323cf28738e1d54fcdb65ed0d15290c79994
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603659"
---
# <a name="investigate-an-activity-in-office-365-cloud-app-security"></a><span data-ttu-id="4408d-103">Office 365 Cloud App Security에서 활동 조사</span><span class="sxs-lookup"><span data-stu-id="4408d-103">Investigate an activity in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="4408d-104">평가 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="4408d-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="4408d-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="4408d-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="4408d-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="4408d-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="4408d-107">사용률 \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4408d-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="4408d-108">평가 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4408d-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="4408d-109">계획을 시작합니다</span><span class="sxs-lookup"><span data-stu-id="4408d-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="4408d-110">배포를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4408d-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="4408d-111">여기는!</span><span class="sxs-lookup"><span data-stu-id="4408d-111">You are here!</span></span>  <br/> [<span data-ttu-id="4408d-112">다음 단계</span><span class="sxs-lookup"><span data-stu-id="4408d-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="4408d-p101">Office 365 클라우드 앱 보안 [감사 로그를 Office 365](detailed-properties-in-the-office-365-audit-log.md)작동합니다. Office 365 클라우드 응용 프로그램 보안 전역 관리자 또는 보안 관리자 작업 로그 페이지를 조직의 Office 365 사용 하는 방법에 대 한 잠재적 문제를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4408d-p101">Office 365 Cloud App Security works with your [Office 365 audit log](detailed-properties-in-the-office-365-audit-log.md). With Office 365 Cloud App Security, as a global administrator or security administrator, you can use the Activity log page to see potential issues in how your organization is using Office 365.</span></span>
  
## <a name="how-to-get-to-the-activity-log-page"></a><span data-ttu-id="4408d-115">활동 로그 페이지로 이동 하는 방법</span><span class="sxs-lookup"><span data-stu-id="4408d-115">How to get to the Activity log page</span></span>

1. <span data-ttu-id="4408d-116">클라우드 응용 프로그램 보안 포털에 이동 ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))에 로그인 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4408d-116">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="4408d-117">화면 위쪽 탐색 모음에서 **조사** 선택 \> **활동 로그**합니다.</span><span class="sxs-lookup"><span data-stu-id="4408d-117">In the navigation bar across the top of the screen, choose **Investigate** \> **Activity log**.</span></span><br/><span data-ttu-id="4408d-118">![O365 CAS 포털에서 조사를 선택 합니다.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span><span class="sxs-lookup"><span data-stu-id="4408d-118">![In the O365 CAS portal, choose Investigate.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span></span>
  
## <a name="review-and-investigate-activities"></a><span data-ttu-id="4408d-119">검토 하 고 활동 조사</span><span class="sxs-lookup"><span data-stu-id="4408d-119">Review and investigate activities</span></span>

<span data-ttu-id="4408d-p102">활동 로그 페이지에서 Office 365를 사용 하 여 조직 내에서 수행 되는 다양 한 작업 목록을 볼 수 있습니다. 특정 유형의 활동 또는 특정 사용자에 초점을 화면의 위쪽에서 필터를 사용할 수 있습니다. 예는 다음 이미지 조직의 Office 365 관리자 계정의 암호를 변경 하는 방법에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4408d-p102">On the Activity log page, you can see a list of various activities that are taking place within your organization using Office 365. You can use filters across the top of the screen to focus on a specific type of activity or a specific user. For example, the following image shows information about an organization's Office 365 admin account's password change:</span></span>
  
![Office 365 클라우드 응용 프로그램 보안에서 조사 선택 \> 활동 로그 합니다.](media/5d54600c-59cd-4f33-b4f0-29b75c37baae.png)
  
<span data-ttu-id="4408d-p103">활동 로그의 각 항목을 보면 처럼 다른 관련된 활동을 찾으려면 줄임표를 클릭 수 있습니다. 예, 동일한 유형의 동일한 IP 주소 또는 동일한 국가/지역에서 다른 활동을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4408d-p103">As you look at each item in the Activity log, you can click the ellipses to find other related activities. For example, you can view other activities of the same type, from the same IP address, or from the same country/region.</span></span>
  
<span data-ttu-id="4408d-p104">너무 다양 한 유형의 활동을 하는 방법에 대 한 정보를 볼 수 있습니다. 예, 사항은 활동 로그에서 볼 수 있는 작업의 일부 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4408d-p104">You can view information about many other kinds of activities, too. For example, here are some of the activities you can view in the Activity log:</span></span>
  
- <span data-ttu-id="4408d-128">구성원을 추가 하거나 그룹에서 제거</span><span class="sxs-lookup"><span data-stu-id="4408d-128">Members added to or removed from groups</span></span>
    
- <span data-ttu-id="4408d-129">사용자 라이선스의 변경 사항</span><span class="sxs-lookup"><span data-stu-id="4408d-129">Changes in user licenses</span></span>
    
- <span data-ttu-id="4408d-130">파일 또는 내부 또는 외부적으로 공유 되는 폴더</span><span class="sxs-lookup"><span data-stu-id="4408d-130">Files or folders shared internally or externally</span></span>
    
- <span data-ttu-id="4408d-131">만든 또는 삭제 된 사이트 또는 사이트 모음</span><span class="sxs-lookup"><span data-stu-id="4408d-131">Created or deleted sites or site collections</span></span>
    
- <span data-ttu-id="4408d-132">착신 전환 규칙 전자 메일</span><span class="sxs-lookup"><span data-stu-id="4408d-132">Email forwarding rules</span></span>
    
<span data-ttu-id="4408d-133">이러한 문제를 Office 365 및 사용자 조직에서 사용 하는 방법을 만들어보겠습니다 활동 로그 페이지는 방식에 따라 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4408d-133">Use the Activity log page to get acquainted with how people in your organization are using Office 365 and what issues they might be having along the way.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="4408d-134">다음 단계</span><span class="sxs-lookup"><span data-stu-id="4408d-134">Next steps</span></span>

- [<span data-ttu-id="4408d-135">검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행</span><span class="sxs-lookup"><span data-stu-id="4408d-135">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="4408d-136">[Office 365 클라우드 응용 프로그램 보안에 대 한 사용률 활동](utilization-activities-for-ocas.md) 을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="4408d-136">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

