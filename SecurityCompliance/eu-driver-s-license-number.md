---
title: EU 운전 면허 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: 이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 드라이버의 라이선스 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: f1a95ecbaf6b6d1ac189290dd6d076cfd91ab30f
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152980"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="6470b-104">EU 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-104">EU Driver's License Number</span></span>

<span data-ttu-id="6470b-105">이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 드라이버의 라이선스 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="6470b-106">이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="6470b-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="6470b-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="6470b-108">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-108">Format</span></span>

<span data-ttu-id="6470b-109">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-110">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-110">Pattern</span></span>

<span data-ttu-id="6470b-111">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6470b-112">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-112">Checksum</span></span>

<span data-ttu-id="6470b-113">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-114">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-114">Definition</span></span>

<span data-ttu-id="6470b-115">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-116">정규식이 해당 `Regex_austria_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-117">From `Keywords_austria_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="6470b-118">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-118">Keywords</span></span>

<span data-ttu-id="6470b-119">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-119"></span></span>
|<span data-ttu-id="6470b-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-121">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-121">dl#</span></span>  <br/> <span data-ttu-id="6470b-122">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-122">driver license</span></span>  <br/> <span data-ttu-id="6470b-123">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-123">driver license number</span></span>  <br/> <span data-ttu-id="6470b-124">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-124">driver licence</span></span>  <br/> <span data-ttu-id="6470b-125">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-125">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-126">drivers license</span></span>  <br/> <span data-ttu-id="6470b-127">driver's licence</span><span class="sxs-lookup"><span data-stu-id="6470b-127">driver's licence</span></span>  <br/> <span data-ttu-id="6470b-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-128">driver's license</span></span>  <br/> <span data-ttu-id="6470b-129">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-129">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-130">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="6470b-131">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-131">driving license number</span></span>  <br/> <span data-ttu-id="6470b-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-132">dlno#</span></span>  <br/> <span data-ttu-id="6470b-133">fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="6470b-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="6470b-134">fuhrerschein republik osterreich</span><span class="sxs-lookup"><span data-stu-id="6470b-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="6470b-135">벨기에</span><span class="sxs-lookup"><span data-stu-id="6470b-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="6470b-136">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-136">Format</span></span>

<span data-ttu-id="6470b-137">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-138">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-138">Pattern</span></span>

<span data-ttu-id="6470b-139">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6470b-140">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-140">Checksum</span></span>

<span data-ttu-id="6470b-141">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-142">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-142">Definition</span></span>

<span data-ttu-id="6470b-143">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-144">정규식이 해당 `Regex_belgium_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-145">From `Keywords_belgium_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="6470b-146">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-146">Keywords</span></span>

<span data-ttu-id="6470b-147">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-147"></span></span>
|<span data-ttu-id="6470b-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-149">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-149">dl#</span></span>  <br/> <span data-ttu-id="6470b-150">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-150">driver license</span></span>  <br/> <span data-ttu-id="6470b-151">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-151">driver license number</span></span>  <br/> <span data-ttu-id="6470b-152">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-152">driver licence</span></span>  <br/> <span data-ttu-id="6470b-153">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-153">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-154">drivers license</span></span>  <br/> <span data-ttu-id="6470b-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-155">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-156">driver's license</span></span>  <br/> <span data-ttu-id="6470b-157">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-157">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-158">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-158">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-159">dlno#</span></span>  <br/> <span data-ttu-id="6470b-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="6470b-160">rijbewijs</span></span>  <br/> <span data-ttu-id="6470b-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="6470b-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="6470b-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6470b-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="6470b-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6470b-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="6470b-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6470b-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="6470b-165">führerschein-veiligheid</span><span class="sxs-lookup"><span data-stu-id="6470b-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="6470b-166">fuehrerschein-Veiligheid</span><span class="sxs-lookup"><span data-stu-id="6470b-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="6470b-167">fuehrerschein-veiligheid</span><span class="sxs-lookup"><span data-stu-id="6470b-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="6470b-168">불가리아</span><span class="sxs-lookup"><span data-stu-id="6470b-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="6470b-169">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-169">Format</span></span>

<span data-ttu-id="6470b-170">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-171">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-171">Pattern</span></span>

<span data-ttu-id="6470b-172">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6470b-173">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-173">Checksum</span></span>

<span data-ttu-id="6470b-174">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-175">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-175">Definition</span></span>

<span data-ttu-id="6470b-176">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-177">정규식이 해당 `Regex_bulgaria_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-178">From `Keywords_bulgaria_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="6470b-179">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-179">Keywords</span></span>

<span data-ttu-id="6470b-180">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-180"></span></span>
|<span data-ttu-id="6470b-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-182">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-182">dl#</span></span>  <br/> <span data-ttu-id="6470b-183">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-183">driver license</span></span>  <br/> <span data-ttu-id="6470b-184">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-184">driver license number</span></span>  <br/> <span data-ttu-id="6470b-185">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-185">driver licence</span></span>  <br/> <span data-ttu-id="6470b-186">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-186">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-187">drivers license</span></span>  <br/> <span data-ttu-id="6470b-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-188">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-189">driver's license</span></span>  <br/> <span data-ttu-id="6470b-190">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-190">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-191">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-191">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-192">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-192">driving license number</span></span>  <br/> <span data-ttu-id="6470b-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-193">dlno#</span></span>  <br/> <span data-ttu-id="6470b-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="6470b-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="6470b-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="6470b-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="6470b-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="6470b-196">сумпс</span></span>  <br/> <span data-ttu-id="6470b-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="6470b-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="6470b-198">크로아티아</span><span class="sxs-lookup"><span data-stu-id="6470b-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="6470b-199">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-199">Format</span></span>

<span data-ttu-id="6470b-200">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-201">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-201">Pattern</span></span>

<span data-ttu-id="6470b-202">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6470b-203">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-203">Checksum</span></span>

<span data-ttu-id="6470b-204">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-205">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-205">Definition</span></span>

<span data-ttu-id="6470b-206">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-207">정규식이 해당 `Regex_croatia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-208">From `Keywords_croatia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="6470b-209">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-209">Keywords</span></span>

<span data-ttu-id="6470b-210">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-210"></span></span>
|<span data-ttu-id="6470b-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-212">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-212">dl#</span></span>  <br/> <span data-ttu-id="6470b-213">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-213">driver license</span></span>  <br/> <span data-ttu-id="6470b-214">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-214">driver license number</span></span>  <br/> <span data-ttu-id="6470b-215">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-215">driver licence</span></span>  <br/> <span data-ttu-id="6470b-216">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-216">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-217">drivers license</span></span>  <br/> <span data-ttu-id="6470b-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-218">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-219">driver's license</span></span>  <br/> <span data-ttu-id="6470b-220">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-220">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-221">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-221">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-222">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-222">driving license number</span></span>  <br/> <span data-ttu-id="6470b-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-223">dlno#</span></span>  <br/> <span data-ttu-id="6470b-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="6470b-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="6470b-225">키프로스</span><span class="sxs-lookup"><span data-stu-id="6470b-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="6470b-226">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-226">Format</span></span>

<span data-ttu-id="6470b-227">공백과 구분 기호를 사용 하지 않고 12 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-228">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-228">Pattern</span></span>

<span data-ttu-id="6470b-229">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6470b-230">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-230">Checksum</span></span>

<span data-ttu-id="6470b-231">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-232">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-232">Definition</span></span>

<span data-ttu-id="6470b-233">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-234">정규식이 해당 `Regex_cyprus_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-235">From `Keywords_cyprus_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-236">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-236">Keywords</span></span>

<span data-ttu-id="6470b-237">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-237"></span></span>
|<span data-ttu-id="6470b-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-239">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-239">dl#</span></span>  <br/> <span data-ttu-id="6470b-240">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-240">driver license</span></span>  <br/> <span data-ttu-id="6470b-241">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-241">driver license number</span></span>  <br/> <span data-ttu-id="6470b-242">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-242">driver licence</span></span>  <br/> <span data-ttu-id="6470b-243">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-243">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-244">drivers license</span></span>  <br/> <span data-ttu-id="6470b-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-245">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-246">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-246">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-247">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-247">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-248">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-248">driving license number</span></span>  <br/> <span data-ttu-id="6470b-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-249">dlno#</span></span>  <br/> <span data-ttu-id="6470b-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="6470b-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="6470b-251">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="6470b-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="6470b-252">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-252">Format</span></span>

<span data-ttu-id="6470b-253">2 개의 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-254">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-254">Pattern</span></span>

<span data-ttu-id="6470b-255">8 개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="6470b-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="6470b-256">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6470b-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="6470b-257">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="6470b-257">A space (optional)</span></span>
    
- <span data-ttu-id="6470b-258">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6470b-259">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-259">Checksum</span></span>

<span data-ttu-id="6470b-260">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-261">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-261">Definition</span></span>

<span data-ttu-id="6470b-262">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-263">정규식이 해당 `Regex_czech_republic_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-264">From `Keywords_czech_republic_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="6470b-265">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-265">Keywords</span></span>

<span data-ttu-id="6470b-266">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-266"></span></span>
|<span data-ttu-id="6470b-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-268">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-268">dl#</span></span>  <br/> <span data-ttu-id="6470b-269">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-269">driver license</span></span>  <br/> <span data-ttu-id="6470b-270">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-270">driver license number</span></span>  <br/> <span data-ttu-id="6470b-271">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-271">driver licence</span></span>  <br/> <span data-ttu-id="6470b-272">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-272">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-273">drivers license</span></span>  <br/> <span data-ttu-id="6470b-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-274">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-275">driver's license</span></span>  <br/> <span data-ttu-id="6470b-276">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-276">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-277">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-277">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-278">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-278">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-279">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-279">driving license number</span></span>  <br/> <span data-ttu-id="6470b-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-280">dlno#</span></span>  <br/> <span data-ttu-id="6470b-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="6470b-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="6470b-282">덴마크</span><span class="sxs-lookup"><span data-stu-id="6470b-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="6470b-283">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-283">Format</span></span>

<span data-ttu-id="6470b-284">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-285">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-285">Pattern</span></span>

<span data-ttu-id="6470b-286">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6470b-287">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-287">Checksum</span></span>

<span data-ttu-id="6470b-288">예</span><span class="sxs-lookup"><span data-stu-id="6470b-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-289">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-289">Definition</span></span>

<span data-ttu-id="6470b-290">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-291">정규식이 해당 `Regex_denmark_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-292">From `Keywords_denmark_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="6470b-293">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-293">Keywords</span></span>

<span data-ttu-id="6470b-294">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-294"></span></span>
|<span data-ttu-id="6470b-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-296">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-296">dl#</span></span>  <br/> <span data-ttu-id="6470b-297">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-297">driver license</span></span>  <br/> <span data-ttu-id="6470b-298">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-298">driver license number</span></span>  <br/> <span data-ttu-id="6470b-299">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-299">driver licence</span></span>  <br/> <span data-ttu-id="6470b-300">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-300">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-301">drivers license</span></span>  <br/> <span data-ttu-id="6470b-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-302">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-303">driver's license</span></span>  <br/> <span data-ttu-id="6470b-304">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-304">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-305">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-305">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-306">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-306">driving license number</span></span>  <br/> <span data-ttu-id="6470b-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-307">dlno#</span></span>  <br/> <span data-ttu-id="6470b-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="6470b-308">kørekort</span></span>  <br/> <span data-ttu-id="6470b-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="6470b-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="6470b-310">에스토니아</span><span class="sxs-lookup"><span data-stu-id="6470b-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="6470b-311">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-311">Format</span></span>

<span data-ttu-id="6470b-312">2 개의 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-313">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-313">Pattern</span></span>

<span data-ttu-id="6470b-314">2 개의 문자와 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="6470b-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="6470b-315">문자 "ET" (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6470b-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="6470b-316">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6470b-317">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-317">Checksum</span></span>

<span data-ttu-id="6470b-318">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-319">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-319">Definition</span></span>

<span data-ttu-id="6470b-320">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-321">정규식이 해당 `Regex_estonia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-322">From `Keywords_estonia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-323">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-323">Keywords</span></span>

<span data-ttu-id="6470b-324">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-324"></span></span>
|<span data-ttu-id="6470b-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-326">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-326">dl#</span></span>  <br/> <span data-ttu-id="6470b-327">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-327">driver license</span></span>  <br/> <span data-ttu-id="6470b-328">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-328">driver license number</span></span>  <br/> <span data-ttu-id="6470b-329">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-329">driver license number</span></span>  <br/> <span data-ttu-id="6470b-330">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-330">driver licence</span></span>  <br/> <span data-ttu-id="6470b-331">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-331">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-332">drivers license</span></span>  <br/> <span data-ttu-id="6470b-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-333">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-334">driver's license</span></span>  <br/> <span data-ttu-id="6470b-335">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-335">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-336">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-336">driving license number</span></span>  <br/> <span data-ttu-id="6470b-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-337">dlno#</span></span>  <br/> <span data-ttu-id="6470b-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="6470b-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="6470b-339">핀란드</span><span class="sxs-lookup"><span data-stu-id="6470b-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="6470b-340">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-340">Format</span></span>

<span data-ttu-id="6470b-341">하이픈을 포함하는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-342">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-342">Pattern</span></span>

<span data-ttu-id="6470b-343">하이픈을 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="6470b-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="6470b-344">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-344">Six digits</span></span> 
    
- <span data-ttu-id="6470b-345">하이픈</span><span class="sxs-lookup"><span data-stu-id="6470b-345">A hyphen</span></span>
    
-  <span data-ttu-id="6470b-346">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="6470b-347">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-347">Checksum</span></span>

<span data-ttu-id="6470b-348">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-349">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-349">Definition</span></span>

<span data-ttu-id="6470b-350">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-351">정규식이 해당 `Regex_finland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-352">From `Keywords_finland_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-353">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-353">Keywords</span></span>

<span data-ttu-id="6470b-354">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-354"></span></span>
|<span data-ttu-id="6470b-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-356">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-356">dl#</span></span>  <br/> <span data-ttu-id="6470b-357">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-357">driver license</span></span>  <br/> <span data-ttu-id="6470b-358">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-358">driver license number</span></span>  <br/> <span data-ttu-id="6470b-359">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-359">driver licence</span></span>  <br/> <span data-ttu-id="6470b-360">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-360">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-361">drivers license</span></span>  <br/> <span data-ttu-id="6470b-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-362">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-363">driver's license</span></span>  <br/> <span data-ttu-id="6470b-364">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-364">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-365">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-365">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-366">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-366">driving license number</span></span>  <br/> <span data-ttu-id="6470b-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-367">dlno#</span></span>  <br/> <span data-ttu-id="6470b-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="6470b-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="6470b-369">프랑스</span><span class="sxs-lookup"><span data-stu-id="6470b-369">France</span></span>

<span data-ttu-id="6470b-370">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"경기도 운전 면허 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6470b-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="6470b-371">독일</span><span class="sxs-lookup"><span data-stu-id="6470b-371">Germany</span></span>

<span data-ttu-id="6470b-372">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일어 운전 면허 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6470b-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="6470b-373">그리스</span><span class="sxs-lookup"><span data-stu-id="6470b-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="6470b-374">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-374">Format</span></span>

<span data-ttu-id="6470b-375">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-376">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-376">Pattern</span></span>

 <span data-ttu-id="6470b-377">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="6470b-378">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-378">Checksum</span></span>

<span data-ttu-id="6470b-379">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-380">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-380">Definition</span></span>

<span data-ttu-id="6470b-381">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-382">정규식이 해당 `Regex_greece_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-383">From `Keywords_greece_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-384">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-384">Keywords</span></span>

<span data-ttu-id="6470b-385">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-385"></span></span>
|<span data-ttu-id="6470b-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-387">DlL</span><span class="sxs-lookup"><span data-stu-id="6470b-387">dlL#</span></span>  <br/> <span data-ttu-id="6470b-388">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-388">driver license</span></span>  <br/> <span data-ttu-id="6470b-389">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-389">driver license number</span></span>  <br/> <span data-ttu-id="6470b-390">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-390">driver licence</span></span>  <br/> <span data-ttu-id="6470b-391">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-391">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-392">drivers license</span></span>  <br/> <span data-ttu-id="6470b-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-393">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-394">driver's license</span></span>  <br/> <span data-ttu-id="6470b-395">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-395">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-396">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-396">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-397">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-397">driving license number</span></span>  <br/> <span data-ttu-id="6470b-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-398">dlno#</span></span>  <br/> <span data-ttu-id="6470b-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="6470b-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="6470b-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="6470b-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="6470b-401">헝가리</span><span class="sxs-lookup"><span data-stu-id="6470b-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="6470b-402">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-402">Format</span></span>

<span data-ttu-id="6470b-403">2 개의 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-404">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-404">Pattern</span></span>

<span data-ttu-id="6470b-405">2 개의 문자와 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="6470b-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="6470b-406">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6470b-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="6470b-407">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6470b-408">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-408">Checksum</span></span>

<span data-ttu-id="6470b-409">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-410">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-410">Definition</span></span>

<span data-ttu-id="6470b-411">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-412">정규식이 해당 `Regex_hungary_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-413">From `Keywords_hungary_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-414">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-414">Keywords</span></span>

<span data-ttu-id="6470b-415">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-415"></span></span>
|<span data-ttu-id="6470b-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-417">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-417">dl#</span></span>  <br/> <span data-ttu-id="6470b-418">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-418">driver license</span></span>  <br/> <span data-ttu-id="6470b-419">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-419">driver license number</span></span>  <br/> <span data-ttu-id="6470b-420">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-420">driver licence</span></span>  <br/> <span data-ttu-id="6470b-421">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-421">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-422">drivers license</span></span>  <br/> <span data-ttu-id="6470b-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-423">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-424">driver's license</span></span>  <br/> <span data-ttu-id="6470b-425">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-425">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-426">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-426">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-427">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-427">driving license number</span></span>  <br/> <span data-ttu-id="6470b-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-428">dlno#</span></span>  <br/> <span data-ttu-id="6470b-429">vezetoi</span><span class="sxs-lookup"><span data-stu-id="6470b-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="6470b-430">Ireland</span><span class="sxs-lookup"><span data-stu-id="6470b-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="6470b-431">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-431">Format</span></span>

<span data-ttu-id="6470b-432">6 자리 숫자와 4 개 문자</span><span class="sxs-lookup"><span data-stu-id="6470b-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-433">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-433">Pattern</span></span>

<span data-ttu-id="6470b-434">6 자리 숫자와 4 개 문자:</span><span class="sxs-lookup"><span data-stu-id="6470b-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="6470b-435">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-435">Six digits</span></span>
    
- <span data-ttu-id="6470b-436">4 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6470b-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6470b-437">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-437">Checksum</span></span>

<span data-ttu-id="6470b-438">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-439">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-439">Definition</span></span>

<span data-ttu-id="6470b-440">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-441">정규식이 해당 `Regex_ireland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-442">From `Keywords_ireland_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-443">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-443">Keywords</span></span>

<span data-ttu-id="6470b-444">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-444"></span></span>
|<span data-ttu-id="6470b-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-446">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-446">dl#</span></span>  <br/> <span data-ttu-id="6470b-447">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-447">driver license</span></span>  <br/> <span data-ttu-id="6470b-448">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-448">driver license number</span></span>  <br/> <span data-ttu-id="6470b-449">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-449">driver licence</span></span>  <br/> <span data-ttu-id="6470b-450">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-450">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-451">drivers license</span></span>  <br/> <span data-ttu-id="6470b-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-452">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-453">driver's license</span></span>  <br/> <span data-ttu-id="6470b-454">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-454">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-455">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-455">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-456">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-456">driving license number</span></span>  <br/> <span data-ttu-id="6470b-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-457">dlno#</span></span>  <br/> <span data-ttu-id="6470b-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="6470b-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="6470b-459">이탈리아</span><span class="sxs-lookup"><span data-stu-id="6470b-459">Italy</span></span>

<span data-ttu-id="6470b-460">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"이탈리아 운전 면허 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6470b-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="6470b-461">라트비아</span><span class="sxs-lookup"><span data-stu-id="6470b-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="6470b-462">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-462">Format</span></span>

<span data-ttu-id="6470b-463">3 개의 문자 및 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-464">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-464">Pattern</span></span>

<span data-ttu-id="6470b-465">3 개의 문자 및 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="6470b-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="6470b-466">3 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6470b-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="6470b-467">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6470b-468">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-468">Checksum</span></span>

<span data-ttu-id="6470b-469">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-470">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-470">Definition</span></span>

<span data-ttu-id="6470b-471">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-472">정규식이 해당 `Regex_latvia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-473">From `Keywords_latvia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-474">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-474">Keywords</span></span>

<span data-ttu-id="6470b-475">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-475"></span></span>
|<span data-ttu-id="6470b-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-477">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-477">dl#</span></span>  <br/> <span data-ttu-id="6470b-478">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-478">driver license</span></span>  <br/> <span data-ttu-id="6470b-479">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-479">driver license number</span></span>  <br/> <span data-ttu-id="6470b-480">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-480">driver licence</span></span>  <br/> <span data-ttu-id="6470b-481">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-481">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-482">drivers license</span></span>  <br/> <span data-ttu-id="6470b-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-483">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-484">driver's license</span></span>  <br/> <span data-ttu-id="6470b-485">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-485">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-486">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-486">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-487">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-487">driving license number</span></span>  <br/> <span data-ttu-id="6470b-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-488">dlno#</span></span>  <br/> <span data-ttu-id="6470b-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="6470b-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="6470b-490">리투아니아</span><span class="sxs-lookup"><span data-stu-id="6470b-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="6470b-491">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-491">Format</span></span>

<span data-ttu-id="6470b-492">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-493">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-493">Pattern</span></span>

 <span data-ttu-id="6470b-494">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="6470b-495">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-495">Checksum</span></span>

<span data-ttu-id="6470b-496">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-497">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-497">Definition</span></span>

<span data-ttu-id="6470b-498">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-499">정규식이 해당 `Regex_lithuania_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-500">From `Keywords_lithuania_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-501">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-501">Keywords</span></span>

<span data-ttu-id="6470b-502">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-502"></span></span>
|<span data-ttu-id="6470b-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-504">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-504">dl#</span></span>  <br/> <span data-ttu-id="6470b-505">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-505">driver license</span></span>  <br/> <span data-ttu-id="6470b-506">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-506">driver license number</span></span>  <br/> <span data-ttu-id="6470b-507">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-507">driver licence</span></span>  <br/> <span data-ttu-id="6470b-508">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-508">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-509">drivers license</span></span>  <br/> <span data-ttu-id="6470b-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-510">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-511">driver's license</span></span>  <br/> <span data-ttu-id="6470b-512">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-512">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-513">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-513">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-514">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-514">driving license number</span></span>  <br/> <span data-ttu-id="6470b-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-515">dlno#</span></span>  <br/> <span data-ttu-id="6470b-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="6470b-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="6470b-517">셈</span><span class="sxs-lookup"><span data-stu-id="6470b-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="6470b-518">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-518">Format</span></span>

<span data-ttu-id="6470b-519">공백과 구분 기호가 없는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-520">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-520">Pattern</span></span>

 <span data-ttu-id="6470b-521">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="6470b-522">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-522">Checksum</span></span>

<span data-ttu-id="6470b-523">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-524">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-524">Definition</span></span>

<span data-ttu-id="6470b-525">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-526">정규식이 해당 `Regex_luxemburg_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-527">From `Keywords_luxemburg_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-528">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-528">Keywords</span></span>

<span data-ttu-id="6470b-529">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-529"></span></span>
|<span data-ttu-id="6470b-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-531">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-531">dl#</span></span>  <br/> <span data-ttu-id="6470b-532">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-532">driver license</span></span>  <br/> <span data-ttu-id="6470b-533">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-533">driver license number</span></span>  <br/> <span data-ttu-id="6470b-534">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-534">driver licence</span></span>  <br/> <span data-ttu-id="6470b-535">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-535">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-536">drivers license</span></span>  <br/> <span data-ttu-id="6470b-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-537">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-538">driver's license</span></span>  <br/> <span data-ttu-id="6470b-539">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-539">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-540">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-540">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-541">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-541">driving license number</span></span>  <br/> <span data-ttu-id="6470b-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-542">dlno#</span></span>  <br/> <span data-ttu-id="6470b-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="6470b-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="6470b-544">몰타</span><span class="sxs-lookup"><span data-stu-id="6470b-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="6470b-545">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-545">Format</span></span>

<span data-ttu-id="6470b-546">지정 된 패턴에서 두 개의 문자와 6 자리 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="6470b-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-547">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-547">Pattern</span></span>

<span data-ttu-id="6470b-548">두 문자와 6 자리 숫자의 조합:</span><span class="sxs-lookup"><span data-stu-id="6470b-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="6470b-549">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6470b-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="6470b-550">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="6470b-550">A space (optional)</span></span>
    
- <span data-ttu-id="6470b-551">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-551">Three digits</span></span>
    
- <span data-ttu-id="6470b-552">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="6470b-552">A space (optional)</span></span>
    
- <span data-ttu-id="6470b-553">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6470b-554">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-554">Checksum</span></span>

<span data-ttu-id="6470b-555">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-556">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-556">Definition</span></span>

<span data-ttu-id="6470b-557">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-558">정규식이 해당 `Regex_malta_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-559">From `Keywords_malta_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-560">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-560">Keywords</span></span>

<span data-ttu-id="6470b-561">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-561"></span></span>
|<span data-ttu-id="6470b-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-563">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-563">dl#</span></span>  <br/> <span data-ttu-id="6470b-564">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-564">driver license</span></span>  <br/> <span data-ttu-id="6470b-565">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-565">driver license number</span></span>  <br/> <span data-ttu-id="6470b-566">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-566">driver licence</span></span>  <br/> <span data-ttu-id="6470b-567">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-567">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-568">drivers license</span></span>  <br/> <span data-ttu-id="6470b-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-569">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-570">driver's license</span></span>  <br/> <span data-ttu-id="6470b-571">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-571">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-572">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-572">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-573">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-573">driving license number</span></span>  <br/> <span data-ttu-id="6470b-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-574">dlno#</span></span>  <br/> <span data-ttu-id="6470b-575">liċenzja tas-sewqan</span><span class="sxs-lookup"><span data-stu-id="6470b-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="6470b-576">네덜란드</span><span class="sxs-lookup"><span data-stu-id="6470b-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="6470b-577">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-577">Format</span></span>

<span data-ttu-id="6470b-578">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-579">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-579">Pattern</span></span>

<span data-ttu-id="6470b-580">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6470b-581">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-581">Checksum</span></span>

<span data-ttu-id="6470b-582">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-583">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-583">Definition</span></span>

<span data-ttu-id="6470b-584">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-585">정규식이 해당 `Regex_netherlands_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-586">From `Keywords_netherlands_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-587">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-587">Keywords</span></span>

<span data-ttu-id="6470b-588">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-588"></span></span>
|<span data-ttu-id="6470b-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-590">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-590">dl#</span></span>  <br/> <span data-ttu-id="6470b-591">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-591">driver license</span></span>  <br/> <span data-ttu-id="6470b-592">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-592">driver license number</span></span>  <br/> <span data-ttu-id="6470b-593">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-593">driver licence</span></span>  <br/> <span data-ttu-id="6470b-594">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-594">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-595">drivers license</span></span>  <br/> <span data-ttu-id="6470b-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-596">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-597">driver's license</span></span>  <br/> <span data-ttu-id="6470b-598">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-598">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-599">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-599">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-600">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-600">driving license number</span></span>  <br/> <span data-ttu-id="6470b-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-601">dlno#</span></span>  <br/> <span data-ttu-id="6470b-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="6470b-602">permis de conduire</span></span>  <br/> <span data-ttu-id="6470b-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="6470b-603">rijbewijs</span></span>  <br/> <span data-ttu-id="6470b-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="6470b-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="6470b-605">폴란드</span><span class="sxs-lookup"><span data-stu-id="6470b-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="6470b-606">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-606">Format</span></span>

<span data-ttu-id="6470b-607">두 개의 슬래시를 포함 하는 14 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-608">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-608">Pattern</span></span>

<span data-ttu-id="6470b-609">14 자리 숫자와 2 개의 슬래시:</span><span class="sxs-lookup"><span data-stu-id="6470b-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="6470b-610">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-610">Five digits</span></span> 
    
- <span data-ttu-id="6470b-611">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="6470b-611">A forward slash</span></span>
    
- <span data-ttu-id="6470b-612">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-612">Two digits</span></span>
    
- <span data-ttu-id="6470b-613">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="6470b-613">A forward slash</span></span>
    
- <span data-ttu-id="6470b-614">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6470b-615">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-615">Checksum</span></span>

<span data-ttu-id="6470b-616">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-617">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-617">Definition</span></span>

<span data-ttu-id="6470b-618">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-619">정규식이 해당 `Regex_poland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-620">From `Keywords_poland_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-621">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-621">Keywords</span></span>

<span data-ttu-id="6470b-622">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-622"></span></span>
|<span data-ttu-id="6470b-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-624">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-624">dl#</span></span>  <br/> <span data-ttu-id="6470b-625">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-625">driver license</span></span>  <br/> <span data-ttu-id="6470b-626">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-626">driver license number</span></span>  <br/> <span data-ttu-id="6470b-627">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-627">driver licence</span></span>  <br/> <span data-ttu-id="6470b-628">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-628">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-629">drivers license</span></span>  <br/> <span data-ttu-id="6470b-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-630">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-631">driver's license</span></span>  <br/> <span data-ttu-id="6470b-632">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-632">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-633">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-633">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-634">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-634">driving license number</span></span>  <br/> <span data-ttu-id="6470b-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-635">dlno#</span></span>  <br/> <span data-ttu-id="6470b-636">prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="6470b-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="6470b-637">포르투갈</span><span class="sxs-lookup"><span data-stu-id="6470b-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="6470b-638">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-638">Format</span></span>

<span data-ttu-id="6470b-639">두 개의 문자와 지정 된 패턴에 있는 일곱 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-640">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-640">Pattern</span></span>

<span data-ttu-id="6470b-641">두 문자 다음에 특수 문자를 사용한 7 개의 숫자를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="6470b-642">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6470b-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="6470b-643">하이픈</span><span class="sxs-lookup"><span data-stu-id="6470b-643">A hyphen</span></span>
    
- <span data-ttu-id="6470b-644">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-644">Six digits</span></span>
    
- <span data-ttu-id="6470b-645">공백</span><span class="sxs-lookup"><span data-stu-id="6470b-645">A space</span></span>
    
- <span data-ttu-id="6470b-646">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6470b-647">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-647">Checksum</span></span>

<span data-ttu-id="6470b-648">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-649">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-649">Definition</span></span>

<span data-ttu-id="6470b-650">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-651">정규식이 해당 `Regex_portugal_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-652">From `Keywords_portugal_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-653">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-653">Keywords</span></span>

<span data-ttu-id="6470b-654">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-654"></span></span>
|<span data-ttu-id="6470b-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-656">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-656">dl#</span></span>  <br/> <span data-ttu-id="6470b-657">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-657">driver license</span></span>  <br/> <span data-ttu-id="6470b-658">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-658">driver license number</span></span>  <br/> <span data-ttu-id="6470b-659">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-659">driver licence</span></span>  <br/> <span data-ttu-id="6470b-660">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-660">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-661">drivers license</span></span>  <br/> <span data-ttu-id="6470b-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-662">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-663">driver's license</span></span>  <br/> <span data-ttu-id="6470b-664">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-664">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-665">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-665">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-666">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-666">driving license number</span></span>  <br/> <span data-ttu-id="6470b-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-667">dlno#</span></span>  <br/> <span data-ttu-id="6470b-668">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="6470b-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="6470b-669">루마니아</span><span class="sxs-lookup"><span data-stu-id="6470b-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="6470b-670">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-670">Format</span></span>

<span data-ttu-id="6470b-671">한 문자 다음에 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-672">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-672">Pattern</span></span>

<span data-ttu-id="6470b-673">1 개의 문자 다음에 8 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="6470b-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="6470b-674">1 개 문자 (대/소문자 구분 안 함) 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="6470b-675">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6470b-676">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-676">Checksum</span></span>

<span data-ttu-id="6470b-677">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-678">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-678">Definition</span></span>

<span data-ttu-id="6470b-679">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-680">정규식이 해당 `Regex_romania_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-681">From `Keywords_romania_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-682">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-682">Keywords</span></span>

<span data-ttu-id="6470b-683">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-683"></span></span>
|<span data-ttu-id="6470b-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-685">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-685">dl#</span></span>  <br/> <span data-ttu-id="6470b-686">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-686">driver license</span></span>  <br/> <span data-ttu-id="6470b-687">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-687">driver license number</span></span>  <br/> <span data-ttu-id="6470b-688">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-688">driver licence</span></span>  <br/> <span data-ttu-id="6470b-689">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-689">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-690">drivers license</span></span>  <br/> <span data-ttu-id="6470b-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-691">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-692">driver's license</span></span>  <br/> <span data-ttu-id="6470b-693">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-693">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-694">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-694">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-695">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-695">driving license number</span></span>  <br/> <span data-ttu-id="6470b-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-696">dlno#</span></span>  <br/> <span data-ttu-id="6470b-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="6470b-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="6470b-698">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="6470b-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="6470b-699">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-699">Format</span></span>

<span data-ttu-id="6470b-700">한 문자 다음에 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-701">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-701">Pattern</span></span>

<span data-ttu-id="6470b-702">한 문자 다음에 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="6470b-703">1 개 문자 (대/소문자 구분 안 함) 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="6470b-704">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="6470b-705">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-705">Checksum</span></span>

<span data-ttu-id="6470b-706">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-707">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-707">Definition</span></span>

<span data-ttu-id="6470b-708">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-709">정규식이 해당 `Regex_slovakia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-710">From `Keywords_slovakia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-711">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-711">Keywords</span></span>

<span data-ttu-id="6470b-712">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-712"></span></span>
|<span data-ttu-id="6470b-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-714">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-714">dl#</span></span>  <br/> <span data-ttu-id="6470b-715">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-715">driver license</span></span>  <br/> <span data-ttu-id="6470b-716">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-716">driver license number</span></span>  <br/> <span data-ttu-id="6470b-717">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-717">driver licence</span></span>  <br/> <span data-ttu-id="6470b-718">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-718">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-719">drivers license</span></span>  <br/> <span data-ttu-id="6470b-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-720">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-721">driver's license</span></span>  <br/> <span data-ttu-id="6470b-722">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-722">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-723">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-723">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-724">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-724">driving license number</span></span>  <br/> <span data-ttu-id="6470b-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-725">dlno#</span></span>  <br/> <span data-ttu-id="6470b-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="6470b-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="6470b-727">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="6470b-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="6470b-728">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-728">Format</span></span>

<span data-ttu-id="6470b-729">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-730">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-730">Pattern</span></span>

<span data-ttu-id="6470b-731">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6470b-732">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-732">Checksum</span></span>

<span data-ttu-id="6470b-733">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-734">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-734">Definition</span></span>

<span data-ttu-id="6470b-735">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-736">정규식이 해당 `Regex_slovenia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-737">From `Keywords_slovenia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-738">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-738">Keywords</span></span>

<span data-ttu-id="6470b-739">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-739"></span></span>
|<span data-ttu-id="6470b-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-741">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-741">dl#</span></span>  <br/> <span data-ttu-id="6470b-742">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-742">driver license</span></span>  <br/> <span data-ttu-id="6470b-743">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-743">driver license number</span></span>  <br/> <span data-ttu-id="6470b-744">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-744">driver licence</span></span>  <br/> <span data-ttu-id="6470b-745">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-745">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-746">drivers license</span></span>  <br/> <span data-ttu-id="6470b-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-747">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-748">driver's license</span></span>  <br/> <span data-ttu-id="6470b-749">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-749">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-750">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-750">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-751">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-751">driving license number</span></span>  <br/> <span data-ttu-id="6470b-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-752">dlno#</span></span>  <br/> <span data-ttu-id="6470b-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="6470b-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="6470b-754">스페인</span><span class="sxs-lookup"><span data-stu-id="6470b-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="6470b-755">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-755">Format</span></span>

<span data-ttu-id="6470b-756">8 자리 숫자와 문자 1 개</span><span class="sxs-lookup"><span data-stu-id="6470b-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-757">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-757">Pattern</span></span>

<span data-ttu-id="6470b-758">8 자리 숫자와 문자 1 개:</span><span class="sxs-lookup"><span data-stu-id="6470b-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="6470b-759">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-759">Eight digits</span></span> 
    
- <span data-ttu-id="6470b-760">1 자리 숫자 또는 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6470b-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6470b-761">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-761">Checksum</span></span>

<span data-ttu-id="6470b-762">예</span><span class="sxs-lookup"><span data-stu-id="6470b-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-763">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-763">Definition</span></span>

<span data-ttu-id="6470b-764">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-765">이 함수 `Func_spain_eu_driver's_license_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-766">From `Keywords_spain_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6470b-767">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-767">Keywords</span></span>

<span data-ttu-id="6470b-768">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-768"></span></span>
|<span data-ttu-id="6470b-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-770">dlno#</span></span>  <br/> <span data-ttu-id="6470b-771">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-771">dl#</span></span>  <br/> <span data-ttu-id="6470b-772">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-772">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-773">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-773">driver licence</span></span>  <br/> <span data-ttu-id="6470b-774">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-774">driver license</span></span>  <br/> <span data-ttu-id="6470b-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-775">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-776">drivers license</span></span>  <br/> <span data-ttu-id="6470b-777">driver's licence</span><span class="sxs-lookup"><span data-stu-id="6470b-777">driver's licence</span></span>  <br/> <span data-ttu-id="6470b-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-778">driver's license</span></span>  <br/> <span data-ttu-id="6470b-779">driving licence</span><span class="sxs-lookup"><span data-stu-id="6470b-779">driving licence</span></span>  <br/> <span data-ttu-id="6470b-780">driving license</span><span class="sxs-lookup"><span data-stu-id="6470b-780">driving license</span></span>  <br/> <span data-ttu-id="6470b-781">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-781">driver licence number</span></span>  <br/> <span data-ttu-id="6470b-782">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-782">driver license number</span></span>  <br/> <span data-ttu-id="6470b-783">영향 요소 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-783">drivers licence number</span></span>  <br/> <span data-ttu-id="6470b-784">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-784">drivers license number</span></span>  <br/> <span data-ttu-id="6470b-785">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-785">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-786">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-786">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-787">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-787">driving licence number</span></span>  <br/> <span data-ttu-id="6470b-788">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-788">driving license number</span></span>  <br/> <span data-ttu-id="6470b-789">추진 허용</span><span class="sxs-lookup"><span data-stu-id="6470b-789">driving permit</span></span>  <br/> <span data-ttu-id="6470b-790">제어 허용 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-790">driving permit number</span></span>  <br/> <span data-ttu-id="6470b-791">permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="6470b-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="6470b-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="6470b-792">permiso conducción</span></span>  <br/> <span data-ttu-id="6470b-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="6470b-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="6470b-794">número de 네트워크 de conducir</span><span class="sxs-lookup"><span data-stu-id="6470b-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="6470b-795">número carnet conducir</span><span class="sxs-lookup"><span data-stu-id="6470b-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="6470b-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="6470b-796">licencia conducir</span></span>  <br/> <span data-ttu-id="6470b-797">número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="6470b-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="6470b-798">número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="6470b-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="6470b-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="6470b-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="6470b-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="6470b-800">permiso conducir</span></span>  <br/> <span data-ttu-id="6470b-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="6470b-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="6470b-802">el carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="6470b-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="6470b-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="6470b-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="6470b-804">스웨덴</span><span class="sxs-lookup"><span data-stu-id="6470b-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="6470b-805">형식일</span><span class="sxs-lookup"><span data-stu-id="6470b-805">Format</span></span>

<span data-ttu-id="6470b-806">하이픈을 포함 하는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6470b-807">패턴</span><span class="sxs-lookup"><span data-stu-id="6470b-807">Pattern</span></span>

<span data-ttu-id="6470b-808">하이픈을 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="6470b-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="6470b-809">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-809">Six digits</span></span> 
    
- <span data-ttu-id="6470b-810">하이픈</span><span class="sxs-lookup"><span data-stu-id="6470b-810">A hyphen</span></span>
    
- <span data-ttu-id="6470b-811">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6470b-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6470b-812">제외</span><span class="sxs-lookup"><span data-stu-id="6470b-812">Checksum</span></span>

<span data-ttu-id="6470b-813">아니요</span><span class="sxs-lookup"><span data-stu-id="6470b-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6470b-814">정의</span><span class="sxs-lookup"><span data-stu-id="6470b-814">Definition</span></span>

<span data-ttu-id="6470b-815">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6470b-816">정규식이 해당 `Regex_sweden_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6470b-817">From `Keywords_sweden_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="6470b-818">키워드</span><span class="sxs-lookup"><span data-stu-id="6470b-818">Keywords</span></span>

<span data-ttu-id="6470b-819">| |</span><span class="sxs-lookup"><span data-stu-id="6470b-819"></span></span>
|<span data-ttu-id="6470b-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6470b-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6470b-821">dl</span><span class="sxs-lookup"><span data-stu-id="6470b-821">dl#</span></span>  <br/> <span data-ttu-id="6470b-822">driver license</span><span class="sxs-lookup"><span data-stu-id="6470b-822">driver license</span></span>  <br/> <span data-ttu-id="6470b-823">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-823">driver license number</span></span>  <br/> <span data-ttu-id="6470b-824">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6470b-824">driver licence</span></span>  <br/> <span data-ttu-id="6470b-825">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6470b-825">drivers lic.</span></span>  <br/> <span data-ttu-id="6470b-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="6470b-826">drivers license</span></span>  <br/> <span data-ttu-id="6470b-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6470b-827">drivers licence</span></span>  <br/> <span data-ttu-id="6470b-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="6470b-828">driver's license</span></span>  <br/> <span data-ttu-id="6470b-829">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-829">driver's license number</span></span>  <br/> <span data-ttu-id="6470b-830">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-830">driver's licence number</span></span>  <br/> <span data-ttu-id="6470b-831">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6470b-831">driving license number</span></span>  <br/> <span data-ttu-id="6470b-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="6470b-832">dlno#</span></span>  <br/> <span data-ttu-id="6470b-833">körkort</span><span class="sxs-lookup"><span data-stu-id="6470b-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="6470b-834">영국의</span><span class="sxs-lookup"><span data-stu-id="6470b-834">UK</span></span>

<span data-ttu-id="6470b-835">자세한 내용은 영국 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6470b-835">For details, see the section "U.K.</span></span> <span data-ttu-id="6470b-836">[중요 한 정보 유형에 서 확인 되는](what-the-sensitive-information-types-look-for.md)운전 면허 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="6470b-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6470b-837">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6470b-837">See also</span></span>

[<span data-ttu-id="6470b-838">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="6470b-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

