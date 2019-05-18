---
title: Advanced eDiscovery에서 custodians을 사용 하 여 작업
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
description: 고급 eDiscovery의 custodian 관리 도구를 사용 하면 법적 사례에 관심이 있는 사용자와 연결 된 데이터를 식별, 보존 및 수집 하는 방법에 대 한 워크플로를 관리할 수 있습니다.
ms.openlocfilehash: 6e365f0b7f80a0a5caa050b2e0b08c94dbed4746
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151600"
---
# <a name="work-with-custodians-in-advanced-ediscovery"></a><span data-ttu-id="09fe5-103">Advanced eDiscovery에서 custodians을 사용 하 여 작업</span><span class="sxs-lookup"><span data-stu-id="09fe5-103">Work with custodians in Advanced eDiscovery</span></span>

<span data-ttu-id="09fe5-104">조직이 법적 조사에 응답 하는 경우 관련 된 콘텐츠를 식별, 보존 및 수집 하는 워크플로는 관련 데이터를 custodians 조직의 구성원을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="09fe5-104">When an organization responds to a legal investigation, the workflow around identifying, preserving, and collecting potentially relevant content is based on the people in the organization who are the custodians of relevant data.</span></span> <span data-ttu-id="09fe5-105">EDiscovery에서는 이러한 개인을 *data custodians* (또는 *custodians*) 라고 하며 "문서 또는 전자 파일의 관리 권한을 가진 사람"으로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="09fe5-105">In eDiscovery, these individuals are called *data custodians* (or just *custodians*) and are defined as "persons having administrative control of a document or electronic file".</span></span> <span data-ttu-id="09fe5-106">예를 들어 전자 메일 메시지의 custodian는 관련 메시지를 포함 하는 사서함의 소유자가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09fe5-106">For example, the custodian of an email message could be the owner of the mailbox that contains the relevant message.</span></span>  

<span data-ttu-id="09fe5-107">조사가 시작 되 면 eDiscovery 팀은 사례와 관련 된 모든 관련 custodians 및 데이터 원본을 빠르게 식별 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="09fe5-107">When an investigation begins, the eDiscovery team must quickly identify all the relevant custodians and data sources related to the case.</span></span> <span data-ttu-id="09fe5-108">시간이 지남에 따라 custodians 및 해당 데이터 원본 목록이 늘어나거나 decreasse 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09fe5-108">Over time, the list of custodians and their data sources may increase or decreasse.</span></span> <span data-ttu-id="09fe5-109">따라서 조직은 사례 수명 주기 동안 custodial 콘텐츠를 식별, 보존 및 수집 하는 제어 된 프로세스를 유지 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="09fe5-109">As a result, organizations must maintain a controlled process around identifying, preserving, and collecting custodial content throughout the life cycle of a case.</span></span>

<span data-ttu-id="09fe5-110">고급 eDiscovery 사례에서는 법률 팀이 조직의 개인을 custodians으로 추가 하 고 Exchange 사서함, OneDrive 계정, SharePoint 및 팀 사이트 등의 custodial 데이터 원본을 자동으로 식별 하 고 보존할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09fe5-110">In an Advanced eDiscovery case, legal teams can add individuals in their organization as custodians, and automatically identify and preserve custodial data sources such as Exchange mailboxes, OneDrive accounts, and SharePoint and Teams sites.</span></span> <span data-ttu-id="09fe5-111">고급 eDiscovery의 기본 제공 custodian 관리 도구를 사용 하면 조직에서 실수로 또는 고의로 삭제 된 정보를 전자적으로 저장 하 여 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09fe5-111">By using the built-in custodian management tool in Advanced eDiscovery, organizations can secure electronically stored information from inadvertent (or intentional) deletion.</span></span> <span data-ttu-id="09fe5-112">이를 통해 적절 한 보존 프로세스를 수동으로 수행 해야 하는 시간이 걸리고 오류가 발생 하기 쉬운 프로세스를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09fe5-112">This lets you eliminate the time-consuming and error-prone process of manually having to perform the legal hold processes.</span></span> 

<span data-ttu-id="09fe5-113">Custodians 사용에 대 한 자세한 내용은 다음 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="09fe5-113">For more information about working with custodians, see the following:</span></span> 

- [<span data-ttu-id="09fe5-114">보유자를 사례에 추가</span><span class="sxs-lookup"><span data-stu-id="09fe5-114">Add custodians to a case</span></span>](add-custodians-to-case.md)

- [<span data-ttu-id="09fe5-115">사례에서 custodians 관리</span><span class="sxs-lookup"><span data-stu-id="09fe5-115">Manage custodians in a case</span></span>](manage-new-custodians.md)

- [<span data-ttu-id="09fe5-116">보유자 활동 보기</span><span class="sxs-lookup"><span data-stu-id="09fe5-116">View custodian activity</span></span>](view-custodian-activity.md)

## <a name="advanced-ediscovery-permissions"></a><span data-ttu-id="09fe5-117">고급 eDiscovery 권한</span><span class="sxs-lookup"><span data-stu-id="09fe5-117">Advanced eDiscovery permissions</span></span>

<span data-ttu-id="09fe5-118">고급 eDiscovery에서 기본 제공 eDiscovery 관리자 역할 그룹을 사용 하 여 올바른 investigators에 필요한 사용 권한을 할당할 수 있으므로 고급 eDiscovery에서 종단 간 워크플로를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09fe5-118">In Advanced eDiscovery, you can use the built-in eDiscovery Manager role group to assign the necessary permissions to legal investigators so they can manage the end-to-end workflow in Advanced eDiscovery.</span></span> <span data-ttu-id="09fe5-119">또는 고급 eDiscovery에서 특정 작업을 수행 하는 데 필요한 역할의 하위 집합을 사용 하 여 사용자 지정 역할 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09fe5-119">Alternatively, you can create custom role groups with a subset of the roles necessary to perform certain actions in a case in Advanced eDiscovery.</span></span> <span data-ttu-id="09fe5-120">EDiscovery 관련 역할에 대 한 자세한 내용은 [Security _AMP_ 준수 센터에서 ediscovery 사용 권한 할당](../assign-ediscovery-permissions.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="09fe5-120">For more information about eDiscovery-related roles, see [Assign eDiscovery permissions in the Security & Compliance Center](../assign-ediscovery-permissions.md).</span></span>
