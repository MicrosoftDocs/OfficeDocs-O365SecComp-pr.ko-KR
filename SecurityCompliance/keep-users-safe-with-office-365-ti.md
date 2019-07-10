---
title: Office 365 사용자에 게 Office 365 위협 조사 및 응답 기능을 안전 하 게 유지
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 07/09/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3387bfc3-028a-42f4-8133-4cbecfaab812
ms.collection:
- M365-security-compliance
description: Office 365 위협 조사 및 응답 기능을 통해 조직이 침입 및 위협을 감지 하 고 위협 으로부터 신속 하 게 완화 및 복구할 수 있는 방법을 알아봅니다.
ms.openlocfilehash: 28fbf0a66370e2e1d407454017943e57f5f368b1
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598984"
---
# <a name="keep-your-office-365-users-safe-with-office-365-threat-investigation-and-response-capabilities"></a><span data-ttu-id="6cb5c-103">Office 365 사용자에 게 Office 365 위협 조사 및 응답 기능을 안전 하 게 유지</span><span class="sxs-lookup"><span data-stu-id="6cb5c-103">Keep your Office 365 users safe with Office 365 threat investigation and response capabilities</span></span>

## <a name="overview"></a><span data-ttu-id="6cb5c-104">개요</span><span class="sxs-lookup"><span data-stu-id="6cb5c-104">Overview</span></span>

<span data-ttu-id="6cb5c-105">어떤 Office 365 사용자가 공격을 받고 있는지, 더 이상 손상 되지 않습니까?</span><span class="sxs-lookup"><span data-stu-id="6cb5c-105">Do you know which of your Office 365 users are under attack, or worse - compromised?</span></span> <span data-ttu-id="6cb5c-106">사용자를 대상으로 하는 공격 으로부터 완화 하 고 복구 하는 방법을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-106">Do know how to mitigate and recover from attacks that are targeting your users?</span></span> <span data-ttu-id="6cb5c-107">Office 365에서 이미 제공 되는 보안 기능을 사용 하 여이 작업을 정확히 확인할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="6cb5c-107">Did you know you can do exactly this with security capabilities that are already available to you in Office 365?</span></span> 
  
<span data-ttu-id="6cb5c-108">Office [365 위협 조사 및 응답](office-365-ti.md) 기능은 Office 365 E5 구독 (Office 365 Advanced Threat Protection 계획 2의 일부로)에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-108">[Office 365 threat investigation and response](office-365-ti.md) capabilities are included in your Office 365 E5 subscription (as part of Office 365 Advanced Threat Protection Plan 2).</span></span> <span data-ttu-id="6cb5c-109">이러한 기능을 통해 Microsoft IT는 주민 등록 수를 확인 하 여 해결 하는 데 걸리는 평균 시간을 80%로 줄이고, 월별 대/소문자 처리량이 지난 2 분기에 비해 매달 37% 씩 증가 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-109">These capabilities have helped Microsoft IT reduce average time to resolution for social engineering incidents by 80%, and increased case throughput by 37% per month compared to the previous 2 quarters!</span></span> 

<span data-ttu-id="6cb5c-110">최근에는 위협 으로부터 검색 및 복구 하는 방법을 개선 하는 데 도움이 되는 새로운 기능이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-110">We've recently added new capabilities to help improve how you can detect and recover from threats!</span></span> <span data-ttu-id="6cb5c-111">다음은 업데이트 된 위협 조사 및 응답 기능을 통해 보다 효율적으로 수행할 수 있는 방법에 대 한 간략 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-111">Here's a quick walk through of how the updated Threat investigation and response capabilities can make you even more efficient.</span></span>
  
## <a name="detect-intrusions-and-threats"></a><span data-ttu-id="6cb5c-112">침입 및 위협 감지</span><span class="sxs-lookup"><span data-stu-id="6cb5c-112">Detect intrusions and threats</span></span>

<span data-ttu-id="6cb5c-113">[위협 탐색기 (또는 실시간 검색)](threat-explorer.md) (위협 탐색기 라고도 함) 보안 관리자 및 분석가가 가장 복잡 한 보안 설정을 안전한 것 처럼 겉보기에 걸어도 워크플로가 바이패스 수 있으므로 엔터프라이즈에서 활성 상태인 위협을 식별 하 고 이해 하는 데 도움이 됩니다. 보낸 사람 whitelists</span><span class="sxs-lookup"><span data-stu-id="6cb5c-113">[Threat Explorer (or real-time detections)](threat-explorer.md) (also referred to as Threat Explorer) helps security admins and analysts identify and understand threats that are active in your enterprise because even the most complex security settings can be circumvented by seemingly innocuous user configurations like safe sender whitelists.</span></span> <span data-ttu-id="6cb5c-114">Explorer에서는 Office 365 글로벌 또는 보안 관리자가 사용자가 맬웨어 또는 피싱 같은 위협에 의해 손상 되었는지 여부를 빠르게 확인할 수 있도록 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-114">Explorer helps Office 365 global or security admins quickly determine whether users have been compromised by threats such as malware or phish.</span></span> <span data-ttu-id="6cb5c-115">이를 통해 위협 및 필수 응답에 대 한 위험성이 가장 많은 사용자를 우선 순위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-115">This helps prioritize which users are most at risk for a threat and the requisite response.</span></span> 
  
<span data-ttu-id="6cb5c-116">또한 Explorer는 관리자가 사용자와 메일 간의 관계를 탐색 하도록 도와줍니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-116">Explorer also helps admins navigate the relationships between users and mail.</span></span> <span data-ttu-id="6cb5c-117">손상 된 특정 메일 확인</span><span class="sxs-lookup"><span data-stu-id="6cb5c-117">Know of a particular mail that was bad?</span></span> <span data-ttu-id="6cb5c-118">이를 검색 하 여 사용자가 메일을 받은 사람을 확인 한 다음 이벤트 시리즈를 따르고 해당 사용자가 수행 하는 작업을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-118">Search for it to see what users received the mail, then follow the series of events and see what those users in turn have done.</span></span>

<span data-ttu-id="6cb5c-119">이러한 기능이 아직 없으면 [지금 사용해 보세요](https://aka.ms/tryo365threatintel3)!</span><span class="sxs-lookup"><span data-stu-id="6cb5c-119">If you don't already have these capabilities, [try it now](https://aka.ms/tryo365threatintel3)!</span></span> <span data-ttu-id="6cb5c-120">그리고 [Office 365 위협 조사 및 응답에 대해 자세히 알아보세요](https://aka.ms/readmoreabouto365threatintel).</span><span class="sxs-lookup"><span data-stu-id="6cb5c-120">And [learn more about Office 365 threat investigation and response](https://aka.ms/readmoreabouto365threatintel).</span></span>
  
![맬웨어 패밀리가 Office 365, 색으로 구분 된 위협 탐색기 스크린샷](media/591338dd-252a-437d-b5f2-87aa42e74b0c.png)
  
## <a name="quickly-mitigate-and-recover-from-threats"></a><span data-ttu-id="6cb5c-122">위협 으로부터 신속 하 게 완화 및 복구</span><span class="sxs-lookup"><span data-stu-id="6cb5c-122">Quickly mitigate and recover from threats</span></span>

<span data-ttu-id="6cb5c-123">보안 관리자가 테 넌 트에서 의심 되거나 악의적인 상황을 확인 하면 **문제 프레임 워크**를 사용 하 여 해당 위협에 빠르게 포함 하 고 대응할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-123">Once security admins have identified something suspicious or malicious happening in their tenant, they can quickly contain and respond to that threat with the **Incident Framework**.</span></span> <span data-ttu-id="6cb5c-124">한 번 클릭으로 원치 않는 메시지를 그룹화 하 고 사용자 사서함에서 전자 메일 메시지를 빠르게 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-124">Group unwanted messages with one-click and quickly remove the email messages from your user's mailboxes.</span></span> 
  
 <span data-ttu-id="6cb5c-125">**업데이트:** 문제 프레임 워크에서 직접 전자 메일을 삭제 (소프트 또는 영구 삭제) 하는 기능이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-125">**UPDATE:** We've added the ability to delete (soft or hard delete) emails directly from the Incident Framework.</span></span> <span data-ttu-id="6cb5c-126">이전 관리자는 메일을 사용자의 정크 폴더로만 이동할 수 있으며, 사용자는 해당 항목을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-126">Previously administrators could only move mails to a user's junk folder, where users could recover the item.</span></span> <span data-ttu-id="6cb5c-127">새로 릴리스된 삭제 기능을 사용 하 여 악성 메일 또는 원치 않는 메일이 영구적으로 제거 되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-127">With the newly released Delete capabilities, you can now be sure that a malicious or unwanted mail is removed permanently.</span></span> 
  
<span data-ttu-id="6cb5c-128">이러한 기능이 아직 없으면 [지금 사용해 보세요](https://aka.ms/tryo365threatintel3)!</span><span class="sxs-lookup"><span data-stu-id="6cb5c-128">If you don't already have these capabilities, [try it now](https://aka.ms/tryo365threatintel3)!</span></span> <span data-ttu-id="6cb5c-129">그리고 [Office 365 위협 조사 및 응답에 대해 자세히 알아보세요](https://aka.ms/readmoreabouto365threatintel).</span><span class="sxs-lookup"><span data-stu-id="6cb5c-129">And [learn more about Office 365 threat investigation and response](https://aka.ms/readmoreabouto365threatintel).</span></span>
  
![인시던트 업데이트 관리의 전자 메일 목록 스크린샷](media/9d8452d3-d8d2-4b26-81f9-76396e08dd17.png)
  
## <a name="leverage-the-threat-telemetry-of-microsoft"></a><span data-ttu-id="6cb5c-131">Microsoft의 위협 원격 분석 활용</span><span class="sxs-lookup"><span data-stu-id="6cb5c-131">Leverage the threat telemetry of Microsoft</span></span>

<span data-ttu-id="6cb5c-132">Office 365 위협 조사 및 응답 기능은 Microsoft 지능형 보안 그래프의 데이터를 사용 하 여 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-132">Office 365 threat investigation and response capabilities are powered with data from the Microsoft Intelligent Security Graph.</span></span> <span data-ttu-id="6cb5c-133">그래프는 Office 365에서 10억 Windows 장치, 4500억 월별 Azure 로그인 및 4000억 월별 전자 메일 메시지의 최신 위협 신호를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-133">The graph acquires the latest threat signal from over 1 billion Windows devices, 450 billion monthly Azure logins, and 400 billion monthly email messages in Office 365.</span></span> <span data-ttu-id="6cb5c-134">이 unrivaled 위협 신호는 관리자 및 보안 분석가가 조직에 영향을 주는 위협에 대 한 전체 정보를 확인 하는 데 중요 한 고객 테 넌 트에 대 한 광범위 한 가시성을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-134">This unrivaled threat signal is what gives the broad visibility into a customer tenant that is crucial for admins and security analysts to have a complete view of the threats impacting their organization.</span></span> 
  
   
## <a name="why-use-office-365-threat-investigation-and-response-capabilities"></a><span data-ttu-id="6cb5c-135">Office 365 위협 조사 및 응답 기능을 사용 하는 이유</span><span class="sxs-lookup"><span data-stu-id="6cb5c-135">Why use Office 365 threat investigation and response capabilities?</span></span>

<span data-ttu-id="6cb5c-136">Gartner에서 $90B를 단독 2017으로 cybersecurity에서 사용한 추정치입니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-136">Gartner estimates that in 2017 alone over $90B was spent on cybersecurity.</span></span> <span data-ttu-id="6cb5c-137">Sid를 제거 하는 경우 Gartner의 주요 조사 분석가는 "업계의 교대조가 검색 및 응답으로 이동 하는 것을 말합니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-137">Sid Deshpande, principal research analyst at Gartner, is quoted as saying that "the industry's shift to detection and response …</span></span> <span data-ttu-id="6cb5c-138">검색 및 응답 기능에 연결 되어 있지 않으면 futile 방지 되는 일반 메시지를 보냅니다. "</span><span class="sxs-lookup"><span data-stu-id="6cb5c-138">sends a clear message that prevention is futile unless it is tied into a detection and response capability."</span></span> <span data-ttu-id="6cb5c-139">위협 조사 및 응답은 모든 기업의 서비스 포트폴리오에서 중요 한 부분으로, 독립 실행형 서비스로 사용 하거나 Office 365 E5의 일부로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-139">Threat investigation and response is a critical part of every enterprise's portfolio of services, and can be consumed as standalone service or as part of Office 365 E5.</span></span>
  
## <a name="whats-next"></a><span data-ttu-id="6cb5c-140">다음 작업</span><span class="sxs-lookup"><span data-stu-id="6cb5c-140">What's Next</span></span>

- <span data-ttu-id="6cb5c-141">이 기록 된 세션의 Office 365 위협 조사 및 응답 기능에 대 한 자세한 내용은 [office 365을 사용 하 여 고 사이버 공격](https://myignite.microsoft.com/videos/53723) 를 계속 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-141">Learn more about Office 365 threat investigation and response capabilities  in this recorded session: [Stay Ahead of the Cyberattacks with Office 365](https://myignite.microsoft.com/videos/53723)</span></span>
    
- <span data-ttu-id="6cb5c-142">[지금 office 365 위협 조사 및 응답 기능을 사용해](https://aka.ms/tryo365threatintel3) 보거나 office E5 평가판을 시작 해 보세요.</span><span class="sxs-lookup"><span data-stu-id="6cb5c-142">[Try out Office 365 threat investigation and response capabilities now](https://aka.ms/tryo365threatintel3) or begin your Office E5 trial today!</span></span> 
    

