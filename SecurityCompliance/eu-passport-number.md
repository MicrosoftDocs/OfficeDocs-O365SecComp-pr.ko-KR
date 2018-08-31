---
title: EU 여권 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 8c00df57-9fb3-459c-ba87-40480c87bd55
description: 이 항목에서는 EU 여권 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
ms.openlocfilehash: 71acc39b885c057e1771ec13b2f3c25017ac1bb6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533582"
---
# <a name="eu-passport-number"></a><span data-ttu-id="dc081-104">EU 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-104">EU Passport Number</span></span>

<span data-ttu-id="dc081-p102">이 항목에서는 EU 여권 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="dc081-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="dc081-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="dc081-108">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-108">Format</span></span>

<span data-ttu-id="dc081-109">선택 하는 공간 및 7 자리 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="dc081-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-110">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-110">Pattern</span></span>

<span data-ttu-id="dc081-111">하나의 문자, 7 자리 숫자 및 하나의 공간 조합:</span><span class="sxs-lookup"><span data-stu-id="dc081-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="dc081-112">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="dc081-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="dc081-113">하나의 공간 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="dc081-113">One space (optional)</span></span>
    
- <span data-ttu-id="dc081-114">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dc081-115">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-115">Checksum</span></span>

<span data-ttu-id="dc081-116">해당 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-117">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-117">Definition</span></span>

<span data-ttu-id="dc081-118">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-119">정규식 `Regex_austria_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-120">키워드에서 `Keywords_austria_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-121">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-121">Keywords</span></span>

<span data-ttu-id="dc081-122">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-122"></span></span>
|<span data-ttu-id="dc081-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-124">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-124">passport number</span></span>  <br/> <span data-ttu-id="dc081-125">오스트리아 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-125">austrian passport number</span></span>  <br/> <span data-ttu-id="dc081-126">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-126">passport no</span></span>  <br/> <span data-ttu-id="dc081-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="dc081-127">reisepass</span></span>  <br/> <span data-ttu-id="dc081-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="dc081-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="dc081-129">벨기에</span><span class="sxs-lookup"><span data-stu-id="dc081-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="dc081-130">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-130">Format</span></span>

<span data-ttu-id="dc081-131">공백이 나 구분 기호 없이 6 자리 숫자 앞에 오는 두 문자</span><span class="sxs-lookup"><span data-stu-id="dc081-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-132">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-132">Pattern</span></span>

<span data-ttu-id="dc081-133">처음 두 6 자리 숫자 앞에 오는 하 고</span><span class="sxs-lookup"><span data-stu-id="dc081-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dc081-134">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-134">Checksum</span></span>

<span data-ttu-id="dc081-135">해당 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-136">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-136">Definition</span></span>

<span data-ttu-id="dc081-137">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-138">정규식 `Regex_belgium_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-139">키워드에서 `Keywords_belgium_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-140">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-140">Keywords</span></span>

<span data-ttu-id="dc081-141">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-141"></span></span>
|<span data-ttu-id="dc081-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-143">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-143">passport number</span></span>  <br/> <span data-ttu-id="dc081-144">벨기에 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-144">belgian passport number</span></span>  <br/> <span data-ttu-id="dc081-145">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-145">passport no</span></span>  <br/> <span data-ttu-id="dc081-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="dc081-146">paspoort</span></span>  <br/> <span data-ttu-id="dc081-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="dc081-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="dc081-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="dc081-148">reisepass kein</span></span>  <br/> <span data-ttu-id="dc081-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="dc081-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="dc081-150">불가리아</span><span class="sxs-lookup"><span data-stu-id="dc081-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="dc081-151">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-151">Format</span></span>

<span data-ttu-id="dc081-152">공백 및 구분 기호 없이 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="dc081-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-153">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-153">Pattern</span></span>

 <span data-ttu-id="dc081-154">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="dc081-155">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-155">Checksum</span></span>

<span data-ttu-id="dc081-156">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-157">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-157">Definition</span></span>

<span data-ttu-id="dc081-158">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-159">정규식 `Regex_bulgaria_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-160">키워드에서 `Keywords_bulgaria_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-161">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-161">Keywords</span></span>

<span data-ttu-id="dc081-162">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-162"></span></span>
|<span data-ttu-id="dc081-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-164">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-164">passport number</span></span>  <br/> <span data-ttu-id="dc081-165">불가리아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="dc081-166">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-166">passport no</span></span>  <br/> <span data-ttu-id="dc081-167">НОМЕР НА ПАСПОРТА</span><span class="sxs-lookup"><span data-stu-id="dc081-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="dc081-168">크로아티아</span><span class="sxs-lookup"><span data-stu-id="dc081-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="dc081-169">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-169">Format</span></span>

<span data-ttu-id="dc081-170">공백 및 구분 기호 없이 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="dc081-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-171">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-171">Pattern</span></span>

 <span data-ttu-id="dc081-172">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="dc081-173">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-173">Checksum</span></span>

<span data-ttu-id="dc081-174">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-175">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-175">Definition</span></span>

<span data-ttu-id="dc081-176">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-177">정규식 `Regex_croatia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-178">키워드에서 `Keywords_croatia_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-179">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-179">Keywords</span></span>

<span data-ttu-id="dc081-180">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-180"></span></span>
|<span data-ttu-id="dc081-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-182">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-182">passport number</span></span>  <br/> <span data-ttu-id="dc081-183">크로아티아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-183">croatian passport number</span></span>  <br/> <span data-ttu-id="dc081-184">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-184">passport no</span></span>  <br/> <span data-ttu-id="dc081-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="dc081-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="dc081-186">키프로스</span><span class="sxs-lookup"><span data-stu-id="dc081-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="dc081-187">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-187">Format</span></span>

<span data-ttu-id="dc081-188">공백이 나 구분 기호 없이 6-8 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="dc081-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-189">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-189">Pattern</span></span>

<span data-ttu-id="dc081-190">6 ~ 8 개의 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="dc081-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dc081-191">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-191">Checksum</span></span>

<span data-ttu-id="dc081-192">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-193">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-193">Definition</span></span>

<span data-ttu-id="dc081-194">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-195">정규식 `Regex_cyprus_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-196">키워드에서 `Keywords_cyprus_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-197">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-197">Keywords</span></span>

<span data-ttu-id="dc081-198">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-198"></span></span>
|<span data-ttu-id="dc081-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-200">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-200">passport number</span></span>  <br/> <span data-ttu-id="dc081-201">키프로스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="dc081-202">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-202">passport no</span></span>  <br/> <span data-ttu-id="dc081-203">ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ</span><span class="sxs-lookup"><span data-stu-id="dc081-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="dc081-204">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="dc081-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="dc081-205">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-205">Format</span></span>

<span data-ttu-id="dc081-206">공백이 나 구분 기호 없이 8 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-207">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-207">Pattern</span></span>

<span data-ttu-id="dc081-208">공백이 나 구분 기호 없이 8 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dc081-209">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-209">Checksum</span></span>

<span data-ttu-id="dc081-210">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-211">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-211">Definition</span></span>

<span data-ttu-id="dc081-212">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-213">정규식 `Regex_czech_republic_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-214">키워드에서 `Keywords_czech_republic_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-215">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-215">Keywords</span></span>

<span data-ttu-id="dc081-216">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-216"></span></span>
|<span data-ttu-id="dc081-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-218">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-218">passport number</span></span>  <br/> <span data-ttu-id="dc081-219">체코어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-219">czech passport number</span></span>  <br/> <span data-ttu-id="dc081-220">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-220">passport no</span></span>  <br/> <span data-ttu-id="dc081-221">cestovní pas</span><span class="sxs-lookup"><span data-stu-id="dc081-221">cestovní pas</span></span>  <br/> <span data-ttu-id="dc081-222">pas</span><span class="sxs-lookup"><span data-stu-id="dc081-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="dc081-223">덴마크</span><span class="sxs-lookup"><span data-stu-id="dc081-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="dc081-224">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-224">Format</span></span>

<span data-ttu-id="dc081-225">공백 및 구분 기호 없이 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="dc081-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-226">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-226">Pattern</span></span>

 <span data-ttu-id="dc081-227">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="dc081-228">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-228">Checksum</span></span>

<span data-ttu-id="dc081-229">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-230">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-230">Definition</span></span>

<span data-ttu-id="dc081-231">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-232">정규식 `Regex_denmark_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-233">키워드에서 `Keywords_denmark_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-234">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-234">Keywords</span></span>

<span data-ttu-id="dc081-235">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-235"></span></span>
|<span data-ttu-id="dc081-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-237">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-237">passport number</span></span>  <br/> <span data-ttu-id="dc081-238">덴마크어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-238">danish passport number</span></span>  <br/> <span data-ttu-id="dc081-239">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-239">passport no</span></span>  <br/> <span data-ttu-id="dc081-240">pas</span><span class="sxs-lookup"><span data-stu-id="dc081-240">pas</span></span>  <br/> <span data-ttu-id="dc081-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="dc081-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="dc081-242">에스토니아</span><span class="sxs-lookup"><span data-stu-id="dc081-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="dc081-243">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-243">Format</span></span>

<span data-ttu-id="dc081-244">공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="dc081-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-245">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-245">Pattern</span></span>

<span data-ttu-id="dc081-246">7 자리 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="dc081-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dc081-247">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-247">Checksum</span></span>

<span data-ttu-id="dc081-248">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-249">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-249">Definition</span></span>

<span data-ttu-id="dc081-250">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-251">정규식 `Regex_estonia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-252">키워드에서 `Keywords_estonia_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-253">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-253">Keywords</span></span>

<span data-ttu-id="dc081-254">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-254"></span></span>
|<span data-ttu-id="dc081-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-256">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-256">passport number</span></span>  <br/> <span data-ttu-id="dc081-257">에스토니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-257">estonian passport number</span></span>  <br/> <span data-ttu-id="dc081-258">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-258">passport no</span></span>  <br/> <span data-ttu-id="dc081-259">eesti kodaniku 통과</span><span class="sxs-lookup"><span data-stu-id="dc081-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="dc081-260">핀란드</span><span class="sxs-lookup"><span data-stu-id="dc081-260">Finland</span></span>

<span data-ttu-id="dc081-261">자세한 내용은의 섹션을 참조 "핀란드 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="dc081-262">프랑스</span><span class="sxs-lookup"><span data-stu-id="dc081-262">France</span></span>

<span data-ttu-id="dc081-263">자세한 내용은의 섹션을 참조 "프랑스 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="dc081-264">독일</span><span class="sxs-lookup"><span data-stu-id="dc081-264">Germany</span></span>

<span data-ttu-id="dc081-265">자세한 내용은의 섹션을 참조 "독일 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="dc081-266">그리스</span><span class="sxs-lookup"><span data-stu-id="dc081-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="dc081-267">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-267">Format</span></span>

<span data-ttu-id="dc081-268">공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 두 문자</span><span class="sxs-lookup"><span data-stu-id="dc081-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-269">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-269">Pattern</span></span>

<span data-ttu-id="dc081-270">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dc081-271">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-271">Checksum</span></span>

<span data-ttu-id="dc081-272">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-273">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-273">Definition</span></span>

<span data-ttu-id="dc081-274">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-275">정규식 `Regex_greece_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-276">키워드에서 `Keywords_greece_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-277">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-277">Keywords</span></span>

<span data-ttu-id="dc081-278">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-278"></span></span>
|<span data-ttu-id="dc081-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-280">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-280">passport number</span></span>  <br/> <span data-ttu-id="dc081-281">그리스어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-281">greek passport number</span></span>  <br/> <span data-ttu-id="dc081-282">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-282">passport no</span></span>  <br/> <span data-ttu-id="dc081-283">ΔΙΑΒΑΤΗΡΙΟ</span><span class="sxs-lookup"><span data-stu-id="dc081-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="dc081-284">헝가리</span><span class="sxs-lookup"><span data-stu-id="dc081-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="dc081-285">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-285">Format</span></span>

<span data-ttu-id="dc081-286">공백이 나 구분 기호 없이 6 또는 7 자리 숫자 앞에 오는 두 문자</span><span class="sxs-lookup"><span data-stu-id="dc081-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-287">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-287">Pattern</span></span>

<span data-ttu-id="dc081-288">6 또는 7 자리 숫자 앞에 오는 두 문자</span><span class="sxs-lookup"><span data-stu-id="dc081-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dc081-289">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-289">Checksum</span></span>

<span data-ttu-id="dc081-290">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-291">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-291">Definition</span></span>

<span data-ttu-id="dc081-292">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-293">정규식 `Regex_hungary_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-294">키워드에서 `Keywords_hungary_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-295">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-295">Keywords</span></span>

<span data-ttu-id="dc081-296">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-296"></span></span>
|<span data-ttu-id="dc081-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-298">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-298">passport number</span></span>  <br/> <span data-ttu-id="dc081-299">헝가리어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="dc081-300">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-300">passport no</span></span>  <br/> <span data-ttu-id="dc081-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="dc081-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="dc081-302">Ireland</span><span class="sxs-lookup"><span data-stu-id="dc081-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="dc081-303">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-303">Format</span></span>

<span data-ttu-id="dc081-304">두 문자나 공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-305">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-305">Pattern</span></span>

<span data-ttu-id="dc081-306">두 문자 또는 7 자리 숫자 앞에 오는 숫자:</span><span class="sxs-lookup"><span data-stu-id="dc081-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="dc081-307">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="dc081-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="dc081-308">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dc081-309">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-309">Checksum</span></span>

<span data-ttu-id="dc081-310">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-311">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-311">Definition</span></span>

<span data-ttu-id="dc081-312">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-313">정규식 `Regex_ireland_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-314">키워드에서 `Keywords_ireland_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-315">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-315">Keywords</span></span>

<span data-ttu-id="dc081-316">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-316"></span></span>
|<span data-ttu-id="dc081-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-318">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-318">passport number</span></span>  <br/> <span data-ttu-id="dc081-319">아일랜드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-319">irish passport number</span></span>  <br/> <span data-ttu-id="dc081-320">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-320">passport no</span></span>  <br/> <span data-ttu-id="dc081-321">pas</span><span class="sxs-lookup"><span data-stu-id="dc081-321">pas</span></span>  <br/> <span data-ttu-id="dc081-322">passport</span><span class="sxs-lookup"><span data-stu-id="dc081-322">passport</span></span>  <br/> <span data-ttu-id="dc081-323">passeport</span><span class="sxs-lookup"><span data-stu-id="dc081-323">passeport</span></span>  <br/> <span data-ttu-id="dc081-324">passeport numero</span><span class="sxs-lookup"><span data-stu-id="dc081-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="dc081-325">이탈리아</span><span class="sxs-lookup"><span data-stu-id="dc081-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="dc081-326">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-326">Format</span></span>

<span data-ttu-id="dc081-327">두 문자나 공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-328">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-328">Pattern</span></span>

<span data-ttu-id="dc081-329">두 문자 또는 7 자리 숫자 앞에 오는 숫자:</span><span class="sxs-lookup"><span data-stu-id="dc081-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="dc081-330">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="dc081-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="dc081-331">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dc081-332">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-332">Checksum</span></span>

<span data-ttu-id="dc081-333">해당 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-334">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-334">Definition</span></span>

<span data-ttu-id="dc081-335">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-336">정규식 `Regex_italy_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-337">키워드에서 `Keywords_italy_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-338">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-338">Keywords</span></span>

<span data-ttu-id="dc081-339">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-339"></span></span>
|<span data-ttu-id="dc081-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-341">이탈리아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-341">italian passport number</span></span>  <br/> <span data-ttu-id="dc081-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="dc081-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="dc081-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="dc081-343">passaporto</span></span>  <br/> <span data-ttu-id="dc081-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="dc081-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="dc081-345">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-345">passport number</span></span>  <br/> <span data-ttu-id="dc081-346">italiana passaporto numero</span><span class="sxs-lookup"><span data-stu-id="dc081-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="dc081-347">passaporto numero</span><span class="sxs-lookup"><span data-stu-id="dc081-347">passaporto numero</span></span>  <br/> <span data-ttu-id="dc081-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="dc081-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="dc081-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="dc081-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="dc081-350">라트비아</span><span class="sxs-lookup"><span data-stu-id="dc081-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="dc081-351">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-351">Format</span></span>

<span data-ttu-id="dc081-352">두 문자나 공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-353">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-353">Pattern</span></span>

<span data-ttu-id="dc081-354">두 문자 또는 7 자리 숫자 앞에 오는 숫자:</span><span class="sxs-lookup"><span data-stu-id="dc081-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="dc081-355">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="dc081-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="dc081-356">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dc081-357">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-357">Checksum</span></span>

<span data-ttu-id="dc081-358">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-359">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-359">Definition</span></span>

<span data-ttu-id="dc081-360">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-361">정규식 `Regex_latvia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-362">키워드에서 `Keywords_latvia_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-363">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-363">Keywords</span></span>

<span data-ttu-id="dc081-364">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-364"></span></span>
|<span data-ttu-id="dc081-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-366">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-366">passport number</span></span>  <br/> <span data-ttu-id="dc081-367">라트비아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-367">latvian passport number</span></span>  <br/> <span data-ttu-id="dc081-368">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-368">passport no</span></span>  <br/> <span data-ttu-id="dc081-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="dc081-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="dc081-370">리투아니아</span><span class="sxs-lookup"><span data-stu-id="dc081-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="dc081-371">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-371">Format</span></span>

<span data-ttu-id="dc081-372">8 개의 숫자 또는 공백이 나 구분 기호 없이 문자</span><span class="sxs-lookup"><span data-stu-id="dc081-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-373">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-373">Pattern</span></span>

<span data-ttu-id="dc081-374">8 개의 숫자 또는 문자 (하지 대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="dc081-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dc081-375">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-375">Checksum</span></span>

<span data-ttu-id="dc081-376">해당 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-377">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-377">Definition</span></span>

<span data-ttu-id="dc081-378">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-379">정규식 `Regex_lithuania_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-380">키워드에서 `Keywords_lithuania_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-381">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-381">Keywords</span></span>

<span data-ttu-id="dc081-382">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-382"></span></span>
|<span data-ttu-id="dc081-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-384">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-384">passport number</span></span>  <br/> <span data-ttu-id="dc081-385">lithunian 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="dc081-386">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-386">passport no</span></span>  <br/> <span data-ttu-id="dc081-387">paso numeris</span><span class="sxs-lookup"><span data-stu-id="dc081-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="dc081-388">룩셈부르크</span><span class="sxs-lookup"><span data-stu-id="dc081-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="dc081-389">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-389">Format</span></span>

<span data-ttu-id="dc081-390">8 개의 숫자 또는 공백이 나 구분 기호 없이 문자</span><span class="sxs-lookup"><span data-stu-id="dc081-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-391">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-391">Pattern</span></span>

<span data-ttu-id="dc081-392">8 개의 숫자 또는 문자 (하지 대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="dc081-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dc081-393">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-393">Checksum</span></span>

<span data-ttu-id="dc081-394">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-395">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-395">Definition</span></span>

<span data-ttu-id="dc081-396">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-397">정규식 `Regex_nation_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-398">키워드에서 `Keywords_nation_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-399">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-399">Keywords</span></span>

<span data-ttu-id="dc081-400">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-400"></span></span>
|<span data-ttu-id="dc081-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-402">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-402">passport number</span></span>  <br/> <span data-ttu-id="dc081-403">라트비아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-403">latvian passport number</span></span>  <br/> <span data-ttu-id="dc081-404">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-404">passport no</span></span>  <br/> <span data-ttu-id="dc081-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="dc081-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="dc081-406">몰타</span><span class="sxs-lookup"><span data-stu-id="dc081-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="dc081-407">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-407">Format</span></span>

<span data-ttu-id="dc081-408">공백이 나 구분 하지 않고 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-409">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-409">Pattern</span></span>

 <span data-ttu-id="dc081-410">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="dc081-411">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-411">Checksum</span></span>

<span data-ttu-id="dc081-412">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-413">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-413">Definition</span></span>

<span data-ttu-id="dc081-414">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-415">정규식 `Regex_malta_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-416">키워드에서 `Keywords_malta_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-417">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-417">Keywords</span></span>

<span data-ttu-id="dc081-418">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-418"></span></span>
|<span data-ttu-id="dc081-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-420">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-420">passport number</span></span>  <br/> <span data-ttu-id="dc081-421">몰타어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-421">maltese passport number</span></span>  <br/> <span data-ttu-id="dc081-422">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-422">passport no</span></span>  <br/> <span data-ttu-id="dc081-423">numru tal passaport</span><span class="sxs-lookup"><span data-stu-id="dc081-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="dc081-424">네덜란드</span><span class="sxs-lookup"><span data-stu-id="dc081-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="dc081-425">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-425">Format</span></span>

<span data-ttu-id="dc081-426">9 개의 문자나 공백이 나 구분 기호 없이 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-427">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-427">Pattern</span></span>

<span data-ttu-id="dc081-428">9 개의 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dc081-429">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-429">Checksum</span></span>

<span data-ttu-id="dc081-430">해당 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-431">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-431">Definition</span></span>

<span data-ttu-id="dc081-432">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-433">정규식 `Regex_netherlands_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-434">키워드에서 `Keywords_netherlands_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-435">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-435">Keywords</span></span>

<span data-ttu-id="dc081-436">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-436"></span></span>
|<span data-ttu-id="dc081-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-438">네덜란드어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-438">dutch passport number</span></span>  <br/> <span data-ttu-id="dc081-439">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-439">passport number</span></span>  <br/> <span data-ttu-id="dc081-440">네덜란드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="dc081-441">nederlanden paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="dc081-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="dc081-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="dc081-442">paspoort</span></span>  <br/> <span data-ttu-id="dc081-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="dc081-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="dc081-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="dc081-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="dc081-445">폴란드</span><span class="sxs-lookup"><span data-stu-id="dc081-445">Poland</span></span>

<span data-ttu-id="dc081-446">자세한 내용은의 섹션을 참조 "폴란드 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="dc081-447">포르투갈</span><span class="sxs-lookup"><span data-stu-id="dc081-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="dc081-448">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-448">Format</span></span>

<span data-ttu-id="dc081-449">공백이 나 구분 기호 없이 6 자리 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="dc081-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-450">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-450">Pattern</span></span>

<span data-ttu-id="dc081-451">6 자리 숫자 앞에 오는 문자 하나:</span><span class="sxs-lookup"><span data-stu-id="dc081-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="dc081-452">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="dc081-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="dc081-453">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dc081-454">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-454">Checksum</span></span>

<span data-ttu-id="dc081-455">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-456">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-456">Definition</span></span>

<span data-ttu-id="dc081-457">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-458">정규식 `Regex_portugal_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-459">키워드에서 `Keywords_portugal_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-460">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-460">Keywords</span></span>

<span data-ttu-id="dc081-461">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-461"></span></span>
|<span data-ttu-id="dc081-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-463">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-463">passport number</span></span>  <br/> <span data-ttu-id="dc081-464">포르투갈어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-464">portugese passport number</span></span>  <br/> <span data-ttu-id="dc081-465">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-465">passport no</span></span>  <br/> <span data-ttu-id="dc081-466">número do passaporte</span><span class="sxs-lookup"><span data-stu-id="dc081-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="dc081-467">루마니아</span><span class="sxs-lookup"><span data-stu-id="dc081-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="dc081-468">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-468">Format</span></span>

<span data-ttu-id="dc081-469">공백 및 구분 기호 없이 8 또는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-470">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-470">Pattern</span></span>

<span data-ttu-id="dc081-471">8 또는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dc081-472">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-472">Checksum</span></span>

<span data-ttu-id="dc081-473">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-474">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-474">Definition</span></span>

<span data-ttu-id="dc081-475">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-476">정규식 `Regex_romania_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-477">키워드에서 `Keywords_romania_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-478">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-478">Keywords</span></span>

<span data-ttu-id="dc081-479">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-479"></span></span>
|<span data-ttu-id="dc081-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-481">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-481">passport number</span></span>  <br/> <span data-ttu-id="dc081-482">루마니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-482">romanian passport number</span></span>  <br/> <span data-ttu-id="dc081-483">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-483">passport no</span></span>  <br/> <span data-ttu-id="dc081-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="dc081-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="dc081-485">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="dc081-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="dc081-486">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-486">Format</span></span>

<span data-ttu-id="dc081-487">한 자리 숫자 또는 공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 문자</span><span class="sxs-lookup"><span data-stu-id="dc081-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-488">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-488">Pattern</span></span>

<span data-ttu-id="dc081-489">한 자리 또는 7 자리 숫자 앞에 오는 문자 (하지 대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="dc081-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dc081-490">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-490">Checksum</span></span>

<span data-ttu-id="dc081-491">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-492">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-492">Definition</span></span>

<span data-ttu-id="dc081-493">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-494">정규식 `Regex_slovakia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-495">키워드에서 `Keywords_slovakia_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-496">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-496">Keywords</span></span>

<span data-ttu-id="dc081-497">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-497"></span></span>
|<span data-ttu-id="dc081-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-499">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-499">passport number</span></span>  <br/> <span data-ttu-id="dc081-500">슬로바키아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="dc081-501">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-501">passport no</span></span>  <br/> <span data-ttu-id="dc081-502">Číslo pasu</span><span class="sxs-lookup"><span data-stu-id="dc081-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="dc081-503">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="dc081-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="dc081-504">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-504">Format</span></span>

<span data-ttu-id="dc081-505">공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 두 문자</span><span class="sxs-lookup"><span data-stu-id="dc081-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-506">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-506">Pattern</span></span>

<span data-ttu-id="dc081-507">7 자리 숫자 앞에 오는 두 문자 수:</span><span class="sxs-lookup"><span data-stu-id="dc081-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="dc081-508">문자 "P"</span><span class="sxs-lookup"><span data-stu-id="dc081-508">The letter "P"</span></span>
    
- <span data-ttu-id="dc081-509">하나의 대문자</span><span class="sxs-lookup"><span data-stu-id="dc081-509">One uppercase letter</span></span>
    
- <span data-ttu-id="dc081-510">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dc081-511">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-511">Checksum</span></span>

<span data-ttu-id="dc081-512">없음</span><span class="sxs-lookup"><span data-stu-id="dc081-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-513">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-513">Definition</span></span>

<span data-ttu-id="dc081-514">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-515">정규식 `Regex_slovenia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-516">키워드에서 `Keywords_slovenia_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-517">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-517">Keywords</span></span>

<span data-ttu-id="dc081-518">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-518"></span></span>
|<span data-ttu-id="dc081-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-520">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-520">passport number</span></span>  <br/> <span data-ttu-id="dc081-521">슬로베니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="dc081-522">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-522">passport no</span></span>  <br/> <span data-ttu-id="dc081-523">Številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="dc081-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="dc081-524">스페인</span><span class="sxs-lookup"><span data-stu-id="dc081-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="dc081-525">형식</span><span class="sxs-lookup"><span data-stu-id="dc081-525">Format</span></span>

<span data-ttu-id="dc081-526">문자와 공백이 나 구분 기호 없이 숫자는 8 또는 9 개 문자 조합</span><span class="sxs-lookup"><span data-stu-id="dc081-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dc081-527">패턴</span><span class="sxs-lookup"><span data-stu-id="dc081-527">Pattern</span></span>

<span data-ttu-id="dc081-528">문자와 숫자는 8 또는 9 개 문자 조합 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="dc081-529">두 자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="dc081-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="dc081-530">한 자리 숫자 또는 문자 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="dc081-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="dc081-531">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="dc081-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dc081-532">체크섬</span><span class="sxs-lookup"><span data-stu-id="dc081-532">Checksum</span></span>

<span data-ttu-id="dc081-533">해당 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="dc081-534">정의</span><span class="sxs-lookup"><span data-stu-id="dc081-534">Definition</span></span>

<span data-ttu-id="dc081-535">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dc081-536">정규식 `Regex_spain_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dc081-537">키워드에서 `Keywords_spain_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc081-538">키워드</span><span class="sxs-lookup"><span data-stu-id="dc081-538">Keywords</span></span>

<span data-ttu-id="dc081-539">| |</span><span class="sxs-lookup"><span data-stu-id="dc081-539"></span></span>
|<span data-ttu-id="dc081-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="dc081-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="dc081-541">passport</span><span class="sxs-lookup"><span data-stu-id="dc081-541">passport</span></span>  <br/> <span data-ttu-id="dc081-542">스페인 passport</span><span class="sxs-lookup"><span data-stu-id="dc081-542">spain passport</span></span>  <br/> <span data-ttu-id="dc081-543">passport도 서</span><span class="sxs-lookup"><span data-stu-id="dc081-543">passport book</span></span>  <br/> <span data-ttu-id="dc081-544">여권 번호</span><span class="sxs-lookup"><span data-stu-id="dc081-544">passport number</span></span>  <br/> <span data-ttu-id="dc081-545">passport 없음</span><span class="sxs-lookup"><span data-stu-id="dc081-545">passport no</span></span>  <br/> <span data-ttu-id="dc081-546">libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="dc081-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="dc081-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="dc081-547">número pasaporte</span></span>  <br/> <span data-ttu-id="dc081-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="dc081-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="dc081-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="dc081-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="dc081-550">스웨덴</span><span class="sxs-lookup"><span data-stu-id="dc081-550">Sweden</span></span>

<span data-ttu-id="dc081-551">자세한 내용은의 섹션을 참조 "스웨덴 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="dc081-552">영국</span><span class="sxs-lookup"><span data-stu-id="dc081-552">UK</span></span>

<span data-ttu-id="dc081-p103">자세한 내용은의 섹션을 참조 "미국/영국 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="dc081-p103">For details, see the section "U.S. / U.K. Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dc081-555">참고 항목</span><span class="sxs-lookup"><span data-stu-id="dc081-555">See also</span></span>

[<span data-ttu-id="dc081-556">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="dc081-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

