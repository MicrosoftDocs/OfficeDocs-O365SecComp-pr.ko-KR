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
ms.openlocfilehash: 7a7fc1ff826aab4096c46535686eb0fd68173c6f
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "25840327"
---
# <a name="eu-passport-number"></a><span data-ttu-id="afde0-104">EU 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-104">EU Passport Number</span></span>

<span data-ttu-id="afde0-p102">이 항목에서는 EU 여권 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="afde0-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="afde0-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="afde0-108">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-108">Format</span></span>

<span data-ttu-id="afde0-109">선택 하는 공간 및 7 자리 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="afde0-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-110">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-110">Pattern</span></span>

<span data-ttu-id="afde0-111">하나의 문자, 7 자리 숫자 및 하나의 공간 조합:</span><span class="sxs-lookup"><span data-stu-id="afde0-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="afde0-112">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="afde0-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="afde0-113">하나의 공간 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="afde0-113">One space (optional)</span></span>
    
- <span data-ttu-id="afde0-114">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="afde0-115">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-115">Checksum</span></span>

<span data-ttu-id="afde0-116">해당 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-117">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-117">Definition</span></span>

<span data-ttu-id="afde0-118">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-119">정규식 `Regex_austria_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-120">키워드에서 `Keywords_austria_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-121">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-121">Keywords</span></span>

<span data-ttu-id="afde0-122">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-122"></span></span>
|<span data-ttu-id="afde0-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-124">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-124">passport number</span></span>  <br/> <span data-ttu-id="afde0-125">오스트리아 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-125">austrian passport number</span></span>  <br/> <span data-ttu-id="afde0-126">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-126">passport no</span></span>  <br/> <span data-ttu-id="afde0-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="afde0-127">reisepass</span></span>  <br/> <span data-ttu-id="afde0-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="afde0-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="afde0-129">벨기에</span><span class="sxs-lookup"><span data-stu-id="afde0-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="afde0-130">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-130">Format</span></span>

<span data-ttu-id="afde0-131">공백이 나 구분 기호 없이 6 자리 숫자 앞에 오는 두 문자</span><span class="sxs-lookup"><span data-stu-id="afde0-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-132">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-132">Pattern</span></span>

<span data-ttu-id="afde0-133">처음 두 6 자리 숫자 앞에 오는 하 고</span><span class="sxs-lookup"><span data-stu-id="afde0-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="afde0-134">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-134">Checksum</span></span>

<span data-ttu-id="afde0-135">해당 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-136">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-136">Definition</span></span>

<span data-ttu-id="afde0-137">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-138">정규식 `Regex_belgium_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-139">키워드에서 `Keywords_belgium_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-140">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-140">Keywords</span></span>

<span data-ttu-id="afde0-141">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-141"></span></span>
|<span data-ttu-id="afde0-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-143">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-143">passport number</span></span>  <br/> <span data-ttu-id="afde0-144">벨기에 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-144">belgian passport number</span></span>  <br/> <span data-ttu-id="afde0-145">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-145">passport no</span></span>  <br/> <span data-ttu-id="afde0-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="afde0-146">paspoort</span></span>  <br/> <span data-ttu-id="afde0-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="afde0-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="afde0-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="afde0-148">reisepass kein</span></span>  <br/> <span data-ttu-id="afde0-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="afde0-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="afde0-150">불가리아</span><span class="sxs-lookup"><span data-stu-id="afde0-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="afde0-151">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-151">Format</span></span>

<span data-ttu-id="afde0-152">공백 및 구분 기호 없이 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="afde0-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-153">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-153">Pattern</span></span>

 <span data-ttu-id="afde0-154">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="afde0-155">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-155">Checksum</span></span>

<span data-ttu-id="afde0-156">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-157">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-157">Definition</span></span>

<span data-ttu-id="afde0-158">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-159">정규식 `Regex_bulgaria_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-160">키워드에서 `Keywords_bulgaria_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-161">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-161">Keywords</span></span>

<span data-ttu-id="afde0-162">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-162"></span></span>
|<span data-ttu-id="afde0-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-164">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-164">passport number</span></span>  <br/> <span data-ttu-id="afde0-165">불가리아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="afde0-166">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-166">passport no</span></span>  <br/> <span data-ttu-id="afde0-167">НОМЕР НА ПАСПОРТА</span><span class="sxs-lookup"><span data-stu-id="afde0-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="afde0-168">크로아티아</span><span class="sxs-lookup"><span data-stu-id="afde0-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="afde0-169">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-169">Format</span></span>

<span data-ttu-id="afde0-170">공백 및 구분 기호 없이 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="afde0-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-171">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-171">Pattern</span></span>

 <span data-ttu-id="afde0-172">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="afde0-173">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-173">Checksum</span></span>

<span data-ttu-id="afde0-174">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-175">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-175">Definition</span></span>

<span data-ttu-id="afde0-176">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-177">정규식 `Regex_croatia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-178">키워드에서 `Keywords_croatia_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-179">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-179">Keywords</span></span>

<span data-ttu-id="afde0-180">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-180"></span></span>
|<span data-ttu-id="afde0-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-182">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-182">passport number</span></span>  <br/> <span data-ttu-id="afde0-183">크로아티아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-183">croatian passport number</span></span>  <br/> <span data-ttu-id="afde0-184">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-184">passport no</span></span>  <br/> <span data-ttu-id="afde0-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="afde0-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="afde0-186">키프로스</span><span class="sxs-lookup"><span data-stu-id="afde0-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="afde0-187">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-187">Format</span></span>

<span data-ttu-id="afde0-188">공백이 나 구분 기호 없이 6-8 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="afde0-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-189">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-189">Pattern</span></span>

<span data-ttu-id="afde0-190">6 ~ 8 개의 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="afde0-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="afde0-191">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-191">Checksum</span></span>

<span data-ttu-id="afde0-192">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-193">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-193">Definition</span></span>

<span data-ttu-id="afde0-194">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-195">정규식 `Regex_cyprus_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-196">키워드에서 `Keywords_cyprus_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-197">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-197">Keywords</span></span>

<span data-ttu-id="afde0-198">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-198"></span></span>
|<span data-ttu-id="afde0-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-200">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-200">passport number</span></span>  <br/> <span data-ttu-id="afde0-201">키프로스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="afde0-202">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-202">passport no</span></span>  <br/> <span data-ttu-id="afde0-203">ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ</span><span class="sxs-lookup"><span data-stu-id="afde0-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="afde0-204">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="afde0-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="afde0-205">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-205">Format</span></span>

<span data-ttu-id="afde0-206">공백이 나 구분 기호 없이 8 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-207">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-207">Pattern</span></span>

<span data-ttu-id="afde0-208">공백이 나 구분 기호 없이 8 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="afde0-209">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-209">Checksum</span></span>

<span data-ttu-id="afde0-210">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-211">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-211">Definition</span></span>

<span data-ttu-id="afde0-212">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-213">정규식 `Regex_czech_republic_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-214">키워드에서 `Keywords_czech_republic_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-215">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-215">Keywords</span></span>

<span data-ttu-id="afde0-216">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-216"></span></span>
|<span data-ttu-id="afde0-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-218">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-218">passport number</span></span>  <br/> <span data-ttu-id="afde0-219">체코어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-219">czech passport number</span></span>  <br/> <span data-ttu-id="afde0-220">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-220">passport no</span></span>  <br/> <span data-ttu-id="afde0-221">cestovní pas</span><span class="sxs-lookup"><span data-stu-id="afde0-221">cestovní pas</span></span>  <br/> <span data-ttu-id="afde0-222">pas</span><span class="sxs-lookup"><span data-stu-id="afde0-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="afde0-223">덴마크</span><span class="sxs-lookup"><span data-stu-id="afde0-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="afde0-224">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-224">Format</span></span>

<span data-ttu-id="afde0-225">공백 및 구분 기호 없이 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="afde0-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-226">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-226">Pattern</span></span>

 <span data-ttu-id="afde0-227">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="afde0-228">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-228">Checksum</span></span>

<span data-ttu-id="afde0-229">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-230">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-230">Definition</span></span>

<span data-ttu-id="afde0-231">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-232">정규식 `Regex_denmark_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-233">키워드에서 `Keywords_denmark_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-234">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-234">Keywords</span></span>

<span data-ttu-id="afde0-235">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-235"></span></span>
|<span data-ttu-id="afde0-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-237">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-237">passport number</span></span>  <br/> <span data-ttu-id="afde0-238">덴마크어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-238">danish passport number</span></span>  <br/> <span data-ttu-id="afde0-239">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-239">passport no</span></span>  <br/> <span data-ttu-id="afde0-240">pas</span><span class="sxs-lookup"><span data-stu-id="afde0-240">pas</span></span>  <br/> <span data-ttu-id="afde0-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="afde0-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="afde0-242">에스토니아</span><span class="sxs-lookup"><span data-stu-id="afde0-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="afde0-243">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-243">Format</span></span>

<span data-ttu-id="afde0-244">공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="afde0-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-245">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-245">Pattern</span></span>

<span data-ttu-id="afde0-246">7 자리 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="afde0-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="afde0-247">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-247">Checksum</span></span>

<span data-ttu-id="afde0-248">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-249">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-249">Definition</span></span>

<span data-ttu-id="afde0-250">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-251">정규식 `Regex_estonia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-252">키워드에서 `Keywords_estonia_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-253">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-253">Keywords</span></span>

<span data-ttu-id="afde0-254">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-254"></span></span>
|<span data-ttu-id="afde0-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-256">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-256">passport number</span></span>  <br/> <span data-ttu-id="afde0-257">에스토니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-257">estonian passport number</span></span>  <br/> <span data-ttu-id="afde0-258">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-258">passport no</span></span>  <br/> <span data-ttu-id="afde0-259">eesti kodaniku 통과</span><span class="sxs-lookup"><span data-stu-id="afde0-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="afde0-260">핀란드</span><span class="sxs-lookup"><span data-stu-id="afde0-260">Finland</span></span>

<span data-ttu-id="afde0-261">자세한 내용은의 섹션을 참조 "핀란드 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="afde0-262">프랑스</span><span class="sxs-lookup"><span data-stu-id="afde0-262">France</span></span>

<span data-ttu-id="afde0-263">자세한 내용은의 섹션을 참조 "프랑스 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="afde0-264">독일</span><span class="sxs-lookup"><span data-stu-id="afde0-264">Germany</span></span>

<span data-ttu-id="afde0-265">자세한 내용은의 섹션을 참조 "독일 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="afde0-266">그리스</span><span class="sxs-lookup"><span data-stu-id="afde0-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="afde0-267">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-267">Format</span></span>

<span data-ttu-id="afde0-268">공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 두 문자</span><span class="sxs-lookup"><span data-stu-id="afde0-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-269">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-269">Pattern</span></span>

<span data-ttu-id="afde0-270">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="afde0-271">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-271">Checksum</span></span>

<span data-ttu-id="afde0-272">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-273">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-273">Definition</span></span>

<span data-ttu-id="afde0-274">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-275">정규식 `Regex_greece_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-276">키워드에서 `Keywords_greece_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-277">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-277">Keywords</span></span>

<span data-ttu-id="afde0-278">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-278"></span></span>
|<span data-ttu-id="afde0-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-280">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-280">passport number</span></span>  <br/> <span data-ttu-id="afde0-281">그리스어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-281">greek passport number</span></span>  <br/> <span data-ttu-id="afde0-282">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-282">passport no</span></span>  <br/> <span data-ttu-id="afde0-283">ΔΙΑΒΑΤΗΡΙΟ</span><span class="sxs-lookup"><span data-stu-id="afde0-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="afde0-284">헝가리</span><span class="sxs-lookup"><span data-stu-id="afde0-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="afde0-285">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-285">Format</span></span>

<span data-ttu-id="afde0-286">공백이 나 구분 기호 없이 6 또는 7 자리 숫자 앞에 오는 두 문자</span><span class="sxs-lookup"><span data-stu-id="afde0-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-287">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-287">Pattern</span></span>

<span data-ttu-id="afde0-288">6 또는 7 자리 숫자 앞에 오는 두 문자</span><span class="sxs-lookup"><span data-stu-id="afde0-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="afde0-289">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-289">Checksum</span></span>

<span data-ttu-id="afde0-290">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-291">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-291">Definition</span></span>

<span data-ttu-id="afde0-292">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-293">정규식 `Regex_hungary_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-294">키워드에서 `Keywords_hungary_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-295">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-295">Keywords</span></span>

<span data-ttu-id="afde0-296">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-296"></span></span>
|<span data-ttu-id="afde0-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-298">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-298">passport number</span></span>  <br/> <span data-ttu-id="afde0-299">헝가리어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="afde0-300">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-300">passport no</span></span>  <br/> <span data-ttu-id="afde0-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="afde0-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="afde0-302">Ireland</span><span class="sxs-lookup"><span data-stu-id="afde0-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="afde0-303">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-303">Format</span></span>

<span data-ttu-id="afde0-304">두 문자나 공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-305">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-305">Pattern</span></span>

<span data-ttu-id="afde0-306">두 문자 또는 7 자리 숫자 앞에 오는 숫자:</span><span class="sxs-lookup"><span data-stu-id="afde0-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="afde0-307">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="afde0-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="afde0-308">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="afde0-309">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-309">Checksum</span></span>

<span data-ttu-id="afde0-310">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-311">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-311">Definition</span></span>

<span data-ttu-id="afde0-312">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-313">정규식 `Regex_ireland_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-314">키워드에서 `Keywords_ireland_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-315">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-315">Keywords</span></span>

<span data-ttu-id="afde0-316">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-316"></span></span>
|<span data-ttu-id="afde0-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-318">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-318">passport number</span></span>  <br/> <span data-ttu-id="afde0-319">아일랜드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-319">irish passport number</span></span>  <br/> <span data-ttu-id="afde0-320">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-320">passport no</span></span>  <br/> <span data-ttu-id="afde0-321">pas</span><span class="sxs-lookup"><span data-stu-id="afde0-321">pas</span></span>  <br/> <span data-ttu-id="afde0-322">passport</span><span class="sxs-lookup"><span data-stu-id="afde0-322">passport</span></span>  <br/> <span data-ttu-id="afde0-323">passeport</span><span class="sxs-lookup"><span data-stu-id="afde0-323">passeport</span></span>  <br/> <span data-ttu-id="afde0-324">passeport numero</span><span class="sxs-lookup"><span data-stu-id="afde0-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="afde0-325">이탈리아</span><span class="sxs-lookup"><span data-stu-id="afde0-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="afde0-326">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-326">Format</span></span>

<span data-ttu-id="afde0-327">두 문자나 공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-328">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-328">Pattern</span></span>

<span data-ttu-id="afde0-329">두 문자 또는 7 자리 숫자 앞에 오는 숫자:</span><span class="sxs-lookup"><span data-stu-id="afde0-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="afde0-330">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="afde0-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="afde0-331">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="afde0-332">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-332">Checksum</span></span>

<span data-ttu-id="afde0-333">해당 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-334">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-334">Definition</span></span>

<span data-ttu-id="afde0-335">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-336">정규식 `Regex_italy_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-337">키워드에서 `Keywords_italy_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-338">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-338">Keywords</span></span>

<span data-ttu-id="afde0-339">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-339"></span></span>
|<span data-ttu-id="afde0-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-341">이탈리아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-341">italian passport number</span></span>  <br/> <span data-ttu-id="afde0-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="afde0-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="afde0-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="afde0-343">passaporto</span></span>  <br/> <span data-ttu-id="afde0-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="afde0-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="afde0-345">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-345">passport number</span></span>  <br/> <span data-ttu-id="afde0-346">italiana passaporto numero</span><span class="sxs-lookup"><span data-stu-id="afde0-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="afde0-347">passaporto numero</span><span class="sxs-lookup"><span data-stu-id="afde0-347">passaporto numero</span></span>  <br/> <span data-ttu-id="afde0-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="afde0-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="afde0-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="afde0-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="afde0-350">라트비아</span><span class="sxs-lookup"><span data-stu-id="afde0-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="afde0-351">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-351">Format</span></span>

<span data-ttu-id="afde0-352">두 문자나 공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-353">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-353">Pattern</span></span>

<span data-ttu-id="afde0-354">두 문자 또는 7 자리 숫자 앞에 오는 숫자:</span><span class="sxs-lookup"><span data-stu-id="afde0-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="afde0-355">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="afde0-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="afde0-356">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="afde0-357">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-357">Checksum</span></span>

<span data-ttu-id="afde0-358">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-359">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-359">Definition</span></span>

<span data-ttu-id="afde0-360">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-361">정규식 `Regex_latvia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-362">키워드에서 `Keywords_latvia_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-363">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-363">Keywords</span></span>

<span data-ttu-id="afde0-364">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-364"></span></span>
|<span data-ttu-id="afde0-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-366">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-366">passport number</span></span>  <br/> <span data-ttu-id="afde0-367">라트비아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-367">latvian passport number</span></span>  <br/> <span data-ttu-id="afde0-368">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-368">passport no</span></span>  <br/> <span data-ttu-id="afde0-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="afde0-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="afde0-370">리투아니아</span><span class="sxs-lookup"><span data-stu-id="afde0-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="afde0-371">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-371">Format</span></span>

<span data-ttu-id="afde0-372">8 개의 숫자 또는 공백이 나 구분 기호 없이 문자</span><span class="sxs-lookup"><span data-stu-id="afde0-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-373">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-373">Pattern</span></span>

<span data-ttu-id="afde0-374">8 개의 숫자 또는 문자 (하지 대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="afde0-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="afde0-375">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-375">Checksum</span></span>

<span data-ttu-id="afde0-376">해당 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-377">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-377">Definition</span></span>

<span data-ttu-id="afde0-378">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-379">정규식 `Regex_lithuania_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-380">키워드에서 `Keywords_lithuania_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-381">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-381">Keywords</span></span>

<span data-ttu-id="afde0-382">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-382"></span></span>
|<span data-ttu-id="afde0-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-384">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-384">passport number</span></span>  <br/> <span data-ttu-id="afde0-385">lithunian 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="afde0-386">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-386">passport no</span></span>  <br/> <span data-ttu-id="afde0-387">paso numeris</span><span class="sxs-lookup"><span data-stu-id="afde0-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="afde0-388">룩셈부르크</span><span class="sxs-lookup"><span data-stu-id="afde0-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="afde0-389">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-389">Format</span></span>

<span data-ttu-id="afde0-390">8 개의 숫자 또는 공백이 나 구분 기호 없이 문자</span><span class="sxs-lookup"><span data-stu-id="afde0-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-391">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-391">Pattern</span></span>

<span data-ttu-id="afde0-392">8 개의 숫자 또는 문자 (하지 대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="afde0-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="afde0-393">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-393">Checksum</span></span>

<span data-ttu-id="afde0-394">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-395">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-395">Definition</span></span>

<span data-ttu-id="afde0-396">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-397">정규식 `Regex_nation_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-398">키워드에서 `Keywords_nation_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-399">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-399">Keywords</span></span>

<span data-ttu-id="afde0-400">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-400"></span></span>
|<span data-ttu-id="afde0-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-402">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-402">passport number</span></span>  <br/> <span data-ttu-id="afde0-403">라트비아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-403">latvian passport number</span></span>  <br/> <span data-ttu-id="afde0-404">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-404">passport no</span></span>  <br/> <span data-ttu-id="afde0-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="afde0-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="afde0-406">몰타</span><span class="sxs-lookup"><span data-stu-id="afde0-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="afde0-407">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-407">Format</span></span>

<span data-ttu-id="afde0-408">공백이 나 구분 하지 않고 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-409">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-409">Pattern</span></span>

 <span data-ttu-id="afde0-410">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="afde0-411">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-411">Checksum</span></span>

<span data-ttu-id="afde0-412">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-413">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-413">Definition</span></span>

<span data-ttu-id="afde0-414">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-415">정규식 `Regex_malta_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-416">키워드에서 `Keywords_malta_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-417">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-417">Keywords</span></span>

<span data-ttu-id="afde0-418">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-418"></span></span>
|<span data-ttu-id="afde0-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-420">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-420">passport number</span></span>  <br/> <span data-ttu-id="afde0-421">몰타어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-421">maltese passport number</span></span>  <br/> <span data-ttu-id="afde0-422">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-422">passport no</span></span>  <br/> <span data-ttu-id="afde0-423">numru tal passaport</span><span class="sxs-lookup"><span data-stu-id="afde0-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="afde0-424">네덜란드</span><span class="sxs-lookup"><span data-stu-id="afde0-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="afde0-425">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-425">Format</span></span>

<span data-ttu-id="afde0-426">9 개의 문자나 공백이 나 구분 기호 없이 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-427">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-427">Pattern</span></span>

<span data-ttu-id="afde0-428">9 개의 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="afde0-429">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-429">Checksum</span></span>

<span data-ttu-id="afde0-430">해당 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-431">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-431">Definition</span></span>

<span data-ttu-id="afde0-432">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-433">정규식 `Regex_netherlands_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-434">키워드에서 `Keywords_netherlands_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-435">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-435">Keywords</span></span>

<span data-ttu-id="afde0-436">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-436"></span></span>
|<span data-ttu-id="afde0-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-438">네덜란드어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-438">dutch passport number</span></span>  <br/> <span data-ttu-id="afde0-439">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-439">passport number</span></span>  <br/> <span data-ttu-id="afde0-440">네덜란드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="afde0-441">nederlanden paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="afde0-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="afde0-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="afde0-442">paspoort</span></span>  <br/> <span data-ttu-id="afde0-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="afde0-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="afde0-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="afde0-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="afde0-445">폴란드</span><span class="sxs-lookup"><span data-stu-id="afde0-445">Poland</span></span>

<span data-ttu-id="afde0-446">자세한 내용은의 섹션을 참조 "폴란드 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="afde0-447">포르투갈</span><span class="sxs-lookup"><span data-stu-id="afde0-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="afde0-448">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-448">Format</span></span>

<span data-ttu-id="afde0-449">공백이 나 구분 기호 없이 6 자리 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="afde0-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-450">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-450">Pattern</span></span>

<span data-ttu-id="afde0-451">6 자리 숫자 앞에 오는 문자 하나:</span><span class="sxs-lookup"><span data-stu-id="afde0-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="afde0-452">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="afde0-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="afde0-453">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="afde0-454">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-454">Checksum</span></span>

<span data-ttu-id="afde0-455">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-456">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-456">Definition</span></span>

<span data-ttu-id="afde0-457">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-458">정규식 `Regex_portugal_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-459">키워드에서 `Keywords_portugal_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-460">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-460">Keywords</span></span>

<span data-ttu-id="afde0-461">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-461"></span></span>
|<span data-ttu-id="afde0-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-463">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-463">passport number</span></span>  <br/> <span data-ttu-id="afde0-464">포르투갈어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="afde0-465">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-465">passport no</span></span>  <br/> <span data-ttu-id="afde0-466">número do passaporte</span><span class="sxs-lookup"><span data-stu-id="afde0-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="afde0-467">루마니아</span><span class="sxs-lookup"><span data-stu-id="afde0-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="afde0-468">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-468">Format</span></span>

<span data-ttu-id="afde0-469">공백 및 구분 기호 없이 8 또는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-470">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-470">Pattern</span></span>

<span data-ttu-id="afde0-471">8 또는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="afde0-472">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-472">Checksum</span></span>

<span data-ttu-id="afde0-473">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-474">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-474">Definition</span></span>

<span data-ttu-id="afde0-475">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-476">정규식 `Regex_romania_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-477">키워드에서 `Keywords_romania_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-478">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-478">Keywords</span></span>

<span data-ttu-id="afde0-479">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-479"></span></span>
|<span data-ttu-id="afde0-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-481">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-481">passport number</span></span>  <br/> <span data-ttu-id="afde0-482">루마니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-482">romanian passport number</span></span>  <br/> <span data-ttu-id="afde0-483">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-483">passport no</span></span>  <br/> <span data-ttu-id="afde0-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="afde0-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="afde0-485">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="afde0-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="afde0-486">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-486">Format</span></span>

<span data-ttu-id="afde0-487">한 자리 숫자 또는 공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 문자</span><span class="sxs-lookup"><span data-stu-id="afde0-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-488">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-488">Pattern</span></span>

<span data-ttu-id="afde0-489">한 자리 또는 7 자리 숫자 앞에 오는 문자 (하지 대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="afde0-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="afde0-490">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-490">Checksum</span></span>

<span data-ttu-id="afde0-491">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-492">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-492">Definition</span></span>

<span data-ttu-id="afde0-493">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-494">정규식 `Regex_slovakia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-495">키워드에서 `Keywords_slovakia_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-496">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-496">Keywords</span></span>

<span data-ttu-id="afde0-497">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-497"></span></span>
|<span data-ttu-id="afde0-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-499">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-499">passport number</span></span>  <br/> <span data-ttu-id="afde0-500">슬로바키아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="afde0-501">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-501">passport no</span></span>  <br/> <span data-ttu-id="afde0-502">Číslo pasu</span><span class="sxs-lookup"><span data-stu-id="afde0-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="afde0-503">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="afde0-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="afde0-504">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-504">Format</span></span>

<span data-ttu-id="afde0-505">공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 두 문자</span><span class="sxs-lookup"><span data-stu-id="afde0-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-506">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-506">Pattern</span></span>

<span data-ttu-id="afde0-507">7 자리 숫자 앞에 오는 두 문자 수:</span><span class="sxs-lookup"><span data-stu-id="afde0-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="afde0-508">문자 "P"</span><span class="sxs-lookup"><span data-stu-id="afde0-508">The letter "P"</span></span>
    
- <span data-ttu-id="afde0-509">하나의 대문자</span><span class="sxs-lookup"><span data-stu-id="afde0-509">One uppercase letter</span></span>
    
- <span data-ttu-id="afde0-510">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="afde0-511">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-511">Checksum</span></span>

<span data-ttu-id="afde0-512">없음</span><span class="sxs-lookup"><span data-stu-id="afde0-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-513">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-513">Definition</span></span>

<span data-ttu-id="afde0-514">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-515">정규식 `Regex_slovenia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-516">키워드에서 `Keywords_slovenia_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-517">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-517">Keywords</span></span>

<span data-ttu-id="afde0-518">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-518"></span></span>
|<span data-ttu-id="afde0-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-520">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-520">passport number</span></span>  <br/> <span data-ttu-id="afde0-521">슬로베니아어 여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="afde0-522">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-522">passport no</span></span>  <br/> <span data-ttu-id="afde0-523">Številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="afde0-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="afde0-524">스페인</span><span class="sxs-lookup"><span data-stu-id="afde0-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="afde0-525">형식</span><span class="sxs-lookup"><span data-stu-id="afde0-525">Format</span></span>

<span data-ttu-id="afde0-526">문자와 공백이 나 구분 기호 없이 숫자는 8 또는 9 개 문자 조합</span><span class="sxs-lookup"><span data-stu-id="afde0-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="afde0-527">패턴</span><span class="sxs-lookup"><span data-stu-id="afde0-527">Pattern</span></span>

<span data-ttu-id="afde0-528">문자와 숫자는 8 또는 9 개 문자 조합 합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="afde0-529">두 자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="afde0-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="afde0-530">한 자리 숫자 또는 문자 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="afde0-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="afde0-531">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="afde0-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="afde0-532">체크섬</span><span class="sxs-lookup"><span data-stu-id="afde0-532">Checksum</span></span>

<span data-ttu-id="afde0-533">해당 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="afde0-534">정의</span><span class="sxs-lookup"><span data-stu-id="afde0-534">Definition</span></span>

<span data-ttu-id="afde0-535">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="afde0-536">정규식 `Regex_spain_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="afde0-537">키워드에서 `Keywords_spain_eu_passport_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="afde0-538">키워드</span><span class="sxs-lookup"><span data-stu-id="afde0-538">Keywords</span></span>

<span data-ttu-id="afde0-539">| |</span><span class="sxs-lookup"><span data-stu-id="afde0-539"></span></span>
|<span data-ttu-id="afde0-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="afde0-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="afde0-541">passport</span><span class="sxs-lookup"><span data-stu-id="afde0-541">passport</span></span>  <br/> <span data-ttu-id="afde0-542">스페인 passport</span><span class="sxs-lookup"><span data-stu-id="afde0-542">spain passport</span></span>  <br/> <span data-ttu-id="afde0-543">passport도 서</span><span class="sxs-lookup"><span data-stu-id="afde0-543">passport book</span></span>  <br/> <span data-ttu-id="afde0-544">여권 번호</span><span class="sxs-lookup"><span data-stu-id="afde0-544">passport number</span></span>  <br/> <span data-ttu-id="afde0-545">passport 없음</span><span class="sxs-lookup"><span data-stu-id="afde0-545">passport no</span></span>  <br/> <span data-ttu-id="afde0-546">libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="afde0-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="afde0-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="afde0-547">número pasaporte</span></span>  <br/> <span data-ttu-id="afde0-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="afde0-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="afde0-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="afde0-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="afde0-550">스웨덴</span><span class="sxs-lookup"><span data-stu-id="afde0-550">Sweden</span></span>

<span data-ttu-id="afde0-551">자세한 내용은의 섹션을 참조 "스웨덴 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="afde0-552">영국</span><span class="sxs-lookup"><span data-stu-id="afde0-552">UK</span></span>

<span data-ttu-id="afde0-p103">자세한 내용은의 섹션을 참조 "미국/영국 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="afde0-p103">For details, see the section "U.S. / U.K. Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="afde0-555">참고 항목</span><span class="sxs-lookup"><span data-stu-id="afde0-555">See also</span></span>

[<span data-ttu-id="afde0-556">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="afde0-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

