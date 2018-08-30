---
title: EU 운전 면허 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: 이 항목에서는 EU 운전 면허 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
ms.openlocfilehash: 065684249f9766d567c63e6b8170d36f56692e45
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533461"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="50d00-104">EU 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-104">EU Driver's License Number</span></span>

<span data-ttu-id="50d00-p102">이 항목에서는 EU 운전 면허 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="50d00-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="50d00-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="50d00-108">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-108">Format</span></span>

<span data-ttu-id="50d00-109">공백 및 구분 기호 없이 8 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-110">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-110">Pattern</span></span>

<span data-ttu-id="50d00-111">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="50d00-112">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-112">Checksum</span></span>

<span data-ttu-id="50d00-113">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-114">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-114">Definition</span></span>

<span data-ttu-id="50d00-115">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-116">정규식 `Regex_austria_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-117">키워드에서 `Keywords_austria_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="50d00-118">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-118">Keywords</span></span>

<span data-ttu-id="50d00-119">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-119"></span></span>
|<span data-ttu-id="50d00-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-121">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-121">dl#</span></span>  <br/> <span data-ttu-id="50d00-122">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-122">driver license</span></span>  <br/> <span data-ttu-id="50d00-123">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-123">driver license number</span></span>  <br/> <span data-ttu-id="50d00-124">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-124">driver licence</span></span>  <br/> <span data-ttu-id="50d00-125">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-125">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-126">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-126">drivers license</span></span>  <br/> <span data-ttu-id="50d00-127">드라이버의 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-127">driver's licence</span></span>  <br/> <span data-ttu-id="50d00-128">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-128">driver's license</span></span>  <br/> <span data-ttu-id="50d00-129">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-129">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-130">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="50d00-131">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-131">driving license number</span></span>  <br/> <span data-ttu-id="50d00-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-132">dlno#</span></span>  <br/> <span data-ttu-id="50d00-133">fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="50d00-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="50d00-134">fuhrerschein republik osterreich</span><span class="sxs-lookup"><span data-stu-id="50d00-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="50d00-135">벨기에</span><span class="sxs-lookup"><span data-stu-id="50d00-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="50d00-136">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-136">Format</span></span>

<span data-ttu-id="50d00-137">공백 및 구분 기호 없이 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-138">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-138">Pattern</span></span>

<span data-ttu-id="50d00-139">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="50d00-140">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-140">Checksum</span></span>

<span data-ttu-id="50d00-141">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-142">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-142">Definition</span></span>

<span data-ttu-id="50d00-143">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-144">정규식 `Regex_belgium_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-145">키워드에서 `Keywords_belgium_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="50d00-146">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-146">Keywords</span></span>

<span data-ttu-id="50d00-147">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-147"></span></span>
|<span data-ttu-id="50d00-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-149">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-149">dl#</span></span>  <br/> <span data-ttu-id="50d00-150">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-150">driver license</span></span>  <br/> <span data-ttu-id="50d00-151">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-151">driver license number</span></span>  <br/> <span data-ttu-id="50d00-152">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-152">driver licence</span></span>  <br/> <span data-ttu-id="50d00-153">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-153">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-154">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-154">drivers license</span></span>  <br/> <span data-ttu-id="50d00-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-155">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-156">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-156">driver's license</span></span>  <br/> <span data-ttu-id="50d00-157">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-157">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-158">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-158">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-159">dlno#</span></span>  <br/> <span data-ttu-id="50d00-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="50d00-160">rijbewijs</span></span>  <br/> <span data-ttu-id="50d00-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="50d00-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="50d00-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="50d00-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="50d00-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="50d00-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="50d00-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="50d00-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="50d00-165">führerschein nr</span><span class="sxs-lookup"><span data-stu-id="50d00-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="50d00-166">fuehrerschein Nr</span><span class="sxs-lookup"><span data-stu-id="50d00-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="50d00-167">fuehrerschein nr</span><span class="sxs-lookup"><span data-stu-id="50d00-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="50d00-168">불가리아</span><span class="sxs-lookup"><span data-stu-id="50d00-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="50d00-169">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-169">Format</span></span>

<span data-ttu-id="50d00-170">공백 및 구분 기호 없이 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="50d00-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-171">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-171">Pattern</span></span>

<span data-ttu-id="50d00-172">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="50d00-173">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-173">Checksum</span></span>

<span data-ttu-id="50d00-174">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-175">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-175">Definition</span></span>

<span data-ttu-id="50d00-176">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-177">정규식 `Regex_bulgaria_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-178">키워드에서 `Keywords_bulgaria_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="50d00-179">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-179">Keywords</span></span>

<span data-ttu-id="50d00-180">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-180"></span></span>
|<span data-ttu-id="50d00-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-182">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-182">dl#</span></span>  <br/> <span data-ttu-id="50d00-183">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-183">driver license</span></span>  <br/> <span data-ttu-id="50d00-184">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-184">driver license number</span></span>  <br/> <span data-ttu-id="50d00-185">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-185">driver licence</span></span>  <br/> <span data-ttu-id="50d00-186">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-186">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-187">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-187">drivers license</span></span>  <br/> <span data-ttu-id="50d00-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-188">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-189">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-189">driver's license</span></span>  <br/> <span data-ttu-id="50d00-190">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-190">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-191">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-191">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-192">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-192">driving license number</span></span>  <br/> <span data-ttu-id="50d00-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-193">dlno#</span></span>  <br/> <span data-ttu-id="50d00-194">СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МПС</span><span class="sxs-lookup"><span data-stu-id="50d00-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="50d00-195">СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МОТОРНО ПРЕВОЗНО СРЕДСТВО</span><span class="sxs-lookup"><span data-stu-id="50d00-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="50d00-196">СУМПС</span><span class="sxs-lookup"><span data-stu-id="50d00-196">сумпс</span></span>  <br/> <span data-ttu-id="50d00-197">ШОФЬОРСКА КНИЖКА</span><span class="sxs-lookup"><span data-stu-id="50d00-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="50d00-198">크로아티아</span><span class="sxs-lookup"><span data-stu-id="50d00-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="50d00-199">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-199">Format</span></span>

<span data-ttu-id="50d00-200">공백 및 구분 기호 없이 8 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-201">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-201">Pattern</span></span>

<span data-ttu-id="50d00-202">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="50d00-203">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-203">Checksum</span></span>

<span data-ttu-id="50d00-204">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-205">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-205">Definition</span></span>

<span data-ttu-id="50d00-206">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-207">정규식 `Regex_croatia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-208">키워드에서 `Keywords_croatia_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="50d00-209">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-209">Keywords</span></span>

<span data-ttu-id="50d00-210">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-210"></span></span>
|<span data-ttu-id="50d00-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-212">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-212">dl#</span></span>  <br/> <span data-ttu-id="50d00-213">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-213">driver license</span></span>  <br/> <span data-ttu-id="50d00-214">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-214">driver license number</span></span>  <br/> <span data-ttu-id="50d00-215">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-215">driver licence</span></span>  <br/> <span data-ttu-id="50d00-216">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-216">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-217">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-217">drivers license</span></span>  <br/> <span data-ttu-id="50d00-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-218">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-219">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-219">driver's license</span></span>  <br/> <span data-ttu-id="50d00-220">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-220">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-221">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-221">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-222">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-222">driving license number</span></span>  <br/> <span data-ttu-id="50d00-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-223">dlno#</span></span>  <br/> <span data-ttu-id="50d00-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="50d00-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="50d00-225">키프로스</span><span class="sxs-lookup"><span data-stu-id="50d00-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="50d00-226">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-226">Format</span></span>

<span data-ttu-id="50d00-227">공백 및 구분 기호 없이 12 자리</span><span class="sxs-lookup"><span data-stu-id="50d00-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-228">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-228">Pattern</span></span>

<span data-ttu-id="50d00-229">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="50d00-230">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-230">Checksum</span></span>

<span data-ttu-id="50d00-231">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-232">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-232">Definition</span></span>

<span data-ttu-id="50d00-233">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-234">정규식 `Regex_cyprus_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-235">키워드에서 `Keywords_cyprus_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-236">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-236">Keywords</span></span>

<span data-ttu-id="50d00-237">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-237"></span></span>
|<span data-ttu-id="50d00-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-239">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-239">dl#</span></span>  <br/> <span data-ttu-id="50d00-240">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-240">driver license</span></span>  <br/> <span data-ttu-id="50d00-241">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-241">driver license number</span></span>  <br/> <span data-ttu-id="50d00-242">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-242">driver licence</span></span>  <br/> <span data-ttu-id="50d00-243">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-243">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-244">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-244">drivers license</span></span>  <br/> <span data-ttu-id="50d00-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-245">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-246">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-246">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-247">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-247">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-248">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-248">driving license number</span></span>  <br/> <span data-ttu-id="50d00-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-249">dlno#</span></span>  <br/> <span data-ttu-id="50d00-250">ΆΔΕΙΑ ΟΔΉΓΗΣΗΣ</span><span class="sxs-lookup"><span data-stu-id="50d00-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="50d00-251">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="50d00-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="50d00-252">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-252">Format</span></span>

<span data-ttu-id="50d00-253">6 자리 숫자 앞에 오는 두 문자</span><span class="sxs-lookup"><span data-stu-id="50d00-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-254">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-254">Pattern</span></span>

<span data-ttu-id="50d00-255">8 대 문자와 숫자:</span><span class="sxs-lookup"><span data-stu-id="50d00-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="50d00-256">두 문자 (대 소문자 구분 안함)</span><span class="sxs-lookup"><span data-stu-id="50d00-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="50d00-257">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="50d00-257">A space (optional)</span></span>
    
- <span data-ttu-id="50d00-258">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="50d00-259">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-259">Checksum</span></span>

<span data-ttu-id="50d00-260">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-261">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-261">Definition</span></span>

<span data-ttu-id="50d00-262">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-263">정규식 `Regex_czech_republic_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-264">키워드에서 `Keywords_czech_republic_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="50d00-265">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-265">Keywords</span></span>

<span data-ttu-id="50d00-266">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-266"></span></span>
|<span data-ttu-id="50d00-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-268">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-268">dl#</span></span>  <br/> <span data-ttu-id="50d00-269">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-269">driver license</span></span>  <br/> <span data-ttu-id="50d00-270">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-270">driver license number</span></span>  <br/> <span data-ttu-id="50d00-271">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-271">driver licence</span></span>  <br/> <span data-ttu-id="50d00-272">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-272">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-273">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-273">drivers license</span></span>  <br/> <span data-ttu-id="50d00-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-274">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-275">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-275">driver's license</span></span>  <br/> <span data-ttu-id="50d00-276">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-276">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-277">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-277">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-278">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-278">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-279">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-279">driving license number</span></span>  <br/> <span data-ttu-id="50d00-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-280">dlno#</span></span>  <br/> <span data-ttu-id="50d00-281">Řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="50d00-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="50d00-282">덴마크</span><span class="sxs-lookup"><span data-stu-id="50d00-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="50d00-283">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-283">Format</span></span>

<span data-ttu-id="50d00-284">공백 및 구분 기호 없이 8 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-285">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-285">Pattern</span></span>

<span data-ttu-id="50d00-286">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="50d00-287">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-287">Checksum</span></span>

<span data-ttu-id="50d00-288">예</span><span class="sxs-lookup"><span data-stu-id="50d00-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-289">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-289">Definition</span></span>

<span data-ttu-id="50d00-290">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-291">정규식 `Regex_denmark_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-292">키워드에서 `Keywords_denmark_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="50d00-293">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-293">Keywords</span></span>

<span data-ttu-id="50d00-294">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-294"></span></span>
|<span data-ttu-id="50d00-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-296">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-296">dl#</span></span>  <br/> <span data-ttu-id="50d00-297">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-297">driver license</span></span>  <br/> <span data-ttu-id="50d00-298">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-298">driver license number</span></span>  <br/> <span data-ttu-id="50d00-299">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-299">driver licence</span></span>  <br/> <span data-ttu-id="50d00-300">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-300">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-301">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-301">drivers license</span></span>  <br/> <span data-ttu-id="50d00-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-302">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-303">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-303">driver's license</span></span>  <br/> <span data-ttu-id="50d00-304">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-304">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-305">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-305">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-306">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-306">driving license number</span></span>  <br/> <span data-ttu-id="50d00-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-307">dlno#</span></span>  <br/> <span data-ttu-id="50d00-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="50d00-308">kørekort</span></span>  <br/> <span data-ttu-id="50d00-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="50d00-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="50d00-310">에스토니아</span><span class="sxs-lookup"><span data-stu-id="50d00-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="50d00-311">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-311">Format</span></span>

<span data-ttu-id="50d00-312">6 자리 숫자 앞에 오는 두 문자</span><span class="sxs-lookup"><span data-stu-id="50d00-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-313">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-313">Pattern</span></span>

<span data-ttu-id="50d00-314">두 대 문자와 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="50d00-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="50d00-315">문자 "ET" (대 소문자 구분 안함)</span><span class="sxs-lookup"><span data-stu-id="50d00-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="50d00-316">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="50d00-317">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-317">Checksum</span></span>

<span data-ttu-id="50d00-318">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-319">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-319">Definition</span></span>

<span data-ttu-id="50d00-320">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-321">정규식 `Regex_estonia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-322">키워드에서 `Keywords_estonia_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-323">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-323">Keywords</span></span>

<span data-ttu-id="50d00-324">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-324"></span></span>
|<span data-ttu-id="50d00-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-326">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-326">dl#</span></span>  <br/> <span data-ttu-id="50d00-327">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-327">driver license</span></span>  <br/> <span data-ttu-id="50d00-328">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-328">driver license number</span></span>  <br/> <span data-ttu-id="50d00-329">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-329">driver license number</span></span>  <br/> <span data-ttu-id="50d00-330">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-330">driver licence</span></span>  <br/> <span data-ttu-id="50d00-331">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-331">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-332">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-332">drivers license</span></span>  <br/> <span data-ttu-id="50d00-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-333">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-334">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-334">driver's license</span></span>  <br/> <span data-ttu-id="50d00-335">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-335">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-336">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-336">driving license number</span></span>  <br/> <span data-ttu-id="50d00-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-337">dlno#</span></span>  <br/> <span data-ttu-id="50d00-338">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="50d00-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="50d00-339">핀란드</span><span class="sxs-lookup"><span data-stu-id="50d00-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="50d00-340">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-340">Format</span></span>

<span data-ttu-id="50d00-341">하이픈을 포함하는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-342">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-342">Pattern</span></span>

<span data-ttu-id="50d00-343">하이픈을 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="50d00-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="50d00-344">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-344">Six digits</span></span> 
    
- <span data-ttu-id="50d00-345">하이픈</span><span class="sxs-lookup"><span data-stu-id="50d00-345">A hyphen</span></span>
    
-  <span data-ttu-id="50d00-346">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="50d00-347">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-347">Checksum</span></span>

<span data-ttu-id="50d00-348">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-349">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-349">Definition</span></span>

<span data-ttu-id="50d00-350">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-351">정규식 `Regex_finland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-352">키워드에서 `Keywords_finland_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-353">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-353">Keywords</span></span>

<span data-ttu-id="50d00-354">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-354"></span></span>
|<span data-ttu-id="50d00-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-356">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-356">dl#</span></span>  <br/> <span data-ttu-id="50d00-357">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-357">driver license</span></span>  <br/> <span data-ttu-id="50d00-358">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-358">driver license number</span></span>  <br/> <span data-ttu-id="50d00-359">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-359">driver licence</span></span>  <br/> <span data-ttu-id="50d00-360">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-360">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-361">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-361">drivers license</span></span>  <br/> <span data-ttu-id="50d00-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-362">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-363">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-363">driver's license</span></span>  <br/> <span data-ttu-id="50d00-364">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-364">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-365">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-365">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-366">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-366">driving license number</span></span>  <br/> <span data-ttu-id="50d00-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-367">dlno#</span></span>  <br/> <span data-ttu-id="50d00-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="50d00-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="50d00-369">프랑스</span><span class="sxs-lookup"><span data-stu-id="50d00-369">France</span></span>

<span data-ttu-id="50d00-370">자세한 내용은의 섹션을 참조 "프랑스 운전 면허 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="50d00-371">독일</span><span class="sxs-lookup"><span data-stu-id="50d00-371">Germany</span></span>

<span data-ttu-id="50d00-372">자세한 내용은의 섹션을 참조 "독일 운전 면허 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="50d00-373">그리스</span><span class="sxs-lookup"><span data-stu-id="50d00-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="50d00-374">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-374">Format</span></span>

<span data-ttu-id="50d00-375">공백 및 구분 기호 없이 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="50d00-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-376">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-376">Pattern</span></span>

 <span data-ttu-id="50d00-377">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="50d00-378">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-378">Checksum</span></span>

<span data-ttu-id="50d00-379">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-380">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-380">Definition</span></span>

<span data-ttu-id="50d00-381">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-382">정규식 `Regex_greece_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-383">키워드에서 `Keywords_greece_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-384">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-384">Keywords</span></span>

<span data-ttu-id="50d00-385">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-385"></span></span>
|<span data-ttu-id="50d00-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-387">dlL #</span><span class="sxs-lookup"><span data-stu-id="50d00-387">dlL#</span></span>  <br/> <span data-ttu-id="50d00-388">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-388">driver license</span></span>  <br/> <span data-ttu-id="50d00-389">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-389">driver license number</span></span>  <br/> <span data-ttu-id="50d00-390">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-390">driver licence</span></span>  <br/> <span data-ttu-id="50d00-391">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-391">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-392">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-392">drivers license</span></span>  <br/> <span data-ttu-id="50d00-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-393">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-394">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-394">driver's license</span></span>  <br/> <span data-ttu-id="50d00-395">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-395">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-396">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-396">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-397">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-397">driving license number</span></span>  <br/> <span data-ttu-id="50d00-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-398">dlno#</span></span>  <br/> <span data-ttu-id="50d00-399">ΔΕΙΑ ΟΔΉΓΗΣΗΣ</span><span class="sxs-lookup"><span data-stu-id="50d00-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="50d00-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="50d00-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="50d00-401">헝가리</span><span class="sxs-lookup"><span data-stu-id="50d00-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="50d00-402">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-402">Format</span></span>

<span data-ttu-id="50d00-403">6 자리 숫자 앞에 오는 두 문자</span><span class="sxs-lookup"><span data-stu-id="50d00-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-404">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-404">Pattern</span></span>

<span data-ttu-id="50d00-405">두 대 문자와 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="50d00-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="50d00-406">두 문자 (대 소문자 구분 안함)</span><span class="sxs-lookup"><span data-stu-id="50d00-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="50d00-407">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="50d00-408">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-408">Checksum</span></span>

<span data-ttu-id="50d00-409">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-410">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-410">Definition</span></span>

<span data-ttu-id="50d00-411">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-412">정규식 `Regex_hungary_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-413">키워드에서 `Keywords_hungary_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-414">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-414">Keywords</span></span>

<span data-ttu-id="50d00-415">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-415"></span></span>
|<span data-ttu-id="50d00-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-417">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-417">dl#</span></span>  <br/> <span data-ttu-id="50d00-418">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-418">driver license</span></span>  <br/> <span data-ttu-id="50d00-419">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-419">driver license number</span></span>  <br/> <span data-ttu-id="50d00-420">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-420">driver licence</span></span>  <br/> <span data-ttu-id="50d00-421">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-421">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-422">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-422">drivers license</span></span>  <br/> <span data-ttu-id="50d00-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-423">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-424">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-424">driver's license</span></span>  <br/> <span data-ttu-id="50d00-425">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-425">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-426">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-426">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-427">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-427">driving license number</span></span>  <br/> <span data-ttu-id="50d00-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-428">dlno#</span></span>  <br/> <span data-ttu-id="50d00-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="50d00-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="50d00-430">Ireland</span><span class="sxs-lookup"><span data-stu-id="50d00-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="50d00-431">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-431">Format</span></span>

<span data-ttu-id="50d00-432">4 개의 문자 앞에 오는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-433">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-433">Pattern</span></span>

<span data-ttu-id="50d00-434">6 자리 숫자 및 4 개의 문자:</span><span class="sxs-lookup"><span data-stu-id="50d00-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="50d00-435">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-435">Six digits</span></span>
    
- <span data-ttu-id="50d00-436">4 개의 문자 (대 소문자 구분 안함)</span><span class="sxs-lookup"><span data-stu-id="50d00-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="50d00-437">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-437">Checksum</span></span>

<span data-ttu-id="50d00-438">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-439">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-439">Definition</span></span>

<span data-ttu-id="50d00-440">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-441">정규식 `Regex_ireland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-442">키워드에서 `Keywords_ireland_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-443">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-443">Keywords</span></span>

<span data-ttu-id="50d00-444">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-444"></span></span>
|<span data-ttu-id="50d00-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-446">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-446">dl#</span></span>  <br/> <span data-ttu-id="50d00-447">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-447">driver license</span></span>  <br/> <span data-ttu-id="50d00-448">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-448">driver license number</span></span>  <br/> <span data-ttu-id="50d00-449">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-449">driver licence</span></span>  <br/> <span data-ttu-id="50d00-450">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-450">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-451">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-451">drivers license</span></span>  <br/> <span data-ttu-id="50d00-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-452">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-453">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-453">driver's license</span></span>  <br/> <span data-ttu-id="50d00-454">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-454">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-455">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-455">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-456">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-456">driving license number</span></span>  <br/> <span data-ttu-id="50d00-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-457">dlno#</span></span>  <br/> <span data-ttu-id="50d00-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="50d00-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="50d00-459">이탈리아</span><span class="sxs-lookup"><span data-stu-id="50d00-459">Italy</span></span>

<span data-ttu-id="50d00-460">자세한 내용은의 섹션을 참조 "이탈리아 운전 면허 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="50d00-461">라트비아</span><span class="sxs-lookup"><span data-stu-id="50d00-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="50d00-462">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-462">Format</span></span>

<span data-ttu-id="50d00-463">6 자리 숫자 앞에 오는 세 개 문자</span><span class="sxs-lookup"><span data-stu-id="50d00-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-464">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-464">Pattern</span></span>

<span data-ttu-id="50d00-465">3 대 문자와 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="50d00-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="50d00-466">세 개 문자 (대 소문자 구분 안함)</span><span class="sxs-lookup"><span data-stu-id="50d00-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="50d00-467">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="50d00-468">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-468">Checksum</span></span>

<span data-ttu-id="50d00-469">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-470">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-470">Definition</span></span>

<span data-ttu-id="50d00-471">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-472">정규식 `Regex_latvia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-473">키워드에서 `Keywords_latvia_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-474">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-474">Keywords</span></span>

<span data-ttu-id="50d00-475">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-475"></span></span>
|<span data-ttu-id="50d00-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-477">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-477">dl#</span></span>  <br/> <span data-ttu-id="50d00-478">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-478">driver license</span></span>  <br/> <span data-ttu-id="50d00-479">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-479">driver license number</span></span>  <br/> <span data-ttu-id="50d00-480">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-480">driver licence</span></span>  <br/> <span data-ttu-id="50d00-481">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-481">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-482">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-482">drivers license</span></span>  <br/> <span data-ttu-id="50d00-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-483">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-484">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-484">driver's license</span></span>  <br/> <span data-ttu-id="50d00-485">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-485">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-486">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-486">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-487">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-487">driving license number</span></span>  <br/> <span data-ttu-id="50d00-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-488">dlno#</span></span>  <br/> <span data-ttu-id="50d00-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="50d00-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="50d00-490">리투아니아</span><span class="sxs-lookup"><span data-stu-id="50d00-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="50d00-491">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-491">Format</span></span>

<span data-ttu-id="50d00-492">공백 및 구분 기호 없이 8 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-493">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-493">Pattern</span></span>

 <span data-ttu-id="50d00-494">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="50d00-495">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-495">Checksum</span></span>

<span data-ttu-id="50d00-496">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-497">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-497">Definition</span></span>

<span data-ttu-id="50d00-498">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-499">정규식 `Regex_lithuania_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-500">키워드에서 `Keywords_lithuania_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-501">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-501">Keywords</span></span>

<span data-ttu-id="50d00-502">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-502"></span></span>
|<span data-ttu-id="50d00-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-504">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-504">dl#</span></span>  <br/> <span data-ttu-id="50d00-505">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-505">driver license</span></span>  <br/> <span data-ttu-id="50d00-506">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-506">driver license number</span></span>  <br/> <span data-ttu-id="50d00-507">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-507">driver licence</span></span>  <br/> <span data-ttu-id="50d00-508">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-508">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-509">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-509">drivers license</span></span>  <br/> <span data-ttu-id="50d00-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-510">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-511">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-511">driver's license</span></span>  <br/> <span data-ttu-id="50d00-512">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-512">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-513">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-513">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-514">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-514">driving license number</span></span>  <br/> <span data-ttu-id="50d00-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-515">dlno#</span></span>  <br/> <span data-ttu-id="50d00-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="50d00-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="50d00-517">룩셈부르크</span><span class="sxs-lookup"><span data-stu-id="50d00-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="50d00-518">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-518">Format</span></span>

<span data-ttu-id="50d00-519">공백 및 구분 기호 없이 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-520">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-520">Pattern</span></span>

 <span data-ttu-id="50d00-521">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="50d00-522">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-522">Checksum</span></span>

<span data-ttu-id="50d00-523">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-524">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-524">Definition</span></span>

<span data-ttu-id="50d00-525">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-526">정규식 `Regex_luxemburg_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-527">키워드에서 `Keywords_luxemburg_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-528">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-528">Keywords</span></span>

<span data-ttu-id="50d00-529">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-529"></span></span>
|<span data-ttu-id="50d00-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-531">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-531">dl#</span></span>  <br/> <span data-ttu-id="50d00-532">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-532">driver license</span></span>  <br/> <span data-ttu-id="50d00-533">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-533">driver license number</span></span>  <br/> <span data-ttu-id="50d00-534">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-534">driver licence</span></span>  <br/> <span data-ttu-id="50d00-535">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-535">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-536">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-536">drivers license</span></span>  <br/> <span data-ttu-id="50d00-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-537">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-538">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-538">driver's license</span></span>  <br/> <span data-ttu-id="50d00-539">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-539">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-540">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-540">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-541">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-541">driving license number</span></span>  <br/> <span data-ttu-id="50d00-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-542">dlno#</span></span>  <br/> <span data-ttu-id="50d00-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="50d00-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="50d00-544">몰타</span><span class="sxs-lookup"><span data-stu-id="50d00-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="50d00-545">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-545">Format</span></span>

<span data-ttu-id="50d00-546">두 문자 및 지정된 된 패턴에 6 자리 숫자의 조합</span><span class="sxs-lookup"><span data-stu-id="50d00-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-547">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-547">Pattern</span></span>

<span data-ttu-id="50d00-548">두 문자와 6 자리 숫자의 조합 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="50d00-549">두 문자 (숫자 또는 문자, 대 소문자 구분 안함)</span><span class="sxs-lookup"><span data-stu-id="50d00-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="50d00-550">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="50d00-550">A space (optional)</span></span>
    
- <span data-ttu-id="50d00-551">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-551">Three digits</span></span>
    
- <span data-ttu-id="50d00-552">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="50d00-552">A space (optional)</span></span>
    
- <span data-ttu-id="50d00-553">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="50d00-554">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-554">Checksum</span></span>

<span data-ttu-id="50d00-555">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-556">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-556">Definition</span></span>

<span data-ttu-id="50d00-557">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-558">정규식 `Regex_malta_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-559">키워드에서 `Keywords_malta_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-560">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-560">Keywords</span></span>

<span data-ttu-id="50d00-561">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-561"></span></span>
|<span data-ttu-id="50d00-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-563">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-563">dl#</span></span>  <br/> <span data-ttu-id="50d00-564">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-564">driver license</span></span>  <br/> <span data-ttu-id="50d00-565">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-565">driver license number</span></span>  <br/> <span data-ttu-id="50d00-566">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-566">driver licence</span></span>  <br/> <span data-ttu-id="50d00-567">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-567">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-568">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-568">drivers license</span></span>  <br/> <span data-ttu-id="50d00-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-569">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-570">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-570">driver's license</span></span>  <br/> <span data-ttu-id="50d00-571">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-571">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-572">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-572">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-573">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-573">driving license number</span></span>  <br/> <span data-ttu-id="50d00-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-574">dlno#</span></span>  <br/> <span data-ttu-id="50d00-575">liċenzja 게 sewqan</span><span class="sxs-lookup"><span data-stu-id="50d00-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="50d00-576">네덜란드</span><span class="sxs-lookup"><span data-stu-id="50d00-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="50d00-577">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-577">Format</span></span>

<span data-ttu-id="50d00-578">공백 및 구분 기호 없이 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-579">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-579">Pattern</span></span>

<span data-ttu-id="50d00-580">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="50d00-581">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-581">Checksum</span></span>

<span data-ttu-id="50d00-582">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-583">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-583">Definition</span></span>

<span data-ttu-id="50d00-584">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-585">정규식 `Regex_netherlands_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-586">키워드에서 `Keywords_netherlands_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-587">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-587">Keywords</span></span>

<span data-ttu-id="50d00-588">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-588"></span></span>
|<span data-ttu-id="50d00-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-590">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-590">dl#</span></span>  <br/> <span data-ttu-id="50d00-591">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-591">driver license</span></span>  <br/> <span data-ttu-id="50d00-592">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-592">driver license number</span></span>  <br/> <span data-ttu-id="50d00-593">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-593">driver licence</span></span>  <br/> <span data-ttu-id="50d00-594">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-594">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-595">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-595">drivers license</span></span>  <br/> <span data-ttu-id="50d00-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-596">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-597">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-597">driver's license</span></span>  <br/> <span data-ttu-id="50d00-598">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-598">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-599">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-599">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-600">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-600">driving license number</span></span>  <br/> <span data-ttu-id="50d00-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-601">dlno#</span></span>  <br/> <span data-ttu-id="50d00-602">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="50d00-602">permis de conduire</span></span>  <br/> <span data-ttu-id="50d00-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="50d00-603">rijbewijs</span></span>  <br/> <span data-ttu-id="50d00-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="50d00-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="50d00-605">폴란드</span><span class="sxs-lookup"><span data-stu-id="50d00-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="50d00-606">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-606">Format</span></span>

<span data-ttu-id="50d00-607">2 슬래시를 포함 하는 14 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-608">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-608">Pattern</span></span>

<span data-ttu-id="50d00-609">14 숫자 및 2 슬래시:</span><span class="sxs-lookup"><span data-stu-id="50d00-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="50d00-610">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-610">Five digits</span></span> 
    
- <span data-ttu-id="50d00-611">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="50d00-611">A forward slash</span></span>
    
- <span data-ttu-id="50d00-612">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-612">Two digits</span></span>
    
- <span data-ttu-id="50d00-613">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="50d00-613">A forward slash</span></span>
    
- <span data-ttu-id="50d00-614">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="50d00-615">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-615">Checksum</span></span>

<span data-ttu-id="50d00-616">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-617">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-617">Definition</span></span>

<span data-ttu-id="50d00-618">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-619">정규식 `Regex_poland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-620">키워드에서 `Keywords_poland_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-621">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-621">Keywords</span></span>

<span data-ttu-id="50d00-622">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-622"></span></span>
|<span data-ttu-id="50d00-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-624">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-624">dl#</span></span>  <br/> <span data-ttu-id="50d00-625">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-625">driver license</span></span>  <br/> <span data-ttu-id="50d00-626">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-626">driver license number</span></span>  <br/> <span data-ttu-id="50d00-627">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-627">driver licence</span></span>  <br/> <span data-ttu-id="50d00-628">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-628">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-629">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-629">drivers license</span></span>  <br/> <span data-ttu-id="50d00-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-630">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-631">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-631">driver's license</span></span>  <br/> <span data-ttu-id="50d00-632">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-632">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-633">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-633">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-634">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-634">driving license number</span></span>  <br/> <span data-ttu-id="50d00-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-635">dlno#</span></span>  <br/> <span data-ttu-id="50d00-636">prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="50d00-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="50d00-637">포르투갈</span><span class="sxs-lookup"><span data-stu-id="50d00-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="50d00-638">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-638">Format</span></span>

<span data-ttu-id="50d00-639">지정된 된 패턴에 일곱 개의 숫자 앞에 오는 두 문자</span><span class="sxs-lookup"><span data-stu-id="50d00-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-640">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-640">Pattern</span></span>

<span data-ttu-id="50d00-641">특수 문자가 포함 된 7 번호 앞에 오는 두 문자 수:</span><span class="sxs-lookup"><span data-stu-id="50d00-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="50d00-642">두 문자 (대 소문자 구분 안함)</span><span class="sxs-lookup"><span data-stu-id="50d00-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="50d00-643">하이픈</span><span class="sxs-lookup"><span data-stu-id="50d00-643">A hyphen</span></span>
    
- <span data-ttu-id="50d00-644">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-644">Six digits</span></span>
    
- <span data-ttu-id="50d00-645">공백</span><span class="sxs-lookup"><span data-stu-id="50d00-645">A space</span></span>
    
- <span data-ttu-id="50d00-646">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="50d00-647">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-647">Checksum</span></span>

<span data-ttu-id="50d00-648">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-649">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-649">Definition</span></span>

<span data-ttu-id="50d00-650">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-651">정규식 `Regex_portugal_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-652">키워드에서 `Keywords_portugal_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-653">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-653">Keywords</span></span>

<span data-ttu-id="50d00-654">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-654"></span></span>
|<span data-ttu-id="50d00-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-656">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-656">dl#</span></span>  <br/> <span data-ttu-id="50d00-657">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-657">driver license</span></span>  <br/> <span data-ttu-id="50d00-658">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-658">driver license number</span></span>  <br/> <span data-ttu-id="50d00-659">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-659">driver licence</span></span>  <br/> <span data-ttu-id="50d00-660">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-660">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-661">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-661">drivers license</span></span>  <br/> <span data-ttu-id="50d00-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-662">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-663">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-663">driver's license</span></span>  <br/> <span data-ttu-id="50d00-664">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-664">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-665">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-665">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-666">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-666">driving license number</span></span>  <br/> <span data-ttu-id="50d00-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-667">dlno#</span></span>  <br/> <span data-ttu-id="50d00-668">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="50d00-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="50d00-669">루마니아</span><span class="sxs-lookup"><span data-stu-id="50d00-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="50d00-670">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-670">Format</span></span>

<span data-ttu-id="50d00-671">8 개의 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="50d00-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-672">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-672">Pattern</span></span>

<span data-ttu-id="50d00-673">8 개의 숫자 앞에 오는 문자 하나:</span><span class="sxs-lookup"><span data-stu-id="50d00-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="50d00-674">하나의 문자 (대 소문자 구분 안함) 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="50d00-675">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="50d00-676">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-676">Checksum</span></span>

<span data-ttu-id="50d00-677">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-678">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-678">Definition</span></span>

<span data-ttu-id="50d00-679">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-680">정규식 `Regex_romania_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-681">키워드에서 `Keywords_romania_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-682">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-682">Keywords</span></span>

<span data-ttu-id="50d00-683">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-683"></span></span>
|<span data-ttu-id="50d00-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-685">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-685">dl#</span></span>  <br/> <span data-ttu-id="50d00-686">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-686">driver license</span></span>  <br/> <span data-ttu-id="50d00-687">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-687">driver license number</span></span>  <br/> <span data-ttu-id="50d00-688">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-688">driver licence</span></span>  <br/> <span data-ttu-id="50d00-689">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-689">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-690">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-690">drivers license</span></span>  <br/> <span data-ttu-id="50d00-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-691">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-692">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-692">driver's license</span></span>  <br/> <span data-ttu-id="50d00-693">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-693">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-694">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-694">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-695">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-695">driving license number</span></span>  <br/> <span data-ttu-id="50d00-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-696">dlno#</span></span>  <br/> <span data-ttu-id="50d00-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="50d00-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="50d00-698">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="50d00-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="50d00-699">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-699">Format</span></span>

<span data-ttu-id="50d00-700">7 자리 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="50d00-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-701">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-701">Pattern</span></span>

<span data-ttu-id="50d00-702">7 자리 숫자 앞에 오는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="50d00-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="50d00-703">하나의 문자 (대 소문자 구분 안함) 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="50d00-704">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="50d00-705">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-705">Checksum</span></span>

<span data-ttu-id="50d00-706">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-707">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-707">Definition</span></span>

<span data-ttu-id="50d00-708">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-709">정규식 `Regex_slovakia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-710">키워드에서 `Keywords_slovakia_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-711">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-711">Keywords</span></span>

<span data-ttu-id="50d00-712">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-712"></span></span>
|<span data-ttu-id="50d00-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-714">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-714">dl#</span></span>  <br/> <span data-ttu-id="50d00-715">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-715">driver license</span></span>  <br/> <span data-ttu-id="50d00-716">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-716">driver license number</span></span>  <br/> <span data-ttu-id="50d00-717">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-717">driver licence</span></span>  <br/> <span data-ttu-id="50d00-718">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-718">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-719">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-719">drivers license</span></span>  <br/> <span data-ttu-id="50d00-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-720">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-721">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-721">driver's license</span></span>  <br/> <span data-ttu-id="50d00-722">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-722">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-723">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-723">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-724">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-724">driving license number</span></span>  <br/> <span data-ttu-id="50d00-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-725">dlno#</span></span>  <br/> <span data-ttu-id="50d00-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="50d00-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="50d00-727">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="50d00-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="50d00-728">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-728">Format</span></span>

<span data-ttu-id="50d00-729">공백 및 구분 기호 없이 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="50d00-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-730">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-730">Pattern</span></span>

<span data-ttu-id="50d00-731">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="50d00-732">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-732">Checksum</span></span>

<span data-ttu-id="50d00-733">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-734">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-734">Definition</span></span>

<span data-ttu-id="50d00-735">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-736">정규식 `Regex_slovenia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-737">키워드에서 `Keywords_slovenia_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-738">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-738">Keywords</span></span>

<span data-ttu-id="50d00-739">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-739"></span></span>
|<span data-ttu-id="50d00-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-741">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-741">dl#</span></span>  <br/> <span data-ttu-id="50d00-742">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-742">driver license</span></span>  <br/> <span data-ttu-id="50d00-743">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-743">driver license number</span></span>  <br/> <span data-ttu-id="50d00-744">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-744">driver licence</span></span>  <br/> <span data-ttu-id="50d00-745">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-745">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-746">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-746">drivers license</span></span>  <br/> <span data-ttu-id="50d00-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-747">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-748">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-748">driver's license</span></span>  <br/> <span data-ttu-id="50d00-749">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-749">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-750">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-750">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-751">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-751">driving license number</span></span>  <br/> <span data-ttu-id="50d00-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-752">dlno#</span></span>  <br/> <span data-ttu-id="50d00-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="50d00-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="50d00-754">스페인</span><span class="sxs-lookup"><span data-stu-id="50d00-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="50d00-755">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-755">Format</span></span>

<span data-ttu-id="50d00-756">한 문자 앞에 오는 8 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-757">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-757">Pattern</span></span>

<span data-ttu-id="50d00-758">8 개의 숫자를 한 글자 앞에 오는:</span><span class="sxs-lookup"><span data-stu-id="50d00-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="50d00-759">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-759">Eight digits</span></span> 
    
- <span data-ttu-id="50d00-760">한 자리 숫자 또는 문자 (대 소문자 구분 안함)</span><span class="sxs-lookup"><span data-stu-id="50d00-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="50d00-761">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-761">Checksum</span></span>

<span data-ttu-id="50d00-762">예</span><span class="sxs-lookup"><span data-stu-id="50d00-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-763">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-763">Definition</span></span>

<span data-ttu-id="50d00-764">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-765">다음은 함수 `Func_spain_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-766">키워드에서 `Keywords_spain_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="50d00-767">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-767">Keywords</span></span>

<span data-ttu-id="50d00-768">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-768"></span></span>
|<span data-ttu-id="50d00-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-770">dlno#</span></span>  <br/> <span data-ttu-id="50d00-771">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-771">dl#</span></span>  <br/> <span data-ttu-id="50d00-772">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-772">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-773">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-773">driver licence</span></span>  <br/> <span data-ttu-id="50d00-774">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-774">driver license</span></span>  <br/> <span data-ttu-id="50d00-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-775">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-776">
drivers license</span><span class="sxs-lookup"><span data-stu-id="50d00-776">drivers license</span></span>  <br/> <span data-ttu-id="50d00-777">드라이버의 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-777">driver's licence</span></span>  <br/> <span data-ttu-id="50d00-778">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-778">driver's license</span></span>  <br/> <span data-ttu-id="50d00-779">driving licence
</span><span class="sxs-lookup"><span data-stu-id="50d00-779">driving licence</span></span>  <br/> <span data-ttu-id="50d00-780">라이선스를 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-780">driving license</span></span>  <br/> <span data-ttu-id="50d00-781">드라이버 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-781">driver licence number</span></span>  <br/> <span data-ttu-id="50d00-782">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-782">driver license number</span></span>  <br/> <span data-ttu-id="50d00-783">드라이버는 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-783">drivers licence number</span></span>  <br/> <span data-ttu-id="50d00-784">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-784">drivers license number</span></span>  <br/> <span data-ttu-id="50d00-785">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-785">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-786">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-786">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-787">driving 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-787">driving licence number</span></span>  <br/> <span data-ttu-id="50d00-788">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-788">driving license number</span></span>  <br/> <span data-ttu-id="50d00-789">허용 제어</span><span class="sxs-lookup"><span data-stu-id="50d00-789">driving permit</span></span>  <br/> <span data-ttu-id="50d00-790">허용 수를 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-790">driving permit number</span></span>  <br/> <span data-ttu-id="50d00-791">permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="50d00-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="50d00-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="50d00-792">permiso conducción</span></span>  <br/> <span data-ttu-id="50d00-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="50d00-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="50d00-794">número de carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="50d00-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="50d00-795">número carnet conducir</span><span class="sxs-lookup"><span data-stu-id="50d00-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="50d00-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="50d00-796">licencia conducir</span></span>  <br/> <span data-ttu-id="50d00-797">número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="50d00-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="50d00-798">número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="50d00-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="50d00-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="50d00-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="50d00-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="50d00-800">permiso conducir</span></span>  <br/> <span data-ttu-id="50d00-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="50d00-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="50d00-802">el carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="50d00-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="50d00-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="50d00-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="50d00-804">스웨덴</span><span class="sxs-lookup"><span data-stu-id="50d00-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="50d00-805">형식</span><span class="sxs-lookup"><span data-stu-id="50d00-805">Format</span></span>

<span data-ttu-id="50d00-806">하이픈을 포함 하는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="50d00-807">패턴</span><span class="sxs-lookup"><span data-stu-id="50d00-807">Pattern</span></span>

<span data-ttu-id="50d00-808">하이픈을 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="50d00-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="50d00-809">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-809">Six digits</span></span> 
    
- <span data-ttu-id="50d00-810">하이픈</span><span class="sxs-lookup"><span data-stu-id="50d00-810">A hyphen</span></span>
    
- <span data-ttu-id="50d00-811">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="50d00-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="50d00-812">체크섬</span><span class="sxs-lookup"><span data-stu-id="50d00-812">Checksum</span></span>

<span data-ttu-id="50d00-813">없음</span><span class="sxs-lookup"><span data-stu-id="50d00-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="50d00-814">정의</span><span class="sxs-lookup"><span data-stu-id="50d00-814">Definition</span></span>

<span data-ttu-id="50d00-815">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="50d00-816">정규식 `Regex_sweden_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="50d00-817">키워드에서 `Keywords_sweden_eu_driver's_license_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="50d00-818">키워드</span><span class="sxs-lookup"><span data-stu-id="50d00-818">Keywords</span></span>

<span data-ttu-id="50d00-819">| |</span><span class="sxs-lookup"><span data-stu-id="50d00-819"></span></span>
|<span data-ttu-id="50d00-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="50d00-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="50d00-821">dl #</span><span class="sxs-lookup"><span data-stu-id="50d00-821">dl#</span></span>  <br/> <span data-ttu-id="50d00-822">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-822">driver license</span></span>  <br/> <span data-ttu-id="50d00-823">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-823">driver license number</span></span>  <br/> <span data-ttu-id="50d00-824">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="50d00-824">driver licence</span></span>  <br/> <span data-ttu-id="50d00-825">드라이버 lic 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-825">drivers lic.</span></span>  <br/> <span data-ttu-id="50d00-826">운전 면허</span><span class="sxs-lookup"><span data-stu-id="50d00-826">drivers license</span></span>  <br/> <span data-ttu-id="50d00-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="50d00-827">drivers licence</span></span>  <br/> <span data-ttu-id="50d00-828">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="50d00-828">driver's license</span></span>  <br/> <span data-ttu-id="50d00-829">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-829">driver's license number</span></span>  <br/> <span data-ttu-id="50d00-830">드라이버의 사용권 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-830">driver's licence number</span></span>  <br/> <span data-ttu-id="50d00-831">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="50d00-831">driving license number</span></span>  <br/> <span data-ttu-id="50d00-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="50d00-832">dlno#</span></span>  <br/> <span data-ttu-id="50d00-833">körkort</span><span class="sxs-lookup"><span data-stu-id="50d00-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="50d00-834">영국</span><span class="sxs-lookup"><span data-stu-id="50d00-834">UK</span></span>

<span data-ttu-id="50d00-p103">자세한 내용은의 섹션을 참조 "영국 운전 면허 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="50d00-p103">For details, see the section "U.K. Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="50d00-837">참고 항목</span><span class="sxs-lookup"><span data-stu-id="50d00-837">See also</span></span>

[<span data-ttu-id="50d00-838">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="50d00-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

