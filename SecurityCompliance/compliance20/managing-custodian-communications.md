---
title: Advanced eDiscovery에서 통신 사용
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 고급 eDiscovery를 사용 하면 법적 조사에 custodians 알리는 법적 보존 알림 워크플로를 쉽게 관리할 수 있습니다.
ms.openlocfilehash: cf5c8f5e932993255bda2cb959657c2c6ded3163
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154910"
---
# <a name="work-with-communications-in-advanced-ediscovery"></a><span data-ttu-id="cd741-103">Advanced eDiscovery에서 통신 사용</span><span class="sxs-lookup"><span data-stu-id="cd741-103">Work with communications in Advanced eDiscovery</span></span>

<span data-ttu-id="cd741-104">고급 eDiscovery를 사용 하면 법적 부서에서 법적 보존 알림을 추적 및 배포 하기 위한 프로세스를 단순화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-104">Advanced eDiscovery allows legal departments to simplify their processes around tracking and distributing legal hold notifications.</span></span> <span data-ttu-id="cd741-105">Custodian communications tool을 사용 하면 법무 부서가 전체 법적 프로세스, 초기 알림, 미리 알림 및 에스컬레이션을 모두 한 곳에 관리 및 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-105">The custodian communications tool enables legal departments to manage and automate the entire legal hold process, from initial notifications, to reminders, and to escalations, all in one location.</span></span>

## <a name="what-is-a-legal-hold-notification"></a><span data-ttu-id="cd741-106">법적 보존 알림 이란?</span><span class="sxs-lookup"><span data-stu-id="cd741-106">What is a legal hold notification?</span></span>

<span data-ttu-id="cd741-107">법적 보존 ( *소송 보존*이 라고도 함)은 조직의 법률 부서에서 법적 조사와 관련이 있을 수 있는 직원, 불확정 직원 또는 custodians에 게 전송 되는 알림입니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-107">A legal hold (also known as a *litigation hold*) notice is a notification sent from an organization’s legal department to employees, contingent staff, or custodians of data that may be relevant to a legal investigation.</span></span> <span data-ttu-id="cd741-108">이러한 알림은 활성 또는 임박한 법적 정보와 관련이 있을 수 있는 모든 콘텐츠 뿐만 아니라 전자적으로 저장 된 정보를 보존 하도록 custodians에 게 지시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-108">These notifications instruct custodians to preserve electronically stored information as well as any content that may be relevant to an active or impending legal matter.</span></span> <span data-ttu-id="cd741-109">법률 팀에서는 각 custodian가 제공 된 지침을 준수 하 고, 읽고, 이해 하 고 동의한 것으로 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-109">Legal teams must know that each custodian has received, read, understood, and has agreed to comply with the given instructions.</span></span>

## <a name="the-legal-hold-notification-process"></a><span data-ttu-id="cd741-110">법적 보존 알림 프로세스</span><span class="sxs-lookup"><span data-stu-id="cd741-110">The legal hold notification process</span></span>

<span data-ttu-id="cd741-111">조직은 임박한 소송 또는 규제 조사에 대해 학습 하는 경우 관련 정보를 보존 하는 업무를 담당 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-111">An organization has a duty to preserve relevant information when it learns about an impending litigation or regulatory investigation.</span></span> <span data-ttu-id="cd741-112">조사에 대 한 보존 요구 사항을 준수 하기 위해 조직은 적절 한 정보를 보존 하기 위한 업무에 대 한 잠재적 custodians을 즉시 알려야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-112">To comply with the preservation requirements of an investigation, the organization should immediately inform potential custodians about their duty to preserve relevant information.</span></span>

<span data-ttu-id="cd741-113">고급 eDiscovery를 사용 하는 경우 법률 팀은 법적 보존 알림 워크플로를 만들고 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-113">With Advanced eDiscovery, legal teams can create and customize their legal hold notification workflow.</span></span> <span data-ttu-id="cd741-114">Custodian communications tool을 사용 하면 합법적인 팀이 다음과 같은 공지와 워크플로를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-114">The custodian communications tool lets legal teams to configure the following notices and workflows:</span></span>

1. <span data-ttu-id="cd741-115">**발급 알림**: 법적 고 지 사항에 대 한 관련 정보를 확인할 수 있는 custodians에 법적 부서의 알림으로 법률 보존 알림을 발급 (또는 시작) 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-115">**Issuance notice**: A legal hold notice is issued (or initiated) by a notification from the legal department to custodians who may have relevant information about the case matter.</span></span> <span data-ttu-id="cd741-116">이 알림 메시지는 검색에 필요한 모든 정보를 보존 하도록 custodians에 지시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-116">This notice instructs the custodians to preserve any information that may be needed for discovery.</span></span>
   
2.  <span data-ttu-id="cd741-117">**재발급 통지**: 예를 들어 custodians는 이전에 요청한 것 보다 더 많은 콘텐츠 (또는 더 적은 콘텐츠)를 보존 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-117">**Re-Issuance notice**: During a case, custodians may be required to preserve additional content (or less content) than was previously requested.</span></span> <span data-ttu-id="cd741-118">이 시나리오에서는 기존 보존 통지를 업데이트 하 고 custodians에 다시 발행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-118">For this scenario, you can update the existing hold notice and re-issue it to custodians.</span></span>

3.  <span data-ttu-id="cd741-119">**릴리스 알림**: 문제가 해결 되 고 custodian가 보존 요구 사항에 더 이상 적용 되지 않으면 사례에서 custodian를 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-119">**Release notice**: Once a matter is resolved and the custodian is no longer subject to a preservation requirement, the custodian can be released from the case.</span></span> <span data-ttu-id="cd741-120">또한 콘텐츠를 보존 하는 데 더 이상 필요 하지 않음을 custodian에 게 알릴 수 있으며, 데이터와 관련 하 여 일반적인 작업 활동을 다시 시작 하는 방법에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-120">Additionally, you can notify the custodian that they are no longer required to preserve content, and provide instructions about how to resume their normal work activity with regard to their data.</span></span>

4. <span data-ttu-id="cd741-121">**미리 알림 및 에스컬레이션**: 일부 인스턴스에서는 알림을 발급 하는 것 만으로는 법적 검색 요구 사항을 충족 하기에 충분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-121">**Reminders and escalations**: In some instances, just issuing a notice isn't enough to satisfy legal discovery requirements.</span></span> <span data-ttu-id="cd741-122">각 알림을 사용 하는 경우 법률 팀은 미리 알림 및 에스컬레이션 워크플로 집합에서 응답 하지 않는 custodians 자동으로 추가 작업을 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-122">With each notification, legal teams can schedule a set of reminder and escalation workflows to automatically follow-up with unresponsive custodians.</span></span>

    - <span data-ttu-id="cd741-123">**미리 알림**: 법적 보존 알림을 발급 하거나 custodians 집합으로 다시 발급 한 후 조직에서 응답 하지 않는 custodians 알림을 보내도록 미리 알림을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-123">**Reminders**:  After a legal hold notice has been issued or re-issued to a set of custodians, an organization can set up reminders to alert unresponsive custodians.</span></span>

    - <span data-ttu-id="cd741-124">**에스컬레이션**: 일정 기간 동안 미리 알림 집합에도 불구 하 고 custodian 응답 하지 않는 경우 법률 팀은 응답성이 없는 워크플로를 설정 하 여 응답 하지 않는 custodians 및 관리자에 게 알릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-124">**Escalations**: In some cases, if a custodian remains unresponsive even after a set of reminders over a period of time, the legal team can set up an escalation workflow to notify unresponsive custodians and their manager.</span></span>

## <a name="role-groups-and-permissions"></a><span data-ttu-id="cd741-125">역할 그룹 및 사용 권한</span><span class="sxs-lookup"><span data-stu-id="cd741-125">Role groups and permissions</span></span> 

<span data-ttu-id="cd741-126">법률 팀은 보안 & 준수 센터에서 eDiscovery 관련 역할 그룹 및 사용 권한을 사용 하 여 서비스 케이스 활동을 제어 하 고 분리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-126">Legal teams can control and segregate their case activity using eDiscovery-related role groups and permissions in the Security & Compliance Center.</span></span> 

<span data-ttu-id="cd741-127">법적 보존 알림을 만들고 관리 하려면 사용자가 다음 역할 그룹에 속해 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-127">To create and manage legal hold notifications, a user must be part of the following role groups:</span></span>

- <span data-ttu-id="cd741-128">**Ediscovery 관리자** -이 역할 그룹의 구성원은 ediscovery 사례를 만들고 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-128">**eDiscovery Manager** - Members of this role group can create and manage eDiscovery cases.</span></span> <span data-ttu-id="cd741-129">구성원을 추가 및 제거 하 고, custodians 및 콘텐츠 위치를 보류 하 고, 법률 보존 알림을 관리 하 고, 사례와 연결 된 콘텐츠 검색을 만들고 편집 하 고, 콘텐츠 검색 결과를 내보내고, 고급 분석을 위한 검색 결과를 준비할 수 있습니다. eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="cd741-129">They can add and remove members, place custodians and content locations on hold, manage legal hold notifications, create and edit Content Searches associated with a case, export the results of a Content Search, and prepare search results for analysis in Advanced eDiscovery.</span></span> <span data-ttu-id="cd741-130">이 역할 그룹에 두 개의 하위 그룹이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-130">There are two sub-groups in this role group.</span></span> <span data-ttu-id="cd741-131">이러한 하위 그룹 간의 차이는 범위를 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-131">The difference between these subgroups is based on scope.</span></span>

  - <span data-ttu-id="cd741-132">**Ediscovery 관리자** -자신이 만들거나 구성원 인 ediscovery 사례를 보고 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-132">**eDiscovery Manager** - Can view and manage the eDiscovery cases they create or are a member of.</span></span> <span data-ttu-id="cd741-133">다른 eDiscovery 관리자가 사례를 만들었지만 두 번째 eDiscovery 관리자를 해당 사례 구성원으로 추가 하지 않는 경우 두 번째 eDiscovery 관리자가 Security & 준수 센터의 eDiscovery 페이지에서 사례를 보거나 열 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-133">If another eDiscovery Manager creates a case but doesn't add a second eDiscovery Manager as a member of that case, the second eDiscovery Manager won't be able to view or open the case on the eDiscovery page in the Security & Compliance Center.</span></span> <span data-ttu-id="cd741-134">eDiscovery 관리자는 고급 eDiscovery의 사례에 액세스 하 여 분석 작업을 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-134">eDiscovery Managers can also access their cases in Advanced eDiscovery to perform analysis tasks.</span></span>

  - <span data-ttu-id="cd741-135">**Ediscovery 관리자** -ediscovery 관리자가 수행할 수 있는 모든 사례 관리 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-135">**eDiscovery Administrator** - Can perform all case management tasks that an eDiscovery Manager can do.</span></span> <span data-ttu-id="cd741-136">또한 eDiscovery 관리자(Administrator)는 다음과 같은 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-136">Additionally, an eDiscovery Administrator can:</span></span>
    
    - <span data-ttu-id="cd741-137">eDiscovery 페이지에 나열된 모든 사례를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-137">View all cases that are listed on the eDiscovery page.</span></span>
    - <span data-ttu-id="cd741-138">조직의 대/소문자를 구성원으로 추가한 후 조직에서 모든 사례를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd741-138">Manage any case in the organization after they add themselves as a member of the case.</span></span>
    - <span data-ttu-id="cd741-139">조직의 모든 경우에 대 한 고급 eDiscovery의 사례 데이터 액세스</span><span class="sxs-lookup"><span data-stu-id="cd741-139">Access case data in Advanced eDiscovery for any case in the organization.</span></span>

<span data-ttu-id="cd741-140">자세한 내용은 [Security _AMP_ 준수 센터에서 eDiscovery 사용 권한 할당](../assign-ediscovery-permissions.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cd741-140">For more information, see [Assign eDiscovery permissions in the Security & Compliance Center](../assign-ediscovery-permissions.md).</span></span>