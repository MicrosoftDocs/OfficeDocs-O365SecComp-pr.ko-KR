---
title: Advanced eDiscovery (Preview)에서 custodians을 사용 하 여 작업
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 538fd7e67456bc669b9f5cf140c995a716239fc2
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32240990"
---
# <a name="work-with-custodians-in-advanced-ediscovery-preview"></a><span data-ttu-id="1d462-102">Advanced eDiscovery (Preview)에서 custodians을 사용 하 여 작업</span><span class="sxs-lookup"><span data-stu-id="1d462-102">Work with custodians in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="1d462-103">조직이 법적 조사에 응답 하는 경우 관련 콘텐츠를 식별, 보존 및 수집 하는 워크플로는 조직 내의 사용자 또는 데이터 custodians을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d462-103">When an organization is responding to a legal investigation, the workflow around identifying, preserving, and collecting potentially relevant content is based off people or data custodians within their organization.</span></span> <span data-ttu-id="1d462-104">eDiscovery에서는 이러한 개인을 *data custodians* (또는 *custodians*) 라고 하며, 문서 또는 전자 파일에 대 한 관리 권한을 가진 사람으로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d462-104">In eDiscovery, these individuals are called *data custodians* (or just *custodians*) and are defined as "persons having administrative control of a document or electronic file.</span></span> <span data-ttu-id="1d462-105">예를 들어 전자 메일 메시지의 custodian는 관련 메시지를 포함 하는 사서함의 소유자가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d462-105">For example, the custodian of an email message could be the owner of the mailbox which contains the relevant message.</span></span>  

<span data-ttu-id="1d462-106">조사가 시작 되 면 eDiscovery 팀은 사례와 관련 된 모든 관련 custodians 및 데이터 원본을 빠르게 식별 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d462-106">When an investigation begins, the eDiscovery team must quickly identify all the relevant custodians and data sources related to the case.</span></span> <span data-ttu-id="1d462-107">시간이 지남에 따라 custodians 및 해당 데이터 원본 목록이 늘어나거나 decreasse 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d462-107">Over time, the list of custodians and their data sources may increase or decreasse.</span></span> <span data-ttu-id="1d462-108">따라서 조직은 사례 수명 주기 동안 custodial 콘텐츠를 식별, 보존 및 수집 하는 제어 된 프로세스를 유지 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d462-108">As a result, organizations must maintain a controlled process around identifying, preserving, and collecting custodial content throughout the life cycle of a case.</span></span>

<span data-ttu-id="1d462-109">고급 eDiscovery (미리 보기)의 경우 법률 팀은 조직의 개인을 custodians으로 추가 하 고 Exchange 사서함, OneDrive 계정, SharePoint 및 팀 사이트 등의 custodial 데이터 원본을 자동으로 식별 하 고 보존할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d462-109">Within an Advanced eDiscovery (Preview) case, legal teams can add individuals in their organization as custodians and automatically identify and preserve custodial data sources such as Exchange mailboxes, OneDrive accounts, and SharePoint and Teams sites.</span></span> <span data-ttu-id="1d462-110">고급 eDiscovery (미리 보기)에서 기본 제공 custodian 관리 도구를 사용 하 여 조직에서 실수로 또는 의도적인 삭제를 통해 전자적으로 저장 된 정보를 보호 하 고 수동, 시간이 오래 걸리고 오류가 발생 하기 쉬운 법적 보존을 사용할 수 있습니다. 프로세서.</span><span class="sxs-lookup"><span data-stu-id="1d462-110">By using the built-in custodian management tool in Advanced eDiscovery (Preview), organizations can secure electronically stored information from inadvertent (or intentional) deletion and say goodbye to manual, time consuming, and error-prone legal hold processes.</span></span> 

<span data-ttu-id="1d462-111">custodians 사용에 대 한 자세한 내용은 다음 문서를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1d462-111">For more information about working with custodians, see the following articles:</span></span> 

- [<span data-ttu-id="1d462-112">보유자를 사례에 추가</span><span class="sxs-lookup"><span data-stu-id="1d462-112">Add custodians to a case</span></span>](add-custodians-to-case.md)

- [<span data-ttu-id="1d462-113">사례에서 custodians 관리</span><span class="sxs-lookup"><span data-stu-id="1d462-113">Manage custodians in a case</span></span>](manage-new-custodians.md)

- [<span data-ttu-id="1d462-114">보유자 활동 보기</span><span class="sxs-lookup"><span data-stu-id="1d462-114">View custodian activity</span></span>](view-custodian-activity.md)

## <a name="roles-and-permissions"></a><span data-ttu-id="1d462-115">역할 및 사용 권한</span><span class="sxs-lookup"><span data-stu-id="1d462-115">Roles and permissions</span></span>

<span data-ttu-id="1d462-116">고급 ediscovery (미리 보기)에서 기본 제공 ediscovery 관리자 역할 그룹을 사용 하 여 사용자가 고급 eDiscovery (미리 보기)에서 종단간 워크플로를 관리할 수 있도록 필요한 사용 권한을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d462-116">In Advanced eDiscovery (Preview), you can use the built-in eDiscovery Manager role group to assign the necessary permissions to users so they can manage the end-to-end workflow in Advanced eDiscovery (Preview).</span></span>
