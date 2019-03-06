---
title: EU 운전 면허 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: 이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 드라이버의 라이선스 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: be9497c325866a670dff8d82b5170f4ca947c4ad
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410753"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="02d03-104">EU 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-104">EU Driver's License Number</span></span>

<span data-ttu-id="02d03-105">이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 드라이버의 라이선스 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="02d03-106">이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="02d03-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="02d03-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="02d03-108">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-108">Format</span></span>

<span data-ttu-id="02d03-109">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-110">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-110">Pattern</span></span>

<span data-ttu-id="02d03-111">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="02d03-112">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-112">Checksum</span></span>

<span data-ttu-id="02d03-113">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-114">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-114">Definition</span></span>

<span data-ttu-id="02d03-115">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-116">정규식이 해당 `Regex_austria_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-117">from `Keywords_austria_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="02d03-118">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-118">Keywords</span></span>

<span data-ttu-id="02d03-119">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-119"></span></span>
|<span data-ttu-id="02d03-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-121">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-121">dl#</span></span>  <br/> <span data-ttu-id="02d03-122">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-122">driver license</span></span>  <br/> <span data-ttu-id="02d03-123">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-123">driver license number</span></span>  <br/> <span data-ttu-id="02d03-124">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-124">driver licence</span></span>  <br/> <span data-ttu-id="02d03-125">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-125">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-126">drivers license</span></span>  <br/> <span data-ttu-id="02d03-127">driver's licence</span><span class="sxs-lookup"><span data-stu-id="02d03-127">driver's licence</span></span>  <br/> <span data-ttu-id="02d03-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-128">driver's license</span></span>  <br/> <span data-ttu-id="02d03-129">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-129">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-130">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="02d03-131">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-131">driving license number</span></span>  <br/> <span data-ttu-id="02d03-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-132">dlno#</span></span>  <br/> <span data-ttu-id="02d03-133">fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="02d03-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="02d03-134">fuhrerschein republik osterreich</span><span class="sxs-lookup"><span data-stu-id="02d03-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="02d03-135">벨기에</span><span class="sxs-lookup"><span data-stu-id="02d03-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="02d03-136">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-136">Format</span></span>

<span data-ttu-id="02d03-137">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-138">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-138">Pattern</span></span>

<span data-ttu-id="02d03-139">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="02d03-140">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-140">Checksum</span></span>

<span data-ttu-id="02d03-141">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-142">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-142">Definition</span></span>

<span data-ttu-id="02d03-143">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-144">정규식이 해당 `Regex_belgium_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-145">from `Keywords_belgium_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="02d03-146">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-146">Keywords</span></span>

<span data-ttu-id="02d03-147">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-147"></span></span>
|<span data-ttu-id="02d03-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-149">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-149">dl#</span></span>  <br/> <span data-ttu-id="02d03-150">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-150">driver license</span></span>  <br/> <span data-ttu-id="02d03-151">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-151">driver license number</span></span>  <br/> <span data-ttu-id="02d03-152">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-152">driver licence</span></span>  <br/> <span data-ttu-id="02d03-153">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-153">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-154">drivers license</span></span>  <br/> <span data-ttu-id="02d03-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-155">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-156">driver's license</span></span>  <br/> <span data-ttu-id="02d03-157">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-157">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-158">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-158">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-159">dlno#</span></span>  <br/> <span data-ttu-id="02d03-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="02d03-160">rijbewijs</span></span>  <br/> <span data-ttu-id="02d03-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="02d03-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="02d03-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="02d03-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="02d03-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="02d03-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="02d03-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="02d03-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="02d03-165">führerschein-veiligheid</span><span class="sxs-lookup"><span data-stu-id="02d03-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="02d03-166">fuehrerschein-veiligheid</span><span class="sxs-lookup"><span data-stu-id="02d03-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="02d03-167">fuehrerschein-veiligheid</span><span class="sxs-lookup"><span data-stu-id="02d03-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="02d03-168">불가리아</span><span class="sxs-lookup"><span data-stu-id="02d03-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="02d03-169">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-169">Format</span></span>

<span data-ttu-id="02d03-170">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-171">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-171">Pattern</span></span>

<span data-ttu-id="02d03-172">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="02d03-173">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-173">Checksum</span></span>

<span data-ttu-id="02d03-174">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-175">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-175">Definition</span></span>

<span data-ttu-id="02d03-176">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-177">정규식이 해당 `Regex_bulgaria_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-178">from `Keywords_bulgaria_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="02d03-179">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-179">Keywords</span></span>

<span data-ttu-id="02d03-180">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-180"></span></span>
|<span data-ttu-id="02d03-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-182">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-182">dl#</span></span>  <br/> <span data-ttu-id="02d03-183">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-183">driver license</span></span>  <br/> <span data-ttu-id="02d03-184">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-184">driver license number</span></span>  <br/> <span data-ttu-id="02d03-185">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-185">driver licence</span></span>  <br/> <span data-ttu-id="02d03-186">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-186">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-187">drivers license</span></span>  <br/> <span data-ttu-id="02d03-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-188">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-189">driver's license</span></span>  <br/> <span data-ttu-id="02d03-190">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-190">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-191">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-191">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-192">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-192">driving license number</span></span>  <br/> <span data-ttu-id="02d03-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-193">dlno#</span></span>  <br/> <span data-ttu-id="02d03-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="02d03-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="02d03-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="02d03-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="02d03-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="02d03-196">сумпс</span></span>  <br/> <span data-ttu-id="02d03-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="02d03-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="02d03-198">크로아티아</span><span class="sxs-lookup"><span data-stu-id="02d03-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="02d03-199">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-199">Format</span></span>

<span data-ttu-id="02d03-200">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-201">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-201">Pattern</span></span>

<span data-ttu-id="02d03-202">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="02d03-203">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-203">Checksum</span></span>

<span data-ttu-id="02d03-204">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-205">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-205">Definition</span></span>

<span data-ttu-id="02d03-206">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-207">정규식이 해당 `Regex_croatia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-208">from `Keywords_croatia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="02d03-209">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-209">Keywords</span></span>

<span data-ttu-id="02d03-210">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-210"></span></span>
|<span data-ttu-id="02d03-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-212">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-212">dl#</span></span>  <br/> <span data-ttu-id="02d03-213">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-213">driver license</span></span>  <br/> <span data-ttu-id="02d03-214">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-214">driver license number</span></span>  <br/> <span data-ttu-id="02d03-215">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-215">driver licence</span></span>  <br/> <span data-ttu-id="02d03-216">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-216">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-217">drivers license</span></span>  <br/> <span data-ttu-id="02d03-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-218">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-219">driver's license</span></span>  <br/> <span data-ttu-id="02d03-220">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-220">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-221">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-221">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-222">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-222">driving license number</span></span>  <br/> <span data-ttu-id="02d03-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-223">dlno#</span></span>  <br/> <span data-ttu-id="02d03-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="02d03-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="02d03-225">키프로스</span><span class="sxs-lookup"><span data-stu-id="02d03-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="02d03-226">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-226">Format</span></span>

<span data-ttu-id="02d03-227">공백과 구분 기호를 사용 하지 않고 12 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-228">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-228">Pattern</span></span>

<span data-ttu-id="02d03-229">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="02d03-230">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-230">Checksum</span></span>

<span data-ttu-id="02d03-231">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-232">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-232">Definition</span></span>

<span data-ttu-id="02d03-233">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-234">정규식이 해당 `Regex_cyprus_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-235">from `Keywords_cyprus_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-236">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-236">Keywords</span></span>

<span data-ttu-id="02d03-237">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-237"></span></span>
|<span data-ttu-id="02d03-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-239">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-239">dl#</span></span>  <br/> <span data-ttu-id="02d03-240">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-240">driver license</span></span>  <br/> <span data-ttu-id="02d03-241">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-241">driver license number</span></span>  <br/> <span data-ttu-id="02d03-242">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-242">driver licence</span></span>  <br/> <span data-ttu-id="02d03-243">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-243">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-244">drivers license</span></span>  <br/> <span data-ttu-id="02d03-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-245">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-246">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-246">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-247">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-247">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-248">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-248">driving license number</span></span>  <br/> <span data-ttu-id="02d03-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-249">dlno#</span></span>  <br/> <span data-ttu-id="02d03-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="02d03-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="02d03-251">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="02d03-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="02d03-252">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-252">Format</span></span>

<span data-ttu-id="02d03-253">2 개의 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-254">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-254">Pattern</span></span>

<span data-ttu-id="02d03-255">8 개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="02d03-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="02d03-256">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="02d03-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="02d03-257">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="02d03-257">A space (optional)</span></span>
    
- <span data-ttu-id="02d03-258">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="02d03-259">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-259">Checksum</span></span>

<span data-ttu-id="02d03-260">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-261">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-261">Definition</span></span>

<span data-ttu-id="02d03-262">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-263">정규식이 해당 `Regex_czech_republic_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-264">from `Keywords_czech_republic_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="02d03-265">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-265">Keywords</span></span>

<span data-ttu-id="02d03-266">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-266"></span></span>
|<span data-ttu-id="02d03-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-268">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-268">dl#</span></span>  <br/> <span data-ttu-id="02d03-269">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-269">driver license</span></span>  <br/> <span data-ttu-id="02d03-270">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-270">driver license number</span></span>  <br/> <span data-ttu-id="02d03-271">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-271">driver licence</span></span>  <br/> <span data-ttu-id="02d03-272">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-272">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-273">drivers license</span></span>  <br/> <span data-ttu-id="02d03-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-274">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-275">driver's license</span></span>  <br/> <span data-ttu-id="02d03-276">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-276">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-277">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-277">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-278">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-278">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-279">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-279">driving license number</span></span>  <br/> <span data-ttu-id="02d03-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-280">dlno#</span></span>  <br/> <span data-ttu-id="02d03-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="02d03-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="02d03-282">덴마크</span><span class="sxs-lookup"><span data-stu-id="02d03-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="02d03-283">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-283">Format</span></span>

<span data-ttu-id="02d03-284">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-285">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-285">Pattern</span></span>

<span data-ttu-id="02d03-286">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="02d03-287">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-287">Checksum</span></span>

<span data-ttu-id="02d03-288">예</span><span class="sxs-lookup"><span data-stu-id="02d03-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-289">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-289">Definition</span></span>

<span data-ttu-id="02d03-290">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-291">정규식이 해당 `Regex_denmark_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-292">from `Keywords_denmark_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="02d03-293">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-293">Keywords</span></span>

<span data-ttu-id="02d03-294">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-294"></span></span>
|<span data-ttu-id="02d03-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-296">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-296">dl#</span></span>  <br/> <span data-ttu-id="02d03-297">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-297">driver license</span></span>  <br/> <span data-ttu-id="02d03-298">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-298">driver license number</span></span>  <br/> <span data-ttu-id="02d03-299">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-299">driver licence</span></span>  <br/> <span data-ttu-id="02d03-300">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-300">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-301">drivers license</span></span>  <br/> <span data-ttu-id="02d03-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-302">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-303">driver's license</span></span>  <br/> <span data-ttu-id="02d03-304">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-304">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-305">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-305">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-306">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-306">driving license number</span></span>  <br/> <span data-ttu-id="02d03-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-307">dlno#</span></span>  <br/> <span data-ttu-id="02d03-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="02d03-308">kørekort</span></span>  <br/> <span data-ttu-id="02d03-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="02d03-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="02d03-310">에스토니아</span><span class="sxs-lookup"><span data-stu-id="02d03-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="02d03-311">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-311">Format</span></span>

<span data-ttu-id="02d03-312">2 개의 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-313">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-313">Pattern</span></span>

<span data-ttu-id="02d03-314">2 개의 문자와 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="02d03-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="02d03-315">문자 "ET" (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="02d03-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="02d03-316">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="02d03-317">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-317">Checksum</span></span>

<span data-ttu-id="02d03-318">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-319">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-319">Definition</span></span>

<span data-ttu-id="02d03-320">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-321">정규식이 해당 `Regex_estonia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-322">from `Keywords_estonia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-323">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-323">Keywords</span></span>

<span data-ttu-id="02d03-324">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-324"></span></span>
|<span data-ttu-id="02d03-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-326">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-326">dl#</span></span>  <br/> <span data-ttu-id="02d03-327">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-327">driver license</span></span>  <br/> <span data-ttu-id="02d03-328">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-328">driver license number</span></span>  <br/> <span data-ttu-id="02d03-329">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-329">driver license number</span></span>  <br/> <span data-ttu-id="02d03-330">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-330">driver licence</span></span>  <br/> <span data-ttu-id="02d03-331">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-331">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-332">drivers license</span></span>  <br/> <span data-ttu-id="02d03-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-333">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-334">driver's license</span></span>  <br/> <span data-ttu-id="02d03-335">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-335">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-336">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-336">driving license number</span></span>  <br/> <span data-ttu-id="02d03-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-337">dlno#</span></span>  <br/> <span data-ttu-id="02d03-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="02d03-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="02d03-339">핀란드</span><span class="sxs-lookup"><span data-stu-id="02d03-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="02d03-340">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-340">Format</span></span>

<span data-ttu-id="02d03-341">하이픈을 포함하는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-342">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-342">Pattern</span></span>

<span data-ttu-id="02d03-343">하이픈을 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="02d03-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="02d03-344">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-344">Six digits</span></span> 
    
- <span data-ttu-id="02d03-345">하이픈</span><span class="sxs-lookup"><span data-stu-id="02d03-345">A hyphen</span></span>
    
-  <span data-ttu-id="02d03-346">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="02d03-347">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-347">Checksum</span></span>

<span data-ttu-id="02d03-348">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-349">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-349">Definition</span></span>

<span data-ttu-id="02d03-350">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-351">정규식이 해당 `Regex_finland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-352">from `Keywords_finland_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-353">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-353">Keywords</span></span>

<span data-ttu-id="02d03-354">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-354"></span></span>
|<span data-ttu-id="02d03-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-356">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-356">dl#</span></span>  <br/> <span data-ttu-id="02d03-357">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-357">driver license</span></span>  <br/> <span data-ttu-id="02d03-358">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-358">driver license number</span></span>  <br/> <span data-ttu-id="02d03-359">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-359">driver licence</span></span>  <br/> <span data-ttu-id="02d03-360">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-360">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-361">drivers license</span></span>  <br/> <span data-ttu-id="02d03-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-362">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-363">driver's license</span></span>  <br/> <span data-ttu-id="02d03-364">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-364">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-365">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-365">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-366">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-366">driving license number</span></span>  <br/> <span data-ttu-id="02d03-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-367">dlno#</span></span>  <br/> <span data-ttu-id="02d03-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="02d03-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="02d03-369">프랑스</span><span class="sxs-lookup"><span data-stu-id="02d03-369">France</span></span>

<span data-ttu-id="02d03-370">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"경기도 운전 면허 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="02d03-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="02d03-371">독일</span><span class="sxs-lookup"><span data-stu-id="02d03-371">Germany</span></span>

<span data-ttu-id="02d03-372">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일어 운전 면허 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="02d03-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="02d03-373">그리스</span><span class="sxs-lookup"><span data-stu-id="02d03-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="02d03-374">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-374">Format</span></span>

<span data-ttu-id="02d03-375">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-376">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-376">Pattern</span></span>

 <span data-ttu-id="02d03-377">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="02d03-378">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-378">Checksum</span></span>

<span data-ttu-id="02d03-379">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-380">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-380">Definition</span></span>

<span data-ttu-id="02d03-381">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-382">정규식이 해당 `Regex_greece_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-383">from `Keywords_greece_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-384">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-384">Keywords</span></span>

<span data-ttu-id="02d03-385">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-385"></span></span>
|<span data-ttu-id="02d03-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-387">dlL</span><span class="sxs-lookup"><span data-stu-id="02d03-387">dlL#</span></span>  <br/> <span data-ttu-id="02d03-388">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-388">driver license</span></span>  <br/> <span data-ttu-id="02d03-389">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-389">driver license number</span></span>  <br/> <span data-ttu-id="02d03-390">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-390">driver licence</span></span>  <br/> <span data-ttu-id="02d03-391">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-391">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-392">drivers license</span></span>  <br/> <span data-ttu-id="02d03-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-393">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-394">driver's license</span></span>  <br/> <span data-ttu-id="02d03-395">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-395">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-396">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-396">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-397">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-397">driving license number</span></span>  <br/> <span data-ttu-id="02d03-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-398">dlno#</span></span>  <br/> <span data-ttu-id="02d03-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="02d03-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="02d03-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="02d03-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="02d03-401">헝가리</span><span class="sxs-lookup"><span data-stu-id="02d03-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="02d03-402">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-402">Format</span></span>

<span data-ttu-id="02d03-403">2 개의 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-404">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-404">Pattern</span></span>

<span data-ttu-id="02d03-405">2 개의 문자와 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="02d03-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="02d03-406">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="02d03-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="02d03-407">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="02d03-408">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-408">Checksum</span></span>

<span data-ttu-id="02d03-409">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-410">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-410">Definition</span></span>

<span data-ttu-id="02d03-411">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-412">정규식이 해당 `Regex_hungary_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-413">from `Keywords_hungary_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-414">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-414">Keywords</span></span>

<span data-ttu-id="02d03-415">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-415"></span></span>
|<span data-ttu-id="02d03-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-417">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-417">dl#</span></span>  <br/> <span data-ttu-id="02d03-418">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-418">driver license</span></span>  <br/> <span data-ttu-id="02d03-419">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-419">driver license number</span></span>  <br/> <span data-ttu-id="02d03-420">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-420">driver licence</span></span>  <br/> <span data-ttu-id="02d03-421">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-421">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-422">drivers license</span></span>  <br/> <span data-ttu-id="02d03-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-423">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-424">driver's license</span></span>  <br/> <span data-ttu-id="02d03-425">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-425">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-426">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-426">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-427">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-427">driving license number</span></span>  <br/> <span data-ttu-id="02d03-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-428">dlno#</span></span>  <br/> <span data-ttu-id="02d03-429">vezetoi</span><span class="sxs-lookup"><span data-stu-id="02d03-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="02d03-430">Ireland</span><span class="sxs-lookup"><span data-stu-id="02d03-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="02d03-431">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-431">Format</span></span>

<span data-ttu-id="02d03-432">6 자리 숫자와 4 개 문자</span><span class="sxs-lookup"><span data-stu-id="02d03-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-433">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-433">Pattern</span></span>

<span data-ttu-id="02d03-434">6 자리 숫자와 4 개 문자:</span><span class="sxs-lookup"><span data-stu-id="02d03-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="02d03-435">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-435">Six digits</span></span>
    
- <span data-ttu-id="02d03-436">4 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="02d03-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="02d03-437">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-437">Checksum</span></span>

<span data-ttu-id="02d03-438">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-439">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-439">Definition</span></span>

<span data-ttu-id="02d03-440">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-441">정규식이 해당 `Regex_ireland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-442">from `Keywords_ireland_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-443">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-443">Keywords</span></span>

<span data-ttu-id="02d03-444">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-444"></span></span>
|<span data-ttu-id="02d03-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-446">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-446">dl#</span></span>  <br/> <span data-ttu-id="02d03-447">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-447">driver license</span></span>  <br/> <span data-ttu-id="02d03-448">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-448">driver license number</span></span>  <br/> <span data-ttu-id="02d03-449">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-449">driver licence</span></span>  <br/> <span data-ttu-id="02d03-450">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-450">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-451">drivers license</span></span>  <br/> <span data-ttu-id="02d03-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-452">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-453">driver's license</span></span>  <br/> <span data-ttu-id="02d03-454">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-454">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-455">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-455">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-456">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-456">driving license number</span></span>  <br/> <span data-ttu-id="02d03-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-457">dlno#</span></span>  <br/> <span data-ttu-id="02d03-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="02d03-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="02d03-459">이탈리아</span><span class="sxs-lookup"><span data-stu-id="02d03-459">Italy</span></span>

<span data-ttu-id="02d03-460">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"이탈리아 운전 면허 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="02d03-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="02d03-461">라트비아</span><span class="sxs-lookup"><span data-stu-id="02d03-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="02d03-462">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-462">Format</span></span>

<span data-ttu-id="02d03-463">3 개의 문자 및 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-464">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-464">Pattern</span></span>

<span data-ttu-id="02d03-465">3 개의 문자 및 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="02d03-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="02d03-466">3 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="02d03-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="02d03-467">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="02d03-468">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-468">Checksum</span></span>

<span data-ttu-id="02d03-469">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-470">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-470">Definition</span></span>

<span data-ttu-id="02d03-471">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-472">정규식이 해당 `Regex_latvia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-473">from `Keywords_latvia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-474">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-474">Keywords</span></span>

<span data-ttu-id="02d03-475">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-475"></span></span>
|<span data-ttu-id="02d03-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-477">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-477">dl#</span></span>  <br/> <span data-ttu-id="02d03-478">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-478">driver license</span></span>  <br/> <span data-ttu-id="02d03-479">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-479">driver license number</span></span>  <br/> <span data-ttu-id="02d03-480">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-480">driver licence</span></span>  <br/> <span data-ttu-id="02d03-481">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-481">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-482">drivers license</span></span>  <br/> <span data-ttu-id="02d03-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-483">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-484">driver's license</span></span>  <br/> <span data-ttu-id="02d03-485">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-485">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-486">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-486">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-487">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-487">driving license number</span></span>  <br/> <span data-ttu-id="02d03-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-488">dlno#</span></span>  <br/> <span data-ttu-id="02d03-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="02d03-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="02d03-490">리투아니아</span><span class="sxs-lookup"><span data-stu-id="02d03-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="02d03-491">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-491">Format</span></span>

<span data-ttu-id="02d03-492">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-493">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-493">Pattern</span></span>

 <span data-ttu-id="02d03-494">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="02d03-495">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-495">Checksum</span></span>

<span data-ttu-id="02d03-496">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-497">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-497">Definition</span></span>

<span data-ttu-id="02d03-498">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-499">정규식이 해당 `Regex_lithuania_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-500">from `Keywords_lithuania_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-501">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-501">Keywords</span></span>

<span data-ttu-id="02d03-502">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-502"></span></span>
|<span data-ttu-id="02d03-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-504">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-504">dl#</span></span>  <br/> <span data-ttu-id="02d03-505">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-505">driver license</span></span>  <br/> <span data-ttu-id="02d03-506">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-506">driver license number</span></span>  <br/> <span data-ttu-id="02d03-507">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-507">driver licence</span></span>  <br/> <span data-ttu-id="02d03-508">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-508">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-509">drivers license</span></span>  <br/> <span data-ttu-id="02d03-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-510">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-511">driver's license</span></span>  <br/> <span data-ttu-id="02d03-512">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-512">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-513">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-513">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-514">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-514">driving license number</span></span>  <br/> <span data-ttu-id="02d03-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-515">dlno#</span></span>  <br/> <span data-ttu-id="02d03-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="02d03-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="02d03-517">셈</span><span class="sxs-lookup"><span data-stu-id="02d03-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="02d03-518">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-518">Format</span></span>

<span data-ttu-id="02d03-519">공백과 구분 기호가 없는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-520">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-520">Pattern</span></span>

 <span data-ttu-id="02d03-521">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="02d03-522">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-522">Checksum</span></span>

<span data-ttu-id="02d03-523">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-524">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-524">Definition</span></span>

<span data-ttu-id="02d03-525">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-526">정규식이 해당 `Regex_luxemburg_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-527">from `Keywords_luxemburg_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-528">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-528">Keywords</span></span>

<span data-ttu-id="02d03-529">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-529"></span></span>
|<span data-ttu-id="02d03-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-531">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-531">dl#</span></span>  <br/> <span data-ttu-id="02d03-532">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-532">driver license</span></span>  <br/> <span data-ttu-id="02d03-533">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-533">driver license number</span></span>  <br/> <span data-ttu-id="02d03-534">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-534">driver licence</span></span>  <br/> <span data-ttu-id="02d03-535">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-535">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-536">drivers license</span></span>  <br/> <span data-ttu-id="02d03-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-537">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-538">driver's license</span></span>  <br/> <span data-ttu-id="02d03-539">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-539">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-540">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-540">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-541">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-541">driving license number</span></span>  <br/> <span data-ttu-id="02d03-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-542">dlno#</span></span>  <br/> <span data-ttu-id="02d03-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="02d03-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="02d03-544">몰타</span><span class="sxs-lookup"><span data-stu-id="02d03-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="02d03-545">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-545">Format</span></span>

<span data-ttu-id="02d03-546">지정 된 패턴에서 두 개의 문자와 6 자리 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="02d03-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-547">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-547">Pattern</span></span>

<span data-ttu-id="02d03-548">두 문자와 6 자리 숫자의 조합:</span><span class="sxs-lookup"><span data-stu-id="02d03-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="02d03-549">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="02d03-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="02d03-550">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="02d03-550">A space (optional)</span></span>
    
- <span data-ttu-id="02d03-551">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-551">Three digits</span></span>
    
- <span data-ttu-id="02d03-552">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="02d03-552">A space (optional)</span></span>
    
- <span data-ttu-id="02d03-553">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="02d03-554">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-554">Checksum</span></span>

<span data-ttu-id="02d03-555">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-556">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-556">Definition</span></span>

<span data-ttu-id="02d03-557">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-558">정규식이 해당 `Regex_malta_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-559">from `Keywords_malta_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-560">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-560">Keywords</span></span>

<span data-ttu-id="02d03-561">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-561"></span></span>
|<span data-ttu-id="02d03-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-563">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-563">dl#</span></span>  <br/> <span data-ttu-id="02d03-564">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-564">driver license</span></span>  <br/> <span data-ttu-id="02d03-565">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-565">driver license number</span></span>  <br/> <span data-ttu-id="02d03-566">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-566">driver licence</span></span>  <br/> <span data-ttu-id="02d03-567">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-567">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-568">drivers license</span></span>  <br/> <span data-ttu-id="02d03-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-569">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-570">driver's license</span></span>  <br/> <span data-ttu-id="02d03-571">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-571">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-572">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-572">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-573">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-573">driving license number</span></span>  <br/> <span data-ttu-id="02d03-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-574">dlno#</span></span>  <br/> <span data-ttu-id="02d03-575">liċenzja tas-sewqan</span><span class="sxs-lookup"><span data-stu-id="02d03-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="02d03-576">네덜란드</span><span class="sxs-lookup"><span data-stu-id="02d03-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="02d03-577">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-577">Format</span></span>

<span data-ttu-id="02d03-578">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-579">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-579">Pattern</span></span>

<span data-ttu-id="02d03-580">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="02d03-581">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-581">Checksum</span></span>

<span data-ttu-id="02d03-582">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-583">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-583">Definition</span></span>

<span data-ttu-id="02d03-584">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-585">정규식이 해당 `Regex_netherlands_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-586">from `Keywords_netherlands_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-587">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-587">Keywords</span></span>

<span data-ttu-id="02d03-588">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-588"></span></span>
|<span data-ttu-id="02d03-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-590">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-590">dl#</span></span>  <br/> <span data-ttu-id="02d03-591">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-591">driver license</span></span>  <br/> <span data-ttu-id="02d03-592">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-592">driver license number</span></span>  <br/> <span data-ttu-id="02d03-593">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-593">driver licence</span></span>  <br/> <span data-ttu-id="02d03-594">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-594">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-595">drivers license</span></span>  <br/> <span data-ttu-id="02d03-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-596">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-597">driver's license</span></span>  <br/> <span data-ttu-id="02d03-598">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-598">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-599">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-599">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-600">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-600">driving license number</span></span>  <br/> <span data-ttu-id="02d03-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-601">dlno#</span></span>  <br/> <span data-ttu-id="02d03-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="02d03-602">permis de conduire</span></span>  <br/> <span data-ttu-id="02d03-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="02d03-603">rijbewijs</span></span>  <br/> <span data-ttu-id="02d03-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="02d03-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="02d03-605">폴란드</span><span class="sxs-lookup"><span data-stu-id="02d03-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="02d03-606">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-606">Format</span></span>

<span data-ttu-id="02d03-607">두 개의 슬래시를 포함 하는 14 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-608">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-608">Pattern</span></span>

<span data-ttu-id="02d03-609">14 자리 숫자와 2 개의 슬래시:</span><span class="sxs-lookup"><span data-stu-id="02d03-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="02d03-610">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-610">Five digits</span></span> 
    
- <span data-ttu-id="02d03-611">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="02d03-611">A forward slash</span></span>
    
- <span data-ttu-id="02d03-612">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-612">Two digits</span></span>
    
- <span data-ttu-id="02d03-613">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="02d03-613">A forward slash</span></span>
    
- <span data-ttu-id="02d03-614">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="02d03-615">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-615">Checksum</span></span>

<span data-ttu-id="02d03-616">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-617">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-617">Definition</span></span>

<span data-ttu-id="02d03-618">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-619">정규식이 해당 `Regex_poland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-620">from `Keywords_poland_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-621">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-621">Keywords</span></span>

<span data-ttu-id="02d03-622">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-622"></span></span>
|<span data-ttu-id="02d03-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-624">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-624">dl#</span></span>  <br/> <span data-ttu-id="02d03-625">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-625">driver license</span></span>  <br/> <span data-ttu-id="02d03-626">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-626">driver license number</span></span>  <br/> <span data-ttu-id="02d03-627">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-627">driver licence</span></span>  <br/> <span data-ttu-id="02d03-628">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-628">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-629">drivers license</span></span>  <br/> <span data-ttu-id="02d03-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-630">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-631">driver's license</span></span>  <br/> <span data-ttu-id="02d03-632">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-632">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-633">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-633">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-634">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-634">driving license number</span></span>  <br/> <span data-ttu-id="02d03-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-635">dlno#</span></span>  <br/> <span data-ttu-id="02d03-636">prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="02d03-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="02d03-637">포르투갈</span><span class="sxs-lookup"><span data-stu-id="02d03-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="02d03-638">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-638">Format</span></span>

<span data-ttu-id="02d03-639">두 개의 문자와 지정 된 패턴에 있는 일곱 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-640">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-640">Pattern</span></span>

<span data-ttu-id="02d03-641">두 문자 다음에 특수 문자를 사용한 7 개의 숫자를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="02d03-642">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="02d03-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="02d03-643">하이픈</span><span class="sxs-lookup"><span data-stu-id="02d03-643">A hyphen</span></span>
    
- <span data-ttu-id="02d03-644">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-644">Six digits</span></span>
    
- <span data-ttu-id="02d03-645">공백</span><span class="sxs-lookup"><span data-stu-id="02d03-645">A space</span></span>
    
- <span data-ttu-id="02d03-646">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="02d03-647">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-647">Checksum</span></span>

<span data-ttu-id="02d03-648">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-649">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-649">Definition</span></span>

<span data-ttu-id="02d03-650">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-651">정규식이 해당 `Regex_portugal_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-652">from `Keywords_portugal_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-653">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-653">Keywords</span></span>

<span data-ttu-id="02d03-654">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-654"></span></span>
|<span data-ttu-id="02d03-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-656">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-656">dl#</span></span>  <br/> <span data-ttu-id="02d03-657">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-657">driver license</span></span>  <br/> <span data-ttu-id="02d03-658">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-658">driver license number</span></span>  <br/> <span data-ttu-id="02d03-659">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-659">driver licence</span></span>  <br/> <span data-ttu-id="02d03-660">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-660">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-661">drivers license</span></span>  <br/> <span data-ttu-id="02d03-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-662">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-663">driver's license</span></span>  <br/> <span data-ttu-id="02d03-664">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-664">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-665">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-665">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-666">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-666">driving license number</span></span>  <br/> <span data-ttu-id="02d03-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-667">dlno#</span></span>  <br/> <span data-ttu-id="02d03-668">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="02d03-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="02d03-669">루마니아</span><span class="sxs-lookup"><span data-stu-id="02d03-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="02d03-670">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-670">Format</span></span>

<span data-ttu-id="02d03-671">한 문자 다음에 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-672">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-672">Pattern</span></span>

<span data-ttu-id="02d03-673">1 개의 문자 다음에 8 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="02d03-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="02d03-674">1 개 문자 (대/소문자 구분 안 함) 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="02d03-675">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="02d03-676">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-676">Checksum</span></span>

<span data-ttu-id="02d03-677">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-678">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-678">Definition</span></span>

<span data-ttu-id="02d03-679">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-680">정규식이 해당 `Regex_romania_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-681">from `Keywords_romania_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-682">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-682">Keywords</span></span>

<span data-ttu-id="02d03-683">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-683"></span></span>
|<span data-ttu-id="02d03-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-685">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-685">dl#</span></span>  <br/> <span data-ttu-id="02d03-686">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-686">driver license</span></span>  <br/> <span data-ttu-id="02d03-687">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-687">driver license number</span></span>  <br/> <span data-ttu-id="02d03-688">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-688">driver licence</span></span>  <br/> <span data-ttu-id="02d03-689">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-689">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-690">drivers license</span></span>  <br/> <span data-ttu-id="02d03-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-691">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-692">driver's license</span></span>  <br/> <span data-ttu-id="02d03-693">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-693">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-694">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-694">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-695">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-695">driving license number</span></span>  <br/> <span data-ttu-id="02d03-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-696">dlno#</span></span>  <br/> <span data-ttu-id="02d03-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="02d03-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="02d03-698">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="02d03-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="02d03-699">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-699">Format</span></span>

<span data-ttu-id="02d03-700">한 문자 다음에 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-701">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-701">Pattern</span></span>

<span data-ttu-id="02d03-702">한 문자 다음에 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="02d03-703">1 개 문자 (대/소문자 구분 안 함) 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="02d03-704">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="02d03-705">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-705">Checksum</span></span>

<span data-ttu-id="02d03-706">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-707">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-707">Definition</span></span>

<span data-ttu-id="02d03-708">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-709">정규식이 해당 `Regex_slovakia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-710">from `Keywords_slovakia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-711">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-711">Keywords</span></span>

<span data-ttu-id="02d03-712">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-712"></span></span>
|<span data-ttu-id="02d03-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-714">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-714">dl#</span></span>  <br/> <span data-ttu-id="02d03-715">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-715">driver license</span></span>  <br/> <span data-ttu-id="02d03-716">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-716">driver license number</span></span>  <br/> <span data-ttu-id="02d03-717">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-717">driver licence</span></span>  <br/> <span data-ttu-id="02d03-718">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-718">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-719">drivers license</span></span>  <br/> <span data-ttu-id="02d03-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-720">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-721">driver's license</span></span>  <br/> <span data-ttu-id="02d03-722">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-722">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-723">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-723">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-724">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-724">driving license number</span></span>  <br/> <span data-ttu-id="02d03-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-725">dlno#</span></span>  <br/> <span data-ttu-id="02d03-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="02d03-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="02d03-727">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="02d03-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="02d03-728">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-728">Format</span></span>

<span data-ttu-id="02d03-729">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-730">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-730">Pattern</span></span>

<span data-ttu-id="02d03-731">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="02d03-732">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-732">Checksum</span></span>

<span data-ttu-id="02d03-733">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-734">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-734">Definition</span></span>

<span data-ttu-id="02d03-735">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-736">정규식이 해당 `Regex_slovenia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-737">from `Keywords_slovenia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-738">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-738">Keywords</span></span>

<span data-ttu-id="02d03-739">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-739"></span></span>
|<span data-ttu-id="02d03-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-741">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-741">dl#</span></span>  <br/> <span data-ttu-id="02d03-742">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-742">driver license</span></span>  <br/> <span data-ttu-id="02d03-743">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-743">driver license number</span></span>  <br/> <span data-ttu-id="02d03-744">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-744">driver licence</span></span>  <br/> <span data-ttu-id="02d03-745">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-745">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-746">drivers license</span></span>  <br/> <span data-ttu-id="02d03-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-747">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-748">driver's license</span></span>  <br/> <span data-ttu-id="02d03-749">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-749">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-750">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-750">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-751">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-751">driving license number</span></span>  <br/> <span data-ttu-id="02d03-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-752">dlno#</span></span>  <br/> <span data-ttu-id="02d03-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="02d03-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="02d03-754">스페인</span><span class="sxs-lookup"><span data-stu-id="02d03-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="02d03-755">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-755">Format</span></span>

<span data-ttu-id="02d03-756">8 자리 숫자와 문자 1 개</span><span class="sxs-lookup"><span data-stu-id="02d03-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-757">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-757">Pattern</span></span>

<span data-ttu-id="02d03-758">8 자리 숫자와 문자 1 개:</span><span class="sxs-lookup"><span data-stu-id="02d03-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="02d03-759">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-759">Eight digits</span></span> 
    
- <span data-ttu-id="02d03-760">1 자리 숫자 또는 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="02d03-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="02d03-761">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-761">Checksum</span></span>

<span data-ttu-id="02d03-762">예</span><span class="sxs-lookup"><span data-stu-id="02d03-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-763">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-763">Definition</span></span>

<span data-ttu-id="02d03-764">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-765">이 함수 `Func_spain_eu_driver's_license_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-766">from `Keywords_spain_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="02d03-767">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-767">Keywords</span></span>

<span data-ttu-id="02d03-768">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-768"></span></span>
|<span data-ttu-id="02d03-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-770">dlno#</span></span>  <br/> <span data-ttu-id="02d03-771">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-771">dl#</span></span>  <br/> <span data-ttu-id="02d03-772">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-772">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-773">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-773">driver licence</span></span>  <br/> <span data-ttu-id="02d03-774">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-774">driver license</span></span>  <br/> <span data-ttu-id="02d03-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-775">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-776">drivers license</span></span>  <br/> <span data-ttu-id="02d03-777">driver's licence</span><span class="sxs-lookup"><span data-stu-id="02d03-777">driver's licence</span></span>  <br/> <span data-ttu-id="02d03-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-778">driver's license</span></span>  <br/> <span data-ttu-id="02d03-779">driving licence</span><span class="sxs-lookup"><span data-stu-id="02d03-779">driving licence</span></span>  <br/> <span data-ttu-id="02d03-780">driving license</span><span class="sxs-lookup"><span data-stu-id="02d03-780">driving license</span></span>  <br/> <span data-ttu-id="02d03-781">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-781">driver licence number</span></span>  <br/> <span data-ttu-id="02d03-782">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-782">driver license number</span></span>  <br/> <span data-ttu-id="02d03-783">영향 요소 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-783">drivers licence number</span></span>  <br/> <span data-ttu-id="02d03-784">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-784">drivers license number</span></span>  <br/> <span data-ttu-id="02d03-785">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-785">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-786">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-786">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-787">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-787">driving licence number</span></span>  <br/> <span data-ttu-id="02d03-788">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-788">driving license number</span></span>  <br/> <span data-ttu-id="02d03-789">추진 허용</span><span class="sxs-lookup"><span data-stu-id="02d03-789">driving permit</span></span>  <br/> <span data-ttu-id="02d03-790">제어 허용 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-790">driving permit number</span></span>  <br/> <span data-ttu-id="02d03-791">permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="02d03-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="02d03-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="02d03-792">permiso conducción</span></span>  <br/> <span data-ttu-id="02d03-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="02d03-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="02d03-794">número de 네트워크 de conducir</span><span class="sxs-lookup"><span data-stu-id="02d03-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="02d03-795">número carnet conducir</span><span class="sxs-lookup"><span data-stu-id="02d03-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="02d03-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="02d03-796">licencia conducir</span></span>  <br/> <span data-ttu-id="02d03-797">número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="02d03-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="02d03-798">número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="02d03-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="02d03-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="02d03-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="02d03-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="02d03-800">permiso conducir</span></span>  <br/> <span data-ttu-id="02d03-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="02d03-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="02d03-802">el carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="02d03-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="02d03-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="02d03-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="02d03-804">스웨덴</span><span class="sxs-lookup"><span data-stu-id="02d03-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="02d03-805">형식일</span><span class="sxs-lookup"><span data-stu-id="02d03-805">Format</span></span>

<span data-ttu-id="02d03-806">하이픈을 포함 하는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="02d03-807">패턴</span><span class="sxs-lookup"><span data-stu-id="02d03-807">Pattern</span></span>

<span data-ttu-id="02d03-808">하이픈을 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="02d03-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="02d03-809">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-809">Six digits</span></span> 
    
- <span data-ttu-id="02d03-810">하이픈</span><span class="sxs-lookup"><span data-stu-id="02d03-810">A hyphen</span></span>
    
- <span data-ttu-id="02d03-811">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="02d03-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="02d03-812">제외</span><span class="sxs-lookup"><span data-stu-id="02d03-812">Checksum</span></span>

<span data-ttu-id="02d03-813">아니요</span><span class="sxs-lookup"><span data-stu-id="02d03-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="02d03-814">정의</span><span class="sxs-lookup"><span data-stu-id="02d03-814">Definition</span></span>

<span data-ttu-id="02d03-815">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="02d03-816">정규식이 해당 `Regex_sweden_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="02d03-817">from `Keywords_sweden_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="02d03-818">키워드</span><span class="sxs-lookup"><span data-stu-id="02d03-818">Keywords</span></span>

<span data-ttu-id="02d03-819">| |</span><span class="sxs-lookup"><span data-stu-id="02d03-819"></span></span>
|<span data-ttu-id="02d03-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="02d03-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="02d03-821">dl</span><span class="sxs-lookup"><span data-stu-id="02d03-821">dl#</span></span>  <br/> <span data-ttu-id="02d03-822">driver license</span><span class="sxs-lookup"><span data-stu-id="02d03-822">driver license</span></span>  <br/> <span data-ttu-id="02d03-823">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-823">driver license number</span></span>  <br/> <span data-ttu-id="02d03-824">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="02d03-824">driver licence</span></span>  <br/> <span data-ttu-id="02d03-825">drivers lic</span><span class="sxs-lookup"><span data-stu-id="02d03-825">drivers lic.</span></span>  <br/> <span data-ttu-id="02d03-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="02d03-826">drivers license</span></span>  <br/> <span data-ttu-id="02d03-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="02d03-827">drivers licence</span></span>  <br/> <span data-ttu-id="02d03-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="02d03-828">driver's license</span></span>  <br/> <span data-ttu-id="02d03-829">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-829">driver's license number</span></span>  <br/> <span data-ttu-id="02d03-830">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-830">driver's licence number</span></span>  <br/> <span data-ttu-id="02d03-831">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="02d03-831">driving license number</span></span>  <br/> <span data-ttu-id="02d03-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="02d03-832">dlno#</span></span>  <br/> <span data-ttu-id="02d03-833">körkort</span><span class="sxs-lookup"><span data-stu-id="02d03-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="02d03-834">영국의</span><span class="sxs-lookup"><span data-stu-id="02d03-834">UK</span></span>

<span data-ttu-id="02d03-835">자세한 내용은 영국 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="02d03-835">For details, see the section "U.K.</span></span> <span data-ttu-id="02d03-836">[중요 한 정보 유형에 서 확인 되는](what-the-sensitive-information-types-look-for.md)운전 면허 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="02d03-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="02d03-837">참고 항목</span><span class="sxs-lookup"><span data-stu-id="02d03-837">See also</span></span>

[<span data-ttu-id="02d03-838">중요한 정보 유형이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="02d03-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

