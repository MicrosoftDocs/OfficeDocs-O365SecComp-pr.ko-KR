---
title: EU 운전 면허 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: 이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 드라이버의 라이선스 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: 86be7b52aed7581fd62ab595ac2c4b63ab33aab3
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217748"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="6adfe-104">EU 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-104">EU Driver's License Number</span></span>

<span data-ttu-id="6adfe-p102">이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 드라이버의 라이선스 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="6adfe-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="6adfe-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-108">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-108">Format</span></span>

<span data-ttu-id="6adfe-109">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-110">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-110">Pattern</span></span>

<span data-ttu-id="6adfe-111">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6adfe-112">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-112">Checksum</span></span>

<span data-ttu-id="6adfe-113">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-114">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-114">Definition</span></span>

<span data-ttu-id="6adfe-115">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-116">정규식이 해당 `Regex_austria_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-117">from `Keywords_austria_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="6adfe-118">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-118">Keywords</span></span>

<span data-ttu-id="6adfe-119">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-119"></span></span>
|<span data-ttu-id="6adfe-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-121">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-121">dl#</span></span>  <br/> <span data-ttu-id="6adfe-122">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-122">driver license</span></span>  <br/> <span data-ttu-id="6adfe-123">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-123">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-124">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-124">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-125">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-125">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-126">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-127">운전의 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-127">driver's licence</span></span>  <br/> <span data-ttu-id="6adfe-128">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-128">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-129">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-129">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-130">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="6adfe-131">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-131">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-132">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-133">fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="6adfe-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="6adfe-134">fuhrerschein republik osterreich</span><span class="sxs-lookup"><span data-stu-id="6adfe-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="6adfe-135">벨기에</span><span class="sxs-lookup"><span data-stu-id="6adfe-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-136">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-136">Format</span></span>

<span data-ttu-id="6adfe-137">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-138">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-138">Pattern</span></span>

<span data-ttu-id="6adfe-139">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6adfe-140">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-140">Checksum</span></span>

<span data-ttu-id="6adfe-141">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-142">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-142">Definition</span></span>

<span data-ttu-id="6adfe-143">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-144">정규식이 해당 `Regex_belgium_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-145">from `Keywords_belgium_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="6adfe-146">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-146">Keywords</span></span>

<span data-ttu-id="6adfe-147">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-147"></span></span>
|<span data-ttu-id="6adfe-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-149">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-149">dl#</span></span>  <br/> <span data-ttu-id="6adfe-150">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-150">driver license</span></span>  <br/> <span data-ttu-id="6adfe-151">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-151">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-152">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-152">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-153">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-153">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-154">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-155">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-156">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-156">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-157">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-157">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-158">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-158">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-159">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="6adfe-160">rijbewijs</span></span>  <br/> <span data-ttu-id="6adfe-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="6adfe-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="6adfe-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6adfe-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="6adfe-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6adfe-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="6adfe-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6adfe-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="6adfe-165">führerschein-veiligheid</span><span class="sxs-lookup"><span data-stu-id="6adfe-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="6adfe-166">fuehrerschein-veiligheid</span><span class="sxs-lookup"><span data-stu-id="6adfe-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="6adfe-167">fuehrerschein-veiligheid</span><span class="sxs-lookup"><span data-stu-id="6adfe-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="6adfe-168">불가리아</span><span class="sxs-lookup"><span data-stu-id="6adfe-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-169">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-169">Format</span></span>

<span data-ttu-id="6adfe-170">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-171">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-171">Pattern</span></span>

<span data-ttu-id="6adfe-172">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6adfe-173">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-173">Checksum</span></span>

<span data-ttu-id="6adfe-174">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-175">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-175">Definition</span></span>

<span data-ttu-id="6adfe-176">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-177">정규식이 해당 `Regex_bulgaria_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-178">from `Keywords_bulgaria_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="6adfe-179">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-179">Keywords</span></span>

<span data-ttu-id="6adfe-180">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-180"></span></span>
|<span data-ttu-id="6adfe-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-182">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-182">dl#</span></span>  <br/> <span data-ttu-id="6adfe-183">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-183">driver license</span></span>  <br/> <span data-ttu-id="6adfe-184">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-184">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-185">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-185">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-186">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-186">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-187">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-188">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-189">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-189">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-190">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-190">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-191">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-191">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-192">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-192">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-193">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="6adfe-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="6adfe-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="6adfe-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="6adfe-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="6adfe-196">сумпс</span></span>  <br/> <span data-ttu-id="6adfe-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="6adfe-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="6adfe-198">크로아티아</span><span class="sxs-lookup"><span data-stu-id="6adfe-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-199">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-199">Format</span></span>

<span data-ttu-id="6adfe-200">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-201">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-201">Pattern</span></span>

<span data-ttu-id="6adfe-202">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6adfe-203">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-203">Checksum</span></span>

<span data-ttu-id="6adfe-204">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-205">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-205">Definition</span></span>

<span data-ttu-id="6adfe-206">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-207">정규식이 해당 `Regex_croatia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-208">from `Keywords_croatia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="6adfe-209">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-209">Keywords</span></span>

<span data-ttu-id="6adfe-210">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-210"></span></span>
|<span data-ttu-id="6adfe-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-212">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-212">dl#</span></span>  <br/> <span data-ttu-id="6adfe-213">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-213">driver license</span></span>  <br/> <span data-ttu-id="6adfe-214">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-214">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-215">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-215">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-216">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-216">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-217">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-218">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-219">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-219">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-220">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-220">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-221">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-221">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-222">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-222">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-223">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="6adfe-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="6adfe-225">키프로스</span><span class="sxs-lookup"><span data-stu-id="6adfe-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-226">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-226">Format</span></span>

<span data-ttu-id="6adfe-227">공백과 구분 기호를 사용 하지 않고 12 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-228">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-228">Pattern</span></span>

<span data-ttu-id="6adfe-229">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6adfe-230">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-230">Checksum</span></span>

<span data-ttu-id="6adfe-231">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-232">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-232">Definition</span></span>

<span data-ttu-id="6adfe-233">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-234">정규식이 해당 `Regex_cyprus_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-235">from `Keywords_cyprus_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-236">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-236">Keywords</span></span>

<span data-ttu-id="6adfe-237">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-237"></span></span>
|<span data-ttu-id="6adfe-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-239">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-239">dl#</span></span>  <br/> <span data-ttu-id="6adfe-240">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-240">driver license</span></span>  <br/> <span data-ttu-id="6adfe-241">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-241">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-242">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-242">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-243">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-243">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-244">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-245">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-246">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-246">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-247">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-247">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-248">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-248">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-249">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="6adfe-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="6adfe-251">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="6adfe-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-252">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-252">Format</span></span>

<span data-ttu-id="6adfe-253">2 개의 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-254">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-254">Pattern</span></span>

<span data-ttu-id="6adfe-255">8 개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="6adfe-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="6adfe-256">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6adfe-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="6adfe-257">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="6adfe-257">A space (optional)</span></span>
    
- <span data-ttu-id="6adfe-258">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6adfe-259">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-259">Checksum</span></span>

<span data-ttu-id="6adfe-260">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-261">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-261">Definition</span></span>

<span data-ttu-id="6adfe-262">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-263">정규식이 해당 `Regex_czech_republic_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-264">from `Keywords_czech_republic_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="6adfe-265">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-265">Keywords</span></span>

<span data-ttu-id="6adfe-266">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-266"></span></span>
|<span data-ttu-id="6adfe-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-268">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-268">dl#</span></span>  <br/> <span data-ttu-id="6adfe-269">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-269">driver license</span></span>  <br/> <span data-ttu-id="6adfe-270">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-270">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-271">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-271">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-272">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-272">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-273">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-274">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-275">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-275">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-276">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-276">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-277">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-277">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-278">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-278">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-279">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-279">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-280">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="6adfe-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="6adfe-282">덴마크</span><span class="sxs-lookup"><span data-stu-id="6adfe-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-283">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-283">Format</span></span>

<span data-ttu-id="6adfe-284">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-285">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-285">Pattern</span></span>

<span data-ttu-id="6adfe-286">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6adfe-287">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-287">Checksum</span></span>

<span data-ttu-id="6adfe-288">예</span><span class="sxs-lookup"><span data-stu-id="6adfe-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-289">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-289">Definition</span></span>

<span data-ttu-id="6adfe-290">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-291">정규식이 해당 `Regex_denmark_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-292">from `Keywords_denmark_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="6adfe-293">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-293">Keywords</span></span>

<span data-ttu-id="6adfe-294">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-294"></span></span>
|<span data-ttu-id="6adfe-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-296">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-296">dl#</span></span>  <br/> <span data-ttu-id="6adfe-297">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-297">driver license</span></span>  <br/> <span data-ttu-id="6adfe-298">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-298">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-299">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-299">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-300">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-300">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-301">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-302">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-303">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-303">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-304">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-304">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-305">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-305">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-306">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-306">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-307">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="6adfe-308">kørekort</span></span>  <br/> <span data-ttu-id="6adfe-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="6adfe-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="6adfe-310">에스토니아</span><span class="sxs-lookup"><span data-stu-id="6adfe-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-311">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-311">Format</span></span>

<span data-ttu-id="6adfe-312">2 개의 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-313">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-313">Pattern</span></span>

<span data-ttu-id="6adfe-314">2 개의 문자와 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="6adfe-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="6adfe-315">문자 "ET" (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6adfe-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="6adfe-316">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6adfe-317">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-317">Checksum</span></span>

<span data-ttu-id="6adfe-318">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-319">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-319">Definition</span></span>

<span data-ttu-id="6adfe-320">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-321">정규식이 해당 `Regex_estonia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-322">from `Keywords_estonia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-323">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-323">Keywords</span></span>

<span data-ttu-id="6adfe-324">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-324"></span></span>
|<span data-ttu-id="6adfe-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-326">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-326">dl#</span></span>  <br/> <span data-ttu-id="6adfe-327">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-327">driver license</span></span>  <br/> <span data-ttu-id="6adfe-328">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-328">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-329">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-329">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-330">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-330">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-331">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-331">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-332">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-333">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-334">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-334">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-335">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-335">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-336">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-336">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-337">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-338">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="6adfe-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="6adfe-339">핀란드</span><span class="sxs-lookup"><span data-stu-id="6adfe-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-340">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-340">Format</span></span>

<span data-ttu-id="6adfe-341">하이픈을 포함하는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-342">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-342">Pattern</span></span>

<span data-ttu-id="6adfe-343">하이픈을 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="6adfe-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="6adfe-344">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-344">Six digits</span></span> 
    
- <span data-ttu-id="6adfe-345">하이픈</span><span class="sxs-lookup"><span data-stu-id="6adfe-345">A hyphen</span></span>
    
-  <span data-ttu-id="6adfe-346">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="6adfe-347">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-347">Checksum</span></span>

<span data-ttu-id="6adfe-348">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-349">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-349">Definition</span></span>

<span data-ttu-id="6adfe-350">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-351">정규식이 해당 `Regex_finland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-352">from `Keywords_finland_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-353">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-353">Keywords</span></span>

<span data-ttu-id="6adfe-354">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-354"></span></span>
|<span data-ttu-id="6adfe-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-356">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-356">dl#</span></span>  <br/> <span data-ttu-id="6adfe-357">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-357">driver license</span></span>  <br/> <span data-ttu-id="6adfe-358">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-358">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-359">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-359">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-360">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-360">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-361">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-362">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-363">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-363">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-364">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-364">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-365">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-365">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-366">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-366">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-367">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="6adfe-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="6adfe-369">프랑스</span><span class="sxs-lookup"><span data-stu-id="6adfe-369">France</span></span>

<span data-ttu-id="6adfe-370">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"경기도 운전 면허 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6adfe-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="6adfe-371">독일</span><span class="sxs-lookup"><span data-stu-id="6adfe-371">Germany</span></span>

<span data-ttu-id="6adfe-372">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일어 운전 면허 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6adfe-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="6adfe-373">그리스</span><span class="sxs-lookup"><span data-stu-id="6adfe-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-374">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-374">Format</span></span>

<span data-ttu-id="6adfe-375">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-376">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-376">Pattern</span></span>

 <span data-ttu-id="6adfe-377">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="6adfe-378">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-378">Checksum</span></span>

<span data-ttu-id="6adfe-379">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-380">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-380">Definition</span></span>

<span data-ttu-id="6adfe-381">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-382">정규식이 해당 `Regex_greece_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-383">from `Keywords_greece_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-384">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-384">Keywords</span></span>

<span data-ttu-id="6adfe-385">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-385"></span></span>
|<span data-ttu-id="6adfe-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-387">dlL</span><span class="sxs-lookup"><span data-stu-id="6adfe-387">dlL#</span></span>  <br/> <span data-ttu-id="6adfe-388">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-388">driver license</span></span>  <br/> <span data-ttu-id="6adfe-389">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-389">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-390">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-390">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-391">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-391">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-392">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-393">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-394">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-394">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-395">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-395">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-396">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-396">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-397">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-397">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-398">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="6adfe-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="6adfe-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="6adfe-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="6adfe-401">헝가리</span><span class="sxs-lookup"><span data-stu-id="6adfe-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-402">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-402">Format</span></span>

<span data-ttu-id="6adfe-403">2 개의 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-404">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-404">Pattern</span></span>

<span data-ttu-id="6adfe-405">2 개의 문자와 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="6adfe-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="6adfe-406">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6adfe-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="6adfe-407">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6adfe-408">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-408">Checksum</span></span>

<span data-ttu-id="6adfe-409">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-410">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-410">Definition</span></span>

<span data-ttu-id="6adfe-411">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-412">정규식이 해당 `Regex_hungary_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-413">from `Keywords_hungary_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-414">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-414">Keywords</span></span>

<span data-ttu-id="6adfe-415">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-415"></span></span>
|<span data-ttu-id="6adfe-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-417">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-417">dl#</span></span>  <br/> <span data-ttu-id="6adfe-418">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-418">driver license</span></span>  <br/> <span data-ttu-id="6adfe-419">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-419">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-420">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-420">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-421">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-421">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-422">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-423">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-424">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-424">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-425">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-425">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-426">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-426">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-427">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-427">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-428">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-429">vezetoi</span><span class="sxs-lookup"><span data-stu-id="6adfe-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="6adfe-430">Ireland</span><span class="sxs-lookup"><span data-stu-id="6adfe-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-431">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-431">Format</span></span>

<span data-ttu-id="6adfe-432">6 자리 숫자와 4 개 문자</span><span class="sxs-lookup"><span data-stu-id="6adfe-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-433">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-433">Pattern</span></span>

<span data-ttu-id="6adfe-434">6 자리 숫자와 4 개 문자:</span><span class="sxs-lookup"><span data-stu-id="6adfe-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="6adfe-435">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-435">Six digits</span></span>
    
- <span data-ttu-id="6adfe-436">4 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6adfe-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6adfe-437">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-437">Checksum</span></span>

<span data-ttu-id="6adfe-438">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-439">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-439">Definition</span></span>

<span data-ttu-id="6adfe-440">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-441">정규식이 해당 `Regex_ireland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-442">from `Keywords_ireland_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-443">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-443">Keywords</span></span>

<span data-ttu-id="6adfe-444">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-444"></span></span>
|<span data-ttu-id="6adfe-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-446">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-446">dl#</span></span>  <br/> <span data-ttu-id="6adfe-447">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-447">driver license</span></span>  <br/> <span data-ttu-id="6adfe-448">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-448">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-449">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-449">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-450">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-450">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-451">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-452">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-453">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-453">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-454">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-454">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-455">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-455">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-456">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-456">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-457">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="6adfe-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="6adfe-459">이탈리아</span><span class="sxs-lookup"><span data-stu-id="6adfe-459">Italy</span></span>

<span data-ttu-id="6adfe-460">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"이탈리아 운전 면허 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6adfe-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="6adfe-461">라트비아</span><span class="sxs-lookup"><span data-stu-id="6adfe-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-462">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-462">Format</span></span>

<span data-ttu-id="6adfe-463">3 개의 문자 및 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-464">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-464">Pattern</span></span>

<span data-ttu-id="6adfe-465">3 개의 문자 및 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="6adfe-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="6adfe-466">3 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6adfe-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="6adfe-467">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6adfe-468">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-468">Checksum</span></span>

<span data-ttu-id="6adfe-469">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-470">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-470">Definition</span></span>

<span data-ttu-id="6adfe-471">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-472">정규식이 해당 `Regex_latvia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-473">from `Keywords_latvia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-474">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-474">Keywords</span></span>

<span data-ttu-id="6adfe-475">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-475"></span></span>
|<span data-ttu-id="6adfe-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-477">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-477">dl#</span></span>  <br/> <span data-ttu-id="6adfe-478">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-478">driver license</span></span>  <br/> <span data-ttu-id="6adfe-479">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-479">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-480">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-480">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-481">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-481">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-482">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-483">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-484">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-484">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-485">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-485">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-486">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-486">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-487">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-487">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-488">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="6adfe-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="6adfe-490">리투아니아</span><span class="sxs-lookup"><span data-stu-id="6adfe-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-491">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-491">Format</span></span>

<span data-ttu-id="6adfe-492">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-493">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-493">Pattern</span></span>

 <span data-ttu-id="6adfe-494">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="6adfe-495">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-495">Checksum</span></span>

<span data-ttu-id="6adfe-496">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-497">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-497">Definition</span></span>

<span data-ttu-id="6adfe-498">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-499">정규식이 해당 `Regex_lithuania_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-500">from `Keywords_lithuania_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-501">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-501">Keywords</span></span>

<span data-ttu-id="6adfe-502">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-502"></span></span>
|<span data-ttu-id="6adfe-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-504">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-504">dl#</span></span>  <br/> <span data-ttu-id="6adfe-505">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-505">driver license</span></span>  <br/> <span data-ttu-id="6adfe-506">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-506">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-507">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-507">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-508">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-508">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-509">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-510">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-511">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-511">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-512">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-512">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-513">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-513">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-514">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-514">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-515">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="6adfe-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="6adfe-517">셈</span><span class="sxs-lookup"><span data-stu-id="6adfe-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-518">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-518">Format</span></span>

<span data-ttu-id="6adfe-519">공백과 구분 기호가 없는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-520">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-520">Pattern</span></span>

 <span data-ttu-id="6adfe-521">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="6adfe-522">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-522">Checksum</span></span>

<span data-ttu-id="6adfe-523">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-524">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-524">Definition</span></span>

<span data-ttu-id="6adfe-525">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-526">정규식이 해당 `Regex_luxemburg_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-527">from `Keywords_luxemburg_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-528">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-528">Keywords</span></span>

<span data-ttu-id="6adfe-529">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-529"></span></span>
|<span data-ttu-id="6adfe-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-531">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-531">dl#</span></span>  <br/> <span data-ttu-id="6adfe-532">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-532">driver license</span></span>  <br/> <span data-ttu-id="6adfe-533">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-533">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-534">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-534">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-535">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-535">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-536">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-537">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-538">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-538">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-539">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-539">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-540">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-540">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-541">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-541">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-542">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="6adfe-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="6adfe-544">몰타</span><span class="sxs-lookup"><span data-stu-id="6adfe-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-545">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-545">Format</span></span>

<span data-ttu-id="6adfe-546">지정 된 패턴에서 두 개의 문자와 6 자리 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="6adfe-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-547">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-547">Pattern</span></span>

<span data-ttu-id="6adfe-548">두 문자와 6 자리 숫자의 조합:</span><span class="sxs-lookup"><span data-stu-id="6adfe-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="6adfe-549">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6adfe-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="6adfe-550">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="6adfe-550">A space (optional)</span></span>
    
- <span data-ttu-id="6adfe-551">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-551">Three digits</span></span>
    
- <span data-ttu-id="6adfe-552">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="6adfe-552">A space (optional)</span></span>
    
- <span data-ttu-id="6adfe-553">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6adfe-554">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-554">Checksum</span></span>

<span data-ttu-id="6adfe-555">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-556">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-556">Definition</span></span>

<span data-ttu-id="6adfe-557">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-558">정규식이 해당 `Regex_malta_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-559">from `Keywords_malta_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-560">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-560">Keywords</span></span>

<span data-ttu-id="6adfe-561">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-561"></span></span>
|<span data-ttu-id="6adfe-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-563">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-563">dl#</span></span>  <br/> <span data-ttu-id="6adfe-564">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-564">driver license</span></span>  <br/> <span data-ttu-id="6adfe-565">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-565">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-566">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-566">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-567">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-567">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-568">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-569">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-570">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-570">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-571">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-571">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-572">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-572">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-573">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-573">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-574">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-575">liċenzja tas-sewqan</span><span class="sxs-lookup"><span data-stu-id="6adfe-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="6adfe-576">네덜란드</span><span class="sxs-lookup"><span data-stu-id="6adfe-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-577">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-577">Format</span></span>

<span data-ttu-id="6adfe-578">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-579">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-579">Pattern</span></span>

<span data-ttu-id="6adfe-580">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6adfe-581">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-581">Checksum</span></span>

<span data-ttu-id="6adfe-582">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-583">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-583">Definition</span></span>

<span data-ttu-id="6adfe-584">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-585">정규식이 해당 `Regex_netherlands_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-586">from `Keywords_netherlands_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-587">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-587">Keywords</span></span>

<span data-ttu-id="6adfe-588">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-588"></span></span>
|<span data-ttu-id="6adfe-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-590">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-590">dl#</span></span>  <br/> <span data-ttu-id="6adfe-591">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-591">driver license</span></span>  <br/> <span data-ttu-id="6adfe-592">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-592">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-593">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-593">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-594">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-594">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-595">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-596">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-597">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-597">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-598">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-598">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-599">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-599">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-600">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-600">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-601">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-602">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="6adfe-602">permis de conduire</span></span>  <br/> <span data-ttu-id="6adfe-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="6adfe-603">rijbewijs</span></span>  <br/> <span data-ttu-id="6adfe-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="6adfe-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="6adfe-605">폴란드</span><span class="sxs-lookup"><span data-stu-id="6adfe-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-606">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-606">Format</span></span>

<span data-ttu-id="6adfe-607">두 개의 슬래시를 포함 하는 14 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-608">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-608">Pattern</span></span>

<span data-ttu-id="6adfe-609">14 자리 숫자와 2 개의 슬래시:</span><span class="sxs-lookup"><span data-stu-id="6adfe-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="6adfe-610">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-610">Five digits</span></span> 
    
- <span data-ttu-id="6adfe-611">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="6adfe-611">A forward slash</span></span>
    
- <span data-ttu-id="6adfe-612">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-612">Two digits</span></span>
    
- <span data-ttu-id="6adfe-613">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="6adfe-613">A forward slash</span></span>
    
- <span data-ttu-id="6adfe-614">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6adfe-615">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-615">Checksum</span></span>

<span data-ttu-id="6adfe-616">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-617">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-617">Definition</span></span>

<span data-ttu-id="6adfe-618">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-619">정규식이 해당 `Regex_poland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-620">from `Keywords_poland_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-621">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-621">Keywords</span></span>

<span data-ttu-id="6adfe-622">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-622"></span></span>
|<span data-ttu-id="6adfe-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-624">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-624">dl#</span></span>  <br/> <span data-ttu-id="6adfe-625">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-625">driver license</span></span>  <br/> <span data-ttu-id="6adfe-626">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-626">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-627">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-627">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-628">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-628">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-629">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-630">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-631">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-631">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-632">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-632">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-633">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-633">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-634">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-634">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-635">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-636">prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="6adfe-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="6adfe-637">포르투갈</span><span class="sxs-lookup"><span data-stu-id="6adfe-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-638">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-638">Format</span></span>

<span data-ttu-id="6adfe-639">두 개의 문자와 지정 된 패턴에 있는 일곱 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-640">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-640">Pattern</span></span>

<span data-ttu-id="6adfe-641">두 문자 다음에 특수 문자를 사용한 7 개의 숫자를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="6adfe-642">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6adfe-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="6adfe-643">하이픈</span><span class="sxs-lookup"><span data-stu-id="6adfe-643">A hyphen</span></span>
    
- <span data-ttu-id="6adfe-644">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-644">Six digits</span></span>
    
- <span data-ttu-id="6adfe-645">공백</span><span class="sxs-lookup"><span data-stu-id="6adfe-645">A space</span></span>
    
- <span data-ttu-id="6adfe-646">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6adfe-647">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-647">Checksum</span></span>

<span data-ttu-id="6adfe-648">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-649">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-649">Definition</span></span>

<span data-ttu-id="6adfe-650">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-651">정규식이 해당 `Regex_portugal_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-652">from `Keywords_portugal_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-653">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-653">Keywords</span></span>

<span data-ttu-id="6adfe-654">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-654"></span></span>
|<span data-ttu-id="6adfe-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-656">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-656">dl#</span></span>  <br/> <span data-ttu-id="6adfe-657">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-657">driver license</span></span>  <br/> <span data-ttu-id="6adfe-658">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-658">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-659">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-659">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-660">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-660">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-661">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-662">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-663">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-663">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-664">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-664">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-665">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-665">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-666">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-666">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-667">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-668">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="6adfe-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="6adfe-669">루마니아</span><span class="sxs-lookup"><span data-stu-id="6adfe-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-670">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-670">Format</span></span>

<span data-ttu-id="6adfe-671">한 문자 다음에 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-672">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-672">Pattern</span></span>

<span data-ttu-id="6adfe-673">1 개의 문자 다음에 8 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="6adfe-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="6adfe-674">1 개 문자 (대/소문자 구분 안 함) 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="6adfe-675">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6adfe-676">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-676">Checksum</span></span>

<span data-ttu-id="6adfe-677">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-678">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-678">Definition</span></span>

<span data-ttu-id="6adfe-679">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-680">정규식이 해당 `Regex_romania_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-681">from `Keywords_romania_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-682">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-682">Keywords</span></span>

<span data-ttu-id="6adfe-683">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-683"></span></span>
|<span data-ttu-id="6adfe-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-685">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-685">dl#</span></span>  <br/> <span data-ttu-id="6adfe-686">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-686">driver license</span></span>  <br/> <span data-ttu-id="6adfe-687">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-687">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-688">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-688">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-689">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-689">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-690">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-691">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-692">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-692">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-693">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-693">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-694">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-694">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-695">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-695">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-696">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="6adfe-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="6adfe-698">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="6adfe-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-699">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-699">Format</span></span>

<span data-ttu-id="6adfe-700">한 문자 다음에 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-701">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-701">Pattern</span></span>

<span data-ttu-id="6adfe-702">한 문자 다음에 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="6adfe-703">1 개 문자 (대/소문자 구분 안 함) 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="6adfe-704">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="6adfe-705">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-705">Checksum</span></span>

<span data-ttu-id="6adfe-706">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-707">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-707">Definition</span></span>

<span data-ttu-id="6adfe-708">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-709">정규식이 해당 `Regex_slovakia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-710">from `Keywords_slovakia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-711">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-711">Keywords</span></span>

<span data-ttu-id="6adfe-712">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-712"></span></span>
|<span data-ttu-id="6adfe-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-714">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-714">dl#</span></span>  <br/> <span data-ttu-id="6adfe-715">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-715">driver license</span></span>  <br/> <span data-ttu-id="6adfe-716">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-716">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-717">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-717">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-718">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-718">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-719">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-720">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-721">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-721">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-722">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-722">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-723">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-723">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-724">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-724">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-725">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="6adfe-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="6adfe-727">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="6adfe-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-728">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-728">Format</span></span>

<span data-ttu-id="6adfe-729">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-730">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-730">Pattern</span></span>

<span data-ttu-id="6adfe-731">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6adfe-732">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-732">Checksum</span></span>

<span data-ttu-id="6adfe-733">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-734">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-734">Definition</span></span>

<span data-ttu-id="6adfe-735">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-736">정규식이 해당 `Regex_slovenia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-737">from `Keywords_slovenia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-738">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-738">Keywords</span></span>

<span data-ttu-id="6adfe-739">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-739"></span></span>
|<span data-ttu-id="6adfe-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-741">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-741">dl#</span></span>  <br/> <span data-ttu-id="6adfe-742">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-742">driver license</span></span>  <br/> <span data-ttu-id="6adfe-743">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-743">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-744">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-744">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-745">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-745">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-746">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-747">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-748">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-748">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-749">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-749">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-750">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-750">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-751">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-751">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-752">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="6adfe-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="6adfe-754">스페인</span><span class="sxs-lookup"><span data-stu-id="6adfe-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-755">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-755">Format</span></span>

<span data-ttu-id="6adfe-756">8 자리 숫자와 문자 1 개</span><span class="sxs-lookup"><span data-stu-id="6adfe-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-757">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-757">Pattern</span></span>

<span data-ttu-id="6adfe-758">8 자리 숫자와 문자 1 개:</span><span class="sxs-lookup"><span data-stu-id="6adfe-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="6adfe-759">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-759">Eight digits</span></span> 
    
- <span data-ttu-id="6adfe-760">1 자리 숫자 또는 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="6adfe-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6adfe-761">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-761">Checksum</span></span>

<span data-ttu-id="6adfe-762">예</span><span class="sxs-lookup"><span data-stu-id="6adfe-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-763">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-763">Definition</span></span>

<span data-ttu-id="6adfe-764">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-765">이 함수 `Func_spain_eu_driver's_license_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-766">from `Keywords_spain_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6adfe-767">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-767">Keywords</span></span>

<span data-ttu-id="6adfe-768">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-768"></span></span>
|<span data-ttu-id="6adfe-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-770">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-771">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-771">dl#</span></span>  <br/> <span data-ttu-id="6adfe-772">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-772">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-773">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-773">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-774">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-774">driver license</span></span>  <br/> <span data-ttu-id="6adfe-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-775">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-776">
drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-776">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-777">운전의 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-777">driver's licence</span></span>  <br/> <span data-ttu-id="6adfe-778">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-778">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-779">driving licence
</span><span class="sxs-lookup"><span data-stu-id="6adfe-779">driving licence</span></span>  <br/> <span data-ttu-id="6adfe-780">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-780">driving license</span></span>  <br/> <span data-ttu-id="6adfe-781">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-781">driver licence number</span></span>  <br/> <span data-ttu-id="6adfe-782">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-782">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-783">영향 요소 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-783">drivers licence number</span></span>  <br/> <span data-ttu-id="6adfe-784">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-784">drivers license number</span></span>  <br/> <span data-ttu-id="6adfe-785">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-785">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-786">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-786">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-787">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-787">driving licence number</span></span>  <br/> <span data-ttu-id="6adfe-788">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-788">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-789">추진 허용</span><span class="sxs-lookup"><span data-stu-id="6adfe-789">driving permit</span></span>  <br/> <span data-ttu-id="6adfe-790">제어 허용 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-790">driving permit number</span></span>  <br/> <span data-ttu-id="6adfe-791">permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="6adfe-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="6adfe-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="6adfe-792">permiso conducción</span></span>  <br/> <span data-ttu-id="6adfe-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="6adfe-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="6adfe-794">número de 네트워크 de conducir</span><span class="sxs-lookup"><span data-stu-id="6adfe-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="6adfe-795">número carnet conducir</span><span class="sxs-lookup"><span data-stu-id="6adfe-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="6adfe-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="6adfe-796">licencia conducir</span></span>  <br/> <span data-ttu-id="6adfe-797">número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="6adfe-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="6adfe-798">número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="6adfe-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="6adfe-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="6adfe-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="6adfe-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="6adfe-800">permiso conducir</span></span>  <br/> <span data-ttu-id="6adfe-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="6adfe-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="6adfe-802">el carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="6adfe-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="6adfe-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="6adfe-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="6adfe-804">스웨덴</span><span class="sxs-lookup"><span data-stu-id="6adfe-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="6adfe-805">형식</span><span class="sxs-lookup"><span data-stu-id="6adfe-805">Format</span></span>

<span data-ttu-id="6adfe-806">하이픈을 포함 하는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6adfe-807">패턴</span><span class="sxs-lookup"><span data-stu-id="6adfe-807">Pattern</span></span>

<span data-ttu-id="6adfe-808">하이픈을 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="6adfe-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="6adfe-809">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-809">Six digits</span></span> 
    
- <span data-ttu-id="6adfe-810">하이픈</span><span class="sxs-lookup"><span data-stu-id="6adfe-810">A hyphen</span></span>
    
- <span data-ttu-id="6adfe-811">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="6adfe-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6adfe-812">체크섬</span><span class="sxs-lookup"><span data-stu-id="6adfe-812">Checksum</span></span>

<span data-ttu-id="6adfe-813">없음</span><span class="sxs-lookup"><span data-stu-id="6adfe-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6adfe-814">정의</span><span class="sxs-lookup"><span data-stu-id="6adfe-814">Definition</span></span>

<span data-ttu-id="6adfe-815">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6adfe-816">정규식이 해당 `Regex_sweden_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6adfe-817">from `Keywords_sweden_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="6adfe-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="6adfe-818">키워드</span><span class="sxs-lookup"><span data-stu-id="6adfe-818">Keywords</span></span>

<span data-ttu-id="6adfe-819">| |</span><span class="sxs-lookup"><span data-stu-id="6adfe-819"></span></span>
|<span data-ttu-id="6adfe-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="6adfe-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6adfe-821">dl</span><span class="sxs-lookup"><span data-stu-id="6adfe-821">dl#</span></span>  <br/> <span data-ttu-id="6adfe-822">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-822">driver license</span></span>  <br/> <span data-ttu-id="6adfe-823">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-823">driver license number</span></span>  <br/> <span data-ttu-id="6adfe-824">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="6adfe-824">driver licence</span></span>  <br/> <span data-ttu-id="6adfe-825">drivers lic</span><span class="sxs-lookup"><span data-stu-id="6adfe-825">drivers lic.</span></span>  <br/> <span data-ttu-id="6adfe-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="6adfe-826">drivers license</span></span>  <br/> <span data-ttu-id="6adfe-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6adfe-827">drivers licence</span></span>  <br/> <span data-ttu-id="6adfe-828">운전 면허</span><span class="sxs-lookup"><span data-stu-id="6adfe-828">driver's license</span></span>  <br/> <span data-ttu-id="6adfe-829">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-829">driver's license number</span></span>  <br/> <span data-ttu-id="6adfe-830">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-830">driver's licence number</span></span>  <br/> <span data-ttu-id="6adfe-831">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="6adfe-831">driving license number</span></span>  <br/> <span data-ttu-id="6adfe-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="6adfe-832">dlno#</span></span>  <br/> <span data-ttu-id="6adfe-833">körkort</span><span class="sxs-lookup"><span data-stu-id="6adfe-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="6adfe-834">영국의</span><span class="sxs-lookup"><span data-stu-id="6adfe-834">UK</span></span>

<span data-ttu-id="6adfe-p103">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"영국 운전 면허 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6adfe-p103">For details, see the section "U.K. Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6adfe-837">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6adfe-837">See also</span></span>

[<span data-ttu-id="6adfe-838">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="6adfe-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

