---
title: Office 365 Cloud App security에 대 한 보안 정책 참조 정보
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aef6c88f-7f47-40ef-9503-2b400e3bc6fd
description: Office 365 활동 정책 및 변칙 검색 정책에 대 한 도움말을 볼 수 있습니다.
ms.openlocfilehash: db44b6cbf5b8c2783cba9862107120d2c33c1559
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264630"
---
# <a name="security-policy-reference-information-for-office-365-cloud-app-security"></a><span data-ttu-id="561a3-103">Office 365 Cloud App security에 대 한 보안 정책 참조 정보</span><span class="sxs-lookup"><span data-stu-id="561a3-103">Security policy reference information for Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="561a3-104">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="561a3-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="561a3-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="561a3-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="561a3-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="561a3-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="561a3-107">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="561a3-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="561a3-108">평가 시작</span><span class="sxs-lookup"><span data-stu-id="561a3-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="561a3-109">계획 시작</span><span class="sxs-lookup"><span data-stu-id="561a3-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="561a3-110">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="561a3-110">You are here!</span></span>  <br/> [<span data-ttu-id="561a3-111">다음 단계</span><span class="sxs-lookup"><span data-stu-id="561a3-111">Next step</span></span>](review-office-365-cas-alerts.md) <br/> |[<span data-ttu-id="561a3-112">활용 시작</span><span class="sxs-lookup"><span data-stu-id="561a3-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="561a3-113">Office 365 Cloud App Security를 사용 하 여 전역 관리자 또는 보안 관리자 인 경우 조직에 대해 두 가지 유형의 정책을 정의 하거나 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="561a3-113">With Office 365 Cloud App Security, if you are a global administrator or security administrator, you can define or edit two kinds of policies for your organization:</span></span>
  
- <span data-ttu-id="561a3-114">정의한 **[작업 정책](activity-policies-and-alerts.md)**</span><span class="sxs-lookup"><span data-stu-id="561a3-114">**[Activity policies](activity-policies-and-alerts.md)** that you define.</span></span> <span data-ttu-id="561a3-115">이러한 정책은 조직의 일반적인 기능 외 다른 지역/국가에서의 관리자 자격 증명을 사용 하 여 로그인을 시도 하는 사용자, 한 시간 내에 사용자에 대 한 로그인 시도 횟수가 너무 많은 경우와 같이 의심 스러운 것으로 정의 하는 작업을 기반으로 합니다. .</span><span class="sxs-lookup"><span data-stu-id="561a3-115">These policies are based on activities that you define as suspicious, such as users attempting to sign in with admin credentials in other regions/countries outside what's normal for your organization, or an extreme number of sign-in attempts for a user within an hour.</span></span> <span data-ttu-id="561a3-116">자세한 내용은 [Office 365 Cloud App Security의 활동 정책 및 경고](activity-policies-and-alerts.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="561a3-116">To learn more, see [Activity policies and alerts in Office 365 Cloud App Security](activity-policies-and-alerts.md).</span></span>
    
- <span data-ttu-id="561a3-117">Office 365 Cloud App Security를 사용 하 여 "외부에서" 사용할 수 있는 **[변칙 검색 정책](anomaly-detection-policies-in-ocas.md)**</span><span class="sxs-lookup"><span data-stu-id="561a3-117">**[Anomaly detection policies](anomaly-detection-policies-in-ocas.md)** that are available "out of the box" with Office 365 Cloud App Security.</span></span> <span data-ttu-id="561a3-118">이러한 정책은 의심 스러운 활동을 검색 하는 자동 알고리즘을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="561a3-118">These policies are based on automatic algorithms that detect suspicious activity.</span></span> <span data-ttu-id="561a3-119">이러한 기본 정책은 예외를 보고 자동으로 경고를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="561a3-119">These default policies watch for anomalies and trigger alerts automatically.</span></span> <span data-ttu-id="561a3-120">자세한 내용은 [Office 365 Cloud App Security의 변칙 검색 정책](anomaly-detection-policies-in-ocas.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="561a3-120">To learn more, see [Anomaly detection policies in Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md).</span></span>
    

