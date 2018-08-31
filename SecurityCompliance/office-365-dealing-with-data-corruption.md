---
title: Office 365 데이터 손상을 처리
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
description: Office 365 및 Microsoft의 활동을 방지 하 고 복구 중에 데이터 손상의 설명 합니다.
ms.openlocfilehash: 087be23ce5dad1daf62357cb08e27c0a15962792
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533590"
---
# <a name="dealing-with-data-corruption-in-office-365"></a><span data-ttu-id="e7ac0-103">Office 365의에서 데이터 손상을 처리</span><span class="sxs-lookup"><span data-stu-id="e7ac0-103">Dealing with Data Corruption in Office 365</span></span>

<span data-ttu-id="e7ac0-p101">대규모 클라우드 서비스를 실행 하는 어려운 측면 중 하나 독립 시스템과 데이터의 양이 주어진 데이터 손상을 처리 하는 방법입니다. 데이터 손상을 원인일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-p101">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems. Data corruption can be caused by:</span></span>
- <span data-ttu-id="e7ac0-106">응용 프로그램 상태 중 일부 또는 전부를 손상 시 키 지 응용 프로그램 또는 인프라 버그</span><span class="sxs-lookup"><span data-stu-id="e7ac0-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span> 
- <span data-ttu-id="e7ac0-107">하드웨어 문제 손실 된 데이터 또는 데이터를 읽을 수 없으면 해당 결과</span><span class="sxs-lookup"><span data-stu-id="e7ac0-107">Hardware issues that result in lost data or an inability to read data</span></span> 
- <span data-ttu-id="e7ac0-108">휴먼 운영 오류</span><span class="sxs-lookup"><span data-stu-id="e7ac0-108">Human operational errors</span></span> 
- <span data-ttu-id="e7ac0-109">악의적인 해커 및 불만 가진된 직원</span><span class="sxs-lookup"><span data-stu-id="e7ac0-109">Malicious hackers and disgruntled employees</span></span> 
- <span data-ttu-id="e7ac0-110">일부 데이터 손실이 발생 하는 외부 서비스에 사고</span><span class="sxs-lookup"><span data-stu-id="e7ac0-110">Incidents in external services that result in some loss of data</span></span> 

<span data-ttu-id="e7ac0-p102">데이터 무결성에 큰 복구 의미가 데이터 손상 문제 감소 하기 때문에 Microsoft에서는 이러한 문제가 발생, 시스템 및 않을 경우 데이터를 복구 하 게 사용할 수 있는 프로세스에서 손상을 방지 하기 위해 Office 365 보호 메커니즘에 작성 됩니다. 데이터 손상에 대해 복구를 높이 엔지니어링 릴리스 프로세스의 다양 한 단계 내 검사 및 프로세스에 존재 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-p102">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Office 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does. Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>
- <span data-ttu-id="e7ac0-113">시스템 디자인</span><span class="sxs-lookup"><span data-stu-id="e7ac0-113">System Design</span></span>
- <span data-ttu-id="e7ac0-114">코드 조직 및 구조</span><span class="sxs-lookup"><span data-stu-id="e7ac0-114">Code organization and structure</span></span> 
- <span data-ttu-id="e7ac0-115">코드 검토</span><span class="sxs-lookup"><span data-stu-id="e7ac0-115">Code review</span></span> 
- <span data-ttu-id="e7ac0-116">단위 테스트, 통합 테스트 및 시스템 테스트</span><span class="sxs-lookup"><span data-stu-id="e7ac0-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="e7ac0-117">출장 와이어 테스트/게이트</span><span class="sxs-lookup"><span data-stu-id="e7ac0-117">Trip wires tests/gates</span></span> 

<span data-ttu-id="e7ac0-p103">Office 365 프로덕션 환경 내에서 데이터 센터 간의 피어 복제 모든 데이터의 라이브 복사본을 여러개 항상 되었는지 확인 합니다. 표준 이미지 및 스크립트를 사용 하 여 손실 된 서버를 복구 하 고 복제 된 데이터를 사용 하 여 고객 데이터를 복원 합니다. Microsoft은 SharePoint Online 및 내부 코드에서 기본 제공 복제를 사용 하 여 Office 365 정보 시스템 설명서 (보안 관련 설명서 포함)만의 백업을 유지 관리 가이드에 표시 되는 기본 제공 데이터 복구 검사와 프로세스를로 인해 리포지토리 도구, 소스 서비스 센터입니다. SharePoint Online에 저장 된 시스템 설명서 및 원본 서비스 센터로 시스템 및 응용 프로그램 이미지를 포함 합니다. SharePoint Online 및 원본 서비스 센터 버전 관리를 사용 하 고 거의 실시간에 복제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-p103">Within Office 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data. Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data. Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Office 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot. System documentation is stored in SharePoint Online, and Source Depot contains system and application images. Both SharePoint Online and Source Depot use versioning and are replicated in near real-time.</span></span> 