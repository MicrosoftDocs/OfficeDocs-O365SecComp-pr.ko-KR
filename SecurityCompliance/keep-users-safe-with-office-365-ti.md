---
title: Office 365 위협 인텔리전스를 사용하여 Office 365 사용자를 안전하게 보호
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3387bfc3-028a-42f4-8133-4cbecfaab812
ms.collection: M365-security-compliance
description: Office 365 위협 인텔리전스 조직 침입 및 위협 요소를 검색 하 고 신속 하 게 완화 및 위협 으로부터 복구를 통해 하는 방법을 설명 합니다.
ms.openlocfilehash: c049e6f811eec8a30eb2b94361f8cdcbdaa8ac49
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995369"
---
# <a name="keep-your-office-365-users-safe-with-office-365-threat-intelligence"></a><span data-ttu-id="1b97d-103">Office 365 위협 인텔리전스를 사용하여 Office 365 사용자를 안전하게 보호</span><span class="sxs-lookup"><span data-stu-id="1b97d-103">Keep your Office 365 users safe with Office 365 Threat Intelligence</span></span>

## <a name="overview"></a><span data-ttu-id="1b97d-104">개요</span><span class="sxs-lookup"><span data-stu-id="1b97d-104">Overview</span></span>

<span data-ttu-id="1b97d-p101">Office 365 사용자 중 어떤 공격을 받고 중이거나 심각한 문제-손상 된 알고 있습니까? 완화 하 고 사용자를 대상으로 하는 공격에서 복구 하는 방법을 알고 있습니까? 알고 이미 지정 된 Office 365에서 사용할 수 있는 보안 기능을 갖춘이 정확 하 게 수행할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="1b97d-p101">Do you know which of your Office 365 users are under attack, or worse - compromised? Do know how to mitigate and recover from attacks that are targeting your users? Did you know you can do exactly this with security capabilities that are already available to you in Office 365?</span></span> 
  
<span data-ttu-id="1b97d-p102">[Office 365 위협 인텔리전스](office-365-ti.md) 는 제품군 Office 365 E5 구독에 포함 된 기능을 합니다. Office 365 위협 인텔리전스 도움을 주었습니다 되는 평균 시간 사회 공학 사고에 대 한 해상도 80% 및 사례 처리량 증가 하 여 37% 감소 이전 2 분기에 비해 매월 Microsoft IT!</span><span class="sxs-lookup"><span data-stu-id="1b97d-p102">[Office 365 Threat Intelligence](office-365-ti.md) is a suite of capabilities included in your Office 365 E5 subscription. Office 365 Threat Intelligence has helped Microsoft IT reduce average time to resolution for social engineering incidents by 80%, and increased case throughput by 37% per month compared to the previous 2 quarters!</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="1b97d-p103">2019 년 2 월에에서 시작 하 고 향후 몇 개월 동안 롤아웃, Office 365 위협 인텔리전스는 되 고 Office 365 고급 위협 보호 계획 2, 추가 위협 보호 기능을 사용 합니다. 자세한 내용은 [Office 365 고급 위협 보호 계획 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [Office 365 고급 위협 Protection 서비스 설명](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1b97d-p103">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
<span data-ttu-id="1b97d-p104">최근에 검색 하 고 위협 으로부터 복구할 수 있는 방법을 개선 하는 새로운 기능 추가 했습니다! 어떻게 업데이트 된 위협 인텔리전스 서비스 가능 하면 훨씬 더 효율적으로의 통해 빠른 워크는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1b97d-p104">We've recently added new capabilities to help improve how you can detect and recover from threats! Here's a quick walk through of how the updated Threat Intelligence service can make you even more efficient.</span></span>
  
## <a name="detect-intrusions-and-threats"></a><span data-ttu-id="1b97d-114">침입 및 위협 요소를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b97d-114">Detect intrusions and threats</span></span>

<span data-ttu-id="1b97d-p105">[탐색기](use-explorer-in-security-and-compliance.md) (위협 탐색기 라고도 함) 보안 관리자와 분석가 식별 하 고 가장 복잡 한 보안 설정도 안전 하 게 보호와 같은 문제가 없는 것 처럼 보이는 사용자 구성을 통해 피할 수 있으므로 기업에서 활성화 된 위협 요소를 이해 하는데 도움이 됩니다 보낸 사람이 whitelists 합니다. 탐색기 도움이 되는 Office 365 전역 또는 보안 관리자는 맬웨어 또는 phish 같은 위협 하 여 사용자가 손상 되었거나 신속 하 게 결정 합니다. 이렇게 하면 우선순위를 지정 하는 사용자에 대 한 위협 요소 및 구성 요소에 대 한 응답에 대 한 위험 가장가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b97d-p105">[Explorer](use-explorer-in-security-and-compliance.md) (also referred to as Threat Explorer) helps security admins and analysts identify and understand threats that are active in your enterprise because even the most complex security settings can be circumvented by seemingly innocuous user configurations like safe sender whitelists. Explorer helps Office 365 global or security admins quickly determine whether users have been compromised by threats such as malware or phish. This helps prioritize which users are most at risk for a threat and the requisite response.</span></span> 
  
<span data-ttu-id="1b97d-p106">탐색기에는 사용자 및 메일 간의 관계를 탐색 하는 관리자가 도움이 됩니다. 잘못 된 했던 특정 메일의 알고 있습니까? 열어 사용자에 게 받은 메일에 대 한 검색, 다음 일련의 이벤트를 수행 하 고 기능 해당 사용자를 차례로 수행을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b97d-p106">Explorer also helps admins navigate the relationships between users and mail. Know of a particular mail that was bad? Search for it to see what users received the mail, then follow the series of events and see what those users in turn have done.</span></span>

<span data-ttu-id="1b97d-p107">위협 인텔리전스, [평가판 다운로드 지금](https://aka.ms/tryo365threatintel3)이 아직 없는 경우! 및 [Office 365 위협 인텔리전스에 대 한 자세한 설명](https://aka.ms/readmoreabouto365threatintel)입니다.</span><span class="sxs-lookup"><span data-stu-id="1b97d-p107">If you don't already have Threat Intelligence, [try it now](https://aka.ms/tryo365threatintel3)! And [learn more about Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span></span>
  
![맬웨어 제품군으로 컬러 코딩 하는 Office 365의 위협 탐색기의 스크린샷](media/591338dd-252a-437d-b5f2-87aa42e74b0c.png)
  
## <a name="quickly-mitigate-and-recover-from-threats"></a><span data-ttu-id="1b97d-124">신속 하 게 완화 하 고 위협 으로부터 복구</span><span class="sxs-lookup"><span data-stu-id="1b97d-124">Quickly mitigate and recover from threats</span></span>

<span data-ttu-id="1b97d-p108">보안 관리자가 의심 스러운 또는 자신의 테 넌 트에 지내세요 악의적인 것을 식별 한 후 신속 하 게 포함 및 **사고 프레임 워크**와 해당 위협에 응답할 수 있습니다. 한번 클릭 하 여 원치 않는 메시지를 그룹화 하 고 신속 하 게 사용자의 사서함에서 전자 메일 메시지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b97d-p108">Once security admins have identified something suspicious or malicious happening in their tenant, they can quickly contain and respond to that threat with the **Incident Framework**. Group unwanted messages with one-click and quickly remove the email messages from your user's mailboxes.</span></span> 
  
 <span data-ttu-id="1b97d-p109">**업데이트:** 인시던트 프레임 워크에서 직접 (소프트 또는 하드 삭제) 전자 메일을 삭제 하는 기능 최근에 추가 했습니다. 이전에 관리자는 사용자는 항목을 복구할 수 있는 사용자의 정크 메일 폴더에 메일 이동할만 수 있습니다. 새로 출시 된 삭제 기능을 함께 이제 확인할 수 있습니다 악의적인 또는 원치 않는 메일 영구적으로 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b97d-p109">**UPDATE:** We've recently added the ability to delete (soft or hard delete) emails directly from the Incident Framework. Previously administrators could only move mails to a user's junk folder, where users could recover the item. With the newly released Delete capabilities, you can now be sure that a malicious or unwanted mail is removed permanently.</span></span> 
  
<span data-ttu-id="1b97d-p110">위협 인텔리전스, [평가판 다운로드 지금](https://aka.ms/tryo365threatintel3)이 아직 없는 경우! 및 [Office 365 위협 인텔리전스에 대 한 자세한 설명](https://aka.ms/readmoreabouto365threatintel)입니다.</span><span class="sxs-lookup"><span data-stu-id="1b97d-p110">If you don't already have Threat Intelligence, [try it now](https://aka.ms/tryo365threatintel3)! And [learn more about Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span></span>
  
![문제 수정 목록이 전자 메일의 스크린샷](media/9d8452d3-d8d2-4b26-81f9-76396e08dd17.png)
  
## <a name="leverage-the-threat-telemetry-of-microsoft"></a><span data-ttu-id="1b97d-133">Microsoft의 위협 원격 분석 활용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1b97d-133">Leverage the threat telemetry of Microsoft</span></span>

<span data-ttu-id="1b97d-p111">Office 365 위협 인텔리전스 지능형 보안은 Microsoft Graph에서 데이터로 전원을 합니다. 그래프의 최신 위협 신호를 개 1 십억 Windows 장치, 450 십억 월별 Azure 로그인 및 Office 365에서 400 십억 월별 전자 메일 메시지를 가져옵니다. 이 남다른된 위협 신호가 조직에 영향을 주지는 위협의 전체 보기를 관리자와 보안 분석가 대 한 중요 한 고객 테 넌 트에 대 한 광범위 한 가시성을 제공 하는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="1b97d-p111">Office 365 Threat Intelligence is powered with data from the Microsoft Intelligent Security Graph. The graph acquires the latest threat signal from over 1 billion Windows devices, 450 billion monthly Azure logins, and 400 billion monthly email messages in Office 365. This unrivaled threat signal is what gives the broad visibility into a customer tenant that is crucial for admins and security analysts to have a complete view of the threats impacting their organization.</span></span> 
  
## <a name="more-to-come"></a><span data-ttu-id="1b97d-137">향후 전망</span><span class="sxs-lookup"><span data-stu-id="1b97d-137">More to come</span></span>

<span data-ttu-id="1b97d-p112">Office 365 위협 인텔리전스 회사의 보안을 강화을 통해 방법에 대 한 예가 방금는! 앞으로 수 주에 포함 하 여 제품을 크게 향상 된 기능 추가 하는 것:</span><span class="sxs-lookup"><span data-stu-id="1b97d-p112">These are just some examples of how Office 365 Threat Intelligence helps you secure your enterprise! In the coming weeks we are adding significant enhancements to the product including:</span></span>
  
- <span data-ttu-id="1b97d-140">Exchange Online 전자 메일 및 SharePoint Online 문서에서 수행 하는 위험할 수 있는 작업에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b97d-140">Providing insight into potentially risky actions taken on Exchange Online email and SharePoint Online documents</span></span>
    
- <span data-ttu-id="1b97d-141">사용자에 게 전송 된 전자 메일 메시지 악의적인 피싱에 대 한 정보를 제공 하가 일부를 포함 하 여 수 수신 및 된 weaponized 된 대로 전에 사용자가 읽기</span><span class="sxs-lookup"><span data-stu-id="1b97d-141">Providing insight into malicious phishing email messages that have been sent to users, including some that have may have been received and read by users before they were weaponized</span></span>
    
- <span data-ttu-id="1b97d-142">보안 문제에 대응 위해 취할 수 있는 작업 admins 그룹의 집합을 늘리면</span><span class="sxs-lookup"><span data-stu-id="1b97d-142">Increasing the set of actions admins can take to respond to incidents</span></span>
    
## <a name="why-threat-intelligence"></a><span data-ttu-id="1b97d-143">인텔리전스 위협 이유?</span><span class="sxs-lookup"><span data-stu-id="1b97d-143">Why Threat Intelligence?</span></span>

<span data-ttu-id="1b97d-p113">Gartner는 $90B을 통해 만으로는 2017에 소요 된 cybersecurity에서 추정 합니다. Sid Deshpande, Gartner에서 보안 주체 연구 분석가 "검색과... 응답 하는 업계 shift 메시지를 보냅니다 분명 방지는 불필요 한 작업 검색 및 응답 기능에 연결 된 경우가 아니면." 고 말하는 인용은 위협 인텔리전스 서비스의 모든 기업의 포트폴리오의 중요 한 부분 이며 독립 실행형 서비스로 또는 Office 365 e 5의 일부로 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b97d-p113">Gartner estimates that in 2017 alone over $90B was spent on cybersecurity. Sid Deshpande, principal research analyst at Gartner, is quoted as saying that "the industry's shift to detection and response … sends a clear message that prevention is futile unless it is tied into a detection and response capability." Threat Intelligence is a critical part of every enterprise's portfolio of services, and can be consumed as standalone service or as part of Office 365 E5.</span></span>
  
## <a name="whats-next"></a><span data-ttu-id="1b97d-148">다음</span><span class="sxs-lookup"><span data-stu-id="1b97d-148">What's Next</span></span>

- <span data-ttu-id="1b97d-149">이 기록 된 세션에서 Office 365 위협 인텔리전스에 대 한 자세한 내용은: [Office 365 위협 정보를 바탕으로 Cyberattacks의 진행 상태를 유지](https://myignite.microsoft.com/videos/53723)</span><span class="sxs-lookup"><span data-stu-id="1b97d-149">Learn more about Office 365 Threat Intelligence in this recorded session: [Stay Ahead of the Cyberattacks with Office 365 Threat Intelligence](https://myignite.microsoft.com/videos/53723)</span></span>
    
- <span data-ttu-id="1b97d-150">[Office 365 위협 인텔리전스 지금 사용해 보기](https://aka.ms/tryo365threatintel3) 또는 Office E5 평가판 오늘 시작!</span><span class="sxs-lookup"><span data-stu-id="1b97d-150">[Try out Office 365 Threat Intelligence now](https://aka.ms/tryo365threatintel3) or begin your Office E5 trial today!</span></span> 
    

