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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255776"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="4ceb4-104">EU 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-104">EU Driver's License Number</span></span>

<span data-ttu-id="4ceb4-105">이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 드라이버의 라이선스 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="4ceb4-106">이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="4ceb4-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="4ceb4-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-108">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-108">Format</span></span>

<span data-ttu-id="4ceb4-109">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-110">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-110">Pattern</span></span>

<span data-ttu-id="4ceb4-111">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4ceb4-112">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-112">Checksum</span></span>

<span data-ttu-id="4ceb4-113">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-114">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-114">Definition</span></span>

<span data-ttu-id="4ceb4-115">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-116">정규식이 해당 `Regex_austria_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-117">from `Keywords_austria_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="4ceb4-118">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-118">Keywords</span></span>

<span data-ttu-id="4ceb4-119">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-119"></span></span>
|<span data-ttu-id="4ceb4-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-121">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-121">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-122">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-122">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-123">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-123">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-124">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-124">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-125">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-125">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-126">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-127">driver's licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-127">driver's licence</span></span>  <br/> <span data-ttu-id="4ceb4-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-128">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-129">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-129">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-130">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="4ceb4-131">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-131">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-132">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-133">fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="4ceb4-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="4ceb4-134">fuhrerschein republik osterreich</span><span class="sxs-lookup"><span data-stu-id="4ceb4-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="4ceb4-135">벨기에</span><span class="sxs-lookup"><span data-stu-id="4ceb4-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-136">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-136">Format</span></span>

<span data-ttu-id="4ceb4-137">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-138">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-138">Pattern</span></span>

<span data-ttu-id="4ceb4-139">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4ceb4-140">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-140">Checksum</span></span>

<span data-ttu-id="4ceb4-141">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-142">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-142">Definition</span></span>

<span data-ttu-id="4ceb4-143">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-144">정규식이 해당 `Regex_belgium_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-145">from `Keywords_belgium_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="4ceb4-146">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-146">Keywords</span></span>

<span data-ttu-id="4ceb4-147">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-147"></span></span>
|<span data-ttu-id="4ceb4-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-149">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-149">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-150">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-150">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-151">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-151">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-152">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-152">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-153">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-153">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-154">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-155">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-156">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-157">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-157">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-158">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-158">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-159">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="4ceb4-160">rijbewijs</span></span>  <br/> <span data-ttu-id="4ceb4-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="4ceb4-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="4ceb4-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="4ceb4-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="4ceb4-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="4ceb4-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="4ceb4-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="4ceb4-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="4ceb4-165">führerschein-veiligheid</span><span class="sxs-lookup"><span data-stu-id="4ceb4-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="4ceb4-166">fuehrerschein-veiligheid</span><span class="sxs-lookup"><span data-stu-id="4ceb4-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="4ceb4-167">fuehrerschein-veiligheid</span><span class="sxs-lookup"><span data-stu-id="4ceb4-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="4ceb4-168">불가리아</span><span class="sxs-lookup"><span data-stu-id="4ceb4-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-169">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-169">Format</span></span>

<span data-ttu-id="4ceb4-170">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-171">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-171">Pattern</span></span>

<span data-ttu-id="4ceb4-172">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4ceb4-173">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-173">Checksum</span></span>

<span data-ttu-id="4ceb4-174">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-175">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-175">Definition</span></span>

<span data-ttu-id="4ceb4-176">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-177">정규식이 해당 `Regex_bulgaria_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-178">from `Keywords_bulgaria_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="4ceb4-179">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-179">Keywords</span></span>

<span data-ttu-id="4ceb4-180">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-180"></span></span>
|<span data-ttu-id="4ceb4-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-182">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-182">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-183">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-183">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-184">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-184">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-185">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-185">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-186">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-186">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-187">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-188">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-189">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-190">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-190">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-191">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-191">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-192">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-192">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-193">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="4ceb4-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="4ceb4-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="4ceb4-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="4ceb4-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="4ceb4-196">сумпс</span></span>  <br/> <span data-ttu-id="4ceb4-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="4ceb4-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="4ceb4-198">크로아티아</span><span class="sxs-lookup"><span data-stu-id="4ceb4-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-199">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-199">Format</span></span>

<span data-ttu-id="4ceb4-200">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-201">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-201">Pattern</span></span>

<span data-ttu-id="4ceb4-202">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4ceb4-203">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-203">Checksum</span></span>

<span data-ttu-id="4ceb4-204">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-205">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-205">Definition</span></span>

<span data-ttu-id="4ceb4-206">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-207">정규식이 해당 `Regex_croatia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-208">from `Keywords_croatia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="4ceb4-209">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-209">Keywords</span></span>

<span data-ttu-id="4ceb4-210">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-210"></span></span>
|<span data-ttu-id="4ceb4-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-212">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-212">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-213">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-213">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-214">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-214">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-215">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-215">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-216">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-216">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-217">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-218">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-219">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-220">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-220">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-221">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-221">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-222">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-222">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-223">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="4ceb4-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="4ceb4-225">키프로스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-226">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-226">Format</span></span>

<span data-ttu-id="4ceb4-227">공백과 구분 기호를 사용 하지 않고 12 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-228">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-228">Pattern</span></span>

<span data-ttu-id="4ceb4-229">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4ceb4-230">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-230">Checksum</span></span>

<span data-ttu-id="4ceb4-231">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-232">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-232">Definition</span></span>

<span data-ttu-id="4ceb4-233">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-234">정규식이 해당 `Regex_cyprus_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-235">from `Keywords_cyprus_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-236">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-236">Keywords</span></span>

<span data-ttu-id="4ceb4-237">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-237"></span></span>
|<span data-ttu-id="4ceb4-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-239">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-239">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-240">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-240">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-241">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-241">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-242">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-242">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-243">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-243">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-244">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-245">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-246">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-246">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-247">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-247">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-248">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-248">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-249">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="4ceb4-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="4ceb4-251">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="4ceb4-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-252">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-252">Format</span></span>

<span data-ttu-id="4ceb4-253">2 개의 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-254">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-254">Pattern</span></span>

<span data-ttu-id="4ceb4-255">8 개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="4ceb4-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="4ceb4-256">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="4ceb4-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="4ceb4-257">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="4ceb4-257">A space (optional)</span></span>
    
- <span data-ttu-id="4ceb4-258">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4ceb4-259">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-259">Checksum</span></span>

<span data-ttu-id="4ceb4-260">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-261">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-261">Definition</span></span>

<span data-ttu-id="4ceb4-262">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-263">정규식이 해당 `Regex_czech_republic_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-264">from `Keywords_czech_republic_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="4ceb4-265">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-265">Keywords</span></span>

<span data-ttu-id="4ceb4-266">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-266"></span></span>
|<span data-ttu-id="4ceb4-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-268">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-268">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-269">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-269">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-270">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-270">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-271">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-271">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-272">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-272">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-273">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-274">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-275">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-276">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-276">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-277">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-277">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-278">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-278">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-279">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-279">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-280">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="4ceb4-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="4ceb4-282">덴마크</span><span class="sxs-lookup"><span data-stu-id="4ceb4-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-283">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-283">Format</span></span>

<span data-ttu-id="4ceb4-284">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-285">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-285">Pattern</span></span>

<span data-ttu-id="4ceb4-286">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4ceb4-287">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-287">Checksum</span></span>

<span data-ttu-id="4ceb4-288">예</span><span class="sxs-lookup"><span data-stu-id="4ceb4-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-289">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-289">Definition</span></span>

<span data-ttu-id="4ceb4-290">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-291">정규식이 해당 `Regex_denmark_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-292">from `Keywords_denmark_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="4ceb4-293">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-293">Keywords</span></span>

<span data-ttu-id="4ceb4-294">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-294"></span></span>
|<span data-ttu-id="4ceb4-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-296">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-296">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-297">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-297">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-298">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-298">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-299">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-299">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-300">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-300">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-301">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-302">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-303">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-304">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-304">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-305">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-305">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-306">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-306">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-307">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="4ceb4-308">kørekort</span></span>  <br/> <span data-ttu-id="4ceb4-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="4ceb4-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="4ceb4-310">에스토니아</span><span class="sxs-lookup"><span data-stu-id="4ceb4-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-311">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-311">Format</span></span>

<span data-ttu-id="4ceb4-312">2 개의 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-313">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-313">Pattern</span></span>

<span data-ttu-id="4ceb4-314">2 개의 문자와 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="4ceb4-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="4ceb4-315">문자 "ET" (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="4ceb4-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="4ceb4-316">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4ceb4-317">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-317">Checksum</span></span>

<span data-ttu-id="4ceb4-318">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-319">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-319">Definition</span></span>

<span data-ttu-id="4ceb4-320">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-321">정규식이 해당 `Regex_estonia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-322">from `Keywords_estonia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-323">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-323">Keywords</span></span>

<span data-ttu-id="4ceb4-324">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-324"></span></span>
|<span data-ttu-id="4ceb4-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-326">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-326">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-327">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-327">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-328">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-328">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-329">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-329">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-330">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-330">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-331">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-331">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-332">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-333">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-334">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-335">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-335">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-336">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-336">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-337">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="4ceb4-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="4ceb4-339">핀란드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-340">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-340">Format</span></span>

<span data-ttu-id="4ceb4-341">하이픈을 포함하는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-342">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-342">Pattern</span></span>

<span data-ttu-id="4ceb4-343">하이픈을 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="4ceb4-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="4ceb4-344">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-344">Six digits</span></span> 
    
- <span data-ttu-id="4ceb4-345">하이픈</span><span class="sxs-lookup"><span data-stu-id="4ceb4-345">A hyphen</span></span>
    
-  <span data-ttu-id="4ceb4-346">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4ceb4-347">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-347">Checksum</span></span>

<span data-ttu-id="4ceb4-348">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-349">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-349">Definition</span></span>

<span data-ttu-id="4ceb4-350">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-351">정규식이 해당 `Regex_finland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-352">from `Keywords_finland_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-353">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-353">Keywords</span></span>

<span data-ttu-id="4ceb4-354">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-354"></span></span>
|<span data-ttu-id="4ceb4-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-356">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-356">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-357">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-357">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-358">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-358">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-359">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-359">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-360">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-360">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-361">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-362">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-363">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-364">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-364">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-365">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-365">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-366">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-366">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-367">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="4ceb4-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="4ceb4-369">프랑스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-369">France</span></span>

<span data-ttu-id="4ceb4-370">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"경기도 운전 면허 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="4ceb4-371">독일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-371">Germany</span></span>

<span data-ttu-id="4ceb4-372">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일어 운전 면허 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="4ceb4-373">그리스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-374">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-374">Format</span></span>

<span data-ttu-id="4ceb4-375">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-376">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-376">Pattern</span></span>

 <span data-ttu-id="4ceb4-377">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="4ceb4-378">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-378">Checksum</span></span>

<span data-ttu-id="4ceb4-379">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-380">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-380">Definition</span></span>

<span data-ttu-id="4ceb4-381">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-382">정규식이 해당 `Regex_greece_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-383">from `Keywords_greece_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-384">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-384">Keywords</span></span>

<span data-ttu-id="4ceb4-385">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-385"></span></span>
|<span data-ttu-id="4ceb4-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-387">dlL</span><span class="sxs-lookup"><span data-stu-id="4ceb4-387">dlL#</span></span>  <br/> <span data-ttu-id="4ceb4-388">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-388">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-389">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-389">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-390">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-390">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-391">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-391">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-392">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-393">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-394">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-395">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-395">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-396">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-396">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-397">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-397">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-398">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="4ceb4-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="4ceb4-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="4ceb4-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="4ceb4-401">헝가리</span><span class="sxs-lookup"><span data-stu-id="4ceb4-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-402">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-402">Format</span></span>

<span data-ttu-id="4ceb4-403">2 개의 문자 다음에 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-404">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-404">Pattern</span></span>

<span data-ttu-id="4ceb4-405">2 개의 문자와 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="4ceb4-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="4ceb4-406">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="4ceb4-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="4ceb4-407">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4ceb4-408">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-408">Checksum</span></span>

<span data-ttu-id="4ceb4-409">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-410">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-410">Definition</span></span>

<span data-ttu-id="4ceb4-411">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-412">정규식이 해당 `Regex_hungary_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-413">from `Keywords_hungary_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-414">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-414">Keywords</span></span>

<span data-ttu-id="4ceb4-415">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-415"></span></span>
|<span data-ttu-id="4ceb4-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-417">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-417">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-418">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-418">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-419">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-419">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-420">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-420">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-421">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-421">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-422">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-423">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-424">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-425">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-425">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-426">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-426">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-427">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-427">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-428">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-429">vezetoi</span><span class="sxs-lookup"><span data-stu-id="4ceb4-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="4ceb4-430">Ireland</span><span class="sxs-lookup"><span data-stu-id="4ceb4-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-431">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-431">Format</span></span>

<span data-ttu-id="4ceb4-432">6 자리 숫자와 4 개 문자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-433">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-433">Pattern</span></span>

<span data-ttu-id="4ceb4-434">6 자리 숫자와 4 개 문자:</span><span class="sxs-lookup"><span data-stu-id="4ceb4-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="4ceb4-435">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-435">Six digits</span></span>
    
- <span data-ttu-id="4ceb4-436">4 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="4ceb4-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4ceb4-437">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-437">Checksum</span></span>

<span data-ttu-id="4ceb4-438">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-439">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-439">Definition</span></span>

<span data-ttu-id="4ceb4-440">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-441">정규식이 해당 `Regex_ireland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-442">from `Keywords_ireland_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-443">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-443">Keywords</span></span>

<span data-ttu-id="4ceb4-444">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-444"></span></span>
|<span data-ttu-id="4ceb4-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-446">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-446">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-447">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-447">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-448">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-448">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-449">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-449">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-450">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-450">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-451">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-452">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-453">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-454">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-454">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-455">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-455">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-456">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-456">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-457">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="4ceb4-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="4ceb4-459">이탈리아</span><span class="sxs-lookup"><span data-stu-id="4ceb4-459">Italy</span></span>

<span data-ttu-id="4ceb4-460">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"이탈리아 운전 면허 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="4ceb4-461">라트비아</span><span class="sxs-lookup"><span data-stu-id="4ceb4-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-462">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-462">Format</span></span>

<span data-ttu-id="4ceb4-463">3 개의 문자 및 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-464">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-464">Pattern</span></span>

<span data-ttu-id="4ceb4-465">3 개의 문자 및 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="4ceb4-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="4ceb4-466">3 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="4ceb4-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="4ceb4-467">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4ceb4-468">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-468">Checksum</span></span>

<span data-ttu-id="4ceb4-469">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-470">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-470">Definition</span></span>

<span data-ttu-id="4ceb4-471">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-472">정규식이 해당 `Regex_latvia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-473">from `Keywords_latvia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-474">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-474">Keywords</span></span>

<span data-ttu-id="4ceb4-475">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-475"></span></span>
|<span data-ttu-id="4ceb4-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-477">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-477">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-478">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-478">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-479">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-479">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-480">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-480">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-481">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-481">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-482">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-483">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-484">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-485">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-485">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-486">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-486">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-487">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-487">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-488">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="4ceb4-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="4ceb4-490">리투아니아</span><span class="sxs-lookup"><span data-stu-id="4ceb4-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-491">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-491">Format</span></span>

<span data-ttu-id="4ceb4-492">공백과 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-493">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-493">Pattern</span></span>

 <span data-ttu-id="4ceb4-494">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="4ceb4-495">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-495">Checksum</span></span>

<span data-ttu-id="4ceb4-496">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-497">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-497">Definition</span></span>

<span data-ttu-id="4ceb4-498">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-499">정규식이 해당 `Regex_lithuania_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-500">from `Keywords_lithuania_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-501">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-501">Keywords</span></span>

<span data-ttu-id="4ceb4-502">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-502"></span></span>
|<span data-ttu-id="4ceb4-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-504">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-504">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-505">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-505">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-506">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-506">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-507">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-507">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-508">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-508">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-509">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-510">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-511">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-512">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-512">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-513">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-513">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-514">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-514">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-515">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="4ceb4-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="4ceb4-517">셈</span><span class="sxs-lookup"><span data-stu-id="4ceb4-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-518">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-518">Format</span></span>

<span data-ttu-id="4ceb4-519">공백과 구분 기호가 없는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-520">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-520">Pattern</span></span>

 <span data-ttu-id="4ceb4-521">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="4ceb4-522">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-522">Checksum</span></span>

<span data-ttu-id="4ceb4-523">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-524">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-524">Definition</span></span>

<span data-ttu-id="4ceb4-525">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-526">정규식이 해당 `Regex_luxemburg_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-527">from `Keywords_luxemburg_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-528">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-528">Keywords</span></span>

<span data-ttu-id="4ceb4-529">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-529"></span></span>
|<span data-ttu-id="4ceb4-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-531">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-531">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-532">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-532">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-533">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-533">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-534">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-534">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-535">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-535">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-536">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-537">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-538">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-539">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-539">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-540">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-540">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-541">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-541">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-542">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="4ceb4-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="4ceb4-544">몰타</span><span class="sxs-lookup"><span data-stu-id="4ceb4-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-545">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-545">Format</span></span>

<span data-ttu-id="4ceb4-546">지정 된 패턴에서 두 개의 문자와 6 자리 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="4ceb4-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-547">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-547">Pattern</span></span>

<span data-ttu-id="4ceb4-548">두 문자와 6 자리 숫자의 조합:</span><span class="sxs-lookup"><span data-stu-id="4ceb4-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="4ceb4-549">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="4ceb4-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="4ceb4-550">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="4ceb4-550">A space (optional)</span></span>
    
- <span data-ttu-id="4ceb4-551">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-551">Three digits</span></span>
    
- <span data-ttu-id="4ceb4-552">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="4ceb4-552">A space (optional)</span></span>
    
- <span data-ttu-id="4ceb4-553">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4ceb4-554">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-554">Checksum</span></span>

<span data-ttu-id="4ceb4-555">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-556">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-556">Definition</span></span>

<span data-ttu-id="4ceb4-557">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-558">정규식이 해당 `Regex_malta_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-559">from `Keywords_malta_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-560">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-560">Keywords</span></span>

<span data-ttu-id="4ceb4-561">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-561"></span></span>
|<span data-ttu-id="4ceb4-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-563">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-563">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-564">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-564">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-565">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-565">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-566">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-566">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-567">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-567">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-568">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-569">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-570">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-571">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-571">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-572">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-572">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-573">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-573">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-574">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-575">liċenzja tas-sewqan</span><span class="sxs-lookup"><span data-stu-id="4ceb4-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="4ceb4-576">네덜란드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-577">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-577">Format</span></span>

<span data-ttu-id="4ceb4-578">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-579">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-579">Pattern</span></span>

<span data-ttu-id="4ceb4-580">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4ceb4-581">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-581">Checksum</span></span>

<span data-ttu-id="4ceb4-582">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-583">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-583">Definition</span></span>

<span data-ttu-id="4ceb4-584">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-585">정규식이 해당 `Regex_netherlands_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-586">from `Keywords_netherlands_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-587">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-587">Keywords</span></span>

<span data-ttu-id="4ceb4-588">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-588"></span></span>
|<span data-ttu-id="4ceb4-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-590">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-590">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-591">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-591">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-592">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-592">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-593">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-593">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-594">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-594">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-595">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-596">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-597">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-598">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-598">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-599">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-599">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-600">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-600">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-601">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="4ceb4-602">permis de conduire</span></span>  <br/> <span data-ttu-id="4ceb4-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="4ceb4-603">rijbewijs</span></span>  <br/> <span data-ttu-id="4ceb4-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="4ceb4-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="4ceb4-605">폴란드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-606">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-606">Format</span></span>

<span data-ttu-id="4ceb4-607">두 개의 슬래시를 포함 하는 14 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-608">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-608">Pattern</span></span>

<span data-ttu-id="4ceb4-609">14 자리 숫자와 2 개의 슬래시:</span><span class="sxs-lookup"><span data-stu-id="4ceb4-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="4ceb4-610">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-610">Five digits</span></span> 
    
- <span data-ttu-id="4ceb4-611">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="4ceb4-611">A forward slash</span></span>
    
- <span data-ttu-id="4ceb4-612">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-612">Two digits</span></span>
    
- <span data-ttu-id="4ceb4-613">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="4ceb4-613">A forward slash</span></span>
    
- <span data-ttu-id="4ceb4-614">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4ceb4-615">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-615">Checksum</span></span>

<span data-ttu-id="4ceb4-616">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-617">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-617">Definition</span></span>

<span data-ttu-id="4ceb4-618">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-619">정규식이 해당 `Regex_poland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-620">from `Keywords_poland_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-621">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-621">Keywords</span></span>

<span data-ttu-id="4ceb4-622">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-622"></span></span>
|<span data-ttu-id="4ceb4-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-624">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-624">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-625">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-625">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-626">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-626">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-627">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-627">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-628">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-628">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-629">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-630">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-631">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-632">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-632">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-633">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-633">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-634">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-634">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-635">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-636">prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="4ceb4-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="4ceb4-637">포르투갈</span><span class="sxs-lookup"><span data-stu-id="4ceb4-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-638">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-638">Format</span></span>

<span data-ttu-id="4ceb4-639">두 개의 문자와 지정 된 패턴에 있는 일곱 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-640">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-640">Pattern</span></span>

<span data-ttu-id="4ceb4-641">두 문자 다음에 특수 문자를 사용한 7 개의 숫자를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="4ceb4-642">2 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="4ceb4-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="4ceb4-643">하이픈</span><span class="sxs-lookup"><span data-stu-id="4ceb4-643">A hyphen</span></span>
    
- <span data-ttu-id="4ceb4-644">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-644">Six digits</span></span>
    
- <span data-ttu-id="4ceb4-645">공백</span><span class="sxs-lookup"><span data-stu-id="4ceb4-645">A space</span></span>
    
- <span data-ttu-id="4ceb4-646">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4ceb4-647">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-647">Checksum</span></span>

<span data-ttu-id="4ceb4-648">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-649">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-649">Definition</span></span>

<span data-ttu-id="4ceb4-650">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-651">정규식이 해당 `Regex_portugal_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-652">from `Keywords_portugal_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-653">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-653">Keywords</span></span>

<span data-ttu-id="4ceb4-654">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-654"></span></span>
|<span data-ttu-id="4ceb4-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-656">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-656">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-657">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-657">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-658">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-658">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-659">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-659">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-660">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-660">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-661">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-662">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-663">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-664">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-664">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-665">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-665">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-666">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-666">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-667">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-668">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="4ceb4-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="4ceb4-669">루마니아</span><span class="sxs-lookup"><span data-stu-id="4ceb4-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-670">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-670">Format</span></span>

<span data-ttu-id="4ceb4-671">한 문자 다음에 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-672">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-672">Pattern</span></span>

<span data-ttu-id="4ceb4-673">1 개의 문자 다음에 8 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="4ceb4-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="4ceb4-674">1 개 문자 (대/소문자 구분 안 함) 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="4ceb4-675">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4ceb4-676">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-676">Checksum</span></span>

<span data-ttu-id="4ceb4-677">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-678">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-678">Definition</span></span>

<span data-ttu-id="4ceb4-679">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-680">정규식이 해당 `Regex_romania_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-681">from `Keywords_romania_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-682">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-682">Keywords</span></span>

<span data-ttu-id="4ceb4-683">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-683"></span></span>
|<span data-ttu-id="4ceb4-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-685">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-685">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-686">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-686">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-687">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-687">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-688">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-688">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-689">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-689">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-690">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-691">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-692">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-693">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-693">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-694">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-694">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-695">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-695">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-696">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="4ceb4-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="4ceb4-698">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="4ceb4-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-699">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-699">Format</span></span>

<span data-ttu-id="4ceb4-700">한 문자 다음에 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-701">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-701">Pattern</span></span>

<span data-ttu-id="4ceb4-702">한 문자 다음에 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="4ceb4-703">1 개 문자 (대/소문자 구분 안 함) 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="4ceb4-704">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4ceb4-705">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-705">Checksum</span></span>

<span data-ttu-id="4ceb4-706">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-707">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-707">Definition</span></span>

<span data-ttu-id="4ceb4-708">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-709">정규식이 해당 `Regex_slovakia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-710">from `Keywords_slovakia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-711">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-711">Keywords</span></span>

<span data-ttu-id="4ceb4-712">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-712"></span></span>
|<span data-ttu-id="4ceb4-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-714">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-714">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-715">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-715">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-716">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-716">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-717">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-717">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-718">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-718">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-719">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-720">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-721">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-722">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-722">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-723">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-723">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-724">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-724">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-725">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="4ceb4-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="4ceb4-727">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="4ceb4-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-728">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-728">Format</span></span>

<span data-ttu-id="4ceb4-729">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-730">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-730">Pattern</span></span>

<span data-ttu-id="4ceb4-731">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4ceb4-732">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-732">Checksum</span></span>

<span data-ttu-id="4ceb4-733">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-734">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-734">Definition</span></span>

<span data-ttu-id="4ceb4-735">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-736">정규식이 해당 `Regex_slovenia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-737">from `Keywords_slovenia_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-738">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-738">Keywords</span></span>

<span data-ttu-id="4ceb4-739">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-739"></span></span>
|<span data-ttu-id="4ceb4-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-741">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-741">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-742">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-742">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-743">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-743">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-744">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-744">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-745">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-745">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-746">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-747">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-748">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-749">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-749">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-750">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-750">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-751">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-751">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-752">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="4ceb4-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="4ceb4-754">스페인</span><span class="sxs-lookup"><span data-stu-id="4ceb4-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-755">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-755">Format</span></span>

<span data-ttu-id="4ceb4-756">8 자리 숫자와 문자 1 개</span><span class="sxs-lookup"><span data-stu-id="4ceb4-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-757">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-757">Pattern</span></span>

<span data-ttu-id="4ceb4-758">8 자리 숫자와 문자 1 개:</span><span class="sxs-lookup"><span data-stu-id="4ceb4-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="4ceb4-759">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-759">Eight digits</span></span> 
    
- <span data-ttu-id="4ceb4-760">1 자리 숫자 또는 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="4ceb4-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4ceb4-761">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-761">Checksum</span></span>

<span data-ttu-id="4ceb4-762">예</span><span class="sxs-lookup"><span data-stu-id="4ceb4-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-763">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-763">Definition</span></span>

<span data-ttu-id="4ceb4-764">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-765">이 함수 `Func_spain_eu_driver's_license_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-766">from `Keywords_spain_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-767">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-767">Keywords</span></span>

<span data-ttu-id="4ceb4-768">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-768"></span></span>
|<span data-ttu-id="4ceb4-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-770">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-771">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-771">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-772">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-772">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-773">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-773">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-774">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-774">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-775">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-776">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-777">driver's licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-777">driver's licence</span></span>  <br/> <span data-ttu-id="4ceb4-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-778">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-779">driving licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-779">driving licence</span></span>  <br/> <span data-ttu-id="4ceb4-780">driving license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-780">driving license</span></span>  <br/> <span data-ttu-id="4ceb4-781">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-781">driver licence number</span></span>  <br/> <span data-ttu-id="4ceb4-782">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-782">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-783">영향 요소 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-783">drivers licence number</span></span>  <br/> <span data-ttu-id="4ceb4-784">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-784">drivers license number</span></span>  <br/> <span data-ttu-id="4ceb4-785">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-785">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-786">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-786">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-787">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-787">driving licence number</span></span>  <br/> <span data-ttu-id="4ceb4-788">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-788">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-789">추진 허용</span><span class="sxs-lookup"><span data-stu-id="4ceb4-789">driving permit</span></span>  <br/> <span data-ttu-id="4ceb4-790">제어 허용 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-790">driving permit number</span></span>  <br/> <span data-ttu-id="4ceb4-791">permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="4ceb4-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="4ceb4-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="4ceb4-792">permiso conducción</span></span>  <br/> <span data-ttu-id="4ceb4-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="4ceb4-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="4ceb4-794">número de 네트워크 de conducir</span><span class="sxs-lookup"><span data-stu-id="4ceb4-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="4ceb4-795">número carnet conducir</span><span class="sxs-lookup"><span data-stu-id="4ceb4-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="4ceb4-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="4ceb4-796">licencia conducir</span></span>  <br/> <span data-ttu-id="4ceb4-797">número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="4ceb4-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="4ceb4-798">número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="4ceb4-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="4ceb4-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="4ceb4-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="4ceb4-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="4ceb4-800">permiso conducir</span></span>  <br/> <span data-ttu-id="4ceb4-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="4ceb4-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="4ceb4-802">el carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="4ceb4-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="4ceb4-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="4ceb4-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="4ceb4-804">스웨덴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="4ceb4-805">형식일</span><span class="sxs-lookup"><span data-stu-id="4ceb4-805">Format</span></span>

<span data-ttu-id="4ceb4-806">하이픈을 포함 하는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4ceb4-807">패턴</span><span class="sxs-lookup"><span data-stu-id="4ceb4-807">Pattern</span></span>

<span data-ttu-id="4ceb4-808">하이픈을 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="4ceb4-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="4ceb4-809">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-809">Six digits</span></span> 
    
- <span data-ttu-id="4ceb4-810">하이픈</span><span class="sxs-lookup"><span data-stu-id="4ceb4-810">A hyphen</span></span>
    
- <span data-ttu-id="4ceb4-811">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="4ceb4-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4ceb4-812">제외</span><span class="sxs-lookup"><span data-stu-id="4ceb4-812">Checksum</span></span>

<span data-ttu-id="4ceb4-813">아니요</span><span class="sxs-lookup"><span data-stu-id="4ceb4-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="4ceb4-814">정의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-814">Definition</span></span>

<span data-ttu-id="4ceb4-815">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4ceb4-816">정규식이 해당 `Regex_sweden_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4ceb4-817">from `Keywords_sweden_eu_driver's_license_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="4ceb4-818">키워드</span><span class="sxs-lookup"><span data-stu-id="4ceb4-818">Keywords</span></span>

<span data-ttu-id="4ceb4-819">| |</span><span class="sxs-lookup"><span data-stu-id="4ceb4-819"></span></span>
|<span data-ttu-id="4ceb4-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="4ceb4-821">dl</span><span class="sxs-lookup"><span data-stu-id="4ceb4-821">dl#</span></span>  <br/> <span data-ttu-id="4ceb4-822">driver license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-822">driver license</span></span>  <br/> <span data-ttu-id="4ceb4-823">드라이버 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-823">driver license number</span></span>  <br/> <span data-ttu-id="4ceb4-824">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="4ceb4-824">driver licence</span></span>  <br/> <span data-ttu-id="4ceb4-825">drivers lic</span><span class="sxs-lookup"><span data-stu-id="4ceb4-825">drivers lic.</span></span>  <br/> <span data-ttu-id="4ceb4-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-826">drivers license</span></span>  <br/> <span data-ttu-id="4ceb4-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="4ceb4-827">drivers licence</span></span>  <br/> <span data-ttu-id="4ceb4-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="4ceb4-828">driver's license</span></span>  <br/> <span data-ttu-id="4ceb4-829">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-829">driver's license number</span></span>  <br/> <span data-ttu-id="4ceb4-830">운전 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-830">driver's licence number</span></span>  <br/> <span data-ttu-id="4ceb4-831">운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="4ceb4-831">driving license number</span></span>  <br/> <span data-ttu-id="4ceb4-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="4ceb4-832">dlno#</span></span>  <br/> <span data-ttu-id="4ceb4-833">körkort</span><span class="sxs-lookup"><span data-stu-id="4ceb4-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="4ceb4-834">영국의</span><span class="sxs-lookup"><span data-stu-id="4ceb4-834">UK</span></span>

<span data-ttu-id="4ceb4-835">자세한 내용은 영국 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-835">For details, see the section "U.K.</span></span> <span data-ttu-id="4ceb4-836">[중요 한 정보 유형에 서 확인 되는](what-the-sensitive-information-types-look-for.md)운전 면허 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="4ceb4-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4ceb4-837">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4ceb4-837">See also</span></span>

[<span data-ttu-id="4ceb4-838">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="4ceb4-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

