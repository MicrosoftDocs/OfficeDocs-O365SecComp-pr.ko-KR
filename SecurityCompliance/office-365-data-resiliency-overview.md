---
title: Office 365의 데이터 복구
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
description: Microsoft Office 365에서 데이터 복구를 이해 합니다.
ms.openlocfilehash: 7d43c766615ff1520c6529427116c42795da8565
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533774"
---
# <a name="data-resiliency-in-office-365"></a><span data-ttu-id="f607b-103">Office 365의 데이터 복구</span><span class="sxs-lookup"><span data-stu-id="f607b-103">Data Resiliency in Office 365</span></span>

## <a name="introduction"></a><span data-ttu-id="f607b-104">소개</span><span class="sxs-lookup"><span data-stu-id="f607b-104">Introduction</span></span>
<span data-ttu-id="f607b-p101">클라우드 컴퓨팅의 복잡 한 특성을 감안할 Microsoft는 아닌지는 경우의 작업, 잘못 된 들어갈 수 있지만 때 고려해 야 합니다. 안정성을 최대화 하 고 문제가 발생 하는 경우 고객에 부정적인 영향을 최소화 하려면 클라우드 서비스 디자인 했습니다. 복잡 한 물리적 인프라에 의존의 전통적인 전략 뒤로 이동 했기 우리 및 클라우드 서비스에 직접 중복을 구축 했습니다. 덜 복잡 한 실제 인프라 및 데이터 복구 서비스를 작성 하 고 고객에 게 고가용성을 제공 하는 보다 지능적인 소프트웨어의 조합을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f607b-p101">Given the complex nature of cloud computing, Microsoft is mindful that it's not a case of if things will go wrong, but rather when. We design our cloud services to maximize reliability and minimize the negative effects on customers when things do go wrong. We have moved beyond the traditional strategy of relying on complex physical infrastructure, and we have built redundancy directly into our cloud services. We use a combination of less complex physical infrastructure and more intelligent software that builds data resiliency into our services and delivers high availability to our customers.</span></span> 

## <a name="resiliency-and-recoverability-are-built-in"></a><span data-ttu-id="f607b-109">복구 및 복구 기능을 기본 제공</span><span class="sxs-lookup"><span data-stu-id="f607b-109">Resiliency and Recoverability Are Built-in</span></span> 
<span data-ttu-id="f607b-p102">원본으로 사용 하는 인프라와 프로세스 일부 지점에서 실패 하는 가정으로 시작 하는 복구 및 복구에 건물: 하드웨어 (인프라) 실패 하 고, 휴먼 실수를 좀더, 소프트웨어 버그를 갖습니다. 것은 소프트웨어 개발자가 클라우드 하기 전에 이러한 사항에 대 한 답변 되지 않은 나타내도록 올바른, 하는 동안 클라우드 하기 전에 매우 다양 한 일반적인 IT 구현에서 이러한 문제 된 처리 하는 방법:</span><span class="sxs-lookup"><span data-stu-id="f607b-p102">Building in resiliency and recovery starts with the assumption that the underlying infrastructure and processes will fail at some point: hardware (infrastructure) will fail, humans will make mistakes, and software will have bugs. While it would be incorrect to say that software developers were not thinking about these things before the cloud, how these issues were handled in a typical IT implementation was very different before the cloud:</span></span> 
- <span data-ttu-id="f607b-p103">첫째, 하드웨어 및 인프라 보호 된 중요 합니다. 이 데이터 센터 99.99% 안정성 필요한 중요 한 기능 및 네트워크 중복 된 것을 의미 하 고 서버 하드웨어 기반 클러스터링을 사용 하면 이중 전원 공급 장치, 이중 네트워크 인터페이스와 유사한 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="f607b-p103">First, hardware and infrastructure protections were significant. This meant having datacenters with 99.99% reliability required significant power and network redundancy, and servers were implemented with hardware-based clustering, dual power supplies, dual network interfaces, and the like.</span></span> 
- <span data-ttu-id="f607b-p104">둘째, 프로세스가 했습니다 기능도 뛰어납니다. 작업 팀이 유지 되는 엄격한 절차, windows가 사용 하 여, 변경 하 고 중요 한 프로젝트 관리 오버 헤드가 경우가 많았습니다 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="f607b-p104">Second, process was paramount. Operations teams maintained rigorous procedures, change windows were employed, and there was often significant project management overhead.</span></span> 
- <span data-ttu-id="f607b-p105">셋째, 배포 얼음 속도로 발생 합니다. 패치 릴리스에 대 한 대기 불과하며 소스를 소유 하지 않고 코드를 배포 하 고 관련 된 하드웨어를 교체 하 고 중요 한 자본 들이지 주 버전을 해제 합니다. 또한, 문제를 해결 하는 유일한 방법은 롤백 했습니다. 따라서 대부분의 IT 조직만 주요 릴리스를 최신 상태로 유지 하는 작업을 방지 하기 위해 배포 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f607b-p105">Third, deployment took place at a glacial pace. Deploying code without owning the source meant waiting for patch releases, and major version releases involved hardware replacement and significant capital outlay. Moreover, the only way to correct a problem was to rollback. Thus, most IT organizations would deploy only major releases to avoid the work to keep up-to-date.</span></span> 
- <span data-ttu-id="f607b-120">마지막으로 배포 된 시스템의 배율을 물론 해당 interconnectedness 수준의 획기적인 훨씬 보다 작은 경우는 이제 했습니다.</span><span class="sxs-lookup"><span data-stu-id="f607b-120">Finally, the scale of deployed systems, as well as the level of their interconnectedness was historically much smaller than it is now.</span></span> 

<span data-ttu-id="f607b-121">오늘날 고객 품질에 영향을 미치지 않고 예상 되는 Microsoft에서 제공 되는 연속 혁신적 하 고 복구 및 복구 기능에에서 사용 하 여 Microsoft의 서비스 및 소프트웨어는 제작 하는 이유는 이유 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="f607b-121">Today, customers expect continuous innovation from Microsoft without compromising quality, and this is one of the reasons why Microsoft's services and software are built with resiliency and recoverability in mind.</span></span> 

## <a name="office-365-data-resiliency-principles"></a><span data-ttu-id="f607b-122">Office 365 데이터 복구 원칙</span><span class="sxs-lookup"><span data-stu-id="f607b-122">Office 365 Data Resiliency Principles</span></span> 
<span data-ttu-id="f607b-p106">복구는 특정 유형의 오류에 대응 하 고 아직 완벽 하 게 작동 고객의 관점에서 볼 때 상태를 유지 하는 클라우드 기반 서비스의 능력을 나타냅니다. 데이터 복구는 Office 365 내에서 어떤 오류가 발생할에 관계 없이 중요 한 고객 데이터 유지 되도록 그대로 유지 하 고 영향을 받지 않은 것을 의미 합니다. 이 위해 Office 365 서비스 되지 않습니다 약 5 개의 특정 복구 원칙을 설계 합니다.</span><span class="sxs-lookup"><span data-stu-id="f607b-p106">Resiliency refers to the ability of a cloud-based service to withstand certain types of failures and yet remain fully-functional from the customers' perspective. Data resiliency means that no matter what failures occur within Office 365, critical customer data remains intact and unaffected. To that end, Office 365 services have been designed around five specific resiliency principles:</span></span> 
- <span data-ttu-id="f607b-p107">중요 하 고 중요 하지 않은 데이터 방법이 있습니다. 특수 한 오류 시나리오에서 (등 여부는 메시지를 읽었습니다) 비-중요 한 데이터를 삭제할 수 있습니다. 아주 비용에 중요 한 데이터 (예: 전자 메일 메시지와 같은 고객 데이터)를 보호 해야 합니다. 디자인 목표를으로 배달 된 메일 메시지는 중요, 항상이 고 메시지를 읽은 여부 등의 작업은 중요 하지 않은 합니다.</span><span class="sxs-lookup"><span data-stu-id="f607b-p107">There is critical and non-critical data. Non-critical data (for example, whether a message was read) can be dropped in rare failure scenarios. Critical data (for example, customer data such as email messages) should be protected at extreme cost. As a design goal, delivered mail messages are always critical, and things like whether a message has been read is non-critical.</span></span> 
- <span data-ttu-id="f607b-130">고객 데이터의 복사본을 다른 내결함성 영역으로 구분 해야 마다 오류 격리를 제공 하려면 도메인 (예: 데이터 센터를 단일 자격 증명 (프로세스, 서버 또는 연산자) 하 여 액세스할 수 있는) 최대한 내결함성 많은 합니다.</span><span class="sxs-lookup"><span data-stu-id="f607b-130">Copies of customer data must be separated into different fault zones or as many fault domains as possible (e.g., datacenters, accessible by single credentials (process, server, or operator)) to provide failure isolation.</span></span> 
- <span data-ttu-id="f607b-131">원자성, 일관성, 격리, 내구성 (ACID)의 일부를 실패 하는 것에 대 한 중요 한 고객 데이터를 모니터링할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f607b-131">Critical customer data must be monitored for failing any part of Atomicity, Consistency, Isolation, Durability (ACID).</span></span> 
- <span data-ttu-id="f607b-p108">고객 데이터 손실 로부터 보호 되어야 합니다. 적극적으로 스캔 하 또는 모니터링, 수리 가능한 및 복구할 수 있는 것이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f607b-p108">Customer data must be protected from corruption. It must be actively scanned or monitored, repairable, and recoverable.</span></span> 
- <span data-ttu-id="f607b-134">따라서 고객의 작업에서 대부분의 데이터 손실 결과 실수로 삭제 된 항목을 복원할 수 있게 해 주는 GUI를 사용 하 여 자신의 복구 하는 고객을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f607b-134">Most data loss results from customer actions, so allow customers to recover on their own using a GUI that enables them to restore accidentally deleted items.</span></span> 
 
<span data-ttu-id="f607b-135">강력한 테스트 및 유효성 검사를 연결 하 여 이러한 원칙, 고객 클라우드 서비스의 구축을 통해 Office 365는를 충족 하 고 연속 혁신 하 고 개선 하기 위한 플랫폼을 보장 하면서 고객의 요구를 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f607b-135">Through the building of our cloud services to these principles, coupled with robust testing and validation, Office 365 is able to meet and exceed the requirements of customers while ensuring a platform for continuous innovation and improvement.</span></span> 

## <a name="related-links"></a><span data-ttu-id="f607b-136">관련된 링크</span><span class="sxs-lookup"><span data-stu-id="f607b-136">Related Links</span></span>

- [<span data-ttu-id="f607b-137">데이터 손상 처리</span><span class="sxs-lookup"><span data-stu-id="f607b-137">Dealing with Data Corruption</span></span>](office-365-dealing-with-data-corruption.md)
- [<span data-ttu-id="f607b-138">맬웨어 및 랜섬웨어 보호</span><span class="sxs-lookup"><span data-stu-id="f607b-138">Malware and Ransomware Protection</span></span>](office-365-malware-and-ransomware-protection.md)
- [<span data-ttu-id="f607b-139">모니터링 및 자동 복구</span><span class="sxs-lookup"><span data-stu-id="f607b-139">Monitoring and Self-Healing</span></span>](office-365-monitoring-and-self-healing.md)
- [<span data-ttu-id="f607b-140">Exchange 데이터 복구</span><span class="sxs-lookup"><span data-stu-id="f607b-140">Exchange Data Resiliency</span></span>](office-365-exchange-data-resiliency.md)
- [<span data-ttu-id="f607b-141">SharePoint 데이터 복구</span><span class="sxs-lookup"><span data-stu-id="f607b-141">SharePoint Data Resiliency</span></span>](office-365-sharepoint-data-resiliency.md)