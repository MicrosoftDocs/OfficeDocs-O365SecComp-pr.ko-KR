---
title: 서비스 거부 공격에 대 한 방어의 주요 원칙을 office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 어떻게 Microsoft 통해, 검색 및 서비스 거부 (DoS) 공격에 대 한 해당 방어에 완화의 핵심 원칙을 활용 합니다.
ms.openlocfilehash: 8355a7897c788241092363a23e198423e81c587a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532893"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a><span data-ttu-id="29760-103">서비스 거부 공격에 대한 보안 핵심 원칙</span><span class="sxs-lookup"><span data-stu-id="29760-103">Core Principles of Defense Against Denial-of-Service Attacks</span></span>
<span data-ttu-id="29760-p101">세 개 코어 통해, 검색 및 완화 방법 모두 네트워크 기반 DoS 공격을 방어 원칙입니다. 통해 검색, 이전에 발생 하 고 완화 하기 전에 수행 되는 검색 합니다. 통해는 DoS 공격에 대 한 최상의 방어입니다. 공격을 감지할 수 없는 완화할 수 없습니다. 하지만 DoS 공격 가장 작은 값을 전달 수 없음, 서비스 감지 되지 않을 공격에 대 한 충분 한 시간 살아남기가 이동 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29760-p101">The three core principles when defending against network-based DoS attacks are Absorption, Detection, and Mitigation. Absorption happens before detection, and detection happens before mitigation. Absorption is the best defense against a DoS attacks. If the attack can't be detected, it can't be mitigated. But if even the smallest DoS attack can't be absorbed, then services aren't going to survive long enough for the attack to be detected.</span></span>

<span data-ttu-id="29760-p102">물론 않은 일반적으로 대부분의 조직에서는이 기술 및 기술에 상당한 투자의 요구에 따라 DoS 공격을 처리 하는 데 필요한 여분의 용량을 구입 하는 것이 불가능 합니다. 이 강조 표시 하는 Microsoft 클라우드 서비스를 사용 하는 보안 이점 중 하나 서비스에 대 한 그 규모 비용 효율적인 방식으로 강력한 네트워크 보호 클라우드 고객에 게 제공할 수 있습니다. 하지만 수직 확장의도 하지만 여전히 있어야 통해, 검색 및 완화 방법 간의 균형 합니다. 해당 간의 균형을 찾으려고 있어 병합할 해야 얼마나 예측 하는 공격 증가율을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="29760-p102">Of course, it is generally not economically feasible for most organizations to purchase the excess capacity necessary to absorb DoS attacks, as this requires a considerable investment in technology and technical skills. This highlights one of the security benefits of using Microsoft cloud services; the sheer scale of our services enables us to provide strong network protection to our cloud customers in a cost-effective manner. But even at our scale, though, there must still be a balance between absorption, detection, and mitigation. To find that balance, we study an attack's growth rate to estimate how much we need to absorb.</span></span>

<span data-ttu-id="29760-p103">검색은 cat-and-mouse 게임입니다. 새로운 방법으로 사용자는 하면 공격 또는 시스템 물리 하려고를 지속적으로 유사 해야 합니다. 검색-Mitigate > 검색-> Mitigate 등과 같은->, 무기한 계속 영구, 영구 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29760-p103">Detection is a cat-and-mouse game. You must constantly look for the new ways people are attacking you or trying to defeat your systems. Detect -> Mitigate -> Detect -> Mitigate, etc., is a perpetual, persistent state that will continue indefinitely.</span></span>

## <a name="defending-against-dos-attacks"></a><span data-ttu-id="29760-116">DoS 공격에 대 한 방어</span><span class="sxs-lookup"><span data-stu-id="29760-116">Defending Against DoS Attacks</span></span>
<span data-ttu-id="29760-p104">DoS 공격을 성공적으로 방어를 초기 검색 반드시 필요 합니다. 시스템에 병목 현상이 발생 하기 전에 공격을 감지, 하 여 방어 대응 계획을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29760-p104">To successfully defend against a DoS attack, early detection is essential. By detecting an attack before the system is overwhelmed, defenders can execute a response plan.</span></span>

<span data-ttu-id="29760-119">다음 수식을 DoS 공격에 영향을 줄에 시간에 근접 한 여러 하는데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29760-119">The following formula will help approximate the time to impact of a DoS attack:</span></span>

   <span data-ttu-id="29760-120">**최대 용량 (최대 용량 X 증가 비율) / = 시간에 미치는 영향**</span><span class="sxs-lookup"><span data-stu-id="29760-120">**Maximum Capacity / (Maximum Capacity X Growth Rate) = Time to Impact**</span></span>

<span data-ttu-id="29760-p105">것일 수 검색 시간에 영향을 시간 후 발생 하는 경우에 DoS 공격 성공적으로 수행 됩니다. 검색 시간에 영향을 시간 전에 발생 하는 경우 온라인 및 완화 전략을 사용 하는 경우에 액세스할 공격 서비스 유지 되어야 합니다. 따라서 다음과 같은 사항을 두 DoS 공격을 방어을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29760-p105">If the time-to-detection occurs after time-to-impact, then it is likely the DoS attack will be successful. If the time-to-detection occurs before time-to-impact, then the services being attacked should remain online and accessible, if mitigation strategies are used. Thus, there are only two things that can be done to defend against DoS attacks:</span></span>
- <span data-ttu-id="29760-124">거듭제곱할 (차례 대로 제공 하는 공격을 감지 하는 시간이 더) 최대 용량;의 최대 용량 증가 또는</span><span class="sxs-lookup"><span data-stu-id="29760-124">Increase capacity to raise the ceiling of maximum capacity (which in turn provides more time to detect an attack); or</span></span>
- <span data-ttu-id="29760-125">검색 하는 시간을 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="29760-125">Decrease the time to detect.</span></span>

<span data-ttu-id="29760-p106">용량을 늘리는 가장 영향이 직접 회계 합니다. 고객 최소한의 기본 통해를 개발 하는 것이 좋습니다 용량 일부 수준의 DoS 공격을 살아남기 수 있는지 확인 합니다. 각 고객에 게 노출, 위험 및 재무 들이지에 대 한 자신의 임계값으로 실제 통해 용량에서 고객을 고객을 달라 집니다. 궁극적으로, 경제적인 이유로 연구 (영문) 및 시간을 검색 하려면 시간을 줄이는 방법에 대 한 투자는 일반적으로 가장 경제적인 방어 합니다.</span><span class="sxs-lookup"><span data-stu-id="29760-p106">Increasing capacity has a direct fiscal impact. Microsoft recommends that customers develop at least basic absorption capacity, to ensure that they can survive some level of DoS attack. The actual absorption capacity will vary from customer to customer, as each customer has their own thresholds for exposure, risk, and financial outlay. Ultimately, for economic reasons, investments of research and time in ways to decrease time-to-detection are usually the most cost-effective defense.</span></span>
