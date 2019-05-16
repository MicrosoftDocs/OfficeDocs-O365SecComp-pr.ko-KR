---
title: DLP에 대한 사용자 지정 중요한 정보 유형
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: 04/23/2019
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: DLP에 대한 사용자 지정 중요한 정보 유형의 개요를 확인합니다.
ms.openlocfilehash: 460b6d584208696011a5bcdd0b8ab00b6de207d3
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077664"
---
# <a name="custom-sensitive-information-types"></a><span data-ttu-id="96e93-103">사용자 지정 중요한 정보 유형</span><span class="sxs-lookup"><span data-stu-id="96e93-103">Custom sensitive information types</span></span>

## <a name="overview"></a><span data-ttu-id="96e93-104">개요</span><span class="sxs-lookup"><span data-stu-id="96e93-104">Overview</span></span>

<span data-ttu-id="96e93-105">Office 365에는 [데이터 손실 방지](data-loss-prevention-policies.md)(DLP) 또는 [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security)와 같이 조직에서 사용하도록 기본으로 제공되는 많은 중요한 정보 유형이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-105">Office 365 includes many built-in sensitive information types that are ready for you to use in your organization, such as for [data loss prevention](data-loss-prevention-policies.md) (DLP), or with [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security).</span></span> <span data-ttu-id="96e93-106">기본 제공되는 중요한 정보 유형은 정규 표현식(정규식) 또는 함수로 정의된 패턴을 기반으로 신용 카드 번호, 은행 계좌 번호, 여권 번호 등을 식별하고 보호하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-106">Built-in sensitive information types can help identify and protect credit card numbers, bank account numbers, passport numbers, and more, based on patterns that are defined by a regular expression (regex) or a function.</span></span> <span data-ttu-id="96e93-107">자세한 내용은 [중요한 정보 유형이 찾는 항목](what-the-sensitive-information-types-look-for.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="96e93-107">To learn more, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>

<span data-ttu-id="96e93-108">그렇지만 다른 유형의 중요한 정보, 예를 들어, 조직 고유의 형식을 사용하는 직원 ID 또는 프로젝트 번호를 식별하고 보호해야 할 경우 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="96e93-108">But what if you need to identify and protect a different type of sensitive information, such as for employee IDs or project numbers, using a format that's specific to your organization?</span></span> <span data-ttu-id="96e93-109">이를 위해 사용자 지정 중요한 정보 유형을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-109">To do this, you can create a custom sensitive information type.</span></span>

<span data-ttu-id="96e93-110">다음은 사용자 지정 중요한 정보 유형의 기본 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-110">The fundamental parts of a custom sensitive information type are:</span></span>

- <span data-ttu-id="96e93-111">**기본 패턴**: 직원 ID 번호, 프로젝트 번호 등으로, 일반적으로 정규식(RegEx)으로 식별되지만, 해당 패턴이 키워드 목록일 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-111">**Primary pattern**: employee ID numbers, project numbers, etc. This is typically identified by a regular expression (RegEx), but it can also be a list of keywords.</span></span>

- <span data-ttu-id="96e93-p103">**추가 증거**: 9자리 직원 ID 번호를 찾고 있다고 가정해 보세요. 모든 9자리 숫자가 직원 ID 번호는 아니므로 "직원", "배지", "ID"또는 추가 정규식을 기반으로 하는 기타 텍스트 패턴과 같은 키워드를 추가로 찾아볼 수 있습니다. 이 뒷받침하는 증거(_뒷받침하는_ 또는 _확증적인_ 증거라고도 함)는 콘텐츠에 있는 9자리 숫자가 실제로 직원 ID 번호일 가능성을 높입니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-p103">**Additional evidence**: Suppose you're looking for a nine-digit employee ID number. Not all nine-digit numbers are employee ID numbers, so you can look for additional text: keywords like "employee", "badge", "ID", or other text patterns based on additional regular expressions. This supporting evidence (also known as _supporting_ or _corroborative_ evidence) increases the likelihood that nine-digit number found in content is really an employee ID number.</span></span>

- <span data-ttu-id="96e93-p104">**문자 근접**: 기본 패턴과 뒷받침하는 증거가 서로 가까울수록 검색된 콘텐츠가 원하는 것일 확률이 높습니다. 다음 다이어그램과 같이 기본 패턴과 뒷받침하는 증거(_근접 범위_라고도 함) 사이의 문자 거리를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-p104">**Character proximity**: It makes sense that the closer the primary pattern and the supporting evidence are to each other, the more likely the detected content is going to be what you're looking for. You can specify the character distance between the primary pattern and the supporting evidence (also known as the _proximity window_) as shown in the following diagram:</span></span>

    ![증거 및 근접 범위 다이어그램](media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)

- <span data-ttu-id="96e93-p105">**신뢰 수준**: 가지고 있는 증거를 뒷받침할수록, 찾고 있는 중요한 정보가 일치하는 확률이 높아집니다. 더 많은 증거를 사용하여 검색된 일치 항목에 대해 높은 수준의 신뢰도를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-p105">**Confidence level**: The more supporting evidence you have, the higher the likelihood that a match contains the sensitive information you're looking for. You can assign higher levels of confidence for matches that are detected by using more evidence.</span></span>

  <span data-ttu-id="96e93-p106">결과가 충족되면 패턴은 해당 개수 및 신뢰도를 반환합니다. 이 결과를 DLP 정책의 조건에서 사용할 수 있습니다. 중요한 정보 유형을 검색하는 조건을 DLP 정책에 추가하면 다음 다이어그램에 표시된 것처럼 개수 및 신뢰도를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-p106">When satisfied, a pattern returns a count and confidence level, which you can use in the conditions in your DLP policies. When you add a condition for detecting a sensitive information type to a DLP policy, you can edit the count and confidence level as shown in the following diagram:</span></span>

    ![인스턴스 개수 및 일치 정확도 옵션](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)

## <a name="creating-custom-sensitive-information-types"></a><span data-ttu-id="96e93-123">사용자 지정 중요한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="96e93-123">Creating custom sensitive information types</span></span>

<span data-ttu-id="96e93-124">보안 및 준수 센터에서 사용자 지정 중요한 정보 유형을 만들려면 몇 가지 옵션 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-124">To create custom sensitive information types in the Security & Compliance Center, you can choose from several options:</span></span>

- <span data-ttu-id="96e93-125">**EDM 사용**(신규!) EDM(Exact Data Match) 기반 분류를 사용하여 사용자 정의 중요한 정보 유형을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-125">**Use EDM** (NEW!) You can set up custom sensitive information types using Exact Data Match (EDM)-based classification.</span></span> <span data-ttu-id="96e93-126">이 방법을 사용하면 주기적으로 새로 고칠 수 있는 보안 데이터베이스를 사용하여 동적인 중요한 정보 유형을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-126">This method enables you to create a dynamic sensitive information type using a secure database that you can refresh periodically.</span></span> <span data-ttu-id="96e93-127">[정확한 데이터 매치(미리 보기)를 사용한 사용자 지정 중요한 정보 유형 만들기](create-custom-sensitive-info-type-edm.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="96e93-127">See [Create a custom sensitive information type with Exact Data Match based classification (Preview)](create-custom-sensitive-info-type-edm.md).</span></span>

- <span data-ttu-id="96e93-128">**PowerShell을 사용** PowerShell을 사용하여 사용자 지정 중요한 정보 유형을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-128">**Use PowerShell** You can set up custom sensitive information types using PowerShell.</span></span> <span data-ttu-id="96e93-129">이 방법은 UI를 사용하는 것보다 복잡하지만 더 다양한 구성 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-129">Although this method is more complex than using the UI, you have more configuration options.</span></span> <span data-ttu-id="96e93-130">[보안 및 준수 센터 PowerShell에서 사용자 지정 중요한 정보 유형 만들기](create-a-custom-sensitive-information-type-in-scc-powershell.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="96e93-130">See [Create a custom sensitive information type in Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span></span>

- <span data-ttu-id="96e93-131">**UI 사용** 보안 및 준수 센터 UI를 사용하여 사용자 지정 중요한 정보 유형을 설정할 수 있습니나.</span><span class="sxs-lookup"><span data-stu-id="96e93-131">**Use the UI** You can set up a custom sensitive information type using the Security & Compliance Center UI.</span></span> <span data-ttu-id="96e93-132">이 방법을 사용하면 정규식, 키워드 및 키워드 사전을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e93-132">With this method, you can use regular expressions, keywords, and keyword dictionaries.</span></span> <span data-ttu-id="96e93-133">자세한 내용은 [사용자 지정 중요한 정보 유형 만들기](create-a-custom-sensitive-information-type.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="96e93-133">To learn more, see [Create a custom sensitive information type](create-a-custom-sensitive-information-type.md).</span></span>



