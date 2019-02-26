---
title: Office 365 위협 인텔리전스를 사용하여 Office 365 사용자를 안전하게 보호
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3387bfc3-028a-42f4-8133-4cbecfaab812
ms.collection:
- M365-security-compliance
description: Office 365 위협 인텔리전스를 통해 조직이 침입 및 위협을 검색 하는 데 도움을 주는 방법 및 위협 으로부터 신속 하 게 완화 및 복구할 수 있는 방법을 알아봅니다.
ms.openlocfilehash: 40b39cc7f388152bd95000e2653ef94b970a6fa3
ms.sourcegitcommit: 1c73c2f83703af0a30a5b0633db00d8e0e6b39b5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/25/2019
ms.locfileid: "30241960"
---
# <a name="keep-your-office-365-users-safe-with-office-365-threat-intelligence"></a><span data-ttu-id="ddd0a-103">Office 365 위협 인텔리전스를 사용하여 Office 365 사용자를 안전하게 보호</span><span class="sxs-lookup"><span data-stu-id="ddd0a-103">Keep your Office 365 users safe with Office 365 Threat Intelligence</span></span>

## <a name="overview"></a><span data-ttu-id="ddd0a-104">개요</span><span class="sxs-lookup"><span data-stu-id="ddd0a-104">Overview</span></span>

<span data-ttu-id="ddd0a-p101">어떤 Office 365 사용자가 공격을 받고 있는지, 더 이상 손상 되지 않습니까? 사용자를 대상으로 하는 공격 으로부터 완화 하 고 복구 하는 방법을 확인 하세요. Office 365에서 이미 제공 되는 보안 기능을 사용 하 여이 작업을 정확히 확인할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="ddd0a-p101">Do you know which of your Office 365 users are under attack, or worse - compromised? Do know how to mitigate and recover from attacks that are targeting your users? Did you know you can do exactly this with security capabilities that are already available to you in Office 365?</span></span> 
  
<span data-ttu-id="ddd0a-p102">[office 365 위협 인텔리전스](office-365-ti.md) 는 office 365 E5 구독에 포함 된 기능 모음입니다. Office 365 위협 인텔리전스를 통해 Microsoft IT는 사회 공학적 인시던트에 대 한 해결 방법을 80%로 줄이고, 월별 사례 처리량을 지난 2 분기에 비해 매달 37% 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ddd0a-p102">[Office 365 Threat Intelligence](office-365-ti.md) is a suite of capabilities included in your Office 365 E5 subscription. Office 365 Threat Intelligence has helped Microsoft IT reduce average time to resolution for social engineering incidents by 80%, and increased case throughput by 37% per month compared to the previous 2 quarters!</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="ddd0a-p103">2019 년 2 월에 시작 해 서 향후 몇 개월 동안 롤아웃 되는 office 365 위협 인텔리전스는 추가 위협 방지 기능을 사용 하 여 office 365 Advanced threat protection 계획 2가 됩니다. 자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ddd0a-p103">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
<span data-ttu-id="ddd0a-p104">최근에는 위협 으로부터 검색 및 복구 하는 방법을 개선 하는 데 도움이 되는 새로운 기능이 추가 되었습니다. 업데이트 된 위협 인텔리전스 서비스를 통해 보다 효율적으로 수행할 수 있는 방법에 대 한 간략 한 설명이 여기에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ddd0a-p104">We've recently added new capabilities to help improve how you can detect and recover from threats! Here's a quick walk through of how the updated Threat Intelligence service can make you even more efficient.</span></span>
  
## <a name="detect-intrusions-and-threats"></a><span data-ttu-id="ddd0a-114">침입 및 위협 감지</span><span class="sxs-lookup"><span data-stu-id="ddd0a-114">Detect intrusions and threats</span></span>

<span data-ttu-id="ddd0a-p105">[탐색기](use-explorer-in-security-and-compliance.md) (위협 탐색기 라고도 함) 보안 관리자 및 분석가가 가장 복잡 한 보안 설정을 안전한 것 처럼 겉보기에 걸어도 워크플로가 바이패스 수 있으므로 엔터프라이즈에서 활성 상태인 위협을 식별 하 고 이해 하는 데 도움이 됩니다. 보낸 사람 whitelists Explorer에서는 Office 365 글로벌 또는 보안 관리자가 사용자가 맬웨어 또는 피싱 같은 위협에 의해 손상 되었는지 여부를 빠르게 확인할 수 있도록 지원 합니다. 이를 통해 위협 및 필수 응답에 대 한 위험성이 가장 많은 사용자를 우선 순위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ddd0a-p105">[Explorer](use-explorer-in-security-and-compliance.md) (also referred to as Threat Explorer) helps security admins and analysts identify and understand threats that are active in your enterprise because even the most complex security settings can be circumvented by seemingly innocuous user configurations like safe sender whitelists. Explorer helps Office 365 global or security admins quickly determine whether users have been compromised by threats such as malware or phish. This helps prioritize which users are most at risk for a threat and the requisite response.</span></span> 
  
<span data-ttu-id="ddd0a-p106">또한 Explorer는 관리자가 사용자와 메일 간의 관계를 탐색 하도록 도와줍니다. 손상 된 특정 메일 확인 이를 검색 하 여 사용자가 메일을 받은 사람을 확인 한 다음 이벤트 시리즈를 따르고 해당 사용자가 수행 하는 작업을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddd0a-p106">Explorer also helps admins navigate the relationships between users and mail. Know of a particular mail that was bad? Search for it to see what users received the mail, then follow the series of events and see what those users in turn have done.</span></span>

<span data-ttu-id="ddd0a-p107">위협 인텔리전스가 아직 없는 경우 [지금 사용해 보세요](https://aka.ms/tryo365threatintel3)! 그리고 [Office 365 위협 인텔리전스에 대해 자세히 알아보세요](https://aka.ms/readmoreabouto365threatintel).</span><span class="sxs-lookup"><span data-stu-id="ddd0a-p107">If you don't already have Threat Intelligence, [try it now](https://aka.ms/tryo365threatintel3)! And [learn more about Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span></span>
  
![맬웨어 패밀리가 Office 365, 색으로 구분 된 위협 탐색기 스크린샷](media/591338dd-252a-437d-b5f2-87aa42e74b0c.png)
  
## <a name="quickly-mitigate-and-recover-from-threats"></a><span data-ttu-id="ddd0a-124">위협 으로부터 신속 하 게 완화 및 복구</span><span class="sxs-lookup"><span data-stu-id="ddd0a-124">Quickly mitigate and recover from threats</span></span>

<span data-ttu-id="ddd0a-p108">보안 관리자가 테 넌 트에서 의심 되거나 악의적인 상황을 확인 하면 **문제 프레임 워크**를 사용 하 여 해당 위협에 빠르게 포함 하 고 대응할 수 있습니다. 한 번 클릭으로 원치 않는 메시지를 그룹화 하 고 사용자 사서함에서 전자 메일 메시지를 빠르게 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddd0a-p108">Once security admins have identified something suspicious or malicious happening in their tenant, they can quickly contain and respond to that threat with the **Incident Framework**. Group unwanted messages with one-click and quickly remove the email messages from your user's mailboxes.</span></span> 
  
 <span data-ttu-id="ddd0a-p109">**업데이트:** 최근에 문제 프레임 워크에서 직접 전자 메일을 삭제 (소프트 또는 영구 삭제) 하는 기능이 추가 되었습니다. 이전 관리자는 메일을 사용자의 정크 폴더로만 이동할 수 있으며, 사용자는 해당 항목을 복구할 수 있습니다. 새로 릴리스된 삭제 기능을 사용 하 여 악성 메일 또는 원치 않는 메일이 영구적으로 제거 되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ddd0a-p109">**UPDATE:** We've recently added the ability to delete (soft or hard delete) emails directly from the Incident Framework. Previously administrators could only move mails to a user's junk folder, where users could recover the item. With the newly released Delete capabilities, you can now be sure that a malicious or unwanted mail is removed permanently.</span></span> 
  
<span data-ttu-id="ddd0a-p110">위협 인텔리전스가 아직 없는 경우 [지금 사용해 보세요](https://aka.ms/tryo365threatintel3)! 그리고 [Office 365 위협 인텔리전스에 대해 자세히 알아보세요](https://aka.ms/readmoreabouto365threatintel).</span><span class="sxs-lookup"><span data-stu-id="ddd0a-p110">If you don't already have Threat Intelligence, [try it now](https://aka.ms/tryo365threatintel3)! And [learn more about Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span></span>
  
![인시던트 업데이트 관리의 전자 메일 목록 스크린샷](media/9d8452d3-d8d2-4b26-81f9-76396e08dd17.png)
  
## <a name="leverage-the-threat-telemetry-of-microsoft"></a><span data-ttu-id="ddd0a-133">Microsoft의 위협 원격 분석 활용</span><span class="sxs-lookup"><span data-stu-id="ddd0a-133">Leverage the threat telemetry of Microsoft</span></span>

<span data-ttu-id="ddd0a-p111">Office 365 위협 인텔리전스는 Microsoft 지능형 보안 그래프의 데이터를 사용 하 여 제공 됩니다. 그래프는 Office 365에서 10억 Windows 장치, 4500억 월별 Azure 로그인 및 4000억 월별 전자 메일 메시지의 최신 위협 신호를 가져옵니다. 이 unrivaled 위협 신호는 관리자 및 보안 분석가가 조직에 영향을 주는 위협에 대 한 전체 정보를 확인 하는 데 중요 한 고객 테 넌 트에 대 한 광범위 한 가시성을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddd0a-p111">Office 365 Threat Intelligence is powered with data from the Microsoft Intelligent Security Graph. The graph acquires the latest threat signal from over 1 billion Windows devices, 450 billion monthly Azure logins, and 400 billion monthly email messages in Office 365. This unrivaled threat signal is what gives the broad visibility into a customer tenant that is crucial for admins and security analysts to have a complete view of the threats impacting their organization.</span></span> 
  
## <a name="more-to-come"></a><span data-ttu-id="ddd0a-137">제공 대상 추가</span><span class="sxs-lookup"><span data-stu-id="ddd0a-137">More to come</span></span>

<span data-ttu-id="ddd0a-p112">다음은 Office 365 위협 인텔리전스에서 엔터프라이즈 보안을 유지 하는 방법을 보여 주는 몇 가지 예입니다. 출시 예정에서는 다음을 포함 하 여 제품에 대 한 향상 된 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddd0a-p112">These are just some examples of how Office 365 Threat Intelligence helps you secure your enterprise! In the coming weeks we are adding significant enhancements to the product including:</span></span>
  
- <span data-ttu-id="ddd0a-140">Exchange online 전자 메일 및 SharePoint online 문서에 대해 수행 되는 잠재적 위험 작업에 대 한 통찰력 제공</span><span class="sxs-lookup"><span data-stu-id="ddd0a-140">Providing insight into potentially risky actions taken on Exchange Online email and SharePoint Online documents</span></span>
    
- <span data-ttu-id="ddd0a-141">weaponized 전에 사용자가 받아서 읽은 것을 비롯 하 여 사용자에 게 전송 된 악의적인 피싱 전자 메일 메시지에 대 한 통찰력 제공</span><span class="sxs-lookup"><span data-stu-id="ddd0a-141">Providing insight into malicious phishing email messages that have been sent to users, including some that have may have been received and read by users before they were weaponized</span></span>
    
- <span data-ttu-id="ddd0a-142">관리자가 인시던트에 대응 하기 위해 취할 수 있는 작업 집합 증가</span><span class="sxs-lookup"><span data-stu-id="ddd0a-142">Increasing the set of actions admins can take to respond to incidents</span></span>
    
## <a name="why-threat-intelligence"></a><span data-ttu-id="ddd0a-143">왜 위협 인텔리전스 인가요?</span><span class="sxs-lookup"><span data-stu-id="ddd0a-143">Why Threat Intelligence?</span></span>

<span data-ttu-id="ddd0a-p113">Gartner에서 $90b를 단독으로 cybersecurity에서 사용한 추정치입니다. Sid를 제거 하는 경우 Gartner의 주요 조사 분석가는 "업계의 교대조가 검색 및 응답으로 이동 하는 것을 말합니다. 검색 및 응답 기능에 연결 되어 있지 않으면 futile 방지 되는 일반 메시지를 보냅니다. " 위협 인텔리전스는 모든 엔터프라이즈의 서비스 포트폴리오에서 중요 한 부분으로, 독립 실행형 서비스로 사용 하거나 Office 365 E5의 일부로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ddd0a-p113">Gartner estimates that in 2017 alone over $90B was spent on cybersecurity. Sid Deshpande, principal research analyst at Gartner, is quoted as saying that "the industry's shift to detection and response … sends a clear message that prevention is futile unless it is tied into a detection and response capability." Threat Intelligence is a critical part of every enterprise's portfolio of services, and can be consumed as standalone service or as part of Office 365 E5.</span></span>
  
## <a name="whats-next"></a><span data-ttu-id="ddd0a-148">다음 작업</span><span class="sxs-lookup"><span data-stu-id="ddd0a-148">What's Next</span></span>

- <span data-ttu-id="ddd0a-149">이 기록 된 세션의 office 365 위협 인텔리전스에 대 한 자세한 내용은 [office 365 위협 인텔리전스를 사용 하 여 고 사이버 공격](https://myignite.microsoft.com/videos/53723) 를 계속 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="ddd0a-149">Learn more about Office 365 Threat Intelligence in this recorded session: [Stay Ahead of the Cyberattacks with Office 365 Threat Intelligence](https://myignite.microsoft.com/videos/53723)</span></span>
    
- <span data-ttu-id="ddd0a-150">[지금 office 365 위협 인텔리전스를 이용해](https://aka.ms/tryo365threatintel3) 보거나 office E5 평가판을 시작 해 보세요.</span><span class="sxs-lookup"><span data-stu-id="ddd0a-150">[Try out Office 365 Threat Intelligence now](https://aka.ms/tryo365threatintel3) or begin your Office E5 trial today!</span></span> 
    

