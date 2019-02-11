---
title: 고급 eDiscovery (미리 보기)에서 custodians 사용
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 4dd2c44b40b5d458f9b200c249fe2f9bb16f83e0
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706019"
---
# <a name="work-with-custodians-in-advanced-ediscovery-preview"></a><span data-ttu-id="1db22-102">고급 eDiscovery (미리 보기)에서 custodians 사용</span><span class="sxs-lookup"><span data-stu-id="1db22-102">Work with custodians in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="1db22-p101">자주, 조직에 응답 법적 조사 하는 경우 잠재적으로 관련 된 콘텐츠를 식별 하 고, 보존, 수집 주위 워크플로 작업이 기반으로 조직 내의 사용자 또는 데이터 custodians 합니다. EDiscovery, 이러한 개인 데이터 custodians 호출 되 면 하 고 "사용자에 게 문서 또는 전자 파일의 관리 제어 필요"로 정의 됩니다. 예, 전자 메일의 데이터 더불어 관련 된 메시지를 포함 하는 사서함의 소유자 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1db22-p101">Often, when an organization is responding to a legal investigation, the workflow around identifying, preserving, and collecting potentially relevant content is based off people or data custodians within their organization. In eDiscovery, these individuals are called data custodians and are defined as “persons having administrative control of a document or electronic file”. For example, the data custodian of an email could be the owner of the mailbox which contains the relevant message.</span></span>  

<span data-ttu-id="1db22-p102">조사 시작 되 면 eDiscovery 팀 모든 관련 custodians 및 데이터 원본 대/소문자와 관련 된를 신속 하 게 식별 해야 합니다. Custodians 및 해당 데이터 원본 목록을 시간이 지남에 따라 확장 되거나 축소 될 수 있습니다. 결과적으로, 조직에 대 한 제어 프로세스를 식별 하를 유지 하 고 수집 하는 경우의 수명 주기 전반에 걸쳐 custodial 콘텐츠를 유지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1db22-p102">When an investigation begins, the eDiscovery team must quickly identify all the relevant custodians and data sources related to the case. Over time, the lists of custodians and their data sources may expand or contract. As a result, organizations must maintain a controlled process around identifying, preserving, and collecting custodial content throughout the lifecycle of a case.</span></span>

<span data-ttu-id="1db22-p103">(미리 보기) 고급 eDiscovery 사례, 내에서 법적 팀 데이터 custodians로 조직 내에서 개별 사용자를 추가 하 고 자동으로 식별 하 고 수 Exchange, OneDrive, SharePoint 및 팀 사이트와 같은 custodial 원본의 보존 합니다. 기본 제공 하 고 전체 더불어 관리 도구를 사용 하 여 조직 수 전자적으로 저장 된 정보 (ESI) 실수로 삭제 되지 않도록에서 보호 하 고 수동, 시간이 오래 걸릴 goodbye 라고 표시 및 오류가 발생 하기 쉬운 법률 프로세스를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="1db22-p103">Within an Advanced eDiscovery (Preview) case, legal teams can add individuals within their organization as data custodians and automatically identify and preserve custodial sources such as Exchange, OneDrive, SharePoint, and Teams sites. By using the built-in and in-place Custodian Management tool, organizations can secure electronically stored information (ESI) from inadvertent deletion and say goodbye to manual, time consuming, and error-prone legal hold processes.</span></span> 

<span data-ttu-id="1db22-111">Custodians를 사용 하는 방법에 대 한 자세한 내용은 다음 문서를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="1db22-111">For more information about working with custodians, see the following articles:</span></span> 

- [<span data-ttu-id="1db22-112">보유자를 사례에 추가</span><span class="sxs-lookup"><span data-stu-id="1db22-112">Add custodians to a case</span></span>](add-custodians-to-case.md)

- [<span data-ttu-id="1db22-113">경우에는 custodians 관리</span><span class="sxs-lookup"><span data-stu-id="1db22-113">Manage custodians in a case</span></span>](manage-new-custodians.md)

- [<span data-ttu-id="1db22-114">보유자 활동 보기</span><span class="sxs-lookup"><span data-stu-id="1db22-114">View custodian activity</span></span>](view-custodian-activity.md)

## <a name="roles-and-permissions"></a><span data-ttu-id="1db22-115">역할 및 사용 권한</span><span class="sxs-lookup"><span data-stu-id="1db22-115">Roles and permissions</span></span>

<span data-ttu-id="1db22-116">고급 eDiscovery (미리 보기)에서 고급 eDiscovery (미리 보기)의 끝-워크플로 관리할 수 있도록 사용자에 게 필요한 사용 권한을 할당 하는 기본 제공 eDiscovery 관리자 역할 그룹을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1db22-116">In Advanced eDiscovery (Preview), you can use the built-in eDiscovery Manager role group to assign the necessary permissions to users so they can manage the end-to-end workflow in Advanced eDiscovery (Preview).</span></span>
