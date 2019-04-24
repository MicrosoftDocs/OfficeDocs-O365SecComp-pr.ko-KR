---
title: EU 여권 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: 이 항목에서는 DLP (데이터 손실 방지) 정책이 EU (유럽 여권 번호) 중요 한 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: 3ab92e87607f41cffa8c15f1179a4eef5369cb29
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256826"
---
# <a name="eu-passport-number"></a><span data-ttu-id="9b1d7-104">EU 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-104">EU Passport Number</span></span>

<span data-ttu-id="9b1d7-105">이 항목에서는 DLP (데이터 손실 방지) 정책이 EU (유럽 여권 번호) 중요 한 정보 유형을 검색할 때 찾는 항목을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="9b1d7-106">이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="9b1d7-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="9b1d7-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-108">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-108">Format</span></span>

<span data-ttu-id="9b1d7-109">1 개의 문자 다음에 선택적 공백, 일곱 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-110">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-110">Pattern</span></span>

<span data-ttu-id="9b1d7-111">한 글자, 일곱 자리 및 한 가지 공백 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="9b1d7-112">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="9b1d7-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="9b1d7-113">1 개의 공백 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="9b1d7-113">One space (optional)</span></span>
    
- <span data-ttu-id="9b1d7-114">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b1d7-115">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-115">Checksum</span></span>

<span data-ttu-id="9b1d7-116">해당 없음</span><span class="sxs-lookup"><span data-stu-id="9b1d7-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-117">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-117">Definition</span></span>

<span data-ttu-id="9b1d7-118">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-119">정규식이 해당 `Regex_austria_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-120">from `Keywords_austria_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-121">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-121">Keywords</span></span>

<span data-ttu-id="9b1d7-122">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-122"></span></span>
|<span data-ttu-id="9b1d7-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-124">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-124">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-125">오스트리아 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-125">austrian passport number</span></span>  <br/> <span data-ttu-id="9b1d7-126">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-126">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="9b1d7-127">reisepass</span></span>  <br/> <span data-ttu-id="9b1d7-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="9b1d7-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="9b1d7-129">벨기에</span><span class="sxs-lookup"><span data-stu-id="9b1d7-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-130">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-130">Format</span></span>

<span data-ttu-id="9b1d7-131">공백 또는 구분 기호가 없는 2 개 문자 다음에 6 자리 숫자 사용</span><span class="sxs-lookup"><span data-stu-id="9b1d7-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-132">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-132">Pattern</span></span>

<span data-ttu-id="9b1d7-133">2 개 문자 및 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-134">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-134">Checksum</span></span>

<span data-ttu-id="9b1d7-135">해당 없음</span><span class="sxs-lookup"><span data-stu-id="9b1d7-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-136">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-136">Definition</span></span>

<span data-ttu-id="9b1d7-137">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-138">정규식이 해당 `Regex_belgium_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-139">from `Keywords_belgium_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-140">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-140">Keywords</span></span>

<span data-ttu-id="9b1d7-141">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-141"></span></span>
|<span data-ttu-id="9b1d7-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-143">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-143">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-144">벨기에 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-144">belgian passport number</span></span>  <br/> <span data-ttu-id="9b1d7-145">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-145">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-146">고 대/ort</span><span class="sxs-lookup"><span data-stu-id="9b1d7-146">paspoort</span></span>  <br/> <span data-ttu-id="9b1d7-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="9b1d7-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="9b1d7-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="9b1d7-148">reisepass kein</span></span>  <br/> <span data-ttu-id="9b1d7-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="9b1d7-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="9b1d7-150">불가리아</span><span class="sxs-lookup"><span data-stu-id="9b1d7-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-151">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-151">Format</span></span>

<span data-ttu-id="9b1d7-152">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-153">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-153">Pattern</span></span>

 <span data-ttu-id="9b1d7-154">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-155">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-155">Checksum</span></span>

<span data-ttu-id="9b1d7-156">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-157">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-157">Definition</span></span>

<span data-ttu-id="9b1d7-158">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-159">정규식이 해당 `Regex_bulgaria_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-160">from `Keywords_bulgaria_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-161">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-161">Keywords</span></span>

<span data-ttu-id="9b1d7-162">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-162"></span></span>
|<span data-ttu-id="9b1d7-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-164">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-164">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-165">불가리아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="9b1d7-166">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-166">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="9b1d7-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="9b1d7-168">크로아티아</span><span class="sxs-lookup"><span data-stu-id="9b1d7-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-169">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-169">Format</span></span>

<span data-ttu-id="9b1d7-170">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-171">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-171">Pattern</span></span>

 <span data-ttu-id="9b1d7-172">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-173">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-173">Checksum</span></span>

<span data-ttu-id="9b1d7-174">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-175">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-175">Definition</span></span>

<span data-ttu-id="9b1d7-176">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-177">정규식이 해당 `Regex_croatia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-178">from `Keywords_croatia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-179">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-179">Keywords</span></span>

<span data-ttu-id="9b1d7-180">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-180"></span></span>
|<span data-ttu-id="9b1d7-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-182">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-182">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-183">크로아티아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-183">croatian passport number</span></span>  <br/> <span data-ttu-id="9b1d7-184">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-184">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="9b1d7-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="9b1d7-186">키프로스</span><span class="sxs-lookup"><span data-stu-id="9b1d7-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-187">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-187">Format</span></span>

<span data-ttu-id="9b1d7-188">공백 또는 구분 기호가 없는 1 개 문자 다음에 6-8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-189">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-189">Pattern</span></span>

<span data-ttu-id="9b1d7-190">한 문자 다음에 6 ~ 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-191">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-191">Checksum</span></span>

<span data-ttu-id="9b1d7-192">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-193">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-193">Definition</span></span>

<span data-ttu-id="9b1d7-194">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-195">정규식이 해당 `Regex_cyprus_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-196">from `Keywords_cyprus_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-197">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-197">Keywords</span></span>

<span data-ttu-id="9b1d7-198">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-198"></span></span>
|<span data-ttu-id="9b1d7-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-200">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-200">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-201">키프로스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="9b1d7-202">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-202">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="9b1d7-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="9b1d7-204">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="9b1d7-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-205">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-205">Format</span></span>

<span data-ttu-id="9b1d7-206">공백이 나 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-207">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-207">Pattern</span></span>

<span data-ttu-id="9b1d7-208">공백이 나 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-209">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-209">Checksum</span></span>

<span data-ttu-id="9b1d7-210">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-211">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-211">Definition</span></span>

<span data-ttu-id="9b1d7-212">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-213">정규식이 해당 `Regex_czech_republic_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-214">from `Keywords_czech_republic_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-215">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-215">Keywords</span></span>

<span data-ttu-id="9b1d7-216">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-216"></span></span>
|<span data-ttu-id="9b1d7-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-218">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-218">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-219">체코어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-219">czech passport number</span></span>  <br/> <span data-ttu-id="9b1d7-220">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-220">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-221">cestovní pas</span><span class="sxs-lookup"><span data-stu-id="9b1d7-221">cestovní pas</span></span>  <br/> <span data-ttu-id="9b1d7-222">pas</span><span class="sxs-lookup"><span data-stu-id="9b1d7-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="9b1d7-223">덴마크</span><span class="sxs-lookup"><span data-stu-id="9b1d7-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-224">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-224">Format</span></span>

<span data-ttu-id="9b1d7-225">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-226">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-226">Pattern</span></span>

 <span data-ttu-id="9b1d7-227">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-228">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-228">Checksum</span></span>

<span data-ttu-id="9b1d7-229">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-230">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-230">Definition</span></span>

<span data-ttu-id="9b1d7-231">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-232">정규식이 해당 `Regex_denmark_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-233">from `Keywords_denmark_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-234">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-234">Keywords</span></span>

<span data-ttu-id="9b1d7-235">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-235"></span></span>
|<span data-ttu-id="9b1d7-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-237">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-237">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-238">덴마크어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-238">danish passport number</span></span>  <br/> <span data-ttu-id="9b1d7-239">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-239">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-240">pas</span><span class="sxs-lookup"><span data-stu-id="9b1d7-240">pas</span></span>  <br/> <span data-ttu-id="9b1d7-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="9b1d7-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="9b1d7-242">에스토니아</span><span class="sxs-lookup"><span data-stu-id="9b1d7-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-243">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-243">Format</span></span>

<span data-ttu-id="9b1d7-244">공백 또는 구분 기호가 없는 1 개 문자 다음에 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-245">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-245">Pattern</span></span>

<span data-ttu-id="9b1d7-246">1 개의 문자 다음에 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-247">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-247">Checksum</span></span>

<span data-ttu-id="9b1d7-248">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-249">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-249">Definition</span></span>

<span data-ttu-id="9b1d7-250">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-251">정규식이 해당 `Regex_estonia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-252">from `Keywords_estonia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-253">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-253">Keywords</span></span>

<span data-ttu-id="9b1d7-254">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-254"></span></span>
|<span data-ttu-id="9b1d7-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-256">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-256">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-257">에스토니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-257">estonian passport number</span></span>  <br/> <span data-ttu-id="9b1d7-258">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-258">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-259">eesti kodaniku pass</span><span class="sxs-lookup"><span data-stu-id="9b1d7-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="9b1d7-260">핀란드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-260">Finland</span></span>

<span data-ttu-id="9b1d7-261">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"핀란드 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="9b1d7-262">프랑스</span><span class="sxs-lookup"><span data-stu-id="9b1d7-262">France</span></span>

<span data-ttu-id="9b1d7-263">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"프랑스 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="9b1d7-264">독일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-264">Germany</span></span>

<span data-ttu-id="9b1d7-265">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="9b1d7-266">그리스</span><span class="sxs-lookup"><span data-stu-id="9b1d7-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-267">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-267">Format</span></span>

<span data-ttu-id="9b1d7-268">공백 또는 구분 기호가 없는 7 자리, 두 문자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-269">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-269">Pattern</span></span>

<span data-ttu-id="9b1d7-270">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-271">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-271">Checksum</span></span>

<span data-ttu-id="9b1d7-272">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-273">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-273">Definition</span></span>

<span data-ttu-id="9b1d7-274">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-275">정규식이 해당 `Regex_greece_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-276">from `Keywords_greece_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-277">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-277">Keywords</span></span>

<span data-ttu-id="9b1d7-278">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-278"></span></span>
|<span data-ttu-id="9b1d7-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-280">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-280">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-281">그리스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-281">greek passport number</span></span>  <br/> <span data-ttu-id="9b1d7-282">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-282">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="9b1d7-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="9b1d7-284">헝가리</span><span class="sxs-lookup"><span data-stu-id="9b1d7-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-285">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-285">Format</span></span>

<span data-ttu-id="9b1d7-286">공백 또는 구분 기호가 없는 2 개 문자 및 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-287">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-287">Pattern</span></span>

<span data-ttu-id="9b1d7-288">2 개의 문자 다음에 6 개 또는 7 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-289">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-289">Checksum</span></span>

<span data-ttu-id="9b1d7-290">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-291">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-291">Definition</span></span>

<span data-ttu-id="9b1d7-292">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-293">정규식이 해당 `Regex_hungary_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-294">from `Keywords_hungary_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-295">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-295">Keywords</span></span>

<span data-ttu-id="9b1d7-296">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-296"></span></span>
|<span data-ttu-id="9b1d7-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-298">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-298">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-299">헝가리어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="9b1d7-300">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-300">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="9b1d7-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="9b1d7-302">Ireland</span><span class="sxs-lookup"><span data-stu-id="9b1d7-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-303">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-303">Format</span></span>

<span data-ttu-id="9b1d7-304">공백이 나 구분 기호가 없는 두 개의 문자 또는 숫자와 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-305">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-305">Pattern</span></span>

<span data-ttu-id="9b1d7-306">두 개의 문자 또는 숫자와 7 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="9b1d7-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="9b1d7-307">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="9b1d7-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="9b1d7-308">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b1d7-309">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-309">Checksum</span></span>

<span data-ttu-id="9b1d7-310">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-311">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-311">Definition</span></span>

<span data-ttu-id="9b1d7-312">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-313">정규식이 해당 `Regex_ireland_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-314">from `Keywords_ireland_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-315">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-315">Keywords</span></span>

<span data-ttu-id="9b1d7-316">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-316"></span></span>
|<span data-ttu-id="9b1d7-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-318">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-318">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-319">아일랜드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-319">irish passport number</span></span>  <br/> <span data-ttu-id="9b1d7-320">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-320">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-321">pas</span><span class="sxs-lookup"><span data-stu-id="9b1d7-321">pas</span></span>  <br/> <span data-ttu-id="9b1d7-322">여권</span><span class="sxs-lookup"><span data-stu-id="9b1d7-322">passport</span></span>  <br/> <span data-ttu-id="9b1d7-323">포트</span><span class="sxs-lookup"><span data-stu-id="9b1d7-323">passeport</span></span>  <br/> <span data-ttu-id="9b1d7-324">포트 numero</span><span class="sxs-lookup"><span data-stu-id="9b1d7-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="9b1d7-325">이탈리아</span><span class="sxs-lookup"><span data-stu-id="9b1d7-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-326">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-326">Format</span></span>

<span data-ttu-id="9b1d7-327">공백이 나 구분 기호가 없는 두 개의 문자 또는 숫자와 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-328">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-328">Pattern</span></span>

<span data-ttu-id="9b1d7-329">두 개의 문자 또는 숫자와 7 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="9b1d7-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="9b1d7-330">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="9b1d7-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="9b1d7-331">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b1d7-332">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-332">Checksum</span></span>

<span data-ttu-id="9b1d7-333">해당 없음</span><span class="sxs-lookup"><span data-stu-id="9b1d7-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-334">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-334">Definition</span></span>

<span data-ttu-id="9b1d7-335">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-336">정규식이 해당 `Regex_italy_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-337">from `Keywords_italy_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-338">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-338">Keywords</span></span>

<span data-ttu-id="9b1d7-339">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-339"></span></span>
|<span data-ttu-id="9b1d7-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-341">이탈리아 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-341">italian passport number</span></span>  <br/> <span data-ttu-id="9b1d7-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="9b1d7-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="9b1d7-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="9b1d7-343">passaporto</span></span>  <br/> <span data-ttu-id="9b1d7-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="9b1d7-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="9b1d7-345">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-345">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-346">italiana passaporto numero</span><span class="sxs-lookup"><span data-stu-id="9b1d7-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="9b1d7-347">passaporto numero</span><span class="sxs-lookup"><span data-stu-id="9b1d7-347">passaporto numero</span></span>  <br/> <span data-ttu-id="9b1d7-348">numéro) 포트 italien</span><span class="sxs-lookup"><span data-stu-id="9b1d7-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="9b1d7-349">numéro (고) 포트</span><span class="sxs-lookup"><span data-stu-id="9b1d7-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="9b1d7-350">라트비아</span><span class="sxs-lookup"><span data-stu-id="9b1d7-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-351">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-351">Format</span></span>

<span data-ttu-id="9b1d7-352">공백이 나 구분 기호가 없는 두 개의 문자 또는 숫자와 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-353">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-353">Pattern</span></span>

<span data-ttu-id="9b1d7-354">두 개의 문자 또는 숫자와 7 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="9b1d7-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="9b1d7-355">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="9b1d7-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="9b1d7-356">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b1d7-357">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-357">Checksum</span></span>

<span data-ttu-id="9b1d7-358">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-359">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-359">Definition</span></span>

<span data-ttu-id="9b1d7-360">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-361">정규식이 해당 `Regex_latvia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-362">from `Keywords_latvia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-363">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-363">Keywords</span></span>

<span data-ttu-id="9b1d7-364">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-364"></span></span>
|<span data-ttu-id="9b1d7-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-366">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-366">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-367">라트비아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-367">latvian passport number</span></span>  <br/> <span data-ttu-id="9b1d7-368">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-368">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="9b1d7-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="9b1d7-370">리투아니아</span><span class="sxs-lookup"><span data-stu-id="9b1d7-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-371">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-371">Format</span></span>

<span data-ttu-id="9b1d7-372">공백이 나 구분 기호가 없는 8 자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-373">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-373">Pattern</span></span>

<span data-ttu-id="9b1d7-374">8 자리 숫자 또는 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="9b1d7-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-375">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-375">Checksum</span></span>

<span data-ttu-id="9b1d7-376">해당 없음</span><span class="sxs-lookup"><span data-stu-id="9b1d7-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-377">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-377">Definition</span></span>

<span data-ttu-id="9b1d7-378">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-379">정규식이 해당 `Regex_lithuania_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-380">from `Keywords_lithuania_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-381">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-381">Keywords</span></span>

<span data-ttu-id="9b1d7-382">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-382"></span></span>
|<span data-ttu-id="9b1d7-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-384">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-384">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-385">lithunian 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="9b1d7-386">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-386">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-387">numeris</span><span class="sxs-lookup"><span data-stu-id="9b1d7-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="9b1d7-388">셈</span><span class="sxs-lookup"><span data-stu-id="9b1d7-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-389">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-389">Format</span></span>

<span data-ttu-id="9b1d7-390">공백이 나 구분 기호가 없는 8 자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-391">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-391">Pattern</span></span>

<span data-ttu-id="9b1d7-392">8 자리 숫자 또는 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="9b1d7-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-393">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-393">Checksum</span></span>

<span data-ttu-id="9b1d7-394">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-395">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-395">Definition</span></span>

<span data-ttu-id="9b1d7-396">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-397">정규식이 해당 `Regex_nation_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-398">from `Keywords_nation_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-399">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-399">Keywords</span></span>

<span data-ttu-id="9b1d7-400">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-400"></span></span>
|<span data-ttu-id="9b1d7-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-402">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-402">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-403">라트비아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-403">latvian passport number</span></span>  <br/> <span data-ttu-id="9b1d7-404">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-404">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="9b1d7-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="9b1d7-406">몰타</span><span class="sxs-lookup"><span data-stu-id="9b1d7-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-407">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-407">Format</span></span>

<span data-ttu-id="9b1d7-408">공백이 나 구분 기호 없이 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-409">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-409">Pattern</span></span>

 <span data-ttu-id="9b1d7-410">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-411">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-411">Checksum</span></span>

<span data-ttu-id="9b1d7-412">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-413">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-413">Definition</span></span>

<span data-ttu-id="9b1d7-414">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-415">정규식이 해당 `Regex_malta_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-416">from `Keywords_malta_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-417">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-417">Keywords</span></span>

<span data-ttu-id="9b1d7-418">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-418"></span></span>
|<span data-ttu-id="9b1d7-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-420">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-420">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-421">몰타어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-421">maltese passport number</span></span>  <br/> <span data-ttu-id="9b1d7-422">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-422">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-423">numru-passaport</span><span class="sxs-lookup"><span data-stu-id="9b1d7-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="9b1d7-424">네덜란드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-425">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-425">Format</span></span>

<span data-ttu-id="9b1d7-426">공백이 나 구분 기호가 없는 9 개의 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-427">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-427">Pattern</span></span>

<span data-ttu-id="9b1d7-428">9 개의 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-429">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-429">Checksum</span></span>

<span data-ttu-id="9b1d7-430">해당 없음</span><span class="sxs-lookup"><span data-stu-id="9b1d7-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-431">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-431">Definition</span></span>

<span data-ttu-id="9b1d7-432">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-433">정규식이 해당 `Regex_netherlands_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-434">from `Keywords_netherlands_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-435">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-435">Keywords</span></span>

<span data-ttu-id="9b1d7-436">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-436"></span></span>
|<span data-ttu-id="9b1d7-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-438">네덜란드어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-438">dutch passport number</span></span>  <br/> <span data-ttu-id="9b1d7-439">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-439">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-440">네덜란드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="9b1d7-441">nederlanden, nummer ort</span><span class="sxs-lookup"><span data-stu-id="9b1d7-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="9b1d7-442">고 대/ort</span><span class="sxs-lookup"><span data-stu-id="9b1d7-442">paspoort</span></span>  <br/> <span data-ttu-id="9b1d7-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="9b1d7-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="9b1d7-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="9b1d7-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="9b1d7-445">폴란드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-445">Poland</span></span>

<span data-ttu-id="9b1d7-446">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"폴란드 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="9b1d7-447">포르투갈</span><span class="sxs-lookup"><span data-stu-id="9b1d7-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-448">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-448">Format</span></span>

<span data-ttu-id="9b1d7-449">공백 또는 구분 기호가 없는 한 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-450">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-450">Pattern</span></span>

<span data-ttu-id="9b1d7-451">1 개의 문자 다음에 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="9b1d7-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="9b1d7-452">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="9b1d7-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="9b1d7-453">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b1d7-454">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-454">Checksum</span></span>

<span data-ttu-id="9b1d7-455">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-456">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-456">Definition</span></span>

<span data-ttu-id="9b1d7-457">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-458">정규식이 해당 `Regex_portugal_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-459">from `Keywords_portugal_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-460">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-460">Keywords</span></span>

<span data-ttu-id="9b1d7-461">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-461"></span></span>
|<span data-ttu-id="9b1d7-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-463">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-463">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-464">포르투갈어 passport 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="9b1d7-465">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-465">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-466">número do passaporte</span><span class="sxs-lookup"><span data-stu-id="9b1d7-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="9b1d7-467">루마니아</span><span class="sxs-lookup"><span data-stu-id="9b1d7-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-468">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-468">Format</span></span>

<span data-ttu-id="9b1d7-469">공백과 구분 기호를 사용 하지 않고 8 또는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-470">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-470">Pattern</span></span>

<span data-ttu-id="9b1d7-471">8 또는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-472">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-472">Checksum</span></span>

<span data-ttu-id="9b1d7-473">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-474">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-474">Definition</span></span>

<span data-ttu-id="9b1d7-475">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-476">정규식이 해당 `Regex_romania_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-477">from `Keywords_romania_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-478">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-478">Keywords</span></span>

<span data-ttu-id="9b1d7-479">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-479"></span></span>
|<span data-ttu-id="9b1d7-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-481">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-481">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-482">루마니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-482">romanian passport number</span></span>  <br/> <span data-ttu-id="9b1d7-483">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-483">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="9b1d7-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="9b1d7-485">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="9b1d7-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-486">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-486">Format</span></span>

<span data-ttu-id="9b1d7-487">공백 또는 구분 기호가 없는 한 자리 숫자 또는 문자 다음에 일곱 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-488">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-488">Pattern</span></span>

<span data-ttu-id="9b1d7-489">1 자리 숫자 또는 문자 (대/소문자 구분 안 함)와 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9b1d7-490">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-490">Checksum</span></span>

<span data-ttu-id="9b1d7-491">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-492">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-492">Definition</span></span>

<span data-ttu-id="9b1d7-493">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-494">정규식이 해당 `Regex_slovakia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-495">from `Keywords_slovakia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-496">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-496">Keywords</span></span>

<span data-ttu-id="9b1d7-497">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-497"></span></span>
|<span data-ttu-id="9b1d7-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-499">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-499">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-500">슬로바키아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="9b1d7-501">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-501">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-502">číslo (u)</span><span class="sxs-lookup"><span data-stu-id="9b1d7-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="9b1d7-503">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="9b1d7-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-504">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-504">Format</span></span>

<span data-ttu-id="9b1d7-505">공백 또는 구분 기호가 없는 7 자리, 두 문자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-506">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-506">Pattern</span></span>

<span data-ttu-id="9b1d7-507">2 개 문자와 7 자리 숫자를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="9b1d7-508">"P" 문자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-508">The letter "P"</span></span>
    
- <span data-ttu-id="9b1d7-509">대문자 1 개</span><span class="sxs-lookup"><span data-stu-id="9b1d7-509">One uppercase letter</span></span>
    
- <span data-ttu-id="9b1d7-510">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b1d7-511">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-511">Checksum</span></span>

<span data-ttu-id="9b1d7-512">아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-513">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-513">Definition</span></span>

<span data-ttu-id="9b1d7-514">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-515">정규식이 해당 `Regex_slovenia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-516">from `Keywords_slovenia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-517">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-517">Keywords</span></span>

<span data-ttu-id="9b1d7-518">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-518"></span></span>
|<span data-ttu-id="9b1d7-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-520">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-520">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-521">슬로베니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9b1d7-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="9b1d7-522">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-522">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-523">številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="9b1d7-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="9b1d7-524">스페인</span><span class="sxs-lookup"><span data-stu-id="9b1d7-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="9b1d7-525">형식일</span><span class="sxs-lookup"><span data-stu-id="9b1d7-525">Format</span></span>

<span data-ttu-id="9b1d7-526">공백이 나 구분 기호가 없는 문자 및 숫자의 8 자리 또는 9 자 조합</span><span class="sxs-lookup"><span data-stu-id="9b1d7-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b1d7-527">패턴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-527">Pattern</span></span>

<span data-ttu-id="9b1d7-528">문자와 숫자의 8 자리 또는 9 자리 조합:</span><span class="sxs-lookup"><span data-stu-id="9b1d7-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="9b1d7-529">두 자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="9b1d7-530">1 자리 숫자 또는 문자 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="9b1d7-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="9b1d7-531">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9b1d7-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b1d7-532">제외</span><span class="sxs-lookup"><span data-stu-id="9b1d7-532">Checksum</span></span>

<span data-ttu-id="9b1d7-533">해당 없음</span><span class="sxs-lookup"><span data-stu-id="9b1d7-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b1d7-534">정의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-534">Definition</span></span>

<span data-ttu-id="9b1d7-535">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b1d7-536">정규식이 해당 `Regex_spain_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b1d7-537">from `Keywords_spain_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b1d7-538">키워드</span><span class="sxs-lookup"><span data-stu-id="9b1d7-538">Keywords</span></span>

<span data-ttu-id="9b1d7-539">| |</span><span class="sxs-lookup"><span data-stu-id="9b1d7-539"></span></span>
|<span data-ttu-id="9b1d7-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9b1d7-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9b1d7-541">여권</span><span class="sxs-lookup"><span data-stu-id="9b1d7-541">passport</span></span>  <br/> <span data-ttu-id="9b1d7-542">스페인 여권</span><span class="sxs-lookup"><span data-stu-id="9b1d7-542">spain passport</span></span>  <br/> <span data-ttu-id="9b1d7-543">passport 책</span><span class="sxs-lookup"><span data-stu-id="9b1d7-543">passport book</span></span>  <br/> <span data-ttu-id="9b1d7-544">passport number</span><span class="sxs-lookup"><span data-stu-id="9b1d7-544">passport number</span></span>  <br/> <span data-ttu-id="9b1d7-545">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9b1d7-545">passport no</span></span>  <br/> <span data-ttu-id="9b1d7-546">pasaporte</span><span class="sxs-lookup"><span data-stu-id="9b1d7-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="9b1d7-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="9b1d7-547">número pasaporte</span></span>  <br/> <span data-ttu-id="9b1d7-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="9b1d7-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="9b1d7-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="9b1d7-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="9b1d7-550">스웨덴</span><span class="sxs-lookup"><span data-stu-id="9b1d7-550">Sweden</span></span>

<span data-ttu-id="9b1d7-551">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"스웨덴 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="9b1d7-552">영국의</span><span class="sxs-lookup"><span data-stu-id="9b1d7-552">UK</span></span>

<span data-ttu-id="9b1d7-553">자세한 내용은 "미국/영국" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="9b1d7-554">[중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)Passport 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9b1d7-555">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9b1d7-555">See also</span></span>

[<span data-ttu-id="9b1d7-556">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="9b1d7-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

