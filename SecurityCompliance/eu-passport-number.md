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
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410933"
---
# <a name="eu-passport-number"></a><span data-ttu-id="9d823-104">EU 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-104">EU Passport Number</span></span>

<span data-ttu-id="9d823-105">이 항목에서는 DLP (데이터 손실 방지) 정책이 EU (유럽 여권 번호) 중요 한 정보 유형을 검색할 때 찾는 항목을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="9d823-106">이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="9d823-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="9d823-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="9d823-108">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-108">Format</span></span>

<span data-ttu-id="9d823-109">1 개의 문자 다음에 선택적 공백, 일곱 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-110">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-110">Pattern</span></span>

<span data-ttu-id="9d823-111">한 글자, 일곱 자리 및 한 가지 공백 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="9d823-112">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="9d823-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="9d823-113">1 개의 공백 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="9d823-113">One space (optional)</span></span>
    
- <span data-ttu-id="9d823-114">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9d823-115">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-115">Checksum</span></span>

<span data-ttu-id="9d823-116">해당 없음</span><span class="sxs-lookup"><span data-stu-id="9d823-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-117">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-117">Definition</span></span>

<span data-ttu-id="9d823-118">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-119">정규식이 해당 `Regex_austria_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-120">from `Keywords_austria_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-121">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-121">Keywords</span></span>

<span data-ttu-id="9d823-122">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-122"></span></span>
|<span data-ttu-id="9d823-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-124">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-124">passport number</span></span>  <br/> <span data-ttu-id="9d823-125">오스트리아 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-125">austrian passport number</span></span>  <br/> <span data-ttu-id="9d823-126">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-126">passport no</span></span>  <br/> <span data-ttu-id="9d823-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="9d823-127">reisepass</span></span>  <br/> <span data-ttu-id="9d823-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="9d823-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="9d823-129">벨기에</span><span class="sxs-lookup"><span data-stu-id="9d823-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="9d823-130">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-130">Format</span></span>

<span data-ttu-id="9d823-131">공백 또는 구분 기호가 없는 2 개 문자 다음에 6 자리 숫자 사용</span><span class="sxs-lookup"><span data-stu-id="9d823-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-132">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-132">Pattern</span></span>

<span data-ttu-id="9d823-133">2 개 문자 및 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9d823-134">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-134">Checksum</span></span>

<span data-ttu-id="9d823-135">해당 없음</span><span class="sxs-lookup"><span data-stu-id="9d823-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-136">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-136">Definition</span></span>

<span data-ttu-id="9d823-137">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-138">정규식이 해당 `Regex_belgium_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-139">from `Keywords_belgium_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-140">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-140">Keywords</span></span>

<span data-ttu-id="9d823-141">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-141"></span></span>
|<span data-ttu-id="9d823-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-143">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-143">passport number</span></span>  <br/> <span data-ttu-id="9d823-144">벨기에 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-144">belgian passport number</span></span>  <br/> <span data-ttu-id="9d823-145">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-145">passport no</span></span>  <br/> <span data-ttu-id="9d823-146">고 대/ort</span><span class="sxs-lookup"><span data-stu-id="9d823-146">paspoort</span></span>  <br/> <span data-ttu-id="9d823-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="9d823-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="9d823-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="9d823-148">reisepass kein</span></span>  <br/> <span data-ttu-id="9d823-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="9d823-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="9d823-150">불가리아</span><span class="sxs-lookup"><span data-stu-id="9d823-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="9d823-151">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-151">Format</span></span>

<span data-ttu-id="9d823-152">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-153">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-153">Pattern</span></span>

 <span data-ttu-id="9d823-154">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="9d823-155">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-155">Checksum</span></span>

<span data-ttu-id="9d823-156">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-157">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-157">Definition</span></span>

<span data-ttu-id="9d823-158">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-159">정규식이 해당 `Regex_bulgaria_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-160">from `Keywords_bulgaria_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-161">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-161">Keywords</span></span>

<span data-ttu-id="9d823-162">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-162"></span></span>
|<span data-ttu-id="9d823-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-164">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-164">passport number</span></span>  <br/> <span data-ttu-id="9d823-165">불가리아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="9d823-166">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-166">passport no</span></span>  <br/> <span data-ttu-id="9d823-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="9d823-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="9d823-168">크로아티아</span><span class="sxs-lookup"><span data-stu-id="9d823-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="9d823-169">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-169">Format</span></span>

<span data-ttu-id="9d823-170">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-171">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-171">Pattern</span></span>

 <span data-ttu-id="9d823-172">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="9d823-173">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-173">Checksum</span></span>

<span data-ttu-id="9d823-174">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-175">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-175">Definition</span></span>

<span data-ttu-id="9d823-176">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-177">정규식이 해당 `Regex_croatia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-178">from `Keywords_croatia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-179">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-179">Keywords</span></span>

<span data-ttu-id="9d823-180">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-180"></span></span>
|<span data-ttu-id="9d823-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-182">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-182">passport number</span></span>  <br/> <span data-ttu-id="9d823-183">크로아티아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-183">croatian passport number</span></span>  <br/> <span data-ttu-id="9d823-184">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-184">passport no</span></span>  <br/> <span data-ttu-id="9d823-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="9d823-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="9d823-186">키프로스</span><span class="sxs-lookup"><span data-stu-id="9d823-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="9d823-187">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-187">Format</span></span>

<span data-ttu-id="9d823-188">공백 또는 구분 기호가 없는 1 개 문자 다음에 6-8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-189">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-189">Pattern</span></span>

<span data-ttu-id="9d823-190">한 문자 다음에 6 ~ 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9d823-191">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-191">Checksum</span></span>

<span data-ttu-id="9d823-192">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-193">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-193">Definition</span></span>

<span data-ttu-id="9d823-194">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-195">정규식이 해당 `Regex_cyprus_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-196">from `Keywords_cyprus_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-197">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-197">Keywords</span></span>

<span data-ttu-id="9d823-198">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-198"></span></span>
|<span data-ttu-id="9d823-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-200">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-200">passport number</span></span>  <br/> <span data-ttu-id="9d823-201">키프로스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="9d823-202">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-202">passport no</span></span>  <br/> <span data-ttu-id="9d823-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="9d823-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="9d823-204">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="9d823-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="9d823-205">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-205">Format</span></span>

<span data-ttu-id="9d823-206">공백이 나 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-207">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-207">Pattern</span></span>

<span data-ttu-id="9d823-208">공백이 나 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9d823-209">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-209">Checksum</span></span>

<span data-ttu-id="9d823-210">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-211">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-211">Definition</span></span>

<span data-ttu-id="9d823-212">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-213">정규식이 해당 `Regex_czech_republic_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-214">from `Keywords_czech_republic_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-215">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-215">Keywords</span></span>

<span data-ttu-id="9d823-216">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-216"></span></span>
|<span data-ttu-id="9d823-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-218">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-218">passport number</span></span>  <br/> <span data-ttu-id="9d823-219">체코어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-219">czech passport number</span></span>  <br/> <span data-ttu-id="9d823-220">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-220">passport no</span></span>  <br/> <span data-ttu-id="9d823-221">cestovní pas</span><span class="sxs-lookup"><span data-stu-id="9d823-221">cestovní pas</span></span>  <br/> <span data-ttu-id="9d823-222">pas</span><span class="sxs-lookup"><span data-stu-id="9d823-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="9d823-223">덴마크</span><span class="sxs-lookup"><span data-stu-id="9d823-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="9d823-224">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-224">Format</span></span>

<span data-ttu-id="9d823-225">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-226">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-226">Pattern</span></span>

 <span data-ttu-id="9d823-227">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="9d823-228">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-228">Checksum</span></span>

<span data-ttu-id="9d823-229">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-230">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-230">Definition</span></span>

<span data-ttu-id="9d823-231">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-232">정규식이 해당 `Regex_denmark_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-233">from `Keywords_denmark_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-234">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-234">Keywords</span></span>

<span data-ttu-id="9d823-235">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-235"></span></span>
|<span data-ttu-id="9d823-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-237">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-237">passport number</span></span>  <br/> <span data-ttu-id="9d823-238">덴마크어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-238">danish passport number</span></span>  <br/> <span data-ttu-id="9d823-239">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-239">passport no</span></span>  <br/> <span data-ttu-id="9d823-240">pas</span><span class="sxs-lookup"><span data-stu-id="9d823-240">pas</span></span>  <br/> <span data-ttu-id="9d823-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="9d823-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="9d823-242">에스토니아</span><span class="sxs-lookup"><span data-stu-id="9d823-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="9d823-243">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-243">Format</span></span>

<span data-ttu-id="9d823-244">공백 또는 구분 기호가 없는 1 개 문자 다음에 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-245">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-245">Pattern</span></span>

<span data-ttu-id="9d823-246">1 개의 문자 다음에 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9d823-247">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-247">Checksum</span></span>

<span data-ttu-id="9d823-248">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-249">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-249">Definition</span></span>

<span data-ttu-id="9d823-250">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-251">정규식이 해당 `Regex_estonia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-252">from `Keywords_estonia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-253">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-253">Keywords</span></span>

<span data-ttu-id="9d823-254">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-254"></span></span>
|<span data-ttu-id="9d823-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-256">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-256">passport number</span></span>  <br/> <span data-ttu-id="9d823-257">에스토니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-257">estonian passport number</span></span>  <br/> <span data-ttu-id="9d823-258">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-258">passport no</span></span>  <br/> <span data-ttu-id="9d823-259">eesti kodaniku pass</span><span class="sxs-lookup"><span data-stu-id="9d823-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="9d823-260">핀란드</span><span class="sxs-lookup"><span data-stu-id="9d823-260">Finland</span></span>

<span data-ttu-id="9d823-261">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"핀란드 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9d823-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="9d823-262">프랑스</span><span class="sxs-lookup"><span data-stu-id="9d823-262">France</span></span>

<span data-ttu-id="9d823-263">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"프랑스 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9d823-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="9d823-264">독일</span><span class="sxs-lookup"><span data-stu-id="9d823-264">Germany</span></span>

<span data-ttu-id="9d823-265">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9d823-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="9d823-266">그리스</span><span class="sxs-lookup"><span data-stu-id="9d823-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="9d823-267">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-267">Format</span></span>

<span data-ttu-id="9d823-268">공백 또는 구분 기호가 없는 7 자리, 두 문자</span><span class="sxs-lookup"><span data-stu-id="9d823-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-269">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-269">Pattern</span></span>

<span data-ttu-id="9d823-270">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9d823-271">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-271">Checksum</span></span>

<span data-ttu-id="9d823-272">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-273">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-273">Definition</span></span>

<span data-ttu-id="9d823-274">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-275">정규식이 해당 `Regex_greece_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-276">from `Keywords_greece_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-277">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-277">Keywords</span></span>

<span data-ttu-id="9d823-278">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-278"></span></span>
|<span data-ttu-id="9d823-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-280">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-280">passport number</span></span>  <br/> <span data-ttu-id="9d823-281">그리스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-281">greek passport number</span></span>  <br/> <span data-ttu-id="9d823-282">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-282">passport no</span></span>  <br/> <span data-ttu-id="9d823-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="9d823-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="9d823-284">헝가리</span><span class="sxs-lookup"><span data-stu-id="9d823-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="9d823-285">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-285">Format</span></span>

<span data-ttu-id="9d823-286">공백 또는 구분 기호가 없는 2 개 문자 및 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-287">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-287">Pattern</span></span>

<span data-ttu-id="9d823-288">2 개의 문자 다음에 6 개 또는 7 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9d823-289">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-289">Checksum</span></span>

<span data-ttu-id="9d823-290">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-291">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-291">Definition</span></span>

<span data-ttu-id="9d823-292">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-293">정규식이 해당 `Regex_hungary_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-294">from `Keywords_hungary_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-295">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-295">Keywords</span></span>

<span data-ttu-id="9d823-296">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-296"></span></span>
|<span data-ttu-id="9d823-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-298">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-298">passport number</span></span>  <br/> <span data-ttu-id="9d823-299">헝가리어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="9d823-300">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-300">passport no</span></span>  <br/> <span data-ttu-id="9d823-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="9d823-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="9d823-302">Ireland</span><span class="sxs-lookup"><span data-stu-id="9d823-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="9d823-303">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-303">Format</span></span>

<span data-ttu-id="9d823-304">공백이 나 구분 기호가 없는 두 개의 문자 또는 숫자와 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-305">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-305">Pattern</span></span>

<span data-ttu-id="9d823-306">두 개의 문자 또는 숫자와 7 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="9d823-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="9d823-307">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="9d823-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="9d823-308">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9d823-309">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-309">Checksum</span></span>

<span data-ttu-id="9d823-310">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-311">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-311">Definition</span></span>

<span data-ttu-id="9d823-312">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-313">정규식이 해당 `Regex_ireland_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-314">from `Keywords_ireland_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-315">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-315">Keywords</span></span>

<span data-ttu-id="9d823-316">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-316"></span></span>
|<span data-ttu-id="9d823-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-318">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-318">passport number</span></span>  <br/> <span data-ttu-id="9d823-319">아일랜드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-319">irish passport number</span></span>  <br/> <span data-ttu-id="9d823-320">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-320">passport no</span></span>  <br/> <span data-ttu-id="9d823-321">pas</span><span class="sxs-lookup"><span data-stu-id="9d823-321">pas</span></span>  <br/> <span data-ttu-id="9d823-322">여권</span><span class="sxs-lookup"><span data-stu-id="9d823-322">passport</span></span>  <br/> <span data-ttu-id="9d823-323">포트</span><span class="sxs-lookup"><span data-stu-id="9d823-323">passeport</span></span>  <br/> <span data-ttu-id="9d823-324">포트 numero</span><span class="sxs-lookup"><span data-stu-id="9d823-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="9d823-325">이탈리아</span><span class="sxs-lookup"><span data-stu-id="9d823-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="9d823-326">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-326">Format</span></span>

<span data-ttu-id="9d823-327">공백이 나 구분 기호가 없는 두 개의 문자 또는 숫자와 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-328">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-328">Pattern</span></span>

<span data-ttu-id="9d823-329">두 개의 문자 또는 숫자와 7 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="9d823-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="9d823-330">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="9d823-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="9d823-331">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9d823-332">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-332">Checksum</span></span>

<span data-ttu-id="9d823-333">해당 없음</span><span class="sxs-lookup"><span data-stu-id="9d823-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-334">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-334">Definition</span></span>

<span data-ttu-id="9d823-335">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-336">정규식이 해당 `Regex_italy_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-337">from `Keywords_italy_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-338">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-338">Keywords</span></span>

<span data-ttu-id="9d823-339">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-339"></span></span>
|<span data-ttu-id="9d823-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-341">이탈리아 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-341">italian passport number</span></span>  <br/> <span data-ttu-id="9d823-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="9d823-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="9d823-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="9d823-343">passaporto</span></span>  <br/> <span data-ttu-id="9d823-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="9d823-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="9d823-345">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-345">passport number</span></span>  <br/> <span data-ttu-id="9d823-346">italiana passaporto numero</span><span class="sxs-lookup"><span data-stu-id="9d823-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="9d823-347">passaporto numero</span><span class="sxs-lookup"><span data-stu-id="9d823-347">passaporto numero</span></span>  <br/> <span data-ttu-id="9d823-348">numéro) 포트 italien</span><span class="sxs-lookup"><span data-stu-id="9d823-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="9d823-349">numéro (고) 포트</span><span class="sxs-lookup"><span data-stu-id="9d823-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="9d823-350">라트비아</span><span class="sxs-lookup"><span data-stu-id="9d823-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="9d823-351">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-351">Format</span></span>

<span data-ttu-id="9d823-352">공백이 나 구분 기호가 없는 두 개의 문자 또는 숫자와 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-353">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-353">Pattern</span></span>

<span data-ttu-id="9d823-354">두 개의 문자 또는 숫자와 7 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="9d823-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="9d823-355">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="9d823-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="9d823-356">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9d823-357">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-357">Checksum</span></span>

<span data-ttu-id="9d823-358">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-359">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-359">Definition</span></span>

<span data-ttu-id="9d823-360">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-361">정규식이 해당 `Regex_latvia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-362">from `Keywords_latvia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-363">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-363">Keywords</span></span>

<span data-ttu-id="9d823-364">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-364"></span></span>
|<span data-ttu-id="9d823-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-366">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-366">passport number</span></span>  <br/> <span data-ttu-id="9d823-367">라트비아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-367">latvian passport number</span></span>  <br/> <span data-ttu-id="9d823-368">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-368">passport no</span></span>  <br/> <span data-ttu-id="9d823-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="9d823-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="9d823-370">리투아니아</span><span class="sxs-lookup"><span data-stu-id="9d823-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="9d823-371">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-371">Format</span></span>

<span data-ttu-id="9d823-372">공백이 나 구분 기호가 없는 8 자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="9d823-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-373">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-373">Pattern</span></span>

<span data-ttu-id="9d823-374">8 자리 숫자 또는 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="9d823-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9d823-375">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-375">Checksum</span></span>

<span data-ttu-id="9d823-376">해당 없음</span><span class="sxs-lookup"><span data-stu-id="9d823-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-377">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-377">Definition</span></span>

<span data-ttu-id="9d823-378">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-379">정규식이 해당 `Regex_lithuania_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-380">from `Keywords_lithuania_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-381">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-381">Keywords</span></span>

<span data-ttu-id="9d823-382">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-382"></span></span>
|<span data-ttu-id="9d823-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-384">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-384">passport number</span></span>  <br/> <span data-ttu-id="9d823-385">lithunian 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="9d823-386">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-386">passport no</span></span>  <br/> <span data-ttu-id="9d823-387">numeris</span><span class="sxs-lookup"><span data-stu-id="9d823-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="9d823-388">셈</span><span class="sxs-lookup"><span data-stu-id="9d823-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="9d823-389">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-389">Format</span></span>

<span data-ttu-id="9d823-390">공백이 나 구분 기호가 없는 8 자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="9d823-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-391">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-391">Pattern</span></span>

<span data-ttu-id="9d823-392">8 자리 숫자 또는 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="9d823-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9d823-393">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-393">Checksum</span></span>

<span data-ttu-id="9d823-394">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-395">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-395">Definition</span></span>

<span data-ttu-id="9d823-396">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-397">정규식이 해당 `Regex_nation_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-398">from `Keywords_nation_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-399">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-399">Keywords</span></span>

<span data-ttu-id="9d823-400">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-400"></span></span>
|<span data-ttu-id="9d823-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-402">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-402">passport number</span></span>  <br/> <span data-ttu-id="9d823-403">라트비아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-403">latvian passport number</span></span>  <br/> <span data-ttu-id="9d823-404">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-404">passport no</span></span>  <br/> <span data-ttu-id="9d823-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="9d823-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="9d823-406">몰타</span><span class="sxs-lookup"><span data-stu-id="9d823-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="9d823-407">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-407">Format</span></span>

<span data-ttu-id="9d823-408">공백이 나 구분 기호 없이 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-409">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-409">Pattern</span></span>

 <span data-ttu-id="9d823-410">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="9d823-411">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-411">Checksum</span></span>

<span data-ttu-id="9d823-412">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-413">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-413">Definition</span></span>

<span data-ttu-id="9d823-414">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-415">정규식이 해당 `Regex_malta_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-416">from `Keywords_malta_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-417">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-417">Keywords</span></span>

<span data-ttu-id="9d823-418">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-418"></span></span>
|<span data-ttu-id="9d823-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-420">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-420">passport number</span></span>  <br/> <span data-ttu-id="9d823-421">몰타어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-421">maltese passport number</span></span>  <br/> <span data-ttu-id="9d823-422">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-422">passport no</span></span>  <br/> <span data-ttu-id="9d823-423">numru-passaport</span><span class="sxs-lookup"><span data-stu-id="9d823-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="9d823-424">네덜란드</span><span class="sxs-lookup"><span data-stu-id="9d823-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="9d823-425">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-425">Format</span></span>

<span data-ttu-id="9d823-426">공백이 나 구분 기호가 없는 9 개의 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-427">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-427">Pattern</span></span>

<span data-ttu-id="9d823-428">9 개의 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9d823-429">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-429">Checksum</span></span>

<span data-ttu-id="9d823-430">해당 없음</span><span class="sxs-lookup"><span data-stu-id="9d823-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-431">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-431">Definition</span></span>

<span data-ttu-id="9d823-432">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-433">정규식이 해당 `Regex_netherlands_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-434">from `Keywords_netherlands_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-435">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-435">Keywords</span></span>

<span data-ttu-id="9d823-436">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-436"></span></span>
|<span data-ttu-id="9d823-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-438">네덜란드어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-438">dutch passport number</span></span>  <br/> <span data-ttu-id="9d823-439">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-439">passport number</span></span>  <br/> <span data-ttu-id="9d823-440">네덜란드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="9d823-441">nederlanden, nummer ort</span><span class="sxs-lookup"><span data-stu-id="9d823-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="9d823-442">고 대/ort</span><span class="sxs-lookup"><span data-stu-id="9d823-442">paspoort</span></span>  <br/> <span data-ttu-id="9d823-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="9d823-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="9d823-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="9d823-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="9d823-445">폴란드</span><span class="sxs-lookup"><span data-stu-id="9d823-445">Poland</span></span>

<span data-ttu-id="9d823-446">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"폴란드 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9d823-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="9d823-447">포르투갈</span><span class="sxs-lookup"><span data-stu-id="9d823-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="9d823-448">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-448">Format</span></span>

<span data-ttu-id="9d823-449">공백 또는 구분 기호가 없는 한 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-450">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-450">Pattern</span></span>

<span data-ttu-id="9d823-451">1 개의 문자 다음에 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="9d823-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="9d823-452">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="9d823-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="9d823-453">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9d823-454">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-454">Checksum</span></span>

<span data-ttu-id="9d823-455">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-456">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-456">Definition</span></span>

<span data-ttu-id="9d823-457">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-458">정규식이 해당 `Regex_portugal_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-459">from `Keywords_portugal_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-460">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-460">Keywords</span></span>

<span data-ttu-id="9d823-461">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-461"></span></span>
|<span data-ttu-id="9d823-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-463">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-463">passport number</span></span>  <br/> <span data-ttu-id="9d823-464">포르투갈어 passport 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="9d823-465">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-465">passport no</span></span>  <br/> <span data-ttu-id="9d823-466">número do passaporte</span><span class="sxs-lookup"><span data-stu-id="9d823-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="9d823-467">루마니아</span><span class="sxs-lookup"><span data-stu-id="9d823-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="9d823-468">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-468">Format</span></span>

<span data-ttu-id="9d823-469">공백과 구분 기호를 사용 하지 않고 8 또는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-470">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-470">Pattern</span></span>

<span data-ttu-id="9d823-471">8 또는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9d823-472">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-472">Checksum</span></span>

<span data-ttu-id="9d823-473">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-474">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-474">Definition</span></span>

<span data-ttu-id="9d823-475">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-476">정규식이 해당 `Regex_romania_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-477">from `Keywords_romania_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-478">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-478">Keywords</span></span>

<span data-ttu-id="9d823-479">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-479"></span></span>
|<span data-ttu-id="9d823-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-481">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-481">passport number</span></span>  <br/> <span data-ttu-id="9d823-482">루마니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-482">romanian passport number</span></span>  <br/> <span data-ttu-id="9d823-483">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-483">passport no</span></span>  <br/> <span data-ttu-id="9d823-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="9d823-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="9d823-485">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="9d823-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="9d823-486">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-486">Format</span></span>

<span data-ttu-id="9d823-487">공백 또는 구분 기호가 없는 한 자리 숫자 또는 문자 다음에 일곱 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-488">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-488">Pattern</span></span>

<span data-ttu-id="9d823-489">1 자리 숫자 또는 문자 (대/소문자 구분 안 함)와 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9d823-490">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-490">Checksum</span></span>

<span data-ttu-id="9d823-491">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-492">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-492">Definition</span></span>

<span data-ttu-id="9d823-493">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-494">정규식이 해당 `Regex_slovakia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-495">from `Keywords_slovakia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-496">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-496">Keywords</span></span>

<span data-ttu-id="9d823-497">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-497"></span></span>
|<span data-ttu-id="9d823-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-499">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-499">passport number</span></span>  <br/> <span data-ttu-id="9d823-500">슬로바키아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="9d823-501">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-501">passport no</span></span>  <br/> <span data-ttu-id="9d823-502">číslo (u)</span><span class="sxs-lookup"><span data-stu-id="9d823-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="9d823-503">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="9d823-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="9d823-504">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-504">Format</span></span>

<span data-ttu-id="9d823-505">공백 또는 구분 기호가 없는 7 자리, 두 문자</span><span class="sxs-lookup"><span data-stu-id="9d823-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-506">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-506">Pattern</span></span>

<span data-ttu-id="9d823-507">2 개 문자와 7 자리 숫자를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="9d823-508">"P" 문자</span><span class="sxs-lookup"><span data-stu-id="9d823-508">The letter "P"</span></span>
    
- <span data-ttu-id="9d823-509">대문자 1 개</span><span class="sxs-lookup"><span data-stu-id="9d823-509">One uppercase letter</span></span>
    
- <span data-ttu-id="9d823-510">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9d823-511">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-511">Checksum</span></span>

<span data-ttu-id="9d823-512">아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-513">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-513">Definition</span></span>

<span data-ttu-id="9d823-514">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-515">정규식이 해당 `Regex_slovenia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-516">from `Keywords_slovenia_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-517">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-517">Keywords</span></span>

<span data-ttu-id="9d823-518">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-518"></span></span>
|<span data-ttu-id="9d823-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-520">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-520">passport number</span></span>  <br/> <span data-ttu-id="9d823-521">슬로베니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="9d823-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="9d823-522">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-522">passport no</span></span>  <br/> <span data-ttu-id="9d823-523">številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="9d823-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="9d823-524">스페인</span><span class="sxs-lookup"><span data-stu-id="9d823-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="9d823-525">형식일</span><span class="sxs-lookup"><span data-stu-id="9d823-525">Format</span></span>

<span data-ttu-id="9d823-526">공백이 나 구분 기호가 없는 문자 및 숫자의 8 자리 또는 9 자 조합</span><span class="sxs-lookup"><span data-stu-id="9d823-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9d823-527">패턴</span><span class="sxs-lookup"><span data-stu-id="9d823-527">Pattern</span></span>

<span data-ttu-id="9d823-528">문자와 숫자의 8 자리 또는 9 자리 조합:</span><span class="sxs-lookup"><span data-stu-id="9d823-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="9d823-529">두 자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="9d823-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="9d823-530">1 자리 숫자 또는 문자 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="9d823-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="9d823-531">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="9d823-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9d823-532">제외</span><span class="sxs-lookup"><span data-stu-id="9d823-532">Checksum</span></span>

<span data-ttu-id="9d823-533">해당 없음</span><span class="sxs-lookup"><span data-stu-id="9d823-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9d823-534">정의</span><span class="sxs-lookup"><span data-stu-id="9d823-534">Definition</span></span>

<span data-ttu-id="9d823-535">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9d823-536">정규식이 해당 `Regex_spain_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9d823-537">from `Keywords_spain_eu_passport_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9d823-538">키워드</span><span class="sxs-lookup"><span data-stu-id="9d823-538">Keywords</span></span>

<span data-ttu-id="9d823-539">| |</span><span class="sxs-lookup"><span data-stu-id="9d823-539"></span></span>
|<span data-ttu-id="9d823-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="9d823-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="9d823-541">여권</span><span class="sxs-lookup"><span data-stu-id="9d823-541">passport</span></span>  <br/> <span data-ttu-id="9d823-542">스페인 여권</span><span class="sxs-lookup"><span data-stu-id="9d823-542">spain passport</span></span>  <br/> <span data-ttu-id="9d823-543">passport 책</span><span class="sxs-lookup"><span data-stu-id="9d823-543">passport book</span></span>  <br/> <span data-ttu-id="9d823-544">passport number</span><span class="sxs-lookup"><span data-stu-id="9d823-544">passport number</span></span>  <br/> <span data-ttu-id="9d823-545">passport 아니요</span><span class="sxs-lookup"><span data-stu-id="9d823-545">passport no</span></span>  <br/> <span data-ttu-id="9d823-546">pasaporte</span><span class="sxs-lookup"><span data-stu-id="9d823-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="9d823-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="9d823-547">número pasaporte</span></span>  <br/> <span data-ttu-id="9d823-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="9d823-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="9d823-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="9d823-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="9d823-550">스웨덴</span><span class="sxs-lookup"><span data-stu-id="9d823-550">Sweden</span></span>

<span data-ttu-id="9d823-551">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"스웨덴 여권 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9d823-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="9d823-552">영국의</span><span class="sxs-lookup"><span data-stu-id="9d823-552">UK</span></span>

<span data-ttu-id="9d823-553">자세한 내용은 "미국/영국" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9d823-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="9d823-554">[중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)Passport 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="9d823-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9d823-555">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9d823-555">See also</span></span>

[<span data-ttu-id="9d823-556">중요한 정보 유형이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="9d823-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

