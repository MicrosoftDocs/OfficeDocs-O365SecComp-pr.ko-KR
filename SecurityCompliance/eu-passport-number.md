---
title: EU 여권 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: 이 항목에서는 DLP (데이터 손실 방지) 정책이 EU (유럽 여권 번호) 중요 한 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: fa3be04dec0f71a2568e046abd6b0af3e20181c5
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152970"
---
# <a name="eu-passport-number"></a><span data-ttu-id="b0140-104">EU 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-104">EU Passport Number</span></span>

<span data-ttu-id="b0140-105">이 항목에서는 DLP (데이터 손실 방지) 정책이 EU (유럽 여권 번호) 중요 한 정보 유형을 검색할 때 찾는 항목을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="b0140-106">이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="b0140-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="b0140-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="b0140-108">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-108">Format</span></span>

<span data-ttu-id="b0140-109">1 개의 문자 다음에 선택적 공백, 일곱 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-110">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-110">Pattern</span></span>

<span data-ttu-id="b0140-111">한 글자, 일곱 자리 및 한 가지 공백 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="b0140-112">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="b0140-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="b0140-113">1 개의 공백 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="b0140-113">One space (optional)</span></span>
    
- <span data-ttu-id="b0140-114">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0140-115">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-115">Checksum</span></span>

<span data-ttu-id="b0140-116">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="b0140-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-117">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-117">Definition</span></span>

<span data-ttu-id="b0140-118">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-119">정규식이 해당 `Regex_austria_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-120">From `Keywords_austria_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-121">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-121">Keywords</span></span>

<span data-ttu-id="b0140-122">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-122"></span></span>
|<span data-ttu-id="b0140-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-124">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-124">passport number</span></span>  <br/> <span data-ttu-id="b0140-125">오스트리아 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-125">austrian passport number</span></span>  <br/> <span data-ttu-id="b0140-126">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-126">passport no</span></span>  <br/> <span data-ttu-id="b0140-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="b0140-127">reisepass</span></span>  <br/> <span data-ttu-id="b0140-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="b0140-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="b0140-129">벨기에</span><span class="sxs-lookup"><span data-stu-id="b0140-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="b0140-130">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-130">Format</span></span>

<span data-ttu-id="b0140-131">공백 또는 구분 기호가 없는 2 개 문자 다음에 6 자리 숫자 사용</span><span class="sxs-lookup"><span data-stu-id="b0140-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-132">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-132">Pattern</span></span>

<span data-ttu-id="b0140-133">2 개 문자 및 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0140-134">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-134">Checksum</span></span>

<span data-ttu-id="b0140-135">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="b0140-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-136">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-136">Definition</span></span>

<span data-ttu-id="b0140-137">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-138">정규식이 해당 `Regex_belgium_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-139">From `Keywords_belgium_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-140">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-140">Keywords</span></span>

<span data-ttu-id="b0140-141">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-141"></span></span>
|<span data-ttu-id="b0140-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-143">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-143">passport number</span></span>  <br/> <span data-ttu-id="b0140-144">벨기에 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-144">belgian passport number</span></span>  <br/> <span data-ttu-id="b0140-145">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-145">passport no</span></span>  <br/> <span data-ttu-id="b0140-146">고 대/ort</span><span class="sxs-lookup"><span data-stu-id="b0140-146">paspoort</span></span>  <br/> <span data-ttu-id="b0140-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="b0140-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="b0140-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="b0140-148">reisepass kein</span></span>  <br/> <span data-ttu-id="b0140-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="b0140-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="b0140-150">불가리아</span><span class="sxs-lookup"><span data-stu-id="b0140-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="b0140-151">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-151">Format</span></span>

<span data-ttu-id="b0140-152">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-153">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-153">Pattern</span></span>

 <span data-ttu-id="b0140-154">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="b0140-155">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-155">Checksum</span></span>

<span data-ttu-id="b0140-156">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-157">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-157">Definition</span></span>

<span data-ttu-id="b0140-158">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-159">정규식이 해당 `Regex_bulgaria_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-160">From `Keywords_bulgaria_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-161">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-161">Keywords</span></span>

<span data-ttu-id="b0140-162">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-162"></span></span>
|<span data-ttu-id="b0140-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-164">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-164">passport number</span></span>  <br/> <span data-ttu-id="b0140-165">불가리아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="b0140-166">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-166">passport no</span></span>  <br/> <span data-ttu-id="b0140-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="b0140-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="b0140-168">크로아티아</span><span class="sxs-lookup"><span data-stu-id="b0140-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="b0140-169">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-169">Format</span></span>

<span data-ttu-id="b0140-170">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-171">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-171">Pattern</span></span>

 <span data-ttu-id="b0140-172">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="b0140-173">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-173">Checksum</span></span>

<span data-ttu-id="b0140-174">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-175">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-175">Definition</span></span>

<span data-ttu-id="b0140-176">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-177">정규식이 해당 `Regex_croatia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-178">From `Keywords_croatia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-179">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-179">Keywords</span></span>

<span data-ttu-id="b0140-180">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-180"></span></span>
|<span data-ttu-id="b0140-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-182">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-182">passport number</span></span>  <br/> <span data-ttu-id="b0140-183">크로아티아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-183">croatian passport number</span></span>  <br/> <span data-ttu-id="b0140-184">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-184">passport no</span></span>  <br/> <span data-ttu-id="b0140-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="b0140-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="b0140-186">키프로스</span><span class="sxs-lookup"><span data-stu-id="b0140-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="b0140-187">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-187">Format</span></span>

<span data-ttu-id="b0140-188">공백 또는 구분 기호가 없는 1 개 문자 다음에 6-8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-189">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-189">Pattern</span></span>

<span data-ttu-id="b0140-190">한 문자 다음에 6 ~ 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0140-191">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-191">Checksum</span></span>

<span data-ttu-id="b0140-192">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-193">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-193">Definition</span></span>

<span data-ttu-id="b0140-194">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-195">정규식이 해당 `Regex_cyprus_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-196">From `Keywords_cyprus_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-197">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-197">Keywords</span></span>

<span data-ttu-id="b0140-198">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-198"></span></span>
|<span data-ttu-id="b0140-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-200">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-200">passport number</span></span>  <br/> <span data-ttu-id="b0140-201">키프로스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="b0140-202">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-202">passport no</span></span>  <br/> <span data-ttu-id="b0140-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="b0140-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="b0140-204">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="b0140-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="b0140-205">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-205">Format</span></span>

<span data-ttu-id="b0140-206">공백이 나 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-207">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-207">Pattern</span></span>

<span data-ttu-id="b0140-208">공백이 나 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0140-209">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-209">Checksum</span></span>

<span data-ttu-id="b0140-210">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-211">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-211">Definition</span></span>

<span data-ttu-id="b0140-212">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-213">정규식이 해당 `Regex_czech_republic_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-214">From `Keywords_czech_republic_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-215">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-215">Keywords</span></span>

<span data-ttu-id="b0140-216">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-216"></span></span>
|<span data-ttu-id="b0140-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-218">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-218">passport number</span></span>  <br/> <span data-ttu-id="b0140-219">체코어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-219">czech passport number</span></span>  <br/> <span data-ttu-id="b0140-220">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-220">passport no</span></span>  <br/> <span data-ttu-id="b0140-221">cestovní pas</span><span class="sxs-lookup"><span data-stu-id="b0140-221">cestovní pas</span></span>  <br/> <span data-ttu-id="b0140-222">pas</span><span class="sxs-lookup"><span data-stu-id="b0140-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="b0140-223">덴마크</span><span class="sxs-lookup"><span data-stu-id="b0140-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="b0140-224">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-224">Format</span></span>

<span data-ttu-id="b0140-225">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-226">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-226">Pattern</span></span>

 <span data-ttu-id="b0140-227">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="b0140-228">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-228">Checksum</span></span>

<span data-ttu-id="b0140-229">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-230">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-230">Definition</span></span>

<span data-ttu-id="b0140-231">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-232">정규식이 해당 `Regex_denmark_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-233">From `Keywords_denmark_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-234">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-234">Keywords</span></span>

<span data-ttu-id="b0140-235">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-235"></span></span>
|<span data-ttu-id="b0140-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-237">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-237">passport number</span></span>  <br/> <span data-ttu-id="b0140-238">덴마크어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-238">danish passport number</span></span>  <br/> <span data-ttu-id="b0140-239">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-239">passport no</span></span>  <br/> <span data-ttu-id="b0140-240">pas</span><span class="sxs-lookup"><span data-stu-id="b0140-240">pas</span></span>  <br/> <span data-ttu-id="b0140-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="b0140-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="b0140-242">에스토니아</span><span class="sxs-lookup"><span data-stu-id="b0140-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="b0140-243">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-243">Format</span></span>

<span data-ttu-id="b0140-244">공백 또는 구분 기호가 없는 1 개 문자 다음에 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-245">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-245">Pattern</span></span>

<span data-ttu-id="b0140-246">1 개의 문자 다음에 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0140-247">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-247">Checksum</span></span>

<span data-ttu-id="b0140-248">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-249">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-249">Definition</span></span>

<span data-ttu-id="b0140-250">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-251">정규식이 해당 `Regex_estonia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-252">From `Keywords_estonia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-253">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-253">Keywords</span></span>

<span data-ttu-id="b0140-254">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-254"></span></span>
|<span data-ttu-id="b0140-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-256">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-256">passport number</span></span>  <br/> <span data-ttu-id="b0140-257">에스토니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-257">estonian passport number</span></span>  <br/> <span data-ttu-id="b0140-258">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-258">passport no</span></span>  <br/> <span data-ttu-id="b0140-259">eesti kodaniku pass</span><span class="sxs-lookup"><span data-stu-id="b0140-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="b0140-260">핀란드</span><span class="sxs-lookup"><span data-stu-id="b0140-260">Finland</span></span>

<span data-ttu-id="b0140-261">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"핀란드 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b0140-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="b0140-262">프랑스</span><span class="sxs-lookup"><span data-stu-id="b0140-262">France</span></span>

<span data-ttu-id="b0140-263">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"프랑스 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b0140-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="b0140-264">독일</span><span class="sxs-lookup"><span data-stu-id="b0140-264">Germany</span></span>

<span data-ttu-id="b0140-265">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b0140-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="b0140-266">그리스</span><span class="sxs-lookup"><span data-stu-id="b0140-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="b0140-267">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-267">Format</span></span>

<span data-ttu-id="b0140-268">공백 또는 구분 기호가 없는 7 자리, 두 문자</span><span class="sxs-lookup"><span data-stu-id="b0140-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-269">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-269">Pattern</span></span>

<span data-ttu-id="b0140-270">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0140-271">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-271">Checksum</span></span>

<span data-ttu-id="b0140-272">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-273">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-273">Definition</span></span>

<span data-ttu-id="b0140-274">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-275">정규식이 해당 `Regex_greece_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-276">From `Keywords_greece_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-277">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-277">Keywords</span></span>

<span data-ttu-id="b0140-278">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-278"></span></span>
|<span data-ttu-id="b0140-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-280">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-280">passport number</span></span>  <br/> <span data-ttu-id="b0140-281">그리스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-281">greek passport number</span></span>  <br/> <span data-ttu-id="b0140-282">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-282">passport no</span></span>  <br/> <span data-ttu-id="b0140-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="b0140-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="b0140-284">헝가리</span><span class="sxs-lookup"><span data-stu-id="b0140-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="b0140-285">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-285">Format</span></span>

<span data-ttu-id="b0140-286">공백 또는 구분 기호가 없는 2 개 문자 및 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-287">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-287">Pattern</span></span>

<span data-ttu-id="b0140-288">2 개의 문자 다음에 6 개 또는 7 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0140-289">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-289">Checksum</span></span>

<span data-ttu-id="b0140-290">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-291">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-291">Definition</span></span>

<span data-ttu-id="b0140-292">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-293">정규식이 해당 `Regex_hungary_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-294">From `Keywords_hungary_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-295">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-295">Keywords</span></span>

<span data-ttu-id="b0140-296">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-296"></span></span>
|<span data-ttu-id="b0140-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-298">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-298">passport number</span></span>  <br/> <span data-ttu-id="b0140-299">헝가리어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="b0140-300">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-300">passport no</span></span>  <br/> <span data-ttu-id="b0140-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="b0140-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="b0140-302">Ireland</span><span class="sxs-lookup"><span data-stu-id="b0140-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="b0140-303">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-303">Format</span></span>

<span data-ttu-id="b0140-304">공백이 나 구분 기호가 없는 두 개의 문자 또는 숫자와 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-305">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-305">Pattern</span></span>

<span data-ttu-id="b0140-306">두 개의 문자 또는 숫자와 7 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="b0140-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="b0140-307">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="b0140-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="b0140-308">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0140-309">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-309">Checksum</span></span>

<span data-ttu-id="b0140-310">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-311">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-311">Definition</span></span>

<span data-ttu-id="b0140-312">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-313">정규식이 해당 `Regex_ireland_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-314">From `Keywords_ireland_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-315">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-315">Keywords</span></span>

<span data-ttu-id="b0140-316">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-316"></span></span>
|<span data-ttu-id="b0140-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-318">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-318">passport number</span></span>  <br/> <span data-ttu-id="b0140-319">아일랜드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-319">irish passport number</span></span>  <br/> <span data-ttu-id="b0140-320">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-320">passport no</span></span>  <br/> <span data-ttu-id="b0140-321">pas</span><span class="sxs-lookup"><span data-stu-id="b0140-321">pas</span></span>  <br/> <span data-ttu-id="b0140-322">여권</span><span class="sxs-lookup"><span data-stu-id="b0140-322">passport</span></span>  <br/> <span data-ttu-id="b0140-323">포트</span><span class="sxs-lookup"><span data-stu-id="b0140-323">passeport</span></span>  <br/> <span data-ttu-id="b0140-324">포트 numero</span><span class="sxs-lookup"><span data-stu-id="b0140-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="b0140-325">이탈리아</span><span class="sxs-lookup"><span data-stu-id="b0140-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="b0140-326">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-326">Format</span></span>

<span data-ttu-id="b0140-327">공백이 나 구분 기호가 없는 두 개의 문자 또는 숫자와 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-328">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-328">Pattern</span></span>

<span data-ttu-id="b0140-329">두 개의 문자 또는 숫자와 7 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="b0140-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="b0140-330">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="b0140-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="b0140-331">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0140-332">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-332">Checksum</span></span>

<span data-ttu-id="b0140-333">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="b0140-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-334">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-334">Definition</span></span>

<span data-ttu-id="b0140-335">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-336">정규식이 해당 `Regex_italy_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-337">From `Keywords_italy_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-338">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-338">Keywords</span></span>

<span data-ttu-id="b0140-339">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-339"></span></span>
|<span data-ttu-id="b0140-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-341">이탈리아 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-341">italian passport number</span></span>  <br/> <span data-ttu-id="b0140-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="b0140-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="b0140-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="b0140-343">passaporto</span></span>  <br/> <span data-ttu-id="b0140-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="b0140-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="b0140-345">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-345">passport number</span></span>  <br/> <span data-ttu-id="b0140-346">italiana passaporto numero</span><span class="sxs-lookup"><span data-stu-id="b0140-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="b0140-347">passaporto numero</span><span class="sxs-lookup"><span data-stu-id="b0140-347">passaporto numero</span></span>  <br/> <span data-ttu-id="b0140-348">numéro) 포트 italien</span><span class="sxs-lookup"><span data-stu-id="b0140-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="b0140-349">numéro (고) 포트</span><span class="sxs-lookup"><span data-stu-id="b0140-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="b0140-350">라트비아</span><span class="sxs-lookup"><span data-stu-id="b0140-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="b0140-351">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-351">Format</span></span>

<span data-ttu-id="b0140-352">공백이 나 구분 기호가 없는 두 개의 문자 또는 숫자와 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-353">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-353">Pattern</span></span>

<span data-ttu-id="b0140-354">두 개의 문자 또는 숫자와 7 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="b0140-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="b0140-355">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="b0140-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="b0140-356">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0140-357">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-357">Checksum</span></span>

<span data-ttu-id="b0140-358">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-359">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-359">Definition</span></span>

<span data-ttu-id="b0140-360">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-361">정규식이 해당 `Regex_latvia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-362">From `Keywords_latvia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-363">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-363">Keywords</span></span>

<span data-ttu-id="b0140-364">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-364"></span></span>
|<span data-ttu-id="b0140-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-366">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-366">passport number</span></span>  <br/> <span data-ttu-id="b0140-367">라트비아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-367">latvian passport number</span></span>  <br/> <span data-ttu-id="b0140-368">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-368">passport no</span></span>  <br/> <span data-ttu-id="b0140-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="b0140-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="b0140-370">리투아니아</span><span class="sxs-lookup"><span data-stu-id="b0140-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="b0140-371">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-371">Format</span></span>

<span data-ttu-id="b0140-372">공백이 나 구분 기호가 없는 8 자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="b0140-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-373">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-373">Pattern</span></span>

<span data-ttu-id="b0140-374">8 자리 숫자 또는 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="b0140-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0140-375">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-375">Checksum</span></span>

<span data-ttu-id="b0140-376">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="b0140-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-377">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-377">Definition</span></span>

<span data-ttu-id="b0140-378">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-379">정규식이 해당 `Regex_lithuania_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-380">From `Keywords_lithuania_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-381">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-381">Keywords</span></span>

<span data-ttu-id="b0140-382">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-382"></span></span>
|<span data-ttu-id="b0140-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-384">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-384">passport number</span></span>  <br/> <span data-ttu-id="b0140-385">lithunian 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="b0140-386">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-386">passport no</span></span>  <br/> <span data-ttu-id="b0140-387">numeris</span><span class="sxs-lookup"><span data-stu-id="b0140-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="b0140-388">셈</span><span class="sxs-lookup"><span data-stu-id="b0140-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="b0140-389">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-389">Format</span></span>

<span data-ttu-id="b0140-390">공백이 나 구분 기호가 없는 8 자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="b0140-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-391">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-391">Pattern</span></span>

<span data-ttu-id="b0140-392">8 자리 숫자 또는 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="b0140-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0140-393">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-393">Checksum</span></span>

<span data-ttu-id="b0140-394">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-395">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-395">Definition</span></span>

<span data-ttu-id="b0140-396">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-397">정규식이 해당 `Regex_nation_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-398">From `Keywords_nation_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-399">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-399">Keywords</span></span>

<span data-ttu-id="b0140-400">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-400"></span></span>
|<span data-ttu-id="b0140-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-402">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-402">passport number</span></span>  <br/> <span data-ttu-id="b0140-403">라트비아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-403">latvian passport number</span></span>  <br/> <span data-ttu-id="b0140-404">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-404">passport no</span></span>  <br/> <span data-ttu-id="b0140-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="b0140-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="b0140-406">몰타</span><span class="sxs-lookup"><span data-stu-id="b0140-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="b0140-407">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-407">Format</span></span>

<span data-ttu-id="b0140-408">공백이 나 구분 기호 없이 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-409">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-409">Pattern</span></span>

 <span data-ttu-id="b0140-410">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="b0140-411">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-411">Checksum</span></span>

<span data-ttu-id="b0140-412">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-413">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-413">Definition</span></span>

<span data-ttu-id="b0140-414">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-415">정규식이 해당 `Regex_malta_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-416">From `Keywords_malta_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-417">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-417">Keywords</span></span>

<span data-ttu-id="b0140-418">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-418"></span></span>
|<span data-ttu-id="b0140-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-420">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-420">passport number</span></span>  <br/> <span data-ttu-id="b0140-421">몰타어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-421">maltese passport number</span></span>  <br/> <span data-ttu-id="b0140-422">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-422">passport no</span></span>  <br/> <span data-ttu-id="b0140-423">numru-passaport</span><span class="sxs-lookup"><span data-stu-id="b0140-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="b0140-424">네덜란드</span><span class="sxs-lookup"><span data-stu-id="b0140-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="b0140-425">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-425">Format</span></span>

<span data-ttu-id="b0140-426">공백이 나 구분 기호가 없는 9 개의 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-427">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-427">Pattern</span></span>

<span data-ttu-id="b0140-428">9 개의 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0140-429">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-429">Checksum</span></span>

<span data-ttu-id="b0140-430">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="b0140-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-431">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-431">Definition</span></span>

<span data-ttu-id="b0140-432">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-433">정규식이 해당 `Regex_netherlands_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-434">From `Keywords_netherlands_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-435">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-435">Keywords</span></span>

<span data-ttu-id="b0140-436">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-436"></span></span>
|<span data-ttu-id="b0140-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-438">네덜란드어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-438">dutch passport number</span></span>  <br/> <span data-ttu-id="b0140-439">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-439">passport number</span></span>  <br/> <span data-ttu-id="b0140-440">네덜란드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="b0140-441">nederlanden, nummer ort</span><span class="sxs-lookup"><span data-stu-id="b0140-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="b0140-442">고 대/ort</span><span class="sxs-lookup"><span data-stu-id="b0140-442">paspoort</span></span>  <br/> <span data-ttu-id="b0140-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="b0140-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="b0140-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="b0140-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="b0140-445">폴란드</span><span class="sxs-lookup"><span data-stu-id="b0140-445">Poland</span></span>

<span data-ttu-id="b0140-446">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"폴란드 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b0140-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="b0140-447">포르투갈</span><span class="sxs-lookup"><span data-stu-id="b0140-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="b0140-448">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-448">Format</span></span>

<span data-ttu-id="b0140-449">공백 또는 구분 기호가 없는 한 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-450">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-450">Pattern</span></span>

<span data-ttu-id="b0140-451">1 개의 문자 다음에 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="b0140-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="b0140-452">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="b0140-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="b0140-453">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0140-454">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-454">Checksum</span></span>

<span data-ttu-id="b0140-455">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-456">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-456">Definition</span></span>

<span data-ttu-id="b0140-457">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-458">정규식이 해당 `Regex_portugal_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-459">From `Keywords_portugal_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-460">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-460">Keywords</span></span>

<span data-ttu-id="b0140-461">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-461"></span></span>
|<span data-ttu-id="b0140-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-463">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-463">passport number</span></span>  <br/> <span data-ttu-id="b0140-464">포르투갈어 passport 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="b0140-465">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-465">passport no</span></span>  <br/> <span data-ttu-id="b0140-466">número do passaporte</span><span class="sxs-lookup"><span data-stu-id="b0140-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="b0140-467">루마니아</span><span class="sxs-lookup"><span data-stu-id="b0140-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="b0140-468">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-468">Format</span></span>

<span data-ttu-id="b0140-469">공백과 구분 기호를 사용 하지 않고 8 또는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-470">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-470">Pattern</span></span>

<span data-ttu-id="b0140-471">8 또는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0140-472">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-472">Checksum</span></span>

<span data-ttu-id="b0140-473">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-474">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-474">Definition</span></span>

<span data-ttu-id="b0140-475">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-476">정규식이 해당 `Regex_romania_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-477">From `Keywords_romania_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-478">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-478">Keywords</span></span>

<span data-ttu-id="b0140-479">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-479"></span></span>
|<span data-ttu-id="b0140-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-481">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-481">passport number</span></span>  <br/> <span data-ttu-id="b0140-482">루마니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-482">romanian passport number</span></span>  <br/> <span data-ttu-id="b0140-483">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-483">passport no</span></span>  <br/> <span data-ttu-id="b0140-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="b0140-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="b0140-485">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="b0140-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="b0140-486">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-486">Format</span></span>

<span data-ttu-id="b0140-487">공백 또는 구분 기호가 없는 한 자리 숫자 또는 문자 다음에 일곱 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-488">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-488">Pattern</span></span>

<span data-ttu-id="b0140-489">1 자리 숫자 또는 문자 (대/소문자 구분 안 함)와 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0140-490">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-490">Checksum</span></span>

<span data-ttu-id="b0140-491">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-492">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-492">Definition</span></span>

<span data-ttu-id="b0140-493">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-494">정규식이 해당 `Regex_slovakia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-495">From `Keywords_slovakia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-496">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-496">Keywords</span></span>

<span data-ttu-id="b0140-497">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-497"></span></span>
|<span data-ttu-id="b0140-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-499">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-499">passport number</span></span>  <br/> <span data-ttu-id="b0140-500">슬로바키아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="b0140-501">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-501">passport no</span></span>  <br/> <span data-ttu-id="b0140-502">číslo (u)</span><span class="sxs-lookup"><span data-stu-id="b0140-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="b0140-503">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="b0140-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="b0140-504">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-504">Format</span></span>

<span data-ttu-id="b0140-505">공백 또는 구분 기호가 없는 7 자리, 두 문자</span><span class="sxs-lookup"><span data-stu-id="b0140-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-506">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-506">Pattern</span></span>

<span data-ttu-id="b0140-507">2 개 문자와 7 자리 숫자를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="b0140-508">"P" 문자</span><span class="sxs-lookup"><span data-stu-id="b0140-508">The letter "P"</span></span>
    
- <span data-ttu-id="b0140-509">대문자 1 개</span><span class="sxs-lookup"><span data-stu-id="b0140-509">One uppercase letter</span></span>
    
- <span data-ttu-id="b0140-510">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0140-511">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-511">Checksum</span></span>

<span data-ttu-id="b0140-512">아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-513">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-513">Definition</span></span>

<span data-ttu-id="b0140-514">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-515">정규식이 해당 `Regex_slovenia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-516">From `Keywords_slovenia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-517">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-517">Keywords</span></span>

<span data-ttu-id="b0140-518">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-518"></span></span>
|<span data-ttu-id="b0140-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-520">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-520">passport number</span></span>  <br/> <span data-ttu-id="b0140-521">슬로베니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="b0140-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="b0140-522">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-522">passport no</span></span>  <br/> <span data-ttu-id="b0140-523">številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="b0140-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="b0140-524">스페인</span><span class="sxs-lookup"><span data-stu-id="b0140-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="b0140-525">형식일</span><span class="sxs-lookup"><span data-stu-id="b0140-525">Format</span></span>

<span data-ttu-id="b0140-526">공백이 나 구분 기호가 없는 문자 및 숫자의 8 자리 또는 9 자 조합</span><span class="sxs-lookup"><span data-stu-id="b0140-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0140-527">패턴</span><span class="sxs-lookup"><span data-stu-id="b0140-527">Pattern</span></span>

<span data-ttu-id="b0140-528">문자와 숫자의 8 자리 또는 9 자리 조합:</span><span class="sxs-lookup"><span data-stu-id="b0140-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="b0140-529">두 자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="b0140-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="b0140-530">1 자리 숫자 또는 문자 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="b0140-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="b0140-531">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b0140-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0140-532">제외</span><span class="sxs-lookup"><span data-stu-id="b0140-532">Checksum</span></span>

<span data-ttu-id="b0140-533">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="b0140-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0140-534">정의</span><span class="sxs-lookup"><span data-stu-id="b0140-534">Definition</span></span>

<span data-ttu-id="b0140-535">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0140-536">정규식이 해당 `Regex_spain_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0140-537">From `Keywords_spain_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0140-538">키워드</span><span class="sxs-lookup"><span data-stu-id="b0140-538">Keywords</span></span>

<span data-ttu-id="b0140-539">| |</span><span class="sxs-lookup"><span data-stu-id="b0140-539"></span></span>
|<span data-ttu-id="b0140-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="b0140-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="b0140-541">여권</span><span class="sxs-lookup"><span data-stu-id="b0140-541">passport</span></span>  <br/> <span data-ttu-id="b0140-542">스페인 여권</span><span class="sxs-lookup"><span data-stu-id="b0140-542">spain passport</span></span>  <br/> <span data-ttu-id="b0140-543">passport 책</span><span class="sxs-lookup"><span data-stu-id="b0140-543">passport book</span></span>  <br/> <span data-ttu-id="b0140-544">passport number</span><span class="sxs-lookup"><span data-stu-id="b0140-544">passport number</span></span>  <br/> <span data-ttu-id="b0140-545">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="b0140-545">passport no</span></span>  <br/> <span data-ttu-id="b0140-546">pasaporte</span><span class="sxs-lookup"><span data-stu-id="b0140-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="b0140-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="b0140-547">número pasaporte</span></span>  <br/> <span data-ttu-id="b0140-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="b0140-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="b0140-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="b0140-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="b0140-550">스웨덴</span><span class="sxs-lookup"><span data-stu-id="b0140-550">Sweden</span></span>

<span data-ttu-id="b0140-551">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"스웨덴 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b0140-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="b0140-552">영국의</span><span class="sxs-lookup"><span data-stu-id="b0140-552">UK</span></span>

<span data-ttu-id="b0140-553">자세한 내용은 "미국/영국" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b0140-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="b0140-554">[중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)Passport 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="b0140-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b0140-555">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b0140-555">See also</span></span>

[<span data-ttu-id="b0140-556">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="b0140-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

