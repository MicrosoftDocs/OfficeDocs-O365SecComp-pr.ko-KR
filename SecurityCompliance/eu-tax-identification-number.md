---
title: EU 세금 Id 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: f04919c8-2356-4de2-bb2a-b9f67f339726
description: 이 항목에서는 EU 세금 Id 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
ms.openlocfilehash: 5192496b393d15fd6d063e09c9bfe1cb3dd7e2dd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533472"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="7a19c-104">EU 세금 Id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-104">EU Tax Identification Number</span></span>

<span data-ttu-id="7a19c-p102">이 항목에서는 EU 세금 식별 번호 (주석) 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="7a19c-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="7a19c-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-108">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-108">Format</span></span>

<span data-ttu-id="7a19c-109">사용자 지정 하이픈 및 슬래시 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="7a19c-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-110">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-110">Pattern</span></span>

<span data-ttu-id="7a19c-111">사용자 지정 하이픈 및 슬래시 9 개의 숫자:</span><span class="sxs-lookup"><span data-stu-id="7a19c-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="7a19c-112">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-112">Two digits</span></span> 
    
- <span data-ttu-id="7a19c-113">하이픈 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="7a19c-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="7a19c-114">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-114">Three digits</span></span>
    
- <span data-ttu-id="7a19c-115">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="7a19c-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="7a19c-116">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-117">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-117">Checksum</span></span>

<span data-ttu-id="7a19c-118">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-119">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-119">Definition</span></span>

<span data-ttu-id="7a19c-120">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-121">다음은 함수 `Func_austria_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-122">키워드에서 `Keywords_austria_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-123">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-124">다음은 함수 `Func_austria_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
          <Match idRef="Keywords_austria_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-125">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="7a19c-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-127">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-127">tax number</span></span>
  
<span data-ttu-id="7a19c-128">번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-128">number</span></span>
  
<span data-ttu-id="7a19c-129">사업자 등록 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-129">tax registration number</span></span>
  
<span data-ttu-id="7a19c-130">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-130">tax id</span></span>
  
<span data-ttu-id="7a19c-131">st.nr 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-131">st.nr.</span></span>
  
<span data-ttu-id="7a19c-132">steuernummer</span><span class="sxs-lookup"><span data-stu-id="7a19c-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="7a19c-133">벨기에</span><span class="sxs-lookup"><span data-stu-id="7a19c-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-134">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-134">Format</span></span>

<span data-ttu-id="7a19c-135">공백 및 구분 기호 없이 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-136">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-136">Pattern</span></span>

<span data-ttu-id="7a19c-137">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="7a19c-137">11 digits:</span></span>
  
- <span data-ttu-id="7a19c-138">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-138">Two digits</span></span>
    
- <span data-ttu-id="7a19c-139">"0" 또는 "1"</span><span class="sxs-lookup"><span data-stu-id="7a19c-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="7a19c-140">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-140">One digit</span></span>
    
- <span data-ttu-id="7a19c-141">"0" 또는 "1" 또는 "2" 또는 "3"</span><span class="sxs-lookup"><span data-stu-id="7a19c-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="7a19c-142">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-143">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-143">Checksum</span></span>

<span data-ttu-id="7a19c-144">해당 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-145">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-145">Definition</span></span>

<span data-ttu-id="7a19c-146">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-147">정규식 `Regex_belgium_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-148">키워드에서 `Keywords_belgium_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-149">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="7a19c-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-151">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-151">tax number</span></span>
  
<span data-ttu-id="7a19c-152">국가 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-152">national registration number</span></span>
  
<span data-ttu-id="7a19c-153">사업자 등록 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-153">tax registration number</span></span>
  
<span data-ttu-id="7a19c-154">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-154">tax id</span></span>
  
<span data-ttu-id="7a19c-155">nif</span><span class="sxs-lookup"><span data-stu-id="7a19c-155">nif</span></span>
  
<span data-ttu-id="7a19c-156">nif #</span><span class="sxs-lookup"><span data-stu-id="7a19c-156">nif#</span></span>
  
<span data-ttu-id="7a19c-157">numéro de registre 국가</span><span class="sxs-lookup"><span data-stu-id="7a19c-157">numéro de registre national</span></span>
  
<span data-ttu-id="7a19c-158">numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="7a19c-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="7a19c-159">불가리아</span><span class="sxs-lookup"><span data-stu-id="7a19c-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-160">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-160">Format</span></span>

<span data-ttu-id="7a19c-161">공백 및 구분 기호 없이 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-162">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-162">Pattern</span></span>

<span data-ttu-id="7a19c-163">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a19c-164">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-164">Checksum</span></span>

<span data-ttu-id="7a19c-165">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-166">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-166">Definition</span></span>

<span data-ttu-id="7a19c-167">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-168">다음은 함수 `Func_bulgaria_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-169">키워드에서 `Keywords_bulgaria_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-170">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-171">다음은 함수 `Func_bulgaria_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
          <Match idRef="Keywords_bulgaria_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-172">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="7a19c-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-174">bucn</span><span class="sxs-lookup"><span data-stu-id="7a19c-174">bucn</span></span>
  
<span data-ttu-id="7a19c-175">uniform 복제 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-175">uniform civil number</span></span>
  
<span data-ttu-id="7a19c-176">bucn #</span><span class="sxs-lookup"><span data-stu-id="7a19c-176">bucn#</span></span>
  
<span data-ttu-id="7a19c-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="7a19c-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="7a19c-178">uniform 복제 id</span><span class="sxs-lookup"><span data-stu-id="7a19c-178">uniform civil id</span></span>
  
<span data-ttu-id="7a19c-179">uniform 복제 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-179">uniform civil no</span></span>
  
<span data-ttu-id="7a19c-180">egn</span><span class="sxs-lookup"><span data-stu-id="7a19c-180">egn</span></span>
  
<span data-ttu-id="7a19c-181">불가리아어 uniform 복제 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="7a19c-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-182">uniformcivilno#</span></span>
  
<span data-ttu-id="7a19c-183">egn #</span><span class="sxs-lookup"><span data-stu-id="7a19c-183">egn#</span></span>
  
<span data-ttu-id="7a19c-184">УНИФОРМ ГРАЖДАНСКИ НОМЕР</span><span class="sxs-lookup"><span data-stu-id="7a19c-184">униформ граждански номер</span></span>
  
<span data-ttu-id="7a19c-185">Униформ id</span><span class="sxs-lookup"><span data-stu-id="7a19c-185">униформ id</span></span>
  
<span data-ttu-id="7a19c-186">Униформ граждански id</span><span class="sxs-lookup"><span data-stu-id="7a19c-186">униформ граждански id</span></span>
  
<span data-ttu-id="7a19c-187">УНИФОРМ ГРАЖДАНСКИ НЕ</span><span class="sxs-lookup"><span data-stu-id="7a19c-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="7a19c-188">크로아티아</span><span class="sxs-lookup"><span data-stu-id="7a19c-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-189">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-189">Format</span></span>

<span data-ttu-id="7a19c-190">공백이 나 구분 기호 없이 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-191">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-191">Pattern</span></span>

<span data-ttu-id="7a19c-192">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="7a19c-192">11 digits:</span></span>
  
- <span data-ttu-id="7a19c-193">임의로 선택 하는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="7a19c-194">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-195">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-195">Checksum</span></span>

<span data-ttu-id="7a19c-196">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-197">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-197">Definition</span></span>

<span data-ttu-id="7a19c-198">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-199">다음은 함수 `Func_croatia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-200">키워드에서 `Keywords_croatia_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-201">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-202">다음은 함수 `Func_croatia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
          <Match idRef="Keywords_croatia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-203">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="7a19c-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-205">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-205">tax number</span></span>
  
<span data-ttu-id="7a19c-206">세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-206">tax</span></span>
  
<span data-ttu-id="7a19c-207">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-207">tax id</span></span>
  
<span data-ttu-id="7a19c-208">oid</span><span class="sxs-lookup"><span data-stu-id="7a19c-208">oid</span></span>
  
<span data-ttu-id="7a19c-209">oid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-209">oid#</span></span>
  
<span data-ttu-id="7a19c-210">porezni broj</span><span class="sxs-lookup"><span data-stu-id="7a19c-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="7a19c-211">키프로스</span><span class="sxs-lookup"><span data-stu-id="7a19c-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-212">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-212">Format</span></span>

<span data-ttu-id="7a19c-213">8 개의 숫자 및 지정된 된 패턴에 있는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="7a19c-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-214">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-214">Pattern</span></span>

<span data-ttu-id="7a19c-215">8 개의 숫자와 문자 하나:</span><span class="sxs-lookup"><span data-stu-id="7a19c-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="7a19c-216">"0"</span><span class="sxs-lookup"><span data-stu-id="7a19c-216">A "0"</span></span> 
    
- <span data-ttu-id="7a19c-217">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-217">Seven digits</span></span>
    
- <span data-ttu-id="7a19c-218">하나의 문자 (대 소문자 구분 안함)</span><span class="sxs-lookup"><span data-stu-id="7a19c-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-219">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-219">Checksum</span></span>

<span data-ttu-id="7a19c-220">해당 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-221">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-221">Definition</span></span>

<span data-ttu-id="7a19c-222">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-223">다음은 함수 `Func_cyprus_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-224">키워드에서 `Keywords_cyprus_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-225">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-226">다음은 함수 `Func_cyprus_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
          <Match idRef="Keywords_cyprus_eu_tax_file_number" />
        </Pattern>
Pattern confidenceLevel="75">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-227">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="7a19c-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-229">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-229">tax number</span></span>
  
<span data-ttu-id="7a19c-230">세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-230">tax</span></span>
  
<span data-ttu-id="7a19c-231">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-231">tax id</span></span>
  
<span data-ttu-id="7a19c-232">세금 id 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-232">tax identification code</span></span>
  
<span data-ttu-id="7a19c-233">눈금</span><span class="sxs-lookup"><span data-stu-id="7a19c-233">tic</span></span>
  
<span data-ttu-id="7a19c-234">눈금 #</span><span class="sxs-lookup"><span data-stu-id="7a19c-234">tic#</span></span>
  
<span data-ttu-id="7a19c-235">ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="7a19c-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="7a19c-236">ΦΟΡΟΛΟΓΙΚΉ ΤΑΥΤΌΤΗΤΑ</span><span class="sxs-lookup"><span data-stu-id="7a19c-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="7a19c-237">ΚΩΔΙΚΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="7a19c-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="7a19c-238">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="7a19c-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-239">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-239">Format</span></span>

<span data-ttu-id="7a19c-240">선택적 백슬래시를 9 또는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-241">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-241">Pattern</span></span>

<span data-ttu-id="7a19c-242">선택적 backslashl 9 또는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="7a19c-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="7a19c-243">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-243">Six digits</span></span> 
    
- <span data-ttu-id="7a19c-244">백슬래시 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="7a19c-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="7a19c-245">3 개 또는 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-246">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-246">Checksum</span></span>

<span data-ttu-id="7a19c-247">해당 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-248">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-248">Definition</span></span>

<span data-ttu-id="7a19c-249">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-250">정규식 `Regex_czech_republic_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-251">키워드에서 `Keywords_czech_republic_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-252">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="7a19c-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-254">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-254">tax number</span></span>
  
<span data-ttu-id="7a19c-255">세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-255">tax</span></span>
  
<span data-ttu-id="7a19c-256">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-256">tax id</span></span>
  
<span data-ttu-id="7a19c-257">개인 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-257">personal number</span></span>
  
<span data-ttu-id="7a19c-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="7a19c-258">daňové číslo</span></span>
  
<span data-ttu-id="7a19c-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="7a19c-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="7a19c-260">덴마크</span><span class="sxs-lookup"><span data-stu-id="7a19c-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-261">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-261">Format</span></span>

<span data-ttu-id="7a19c-262">하이픈을 포함 하는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-263">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-263">Pattern</span></span>

<span data-ttu-id="7a19c-264">10 자리 숫자를 hyphenl를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="7a19c-265">생일 (DDMMYY)에 해당 하는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="7a19c-266">하이픈</span><span class="sxs-lookup"><span data-stu-id="7a19c-266">A hyphen</span></span>
    
- <span data-ttu-id="7a19c-267">개인의 성별 (1 여자 2 남자 및 탑재에 대해서도 홀수)에 해당 하는 첫번째 숫자 생일 세기에 해당 하는 여기서 시퀀스 번호에 해당 하는 4 자리 숫자와 마지막 자릿수</span><span class="sxs-lookup"><span data-stu-id="7a19c-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-268">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-268">Checksum</span></span>

<span data-ttu-id="7a19c-269">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-270">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-270">Definition</span></span>

<span data-ttu-id="7a19c-271">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-272">다음은 함수 `Func_denmark_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-273">키워드에서 `Keywords_denmark_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-274">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-275">다음은 함수 `Func_denmark_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
          <Match idRef="Keywords_denmark_eu_tax_file_number" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-276">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="7a19c-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-278">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-278">tax number</span></span>
  
<span data-ttu-id="7a19c-279">세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-279">tax</span></span>
  
<span data-ttu-id="7a19c-280">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-280">tax id</span></span>
  
<span data-ttu-id="7a19c-281">cpr 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-281">cpr number</span></span>
  
<span data-ttu-id="7a19c-282">cpr #</span><span class="sxs-lookup"><span data-stu-id="7a19c-282">cpr#</span></span>
  
<span data-ttu-id="7a19c-283">skat nummer</span><span class="sxs-lookup"><span data-stu-id="7a19c-283">skat nummer</span></span>
  
<span data-ttu-id="7a19c-284">skat id</span><span class="sxs-lookup"><span data-stu-id="7a19c-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="7a19c-285">에스토니아</span><span class="sxs-lookup"><span data-stu-id="7a19c-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-286">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-286">Format</span></span>

<span data-ttu-id="7a19c-287">공백이 나 구분 기호 없이 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-288">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-288">Pattern</span></span>

<span data-ttu-id="7a19c-289">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="7a19c-289">11 digits:</span></span>
  
-  <span data-ttu-id="7a19c-290">성별 및 여기서 홀수인 1 여자 2 남자를 나타내고 짝수 나타냅니다 탑재 다음과 같이 생일 세기에 해당 하는 한 자리 숫자: 1, 2 19 세기;에 대 한 3, 4 20 세기;에 대 한 5, 6 21 세기에 대 한 및</span><span class="sxs-lookup"><span data-stu-id="7a19c-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="7a19c-291">생일 (YYMMDD)에 해당 하는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="7a19c-292">같은 날짜 태어난 장애인을 구분 하는 일련 번호에 해당 하는 세 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="7a19c-293">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-294">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-294">Checksum</span></span>

<span data-ttu-id="7a19c-295">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-296">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-296">Definition</span></span>

<span data-ttu-id="7a19c-297">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-298">다음은 함수 `Func_estonia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-299">키워드에서 `Keywords_estonia_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-300">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-301">다음은 함수 `Func_estonia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
          <Match idRef="Keywords_estonia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-302">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="7a19c-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-304">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-304">tax number</span></span>
  
<span data-ttu-id="7a19c-305">세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-305">tax</span></span>
  
<span data-ttu-id="7a19c-306">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-306">tax id</span></span>
  
<span data-ttu-id="7a19c-307">개인 코드</span><span class="sxs-lookup"><span data-stu-id="7a19c-307">personal code</span></span>
  
<span data-ttu-id="7a19c-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="7a19c-308">maksunumber</span></span>
  
<span data-ttu-id="7a19c-309">maksu id</span><span class="sxs-lookup"><span data-stu-id="7a19c-309">maksu id</span></span>
  
<span data-ttu-id="7a19c-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="7a19c-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="7a19c-311">핀란드</span><span class="sxs-lookup"><span data-stu-id="7a19c-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-312">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-312">Format</span></span>

<span data-ttu-id="7a19c-313">숫자는 11 자리의 조합 문자 및 더하기 및 빼기 기호</span><span class="sxs-lookup"><span data-stu-id="7a19c-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-314">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-314">Pattern</span></span>

<span data-ttu-id="7a19c-315">숫자는 11 자리의 조합 문자 및 더하기 및 빼기 기호:</span><span class="sxs-lookup"><span data-stu-id="7a19c-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="7a19c-316">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-316">Six digits</span></span>
    
- <span data-ttu-id="7a19c-317">다음 중 하나: 더하기 기호, 빼기 기호 또는 더하기 기호를 의미 있는 문자 "A" (하지 대/소문자 구분) 1800-1899 년 사이 태어난 빼기 서명 간의 태어난 의미 1900-1999 및 "A" 2000 탄생 하 게 하는 방법 및 완료</span><span class="sxs-lookup"><span data-stu-id="7a19c-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="7a19c-318">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-318">Three digits</span></span>
    
- <span data-ttu-id="7a19c-319">하나의 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-320">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-320">Checksum</span></span>

<span data-ttu-id="7a19c-321">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-322">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-322">Definition</span></span>

<span data-ttu-id="7a19c-323">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-324">다음은 함수 `Func_finland_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-325">키워드에서 `Keywords_finland_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-326">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-327">다음은 함수 `Func_finland_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
          <Match idRef="Keywords_finland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-328">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="7a19c-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-330">identification number
</span><span class="sxs-lookup"><span data-stu-id="7a19c-330">identification number</span></span>
  
<span data-ttu-id="7a19c-331">개인 id</span><span class="sxs-lookup"><span data-stu-id="7a19c-331">personal id</span></span>
  
<span data-ttu-id="7a19c-332">identity 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-332">identity number</span></span>
  
<span data-ttu-id="7a19c-333">핀란드 국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-333">finnish national id number</span></span>
  
<span data-ttu-id="7a19c-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="7a19c-334">personalidnumber#</span></span>
  
<span data-ttu-id="7a19c-335">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-335">national identification number</span></span>
  
<span data-ttu-id="7a19c-336">id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-336">id number</span></span>
  
<span data-ttu-id="7a19c-337">국가 id 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-337">national id no.</span></span>
  
<span data-ttu-id="7a19c-338">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-338">national id number</span></span>
  
<span data-ttu-id="7a19c-339">id 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-339">id no</span></span>
  
<span data-ttu-id="7a19c-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="7a19c-340">tunnistenumero</span></span>
  
<span data-ttu-id="7a19c-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="7a19c-341">henkilötunnus</span></span>
  
<span data-ttu-id="7a19c-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="7a19c-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="7a19c-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="7a19c-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="7a19c-344">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="7a19c-344">identiteetti numero</span></span>
  
<span data-ttu-id="7a19c-345">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="7a19c-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="7a19c-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="7a19c-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="7a19c-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="7a19c-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="7a19c-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="7a19c-348">tunnusnumero</span></span>
  
<span data-ttu-id="7a19c-349">kansallinen tunnus numero</span><span class="sxs-lookup"><span data-stu-id="7a19c-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="7a19c-350">프랑스</span><span class="sxs-lookup"><span data-stu-id="7a19c-350">France</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-351">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-351">Format</span></span>

<span data-ttu-id="7a19c-352">개인 및 엔터티에 대 한 숫자 9 개에 대 한 13 자릿수</span><span class="sxs-lookup"><span data-stu-id="7a19c-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-353">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-353">Pattern</span></span>

<span data-ttu-id="7a19c-354">개별 사용자에 대 한 자리 숫자 13:</span><span class="sxs-lookup"><span data-stu-id="7a19c-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="7a19c-355">0, 1, 2 또는 3 이어야 하는 한 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="7a19c-356">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-356">12 digits</span></span>
    
<span data-ttu-id="7a19c-357">엔터티에 대 한 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="7a19c-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a19c-358">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-358">Checksum</span></span>

<span data-ttu-id="7a19c-359">해당 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-360">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-360">Definition</span></span>

<span data-ttu-id="7a19c-361">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-362">다음은 함수 `Func_france_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-363">키워드에서 `Keywords_france_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-364">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-365">다음은 함수 `Func_france_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
          <Match idRef="Keywords_france_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-366">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="7a19c-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-368">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-368">tax identification number</span></span>
  
<span data-ttu-id="7a19c-369">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-369">tax number</span></span>
  
<span data-ttu-id="7a19c-370">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-370">tax id</span></span>
  
<span data-ttu-id="7a19c-371">numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="7a19c-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="7a19c-372">독일</span><span class="sxs-lookup"><span data-stu-id="7a19c-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-373">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-373">Format</span></span>

<span data-ttu-id="7a19c-374">공백 및 구분 기호 없이 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-375">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-375">Pattern</span></span>

<span data-ttu-id="7a19c-376">11 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="7a19c-376">11 digits :</span></span>
  
-  <span data-ttu-id="7a19c-377">10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-377">Ten digits</span></span> 
    
- <span data-ttu-id="7a19c-378">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-379">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-379">Checksum</span></span>

<span data-ttu-id="7a19c-380">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-381">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-381">Definition</span></span>

<span data-ttu-id="7a19c-382">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-383">다음은 함수 `Func_germany_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-384">키워드에서 `Keywords_germany_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-385">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-386">다음은 함수 `Func_germany_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
          <Match idRef="Keywords_germany_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-387">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="7a19c-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-389">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-389">tax number</span></span>
  
<span data-ttu-id="7a19c-390">no를 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-390">tax no.</span></span>
  
<span data-ttu-id="7a19c-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-391">taxno#</span></span>
  
<span data-ttu-id="7a19c-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="7a19c-392">taxnumber#</span></span>
  
<span data-ttu-id="7a19c-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="7a19c-393">taxnumber</span></span>
  
<span data-ttu-id="7a19c-394">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-394">tax id</span></span>
  
<span data-ttu-id="7a19c-395">taxid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-395">taxid#</span></span>
  
<span data-ttu-id="7a19c-396">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-396">tax identification number</span></span>
  
<span data-ttu-id="7a19c-397">식별을 더 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-397">tax identification no.</span></span>
  
<span data-ttu-id="7a19c-398">steuernummer</span><span class="sxs-lookup"><span data-stu-id="7a19c-398">steuernummer</span></span>
  
<span data-ttu-id="7a19c-399">steuer id</span><span class="sxs-lookup"><span data-stu-id="7a19c-399">steuer id</span></span>
  
<span data-ttu-id="7a19c-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="7a19c-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="7a19c-401">그리스</span><span class="sxs-lookup"><span data-stu-id="7a19c-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-402">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-402">Format</span></span>

<span data-ttu-id="7a19c-403">공백 및 구분 기호 없이 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="7a19c-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-404">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-404">Pattern</span></span>

<span data-ttu-id="7a19c-405">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a19c-406">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-406">Checksum</span></span>

<span data-ttu-id="7a19c-407">해당 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-408">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-408">Definition</span></span>

<span data-ttu-id="7a19c-409">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-410">정규식 `Regex_greece_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-411">키워드에서 `Keywords_greece_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-412">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="7a19c-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-414">afm</span><span class="sxs-lookup"><span data-stu-id="7a19c-414">afm</span></span>
  
<span data-ttu-id="7a19c-415">tin
</span><span class="sxs-lookup"><span data-stu-id="7a19c-415">tin</span></span>
  
<span data-ttu-id="7a19c-416">id를 더 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-416">tax id no.</span></span>
  
<span data-ttu-id="7a19c-417">id를 더 세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-417">tax id no</span></span>
  
<span data-ttu-id="7a19c-418">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-418">tax identification number</span></span>
  
<span data-ttu-id="7a19c-419">세금 레지스트리 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-419">tax registry number</span></span>
  
<span data-ttu-id="7a19c-420">레지스트리를 더 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-420">tax registry no.</span></span>
  
<span data-ttu-id="7a19c-421">afm #</span><span class="sxs-lookup"><span data-stu-id="7a19c-421">afm#</span></span>
  
<span data-ttu-id="7a19c-422">주석 #</span><span class="sxs-lookup"><span data-stu-id="7a19c-422">tin#</span></span>
  
<span data-ttu-id="7a19c-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-423">taxidno#</span></span>
  
<span data-ttu-id="7a19c-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-424">taxregistryno#</span></span>
  
<span data-ttu-id="7a19c-425">ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="7a19c-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="7a19c-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="7a19c-426">aφμ</span></span>
  
<span data-ttu-id="7a19c-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="7a19c-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="7a19c-428">ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ ΝΟ 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="7a19c-429">ΤΟΝ ΑΡΙΘΜΌ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="7a19c-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="7a19c-430">헝가리</span><span class="sxs-lookup"><span data-stu-id="7a19c-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-431">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-431">Format</span></span>

<span data-ttu-id="7a19c-432">공백이 나 구분 기호 없이 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-433">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-433">Pattern</span></span>

<span data-ttu-id="7a19c-434">10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="7a19c-434">Ten digits:</span></span>
  
-  <span data-ttu-id="7a19c-435">"8" 되어야 하는 한 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="7a19c-436">날짜 사이의 일 수에 해당 하는 5 자리 01/01/1867 및 개인의 생일의 날짜</span><span class="sxs-lookup"><span data-stu-id="7a19c-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="7a19c-437">하루에 탄생 하 게 하는 개인을 구분 하기 위해 우연히 생성 번호에 해당 하는 세 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="7a19c-438">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-439">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-439">Checksum</span></span>

<span data-ttu-id="7a19c-440">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-441">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-441">Definition</span></span>

<span data-ttu-id="7a19c-442">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-443">다음은 함수 `Func_hungary_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-444">키워드에서 `Keywords_hungary_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-445">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-446">다음은 함수 `Func_hungary_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
          <Match idRef="Keywords_hungary_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-447">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="7a19c-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-449">헝가리어 세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="7a19c-450">헝가리어 주석</span><span class="sxs-lookup"><span data-stu-id="7a19c-450">hungarian tin</span></span>
  
<span data-ttu-id="7a19c-451">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-451">tax id number</span></span>
  
<span data-ttu-id="7a19c-452">vat 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-452">vat number</span></span>
  
<span data-ttu-id="7a19c-453">인증 기관을 더 세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-453">tax authority no</span></span>
  
<span data-ttu-id="7a19c-454">세금 id 세금 identity 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-454">tax id tax identity number</span></span>
  
<span data-ttu-id="7a19c-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="7a19c-455">taxidnumber#</span></span>
  
<span data-ttu-id="7a19c-456">주석 #</span><span class="sxs-lookup"><span data-stu-id="7a19c-456">tin#</span></span>
  
<span data-ttu-id="7a19c-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="7a19c-457">hungatiantin#</span></span>
  
<span data-ttu-id="7a19c-458">식별을 더 세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-458">tax identification no</span></span>
  
<span data-ttu-id="7a19c-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-459">taxidno#</span></span>
  
<span data-ttu-id="7a19c-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="7a19c-460">adóazonosító szám</span></span>
  
<span data-ttu-id="7a19c-461">adószám</span><span class="sxs-lookup"><span data-stu-id="7a19c-461">adószám</span></span>
  
<span data-ttu-id="7a19c-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="7a19c-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="7a19c-463">Ireland</span><span class="sxs-lookup"><span data-stu-id="7a19c-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-464">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-464">Format</span></span>

<span data-ttu-id="7a19c-465">공백이 나 구분 기호 없이 문자 앞에 오는 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-466">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-466">Pattern</span></span>

<span data-ttu-id="7a19c-467">7 자리 숫자 앞에 오는 문자를:</span><span class="sxs-lookup"><span data-stu-id="7a19c-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="7a19c-468">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-468">Seven digits</span></span> 
    
- <span data-ttu-id="7a19c-469">하나의 문자 (대 소문자 구분 안함)</span><span class="sxs-lookup"><span data-stu-id="7a19c-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-470">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-470">Checksum</span></span>

<span data-ttu-id="7a19c-471">해당 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-472">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-472">Definition</span></span>

<span data-ttu-id="7a19c-473">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-474">다음은 함수 `Func_ireland_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-475">키워드에서 `Keywords_ireland_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-476">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-477">다음은 함수 `Func_ireland_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
          <Match idRef="Keywords_ireland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-478">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="7a19c-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-480">공공 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-480">public service no</span></span>
  
<span data-ttu-id="7a19c-481">개인 공공 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-481">personal public service no</span></span>
  
<span data-ttu-id="7a19c-482">pps 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-482">pps no</span></span>
  
<span data-ttu-id="7a19c-483">개인 no 서비스</span><span class="sxs-lookup"><span data-stu-id="7a19c-483">personal service no</span></span>
  
<span data-ttu-id="7a19c-484">pps 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-484">pps service no</span></span>
  
<span data-ttu-id="7a19c-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-485">ppsno#</span></span>
  
<span data-ttu-id="7a19c-486">아일랜드 pps 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-486">irish pps no</span></span>
  
<span data-ttu-id="7a19c-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-487">publicserviceno#</span></span>
  
<span data-ttu-id="7a19c-488">개인 공공 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-488">personal public service number</span></span>
  
<span data-ttu-id="7a19c-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="7a19c-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="7a19c-490">pps uimh</span><span class="sxs-lookup"><span data-stu-id="7a19c-490">pps uimh</span></span>
  
<span data-ttu-id="7a19c-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="7a19c-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="7a19c-492">이탈리아</span><span class="sxs-lookup"><span data-stu-id="7a19c-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-493">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-493">Format</span></span>

<span data-ttu-id="7a19c-494">16 비트 문자 및 지정 된 패턴의 자릿수</span><span class="sxs-lookup"><span data-stu-id="7a19c-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-495">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-495">Pattern</span></span>

<span data-ttu-id="7a19c-496">16 대 문자와 숫자:</span><span class="sxs-lookup"><span data-stu-id="7a19c-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="7a19c-497">패밀리 이름에서 처음 세 자음에 해당 하는 세 개 문자</span><span class="sxs-lookup"><span data-stu-id="7a19c-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="7a19c-498">먼저, 세번째 및 네번째에 해당 하는 세 글자로 자음 첫 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="7a19c-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="7a19c-499">마지막 생일의 연도의 숫자에 해당 하는 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="7a19c-500">생일의 월에 해당 하는 한 자리 숫자-문자 사전순으로 사용 되지만 문자를 E, H, L, M, P, R T로 사용 됩니다 (따라서 1 월 A 이며 년 10 월 R)</span><span class="sxs-lookup"><span data-stu-id="7a19c-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="7a19c-501">40 수 컷 구별 하기 위해 산포도 대 한 생일 요일에 추가 되는 여기서 생일의 월의 날짜에 해당 하는 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="7a19c-502">사용자 출생 여기서는 지방 자치 단체에 특정 지역 번호에 해당 하는 4 자리 숫자-외국에 사용 되는 전체 국가 코드</span><span class="sxs-lookup"><span data-stu-id="7a19c-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="7a19c-503">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-504">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-504">Checksum</span></span>

<span data-ttu-id="7a19c-505">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-506">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-506">Definition</span></span>

<span data-ttu-id="7a19c-507">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-508">다음은 함수 `Func_italy_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-509">키워드에서 `Keywords_italy_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-510">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-511">다음은 함수 `Func_italy_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
          <Match idRef="Keywords_italy_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-512">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="7a19c-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-514">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-514">tax number</span></span>
  
<span data-ttu-id="7a19c-515">no를 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-515">tax no.</span></span>
  
<span data-ttu-id="7a19c-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-516">taxno#</span></span>
  
<span data-ttu-id="7a19c-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="7a19c-517">taxnumber#</span></span>
  
<span data-ttu-id="7a19c-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="7a19c-518">taxnumber</span></span>
  
<span data-ttu-id="7a19c-519">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-519">tax id</span></span>
  
<span data-ttu-id="7a19c-520">taxid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-520">taxid#</span></span>
  
<span data-ttu-id="7a19c-521">회계 코드</span><span class="sxs-lookup"><span data-stu-id="7a19c-521">fiscal code</span></span>
  
<span data-ttu-id="7a19c-522">codice fiscale</span><span class="sxs-lookup"><span data-stu-id="7a19c-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="7a19c-523">라트비아</span><span class="sxs-lookup"><span data-stu-id="7a19c-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-524">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-524">Format</span></span>

<span data-ttu-id="7a19c-525">공백이 나 구분 기호 없이 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-526">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-526">Pattern</span></span>

<span data-ttu-id="7a19c-527">지정된 된 패턴에 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="7a19c-528">생일 (DDMMYY)의 날짜에 해당 하는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="7a19c-529">여기서 19 세기에 해당 하는 "0", "1" 해당 20 세기에 "2" 하 고 해당 21 세기 생일 세기에 해당 하는 한 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="7a19c-530">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-531">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-531">Checksum</span></span>

<span data-ttu-id="7a19c-532">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-533">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-533">Definition</span></span>

<span data-ttu-id="7a19c-534">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-535">다음은 함수 `Func_latvia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-536">키워드에서 `Keywords_latvia_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-537">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-538">다음은 함수 `Func_latvia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
          <Match idRef="Keywords_latvia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-539">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="7a19c-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-541">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-541">tax number</span></span>
  
<span data-ttu-id="7a19c-542">no를 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-542">tax no.</span></span>
  
<span data-ttu-id="7a19c-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-543">taxno#</span></span>
  
<span data-ttu-id="7a19c-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="7a19c-544">taxnumber#</span></span>
  
<span data-ttu-id="7a19c-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="7a19c-545">taxnumber</span></span>
  
<span data-ttu-id="7a19c-546">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-546">tax id</span></span>
  
<span data-ttu-id="7a19c-547">taxid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-547">taxid#</span></span>
  
<span data-ttu-id="7a19c-548">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-548">tax identification number</span></span>
  
<span data-ttu-id="7a19c-549">식별을 더 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-549">tax identification no.</span></span>
  
<span data-ttu-id="7a19c-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="7a19c-550">nodokļa numurs</span></span>
  
<span data-ttu-id="7a19c-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="7a19c-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="7a19c-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="7a19c-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="7a19c-553">리투아니아</span><span class="sxs-lookup"><span data-stu-id="7a19c-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-554">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-554">Format</span></span>

<span data-ttu-id="7a19c-555">공백이 나 구분 기호 없이 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-556">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-556">Pattern</span></span>

<span data-ttu-id="7a19c-557">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a19c-558">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-558">Checksum</span></span>

<span data-ttu-id="7a19c-559">해당 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-560">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-560">Definition</span></span>

<span data-ttu-id="7a19c-561">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-562">다음은 함수 `Func_lithuania_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-563">키워드에서 `Keywords_lithuania_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-564">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-565">다음은 함수 `Func_lithuania_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
          <Match idRef="Keywords_lithuania_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-566">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="7a19c-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-568">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-568">tax number</span></span>
  
<span data-ttu-id="7a19c-569">no를 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-569">tax no.</span></span>
  
<span data-ttu-id="7a19c-570">세금 no #</span><span class="sxs-lookup"><span data-stu-id="7a19c-570">tax no#</span></span>
  
<span data-ttu-id="7a19c-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="7a19c-571">taxnumber#</span></span>
  
<span data-ttu-id="7a19c-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="7a19c-572">taxnumber</span></span>
  
<span data-ttu-id="7a19c-573">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-573">tax id</span></span>
  
<span data-ttu-id="7a19c-574">taxid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-574">taxid#</span></span>
  
<span data-ttu-id="7a19c-575">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-575">tax identification number</span></span>
  
<span data-ttu-id="7a19c-576">식별을 더 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-576">tax identification no.</span></span>
  
<span data-ttu-id="7a19c-577">mokesčių id</span><span class="sxs-lookup"><span data-stu-id="7a19c-577">mokesčių id</span></span>
  
<span data-ttu-id="7a19c-578">mokesčių numeris</span><span class="sxs-lookup"><span data-stu-id="7a19c-578">mokesčių numeris</span></span>
  
<span data-ttu-id="7a19c-579">mokesčių identifikavimas numeris</span><span class="sxs-lookup"><span data-stu-id="7a19c-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="7a19c-580">룩셈부르크</span><span class="sxs-lookup"><span data-stu-id="7a19c-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-581">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-581">Format</span></span>

<span data-ttu-id="7a19c-582">공백이 나 구분 기호 없이 13 자릿수</span><span class="sxs-lookup"><span data-stu-id="7a19c-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-583">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-583">Pattern</span></span>

<span data-ttu-id="7a19c-584">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="7a19c-584">13 digits:</span></span>
  
-  <span data-ttu-id="7a19c-585">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-585">11 digits</span></span> 
    
- <span data-ttu-id="7a19c-586">2개의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-587">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-587">Checksum</span></span>

<span data-ttu-id="7a19c-588">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-589">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-589">Definition</span></span>

<span data-ttu-id="7a19c-590">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-591">다음은 함수 `Func_luxemburg_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-592">키워드에서 `Keywords_luxemburg_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-593">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-594">다음은 함수 `Func_luxemburg_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
          <Match idRef="Keywords_luxemburg_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-595">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="7a19c-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-597">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-597">tax number</span></span>
  
<span data-ttu-id="7a19c-598">no를 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-598">tax no.</span></span>
  
<span data-ttu-id="7a19c-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-599">taxno#</span></span>
  
<span data-ttu-id="7a19c-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="7a19c-600">taxnumber#</span></span>
  
<span data-ttu-id="7a19c-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="7a19c-601">taxnumber</span></span>
  
<span data-ttu-id="7a19c-602">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-602">tax id</span></span>
  
<span data-ttu-id="7a19c-603">taxid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-603">taxid#</span></span>
  
<span data-ttu-id="7a19c-604">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-604">tax identification number</span></span>
  
<span data-ttu-id="7a19c-605">식별을 더 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-605">tax identification no.</span></span>
  
<span data-ttu-id="7a19c-606">steuernummer</span><span class="sxs-lookup"><span data-stu-id="7a19c-606">steuernummer</span></span>
  
<span data-ttu-id="7a19c-607">steuer id</span><span class="sxs-lookup"><span data-stu-id="7a19c-607">steuer id</span></span>
  
<span data-ttu-id="7a19c-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="7a19c-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="7a19c-609">몰타</span><span class="sxs-lookup"><span data-stu-id="7a19c-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-610">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-610">Format</span></span>

<span data-ttu-id="7a19c-611">몰타어 국민에 대 한: 7 자리 숫자 및 지정된 된 패턴에 있는 문자 하나</span><span class="sxs-lookup"><span data-stu-id="7a19c-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="7a19c-612">비 몰타어 국민 및 몰타어 엔터티: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-613">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-613">Pattern</span></span>

<span data-ttu-id="7a19c-614">몰타어 국민: 7 자리 숫자와 문자 하나</span><span class="sxs-lookup"><span data-stu-id="7a19c-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="7a19c-615">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-615">Seven digits</span></span> 
    
- <span data-ttu-id="7a19c-616">하나의 문자 (대 소문자 구분 안함)</span><span class="sxs-lookup"><span data-stu-id="7a19c-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="7a19c-617">비 몰타어 국민 및 몰타어 엔터티: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="7a19c-618">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="7a19c-619">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-619">Checksum</span></span>

<span data-ttu-id="7a19c-620">해당 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-621">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-621">Definition</span></span>

<span data-ttu-id="7a19c-622">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-623">다음은 함수 `Func_malta_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-624">키워드에서 `Keywords_malta_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-625">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-626">다음은 함수 `Func_malta_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_malta_eu_tax_file_number" />
          <Match idRef="Keywords_malta_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-627">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="7a19c-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-629">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-629">tax number</span></span>
  
<span data-ttu-id="7a19c-630">no를 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-630">tax no.</span></span>
  
<span data-ttu-id="7a19c-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-631">taxno#</span></span>
  
<span data-ttu-id="7a19c-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="7a19c-632">taxnumber#</span></span>
  
<span data-ttu-id="7a19c-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="7a19c-633">taxnumber</span></span>
  
<span data-ttu-id="7a19c-634">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-634">tax id</span></span>
  
<span data-ttu-id="7a19c-635">taxid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-635">taxid#</span></span>
  
<span data-ttu-id="7a19c-636">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-636">tax identification number</span></span>
  
<span data-ttu-id="7a19c-637">식별을 더 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-637">tax identification no.</span></span>
  
<span data-ttu-id="7a19c-638">numru tat taxxa</span><span class="sxs-lookup"><span data-stu-id="7a19c-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="7a19c-639">id tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="7a19c-639">id tat-taxxa</span></span>
  
<span data-ttu-id="7a19c-640">numru ta ' identifikazzjoni tat taxxa</span><span class="sxs-lookup"><span data-stu-id="7a19c-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="7a19c-641">네덜란드</span><span class="sxs-lookup"><span data-stu-id="7a19c-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-642">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-642">Format</span></span>

<span data-ttu-id="7a19c-643">공백이 나 구분 기호 없이 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="7a19c-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-644">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-644">Pattern</span></span>

<span data-ttu-id="7a19c-645">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="7a19c-646">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-646">Checksum</span></span>

<span data-ttu-id="7a19c-647">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-648">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-648">Definition</span></span>

<span data-ttu-id="7a19c-649">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-650">다음은 함수 `Func_netherlands_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-651">키워드에서 `Keywords_netherlands_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-652">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-653">다음은 함수 `Func_netherlands_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
          <Match idRef="Keywords_netherlands_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-654">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="7a19c-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-656">네덜란드 세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="7a19c-657">네덜란드 세금 식별</span><span class="sxs-lookup"><span data-stu-id="7a19c-657">netherlands tax identification</span></span>
  
<span data-ttu-id="7a19c-658">네덜란드령의 세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="7a19c-659">네덜란드령의 세금 식별</span><span class="sxs-lookup"><span data-stu-id="7a19c-659">netherland's tax identification</span></span>
  
<span data-ttu-id="7a19c-660">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-660">tax identification number</span></span>
  
<span data-ttu-id="7a19c-661">네덜란드어 세금 id</span><span class="sxs-lookup"><span data-stu-id="7a19c-661">dutch tax id</span></span>
  
<span data-ttu-id="7a19c-662">네덜란드어 세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-662">dutch tax identification number</span></span>
  
<span data-ttu-id="7a19c-663">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-663">tax id</span></span>
  
<span data-ttu-id="7a19c-664">세금 id #</span><span class="sxs-lookup"><span data-stu-id="7a19c-664">tax id#</span></span>
  
<span data-ttu-id="7a19c-665">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-665">tax number</span></span>
  
<span data-ttu-id="7a19c-666">세금 no #</span><span class="sxs-lookup"><span data-stu-id="7a19c-666">tax no#</span></span>
  
<span data-ttu-id="7a19c-667">세금 #</span><span class="sxs-lookup"><span data-stu-id="7a19c-667">tax#</span></span>
  
<span data-ttu-id="7a19c-668">tin
</span><span class="sxs-lookup"><span data-stu-id="7a19c-668">tin</span></span>
  
<span data-ttu-id="7a19c-669">주석 #</span><span class="sxs-lookup"><span data-stu-id="7a19c-669">tin#</span></span>
  
<span data-ttu-id="7a19c-670">네덜란드 주석</span><span class="sxs-lookup"><span data-stu-id="7a19c-670">netherlands tin</span></span>
  
<span data-ttu-id="7a19c-671">네덜란드령의 주석</span><span class="sxs-lookup"><span data-stu-id="7a19c-671">netherland's tin</span></span>
  
<span data-ttu-id="7a19c-672">네덜란드 belasting identificatienummer</span><span class="sxs-lookup"><span data-stu-id="7a19c-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="7a19c-673">identificatienummer van belasting</span><span class="sxs-lookup"><span data-stu-id="7a19c-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="7a19c-674">identificatienummer belasting</span><span class="sxs-lookup"><span data-stu-id="7a19c-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="7a19c-675">네덜란드 belasting identificatie</span><span class="sxs-lookup"><span data-stu-id="7a19c-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="7a19c-676">네덜란드 belasting id nummer</span><span class="sxs-lookup"><span data-stu-id="7a19c-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="7a19c-677">네덜란드 belastingnummer</span><span class="sxs-lookup"><span data-stu-id="7a19c-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="7a19c-678">btw nummer</span><span class="sxs-lookup"><span data-stu-id="7a19c-678">btw nummer</span></span>
  
<span data-ttu-id="7a19c-679">nederlandse belasting identificatie</span><span class="sxs-lookup"><span data-stu-id="7a19c-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="7a19c-680">폴란드</span><span class="sxs-lookup"><span data-stu-id="7a19c-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-681">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-681">Format</span></span>

<span data-ttu-id="7a19c-682">공백이 나 구분 기호 없이 11 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-683">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-683">Pattern</span></span>

<span data-ttu-id="7a19c-684">11 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a19c-685">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-685">Checksum</span></span>

<span data-ttu-id="7a19c-686">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-687">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-687">Definition</span></span>

<span data-ttu-id="7a19c-688">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-689">다음은 함수 `Func_poland_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-690">키워드에서 `Keywords_poland_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-691">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-692">다음은 함수 `Func_poland_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
          <Match idRef="Keywords_poland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-693">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="7a19c-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-695">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-695">tax number</span></span>
  
<span data-ttu-id="7a19c-696">no를 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-696">tax no.</span></span>
  
<span data-ttu-id="7a19c-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-697">taxno#</span></span>
  
<span data-ttu-id="7a19c-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="7a19c-698">taxnumber#</span></span>
  
<span data-ttu-id="7a19c-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="7a19c-699">taxnumber</span></span>
  
<span data-ttu-id="7a19c-700">닙 (nip)</span><span class="sxs-lookup"><span data-stu-id="7a19c-700">nip</span></span>
  
<span data-ttu-id="7a19c-701">닙 (nip) #</span><span class="sxs-lookup"><span data-stu-id="7a19c-701">nip#</span></span>
  
<span data-ttu-id="7a19c-702">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-702">tax id</span></span>
  
<span data-ttu-id="7a19c-703">세금 id #</span><span class="sxs-lookup"><span data-stu-id="7a19c-703">tax id#</span></span>
  
<span data-ttu-id="7a19c-704">닙 (nip) id</span><span class="sxs-lookup"><span data-stu-id="7a19c-704">nip id</span></span>
  
<span data-ttu-id="7a19c-705">닙 (nip) id #</span><span class="sxs-lookup"><span data-stu-id="7a19c-705">nip id#</span></span>
  
<span data-ttu-id="7a19c-706">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-706">tax identification number</span></span>
  
<span data-ttu-id="7a19c-707">식별을 더 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-707">tax identification no.</span></span>
  
<span data-ttu-id="7a19c-708">vat 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-708">vat number</span></span>
  
<span data-ttu-id="7a19c-709">no를 vat 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-709">vat no.</span></span>
  
<span data-ttu-id="7a19c-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-710">vatno#</span></span>
  
<span data-ttu-id="7a19c-711">vat id</span><span class="sxs-lookup"><span data-stu-id="7a19c-711">vat id</span></span>
  
<span data-ttu-id="7a19c-712">vat id #</span><span class="sxs-lookup"><span data-stu-id="7a19c-712">vat id#</span></span>
  
<span data-ttu-id="7a19c-713">u r identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="7a19c-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="7a19c-714">polski u r identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="7a19c-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="7a19c-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="7a19c-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="7a19c-716">포르투갈</span><span class="sxs-lookup"><span data-stu-id="7a19c-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-717">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-717">Format</span></span>

<span data-ttu-id="7a19c-718">공백이 나 구분 기호 없이 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="7a19c-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-719">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-719">Pattern</span></span>

<span data-ttu-id="7a19c-720">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a19c-721">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-721">Checksum</span></span>

<span data-ttu-id="7a19c-722">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-723">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-723">Definition</span></span>

<span data-ttu-id="7a19c-724">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-725">다음은 함수 `Func_portugal_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-726">키워드에서 `Keywords_portugal_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-727">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-728">다음은 함수 `Func_portugal_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
          <Match idRef="Keywords_portugal_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-729">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="7a19c-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-731">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-731">tax number</span></span>
  
<span data-ttu-id="7a19c-732">no를 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-732">tax no.</span></span>
  
<span data-ttu-id="7a19c-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-733">taxno#</span></span>
  
<span data-ttu-id="7a19c-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="7a19c-734">taxnumber#</span></span>
  
<span data-ttu-id="7a19c-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="7a19c-735">taxnumber</span></span>
  
<span data-ttu-id="7a19c-736">nif</span><span class="sxs-lookup"><span data-stu-id="7a19c-736">nif</span></span>
  
<span data-ttu-id="7a19c-737">nif #</span><span class="sxs-lookup"><span data-stu-id="7a19c-737">nif#</span></span>
  
<span data-ttu-id="7a19c-738">회계 numero</span><span class="sxs-lookup"><span data-stu-id="7a19c-738">numero fiscal</span></span>
  
<span data-ttu-id="7a19c-739">회계 número de identificação</span><span class="sxs-lookup"><span data-stu-id="7a19c-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="7a19c-740">루마니아</span><span class="sxs-lookup"><span data-stu-id="7a19c-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-741">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-741">Format</span></span>

<span data-ttu-id="7a19c-742">공백이 나 구분 기호 없이 13 자릿수</span><span class="sxs-lookup"><span data-stu-id="7a19c-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-743">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-743">Pattern</span></span>

<span data-ttu-id="7a19c-744">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a19c-745">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-745">Checksum</span></span>

<span data-ttu-id="7a19c-746">해당 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-747">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-747">Definition</span></span>

<span data-ttu-id="7a19c-748">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-749">정규식 `Regex_romania_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-750">키워드에서 `Keywords_romania_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-751">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="7a19c-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-753">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-753">tax id</span></span>
  
<span data-ttu-id="7a19c-754">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-754">tax id number</span></span>
  
<span data-ttu-id="7a19c-755">파일을 더 세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-755">tax file no</span></span>
  
<span data-ttu-id="7a19c-756">

tax file number</span><span class="sxs-lookup"><span data-stu-id="7a19c-756">tax file number</span></span>
  
<span data-ttu-id="7a19c-757">no 세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-757">tax no</span></span>
  
<span data-ttu-id="7a19c-758">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-758">tax number</span></span>
  
<span data-ttu-id="7a19c-759">taxid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-759">taxid#</span></span>
  
<span data-ttu-id="7a19c-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-760">taxno#</span></span>
  
<span data-ttu-id="7a19c-761">id ul taxei</span><span class="sxs-lookup"><span data-stu-id="7a19c-761">id-ul taxei</span></span>
  
<span data-ttu-id="7a19c-762">numărul de identificare fiscală</span><span class="sxs-lookup"><span data-stu-id="7a19c-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="7a19c-763">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="7a19c-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-764">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-764">Format</span></span>

<span data-ttu-id="7a19c-765">공백이 나 구분 기호 없이 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-766">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-766">Pattern</span></span>

<span data-ttu-id="7a19c-767">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a19c-768">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-768">Checksum</span></span>

<span data-ttu-id="7a19c-769">해당 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-770">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-770">Definition</span></span>

<span data-ttu-id="7a19c-771">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-772">정규식 `Regex_slovakia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-773">키워드에서 `Keywords_slovakia_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-774">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="7a19c-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-776">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-776">tax id</span></span>
  
<span data-ttu-id="7a19c-777">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-777">tax id number</span></span>
  
<span data-ttu-id="7a19c-778">주석 id</span><span class="sxs-lookup"><span data-stu-id="7a19c-778">tin id</span></span>
  
<span data-ttu-id="7a19c-779">주석 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-779">tin no</span></span>
  
<span data-ttu-id="7a19c-780">슬로바키아어 주석 id</span><span class="sxs-lookup"><span data-stu-id="7a19c-780">slovakian tin id</span></span>
  
<span data-ttu-id="7a19c-781">tin
</span><span class="sxs-lookup"><span data-stu-id="7a19c-781">tin</span></span>
  
<span data-ttu-id="7a19c-782">파일을 더 세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-782">tax file no</span></span>
  
<span data-ttu-id="7a19c-783">

tax file number</span><span class="sxs-lookup"><span data-stu-id="7a19c-783">tax file number</span></span>
  
<span data-ttu-id="7a19c-784">no 세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-784">tax no</span></span>
  
<span data-ttu-id="7a19c-785">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-785">tax number</span></span>
  
<span data-ttu-id="7a19c-786">taxid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-786">taxid#</span></span>
  
<span data-ttu-id="7a19c-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-787">taxno#</span></span>
  
<span data-ttu-id="7a19c-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="7a19c-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="7a19c-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="7a19c-789">daňové číslo</span></span>
  
<span data-ttu-id="7a19c-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="7a19c-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="7a19c-791">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="7a19c-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-792">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-792">Format</span></span>

<span data-ttu-id="7a19c-793">공백이 나 구분 기호 없이 8 개의 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-794">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-794">Pattern</span></span>

<span data-ttu-id="7a19c-795">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a19c-796">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-796">Checksum</span></span>

<span data-ttu-id="7a19c-797">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-798">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-798">Definition</span></span>

<span data-ttu-id="7a19c-799">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-800">다음은 함수 `Func_slovenia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-801">키워드에서 `Keywords_slovenia_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-802">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-803">다음은 함수 `Func_slovenia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_nation_eu_tax_file_number" />
          <Match idRef="Keywords_nation_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-804">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="7a19c-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-806">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-806">tax id</span></span>
  
<span data-ttu-id="7a19c-807">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-807">tax id number</span></span>
  
<span data-ttu-id="7a19c-808">주석 id</span><span class="sxs-lookup"><span data-stu-id="7a19c-808">tin id</span></span>
  
<span data-ttu-id="7a19c-809">주석 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-809">tin no</span></span>
  
<span data-ttu-id="7a19c-810">슬로베니아어 주석 id</span><span class="sxs-lookup"><span data-stu-id="7a19c-810">slovenian tin id</span></span>
  
<span data-ttu-id="7a19c-811">tin
</span><span class="sxs-lookup"><span data-stu-id="7a19c-811">tin</span></span>
  
<span data-ttu-id="7a19c-812">파일을 더 세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-812">tax file no</span></span>
  
<span data-ttu-id="7a19c-813">

tax file number</span><span class="sxs-lookup"><span data-stu-id="7a19c-813">tax file number</span></span>
  
<span data-ttu-id="7a19c-814">no 세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-814">tax no</span></span>
  
<span data-ttu-id="7a19c-815">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-815">tax number</span></span>
  
<span data-ttu-id="7a19c-816">taxid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-816">taxid#</span></span>
  
<span data-ttu-id="7a19c-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-817">taxno#</span></span>
  
<span data-ttu-id="7a19c-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="7a19c-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="7a19c-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="7a19c-819">davčna številka</span></span>
  
<span data-ttu-id="7a19c-820">Številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="7a19c-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="7a19c-821">스페인</span><span class="sxs-lookup"><span data-stu-id="7a19c-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-822">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-822">Format</span></span>

<span data-ttu-id="7a19c-823">7 또는 8 개의 숫자와 지정한 패턴에 하나 또는 두 문자</span><span class="sxs-lookup"><span data-stu-id="7a19c-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-824">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-824">Pattern</span></span>

<span data-ttu-id="7a19c-825">스페인 국가 Id 카드와 스페인어 자연 스러운 사용자:</span><span class="sxs-lookup"><span data-stu-id="7a19c-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="7a19c-826">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-826">Eight digits</span></span> 
    
- <span data-ttu-id="7a19c-827">하나의 대문자 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="7a19c-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="7a19c-828">스페인 국가 Id 카드 없이 비 상주 Spaniards</span><span class="sxs-lookup"><span data-stu-id="7a19c-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="7a19c-829">하나의 대문자 "L" (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="7a19c-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="7a19c-830">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-830">Seven digits</span></span>
    
- <span data-ttu-id="7a19c-831">하나의 대문자 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="7a19c-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="7a19c-832">14 년 없이 스페인 국가 Id 카드의 기간을 아래에서 상주 Spaniards:</span><span class="sxs-lookup"><span data-stu-id="7a19c-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="7a19c-833">하나의 대문자 "K" (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="7a19c-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="7a19c-834">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-834">Seven digits</span></span> 
    
- <span data-ttu-id="7a19c-835">하나의 대문자 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="7a19c-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="7a19c-836">한 말야 Id 번호로 foreigners</span><span class="sxs-lookup"><span data-stu-id="7a19c-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="7a19c-837">"X", "Y" 또는 "Z" (대/소문자 구분) 즉 글자 하나의 대문자</span><span class="sxs-lookup"><span data-stu-id="7a19c-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="7a19c-838">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-838">Seven digits</span></span>
    
- <span data-ttu-id="7a19c-839">하나의 대문자 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="7a19c-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="7a19c-840">Id 번호 말야의 없이 foreigners</span><span class="sxs-lookup"><span data-stu-id="7a19c-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="7a19c-841">"M" (대/소문자 구분)는 하나의 대문자</span><span class="sxs-lookup"><span data-stu-id="7a19c-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="7a19c-842">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-842">Seven digits</span></span>
    
- <span data-ttu-id="7a19c-843">하나의 대문자 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="7a19c-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="7a19c-844">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-844">Checksum</span></span>

<span data-ttu-id="7a19c-845">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-846">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-846">Definition</span></span>

<span data-ttu-id="7a19c-847">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-848">다음은 함수 `Func_spain_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-849">키워드에서 `Keywords_spain_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-850">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-851">다음은 함수 `Func_spain_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
          <Match idRef="Keywords_spain_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-852">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="7a19c-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-854">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-854">tax id</span></span>
  
<span data-ttu-id="7a19c-855">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-855">tax id number</span></span>
  
<span data-ttu-id="7a19c-856">cif id</span><span class="sxs-lookup"><span data-stu-id="7a19c-856">cif id</span></span>
  
<span data-ttu-id="7a19c-857">cif 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-857">cif no</span></span>
  
<span data-ttu-id="7a19c-858">스페인어 cif id</span><span class="sxs-lookup"><span data-stu-id="7a19c-858">spanish cif id</span></span>
  
<span data-ttu-id="7a19c-859">cif</span><span class="sxs-lookup"><span data-stu-id="7a19c-859">cif</span></span>
  
<span data-ttu-id="7a19c-860">파일을 더 세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-860">tax file no</span></span>
  
<span data-ttu-id="7a19c-861">스페인어 cif 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-861">spanish cif number</span></span>
  
<span data-ttu-id="7a19c-862">

tax file number</span><span class="sxs-lookup"><span data-stu-id="7a19c-862">tax file number</span></span>
  
<span data-ttu-id="7a19c-863">스페인어 cif 없음</span><span class="sxs-lookup"><span data-stu-id="7a19c-863">spanish cif no</span></span>
  
<span data-ttu-id="7a19c-864">no 세금</span><span class="sxs-lookup"><span data-stu-id="7a19c-864">tax no</span></span>
  
<span data-ttu-id="7a19c-865">세금 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-865">tax number</span></span>
  
<span data-ttu-id="7a19c-866">taxid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-866">taxid#</span></span>
  
<span data-ttu-id="7a19c-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-867">taxno#</span></span>
  
<span data-ttu-id="7a19c-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-868">cifid#</span></span>
  
<span data-ttu-id="7a19c-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-869">spanishcifid#</span></span>
  
<span data-ttu-id="7a19c-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="7a19c-870">spanishcifno#</span></span>
  
<span data-ttu-id="7a19c-871">número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="7a19c-871">número de contribuyente</span></span>
  
<span data-ttu-id="7a19c-872">número de impuesto corporativo</span><span class="sxs-lookup"><span data-stu-id="7a19c-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="7a19c-873">회계 número de identificación</span><span class="sxs-lookup"><span data-stu-id="7a19c-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="7a19c-874">cif número</span><span class="sxs-lookup"><span data-stu-id="7a19c-874">cif número</span></span>
  
<span data-ttu-id="7a19c-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="7a19c-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="7a19c-876">스웨덴</span><span class="sxs-lookup"><span data-stu-id="7a19c-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-877">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-877">Format</span></span>

<span data-ttu-id="7a19c-878">10 자리 숫자 및 지정된 된 패턴의 기호</span><span class="sxs-lookup"><span data-stu-id="7a19c-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-879">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-879">Pattern</span></span>

<span data-ttu-id="7a19c-880">10 자리 숫자 및 기호:</span><span class="sxs-lookup"><span data-stu-id="7a19c-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="7a19c-881">생일 (YYMMDD)에 해당 하는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="7a19c-882">더하기 기호, 빼기 기호 또는 백슬래시</span><span class="sxs-lookup"><span data-stu-id="7a19c-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="7a19c-883">Id를 구성 하는 세 자리 번호 매기기 고유 위치:</span><span class="sxs-lookup"><span data-stu-id="7a19c-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="7a19c-884">1990 전에 발급 된 번호에 대 한 7 번째 및 여덟 번째 숫자는 생일 또는 foreign-born 사용자의 국가 식별</span><span class="sxs-lookup"><span data-stu-id="7a19c-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="7a19c-885">9 번째 위치에 숫자 1 여자 2 남자 또는 탑재에 대해서도 어느 홀수 하 여 성별을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="7a19c-886">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a19c-887">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-887">Checksum</span></span>

<span data-ttu-id="7a19c-888">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-889">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-889">Definition</span></span>

<span data-ttu-id="7a19c-890">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-891">다음은 함수 `Func_sweden_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-892">키워드에서 `Keywords_sweden_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="7a19c-893">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-894">다음은 함수 `Func_sweden_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
          <Match idRef="Keywords_sweden_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-895">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="7a19c-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-897">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-897">tax id</span></span>
  
<span data-ttu-id="7a19c-898">id를 더 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-898">tax id no.</span></span>
  
<span data-ttu-id="7a19c-899">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-899">tax id number</span></span>
  
<span data-ttu-id="7a19c-900">tax identification
</span><span class="sxs-lookup"><span data-stu-id="7a19c-900">tax identification</span></span>
  
<span data-ttu-id="7a19c-901">세금 식별 #</span><span class="sxs-lookup"><span data-stu-id="7a19c-901">tax identification#</span></span>
  
<span data-ttu-id="7a19c-902">no를 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-902">tax no.</span></span>
  
<span data-ttu-id="7a19c-903">세금 #</span><span class="sxs-lookup"><span data-stu-id="7a19c-903">tax#</span></span>
  
<span data-ttu-id="7a19c-904">taxid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-904">taxid#</span></span>
  
<span data-ttu-id="7a19c-905">세금 파일</span><span class="sxs-lookup"><span data-stu-id="7a19c-905">tax file</span></span>
  
<span data-ttu-id="7a19c-906">파일을 더 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-906">tax file no.</span></span>
  
<span data-ttu-id="7a19c-907">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-907">personal id number</span></span>
  
<span data-ttu-id="7a19c-908">skatt id nummer</span><span class="sxs-lookup"><span data-stu-id="7a19c-908">skatt id nummer</span></span>
  
<span data-ttu-id="7a19c-909">skatt identifikation</span><span class="sxs-lookup"><span data-stu-id="7a19c-909">skatt identifikation</span></span>
  
<span data-ttu-id="7a19c-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="7a19c-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="7a19c-911">영국</span><span class="sxs-lookup"><span data-stu-id="7a19c-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="7a19c-912">형식</span><span class="sxs-lookup"><span data-stu-id="7a19c-912">Format</span></span>

<span data-ttu-id="7a19c-913">공백 및 구분 기호 없이 10 자리 고유 납세자 참조 (UTR):</span><span class="sxs-lookup"><span data-stu-id="7a19c-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="7a19c-p103">국가별 보험 번호 (NINO): 자세한 내용은의 섹션을 참조 "영국 National 보험 번호 (NINO)" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-p103">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a19c-916">패턴</span><span class="sxs-lookup"><span data-stu-id="7a19c-916">Pattern</span></span>

<span data-ttu-id="7a19c-917">고유 납세자 참조 (UTR): 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="7a19c-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="7a19c-p104">국가별 보험 번호 (NINO): 자세한 내용은의 섹션을 참조 "영국 National 보험 번호 (NINO)" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-p104">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a19c-920">체크섬</span><span class="sxs-lookup"><span data-stu-id="7a19c-920">Checksum</span></span>

<span data-ttu-id="7a19c-921">예</span><span class="sxs-lookup"><span data-stu-id="7a19c-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a19c-922">정의</span><span class="sxs-lookup"><span data-stu-id="7a19c-922">Definition</span></span>

<span data-ttu-id="7a19c-923">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a19c-924">다음은 함수 `Func_uk_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a19c-925">키워드에서 `Keywords_uk_eu_tax_file_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a19c-926">키워드</span><span class="sxs-lookup"><span data-stu-id="7a19c-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="7a19c-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="7a19c-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="7a19c-928">tax id
</span><span class="sxs-lookup"><span data-stu-id="7a19c-928">tax id</span></span>
  
<span data-ttu-id="7a19c-929">id를 더 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-929">tax id no.</span></span>
  
<span data-ttu-id="7a19c-930">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="7a19c-930">tax id number</span></span>
  
<span data-ttu-id="7a19c-931">tax identification
</span><span class="sxs-lookup"><span data-stu-id="7a19c-931">tax identification</span></span>
  
<span data-ttu-id="7a19c-932">세금 식별 #</span><span class="sxs-lookup"><span data-stu-id="7a19c-932">tax identification#</span></span>
  
<span data-ttu-id="7a19c-933">no를 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-933">tax no.</span></span>
  
<span data-ttu-id="7a19c-934">세금 #</span><span class="sxs-lookup"><span data-stu-id="7a19c-934">tax#</span></span>
  
<span data-ttu-id="7a19c-935">taxid #</span><span class="sxs-lookup"><span data-stu-id="7a19c-935">taxid#</span></span>
  
<span data-ttu-id="7a19c-936">세금 파일</span><span class="sxs-lookup"><span data-stu-id="7a19c-936">tax file</span></span>
  
<span data-ttu-id="7a19c-937">파일을 더 세금 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a19c-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7a19c-938">참고 항목</span><span class="sxs-lookup"><span data-stu-id="7a19c-938">See also</span></span>

[<span data-ttu-id="7a19c-939">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="7a19c-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

