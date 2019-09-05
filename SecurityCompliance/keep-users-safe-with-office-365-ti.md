---
title: Office 365 위협 조사 및 응답 기능을 사용 하 여 조직을 안전 하 게 유지
ms.author: deniseb
author: denisebmsft
manager: dansimp
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
ms.openlocfilehash: 217203c0bfa29352bc7e1b2b3976f11966034fb0
ms.sourcegitcommit: 4a2bde56178609e75c1ad7ecad2db5e049fc0c45
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2019
ms.locfileid: "36761694"
---
# <a name="keep-your-organization-safe-with-office-365-threat-investigation-and-response-capabilities"></a><span data-ttu-id="8df27-103">Office 365 위협 조사 및 응답 기능을 사용 하 여 조직을 안전 하 게 유지</span><span class="sxs-lookup"><span data-stu-id="8df27-103">Keep your organization safe with Office 365 threat investigation and response capabilities</span></span>

<span data-ttu-id="8df27-104">어떤 Office 365 사용자가 공격을 받고 있는지, 더 이상 손상 되지 않습니까?</span><span class="sxs-lookup"><span data-stu-id="8df27-104">Do you know which of your Office 365 users are under attack, or worse - compromised?</span></span> <span data-ttu-id="8df27-105">사용자를 대상으로 하는 공격 으로부터 완화 하 고 복구 하는 방법을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="8df27-105">Do know how to mitigate and recover from attacks that are targeting your users?</span></span> <span data-ttu-id="8df27-106">Office 365 E5에서 이미 제공 되는 보안 기능을 사용 하 여이 작업을 정확히 확인할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="8df27-106">Did you know you can do exactly this with security capabilities that are already available to you in Office 365 E5?</span></span> 
  
<span data-ttu-id="8df27-107">Office [365 위협 조사 및 응답](office-365-ti.md) 기능은 Office 365 E5 구독 ( [Office 365 Advanced threat Protection](office-365-atp.md) 계획 2의 일부로)에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-107">[Office 365 threat investigation and response](office-365-ti.md) capabilities are included in your Office 365 E5 subscription (as part of [Office 365 Advanced Threat Protection](office-365-atp.md) Plan 2).</span></span> <span data-ttu-id="8df27-108">이러한 기능을 통해 Microsoft IT는 사회 공학적 인시던트에 대 한 해결 방법을 80%로 줄이고 사례 처리량을 대폭 높여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-108">These capabilities have helped Microsoft IT reduce average time to resolution for social engineering incidents by 80%, and increased case throughput dramatically.</span></span> <span data-ttu-id="8df27-109">최근에는 위협 으로부터 검색 및 복구할 수 있는 방법을 개선 하기 위해 새로운 기능이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-109">Recently, new capabilities were added to help improve how you can detect and recover from threats.</span></span> <span data-ttu-id="8df27-110">이 문서를 읽으면 위협 조사 및 응답 기능이 보안 운영 팀을 보다 효율적이 고 효율적으로 활용 하는 방법을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-110">Read this article to see how threat investigation and response capabilities can help your security operations team be more effective and efficient.</span></span>
  
## <a name="detect-intrusions-and-threats"></a><span data-ttu-id="8df27-111">침입 및 위협 감지</span><span class="sxs-lookup"><span data-stu-id="8df27-111">Detect intrusions and threats</span></span>

<span data-ttu-id="8df27-112">[위협 탐색기](threat-explorer.md) (탐색기 라고도 함)은 보안 관리자 및 분석가가 조직에서 활성 상태인 위협을 식별 하 고 이해 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-112">[Threat Explorer](threat-explorer.md) (also referred to as Explorer) helps security administrators and analysts identify and understand threats that are active in your organization.</span></span> <span data-ttu-id="8df27-113">가장 복잡 한 보안 설정은 안전한 보낸 사람 목록과 같은 무해 한 사용자 구성을 사용 하 여 걸어도 워크플로가 바이패스 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-113">Even the most complex security settings can be circumvented by seemingly innocuous user configurations like safe-sender allow lists.</span></span> <span data-ttu-id="8df27-114">Explorer를 통해 Office 365 글로벌 또는 보안 관리자가 사용자가 악성 프로그램 또는 피싱 같은 위협에 의해 손상 되었는지 여부를 빠르게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-114">Explorer helps Office 365 global or security administrators quickly determine whether users have been compromised by threats, such as malware or phish.</span></span> <span data-ttu-id="8df27-115">이를 통해 위협과 필수 응답에 대 한 위험성이 가장 높은 사용자 계정에 대 한 우선 순위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-115">This helps prioritize which user accounts are most at risk for a threat and the requisite response.</span></span> 
  
<span data-ttu-id="8df27-116">또한 Explorer는 관리자가 사용자와 메일 간의 관계를 탐색 하도록 도와줍니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-116">Explorer also helps administrators navigate the relationships between users and mail.</span></span> <span data-ttu-id="8df27-117">손상 된 특정 메일 확인</span><span class="sxs-lookup"><span data-stu-id="8df27-117">Know of a particular mail that was bad?</span></span> <span data-ttu-id="8df27-118">이를 검색 하 여 사용자가 메일을 받은 사람을 확인 한 다음 이벤트 시리즈를 따르고 해당 사용자가 수행 하는 작업을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-118">Search for it to see what users received the mail, then follow the series of events and see what those users in turn have done.</span></span>

![맬웨어 패밀리가 Office 365, 색으로 구분 된 위협 탐색기 스크린샷](media/591338dd-252a-437d-b5f2-87aa42e74b0c.png)
  
## <a name="quickly-mitigate-and-recover-from-threats"></a><span data-ttu-id="8df27-120">위협 으로부터 신속 하 게 완화 및 복구</span><span class="sxs-lookup"><span data-stu-id="8df27-120">Quickly mitigate and recover from threats</span></span>

<span data-ttu-id="8df27-121">일단 보안 관리자가 테 넌 트에서 의심 되거나 악의적인 상황을 확인 하면 **문제 프레임 워크**를 사용 하 여 해당 위협에 빠르게 포함 하 고 대응할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-121">Once security administrators have identified something suspicious or malicious happening in their tenant, they can quickly contain and respond to that threat with the **Incident Framework**.</span></span> <span data-ttu-id="8df27-122">한 번 클릭으로 원치 않는 메시지를 그룹화 하 고 사용자 사서함에서 전자 메일 메시지를 빠르게 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-122">Group unwanted messages with one-click and quickly remove the email messages from your user's mailboxes.</span></span> 
  
 <span data-ttu-id="8df27-123">**업데이트:** 인시던트 프레임 워크에서 직접 전자 메일 메시지를 삭제 (소프트 또는 영구 삭제) 하는 기능이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-123">**UPDATE:** The ability to delete (soft or hard delete) email messages directly from the Incident framework has been added.</span></span> <span data-ttu-id="8df27-124">이전 관리자는 메일을 사용자의 정크 폴더로만 이동할 수 있으며, 사용자는 해당 항목을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-124">Previously administrators could only move mails to a user's junk folder, where users could recover the item.</span></span> <span data-ttu-id="8df27-125">새로 릴리스된 삭제 기능을 사용 하 여 악성 메일 또는 원치 않는 메일이 영구적으로 제거 되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-125">With the newly released Delete capabilities, you can now be sure that a malicious or unwanted mail is removed permanently.</span></span> 
    
![인시던트 업데이트 관리의 전자 메일 목록 스크린샷](media/9d8452d3-d8d2-4b26-81f9-76396e08dd17.png)
  
## <a name="leverage-the-threat-telemetry-of-microsoft"></a><span data-ttu-id="8df27-127">Microsoft의 위협 원격 분석 활용</span><span class="sxs-lookup"><span data-stu-id="8df27-127">Leverage the threat telemetry of Microsoft</span></span>

<span data-ttu-id="8df27-128">Office 365 위협 조사 및 응답 기능은 [Microsoft 지능형 보안 그래프](https://go.microsoft.com/fwlink/?linkid=2036223)의 데이터를 사용 하 여 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-128">Office 365 threat investigation and response capabilities are powered with data from the [Microsoft Intelligent Security Graph](https://go.microsoft.com/fwlink/?linkid=2036223).</span></span> <span data-ttu-id="8df27-129">그래프는 Office 365에서 10억 Windows 장치, 4500억 월별 Azure 로그인 및 4000억 월별 전자 메일 메시지의 최신 위협 신호를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-129">The graph acquires the latest threat signal from over 1 billion Windows devices, 450 billion monthly Azure logins, and 400 billion monthly email messages in Office 365.</span></span> <span data-ttu-id="8df27-130">이 unrivaled threat signal은 보안 운영 팀이 조직에 영향을 주는 위협에 대 한 보다 자세한 정보를 확인할 수 있도록 하는 다양 한 가시성을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-130">This unrivaled threat signal is what gives the broad visibility your security operations team have for a more complete view of the threats impacting your organization.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="8df27-131">다음 단계</span><span class="sxs-lookup"><span data-stu-id="8df27-131">Next steps</span></span>

- <span data-ttu-id="8df27-132">자세한 내용은 [Office 365 Advanced Threat Protection](office-365-atp.md)를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="8df27-132">Learn more about [Office 365 Advanced Threat Protection](office-365-atp.md).</span></span>

- <span data-ttu-id="8df27-133">이 기록 된 세션의 Office 365 위협 조사 및 응답 기능에 대 한 자세한 내용은 [office 365을 사용 하 여 고 사이버 공격](https://myignite.microsoft.com/videos/53723)를 계속 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="8df27-133">Learn more about Office 365 threat investigation and response capabilities in this recorded session: [Stay Ahead of the Cyberattacks with Office 365](https://myignite.microsoft.com/videos/53723).</span></span>

- <span data-ttu-id="8df27-134">아직 Office 365 Advanced Threat Protection 계획 2가 없는 경우 지금 구입 하거나 구매 하세요.</span><span class="sxs-lookup"><span data-stu-id="8df27-134">If you don't already have Office 365 Advanced Threat Protection Plan 2, try or buy it now.</span></span> <span data-ttu-id="8df27-135">[Office 365 Advanced Threat Protection: 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection#pmg-allup-content)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8df27-135">See [Office 365 Advanced Threat Protection: Plans and pricing](https://products.office.com/exchange/advance-threat-protection#pmg-allup-content).</span></span>
    
- <span data-ttu-id="8df27-136">[Microsoft Defender Advanced Threat protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)을 사용 하 여 보호 기능을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df27-136">Extend protection with [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection).</span></span>